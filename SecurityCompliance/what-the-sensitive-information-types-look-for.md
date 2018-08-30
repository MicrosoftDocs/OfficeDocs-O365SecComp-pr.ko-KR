---
title: 중요 한 정보 형식을 찾습니다.
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Office 365 보안에서 데이터 손실 방지 (DLP) &amp; 준수 센터 DLP 정책에서 사용 하 여 사용할 수 있는 80 중요 한 정보 유형을 포함 합니다. 이 항목 모두 이러한 중요 한 정보 유형 및 각 종류를 감지 하는 경우의 DLP 정책을 찾아 나와 있습니다.
ms.openlocfilehash: 064606085363ba9de972511642993277451c8ce3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533872"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="c5035-104">중요 한 정보 형식을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-104">What the sensitive information types look for</span></span>

<span data-ttu-id="c5035-p102">Office 365 보안에서 데이터 손실 방지 (DLP) &amp; 준수 센터 DLP 정책에서 사용 하 여 사용할 수 있는 많은 중요 한 정보 유형을 포함 합니다. 이 항목 모두 이러한 중요 한 정보 유형 및 각 종류를 감지 하는 경우의 DLP 정책을 찾아 나와 있습니다. 중요 한 정보 유형 정규식 또는 함수를 식별할 수 있는 패턴에 의해 정의 됩니다. 또한 확증 적 인증 거 키워드 및 체크섬와 같은 중요 한 정보 형식을 식별 하기 위해 사용할 수 있습니다. 신뢰 수준 및 근접성 평가 프로세스에도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="c5035-110">ABA 라우팅 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-111">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-111">Format</span></span>

<span data-ttu-id="c5035-112">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-113">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-113">Pattern</span></span>

<span data-ttu-id="c5035-114">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="c5035-114">Formatted:</span></span>
- <span data-ttu-id="c5035-115">0, 1, 2, 3, 6, 7 또는 8로 시작하는 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="c5035-116">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-116">A hyphen</span></span>
- <span data-ttu-id="c5035-117">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-117">Four digits</span></span>
- <span data-ttu-id="c5035-118">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-118">A hyphen</span></span>
- <span data-ttu-id="c5035-119">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-119">A digit</span></span>

<span data-ttu-id="c5035-120">포맷 되지 않음: 9 연속 되는 숫자 0, 1, 2, 3, 6, 7 또는 8로 시작</span><span class="sxs-lookup"><span data-stu-id="c5035-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="c5035-121">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-121">Checksum</span></span>

<span data-ttu-id="c5035-122">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-123">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-123">Definition</span></span>

<span data-ttu-id="c5035-124">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-125">Func_aba_routing 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-126">Keyword_ABA_Routing의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="c5035-127">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="c5035-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="c5035-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="c5035-129">aba</span><span class="sxs-lookup"><span data-stu-id="c5035-129">aba</span></span>
- <span data-ttu-id="c5035-130">
aba #</span><span class="sxs-lookup"><span data-stu-id="c5035-130">aba #</span></span>
- <span data-ttu-id="c5035-131">
aba routing #</span><span class="sxs-lookup"><span data-stu-id="c5035-131">aba routing #</span></span>
- <span data-ttu-id="c5035-132">
aba routing number</span><span class="sxs-lookup"><span data-stu-id="c5035-132">aba routing number</span></span>
- <span data-ttu-id="c5035-133">
aba #</span><span class="sxs-lookup"><span data-stu-id="c5035-133">aba#</span></span>
- <span data-ttu-id="c5035-134">
abarouting#</span><span class="sxs-lookup"><span data-stu-id="c5035-134">abarouting#</span></span>
- <span data-ttu-id="c5035-135">
aba number</span><span class="sxs-lookup"><span data-stu-id="c5035-135">aba number</span></span>
- <span data-ttu-id="c5035-136">
abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="c5035-136">abaroutingnumber</span></span>
- <span data-ttu-id="c5035-137">
american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="c5035-137">american bank association routing #</span></span>
- <span data-ttu-id="c5035-138">
american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="c5035-138">american bank association routing number</span></span>
- <span data-ttu-id="c5035-139">
americanbankassociationrouting#</span><span class="sxs-lookup"><span data-stu-id="c5035-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="c5035-140">
americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="c5035-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="c5035-141">
bank routing number</span><span class="sxs-lookup"><span data-stu-id="c5035-141">bank routing number</span></span>
- <span data-ttu-id="c5035-142">
bankrouting#</span><span class="sxs-lookup"><span data-stu-id="c5035-142">bankrouting#</span></span>
- <span data-ttu-id="c5035-143">
bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="c5035-143">bankroutingnumber</span></span>
- <span data-ttu-id="c5035-144">
routing transit number</span><span class="sxs-lookup"><span data-stu-id="c5035-144">routing transit number</span></span>
- <span data-ttu-id="c5035-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="c5035-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="c5035-146">아르헨티나 국가 ID(DNI) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-147">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-147">Format</span></span>

<span data-ttu-id="c5035-148">마침표로 구분된 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-149">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-149">Pattern</span></span>

<span data-ttu-id="c5035-150">8자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-150">Eight digits:</span></span>
- <span data-ttu-id="c5035-151">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-151">Two digits</span></span>
- <span data-ttu-id="c5035-152">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-152">A period</span></span>
- <span data-ttu-id="c5035-153">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-153">Three digits</span></span>
- <span data-ttu-id="c5035-154">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-154">A period</span></span>
- <span data-ttu-id="c5035-155">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-156">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-156">Checksum</span></span>

<span data-ttu-id="c5035-157">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-158">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-158">Definition</span></span>

<span data-ttu-id="c5035-159">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-160">Regex_argentina_national_id 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-161">Keyword_argentina_national_id에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-162">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="c5035-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="c5035-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="c5035-164">Argentina National Identity number
</span><span class="sxs-lookup"><span data-stu-id="c5035-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="c5035-165">ID</span><span class="sxs-lookup"><span data-stu-id="c5035-165">Identity</span></span> 
- <span data-ttu-id="c5035-166">식별 국가 Id 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="c5035-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="c5035-167">DNI</span></span> 
- <span data-ttu-id="c5035-168">사용자의 NIC 국가 레지스트리</span><span class="sxs-lookup"><span data-stu-id="c5035-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="c5035-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="c5035-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="c5035-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="c5035-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="c5035-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="c5035-171">Identidad</span></span> 
- <span data-ttu-id="c5035-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="c5035-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="c5035-173">호주 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-174">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-174">Format</span></span>

<span data-ttu-id="c5035-175">6-10자리 숫자(은행 지점 번호 포함 또는 제외)</span><span class="sxs-lookup"><span data-stu-id="c5035-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-176">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-176">Pattern</span></span>

<span data-ttu-id="c5035-p103">계좌 번호는 6-10 자리의입니다. 호주 은행 상태 분기 번호:</span><span class="sxs-lookup"><span data-stu-id="c5035-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="c5035-179">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-179">Three digits</span></span> 
- <span data-ttu-id="c5035-180">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-180">A hyphen</span></span> 
- <span data-ttu-id="c5035-181">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-182">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-182">Checksum</span></span>

<span data-ttu-id="c5035-183">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-184">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-184">Definition</span></span>

<span data-ttu-id="c5035-185">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-186">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="c5035-187">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="c5035-188">Regex_australia_bank_account_number_bsb 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="c5035-189">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-190">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="c5035-191">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-192">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="c5035-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="c5035-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="c5035-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="c5035-194">swift bank code</span></span>
- <span data-ttu-id="c5035-195">
correspondent bank</span><span class="sxs-lookup"><span data-stu-id="c5035-195">correspondent bank</span></span>
- <span data-ttu-id="c5035-196">
base currency</span><span class="sxs-lookup"><span data-stu-id="c5035-196">base currency</span></span>
- <span data-ttu-id="c5035-197">
usa account</span><span class="sxs-lookup"><span data-stu-id="c5035-197">usa account</span></span>
- <span data-ttu-id="c5035-198">
holder address</span><span class="sxs-lookup"><span data-stu-id="c5035-198">holder address</span></span>
- <span data-ttu-id="c5035-199">
bank address</span><span class="sxs-lookup"><span data-stu-id="c5035-199">bank address</span></span>
- <span data-ttu-id="c5035-200">
information account</span><span class="sxs-lookup"><span data-stu-id="c5035-200">information account</span></span>
- <span data-ttu-id="c5035-201">
fund transfers</span><span class="sxs-lookup"><span data-stu-id="c5035-201">fund transfers</span></span>
- <span data-ttu-id="c5035-202">
bank charges</span><span class="sxs-lookup"><span data-stu-id="c5035-202">bank charges</span></span>
- <span data-ttu-id="c5035-203">
bank details</span><span class="sxs-lookup"><span data-stu-id="c5035-203">bank details</span></span>
- <span data-ttu-id="c5035-204">
banking information</span><span class="sxs-lookup"><span data-stu-id="c5035-204">banking information</span></span>
- <span data-ttu-id="c5035-205">
full names</span><span class="sxs-lookup"><span data-stu-id="c5035-205">full names</span></span>
- <span data-ttu-id="c5035-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="c5035-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="c5035-207">호주 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-208">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-208">Format</span></span>

<span data-ttu-id="c5035-209">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-210">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-210">Pattern</span></span>

<span data-ttu-id="c5035-211">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="c5035-212">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-213">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-213">Two digits</span></span> 
- <span data-ttu-id="c5035-214">5자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="c5035-215">또는</span><span class="sxs-lookup"><span data-stu-id="c5035-215">OR</span></span>

- <span data-ttu-id="c5035-216">1-2개의 선택적 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-217">4-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-217">4-9 digits</span></span>

<span data-ttu-id="c5035-218">또는</span><span class="sxs-lookup"><span data-stu-id="c5035-218">OR</span></span>

- <span data-ttu-id="c5035-219">9자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-220">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-220">Checksum</span></span>

<span data-ttu-id="c5035-221">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-222">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-222">Definition</span></span>

<span data-ttu-id="c5035-223">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-224">Regex_australia_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-225">Keyword_australia_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="c5035-226">Keyword_australia_drivers_license_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-227">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="c5035-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="c5035-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="c5035-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="c5035-229">international driving permits</span></span>
- <span data-ttu-id="c5035-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="c5035-230">australian automobile association</span></span>
- <span data-ttu-id="c5035-231">
sydney nsw</span><span class="sxs-lookup"><span data-stu-id="c5035-231">sydney nsw</span></span>
- <span data-ttu-id="c5035-232">
international driving permit</span><span class="sxs-lookup"><span data-stu-id="c5035-232">international driving permit</span></span>
- <span data-ttu-id="c5035-233">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="c5035-233">DriverLicence</span></span>
- <span data-ttu-id="c5035-234">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="c5035-234">DriverLicences</span></span>
- <span data-ttu-id="c5035-235">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-235">Driver Lic</span></span>
- <span data-ttu-id="c5035-236">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-236">Driver Licence</span></span>
- <span data-ttu-id="c5035-237">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="c5035-237">Driver Licences</span></span>
- <span data-ttu-id="c5035-238">DriversLic</span><span class="sxs-lookup"><span data-stu-id="c5035-238">DriversLic</span></span>
- <span data-ttu-id="c5035-239">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="c5035-239">DriversLicence</span></span>
- <span data-ttu-id="c5035-240">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="c5035-240">DriversLicences</span></span>
- <span data-ttu-id="c5035-241">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-241">Drivers Lic</span></span>
- <span data-ttu-id="c5035-242">드라이버 Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-242">Drivers Lics</span></span>
- <span data-ttu-id="c5035-243">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="c5035-243">Drivers Licence</span></span>
- <span data-ttu-id="c5035-244">드라이버 라이센스</span><span class="sxs-lookup"><span data-stu-id="c5035-244">Drivers Licences</span></span>
- <span data-ttu-id="c5035-245">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-245">Driver'Lic</span></span>
- <span data-ttu-id="c5035-246">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-246">Driver'Lics</span></span>
- <span data-ttu-id="c5035-247">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="c5035-247">Driver'Licence</span></span>
- <span data-ttu-id="c5035-248">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="c5035-248">Driver'Licences</span></span>
- <span data-ttu-id="c5035-249">드라이버 ' Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-249">Driver' Lic</span></span>
- <span data-ttu-id="c5035-250">드라이버 ' Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-250">Driver' Lics</span></span>
- <span data-ttu-id="c5035-251">드라이버 ' 사용권</span><span class="sxs-lookup"><span data-stu-id="c5035-251">Driver' Licence</span></span>
- <span data-ttu-id="c5035-252">드라이버 ' 라이센스</span><span class="sxs-lookup"><span data-stu-id="c5035-252">Driver' Licences</span></span>
- <span data-ttu-id="c5035-253">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="c5035-253">Driver'sLic</span></span>
- <span data-ttu-id="c5035-254">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="c5035-254">Driver'sLics</span></span>
- <span data-ttu-id="c5035-255">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="c5035-255">Driver'sLicence</span></span>
- <span data-ttu-id="c5035-256">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="c5035-256">Driver'sLicences</span></span>
- <span data-ttu-id="c5035-257">드라이버의 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-257">Driver's Lic</span></span>
- <span data-ttu-id="c5035-258">드라이버의 Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-258">Driver's Lics</span></span>
- <span data-ttu-id="c5035-259">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-259">Driver's Licence</span></span>
- <span data-ttu-id="c5035-260">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="c5035-260">Driver's Licences</span></span>
- <span data-ttu-id="c5035-261">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-261">DriverLic#</span></span>
- <span data-ttu-id="c5035-262">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-262">DriverLics#</span></span>
- <span data-ttu-id="c5035-263">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="c5035-263">DriverLicence#</span></span>
- <span data-ttu-id="c5035-264">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="c5035-264">DriverLicences#</span></span>
- <span data-ttu-id="c5035-265">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="c5035-265">Driver Lic#</span></span>
- <span data-ttu-id="c5035-266">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-266">Driver Lics#</span></span>
- <span data-ttu-id="c5035-267">드라이버 사용권 #</span><span class="sxs-lookup"><span data-stu-id="c5035-267">Driver Licence#</span></span>
- <span data-ttu-id="c5035-268">드라이버 라이센스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-268">Driver Licences#</span></span>
- <span data-ttu-id="c5035-269">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-269">DriversLic#</span></span>
- <span data-ttu-id="c5035-270">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-270">DriversLics#</span></span>
- <span data-ttu-id="c5035-271">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="c5035-271">DriversLicence#</span></span>
- <span data-ttu-id="c5035-272">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="c5035-272">DriversLicences#</span></span>
- <span data-ttu-id="c5035-273">드라이버 Lic #</span><span class="sxs-lookup"><span data-stu-id="c5035-273">Drivers Lic#</span></span>
- <span data-ttu-id="c5035-274">드라이버 Lics #</span><span class="sxs-lookup"><span data-stu-id="c5035-274">Drivers Lics#</span></span>
- <span data-ttu-id="c5035-275">드라이버 사용권 #</span><span class="sxs-lookup"><span data-stu-id="c5035-275">Drivers Licence#</span></span>
- <span data-ttu-id="c5035-276">드라이버 라이센스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-276">Drivers Licences#</span></span>
- <span data-ttu-id="c5035-277">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-277">Driver'Lic#</span></span>
- <span data-ttu-id="c5035-278">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-278">Driver'Lics#</span></span>
- <span data-ttu-id="c5035-279">Driver'Licence #
</span><span class="sxs-lookup"><span data-stu-id="c5035-279">Driver'Licence#</span></span>
- <span data-ttu-id="c5035-280">Driver'Licences#
</span><span class="sxs-lookup"><span data-stu-id="c5035-280">Driver'Licences#</span></span>
- <span data-ttu-id="c5035-281">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-281">Driver' Lic#</span></span>
- <span data-ttu-id="c5035-282">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-282">Driver' Lics#</span></span>
- <span data-ttu-id="c5035-283">드라이버 ' 사용권 #</span><span class="sxs-lookup"><span data-stu-id="c5035-283">Driver' Licence#</span></span>
- <span data-ttu-id="c5035-284">드라이버 ' 라이센스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-284">Driver' Licences#</span></span>
- <span data-ttu-id="c5035-285">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-285">Driver'sLic#</span></span>
- <span data-ttu-id="c5035-286">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-286">Driver'sLics#</span></span>
- <span data-ttu-id="c5035-287">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="c5035-287">Driver'sLicence#</span></span>
- <span data-ttu-id="c5035-288">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="c5035-288">Driver'sLicences#</span></span>
- <span data-ttu-id="c5035-289">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-289">Driver's Lic#</span></span>
- <span data-ttu-id="c5035-290">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-290">Driver's Lics#</span></span>
- <span data-ttu-id="c5035-291">드라이버의 사용권 #</span><span class="sxs-lookup"><span data-stu-id="c5035-291">Driver's Licence#</span></span>
- <span data-ttu-id="c5035-292">드라이버의 라이센스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-292">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="c5035-293">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="c5035-293">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="c5035-294">aaa</span><span class="sxs-lookup"><span data-stu-id="c5035-294">aaa</span></span>
- <span data-ttu-id="c5035-295">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-295">DriverLicense</span></span>
- <span data-ttu-id="c5035-296">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-296">DriverLicenses</span></span>
- <span data-ttu-id="c5035-297">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-297">Driver License</span></span>
- <span data-ttu-id="c5035-298">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-298">Driver Licenses</span></span>
- <span data-ttu-id="c5035-299">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-299">DriversLicense</span></span>
- <span data-ttu-id="c5035-300">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-300">DriversLicenses</span></span>
- <span data-ttu-id="c5035-301">운전 면허</span><span class="sxs-lookup"><span data-stu-id="c5035-301">Drivers License</span></span>
- <span data-ttu-id="c5035-302">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-302">Drivers Licenses</span></span>
- <span data-ttu-id="c5035-303">Driver'License</span><span class="sxs-lookup"><span data-stu-id="c5035-303">Driver'License</span></span>
- <span data-ttu-id="c5035-304">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="c5035-304">Driver'Licenses</span></span>
- <span data-ttu-id="c5035-305">드라이버 ' 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-305">Driver' License</span></span>
- <span data-ttu-id="c5035-306">드라이버 ' 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-306">Driver' Licenses</span></span>
- <span data-ttu-id="c5035-307">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-307">Driver'sLicense</span></span>
- <span data-ttu-id="c5035-308">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-308">Driver'sLicenses</span></span>
- <span data-ttu-id="c5035-309">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-309">Driver's License</span></span>
- <span data-ttu-id="c5035-310">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-310">Driver's Licenses</span></span>
- <span data-ttu-id="c5035-311">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-311">DriverLicense#</span></span>
- <span data-ttu-id="c5035-312">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-312">DriverLicenses#</span></span>
- <span data-ttu-id="c5035-313">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-313">Driver License#</span></span>
- <span data-ttu-id="c5035-314">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-314">Driver Licenses#</span></span>
- <span data-ttu-id="c5035-315">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-315">DriversLicense#</span></span>
- <span data-ttu-id="c5035-316">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-316">DriversLicenses#</span></span>
- <span data-ttu-id="c5035-317">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-317">Drivers License#</span></span>
- <span data-ttu-id="c5035-318">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-318">Drivers Licenses#</span></span>
- <span data-ttu-id="c5035-319">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-319">Driver'License#</span></span>
- <span data-ttu-id="c5035-320">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="c5035-320">Driver'Licenses#</span></span>
- <span data-ttu-id="c5035-321">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-321">Driver' License#</span></span>
- <span data-ttu-id="c5035-322">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="c5035-322">Driver' Licenses#</span></span>
- <span data-ttu-id="c5035-323">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-323">Driver'sLicense#</span></span>
- <span data-ttu-id="c5035-324">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-324">Driver'sLicenses#</span></span>
- <span data-ttu-id="c5035-325">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-325">Driver's License#</span></span>
- <span data-ttu-id="c5035-326">

Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="c5035-326">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="c5035-327">호주 의료 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-327">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-328">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-328">Format</span></span>

<span data-ttu-id="c5035-329">10-11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-329">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-330">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-330">Pattern</span></span>

<span data-ttu-id="c5035-331">10-11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-331">10-11 digits:</span></span>
- <span data-ttu-id="c5035-332">첫 번째 숫자는 2-6 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-332">First digit is in the range 2-6</span></span>
- <span data-ttu-id="c5035-333">9번째 숫자는 검사 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-333">Ninth digit is a check digit</span></span>
- <span data-ttu-id="c5035-334">10번째 숫자는 문제 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-334">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="c5035-335">11번째 숫자(선택 사항)는 개인 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-335">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-336">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-336">Checksum</span></span>

<span data-ttu-id="c5035-337">예</span><span class="sxs-lookup"><span data-stu-id="c5035-337">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-338">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-338">Definition</span></span>

<span data-ttu-id="c5035-339">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-339">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-340">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-340">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-341">Keyword_Australia_Medical_Account_Number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-341">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="c5035-342">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-342">The checksum passes.</span></span>

<span data-ttu-id="c5035-343">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-343">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-344">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-344">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-345">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-345">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-346">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-346">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="c5035-347">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="c5035-347">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="c5035-348">bank account details</span><span class="sxs-lookup"><span data-stu-id="c5035-348">bank account details</span></span>
- <span data-ttu-id="c5035-349">
medicare payments</span><span class="sxs-lookup"><span data-stu-id="c5035-349">medicare payments</span></span>
- <span data-ttu-id="c5035-350">
mortgage account</span><span class="sxs-lookup"><span data-stu-id="c5035-350">mortgage account</span></span>
- <span data-ttu-id="c5035-351">
bank payments</span><span class="sxs-lookup"><span data-stu-id="c5035-351">bank payments</span></span>
- <span data-ttu-id="c5035-352">
information branch</span><span class="sxs-lookup"><span data-stu-id="c5035-352">information branch</span></span>
- <span data-ttu-id="c5035-353">
credit card loan</span><span class="sxs-lookup"><span data-stu-id="c5035-353">credit card loan</span></span>
- <span data-ttu-id="c5035-354">
department of human services</span><span class="sxs-lookup"><span data-stu-id="c5035-354">department of human services</span></span>
- <span data-ttu-id="c5035-355">로컬 서비스</span><span class="sxs-lookup"><span data-stu-id="c5035-355">local service</span></span>
- <span data-ttu-id="c5035-356">

medicare</span><span class="sxs-lookup"><span data-stu-id="c5035-356">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="c5035-357">호주 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-357">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-358">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-358">Format</span></span>

<span data-ttu-id="c5035-359">문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-359">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-360">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-360">Pattern</span></span>

<span data-ttu-id="c5035-361">1개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-361">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-362">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-362">Checksum</span></span>

<span data-ttu-id="c5035-363">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-363">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-364">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-364">Definition</span></span>

<span data-ttu-id="c5035-365">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-366">Regex_australia_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-366">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-367">Keyword_passport 또는 Keyword_australia_passport_number에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-367">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-368">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-368">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="c5035-369">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-369">Keyword_passport</span></span>

- <span data-ttu-id="c5035-370">Passport Number</span><span class="sxs-lookup"><span data-stu-id="c5035-370">Passport Number</span></span>
- <span data-ttu-id="c5035-371">
Passport No</span><span class="sxs-lookup"><span data-stu-id="c5035-371">Passport No</span></span>
- <span data-ttu-id="c5035-372">Passport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-372">Passport #</span></span>
- <span data-ttu-id="c5035-373">Passport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-373">Passport#</span></span>
- <span data-ttu-id="c5035-374">PassportID</span><span class="sxs-lookup"><span data-stu-id="c5035-374">PassportID</span></span>
- <span data-ttu-id="c5035-375">Passportno
</span><span class="sxs-lookup"><span data-stu-id="c5035-375">Passportno</span></span>
- <span data-ttu-id="c5035-376">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-376">passportnumber</span></span>
- <span data-ttu-id="c5035-377">パスポート</span><span class="sxs-lookup"><span data-stu-id="c5035-377">パスポート</span></span>
- <span data-ttu-id="c5035-378">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-378">パスポート番号</span></span>
- <span data-ttu-id="c5035-379">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="c5035-379">パスポートのNum</span></span>
- <span data-ttu-id="c5035-380">
パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="c5035-380">パスポート ＃</span></span> 
- <span data-ttu-id="c5035-381">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="c5035-381">Numéro de passeport</span></span>
- <span data-ttu-id="c5035-382">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="c5035-382">Passeport n °</span></span>
- <span data-ttu-id="c5035-383">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="c5035-383">Passeport Non</span></span>
- <span data-ttu-id="c5035-384">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-384">Passeport #</span></span>
- <span data-ttu-id="c5035-385">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-385">Passeport#</span></span>
- <span data-ttu-id="c5035-386">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="c5035-386">PasseportNon</span></span>
- <span data-ttu-id="c5035-387">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="c5035-387">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="c5035-388">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="c5035-388">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="c5035-389">passport</span><span class="sxs-lookup"><span data-stu-id="c5035-389">passport</span></span>
- <span data-ttu-id="c5035-390">
passport details</span><span class="sxs-lookup"><span data-stu-id="c5035-390">passport details</span></span>
- <span data-ttu-id="c5035-391">
immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="c5035-391">immigration and citizenship</span></span>
- <span data-ttu-id="c5035-392">
commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="c5035-392">commonwealth of australia</span></span>
- <span data-ttu-id="c5035-393">
department of immigration</span><span class="sxs-lookup"><span data-stu-id="c5035-393">department of immigration</span></span>
- <span data-ttu-id="c5035-394">
residential address</span><span class="sxs-lookup"><span data-stu-id="c5035-394">residential address</span></span>
- <span data-ttu-id="c5035-395">
department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="c5035-395">department of immigration and citizenship</span></span>
- <span data-ttu-id="c5035-396">visa
</span><span class="sxs-lookup"><span data-stu-id="c5035-396">visa</span></span>
- <span data-ttu-id="c5035-397">
national identity card</span><span class="sxs-lookup"><span data-stu-id="c5035-397">national identity card</span></span>
- <span data-ttu-id="c5035-398">여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-398">passport number</span></span>
- <span data-ttu-id="c5035-399">
travel document</span><span class="sxs-lookup"><span data-stu-id="c5035-399">travel document</span></span>
- <span data-ttu-id="c5035-400">

issuing authority</span><span class="sxs-lookup"><span data-stu-id="c5035-400">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="c5035-401">호주 세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-401">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-402">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-402">Format</span></span>

<span data-ttu-id="c5035-403">8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-403">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-404">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-404">Pattern</span></span>

<span data-ttu-id="c5035-405">일반적으로 다음과 같이 공백과 함께 표시되는 8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-405">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="c5035-406">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-406">Three digits</span></span> 
- <span data-ttu-id="c5035-407">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-407">An optional space</span></span> 
- <span data-ttu-id="c5035-408">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-408">Three digits</span></span> 
- <span data-ttu-id="c5035-409">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-409">An optional space</span></span> 
- <span data-ttu-id="c5035-410">마지막 숫자가 검사 숫자인 2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-410">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-411">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-411">Checksum</span></span>

<span data-ttu-id="c5035-412">예</span><span class="sxs-lookup"><span data-stu-id="c5035-412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-413">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-413">Definition</span></span>

<span data-ttu-id="c5035-414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-415">Func_australian_tax_file_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-415">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-416">Keyword_Australia_Tax_File_Number 또는 Keyword_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-416">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="c5035-417">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-417">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-418">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-418">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="c5035-419">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="c5035-419">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="c5035-420">australian business number</span><span class="sxs-lookup"><span data-stu-id="c5035-420">australian business number</span></span>
- <span data-ttu-id="c5035-421">
marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="c5035-421">marginal tax rate</span></span>
- <span data-ttu-id="c5035-422">
medicare levy</span><span class="sxs-lookup"><span data-stu-id="c5035-422">medicare levy</span></span>
- <span data-ttu-id="c5035-423">
portfolio number</span><span class="sxs-lookup"><span data-stu-id="c5035-423">portfolio number</span></span>
- <span data-ttu-id="c5035-424">
service veterans</span><span class="sxs-lookup"><span data-stu-id="c5035-424">service veterans</span></span>
- <span data-ttu-id="c5035-425">
withholding tax</span><span class="sxs-lookup"><span data-stu-id="c5035-425">withholding tax</span></span>
- <span data-ttu-id="c5035-426">
individual tax return</span><span class="sxs-lookup"><span data-stu-id="c5035-426">individual tax return</span></span>
- <span data-ttu-id="c5035-427">

tax file number</span><span class="sxs-lookup"><span data-stu-id="c5035-427">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="c5035-428">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="c5035-428">Keyword_number_exclusions</span></span>

- <span data-ttu-id="c5035-429">00000000</span><span class="sxs-lookup"><span data-stu-id="c5035-429">00000000</span></span>
- <span data-ttu-id="c5035-430">11111111</span><span class="sxs-lookup"><span data-stu-id="c5035-430">11111111</span></span>
- <span data-ttu-id="c5035-431">22222222</span><span class="sxs-lookup"><span data-stu-id="c5035-431">22222222</span></span>
- <span data-ttu-id="c5035-432">33333333</span><span class="sxs-lookup"><span data-stu-id="c5035-432">33333333</span></span>
- <span data-ttu-id="c5035-433">44444444</span><span class="sxs-lookup"><span data-stu-id="c5035-433">44444444</span></span>
- <span data-ttu-id="c5035-434">55555555</span><span class="sxs-lookup"><span data-stu-id="c5035-434">55555555</span></span>
- <span data-ttu-id="c5035-435">66666666</span><span class="sxs-lookup"><span data-stu-id="c5035-435">66666666</span></span>
- <span data-ttu-id="c5035-436">77777777</span><span class="sxs-lookup"><span data-stu-id="c5035-436">77777777</span></span>
- <span data-ttu-id="c5035-437">88888888</span><span class="sxs-lookup"><span data-stu-id="c5035-437">88888888</span></span>
- <span data-ttu-id="c5035-438">99999999</span><span class="sxs-lookup"><span data-stu-id="c5035-438">99999999</span></span>
- <span data-ttu-id="c5035-439">000000000</span><span class="sxs-lookup"><span data-stu-id="c5035-439">000000000</span></span>
- <span data-ttu-id="c5035-440">111111111</span><span class="sxs-lookup"><span data-stu-id="c5035-440">111111111</span></span>
- <span data-ttu-id="c5035-441">222222222</span><span class="sxs-lookup"><span data-stu-id="c5035-441">222222222</span></span>
- <span data-ttu-id="c5035-442">333333333</span><span class="sxs-lookup"><span data-stu-id="c5035-442">333333333</span></span>
- <span data-ttu-id="c5035-443">444444444</span><span class="sxs-lookup"><span data-stu-id="c5035-443">444444444</span></span>
- <span data-ttu-id="c5035-444">555555555</span><span class="sxs-lookup"><span data-stu-id="c5035-444">555555555</span></span>
- <span data-ttu-id="c5035-445">666666666</span><span class="sxs-lookup"><span data-stu-id="c5035-445">666666666</span></span>
- <span data-ttu-id="c5035-446">777777777</span><span class="sxs-lookup"><span data-stu-id="c5035-446">777777777</span></span>
- <span data-ttu-id="c5035-447">888888888</span><span class="sxs-lookup"><span data-stu-id="c5035-447">888888888</span></span>
- <span data-ttu-id="c5035-448">999999999</span><span class="sxs-lookup"><span data-stu-id="c5035-448">999999999</span></span>
- <span data-ttu-id="c5035-449">0000000000</span><span class="sxs-lookup"><span data-stu-id="c5035-449">0000000000</span></span>
- <span data-ttu-id="c5035-450">1111111111</span><span class="sxs-lookup"><span data-stu-id="c5035-450">1111111111</span></span>
- <span data-ttu-id="c5035-451">2222222222</span><span class="sxs-lookup"><span data-stu-id="c5035-451">2222222222</span></span>
- <span data-ttu-id="c5035-452">3333333333</span><span class="sxs-lookup"><span data-stu-id="c5035-452">3333333333</span></span>
- <span data-ttu-id="c5035-453">4444444444</span><span class="sxs-lookup"><span data-stu-id="c5035-453">4444444444</span></span>
- <span data-ttu-id="c5035-454">5555555555</span><span class="sxs-lookup"><span data-stu-id="c5035-454">5555555555</span></span>
- <span data-ttu-id="c5035-455">6666666666</span><span class="sxs-lookup"><span data-stu-id="c5035-455">6666666666</span></span>
- <span data-ttu-id="c5035-456">7777777777</span><span class="sxs-lookup"><span data-stu-id="c5035-456">7777777777</span></span>
- <span data-ttu-id="c5035-457">8888888888</span><span class="sxs-lookup"><span data-stu-id="c5035-457">8888888888</span></span>
- <span data-ttu-id="c5035-458">9999999999</span><span class="sxs-lookup"><span data-stu-id="c5035-458">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="c5035-459">벨기에 국가 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-459">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-460">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-460">Format</span></span>

<span data-ttu-id="c5035-461">11자리 숫자와 구분 기호</span><span class="sxs-lookup"><span data-stu-id="c5035-461">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-462">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-462">Pattern</span></span>

<span data-ttu-id="c5035-463">11자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="c5035-463">11 digits plus delimiters:</span></span>
- <span data-ttu-id="c5035-464">생년월일을 나타내는 YY.MM.DD 형식의 6자리 숫자와 마침표 2개 </span><span class="sxs-lookup"><span data-stu-id="c5035-464">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="c5035-465">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-465">A hyphen</span></span> 
- <span data-ttu-id="c5035-466">세 개의 순차적 숫자(남성의 경우 홀수, 여성의 경우 짝수) </span><span class="sxs-lookup"><span data-stu-id="c5035-466">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="c5035-467">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-467">A period</span></span> 
- <span data-ttu-id="c5035-468">검사 숫자에 해당하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-468">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-469">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-469">Checksum</span></span>

<span data-ttu-id="c5035-470">예</span><span class="sxs-lookup"><span data-stu-id="c5035-470">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-471">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-471">Definition</span></span>

<span data-ttu-id="c5035-472">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-472">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-473">Func_belgium_national_number 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-473">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-474">Keyword_belgium_national_number에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-474">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="c5035-475">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-475">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-476">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-476">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="c5035-477">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="c5035-477">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="c5035-478">Identity</span><span class="sxs-lookup"><span data-stu-id="c5035-478">Identity</span></span>
- <span data-ttu-id="c5035-479">Registration</span><span class="sxs-lookup"><span data-stu-id="c5035-479">Registration</span></span>
- <span data-ttu-id="c5035-480">Identification</span><span class="sxs-lookup"><span data-stu-id="c5035-480">Identification</span></span> 
- <span data-ttu-id="c5035-481">ID</span><span class="sxs-lookup"><span data-stu-id="c5035-481">ID</span></span> 
- <span data-ttu-id="c5035-482">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="c5035-482">Identiteitskaart</span></span>
- <span data-ttu-id="c5035-483">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="c5035-483">Registratie nummer</span></span> 
- <span data-ttu-id="c5035-484">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-484">Identificatie nummer</span></span> 
- <span data-ttu-id="c5035-485">Identiteit</span><span class="sxs-lookup"><span data-stu-id="c5035-485">Identiteit</span></span>
- <span data-ttu-id="c5035-486">Registratie</span><span class="sxs-lookup"><span data-stu-id="c5035-486">Registratie</span></span>
- <span data-ttu-id="c5035-487">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="c5035-487">Identificatie</span></span> 
- <span data-ttu-id="c5035-488">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="c5035-488">Carte d’identité</span></span> 
- <span data-ttu-id="c5035-489">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="c5035-489">numéro d'immatriculation</span></span>
- <span data-ttu-id="c5035-490">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="c5035-490">numéro d'identification</span></span>
- <span data-ttu-id="c5035-491">
identité
</span><span class="sxs-lookup"><span data-stu-id="c5035-491">identité</span></span> 
- <span data-ttu-id="c5035-492">inscription
</span><span class="sxs-lookup"><span data-stu-id="c5035-492">inscription</span></span> 
- <span data-ttu-id="c5035-493">Identifikation</span><span class="sxs-lookup"><span data-stu-id="c5035-493">Identifikation</span></span>
- <span data-ttu-id="c5035-494">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="c5035-494">Identifizierung</span></span>
- <span data-ttu-id="c5035-495">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-495">Identifikationsnummer</span></span>
- <span data-ttu-id="c5035-496">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="c5035-496">Personalausweis</span></span>
- <span data-ttu-id="c5035-497">Registrierung</span><span class="sxs-lookup"><span data-stu-id="c5035-497">Registrierung</span></span>
- <span data-ttu-id="c5035-498">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-498">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="c5035-499">브라질 CPF 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-499">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-500">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-500">Format</span></span>

