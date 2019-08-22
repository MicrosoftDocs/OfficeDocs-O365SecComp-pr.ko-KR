---
title: EU 국가 식별 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 국가 식별 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: cbcacb3f85877f5a84238468fb52d612d90f5f0b
ms.sourcegitcommit: 3f3f3ecb28ef65d023f3573f9a4e09a0586d8f53
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2019
ms.locfileid: "36490775"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="77f15-104">EU 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-104">EU National Identification Number</span></span>

<span data-ttu-id="77f15-105">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 국가 식별 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="77f15-106">이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="77f15-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="77f15-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="77f15-108">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-108">Format</span></span>

<span data-ttu-id="77f15-109">문자, 숫자 및 특수 문자의 24 자 조합</span><span class="sxs-lookup"><span data-stu-id="77f15-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-110">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-110">Pattern</span></span>

<span data-ttu-id="77f15-111">24 문자:</span><span class="sxs-lookup"><span data-stu-id="77f15-111">24 characters:</span></span>
  
-  <span data-ttu-id="77f15-112">22 개 문자 (대/소문자 구분 안 함), 숫자, 백슬래시, 슬래시 또는 더하기 기호</span><span class="sxs-lookup"><span data-stu-id="77f15-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="77f15-113">2 개의 문자 (대/소문자 구분 안 함), 숫자, 백슬래시, 슬래시, 더하기 기호 또는 등호</span><span class="sxs-lookup"><span data-stu-id="77f15-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-114">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-114">Checksum</span></span>

<span data-ttu-id="77f15-115">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="77f15-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-116">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-116">Definition</span></span>

<span data-ttu-id="77f15-117">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-118">정규식이 해당 `Regex_austria_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-119">From `Keywords_austria_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="77f15-120">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-120">Keywords</span></span>

#### <a name="keywords_austria_eu_national_id_card"></a><span data-ttu-id="77f15-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="77f15-122">오스트리아 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-122">austrian identity number</span></span>
  
<span data-ttu-id="77f15-123">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-123">national identity number</span></span>
  
<span data-ttu-id="77f15-124">id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-124">identity number</span></span>
  
<span data-ttu-id="77f15-125">national id</span><span class="sxs-lookup"><span data-stu-id="77f15-125">national id</span></span>
  
<span data-ttu-id="77f15-126">personalausweis republik österreich</span><span class="sxs-lookup"><span data-stu-id="77f15-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="77f15-127">벨기에</span><span class="sxs-lookup"><span data-stu-id="77f15-127">Belgium</span></span>

<span data-ttu-id="77f15-128">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"벨기에 국가 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="77f15-129">불가리아</span><span class="sxs-lookup"><span data-stu-id="77f15-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="77f15-130">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-130">Format</span></span>

<span data-ttu-id="77f15-131">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-132">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-132">Pattern</span></span>

<span data-ttu-id="77f15-133">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="77f15-134">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="77f15-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="77f15-135">출생 순서에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="77f15-136">성별에 해당 하는 1 자리 숫자와이에 해당 하는 짝수 자리 숫자 및 암의 홀수 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="77f15-137">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-138">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-138">Checksum</span></span>

<span data-ttu-id="77f15-139">예</span><span class="sxs-lookup"><span data-stu-id="77f15-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-140">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-140">Definition</span></span>

<span data-ttu-id="77f15-141">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-142">이 함수 `Func_bulgaria_national_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-143">From `Keywords_bulgaria_national_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="77f15-144">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-145">이 함수 `Func_bulgaria_national_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-146">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-146">Keywords</span></span>

#### <a name="keywords_bulgaria_national_number"></a><span data-ttu-id="77f15-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="77f15-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="77f15-148">egn</span><span class="sxs-lookup"><span data-stu-id="77f15-148">egn</span></span>
  
<span data-ttu-id="77f15-149">egn #</span><span class="sxs-lookup"><span data-stu-id="77f15-149">egn#</span></span>
  
<span data-ttu-id="77f15-150">불가리아어 국가 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-150">bulgarian national number</span></span>
  
<span data-ttu-id="77f15-151">국가 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-151">national number</span></span>
  
<span data-ttu-id="77f15-152">social security number</span><span class="sxs-lookup"><span data-stu-id="77f15-152">social security number</span></span>
  
<span data-ttu-id="77f15-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="77f15-153">nationalnumber#</span></span>
  
<span data-ttu-id="77f15-154">ssn #</span><span class="sxs-lookup"><span data-stu-id="77f15-154">ssn#</span></span>
  
<span data-ttu-id="77f15-155">ssn</span><span class="sxs-lookup"><span data-stu-id="77f15-155">ssn</span></span>
  
<span data-ttu-id="77f15-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="77f15-156">nationalnumber</span></span>
  
<span data-ttu-id="77f15-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="77f15-157">bnn#</span></span>
  
<span data-ttu-id="77f15-158">bnn</span><span class="sxs-lookup"><span data-stu-id="77f15-158">bnn</span></span>
  
<span data-ttu-id="77f15-159">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-159">personal id number</span></span>
  
<span data-ttu-id="77f15-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="77f15-160">personalidnumber#</span></span>
  
<span data-ttu-id="77f15-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="77f15-161">единен граждански номер</span></span>
  
<span data-ttu-id="77f15-162">edinen grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="77f15-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="77f15-163">егн</span><span class="sxs-lookup"><span data-stu-id="77f15-163">егн</span></span>
  
<span data-ttu-id="77f15-164">егн #</span><span class="sxs-lookup"><span data-stu-id="77f15-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="77f15-165">크로아티아</span><span class="sxs-lookup"><span data-stu-id="77f15-165">Croatia</span></span>

<span data-ttu-id="77f15-166">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"크로아티아 id 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="77f15-167">키프로스</span><span class="sxs-lookup"><span data-stu-id="77f15-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="77f15-168">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-168">Format</span></span>

<span data-ttu-id="77f15-169">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-170">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-170">Pattern</span></span>

 <span data-ttu-id="77f15-171">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="77f15-172">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-172">Checksum</span></span>

<span data-ttu-id="77f15-173">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="77f15-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-174">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-174">Definition</span></span>

<span data-ttu-id="77f15-175">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-176">정규식이 해당 `Regex_cyprus_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-177">From `Keywords_cyprus_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="77f15-178">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-178">Keywords</span></span>

