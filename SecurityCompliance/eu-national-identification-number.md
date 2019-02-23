---
title: EU 국가 식별 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 국가 식별 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: 9a85fd6954f39de348874e03268a2e19ae47366c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220638"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="ddde2-104">EU 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-104">EU National Identification Number</span></span>

<span data-ttu-id="ddde2-p102">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 국가 식별 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="ddde2-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="ddde2-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-108">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-108">Format</span></span>

<span data-ttu-id="ddde2-109">문자, 숫자 및 특수 문자의 24 자 조합</span><span class="sxs-lookup"><span data-stu-id="ddde2-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-110">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-110">Pattern</span></span>

<span data-ttu-id="ddde2-111">24 문자:</span><span class="sxs-lookup"><span data-stu-id="ddde2-111">24 characters:</span></span>
  
-  <span data-ttu-id="ddde2-112">22 개 문자 (대/소문자 구분 안 함), 숫자, 백슬래시, 슬래시 또는 더하기 기호</span><span class="sxs-lookup"><span data-stu-id="ddde2-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="ddde2-113">2 개의 문자 (대/소문자 구분 안 함), 숫자, 백슬래시, 슬래시, 더하기 기호 또는 등호</span><span class="sxs-lookup"><span data-stu-id="ddde2-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-114">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-114">Checksum</span></span>

<span data-ttu-id="ddde2-115">해당 없음</span><span class="sxs-lookup"><span data-stu-id="ddde2-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-116">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-116">Definition</span></span>

<span data-ttu-id="ddde2-117">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-118">정규식이 해당 `Regex_austria_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-119">from `Keywords_austria_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ddde2-120">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="ddde2-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-122">오스트리아 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-122">austrian identity number</span></span>
  
<span data-ttu-id="ddde2-123">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-123">national identity number</span></span>
  
<span data-ttu-id="ddde2-124">id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-124">identity number</span></span>
  
<span data-ttu-id="ddde2-125">
national id</span><span class="sxs-lookup"><span data-stu-id="ddde2-125">national id</span></span>
  
<span data-ttu-id="ddde2-126">personalausweis republik österreich</span><span class="sxs-lookup"><span data-stu-id="ddde2-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="ddde2-127">벨기에</span><span class="sxs-lookup"><span data-stu-id="ddde2-127">Belgium</span></span>

<span data-ttu-id="ddde2-128">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"벨기에 국가 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="ddde2-129">불가리아</span><span class="sxs-lookup"><span data-stu-id="ddde2-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-130">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-130">Format</span></span>

<span data-ttu-id="ddde2-131">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-132">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-132">Pattern</span></span>

<span data-ttu-id="ddde2-133">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="ddde2-134">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="ddde2-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="ddde2-135">출생 순서에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="ddde2-136">성별에 해당 하는 1 자리 숫자와이에 해당 하는 짝수 자리 숫자 및 암의 홀수 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="ddde2-137">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-138">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-138">Checksum</span></span>

<span data-ttu-id="ddde2-139">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-140">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-140">Definition</span></span>

<span data-ttu-id="ddde2-141">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-142">이 함수 `Func_bulgaria_national_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-143">from `Keywords_bulgaria_national_number` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="ddde2-144">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-145">이 함수 `Func_bulgaria_national_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-146">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="ddde2-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="ddde2-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="ddde2-148">egn</span><span class="sxs-lookup"><span data-stu-id="ddde2-148">egn</span></span>
  
<span data-ttu-id="ddde2-149">egn #</span><span class="sxs-lookup"><span data-stu-id="ddde2-149">egn#</span></span>
  
<span data-ttu-id="ddde2-150">불가리아어 국가 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-150">bulgarian national number</span></span>
  
<span data-ttu-id="ddde2-151">국가 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-151">national number</span></span>
  
<span data-ttu-id="ddde2-152">social security number
</span><span class="sxs-lookup"><span data-stu-id="ddde2-152">social security number</span></span>
  
<span data-ttu-id="ddde2-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="ddde2-153">nationalnumber#</span></span>
  
<span data-ttu-id="ddde2-154">ssn</span><span class="sxs-lookup"><span data-stu-id="ddde2-154">ssn#</span></span>
  
<span data-ttu-id="ddde2-155">ssn</span><span class="sxs-lookup"><span data-stu-id="ddde2-155">ssn</span></span>
  
<span data-ttu-id="ddde2-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="ddde2-156">nationalnumber</span></span>
  
<span data-ttu-id="ddde2-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="ddde2-157">bnn#</span></span>
  
<span data-ttu-id="ddde2-158">bnn</span><span class="sxs-lookup"><span data-stu-id="ddde2-158">bnn</span></span>
  
<span data-ttu-id="ddde2-159">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-159">personal id number</span></span>
  
<span data-ttu-id="ddde2-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="ddde2-160">personalidnumber#</span></span>
  
<span data-ttu-id="ddde2-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="ddde2-161">единен граждански номер</span></span>
  
<span data-ttu-id="ddde2-162">edinen grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="ddde2-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="ddde2-163">егн</span><span class="sxs-lookup"><span data-stu-id="ddde2-163">егн</span></span>
  
<span data-ttu-id="ddde2-164">егн #</span><span class="sxs-lookup"><span data-stu-id="ddde2-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="ddde2-165">크로아티아</span><span class="sxs-lookup"><span data-stu-id="ddde2-165">Croatia</span></span>

<span data-ttu-id="ddde2-166">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"크로아티아 id 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="ddde2-167">키프로스</span><span class="sxs-lookup"><span data-stu-id="ddde2-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-168">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-168">Format</span></span>

<span data-ttu-id="ddde2-169">공백과 구분 기호가 없는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-170">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-170">Pattern</span></span>

 <span data-ttu-id="ddde2-171">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="ddde2-172">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-172">Checksum</span></span>

<span data-ttu-id="ddde2-173">해당 없음</span><span class="sxs-lookup"><span data-stu-id="ddde2-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-174">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-174">Definition</span></span>

<span data-ttu-id="ddde2-175">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-176">정규식이 해당 `Regex_cyprus_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-177">from `Keywords_cyprus_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ddde2-178">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="ddde2-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-180">id 카드 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-180">id card number</span></span>
  
