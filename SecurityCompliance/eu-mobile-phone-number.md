---
title: EU 휴대폰 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Office 365 보안에서 데이터 손실 방지 (DLP) &amp; 준수 센터 DLP 정책에서 사용 하 여 사용할 수 있는 많은 중요 한 정보 유형을 포함 합니다. 이 항목에서는 EU 휴대폰 번호 중요 한 정보 유형에 설명 합니다.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533403"
---
# <a name="eu-mobile-phone-number"></a><span data-ttu-id="a9b31-104">EU 휴대폰 번호</span><span class="sxs-lookup"><span data-stu-id="a9b31-104">EU Mobile Phone Number</span></span>

<span data-ttu-id="a9b31-p102">Office 365 보안에서 데이터 손실 방지 (DLP) &amp; 준수 센터 DLP 정책에서 사용 하 여 사용할 수 있는 많은 중요 한 정보 유형을 포함 합니다. 이 항목에서는 EU 휴대폰 번호 중요 한 정보 유형에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Mobile Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="a9b31-107">오스트리아</span><span class="sxs-lookup"><span data-stu-id="a9b31-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="a9b31-108">형식</span><span class="sxs-lookup"><span data-stu-id="a9b31-108">Format</span></span>

<span data-ttu-id="a9b31-109">표준 길이 없이 자릿수</span><span class="sxs-lookup"><span data-stu-id="a9b31-109">Digits without standard lengths</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a9b31-110">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-110">Pattern</span></span>

-  <span data-ttu-id="a9b31-111">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-111">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="a9b31-112">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-112">Definition</span></span>

<span data-ttu-id="a9b31-113">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-113">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-114">정규식 `Regex_austria_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-114">The regular expression  `Regex_austria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-115">정규식 `Regex_austria_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-115">The regular expression  `Regex_austria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-116">키워드에서 `Keywords_austria_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-116">A keyword from  `Keywords_austria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="a9b31-117">벨기에</span><span class="sxs-lookup"><span data-stu-id="a9b31-117">Belgium</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-118">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-118">Pattern</span></span>

-  <span data-ttu-id="a9b31-119">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-119">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="a9b31-120">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-120">Definition</span></span>

<span data-ttu-id="a9b31-121">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-122">정규식 `Regex_belgium_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-122">The regular expression  `Regex_belgium_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-123">정규식 `Regex_belgium_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-123">The regular expression  `Regex_belgium_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-124">키워드에서 `Keywords_belgium_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-124">A keyword from  `Keywords_belgium_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="a9b31-125">불가리아</span><span class="sxs-lookup"><span data-stu-id="a9b31-125">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-126">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-126">Pattern</span></span>

-  <span data-ttu-id="a9b31-127">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-127">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="a9b31-128">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-128">Definition</span></span>

<span data-ttu-id="a9b31-129">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-129">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-130">정규식 `Regex_bulgaria_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-130">The regular expression  `Regex_bulgaria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-131">정규식 `Regex_bulgaria_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-131">The regular expression  `Regex_bulgaria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-132">키워드에서 `Keywords_bulgaria_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-132">A keyword from  `Keywords_bulgaria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="a9b31-133">크로아티아</span><span class="sxs-lookup"><span data-stu-id="a9b31-133">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-134">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-134">Pattern</span></span>

-  <span data-ttu-id="a9b31-135">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-135">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="a9b31-136">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-136">Definition</span></span>

<span data-ttu-id="a9b31-137">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-138">정규식 `Regex_croatia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-138">The regular expression  `Regex_croatia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-139">정규식 `Regex_croatia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-139">The regular expression  `Regex_croatia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-140">키워드에서 `Keywords_croatia_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-140">A keyword from  `Keywords_croatia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a><span data-ttu-id="a9b31-141">키프로스</span><span class="sxs-lookup"><span data-stu-id="a9b31-141">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-142">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-142">Pattern</span></span>

-  <span data-ttu-id="a9b31-143">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-144">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-144">Checksum</span></span>

<span data-ttu-id="a9b31-145">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-146">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-146">Definition</span></span>

