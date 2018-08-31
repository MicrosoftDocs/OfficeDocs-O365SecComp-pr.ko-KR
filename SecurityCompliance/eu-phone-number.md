---
title: EU 전화번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1c90ca41-1681-46bf-8ad6-6bf4cec5c426
description: Office 365 보안에서 데이터 손실 방지 (DLP) &amp; 준수 센터 DLP 정책에서 사용 하 여 사용할 수 있는 많은 중요 한 정보 유형을 포함 합니다. 이 항목에서는 EU 전화번호 중요 한 정보 유형에 설명 합니다.
ms.openlocfilehash: 9dd878e3385312982f9f3a4927205e3ebb27aabb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533571"
---
# <a name="eu-phone-number"></a><span data-ttu-id="728e6-104">EU 전화번호</span><span class="sxs-lookup"><span data-stu-id="728e6-104">EU Phone Number</span></span>

<span data-ttu-id="728e6-p102">Office 365 보안에서 데이터 손실 방지 (DLP) &amp; 준수 센터 DLP 정책에서 사용 하 여 사용할 수 있는 많은 중요 한 정보 유형을 포함 합니다. 이 항목에서는 EU 전화번호 중요 한 정보 유형에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="728e6-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="728e6-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="728e6-108">형식</span><span class="sxs-lookup"><span data-stu-id="728e6-108">Format</span></span>

<span data-ttu-id="728e6-109">없음 표준 길이</span><span class="sxs-lookup"><span data-stu-id="728e6-109">No standard length</span></span>
  
### <a name="pattern"></a><span data-ttu-id="728e6-110">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-110">Pattern</span></span>

- <span data-ttu-id="728e6-111">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-111">Digits</span></span> 
    
- <span data-ttu-id="728e6-112">휴대폰 번호만 숫자 "6"로 시작</span><span class="sxs-lookup"><span data-stu-id="728e6-112">Only mobile phone numbers begin with the digit "6"</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-113">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-113">Checksum</span></span>

<span data-ttu-id="728e6-114">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-114">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-115">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-115">Definition</span></span>

<span data-ttu-id="728e6-116">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-117">정규식 `Regex_austria_eu_telephone_number_1` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-117">The regular expression  `Regex_austria_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-118">키워드에서 `Keywords_austria_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-118">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-119">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-119">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-120">정규식 `Regex_austria_eu_telephone_number_2` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-120">The regular expression  `Regex_austria_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-121">키워드에서 `Keywords_austria_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-121">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_1" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_2" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_2" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="728e6-122">벨기에</span><span class="sxs-lookup"><span data-stu-id="728e6-122">Belgium</span></span>

### <a name="definition"></a><span data-ttu-id="728e6-123">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-123">Definition</span></span>

<span data-ttu-id="728e6-124">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-125">정규식 `Regex_belgium_eu_telephone_number_1` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-125">The regular expression  `Regex_belgium_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-126">키워드에서 `Keywords_belgium_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-126">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-127">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-127">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-128">정규식 `Regex_belgium_eu_telephone_number_2` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-128">The regular expression  `Regex_belgium_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-129">키워드에서 `Keywords_belgium_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-129">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_1" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_2" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_2" />
          </Pattern></Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="728e6-130">불가리아</span><span class="sxs-lookup"><span data-stu-id="728e6-130">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-131">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-131">Pattern</span></span>

- <span data-ttu-id="728e6-132">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-132">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-133">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-133">Checksum</span></span>

<span data-ttu-id="728e6-134">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-134">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-135">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-135">Definition</span></span>

<span data-ttu-id="728e6-136">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-137">정규식 `Regex_bulgaria_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-137">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-138">키워드에서 `Keywords_bulgaria_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-138">A keyword from  `Keywords_bulgaria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-139">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-139">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-140">정규식 `Regex_bulgaria_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-140">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_telephone_number" />
          <Match idRef="Keywords_bulgaria_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_bulgaria_eu_formatted_telephone_number" />
          </Pattern>
          
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="728e6-141">크로아티아</span><span class="sxs-lookup"><span data-stu-id="728e6-141">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-142">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-142">Pattern</span></span>

- <span data-ttu-id="728e6-143">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-144">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-144">Checksum</span></span>

<span data-ttu-id="728e6-145">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-146">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-146">Definition</span></span>

