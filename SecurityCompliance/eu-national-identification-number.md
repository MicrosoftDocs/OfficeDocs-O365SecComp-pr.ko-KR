---
title: EU 국가 식별 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 국가 식별 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: 205019d040648f0600f3dbf4403063edf9f31c41
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154463"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="f6541-104">EU 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-104">EU National Identification Number</span></span>

<span data-ttu-id="f6541-105">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 국가 식별 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="f6541-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="f6541-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="f6541-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="f6541-108">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-108">Format</span></span>

<span data-ttu-id="f6541-109">문자, 숫자 및 특수 문자의 24 자 조합</span><span class="sxs-lookup"><span data-stu-id="f6541-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-110">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-110">Pattern</span></span>

<span data-ttu-id="f6541-111">24 문자:</span><span class="sxs-lookup"><span data-stu-id="f6541-111">24 characters:</span></span>
  
-  <span data-ttu-id="f6541-112">22 개 문자 (대/소문자 구분 안 함), 숫자, 백슬래시, 슬래시 또는 더하기 기호</span><span class="sxs-lookup"><span data-stu-id="f6541-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="f6541-113">2 개의 문자 (대/소문자 구분 안 함), 숫자, 백슬래시, 슬래시, 더하기 기호 또는 등호</span><span class="sxs-lookup"><span data-stu-id="f6541-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-114">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-114">Checksum</span></span>

<span data-ttu-id="f6541-115">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="f6541-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-116">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-116">Definition</span></span>

<span data-ttu-id="f6541-117">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-118">정규식이 해당 `Regex_austria_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-119">From `Keywords_austria_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-120">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="f6541-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="f6541-122">오스트리아 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-122">austrian identity number</span></span>
  
<span data-ttu-id="f6541-123">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-123">national identity number</span></span>
  
<span data-ttu-id="f6541-124">id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-124">identity number</span></span>
  
<span data-ttu-id="f6541-125">national id</span><span class="sxs-lookup"><span data-stu-id="f6541-125">national id</span></span>
  
<span data-ttu-id="f6541-126">personalausweis republik österreich</span><span class="sxs-lookup"><span data-stu-id="f6541-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="f6541-127">벨기에</span><span class="sxs-lookup"><span data-stu-id="f6541-127">Belgium</span></span>

<span data-ttu-id="f6541-128">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"벨기에 국가 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="f6541-129">불가리아</span><span class="sxs-lookup"><span data-stu-id="f6541-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="f6541-130">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-130">Format</span></span>

<span data-ttu-id="f6541-131">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-132">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-132">Pattern</span></span>

<span data-ttu-id="f6541-133">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="f6541-134">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="f6541-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="f6541-135">출생 순서에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="f6541-136">성별에 해당 하는 1 자리 숫자와이에 해당 하는 짝수 자리 숫자 및 암의 홀수 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="f6541-137">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-138">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-138">Checksum</span></span>

<span data-ttu-id="f6541-139">예</span><span class="sxs-lookup"><span data-stu-id="f6541-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-140">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-140">Definition</span></span>

<span data-ttu-id="f6541-141">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-142">이 함수 `Func_bulgaria_national_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-143">From `Keywords_bulgaria_national_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="f6541-144">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-145">이 함수 `Func_bulgaria_national_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-146">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="f6541-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="f6541-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="f6541-148">egn</span><span class="sxs-lookup"><span data-stu-id="f6541-148">egn</span></span>
  
<span data-ttu-id="f6541-149">egn#</span><span class="sxs-lookup"><span data-stu-id="f6541-149">egn#</span></span>
  
<span data-ttu-id="f6541-150">불가리아어 국가 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-150">bulgarian national number</span></span>
  
<span data-ttu-id="f6541-151">국가 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-151">national number</span></span>
  
<span data-ttu-id="f6541-152">social security number</span><span class="sxs-lookup"><span data-stu-id="f6541-152">social security number</span></span>
  
<span data-ttu-id="f6541-153">nationalnumber#</span><span class="sxs-lookup"><span data-stu-id="f6541-153">nationalnumber#</span></span>
  
<span data-ttu-id="f6541-154">ssn</span><span class="sxs-lookup"><span data-stu-id="f6541-154">ssn#</span></span>
  
<span data-ttu-id="f6541-155">ssn</span><span class="sxs-lookup"><span data-stu-id="f6541-155">ssn</span></span>
  
<span data-ttu-id="f6541-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="f6541-156">nationalnumber</span></span>
  
<span data-ttu-id="f6541-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="f6541-157">bnn#</span></span>
  
<span data-ttu-id="f6541-158">bnn</span><span class="sxs-lookup"><span data-stu-id="f6541-158">bnn</span></span>
  
<span data-ttu-id="f6541-159">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-159">personal id number</span></span>
  
<span data-ttu-id="f6541-160">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="f6541-160">personalidnumber#</span></span>
  
<span data-ttu-id="f6541-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="f6541-161">единен граждански номер</span></span>
  
<span data-ttu-id="f6541-162">edinen grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="f6541-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="f6541-163">егн</span><span class="sxs-lookup"><span data-stu-id="f6541-163">егн</span></span>
  
<span data-ttu-id="f6541-164">егн#</span><span class="sxs-lookup"><span data-stu-id="f6541-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="f6541-165">크로아티아</span><span class="sxs-lookup"><span data-stu-id="f6541-165">Croatia</span></span>

<span data-ttu-id="f6541-166">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"크로아티아 id 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="f6541-167">키프로스</span><span class="sxs-lookup"><span data-stu-id="f6541-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="f6541-168">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-168">Format</span></span>

<span data-ttu-id="f6541-169">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-170">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-170">Pattern</span></span>

 <span data-ttu-id="f6541-171">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="f6541-172">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-172">Checksum</span></span>

<span data-ttu-id="f6541-173">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="f6541-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-174">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-174">Definition</span></span>

<span data-ttu-id="f6541-175">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-176">정규식이 해당 `Regex_cyprus_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-177">From `Keywords_cyprus_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-178">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="f6541-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="f6541-180">id 카드 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-180">id card number</span></span>
  