<span data-ttu-id="a9b31-147">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-148">정규식 `Regex_cyprus_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-148">The regular expression  `Regex_cyprus_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-149">정규식 `Regex_cyprus_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-149">The regular expression  `Regex_cyprus_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-150">키워드에서 `Keywords_cyprus_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-150">A keyword from  `Keywords_cyprus_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="a9b31-151">체코 공화국</span><span class="sxs-lookup"><span data-stu-id="a9b31-151">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-152">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-152">Pattern</span></span>

-  <span data-ttu-id="a9b31-153">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-153">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-154">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-154">Checksum</span></span>

<span data-ttu-id="a9b31-155">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-155">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-156">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-156">Definition</span></span>

<span data-ttu-id="a9b31-157">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-157">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-158">정규식 `Regex_czech_republic_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-158">The regular expression  `Regex_czech_republic_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-159">정규식 `Regex_czech_republic_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-159">The regular expression  `Regex_czech_republic_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-160">키워드에서 `Keywords_czech_republic_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-160">A keyword from  `Keywords_czech_republic_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a><span data-ttu-id="a9b31-161">덴마크</span><span class="sxs-lookup"><span data-stu-id="a9b31-161">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-162">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-162">Pattern</span></span>

-  <span data-ttu-id="a9b31-163">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-163">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-164">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-164">Checksum</span></span>

<span data-ttu-id="a9b31-165">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-165">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-166">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-166">Definition</span></span>

<span data-ttu-id="a9b31-167">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-167">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-168">정규식 `Regex_denmark_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-168">The regular expression  `Regex_denmark_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-169">정규식 `Regex_denmark_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-169">The regular expression  `Regex_denmark_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-170">키워드에서 `Keywords_denmark_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-170">A keyword from  `Keywords_denmark_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a><span data-ttu-id="a9b31-171">에스토니아</span><span class="sxs-lookup"><span data-stu-id="a9b31-171">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-172">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-172">Pattern</span></span>

-  <span data-ttu-id="a9b31-173">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-173">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-174">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-174">Checksum</span></span>

<span data-ttu-id="a9b31-175">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-175">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-176">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-176">Definition</span></span>

<span data-ttu-id="a9b31-177">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-177">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-178">정규식 `Regex_estonia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-178">The regular expression  `Regex_estonia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-179">정규식 `Regex_estonia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-179">The regular expression  `Regex_estonia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-180">키워드에서 `Keywords_estonia_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-180">A keyword from  `Keywords_estonia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a><span data-ttu-id="a9b31-181">핀란드</span><span class="sxs-lookup"><span data-stu-id="a9b31-181">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-182">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-182">Pattern</span></span>

-  <span data-ttu-id="a9b31-183">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-183">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-184">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-184">Checksum</span></span>

<span data-ttu-id="a9b31-185">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-185">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-186">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-186">Definition</span></span>

<span data-ttu-id="a9b31-187">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-187">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-188">정규식 `Regex_finland_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-188">The regular expression  `Regex_finland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-189">정규식 `Regex_finland_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-189">The regular expression  `Regex_finland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-190">키워드에서 `Keywords_finland_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-190">A keyword from  `Keywords_finland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="a9b31-191">프랑스</span><span class="sxs-lookup"><span data-stu-id="a9b31-191">France</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-192">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-192">Pattern</span></span>

-  <span data-ttu-id="a9b31-193">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-193">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-194">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-194">Checksum</span></span>

<span data-ttu-id="a9b31-195">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-195">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-196">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-196">Definition</span></span>

<span data-ttu-id="a9b31-197">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-197">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-198">정규식 `Regex_france_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-198">The regular expression  `Regex_france_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-199">정규식 `Regex_france_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-199">The regular expression  `Regex_france_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-200">키워드에서 `Keywords_france_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-200">A keyword from  `Keywords_france_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a><span data-ttu-id="a9b31-201">독일</span><span class="sxs-lookup"><span data-stu-id="a9b31-201">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-202">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-202">Pattern</span></span>

-  <span data-ttu-id="a9b31-203">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-203">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-204">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-204">Checksum</span></span>

<span data-ttu-id="a9b31-205">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-205">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-206">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-206">Definition</span></span>