<span data-ttu-id="ddde2-181">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-181">national identification number</span></span>
  
<span data-ttu-id="ddde2-182">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-182">personal id number</span></span>
  
<span data-ttu-id="ddde2-183">id 카드 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-183">identity card number</span></span>
  
<span data-ttu-id="ddde2-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="ddde2-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="ddde2-185">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="ddde2-185">Czech Republic</span></span>

<span data-ttu-id="ddde2-186">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"체코어 국내 id 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="ddde2-187">덴마크</span><span class="sxs-lookup"><span data-stu-id="ddde2-187">Denmark</span></span>

<span data-ttu-id="ddde2-188">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"덴마크 개인 식별 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="ddde2-189">에스토니아</span><span class="sxs-lookup"><span data-stu-id="ddde2-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-190">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-190">Format</span></span>

<span data-ttu-id="ddde2-191">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-192">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-192">Pattern</span></span>

<span data-ttu-id="ddde2-193">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="ddde2-193">11 digits:</span></span>
  
- <span data-ttu-id="ddde2-194">출생의 성별 및 세기에 해당 하는 1 자리 숫자 (예: 암, 수, 19th 세기, 3-4:20th 세기, 5-6 = 21 세기)</span><span class="sxs-lookup"><span data-stu-id="ddde2-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="ddde2-195">출생 날짜에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="ddde2-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="ddde2-196">같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="ddde2-197">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-198">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-198">Checksum</span></span>

<span data-ttu-id="ddde2-199">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-200">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-200">Definition</span></span>

<span data-ttu-id="ddde2-201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-202">이 함수 `Func_estonia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-203">from `Keywords_estonia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-204">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-205">이 함수 `Func_estonia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-206">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="ddde2-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-208">개인 식별 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-208">personal identification code</span></span>
  
<span data-ttu-id="ddde2-209">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-209">personal identification number</span></span>
  
<span data-ttu-id="ddde2-210">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-210">national identification number</span></span>
  
<span data-ttu-id="ddde2-211">국가 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-211">national number</span></span>
  
<span data-ttu-id="ddde2-212">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-212">personal id number</span></span>
  
<span data-ttu-id="ddde2-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="ddde2-213">personalidnumber#</span></span>
  
<span data-ttu-id="ddde2-214">ik</span><span class="sxs-lookup"><span data-stu-id="ddde2-214">ik</span></span>
  
<span data-ttu-id="ddde2-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="ddde2-215">isikukood</span></span>
  
<span data-ttu-id="ddde2-216">id-kaart</span><span class="sxs-lookup"><span data-stu-id="ddde2-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="ddde2-217">핀란드</span><span class="sxs-lookup"><span data-stu-id="ddde2-217">Finland</span></span>

<span data-ttu-id="ddde2-218">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"핀란드 국가 ID" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="ddde2-219">프랑스</span><span class="sxs-lookup"><span data-stu-id="ddde2-219">France</span></span>

<span data-ttu-id="ddde2-220">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 국가 ID 카드 (cni)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="ddde2-221">독일</span><span class="sxs-lookup"><span data-stu-id="ddde2-221">Germany</span></span>

<span data-ttu-id="ddde2-222">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 id 카드 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="ddde2-223">그리스</span><span class="sxs-lookup"><span data-stu-id="ddde2-223">Greece</span></span>

<span data-ttu-id="ddde2-224">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"그리스 국가 ID 카드" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="ddde2-225">헝가리</span><span class="sxs-lookup"><span data-stu-id="ddde2-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-226">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-226">Format</span></span>

<span data-ttu-id="ddde2-227">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-228">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-228">Pattern</span></span>

<span data-ttu-id="ddde2-229">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="ddde2-229">11 digits:</span></span>
  
-  <span data-ttu-id="ddde2-230">성별에 해당 하는 1 자리 숫자 (1gb, 2 암, 기타 번호는 두 개를 포함 하는 경우에만 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="ddde2-231">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="ddde2-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="ddde2-232">일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="ddde2-233">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-234">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-234">Checksum</span></span>

<span data-ttu-id="ddde2-235">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-236">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-236">Definition</span></span>

<span data-ttu-id="ddde2-237">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-238">이 함수 `Func_hungary_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-239">from `Keywords_hungary_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-240">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-241">이 함수 `Func_hungary_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-242">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="ddde2-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-244">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-244">personal identification number</span></span>
  
