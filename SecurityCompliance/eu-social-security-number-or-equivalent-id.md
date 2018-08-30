---
title: EU 사회보장 번호 또는에 상응 하는 ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: 이 항목에서는 EU 사회보장 번호 또는 해당 하는 ID 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533379"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="328b8-104">EU 사회보장 번호 또는에 상응 하는 ID</span><span class="sxs-lookup"><span data-stu-id="328b8-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="328b8-p102">이 항목에서는 EU 사회보장 번호 (SSN) 또는 해당 하는 ID 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="328b8-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="328b8-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="328b8-108">형식</span><span class="sxs-lookup"><span data-stu-id="328b8-108">Format</span></span>

<span data-ttu-id="328b8-109">지정 된 형식에서 10 자 사이일</span><span class="sxs-lookup"><span data-stu-id="328b8-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="328b8-110">패턴</span><span class="sxs-lookup"><span data-stu-id="328b8-110">Pattern</span></span>

<span data-ttu-id="328b8-111">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="328b8-111">10 digits:</span></span>
  
-  <span data-ttu-id="328b8-112">일련 번호에 해당 하는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="328b8-113">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-113">One check digit</span></span>
    
- <span data-ttu-id="328b8-114">생일 (DDMMYY)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="328b8-115">체크섬</span><span class="sxs-lookup"><span data-stu-id="328b8-115">Checksum</span></span>

<span data-ttu-id="328b8-116">예</span><span class="sxs-lookup"><span data-stu-id="328b8-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="328b8-117">정의</span><span class="sxs-lookup"><span data-stu-id="328b8-117">Definition</span></span>

<span data-ttu-id="328b8-118">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-119">다음은 함수 `Func_austria_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="328b8-120">키워드에서 `Keywords_austria_eu_ssn_or_equivalent` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="328b8-121">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-122">다음은 함수 `Func_austria_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="328b8-123">키워드</span><span class="sxs-lookup"><span data-stu-id="328b8-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="328b8-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="328b8-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="328b8-125">주민등록 없음</span><span class="sxs-lookup"><span data-stu-id="328b8-125">social security no</span></span>
  
<span data-ttu-id="328b8-126">social security number
</span><span class="sxs-lookup"><span data-stu-id="328b8-126">social security number</span></span>
  
<span data-ttu-id="328b8-127">
social security code</span><span class="sxs-lookup"><span data-stu-id="328b8-127">social security code</span></span>
  
<span data-ttu-id="328b8-128">보험 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-128">insurance number</span></span>
  
<span data-ttu-id="328b8-129">오스트리아 ssn</span><span class="sxs-lookup"><span data-stu-id="328b8-129">austrian ssn</span></span>
  
<span data-ttu-id="328b8-130">ssn #</span><span class="sxs-lookup"><span data-stu-id="328b8-130">ssn#</span></span>
  
<span data-ttu-id="328b8-131">ssn</span><span class="sxs-lookup"><span data-stu-id="328b8-131">ssn</span></span>
  
<span data-ttu-id="328b8-132">보험 코드</span><span class="sxs-lookup"><span data-stu-id="328b8-132">insurance code</span></span>
  
<span data-ttu-id="328b8-133">보험 코드 #</span><span class="sxs-lookup"><span data-stu-id="328b8-133">insurance code#</span></span>
  
<span data-ttu-id="328b8-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="328b8-134">socialsecurityno#</span></span>
  
<span data-ttu-id="328b8-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="328b8-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="328b8-136">soziale 독일어 kein</span><span class="sxs-lookup"><span data-stu-id="328b8-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="328b8-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="328b8-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="328b8-138">벨기에</span><span class="sxs-lookup"><span data-stu-id="328b8-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="328b8-139">형식</span><span class="sxs-lookup"><span data-stu-id="328b8-139">Format</span></span>

<span data-ttu-id="328b8-140">공백이 나 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="328b8-141">패턴</span><span class="sxs-lookup"><span data-stu-id="328b8-141">Pattern</span></span>

<span data-ttu-id="328b8-142">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="328b8-143">체크섬</span><span class="sxs-lookup"><span data-stu-id="328b8-143">Checksum</span></span>

<span data-ttu-id="328b8-144">예</span><span class="sxs-lookup"><span data-stu-id="328b8-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="328b8-145">정의</span><span class="sxs-lookup"><span data-stu-id="328b8-145">Definition</span></span>

<span data-ttu-id="328b8-146">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-147">다음은 함수 `Func_belgium_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="328b8-148">키워드에서 `Keywords_belgium_eu_ssn_or_equivalent` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="328b8-149">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-150">다음은 함수 `Func_belgium_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="328b8-151">키워드</span><span class="sxs-lookup"><span data-stu-id="328b8-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="328b8-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="328b8-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="328b8-153">국가 번호 (벨기에)</span><span class="sxs-lookup"><span data-stu-id="328b8-153">belgian national number</span></span>
  