#### <a name="keywords_cyprus_eu_national_id_card"></a><span data-ttu-id="77f15-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="77f15-180">id 카드 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-180">id card number</span></span>
  
<span data-ttu-id="77f15-181">national identification number</span><span class="sxs-lookup"><span data-stu-id="77f15-181">national identification number</span></span>
  
<span data-ttu-id="77f15-182">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-182">personal id number</span></span>
  
<span data-ttu-id="77f15-183">id 카드 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-183">identity card number</span></span>
  
<span data-ttu-id="77f15-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="77f15-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="77f15-185">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="77f15-185">Czech Republic</span></span>

<span data-ttu-id="77f15-186">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"체코어 국내 id 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="77f15-187">덴마크</span><span class="sxs-lookup"><span data-stu-id="77f15-187">Denmark</span></span>

<span data-ttu-id="77f15-188">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"덴마크 개인 식별 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="77f15-189">에스토니아</span><span class="sxs-lookup"><span data-stu-id="77f15-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="77f15-190">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-190">Format</span></span>

<span data-ttu-id="77f15-191">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-192">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-192">Pattern</span></span>

<span data-ttu-id="77f15-193">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="77f15-193">11 digits:</span></span>
  
- <span data-ttu-id="77f15-194">출생의 성별 및 세기에 해당 하는 1 자리 숫자 (예: 1-2 암, 수, 19th 세기, 3-4:20th 세기, 5-6 = 21 세기)</span><span class="sxs-lookup"><span data-stu-id="77f15-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="77f15-195">출생 날짜에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="77f15-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="77f15-196">같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="77f15-197">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-198">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-198">Checksum</span></span>

<span data-ttu-id="77f15-199">예</span><span class="sxs-lookup"><span data-stu-id="77f15-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-200">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-200">Definition</span></span>

<span data-ttu-id="77f15-201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-202">이 함수 `Func_estonia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-203">From `Keywords_estonia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-204">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-205">이 함수 `Func_estonia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-206">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-206">Keywords</span></span>

#### <a name="keywords_estonia_eu_national_id_card"></a><span data-ttu-id="77f15-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="77f15-208">개인 식별 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-208">personal identification code</span></span>
  
<span data-ttu-id="77f15-209">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-209">personal identification number</span></span>
  
<span data-ttu-id="77f15-210">national identification number</span><span class="sxs-lookup"><span data-stu-id="77f15-210">national identification number</span></span>
  
<span data-ttu-id="77f15-211">국가 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-211">national number</span></span>
  
<span data-ttu-id="77f15-212">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-212">personal id number</span></span>
  
<span data-ttu-id="77f15-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="77f15-213">personalidnumber#</span></span>
  
<span data-ttu-id="77f15-214">ik</span><span class="sxs-lookup"><span data-stu-id="77f15-214">ik</span></span>
  
<span data-ttu-id="77f15-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="77f15-215">isikukood</span></span>
  
<span data-ttu-id="77f15-216">id-kaart</span><span class="sxs-lookup"><span data-stu-id="77f15-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="77f15-217">핀란드</span><span class="sxs-lookup"><span data-stu-id="77f15-217">Finland</span></span>

<span data-ttu-id="77f15-218">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"핀란드 국가 ID" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="77f15-219">프랑스</span><span class="sxs-lookup"><span data-stu-id="77f15-219">France</span></span>

<span data-ttu-id="77f15-220">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 국가 ID 카드 (cni)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="77f15-221">독일</span><span class="sxs-lookup"><span data-stu-id="77f15-221">Germany</span></span>

<span data-ttu-id="77f15-222">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 Id 카드 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="77f15-223">그리스</span><span class="sxs-lookup"><span data-stu-id="77f15-223">Greece</span></span>

<span data-ttu-id="77f15-224">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"그리스 국가 ID 카드" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="77f15-225">헝가리</span><span class="sxs-lookup"><span data-stu-id="77f15-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="77f15-226">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-226">Format</span></span>

<span data-ttu-id="77f15-227">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-228">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-228">Pattern</span></span>

<span data-ttu-id="77f15-229">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="77f15-229">11 digits:</span></span>
  
-  <span data-ttu-id="77f15-230">성별에 해당 하는 1 자리 숫자 (1gb, 2 암, 기타 번호는 두 개를 포함 하는 경우 1900에만 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="77f15-231">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="77f15-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="77f15-232">일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="77f15-233">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-234">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-234">Checksum</span></span>

<span data-ttu-id="77f15-235">예</span><span class="sxs-lookup"><span data-stu-id="77f15-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-236">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-236">Definition</span></span>

<span data-ttu-id="77f15-237">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-238">이 함수 `Func_hungary_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-239">From `Keywords_hungary_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-240">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-241">이 함수 `Func_hungary_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-242">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-242">Keywords</span></span>