<span data-ttu-id="ddde2-245">identification number
</span><span class="sxs-lookup"><span data-stu-id="ddde2-245">identification number</span></span>
  
<span data-ttu-id="ddde2-246">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-246">personal id number</span></span>
  
<span data-ttu-id="ddde2-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="ddde2-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="ddde2-248">Ireland</span><span class="sxs-lookup"><span data-stu-id="ddde2-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-249">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-249">Format</span></span>

<span data-ttu-id="ddde2-250">지정 된 패턴에서 문자, 숫자 및 공백의 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="ddde2-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-251">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-251">Pattern</span></span>

<span data-ttu-id="ddde2-252">지정 된 패턴에서 문자, 숫자 및 공백의 9 자 조합</span><span class="sxs-lookup"><span data-stu-id="ddde2-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="ddde2-253">01 년 1 월 2013 일 현재 위치:</span><span class="sxs-lookup"><span data-stu-id="ddde2-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="ddde2-254">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-254">Seven digits</span></span> 
    
- <span data-ttu-id="ddde2-255">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-255">One check digit</span></span>
    
- <span data-ttu-id="ddde2-256">1 개의 공백 또는 대문자 "W" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="ddde2-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="ddde2-257">01 년 1 월 2013 일 이전:</span><span class="sxs-lookup"><span data-stu-id="ddde2-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="ddde2-258">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-258">Seven digits</span></span> 
    
- <span data-ttu-id="ddde2-259">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-259">One check digit</span></span>
    
- <span data-ttu-id="ddde2-260">1 개의 공백 또는 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="ddde2-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-261">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-261">Checksum</span></span>

<span data-ttu-id="ddde2-262">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-263">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-263">Definition</span></span>

<span data-ttu-id="ddde2-264">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-265">이 함수는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="ddde2-266">from 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-266">A keyword from is found.</span></span>
    
<span data-ttu-id="ddde2-267">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-268">이 함수는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-269">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="ddde2-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-271">개인 공용 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-271">personal public service number</span></span>
  
<span data-ttu-id="ddde2-272">pps 아니요</span><span class="sxs-lookup"><span data-stu-id="ddde2-272">pps no</span></span>
  
<span data-ttu-id="ddde2-273">수입 및 주민 등록 보험 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="ddde2-274">rsi 아니요</span><span class="sxs-lookup"><span data-stu-id="ddde2-274">rsi no</span></span>
  
<span data-ttu-id="ddde2-275">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-275">personal identification number</span></span>
  
<span data-ttu-id="ddde2-276">identification number
</span><span class="sxs-lookup"><span data-stu-id="ddde2-276">identification number</span></span>
  
<span data-ttu-id="ddde2-277">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-277">personal id number</span></span>
  
<span data-ttu-id="ddde2-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="ddde2-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="ddde2-p103">uimh psp</span><span class="sxs-lookup"><span data-stu-id="ddde2-p103">uimh. psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="ddde2-281">이탈리아</span><span class="sxs-lookup"><span data-stu-id="ddde2-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-282">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-282">Format</span></span>

<span data-ttu-id="ddde2-283">지정 된 패턴에 해당 하는 문자 및 숫자의 16 자 조합</span><span class="sxs-lookup"><span data-stu-id="ddde2-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-284">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-284">Pattern</span></span>