<span data-ttu-id="728e6-147">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-148">정규식 `Regex_croatia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-148">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-149">키워드에서 `Keywords_croatia_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-149">A keyword from  `Keywords_croatia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-150">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-150">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-151">정규식 `Regex_croatia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-151">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_telephone_number" />
          <Match idRef="Keywords_croatia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_croatia_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="cyprus"></a><span data-ttu-id="728e6-152">키프로스</span><span class="sxs-lookup"><span data-stu-id="728e6-152">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-153">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-153">Pattern</span></span>

- <span data-ttu-id="728e6-154">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-154">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-155">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-155">Checksum</span></span>

<span data-ttu-id="728e6-156">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-156">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-157">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-157">Definition</span></span>

<span data-ttu-id="728e6-158">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-159">정규식 `Regex_cyprus_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-159">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-160">키워드에서 `Keywords_cyprus_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-160">A keyword from  `Keywords_cyprus_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-161">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-161">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-162">정규식 `Regex_cyprus_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-162">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_telephone_number" />
          <Match idRef="Keywords_cyprus_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_cyprus_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="728e6-163">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="728e6-163">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-164">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-164">Pattern</span></span>

- <span data-ttu-id="728e6-165">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-165">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-166">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-166">Checksum</span></span>

<span data-ttu-id="728e6-167">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-167">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-168">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-168">Definition</span></span>

<span data-ttu-id="728e6-169">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-169">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-170">정규식 `Regex_czech_republic_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-170">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-171">키워드에서 `Keywords_czech_republic_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-171">A keyword from  `Keywords_czech_republic_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-172">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-172">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-173">정규식 `Regex_czech_republic_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-173">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_telephone_number" />
          <Match idRef="Keywords_czech_republic_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_czech_republic_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="denmark"></a><span data-ttu-id="728e6-174">덴마크</span><span class="sxs-lookup"><span data-stu-id="728e6-174">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-175">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-175">Pattern</span></span>

- <span data-ttu-id="728e6-176">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-176">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-177">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-177">Checksum</span></span>

<span data-ttu-id="728e6-178">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-178">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-179">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-179">Definition</span></span>

<span data-ttu-id="728e6-180">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-180">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-181">정규식 `Regex_denmark_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-181">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-182">키워드에서 `Keywords_denmark_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-182">A keyword from  `Keywords_denmark_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-183">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-184">정규식 `Regex_denmark_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-184">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_telephone_number" />
          <Match idRef="Keywords_denmark_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_denmark_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="estonia"></a><span data-ttu-id="728e6-185">에스토니아</span><span class="sxs-lookup"><span data-stu-id="728e6-185">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-186">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-186">Pattern</span></span>

- <span data-ttu-id="728e6-187">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-187">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-188">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-188">Checksum</span></span>

<span data-ttu-id="728e6-189">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-189">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-190">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-190">Definition</span></span>

<span data-ttu-id="728e6-191">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-191">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-192">정규식 `Regex_estonia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-192">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-193">키워드에서 `Keywords_estonia_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-193">A keyword from  `Keywords_estonia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-194">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-195">정규식 `Regex_estonia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-195">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_telephone_number" />
          <Match idRef="Keywords_estonia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_estonia_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="finland"></a><span data-ttu-id="728e6-196">핀란드</span><span class="sxs-lookup"><span data-stu-id="728e6-196">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-197">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-197">Pattern</span></span>

- <span data-ttu-id="728e6-198">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-198">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-199">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-199">Checksum</span></span>

<span data-ttu-id="728e6-200">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-200">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-201">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-201">Definition</span></span>

<span data-ttu-id="728e6-202">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-203">정규식 `Regex_finland_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-203">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-204">키워드에서 `Keywords_finland_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-204">A keyword from  `Keywords_finland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-205">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-205">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-206">정규식 `Regex_finland_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-206">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_telephone_number" />
          <Match idRef="Keywords_finland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_finland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="728e6-207">프랑스</span><span class="sxs-lookup"><span data-stu-id="728e6-207">France</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-208">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-208">Pattern</span></span>

- <span data-ttu-id="728e6-209">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-209">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-210">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-210">Checksum</span></span>

<span data-ttu-id="728e6-211">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-211">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-212">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-212">Definition</span></span>

<span data-ttu-id="728e6-213">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-213">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-214">정규식 `Regex_france_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-214">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-215">키워드에서 `Keywords_france_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-215">A keyword from  `Keywords_france_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-216">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-217">정규식 `Regex_france_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-217">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_telephone_number" />
          <Match idRef="Keywords_france_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_france_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="germany"></a><span data-ttu-id="728e6-218">독일</span><span class="sxs-lookup"><span data-stu-id="728e6-218">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-219">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-219">Pattern</span></span>

