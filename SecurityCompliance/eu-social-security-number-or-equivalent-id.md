---
title: EU 주민 등록 번호 또는 동등한 ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 주민 등록 번호 또는 동등한 ID 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: abcefb6930e9c02d2f32d84b65accfecf1e20d95
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216528"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="752aa-104">EU 주민 등록 번호 또는 동등한 ID</span><span class="sxs-lookup"><span data-stu-id="752aa-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="752aa-p102">이 항목에서는 DLP (데이터 손실 방지) 정책이 EU SSN (사회 보장 번호) 또는 동등한 ID 중요 정보 유형을 검색할 때 어떤 사항을 찾을 지를 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="752aa-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="752aa-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="752aa-108">형식</span><span class="sxs-lookup"><span data-stu-id="752aa-108">Format</span></span>

<span data-ttu-id="752aa-109">지정 된 형식의 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="752aa-110">패턴</span><span class="sxs-lookup"><span data-stu-id="752aa-110">Pattern</span></span>

<span data-ttu-id="752aa-111">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="752aa-111">10 digits:</span></span>
  
-  <span data-ttu-id="752aa-112">일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="752aa-113">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="752aa-113">One check digit</span></span>
    
- <span data-ttu-id="752aa-114">생년월일에 해당 하는 6 자리 숫자 (ddmmyy)</span><span class="sxs-lookup"><span data-stu-id="752aa-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="752aa-115">체크섬</span><span class="sxs-lookup"><span data-stu-id="752aa-115">Checksum</span></span>

<span data-ttu-id="752aa-116">예</span><span class="sxs-lookup"><span data-stu-id="752aa-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="752aa-117">정의</span><span class="sxs-lookup"><span data-stu-id="752aa-117">Definition</span></span>

<span data-ttu-id="752aa-118">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-119">이 함수 `Func_austria_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="752aa-120">from `Keywords_austria_eu_ssn_or_equivalent` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="752aa-121">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-122">이 함수 `Func_austria_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="752aa-123">키워드</span><span class="sxs-lookup"><span data-stu-id="752aa-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="752aa-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="752aa-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="752aa-125">소셜 보안 아니요</span><span class="sxs-lookup"><span data-stu-id="752aa-125">social security no</span></span>
  
<span data-ttu-id="752aa-126">social security number
</span><span class="sxs-lookup"><span data-stu-id="752aa-126">social security number</span></span>
  
<span data-ttu-id="752aa-127">
social security code</span><span class="sxs-lookup"><span data-stu-id="752aa-127">social security code</span></span>
  
<span data-ttu-id="752aa-128">보험 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-128">insurance number</span></span>
  
<span data-ttu-id="752aa-129">오스트리아</span><span class="sxs-lookup"><span data-stu-id="752aa-129">austrian ssn</span></span>
  
<span data-ttu-id="752aa-130">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-130">ssn#</span></span>
  
<span data-ttu-id="752aa-131">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-131">ssn</span></span>
  
<span data-ttu-id="752aa-132">보험 코드</span><span class="sxs-lookup"><span data-stu-id="752aa-132">insurance code</span></span>
  
<span data-ttu-id="752aa-133">보험 코드 #</span><span class="sxs-lookup"><span data-stu-id="752aa-133">insurance code#</span></span>
  
<span data-ttu-id="752aa-134">사회 alsecurityno #</span><span class="sxs-lookup"><span data-stu-id="752aa-134">socialsecurityno#</span></span>
  
<span data-ttu-id="752aa-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="752aa-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="752aa-136">soziale sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="752aa-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="752aa-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="752aa-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="752aa-138">벨기에</span><span class="sxs-lookup"><span data-stu-id="752aa-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="752aa-139">형식</span><span class="sxs-lookup"><span data-stu-id="752aa-139">Format</span></span>

<span data-ttu-id="752aa-140">공백이 나 구분 기호가 없는 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="752aa-141">패턴</span><span class="sxs-lookup"><span data-stu-id="752aa-141">Pattern</span></span>

<span data-ttu-id="752aa-142">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="752aa-143">체크섬</span><span class="sxs-lookup"><span data-stu-id="752aa-143">Checksum</span></span>

<span data-ttu-id="752aa-144">예</span><span class="sxs-lookup"><span data-stu-id="752aa-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="752aa-145">정의</span><span class="sxs-lookup"><span data-stu-id="752aa-145">Definition</span></span>

<span data-ttu-id="752aa-146">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-147">이 함수 `Func_belgium_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="752aa-148">from `Keywords_belgium_eu_ssn_or_equivalent` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="752aa-149">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-150">이 함수 `Func_belgium_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="752aa-151">키워드</span><span class="sxs-lookup"><span data-stu-id="752aa-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="752aa-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="752aa-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="752aa-153">벨기에 국가 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-153">belgian national number</span></span>
  