<span data-ttu-id="f6541-181">national identification number</span><span class="sxs-lookup"><span data-stu-id="f6541-181">national identification number</span></span>
  
<span data-ttu-id="f6541-182">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-182">personal id number</span></span>
  
<span data-ttu-id="f6541-183">id 카드 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-183">identity card number</span></span>
  
<span data-ttu-id="f6541-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="f6541-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="f6541-185">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="f6541-185">Czech Republic</span></span>

<span data-ttu-id="f6541-186">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"체코어 국내 id 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="f6541-187">덴마크</span><span class="sxs-lookup"><span data-stu-id="f6541-187">Denmark</span></span>

<span data-ttu-id="f6541-188">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"덴마크 개인 식별 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="f6541-189">에스토니아</span><span class="sxs-lookup"><span data-stu-id="f6541-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="f6541-190">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-190">Format</span></span>

<span data-ttu-id="f6541-191">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-192">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-192">Pattern</span></span>

<span data-ttu-id="f6541-193">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="f6541-193">11 digits:</span></span>
  
- <span data-ttu-id="f6541-194">출생의 성별 및 세기에 해당 하는 1 자리 숫자 (예: 1-2 암, 수, 19th 세기, 3-4:20th 세기, 5-6 = 21 세기)</span><span class="sxs-lookup"><span data-stu-id="f6541-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="f6541-195">출생 날짜에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="f6541-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="f6541-196">같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="f6541-197">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-198">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-198">Checksum</span></span>

<span data-ttu-id="f6541-199">예</span><span class="sxs-lookup"><span data-stu-id="f6541-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-200">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-200">Definition</span></span>

<span data-ttu-id="f6541-201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-202">이 함수 `Func_estonia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-203">From `Keywords_estonia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-204">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-205">이 함수 `Func_estonia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-206">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="f6541-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="f6541-208">개인 식별 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-208">personal identification code</span></span>
  
<span data-ttu-id="f6541-209">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-209">personal identification number</span></span>
  
<span data-ttu-id="f6541-210">national identification number</span><span class="sxs-lookup"><span data-stu-id="f6541-210">national identification number</span></span>
  
<span data-ttu-id="f6541-211">국가 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-211">national number</span></span>
  
<span data-ttu-id="f6541-212">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-212">personal id number</span></span>
  
<span data-ttu-id="f6541-213">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="f6541-213">personalidnumber#</span></span>
  
<span data-ttu-id="f6541-214">ik</span><span class="sxs-lookup"><span data-stu-id="f6541-214">ik</span></span>
  
<span data-ttu-id="f6541-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="f6541-215">isikukood</span></span>
  
<span data-ttu-id="f6541-216">id-kaart</span><span class="sxs-lookup"><span data-stu-id="f6541-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="f6541-217">핀란드</span><span class="sxs-lookup"><span data-stu-id="f6541-217">Finland</span></span>

<span data-ttu-id="f6541-218">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"핀란드 국가 ID" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="f6541-219">프랑스</span><span class="sxs-lookup"><span data-stu-id="f6541-219">France</span></span>

<span data-ttu-id="f6541-220">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 국가 ID 카드 (cni)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="f6541-221">독일</span><span class="sxs-lookup"><span data-stu-id="f6541-221">Germany</span></span>

<span data-ttu-id="f6541-222">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 Id 카드 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="f6541-223">그리스</span><span class="sxs-lookup"><span data-stu-id="f6541-223">Greece</span></span>

<span data-ttu-id="f6541-224">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"그리스 국가 ID 카드" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="f6541-225">헝가리</span><span class="sxs-lookup"><span data-stu-id="f6541-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="f6541-226">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-226">Format</span></span>

<span data-ttu-id="f6541-227">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-228">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-228">Pattern</span></span>

<span data-ttu-id="f6541-229">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="f6541-229">11 digits:</span></span>
  
-  <span data-ttu-id="f6541-230">성별에 해당 하는 1 자리 숫자 (1gb, 2 암, 기타 번호는 두 개를 포함 하는 경우 1900에만 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="f6541-231">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="f6541-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="f6541-232">일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="f6541-233">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-234">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-234">Checksum</span></span>

<span data-ttu-id="f6541-235">예</span><span class="sxs-lookup"><span data-stu-id="f6541-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-236">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-236">Definition</span></span>

<span data-ttu-id="f6541-237">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-238">이 함수 `Func_hungary_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-239">From `Keywords_hungary_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-240">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-241">이 함수 `Func_hungary_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-242">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="f6541-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="f6541-244">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-244">personal identification number</span></span>
  