- <span data-ttu-id="728e6-220">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-220">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-221">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-221">Checksum</span></span>

<span data-ttu-id="728e6-222">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-222">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-223">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-223">Definition</span></span>

<span data-ttu-id="728e6-224">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-224">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-225">정규식 `Regex_germany_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-225">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-226">키워드에서 `Keywords_germany_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-226">A keyword from  `Keywords_germany_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-227">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-228">정규식 `Regex_germany_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-228">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_telephone_number" />
          <Match idRef="Keywords_germany_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_germany_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="greece"></a><span data-ttu-id="728e6-229">그리스</span><span class="sxs-lookup"><span data-stu-id="728e6-229">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-230">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-230">Pattern</span></span>

- <span data-ttu-id="728e6-231">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-231">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-232">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-232">Checksum</span></span>

<span data-ttu-id="728e6-233">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-233">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-234">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-234">Definition</span></span>

<span data-ttu-id="728e6-235">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-235">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-236">정규식 `Regex_greece_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-236">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-237">키워드에서 `Keywords_greece_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-237">A keyword from  `Keywords_greece_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-238">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-238">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-239">정규식 `Regex_greece_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-239">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_telephone_number" />
          <Match idRef="Keywords_greece_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_greece_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="hungary"></a><span data-ttu-id="728e6-240">헝가리</span><span class="sxs-lookup"><span data-stu-id="728e6-240">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-241">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-241">Pattern</span></span>

- <span data-ttu-id="728e6-242">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-242">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-243">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-243">Checksum</span></span>

<span data-ttu-id="728e6-244">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-244">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-245">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-245">Definition</span></span>

<span data-ttu-id="728e6-246">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-247">정규식 `Regex_hungary_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-247">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-248">키워드에서 `Keywords_hungary_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-248">A keyword from  `Keywords_hungary_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-249">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-250">정규식 `Regex_hungary_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-250">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_telephone_number" />
          <Match idRef="Keywords_hungary_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_hungary_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="ireland"></a><span data-ttu-id="728e6-251">Ireland</span><span class="sxs-lookup"><span data-stu-id="728e6-251">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-252">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-252">Pattern</span></span>

- <span data-ttu-id="728e6-253">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-254">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-254">Checksum</span></span>

<span data-ttu-id="728e6-255">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-256">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-256">Definition</span></span>

<span data-ttu-id="728e6-257">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-258">정규식 `Regex_ireland_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-258">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-259">키워드에서 `Keywords_ireland_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-259">A keyword from  `Keywords_ireland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-260">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-261">정규식 `Regex_ireland_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-261">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_telephone_number" />
          <Match idRef="Keywords_ireland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_ireland_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="italy"></a><span data-ttu-id="728e6-262">이탈리아</span><span class="sxs-lookup"><span data-stu-id="728e6-262">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-263">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-263">Pattern</span></span>

- <span data-ttu-id="728e6-264">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-264">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-265">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-265">Checksum</span></span>

<span data-ttu-id="728e6-266">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-266">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-267">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-267">Definition</span></span>

<span data-ttu-id="728e6-268">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-268">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-269">정규식 `Regex_italy_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-269">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-270">키워드에서 `Keywords_italy_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-270">A keyword from  `Keywords_italy_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-271">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-272">정규식 `Regex_italy_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-272">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_telephone_number" />
          <Match idRef="Keywords_italy_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_italy_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="latvia"></a><span data-ttu-id="728e6-273">라트비아</span><span class="sxs-lookup"><span data-stu-id="728e6-273">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-274">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-274">Pattern</span></span>

- <span data-ttu-id="728e6-275">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-275">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-276">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-276">Checksum</span></span>

<span data-ttu-id="728e6-277">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-277">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-278">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-278">Definition</span></span>

<span data-ttu-id="728e6-279">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-279">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-280">정규식 `Regex_latvia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-280">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-281">키워드에서 `Keywords_latvia_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-281">A keyword from  `Keywords_latvia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-282">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-283">정규식 `Regex_latvia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-283">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_telephone_number" />
          <Match idRef="Keywords_latvia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_latvia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="lithuania"></a><span data-ttu-id="728e6-284">리투아니아</span><span class="sxs-lookup"><span data-stu-id="728e6-284">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-285">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-285">Pattern</span></span>

- <span data-ttu-id="728e6-286">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-286">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-287">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-287">Checksum</span></span>

<span data-ttu-id="728e6-288">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-288">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-289">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-289">Definition</span></span>

<span data-ttu-id="728e6-290">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-291">정규식 `Regex_lithuania_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-291">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-292">키워드에서 `Keywords_lithuania_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-292">A keyword from  `Keywords_lithuania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-293">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-293">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-294">정규식 `Regex_lithuania_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-294">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_telephone_number" />
          <Match idRef="Keywords_lithuania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_lithuania_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="728e6-295">룩셈부르크</span><span class="sxs-lookup"><span data-stu-id="728e6-295">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-296">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-296">Pattern</span></span>