<span data-ttu-id="ddde2-285">문자와 숫자의 16 자 조합:</span><span class="sxs-lookup"><span data-stu-id="ddde2-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="ddde2-286">가족 이름에서 처음 세 개의 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="ddde2-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="ddde2-287">이름의 첫 번째, 세 번째 및 네 번째 자음에 해당 하는 3 개의 문자</span><span class="sxs-lookup"><span data-stu-id="ddde2-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="ddde2-288">출생 연도의 마지막 자리에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="ddde2-289">출생 월의 문자에 해당 하는 한 문자는 알파벳 순서로 사용 되지만 1 ~ E, H, L, M, P, r에 해당 하는 문자를 사용 하는 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="ddde2-290">genders를 구분 하기 위해 출생 달의 날짜에 해당 하는 2 자리 숫자 (40)가 여성 생년월일에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="ddde2-291">사용자가 태어난 municipality 관련 지역 번호에 해당 하는 4 자리 숫자 (국가 전체 코드는 외국 국가에 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="ddde2-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="ddde2-292">1 개의 패리티 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-293">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-293">Checksum</span></span>

<span data-ttu-id="ddde2-294">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-295">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-295">Definition</span></span>

<span data-ttu-id="ddde2-296">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-297">이 함수 `Func_italy_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-298">from `Keywords_italy_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-299">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-300">이 함수 `Func_italy_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-301">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="ddde2-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-303">개인 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-303">personal code</span></span>
  
<span data-ttu-id="ddde2-304">개인 코드 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-304">personal code number</span></span>
  
<span data-ttu-id="ddde2-305">개인 인증서 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-305">personal certificate number</span></span>
  
<span data-ttu-id="ddde2-306">회계 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-306">fiscal code</span></span>
  
<span data-ttu-id="ddde2-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-307">personalcodeno#</span></span>
  
<span data-ttu-id="ddde2-308">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-308">personal id number</span></span>
  
<span data-ttu-id="ddde2-309">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-309">personal id code</span></span>
  
<span data-ttu-id="ddde2-310">codice personale</span><span class="sxs-lookup"><span data-stu-id="ddde2-310">codice personale</span></span>
  
<span data-ttu-id="ddde2-311">numero certificato personale</span><span class="sxs-lookup"><span data-stu-id="ddde2-311">numero certificato personale</span></span>
  
<span data-ttu-id="ddde2-312">numero personale</span><span class="sxs-lookup"><span data-stu-id="ddde2-312">numero personale</span></span>
  
<span data-ttu-id="ddde2-313">numero id personale</span><span class="sxs-lookup"><span data-stu-id="ddde2-313">numero id personale</span></span>
  
<span data-ttu-id="ddde2-314">codice id personale</span><span class="sxs-lookup"><span data-stu-id="ddde2-314">codice id personale</span></span>
  
<span data-ttu-id="ddde2-315">codice</span><span class="sxs-lookup"><span data-stu-id="ddde2-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="ddde2-316">이탈리아</span><span class="sxs-lookup"><span data-stu-id="ddde2-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-317">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-317">Format</span></span>

<span data-ttu-id="ddde2-318">지정 된 형식의 11 자리 숫자 및 하이픈</span><span class="sxs-lookup"><span data-stu-id="ddde2-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-319">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-319">Pattern</span></span>

<span data-ttu-id="ddde2-320">11 자리 숫자와 하이픈:</span><span class="sxs-lookup"><span data-stu-id="ddde2-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="ddde2-321">생년월일에 해당 하는 6 자리 숫자 (ddmmyy)</span><span class="sxs-lookup"><span data-stu-id="ddde2-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="ddde2-322">하이픈</span><span class="sxs-lookup"><span data-stu-id="ddde2-322">A hyphen</span></span>
    
- <span data-ttu-id="ddde2-323">출생 세기에 해당 하는 1 자리 숫자 (19th 세기의 경우 "1", 21 세기의 경우 "2")</span><span class="sxs-lookup"><span data-stu-id="ddde2-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="ddde2-324">임의로 생성 되는 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-325">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-325">Checksum</span></span>

<span data-ttu-id="ddde2-326">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-327">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-327">Definition</span></span>

<span data-ttu-id="ddde2-328">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-329">이 함수 `Func_latvia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-330">from `Keywords_latvia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-331">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-332">이 함수 `Func_latvia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-333">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="ddde2-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-335">개인 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-335">personal code</span></span>
  
<span data-ttu-id="ddde2-336">개인 코드 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-336">personal code number</span></span>
  
<span data-ttu-id="ddde2-337">개인 인증서 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-337">personal certificate number</span></span>
  
<span data-ttu-id="ddde2-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-338">personalcodeno#</span></span>
  
<span data-ttu-id="ddde2-339">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-339">personal id number</span></span>
  
<span data-ttu-id="ddde2-340">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-340">personal id code</span></span>
  
<span data-ttu-id="ddde2-341">가상 사용자 kods</span><span class="sxs-lookup"><span data-stu-id="ddde2-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="ddde2-342">리투아니아</span><span class="sxs-lookup"><span data-stu-id="ddde2-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-343">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-343">Format</span></span>