#### <a name="keywords_hungary_eu_national_id_card"></a><span data-ttu-id="77f15-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="77f15-244">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-244">personal identification number</span></span>
  
<span data-ttu-id="77f15-245">identification number</span><span class="sxs-lookup"><span data-stu-id="77f15-245">identification number</span></span>
  
<span data-ttu-id="77f15-246">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-246">personal id number</span></span>
  
<span data-ttu-id="77f15-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="77f15-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="77f15-248">Ireland</span><span class="sxs-lookup"><span data-stu-id="77f15-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="77f15-249">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-249">Format</span></span>

<span data-ttu-id="77f15-250">지정 된 패턴에서 문자, 숫자 및 공백의 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="77f15-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-251">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-251">Pattern</span></span>

<span data-ttu-id="77f15-252">지정 된 패턴에서 문자, 숫자 및 공백의 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="77f15-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="77f15-253">01 년 1 월 2013 일 현재 위치:</span><span class="sxs-lookup"><span data-stu-id="77f15-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="77f15-254">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-254">Seven digits</span></span> 
    
- <span data-ttu-id="77f15-255">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-255">One check digit</span></span>
    
- <span data-ttu-id="77f15-256">1 개의 공백 또는 대문자 "W" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="77f15-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="77f15-257">01 년 1 월 2013 일 이전:</span><span class="sxs-lookup"><span data-stu-id="77f15-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="77f15-258">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-258">Seven digits</span></span> 
    
- <span data-ttu-id="77f15-259">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-259">One check digit</span></span>
    
- <span data-ttu-id="77f15-260">1 개의 공백 또는 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="77f15-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-261">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-261">Checksum</span></span>

<span data-ttu-id="77f15-262">예</span><span class="sxs-lookup"><span data-stu-id="77f15-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-263">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-263">Definition</span></span>

<span data-ttu-id="77f15-264">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-265">이 함수는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="77f15-266">From 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-266">A keyword from is found.</span></span>
    
<span data-ttu-id="77f15-267">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-268">이 함수는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-269">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-269">Keywords</span></span>

#### <a name="keywords_ireland_eu_national_id_card"></a><span data-ttu-id="77f15-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="77f15-271">개인 공용 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-271">personal public service number</span></span>
  
<span data-ttu-id="77f15-272">pps 아니요</span><span class="sxs-lookup"><span data-stu-id="77f15-272">pps no</span></span>
  
<span data-ttu-id="77f15-273">수입 및 주민 등록 보험 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="77f15-274">rsi 아니요</span><span class="sxs-lookup"><span data-stu-id="77f15-274">rsi no</span></span>
  
<span data-ttu-id="77f15-275">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-275">personal identification number</span></span>
  
<span data-ttu-id="77f15-276">identification number</span><span class="sxs-lookup"><span data-stu-id="77f15-276">identification number</span></span>
  
<span data-ttu-id="77f15-277">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-277">personal id number</span></span>
  
<span data-ttu-id="77f15-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="77f15-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="77f15-279">uimh</span><span class="sxs-lookup"><span data-stu-id="77f15-279">uimh.</span></span> <span data-ttu-id="77f15-280">psp</span><span class="sxs-lookup"><span data-stu-id="77f15-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="77f15-281">이탈리아</span><span class="sxs-lookup"><span data-stu-id="77f15-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="77f15-282">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-282">Format</span></span>

<span data-ttu-id="77f15-283">지정 된 패턴에 해당 하는 문자 및 숫자의 16 자 조합</span><span class="sxs-lookup"><span data-stu-id="77f15-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-284">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-284">Pattern</span></span>

