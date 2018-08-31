---
title: EU 국가 Id 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: 이 항목에서는 EU 국가 Id 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533439"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="81395-104">EU 국가 Id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-104">EU National Identification Number</span></span>

<span data-ttu-id="81395-p102">이 항목에서는 EU 국가 Id 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="81395-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="81395-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="81395-108">형식</span><span class="sxs-lookup"><span data-stu-id="81395-108">Format</span></span>

<span data-ttu-id="81395-109">문자, 숫자 및 특수 문자는 24 문자 조합</span><span class="sxs-lookup"><span data-stu-id="81395-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-110">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-110">Pattern</span></span>

<span data-ttu-id="81395-111">24 문자 수:</span><span class="sxs-lookup"><span data-stu-id="81395-111">24 characters:</span></span>
  
-  <span data-ttu-id="81395-112">22 문자 (대 소문자 구분 안함), 숫자, 백슬래시, 슬래시, 또는 더하기 기호</span><span class="sxs-lookup"><span data-stu-id="81395-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="81395-113">두 문자 (대 소문자 구분 안함), 숫자, 백슬래시, 슬래시, 더하기 기호 또는 등호</span><span class="sxs-lookup"><span data-stu-id="81395-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-114">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-114">Checksum</span></span>

<span data-ttu-id="81395-115">해당 없음</span><span class="sxs-lookup"><span data-stu-id="81395-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-116">정의</span><span class="sxs-lookup"><span data-stu-id="81395-116">Definition</span></span>

<span data-ttu-id="81395-117">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-118">정규식 `Regex_austria_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-119">키워드에서 `Keywords_austria_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="81395-120">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="81395-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="81395-122">오스트리아 identity 번호</span><span class="sxs-lookup"><span data-stu-id="81395-122">austrian identity number</span></span>
  
<span data-ttu-id="81395-123">identity 국가 번호</span><span class="sxs-lookup"><span data-stu-id="81395-123">national identity number</span></span>
  
<span data-ttu-id="81395-124">identity 번호</span><span class="sxs-lookup"><span data-stu-id="81395-124">identity number</span></span>
  
<span data-ttu-id="81395-125">
national id</span><span class="sxs-lookup"><span data-stu-id="81395-125">national id</span></span>
  
<span data-ttu-id="81395-126">personalausweis republik österreich</span><span class="sxs-lookup"><span data-stu-id="81395-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="81395-127">벨기에</span><span class="sxs-lookup"><span data-stu-id="81395-127">Belgium</span></span>

<span data-ttu-id="81395-128">자세한 내용은의 섹션을 참조 "벨기에 국가 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="81395-129">불가리아</span><span class="sxs-lookup"><span data-stu-id="81395-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="81395-130">형식</span><span class="sxs-lookup"><span data-stu-id="81395-130">Format</span></span>

<span data-ttu-id="81395-131">공백 및 구분 기호 없이 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-132">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-132">Pattern</span></span>

<span data-ttu-id="81395-133">공백 및 구분 기호 없이 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="81395-134">생일 (YYMMDD)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="81395-135">생일 축에 해당 하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="81395-136">성별에 해당 하는 한 자리 숫자: 1 여자 2 남자 및 탑재에 대 한 홀수 짝수 숫자로</span><span class="sxs-lookup"><span data-stu-id="81395-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="81395-137">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-138">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-138">Checksum</span></span>

<span data-ttu-id="81395-139">예</span><span class="sxs-lookup"><span data-stu-id="81395-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-140">정의</span><span class="sxs-lookup"><span data-stu-id="81395-140">Definition</span></span>

<span data-ttu-id="81395-141">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-142">다음은 함수 `Func_bulgaria_national_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-143">키워드에서 `Keywords_bulgaria_national_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="81395-144">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-145">다음은 함수 `Func_bulgaria_national_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-146">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="81395-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="81395-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="81395-148">egn</span><span class="sxs-lookup"><span data-stu-id="81395-148">egn</span></span>
  
<span data-ttu-id="81395-149">egn #</span><span class="sxs-lookup"><span data-stu-id="81395-149">egn#</span></span>
  
<span data-ttu-id="81395-150">불가리아어 국가 번호</span><span class="sxs-lookup"><span data-stu-id="81395-150">bulgarian national number</span></span>
  
<span data-ttu-id="81395-151">국가 번호</span><span class="sxs-lookup"><span data-stu-id="81395-151">national number</span></span>
  
<span data-ttu-id="81395-152">social security number
</span><span class="sxs-lookup"><span data-stu-id="81395-152">social security number</span></span>
  
<span data-ttu-id="81395-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="81395-153">nationalnumber#</span></span>
  
<span data-ttu-id="81395-154">ssn #</span><span class="sxs-lookup"><span data-stu-id="81395-154">ssn#</span></span>
  
<span data-ttu-id="81395-155">ssn</span><span class="sxs-lookup"><span data-stu-id="81395-155">ssn</span></span>
  
<span data-ttu-id="81395-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="81395-156">nationalnumber</span></span>
  
<span data-ttu-id="81395-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="81395-157">bnn#</span></span>
  
<span data-ttu-id="81395-158">bnn</span><span class="sxs-lookup"><span data-stu-id="81395-158">bnn</span></span>
  
<span data-ttu-id="81395-159">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-159">personal id number</span></span>
  
<span data-ttu-id="81395-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="81395-160">personalidnumber#</span></span>
  
<span data-ttu-id="81395-161">ЕДИНЕН ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="81395-161">единен граждански номер</span></span>
  
<span data-ttu-id="81395-162">edinen grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="81395-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="81395-163">ЕГН</span><span class="sxs-lookup"><span data-stu-id="81395-163">егн</span></span>
  
<span data-ttu-id="81395-164">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="81395-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="81395-165">크로아티아</span><span class="sxs-lookup"><span data-stu-id="81395-165">Croatia</span></span>

<span data-ttu-id="81395-166">자세한 내용은의 섹션을 참조 "크로아티아 Identity Number" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="81395-167">키프로스</span><span class="sxs-lookup"><span data-stu-id="81395-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="81395-168">형식</span><span class="sxs-lookup"><span data-stu-id="81395-168">Format</span></span>

<span data-ttu-id="81395-169">공백 및 구분 기호 없이 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-170">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-170">Pattern</span></span>

 <span data-ttu-id="81395-171">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="81395-172">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-172">Checksum</span></span>

<span data-ttu-id="81395-173">해당 없음</span><span class="sxs-lookup"><span data-stu-id="81395-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-174">정의</span><span class="sxs-lookup"><span data-stu-id="81395-174">Definition</span></span>

<span data-ttu-id="81395-175">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-176">정규식 `Regex_cyprus_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-177">키워드에서 `Keywords_cyprus_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="81395-178">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="81395-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="81395-180">id 카드 번호</span><span class="sxs-lookup"><span data-stu-id="81395-180">id card number</span></span>
  