<span data-ttu-id="752aa-154">국가 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-154">national number</span></span>
  
<span data-ttu-id="752aa-155">social security number
</span><span class="sxs-lookup"><span data-stu-id="752aa-155">social security number</span></span>
  
<span data-ttu-id="752aa-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-156">nationalnumber#</span></span>
  
<span data-ttu-id="752aa-157">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-157">ssn#</span></span>
  
<span data-ttu-id="752aa-158">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-158">ssn</span></span>
  
<span data-ttu-id="752aa-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="752aa-159">nationalnumber</span></span>
  
<span data-ttu-id="752aa-160">bnn #</span><span class="sxs-lookup"><span data-stu-id="752aa-160">bnn#</span></span>
  
<span data-ttu-id="752aa-161">bnn</span><span class="sxs-lookup"><span data-stu-id="752aa-161">bnn</span></span>
  
<span data-ttu-id="752aa-162">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-162">personal id number</span></span>
  
<span data-ttu-id="752aa-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-163">personalidnumber#</span></span>
  
<span data-ttu-id="752aa-164">numéro 국가</span><span class="sxs-lookup"><span data-stu-id="752aa-164">numéro national</span></span>
  
<span data-ttu-id="752aa-165">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="752aa-165">numéro de sécurité</span></span>
  
<span data-ttu-id="752aa-166">numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="752aa-166">numéro d'assuré</span></span>
  
<span data-ttu-id="752aa-167">identifiant 국가</span><span class="sxs-lookup"><span data-stu-id="752aa-167">identifiant national</span></span>
  
<span data-ttu-id="752aa-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="752aa-168">identifiantnational#</span></span>
  
<span data-ttu-id="752aa-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="752aa-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="752aa-170">크로아티아</span><span class="sxs-lookup"><span data-stu-id="752aa-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="752aa-171">형식</span><span class="sxs-lookup"><span data-stu-id="752aa-171">Format</span></span>

<span data-ttu-id="752aa-172">공백과 구분 기호를 사용 하지 않고 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="752aa-173">패턴</span><span class="sxs-lookup"><span data-stu-id="752aa-173">Pattern</span></span>

 <span data-ttu-id="752aa-174">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="752aa-174">11 digits:</span></span> 
  
-  <span data-ttu-id="752aa-175">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-175">Ten digits</span></span> 
    
- <span data-ttu-id="752aa-176">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="752aa-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="752aa-177">체크섬</span><span class="sxs-lookup"><span data-stu-id="752aa-177">Checksum</span></span>

<span data-ttu-id="752aa-178">예</span><span class="sxs-lookup"><span data-stu-id="752aa-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="752aa-179">정의</span><span class="sxs-lookup"><span data-stu-id="752aa-179">Definition</span></span>