<span data-ttu-id="77f15-285">문자와 숫자의 16 자 조합:</span><span class="sxs-lookup"><span data-stu-id="77f15-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="77f15-286">가족 이름에서 처음 세 개의 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="77f15-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="77f15-287">이름의 첫 번째, 세 번째 및 네 번째 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="77f15-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="77f15-288">출생 연도의 마지막 자리에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="77f15-289">출생 월의 문자에 해당 하는 한 문자는 알파벳 순서로 사용 되지만 1 ~ E, H, L, M, P, R에 해당 하는 문자를 사용 하는 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="77f15-290">Genders를 구분 하기 위해 출생 달의 날짜에 해당 하는 2 자리 숫자 (40)가 여성 생년월일에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="77f15-291">사용자가 태어난 municipality 관련 지역 번호에 해당 하는 4 자리 숫자 (국가 전체 코드는 외국 국가에 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="77f15-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="77f15-292">1 개의 패리티 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-293">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-293">Checksum</span></span>

<span data-ttu-id="77f15-294">예</span><span class="sxs-lookup"><span data-stu-id="77f15-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-295">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-295">Definition</span></span>

<span data-ttu-id="77f15-296">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-297">이 함수 `Func_italy_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-298">From `Keywords_italy_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-299">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-300">이 함수 `Func_italy_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-301">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-301">Keywords</span></span>

#### <a name="keywords_italy_eu_national_id_card"></a><span data-ttu-id="77f15-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="77f15-303">개인 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-303">personal code</span></span>
  
<span data-ttu-id="77f15-304">개인 코드 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-304">personal code number</span></span>
  
<span data-ttu-id="77f15-305">개인 인증서 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-305">personal certificate number</span></span>
  
<span data-ttu-id="77f15-306">회계 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-306">fiscal code</span></span>
  
<span data-ttu-id="77f15-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="77f15-307">personalcodeno#</span></span>
  
<span data-ttu-id="77f15-308">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-308">personal id number</span></span>
  
<span data-ttu-id="77f15-309">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-309">personal id code</span></span>
  
<span data-ttu-id="77f15-310">codice personale</span><span class="sxs-lookup"><span data-stu-id="77f15-310">codice personale</span></span>
  
<span data-ttu-id="77f15-311">numero certificato personale</span><span class="sxs-lookup"><span data-stu-id="77f15-311">numero certificato personale</span></span>
  
<span data-ttu-id="77f15-312">numero personale</span><span class="sxs-lookup"><span data-stu-id="77f15-312">numero personale</span></span>
  
<span data-ttu-id="77f15-313">numero id personale</span><span class="sxs-lookup"><span data-stu-id="77f15-313">numero id personale</span></span>
  
<span data-ttu-id="77f15-314">codice id personale</span><span class="sxs-lookup"><span data-stu-id="77f15-314">codice id personale</span></span>
  
<span data-ttu-id="77f15-315">codice</span><span class="sxs-lookup"><span data-stu-id="77f15-315">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="77f15-316">라트비아</span><span class="sxs-lookup"><span data-stu-id="77f15-316">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="77f15-317">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-317">Format</span></span>

<span data-ttu-id="77f15-318">지정 된 형식의 11 자리 숫자 및 하이픈</span><span class="sxs-lookup"><span data-stu-id="77f15-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-319">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-319">Pattern</span></span>

<span data-ttu-id="77f15-320">11 자리 숫자와 하이픈:</span><span class="sxs-lookup"><span data-stu-id="77f15-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="77f15-321">생년월일에 해당 하는 6 자리 숫자 (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="77f15-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="77f15-322">하이픈</span><span class="sxs-lookup"><span data-stu-id="77f15-322">A hyphen</span></span>
    
- <span data-ttu-id="77f15-323">출생 세기에 해당 하는 1 자리 숫자 (19th 세기의 경우 "1", 21 세기의 경우 "2")</span><span class="sxs-lookup"><span data-stu-id="77f15-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="77f15-324">임의로 생성 되는 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-325">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-325">Checksum</span></span>

<span data-ttu-id="77f15-326">예</span><span class="sxs-lookup"><span data-stu-id="77f15-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-327">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-327">Definition</span></span>

<span data-ttu-id="77f15-328">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-329">이 함수 `Func_latvia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-330">From `Keywords_latvia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-331">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-332">이 함수 `Func_latvia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-333">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-333">Keywords</span></span>

#### <a name="keywords_latvia_eu_national_id_card"></a><span data-ttu-id="77f15-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="77f15-335">개인 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-335">personal code</span></span>
  
<span data-ttu-id="77f15-336">개인 코드 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-336">personal code number</span></span>
  
<span data-ttu-id="77f15-337">개인 인증서 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-337">personal certificate number</span></span>
  
<span data-ttu-id="77f15-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="77f15-338">personalcodeno#</span></span>
  
<span data-ttu-id="77f15-339">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-339">personal id number</span></span>
  
<span data-ttu-id="77f15-340">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-340">personal id code</span></span>
  