<span data-ttu-id="328b8-154">국가 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-154">national number</span></span>
  
<span data-ttu-id="328b8-155">social security number
</span><span class="sxs-lookup"><span data-stu-id="328b8-155">social security number</span></span>
  
<span data-ttu-id="328b8-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-156">nationalnumber#</span></span>
  
<span data-ttu-id="328b8-157">ssn #</span><span class="sxs-lookup"><span data-stu-id="328b8-157">ssn#</span></span>
  
<span data-ttu-id="328b8-158">ssn</span><span class="sxs-lookup"><span data-stu-id="328b8-158">ssn</span></span>
  
<span data-ttu-id="328b8-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="328b8-159">nationalnumber</span></span>
  
<span data-ttu-id="328b8-160">bnn #</span><span class="sxs-lookup"><span data-stu-id="328b8-160">bnn#</span></span>
  
<span data-ttu-id="328b8-161">bnn</span><span class="sxs-lookup"><span data-stu-id="328b8-161">bnn</span></span>
  
<span data-ttu-id="328b8-162">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-162">personal id number</span></span>
  
<span data-ttu-id="328b8-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-163">personalidnumber#</span></span>
  
<span data-ttu-id="328b8-164">numéro 국가</span><span class="sxs-lookup"><span data-stu-id="328b8-164">numéro national</span></span>
  
<span data-ttu-id="328b8-165">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="328b8-165">numéro de sécurité</span></span>
  
<span data-ttu-id="328b8-166">numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="328b8-166">numéro d'assuré</span></span>
  
<span data-ttu-id="328b8-167">identifiant 국가</span><span class="sxs-lookup"><span data-stu-id="328b8-167">identifiant national</span></span>
  
<span data-ttu-id="328b8-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="328b8-168">identifiantnational#</span></span>
  
<span data-ttu-id="328b8-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="328b8-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="328b8-170">크로아티아</span><span class="sxs-lookup"><span data-stu-id="328b8-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="328b8-171">형식</span><span class="sxs-lookup"><span data-stu-id="328b8-171">Format</span></span>

<span data-ttu-id="328b8-172">공백 및 구분 기호 없이 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="328b8-173">패턴</span><span class="sxs-lookup"><span data-stu-id="328b8-173">Pattern</span></span>

 <span data-ttu-id="328b8-174">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="328b8-174">11 digits:</span></span> 
  
-  <span data-ttu-id="328b8-175">10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-175">Ten digits</span></span> 
    
- <span data-ttu-id="328b8-176">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="328b8-177">체크섬</span><span class="sxs-lookup"><span data-stu-id="328b8-177">Checksum</span></span>

<span data-ttu-id="328b8-178">예</span><span class="sxs-lookup"><span data-stu-id="328b8-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="328b8-179">정의</span><span class="sxs-lookup"><span data-stu-id="328b8-179">Definition</span></span>