<span data-ttu-id="752aa-180">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-181">이 함수 `Func_croatia_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="752aa-182">from `Keywords_croatia_eu_ssn_or_equivalent` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="752aa-183">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-184">이 함수 `Func_croatia_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="752aa-185">키워드</span><span class="sxs-lookup"><span data-stu-id="752aa-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="752aa-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="752aa-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="752aa-187">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-187">personal identification number</span></span>
  
<span data-ttu-id="752aa-188">마스터 시민 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-188">master citizen number</span></span>
  
<span data-ttu-id="752aa-189">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-189">national identification number</span></span>
  
<span data-ttu-id="752aa-190">social security number
</span><span class="sxs-lookup"><span data-stu-id="752aa-190">social security number</span></span>
  
<span data-ttu-id="752aa-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-191">nationalnumber#</span></span>
  
<span data-ttu-id="752aa-192">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-192">ssn#</span></span>
  
<span data-ttu-id="752aa-193">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-193">ssn</span></span>
  
<span data-ttu-id="752aa-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="752aa-194">nationalnumber</span></span>
  
<span data-ttu-id="752aa-195">bnn #</span><span class="sxs-lookup"><span data-stu-id="752aa-195">bnn#</span></span>
  
<span data-ttu-id="752aa-196">bnn</span><span class="sxs-lookup"><span data-stu-id="752aa-196">bnn</span></span>
  
<span data-ttu-id="752aa-197">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-197">personal id number</span></span>
  
<span data-ttu-id="752aa-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-198">personalidnumber#</span></span>
  
<span data-ttu-id="752aa-199">oib</span><span class="sxs-lookup"><span data-stu-id="752aa-199">oib</span></span>
  
<span data-ttu-id="752aa-200">osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="752aa-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="752aa-201">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="752aa-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="752aa-202">형식</span><span class="sxs-lookup"><span data-stu-id="752aa-202">Format</span></span>

<span data-ttu-id="752aa-203">지정 된 패턴의 10 자리 및 백슬래시</span><span class="sxs-lookup"><span data-stu-id="752aa-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="752aa-204">패턴</span><span class="sxs-lookup"><span data-stu-id="752aa-204">Pattern</span></span>

<span data-ttu-id="752aa-205">10 자리 숫자와 백슬래시:</span><span class="sxs-lookup"><span data-stu-id="752aa-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="752aa-206">생년월일에 해당 하는 6 자리 숫자 (YYMMDD):</span><span class="sxs-lookup"><span data-stu-id="752aa-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="752aa-207">백슬래시</span><span class="sxs-lookup"><span data-stu-id="752aa-207">A backslash</span></span>
    
- <span data-ttu-id="752aa-208">같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="752aa-209">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="752aa-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="752aa-210">체크섬</span><span class="sxs-lookup"><span data-stu-id="752aa-210">Checksum</span></span>

<span data-ttu-id="752aa-211">예</span><span class="sxs-lookup"><span data-stu-id="752aa-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="752aa-212">정의</span><span class="sxs-lookup"><span data-stu-id="752aa-212">Definition</span></span>

<span data-ttu-id="752aa-213">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-214">이 함수 `Func_czech_republic_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="752aa-215">from `Keywords_czech_republic_eu_ssn_or_equivalent` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="752aa-216">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-217">이 함수 `Func_czech_republic_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="752aa-218">키워드</span><span class="sxs-lookup"><span data-stu-id="752aa-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="752aa-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="752aa-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="752aa-220">돌 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-220">birth number</span></span>
  
<span data-ttu-id="752aa-221">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-221">national identification number</span></span>
  
<span data-ttu-id="752aa-222">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-222">personal identification number</span></span>
  
<span data-ttu-id="752aa-223">social security number
</span><span class="sxs-lookup"><span data-stu-id="752aa-223">social security number</span></span>
  
<span data-ttu-id="752aa-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-224">nationalnumber#</span></span>
  
<span data-ttu-id="752aa-225">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-225">ssn#</span></span>
  
<span data-ttu-id="752aa-226">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-226">ssn</span></span>
  
<span data-ttu-id="752aa-227">국가 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-227">national number</span></span>
  
<span data-ttu-id="752aa-228">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-228">personal id number</span></span>
  
<span data-ttu-id="752aa-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-229">personalidnumber#</span></span>
  
<span data-ttu-id="752aa-230">rč</span><span class="sxs-lookup"><span data-stu-id="752aa-230">rč</span></span>
  
<span data-ttu-id="752aa-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="752aa-231">rodné číslo</span></span>
  
<span data-ttu-id="752aa-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="752aa-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="752aa-233">덴마크</span><span class="sxs-lookup"><span data-stu-id="752aa-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="752aa-234">형식</span><span class="sxs-lookup"><span data-stu-id="752aa-234">Format</span></span>

<span data-ttu-id="752aa-235">지정 된 패턴의 10 자리 및 하이픈</span><span class="sxs-lookup"><span data-stu-id="752aa-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="752aa-236">패턴</span><span class="sxs-lookup"><span data-stu-id="752aa-236">Pattern</span></span>

<span data-ttu-id="752aa-237">10 자리 숫자와 하이픈:</span><span class="sxs-lookup"><span data-stu-id="752aa-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="752aa-238">생년월일에 해당 하는 6 자리 숫자 (ddmmyy)</span><span class="sxs-lookup"><span data-stu-id="752aa-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="752aa-239">하이픈</span><span class="sxs-lookup"><span data-stu-id="752aa-239">A hyphen</span></span>
    
- <span data-ttu-id="752aa-240">일련 번호에 해당 하는 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="752aa-241">체크섬</span><span class="sxs-lookup"><span data-stu-id="752aa-241">Checksum</span></span>