<span data-ttu-id="77f15-341">가상 사용자 kods</span><span class="sxs-lookup"><span data-stu-id="77f15-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="77f15-342">리투아니아</span><span class="sxs-lookup"><span data-stu-id="77f15-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="77f15-343">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-343">Format</span></span>

<span data-ttu-id="77f15-344">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-345">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-345">Pattern</span></span>

<span data-ttu-id="77f15-346">공백과 구분 기호를 사용 하지 않고 11 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="77f15-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="77f15-347">사용자의 성별 및 출생 세기에 해당 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="77f15-348">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="77f15-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="77f15-349">출생 날짜의 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="77f15-350">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-351">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-351">Checksum</span></span>

<span data-ttu-id="77f15-352">예</span><span class="sxs-lookup"><span data-stu-id="77f15-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-353">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-353">Definition</span></span>

<span data-ttu-id="77f15-354">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-355">이 함수 `Func_lithuania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-356">From `Keywords_lithuania_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-357">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-358">이 함수 `Func_lithuania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-359">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-359">Keywords</span></span>

#### <a name="keywords_lithuania_eu_national_id_card"></a><span data-ttu-id="77f15-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="77f15-361">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-361">personal numeric code</span></span>
  
<span data-ttu-id="77f15-362">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-362">unique identification number</span></span>
  
<span data-ttu-id="77f15-363">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-363">citizen service number</span></span>
  
<span data-ttu-id="77f15-364">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-364">unique identity number</span></span>
  
<span data-ttu-id="77f15-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="77f15-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="77f15-366">개인 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-366">personal code.</span></span>
  
<span data-ttu-id="77f15-367">as메이 inis kodas</span><span class="sxs-lookup"><span data-stu-id="77f15-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="77f15-368">unikalus identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="77f15-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="77f15-369">piliečio paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="77f15-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="77f15-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="77f15-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="77f15-371">asmens kodas.</span><span class="sxs-lookup"><span data-stu-id="77f15-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="77f15-372">셈</span><span class="sxs-lookup"><span data-stu-id="77f15-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="77f15-373">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-373">Format</span></span>

<span data-ttu-id="77f15-374">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-375">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-375">Pattern</span></span>

<span data-ttu-id="77f15-376">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-376">11 digits</span></span>
  
- <span data-ttu-id="77f15-377">사용자의 성별 및 출생 세기에 해당 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="77f15-378">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="77f15-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="77f15-379">출생 날짜의 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="77f15-380">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-381">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-381">Checksum</span></span>

<span data-ttu-id="77f15-382">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="77f15-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-383">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-383">Definition</span></span>

<span data-ttu-id="77f15-384">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-385">정규식이 해당 `Regex_luxemburg_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-386">From `Keywords_luxemburg_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="77f15-387">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-387">Keywords</span></span>

#### <a name="keywords_luxemburg_eu_national_id_card"></a><span data-ttu-id="77f15-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="77f15-389">개인 id</span><span class="sxs-lookup"><span data-stu-id="77f15-389">personal id</span></span>
  
<span data-ttu-id="77f15-390">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-390">personal id number</span></span>
  
<span data-ttu-id="77f15-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="77f15-391">personalidno#</span></span>
  
<span data-ttu-id="77f15-392">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-392">unique id number</span></span>
  
<span data-ttu-id="77f15-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="77f15-393">personalidnumber#</span></span>
  
<span data-ttu-id="77f15-394">고유 id 키</span><span class="sxs-lookup"><span data-stu-id="77f15-394">unique id key</span></span>
  
<span data-ttu-id="77f15-395">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-395">personal id code</span></span>
  
<span data-ttu-id="77f15-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="77f15-396">uniqueidkey#</span></span>
  
<span data-ttu-id="77f15-397">개별 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-397">individual code</span></span>
  
<span data-ttu-id="77f15-398">개별 id</span><span class="sxs-lookup"><span data-stu-id="77f15-398">individual id</span></span>
  
<span data-ttu-id="77f15-399">eindeutige id-nummer</span><span class="sxs-lookup"><span data-stu-id="77f15-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="77f15-400">eindeutige id</span><span class="sxs-lookup"><span data-stu-id="77f15-400">eindeutige id</span></span>
  
<span data-ttu-id="77f15-401">id personnelle</span><span class="sxs-lookup"><span data-stu-id="77f15-401">id personnelle</span></span>
  
<span data-ttu-id="77f15-402">numéro d'identification 담당자</span><span class="sxs-lookup"><span data-stu-id="77f15-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="77f15-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="77f15-403">idpersonnelle#</span></span>
  
<span data-ttu-id="77f15-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="77f15-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="77f15-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="77f15-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="77f15-406">몰타</span><span class="sxs-lookup"><span data-stu-id="77f15-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="77f15-407">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-407">Format</span></span>

<span data-ttu-id="77f15-408">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-409">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-409">Pattern</span></span>

<span data-ttu-id="77f15-410">7 자리 숫자와 문자 1 개:</span><span class="sxs-lookup"><span data-stu-id="77f15-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="77f15-411">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-411">Seven digits</span></span> 
    
- <span data-ttu-id="77f15-412">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="77f15-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-413">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-413">Checksum</span></span>

<span data-ttu-id="77f15-414">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="77f15-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-415">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-415">Definition</span></span>

<span data-ttu-id="77f15-416">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-417">정규식이 해당 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-418">From `Keywords_malta_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-419">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-420">정규식이 해당 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-421">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-421">Keywords</span></span>