<span data-ttu-id="f6541-245">identification number</span><span class="sxs-lookup"><span data-stu-id="f6541-245">identification number</span></span>
  
<span data-ttu-id="f6541-246">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-246">personal id number</span></span>
  
<span data-ttu-id="f6541-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="f6541-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="f6541-248">Ireland</span><span class="sxs-lookup"><span data-stu-id="f6541-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="f6541-249">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-249">Format</span></span>

<span data-ttu-id="f6541-250">지정 된 패턴에서 문자, 숫자 및 공백의 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="f6541-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-251">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-251">Pattern</span></span>

<span data-ttu-id="f6541-252">지정 된 패턴에서 문자, 숫자 및 공백의 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="f6541-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="f6541-253">01 년 1 월 2013 일 현재 위치:</span><span class="sxs-lookup"><span data-stu-id="f6541-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="f6541-254">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-254">Seven digits</span></span> 
    
- <span data-ttu-id="f6541-255">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-255">One check digit</span></span>
    
- <span data-ttu-id="f6541-256">1 개의 공백 또는 대문자 "W" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="f6541-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="f6541-257">01 년 1 월 2013 일 이전:</span><span class="sxs-lookup"><span data-stu-id="f6541-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="f6541-258">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-258">Seven digits</span></span> 
    
- <span data-ttu-id="f6541-259">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-259">One check digit</span></span>
    
- <span data-ttu-id="f6541-260">1 개의 공백 또는 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="f6541-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-261">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-261">Checksum</span></span>

<span data-ttu-id="f6541-262">예</span><span class="sxs-lookup"><span data-stu-id="f6541-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-263">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-263">Definition</span></span>

<span data-ttu-id="f6541-264">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-265">이 함수는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="f6541-266">From 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-266">A keyword from is found.</span></span>
    
<span data-ttu-id="f6541-267">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-268">이 함수는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-268">The function finds content that matches the pattern.</span></span>
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-269">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="f6541-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="f6541-271">개인 공용 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-271">personal public service number</span></span>
  
<span data-ttu-id="f6541-272">pps 아니요</span><span class="sxs-lookup"><span data-stu-id="f6541-272">pps no</span></span>
  
<span data-ttu-id="f6541-273">수입 및 주민 등록 보험 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="f6541-274">rsi 아니요</span><span class="sxs-lookup"><span data-stu-id="f6541-274">rsi no</span></span>
  
<span data-ttu-id="f6541-275">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-275">personal identification number</span></span>
  
<span data-ttu-id="f6541-276">identification number</span><span class="sxs-lookup"><span data-stu-id="f6541-276">identification number</span></span>
  
<span data-ttu-id="f6541-277">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-277">personal id number</span></span>
  
<span data-ttu-id="f6541-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="f6541-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="f6541-279">uimh</span><span class="sxs-lookup"><span data-stu-id="f6541-279">uimh.</span></span> <span data-ttu-id="f6541-280">psp</span><span class="sxs-lookup"><span data-stu-id="f6541-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="f6541-281">이탈리아</span><span class="sxs-lookup"><span data-stu-id="f6541-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="f6541-282">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-282">Format</span></span>

<span data-ttu-id="f6541-283">지정 된 패턴에 해당 하는 문자 및 숫자의 16 자 조합</span><span class="sxs-lookup"><span data-stu-id="f6541-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-284">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-284">Pattern</span></span>