<span data-ttu-id="328b8-180">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-181">다음은 함수 `Func_croatia_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="328b8-182">키워드에서 `Keywords_croatia_eu_ssn_or_equivalent` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="328b8-183">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-184">다음은 함수 `Func_croatia_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="328b8-185">키워드</span><span class="sxs-lookup"><span data-stu-id="328b8-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="328b8-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="328b8-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="328b8-187">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-187">personal identification number</span></span>
  
<span data-ttu-id="328b8-188">마스터 시민 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-188">master citizen number</span></span>
  
<span data-ttu-id="328b8-189">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-189">national identification number</span></span>
  
<span data-ttu-id="328b8-190">social security number
</span><span class="sxs-lookup"><span data-stu-id="328b8-190">social security number</span></span>
  
<span data-ttu-id="328b8-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-191">nationalnumber#</span></span>
  
<span data-ttu-id="328b8-192">ssn #</span><span class="sxs-lookup"><span data-stu-id="328b8-192">ssn#</span></span>
  
<span data-ttu-id="328b8-193">ssn</span><span class="sxs-lookup"><span data-stu-id="328b8-193">ssn</span></span>
  
<span data-ttu-id="328b8-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="328b8-194">nationalnumber</span></span>
  
<span data-ttu-id="328b8-195">bnn #</span><span class="sxs-lookup"><span data-stu-id="328b8-195">bnn#</span></span>
  
<span data-ttu-id="328b8-196">bnn</span><span class="sxs-lookup"><span data-stu-id="328b8-196">bnn</span></span>
  
<span data-ttu-id="328b8-197">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-197">personal id number</span></span>
  
<span data-ttu-id="328b8-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-198">personalidnumber#</span></span>
  
<span data-ttu-id="328b8-199">oib</span><span class="sxs-lookup"><span data-stu-id="328b8-199">oib</span></span>
  
<span data-ttu-id="328b8-200">osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="328b8-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="328b8-201">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="328b8-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="328b8-202">형식</span><span class="sxs-lookup"><span data-stu-id="328b8-202">Format</span></span>

<span data-ttu-id="328b8-203">10 자리 숫자와 지정한 패턴에 백슬래시</span><span class="sxs-lookup"><span data-stu-id="328b8-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="328b8-204">패턴</span><span class="sxs-lookup"><span data-stu-id="328b8-204">Pattern</span></span>

<span data-ttu-id="328b8-205">10 자리 숫자와 백슬래시:</span><span class="sxs-lookup"><span data-stu-id="328b8-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="328b8-206">생일 (YYMMDD)에 해당 하는 6 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="328b8-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="328b8-207">백슬래시</span><span class="sxs-lookup"><span data-stu-id="328b8-207">A backslash</span></span>
    
- <span data-ttu-id="328b8-208">같은 날짜 탄생 하 게 하는 사용자를 구분 하는 일련 번호에 해당 하는 세 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="328b8-209">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="328b8-210">체크섬</span><span class="sxs-lookup"><span data-stu-id="328b8-210">Checksum</span></span>

<span data-ttu-id="328b8-211">예</span><span class="sxs-lookup"><span data-stu-id="328b8-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="328b8-212">정의</span><span class="sxs-lookup"><span data-stu-id="328b8-212">Definition</span></span>

<span data-ttu-id="328b8-213">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-214">다음은 함수 `Func_czech_republic_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="328b8-215">키워드에서 `Keywords_czech_republic_eu_ssn_or_equivalent` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="328b8-216">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-217">다음은 함수 `Func_czech_republic_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="328b8-218">키워드</span><span class="sxs-lookup"><span data-stu-id="328b8-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="328b8-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="328b8-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="328b8-220">생일 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-220">birth number</span></span>
  
<span data-ttu-id="328b8-221">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-221">national identification number</span></span>
  
<span data-ttu-id="328b8-222">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-222">personal identification number</span></span>
  
<span data-ttu-id="328b8-223">social security number
</span><span class="sxs-lookup"><span data-stu-id="328b8-223">social security number</span></span>
  
<span data-ttu-id="328b8-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-224">nationalnumber#</span></span>
  