<span data-ttu-id="81395-181">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-181">national identification number</span></span>
  
<span data-ttu-id="81395-182">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-182">personal id number</span></span>
  
<span data-ttu-id="81395-183">id 카드 번호</span><span class="sxs-lookup"><span data-stu-id="81395-183">identity card number</span></span>
  
<span data-ttu-id="81395-184">ΤΑΥΤΟΤΗΤΑΣ</span><span class="sxs-lookup"><span data-stu-id="81395-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="81395-185">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="81395-185">Czech Republic</span></span>

<span data-ttu-id="81395-186">자세한 내용은의 섹션을 참조 "체코어 국가 Identity Number" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="81395-187">덴마크</span><span class="sxs-lookup"><span data-stu-id="81395-187">Denmark</span></span>

<span data-ttu-id="81395-188">자세한 내용은의 섹션을 참조 "덴마크 개인 Id 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="81395-189">에스토니아</span><span class="sxs-lookup"><span data-stu-id="81395-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="81395-190">형식</span><span class="sxs-lookup"><span data-stu-id="81395-190">Format</span></span>

<span data-ttu-id="81395-191">공백 및 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-192">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-192">Pattern</span></span>

<span data-ttu-id="81395-193">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="81395-193">11 digits:</span></span>
  
- <span data-ttu-id="81395-194">성별 및 생일 세기에 해당 하는 한 자리 숫자 (홀수 번호 1 여자 2 남자, 짝수 여성; 1-2: 19 세기; 3-4: 20 세기; 5-6: 21 세기)</span><span class="sxs-lookup"><span data-stu-id="81395-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="81395-195">생일 (YYMMDD)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="81395-196">같은 날짜 태어난 장애인을 구분 하는 일련 번호에 해당 하는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="81395-197">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-198">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-198">Checksum</span></span>

<span data-ttu-id="81395-199">예</span><span class="sxs-lookup"><span data-stu-id="81395-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-200">정의</span><span class="sxs-lookup"><span data-stu-id="81395-200">Definition</span></span>