<span data-ttu-id="f6541-285">문자와 숫자의 16 자 조합:</span><span class="sxs-lookup"><span data-stu-id="f6541-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="f6541-286">가족 이름에서 처음 세 개의 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="f6541-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="f6541-287">이름의 첫 번째, 세 번째 및 네 번째 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="f6541-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="f6541-288">출생 연도의 마지막 자리에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="f6541-289">출생 월의 문자에 해당 하는 한 문자는 알파벳 순서로 사용 되지만 1 ~ E, H, L, M, P, R에 해당 하는 문자를 사용 하는 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="f6541-290">Genders를 구분 하기 위해 출생 달의 날짜에 해당 하는 2 자리 숫자 (40)가 여성 생년월일에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="f6541-291">사용자가 태어난 municipality 관련 지역 번호에 해당 하는 4 자리 숫자 (국가 전체 코드는 외국 국가에 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="f6541-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="f6541-292">1 개의 패리티 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-293">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-293">Checksum</span></span>

<span data-ttu-id="f6541-294">예</span><span class="sxs-lookup"><span data-stu-id="f6541-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-295">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-295">Definition</span></span>

<span data-ttu-id="f6541-296">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-297">이 함수 `Func_italy_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-298">From `Keywords_italy_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-299">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-300">이 함수 `Func_italy_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-301">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="f6541-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="f6541-303">개인 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-303">personal code</span></span>
  
<span data-ttu-id="f6541-304">개인 코드 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-304">personal code number</span></span>
  
<span data-ttu-id="f6541-305">개인 인증서 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-305">personal certificate number</span></span>
  
<span data-ttu-id="f6541-306">회계 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-306">fiscal code</span></span>
  
<span data-ttu-id="f6541-307">personalcodeno#</span><span class="sxs-lookup"><span data-stu-id="f6541-307">personalcodeno#</span></span>
  
<span data-ttu-id="f6541-308">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-308">personal id number</span></span>
  
<span data-ttu-id="f6541-309">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-309">personal id code</span></span>
  
<span data-ttu-id="f6541-310">codice personale</span><span class="sxs-lookup"><span data-stu-id="f6541-310">codice personale</span></span>
  
<span data-ttu-id="f6541-311">numero certificato personale</span><span class="sxs-lookup"><span data-stu-id="f6541-311">numero certificato personale</span></span>
  
<span data-ttu-id="f6541-312">numero personale</span><span class="sxs-lookup"><span data-stu-id="f6541-312">numero personale</span></span>
  
<span data-ttu-id="f6541-313">numero id personale</span><span class="sxs-lookup"><span data-stu-id="f6541-313">numero id personale</span></span>
  
<span data-ttu-id="f6541-314">codice id personale</span><span class="sxs-lookup"><span data-stu-id="f6541-314">codice id personale</span></span>
  
<span data-ttu-id="f6541-315">codice</span><span class="sxs-lookup"><span data-stu-id="f6541-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="f6541-316">이탈리아</span><span class="sxs-lookup"><span data-stu-id="f6541-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="f6541-317">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-317">Format</span></span>

<span data-ttu-id="f6541-318">지정 된 형식의 11 자리 숫자 및 하이픈</span><span class="sxs-lookup"><span data-stu-id="f6541-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-319">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-319">Pattern</span></span>

<span data-ttu-id="f6541-320">11 자리 숫자와 하이픈:</span><span class="sxs-lookup"><span data-stu-id="f6541-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="f6541-321">생년월일에 해당 하는 6 자리 숫자 (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="f6541-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="f6541-322">하이픈</span><span class="sxs-lookup"><span data-stu-id="f6541-322">A hyphen</span></span>
    
- <span data-ttu-id="f6541-323">출생 세기에 해당 하는 1 자리 숫자 (19th 세기의 경우 "1", 21 세기의 경우 "2")</span><span class="sxs-lookup"><span data-stu-id="f6541-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="f6541-324">임의로 생성 되는 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-325">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-325">Checksum</span></span>

<span data-ttu-id="f6541-326">예</span><span class="sxs-lookup"><span data-stu-id="f6541-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-327">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-327">Definition</span></span>

<span data-ttu-id="f6541-328">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-329">이 함수 `Func_latvia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-330">From `Keywords_latvia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-331">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-332">이 함수 `Func_latvia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-333">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="f6541-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="f6541-335">개인 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-335">personal code</span></span>
  
<span data-ttu-id="f6541-336">개인 코드 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-336">personal code number</span></span>
  
<span data-ttu-id="f6541-337">개인 인증서 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-337">personal certificate number</span></span>
  
<span data-ttu-id="f6541-338">personalcodeno#</span><span class="sxs-lookup"><span data-stu-id="f6541-338">personalcodeno#</span></span>
  
<span data-ttu-id="f6541-339">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-339">personal id number</span></span>
  
<span data-ttu-id="f6541-340">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-340">personal id code</span></span>
  
<span data-ttu-id="f6541-341">가상 사용자 kods</span><span class="sxs-lookup"><span data-stu-id="f6541-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="f6541-342">리투아니아</span><span class="sxs-lookup"><span data-stu-id="f6541-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="f6541-343">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-343">Format</span></span>

<span data-ttu-id="f6541-344">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-345">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-345">Pattern</span></span>