<span data-ttu-id="752aa-242">예</span><span class="sxs-lookup"><span data-stu-id="752aa-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="752aa-243">정의</span><span class="sxs-lookup"><span data-stu-id="752aa-243">Definition</span></span>

<span data-ttu-id="752aa-244">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-245">이 함수 `Func_denmark_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="752aa-246">from `Keywords_denmark_eu_ssn_or_equivalent` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="752aa-247">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-248">이 함수 `Func_denmark_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="752aa-249">키워드</span><span class="sxs-lookup"><span data-stu-id="752aa-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="752aa-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="752aa-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="752aa-251">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-251">personal identification number</span></span>
  
<span data-ttu-id="752aa-252">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-252">national identification number</span></span>
  
<span data-ttu-id="752aa-253">social security number
</span><span class="sxs-lookup"><span data-stu-id="752aa-253">social security number</span></span>
  
<span data-ttu-id="752aa-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-254">nationalnumber#</span></span>
  
<span data-ttu-id="752aa-255">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-255">ssn#</span></span>
  
<span data-ttu-id="752aa-256">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-256">ssn</span></span>
  
<span data-ttu-id="752aa-257">국가 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-257">national number</span></span>
  
<span data-ttu-id="752aa-258">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-258">personal id number</span></span>
  
<span data-ttu-id="752aa-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-259">personalidnumber#</span></span>
  
<span data-ttu-id="752aa-260">cpr-nummer</span><span class="sxs-lookup"><span data-stu-id="752aa-260">cpr-nummer</span></span>
  
<span data-ttu-id="752aa-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="752aa-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="752aa-262">핀란드</span><span class="sxs-lookup"><span data-stu-id="752aa-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="752aa-263">형식</span><span class="sxs-lookup"><span data-stu-id="752aa-263">Format</span></span>

<span data-ttu-id="752aa-264">지정 된 형식의 11 자 조합</span><span class="sxs-lookup"><span data-stu-id="752aa-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="752aa-265">패턴</span><span class="sxs-lookup"><span data-stu-id="752aa-265">Pattern</span></span>

<span data-ttu-id="752aa-266">다음은 지정 된 형식의 11 자 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="752aa-267">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-267">Six digits</span></span> 
    
- <span data-ttu-id="752aa-268">다음 중 하나의 인스턴스에 대해 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="752aa-269">더하기 기호</span><span class="sxs-lookup"><span data-stu-id="752aa-269">Plus symbol</span></span>
    
  - <span data-ttu-id="752aa-270">빼기 기호</span><span class="sxs-lookup"><span data-stu-id="752aa-270">Minus symbol</span></span>
    
  - <span data-ttu-id="752aa-271">문자 "A" (대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="752aa-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="752aa-272">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-272">Three digits</span></span>
    
- <span data-ttu-id="752aa-273">1 개의 문자 또는 1 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="752aa-274">체크섬</span><span class="sxs-lookup"><span data-stu-id="752aa-274">Checksum</span></span>

<span data-ttu-id="752aa-275">예</span><span class="sxs-lookup"><span data-stu-id="752aa-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="752aa-276">정의</span><span class="sxs-lookup"><span data-stu-id="752aa-276">Definition</span></span>

<span data-ttu-id="752aa-277">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-278">이 함수 `Func_finland_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="752aa-279">from `Keywords_finland_eu_ssn_or_equivalent` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="752aa-280">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-281">이 함수 `Func_finland_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="752aa-282">키워드</span><span class="sxs-lookup"><span data-stu-id="752aa-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="752aa-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="752aa-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="752aa-284">identification number
</span><span class="sxs-lookup"><span data-stu-id="752aa-284">identification number</span></span>
  
<span data-ttu-id="752aa-285">개인 id</span><span class="sxs-lookup"><span data-stu-id="752aa-285">personal id</span></span>
  
<span data-ttu-id="752aa-286">id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-286">identity number</span></span>
  
<span data-ttu-id="752aa-287">핀란드어 국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-287">finnish national id number</span></span>
  
<span data-ttu-id="752aa-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="752aa-288">personalidnumber#</span></span>
  
<span data-ttu-id="752aa-289">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-289">national identification number</span></span>
  
<span data-ttu-id="752aa-290">id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-290">id number</span></span>
  
<span data-ttu-id="752aa-291">국가 id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-291">national id no.</span></span>
  
<span data-ttu-id="752aa-292">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-292">national id number</span></span>
  
<span data-ttu-id="752aa-293">id 없음</span><span class="sxs-lookup"><span data-stu-id="752aa-293">id no</span></span>
  
