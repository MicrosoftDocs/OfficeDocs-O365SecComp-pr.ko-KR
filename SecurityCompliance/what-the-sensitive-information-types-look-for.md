---
title: 중요 한 정보 형식을 찾습니다.
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 준비가 된 80 중요 한 정보 유형이 포함 되어 있습니다. 이 항목에서는 이러한 모든 중요 한 정보 유형을 소개 하 고 DLP 정책이 각 유형을 검색할 때 어떤 내용을 찾을 지를 보여 줍니다.
ms.openlocfilehash: 17fb0b8d745168f8000fba9e6fc42f3c255a1937
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216358"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="76436-104">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="76436-104">What the sensitive information types look for</span></span>

<span data-ttu-id="76436-p102">Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 수 있는 중요 한 정보 유형이 많이 포함 되어 있습니다. 이 항목에서는 이러한 모든 중요 한 정보 유형을 소개 하 고 DLP 정책이 각 유형을 검색할 때 어떤 내용을 찾을 지를 보여 줍니다. 중요 한 정보 유형은 정규식 이나 함수로 식별 될 수 있는 패턴으로 정의 됩니다. 또한 키워드 및 체크섬과 같은 적인 증거를 사용 하 여 중요 한 정보 유형을 식별할 수 있습니다. 정확도 수준 및 근접성도 평가 프로세스에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="76436-110">ABA 라우팅 번호</span><span class="sxs-lookup"><span data-stu-id="76436-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-111">형식</span><span class="sxs-lookup"><span data-stu-id="76436-111">Format</span></span>

<span data-ttu-id="76436-112">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-113">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-113">Pattern</span></span>

<span data-ttu-id="76436-114">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="76436-114">Formatted:</span></span>
- <span data-ttu-id="76436-115">0, 1, 2, 3, 6, 7 또는 8로 시작하는 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="76436-116">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-116">A hyphen</span></span>
- <span data-ttu-id="76436-117">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-117">Four digits</span></span>
- <span data-ttu-id="76436-118">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-118">A hyphen</span></span>
- <span data-ttu-id="76436-119">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-119">A digit</span></span>

<span data-ttu-id="76436-120">서식 없음: 0, 1, 2, 3, 6, 7 또는 8로 시작 하는 9 개의 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="76436-121">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-121">Checksum</span></span>

<span data-ttu-id="76436-122">없음</span><span class="sxs-lookup"><span data-stu-id="76436-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-123">정의</span><span class="sxs-lookup"><span data-stu-id="76436-123">Definition</span></span>

<span data-ttu-id="76436-124">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-125">Func_aba_routing 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-126">Keyword_ABA_Routing의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="76436-127">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="76436-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="76436-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="76436-129">aba</span><span class="sxs-lookup"><span data-stu-id="76436-129">aba</span></span>
- <span data-ttu-id="76436-130">
aba #</span><span class="sxs-lookup"><span data-stu-id="76436-130">aba #</span></span>
- <span data-ttu-id="76436-131">
aba routing #</span><span class="sxs-lookup"><span data-stu-id="76436-131">aba routing #</span></span>
- <span data-ttu-id="76436-132">
aba routing number</span><span class="sxs-lookup"><span data-stu-id="76436-132">aba routing number</span></span>
- <span data-ttu-id="76436-133">
aba #</span><span class="sxs-lookup"><span data-stu-id="76436-133">aba#</span></span>
- <span data-ttu-id="76436-134">
abarouting#</span><span class="sxs-lookup"><span data-stu-id="76436-134">abarouting#</span></span>
- <span data-ttu-id="76436-135">
aba number</span><span class="sxs-lookup"><span data-stu-id="76436-135">aba number</span></span>
- <span data-ttu-id="76436-136">
abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="76436-136">abaroutingnumber</span></span>
- <span data-ttu-id="76436-137">
american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="76436-137">american bank association routing #</span></span>
- <span data-ttu-id="76436-138">
american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="76436-138">american bank association routing number</span></span>
- <span data-ttu-id="76436-139">
americanbankassociationrouting#</span><span class="sxs-lookup"><span data-stu-id="76436-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="76436-140">
americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="76436-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="76436-141">
bank routing number</span><span class="sxs-lookup"><span data-stu-id="76436-141">bank routing number</span></span>
- <span data-ttu-id="76436-142">
bankrouting#</span><span class="sxs-lookup"><span data-stu-id="76436-142">bankrouting#</span></span>
- <span data-ttu-id="76436-143">
bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="76436-143">bankroutingnumber</span></span>
- <span data-ttu-id="76436-144">
routing transit number</span><span class="sxs-lookup"><span data-stu-id="76436-144">routing transit number</span></span>
- <span data-ttu-id="76436-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="76436-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="76436-146">아르헨티나 국가 ID(DNI) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-147">형식</span><span class="sxs-lookup"><span data-stu-id="76436-147">Format</span></span>

<span data-ttu-id="76436-148">마침표로 구분된 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-149">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-149">Pattern</span></span>

<span data-ttu-id="76436-150">8자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-150">Eight digits:</span></span>
- <span data-ttu-id="76436-151">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-151">Two digits</span></span>
- <span data-ttu-id="76436-152">마침표 </span><span class="sxs-lookup"><span data-stu-id="76436-152">A period</span></span>
- <span data-ttu-id="76436-153">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-153">Three digits</span></span>
- <span data-ttu-id="76436-154">마침표 </span><span class="sxs-lookup"><span data-stu-id="76436-154">A period</span></span>
- <span data-ttu-id="76436-155">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-156">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-156">Checksum</span></span>

<span data-ttu-id="76436-157">없음</span><span class="sxs-lookup"><span data-stu-id="76436-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-158">정의</span><span class="sxs-lookup"><span data-stu-id="76436-158">Definition</span></span>

<span data-ttu-id="76436-159">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-160">정규식 Regex_argentina_national_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-161">Keyword_argentina_national_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-162">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="76436-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="76436-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="76436-164">Argentina National Identity number
</span><span class="sxs-lookup"><span data-stu-id="76436-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="76436-165">ID</span><span class="sxs-lookup"><span data-stu-id="76436-165">Identity</span></span> 
- <span data-ttu-id="76436-166">식별 국가 id 카드</span><span class="sxs-lookup"><span data-stu-id="76436-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="76436-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="76436-167">DNI</span></span> 
- <span data-ttu-id="76436-168">개인의 NIC 국내 레지스트리</span><span class="sxs-lookup"><span data-stu-id="76436-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="76436-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="76436-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="76436-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="76436-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="76436-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="76436-171">Identidad</span></span> 
- <span data-ttu-id="76436-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="76436-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="76436-173">호주 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="76436-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-174">형식</span><span class="sxs-lookup"><span data-stu-id="76436-174">Format</span></span>

<span data-ttu-id="76436-175">6-10자리 숫자(은행 지점 번호 포함 또는 제외)</span><span class="sxs-lookup"><span data-stu-id="76436-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-176">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-176">Pattern</span></span>

<span data-ttu-id="76436-p103">계정 번호는 6-10 자리 숫자입니다. 오스트레일리아 bank 상태 분기 번호:</span><span class="sxs-lookup"><span data-stu-id="76436-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="76436-179">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-179">Three digits</span></span> 
- <span data-ttu-id="76436-180">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-180">A hyphen</span></span> 
- <span data-ttu-id="76436-181">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-182">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-182">Checksum</span></span>

<span data-ttu-id="76436-183">없음</span><span class="sxs-lookup"><span data-stu-id="76436-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-184">정의</span><span class="sxs-lookup"><span data-stu-id="76436-184">Definition</span></span>

<span data-ttu-id="76436-185">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-186">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="76436-187">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="76436-188">Regex_australia_bank_account_number_bsb 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="76436-189">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-190">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="76436-191">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-192">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="76436-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="76436-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="76436-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="76436-194">swift bank code</span></span>
- <span data-ttu-id="76436-195">
correspondent bank</span><span class="sxs-lookup"><span data-stu-id="76436-195">correspondent bank</span></span>
- <span data-ttu-id="76436-196">
base currency</span><span class="sxs-lookup"><span data-stu-id="76436-196">base currency</span></span>
- <span data-ttu-id="76436-197">
usa account</span><span class="sxs-lookup"><span data-stu-id="76436-197">usa account</span></span>
- <span data-ttu-id="76436-198">
holder address</span><span class="sxs-lookup"><span data-stu-id="76436-198">holder address</span></span>
- <span data-ttu-id="76436-199">
bank address</span><span class="sxs-lookup"><span data-stu-id="76436-199">bank address</span></span>
- <span data-ttu-id="76436-200">
information account</span><span class="sxs-lookup"><span data-stu-id="76436-200">information account</span></span>
- <span data-ttu-id="76436-201">
fund transfers</span><span class="sxs-lookup"><span data-stu-id="76436-201">fund transfers</span></span>
- <span data-ttu-id="76436-202">
bank charges</span><span class="sxs-lookup"><span data-stu-id="76436-202">bank charges</span></span>
- <span data-ttu-id="76436-203">
bank details</span><span class="sxs-lookup"><span data-stu-id="76436-203">bank details</span></span>
- <span data-ttu-id="76436-204">
banking information</span><span class="sxs-lookup"><span data-stu-id="76436-204">banking information</span></span>
- <span data-ttu-id="76436-205">
full names</span><span class="sxs-lookup"><span data-stu-id="76436-205">full names</span></span>
- <span data-ttu-id="76436-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="76436-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="76436-207">호주 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-208">형식</span><span class="sxs-lookup"><span data-stu-id="76436-208">Format</span></span>

<span data-ttu-id="76436-209">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-210">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-210">Pattern</span></span>

<span data-ttu-id="76436-211">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="76436-212">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="76436-213">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-213">Two digits</span></span> 
- <span data-ttu-id="76436-214">5자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="76436-215">또는</span><span class="sxs-lookup"><span data-stu-id="76436-215">OR</span></span>

- <span data-ttu-id="76436-216">1-2개의 선택적 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="76436-217">4-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-217">4-9 digits</span></span>

<span data-ttu-id="76436-218">또는</span><span class="sxs-lookup"><span data-stu-id="76436-218">OR</span></span>

- <span data-ttu-id="76436-219">9자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-220">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-220">Checksum</span></span>

<span data-ttu-id="76436-221">없음</span><span class="sxs-lookup"><span data-stu-id="76436-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-222">정의</span><span class="sxs-lookup"><span data-stu-id="76436-222">Definition</span></span>