<span data-ttu-id="a9b31-207">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-207">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-208">정규식 `Regex_germany_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-208">The regular expression  `Regex_germany_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-209">정규식 `Regex_germany_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-209">The regular expression  `Regex_germany_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-210">키워드에서 `Keywords_germany_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-210">A keyword from  `Keywords_germany_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a><span data-ttu-id="a9b31-211">그리스</span><span class="sxs-lookup"><span data-stu-id="a9b31-211">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-212">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-212">Pattern</span></span>

-  <span data-ttu-id="a9b31-213">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-213">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-214">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-214">Checksum</span></span>

<span data-ttu-id="a9b31-215">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-215">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-216">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-216">Definition</span></span>

<span data-ttu-id="a9b31-217">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-217">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-218">정규식 `Regex_greece_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-218">The regular expression  `Regex_greece_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-219">정규식 `Regex_greece_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-219">The regular expression  `Regex_greece_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-220">키워드에서 `Keywords_greece_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-220">A keyword from  `Keywords_greece_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a><span data-ttu-id="a9b31-221">헝가리</span><span class="sxs-lookup"><span data-stu-id="a9b31-221">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-222">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-222">Pattern</span></span>

-  <span data-ttu-id="a9b31-223">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-223">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-224">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-224">Checksum</span></span>

<span data-ttu-id="a9b31-225">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-225">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-226">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-226">Definition</span></span>

<span data-ttu-id="a9b31-227">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-228">정규식 `Regex_hungary_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-228">The regular expression  `Regex_hungary_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-229">정규식 `Regex_hungary_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-229">The regular expression  `Regex_hungary_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-230">키워드에서 `Keywords_hungary_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-230">A keyword from  `Keywords_hungary_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a><span data-ttu-id="a9b31-231">Ireland</span><span class="sxs-lookup"><span data-stu-id="a9b31-231">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-232">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-232">Pattern</span></span>

-  <span data-ttu-id="a9b31-233">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-233">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-234">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-234">Checksum</span></span>

<span data-ttu-id="a9b31-235">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-235">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-236">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-236">Definition</span></span>

<span data-ttu-id="a9b31-237">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-237">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-238">정규식 `Regex_ireland_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-238">The regular expression  `Regex_ireland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-239">정규식 `Regex_ireland_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-239">The regular expression  `Regex_ireland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-240">키워드에서 `Keywords_ireland_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-240">A keyword from  `Keywords_ireland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a><span data-ttu-id="a9b31-241">이탈리아</span><span class="sxs-lookup"><span data-stu-id="a9b31-241">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-242">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-242">Pattern</span></span>

-  <span data-ttu-id="a9b31-243">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-243">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-244">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-244">Checksum</span></span>

<span data-ttu-id="a9b31-245">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-245">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-246">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-246">Definition</span></span>

<span data-ttu-id="a9b31-247">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-248">정규식 `Regex_italy_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-248">The regular expression  `Regex_italy_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-249">정규식 `Regex_italy_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-249">The regular expression  `Regex_italy_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-250">키워드에서 `Keywords_italy_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-250">A keyword from  `Keywords_italy_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a><span data-ttu-id="a9b31-251">라트비아</span><span class="sxs-lookup"><span data-stu-id="a9b31-251">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-252">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-252">Pattern</span></span>

-  <span data-ttu-id="a9b31-253">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-254">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-254">Checksum</span></span>

<span data-ttu-id="a9b31-255">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-256">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-256">Definition</span></span>

<span data-ttu-id="a9b31-257">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-258">정규식 `Regex_latvia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-258">The regular expression  `Regex_latvia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-259">정규식 `Regex_latvia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-259">The regular expression  `Regex_latvia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-260">키워드에서 `Keywords_latvia_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-260">A keyword from  `Keywords_latvia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a><span data-ttu-id="a9b31-261">리투아니아</span><span class="sxs-lookup"><span data-stu-id="a9b31-261">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-262">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-262">Pattern</span></span>

-  <span data-ttu-id="a9b31-263">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-263">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-264">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-264">Checksum</span></span>

<span data-ttu-id="a9b31-265">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-265">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-266">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-266">Definition</span></span>