<span data-ttu-id="752aa-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="752aa-294">tunnistenumero</span></span>
  
<span data-ttu-id="752aa-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="752aa-295">henkilötunnus</span></span>
  
<span data-ttu-id="752aa-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="752aa-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="752aa-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="752aa-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="752aa-298">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="752aa-298">identiteetti numero</span></span>
  
<span data-ttu-id="752aa-299">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="752aa-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="752aa-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="752aa-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="752aa-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="752aa-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="752aa-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="752aa-302">tunnusnumero</span></span>
  
<span data-ttu-id="752aa-303">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="752aa-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="752aa-304">hetu</span><span class="sxs-lookup"><span data-stu-id="752aa-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="752aa-305">프랑스</span><span class="sxs-lookup"><span data-stu-id="752aa-305">France</span></span>

<span data-ttu-id="752aa-306">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"프랑스 사회 보장 번호 (INSEE)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="752aa-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="752aa-307">독일</span><span class="sxs-lookup"><span data-stu-id="752aa-307">Germany</span></span>

<span data-ttu-id="752aa-308">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 id 카드 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="752aa-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="752aa-309">그리스</span><span class="sxs-lookup"><span data-stu-id="752aa-309">Greece</span></span>

<span data-ttu-id="752aa-310">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"그리스 국가 ID 카드" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="752aa-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="752aa-311">헝가리</span><span class="sxs-lookup"><span data-stu-id="752aa-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="752aa-312">형식</span><span class="sxs-lookup"><span data-stu-id="752aa-312">Format</span></span>

<span data-ttu-id="752aa-313">공백과 구분 기호를 사용 하지 않고 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="752aa-314">패턴</span><span class="sxs-lookup"><span data-stu-id="752aa-314">Pattern</span></span>

<span data-ttu-id="752aa-315">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="752aa-316">체크섬</span><span class="sxs-lookup"><span data-stu-id="752aa-316">Checksum</span></span>

<span data-ttu-id="752aa-317">예</span><span class="sxs-lookup"><span data-stu-id="752aa-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="752aa-318">정의</span><span class="sxs-lookup"><span data-stu-id="752aa-318">Definition</span></span>