<span data-ttu-id="81395-201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-202">다음은 함수 `Func_estonia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-203">키워드에서 `Keywords_estonia_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-204">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-205">다음은 함수 `Func_estonia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-206">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="81395-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="81395-208">개인 식별 코드</span><span class="sxs-lookup"><span data-stu-id="81395-208">personal identification code</span></span>
  
<span data-ttu-id="81395-209">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="81395-209">personal identification number</span></span>
  
<span data-ttu-id="81395-210">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-210">national identification number</span></span>
  
<span data-ttu-id="81395-211">국가 번호</span><span class="sxs-lookup"><span data-stu-id="81395-211">national number</span></span>
  
<span data-ttu-id="81395-212">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-212">personal id number</span></span>
  
<span data-ttu-id="81395-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="81395-213">personalidnumber#</span></span>
  
<span data-ttu-id="81395-214">ik</span><span class="sxs-lookup"><span data-stu-id="81395-214">ik</span></span>
  
<span data-ttu-id="81395-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="81395-215">isikukood</span></span>
  
<span data-ttu-id="81395-216">id kaart</span><span class="sxs-lookup"><span data-stu-id="81395-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="81395-217">핀란드</span><span class="sxs-lookup"><span data-stu-id="81395-217">Finland</span></span>

<span data-ttu-id="81395-218">자세한 내용은의 섹션을 참조 "핀란드 국가 ID" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="81395-219">프랑스</span><span class="sxs-lookup"><span data-stu-id="81395-219">France</span></span>

<span data-ttu-id="81395-220">자세한 내용은의 섹션을 참조 "프랑스 국가 ID 카드 (CNI)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="81395-221">독일</span><span class="sxs-lookup"><span data-stu-id="81395-221">Germany</span></span>

<span data-ttu-id="81395-222">자세한 내용은의 섹션을 참조 "독일 Id 카드 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="81395-223">그리스</span><span class="sxs-lookup"><span data-stu-id="81395-223">Greece</span></span>

<span data-ttu-id="81395-224">자세한 내용은의 섹션을 참조 "그리스 국가 ID 카드" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="81395-225">헝가리</span><span class="sxs-lookup"><span data-stu-id="81395-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="81395-226">형식</span><span class="sxs-lookup"><span data-stu-id="81395-226">Format</span></span>

<span data-ttu-id="81395-227">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-228">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-228">Pattern</span></span>

<span data-ttu-id="81395-229">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="81395-229">11 digits:</span></span>
  
-  <span data-ttu-id="81395-230">성별 (1-2 남자, 2-탑재, 다른 번호는 1900 하기 전에 태어난 시민 또는 이중 참여 의식와 시민에 대 한 가능한도)에 해당 하는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="81395-231">생일 (YYMMDD)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="81395-232">일련 번호에 해당 하는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="81395-233">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-234">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-234">Checksum</span></span>

<span data-ttu-id="81395-235">예</span><span class="sxs-lookup"><span data-stu-id="81395-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-236">정의</span><span class="sxs-lookup"><span data-stu-id="81395-236">Definition</span></span>

<span data-ttu-id="81395-237">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-238">다음은 함수 `Func_hungary_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-239">키워드에서 `Keywords_hungary_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-240">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-241">다음은 함수 `Func_hungary_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-242">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="81395-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="81395-244">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="81395-244">personal identification number</span></span>
  
<span data-ttu-id="81395-245">identification number
</span><span class="sxs-lookup"><span data-stu-id="81395-245">identification number</span></span>
  
<span data-ttu-id="81395-246">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-246">personal id number</span></span>
  
<span data-ttu-id="81395-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="81395-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="81395-248">Ireland</span><span class="sxs-lookup"><span data-stu-id="81395-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="81395-249">형식</span><span class="sxs-lookup"><span data-stu-id="81395-249">Format</span></span>

<span data-ttu-id="81395-250">문자, 숫자 및 지정된 된 패턴에 포함 된 공백은 9 개 문자 조합</span><span class="sxs-lookup"><span data-stu-id="81395-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-251">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-251">Pattern</span></span>

<span data-ttu-id="81395-252">문자, 숫자 및 지정된 된 패턴에 포함 된 공백은 9 개 문자 조합</span><span class="sxs-lookup"><span data-stu-id="81395-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="81395-253">현재 2013 년 1 월 1 일에서:</span><span class="sxs-lookup"><span data-stu-id="81395-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="81395-254">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-254">Seven digits</span></span> 
    
- <span data-ttu-id="81395-255">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-255">One check digit</span></span>
    