<span data-ttu-id="ddde2-344">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-345">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-345">Pattern</span></span>

<span data-ttu-id="ddde2-346">공백과 구분 기호를 사용 하지 않고 11 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="ddde2-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="ddde2-347">사용자의 성별 및 출생 세기에 해당 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="ddde2-348">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="ddde2-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="ddde2-349">출생 날짜의 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="ddde2-350">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-351">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-351">Checksum</span></span>

<span data-ttu-id="ddde2-352">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-353">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-353">Definition</span></span>

<span data-ttu-id="ddde2-354">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-355">이 함수 `Func_lithuania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-356">from `Keywords_lithuania_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-357">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-358">이 함수 `Func_lithuania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-359">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="ddde2-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-361">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-361">personal numeric code</span></span>
  
<span data-ttu-id="ddde2-362">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-362">unique identification number</span></span>
  
<span data-ttu-id="ddde2-363">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-363">citizen service number</span></span>
  
<span data-ttu-id="ddde2-364">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-364">unique identity number</span></span>
  
<span data-ttu-id="ddde2-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="ddde2-366">개인 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-366">personal code.</span></span>
  
<span data-ttu-id="ddde2-367">as메이 inis kodas</span><span class="sxs-lookup"><span data-stu-id="ddde2-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="ddde2-368">unikalus identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="ddde2-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="ddde2-369">piliečio paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="ddde2-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="ddde2-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="ddde2-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="ddde2-371">asmens kodas</span><span class="sxs-lookup"><span data-stu-id="ddde2-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="ddde2-372">셈</span><span class="sxs-lookup"><span data-stu-id="ddde2-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-373">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-373">Format</span></span>

<span data-ttu-id="ddde2-374">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-375">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-375">Pattern</span></span>

<span data-ttu-id="ddde2-376">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-376">11 digits</span></span>
  
- <span data-ttu-id="ddde2-377">사용자의 성별 및 출생 세기에 해당 하는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="ddde2-378">생년월일에 해당 하는 6 자리 숫자 (YYMMDD)</span><span class="sxs-lookup"><span data-stu-id="ddde2-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="ddde2-379">출생 날짜의 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="ddde2-380">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-381">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-381">Checksum</span></span>

<span data-ttu-id="ddde2-382">해당 없음</span><span class="sxs-lookup"><span data-stu-id="ddde2-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-383">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-383">Definition</span></span>

<span data-ttu-id="ddde2-384">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-385">정규식이 해당 `Regex_luxemburg_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-386">from `Keywords_luxemburg_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ddde2-387">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="ddde2-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-389">개인 id</span><span class="sxs-lookup"><span data-stu-id="ddde2-389">personal id</span></span>
  
<span data-ttu-id="ddde2-390">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-390">personal id number</span></span>
  
<span data-ttu-id="ddde2-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-391">personalidno#</span></span>
  
<span data-ttu-id="ddde2-392">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-392">unique id number</span></span>
  
<span data-ttu-id="ddde2-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="ddde2-393">personalidnumber#</span></span>
  
<span data-ttu-id="ddde2-394">고유 id 키</span><span class="sxs-lookup"><span data-stu-id="ddde2-394">unique id key</span></span>
  
<span data-ttu-id="ddde2-395">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-395">personal id code</span></span>
  
<span data-ttu-id="ddde2-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="ddde2-396">uniqueidkey#</span></span>
  
<span data-ttu-id="ddde2-397">개별 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-397">individual code</span></span>
  
<span data-ttu-id="ddde2-398">개별 id</span><span class="sxs-lookup"><span data-stu-id="ddde2-398">individual id</span></span>
  
<span data-ttu-id="ddde2-399">eindeutige id-nummer</span><span class="sxs-lookup"><span data-stu-id="ddde2-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="ddde2-400">eindeutige id</span><span class="sxs-lookup"><span data-stu-id="ddde2-400">eindeutige id</span></span>
  
<span data-ttu-id="ddde2-401">id personnelle</span><span class="sxs-lookup"><span data-stu-id="ddde2-401">id personnelle</span></span>
  
<span data-ttu-id="ddde2-402">numéro d'identification 담당자</span><span class="sxs-lookup"><span data-stu-id="ddde2-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="ddde2-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="ddde2-403">idpersonnelle#</span></span>
  
<span data-ttu-id="ddde2-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="ddde2-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="ddde2-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="ddde2-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="ddde2-406">몰타</span><span class="sxs-lookup"><span data-stu-id="ddde2-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-407">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-407">Format</span></span>

<span data-ttu-id="ddde2-408">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-409">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-409">Pattern</span></span>

<span data-ttu-id="ddde2-410">7 자리 숫자와 문자 1 개:</span><span class="sxs-lookup"><span data-stu-id="ddde2-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="ddde2-411">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-411">Seven digits</span></span> 
    
- <span data-ttu-id="ddde2-412">대문자 1 개 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="ddde2-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-413">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-413">Checksum</span></span>

<span data-ttu-id="ddde2-414">해당 없음</span><span class="sxs-lookup"><span data-stu-id="ddde2-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-415">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-415">Definition</span></span>

<span data-ttu-id="ddde2-416">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-417">정규식이 해당 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-418">from `Keywords_malta_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-419">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-420">정규식이 해당 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-421">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="ddde2-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-423">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-423">personal numeric code</span></span>
  