#### <a name="keywords_malta_eu_national_id_card"></a><span data-ttu-id="77f15-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="77f15-423">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-423">personal numeric code</span></span>
  
<span data-ttu-id="77f15-424">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-424">unique identification number</span></span>
  
<span data-ttu-id="77f15-425">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-425">citizen service number</span></span>
  
<span data-ttu-id="77f15-426">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-426">unique identity number</span></span>
  
<span data-ttu-id="77f15-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="77f15-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="77f15-428">kodiċi numerali personali</span><span class="sxs-lookup"><span data-stu-id="77f15-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="77f15-429">numru ta ' uniku</span><span class="sxs-lookup"><span data-stu-id="77f15-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="77f15-430">numru taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="77f15-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="77f15-431">numru ta ' uniku</span><span class="sxs-lookup"><span data-stu-id="77f15-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="77f15-432">네덜란드</span><span class="sxs-lookup"><span data-stu-id="77f15-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="77f15-433">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-433">Format</span></span>

<span data-ttu-id="77f15-434">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-435">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-435">Pattern</span></span>

<span data-ttu-id="77f15-436">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="77f15-437">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-437">Checksum</span></span>

<span data-ttu-id="77f15-438">예</span><span class="sxs-lookup"><span data-stu-id="77f15-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-439">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-439">Definition</span></span>

<span data-ttu-id="77f15-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-441">이 함수 `Func_netherlands_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-442">From 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-442">A keyword from is found.</span></span>
    
<span data-ttu-id="77f15-443">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-444">이 함수 `Func_netherlands_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-445">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-445">Keywords</span></span>

#### <a name="keywords_netherlands_eu_national_id_card"></a><span data-ttu-id="77f15-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="77f15-447">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-447">personal numeric code</span></span>
  
<span data-ttu-id="77f15-448">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-448">unique identification number</span></span>
  
<span data-ttu-id="77f15-449">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-449">citizen service number</span></span>
  
<span data-ttu-id="77f15-450">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-450">unique identity number</span></span>
  
<span data-ttu-id="77f15-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="77f15-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="77f15-452">bsn</span><span class="sxs-lookup"><span data-stu-id="77f15-452">bsn</span></span>
  
<span data-ttu-id="77f15-453">bsn #</span><span class="sxs-lookup"><span data-stu-id="77f15-453">bsn#</span></span>
  
<span data-ttu-id="77f15-454">persoonlijke 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="77f15-455">identificatienummer</span><span class="sxs-lookup"><span data-stu-id="77f15-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="77f15-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="77f15-456">burgerservicenummer</span></span>
  
<span data-ttu-id="77f15-457">identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="77f15-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="77f15-458">폴란드</span><span class="sxs-lookup"><span data-stu-id="77f15-458">Poland</span></span>

<span data-ttu-id="77f15-459">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"폴란드 국가 ID (PESEL)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="77f15-460">포르투갈</span><span class="sxs-lookup"><span data-stu-id="77f15-460">Portugal</span></span>

<span data-ttu-id="77f15-461">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"포르투갈 시민이 카드 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="77f15-462">루마니아</span><span class="sxs-lookup"><span data-stu-id="77f15-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="77f15-463">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-463">Format</span></span>

<span data-ttu-id="77f15-464">공백과 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-465">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-465">Pattern</span></span>

<span data-ttu-id="77f15-466">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="77f15-467">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-467">Checksum</span></span>

<span data-ttu-id="77f15-468">예</span><span class="sxs-lookup"><span data-stu-id="77f15-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-469">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-469">Definition</span></span>