<span data-ttu-id="76436-223">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-224">Regex_australia_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-225">Keyword_australia_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="76436-226">Keyword_australia_drivers_license_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-227">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="76436-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="76436-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="76436-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="76436-229">international driving permits</span></span>
- <span data-ttu-id="76436-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="76436-230">australian automobile association</span></span>
- <span data-ttu-id="76436-231">
international driving permit</span><span class="sxs-lookup"><span data-stu-id="76436-231">international driving permit</span></span>
- <span data-ttu-id="76436-232">driverlicence</span><span class="sxs-lookup"><span data-stu-id="76436-232">DriverLicence</span></span>
- <span data-ttu-id="76436-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="76436-233">DriverLicences</span></span>
- <span data-ttu-id="76436-234">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="76436-234">Driver Lic</span></span>
- <span data-ttu-id="76436-235">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="76436-235">Driver Licence</span></span>
- <span data-ttu-id="76436-236">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="76436-236">Driver Licences</span></span>
- <span data-ttu-id="76436-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="76436-237">DriversLic</span></span>
- <span data-ttu-id="76436-238">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-238">DriversLicence</span></span>
- <span data-ttu-id="76436-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="76436-239">DriversLicences</span></span>
- <span data-ttu-id="76436-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="76436-240">Drivers Lic</span></span>
- <span data-ttu-id="76436-241">드라이버 lics</span><span class="sxs-lookup"><span data-stu-id="76436-241">Drivers Lics</span></span>
- <span data-ttu-id="76436-242">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-242">Drivers Licence</span></span>
- <span data-ttu-id="76436-243">라이선스 드라이버</span><span class="sxs-lookup"><span data-stu-id="76436-243">Drivers Licences</span></span>
- <span data-ttu-id="76436-244">driver' Lic</span><span class="sxs-lookup"><span data-stu-id="76436-244">Driver'Lic</span></span>
- <span data-ttu-id="76436-245">driver'lics</span><span class="sxs-lookup"><span data-stu-id="76436-245">Driver'Lics</span></span>
- <span data-ttu-id="76436-246">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-246">Driver'Licence</span></span>
- <span data-ttu-id="76436-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="76436-247">Driver'Licences</span></span>
- <span data-ttu-id="76436-248">드라이버 ' Lic</span><span class="sxs-lookup"><span data-stu-id="76436-248">Driver' Lic</span></span>
- <span data-ttu-id="76436-249">드라이버의 lics</span><span class="sxs-lookup"><span data-stu-id="76436-249">Driver' Lics</span></span>
- <span data-ttu-id="76436-250">운전의 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-250">Driver' Licence</span></span>
- <span data-ttu-id="76436-251">드라이버 ' 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-251">Driver' Licences</span></span>
- <span data-ttu-id="76436-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="76436-252">Driver'sLic</span></span>
- <span data-ttu-id="76436-253">drivers (slics)</span><span class="sxs-lookup"><span data-stu-id="76436-253">Driver'sLics</span></span>
- <span data-ttu-id="76436-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="76436-254">Driver'sLicence</span></span>
- <span data-ttu-id="76436-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="76436-255">Driver'sLicences</span></span>
- <span data-ttu-id="76436-256">드라이버의 Lic</span><span class="sxs-lookup"><span data-stu-id="76436-256">Driver's Lic</span></span>
- <span data-ttu-id="76436-257">운전 lics</span><span class="sxs-lookup"><span data-stu-id="76436-257">Driver's Lics</span></span>
- <span data-ttu-id="76436-258">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="76436-258">Driver's Licence</span></span>
- <span data-ttu-id="76436-259">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="76436-259">Driver's Licences</span></span>
- <span data-ttu-id="76436-260">driverlic #</span><span class="sxs-lookup"><span data-stu-id="76436-260">DriverLic#</span></span>
- <span data-ttu-id="76436-261">driverlics #</span><span class="sxs-lookup"><span data-stu-id="76436-261">DriverLics#</span></span>
- <span data-ttu-id="76436-262">driverlicence #</span><span class="sxs-lookup"><span data-stu-id="76436-262">DriverLicence#</span></span>
- <span data-ttu-id="76436-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="76436-263">DriverLicences#</span></span>
- <span data-ttu-id="76436-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="76436-264">Driver Lic#</span></span>
- <span data-ttu-id="76436-265">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-265">Driver Lics#</span></span>
- <span data-ttu-id="76436-266">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-266">Driver Licence#</span></span>
- <span data-ttu-id="76436-267">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-267">Driver Licences#</span></span>
- <span data-ttu-id="76436-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="76436-268">DriversLic#</span></span>
- <span data-ttu-id="76436-269">driverslics #</span><span class="sxs-lookup"><span data-stu-id="76436-269">DriversLics#</span></span>
- <span data-ttu-id="76436-270">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-270">DriversLicence#</span></span>
- <span data-ttu-id="76436-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="76436-271">DriversLicences#</span></span>
- <span data-ttu-id="76436-272">Drivers Lic #</span><span class="sxs-lookup"><span data-stu-id="76436-272">Drivers Lic#</span></span>
- <span data-ttu-id="76436-273">드라이버 lics #</span><span class="sxs-lookup"><span data-stu-id="76436-273">Drivers Lics#</span></span>
- <span data-ttu-id="76436-274">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-274">Drivers Licence#</span></span>
- <span data-ttu-id="76436-275">Drivers 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-275">Drivers Licences#</span></span>
- <span data-ttu-id="76436-276">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-276">Driver'Lic#</span></span>
- <span data-ttu-id="76436-277">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-277">Driver'Lics#</span></span>
- <span data-ttu-id="76436-278">Driver'Licence #
</span><span class="sxs-lookup"><span data-stu-id="76436-278">Driver'Licence#</span></span>
- <span data-ttu-id="76436-279">Driver'Licences#
</span><span class="sxs-lookup"><span data-stu-id="76436-279">Driver'Licences#</span></span>
- <span data-ttu-id="76436-280">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-280">Driver' Lic#</span></span>
- <span data-ttu-id="76436-281">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-281">Driver' Lics#</span></span>
- <span data-ttu-id="76436-282">운전의 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="76436-282">Driver' Licence#</span></span>
- <span data-ttu-id="76436-283">Driver ' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-283">Driver' Licences#</span></span>
- <span data-ttu-id="76436-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="76436-284">Driver'sLic#</span></span>
- <span data-ttu-id="76436-285">drivers (slics #)</span><span class="sxs-lookup"><span data-stu-id="76436-285">Driver'sLics#</span></span>
- <span data-ttu-id="76436-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="76436-286">Driver'sLicence#</span></span>
- <span data-ttu-id="76436-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="76436-287">Driver'sLicences#</span></span>
- <span data-ttu-id="76436-288">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-288">Driver's Lic#</span></span>
- <span data-ttu-id="76436-289">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-289">Driver's Lics#</span></span>
- <span data-ttu-id="76436-290">운전 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-290">Driver's Licence#</span></span>
- <span data-ttu-id="76436-291">운전 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="76436-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="76436-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="76436-293">aaa</span><span class="sxs-lookup"><span data-stu-id="76436-293">aaa</span></span>
- <span data-ttu-id="76436-294">driverlicense</span><span class="sxs-lookup"><span data-stu-id="76436-294">DriverLicense</span></span>
- <span data-ttu-id="76436-295">driverlicenses</span><span class="sxs-lookup"><span data-stu-id="76436-295">DriverLicenses</span></span>
- <span data-ttu-id="76436-296">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-296">Driver License</span></span>
- <span data-ttu-id="76436-297">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-297">Driver Licenses</span></span>
- <span data-ttu-id="76436-298">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-298">DriversLicense</span></span>
- <span data-ttu-id="76436-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-299">DriversLicenses</span></span>
- <span data-ttu-id="76436-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="76436-300">Drivers License</span></span>
- <span data-ttu-id="76436-301">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-301">Drivers Licenses</span></span>
- <span data-ttu-id="76436-302">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-302">Driver'License</span></span>
- <span data-ttu-id="76436-303">driver'licenses</span><span class="sxs-lookup"><span data-stu-id="76436-303">Driver'Licenses</span></span>
- <span data-ttu-id="76436-304">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-304">Driver' License</span></span>
- <span data-ttu-id="76436-305">운전 면허증</span><span class="sxs-lookup"><span data-stu-id="76436-305">Driver' Licenses</span></span>
- <span data-ttu-id="76436-306">driver'slicense</span><span class="sxs-lookup"><span data-stu-id="76436-306">Driver'sLicense</span></span>
- <span data-ttu-id="76436-307">driver'slicenses</span><span class="sxs-lookup"><span data-stu-id="76436-307">Driver'sLicenses</span></span>
- <span data-ttu-id="76436-308">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-308">Driver's License</span></span>
- <span data-ttu-id="76436-309">운전 면허증</span><span class="sxs-lookup"><span data-stu-id="76436-309">Driver's Licenses</span></span>
- <span data-ttu-id="76436-310">driverlicense #</span><span class="sxs-lookup"><span data-stu-id="76436-310">DriverLicense#</span></span>
- <span data-ttu-id="76436-311">driverlicenses #</span><span class="sxs-lookup"><span data-stu-id="76436-311">DriverLicenses#</span></span>
- <span data-ttu-id="76436-312">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-312">Driver License#</span></span>
- <span data-ttu-id="76436-313">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-313">Driver Licenses#</span></span>
- <span data-ttu-id="76436-314">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-314">DriversLicense#</span></span>
- <span data-ttu-id="76436-315">드라이버 라이선스 수</span><span class="sxs-lookup"><span data-stu-id="76436-315">DriversLicenses#</span></span>
- <span data-ttu-id="76436-316">Drivers License #</span><span class="sxs-lookup"><span data-stu-id="76436-316">Drivers License#</span></span>
- <span data-ttu-id="76436-317">Drivers 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-317">Drivers Licenses#</span></span>
- <span data-ttu-id="76436-318">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="76436-318">Driver'License#</span></span>
- <span data-ttu-id="76436-319">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="76436-319">Driver'Licenses#</span></span>
- <span data-ttu-id="76436-320">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="76436-320">Driver' License#</span></span>
- <span data-ttu-id="76436-321">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="76436-321">Driver' Licenses#</span></span>
- <span data-ttu-id="76436-322">driver'slicense #</span><span class="sxs-lookup"><span data-stu-id="76436-322">Driver'sLicense#</span></span>
- <span data-ttu-id="76436-323">driver'slicenses #</span><span class="sxs-lookup"><span data-stu-id="76436-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="76436-324">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="76436-324">Driver's License#</span></span>
- <span data-ttu-id="76436-325">

Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="76436-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="76436-326">호주 의료 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="76436-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-327">형식</span><span class="sxs-lookup"><span data-stu-id="76436-327">Format</span></span>

<span data-ttu-id="76436-328">10-11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-329">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-329">Pattern</span></span>

<span data-ttu-id="76436-330">10-11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-330">10-11 digits:</span></span>
- <span data-ttu-id="76436-331">첫 번째 숫자는 2-6 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="76436-332">9번째 숫자는 검사 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="76436-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="76436-333">10번째 숫자는 문제 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="76436-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="76436-334">11번째 숫자(선택 사항)는 개인 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="76436-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-335">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-335">Checksum</span></span>

<span data-ttu-id="76436-336">예</span><span class="sxs-lookup"><span data-stu-id="76436-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-337">정의</span><span class="sxs-lookup"><span data-stu-id="76436-337">Definition</span></span>

<span data-ttu-id="76436-338">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-339">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-340">Keyword_Australia_Medical_Account_Number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="76436-341">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-341">The checksum passes.</span></span>

<span data-ttu-id="76436-342">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-343">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-344">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-344">The checksum passes.</span></span>

```
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-345">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="76436-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="76436-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="76436-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="76436-347">bank account details</span></span>
- <span data-ttu-id="76436-348">
medicare payments</span><span class="sxs-lookup"><span data-stu-id="76436-348">medicare payments</span></span>
- <span data-ttu-id="76436-349">
mortgage account</span><span class="sxs-lookup"><span data-stu-id="76436-349">mortgage account</span></span>
- <span data-ttu-id="76436-350">
bank payments</span><span class="sxs-lookup"><span data-stu-id="76436-350">bank payments</span></span>
- <span data-ttu-id="76436-351">
information branch</span><span class="sxs-lookup"><span data-stu-id="76436-351">information branch</span></span>
- <span data-ttu-id="76436-352">
credit card loan</span><span class="sxs-lookup"><span data-stu-id="76436-352">credit card loan</span></span>
- <span data-ttu-id="76436-353">
department of human services</span><span class="sxs-lookup"><span data-stu-id="76436-353">department of human services</span></span>
- <span data-ttu-id="76436-354">로컬 서비스</span><span class="sxs-lookup"><span data-stu-id="76436-354">local service</span></span>
- <span data-ttu-id="76436-355">

medicare</span><span class="sxs-lookup"><span data-stu-id="76436-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="76436-356">호주 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-357">형식</span><span class="sxs-lookup"><span data-stu-id="76436-357">Format</span></span>

<span data-ttu-id="76436-358">문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-359">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-359">Pattern</span></span>

<span data-ttu-id="76436-360">1개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-361">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-361">Checksum</span></span>

<span data-ttu-id="76436-362">없음</span><span class="sxs-lookup"><span data-stu-id="76436-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-363">정의</span><span class="sxs-lookup"><span data-stu-id="76436-363">Definition</span></span>

<span data-ttu-id="76436-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-365">Regex_australia_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-366">Keyword_passport 또는 Keyword_australia_passport_number의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a><span data-ttu-id="76436-367">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="76436-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="76436-368">Keyword_passport</span></span>

- <span data-ttu-id="76436-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="76436-369">Passport Number</span></span>
- <span data-ttu-id="76436-370">
Passport No</span><span class="sxs-lookup"><span data-stu-id="76436-370">Passport No</span></span>
- <span data-ttu-id="76436-371">Passport #
</span><span class="sxs-lookup"><span data-stu-id="76436-371">Passport #</span></span>
- <span data-ttu-id="76436-372">Passport#
</span><span class="sxs-lookup"><span data-stu-id="76436-372">Passport#</span></span>
- <span data-ttu-id="76436-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="76436-373">PassportID</span></span>
- <span data-ttu-id="76436-374">Passportno
</span><span class="sxs-lookup"><span data-stu-id="76436-374">Passportno</span></span>
- <span data-ttu-id="76436-375">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-375">passportnumber</span></span>
- <span data-ttu-id="76436-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="76436-376">パスポート</span></span>
- <span data-ttu-id="76436-377">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="76436-377">パスポート番号</span></span>
- <span data-ttu-id="76436-378">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="76436-378">パスポートのNum</span></span>
- <span data-ttu-id="76436-379">
パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="76436-379">パスポート ＃</span></span> 
- <span data-ttu-id="76436-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="76436-380">Numéro de passeport</span></span>
- <span data-ttu-id="76436-381">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="76436-381">Passeport n °</span></span>
- <span data-ttu-id="76436-382">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="76436-382">Passeport Non</span></span>
- <span data-ttu-id="76436-383">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="76436-383">Passeport #</span></span>
- <span data-ttu-id="76436-384">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="76436-384">Passeport#</span></span>
- <span data-ttu-id="76436-385">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="76436-385">PasseportNon</span></span>
- <span data-ttu-id="76436-386">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="76436-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="76436-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="76436-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="76436-388">passport</span><span class="sxs-lookup"><span data-stu-id="76436-388">passport</span></span>
- <span data-ttu-id="76436-389">
passport details</span><span class="sxs-lookup"><span data-stu-id="76436-389">passport details</span></span>
- <span data-ttu-id="76436-390">
immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="76436-390">immigration and citizenship</span></span>
- <span data-ttu-id="76436-391">
commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="76436-391">commonwealth of australia</span></span>
- <span data-ttu-id="76436-392">
department of immigration</span><span class="sxs-lookup"><span data-stu-id="76436-392">department of immigration</span></span>
- <span data-ttu-id="76436-393">
residential address</span><span class="sxs-lookup"><span data-stu-id="76436-393">residential address</span></span>
- <span data-ttu-id="76436-394">
department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="76436-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="76436-395">visa
</span><span class="sxs-lookup"><span data-stu-id="76436-395">visa</span></span>
- <span data-ttu-id="76436-396">
national identity card</span><span class="sxs-lookup"><span data-stu-id="76436-396">national identity card</span></span>
- <span data-ttu-id="76436-397">여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-397">passport number</span></span>
- <span data-ttu-id="76436-398">
travel document</span><span class="sxs-lookup"><span data-stu-id="76436-398">travel document</span></span>
- <span data-ttu-id="76436-399">

issuing authority</span><span class="sxs-lookup"><span data-stu-id="76436-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="76436-400">호주 세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="76436-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-401">형식</span><span class="sxs-lookup"><span data-stu-id="76436-401">Format</span></span>

<span data-ttu-id="76436-402">8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-403">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-403">Pattern</span></span>

<span data-ttu-id="76436-404">일반적으로 다음과 같이 공백과 함께 표시되는 8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="76436-405">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-405">Three digits</span></span> 
- <span data-ttu-id="76436-406">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="76436-406">An optional space</span></span> 
- <span data-ttu-id="76436-407">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-407">Three digits</span></span> 
- <span data-ttu-id="76436-408">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="76436-408">An optional space</span></span> 
- <span data-ttu-id="76436-409">마지막 숫자가 검사 숫자인 2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-410">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-410">Checksum</span></span>

<span data-ttu-id="76436-411">예</span><span class="sxs-lookup"><span data-stu-id="76436-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-412">정의</span><span class="sxs-lookup"><span data-stu-id="76436-412">Definition</span></span>

<span data-ttu-id="76436-413">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-414">Func_australian_tax_file_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-415">Keyword_Australia_Tax_File_Number 또는 Keyword_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="76436-416">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-416">The checksum passes.</span></span>

```
    <!-- Australia Tax File Number -->
<Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
    
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_Australia_Tax_File_Number" />
          <Match idRef="Keyword_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-417">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="76436-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="76436-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="76436-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="76436-419">australian business number</span></span>
- <span data-ttu-id="76436-420">
marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="76436-420">marginal tax rate</span></span>
- <span data-ttu-id="76436-421">
medicare levy</span><span class="sxs-lookup"><span data-stu-id="76436-421">medicare levy</span></span>
- <span data-ttu-id="76436-422">
portfolio number</span><span class="sxs-lookup"><span data-stu-id="76436-422">portfolio number</span></span>
- <span data-ttu-id="76436-423">
service veterans</span><span class="sxs-lookup"><span data-stu-id="76436-423">service veterans</span></span>
- <span data-ttu-id="76436-424">
withholding tax</span><span class="sxs-lookup"><span data-stu-id="76436-424">withholding tax</span></span>
- <span data-ttu-id="76436-425">
individual tax return</span><span class="sxs-lookup"><span data-stu-id="76436-425">individual tax return</span></span>
- <span data-ttu-id="76436-426">

tax file number</span><span class="sxs-lookup"><span data-stu-id="76436-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="76436-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="76436-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="76436-428">00000000</span><span class="sxs-lookup"><span data-stu-id="76436-428">00000000</span></span>
- <span data-ttu-id="76436-429">11111111</span><span class="sxs-lookup"><span data-stu-id="76436-429">11111111</span></span>
- <span data-ttu-id="76436-430">22222222</span><span class="sxs-lookup"><span data-stu-id="76436-430">22222222</span></span>
- <span data-ttu-id="76436-431">33333333</span><span class="sxs-lookup"><span data-stu-id="76436-431">33333333</span></span>
- <span data-ttu-id="76436-432">44444444</span><span class="sxs-lookup"><span data-stu-id="76436-432">44444444</span></span>
- <span data-ttu-id="76436-433">55555555</span><span class="sxs-lookup"><span data-stu-id="76436-433">55555555</span></span>
- <span data-ttu-id="76436-434">66666666</span><span class="sxs-lookup"><span data-stu-id="76436-434">66666666</span></span>
- <span data-ttu-id="76436-435">77777777</span><span class="sxs-lookup"><span data-stu-id="76436-435">77777777</span></span>
- <span data-ttu-id="76436-436">88888888</span><span class="sxs-lookup"><span data-stu-id="76436-436">88888888</span></span>
- <span data-ttu-id="76436-437">99999999</span><span class="sxs-lookup"><span data-stu-id="76436-437">99999999</span></span>
- <span data-ttu-id="76436-438">000000000</span><span class="sxs-lookup"><span data-stu-id="76436-438">000000000</span></span>
- <span data-ttu-id="76436-439">111111111</span><span class="sxs-lookup"><span data-stu-id="76436-439">111111111</span></span>
- <span data-ttu-id="76436-440">222222222</span><span class="sxs-lookup"><span data-stu-id="76436-440">222222222</span></span>
- <span data-ttu-id="76436-441">333333333</span><span class="sxs-lookup"><span data-stu-id="76436-441">333333333</span></span>
- <span data-ttu-id="76436-442">444444444</span><span class="sxs-lookup"><span data-stu-id="76436-442">444444444</span></span>
- <span data-ttu-id="76436-443">555555555</span><span class="sxs-lookup"><span data-stu-id="76436-443">555555555</span></span>
- <span data-ttu-id="76436-444">666666666</span><span class="sxs-lookup"><span data-stu-id="76436-444">666666666</span></span>
- <span data-ttu-id="76436-445">777777777</span><span class="sxs-lookup"><span data-stu-id="76436-445">777777777</span></span>
- <span data-ttu-id="76436-446">888888888</span><span class="sxs-lookup"><span data-stu-id="76436-446">888888888</span></span>
- <span data-ttu-id="76436-447">999999999</span><span class="sxs-lookup"><span data-stu-id="76436-447">999999999</span></span>
- <span data-ttu-id="76436-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="76436-448">0000000000</span></span>
- <span data-ttu-id="76436-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="76436-449">1111111111</span></span>
- <span data-ttu-id="76436-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="76436-450">2222222222</span></span>
- <span data-ttu-id="76436-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="76436-451">3333333333</span></span>
- <span data-ttu-id="76436-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="76436-452">4444444444</span></span>
- <span data-ttu-id="76436-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="76436-453">5555555555</span></span>
- <span data-ttu-id="76436-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="76436-454">6666666666</span></span>
- <span data-ttu-id="76436-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="76436-455">7777777777</span></span>
- <span data-ttu-id="76436-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="76436-456">8888888888</span></span>
- <span data-ttu-id="76436-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="76436-457">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="76436-458">벨기에 국가 번호</span><span class="sxs-lookup"><span data-stu-id="76436-458">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-459">형식</span><span class="sxs-lookup"><span data-stu-id="76436-459">Format</span></span>

<span data-ttu-id="76436-460">11자리 숫자와 구분 기호</span><span class="sxs-lookup"><span data-stu-id="76436-460">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-461">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-461">Pattern</span></span>

<span data-ttu-id="76436-462">11자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="76436-462">11 digits plus delimiters:</span></span>
- <span data-ttu-id="76436-463">생년월일을 나타내는 YY.MM.DD 형식의 6자리 숫자와 마침표 2개 </span><span class="sxs-lookup"><span data-stu-id="76436-463">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="76436-464">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-464">A hyphen</span></span> 
- <span data-ttu-id="76436-465">세 개의 순차적 숫자(남성의 경우 홀수, 여성의 경우 짝수) </span><span class="sxs-lookup"><span data-stu-id="76436-465">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="76436-466">마침표 </span><span class="sxs-lookup"><span data-stu-id="76436-466">A period</span></span> 
- <span data-ttu-id="76436-467">검사 숫자에 해당하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-467">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-468">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-468">Checksum</span></span>

<span data-ttu-id="76436-469">예</span><span class="sxs-lookup"><span data-stu-id="76436-469">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-470">정의</span><span class="sxs-lookup"><span data-stu-id="76436-470">Definition</span></span>

<span data-ttu-id="76436-471">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-472">Func_belgium_national_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-472">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-473">Keyword_belgium_national_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-473">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="76436-474">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-474">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-475">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-475">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="76436-476">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="76436-476">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="76436-477">Identity</span><span class="sxs-lookup"><span data-stu-id="76436-477">Identity</span></span>
- <span data-ttu-id="76436-478">Registration</span><span class="sxs-lookup"><span data-stu-id="76436-478">Registration</span></span>
- <span data-ttu-id="76436-479">Identification</span><span class="sxs-lookup"><span data-stu-id="76436-479">Identification</span></span> 
- <span data-ttu-id="76436-480">ID</span><span class="sxs-lookup"><span data-stu-id="76436-480">ID</span></span> 
- <span data-ttu-id="76436-481">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="76436-481">Identiteitskaart</span></span>
- <span data-ttu-id="76436-482">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="76436-482">Registratie nummer</span></span> 
- <span data-ttu-id="76436-483">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="76436-483">Identificatie nummer</span></span> 
- <span data-ttu-id="76436-484">Identiteit</span><span class="sxs-lookup"><span data-stu-id="76436-484">Identiteit</span></span>
- <span data-ttu-id="76436-485">Registratie</span><span class="sxs-lookup"><span data-stu-id="76436-485">Registratie</span></span>
- <span data-ttu-id="76436-486">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="76436-486">Identificatie</span></span> 
- <span data-ttu-id="76436-487">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="76436-487">Carte d’identité</span></span> 
- <span data-ttu-id="76436-488">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="76436-488">numéro d'immatriculation</span></span>
- <span data-ttu-id="76436-489">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="76436-489">numéro d'identification</span></span>
- <span data-ttu-id="76436-490">
identité
</span><span class="sxs-lookup"><span data-stu-id="76436-490">identité</span></span> 
- <span data-ttu-id="76436-491">inscription
</span><span class="sxs-lookup"><span data-stu-id="76436-491">inscription</span></span> 
- <span data-ttu-id="76436-492">Identifikation</span><span class="sxs-lookup"><span data-stu-id="76436-492">Identifikation</span></span>
- <span data-ttu-id="76436-493">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="76436-493">Identifizierung</span></span>
- <span data-ttu-id="76436-494">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="76436-494">Identifikationsnummer</span></span>
- <span data-ttu-id="76436-495">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="76436-495">Personalausweis</span></span>
- <span data-ttu-id="76436-496">Registrierung</span><span class="sxs-lookup"><span data-stu-id="76436-496">Registrierung</span></span>
- <span data-ttu-id="76436-497">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="76436-497">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="76436-498">브라질 CPF 번호</span><span class="sxs-lookup"><span data-stu-id="76436-498">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-499">형식</span><span class="sxs-lookup"><span data-stu-id="76436-499">Format</span></span>

<span data-ttu-id="76436-500">서식이 있거나 서식이 없을 수 있는 검사 숫자를 포함하는 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-500">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-501">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-501">Pattern</span></span>

<span data-ttu-id="76436-502">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="76436-502">Formatted:</span></span>
- <span data-ttu-id="76436-503">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-503">Three digits</span></span> 
- <span data-ttu-id="76436-504">마침표 </span><span class="sxs-lookup"><span data-stu-id="76436-504">A period</span></span> 
- <span data-ttu-id="76436-505">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-505">Three digits</span></span> 
- <span data-ttu-id="76436-506">마침표 </span><span class="sxs-lookup"><span data-stu-id="76436-506">A period</span></span> 
- <span data-ttu-id="76436-507">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-507">Three digits</span></span> 
- <span data-ttu-id="76436-508">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-508">A hyphen</span></span> 
- <span data-ttu-id="76436-509">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-509">Two digits which are check digits</span></span>

<span data-ttu-id="76436-510">서식 없음:</span><span class="sxs-lookup"><span data-stu-id="76436-510">Unformatted:</span></span>
- <span data-ttu-id="76436-511">마지막 2자리 숫자가 검사 숫자인 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-511">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-512">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-512">Checksum</span></span>

<span data-ttu-id="76436-513">예</span><span class="sxs-lookup"><span data-stu-id="76436-513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-514">정의</span><span class="sxs-lookup"><span data-stu-id="76436-514">Definition</span></span>

<span data-ttu-id="76436-515">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-515">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-516">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-516">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-517">Keyword_brazil_cpf에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-517">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="76436-518">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-518">The checksum passes.</span></span>

<span data-ttu-id="76436-519">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-519">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-520">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-520">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-521">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-521">The checksum passes.</span></span>

```
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-522">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-522">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="76436-523">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="76436-523">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="76436-524">CPF</span><span class="sxs-lookup"><span data-stu-id="76436-524">CPF</span></span>
- <span data-ttu-id="76436-525">Identification</span><span class="sxs-lookup"><span data-stu-id="76436-525">Identification</span></span>
- <span data-ttu-id="76436-526">Registration</span><span class="sxs-lookup"><span data-stu-id="76436-526">Registration</span></span>
- <span data-ttu-id="76436-527">Revenue</span><span class="sxs-lookup"><span data-stu-id="76436-527">Revenue</span></span>
- <span data-ttu-id="76436-528">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="76436-528">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="76436-529">Imposto
</span><span class="sxs-lookup"><span data-stu-id="76436-529">Imposto</span></span> 
- <span data-ttu-id="76436-530">Identificação
</span><span class="sxs-lookup"><span data-stu-id="76436-530">Identificação</span></span> 
- <span data-ttu-id="76436-531">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="76436-531">Inscrição</span></span> 
- <span data-ttu-id="76436-532">Receita

</span><span class="sxs-lookup"><span data-stu-id="76436-532">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="76436-533">브라질 법인 번호(CNPJ)</span><span class="sxs-lookup"><span data-stu-id="76436-533">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="76436-534">형식</span><span class="sxs-lookup"><span data-stu-id="76436-534">Format</span></span>

<span data-ttu-id="76436-535">등록 번호, 지점 번호, 검사 숫자 및 구분 기호를 포함하는 14자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-535">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-536">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-536">Pattern</span></span>
<span data-ttu-id="76436-537">14자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="76436-537">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="76436-538">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-538">Two digits</span></span> 
- <span data-ttu-id="76436-539">마침표</span><span class="sxs-lookup"><span data-stu-id="76436-539">A period</span></span> 
- <span data-ttu-id="76436-540">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-540">Three digits</span></span> 
- <span data-ttu-id="76436-541">마침표 </span><span class="sxs-lookup"><span data-stu-id="76436-541">A period</span></span> 
- <span data-ttu-id="76436-542">3자리 숫자(처음 8자리 숫자는 등록 번호임) </span><span class="sxs-lookup"><span data-stu-id="76436-542">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="76436-543">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="76436-543">A forward slash</span></span> 
- <span data-ttu-id="76436-544">4자리 지점 번호 </span><span class="sxs-lookup"><span data-stu-id="76436-544">Four-digit branch number</span></span> 
- <span data-ttu-id="76436-545">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-545">A hyphen</span></span> 
- <span data-ttu-id="76436-546">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-546">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-547">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-547">Checksum</span></span>

<span data-ttu-id="76436-548">예</span><span class="sxs-lookup"><span data-stu-id="76436-548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-549">정의</span><span class="sxs-lookup"><span data-stu-id="76436-549">Definition</span></span>

<span data-ttu-id="76436-550">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-551">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-551">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-552">Keyword_brazil_cnpj에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-552">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="76436-553">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-553">The checksum passes.</span></span>

<span data-ttu-id="76436-554">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-554">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-555">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-555">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-556">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-556">The checksum passes.</span></span>

```
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-557">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-557">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="76436-558">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="76436-558">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="76436-559">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="76436-559">CNPJ</span></span> 
- <span data-ttu-id="76436-560">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="76436-560">CNPJ/MF</span></span> 
- <span data-ttu-id="76436-561">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="76436-561">CNPJ-MF</span></span> 
- <span data-ttu-id="76436-562">National Registry of Legal Entities
</span><span class="sxs-lookup"><span data-stu-id="76436-562">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="76436-563">Taxpayers Registry
</span><span class="sxs-lookup"><span data-stu-id="76436-563">Taxpayers Registry</span></span> 
- <span data-ttu-id="76436-564">Legal entity
</span><span class="sxs-lookup"><span data-stu-id="76436-564">Legal entity</span></span> 
- <span data-ttu-id="76436-565">Legal entities
</span><span class="sxs-lookup"><span data-stu-id="76436-565">Legal entities</span></span> 
- <span data-ttu-id="76436-566">Registration Status
</span><span class="sxs-lookup"><span data-stu-id="76436-566">Registration Status</span></span> 
- <span data-ttu-id="76436-567">Business
</span><span class="sxs-lookup"><span data-stu-id="76436-567">Business</span></span> 
- <span data-ttu-id="76436-568">Company</span><span class="sxs-lookup"><span data-stu-id="76436-568">Company</span></span>
- <span data-ttu-id="76436-569">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="76436-569">CNPJ</span></span> 
- <span data-ttu-id="76436-570">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="76436-570">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="76436-571">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="76436-571">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="76436-572">CGC
</span><span class="sxs-lookup"><span data-stu-id="76436-572">CGC</span></span> 
- <span data-ttu-id="76436-573">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="76436-573">Pessoa jurídica</span></span> 
- <span data-ttu-id="76436-574">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="76436-574">Pessoas jurídicas</span></span> 
- <span data-ttu-id="76436-575">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="76436-575">Situação cadastral</span></span> 
- <span data-ttu-id="76436-576">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="76436-576">Inscrição</span></span> 
- <span data-ttu-id="76436-577">Empresa
</span><span class="sxs-lookup"><span data-stu-id="76436-577">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="76436-578">	브라질 국가 ID 카드(RG)</span><span class="sxs-lookup"><span data-stu-id="76436-578">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="76436-579">형식</span><span class="sxs-lookup"><span data-stu-id="76436-579">Format</span></span>

<span data-ttu-id="76436-580">Registro Geral (이전 형식): 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-580">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="76436-581">Registro de Identidade (RIC) (새 형식): 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-581">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-582">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-582">Pattern</span></span>

<span data-ttu-id="76436-583">Registro Geral(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="76436-583">Registro Geral (old format):</span></span>
- <span data-ttu-id="76436-584">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-584">Two digits</span></span> 
- <span data-ttu-id="76436-585">마침표</span><span class="sxs-lookup"><span data-stu-id="76436-585">A period</span></span> 
- <span data-ttu-id="76436-586">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-586">Three digits</span></span> 
- <span data-ttu-id="76436-587">마침표</span><span class="sxs-lookup"><span data-stu-id="76436-587">A period</span></span> 
- <span data-ttu-id="76436-588">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-588">Three digits</span></span> 
- <span data-ttu-id="76436-589">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-589">A hyphen</span></span> 
- <span data-ttu-id="76436-590">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-590">One digit which is a check digit</span></span>

<span data-ttu-id="76436-591">Registro de Identidade (RIC) (새 형식):</span><span class="sxs-lookup"><span data-stu-id="76436-591">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="76436-592">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-592">10 digits</span></span> 
- <span data-ttu-id="76436-593">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-593">A hyphen</span></span> 
- <span data-ttu-id="76436-594">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-594">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-595">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-595">Checksum</span></span>

<span data-ttu-id="76436-596">예</span><span class="sxs-lookup"><span data-stu-id="76436-596">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-597">정의</span><span class="sxs-lookup"><span data-stu-id="76436-597">Definition</span></span>

<span data-ttu-id="76436-598">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-598">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-599">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-599">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-600">Keyword_brazil_rg에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-600">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="76436-601">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-601">The checksum passes.</span></span>

<span data-ttu-id="76436-602">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-602">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-603">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-603">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-604">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-604">The checksum passes.</span></span>

```
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-605">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-605">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="76436-606">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="76436-606">Keyword_brazil_rg</span></span>

<span data-ttu-id="76436-607">Cédula de identidade identity card 국립 id número de rregistro registro de Iidentidade registro geral RG (이 키워드는 대/소문자를 구분 함) RIC (이 키워드는 대/소문자를 구분 함)</span><span class="sxs-lookup"><span data-stu-id="76436-607">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="76436-608">캐나다 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="76436-608">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-609">형식</span><span class="sxs-lookup"><span data-stu-id="76436-609">Format</span></span>

<span data-ttu-id="76436-610">7 또는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-610">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-611">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-611">Pattern</span></span>

<span data-ttu-id="76436-612">캐나다 은행 계좌 번호는 7 또는 12자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="76436-612">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="76436-613">캐나다 은행 계좌 송금 번호:</span><span class="sxs-lookup"><span data-stu-id="76436-613">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="76436-614">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-614">Five digits</span></span> 
- <span data-ttu-id="76436-615">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-615">A hyphen</span></span> 
- <span data-ttu-id="76436-616">3 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="76436-616">Three digits OR</span></span>
- <span data-ttu-id="76436-617">"0"</span><span class="sxs-lookup"><span data-stu-id="76436-617">A zero "0"</span></span> 
- <span data-ttu-id="76436-618">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-618">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-619">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-619">Checksum</span></span>

<span data-ttu-id="76436-620">없음</span><span class="sxs-lookup"><span data-stu-id="76436-620">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-621">정의</span><span class="sxs-lookup"><span data-stu-id="76436-621">Definition</span></span>

<span data-ttu-id="76436-622">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-622">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-623">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-623">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-624">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-624">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="76436-625">Regex_canada_bank_account_transit_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-625">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="76436-626">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-627">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-627">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-628">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-628">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-629">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-629">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="76436-630">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="76436-630">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="76436-631">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="76436-631">canada savings bonds</span></span>
- <span data-ttu-id="76436-632">
canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="76436-632">canada revenue agency</span></span>
- <span data-ttu-id="76436-633">
canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="76436-633">canadian financial institution</span></span>
- <span data-ttu-id="76436-634">
direct deposit form</span><span class="sxs-lookup"><span data-stu-id="76436-634">direct deposit form</span></span>
- <span data-ttu-id="76436-635">
canadian citizen</span><span class="sxs-lookup"><span data-stu-id="76436-635">canadian citizen</span></span>
- <span data-ttu-id="76436-636">
legal representative</span><span class="sxs-lookup"><span data-stu-id="76436-636">legal representative</span></span>
- <span data-ttu-id="76436-637">
notary public</span><span class="sxs-lookup"><span data-stu-id="76436-637">notary public</span></span>
- <span data-ttu-id="76436-638">
commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="76436-638">commissioner for oaths</span></span>
- <span data-ttu-id="76436-639">
child care benefit</span><span class="sxs-lookup"><span data-stu-id="76436-639">child care benefit</span></span>
- <span data-ttu-id="76436-640">
universal child care</span><span class="sxs-lookup"><span data-stu-id="76436-640">universal child care</span></span>
- <span data-ttu-id="76436-641">
canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="76436-641">canada child tax benefit</span></span>
- <span data-ttu-id="76436-642">
income tax benefit</span><span class="sxs-lookup"><span data-stu-id="76436-642">income tax benefit</span></span>
- <span data-ttu-id="76436-643">
harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="76436-643">harmonized sales tax</span></span>
- <span data-ttu-id="76436-644">social insurance number</span><span class="sxs-lookup"><span data-stu-id="76436-644">social insurance number</span></span>
- <span data-ttu-id="76436-645">
income tax refund</span><span class="sxs-lookup"><span data-stu-id="76436-645">income tax refund</span></span>
- <span data-ttu-id="76436-646">
child tax benefit</span><span class="sxs-lookup"><span data-stu-id="76436-646">child tax benefit</span></span>
- <span data-ttu-id="76436-647">
territorial payments</span><span class="sxs-lookup"><span data-stu-id="76436-647">territorial payments</span></span>
- <span data-ttu-id="76436-648">
institution number</span><span class="sxs-lookup"><span data-stu-id="76436-648">institution number</span></span>
- <span data-ttu-id="76436-649">
deposit request</span><span class="sxs-lookup"><span data-stu-id="76436-649">deposit request</span></span>
- <span data-ttu-id="76436-650">
banking information</span><span class="sxs-lookup"><span data-stu-id="76436-650">banking information</span></span>
- <span data-ttu-id="76436-651">

direct deposit</span><span class="sxs-lookup"><span data-stu-id="76436-651">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="76436-652">캐나다 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-652">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-653">형식</span><span class="sxs-lookup"><span data-stu-id="76436-653">Format</span></span>

<span data-ttu-id="76436-654">지역마다 다름</span><span class="sxs-lookup"><span data-stu-id="76436-654">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-655">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-655">Pattern</span></span>

<span data-ttu-id="76436-656">앨버타, 브리티시 콜롬비아, 매니토바, 뉴브런즈윅, 뉴펀들랜드/래브라도, 노바스코샤, 온타리오, 프린스에드워드아일랜드, 퀘벡 및 서스캐처원을 포함하는 다양한 패턴</span><span class="sxs-lookup"><span data-stu-id="76436-656">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-657">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-657">Checksum</span></span>

<span data-ttu-id="76436-658">없음</span><span class="sxs-lookup"><span data-stu-id="76436-658">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-659">정의</span><span class="sxs-lookup"><span data-stu-id="76436-659">Definition</span></span>

<span data-ttu-id="76436-660">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-660">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-661">Func_[province_name]_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-661">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-662">Keyword_[province_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-662">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="76436-663">Keyword_canada_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-663">A keyword from Keyword_canada_drivers_license is found.</span></span>

```
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-664">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-664">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="76436-665">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="76436-665">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="76436-666">시/도 약어(예: AB)</span><span class="sxs-lookup"><span data-stu-id="76436-666">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="76436-667">
시/도 이름(예: 앨버타)</span><span class="sxs-lookup"><span data-stu-id="76436-667">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="76436-668">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="76436-668">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="76436-669">DL</span><span class="sxs-lookup"><span data-stu-id="76436-669">DL</span></span>
- <span data-ttu-id="76436-670">DLS</span><span class="sxs-lookup"><span data-stu-id="76436-670">DLS</span></span>
- <span data-ttu-id="76436-671">cdl</span><span class="sxs-lookup"><span data-stu-id="76436-671">CDL</span></span>
- <span data-ttu-id="76436-672">cdls</span><span class="sxs-lookup"><span data-stu-id="76436-672">CDLS</span></span>
- <span data-ttu-id="76436-673">driverlic</span><span class="sxs-lookup"><span data-stu-id="76436-673">DriverLic</span></span>
- <span data-ttu-id="76436-674">driverlics</span><span class="sxs-lookup"><span data-stu-id="76436-674">DriverLics</span></span>
- <span data-ttu-id="76436-675">driverlicense</span><span class="sxs-lookup"><span data-stu-id="76436-675">DriverLicense</span></span>
- <span data-ttu-id="76436-676">driverlicenses</span><span class="sxs-lookup"><span data-stu-id="76436-676">DriverLicenses</span></span>
- <span data-ttu-id="76436-677">driverlicence</span><span class="sxs-lookup"><span data-stu-id="76436-677">DriverLicence</span></span>
- <span data-ttu-id="76436-678">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="76436-678">DriverLicences</span></span>
- <span data-ttu-id="76436-679">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="76436-679">Driver Lic</span></span>
- <span data-ttu-id="76436-680">드라이버 lics</span><span class="sxs-lookup"><span data-stu-id="76436-680">Driver Lics</span></span>
- <span data-ttu-id="76436-681">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-681">Driver License</span></span>
- <span data-ttu-id="76436-682">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-682">Driver Licenses</span></span>
- <span data-ttu-id="76436-683">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="76436-683">Driver Licence</span></span>
- <span data-ttu-id="76436-684">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="76436-684">Driver Licences</span></span>
- <span data-ttu-id="76436-685">DriversLic</span><span class="sxs-lookup"><span data-stu-id="76436-685">DriversLic</span></span>
- <span data-ttu-id="76436-686">driverslics</span><span class="sxs-lookup"><span data-stu-id="76436-686">DriversLics</span></span>
- <span data-ttu-id="76436-687">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-687">DriversLicence</span></span>
- <span data-ttu-id="76436-688">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="76436-688">DriversLicences</span></span>
- <span data-ttu-id="76436-689">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-689">DriversLicense</span></span>
- <span data-ttu-id="76436-690">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-690">DriversLicenses</span></span>
- <span data-ttu-id="76436-691">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="76436-691">Drivers Lic</span></span>
- <span data-ttu-id="76436-692">드라이버 lics</span><span class="sxs-lookup"><span data-stu-id="76436-692">Drivers Lics</span></span>
- <span data-ttu-id="76436-693">Drivers License</span><span class="sxs-lookup"><span data-stu-id="76436-693">Drivers License</span></span>
- <span data-ttu-id="76436-694">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-694">Drivers Licenses</span></span>
- <span data-ttu-id="76436-695">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-695">Drivers Licence</span></span>
- <span data-ttu-id="76436-696">라이선스 드라이버</span><span class="sxs-lookup"><span data-stu-id="76436-696">Drivers Licences</span></span>
- <span data-ttu-id="76436-697">driver' Lic</span><span class="sxs-lookup"><span data-stu-id="76436-697">Driver'Lic</span></span>
- <span data-ttu-id="76436-698">driver'lics</span><span class="sxs-lookup"><span data-stu-id="76436-698">Driver'Lics</span></span>
- <span data-ttu-id="76436-699">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-699">Driver'License</span></span>
- <span data-ttu-id="76436-700">driver'licenses</span><span class="sxs-lookup"><span data-stu-id="76436-700">Driver'Licenses</span></span>
- <span data-ttu-id="76436-701">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-701">Driver'Licence</span></span>
- <span data-ttu-id="76436-702">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="76436-702">Driver'Licences</span></span>
- <span data-ttu-id="76436-703">드라이버 ' Lic</span><span class="sxs-lookup"><span data-stu-id="76436-703">Driver' Lic</span></span>
- <span data-ttu-id="76436-704">드라이버의 lics</span><span class="sxs-lookup"><span data-stu-id="76436-704">Driver' Lics</span></span>
- <span data-ttu-id="76436-705">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-705">Driver' License</span></span>
- <span data-ttu-id="76436-706">운전 면허증</span><span class="sxs-lookup"><span data-stu-id="76436-706">Driver' Licenses</span></span>
- <span data-ttu-id="76436-707">운전의 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-707">Driver' Licence</span></span>
- <span data-ttu-id="76436-708">드라이버 ' 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-708">Driver' Licences</span></span>
- <span data-ttu-id="76436-709">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="76436-709">Driver'sLic</span></span>
- <span data-ttu-id="76436-710">drivers (slics)</span><span class="sxs-lookup"><span data-stu-id="76436-710">Driver'sLics</span></span>
- <span data-ttu-id="76436-711">driver'slicense</span><span class="sxs-lookup"><span data-stu-id="76436-711">Driver'sLicense</span></span>
- <span data-ttu-id="76436-712">driver'slicenses</span><span class="sxs-lookup"><span data-stu-id="76436-712">Driver'sLicenses</span></span>
- <span data-ttu-id="76436-713">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="76436-713">Driver'sLicence</span></span>
- <span data-ttu-id="76436-714">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="76436-714">Driver'sLicences</span></span>
- <span data-ttu-id="76436-715">드라이버의 Lic</span><span class="sxs-lookup"><span data-stu-id="76436-715">Driver's Lic</span></span>
- <span data-ttu-id="76436-716">운전 lics</span><span class="sxs-lookup"><span data-stu-id="76436-716">Driver's Lics</span></span>
- <span data-ttu-id="76436-717">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-717">Driver's License</span></span>
- <span data-ttu-id="76436-718">운전 면허증</span><span class="sxs-lookup"><span data-stu-id="76436-718">Driver's Licenses</span></span>
- <span data-ttu-id="76436-719">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="76436-719">Driver's Licence</span></span>
- <span data-ttu-id="76436-720">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="76436-720">Driver's Licences</span></span>
- <span data-ttu-id="76436-721">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="76436-721">Permis de Conduire</span></span>
- <span data-ttu-id="76436-722">id</span><span class="sxs-lookup"><span data-stu-id="76436-722">id</span></span>
- <span data-ttu-id="76436-723">번호가</span><span class="sxs-lookup"><span data-stu-id="76436-723">ids</span></span>
- <span data-ttu-id="76436-724">
idcard number</span><span class="sxs-lookup"><span data-stu-id="76436-724">idcard number</span></span>
- <span data-ttu-id="76436-725">
idcard numbers</span><span class="sxs-lookup"><span data-stu-id="76436-725">idcard numbers</span></span>
- <span data-ttu-id="76436-726">
idcard #</span><span class="sxs-lookup"><span data-stu-id="76436-726">idcard #</span></span>
- <span data-ttu-id="76436-727">
idcard #s</span><span class="sxs-lookup"><span data-stu-id="76436-727">idcard #s</span></span>
- <span data-ttu-id="76436-728">idcard 카드</span><span class="sxs-lookup"><span data-stu-id="76436-728">idcard card</span></span>
- <span data-ttu-id="76436-729">idcard 카드</span><span class="sxs-lookup"><span data-stu-id="76436-729">idcard cards</span></span>
- <span data-ttu-id="76436-730">idcard</span><span class="sxs-lookup"><span data-stu-id="76436-730">idcard</span></span>
- <span data-ttu-id="76436-731">identification number
</span><span class="sxs-lookup"><span data-stu-id="76436-731">identification number</span></span>
- <span data-ttu-id="76436-732">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="76436-732">identification numbers</span></span>
- <span data-ttu-id="76436-733">identification #
</span><span class="sxs-lookup"><span data-stu-id="76436-733">identification #</span></span>
- <span data-ttu-id="76436-734">
identification #s</span><span class="sxs-lookup"><span data-stu-id="76436-734">identification #s</span></span>
- <span data-ttu-id="76436-735">식별 카드</span><span class="sxs-lookup"><span data-stu-id="76436-735">identification card</span></span>
- <span data-ttu-id="76436-736">식별 카드</span><span class="sxs-lookup"><span data-stu-id="76436-736">identification cards</span></span>
- <span data-ttu-id="76436-737">
identification
</span><span class="sxs-lookup"><span data-stu-id="76436-737">identification</span></span> 
- <span data-ttu-id="76436-738">DL#</span><span class="sxs-lookup"><span data-stu-id="76436-738">DL#</span></span>
- <span data-ttu-id="76436-739">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="76436-739">DLS#</span></span> 
- <span data-ttu-id="76436-740">CDL#
</span><span class="sxs-lookup"><span data-stu-id="76436-740">CDL#</span></span> 
- <span data-ttu-id="76436-741">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="76436-741">CDLS#</span></span> 
- <span data-ttu-id="76436-742">driverlic #</span><span class="sxs-lookup"><span data-stu-id="76436-742">DriverLic#</span></span> 
- <span data-ttu-id="76436-743">driverlics #</span><span class="sxs-lookup"><span data-stu-id="76436-743">DriverLics#</span></span> 
- <span data-ttu-id="76436-744">driverlicense #</span><span class="sxs-lookup"><span data-stu-id="76436-744">DriverLicense#</span></span> 
- <span data-ttu-id="76436-745">driverlicenses #</span><span class="sxs-lookup"><span data-stu-id="76436-745">DriverLicenses#</span></span> 
- <span data-ttu-id="76436-746">driverlicence #</span><span class="sxs-lookup"><span data-stu-id="76436-746">DriverLicence#</span></span> 
- <span data-ttu-id="76436-747">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="76436-747">DriverLicences#</span></span> 
- <span data-ttu-id="76436-748">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="76436-748">Driver Lic#</span></span>
- <span data-ttu-id="76436-749">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-749">Driver Lics#</span></span> 
- <span data-ttu-id="76436-750">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-750">Driver License#</span></span> 
- <span data-ttu-id="76436-751">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-751">Driver Licenses#</span></span> 
- <span data-ttu-id="76436-752">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-752">Driver License#</span></span> 
- <span data-ttu-id="76436-753">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-753">Driver Licences#</span></span> 
- <span data-ttu-id="76436-754">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="76436-754">DriversLic#</span></span> 
- <span data-ttu-id="76436-755">driverslics #</span><span class="sxs-lookup"><span data-stu-id="76436-755">DriversLics#</span></span> 
- <span data-ttu-id="76436-756">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-756">DriversLicense#</span></span> 
- <span data-ttu-id="76436-757">드라이버 라이선스 수</span><span class="sxs-lookup"><span data-stu-id="76436-757">DriversLicenses#</span></span> 
- <span data-ttu-id="76436-758">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-758">DriversLicence#</span></span> 
- <span data-ttu-id="76436-759">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="76436-759">DriversLicences#</span></span> 
- <span data-ttu-id="76436-760">Drivers Lic #</span><span class="sxs-lookup"><span data-stu-id="76436-760">Drivers Lic#</span></span> 
- <span data-ttu-id="76436-761">드라이버 lics #</span><span class="sxs-lookup"><span data-stu-id="76436-761">Drivers Lics#</span></span> 
- <span data-ttu-id="76436-762">Drivers License #</span><span class="sxs-lookup"><span data-stu-id="76436-762">Drivers License#</span></span> 
- <span data-ttu-id="76436-763">Drivers 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-763">Drivers Licenses#</span></span> 
- <span data-ttu-id="76436-764">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-764">Drivers Licence#</span></span> 
- <span data-ttu-id="76436-765">Drivers 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-765">Drivers Licences#</span></span> 
- <span data-ttu-id="76436-766">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-766">Driver'Lic#</span></span> 
- <span data-ttu-id="76436-767">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-767">Driver'Lics#</span></span> 
- <span data-ttu-id="76436-768">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="76436-768">Driver'License#</span></span> 
- <span data-ttu-id="76436-769">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="76436-769">Driver'Licenses#</span></span> 
- <span data-ttu-id="76436-770">Driver'Licence #
</span><span class="sxs-lookup"><span data-stu-id="76436-770">Driver'Licence#</span></span> 
- <span data-ttu-id="76436-771">Driver'Licences#
</span><span class="sxs-lookup"><span data-stu-id="76436-771">Driver'Licences#</span></span> 
- <span data-ttu-id="76436-772">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-772">Driver' Lic#</span></span> 
- <span data-ttu-id="76436-773">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-773">Driver' Lics#</span></span> 
- <span data-ttu-id="76436-774">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="76436-774">Driver' License#</span></span> 
- <span data-ttu-id="76436-775">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="76436-775">Driver' Licenses#</span></span> 
- <span data-ttu-id="76436-776">운전의 라이선스 번호</span><span class="sxs-lookup"><span data-stu-id="76436-776">Driver' Licence#</span></span> 
- <span data-ttu-id="76436-777">Driver ' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-777">Driver' Licences#</span></span> 
- <span data-ttu-id="76436-778">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="76436-778">Driver'sLic#</span></span> 
- <span data-ttu-id="76436-779">drivers (slics #)</span><span class="sxs-lookup"><span data-stu-id="76436-779">Driver'sLics#</span></span> 
- <span data-ttu-id="76436-780">driver'slicense #</span><span class="sxs-lookup"><span data-stu-id="76436-780">Driver'sLicense#</span></span> 
- <span data-ttu-id="76436-781">driver'slicenses #</span><span class="sxs-lookup"><span data-stu-id="76436-781">Driver'sLicenses#</span></span> 
- <span data-ttu-id="76436-782">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="76436-782">Driver'sLicence#</span></span> 
- <span data-ttu-id="76436-783">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="76436-783">Driver'sLicences#</span></span> 
- <span data-ttu-id="76436-784">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-784">Driver's Lic#</span></span> 
- <span data-ttu-id="76436-785">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-785">Driver's Lics#</span></span> 
- <span data-ttu-id="76436-786">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="76436-786">Driver's License#</span></span> 
- <span data-ttu-id="76436-787">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="76436-787">Driver's Licenses#</span></span> 
- <span data-ttu-id="76436-788">운전 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-788">Driver's Licence#</span></span> 
- <span data-ttu-id="76436-789">운전 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-789">Driver's Licences#</span></span> 
- <span data-ttu-id="76436-790">Permis de Conduire #</span><span class="sxs-lookup"><span data-stu-id="76436-790">Permis de Conduire#</span></span> 
- <span data-ttu-id="76436-791">i</span><span class="sxs-lookup"><span data-stu-id="76436-791">id#</span></span> 
- <span data-ttu-id="76436-792">번호가</span><span class="sxs-lookup"><span data-stu-id="76436-792">ids#</span></span> 
- <span data-ttu-id="76436-793">idcard card#
</span><span class="sxs-lookup"><span data-stu-id="76436-793">idcard card#</span></span> 
- <span data-ttu-id="76436-794">idcard cards#
</span><span class="sxs-lookup"><span data-stu-id="76436-794">idcard cards#</span></span> 
- <span data-ttu-id="76436-795">idcard#
</span><span class="sxs-lookup"><span data-stu-id="76436-795">idcard#</span></span> 
- <span data-ttu-id="76436-796">identification card#
</span><span class="sxs-lookup"><span data-stu-id="76436-796">identification card#</span></span> 
- <span data-ttu-id="76436-797">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="76436-797">identification cards#</span></span> 
- <span data-ttu-id="76436-798">identification#
</span><span class="sxs-lookup"><span data-stu-id="76436-798">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="76436-799">캐나다 건강 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="76436-799">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-800">형식</span><span class="sxs-lookup"><span data-stu-id="76436-800">Format</span></span>

<span data-ttu-id="76436-801">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-801">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-802">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-802">Pattern</span></span>

<span data-ttu-id="76436-803">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-803">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-804">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-804">Checksum</span></span>

<span data-ttu-id="76436-805">없음</span><span class="sxs-lookup"><span data-stu-id="76436-805">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-806">정의</span><span class="sxs-lookup"><span data-stu-id="76436-806">Definition</span></span>

<span data-ttu-id="76436-807">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-807">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-808">Regex_canada_health_service_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-808">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-809">Keyword_canada_health_service_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-809">A keyword from Keyword_canada_health_service_number is found.</span></span>

```
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-810">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-810">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="76436-811">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="76436-811">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="76436-812">personal health number</span><span class="sxs-lookup"><span data-stu-id="76436-812">personal health number</span></span>
- <span data-ttu-id="76436-813">
patient information</span><span class="sxs-lookup"><span data-stu-id="76436-813">patient information</span></span>
- <span data-ttu-id="76436-814">상태 서비스</span><span class="sxs-lookup"><span data-stu-id="76436-814">health services</span></span>
- <span data-ttu-id="76436-815">
speciality services</span><span class="sxs-lookup"><span data-stu-id="76436-815">speciality services</span></span>
- <span data-ttu-id="76436-816">
automobile accident</span><span class="sxs-lookup"><span data-stu-id="76436-816">automobile accident</span></span>
- <span data-ttu-id="76436-817">
patient hospital</span><span class="sxs-lookup"><span data-stu-id="76436-817">patient hospital</span></span>
- <span data-ttu-id="76436-818">
psychiatrist</span><span class="sxs-lookup"><span data-stu-id="76436-818">psychiatrist</span></span>
- <span data-ttu-id="76436-819">
workers compensation</span><span class="sxs-lookup"><span data-stu-id="76436-819">workers compensation</span></span>
- <span data-ttu-id="76436-820">
disability</span><span class="sxs-lookup"><span data-stu-id="76436-820">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="76436-821">캐나다 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-821">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-822">형식</span><span class="sxs-lookup"><span data-stu-id="76436-822">Format</span></span>

<span data-ttu-id="76436-823">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-823">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-824">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-824">Pattern</span></span>

<span data-ttu-id="76436-825">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-825">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-826">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-826">Checksum</span></span>

<span data-ttu-id="76436-827">없음</span><span class="sxs-lookup"><span data-stu-id="76436-827">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-828">정의</span><span class="sxs-lookup"><span data-stu-id="76436-828">Definition</span></span>

<span data-ttu-id="76436-829">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-829">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-830">Regex_canada_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-830">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-831">Keyword_canada_passport_number 또는 Keyword_passport의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-831">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

``` 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-832">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-832">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="76436-833">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="76436-833">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="76436-834">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="76436-834">canadian citizenship</span></span>
- <span data-ttu-id="76436-835">
canadian passport</span><span class="sxs-lookup"><span data-stu-id="76436-835">canadian passport</span></span>
- <span data-ttu-id="76436-836">
passport application</span><span class="sxs-lookup"><span data-stu-id="76436-836">passport application</span></span>
- <span data-ttu-id="76436-837">
passport photos</span><span class="sxs-lookup"><span data-stu-id="76436-837">passport photos</span></span>
- <span data-ttu-id="76436-838">
certified translator</span><span class="sxs-lookup"><span data-stu-id="76436-838">certified translator</span></span>
- <span data-ttu-id="76436-839">
canadian citizens</span><span class="sxs-lookup"><span data-stu-id="76436-839">canadian citizens</span></span>
- <span data-ttu-id="76436-840">
processing times</span><span class="sxs-lookup"><span data-stu-id="76436-840">processing times</span></span>
- <span data-ttu-id="76436-841">

renewal application</span><span class="sxs-lookup"><span data-stu-id="76436-841">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="76436-842">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="76436-842">Keyword_passport</span></span>

- <span data-ttu-id="76436-843">Passport Number</span><span class="sxs-lookup"><span data-stu-id="76436-843">Passport Number</span></span>
- <span data-ttu-id="76436-844">
Passport No</span><span class="sxs-lookup"><span data-stu-id="76436-844">Passport No</span></span>
- <span data-ttu-id="76436-845">Passport #
</span><span class="sxs-lookup"><span data-stu-id="76436-845">Passport #</span></span>
- <span data-ttu-id="76436-846">Passport#
</span><span class="sxs-lookup"><span data-stu-id="76436-846">Passport#</span></span>
- <span data-ttu-id="76436-847">PassportID</span><span class="sxs-lookup"><span data-stu-id="76436-847">PassportID</span></span>
- <span data-ttu-id="76436-848">Passportno
</span><span class="sxs-lookup"><span data-stu-id="76436-848">Passportno</span></span>
- <span data-ttu-id="76436-849">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-849">passportnumber</span></span>
- <span data-ttu-id="76436-850">パスポート</span><span class="sxs-lookup"><span data-stu-id="76436-850">パスポート</span></span>
- <span data-ttu-id="76436-851">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="76436-851">パスポート番号</span></span>
- <span data-ttu-id="76436-852">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="76436-852">パスポートのNum</span></span>
- <span data-ttu-id="76436-853">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="76436-853">パスポート＃</span></span>
- <span data-ttu-id="76436-854">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="76436-854">Numéro de passeport</span></span>
- <span data-ttu-id="76436-855">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="76436-855">Passeport n °</span></span>
- <span data-ttu-id="76436-856">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="76436-856">Passeport Non</span></span>
- <span data-ttu-id="76436-857">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="76436-857">Passeport #</span></span>
- <span data-ttu-id="76436-858">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="76436-858">Passeport#</span></span>
- <span data-ttu-id="76436-859">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="76436-859">PasseportNon</span></span>
- <span data-ttu-id="76436-860">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="76436-860">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="76436-861">캐나다 PHIN(개인 건강 식별 번호)</span><span class="sxs-lookup"><span data-stu-id="76436-861">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="76436-862">형식</span><span class="sxs-lookup"><span data-stu-id="76436-862">Format</span></span>

<span data-ttu-id="76436-863">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-863">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-864">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-864">Pattern</span></span>

<span data-ttu-id="76436-865">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-865">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-866">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-866">Checksum</span></span>

<span data-ttu-id="76436-867">없음</span><span class="sxs-lookup"><span data-stu-id="76436-867">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-868">정의</span><span class="sxs-lookup"><span data-stu-id="76436-868">Definition</span></span>

<span data-ttu-id="76436-p104">DLP 정책은 300 문자 (예: Regex_canada_phin)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다. Keyword_canada_phin 또는 Keyword_canada_provinces의 키워드를 두 개 이상 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-871">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-871">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="76436-872">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="76436-872">Keyword_canada_phin</span></span>

- <span data-ttu-id="76436-873">social insurance number</span><span class="sxs-lookup"><span data-stu-id="76436-873">social insurance number</span></span>
- <span data-ttu-id="76436-874">
health information act</span><span class="sxs-lookup"><span data-stu-id="76436-874">health information act</span></span>
- <span data-ttu-id="76436-875">
income tax information</span><span class="sxs-lookup"><span data-stu-id="76436-875">income tax information</span></span>
- <span data-ttu-id="76436-876">
manitoba health</span><span class="sxs-lookup"><span data-stu-id="76436-876">manitoba health</span></span>
- <span data-ttu-id="76436-877">
health registration</span><span class="sxs-lookup"><span data-stu-id="76436-877">health registration</span></span>
- <span data-ttu-id="76436-878">
prescription purchases</span><span class="sxs-lookup"><span data-stu-id="76436-878">prescription purchases</span></span>
- <span data-ttu-id="76436-879">
benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="76436-879">benefit eligibility</span></span>
- <span data-ttu-id="76436-880">
personal health</span><span class="sxs-lookup"><span data-stu-id="76436-880">personal health</span></span>
- <span data-ttu-id="76436-881">
power of attorney</span><span class="sxs-lookup"><span data-stu-id="76436-881">power of attorney</span></span>
- <span data-ttu-id="76436-882">
registration number</span><span class="sxs-lookup"><span data-stu-id="76436-882">registration number</span></span>
- <span data-ttu-id="76436-883">personal health number</span><span class="sxs-lookup"><span data-stu-id="76436-883">personal health number</span></span>
- <span data-ttu-id="76436-884">
practitioner referral</span><span class="sxs-lookup"><span data-stu-id="76436-884">practitioner referral</span></span>
- <span data-ttu-id="76436-885">
wellness professional</span><span class="sxs-lookup"><span data-stu-id="76436-885">wellness professional</span></span>
- <span data-ttu-id="76436-886">
patient referral</span><span class="sxs-lookup"><span data-stu-id="76436-886">patient referral</span></span>
- <span data-ttu-id="76436-887">

health and wellness</span><span class="sxs-lookup"><span data-stu-id="76436-887">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="76436-888">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="76436-888">Keyword_canada_provinces</span></span>

- <span data-ttu-id="76436-889">Nunavut</span><span class="sxs-lookup"><span data-stu-id="76436-889">Nunavut</span></span>
- <span data-ttu-id="76436-890">
Quebec</span><span class="sxs-lookup"><span data-stu-id="76436-890">Quebec</span></span>
- <span data-ttu-id="76436-891">
Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="76436-891">Northwest Territories</span></span>
- <span data-ttu-id="76436-892">
Ontario</span><span class="sxs-lookup"><span data-stu-id="76436-892">Ontario</span></span>
- <span data-ttu-id="76436-893">
British Columbia</span><span class="sxs-lookup"><span data-stu-id="76436-893">British Columbia</span></span>
- <span data-ttu-id="76436-894">
Alberta</span><span class="sxs-lookup"><span data-stu-id="76436-894">Alberta</span></span>
- <span data-ttu-id="76436-895">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="76436-895">Saskatchewan</span></span>
- <span data-ttu-id="76436-896">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="76436-896">Manitoba</span></span>
- <span data-ttu-id="76436-897">
Yukon</span><span class="sxs-lookup"><span data-stu-id="76436-897">Yukon</span></span>
- <span data-ttu-id="76436-898">
Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="76436-898">Newfoundland and Labrador</span></span>
- <span data-ttu-id="76436-899">
New Brunswick</span><span class="sxs-lookup"><span data-stu-id="76436-899">New Brunswick</span></span>
- <span data-ttu-id="76436-900">
Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="76436-900">Nova Scotia</span></span>
- <span data-ttu-id="76436-901">
Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="76436-901">Prince Edward Island</span></span>
- <span data-ttu-id="76436-902">Canada</span><span class="sxs-lookup"><span data-stu-id="76436-902">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="76436-903">캐나다 사회 보험 번호</span><span class="sxs-lookup"><span data-stu-id="76436-903">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-904">형식</span><span class="sxs-lookup"><span data-stu-id="76436-904">Format</span></span>

<span data-ttu-id="76436-905">선택적 하이픈 또는 공백을 포함하는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-905">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-906">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-906">Pattern</span></span>

<span data-ttu-id="76436-907">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="76436-907">Formatted:</span></span>
- <span data-ttu-id="76436-908">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-908">Three digits</span></span> 
- <span data-ttu-id="76436-909">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="76436-909">A hyphen or space</span></span> 
- <span data-ttu-id="76436-910">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-910">Three digits</span></span> 
- <span data-ttu-id="76436-911">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="76436-911">A hyphen or space</span></span> 
- <span data-ttu-id="76436-912">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-912">Three digits</span></span>

<span data-ttu-id="76436-913">서식 없음: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-913">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-914">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-914">Checksum</span></span>

<span data-ttu-id="76436-915">예</span><span class="sxs-lookup"><span data-stu-id="76436-915">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-916">정의</span><span class="sxs-lookup"><span data-stu-id="76436-916">Definition</span></span>

<span data-ttu-id="76436-917">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-917">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-918">Func_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-918">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-919">2개 이상의 다음 항목 조합:</span><span class="sxs-lookup"><span data-stu-id="76436-919">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="76436-920">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-920">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="76436-921">Keyword_sin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-921">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="76436-922">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-922">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="76436-923">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-923">The checksum passes.</span></span>

<span data-ttu-id="76436-924">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-924">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-925">Func_unformatted_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-925">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-926">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-926">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="76436-927">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-927">The checksum passes.</span></span>

```
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-928">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-928">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="76436-929">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="76436-929">Keyword_sin</span></span>

- <span data-ttu-id="76436-930">sin</span><span class="sxs-lookup"><span data-stu-id="76436-930">sin</span></span> 
- <span data-ttu-id="76436-931">social insurance
</span><span class="sxs-lookup"><span data-stu-id="76436-931">social insurance</span></span> 
- <span data-ttu-id="76436-932">numero d'assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="76436-932">numero d'assurance sociale</span></span> 
- <span data-ttu-id="76436-933">sins
</span><span class="sxs-lookup"><span data-stu-id="76436-933">sins</span></span> 
- <span data-ttu-id="76436-934">ssn</span><span class="sxs-lookup"><span data-stu-id="76436-934">ssn</span></span> 
- <span data-ttu-id="76436-935">있는 ssn</span><span class="sxs-lookup"><span data-stu-id="76436-935">ssns</span></span> 
- <span data-ttu-id="76436-936">소셜 보안</span><span class="sxs-lookup"><span data-stu-id="76436-936">social security</span></span> 
- <span data-ttu-id="76436-937">numero d'assurance social
</span><span class="sxs-lookup"><span data-stu-id="76436-937">numero d'assurance social</span></span> 
- <span data-ttu-id="76436-938">국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="76436-938">national identification number</span></span> 
- <span data-ttu-id="76436-939">
national id</span><span class="sxs-lookup"><span data-stu-id="76436-939">national id</span></span> 
- <span data-ttu-id="76436-940">sin#
</span><span class="sxs-lookup"><span data-stu-id="76436-940">sin#</span></span> 
- <span data-ttu-id="76436-941">soc ins
</span><span class="sxs-lookup"><span data-stu-id="76436-941">soc ins</span></span> 
- <span data-ttu-id="76436-942">social ins
</span><span class="sxs-lookup"><span data-stu-id="76436-942">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="76436-943">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="76436-943">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="76436-944">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-944">driver's license</span></span> 
- <span data-ttu-id="76436-945">drivers license</span><span class="sxs-lookup"><span data-stu-id="76436-945">drivers license</span></span> 
- <span data-ttu-id="76436-946">운전의 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-946">driver's licence</span></span> 
- <span data-ttu-id="76436-947">drivers licence</span><span class="sxs-lookup"><span data-stu-id="76436-947">drivers licence</span></span> 
- <span data-ttu-id="76436-948">DOB
</span><span class="sxs-lookup"><span data-stu-id="76436-948">DOB</span></span> 
- <span data-ttu-id="76436-949">생년월일</span><span class="sxs-lookup"><span data-stu-id="76436-949">Birthdate</span></span> 
- <span data-ttu-id="76436-950">생일 </span><span class="sxs-lookup"><span data-stu-id="76436-950">Birthday</span></span> 
- <span data-ttu-id="76436-951">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="76436-951">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="76436-952">	칠레 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-952">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-953">형식</span><span class="sxs-lookup"><span data-stu-id="76436-953">Format</span></span>

<span data-ttu-id="76436-954">7-8 자리 숫자와 구분 기호 확인 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="76436-954">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-955">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-955">Pattern</span></span>

<span data-ttu-id="76436-956">7-8자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="76436-956">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="76436-957">1-2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-957">1-2 digits</span></span> 
- <span data-ttu-id="76436-958">마침표 </span><span class="sxs-lookup"><span data-stu-id="76436-958">A period</span></span> 
- <span data-ttu-id="76436-959">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-959">Three digits</span></span> 
- <span data-ttu-id="76436-960">마침표</span><span class="sxs-lookup"><span data-stu-id="76436-960">A period</span></span> 
- <span data-ttu-id="76436-961">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-961">Three digits</span></span> 
- <span data-ttu-id="76436-962">대시 1개</span><span class="sxs-lookup"><span data-stu-id="76436-962">A dash</span></span> 
- <span data-ttu-id="76436-963">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-963">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-964">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-964">Checksum</span></span>

<span data-ttu-id="76436-965">예</span><span class="sxs-lookup"><span data-stu-id="76436-965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-966">정의</span><span class="sxs-lookup"><span data-stu-id="76436-966">Definition</span></span>

<span data-ttu-id="76436-967">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-967">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-968">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-968">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-969">Keyword_chile_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-969">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="76436-970">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-970">The checksum passes.</span></span>

<span data-ttu-id="76436-971">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-971">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-972">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-972">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-973">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-973">The checksum passes.</span></span>

```
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-974">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-974">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="76436-975">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="76436-975">Keyword_chile_id_card</span></span>

- <span data-ttu-id="76436-976">National Identification Number
</span><span class="sxs-lookup"><span data-stu-id="76436-976">National Identification Number</span></span> 
- <span data-ttu-id="76436-977">Identity card</span><span class="sxs-lookup"><span data-stu-id="76436-977">Identity card</span></span> 
- <span data-ttu-id="76436-978">ID</span><span class="sxs-lookup"><span data-stu-id="76436-978">ID</span></span> 
- <span data-ttu-id="76436-979">Identification</span><span class="sxs-lookup"><span data-stu-id="76436-979">Identification</span></span> 
- <span data-ttu-id="76436-980">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="76436-980">Rol Único Nacional</span></span> 
- <span data-ttu-id="76436-981">실행</span><span class="sxs-lookup"><span data-stu-id="76436-981">RUN</span></span> 
- <span data-ttu-id="76436-982">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="76436-982">Rol Único Tributario</span></span> 
- <span data-ttu-id="76436-983">RUT
</span><span class="sxs-lookup"><span data-stu-id="76436-983">RUT</span></span> 
- <span data-ttu-id="76436-984">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="76436-984">Cédula de Identidad</span></span> 
- <span data-ttu-id="76436-985">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="76436-985">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="76436-986">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="76436-986">Tarjeta de identificación</span></span> 
- <span data-ttu-id="76436-987">Identificación
</span><span class="sxs-lookup"><span data-stu-id="76436-987">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="76436-988">	중국 주민 ID 카드(PRC) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-988">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-989">형식</span><span class="sxs-lookup"><span data-stu-id="76436-989">Format</span></span>

<span data-ttu-id="76436-990">18자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-990">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-991">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-991">Pattern</span></span>

<span data-ttu-id="76436-992">18자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-992">18 digits:</span></span>
- <span data-ttu-id="76436-993">주소 코드에 해당하는 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-993">Six digits which are an address code</span></span> 
- <span data-ttu-id="76436-994">생년월일에 해당하는 YYYYMMDD 형식의 8자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-994">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="76436-995">주문 코드에 해당하는 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-995">Three digits which are an order code</span></span> 
- <span data-ttu-id="76436-996">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-996">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-997">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-997">Checksum</span></span>

<span data-ttu-id="76436-998">예</span><span class="sxs-lookup"><span data-stu-id="76436-998">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-999">정의</span><span class="sxs-lookup"><span data-stu-id="76436-999">Definition</span></span>

<span data-ttu-id="76436-1000">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1000">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1001">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1001">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1002">Keyword_china_resident_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1002">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="76436-1003">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1003">The checksum passes.</span></span>

<span data-ttu-id="76436-1004">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1005">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1005">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1006">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1006">The checksum passes.</span></span>

```
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1007">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1007">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="76436-1008">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="76436-1008">Keyword_china_resident_id</span></span>

- <span data-ttu-id="76436-1009">Resident Identity Card
</span><span class="sxs-lookup"><span data-stu-id="76436-1009">Resident Identity Card</span></span> 
- <span data-ttu-id="76436-1010">중국</span><span class="sxs-lookup"><span data-stu-id="76436-1010">PRC</span></span> 
- <span data-ttu-id="76436-1011">National Identification Card
</span><span class="sxs-lookup"><span data-stu-id="76436-1011">National Identification Card</span></span> 
- <span data-ttu-id="76436-1012">身份证 </span><span class="sxs-lookup"><span data-stu-id="76436-1012">身份证</span></span> 
- <span data-ttu-id="76436-1013">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="76436-1013">居民 身份证</span></span> 
- <span data-ttu-id="76436-1014">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="76436-1014">居民身份证</span></span> 
- <span data-ttu-id="76436-1015">鉴定

</span><span class="sxs-lookup"><span data-stu-id="76436-1015">鉴定</span></span> 
- <span data-ttu-id="76436-1016">身分證 </span><span class="sxs-lookup"><span data-stu-id="76436-1016">身分證</span></span> 
- <span data-ttu-id="76436-1017">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="76436-1017">居民 身份證</span></span>
- <span data-ttu-id="76436-1018">鑑定 </span><span class="sxs-lookup"><span data-stu-id="76436-1018">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="76436-1019">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1019">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1020">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1020">Format</span></span>

<span data-ttu-id="76436-1021">서식이 있거나 서식이 없을 수 있는 16 자리 (dddddddddddddddd), Luhn 테스트를 통과 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1021">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1022">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1022">Pattern</span></span>

<span data-ttu-id="76436-1023">Visa, MasterCard, Discover Card, JCB, American Express, 상품권 및 식사권을 비롯하여 전 세계 모든 주요 브랜드 카드를 검색하는 매우 복잡하고 강력한 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1023">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1024">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1024">Checksum</span></span>

<span data-ttu-id="76436-1025">있음(Luhn 체크섬)</span><span class="sxs-lookup"><span data-stu-id="76436-1025">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1026">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1026">Definition</span></span>

<span data-ttu-id="76436-1027">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1027">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1028">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1028">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1029">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1029">One of the following is true:</span></span>
    - <span data-ttu-id="76436-1030">Keyword_cc_verification의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1030">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="76436-1031">Keyword_cc_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1031">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="76436-1032">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1032">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="76436-1033">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1033">The checksum passes.</span></span>

<span data-ttu-id="76436-1034">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1034">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1035">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1035">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1036">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1036">The checksum passes.</span></span>

```
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1037">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1037">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="76436-1038">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="76436-1038">Keyword_cc_verification</span></span>

- <span data-ttu-id="76436-1039">card verification</span><span class="sxs-lookup"><span data-stu-id="76436-1039">card verification</span></span>
- <span data-ttu-id="76436-1040">card identification number</span><span class="sxs-lookup"><span data-stu-id="76436-1040">card identification number</span></span>
- <span data-ttu-id="76436-1041">cvn
</span><span class="sxs-lookup"><span data-stu-id="76436-1041">cvn</span></span>
- <span data-ttu-id="76436-1042">cid
</span><span class="sxs-lookup"><span data-stu-id="76436-1042">cid</span></span>
- <span data-ttu-id="76436-1043">cvc2</span><span class="sxs-lookup"><span data-stu-id="76436-1043">cvc2</span></span>
- <span data-ttu-id="76436-1044">cvv2</span><span class="sxs-lookup"><span data-stu-id="76436-1044">cvv2</span></span>
- <span data-ttu-id="76436-1045">pin block
</span><span class="sxs-lookup"><span data-stu-id="76436-1045">pin block</span></span>
- <span data-ttu-id="76436-1046">security code
</span><span class="sxs-lookup"><span data-stu-id="76436-1046">security code</span></span>
- <span data-ttu-id="76436-1047">security number
</span><span class="sxs-lookup"><span data-stu-id="76436-1047">security number</span></span>
- <span data-ttu-id="76436-1048">security no
</span><span class="sxs-lookup"><span data-stu-id="76436-1048">security no</span></span>
- <span data-ttu-id="76436-1049">issue number
</span><span class="sxs-lookup"><span data-stu-id="76436-1049">issue number</span></span>
- <span data-ttu-id="76436-1050">issue no
</span><span class="sxs-lookup"><span data-stu-id="76436-1050">issue no</span></span>
- <span data-ttu-id="76436-1051">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="76436-1051">cryptogramme</span></span>
- <span data-ttu-id="76436-1052">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="76436-1052">numéro de sécurité</span></span>
- <span data-ttu-id="76436-1053">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="76436-1053">numero de securite</span></span>
- <span data-ttu-id="76436-1054">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1054">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="76436-1055">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1055">kreditkartenprufnummer</span></span>
- <span data-ttu-id="76436-1056">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="76436-1056">prüfziffer</span></span>
- <span data-ttu-id="76436-1057">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="76436-1057">prufziffer</span></span>
- <span data-ttu-id="76436-1058">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="76436-1058">sicherheits Kode</span></span>
- <span data-ttu-id="76436-1059">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="76436-1059">sicherheitscode</span></span>
- <span data-ttu-id="76436-1060">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1060">sicherheitsnummer</span></span>
- <span data-ttu-id="76436-1061">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="76436-1061">verfalldatum</span></span>
- <span data-ttu-id="76436-1062">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="76436-1062">codice di verifica</span></span>
- <span data-ttu-id="76436-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="76436-p105">cod. sicurezza</span></span>
- <span data-ttu-id="76436-1065">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="76436-1065">cod sicurezza</span></span>
- <span data-ttu-id="76436-1066">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="76436-1066">n autorizzazione</span></span>
- <span data-ttu-id="76436-1067">código
</span><span class="sxs-lookup"><span data-stu-id="76436-1067">código</span></span>
- <span data-ttu-id="76436-1068">codigo
</span><span class="sxs-lookup"><span data-stu-id="76436-1068">codigo</span></span>
- <span data-ttu-id="76436-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="76436-p106">cod. seg</span></span>
- <span data-ttu-id="76436-1071">cod seg</span><span class="sxs-lookup"><span data-stu-id="76436-1071">cod seg</span></span>
- <span data-ttu-id="76436-1072">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="76436-1072">código de segurança</span></span>
- <span data-ttu-id="76436-1073">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="76436-1073">codigo de seguranca</span></span>
- <span data-ttu-id="76436-1074">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="76436-1074">codigo de segurança</span></span>
- <span data-ttu-id="76436-1075">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="76436-1075">código de seguranca</span></span>
- <span data-ttu-id="76436-p107">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="76436-p107">cód. segurança</span></span>
- <span data-ttu-id="76436-p108">cod. seguranca cod segurança</span><span class="sxs-lookup"><span data-stu-id="76436-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="76436-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="76436-p109">cód. seguranca</span></span>
- <span data-ttu-id="76436-1083">cód segurança</span><span class="sxs-lookup"><span data-stu-id="76436-1083">cód segurança</span></span>
- <span data-ttu-id="76436-1084">cod seguranca cod segurança</span><span class="sxs-lookup"><span data-stu-id="76436-1084">cod seguranca cod segurança</span></span>
- <span data-ttu-id="76436-1085">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="76436-1085">cód seguranca</span></span>
- <span data-ttu-id="76436-1086">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="76436-1086">número de verificação</span></span>
- <span data-ttu-id="76436-1087">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="76436-1087">numero de verificacao</span></span>
- <span data-ttu-id="76436-1088">ablauf
</span><span class="sxs-lookup"><span data-stu-id="76436-1088">ablauf</span></span>
- <span data-ttu-id="76436-1089">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="76436-1089">gültig bis</span></span>
- <span data-ttu-id="76436-1090">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="76436-1090">gültigkeitsdatum</span></span>
- <span data-ttu-id="76436-1091">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="76436-1091">gultig bis</span></span>
- <span data-ttu-id="76436-1092">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="76436-1092">gultigkeitsdatum</span></span>
- <span data-ttu-id="76436-1093">scadenza
</span><span class="sxs-lookup"><span data-stu-id="76436-1093">scadenza</span></span>
- <span data-ttu-id="76436-1094">data scad
</span><span class="sxs-lookup"><span data-stu-id="76436-1094">data scad</span></span>
- <span data-ttu-id="76436-1095">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="76436-1095">fecha de expiracion</span></span>
- <span data-ttu-id="76436-1096">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="76436-1096">fecha de venc</span></span>
- <span data-ttu-id="76436-1097">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="76436-1097">vencimiento</span></span>
- <span data-ttu-id="76436-1098">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="76436-1098">válido hasta</span></span>
- <span data-ttu-id="76436-1099">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="76436-1099">valido hasta</span></span>
- <span data-ttu-id="76436-1100">vto
</span><span class="sxs-lookup"><span data-stu-id="76436-1100">vto</span></span>
- <span data-ttu-id="76436-1101">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="76436-1101">data de expiração</span></span>
- <span data-ttu-id="76436-1102">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="76436-1102">data de expiracao</span></span>
- <span data-ttu-id="76436-1103">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="76436-1103">data em que expira</span></span>
- <span data-ttu-id="76436-1104">validade
</span><span class="sxs-lookup"><span data-stu-id="76436-1104">validade</span></span>
- <span data-ttu-id="76436-1105">valor
</span><span class="sxs-lookup"><span data-stu-id="76436-1105">valor</span></span>
- <span data-ttu-id="76436-1106">vencimento
</span><span class="sxs-lookup"><span data-stu-id="76436-1106">vencimento</span></span>
- <span data-ttu-id="76436-1107">venc</span><span class="sxs-lookup"><span data-stu-id="76436-1107">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="76436-1108">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="76436-1108">Keyword_cc_name</span></span>

- <span data-ttu-id="76436-1109">amex</span><span class="sxs-lookup"><span data-stu-id="76436-1109">amex</span></span>
- <span data-ttu-id="76436-1110">
american express</span><span class="sxs-lookup"><span data-stu-id="76436-1110">american express</span></span>
- <span data-ttu-id="76436-1111">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="76436-1111">americanexpress</span></span>
- <span data-ttu-id="76436-1112">Visa</span><span class="sxs-lookup"><span data-stu-id="76436-1112">Visa</span></span>
- <span data-ttu-id="76436-1113">mastercard
</span><span class="sxs-lookup"><span data-stu-id="76436-1113">mastercard</span></span>
- <span data-ttu-id="76436-1114">master card
</span><span class="sxs-lookup"><span data-stu-id="76436-1114">master card</span></span>
- <span data-ttu-id="76436-1115">
mc
</span><span class="sxs-lookup"><span data-stu-id="76436-1115">mc</span></span> 
- <span data-ttu-id="76436-1116">mastercards</span><span class="sxs-lookup"><span data-stu-id="76436-1116">mastercards</span></span>
- <span data-ttu-id="76436-1117">
master cards</span><span class="sxs-lookup"><span data-stu-id="76436-1117">master cards</span></span>
- <span data-ttu-id="76436-1118">식사 권을의 방망이</span><span class="sxs-lookup"><span data-stu-id="76436-1118">diner's Club</span></span>
- <span data-ttu-id="76436-1119">diners club
</span><span class="sxs-lookup"><span data-stu-id="76436-1119">diners club</span></span>
- <span data-ttu-id="76436-1120">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="76436-1120">dinersclub</span></span>
- <span data-ttu-id="76436-1121">discover card
</span><span class="sxs-lookup"><span data-stu-id="76436-1121">discover card</span></span>
- <span data-ttu-id="76436-1122">discovercard
</span><span class="sxs-lookup"><span data-stu-id="76436-1122">discovercard</span></span>
- <span data-ttu-id="76436-1123">discover cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1123">discover cards</span></span>
- <span data-ttu-id="76436-1124">JCB</span><span class="sxs-lookup"><span data-stu-id="76436-1124">JCB</span></span>
- <span data-ttu-id="76436-1125">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="76436-1125">japanese card bureau</span></span>
- <span data-ttu-id="76436-1126">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="76436-1126">carte blanche</span></span>
- <span data-ttu-id="76436-1127">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="76436-1127">carteblanche</span></span>
- <span data-ttu-id="76436-1128">credit card
</span><span class="sxs-lookup"><span data-stu-id="76436-1128">credit card</span></span>
- <span data-ttu-id="76436-1129">참조란</span><span class="sxs-lookup"><span data-stu-id="76436-1129">cc#</span></span>
- <span data-ttu-id="76436-1130">참조 #:</span><span class="sxs-lookup"><span data-stu-id="76436-1130">cc#:</span></span>
- <span data-ttu-id="76436-1131">
expiration date</span><span class="sxs-lookup"><span data-stu-id="76436-1131">expiration date</span></span>
- <span data-ttu-id="76436-1132">exp date
</span><span class="sxs-lookup"><span data-stu-id="76436-1132">exp date</span></span>
- <span data-ttu-id="76436-1133">
expiry date</span><span class="sxs-lookup"><span data-stu-id="76436-1133">expiry date</span></span>
- <span data-ttu-id="76436-1134">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="76436-1134">date d’expiration</span></span>
- <span data-ttu-id="76436-1135">
date d'exp</span><span class="sxs-lookup"><span data-stu-id="76436-1135">date d'exp</span></span>
- <span data-ttu-id="76436-1136">
date expiration</span><span class="sxs-lookup"><span data-stu-id="76436-1136">date expiration</span></span>
- <span data-ttu-id="76436-1137">bank card
</span><span class="sxs-lookup"><span data-stu-id="76436-1137">bank card</span></span>
- <span data-ttu-id="76436-1138">
bankcard</span><span class="sxs-lookup"><span data-stu-id="76436-1138">bankcard</span></span>
- <span data-ttu-id="76436-1139">card number
</span><span class="sxs-lookup"><span data-stu-id="76436-1139">card number</span></span>
- <span data-ttu-id="76436-1140">card num
</span><span class="sxs-lookup"><span data-stu-id="76436-1140">card num</span></span>
- <span data-ttu-id="76436-1141">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-1141">cardnumber</span></span>
- <span data-ttu-id="76436-1142">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="76436-1142">cardnumbers</span></span>
- <span data-ttu-id="76436-1143">card numbers
</span><span class="sxs-lookup"><span data-stu-id="76436-1143">card numbers</span></span>
- <span data-ttu-id="76436-1144">creditcard
</span><span class="sxs-lookup"><span data-stu-id="76436-1144">creditcard</span></span>
- <span data-ttu-id="76436-1145">credit cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1145">credit cards</span></span>
- <span data-ttu-id="76436-1146">creditcards
</span><span class="sxs-lookup"><span data-stu-id="76436-1146">creditcards</span></span>
- <span data-ttu-id="76436-1147">ccn
</span><span class="sxs-lookup"><span data-stu-id="76436-1147">ccn</span></span>
- <span data-ttu-id="76436-1148">card holder
</span><span class="sxs-lookup"><span data-stu-id="76436-1148">card holder</span></span>
- <span data-ttu-id="76436-1149">cardholder
</span><span class="sxs-lookup"><span data-stu-id="76436-1149">cardholder</span></span>
- <span data-ttu-id="76436-1150">card holders
</span><span class="sxs-lookup"><span data-stu-id="76436-1150">card holders</span></span>
- <span data-ttu-id="76436-1151">cardholders
</span><span class="sxs-lookup"><span data-stu-id="76436-1151">cardholders</span></span>
- <span data-ttu-id="76436-1152">check card
</span><span class="sxs-lookup"><span data-stu-id="76436-1152">check card</span></span>
- <span data-ttu-id="76436-1153">checkcard
</span><span class="sxs-lookup"><span data-stu-id="76436-1153">checkcard</span></span>
- <span data-ttu-id="76436-1154">check cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1154">check cards</span></span>
- <span data-ttu-id="76436-1155">checkcards
</span><span class="sxs-lookup"><span data-stu-id="76436-1155">checkcards</span></span>
- <span data-ttu-id="76436-1156">debit card
</span><span class="sxs-lookup"><span data-stu-id="76436-1156">debit card</span></span>
- <span data-ttu-id="76436-1157">debitcard
</span><span class="sxs-lookup"><span data-stu-id="76436-1157">debitcard</span></span>
- <span data-ttu-id="76436-1158">debit cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1158">debit cards</span></span>
- <span data-ttu-id="76436-1159">debitcards
</span><span class="sxs-lookup"><span data-stu-id="76436-1159">debitcards</span></span>
- <span data-ttu-id="76436-1160">atm card
</span><span class="sxs-lookup"><span data-stu-id="76436-1160">atm card</span></span>
- <span data-ttu-id="76436-1161">atmcard
</span><span class="sxs-lookup"><span data-stu-id="76436-1161">atmcard</span></span>
- <span data-ttu-id="76436-1162">atm cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1162">atm cards</span></span>
- <span data-ttu-id="76436-1163">atmcards
</span><span class="sxs-lookup"><span data-stu-id="76436-1163">atmcards</span></span>
- <span data-ttu-id="76436-1164">
enroute</span><span class="sxs-lookup"><span data-stu-id="76436-1164">enroute</span></span>
- <span data-ttu-id="76436-1165">
en route</span><span class="sxs-lookup"><span data-stu-id="76436-1165">en route</span></span>
- <span data-ttu-id="76436-1166">card type
</span><span class="sxs-lookup"><span data-stu-id="76436-1166">card type</span></span>
- <span data-ttu-id="76436-1167">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="76436-1167">carte bancaire</span></span>
- <span data-ttu-id="76436-1168">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="76436-1168">carte de crédit</span></span>
- <span data-ttu-id="76436-1169">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="76436-1169">carte de credit</span></span>
- <span data-ttu-id="76436-1170">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="76436-1170">numéro de carte</span></span>
- <span data-ttu-id="76436-1171">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="76436-1171">numero de carte</span></span>
- <span data-ttu-id="76436-1172">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="76436-1172">nº de la carte</span></span>
- <span data-ttu-id="76436-1173">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="76436-1173">nº de carte</span></span>
- <span data-ttu-id="76436-1174">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="76436-1174">kreditkarte</span></span>
- <span data-ttu-id="76436-1175">karte
</span><span class="sxs-lookup"><span data-stu-id="76436-1175">karte</span></span>
- <span data-ttu-id="76436-1176">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="76436-1176">karteninhaber</span></span>
- <span data-ttu-id="76436-1177">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="76436-1177">karteninhabers</span></span>
- <span data-ttu-id="76436-1178">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="76436-1178">kreditkarteninhaber</span></span>
- <span data-ttu-id="76436-1179">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="76436-1179">kreditkarteninstitut</span></span>
- <span data-ttu-id="76436-1180">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="76436-1180">kreditkartentyp</span></span>
- <span data-ttu-id="76436-1181">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="76436-1181">eigentümername</span></span>
- <span data-ttu-id="76436-1182">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="76436-1182">kartennr</span></span> 
- <span data-ttu-id="76436-1183">kartennummer</span><span class="sxs-lookup"><span data-stu-id="76436-1183">kartennummer</span></span>
- <span data-ttu-id="76436-1184">
kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="76436-1184">kreditkartennummer</span></span>
- <span data-ttu-id="76436-1185">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="76436-1185">kreditkarten-nummer</span></span>
- <span data-ttu-id="76436-1186">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1186">carta di credito</span></span>
- <span data-ttu-id="76436-1187">carta credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1187">carta credito</span></span>
- <span data-ttu-id="76436-1188">카 ta</span><span class="sxs-lookup"><span data-stu-id="76436-1188">carta</span></span>
- <span data-ttu-id="76436-1189">n 카 ta</span><span class="sxs-lookup"><span data-stu-id="76436-1189">n carta</span></span>
- <span data-ttu-id="76436-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="76436-p110">nr. carta</span></span>
- <span data-ttu-id="76436-1192">veiligheid 카 ta</span><span class="sxs-lookup"><span data-stu-id="76436-1192">nr carta</span></span>
- <span data-ttu-id="76436-1193">numero carta
</span><span class="sxs-lookup"><span data-stu-id="76436-1193">numero carta</span></span>
- <span data-ttu-id="76436-1194">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="76436-1194">numero della carta</span></span>
- <span data-ttu-id="76436-1195">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="76436-1195">numero di carta</span></span>
- <span data-ttu-id="76436-1196">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1196">tarjeta credito</span></span>
- <span data-ttu-id="76436-1197">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1197">tarjeta de credito</span></span>
- <span data-ttu-id="76436-1198">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="76436-1198">tarjeta crédito</span></span>
- <span data-ttu-id="76436-1199">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="76436-1199">tarjeta de crédito</span></span>
- <span data-ttu-id="76436-1200">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="76436-1200">tarjeta de atm</span></span>
- <span data-ttu-id="76436-1201">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="76436-1201">tarjeta atm</span></span>
- <span data-ttu-id="76436-1202">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1202">tarjeta debito</span></span>
- <span data-ttu-id="76436-1203">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1203">tarjeta de debito</span></span>
- <span data-ttu-id="76436-1204">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="76436-1204">tarjeta débito</span></span>
- <span data-ttu-id="76436-1205">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="76436-1205">tarjeta de débito</span></span>
- <span data-ttu-id="76436-1206">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="76436-1206">nº de tarjeta</span></span>
- <span data-ttu-id="76436-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="76436-p111">no. de tarjeta</span></span>
- <span data-ttu-id="76436-1209">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="76436-1209">no de tarjeta</span></span>
- <span data-ttu-id="76436-1210">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="76436-1210">numero de tarjeta</span></span>
- <span data-ttu-id="76436-1211">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="76436-1211">número de tarjeta</span></span>
- <span data-ttu-id="76436-1212">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="76436-1212">tarjeta no</span></span>
- <span data-ttu-id="76436-1213">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="76436-1213">tarjetahabiente</span></span>
- <span data-ttu-id="76436-1214">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="76436-1214">cartão de crédito</span></span>
- <span data-ttu-id="76436-1215">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1215">cartão de credito</span></span>
- <span data-ttu-id="76436-1216">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="76436-1216">cartao de crédito</span></span>
- <span data-ttu-id="76436-1217">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1217">cartao de credito</span></span>
- <span data-ttu-id="76436-1218">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="76436-1218">cartão de débito</span></span>
- <span data-ttu-id="76436-1219">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="76436-1219">cartao de débito</span></span>
- <span data-ttu-id="76436-1220">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1220">cartão de debito</span></span>
- <span data-ttu-id="76436-1221">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1221">cartao de debito</span></span>
- <span data-ttu-id="76436-1222">débito automático</span><span class="sxs-lookup"><span data-stu-id="76436-1222">débito automático</span></span>
- <span data-ttu-id="76436-1223">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="76436-1223">debito automatico</span></span>
- <span data-ttu-id="76436-1224">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="76436-1224">número do cartão</span></span>
- <span data-ttu-id="76436-1225">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-1225">numero do cartão</span></span> 
- <span data-ttu-id="76436-1226">número do cartao</span><span class="sxs-lookup"><span data-stu-id="76436-1226">número do cartao</span></span>
- <span data-ttu-id="76436-1227">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="76436-1227">numero do cartao</span></span>
- <span data-ttu-id="76436-1228">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-1228">número de cartão</span></span>
- <span data-ttu-id="76436-1229">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-1229">numero de cartão</span></span>
- <span data-ttu-id="76436-1230">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-1230">número de cartao</span></span>
- <span data-ttu-id="76436-1231">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-1231">numero de cartao</span></span>
- <span data-ttu-id="76436-1232">n º cartão</span><span class="sxs-lookup"><span data-stu-id="76436-1232">nº do cartão</span></span>
- <span data-ttu-id="76436-1233">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-1233">nº do cartao</span></span>
- <span data-ttu-id="76436-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-p112">nº. do cartão</span></span>
- <span data-ttu-id="76436-1236">do no cartão</span><span class="sxs-lookup"><span data-stu-id="76436-1236">no do cartão</span></span>
- <span data-ttu-id="76436-1237">작업 없음</span><span class="sxs-lookup"><span data-stu-id="76436-1237">no do cartao</span></span>
- <span data-ttu-id="76436-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-p113">no. do cartão</span></span>
- <span data-ttu-id="76436-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="76436-1242">	크로아티아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1242">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1243">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1243">Format</span></span>

<span data-ttu-id="76436-1244">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1245">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1245">Pattern</span></span>

<span data-ttu-id="76436-1246">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1247">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1247">Checksum</span></span>

<span data-ttu-id="76436-1248">없음</span><span class="sxs-lookup"><span data-stu-id="76436-1248">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1249">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1249">Definition</span></span>

<span data-ttu-id="76436-1250">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1251">Func_croatia_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1251">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1252">Keyword_croatia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1252">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1253">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1253">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="76436-1254">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="76436-1254">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="76436-1255">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="76436-1255">Croatian identity card</span></span>
- <span data-ttu-id="76436-1256">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="76436-1256">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="76436-1257">	크로아티아 개인 식별(OIB) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1257">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1258">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1258">Format</span></span>

<span data-ttu-id="76436-1259">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1259">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1260">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1260">Pattern</span></span>

<span data-ttu-id="76436-1261">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-1261">11 digits:</span></span>
- <span data-ttu-id="76436-1262">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1262">10 digits</span></span> 
- <span data-ttu-id="76436-1263">최종 자릿수는 국제 데이터 교환 목적을 위한 검사 숫자 이며, HR는 11 자리 숫자 앞에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1263">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1264">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1264">Checksum</span></span>

<span data-ttu-id="76436-1265">예</span><span class="sxs-lookup"><span data-stu-id="76436-1265">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1266">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1266">Definition</span></span>

<span data-ttu-id="76436-1267">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1267">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1268">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1268">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1269">Keyword_croatia_oib_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1269">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="76436-1270">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1270">The checksum passes.</span></span>

<span data-ttu-id="76436-1271">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1272">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1272">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1273">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1273">The checksum passes.</span></span>

```
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1274">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1274">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="76436-1275">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="76436-1275">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="76436-1276">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="76436-1276">Personal Identification Number</span></span>
- <span data-ttu-id="76436-1277">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="76436-1277">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="76436-1278">OIB
</span><span class="sxs-lookup"><span data-stu-id="76436-1278">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="76436-1279">체코어 개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1279">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1280">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1280">Format</span></span>

<span data-ttu-id="76436-1281">선택적 슬래시 (이전 형식)가 있는 9 자리 숫자와 슬래시 (새 형식)가 있는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1281">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1282">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1282">Pattern</span></span>

<span data-ttu-id="76436-1283">9 자리 숫자 (이전 형식):</span><span class="sxs-lookup"><span data-stu-id="76436-1283">Nine digits (old format):</span></span>
- <span data-ttu-id="76436-1284">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1284">Nine digits</span></span>

<span data-ttu-id="76436-1285">또는</span><span class="sxs-lookup"><span data-stu-id="76436-1285">OR</span></span>

- <span data-ttu-id="76436-1286">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1286">Six digits that represent date of birth</span></span>
- <span data-ttu-id="76436-1287">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="76436-1287">A forward slash</span></span>
- <span data-ttu-id="76436-1288">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1288">Three digits</span></span>

<span data-ttu-id="76436-1289">10 자리 숫자 (새 형식):</span><span class="sxs-lookup"><span data-stu-id="76436-1289">10 digits (new format):</span></span>
- <span data-ttu-id="76436-1290">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1290">10 digits</span></span>

<span data-ttu-id="76436-1291">또는</span><span class="sxs-lookup"><span data-stu-id="76436-1291">OR</span></span>

- <span data-ttu-id="76436-1292">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1292">Six digits that represent date of birth</span></span>
- <span data-ttu-id="76436-1293">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="76436-1293">A forward slash</span></span> 
- <span data-ttu-id="76436-1294">마지막 숫자가 검사 숫자인 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1294">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1295">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1295">Checksum</span></span>

<span data-ttu-id="76436-1296">예</span><span class="sxs-lookup"><span data-stu-id="76436-1296">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1297">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1297">Definition</span></span>

<span data-ttu-id="76436-p115">DLP 정책은 300 문자 근사에서 Func_czech_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다. Keyword_czech_id_card에서 키워드가 발견 되었습니다. 체크섬이 통과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="76436-1301">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1301">Keywords</span></span>

- <span data-ttu-id="76436-1302">체코어 개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1302">czech personal identity number</span></span>
- <span data-ttu-id="76436-1303">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="76436-1303">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="76436-1304">	덴마크 개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1304">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1305">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1305">Format</span></span>

<span data-ttu-id="76436-1306">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1306">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1307">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1307">Pattern</span></span>

<span data-ttu-id="76436-1308">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-1308">10 digits:</span></span>
- <span data-ttu-id="76436-1309">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-1309">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="76436-1310">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-1310">A hyphen</span></span> 
- <span data-ttu-id="76436-1311">마지막 숫자가 검사 숫자인 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1311">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1312">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1312">Checksum</span></span>

<span data-ttu-id="76436-1313">예</span><span class="sxs-lookup"><span data-stu-id="76436-1313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1314">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1314">Definition</span></span>

<span data-ttu-id="76436-p116">DLP 정책은 300 문자 (예: Regex_denmark_id)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다. Keyword_denmark_id에서 키워드가 발견 되었습니다. 체크섬이 통과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1318">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1318">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="76436-1319">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="76436-1319">Keyword_denmark_id</span></span>

- <span data-ttu-id="76436-1320">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="76436-1320">Personal Identification Number</span></span>
- <span data-ttu-id="76436-1321">CPR</span><span class="sxs-lookup"><span data-stu-id="76436-1321">CPR</span></span>
- <span data-ttu-id="76436-1322">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="76436-1322">Det Centrale Personregister</span></span>
- <span data-ttu-id="76436-1323">Personnummer</span><span class="sxs-lookup"><span data-stu-id="76436-1323">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="76436-1324">DEA(약물 집행 기구) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1324">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1325">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1325">Format</span></span>

<span data-ttu-id="76436-1326">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1326">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1327">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1327">Pattern</span></span>

<span data-ttu-id="76436-1328">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1328">Pattern must include all of the following:</span></span>
- <span data-ttu-id="76436-1329">등록 코드에 해당하는 abcdefghjklmnprstux 중 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-1329">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="76436-1330">등록자 성의 첫 문자에 해당하는 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-1330">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="76436-1331">검사 숫자의 마지막 7개 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1331">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1332">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1332">Checksum</span></span>

<span data-ttu-id="76436-1333">예</span><span class="sxs-lookup"><span data-stu-id="76436-1333">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1334">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1334">Definition</span></span>

<span data-ttu-id="76436-1335">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1335">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1336">Func_dea_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1336">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1337">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1337">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1338">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1338">Keywords</span></span>

<span data-ttu-id="76436-1339">없음</span><span class="sxs-lookup"><span data-stu-id="76436-1339">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="76436-1340">유럽 직불 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1340">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1341">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1341">Format</span></span>

<span data-ttu-id="76436-1342">16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1342">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1343">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1343">Pattern</span></span>

<span data-ttu-id="76436-1344">매우 복잡하고 강력한 패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1344">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1345">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1345">Checksum</span></span>

<span data-ttu-id="76436-1346">예</span><span class="sxs-lookup"><span data-stu-id="76436-1346">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1347">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1347">Definition</span></span>

<span data-ttu-id="76436-1348">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1348">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1349">Func_eu_debit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1349">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1350">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1350">At least one of the following is true:</span></span>
    - <span data-ttu-id="76436-1351">Keyword_eu_debit_card의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1351">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="76436-1352">Keyword_card_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1352">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="76436-1353">Keyword_card_security_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1353">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="76436-1354">Keyword_card_expiration_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1354">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="76436-1355">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1355">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="76436-1356">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1356">The checksum passes.</span></span>

```
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1357">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1357">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="76436-1358">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="76436-1358">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="76436-1359">계정 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1359">account number</span></span> 
- <span data-ttu-id="76436-1360">card number
</span><span class="sxs-lookup"><span data-stu-id="76436-1360">card number</span></span> 
- <span data-ttu-id="76436-1361">card no.
</span><span class="sxs-lookup"><span data-stu-id="76436-1361">card no.</span></span> 
- <span data-ttu-id="76436-1362">security number
</span><span class="sxs-lookup"><span data-stu-id="76436-1362">security number</span></span> 
- <span data-ttu-id="76436-1363">참조란</span><span class="sxs-lookup"><span data-stu-id="76436-1363">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="76436-1364">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="76436-1364">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="76436-1365">acct nbr
</span><span class="sxs-lookup"><span data-stu-id="76436-1365">acct nbr</span></span> 
- <span data-ttu-id="76436-1366">acct num
</span><span class="sxs-lookup"><span data-stu-id="76436-1366">acct num</span></span> 
- <span data-ttu-id="76436-1367">acct no
</span><span class="sxs-lookup"><span data-stu-id="76436-1367">acct no</span></span> 
- <span data-ttu-id="76436-1368">american express
</span><span class="sxs-lookup"><span data-stu-id="76436-1368">american express</span></span> 
- <span data-ttu-id="76436-1369">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="76436-1369">americanexpress</span></span> 
- <span data-ttu-id="76436-1370">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="76436-1370">americano espresso</span></span> 
- <span data-ttu-id="76436-1371">amex</span><span class="sxs-lookup"><span data-stu-id="76436-1371">amex</span></span> 
- <span data-ttu-id="76436-1372">atm card
</span><span class="sxs-lookup"><span data-stu-id="76436-1372">atm card</span></span> 
- <span data-ttu-id="76436-1373">atm cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1373">atm cards</span></span> 
- <span data-ttu-id="76436-1374">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="76436-1374">atm kaart</span></span> 
- <span data-ttu-id="76436-1375">atmcard
</span><span class="sxs-lookup"><span data-stu-id="76436-1375">atmcard</span></span> 
- <span data-ttu-id="76436-1376">atmcards
</span><span class="sxs-lookup"><span data-stu-id="76436-1376">atmcards</span></span> 
- <span data-ttu-id="76436-1377">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="76436-1377">atmkaart</span></span> 
- <span data-ttu-id="76436-1378">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="76436-1378">atmkaarten</span></span> 
- <span data-ttu-id="76436-1379">bancontact
</span><span class="sxs-lookup"><span data-stu-id="76436-1379">bancontact</span></span> 
- <span data-ttu-id="76436-1380">bank card
</span><span class="sxs-lookup"><span data-stu-id="76436-1380">bank card</span></span> 
- <span data-ttu-id="76436-1381">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="76436-1381">bankkaart</span></span> 
- <span data-ttu-id="76436-1382">card holder
</span><span class="sxs-lookup"><span data-stu-id="76436-1382">card holder</span></span> 
- <span data-ttu-id="76436-1383">card holders
</span><span class="sxs-lookup"><span data-stu-id="76436-1383">card holders</span></span> 
- <span data-ttu-id="76436-1384">card num
</span><span class="sxs-lookup"><span data-stu-id="76436-1384">card num</span></span> 
- <span data-ttu-id="76436-1385">card number
</span><span class="sxs-lookup"><span data-stu-id="76436-1385">card number</span></span> 
- <span data-ttu-id="76436-1386">card numbers
</span><span class="sxs-lookup"><span data-stu-id="76436-1386">card numbers</span></span> 
- <span data-ttu-id="76436-1387">card type
</span><span class="sxs-lookup"><span data-stu-id="76436-1387">card type</span></span> 
- <span data-ttu-id="76436-1388">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="76436-1388">cardano numerico</span></span> 
- <span data-ttu-id="76436-1389">cardholder
</span><span class="sxs-lookup"><span data-stu-id="76436-1389">cardholder</span></span> 
- <span data-ttu-id="76436-1390">cardholders
</span><span class="sxs-lookup"><span data-stu-id="76436-1390">cardholders</span></span> 
- <span data-ttu-id="76436-1391">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-1391">cardnumber</span></span> 
- <span data-ttu-id="76436-1392">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="76436-1392">cardnumbers</span></span> 
- <span data-ttu-id="76436-1393">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="76436-1393">carta bianca</span></span> 
- <span data-ttu-id="76436-1394">carta credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1394">carta credito</span></span> 
- <span data-ttu-id="76436-1395">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1395">carta di credito</span></span> 
- <span data-ttu-id="76436-1396">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1396">cartao de credito</span></span> 
- <span data-ttu-id="76436-1397">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="76436-1397">cartao de crédito</span></span> 
- <span data-ttu-id="76436-1398">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1398">cartao de debito</span></span> 
- <span data-ttu-id="76436-1399">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="76436-1399">cartao de débito</span></span> 
- <span data-ttu-id="76436-1400">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="76436-1400">carte bancaire</span></span> 
- <span data-ttu-id="76436-1401">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="76436-1401">carte blanche</span></span> 
- <span data-ttu-id="76436-1402">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="76436-1402">carte bleue</span></span> 
- <span data-ttu-id="76436-1403">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="76436-1403">carte de credit</span></span> 
- <span data-ttu-id="76436-1404">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="76436-1404">carte de crédit</span></span> 
- <span data-ttu-id="76436-1405">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1405">carte di credito</span></span> 
- <span data-ttu-id="76436-1406">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="76436-1406">carteblanche</span></span> 
- <span data-ttu-id="76436-1407">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1407">cartão de credito</span></span> 
- <span data-ttu-id="76436-1408">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="76436-1408">cartão de crédito</span></span> 
- <span data-ttu-id="76436-1409">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1409">cartão de debito</span></span> 
- <span data-ttu-id="76436-1410">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="76436-1410">cartão de débito</span></span> 
- <span data-ttu-id="76436-1411">cb
</span><span class="sxs-lookup"><span data-stu-id="76436-1411">cb</span></span> 
- <span data-ttu-id="76436-1412">ccn
</span><span class="sxs-lookup"><span data-stu-id="76436-1412">ccn</span></span> 
- <span data-ttu-id="76436-1413">check card
</span><span class="sxs-lookup"><span data-stu-id="76436-1413">check card</span></span> 
- <span data-ttu-id="76436-1414">check cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1414">check cards</span></span> 
- <span data-ttu-id="76436-1415">checkcard
</span><span class="sxs-lookup"><span data-stu-id="76436-1415">checkcard</span></span>
- <span data-ttu-id="76436-1416">checkcards
</span><span class="sxs-lookup"><span data-stu-id="76436-1416">checkcards</span></span> 
- <span data-ttu-id="76436-1417">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="76436-1417">chequekaart</span></span> 
- <span data-ttu-id="76436-1418">cirrus
</span><span class="sxs-lookup"><span data-stu-id="76436-1418">cirrus</span></span> 
- <span data-ttu-id="76436-1419">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="76436-1419">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="76436-1420">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="76436-1420">controlekaart</span></span> 
- <span data-ttu-id="76436-1421">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="76436-1421">controlekaarten</span></span> 
- <span data-ttu-id="76436-1422">credit card
</span><span class="sxs-lookup"><span data-stu-id="76436-1422">credit card</span></span> 
- <span data-ttu-id="76436-1423">credit cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1423">credit cards</span></span> 
- <span data-ttu-id="76436-1424">creditcard
</span><span class="sxs-lookup"><span data-stu-id="76436-1424">creditcard</span></span> 
- <span data-ttu-id="76436-1425">creditcards
</span><span class="sxs-lookup"><span data-stu-id="76436-1425">creditcards</span></span> 
- <span data-ttu-id="76436-1426">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="76436-1426">debetkaart</span></span> 
- <span data-ttu-id="76436-1427">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="76436-1427">debetkaarten</span></span> 
- <span data-ttu-id="76436-1428">debit card
</span><span class="sxs-lookup"><span data-stu-id="76436-1428">debit card</span></span> 
- <span data-ttu-id="76436-1429">debit cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1429">debit cards</span></span> 
- <span data-ttu-id="76436-1430">debitcard
</span><span class="sxs-lookup"><span data-stu-id="76436-1430">debitcard</span></span> 
- <span data-ttu-id="76436-1431">debitcards
</span><span class="sxs-lookup"><span data-stu-id="76436-1431">debitcards</span></span> 
- <span data-ttu-id="76436-1432">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="76436-1432">debito automatico</span></span> 
- <span data-ttu-id="76436-1433">diners club
</span><span class="sxs-lookup"><span data-stu-id="76436-1433">diners club</span></span> 
- <span data-ttu-id="76436-1434">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="76436-1434">dinersclub</span></span> 
- <span data-ttu-id="76436-1435">찾아보십시오</span><span class="sxs-lookup"><span data-stu-id="76436-1435">discover</span></span> 
- <span data-ttu-id="76436-1436">discover card
</span><span class="sxs-lookup"><span data-stu-id="76436-1436">discover card</span></span> 
- <span data-ttu-id="76436-1437">discover cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1437">discover cards</span></span> 
- <span data-ttu-id="76436-1438">discovercard
</span><span class="sxs-lookup"><span data-stu-id="76436-1438">discovercard</span></span> 
- <span data-ttu-id="76436-1439">discovercards
</span><span class="sxs-lookup"><span data-stu-id="76436-1439">discovercards</span></span> 
- <span data-ttu-id="76436-1440">débito automático</span><span class="sxs-lookup"><span data-stu-id="76436-1440">débito automático</span></span>
- <span data-ttu-id="76436-1441">
edc
</span><span class="sxs-lookup"><span data-stu-id="76436-1441">edc</span></span> 
- <span data-ttu-id="76436-1442">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="76436-1442">eigentümername</span></span> 
- <span data-ttu-id="76436-1443">european debit card
</span><span class="sxs-lookup"><span data-stu-id="76436-1443">european debit card</span></span> 
- <span data-ttu-id="76436-1444">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="76436-1444">hoofdkaart</span></span> 
- <span data-ttu-id="76436-1445">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="76436-1445">hoofdkaarten</span></span> 
- <span data-ttu-id="76436-1446">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="76436-1446">in viaggio</span></span> 
- <span data-ttu-id="76436-1447">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="76436-1447">japanese card bureau</span></span> 
- <span data-ttu-id="76436-1448">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="76436-1448">japanse kaartdienst</span></span> 
- <span data-ttu-id="76436-1449">jcb
</span><span class="sxs-lookup"><span data-stu-id="76436-1449">jcb</span></span> 
- <span data-ttu-id="76436-1450">kaart
</span><span class="sxs-lookup"><span data-stu-id="76436-1450">kaart</span></span> 
- <span data-ttu-id="76436-1451">kaart num
</span><span class="sxs-lookup"><span data-stu-id="76436-1451">kaart num</span></span> 
- <span data-ttu-id="76436-1452">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="76436-1452">kaartaantal</span></span> 
- <span data-ttu-id="76436-1453">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="76436-1453">kaartaantallen</span></span> 
- <span data-ttu-id="76436-1454">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="76436-1454">kaarthouder</span></span> 
- <span data-ttu-id="76436-1455">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="76436-1455">kaarthouders</span></span> 
- <span data-ttu-id="76436-1456">karte
</span><span class="sxs-lookup"><span data-stu-id="76436-1456">karte</span></span>  
- <span data-ttu-id="76436-1457">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="76436-1457">karteninhaber</span></span> 
- <span data-ttu-id="76436-1458">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="76436-1458">karteninhabers</span></span>
- <span data-ttu-id="76436-1459">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="76436-1459">kartennr</span></span> 
- <span data-ttu-id="76436-1460">kartennummer</span><span class="sxs-lookup"><span data-stu-id="76436-1460">kartennummer</span></span> 
- <span data-ttu-id="76436-1461">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="76436-1461">kreditkarte</span></span> 
- <span data-ttu-id="76436-1462">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="76436-1462">kreditkarten-nummer</span></span> 
- <span data-ttu-id="76436-1463">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="76436-1463">kreditkarteninhaber</span></span> 
- <span data-ttu-id="76436-1464">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="76436-1464">kreditkarteninstitut</span></span> 
- <span data-ttu-id="76436-1465">kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1465">kreditkartennummer</span></span> 
- <span data-ttu-id="76436-1466">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="76436-1466">kreditkartentyp</span></span> 
- <span data-ttu-id="76436-1467">maestro
</span><span class="sxs-lookup"><span data-stu-id="76436-1467">maestro</span></span> 
- <span data-ttu-id="76436-1468">master card
</span><span class="sxs-lookup"><span data-stu-id="76436-1468">master card</span></span> 
- <span data-ttu-id="76436-1469">master cards
</span><span class="sxs-lookup"><span data-stu-id="76436-1469">master cards</span></span> 
- <span data-ttu-id="76436-1470">mastercard
</span><span class="sxs-lookup"><span data-stu-id="76436-1470">mastercard</span></span> 
- <span data-ttu-id="76436-1471">mastercards</span><span class="sxs-lookup"><span data-stu-id="76436-1471">mastercards</span></span> 
- <span data-ttu-id="76436-1472">mc</span><span class="sxs-lookup"><span data-stu-id="76436-1472">mc</span></span> 
- <span data-ttu-id="76436-1473">mister cash
</span><span class="sxs-lookup"><span data-stu-id="76436-1473">mister cash</span></span> 
- <span data-ttu-id="76436-1474">n 카 ta</span><span class="sxs-lookup"><span data-stu-id="76436-1474">n carta</span></span> 
- <span data-ttu-id="76436-1475">카 ta</span><span class="sxs-lookup"><span data-stu-id="76436-1475">carta</span></span> 
- <span data-ttu-id="76436-1476">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="76436-1476">no de tarjeta</span></span> 
- <span data-ttu-id="76436-1477">작업 없음</span><span class="sxs-lookup"><span data-stu-id="76436-1477">no do cartao</span></span> 
- <span data-ttu-id="76436-1478">do no cartão</span><span class="sxs-lookup"><span data-stu-id="76436-1478">no do cartão</span></span> 
- <span data-ttu-id="76436-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="76436-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="76436-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-p118">no. do cartao</span></span> 
- <span data-ttu-id="76436-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-p119">no. do cartão</span></span> 
- <span data-ttu-id="76436-1485">veiligheid 카 ta</span><span class="sxs-lookup"><span data-stu-id="76436-1485">nr carta</span></span> 
- <span data-ttu-id="76436-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="76436-p120">nr. carta</span></span> 
- <span data-ttu-id="76436-1488">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="76436-1488">numeri di scheda</span></span> 
- <span data-ttu-id="76436-1489">numero carta
</span><span class="sxs-lookup"><span data-stu-id="76436-1489">numero carta</span></span> 
- <span data-ttu-id="76436-1490">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-1490">numero de cartao</span></span> 
- <span data-ttu-id="76436-1491">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="76436-1491">numero de carte</span></span> 
- <span data-ttu-id="76436-1492">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-1492">numero de cartão</span></span> 
- <span data-ttu-id="76436-1493">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="76436-1493">numero de tarjeta</span></span>
- <span data-ttu-id="76436-1494">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="76436-1494">numero della carta</span></span> 
- <span data-ttu-id="76436-1495">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="76436-1495">numero di carta</span></span> 
- <span data-ttu-id="76436-1496">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="76436-1496">numero di scheda</span></span> 
- <span data-ttu-id="76436-1497">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-1497">numero do cartao</span></span> 
- <span data-ttu-id="76436-1498">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-1498">numero do cartão</span></span> 
- <span data-ttu-id="76436-1499">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="76436-1499">numéro de carte</span></span> 
- <span data-ttu-id="76436-1500">nº carta
</span><span class="sxs-lookup"><span data-stu-id="76436-1500">nº carta</span></span> 
- <span data-ttu-id="76436-1501">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="76436-1501">nº de carte</span></span> 
- <span data-ttu-id="76436-1502">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="76436-1502">nº de la carte</span></span> 
- <span data-ttu-id="76436-1503">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="76436-1503">nº de tarjeta</span></span> 
- <span data-ttu-id="76436-1504">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-1504">nº do cartao</span></span> 
- <span data-ttu-id="76436-1505">n º cartão</span><span class="sxs-lookup"><span data-stu-id="76436-1505">nº do cartão</span></span> 
- <span data-ttu-id="76436-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-p121">nº. do cartão</span></span> 
- <span data-ttu-id="76436-1508">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="76436-1508">número de cartao</span></span> 
- <span data-ttu-id="76436-1509">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="76436-1509">número de cartão</span></span> 
- <span data-ttu-id="76436-1510">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="76436-1510">número de tarjeta</span></span> 
- <span data-ttu-id="76436-1511">número do cartao</span><span class="sxs-lookup"><span data-stu-id="76436-1511">número do cartao</span></span> 
- <span data-ttu-id="76436-1512">scheda dell'assegno
</span><span class="sxs-lookup"><span data-stu-id="76436-1512">scheda dell'assegno</span></span> 
- <span data-ttu-id="76436-1513">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="76436-1513">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="76436-1514">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="76436-1514">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="76436-1515">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="76436-1515">scheda della banca</span></span> 
- <span data-ttu-id="76436-1516">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="76436-1516">scheda di controllo</span></span> 
- <span data-ttu-id="76436-1517">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1517">scheda di debito</span></span> 
- <span data-ttu-id="76436-1518">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="76436-1518">scheda matrice</span></span> 
- <span data-ttu-id="76436-1519">schede dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="76436-1519">schede dell'atmosfera</span></span> 
- <span data-ttu-id="76436-1520">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="76436-1520">schede di controllo</span></span> 
- <span data-ttu-id="76436-1521">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1521">schede di debito</span></span> 
- <span data-ttu-id="76436-1522">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="76436-1522">schede matrici</span></span> 
- <span data-ttu-id="76436-1523">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="76436-1523">scoprono la scheda</span></span> 
- <span data-ttu-id="76436-1524">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="76436-1524">scoprono le schede</span></span> 
- <span data-ttu-id="76436-1525">solo
</span><span class="sxs-lookup"><span data-stu-id="76436-1525">solo</span></span> 
- <span data-ttu-id="76436-1526">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="76436-1526">supporti di scheda</span></span> 
- <span data-ttu-id="76436-1527">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="76436-1527">supporto di scheda</span></span> 
- <span data-ttu-id="76436-1528">스위치</span><span class="sxs-lookup"><span data-stu-id="76436-1528">switch</span></span> 
- <span data-ttu-id="76436-1529">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="76436-1529">tarjeta atm</span></span> 
- <span data-ttu-id="76436-1530">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1530">tarjeta credito</span></span> 
- <span data-ttu-id="76436-1531">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="76436-1531">tarjeta de atm</span></span> 
- <span data-ttu-id="76436-1532">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="76436-1532">tarjeta de credito</span></span> 
- <span data-ttu-id="76436-1533">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1533">tarjeta de debito</span></span> 
- <span data-ttu-id="76436-1534">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="76436-1534">tarjeta debito</span></span> 
- <span data-ttu-id="76436-1535">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="76436-1535">tarjeta no</span></span>
- <span data-ttu-id="76436-1536">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="76436-1536">tarjetahabiente</span></span> 
- <span data-ttu-id="76436-1537">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="76436-1537">tipo della scheda</span></span> 
- <span data-ttu-id="76436-1538">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="76436-1538">ufficio giapponese della</span></span> 
- <span data-ttu-id="76436-1539">scheda
</span><span class="sxs-lookup"><span data-stu-id="76436-1539">scheda</span></span> 
- <span data-ttu-id="76436-1540">v pay
</span><span class="sxs-lookup"><span data-stu-id="76436-1540">v pay</span></span> 
- <span data-ttu-id="76436-1541">v-지급</span><span class="sxs-lookup"><span data-stu-id="76436-1541">v-pay</span></span> 
- <span data-ttu-id="76436-1542">visa
</span><span class="sxs-lookup"><span data-stu-id="76436-1542">visa</span></span> 
- <span data-ttu-id="76436-1543">visa plus
</span><span class="sxs-lookup"><span data-stu-id="76436-1543">visa plus</span></span> 
- <span data-ttu-id="76436-1544">visa electron
</span><span class="sxs-lookup"><span data-stu-id="76436-1544">visa electron</span></span> 
- <span data-ttu-id="76436-1545">visto
</span><span class="sxs-lookup"><span data-stu-id="76436-1545">visto</span></span> 
- <span data-ttu-id="76436-1546">visum
</span><span class="sxs-lookup"><span data-stu-id="76436-1546">visum</span></span> 
- <span data-ttu-id="76436-1547">vpay
</span><span class="sxs-lookup"><span data-stu-id="76436-1547">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="76436-1548">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="76436-1548">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="76436-1549">card identification number</span><span class="sxs-lookup"><span data-stu-id="76436-1549">card identification number</span></span>
- <span data-ttu-id="76436-1550">card verification</span><span class="sxs-lookup"><span data-stu-id="76436-1550">card verification</span></span> 
- <span data-ttu-id="76436-1551">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="76436-1551">cardi la verifica</span></span> 
- <span data-ttu-id="76436-1552">cid
</span><span class="sxs-lookup"><span data-stu-id="76436-1552">cid</span></span> 
- <span data-ttu-id="76436-1553">cod seg</span><span class="sxs-lookup"><span data-stu-id="76436-1553">cod seg</span></span> 
- <span data-ttu-id="76436-1554">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="76436-1554">cod seguranca</span></span> 
- <span data-ttu-id="76436-1555">cod segurança</span><span class="sxs-lookup"><span data-stu-id="76436-1555">cod segurança</span></span> 
- <span data-ttu-id="76436-1556">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="76436-1556">cod sicurezza</span></span> 
- <span data-ttu-id="76436-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="76436-p122">cod. seg</span></span> 
- <span data-ttu-id="76436-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="76436-p123">cod. seguranca</span></span> 
- <span data-ttu-id="76436-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="76436-p124">cod. segurança</span></span> 
- <span data-ttu-id="76436-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="76436-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="76436-1565">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="76436-1565">codice di sicurezza</span></span> 
- <span data-ttu-id="76436-1566">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="76436-1566">codice di verifica</span></span> 
- <span data-ttu-id="76436-1567">codigo
</span><span class="sxs-lookup"><span data-stu-id="76436-1567">codigo</span></span> 
- <span data-ttu-id="76436-1568">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="76436-1568">codigo de seguranca</span></span> 
- <span data-ttu-id="76436-1569">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="76436-1569">codigo de segurança</span></span> 
- <span data-ttu-id="76436-1570">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="76436-1570">crittogramma</span></span> 
- <span data-ttu-id="76436-1571">cryptogram
</span><span class="sxs-lookup"><span data-stu-id="76436-1571">cryptogram</span></span> 
- <span data-ttu-id="76436-1572">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="76436-1572">cryptogramme</span></span> 
- <span data-ttu-id="76436-1573">cv2</span><span class="sxs-lookup"><span data-stu-id="76436-1573">cv2</span></span> 
- <span data-ttu-id="76436-1574">cvc
</span><span class="sxs-lookup"><span data-stu-id="76436-1574">cvc</span></span> 
- <span data-ttu-id="76436-1575">cvc2</span><span class="sxs-lookup"><span data-stu-id="76436-1575">cvc2</span></span> 
- <span data-ttu-id="76436-1576">cvn
</span><span class="sxs-lookup"><span data-stu-id="76436-1576">cvn</span></span> 
- <span data-ttu-id="76436-1577">cvv
</span><span class="sxs-lookup"><span data-stu-id="76436-1577">cvv</span></span> 
- <span data-ttu-id="76436-1578">cvv2</span><span class="sxs-lookup"><span data-stu-id="76436-1578">cvv2</span></span> 
- <span data-ttu-id="76436-1579">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="76436-1579">cód seguranca</span></span> 
- <span data-ttu-id="76436-1580">cód segurança</span><span class="sxs-lookup"><span data-stu-id="76436-1580">cód segurança</span></span> 
- <span data-ttu-id="76436-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="76436-p126">cód. seguranca</span></span> 
- <span data-ttu-id="76436-p127">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="76436-p127">cód. segurança</span></span> 
- <span data-ttu-id="76436-1585">código
</span><span class="sxs-lookup"><span data-stu-id="76436-1585">código</span></span> 
- <span data-ttu-id="76436-1586">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="76436-1586">código de seguranca</span></span> 
- <span data-ttu-id="76436-1587">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="76436-1587">código de segurança</span></span> 
- <span data-ttu-id="76436-1588">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="76436-1588">de kaart controle</span></span> 
- <span data-ttu-id="76436-1589">geeft nr uit
</span><span class="sxs-lookup"><span data-stu-id="76436-1589">geeft nr uit</span></span> 
- <span data-ttu-id="76436-1590">issue no
</span><span class="sxs-lookup"><span data-stu-id="76436-1590">issue no</span></span> 
- <span data-ttu-id="76436-1591">issue number
</span><span class="sxs-lookup"><span data-stu-id="76436-1591">issue number</span></span> 
- <span data-ttu-id="76436-1592">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1592">kaartidentificatienummer</span></span> 
- <span data-ttu-id="76436-1593">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1593">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="76436-1594">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1594">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="76436-1595">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="76436-1595">kwestieaantal</span></span> 
- <span data-ttu-id="76436-p128">no. dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="76436-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="76436-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="76436-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="76436-1600">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="76436-1600">numero de securite</span></span> 
- <span data-ttu-id="76436-1601">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="76436-1601">numero de verificacao</span></span> 
- <span data-ttu-id="76436-1602">numero dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="76436-1602">numero dell'edizione</span></span> 
- <span data-ttu-id="76436-1603">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="76436-1603">numero di identificazione della</span></span> 
- <span data-ttu-id="76436-1604">scheda
</span><span class="sxs-lookup"><span data-stu-id="76436-1604">scheda</span></span> 
- <span data-ttu-id="76436-1605">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="76436-1605">numero di sicurezza</span></span> 
- <span data-ttu-id="76436-1606">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="76436-1606">numero van veiligheid</span></span> 
- <span data-ttu-id="76436-1607">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="76436-1607">numéro de sécurité</span></span> 
- <span data-ttu-id="76436-1608">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="76436-1608">nº autorizzazione</span></span> 
- <span data-ttu-id="76436-1609">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="76436-1609">número de verificação</span></span> 
- <span data-ttu-id="76436-1610">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="76436-1610">perno il blocco</span></span> 
- <span data-ttu-id="76436-1611">pin block
</span><span class="sxs-lookup"><span data-stu-id="76436-1611">pin block</span></span> 
- <span data-ttu-id="76436-1612">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="76436-1612">prufziffer</span></span> 
- <span data-ttu-id="76436-1613">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="76436-1613">prüfziffer</span></span> 
- <span data-ttu-id="76436-1614">security code
</span><span class="sxs-lookup"><span data-stu-id="76436-1614">security code</span></span> 
- <span data-ttu-id="76436-1615">security no
</span><span class="sxs-lookup"><span data-stu-id="76436-1615">security no</span></span> 
- <span data-ttu-id="76436-1616">security number
</span><span class="sxs-lookup"><span data-stu-id="76436-1616">security number</span></span> 
- <span data-ttu-id="76436-1617">sicherheits kode
</span><span class="sxs-lookup"><span data-stu-id="76436-1617">sicherheits kode</span></span> 
- <span data-ttu-id="76436-1618">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="76436-1618">sicherheitscode</span></span> 
- <span data-ttu-id="76436-1619">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1619">sicherheitsnummer</span></span> 
- <span data-ttu-id="76436-1620">speldblok
</span><span class="sxs-lookup"><span data-stu-id="76436-1620">speldblok</span></span> 
- <span data-ttu-id="76436-1621">veiligheid 번호:
</span><span class="sxs-lookup"><span data-stu-id="76436-1621">veiligheid nr</span></span> 
- <span data-ttu-id="76436-1622">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="76436-1622">veiligheidsaantal</span></span> 
- <span data-ttu-id="76436-1623">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="76436-1623">veiligheidscode</span></span> 
- <span data-ttu-id="76436-1624">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="76436-1624">veiligheidsnummer</span></span> 
- <span data-ttu-id="76436-1625">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="76436-1625">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="76436-1626">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="76436-1626">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="76436-1627">ablauf
</span><span class="sxs-lookup"><span data-stu-id="76436-1627">ablauf</span></span> 
- <span data-ttu-id="76436-1628">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="76436-1628">data de expiracao</span></span> 
- <span data-ttu-id="76436-1629">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="76436-1629">data de expiração</span></span> 
- <span data-ttu-id="76436-1630">data del exp
</span><span class="sxs-lookup"><span data-stu-id="76436-1630">data del exp</span></span> 
- <span data-ttu-id="76436-1631">data di exp
</span><span class="sxs-lookup"><span data-stu-id="76436-1631">data di exp</span></span> 
- <span data-ttu-id="76436-1632">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="76436-1632">data di scadenza</span></span> 
- <span data-ttu-id="76436-1633">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="76436-1633">data em que expira</span></span> 
- <span data-ttu-id="76436-1634">data scad
</span><span class="sxs-lookup"><span data-stu-id="76436-1634">data scad</span></span> 
- <span data-ttu-id="76436-1635">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="76436-1635">data scadenza</span></span> 
- <span data-ttu-id="76436-1636">date de validité
</span><span class="sxs-lookup"><span data-stu-id="76436-1636">date de validité</span></span> 
- <span data-ttu-id="76436-1637">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="76436-1637">datum afloop</span></span> 
- <span data-ttu-id="76436-1638">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="76436-1638">datum van exp</span></span> 
- <span data-ttu-id="76436-1639">de afloop
</span><span class="sxs-lookup"><span data-stu-id="76436-1639">de afloop</span></span> 
- <span data-ttu-id="76436-1640">espira
</span><span class="sxs-lookup"><span data-stu-id="76436-1640">espira</span></span> 
- <span data-ttu-id="76436-1641">espira
</span><span class="sxs-lookup"><span data-stu-id="76436-1641">espira</span></span> 
- <span data-ttu-id="76436-1642">exp date
</span><span class="sxs-lookup"><span data-stu-id="76436-1642">exp date</span></span> 
- <span data-ttu-id="76436-1643">exp datum
</span><span class="sxs-lookup"><span data-stu-id="76436-1643">exp datum</span></span> 
- <span data-ttu-id="76436-1644">행사</span><span class="sxs-lookup"><span data-stu-id="76436-1644">expiration</span></span> 
- <span data-ttu-id="76436-1645">만료
</span><span class="sxs-lookup"><span data-stu-id="76436-1645">expire</span></span> 
- <span data-ttu-id="76436-1646">expires
</span><span class="sxs-lookup"><span data-stu-id="76436-1646">expires</span></span> 
- <span data-ttu-id="76436-1647">expiry
</span><span class="sxs-lookup"><span data-stu-id="76436-1647">expiry</span></span> 
- <span data-ttu-id="76436-1648">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="76436-1648">fecha de expiracion</span></span> 
- <span data-ttu-id="76436-1649">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="76436-1649">fecha de venc</span></span> 
- <span data-ttu-id="76436-1650">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="76436-1650">gultig bis</span></span> 
- <span data-ttu-id="76436-1651">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="76436-1651">gultigkeitsdatum</span></span> 
- <span data-ttu-id="76436-1652">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="76436-1652">gültig bis</span></span> 
- <span data-ttu-id="76436-1653">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="76436-1653">gültigkeitsdatum</span></span> 
- <span data-ttu-id="76436-1654">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="76436-1654">la scadenza</span></span> 
- <span data-ttu-id="76436-1655">scadenza
</span><span class="sxs-lookup"><span data-stu-id="76436-1655">scadenza</span></span> 
- <span data-ttu-id="76436-1656">valable
</span><span class="sxs-lookup"><span data-stu-id="76436-1656">valable</span></span> 
- <span data-ttu-id="76436-1657">validade
</span><span class="sxs-lookup"><span data-stu-id="76436-1657">validade</span></span> 
- <span data-ttu-id="76436-1658">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="76436-1658">valido hasta</span></span> 
- <span data-ttu-id="76436-1659">valor
</span><span class="sxs-lookup"><span data-stu-id="76436-1659">valor</span></span> 
- <span data-ttu-id="76436-1660">venc
</span><span class="sxs-lookup"><span data-stu-id="76436-1660">venc</span></span> 
- <span data-ttu-id="76436-1661">vencimento
</span><span class="sxs-lookup"><span data-stu-id="76436-1661">vencimento</span></span> 
- <span data-ttu-id="76436-1662">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="76436-1662">vencimiento</span></span> 
- <span data-ttu-id="76436-1663">verloopt
</span><span class="sxs-lookup"><span data-stu-id="76436-1663">verloopt</span></span> 
- <span data-ttu-id="76436-1664">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="76436-1664">vervaldag</span></span> 
- <span data-ttu-id="76436-1665">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="76436-1665">vervaldatum</span></span> 
- <span data-ttu-id="76436-1666">vto
</span><span class="sxs-lookup"><span data-stu-id="76436-1666">vto</span></span> 
- <span data-ttu-id="76436-1667">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="76436-1667">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="76436-1668">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1668">EU Driver's License Number</span></span>

<span data-ttu-id="76436-1669">자세한 내용은 [EU 운전 면허 번호 중요 정보 유형을](eu-driver-s-license-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="76436-1669">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="76436-1670">EU 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1670">EU National Identification Number</span></span>

<span data-ttu-id="76436-1671">자세한 내용은 [EU 국가 식별 번호 중요 한 정보 유형을](eu-national-identification-number.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76436-1671">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="76436-1672">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1672">EU Passport Number</span></span>

<span data-ttu-id="76436-1673">자세한 내용은 [EU Passport 번호 중요 한 정보 유형을](eu-passport-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="76436-1673">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="76436-1674">EU 주민 등록 번호 또는 동등한 ID</span><span class="sxs-lookup"><span data-stu-id="76436-1674">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="76436-1675">자세한 내용은 [EU 주민 등록 번호 또는 동등한 ID 중요 정보 유형을](eu-social-security-number-or-equivalent-id.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="76436-1675">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="76436-1676">EU 세금 확인 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1676">EU Tax Identification Number</span></span>

<span data-ttu-id="76436-1677">자세한 내용은 [EU 세금 식별 번호 중요 한 정보 유형을](eu-tax-identification-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="76436-1677">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="76436-1678">핀란드 국가 ID</span><span class="sxs-lookup"><span data-stu-id="76436-1678">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="76436-1679">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1679">Format</span></span>

<span data-ttu-id="76436-1680">세기를 나타내는 6자리 숫자와 문자, 3자리 숫자와 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1680">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1681">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1681">Pattern</span></span>

<span data-ttu-id="76436-1682">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1682">Pattern must include all of the following:</span></span>
- <span data-ttu-id="76436-1683">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1683">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="76436-1684">세기 표시('-', '+' 또는 'a')</span><span class="sxs-lookup"><span data-stu-id="76436-1684">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="76436-1685">3자리 개인 ID 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1685">Three-digit personal identification number</span></span> 
- <span data-ttu-id="76436-1686">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-1686">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1687">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1687">Checksum</span></span>

<span data-ttu-id="76436-1688">예</span><span class="sxs-lookup"><span data-stu-id="76436-1688">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1689">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1689">Definition</span></span>

<span data-ttu-id="76436-1690">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1690">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1691">Func_finnish_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1691">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1692">Keyword_finnish_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1692">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="76436-1693">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1693">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1694">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1694">Keywords</span></span>

- <span data-ttu-id="76436-1695">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="76436-1695">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="76436-1696">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="76436-1696">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="76436-1697">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="76436-1697">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="76436-1698">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="76436-1698">Personbeteckning</span></span>
- <span data-ttu-id="76436-1699">Personnummer</span><span class="sxs-lookup"><span data-stu-id="76436-1699">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="76436-1700">핀란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1700">Finland Passport Number</span></span>

<span data-ttu-id="76436-p130">9 개의 문자 및 숫자 패턴 조합 형식 조합: 두 문자 (대/소문자 구분 안 함) 7 자리 체크섬 정의 없음 DLP 정책은이 유형의 중요 한 정보를 검색 한 것으로,이에 따라 300 문자의 근사: 정규식 Regex_finland_passport_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다. Keyword_finland_passport_number에서 키워드가 발견 되었습니다. passport Keyword_finland_passport_number <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity></span><span class="sxs-lookup"><span data-stu-id="76436-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="76436-1705">프랑스 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1705">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1706">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1706">Format</span></span>

<span data-ttu-id="76436-1707">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1707">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1708">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1708">Pattern</span></span>

<span data-ttu-id="76436-1709">비슷한 패턴(예: 프랑스 전화 번호)을 무시하기 위한 유효성 검사 기능을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1709">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1710">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1710">Checksum</span></span>

<span data-ttu-id="76436-1711">없음</span><span class="sxs-lookup"><span data-stu-id="76436-1711">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1712">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1712">Definition</span></span>

<span data-ttu-id="76436-1713">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1713">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1714">Func_french_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1714">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1715">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1715">At least one of the following is true:</span></span>
- <span data-ttu-id="76436-1716">Keyword_french_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1716">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="76436-1717">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1717">The function Func_eu_date finds a date in the right date format.</span></span>

```
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1718">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1718">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="76436-1719">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="76436-1719">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="76436-1720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="76436-1720">drivers licence</span></span>
- <span data-ttu-id="76436-1721">
drivers license</span><span class="sxs-lookup"><span data-stu-id="76436-1721">drivers license</span></span>
- <span data-ttu-id="76436-1722">driving licence
</span><span class="sxs-lookup"><span data-stu-id="76436-1722">driving licence</span></span>
- <span data-ttu-id="76436-1723">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-1723">driving license</span></span>
- <span data-ttu-id="76436-1724">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="76436-1724">permis de conduire</span></span>
- <span data-ttu-id="76436-1725">
licence number</span><span class="sxs-lookup"><span data-stu-id="76436-1725">licence number</span></span>
- <span data-ttu-id="76436-1726">
license number</span><span class="sxs-lookup"><span data-stu-id="76436-1726">license number</span></span>
- <span data-ttu-id="76436-1727">
licence numbers</span><span class="sxs-lookup"><span data-stu-id="76436-1727">licence numbers</span></span>
- <span data-ttu-id="76436-1728">

license numbers</span><span class="sxs-lookup"><span data-stu-id="76436-1728">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="76436-1729">프랑스 국가 ID 카드(CNI)</span><span class="sxs-lookup"><span data-stu-id="76436-1729">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="76436-1730">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1730">Format</span></span>

<span data-ttu-id="76436-1731">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1731">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1732">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1732">Pattern</span></span>

<span data-ttu-id="76436-1733">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1733">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1734">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1734">Checksum</span></span>

<span data-ttu-id="76436-1735">없음</span><span class="sxs-lookup"><span data-stu-id="76436-1735">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1736">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1736">Definition</span></span>

<span data-ttu-id="76436-1737">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1737">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1738">Regex_france_cni 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1738">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1739">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1739">Keywords</span></span>

<span data-ttu-id="76436-1740">없음</span><span class="sxs-lookup"><span data-stu-id="76436-1740">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="76436-1741">프랑스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1741">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1742">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1742">Format</span></span>

<span data-ttu-id="76436-1743">9자리 숫자 및 문자</span><span class="sxs-lookup"><span data-stu-id="76436-1743">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1744">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1744">Pattern</span></span>

<span data-ttu-id="76436-1745">9자리 숫자 및 문자:</span><span class="sxs-lookup"><span data-stu-id="76436-1745">Nine digits and letters:</span></span>
- <span data-ttu-id="76436-1746">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1746">Two digits</span></span> 
- <span data-ttu-id="76436-1747">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-1747">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="76436-1748">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1748">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1749">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1749">Checksum</span></span>

<span data-ttu-id="76436-1750">없음</span><span class="sxs-lookup"><span data-stu-id="76436-1750">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1751">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1751">Definition</span></span>

<span data-ttu-id="76436-1752">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1752">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1753">Func_fr_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1753">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1754">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1754">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1755">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1755">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="76436-1756">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="76436-1756">Keyword_passport</span></span>

- <span data-ttu-id="76436-1757">Passport Number</span><span class="sxs-lookup"><span data-stu-id="76436-1757">Passport Number</span></span>
- <span data-ttu-id="76436-1758">
Passport No</span><span class="sxs-lookup"><span data-stu-id="76436-1758">Passport No</span></span>
- <span data-ttu-id="76436-1759">Passport #
</span><span class="sxs-lookup"><span data-stu-id="76436-1759">Passport #</span></span>
- <span data-ttu-id="76436-1760">Passport#
</span><span class="sxs-lookup"><span data-stu-id="76436-1760">Passport#</span></span>
- <span data-ttu-id="76436-1761">PassportID</span><span class="sxs-lookup"><span data-stu-id="76436-1761">PassportID</span></span>
- <span data-ttu-id="76436-1762">Passportno
</span><span class="sxs-lookup"><span data-stu-id="76436-1762">Passportno</span></span>
- <span data-ttu-id="76436-1763">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-1763">passportnumber</span></span>
- <span data-ttu-id="76436-1764">パスポート</span><span class="sxs-lookup"><span data-stu-id="76436-1764">パスポート</span></span>
- <span data-ttu-id="76436-1765">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="76436-1765">パスポート番号</span></span>
- <span data-ttu-id="76436-1766">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="76436-1766">パスポートのNum</span></span>
- <span data-ttu-id="76436-1767">
パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="76436-1767">パスポート ＃</span></span> 
- <span data-ttu-id="76436-1768">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="76436-1768">Numéro de passeport</span></span>
- <span data-ttu-id="76436-1769">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="76436-1769">Passeport n °</span></span>
- <span data-ttu-id="76436-1770">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="76436-1770">Passeport Non</span></span>
- <span data-ttu-id="76436-1771">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="76436-1771">Passeport #</span></span>
- <span data-ttu-id="76436-1772">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="76436-1772">Passeport#</span></span>
- <span data-ttu-id="76436-1773">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="76436-1773">PasseportNon</span></span>
- <span data-ttu-id="76436-1774">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="76436-1774">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="76436-1775">프랑스 사회 보장 번호(INSEE)</span><span class="sxs-lookup"><span data-stu-id="76436-1775">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="76436-1776">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1776">Format</span></span>

<span data-ttu-id="76436-1777">15자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1777">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1778">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1778">Pattern</span></span>

<span data-ttu-id="76436-1779">다음 두 패턴 중 하나가 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1779">Must match one of two patterns:</span></span>
- <span data-ttu-id="76436-1780">13 자리 숫자와 공백 다음 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1780">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="76436-1781">또는</span><span class="sxs-lookup"><span data-stu-id="76436-1781">or</span></span>
- <span data-ttu-id="76436-1782">15자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1782">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1783">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1783">Checksum</span></span>

<span data-ttu-id="76436-1784">예</span><span class="sxs-lookup"><span data-stu-id="76436-1784">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1785">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1785">Definition</span></span>

<span data-ttu-id="76436-1786">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1786">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1787">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1787">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1788">Keyword_fr_insee의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1788">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="76436-1789">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1789">The checksum passes.</span></span>

<span data-ttu-id="76436-1790">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1790">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1791">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1791">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1792">Keyword_fr_insee의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1792">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="76436-1793">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1793">The checksum passes.</span></span>

```
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1794">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1794">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="76436-1795">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="76436-1795">Keyword_fr_insee</span></span>

- <span data-ttu-id="76436-1796">insee</span><span class="sxs-lookup"><span data-stu-id="76436-1796">insee</span></span>
- <span data-ttu-id="76436-1797">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="76436-1797">securité sociale</span></span>
- <span data-ttu-id="76436-1798">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="76436-1798">securite sociale</span></span>
- <span data-ttu-id="76436-1799">
national id</span><span class="sxs-lookup"><span data-stu-id="76436-1799">national id</span></span>
- <span data-ttu-id="76436-1800">
national identification</span><span class="sxs-lookup"><span data-stu-id="76436-1800">national identification</span></span>
- <span data-ttu-id="76436-1801">
numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="76436-1801">numéro d'identité</span></span>
- <span data-ttu-id="76436-1802">d'identité 없음</span><span class="sxs-lookup"><span data-stu-id="76436-1802">no d'identité</span></span>
- <span data-ttu-id="76436-p131">
no. d'identité</span><span class="sxs-lookup"><span data-stu-id="76436-p131">no. d'identité</span></span>
- <span data-ttu-id="76436-1805">
numero d'identite</span><span class="sxs-lookup"><span data-stu-id="76436-1805">numero d'identite</span></span>
- <span data-ttu-id="76436-1806">d'identite 없음</span><span class="sxs-lookup"><span data-stu-id="76436-1806">no d'identite</span></span>
- <span data-ttu-id="76436-p132">
no. d'identite</span><span class="sxs-lookup"><span data-stu-id="76436-p132">no. d'identite</span></span>
- <span data-ttu-id="76436-1809">social security number
</span><span class="sxs-lookup"><span data-stu-id="76436-1809">social security number</span></span>
- <span data-ttu-id="76436-1810">
social security code</span><span class="sxs-lookup"><span data-stu-id="76436-1810">social security code</span></span>
- <span data-ttu-id="76436-1811">social insurance number</span><span class="sxs-lookup"><span data-stu-id="76436-1811">social insurance number</span></span>
- <span data-ttu-id="76436-1812">
le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="76436-1812">le numéro d'identification nationale</span></span>
- <span data-ttu-id="76436-1813">
d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="76436-1813">d'identité nationale</span></span>
- <span data-ttu-id="76436-1814">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="76436-1814">numéro de sécurité sociale</span></span>
- <span data-ttu-id="76436-1815">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="76436-1815">le code de la sécurité sociale</span></span>
- <span data-ttu-id="76436-1816">
numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="76436-1816">numéro d'assurance sociale</span></span>
- <span data-ttu-id="76436-1817">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="76436-1817">numéro de sécu</span></span>
- <span data-ttu-id="76436-1818">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="76436-1818">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="76436-1819">독일 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1819">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1820">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1820">Format</span></span>

<span data-ttu-id="76436-1821">11자리 숫자와 문자 조합</span><span class="sxs-lookup"><span data-stu-id="76436-1821">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1822">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1822">Pattern</span></span>

<span data-ttu-id="76436-1823">11자리 숫자와 문자(대/소문자 구분 안 함):</span><span class="sxs-lookup"><span data-stu-id="76436-1823">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="76436-1824">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="76436-1824">A digit or letter</span></span> 
- <span data-ttu-id="76436-1825">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1825">Two digits</span></span> 
- <span data-ttu-id="76436-1826">6자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="76436-1826">Six digits or letters</span></span> 
- <span data-ttu-id="76436-1827">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1827">A digit</span></span> 
- <span data-ttu-id="76436-1828">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="76436-1828">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1829">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1829">Checksum</span></span>

<span data-ttu-id="76436-1830">예</span><span class="sxs-lookup"><span data-stu-id="76436-1830">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1831">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1831">Definition</span></span>

<span data-ttu-id="76436-1832">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1833">Func_german_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1833">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1834">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1834">At least one of the following is true:</span></span>
    - <span data-ttu-id="76436-1835">Keyword_german_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1835">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="76436-1836">Keyword_german_drivers_license_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1836">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="76436-1837">Keyword_german_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1837">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="76436-1838">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1838">The checksum passes.</span></span>

```
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1839">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1839">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="76436-1840">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="76436-1840">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="76436-1841">Führerschein</span><span class="sxs-lookup"><span data-stu-id="76436-1841">Führerschein</span></span>
- <span data-ttu-id="76436-1842">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="76436-1842">Fuhrerschein</span></span>
- <span data-ttu-id="76436-1843">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="76436-1843">Fuehrerschein</span></span>
- <span data-ttu-id="76436-1844">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="76436-1844">Führerscheinnummer</span></span>
- <span data-ttu-id="76436-1845">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="76436-1845">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="76436-1846">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="76436-1846">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="76436-1847">
Führerschein-
</span><span class="sxs-lookup"><span data-stu-id="76436-1847">Führerschein-</span></span> 
- <span data-ttu-id="76436-1848">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="76436-1848">Fuhrerschein-</span></span> 
- <span data-ttu-id="76436-1849">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="76436-1849">Fuehrerschein-</span></span> 
- <span data-ttu-id="76436-1850">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="76436-1850">FührerscheinnummerNr</span></span>
- <span data-ttu-id="76436-1851">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="76436-1851">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="76436-1852">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="76436-1852">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="76436-1853">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="76436-1853">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="76436-1854">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="76436-1854">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="76436-1855">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="76436-1855">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="76436-1856">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="76436-1856">Führerschein- Nr</span></span>
- <span data-ttu-id="76436-1857">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="76436-1857">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="76436-1858">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="76436-1858">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="76436-1859">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="76436-1859">Führerschein- Klasse</span></span> 
- <span data-ttu-id="76436-1860">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="76436-1860">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="76436-1861">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="76436-1861">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="76436-1862">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="76436-1862">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="76436-1863">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="76436-1863">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="76436-1864">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="76436-1864">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="76436-1865">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="76436-1865">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="76436-1866">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="76436-1866">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="76436-1867">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="76436-1867">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="76436-1868">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="76436-1868">Führerschein- Nr</span></span> 
- <span data-ttu-id="76436-1869">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="76436-1869">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="76436-1870">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="76436-1870">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="76436-1871">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="76436-1871">Führerschein- Klasse</span></span> 
- <span data-ttu-id="76436-1872">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="76436-1872">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="76436-1873">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="76436-1873">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="76436-1874">DL</span><span class="sxs-lookup"><span data-stu-id="76436-1874">DL</span></span> 
- <span data-ttu-id="76436-1875">DLS</span><span class="sxs-lookup"><span data-stu-id="76436-1875">DLS</span></span>
- <span data-ttu-id="76436-1876">
Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="76436-1876">Driv Lic</span></span> 
- <span data-ttu-id="76436-1877">Driv Licen
</span><span class="sxs-lookup"><span data-stu-id="76436-1877">Driv Licen</span></span> 
- <span data-ttu-id="76436-1878">Driv License</span><span class="sxs-lookup"><span data-stu-id="76436-1878">Driv License</span></span>
- <span data-ttu-id="76436-1879">
Driv Licenses
</span><span class="sxs-lookup"><span data-stu-id="76436-1879">Driv Licenses</span></span> 
- <span data-ttu-id="76436-1880">Driv Licence
</span><span class="sxs-lookup"><span data-stu-id="76436-1880">Driv Licence</span></span> 
- <span data-ttu-id="76436-1881">Driv Licences
</span><span class="sxs-lookup"><span data-stu-id="76436-1881">Driv Licences</span></span> 
- <span data-ttu-id="76436-1882">Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="76436-1882">Driv Lic</span></span> 
- <span data-ttu-id="76436-1883">Driver Licen
</span><span class="sxs-lookup"><span data-stu-id="76436-1883">Driver Licen</span></span> 
- <span data-ttu-id="76436-1884">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-1884">Driver License</span></span> 
- <span data-ttu-id="76436-1885">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-1885">Driver Licenses</span></span> 
- <span data-ttu-id="76436-1886">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="76436-1886">Driver Licence</span></span> 
- <span data-ttu-id="76436-1887">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="76436-1887">Driver Licences</span></span> 
- <span data-ttu-id="76436-1888">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="76436-1888">Drivers Lic</span></span> 
- <span data-ttu-id="76436-1889">Drivers licen</span><span class="sxs-lookup"><span data-stu-id="76436-1889">Drivers Licen</span></span> 
- <span data-ttu-id="76436-1890">Drivers License</span><span class="sxs-lookup"><span data-stu-id="76436-1890">Drivers License</span></span> 
- <span data-ttu-id="76436-1891">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-1891">Drivers Licenses</span></span> 
- <span data-ttu-id="76436-1892">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-1892">Drivers Licence</span></span> 
- <span data-ttu-id="76436-1893">라이선스 드라이버</span><span class="sxs-lookup"><span data-stu-id="76436-1893">Drivers Licences</span></span> 
- <span data-ttu-id="76436-1894">드라이버의 Lic</span><span class="sxs-lookup"><span data-stu-id="76436-1894">Driver's Lic</span></span> 
- <span data-ttu-id="76436-1895">Driver's Licen
</span><span class="sxs-lookup"><span data-stu-id="76436-1895">Driver's Licen</span></span> 
- <span data-ttu-id="76436-1896">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-1896">Driver's License</span></span> 
- <span data-ttu-id="76436-1897">운전 면허증</span><span class="sxs-lookup"><span data-stu-id="76436-1897">Driver's Licenses</span></span> 
- <span data-ttu-id="76436-1898">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="76436-1898">Driver's Licence</span></span> 
- <span data-ttu-id="76436-1899">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="76436-1899">Driver's Licences</span></span> 
- <span data-ttu-id="76436-1900">Driving Lic
</span><span class="sxs-lookup"><span data-stu-id="76436-1900">Driving Lic</span></span> 
- <span data-ttu-id="76436-1901">Driving Licen
</span><span class="sxs-lookup"><span data-stu-id="76436-1901">Driving Licen</span></span> 
- <span data-ttu-id="76436-1902">Driving License
</span><span class="sxs-lookup"><span data-stu-id="76436-1902">Driving License</span></span> 
- <span data-ttu-id="76436-1903">Driving Licenses
</span><span class="sxs-lookup"><span data-stu-id="76436-1903">Driving Licenses</span></span> 
- <span data-ttu-id="76436-1904">Driving Licence

</span><span class="sxs-lookup"><span data-stu-id="76436-1904">Driving Licence</span></span> 
- <span data-ttu-id="76436-1905">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="76436-1905">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="76436-1906">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="76436-1906">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="76436-1907">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1907">Nr-Führerschein</span></span> 
- <span data-ttu-id="76436-1908">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1908">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="76436-1909">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1909">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="76436-1910">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1910">No-Führerschein</span></span> 
- <span data-ttu-id="76436-1911">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1911">No-Fuhrerschein</span></span> 
- <span data-ttu-id="76436-1912">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1912">No-Fuehrerschein</span></span> 
- <span data-ttu-id="76436-1913">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1913">N-Führerschein</span></span> 
- <span data-ttu-id="76436-1914">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1914">N-Fuhrerschein</span></span> 
- <span data-ttu-id="76436-1915">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="76436-1915">N-Fuehrerschein</span></span>
- <span data-ttu-id="76436-1916">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1916">Nr-Führerschein</span></span> 
- <span data-ttu-id="76436-1917">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1917">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="76436-1918">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1918">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="76436-1919">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1919">No-Führerschein</span></span> 
- <span data-ttu-id="76436-1920">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1920">No-Fuhrerschein</span></span> 
- <span data-ttu-id="76436-1921">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1921">No-Fuehrerschein</span></span> 
- <span data-ttu-id="76436-1922">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1922">N-Führerschein</span></span> 
- <span data-ttu-id="76436-1923">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="76436-1923">N-Fuhrerschein</span></span> 
- <span data-ttu-id="76436-1924">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="76436-1924">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="76436-1925">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="76436-1925">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="76436-1926">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="76436-1926">ausstellungsdatum</span></span>
- <span data-ttu-id="76436-1927">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="76436-1927">ausstellungsort</span></span>
- <span data-ttu-id="76436-1928">
ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="76436-1928">ausstellende behöde</span></span>
- <span data-ttu-id="76436-1929">
ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="76436-1929">ausstellende behorde</span></span>
- <span data-ttu-id="76436-1930">

ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="76436-1930">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="76436-1931">독일 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1931">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1932">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1932">Format</span></span>

<span data-ttu-id="76436-1933">10자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="76436-1933">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1934">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1934">Pattern</span></span>

<span data-ttu-id="76436-1935">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1935">Pattern must include all of the following:</span></span>
- <span data-ttu-id="76436-1936">첫 번째 문자는 숫자 또는 (C, F, G, H, J, K) 집합의 문자임</span><span class="sxs-lookup"><span data-stu-id="76436-1936">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="76436-1937">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1937">Three digits</span></span> 
- <span data-ttu-id="76436-1938">5자리 숫자 또는 (C, -H, J-N, P, R, T, V-Z) 집합의 문자</span><span class="sxs-lookup"><span data-stu-id="76436-1938">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="76436-1939">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1939">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1940">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1940">Checksum</span></span>

<span data-ttu-id="76436-1941">예</span><span class="sxs-lookup"><span data-stu-id="76436-1941">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1942">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1942">Definition</span></span>

<span data-ttu-id="76436-1943">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1943">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1944">Func_german_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1944">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1945">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1945">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="76436-1946">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1946">The checksum passes.</span></span>

<span data-ttu-id="76436-1947">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1947">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1948">Func_german_passport_data 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1948">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1949">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1949">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="76436-1950">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1950">The checksum passes.</span></span>

```
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1951">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1951">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="76436-1952">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="76436-1952">Keyword_german_passport</span></span>

- <span data-ttu-id="76436-1953">reisepass</span><span class="sxs-lookup"><span data-stu-id="76436-1953">reisepass</span></span>
- <span data-ttu-id="76436-1954">
reisepasse</span><span class="sxs-lookup"><span data-stu-id="76436-1954">reisepasse</span></span>
- <span data-ttu-id="76436-1955">
reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="76436-1955">reisepassnummer</span></span>
- <span data-ttu-id="76436-1956">passport</span><span class="sxs-lookup"><span data-stu-id="76436-1956">passport</span></span>
- <span data-ttu-id="76436-1957">

passports</span><span class="sxs-lookup"><span data-stu-id="76436-1957">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="76436-1958">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="76436-1958">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="76436-1959">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="76436-1959">geburtsdatum</span></span>
- <span data-ttu-id="76436-1960">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="76436-1960">ausstellungsdatum</span></span>
- <span data-ttu-id="76436-1961">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="76436-1961">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="76436-1962">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="76436-1962">Keyword_german_passport_number</span></span>

<span data-ttu-id="76436-1963">Reisepass veiligheid-Reisepass</span><span class="sxs-lookup"><span data-stu-id="76436-1963">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="76436-1964">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="76436-1964">Keyword_german_passport1</span></span>

<span data-ttu-id="76436-1965">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="76436-1965">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="76436-1966">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="76436-1966">Keyword_german_passport2</span></span>

<span data-ttu-id="76436-1967">bnationalit</span><span class="sxs-lookup"><span data-stu-id="76436-1967">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="76436-1968">독일 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-1968">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-1969">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1969">Format</span></span>

<span data-ttu-id="76436-1970">2010 년 11 월 1 일 이후: 9 개 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1970">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="76436-1971">1 월 1987 년 10 월 31 일 (2010:10 자리 숫자)</span><span class="sxs-lookup"><span data-stu-id="76436-1971">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1972">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1972">Pattern</span></span>

<span data-ttu-id="76436-1973">2010년 11월 1일 이후:</span><span class="sxs-lookup"><span data-stu-id="76436-1973">Since 1 November 2010:</span></span>
- <span data-ttu-id="76436-1974">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-1974">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="76436-1975">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1975">Eight digits</span></span>

<span data-ttu-id="76436-1976">1 년 4 월 1987 일 ~ 10 월 31 일까 지:</span><span class="sxs-lookup"><span data-stu-id="76436-1976">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="76436-1977">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-1977">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-1978">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-1978">Checksum</span></span>

<span data-ttu-id="76436-1979">없음</span><span class="sxs-lookup"><span data-stu-id="76436-1979">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-1980">정의</span><span class="sxs-lookup"><span data-stu-id="76436-1980">Definition</span></span>

<span data-ttu-id="76436-1981">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1981">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-1982">정규식 Regex_germany_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1982">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-1983">Keyword_germany_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-1983">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-1984">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-1984">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="76436-1985">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="76436-1985">Keyword_germany_id_card</span></span>

- <span data-ttu-id="76436-1986">Identity Card</span><span class="sxs-lookup"><span data-stu-id="76436-1986">Identity Card</span></span>
- <span data-ttu-id="76436-1987">ID</span><span class="sxs-lookup"><span data-stu-id="76436-1987">ID</span></span>
- <span data-ttu-id="76436-1988">Identification</span><span class="sxs-lookup"><span data-stu-id="76436-1988">Identification</span></span>
- <span data-ttu-id="76436-1989">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="76436-1989">Personalausweis</span></span>
- <span data-ttu-id="76436-1990">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="76436-1990">Identifizierungsnummer</span></span>
- <span data-ttu-id="76436-1991">Ausweis</span><span class="sxs-lookup"><span data-stu-id="76436-1991">Ausweis</span></span>
- <span data-ttu-id="76436-1992">Identifikation</span><span class="sxs-lookup"><span data-stu-id="76436-1992">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="76436-1993">그리스 국가 ID 카드</span><span class="sxs-lookup"><span data-stu-id="76436-1993">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="76436-1994">형식</span><span class="sxs-lookup"><span data-stu-id="76436-1994">Format</span></span>

<span data-ttu-id="76436-1995">7-8자리 문자 및 숫자와 대시의 조합</span><span class="sxs-lookup"><span data-stu-id="76436-1995">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-1996">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-1996">Pattern</span></span>

<span data-ttu-id="76436-1997">7자리 문자 및 숫자(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="76436-1997">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="76436-1998">1개 문자(그리스어 알파벳의 임의 문자) </span><span class="sxs-lookup"><span data-stu-id="76436-1998">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="76436-1999">대시 1개</span><span class="sxs-lookup"><span data-stu-id="76436-1999">A dash</span></span> 
- <span data-ttu-id="76436-2000">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2000">Six digits</span></span>

<span data-ttu-id="76436-2001">8자리 문자와 숫자(새로운 형식):</span><span class="sxs-lookup"><span data-stu-id="76436-2001">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="76436-2002">그리스어 및 라틴어 알파벳 둘 다에 해당 대문자가 포함된 2개 문자(ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="76436-2002">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="76436-2003">대시 1개</span><span class="sxs-lookup"><span data-stu-id="76436-2003">A dash</span></span> 
- <span data-ttu-id="76436-2004">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2004">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2005">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2005">Checksum</span></span>

<span data-ttu-id="76436-2006">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2006">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2007">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2007">Definition</span></span>

<span data-ttu-id="76436-2008">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2008">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2009">정규식 Regex_greece_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2009">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2010">Keyword_greece_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2010">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2011">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2011">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="76436-2012">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="76436-2012">Keyword_greece_id_card</span></span>

- <span data-ttu-id="76436-2013">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="76436-2013">Greek identity Card</span></span>
- <span data-ttu-id="76436-2014">Tautotita</span><span class="sxs-lookup"><span data-stu-id="76436-2014">Tautotita</span></span>
- <span data-ttu-id="76436-2015">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="76436-2015">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="76436-2016">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="76436-2016">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="76436-2017">HKID(홍콩 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2017">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2018">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2018">Format</span></span>

<span data-ttu-id="76436-2019">8-9자리 문자 및 숫자와 마지막 문자를 선택적 괄호로 묶어서 조합</span><span class="sxs-lookup"><span data-stu-id="76436-2019">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2020">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2020">Pattern</span></span>

<span data-ttu-id="76436-2021">8-9자리 문자 조합:</span><span class="sxs-lookup"><span data-stu-id="76436-2021">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="76436-2022">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2022">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="76436-2023">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2023">Six digits</span></span> 
- <span data-ttu-id="76436-2024">검사 숫자에 해당하고 선택적으로 괄호로 묶는 마지막 문자(임의 숫자 또는 문자 A)</span><span class="sxs-lookup"><span data-stu-id="76436-2024">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2025">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2025">Checksum</span></span>

<span data-ttu-id="76436-2026">예</span><span class="sxs-lookup"><span data-stu-id="76436-2026">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2027">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2027">Definition</span></span>

<span data-ttu-id="76436-2028">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2028">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2029">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2029">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2030">Keyword_hong_kong_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2030">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="76436-2031">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2031">The checksum passes.</span></span>

<span data-ttu-id="76436-2032">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2032">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2033">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2033">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2034">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2034">The checksum passes.</span></span>

```
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2035">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2035">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="76436-2036">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="76436-2036">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="76436-2037">홍콩 특별 식별자 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2037">hong kong identity card</span></span>
- <span data-ttu-id="76436-2038">HKIDC</span><span class="sxs-lookup"><span data-stu-id="76436-2038">HKIDC</span></span>
- <span data-ttu-id="76436-2039">id 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2039">id card</span></span>
- <span data-ttu-id="76436-2040">identity card</span><span class="sxs-lookup"><span data-stu-id="76436-2040">identity card</span></span>
- <span data-ttu-id="76436-2041">zh-hk id 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2041">hk identity card</span></span>
- <span data-ttu-id="76436-2042">홍콩 id</span><span class="sxs-lookup"><span data-stu-id="76436-2042">hong kong id</span></span>
- <span data-ttu-id="76436-2043">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="76436-2043">香港身份證</span></span>
- <span data-ttu-id="76436-2044">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="76436-2044">香港永久性居民身份證</span></span>
- <span data-ttu-id="76436-2045">身份證
</span><span class="sxs-lookup"><span data-stu-id="76436-2045">身份證</span></span>
- <span data-ttu-id="76436-2046">身份証</span><span class="sxs-lookup"><span data-stu-id="76436-2046">身份証</span></span>
- <span data-ttu-id="76436-2047">身分證 </span><span class="sxs-lookup"><span data-stu-id="76436-2047">身分證</span></span>
- <span data-ttu-id="76436-2048">身分証</span><span class="sxs-lookup"><span data-stu-id="76436-2048">身分証</span></span>
- <span data-ttu-id="76436-2049">香港身份証</span><span class="sxs-lookup"><span data-stu-id="76436-2049">香港身份証</span></span>
- <span data-ttu-id="76436-2050">香港身分證</span><span class="sxs-lookup"><span data-stu-id="76436-2050">香港身分證</span></span>
- <span data-ttu-id="76436-2051">香港身分証</span><span class="sxs-lookup"><span data-stu-id="76436-2051">香港身分証</span></span>
- <span data-ttu-id="76436-2052">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="76436-2052">香港身份證</span></span>
- <span data-ttu-id="76436-2053">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="76436-2053">香港居民身份證</span></span>
- <span data-ttu-id="76436-2054">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="76436-2054">香港居民身份証</span></span>
- <span data-ttu-id="76436-2055">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="76436-2055">香港居民身分證</span></span>
- <span data-ttu-id="76436-2056">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="76436-2056">香港居民身分証</span></span>
- <span data-ttu-id="76436-2057">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="76436-2057">香港永久性居民身份証</span></span>
- <span data-ttu-id="76436-2058">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="76436-2058">香港永久性居民身分證</span></span>
- <span data-ttu-id="76436-2059">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="76436-2059">香港永久性居民身分証</span></span>
- <span data-ttu-id="76436-2060">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="76436-2060">香港永久性居民身份證</span></span>
- <span data-ttu-id="76436-2061">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="76436-2061">香港非永久性居民身份證</span></span>
- <span data-ttu-id="76436-2062">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="76436-2062">香港非永久性居民身份証</span></span>
- <span data-ttu-id="76436-2063">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="76436-2063">香港非永久性居民身分證</span></span>
- <span data-ttu-id="76436-2064">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="76436-2064">香港非永久性居民身分証</span></span>
- <span data-ttu-id="76436-2065">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="76436-2065">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="76436-2066">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="76436-2066">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="76436-2067">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="76436-2067">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="76436-2068">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="76436-2068">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="76436-2069">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="76436-2069">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="76436-2070">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="76436-2070">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="76436-2071">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="76436-2071">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="76436-2072">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="76436-2072">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="76436-2073">인도 PAN(영구 계정 번호)</span><span class="sxs-lookup"><span data-stu-id="76436-2073">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="76436-2074">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2074">Format</span></span>

<span data-ttu-id="76436-2075">10자리 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2075">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2076">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2076">Pattern</span></span>

<span data-ttu-id="76436-2077">10자리 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2077">10 letters or digits:</span></span>
- <span data-ttu-id="76436-2078">5개 문자(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="76436-2078">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="76436-2079">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2079">Four digits</span></span> 
- <span data-ttu-id="76436-2080">알파벳 검사 숫자에 해당하는 문자 1개</span><span class="sxs-lookup"><span data-stu-id="76436-2080">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2081">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2081">Checksum</span></span>

<span data-ttu-id="76436-2082">예</span><span class="sxs-lookup"><span data-stu-id="76436-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2083">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2083">Definition</span></span>

<span data-ttu-id="76436-2084">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2084">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2085">정규식 Regex_india_permanent_account_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2085">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2086">Keyword_india_permanent_account_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2086">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="76436-2087">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2087">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2088">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2088">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="76436-2089">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="76436-2089">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="76436-2090">Permanent Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2090">Permanent Account Number</span></span> 
- <span data-ttu-id="76436-2091">PAN
</span><span class="sxs-lookup"><span data-stu-id="76436-2091">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="76436-2092">인도 고유 ID(Aadhaar) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2092">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2093">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2093">Format</span></span>

<span data-ttu-id="76436-2094">선택적 공백 또는 대시를 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2094">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2095">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2095">Pattern</span></span>

<span data-ttu-id="76436-2096">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2096">12 digits:</span></span>
- <span data-ttu-id="76436-2097">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2097">Four digits</span></span> 
- <span data-ttu-id="76436-2098">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="76436-2098">An optional space or dash</span></span> 
- <span data-ttu-id="76436-2099">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2099">Four digits</span></span> 
- <span data-ttu-id="76436-2100">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="76436-2100">An optional space or dash</span></span> 
- <span data-ttu-id="76436-2101">검사 숫자에 해당하는 마지막 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2101">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2102">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2102">Checksum</span></span>

<span data-ttu-id="76436-2103">예</span><span class="sxs-lookup"><span data-stu-id="76436-2103">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2104">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2104">Definition</span></span>

<span data-ttu-id="76436-p133">DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다. Keyword_india_aadhar에서 키워드가 발견 되었습니다. 체크섬이 통과 됩니다. DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다. 체크섬이 통과 됩니다. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="76436-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="76436-2111">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2111">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="76436-2112">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="76436-2112">Keyword_india_aadhar</span></span>
- <span data-ttu-id="76436-2113">Aadhar</span><span class="sxs-lookup"><span data-stu-id="76436-2113">Aadhar</span></span>
- <span data-ttu-id="76436-2114">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="76436-2114">Aadhaar</span></span>
- <span data-ttu-id="76436-2115">UID</span><span class="sxs-lookup"><span data-stu-id="76436-2115">UID</span></span>
- <span data-ttu-id="76436-2116">आधार</span><span class="sxs-lookup"><span data-stu-id="76436-2116">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="76436-2117">인도네시아 ID 카드(KTP) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2117">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2118">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2118">Format</span></span>

<span data-ttu-id="76436-2119">선택적으로 마침표를 포함하는 16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2119">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2120">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2120">Pattern</span></span>

<span data-ttu-id="76436-2121">16자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2121">16 digits:</span></span>
- <span data-ttu-id="76436-2122">2자리 시/도 코드 </span><span class="sxs-lookup"><span data-stu-id="76436-2122">Two-digit province code</span></span> 
- <span data-ttu-id="76436-2123">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="76436-2123">A period (optional)</span></span> 
- <span data-ttu-id="76436-2124">2자리 지역 또는 구/군/시 코드 </span><span class="sxs-lookup"><span data-stu-id="76436-2124">Two-digit regency or city code</span></span> 
- <span data-ttu-id="76436-2125">2자리 소구역 코드 </span><span class="sxs-lookup"><span data-stu-id="76436-2125">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="76436-2126">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="76436-2126">A period (optional)</span></span> 
- <span data-ttu-id="76436-2127">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-2127">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="76436-2128">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="76436-2128">A period (optional)</span></span> 
- <span data-ttu-id="76436-2129">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2129">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2130">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2130">Checksum</span></span>

<span data-ttu-id="76436-2131">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2131">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2132">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2132">Definition</span></span>

<span data-ttu-id="76436-2133">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2133">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2134">정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2134">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2135">Keyword_indonesia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2135">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="76436-2136">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2137">정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2137">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

```
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2138">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2138">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="76436-2139">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="76436-2139">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="76436-2140">KTP</span><span class="sxs-lookup"><span data-stu-id="76436-2140">KTP</span></span>
- <span data-ttu-id="76436-2141">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="76436-2141">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="76436-2142">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="76436-2142">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="76436-2143">IBAN(국제 은행 계좌 번호)</span><span class="sxs-lookup"><span data-stu-id="76436-2143">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="76436-2144">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2144">Format</span></span>

<span data-ttu-id="76436-2145">국가 코드 (두 문자) + 검사 숫자 (2 자리 숫자)와 bban 숫자 (최대 30 자)</span><span class="sxs-lookup"><span data-stu-id="76436-2145">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2146">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2146">Pattern</span></span>

<span data-ttu-id="76436-2147">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2147">Pattern must include all of the following:</span></span>

- <span data-ttu-id="76436-2148">두 글자로 된 국가 코드</span><span class="sxs-lookup"><span data-stu-id="76436-2148">Two-letter country code</span></span>
- <span data-ttu-id="76436-2149">두 개의 검사 숫자 (선택적 공백)</span><span class="sxs-lookup"><span data-stu-id="76436-2149">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="76436-2150">1-7 개 문자 또는 숫자의 그룹 (공백으로 구분 가능)</span><span class="sxs-lookup"><span data-stu-id="76436-2150">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="76436-2151">1-3 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2151">1-3 letters or digits</span></span>

<span data-ttu-id="76436-p134">각 국가의 형식은 약간 다릅니다. iban 중요 한 정보 유형은 다음과 같은 60 국가를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="76436-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, kw, hu,, to,,, fr,,, i,,, ie, il, is,, l,, 5, 60, md, me, mk, e, mt, mu , nl-nl, no, pl, pt, ro, rs, sa, se, si,, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="76436-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2155">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2155">Checksum</span></span>

<span data-ttu-id="76436-2156">예</span><span class="sxs-lookup"><span data-stu-id="76436-2156">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2157">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2157">Definition</span></span>

<span data-ttu-id="76436-2158">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2158">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2159">Func_iban 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2159">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2160">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2160">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2161">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2161">Keywords</span></span>

<span data-ttu-id="76436-2162">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2162">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="76436-2163">IP 주소</span><span class="sxs-lookup"><span data-stu-id="76436-2163">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="76436-2164">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2164">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="76436-2165">IPv4:</span><span class="sxs-lookup"><span data-stu-id="76436-2165">IPv4:</span></span>
<span data-ttu-id="76436-2166">IPv4 주소의 서식 있는 버전(마침표 있음) 및 서식 없는 버전(마침표 없음)으로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2166">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="76436-2167">IPv6:</span><span class="sxs-lookup"><span data-stu-id="76436-2167">IPv6:</span></span>
<span data-ttu-id="76436-2168">서식 있는(콜론 포함) IPv6 번호로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2168">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2169">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2169">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2170">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2170">Checksum</span></span>

<span data-ttu-id="76436-2171">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2172">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2172">Definition</span></span>

<span data-ttu-id="76436-2173">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2173">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2174">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2174">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2175">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2175">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="76436-2176">IPv4의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2176">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2177">Regex_ipv4_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2177">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2178">Keyword_ipaddress의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2178">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="76436-2179">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2179">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2180">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2180">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2181">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2181">No keyword from Keyword_ipaddress is found.</span></span>

```
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2182">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2182">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="76436-2183">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="76436-2183">Keyword_ipaddress</span></span>

- <span data-ttu-id="76436-2184">IP(이 키워드는 대/소문자를 구분함)</span><span class="sxs-lookup"><span data-stu-id="76436-2184">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="76436-2185">ip address
</span><span class="sxs-lookup"><span data-stu-id="76436-2185">ip address</span></span> 
- <span data-ttu-id="76436-2186">ip addresses</span><span class="sxs-lookup"><span data-stu-id="76436-2186">ip addresses</span></span>
- <span data-ttu-id="76436-2187">internet protocol</span><span class="sxs-lookup"><span data-stu-id="76436-2187">internet protocol</span></span>
- <span data-ttu-id="76436-2188">
IP-כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="76436-2188">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="76436-2189">Diseases의 국제 분류 (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="76436-2189">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="76436-2190">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2190">Format</span></span>

<span data-ttu-id="76436-2191">사전</span><span class="sxs-lookup"><span data-stu-id="76436-2191">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2192">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2192">Pattern</span></span>

<span data-ttu-id="76436-2193">Keyword</span><span class="sxs-lookup"><span data-stu-id="76436-2193">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2194">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2194">Checksum</span></span>

<span data-ttu-id="76436-2195">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2195">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2196">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2196">Definition</span></span>

<span data-ttu-id="76436-2197">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2197">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2198">Dictionary_icd_10_cm에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2198">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="76436-2199">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2199">Keywords</span></span>

<span data-ttu-id="76436-p135">Dictionary_icd_10_cm 키워드 사전의 모든 용어 이며, [Diseases의 국제 분류, 10 번째 수정, 임상 수정 (icd-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604)을 기반으로 합니다. 이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="76436-2202">Diseases의 국제 분류 (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="76436-2202">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="76436-2203">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2203">Format</span></span>

<span data-ttu-id="76436-2204">사전</span><span class="sxs-lookup"><span data-stu-id="76436-2204">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2205">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2205">Pattern</span></span>

<span data-ttu-id="76436-2206">Keyword</span><span class="sxs-lookup"><span data-stu-id="76436-2206">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2207">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2207">Checksum</span></span>

<span data-ttu-id="76436-2208">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2208">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2209">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2209">Definition</span></span>

<span data-ttu-id="76436-2210">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2210">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2211">Dictionary_icd_9_cm에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2211">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2212">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2212">Keywords</span></span>

<span data-ttu-id="76436-p136">[Diseases의 국가별 분류, 9 번째 버전의 임상 수정 (icd-9cm)](https://go.microsoft.com/fwlink/?linkid=852605)을 기반으로 하는 Dictionary_icd_9_cm 키워드 사전의 모든 용어입니다. 이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="76436-2215">아일랜드 PPS(개인 공공 서비스) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2215">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2216">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2216">Format</span></span>

<span data-ttu-id="76436-2217">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="76436-2217">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="76436-2218">7자리 숫자와 1-2개 문자 </span><span class="sxs-lookup"><span data-stu-id="76436-2218">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="76436-2219">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="76436-2219">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="76436-2220">7자리 숫자와 2개 문자</span><span class="sxs-lookup"><span data-stu-id="76436-2220">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2221">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2221">Pattern</span></span>

<span data-ttu-id="76436-2222">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="76436-2222">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="76436-2223">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2223">Seven digits</span></span> 
- <span data-ttu-id="76436-2224">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2224">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="76436-2225">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="76436-2225">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="76436-2226">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2226">Seven digits</span></span> 
- <span data-ttu-id="76436-2227">알파벳 검사 숫자에 해당하는 문자 1개(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="76436-2227">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="76436-2228">문자 "A" 또는 "H"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2228">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2229">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2229">Checksum</span></span>

<span data-ttu-id="76436-2230">예</span><span class="sxs-lookup"><span data-stu-id="76436-2230">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2231">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2231">Definition</span></span>

<span data-ttu-id="76436-2232">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2232">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2233">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2233">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2234">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2234">One of the following is true:</span></span>
    - <span data-ttu-id="76436-2235">Keyword_ireland_pps에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2235">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="76436-2236">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2236">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="76436-2237">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2237">The checksum passes.</span></span>

<span data-ttu-id="76436-2238">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2238">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2239">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2239">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2240">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2240">The checksum passes.</span></span>

```
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2241">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2241">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="76436-2242">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="76436-2242">Keyword_ireland_pps</span></span>

- <span data-ttu-id="76436-2243">Personal Public Service Number 
</span><span class="sxs-lookup"><span data-stu-id="76436-2243">Personal Public Service Number</span></span> 
- <span data-ttu-id="76436-2244">PPS Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2244">PPS Number</span></span> 
- <span data-ttu-id="76436-2245">PPS Num
</span><span class="sxs-lookup"><span data-stu-id="76436-2245">PPS Num</span></span> 
- <span data-ttu-id="76436-2246">PPS No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2246">PPS No.</span></span> 
- <span data-ttu-id="76436-2247">PPS #
</span><span class="sxs-lookup"><span data-stu-id="76436-2247">PPS #</span></span> 
- <span data-ttu-id="76436-2248">PPS#
</span><span class="sxs-lookup"><span data-stu-id="76436-2248">PPS#</span></span> 
- <span data-ttu-id="76436-2249">PPSN
</span><span class="sxs-lookup"><span data-stu-id="76436-2249">PPSN</span></span> 
- <span data-ttu-id="76436-2250">Public Services Card
</span><span class="sxs-lookup"><span data-stu-id="76436-2250">Public Services Card</span></span> 
- <span data-ttu-id="76436-2251">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="76436-2251">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="76436-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="76436-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="76436-2254">PSP
</span><span class="sxs-lookup"><span data-stu-id="76436-2254">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="76436-2255">이스라엘 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2255">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2256">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2256">Format</span></span>

<span data-ttu-id="76436-2257">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2257">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2258">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2258">Pattern</span></span>

<span data-ttu-id="76436-2259">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="76436-2259">Formatted:</span></span>
- <span data-ttu-id="76436-2260">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2260">Two digits</span></span> 
- <span data-ttu-id="76436-2261">대시 1개</span><span class="sxs-lookup"><span data-stu-id="76436-2261">A dash</span></span> 
- <span data-ttu-id="76436-2262">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2262">Three digits</span></span> 
- <span data-ttu-id="76436-2263">대시 1개</span><span class="sxs-lookup"><span data-stu-id="76436-2263">A dash</span></span> 
- <span data-ttu-id="76436-2264">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2264">Eight digits</span></span>

<span data-ttu-id="76436-2265">서식 없음:</span><span class="sxs-lookup"><span data-stu-id="76436-2265">Unformatted:</span></span>
- <span data-ttu-id="76436-2266">13자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2266">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2267">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2267">Checksum</span></span>

<span data-ttu-id="76436-2268">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2269">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2269">Definition</span></span>

<span data-ttu-id="76436-2270">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2271">Regex_israel_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2271">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2272">Keyword_israel_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2272">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2273">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2273">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="76436-2274">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="76436-2274">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="76436-2275">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2275">Bank Account Number</span></span> 
- <span data-ttu-id="76436-2276">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="76436-2276">Bank Account</span></span> 
- <span data-ttu-id="76436-2277">Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2277">Account Number</span></span> 
- <span data-ttu-id="76436-2278">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="76436-2278">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="76436-2279">이스라엘 국가 ID</span><span class="sxs-lookup"><span data-stu-id="76436-2279">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="76436-2280">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2280">Format</span></span>

<span data-ttu-id="76436-2281">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2281">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2282">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2282">Pattern</span></span>

<span data-ttu-id="76436-2283">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2283">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2284">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2284">Checksum</span></span>

<span data-ttu-id="76436-2285">예</span><span class="sxs-lookup"><span data-stu-id="76436-2285">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2286">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2286">Definition</span></span>

<span data-ttu-id="76436-2287">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2288">Func_israeli_national_id_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2288">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2289">Keyword_Israel_National_ID의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2289">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="76436-2290">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2290">The checksum passes.</span></span>

```
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2291">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2291">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="76436-2292">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="76436-2292">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="76436-2293">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="76436-2293">מספר זהות</span></span> 
- <span data-ttu-id="76436-2294">National ID Number</span><span class="sxs-lookup"><span data-stu-id="76436-2294">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="76436-2295">이탈리아 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2295">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2296">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2296">Format</span></span>

<span data-ttu-id="76436-2297">10개의 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="76436-2297">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2298">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2298">Pattern</span></span>

- <span data-ttu-id="76436-2299">10개의 문자 및 숫자 조합:</span><span class="sxs-lookup"><span data-stu-id="76436-2299">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="76436-2300">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2300">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="76436-2301">문자 "A" 또는 "V"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2301">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="76436-2302">7개 문자(대/소문자 구분 안 함), 숫자 또는 밑줄 문자</span><span class="sxs-lookup"><span data-stu-id="76436-2302">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="76436-2303">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2303">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2304">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2304">Checksum</span></span>

<span data-ttu-id="76436-2305">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2305">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2306">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2306">Definition</span></span>

<span data-ttu-id="76436-2307">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2308">Regex_italy_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2308">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2309">Keyword_italy_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2309">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2310">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2310">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="76436-2311">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="76436-2311">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="76436-2312">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="76436-2312">numero di patente di guida</span></span> 
- <span data-ttu-id="76436-2313">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="76436-2313">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="76436-2314">일본 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2314">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2315">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2315">Format</span></span>

<span data-ttu-id="76436-2316">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2316">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2317">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2317">Pattern</span></span>

<span data-ttu-id="76436-2318">은행 계좌 번호:</span><span class="sxs-lookup"><span data-stu-id="76436-2318">Bank account number:</span></span>
- <span data-ttu-id="76436-2319">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2319">Seven or eight digits</span></span>
- <span data-ttu-id="76436-2320">은행 계좌 지점 코드:</span><span class="sxs-lookup"><span data-stu-id="76436-2320">Bank account branch code:</span></span>
- <span data-ttu-id="76436-2321">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2321">Four digits</span></span> 
- <span data-ttu-id="76436-2322">공백 또는 대시(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="76436-2322">A space or dash (optional)</span></span> 
- <span data-ttu-id="76436-2323">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2323">Three digits</span></span>

<span data-ttu-id="76436-2324">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2324">Checksum</span></span>

<span data-ttu-id="76436-2325">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2325">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2326">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2326">Definition</span></span>

<span data-ttu-id="76436-2327">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2327">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2328">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2328">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2329">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2329">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="76436-2330">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2330">One of the following is true:</span></span>
- <span data-ttu-id="76436-2331">Func_jp_bank_account_branch_code 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2331">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2332">Keyword_jp_bank_branch_code의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2332">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="76436-2333">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2333">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2334">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2334">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2335">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2335">A keyword from Keyword_jp_bank_account is found.</span></span>

```
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2336">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2336">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="76436-2337">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="76436-2337">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="76436-2338">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2338">Checking Account Number</span></span> 
- <span data-ttu-id="76436-2339">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="76436-2339">Checking Account</span></span> 
- <span data-ttu-id="76436-2340">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="76436-2340">Checking Account #</span></span> 
- <span data-ttu-id="76436-2341">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2341">Checking Acct Number</span></span> 
- <span data-ttu-id="76436-2342">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="76436-2342">Checking Acct #</span></span> 
- <span data-ttu-id="76436-2343">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2343">Checking Acct No.</span></span> 
- <span data-ttu-id="76436-2344">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2344">Checking Account No.</span></span> 
- <span data-ttu-id="76436-2345">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2345">Bank Account Number</span></span> 
- <span data-ttu-id="76436-2346">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="76436-2346">Bank Account</span></span> 
- <span data-ttu-id="76436-2347">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="76436-2347">Bank Account #</span></span> 
- <span data-ttu-id="76436-2348">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2348">Bank Acct Number</span></span> 
- <span data-ttu-id="76436-2349">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="76436-2349">Bank Acct #</span></span> 
- <span data-ttu-id="76436-2350">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2350">Bank Acct No.</span></span> 
- <span data-ttu-id="76436-2351">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2351">Bank Account No.</span></span> 
- <span data-ttu-id="76436-2352">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2352">Savings Account Number</span></span> 
- <span data-ttu-id="76436-2353">저축 계정</span><span class="sxs-lookup"><span data-stu-id="76436-2353">Savings Account</span></span> 
- <span data-ttu-id="76436-2354">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="76436-2354">Savings Account #</span></span> 
- <span data-ttu-id="76436-2355">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2355">Savings Acct Number</span></span> 
- <span data-ttu-id="76436-2356">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="76436-2356">Savings Acct #</span></span> 
- <span data-ttu-id="76436-2357">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2357">Savings Acct No.</span></span> 
- <span data-ttu-id="76436-2358">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2358">Savings Account No.</span></span> 
- <span data-ttu-id="76436-2359">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2359">Debit Account Number</span></span> 
- <span data-ttu-id="76436-2360">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="76436-2360">Debit Account</span></span> 
- <span data-ttu-id="76436-2361">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="76436-2361">Debit Account #</span></span> 
- <span data-ttu-id="76436-2362">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2362">Debit Acct Number</span></span> 
- <span data-ttu-id="76436-2363">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="76436-2363">Debit Acct #</span></span> 
- <span data-ttu-id="76436-2364">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2364">Debit Acct No.</span></span> 
- <span data-ttu-id="76436-2365">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2365">Debit Account No.</span></span> 
- <span data-ttu-id="76436-2366">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="76436-2366">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="76436-2367"># アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="76436-2367">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="76436-2368">#勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="76436-2368">＃勘定の確認</span></span> 
- <span data-ttu-id="76436-2369">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="76436-2369">勘定番号の確認</span></span> 
- <span data-ttu-id="76436-2370">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="76436-2370">口座番号の確認</span></span> 
- <span data-ttu-id="76436-2371">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="76436-2371">銀行口座番号</span></span> 
- <span data-ttu-id="76436-2372">銀行口座</span><span class="sxs-lookup"><span data-stu-id="76436-2372">銀行口座</span></span> 
- <span data-ttu-id="76436-2373">銀行口座 #
</span><span class="sxs-lookup"><span data-stu-id="76436-2373">銀行口座＃</span></span> 
- <span data-ttu-id="76436-2374">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2374">銀行の勘定番号</span></span> 
- <span data-ttu-id="76436-2375">銀行のacct #
</span><span class="sxs-lookup"><span data-stu-id="76436-2375">銀行のacct＃</span></span> 
- <span data-ttu-id="76436-2376">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="76436-2376">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="76436-2377">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="76436-2377">銀行口座番号</span></span>
- <span data-ttu-id="76436-2378">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2378">普通預金口座番号</span></span> 
- <span data-ttu-id="76436-2379">預金口座
</span><span class="sxs-lookup"><span data-stu-id="76436-2379">預金口座</span></span> 
- <span data-ttu-id="76436-2380">貯蓄口座 #
</span><span class="sxs-lookup"><span data-stu-id="76436-2380">貯蓄口座＃</span></span> 
- <span data-ttu-id="76436-2381">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="76436-2381">貯蓄勘定の数</span></span> 
- <span data-ttu-id="76436-2382">貯蓄勘定 #
</span><span class="sxs-lookup"><span data-stu-id="76436-2382">貯蓄勘定＃</span></span> 
- <span data-ttu-id="76436-2383">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2383">貯蓄勘定番号</span></span> 
- <span data-ttu-id="76436-2384">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2384">普通預金口座番号</span></span> 
- <span data-ttu-id="76436-2385">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2385">引き落とし口座番号</span></span> 
- <span data-ttu-id="76436-2386">口座番号</span><span class="sxs-lookup"><span data-stu-id="76436-2386">口座番号</span></span> 
- <span data-ttu-id="76436-2387">口座番号 #
</span><span class="sxs-lookup"><span data-stu-id="76436-2387">口座番号＃</span></span> 
- <span data-ttu-id="76436-2388">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2388">デビットのacct番号</span></span> 
- <span data-ttu-id="76436-2389">デビット勘定 #
</span><span class="sxs-lookup"><span data-stu-id="76436-2389">デビット勘定＃</span></span> 
- <span data-ttu-id="76436-2390">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2390">デビットACCTの番号</span></span> 
- <span data-ttu-id="76436-2391">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2391">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="76436-2392">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="76436-2392">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="76436-2393">Otemachi</span><span class="sxs-lookup"><span data-stu-id="76436-2393">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="76436-2394">일본 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2394">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2395">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2395">Format</span></span>

<span data-ttu-id="76436-2396">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2396">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2397">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2397">Pattern</span></span>

<span data-ttu-id="76436-2398">12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2398">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2399">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2399">Checksum</span></span>

<span data-ttu-id="76436-2400">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2400">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2401">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2401">Definition</span></span>

<span data-ttu-id="76436-2402">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2402">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2403">Func_jp_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2403">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2404">Keyword_jp_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2404">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2405">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2405">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="76436-2406">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="76436-2406">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="76436-2407">dl#
</span><span class="sxs-lookup"><span data-stu-id="76436-2407">dl#</span></span> 
- <span data-ttu-id="76436-2408">DL</span><span class="sxs-lookup"><span data-stu-id="76436-2408">DL＃</span></span> 
- <span data-ttu-id="76436-2409">된다</span><span class="sxs-lookup"><span data-stu-id="76436-2409">dls#</span></span> 
- <span data-ttu-id="76436-2410">된다</span><span class="sxs-lookup"><span data-stu-id="76436-2410">DLS＃</span></span> 
- <span data-ttu-id="76436-2411">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-2411">driver license</span></span> 
- <span data-ttu-id="76436-2412">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-2412">driver licenses</span></span> 
- <span data-ttu-id="76436-2413">drivers license</span><span class="sxs-lookup"><span data-stu-id="76436-2413">drivers license</span></span> 
- <span data-ttu-id="76436-2414">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-2414">driver's license</span></span> 
- <span data-ttu-id="76436-2415">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-2415">drivers licenses</span></span> 
- <span data-ttu-id="76436-2416">운전 면허증</span><span class="sxs-lookup"><span data-stu-id="76436-2416">driver's licenses</span></span> 
- <span data-ttu-id="76436-2417">driving licence
</span><span class="sxs-lookup"><span data-stu-id="76436-2417">driving licence</span></span> 
- <span data-ttu-id="76436-2418">lic</span><span class="sxs-lookup"><span data-stu-id="76436-2418">lic#</span></span> 
- <span data-ttu-id="76436-2419">LIC</span><span class="sxs-lookup"><span data-stu-id="76436-2419">LIC＃</span></span> 
- <span data-ttu-id="76436-2420">lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-2420">lics#</span></span> 
- <span data-ttu-id="76436-2421">상태 id</span><span class="sxs-lookup"><span data-stu-id="76436-2421">state id</span></span> 
- <span data-ttu-id="76436-2422">state identification
</span><span class="sxs-lookup"><span data-stu-id="76436-2422">state identification</span></span> 
- <span data-ttu-id="76436-2423">state identification number
</span><span class="sxs-lookup"><span data-stu-id="76436-2423">state identification number</span></span> 
- <span data-ttu-id="76436-2424">低所得国 #
</span><span class="sxs-lookup"><span data-stu-id="76436-2424">低所得国＃</span></span> 
- <span data-ttu-id="76436-2425">免許証
</span><span class="sxs-lookup"><span data-stu-id="76436-2425">免許証</span></span> 
- <span data-ttu-id="76436-2426">状態ID</span><span class="sxs-lookup"><span data-stu-id="76436-2426">状態ID</span></span>
- <span data-ttu-id="76436-2427">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="76436-2427">状態の識別</span></span> 
- <span data-ttu-id="76436-2428">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2428">状態の識別番号</span></span> 
- <span data-ttu-id="76436-2429">運転免許
</span><span class="sxs-lookup"><span data-stu-id="76436-2429">運転免許</span></span> 
- <span data-ttu-id="76436-2430">運転免許証
</span><span class="sxs-lookup"><span data-stu-id="76436-2430">運転免許証</span></span> 
- <span data-ttu-id="76436-2431">運転免許証番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2431">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="76436-2432">일본 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2432">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2433">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2433">Format</span></span>

<span data-ttu-id="76436-2434">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2434">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2435">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2435">Pattern</span></span>

<span data-ttu-id="76436-2436">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2436">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2437">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2437">Checksum</span></span>

<span data-ttu-id="76436-2438">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2438">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2439">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2439">Definition</span></span>

<span data-ttu-id="76436-2440">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2441">Func_jp_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2441">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2442">Keyword_jp_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2442">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2443">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2443">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="76436-2444">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="76436-2444">Keyword_jp_passport</span></span>

- <span data-ttu-id="76436-2445">パスポート
</span><span class="sxs-lookup"><span data-stu-id="76436-2445">パスポート</span></span> 
- <span data-ttu-id="76436-2446">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2446">パスポート番号</span></span> 
- <span data-ttu-id="76436-2447">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="76436-2447">パスポートのNum</span></span> 
- <span data-ttu-id="76436-2448">パスポート #
</span><span class="sxs-lookup"><span data-stu-id="76436-2448">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="76436-2449">일본 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2449">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2450">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2450">Format</span></span>

<span data-ttu-id="76436-2451">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2451">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2452">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2452">Pattern</span></span>

<span data-ttu-id="76436-2453">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2453">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2454">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2454">Checksum</span></span>

<span data-ttu-id="76436-2455">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2455">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2456">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2456">Definition</span></span>

<span data-ttu-id="76436-2457">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2458">Func_jp_resident_registration_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2458">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2459">Keyword_jp_resident_registration_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2459">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2460">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2460">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="76436-2461">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="76436-2461">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="76436-2462">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="76436-2462">Resident Registration Number</span></span>
- <span data-ttu-id="76436-2463">Resident Register Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2463">Resident Register Number</span></span> 
- <span data-ttu-id="76436-2464">Residents Basic Registry Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2464">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="76436-2465">Resident Registration No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2465">Resident Registration No.</span></span> 
- <span data-ttu-id="76436-2466">Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2466">Resident Register No.</span></span> 
- <span data-ttu-id="76436-2467">Residents Basic Registry No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2467">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="76436-2468">Basic Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2468">Basic Resident Register No.</span></span> 
- <span data-ttu-id="76436-2469">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="76436-2469">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="76436-2470">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2470">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="76436-2471">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="76436-2471">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="76436-2472">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2472">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="76436-2473">일본 SIN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="76436-2473">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="76436-2474">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2474">Format</span></span>

<span data-ttu-id="76436-2475">7-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2475">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2476">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2476">Pattern</span></span>

<span data-ttu-id="76436-2477">7-12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2477">7-12 digits:</span></span>
- <span data-ttu-id="76436-2478">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2478">Four digits</span></span> 
- <span data-ttu-id="76436-2479">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="76436-2479">A hyphen (optional)</span></span> 
- <span data-ttu-id="76436-2480">6 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="76436-2480">Six digits OR</span></span>
- <span data-ttu-id="76436-2481">7-12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2481">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2482">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2482">Checksum</span></span>

<span data-ttu-id="76436-2483">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2483">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2484">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2484">Definition</span></span>

<span data-ttu-id="76436-2485">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2485">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2486">Func_jp_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2486">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2487">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2487">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="76436-2488">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2488">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2489">Func_jp_sin_pre_1997 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2489">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2490">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2490">A keyword from Keyword_jp_sin is found.</span></span>

```
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2491">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2491">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="76436-2492">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="76436-2492">Keyword_jp_sin</span></span>

- <span data-ttu-id="76436-2493">Social Insurance No.
</span><span class="sxs-lookup"><span data-stu-id="76436-2493">Social Insurance No.</span></span> 
- <span data-ttu-id="76436-2494">Social Insurance Num
</span><span class="sxs-lookup"><span data-stu-id="76436-2494">Social Insurance Num</span></span> 
- <span data-ttu-id="76436-2495">Social Insurance Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2495">Social Insurance Number</span></span> 
- <span data-ttu-id="76436-2496">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="76436-2496">社会保険のテンキー</span></span> 
- <span data-ttu-id="76436-2497">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2497">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="76436-2498">일본어 거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2498">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2499">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2499">Format</span></span>

<span data-ttu-id="76436-2500">12 개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2500">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2501">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2501">Pattern</span></span>

<span data-ttu-id="76436-2502">12 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2502">12 letters and digits:</span></span>
- <span data-ttu-id="76436-2503">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2503">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="76436-2504">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2504">Eight digits</span></span> 
- <span data-ttu-id="76436-2505">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2505">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2506">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2506">Checksum</span></span>

<span data-ttu-id="76436-2507">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2507">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2508">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2508">Definition</span></span>

<span data-ttu-id="76436-2509">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2509">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2510">정규식 Regex_jp_residence_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2510">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2511">Keyword_jp_residence_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2511">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2512">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2512">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="76436-2513">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="76436-2513">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="76436-2514">거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2514">Residence card number</span></span>
- <span data-ttu-id="76436-2515">거주지 카드 아니요</span><span class="sxs-lookup"><span data-stu-id="76436-2515">Residence card no</span></span>
- <span data-ttu-id="76436-2516">거주지 카드 #</span><span class="sxs-lookup"><span data-stu-id="76436-2516">Residence card #</span></span>
- <span data-ttu-id="76436-2517">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="76436-2517">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="76436-2518">말레이시아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2518">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2519">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2519">Format</span></span>

<span data-ttu-id="76436-2520">선택적으로 하이픈을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2520">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2521">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2521">Pattern</span></span>

<span data-ttu-id="76436-2522">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2522">12 digits:</span></span>
- <span data-ttu-id="76436-2523">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-2523">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="76436-2524">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="76436-2524">A dash (optional)</span></span> 
- <span data-ttu-id="76436-2525">2개 문자로 이루어진 출생지 코드 </span><span class="sxs-lookup"><span data-stu-id="76436-2525">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="76436-2526">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="76436-2526">A dash (optional)</span></span> 
- <span data-ttu-id="76436-2527">임의의 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-2527">Three random digits</span></span> 
- <span data-ttu-id="76436-2528">1자리 성별 코드</span><span class="sxs-lookup"><span data-stu-id="76436-2528">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2529">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2529">Checksum</span></span>

<span data-ttu-id="76436-2530">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2530">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2531">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2531">Definition</span></span>

<span data-ttu-id="76436-2532">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2532">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2533">정규식 Regex_malaysia_id_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2533">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2534">Keyword_malaysia_id_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2534">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2535">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2535">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="76436-2536">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="76436-2536">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="76436-2537">디지털 응용 프로그램 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2537">digital application card</span></span>
- <span data-ttu-id="76436-2538">i/c</span><span class="sxs-lookup"><span data-stu-id="76436-2538">i/c</span></span>
- <span data-ttu-id="76436-2539">i/c 아니요</span><span class="sxs-lookup"><span data-stu-id="76436-2539">i/c no</span></span>
- <span data-ttu-id="76436-2540">비용</span><span class="sxs-lookup"><span data-stu-id="76436-2540">ic</span></span>
- <span data-ttu-id="76436-2541">ic 아니요</span><span class="sxs-lookup"><span data-stu-id="76436-2541">ic no</span></span>
- <span data-ttu-id="76436-2542">id 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2542">id card</span></span>
- <span data-ttu-id="76436-2543">식별 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2543">identification Card</span></span>
- <span data-ttu-id="76436-2544">identity card</span><span class="sxs-lookup"><span data-stu-id="76436-2544">identity card</span></span>
- <span data-ttu-id="76436-2545">k/p</span><span class="sxs-lookup"><span data-stu-id="76436-2545">k/p</span></span>
- <span data-ttu-id="76436-2546">k/p 아니요</span><span class="sxs-lookup"><span data-stu-id="76436-2546">k/p no</span></span>
- <span data-ttu-id="76436-2547">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="76436-2547">kad akuan diri</span></span>
- <span data-ttu-id="76436-2548">kad aplikasi 디지털</span><span class="sxs-lookup"><span data-stu-id="76436-2548">kad aplikasi digital</span></span>
- <span data-ttu-id="76436-2549">kad pengenalan 말레이시아</span><span class="sxs-lookup"><span data-stu-id="76436-2549">kad pengenalan malaysia</span></span>
- <span data-ttu-id="76436-2550">kp</span><span class="sxs-lookup"><span data-stu-id="76436-2550">kp</span></span>
- <span data-ttu-id="76436-2551">kp 아니요</span><span class="sxs-lookup"><span data-stu-id="76436-2551">kp no</span></span>
- <span data-ttu-id="76436-2552">mykad</span><span class="sxs-lookup"><span data-stu-id="76436-2552">mykad</span></span>
- <span data-ttu-id="76436-2553">mykas</span><span class="sxs-lookup"><span data-stu-id="76436-2553">mykas</span></span>
- <span data-ttu-id="76436-2554">mykid</span><span class="sxs-lookup"><span data-stu-id="76436-2554">mykid</span></span>
- <span data-ttu-id="76436-2555">mypr</span><span class="sxs-lookup"><span data-stu-id="76436-2555">mypr</span></span>
- <span data-ttu-id="76436-2556">myta</span><span class="sxs-lookup"><span data-stu-id="76436-2556">mytentera</span></span>
- <span data-ttu-id="76436-2557">말레이시아 id 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2557">malaysia identity card</span></span>
- <span data-ttu-id="76436-2558">말레이지아 id 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2558">malaysian identity card</span></span>
- <span data-ttu-id="76436-2559">nric</span><span class="sxs-lookup"><span data-stu-id="76436-2559">nric</span></span>
- <span data-ttu-id="76436-2560">개인 식별 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2560">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="76436-2561">네덜란드 시민 서비스(BSN) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2561">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2562">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2562">Format</span></span>

<span data-ttu-id="76436-2563">선택적으로 공백을 포함하는 8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2563">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2564">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2564">Pattern</span></span>

<span data-ttu-id="76436-2565">8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2565">8-9 digits:</span></span>
- <span data-ttu-id="76436-2566">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2566">Three digits</span></span> 
- <span data-ttu-id="76436-2567">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="76436-2567">A space (optional)</span></span> 
- <span data-ttu-id="76436-2568">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2568">Three digits</span></span> 
- <span data-ttu-id="76436-2569">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="76436-2569">A space (optional)</span></span> 
- <span data-ttu-id="76436-2570">2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2570">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2571">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2571">Checksum</span></span>

<span data-ttu-id="76436-2572">예</span><span class="sxs-lookup"><span data-stu-id="76436-2572">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2573">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2573">Definition</span></span>

<span data-ttu-id="76436-2574">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2574">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2575">Func_netherlands_bsn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2575">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2576">Keyword_netherlands_bsn에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2576">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="76436-2577">Func_eu_date2 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2577">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="76436-2578">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2578">The checksum passes.</span></span>

```
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2579">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2579">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="76436-2580">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="76436-2580">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="76436-2581">Citizen service number
</span><span class="sxs-lookup"><span data-stu-id="76436-2581">Citizen service number</span></span> 
- <span data-ttu-id="76436-2582">BSN

</span><span class="sxs-lookup"><span data-stu-id="76436-2582">BSN</span></span> 
- <span data-ttu-id="76436-2583">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="76436-2583">Burgerservicenummer</span></span> 
- <span data-ttu-id="76436-2584">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="76436-2584">Sofinummer</span></span> 
- <span data-ttu-id="76436-2585">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="76436-2585">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="76436-2586">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="76436-2586">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="76436-2587">뉴질랜드 보건부 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2587">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2588">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2588">Format</span></span>

<span data-ttu-id="76436-2589">3개 문자, 공백 1개(선택 사항) 및 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2589">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2590">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2590">Pattern</span></span>

<span data-ttu-id="76436-2591">3 개의 문자 (대/소문자 구분 안 함) 공백 (선택 사항) 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2591">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2592">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2592">Checksum</span></span>

<span data-ttu-id="76436-2593">예</span><span class="sxs-lookup"><span data-stu-id="76436-2593">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2594">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2594">Definition</span></span>

<span data-ttu-id="76436-2595">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2596">Func_new_zealand_ministry_of_health_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2596">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2597">Keyword_nz_terms의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2597">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="76436-2598">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2598">The checksum passes.</span></span>

```
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

<span data-ttu-id="76436-2599">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2599">Keywords</span></span>

<span data-ttu-id="76436-2600">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="76436-2600">Keyword_nz_terms</span></span>

- <span data-ttu-id="76436-2601">NHI
</span><span class="sxs-lookup"><span data-stu-id="76436-2601">NHI</span></span> 
- <span data-ttu-id="76436-2602">뉴질랜드</span><span class="sxs-lookup"><span data-stu-id="76436-2602">New Zealand</span></span> 
- <span data-ttu-id="76436-2603">상태</span><span class="sxs-lookup"><span data-stu-id="76436-2603">Health</span></span> 
- <span data-ttu-id="76436-2604">treatment
</span><span class="sxs-lookup"><span data-stu-id="76436-2604">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="76436-2605">Norway Identification Number</span><span class="sxs-lookup"><span data-stu-id="76436-2605">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2606">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2606">Format</span></span>

<span data-ttu-id="76436-2607">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2607">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2608">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2608">Pattern</span></span>

<span data-ttu-id="76436-2609">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2609">11 digits:</span></span>
- <span data-ttu-id="76436-2610">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-2610">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="76436-2611">3자리 개인 번호 </span><span class="sxs-lookup"><span data-stu-id="76436-2611">Three-digit individual number</span></span> 
- <span data-ttu-id="76436-2612">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2612">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2613">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2613">Checksum</span></span>

<span data-ttu-id="76436-2614">예</span><span class="sxs-lookup"><span data-stu-id="76436-2614">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2615">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2615">Definition</span></span>

<span data-ttu-id="76436-2616">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2616">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2617">Func_norway_id_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2617">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2618">Keyword_norway_id_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2618">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="76436-2619">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2619">The checksum passes.</span></span>
- <span data-ttu-id="76436-2620">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2620">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2621">Func_norway_id_numbe 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2621">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2622">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2622">The checksum passes.</span></span>

```
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2623">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2623">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="76436-2624">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="76436-2624">Keyword_norway_id_number</span></span>

- <span data-ttu-id="76436-2625">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="76436-2625">Personal identification number</span></span>
- <span data-ttu-id="76436-2626">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="76436-2626">Norwegian ID Number</span></span>
- <span data-ttu-id="76436-2627">ID Number</span><span class="sxs-lookup"><span data-stu-id="76436-2627">ID Number</span></span>
- <span data-ttu-id="76436-2628">Identification</span><span class="sxs-lookup"><span data-stu-id="76436-2628">Identification</span></span>
- <span data-ttu-id="76436-2629">Personnummer</span><span class="sxs-lookup"><span data-stu-id="76436-2629">Personnummer</span></span>
- <span data-ttu-id="76436-2630">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="76436-2630">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="76436-2631">필리핀 통합 다목적 ID 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2631">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2632">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2632">Format</span></span>

<span data-ttu-id="76436-2633">하이픈으로 구분된 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2633">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2634">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2634">Pattern</span></span>

<span data-ttu-id="76436-2635">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2635">12 digits:</span></span>
- <span data-ttu-id="76436-2636">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2636">Four digits</span></span> 
- <span data-ttu-id="76436-2637">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-2637">A hyphen</span></span> 
- <span data-ttu-id="76436-2638">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2638">Seven digits</span></span> 
- <span data-ttu-id="76436-2639">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-2639">A hyphen</span></span> 
- <span data-ttu-id="76436-2640">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2640">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2641">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2641">Checksum</span></span>

<span data-ttu-id="76436-2642">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2642">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2643">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2643">Definition</span></span>

<span data-ttu-id="76436-2644">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2644">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2645">정규식 Regex_philippines_unified_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2645">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2646">Keyword_philippines_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2646">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2647">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2647">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="76436-2648">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="76436-2648">Keyword_philippines_id</span></span>

- <span data-ttu-id="76436-2649">Unified Multi-Purpose ID
</span><span class="sxs-lookup"><span data-stu-id="76436-2649">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="76436-2650">UMID
</span><span class="sxs-lookup"><span data-stu-id="76436-2650">UMID</span></span> 
- <span data-ttu-id="76436-2651">Identity Card</span><span class="sxs-lookup"><span data-stu-id="76436-2651">Identity Card</span></span> 
- <span data-ttu-id="76436-2652">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="76436-2652">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="76436-2653">폴란드 ID 카드</span><span class="sxs-lookup"><span data-stu-id="76436-2653">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="76436-2654">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2654">Format</span></span>

<span data-ttu-id="76436-2655">3개의 문자 및 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2655">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2656">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2656">Pattern</span></span>

<span data-ttu-id="76436-2657">3개의 문자(대/소문자 구분 안 함)와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2657">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2658">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2658">Checksum</span></span>

<span data-ttu-id="76436-2659">예</span><span class="sxs-lookup"><span data-stu-id="76436-2659">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2660">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2660">Definition</span></span>

<span data-ttu-id="76436-p138">DLP 정책은 300 문자 근사에서 Func_polish_national_id 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다. Keyword_polish_national_id_passport_number에서 키워드가 발견 되었습니다. 체크섬이 통과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2664">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2664">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="76436-2665">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="76436-2665">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="76436-2666">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="76436-2666">Dowód osobisty</span></span>
- <span data-ttu-id="76436-2667">u r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="76436-2667">Numer dowodu osobistego</span></span>
- <span data-ttu-id="76436-2668">Nazwa i u r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="76436-2668">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="76436-2669">Nazwa i veiligheid dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="76436-2669">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="76436-2670">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="76436-2670">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="76436-2671">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="76436-2671">Dowód Tożsamości</span></span>
- <span data-ttu-id="76436-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="76436-p139">dow. os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="76436-2674">폴란드 국가 ID(PESEL)</span><span class="sxs-lookup"><span data-stu-id="76436-2674">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="76436-2675">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2675">Format</span></span>

<span data-ttu-id="76436-2676">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2676">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2677">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2677">Pattern</span></span>

<span data-ttu-id="76436-2678">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2678">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2679">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2679">Checksum</span></span>

<span data-ttu-id="76436-2680">예</span><span class="sxs-lookup"><span data-stu-id="76436-2680">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2681">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2681">Definition</span></span>

<span data-ttu-id="76436-2682">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2682">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2683">Func_pesel_identification_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2683">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2684">Keyword_pesel_identification_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2684">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="76436-2685">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2685">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2686">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2686">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="76436-2687">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="76436-2687">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="76436-2688">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="76436-2688">Nr PESEL</span></span>
- <span data-ttu-id="76436-2689">PESEL</span><span class="sxs-lookup"><span data-stu-id="76436-2689">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="76436-2690">폴란드 여권</span><span class="sxs-lookup"><span data-stu-id="76436-2690">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="76436-2691">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2691">Format</span></span>

<span data-ttu-id="76436-2692">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2692">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2693">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2693">Pattern</span></span>

<span data-ttu-id="76436-2694">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2694">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2695">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2695">Checksum</span></span>

<span data-ttu-id="76436-2696">예</span><span class="sxs-lookup"><span data-stu-id="76436-2696">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2697">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2697">Definition</span></span>

<span data-ttu-id="76436-2698">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2698">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2699">Func_polish_passport_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2699">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2700">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2700">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="76436-2701">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2701">The checksum passes.</span></span>

```
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="76436-2702">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2702">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="76436-2703">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="76436-2703">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="76436-2704">u r i (zportu)</span><span class="sxs-lookup"><span data-stu-id="76436-2704">Numer paszportu</span></span>
- <span data-ttu-id="76436-p140">veiligheid zportu</span><span class="sxs-lookup"><span data-stu-id="76436-p140">Nr. Paszportu</span></span>
- <span data-ttu-id="76436-2707">고 zport</span><span class="sxs-lookup"><span data-stu-id="76436-2707">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="76436-2708">포르투갈 시민 카드 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2708">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2709">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2709">Format</span></span>

<span data-ttu-id="76436-2710">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2710">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2711">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2711">Pattern</span></span>

<span data-ttu-id="76436-2712">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2712">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2713">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2713">Checksum</span></span>

<span data-ttu-id="76436-2714">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2714">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2715">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2715">Definition</span></span>

<span data-ttu-id="76436-2716">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2716">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2717">정규식 Regex_portugal_citizen_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2717">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2718">Keyword_portugal_citizen_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2718">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2719">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2719">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="76436-2720">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="76436-2720">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="76436-2721">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="76436-2721">Citizen Card</span></span>
- <span data-ttu-id="76436-2722">National ID Card</span><span class="sxs-lookup"><span data-stu-id="76436-2722">National ID Card</span></span>
- <span data-ttu-id="76436-2723">CC</span><span class="sxs-lookup"><span data-stu-id="76436-2723">CC</span></span>
- <span data-ttu-id="76436-2724">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="76436-2724">Cartão de Cidadão</span></span>
- <span data-ttu-id="76436-2725">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="76436-2725">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="76436-2726">사우디 아라비아 국가 ID</span><span class="sxs-lookup"><span data-stu-id="76436-2726">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="76436-2727">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2727">Format</span></span>

<span data-ttu-id="76436-2728">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2728">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2729">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2729">Pattern</span></span>

<span data-ttu-id="76436-2730">10자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2730">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2731">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2731">Checksum</span></span>

<span data-ttu-id="76436-2732">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2732">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2733">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2733">Definition</span></span>

<span data-ttu-id="76436-2734">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2734">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2735">Regex_saudi_arabia_national_id 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2735">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2736">Keyword_saudi_arabia_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2736">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2737">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2737">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="76436-2738">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="76436-2738">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="76436-2739">Identification Card
</span><span class="sxs-lookup"><span data-stu-id="76436-2739">Identification Card</span></span> 
- <span data-ttu-id="76436-2740">I card number
</span><span class="sxs-lookup"><span data-stu-id="76436-2740">I card number</span></span> 
- <span data-ttu-id="76436-2741">ID 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2741">ID number</span></span> 
- <span data-ttu-id="76436-2742">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="76436-2742">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="76436-2743">싱가포르 NRIC(국가 등록 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2743">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2744">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2744">Format</span></span>

<span data-ttu-id="76436-2745">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2745">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2746">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2746">Pattern</span></span>

- <span data-ttu-id="76436-2747">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2747">Nine letters and digits:</span></span>
- <span data-ttu-id="76436-2748">문자 "F", "G", "S" 또는 "T"(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="76436-2748">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="76436-2749">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2749">Seven digits</span></span> 
- <span data-ttu-id="76436-2750">알파벳 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2750">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2751">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2751">Checksum</span></span>

<span data-ttu-id="76436-2752">예</span><span class="sxs-lookup"><span data-stu-id="76436-2752">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2753">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2753">Definition</span></span>

<span data-ttu-id="76436-2754">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2754">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2755">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2755">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2756">Keyword_singapore_nric에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2756">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="76436-2757">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2757">The checksum passes.</span></span>

<span data-ttu-id="76436-2758">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2758">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2759">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2759">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2760">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2760">The checksum passes.</span></span>

```
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2761">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2761">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="76436-2762">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="76436-2762">Keyword_singapore_nric</span></span>

- <span data-ttu-id="76436-2763">National Registration Identity Card
</span><span class="sxs-lookup"><span data-stu-id="76436-2763">National Registration Identity Card</span></span> 
- <span data-ttu-id="76436-2764">Identity Card Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2764">Identity Card Number</span></span> 
- <span data-ttu-id="76436-2765">NRIC
</span><span class="sxs-lookup"><span data-stu-id="76436-2765">NRIC</span></span> 
- <span data-ttu-id="76436-2766">IC
</span><span class="sxs-lookup"><span data-stu-id="76436-2766">IC</span></span> 
- <span data-ttu-id="76436-2767">Foreign Identification Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2767">Foreign Identification Number</span></span> 
- <span data-ttu-id="76436-2768">FIN
</span><span class="sxs-lookup"><span data-stu-id="76436-2768">FIN</span></span> 
- <span data-ttu-id="76436-2769">身份证 </span><span class="sxs-lookup"><span data-stu-id="76436-2769">身份证</span></span> 
- <span data-ttu-id="76436-2770">身份證
</span><span class="sxs-lookup"><span data-stu-id="76436-2770">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="76436-2771">남아프리카 공화국 식별 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2771">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2772">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2772">Format</span></span>

<span data-ttu-id="76436-2773">공백을 포함할 수 있는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2773">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2774">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2774">Pattern</span></span>

<span data-ttu-id="76436-2775">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2775">13 digits:</span></span>
- <span data-ttu-id="76436-2776">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-2776">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="76436-2777">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2777">Four digits</span></span> 
- <span data-ttu-id="76436-2778">1자리 시민권 표시 </span><span class="sxs-lookup"><span data-stu-id="76436-2778">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="76436-2779">숫자 "8" 또는 "9" </span><span class="sxs-lookup"><span data-stu-id="76436-2779">The digit "8" or "9"</span></span> 
- <span data-ttu-id="76436-2780">체크섬 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2780">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2781">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2781">Checksum</span></span>

<span data-ttu-id="76436-2782">예</span><span class="sxs-lookup"><span data-stu-id="76436-2782">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2783">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2783">Definition</span></span>

<span data-ttu-id="76436-2784">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2785">Func_south_africa_identification_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2785">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2786">Keyword_south_africa_identification_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2786">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="76436-2787">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2787">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2788">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2788">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="76436-2789">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="76436-2789">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="76436-2790">Identity card</span><span class="sxs-lookup"><span data-stu-id="76436-2790">Identity card</span></span>
- <span data-ttu-id="76436-2791">ID</span><span class="sxs-lookup"><span data-stu-id="76436-2791">ID</span></span>
- <span data-ttu-id="76436-2792">Identification</span><span class="sxs-lookup"><span data-stu-id="76436-2792">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="76436-2793">한국 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2793">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2794">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2794">Format</span></span>

<span data-ttu-id="76436-2795">하이픈을 포함하는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2795">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2796">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2796">Pattern</span></span>

<span data-ttu-id="76436-2797">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2797">13 digits:</span></span>
- <span data-ttu-id="76436-2798">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-2798">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="76436-2799">하이픈</span><span class="sxs-lookup"><span data-stu-id="76436-2799">A hyphen</span></span> 
- <span data-ttu-id="76436-2800">세기 및 성별에 따라 결정되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-2800">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="76436-2801">4자리 출생 지역 코드 </span><span class="sxs-lookup"><span data-stu-id="76436-2801">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="76436-2802">앞 번호가 동일한 사람을 구분하기 위해 사용되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="76436-2802">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="76436-2803">검사 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2803">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2804">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2804">Checksum</span></span>

<span data-ttu-id="76436-2805">예</span><span class="sxs-lookup"><span data-stu-id="76436-2805">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2806">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2806">Definition</span></span>

<span data-ttu-id="76436-2807">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2807">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2808">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2808">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2809">Keyword_south_korea_resident_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2809">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="76436-2810">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2810">The checksum passes.</span></span>

<span data-ttu-id="76436-2811">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2811">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2812">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2812">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2813">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2813">The checksum passes.</span></span>

```
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2814">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2814">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="76436-2815">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="76436-2815">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="76436-2816">National ID card
</span><span class="sxs-lookup"><span data-stu-id="76436-2816">National ID card</span></span> 
- <span data-ttu-id="76436-2817">Citizen's Registration Number
</span><span class="sxs-lookup"><span data-stu-id="76436-2817">Citizen's Registration Number</span></span> 
- <span data-ttu-id="76436-2818">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="76436-2818">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="76436-2819">RRN
</span><span class="sxs-lookup"><span data-stu-id="76436-2819">RRN</span></span> 
- <span data-ttu-id="76436-2820">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="76436-2820">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="76436-2821">스페인 SSN(사회 보장 번호)</span><span class="sxs-lookup"><span data-stu-id="76436-2821">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="76436-2822">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2822">Format</span></span>

<span data-ttu-id="76436-2823">11-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2823">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2824">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2824">Pattern</span></span>

<span data-ttu-id="76436-2825">11-12 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2825">11-12 digits:</span></span>
- <span data-ttu-id="76436-2826">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2826">Two digits</span></span> 
- <span data-ttu-id="76436-2827">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="76436-2827">A forward slash (optional)</span></span> 
- <span data-ttu-id="76436-2828">7-8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2828">7-8 digits</span></span> 
- <span data-ttu-id="76436-2829">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="76436-2829">A forward slash (optional)</span></span> 
- <span data-ttu-id="76436-2830">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2830">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2831">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2831">Checksum</span></span>

<span data-ttu-id="76436-2832">예</span><span class="sxs-lookup"><span data-stu-id="76436-2832">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2833">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2833">Definition</span></span>

<span data-ttu-id="76436-2834">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2834">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2835">Func_spanish_social_security_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2835">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2836">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2836">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2837">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2837">Keywords</span></span>

<span data-ttu-id="76436-2838">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2838">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="76436-2839">스웨덴 국가 ID</span><span class="sxs-lookup"><span data-stu-id="76436-2839">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="76436-2840">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2840">Format</span></span>

<span data-ttu-id="76436-2841">10 또는 12자리 숫자와 선택적 구분 기호</span><span class="sxs-lookup"><span data-stu-id="76436-2841">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2842">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2842">Pattern</span></span>

<span data-ttu-id="76436-2843">10 또는 12자리 숫자와 선택적 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="76436-2843">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="76436-2844">2-4자리 숫자(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="76436-2844">2-4 digits (optional)</span></span> 
- <span data-ttu-id="76436-2845">YYMMDD 날짜 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2845">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="76436-2846">구분 기호 "-" 또는 "+"(선택 사항) 및</span><span class="sxs-lookup"><span data-stu-id="76436-2846">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="76436-2847">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2847">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2848">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2848">Checksum</span></span>

<span data-ttu-id="76436-2849">예</span><span class="sxs-lookup"><span data-stu-id="76436-2849">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2850">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2850">Definition</span></span>

<span data-ttu-id="76436-2851">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2851">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2852">Func_swedish_national_identifier 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2852">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2853">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2853">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2854">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2854">Keywords</span></span>

<span data-ttu-id="76436-2855">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2855">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="76436-2856">스웨덴 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2856">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2857">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2857">Format</span></span>

<span data-ttu-id="76436-2858">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2858">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2859">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2859">Pattern</span></span>

<span data-ttu-id="76436-2860">8자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2860">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2861">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2861">Checksum</span></span>

<span data-ttu-id="76436-2862">아니요</span><span class="sxs-lookup"><span data-stu-id="76436-2862">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2863">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2863">Definition</span></span>

<span data-ttu-id="76436-2864">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2864">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2865">Regex_sweden_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2865">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2866">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2866">One of the following is true:</span></span>
    - <span data-ttu-id="76436-2867">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2867">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="76436-2868">Keyword_sweden_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2868">A keyword from Keyword_sweden_passport is found.</span></span>

```
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2869">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2869">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="76436-2870">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="76436-2870">Keyword_sweden_passport</span></span>

- <span data-ttu-id="76436-2871">visa requirements
</span><span class="sxs-lookup"><span data-stu-id="76436-2871">visa requirements</span></span> 
- <span data-ttu-id="76436-2872">Alien Registration Card
</span><span class="sxs-lookup"><span data-stu-id="76436-2872">Alien Registration Card</span></span> 
- <span data-ttu-id="76436-2873">Schengen visas
</span><span class="sxs-lookup"><span data-stu-id="76436-2873">Schengen visas</span></span> 
- <span data-ttu-id="76436-2874">Schengen visa
</span><span class="sxs-lookup"><span data-stu-id="76436-2874">Schengen visa</span></span> 
- <span data-ttu-id="76436-2875">Visa Processing
</span><span class="sxs-lookup"><span data-stu-id="76436-2875">Visa Processing</span></span> 
- <span data-ttu-id="76436-2876">Visa Type
</span><span class="sxs-lookup"><span data-stu-id="76436-2876">Visa Type</span></span> 
- <span data-ttu-id="76436-2877">Single Entry
</span><span class="sxs-lookup"><span data-stu-id="76436-2877">Single Entry</span></span> 
- <span data-ttu-id="76436-2878">Multiple Entry
</span><span class="sxs-lookup"><span data-stu-id="76436-2878">Multiple Entry</span></span> 
- <span data-ttu-id="76436-2879">G3 Processing Fees

</span><span class="sxs-lookup"><span data-stu-id="76436-2879">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="76436-2880">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="76436-2880">Keyword_passport</span></span>

- <span data-ttu-id="76436-2881">Passport Number</span><span class="sxs-lookup"><span data-stu-id="76436-2881">Passport Number</span></span> 
- <span data-ttu-id="76436-2882">
Passport No</span><span class="sxs-lookup"><span data-stu-id="76436-2882">Passport No</span></span> 
- <span data-ttu-id="76436-2883">Passport #
</span><span class="sxs-lookup"><span data-stu-id="76436-2883">Passport #</span></span> 
- <span data-ttu-id="76436-2884">Passport#
</span><span class="sxs-lookup"><span data-stu-id="76436-2884">Passport#</span></span> 
- <span data-ttu-id="76436-2885">PassportID</span><span class="sxs-lookup"><span data-stu-id="76436-2885">PassportID</span></span> 
- <span data-ttu-id="76436-2886">Passportno
</span><span class="sxs-lookup"><span data-stu-id="76436-2886">Passportno</span></span> 
- <span data-ttu-id="76436-2887">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-2887">passportnumber</span></span> 
- <span data-ttu-id="76436-2888">パスポート</span><span class="sxs-lookup"><span data-stu-id="76436-2888">パスポート</span></span> 
- <span data-ttu-id="76436-2889">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2889">パスポート番号</span></span> 
- <span data-ttu-id="76436-2890">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="76436-2890">パスポートのNum</span></span> 
- <span data-ttu-id="76436-2891">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="76436-2891">パスポート＃</span></span> 
- <span data-ttu-id="76436-2892">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="76436-2892">Numéro de passeport</span></span> 
- <span data-ttu-id="76436-2893">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="76436-2893">Passeport n °</span></span> 
- <span data-ttu-id="76436-2894">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="76436-2894">Passeport Non</span></span> 
- <span data-ttu-id="76436-2895">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="76436-2895">Passeport #</span></span> 
- <span data-ttu-id="76436-2896">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="76436-2896">Passeport#</span></span> 
- <span data-ttu-id="76436-2897">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="76436-2897">PasseportNon</span></span> 
- <span data-ttu-id="76436-2898">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="76436-2898">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="76436-2899">SWIFT 코드</span><span class="sxs-lookup"><span data-stu-id="76436-2899">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="76436-2900">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2900">Format</span></span>

<span data-ttu-id="76436-2901">4개의 문자, 5-31개 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2901">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2902">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2902">Pattern</span></span>

<span data-ttu-id="76436-2903">4개의 문자, 5-31개 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2903">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="76436-2904">4문자 은행 코드(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2904">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="76436-2905">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="76436-2905">An optional space</span></span> 
- <span data-ttu-id="76436-2906">4-28개 문자 또는 숫자[BBAN(기본 은행 계좌 번호)]</span><span class="sxs-lookup"><span data-stu-id="76436-2906">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="76436-2907">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="76436-2907">An optional space</span></span> 
- <span data-ttu-id="76436-2908">1-3개 문자 또는 숫자(BBAN의 나머지)</span><span class="sxs-lookup"><span data-stu-id="76436-2908">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2909">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2909">Checksum</span></span>

<span data-ttu-id="76436-2910">아니요</span><span class="sxs-lookup"><span data-stu-id="76436-2910">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2911">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2911">Definition</span></span>

<span data-ttu-id="76436-2912">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2913">Regex_swift 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2913">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2914">Keyword_swift의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2914">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2915">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2915">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="76436-2916">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="76436-2916">Keyword_swift</span></span>

- <span data-ttu-id="76436-2917">international organization for standardization 9362
</span><span class="sxs-lookup"><span data-stu-id="76436-2917">international organization for standardization 9362</span></span> 
- <span data-ttu-id="76436-2918">iso 9362
</span><span class="sxs-lookup"><span data-stu-id="76436-2918">iso 9362</span></span> 
- <span data-ttu-id="76436-2919">iso9362</span><span class="sxs-lookup"><span data-stu-id="76436-2919">iso9362</span></span> 
- <span data-ttu-id="76436-2920">swift\#</span><span class="sxs-lookup"><span data-stu-id="76436-2920">swift\#</span></span> 
- <span data-ttu-id="76436-2921">swiftcode
</span><span class="sxs-lookup"><span data-stu-id="76436-2921">swiftcode</span></span> 
- <span data-ttu-id="76436-2922">swiftnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-2922">swiftnumber</span></span> 
- <span data-ttu-id="76436-2923">swiftroutingnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-2923">swiftroutingnumber</span></span> 
- <span data-ttu-id="76436-2924">swift code
</span><span class="sxs-lookup"><span data-stu-id="76436-2924">swift code</span></span> 
- <span data-ttu-id="76436-2925">swift number #
</span><span class="sxs-lookup"><span data-stu-id="76436-2925">swift number #</span></span> 
- <span data-ttu-id="76436-2926">swift routing number
</span><span class="sxs-lookup"><span data-stu-id="76436-2926">swift routing number</span></span> 
- <span data-ttu-id="76436-2927">bic number
</span><span class="sxs-lookup"><span data-stu-id="76436-2927">bic number</span></span> 
- <span data-ttu-id="76436-2928">bic code
</span><span class="sxs-lookup"><span data-stu-id="76436-2928">bic code</span></span> 
- <span data-ttu-id="76436-2929">bic\#</span><span class="sxs-lookup"><span data-stu-id="76436-2929">bic \#</span></span> 
- <span data-ttu-id="76436-2930">bic\#</span><span class="sxs-lookup"><span data-stu-id="76436-2930">bic\#</span></span> 
- <span data-ttu-id="76436-2931">bank identifier code
</span><span class="sxs-lookup"><span data-stu-id="76436-2931">bank identifier code</span></span> 
- <span data-ttu-id="76436-2932">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="76436-2932">標準化9362</span></span> 
- <span data-ttu-id="76436-2933">迅速＃
</span><span class="sxs-lookup"><span data-stu-id="76436-2933">迅速＃</span></span> 
- <span data-ttu-id="76436-2934">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="76436-2934">SWIFTコード</span></span> 
- <span data-ttu-id="76436-2935">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2935">SWIFT番号</span></span> 
- <span data-ttu-id="76436-2936">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2936">迅速なルーティング番号</span></span> 
- <span data-ttu-id="76436-2937">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="76436-2937">BIC番号</span></span> 
- <span data-ttu-id="76436-2938">BICコード
</span><span class="sxs-lookup"><span data-stu-id="76436-2938">BICコード</span></span> 
- <span data-ttu-id="76436-2939">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="76436-2939">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="76436-2940">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="76436-2940">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="76436-2941">rapide\#</span><span class="sxs-lookup"><span data-stu-id="76436-2941">rapide \#</span></span> 
- <span data-ttu-id="76436-2942">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="76436-2942">code SWIFT</span></span> 
- <span data-ttu-id="76436-2943">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="76436-2943">le numéro de swift</span></span> 
- <span data-ttu-id="76436-2944">swift numéro d'acheminement
</span><span class="sxs-lookup"><span data-stu-id="76436-2944">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="76436-2945">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="76436-2945">le numéro BIC</span></span> 
- <span data-ttu-id="76436-2946">\#bic</span><span class="sxs-lookup"><span data-stu-id="76436-2946">\# BIC</span></span> 
- <span data-ttu-id="76436-2947">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="76436-2947">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="76436-2948">대만 국가 ID</span><span class="sxs-lookup"><span data-stu-id="76436-2948">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="76436-2949">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2949">Format</span></span>

<span data-ttu-id="76436-2950">1개의 문자, 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2950">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2951">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2951">Pattern</span></span>

<span data-ttu-id="76436-2952">1개의 문자, 9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-2952">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="76436-2953">1개 문자(영문, 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-2953">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="76436-2954">숫자 "1" 또는 "2"</span><span class="sxs-lookup"><span data-stu-id="76436-2954">The digit "1" or "2"</span></span> 
- <span data-ttu-id="76436-2955">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2955">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2956">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2956">Checksum</span></span>

<span data-ttu-id="76436-2957">예</span><span class="sxs-lookup"><span data-stu-id="76436-2957">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2958">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2958">Definition</span></span>

<span data-ttu-id="76436-2959">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2959">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2960">Func_taiwanese_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2960">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2961">Keyword_taiwanese_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2961">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="76436-2962">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2962">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2963">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2963">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="76436-2964">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="76436-2964">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="76436-2965">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="76436-2965">身份證字號</span></span> 
- <span data-ttu-id="76436-2966">身份證
</span><span class="sxs-lookup"><span data-stu-id="76436-2966">身份證</span></span> 
- <span data-ttu-id="76436-2967">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="76436-2967">身份證號碼</span></span> 
- <span data-ttu-id="76436-2968">身份證號
</span><span class="sxs-lookup"><span data-stu-id="76436-2968">身份證號</span></span> 
- <span data-ttu-id="76436-2969">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="76436-2969">身分證字號</span></span> 
- <span data-ttu-id="76436-2970">身分證 </span><span class="sxs-lookup"><span data-stu-id="76436-2970">身分證</span></span> 
- <span data-ttu-id="76436-2971">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="76436-2971">身分證號碼</span></span> 
- <span data-ttu-id="76436-2972">身份證號
</span><span class="sxs-lookup"><span data-stu-id="76436-2972">身份證號</span></span> 
- <span data-ttu-id="76436-2973">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="76436-2973">身分證統一編號</span></span> 
- <span data-ttu-id="76436-2974">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="76436-2974">國民身分證統一編號</span></span> 
- <span data-ttu-id="76436-2975">簽名
</span><span class="sxs-lookup"><span data-stu-id="76436-2975">簽名</span></span> 
- <span data-ttu-id="76436-2976">蓋章
</span><span class="sxs-lookup"><span data-stu-id="76436-2976">蓋章</span></span> 
- <span data-ttu-id="76436-2977">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="76436-2977">簽名或蓋章</span></span> 
- <span data-ttu-id="76436-2978">簽章</span><span class="sxs-lookup"><span data-stu-id="76436-2978">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="76436-2979">	대만 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2979">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-2980">형식</span><span class="sxs-lookup"><span data-stu-id="76436-2980">Format</span></span>

- <span data-ttu-id="76436-2981">생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2981">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="76436-2982">비-생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2982">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-2983">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-2983">Pattern</span></span>
<span data-ttu-id="76436-2984">생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="76436-2984">Biometric passport number:</span></span>
- <span data-ttu-id="76436-2985">숫자 "3" </span><span class="sxs-lookup"><span data-stu-id="76436-2985">The digit "3"</span></span> 
- <span data-ttu-id="76436-2986">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2986">Eight digits</span></span>

<span data-ttu-id="76436-2987">비-생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="76436-2987">Non-biometric passport number:</span></span>
- <span data-ttu-id="76436-2988">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-2988">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-2989">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-2989">Checksum</span></span>

<span data-ttu-id="76436-2990">없음</span><span class="sxs-lookup"><span data-stu-id="76436-2990">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-2991">정의</span><span class="sxs-lookup"><span data-stu-id="76436-2991">Definition</span></span>

<span data-ttu-id="76436-2992">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2992">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-2993">정규식 Regex_taiwan_passport 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2993">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-2994">Keyword_taiwan_passport에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-2994">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-2995">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-2995">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="76436-2996">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="76436-2996">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="76436-2997">ROC passport number
</span><span class="sxs-lookup"><span data-stu-id="76436-2997">ROC passport number</span></span> 
- <span data-ttu-id="76436-2998">여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-2998">Passport number</span></span> 
- <span data-ttu-id="76436-2999">Passport 아니요</span><span class="sxs-lookup"><span data-stu-id="76436-2999">Passport no</span></span> 
- <span data-ttu-id="76436-3000">Passport Num
</span><span class="sxs-lookup"><span data-stu-id="76436-3000">Passport Num</span></span> 
- <span data-ttu-id="76436-3001">Passport #
</span><span class="sxs-lookup"><span data-stu-id="76436-3001">Passport #</span></span> 
- <span data-ttu-id="76436-3002">护照
</span><span class="sxs-lookup"><span data-stu-id="76436-3002">护照</span></span> 
- <span data-ttu-id="76436-3003">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="76436-3003">中華民國護照</span></span> 
- <span data-ttu-id="76436-3004">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="76436-3004">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="76436-3005">대만 거주 인증(ARC/TARC) 번호</span><span class="sxs-lookup"><span data-stu-id="76436-3005">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-3006">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3006">Format</span></span>

<span data-ttu-id="76436-3007">10개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3007">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3008">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3008">Pattern</span></span>

<span data-ttu-id="76436-3009">10개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-3009">10 letters and digits:</span></span>
- <span data-ttu-id="76436-3010">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-3010">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="76436-3011">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3011">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3012">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3012">Checksum</span></span>

<span data-ttu-id="76436-3013">없음</span><span class="sxs-lookup"><span data-stu-id="76436-3013">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3014">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3014">Definition</span></span>

<span data-ttu-id="76436-3015">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3015">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3016">정규식 Regex_taiwan_resident_certificate 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3016">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3017">Keyword_taiwan_resident_certificate에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3017">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3018">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3018">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="76436-3019">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="76436-3019">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="76436-3020">Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="76436-3020">Resident Certificate</span></span> 
- <span data-ttu-id="76436-3021">상주 인증서</span><span class="sxs-lookup"><span data-stu-id="76436-3021">Resident Cert</span></span> 
- <span data-ttu-id="76436-3022">Resident Cert.
</span><span class="sxs-lookup"><span data-stu-id="76436-3022">Resident Cert.</span></span> 
- <span data-ttu-id="76436-3023">식별 카드</span><span class="sxs-lookup"><span data-stu-id="76436-3023">Identification card</span></span> 
- <span data-ttu-id="76436-3024">Alien Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="76436-3024">Alien Resident Certificate</span></span> 
- <span data-ttu-id="76436-3025">화살표</span><span class="sxs-lookup"><span data-stu-id="76436-3025">ARC</span></span> 
- <span data-ttu-id="76436-3026">Taiwan Area Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="76436-3026">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="76436-3027">TARC
</span><span class="sxs-lookup"><span data-stu-id="76436-3027">TARC</span></span> 
- <span data-ttu-id="76436-3028">居留證
</span><span class="sxs-lookup"><span data-stu-id="76436-3028">居留證</span></span> 
- <span data-ttu-id="76436-3029">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="76436-3029">外僑居留證</span></span> 
- <span data-ttu-id="76436-3030">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="76436-3030">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="76436-3031">태국어 인구 식별 코드</span><span class="sxs-lookup"><span data-stu-id="76436-3031">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="76436-3032">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3032">Format</span></span>

<span data-ttu-id="76436-3033">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3033">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3034">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3034">Pattern</span></span>

<span data-ttu-id="76436-3035">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-3035">13 digits:</span></span>
- <span data-ttu-id="76436-3036">첫 번째 숫자가 0 또는 9가 아님</span><span class="sxs-lookup"><span data-stu-id="76436-3036">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="76436-3037">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3037">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3038">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3038">Checksum</span></span>

<span data-ttu-id="76436-3039">예</span><span class="sxs-lookup"><span data-stu-id="76436-3039">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3040">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3040">Definition</span></span>

<span data-ttu-id="76436-3041">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3041">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3042">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3042">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3043">Keyword_Thai_Citizen_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3043">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="76436-3044">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3044">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3045">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3045">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```
<!-- Thai Citizen ID -->
-<Entity id="44ca9e86-ead7-4c5d-884a-e2eaa401515e" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
      <Match idRef="Keyword_Thai_Citizen_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3046">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3046">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="76436-3047">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="76436-3047">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="76436-3048">ID Number</span><span class="sxs-lookup"><span data-stu-id="76436-3048">ID Number</span></span>
- <span data-ttu-id="76436-3049">id 번호</span><span class="sxs-lookup"><span data-stu-id="76436-3049">Identification Number</span></span>
- <span data-ttu-id="76436-3050">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="76436-3050">บัตรประชาชน</span></span>
- <span data-ttu-id="76436-3051">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="76436-3051">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="76436-3052">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="76436-3052">บัตรประชาชน</span></span>
- <span data-ttu-id="76436-3053">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="76436-3053">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="76436-3054">터키어 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="76436-3054">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-3055">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3055">Format</span></span>

<span data-ttu-id="76436-3056">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3056">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3057">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3057">Pattern</span></span>

<span data-ttu-id="76436-3058">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3058">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3059">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3059">Checksum</span></span>

<span data-ttu-id="76436-3060">예</span><span class="sxs-lookup"><span data-stu-id="76436-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3061">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3061">Definition</span></span>

<span data-ttu-id="76436-3062">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3063">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3063">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3064">Keyword_Turkish_National_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3064">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="76436-3065">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3065">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3066">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3066">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```
<!-- Turkish National Identity -->
-<Entity id="fb621f20-3876-4cfc-acec-8c8e73ca32c7" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Turkish_National_Id"/>
      <Match idRef="Keyword_Turkish_National_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Turkish_National_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3067">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3067">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="76436-3068">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="76436-3068">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="76436-3069">TC Kimlik 아니요</span><span class="sxs-lookup"><span data-stu-id="76436-3069">TC Kimlik No</span></span>
- <span data-ttu-id="76436-3070">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="76436-3070">TC Kimlik numarası</span></span>
- <span data-ttu-id="76436-3071">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="76436-3071">Vatandaşlık numarası</span></span>
- <span data-ttu-id="76436-3072">Vatandaşlık 아니요</span><span class="sxs-lookup"><span data-stu-id="76436-3072">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="76436-p141">영국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-3075">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3075">Format</span></span>

<span data-ttu-id="76436-3076">지정된 형식의 18개 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="76436-3076">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3077">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3077">Pattern</span></span>

<span data-ttu-id="76436-3078">18개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-3078">18 letters and digits:</span></span>
- <span data-ttu-id="76436-3079">5개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="76436-3079">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="76436-3080">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3080">One digit</span></span> 
- <span data-ttu-id="76436-3081">생년월일에 대한 DDMMY 날짜 형식의 5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3081">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="76436-3082">2개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="76436-3082">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="76436-3083">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3083">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3084">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3084">Checksum</span></span>

<span data-ttu-id="76436-3085">예</span><span class="sxs-lookup"><span data-stu-id="76436-3085">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3086">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3086">Definition</span></span>

<span data-ttu-id="76436-3087">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3087">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3088">Func_uk_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3088">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3089">Keyword_uk_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3089">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="76436-3090">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3090">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3091">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3091">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="76436-3092">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="76436-3092">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="76436-3093">DVLA
</span><span class="sxs-lookup"><span data-stu-id="76436-3093">DVLA</span></span> 
- <span data-ttu-id="76436-3094">light vans
</span><span class="sxs-lookup"><span data-stu-id="76436-3094">light vans</span></span> 
- <span data-ttu-id="76436-3095">quadbikes
</span><span class="sxs-lookup"><span data-stu-id="76436-3095">quadbikes</span></span> 
- <span data-ttu-id="76436-3096">motor cars
</span><span class="sxs-lookup"><span data-stu-id="76436-3096">motor cars</span></span> 
- <span data-ttu-id="76436-3097">125cc</span><span class="sxs-lookup"><span data-stu-id="76436-3097">125cc</span></span> 
- <span data-ttu-id="76436-3098">sidecar
</span><span class="sxs-lookup"><span data-stu-id="76436-3098">sidecar</span></span> 
- <span data-ttu-id="76436-3099">tricycles
</span><span class="sxs-lookup"><span data-stu-id="76436-3099">tricycles</span></span> 
- <span data-ttu-id="76436-3100">motorcycles
</span><span class="sxs-lookup"><span data-stu-id="76436-3100">motorcycles</span></span> 
- <span data-ttu-id="76436-3101">photocard licence
</span><span class="sxs-lookup"><span data-stu-id="76436-3101">photocard licence</span></span> 
- <span data-ttu-id="76436-3102">learner drivers
</span><span class="sxs-lookup"><span data-stu-id="76436-3102">learner drivers</span></span> 
- <span data-ttu-id="76436-3103">licence holder
</span><span class="sxs-lookup"><span data-stu-id="76436-3103">licence holder</span></span> 
- <span data-ttu-id="76436-3104">licence holders
</span><span class="sxs-lookup"><span data-stu-id="76436-3104">licence holders</span></span> 
- <span data-ttu-id="76436-3105">driving licences
</span><span class="sxs-lookup"><span data-stu-id="76436-3105">driving licences</span></span> 
- <span data-ttu-id="76436-3106">driving licence
</span><span class="sxs-lookup"><span data-stu-id="76436-3106">driving licence</span></span> 
- <span data-ttu-id="76436-3107">dual control car
</span><span class="sxs-lookup"><span data-stu-id="76436-3107">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="76436-p142">영국 선거 롤 번호</span><span class="sxs-lookup"><span data-stu-id="76436-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-3110">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3110">Format</span></span>

<span data-ttu-id="76436-3111">2개의 문자, 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3111">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3112">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3112">Pattern</span></span>

<span data-ttu-id="76436-3113">2개의 문자(대/소문자 구분 안 함)와 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3113">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3114">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3114">Checksum</span></span>

<span data-ttu-id="76436-3115">없음</span><span class="sxs-lookup"><span data-stu-id="76436-3115">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3116">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3116">Definition</span></span>

<span data-ttu-id="76436-3117">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3118">Regex_uk_electoral 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3118">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3119">Keyword_uk_electoral의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3119">A keyword from Keyword_uk_electoral is found.</span></span>

```
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3120">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3120">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="76436-3121">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="76436-3121">Keyword_uk_electoral</span></span>

- <span data-ttu-id="76436-3122">council nomination
</span><span class="sxs-lookup"><span data-stu-id="76436-3122">council nomination</span></span> 
- <span data-ttu-id="76436-3123">nomination form
</span><span class="sxs-lookup"><span data-stu-id="76436-3123">nomination form</span></span> 
- <span data-ttu-id="76436-3124">electoral register

</span><span class="sxs-lookup"><span data-stu-id="76436-3124">electoral register</span></span> 
- <span data-ttu-id="76436-3125">electoral roll</span><span class="sxs-lookup"><span data-stu-id="76436-3125">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="76436-p143">영국 국립 보건 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="76436-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-3128">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3128">Format</span></span>

<span data-ttu-id="76436-3129">공백으로 구분된 10-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3129">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3130">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3130">Pattern</span></span>

<span data-ttu-id="76436-3131">10-17자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="76436-3131">10-17 digits:</span></span>
- <span data-ttu-id="76436-3132">3 또는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3132">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="76436-3133">공백</span><span class="sxs-lookup"><span data-stu-id="76436-3133">A space</span></span> 
- <span data-ttu-id="76436-3134">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3134">Three digits</span></span> 
- <span data-ttu-id="76436-3135">공백</span><span class="sxs-lookup"><span data-stu-id="76436-3135">A space</span></span> 
- <span data-ttu-id="76436-3136">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3136">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3137">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3137">Checksum</span></span>

<span data-ttu-id="76436-3138">예</span><span class="sxs-lookup"><span data-stu-id="76436-3138">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3139">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3139">Definition</span></span>

<span data-ttu-id="76436-3140">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3140">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3141">Func_uk_nhs_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3141">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3142">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3142">One of the following is true:</span></span>
    - <span data-ttu-id="76436-3143">Keyword_uk_nhs_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3143">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="76436-3144">Keyword_uk_nhs_number1의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3144">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="76436-3145">Keyword_uk_nhs_number_dob의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3145">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="76436-3146">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3146">The checksum passes.</span></span>

```
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3147">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3147">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="76436-3148">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="76436-3148">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="76436-3149">국립 보건 서비스
</span><span class="sxs-lookup"><span data-stu-id="76436-3149">national health service</span></span> 
- <span data-ttu-id="76436-3150">nhs
</span><span class="sxs-lookup"><span data-stu-id="76436-3150">nhs</span></span> 
- <span data-ttu-id="76436-3151">health services authority

</span><span class="sxs-lookup"><span data-stu-id="76436-3151">health services authority</span></span> 
- <span data-ttu-id="76436-3152">health authority</span><span class="sxs-lookup"><span data-stu-id="76436-3152">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="76436-3153">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="76436-3153">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="76436-3154">patient id
</span><span class="sxs-lookup"><span data-stu-id="76436-3154">patient id</span></span> 
- <span data-ttu-id="76436-3155">patient identification
</span><span class="sxs-lookup"><span data-stu-id="76436-3155">patient identification</span></span> 
- <span data-ttu-id="76436-3156">patient no

</span><span class="sxs-lookup"><span data-stu-id="76436-3156">patient no</span></span> 
- <span data-ttu-id="76436-3157">patient number</span><span class="sxs-lookup"><span data-stu-id="76436-3157">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="76436-3158">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="76436-3158">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="76436-3159">GP</span><span class="sxs-lookup"><span data-stu-id="76436-3159">GP</span></span> 
- <span data-ttu-id="76436-3160">DOB
</span><span class="sxs-lookup"><span data-stu-id="76436-3160">DOB</span></span> 
- <span data-ttu-id="76436-3161">D. O. B</span><span class="sxs-lookup"><span data-stu-id="76436-3161">D.O.B</span></span> 
- <span data-ttu-id="76436-3162">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="76436-3162">Date of Birth</span></span> 
- <span data-ttu-id="76436-3163">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="76436-3163">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="76436-p144">영국 NINO(국민 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="76436-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="76436-3166">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3166">Format</span></span>

<span data-ttu-id="76436-3167">공백 또는 대시로 구분 된 7 자 또는 9 자</span><span class="sxs-lookup"><span data-stu-id="76436-3167">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3168">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3168">Pattern</span></span>

<span data-ttu-id="76436-3169">다음과 같은 두 가지 패턴을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3169">Two possible patterns:</span></span>

- <span data-ttu-id="76436-3170">두 문자 (유효한 NINOs이 접두사의 특정 문자만 사용 하며이 패턴의 유효성 검사는 대/소문자를 구분 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="76436-3170">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="76436-3171">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3171">Six digits</span></span>
- <span data-ttu-id="76436-3172">' A ', ' B ', ' C ' 또는 ' d ' (접두사와 마찬가지로 접미사에서는 특정 문자만 허용 되며 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="76436-3172">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="76436-3173">또는</span><span class="sxs-lookup"><span data-stu-id="76436-3173">OR</span></span>

- <span data-ttu-id="76436-3174">2 개 문자</span><span class="sxs-lookup"><span data-stu-id="76436-3174">Two letters</span></span>
- <span data-ttu-id="76436-3175">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="76436-3175">A space or dash</span></span>
- <span data-ttu-id="76436-3176">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3176">Two digits</span></span>
- <span data-ttu-id="76436-3177">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="76436-3177">A space or dash</span></span>
- <span data-ttu-id="76436-3178">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3178">Two digits</span></span>
- <span data-ttu-id="76436-3179">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="76436-3179">A space or dash</span></span>
- <span data-ttu-id="76436-3180">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3180">Two digits</span></span>
- <span data-ttu-id="76436-3181">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="76436-3181">A space or dash</span></span>
- <span data-ttu-id="76436-3182">' A ', ' B ', ' C ' 또는 ' d ' 중 하나</span><span class="sxs-lookup"><span data-stu-id="76436-3182">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3183">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3183">Checksum</span></span>

<span data-ttu-id="76436-3184">없음</span><span class="sxs-lookup"><span data-stu-id="76436-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3185">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3185">Definition</span></span>

<span data-ttu-id="76436-3186">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3186">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3187">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3187">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3188">Keyword_uk_nino의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3188">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="76436-3189">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3190">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3190">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3191">Keyword_uk_nino의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3191">No keyword from Keyword_uk_nino is found.</span></span>

```
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3192">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3192">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="76436-3193">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="76436-3193">Keyword_uk_nino</span></span>

- <span data-ttu-id="76436-3194">national insurance number
</span><span class="sxs-lookup"><span data-stu-id="76436-3194">national insurance number</span></span> 
- <span data-ttu-id="76436-3195">national insurance contributions
</span><span class="sxs-lookup"><span data-stu-id="76436-3195">national insurance contributions</span></span> 
- <span data-ttu-id="76436-3196">protection act
</span><span class="sxs-lookup"><span data-stu-id="76436-3196">protection act</span></span> 
- <span data-ttu-id="76436-3197">insurance
</span><span class="sxs-lookup"><span data-stu-id="76436-3197">insurance</span></span> 
- <span data-ttu-id="76436-3198">social security number
</span><span class="sxs-lookup"><span data-stu-id="76436-3198">social security number</span></span> 
- <span data-ttu-id="76436-3199">insurance application
</span><span class="sxs-lookup"><span data-stu-id="76436-3199">insurance application</span></span> 
- <span data-ttu-id="76436-3200">medical application
</span><span class="sxs-lookup"><span data-stu-id="76436-3200">medical application</span></span> 
- <span data-ttu-id="76436-3201">social insurance
</span><span class="sxs-lookup"><span data-stu-id="76436-3201">social insurance</span></span> 
- <span data-ttu-id="76436-3202">medical attention
</span><span class="sxs-lookup"><span data-stu-id="76436-3202">medical attention</span></span> 
- <span data-ttu-id="76436-3203">소셜 보안</span><span class="sxs-lookup"><span data-stu-id="76436-3203">social security</span></span> 
- <span data-ttu-id="76436-3204">great britain
</span><span class="sxs-lookup"><span data-stu-id="76436-3204">great britain</span></span> 
- <span data-ttu-id="76436-3205">insurance
</span><span class="sxs-lookup"><span data-stu-id="76436-3205">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="76436-p145">미국/영국 여권 번호</span><span class="sxs-lookup"><span data-stu-id="76436-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-3208">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3208">Format</span></span>

<span data-ttu-id="76436-3209">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3209">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3210">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3210">Pattern</span></span>

<span data-ttu-id="76436-3211">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3211">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3212">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3212">Checksum</span></span>

<span data-ttu-id="76436-3213">없음</span><span class="sxs-lookup"><span data-stu-id="76436-3213">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3214">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3214">Definition</span></span>

<span data-ttu-id="76436-3215">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3215">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3216">Func_usa_uk_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3216">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3217">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3217">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3218">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3218">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="76436-3219">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="76436-3219">Keyword_passport</span></span>

- <span data-ttu-id="76436-3220">Passport Number</span><span class="sxs-lookup"><span data-stu-id="76436-3220">Passport Number</span></span> 
- <span data-ttu-id="76436-3221">
Passport No</span><span class="sxs-lookup"><span data-stu-id="76436-3221">Passport No</span></span> 
- <span data-ttu-id="76436-3222">Passport #
</span><span class="sxs-lookup"><span data-stu-id="76436-3222">Passport #</span></span> 
- <span data-ttu-id="76436-3223">Passport#
</span><span class="sxs-lookup"><span data-stu-id="76436-3223">Passport#</span></span> 
- <span data-ttu-id="76436-3224">PassportID</span><span class="sxs-lookup"><span data-stu-id="76436-3224">PassportID</span></span> 
- <span data-ttu-id="76436-3225">Passportno
</span><span class="sxs-lookup"><span data-stu-id="76436-3225">Passportno</span></span> 
- <span data-ttu-id="76436-3226">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="76436-3226">passportnumber</span></span> 
- <span data-ttu-id="76436-3227">パスポート</span><span class="sxs-lookup"><span data-stu-id="76436-3227">パスポート</span></span> 
- <span data-ttu-id="76436-3228">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="76436-3228">パスポート番号</span></span> 
- <span data-ttu-id="76436-3229">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="76436-3229">パスポートのNum</span></span> 
- <span data-ttu-id="76436-3230">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="76436-3230">パスポート＃</span></span> 
- <span data-ttu-id="76436-3231">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="76436-3231">Numéro de passeport</span></span> 
- <span data-ttu-id="76436-3232">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="76436-3232">Passeport n °</span></span> 
- <span data-ttu-id="76436-3233">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="76436-3233">Passeport Non</span></span> 
- <span data-ttu-id="76436-3234">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="76436-3234">Passeport #</span></span> 
- <span data-ttu-id="76436-3235">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="76436-3235">Passeport#</span></span> 
- <span data-ttu-id="76436-3236">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="76436-3236">PasseportNon</span></span> 
- <span data-ttu-id="76436-3237">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="76436-3237">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="76436-3238">미국 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="76436-3238">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-3239">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3239">Format</span></span>

<span data-ttu-id="76436-3240">8-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3240">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3241">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3241">Pattern</span></span>

<span data-ttu-id="76436-3242">8-17자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3242">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3243">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3243">Checksum</span></span>

<span data-ttu-id="76436-3244">없음</span><span class="sxs-lookup"><span data-stu-id="76436-3244">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3245">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3245">Definition</span></span>

<span data-ttu-id="76436-3246">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3247">Regex_usa_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3247">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3248">Keyword_usa_Bank_Account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3248">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3249">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3249">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="76436-3250">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="76436-3250">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="76436-3251">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-3251">Checking Account Number</span></span> 
- <span data-ttu-id="76436-3252">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="76436-3252">Checking Account</span></span> 
- <span data-ttu-id="76436-3253">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="76436-3253">Checking Account #</span></span> 
- <span data-ttu-id="76436-3254">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="76436-3254">Checking Acct Number</span></span> 
- <span data-ttu-id="76436-3255">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="76436-3255">Checking Acct #</span></span> 
- <span data-ttu-id="76436-3256">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="76436-3256">Checking Acct No.</span></span> 
- <span data-ttu-id="76436-3257">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="76436-3257">Checking Account No.</span></span> 
- <span data-ttu-id="76436-3258">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-3258">Bank Account Number</span></span> 
- <span data-ttu-id="76436-3259">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="76436-3259">Bank Account #</span></span> 
- <span data-ttu-id="76436-3260">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="76436-3260">Bank Acct Number</span></span> 
- <span data-ttu-id="76436-3261">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="76436-3261">Bank Acct #</span></span> 
- <span data-ttu-id="76436-3262">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="76436-3262">Bank Acct No.</span></span> 
- <span data-ttu-id="76436-3263">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="76436-3263">Bank Account No.</span></span> 
- <span data-ttu-id="76436-3264">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-3264">Savings Account Number</span></span> 
- <span data-ttu-id="76436-3265">Savings Account.
</span><span class="sxs-lookup"><span data-stu-id="76436-3265">Savings Account.</span></span> 
- <span data-ttu-id="76436-3266">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="76436-3266">Savings Account #</span></span> 
- <span data-ttu-id="76436-3267">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="76436-3267">Savings Acct Number</span></span> 
- <span data-ttu-id="76436-3268">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="76436-3268">Savings Acct #</span></span> 
- <span data-ttu-id="76436-3269">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="76436-3269">Savings Acct No.</span></span> 
- <span data-ttu-id="76436-3270">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="76436-3270">Savings Account No.</span></span> 
- <span data-ttu-id="76436-3271">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="76436-3271">Debit Account Number</span></span> 
- <span data-ttu-id="76436-3272">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="76436-3272">Debit Account</span></span> 
- <span data-ttu-id="76436-3273">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="76436-3273">Debit Account #</span></span> 
- <span data-ttu-id="76436-3274">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="76436-3274">Debit Acct Number</span></span> 
- <span data-ttu-id="76436-3275">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="76436-3275">Debit Acct #</span></span> 
- <span data-ttu-id="76436-3276">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="76436-3276">Debit Acct No.</span></span> 
- <span data-ttu-id="76436-3277">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="76436-3277">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="76436-3278">미국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="76436-3278">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="76436-3279">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3279">Format</span></span>

<span data-ttu-id="76436-3280">주마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3280">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3281">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3281">Pattern</span></span>

<span data-ttu-id="76436-3282">주마다 다릅니다(예: 뉴욕).</span><span class="sxs-lookup"><span data-stu-id="76436-3282">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="76436-3283">ddd ddd ddd와 같이 9 자리 숫자는 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3283">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="76436-3284">ddddddddd와 같은 9 자리 숫자가 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3284">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3285">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3285">Checksum</span></span>

<span data-ttu-id="76436-3286">없음</span><span class="sxs-lookup"><span data-stu-id="76436-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3287">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3287">Definition</span></span>

<span data-ttu-id="76436-3288">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3289">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3289">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3290">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3290">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="76436-3291">Keyword_us_drivers_license에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3291">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="76436-3292">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3292">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3293">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3293">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3294">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3294">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="76436-3295">Keyword_us_drivers_license_abbreviations의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3295">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="76436-3296">Keyword_us_drivers_license의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3296">No keyword from Keyword_us_drivers_license is found.</span></span>

```
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
```

### <a name="keywords"></a><span data-ttu-id="76436-3297">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3297">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="76436-3298">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="76436-3298">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="76436-3299">DL</span><span class="sxs-lookup"><span data-stu-id="76436-3299">DL</span></span> 
- <span data-ttu-id="76436-3300">DLS</span><span class="sxs-lookup"><span data-stu-id="76436-3300">DLS</span></span> 
- <span data-ttu-id="76436-3301">cdl</span><span class="sxs-lookup"><span data-stu-id="76436-3301">CDL</span></span> 
- <span data-ttu-id="76436-3302">cdls</span><span class="sxs-lookup"><span data-stu-id="76436-3302">CDLS</span></span> 
- <span data-ttu-id="76436-3303">ID</span><span class="sxs-lookup"><span data-stu-id="76436-3303">ID</span></span> 
- <span data-ttu-id="76436-3304">번호가</span><span class="sxs-lookup"><span data-stu-id="76436-3304">IDs</span></span> 
- <span data-ttu-id="76436-3305">DL#</span><span class="sxs-lookup"><span data-stu-id="76436-3305">DL#</span></span> 
- <span data-ttu-id="76436-3306">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="76436-3306">DLS#</span></span> 
- <span data-ttu-id="76436-3307">CDL#
</span><span class="sxs-lookup"><span data-stu-id="76436-3307">CDL#</span></span> 
- <span data-ttu-id="76436-3308">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="76436-3308">CDLS#</span></span> 
- <span data-ttu-id="76436-3309">ID#</span><span class="sxs-lookup"><span data-stu-id="76436-3309">ID#</span></span>
- <span data-ttu-id="76436-3310">
IDs#
</span><span class="sxs-lookup"><span data-stu-id="76436-3310">IDs#</span></span> 
- <span data-ttu-id="76436-3311">ID 번호</span><span class="sxs-lookup"><span data-stu-id="76436-3311">ID number</span></span> 
- <span data-ttu-id="76436-3312">ID numbers
</span><span class="sxs-lookup"><span data-stu-id="76436-3312">ID numbers</span></span> 
- <span data-ttu-id="76436-3313">LIC</span><span class="sxs-lookup"><span data-stu-id="76436-3313">LIC</span></span> 
- <span data-ttu-id="76436-3314">LIC#
</span><span class="sxs-lookup"><span data-stu-id="76436-3314">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="76436-3315">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="76436-3315">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="76436-3316">driverlic</span><span class="sxs-lookup"><span data-stu-id="76436-3316">DriverLic</span></span> 
- <span data-ttu-id="76436-3317">driverlics</span><span class="sxs-lookup"><span data-stu-id="76436-3317">DriverLics</span></span> 
- <span data-ttu-id="76436-3318">driverlicense</span><span class="sxs-lookup"><span data-stu-id="76436-3318">DriverLicense</span></span> 
- <span data-ttu-id="76436-3319">driverlicenses</span><span class="sxs-lookup"><span data-stu-id="76436-3319">DriverLicenses</span></span> 
- <span data-ttu-id="76436-3320">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="76436-3320">Driver Lic</span></span> 
- <span data-ttu-id="76436-3321">드라이버 lics</span><span class="sxs-lookup"><span data-stu-id="76436-3321">Driver Lics</span></span> 
- <span data-ttu-id="76436-3322">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-3322">Driver License</span></span> 
- <span data-ttu-id="76436-3323">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-3323">Driver Licenses</span></span> 
- <span data-ttu-id="76436-3324">DriversLic</span><span class="sxs-lookup"><span data-stu-id="76436-3324">DriversLic</span></span> 
- <span data-ttu-id="76436-3325">driverslics</span><span class="sxs-lookup"><span data-stu-id="76436-3325">DriversLics</span></span> 
- <span data-ttu-id="76436-3326">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-3326">DriversLicense</span></span> 
- <span data-ttu-id="76436-3327">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-3327">DriversLicenses</span></span> 
- <span data-ttu-id="76436-3328">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="76436-3328">Drivers Lic</span></span> 
- <span data-ttu-id="76436-3329">드라이버 lics</span><span class="sxs-lookup"><span data-stu-id="76436-3329">Drivers Lics</span></span> 
- <span data-ttu-id="76436-3330">Drivers License</span><span class="sxs-lookup"><span data-stu-id="76436-3330">Drivers License</span></span> 
- <span data-ttu-id="76436-3331">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-3331">Drivers Licenses</span></span> 
- <span data-ttu-id="76436-3332">driver' Lic</span><span class="sxs-lookup"><span data-stu-id="76436-3332">Driver'Lic</span></span> 
- <span data-ttu-id="76436-3333">driver'lics</span><span class="sxs-lookup"><span data-stu-id="76436-3333">Driver'Lics</span></span> 
- <span data-ttu-id="76436-3334">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="76436-3334">Driver'License</span></span> 
- <span data-ttu-id="76436-3335">driver'licenses</span><span class="sxs-lookup"><span data-stu-id="76436-3335">Driver'Licenses</span></span> 
- <span data-ttu-id="76436-3336">드라이버 ' Lic</span><span class="sxs-lookup"><span data-stu-id="76436-3336">Driver' Lic</span></span> 
- <span data-ttu-id="76436-3337">드라이버의 lics</span><span class="sxs-lookup"><span data-stu-id="76436-3337">Driver' Lics</span></span> 
- <span data-ttu-id="76436-3338">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-3338">Driver' License</span></span> 
- <span data-ttu-id="76436-3339">운전 면허증</span><span class="sxs-lookup"><span data-stu-id="76436-3339">Driver' Licenses</span></span>
- <span data-ttu-id="76436-3340">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="76436-3340">Driver'sLic</span></span> 
- <span data-ttu-id="76436-3341">drivers (slics)</span><span class="sxs-lookup"><span data-stu-id="76436-3341">Driver'sLics</span></span> 
- <span data-ttu-id="76436-3342">driver'slicense</span><span class="sxs-lookup"><span data-stu-id="76436-3342">Driver'sLicense</span></span> 
- <span data-ttu-id="76436-3343">driver'slicenses</span><span class="sxs-lookup"><span data-stu-id="76436-3343">Driver'sLicenses</span></span> 
- <span data-ttu-id="76436-3344">드라이버의 Lic</span><span class="sxs-lookup"><span data-stu-id="76436-3344">Driver's Lic</span></span> 
- <span data-ttu-id="76436-3345">운전 lics</span><span class="sxs-lookup"><span data-stu-id="76436-3345">Driver's Lics</span></span> 
- <span data-ttu-id="76436-3346">운전 면허</span><span class="sxs-lookup"><span data-stu-id="76436-3346">Driver's License</span></span> 
- <span data-ttu-id="76436-3347">운전 면허증</span><span class="sxs-lookup"><span data-stu-id="76436-3347">Driver's Licenses</span></span> 
- <span data-ttu-id="76436-3348">identification number
</span><span class="sxs-lookup"><span data-stu-id="76436-3348">identification number</span></span> 
- <span data-ttu-id="76436-3349">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="76436-3349">identification numbers</span></span> 
- <span data-ttu-id="76436-3350">identification #
</span><span class="sxs-lookup"><span data-stu-id="76436-3350">identification #</span></span> 
- <span data-ttu-id="76436-3351">id 카드</span><span class="sxs-lookup"><span data-stu-id="76436-3351">id card</span></span> 
- <span data-ttu-id="76436-3352">id 카드</span><span class="sxs-lookup"><span data-stu-id="76436-3352">id cards</span></span> 
- <span data-ttu-id="76436-3353">식별 카드</span><span class="sxs-lookup"><span data-stu-id="76436-3353">identification card</span></span> 
- <span data-ttu-id="76436-3354">식별 카드</span><span class="sxs-lookup"><span data-stu-id="76436-3354">identification cards</span></span> 
- <span data-ttu-id="76436-3355">driverlic #</span><span class="sxs-lookup"><span data-stu-id="76436-3355">DriverLic#</span></span> 
- <span data-ttu-id="76436-3356">driverlics #</span><span class="sxs-lookup"><span data-stu-id="76436-3356">DriverLics#</span></span> 
- <span data-ttu-id="76436-3357">driverlicense #</span><span class="sxs-lookup"><span data-stu-id="76436-3357">DriverLicense#</span></span> 
- <span data-ttu-id="76436-3358">driverlicenses #</span><span class="sxs-lookup"><span data-stu-id="76436-3358">DriverLicenses#</span></span> 
- <span data-ttu-id="76436-3359">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="76436-3359">Driver Lic#</span></span> 
- <span data-ttu-id="76436-3360">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-3360">Driver Lics#</span></span> 
- <span data-ttu-id="76436-3361">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-3361">Driver License#</span></span> 
- <span data-ttu-id="76436-3362">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-3362">Driver Licenses#</span></span> 
- <span data-ttu-id="76436-3363">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="76436-3363">DriversLic#</span></span> 
- <span data-ttu-id="76436-3364">driverslics #</span><span class="sxs-lookup"><span data-stu-id="76436-3364">DriversLics#</span></span> 
- <span data-ttu-id="76436-3365">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-3365">DriversLicense#</span></span> 
- <span data-ttu-id="76436-3366">드라이버 라이선스 수</span><span class="sxs-lookup"><span data-stu-id="76436-3366">DriversLicenses#</span></span> 
- <span data-ttu-id="76436-3367">Drivers Lic #</span><span class="sxs-lookup"><span data-stu-id="76436-3367">Drivers Lic#</span></span> 
- <span data-ttu-id="76436-3368">드라이버 lics #</span><span class="sxs-lookup"><span data-stu-id="76436-3368">Drivers Lics#</span></span> 
- <span data-ttu-id="76436-3369">Drivers License #</span><span class="sxs-lookup"><span data-stu-id="76436-3369">Drivers License#</span></span> 
- <span data-ttu-id="76436-3370">Drivers 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="76436-3370">Drivers Licenses#</span></span> 
- <span data-ttu-id="76436-3371">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-3371">Driver'Lic#</span></span> 
- <span data-ttu-id="76436-3372">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-3372">Driver'Lics#</span></span> 
- <span data-ttu-id="76436-3373">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="76436-3373">Driver'License#</span></span> 
- <span data-ttu-id="76436-3374">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="76436-3374">Driver'Licenses#</span></span> 
- <span data-ttu-id="76436-3375">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-3375">Driver' Lic#</span></span> 
- <span data-ttu-id="76436-3376">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-3376">Driver' Lics#</span></span> 
- <span data-ttu-id="76436-3377">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="76436-3377">Driver' License#</span></span> 
- <span data-ttu-id="76436-3378">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="76436-3378">Driver' Licenses#</span></span> 
- <span data-ttu-id="76436-3379">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="76436-3379">Driver'sLic#</span></span> 
- <span data-ttu-id="76436-3380">drivers (slics #)</span><span class="sxs-lookup"><span data-stu-id="76436-3380">Driver'sLics#</span></span> 
- <span data-ttu-id="76436-3381">driver'slicense #</span><span class="sxs-lookup"><span data-stu-id="76436-3381">Driver'sLicense#</span></span> 
- <span data-ttu-id="76436-3382">driver'slicenses #</span><span class="sxs-lookup"><span data-stu-id="76436-3382">Driver'sLicenses#</span></span> 
- <span data-ttu-id="76436-3383">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="76436-3383">Driver's Lic#</span></span> 
- <span data-ttu-id="76436-3384">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="76436-3384">Driver's Lics#</span></span> 
- <span data-ttu-id="76436-3385">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="76436-3385">Driver's License#</span></span> 
- <span data-ttu-id="76436-3386">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="76436-3386">Driver's Licenses#</span></span> 
- <span data-ttu-id="76436-3387">id 카드 #</span><span class="sxs-lookup"><span data-stu-id="76436-3387">id card#</span></span> 
- <span data-ttu-id="76436-3388">id cards#
</span><span class="sxs-lookup"><span data-stu-id="76436-3388">id cards#</span></span> 
- <span data-ttu-id="76436-3389">identification card#
</span><span class="sxs-lookup"><span data-stu-id="76436-3389">identification card#</span></span> 
- <span data-ttu-id="76436-3390">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="76436-3390">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="76436-3391">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="76436-3391">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="76436-3392">주 약어(예: "NY")
</span><span class="sxs-lookup"><span data-stu-id="76436-3392">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="76436-3393">주 이름(예: "New York")
</span><span class="sxs-lookup"><span data-stu-id="76436-3393">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="76436-3394">미국 ITIN(개인 납세자 번호)</span><span class="sxs-lookup"><span data-stu-id="76436-3394">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="76436-3395">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3395">Format</span></span>

<span data-ttu-id="76436-3396">"9"로 시작되고, "7" 또는 "8"을 4번째 숫자로 포함하고, 경우에 따라 공백이나 대시로 서식이 지정된 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3396">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3397">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3397">Pattern</span></span>

<span data-ttu-id="76436-3398">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="76436-3398">Formatted:</span></span>
- <span data-ttu-id="76436-3399">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3399">The digit "9"</span></span> 
- <span data-ttu-id="76436-3400">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3400">Two digits</span></span> 
- <span data-ttu-id="76436-3401">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="76436-3401">A space or dash</span></span> 
- <span data-ttu-id="76436-3402">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="76436-3402">A "7" or "8"</span></span> 
- <span data-ttu-id="76436-3403">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3403">A digit</span></span> 
- <span data-ttu-id="76436-3404">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="76436-3404">A space, or dash</span></span> 
- <span data-ttu-id="76436-3405">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3405">Four digits</span></span>

<span data-ttu-id="76436-3406">서식 없음:</span><span class="sxs-lookup"><span data-stu-id="76436-3406">Unformatted:</span></span>
- <span data-ttu-id="76436-3407">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3407">The digit "9"</span></span> 
- <span data-ttu-id="76436-3408">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3408">Two digits</span></span> 
- <span data-ttu-id="76436-3409">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="76436-3409">A "7" or "8"</span></span> 
- <span data-ttu-id="76436-3410">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3410">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3411">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3411">Checksum</span></span>

<span data-ttu-id="76436-3412">없음</span><span class="sxs-lookup"><span data-stu-id="76436-3412">No</span></span>

### <a name="definition"></a><span data-ttu-id="76436-3413">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3413">Definition</span></span>

<span data-ttu-id="76436-3414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3415">Func_formatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3415">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3416">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3416">At least one of the following is true:</span></span>
    - <span data-ttu-id="76436-3417">Keyword_itin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3417">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="76436-3418">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3418">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="76436-3419">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3419">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="76436-3420">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3420">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="76436-3421">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3421">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3422">Func_unformatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3422">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3423">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3423">At least one of the following is true:</span></span>
    - <span data-ttu-id="76436-3424">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3424">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="76436-3425">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3425">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="76436-3426">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3426">The function Func_us_date finds a date in the right date format.</span></span>

```
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3427">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3427">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="76436-3428">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="76436-3428">Keyword_itin</span></span>

- <span data-ttu-id="76436-3429">taxpayer
</span><span class="sxs-lookup"><span data-stu-id="76436-3429">taxpayer</span></span> 
- <span data-ttu-id="76436-3430">tax id
</span><span class="sxs-lookup"><span data-stu-id="76436-3430">tax id</span></span> 
- <span data-ttu-id="76436-3431">tax identification
</span><span class="sxs-lookup"><span data-stu-id="76436-3431">tax identification</span></span> 
- <span data-ttu-id="76436-3432">itin
</span><span class="sxs-lookup"><span data-stu-id="76436-3432">itin</span></span> 
- <span data-ttu-id="76436-3433">ssn</span><span class="sxs-lookup"><span data-stu-id="76436-3433">ssn</span></span> 
- <span data-ttu-id="76436-3434">tin
</span><span class="sxs-lookup"><span data-stu-id="76436-3434">tin</span></span> 
- <span data-ttu-id="76436-3435">소셜 보안</span><span class="sxs-lookup"><span data-stu-id="76436-3435">social security</span></span> 
- <span data-ttu-id="76436-3436">tax payer
</span><span class="sxs-lookup"><span data-stu-id="76436-3436">tax payer</span></span> 
- <span data-ttu-id="76436-3437">itins
</span><span class="sxs-lookup"><span data-stu-id="76436-3437">itins</span></span> 
- <span data-ttu-id="76436-3438">taxid

</span><span class="sxs-lookup"><span data-stu-id="76436-3438">taxid</span></span> 
- <span data-ttu-id="76436-3439">individual taxpayer
</span><span class="sxs-lookup"><span data-stu-id="76436-3439">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="76436-3440">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="76436-3440">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="76436-3441">License</span><span class="sxs-lookup"><span data-stu-id="76436-3441">License</span></span> 
- <span data-ttu-id="76436-3442">DL</span><span class="sxs-lookup"><span data-stu-id="76436-3442">DL</span></span> 
- <span data-ttu-id="76436-3443">DOB
</span><span class="sxs-lookup"><span data-stu-id="76436-3443">DOB</span></span> 
- <span data-ttu-id="76436-3444">생년월일</span><span class="sxs-lookup"><span data-stu-id="76436-3444">Birthdate</span></span> 
- <span data-ttu-id="76436-3445">생일 </span><span class="sxs-lookup"><span data-stu-id="76436-3445">Birthday</span></span> 
- <span data-ttu-id="76436-3446">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="76436-3446">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="76436-3447">미국 SSN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="76436-3447">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="76436-3448">형식</span><span class="sxs-lookup"><span data-stu-id="76436-3448">Format</span></span>

<span data-ttu-id="76436-3449">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="76436-3449">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="76436-3450">mid가 2011 이전에 실행 된 경우 SSN은 특정 범위 내에서 번호의 특정 부분이 유효한 지 확인 하는 강력한 서식을 사용 해야 하지만 검사 값은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3450">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="76436-3451">패턴</span><span class="sxs-lookup"><span data-stu-id="76436-3451">Pattern</span></span>

<span data-ttu-id="76436-3452">다음의 네 가지 패턴에서 ssns를 검색 하는 함수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3452">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="76436-3453">Func_ssn는 대시 또는 공백을 사용 하 여 서식이 지정 된 2011 이전의 고급 서식 (ddd-dd-dddd 또는 ddd dd dd)을 사용 하 여 ssns를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3453">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="76436-3454">Func_unformatted_ssn는 형식이 지정 되지 않은 2011 이전 형식으로 서식이 지정 된 ssns를 찾습니다 (ddddddddd).</span><span class="sxs-lookup"><span data-stu-id="76436-3454">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="76436-3455">Func_randomized_formatted_ssn는 대시 또는 공백으로 서식이 지정 된 post-2011 ssns를 찾습니다 (ddd-dd-dddd 또는 ddd dd dddd).</span><span class="sxs-lookup"><span data-stu-id="76436-3455">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="76436-3456">Func_randomized_unformatted_ssn는 형식 없는 2011 ssns를 찾고, 서식이 없는 9 자리 숫자 (ddddddddd)를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3456">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="76436-3457">체크섬</span><span class="sxs-lookup"><span data-stu-id="76436-3457">Checksum</span></span>

<span data-ttu-id="76436-3458">없음</span><span class="sxs-lookup"><span data-stu-id="76436-3458">No</span></span>


### <a name="definition"></a><span data-ttu-id="76436-3459">정의</span><span class="sxs-lookup"><span data-stu-id="76436-3459">Definition</span></span>

<span data-ttu-id="76436-3460">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3461">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3461">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3462">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3462">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="76436-3463">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3464">Func_unformatted_ssn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3464">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3465">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3465">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="76436-3466">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3467">Func_randomized_formatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3467">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3468">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3468">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="76436-3469">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3469">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="76436-3470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 55% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3470">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="76436-3471">Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3471">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="76436-3472">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3472">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="76436-3473">Func_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76436-3473">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

```
<!-- U.S. Social Security Number (SSN) -->
    <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="76436-3474">키워드</span><span class="sxs-lookup"><span data-stu-id="76436-3474">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="76436-3475">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="76436-3475">Keyword_ssn</span></span>

- <span data-ttu-id="76436-3476">Social Security
</span><span class="sxs-lookup"><span data-stu-id="76436-3476">Social Security</span></span> 
- <span data-ttu-id="76436-3477">Social Security#
</span><span class="sxs-lookup"><span data-stu-id="76436-3477">Social Security#</span></span> 
- <span data-ttu-id="76436-3478">Soc Sec
</span><span class="sxs-lookup"><span data-stu-id="76436-3478">Soc Sec</span></span> 
- <span data-ttu-id="76436-3479">SSN</span><span class="sxs-lookup"><span data-stu-id="76436-3479">SSN</span></span> 
- <span data-ttu-id="76436-3480">SSNS
</span><span class="sxs-lookup"><span data-stu-id="76436-3480">SSNS</span></span> 
- <span data-ttu-id="76436-3481">SSN#
</span><span class="sxs-lookup"><span data-stu-id="76436-3481">SSN#</span></span> 
- <span data-ttu-id="76436-3482">SS#
</span><span class="sxs-lookup"><span data-stu-id="76436-3482">SS#</span></span> 
- <span data-ttu-id="76436-3483">SSID
</span><span class="sxs-lookup"><span data-stu-id="76436-3483">SSID</span></span> 
   

