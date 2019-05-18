---
title: EU 세금 확인 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 EU 세금 식별 번호 중요 정보 유형을 검색할 때 DLP (데이터 손실 방지) 정책이 어떤 역할을 검색 하나요를 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: adcd9be9b5f8775ad39010d771ff2ac214df1e17
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152960"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="53926-104">EU 세금 확인 번호</span><span class="sxs-lookup"><span data-stu-id="53926-104">EU Tax Identification Number</span></span>

<span data-ttu-id="53926-105">이 항목에서는 언급 (데이터 손실 방지) 정책이 EU (유럽 세금 식별 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53926-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="53926-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="53926-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="53926-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="53926-108">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-108">Format</span></span>

<span data-ttu-id="53926-109">하이픈 및 슬래시가 있는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-110">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-110">Pattern</span></span>

<span data-ttu-id="53926-111">하이픈 및 슬래시가 있는 9 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="53926-112">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-112">Two digits</span></span> 
    
- <span data-ttu-id="53926-113">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53926-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="53926-114">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-114">Three digits</span></span>
    
- <span data-ttu-id="53926-115">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53926-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="53926-116">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-117">제외</span><span class="sxs-lookup"><span data-stu-id="53926-117">Checksum</span></span>

<span data-ttu-id="53926-118">예</span><span class="sxs-lookup"><span data-stu-id="53926-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-119">정의</span><span class="sxs-lookup"><span data-stu-id="53926-119">Definition</span></span>

<span data-ttu-id="53926-120">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-121">이 함수 `Func_austria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-122">From `Keywords_austria_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-123">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-124">이 함수 `Func_austria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-125">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="53926-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="53926-127">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-127">tax number</span></span>
  
<span data-ttu-id="53926-128">수</span><span class="sxs-lookup"><span data-stu-id="53926-128">number</span></span>
  
<span data-ttu-id="53926-129">세금 등록 번호</span><span class="sxs-lookup"><span data-stu-id="53926-129">tax registration number</span></span>
  
<span data-ttu-id="53926-130">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-130">tax id</span></span>
  
<span data-ttu-id="53926-131">st.nr</span><span class="sxs-lookup"><span data-stu-id="53926-131">st.nr.</span></span>
  
<span data-ttu-id="53926-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="53926-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="53926-133">벨기에</span><span class="sxs-lookup"><span data-stu-id="53926-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="53926-134">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-134">Format</span></span>

<span data-ttu-id="53926-135">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-136">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-136">Pattern</span></span>

<span data-ttu-id="53926-137">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-137">11 digits:</span></span>
  
- <span data-ttu-id="53926-138">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-138">Two digits</span></span>
    
- <span data-ttu-id="53926-139">"0" 또는 "1"</span><span class="sxs-lookup"><span data-stu-id="53926-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="53926-140">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-140">One digit</span></span>
    
- <span data-ttu-id="53926-141">"0" 또는 "1" 또는 "2" 또는 "3"</span><span class="sxs-lookup"><span data-stu-id="53926-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="53926-142">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-143">제외</span><span class="sxs-lookup"><span data-stu-id="53926-143">Checksum</span></span>

<span data-ttu-id="53926-144">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-145">정의</span><span class="sxs-lookup"><span data-stu-id="53926-145">Definition</span></span>

<span data-ttu-id="53926-146">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-147">정규식이 해당 `Regex_belgium_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-148">From `Keywords_belgium_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53926-149">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="53926-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="53926-151">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-151">tax number</span></span>
  
<span data-ttu-id="53926-152">국가 등록 번호</span><span class="sxs-lookup"><span data-stu-id="53926-152">national registration number</span></span>
  
<span data-ttu-id="53926-153">세금 등록 번호</span><span class="sxs-lookup"><span data-stu-id="53926-153">tax registration number</span></span>
  
<span data-ttu-id="53926-154">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-154">tax id</span></span>
  
<span data-ttu-id="53926-155">m</span><span class="sxs-lookup"><span data-stu-id="53926-155">nif</span></span>
  
<span data-ttu-id="53926-156">m</span><span class="sxs-lookup"><span data-stu-id="53926-156">nif#</span></span>
  
<span data-ttu-id="53926-157">numéro de registre 국립</span><span class="sxs-lookup"><span data-stu-id="53926-157">numéro de registre national</span></span>
  
<span data-ttu-id="53926-158">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="53926-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="53926-159">불가리아</span><span class="sxs-lookup"><span data-stu-id="53926-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="53926-160">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-160">Format</span></span>

<span data-ttu-id="53926-161">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-162">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-162">Pattern</span></span>

<span data-ttu-id="53926-163">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-164">제외</span><span class="sxs-lookup"><span data-stu-id="53926-164">Checksum</span></span>

<span data-ttu-id="53926-165">예</span><span class="sxs-lookup"><span data-stu-id="53926-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-166">정의</span><span class="sxs-lookup"><span data-stu-id="53926-166">Definition</span></span>

<span data-ttu-id="53926-167">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-168">이 함수 `Func_bulgaria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-169">From `Keywords_bulgaria_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-170">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-171">이 함수 `Func_bulgaria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-172">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="53926-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="53926-174">고 대 cn</span><span class="sxs-lookup"><span data-stu-id="53926-174">bucn</span></span>
  
<span data-ttu-id="53926-175">일관적인 민사 번호</span><span class="sxs-lookup"><span data-stu-id="53926-175">uniform civil number</span></span>
  
<span data-ttu-id="53926-176">과 (와) cn #</span><span class="sxs-lookup"><span data-stu-id="53926-176">bucn#</span></span>
  
<span data-ttu-id="53926-177">uniformcivilnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="53926-178">일정 한 민사 일련번호</span><span class="sxs-lookup"><span data-stu-id="53926-178">uniform civil id</span></span>
  
<span data-ttu-id="53926-179">일관적인 민사</span><span class="sxs-lookup"><span data-stu-id="53926-179">uniform civil no</span></span>
  
<span data-ttu-id="53926-180">egn</span><span class="sxs-lookup"><span data-stu-id="53926-180">egn</span></span>
  
<span data-ttu-id="53926-181">불가리아어 (민사)</span><span class="sxs-lookup"><span data-stu-id="53926-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="53926-182">uniformcivilno#</span><span class="sxs-lookup"><span data-stu-id="53926-182">uniformcivilno#</span></span>
  
<span data-ttu-id="53926-183">egn#</span><span class="sxs-lookup"><span data-stu-id="53926-183">egn#</span></span>
  
<span data-ttu-id="53926-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="53926-184">униформ граждански номер</span></span>
  
<span data-ttu-id="53926-185">униформ id</span><span class="sxs-lookup"><span data-stu-id="53926-185">униформ id</span></span>
  
<span data-ttu-id="53926-186">униформ граждански id</span><span class="sxs-lookup"><span data-stu-id="53926-186">униформ граждански id</span></span>
  
<span data-ttu-id="53926-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="53926-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="53926-188">크로아티아</span><span class="sxs-lookup"><span data-stu-id="53926-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="53926-189">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-189">Format</span></span>

<span data-ttu-id="53926-190">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-191">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-191">Pattern</span></span>

<span data-ttu-id="53926-192">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-192">11 digits:</span></span>
  
- <span data-ttu-id="53926-193">임의로 선택한 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="53926-194">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="53926-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-195">제외</span><span class="sxs-lookup"><span data-stu-id="53926-195">Checksum</span></span>

<span data-ttu-id="53926-196">예</span><span class="sxs-lookup"><span data-stu-id="53926-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-197">정의</span><span class="sxs-lookup"><span data-stu-id="53926-197">Definition</span></span>

<span data-ttu-id="53926-198">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-199">이 함수 `Func_croatia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-200">From `Keywords_croatia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-202">이 함수 `Func_croatia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-203">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="53926-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="53926-205">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-205">tax number</span></span>
  
<span data-ttu-id="53926-206">세금</span><span class="sxs-lookup"><span data-stu-id="53926-206">tax</span></span>
  
<span data-ttu-id="53926-207">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-207">tax id</span></span>
  
<span data-ttu-id="53926-208">원환형</span><span class="sxs-lookup"><span data-stu-id="53926-208">oid</span></span>
  
<span data-ttu-id="53926-209">원환형</span><span class="sxs-lookup"><span data-stu-id="53926-209">oid#</span></span>
  
<span data-ttu-id="53926-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="53926-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="53926-211">키프로스</span><span class="sxs-lookup"><span data-stu-id="53926-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="53926-212">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-212">Format</span></span>

<span data-ttu-id="53926-213">지정 된 패턴에서 8 자리 및 1 개 문자</span><span class="sxs-lookup"><span data-stu-id="53926-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-214">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-214">Pattern</span></span>

<span data-ttu-id="53926-215">8 자리 숫자와 1 개 문자:</span><span class="sxs-lookup"><span data-stu-id="53926-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="53926-216">"0"</span><span class="sxs-lookup"><span data-stu-id="53926-216">A "0"</span></span> 
    
- <span data-ttu-id="53926-217">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-217">Seven digits</span></span>
    
- <span data-ttu-id="53926-218">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="53926-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-219">제외</span><span class="sxs-lookup"><span data-stu-id="53926-219">Checksum</span></span>

<span data-ttu-id="53926-220">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-221">정의</span><span class="sxs-lookup"><span data-stu-id="53926-221">Definition</span></span>

<span data-ttu-id="53926-222">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-223">이 함수 `Func_cyprus_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-224">From `Keywords_cyprus_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-225">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-226">이 함수 `Func_cyprus_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-227">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="53926-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="53926-229">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-229">tax number</span></span>
  
<span data-ttu-id="53926-230">세금</span><span class="sxs-lookup"><span data-stu-id="53926-230">tax</span></span>
  
<span data-ttu-id="53926-231">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-231">tax id</span></span>
  
<span data-ttu-id="53926-232">세금 식별 코드</span><span class="sxs-lookup"><span data-stu-id="53926-232">tax identification code</span></span>
  
<span data-ttu-id="53926-233">tic</span><span class="sxs-lookup"><span data-stu-id="53926-233">tic</span></span>
  
<span data-ttu-id="53926-234">tic#</span><span class="sxs-lookup"><span data-stu-id="53926-234">tic#</span></span>
  
<span data-ttu-id="53926-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="53926-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="53926-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="53926-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="53926-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="53926-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="53926-238">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="53926-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="53926-239">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-239">Format</span></span>

<span data-ttu-id="53926-240">선택적 백슬래시가 있는 9 자리 또는 10 진수</span><span class="sxs-lookup"><span data-stu-id="53926-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-241">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-241">Pattern</span></span>

<span data-ttu-id="53926-242">선택적 backslashl이 있는 아홉 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="53926-243">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-243">Six digits</span></span> 
    
- <span data-ttu-id="53926-244">백슬래시 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53926-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="53926-245">3 ~ 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-246">제외</span><span class="sxs-lookup"><span data-stu-id="53926-246">Checksum</span></span>

<span data-ttu-id="53926-247">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-248">정의</span><span class="sxs-lookup"><span data-stu-id="53926-248">Definition</span></span>

<span data-ttu-id="53926-249">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-250">정규식이 해당 `Regex_czech_republic_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-251">From `Keywords_czech_republic_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53926-252">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="53926-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="53926-254">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-254">tax number</span></span>
  
<span data-ttu-id="53926-255">세금</span><span class="sxs-lookup"><span data-stu-id="53926-255">tax</span></span>
  
<span data-ttu-id="53926-256">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-256">tax id</span></span>
  
<span data-ttu-id="53926-257">개인 번호</span><span class="sxs-lookup"><span data-stu-id="53926-257">personal number</span></span>
  
<span data-ttu-id="53926-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="53926-258">daňové číslo</span></span>
  
<span data-ttu-id="53926-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="53926-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="53926-260">덴마크</span><span class="sxs-lookup"><span data-stu-id="53926-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="53926-261">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-261">Format</span></span>

<span data-ttu-id="53926-262">하이픈을 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-263">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-263">Pattern</span></span>

<span data-ttu-id="53926-264">Hyphenl를 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="53926-265">생년월일에 해당 하는 6 자리 숫자 (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="53926-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="53926-266">하이픈</span><span class="sxs-lookup"><span data-stu-id="53926-266">A hyphen</span></span>
    
- <span data-ttu-id="53926-267">첫 번째 숫자가 출생 세기에 해당 하 고 마지막 숫자가 개별 성별에 해당 하는 시퀀스 번호에 해당 하는 4 자리 숫자 (남성의 경우 홀수 및 암에도 해당)</span><span class="sxs-lookup"><span data-stu-id="53926-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-268">제외</span><span class="sxs-lookup"><span data-stu-id="53926-268">Checksum</span></span>

<span data-ttu-id="53926-269">예</span><span class="sxs-lookup"><span data-stu-id="53926-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-270">정의</span><span class="sxs-lookup"><span data-stu-id="53926-270">Definition</span></span>

<span data-ttu-id="53926-271">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-272">이 함수 `Func_denmark_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-273">From `Keywords_denmark_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-274">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-275">이 함수 `Func_denmark_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-276">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="53926-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="53926-278">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-278">tax number</span></span>
  
<span data-ttu-id="53926-279">세금</span><span class="sxs-lookup"><span data-stu-id="53926-279">tax</span></span>
  
<span data-ttu-id="53926-280">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-280">tax id</span></span>
  
<span data-ttu-id="53926-281">cpr 번호</span><span class="sxs-lookup"><span data-stu-id="53926-281">cpr number</span></span>
  
<span data-ttu-id="53926-282">cpr#</span><span class="sxs-lookup"><span data-stu-id="53926-282">cpr#</span></span>
  
<span data-ttu-id="53926-283">nummer에서</span><span class="sxs-lookup"><span data-stu-id="53926-283">skat nummer</span></span>
  
<span data-ttu-id="53926-284">번호 (|)</span><span class="sxs-lookup"><span data-stu-id="53926-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="53926-285">에스토니아</span><span class="sxs-lookup"><span data-stu-id="53926-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="53926-286">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-286">Format</span></span>

<span data-ttu-id="53926-287">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-288">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-288">Pattern</span></span>

<span data-ttu-id="53926-289">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-289">11 digits:</span></span>
  
-  <span data-ttu-id="53926-290">성별에 해당 하는 숫자와 홀수로 해당 하 고, 홀수를 지정 하 여 19th 세기에 대해 1, 2를 나타내는 숫자입니다. 3, 20th 세기에 대해 4를 적용 합니다. 21 세기에 대해 5, 6</span><span class="sxs-lookup"><span data-stu-id="53926-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="53926-291">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="53926-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="53926-292">같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="53926-293">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="53926-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-294">제외</span><span class="sxs-lookup"><span data-stu-id="53926-294">Checksum</span></span>

<span data-ttu-id="53926-295">예</span><span class="sxs-lookup"><span data-stu-id="53926-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-296">정의</span><span class="sxs-lookup"><span data-stu-id="53926-296">Definition</span></span>

<span data-ttu-id="53926-297">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-298">이 함수 `Func_estonia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-299">From `Keywords_estonia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-300">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-301">이 함수 `Func_estonia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-302">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="53926-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="53926-304">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-304">tax number</span></span>
  
<span data-ttu-id="53926-305">세금</span><span class="sxs-lookup"><span data-stu-id="53926-305">tax</span></span>
  
<span data-ttu-id="53926-306">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-306">tax id</span></span>
  
<span data-ttu-id="53926-307">개인 코드</span><span class="sxs-lookup"><span data-stu-id="53926-307">personal code</span></span>
  
<span data-ttu-id="53926-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="53926-308">maksunumber</span></span>
  
<span data-ttu-id="53926-309">maksu id</span><span class="sxs-lookup"><span data-stu-id="53926-309">maksu id</span></span>
  
<span data-ttu-id="53926-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="53926-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="53926-311">핀란드</span><span class="sxs-lookup"><span data-stu-id="53926-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="53926-312">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-312">Format</span></span>

<span data-ttu-id="53926-313">숫자, 문자, 더하기 및 빼기 기호를 11 문자로 조합</span><span class="sxs-lookup"><span data-stu-id="53926-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-314">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-314">Pattern</span></span>

<span data-ttu-id="53926-315">숫자, 문자, 더하기 및 빼기 기호를 11 문자로 조합한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="53926-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="53926-316">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-316">Six digits</span></span>
    
- <span data-ttu-id="53926-317">더하기 기호, 빼기 기호 또는 + 기호가 1800-1899 사이에 태어난 것을 의미 하는 "A" (대/소문자 구분 안 함), 빼기 기호는 1900-1999 사이에 출생를 의미 하며 "A"는 "A"를 2000 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="53926-318">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-318">Three digits</span></span>
    
- <span data-ttu-id="53926-319">1 개의 문자 또는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-320">제외</span><span class="sxs-lookup"><span data-stu-id="53926-320">Checksum</span></span>

<span data-ttu-id="53926-321">예</span><span class="sxs-lookup"><span data-stu-id="53926-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-322">정의</span><span class="sxs-lookup"><span data-stu-id="53926-322">Definition</span></span>

<span data-ttu-id="53926-323">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-324">이 함수 `Func_finland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-325">From `Keywords_finland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-326">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-327">이 함수 `Func_finland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-328">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="53926-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="53926-330">identification number</span><span class="sxs-lookup"><span data-stu-id="53926-330">identification number</span></span>
  
<span data-ttu-id="53926-331">개인 id</span><span class="sxs-lookup"><span data-stu-id="53926-331">personal id</span></span>
  
<span data-ttu-id="53926-332">id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-332">identity number</span></span>
  
<span data-ttu-id="53926-333">핀란드어 국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-333">finnish national id number</span></span>
  
<span data-ttu-id="53926-334">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-334">personalidnumber#</span></span>
  
<span data-ttu-id="53926-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="53926-335">national identification number</span></span>
  
<span data-ttu-id="53926-336">id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-336">id number</span></span>
  
<span data-ttu-id="53926-337">국가 id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="53926-337">national id no.</span></span>
  
<span data-ttu-id="53926-338">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-338">national id number</span></span>
  
<span data-ttu-id="53926-339">id 없음</span><span class="sxs-lookup"><span data-stu-id="53926-339">id no</span></span>
  
<span data-ttu-id="53926-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="53926-340">tunnistenumero</span></span>
  
<span data-ttu-id="53926-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="53926-341">henkilötunnus</span></span>
  
<span data-ttu-id="53926-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="53926-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="53926-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="53926-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="53926-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="53926-344">identiteetti numero</span></span>
  
<span data-ttu-id="53926-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="53926-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="53926-346">henkilötunnusnumero#</span><span class="sxs-lookup"><span data-stu-id="53926-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="53926-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="53926-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="53926-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="53926-348">tunnusnumero</span></span>
  
<span data-ttu-id="53926-349">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="53926-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="53926-350">프랑스</span><span class="sxs-lookup"><span data-stu-id="53926-350">France</span></span>

### <a name="format"></a><span data-ttu-id="53926-351">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-351">Format</span></span>

<span data-ttu-id="53926-352">개별 사용자의 경우 13 자리 숫자 및 엔터티의 경우 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-353">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-353">Pattern</span></span>

<span data-ttu-id="53926-354">개별 사용자에 대 한 13 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="53926-355">0, 1, 2 또는 3 이어야 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="53926-356">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-356">12 digits</span></span>
    
<span data-ttu-id="53926-357">엔터티의 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-358">제외</span><span class="sxs-lookup"><span data-stu-id="53926-358">Checksum</span></span>

<span data-ttu-id="53926-359">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-360">정의</span><span class="sxs-lookup"><span data-stu-id="53926-360">Definition</span></span>

<span data-ttu-id="53926-361">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-362">이 함수 `Func_france_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-363">From `Keywords_france_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-365">이 함수 `Func_france_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-366">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="53926-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="53926-368">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-368">tax identification number</span></span>
  
<span data-ttu-id="53926-369">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-369">tax number</span></span>
  
<span data-ttu-id="53926-370">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-370">tax id</span></span>
  
<span data-ttu-id="53926-371">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="53926-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="53926-372">독일</span><span class="sxs-lookup"><span data-stu-id="53926-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="53926-373">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-373">Format</span></span>

<span data-ttu-id="53926-374">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-375">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-375">Pattern</span></span>

<span data-ttu-id="53926-376">11 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-376">11 digits :</span></span>
  
-  <span data-ttu-id="53926-377">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-377">Ten digits</span></span> 
    
- <span data-ttu-id="53926-378">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="53926-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-379">제외</span><span class="sxs-lookup"><span data-stu-id="53926-379">Checksum</span></span>

<span data-ttu-id="53926-380">예</span><span class="sxs-lookup"><span data-stu-id="53926-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-381">정의</span><span class="sxs-lookup"><span data-stu-id="53926-381">Definition</span></span>

<span data-ttu-id="53926-382">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-383">이 함수 `Func_germany_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-384">From `Keywords_germany_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-385">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-386">이 함수 `Func_germany_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-387">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="53926-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="53926-389">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-389">tax number</span></span>
  
<span data-ttu-id="53926-390">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-390">tax no.</span></span>
  
<span data-ttu-id="53926-391">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-391">taxno#</span></span>
  
<span data-ttu-id="53926-392">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-392">taxnumber#</span></span>
  
<span data-ttu-id="53926-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="53926-393">taxnumber</span></span>
  
<span data-ttu-id="53926-394">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-394">tax id</span></span>
  
<span data-ttu-id="53926-395">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-395">taxid#</span></span>
  
<span data-ttu-id="53926-396">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-396">tax identification number</span></span>
  
<span data-ttu-id="53926-397">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-397">tax identification no.</span></span>
  
<span data-ttu-id="53926-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="53926-398">steuernummer</span></span>
  
<span data-ttu-id="53926-399">steuer id</span><span class="sxs-lookup"><span data-stu-id="53926-399">steuer id</span></span>
  
<span data-ttu-id="53926-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="53926-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="53926-401">그리스</span><span class="sxs-lookup"><span data-stu-id="53926-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="53926-402">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-402">Format</span></span>

<span data-ttu-id="53926-403">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-404">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-404">Pattern</span></span>

<span data-ttu-id="53926-405">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-406">제외</span><span class="sxs-lookup"><span data-stu-id="53926-406">Checksum</span></span>

<span data-ttu-id="53926-407">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-408">정의</span><span class="sxs-lookup"><span data-stu-id="53926-408">Definition</span></span>

<span data-ttu-id="53926-409">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-410">정규식이 해당 `Regex_greece_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-411">From `Keywords_greece_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53926-412">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="53926-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="53926-414">afm</span><span class="sxs-lookup"><span data-stu-id="53926-414">afm</span></span>
  
<span data-ttu-id="53926-415">언급</span><span class="sxs-lookup"><span data-stu-id="53926-415">tin</span></span>
  
<span data-ttu-id="53926-416">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="53926-416">tax id no.</span></span>
  
<span data-ttu-id="53926-417">세금 번호 없음</span><span class="sxs-lookup"><span data-stu-id="53926-417">tax id no</span></span>
  
<span data-ttu-id="53926-418">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-418">tax identification number</span></span>
  
<span data-ttu-id="53926-419">세금 레지스트리 번호</span><span class="sxs-lookup"><span data-stu-id="53926-419">tax registry number</span></span>
  
<span data-ttu-id="53926-420">세금 레지스트리 번호</span><span class="sxs-lookup"><span data-stu-id="53926-420">tax registry no.</span></span>
  
<span data-ttu-id="53926-421">afm #</span><span class="sxs-lookup"><span data-stu-id="53926-421">afm#</span></span>
  
<span data-ttu-id="53926-422">언급</span><span class="sxs-lookup"><span data-stu-id="53926-422">tin#</span></span>
  
<span data-ttu-id="53926-423">taxidno#</span><span class="sxs-lookup"><span data-stu-id="53926-423">taxidno#</span></span>
  
<span data-ttu-id="53926-424">taxregistryno#</span><span class="sxs-lookup"><span data-stu-id="53926-424">taxregistryno#</span></span>
  
<span data-ttu-id="53926-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="53926-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="53926-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="53926-426">aφμ</span></span>
  
<span data-ttu-id="53926-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="53926-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="53926-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="53926-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="53926-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="53926-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="53926-430">헝가리</span><span class="sxs-lookup"><span data-stu-id="53926-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="53926-431">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-431">Format</span></span>

<span data-ttu-id="53926-432">공백이 나 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-433">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-433">Pattern</span></span>

<span data-ttu-id="53926-434">10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-434">Ten digits:</span></span>
  
-  <span data-ttu-id="53926-435">"8" 이어야 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="53926-436">날짜 01/01/1867과 개별 생년월일 사이의 일 수에 해당 하는 5 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="53926-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="53926-437">같은 날에 태어난 사람을 구별 하기 위해 기회가 만든 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="53926-438">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="53926-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-439">제외</span><span class="sxs-lookup"><span data-stu-id="53926-439">Checksum</span></span>

<span data-ttu-id="53926-440">예</span><span class="sxs-lookup"><span data-stu-id="53926-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-441">정의</span><span class="sxs-lookup"><span data-stu-id="53926-441">Definition</span></span>

<span data-ttu-id="53926-442">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-443">이 함수 `Func_hungary_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-444">From `Keywords_hungary_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-445">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-446">이 함수 `Func_hungary_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-447">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="53926-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="53926-449">헝가리어 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="53926-450">헝가리어 언급</span><span class="sxs-lookup"><span data-stu-id="53926-450">hungarian tin</span></span>
  
<span data-ttu-id="53926-451">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-451">tax id number</span></span>
  
<span data-ttu-id="53926-452">vat 번호</span><span class="sxs-lookup"><span data-stu-id="53926-452">vat number</span></span>
  
<span data-ttu-id="53926-453">세금 기관 아니요</span><span class="sxs-lookup"><span data-stu-id="53926-453">tax authority no</span></span>
  
<span data-ttu-id="53926-454">세금 id 세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-454">tax id tax identity number</span></span>
  
<span data-ttu-id="53926-455">taxidnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-455">taxidnumber#</span></span>
  
<span data-ttu-id="53926-456">언급</span><span class="sxs-lookup"><span data-stu-id="53926-456">tin#</span></span>
  
<span data-ttu-id="53926-457">hungatiantin#</span><span class="sxs-lookup"><span data-stu-id="53926-457">hungatiantin#</span></span>
  
<span data-ttu-id="53926-458">세금 식별 아니요</span><span class="sxs-lookup"><span data-stu-id="53926-458">tax identification no</span></span>
  
<span data-ttu-id="53926-459">taxidno#</span><span class="sxs-lookup"><span data-stu-id="53926-459">taxidno#</span></span>
  
<span data-ttu-id="53926-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="53926-460">adóazonosító szám</span></span>
  
<span data-ttu-id="53926-461">adószám</span><span class="sxs-lookup"><span data-stu-id="53926-461">adószám</span></span>
  
<span data-ttu-id="53926-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="53926-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="53926-463">Ireland</span><span class="sxs-lookup"><span data-stu-id="53926-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="53926-464">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-464">Format</span></span>

<span data-ttu-id="53926-465">공백 또는 구분 기호가 없는 7 자리 숫자와 문자</span><span class="sxs-lookup"><span data-stu-id="53926-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-466">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-466">Pattern</span></span>

<span data-ttu-id="53926-467">7 자리 숫자와 문자</span><span class="sxs-lookup"><span data-stu-id="53926-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="53926-468">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-468">Seven digits</span></span> 
    
- <span data-ttu-id="53926-469">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="53926-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-470">제외</span><span class="sxs-lookup"><span data-stu-id="53926-470">Checksum</span></span>

<span data-ttu-id="53926-471">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-472">정의</span><span class="sxs-lookup"><span data-stu-id="53926-472">Definition</span></span>

<span data-ttu-id="53926-473">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-474">이 함수 `Func_ireland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-475">From `Keywords_ireland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-476">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-477">이 함수 `Func_ireland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-478">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="53926-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="53926-480">공용 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="53926-480">public service no</span></span>
  
<span data-ttu-id="53926-481">개인 공용 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="53926-481">personal public service no</span></span>
  
<span data-ttu-id="53926-482">pps 아니요</span><span class="sxs-lookup"><span data-stu-id="53926-482">pps no</span></span>
  
<span data-ttu-id="53926-483">개인 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="53926-483">personal service no</span></span>
  
<span data-ttu-id="53926-484">pps 서비스 없음</span><span class="sxs-lookup"><span data-stu-id="53926-484">pps service no</span></span>
  
<span data-ttu-id="53926-485">ppsno#</span><span class="sxs-lookup"><span data-stu-id="53926-485">ppsno#</span></span>
  
<span data-ttu-id="53926-486">아일랜드 pps 아니요</span><span class="sxs-lookup"><span data-stu-id="53926-486">irish pps no</span></span>
  
<span data-ttu-id="53926-487">publicserviceno#</span><span class="sxs-lookup"><span data-stu-id="53926-487">publicserviceno#</span></span>
  
<span data-ttu-id="53926-488">개인 공용 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="53926-488">personal public service number</span></span>
  
<span data-ttu-id="53926-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="53926-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="53926-490">pps uimh</span><span class="sxs-lookup"><span data-stu-id="53926-490">pps uimh</span></span>
  
<span data-ttu-id="53926-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="53926-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="53926-492">이탈리아</span><span class="sxs-lookup"><span data-stu-id="53926-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="53926-493">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-493">Format</span></span>

<span data-ttu-id="53926-494">지정 된 패턴의 문자와 숫자 16 개</span><span class="sxs-lookup"><span data-stu-id="53926-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-495">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-495">Pattern</span></span>

<span data-ttu-id="53926-496">16 자의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="53926-497">가족 이름에서 처음 세 개의 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="53926-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="53926-498">이름의 첫 번째, 세 번째 및 네 번째 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="53926-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="53926-499">출생 연도의 마지막 자리에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="53926-500">출생 달에 해당 하는 1 자리 숫자는 알파벳 순으로 사용 되지만 A에서 E, H, L, M, P, R에 해당 하는 문자만 사용 되며, 따라서 1 월은 A와 10 월이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53926-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="53926-501">남성의와 구별 하기 위해 여성의 경우 짝수에서 출생 일에 40이 추가 되는 출생 달의 날짜에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="53926-502">사용자가 태어난 municipality 관련 지역 번호에 해당 하는 4 자리 숫자-국가 전체 코드를 외국 국가에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="53926-503">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="53926-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-504">제외</span><span class="sxs-lookup"><span data-stu-id="53926-504">Checksum</span></span>

<span data-ttu-id="53926-505">예</span><span class="sxs-lookup"><span data-stu-id="53926-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-506">정의</span><span class="sxs-lookup"><span data-stu-id="53926-506">Definition</span></span>

<span data-ttu-id="53926-507">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-508">이 함수 `Func_italy_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-509">From `Keywords_italy_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-510">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-511">이 함수 `Func_italy_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-512">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="53926-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="53926-514">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-514">tax number</span></span>
  
<span data-ttu-id="53926-515">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-515">tax no.</span></span>
  
<span data-ttu-id="53926-516">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-516">taxno#</span></span>
  
<span data-ttu-id="53926-517">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-517">taxnumber#</span></span>
  
<span data-ttu-id="53926-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="53926-518">taxnumber</span></span>
  
<span data-ttu-id="53926-519">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-519">tax id</span></span>
  
<span data-ttu-id="53926-520">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-520">taxid#</span></span>
  
<span data-ttu-id="53926-521">회계 코드</span><span class="sxs-lookup"><span data-stu-id="53926-521">fiscal code</span></span>
  
<span data-ttu-id="53926-522">codice</span><span class="sxs-lookup"><span data-stu-id="53926-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="53926-523">라트비아</span><span class="sxs-lookup"><span data-stu-id="53926-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="53926-524">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-524">Format</span></span>

<span data-ttu-id="53926-525">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-526">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-526">Pattern</span></span>

<span data-ttu-id="53926-527">지정 된 패턴에서 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="53926-528">출생 날짜에 해당 하는 6 자리 숫자 (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="53926-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="53926-529">출생 세기에 해당 하는 1 자리 숫자 이며, "0"은 19th 세기에 해당 하 고 "1"은 20th 세기에 해당 하며 21 세기에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="53926-530">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-531">제외</span><span class="sxs-lookup"><span data-stu-id="53926-531">Checksum</span></span>

<span data-ttu-id="53926-532">예</span><span class="sxs-lookup"><span data-stu-id="53926-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-533">정의</span><span class="sxs-lookup"><span data-stu-id="53926-533">Definition</span></span>

<span data-ttu-id="53926-534">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-535">이 함수 `Func_latvia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-536">From `Keywords_latvia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-537">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-538">이 함수 `Func_latvia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-539">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="53926-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="53926-541">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-541">tax number</span></span>
  
<span data-ttu-id="53926-542">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-542">tax no.</span></span>
  
<span data-ttu-id="53926-543">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-543">taxno#</span></span>
  
<span data-ttu-id="53926-544">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-544">taxnumber#</span></span>
  
<span data-ttu-id="53926-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="53926-545">taxnumber</span></span>
  
<span data-ttu-id="53926-546">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-546">tax id</span></span>
  
<span data-ttu-id="53926-547">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-547">taxid#</span></span>
  
<span data-ttu-id="53926-548">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-548">tax identification number</span></span>
  
<span data-ttu-id="53926-549">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-549">tax identification no.</span></span>
  
<span data-ttu-id="53926-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="53926-550">nodokļa numurs</span></span>
  
<span data-ttu-id="53926-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="53926-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="53926-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="53926-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="53926-553">리투아니아</span><span class="sxs-lookup"><span data-stu-id="53926-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="53926-554">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-554">Format</span></span>

<span data-ttu-id="53926-555">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-556">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-556">Pattern</span></span>

<span data-ttu-id="53926-557">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-558">제외</span><span class="sxs-lookup"><span data-stu-id="53926-558">Checksum</span></span>

<span data-ttu-id="53926-559">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-560">정의</span><span class="sxs-lookup"><span data-stu-id="53926-560">Definition</span></span>

<span data-ttu-id="53926-561">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-562">이 함수 `Func_lithuania_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-563">From `Keywords_lithuania_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-564">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-565">이 함수 `Func_lithuania_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-566">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="53926-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="53926-568">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-568">tax number</span></span>
  
<span data-ttu-id="53926-569">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-569">tax no.</span></span>
  
<span data-ttu-id="53926-570">세금 없음 #</span><span class="sxs-lookup"><span data-stu-id="53926-570">tax no#</span></span>
  
<span data-ttu-id="53926-571">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-571">taxnumber#</span></span>
  
<span data-ttu-id="53926-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="53926-572">taxnumber</span></span>
  
<span data-ttu-id="53926-573">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-573">tax id</span></span>
  
<span data-ttu-id="53926-574">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-574">taxid#</span></span>
  
<span data-ttu-id="53926-575">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-575">tax identification number</span></span>
  
<span data-ttu-id="53926-576">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-576">tax identification no.</span></span>
  
<span data-ttu-id="53926-577">mokesčių id</span><span class="sxs-lookup"><span data-stu-id="53926-577">mokesčių id</span></span>
  
<span data-ttu-id="53926-578">mokesčių numeris</span><span class="sxs-lookup"><span data-stu-id="53926-578">mokesčių numeris</span></span>
  
<span data-ttu-id="53926-579">mokesčių identifikavimas numeris</span><span class="sxs-lookup"><span data-stu-id="53926-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="53926-580">셈</span><span class="sxs-lookup"><span data-stu-id="53926-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="53926-581">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-581">Format</span></span>

<span data-ttu-id="53926-582">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-583">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-583">Pattern</span></span>

<span data-ttu-id="53926-584">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="53926-584">13 digits:</span></span>
  
-  <span data-ttu-id="53926-585">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-585">11 digits</span></span> 
    
- <span data-ttu-id="53926-586">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-587">제외</span><span class="sxs-lookup"><span data-stu-id="53926-587">Checksum</span></span>

<span data-ttu-id="53926-588">예</span><span class="sxs-lookup"><span data-stu-id="53926-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-589">정의</span><span class="sxs-lookup"><span data-stu-id="53926-589">Definition</span></span>

<span data-ttu-id="53926-590">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-591">이 함수 `Func_luxemburg_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-592">From `Keywords_luxemburg_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-593">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-594">이 함수 `Func_luxemburg_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-595">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="53926-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="53926-597">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-597">tax number</span></span>
  
<span data-ttu-id="53926-598">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-598">tax no.</span></span>
  
<span data-ttu-id="53926-599">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-599">taxno#</span></span>
  
<span data-ttu-id="53926-600">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-600">taxnumber#</span></span>
  
<span data-ttu-id="53926-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="53926-601">taxnumber</span></span>
  
<span data-ttu-id="53926-602">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-602">tax id</span></span>
  
<span data-ttu-id="53926-603">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-603">taxid#</span></span>
  
<span data-ttu-id="53926-604">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-604">tax identification number</span></span>
  
<span data-ttu-id="53926-605">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-605">tax identification no.</span></span>
  
<span data-ttu-id="53926-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="53926-606">steuernummer</span></span>
  
<span data-ttu-id="53926-607">steuer id</span><span class="sxs-lookup"><span data-stu-id="53926-607">steuer id</span></span>
  
<span data-ttu-id="53926-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="53926-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="53926-609">몰타</span><span class="sxs-lookup"><span data-stu-id="53926-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="53926-610">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-610">Format</span></span>

<span data-ttu-id="53926-611">몰타어 nationals의 경우 지정 된 패턴의 7 자리 및 한 문자</span><span class="sxs-lookup"><span data-stu-id="53926-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="53926-612">몰타어 이외의 nationals 및 몰타어 엔터티: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-613">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-613">Pattern</span></span>

<span data-ttu-id="53926-614">몰타어 nationals: 7 자리 숫자 및 1 개 문자</span><span class="sxs-lookup"><span data-stu-id="53926-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="53926-615">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-615">Seven digits</span></span> 
    
- <span data-ttu-id="53926-616">1 개 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="53926-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="53926-617">몰타어 이외의 nationals 및 몰타어 엔터티: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="53926-618">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="53926-619">제외</span><span class="sxs-lookup"><span data-stu-id="53926-619">Checksum</span></span>

<span data-ttu-id="53926-620">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-621">정의</span><span class="sxs-lookup"><span data-stu-id="53926-621">Definition</span></span>

<span data-ttu-id="53926-622">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-623">이 함수 `Func_malta_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-624">From `Keywords_malta_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-625">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-626">이 함수 `Func_malta_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-627">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="53926-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="53926-629">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-629">tax number</span></span>
  
<span data-ttu-id="53926-630">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-630">tax no.</span></span>
  
<span data-ttu-id="53926-631">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-631">taxno#</span></span>
  
<span data-ttu-id="53926-632">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-632">taxnumber#</span></span>
  
<span data-ttu-id="53926-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="53926-633">taxnumber</span></span>
  
<span data-ttu-id="53926-634">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-634">tax id</span></span>
  
<span data-ttu-id="53926-635">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-635">taxid#</span></span>
  
<span data-ttu-id="53926-636">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-636">tax identification number</span></span>
  
<span data-ttu-id="53926-637">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-637">tax identification no.</span></span>
  
<span data-ttu-id="53926-638">numru tat</span><span class="sxs-lookup"><span data-stu-id="53926-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="53926-639">id tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="53926-639">id tat-taxxa</span></span>
  
<span data-ttu-id="53926-640">numru ta ' taxxa</span><span class="sxs-lookup"><span data-stu-id="53926-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="53926-641">네덜란드</span><span class="sxs-lookup"><span data-stu-id="53926-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="53926-642">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-642">Format</span></span>

<span data-ttu-id="53926-643">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-644">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-644">Pattern</span></span>

<span data-ttu-id="53926-645">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="53926-646">제외</span><span class="sxs-lookup"><span data-stu-id="53926-646">Checksum</span></span>

<span data-ttu-id="53926-647">예</span><span class="sxs-lookup"><span data-stu-id="53926-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-648">정의</span><span class="sxs-lookup"><span data-stu-id="53926-648">Definition</span></span>

<span data-ttu-id="53926-649">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-650">이 함수 `Func_netherlands_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-651">From `Keywords_netherlands_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-652">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-653">이 함수 `Func_netherlands_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-654">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="53926-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="53926-656">네덜란드 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="53926-657">네덜란드 세금 식별</span><span class="sxs-lookup"><span data-stu-id="53926-657">netherlands tax identification</span></span>
  
<span data-ttu-id="53926-658">netherland의 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="53926-659">netherland의 세금 식별</span><span class="sxs-lookup"><span data-stu-id="53926-659">netherland's tax identification</span></span>
  
<span data-ttu-id="53926-660">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-660">tax identification number</span></span>
  
<span data-ttu-id="53926-661">네덜란드어 세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-661">dutch tax id</span></span>
  
<span data-ttu-id="53926-662">네덜란드어 세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-662">dutch tax identification number</span></span>
  
<span data-ttu-id="53926-663">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-663">tax id</span></span>
  
<span data-ttu-id="53926-664">세금 id #</span><span class="sxs-lookup"><span data-stu-id="53926-664">tax id#</span></span>
  
<span data-ttu-id="53926-665">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-665">tax number</span></span>
  
<span data-ttu-id="53926-666">세금 없음 #</span><span class="sxs-lookup"><span data-stu-id="53926-666">tax no#</span></span>
  
<span data-ttu-id="53926-667">세금</span><span class="sxs-lookup"><span data-stu-id="53926-667">tax#</span></span>
  
<span data-ttu-id="53926-668">언급</span><span class="sxs-lookup"><span data-stu-id="53926-668">tin</span></span>
  
<span data-ttu-id="53926-669">언급</span><span class="sxs-lookup"><span data-stu-id="53926-669">tin#</span></span>
  
<span data-ttu-id="53926-670">네덜란드 언급</span><span class="sxs-lookup"><span data-stu-id="53926-670">netherlands tin</span></span>
  
<span data-ttu-id="53926-671">netherland의 언급</span><span class="sxs-lookup"><span data-stu-id="53926-671">netherland's tin</span></span>
  
<span data-ttu-id="53926-672">nederlands belasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="53926-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="53926-673">identificatienummer van belasting</span><span class="sxs-lookup"><span data-stu-id="53926-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="53926-674">identificatienummer belasting</span><span class="sxs-lookup"><span data-stu-id="53926-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="53926-675">nederlands belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="53926-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="53926-676">nederlands belasting id nummer</span><span class="sxs-lookup"><span data-stu-id="53926-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="53926-677">nederlands belastingnummer</span><span class="sxs-lookup"><span data-stu-id="53926-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="53926-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="53926-678">btw nummer</span></span>
  
<span data-ttu-id="53926-679">nederlandse belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="53926-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="53926-680">폴란드</span><span class="sxs-lookup"><span data-stu-id="53926-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="53926-681">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-681">Format</span></span>

<span data-ttu-id="53926-682">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-683">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-683">Pattern</span></span>

<span data-ttu-id="53926-684">11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-685">제외</span><span class="sxs-lookup"><span data-stu-id="53926-685">Checksum</span></span>

<span data-ttu-id="53926-686">예</span><span class="sxs-lookup"><span data-stu-id="53926-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-687">정의</span><span class="sxs-lookup"><span data-stu-id="53926-687">Definition</span></span>

<span data-ttu-id="53926-688">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-689">이 함수 `Func_poland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-690">From `Keywords_poland_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-691">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-692">이 함수 `Func_poland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-693">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="53926-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="53926-695">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-695">tax number</span></span>
  
<span data-ttu-id="53926-696">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-696">tax no.</span></span>
  
<span data-ttu-id="53926-697">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-697">taxno#</span></span>
  
<span data-ttu-id="53926-698">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-698">taxnumber#</span></span>
  
<span data-ttu-id="53926-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="53926-699">taxnumber</span></span>
  
<span data-ttu-id="53926-700">nip</span><span class="sxs-lookup"><span data-stu-id="53926-700">nip</span></span>
  
<span data-ttu-id="53926-701">nip#</span><span class="sxs-lookup"><span data-stu-id="53926-701">nip#</span></span>
  
<span data-ttu-id="53926-702">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-702">tax id</span></span>
  
<span data-ttu-id="53926-703">세금 id #</span><span class="sxs-lookup"><span data-stu-id="53926-703">tax id#</span></span>
  
<span data-ttu-id="53926-704">nip id</span><span class="sxs-lookup"><span data-stu-id="53926-704">nip id</span></span>
  
<span data-ttu-id="53926-705">nip id #</span><span class="sxs-lookup"><span data-stu-id="53926-705">nip id#</span></span>
  
<span data-ttu-id="53926-706">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-706">tax identification number</span></span>
  
<span data-ttu-id="53926-707">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-707">tax identification no.</span></span>
  
<span data-ttu-id="53926-708">vat 번호</span><span class="sxs-lookup"><span data-stu-id="53926-708">vat number</span></span>
  
<span data-ttu-id="53926-709">vat 번호</span><span class="sxs-lookup"><span data-stu-id="53926-709">vat no.</span></span>
  
<span data-ttu-id="53926-710">vatno#</span><span class="sxs-lookup"><span data-stu-id="53926-710">vatno#</span></span>
  
<span data-ttu-id="53926-711">vat id</span><span class="sxs-lookup"><span data-stu-id="53926-711">vat id</span></span>
  
<span data-ttu-id="53926-712">vat id #</span><span class="sxs-lookup"><span data-stu-id="53926-712">vat id#</span></span>
  
<span data-ttu-id="53926-713">u r i identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="53926-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="53926-714">정책 스키 u r i identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="53926-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="53926-715">numeridentyfikacjipodatkowej#</span><span class="sxs-lookup"><span data-stu-id="53926-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="53926-716">포르투갈</span><span class="sxs-lookup"><span data-stu-id="53926-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="53926-717">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-717">Format</span></span>

<span data-ttu-id="53926-718">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-719">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-719">Pattern</span></span>

<span data-ttu-id="53926-720">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-721">제외</span><span class="sxs-lookup"><span data-stu-id="53926-721">Checksum</span></span>

<span data-ttu-id="53926-722">예</span><span class="sxs-lookup"><span data-stu-id="53926-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-723">정의</span><span class="sxs-lookup"><span data-stu-id="53926-723">Definition</span></span>

<span data-ttu-id="53926-724">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-725">이 함수 `Func_portugal_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-726">From `Keywords_portugal_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-727">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-728">이 함수 `Func_portugal_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-729">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="53926-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="53926-731">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-731">tax number</span></span>
  
<span data-ttu-id="53926-732">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-732">tax no.</span></span>
  
<span data-ttu-id="53926-733">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-733">taxno#</span></span>
  
<span data-ttu-id="53926-734">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="53926-734">taxnumber#</span></span>
  
<span data-ttu-id="53926-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="53926-735">taxnumber</span></span>
  
<span data-ttu-id="53926-736">m</span><span class="sxs-lookup"><span data-stu-id="53926-736">nif</span></span>
  
<span data-ttu-id="53926-737">m</span><span class="sxs-lookup"><span data-stu-id="53926-737">nif#</span></span>
  
<span data-ttu-id="53926-738">numero 회계</span><span class="sxs-lookup"><span data-stu-id="53926-738">numero fiscal</span></span>
  
<span data-ttu-id="53926-739">número de identificação 회계</span><span class="sxs-lookup"><span data-stu-id="53926-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="53926-740">루마니아</span><span class="sxs-lookup"><span data-stu-id="53926-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="53926-741">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-741">Format</span></span>

<span data-ttu-id="53926-742">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-743">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-743">Pattern</span></span>

<span data-ttu-id="53926-744">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-745">제외</span><span class="sxs-lookup"><span data-stu-id="53926-745">Checksum</span></span>

<span data-ttu-id="53926-746">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-747">정의</span><span class="sxs-lookup"><span data-stu-id="53926-747">Definition</span></span>

<span data-ttu-id="53926-748">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-749">정규식이 해당 `Regex_romania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-750">From `Keywords_romania_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53926-751">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="53926-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="53926-753">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-753">tax id</span></span>
  
<span data-ttu-id="53926-754">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-754">tax id number</span></span>
  
<span data-ttu-id="53926-755">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="53926-755">tax file no</span></span>
  
<span data-ttu-id="53926-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="53926-756">tax file number</span></span>
  
<span data-ttu-id="53926-757">세금 없음</span><span class="sxs-lookup"><span data-stu-id="53926-757">tax no</span></span>
  
<span data-ttu-id="53926-758">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-758">tax number</span></span>
  
<span data-ttu-id="53926-759">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-759">taxid#</span></span>
  
<span data-ttu-id="53926-760">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-760">taxno#</span></span>
  
<span data-ttu-id="53926-761">id-ul taxei</span><span class="sxs-lookup"><span data-stu-id="53926-761">id-ul taxei</span></span>
  
<span data-ttu-id="53926-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="53926-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="53926-763">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="53926-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="53926-764">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-764">Format</span></span>

<span data-ttu-id="53926-765">공백이 나 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-766">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-766">Pattern</span></span>

<span data-ttu-id="53926-767">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-768">제외</span><span class="sxs-lookup"><span data-stu-id="53926-768">Checksum</span></span>

<span data-ttu-id="53926-769">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="53926-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-770">정의</span><span class="sxs-lookup"><span data-stu-id="53926-770">Definition</span></span>

<span data-ttu-id="53926-771">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-772">정규식이 해당 `Regex_slovakia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-773">From `Keywords_slovakia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53926-774">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="53926-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="53926-776">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-776">tax id</span></span>
  
<span data-ttu-id="53926-777">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-777">tax id number</span></span>
  
<span data-ttu-id="53926-778">언급 id</span><span class="sxs-lookup"><span data-stu-id="53926-778">tin id</span></span>
  
<span data-ttu-id="53926-779">언급 아니요</span><span class="sxs-lookup"><span data-stu-id="53926-779">tin no</span></span>
  
<span data-ttu-id="53926-780">슬로바키아어 언급 id</span><span class="sxs-lookup"><span data-stu-id="53926-780">slovakian tin id</span></span>
  
<span data-ttu-id="53926-781">언급</span><span class="sxs-lookup"><span data-stu-id="53926-781">tin</span></span>
  
<span data-ttu-id="53926-782">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="53926-782">tax file no</span></span>
  
<span data-ttu-id="53926-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="53926-783">tax file number</span></span>
  
<span data-ttu-id="53926-784">세금 없음</span><span class="sxs-lookup"><span data-stu-id="53926-784">tax no</span></span>
  
<span data-ttu-id="53926-785">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-785">tax number</span></span>
  
<span data-ttu-id="53926-786">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-786">taxid#</span></span>
  
<span data-ttu-id="53926-787">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-787">taxno#</span></span>
  
<span data-ttu-id="53926-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="53926-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="53926-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="53926-789">daňové číslo</span></span>
  
<span data-ttu-id="53926-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="53926-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="53926-791">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="53926-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="53926-792">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-792">Format</span></span>

<span data-ttu-id="53926-793">공백이 나 구분 기호가 없는 8 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-794">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-794">Pattern</span></span>

<span data-ttu-id="53926-795">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-796">제외</span><span class="sxs-lookup"><span data-stu-id="53926-796">Checksum</span></span>

<span data-ttu-id="53926-797">예</span><span class="sxs-lookup"><span data-stu-id="53926-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-798">정의</span><span class="sxs-lookup"><span data-stu-id="53926-798">Definition</span></span>

<span data-ttu-id="53926-799">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-800">이 함수 `Func_slovenia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-801">From `Keywords_slovenia_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-802">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-803">이 함수 `Func_slovenia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-804">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="53926-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="53926-806">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-806">tax id</span></span>
  
<span data-ttu-id="53926-807">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-807">tax id number</span></span>
  
<span data-ttu-id="53926-808">언급 id</span><span class="sxs-lookup"><span data-stu-id="53926-808">tin id</span></span>
  
<span data-ttu-id="53926-809">언급 아니요</span><span class="sxs-lookup"><span data-stu-id="53926-809">tin no</span></span>
  
<span data-ttu-id="53926-810">슬로베니아어 언급 id</span><span class="sxs-lookup"><span data-stu-id="53926-810">slovenian tin id</span></span>
  
<span data-ttu-id="53926-811">언급</span><span class="sxs-lookup"><span data-stu-id="53926-811">tin</span></span>
  
<span data-ttu-id="53926-812">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="53926-812">tax file no</span></span>
  
<span data-ttu-id="53926-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="53926-813">tax file number</span></span>
  
<span data-ttu-id="53926-814">세금 없음</span><span class="sxs-lookup"><span data-stu-id="53926-814">tax no</span></span>
  
<span data-ttu-id="53926-815">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-815">tax number</span></span>
  
<span data-ttu-id="53926-816">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-816">taxid#</span></span>
  
<span data-ttu-id="53926-817">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-817">taxno#</span></span>
  
<span data-ttu-id="53926-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="53926-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="53926-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="53926-819">davčna številka</span></span>
  
<span data-ttu-id="53926-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="53926-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="53926-821">스페인</span><span class="sxs-lookup"><span data-stu-id="53926-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="53926-822">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-822">Format</span></span>

<span data-ttu-id="53926-823">지정 된 패턴에 7 ~ 8 자리 숫자와 한 가지 또는 두 개의 문자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-824">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-824">Pattern</span></span>

<span data-ttu-id="53926-825">스페인 국내 Id 카드가 있는 스페인어 (자연 사용자):</span><span class="sxs-lookup"><span data-stu-id="53926-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="53926-826">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-826">Eight digits</span></span> 
    
- <span data-ttu-id="53926-827">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="53926-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="53926-828">스페인 국가 Id 카드가 없는 상주 하지 않는 Spaniards</span><span class="sxs-lookup"><span data-stu-id="53926-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="53926-829">1 개의 대문자 "L" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="53926-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="53926-830">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-830">Seven digits</span></span>
    
- <span data-ttu-id="53926-831">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="53926-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="53926-832">스페인 국가 Id 카드를 사용 하지 않고 14 년 동안 상주 하는 Spaniards:</span><span class="sxs-lookup"><span data-stu-id="53926-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="53926-833">1 개의 대문자 "K" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="53926-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="53926-834">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-834">Seven digits</span></span> 
    
- <span data-ttu-id="53926-835">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="53926-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="53926-836">Foreigner의 식별 번호를 사용 하는 Foreigners</span><span class="sxs-lookup"><span data-stu-id="53926-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="53926-837">"X", "Y" 또는 "Z" (대/소문자 구분)의 대문자 1 개</span><span class="sxs-lookup"><span data-stu-id="53926-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="53926-838">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-838">Seven digits</span></span>
    
- <span data-ttu-id="53926-839">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="53926-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="53926-840">Foreigner의 Id 번호가 없는 Foreigners</span><span class="sxs-lookup"><span data-stu-id="53926-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="53926-841">"M"을 나타내는 대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="53926-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="53926-842">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-842">Seven digits</span></span>
    
- <span data-ttu-id="53926-843">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="53926-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="53926-844">제외</span><span class="sxs-lookup"><span data-stu-id="53926-844">Checksum</span></span>

<span data-ttu-id="53926-845">예</span><span class="sxs-lookup"><span data-stu-id="53926-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-846">정의</span><span class="sxs-lookup"><span data-stu-id="53926-846">Definition</span></span>

<span data-ttu-id="53926-847">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-848">이 함수 `Func_spain_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-849">From `Keywords_spain_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-850">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-851">이 함수 `Func_spain_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-852">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="53926-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="53926-854">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-854">tax id</span></span>
  
<span data-ttu-id="53926-855">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-855">tax id number</span></span>
  
<span data-ttu-id="53926-856">cif id</span><span class="sxs-lookup"><span data-stu-id="53926-856">cif id</span></span>
  
<span data-ttu-id="53926-857">cif 아니요</span><span class="sxs-lookup"><span data-stu-id="53926-857">cif no</span></span>
  
<span data-ttu-id="53926-858">스페인어 cif id</span><span class="sxs-lookup"><span data-stu-id="53926-858">spanish cif id</span></span>
  
<span data-ttu-id="53926-859">cif</span><span class="sxs-lookup"><span data-stu-id="53926-859">cif</span></span>
  
<span data-ttu-id="53926-860">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="53926-860">tax file no</span></span>
  
<span data-ttu-id="53926-861">스페인어 cif 번호</span><span class="sxs-lookup"><span data-stu-id="53926-861">spanish cif number</span></span>
  
<span data-ttu-id="53926-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="53926-862">tax file number</span></span>
  
<span data-ttu-id="53926-863">스페인어 cif 아니요</span><span class="sxs-lookup"><span data-stu-id="53926-863">spanish cif no</span></span>
  
<span data-ttu-id="53926-864">세금 없음</span><span class="sxs-lookup"><span data-stu-id="53926-864">tax no</span></span>
  
<span data-ttu-id="53926-865">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-865">tax number</span></span>
  
<span data-ttu-id="53926-866">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-866">taxid#</span></span>
  
<span data-ttu-id="53926-867">taxno#</span><span class="sxs-lookup"><span data-stu-id="53926-867">taxno#</span></span>
  
<span data-ttu-id="53926-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="53926-868">cifid#</span></span>
  
<span data-ttu-id="53926-869">spanishcifid#</span><span class="sxs-lookup"><span data-stu-id="53926-869">spanishcifid#</span></span>
  
<span data-ttu-id="53926-870">spanishcifno#</span><span class="sxs-lookup"><span data-stu-id="53926-870">spanishcifno#</span></span>
  
<span data-ttu-id="53926-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="53926-871">número de contribuyente</span></span>
  
<span data-ttu-id="53926-872">número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="53926-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="53926-873">número de identificación 회계</span><span class="sxs-lookup"><span data-stu-id="53926-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="53926-874">cif número</span><span class="sxs-lookup"><span data-stu-id="53926-874">cif número</span></span>
  
<span data-ttu-id="53926-875">cifnúmero#</span><span class="sxs-lookup"><span data-stu-id="53926-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="53926-876">스웨덴</span><span class="sxs-lookup"><span data-stu-id="53926-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="53926-877">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-877">Format</span></span>

<span data-ttu-id="53926-878">지정 된 패턴의 10 자리 숫자와 기호</span><span class="sxs-lookup"><span data-stu-id="53926-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-879">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-879">Pattern</span></span>

<span data-ttu-id="53926-880">10 자리 숫자와 기호:</span><span class="sxs-lookup"><span data-stu-id="53926-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="53926-881">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="53926-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="53926-882">더하기 기호, 빼기 기호 또는 백슬래시</span><span class="sxs-lookup"><span data-stu-id="53926-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="53926-883">다음은 식별 번호를 고유 하 게 만드는 3 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="53926-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="53926-884">1990 이전에 실행 된 번호의 경우 일곱째 및 여덟 번째 숫자는 출생 또는 외부에서 태어난 사람의 국가를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="53926-885">아홉 번째 위치의 숫자는 성별에 대 한 홀수 또는 암도를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="53926-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="53926-886">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="53926-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53926-887">제외</span><span class="sxs-lookup"><span data-stu-id="53926-887">Checksum</span></span>

<span data-ttu-id="53926-888">예</span><span class="sxs-lookup"><span data-stu-id="53926-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-889">정의</span><span class="sxs-lookup"><span data-stu-id="53926-889">Definition</span></span>

<span data-ttu-id="53926-890">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-891">이 함수 `Func_sweden_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-892">From `Keywords_sweden_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="53926-893">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-894">이 함수 `Func_sweden_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="53926-895">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="53926-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="53926-897">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-897">tax id</span></span>
  
<span data-ttu-id="53926-898">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="53926-898">tax id no.</span></span>
  
<span data-ttu-id="53926-899">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-899">tax id number</span></span>
  
<span data-ttu-id="53926-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="53926-900">tax identification</span></span>
  
<span data-ttu-id="53926-901">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-901">tax identification#</span></span>
  
<span data-ttu-id="53926-902">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-902">tax no.</span></span>
  
<span data-ttu-id="53926-903">세금</span><span class="sxs-lookup"><span data-stu-id="53926-903">tax#</span></span>
  
<span data-ttu-id="53926-904">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-904">taxid#</span></span>
  
<span data-ttu-id="53926-905">세금 파일</span><span class="sxs-lookup"><span data-stu-id="53926-905">tax file</span></span>
  
<span data-ttu-id="53926-906">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="53926-906">tax file no.</span></span>
  
<span data-ttu-id="53926-907">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-907">personal id number</span></span>
  
<span data-ttu-id="53926-908">(nummer at&t id)</span><span class="sxs-lookup"><span data-stu-id="53926-908">skatt id nummer</span></span>
  
<span data-ttu-id="53926-909">identifikation at&t</span><span class="sxs-lookup"><span data-stu-id="53926-909">skatt identifikation</span></span>
  
<span data-ttu-id="53926-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="53926-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="53926-911">영국의</span><span class="sxs-lookup"><span data-stu-id="53926-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="53926-912">형식일</span><span class="sxs-lookup"><span data-stu-id="53926-912">Format</span></span>

<span data-ttu-id="53926-913">UTR (Unique Taxpayer Reference): 공백 및 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="53926-914">국가 보험 번호 (NINO): 자세한 내용은 영국 섹션 "을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53926-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="53926-915">[중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)국가 보험 번호 (NINO) "입니다.</span><span class="sxs-lookup"><span data-stu-id="53926-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53926-916">패턴</span><span class="sxs-lookup"><span data-stu-id="53926-916">Pattern</span></span>

<span data-ttu-id="53926-917">UTR (Unique Taxpayer Reference): 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="53926-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="53926-918">국가 보험 번호 (NINO): 자세한 내용은 영국 섹션 "을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53926-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="53926-919">[중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)국가 보험 번호 (NINO) "입니다.</span><span class="sxs-lookup"><span data-stu-id="53926-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53926-920">제외</span><span class="sxs-lookup"><span data-stu-id="53926-920">Checksum</span></span>

<span data-ttu-id="53926-921">예</span><span class="sxs-lookup"><span data-stu-id="53926-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="53926-922">정의</span><span class="sxs-lookup"><span data-stu-id="53926-922">Definition</span></span>

<span data-ttu-id="53926-923">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="53926-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53926-924">이 함수 `Func_uk_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53926-925">From `Keywords_uk_eu_tax_file_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="53926-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53926-926">키워드</span><span class="sxs-lookup"><span data-stu-id="53926-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="53926-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="53926-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="53926-928">tax id</span><span class="sxs-lookup"><span data-stu-id="53926-928">tax id</span></span>
  
<span data-ttu-id="53926-929">세금 번호 번호</span><span class="sxs-lookup"><span data-stu-id="53926-929">tax id no.</span></span>
  
<span data-ttu-id="53926-930">세금 id 번호</span><span class="sxs-lookup"><span data-stu-id="53926-930">tax id number</span></span>
  
<span data-ttu-id="53926-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="53926-931">tax identification</span></span>
  
<span data-ttu-id="53926-932">세금 식별 번호</span><span class="sxs-lookup"><span data-stu-id="53926-932">tax identification#</span></span>
  
<span data-ttu-id="53926-933">세금 번호</span><span class="sxs-lookup"><span data-stu-id="53926-933">tax no.</span></span>
  
<span data-ttu-id="53926-934">세금</span><span class="sxs-lookup"><span data-stu-id="53926-934">tax#</span></span>
  
<span data-ttu-id="53926-935">taxid#</span><span class="sxs-lookup"><span data-stu-id="53926-935">taxid#</span></span>
  
<span data-ttu-id="53926-936">세금 파일</span><span class="sxs-lookup"><span data-stu-id="53926-936">tax file</span></span>
  
<span data-ttu-id="53926-937">세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="53926-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53926-938">참고 항목</span><span class="sxs-lookup"><span data-stu-id="53926-938">See also</span></span>

[<span data-ttu-id="53926-939">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="53926-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