<span data-ttu-id="77f15-470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-471">이 함수 `Func_romania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-472">From `Keywords_romania_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-473">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-474">이 함수 `Func_romania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-475">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-475">Keywords</span></span>

#### <a name="keywords_romania_eu_national_id_card"></a><span data-ttu-id="77f15-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="77f15-477">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-477">personal numeric code</span></span>
  
<span data-ttu-id="77f15-478">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-478">unique identification number</span></span>
  
<span data-ttu-id="77f15-479">cnp</span><span class="sxs-lookup"><span data-stu-id="77f15-479">cnp</span></span>
  
<span data-ttu-id="77f15-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="77f15-480">cnp#</span></span>
  
<span data-ttu-id="77f15-481">pin</span><span class="sxs-lookup"><span data-stu-id="77f15-481">pin</span></span>
  
<span data-ttu-id="77f15-482">pin #</span><span class="sxs-lookup"><span data-stu-id="77f15-482">pin#</span></span>
  
<span data-ttu-id="77f15-483">보험 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-483">insurance number</span></span>
  
<span data-ttu-id="77f15-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="77f15-484">insurancenumber#</span></span>
  
<span data-ttu-id="77f15-485">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-485">unique identity number</span></span>
  
<span data-ttu-id="77f15-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="77f15-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="77f15-487">cod 숫자 개인</span><span class="sxs-lookup"><span data-stu-id="77f15-487">cod numeric personal</span></span>
  
<span data-ttu-id="77f15-488">cod identificare personal</span><span class="sxs-lookup"><span data-stu-id="77f15-488">cod identificare personal</span></span>
  
<span data-ttu-id="77f15-489">cod unic identificare</span><span class="sxs-lookup"><span data-stu-id="77f15-489">cod unic identificare</span></span>
  
<span data-ttu-id="77f15-490">număr personal unic</span><span class="sxs-lookup"><span data-stu-id="77f15-490">număr personal unic</span></span>
  
<span data-ttu-id="77f15-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="77f15-491">număr identitate</span></span>
  
<span data-ttu-id="77f15-492">număr identificare personal</span><span class="sxs-lookup"><span data-stu-id="77f15-492">număr identificare personal</span></span>
  
<span data-ttu-id="77f15-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="77f15-493">număridentitate#</span></span>
  
<span data-ttu-id="77f15-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="77f15-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="77f15-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="77f15-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="77f15-496">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="77f15-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="77f15-497">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-497">Format</span></span>

<span data-ttu-id="77f15-498">백슬래시 하나를 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-499">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-499">Pattern</span></span>

<span data-ttu-id="77f15-500">백슬래시 하나를 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="77f15-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="77f15-501">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-501">Checksum</span></span>

<span data-ttu-id="77f15-502">예</span><span class="sxs-lookup"><span data-stu-id="77f15-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-503">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-503">Definition</span></span>

<span data-ttu-id="77f15-504">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-505">이 함수 `Func_slovakia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-506">From `Keywords_slovakia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-507">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-508">이 함수 `Func_slovakia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-509">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-509">Keywords</span></span>

#### <a name="keywords_slovakia_eu_national_id_card"></a><span data-ttu-id="77f15-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="77f15-511">돌 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-511">birth number</span></span>
  
<span data-ttu-id="77f15-512">national identification number</span><span class="sxs-lookup"><span data-stu-id="77f15-512">national identification number</span></span>
  
<span data-ttu-id="77f15-513">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-513">personal identification number</span></span>
  
<span data-ttu-id="77f15-514">social security number</span><span class="sxs-lookup"><span data-stu-id="77f15-514">social security number</span></span>
  
<span data-ttu-id="77f15-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="77f15-515">nationalnumber#</span></span>
  
<span data-ttu-id="77f15-516">ssn #</span><span class="sxs-lookup"><span data-stu-id="77f15-516">ssn#</span></span>
  
<span data-ttu-id="77f15-517">ssn</span><span class="sxs-lookup"><span data-stu-id="77f15-517">ssn</span></span>
  
<span data-ttu-id="77f15-518">국가 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-518">national number</span></span>
  
<span data-ttu-id="77f15-519">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-519">personal id number</span></span>
  
<span data-ttu-id="77f15-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="77f15-520">personalidnumber#</span></span>
  
<span data-ttu-id="77f15-521">rč</span><span class="sxs-lookup"><span data-stu-id="77f15-521">rč</span></span>
  
<span data-ttu-id="77f15-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="77f15-522">rodné číslo</span></span>
  
<span data-ttu-id="77f15-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="77f15-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="77f15-524">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="77f15-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="77f15-525">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-525">Format</span></span>

<span data-ttu-id="77f15-526">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-527">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-527">Pattern</span></span>

<span data-ttu-id="77f15-528">지정 된 패턴의 13 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="77f15-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="77f15-529">생년월일 (DDMMLLL)에 해당 하는 7 자리 숫자 이며 "LLL"은 출생 연도의 마지막 세 자리에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="77f15-530">출생 면적에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="77f15-531">같은 날에 태어난 사용자의 성별 및 일련 번호 조합에 해당 하는 3 자리 숫자 (남성는 000-499, 암은 500-999)</span><span class="sxs-lookup"><span data-stu-id="77f15-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="77f15-532">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-533">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-533">Checksum</span></span>

<span data-ttu-id="77f15-534">예</span><span class="sxs-lookup"><span data-stu-id="77f15-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-535">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-535">Definition</span></span>

<span data-ttu-id="77f15-536">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-537">이 함수 `Func_slovenia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-538">From `Keywords_slovenia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="77f15-539">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-540">이 함수 `Func_slovenia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="77f15-541">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-541">Keywords</span></span>

#### <a name="keywords_slovenia_eu_national_id_card"></a><span data-ttu-id="77f15-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="77f15-543">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="77f15-543">personal numeric code</span></span>
  