<span data-ttu-id="328b8-225">ssn #</span><span class="sxs-lookup"><span data-stu-id="328b8-225">ssn#</span></span>
  
<span data-ttu-id="328b8-226">ssn</span><span class="sxs-lookup"><span data-stu-id="328b8-226">ssn</span></span>
  
<span data-ttu-id="328b8-227">국가 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-227">national number</span></span>
  
<span data-ttu-id="328b8-228">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-228">personal id number</span></span>
  
<span data-ttu-id="328b8-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-229">personalidnumber#</span></span>
  
<span data-ttu-id="328b8-230">rč</span><span class="sxs-lookup"><span data-stu-id="328b8-230">rč</span></span>
  
<span data-ttu-id="328b8-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="328b8-231">rodné číslo</span></span>
  
<span data-ttu-id="328b8-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="328b8-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="328b8-233">덴마크</span><span class="sxs-lookup"><span data-stu-id="328b8-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="328b8-234">형식</span><span class="sxs-lookup"><span data-stu-id="328b8-234">Format</span></span>

<span data-ttu-id="328b8-235">10 자리 숫자 및 지정된 된 패턴에 하이픈</span><span class="sxs-lookup"><span data-stu-id="328b8-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="328b8-236">패턴</span><span class="sxs-lookup"><span data-stu-id="328b8-236">Pattern</span></span>

<span data-ttu-id="328b8-237">10 자리 숫자 및 하이픈:</span><span class="sxs-lookup"><span data-stu-id="328b8-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="328b8-238">생일 (DDMMYY)에 해당 하는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="328b8-239">하이픈</span><span class="sxs-lookup"><span data-stu-id="328b8-239">A hyphen</span></span>
    
- <span data-ttu-id="328b8-240">시퀀스 번호에 해당 하는 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="328b8-241">체크섬</span><span class="sxs-lookup"><span data-stu-id="328b8-241">Checksum</span></span>

<span data-ttu-id="328b8-242">예</span><span class="sxs-lookup"><span data-stu-id="328b8-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="328b8-243">정의</span><span class="sxs-lookup"><span data-stu-id="328b8-243">Definition</span></span>