- <span data-ttu-id="81395-256">한 칸 또는 대문자 "W" (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="81395-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="81395-257">2013 년 1 월 1 일 하기 전에:</span><span class="sxs-lookup"><span data-stu-id="81395-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="81395-258">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-258">Seven digits</span></span> 
    
- <span data-ttu-id="81395-259">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-259">One check digit</span></span>
    
- <span data-ttu-id="81395-260">한 칸 또는 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="81395-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-261">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-261">Checksum</span></span>

<span data-ttu-id="81395-262">예</span><span class="sxs-lookup"><span data-stu-id="81395-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-263">정의</span><span class="sxs-lookup"><span data-stu-id="81395-263">Definition</span></span>

<span data-ttu-id="81395-264">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-265">다음은 함수 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="81395-266">키워드에서 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81395-266">A keyword from is found.</span></span>
    
<span data-ttu-id="81395-267">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-268">다음은 함수 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="81395-269">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="81395-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="81395-271">개인 공공 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="81395-271">personal public service number</span></span>
  
<span data-ttu-id="81395-272">pps 없음</span><span class="sxs-lookup"><span data-stu-id="81395-272">pps no</span></span>
  
<span data-ttu-id="81395-273">수익 및 사회 보험 번호</span><span class="sxs-lookup"><span data-stu-id="81395-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="81395-274">rsi 없음</span><span class="sxs-lookup"><span data-stu-id="81395-274">rsi no</span></span>
  
<span data-ttu-id="81395-275">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="81395-275">personal identification number</span></span>
  
<span data-ttu-id="81395-276">identification number
</span><span class="sxs-lookup"><span data-stu-id="81395-276">identification number</span></span>
  
<span data-ttu-id="81395-277">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-277">personal id number</span></span>
  
<span data-ttu-id="81395-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="81395-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="81395-p103">uimh 합니다. psp</span><span class="sxs-lookup"><span data-stu-id="81395-p103">uimh. psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="81395-281">이탈리아</span><span class="sxs-lookup"><span data-stu-id="81395-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="81395-282">형식</span><span class="sxs-lookup"><span data-stu-id="81395-282">Format</span></span>

<span data-ttu-id="81395-283">문자와 지정한 패턴의 자릿수의 16 자리의 조합</span><span class="sxs-lookup"><span data-stu-id="81395-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-284">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-284">Pattern</span></span>

<span data-ttu-id="81395-285">문자와 숫자의 16 자리의 조합 합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="81395-286">패밀리 이름에서 처음 세 자음에 해당 하는 세 개 문자</span><span class="sxs-lookup"><span data-stu-id="81395-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="81395-287">먼저, 세번째 및 네번째에 해당 하는 세 글자로 자음 첫 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="81395-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="81395-288">마지막 생일의 연도의 숫자에 해당 하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="81395-289">달의 생일 편지에 해당 하는 하나의 문자-문자 사전순으로 사용 되지만 문자를 E, H, L, M, P, R T로 사용 됩니다 (따라서 1 월 A 이며 년 10 월 R)</span><span class="sxs-lookup"><span data-stu-id="81395-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="81395-290">생일의 월의 날짜에 해당 하는 두 자리-성별을 구별 하기 위해 40 여자 생일 요일에 추가 됩니다</span><span class="sxs-lookup"><span data-stu-id="81395-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="81395-291">사용자 출생 여기서는 지방 자치 단체에 특정 지역 번호에 해당 하는 4 자리 숫자 (국가 수준의 코드는 외국에 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="81395-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="81395-292">하나의 패리티 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-293">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-293">Checksum</span></span>

<span data-ttu-id="81395-294">예</span><span class="sxs-lookup"><span data-stu-id="81395-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-295">정의</span><span class="sxs-lookup"><span data-stu-id="81395-295">Definition</span></span>

<span data-ttu-id="81395-296">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-297">다음은 함수 `Func_italy_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-298">키워드에서 `Keywords_italy_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-299">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-300">다음은 함수 `Func_italy_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-301">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="81395-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="81395-303">개인 코드</span><span class="sxs-lookup"><span data-stu-id="81395-303">personal code</span></span>
  
<span data-ttu-id="81395-304">개인 코드 번호</span><span class="sxs-lookup"><span data-stu-id="81395-304">personal code number</span></span>
  
<span data-ttu-id="81395-305">개인 인증서 번호</span><span class="sxs-lookup"><span data-stu-id="81395-305">personal certificate number</span></span>
  
<span data-ttu-id="81395-306">회계 코드</span><span class="sxs-lookup"><span data-stu-id="81395-306">fiscal code</span></span>
  
<span data-ttu-id="81395-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="81395-307">personalcodeno#</span></span>
  
<span data-ttu-id="81395-308">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-308">personal id number</span></span>
  
<span data-ttu-id="81395-309">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="81395-309">personal id code</span></span>
  
<span data-ttu-id="81395-310">codice personale</span><span class="sxs-lookup"><span data-stu-id="81395-310">codice personale</span></span>
  
<span data-ttu-id="81395-311">numero certificato personale</span><span class="sxs-lookup"><span data-stu-id="81395-311">numero certificato personale</span></span>
  
<span data-ttu-id="81395-312">numero personale</span><span class="sxs-lookup"><span data-stu-id="81395-312">numero personale</span></span>
  
<span data-ttu-id="81395-313">numero id personale</span><span class="sxs-lookup"><span data-stu-id="81395-313">numero id personale</span></span>
  
<span data-ttu-id="81395-314">codice id personale</span><span class="sxs-lookup"><span data-stu-id="81395-314">codice id personale</span></span>
  
<span data-ttu-id="81395-315">codice fiscale</span><span class="sxs-lookup"><span data-stu-id="81395-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="81395-316">이탈리아</span><span class="sxs-lookup"><span data-stu-id="81395-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="81395-317">형식</span><span class="sxs-lookup"><span data-stu-id="81395-317">Format</span></span>

<span data-ttu-id="81395-318">11 및 지정 된 형식 하이픈</span><span class="sxs-lookup"><span data-stu-id="81395-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-319">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-319">Pattern</span></span>

<span data-ttu-id="81395-320">11 자릿수와 하이픈:</span><span class="sxs-lookup"><span data-stu-id="81395-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="81395-321">생일 (DDMMYY)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="81395-322">하이픈</span><span class="sxs-lookup"><span data-stu-id="81395-322">A hyphen</span></span>
    
- <span data-ttu-id="81395-323">(19 세기 "0", 20 세기에 대 한 "1" 및 "2" 21 세기에 대 한) 생일 세기에 해당 하는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="81395-324">임의로 생성 하는 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-325">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-325">Checksum</span></span>

<span data-ttu-id="81395-326">예</span><span class="sxs-lookup"><span data-stu-id="81395-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-327">정의</span><span class="sxs-lookup"><span data-stu-id="81395-327">Definition</span></span>

<span data-ttu-id="81395-328">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-329">다음은 함수 `Func_latvia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-330">키워드에서 `Keywords_latvia_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-331">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-332">다음은 함수 `Func_latvia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-333">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="81395-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="81395-335">개인 코드</span><span class="sxs-lookup"><span data-stu-id="81395-335">personal code</span></span>
  
<span data-ttu-id="81395-336">개인 코드 번호</span><span class="sxs-lookup"><span data-stu-id="81395-336">personal code number</span></span>
  
<span data-ttu-id="81395-337">개인 인증서 번호</span><span class="sxs-lookup"><span data-stu-id="81395-337">personal certificate number</span></span>
  
<span data-ttu-id="81395-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="81395-338">personalcodeno#</span></span>
  
<span data-ttu-id="81395-339">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-339">personal id number</span></span>
  
<span data-ttu-id="81395-340">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="81395-340">personal id code</span></span>
  
<span data-ttu-id="81395-341">사용자가 나옵니다 kods</span><span class="sxs-lookup"><span data-stu-id="81395-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="81395-342">리투아니아</span><span class="sxs-lookup"><span data-stu-id="81395-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="81395-343">형식</span><span class="sxs-lookup"><span data-stu-id="81395-343">Format</span></span>

<span data-ttu-id="81395-344">공백 및 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-345">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-345">Pattern</span></span>

<span data-ttu-id="81395-346">공백 및 구분 기호 없이 11 숫자:</span><span class="sxs-lookup"><span data-stu-id="81395-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="81395-347">사용자의 성별와 생일 세기에 해당 하는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="81395-348">생일 (YYMMDD)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="81395-349">생일의 날짜의 일련 번호에 해당 하는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="81395-350">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-351">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-351">Checksum</span></span>

<span data-ttu-id="81395-352">예</span><span class="sxs-lookup"><span data-stu-id="81395-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-353">정의</span><span class="sxs-lookup"><span data-stu-id="81395-353">Definition</span></span>

<span data-ttu-id="81395-354">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-355">다음은 함수 `Func_lithuania_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-356">키워드에서 `Keywords_lithuania_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-357">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-358">다음은 함수 `Func_lithuania_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-359">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="81395-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="81395-361">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="81395-361">personal numeric code</span></span>
  
<span data-ttu-id="81395-362">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-362">unique identification number</span></span>
  
<span data-ttu-id="81395-363">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="81395-363">citizen service number</span></span>
  
<span data-ttu-id="81395-364">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-364">unique identity number</span></span>
  
<span data-ttu-id="81395-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="81395-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="81395-366">개인 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="81395-366">personal code.</span></span>
  
<span data-ttu-id="81395-367">asmeninis skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="81395-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="81395-368">unikalus identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="81395-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="81395-369">piliečio paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="81395-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="81395-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="81395-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="81395-371">asmens kodas 합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="81395-372">룩셈부르크</span><span class="sxs-lookup"><span data-stu-id="81395-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="81395-373">형식</span><span class="sxs-lookup"><span data-stu-id="81395-373">Format</span></span>

<span data-ttu-id="81395-374">공백 및 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-375">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-375">Pattern</span></span>

<span data-ttu-id="81395-376">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-376">11 digits</span></span>
  
- <span data-ttu-id="81395-377">사용자의 성별와 생일 세기에 해당 하는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="81395-378">생일 (YYMMDD)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="81395-379">생일의 날짜의 일련 번호에 해당 하는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="81395-380">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-381">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-381">Checksum</span></span>

<span data-ttu-id="81395-382">해당 없음</span><span class="sxs-lookup"><span data-stu-id="81395-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-383">정의</span><span class="sxs-lookup"><span data-stu-id="81395-383">Definition</span></span>

<span data-ttu-id="81395-384">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-385">정규식 `Regex_luxemburg_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-386">키워드에서 `Keywords_luxemburg_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="81395-387">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="81395-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="81395-389">개인 id</span><span class="sxs-lookup"><span data-stu-id="81395-389">personal id</span></span>
  
<span data-ttu-id="81395-390">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-390">personal id number</span></span>
  
<span data-ttu-id="81395-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="81395-391">personalidno#</span></span>
  
<span data-ttu-id="81395-392">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-392">unique id number</span></span>
  
<span data-ttu-id="81395-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="81395-393">personalidnumber#</span></span>
  
<span data-ttu-id="81395-394">고유 id 키</span><span class="sxs-lookup"><span data-stu-id="81395-394">unique id key</span></span>
  
<span data-ttu-id="81395-395">개인 id 코드</span><span class="sxs-lookup"><span data-stu-id="81395-395">personal id code</span></span>
  
<span data-ttu-id="81395-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="81395-396">uniqueidkey#</span></span>
  
<span data-ttu-id="81395-397">개별 코드</span><span class="sxs-lookup"><span data-stu-id="81395-397">individual code</span></span>
  
<span data-ttu-id="81395-398">개별 id</span><span class="sxs-lookup"><span data-stu-id="81395-398">individual id</span></span>
  
<span data-ttu-id="81395-399">eindeutige id nummer</span><span class="sxs-lookup"><span data-stu-id="81395-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="81395-400">eindeutige id</span><span class="sxs-lookup"><span data-stu-id="81395-400">eindeutige id</span></span>
  
<span data-ttu-id="81395-401">id personnelle</span><span class="sxs-lookup"><span data-stu-id="81395-401">id personnelle</span></span>
  
<span data-ttu-id="81395-402">numéro d'identification 담당자</span><span class="sxs-lookup"><span data-stu-id="81395-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="81395-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="81395-403">idpersonnelle#</span></span>
  
<span data-ttu-id="81395-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="81395-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="81395-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="81395-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="81395-406">몰타</span><span class="sxs-lookup"><span data-stu-id="81395-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="81395-407">형식</span><span class="sxs-lookup"><span data-stu-id="81395-407">Format</span></span>

<span data-ttu-id="81395-408">한 문자 앞에 오는 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-409">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-409">Pattern</span></span>

<span data-ttu-id="81395-410">7 자리 숫자를 한 문자 앞에 오는:</span><span class="sxs-lookup"><span data-stu-id="81395-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="81395-411">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-411">Seven digits</span></span> 
    
- <span data-ttu-id="81395-412">하나의 대문자 (대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="81395-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-413">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-413">Checksum</span></span>

<span data-ttu-id="81395-414">해당 없음</span><span class="sxs-lookup"><span data-stu-id="81395-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-415">정의</span><span class="sxs-lookup"><span data-stu-id="81395-415">Definition</span></span>

<span data-ttu-id="81395-416">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-417">정규식 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-418">키워드에서 `Keywords_malta_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-419">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-420">정규식 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-421">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="81395-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="81395-423">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="81395-423">personal numeric code</span></span>
  
<span data-ttu-id="81395-424">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-424">unique identification number</span></span>
  
<span data-ttu-id="81395-425">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="81395-425">citizen service number</span></span>
  
<span data-ttu-id="81395-426">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-426">unique identity number</span></span>
  
<span data-ttu-id="81395-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="81395-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="81395-428">kodiċi numerali personali</span><span class="sxs-lookup"><span data-stu-id="81395-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="81395-429">numru ta ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="81395-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="81395-430">numru 게 servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="81395-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="81395-431">numru ta' identità uniku</span><span class="sxs-lookup"><span data-stu-id="81395-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="81395-432">네덜란드</span><span class="sxs-lookup"><span data-stu-id="81395-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="81395-433">형식</span><span class="sxs-lookup"><span data-stu-id="81395-433">Format</span></span>

<span data-ttu-id="81395-434">공백이 나 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="81395-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-435">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-435">Pattern</span></span>

<span data-ttu-id="81395-436">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="81395-437">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-437">Checksum</span></span>

<span data-ttu-id="81395-438">예</span><span class="sxs-lookup"><span data-stu-id="81395-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-439">정의</span><span class="sxs-lookup"><span data-stu-id="81395-439">Definition</span></span>

<span data-ttu-id="81395-440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-441">다음은 함수 `Func_netherlands_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-442">키워드에서 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81395-442">A keyword from is found.</span></span>
    
<span data-ttu-id="81395-443">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-444">다음은 함수 `Func_netherlands_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-445">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="81395-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="81395-447">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="81395-447">personal numeric code</span></span>
  
<span data-ttu-id="81395-448">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-448">unique identification number</span></span>
  
<span data-ttu-id="81395-449">시민 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="81395-449">citizen service number</span></span>
  
<span data-ttu-id="81395-450">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-450">unique identity number</span></span>
  
<span data-ttu-id="81395-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="81395-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="81395-452">bsn</span><span class="sxs-lookup"><span data-stu-id="81395-452">bsn</span></span>
  
<span data-ttu-id="81395-453">bsn #</span><span class="sxs-lookup"><span data-stu-id="81395-453">bsn#</span></span>
  
<span data-ttu-id="81395-454">persoonlijke numerieke 코드</span><span class="sxs-lookup"><span data-stu-id="81395-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="81395-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="81395-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="81395-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="81395-456">burgerservicenummer</span></span>
  
<span data-ttu-id="81395-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="81395-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="81395-458">폴란드</span><span class="sxs-lookup"><span data-stu-id="81395-458">Poland</span></span>

<span data-ttu-id="81395-459">자세한 내용은의 섹션을 참조 "폴란드 국가 ID (PESEL)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="81395-460">포르투갈</span><span class="sxs-lookup"><span data-stu-id="81395-460">Portugal</span></span>

<span data-ttu-id="81395-461">자세한 내용은의 섹션을 참조 "포르투갈 시민 카드 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="81395-462">루마니아</span><span class="sxs-lookup"><span data-stu-id="81395-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="81395-463">형식</span><span class="sxs-lookup"><span data-stu-id="81395-463">Format</span></span>

<span data-ttu-id="81395-464">공백 및 구분 기호 없이 13 자릿수</span><span class="sxs-lookup"><span data-stu-id="81395-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-465">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-465">Pattern</span></span>

<span data-ttu-id="81395-466">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="81395-467">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-467">Checksum</span></span>

<span data-ttu-id="81395-468">예</span><span class="sxs-lookup"><span data-stu-id="81395-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-469">정의</span><span class="sxs-lookup"><span data-stu-id="81395-469">Definition</span></span>

<span data-ttu-id="81395-470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-471">다음은 함수 `Func_romania_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-472">키워드에서 `Keywords_romania_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-473">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-474">다음은 함수 `Func_romania_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-475">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="81395-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="81395-477">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="81395-477">personal numeric code</span></span>
  
<span data-ttu-id="81395-478">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-478">unique identification number</span></span>
  
<span data-ttu-id="81395-479">cnp</span><span class="sxs-lookup"><span data-stu-id="81395-479">cnp</span></span>
  
<span data-ttu-id="81395-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="81395-480">cnp#</span></span>
  
<span data-ttu-id="81395-481">고정</span><span class="sxs-lookup"><span data-stu-id="81395-481">pin</span></span>
  
<span data-ttu-id="81395-482">핀 번호</span><span class="sxs-lookup"><span data-stu-id="81395-482">pin#</span></span>
  
<span data-ttu-id="81395-483">보험 번호</span><span class="sxs-lookup"><span data-stu-id="81395-483">insurance number</span></span>
  
<span data-ttu-id="81395-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="81395-484">insurancenumber#</span></span>
  
<span data-ttu-id="81395-485">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-485">unique identity number</span></span>
  
<span data-ttu-id="81395-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="81395-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="81395-487">코드 숫자 개인</span><span class="sxs-lookup"><span data-stu-id="81395-487">cod numeric personal</span></span>
  
<span data-ttu-id="81395-488">개인 identificare 대구</span><span class="sxs-lookup"><span data-stu-id="81395-488">cod identificare personal</span></span>
  
<span data-ttu-id="81395-489">코드 unic identificare</span><span class="sxs-lookup"><span data-stu-id="81395-489">cod unic identificare</span></span>
  
<span data-ttu-id="81395-490">număr 개인 unic</span><span class="sxs-lookup"><span data-stu-id="81395-490">număr personal unic</span></span>
  
<span data-ttu-id="81395-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="81395-491">număr identitate</span></span>
  
<span data-ttu-id="81395-492">개인 număr identificare</span><span class="sxs-lookup"><span data-stu-id="81395-492">număr identificare personal</span></span>
  
<span data-ttu-id="81395-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="81395-493">număridentitate#</span></span>
  
<span data-ttu-id="81395-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="81395-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="81395-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="81395-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="81395-496">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="81395-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="81395-497">형식</span><span class="sxs-lookup"><span data-stu-id="81395-497">Format</span></span>

<span data-ttu-id="81395-498">하나의 백슬래시를 포함 하는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-499">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-499">Pattern</span></span>

<span data-ttu-id="81395-500">하나의 백슬래시를 포함 하는 10 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="81395-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="81395-501">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-501">Checksum</span></span>

<span data-ttu-id="81395-502">예</span><span class="sxs-lookup"><span data-stu-id="81395-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-503">정의</span><span class="sxs-lookup"><span data-stu-id="81395-503">Definition</span></span>

<span data-ttu-id="81395-504">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-505">다음은 함수 `Func_slovakia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-506">키워드에서 `Keywords_slovakia_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-507">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-508">다음은 함수 `Func_slovakia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-509">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="81395-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="81395-511">생일 번호</span><span class="sxs-lookup"><span data-stu-id="81395-511">birth number</span></span>
  
<span data-ttu-id="81395-512">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-512">national identification number</span></span>
  
<span data-ttu-id="81395-513">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="81395-513">personal identification number</span></span>
  
<span data-ttu-id="81395-514">social security number
</span><span class="sxs-lookup"><span data-stu-id="81395-514">social security number</span></span>
  
<span data-ttu-id="81395-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="81395-515">nationalnumber#</span></span>
  
<span data-ttu-id="81395-516">ssn #</span><span class="sxs-lookup"><span data-stu-id="81395-516">ssn#</span></span>
  
<span data-ttu-id="81395-517">ssn</span><span class="sxs-lookup"><span data-stu-id="81395-517">ssn</span></span>
  
<span data-ttu-id="81395-518">국가 번호</span><span class="sxs-lookup"><span data-stu-id="81395-518">national number</span></span>
  
<span data-ttu-id="81395-519">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-519">personal id number</span></span>
  
<span data-ttu-id="81395-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="81395-520">personalidnumber#</span></span>
  
<span data-ttu-id="81395-521">rč</span><span class="sxs-lookup"><span data-stu-id="81395-521">rč</span></span>
  
<span data-ttu-id="81395-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="81395-522">rodné číslo</span></span>
  
<span data-ttu-id="81395-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="81395-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="81395-524">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="81395-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="81395-525">형식</span><span class="sxs-lookup"><span data-stu-id="81395-525">Format</span></span>

<span data-ttu-id="81395-526">공백이 나 구분 기호 없이 13 자릿수</span><span class="sxs-lookup"><span data-stu-id="81395-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-527">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-527">Pattern</span></span>

<span data-ttu-id="81395-528">지정된 된 패턴의 자릿수 13:</span><span class="sxs-lookup"><span data-stu-id="81395-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="81395-529">"LLL" 해당 생일의 연도의 세 자리 마지막 생일 (DDMMLLL)에 해당 하는 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="81395-530">생일의 영역에 해당 하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="81395-531">성별 및 일련 번호의 조합에 해당 하는 (000 499 1 여자 2 남자에 대 한) 및 500-999 탑재에 대 한 동일한 날에 태어난 사용자에 게는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="81395-532">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-533">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-533">Checksum</span></span>

<span data-ttu-id="81395-534">예</span><span class="sxs-lookup"><span data-stu-id="81395-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-535">정의</span><span class="sxs-lookup"><span data-stu-id="81395-535">Definition</span></span>

<span data-ttu-id="81395-536">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-537">다음은 함수 `Func_slovenia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-538">키워드에서 `Keywords_slovenia_eu_national_id_card` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="81395-539">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-540">다음은 함수 `Func_slovenia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="81395-541">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="81395-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="81395-543">개인 숫자 코드</span><span class="sxs-lookup"><span data-stu-id="81395-543">personal numeric code</span></span>
  
<span data-ttu-id="81395-544">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-544">unique identification number</span></span>
  
<span data-ttu-id="81395-545">등록 하는 고유 번호</span><span class="sxs-lookup"><span data-stu-id="81395-545">unique registration number</span></span>
  
<span data-ttu-id="81395-546">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-546">unique identity number</span></span>
  
<span data-ttu-id="81395-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="81395-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="81395-548">고유 마스터 시민 번호</span><span class="sxs-lookup"><span data-stu-id="81395-548">unique master citizen number</span></span>
  
<span data-ttu-id="81395-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="81395-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="81395-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="81395-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="81395-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="81395-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="81395-552">emšo</span><span class="sxs-lookup"><span data-stu-id="81395-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="81395-553">스페인</span><span class="sxs-lookup"><span data-stu-id="81395-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="81395-554">형식</span><span class="sxs-lookup"><span data-stu-id="81395-554">Format</span></span>

<span data-ttu-id="81395-555">한 문자 앞에 오는 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="81395-556">패턴</span><span class="sxs-lookup"><span data-stu-id="81395-556">Pattern</span></span>

<span data-ttu-id="81395-557">한 문자 앞에 오는 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="81395-558">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="81395-558">Seven digits</span></span>
    
- <span data-ttu-id="81395-559">한 자리 숫자 또는 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="81395-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="81395-560">체크섬</span><span class="sxs-lookup"><span data-stu-id="81395-560">Checksum</span></span>

<span data-ttu-id="81395-561">해당 없음</span><span class="sxs-lookup"><span data-stu-id="81395-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="81395-562">정의</span><span class="sxs-lookup"><span data-stu-id="81395-562">Definition</span></span>

<span data-ttu-id="81395-563">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="81395-564">정규식 `Regex_spain_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="81395-565">키워드에서 `Keywords_spain_eu_national_id_card"` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81395-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="81395-566">키워드</span><span class="sxs-lookup"><span data-stu-id="81395-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="81395-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="81395-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="81395-568">dni</span><span class="sxs-lookup"><span data-stu-id="81395-568">dni</span></span>
  
<span data-ttu-id="81395-569">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-569">national identification number</span></span>
  
<span data-ttu-id="81395-570">identity 국가 번호</span><span class="sxs-lookup"><span data-stu-id="81395-570">national identity number</span></span>
  
<span data-ttu-id="81395-571">보험 번호</span><span class="sxs-lookup"><span data-stu-id="81395-571">insurance number</span></span>
  
<span data-ttu-id="81395-572">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="81395-572">personal identification number</span></span>
  
<span data-ttu-id="81395-573">국가 identity</span><span class="sxs-lookup"><span data-stu-id="81395-573">national identity</span></span>
  
<span data-ttu-id="81395-574">개인 id 없음</span><span class="sxs-lookup"><span data-stu-id="81395-574">personal identity no</span></span>
  
<span data-ttu-id="81395-575">고유 id 번호</span><span class="sxs-lookup"><span data-stu-id="81395-575">unique identity number</span></span>
  
<span data-ttu-id="81395-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="81395-576">nationalidno#</span></span>
  
<span data-ttu-id="81395-577">uniqueid #</span><span class="sxs-lookup"><span data-stu-id="81395-577">uniqueid#</span></span>
  
<span data-ttu-id="81395-578">dni #</span><span class="sxs-lookup"><span data-stu-id="81395-578">dni#</span></span>
  
<span data-ttu-id="81395-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="81395-579">nationalid#</span></span>
  
<span data-ttu-id="81395-580">nie #</span><span class="sxs-lookup"><span data-stu-id="81395-580">nie#</span></span>
  
<span data-ttu-id="81395-581">nie</span><span class="sxs-lookup"><span data-stu-id="81395-581">nie</span></span>
  
<span data-ttu-id="81395-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="81395-582">nienúmero#</span></span>
  
<span data-ttu-id="81395-583">nie número</span><span class="sxs-lookup"><span data-stu-id="81395-583">nie número</span></span>
  
<span data-ttu-id="81395-584">documento nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="81395-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="81395-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="81395-585">identidad único</span></span>
  
<span data-ttu-id="81395-586">número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="81395-586">número nacional identidad</span></span>
  
<span data-ttu-id="81395-587">dni número</span><span class="sxs-lookup"><span data-stu-id="81395-587">dni número</span></span>
  
<span data-ttu-id="81395-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="81395-588">dninúmero#</span></span>
  
<span data-ttu-id="81395-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="81395-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="81395-590">스웨덴</span><span class="sxs-lookup"><span data-stu-id="81395-590">Sweden</span></span>

<span data-ttu-id="81395-591">자세한 내용은의 섹션을 참조 "스웨덴 국가 ID" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81395-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="81395-592">참고 항목</span><span class="sxs-lookup"><span data-stu-id="81395-592">See also</span></span>

[<span data-ttu-id="81395-593">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="81395-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