<span data-ttu-id="c5035-501">서식이 있거나 서식이 없을 수 있는 검사 숫자를 포함하는 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-501">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-502">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-502">Pattern</span></span>

<span data-ttu-id="c5035-503">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="c5035-503">Formatted:</span></span>
- <span data-ttu-id="c5035-504">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-504">Three digits</span></span> 
- <span data-ttu-id="c5035-505">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-505">A period</span></span> 
- <span data-ttu-id="c5035-506">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-506">Three digits</span></span> 
- <span data-ttu-id="c5035-507">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-507">A period</span></span> 
- <span data-ttu-id="c5035-508">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-508">Three digits</span></span> 
- <span data-ttu-id="c5035-509">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-509">A hyphen</span></span> 
- <span data-ttu-id="c5035-510">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-510">Two digits which are check digits</span></span>

<span data-ttu-id="c5035-511">서식 없음:</span><span class="sxs-lookup"><span data-stu-id="c5035-511">Unformatted:</span></span>
- <span data-ttu-id="c5035-512">마지막 2자리 숫자가 검사 숫자인 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-512">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-513">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-513">Checksum</span></span>

<span data-ttu-id="c5035-514">예</span><span class="sxs-lookup"><span data-stu-id="c5035-514">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-515">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-515">Definition</span></span>

<span data-ttu-id="c5035-516">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-516">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-517">Func_brazil_cpf 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-517">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-518">Keyword_brazil_cpf에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-518">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="c5035-519">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-519">The checksum passes.</span></span>

<span data-ttu-id="c5035-520">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-521">Func_brazil_cpf 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-521">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-522">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-522">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-523">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-523">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="c5035-524">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="c5035-524">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="c5035-525">CPF</span><span class="sxs-lookup"><span data-stu-id="c5035-525">CPF</span></span>
- <span data-ttu-id="c5035-526">Identification</span><span class="sxs-lookup"><span data-stu-id="c5035-526">Identification</span></span>
- <span data-ttu-id="c5035-527">Registration</span><span class="sxs-lookup"><span data-stu-id="c5035-527">Registration</span></span>
- <span data-ttu-id="c5035-528">Revenue</span><span class="sxs-lookup"><span data-stu-id="c5035-528">Revenue</span></span>
- <span data-ttu-id="c5035-529">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="c5035-529">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="c5035-530">Imposto
</span><span class="sxs-lookup"><span data-stu-id="c5035-530">Imposto</span></span> 
- <span data-ttu-id="c5035-531">Identificação
</span><span class="sxs-lookup"><span data-stu-id="c5035-531">Identificação</span></span> 
- <span data-ttu-id="c5035-532">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="c5035-532">Inscrição</span></span> 
- <span data-ttu-id="c5035-533">Receita

</span><span class="sxs-lookup"><span data-stu-id="c5035-533">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="c5035-534">브라질 법인 번호(CNPJ)</span><span class="sxs-lookup"><span data-stu-id="c5035-534">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-535">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-535">Format</span></span>

<span data-ttu-id="c5035-536">등록 번호, 지점 번호, 검사 숫자 및 구분 기호를 포함하는 14자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-536">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-537">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-537">Pattern</span></span>
<span data-ttu-id="c5035-538">14자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="c5035-538">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="c5035-539">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-539">Two digits</span></span> 
- <span data-ttu-id="c5035-540">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-540">A period</span></span> 
- <span data-ttu-id="c5035-541">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-541">Three digits</span></span> 
- <span data-ttu-id="c5035-542">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-542">A period</span></span> 
- <span data-ttu-id="c5035-543">3자리 숫자(처음 8자리 숫자는 등록 번호임) </span><span class="sxs-lookup"><span data-stu-id="c5035-543">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="c5035-544">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="c5035-544">A forward slash</span></span> 
- <span data-ttu-id="c5035-545">4자리 지점 번호 </span><span class="sxs-lookup"><span data-stu-id="c5035-545">Four-digit branch number</span></span> 
- <span data-ttu-id="c5035-546">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-546">A hyphen</span></span> 
- <span data-ttu-id="c5035-547">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-547">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-548">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-548">Checksum</span></span>

<span data-ttu-id="c5035-549">예</span><span class="sxs-lookup"><span data-stu-id="c5035-549">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-550">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-550">Definition</span></span>

<span data-ttu-id="c5035-551">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-551">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-552">Func_brazil_cnpj 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-552">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-553">Keyword_brazil_cnpj에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-553">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="c5035-554">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-554">The checksum passes.</span></span>

<span data-ttu-id="c5035-555">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-555">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-556">Func_brazil_cnpj 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-556">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-557">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-557">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-558">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-558">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="c5035-559">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="c5035-559">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="c5035-560">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="c5035-560">CNPJ</span></span> 
- <span data-ttu-id="c5035-561">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="c5035-561">CNPJ/MF</span></span> 
- <span data-ttu-id="c5035-562">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="c5035-562">CNPJ-MF</span></span> 
- <span data-ttu-id="c5035-563">National Registry of Legal Entities
</span><span class="sxs-lookup"><span data-stu-id="c5035-563">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="c5035-564">Taxpayers Registry
</span><span class="sxs-lookup"><span data-stu-id="c5035-564">Taxpayers Registry</span></span> 
- <span data-ttu-id="c5035-565">Legal entity
</span><span class="sxs-lookup"><span data-stu-id="c5035-565">Legal entity</span></span> 
- <span data-ttu-id="c5035-566">Legal entities
</span><span class="sxs-lookup"><span data-stu-id="c5035-566">Legal entities</span></span> 
- <span data-ttu-id="c5035-567">Registration Status
</span><span class="sxs-lookup"><span data-stu-id="c5035-567">Registration Status</span></span> 
- <span data-ttu-id="c5035-568">Business
</span><span class="sxs-lookup"><span data-stu-id="c5035-568">Business</span></span> 
- <span data-ttu-id="c5035-569">Company</span><span class="sxs-lookup"><span data-stu-id="c5035-569">Company</span></span>
- <span data-ttu-id="c5035-570">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="c5035-570">CNPJ</span></span> 
- <span data-ttu-id="c5035-571">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="c5035-571">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="c5035-572">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="c5035-572">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="c5035-573">CGC
</span><span class="sxs-lookup"><span data-stu-id="c5035-573">CGC</span></span> 
- <span data-ttu-id="c5035-574">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="c5035-574">Pessoa jurídica</span></span> 
- <span data-ttu-id="c5035-575">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="c5035-575">Pessoas jurídicas</span></span> 
- <span data-ttu-id="c5035-576">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="c5035-576">Situação cadastral</span></span> 
- <span data-ttu-id="c5035-577">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="c5035-577">Inscrição</span></span> 
- <span data-ttu-id="c5035-578">Empresa
</span><span class="sxs-lookup"><span data-stu-id="c5035-578">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="c5035-579">	브라질 국가 ID 카드(RG)</span><span class="sxs-lookup"><span data-stu-id="c5035-579">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-580">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-580">Format</span></span>

<span data-ttu-id="c5035-581">Registro Geral (이전 형식): 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="c5035-581">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="c5035-582">Registro de Identidade (RIC) (새 형식): 11</span><span class="sxs-lookup"><span data-stu-id="c5035-582">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-583">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-583">Pattern</span></span>