<span data-ttu-id="f6541-346">공백과 구분 기호를 사용 하지 않고 11 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="f6541-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="f6541-347">사용자의 성별 및 출생 세기에 해당 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="f6541-348">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="f6541-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="f6541-349">출생 날짜의 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="f6541-350">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-351">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-351">Checksum</span></span>

<span data-ttu-id="f6541-352">예</span><span class="sxs-lookup"><span data-stu-id="f6541-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-353">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-353">Definition</span></span>

<span data-ttu-id="f6541-354">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-355">이 함수 `Func_lithuania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-356">From `Keywords_lithuania_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-357">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-358">이 함수 `Func_lithuania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-359">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="f6541-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="f6541-361">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-361">personal numeric code</span></span>
  
<span data-ttu-id="f6541-362">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-362">unique identification number</span></span>
  
<span data-ttu-id="f6541-363">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-363">citizen service number</span></span>
  
<span data-ttu-id="f6541-364">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-364">unique identity number</span></span>
  
<span data-ttu-id="f6541-365">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="f6541-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="f6541-366">개인 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-366">personal code.</span></span>
  
<span data-ttu-id="f6541-367">as메이 inis kodas</span><span class="sxs-lookup"><span data-stu-id="f6541-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="f6541-368">unikalus identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="f6541-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="f6541-369">piliečio paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="f6541-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="f6541-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="f6541-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="f6541-371">asmens kodas.</span><span class="sxs-lookup"><span data-stu-id="f6541-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="f6541-372">셈</span><span class="sxs-lookup"><span data-stu-id="f6541-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="f6541-373">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-373">Format</span></span>

<span data-ttu-id="f6541-374">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-375">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-375">Pattern</span></span>

<span data-ttu-id="f6541-376">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-376">11 digits</span></span>
  
- <span data-ttu-id="f6541-377">사용자의 성별 및 출생 세기에 해당 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="f6541-378">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="f6541-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="f6541-379">출생 날짜의 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="f6541-380">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-381">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-381">Checksum</span></span>

<span data-ttu-id="f6541-382">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="f6541-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-383">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-383">Definition</span></span>

<span data-ttu-id="f6541-384">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-385">정규식이 해당 `Regex_luxemburg_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-386">From `Keywords_luxemburg_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-387">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="f6541-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="f6541-389">개인 id</span><span class="sxs-lookup"><span data-stu-id="f6541-389">personal id</span></span>
  
<span data-ttu-id="f6541-390">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-390">personal id number</span></span>
  
<span data-ttu-id="f6541-391">personalidno#</span><span class="sxs-lookup"><span data-stu-id="f6541-391">personalidno#</span></span>
  
<span data-ttu-id="f6541-392">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-392">unique id number</span></span>
  
<span data-ttu-id="f6541-393">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="f6541-393">personalidnumber#</span></span>
  
<span data-ttu-id="f6541-394">고유 id 키</span><span class="sxs-lookup"><span data-stu-id="f6541-394">unique id key</span></span>
  
<span data-ttu-id="f6541-395">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-395">personal id code</span></span>
  
<span data-ttu-id="f6541-396">uniqueidkey#</span><span class="sxs-lookup"><span data-stu-id="f6541-396">uniqueidkey#</span></span>
  
<span data-ttu-id="f6541-397">개별 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-397">individual code</span></span>
  
<span data-ttu-id="f6541-398">개별 id</span><span class="sxs-lookup"><span data-stu-id="f6541-398">individual id</span></span>
  
<span data-ttu-id="f6541-399">eindeutige id-nummer</span><span class="sxs-lookup"><span data-stu-id="f6541-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="f6541-400">eindeutige id</span><span class="sxs-lookup"><span data-stu-id="f6541-400">eindeutige id</span></span>
  
<span data-ttu-id="f6541-401">id personnelle</span><span class="sxs-lookup"><span data-stu-id="f6541-401">id personnelle</span></span>
  
<span data-ttu-id="f6541-402">numéro d'identification 담당자</span><span class="sxs-lookup"><span data-stu-id="f6541-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="f6541-403">idpersonnelle#</span><span class="sxs-lookup"><span data-stu-id="f6541-403">idpersonnelle#</span></span>
  
<span data-ttu-id="f6541-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="f6541-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="f6541-405">eindeutigeid#</span><span class="sxs-lookup"><span data-stu-id="f6541-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="f6541-406">몰타</span><span class="sxs-lookup"><span data-stu-id="f6541-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="f6541-407">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-407">Format</span></span>

<span data-ttu-id="f6541-408">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-409">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-409">Pattern</span></span>

<span data-ttu-id="f6541-410">7 자리 숫자와 문자 1 개:</span><span class="sxs-lookup"><span data-stu-id="f6541-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="f6541-411">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-411">Seven digits</span></span> 
    
- <span data-ttu-id="f6541-412">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="f6541-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-413">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-413">Checksum</span></span>

<span data-ttu-id="f6541-414">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="f6541-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-415">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-415">Definition</span></span>

<span data-ttu-id="f6541-416">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-417">정규식이 해당 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-418">From `Keywords_malta_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-419">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-420">정규식이 해당 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-421">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="f6541-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="f6541-423">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-423">personal numeric code</span></span>
  