- <span data-ttu-id="728e6-297">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-297">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-298">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-298">Checksum</span></span>

<span data-ttu-id="728e6-299">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-299">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-300">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-300">Definition</span></span>

<span data-ttu-id="728e6-301">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-302">정규식 `Regex_luxemburg_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-302">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-303">키워드에서 `Keywords_luxemburg_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-303">A keyword from  `Keywords_luxemburg_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-304">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-304">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-305">정규식 `Regex_luxemburg_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-305">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_telephone_number" />
          <Match idRef="Keywords_luxemburg_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_luxemburg_eu_formatted_telephone_number" />
                  </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="728e6-306">몰타</span><span class="sxs-lookup"><span data-stu-id="728e6-306">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-307">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-307">Pattern</span></span>

- <span data-ttu-id="728e6-308">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-308">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-309">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-309">Checksum</span></span>

<span data-ttu-id="728e6-310">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-310">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-311">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-311">Definition</span></span>

<span data-ttu-id="728e6-312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-313">정규식 `Regex_malta_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-313">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-314">키워드에서 `Keywords_malta_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-314">A keyword from  `Keywords_malta_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-315">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-315">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-316">정규식 `Regex_malta_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-316">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_telephone_number" />
          <Match idRef="Keywords_malta_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_malta_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="728e6-317">네덜란드</span><span class="sxs-lookup"><span data-stu-id="728e6-317">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-318">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-318">Pattern</span></span>

- <span data-ttu-id="728e6-319">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-319">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-320">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-320">Checksum</span></span>

<span data-ttu-id="728e6-321">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-321">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-322">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-322">Definition</span></span>

<span data-ttu-id="728e6-323">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-323">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-324">정규식 `Regex_netherlands_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-324">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-325">키워드에서 `Keywords_netherlands_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-325">A keyword from  `Keywords_netherlands_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-326">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-327">정규식 `Regex_netherlands_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-327">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_telephone_number" />
          <Match idRef="Keywords_netherlands_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_netherlands_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="728e6-328">폴란드</span><span class="sxs-lookup"><span data-stu-id="728e6-328">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-329">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-329">Pattern</span></span>

- <span data-ttu-id="728e6-330">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-330">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-331">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-331">Checksum</span></span>

<span data-ttu-id="728e6-332">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-332">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-333">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-333">Definition</span></span>

<span data-ttu-id="728e6-334">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-334">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-335">정규식 `Regex_poland_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-335">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-336">키워드에서 `Keywords_poland_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-336">A keyword from  `Keywords_poland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-337">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-338">정규식 `Regex_poland_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-338">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_telephone_number" />
          <Match idRef="Keywords_poland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_poland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="728e6-339">포르투갈</span><span class="sxs-lookup"><span data-stu-id="728e6-339">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-340">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-340">Pattern</span></span>

- <span data-ttu-id="728e6-341">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-341">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-342">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-342">Checksum</span></span>

<span data-ttu-id="728e6-343">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-343">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-344">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-344">Definition</span></span>

<span data-ttu-id="728e6-345">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-345">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-346">정규식 `Regex_portugal_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-346">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-347">키워드에서 `Keywords_portugal_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-347">A keyword from  `Keywords_portugal_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-348">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-348">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-349">정규식 `Regex_portugal_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-349">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_telephone_number" />
          <Match idRef="Keywords_portugal_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_portugal_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="romania"></a><span data-ttu-id="728e6-350">루마니아</span><span class="sxs-lookup"><span data-stu-id="728e6-350">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-351">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-351">Pattern</span></span>

- <span data-ttu-id="728e6-352">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-352">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-353">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-353">Checksum</span></span>