<span data-ttu-id="328b8-244">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-245">다음은 함수 `Func_denmark_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="328b8-246">키워드에서 `Keywords_denmark_eu_ssn_or_equivalent` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="328b8-247">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-248">다음은 함수 `Func_denmark_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="328b8-249">키워드</span><span class="sxs-lookup"><span data-stu-id="328b8-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="328b8-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="328b8-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="328b8-251">개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-251">personal identification number</span></span>
  
<span data-ttu-id="328b8-252">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-252">national identification number</span></span>
  
<span data-ttu-id="328b8-253">social security number
</span><span class="sxs-lookup"><span data-stu-id="328b8-253">social security number</span></span>
  
<span data-ttu-id="328b8-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-254">nationalnumber#</span></span>
  
<span data-ttu-id="328b8-255">ssn #</span><span class="sxs-lookup"><span data-stu-id="328b8-255">ssn#</span></span>
  
<span data-ttu-id="328b8-256">ssn</span><span class="sxs-lookup"><span data-stu-id="328b8-256">ssn</span></span>
  
<span data-ttu-id="328b8-257">국가 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-257">national number</span></span>
  
<span data-ttu-id="328b8-258">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-258">personal id number</span></span>
  
<span data-ttu-id="328b8-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-259">personalidnumber#</span></span>
  
<span data-ttu-id="328b8-260">cpr nummer</span><span class="sxs-lookup"><span data-stu-id="328b8-260">cpr-nummer</span></span>
  
<span data-ttu-id="328b8-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="328b8-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="328b8-262">핀란드</span><span class="sxs-lookup"><span data-stu-id="328b8-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="328b8-263">형식</span><span class="sxs-lookup"><span data-stu-id="328b8-263">Format</span></span>

<span data-ttu-id="328b8-264">지정 된 형식에는 11 자리의 조합</span><span class="sxs-lookup"><span data-stu-id="328b8-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="328b8-265">패턴</span><span class="sxs-lookup"><span data-stu-id="328b8-265">Pattern</span></span>

<span data-ttu-id="328b8-266">지정 된 형식에는 11 자리의 조합 합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="328b8-267">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-267">Six digits</span></span> 
    
- <span data-ttu-id="328b8-268">하나의 인스턴스는 다음 중 하나:</span><span class="sxs-lookup"><span data-stu-id="328b8-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="328b8-269">더하기 기호</span><span class="sxs-lookup"><span data-stu-id="328b8-269">Plus symbol</span></span>
    
  - <span data-ttu-id="328b8-270">빼기 기호</span><span class="sxs-lookup"><span data-stu-id="328b8-270">Minus symbol</span></span>
    
  - <span data-ttu-id="328b8-271">"A" 문자 (대 소문자 구분 안함)</span><span class="sxs-lookup"><span data-stu-id="328b8-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="328b8-272">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-272">Three digits</span></span>
    
- <span data-ttu-id="328b8-273">하나의 문자 또는 한 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="328b8-274">체크섬</span><span class="sxs-lookup"><span data-stu-id="328b8-274">Checksum</span></span>

<span data-ttu-id="328b8-275">예</span><span class="sxs-lookup"><span data-stu-id="328b8-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="328b8-276">정의</span><span class="sxs-lookup"><span data-stu-id="328b8-276">Definition</span></span>

<span data-ttu-id="328b8-277">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-278">다음은 함수 `Func_finland_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="328b8-279">키워드에서 `Keywords_finland_eu_ssn_or_equivalent` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="328b8-280">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-281">다음은 함수 `Func_finland_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="328b8-282">키워드</span><span class="sxs-lookup"><span data-stu-id="328b8-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="328b8-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="328b8-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="328b8-284">identification number
</span><span class="sxs-lookup"><span data-stu-id="328b8-284">identification number</span></span>
  
<span data-ttu-id="328b8-285">개인 id</span><span class="sxs-lookup"><span data-stu-id="328b8-285">personal id</span></span>
  
<span data-ttu-id="328b8-286">identity 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-286">identity number</span></span>
  
<span data-ttu-id="328b8-287">핀란드 국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-287">finnish national id number</span></span>
  
<span data-ttu-id="328b8-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-288">personalidnumber#</span></span>
  
<span data-ttu-id="328b8-289">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-289">national identification number</span></span>
  
<span data-ttu-id="328b8-290">id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-290">id number</span></span>
  
<span data-ttu-id="328b8-291">국가 id 없습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-291">national id no.</span></span>
  
<span data-ttu-id="328b8-292">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-292">national id number</span></span>
  
<span data-ttu-id="328b8-293">id 없음</span><span class="sxs-lookup"><span data-stu-id="328b8-293">id no</span></span>
  
<span data-ttu-id="328b8-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="328b8-294">tunnistenumero</span></span>
  
<span data-ttu-id="328b8-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="328b8-295">henkilötunnus</span></span>
  
<span data-ttu-id="328b8-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="328b8-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="328b8-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="328b8-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="328b8-298">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="328b8-298">identiteetti numero</span></span>
  
<span data-ttu-id="328b8-299">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="328b8-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="328b8-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="328b8-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="328b8-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="328b8-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="328b8-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="328b8-302">tunnusnumero</span></span>
  
<span data-ttu-id="328b8-303">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="328b8-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="328b8-304">hetu</span><span class="sxs-lookup"><span data-stu-id="328b8-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="328b8-305">프랑스</span><span class="sxs-lookup"><span data-stu-id="328b8-305">France</span></span>

<span data-ttu-id="328b8-306">자세한 내용은의 섹션을 참조 "프랑스 사회보장 번호 (INSEE)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="328b8-307">독일</span><span class="sxs-lookup"><span data-stu-id="328b8-307">Germany</span></span>