<span data-ttu-id="f6541-424">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-424">unique identification number</span></span>
  
<span data-ttu-id="f6541-425">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-425">citizen service number</span></span>
  
<span data-ttu-id="f6541-426">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-426">unique identity number</span></span>
  
<span data-ttu-id="f6541-427">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="f6541-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="f6541-428">kodiċi numerali personali</span><span class="sxs-lookup"><span data-stu-id="f6541-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="f6541-429">numru ta ' uniku</span><span class="sxs-lookup"><span data-stu-id="f6541-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="f6541-430">numru taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="f6541-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="f6541-431">numru ta ' uniku</span><span class="sxs-lookup"><span data-stu-id="f6541-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="f6541-432">네덜란드</span><span class="sxs-lookup"><span data-stu-id="f6541-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="f6541-433">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-433">Format</span></span>

<span data-ttu-id="f6541-434">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-435">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-435">Pattern</span></span>

<span data-ttu-id="f6541-436">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f6541-437">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-437">Checksum</span></span>

<span data-ttu-id="f6541-438">예</span><span class="sxs-lookup"><span data-stu-id="f6541-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-439">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-439">Definition</span></span>

<span data-ttu-id="f6541-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-441">이 함수 `Func_netherlands_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-442">From 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-442">A keyword from is found.</span></span>
    
<span data-ttu-id="f6541-443">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-444">이 함수 `Func_netherlands_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-445">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="f6541-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="f6541-447">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-447">personal numeric code</span></span>
  
<span data-ttu-id="f6541-448">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-448">unique identification number</span></span>
  
<span data-ttu-id="f6541-449">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-449">citizen service number</span></span>
  
<span data-ttu-id="f6541-450">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-450">unique identity number</span></span>
  
<span data-ttu-id="f6541-451">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="f6541-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="f6541-452">bsn</span><span class="sxs-lookup"><span data-stu-id="f6541-452">bsn</span></span>
  
<span data-ttu-id="f6541-453">bsn</span><span class="sxs-lookup"><span data-stu-id="f6541-453">bsn#</span></span>
  
<span data-ttu-id="f6541-454">persoonlijke 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="f6541-455">identificatienummer</span><span class="sxs-lookup"><span data-stu-id="f6541-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="f6541-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="f6541-456">burgerservicenummer</span></span>
  
<span data-ttu-id="f6541-457">identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="f6541-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="f6541-458">폴란드</span><span class="sxs-lookup"><span data-stu-id="f6541-458">Poland</span></span>

<span data-ttu-id="f6541-459">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"폴란드 국가 ID (PESEL)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="f6541-460">포르투갈</span><span class="sxs-lookup"><span data-stu-id="f6541-460">Portugal</span></span>

<span data-ttu-id="f6541-461">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"포르투갈 시민이 카드 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="f6541-462">루마니아</span><span class="sxs-lookup"><span data-stu-id="f6541-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="f6541-463">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-463">Format</span></span>

<span data-ttu-id="f6541-464">공백과 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-465">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-465">Pattern</span></span>

<span data-ttu-id="f6541-466">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f6541-467">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-467">Checksum</span></span>

<span data-ttu-id="f6541-468">예</span><span class="sxs-lookup"><span data-stu-id="f6541-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-469">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-469">Definition</span></span>