<span data-ttu-id="ddde2-424">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-424">unique identification number</span></span>
  
<span data-ttu-id="ddde2-425">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-425">citizen service number</span></span>
  
<span data-ttu-id="ddde2-426">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-426">unique identity number</span></span>
  
<span data-ttu-id="ddde2-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="ddde2-428">kodiċi numerali personali</span><span class="sxs-lookup"><span data-stu-id="ddde2-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="ddde2-429">numru ta ' uniku</span><span class="sxs-lookup"><span data-stu-id="ddde2-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="ddde2-430">numru taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="ddde2-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="ddde2-431">numru ta ' uniku</span><span class="sxs-lookup"><span data-stu-id="ddde2-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="ddde2-432">네덜란드</span><span class="sxs-lookup"><span data-stu-id="ddde2-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-433">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-433">Format</span></span>

<span data-ttu-id="ddde2-434">공백이 나 구분 기호가 없는 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-435">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-435">Pattern</span></span>

<span data-ttu-id="ddde2-436">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ddde2-437">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-437">Checksum</span></span>

<span data-ttu-id="ddde2-438">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-439">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-439">Definition</span></span>

<span data-ttu-id="ddde2-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-441">이 함수 `Func_netherlands_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-442">from 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-442">A keyword from is found.</span></span>
    
<span data-ttu-id="ddde2-443">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-444">이 함수 `Func_netherlands_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-445">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="ddde2-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-447">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-447">personal numeric code</span></span>
  
<span data-ttu-id="ddde2-448">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-448">unique identification number</span></span>
  
<span data-ttu-id="ddde2-449">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-449">citizen service number</span></span>
  
<span data-ttu-id="ddde2-450">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-450">unique identity number</span></span>
  
<span data-ttu-id="ddde2-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="ddde2-452">bsn</span><span class="sxs-lookup"><span data-stu-id="ddde2-452">bsn</span></span>
  
<span data-ttu-id="ddde2-453">bsn</span><span class="sxs-lookup"><span data-stu-id="ddde2-453">bsn#</span></span>
  
<span data-ttu-id="ddde2-454">persoonlijke 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="ddde2-455">identificatienummer</span><span class="sxs-lookup"><span data-stu-id="ddde2-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="ddde2-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="ddde2-456">burgerservicenummer</span></span>
  
<span data-ttu-id="ddde2-457">identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="ddde2-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="ddde2-458">폴란드</span><span class="sxs-lookup"><span data-stu-id="ddde2-458">Poland</span></span>

<span data-ttu-id="ddde2-459">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"폴란드 국가 ID (PESEL)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="ddde2-460">포르투갈</span><span class="sxs-lookup"><span data-stu-id="ddde2-460">Portugal</span></span>

<span data-ttu-id="ddde2-461">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"포르투갈 시민이 카드 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="ddde2-462">루마니아</span><span class="sxs-lookup"><span data-stu-id="ddde2-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-463">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-463">Format</span></span>

<span data-ttu-id="ddde2-464">공백과 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-465">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-465">Pattern</span></span>

<span data-ttu-id="ddde2-466">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ddde2-467">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-467">Checksum</span></span>

<span data-ttu-id="ddde2-468">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-469">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-469">Definition</span></span>

