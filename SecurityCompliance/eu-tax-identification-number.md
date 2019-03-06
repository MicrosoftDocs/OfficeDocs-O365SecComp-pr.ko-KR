---
title: EU 세금 확인 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 EU 세금 식별 번호 중요 정보 유형을 검색할 때 DLP (데이터 손실 방지) 정책이 어떤 역할을 검색 하나요를 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: 4914ff078695519c2a298190d82c86a6abebceb9
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410913"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="b5030-104">EU 세금 확인 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-104">EU Tax Identification Number</span></span>

<span data-ttu-id="b5030-105">이 항목에서는 언급 (데이터 손실 방지) 정책이 EU (유럽 세금 식별 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="b5030-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="b5030-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="b5030-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="b5030-108">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-108">Format</span></span>

<span data-ttu-id="b5030-109">하이픈 및 슬래시가 있는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-110">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-110">Pattern</span></span>

<span data-ttu-id="b5030-111">하이픈 및 슬래시가 있는 9 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="b5030-112">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-112">Two digits</span></span> 
    
- <span data-ttu-id="b5030-113">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="b5030-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="b5030-114">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-114">Three digits</span></span>
    
- <span data-ttu-id="b5030-115">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="b5030-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="b5030-116">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-117">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-117">Checksum</span></span>

<span data-ttu-id="b5030-118">예</span><span class="sxs-lookup"><span data-stu-id="b5030-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-119">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-119">Definition</span></span>

<span data-ttu-id="b5030-120">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-121">이 함수 `Func_austria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-122">from `Keywords_austria_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-123">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-124">이 함수 `Func_austria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-125">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="b5030-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-127">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-127">tax number</span></span>
  
<span data-ttu-id="b5030-128">수</span><span class="sxs-lookup"><span data-stu-id="b5030-128">number</span></span>
  
<span data-ttu-id="b5030-129">세금 등록 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-129">tax registration number</span></span>
  
<span data-ttu-id="b5030-130">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-130">tax id</span></span>
  
<span data-ttu-id="b5030-131">st.nr</span><span class="sxs-lookup"><span data-stu-id="b5030-131">st.nr.</span></span>
  
<span data-ttu-id="b5030-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="b5030-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="b5030-133">벨기에</span><span class="sxs-lookup"><span data-stu-id="b5030-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="b5030-134">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-134">Format</span></span>

<span data-ttu-id="b5030-135">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-136">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-136">Pattern</span></span>

<span data-ttu-id="b5030-137">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-137">11 digits:</span></span>
  
- <span data-ttu-id="b5030-138">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-138">Two digits</span></span>
    
- <span data-ttu-id="b5030-139">"0" 또는 "1"</span><span class="sxs-lookup"><span data-stu-id="b5030-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="b5030-140">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-140">One digit</span></span>
    
- <span data-ttu-id="b5030-141">"0" 또는 "1" 또는 "2" 또는 "3"</span><span class="sxs-lookup"><span data-stu-id="b5030-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="b5030-142">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-143">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-143">Checksum</span></span>

<span data-ttu-id="b5030-144">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-145">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-145">Definition</span></span>

<span data-ttu-id="b5030-146">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-147">정규식이 해당 `Regex_belgium_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-148">from `Keywords_belgium_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b5030-149">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="b5030-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-151">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-151">tax number</span></span>
  
<span data-ttu-id="b5030-152">국가 등록 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-152">national registration number</span></span>
  
<span data-ttu-id="b5030-153">세금 등록 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-153">tax registration number</span></span>
  
<span data-ttu-id="b5030-154">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-154">tax id</span></span>
  
<span data-ttu-id="b5030-155">m</span><span class="sxs-lookup"><span data-stu-id="b5030-155">nif</span></span>
  
<span data-ttu-id="b5030-156">m</span><span class="sxs-lookup"><span data-stu-id="b5030-156">nif#</span></span>
  
<span data-ttu-id="b5030-157">numéro de registre 국립</span><span class="sxs-lookup"><span data-stu-id="b5030-157">numéro de registre national</span></span>
  
<span data-ttu-id="b5030-158">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="b5030-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="b5030-159">불가리아</span><span class="sxs-lookup"><span data-stu-id="b5030-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="b5030-160">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-160">Format</span></span>

<span data-ttu-id="b5030-161">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-162">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-162">Pattern</span></span>

<span data-ttu-id="b5030-163">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-164">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-164">Checksum</span></span>

<span data-ttu-id="b5030-165">예</span><span class="sxs-lookup"><span data-stu-id="b5030-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-166">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-166">Definition</span></span>

<span data-ttu-id="b5030-167">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-168">이 함수 `Func_bulgaria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-169">from `Keywords_bulgaria_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-170">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-171">이 함수 `Func_bulgaria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-172">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="b5030-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-174">고 대 cn</span><span class="sxs-lookup"><span data-stu-id="b5030-174">bucn</span></span>
  
<span data-ttu-id="b5030-175">일관적인 민사 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-175">uniform civil number</span></span>
  
<span data-ttu-id="b5030-176">과 (와) cn #</span><span class="sxs-lookup"><span data-stu-id="b5030-176">bucn#</span></span>
  
<span data-ttu-id="b5030-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="b5030-178">일정 한 민사 일련번호</span><span class="sxs-lookup"><span data-stu-id="b5030-178">uniform civil id</span></span>
  
<span data-ttu-id="b5030-179">일관적인 민사</span><span class="sxs-lookup"><span data-stu-id="b5030-179">uniform civil no</span></span>
  
<span data-ttu-id="b5030-180">egn</span><span class="sxs-lookup"><span data-stu-id="b5030-180">egn</span></span>
  
<span data-ttu-id="b5030-181">불가리아어 (민사)</span><span class="sxs-lookup"><span data-stu-id="b5030-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="b5030-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="b5030-182">uniformcivilno#</span></span>
  
<span data-ttu-id="b5030-183">egn #</span><span class="sxs-lookup"><span data-stu-id="b5030-183">egn#</span></span>
  
<span data-ttu-id="b5030-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="b5030-184">униформ граждански номер</span></span>
  
<span data-ttu-id="b5030-185">униформ id</span><span class="sxs-lookup"><span data-stu-id="b5030-185">униформ id</span></span>
  
<span data-ttu-id="b5030-186">униформ граждански id</span><span class="sxs-lookup"><span data-stu-id="b5030-186">униформ граждански id</span></span>
  
<span data-ttu-id="b5030-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="b5030-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="b5030-188">크로아티아</span><span class="sxs-lookup"><span data-stu-id="b5030-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="b5030-189">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-189">Format</span></span>

<span data-ttu-id="b5030-190">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-191">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-191">Pattern</span></span>

<span data-ttu-id="b5030-192">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-192">11 digits:</span></span>
  
- <span data-ttu-id="b5030-193">임의로 선택한 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="b5030-194">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="b5030-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-195">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-195">Checksum</span></span>

<span data-ttu-id="b5030-196">예</span><span class="sxs-lookup"><span data-stu-id="b5030-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-197">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-197">Definition</span></span>

<span data-ttu-id="b5030-198">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-199">이 함수 `Func_croatia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-200">from `Keywords_croatia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-202">이 함수 `Func_croatia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-203">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="b5030-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-205">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-205">tax number</span></span>
  
<span data-ttu-id="b5030-206">세금</span><span class="sxs-lookup"><span data-stu-id="b5030-206">tax</span></span>
  
<span data-ttu-id="b5030-207">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-207">tax id</span></span>
  
<span data-ttu-id="b5030-208">원환형</span><span class="sxs-lookup"><span data-stu-id="b5030-208">oid</span></span>
  
<span data-ttu-id="b5030-209">원환형</span><span class="sxs-lookup"><span data-stu-id="b5030-209">oid#</span></span>
  
<span data-ttu-id="b5030-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="b5030-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="b5030-211">키프로스</span><span class="sxs-lookup"><span data-stu-id="b5030-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="b5030-212">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-212">Format</span></span>

<span data-ttu-id="b5030-213">지정 된 패턴에서 8 자리 및 1 개 문자</span><span class="sxs-lookup"><span data-stu-id="b5030-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-214">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-214">Pattern</span></span>

<span data-ttu-id="b5030-215">8 자리 숫자와 1 개 문자:</span><span class="sxs-lookup"><span data-stu-id="b5030-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="b5030-216">"0"</span><span class="sxs-lookup"><span data-stu-id="b5030-216">A "0"</span></span> 
    
- <span data-ttu-id="b5030-217">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-217">Seven digits</span></span>
    
- <span data-ttu-id="b5030-218">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b5030-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-219">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-219">Checksum</span></span>

<span data-ttu-id="b5030-220">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-221">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-221">Definition</span></span>

<span data-ttu-id="b5030-222">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-223">이 함수 `Func_cyprus_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-224">from `Keywords_cyprus_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-225">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-226">이 함수 `Func_cyprus_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-227">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="b5030-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-229">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-229">tax number</span></span>
  
<span data-ttu-id="b5030-230">세금</span><span class="sxs-lookup"><span data-stu-id="b5030-230">tax</span></span>
  
<span data-ttu-id="b5030-231">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-231">tax id</span></span>
  
<span data-ttu-id="b5030-232">세금 식별 코드</span><span class="sxs-lookup"><span data-stu-id="b5030-232">tax identification code</span></span>
  
<span data-ttu-id="b5030-233">tic</span><span class="sxs-lookup"><span data-stu-id="b5030-233">tic</span></span>
  
<span data-ttu-id="b5030-234">tic #</span><span class="sxs-lookup"><span data-stu-id="b5030-234">tic#</span></span>
  
<span data-ttu-id="b5030-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="b5030-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="b5030-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="b5030-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="b5030-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="b5030-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="b5030-238">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="b5030-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="b5030-239">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-239">Format</span></span>

<span data-ttu-id="b5030-240">선택적 백슬래시가 있는 9 자리 또는 10 진수</span><span class="sxs-lookup"><span data-stu-id="b5030-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-241">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-241">Pattern</span></span>

<span data-ttu-id="b5030-242">선택적 backslashl이 있는 아홉 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="b5030-243">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-243">Six digits</span></span> 
    
- <span data-ttu-id="b5030-244">백슬래시 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="b5030-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="b5030-245">3 ~ 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-246">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-246">Checksum</span></span>

<span data-ttu-id="b5030-247">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-248">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-248">Definition</span></span>

<span data-ttu-id="b5030-249">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-250">정규식이 해당 `Regex_czech_republic_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-251">from `Keywords_czech_republic_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b5030-252">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="b5030-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-254">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-254">tax number</span></span>
  
<span data-ttu-id="b5030-255">세금</span><span class="sxs-lookup"><span data-stu-id="b5030-255">tax</span></span>
  
<span data-ttu-id="b5030-256">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-256">tax id</span></span>
  
<span data-ttu-id="b5030-257">개인 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-257">personal number</span></span>
  
<span data-ttu-id="b5030-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="b5030-258">daňové číslo</span></span>
  
<span data-ttu-id="b5030-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="b5030-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="b5030-260">덴마크</span><span class="sxs-lookup"><span data-stu-id="b5030-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="b5030-261">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-261">Format</span></span>

<span data-ttu-id="b5030-262">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-263">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-263">Pattern</span></span>

<span data-ttu-id="b5030-264">hyphenl를 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="b5030-265">생년월일에 해당 하는 6 자리 숫자 (ddmmyy)</span><span class="sxs-lookup"><span data-stu-id="b5030-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="b5030-266">하이픈</span><span class="sxs-lookup"><span data-stu-id="b5030-266">A hyphen</span></span>
    
- <span data-ttu-id="b5030-267">첫 번째 숫자가 출생 세기에 해당 하 고 마지막 숫자가 개별 성별에 해당 하는 시퀀스 번호에 해당 하는 4 자리 숫자 (남성의 경우 홀수 및 암에도 해당)</span><span class="sxs-lookup"><span data-stu-id="b5030-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-268">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-268">Checksum</span></span>

<span data-ttu-id="b5030-269">예</span><span class="sxs-lookup"><span data-stu-id="b5030-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-270">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-270">Definition</span></span>

<span data-ttu-id="b5030-271">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-272">이 함수 `Func_denmark_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-273">from `Keywords_denmark_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-275">이 함수 `Func_denmark_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-276">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="b5030-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-278">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-278">tax number</span></span>
  
<span data-ttu-id="b5030-279">세금</span><span class="sxs-lookup"><span data-stu-id="b5030-279">tax</span></span>
  
<span data-ttu-id="b5030-280">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-280">tax id</span></span>
  
<span data-ttu-id="b5030-281">cpr 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-281">cpr number</span></span>
  
<span data-ttu-id="b5030-282">cpr #</span><span class="sxs-lookup"><span data-stu-id="b5030-282">cpr#</span></span>
  
<span data-ttu-id="b5030-283">nummer에서</span><span class="sxs-lookup"><span data-stu-id="b5030-283">skat nummer</span></span>
  
<span data-ttu-id="b5030-284">번호 (|)</span><span class="sxs-lookup"><span data-stu-id="b5030-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="b5030-285">에스토니아</span><span class="sxs-lookup"><span data-stu-id="b5030-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="b5030-286">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-286">Format</span></span>

<span data-ttu-id="b5030-287">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-288">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-288">Pattern</span></span>

<span data-ttu-id="b5030-289">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-289">11 digits:</span></span>
  
-  <span data-ttu-id="b5030-290">성별에 해당 하는 숫자와 홀수로 해당 하 고, 홀수를 지정 하 여 19th 세기에 대해 1, 2를 나타내는 숫자입니다. 3, 20th 세기에 대해 4를 적용 합니다. 21 세기에 대해 5, 6</span><span class="sxs-lookup"><span data-stu-id="b5030-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="b5030-291">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="b5030-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="b5030-292">같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="b5030-293">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="b5030-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-294">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-294">Checksum</span></span>

<span data-ttu-id="b5030-295">예</span><span class="sxs-lookup"><span data-stu-id="b5030-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-296">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-296">Definition</span></span>

<span data-ttu-id="b5030-297">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-298">이 함수 `Func_estonia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-299">from `Keywords_estonia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-300">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-301">이 함수 `Func_estonia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-302">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="b5030-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-304">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-304">tax number</span></span>
  
<span data-ttu-id="b5030-305">세금</span><span class="sxs-lookup"><span data-stu-id="b5030-305">tax</span></span>
  
<span data-ttu-id="b5030-306">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-306">tax id</span></span>
  
<span data-ttu-id="b5030-307">개인 코드</span><span class="sxs-lookup"><span data-stu-id="b5030-307">personal code</span></span>
  
<span data-ttu-id="b5030-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="b5030-308">maksunumber</span></span>
  
<span data-ttu-id="b5030-309">maksu id</span><span class="sxs-lookup"><span data-stu-id="b5030-309">maksu id</span></span>
  
<span data-ttu-id="b5030-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="b5030-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="b5030-311">핀란드</span><span class="sxs-lookup"><span data-stu-id="b5030-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="b5030-312">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-312">Format</span></span>

<span data-ttu-id="b5030-313">숫자, 문자, 더하기 및 빼기 기호를 11 문자로 조합</span><span class="sxs-lookup"><span data-stu-id="b5030-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-314">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-314">Pattern</span></span>

<span data-ttu-id="b5030-315">숫자, 문자, 더하기 및 빼기 기호를 11 문자로 조합한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="b5030-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-316">Six digits</span></span>
    
- <span data-ttu-id="b5030-317">더하기 기호, 빼기 기호 또는 + 기호가 1800-1899 사이에 태어난 것을 의미 하는 "a" (대/소문자 구분 안 함), 빼기 기호는 1900-1999 사이에 출생를 의미 하며 "a"는 "a"를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="b5030-318">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-318">Three digits</span></span>
    
- <span data-ttu-id="b5030-319">1 개의 문자 또는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-320">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-320">Checksum</span></span>

<span data-ttu-id="b5030-321">예</span><span class="sxs-lookup"><span data-stu-id="b5030-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-322">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-322">Definition</span></span>

<span data-ttu-id="b5030-323">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-324">이 함수 `Func_finland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-325">from `Keywords_finland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-326">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-327">이 함수 `Func_finland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-328">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="b5030-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-330">identification number</span><span class="sxs-lookup"><span data-stu-id="b5030-330">identification number</span></span>
  
<span data-ttu-id="b5030-331">개인 id</span><span class="sxs-lookup"><span data-stu-id="b5030-331">personal id</span></span>
  
<span data-ttu-id="b5030-332">id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-332">identity number</span></span>
  
<span data-ttu-id="b5030-333">핀란드어 국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-333">finnish national id number</span></span>
  
<span data-ttu-id="b5030-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-334">personalidnumber#</span></span>
  
<span data-ttu-id="b5030-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="b5030-335">national identification number</span></span>
  
<span data-ttu-id="b5030-336">id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-336">id number</span></span>
  
<span data-ttu-id="b5030-337">국가 id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-337">national id no.</span></span>
  
<span data-ttu-id="b5030-338">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-338">national id number</span></span>
  
<span data-ttu-id="b5030-339">id 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-339">id no</span></span>
  
<span data-ttu-id="b5030-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b5030-340">tunnistenumero</span></span>
  
<span data-ttu-id="b5030-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="b5030-341">henkilötunnus</span></span>
  
<span data-ttu-id="b5030-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b5030-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="b5030-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="b5030-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="b5030-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="b5030-344">identiteetti numero</span></span>
  
<span data-ttu-id="b5030-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="b5030-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="b5030-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="b5030-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="b5030-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="b5030-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="b5030-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="b5030-348">tunnusnumero</span></span>
  
<span data-ttu-id="b5030-349">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="b5030-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="b5030-350">프랑스</span><span class="sxs-lookup"><span data-stu-id="b5030-350">France</span></span>

### <a name="format"></a><span data-ttu-id="b5030-351">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-351">Format</span></span>

<span data-ttu-id="b5030-352">개별 사용자의 경우 13 자리 숫자 및 엔터티의 경우 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-353">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-353">Pattern</span></span>

<span data-ttu-id="b5030-354">개별 사용자에 대 한 13 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="b5030-355">0, 1, 2 또는 3 이어야 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="b5030-356">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-356">12 digits</span></span>
    
<span data-ttu-id="b5030-357">엔터티의 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-358">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-358">Checksum</span></span>

<span data-ttu-id="b5030-359">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-360">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-360">Definition</span></span>

<span data-ttu-id="b5030-361">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-362">이 함수 `Func_france_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-363">from `Keywords_france_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-365">이 함수 `Func_france_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-366">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="b5030-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-368">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-368">tax identification number</span></span>
  
<span data-ttu-id="b5030-369">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-369">tax number</span></span>
  
<span data-ttu-id="b5030-370">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-370">tax id</span></span>
  
<span data-ttu-id="b5030-371">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="b5030-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="b5030-372">독일</span><span class="sxs-lookup"><span data-stu-id="b5030-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="b5030-373">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-373">Format</span></span>

<span data-ttu-id="b5030-374">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-375">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-375">Pattern</span></span>

<span data-ttu-id="b5030-376">11 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-376">11 digits :</span></span>
  
-  <span data-ttu-id="b5030-377">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-377">Ten digits</span></span> 
    
- <span data-ttu-id="b5030-378">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="b5030-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-379">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-379">Checksum</span></span>

<span data-ttu-id="b5030-380">예</span><span class="sxs-lookup"><span data-stu-id="b5030-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-381">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-381">Definition</span></span>

<span data-ttu-id="b5030-382">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-383">이 함수 `Func_germany_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-384">from `Keywords_germany_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-385">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-386">이 함수 `Func_germany_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-387">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="b5030-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-389">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-389">tax number</span></span>
  
<span data-ttu-id="b5030-390">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-390">tax no.</span></span>
  
<span data-ttu-id="b5030-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-391">taxno#</span></span>
  
<span data-ttu-id="b5030-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-392">taxnumber#</span></span>
  
<span data-ttu-id="b5030-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="b5030-393">taxnumber</span></span>
  
<span data-ttu-id="b5030-394">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-394">tax id</span></span>
  
<span data-ttu-id="b5030-395">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-395">taxid#</span></span>
  
<span data-ttu-id="b5030-396">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-396">tax identification number</span></span>
  
<span data-ttu-id="b5030-397">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-397">tax identification no.</span></span>
  
<span data-ttu-id="b5030-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="b5030-398">steuernummer</span></span>
  
<span data-ttu-id="b5030-399">steuer id</span><span class="sxs-lookup"><span data-stu-id="b5030-399">steuer id</span></span>
  
<span data-ttu-id="b5030-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="b5030-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="b5030-401">그리스</span><span class="sxs-lookup"><span data-stu-id="b5030-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="b5030-402">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-402">Format</span></span>

<span data-ttu-id="b5030-403">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-404">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-404">Pattern</span></span>

<span data-ttu-id="b5030-405">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-406">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-406">Checksum</span></span>

<span data-ttu-id="b5030-407">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-408">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-408">Definition</span></span>

<span data-ttu-id="b5030-409">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-410">정규식이 해당 `Regex_greece_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-411">from `Keywords_greece_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b5030-412">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="b5030-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-414">afm</span><span class="sxs-lookup"><span data-stu-id="b5030-414">afm</span></span>
  
<span data-ttu-id="b5030-415">언급</span><span class="sxs-lookup"><span data-stu-id="b5030-415">tin</span></span>
  
<span data-ttu-id="b5030-416">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-416">tax id no.</span></span>
  
<span data-ttu-id="b5030-417">세금 번호 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-417">tax id no</span></span>
  
<span data-ttu-id="b5030-418">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-418">tax identification number</span></span>
  
<span data-ttu-id="b5030-419">세금 레지스트리 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-419">tax registry number</span></span>
  
<span data-ttu-id="b5030-420">세금 레지스트리 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-420">tax registry no.</span></span>
  
<span data-ttu-id="b5030-421">afm #</span><span class="sxs-lookup"><span data-stu-id="b5030-421">afm#</span></span>
  
<span data-ttu-id="b5030-422">언급</span><span class="sxs-lookup"><span data-stu-id="b5030-422">tin#</span></span>
  
<span data-ttu-id="b5030-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="b5030-423">taxidno#</span></span>
  
<span data-ttu-id="b5030-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="b5030-424">taxregistryno#</span></span>
  
<span data-ttu-id="b5030-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="b5030-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="b5030-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="b5030-426">aφμ</span></span>
  
<span data-ttu-id="b5030-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="b5030-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="b5030-428">φορολογικού μητρώου νο</span><span class="sxs-lookup"><span data-stu-id="b5030-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="b5030-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="b5030-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="b5030-430">헝가리</span><span class="sxs-lookup"><span data-stu-id="b5030-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="b5030-431">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-431">Format</span></span>

<span data-ttu-id="b5030-432">공백이 나 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-433">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-433">Pattern</span></span>

<span data-ttu-id="b5030-434">10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-434">Ten digits:</span></span>
  
-  <span data-ttu-id="b5030-435">"8" 이어야 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="b5030-436">날짜 01/01/1867과 개별 생년월일 사이의 일 수에 해당 하는 5 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="b5030-437">같은 날에 태어난 사람을 구별 하기 위해 기회가 만든 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="b5030-438">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="b5030-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-439">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-439">Checksum</span></span>

<span data-ttu-id="b5030-440">예</span><span class="sxs-lookup"><span data-stu-id="b5030-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-441">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-441">Definition</span></span>

<span data-ttu-id="b5030-442">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-443">이 함수 `Func_hungary_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-444">from `Keywords_hungary_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-445">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-446">이 함수 `Func_hungary_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-447">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="b5030-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-449">헝가리어 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="b5030-450">헝가리어 언급</span><span class="sxs-lookup"><span data-stu-id="b5030-450">hungarian tin</span></span>
  
<span data-ttu-id="b5030-451">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-451">tax id number</span></span>
  
<span data-ttu-id="b5030-452">vat 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-452">vat number</span></span>
  
<span data-ttu-id="b5030-453">세금 기관 아니요</span><span class="sxs-lookup"><span data-stu-id="b5030-453">tax authority no</span></span>
  
<span data-ttu-id="b5030-454">세금 id 세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-454">tax id tax identity number</span></span>
  
<span data-ttu-id="b5030-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-455">taxidnumber#</span></span>
  
<span data-ttu-id="b5030-456">언급</span><span class="sxs-lookup"><span data-stu-id="b5030-456">tin#</span></span>
  
<span data-ttu-id="b5030-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="b5030-457">hungatiantin#</span></span>
  
<span data-ttu-id="b5030-458">세금 식별 아니요</span><span class="sxs-lookup"><span data-stu-id="b5030-458">tax identification no</span></span>
  
<span data-ttu-id="b5030-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="b5030-459">taxidno#</span></span>
  
<span data-ttu-id="b5030-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="b5030-460">adóazonosító szám</span></span>
  
<span data-ttu-id="b5030-461">adószám</span><span class="sxs-lookup"><span data-stu-id="b5030-461">adószám</span></span>
  
<span data-ttu-id="b5030-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="b5030-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="b5030-463">Ireland</span><span class="sxs-lookup"><span data-stu-id="b5030-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="b5030-464">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-464">Format</span></span>

<span data-ttu-id="b5030-465">공백 또는 구분 기호가 없는 7 자리 숫자와 문자</span><span class="sxs-lookup"><span data-stu-id="b5030-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-466">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-466">Pattern</span></span>

<span data-ttu-id="b5030-467">7 자리 숫자와 문자</span><span class="sxs-lookup"><span data-stu-id="b5030-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="b5030-468">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-468">Seven digits</span></span> 
    
- <span data-ttu-id="b5030-469">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b5030-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-470">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-470">Checksum</span></span>

<span data-ttu-id="b5030-471">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-472">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-472">Definition</span></span>

<span data-ttu-id="b5030-473">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-474">이 함수 `Func_ireland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-475">from `Keywords_ireland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-476">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-477">이 함수 `Func_ireland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-478">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="b5030-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-480">공용 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-480">public service no</span></span>
  
<span data-ttu-id="b5030-481">개인 공용 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-481">personal public service no</span></span>
  
<span data-ttu-id="b5030-482">pps 아니요</span><span class="sxs-lookup"><span data-stu-id="b5030-482">pps no</span></span>
  
<span data-ttu-id="b5030-483">개인 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-483">personal service no</span></span>
  
<span data-ttu-id="b5030-484">pps 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-484">pps service no</span></span>
  
<span data-ttu-id="b5030-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="b5030-485">ppsno#</span></span>
  
<span data-ttu-id="b5030-486">아일랜드 pps 아니요</span><span class="sxs-lookup"><span data-stu-id="b5030-486">irish pps no</span></span>
  
<span data-ttu-id="b5030-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="b5030-487">publicserviceno#</span></span>
  
<span data-ttu-id="b5030-488">개인 공용 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-488">personal public service number</span></span>
  
<span data-ttu-id="b5030-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="b5030-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="b5030-490">pps uimh</span><span class="sxs-lookup"><span data-stu-id="b5030-490">pps uimh</span></span>
  
<span data-ttu-id="b5030-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="b5030-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="b5030-492">이탈리아</span><span class="sxs-lookup"><span data-stu-id="b5030-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="b5030-493">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-493">Format</span></span>

<span data-ttu-id="b5030-494">지정 된 패턴의 문자와 숫자 16 개</span><span class="sxs-lookup"><span data-stu-id="b5030-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-495">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-495">Pattern</span></span>

<span data-ttu-id="b5030-496">16 자의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="b5030-497">가족 이름에서 처음 세 개의 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="b5030-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="b5030-498">이름의 첫 번째, 세 번째 및 네 번째 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="b5030-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="b5030-499">출생 연도의 마지막 자리에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="b5030-500">출생 달에 해당 하는 1 자리 숫자는 알파벳 순으로 사용 되지만 a에서 E, H, L, M, P, R에 해당 하는 문자만 사용 되며, 따라서 1 월은 a와 10 월이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="b5030-501">남성의와 구별 하기 위해 여성의 경우 짝수에서 출생 일에 40이 추가 되는 출생 달의 날짜에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="b5030-502">사용자가 태어난 municipality 관련 지역 번호에 해당 하는 4 자리 숫자-국가 전체 코드를 외국 국가에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="b5030-503">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="b5030-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-504">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-504">Checksum</span></span>

<span data-ttu-id="b5030-505">예</span><span class="sxs-lookup"><span data-stu-id="b5030-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-506">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-506">Definition</span></span>

<span data-ttu-id="b5030-507">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-508">이 함수 `Func_italy_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-509">from `Keywords_italy_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-510">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-511">이 함수 `Func_italy_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-512">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="b5030-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-514">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-514">tax number</span></span>
  
<span data-ttu-id="b5030-515">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-515">tax no.</span></span>
  
<span data-ttu-id="b5030-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-516">taxno#</span></span>
  
<span data-ttu-id="b5030-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-517">taxnumber#</span></span>
  
<span data-ttu-id="b5030-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="b5030-518">taxnumber</span></span>
  
<span data-ttu-id="b5030-519">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-519">tax id</span></span>
  
<span data-ttu-id="b5030-520">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-520">taxid#</span></span>
  
<span data-ttu-id="b5030-521">회계 코드</span><span class="sxs-lookup"><span data-stu-id="b5030-521">fiscal code</span></span>
  
<span data-ttu-id="b5030-522">codice</span><span class="sxs-lookup"><span data-stu-id="b5030-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="b5030-523">라트비아</span><span class="sxs-lookup"><span data-stu-id="b5030-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="b5030-524">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-524">Format</span></span>

<span data-ttu-id="b5030-525">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-526">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-526">Pattern</span></span>

<span data-ttu-id="b5030-527">지정 된 패턴에서 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="b5030-528">출생 날짜에 해당 하는 6 자리 숫자 (ddmmyy)</span><span class="sxs-lookup"><span data-stu-id="b5030-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="b5030-529">출생 세기에 해당 하는 1 자리 숫자 이며, "0"은 19th 세기에 해당 하 고 "1"은 20th 세기에 해당 하며 21 세기에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="b5030-530">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-531">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-531">Checksum</span></span>

<span data-ttu-id="b5030-532">예</span><span class="sxs-lookup"><span data-stu-id="b5030-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-533">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-533">Definition</span></span>

<span data-ttu-id="b5030-534">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-535">이 함수 `Func_latvia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-536">from `Keywords_latvia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-537">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-538">이 함수 `Func_latvia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-539">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="b5030-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-541">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-541">tax number</span></span>
  
<span data-ttu-id="b5030-542">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-542">tax no.</span></span>
  
<span data-ttu-id="b5030-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-543">taxno#</span></span>
  
<span data-ttu-id="b5030-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-544">taxnumber#</span></span>
  
<span data-ttu-id="b5030-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="b5030-545">taxnumber</span></span>
  
<span data-ttu-id="b5030-546">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-546">tax id</span></span>
  
<span data-ttu-id="b5030-547">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-547">taxid#</span></span>
  
<span data-ttu-id="b5030-548">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-548">tax identification number</span></span>
  
<span data-ttu-id="b5030-549">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-549">tax identification no.</span></span>
  
<span data-ttu-id="b5030-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="b5030-550">nodokļa numurs</span></span>
  
<span data-ttu-id="b5030-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="b5030-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="b5030-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="b5030-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="b5030-553">리투아니아</span><span class="sxs-lookup"><span data-stu-id="b5030-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="b5030-554">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-554">Format</span></span>

<span data-ttu-id="b5030-555">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-556">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-556">Pattern</span></span>

<span data-ttu-id="b5030-557">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-558">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-558">Checksum</span></span>

<span data-ttu-id="b5030-559">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-560">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-560">Definition</span></span>

<span data-ttu-id="b5030-561">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-562">이 함수 `Func_lithuania_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-563">from `Keywords_lithuania_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-564">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-565">이 함수 `Func_lithuania_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-566">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="b5030-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-568">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-568">tax number</span></span>
  
<span data-ttu-id="b5030-569">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-569">tax no.</span></span>
  
<span data-ttu-id="b5030-570">세금 없음 #</span><span class="sxs-lookup"><span data-stu-id="b5030-570">tax no#</span></span>
  
<span data-ttu-id="b5030-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-571">taxnumber#</span></span>
  
<span data-ttu-id="b5030-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="b5030-572">taxnumber</span></span>
  
<span data-ttu-id="b5030-573">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-573">tax id</span></span>
  
<span data-ttu-id="b5030-574">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-574">taxid#</span></span>
  
<span data-ttu-id="b5030-575">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-575">tax identification number</span></span>
  
<span data-ttu-id="b5030-576">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-576">tax identification no.</span></span>
  
<span data-ttu-id="b5030-577">mokesčių id</span><span class="sxs-lookup"><span data-stu-id="b5030-577">mokesčių id</span></span>
  
<span data-ttu-id="b5030-578">mokesčių numeris</span><span class="sxs-lookup"><span data-stu-id="b5030-578">mokesčių numeris</span></span>
  
<span data-ttu-id="b5030-579">mokesčių identifikavimas numeris</span><span class="sxs-lookup"><span data-stu-id="b5030-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="b5030-580">셈</span><span class="sxs-lookup"><span data-stu-id="b5030-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="b5030-581">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-581">Format</span></span>

<span data-ttu-id="b5030-582">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-583">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-583">Pattern</span></span>

<span data-ttu-id="b5030-584">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="b5030-584">13 digits:</span></span>
  
-  <span data-ttu-id="b5030-585">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-585">11 digits</span></span> 
    
- <span data-ttu-id="b5030-586">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-587">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-587">Checksum</span></span>

<span data-ttu-id="b5030-588">예</span><span class="sxs-lookup"><span data-stu-id="b5030-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-589">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-589">Definition</span></span>

<span data-ttu-id="b5030-590">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-591">이 함수 `Func_luxemburg_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-592">from `Keywords_luxemburg_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-593">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-594">이 함수 `Func_luxemburg_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-595">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="b5030-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-597">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-597">tax number</span></span>
  
<span data-ttu-id="b5030-598">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-598">tax no.</span></span>
  
<span data-ttu-id="b5030-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-599">taxno#</span></span>
  
<span data-ttu-id="b5030-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-600">taxnumber#</span></span>
  
<span data-ttu-id="b5030-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="b5030-601">taxnumber</span></span>
  
<span data-ttu-id="b5030-602">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-602">tax id</span></span>
  
<span data-ttu-id="b5030-603">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-603">taxid#</span></span>
  
<span data-ttu-id="b5030-604">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-604">tax identification number</span></span>
  
<span data-ttu-id="b5030-605">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-605">tax identification no.</span></span>
  
<span data-ttu-id="b5030-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="b5030-606">steuernummer</span></span>
  
<span data-ttu-id="b5030-607">steuer id</span><span class="sxs-lookup"><span data-stu-id="b5030-607">steuer id</span></span>
  
<span data-ttu-id="b5030-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="b5030-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="b5030-609">몰타</span><span class="sxs-lookup"><span data-stu-id="b5030-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="b5030-610">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-610">Format</span></span>

<span data-ttu-id="b5030-611">몰타어 nationals의 경우 지정 된 패턴의 7 자리 및 한 문자</span><span class="sxs-lookup"><span data-stu-id="b5030-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="b5030-612">몰타어 이외의 nationals 및 몰타어 엔터티: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-613">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-613">Pattern</span></span>

<span data-ttu-id="b5030-614">몰타어 nationals: 7 자리 숫자 및 1 개 문자</span><span class="sxs-lookup"><span data-stu-id="b5030-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="b5030-615">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-615">Seven digits</span></span> 
    
- <span data-ttu-id="b5030-616">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="b5030-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="b5030-617">몰타어 이외의 nationals 및 몰타어 엔터티: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="b5030-618">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="b5030-619">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-619">Checksum</span></span>

<span data-ttu-id="b5030-620">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-621">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-621">Definition</span></span>

<span data-ttu-id="b5030-622">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-623">이 함수 `Func_malta_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-624">from `Keywords_malta_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-625">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-626">이 함수 `Func_malta_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-627">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="b5030-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-629">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-629">tax number</span></span>
  
<span data-ttu-id="b5030-630">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-630">tax no.</span></span>
  
<span data-ttu-id="b5030-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-631">taxno#</span></span>
  
<span data-ttu-id="b5030-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-632">taxnumber#</span></span>
  
<span data-ttu-id="b5030-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="b5030-633">taxnumber</span></span>
  
<span data-ttu-id="b5030-634">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-634">tax id</span></span>
  
<span data-ttu-id="b5030-635">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-635">taxid#</span></span>
  
<span data-ttu-id="b5030-636">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-636">tax identification number</span></span>
  
<span data-ttu-id="b5030-637">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-637">tax identification no.</span></span>
  
<span data-ttu-id="b5030-638">numru tat</span><span class="sxs-lookup"><span data-stu-id="b5030-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="b5030-639">id tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="b5030-639">id tat-taxxa</span></span>
  
<span data-ttu-id="b5030-640">numru ta ' taxxa</span><span class="sxs-lookup"><span data-stu-id="b5030-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="b5030-641">네덜란드</span><span class="sxs-lookup"><span data-stu-id="b5030-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="b5030-642">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-642">Format</span></span>

<span data-ttu-id="b5030-643">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-644">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-644">Pattern</span></span>

<span data-ttu-id="b5030-645">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="b5030-646">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-646">Checksum</span></span>

<span data-ttu-id="b5030-647">예</span><span class="sxs-lookup"><span data-stu-id="b5030-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-648">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-648">Definition</span></span>

<span data-ttu-id="b5030-649">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-650">이 함수 `Func_netherlands_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-651">from `Keywords_netherlands_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-652">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-653">이 함수 `Func_netherlands_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-654">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="b5030-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-656">네덜란드 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="b5030-657">네덜란드 세금 식별</span><span class="sxs-lookup"><span data-stu-id="b5030-657">netherlands tax identification</span></span>
  
<span data-ttu-id="b5030-658">netherland의 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="b5030-659">netherland의 세금 식별</span><span class="sxs-lookup"><span data-stu-id="b5030-659">netherland's tax identification</span></span>
  
<span data-ttu-id="b5030-660">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-660">tax identification number</span></span>
  
<span data-ttu-id="b5030-661">네덜란드어 세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-661">dutch tax id</span></span>
  
<span data-ttu-id="b5030-662">네덜란드어 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-662">dutch tax identification number</span></span>
  
<span data-ttu-id="b5030-663">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-663">tax id</span></span>
  
<span data-ttu-id="b5030-664">세금 id #</span><span class="sxs-lookup"><span data-stu-id="b5030-664">tax id#</span></span>
  
<span data-ttu-id="b5030-665">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-665">tax number</span></span>
  
<span data-ttu-id="b5030-666">세금 없음 #</span><span class="sxs-lookup"><span data-stu-id="b5030-666">tax no#</span></span>
  
<span data-ttu-id="b5030-667">세금</span><span class="sxs-lookup"><span data-stu-id="b5030-667">tax#</span></span>
  
<span data-ttu-id="b5030-668">언급</span><span class="sxs-lookup"><span data-stu-id="b5030-668">tin</span></span>
  
<span data-ttu-id="b5030-669">언급</span><span class="sxs-lookup"><span data-stu-id="b5030-669">tin#</span></span>
  
<span data-ttu-id="b5030-670">네덜란드 언급</span><span class="sxs-lookup"><span data-stu-id="b5030-670">netherlands tin</span></span>
  
<span data-ttu-id="b5030-671">netherland의 언급</span><span class="sxs-lookup"><span data-stu-id="b5030-671">netherland's tin</span></span>
  
<span data-ttu-id="b5030-672">nederlands belasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="b5030-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="b5030-673">identificatienummer van belasting</span><span class="sxs-lookup"><span data-stu-id="b5030-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="b5030-674">identificatienummer belasting</span><span class="sxs-lookup"><span data-stu-id="b5030-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="b5030-675">nederlands belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="b5030-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="b5030-676">nederlands belasting id nummer</span><span class="sxs-lookup"><span data-stu-id="b5030-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="b5030-677">nederlands belastingnummer</span><span class="sxs-lookup"><span data-stu-id="b5030-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="b5030-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="b5030-678">btw nummer</span></span>
  
<span data-ttu-id="b5030-679">nederlandse belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="b5030-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="b5030-680">폴란드</span><span class="sxs-lookup"><span data-stu-id="b5030-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="b5030-681">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-681">Format</span></span>

<span data-ttu-id="b5030-682">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-683">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-683">Pattern</span></span>

<span data-ttu-id="b5030-684">11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-685">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-685">Checksum</span></span>

<span data-ttu-id="b5030-686">예</span><span class="sxs-lookup"><span data-stu-id="b5030-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-687">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-687">Definition</span></span>

<span data-ttu-id="b5030-688">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-689">이 함수 `Func_poland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-690">from `Keywords_poland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-691">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-692">이 함수 `Func_poland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-693">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="b5030-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-695">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-695">tax number</span></span>
  
<span data-ttu-id="b5030-696">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-696">tax no.</span></span>
  
<span data-ttu-id="b5030-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-697">taxno#</span></span>
  
<span data-ttu-id="b5030-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-698">taxnumber#</span></span>
  
<span data-ttu-id="b5030-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="b5030-699">taxnumber</span></span>
  
<span data-ttu-id="b5030-700">nip</span><span class="sxs-lookup"><span data-stu-id="b5030-700">nip</span></span>
  
<span data-ttu-id="b5030-701">nip #</span><span class="sxs-lookup"><span data-stu-id="b5030-701">nip#</span></span>
  
<span data-ttu-id="b5030-702">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-702">tax id</span></span>
  
<span data-ttu-id="b5030-703">세금 id #</span><span class="sxs-lookup"><span data-stu-id="b5030-703">tax id#</span></span>
  
<span data-ttu-id="b5030-704">nip id</span><span class="sxs-lookup"><span data-stu-id="b5030-704">nip id</span></span>
  
<span data-ttu-id="b5030-705">nip id #</span><span class="sxs-lookup"><span data-stu-id="b5030-705">nip id#</span></span>
  
<span data-ttu-id="b5030-706">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-706">tax identification number</span></span>
  
<span data-ttu-id="b5030-707">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-707">tax identification no.</span></span>
  
<span data-ttu-id="b5030-708">vat 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-708">vat number</span></span>
  
<span data-ttu-id="b5030-709">vat 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-709">vat no.</span></span>
  
<span data-ttu-id="b5030-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="b5030-710">vatno#</span></span>
  
<span data-ttu-id="b5030-711">vat id</span><span class="sxs-lookup"><span data-stu-id="b5030-711">vat id</span></span>
  
<span data-ttu-id="b5030-712">vat id #</span><span class="sxs-lookup"><span data-stu-id="b5030-712">vat id#</span></span>
  
<span data-ttu-id="b5030-713">u r i identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="b5030-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="b5030-714">정책 스키 u r i identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="b5030-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="b5030-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="b5030-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="b5030-716">포르투갈</span><span class="sxs-lookup"><span data-stu-id="b5030-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="b5030-717">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-717">Format</span></span>

<span data-ttu-id="b5030-718">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-719">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-719">Pattern</span></span>

<span data-ttu-id="b5030-720">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-721">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-721">Checksum</span></span>

<span data-ttu-id="b5030-722">예</span><span class="sxs-lookup"><span data-stu-id="b5030-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-723">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-723">Definition</span></span>

<span data-ttu-id="b5030-724">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-725">이 함수 `Func_portugal_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-726">from `Keywords_portugal_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-727">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-728">이 함수 `Func_portugal_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-729">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="b5030-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-731">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-731">tax number</span></span>
  
<span data-ttu-id="b5030-732">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-732">tax no.</span></span>
  
<span data-ttu-id="b5030-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-733">taxno#</span></span>
  
<span data-ttu-id="b5030-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="b5030-734">taxnumber#</span></span>
  
<span data-ttu-id="b5030-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="b5030-735">taxnumber</span></span>
  
<span data-ttu-id="b5030-736">m</span><span class="sxs-lookup"><span data-stu-id="b5030-736">nif</span></span>
  
<span data-ttu-id="b5030-737">m</span><span class="sxs-lookup"><span data-stu-id="b5030-737">nif#</span></span>
  
<span data-ttu-id="b5030-738">numero 회계</span><span class="sxs-lookup"><span data-stu-id="b5030-738">numero fiscal</span></span>
  
<span data-ttu-id="b5030-739">número de identificação 회계</span><span class="sxs-lookup"><span data-stu-id="b5030-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="b5030-740">루마니아</span><span class="sxs-lookup"><span data-stu-id="b5030-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="b5030-741">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-741">Format</span></span>

<span data-ttu-id="b5030-742">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-743">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-743">Pattern</span></span>

<span data-ttu-id="b5030-744">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-745">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-745">Checksum</span></span>

<span data-ttu-id="b5030-746">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-747">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-747">Definition</span></span>

<span data-ttu-id="b5030-748">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-749">정규식이 해당 `Regex_romania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-750">from `Keywords_romania_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b5030-751">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="b5030-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-753">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-753">tax id</span></span>
  
<span data-ttu-id="b5030-754">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-754">tax id number</span></span>
  
<span data-ttu-id="b5030-755">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-755">tax file no</span></span>
  
<span data-ttu-id="b5030-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="b5030-756">tax file number</span></span>
  
<span data-ttu-id="b5030-757">세금 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-757">tax no</span></span>
  
<span data-ttu-id="b5030-758">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-758">tax number</span></span>
  
<span data-ttu-id="b5030-759">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-759">taxid#</span></span>
  
<span data-ttu-id="b5030-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-760">taxno#</span></span>
  
<span data-ttu-id="b5030-761">id-ul taxei</span><span class="sxs-lookup"><span data-stu-id="b5030-761">id-ul taxei</span></span>
  
<span data-ttu-id="b5030-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="b5030-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="b5030-763">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="b5030-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="b5030-764">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-764">Format</span></span>

<span data-ttu-id="b5030-765">공백이 나 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-766">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-766">Pattern</span></span>

<span data-ttu-id="b5030-767">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-768">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-768">Checksum</span></span>

<span data-ttu-id="b5030-769">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-770">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-770">Definition</span></span>

<span data-ttu-id="b5030-771">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-772">정규식이 해당 `Regex_slovakia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-773">from `Keywords_slovakia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b5030-774">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="b5030-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-776">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-776">tax id</span></span>
  
<span data-ttu-id="b5030-777">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-777">tax id number</span></span>
  
<span data-ttu-id="b5030-778">언급 id</span><span class="sxs-lookup"><span data-stu-id="b5030-778">tin id</span></span>
  
<span data-ttu-id="b5030-779">언급 아니요</span><span class="sxs-lookup"><span data-stu-id="b5030-779">tin no</span></span>
  
<span data-ttu-id="b5030-780">슬로바키아어 언급 id</span><span class="sxs-lookup"><span data-stu-id="b5030-780">slovakian tin id</span></span>
  
<span data-ttu-id="b5030-781">언급</span><span class="sxs-lookup"><span data-stu-id="b5030-781">tin</span></span>
  
<span data-ttu-id="b5030-782">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-782">tax file no</span></span>
  
<span data-ttu-id="b5030-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="b5030-783">tax file number</span></span>
  
<span data-ttu-id="b5030-784">세금 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-784">tax no</span></span>
  
<span data-ttu-id="b5030-785">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-785">tax number</span></span>
  
<span data-ttu-id="b5030-786">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-786">taxid#</span></span>
  
<span data-ttu-id="b5030-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-787">taxno#</span></span>
  
<span data-ttu-id="b5030-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="b5030-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="b5030-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="b5030-789">daňové číslo</span></span>
  
<span data-ttu-id="b5030-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="b5030-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="b5030-791">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="b5030-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="b5030-792">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-792">Format</span></span>

<span data-ttu-id="b5030-793">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-794">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-794">Pattern</span></span>

<span data-ttu-id="b5030-795">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-796">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-796">Checksum</span></span>

<span data-ttu-id="b5030-797">예</span><span class="sxs-lookup"><span data-stu-id="b5030-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-798">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-798">Definition</span></span>

<span data-ttu-id="b5030-799">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-800">이 함수 `Func_slovenia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-801">from `Keywords_slovenia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-802">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-803">이 함수 `Func_slovenia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-804">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="b5030-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-806">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-806">tax id</span></span>
  
<span data-ttu-id="b5030-807">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-807">tax id number</span></span>
  
<span data-ttu-id="b5030-808">언급 id</span><span class="sxs-lookup"><span data-stu-id="b5030-808">tin id</span></span>
  
<span data-ttu-id="b5030-809">언급 아니요</span><span class="sxs-lookup"><span data-stu-id="b5030-809">tin no</span></span>
  
<span data-ttu-id="b5030-810">슬로베니아어 언급 id</span><span class="sxs-lookup"><span data-stu-id="b5030-810">slovenian tin id</span></span>
  
<span data-ttu-id="b5030-811">언급</span><span class="sxs-lookup"><span data-stu-id="b5030-811">tin</span></span>
  
<span data-ttu-id="b5030-812">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-812">tax file no</span></span>
  
<span data-ttu-id="b5030-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="b5030-813">tax file number</span></span>
  
<span data-ttu-id="b5030-814">세금 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-814">tax no</span></span>
  
<span data-ttu-id="b5030-815">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-815">tax number</span></span>
  
<span data-ttu-id="b5030-816">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-816">taxid#</span></span>
  
<span data-ttu-id="b5030-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-817">taxno#</span></span>
  
<span data-ttu-id="b5030-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="b5030-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="b5030-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="b5030-819">davčna številka</span></span>
  
<span data-ttu-id="b5030-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="b5030-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="b5030-821">스페인</span><span class="sxs-lookup"><span data-stu-id="b5030-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="b5030-822">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-822">Format</span></span>

<span data-ttu-id="b5030-823">지정 된 패턴에 7 ~ 8 자리 숫자와 한 가지 또는 두 개의 문자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-824">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-824">Pattern</span></span>

<span data-ttu-id="b5030-825">스페인 국내 id 카드가 있는 스페인어 (자연 사용자):</span><span class="sxs-lookup"><span data-stu-id="b5030-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="b5030-826">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-826">Eight digits</span></span> 
    
- <span data-ttu-id="b5030-827">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="b5030-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="b5030-828">스페인 국가 id 카드가 없는 상주 하지 않는 Spaniards</span><span class="sxs-lookup"><span data-stu-id="b5030-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="b5030-829">1 개의 대문자 "L" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="b5030-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="b5030-830">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-830">Seven digits</span></span>
    
- <span data-ttu-id="b5030-831">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="b5030-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="b5030-832">스페인 국가 id 카드를 사용 하지 않고 14 년 동안 상주 하는 Spaniards:</span><span class="sxs-lookup"><span data-stu-id="b5030-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="b5030-833">1 개의 대문자 "K" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="b5030-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="b5030-834">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-834">Seven digits</span></span> 
    
- <span data-ttu-id="b5030-835">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="b5030-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="b5030-836">Foreigner의 식별 번호를 사용 하는 Foreigners</span><span class="sxs-lookup"><span data-stu-id="b5030-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="b5030-837">"X", "Y" 또는 "Z" (대/소문자 구분)의 대문자 1 개</span><span class="sxs-lookup"><span data-stu-id="b5030-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="b5030-838">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-838">Seven digits</span></span>
    
- <span data-ttu-id="b5030-839">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="b5030-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="b5030-840">Foreigner의 id 번호가 없는 Foreigners</span><span class="sxs-lookup"><span data-stu-id="b5030-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="b5030-841">"M"을 나타내는 대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="b5030-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="b5030-842">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-842">Seven digits</span></span>
    
- <span data-ttu-id="b5030-843">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="b5030-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="b5030-844">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-844">Checksum</span></span>

<span data-ttu-id="b5030-845">예</span><span class="sxs-lookup"><span data-stu-id="b5030-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-846">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-846">Definition</span></span>

<span data-ttu-id="b5030-847">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-848">이 함수 `Func_spain_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-849">from `Keywords_spain_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-850">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-851">이 함수 `Func_spain_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-852">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="b5030-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-854">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-854">tax id</span></span>
  
<span data-ttu-id="b5030-855">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-855">tax id number</span></span>
  
<span data-ttu-id="b5030-856">cif id</span><span class="sxs-lookup"><span data-stu-id="b5030-856">cif id</span></span>
  
<span data-ttu-id="b5030-857">cif 아니요</span><span class="sxs-lookup"><span data-stu-id="b5030-857">cif no</span></span>
  
<span data-ttu-id="b5030-858">스페인어 cif id</span><span class="sxs-lookup"><span data-stu-id="b5030-858">spanish cif id</span></span>
  
<span data-ttu-id="b5030-859">cif</span><span class="sxs-lookup"><span data-stu-id="b5030-859">cif</span></span>
  
<span data-ttu-id="b5030-860">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-860">tax file no</span></span>
  
<span data-ttu-id="b5030-861">스페인어 cif 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-861">spanish cif number</span></span>
  
<span data-ttu-id="b5030-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="b5030-862">tax file number</span></span>
  
<span data-ttu-id="b5030-863">스페인어 cif 아니요</span><span class="sxs-lookup"><span data-stu-id="b5030-863">spanish cif no</span></span>
  
<span data-ttu-id="b5030-864">세금 없음</span><span class="sxs-lookup"><span data-stu-id="b5030-864">tax no</span></span>
  
<span data-ttu-id="b5030-865">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-865">tax number</span></span>
  
<span data-ttu-id="b5030-866">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-866">taxid#</span></span>
  
<span data-ttu-id="b5030-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="b5030-867">taxno#</span></span>
  
<span data-ttu-id="b5030-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="b5030-868">cifid#</span></span>
  
<span data-ttu-id="b5030-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="b5030-869">spanishcifid#</span></span>
  
<span data-ttu-id="b5030-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="b5030-870">spanishcifno#</span></span>
  
<span data-ttu-id="b5030-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="b5030-871">número de contribuyente</span></span>
  
<span data-ttu-id="b5030-872">número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="b5030-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="b5030-873">número de identificación 회계</span><span class="sxs-lookup"><span data-stu-id="b5030-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="b5030-874">cif número</span><span class="sxs-lookup"><span data-stu-id="b5030-874">cif número</span></span>
  
<span data-ttu-id="b5030-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="b5030-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="b5030-876">스웨덴</span><span class="sxs-lookup"><span data-stu-id="b5030-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="b5030-877">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-877">Format</span></span>

<span data-ttu-id="b5030-878">지정 된 패턴의 10 자리 숫자와 기호</span><span class="sxs-lookup"><span data-stu-id="b5030-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-879">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-879">Pattern</span></span>

<span data-ttu-id="b5030-880">10 자리 숫자와 기호:</span><span class="sxs-lookup"><span data-stu-id="b5030-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="b5030-881">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="b5030-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="b5030-882">더하기 기호, 빼기 기호 또는 백슬래시</span><span class="sxs-lookup"><span data-stu-id="b5030-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="b5030-883">다음은 식별 번호를 고유 하 게 만드는 3 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="b5030-884">1990 이전에 실행 된 번호의 경우 일곱째 및 여덟 번째 숫자는 출생 또는 외부에서 태어난 사람의 국가를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="b5030-885">아홉 번째 위치의 숫자는 성별에 대 한 홀수 또는 암도를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="b5030-886">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="b5030-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b5030-887">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-887">Checksum</span></span>

<span data-ttu-id="b5030-888">예</span><span class="sxs-lookup"><span data-stu-id="b5030-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-889">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-889">Definition</span></span>

<span data-ttu-id="b5030-890">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-891">이 함수 `Func_sweden_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-892">from `Keywords_sweden_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="b5030-893">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-894">이 함수 `Func_sweden_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b5030-895">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="b5030-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-897">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-897">tax id</span></span>
  
<span data-ttu-id="b5030-898">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-898">tax id no.</span></span>
  
<span data-ttu-id="b5030-899">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-899">tax id number</span></span>
  
<span data-ttu-id="b5030-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="b5030-900">tax identification</span></span>
  
<span data-ttu-id="b5030-901">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-901">tax identification#</span></span>
  
<span data-ttu-id="b5030-902">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-902">tax no.</span></span>
  
<span data-ttu-id="b5030-903">세금</span><span class="sxs-lookup"><span data-stu-id="b5030-903">tax#</span></span>
  
<span data-ttu-id="b5030-904">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-904">taxid#</span></span>
  
<span data-ttu-id="b5030-905">세금 파일</span><span class="sxs-lookup"><span data-stu-id="b5030-905">tax file</span></span>
  
<span data-ttu-id="b5030-906">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-906">tax file no.</span></span>
  
<span data-ttu-id="b5030-907">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-907">personal id number</span></span>
  
<span data-ttu-id="b5030-908">(nummer at&t id)</span><span class="sxs-lookup"><span data-stu-id="b5030-908">skatt id nummer</span></span>
  
<span data-ttu-id="b5030-909">identifikation at&t</span><span class="sxs-lookup"><span data-stu-id="b5030-909">skatt identifikation</span></span>
  
<span data-ttu-id="b5030-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="b5030-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="b5030-911">영국의</span><span class="sxs-lookup"><span data-stu-id="b5030-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="b5030-912">형식일</span><span class="sxs-lookup"><span data-stu-id="b5030-912">Format</span></span>

<span data-ttu-id="b5030-913">utr (Unique Taxpayer Reference): 공백 및 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="b5030-914">국가 보험 번호 (NINO): 자세한 내용은 영국 섹션 "을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5030-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="b5030-915">[중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)국가 보험 번호 (NINO) "입니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b5030-916">패턴</span><span class="sxs-lookup"><span data-stu-id="b5030-916">Pattern</span></span>

<span data-ttu-id="b5030-917">utr (Unique Taxpayer Reference): 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="b5030-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="b5030-918">국가 보험 번호 (NINO): 자세한 내용은 영국 섹션 "을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5030-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="b5030-919">[중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)국가 보험 번호 (NINO) "입니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b5030-920">제외</span><span class="sxs-lookup"><span data-stu-id="b5030-920">Checksum</span></span>

<span data-ttu-id="b5030-921">예</span><span class="sxs-lookup"><span data-stu-id="b5030-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b5030-922">정의</span><span class="sxs-lookup"><span data-stu-id="b5030-922">Definition</span></span>

<span data-ttu-id="b5030-923">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b5030-924">이 함수 `Func_uk_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b5030-925">from `Keywords_uk_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="b5030-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b5030-926">키워드</span><span class="sxs-lookup"><span data-stu-id="b5030-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="b5030-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b5030-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="b5030-928">tax id</span><span class="sxs-lookup"><span data-stu-id="b5030-928">tax id</span></span>
  
<span data-ttu-id="b5030-929">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-929">tax id no.</span></span>
  
<span data-ttu-id="b5030-930">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-930">tax id number</span></span>
  
<span data-ttu-id="b5030-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="b5030-931">tax identification</span></span>
  
<span data-ttu-id="b5030-932">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-932">tax identification#</span></span>
  
<span data-ttu-id="b5030-933">세금 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-933">tax no.</span></span>
  
<span data-ttu-id="b5030-934">세금</span><span class="sxs-lookup"><span data-stu-id="b5030-934">tax#</span></span>
  
<span data-ttu-id="b5030-935">taxid #</span><span class="sxs-lookup"><span data-stu-id="b5030-935">taxid#</span></span>
  
<span data-ttu-id="b5030-936">세금 파일</span><span class="sxs-lookup"><span data-stu-id="b5030-936">tax file</span></span>
  
<span data-ttu-id="b5030-937">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="b5030-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5030-938">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b5030-938">See also</span></span>

[<span data-ttu-id="b5030-939">중요한 정보 유형이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="b5030-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