<span data-ttu-id="f6541-470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-471">이 함수 `Func_romania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-472">From `Keywords_romania_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-473">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-474">이 함수 `Func_romania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-475">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="f6541-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="f6541-477">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-477">personal numeric code</span></span>
  
<span data-ttu-id="f6541-478">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-478">unique identification number</span></span>
  
<span data-ttu-id="f6541-479">cnp</span><span class="sxs-lookup"><span data-stu-id="f6541-479">cnp</span></span>
  
<span data-ttu-id="f6541-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="f6541-480">cnp#</span></span>
  
<span data-ttu-id="f6541-481">pin</span><span class="sxs-lookup"><span data-stu-id="f6541-481">pin</span></span>
  
<span data-ttu-id="f6541-482">pin</span><span class="sxs-lookup"><span data-stu-id="f6541-482">pin#</span></span>
  
<span data-ttu-id="f6541-483">보험 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-483">insurance number</span></span>
  
<span data-ttu-id="f6541-484">insurancenumber#</span><span class="sxs-lookup"><span data-stu-id="f6541-484">insurancenumber#</span></span>
  
<span data-ttu-id="f6541-485">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-485">unique identity number</span></span>
  
<span data-ttu-id="f6541-486">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="f6541-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="f6541-487">cod 숫자 개인</span><span class="sxs-lookup"><span data-stu-id="f6541-487">cod numeric personal</span></span>
  
<span data-ttu-id="f6541-488">cod identificare personal</span><span class="sxs-lookup"><span data-stu-id="f6541-488">cod identificare personal</span></span>
  
<span data-ttu-id="f6541-489">cod unic identificare</span><span class="sxs-lookup"><span data-stu-id="f6541-489">cod unic identificare</span></span>
  
<span data-ttu-id="f6541-490">număr personal unic</span><span class="sxs-lookup"><span data-stu-id="f6541-490">număr personal unic</span></span>
  
<span data-ttu-id="f6541-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="f6541-491">număr identitate</span></span>
  
<span data-ttu-id="f6541-492">număr identificare personal</span><span class="sxs-lookup"><span data-stu-id="f6541-492">număr identificare personal</span></span>
  
<span data-ttu-id="f6541-493">număridentitate#</span><span class="sxs-lookup"><span data-stu-id="f6541-493">număridentitate#</span></span>
  
<span data-ttu-id="f6541-494">codnumericpersonal#</span><span class="sxs-lookup"><span data-stu-id="f6541-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="f6541-495">numărpersonalunic#</span><span class="sxs-lookup"><span data-stu-id="f6541-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="f6541-496">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="f6541-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="f6541-497">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-497">Format</span></span>

<span data-ttu-id="f6541-498">백슬래시 하나를 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-499">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-499">Pattern</span></span>

<span data-ttu-id="f6541-500">백슬래시 하나를 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="f6541-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f6541-501">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-501">Checksum</span></span>

<span data-ttu-id="f6541-502">예</span><span class="sxs-lookup"><span data-stu-id="f6541-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-503">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-503">Definition</span></span>

<span data-ttu-id="f6541-504">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-505">이 함수 `Func_slovakia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-506">From `Keywords_slovakia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-507">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-508">이 함수 `Func_slovakia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-509">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="f6541-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="f6541-511">돌 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-511">birth number</span></span>
  
<span data-ttu-id="f6541-512">national identification number</span><span class="sxs-lookup"><span data-stu-id="f6541-512">national identification number</span></span>
  
<span data-ttu-id="f6541-513">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-513">personal identification number</span></span>
  
<span data-ttu-id="f6541-514">social security number</span><span class="sxs-lookup"><span data-stu-id="f6541-514">social security number</span></span>
  
<span data-ttu-id="f6541-515">nationalnumber#</span><span class="sxs-lookup"><span data-stu-id="f6541-515">nationalnumber#</span></span>
  
<span data-ttu-id="f6541-516">ssn</span><span class="sxs-lookup"><span data-stu-id="f6541-516">ssn#</span></span>
  
<span data-ttu-id="f6541-517">ssn</span><span class="sxs-lookup"><span data-stu-id="f6541-517">ssn</span></span>
  
<span data-ttu-id="f6541-518">국가 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-518">national number</span></span>
  
<span data-ttu-id="f6541-519">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-519">personal id number</span></span>
  
<span data-ttu-id="f6541-520">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="f6541-520">personalidnumber#</span></span>
  
<span data-ttu-id="f6541-521">rč</span><span class="sxs-lookup"><span data-stu-id="f6541-521">rč</span></span>
  
<span data-ttu-id="f6541-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="f6541-522">rodné číslo</span></span>
  
<span data-ttu-id="f6541-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="f6541-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="f6541-524">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="f6541-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="f6541-525">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-525">Format</span></span>

<span data-ttu-id="f6541-526">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-527">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-527">Pattern</span></span>

<span data-ttu-id="f6541-528">지정 된 패턴의 13 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="f6541-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="f6541-529">생년월일 (DDMMLLL)에 해당 하는 7 자리 숫자 이며 "LLL"은 출생 연도의 마지막 세 자리에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="f6541-530">출생 면적에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="f6541-531">같은 날에 태어난 사용자의 성별 및 일련 번호 조합에 해당 하는 3 자리 숫자 (남성는 000-499, 암은 500-999)</span><span class="sxs-lookup"><span data-stu-id="f6541-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="f6541-532">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-533">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-533">Checksum</span></span>

<span data-ttu-id="f6541-534">예</span><span class="sxs-lookup"><span data-stu-id="f6541-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-535">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-535">Definition</span></span>

<span data-ttu-id="f6541-536">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-537">이 함수 `Func_slovenia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-538">From `Keywords_slovenia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f6541-539">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-540">이 함수 `Func_slovenia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-541">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="f6541-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="f6541-543">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="f6541-543">personal numeric code</span></span>
  
<span data-ttu-id="f6541-544">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-544">unique identification number</span></span>
  
<span data-ttu-id="f6541-545">고유 등록 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-545">unique registration number</span></span>
  