<span data-ttu-id="ddde2-470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-471">이 함수 `Func_romania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-472">from `Keywords_romania_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-473">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-474">이 함수 `Func_romania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-475">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="ddde2-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-477">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-477">personal numeric code</span></span>
  
<span data-ttu-id="ddde2-478">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-478">unique identification number</span></span>
  
<span data-ttu-id="ddde2-479">cnp</span><span class="sxs-lookup"><span data-stu-id="ddde2-479">cnp</span></span>
  
<span data-ttu-id="ddde2-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="ddde2-480">cnp#</span></span>
  
<span data-ttu-id="ddde2-481">고정</span><span class="sxs-lookup"><span data-stu-id="ddde2-481">pin</span></span>
  
<span data-ttu-id="ddde2-482">pin</span><span class="sxs-lookup"><span data-stu-id="ddde2-482">pin#</span></span>
  
<span data-ttu-id="ddde2-483">보험 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-483">insurance number</span></span>
  
<span data-ttu-id="ddde2-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="ddde2-484">insurancenumber#</span></span>
  
<span data-ttu-id="ddde2-485">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-485">unique identity number</span></span>
  
<span data-ttu-id="ddde2-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="ddde2-487">cod 숫자 개인</span><span class="sxs-lookup"><span data-stu-id="ddde2-487">cod numeric personal</span></span>
  
<span data-ttu-id="ddde2-488">cod identificare personal</span><span class="sxs-lookup"><span data-stu-id="ddde2-488">cod identificare personal</span></span>
  
<span data-ttu-id="ddde2-489">cod unic identificare</span><span class="sxs-lookup"><span data-stu-id="ddde2-489">cod unic identificare</span></span>
  
<span data-ttu-id="ddde2-490">număr personal unic</span><span class="sxs-lookup"><span data-stu-id="ddde2-490">număr personal unic</span></span>
  
<span data-ttu-id="ddde2-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="ddde2-491">număr identitate</span></span>
  
<span data-ttu-id="ddde2-492">număr identificare personal</span><span class="sxs-lookup"><span data-stu-id="ddde2-492">număr identificare personal</span></span>
  
<span data-ttu-id="ddde2-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="ddde2-493">număridentitate#</span></span>
  
<span data-ttu-id="ddde2-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="ddde2-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="ddde2-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="ddde2-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="ddde2-496">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="ddde2-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-497">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-497">Format</span></span>

<span data-ttu-id="ddde2-498">백슬래시 하나를 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-499">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-499">Pattern</span></span>

<span data-ttu-id="ddde2-500">백슬래시 하나를 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="ddde2-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ddde2-501">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-501">Checksum</span></span>

<span data-ttu-id="ddde2-502">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-503">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-503">Definition</span></span>

<span data-ttu-id="ddde2-504">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-505">이 함수 `Func_slovakia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-506">from `Keywords_slovakia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-507">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-508">이 함수 `Func_slovakia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-509">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="ddde2-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-511">돌 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-511">birth number</span></span>
  
<span data-ttu-id="ddde2-512">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-512">national identification number</span></span>
  
<span data-ttu-id="ddde2-513">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-513">personal identification number</span></span>
  
<span data-ttu-id="ddde2-514">social security number
</span><span class="sxs-lookup"><span data-stu-id="ddde2-514">social security number</span></span>
  
<span data-ttu-id="ddde2-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="ddde2-515">nationalnumber#</span></span>
  
<span data-ttu-id="ddde2-516">ssn</span><span class="sxs-lookup"><span data-stu-id="ddde2-516">ssn#</span></span>
  
<span data-ttu-id="ddde2-517">ssn</span><span class="sxs-lookup"><span data-stu-id="ddde2-517">ssn</span></span>
  
<span data-ttu-id="ddde2-518">국가 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-518">national number</span></span>
  
<span data-ttu-id="ddde2-519">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-519">personal id number</span></span>
  
<span data-ttu-id="ddde2-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="ddde2-520">personalidnumber#</span></span>
  
<span data-ttu-id="ddde2-521">rč</span><span class="sxs-lookup"><span data-stu-id="ddde2-521">rč</span></span>
  
<span data-ttu-id="ddde2-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="ddde2-522">rodné číslo</span></span>
  
<span data-ttu-id="ddde2-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="ddde2-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="ddde2-524">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="ddde2-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-525">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-525">Format</span></span>

<span data-ttu-id="ddde2-526">공백이 나 구분 기호가 없는 13 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-527">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-527">Pattern</span></span>

<span data-ttu-id="ddde2-528">지정 된 패턴의 13 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="ddde2-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="ddde2-529">생년월일 (ddmmlll)에 해당 하는 7 자리 숫자 이며 "lll"은 출생 연도의 마지막 세 자리에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="ddde2-530">출생 면적에 해당 하는 2 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="ddde2-531">같은 날에 태어난 사용자의 성별 및 일련 번호 조합에 해당 하는 3 자리 숫자 (남성는 000-499, 암은 500-999)</span><span class="sxs-lookup"><span data-stu-id="ddde2-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="ddde2-532">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-533">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-533">Checksum</span></span>

<span data-ttu-id="ddde2-534">예</span><span class="sxs-lookup"><span data-stu-id="ddde2-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-535">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-535">Definition</span></span>

<span data-ttu-id="ddde2-536">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-537">이 함수 `Func_slovenia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-538">from `Keywords_slovenia_eu_national_id_card` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="ddde2-539">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-540">이 함수 `Func_slovenia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="ddde2-541">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="ddde2-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-543">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="ddde2-543">personal numeric code</span></span>
  
<span data-ttu-id="ddde2-544">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-544">unique identification number</span></span>
  
<span data-ttu-id="ddde2-545">고유 등록 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-545">unique registration number</span></span>
  