<span data-ttu-id="728e6-354">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-354">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-355">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-355">Definition</span></span>

<span data-ttu-id="728e6-356">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-356">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-357">정규식 `Regex_romania_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-357">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-358">키워드에서 `Keywords_romania_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-358">A keyword from  `Keywords_romania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-359">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-359">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-360">정규식 `Regex_romania_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-360">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_telephone_number" />
          <Match idRef="Keywords_romania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_romania_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="728e6-361">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="728e6-361">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-362">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-362">Pattern</span></span>

- <span data-ttu-id="728e6-363">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-364">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-364">Checksum</span></span>

<span data-ttu-id="728e6-365">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-366">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-366">Definition</span></span>

<span data-ttu-id="728e6-367">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-368">정규식 `Regex_slovakia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-368">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-369">키워드에서 `Keywords_slovakia_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-369">A keyword from  `Keywords_slovakia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-370">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-370">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-371">정규식 `Regex_slovakia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-371">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_telephone_number" />
          <Match idRef="Keywords_slovakia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovakia_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="728e6-372">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="728e6-372">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-373">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-373">Pattern</span></span>

- <span data-ttu-id="728e6-374">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-374">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-375">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-375">Checksum</span></span>

<span data-ttu-id="728e6-376">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-377">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-377">Definition</span></span>

<span data-ttu-id="728e6-378">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-379">정규식 `Regex_slovenia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-379">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-380">키워드에서 `Keywords_slovenia_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-380">A keyword from  `Keywords_slovenia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-381">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-382">정규식 `Regex_slovenia_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-382">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_telephone_number" />
          <Match idRef="Keywords_slovenia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovenia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="spain"></a><span data-ttu-id="728e6-383">스페인</span><span class="sxs-lookup"><span data-stu-id="728e6-383">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-384">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-384">Pattern</span></span>

- <span data-ttu-id="728e6-385">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-385">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-386">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-386">Checksum</span></span>

<span data-ttu-id="728e6-387">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-387">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-388">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-388">Definition</span></span>

<span data-ttu-id="728e6-389">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-390">정규식 `Regex_spain_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-390">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-391">키워드에서 `Keywords_spain_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-391">A keyword from  `Keywords_spain_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-392">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-392">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-393">정규식 `Regex_spain_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-393">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_telephone_number" />
          <Match idRef="Keywords_spain_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_spain_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="sweden"></a><span data-ttu-id="728e6-394">스웨덴</span><span class="sxs-lookup"><span data-stu-id="728e6-394">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-395">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-395">Pattern</span></span>

- <span data-ttu-id="728e6-396">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-396">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-397">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-397">Checksum</span></span>

<span data-ttu-id="728e6-398">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-398">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-399">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-399">Definition</span></span>

<span data-ttu-id="728e6-400">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-400">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-401">정규식 `Regex_sweden_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-401">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-402">키워드에서 `Keywords_sweden_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-402">A keyword from  `Keywords_sweden_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-403">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-404">정규식 `Regex_sweden_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-404">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_telephone_number" />
          <Match idRef="Keywords_sweden_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_sweden_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="uk"></a><span data-ttu-id="728e6-405">영국</span><span class="sxs-lookup"><span data-stu-id="728e6-405">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="728e6-406">패턴</span><span class="sxs-lookup"><span data-stu-id="728e6-406">Pattern</span></span>

- <span data-ttu-id="728e6-407">숫자</span><span class="sxs-lookup"><span data-stu-id="728e6-407">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="728e6-408">체크섬</span><span class="sxs-lookup"><span data-stu-id="728e6-408">Checksum</span></span>

<span data-ttu-id="728e6-409">해당 없음</span><span class="sxs-lookup"><span data-stu-id="728e6-409">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="728e6-410">정의</span><span class="sxs-lookup"><span data-stu-id="728e6-410">Definition</span></span>

<span data-ttu-id="728e6-411">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-412">정규식 `Regex_uk_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-412">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="728e6-413">키워드에서 `Keywords_uk_eu_telephone_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-413">A keyword from  `Keywords_uk_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="728e6-414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="728e6-415">정규식 `Regex_uk_eu_telephone_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="728e6-415">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_telephone_number" />
          <Match idRef="Keywords_uk_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_uk_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="728e6-416">참고 항목</span><span class="sxs-lookup"><span data-stu-id="728e6-416">See also</span></span>

[<span data-ttu-id="728e6-417">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="728e6-417">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