<span data-ttu-id="77f15-544">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-544">unique identification number</span></span>
  
<span data-ttu-id="77f15-545">고유 등록 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-545">unique registration number</span></span>
  
<span data-ttu-id="77f15-546">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-546">unique identity number</span></span>
  
<span data-ttu-id="77f15-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="77f15-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="77f15-548">고유 마스터 시민 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-548">unique master citizen number</span></span>
  
<span data-ttu-id="77f15-549">ed명령이 vena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="77f15-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="77f15-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="77f15-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="77f15-551">ed명령이 vena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="77f15-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="77f15-552">emšo</span><span class="sxs-lookup"><span data-stu-id="77f15-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="77f15-553">스페인</span><span class="sxs-lookup"><span data-stu-id="77f15-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="77f15-554">형식일</span><span class="sxs-lookup"><span data-stu-id="77f15-554">Format</span></span>

<span data-ttu-id="77f15-555">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="77f15-556">패턴</span><span class="sxs-lookup"><span data-stu-id="77f15-556">Pattern</span></span>

<span data-ttu-id="77f15-557">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="77f15-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="77f15-558">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="77f15-558">Seven digits</span></span>
    
- <span data-ttu-id="77f15-559">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="77f15-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="77f15-560">제외</span><span class="sxs-lookup"><span data-stu-id="77f15-560">Checksum</span></span>

<span data-ttu-id="77f15-561">해당 사항 없음</span><span class="sxs-lookup"><span data-stu-id="77f15-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="77f15-562">정의</span><span class="sxs-lookup"><span data-stu-id="77f15-562">Definition</span></span>

<span data-ttu-id="77f15-563">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="77f15-564">정규식이 해당 `Regex_spain_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="77f15-565">From `Keywords_spain_eu_national_id_card"` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="77f15-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="77f15-566">키워드</span><span class="sxs-lookup"><span data-stu-id="77f15-566">Keywords</span></span>

#### <a name="keywords_spain_eu_national_id_card"></a><span data-ttu-id="77f15-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="77f15-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="77f15-568">dni</span><span class="sxs-lookup"><span data-stu-id="77f15-568">dni</span></span>
  
<span data-ttu-id="77f15-569">national identification number</span><span class="sxs-lookup"><span data-stu-id="77f15-569">national identification number</span></span>
  
<span data-ttu-id="77f15-570">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-570">national identity number</span></span>
  
<span data-ttu-id="77f15-571">보험 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-571">insurance number</span></span>
  
<span data-ttu-id="77f15-572">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-572">personal identification number</span></span>
  
<span data-ttu-id="77f15-573">국가 id</span><span class="sxs-lookup"><span data-stu-id="77f15-573">national identity</span></span>
  
<span data-ttu-id="77f15-574">개인 id 없음</span><span class="sxs-lookup"><span data-stu-id="77f15-574">personal identity no</span></span>
  
<span data-ttu-id="77f15-575">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="77f15-575">unique identity number</span></span>
  
<span data-ttu-id="77f15-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="77f15-576">nationalidno#</span></span>
  
<span data-ttu-id="77f15-577">uniqueid #</span><span class="sxs-lookup"><span data-stu-id="77f15-577">uniqueid#</span></span>
  
<span data-ttu-id="77f15-578">dni #</span><span class="sxs-lookup"><span data-stu-id="77f15-578">dni#</span></span>
  
<span data-ttu-id="77f15-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="77f15-579">nationalid#</span></span>
  
<span data-ttu-id="77f15-580">nie #</span><span class="sxs-lookup"><span data-stu-id="77f15-580">nie#</span></span>
  
<span data-ttu-id="77f15-581">nie</span><span class="sxs-lookup"><span data-stu-id="77f15-581">nie</span></span>
  
<span data-ttu-id="77f15-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="77f15-582">nienúmero#</span></span>
  
<span data-ttu-id="77f15-583">nie número</span><span class="sxs-lookup"><span data-stu-id="77f15-583">nie número</span></span>
  
<span data-ttu-id="77f15-584">documento nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="77f15-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="77f15-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="77f15-585">identidad único</span></span>
  
<span data-ttu-id="77f15-586">número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="77f15-586">número nacional identidad</span></span>
  
<span data-ttu-id="77f15-587">dni número</span><span class="sxs-lookup"><span data-stu-id="77f15-587">dni número</span></span>
  
<span data-ttu-id="77f15-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="77f15-588">dninúmero#</span></span>
  
<span data-ttu-id="77f15-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="77f15-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="77f15-590">스웨덴</span><span class="sxs-lookup"><span data-stu-id="77f15-590">Sweden</span></span>

<span data-ttu-id="77f15-591">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스웨덴 국가 ID" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="77f15-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77f15-592">참고 항목</span><span class="sxs-lookup"><span data-stu-id="77f15-592">See also</span></span>

[<span data-ttu-id="77f15-593">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="77f15-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