<span data-ttu-id="a9b31-267">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-268">정규식 `Regex_lithuania_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-268">The regular expression  `Regex_lithuania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-269">정규식 `Regex_lithuania_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-269">The regular expression  `Regex_lithuania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-270">키워드에서 `Keywords_lithuania_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-270">A keyword from  `Keywords_lithuania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="a9b31-271">룩셈부르크</span><span class="sxs-lookup"><span data-stu-id="a9b31-271">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-272">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-272">Pattern</span></span>

-  <span data-ttu-id="a9b31-273">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-273">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-274">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-274">Checksum</span></span>

<span data-ttu-id="a9b31-275">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-275">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-276">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-276">Definition</span></span>

<span data-ttu-id="a9b31-277">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-277">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-278">정규식 `Regex_luxumburg_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-278">The regular expression  `Regex_luxumburg_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-279">정규식 `Regex_luxumburg_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-279">The regular expression  `Regex_luxumburg_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-280">키워드에서 `Keywords_luxumburg_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-280">A keyword from  `Keywords_luxumburg_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="a9b31-281">몰타</span><span class="sxs-lookup"><span data-stu-id="a9b31-281">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-282">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-282">Pattern</span></span>

-  <span data-ttu-id="a9b31-283">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-283">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-284">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-284">Checksum</span></span>

<span data-ttu-id="a9b31-285">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-285">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-286">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-286">Definition</span></span>

<span data-ttu-id="a9b31-287">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-288">정규식 `Regex_malta_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-288">The regular expression  `Regex_malta_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-289">정규식 `Regex_malta_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-289">The regular expression  `Regex_malta_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-290">키워드에서 `Keywords_malta_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-290">A keyword from  `Keywords_malta_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="a9b31-291">네덜란드</span><span class="sxs-lookup"><span data-stu-id="a9b31-291">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-292">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-292">Pattern</span></span>

-  <span data-ttu-id="a9b31-293">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-293">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-294">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-294">Checksum</span></span>

<span data-ttu-id="a9b31-295">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-295">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-296">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-296">Definition</span></span>

<span data-ttu-id="a9b31-297">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-297">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-298">정규식 `Regex_netherlands_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-298">The regular expression  `Regex_netherlands_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-299">정규식 `Regex_netherlands_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-299">The regular expression  `Regex_netherlands_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-300">키워드에서 `Keywords_netherlands_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-300">A keyword from  `Keywords_netherlands_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="a9b31-301">폴란드</span><span class="sxs-lookup"><span data-stu-id="a9b31-301">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-302">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-302">Pattern</span></span>

-  <span data-ttu-id="a9b31-303">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-303">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-304">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-304">Checksum</span></span>

<span data-ttu-id="a9b31-305">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-305">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-306">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-306">Definition</span></span>

<span data-ttu-id="a9b31-307">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-308">정규식 `Regex_poland_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-308">The regular expression  `Regex_poland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-309">정규식 `Regex_poland_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-309">The regular expression  `Regex_poland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-310">키워드에서 `Keywords_poland_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-310">A keyword from  `Keywords_poland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="a9b31-311">포르투갈</span><span class="sxs-lookup"><span data-stu-id="a9b31-311">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-312">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-312">Pattern</span></span>

-  <span data-ttu-id="a9b31-313">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-313">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-314">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-314">Checksum</span></span>

<span data-ttu-id="a9b31-315">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-315">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-316">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-316">Definition</span></span>

<span data-ttu-id="a9b31-317">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-317">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-318">정규식 `Regex_portugal_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-318">The regular expression  `Regex_portugal_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-319">정규식 `Regex_portugal_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-319">The regular expression  `Regex_portugal_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-320">키워드에서 `Keywords_portugal_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-320">A keyword from  `Keywords_portugal_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a><span data-ttu-id="a9b31-321">루마니아</span><span class="sxs-lookup"><span data-stu-id="a9b31-321">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-322">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-322">Pattern</span></span>

-  <span data-ttu-id="a9b31-323">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-323">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-324">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-324">Checksum</span></span>

<span data-ttu-id="a9b31-325">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-325">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-326">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-326">Definition</span></span>