<span data-ttu-id="328b8-308">자세한 내용은의 섹션을 참조 "독일 Id 카드 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="328b8-309">그리스</span><span class="sxs-lookup"><span data-stu-id="328b8-309">Greece</span></span>

<span data-ttu-id="328b8-310">자세한 내용은의 섹션을 참조 "그리스 국가 ID 카드" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="328b8-311">헝가리</span><span class="sxs-lookup"><span data-stu-id="328b8-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="328b8-312">형식</span><span class="sxs-lookup"><span data-stu-id="328b8-312">Format</span></span>

<span data-ttu-id="328b8-313">공백 및 구분 기호 없이 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="328b8-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="328b8-314">패턴</span><span class="sxs-lookup"><span data-stu-id="328b8-314">Pattern</span></span>

<span data-ttu-id="328b8-315">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="328b8-316">체크섬</span><span class="sxs-lookup"><span data-stu-id="328b8-316">Checksum</span></span>

<span data-ttu-id="328b8-317">예</span><span class="sxs-lookup"><span data-stu-id="328b8-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="328b8-318">정의</span><span class="sxs-lookup"><span data-stu-id="328b8-318">Definition</span></span>

<span data-ttu-id="328b8-319">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-320">다음은 함수 `Func_hungary_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="328b8-321">키워드에서 `Keywords_hungary_eu_ssn_or_equivalent` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="328b8-322">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-323">다음은 함수 `Func_hungary_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="328b8-324">키워드</span><span class="sxs-lookup"><span data-stu-id="328b8-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="328b8-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="328b8-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="328b8-326">헝가리어 사회보장 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-326">hungarian social security number</span></span>
  
<span data-ttu-id="328b8-327">social security number
</span><span class="sxs-lookup"><span data-stu-id="328b8-327">social security number</span></span>
  
<span data-ttu-id="328b8-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="328b8-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="328b8-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="328b8-329">hssn#</span></span>
  
<span data-ttu-id="328b8-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="328b8-330">socialsecuritynno</span></span>
  
<span data-ttu-id="328b8-331">hssn</span><span class="sxs-lookup"><span data-stu-id="328b8-331">hssn</span></span>
  
<span data-ttu-id="328b8-332">taj</span><span class="sxs-lookup"><span data-stu-id="328b8-332">taj</span></span>
  
<span data-ttu-id="328b8-333">taj #</span><span class="sxs-lookup"><span data-stu-id="328b8-333">taj#</span></span>
  
<span data-ttu-id="328b8-334">ssn</span><span class="sxs-lookup"><span data-stu-id="328b8-334">ssn</span></span>
  
<span data-ttu-id="328b8-335">ssn #</span><span class="sxs-lookup"><span data-stu-id="328b8-335">ssn#</span></span>
  
<span data-ttu-id="328b8-336">주민등록 없음</span><span class="sxs-lookup"><span data-stu-id="328b8-336">social security no</span></span>
  
<span data-ttu-id="328b8-337">áfa</span><span class="sxs-lookup"><span data-stu-id="328b8-337">áfa</span></span>
  
<span data-ttu-id="328b8-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="328b8-338">közösségi adószám</span></span>
  
<span data-ttu-id="328b8-339">általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="328b8-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="328b8-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="328b8-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="328b8-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="328b8-341">áfa szám</span></span>
  
<span data-ttu-id="328b8-342">magyar áfa szám</span><span class="sxs-lookup"><span data-stu-id="328b8-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="328b8-343">포르투갈</span><span class="sxs-lookup"><span data-stu-id="328b8-343">Portugal</span></span>

<span data-ttu-id="328b8-344">자세한 내용은의 섹션을 참조 "포르투갈 시민 카드 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="328b8-345">스페인</span><span class="sxs-lookup"><span data-stu-id="328b8-345">Spain</span></span>

<span data-ttu-id="328b8-346">자세한 내용은의 섹션을 참조 "스페인 사회보장 번호 (SSN)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="328b8-347">스웨덴</span><span class="sxs-lookup"><span data-stu-id="328b8-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="328b8-348">형식</span><span class="sxs-lookup"><span data-stu-id="328b8-348">Format</span></span>

<span data-ttu-id="328b8-349">공백 및 구분 기호 없이 12 자리</span><span class="sxs-lookup"><span data-stu-id="328b8-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="328b8-350">패턴</span><span class="sxs-lookup"><span data-stu-id="328b8-350">Pattern</span></span>

<span data-ttu-id="328b8-351">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="328b8-351">12 digits:</span></span>
  
-  <span data-ttu-id="328b8-352">생일 (YYYYMMDD)에 해당 하는 8 개의 자릿수</span><span class="sxs-lookup"><span data-stu-id="328b8-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="328b8-353">일련 번호에 해당 하는 세 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="328b8-354">일련번호에서 마지막 숫자 1 여자 2 남자 하는 것이 홀수와 짝수 탑재에 대 한 할당 하 여 성별을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="328b8-355">1990, 최대 일련번호의 배정에 상응는 국가 번호의 bearer 출생 하거나 (1947 하기 전에 태어난) 하는 경우 여기에서 자신이 명의 된 살고 있는, 세금 레코드에 따라 1947, 1 월 1에서 특수 코드 (일반적으로 7 자리 수로 9)에 대 한 immigrants</span><span class="sxs-lookup"><span data-stu-id="328b8-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="328b8-356">하나 이상의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="328b8-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="328b8-357">체크섬</span><span class="sxs-lookup"><span data-stu-id="328b8-357">Checksum</span></span>

<span data-ttu-id="328b8-358">예</span><span class="sxs-lookup"><span data-stu-id="328b8-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="328b8-359">정의</span><span class="sxs-lookup"><span data-stu-id="328b8-359">Definition</span></span>

<span data-ttu-id="328b8-360">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-361">다음은 함수 `Func_sweden_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="328b8-362">키워드에서 `Keywords_sweden_eu_ssn_or_equivalent` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="328b8-363">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="328b8-364">다음은 함수 `Func_sweden_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="328b8-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="328b8-365">키워드</span><span class="sxs-lookup"><span data-stu-id="328b8-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="328b8-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="328b8-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="328b8-367">개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="328b8-367">personal id number</span></span>
  
<span data-ttu-id="328b8-368">identification number
</span><span class="sxs-lookup"><span data-stu-id="328b8-368">identification number</span></span>
  
<span data-ttu-id="328b8-369">개인 id 없음</span><span class="sxs-lookup"><span data-stu-id="328b8-369">personal id no</span></span>
  
<span data-ttu-id="328b8-370">identity 없음</span><span class="sxs-lookup"><span data-stu-id="328b8-370">identity no</span></span>
  
<span data-ttu-id="328b8-371">식별 없음</span><span class="sxs-lookup"><span data-stu-id="328b8-371">identification no</span></span>
  
<span data-ttu-id="328b8-372">개인 식별 없음</span><span class="sxs-lookup"><span data-stu-id="328b8-372">personal identification no</span></span>
  
<span data-ttu-id="328b8-373">personnummer id</span><span class="sxs-lookup"><span data-stu-id="328b8-373">personnummer id</span></span>
  
<span data-ttu-id="328b8-374">personligt id nummer</span><span class="sxs-lookup"><span data-stu-id="328b8-374">personligt id-nummer</span></span>
  
<span data-ttu-id="328b8-375">unikt id nummer</span><span class="sxs-lookup"><span data-stu-id="328b8-375">unikt id-nummer</span></span>
  
<span data-ttu-id="328b8-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="328b8-376">personnummer</span></span>
  
<span data-ttu-id="328b8-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="328b8-377">identifikationsnumret</span></span>
  
<span data-ttu-id="328b8-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="328b8-378">personnummer#</span></span>
  
<span data-ttu-id="328b8-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="328b8-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="328b8-380">참고 항목</span><span class="sxs-lookup"><span data-stu-id="328b8-380">See also</span></span>

[<span data-ttu-id="328b8-381">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="328b8-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