<span data-ttu-id="ddde2-546">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-546">unique identity number</span></span>
  
<span data-ttu-id="ddde2-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="ddde2-548">고유 마스터 시민 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-548">unique master citizen number</span></span>
  
<span data-ttu-id="ddde2-549">ed명령이 vena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="ddde2-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="ddde2-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="ddde2-551">ed명령이 vena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="ddde2-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="ddde2-552">emšo</span><span class="sxs-lookup"><span data-stu-id="ddde2-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="ddde2-553">스페인</span><span class="sxs-lookup"><span data-stu-id="ddde2-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="ddde2-554">형식</span><span class="sxs-lookup"><span data-stu-id="ddde2-554">Format</span></span>

<span data-ttu-id="ddde2-555">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ddde2-556">패턴</span><span class="sxs-lookup"><span data-stu-id="ddde2-556">Pattern</span></span>

<span data-ttu-id="ddde2-557">7 자리 숫자와 문자 1 개</span><span class="sxs-lookup"><span data-stu-id="ddde2-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="ddde2-558">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="ddde2-558">Seven digits</span></span>
    
- <span data-ttu-id="ddde2-559">1 자리 숫자 또는 문자 (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="ddde2-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ddde2-560">체크섬</span><span class="sxs-lookup"><span data-stu-id="ddde2-560">Checksum</span></span>

<span data-ttu-id="ddde2-561">해당 없음</span><span class="sxs-lookup"><span data-stu-id="ddde2-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="ddde2-562">정의</span><span class="sxs-lookup"><span data-stu-id="ddde2-562">Definition</span></span>

<span data-ttu-id="ddde2-563">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ddde2-564">정규식이 해당 `Regex_spain_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ddde2-565">from `Keywords_spain_eu_national_id_card"` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="ddde2-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ddde2-566">키워드</span><span class="sxs-lookup"><span data-stu-id="ddde2-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="ddde2-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="ddde2-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="ddde2-568">dni</span><span class="sxs-lookup"><span data-stu-id="ddde2-568">dni</span></span>
  
<span data-ttu-id="ddde2-569">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-569">national identification number</span></span>
  
<span data-ttu-id="ddde2-570">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-570">national identity number</span></span>
  
<span data-ttu-id="ddde2-571">보험 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-571">insurance number</span></span>
  
<span data-ttu-id="ddde2-572">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-572">personal identification number</span></span>
  
<span data-ttu-id="ddde2-573">국가 id</span><span class="sxs-lookup"><span data-stu-id="ddde2-573">national identity</span></span>
  
<span data-ttu-id="ddde2-574">개인 id 없음</span><span class="sxs-lookup"><span data-stu-id="ddde2-574">personal identity no</span></span>
  
<span data-ttu-id="ddde2-575">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="ddde2-575">unique identity number</span></span>
  
<span data-ttu-id="ddde2-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="ddde2-576">nationalidno#</span></span>
  
<span data-ttu-id="ddde2-577">uniqueid</span><span class="sxs-lookup"><span data-stu-id="ddde2-577">uniqueid#</span></span>
  
<span data-ttu-id="ddde2-578">dni</span><span class="sxs-lookup"><span data-stu-id="ddde2-578">dni#</span></span>
  
<span data-ttu-id="ddde2-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="ddde2-579">nationalid#</span></span>
  
<span data-ttu-id="ddde2-580">nie #</span><span class="sxs-lookup"><span data-stu-id="ddde2-580">nie#</span></span>
  
<span data-ttu-id="ddde2-581">nie</span><span class="sxs-lookup"><span data-stu-id="ddde2-581">nie</span></span>
  
<span data-ttu-id="ddde2-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="ddde2-582">nienúmero#</span></span>
  
<span data-ttu-id="ddde2-583">nie número</span><span class="sxs-lookup"><span data-stu-id="ddde2-583">nie número</span></span>
  
<span data-ttu-id="ddde2-584">documento nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="ddde2-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="ddde2-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="ddde2-585">identidad único</span></span>
  
<span data-ttu-id="ddde2-586">número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="ddde2-586">número nacional identidad</span></span>
  
<span data-ttu-id="ddde2-587">dni número</span><span class="sxs-lookup"><span data-stu-id="ddde2-587">dni número</span></span>
  
<span data-ttu-id="ddde2-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="ddde2-588">dninúmero#</span></span>
  
<span data-ttu-id="ddde2-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="ddde2-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="ddde2-590">스웨덴</span><span class="sxs-lookup"><span data-stu-id="ddde2-590">Sweden</span></span>

<span data-ttu-id="ddde2-591">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스웨덴 국가 ID" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ddde2-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ddde2-592">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ddde2-592">See also</span></span>

[<span data-ttu-id="ddde2-593">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="ddde2-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