<span data-ttu-id="a9b31-327">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-327">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-328">정규식 `Regex_romania_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-328">The regular expression  `Regex_romania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-329">정규식 `Regex_romania_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-329">The regular expression  `Regex_romania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-330">키워드에서 `Keywords_romania_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-330">A keyword from  `Keywords_romania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="a9b31-331">슬로바키아</span><span class="sxs-lookup"><span data-stu-id="a9b31-331">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-332">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-332">Pattern</span></span>

-  <span data-ttu-id="a9b31-333">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-333">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-334">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-334">Checksum</span></span>

<span data-ttu-id="a9b31-335">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-335">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-336">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-336">Definition</span></span>

<span data-ttu-id="a9b31-337">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-338">정규식 `Regex_slovakia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-338">The regular expression  `Regex_slovakia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-339">정규식 `Regex_slovakia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-339">The regular expression  `Regex_slovakia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-340">키워드에서 `Keywords_slovakia_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-340">A keyword from  `Keywords_slovakia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="a9b31-341">슬로베니아</span><span class="sxs-lookup"><span data-stu-id="a9b31-341">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-342">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-342">Pattern</span></span>

-  <span data-ttu-id="a9b31-343">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-343">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-344">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-344">Checksum</span></span>

<span data-ttu-id="a9b31-345">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-345">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-346">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-346">Definition</span></span>

<span data-ttu-id="a9b31-347">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-347">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-348">정규식 `Regex_slovenia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-348">The regular expression  `Regex_slovenia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-349">정규식 `Regex_slovenia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-349">The regular expression  `Regex_slovenia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-350">키워드에서 `Keywords_slovenia_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-350">A keyword from  `Keywords_slovenia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a><span data-ttu-id="a9b31-351">스페인</span><span class="sxs-lookup"><span data-stu-id="a9b31-351">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-352">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-352">Pattern</span></span>

-  <span data-ttu-id="a9b31-353">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-353">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-354">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-354">Checksum</span></span>

<span data-ttu-id="a9b31-355">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-355">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-356">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-356">Definition</span></span>

<span data-ttu-id="a9b31-357">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-358">정규식 `Regex_spain_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-358">The regular expression  `Regex_spain_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-359">정규식 `Regex_spain_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-359">The regular expression  `Regex_spain_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-360">키워드에서 `Keywords_spain_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-360">A keyword from  `Keywords_spain_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a><span data-ttu-id="a9b31-361">스웨덴</span><span class="sxs-lookup"><span data-stu-id="a9b31-361">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-362">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-362">Pattern</span></span>

-  <span data-ttu-id="a9b31-363">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-364">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-364">Checksum</span></span>

<span data-ttu-id="a9b31-365">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-366">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-366">Definition</span></span>

<span data-ttu-id="a9b31-367">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-368">정규식 `Regex_sweden_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-368">The regular expression  `Regex_sweden_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-369">정규식 `Regex_sweden_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-369">The regular expression  `Regex_sweden_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-370">키워드에서 `Keywords_sweden_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-370">A keyword from  `Keywords_sweden_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a><span data-ttu-id="a9b31-371">영국</span><span class="sxs-lookup"><span data-stu-id="a9b31-371">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="a9b31-372">패턴</span><span class="sxs-lookup"><span data-stu-id="a9b31-372">Pattern</span></span>

-  <span data-ttu-id="a9b31-373">숫자</span><span class="sxs-lookup"><span data-stu-id="a9b31-373">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a9b31-374">체크섬</span><span class="sxs-lookup"><span data-stu-id="a9b31-374">Checksum</span></span>

<span data-ttu-id="a9b31-375">해당 없음</span><span class="sxs-lookup"><span data-stu-id="a9b31-375">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="a9b31-376">정의</span><span class="sxs-lookup"><span data-stu-id="a9b31-376">Definition</span></span>

<span data-ttu-id="a9b31-377">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-377">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a9b31-378">정규식 `Regex_uk_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-378">The regular expression  `Regex_uk_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-379">정규식 `Regex_uk_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-379">The regular expression  `Regex_uk_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a9b31-380">키워드에서 `Keywords_uk_eu_mobile_number` 를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b31-380">A keyword from  `Keywords_uk_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="a9b31-381">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a9b31-381">See also</span></span>

[<span data-ttu-id="a9b31-382">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="a9b31-382">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