<span data-ttu-id="c5035-584">Registro Geral(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="c5035-584">Registro Geral (old format):</span></span>
- <span data-ttu-id="c5035-585">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-585">Two digits</span></span> 
- <span data-ttu-id="c5035-586">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-586">A period</span></span> 
- <span data-ttu-id="c5035-587">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-587">Three digits</span></span> 
- <span data-ttu-id="c5035-588">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-588">A period</span></span> 
- <span data-ttu-id="c5035-589">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-589">Three digits</span></span> 
- <span data-ttu-id="c5035-590">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-590">A hyphen</span></span> 
- <span data-ttu-id="c5035-591">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-591">One digit which is a check digit</span></span>

<span data-ttu-id="c5035-592">Registro de Identidade (RIC) (새 형식):</span><span class="sxs-lookup"><span data-stu-id="c5035-592">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="c5035-593">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-593">10 digits</span></span> 
- <span data-ttu-id="c5035-594">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-594">A hyphen</span></span> 
- <span data-ttu-id="c5035-595">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-595">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-596">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-596">Checksum</span></span>

<span data-ttu-id="c5035-597">예</span><span class="sxs-lookup"><span data-stu-id="c5035-597">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-598">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-598">Definition</span></span>

<span data-ttu-id="c5035-599">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-599">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-600">Func_brazil_rg 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-600">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-601">Keyword_brazil_rg에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-601">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="c5035-602">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-602">The checksum passes.</span></span>

<span data-ttu-id="c5035-603">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-603">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-604">Func_brazil_rg 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-604">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-605">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-605">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-606">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-606">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="c5035-607">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="c5035-607">Keyword_brazil_rg</span></span>

<span data-ttu-id="c5035-608">Cédula de identidade id 카드 국가 id número de rregistro registro de Iidentidade registro geral (이 키워드는 대/소문자 구분) RG RIC (이 키워드는 대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="c5035-608">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="c5035-609">캐나다 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-609">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-610">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-610">Format</span></span>

<span data-ttu-id="c5035-611">7 또는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-611">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-612">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-612">Pattern</span></span>

<span data-ttu-id="c5035-613">캐나다 은행 계좌 번호는 7 또는 12자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-613">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="c5035-614">캐나다 은행 계좌 송금 번호:</span><span class="sxs-lookup"><span data-stu-id="c5035-614">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="c5035-615">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-615">Five digits</span></span> 
- <span data-ttu-id="c5035-616">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-616">A hyphen</span></span> 
- <span data-ttu-id="c5035-617">세 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="c5035-617">Three digits OR</span></span>
- <span data-ttu-id="c5035-618">"0"</span><span class="sxs-lookup"><span data-stu-id="c5035-618">A zero "0"</span></span> 
- <span data-ttu-id="c5035-619">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-619">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-620">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-620">Checksum</span></span>

<span data-ttu-id="c5035-621">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-621">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-622">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-622">Definition</span></span>

<span data-ttu-id="c5035-623">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-623">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-624">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-624">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-625">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-625">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="c5035-626">Regex_canada_bank_account_transit_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-626">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="c5035-627">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-627">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-628">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-628">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-629">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-629">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-630">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-630">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="c5035-631">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="c5035-631">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="c5035-632">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="c5035-632">canada savings bonds</span></span>
- <span data-ttu-id="c5035-633">
canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="c5035-633">canada revenue agency</span></span>
- <span data-ttu-id="c5035-634">
canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="c5035-634">canadian financial institution</span></span>
- <span data-ttu-id="c5035-635">
direct deposit form</span><span class="sxs-lookup"><span data-stu-id="c5035-635">direct deposit form</span></span>
- <span data-ttu-id="c5035-636">
canadian citizen</span><span class="sxs-lookup"><span data-stu-id="c5035-636">canadian citizen</span></span>
- <span data-ttu-id="c5035-637">
legal representative</span><span class="sxs-lookup"><span data-stu-id="c5035-637">legal representative</span></span>
- <span data-ttu-id="c5035-638">
notary public</span><span class="sxs-lookup"><span data-stu-id="c5035-638">notary public</span></span>
- <span data-ttu-id="c5035-639">
commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="c5035-639">commissioner for oaths</span></span>
- <span data-ttu-id="c5035-640">
child care benefit</span><span class="sxs-lookup"><span data-stu-id="c5035-640">child care benefit</span></span>
- <span data-ttu-id="c5035-641">
universal child care</span><span class="sxs-lookup"><span data-stu-id="c5035-641">universal child care</span></span>
- <span data-ttu-id="c5035-642">
canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="c5035-642">canada child tax benefit</span></span>
- <span data-ttu-id="c5035-643">
income tax benefit</span><span class="sxs-lookup"><span data-stu-id="c5035-643">income tax benefit</span></span>
- <span data-ttu-id="c5035-644">
harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="c5035-644">harmonized sales tax</span></span>
- <span data-ttu-id="c5035-645">social insurance number</span><span class="sxs-lookup"><span data-stu-id="c5035-645">social insurance number</span></span>
- <span data-ttu-id="c5035-646">
income tax refund</span><span class="sxs-lookup"><span data-stu-id="c5035-646">income tax refund</span></span>
- <span data-ttu-id="c5035-647">
child tax benefit</span><span class="sxs-lookup"><span data-stu-id="c5035-647">child tax benefit</span></span>
- <span data-ttu-id="c5035-648">
territorial payments</span><span class="sxs-lookup"><span data-stu-id="c5035-648">territorial payments</span></span>
- <span data-ttu-id="c5035-649">
institution number</span><span class="sxs-lookup"><span data-stu-id="c5035-649">institution number</span></span>
- <span data-ttu-id="c5035-650">
deposit request</span><span class="sxs-lookup"><span data-stu-id="c5035-650">deposit request</span></span>
- <span data-ttu-id="c5035-651">
banking information</span><span class="sxs-lookup"><span data-stu-id="c5035-651">banking information</span></span>
- <span data-ttu-id="c5035-652">

direct deposit</span><span class="sxs-lookup"><span data-stu-id="c5035-652">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="c5035-653">캐나다 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-653">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-654">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-654">Format</span></span>

<span data-ttu-id="c5035-655">지역마다 다름</span><span class="sxs-lookup"><span data-stu-id="c5035-655">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-656">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-656">Pattern</span></span>

<span data-ttu-id="c5035-657">앨버타, 브리티시 콜롬비아, 매니토바, 뉴브런즈윅, 뉴펀들랜드/래브라도, 노바스코샤, 온타리오, 프린스에드워드아일랜드, 퀘벡 및 서스캐처원을 포함하는 다양한 패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-657">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-658">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-658">Checksum</span></span>

<span data-ttu-id="c5035-659">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-659">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-660">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-660">Definition</span></span>

<span data-ttu-id="c5035-661">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-661">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-662">Func_[province_name]_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-662">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-663">Keyword_[province_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-663">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="c5035-664">Keyword_canada_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-664">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-665">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-665">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="c5035-666">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="c5035-666">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="c5035-667">시/도 약어(예: AB)</span><span class="sxs-lookup"><span data-stu-id="c5035-667">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="c5035-668">
시/도 이름(예: 앨버타)</span><span class="sxs-lookup"><span data-stu-id="c5035-668">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="c5035-669">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="c5035-669">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="c5035-670">DL</span><span class="sxs-lookup"><span data-stu-id="c5035-670">DL</span></span>
- <span data-ttu-id="c5035-671">DLS</span><span class="sxs-lookup"><span data-stu-id="c5035-671">DLS</span></span>
- <span data-ttu-id="c5035-672">CDL</span><span class="sxs-lookup"><span data-stu-id="c5035-672">CDL</span></span>
- <span data-ttu-id="c5035-673">CDLS</span><span class="sxs-lookup"><span data-stu-id="c5035-673">CDLS</span></span>
- <span data-ttu-id="c5035-674">DriverLic</span><span class="sxs-lookup"><span data-stu-id="c5035-674">DriverLic</span></span>
- <span data-ttu-id="c5035-675">DriverLics</span><span class="sxs-lookup"><span data-stu-id="c5035-675">DriverLics</span></span>
- <span data-ttu-id="c5035-676">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-676">DriverLicense</span></span>
- <span data-ttu-id="c5035-677">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-677">DriverLicenses</span></span>
- <span data-ttu-id="c5035-678">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="c5035-678">DriverLicence</span></span>
- <span data-ttu-id="c5035-679">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="c5035-679">DriverLicences</span></span>
- <span data-ttu-id="c5035-680">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-680">Driver Lic</span></span>
- <span data-ttu-id="c5035-681">드라이버 Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-681">Driver Lics</span></span>
- <span data-ttu-id="c5035-682">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-682">Driver License</span></span>
- <span data-ttu-id="c5035-683">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-683">Driver Licenses</span></span>
- <span data-ttu-id="c5035-684">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-684">Driver Licence</span></span>
- <span data-ttu-id="c5035-685">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="c5035-685">Driver Licences</span></span>
- <span data-ttu-id="c5035-686">DriversLic</span><span class="sxs-lookup"><span data-stu-id="c5035-686">DriversLic</span></span>
- <span data-ttu-id="c5035-687">DriversLics</span><span class="sxs-lookup"><span data-stu-id="c5035-687">DriversLics</span></span>
- <span data-ttu-id="c5035-688">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="c5035-688">DriversLicence</span></span>
- <span data-ttu-id="c5035-689">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="c5035-689">DriversLicences</span></span>
- <span data-ttu-id="c5035-690">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-690">DriversLicense</span></span>
- <span data-ttu-id="c5035-691">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-691">DriversLicenses</span></span>
- <span data-ttu-id="c5035-692">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-692">Drivers Lic</span></span>
- <span data-ttu-id="c5035-693">드라이버 Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-693">Drivers Lics</span></span>
- <span data-ttu-id="c5035-694">운전 면허</span><span class="sxs-lookup"><span data-stu-id="c5035-694">Drivers License</span></span>
- <span data-ttu-id="c5035-695">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-695">Drivers Licenses</span></span>
- <span data-ttu-id="c5035-696">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="c5035-696">Drivers Licence</span></span>
- <span data-ttu-id="c5035-697">드라이버 라이센스</span><span class="sxs-lookup"><span data-stu-id="c5035-697">Drivers Licences</span></span>
- <span data-ttu-id="c5035-698">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-698">Driver'Lic</span></span>
- <span data-ttu-id="c5035-699">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-699">Driver'Lics</span></span>
- <span data-ttu-id="c5035-700">Driver'License</span><span class="sxs-lookup"><span data-stu-id="c5035-700">Driver'License</span></span>
- <span data-ttu-id="c5035-701">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="c5035-701">Driver'Licenses</span></span>
- <span data-ttu-id="c5035-702">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="c5035-702">Driver'Licence</span></span>
- <span data-ttu-id="c5035-703">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="c5035-703">Driver'Licences</span></span>
- <span data-ttu-id="c5035-704">드라이버 ' Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-704">Driver' Lic</span></span>
- <span data-ttu-id="c5035-705">드라이버 ' Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-705">Driver' Lics</span></span>
- <span data-ttu-id="c5035-706">드라이버 ' 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-706">Driver' License</span></span>
- <span data-ttu-id="c5035-707">드라이버 ' 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-707">Driver' Licenses</span></span>
- <span data-ttu-id="c5035-708">드라이버 ' 사용권</span><span class="sxs-lookup"><span data-stu-id="c5035-708">Driver' Licence</span></span>
- <span data-ttu-id="c5035-709">드라이버 ' 라이센스</span><span class="sxs-lookup"><span data-stu-id="c5035-709">Driver' Licences</span></span>
- <span data-ttu-id="c5035-710">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="c5035-710">Driver'sLic</span></span>
- <span data-ttu-id="c5035-711">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="c5035-711">Driver'sLics</span></span>
- <span data-ttu-id="c5035-712">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-712">Driver'sLicense</span></span>
- <span data-ttu-id="c5035-713">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-713">Driver'sLicenses</span></span>
- <span data-ttu-id="c5035-714">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="c5035-714">Driver'sLicence</span></span>
- <span data-ttu-id="c5035-715">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="c5035-715">Driver'sLicences</span></span>
- <span data-ttu-id="c5035-716">드라이버의 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-716">Driver's Lic</span></span>
- <span data-ttu-id="c5035-717">드라이버의 Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-717">Driver's Lics</span></span>
- <span data-ttu-id="c5035-718">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-718">Driver's License</span></span>
- <span data-ttu-id="c5035-719">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-719">Driver's Licenses</span></span>
- <span data-ttu-id="c5035-720">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-720">Driver's Licence</span></span>
- <span data-ttu-id="c5035-721">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="c5035-721">Driver's Licences</span></span>
- <span data-ttu-id="c5035-722">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="c5035-722">Permis de Conduire</span></span>
- <span data-ttu-id="c5035-723">id</span><span class="sxs-lookup"><span data-stu-id="c5035-723">id</span></span>
- <span data-ttu-id="c5035-724">id</span><span class="sxs-lookup"><span data-stu-id="c5035-724">ids</span></span>
- <span data-ttu-id="c5035-725">
idcard number</span><span class="sxs-lookup"><span data-stu-id="c5035-725">idcard number</span></span>
- <span data-ttu-id="c5035-726">
idcard numbers</span><span class="sxs-lookup"><span data-stu-id="c5035-726">idcard numbers</span></span>
- <span data-ttu-id="c5035-727">
idcard #</span><span class="sxs-lookup"><span data-stu-id="c5035-727">idcard #</span></span>
- <span data-ttu-id="c5035-728">
idcard #s</span><span class="sxs-lookup"><span data-stu-id="c5035-728">idcard #s</span></span>
- <span data-ttu-id="c5035-729">idcard 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-729">idcard card</span></span>
- <span data-ttu-id="c5035-730">idcard 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-730">idcard cards</span></span>
- <span data-ttu-id="c5035-731">idcard</span><span class="sxs-lookup"><span data-stu-id="c5035-731">idcard</span></span>
- <span data-ttu-id="c5035-732">identification number
</span><span class="sxs-lookup"><span data-stu-id="c5035-732">identification number</span></span>
- <span data-ttu-id="c5035-733">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="c5035-733">identification numbers</span></span>
- <span data-ttu-id="c5035-734">identification #
</span><span class="sxs-lookup"><span data-stu-id="c5035-734">identification #</span></span>
- <span data-ttu-id="c5035-735">
identification #s</span><span class="sxs-lookup"><span data-stu-id="c5035-735">identification #s</span></span>
- <span data-ttu-id="c5035-736">id 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-736">identification card</span></span>
- <span data-ttu-id="c5035-737">식별 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-737">identification cards</span></span>
- <span data-ttu-id="c5035-738">
identification
</span><span class="sxs-lookup"><span data-stu-id="c5035-738">identification</span></span> 
- <span data-ttu-id="c5035-739">DL#</span><span class="sxs-lookup"><span data-stu-id="c5035-739">DL#</span></span>
- <span data-ttu-id="c5035-740">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="c5035-740">DLS#</span></span> 
- <span data-ttu-id="c5035-741">CDL#
</span><span class="sxs-lookup"><span data-stu-id="c5035-741">CDL#</span></span> 
- <span data-ttu-id="c5035-742">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="c5035-742">CDLS#</span></span> 
- <span data-ttu-id="c5035-743">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-743">DriverLic#</span></span> 
- <span data-ttu-id="c5035-744">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-744">DriverLics#</span></span> 
- <span data-ttu-id="c5035-745">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-745">DriverLicense#</span></span> 
- <span data-ttu-id="c5035-746">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-746">DriverLicenses#</span></span> 
- <span data-ttu-id="c5035-747">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="c5035-747">DriverLicence#</span></span> 
- <span data-ttu-id="c5035-748">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="c5035-748">DriverLicences#</span></span> 
- <span data-ttu-id="c5035-749">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="c5035-749">Driver Lic#</span></span>
- <span data-ttu-id="c5035-750">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-750">Driver Lics#</span></span> 
- <span data-ttu-id="c5035-751">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-751">Driver License#</span></span> 
- <span data-ttu-id="c5035-752">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-752">Driver Licenses#</span></span> 
- <span data-ttu-id="c5035-753">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-753">Driver License#</span></span> 
- <span data-ttu-id="c5035-754">드라이버 라이센스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-754">Driver Licences#</span></span> 
- <span data-ttu-id="c5035-755">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-755">DriversLic#</span></span> 
- <span data-ttu-id="c5035-756">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-756">DriversLics#</span></span> 
- <span data-ttu-id="c5035-757">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-757">DriversLicense#</span></span> 
- <span data-ttu-id="c5035-758">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-758">DriversLicenses#</span></span> 
- <span data-ttu-id="c5035-759">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="c5035-759">DriversLicence#</span></span> 
- <span data-ttu-id="c5035-760">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="c5035-760">DriversLicences#</span></span> 
- <span data-ttu-id="c5035-761">드라이버 Lic #</span><span class="sxs-lookup"><span data-stu-id="c5035-761">Drivers Lic#</span></span> 
- <span data-ttu-id="c5035-762">드라이버 Lics #</span><span class="sxs-lookup"><span data-stu-id="c5035-762">Drivers Lics#</span></span> 
- <span data-ttu-id="c5035-763">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-763">Drivers License#</span></span> 
- <span data-ttu-id="c5035-764">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-764">Drivers Licenses#</span></span> 
- <span data-ttu-id="c5035-765">드라이버 사용권 #</span><span class="sxs-lookup"><span data-stu-id="c5035-765">Drivers Licence#</span></span> 
- <span data-ttu-id="c5035-766">드라이버 라이센스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-766">Drivers Licences#</span></span> 
- <span data-ttu-id="c5035-767">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-767">Driver'Lic#</span></span> 
- <span data-ttu-id="c5035-768">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-768">Driver'Lics#</span></span> 
- <span data-ttu-id="c5035-769">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-769">Driver'License#</span></span> 
- <span data-ttu-id="c5035-770">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="c5035-770">Driver'Licenses#</span></span> 
- <span data-ttu-id="c5035-771">Driver'Licence #
</span><span class="sxs-lookup"><span data-stu-id="c5035-771">Driver'Licence#</span></span> 
- <span data-ttu-id="c5035-772">Driver'Licences#
</span><span class="sxs-lookup"><span data-stu-id="c5035-772">Driver'Licences#</span></span> 
- <span data-ttu-id="c5035-773">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-773">Driver' Lic#</span></span> 
- <span data-ttu-id="c5035-774">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-774">Driver' Lics#</span></span> 
- <span data-ttu-id="c5035-775">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-775">Driver' License#</span></span> 
- <span data-ttu-id="c5035-776">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="c5035-776">Driver' Licenses#</span></span> 
- <span data-ttu-id="c5035-777">드라이버 ' 사용권 #</span><span class="sxs-lookup"><span data-stu-id="c5035-777">Driver' Licence#</span></span> 
- <span data-ttu-id="c5035-778">드라이버 ' 라이센스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-778">Driver' Licences#</span></span> 
- <span data-ttu-id="c5035-779">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-779">Driver'sLic#</span></span> 
- <span data-ttu-id="c5035-780">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-780">Driver'sLics#</span></span> 
- <span data-ttu-id="c5035-781">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-781">Driver'sLicense#</span></span> 
- <span data-ttu-id="c5035-782">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-782">Driver'sLicenses#</span></span> 
- <span data-ttu-id="c5035-783">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="c5035-783">Driver'sLicence#</span></span> 
- <span data-ttu-id="c5035-784">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="c5035-784">Driver'sLicences#</span></span> 
- <span data-ttu-id="c5035-785">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-785">Driver's Lic#</span></span> 
- <span data-ttu-id="c5035-786">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-786">Driver's Lics#</span></span> 
- <span data-ttu-id="c5035-787">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-787">Driver's License#</span></span> 
- <span data-ttu-id="c5035-788">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="c5035-788">Driver's Licenses#</span></span> 
- <span data-ttu-id="c5035-789">드라이버의 사용권 #</span><span class="sxs-lookup"><span data-stu-id="c5035-789">Driver's Licence#</span></span> 
- <span data-ttu-id="c5035-790">드라이버의 라이센스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-790">Driver's Licences#</span></span> 
- <span data-ttu-id="c5035-791">Permis de Conduire #</span><span class="sxs-lookup"><span data-stu-id="c5035-791">Permis de Conduire#</span></span> 
- <span data-ttu-id="c5035-792">id #</span><span class="sxs-lookup"><span data-stu-id="c5035-792">id#</span></span> 
- <span data-ttu-id="c5035-793">id #</span><span class="sxs-lookup"><span data-stu-id="c5035-793">ids#</span></span> 
- <span data-ttu-id="c5035-794">idcard card#
</span><span class="sxs-lookup"><span data-stu-id="c5035-794">idcard card#</span></span> 
- <span data-ttu-id="c5035-795">idcard cards#
</span><span class="sxs-lookup"><span data-stu-id="c5035-795">idcard cards#</span></span> 
- <span data-ttu-id="c5035-796">idcard#
</span><span class="sxs-lookup"><span data-stu-id="c5035-796">idcard#</span></span> 
- <span data-ttu-id="c5035-797">identification card#
</span><span class="sxs-lookup"><span data-stu-id="c5035-797">identification card#</span></span> 
- <span data-ttu-id="c5035-798">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="c5035-798">identification cards#</span></span> 
- <span data-ttu-id="c5035-799">identification#
</span><span class="sxs-lookup"><span data-stu-id="c5035-799">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="c5035-800">캐나다 건강 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-800">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-801">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-801">Format</span></span>

<span data-ttu-id="c5035-802">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-802">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-803">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-803">Pattern</span></span>

<span data-ttu-id="c5035-804">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-804">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-805">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-805">Checksum</span></span>

<span data-ttu-id="c5035-806">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-806">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-807">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-807">Definition</span></span>

<span data-ttu-id="c5035-808">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-808">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-809">Regex_canada_health_service_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-809">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-810">Keyword_canada_health_service_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-810">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-811">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-811">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="c5035-812">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="c5035-812">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="c5035-813">personal health number</span><span class="sxs-lookup"><span data-stu-id="c5035-813">personal health number</span></span>
- <span data-ttu-id="c5035-814">
patient information</span><span class="sxs-lookup"><span data-stu-id="c5035-814">patient information</span></span>
- <span data-ttu-id="c5035-815">상태 서비스</span><span class="sxs-lookup"><span data-stu-id="c5035-815">health services</span></span>
- <span data-ttu-id="c5035-816">
speciality services</span><span class="sxs-lookup"><span data-stu-id="c5035-816">speciality services</span></span>
- <span data-ttu-id="c5035-817">
automobile accident</span><span class="sxs-lookup"><span data-stu-id="c5035-817">automobile accident</span></span>
- <span data-ttu-id="c5035-818">
patient hospital</span><span class="sxs-lookup"><span data-stu-id="c5035-818">patient hospital</span></span>
- <span data-ttu-id="c5035-819">
psychiatrist</span><span class="sxs-lookup"><span data-stu-id="c5035-819">psychiatrist</span></span>
- <span data-ttu-id="c5035-820">
workers compensation</span><span class="sxs-lookup"><span data-stu-id="c5035-820">workers compensation</span></span>
- <span data-ttu-id="c5035-821">
disability</span><span class="sxs-lookup"><span data-stu-id="c5035-821">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="c5035-822">캐나다 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-822">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-823">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-823">Format</span></span>

<span data-ttu-id="c5035-824">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-824">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-825">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-825">Pattern</span></span>

<span data-ttu-id="c5035-826">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-826">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-827">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-827">Checksum</span></span>

<span data-ttu-id="c5035-828">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-828">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-829">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-829">Definition</span></span>

<span data-ttu-id="c5035-830">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-830">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-831">Regex_canada_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-831">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-832">Keyword_canada_passport_number 또는 Keyword_passport에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-832">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-833">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-833">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="c5035-834">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="c5035-834">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="c5035-835">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="c5035-835">canadian citizenship</span></span>
- <span data-ttu-id="c5035-836">
canadian passport</span><span class="sxs-lookup"><span data-stu-id="c5035-836">canadian passport</span></span>
- <span data-ttu-id="c5035-837">
passport application</span><span class="sxs-lookup"><span data-stu-id="c5035-837">passport application</span></span>
- <span data-ttu-id="c5035-838">
passport photos</span><span class="sxs-lookup"><span data-stu-id="c5035-838">passport photos</span></span>
- <span data-ttu-id="c5035-839">
certified translator</span><span class="sxs-lookup"><span data-stu-id="c5035-839">certified translator</span></span>
- <span data-ttu-id="c5035-840">
canadian citizens</span><span class="sxs-lookup"><span data-stu-id="c5035-840">canadian citizens</span></span>
- <span data-ttu-id="c5035-841">
processing times</span><span class="sxs-lookup"><span data-stu-id="c5035-841">processing times</span></span>
- <span data-ttu-id="c5035-842">

renewal application</span><span class="sxs-lookup"><span data-stu-id="c5035-842">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="c5035-843">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-843">Keyword_passport</span></span>

- <span data-ttu-id="c5035-844">Passport Number</span><span class="sxs-lookup"><span data-stu-id="c5035-844">Passport Number</span></span>
- <span data-ttu-id="c5035-845">
Passport No</span><span class="sxs-lookup"><span data-stu-id="c5035-845">Passport No</span></span>
- <span data-ttu-id="c5035-846">Passport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-846">Passport #</span></span>
- <span data-ttu-id="c5035-847">Passport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-847">Passport#</span></span>
- <span data-ttu-id="c5035-848">PassportID</span><span class="sxs-lookup"><span data-stu-id="c5035-848">PassportID</span></span>
- <span data-ttu-id="c5035-849">Passportno
</span><span class="sxs-lookup"><span data-stu-id="c5035-849">Passportno</span></span>
- <span data-ttu-id="c5035-850">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-850">passportnumber</span></span>
- <span data-ttu-id="c5035-851">パスポート</span><span class="sxs-lookup"><span data-stu-id="c5035-851">パスポート</span></span>
- <span data-ttu-id="c5035-852">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-852">パスポート番号</span></span>
- <span data-ttu-id="c5035-853">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="c5035-853">パスポートのNum</span></span>
- <span data-ttu-id="c5035-854">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="c5035-854">パスポート＃</span></span>
- <span data-ttu-id="c5035-855">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="c5035-855">Numéro de passeport</span></span>
- <span data-ttu-id="c5035-856">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="c5035-856">Passeport n °</span></span>
- <span data-ttu-id="c5035-857">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="c5035-857">Passeport Non</span></span>
- <span data-ttu-id="c5035-858">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-858">Passeport #</span></span>
- <span data-ttu-id="c5035-859">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-859">Passeport#</span></span>
- <span data-ttu-id="c5035-860">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="c5035-860">PasseportNon</span></span>
- <span data-ttu-id="c5035-861">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="c5035-861">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="c5035-862">캐나다 PHIN(개인 건강 식별 번호)</span><span class="sxs-lookup"><span data-stu-id="c5035-862">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-863">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-863">Format</span></span>

<span data-ttu-id="c5035-864">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-864">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-865">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-865">Pattern</span></span>

<span data-ttu-id="c5035-866">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-866">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-867">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-867">Checksum</span></span>

<span data-ttu-id="c5035-868">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-868">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-869">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-869">Definition</span></span>

<span data-ttu-id="c5035-p104">DLP 정책은 이러한 종류의 중요 한 정보를 감지 했습니다 판단 75%에 근접 300 자 내에 있는 경우,: Regex_canada_phin 정규식 패턴과 일치 하는 콘텐츠를 찾습니다. Keyword_canada_phin 또는 Keyword_canada_provinces에서 키워드를 둘 이상 발견 되.</span><span class="sxs-lookup"><span data-stu-id="c5035-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-872">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-872">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="c5035-873">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="c5035-873">Keyword_canada_phin</span></span>

- <span data-ttu-id="c5035-874">social insurance number</span><span class="sxs-lookup"><span data-stu-id="c5035-874">social insurance number</span></span>
- <span data-ttu-id="c5035-875">
health information act</span><span class="sxs-lookup"><span data-stu-id="c5035-875">health information act</span></span>
- <span data-ttu-id="c5035-876">
income tax information</span><span class="sxs-lookup"><span data-stu-id="c5035-876">income tax information</span></span>
- <span data-ttu-id="c5035-877">
manitoba health</span><span class="sxs-lookup"><span data-stu-id="c5035-877">manitoba health</span></span>
- <span data-ttu-id="c5035-878">
health registration</span><span class="sxs-lookup"><span data-stu-id="c5035-878">health registration</span></span>
- <span data-ttu-id="c5035-879">
prescription purchases</span><span class="sxs-lookup"><span data-stu-id="c5035-879">prescription purchases</span></span>
- <span data-ttu-id="c5035-880">
benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="c5035-880">benefit eligibility</span></span>
- <span data-ttu-id="c5035-881">
personal health</span><span class="sxs-lookup"><span data-stu-id="c5035-881">personal health</span></span>
- <span data-ttu-id="c5035-882">
power of attorney</span><span class="sxs-lookup"><span data-stu-id="c5035-882">power of attorney</span></span>
- <span data-ttu-id="c5035-883">
registration number</span><span class="sxs-lookup"><span data-stu-id="c5035-883">registration number</span></span>
- <span data-ttu-id="c5035-884">personal health number</span><span class="sxs-lookup"><span data-stu-id="c5035-884">personal health number</span></span>
- <span data-ttu-id="c5035-885">
practitioner referral</span><span class="sxs-lookup"><span data-stu-id="c5035-885">practitioner referral</span></span>
- <span data-ttu-id="c5035-886">
wellness professional</span><span class="sxs-lookup"><span data-stu-id="c5035-886">wellness professional</span></span>
- <span data-ttu-id="c5035-887">
patient referral</span><span class="sxs-lookup"><span data-stu-id="c5035-887">patient referral</span></span>
- <span data-ttu-id="c5035-888">

health and wellness</span><span class="sxs-lookup"><span data-stu-id="c5035-888">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="c5035-889">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="c5035-889">Keyword_canada_provinces</span></span>

- <span data-ttu-id="c5035-890">Nunavut</span><span class="sxs-lookup"><span data-stu-id="c5035-890">Nunavut</span></span>
- <span data-ttu-id="c5035-891">
Quebec</span><span class="sxs-lookup"><span data-stu-id="c5035-891">Quebec</span></span>
- <span data-ttu-id="c5035-892">
Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="c5035-892">Northwest Territories</span></span>
- <span data-ttu-id="c5035-893">
Ontario</span><span class="sxs-lookup"><span data-stu-id="c5035-893">Ontario</span></span>
- <span data-ttu-id="c5035-894">
British Columbia</span><span class="sxs-lookup"><span data-stu-id="c5035-894">British Columbia</span></span>
- <span data-ttu-id="c5035-895">
Alberta</span><span class="sxs-lookup"><span data-stu-id="c5035-895">Alberta</span></span>
- <span data-ttu-id="c5035-896">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="c5035-896">Saskatchewan</span></span>
- <span data-ttu-id="c5035-897">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="c5035-897">Manitoba</span></span>
- <span data-ttu-id="c5035-898">
Yukon</span><span class="sxs-lookup"><span data-stu-id="c5035-898">Yukon</span></span>
- <span data-ttu-id="c5035-899">
Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="c5035-899">Newfoundland and Labrador</span></span>
- <span data-ttu-id="c5035-900">
New Brunswick</span><span class="sxs-lookup"><span data-stu-id="c5035-900">New Brunswick</span></span>
- <span data-ttu-id="c5035-901">
Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="c5035-901">Nova Scotia</span></span>
- <span data-ttu-id="c5035-902">
Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="c5035-902">Prince Edward Island</span></span>
- <span data-ttu-id="c5035-903">Canada</span><span class="sxs-lookup"><span data-stu-id="c5035-903">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="c5035-904">캐나다 사회 보험 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-904">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-905">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-905">Format</span></span>

<span data-ttu-id="c5035-906">선택적 하이픈 또는 공백을 포함하는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-906">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-907">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-907">Pattern</span></span>

<span data-ttu-id="c5035-908">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="c5035-908">Formatted:</span></span>
- <span data-ttu-id="c5035-909">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-909">Three digits</span></span> 
- <span data-ttu-id="c5035-910">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="c5035-910">A hyphen or space</span></span> 
- <span data-ttu-id="c5035-911">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-911">Three digits</span></span> 
- <span data-ttu-id="c5035-912">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="c5035-912">A hyphen or space</span></span> 
- <span data-ttu-id="c5035-913">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-913">Three digits</span></span>

<span data-ttu-id="c5035-914">숫자 9 개 포맷 되지 않음:</span><span class="sxs-lookup"><span data-stu-id="c5035-914">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-915">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-915">Checksum</span></span>

<span data-ttu-id="c5035-916">예</span><span class="sxs-lookup"><span data-stu-id="c5035-916">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-917">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-917">Definition</span></span>

<span data-ttu-id="c5035-918">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-918">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-919">Func_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-919">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-920">2개 이상의 다음 항목 조합:</span><span class="sxs-lookup"><span data-stu-id="c5035-920">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="c5035-921">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-921">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="c5035-922">Keyword_sin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-922">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="c5035-923">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-923">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="c5035-924">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-924">The checksum passes.</span></span>

<span data-ttu-id="c5035-925">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-925">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-926">Func_unformatted_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-926">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-927">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-927">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="c5035-928">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-928">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-929">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-929">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="c5035-930">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="c5035-930">Keyword_sin</span></span>

- <span data-ttu-id="c5035-931">sin</span><span class="sxs-lookup"><span data-stu-id="c5035-931">sin</span></span> 
- <span data-ttu-id="c5035-932">social insurance
</span><span class="sxs-lookup"><span data-stu-id="c5035-932">social insurance</span></span> 
- <span data-ttu-id="c5035-933">numero d'assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="c5035-933">numero d'assurance sociale</span></span> 
- <span data-ttu-id="c5035-934">sins
</span><span class="sxs-lookup"><span data-stu-id="c5035-934">sins</span></span> 
- <span data-ttu-id="c5035-935">ssn</span><span class="sxs-lookup"><span data-stu-id="c5035-935">ssn</span></span> 
- <span data-ttu-id="c5035-936">ssns</span><span class="sxs-lookup"><span data-stu-id="c5035-936">ssns</span></span> 
- <span data-ttu-id="c5035-937">공유 보안</span><span class="sxs-lookup"><span data-stu-id="c5035-937">social security</span></span> 
- <span data-ttu-id="c5035-938">numero d'assurance social
</span><span class="sxs-lookup"><span data-stu-id="c5035-938">numero d'assurance social</span></span> 
- <span data-ttu-id="c5035-939">국가 id 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-939">national identification number</span></span> 
- <span data-ttu-id="c5035-940">
national id</span><span class="sxs-lookup"><span data-stu-id="c5035-940">national id</span></span> 
- <span data-ttu-id="c5035-941">sin#
</span><span class="sxs-lookup"><span data-stu-id="c5035-941">sin#</span></span> 
- <span data-ttu-id="c5035-942">soc ins
</span><span class="sxs-lookup"><span data-stu-id="c5035-942">soc ins</span></span> 
- <span data-ttu-id="c5035-943">social ins
</span><span class="sxs-lookup"><span data-stu-id="c5035-943">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="c5035-944">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="c5035-944">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="c5035-945">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-945">driver's license</span></span> 
- <span data-ttu-id="c5035-946">운전 면허</span><span class="sxs-lookup"><span data-stu-id="c5035-946">drivers license</span></span> 
- <span data-ttu-id="c5035-947">드라이버의 사용권</span><span class="sxs-lookup"><span data-stu-id="c5035-947">driver's licence</span></span> 
- <span data-ttu-id="c5035-948">drivers licence</span><span class="sxs-lookup"><span data-stu-id="c5035-948">drivers licence</span></span> 
- <span data-ttu-id="c5035-949">DOB
</span><span class="sxs-lookup"><span data-stu-id="c5035-949">DOB</span></span> 
- <span data-ttu-id="c5035-950">생년월일</span><span class="sxs-lookup"><span data-stu-id="c5035-950">Birthdate</span></span> 
- <span data-ttu-id="c5035-951">생일 </span><span class="sxs-lookup"><span data-stu-id="c5035-951">Birthday</span></span> 
- <span data-ttu-id="c5035-952">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="c5035-952">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="c5035-953">	칠레 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-953">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-954">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-954">Format</span></span>

<span data-ttu-id="c5035-955">7-8 자릿수와 구분 기호 확인 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-955">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-956">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-956">Pattern</span></span>

<span data-ttu-id="c5035-957">7-8자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="c5035-957">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="c5035-958">1-2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-958">1-2 digits</span></span> 
- <span data-ttu-id="c5035-959">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-959">A period</span></span> 
- <span data-ttu-id="c5035-960">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-960">Three digits</span></span> 
- <span data-ttu-id="c5035-961">마침표 </span><span class="sxs-lookup"><span data-stu-id="c5035-961">A period</span></span> 
- <span data-ttu-id="c5035-962">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-962">Three digits</span></span> 
- <span data-ttu-id="c5035-963">대시 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-963">A dash</span></span> 
- <span data-ttu-id="c5035-964">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-964">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-965">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-965">Checksum</span></span>

<span data-ttu-id="c5035-966">예</span><span class="sxs-lookup"><span data-stu-id="c5035-966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-967">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-967">Definition</span></span>

<span data-ttu-id="c5035-968">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-969">Func_chile_id_card 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-969">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-970">Keyword_chile_id_card에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-970">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="c5035-971">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-971">The checksum passes.</span></span>

<span data-ttu-id="c5035-972">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-972">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-973">Func_chile_id_card 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-973">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-974">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-974">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-975">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-975">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="c5035-976">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="c5035-976">Keyword_chile_id_card</span></span>

- <span data-ttu-id="c5035-977">National Identification Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-977">National Identification Number</span></span> 
- <span data-ttu-id="c5035-978">Identity card</span><span class="sxs-lookup"><span data-stu-id="c5035-978">Identity card</span></span> 
- <span data-ttu-id="c5035-979">ID</span><span class="sxs-lookup"><span data-stu-id="c5035-979">ID</span></span> 
- <span data-ttu-id="c5035-980">Identification</span><span class="sxs-lookup"><span data-stu-id="c5035-980">Identification</span></span> 
- <span data-ttu-id="c5035-981">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="c5035-981">Rol Único Nacional</span></span> 
- <span data-ttu-id="c5035-982">실행</span><span class="sxs-lookup"><span data-stu-id="c5035-982">RUN</span></span> 
- <span data-ttu-id="c5035-983">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="c5035-983">Rol Único Tributario</span></span> 
- <span data-ttu-id="c5035-984">RUT
</span><span class="sxs-lookup"><span data-stu-id="c5035-984">RUT</span></span> 
- <span data-ttu-id="c5035-985">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="c5035-985">Cédula de Identidad</span></span> 
- <span data-ttu-id="c5035-986">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="c5035-986">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="c5035-987">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="c5035-987">Tarjeta de identificación</span></span> 
- <span data-ttu-id="c5035-988">Identificación
</span><span class="sxs-lookup"><span data-stu-id="c5035-988">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="c5035-989">	중국 주민 ID 카드(PRC) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-989">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-990">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-990">Format</span></span>

<span data-ttu-id="c5035-991">18자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-991">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-992">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-992">Pattern</span></span>

<span data-ttu-id="c5035-993">18자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-993">18 digits:</span></span>
- <span data-ttu-id="c5035-994">주소 코드에 해당하는 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-994">Six digits which are an address code</span></span> 
- <span data-ttu-id="c5035-995">생년월일에 해당하는 YYYYMMDD 형식의 8자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-995">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="c5035-996">주문 코드에 해당하는 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-996">Three digits which are an order code</span></span> 
- <span data-ttu-id="c5035-997">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-997">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-998">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-998">Checksum</span></span>

<span data-ttu-id="c5035-999">예</span><span class="sxs-lookup"><span data-stu-id="c5035-999">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1000">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1000">Definition</span></span>

<span data-ttu-id="c5035-1001">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1001">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1002">Func_china_resident_id 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1002">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1003">Keyword_china_resident_id에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1003">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="c5035-1004">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1004">The checksum passes.</span></span>

<span data-ttu-id="c5035-1005">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1005">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1006">Func_china_resident_id 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1006">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1007">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1007">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-1008">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1008">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="c5035-1009">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="c5035-1009">Keyword_china_resident_id</span></span>

- <span data-ttu-id="c5035-1010">Resident Identity Card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1010">Resident Identity Card</span></span> 
- <span data-ttu-id="c5035-1011">PRC
</span><span class="sxs-lookup"><span data-stu-id="c5035-1011">PRC</span></span> 
- <span data-ttu-id="c5035-1012">National Identification Card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1012">National Identification Card</span></span> 
- <span data-ttu-id="c5035-1013">身份证 </span><span class="sxs-lookup"><span data-stu-id="c5035-1013">身份证</span></span> 
- <span data-ttu-id="c5035-1014">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="c5035-1014">居民 身份证</span></span> 
- <span data-ttu-id="c5035-1015">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="c5035-1015">居民身份证</span></span> 
- <span data-ttu-id="c5035-1016">鉴定

</span><span class="sxs-lookup"><span data-stu-id="c5035-1016">鉴定</span></span> 
- <span data-ttu-id="c5035-1017">身分證 </span><span class="sxs-lookup"><span data-stu-id="c5035-1017">身分證</span></span> 
- <span data-ttu-id="c5035-1018">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="c5035-1018">居民 身份證</span></span>
- <span data-ttu-id="c5035-1019">鑑定 </span><span class="sxs-lookup"><span data-stu-id="c5035-1019">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="c5035-1020">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1020">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1021">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1021">Format</span></span>

<span data-ttu-id="c5035-1022">서식을 지정할 수는 16 자리 또는 서식이 지정 되지 않은 (dddddddddddddddd) Luhn 테스트로 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1022">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1023">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1023">Pattern</span></span>

<span data-ttu-id="c5035-1024">Visa, MasterCard, Discover Card, JCB, American Express, 상품권 및 식사권을 비롯하여 전 세계 모든 주요 브랜드 카드를 검색하는 매우 복잡하고 강력한 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1024">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1025">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1025">Checksum</span></span>

<span data-ttu-id="c5035-1026">있음(Luhn 체크섬)</span><span class="sxs-lookup"><span data-stu-id="c5035-1026">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1027">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1027">Definition</span></span>

<span data-ttu-id="c5035-1028">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1028">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1029">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1029">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1030">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1030">One of the following is true:</span></span>
    - <span data-ttu-id="c5035-1031">Keyword_cc_verification의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1031">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="c5035-1032">Keyword_cc_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1032">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="c5035-1033">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1033">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="c5035-1034">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1034">The checksum passes.</span></span>

<span data-ttu-id="c5035-1035">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1035">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1036">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1036">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1037">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1037">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-1038">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1038">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="c5035-1039">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="c5035-1039">Keyword_cc_verification</span></span>

- <span data-ttu-id="c5035-1040">card verification</span><span class="sxs-lookup"><span data-stu-id="c5035-1040">card verification</span></span>
- <span data-ttu-id="c5035-1041">card identification number</span><span class="sxs-lookup"><span data-stu-id="c5035-1041">card identification number</span></span>
- <span data-ttu-id="c5035-1042">cvn
</span><span class="sxs-lookup"><span data-stu-id="c5035-1042">cvn</span></span>
- <span data-ttu-id="c5035-1043">cid
</span><span class="sxs-lookup"><span data-stu-id="c5035-1043">cid</span></span>
- <span data-ttu-id="c5035-1044">cvc2</span><span class="sxs-lookup"><span data-stu-id="c5035-1044">cvc2</span></span>
- <span data-ttu-id="c5035-1045">cvv2</span><span class="sxs-lookup"><span data-stu-id="c5035-1045">cvv2</span></span>
- <span data-ttu-id="c5035-1046">pin block
</span><span class="sxs-lookup"><span data-stu-id="c5035-1046">pin block</span></span>
- <span data-ttu-id="c5035-1047">security code
</span><span class="sxs-lookup"><span data-stu-id="c5035-1047">security code</span></span>
- <span data-ttu-id="c5035-1048">security number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1048">security number</span></span>
- <span data-ttu-id="c5035-1049">security no
</span><span class="sxs-lookup"><span data-stu-id="c5035-1049">security no</span></span>
- <span data-ttu-id="c5035-1050">issue number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1050">issue number</span></span>
- <span data-ttu-id="c5035-1051">issue no
</span><span class="sxs-lookup"><span data-stu-id="c5035-1051">issue no</span></span>
- <span data-ttu-id="c5035-1052">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="c5035-1052">cryptogramme</span></span>
- <span data-ttu-id="c5035-1053">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="c5035-1053">numéro de sécurité</span></span>
- <span data-ttu-id="c5035-1054">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="c5035-1054">numero de securite</span></span>
- <span data-ttu-id="c5035-1055">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1055">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="c5035-1056">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1056">kreditkartenprufnummer</span></span>
- <span data-ttu-id="c5035-1057">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1057">prüfziffer</span></span>
- <span data-ttu-id="c5035-1058">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1058">prufziffer</span></span>
- <span data-ttu-id="c5035-1059">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="c5035-1059">sicherheits Kode</span></span>
- <span data-ttu-id="c5035-1060">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="c5035-1060">sicherheitscode</span></span>
- <span data-ttu-id="c5035-1061">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1061">sicherheitsnummer</span></span>
- <span data-ttu-id="c5035-1062">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1062">verfalldatum</span></span>
- <span data-ttu-id="c5035-1063">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="c5035-1063">codice di verifica</span></span>
- <span data-ttu-id="c5035-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="c5035-p105">cod. sicurezza</span></span>
- <span data-ttu-id="c5035-1066">코드 sicurezza</span><span class="sxs-lookup"><span data-stu-id="c5035-1066">cod sicurezza</span></span>
- <span data-ttu-id="c5035-1067">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="c5035-1067">n autorizzazione</span></span>
- <span data-ttu-id="c5035-1068">código
</span><span class="sxs-lookup"><span data-stu-id="c5035-1068">código</span></span>
- <span data-ttu-id="c5035-1069">codigo
</span><span class="sxs-lookup"><span data-stu-id="c5035-1069">codigo</span></span>
- <span data-ttu-id="c5035-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="c5035-p106">cod. seg</span></span>
- <span data-ttu-id="c5035-1072">코드 seg</span><span class="sxs-lookup"><span data-stu-id="c5035-1072">cod seg</span></span>
- <span data-ttu-id="c5035-1073">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="c5035-1073">código de segurança</span></span>
- <span data-ttu-id="c5035-1074">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="c5035-1074">codigo de seguranca</span></span>
- <span data-ttu-id="c5035-1075">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="c5035-1075">codigo de segurança</span></span>
- <span data-ttu-id="c5035-1076">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="c5035-1076">código de seguranca</span></span>
- <span data-ttu-id="c5035-p107">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="c5035-p107">cód. segurança</span></span>
- <span data-ttu-id="c5035-p108">코드입니다. 브라질어 코드입니다. segurança</span><span class="sxs-lookup"><span data-stu-id="c5035-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="c5035-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="c5035-p109">cód. seguranca</span></span>
- <span data-ttu-id="c5035-1084">cód segurança</span><span class="sxs-lookup"><span data-stu-id="c5035-1084">cód segurança</span></span>
- <span data-ttu-id="c5035-1085">브라질어 코드 segurança 대구</span><span class="sxs-lookup"><span data-stu-id="c5035-1085">cod seguranca cod segurança</span></span>
- <span data-ttu-id="c5035-1086">cód 브라질어</span><span class="sxs-lookup"><span data-stu-id="c5035-1086">cód seguranca</span></span>
- <span data-ttu-id="c5035-1087">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="c5035-1087">número de verificação</span></span>
- <span data-ttu-id="c5035-1088">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1088">numero de verificacao</span></span>
- <span data-ttu-id="c5035-1089">ablauf
</span><span class="sxs-lookup"><span data-stu-id="c5035-1089">ablauf</span></span>
- <span data-ttu-id="c5035-1090">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="c5035-1090">gültig bis</span></span>
- <span data-ttu-id="c5035-1091">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1091">gültigkeitsdatum</span></span>
- <span data-ttu-id="c5035-1092">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="c5035-1092">gultig bis</span></span>
- <span data-ttu-id="c5035-1093">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1093">gultigkeitsdatum</span></span>
- <span data-ttu-id="c5035-1094">scadenza
</span><span class="sxs-lookup"><span data-stu-id="c5035-1094">scadenza</span></span>
- <span data-ttu-id="c5035-1095">data scad
</span><span class="sxs-lookup"><span data-stu-id="c5035-1095">data scad</span></span>
- <span data-ttu-id="c5035-1096">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="c5035-1096">fecha de expiracion</span></span>
- <span data-ttu-id="c5035-1097">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="c5035-1097">fecha de venc</span></span>
- <span data-ttu-id="c5035-1098">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="c5035-1098">vencimiento</span></span>
- <span data-ttu-id="c5035-1099">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1099">válido hasta</span></span>
- <span data-ttu-id="c5035-1100">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1100">valido hasta</span></span>
- <span data-ttu-id="c5035-1101">vto
</span><span class="sxs-lookup"><span data-stu-id="c5035-1101">vto</span></span>
- <span data-ttu-id="c5035-1102">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="c5035-1102">data de expiração</span></span>
- <span data-ttu-id="c5035-1103">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1103">data de expiracao</span></span>
- <span data-ttu-id="c5035-1104">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="c5035-1104">data em que expira</span></span>
- <span data-ttu-id="c5035-1105">validade
</span><span class="sxs-lookup"><span data-stu-id="c5035-1105">validade</span></span>
- <span data-ttu-id="c5035-1106">valor
</span><span class="sxs-lookup"><span data-stu-id="c5035-1106">valor</span></span>
- <span data-ttu-id="c5035-1107">vencimento
</span><span class="sxs-lookup"><span data-stu-id="c5035-1107">vencimento</span></span>
- <span data-ttu-id="c5035-1108">Venc</span><span class="sxs-lookup"><span data-stu-id="c5035-1108">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="c5035-1109">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="c5035-1109">Keyword_cc_name</span></span>

- <span data-ttu-id="c5035-1110">amex</span><span class="sxs-lookup"><span data-stu-id="c5035-1110">amex</span></span>
- <span data-ttu-id="c5035-1111">
american express</span><span class="sxs-lookup"><span data-stu-id="c5035-1111">american express</span></span>
- <span data-ttu-id="c5035-1112">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="c5035-1112">americanexpress</span></span>
- <span data-ttu-id="c5035-1113">Visa</span><span class="sxs-lookup"><span data-stu-id="c5035-1113">Visa</span></span>
- <span data-ttu-id="c5035-1114">mastercard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1114">mastercard</span></span>
- <span data-ttu-id="c5035-1115">master card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1115">master card</span></span>
- <span data-ttu-id="c5035-1116">
mc
</span><span class="sxs-lookup"><span data-stu-id="c5035-1116">mc</span></span> 
- <span data-ttu-id="c5035-1117">mastercards</span><span class="sxs-lookup"><span data-stu-id="c5035-1117">mastercards</span></span>
- <span data-ttu-id="c5035-1118">
master cards</span><span class="sxs-lookup"><span data-stu-id="c5035-1118">master cards</span></span>
- <span data-ttu-id="c5035-1119">diner의 클럽</span><span class="sxs-lookup"><span data-stu-id="c5035-1119">diner's Club</span></span>
- <span data-ttu-id="c5035-1120">diners club
</span><span class="sxs-lookup"><span data-stu-id="c5035-1120">diners club</span></span>
- <span data-ttu-id="c5035-1121">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="c5035-1121">dinersclub</span></span>
- <span data-ttu-id="c5035-1122">discover card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1122">discover card</span></span>
- <span data-ttu-id="c5035-1123">discovercard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1123">discovercard</span></span>
- <span data-ttu-id="c5035-1124">discover cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1124">discover cards</span></span>
- <span data-ttu-id="c5035-1125">JCB</span><span class="sxs-lookup"><span data-stu-id="c5035-1125">JCB</span></span>
- <span data-ttu-id="c5035-1126">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="c5035-1126">japanese card bureau</span></span>
- <span data-ttu-id="c5035-1127">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="c5035-1127">carte blanche</span></span>
- <span data-ttu-id="c5035-1128">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="c5035-1128">carteblanche</span></span>
- <span data-ttu-id="c5035-1129">credit card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1129">credit card</span></span>
- <span data-ttu-id="c5035-1130">cc #</span><span class="sxs-lookup"><span data-stu-id="c5035-1130">cc#</span></span>
- <span data-ttu-id="c5035-1131">cc #의 경우:</span><span class="sxs-lookup"><span data-stu-id="c5035-1131">cc#:</span></span>
- <span data-ttu-id="c5035-1132">
expiration date</span><span class="sxs-lookup"><span data-stu-id="c5035-1132">expiration date</span></span>
- <span data-ttu-id="c5035-1133">exp date
</span><span class="sxs-lookup"><span data-stu-id="c5035-1133">exp date</span></span>
- <span data-ttu-id="c5035-1134">
expiry date</span><span class="sxs-lookup"><span data-stu-id="c5035-1134">expiry date</span></span>
- <span data-ttu-id="c5035-1135">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="c5035-1135">date d’expiration</span></span>
- <span data-ttu-id="c5035-1136">
date d'exp</span><span class="sxs-lookup"><span data-stu-id="c5035-1136">date d'exp</span></span>
- <span data-ttu-id="c5035-1137">
date expiration</span><span class="sxs-lookup"><span data-stu-id="c5035-1137">date expiration</span></span>
- <span data-ttu-id="c5035-1138">bank card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1138">bank card</span></span>
- <span data-ttu-id="c5035-1139">
bankcard</span><span class="sxs-lookup"><span data-stu-id="c5035-1139">bankcard</span></span>
- <span data-ttu-id="c5035-1140">card number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1140">card number</span></span>
- <span data-ttu-id="c5035-1141">card num
</span><span class="sxs-lookup"><span data-stu-id="c5035-1141">card num</span></span>
- <span data-ttu-id="c5035-1142">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-1142">cardnumber</span></span>
- <span data-ttu-id="c5035-1143">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="c5035-1143">cardnumbers</span></span>
- <span data-ttu-id="c5035-1144">card numbers
</span><span class="sxs-lookup"><span data-stu-id="c5035-1144">card numbers</span></span>
- <span data-ttu-id="c5035-1145">creditcard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1145">creditcard</span></span>
- <span data-ttu-id="c5035-1146">credit cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1146">credit cards</span></span>
- <span data-ttu-id="c5035-1147">creditcards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1147">creditcards</span></span>
- <span data-ttu-id="c5035-1148">ccn
</span><span class="sxs-lookup"><span data-stu-id="c5035-1148">ccn</span></span>
- <span data-ttu-id="c5035-1149">card holder
</span><span class="sxs-lookup"><span data-stu-id="c5035-1149">card holder</span></span>
- <span data-ttu-id="c5035-1150">cardholder
</span><span class="sxs-lookup"><span data-stu-id="c5035-1150">cardholder</span></span>
- <span data-ttu-id="c5035-1151">card holders
</span><span class="sxs-lookup"><span data-stu-id="c5035-1151">card holders</span></span>
- <span data-ttu-id="c5035-1152">cardholders
</span><span class="sxs-lookup"><span data-stu-id="c5035-1152">cardholders</span></span>
- <span data-ttu-id="c5035-1153">check card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1153">check card</span></span>
- <span data-ttu-id="c5035-1154">checkcard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1154">checkcard</span></span>
- <span data-ttu-id="c5035-1155">check cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1155">check cards</span></span>
- <span data-ttu-id="c5035-1156">checkcards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1156">checkcards</span></span>
- <span data-ttu-id="c5035-1157">debit card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1157">debit card</span></span>
- <span data-ttu-id="c5035-1158">debitcard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1158">debitcard</span></span>
- <span data-ttu-id="c5035-1159">debit cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1159">debit cards</span></span>
- <span data-ttu-id="c5035-1160">debitcards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1160">debitcards</span></span>
- <span data-ttu-id="c5035-1161">atm card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1161">atm card</span></span>
- <span data-ttu-id="c5035-1162">atmcard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1162">atmcard</span></span>
- <span data-ttu-id="c5035-1163">atm cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1163">atm cards</span></span>
- <span data-ttu-id="c5035-1164">atmcards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1164">atmcards</span></span>
- <span data-ttu-id="c5035-1165">
enroute</span><span class="sxs-lookup"><span data-stu-id="c5035-1165">enroute</span></span>
- <span data-ttu-id="c5035-1166">
en route</span><span class="sxs-lookup"><span data-stu-id="c5035-1166">en route</span></span>
- <span data-ttu-id="c5035-1167">card type
</span><span class="sxs-lookup"><span data-stu-id="c5035-1167">card type</span></span>
- <span data-ttu-id="c5035-1168">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="c5035-1168">carte bancaire</span></span>
- <span data-ttu-id="c5035-1169">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="c5035-1169">carte de crédit</span></span>
- <span data-ttu-id="c5035-1170">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="c5035-1170">carte de credit</span></span>
- <span data-ttu-id="c5035-1171">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1171">numéro de carte</span></span>
- <span data-ttu-id="c5035-1172">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1172">numero de carte</span></span>
- <span data-ttu-id="c5035-1173">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1173">nº de la carte</span></span>
- <span data-ttu-id="c5035-1174">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1174">nº de carte</span></span>
- <span data-ttu-id="c5035-1175">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1175">kreditkarte</span></span>
- <span data-ttu-id="c5035-1176">karte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1176">karte</span></span>
- <span data-ttu-id="c5035-1177">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="c5035-1177">karteninhaber</span></span>
- <span data-ttu-id="c5035-1178">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="c5035-1178">karteninhabers</span></span>
- <span data-ttu-id="c5035-1179">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="c5035-1179">kreditkarteninhaber</span></span>
- <span data-ttu-id="c5035-1180">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="c5035-1180">kreditkarteninstitut</span></span>
- <span data-ttu-id="c5035-1181">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="c5035-1181">kreditkartentyp</span></span>
- <span data-ttu-id="c5035-1182">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="c5035-1182">eigentümername</span></span>
- <span data-ttu-id="c5035-1183">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1183">kartennr</span></span> 
- <span data-ttu-id="c5035-1184">kartennummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1184">kartennummer</span></span>
- <span data-ttu-id="c5035-1185">
kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1185">kreditkartennummer</span></span>
- <span data-ttu-id="c5035-1186">kreditkarten nummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1186">kreditkarten-nummer</span></span>
- <span data-ttu-id="c5035-1187">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1187">carta di credito</span></span>
- <span data-ttu-id="c5035-1188">carta credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1188">carta credito</span></span>
- <span data-ttu-id="c5035-1189">carta</span><span class="sxs-lookup"><span data-stu-id="c5035-1189">carta</span></span>
- <span data-ttu-id="c5035-1190">n carta</span><span class="sxs-lookup"><span data-stu-id="c5035-1190">n carta</span></span>
- <span data-ttu-id="c5035-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-p110">nr. carta</span></span>
- <span data-ttu-id="c5035-1193">nr carta</span><span class="sxs-lookup"><span data-stu-id="c5035-1193">nr carta</span></span>
- <span data-ttu-id="c5035-1194">numero carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1194">numero carta</span></span>
- <span data-ttu-id="c5035-1195">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1195">numero della carta</span></span>
- <span data-ttu-id="c5035-1196">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1196">numero di carta</span></span>
- <span data-ttu-id="c5035-1197">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1197">tarjeta credito</span></span>
- <span data-ttu-id="c5035-1198">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1198">tarjeta de credito</span></span>
- <span data-ttu-id="c5035-1199">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="c5035-1199">tarjeta crédito</span></span>
- <span data-ttu-id="c5035-1200">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="c5035-1200">tarjeta de crédito</span></span>
- <span data-ttu-id="c5035-1201">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="c5035-1201">tarjeta de atm</span></span>
- <span data-ttu-id="c5035-1202">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="c5035-1202">tarjeta atm</span></span>
- <span data-ttu-id="c5035-1203">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1203">tarjeta debito</span></span>
- <span data-ttu-id="c5035-1204">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1204">tarjeta de debito</span></span>
- <span data-ttu-id="c5035-1205">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="c5035-1205">tarjeta débito</span></span>
- <span data-ttu-id="c5035-1206">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="c5035-1206">tarjeta de débito</span></span>
- <span data-ttu-id="c5035-1207">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1207">nº de tarjeta</span></span>
- <span data-ttu-id="c5035-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="c5035-p111">no. de tarjeta</span></span>
- <span data-ttu-id="c5035-1210">de tarjeta 없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1210">no de tarjeta</span></span>
- <span data-ttu-id="c5035-1211">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1211">numero de tarjeta</span></span>
- <span data-ttu-id="c5035-1212">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1212">número de tarjeta</span></span>
- <span data-ttu-id="c5035-1213">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="c5035-1213">tarjeta no</span></span>
- <span data-ttu-id="c5035-1214">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="c5035-1214">tarjetahabiente</span></span>
- <span data-ttu-id="c5035-1215">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1215">cartão de crédito</span></span>
- <span data-ttu-id="c5035-1216">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1216">cartão de credito</span></span>
- <span data-ttu-id="c5035-1217">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1217">cartao de crédito</span></span>
- <span data-ttu-id="c5035-1218">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1218">cartao de credito</span></span>
- <span data-ttu-id="c5035-1219">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1219">cartão de débito</span></span>
- <span data-ttu-id="c5035-1220">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1220">cartao de débito</span></span>
- <span data-ttu-id="c5035-1221">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1221">cartão de debito</span></span>
- <span data-ttu-id="c5035-1222">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1222">cartao de debito</span></span>
- <span data-ttu-id="c5035-1223">débito automático</span><span class="sxs-lookup"><span data-stu-id="c5035-1223">débito automático</span></span>
- <span data-ttu-id="c5035-1224">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="c5035-1224">debito automatico</span></span>
- <span data-ttu-id="c5035-1225">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="c5035-1225">número do cartão</span></span>
- <span data-ttu-id="c5035-1226">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-1226">numero do cartão</span></span> 
- <span data-ttu-id="c5035-1227">número do cartao</span><span class="sxs-lookup"><span data-stu-id="c5035-1227">número do cartao</span></span>
- <span data-ttu-id="c5035-1228">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="c5035-1228">numero do cartao</span></span>
- <span data-ttu-id="c5035-1229">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-1229">número de cartão</span></span>
- <span data-ttu-id="c5035-1230">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-1230">numero de cartão</span></span>
- <span data-ttu-id="c5035-1231">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1231">número de cartao</span></span>
- <span data-ttu-id="c5035-1232">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1232">numero de cartao</span></span>
- <span data-ttu-id="c5035-1233">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="c5035-1233">nº do cartão</span></span>
- <span data-ttu-id="c5035-1234">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1234">nº do cartao</span></span>
- <span data-ttu-id="c5035-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-p112">nº. do cartão</span></span>
- <span data-ttu-id="c5035-1237">do cartão 없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1237">no do cartão</span></span>
- <span data-ttu-id="c5035-1238">do cartao 없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1238">no do cartao</span></span>
- <span data-ttu-id="c5035-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-p113">no. do cartão</span></span>
- <span data-ttu-id="c5035-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="c5035-1243">	크로아티아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1243">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1244">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1244">Format</span></span>

<span data-ttu-id="c5035-1245">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1245">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1246">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1246">Pattern</span></span>

<span data-ttu-id="c5035-1247">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1247">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1248">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1248">Checksum</span></span>

<span data-ttu-id="c5035-1249">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1249">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1250">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1250">Definition</span></span>

<span data-ttu-id="c5035-1251">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1251">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1252">Func_croatia_id_card 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1252">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1253">Keyword_croatia_id_card에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1253">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-1254">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1254">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="c5035-1255">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="c5035-1255">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="c5035-1256">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="c5035-1256">Croatian identity card</span></span>
- <span data-ttu-id="c5035-1257">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="c5035-1257">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="c5035-1258">	크로아티아 개인 식별(OIB) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1258">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1259">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1259">Format</span></span>

<span data-ttu-id="c5035-1260">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1260">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1261">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1261">Pattern</span></span>

<span data-ttu-id="c5035-1262">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-1262">10 digits:</span></span>
- <span data-ttu-id="c5035-1263">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1263">Six digits in the form DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="c5035-1264">마지막 숫자가 검사 숫자인 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1264">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1265">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1265">Checksum</span></span>

<span data-ttu-id="c5035-1266">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1266">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1267">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1267">Definition</span></span>

<span data-ttu-id="c5035-1268">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1268">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1269">Func_croatia_oib_number 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1269">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1270">Keyword_croatia_oib_number에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1270">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="c5035-1271">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1271">The checksum passes.</span></span>

<span data-ttu-id="c5035-1272">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1272">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1273">Func_croatia_oib_number 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1273">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1274">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1274">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-1275">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1275">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="c5035-1276">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="c5035-1276">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="c5035-1277">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="c5035-1277">Personal Identification Number</span></span>
- <span data-ttu-id="c5035-1278">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="c5035-1278">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="c5035-1279">OIB
</span><span class="sxs-lookup"><span data-stu-id="c5035-1279">OIB</span></span> 

   
## <a name="czech-national-identity-card-number"></a><span data-ttu-id="c5035-1280">	체코 국가 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1280">Czech National Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1281">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1281">Format</span></span>

<span data-ttu-id="c5035-1282">정방향 슬래시를 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1282">10 digits containing a forward slash</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1283">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1283">Pattern</span></span>

<span data-ttu-id="c5035-1284">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-1284">10 digits:</span></span>
- <span data-ttu-id="c5035-1285">생년월일에 해당하는 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1285">Six digits which are the date of birth</span></span> 
- <span data-ttu-id="c5035-1286">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="c5035-1286">A forward slash</span></span> 
- <span data-ttu-id="c5035-1287">마지막 숫자가 검사 숫자인 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1287">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1288">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1288">Checksum</span></span>

<span data-ttu-id="c5035-1289">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1289">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1290">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1290">Definition</span></span>

<span data-ttu-id="c5035-p115">DLP 정책은 이러한 종류의 중요 한 정보를 감지 했습니다 판단 85%에 근접 300 자 내에 있는 경우,: Func_czech_id_card 함수는 패턴과 일치 하는 콘텐츠를 찾습니다. Keyword_czech_id_card에서 키워드를 발견 됩니다. 체크섬을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech National Identity Card Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_czech_id_card"/>
     <Match idRef="Keyword_czech_id_card"/>
  </Pattern>
</Entity>
```


### <a name="keywords"></a><span data-ttu-id="c5035-1294">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1294">Keywords</span></span>

- <span data-ttu-id="c5035-1295">Keyword_czech_id_card</span><span class="sxs-lookup"><span data-stu-id="c5035-1295">Keyword_czech_id_card</span></span>
- <span data-ttu-id="c5035-1296">Czech national identity card</span><span class="sxs-lookup"><span data-stu-id="c5035-1296">Czech national identity card</span></span>
- <span data-ttu-id="c5035-1297">Občanský průka</span><span class="sxs-lookup"><span data-stu-id="c5035-1297">Občanský průka</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="c5035-1298">	덴마크 개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1298">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1299">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1299">Format</span></span>

<span data-ttu-id="c5035-1300">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1300">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1301">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1301">Pattern</span></span>

<span data-ttu-id="c5035-1302">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-1302">10 digits:</span></span>
- <span data-ttu-id="c5035-1303">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-1303">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="c5035-1304">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-1304">A hyphen</span></span> 
- <span data-ttu-id="c5035-1305">마지막 숫자가 검사 숫자인 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1305">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1306">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1306">Checksum</span></span>

<span data-ttu-id="c5035-1307">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1307">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1308">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1308">Definition</span></span>

<span data-ttu-id="c5035-p116">DLP 정책은 이러한 종류의 중요 한 정보를 감지 했습니다 판단 75%에 근접 300 자 내에 있는 경우,: Regex_denmark_id 정규식 패턴과 일치 하는 콘텐츠를 찾습니다. Keyword_denmark_id에서 키워드를 발견 됩니다. 체크섬을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-1312">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1312">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="c5035-1313">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="c5035-1313">Keyword_denmark_id</span></span>

- <span data-ttu-id="c5035-1314">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="c5035-1314">Personal Identification Number</span></span>
- <span data-ttu-id="c5035-1315">CPR</span><span class="sxs-lookup"><span data-stu-id="c5035-1315">CPR</span></span>
- <span data-ttu-id="c5035-1316">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="c5035-1316">Det Centrale Personregister</span></span>
- <span data-ttu-id="c5035-1317">Personnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1317">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="c5035-1318">DEA(약물 집행 기구) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1318">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1319">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1319">Format</span></span>

<span data-ttu-id="c5035-1320">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1320">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1321">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1321">Pattern</span></span>

<span data-ttu-id="c5035-1322">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1322">Pattern must include all of the following:</span></span>
- <span data-ttu-id="c5035-1323">등록 코드에 해당하는 abcdefghjklmnprstux 중 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-1323">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="c5035-1324">등록자 성의 첫 문자에 해당하는 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-1324">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="c5035-1325">검사 숫자의 마지막 7개 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1325">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1326">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1326">Checksum</span></span>

<span data-ttu-id="c5035-1327">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1327">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1328">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1328">Definition</span></span>

<span data-ttu-id="c5035-1329">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1329">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1330">Func_dea_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1330">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1331">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1331">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-1332">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1332">Keywords</span></span>

<span data-ttu-id="c5035-1333">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1333">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="c5035-1334">유럽 직불 카드 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1334">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1335">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1335">Format</span></span>

<span data-ttu-id="c5035-1336">16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1336">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1337">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1337">Pattern</span></span>

<span data-ttu-id="c5035-1338">매우 복잡하고 강력한 패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1338">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1339">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1339">Checksum</span></span>

<span data-ttu-id="c5035-1340">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1340">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1341">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1341">Definition</span></span>

<span data-ttu-id="c5035-1342">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1343">Func_eu_debit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1343">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1344">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1344">At least one of the following is true:</span></span>
    - <span data-ttu-id="c5035-1345">Keyword_eu_debit_card의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1345">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="c5035-1346">Keyword_card_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1346">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="c5035-1347">Keyword_card_security_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1347">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="c5035-1348">Keyword_card_expiration_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1348">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="c5035-1349">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1349">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="c5035-1350">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1350">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-1351">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1351">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="c5035-1352">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="c5035-1352">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="c5035-1353">계좌 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1353">account number</span></span> 
- <span data-ttu-id="c5035-1354">card number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1354">card number</span></span> 
- <span data-ttu-id="c5035-1355">card no.
</span><span class="sxs-lookup"><span data-stu-id="c5035-1355">card no.</span></span> 
- <span data-ttu-id="c5035-1356">security number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1356">security number</span></span> 
- <span data-ttu-id="c5035-1357">cc #</span><span class="sxs-lookup"><span data-stu-id="c5035-1357">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="c5035-1358">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="c5035-1358">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="c5035-1359">acct nbr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1359">acct nbr</span></span> 
- <span data-ttu-id="c5035-1360">acct num
</span><span class="sxs-lookup"><span data-stu-id="c5035-1360">acct num</span></span> 
- <span data-ttu-id="c5035-1361">acct no
</span><span class="sxs-lookup"><span data-stu-id="c5035-1361">acct no</span></span> 
- <span data-ttu-id="c5035-1362">american express
</span><span class="sxs-lookup"><span data-stu-id="c5035-1362">american express</span></span> 
- <span data-ttu-id="c5035-1363">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="c5035-1363">americanexpress</span></span> 
- <span data-ttu-id="c5035-1364">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="c5035-1364">americano espresso</span></span> 
- <span data-ttu-id="c5035-1365">amex</span><span class="sxs-lookup"><span data-stu-id="c5035-1365">amex</span></span> 
- <span data-ttu-id="c5035-1366">atm card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1366">atm card</span></span> 
- <span data-ttu-id="c5035-1367">atm cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1367">atm cards</span></span> 
- <span data-ttu-id="c5035-1368">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="c5035-1368">atm kaart</span></span> 
- <span data-ttu-id="c5035-1369">atmcard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1369">atmcard</span></span> 
- <span data-ttu-id="c5035-1370">atmcards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1370">atmcards</span></span> 
- <span data-ttu-id="c5035-1371">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="c5035-1371">atmkaart</span></span> 
- <span data-ttu-id="c5035-1372">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="c5035-1372">atmkaarten</span></span> 
- <span data-ttu-id="c5035-1373">bancontact
</span><span class="sxs-lookup"><span data-stu-id="c5035-1373">bancontact</span></span> 
- <span data-ttu-id="c5035-1374">bank card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1374">bank card</span></span> 
- <span data-ttu-id="c5035-1375">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="c5035-1375">bankkaart</span></span> 
- <span data-ttu-id="c5035-1376">card holder
</span><span class="sxs-lookup"><span data-stu-id="c5035-1376">card holder</span></span> 
- <span data-ttu-id="c5035-1377">card holders
</span><span class="sxs-lookup"><span data-stu-id="c5035-1377">card holders</span></span> 
- <span data-ttu-id="c5035-1378">card num
</span><span class="sxs-lookup"><span data-stu-id="c5035-1378">card num</span></span> 
- <span data-ttu-id="c5035-1379">card number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1379">card number</span></span> 
- <span data-ttu-id="c5035-1380">card numbers
</span><span class="sxs-lookup"><span data-stu-id="c5035-1380">card numbers</span></span> 
- <span data-ttu-id="c5035-1381">card type
</span><span class="sxs-lookup"><span data-stu-id="c5035-1381">card type</span></span> 
- <span data-ttu-id="c5035-1382">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="c5035-1382">cardano numerico</span></span> 
- <span data-ttu-id="c5035-1383">cardholder
</span><span class="sxs-lookup"><span data-stu-id="c5035-1383">cardholder</span></span> 
- <span data-ttu-id="c5035-1384">cardholders
</span><span class="sxs-lookup"><span data-stu-id="c5035-1384">cardholders</span></span> 
- <span data-ttu-id="c5035-1385">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-1385">cardnumber</span></span> 
- <span data-ttu-id="c5035-1386">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="c5035-1386">cardnumbers</span></span> 
- <span data-ttu-id="c5035-1387">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="c5035-1387">carta bianca</span></span> 
- <span data-ttu-id="c5035-1388">carta credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1388">carta credito</span></span> 
- <span data-ttu-id="c5035-1389">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1389">carta di credito</span></span> 
- <span data-ttu-id="c5035-1390">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1390">cartao de credito</span></span> 
- <span data-ttu-id="c5035-1391">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1391">cartao de crédito</span></span> 
- <span data-ttu-id="c5035-1392">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1392">cartao de debito</span></span> 
- <span data-ttu-id="c5035-1393">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1393">cartao de débito</span></span> 
- <span data-ttu-id="c5035-1394">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="c5035-1394">carte bancaire</span></span> 
- <span data-ttu-id="c5035-1395">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="c5035-1395">carte blanche</span></span> 
- <span data-ttu-id="c5035-1396">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="c5035-1396">carte bleue</span></span> 
- <span data-ttu-id="c5035-1397">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="c5035-1397">carte de credit</span></span> 
- <span data-ttu-id="c5035-1398">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="c5035-1398">carte de crédit</span></span> 
- <span data-ttu-id="c5035-1399">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1399">carte di credito</span></span> 
- <span data-ttu-id="c5035-1400">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="c5035-1400">carteblanche</span></span> 
- <span data-ttu-id="c5035-1401">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1401">cartão de credito</span></span> 
- <span data-ttu-id="c5035-1402">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1402">cartão de crédito</span></span> 
- <span data-ttu-id="c5035-1403">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1403">cartão de debito</span></span> 
- <span data-ttu-id="c5035-1404">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1404">cartão de débito</span></span> 
- <span data-ttu-id="c5035-1405">cb
</span><span class="sxs-lookup"><span data-stu-id="c5035-1405">cb</span></span> 
- <span data-ttu-id="c5035-1406">ccn
</span><span class="sxs-lookup"><span data-stu-id="c5035-1406">ccn</span></span> 
- <span data-ttu-id="c5035-1407">check card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1407">check card</span></span> 
- <span data-ttu-id="c5035-1408">check cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1408">check cards</span></span> 
- <span data-ttu-id="c5035-1409">checkcard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1409">checkcard</span></span>
- <span data-ttu-id="c5035-1410">checkcards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1410">checkcards</span></span> 
- <span data-ttu-id="c5035-1411">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="c5035-1411">chequekaart</span></span> 
- <span data-ttu-id="c5035-1412">cirrus
</span><span class="sxs-lookup"><span data-stu-id="c5035-1412">cirrus</span></span> 
- <span data-ttu-id="c5035-1413">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="c5035-1413">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="c5035-1414">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="c5035-1414">controlekaart</span></span> 
- <span data-ttu-id="c5035-1415">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="c5035-1415">controlekaarten</span></span> 
- <span data-ttu-id="c5035-1416">credit card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1416">credit card</span></span> 
- <span data-ttu-id="c5035-1417">credit cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1417">credit cards</span></span> 
- <span data-ttu-id="c5035-1418">creditcard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1418">creditcard</span></span> 
- <span data-ttu-id="c5035-1419">creditcards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1419">creditcards</span></span> 
- <span data-ttu-id="c5035-1420">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="c5035-1420">debetkaart</span></span> 
- <span data-ttu-id="c5035-1421">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="c5035-1421">debetkaarten</span></span> 
- <span data-ttu-id="c5035-1422">debit card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1422">debit card</span></span> 
- <span data-ttu-id="c5035-1423">debit cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1423">debit cards</span></span> 
- <span data-ttu-id="c5035-1424">debitcard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1424">debitcard</span></span> 
- <span data-ttu-id="c5035-1425">debitcards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1425">debitcards</span></span> 
- <span data-ttu-id="c5035-1426">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="c5035-1426">debito automatico</span></span> 
- <span data-ttu-id="c5035-1427">diners club
</span><span class="sxs-lookup"><span data-stu-id="c5035-1427">diners club</span></span> 
- <span data-ttu-id="c5035-1428">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="c5035-1428">dinersclub</span></span> 
- <span data-ttu-id="c5035-1429">검색</span><span class="sxs-lookup"><span data-stu-id="c5035-1429">discover</span></span> 
- <span data-ttu-id="c5035-1430">discover card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1430">discover card</span></span> 
- <span data-ttu-id="c5035-1431">discover cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1431">discover cards</span></span> 
- <span data-ttu-id="c5035-1432">discovercard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1432">discovercard</span></span> 
- <span data-ttu-id="c5035-1433">discovercards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1433">discovercards</span></span> 
- <span data-ttu-id="c5035-1434">débito automático</span><span class="sxs-lookup"><span data-stu-id="c5035-1434">débito automático</span></span>
- <span data-ttu-id="c5035-1435">
edc
</span><span class="sxs-lookup"><span data-stu-id="c5035-1435">edc</span></span> 
- <span data-ttu-id="c5035-1436">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="c5035-1436">eigentümername</span></span> 
- <span data-ttu-id="c5035-1437">european debit card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1437">european debit card</span></span> 
- <span data-ttu-id="c5035-1438">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="c5035-1438">hoofdkaart</span></span> 
- <span data-ttu-id="c5035-1439">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="c5035-1439">hoofdkaarten</span></span> 
- <span data-ttu-id="c5035-1440">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="c5035-1440">in viaggio</span></span> 
- <span data-ttu-id="c5035-1441">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="c5035-1441">japanese card bureau</span></span> 
- <span data-ttu-id="c5035-1442">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="c5035-1442">japanse kaartdienst</span></span> 
- <span data-ttu-id="c5035-1443">jcb
</span><span class="sxs-lookup"><span data-stu-id="c5035-1443">jcb</span></span> 
- <span data-ttu-id="c5035-1444">kaart
</span><span class="sxs-lookup"><span data-stu-id="c5035-1444">kaart</span></span> 
- <span data-ttu-id="c5035-1445">kaart num
</span><span class="sxs-lookup"><span data-stu-id="c5035-1445">kaart num</span></span> 
- <span data-ttu-id="c5035-1446">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="c5035-1446">kaartaantal</span></span> 
- <span data-ttu-id="c5035-1447">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="c5035-1447">kaartaantallen</span></span> 
- <span data-ttu-id="c5035-1448">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="c5035-1448">kaarthouder</span></span> 
- <span data-ttu-id="c5035-1449">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="c5035-1449">kaarthouders</span></span> 
- <span data-ttu-id="c5035-1450">karte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1450">karte</span></span>  
- <span data-ttu-id="c5035-1451">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="c5035-1451">karteninhaber</span></span> 
- <span data-ttu-id="c5035-1452">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="c5035-1452">karteninhabers</span></span>
- <span data-ttu-id="c5035-1453">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1453">kartennr</span></span> 
- <span data-ttu-id="c5035-1454">kartennummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1454">kartennummer</span></span> 
- <span data-ttu-id="c5035-1455">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1455">kreditkarte</span></span> 
- <span data-ttu-id="c5035-1456">kreditkarten nummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1456">kreditkarten-nummer</span></span> 
- <span data-ttu-id="c5035-1457">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="c5035-1457">kreditkarteninhaber</span></span> 
- <span data-ttu-id="c5035-1458">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="c5035-1458">kreditkarteninstitut</span></span> 
- <span data-ttu-id="c5035-1459">kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1459">kreditkartennummer</span></span> 
- <span data-ttu-id="c5035-1460">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="c5035-1460">kreditkartentyp</span></span> 
- <span data-ttu-id="c5035-1461">maestro
</span><span class="sxs-lookup"><span data-stu-id="c5035-1461">maestro</span></span> 
- <span data-ttu-id="c5035-1462">master card
</span><span class="sxs-lookup"><span data-stu-id="c5035-1462">master card</span></span> 
- <span data-ttu-id="c5035-1463">master cards
</span><span class="sxs-lookup"><span data-stu-id="c5035-1463">master cards</span></span> 
- <span data-ttu-id="c5035-1464">mastercard
</span><span class="sxs-lookup"><span data-stu-id="c5035-1464">mastercard</span></span> 
- <span data-ttu-id="c5035-1465">mastercards</span><span class="sxs-lookup"><span data-stu-id="c5035-1465">mastercards</span></span> 
- <span data-ttu-id="c5035-1466">mc</span><span class="sxs-lookup"><span data-stu-id="c5035-1466">mc</span></span> 
- <span data-ttu-id="c5035-1467">mister cash
</span><span class="sxs-lookup"><span data-stu-id="c5035-1467">mister cash</span></span> 
- <span data-ttu-id="c5035-1468">n carta</span><span class="sxs-lookup"><span data-stu-id="c5035-1468">n carta</span></span> 
- <span data-ttu-id="c5035-1469">carta</span><span class="sxs-lookup"><span data-stu-id="c5035-1469">carta</span></span> 
- <span data-ttu-id="c5035-1470">de tarjeta 없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1470">no de tarjeta</span></span> 
- <span data-ttu-id="c5035-1471">do cartao 없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1471">no do cartao</span></span> 
- <span data-ttu-id="c5035-1472">do cartão 없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1472">no do cartão</span></span> 
- <span data-ttu-id="c5035-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="c5035-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="c5035-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-p118">no. do cartao</span></span> 
- <span data-ttu-id="c5035-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-p119">no. do cartão</span></span> 
- <span data-ttu-id="c5035-1479">nr carta</span><span class="sxs-lookup"><span data-stu-id="c5035-1479">nr carta</span></span> 
- <span data-ttu-id="c5035-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-p120">nr. carta</span></span> 
- <span data-ttu-id="c5035-1482">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="c5035-1482">numeri di scheda</span></span> 
- <span data-ttu-id="c5035-1483">numero carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1483">numero carta</span></span> 
- <span data-ttu-id="c5035-1484">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1484">numero de cartao</span></span> 
- <span data-ttu-id="c5035-1485">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1485">numero de carte</span></span> 
- <span data-ttu-id="c5035-1486">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-1486">numero de cartão</span></span> 
- <span data-ttu-id="c5035-1487">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1487">numero de tarjeta</span></span>
- <span data-ttu-id="c5035-1488">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1488">numero della carta</span></span> 
- <span data-ttu-id="c5035-1489">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1489">numero di carta</span></span> 
- <span data-ttu-id="c5035-1490">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="c5035-1490">numero di scheda</span></span> 
- <span data-ttu-id="c5035-1491">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1491">numero do cartao</span></span> 
- <span data-ttu-id="c5035-1492">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-1492">numero do cartão</span></span> 
- <span data-ttu-id="c5035-1493">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1493">numéro de carte</span></span> 
- <span data-ttu-id="c5035-1494">nº carta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1494">nº carta</span></span> 
- <span data-ttu-id="c5035-1495">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1495">nº de carte</span></span> 
- <span data-ttu-id="c5035-1496">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="c5035-1496">nº de la carte</span></span> 
- <span data-ttu-id="c5035-1497">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1497">nº de tarjeta</span></span> 
- <span data-ttu-id="c5035-1498">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1498">nº do cartao</span></span> 
- <span data-ttu-id="c5035-1499">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="c5035-1499">nº do cartão</span></span> 
- <span data-ttu-id="c5035-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-p121">nº. do cartão</span></span> 
- <span data-ttu-id="c5035-1502">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1502">número de cartao</span></span> 
- <span data-ttu-id="c5035-1503">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="c5035-1503">número de cartão</span></span> 
- <span data-ttu-id="c5035-1504">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1504">número de tarjeta</span></span> 
- <span data-ttu-id="c5035-1505">número do cartao</span><span class="sxs-lookup"><span data-stu-id="c5035-1505">número do cartao</span></span> 
- <span data-ttu-id="c5035-1506">scheda dell'assegno
</span><span class="sxs-lookup"><span data-stu-id="c5035-1506">scheda dell'assegno</span></span> 
- <span data-ttu-id="c5035-1507">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="c5035-1507">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="c5035-1508">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="c5035-1508">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="c5035-1509">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="c5035-1509">scheda della banca</span></span> 
- <span data-ttu-id="c5035-1510">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="c5035-1510">scheda di controllo</span></span> 
- <span data-ttu-id="c5035-1511">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1511">scheda di debito</span></span> 
- <span data-ttu-id="c5035-1512">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="c5035-1512">scheda matrice</span></span> 
- <span data-ttu-id="c5035-1513">schede dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="c5035-1513">schede dell'atmosfera</span></span> 
- <span data-ttu-id="c5035-1514">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="c5035-1514">schede di controllo</span></span> 
- <span data-ttu-id="c5035-1515">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1515">schede di debito</span></span> 
- <span data-ttu-id="c5035-1516">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="c5035-1516">schede matrici</span></span> 
- <span data-ttu-id="c5035-1517">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="c5035-1517">scoprono la scheda</span></span> 
- <span data-ttu-id="c5035-1518">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="c5035-1518">scoprono le schede</span></span> 
- <span data-ttu-id="c5035-1519">solo
</span><span class="sxs-lookup"><span data-stu-id="c5035-1519">solo</span></span> 
- <span data-ttu-id="c5035-1520">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="c5035-1520">supporti di scheda</span></span> 
- <span data-ttu-id="c5035-1521">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="c5035-1521">supporto di scheda</span></span> 
- <span data-ttu-id="c5035-1522">스위치</span><span class="sxs-lookup"><span data-stu-id="c5035-1522">switch</span></span> 
- <span data-ttu-id="c5035-1523">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="c5035-1523">tarjeta atm</span></span> 
- <span data-ttu-id="c5035-1524">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1524">tarjeta credito</span></span> 
- <span data-ttu-id="c5035-1525">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="c5035-1525">tarjeta de atm</span></span> 
- <span data-ttu-id="c5035-1526">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1526">tarjeta de credito</span></span> 
- <span data-ttu-id="c5035-1527">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1527">tarjeta de debito</span></span> 
- <span data-ttu-id="c5035-1528">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="c5035-1528">tarjeta debito</span></span> 
- <span data-ttu-id="c5035-1529">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="c5035-1529">tarjeta no</span></span>
- <span data-ttu-id="c5035-1530">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="c5035-1530">tarjetahabiente</span></span> 
- <span data-ttu-id="c5035-1531">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="c5035-1531">tipo della scheda</span></span> 
- <span data-ttu-id="c5035-1532">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="c5035-1532">ufficio giapponese della</span></span> 
- <span data-ttu-id="c5035-1533">scheda
</span><span class="sxs-lookup"><span data-stu-id="c5035-1533">scheda</span></span> 
- <span data-ttu-id="c5035-1534">v pay
</span><span class="sxs-lookup"><span data-stu-id="c5035-1534">v pay</span></span> 
- <span data-ttu-id="c5035-1535">v 급여</span><span class="sxs-lookup"><span data-stu-id="c5035-1535">v-pay</span></span> 
- <span data-ttu-id="c5035-1536">visa
</span><span class="sxs-lookup"><span data-stu-id="c5035-1536">visa</span></span> 
- <span data-ttu-id="c5035-1537">visa plus
</span><span class="sxs-lookup"><span data-stu-id="c5035-1537">visa plus</span></span> 
- <span data-ttu-id="c5035-1538">visa electron
</span><span class="sxs-lookup"><span data-stu-id="c5035-1538">visa electron</span></span> 
- <span data-ttu-id="c5035-1539">visto
</span><span class="sxs-lookup"><span data-stu-id="c5035-1539">visto</span></span> 
- <span data-ttu-id="c5035-1540">visum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1540">visum</span></span> 
- <span data-ttu-id="c5035-1541">vpay
</span><span class="sxs-lookup"><span data-stu-id="c5035-1541">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="c5035-1542">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="c5035-1542">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="c5035-1543">card identification number</span><span class="sxs-lookup"><span data-stu-id="c5035-1543">card identification number</span></span>
- <span data-ttu-id="c5035-1544">card verification</span><span class="sxs-lookup"><span data-stu-id="c5035-1544">card verification</span></span> 
- <span data-ttu-id="c5035-1545">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="c5035-1545">cardi la verifica</span></span> 
- <span data-ttu-id="c5035-1546">cid
</span><span class="sxs-lookup"><span data-stu-id="c5035-1546">cid</span></span> 
- <span data-ttu-id="c5035-1547">코드 seg</span><span class="sxs-lookup"><span data-stu-id="c5035-1547">cod seg</span></span> 
- <span data-ttu-id="c5035-1548">코드 브라질어</span><span class="sxs-lookup"><span data-stu-id="c5035-1548">cod seguranca</span></span> 
- <span data-ttu-id="c5035-1549">코드 segurança</span><span class="sxs-lookup"><span data-stu-id="c5035-1549">cod segurança</span></span> 
- <span data-ttu-id="c5035-1550">코드 sicurezza</span><span class="sxs-lookup"><span data-stu-id="c5035-1550">cod sicurezza</span></span> 
- <span data-ttu-id="c5035-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="c5035-p122">cod. seg</span></span> 
- <span data-ttu-id="c5035-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="c5035-p123">cod. seguranca</span></span> 
- <span data-ttu-id="c5035-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="c5035-p124">cod. segurança</span></span> 
- <span data-ttu-id="c5035-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="c5035-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="c5035-1559">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="c5035-1559">codice di sicurezza</span></span> 
- <span data-ttu-id="c5035-1560">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="c5035-1560">codice di verifica</span></span> 
- <span data-ttu-id="c5035-1561">codigo
</span><span class="sxs-lookup"><span data-stu-id="c5035-1561">codigo</span></span> 
- <span data-ttu-id="c5035-1562">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="c5035-1562">codigo de seguranca</span></span> 
- <span data-ttu-id="c5035-1563">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="c5035-1563">codigo de segurança</span></span> 
- <span data-ttu-id="c5035-1564">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="c5035-1564">crittogramma</span></span> 
- <span data-ttu-id="c5035-1565">cryptogram
</span><span class="sxs-lookup"><span data-stu-id="c5035-1565">cryptogram</span></span> 
- <span data-ttu-id="c5035-1566">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="c5035-1566">cryptogramme</span></span> 
- <span data-ttu-id="c5035-1567">cv2</span><span class="sxs-lookup"><span data-stu-id="c5035-1567">cv2</span></span> 
- <span data-ttu-id="c5035-1568">cvc
</span><span class="sxs-lookup"><span data-stu-id="c5035-1568">cvc</span></span> 
- <span data-ttu-id="c5035-1569">cvc2</span><span class="sxs-lookup"><span data-stu-id="c5035-1569">cvc2</span></span> 
- <span data-ttu-id="c5035-1570">cvn
</span><span class="sxs-lookup"><span data-stu-id="c5035-1570">cvn</span></span> 
- <span data-ttu-id="c5035-1571">cvv
</span><span class="sxs-lookup"><span data-stu-id="c5035-1571">cvv</span></span> 
- <span data-ttu-id="c5035-1572">cvv2</span><span class="sxs-lookup"><span data-stu-id="c5035-1572">cvv2</span></span> 
- <span data-ttu-id="c5035-1573">cód 브라질어</span><span class="sxs-lookup"><span data-stu-id="c5035-1573">cód seguranca</span></span> 
- <span data-ttu-id="c5035-1574">cód segurança</span><span class="sxs-lookup"><span data-stu-id="c5035-1574">cód segurança</span></span> 
- <span data-ttu-id="c5035-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="c5035-p126">cód. seguranca</span></span> 
- <span data-ttu-id="c5035-p127">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="c5035-p127">cód. segurança</span></span> 
- <span data-ttu-id="c5035-1579">código
</span><span class="sxs-lookup"><span data-stu-id="c5035-1579">código</span></span> 
- <span data-ttu-id="c5035-1580">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="c5035-1580">código de seguranca</span></span> 
- <span data-ttu-id="c5035-1581">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="c5035-1581">código de segurança</span></span> 
- <span data-ttu-id="c5035-1582">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="c5035-1582">de kaart controle</span></span> 
- <span data-ttu-id="c5035-1583">geeft nr uit
</span><span class="sxs-lookup"><span data-stu-id="c5035-1583">geeft nr uit</span></span> 
- <span data-ttu-id="c5035-1584">issue no
</span><span class="sxs-lookup"><span data-stu-id="c5035-1584">issue no</span></span> 
- <span data-ttu-id="c5035-1585">issue number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1585">issue number</span></span> 
- <span data-ttu-id="c5035-1586">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1586">kaartidentificatienummer</span></span> 
- <span data-ttu-id="c5035-1587">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1587">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="c5035-1588">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1588">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="c5035-1589">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="c5035-1589">kwestieaantal</span></span> 
- <span data-ttu-id="c5035-p128">no. dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="c5035-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="c5035-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="c5035-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="c5035-1594">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="c5035-1594">numero de securite</span></span> 
- <span data-ttu-id="c5035-1595">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1595">numero de verificacao</span></span> 
- <span data-ttu-id="c5035-1596">numero dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="c5035-1596">numero dell'edizione</span></span> 
- <span data-ttu-id="c5035-1597">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="c5035-1597">numero di identificazione della</span></span> 
- <span data-ttu-id="c5035-1598">scheda
</span><span class="sxs-lookup"><span data-stu-id="c5035-1598">scheda</span></span> 
- <span data-ttu-id="c5035-1599">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="c5035-1599">numero di sicurezza</span></span> 
- <span data-ttu-id="c5035-1600">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="c5035-1600">numero van veiligheid</span></span> 
- <span data-ttu-id="c5035-1601">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="c5035-1601">numéro de sécurité</span></span> 
- <span data-ttu-id="c5035-1602">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="c5035-1602">nº autorizzazione</span></span> 
- <span data-ttu-id="c5035-1603">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="c5035-1603">número de verificação</span></span> 
- <span data-ttu-id="c5035-1604">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="c5035-1604">perno il blocco</span></span> 
- <span data-ttu-id="c5035-1605">pin block
</span><span class="sxs-lookup"><span data-stu-id="c5035-1605">pin block</span></span> 
- <span data-ttu-id="c5035-1606">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1606">prufziffer</span></span> 
- <span data-ttu-id="c5035-1607">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1607">prüfziffer</span></span> 
- <span data-ttu-id="c5035-1608">security code
</span><span class="sxs-lookup"><span data-stu-id="c5035-1608">security code</span></span> 
- <span data-ttu-id="c5035-1609">security no
</span><span class="sxs-lookup"><span data-stu-id="c5035-1609">security no</span></span> 
- <span data-ttu-id="c5035-1610">security number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1610">security number</span></span> 
- <span data-ttu-id="c5035-1611">sicherheits kode
</span><span class="sxs-lookup"><span data-stu-id="c5035-1611">sicherheits kode</span></span> 
- <span data-ttu-id="c5035-1612">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="c5035-1612">sicherheitscode</span></span> 
- <span data-ttu-id="c5035-1613">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1613">sicherheitsnummer</span></span> 
- <span data-ttu-id="c5035-1614">speldblok
</span><span class="sxs-lookup"><span data-stu-id="c5035-1614">speldblok</span></span> 
- <span data-ttu-id="c5035-1615">veiligheid 번호:
</span><span class="sxs-lookup"><span data-stu-id="c5035-1615">veiligheid nr</span></span> 
- <span data-ttu-id="c5035-1616">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="c5035-1616">veiligheidsaantal</span></span> 
- <span data-ttu-id="c5035-1617">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="c5035-1617">veiligheidscode</span></span> 
- <span data-ttu-id="c5035-1618">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-1618">veiligheidsnummer</span></span> 
- <span data-ttu-id="c5035-1619">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1619">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="c5035-1620">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="c5035-1620">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="c5035-1621">ablauf
</span><span class="sxs-lookup"><span data-stu-id="c5035-1621">ablauf</span></span> 
- <span data-ttu-id="c5035-1622">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="c5035-1622">data de expiracao</span></span> 
- <span data-ttu-id="c5035-1623">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="c5035-1623">data de expiração</span></span> 
- <span data-ttu-id="c5035-1624">data del exp
</span><span class="sxs-lookup"><span data-stu-id="c5035-1624">data del exp</span></span> 
- <span data-ttu-id="c5035-1625">data di exp
</span><span class="sxs-lookup"><span data-stu-id="c5035-1625">data di exp</span></span> 
- <span data-ttu-id="c5035-1626">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="c5035-1626">data di scadenza</span></span> 
- <span data-ttu-id="c5035-1627">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="c5035-1627">data em que expira</span></span> 
- <span data-ttu-id="c5035-1628">data scad
</span><span class="sxs-lookup"><span data-stu-id="c5035-1628">data scad</span></span> 
- <span data-ttu-id="c5035-1629">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="c5035-1629">data scadenza</span></span> 
- <span data-ttu-id="c5035-1630">date de validité
</span><span class="sxs-lookup"><span data-stu-id="c5035-1630">date de validité</span></span> 
- <span data-ttu-id="c5035-1631">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="c5035-1631">datum afloop</span></span> 
- <span data-ttu-id="c5035-1632">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="c5035-1632">datum van exp</span></span> 
- <span data-ttu-id="c5035-1633">de afloop
</span><span class="sxs-lookup"><span data-stu-id="c5035-1633">de afloop</span></span> 
- <span data-ttu-id="c5035-1634">espira
</span><span class="sxs-lookup"><span data-stu-id="c5035-1634">espira</span></span> 
- <span data-ttu-id="c5035-1635">espira
</span><span class="sxs-lookup"><span data-stu-id="c5035-1635">espira</span></span> 
- <span data-ttu-id="c5035-1636">exp date
</span><span class="sxs-lookup"><span data-stu-id="c5035-1636">exp date</span></span> 
- <span data-ttu-id="c5035-1637">exp datum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1637">exp datum</span></span> 
- <span data-ttu-id="c5035-1638">만료</span><span class="sxs-lookup"><span data-stu-id="c5035-1638">expiration</span></span> 
- <span data-ttu-id="c5035-1639">만료
</span><span class="sxs-lookup"><span data-stu-id="c5035-1639">expire</span></span> 
- <span data-ttu-id="c5035-1640">expires
</span><span class="sxs-lookup"><span data-stu-id="c5035-1640">expires</span></span> 
- <span data-ttu-id="c5035-1641">expiry
</span><span class="sxs-lookup"><span data-stu-id="c5035-1641">expiry</span></span> 
- <span data-ttu-id="c5035-1642">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="c5035-1642">fecha de expiracion</span></span> 
- <span data-ttu-id="c5035-1643">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="c5035-1643">fecha de venc</span></span> 
- <span data-ttu-id="c5035-1644">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="c5035-1644">gultig bis</span></span> 
- <span data-ttu-id="c5035-1645">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1645">gultigkeitsdatum</span></span> 
- <span data-ttu-id="c5035-1646">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="c5035-1646">gültig bis</span></span> 
- <span data-ttu-id="c5035-1647">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1647">gültigkeitsdatum</span></span> 
- <span data-ttu-id="c5035-1648">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="c5035-1648">la scadenza</span></span> 
- <span data-ttu-id="c5035-1649">scadenza
</span><span class="sxs-lookup"><span data-stu-id="c5035-1649">scadenza</span></span> 
- <span data-ttu-id="c5035-1650">valable
</span><span class="sxs-lookup"><span data-stu-id="c5035-1650">valable</span></span> 
- <span data-ttu-id="c5035-1651">validade
</span><span class="sxs-lookup"><span data-stu-id="c5035-1651">validade</span></span> 
- <span data-ttu-id="c5035-1652">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1652">valido hasta</span></span> 
- <span data-ttu-id="c5035-1653">valor
</span><span class="sxs-lookup"><span data-stu-id="c5035-1653">valor</span></span> 
- <span data-ttu-id="c5035-1654">venc
</span><span class="sxs-lookup"><span data-stu-id="c5035-1654">venc</span></span> 
- <span data-ttu-id="c5035-1655">vencimento
</span><span class="sxs-lookup"><span data-stu-id="c5035-1655">vencimento</span></span> 
- <span data-ttu-id="c5035-1656">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="c5035-1656">vencimiento</span></span> 
- <span data-ttu-id="c5035-1657">verloopt
</span><span class="sxs-lookup"><span data-stu-id="c5035-1657">verloopt</span></span> 
- <span data-ttu-id="c5035-1658">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="c5035-1658">vervaldag</span></span> 
- <span data-ttu-id="c5035-1659">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1659">vervaldatum</span></span> 
- <span data-ttu-id="c5035-1660">vto
</span><span class="sxs-lookup"><span data-stu-id="c5035-1660">vto</span></span> 
- <span data-ttu-id="c5035-1661">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="c5035-1661">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="c5035-1662">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1662">EU Driver's License Number</span></span>

<span data-ttu-id="c5035-1663">자세한 내용은 [EU 운전 면허 번호 중요 한 정보 유형](eu-driver-s-license-number.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c5035-1663">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="c5035-1664">EU 국가 Id 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1664">EU National Identification Number</span></span>

<span data-ttu-id="c5035-1665">자세한 내용을 보려면, [EU 국가 Id 번호 중요 한 정보 유형](eu-national-identification-number.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c5035-1665">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="c5035-1666">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1666">EU Passport Number</span></span>

<span data-ttu-id="c5035-1667">자세한 내용을 보려면, [EU 여권 번호 중요 한 정보 유형](eu-passport-number.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c5035-1667">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="c5035-1668">EU 사회보장 번호 또는에 상응 하는 ID</span><span class="sxs-lookup"><span data-stu-id="c5035-1668">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="c5035-1669">자세한 내용을 보려면 [EU 사회보장 번호 또는 중요 한 정보 형식에 해당 ID를](eu-social-security-number-or-equivalent-id.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c5035-1669">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="c5035-1670">EU 세금 Id 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1670">EU Tax Identification Number</span></span>

<span data-ttu-id="c5035-1671">자세한 내용을 보려면, [EU 세금 Id 번호 중요 한 정보 유형](eu-tax-identification-number.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c5035-1671">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="c5035-1672">핀란드 국가 ID</span><span class="sxs-lookup"><span data-stu-id="c5035-1672">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1673">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1673">Format</span></span>

<span data-ttu-id="c5035-1674">세기를 나타내는 6자리 숫자와 문자, 3자리 숫자와 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1674">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1675">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1675">Pattern</span></span>

<span data-ttu-id="c5035-1676">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1676">Pattern must include all of the following:</span></span>
- <span data-ttu-id="c5035-1677">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1677">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="c5035-1678">세기 표시('-', '+' 또는 'a')</span><span class="sxs-lookup"><span data-stu-id="c5035-1678">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="c5035-1679">3자리 개인 ID 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1679">Three-digit personal identification number</span></span> 
- <span data-ttu-id="c5035-1680">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-1680">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1681">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1681">Checksum</span></span>

<span data-ttu-id="c5035-1682">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1682">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1683">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1683">Definition</span></span>

<span data-ttu-id="c5035-1684">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1684">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1685">Func_finnish_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1685">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1686">Keyword_finnish_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1686">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="c5035-1687">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1687">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-1688">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1688">Keywords</span></span>

- <span data-ttu-id="c5035-1689">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="c5035-1689">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="c5035-1690">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="c5035-1690">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="c5035-1691">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="c5035-1691">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="c5035-1692">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="c5035-1692">Personbeteckning</span></span>
- <span data-ttu-id="c5035-1693">Personnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1693">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="c5035-1694">핀란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1694">Finland Passport Number</span></span>

<span data-ttu-id="c5035-p130">9 개의 문자와 숫자 패턴 조합 9 개의 대 문자와 숫자의 조합 서식: 두 문자 (하지 대/소문자 구분) 7 자리 체크섬 No 정의 A DLP 정책은 판단 하는 경우 이러한 종류의 중요 한 정보를 검색에 75%, 내 프로그램 300 자 근접: Regex_finland_passport_number 정규식 패턴과 일치 하는 콘텐츠를 찾습니다. Keyword_finland_passport_number에서 키워드를 발견 됩니다. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> 키워드 Keyword_finland_passport_number Passport Passi</span><span class="sxs-lookup"><span data-stu-id="c5035-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="c5035-1699">프랑스 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1699">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1700">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1700">Format</span></span>

<span data-ttu-id="c5035-1701">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1701">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1702">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1702">Pattern</span></span>

<span data-ttu-id="c5035-1703">비슷한 패턴(예: 프랑스 전화 번호)을 무시하기 위한 유효성 검사 기능을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1703">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1704">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1704">Checksum</span></span>

<span data-ttu-id="c5035-1705">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1705">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1706">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1706">Definition</span></span>

<span data-ttu-id="c5035-1707">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1707">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1708">Func_french_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1708">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1709">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1709">At least one of the following is true:</span></span>
- <span data-ttu-id="c5035-1710">Keyword_french_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1710">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="c5035-1711">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1711">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-1712">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1712">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="c5035-1713">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="c5035-1713">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="c5035-1714">drivers licence</span><span class="sxs-lookup"><span data-stu-id="c5035-1714">drivers licence</span></span>
- <span data-ttu-id="c5035-1715">
drivers license</span><span class="sxs-lookup"><span data-stu-id="c5035-1715">drivers license</span></span>
- <span data-ttu-id="c5035-1716">driving licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-1716">driving licence</span></span>
- <span data-ttu-id="c5035-1717">라이선스를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1717">driving license</span></span>
- <span data-ttu-id="c5035-1718">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="c5035-1718">permis de conduire</span></span>
- <span data-ttu-id="c5035-1719">
licence number</span><span class="sxs-lookup"><span data-stu-id="c5035-1719">licence number</span></span>
- <span data-ttu-id="c5035-1720">
license number</span><span class="sxs-lookup"><span data-stu-id="c5035-1720">license number</span></span>
- <span data-ttu-id="c5035-1721">
licence numbers</span><span class="sxs-lookup"><span data-stu-id="c5035-1721">licence numbers</span></span>
- <span data-ttu-id="c5035-1722">

license numbers</span><span class="sxs-lookup"><span data-stu-id="c5035-1722">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="c5035-1723">프랑스 국가 ID 카드(CNI)</span><span class="sxs-lookup"><span data-stu-id="c5035-1723">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1724">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1724">Format</span></span>

<span data-ttu-id="c5035-1725">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1725">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1726">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1726">Pattern</span></span>

<span data-ttu-id="c5035-1727">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1727">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1728">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1728">Checksum</span></span>

<span data-ttu-id="c5035-1729">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1729">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1730">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1730">Definition</span></span>

<span data-ttu-id="c5035-1731">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1731">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1732">Regex_france_cni 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1732">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-1733">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1733">Keywords</span></span>

<span data-ttu-id="c5035-1734">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1734">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="c5035-1735">프랑스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1735">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1736">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1736">Format</span></span>

<span data-ttu-id="c5035-1737">9자리 숫자 및 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-1737">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1738">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1738">Pattern</span></span>

<span data-ttu-id="c5035-1739">9자리 숫자 및 문자:</span><span class="sxs-lookup"><span data-stu-id="c5035-1739">Nine digits and letters:</span></span>
- <span data-ttu-id="c5035-1740">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1740">Two digits</span></span> 
- <span data-ttu-id="c5035-1741">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-1741">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-1742">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1742">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1743">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1743">Checksum</span></span>

<span data-ttu-id="c5035-1744">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1744">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1745">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1745">Definition</span></span>

<span data-ttu-id="c5035-1746">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1746">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1747">Func_fr_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1747">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1748">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1748">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-1749">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1749">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="c5035-1750">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-1750">Keyword_passport</span></span>

- <span data-ttu-id="c5035-1751">Passport Number</span><span class="sxs-lookup"><span data-stu-id="c5035-1751">Passport Number</span></span>
- <span data-ttu-id="c5035-1752">
Passport No</span><span class="sxs-lookup"><span data-stu-id="c5035-1752">Passport No</span></span>
- <span data-ttu-id="c5035-1753">Passport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-1753">Passport #</span></span>
- <span data-ttu-id="c5035-1754">Passport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-1754">Passport#</span></span>
- <span data-ttu-id="c5035-1755">PassportID</span><span class="sxs-lookup"><span data-stu-id="c5035-1755">PassportID</span></span>
- <span data-ttu-id="c5035-1756">Passportno
</span><span class="sxs-lookup"><span data-stu-id="c5035-1756">Passportno</span></span>
- <span data-ttu-id="c5035-1757">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-1757">passportnumber</span></span>
- <span data-ttu-id="c5035-1758">パスポート</span><span class="sxs-lookup"><span data-stu-id="c5035-1758">パスポート</span></span>
- <span data-ttu-id="c5035-1759">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-1759">パスポート番号</span></span>
- <span data-ttu-id="c5035-1760">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="c5035-1760">パスポートのNum</span></span>
- <span data-ttu-id="c5035-1761">
パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="c5035-1761">パスポート ＃</span></span> 
- <span data-ttu-id="c5035-1762">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="c5035-1762">Numéro de passeport</span></span>
- <span data-ttu-id="c5035-1763">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="c5035-1763">Passeport n °</span></span>
- <span data-ttu-id="c5035-1764">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="c5035-1764">Passeport Non</span></span>
- <span data-ttu-id="c5035-1765">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-1765">Passeport #</span></span>
- <span data-ttu-id="c5035-1766">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-1766">Passeport#</span></span>
- <span data-ttu-id="c5035-1767">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="c5035-1767">PasseportNon</span></span>
- <span data-ttu-id="c5035-1768">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="c5035-1768">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="c5035-1769">프랑스 사회 보장 번호(INSEE)</span><span class="sxs-lookup"><span data-stu-id="c5035-1769">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1770">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1770">Format</span></span>

<span data-ttu-id="c5035-1771">15자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1771">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1772">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1772">Pattern</span></span>

<span data-ttu-id="c5035-1773">다음 두 패턴 중 하나가 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1773">Must match one of two patterns:</span></span>
- <span data-ttu-id="c5035-1774">두 자리 숫자 앞에 오는 공백 뒤 13 자릿수</span><span class="sxs-lookup"><span data-stu-id="c5035-1774">13 digits followed by a space followed by two digits</span></span></br>
<span data-ttu-id="c5035-1775">또는</span><span class="sxs-lookup"><span data-stu-id="c5035-1775">or</span></span>
- <span data-ttu-id="c5035-1776">15자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1776">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1777">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1777">Checksum</span></span>

<span data-ttu-id="c5035-1778">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1778">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1779">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1779">Definition</span></span>

<span data-ttu-id="c5035-1780">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1780">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1781">Func_french_insee 또는 Func_fr_insee 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1781">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1782">Keyword_fr_insee의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1782">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="c5035-1783">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1783">The checksum passes.</span></span>

<span data-ttu-id="c5035-1784">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1785">Func_french_insee 또는 Func_fr_insee 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1785">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1786">Keyword_fr_insee의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1786">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="c5035-1787">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1787">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-1788">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1788">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="c5035-1789">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="c5035-1789">Keyword_fr_insee</span></span>

- <span data-ttu-id="c5035-1790">insee</span><span class="sxs-lookup"><span data-stu-id="c5035-1790">insee</span></span>
- <span data-ttu-id="c5035-1791">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="c5035-1791">securité sociale</span></span>
- <span data-ttu-id="c5035-1792">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="c5035-1792">securite sociale</span></span>
- <span data-ttu-id="c5035-1793">
national id</span><span class="sxs-lookup"><span data-stu-id="c5035-1793">national id</span></span>
- <span data-ttu-id="c5035-1794">
national identification</span><span class="sxs-lookup"><span data-stu-id="c5035-1794">national identification</span></span>
- <span data-ttu-id="c5035-1795">
numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="c5035-1795">numéro d'identité</span></span>
- <span data-ttu-id="c5035-1796">없음 d'identité</span><span class="sxs-lookup"><span data-stu-id="c5035-1796">no d'identité</span></span>
- <span data-ttu-id="c5035-p131">
no. d'identité</span><span class="sxs-lookup"><span data-stu-id="c5035-p131">no. d'identité</span></span>
- <span data-ttu-id="c5035-1799">
numero d'identite</span><span class="sxs-lookup"><span data-stu-id="c5035-1799">numero d'identite</span></span>
- <span data-ttu-id="c5035-1800">없음 d'identite</span><span class="sxs-lookup"><span data-stu-id="c5035-1800">no d'identite</span></span>
- <span data-ttu-id="c5035-p132">
no. d'identite</span><span class="sxs-lookup"><span data-stu-id="c5035-p132">no. d'identite</span></span>
- <span data-ttu-id="c5035-1803">social security number
</span><span class="sxs-lookup"><span data-stu-id="c5035-1803">social security number</span></span>
- <span data-ttu-id="c5035-1804">
social security code</span><span class="sxs-lookup"><span data-stu-id="c5035-1804">social security code</span></span>
- <span data-ttu-id="c5035-1805">social insurance number</span><span class="sxs-lookup"><span data-stu-id="c5035-1805">social insurance number</span></span>
- <span data-ttu-id="c5035-1806">
le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="c5035-1806">le numéro d'identification nationale</span></span>
- <span data-ttu-id="c5035-1807">
d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="c5035-1807">d'identité nationale</span></span>
- <span data-ttu-id="c5035-1808">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="c5035-1808">numéro de sécurité sociale</span></span>
- <span data-ttu-id="c5035-1809">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="c5035-1809">le code de la sécurité sociale</span></span>
- <span data-ttu-id="c5035-1810">
numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="c5035-1810">numéro d'assurance sociale</span></span>
- <span data-ttu-id="c5035-1811">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="c5035-1811">numéro de sécu</span></span>
- <span data-ttu-id="c5035-1812">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="c5035-1812">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="c5035-1813">독일 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1813">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1814">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1814">Format</span></span>

<span data-ttu-id="c5035-1815">11자리 숫자와 문자 조합</span><span class="sxs-lookup"><span data-stu-id="c5035-1815">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1816">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1816">Pattern</span></span>

<span data-ttu-id="c5035-1817">11자리 숫자와 문자(대/소문자 구분 안 함):</span><span class="sxs-lookup"><span data-stu-id="c5035-1817">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="c5035-1818">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-1818">A digit or letter</span></span> 
- <span data-ttu-id="c5035-1819">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1819">Two digits</span></span> 
- <span data-ttu-id="c5035-1820">6자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-1820">Six digits or letters</span></span> 
- <span data-ttu-id="c5035-1821">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1821">A digit</span></span> 
- <span data-ttu-id="c5035-1822">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-1822">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1823">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1823">Checksum</span></span>

<span data-ttu-id="c5035-1824">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1825">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1825">Definition</span></span>

<span data-ttu-id="c5035-1826">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1826">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1827">Func_german_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1827">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1828">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1828">At least one of the following is true:</span></span>
    - <span data-ttu-id="c5035-1829">Keyword_german_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1829">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="c5035-1830">Keyword_german_drivers_license_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1830">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="c5035-1831">Keyword_german_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1831">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="c5035-1832">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1832">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-1833">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1833">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="c5035-1834">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="c5035-1834">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="c5035-1835">Führerschein</span><span class="sxs-lookup"><span data-stu-id="c5035-1835">Führerschein</span></span>
- <span data-ttu-id="c5035-1836">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="c5035-1836">Fuhrerschein</span></span>
- <span data-ttu-id="c5035-1837">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="c5035-1837">Fuehrerschein</span></span>
- <span data-ttu-id="c5035-1838">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1838">Führerscheinnummer</span></span>
- <span data-ttu-id="c5035-1839">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1839">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="c5035-1840">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1840">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="c5035-1841">
Führerschein-
</span><span class="sxs-lookup"><span data-stu-id="c5035-1841">Führerschein-</span></span> 
- <span data-ttu-id="c5035-1842">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="c5035-1842">Fuhrerschein-</span></span> 
- <span data-ttu-id="c5035-1843">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="c5035-1843">Fuehrerschein-</span></span> 
- <span data-ttu-id="c5035-1844">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="c5035-1844">FührerscheinnummerNr</span></span>
- <span data-ttu-id="c5035-1845">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="c5035-1845">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="c5035-1846">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="c5035-1846">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="c5035-1847">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1847">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="c5035-1848">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1848">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="c5035-1849">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1849">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="c5035-1850">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1850">Führerschein- Nr</span></span>
- <span data-ttu-id="c5035-1851">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1851">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="c5035-1852">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1852">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="c5035-1853">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="c5035-1853">Führerschein- Klasse</span></span> 
- <span data-ttu-id="c5035-1854">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="c5035-1854">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="c5035-1855">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1855">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="c5035-1856">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="c5035-1856">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="c5035-1857">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="c5035-1857">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="c5035-1858">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="c5035-1858">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="c5035-1859">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1859">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="c5035-1860">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1860">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="c5035-1861">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1861">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="c5035-1862">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1862">Führerschein- Nr</span></span> 
- <span data-ttu-id="c5035-1863">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1863">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="c5035-1864">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1864">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="c5035-1865">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="c5035-1865">Führerschein- Klasse</span></span> 
- <span data-ttu-id="c5035-1866">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="c5035-1866">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="c5035-1867">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1867">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="c5035-1868">DL</span><span class="sxs-lookup"><span data-stu-id="c5035-1868">DL</span></span> 
- <span data-ttu-id="c5035-1869">DLS</span><span class="sxs-lookup"><span data-stu-id="c5035-1869">DLS</span></span>
- <span data-ttu-id="c5035-1870">
Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="c5035-1870">Driv Lic</span></span> 
- <span data-ttu-id="c5035-1871">Driv Licen
</span><span class="sxs-lookup"><span data-stu-id="c5035-1871">Driv Licen</span></span> 
- <span data-ttu-id="c5035-1872">Driv License</span><span class="sxs-lookup"><span data-stu-id="c5035-1872">Driv License</span></span>
- <span data-ttu-id="c5035-1873">
Driv Licenses
</span><span class="sxs-lookup"><span data-stu-id="c5035-1873">Driv Licenses</span></span> 
- <span data-ttu-id="c5035-1874">Driv Licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-1874">Driv Licence</span></span> 
- <span data-ttu-id="c5035-1875">Driv Licences
</span><span class="sxs-lookup"><span data-stu-id="c5035-1875">Driv Licences</span></span> 
- <span data-ttu-id="c5035-1876">Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="c5035-1876">Driv Lic</span></span> 
- <span data-ttu-id="c5035-1877">Driver Licen
</span><span class="sxs-lookup"><span data-stu-id="c5035-1877">Driver Licen</span></span> 
- <span data-ttu-id="c5035-1878">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-1878">Driver License</span></span> 
- <span data-ttu-id="c5035-1879">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-1879">Driver Licenses</span></span> 
- <span data-ttu-id="c5035-1880">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-1880">Driver Licence</span></span> 
- <span data-ttu-id="c5035-1881">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="c5035-1881">Driver Licences</span></span> 
- <span data-ttu-id="c5035-1882">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-1882">Drivers Lic</span></span> 
- <span data-ttu-id="c5035-1883">드라이버 Licen</span><span class="sxs-lookup"><span data-stu-id="c5035-1883">Drivers Licen</span></span> 
- <span data-ttu-id="c5035-1884">운전 면허</span><span class="sxs-lookup"><span data-stu-id="c5035-1884">Drivers License</span></span> 
- <span data-ttu-id="c5035-1885">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-1885">Drivers Licenses</span></span> 
- <span data-ttu-id="c5035-1886">드라이버 사용권</span><span class="sxs-lookup"><span data-stu-id="c5035-1886">Drivers Licence</span></span> 
- <span data-ttu-id="c5035-1887">드라이버 라이센스</span><span class="sxs-lookup"><span data-stu-id="c5035-1887">Drivers Licences</span></span> 
- <span data-ttu-id="c5035-1888">드라이버의 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-1888">Driver's Lic</span></span> 
- <span data-ttu-id="c5035-1889">Driver's Licen
</span><span class="sxs-lookup"><span data-stu-id="c5035-1889">Driver's Licen</span></span> 
- <span data-ttu-id="c5035-1890">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-1890">Driver's License</span></span> 
- <span data-ttu-id="c5035-1891">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-1891">Driver's Licenses</span></span> 
- <span data-ttu-id="c5035-1892">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-1892">Driver's Licence</span></span> 
- <span data-ttu-id="c5035-1893">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="c5035-1893">Driver's Licences</span></span> 
- <span data-ttu-id="c5035-1894">Driving Lic
</span><span class="sxs-lookup"><span data-stu-id="c5035-1894">Driving Lic</span></span> 
- <span data-ttu-id="c5035-1895">Driving Licen
</span><span class="sxs-lookup"><span data-stu-id="c5035-1895">Driving Licen</span></span> 
- <span data-ttu-id="c5035-1896">Driving License
</span><span class="sxs-lookup"><span data-stu-id="c5035-1896">Driving License</span></span> 
- <span data-ttu-id="c5035-1897">Driving Licenses
</span><span class="sxs-lookup"><span data-stu-id="c5035-1897">Driving Licenses</span></span> 
- <span data-ttu-id="c5035-1898">Driving Licence

</span><span class="sxs-lookup"><span data-stu-id="c5035-1898">Driving Licence</span></span> 
- <span data-ttu-id="c5035-1899">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="c5035-1899">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="c5035-1900">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="c5035-1900">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="c5035-1901">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1901">Nr-Führerschein</span></span> 
- <span data-ttu-id="c5035-1902">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1902">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="c5035-1903">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1903">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="c5035-1904">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1904">No-Führerschein</span></span> 
- <span data-ttu-id="c5035-1905">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1905">No-Fuhrerschein</span></span> 
- <span data-ttu-id="c5035-1906">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1906">No-Fuehrerschein</span></span> 
- <span data-ttu-id="c5035-1907">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1907">N-Führerschein</span></span> 
- <span data-ttu-id="c5035-1908">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1908">N-Fuhrerschein</span></span> 
- <span data-ttu-id="c5035-1909">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="c5035-1909">N-Fuehrerschein</span></span>
- <span data-ttu-id="c5035-1910">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1910">Nr-Führerschein</span></span> 
- <span data-ttu-id="c5035-1911">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1911">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="c5035-1912">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1912">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="c5035-1913">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1913">No-Führerschein</span></span> 
- <span data-ttu-id="c5035-1914">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1914">No-Fuhrerschein</span></span> 
- <span data-ttu-id="c5035-1915">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1915">No-Fuehrerschein</span></span> 
- <span data-ttu-id="c5035-1916">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1916">N-Führerschein</span></span> 
- <span data-ttu-id="c5035-1917">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="c5035-1917">N-Fuhrerschein</span></span> 
- <span data-ttu-id="c5035-1918">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="c5035-1918">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="c5035-1919">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="c5035-1919">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="c5035-1920">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="c5035-1920">ausstellungsdatum</span></span>
- <span data-ttu-id="c5035-1921">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="c5035-1921">ausstellungsort</span></span>
- <span data-ttu-id="c5035-1922">
ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="c5035-1922">ausstellende behöde</span></span>
- <span data-ttu-id="c5035-1923">
ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="c5035-1923">ausstellende behorde</span></span>
- <span data-ttu-id="c5035-1924">

ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="c5035-1924">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="c5035-1925">독일 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1925">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1926">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1926">Format</span></span>

<span data-ttu-id="c5035-1927">10자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-1927">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1928">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1928">Pattern</span></span>

<span data-ttu-id="c5035-1929">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1929">Pattern must include all of the following:</span></span>
- <span data-ttu-id="c5035-1930">첫 번째 문자는 숫자 또는 (C, F, G, H, J, K) 집합의 문자임</span><span class="sxs-lookup"><span data-stu-id="c5035-1930">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="c5035-1931">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1931">Three digits</span></span> 
- <span data-ttu-id="c5035-1932">5자리 숫자 또는 (C, -H, J-N, P, R, T, V-Z) 집합의 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-1932">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="c5035-1933">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1933">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1934">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1934">Checksum</span></span>

<span data-ttu-id="c5035-1935">예</span><span class="sxs-lookup"><span data-stu-id="c5035-1935">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1936">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1936">Definition</span></span>

<span data-ttu-id="c5035-1937">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1937">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1938">Func_german_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1938">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1939">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1939">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="c5035-1940">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1940">The checksum passes.</span></span>

<span data-ttu-id="c5035-1941">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1941">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1942">Func_german_passport_data 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1942">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1943">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1943">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="c5035-1944">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1944">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-1945">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1945">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="c5035-1946">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-1946">Keyword_german_passport</span></span>

- <span data-ttu-id="c5035-1947">reisepass</span><span class="sxs-lookup"><span data-stu-id="c5035-1947">reisepass</span></span>
- <span data-ttu-id="c5035-1948">
reisepasse</span><span class="sxs-lookup"><span data-stu-id="c5035-1948">reisepasse</span></span>
- <span data-ttu-id="c5035-1949">
reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1949">reisepassnummer</span></span>
- <span data-ttu-id="c5035-1950">passport</span><span class="sxs-lookup"><span data-stu-id="c5035-1950">passport</span></span>
- <span data-ttu-id="c5035-1951">

passports</span><span class="sxs-lookup"><span data-stu-id="c5035-1951">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="c5035-1952">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="c5035-1952">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="c5035-1953">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="c5035-1953">geburtsdatum</span></span>
- <span data-ttu-id="c5035-1954">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="c5035-1954">ausstellungsdatum</span></span>
- <span data-ttu-id="c5035-1955">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="c5035-1955">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="c5035-1956">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="c5035-1956">Keyword_german_passport_number</span></span>

<span data-ttu-id="c5035-1957">더-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="c5035-1957">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="c5035-1958">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="c5035-1958">Keyword_german_passport1</span></span>

<span data-ttu-id="c5035-1959">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="c5035-1959">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="c5035-1960">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="c5035-1960">Keyword_german_passport2</span></span>

<span data-ttu-id="c5035-1961">bnationalit.t</span><span class="sxs-lookup"><span data-stu-id="c5035-1961">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="c5035-1962">독일 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-1962">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1963">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1963">Format</span></span>

<span data-ttu-id="c5035-1964">2010 년 11 월 월 1 일 이후: 9 개의 대 문자와 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1964">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="c5035-1965">31 년 10 월 2010: 10 자리까지 1 년 4 월 1987에서</span><span class="sxs-lookup"><span data-stu-id="c5035-1965">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1966">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1966">Pattern</span></span>

<span data-ttu-id="c5035-1967">2010년 11월 1일 이후:</span><span class="sxs-lookup"><span data-stu-id="c5035-1967">Since 1 November 2010:</span></span>
- <span data-ttu-id="c5035-1968">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-1968">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-1969">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1969">Eight digits</span></span>

<span data-ttu-id="c5035-1970">2010 년 10 월 월 31 일 때까지 1 년 4 월 1987에서:</span><span class="sxs-lookup"><span data-stu-id="c5035-1970">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="c5035-1971">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1971">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1972">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1972">Checksum</span></span>

<span data-ttu-id="c5035-1973">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-1973">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-1974">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-1974">Definition</span></span>

<span data-ttu-id="c5035-1975">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1975">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-1976">Regex_germany_id_card 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1976">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-1977">Keyword_germany_id_card에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-1977">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-1978">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-1978">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="c5035-1979">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="c5035-1979">Keyword_germany_id_card</span></span>

- <span data-ttu-id="c5035-1980">Identity Card</span><span class="sxs-lookup"><span data-stu-id="c5035-1980">Identity Card</span></span>
- <span data-ttu-id="c5035-1981">ID</span><span class="sxs-lookup"><span data-stu-id="c5035-1981">ID</span></span>
- <span data-ttu-id="c5035-1982">Identification</span><span class="sxs-lookup"><span data-stu-id="c5035-1982">Identification</span></span>
- <span data-ttu-id="c5035-1983">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="c5035-1983">Personalausweis</span></span>
- <span data-ttu-id="c5035-1984">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-1984">Identifizierungsnummer</span></span>
- <span data-ttu-id="c5035-1985">Ausweis</span><span class="sxs-lookup"><span data-stu-id="c5035-1985">Ausweis</span></span>
- <span data-ttu-id="c5035-1986">Identifikation</span><span class="sxs-lookup"><span data-stu-id="c5035-1986">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="c5035-1987">그리스 국가 ID 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-1987">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="c5035-1988">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-1988">Format</span></span>

<span data-ttu-id="c5035-1989">7-8자리 문자 및 숫자와 대시의 조합</span><span class="sxs-lookup"><span data-stu-id="c5035-1989">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-1990">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-1990">Pattern</span></span>

<span data-ttu-id="c5035-1991">7자리 문자 및 숫자(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="c5035-1991">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="c5035-1992">1개 문자(그리스어 알파벳의 임의 문자) </span><span class="sxs-lookup"><span data-stu-id="c5035-1992">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="c5035-1993">대시 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-1993">A dash</span></span> 
- <span data-ttu-id="c5035-1994">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1994">Six digits</span></span>

<span data-ttu-id="c5035-1995">8자리 문자와 숫자(새로운 형식):</span><span class="sxs-lookup"><span data-stu-id="c5035-1995">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="c5035-1996">그리스어 및 라틴어 알파벳 둘 다에 해당 대문자가 포함된 2개 문자(ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="c5035-1996">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="c5035-1997">대시 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-1997">A dash</span></span> 
- <span data-ttu-id="c5035-1998">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-1998">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-1999">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-1999">Checksum</span></span>

<span data-ttu-id="c5035-2000">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2000">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2001">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2001">Definition</span></span>

<span data-ttu-id="c5035-2002">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2002">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2003">Regex_greece_id_card 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2003">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2004">Keyword_greece_id_card에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2004">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2005">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2005">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="c5035-2006">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="c5035-2006">Keyword_greece_id_card</span></span>

- <span data-ttu-id="c5035-2007">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="c5035-2007">Greek identity Card</span></span>
- <span data-ttu-id="c5035-2008">Tautotita</span><span class="sxs-lookup"><span data-stu-id="c5035-2008">Tautotita</span></span>
- <span data-ttu-id="c5035-2009">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="c5035-2009">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="c5035-2010">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="c5035-2010">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="c5035-2011">HKID(홍콩 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2011">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2012">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2012">Format</span></span>

<span data-ttu-id="c5035-2013">8-9자리 문자 및 숫자와 마지막 문자를 선택적 괄호로 묶어서 조합</span><span class="sxs-lookup"><span data-stu-id="c5035-2013">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2014">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2014">Pattern</span></span>

<span data-ttu-id="c5035-2015">8-9자리 문자 조합:</span><span class="sxs-lookup"><span data-stu-id="c5035-2015">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="c5035-2016">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2016">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-2017">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2017">Six digits</span></span> 
- <span data-ttu-id="c5035-2018">검사 숫자에 해당하고 선택적으로 괄호로 묶는 마지막 문자(임의 숫자 또는 문자 A)</span><span class="sxs-lookup"><span data-stu-id="c5035-2018">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2019">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2019">Checksum</span></span>

<span data-ttu-id="c5035-2020">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2020">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2021">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2021">Definition</span></span>

<span data-ttu-id="c5035-2022">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2022">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2023">Func_hong_kong_id_card 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2023">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2024">Keyword_hong_kong_id_card에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2024">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="c5035-2025">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2025">The checksum passes.</span></span>

<span data-ttu-id="c5035-2026">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2026">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2027">Func_hong_kong_id_card 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2027">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2028">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2028">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2029">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2029">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="c5035-2030">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="c5035-2030">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="c5035-2031">Hong Kong Identity Card</span><span class="sxs-lookup"><span data-stu-id="c5035-2031">Hong Kong Identity Card</span></span>
- <span data-ttu-id="c5035-2032">HKID</span><span class="sxs-lookup"><span data-stu-id="c5035-2032">HKID</span></span>
- <span data-ttu-id="c5035-2033">ID card</span><span class="sxs-lookup"><span data-stu-id="c5035-2033">ID card</span></span>
- <span data-ttu-id="c5035-2034">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="c5035-2034">香港身份證</span></span> 
- <span data-ttu-id="c5035-2035">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="c5035-2035">香港永久性居民身份證</span></span> 
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="c5035-2036">인도 PAN(영구 계정 번호)</span><span class="sxs-lookup"><span data-stu-id="c5035-2036">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2037">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2037">Format</span></span>

<span data-ttu-id="c5035-2038">10자리 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2038">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2039">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2039">Pattern</span></span>

<span data-ttu-id="c5035-2040">10자리 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2040">10 letters or digits:</span></span>
- <span data-ttu-id="c5035-2041">5개 문자(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="c5035-2041">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-2042">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2042">Four digits</span></span> 
- <span data-ttu-id="c5035-2043">알파벳 검사 숫자에 해당하는 문자 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-2043">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2044">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2044">Checksum</span></span>

<span data-ttu-id="c5035-2045">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2045">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2046">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2046">Definition</span></span>

<span data-ttu-id="c5035-2047">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2047">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2048">Regex_india_permanent_account_number 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2048">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2049">Keyword_india_permanent_account_number에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2049">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="c5035-2050">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2050">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2051">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2051">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="c5035-2052">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2052">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="c5035-2053">Permanent Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2053">Permanent Account Number</span></span> 
- <span data-ttu-id="c5035-2054">PAN
</span><span class="sxs-lookup"><span data-stu-id="c5035-2054">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="c5035-2055">인도 고유 ID(Aadhaar) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2055">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2056">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2056">Format</span></span>

<span data-ttu-id="c5035-2057">선택적 공백 또는 대시를 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2057">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2058">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2058">Pattern</span></span>

<span data-ttu-id="c5035-2059">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2059">12 digits:</span></span>
- <span data-ttu-id="c5035-2060">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2060">Four digits</span></span> 
- <span data-ttu-id="c5035-2061">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="c5035-2061">An optional space or dash</span></span> 
- <span data-ttu-id="c5035-2062">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2062">Four digits</span></span> 
- <span data-ttu-id="c5035-2063">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="c5035-2063">An optional space or dash</span></span> 
- <span data-ttu-id="c5035-2064">검사 숫자에 해당하는 마지막 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2064">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2065">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2065">Checksum</span></span>

<span data-ttu-id="c5035-2066">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2066">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2067">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2067">Definition</span></span>

<span data-ttu-id="c5035-p133">DLP 정책은 이러한 종류의 중요 한 정보를 감지 했습니다 판단 85%에 근접 300 자 내에 있는 경우,: Func_india_aadhaar 함수는 패턴과 일치 하는 콘텐츠를 찾습니다. Keyword_india_aadhar에서 키워드를 발견 됩니다. 체크섬을 전달합니다. DLP 정책은 이러한 종류의 중요 한 정보를 감지 했습니다 판단 75%에 근접 300 자 내에 있는 경우,: Func_india_aadhaar 함수는 패턴과 일치 하는 콘텐츠를 찾습니다. 체크섬을 전달합니다. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="c5035-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="c5035-2074">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2074">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="c5035-2075">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="c5035-2075">Keyword_india_aadhar</span></span>
- <span data-ttu-id="c5035-2076">Aadhar</span><span class="sxs-lookup"><span data-stu-id="c5035-2076">Aadhar</span></span>
- <span data-ttu-id="c5035-2077">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="c5035-2077">Aadhaar</span></span>
- <span data-ttu-id="c5035-2078">UID</span><span class="sxs-lookup"><span data-stu-id="c5035-2078">UID</span></span>
- <span data-ttu-id="c5035-2079">आधार</span><span class="sxs-lookup"><span data-stu-id="c5035-2079">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="c5035-2080">인도네시아 ID 카드(KTP) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2080">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2081">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2081">Format</span></span>

<span data-ttu-id="c5035-2082">선택적으로 마침표를 포함하는 16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2082">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2083">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2083">Pattern</span></span>

<span data-ttu-id="c5035-2084">16자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2084">16 digits:</span></span>
- <span data-ttu-id="c5035-2085">2자리 시/도 코드 </span><span class="sxs-lookup"><span data-stu-id="c5035-2085">Two-digit province code</span></span> 
- <span data-ttu-id="c5035-2086">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="c5035-2086">A period (optional)</span></span> 
- <span data-ttu-id="c5035-2087">2자리 지역 또는 구/군/시 코드 </span><span class="sxs-lookup"><span data-stu-id="c5035-2087">Two-digit regency or city code</span></span> 
- <span data-ttu-id="c5035-2088">2자리 소구역 코드 </span><span class="sxs-lookup"><span data-stu-id="c5035-2088">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="c5035-2089">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="c5035-2089">A period (optional)</span></span> 
- <span data-ttu-id="c5035-2090">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2090">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="c5035-2091">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="c5035-2091">A period (optional)</span></span> 
- <span data-ttu-id="c5035-2092">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2092">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2093">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2093">Checksum</span></span>

<span data-ttu-id="c5035-2094">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2094">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2095">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2095">Definition</span></span>

<span data-ttu-id="c5035-2096">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2096">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2097">Regex_indonesia_id_card 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2097">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2098">Keyword_indonesia_id_card에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2098">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="c5035-2099">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2099">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2100">Regex_indonesia_id_card 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2100">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2101">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2101">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="c5035-2102">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="c5035-2102">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="c5035-2103">KTP</span><span class="sxs-lookup"><span data-stu-id="c5035-2103">KTP</span></span>
- <span data-ttu-id="c5035-2104">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="c5035-2104">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="c5035-2105">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="c5035-2105">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="c5035-2106">IBAN(국제 은행 계좌 번호)</span><span class="sxs-lookup"><span data-stu-id="c5035-2106">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2107">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2107">Format</span></span>

<span data-ttu-id="c5035-2108">국가 코드 (처음 두) 더하기 bban 번호 (최대 30 개의 문자) plus 자리 숫자 (두 자리 숫자) 확인</span><span class="sxs-lookup"><span data-stu-id="c5035-2108">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2109">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2109">Pattern</span></span>

<span data-ttu-id="c5035-2110">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2110">Pattern must include all of the following:</span></span>

- <span data-ttu-id="c5035-2111">두 문자로 된 국가 코드</span><span class="sxs-lookup"><span data-stu-id="c5035-2111">Two-letter country code</span></span>
- <span data-ttu-id="c5035-2112">두 검사 자리 숫자 (선택 사항 공간을 앞에 오는)</span><span class="sxs-lookup"><span data-stu-id="c5035-2112">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="c5035-2113">1-7 그룹 4 개의 문자 또는 숫자 (공백으로 구분 수)</span><span class="sxs-lookup"><span data-stu-id="c5035-2113">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="c5035-2114">1-3 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2114">1-3 letters or digits</span></span>

<span data-ttu-id="c5035-p134">각 국가 대 한 형식은 약간 다릅니다. IBAN 중요 한 정보 유형에서는 이러한 60 국가 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="c5035-2117">ad, ae, a에서에서 달리 ba, 배경, bh, 채널, cr, cy, cz, de, 진한, do, ee, es, 무선, 중, fr, gb, ge, gi, gl가, hr, 될 hu, 즉, 일리노이은 그, kw, kz, 파운드, li, lt, lu, lv, mc, md, me, mk, mr, 체, 뮤 nl, 아니요 pl, pt, 되는, rs, sa, se, si, sk, sm, 조지아 주, tr, vg</span><span class="sxs-lookup"><span data-stu-id="c5035-2117">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2118">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2118">Checksum</span></span>

<span data-ttu-id="c5035-2119">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2119">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2120">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2120">Definition</span></span>

<span data-ttu-id="c5035-2121">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2121">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2122">Func_iban 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2122">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2123">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2123">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2124">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2124">Keywords</span></span>

<span data-ttu-id="c5035-2125">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2125">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="c5035-2126">IP 주소</span><span class="sxs-lookup"><span data-stu-id="c5035-2126">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2127">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2127">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="c5035-2128">IPv4:</span><span class="sxs-lookup"><span data-stu-id="c5035-2128">IPv4:</span></span>
<span data-ttu-id="c5035-2129">IPv4 주소의 서식 있는 버전(마침표 있음) 및 서식 없는 버전(마침표 없음)으로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2129">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="c5035-2130">IPv6:</span><span class="sxs-lookup"><span data-stu-id="c5035-2130">IPv6:</span></span>
<span data-ttu-id="c5035-2131">서식 있는(콜론 포함) IPv6 번호로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2131">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2132">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2132">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2133">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2133">Checksum</span></span>

<span data-ttu-id="c5035-2134">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2134">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2135">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2135">Definition</span></span>

<span data-ttu-id="c5035-2136">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2136">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2137">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2137">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2138">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2138">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="c5035-2139">IPv4의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2139">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2140">Regex_ipv4_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2140">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2141">Keyword_ipaddress의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2141">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="c5035-2142">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2142">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2143">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2143">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2144">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2144">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2145">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2145">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="c5035-2146">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="c5035-2146">Keyword_ipaddress</span></span>

- <span data-ttu-id="c5035-2147">IP(이 키워드는 대/소문자를 구분함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2147">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="c5035-2148">ip address
</span><span class="sxs-lookup"><span data-stu-id="c5035-2148">ip address</span></span> 
- <span data-ttu-id="c5035-2149">ip addresses</span><span class="sxs-lookup"><span data-stu-id="c5035-2149">ip addresses</span></span>
- <span data-ttu-id="c5035-2150">internet protocol</span><span class="sxs-lookup"><span data-stu-id="c5035-2150">internet protocol</span></span>
- <span data-ttu-id="c5035-2151">
IP-כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="c5035-2151">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="c5035-2152">병 (ICD-10-CM)의 국제 분류</span><span class="sxs-lookup"><span data-stu-id="c5035-2152">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2153">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2153">Format</span></span>

<span data-ttu-id="c5035-2154">사전</span><span class="sxs-lookup"><span data-stu-id="c5035-2154">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2155">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2155">Pattern</span></span>

<span data-ttu-id="c5035-2156">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2156">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2157">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2157">Checksum</span></span>

<span data-ttu-id="c5035-2158">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2158">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2159">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2159">Definition</span></span>

<span data-ttu-id="c5035-2160">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2160">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2161">Dictionary_icd_10_cm에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2161">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="c5035-2162">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2162">Keywords</span></span>

<span data-ttu-id="c5035-p135">Dictionary_icd_10_cm 키워드 사전에 있는 모든 용어는 기반으로는 [국제 병 분류, 10 번째 수정 버전, 임상 수정 (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604)합니다. 이 형식은 보험 코드 하지 용어에 대해서만 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="c5035-2165">병 (ICD-9-CM)의 국제 분류</span><span class="sxs-lookup"><span data-stu-id="c5035-2165">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2166">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2166">Format</span></span>

<span data-ttu-id="c5035-2167">사전</span><span class="sxs-lookup"><span data-stu-id="c5035-2167">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2168">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2168">Pattern</span></span>

<span data-ttu-id="c5035-2169">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2169">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2170">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2170">Checksum</span></span>

<span data-ttu-id="c5035-2171">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2172">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2172">Definition</span></span>

<span data-ttu-id="c5035-2173">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2173">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2174">Dictionary_icd_9_cm에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2174">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2175">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2175">Keywords</span></span>

<span data-ttu-id="c5035-p136">Dictionary_icd_9_cm 키워드 사전에 있는 모든 용어를 기반으로는 [국제 병 분류, 번째 수정 버전, 임상 수정 (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605)합니다. 이 형식은 보험 코드 하지 용어에 대해서만 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="c5035-2178">아일랜드 PPS(개인 공공 서비스) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2178">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2179">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2179">Format</span></span>

<span data-ttu-id="c5035-2180">31 10 진수 2012) (될때까지 이전 형식:</span><span class="sxs-lookup"><span data-stu-id="c5035-2180">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="c5035-2181">7자리 숫자와 1-2개 문자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2181">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="c5035-2182">새 형식 (1 Jan 2013 여운 및):</span><span class="sxs-lookup"><span data-stu-id="c5035-2182">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="c5035-2183">7자리 숫자와 2개 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-2183">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2184">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2184">Pattern</span></span>

<span data-ttu-id="c5035-2185">31 10 진수 2012) (될때까지 이전 형식:</span><span class="sxs-lookup"><span data-stu-id="c5035-2185">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="c5035-2186">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2186">Seven digits</span></span> 
- <span data-ttu-id="c5035-2187">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2187">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="c5035-2188">새 형식 (1 Jan 2013 여운 및):</span><span class="sxs-lookup"><span data-stu-id="c5035-2188">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="c5035-2189">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2189">Seven digits</span></span> 
- <span data-ttu-id="c5035-2190">알파벳 검사 숫자에 해당하는 문자 1개(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="c5035-2190">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="c5035-2191">문자 "A" 또는 "H"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2191">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2192">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2192">Checksum</span></span>

<span data-ttu-id="c5035-2193">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2194">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2194">Definition</span></span>

<span data-ttu-id="c5035-2195">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2196">Func_ireland_pps 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2196">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2197">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2197">One of the following is true:</span></span>
    - <span data-ttu-id="c5035-2198">Keyword_ireland_pps에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2198">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="c5035-2199">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2199">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="c5035-2200">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2200">The checksum passes.</span></span>

<span data-ttu-id="c5035-2201">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2201">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2202">Func_ireland_pps 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2202">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2203">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2203">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2204">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2204">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="c5035-2205">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="c5035-2205">Keyword_ireland_pps</span></span>

- <span data-ttu-id="c5035-2206">Personal Public Service Number 
</span><span class="sxs-lookup"><span data-stu-id="c5035-2206">Personal Public Service Number</span></span> 
- <span data-ttu-id="c5035-2207">PPS Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2207">PPS Number</span></span> 
- <span data-ttu-id="c5035-2208">PPS Num
</span><span class="sxs-lookup"><span data-stu-id="c5035-2208">PPS Num</span></span> 
- <span data-ttu-id="c5035-2209">PPS No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2209">PPS No.</span></span> 
- <span data-ttu-id="c5035-2210">PPS #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2210">PPS #</span></span> 
- <span data-ttu-id="c5035-2211">PPS#
</span><span class="sxs-lookup"><span data-stu-id="c5035-2211">PPS#</span></span> 
- <span data-ttu-id="c5035-2212">PPSN
</span><span class="sxs-lookup"><span data-stu-id="c5035-2212">PPSN</span></span> 
- <span data-ttu-id="c5035-2213">Public Services Card
</span><span class="sxs-lookup"><span data-stu-id="c5035-2213">Public Services Card</span></span> 
- <span data-ttu-id="c5035-2214">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="c5035-2214">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="c5035-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="c5035-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="c5035-2217">PSP
</span><span class="sxs-lookup"><span data-stu-id="c5035-2217">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="c5035-2218">이스라엘 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2218">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2219">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2219">Format</span></span>

<span data-ttu-id="c5035-2220">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2220">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2221">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2221">Pattern</span></span>

<span data-ttu-id="c5035-2222">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="c5035-2222">Formatted:</span></span>
- <span data-ttu-id="c5035-2223">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2223">Two digits</span></span> 
- <span data-ttu-id="c5035-2224">대시 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-2224">A dash</span></span> 
- <span data-ttu-id="c5035-2225">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2225">Three digits</span></span> 
- <span data-ttu-id="c5035-2226">대시 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-2226">A dash</span></span> 
- <span data-ttu-id="c5035-2227">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2227">Eight digits</span></span>

<span data-ttu-id="c5035-2228">서식 없음:</span><span class="sxs-lookup"><span data-stu-id="c5035-2228">Unformatted:</span></span>
- <span data-ttu-id="c5035-2229">13자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2229">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2230">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2230">Checksum</span></span>

<span data-ttu-id="c5035-2231">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2232">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2232">Definition</span></span>

<span data-ttu-id="c5035-2233">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2234">Regex_israel_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2234">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2235">Keyword_israel_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2235">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2236">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2236">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="c5035-2237">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2237">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="c5035-2238">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2238">Bank Account Number</span></span> 
- <span data-ttu-id="c5035-2239">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="c5035-2239">Bank Account</span></span> 
- <span data-ttu-id="c5035-2240">Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2240">Account Number</span></span> 
- <span data-ttu-id="c5035-2241">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="c5035-2241">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="c5035-2242">이스라엘 국가 ID</span><span class="sxs-lookup"><span data-stu-id="c5035-2242">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2243">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2243">Format</span></span>

<span data-ttu-id="c5035-2244">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2245">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2245">Pattern</span></span>

<span data-ttu-id="c5035-2246">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2247">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2247">Checksum</span></span>

<span data-ttu-id="c5035-2248">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2248">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2249">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2249">Definition</span></span>

<span data-ttu-id="c5035-2250">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2251">Func_israeli_national_id_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2251">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2252">Keyword_Israel_National_ID의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2252">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="c5035-2253">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2253">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2254">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2254">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="c5035-2255">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="c5035-2255">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="c5035-2256">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="c5035-2256">מספר זהות</span></span> 
- <span data-ttu-id="c5035-2257">National ID Number</span><span class="sxs-lookup"><span data-stu-id="c5035-2257">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="c5035-2258">이탈리아 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2258">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2259">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2259">Format</span></span>

<span data-ttu-id="c5035-2260">10개의 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="c5035-2260">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2261">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2261">Pattern</span></span>

- <span data-ttu-id="c5035-2262">10개의 문자 및 숫자 조합:</span><span class="sxs-lookup"><span data-stu-id="c5035-2262">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="c5035-2263">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2263">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-2264">문자 "A" 또는 "V"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2264">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-2265">7개 문자(대/소문자 구분 안 함), 숫자 또는 밑줄 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-2265">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="c5035-2266">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2266">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2267">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2267">Checksum</span></span>

<span data-ttu-id="c5035-2268">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2269">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2269">Definition</span></span>

<span data-ttu-id="c5035-2270">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2271">Regex_italy_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2271">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2272">Keyword_italy_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2272">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2273">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2273">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="c5035-2274">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2274">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="c5035-2275">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="c5035-2275">numero di patente di guida</span></span> 
- <span data-ttu-id="c5035-2276">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="c5035-2276">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="c5035-2277">일본 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2277">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2278">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2278">Format</span></span>

<span data-ttu-id="c5035-2279">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2279">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2280">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2280">Pattern</span></span>

<span data-ttu-id="c5035-2281">은행 계좌 번호:</span><span class="sxs-lookup"><span data-stu-id="c5035-2281">Bank account number:</span></span>
- <span data-ttu-id="c5035-2282">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2282">Seven or eight digits</span></span>
- <span data-ttu-id="c5035-2283">은행 계좌 지점 코드:</span><span class="sxs-lookup"><span data-stu-id="c5035-2283">Bank account branch code:</span></span>
- <span data-ttu-id="c5035-2284">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2284">Four digits</span></span> 
- <span data-ttu-id="c5035-2285">공백 또는 대시(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="c5035-2285">A space or dash (optional)</span></span> 
- <span data-ttu-id="c5035-2286">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2286">Three digits</span></span>

<span data-ttu-id="c5035-2287">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2287">Checksum</span></span>

<span data-ttu-id="c5035-2288">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2288">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2289">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2289">Definition</span></span>

<span data-ttu-id="c5035-2290">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2290">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2291">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2291">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2292">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2292">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="c5035-2293">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2293">One of the following is true:</span></span>
- <span data-ttu-id="c5035-2294">Func_jp_bank_account_branch_code 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2294">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2295">Keyword_jp_bank_branch_code의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2295">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="c5035-2296">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2296">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2297">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2297">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2298">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2298">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2299">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2299">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="c5035-2300">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="c5035-2300">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="c5035-2301">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2301">Checking Account Number</span></span> 
- <span data-ttu-id="c5035-2302">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="c5035-2302">Checking Account</span></span> 
- <span data-ttu-id="c5035-2303">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2303">Checking Account #</span></span> 
- <span data-ttu-id="c5035-2304">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2304">Checking Acct Number</span></span> 
- <span data-ttu-id="c5035-2305">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2305">Checking Acct #</span></span> 
- <span data-ttu-id="c5035-2306">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2306">Checking Acct No.</span></span> 
- <span data-ttu-id="c5035-2307">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2307">Checking Account No.</span></span> 
- <span data-ttu-id="c5035-2308">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2308">Bank Account Number</span></span> 
- <span data-ttu-id="c5035-2309">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="c5035-2309">Bank Account</span></span> 
- <span data-ttu-id="c5035-2310">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2310">Bank Account #</span></span> 
- <span data-ttu-id="c5035-2311">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2311">Bank Acct Number</span></span> 
- <span data-ttu-id="c5035-2312">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2312">Bank Acct #</span></span> 
- <span data-ttu-id="c5035-2313">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2313">Bank Acct No.</span></span> 
- <span data-ttu-id="c5035-2314">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2314">Bank Account No.</span></span> 
- <span data-ttu-id="c5035-2315">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2315">Savings Account Number</span></span> 
- <span data-ttu-id="c5035-2316">절감 계정</span><span class="sxs-lookup"><span data-stu-id="c5035-2316">Savings Account</span></span> 
- <span data-ttu-id="c5035-2317">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2317">Savings Account #</span></span> 
- <span data-ttu-id="c5035-2318">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2318">Savings Acct Number</span></span> 
- <span data-ttu-id="c5035-2319">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2319">Savings Acct #</span></span> 
- <span data-ttu-id="c5035-2320">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2320">Savings Acct No.</span></span> 
- <span data-ttu-id="c5035-2321">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2321">Savings Account No.</span></span> 
- <span data-ttu-id="c5035-2322">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2322">Debit Account Number</span></span> 
- <span data-ttu-id="c5035-2323">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="c5035-2323">Debit Account</span></span> 
- <span data-ttu-id="c5035-2324">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2324">Debit Account #</span></span> 
- <span data-ttu-id="c5035-2325">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2325">Debit Acct Number</span></span> 
- <span data-ttu-id="c5035-2326">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2326">Debit Acct #</span></span> 
- <span data-ttu-id="c5035-2327">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2327">Debit Acct No.</span></span> 
- <span data-ttu-id="c5035-2328">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2328">Debit Account No.</span></span> 
- <span data-ttu-id="c5035-2329">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="c5035-2329">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="c5035-2330"># アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="c5035-2330">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="c5035-2331">#勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="c5035-2331">＃勘定の確認</span></span> 
- <span data-ttu-id="c5035-2332">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="c5035-2332">勘定番号の確認</span></span> 
- <span data-ttu-id="c5035-2333">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="c5035-2333">口座番号の確認</span></span> 
- <span data-ttu-id="c5035-2334">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="c5035-2334">銀行口座番号</span></span> 
- <span data-ttu-id="c5035-2335">銀行口座</span><span class="sxs-lookup"><span data-stu-id="c5035-2335">銀行口座</span></span> 
- <span data-ttu-id="c5035-2336">銀行口座 #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2336">銀行口座＃</span></span> 
- <span data-ttu-id="c5035-2337">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2337">銀行の勘定番号</span></span> 
- <span data-ttu-id="c5035-2338">銀行のacct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2338">銀行のacct＃</span></span> 
- <span data-ttu-id="c5035-2339">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="c5035-2339">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="c5035-2340">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="c5035-2340">銀行口座番号</span></span>
- <span data-ttu-id="c5035-2341">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2341">普通預金口座番号</span></span> 
- <span data-ttu-id="c5035-2342">預金口座
</span><span class="sxs-lookup"><span data-stu-id="c5035-2342">預金口座</span></span> 
- <span data-ttu-id="c5035-2343">貯蓄口座 #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2343">貯蓄口座＃</span></span> 
- <span data-ttu-id="c5035-2344">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="c5035-2344">貯蓄勘定の数</span></span> 
- <span data-ttu-id="c5035-2345">貯蓄勘定 #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2345">貯蓄勘定＃</span></span> 
- <span data-ttu-id="c5035-2346">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2346">貯蓄勘定番号</span></span> 
- <span data-ttu-id="c5035-2347">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2347">普通預金口座番号</span></span> 
- <span data-ttu-id="c5035-2348">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2348">引き落とし口座番号</span></span> 
- <span data-ttu-id="c5035-2349">口座番号</span><span class="sxs-lookup"><span data-stu-id="c5035-2349">口座番号</span></span> 
- <span data-ttu-id="c5035-2350">口座番号 #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2350">口座番号＃</span></span> 
- <span data-ttu-id="c5035-2351">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2351">デビットのacct番号</span></span> 
- <span data-ttu-id="c5035-2352">デビット勘定 #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2352">デビット勘定＃</span></span> 
- <span data-ttu-id="c5035-2353">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2353">デビットACCTの番号</span></span> 
- <span data-ttu-id="c5035-2354">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2354">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="c5035-2355">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="c5035-2355">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="c5035-2356">Otemachi</span><span class="sxs-lookup"><span data-stu-id="c5035-2356">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="c5035-2357">일본 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2357">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2358">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2358">Format</span></span>

<span data-ttu-id="c5035-2359">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2359">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2360">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2360">Pattern</span></span>

<span data-ttu-id="c5035-2361">12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2361">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2362">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2362">Checksum</span></span>

<span data-ttu-id="c5035-2363">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2363">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2364">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2364">Definition</span></span>

<span data-ttu-id="c5035-2365">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2366">Func_jp_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2366">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2367">Keyword_jp_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2367">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2368">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2368">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="c5035-2369">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2369">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="c5035-2370">dl#
</span><span class="sxs-lookup"><span data-stu-id="c5035-2370">dl#</span></span> 
- <span data-ttu-id="c5035-2371">DL #</span><span class="sxs-lookup"><span data-stu-id="c5035-2371">DL＃</span></span> 
- <span data-ttu-id="c5035-2372">dl #</span><span class="sxs-lookup"><span data-stu-id="c5035-2372">dls#</span></span> 
- <span data-ttu-id="c5035-2373">DL #</span><span class="sxs-lookup"><span data-stu-id="c5035-2373">DLS＃</span></span> 
- <span data-ttu-id="c5035-2374">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-2374">driver license</span></span> 
- <span data-ttu-id="c5035-2375">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-2375">driver licenses</span></span> 
- <span data-ttu-id="c5035-2376">운전 면허</span><span class="sxs-lookup"><span data-stu-id="c5035-2376">drivers license</span></span> 
- <span data-ttu-id="c5035-2377">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-2377">driver's license</span></span> 
- <span data-ttu-id="c5035-2378">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-2378">drivers licenses</span></span> 
- <span data-ttu-id="c5035-2379">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-2379">driver's licenses</span></span> 
- <span data-ttu-id="c5035-2380">driving licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-2380">driving licence</span></span> 
- <span data-ttu-id="c5035-2381">lic #</span><span class="sxs-lookup"><span data-stu-id="c5035-2381">lic#</span></span> 
- <span data-ttu-id="c5035-2382">LIC #</span><span class="sxs-lookup"><span data-stu-id="c5035-2382">LIC＃</span></span> 
- <span data-ttu-id="c5035-2383">lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-2383">lics#</span></span> 
- <span data-ttu-id="c5035-2384">상태 id</span><span class="sxs-lookup"><span data-stu-id="c5035-2384">state id</span></span> 
- <span data-ttu-id="c5035-2385">state identification
</span><span class="sxs-lookup"><span data-stu-id="c5035-2385">state identification</span></span> 
- <span data-ttu-id="c5035-2386">state identification number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2386">state identification number</span></span> 
- <span data-ttu-id="c5035-2387">低所得国 #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2387">低所得国＃</span></span> 
- <span data-ttu-id="c5035-2388">免許証
</span><span class="sxs-lookup"><span data-stu-id="c5035-2388">免許証</span></span> 
- <span data-ttu-id="c5035-2389">状態ID</span><span class="sxs-lookup"><span data-stu-id="c5035-2389">状態ID</span></span>
- <span data-ttu-id="c5035-2390">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="c5035-2390">状態の識別</span></span> 
- <span data-ttu-id="c5035-2391">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2391">状態の識別番号</span></span> 
- <span data-ttu-id="c5035-2392">運転免許
</span><span class="sxs-lookup"><span data-stu-id="c5035-2392">運転免許</span></span> 
- <span data-ttu-id="c5035-2393">運転免許証
</span><span class="sxs-lookup"><span data-stu-id="c5035-2393">運転免許証</span></span> 
- <span data-ttu-id="c5035-2394">運転免許証番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2394">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="c5035-2395">일본 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2395">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2396">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2396">Format</span></span>

<span data-ttu-id="c5035-2397">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2397">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2398">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2398">Pattern</span></span>

<span data-ttu-id="c5035-2399">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2399">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2400">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2400">Checksum</span></span>

<span data-ttu-id="c5035-2401">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2401">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2402">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2402">Definition</span></span>

<span data-ttu-id="c5035-2403">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2404">Func_jp_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2404">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2405">Keyword_jp_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2405">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2406">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2406">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="c5035-2407">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-2407">Keyword_jp_passport</span></span>

- <span data-ttu-id="c5035-2408">パスポート
</span><span class="sxs-lookup"><span data-stu-id="c5035-2408">パスポート</span></span> 
- <span data-ttu-id="c5035-2409">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2409">パスポート番号</span></span> 
- <span data-ttu-id="c5035-2410">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="c5035-2410">パスポートのNum</span></span> 
- <span data-ttu-id="c5035-2411">パスポート #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2411">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="c5035-2412">일본 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2412">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2413">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2413">Format</span></span>

<span data-ttu-id="c5035-2414">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2414">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2415">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2415">Pattern</span></span>

<span data-ttu-id="c5035-2416">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2416">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2417">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2417">Checksum</span></span>

<span data-ttu-id="c5035-2418">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2418">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2419">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2419">Definition</span></span>

<span data-ttu-id="c5035-2420">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2420">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2421">Func_jp_resident_registration_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2421">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2422">Keyword_jp_resident_registration_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2422">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2423">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2423">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="c5035-2424">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2424">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="c5035-2425">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="c5035-2425">Resident Registration Number</span></span>
- <span data-ttu-id="c5035-2426">Resident Register Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2426">Resident Register Number</span></span> 
- <span data-ttu-id="c5035-2427">Residents Basic Registry Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2427">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="c5035-2428">Resident Registration No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2428">Resident Registration No.</span></span> 
- <span data-ttu-id="c5035-2429">Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2429">Resident Register No.</span></span> 
- <span data-ttu-id="c5035-2430">Residents Basic Registry No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2430">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="c5035-2431">Basic Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2431">Basic Resident Register No.</span></span> 
- <span data-ttu-id="c5035-2432">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="c5035-2432">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="c5035-2433">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2433">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="c5035-2434">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="c5035-2434">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="c5035-2435">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2435">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="c5035-2436">일본 SIN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="c5035-2436">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2437">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2437">Format</span></span>

<span data-ttu-id="c5035-2438">7-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2438">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2439">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2439">Pattern</span></span>

<span data-ttu-id="c5035-2440">7-12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2440">7-12 digits:</span></span>
- <span data-ttu-id="c5035-2441">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2441">Four digits</span></span> 
- <span data-ttu-id="c5035-2442">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="c5035-2442">A hyphen (optional)</span></span> 
- <span data-ttu-id="c5035-2443">6 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="c5035-2443">Six digits OR</span></span>
- <span data-ttu-id="c5035-2444">7-12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2444">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2445">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2445">Checksum</span></span>

<span data-ttu-id="c5035-2446">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2446">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2447">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2447">Definition</span></span>

<span data-ttu-id="c5035-2448">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2448">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2449">Func_jp_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2449">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2450">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2450">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="c5035-2451">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2451">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2452">Func_jp_sin_pre_1997 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2452">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2453">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2453">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2454">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2454">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="c5035-2455">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="c5035-2455">Keyword_jp_sin</span></span>

- <span data-ttu-id="c5035-2456">Social Insurance No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2456">Social Insurance No.</span></span> 
- <span data-ttu-id="c5035-2457">Social Insurance Num
</span><span class="sxs-lookup"><span data-stu-id="c5035-2457">Social Insurance Num</span></span> 
- <span data-ttu-id="c5035-2458">Social Insurance Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2458">Social Insurance Number</span></span> 
- <span data-ttu-id="c5035-2459">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="c5035-2459">社会保険のテンキー</span></span> 
- <span data-ttu-id="c5035-2460">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2460">社会保険番号</span></span> 
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="c5035-2461">말레이시아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2461">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2462">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2462">Format</span></span>

<span data-ttu-id="c5035-2463">선택적으로 하이픈을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2463">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2464">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2464">Pattern</span></span>

<span data-ttu-id="c5035-2465">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2465">12 digits:</span></span>
- <span data-ttu-id="c5035-2466">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2466">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="c5035-2467">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="c5035-2467">A dash (optional)</span></span> 
- <span data-ttu-id="c5035-2468">2개 문자로 이루어진 출생지 코드 </span><span class="sxs-lookup"><span data-stu-id="c5035-2468">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="c5035-2469">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="c5035-2469">A dash (optional)</span></span> 
- <span data-ttu-id="c5035-2470">임의의 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2470">Three random digits</span></span> 
- <span data-ttu-id="c5035-2471">1자리 성별 코드</span><span class="sxs-lookup"><span data-stu-id="c5035-2471">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2472">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2472">Checksum</span></span>

<span data-ttu-id="c5035-2473">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2474">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2474">Definition</span></span>

<span data-ttu-id="c5035-2475">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2476">Regex_malaysia_id_card_number 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2476">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2477">Keyword_malaysia_id_card_number에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2477">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2478">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2478">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="c5035-2479">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2479">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="c5035-2480">MyKad</span><span class="sxs-lookup"><span data-stu-id="c5035-2480">MyKad</span></span> 
- <span data-ttu-id="c5035-2481">Identity Card</span><span class="sxs-lookup"><span data-stu-id="c5035-2481">Identity Card</span></span> 
- <span data-ttu-id="c5035-2482">ID 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-2482">ID Card</span></span> 
- <span data-ttu-id="c5035-2483">Id 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-2483">Identification Card</span></span> 
- <span data-ttu-id="c5035-2484">Digital Application Card
</span><span class="sxs-lookup"><span data-stu-id="c5035-2484">Digital Application Card</span></span> 
- <span data-ttu-id="c5035-2485">Kad Akuan Diri
</span><span class="sxs-lookup"><span data-stu-id="c5035-2485">Kad Akuan Diri</span></span> 
- <span data-ttu-id="c5035-2486">Kad Aplikasi Digital
</span><span class="sxs-lookup"><span data-stu-id="c5035-2486">Kad Aplikasi Digital</span></span> 
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="c5035-2487">네덜란드 시민 서비스(BSN) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2487">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2488">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2488">Format</span></span>

<span data-ttu-id="c5035-2489">선택적으로 공백을 포함하는 8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2489">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2490">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2490">Pattern</span></span>

<span data-ttu-id="c5035-2491">8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2491">8-9 digits:</span></span>
- <span data-ttu-id="c5035-2492">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2492">Three digits</span></span> 
- <span data-ttu-id="c5035-2493">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="c5035-2493">A space (optional)</span></span> 
- <span data-ttu-id="c5035-2494">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2494">Three digits</span></span> 
- <span data-ttu-id="c5035-2495">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="c5035-2495">A space (optional)</span></span> 
- <span data-ttu-id="c5035-2496">2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2496">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2497">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2497">Checksum</span></span>

<span data-ttu-id="c5035-2498">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2498">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2499">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2499">Definition</span></span>

<span data-ttu-id="c5035-2500">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2500">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2501">Func_netherlands_bsn 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2501">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2502">Keyword_netherlands_bsn에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2502">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="c5035-2503">Func_eu_date2 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2503">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="c5035-2504">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2504">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2505">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2505">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="c5035-2506">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="c5035-2506">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="c5035-2507">Citizen service number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2507">Citizen service number</span></span> 
- <span data-ttu-id="c5035-2508">BSN

</span><span class="sxs-lookup"><span data-stu-id="c5035-2508">BSN</span></span> 
- <span data-ttu-id="c5035-2509">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-2509">Burgerservicenummer</span></span> 
- <span data-ttu-id="c5035-2510">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-2510">Sofinummer</span></span> 
- <span data-ttu-id="c5035-2511">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-2511">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="c5035-2512">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="c5035-2512">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="c5035-2513">뉴질랜드 보건부 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2513">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2514">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2514">Format</span></span>

<span data-ttu-id="c5035-2515">3개 문자, 공백 1개(선택 사항) 및 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2515">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2516">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2516">Pattern</span></span>

<span data-ttu-id="c5035-2517">3 개 문자 (하지 대/소문자 구분)는 공간 (선택 사항) 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2517">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2518">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2518">Checksum</span></span>

<span data-ttu-id="c5035-2519">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2519">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2520">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2520">Definition</span></span>

<span data-ttu-id="c5035-2521">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2521">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2522">Func_new_zealand_ministry_of_health_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2522">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2523">Keyword_nz_terms의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2523">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="c5035-2524">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2524">The checksum passes.</span></span>

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

<span data-ttu-id="c5035-2525">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2525">Keywords</span></span>

<span data-ttu-id="c5035-2526">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="c5035-2526">Keyword_nz_terms</span></span>

- <span data-ttu-id="c5035-2527">NHI
</span><span class="sxs-lookup"><span data-stu-id="c5035-2527">NHI</span></span> 
- <span data-ttu-id="c5035-2528">뉴질랜드</span><span class="sxs-lookup"><span data-stu-id="c5035-2528">New Zealand</span></span> 
- <span data-ttu-id="c5035-2529">상태</span><span class="sxs-lookup"><span data-stu-id="c5035-2529">Health</span></span> 
- <span data-ttu-id="c5035-2530">treatment
</span><span class="sxs-lookup"><span data-stu-id="c5035-2530">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="c5035-2531">Norway Identification Number</span><span class="sxs-lookup"><span data-stu-id="c5035-2531">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2532">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2532">Format</span></span>

<span data-ttu-id="c5035-2533">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2533">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2534">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2534">Pattern</span></span>

<span data-ttu-id="c5035-2535">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2535">11 digits:</span></span>
- <span data-ttu-id="c5035-2536">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2536">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="c5035-2537">3자리 개인 번호 </span><span class="sxs-lookup"><span data-stu-id="c5035-2537">Three-digit individual number</span></span> 
- <span data-ttu-id="c5035-2538">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2538">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2539">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2539">Checksum</span></span>

<span data-ttu-id="c5035-2540">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2540">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2541">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2541">Definition</span></span>

<span data-ttu-id="c5035-2542">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2542">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2543">Func_norway_id_number 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2543">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2544">Keyword_norway_id_number에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2544">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="c5035-2545">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2545">The checksum passes.</span></span>
- <span data-ttu-id="c5035-2546">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2546">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2547">Func_norway_id_numbe 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2547">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2548">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2548">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2549">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2549">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="c5035-2550">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2550">Keyword_norway_id_number</span></span>

- <span data-ttu-id="c5035-2551">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="c5035-2551">Personal identification number</span></span>
- <span data-ttu-id="c5035-2552">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="c5035-2552">Norwegian ID Number</span></span>
- <span data-ttu-id="c5035-2553">ID Number</span><span class="sxs-lookup"><span data-stu-id="c5035-2553">ID Number</span></span>
- <span data-ttu-id="c5035-2554">Identification</span><span class="sxs-lookup"><span data-stu-id="c5035-2554">Identification</span></span>
- <span data-ttu-id="c5035-2555">Personnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-2555">Personnummer</span></span>
- <span data-ttu-id="c5035-2556">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="c5035-2556">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="c5035-2557">필리핀 통합 다목적 ID 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2557">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2558">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2558">Format</span></span>

<span data-ttu-id="c5035-2559">하이픈으로 구분된 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2559">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2560">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2560">Pattern</span></span>

<span data-ttu-id="c5035-2561">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2561">12 digits:</span></span>
- <span data-ttu-id="c5035-2562">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2562">Four digits</span></span> 
- <span data-ttu-id="c5035-2563">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-2563">A hyphen</span></span> 
- <span data-ttu-id="c5035-2564">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2564">Seven digits</span></span> 
- <span data-ttu-id="c5035-2565">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-2565">A hyphen</span></span> 
- <span data-ttu-id="c5035-2566">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2566">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2567">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2567">Checksum</span></span>

<span data-ttu-id="c5035-2568">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2568">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2569">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2569">Definition</span></span>

<span data-ttu-id="c5035-2570">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2571">Regex_philippines_unified_id 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2571">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2572">Keyword_philippines_id에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2572">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2573">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2573">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="c5035-2574">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="c5035-2574">Keyword_philippines_id</span></span>

- <span data-ttu-id="c5035-2575">Unified Multi-Purpose ID
</span><span class="sxs-lookup"><span data-stu-id="c5035-2575">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="c5035-2576">UMID
</span><span class="sxs-lookup"><span data-stu-id="c5035-2576">UMID</span></span> 
- <span data-ttu-id="c5035-2577">Identity Card</span><span class="sxs-lookup"><span data-stu-id="c5035-2577">Identity Card</span></span> 
- <span data-ttu-id="c5035-2578">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="c5035-2578">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="c5035-2579">폴란드 ID 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-2579">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2580">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2580">Format</span></span>

<span data-ttu-id="c5035-2581">3개의 문자 및 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2581">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2582">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2582">Pattern</span></span>

<span data-ttu-id="c5035-2583">3개의 문자(대/소문자 구분 안 함)와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2583">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2584">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2584">Checksum</span></span>

<span data-ttu-id="c5035-2585">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2586">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2586">Definition</span></span>

<span data-ttu-id="c5035-p138">DLP 정책은 이러한 종류의 중요 한 정보를 감지 했습니다 판단 75%에 근접 300 자 내에 있는 경우,: Func_polish_national_id 함수는 패턴과 일치 하는 콘텐츠를 찾습니다. Keyword_polish_national_id_passport_number에서 키워드를 발견 됩니다. 체크섬을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2590">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2590">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="c5035-2591">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2591">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="c5035-2592">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="c5035-2592">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="c5035-2593">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="c5035-2593">Dowód Tożsamości</span></span> 
- <span data-ttu-id="c5035-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="c5035-p139">dow. os.</span></span> 

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="c5035-2596">폴란드 국가 ID(PESEL)</span><span class="sxs-lookup"><span data-stu-id="c5035-2596">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2597">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2597">Format</span></span>

<span data-ttu-id="c5035-2598">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2598">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2599">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2599">Pattern</span></span>

<span data-ttu-id="c5035-2600">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2600">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2601">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2601">Checksum</span></span>

<span data-ttu-id="c5035-2602">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2602">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2603">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2603">Definition</span></span>

<span data-ttu-id="c5035-2604">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2604">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2605">Func_pesel_identification_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2605">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2606">Keyword_pesel_identification_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2606">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="c5035-2607">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2607">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2608">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2608">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="c5035-2609">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2609">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="c5035-2610">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="c5035-2610">Nr PESEL</span></span>
- <span data-ttu-id="c5035-2611">PESEL</span><span class="sxs-lookup"><span data-stu-id="c5035-2611">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="c5035-2612">폴란드 여권</span><span class="sxs-lookup"><span data-stu-id="c5035-2612">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2613">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2613">Format</span></span>

<span data-ttu-id="c5035-2614">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2614">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2615">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2615">Pattern</span></span>

<span data-ttu-id="c5035-2616">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2616">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2617">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2617">Checksum</span></span>

<span data-ttu-id="c5035-2618">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2618">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2619">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2619">Definition</span></span>

<span data-ttu-id="c5035-2620">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2620">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2621">Func_polish_passport_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2621">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2622">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2622">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="c5035-2623">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2623">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2624">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2624">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="c5035-2625">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2625">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="c5035-2626">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="c5035-2626">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="c5035-2627">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="c5035-2627">Dowód Tożsamości</span></span> 
- <span data-ttu-id="c5035-p140">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="c5035-p140">dow. os.</span></span> 

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="c5035-2630">포르투갈 시민 카드 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2630">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2631">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2631">Format</span></span>

<span data-ttu-id="c5035-2632">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2632">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2633">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2633">Pattern</span></span>

<span data-ttu-id="c5035-2634">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2634">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2635">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2635">Checksum</span></span>

<span data-ttu-id="c5035-2636">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2636">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2637">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2637">Definition</span></span>

<span data-ttu-id="c5035-2638">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2638">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2639">Regex_portugal_citizen_card 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2639">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2640">Keyword_portugal_citizen_card에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2640">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2641">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2641">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="c5035-2642">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="c5035-2642">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="c5035-2643">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="c5035-2643">Citizen Card</span></span>
- <span data-ttu-id="c5035-2644">National ID Card</span><span class="sxs-lookup"><span data-stu-id="c5035-2644">National ID Card</span></span>
- <span data-ttu-id="c5035-2645">CC</span><span class="sxs-lookup"><span data-stu-id="c5035-2645">CC</span></span>
- <span data-ttu-id="c5035-2646">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="c5035-2646">Cartão de Cidadão</span></span>
- <span data-ttu-id="c5035-2647">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="c5035-2647">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="c5035-2648">사우디 아라비아 국가 ID</span><span class="sxs-lookup"><span data-stu-id="c5035-2648">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2649">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2649">Format</span></span>

<span data-ttu-id="c5035-2650">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2650">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2651">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2651">Pattern</span></span>

<span data-ttu-id="c5035-2652">10자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2652">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2653">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2653">Checksum</span></span>

<span data-ttu-id="c5035-2654">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2654">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2655">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2655">Definition</span></span>

<span data-ttu-id="c5035-2656">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2656">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2657">Regex_saudi_arabia_national_id 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2657">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2658">Keyword_saudi_arabia_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2658">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2659">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2659">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="c5035-2660">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="c5035-2660">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="c5035-2661">Identification Card
</span><span class="sxs-lookup"><span data-stu-id="c5035-2661">Identification Card</span></span> 
- <span data-ttu-id="c5035-2662">I card number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2662">I card number</span></span> 
- <span data-ttu-id="c5035-2663">ID 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2663">ID number</span></span> 
- <span data-ttu-id="c5035-2664">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="c5035-2664">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="c5035-2665">싱가포르 NRIC(국가 등록 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2665">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2666">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2666">Format</span></span>

<span data-ttu-id="c5035-2667">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2667">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2668">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2668">Pattern</span></span>

- <span data-ttu-id="c5035-2669">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2669">Nine letters and digits:</span></span>
- <span data-ttu-id="c5035-2670">문자 "F", "G", "S" 또는 "T"(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="c5035-2670">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-2671">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2671">Seven digits</span></span> 
- <span data-ttu-id="c5035-2672">알파벳 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2672">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2673">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2673">Checksum</span></span>

<span data-ttu-id="c5035-2674">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2674">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2675">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2675">Definition</span></span>

<span data-ttu-id="c5035-2676">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2676">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2677">Regex_singapore_nric 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2677">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2678">Keyword_singapore_nric에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2678">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="c5035-2679">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2679">The checksum passes.</span></span>

<span data-ttu-id="c5035-2680">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2681">Regex_singapore_nric 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2681">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2682">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2682">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2683">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2683">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="c5035-2684">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="c5035-2684">Keyword_singapore_nric</span></span>

- <span data-ttu-id="c5035-2685">National Registration Identity Card
</span><span class="sxs-lookup"><span data-stu-id="c5035-2685">National Registration Identity Card</span></span> 
- <span data-ttu-id="c5035-2686">Identity Card Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2686">Identity Card Number</span></span> 
- <span data-ttu-id="c5035-2687">NRIC
</span><span class="sxs-lookup"><span data-stu-id="c5035-2687">NRIC</span></span> 
- <span data-ttu-id="c5035-2688">IC
</span><span class="sxs-lookup"><span data-stu-id="c5035-2688">IC</span></span> 
- <span data-ttu-id="c5035-2689">Foreign Identification Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2689">Foreign Identification Number</span></span> 
- <span data-ttu-id="c5035-2690">FIN
</span><span class="sxs-lookup"><span data-stu-id="c5035-2690">FIN</span></span> 
- <span data-ttu-id="c5035-2691">身份证 </span><span class="sxs-lookup"><span data-stu-id="c5035-2691">身份证</span></span> 
- <span data-ttu-id="c5035-2692">身份證
</span><span class="sxs-lookup"><span data-stu-id="c5035-2692">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="c5035-2693">남아프리카 공화국 식별 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2693">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2694">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2694">Format</span></span>

<span data-ttu-id="c5035-2695">공백을 포함할 수 있는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2695">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2696">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2696">Pattern</span></span>

<span data-ttu-id="c5035-2697">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2697">13 digits:</span></span>
- <span data-ttu-id="c5035-2698">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2698">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="c5035-2699">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2699">Four digits</span></span> 
- <span data-ttu-id="c5035-2700">1자리 시민권 표시 </span><span class="sxs-lookup"><span data-stu-id="c5035-2700">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="c5035-2701">숫자 "8" 또는 "9" </span><span class="sxs-lookup"><span data-stu-id="c5035-2701">The digit "8" or "9"</span></span> 
- <span data-ttu-id="c5035-2702">체크섬 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2702">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2703">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2703">Checksum</span></span>

<span data-ttu-id="c5035-2704">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2704">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2705">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2705">Definition</span></span>

<span data-ttu-id="c5035-2706">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2706">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2707">Func_south_africa_identification_number 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2707">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2708">Keyword_south_africa_identification_number에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2708">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="c5035-2709">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2709">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2710">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2710">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="c5035-2711">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2711">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="c5035-2712">Identity card</span><span class="sxs-lookup"><span data-stu-id="c5035-2712">Identity card</span></span>
- <span data-ttu-id="c5035-2713">ID</span><span class="sxs-lookup"><span data-stu-id="c5035-2713">ID</span></span>
- <span data-ttu-id="c5035-2714">Identification</span><span class="sxs-lookup"><span data-stu-id="c5035-2714">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="c5035-2715">한국 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2715">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2716">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2716">Format</span></span>

<span data-ttu-id="c5035-2717">하이픈을 포함하는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2717">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2718">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2718">Pattern</span></span>

<span data-ttu-id="c5035-2719">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2719">13 digits:</span></span>
- <span data-ttu-id="c5035-2720">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2720">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="c5035-2721">하이픈</span><span class="sxs-lookup"><span data-stu-id="c5035-2721">A hyphen</span></span> 
- <span data-ttu-id="c5035-2722">세기 및 성별에 따라 결정되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2722">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="c5035-2723">4자리 출생 지역 코드 </span><span class="sxs-lookup"><span data-stu-id="c5035-2723">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="c5035-2724">앞 번호가 동일한 사람을 구분하기 위해 사용되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="c5035-2724">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="c5035-2725">검사 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2725">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2726">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2726">Checksum</span></span>

<span data-ttu-id="c5035-2727">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2727">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2728">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2728">Definition</span></span>

<span data-ttu-id="c5035-2729">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2729">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2730">Func_south_korea_resident_number 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2730">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2731">Keyword_south_korea_resident_number에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2731">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="c5035-2732">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2732">The checksum passes.</span></span>

<span data-ttu-id="c5035-2733">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2733">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2734">Func_south_korea_resident_number 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2734">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2735">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2735">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2736">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2736">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="c5035-2737">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="c5035-2737">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="c5035-2738">National ID card
</span><span class="sxs-lookup"><span data-stu-id="c5035-2738">National ID card</span></span> 
- <span data-ttu-id="c5035-2739">Citizen's Registration Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2739">Citizen's Registration Number</span></span> 
- <span data-ttu-id="c5035-2740">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="c5035-2740">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="c5035-2741">RRN
</span><span class="sxs-lookup"><span data-stu-id="c5035-2741">RRN</span></span> 
- <span data-ttu-id="c5035-2742">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2742">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="c5035-2743">스페인 SSN(사회 보장 번호)</span><span class="sxs-lookup"><span data-stu-id="c5035-2743">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2744">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2744">Format</span></span>

<span data-ttu-id="c5035-2745">11-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2745">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2746">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2746">Pattern</span></span>

<span data-ttu-id="c5035-2747">11 12 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2747">11-12 digits:</span></span>
- <span data-ttu-id="c5035-2748">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2748">Two digits</span></span> 
- <span data-ttu-id="c5035-2749">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="c5035-2749">A forward slash (optional)</span></span> 
- <span data-ttu-id="c5035-2750">7-8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2750">7-8 digits</span></span> 
- <span data-ttu-id="c5035-2751">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="c5035-2751">A forward slash (optional)</span></span> 
- <span data-ttu-id="c5035-2752">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2752">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2753">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2753">Checksum</span></span>

<span data-ttu-id="c5035-2754">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2754">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2755">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2755">Definition</span></span>

<span data-ttu-id="c5035-2756">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2757">Func_spanish_social_security_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2757">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2758">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2758">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2759">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2759">Keywords</span></span>

<span data-ttu-id="c5035-2760">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2760">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="c5035-2761">스웨덴 국가 ID</span><span class="sxs-lookup"><span data-stu-id="c5035-2761">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2762">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2762">Format</span></span>

<span data-ttu-id="c5035-2763">10 또는 12자리 숫자와 선택적 구분 기호</span><span class="sxs-lookup"><span data-stu-id="c5035-2763">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2764">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2764">Pattern</span></span>

<span data-ttu-id="c5035-2765">10 또는 12자리 숫자와 선택적 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="c5035-2765">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="c5035-2766">2-4자리 숫자(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="c5035-2766">2-4 digits (optional)</span></span> 
- <span data-ttu-id="c5035-2767">YYMMDD 날짜 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2767">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="c5035-2768">구분 기호 "-" 또는 "+"(선택 사항) 및</span><span class="sxs-lookup"><span data-stu-id="c5035-2768">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="c5035-2769">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2769">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2770">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2770">Checksum</span></span>

<span data-ttu-id="c5035-2771">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2771">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2772">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2772">Definition</span></span>

<span data-ttu-id="c5035-2773">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2773">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2774">Func_swedish_national_identifier 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2774">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2775">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2775">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2776">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2776">Keywords</span></span>

<span data-ttu-id="c5035-2777">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2777">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="c5035-2778">스웨덴 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2778">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2779">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2779">Format</span></span>

<span data-ttu-id="c5035-2780">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2780">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2781">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2781">Pattern</span></span>

<span data-ttu-id="c5035-2782">8자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2782">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2783">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2783">Checksum</span></span>

<span data-ttu-id="c5035-2784">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2784">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2785">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2785">Definition</span></span>

<span data-ttu-id="c5035-2786">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2786">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2787">Regex_sweden_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2787">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2788">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2788">One of the following is true:</span></span>
    - <span data-ttu-id="c5035-2789">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2789">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="c5035-2790">Keyword_sweden_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2790">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-2791">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2791">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="c5035-2792">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-2792">Keyword_sweden_passport</span></span>

- <span data-ttu-id="c5035-2793">visa requirements
</span><span class="sxs-lookup"><span data-stu-id="c5035-2793">visa requirements</span></span> 
- <span data-ttu-id="c5035-2794">Alien Registration Card
</span><span class="sxs-lookup"><span data-stu-id="c5035-2794">Alien Registration Card</span></span> 
- <span data-ttu-id="c5035-2795">Schengen visas
</span><span class="sxs-lookup"><span data-stu-id="c5035-2795">Schengen visas</span></span> 
- <span data-ttu-id="c5035-2796">Schengen visa
</span><span class="sxs-lookup"><span data-stu-id="c5035-2796">Schengen visa</span></span> 
- <span data-ttu-id="c5035-2797">Visa Processing
</span><span class="sxs-lookup"><span data-stu-id="c5035-2797">Visa Processing</span></span> 
- <span data-ttu-id="c5035-2798">Visa Type
</span><span class="sxs-lookup"><span data-stu-id="c5035-2798">Visa Type</span></span> 
- <span data-ttu-id="c5035-2799">Single Entry
</span><span class="sxs-lookup"><span data-stu-id="c5035-2799">Single Entry</span></span> 
- <span data-ttu-id="c5035-2800">Multiple Entry
</span><span class="sxs-lookup"><span data-stu-id="c5035-2800">Multiple Entry</span></span> 
- <span data-ttu-id="c5035-2801">G3 Processing Fees

</span><span class="sxs-lookup"><span data-stu-id="c5035-2801">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="c5035-2802">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-2802">Keyword_passport</span></span>

- <span data-ttu-id="c5035-2803">Passport Number</span><span class="sxs-lookup"><span data-stu-id="c5035-2803">Passport Number</span></span> 
- <span data-ttu-id="c5035-2804">
Passport No</span><span class="sxs-lookup"><span data-stu-id="c5035-2804">Passport No</span></span> 
- <span data-ttu-id="c5035-2805">Passport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2805">Passport #</span></span> 
- <span data-ttu-id="c5035-2806">Passport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-2806">Passport#</span></span> 
- <span data-ttu-id="c5035-2807">PassportID</span><span class="sxs-lookup"><span data-stu-id="c5035-2807">PassportID</span></span> 
- <span data-ttu-id="c5035-2808">Passportno
</span><span class="sxs-lookup"><span data-stu-id="c5035-2808">Passportno</span></span> 
- <span data-ttu-id="c5035-2809">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-2809">passportnumber</span></span> 
- <span data-ttu-id="c5035-2810">パスポート</span><span class="sxs-lookup"><span data-stu-id="c5035-2810">パスポート</span></span> 
- <span data-ttu-id="c5035-2811">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2811">パスポート番号</span></span> 
- <span data-ttu-id="c5035-2812">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="c5035-2812">パスポートのNum</span></span> 
- <span data-ttu-id="c5035-2813">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="c5035-2813">パスポート＃</span></span> 
- <span data-ttu-id="c5035-2814">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="c5035-2814">Numéro de passeport</span></span> 
- <span data-ttu-id="c5035-2815">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="c5035-2815">Passeport n °</span></span> 
- <span data-ttu-id="c5035-2816">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="c5035-2816">Passeport Non</span></span> 
- <span data-ttu-id="c5035-2817">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2817">Passeport #</span></span> 
- <span data-ttu-id="c5035-2818">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-2818">Passeport#</span></span> 
- <span data-ttu-id="c5035-2819">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="c5035-2819">PasseportNon</span></span> 
- <span data-ttu-id="c5035-2820">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="c5035-2820">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="c5035-2821">SWIFT 코드</span><span class="sxs-lookup"><span data-stu-id="c5035-2821">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2822">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2822">Format</span></span>

<span data-ttu-id="c5035-2823">4개의 문자, 5-31개 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2823">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2824">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2824">Pattern</span></span>

<span data-ttu-id="c5035-2825">4개의 문자, 5-31개 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2825">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="c5035-2826">4문자 은행 코드(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2826">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-2827">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-2827">An optional space</span></span> 
- <span data-ttu-id="c5035-2828">4-28개 문자 또는 숫자[BBAN(기본 은행 계좌 번호)]</span><span class="sxs-lookup"><span data-stu-id="c5035-2828">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="c5035-2829">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="c5035-2829">An optional space</span></span> 
- <span data-ttu-id="c5035-2830">1-3개 문자 또는 숫자(BBAN의 나머지)</span><span class="sxs-lookup"><span data-stu-id="c5035-2830">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2831">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2831">Checksum</span></span>

<span data-ttu-id="c5035-2832">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2832">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2833">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2833">Definition</span></span>

<span data-ttu-id="c5035-2834">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2834">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2835">Regex_swift 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2835">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2836">Keyword_swift의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2836">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2837">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2837">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="c5035-2838">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="c5035-2838">Keyword_swift</span></span>

- <span data-ttu-id="c5035-2839">international organization for standardization 9362
</span><span class="sxs-lookup"><span data-stu-id="c5035-2839">international organization for standardization 9362</span></span> 
- <span data-ttu-id="c5035-2840">iso 9362
</span><span class="sxs-lookup"><span data-stu-id="c5035-2840">iso 9362</span></span> 
- <span data-ttu-id="c5035-2841">iso9362</span><span class="sxs-lookup"><span data-stu-id="c5035-2841">iso9362</span></span> 
- <span data-ttu-id="c5035-2842">swift\#</span><span class="sxs-lookup"><span data-stu-id="c5035-2842">swift\#</span></span> 
- <span data-ttu-id="c5035-2843">swiftcode
</span><span class="sxs-lookup"><span data-stu-id="c5035-2843">swiftcode</span></span> 
- <span data-ttu-id="c5035-2844">swiftnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-2844">swiftnumber</span></span> 
- <span data-ttu-id="c5035-2845">swiftroutingnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-2845">swiftroutingnumber</span></span> 
- <span data-ttu-id="c5035-2846">swift code
</span><span class="sxs-lookup"><span data-stu-id="c5035-2846">swift code</span></span> 
- <span data-ttu-id="c5035-2847">swift number #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2847">swift number #</span></span> 
- <span data-ttu-id="c5035-2848">swift routing number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2848">swift routing number</span></span> 
- <span data-ttu-id="c5035-2849">bic number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2849">bic number</span></span> 
- <span data-ttu-id="c5035-2850">bic code
</span><span class="sxs-lookup"><span data-stu-id="c5035-2850">bic code</span></span> 
- <span data-ttu-id="c5035-2851">bic\#</span><span class="sxs-lookup"><span data-stu-id="c5035-2851">bic \#</span></span> 
- <span data-ttu-id="c5035-2852">bic\#</span><span class="sxs-lookup"><span data-stu-id="c5035-2852">bic\#</span></span> 
- <span data-ttu-id="c5035-2853">bank identifier code
</span><span class="sxs-lookup"><span data-stu-id="c5035-2853">bank identifier code</span></span> 
- <span data-ttu-id="c5035-2854">標準化9362</span><span class="sxs-lookup"><span data-stu-id="c5035-2854">標準化9362</span></span> 
- <span data-ttu-id="c5035-2855">迅速＃
</span><span class="sxs-lookup"><span data-stu-id="c5035-2855">迅速＃</span></span> 
- <span data-ttu-id="c5035-2856">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="c5035-2856">SWIFTコード</span></span> 
- <span data-ttu-id="c5035-2857">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2857">SWIFT番号</span></span> 
- <span data-ttu-id="c5035-2858">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2858">迅速なルーティング番号</span></span> 
- <span data-ttu-id="c5035-2859">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-2859">BIC番号</span></span> 
- <span data-ttu-id="c5035-2860">BICコード
</span><span class="sxs-lookup"><span data-stu-id="c5035-2860">BICコード</span></span> 
- <span data-ttu-id="c5035-2861">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="c5035-2861">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="c5035-2862">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="c5035-2862">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="c5035-2863">rapide\#</span><span class="sxs-lookup"><span data-stu-id="c5035-2863">rapide \#</span></span> 
- <span data-ttu-id="c5035-2864">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="c5035-2864">code SWIFT</span></span> 
- <span data-ttu-id="c5035-2865">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="c5035-2865">le numéro de swift</span></span> 
- <span data-ttu-id="c5035-2866">swift numéro d'acheminement
</span><span class="sxs-lookup"><span data-stu-id="c5035-2866">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="c5035-2867">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="c5035-2867">le numéro BIC</span></span> 
- <span data-ttu-id="c5035-2868">\#BIC</span><span class="sxs-lookup"><span data-stu-id="c5035-2868">\# BIC</span></span> 
- <span data-ttu-id="c5035-2869">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="c5035-2869">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="c5035-2870">대만 국가 ID</span><span class="sxs-lookup"><span data-stu-id="c5035-2870">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2871">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2871">Format</span></span>

<span data-ttu-id="c5035-2872">1개의 문자, 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2872">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2873">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2873">Pattern</span></span>

<span data-ttu-id="c5035-2874">1개의 문자, 9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2874">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="c5035-2875">1개 문자(영문, 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2875">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="c5035-2876">숫자 "1" 또는 "2"</span><span class="sxs-lookup"><span data-stu-id="c5035-2876">The digit "1" or "2"</span></span> 
- <span data-ttu-id="c5035-2877">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2877">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2878">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2878">Checksum</span></span>

<span data-ttu-id="c5035-2879">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2879">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2880">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2880">Definition</span></span>

<span data-ttu-id="c5035-2881">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2881">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2882">Func_taiwanese_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2882">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2883">Keyword_taiwanese_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2883">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="c5035-2884">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2884">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2885">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2885">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="c5035-2886">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="c5035-2886">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="c5035-2887">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="c5035-2887">身份證字號</span></span> 
- <span data-ttu-id="c5035-2888">身份證
</span><span class="sxs-lookup"><span data-stu-id="c5035-2888">身份證</span></span> 
- <span data-ttu-id="c5035-2889">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="c5035-2889">身份證號碼</span></span> 
- <span data-ttu-id="c5035-2890">身份證號
</span><span class="sxs-lookup"><span data-stu-id="c5035-2890">身份證號</span></span> 
- <span data-ttu-id="c5035-2891">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="c5035-2891">身分證字號</span></span> 
- <span data-ttu-id="c5035-2892">身分證 </span><span class="sxs-lookup"><span data-stu-id="c5035-2892">身分證</span></span> 
- <span data-ttu-id="c5035-2893">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="c5035-2893">身分證號碼</span></span> 
- <span data-ttu-id="c5035-2894">身份證號
</span><span class="sxs-lookup"><span data-stu-id="c5035-2894">身份證號</span></span> 
- <span data-ttu-id="c5035-2895">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="c5035-2895">身分證統一編號</span></span> 
- <span data-ttu-id="c5035-2896">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="c5035-2896">國民身分證統一編號</span></span> 
- <span data-ttu-id="c5035-2897">簽名
</span><span class="sxs-lookup"><span data-stu-id="c5035-2897">簽名</span></span> 
- <span data-ttu-id="c5035-2898">蓋章
</span><span class="sxs-lookup"><span data-stu-id="c5035-2898">蓋章</span></span> 
- <span data-ttu-id="c5035-2899">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="c5035-2899">簽名或蓋章</span></span> 
- <span data-ttu-id="c5035-2900">簽章</span><span class="sxs-lookup"><span data-stu-id="c5035-2900">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="c5035-2901">	대만 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2901">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2902">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2902">Format</span></span>

- <span data-ttu-id="c5035-2903">생체 인식 여권 번호: 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="c5035-2903">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="c5035-2904">비-생체 인식 여권 번호: 숫자 9 개</span><span class="sxs-lookup"><span data-stu-id="c5035-2904">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2905">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2905">Pattern</span></span>
<span data-ttu-id="c5035-2906">생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="c5035-2906">Biometric passport number:</span></span>
- <span data-ttu-id="c5035-2907">숫자 "3" </span><span class="sxs-lookup"><span data-stu-id="c5035-2907">The digit "3"</span></span> 
- <span data-ttu-id="c5035-2908">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2908">Eight digits</span></span>

<span data-ttu-id="c5035-2909">비-생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="c5035-2909">Non-biometric passport number:</span></span>
- <span data-ttu-id="c5035-2910">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2910">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2911">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2911">Checksum</span></span>

<span data-ttu-id="c5035-2912">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2912">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2913">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2913">Definition</span></span>

<span data-ttu-id="c5035-2914">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2914">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2915">Regex_taiwan_passport 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2915">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2916">Keyword_taiwan_passport에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2916">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2917">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2917">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="c5035-2918">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-2918">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="c5035-2919">ROC passport number
</span><span class="sxs-lookup"><span data-stu-id="c5035-2919">ROC passport number</span></span> 
- <span data-ttu-id="c5035-2920">여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2920">Passport number</span></span> 
- <span data-ttu-id="c5035-2921">Passport 없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2921">Passport no</span></span> 
- <span data-ttu-id="c5035-2922">Passport Num
</span><span class="sxs-lookup"><span data-stu-id="c5035-2922">Passport Num</span></span> 
- <span data-ttu-id="c5035-2923">Passport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-2923">Passport #</span></span> 
- <span data-ttu-id="c5035-2924">护照
</span><span class="sxs-lookup"><span data-stu-id="c5035-2924">护照</span></span> 
- <span data-ttu-id="c5035-2925">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="c5035-2925">中華民國護照</span></span> 
- <span data-ttu-id="c5035-2926">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="c5035-2926">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="c5035-2927">대만 거주 인증(ARC/TARC) 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-2927">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2928">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2928">Format</span></span>

<span data-ttu-id="c5035-2929">10개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2929">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2930">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2930">Pattern</span></span>

<span data-ttu-id="c5035-2931">10개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2931">10 letters and digits:</span></span>
- <span data-ttu-id="c5035-2932">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="c5035-2932">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="c5035-2933">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2933">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2934">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2934">Checksum</span></span>

<span data-ttu-id="c5035-2935">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2935">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2936">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2936">Definition</span></span>

<span data-ttu-id="c5035-2937">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2937">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2938">Regex_taiwan_resident_certificate 정규식 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2938">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2939">Keyword_taiwan_resident_certificate에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2939">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2940">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2940">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="c5035-2941">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="c5035-2941">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="c5035-2942">Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="c5035-2942">Resident Certificate</span></span> 
- <span data-ttu-id="c5035-2943">상주 Cert</span><span class="sxs-lookup"><span data-stu-id="c5035-2943">Resident Cert</span></span> 
- <span data-ttu-id="c5035-2944">Resident Cert.
</span><span class="sxs-lookup"><span data-stu-id="c5035-2944">Resident Cert.</span></span> 
- <span data-ttu-id="c5035-2945">Id 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-2945">Identification card</span></span> 
- <span data-ttu-id="c5035-2946">Alien Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="c5035-2946">Alien Resident Certificate</span></span> 
- <span data-ttu-id="c5035-2947">ARC
</span><span class="sxs-lookup"><span data-stu-id="c5035-2947">ARC</span></span> 
- <span data-ttu-id="c5035-2948">Taiwan Area Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="c5035-2948">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="c5035-2949">TARC
</span><span class="sxs-lookup"><span data-stu-id="c5035-2949">TARC</span></span> 
- <span data-ttu-id="c5035-2950">居留證
</span><span class="sxs-lookup"><span data-stu-id="c5035-2950">居留證</span></span> 
- <span data-ttu-id="c5035-2951">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="c5035-2951">外僑居留證</span></span> 
- <span data-ttu-id="c5035-2952">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="c5035-2952">台灣地區居留證</span></span> 
   
## <a name="uk-drivers-license-number"></a><span data-ttu-id="c5035-p141">영국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2955">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2955">Format</span></span>

<span data-ttu-id="c5035-2956">지정된 형식의 18개 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="c5035-2956">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2957">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2957">Pattern</span></span>

<span data-ttu-id="c5035-2958">18개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-2958">18 letters and digits:</span></span>
- <span data-ttu-id="c5035-2959">5개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="c5035-2959">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="c5035-2960">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2960">One digit</span></span> 
- <span data-ttu-id="c5035-2961">생년월일에 대한 DDMMY 날짜 형식의 5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2961">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="c5035-2962">2개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="c5035-2962">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="c5035-2963">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2963">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2964">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2964">Checksum</span></span>

<span data-ttu-id="c5035-2965">예</span><span class="sxs-lookup"><span data-stu-id="c5035-2965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2966">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2966">Definition</span></span>

<span data-ttu-id="c5035-2967">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2967">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2968">Func_uk_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2968">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2969">Keyword_uk_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2969">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="c5035-2970">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2970">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-2971">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-2971">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="c5035-2972">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="c5035-2972">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="c5035-2973">DVLA
</span><span class="sxs-lookup"><span data-stu-id="c5035-2973">DVLA</span></span> 
- <span data-ttu-id="c5035-2974">light vans
</span><span class="sxs-lookup"><span data-stu-id="c5035-2974">light vans</span></span> 
- <span data-ttu-id="c5035-2975">quadbikes
</span><span class="sxs-lookup"><span data-stu-id="c5035-2975">quadbikes</span></span> 
- <span data-ttu-id="c5035-2976">motor cars
</span><span class="sxs-lookup"><span data-stu-id="c5035-2976">motor cars</span></span> 
- <span data-ttu-id="c5035-2977">125cc</span><span class="sxs-lookup"><span data-stu-id="c5035-2977">125cc</span></span> 
- <span data-ttu-id="c5035-2978">sidecar
</span><span class="sxs-lookup"><span data-stu-id="c5035-2978">sidecar</span></span> 
- <span data-ttu-id="c5035-2979">tricycles
</span><span class="sxs-lookup"><span data-stu-id="c5035-2979">tricycles</span></span> 
- <span data-ttu-id="c5035-2980">motorcycles
</span><span class="sxs-lookup"><span data-stu-id="c5035-2980">motorcycles</span></span> 
- <span data-ttu-id="c5035-2981">photocard licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-2981">photocard licence</span></span> 
- <span data-ttu-id="c5035-2982">learner drivers
</span><span class="sxs-lookup"><span data-stu-id="c5035-2982">learner drivers</span></span> 
- <span data-ttu-id="c5035-2983">licence holder
</span><span class="sxs-lookup"><span data-stu-id="c5035-2983">licence holder</span></span> 
- <span data-ttu-id="c5035-2984">licence holders
</span><span class="sxs-lookup"><span data-stu-id="c5035-2984">licence holders</span></span> 
- <span data-ttu-id="c5035-2985">driving licences
</span><span class="sxs-lookup"><span data-stu-id="c5035-2985">driving licences</span></span> 
- <span data-ttu-id="c5035-2986">driving licence
</span><span class="sxs-lookup"><span data-stu-id="c5035-2986">driving licence</span></span> 
- <span data-ttu-id="c5035-2987">dual control car
</span><span class="sxs-lookup"><span data-stu-id="c5035-2987">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="c5035-p142">영국 선거 롤 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-2990">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-2990">Format</span></span>

<span data-ttu-id="c5035-2991">2개의 문자, 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2991">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-2992">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-2992">Pattern</span></span>

<span data-ttu-id="c5035-2993">2개의 문자(대/소문자 구분 안 함)와 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-2993">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-2994">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-2994">Checksum</span></span>

<span data-ttu-id="c5035-2995">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-2995">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-2996">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-2996">Definition</span></span>

<span data-ttu-id="c5035-2997">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2997">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-2998">Regex_uk_electoral 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2998">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-2999">Keyword_uk_electoral의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-2999">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-3000">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-3000">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="c5035-3001">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="c5035-3001">Keyword_uk_electoral</span></span>

- <span data-ttu-id="c5035-3002">council nomination
</span><span class="sxs-lookup"><span data-stu-id="c5035-3002">council nomination</span></span> 
- <span data-ttu-id="c5035-3003">nomination form
</span><span class="sxs-lookup"><span data-stu-id="c5035-3003">nomination form</span></span> 
- <span data-ttu-id="c5035-3004">electoral register

</span><span class="sxs-lookup"><span data-stu-id="c5035-3004">electoral register</span></span> 
- <span data-ttu-id="c5035-3005">electoral roll</span><span class="sxs-lookup"><span data-stu-id="c5035-3005">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="c5035-p143">영국 국립 보건 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-3008">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-3008">Format</span></span>

<span data-ttu-id="c5035-3009">공백으로 구분된 10-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3009">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-3010">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-3010">Pattern</span></span>

<span data-ttu-id="c5035-3011">10-17자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="c5035-3011">10-17 digits:</span></span>
- <span data-ttu-id="c5035-3012">3 또는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3012">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="c5035-3013">공백</span><span class="sxs-lookup"><span data-stu-id="c5035-3013">A space</span></span> 
- <span data-ttu-id="c5035-3014">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3014">Three digits</span></span> 
- <span data-ttu-id="c5035-3015">공백</span><span class="sxs-lookup"><span data-stu-id="c5035-3015">A space</span></span> 
- <span data-ttu-id="c5035-3016">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3016">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-3017">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-3017">Checksum</span></span>

<span data-ttu-id="c5035-3018">예</span><span class="sxs-lookup"><span data-stu-id="c5035-3018">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-3019">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-3019">Definition</span></span>

<span data-ttu-id="c5035-3020">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3020">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3021">Func_uk_nhs_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3021">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3022">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3022">One of the following is true:</span></span>
    - <span data-ttu-id="c5035-3023">Keyword_uk_nhs_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3023">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="c5035-3024">Keyword_uk_nhs_number1의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3024">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="c5035-3025">Keyword_uk_nhs_number_dob의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3025">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="c5035-3026">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3026">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-3027">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-3027">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="c5035-3028">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="c5035-3028">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="c5035-3029">국립 보건 서비스
</span><span class="sxs-lookup"><span data-stu-id="c5035-3029">national health service</span></span> 
- <span data-ttu-id="c5035-3030">nhs
</span><span class="sxs-lookup"><span data-stu-id="c5035-3030">nhs</span></span> 
- <span data-ttu-id="c5035-3031">health services authority

</span><span class="sxs-lookup"><span data-stu-id="c5035-3031">health services authority</span></span> 
- <span data-ttu-id="c5035-3032">health authority</span><span class="sxs-lookup"><span data-stu-id="c5035-3032">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="c5035-3033">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="c5035-3033">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="c5035-3034">patient id
</span><span class="sxs-lookup"><span data-stu-id="c5035-3034">patient id</span></span> 
- <span data-ttu-id="c5035-3035">patient identification
</span><span class="sxs-lookup"><span data-stu-id="c5035-3035">patient identification</span></span> 
- <span data-ttu-id="c5035-3036">patient no

</span><span class="sxs-lookup"><span data-stu-id="c5035-3036">patient no</span></span> 
- <span data-ttu-id="c5035-3037">patient number</span><span class="sxs-lookup"><span data-stu-id="c5035-3037">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="c5035-3038">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="c5035-3038">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="c5035-3039">GP</span><span class="sxs-lookup"><span data-stu-id="c5035-3039">GP</span></span> 
- <span data-ttu-id="c5035-3040">DOB
</span><span class="sxs-lookup"><span data-stu-id="c5035-3040">DOB</span></span> 
- <span data-ttu-id="c5035-3041">D.O.B</span><span class="sxs-lookup"><span data-stu-id="c5035-3041">D.O.B</span></span> 
- <span data-ttu-id="c5035-3042">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="c5035-3042">Date of Birth</span></span> 
- <span data-ttu-id="c5035-3043">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="c5035-3043">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="c5035-p144">영국 NINO(국민 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="c5035-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-3046">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-3046">Format</span></span>

<span data-ttu-id="c5035-3047">7 문자나 공백이 나 파선으로 구분 하 여 9 문자</span><span class="sxs-lookup"><span data-stu-id="c5035-3047">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-3048">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-3048">Pattern</span></span>

<span data-ttu-id="c5035-3049">두 가능한 패턴:</span><span class="sxs-lookup"><span data-stu-id="c5035-3049">Two possible patterns:</span></span>

- <span data-ttu-id="c5035-3050">처음 두 (유효한 NINOs이이 패턴의 유효성을 검사;는이 접두사에 특정 문자만 사용 하지 대/소문자 구분)</span><span class="sxs-lookup"><span data-stu-id="c5035-3050">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="c5035-3051">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3051">Six digits</span></span>
- <span data-ttu-id="c5035-3052">'A', 'B', 'C' 또는 명의 ' (예: 접두사를 특정 문자에에서는 사용할 수는 접미사; 하지 대/소문자 구분만)</span><span class="sxs-lookup"><span data-stu-id="c5035-3052">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="c5035-3053">또는</span><span class="sxs-lookup"><span data-stu-id="c5035-3053">OR</span></span>

- <span data-ttu-id="c5035-3054">처음 두</span><span class="sxs-lookup"><span data-stu-id="c5035-3054">Two letters</span></span>
- <span data-ttu-id="c5035-3055">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="c5035-3055">A space or dash</span></span>
- <span data-ttu-id="c5035-3056">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3056">Two digits</span></span>
- <span data-ttu-id="c5035-3057">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="c5035-3057">A space or dash</span></span>
- <span data-ttu-id="c5035-3058">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3058">Two digits</span></span>
- <span data-ttu-id="c5035-3059">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="c5035-3059">A space or dash</span></span>
- <span data-ttu-id="c5035-3060">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3060">Two digits</span></span>
- <span data-ttu-id="c5035-3061">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="c5035-3061">A space or dash</span></span>
- <span data-ttu-id="c5035-3062">두 'A', 'B', 'C' 또는 명의 '</span><span class="sxs-lookup"><span data-stu-id="c5035-3062">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-3063">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-3063">Checksum</span></span>

<span data-ttu-id="c5035-3064">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-3064">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-3065">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-3065">Definition</span></span>

<span data-ttu-id="c5035-3066">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3066">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3067">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3067">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3068">Keyword_uk_nino의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3068">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="c5035-3069">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3069">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3070">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3070">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3071">Keyword_uk_nino의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3071">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-3072">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-3072">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="c5035-3073">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="c5035-3073">Keyword_uk_nino</span></span>

- <span data-ttu-id="c5035-3074">national insurance number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3074">national insurance number</span></span> 
- <span data-ttu-id="c5035-3075">national insurance contributions
</span><span class="sxs-lookup"><span data-stu-id="c5035-3075">national insurance contributions</span></span> 
- <span data-ttu-id="c5035-3076">protection act
</span><span class="sxs-lookup"><span data-stu-id="c5035-3076">protection act</span></span> 
- <span data-ttu-id="c5035-3077">insurance
</span><span class="sxs-lookup"><span data-stu-id="c5035-3077">insurance</span></span> 
- <span data-ttu-id="c5035-3078">social security number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3078">social security number</span></span> 
- <span data-ttu-id="c5035-3079">insurance application
</span><span class="sxs-lookup"><span data-stu-id="c5035-3079">insurance application</span></span> 
- <span data-ttu-id="c5035-3080">medical application
</span><span class="sxs-lookup"><span data-stu-id="c5035-3080">medical application</span></span> 
- <span data-ttu-id="c5035-3081">social insurance
</span><span class="sxs-lookup"><span data-stu-id="c5035-3081">social insurance</span></span> 
- <span data-ttu-id="c5035-3082">medical attention
</span><span class="sxs-lookup"><span data-stu-id="c5035-3082">medical attention</span></span> 
- <span data-ttu-id="c5035-3083">공유 보안</span><span class="sxs-lookup"><span data-stu-id="c5035-3083">social security</span></span> 
- <span data-ttu-id="c5035-3084">great britain
</span><span class="sxs-lookup"><span data-stu-id="c5035-3084">great britain</span></span> 
- <span data-ttu-id="c5035-3085">insurance
</span><span class="sxs-lookup"><span data-stu-id="c5035-3085">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="c5035-p145">미국/영국 여권 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-3088">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-3088">Format</span></span>

<span data-ttu-id="c5035-3089">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3089">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-3090">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-3090">Pattern</span></span>

<span data-ttu-id="c5035-3091">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3091">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-3092">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-3092">Checksum</span></span>

<span data-ttu-id="c5035-3093">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-3093">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-3094">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-3094">Definition</span></span>

<span data-ttu-id="c5035-3095">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3095">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3096">Func_usa_uk_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3096">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3097">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3097">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-3098">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-3098">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="c5035-3099">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="c5035-3099">Keyword_passport</span></span>

- <span data-ttu-id="c5035-3100">Passport Number</span><span class="sxs-lookup"><span data-stu-id="c5035-3100">Passport Number</span></span> 
- <span data-ttu-id="c5035-3101">
Passport No</span><span class="sxs-lookup"><span data-stu-id="c5035-3101">Passport No</span></span> 
- <span data-ttu-id="c5035-3102">Passport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3102">Passport #</span></span> 
- <span data-ttu-id="c5035-3103">Passport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3103">Passport#</span></span> 
- <span data-ttu-id="c5035-3104">PassportID</span><span class="sxs-lookup"><span data-stu-id="c5035-3104">PassportID</span></span> 
- <span data-ttu-id="c5035-3105">Passportno
</span><span class="sxs-lookup"><span data-stu-id="c5035-3105">Passportno</span></span> 
- <span data-ttu-id="c5035-3106">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="c5035-3106">passportnumber</span></span> 
- <span data-ttu-id="c5035-3107">パスポート</span><span class="sxs-lookup"><span data-stu-id="c5035-3107">パスポート</span></span> 
- <span data-ttu-id="c5035-3108">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="c5035-3108">パスポート番号</span></span> 
- <span data-ttu-id="c5035-3109">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="c5035-3109">パスポートのNum</span></span> 
- <span data-ttu-id="c5035-3110">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="c5035-3110">パスポート＃</span></span> 
- <span data-ttu-id="c5035-3111">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="c5035-3111">Numéro de passeport</span></span> 
- <span data-ttu-id="c5035-3112">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="c5035-3112">Passeport n °</span></span> 
- <span data-ttu-id="c5035-3113">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="c5035-3113">Passeport Non</span></span> 
- <span data-ttu-id="c5035-3114">Passeport #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3114">Passeport #</span></span> 
- <span data-ttu-id="c5035-3115">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3115">Passeport#</span></span> 
- <span data-ttu-id="c5035-3116">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="c5035-3116">PasseportNon</span></span> 
- <span data-ttu-id="c5035-3117">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="c5035-3117">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="c5035-3118">미국 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-3118">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-3119">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-3119">Format</span></span>

<span data-ttu-id="c5035-3120">8-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3120">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-3121">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-3121">Pattern</span></span>

<span data-ttu-id="c5035-3122">8-17자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3122">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-3123">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-3123">Checksum</span></span>

<span data-ttu-id="c5035-3124">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-3124">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-3125">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-3125">Definition</span></span>

<span data-ttu-id="c5035-3126">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3126">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3127">Regex_usa_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3127">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3128">Keyword_usa_Bank_Account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3128">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c5035-3129">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-3129">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="c5035-3130">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="c5035-3130">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="c5035-3131">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3131">Checking Account Number</span></span> 
- <span data-ttu-id="c5035-3132">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="c5035-3132">Checking Account</span></span> 
- <span data-ttu-id="c5035-3133">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3133">Checking Account #</span></span> 
- <span data-ttu-id="c5035-3134">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3134">Checking Acct Number</span></span> 
- <span data-ttu-id="c5035-3135">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3135">Checking Acct #</span></span> 
- <span data-ttu-id="c5035-3136">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3136">Checking Acct No.</span></span> 
- <span data-ttu-id="c5035-3137">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3137">Checking Account No.</span></span> 
- <span data-ttu-id="c5035-3138">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3138">Bank Account Number</span></span> 
- <span data-ttu-id="c5035-3139">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3139">Bank Account #</span></span> 
- <span data-ttu-id="c5035-3140">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3140">Bank Acct Number</span></span> 
- <span data-ttu-id="c5035-3141">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3141">Bank Acct #</span></span> 
- <span data-ttu-id="c5035-3142">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3142">Bank Acct No.</span></span> 
- <span data-ttu-id="c5035-3143">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3143">Bank Account No.</span></span> 
- <span data-ttu-id="c5035-3144">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3144">Savings Account Number</span></span> 
- <span data-ttu-id="c5035-3145">Savings Account.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3145">Savings Account.</span></span> 
- <span data-ttu-id="c5035-3146">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3146">Savings Account #</span></span> 
- <span data-ttu-id="c5035-3147">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3147">Savings Acct Number</span></span> 
- <span data-ttu-id="c5035-3148">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3148">Savings Acct #</span></span> 
- <span data-ttu-id="c5035-3149">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3149">Savings Acct No.</span></span> 
- <span data-ttu-id="c5035-3150">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3150">Savings Account No.</span></span> 
- <span data-ttu-id="c5035-3151">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3151">Debit Account Number</span></span> 
- <span data-ttu-id="c5035-3152">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="c5035-3152">Debit Account</span></span> 
- <span data-ttu-id="c5035-3153">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3153">Debit Account #</span></span> 
- <span data-ttu-id="c5035-3154">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3154">Debit Acct Number</span></span> 
- <span data-ttu-id="c5035-3155">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3155">Debit Acct #</span></span> 
- <span data-ttu-id="c5035-3156">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3156">Debit Acct No.</span></span> 
- <span data-ttu-id="c5035-3157">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="c5035-3157">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="c5035-3158">미국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-3158">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="c5035-3159">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-3159">Format</span></span>

<span data-ttu-id="c5035-3160">주마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3160">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-3161">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-3161">Pattern</span></span>

<span data-ttu-id="c5035-3162">주마다 다릅니다(예: 뉴욕).</span><span class="sxs-lookup"><span data-stu-id="c5035-3162">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="c5035-3163">숫자 9 개 ddd ddd ddd 일치와 동일 하 게 서식이 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3163">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="c5035-3164">Ddddddddd 같은 숫자 9 개 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3164">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-3165">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-3165">Checksum</span></span>

<span data-ttu-id="c5035-3166">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-3166">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-3167">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-3167">Definition</span></span>

<span data-ttu-id="c5035-3168">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3168">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3169">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3169">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3170">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3170">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="c5035-3171">Keyword_us_drivers_license에서 키워드를 발견 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3171">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="c5035-3172">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3172">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3173">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3173">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3174">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3174">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="c5035-3175">Keyword_us_drivers_license_abbreviations의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3175">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="c5035-3176">Keyword_us_drivers_license의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3176">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-3177">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-3177">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="c5035-3178">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="c5035-3178">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="c5035-3179">DL</span><span class="sxs-lookup"><span data-stu-id="c5035-3179">DL</span></span> 
- <span data-ttu-id="c5035-3180">DLS</span><span class="sxs-lookup"><span data-stu-id="c5035-3180">DLS</span></span> 
- <span data-ttu-id="c5035-3181">CDL</span><span class="sxs-lookup"><span data-stu-id="c5035-3181">CDL</span></span> 
- <span data-ttu-id="c5035-3182">CDLS</span><span class="sxs-lookup"><span data-stu-id="c5035-3182">CDLS</span></span> 
- <span data-ttu-id="c5035-3183">ID</span><span class="sxs-lookup"><span data-stu-id="c5035-3183">ID</span></span> 
- <span data-ttu-id="c5035-3184">Id</span><span class="sxs-lookup"><span data-stu-id="c5035-3184">IDs</span></span> 
- <span data-ttu-id="c5035-3185">DL#</span><span class="sxs-lookup"><span data-stu-id="c5035-3185">DL#</span></span> 
- <span data-ttu-id="c5035-3186">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3186">DLS#</span></span> 
- <span data-ttu-id="c5035-3187">CDL#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3187">CDL#</span></span> 
- <span data-ttu-id="c5035-3188">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3188">CDLS#</span></span> 
- <span data-ttu-id="c5035-3189">ID#</span><span class="sxs-lookup"><span data-stu-id="c5035-3189">ID#</span></span>
- <span data-ttu-id="c5035-3190">
IDs#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3190">IDs#</span></span> 
- <span data-ttu-id="c5035-3191">ID 번호</span><span class="sxs-lookup"><span data-stu-id="c5035-3191">ID number</span></span> 
- <span data-ttu-id="c5035-3192">ID numbers
</span><span class="sxs-lookup"><span data-stu-id="c5035-3192">ID numbers</span></span> 
- <span data-ttu-id="c5035-3193">LIC</span><span class="sxs-lookup"><span data-stu-id="c5035-3193">LIC</span></span> 
- <span data-ttu-id="c5035-3194">LIC#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3194">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="c5035-3195">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="c5035-3195">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="c5035-3196">DriverLic</span><span class="sxs-lookup"><span data-stu-id="c5035-3196">DriverLic</span></span> 
- <span data-ttu-id="c5035-3197">DriverLics</span><span class="sxs-lookup"><span data-stu-id="c5035-3197">DriverLics</span></span> 
- <span data-ttu-id="c5035-3198">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-3198">DriverLicense</span></span> 
- <span data-ttu-id="c5035-3199">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-3199">DriverLicenses</span></span> 
- <span data-ttu-id="c5035-3200">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-3200">Driver Lic</span></span> 
- <span data-ttu-id="c5035-3201">드라이버 Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-3201">Driver Lics</span></span> 
- <span data-ttu-id="c5035-3202">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-3202">Driver License</span></span> 
- <span data-ttu-id="c5035-3203">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-3203">Driver Licenses</span></span> 
- <span data-ttu-id="c5035-3204">DriversLic</span><span class="sxs-lookup"><span data-stu-id="c5035-3204">DriversLic</span></span> 
- <span data-ttu-id="c5035-3205">DriversLics</span><span class="sxs-lookup"><span data-stu-id="c5035-3205">DriversLics</span></span> 
- <span data-ttu-id="c5035-3206">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-3206">DriversLicense</span></span> 
- <span data-ttu-id="c5035-3207">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-3207">DriversLicenses</span></span> 
- <span data-ttu-id="c5035-3208">드라이버 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-3208">Drivers Lic</span></span> 
- <span data-ttu-id="c5035-3209">드라이버 Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-3209">Drivers Lics</span></span> 
- <span data-ttu-id="c5035-3210">운전 면허</span><span class="sxs-lookup"><span data-stu-id="c5035-3210">Drivers License</span></span> 
- <span data-ttu-id="c5035-3211">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-3211">Drivers Licenses</span></span> 
- <span data-ttu-id="c5035-3212">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-3212">Driver'Lic</span></span> 
- <span data-ttu-id="c5035-3213">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-3213">Driver'Lics</span></span> 
- <span data-ttu-id="c5035-3214">Driver'License</span><span class="sxs-lookup"><span data-stu-id="c5035-3214">Driver'License</span></span> 
- <span data-ttu-id="c5035-3215">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="c5035-3215">Driver'Licenses</span></span> 
- <span data-ttu-id="c5035-3216">드라이버 ' Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-3216">Driver' Lic</span></span> 
- <span data-ttu-id="c5035-3217">드라이버 ' Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-3217">Driver' Lics</span></span> 
- <span data-ttu-id="c5035-3218">드라이버 ' 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-3218">Driver' License</span></span> 
- <span data-ttu-id="c5035-3219">드라이버 ' 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-3219">Driver' Licenses</span></span>
- <span data-ttu-id="c5035-3220">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="c5035-3220">Driver'sLic</span></span> 
- <span data-ttu-id="c5035-3221">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="c5035-3221">Driver'sLics</span></span> 
- <span data-ttu-id="c5035-3222">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="c5035-3222">Driver'sLicense</span></span> 
- <span data-ttu-id="c5035-3223">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="c5035-3223">Driver'sLicenses</span></span> 
- <span data-ttu-id="c5035-3224">드라이버의 Lic</span><span class="sxs-lookup"><span data-stu-id="c5035-3224">Driver's Lic</span></span> 
- <span data-ttu-id="c5035-3225">드라이버의 Lics</span><span class="sxs-lookup"><span data-stu-id="c5035-3225">Driver's Lics</span></span> 
- <span data-ttu-id="c5035-3226">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-3226">Driver's License</span></span> 
- <span data-ttu-id="c5035-3227">드라이버의 라이선스</span><span class="sxs-lookup"><span data-stu-id="c5035-3227">Driver's Licenses</span></span> 
- <span data-ttu-id="c5035-3228">identification number
</span><span class="sxs-lookup"><span data-stu-id="c5035-3228">identification number</span></span> 
- <span data-ttu-id="c5035-3229">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="c5035-3229">identification numbers</span></span> 
- <span data-ttu-id="c5035-3230">identification #
</span><span class="sxs-lookup"><span data-stu-id="c5035-3230">identification #</span></span> 
- <span data-ttu-id="c5035-3231">id 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-3231">id card</span></span> 
- <span data-ttu-id="c5035-3232">id 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-3232">id cards</span></span> 
- <span data-ttu-id="c5035-3233">id 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-3233">identification card</span></span> 
- <span data-ttu-id="c5035-3234">식별 카드</span><span class="sxs-lookup"><span data-stu-id="c5035-3234">identification cards</span></span> 
- <span data-ttu-id="c5035-3235">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-3235">DriverLic#</span></span> 
- <span data-ttu-id="c5035-3236">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-3236">DriverLics#</span></span> 
- <span data-ttu-id="c5035-3237">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-3237">DriverLicense#</span></span> 
- <span data-ttu-id="c5035-3238">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-3238">DriverLicenses#</span></span> 
- <span data-ttu-id="c5035-3239">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="c5035-3239">Driver Lic#</span></span> 
- <span data-ttu-id="c5035-3240">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3240">Driver Lics#</span></span> 
- <span data-ttu-id="c5035-3241">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-3241">Driver License#</span></span> 
- <span data-ttu-id="c5035-3242">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-3242">Driver Licenses#</span></span> 
- <span data-ttu-id="c5035-3243">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-3243">DriversLic#</span></span> 
- <span data-ttu-id="c5035-3244">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-3244">DriversLics#</span></span> 
- <span data-ttu-id="c5035-3245">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-3245">DriversLicense#</span></span> 
- <span data-ttu-id="c5035-3246">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-3246">DriversLicenses#</span></span> 
- <span data-ttu-id="c5035-3247">드라이버 Lic #</span><span class="sxs-lookup"><span data-stu-id="c5035-3247">Drivers Lic#</span></span> 
- <span data-ttu-id="c5035-3248">드라이버 Lics #</span><span class="sxs-lookup"><span data-stu-id="c5035-3248">Drivers Lics#</span></span> 
- <span data-ttu-id="c5035-3249">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-3249">Drivers License#</span></span> 
- <span data-ttu-id="c5035-3250">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="c5035-3250">Drivers Licenses#</span></span> 
- <span data-ttu-id="c5035-3251">Driver'Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3251">Driver'Lic#</span></span> 
- <span data-ttu-id="c5035-3252">Driver'Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3252">Driver'Lics#</span></span> 
- <span data-ttu-id="c5035-3253">Driver'License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3253">Driver'License#</span></span> 
- <span data-ttu-id="c5035-3254">Driver'Licenses#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3254">Driver'Licenses#</span></span> 
- <span data-ttu-id="c5035-3255">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3255">Driver' Lic#</span></span> 
- <span data-ttu-id="c5035-3256">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3256">Driver' Lics#</span></span> 
- <span data-ttu-id="c5035-3257">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3257">Driver' License#</span></span> 
- <span data-ttu-id="c5035-3258">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3258">Driver' Licenses#</span></span> 
- <span data-ttu-id="c5035-3259">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="c5035-3259">Driver'sLic#</span></span> 
- <span data-ttu-id="c5035-3260">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="c5035-3260">Driver'sLics#</span></span> 
- <span data-ttu-id="c5035-3261">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="c5035-3261">Driver'sLicense#</span></span> 
- <span data-ttu-id="c5035-3262">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="c5035-3262">Driver'sLicenses#</span></span> 
- <span data-ttu-id="c5035-3263">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3263">Driver's Lic#</span></span> 
- <span data-ttu-id="c5035-3264">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3264">Driver's Lics#</span></span> 
- <span data-ttu-id="c5035-3265">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3265">Driver's License#</span></span> 
- <span data-ttu-id="c5035-3266">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3266">Driver's Licenses#</span></span> 
- <span data-ttu-id="c5035-3267">id 카드 #</span><span class="sxs-lookup"><span data-stu-id="c5035-3267">id card#</span></span> 
- <span data-ttu-id="c5035-3268">id cards#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3268">id cards#</span></span> 
- <span data-ttu-id="c5035-3269">identification card#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3269">identification card#</span></span> 
- <span data-ttu-id="c5035-3270">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3270">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="c5035-3271">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="c5035-3271">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="c5035-3272">주 약어(예: "NY")
</span><span class="sxs-lookup"><span data-stu-id="c5035-3272">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="c5035-3273">주 이름(예: "New York")
</span><span class="sxs-lookup"><span data-stu-id="c5035-3273">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="c5035-3274">미국 ITIN(개인 납세자 번호)</span><span class="sxs-lookup"><span data-stu-id="c5035-3274">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-3275">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-3275">Format</span></span>

<span data-ttu-id="c5035-3276">"9"로 시작되고, "7" 또는 "8"을 4번째 숫자로 포함하고, 경우에 따라 공백이나 대시로 서식이 지정된 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3276">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-3277">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-3277">Pattern</span></span>

<span data-ttu-id="c5035-3278">서식 있음:</span><span class="sxs-lookup"><span data-stu-id="c5035-3278">Formatted:</span></span>
- <span data-ttu-id="c5035-3279">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3279">The digit "9"</span></span> 
- <span data-ttu-id="c5035-3280">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3280">Two digits</span></span> 
- <span data-ttu-id="c5035-3281">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="c5035-3281">A space or dash</span></span> 
- <span data-ttu-id="c5035-3282">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="c5035-3282">A "7" or "8"</span></span> 
- <span data-ttu-id="c5035-3283">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3283">A digit</span></span> 
- <span data-ttu-id="c5035-3284">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="c5035-3284">A space, or dash</span></span> 
- <span data-ttu-id="c5035-3285">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3285">Four digits</span></span>

<span data-ttu-id="c5035-3286">서식 없음:</span><span class="sxs-lookup"><span data-stu-id="c5035-3286">Unformatted:</span></span>
- <span data-ttu-id="c5035-3287">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3287">The digit "9"</span></span> 
- <span data-ttu-id="c5035-3288">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3288">Two digits</span></span> 
- <span data-ttu-id="c5035-3289">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="c5035-3289">A "7" or "8"</span></span> 
- <span data-ttu-id="c5035-3290">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3290">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-3291">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-3291">Checksum</span></span>

<span data-ttu-id="c5035-3292">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-3292">No</span></span>

### <a name="definition"></a><span data-ttu-id="c5035-3293">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-3293">Definition</span></span>

<span data-ttu-id="c5035-3294">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3294">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3295">Func_formatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3295">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3296">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3296">At least one of the following is true:</span></span>
    - <span data-ttu-id="c5035-3297">Keyword_itin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3297">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="c5035-3298">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3298">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="c5035-3299">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3299">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="c5035-3300">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3300">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="c5035-3301">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3302">Func_unformatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3302">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3303">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3303">At least one of the following is true:</span></span>
    - <span data-ttu-id="c5035-3304">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3304">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="c5035-3305">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3305">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="c5035-3306">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3306">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-3307">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-3307">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="c5035-3308">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="c5035-3308">Keyword_itin</span></span>

- <span data-ttu-id="c5035-3309">taxpayer
</span><span class="sxs-lookup"><span data-stu-id="c5035-3309">taxpayer</span></span> 
- <span data-ttu-id="c5035-3310">tax id
</span><span class="sxs-lookup"><span data-stu-id="c5035-3310">tax id</span></span> 
- <span data-ttu-id="c5035-3311">tax identification
</span><span class="sxs-lookup"><span data-stu-id="c5035-3311">tax identification</span></span> 
- <span data-ttu-id="c5035-3312">itin
</span><span class="sxs-lookup"><span data-stu-id="c5035-3312">itin</span></span> 
- <span data-ttu-id="c5035-3313">ssn</span><span class="sxs-lookup"><span data-stu-id="c5035-3313">ssn</span></span> 
- <span data-ttu-id="c5035-3314">tin
</span><span class="sxs-lookup"><span data-stu-id="c5035-3314">tin</span></span> 
- <span data-ttu-id="c5035-3315">공유 보안</span><span class="sxs-lookup"><span data-stu-id="c5035-3315">social security</span></span> 
- <span data-ttu-id="c5035-3316">tax payer
</span><span class="sxs-lookup"><span data-stu-id="c5035-3316">tax payer</span></span> 
- <span data-ttu-id="c5035-3317">itins
</span><span class="sxs-lookup"><span data-stu-id="c5035-3317">itins</span></span> 
- <span data-ttu-id="c5035-3318">taxid

</span><span class="sxs-lookup"><span data-stu-id="c5035-3318">taxid</span></span> 
- <span data-ttu-id="c5035-3319">individual taxpayer
</span><span class="sxs-lookup"><span data-stu-id="c5035-3319">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="c5035-3320">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="c5035-3320">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="c5035-3321">License</span><span class="sxs-lookup"><span data-stu-id="c5035-3321">License</span></span> 
- <span data-ttu-id="c5035-3322">DL</span><span class="sxs-lookup"><span data-stu-id="c5035-3322">DL</span></span> 
- <span data-ttu-id="c5035-3323">DOB
</span><span class="sxs-lookup"><span data-stu-id="c5035-3323">DOB</span></span> 
- <span data-ttu-id="c5035-3324">생년월일</span><span class="sxs-lookup"><span data-stu-id="c5035-3324">Birthdate</span></span> 
- <span data-ttu-id="c5035-3325">생일 </span><span class="sxs-lookup"><span data-stu-id="c5035-3325">Birthday</span></span> 
- <span data-ttu-id="c5035-3326">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="c5035-3326">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="c5035-3327">미국 SSN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="c5035-3327">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="c5035-3328">형식</span><span class="sxs-lookup"><span data-stu-id="c5035-3328">Format</span></span>

<span data-ttu-id="c5035-3329">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="c5035-3329">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="c5035-3330">2011 mid 하기 전에 발급 하는 경우는 SSN 강력한 위치 번호의 특정 부분 범위 내에 있어야 유효한 것으로 특정 범위 서식 지정 (다르지만 체크섬이 없는).</span><span class="sxs-lookup"><span data-stu-id="c5035-3330">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="c5035-3331">패턴</span><span class="sxs-lookup"><span data-stu-id="c5035-3331">Pattern</span></span>

<span data-ttu-id="c5035-3332">4 개의 함수 SSNs 4 개의 서로 다른 패턴에 나타나는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3332">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="c5035-3333">Func_ssn p r e 2011 강력한 서식이 적용 된 대시 또는 공백 (ddd-dd-dddd OR ddd dd dddd)으로 포맷 된 SSNs 발견</span><span class="sxs-lookup"><span data-stu-id="c5035-3333">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="c5035-3334">Func_unformatted_ssn p r e 2011 강력한 서식이 지정 된 연속 되는 숫자 9 개 (ddddddddd)로 서식이 지정 된 되지 않은 SSNs 발견</span><span class="sxs-lookup"><span data-stu-id="c5035-3334">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="c5035-3335">Func_randomized_formatted_ssn 대시 또는 공백 (ddd-dd-dddd OR ddd dd dddd)로 서식이 지정 된 게시물 2011 SSNs 발견</span><span class="sxs-lookup"><span data-stu-id="c5035-3335">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="c5035-3336">Func_randomized_unformatted_ssn 연속 되는 숫자 9 개 (ddddddddd)로 서식이 지정 된 되지 않은 게시물 2011 SSNs 발견</span><span class="sxs-lookup"><span data-stu-id="c5035-3336">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="c5035-3337">체크섬</span><span class="sxs-lookup"><span data-stu-id="c5035-3337">Checksum</span></span>

<span data-ttu-id="c5035-3338">없음</span><span class="sxs-lookup"><span data-stu-id="c5035-3338">No</span></span>


### <a name="definition"></a><span data-ttu-id="c5035-3339">정의</span><span class="sxs-lookup"><span data-stu-id="c5035-3339">Definition</span></span>

<span data-ttu-id="c5035-3340">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3340">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3341">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3341">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3342">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3342">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="c5035-3343">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3343">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3344">Func_unformatted_ssn 함수는 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3344">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3345">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3345">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="c5035-3346">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3346">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3347">Func_randomized_formatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3347">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3348">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3348">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="c5035-3349">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3349">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="c5035-3350">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 55% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3350">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c5035-3351">Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3351">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="c5035-3352">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3352">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="c5035-3353">Func_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5035-3353">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="c5035-3354">키워드</span><span class="sxs-lookup"><span data-stu-id="c5035-3354">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="c5035-3355">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="c5035-3355">Keyword_ssn</span></span>

- <span data-ttu-id="c5035-3356">Social Security
</span><span class="sxs-lookup"><span data-stu-id="c5035-3356">Social Security</span></span> 
- <span data-ttu-id="c5035-3357">Social Security#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3357">Social Security#</span></span> 
- <span data-ttu-id="c5035-3358">Soc Sec
</span><span class="sxs-lookup"><span data-stu-id="c5035-3358">Soc Sec</span></span> 
- <span data-ttu-id="c5035-3359">SSN</span><span class="sxs-lookup"><span data-stu-id="c5035-3359">SSN</span></span> 
- <span data-ttu-id="c5035-3360">SSNS
</span><span class="sxs-lookup"><span data-stu-id="c5035-3360">SSNS</span></span> 
- <span data-ttu-id="c5035-3361">SSN#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3361">SSN#</span></span> 
- <span data-ttu-id="c5035-3362">SS#
</span><span class="sxs-lookup"><span data-stu-id="c5035-3362">SS#</span></span> 
- <span data-ttu-id="c5035-3363">SSID
</span><span class="sxs-lookup"><span data-stu-id="c5035-3363">SSID</span></span> 
   