<span data-ttu-id="f6541-546">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-546">unique identity number</span></span>
  
<span data-ttu-id="f6541-547">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="f6541-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="f6541-548">고유 마스터 시민 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-548">unique master citizen number</span></span>
  
<span data-ttu-id="f6541-549">ed명령이 vena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="f6541-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="f6541-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="f6541-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="f6541-551">ed명령이 vena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="f6541-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="f6541-552">emšo</span><span class="sxs-lookup"><span data-stu-id="f6541-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="f6541-553">스페인</span><span class="sxs-lookup"><span data-stu-id="f6541-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="f6541-554">형식일</span><span class="sxs-lookup"><span data-stu-id="f6541-554">Format</span></span>

<span data-ttu-id="f6541-555">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f6541-556">패턴</span><span class="sxs-lookup"><span data-stu-id="f6541-556">Pattern</span></span>

<span data-ttu-id="f6541-557">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="f6541-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="f6541-558">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="f6541-558">Seven digits</span></span>
    
- <span data-ttu-id="f6541-559">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="f6541-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f6541-560">제외</span><span class="sxs-lookup"><span data-stu-id="f6541-560">Checksum</span></span>

<span data-ttu-id="f6541-561">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="f6541-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f6541-562">정의</span><span class="sxs-lookup"><span data-stu-id="f6541-562">Definition</span></span>

<span data-ttu-id="f6541-563">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f6541-564">정규식이 해당 `Regex_spain_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f6541-565">From `Keywords_spain_eu_national_id_card"` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="f6541-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f6541-566">키워드</span><span class="sxs-lookup"><span data-stu-id="f6541-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="f6541-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f6541-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="f6541-568">dni</span><span class="sxs-lookup"><span data-stu-id="f6541-568">dni</span></span>
  
<span data-ttu-id="f6541-569">national identification number</span><span class="sxs-lookup"><span data-stu-id="f6541-569">national identification number</span></span>
  
<span data-ttu-id="f6541-570">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-570">national identity number</span></span>
  
<span data-ttu-id="f6541-571">보험 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-571">insurance number</span></span>
  
<span data-ttu-id="f6541-572">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-572">personal identification number</span></span>
  
<span data-ttu-id="f6541-573">국가 id</span><span class="sxs-lookup"><span data-stu-id="f6541-573">national identity</span></span>
  
<span data-ttu-id="f6541-574">개인 id 없음</span><span class="sxs-lookup"><span data-stu-id="f6541-574">personal identity no</span></span>
  
<span data-ttu-id="f6541-575">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="f6541-575">unique identity number</span></span>
  
<span data-ttu-id="f6541-576">nationalidno#</span><span class="sxs-lookup"><span data-stu-id="f6541-576">nationalidno#</span></span>
  
<span data-ttu-id="f6541-577">uniqueid</span><span class="sxs-lookup"><span data-stu-id="f6541-577">uniqueid#</span></span>
  
<span data-ttu-id="f6541-578">dni</span><span class="sxs-lookup"><span data-stu-id="f6541-578">dni#</span></span>
  
<span data-ttu-id="f6541-579">nationalid#</span><span class="sxs-lookup"><span data-stu-id="f6541-579">nationalid#</span></span>
  
<span data-ttu-id="f6541-580">nie #</span><span class="sxs-lookup"><span data-stu-id="f6541-580">nie#</span></span>
  
<span data-ttu-id="f6541-581">nie</span><span class="sxs-lookup"><span data-stu-id="f6541-581">nie</span></span>
  
<span data-ttu-id="f6541-582">nienúmero#</span><span class="sxs-lookup"><span data-stu-id="f6541-582">nienúmero#</span></span>
  
<span data-ttu-id="f6541-583">nie número</span><span class="sxs-lookup"><span data-stu-id="f6541-583">nie número</span></span>
  
<span data-ttu-id="f6541-584">documento nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="f6541-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="f6541-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="f6541-585">identidad único</span></span>
  
<span data-ttu-id="f6541-586">número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="f6541-586">número nacional identidad</span></span>
  
<span data-ttu-id="f6541-587">dni número</span><span class="sxs-lookup"><span data-stu-id="f6541-587">dni número</span></span>
  
<span data-ttu-id="f6541-588">dninúmero#</span><span class="sxs-lookup"><span data-stu-id="f6541-588">dninúmero#</span></span>
  
<span data-ttu-id="f6541-589">identidadúnico#</span><span class="sxs-lookup"><span data-stu-id="f6541-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="f6541-590">스웨덴</span><span class="sxs-lookup"><span data-stu-id="f6541-590">Sweden</span></span>

<span data-ttu-id="f6541-591">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스웨덴 국가 ID" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6541-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f6541-592">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f6541-592">See also</span></span>

[<span data-ttu-id="f6541-593">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="f6541-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

