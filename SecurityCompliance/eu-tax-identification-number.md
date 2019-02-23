---
title: EU 세금 확인 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: 이 항목에서는 EU 세금 식별 번호 중요 정보 유형을 검색할 때 DLP (데이터 손실 방지) 정책이 어떤 역할을 검색 하나요를 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: f851cce4be70fd41c24a7876d97c452f0a738eda
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213828"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="bbc18-104">EU 세금 확인 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-104">EU Tax Identification Number</span></span>

<span data-ttu-id="bbc18-p102">이 항목에서는 언급 (데이터 손실 방지) 정책이 EU (유럽 세금 식별 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="bbc18-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="bbc18-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-108">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-108">Format</span></span>

<span data-ttu-id="bbc18-109">하이픈 및 슬래시가 있는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-110">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-110">Pattern</span></span>

<span data-ttu-id="bbc18-111">하이픈 및 슬래시가 있는 9 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="bbc18-112">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-112">Two digits</span></span> 
    
- <span data-ttu-id="bbc18-113">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="bbc18-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="bbc18-114">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-114">Three digits</span></span>
    
- <span data-ttu-id="bbc18-115">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="bbc18-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="bbc18-116">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-117">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-117">Checksum</span></span>

<span data-ttu-id="bbc18-118">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-119">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-119">Definition</span></span>

<span data-ttu-id="bbc18-120">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-121">이 함수 `Func_austria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-122">from `Keywords_austria_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-123">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-124">이 함수 `Func_austria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-125">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="bbc18-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-127">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-127">tax number</span></span>
  
<span data-ttu-id="bbc18-128">수</span><span class="sxs-lookup"><span data-stu-id="bbc18-128">number</span></span>
  
<span data-ttu-id="bbc18-129">세금 등록 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-129">tax registration number</span></span>
  
<span data-ttu-id="bbc18-130">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-130">tax id</span></span>
  
<span data-ttu-id="bbc18-131">st.nr</span><span class="sxs-lookup"><span data-stu-id="bbc18-131">st.nr.</span></span>
  
<span data-ttu-id="bbc18-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="bbc18-133">벨기에</span><span class="sxs-lookup"><span data-stu-id="bbc18-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-134">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-134">Format</span></span>

<span data-ttu-id="bbc18-135">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-136">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-136">Pattern</span></span>

<span data-ttu-id="bbc18-137">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-137">11 digits:</span></span>
  
- <span data-ttu-id="bbc18-138">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-138">Two digits</span></span>
    
- <span data-ttu-id="bbc18-139">"0" 또는 "1"</span><span class="sxs-lookup"><span data-stu-id="bbc18-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="bbc18-140">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-140">One digit</span></span>
    
- <span data-ttu-id="bbc18-141">"0" 또는 "1" 또는 "2" 또는 "3"</span><span class="sxs-lookup"><span data-stu-id="bbc18-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="bbc18-142">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-143">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-143">Checksum</span></span>

<span data-ttu-id="bbc18-144">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-145">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-145">Definition</span></span>

<span data-ttu-id="bbc18-146">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-147">정규식이 해당 `Regex_belgium_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-148">from `Keywords_belgium_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bbc18-149">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="bbc18-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-151">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-151">tax number</span></span>
  
<span data-ttu-id="bbc18-152">국가 등록 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-152">national registration number</span></span>
  
<span data-ttu-id="bbc18-153">세금 등록 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-153">tax registration number</span></span>
  
<span data-ttu-id="bbc18-154">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-154">tax id</span></span>
  
<span data-ttu-id="bbc18-155">m</span><span class="sxs-lookup"><span data-stu-id="bbc18-155">nif</span></span>
  
<span data-ttu-id="bbc18-156">m</span><span class="sxs-lookup"><span data-stu-id="bbc18-156">nif#</span></span>
  
<span data-ttu-id="bbc18-157">numéro de registre 국립</span><span class="sxs-lookup"><span data-stu-id="bbc18-157">numéro de registre national</span></span>
  
<span data-ttu-id="bbc18-158">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="bbc18-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="bbc18-159">불가리아</span><span class="sxs-lookup"><span data-stu-id="bbc18-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-160">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-160">Format</span></span>

<span data-ttu-id="bbc18-161">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-162">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-162">Pattern</span></span>

<span data-ttu-id="bbc18-163">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-164">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-164">Checksum</span></span>

<span data-ttu-id="bbc18-165">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-166">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-166">Definition</span></span>

<span data-ttu-id="bbc18-167">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-168">이 함수 `Func_bulgaria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-169">from `Keywords_bulgaria_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-170">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-171">이 함수 `Func_bulgaria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-172">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="bbc18-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-174">고 대 cn</span><span class="sxs-lookup"><span data-stu-id="bbc18-174">bucn</span></span>
  
<span data-ttu-id="bbc18-175">일관적인 민사 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-175">uniform civil number</span></span>
  
<span data-ttu-id="bbc18-176">과 (와) cn #</span><span class="sxs-lookup"><span data-stu-id="bbc18-176">bucn#</span></span>
  
<span data-ttu-id="bbc18-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="bbc18-178">일정 한 민사 일련번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-178">uniform civil id</span></span>
  
<span data-ttu-id="bbc18-179">일관적인 민사</span><span class="sxs-lookup"><span data-stu-id="bbc18-179">uniform civil no</span></span>
  
<span data-ttu-id="bbc18-180">egn</span><span class="sxs-lookup"><span data-stu-id="bbc18-180">egn</span></span>
  
<span data-ttu-id="bbc18-181">불가리아어 (민사)</span><span class="sxs-lookup"><span data-stu-id="bbc18-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="bbc18-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-182">uniformcivilno#</span></span>
  
<span data-ttu-id="bbc18-183">egn #</span><span class="sxs-lookup"><span data-stu-id="bbc18-183">egn#</span></span>
  
<span data-ttu-id="bbc18-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="bbc18-184">униформ граждански номер</span></span>
  
<span data-ttu-id="bbc18-185">униформ id</span><span class="sxs-lookup"><span data-stu-id="bbc18-185">униформ id</span></span>
  
<span data-ttu-id="bbc18-186">униформ граждански id</span><span class="sxs-lookup"><span data-stu-id="bbc18-186">униформ граждански id</span></span>
  
<span data-ttu-id="bbc18-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="bbc18-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="bbc18-188">크로아티아</span><span class="sxs-lookup"><span data-stu-id="bbc18-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-189">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-189">Format</span></span>

<span data-ttu-id="bbc18-190">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-191">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-191">Pattern</span></span>

<span data-ttu-id="bbc18-192">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-192">11 digits:</span></span>
  
- <span data-ttu-id="bbc18-193">임의로 선택한 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="bbc18-194">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="bbc18-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-195">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-195">Checksum</span></span>

<span data-ttu-id="bbc18-196">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-197">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-197">Definition</span></span>

<span data-ttu-id="bbc18-198">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-199">이 함수 `Func_croatia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-200">from `Keywords_croatia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-202">이 함수 `Func_croatia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-203">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="bbc18-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-205">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-205">tax number</span></span>
  
<span data-ttu-id="bbc18-206">세금</span><span class="sxs-lookup"><span data-stu-id="bbc18-206">tax</span></span>
  
<span data-ttu-id="bbc18-207">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-207">tax id</span></span>
  
<span data-ttu-id="bbc18-208">원환형</span><span class="sxs-lookup"><span data-stu-id="bbc18-208">oid</span></span>
  
<span data-ttu-id="bbc18-209">원환형</span><span class="sxs-lookup"><span data-stu-id="bbc18-209">oid#</span></span>
  
<span data-ttu-id="bbc18-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="bbc18-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="bbc18-211">키프로스</span><span class="sxs-lookup"><span data-stu-id="bbc18-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-212">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-212">Format</span></span>

<span data-ttu-id="bbc18-213">지정 된 패턴에서 8 자리 및 1 개 문자</span><span class="sxs-lookup"><span data-stu-id="bbc18-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-214">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-214">Pattern</span></span>

<span data-ttu-id="bbc18-215">8 자리 숫자와 1 개 문자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="bbc18-216">"0"</span><span class="sxs-lookup"><span data-stu-id="bbc18-216">A "0"</span></span> 
    
- <span data-ttu-id="bbc18-217">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-217">Seven digits</span></span>
    
- <span data-ttu-id="bbc18-218">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="bbc18-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-219">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-219">Checksum</span></span>

<span data-ttu-id="bbc18-220">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-221">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-221">Definition</span></span>

<span data-ttu-id="bbc18-222">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-223">이 함수 `Func_cyprus_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-224">from `Keywords_cyprus_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-225">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-226">이 함수 `Func_cyprus_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-227">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="bbc18-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-229">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-229">tax number</span></span>
  
<span data-ttu-id="bbc18-230">세금</span><span class="sxs-lookup"><span data-stu-id="bbc18-230">tax</span></span>
  
<span data-ttu-id="bbc18-231">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-231">tax id</span></span>
  
<span data-ttu-id="bbc18-232">세금 식별 코드</span><span class="sxs-lookup"><span data-stu-id="bbc18-232">tax identification code</span></span>
  
<span data-ttu-id="bbc18-233">tic</span><span class="sxs-lookup"><span data-stu-id="bbc18-233">tic</span></span>
  
<span data-ttu-id="bbc18-234">tic #</span><span class="sxs-lookup"><span data-stu-id="bbc18-234">tic#</span></span>
  
<span data-ttu-id="bbc18-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="bbc18-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="bbc18-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="bbc18-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="bbc18-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="bbc18-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="bbc18-238">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="bbc18-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-239">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-239">Format</span></span>

<span data-ttu-id="bbc18-240">선택적 백슬래시가 있는 9 자리 또는 10 진수</span><span class="sxs-lookup"><span data-stu-id="bbc18-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-241">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-241">Pattern</span></span>

<span data-ttu-id="bbc18-242">선택적 backslashl이 있는 아홉 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="bbc18-243">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-243">Six digits</span></span> 
    
- <span data-ttu-id="bbc18-244">백슬래시 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="bbc18-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="bbc18-245">3 ~ 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-246">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-246">Checksum</span></span>

<span data-ttu-id="bbc18-247">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-248">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-248">Definition</span></span>

<span data-ttu-id="bbc18-249">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-250">정규식이 해당 `Regex_czech_republic_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-251">from `Keywords_czech_republic_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bbc18-252">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="bbc18-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-254">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-254">tax number</span></span>
  
<span data-ttu-id="bbc18-255">세금</span><span class="sxs-lookup"><span data-stu-id="bbc18-255">tax</span></span>
  
<span data-ttu-id="bbc18-256">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-256">tax id</span></span>
  
<span data-ttu-id="bbc18-257">개인 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-257">personal number</span></span>
  
<span data-ttu-id="bbc18-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="bbc18-258">daňové číslo</span></span>
  
<span data-ttu-id="bbc18-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="bbc18-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="bbc18-260">덴마크</span><span class="sxs-lookup"><span data-stu-id="bbc18-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-261">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-261">Format</span></span>

<span data-ttu-id="bbc18-262">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-263">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-263">Pattern</span></span>

<span data-ttu-id="bbc18-264">hyphenl를 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="bbc18-265">생년월일에 해당 하는 6 자리 숫자 (ddmmyy)</span><span class="sxs-lookup"><span data-stu-id="bbc18-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="bbc18-266">하이픈</span><span class="sxs-lookup"><span data-stu-id="bbc18-266">A hyphen</span></span>
    
- <span data-ttu-id="bbc18-267">첫 번째 숫자가 출생 세기에 해당 하 고 마지막 숫자가 개별 성별에 해당 하는 시퀀스 번호에 해당 하는 4 자리 숫자 (남성의 경우 홀수 및 암에도 해당)</span><span class="sxs-lookup"><span data-stu-id="bbc18-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-268">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-268">Checksum</span></span>

<span data-ttu-id="bbc18-269">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-270">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-270">Definition</span></span>

<span data-ttu-id="bbc18-271">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-272">이 함수 `Func_denmark_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-273">from `Keywords_denmark_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-275">이 함수 `Func_denmark_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-276">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="bbc18-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-278">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-278">tax number</span></span>
  
<span data-ttu-id="bbc18-279">세금</span><span class="sxs-lookup"><span data-stu-id="bbc18-279">tax</span></span>
  
<span data-ttu-id="bbc18-280">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-280">tax id</span></span>
  
<span data-ttu-id="bbc18-281">cpr 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-281">cpr number</span></span>
  
<span data-ttu-id="bbc18-282">cpr #</span><span class="sxs-lookup"><span data-stu-id="bbc18-282">cpr#</span></span>
  
<span data-ttu-id="bbc18-283">nummer에서</span><span class="sxs-lookup"><span data-stu-id="bbc18-283">skat nummer</span></span>
  
<span data-ttu-id="bbc18-284">번호 (|)</span><span class="sxs-lookup"><span data-stu-id="bbc18-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="bbc18-285">에스토니아</span><span class="sxs-lookup"><span data-stu-id="bbc18-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-286">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-286">Format</span></span>

<span data-ttu-id="bbc18-287">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-288">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-288">Pattern</span></span>

<span data-ttu-id="bbc18-289">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-289">11 digits:</span></span>
  
-  <span data-ttu-id="bbc18-290">성별에 해당 하는 숫자와 홀수로 해당 하 고, 홀수를 지정 하 여 19th 세기에 대해 1, 2를 나타내는 숫자입니다. 3, 20th 세기에 대해 4를 적용 합니다. 21 세기에 대해 5, 6</span><span class="sxs-lookup"><span data-stu-id="bbc18-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="bbc18-291">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="bbc18-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="bbc18-292">같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="bbc18-293">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="bbc18-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-294">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-294">Checksum</span></span>

<span data-ttu-id="bbc18-295">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-296">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-296">Definition</span></span>

<span data-ttu-id="bbc18-297">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-298">이 함수 `Func_estonia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-299">from `Keywords_estonia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-300">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-301">이 함수 `Func_estonia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-302">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="bbc18-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-304">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-304">tax number</span></span>
  
<span data-ttu-id="bbc18-305">세금</span><span class="sxs-lookup"><span data-stu-id="bbc18-305">tax</span></span>
  
<span data-ttu-id="bbc18-306">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-306">tax id</span></span>
  
<span data-ttu-id="bbc18-307">개인 코드</span><span class="sxs-lookup"><span data-stu-id="bbc18-307">personal code</span></span>
  
<span data-ttu-id="bbc18-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-308">maksunumber</span></span>
  
<span data-ttu-id="bbc18-309">maksu id</span><span class="sxs-lookup"><span data-stu-id="bbc18-309">maksu id</span></span>
  
<span data-ttu-id="bbc18-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="bbc18-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="bbc18-311">핀란드</span><span class="sxs-lookup"><span data-stu-id="bbc18-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-312">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-312">Format</span></span>

<span data-ttu-id="bbc18-313">숫자, 문자, 더하기 및 빼기 기호를 11 문자로 조합</span><span class="sxs-lookup"><span data-stu-id="bbc18-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-314">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-314">Pattern</span></span>

<span data-ttu-id="bbc18-315">숫자, 문자, 더하기 및 빼기 기호를 11 문자로 조합한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="bbc18-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-316">Six digits</span></span>
    
- <span data-ttu-id="bbc18-317">더하기 기호, 빼기 기호 또는 + 기호가 1800-1899 사이에 태어난 것을 의미 하는 "a" (대/소문자 구분 안 함), 빼기 기호는 1900-1999 사이에 출생를 의미 하며 "a"는 "a"를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="bbc18-318">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-318">Three digits</span></span>
    
- <span data-ttu-id="bbc18-319">1 개의 문자 또는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-320">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-320">Checksum</span></span>

<span data-ttu-id="bbc18-321">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-322">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-322">Definition</span></span>

<span data-ttu-id="bbc18-323">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-324">이 함수 `Func_finland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-325">from `Keywords_finland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-326">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-327">이 함수 `Func_finland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-328">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="bbc18-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-330">identification number
</span><span class="sxs-lookup"><span data-stu-id="bbc18-330">identification number</span></span>
  
<span data-ttu-id="bbc18-331">개인 id</span><span class="sxs-lookup"><span data-stu-id="bbc18-331">personal id</span></span>
  
<span data-ttu-id="bbc18-332">id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-332">identity number</span></span>
  
<span data-ttu-id="bbc18-333">핀란드어 국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-333">finnish national id number</span></span>
  
<span data-ttu-id="bbc18-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-334">personalidnumber#</span></span>
  
<span data-ttu-id="bbc18-335">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-335">national identification number</span></span>
  
<span data-ttu-id="bbc18-336">id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-336">id number</span></span>
  
<span data-ttu-id="bbc18-337">국가 id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-337">national id no.</span></span>
  
<span data-ttu-id="bbc18-338">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-338">national id number</span></span>
  
<span data-ttu-id="bbc18-339">id 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-339">id no</span></span>
  
<span data-ttu-id="bbc18-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="bbc18-340">tunnistenumero</span></span>
  
<span data-ttu-id="bbc18-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="bbc18-341">henkilötunnus</span></span>
  
<span data-ttu-id="bbc18-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="bbc18-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="bbc18-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="bbc18-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="bbc18-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="bbc18-344">identiteetti numero</span></span>
  
<span data-ttu-id="bbc18-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="bbc18-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="bbc18-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="bbc18-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="bbc18-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="bbc18-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="bbc18-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="bbc18-348">tunnusnumero</span></span>
  
<span data-ttu-id="bbc18-349">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="bbc18-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="bbc18-350">프랑스</span><span class="sxs-lookup"><span data-stu-id="bbc18-350">France</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-351">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-351">Format</span></span>

<span data-ttu-id="bbc18-352">개별 사용자의 경우 13 자리 숫자 및 엔터티의 경우 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-353">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-353">Pattern</span></span>

<span data-ttu-id="bbc18-354">개별 사용자에 대 한 13 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="bbc18-355">0, 1, 2 또는 3 이어야 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="bbc18-356">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-356">12 digits</span></span>
    
<span data-ttu-id="bbc18-357">엔터티의 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-358">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-358">Checksum</span></span>

<span data-ttu-id="bbc18-359">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-360">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-360">Definition</span></span>

<span data-ttu-id="bbc18-361">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-362">이 함수 `Func_france_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-363">from `Keywords_france_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-365">이 함수 `Func_france_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-366">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="bbc18-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-368">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-368">tax identification number</span></span>
  
<span data-ttu-id="bbc18-369">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-369">tax number</span></span>
  
<span data-ttu-id="bbc18-370">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-370">tax id</span></span>
  
<span data-ttu-id="bbc18-371">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="bbc18-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="bbc18-372">독일</span><span class="sxs-lookup"><span data-stu-id="bbc18-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-373">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-373">Format</span></span>

<span data-ttu-id="bbc18-374">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-375">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-375">Pattern</span></span>

<span data-ttu-id="bbc18-376">11 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-376">11 digits :</span></span>
  
-  <span data-ttu-id="bbc18-377">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-377">Ten digits</span></span> 
    
- <span data-ttu-id="bbc18-378">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="bbc18-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-379">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-379">Checksum</span></span>

<span data-ttu-id="bbc18-380">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-381">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-381">Definition</span></span>

<span data-ttu-id="bbc18-382">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-383">이 함수 `Func_germany_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-384">from `Keywords_germany_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-385">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-386">이 함수 `Func_germany_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-387">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="bbc18-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-389">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-389">tax number</span></span>
  
<span data-ttu-id="bbc18-390">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-390">tax no.</span></span>
  
<span data-ttu-id="bbc18-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-391">taxno#</span></span>
  
<span data-ttu-id="bbc18-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-392">taxnumber#</span></span>
  
<span data-ttu-id="bbc18-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-393">taxnumber</span></span>
  
<span data-ttu-id="bbc18-394">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-394">tax id</span></span>
  
<span data-ttu-id="bbc18-395">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-395">taxid#</span></span>
  
<span data-ttu-id="bbc18-396">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-396">tax identification number</span></span>
  
<span data-ttu-id="bbc18-397">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-397">tax identification no.</span></span>
  
<span data-ttu-id="bbc18-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-398">steuernummer</span></span>
  
<span data-ttu-id="bbc18-399">steuer id</span><span class="sxs-lookup"><span data-stu-id="bbc18-399">steuer id</span></span>
  
<span data-ttu-id="bbc18-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="bbc18-401">그리스</span><span class="sxs-lookup"><span data-stu-id="bbc18-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-402">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-402">Format</span></span>

<span data-ttu-id="bbc18-403">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-404">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-404">Pattern</span></span>

<span data-ttu-id="bbc18-405">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-406">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-406">Checksum</span></span>

<span data-ttu-id="bbc18-407">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-408">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-408">Definition</span></span>

<span data-ttu-id="bbc18-409">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-410">정규식이 해당 `Regex_greece_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-411">from `Keywords_greece_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bbc18-412">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="bbc18-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-414">afm</span><span class="sxs-lookup"><span data-stu-id="bbc18-414">afm</span></span>
  
<span data-ttu-id="bbc18-415">tin
</span><span class="sxs-lookup"><span data-stu-id="bbc18-415">tin</span></span>
  
<span data-ttu-id="bbc18-416">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-416">tax id no.</span></span>
  
<span data-ttu-id="bbc18-417">세금 번호 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-417">tax id no</span></span>
  
<span data-ttu-id="bbc18-418">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-418">tax identification number</span></span>
  
<span data-ttu-id="bbc18-419">세금 레지스트리 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-419">tax registry number</span></span>
  
<span data-ttu-id="bbc18-420">세금 레지스트리 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-420">tax registry no.</span></span>
  
<span data-ttu-id="bbc18-421">afm #</span><span class="sxs-lookup"><span data-stu-id="bbc18-421">afm#</span></span>
  
<span data-ttu-id="bbc18-422">언급</span><span class="sxs-lookup"><span data-stu-id="bbc18-422">tin#</span></span>
  
<span data-ttu-id="bbc18-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-423">taxidno#</span></span>
  
<span data-ttu-id="bbc18-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-424">taxregistryno#</span></span>
  
<span data-ttu-id="bbc18-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="bbc18-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="bbc18-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="bbc18-426">aφμ</span></span>
  
<span data-ttu-id="bbc18-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="bbc18-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="bbc18-428">φορολογικού μητρώου νο</span><span class="sxs-lookup"><span data-stu-id="bbc18-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="bbc18-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="bbc18-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="bbc18-430">헝가리</span><span class="sxs-lookup"><span data-stu-id="bbc18-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-431">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-431">Format</span></span>

<span data-ttu-id="bbc18-432">공백이 나 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-433">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-433">Pattern</span></span>

<span data-ttu-id="bbc18-434">10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-434">Ten digits:</span></span>
  
-  <span data-ttu-id="bbc18-435">"8" 이어야 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="bbc18-436">날짜 01/01/1867과 개별 생년월일 사이의 일 수에 해당 하는 5 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="bbc18-437">같은 날에 태어난 사람을 구별 하기 위해 기회가 만든 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="bbc18-438">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="bbc18-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-439">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-439">Checksum</span></span>

<span data-ttu-id="bbc18-440">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-441">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-441">Definition</span></span>

<span data-ttu-id="bbc18-442">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-443">이 함수 `Func_hungary_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-444">from `Keywords_hungary_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-445">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-446">이 함수 `Func_hungary_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-447">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="bbc18-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-449">헝가리어 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="bbc18-450">헝가리어 언급</span><span class="sxs-lookup"><span data-stu-id="bbc18-450">hungarian tin</span></span>
  
<span data-ttu-id="bbc18-451">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-451">tax id number</span></span>
  
<span data-ttu-id="bbc18-452">vat 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-452">vat number</span></span>
  
<span data-ttu-id="bbc18-453">세금 기관 아니요</span><span class="sxs-lookup"><span data-stu-id="bbc18-453">tax authority no</span></span>
  
<span data-ttu-id="bbc18-454">세금 id 세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-454">tax id tax identity number</span></span>
  
<span data-ttu-id="bbc18-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-455">taxidnumber#</span></span>
  
<span data-ttu-id="bbc18-456">언급</span><span class="sxs-lookup"><span data-stu-id="bbc18-456">tin#</span></span>
  
<span data-ttu-id="bbc18-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="bbc18-457">hungatiantin#</span></span>
  
<span data-ttu-id="bbc18-458">세금 식별 아니요</span><span class="sxs-lookup"><span data-stu-id="bbc18-458">tax identification no</span></span>
  
<span data-ttu-id="bbc18-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-459">taxidno#</span></span>
  
<span data-ttu-id="bbc18-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="bbc18-460">adóazonosító szám</span></span>
  
<span data-ttu-id="bbc18-461">adószám</span><span class="sxs-lookup"><span data-stu-id="bbc18-461">adószám</span></span>
  
<span data-ttu-id="bbc18-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="bbc18-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="bbc18-463">Ireland</span><span class="sxs-lookup"><span data-stu-id="bbc18-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-464">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-464">Format</span></span>

<span data-ttu-id="bbc18-465">공백 또는 구분 기호가 없는 7 자리 숫자와 문자</span><span class="sxs-lookup"><span data-stu-id="bbc18-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-466">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-466">Pattern</span></span>

<span data-ttu-id="bbc18-467">7 자리 숫자와 문자</span><span class="sxs-lookup"><span data-stu-id="bbc18-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="bbc18-468">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-468">Seven digits</span></span> 
    
- <span data-ttu-id="bbc18-469">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="bbc18-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-470">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-470">Checksum</span></span>

<span data-ttu-id="bbc18-471">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-472">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-472">Definition</span></span>

<span data-ttu-id="bbc18-473">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-474">이 함수 `Func_ireland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-475">from `Keywords_ireland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-476">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-477">이 함수 `Func_ireland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-478">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="bbc18-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-480">공용 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-480">public service no</span></span>
  
<span data-ttu-id="bbc18-481">개인 공용 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-481">personal public service no</span></span>
  
<span data-ttu-id="bbc18-482">pps 아니요</span><span class="sxs-lookup"><span data-stu-id="bbc18-482">pps no</span></span>
  
<span data-ttu-id="bbc18-483">개인 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-483">personal service no</span></span>
  
<span data-ttu-id="bbc18-484">pps 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-484">pps service no</span></span>
  
<span data-ttu-id="bbc18-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-485">ppsno#</span></span>
  
<span data-ttu-id="bbc18-486">아일랜드 pps 아니요</span><span class="sxs-lookup"><span data-stu-id="bbc18-486">irish pps no</span></span>
  
<span data-ttu-id="bbc18-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-487">publicserviceno#</span></span>
  
<span data-ttu-id="bbc18-488">개인 공용 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-488">personal public service number</span></span>
  
<span data-ttu-id="bbc18-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="bbc18-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="bbc18-490">pps uimh</span><span class="sxs-lookup"><span data-stu-id="bbc18-490">pps uimh</span></span>
  
<span data-ttu-id="bbc18-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="bbc18-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="bbc18-492">이탈리아</span><span class="sxs-lookup"><span data-stu-id="bbc18-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-493">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-493">Format</span></span>

<span data-ttu-id="bbc18-494">지정 된 패턴의 문자와 숫자 16 개</span><span class="sxs-lookup"><span data-stu-id="bbc18-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-495">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-495">Pattern</span></span>

<span data-ttu-id="bbc18-496">16 자의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="bbc18-497">가족 이름에서 처음 세 개의 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="bbc18-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="bbc18-498">이름의 첫 번째, 세 번째 및 네 번째 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="bbc18-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="bbc18-499">출생 연도의 마지막 자리에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="bbc18-500">출생 달에 해당 하는 1 자리 숫자는 알파벳 순으로 사용 되지만 a에서 E, H, L, M, P, R에 해당 하는 문자만 사용 되며, 따라서 1 월은 a와 10 월이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="bbc18-501">남성의와 구별 하기 위해 여성의 경우 짝수에서 출생 일에 40이 추가 되는 출생 달의 날짜에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="bbc18-502">사용자가 태어난 municipality 관련 지역 번호에 해당 하는 4 자리 숫자-국가 전체 코드를 외국 국가에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="bbc18-503">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="bbc18-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-504">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-504">Checksum</span></span>

<span data-ttu-id="bbc18-505">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-506">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-506">Definition</span></span>

<span data-ttu-id="bbc18-507">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-508">이 함수 `Func_italy_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-509">from `Keywords_italy_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-510">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-511">이 함수 `Func_italy_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-512">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="bbc18-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-514">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-514">tax number</span></span>
  
<span data-ttu-id="bbc18-515">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-515">tax no.</span></span>
  
<span data-ttu-id="bbc18-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-516">taxno#</span></span>
  
<span data-ttu-id="bbc18-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-517">taxnumber#</span></span>
  
<span data-ttu-id="bbc18-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-518">taxnumber</span></span>
  
<span data-ttu-id="bbc18-519">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-519">tax id</span></span>
  
<span data-ttu-id="bbc18-520">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-520">taxid#</span></span>
  
<span data-ttu-id="bbc18-521">회계 코드</span><span class="sxs-lookup"><span data-stu-id="bbc18-521">fiscal code</span></span>
  
<span data-ttu-id="bbc18-522">codice</span><span class="sxs-lookup"><span data-stu-id="bbc18-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="bbc18-523">라트비아</span><span class="sxs-lookup"><span data-stu-id="bbc18-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-524">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-524">Format</span></span>

<span data-ttu-id="bbc18-525">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-526">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-526">Pattern</span></span>

<span data-ttu-id="bbc18-527">지정 된 패턴에서 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="bbc18-528">출생 날짜에 해당 하는 6 자리 숫자 (ddmmyy)</span><span class="sxs-lookup"><span data-stu-id="bbc18-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="bbc18-529">출생 세기에 해당 하는 1 자리 숫자 이며, "0"은 19th 세기에 해당 하 고 "1"은 20th 세기에 해당 하며 21 세기에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="bbc18-530">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-531">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-531">Checksum</span></span>

<span data-ttu-id="bbc18-532">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-533">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-533">Definition</span></span>

<span data-ttu-id="bbc18-534">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-535">이 함수 `Func_latvia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-536">from `Keywords_latvia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-537">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-538">이 함수 `Func_latvia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-539">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="bbc18-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-541">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-541">tax number</span></span>
  
<span data-ttu-id="bbc18-542">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-542">tax no.</span></span>
  
<span data-ttu-id="bbc18-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-543">taxno#</span></span>
  
<span data-ttu-id="bbc18-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-544">taxnumber#</span></span>
  
<span data-ttu-id="bbc18-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-545">taxnumber</span></span>
  
<span data-ttu-id="bbc18-546">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-546">tax id</span></span>
  
<span data-ttu-id="bbc18-547">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-547">taxid#</span></span>
  
<span data-ttu-id="bbc18-548">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-548">tax identification number</span></span>
  
<span data-ttu-id="bbc18-549">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-549">tax identification no.</span></span>
  
<span data-ttu-id="bbc18-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="bbc18-550">nodokļa numurs</span></span>
  
<span data-ttu-id="bbc18-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="bbc18-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="bbc18-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="bbc18-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="bbc18-553">리투아니아</span><span class="sxs-lookup"><span data-stu-id="bbc18-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-554">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-554">Format</span></span>

<span data-ttu-id="bbc18-555">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-556">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-556">Pattern</span></span>

<span data-ttu-id="bbc18-557">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-558">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-558">Checksum</span></span>

<span data-ttu-id="bbc18-559">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-560">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-560">Definition</span></span>

<span data-ttu-id="bbc18-561">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-562">이 함수 `Func_lithuania_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-563">from `Keywords_lithuania_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-564">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-565">이 함수 `Func_lithuania_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-566">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="bbc18-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-568">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-568">tax number</span></span>
  
<span data-ttu-id="bbc18-569">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-569">tax no.</span></span>
  
<span data-ttu-id="bbc18-570">세금 없음 #</span><span class="sxs-lookup"><span data-stu-id="bbc18-570">tax no#</span></span>
  
<span data-ttu-id="bbc18-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-571">taxnumber#</span></span>
  
<span data-ttu-id="bbc18-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-572">taxnumber</span></span>
  
<span data-ttu-id="bbc18-573">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-573">tax id</span></span>
  
<span data-ttu-id="bbc18-574">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-574">taxid#</span></span>
  
<span data-ttu-id="bbc18-575">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-575">tax identification number</span></span>
  
<span data-ttu-id="bbc18-576">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-576">tax identification no.</span></span>
  
<span data-ttu-id="bbc18-577">mokesčių id</span><span class="sxs-lookup"><span data-stu-id="bbc18-577">mokesčių id</span></span>
  
<span data-ttu-id="bbc18-578">mokesčių numeris</span><span class="sxs-lookup"><span data-stu-id="bbc18-578">mokesčių numeris</span></span>
  
<span data-ttu-id="bbc18-579">mokesčių identifikavimas numeris</span><span class="sxs-lookup"><span data-stu-id="bbc18-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="bbc18-580">셈</span><span class="sxs-lookup"><span data-stu-id="bbc18-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-581">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-581">Format</span></span>

<span data-ttu-id="bbc18-582">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-583">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-583">Pattern</span></span>

<span data-ttu-id="bbc18-584">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="bbc18-584">13 digits:</span></span>
  
-  <span data-ttu-id="bbc18-585">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-585">11 digits</span></span> 
    
- <span data-ttu-id="bbc18-586">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-587">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-587">Checksum</span></span>

<span data-ttu-id="bbc18-588">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-589">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-589">Definition</span></span>

<span data-ttu-id="bbc18-590">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-591">이 함수 `Func_luxemburg_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-592">from `Keywords_luxemburg_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-593">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-594">이 함수 `Func_luxemburg_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-595">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="bbc18-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-597">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-597">tax number</span></span>
  
<span data-ttu-id="bbc18-598">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-598">tax no.</span></span>
  
<span data-ttu-id="bbc18-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-599">taxno#</span></span>
  
<span data-ttu-id="bbc18-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-600">taxnumber#</span></span>
  
<span data-ttu-id="bbc18-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-601">taxnumber</span></span>
  
<span data-ttu-id="bbc18-602">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-602">tax id</span></span>
  
<span data-ttu-id="bbc18-603">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-603">taxid#</span></span>
  
<span data-ttu-id="bbc18-604">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-604">tax identification number</span></span>
  
<span data-ttu-id="bbc18-605">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-605">tax identification no.</span></span>
  
<span data-ttu-id="bbc18-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-606">steuernummer</span></span>
  
<span data-ttu-id="bbc18-607">steuer id</span><span class="sxs-lookup"><span data-stu-id="bbc18-607">steuer id</span></span>
  
<span data-ttu-id="bbc18-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="bbc18-609">몰타</span><span class="sxs-lookup"><span data-stu-id="bbc18-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-610">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-610">Format</span></span>

<span data-ttu-id="bbc18-611">몰타어 nationals의 경우 지정 된 패턴의 7 자리 및 한 문자</span><span class="sxs-lookup"><span data-stu-id="bbc18-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="bbc18-612">몰타어 이외의 nationals 및 몰타어 엔터티: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-613">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-613">Pattern</span></span>

<span data-ttu-id="bbc18-614">몰타어 nationals: 7 자리 숫자 및 1 개 문자</span><span class="sxs-lookup"><span data-stu-id="bbc18-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="bbc18-615">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-615">Seven digits</span></span> 
    
- <span data-ttu-id="bbc18-616">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="bbc18-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="bbc18-617">몰타어 이외의 nationals 및 몰타어 엔터티: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="bbc18-618">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="bbc18-619">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-619">Checksum</span></span>

<span data-ttu-id="bbc18-620">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-621">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-621">Definition</span></span>

<span data-ttu-id="bbc18-622">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-623">이 함수 `Func_malta_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-624">from `Keywords_malta_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-625">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-626">이 함수 `Func_malta_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-627">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="bbc18-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-629">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-629">tax number</span></span>
  
<span data-ttu-id="bbc18-630">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-630">tax no.</span></span>
  
<span data-ttu-id="bbc18-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-631">taxno#</span></span>
  
<span data-ttu-id="bbc18-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-632">taxnumber#</span></span>
  
<span data-ttu-id="bbc18-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-633">taxnumber</span></span>
  
<span data-ttu-id="bbc18-634">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-634">tax id</span></span>
  
<span data-ttu-id="bbc18-635">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-635">taxid#</span></span>
  
<span data-ttu-id="bbc18-636">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-636">tax identification number</span></span>
  
<span data-ttu-id="bbc18-637">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-637">tax identification no.</span></span>
  
<span data-ttu-id="bbc18-638">numru tat</span><span class="sxs-lookup"><span data-stu-id="bbc18-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="bbc18-639">id tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="bbc18-639">id tat-taxxa</span></span>
  
<span data-ttu-id="bbc18-640">numru ta ' taxxa</span><span class="sxs-lookup"><span data-stu-id="bbc18-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="bbc18-641">네덜란드</span><span class="sxs-lookup"><span data-stu-id="bbc18-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-642">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-642">Format</span></span>

<span data-ttu-id="bbc18-643">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-644">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-644">Pattern</span></span>

<span data-ttu-id="bbc18-645">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="bbc18-646">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-646">Checksum</span></span>

<span data-ttu-id="bbc18-647">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-648">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-648">Definition</span></span>

<span data-ttu-id="bbc18-649">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-650">이 함수 `Func_netherlands_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-651">from `Keywords_netherlands_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-652">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-653">이 함수 `Func_netherlands_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-654">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="bbc18-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-656">네덜란드 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="bbc18-657">네덜란드 세금 식별</span><span class="sxs-lookup"><span data-stu-id="bbc18-657">netherlands tax identification</span></span>
  
<span data-ttu-id="bbc18-658">netherland의 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="bbc18-659">netherland의 세금 식별</span><span class="sxs-lookup"><span data-stu-id="bbc18-659">netherland's tax identification</span></span>
  
<span data-ttu-id="bbc18-660">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-660">tax identification number</span></span>
  
<span data-ttu-id="bbc18-661">네덜란드어 세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-661">dutch tax id</span></span>
  
<span data-ttu-id="bbc18-662">네덜란드어 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-662">dutch tax identification number</span></span>
  
<span data-ttu-id="bbc18-663">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-663">tax id</span></span>
  
<span data-ttu-id="bbc18-664">세금 id #</span><span class="sxs-lookup"><span data-stu-id="bbc18-664">tax id#</span></span>
  
<span data-ttu-id="bbc18-665">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-665">tax number</span></span>
  
<span data-ttu-id="bbc18-666">세금 없음 #</span><span class="sxs-lookup"><span data-stu-id="bbc18-666">tax no#</span></span>
  
<span data-ttu-id="bbc18-667">세금</span><span class="sxs-lookup"><span data-stu-id="bbc18-667">tax#</span></span>
  
<span data-ttu-id="bbc18-668">tin
</span><span class="sxs-lookup"><span data-stu-id="bbc18-668">tin</span></span>
  
<span data-ttu-id="bbc18-669">언급</span><span class="sxs-lookup"><span data-stu-id="bbc18-669">tin#</span></span>
  
<span data-ttu-id="bbc18-670">네덜란드 언급</span><span class="sxs-lookup"><span data-stu-id="bbc18-670">netherlands tin</span></span>
  
<span data-ttu-id="bbc18-671">netherland의 언급</span><span class="sxs-lookup"><span data-stu-id="bbc18-671">netherland's tin</span></span>
  
<span data-ttu-id="bbc18-672">nederlands belasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="bbc18-673">identificatienummer van belasting</span><span class="sxs-lookup"><span data-stu-id="bbc18-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="bbc18-674">identificatienummer belasting</span><span class="sxs-lookup"><span data-stu-id="bbc18-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="bbc18-675">nederlands belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="bbc18-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="bbc18-676">nederlands belasting id nummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="bbc18-677">nederlands belastingnummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="bbc18-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-678">btw nummer</span></span>
  
<span data-ttu-id="bbc18-679">nederlandse belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="bbc18-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="bbc18-680">폴란드</span><span class="sxs-lookup"><span data-stu-id="bbc18-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-681">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-681">Format</span></span>

<span data-ttu-id="bbc18-682">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-683">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-683">Pattern</span></span>

<span data-ttu-id="bbc18-684">11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-685">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-685">Checksum</span></span>

<span data-ttu-id="bbc18-686">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-687">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-687">Definition</span></span>

<span data-ttu-id="bbc18-688">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-689">이 함수 `Func_poland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-690">from `Keywords_poland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-691">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-692">이 함수 `Func_poland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-693">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="bbc18-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-695">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-695">tax number</span></span>
  
<span data-ttu-id="bbc18-696">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-696">tax no.</span></span>
  
<span data-ttu-id="bbc18-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-697">taxno#</span></span>
  
<span data-ttu-id="bbc18-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-698">taxnumber#</span></span>
  
<span data-ttu-id="bbc18-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-699">taxnumber</span></span>
  
<span data-ttu-id="bbc18-700">nip</span><span class="sxs-lookup"><span data-stu-id="bbc18-700">nip</span></span>
  
<span data-ttu-id="bbc18-701">nip #</span><span class="sxs-lookup"><span data-stu-id="bbc18-701">nip#</span></span>
  
<span data-ttu-id="bbc18-702">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-702">tax id</span></span>
  
<span data-ttu-id="bbc18-703">세금 id #</span><span class="sxs-lookup"><span data-stu-id="bbc18-703">tax id#</span></span>
  
<span data-ttu-id="bbc18-704">nip id</span><span class="sxs-lookup"><span data-stu-id="bbc18-704">nip id</span></span>
  
<span data-ttu-id="bbc18-705">nip id #</span><span class="sxs-lookup"><span data-stu-id="bbc18-705">nip id#</span></span>
  
<span data-ttu-id="bbc18-706">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-706">tax identification number</span></span>
  
<span data-ttu-id="bbc18-707">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-707">tax identification no.</span></span>
  
<span data-ttu-id="bbc18-708">vat 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-708">vat number</span></span>
  
<span data-ttu-id="bbc18-709">vat 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-709">vat no.</span></span>
  
<span data-ttu-id="bbc18-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-710">vatno#</span></span>
  
<span data-ttu-id="bbc18-711">vat id</span><span class="sxs-lookup"><span data-stu-id="bbc18-711">vat id</span></span>
  
<span data-ttu-id="bbc18-712">vat id #</span><span class="sxs-lookup"><span data-stu-id="bbc18-712">vat id#</span></span>
  
<span data-ttu-id="bbc18-713">u r i identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="bbc18-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="bbc18-714">정책 스키 u r i identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="bbc18-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="bbc18-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="bbc18-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="bbc18-716">포르투갈</span><span class="sxs-lookup"><span data-stu-id="bbc18-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-717">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-717">Format</span></span>

<span data-ttu-id="bbc18-718">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-719">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-719">Pattern</span></span>

<span data-ttu-id="bbc18-720">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-721">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-721">Checksum</span></span>

<span data-ttu-id="bbc18-722">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-723">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-723">Definition</span></span>

<span data-ttu-id="bbc18-724">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-725">이 함수 `Func_portugal_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-726">from `Keywords_portugal_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-727">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-728">이 함수 `Func_portugal_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-729">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="bbc18-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-731">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-731">tax number</span></span>
  
<span data-ttu-id="bbc18-732">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-732">tax no.</span></span>
  
<span data-ttu-id="bbc18-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-733">taxno#</span></span>
  
<span data-ttu-id="bbc18-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="bbc18-734">taxnumber#</span></span>
  
<span data-ttu-id="bbc18-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="bbc18-735">taxnumber</span></span>
  
<span data-ttu-id="bbc18-736">m</span><span class="sxs-lookup"><span data-stu-id="bbc18-736">nif</span></span>
  
<span data-ttu-id="bbc18-737">m</span><span class="sxs-lookup"><span data-stu-id="bbc18-737">nif#</span></span>
  
<span data-ttu-id="bbc18-738">numero 회계</span><span class="sxs-lookup"><span data-stu-id="bbc18-738">numero fiscal</span></span>
  
<span data-ttu-id="bbc18-739">número de identificação 회계</span><span class="sxs-lookup"><span data-stu-id="bbc18-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="bbc18-740">루마니아</span><span class="sxs-lookup"><span data-stu-id="bbc18-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-741">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-741">Format</span></span>

<span data-ttu-id="bbc18-742">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-743">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-743">Pattern</span></span>

<span data-ttu-id="bbc18-744">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-745">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-745">Checksum</span></span>

<span data-ttu-id="bbc18-746">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-747">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-747">Definition</span></span>

<span data-ttu-id="bbc18-748">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-749">정규식이 해당 `Regex_romania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-750">from `Keywords_romania_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bbc18-751">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="bbc18-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-753">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-753">tax id</span></span>
  
<span data-ttu-id="bbc18-754">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-754">tax id number</span></span>
  
<span data-ttu-id="bbc18-755">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-755">tax file no</span></span>
  
<span data-ttu-id="bbc18-756">

tax file number</span><span class="sxs-lookup"><span data-stu-id="bbc18-756">tax file number</span></span>
  
<span data-ttu-id="bbc18-757">세금 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-757">tax no</span></span>
  
<span data-ttu-id="bbc18-758">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-758">tax number</span></span>
  
<span data-ttu-id="bbc18-759">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-759">taxid#</span></span>
  
<span data-ttu-id="bbc18-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-760">taxno#</span></span>
  
<span data-ttu-id="bbc18-761">id-ul taxei</span><span class="sxs-lookup"><span data-stu-id="bbc18-761">id-ul taxei</span></span>
  
<span data-ttu-id="bbc18-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="bbc18-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="bbc18-763">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="bbc18-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-764">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-764">Format</span></span>

<span data-ttu-id="bbc18-765">공백이 나 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-766">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-766">Pattern</span></span>

<span data-ttu-id="bbc18-767">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-768">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-768">Checksum</span></span>

<span data-ttu-id="bbc18-769">해당 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-770">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-770">Definition</span></span>

<span data-ttu-id="bbc18-771">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-772">정규식이 해당 `Regex_slovakia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-773">from `Keywords_slovakia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bbc18-774">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="bbc18-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-776">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-776">tax id</span></span>
  
<span data-ttu-id="bbc18-777">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-777">tax id number</span></span>
  
<span data-ttu-id="bbc18-778">언급 id</span><span class="sxs-lookup"><span data-stu-id="bbc18-778">tin id</span></span>
  
<span data-ttu-id="bbc18-779">언급 아니요</span><span class="sxs-lookup"><span data-stu-id="bbc18-779">tin no</span></span>
  
<span data-ttu-id="bbc18-780">슬로바키아어 언급 id</span><span class="sxs-lookup"><span data-stu-id="bbc18-780">slovakian tin id</span></span>
  
<span data-ttu-id="bbc18-781">tin
</span><span class="sxs-lookup"><span data-stu-id="bbc18-781">tin</span></span>
  
<span data-ttu-id="bbc18-782">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-782">tax file no</span></span>
  
<span data-ttu-id="bbc18-783">

tax file number</span><span class="sxs-lookup"><span data-stu-id="bbc18-783">tax file number</span></span>
  
<span data-ttu-id="bbc18-784">세금 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-784">tax no</span></span>
  
<span data-ttu-id="bbc18-785">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-785">tax number</span></span>
  
<span data-ttu-id="bbc18-786">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-786">taxid#</span></span>
  
<span data-ttu-id="bbc18-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-787">taxno#</span></span>
  
<span data-ttu-id="bbc18-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="bbc18-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="bbc18-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="bbc18-789">daňové číslo</span></span>
  
<span data-ttu-id="bbc18-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="bbc18-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="bbc18-791">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="bbc18-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-792">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-792">Format</span></span>

<span data-ttu-id="bbc18-793">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-794">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-794">Pattern</span></span>

<span data-ttu-id="bbc18-795">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-796">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-796">Checksum</span></span>

<span data-ttu-id="bbc18-797">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-798">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-798">Definition</span></span>

<span data-ttu-id="bbc18-799">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-800">이 함수 `Func_slovenia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-801">from `Keywords_slovenia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-802">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-803">이 함수 `Func_slovenia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-804">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="bbc18-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-806">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-806">tax id</span></span>
  
<span data-ttu-id="bbc18-807">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-807">tax id number</span></span>
  
<span data-ttu-id="bbc18-808">언급 id</span><span class="sxs-lookup"><span data-stu-id="bbc18-808">tin id</span></span>
  
<span data-ttu-id="bbc18-809">언급 아니요</span><span class="sxs-lookup"><span data-stu-id="bbc18-809">tin no</span></span>
  
<span data-ttu-id="bbc18-810">슬로베니아어 언급 id</span><span class="sxs-lookup"><span data-stu-id="bbc18-810">slovenian tin id</span></span>
  
<span data-ttu-id="bbc18-811">tin
</span><span class="sxs-lookup"><span data-stu-id="bbc18-811">tin</span></span>
  
<span data-ttu-id="bbc18-812">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-812">tax file no</span></span>
  
<span data-ttu-id="bbc18-813">

tax file number</span><span class="sxs-lookup"><span data-stu-id="bbc18-813">tax file number</span></span>
  
<span data-ttu-id="bbc18-814">세금 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-814">tax no</span></span>
  
<span data-ttu-id="bbc18-815">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-815">tax number</span></span>
  
<span data-ttu-id="bbc18-816">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-816">taxid#</span></span>
  
<span data-ttu-id="bbc18-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-817">taxno#</span></span>
  
<span data-ttu-id="bbc18-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="bbc18-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="bbc18-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="bbc18-819">davčna številka</span></span>
  
<span data-ttu-id="bbc18-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="bbc18-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="bbc18-821">스페인</span><span class="sxs-lookup"><span data-stu-id="bbc18-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-822">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-822">Format</span></span>

<span data-ttu-id="bbc18-823">지정 된 패턴에 7 ~ 8 자리 숫자와 한 가지 또는 두 개의 문자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-824">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-824">Pattern</span></span>

<span data-ttu-id="bbc18-825">스페인 국내 id 카드가 있는 스페인어 (자연 사용자):</span><span class="sxs-lookup"><span data-stu-id="bbc18-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="bbc18-826">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-826">Eight digits</span></span> 
    
- <span data-ttu-id="bbc18-827">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="bbc18-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="bbc18-828">스페인 국가 id 카드가 없는 상주 하지 않는 Spaniards</span><span class="sxs-lookup"><span data-stu-id="bbc18-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="bbc18-829">1 개의 대문자 "L" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="bbc18-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="bbc18-830">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-830">Seven digits</span></span>
    
- <span data-ttu-id="bbc18-831">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="bbc18-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="bbc18-832">스페인 국가 id 카드를 사용 하지 않고 14 년 동안 상주 하는 Spaniards:</span><span class="sxs-lookup"><span data-stu-id="bbc18-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="bbc18-833">1 개의 대문자 "K" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="bbc18-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="bbc18-834">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-834">Seven digits</span></span> 
    
- <span data-ttu-id="bbc18-835">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="bbc18-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="bbc18-836">Foreigner의 식별 번호를 사용 하는 Foreigners</span><span class="sxs-lookup"><span data-stu-id="bbc18-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="bbc18-837">"X", "Y" 또는 "Z" (대/소문자 구분)의 대문자 1 개</span><span class="sxs-lookup"><span data-stu-id="bbc18-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="bbc18-838">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-838">Seven digits</span></span>
    
- <span data-ttu-id="bbc18-839">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="bbc18-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="bbc18-840">Foreigner의 id 번호가 없는 Foreigners</span><span class="sxs-lookup"><span data-stu-id="bbc18-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="bbc18-841">"M"을 나타내는 대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="bbc18-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="bbc18-842">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-842">Seven digits</span></span>
    
- <span data-ttu-id="bbc18-843">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="bbc18-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="bbc18-844">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-844">Checksum</span></span>

<span data-ttu-id="bbc18-845">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-846">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-846">Definition</span></span>

<span data-ttu-id="bbc18-847">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-848">이 함수 `Func_spain_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-849">from `Keywords_spain_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-850">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-851">이 함수 `Func_spain_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-852">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="bbc18-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-854">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-854">tax id</span></span>
  
<span data-ttu-id="bbc18-855">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-855">tax id number</span></span>
  
<span data-ttu-id="bbc18-856">cif id</span><span class="sxs-lookup"><span data-stu-id="bbc18-856">cif id</span></span>
  
<span data-ttu-id="bbc18-857">cif 아니요</span><span class="sxs-lookup"><span data-stu-id="bbc18-857">cif no</span></span>
  
<span data-ttu-id="bbc18-858">스페인어 cif id</span><span class="sxs-lookup"><span data-stu-id="bbc18-858">spanish cif id</span></span>
  
<span data-ttu-id="bbc18-859">cif</span><span class="sxs-lookup"><span data-stu-id="bbc18-859">cif</span></span>
  
<span data-ttu-id="bbc18-860">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-860">tax file no</span></span>
  
<span data-ttu-id="bbc18-861">스페인어 cif 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-861">spanish cif number</span></span>
  
<span data-ttu-id="bbc18-862">

tax file number</span><span class="sxs-lookup"><span data-stu-id="bbc18-862">tax file number</span></span>
  
<span data-ttu-id="bbc18-863">스페인어 cif 아니요</span><span class="sxs-lookup"><span data-stu-id="bbc18-863">spanish cif no</span></span>
  
<span data-ttu-id="bbc18-864">세금 없음</span><span class="sxs-lookup"><span data-stu-id="bbc18-864">tax no</span></span>
  
<span data-ttu-id="bbc18-865">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-865">tax number</span></span>
  
<span data-ttu-id="bbc18-866">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-866">taxid#</span></span>
  
<span data-ttu-id="bbc18-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-867">taxno#</span></span>
  
<span data-ttu-id="bbc18-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-868">cifid#</span></span>
  
<span data-ttu-id="bbc18-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-869">spanishcifid#</span></span>
  
<span data-ttu-id="bbc18-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="bbc18-870">spanishcifno#</span></span>
  
<span data-ttu-id="bbc18-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="bbc18-871">número de contribuyente</span></span>
  
<span data-ttu-id="bbc18-872">número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="bbc18-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="bbc18-873">número de identificación 회계</span><span class="sxs-lookup"><span data-stu-id="bbc18-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="bbc18-874">cif número</span><span class="sxs-lookup"><span data-stu-id="bbc18-874">cif número</span></span>
  
<span data-ttu-id="bbc18-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="bbc18-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="bbc18-876">스웨덴</span><span class="sxs-lookup"><span data-stu-id="bbc18-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-877">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-877">Format</span></span>

<span data-ttu-id="bbc18-878">지정 된 패턴의 10 자리 숫자와 기호</span><span class="sxs-lookup"><span data-stu-id="bbc18-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-879">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-879">Pattern</span></span>

<span data-ttu-id="bbc18-880">10 자리 숫자와 기호:</span><span class="sxs-lookup"><span data-stu-id="bbc18-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="bbc18-881">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="bbc18-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="bbc18-882">더하기 기호, 빼기 기호 또는 백슬래시</span><span class="sxs-lookup"><span data-stu-id="bbc18-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="bbc18-883">다음은 식별 번호를 고유 하 게 만드는 3 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="bbc18-884">1990 이전에 실행 된 번호의 경우 일곱째 및 여덟 번째 숫자는 출생 또는 외부에서 태어난 사람의 국가를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="bbc18-885">아홉 번째 위치의 숫자는 성별에 대 한 홀수 또는 암도를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="bbc18-886">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="bbc18-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="bbc18-887">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-887">Checksum</span></span>

<span data-ttu-id="bbc18-888">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-889">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-889">Definition</span></span>

<span data-ttu-id="bbc18-890">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-891">이 함수 `Func_sweden_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-892">from `Keywords_sweden_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="bbc18-893">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-894">이 함수 `Func_sweden_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="bbc18-895">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="bbc18-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-897">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-897">tax id</span></span>
  
<span data-ttu-id="bbc18-898">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-898">tax id no.</span></span>
  
<span data-ttu-id="bbc18-899">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-899">tax id number</span></span>
  
<span data-ttu-id="bbc18-900">tax identification
</span><span class="sxs-lookup"><span data-stu-id="bbc18-900">tax identification</span></span>
  
<span data-ttu-id="bbc18-901">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-901">tax identification#</span></span>
  
<span data-ttu-id="bbc18-902">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-902">tax no.</span></span>
  
<span data-ttu-id="bbc18-903">세금</span><span class="sxs-lookup"><span data-stu-id="bbc18-903">tax#</span></span>
  
<span data-ttu-id="bbc18-904">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-904">taxid#</span></span>
  
<span data-ttu-id="bbc18-905">세금 파일</span><span class="sxs-lookup"><span data-stu-id="bbc18-905">tax file</span></span>
  
<span data-ttu-id="bbc18-906">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-906">tax file no.</span></span>
  
<span data-ttu-id="bbc18-907">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-907">personal id number</span></span>
  
<span data-ttu-id="bbc18-908">(nummer at&t id)</span><span class="sxs-lookup"><span data-stu-id="bbc18-908">skatt id nummer</span></span>
  
<span data-ttu-id="bbc18-909">identifikation at&t</span><span class="sxs-lookup"><span data-stu-id="bbc18-909">skatt identifikation</span></span>
  
<span data-ttu-id="bbc18-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="bbc18-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="bbc18-911">영국의</span><span class="sxs-lookup"><span data-stu-id="bbc18-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="bbc18-912">형식</span><span class="sxs-lookup"><span data-stu-id="bbc18-912">Format</span></span>

<span data-ttu-id="bbc18-913">utr (Unique Taxpayer Reference): 공백 및 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="bbc18-p103">국가 보험 번호 (NINO): 자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"영국 국립 보험 번호 (NINO)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bbc18-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="bbc18-916">패턴</span><span class="sxs-lookup"><span data-stu-id="bbc18-916">Pattern</span></span>

<span data-ttu-id="bbc18-917">utr (Unique Taxpayer Reference): 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="bbc18-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="bbc18-p104">국가 보험 번호 (NINO): 자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"영국 국립 보험 번호 (NINO)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bbc18-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="bbc18-920">체크섬</span><span class="sxs-lookup"><span data-stu-id="bbc18-920">Checksum</span></span>

<span data-ttu-id="bbc18-921">예</span><span class="sxs-lookup"><span data-stu-id="bbc18-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="bbc18-922">정의</span><span class="sxs-lookup"><span data-stu-id="bbc18-922">Definition</span></span>

<span data-ttu-id="bbc18-923">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="bbc18-924">이 함수 `Func_uk_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="bbc18-925">from `Keywords_uk_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="bbc18-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="bbc18-926">키워드</span><span class="sxs-lookup"><span data-stu-id="bbc18-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="bbc18-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="bbc18-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="bbc18-928">tax id
</span><span class="sxs-lookup"><span data-stu-id="bbc18-928">tax id</span></span>
  
<span data-ttu-id="bbc18-929">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-929">tax id no.</span></span>
  
<span data-ttu-id="bbc18-930">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-930">tax id number</span></span>
  
<span data-ttu-id="bbc18-931">tax identification
</span><span class="sxs-lookup"><span data-stu-id="bbc18-931">tax identification</span></span>
  
<span data-ttu-id="bbc18-932">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-932">tax identification#</span></span>
  
<span data-ttu-id="bbc18-933">세금 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-933">tax no.</span></span>
  
<span data-ttu-id="bbc18-934">세금</span><span class="sxs-lookup"><span data-stu-id="bbc18-934">tax#</span></span>
  
<span data-ttu-id="bbc18-935">taxid #</span><span class="sxs-lookup"><span data-stu-id="bbc18-935">taxid#</span></span>
  
<span data-ttu-id="bbc18-936">세금 파일</span><span class="sxs-lookup"><span data-stu-id="bbc18-936">tax file</span></span>
  
<span data-ttu-id="bbc18-937">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="bbc18-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbc18-938">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bbc18-938">See also</span></span>

[<span data-ttu-id="bbc18-939">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="bbc18-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