<span data-ttu-id="752aa-319">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-320">이 함수 `Func_hungary_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="752aa-321">from `Keywords_hungary_eu_ssn_or_equivalent` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="752aa-322">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-323">이 함수 `Func_hungary_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="752aa-324">키워드</span><span class="sxs-lookup"><span data-stu-id="752aa-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="752aa-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="752aa-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="752aa-326">헝가리어 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-326">hungarian social security number</span></span>
  
<span data-ttu-id="752aa-327">social security number
</span><span class="sxs-lookup"><span data-stu-id="752aa-327">social security number</span></span>
  
<span data-ttu-id="752aa-328">사회 alsecurity번호 #</span><span class="sxs-lookup"><span data-stu-id="752aa-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="752aa-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="752aa-329">hssn#</span></span>
  
<span data-ttu-id="752aa-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="752aa-330">socialsecuritynno</span></span>
  
<span data-ttu-id="752aa-331">hssn</span><span class="sxs-lookup"><span data-stu-id="752aa-331">hssn</span></span>
  
<span data-ttu-id="752aa-332">taj</span><span class="sxs-lookup"><span data-stu-id="752aa-332">taj</span></span>
  
<span data-ttu-id="752aa-333">taj #</span><span class="sxs-lookup"><span data-stu-id="752aa-333">taj#</span></span>
  
<span data-ttu-id="752aa-334">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-334">ssn</span></span>
  
<span data-ttu-id="752aa-335">ssn</span><span class="sxs-lookup"><span data-stu-id="752aa-335">ssn#</span></span>
  
<span data-ttu-id="752aa-336">소셜 보안 아니요</span><span class="sxs-lookup"><span data-stu-id="752aa-336">social security no</span></span>
  
<span data-ttu-id="752aa-337">áfa</span><span class="sxs-lookup"><span data-stu-id="752aa-337">áfa</span></span>
  
<span data-ttu-id="752aa-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="752aa-338">közösségi adószám</span></span>
  
<span data-ttu-id="752aa-339">általános forgalmi adó</span><span class="sxs-lookup"><span data-stu-id="752aa-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="752aa-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="752aa-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="752aa-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="752aa-341">áfa szám</span></span>
  
<span data-ttu-id="752aa-342">magyar áfa szám</span><span class="sxs-lookup"><span data-stu-id="752aa-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="752aa-343">포르투갈</span><span class="sxs-lookup"><span data-stu-id="752aa-343">Portugal</span></span>

<span data-ttu-id="752aa-344">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"포르투갈 시민이 카드 번호" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="752aa-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="752aa-345">스페인</span><span class="sxs-lookup"><span data-stu-id="752aa-345">Spain</span></span>

<span data-ttu-id="752aa-346">자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스페인 SSN (사회 보장 번호)" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="752aa-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="752aa-347">스웨덴</span><span class="sxs-lookup"><span data-stu-id="752aa-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="752aa-348">형식</span><span class="sxs-lookup"><span data-stu-id="752aa-348">Format</span></span>

<span data-ttu-id="752aa-349">공백과 구분 기호를 사용 하지 않고 12 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="752aa-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="752aa-350">패턴</span><span class="sxs-lookup"><span data-stu-id="752aa-350">Pattern</span></span>

<span data-ttu-id="752aa-351">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="752aa-351">12 digits:</span></span>
  
-  <span data-ttu-id="752aa-352">출생 날짜에 해당 하는 8 자리 숫자 (YYYYMMDD)</span><span class="sxs-lookup"><span data-stu-id="752aa-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="752aa-353">일련 번호에 해당 하는 3 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="752aa-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="752aa-354">일련 번호의 마지막 숫자는 남성에 홀수를 할당 하는 성별과 암의 짝수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="752aa-355">최대 1990의 일련 번호를 사용 하 여 전화를 corresponded 하는 국가, 즉 세금 레코드에 따라 (1947 이전에 태어난 경우)에는에 대 한 작업을 수행 하는 경우 (예를 들어 세금이 기록 됨) immigrants</span><span class="sxs-lookup"><span data-stu-id="752aa-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="752aa-356">검사 숫자 1 개</span><span class="sxs-lookup"><span data-stu-id="752aa-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="752aa-357">체크섬</span><span class="sxs-lookup"><span data-stu-id="752aa-357">Checksum</span></span>

<span data-ttu-id="752aa-358">예</span><span class="sxs-lookup"><span data-stu-id="752aa-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="752aa-359">정의</span><span class="sxs-lookup"><span data-stu-id="752aa-359">Definition</span></span>

<span data-ttu-id="752aa-360">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-361">이 함수 `Func_sweden_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="752aa-362">from `Keywords_sweden_eu_ssn_or_equivalent` 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="752aa-363">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="752aa-364">이 함수 `Func_sweden_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="752aa-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="752aa-365">키워드</span><span class="sxs-lookup"><span data-stu-id="752aa-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="752aa-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="752aa-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="752aa-367">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="752aa-367">personal id number</span></span>
  
<span data-ttu-id="752aa-368">identification number
</span><span class="sxs-lookup"><span data-stu-id="752aa-368">identification number</span></span>
  
<span data-ttu-id="752aa-369">개인 id 없음</span><span class="sxs-lookup"><span data-stu-id="752aa-369">personal id no</span></span>
  
<span data-ttu-id="752aa-370">identity no</span><span class="sxs-lookup"><span data-stu-id="752aa-370">identity no</span></span>
  
<span data-ttu-id="752aa-371">id 아니요</span><span class="sxs-lookup"><span data-stu-id="752aa-371">identification no</span></span>
  
<span data-ttu-id="752aa-372">개인 식별 아니요</span><span class="sxs-lookup"><span data-stu-id="752aa-372">personal identification no</span></span>
  
<span data-ttu-id="752aa-373">personnummer id</span><span class="sxs-lookup"><span data-stu-id="752aa-373">personnummer id</span></span>
  
<span data-ttu-id="752aa-374">personligt id-nummer</span><span class="sxs-lookup"><span data-stu-id="752aa-374">personligt id-nummer</span></span>
  
<span data-ttu-id="752aa-375">unikt id-nummer</span><span class="sxs-lookup"><span data-stu-id="752aa-375">unikt id-nummer</span></span>
  
<span data-ttu-id="752aa-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="752aa-376">personnummer</span></span>
  
<span data-ttu-id="752aa-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="752aa-377">identifikationsnumret</span></span>
  
<span data-ttu-id="752aa-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="752aa-378">personnummer#</span></span>
  
<span data-ttu-id="752aa-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="752aa-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="752aa-380">참고 항목</span><span class="sxs-lookup"><span data-stu-id="752aa-380">See also</span></span>

[<span data-ttu-id="752aa-381">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="752aa-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

