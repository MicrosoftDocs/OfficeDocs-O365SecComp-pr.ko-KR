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
ms.collection:
- M365-security-compliance
description: Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 준비가 된 80 중요 한 정보 유형이 포함 되어 있습니다. 이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다.
ms.openlocfilehash: e9811b285e98a791570dc91e275cb5cead4f8bc9
ms.sourcegitcommit: 6e8e2b43a4bea31c1e835c5b050824651c6a0094
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30537645"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="a9974-104">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="a9974-104">What the sensitive information types look for</span></span>

<span data-ttu-id="a9974-105">Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 수 있는 중요 한 정보 유형이 많이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="a9974-106">이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="a9974-107">중요한 정보 유형은 정규식이나 함수로 식별될 수 있는 패턴으로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="a9974-108">또한 키워드 및 체크섬과 같은 확증적인 증거를 사용하여 중요한 정보 유형을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="a9974-109">이러한 평가 프로세스에서 신뢰 수준 및 근접성도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="a9974-110">ABA 라우팅 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-111">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-111">Format</span></span>

<span data-ttu-id="a9974-112">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-113">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-113">Pattern</span></span>

<span data-ttu-id="a9974-114">서식이</span><span class="sxs-lookup"><span data-stu-id="a9974-114">Formatted:</span></span>
- <span data-ttu-id="a9974-115">0, 1, 2, 3, 6, 7 또는 8로 시작하는 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="a9974-116">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-116">A hyphen</span></span>
- <span data-ttu-id="a9974-117">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-117">Four digits</span></span>
- <span data-ttu-id="a9974-118">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-118">A hyphen</span></span>
- <span data-ttu-id="a9974-119">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-119">A digit</span></span>

<span data-ttu-id="a9974-120">서식 없음: 0, 1, 2, 3, 6, 7 또는 8로 시작 하는 9 개의 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="a9974-121">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-121">Checksum</span></span>

<span data-ttu-id="a9974-122">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-123">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-123">Definition</span></span>

<span data-ttu-id="a9974-124">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-125">Func_aba_routing 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-126">Keyword_ABA_Routing의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="a9974-127">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="a9974-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="a9974-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="a9974-129">aba</span><span class="sxs-lookup"><span data-stu-id="a9974-129">aba</span></span>
- <span data-ttu-id="a9974-130">aba #</span><span class="sxs-lookup"><span data-stu-id="a9974-130">aba #</span></span>
- <span data-ttu-id="a9974-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="a9974-131">aba routing #</span></span>
- <span data-ttu-id="a9974-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="a9974-132">aba routing number</span></span>
- <span data-ttu-id="a9974-133">aba</span><span class="sxs-lookup"><span data-stu-id="a9974-133">aba#</span></span>
- <span data-ttu-id="a9974-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="a9974-134">abarouting#</span></span>
- <span data-ttu-id="a9974-135">aba number</span><span class="sxs-lookup"><span data-stu-id="a9974-135">aba number</span></span>
- <span data-ttu-id="a9974-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-136">abaroutingnumber</span></span>
- <span data-ttu-id="a9974-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="a9974-137">american bank association routing #</span></span>
- <span data-ttu-id="a9974-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="a9974-138">american bank association routing number</span></span>
- <span data-ttu-id="a9974-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="a9974-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="a9974-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="a9974-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="a9974-141">bank routing number</span></span>
- <span data-ttu-id="a9974-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="a9974-142">bankrouting#</span></span>
- <span data-ttu-id="a9974-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-143">bankroutingnumber</span></span>
- <span data-ttu-id="a9974-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="a9974-144">routing transit number</span></span>
- <span data-ttu-id="a9974-145">rtn</span><span class="sxs-lookup"><span data-stu-id="a9974-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="a9974-146">아르헨티나 국가 ID(DNI) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-147">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-147">Format</span></span>

<span data-ttu-id="a9974-148">마침표로 구분된 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-149">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-149">Pattern</span></span>

<span data-ttu-id="a9974-150">8자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-150">Eight digits:</span></span>
- <span data-ttu-id="a9974-151">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-151">Two digits</span></span>
- <span data-ttu-id="a9974-152">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-152">A period</span></span>
- <span data-ttu-id="a9974-153">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-153">Three digits</span></span>
- <span data-ttu-id="a9974-154">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-154">A period</span></span>
- <span data-ttu-id="a9974-155">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-156">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-156">Checksum</span></span>

<span data-ttu-id="a9974-157">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-158">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-158">Definition</span></span>

<span data-ttu-id="a9974-159">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-160">정규식 Regex_argentina_national_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-161">Keyword_argentina_national_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-162">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="a9974-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="a9974-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="a9974-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="a9974-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="a9974-165">ID</span><span class="sxs-lookup"><span data-stu-id="a9974-165">Identity</span></span> 
- <span data-ttu-id="a9974-166">식별 국가 id 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="a9974-167">DNI</span><span class="sxs-lookup"><span data-stu-id="a9974-167">DNI</span></span> 
- <span data-ttu-id="a9974-168">개인의 NIC 국내 레지스트리</span><span class="sxs-lookup"><span data-stu-id="a9974-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="a9974-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="a9974-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="a9974-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="a9974-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="a9974-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="a9974-171">Identidad</span></span> 
- <span data-ttu-id="a9974-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="a9974-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="a9974-173">호주 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-174">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-174">Format</span></span>

<span data-ttu-id="a9974-175">6-10자리 숫자(은행 지점 번호 포함 또는 제외)</span><span class="sxs-lookup"><span data-stu-id="a9974-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-176">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-176">Pattern</span></span>

<span data-ttu-id="a9974-177">계좌 번호는 6-10자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="a9974-178">호주 은행 지점 번호:</span><span class="sxs-lookup"><span data-stu-id="a9974-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="a9974-179">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-179">Three digits</span></span> 
- <span data-ttu-id="a9974-180">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-180">A hyphen</span></span> 
- <span data-ttu-id="a9974-181">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-182">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-182">Checksum</span></span>

<span data-ttu-id="a9974-183">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-184">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-184">Definition</span></span>

<span data-ttu-id="a9974-185">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-186">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="a9974-187">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="a9974-188">Regex_australia_bank_account_number_bsb 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="a9974-189">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-190">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="a9974-191">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-192">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="a9974-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="a9974-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="a9974-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="a9974-194">swift bank code</span></span>
- <span data-ttu-id="a9974-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="a9974-195">correspondent bank</span></span>
- <span data-ttu-id="a9974-196">base currency</span><span class="sxs-lookup"><span data-stu-id="a9974-196">base currency</span></span>
- <span data-ttu-id="a9974-197">usa account</span><span class="sxs-lookup"><span data-stu-id="a9974-197">usa account</span></span>
- <span data-ttu-id="a9974-198">holder address</span><span class="sxs-lookup"><span data-stu-id="a9974-198">holder address</span></span>
- <span data-ttu-id="a9974-199">bank address</span><span class="sxs-lookup"><span data-stu-id="a9974-199">bank address</span></span>
- <span data-ttu-id="a9974-200">information account</span><span class="sxs-lookup"><span data-stu-id="a9974-200">information account</span></span>
- <span data-ttu-id="a9974-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="a9974-201">fund transfers</span></span>
- <span data-ttu-id="a9974-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="a9974-202">bank charges</span></span>
- <span data-ttu-id="a9974-203">bank details</span><span class="sxs-lookup"><span data-stu-id="a9974-203">bank details</span></span>
- <span data-ttu-id="a9974-204">banking information</span><span class="sxs-lookup"><span data-stu-id="a9974-204">banking information</span></span>
- <span data-ttu-id="a9974-205">full names</span><span class="sxs-lookup"><span data-stu-id="a9974-205">full names</span></span>
- <span data-ttu-id="a9974-206">iaea</span><span class="sxs-lookup"><span data-stu-id="a9974-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="a9974-207">호주 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-208">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-208">Format</span></span>

<span data-ttu-id="a9974-209">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-210">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-210">Pattern</span></span>

<span data-ttu-id="a9974-211">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="a9974-212">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-213">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-213">Two digits</span></span> 
- <span data-ttu-id="a9974-214">5자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="a9974-215">또는</span><span class="sxs-lookup"><span data-stu-id="a9974-215">OR</span></span>

- <span data-ttu-id="a9974-216">1-2개의 선택적 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-217">4-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-217">4-9 digits</span></span>

<span data-ttu-id="a9974-218">또는</span><span class="sxs-lookup"><span data-stu-id="a9974-218">OR</span></span>

- <span data-ttu-id="a9974-219">9자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-220">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-220">Checksum</span></span>

<span data-ttu-id="a9974-221">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-222">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-222">Definition</span></span>

<span data-ttu-id="a9974-223">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-224">Regex_australia_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-225">Keyword_australia_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="a9974-226">Keyword_australia_drivers_license_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-227">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="a9974-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="a9974-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="a9974-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="a9974-229">international driving permits</span></span>
- <span data-ttu-id="a9974-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="a9974-230">australian automobile association</span></span>
- <span data-ttu-id="a9974-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="a9974-231">international driving permit</span></span>
- <span data-ttu-id="a9974-232">driverlicence</span><span class="sxs-lookup"><span data-stu-id="a9974-232">DriverLicence</span></span>
- <span data-ttu-id="a9974-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="a9974-233">DriverLicences</span></span>
- <span data-ttu-id="a9974-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-234">Driver Lic</span></span>
- <span data-ttu-id="a9974-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-235">Driver Licence</span></span>
- <span data-ttu-id="a9974-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-236">Driver Licences</span></span>
- <span data-ttu-id="a9974-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="a9974-237">DriversLic</span></span>
- <span data-ttu-id="a9974-238">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-238">DriversLicence</span></span>
- <span data-ttu-id="a9974-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="a9974-239">DriversLicences</span></span>
- <span data-ttu-id="a9974-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-240">Drivers Lic</span></span>
- <span data-ttu-id="a9974-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-241">Drivers Lics</span></span>
- <span data-ttu-id="a9974-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-242">Drivers Licence</span></span>
- <span data-ttu-id="a9974-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-243">Drivers Licences</span></span>
- <span data-ttu-id="a9974-244">driver' Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-244">Driver'Lic</span></span>
- <span data-ttu-id="a9974-245">driver'lics</span><span class="sxs-lookup"><span data-stu-id="a9974-245">Driver'Lics</span></span>
- <span data-ttu-id="a9974-246">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-246">Driver'Licence</span></span>
- <span data-ttu-id="a9974-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-247">Driver'Licences</span></span>
- <span data-ttu-id="a9974-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-248">Driver' Lic</span></span>
- <span data-ttu-id="a9974-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-249">Driver' Lics</span></span>
- <span data-ttu-id="a9974-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-250">Driver' Licence</span></span>
- <span data-ttu-id="a9974-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-251">Driver' Licences</span></span>
- <span data-ttu-id="a9974-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="a9974-252">Driver'sLic</span></span>
- <span data-ttu-id="a9974-253">drivers (slics)</span><span class="sxs-lookup"><span data-stu-id="a9974-253">Driver'sLics</span></span>
- <span data-ttu-id="a9974-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="a9974-254">Driver'sLicence</span></span>
- <span data-ttu-id="a9974-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="a9974-255">Driver'sLicences</span></span>
- <span data-ttu-id="a9974-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-256">Driver's Lic</span></span>
- <span data-ttu-id="a9974-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-257">Driver's Lics</span></span>
- <span data-ttu-id="a9974-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-258">Driver's Licence</span></span>
- <span data-ttu-id="a9974-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-259">Driver's Licences</span></span>
- <span data-ttu-id="a9974-260">driverlic #</span><span class="sxs-lookup"><span data-stu-id="a9974-260">DriverLic#</span></span>
- <span data-ttu-id="a9974-261">driverlics #</span><span class="sxs-lookup"><span data-stu-id="a9974-261">DriverLics#</span></span>
- <span data-ttu-id="a9974-262">driverlicence #</span><span class="sxs-lookup"><span data-stu-id="a9974-262">DriverLicence#</span></span>
- <span data-ttu-id="a9974-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="a9974-263">DriverLicences#</span></span>
- <span data-ttu-id="a9974-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-264">Driver Lic#</span></span>
- <span data-ttu-id="a9974-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-265">Driver Lics#</span></span>
- <span data-ttu-id="a9974-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="a9974-266">Driver Licence#</span></span>
- <span data-ttu-id="a9974-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="a9974-267">Driver Licences#</span></span>
- <span data-ttu-id="a9974-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="a9974-268">DriversLic#</span></span>
- <span data-ttu-id="a9974-269">driverslics #</span><span class="sxs-lookup"><span data-stu-id="a9974-269">DriversLics#</span></span>
- <span data-ttu-id="a9974-270">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-270">DriversLicence#</span></span>
- <span data-ttu-id="a9974-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="a9974-271">DriversLicences#</span></span>
- <span data-ttu-id="a9974-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-272">Drivers Lic#</span></span>
- <span data-ttu-id="a9974-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-273">Drivers Lics#</span></span>
- <span data-ttu-id="a9974-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="a9974-274">Drivers Licence#</span></span>
- <span data-ttu-id="a9974-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="a9974-275">Drivers Licences#</span></span>
- <span data-ttu-id="a9974-276">driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="a9974-276">Driver'Lic#</span></span>
- <span data-ttu-id="a9974-277">driver'lics #</span><span class="sxs-lookup"><span data-stu-id="a9974-277">Driver'Lics#</span></span>
- <span data-ttu-id="a9974-278">driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-278">Driver'Licence#</span></span>
- <span data-ttu-id="a9974-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="a9974-279">Driver'Licences#</span></span>
- <span data-ttu-id="a9974-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-280">Driver' Lic#</span></span>
- <span data-ttu-id="a9974-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-281">Driver' Lics#</span></span>
- <span data-ttu-id="a9974-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="a9974-282">Driver' Licence#</span></span>
- <span data-ttu-id="a9974-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="a9974-283">Driver' Licences#</span></span>
- <span data-ttu-id="a9974-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="a9974-284">Driver'sLic#</span></span>
- <span data-ttu-id="a9974-285">drivers (slics #)</span><span class="sxs-lookup"><span data-stu-id="a9974-285">Driver'sLics#</span></span>
- <span data-ttu-id="a9974-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="a9974-286">Driver'sLicence#</span></span>
- <span data-ttu-id="a9974-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="a9974-287">Driver'sLicences#</span></span>
- <span data-ttu-id="a9974-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-288">Driver's Lic#</span></span>
- <span data-ttu-id="a9974-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-289">Driver's Lics#</span></span>
- <span data-ttu-id="a9974-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="a9974-290">Driver's Licence#</span></span>
- <span data-ttu-id="a9974-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="a9974-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="a9974-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="a9974-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="a9974-293">aaa</span><span class="sxs-lookup"><span data-stu-id="a9974-293">aaa</span></span>
- <span data-ttu-id="a9974-294">driverlicense</span><span class="sxs-lookup"><span data-stu-id="a9974-294">DriverLicense</span></span>
- <span data-ttu-id="a9974-295">driverlicenses</span><span class="sxs-lookup"><span data-stu-id="a9974-295">DriverLicenses</span></span>
- <span data-ttu-id="a9974-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="a9974-296">Driver License</span></span>
- <span data-ttu-id="a9974-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-297">Driver Licenses</span></span>
- <span data-ttu-id="a9974-298">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-298">DriversLicense</span></span>
- <span data-ttu-id="a9974-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-299">DriversLicenses</span></span>
- <span data-ttu-id="a9974-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="a9974-300">Drivers License</span></span>
- <span data-ttu-id="a9974-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-301">Drivers Licenses</span></span>
- <span data-ttu-id="a9974-302">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-302">Driver'License</span></span>
- <span data-ttu-id="a9974-303">driver'licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-303">Driver'Licenses</span></span>
- <span data-ttu-id="a9974-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="a9974-304">Driver' License</span></span>
- <span data-ttu-id="a9974-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-305">Driver' Licenses</span></span>
- <span data-ttu-id="a9974-306">driver'slicense</span><span class="sxs-lookup"><span data-stu-id="a9974-306">Driver'sLicense</span></span>
- <span data-ttu-id="a9974-307">driver'slicenses</span><span class="sxs-lookup"><span data-stu-id="a9974-307">Driver'sLicenses</span></span>
- <span data-ttu-id="a9974-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="a9974-308">Driver's License</span></span>
- <span data-ttu-id="a9974-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-309">Driver's Licenses</span></span>
- <span data-ttu-id="a9974-310">driverlicense #</span><span class="sxs-lookup"><span data-stu-id="a9974-310">DriverLicense#</span></span>
- <span data-ttu-id="a9974-311">driverlicenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-311">DriverLicenses#</span></span>
- <span data-ttu-id="a9974-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="a9974-312">Driver License#</span></span>
- <span data-ttu-id="a9974-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-313">Driver Licenses#</span></span>
- <span data-ttu-id="a9974-314">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-314">DriversLicense#</span></span>
- <span data-ttu-id="a9974-315">드라이버 라이선스 수</span><span class="sxs-lookup"><span data-stu-id="a9974-315">DriversLicenses#</span></span>
- <span data-ttu-id="a9974-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="a9974-316">Drivers License#</span></span>
- <span data-ttu-id="a9974-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-317">Drivers Licenses#</span></span>
- <span data-ttu-id="a9974-318">driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-318">Driver'License#</span></span>
- <span data-ttu-id="a9974-319">driver'licenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-319">Driver'Licenses#</span></span>
- <span data-ttu-id="a9974-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="a9974-320">Driver' License#</span></span>
- <span data-ttu-id="a9974-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-321">Driver' Licenses#</span></span>
- <span data-ttu-id="a9974-322">driver'slicense #</span><span class="sxs-lookup"><span data-stu-id="a9974-322">Driver'sLicense#</span></span>
- <span data-ttu-id="a9974-323">driver'slicenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="a9974-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="a9974-324">Driver's License#</span></span>
- <span data-ttu-id="a9974-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="a9974-326">호주 의료 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-327">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-327">Format</span></span>

<span data-ttu-id="a9974-328">10-11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-329">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-329">Pattern</span></span>

<span data-ttu-id="a9974-330">10-11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-330">10-11 digits:</span></span>
- <span data-ttu-id="a9974-331">첫 번째 숫자는 2-6 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="a9974-332">9번째 숫자는 검사 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="a9974-333">10번째 숫자는 문제 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="a9974-334">11번째 숫자(선택 사항)는 개인 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-335">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-335">Checksum</span></span>

<span data-ttu-id="a9974-336">예</span><span class="sxs-lookup"><span data-stu-id="a9974-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-337">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-337">Definition</span></span>

<span data-ttu-id="a9974-338">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-339">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-340">Keyword_Australia_Medical_Account_Number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="a9974-341">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-341">The checksum passes.</span></span>

<span data-ttu-id="a9974-342">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-343">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-344">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-345">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="a9974-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="a9974-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="a9974-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="a9974-347">bank account details</span></span>
- <span data-ttu-id="a9974-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="a9974-348">medicare payments</span></span>
- <span data-ttu-id="a9974-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="a9974-349">mortgage account</span></span>
- <span data-ttu-id="a9974-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="a9974-350">bank payments</span></span>
- <span data-ttu-id="a9974-351">information branch</span><span class="sxs-lookup"><span data-stu-id="a9974-351">information branch</span></span>
- <span data-ttu-id="a9974-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="a9974-352">credit card loan</span></span>
- <span data-ttu-id="a9974-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="a9974-353">department of human services</span></span>
- <span data-ttu-id="a9974-354">local service</span><span class="sxs-lookup"><span data-stu-id="a9974-354">local service</span></span>
- <span data-ttu-id="a9974-355">medicare</span><span class="sxs-lookup"><span data-stu-id="a9974-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="a9974-356">호주 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-357">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-357">Format</span></span>

<span data-ttu-id="a9974-358">문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-359">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-359">Pattern</span></span>

<span data-ttu-id="a9974-360">1개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-361">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-361">Checksum</span></span>

<span data-ttu-id="a9974-362">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-363">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-363">Definition</span></span>

<span data-ttu-id="a9974-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-365">Regex_australia_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-366">Keyword_passport 또는 Keyword_australia_passport_number의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-367">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="a9974-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-368">Keyword_passport</span></span>

- <span data-ttu-id="a9974-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="a9974-369">Passport Number</span></span>
- <span data-ttu-id="a9974-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="a9974-370">Passport No</span></span>
- <span data-ttu-id="a9974-371">Passport #</span><span class="sxs-lookup"><span data-stu-id="a9974-371">Passport #</span></span>
- <span data-ttu-id="a9974-372">여권</span><span class="sxs-lookup"><span data-stu-id="a9974-372">Passport#</span></span>
- <span data-ttu-id="a9974-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="a9974-373">PassportID</span></span>
- <span data-ttu-id="a9974-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="a9974-374">Passportno</span></span>
- <span data-ttu-id="a9974-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-375">passportnumber</span></span>
- <span data-ttu-id="a9974-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="a9974-376">パスポート</span></span>
- <span data-ttu-id="a9974-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="a9974-377">パスポート番号</span></span>
- <span data-ttu-id="a9974-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="a9974-378">パスポートのNum</span></span>
- <span data-ttu-id="a9974-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="a9974-379">パスポート ＃</span></span> 
- <span data-ttu-id="a9974-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a9974-380">Numéro de passeport</span></span>
- <span data-ttu-id="a9974-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="a9974-381">Passeport n °</span></span>
- <span data-ttu-id="a9974-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="a9974-382">Passeport Non</span></span>
- <span data-ttu-id="a9974-383">Passeport #</span><span class="sxs-lookup"><span data-stu-id="a9974-383">Passeport #</span></span>
- <span data-ttu-id="a9974-384">포트 #</span><span class="sxs-lookup"><span data-stu-id="a9974-384">Passeport#</span></span>
- <span data-ttu-id="a9974-385">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="a9974-385">PasseportNon</span></span>
- <span data-ttu-id="a9974-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="a9974-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="a9974-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="a9974-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="a9974-388">여권</span><span class="sxs-lookup"><span data-stu-id="a9974-388">passport</span></span>
- <span data-ttu-id="a9974-389">passport details</span><span class="sxs-lookup"><span data-stu-id="a9974-389">passport details</span></span>
- <span data-ttu-id="a9974-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="a9974-390">immigration and citizenship</span></span>
- <span data-ttu-id="a9974-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="a9974-391">commonwealth of australia</span></span>
- <span data-ttu-id="a9974-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="a9974-392">department of immigration</span></span>
- <span data-ttu-id="a9974-393">residential address</span><span class="sxs-lookup"><span data-stu-id="a9974-393">residential address</span></span>
- <span data-ttu-id="a9974-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="a9974-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="a9974-395">visa</span><span class="sxs-lookup"><span data-stu-id="a9974-395">visa</span></span>
- <span data-ttu-id="a9974-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="a9974-396">national identity card</span></span>
- <span data-ttu-id="a9974-397">passport number</span><span class="sxs-lookup"><span data-stu-id="a9974-397">passport number</span></span>
- <span data-ttu-id="a9974-398">travel document</span><span class="sxs-lookup"><span data-stu-id="a9974-398">travel document</span></span>
- <span data-ttu-id="a9974-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="a9974-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="a9974-400">호주 세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-401">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-401">Format</span></span>

<span data-ttu-id="a9974-402">8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-403">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-403">Pattern</span></span>

<span data-ttu-id="a9974-404">일반적으로 다음과 같이 공백과 함께 표시되는 8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="a9974-405">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-405">Three digits</span></span> 
- <span data-ttu-id="a9974-406">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-406">An optional space</span></span> 
- <span data-ttu-id="a9974-407">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-407">Three digits</span></span> 
- <span data-ttu-id="a9974-408">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-408">An optional space</span></span> 
- <span data-ttu-id="a9974-409">마지막 숫자가 검사 숫자인 2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-410">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-410">Checksum</span></span>

<span data-ttu-id="a9974-411">예</span><span class="sxs-lookup"><span data-stu-id="a9974-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-412">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-412">Definition</span></span>

<span data-ttu-id="a9974-413">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-414">Func_australian_tax_file_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-415">Keyword_Australia_Tax_File_Number 또는 Keyword_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="a9974-416">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-417">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="a9974-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="a9974-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="a9974-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="a9974-419">australian business number</span></span>
- <span data-ttu-id="a9974-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="a9974-420">marginal tax rate</span></span>
- <span data-ttu-id="a9974-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="a9974-421">medicare levy</span></span>
- <span data-ttu-id="a9974-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="a9974-422">portfolio number</span></span>
- <span data-ttu-id="a9974-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="a9974-423">service veterans</span></span>
- <span data-ttu-id="a9974-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="a9974-424">withholding tax</span></span>
- <span data-ttu-id="a9974-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="a9974-425">individual tax return</span></span>
- <span data-ttu-id="a9974-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="a9974-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="a9974-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="a9974-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="a9974-428">00000000</span><span class="sxs-lookup"><span data-stu-id="a9974-428">00000000</span></span>
- <span data-ttu-id="a9974-429">11111111</span><span class="sxs-lookup"><span data-stu-id="a9974-429">11111111</span></span>
- <span data-ttu-id="a9974-430">22222222</span><span class="sxs-lookup"><span data-stu-id="a9974-430">22222222</span></span>
- <span data-ttu-id="a9974-431">33333333</span><span class="sxs-lookup"><span data-stu-id="a9974-431">33333333</span></span>
- <span data-ttu-id="a9974-432">44444444</span><span class="sxs-lookup"><span data-stu-id="a9974-432">44444444</span></span>
- <span data-ttu-id="a9974-433">55555555</span><span class="sxs-lookup"><span data-stu-id="a9974-433">55555555</span></span>
- <span data-ttu-id="a9974-434">66666666</span><span class="sxs-lookup"><span data-stu-id="a9974-434">66666666</span></span>
- <span data-ttu-id="a9974-435">77777777</span><span class="sxs-lookup"><span data-stu-id="a9974-435">77777777</span></span>
- <span data-ttu-id="a9974-436">88888888</span><span class="sxs-lookup"><span data-stu-id="a9974-436">88888888</span></span>
- <span data-ttu-id="a9974-437">99999999</span><span class="sxs-lookup"><span data-stu-id="a9974-437">99999999</span></span>
- <span data-ttu-id="a9974-438">000000000</span><span class="sxs-lookup"><span data-stu-id="a9974-438">000000000</span></span>
- <span data-ttu-id="a9974-439">111111111</span><span class="sxs-lookup"><span data-stu-id="a9974-439">111111111</span></span>
- <span data-ttu-id="a9974-440">222222222</span><span class="sxs-lookup"><span data-stu-id="a9974-440">222222222</span></span>
- <span data-ttu-id="a9974-441">333333333</span><span class="sxs-lookup"><span data-stu-id="a9974-441">333333333</span></span>
- <span data-ttu-id="a9974-442">444444444</span><span class="sxs-lookup"><span data-stu-id="a9974-442">444444444</span></span>
- <span data-ttu-id="a9974-443">555555555</span><span class="sxs-lookup"><span data-stu-id="a9974-443">555555555</span></span>
- <span data-ttu-id="a9974-444">666666666</span><span class="sxs-lookup"><span data-stu-id="a9974-444">666666666</span></span>
- <span data-ttu-id="a9974-445">777777777</span><span class="sxs-lookup"><span data-stu-id="a9974-445">777777777</span></span>
- <span data-ttu-id="a9974-446">888888888</span><span class="sxs-lookup"><span data-stu-id="a9974-446">888888888</span></span>
- <span data-ttu-id="a9974-447">999999999</span><span class="sxs-lookup"><span data-stu-id="a9974-447">999999999</span></span>
- <span data-ttu-id="a9974-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="a9974-448">0000000000</span></span>
- <span data-ttu-id="a9974-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="a9974-449">1111111111</span></span>
- <span data-ttu-id="a9974-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="a9974-450">2222222222</span></span>
- <span data-ttu-id="a9974-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="a9974-451">3333333333</span></span>
- <span data-ttu-id="a9974-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="a9974-452">4444444444</span></span>
- <span data-ttu-id="a9974-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="a9974-453">5555555555</span></span>
- <span data-ttu-id="a9974-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="a9974-454">6666666666</span></span>
- <span data-ttu-id="a9974-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="a9974-455">7777777777</span></span>
- <span data-ttu-id="a9974-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="a9974-456">8888888888</span></span>
- <span data-ttu-id="a9974-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="a9974-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="a9974-458">Azure DocumentDB 인증 키</span><span class="sxs-lookup"><span data-stu-id="a9974-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="a9974-459">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-459">Format</span></span>

<span data-ttu-id="a9974-460">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "DocumentDb" 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-461">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-461">Pattern</span></span>

- <span data-ttu-id="a9974-462">"DocumentDb" 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="a9974-463">3-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-464">보다 큼 기호 (>), 등호 (=), 따옴표 (") 또는 아포스트로피 (')</span><span class="sxs-lookup"><span data-stu-id="a9974-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="a9974-465">86의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="a9974-466">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-467">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-467">Checksum</span></span>

<span data-ttu-id="a9974-468">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-469">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-469">Definition</span></span>

<span data-ttu-id="a9974-470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-471">정규식 CEP_Regex_AzureDocumentDBAuthKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-472">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!-- Azure Document DB Auth Key -->
<Entity id="0f587d92-eb28-44a9-bd1c-90f2892b47aa" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureDocumentDBAuthKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
          </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-473">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-473">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="a9974-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="a9974-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="a9974-475">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-476">극동</span><span class="sxs-lookup"><span data-stu-id="a9974-476">contoso</span></span>
- <span data-ttu-id="a9974-477">fabrikam</span><span class="sxs-lookup"><span data-stu-id="a9974-477">fabrikam</span></span>
- <span data-ttu-id="a9974-478">대양</span><span class="sxs-lookup"><span data-stu-id="a9974-478">northwind</span></span>
- <span data-ttu-id="a9974-479">샌드박스</span><span class="sxs-lookup"><span data-stu-id="a9974-479">sandbox</span></span>
- <span data-ttu-id="a9974-480">용 onebox</span><span class="sxs-lookup"><span data-stu-id="a9974-480">onebox</span></span>
- <span data-ttu-id="a9974-481">로컬</span><span class="sxs-lookup"><span data-stu-id="a9974-481">localhost</span></span>
- <span data-ttu-id="a9974-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="a9974-482">127.0.0.1</span></span>
- <span data-ttu-id="a9974-483">testacs입니다. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="a9974-483">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="a9974-484">s-int<!--no-hyperlink--></span><span class="sxs-lookup"><span data-stu-id="a9974-484">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="a9974-485">azure IAAS 데이터베이스 연결 문자열 및 azure SQL 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-485">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="a9974-486">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-486">Format</span></span>

<span data-ttu-id="a9974-487">"server", "server" 또는 "data source" 라는 문자열은 "cloudapp. azure"를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다. <!--no-hyperlink-->com "또는" cloudapp. <!--no-hyperlink-->net "또는" 데이터베이스. <!--no-hyperlink-->net "과 문자열" password "또는" password "또는" pwd "가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-487">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.<!--no-hyperlink-->com" or "cloudapp.azure.<!--no-hyperlink-->net" or "database.windows.<!--no-hyperlink-->net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-488">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-488">Pattern</span></span>

- <span data-ttu-id="a9974-489">문자열 "server", "Server" 또는 "data source"</span><span class="sxs-lookup"><span data-stu-id="a9974-489">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="a9974-490">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-490">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-491">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-491">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-492">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-492">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-493">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-493">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-494">문자열 "cloudapp. <!--no-hyperlink-->com "," cloudapp. <!--no-hyperlink-->net "또는" database. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="a9974-494">The string "cloudapp.azure.<!--no-hyperlink-->com", "cloudapp.azure.<!--no-hyperlink-->net", or "database.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="a9974-495">1-300에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-495">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-496">문자열 "password", "password" 또는 "pwd"</span><span class="sxs-lookup"><span data-stu-id="a9974-496">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="a9974-497">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-498">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-498">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-499">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-499">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-500">세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')가 아닌 하나 이상의 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-500">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="a9974-501">세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')</span><span class="sxs-lookup"><span data-stu-id="a9974-501">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-502">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-502">Checksum</span></span>

<span data-ttu-id="a9974-503">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-503">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-504">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-504">Definition</span></span>

<span data-ttu-id="a9974-505">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-505">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-506">정규식 CEP_Regex_AzureConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-506">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-507">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-507">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IAAS Database Connection String and Azure SQL Connection String-->
<Entity id="ce1a126d-186f-4700-8c0c-486157b953fd" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-508">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-508">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="a9974-509">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="a9974-509">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="a9974-510">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-510">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-511">극동</span><span class="sxs-lookup"><span data-stu-id="a9974-511">contoso</span></span>
- <span data-ttu-id="a9974-512">fabrikam</span><span class="sxs-lookup"><span data-stu-id="a9974-512">fabrikam</span></span>
- <span data-ttu-id="a9974-513">대양</span><span class="sxs-lookup"><span data-stu-id="a9974-513">northwind</span></span>
- <span data-ttu-id="a9974-514">샌드박스</span><span class="sxs-lookup"><span data-stu-id="a9974-514">sandbox</span></span>
- <span data-ttu-id="a9974-515">용 onebox</span><span class="sxs-lookup"><span data-stu-id="a9974-515">onebox</span></span>
- <span data-ttu-id="a9974-516">로컬</span><span class="sxs-lookup"><span data-stu-id="a9974-516">localhost</span></span>
- <span data-ttu-id="a9974-517">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="a9974-517">127.0.0.1</span></span>
- <span data-ttu-id="a9974-518">testacs입니다. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="a9974-518">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="a9974-519">s-int<!--no-hyperlink--></span><span class="sxs-lookup"><span data-stu-id="a9974-519">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="a9974-520">Azure IoT Connection 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-520">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="a9974-521">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-521">Format</span></span>

<span data-ttu-id="a9974-522">문자열 "HostName" 뒤에 "azure-devices" 라는 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열이 표시 됩니다. <!--no-hyperlink-->net "및" sharedaccesskey "</span><span class="sxs-lookup"><span data-stu-id="a9974-522">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.<!--no-hyperlink-->net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-523">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-523">Pattern</span></span>

- <span data-ttu-id="a9974-524">문자열 "HostName"</span><span class="sxs-lookup"><span data-stu-id="a9974-524">The string "HostName"</span></span>
- <span data-ttu-id="a9974-525">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-525">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-526">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-526">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-527">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-527">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-528">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-528">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-529">문자열 "azure-장치 <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="a9974-529">The string "azure-devices.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="a9974-530">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-530">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-531">"sharedaccesskey" 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-531">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="a9974-532">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-532">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-533">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-533">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-534">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-534">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-535">43의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-535">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="a9974-536">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-536">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-537">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-537">Checksum</span></span>

<span data-ttu-id="a9974-538">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-538">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-539">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-539">Definition</span></span>

<span data-ttu-id="a9974-540">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-540">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-541">정규식 CEP_Regex_AzureIoTConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-541">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-542">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-542">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IoT Connection String-->
<Entity id="0b34bec3-d5d6-4974-b7b0-dcdb5c90c29d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureIoTConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-543">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-543">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="a9974-544">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="a9974-544">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="a9974-545">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-545">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-546">극동</span><span class="sxs-lookup"><span data-stu-id="a9974-546">contoso</span></span>
- <span data-ttu-id="a9974-547">fabrikam</span><span class="sxs-lookup"><span data-stu-id="a9974-547">fabrikam</span></span>
- <span data-ttu-id="a9974-548">대양</span><span class="sxs-lookup"><span data-stu-id="a9974-548">northwind</span></span>
- <span data-ttu-id="a9974-549">샌드박스</span><span class="sxs-lookup"><span data-stu-id="a9974-549">sandbox</span></span>
- <span data-ttu-id="a9974-550">용 onebox</span><span class="sxs-lookup"><span data-stu-id="a9974-550">onebox</span></span>
- <span data-ttu-id="a9974-551">로컬</span><span class="sxs-lookup"><span data-stu-id="a9974-551">localhost</span></span>
- <span data-ttu-id="a9974-552">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="a9974-552">127.0.0.1</span></span>
- <span data-ttu-id="a9974-553">testacs입니다. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="a9974-553">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="a9974-554">s-int<!--no-hyperlink--></span><span class="sxs-lookup"><span data-stu-id="a9974-554">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="a9974-555">Azure 게시 설정 암호</span><span class="sxs-lookup"><span data-stu-id="a9974-555">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="a9974-556">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-556">Format</span></span>

<span data-ttu-id="a9974-557">문자열 "userpwd =" 다음에 영숫자 문자열이 나옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-557">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-558">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-558">Pattern</span></span>

- <span data-ttu-id="a9974-559">문자열 "userpwd ="</span><span class="sxs-lookup"><span data-stu-id="a9974-559">The string "userpwd="</span></span>
- <span data-ttu-id="a9974-560">60 대 문자와 숫자의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-560">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="a9974-561">큰따옴표 (")</span><span class="sxs-lookup"><span data-stu-id="a9974-561">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-562">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-562">Checksum</span></span>

<span data-ttu-id="a9974-563">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-563">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-564">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-564">Definition</span></span>

<span data-ttu-id="a9974-565">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-565">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-566">정규식 CEP_Regex_AzurePublishSettingPasswords 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-566">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-567">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-567">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```
<!--Azure Publish Setting Password-->
<Entity id="75f4cc8a-a68e-49e5-89ce-fa8f03d286a5" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="CEP_Regex_AzurePublishSettingPasswords" />
       <Any minMatches="0" maxMatches="0">
           <Match idRef="CEP_CommonExampleKeywords" />
       </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-568">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-568">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="a9974-569">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="a9974-569">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="a9974-570">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-570">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-571">극동</span><span class="sxs-lookup"><span data-stu-id="a9974-571">contoso</span></span>
- <span data-ttu-id="a9974-572">fabrikam</span><span class="sxs-lookup"><span data-stu-id="a9974-572">fabrikam</span></span>
- <span data-ttu-id="a9974-573">대양</span><span class="sxs-lookup"><span data-stu-id="a9974-573">northwind</span></span>
- <span data-ttu-id="a9974-574">샌드박스</span><span class="sxs-lookup"><span data-stu-id="a9974-574">sandbox</span></span>
- <span data-ttu-id="a9974-575">용 onebox</span><span class="sxs-lookup"><span data-stu-id="a9974-575">onebox</span></span>
- <span data-ttu-id="a9974-576">로컬</span><span class="sxs-lookup"><span data-stu-id="a9974-576">localhost</span></span>
- <span data-ttu-id="a9974-577">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="a9974-577">127.0.0.1</span></span>
- <span data-ttu-id="a9974-578">testacs입니다. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="a9974-578">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="a9974-579">s-int<!--no-hyperlink--></span><span class="sxs-lookup"><span data-stu-id="a9974-579">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="a9974-580">Azure Redis 캐시 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-580">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="a9974-581">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-581">Format</span></span>

<span data-ttu-id="a9974-582">문자열 "redis. <!--no-hyperlink-->net "문자열" password "또는" pwd "를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-582">The string "redis.cache.windows.<!--no-hyperlink-->net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-583">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-583">Pattern</span></span>

- <span data-ttu-id="a9974-584">문자열 "redis. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="a9974-584">The string "redis.cache.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="a9974-585">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-585">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-586">문자열 "password" 또는 "pwd"</span><span class="sxs-lookup"><span data-stu-id="a9974-586">The string "password" or "pwd"</span></span>
- <span data-ttu-id="a9974-587">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-587">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-588">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-588">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-589">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-589">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-590">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-590">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="a9974-591">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-591">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-592">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-592">Checksum</span></span>

<span data-ttu-id="a9974-593">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-593">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-594">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-594">Definition</span></span>

<span data-ttu-id="a9974-595">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-596">정규식 CEP_Regex_AzureRedisCacheConnectionString가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-596">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="a9974-597">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-597">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Redis Cache Connection String-->
<Entity id="095a7e6c-efd8-46d5-af7b-5298d53a49fc" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureRedisCacheConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-598">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-598">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="a9974-599">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="a9974-599">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="a9974-600">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-600">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-601">극동</span><span class="sxs-lookup"><span data-stu-id="a9974-601">contoso</span></span>
- <span data-ttu-id="a9974-602">fabrikam</span><span class="sxs-lookup"><span data-stu-id="a9974-602">fabrikam</span></span>
- <span data-ttu-id="a9974-603">대양</span><span class="sxs-lookup"><span data-stu-id="a9974-603">northwind</span></span>
- <span data-ttu-id="a9974-604">샌드박스</span><span class="sxs-lookup"><span data-stu-id="a9974-604">sandbox</span></span>
- <span data-ttu-id="a9974-605">용 onebox</span><span class="sxs-lookup"><span data-stu-id="a9974-605">onebox</span></span>
- <span data-ttu-id="a9974-606">로컬</span><span class="sxs-lookup"><span data-stu-id="a9974-606">localhost</span></span>
- <span data-ttu-id="a9974-607">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="a9974-607">127.0.0.1</span></span>
- <span data-ttu-id="a9974-608">testacs입니다. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="a9974-608">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="a9974-609">s-int<!--no-hyperlink--></span><span class="sxs-lookup"><span data-stu-id="a9974-609">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="a9974-610">Azure SAS</span><span class="sxs-lookup"><span data-stu-id="a9974-610">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="a9974-611">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-611">Format</span></span>

<span data-ttu-id="a9974-612">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 문자열 "sig"</span><span class="sxs-lookup"><span data-stu-id="a9974-612">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-613">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-613">Pattern</span></span>

- <span data-ttu-id="a9974-614">문자열 "sig"</span><span class="sxs-lookup"><span data-stu-id="a9974-614">The string "sig"</span></span>
- <span data-ttu-id="a9974-615">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-615">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-616">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-616">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-617">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-617">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-618">대/소문자, 숫자 또는 백분율 기호 (%)가 43-53 자 사이의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-618">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="a9974-619">문자열 "% 3d"</span><span class="sxs-lookup"><span data-stu-id="a9974-619">The string "%3d"</span></span>
- <span data-ttu-id="a9974-620">소문자 또는 대문자, 숫자 또는 백분율 기호 (%)가 아닌 모든 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-620">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-621">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-621">Checksum</span></span>

<span data-ttu-id="a9974-622">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-622">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-623">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-623">Definition</span></span>

<span data-ttu-id="a9974-624">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-624">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-625">정규식 CEP_Regex_AzureSAS 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-625">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="a9974-626">Azure Service Bus 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-626">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="a9974-627">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-627">Format</span></span>

<span data-ttu-id="a9974-628">문자열 "끝점" 뒤에 "servicebus" 라는 문자열을 포함 하 여 아래 패턴에 나와 있는 문자 및 문자열이 표시 됩니다. <!--no-hyperlink-->net "및" SharedAccesKey "을 차례로 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-628">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.<!--no-hyperlink-->net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-629">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-629">Pattern</span></span>

- <span data-ttu-id="a9974-630">문자열 "끝점"</span><span class="sxs-lookup"><span data-stu-id="a9974-630">The string "EndPoint"</span></span>
- <span data-ttu-id="a9974-631">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-631">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-632">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-632">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-633">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-633">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-634">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-634">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-635">문자열 "servicebus. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="a9974-635">The string "servicebus.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="a9974-636">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-636">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-637">"sharedaccesskey" 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-637">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="a9974-638">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-638">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-639">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-639">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-640">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-640">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-641">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-641">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="a9974-642">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-642">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-643">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-643">Checksum</span></span>

<span data-ttu-id="a9974-644">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-644">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-645">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-645">Definition</span></span>

<span data-ttu-id="a9974-646">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-646">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-647">정규식 CEP_Regex_AzureServiceBusConnectionString가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-647">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="a9974-648">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-648">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Service Bus Connection String-->
<Entity id="b9a6578f-a83f-4fcd-bf44-2130bae49a6f" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureServiceBusConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-649">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-649">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="a9974-650">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="a9974-650">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="a9974-651">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-651">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-652">극동</span><span class="sxs-lookup"><span data-stu-id="a9974-652">contoso</span></span>
- <span data-ttu-id="a9974-653">fabrikam</span><span class="sxs-lookup"><span data-stu-id="a9974-653">fabrikam</span></span>
- <span data-ttu-id="a9974-654">대양</span><span class="sxs-lookup"><span data-stu-id="a9974-654">northwind</span></span>
- <span data-ttu-id="a9974-655">샌드박스</span><span class="sxs-lookup"><span data-stu-id="a9974-655">sandbox</span></span>
- <span data-ttu-id="a9974-656">용 onebox</span><span class="sxs-lookup"><span data-stu-id="a9974-656">onebox</span></span>
- <span data-ttu-id="a9974-657">로컬</span><span class="sxs-lookup"><span data-stu-id="a9974-657">localhost</span></span>
- <span data-ttu-id="a9974-658">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="a9974-658">127.0.0.1</span></span>
- <span data-ttu-id="a9974-659">testacs입니다. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="a9974-659">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="a9974-660">s-int<!--no-hyperlink--></span><span class="sxs-lookup"><span data-stu-id="a9974-660">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="a9974-661">Azure 저장소 계정 키</span><span class="sxs-lookup"><span data-stu-id="a9974-661">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="a9974-662">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-662">Format</span></span>

<span data-ttu-id="a9974-663">"defaultendpointsprotocol" 문자열은 "AccountKey" 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-663">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-664">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-664">Pattern</span></span>

- <span data-ttu-id="a9974-665">문자열 "defaultendpointsprotocol"</span><span class="sxs-lookup"><span data-stu-id="a9974-665">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="a9974-666">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-666">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-667">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-667">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-668">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-668">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-669">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-669">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-670">문자열 "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="a9974-670">The string "AccountKey"</span></span>
- <span data-ttu-id="a9974-671">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-671">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-672">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-672">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-673">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-673">0-2 whitespace characters</span></span>
- <span data-ttu-id="a9974-674">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-674">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="a9974-675">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-675">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-676">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-676">Checksum</span></span>

<span data-ttu-id="a9974-677">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-677">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-678">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-678">Definition</span></span>

<span data-ttu-id="a9974-679">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-679">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-680">정규식 CEP_Regex_AzureStorageAccountKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-680">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-681">CEP_AzureEmulatorStorageAccountFilter 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-681">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-682">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-682">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key-->
<Entity id="c7bc98e8-551a-4c35-a92d-d2c8cda714a7" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_AzureEmulatorStorageAccountFilter" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-683">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-683">Keywords</span></span>

#### <a name="cepazureemulatorstorageaccountfilter"></a><span data-ttu-id="a9974-684">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="a9974-684">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="a9974-685">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-685">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="a9974-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="a9974-687">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="a9974-687">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="a9974-688">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-688">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-689">극동</span><span class="sxs-lookup"><span data-stu-id="a9974-689">contoso</span></span>
- <span data-ttu-id="a9974-690">fabrikam</span><span class="sxs-lookup"><span data-stu-id="a9974-690">fabrikam</span></span>
- <span data-ttu-id="a9974-691">대양</span><span class="sxs-lookup"><span data-stu-id="a9974-691">northwind</span></span>
- <span data-ttu-id="a9974-692">샌드박스</span><span class="sxs-lookup"><span data-stu-id="a9974-692">sandbox</span></span>
- <span data-ttu-id="a9974-693">용 onebox</span><span class="sxs-lookup"><span data-stu-id="a9974-693">onebox</span></span>
- <span data-ttu-id="a9974-694">로컬</span><span class="sxs-lookup"><span data-stu-id="a9974-694">localhost</span></span>
- <span data-ttu-id="a9974-695">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="a9974-695">127.0.0.1</span></span>
- <span data-ttu-id="a9974-696">testacs입니다. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="a9974-696">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="a9974-697">s-int<!--no-hyperlink--></span><span class="sxs-lookup"><span data-stu-id="a9974-697">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="a9974-698">Azure 저장소 계정 키 (일반)</span><span class="sxs-lookup"><span data-stu-id="a9974-698">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-699">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-699">Format</span></span>

<span data-ttu-id="a9974-700">아래 패턴에 윤곽선이 있는 문자 앞 이나 뒤에 오는 86 문자의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-700">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-701">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-701">Pattern</span></span>

- <span data-ttu-id="a9974-702">> (보다 큼 기호), 아포스트로피 ('), 등호 (=), 따옴표 (") 또는 숫자 기호 (#)</span><span class="sxs-lookup"><span data-stu-id="a9974-702">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="a9974-703">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-703">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="a9974-704">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-704">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="a9974-705">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-705">Checksum</span></span>

<span data-ttu-id="a9974-706">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-706">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-707">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-707">Definition</span></span>

<span data-ttu-id="a9974-708">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-708">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-709">정규식 CEP_Regex_AzureStorageAccountKeyGeneric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-709">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="a9974-710">벨기에 국가 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-710">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-711">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-711">Format</span></span>

<span data-ttu-id="a9974-712">11자리 숫자와 구분 기호</span><span class="sxs-lookup"><span data-stu-id="a9974-712">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-713">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-713">Pattern</span></span>

<span data-ttu-id="a9974-714">11자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="a9974-714">11 digits plus delimiters:</span></span>
- <span data-ttu-id="a9974-715">생년월일을 나타내는 YY.MM.DD 형식의 6자리 숫자와 마침표 2개 </span><span class="sxs-lookup"><span data-stu-id="a9974-715">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="a9974-716">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-716">A hyphen</span></span> 
- <span data-ttu-id="a9974-717">세 개의 순차적 숫자(남성의 경우 홀수, 여성의 경우 짝수) </span><span class="sxs-lookup"><span data-stu-id="a9974-717">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="a9974-718">마침표</span><span class="sxs-lookup"><span data-stu-id="a9974-718">A period</span></span> 
- <span data-ttu-id="a9974-719">검사 숫자에 해당하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-719">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-720">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-720">Checksum</span></span>

<span data-ttu-id="a9974-721">예</span><span class="sxs-lookup"><span data-stu-id="a9974-721">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-722">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-722">Definition</span></span>

<span data-ttu-id="a9974-723">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-723">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-724">Func_belgium_national_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-724">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-725">Keyword_belgium_national_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-725">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="a9974-726">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-726">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-727">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-727">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="a9974-728">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="a9974-728">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="a9974-729">ID</span><span class="sxs-lookup"><span data-stu-id="a9974-729">Identity</span></span>
- <span data-ttu-id="a9974-730">등록</span><span class="sxs-lookup"><span data-stu-id="a9974-730">Registration</span></span>
- <span data-ttu-id="a9974-731">확인과</span><span class="sxs-lookup"><span data-stu-id="a9974-731">Identification</span></span> 
- <span data-ttu-id="a9974-732">ID</span><span class="sxs-lookup"><span data-stu-id="a9974-732">ID</span></span> 
- <span data-ttu-id="a9974-733">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="a9974-733">Identiteitskaart</span></span>
- <span data-ttu-id="a9974-734">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="a9974-734">Registratie nummer</span></span> 
- <span data-ttu-id="a9974-735">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="a9974-735">Identificatie nummer</span></span> 
- <span data-ttu-id="a9974-736">Identiteit</span><span class="sxs-lookup"><span data-stu-id="a9974-736">Identiteit</span></span>
- <span data-ttu-id="a9974-737">Registratie</span><span class="sxs-lookup"><span data-stu-id="a9974-737">Registratie</span></span>
- <span data-ttu-id="a9974-738">Identificatie</span><span class="sxs-lookup"><span data-stu-id="a9974-738">Identificatie</span></span> 
- <span data-ttu-id="a9974-739">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="a9974-739">Carte d’identité</span></span> 
- <span data-ttu-id="a9974-740">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="a9974-740">numéro d'immatriculation</span></span>
- <span data-ttu-id="a9974-741">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="a9974-741">numéro d'identification</span></span>
- <span data-ttu-id="a9974-742">identité</span><span class="sxs-lookup"><span data-stu-id="a9974-742">identité</span></span> 
- <span data-ttu-id="a9974-743">inscription</span><span class="sxs-lookup"><span data-stu-id="a9974-743">inscription</span></span> 
- <span data-ttu-id="a9974-744">Identifikation</span><span class="sxs-lookup"><span data-stu-id="a9974-744">Identifikation</span></span>
- <span data-ttu-id="a9974-745">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="a9974-745">Identifizierung</span></span>
- <span data-ttu-id="a9974-746">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-746">Identifikationsnummer</span></span>
- <span data-ttu-id="a9974-747">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="a9974-747">Personalausweis</span></span>
- <span data-ttu-id="a9974-748">Registrierung</span><span class="sxs-lookup"><span data-stu-id="a9974-748">Registrierung</span></span>
- <span data-ttu-id="a9974-749">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-749">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="a9974-750">브라질 CPF 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-750">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-751">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-751">Format</span></span>

<span data-ttu-id="a9974-752">서식이 있거나 서식이 없을 수 있는 검사 숫자를 포함하는 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-752">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-753">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-753">Pattern</span></span>

<span data-ttu-id="a9974-754">서식이</span><span class="sxs-lookup"><span data-stu-id="a9974-754">Formatted:</span></span>
- <span data-ttu-id="a9974-755">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-755">Three digits</span></span> 
- <span data-ttu-id="a9974-756">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-756">A period</span></span> 
- <span data-ttu-id="a9974-757">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-757">Three digits</span></span> 
- <span data-ttu-id="a9974-758">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-758">A period</span></span> 
- <span data-ttu-id="a9974-759">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-759">Three digits</span></span> 
- <span data-ttu-id="a9974-760">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-760">A hyphen</span></span> 
- <span data-ttu-id="a9974-761">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-761">Two digits which are check digits</span></span>

<span data-ttu-id="a9974-762">서식</span><span class="sxs-lookup"><span data-stu-id="a9974-762">Unformatted:</span></span>
- <span data-ttu-id="a9974-763">마지막 2자리 숫자가 검사 숫자인 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-763">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-764">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-764">Checksum</span></span>

<span data-ttu-id="a9974-765">예</span><span class="sxs-lookup"><span data-stu-id="a9974-765">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-766">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-766">Definition</span></span>

<span data-ttu-id="a9974-767">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-767">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-768">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-768">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-769">Keyword_brazil_cpf에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-769">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="a9974-770">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-770">The checksum passes.</span></span>

<span data-ttu-id="a9974-771">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-772">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-772">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-773">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-773">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-774">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-774">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="a9974-775">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="a9974-775">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="a9974-776">CPF</span><span class="sxs-lookup"><span data-stu-id="a9974-776">CPF</span></span>
- <span data-ttu-id="a9974-777">확인과</span><span class="sxs-lookup"><span data-stu-id="a9974-777">Identification</span></span>
- <span data-ttu-id="a9974-778">등록</span><span class="sxs-lookup"><span data-stu-id="a9974-778">Registration</span></span>
- <span data-ttu-id="a9974-779">별</span><span class="sxs-lookup"><span data-stu-id="a9974-779">Revenue</span></span>
- <span data-ttu-id="a9974-780">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="a9974-780">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="a9974-781">Imposto</span><span class="sxs-lookup"><span data-stu-id="a9974-781">Imposto</span></span> 
- <span data-ttu-id="a9974-782">Identificação</span><span class="sxs-lookup"><span data-stu-id="a9974-782">Identificação</span></span> 
- <span data-ttu-id="a9974-783">Inscrição</span><span class="sxs-lookup"><span data-stu-id="a9974-783">Inscrição</span></span> 
- <span data-ttu-id="a9974-784">고 eita</span><span class="sxs-lookup"><span data-stu-id="a9974-784">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="a9974-785">브라질 법인 번호(CNPJ)</span><span class="sxs-lookup"><span data-stu-id="a9974-785">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-786">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-786">Format</span></span>

<span data-ttu-id="a9974-787">등록 번호, 지점 번호, 검사 숫자 및 구분 기호를 포함하는 14자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-787">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-788">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-788">Pattern</span></span>
<span data-ttu-id="a9974-789">14자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="a9974-789">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="a9974-790">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-790">Two digits</span></span> 
- <span data-ttu-id="a9974-791">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-791">A period</span></span> 
- <span data-ttu-id="a9974-792">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-792">Three digits</span></span> 
- <span data-ttu-id="a9974-793">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-793">A period</span></span> 
- <span data-ttu-id="a9974-794">3자리 숫자(처음 8자리 숫자는 등록 번호임) </span><span class="sxs-lookup"><span data-stu-id="a9974-794">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="a9974-795">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="a9974-795">A forward slash</span></span> 
- <span data-ttu-id="a9974-796">4자리 지점 번호 </span><span class="sxs-lookup"><span data-stu-id="a9974-796">Four-digit branch number</span></span> 
- <span data-ttu-id="a9974-797">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-797">A hyphen</span></span> 
- <span data-ttu-id="a9974-798">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-798">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-799">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-799">Checksum</span></span>

<span data-ttu-id="a9974-800">예</span><span class="sxs-lookup"><span data-stu-id="a9974-800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-801">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-801">Definition</span></span>

<span data-ttu-id="a9974-802">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-803">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-803">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-804">Keyword_brazil_cnpj에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-804">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="a9974-805">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-805">The checksum passes.</span></span>

<span data-ttu-id="a9974-806">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-807">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-807">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-808">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-808">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-809">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-809">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="a9974-810">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="a9974-810">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="a9974-811">CNPJ</span><span class="sxs-lookup"><span data-stu-id="a9974-811">CNPJ</span></span> 
- <span data-ttu-id="a9974-812">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="a9974-812">CNPJ/MF</span></span> 
- <span data-ttu-id="a9974-813">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="a9974-813">CNPJ-MF</span></span> 
- <span data-ttu-id="a9974-814">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="a9974-814">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="a9974-815">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="a9974-815">Taxpayers Registry</span></span> 
- <span data-ttu-id="a9974-816">Legal entity</span><span class="sxs-lookup"><span data-stu-id="a9974-816">Legal entity</span></span> 
- <span data-ttu-id="a9974-817">Legal entities</span><span class="sxs-lookup"><span data-stu-id="a9974-817">Legal entities</span></span> 
- <span data-ttu-id="a9974-818">Registration Status</span><span class="sxs-lookup"><span data-stu-id="a9974-818">Registration Status</span></span> 
- <span data-ttu-id="a9974-819">비즈니스</span><span class="sxs-lookup"><span data-stu-id="a9974-819">Business</span></span> 
- <span data-ttu-id="a9974-820">Company</span><span class="sxs-lookup"><span data-stu-id="a9974-820">Company</span></span>
- <span data-ttu-id="a9974-821">CNPJ</span><span class="sxs-lookup"><span data-stu-id="a9974-821">CNPJ</span></span> 
- <span data-ttu-id="a9974-822">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="a9974-822">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="a9974-823">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="a9974-823">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="a9974-824">cgc</span><span class="sxs-lookup"><span data-stu-id="a9974-824">CGC</span></span> 
- <span data-ttu-id="a9974-825">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="a9974-825">Pessoa jurídica</span></span> 
- <span data-ttu-id="a9974-826">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="a9974-826">Pessoas jurídicas</span></span> 
- <span data-ttu-id="a9974-827">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="a9974-827">Situação cadastral</span></span> 
- <span data-ttu-id="a9974-828">Inscrição</span><span class="sxs-lookup"><span data-stu-id="a9974-828">Inscrição</span></span> 
- <span data-ttu-id="a9974-829">포털</span><span class="sxs-lookup"><span data-stu-id="a9974-829">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="a9974-830">	브라질 국가 ID 카드(RG)</span><span class="sxs-lookup"><span data-stu-id="a9974-830">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-831">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-831">Format</span></span>

<span data-ttu-id="a9974-832">Registro Geral (이전 형식): 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-832">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="a9974-833">Registro de Identidade (RIC) (새 형식): 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-833">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-834">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-834">Pattern</span></span>

<span data-ttu-id="a9974-835">Registro Geral(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="a9974-835">Registro Geral (old format):</span></span>
- <span data-ttu-id="a9974-836">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-836">Two digits</span></span> 
- <span data-ttu-id="a9974-837">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-837">A period</span></span> 
- <span data-ttu-id="a9974-838">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-838">Three digits</span></span> 
- <span data-ttu-id="a9974-839">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-839">A period</span></span> 
- <span data-ttu-id="a9974-840">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-840">Three digits</span></span> 
- <span data-ttu-id="a9974-841">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-841">A hyphen</span></span> 
- <span data-ttu-id="a9974-842">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-842">One digit which is a check digit</span></span>

<span data-ttu-id="a9974-843">Registro de Identidade (RIC) (새 형식):</span><span class="sxs-lookup"><span data-stu-id="a9974-843">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="a9974-844">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-844">10 digits</span></span> 
- <span data-ttu-id="a9974-845">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-845">A hyphen</span></span> 
- <span data-ttu-id="a9974-846">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-846">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-847">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-847">Checksum</span></span>

<span data-ttu-id="a9974-848">예</span><span class="sxs-lookup"><span data-stu-id="a9974-848">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-849">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-849">Definition</span></span>

<span data-ttu-id="a9974-850">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-850">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-851">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-851">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-852">Keyword_brazil_rg에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-852">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="a9974-853">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-853">The checksum passes.</span></span>

<span data-ttu-id="a9974-854">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-854">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-855">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-855">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-856">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-857">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-857">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="a9974-858">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="a9974-858">Keyword_brazil_rg</span></span>

<span data-ttu-id="a9974-859">Cédula de identidade identity card 국립 id número de rregistro registro de Iidentidade registro geral RG (이 키워드는 대/소문자를 구분 함) RIC (이 키워드는 대/소문자를 구분 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-859">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="a9974-860">캐나다 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-860">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-861">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-861">Format</span></span>

<span data-ttu-id="a9974-862">7 또는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-862">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-863">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-863">Pattern</span></span>

<span data-ttu-id="a9974-864">캐나다 은행 계좌 번호는 7 또는 12자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-864">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="a9974-865">캐나다 은행 계좌 송금 번호:</span><span class="sxs-lookup"><span data-stu-id="a9974-865">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="a9974-866">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-866">Five digits</span></span> 
- <span data-ttu-id="a9974-867">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-867">A hyphen</span></span> 
- <span data-ttu-id="a9974-868">3 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="a9974-868">Three digits OR</span></span>
- <span data-ttu-id="a9974-869">"0"</span><span class="sxs-lookup"><span data-stu-id="a9974-869">A zero "0"</span></span> 
- <span data-ttu-id="a9974-870">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-870">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-871">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-871">Checksum</span></span>

<span data-ttu-id="a9974-872">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-872">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-873">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-873">Definition</span></span>

<span data-ttu-id="a9974-874">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-874">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-875">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-875">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-876">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-876">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="a9974-877">Regex_canada_bank_account_transit_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-877">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="a9974-878">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-878">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-879">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-879">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-880">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-880">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-881">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-881">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="a9974-882">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="a9974-882">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="a9974-883">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="a9974-883">canada savings bonds</span></span>
- <span data-ttu-id="a9974-884">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="a9974-884">canada revenue agency</span></span>
- <span data-ttu-id="a9974-885">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="a9974-885">canadian financial institution</span></span>
- <span data-ttu-id="a9974-886">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="a9974-886">direct deposit form</span></span>
- <span data-ttu-id="a9974-887">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="a9974-887">canadian citizen</span></span>
- <span data-ttu-id="a9974-888">legal representative</span><span class="sxs-lookup"><span data-stu-id="a9974-888">legal representative</span></span>
- <span data-ttu-id="a9974-889">notary public</span><span class="sxs-lookup"><span data-stu-id="a9974-889">notary public</span></span>
- <span data-ttu-id="a9974-890">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="a9974-890">commissioner for oaths</span></span>
- <span data-ttu-id="a9974-891">child care benefit</span><span class="sxs-lookup"><span data-stu-id="a9974-891">child care benefit</span></span>
- <span data-ttu-id="a9974-892">universal child care</span><span class="sxs-lookup"><span data-stu-id="a9974-892">universal child care</span></span>
- <span data-ttu-id="a9974-893">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="a9974-893">canada child tax benefit</span></span>
- <span data-ttu-id="a9974-894">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="a9974-894">income tax benefit</span></span>
- <span data-ttu-id="a9974-895">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="a9974-895">harmonized sales tax</span></span>
- <span data-ttu-id="a9974-896">social insurance number</span><span class="sxs-lookup"><span data-stu-id="a9974-896">social insurance number</span></span>
- <span data-ttu-id="a9974-897">income tax refund</span><span class="sxs-lookup"><span data-stu-id="a9974-897">income tax refund</span></span>
- <span data-ttu-id="a9974-898">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="a9974-898">child tax benefit</span></span>
- <span data-ttu-id="a9974-899">territorial payments</span><span class="sxs-lookup"><span data-stu-id="a9974-899">territorial payments</span></span>
- <span data-ttu-id="a9974-900">institution number</span><span class="sxs-lookup"><span data-stu-id="a9974-900">institution number</span></span>
- <span data-ttu-id="a9974-901">deposit request</span><span class="sxs-lookup"><span data-stu-id="a9974-901">deposit request</span></span>
- <span data-ttu-id="a9974-902">banking information</span><span class="sxs-lookup"><span data-stu-id="a9974-902">banking information</span></span>
- <span data-ttu-id="a9974-903">direct deposit</span><span class="sxs-lookup"><span data-stu-id="a9974-903">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="a9974-904">캐나다 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-904">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-905">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-905">Format</span></span>

<span data-ttu-id="a9974-906">지역마다 다름</span><span class="sxs-lookup"><span data-stu-id="a9974-906">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-907">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-907">Pattern</span></span>

<span data-ttu-id="a9974-908">앨버타, 브리티시 콜롬비아, 매니토바, 뉴브런즈윅, 뉴펀들랜드/래브라도, 노바스코샤, 온타리오, 프린스에드워드아일랜드, 퀘벡 및 서스캐처원을 포함하는 다양한 패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-908">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-909">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-909">Checksum</span></span>

<span data-ttu-id="a9974-910">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-910">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-911">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-911">Definition</span></span>

<span data-ttu-id="a9974-912">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-913">Func_[province_name]_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-913">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-914">Keyword_[province_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-914">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="a9974-915">Keyword_canada_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-915">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-916">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-916">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="a9974-917">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="a9974-917">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="a9974-918">시/도 약어(예: AB)</span><span class="sxs-lookup"><span data-stu-id="a9974-918">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="a9974-919">시/도 이름(예: 앨버타)</span><span class="sxs-lookup"><span data-stu-id="a9974-919">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="a9974-920">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="a9974-920">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="a9974-921">DL</span><span class="sxs-lookup"><span data-stu-id="a9974-921">DL</span></span>
- <span data-ttu-id="a9974-922">된다</span><span class="sxs-lookup"><span data-stu-id="a9974-922">DLS</span></span>
- <span data-ttu-id="a9974-923">cdl</span><span class="sxs-lookup"><span data-stu-id="a9974-923">CDL</span></span>
- <span data-ttu-id="a9974-924">cdls</span><span class="sxs-lookup"><span data-stu-id="a9974-924">CDLS</span></span>
- <span data-ttu-id="a9974-925">driverlic</span><span class="sxs-lookup"><span data-stu-id="a9974-925">DriverLic</span></span>
- <span data-ttu-id="a9974-926">driverlics</span><span class="sxs-lookup"><span data-stu-id="a9974-926">DriverLics</span></span>
- <span data-ttu-id="a9974-927">driverlicense</span><span class="sxs-lookup"><span data-stu-id="a9974-927">DriverLicense</span></span>
- <span data-ttu-id="a9974-928">driverlicenses</span><span class="sxs-lookup"><span data-stu-id="a9974-928">DriverLicenses</span></span>
- <span data-ttu-id="a9974-929">driverlicence</span><span class="sxs-lookup"><span data-stu-id="a9974-929">DriverLicence</span></span>
- <span data-ttu-id="a9974-930">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="a9974-930">DriverLicences</span></span>
- <span data-ttu-id="a9974-931">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-931">Driver Lic</span></span>
- <span data-ttu-id="a9974-932">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-932">Driver Lics</span></span>
- <span data-ttu-id="a9974-933">Driver License</span><span class="sxs-lookup"><span data-stu-id="a9974-933">Driver License</span></span>
- <span data-ttu-id="a9974-934">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-934">Driver Licenses</span></span>
- <span data-ttu-id="a9974-935">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-935">Driver Licence</span></span>
- <span data-ttu-id="a9974-936">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-936">Driver Licences</span></span>
- <span data-ttu-id="a9974-937">DriversLic</span><span class="sxs-lookup"><span data-stu-id="a9974-937">DriversLic</span></span>
- <span data-ttu-id="a9974-938">driverslics</span><span class="sxs-lookup"><span data-stu-id="a9974-938">DriversLics</span></span>
- <span data-ttu-id="a9974-939">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-939">DriversLicence</span></span>
- <span data-ttu-id="a9974-940">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="a9974-940">DriversLicences</span></span>
- <span data-ttu-id="a9974-941">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-941">DriversLicense</span></span>
- <span data-ttu-id="a9974-942">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-942">DriversLicenses</span></span>
- <span data-ttu-id="a9974-943">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-943">Drivers Lic</span></span>
- <span data-ttu-id="a9974-944">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-944">Drivers Lics</span></span>
- <span data-ttu-id="a9974-945">Drivers License</span><span class="sxs-lookup"><span data-stu-id="a9974-945">Drivers License</span></span>
- <span data-ttu-id="a9974-946">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-946">Drivers Licenses</span></span>
- <span data-ttu-id="a9974-947">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-947">Drivers Licence</span></span>
- <span data-ttu-id="a9974-948">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-948">Drivers Licences</span></span>
- <span data-ttu-id="a9974-949">driver' Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-949">Driver'Lic</span></span>
- <span data-ttu-id="a9974-950">driver'lics</span><span class="sxs-lookup"><span data-stu-id="a9974-950">Driver'Lics</span></span>
- <span data-ttu-id="a9974-951">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-951">Driver'License</span></span>
- <span data-ttu-id="a9974-952">driver'licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-952">Driver'Licenses</span></span>
- <span data-ttu-id="a9974-953">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-953">Driver'Licence</span></span>
- <span data-ttu-id="a9974-954">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-954">Driver'Licences</span></span>
- <span data-ttu-id="a9974-955">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-955">Driver' Lic</span></span>
- <span data-ttu-id="a9974-956">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-956">Driver' Lics</span></span>
- <span data-ttu-id="a9974-957">Driver' License</span><span class="sxs-lookup"><span data-stu-id="a9974-957">Driver' License</span></span>
- <span data-ttu-id="a9974-958">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-958">Driver' Licenses</span></span>
- <span data-ttu-id="a9974-959">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-959">Driver' Licence</span></span>
- <span data-ttu-id="a9974-960">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-960">Driver' Licences</span></span>
- <span data-ttu-id="a9974-961">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="a9974-961">Driver'sLic</span></span>
- <span data-ttu-id="a9974-962">drivers (slics)</span><span class="sxs-lookup"><span data-stu-id="a9974-962">Driver'sLics</span></span>
- <span data-ttu-id="a9974-963">driver'slicense</span><span class="sxs-lookup"><span data-stu-id="a9974-963">Driver'sLicense</span></span>
- <span data-ttu-id="a9974-964">driver'slicenses</span><span class="sxs-lookup"><span data-stu-id="a9974-964">Driver'sLicenses</span></span>
- <span data-ttu-id="a9974-965">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="a9974-965">Driver'sLicence</span></span>
- <span data-ttu-id="a9974-966">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="a9974-966">Driver'sLicences</span></span>
- <span data-ttu-id="a9974-967">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-967">Driver's Lic</span></span>
- <span data-ttu-id="a9974-968">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-968">Driver's Lics</span></span>
- <span data-ttu-id="a9974-969">Driver's License</span><span class="sxs-lookup"><span data-stu-id="a9974-969">Driver's License</span></span>
- <span data-ttu-id="a9974-970">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-970">Driver's Licenses</span></span>
- <span data-ttu-id="a9974-971">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-971">Driver's Licence</span></span>
- <span data-ttu-id="a9974-972">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-972">Driver's Licences</span></span>
- <span data-ttu-id="a9974-973">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="a9974-973">Permis de Conduire</span></span>
- <span data-ttu-id="a9974-974">id</span><span class="sxs-lookup"><span data-stu-id="a9974-974">id</span></span>
- <span data-ttu-id="a9974-975">번호가</span><span class="sxs-lookup"><span data-stu-id="a9974-975">ids</span></span>
- <span data-ttu-id="a9974-976">idcard number</span><span class="sxs-lookup"><span data-stu-id="a9974-976">idcard number</span></span>
- <span data-ttu-id="a9974-977">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="a9974-977">idcard numbers</span></span>
- <span data-ttu-id="a9974-978">idcard #</span><span class="sxs-lookup"><span data-stu-id="a9974-978">idcard #</span></span>
- <span data-ttu-id="a9974-979">idcard #s</span><span class="sxs-lookup"><span data-stu-id="a9974-979">idcard #s</span></span>
- <span data-ttu-id="a9974-980">idcard card</span><span class="sxs-lookup"><span data-stu-id="a9974-980">idcard card</span></span>
- <span data-ttu-id="a9974-981">idcard cards</span><span class="sxs-lookup"><span data-stu-id="a9974-981">idcard cards</span></span>
- <span data-ttu-id="a9974-982">idcard</span><span class="sxs-lookup"><span data-stu-id="a9974-982">idcard</span></span>
- <span data-ttu-id="a9974-983">identification number</span><span class="sxs-lookup"><span data-stu-id="a9974-983">identification number</span></span>
- <span data-ttu-id="a9974-984">identification numbers</span><span class="sxs-lookup"><span data-stu-id="a9974-984">identification numbers</span></span>
- <span data-ttu-id="a9974-985">identification #</span><span class="sxs-lookup"><span data-stu-id="a9974-985">identification #</span></span>
- <span data-ttu-id="a9974-986">identification #s</span><span class="sxs-lookup"><span data-stu-id="a9974-986">identification #s</span></span>
- <span data-ttu-id="a9974-987">identification card</span><span class="sxs-lookup"><span data-stu-id="a9974-987">identification card</span></span>
- <span data-ttu-id="a9974-988">identification cards</span><span class="sxs-lookup"><span data-stu-id="a9974-988">identification cards</span></span>
- <span data-ttu-id="a9974-989">확인과</span><span class="sxs-lookup"><span data-stu-id="a9974-989">identification</span></span> 
- <span data-ttu-id="a9974-990">DL</span><span class="sxs-lookup"><span data-stu-id="a9974-990">DL#</span></span>
- <span data-ttu-id="a9974-991">된다</span><span class="sxs-lookup"><span data-stu-id="a9974-991">DLS#</span></span> 
- <span data-ttu-id="a9974-992">cdl #</span><span class="sxs-lookup"><span data-stu-id="a9974-992">CDL#</span></span> 
- <span data-ttu-id="a9974-993">cdls #</span><span class="sxs-lookup"><span data-stu-id="a9974-993">CDLS#</span></span> 
- <span data-ttu-id="a9974-994">driverlic #</span><span class="sxs-lookup"><span data-stu-id="a9974-994">DriverLic#</span></span> 
- <span data-ttu-id="a9974-995">driverlics #</span><span class="sxs-lookup"><span data-stu-id="a9974-995">DriverLics#</span></span> 
- <span data-ttu-id="a9974-996">driverlicense #</span><span class="sxs-lookup"><span data-stu-id="a9974-996">DriverLicense#</span></span> 
- <span data-ttu-id="a9974-997">driverlicenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-997">DriverLicenses#</span></span> 
- <span data-ttu-id="a9974-998">driverlicence #</span><span class="sxs-lookup"><span data-stu-id="a9974-998">DriverLicence#</span></span> 
- <span data-ttu-id="a9974-999">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="a9974-999">DriverLicences#</span></span> 
- <span data-ttu-id="a9974-1000">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-1000">Driver Lic#</span></span>
- <span data-ttu-id="a9974-1001">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-1001">Driver Lics#</span></span> 
- <span data-ttu-id="a9974-1002">Driver License#</span><span class="sxs-lookup"><span data-stu-id="a9974-1002">Driver License#</span></span> 
- <span data-ttu-id="a9974-1003">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-1003">Driver Licenses#</span></span> 
- <span data-ttu-id="a9974-1004">Driver License#</span><span class="sxs-lookup"><span data-stu-id="a9974-1004">Driver License#</span></span> 
- <span data-ttu-id="a9974-1005">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="a9974-1005">Driver Licences#</span></span> 
- <span data-ttu-id="a9974-1006">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="a9974-1006">DriversLic#</span></span> 
- <span data-ttu-id="a9974-1007">driverslics #</span><span class="sxs-lookup"><span data-stu-id="a9974-1007">DriversLics#</span></span> 
- <span data-ttu-id="a9974-1008">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-1008">DriversLicense#</span></span> 
- <span data-ttu-id="a9974-1009">드라이버 라이선스 수</span><span class="sxs-lookup"><span data-stu-id="a9974-1009">DriversLicenses#</span></span> 
- <span data-ttu-id="a9974-1010">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-1010">DriversLicence#</span></span> 
- <span data-ttu-id="a9974-1011">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="a9974-1011">DriversLicences#</span></span> 
- <span data-ttu-id="a9974-1012">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-1012">Drivers Lic#</span></span> 
- <span data-ttu-id="a9974-1013">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-1013">Drivers Lics#</span></span> 
- <span data-ttu-id="a9974-1014">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="a9974-1014">Drivers License#</span></span> 
- <span data-ttu-id="a9974-1015">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-1015">Drivers Licenses#</span></span> 
- <span data-ttu-id="a9974-1016">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="a9974-1016">Drivers Licence#</span></span> 
- <span data-ttu-id="a9974-1017">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="a9974-1017">Drivers Licences#</span></span> 
- <span data-ttu-id="a9974-1018">driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="a9974-1018">Driver'Lic#</span></span> 
- <span data-ttu-id="a9974-1019">driver'lics #</span><span class="sxs-lookup"><span data-stu-id="a9974-1019">Driver'Lics#</span></span> 
- <span data-ttu-id="a9974-1020">driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-1020">Driver'License#</span></span> 
- <span data-ttu-id="a9974-1021">driver'licenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-1021">Driver'Licenses#</span></span> 
- <span data-ttu-id="a9974-1022">driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-1022">Driver'Licence#</span></span> 
- <span data-ttu-id="a9974-1023">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="a9974-1023">Driver'Licences#</span></span> 
- <span data-ttu-id="a9974-1024">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-1024">Driver' Lic#</span></span> 
- <span data-ttu-id="a9974-1025">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-1025">Driver' Lics#</span></span> 
- <span data-ttu-id="a9974-1026">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="a9974-1026">Driver' License#</span></span> 
- <span data-ttu-id="a9974-1027">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-1027">Driver' Licenses#</span></span> 
- <span data-ttu-id="a9974-1028">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="a9974-1028">Driver' Licence#</span></span> 
- <span data-ttu-id="a9974-1029">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="a9974-1029">Driver' Licences#</span></span> 
- <span data-ttu-id="a9974-1030">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="a9974-1030">Driver'sLic#</span></span> 
- <span data-ttu-id="a9974-1031">drivers (slics #)</span><span class="sxs-lookup"><span data-stu-id="a9974-1031">Driver'sLics#</span></span> 
- <span data-ttu-id="a9974-1032">driver'slicense #</span><span class="sxs-lookup"><span data-stu-id="a9974-1032">Driver'sLicense#</span></span> 
- <span data-ttu-id="a9974-1033">driver'slicenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-1033">Driver'sLicenses#</span></span> 
- <span data-ttu-id="a9974-1034">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="a9974-1034">Driver'sLicence#</span></span> 
- <span data-ttu-id="a9974-1035">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="a9974-1035">Driver'sLicences#</span></span> 
- <span data-ttu-id="a9974-1036">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-1036">Driver's Lic#</span></span> 
- <span data-ttu-id="a9974-1037">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-1037">Driver's Lics#</span></span> 
- <span data-ttu-id="a9974-1038">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="a9974-1038">Driver's License#</span></span> 
- <span data-ttu-id="a9974-1039">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-1039">Driver's Licenses#</span></span> 
- <span data-ttu-id="a9974-1040">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="a9974-1040">Driver's Licence#</span></span> 
- <span data-ttu-id="a9974-1041">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="a9974-1041">Driver's Licences#</span></span> 
- <span data-ttu-id="a9974-1042">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="a9974-1042">Permis de Conduire#</span></span> 
- <span data-ttu-id="a9974-1043">i</span><span class="sxs-lookup"><span data-stu-id="a9974-1043">id#</span></span> 
- <span data-ttu-id="a9974-1044">번호가</span><span class="sxs-lookup"><span data-stu-id="a9974-1044">ids#</span></span> 
- <span data-ttu-id="a9974-1045">idcard card#</span><span class="sxs-lookup"><span data-stu-id="a9974-1045">idcard card#</span></span> 
- <span data-ttu-id="a9974-1046">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="a9974-1046">idcard cards#</span></span> 
- <span data-ttu-id="a9974-1047">idcard #</span><span class="sxs-lookup"><span data-stu-id="a9974-1047">idcard#</span></span> 
- <span data-ttu-id="a9974-1048">identification card#</span><span class="sxs-lookup"><span data-stu-id="a9974-1048">identification card#</span></span> 
- <span data-ttu-id="a9974-1049">identification cards#</span><span class="sxs-lookup"><span data-stu-id="a9974-1049">identification cards#</span></span> 
- <span data-ttu-id="a9974-1050">확인과</span><span class="sxs-lookup"><span data-stu-id="a9974-1050">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="a9974-1051">캐나다 건강 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1051">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1052">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1052">Format</span></span>

<span data-ttu-id="a9974-1053">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1053">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1054">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1054">Pattern</span></span>

<span data-ttu-id="a9974-1055">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1055">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1056">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1056">Checksum</span></span>

<span data-ttu-id="a9974-1057">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-1057">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1058">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1058">Definition</span></span>

<span data-ttu-id="a9974-1059">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1059">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1060">Regex_canada_health_service_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1060">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1061">Keyword_canada_health_service_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1061">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1062">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1062">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="a9974-1063">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="a9974-1063">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="a9974-1064">personal health number</span><span class="sxs-lookup"><span data-stu-id="a9974-1064">personal health number</span></span>
- <span data-ttu-id="a9974-1065">patient information</span><span class="sxs-lookup"><span data-stu-id="a9974-1065">patient information</span></span>
- <span data-ttu-id="a9974-1066">health services</span><span class="sxs-lookup"><span data-stu-id="a9974-1066">health services</span></span>
- <span data-ttu-id="a9974-1067">speciality services</span><span class="sxs-lookup"><span data-stu-id="a9974-1067">speciality services</span></span>
- <span data-ttu-id="a9974-1068">automobile accident</span><span class="sxs-lookup"><span data-stu-id="a9974-1068">automobile accident</span></span>
- <span data-ttu-id="a9974-1069">patient hospital</span><span class="sxs-lookup"><span data-stu-id="a9974-1069">patient hospital</span></span>
- <span data-ttu-id="a9974-1070">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="a9974-1070">psychiatrist</span></span>
- <span data-ttu-id="a9974-1071">workers compensation</span><span class="sxs-lookup"><span data-stu-id="a9974-1071">workers compensation</span></span>
- <span data-ttu-id="a9974-1072">종류</span><span class="sxs-lookup"><span data-stu-id="a9974-1072">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="a9974-1073">캐나다 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1073">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1074">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1074">Format</span></span>

<span data-ttu-id="a9974-1075">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1075">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1076">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1076">Pattern</span></span>

<span data-ttu-id="a9974-1077">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1077">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1078">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1078">Checksum</span></span>

<span data-ttu-id="a9974-1079">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-1079">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1080">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1080">Definition</span></span>

<span data-ttu-id="a9974-1081">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1081">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1082">Regex_canada_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1082">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1083">Keyword_canada_passport_number 또는 Keyword_passport의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1083">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1084">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1084">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="a9974-1085">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="a9974-1085">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="a9974-1086">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="a9974-1086">canadian citizenship</span></span>
- <span data-ttu-id="a9974-1087">canadian passport</span><span class="sxs-lookup"><span data-stu-id="a9974-1087">canadian passport</span></span>
- <span data-ttu-id="a9974-1088">passport application</span><span class="sxs-lookup"><span data-stu-id="a9974-1088">passport application</span></span>
- <span data-ttu-id="a9974-1089">passport photos</span><span class="sxs-lookup"><span data-stu-id="a9974-1089">passport photos</span></span>
- <span data-ttu-id="a9974-1090">certified translator</span><span class="sxs-lookup"><span data-stu-id="a9974-1090">certified translator</span></span>
- <span data-ttu-id="a9974-1091">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="a9974-1091">canadian citizens</span></span>
- <span data-ttu-id="a9974-1092">processing times</span><span class="sxs-lookup"><span data-stu-id="a9974-1092">processing times</span></span>
- <span data-ttu-id="a9974-1093">renewal application</span><span class="sxs-lookup"><span data-stu-id="a9974-1093">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="a9974-1094">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-1094">Keyword_passport</span></span>

- <span data-ttu-id="a9974-1095">Passport Number</span><span class="sxs-lookup"><span data-stu-id="a9974-1095">Passport Number</span></span>
- <span data-ttu-id="a9974-1096">Passport No</span><span class="sxs-lookup"><span data-stu-id="a9974-1096">Passport No</span></span>
- <span data-ttu-id="a9974-1097">Passport #</span><span class="sxs-lookup"><span data-stu-id="a9974-1097">Passport #</span></span>
- <span data-ttu-id="a9974-1098">여권</span><span class="sxs-lookup"><span data-stu-id="a9974-1098">Passport#</span></span>
- <span data-ttu-id="a9974-1099">PassportID</span><span class="sxs-lookup"><span data-stu-id="a9974-1099">PassportID</span></span>
- <span data-ttu-id="a9974-1100">Passportno</span><span class="sxs-lookup"><span data-stu-id="a9974-1100">Passportno</span></span>
- <span data-ttu-id="a9974-1101">passportnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-1101">passportnumber</span></span>
- <span data-ttu-id="a9974-1102">パスポート</span><span class="sxs-lookup"><span data-stu-id="a9974-1102">パスポート</span></span>
- <span data-ttu-id="a9974-1103">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="a9974-1103">パスポート番号</span></span>
- <span data-ttu-id="a9974-1104">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="a9974-1104">パスポートのNum</span></span>
- <span data-ttu-id="a9974-1105">パスポート #</span><span class="sxs-lookup"><span data-stu-id="a9974-1105">パスポート＃</span></span>
- <span data-ttu-id="a9974-1106">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a9974-1106">Numéro de passeport</span></span>
- <span data-ttu-id="a9974-1107">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="a9974-1107">Passeport n °</span></span>
- <span data-ttu-id="a9974-1108">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="a9974-1108">Passeport Non</span></span>
- <span data-ttu-id="a9974-1109">Passeport #</span><span class="sxs-lookup"><span data-stu-id="a9974-1109">Passeport #</span></span>
- <span data-ttu-id="a9974-1110">포트 #</span><span class="sxs-lookup"><span data-stu-id="a9974-1110">Passeport#</span></span>
- <span data-ttu-id="a9974-1111">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="a9974-1111">PasseportNon</span></span>
- <span data-ttu-id="a9974-1112">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="a9974-1112">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="a9974-1113">캐나다 PHIN(개인 건강 식별 번호)</span><span class="sxs-lookup"><span data-stu-id="a9974-1113">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1114">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1114">Format</span></span>

<span data-ttu-id="a9974-1115">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1115">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1116">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1116">Pattern</span></span>

<span data-ttu-id="a9974-1117">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1117">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1118">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1118">Checksum</span></span>

<span data-ttu-id="a9974-1119">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-1119">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1120">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1120">Definition</span></span>

<span data-ttu-id="a9974-1121">DLP 정책은 300 문자 (예: Regex_canada_phin)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="a9974-1122">Keyword_canada_phin 또는 Keyword_canada_provinces의 키워드를 두 개 이상 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1122">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1123">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1123">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="a9974-1124">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="a9974-1124">Keyword_canada_phin</span></span>

- <span data-ttu-id="a9974-1125">social insurance number</span><span class="sxs-lookup"><span data-stu-id="a9974-1125">social insurance number</span></span>
- <span data-ttu-id="a9974-1126">health information act</span><span class="sxs-lookup"><span data-stu-id="a9974-1126">health information act</span></span>
- <span data-ttu-id="a9974-1127">income tax information</span><span class="sxs-lookup"><span data-stu-id="a9974-1127">income tax information</span></span>
- <span data-ttu-id="a9974-1128">manitoba health</span><span class="sxs-lookup"><span data-stu-id="a9974-1128">manitoba health</span></span>
- <span data-ttu-id="a9974-1129">health registration</span><span class="sxs-lookup"><span data-stu-id="a9974-1129">health registration</span></span>
- <span data-ttu-id="a9974-1130">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="a9974-1130">prescription purchases</span></span>
- <span data-ttu-id="a9974-1131">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="a9974-1131">benefit eligibility</span></span>
- <span data-ttu-id="a9974-1132">personal health</span><span class="sxs-lookup"><span data-stu-id="a9974-1132">personal health</span></span>
- <span data-ttu-id="a9974-1133">power of attorney</span><span class="sxs-lookup"><span data-stu-id="a9974-1133">power of attorney</span></span>
- <span data-ttu-id="a9974-1134">registration number</span><span class="sxs-lookup"><span data-stu-id="a9974-1134">registration number</span></span>
- <span data-ttu-id="a9974-1135">personal health number</span><span class="sxs-lookup"><span data-stu-id="a9974-1135">personal health number</span></span>
- <span data-ttu-id="a9974-1136">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="a9974-1136">practitioner referral</span></span>
- <span data-ttu-id="a9974-1137">wellness professional</span><span class="sxs-lookup"><span data-stu-id="a9974-1137">wellness professional</span></span>
- <span data-ttu-id="a9974-1138">patient referral</span><span class="sxs-lookup"><span data-stu-id="a9974-1138">patient referral</span></span>
- <span data-ttu-id="a9974-1139">health and wellness</span><span class="sxs-lookup"><span data-stu-id="a9974-1139">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="a9974-1140">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="a9974-1140">Keyword_canada_provinces</span></span>

- <span data-ttu-id="a9974-1141">Nunavut</span><span class="sxs-lookup"><span data-stu-id="a9974-1141">Nunavut</span></span>
- <span data-ttu-id="a9974-1142">퀘벡</span><span class="sxs-lookup"><span data-stu-id="a9974-1142">Quebec</span></span>
- <span data-ttu-id="a9974-1143">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="a9974-1143">Northwest Territories</span></span>
- <span data-ttu-id="a9974-1144">온타리오</span><span class="sxs-lookup"><span data-stu-id="a9974-1144">Ontario</span></span>
- <span data-ttu-id="a9974-1145">British Columbia</span><span class="sxs-lookup"><span data-stu-id="a9974-1145">British Columbia</span></span>
- <span data-ttu-id="a9974-1146">앨버타</span><span class="sxs-lookup"><span data-stu-id="a9974-1146">Alberta</span></span>
- <span data-ttu-id="a9974-1147">서스캐처원</span><span class="sxs-lookup"><span data-stu-id="a9974-1147">Saskatchewan</span></span>
- <span data-ttu-id="a9974-1148">매니토바</span><span class="sxs-lookup"><span data-stu-id="a9974-1148">Manitoba</span></span>
- <span data-ttu-id="a9974-1149">Yukon</span><span class="sxs-lookup"><span data-stu-id="a9974-1149">Yukon</span></span>
- <span data-ttu-id="a9974-1150">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="a9974-1150">Newfoundland and Labrador</span></span>
- <span data-ttu-id="a9974-1151">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="a9974-1151">New Brunswick</span></span>
- <span data-ttu-id="a9974-1152">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="a9974-1152">Nova Scotia</span></span>
- <span data-ttu-id="a9974-1153">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="a9974-1153">Prince Edward Island</span></span>
- <span data-ttu-id="a9974-1154">캐나다</span><span class="sxs-lookup"><span data-stu-id="a9974-1154">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="a9974-1155">캐나다 사회 보험 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1155">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1156">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1156">Format</span></span>

<span data-ttu-id="a9974-1157">선택적 하이픈 또는 공백을 포함하는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1157">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1158">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1158">Pattern</span></span>

<span data-ttu-id="a9974-1159">서식이</span><span class="sxs-lookup"><span data-stu-id="a9974-1159">Formatted:</span></span>
- <span data-ttu-id="a9974-1160">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1160">Three digits</span></span> 
- <span data-ttu-id="a9974-1161">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="a9974-1161">A hyphen or space</span></span> 
- <span data-ttu-id="a9974-1162">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1162">Three digits</span></span> 
- <span data-ttu-id="a9974-1163">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="a9974-1163">A hyphen or space</span></span> 
- <span data-ttu-id="a9974-1164">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1164">Three digits</span></span>

<span data-ttu-id="a9974-1165">서식 없음: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1165">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1166">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1166">Checksum</span></span>

<span data-ttu-id="a9974-1167">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1167">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1168">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1168">Definition</span></span>

<span data-ttu-id="a9974-1169">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1169">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1170">Func_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1170">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1171">2개 이상의 다음 항목 조합:</span><span class="sxs-lookup"><span data-stu-id="a9974-1171">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="a9974-1172">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1172">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="a9974-1173">Keyword_sin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1173">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="a9974-1174">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1174">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="a9974-1175">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1175">The checksum passes.</span></span>

<span data-ttu-id="a9974-1176">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1177">Func_unformatted_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1177">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1178">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1178">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="a9974-1179">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1179">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1180">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1180">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="a9974-1181">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="a9974-1181">Keyword_sin</span></span>

- <span data-ttu-id="a9974-1182">sin</span><span class="sxs-lookup"><span data-stu-id="a9974-1182">sin</span></span> 
- <span data-ttu-id="a9974-1183">social insurance</span><span class="sxs-lookup"><span data-stu-id="a9974-1183">social insurance</span></span> 
- <span data-ttu-id="a9974-1184">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="a9974-1184">numero d'assurance sociale</span></span> 
- <span data-ttu-id="a9974-1185">죄</span><span class="sxs-lookup"><span data-stu-id="a9974-1185">sins</span></span> 
- <span data-ttu-id="a9974-1186">ssn</span><span class="sxs-lookup"><span data-stu-id="a9974-1186">ssn</span></span> 
- <span data-ttu-id="a9974-1187">있는 ssn</span><span class="sxs-lookup"><span data-stu-id="a9974-1187">ssns</span></span> 
- <span data-ttu-id="a9974-1188">social security</span><span class="sxs-lookup"><span data-stu-id="a9974-1188">social security</span></span> 
- <span data-ttu-id="a9974-1189">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="a9974-1189">numero d'assurance social</span></span> 
- <span data-ttu-id="a9974-1190">national identification number</span><span class="sxs-lookup"><span data-stu-id="a9974-1190">national identification number</span></span> 
- <span data-ttu-id="a9974-1191">national id</span><span class="sxs-lookup"><span data-stu-id="a9974-1191">national id</span></span> 
- <span data-ttu-id="a9974-1192">sin</span><span class="sxs-lookup"><span data-stu-id="a9974-1192">sin#</span></span> 
- <span data-ttu-id="a9974-1193">soc ins</span><span class="sxs-lookup"><span data-stu-id="a9974-1193">soc ins</span></span> 
- <span data-ttu-id="a9974-1194">social ins</span><span class="sxs-lookup"><span data-stu-id="a9974-1194">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="a9974-1195">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="a9974-1195">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="a9974-1196">driver's license</span><span class="sxs-lookup"><span data-stu-id="a9974-1196">driver's license</span></span> 
- <span data-ttu-id="a9974-1197">drivers license</span><span class="sxs-lookup"><span data-stu-id="a9974-1197">drivers license</span></span> 
- <span data-ttu-id="a9974-1198">driver's licence</span><span class="sxs-lookup"><span data-stu-id="a9974-1198">driver's licence</span></span> 
- <span data-ttu-id="a9974-1199">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a9974-1199">drivers licence</span></span> 
- <span data-ttu-id="a9974-1200">dob</span><span class="sxs-lookup"><span data-stu-id="a9974-1200">DOB</span></span> 
- <span data-ttu-id="a9974-1201">생년월일</span><span class="sxs-lookup"><span data-stu-id="a9974-1201">Birthdate</span></span> 
- <span data-ttu-id="a9974-1202">생일</span><span class="sxs-lookup"><span data-stu-id="a9974-1202">Birthday</span></span> 
- <span data-ttu-id="a9974-1203">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="a9974-1203">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="a9974-1204">	칠레 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1204">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1205">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1205">Format</span></span>

<span data-ttu-id="a9974-1206">7-8 자리 숫자와 구분 기호 확인 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-1206">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1207">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1207">Pattern</span></span>

<span data-ttu-id="a9974-1208">7-8자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="a9974-1208">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="a9974-1209">1-2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1209">1-2 digits</span></span> 
- <span data-ttu-id="a9974-1210">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-1210">A period</span></span> 
- <span data-ttu-id="a9974-1211">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1211">Three digits</span></span> 
- <span data-ttu-id="a9974-1212">마침표 </span><span class="sxs-lookup"><span data-stu-id="a9974-1212">A period</span></span> 
- <span data-ttu-id="a9974-1213">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1213">Three digits</span></span> 
- <span data-ttu-id="a9974-1214">대시 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-1214">A dash</span></span> 
- <span data-ttu-id="a9974-1215">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-1215">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1216">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1216">Checksum</span></span>

<span data-ttu-id="a9974-1217">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1217">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1218">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1218">Definition</span></span>

<span data-ttu-id="a9974-1219">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1219">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1220">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1220">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1221">Keyword_chile_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1221">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="a9974-1222">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1222">The checksum passes.</span></span>

<span data-ttu-id="a9974-1223">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1224">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1224">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1225">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1225">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1226">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1226">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="a9974-1227">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="a9974-1227">Keyword_chile_id_card</span></span>

- <span data-ttu-id="a9974-1228">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="a9974-1228">National Identification Number</span></span> 
- <span data-ttu-id="a9974-1229">Identity card</span><span class="sxs-lookup"><span data-stu-id="a9974-1229">Identity card</span></span> 
- <span data-ttu-id="a9974-1230">ID</span><span class="sxs-lookup"><span data-stu-id="a9974-1230">ID</span></span> 
- <span data-ttu-id="a9974-1231">확인과</span><span class="sxs-lookup"><span data-stu-id="a9974-1231">Identification</span></span> 
- <span data-ttu-id="a9974-1232">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="a9974-1232">Rol Único Nacional</span></span> 
- <span data-ttu-id="a9974-1233">실행</span><span class="sxs-lookup"><span data-stu-id="a9974-1233">RUN</span></span> 
- <span data-ttu-id="a9974-1234">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="a9974-1234">Rol Único Tributario</span></span> 
- <span data-ttu-id="a9974-1235">RUT</span><span class="sxs-lookup"><span data-stu-id="a9974-1235">RUT</span></span> 
- <span data-ttu-id="a9974-1236">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="a9974-1236">Cédula de Identidad</span></span> 
- <span data-ttu-id="a9974-1237">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="a9974-1237">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="a9974-1238">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="a9974-1238">Tarjeta de identificación</span></span> 
- <span data-ttu-id="a9974-1239">Identificación</span><span class="sxs-lookup"><span data-stu-id="a9974-1239">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="a9974-1240">	중국 주민 ID 카드(PRC) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1240">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1241">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1241">Format</span></span>

<span data-ttu-id="a9974-1242">18자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1242">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1243">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1243">Pattern</span></span>

<span data-ttu-id="a9974-1244">18자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-1244">18 digits:</span></span>
- <span data-ttu-id="a9974-1245">주소 코드에 해당하는 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-1245">Six digits which are an address code</span></span> 
- <span data-ttu-id="a9974-1246">생년월일에 해당하는 YYYYMMDD 형식의 8자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-1246">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="a9974-1247">주문 코드에 해당하는 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-1247">Three digits which are an order code</span></span> 
- <span data-ttu-id="a9974-1248">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1248">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1249">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1249">Checksum</span></span>

<span data-ttu-id="a9974-1250">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1250">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1251">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1251">Definition</span></span>

<span data-ttu-id="a9974-1252">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1252">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1253">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1253">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1254">Keyword_china_resident_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1254">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="a9974-1255">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1255">The checksum passes.</span></span>

<span data-ttu-id="a9974-1256">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1256">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1257">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1257">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1258">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1258">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1259">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1259">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="a9974-1260">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="a9974-1260">Keyword_china_resident_id</span></span>

- <span data-ttu-id="a9974-1261">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="a9974-1261">Resident Identity Card</span></span> 
- <span data-ttu-id="a9974-1262">중국</span><span class="sxs-lookup"><span data-stu-id="a9974-1262">PRC</span></span> 
- <span data-ttu-id="a9974-1263">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="a9974-1263">National Identification Card</span></span> 
- <span data-ttu-id="a9974-1264">身份证</span><span class="sxs-lookup"><span data-stu-id="a9974-1264">身份证</span></span> 
- <span data-ttu-id="a9974-1265">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="a9974-1265">居民 身份证</span></span> 
- <span data-ttu-id="a9974-1266">居民身份证</span><span class="sxs-lookup"><span data-stu-id="a9974-1266">居民身份证</span></span> 
- <span data-ttu-id="a9974-1267">鉴定</span><span class="sxs-lookup"><span data-stu-id="a9974-1267">鉴定</span></span> 
- <span data-ttu-id="a9974-1268">身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-1268">身分證</span></span> 
- <span data-ttu-id="a9974-1269">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-1269">居民 身份證</span></span>
- <span data-ttu-id="a9974-1270">鑑定</span><span class="sxs-lookup"><span data-stu-id="a9974-1270">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="a9974-1271">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1271">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1272">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1272">Format</span></span>

<span data-ttu-id="a9974-1273">서식이 있거나 서식이 없을 수 있는 16 자리 (dddddddddddddddd), Luhn 테스트를 통과 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1273">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1274">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1274">Pattern</span></span>

<span data-ttu-id="a9974-1275">Visa, MasterCard, Discover Card, JCB, American Express, 상품권 및 식사권을 비롯하여 전 세계 모든 주요 브랜드 카드를 검색하는 매우 복잡하고 강력한 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1275">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1276">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1276">Checksum</span></span>

<span data-ttu-id="a9974-1277">있음(Luhn 체크섬)</span><span class="sxs-lookup"><span data-stu-id="a9974-1277">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1278">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1278">Definition</span></span>

<span data-ttu-id="a9974-1279">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1279">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1280">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1280">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1281">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1281">One of the following is true:</span></span>
    - <span data-ttu-id="a9974-1282">Keyword_cc_verification의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1282">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="a9974-1283">Keyword_cc_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1283">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="a9974-1284">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1284">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="a9974-1285">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1285">The checksum passes.</span></span>

<span data-ttu-id="a9974-1286">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1286">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1287">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1287">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1288">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1288">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1289">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1289">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="a9974-1290">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="a9974-1290">Keyword_cc_verification</span></span>

- <span data-ttu-id="a9974-1291">card verification</span><span class="sxs-lookup"><span data-stu-id="a9974-1291">card verification</span></span>
- <span data-ttu-id="a9974-1292">card identification number</span><span class="sxs-lookup"><span data-stu-id="a9974-1292">card identification number</span></span>
- <span data-ttu-id="a9974-1293">cvn</span><span class="sxs-lookup"><span data-stu-id="a9974-1293">cvn</span></span>
- <span data-ttu-id="a9974-1294">cid</span><span class="sxs-lookup"><span data-stu-id="a9974-1294">cid</span></span>
- <span data-ttu-id="a9974-1295">cvc2</span><span class="sxs-lookup"><span data-stu-id="a9974-1295">cvc2</span></span>
- <span data-ttu-id="a9974-1296">cvv2</span><span class="sxs-lookup"><span data-stu-id="a9974-1296">cvv2</span></span>
- <span data-ttu-id="a9974-1297">pin block</span><span class="sxs-lookup"><span data-stu-id="a9974-1297">pin block</span></span>
- <span data-ttu-id="a9974-1298">security code</span><span class="sxs-lookup"><span data-stu-id="a9974-1298">security code</span></span>
- <span data-ttu-id="a9974-1299">security number</span><span class="sxs-lookup"><span data-stu-id="a9974-1299">security number</span></span>
- <span data-ttu-id="a9974-1300">security no</span><span class="sxs-lookup"><span data-stu-id="a9974-1300">security no</span></span>
- <span data-ttu-id="a9974-1301">issue number</span><span class="sxs-lookup"><span data-stu-id="a9974-1301">issue number</span></span>
- <span data-ttu-id="a9974-1302">issue no</span><span class="sxs-lookup"><span data-stu-id="a9974-1302">issue no</span></span>
- <span data-ttu-id="a9974-1303">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="a9974-1303">cryptogramme</span></span>
- <span data-ttu-id="a9974-1304">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="a9974-1304">numéro de sécurité</span></span>
- <span data-ttu-id="a9974-1305">numero de securite</span><span class="sxs-lookup"><span data-stu-id="a9974-1305">numero de securite</span></span>
- <span data-ttu-id="a9974-1306">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1306">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="a9974-1307">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1307">kreditkartenprufnummer</span></span>
- <span data-ttu-id="a9974-1308">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="a9974-1308">prüfziffer</span></span>
- <span data-ttu-id="a9974-1309">prufziffer</span><span class="sxs-lookup"><span data-stu-id="a9974-1309">prufziffer</span></span>
- <span data-ttu-id="a9974-1310">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="a9974-1310">sicherheits Kode</span></span>
- <span data-ttu-id="a9974-1311">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="a9974-1311">sicherheitscode</span></span>
- <span data-ttu-id="a9974-1312">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1312">sicherheitsnummer</span></span>
- <span data-ttu-id="a9974-1313">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="a9974-1313">verfalldatum</span></span>
- <span data-ttu-id="a9974-1314">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="a9974-1314">codice di verifica</span></span>
- <span data-ttu-id="a9974-1315">cod.</span><span class="sxs-lookup"><span data-stu-id="a9974-1315">cod.</span></span> <span data-ttu-id="a9974-1316">sicurezza</span><span class="sxs-lookup"><span data-stu-id="a9974-1316">sicurezza</span></span>
- <span data-ttu-id="a9974-1317">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="a9974-1317">cod sicurezza</span></span>
- <span data-ttu-id="a9974-1318">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a9974-1318">n autorizzazione</span></span>
- <span data-ttu-id="a9974-1319">código</span><span class="sxs-lookup"><span data-stu-id="a9974-1319">código</span></span>
- <span data-ttu-id="a9974-1320">codigo</span><span class="sxs-lookup"><span data-stu-id="a9974-1320">codigo</span></span>
- <span data-ttu-id="a9974-1321">cod.</span><span class="sxs-lookup"><span data-stu-id="a9974-1321">cod.</span></span> <span data-ttu-id="a9974-1322">seg</span><span class="sxs-lookup"><span data-stu-id="a9974-1322">seg</span></span>
- <span data-ttu-id="a9974-1323">cod seg</span><span class="sxs-lookup"><span data-stu-id="a9974-1323">cod seg</span></span>
- <span data-ttu-id="a9974-1324">código de segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1324">código de segurança</span></span>
- <span data-ttu-id="a9974-1325">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1325">codigo de seguranca</span></span>
- <span data-ttu-id="a9974-1326">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1326">codigo de segurança</span></span>
- <span data-ttu-id="a9974-1327">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1327">código de seguranca</span></span>
- <span data-ttu-id="a9974-1328">cód</span><span class="sxs-lookup"><span data-stu-id="a9974-1328">cód.</span></span> <span data-ttu-id="a9974-1329">segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1329">segurança</span></span>
- <span data-ttu-id="a9974-1330">cod.</span><span class="sxs-lookup"><span data-stu-id="a9974-1330">cod.</span></span> <span data-ttu-id="a9974-1331">seguranca cod</span><span class="sxs-lookup"><span data-stu-id="a9974-1331">seguranca cod.</span></span> <span data-ttu-id="a9974-1332">segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1332">segurança</span></span>
- <span data-ttu-id="a9974-1333">cód</span><span class="sxs-lookup"><span data-stu-id="a9974-1333">cód.</span></span> <span data-ttu-id="a9974-1334">seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1334">seguranca</span></span>
- <span data-ttu-id="a9974-1335">cód segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1335">cód segurança</span></span>
- <span data-ttu-id="a9974-1336">cod seguranca cod segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1336">cod seguranca cod segurança</span></span>
- <span data-ttu-id="a9974-1337">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1337">cód seguranca</span></span>
- <span data-ttu-id="a9974-1338">número de verificação</span><span class="sxs-lookup"><span data-stu-id="a9974-1338">número de verificação</span></span>
- <span data-ttu-id="a9974-1339">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="a9974-1339">numero de verificacao</span></span>
- <span data-ttu-id="a9974-1340">ablauf</span><span class="sxs-lookup"><span data-stu-id="a9974-1340">ablauf</span></span>
- <span data-ttu-id="a9974-1341">gültig bis</span><span class="sxs-lookup"><span data-stu-id="a9974-1341">gültig bis</span></span>
- <span data-ttu-id="a9974-1342">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="a9974-1342">gültigkeitsdatum</span></span>
- <span data-ttu-id="a9974-1343">gultig bis</span><span class="sxs-lookup"><span data-stu-id="a9974-1343">gultig bis</span></span>
- <span data-ttu-id="a9974-1344">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="a9974-1344">gultigkeitsdatum</span></span>
- <span data-ttu-id="a9974-1345">scadenza</span><span class="sxs-lookup"><span data-stu-id="a9974-1345">scadenza</span></span>
- <span data-ttu-id="a9974-1346">data scad</span><span class="sxs-lookup"><span data-stu-id="a9974-1346">data scad</span></span>
- <span data-ttu-id="a9974-1347">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="a9974-1347">fecha de expiracion</span></span>
- <span data-ttu-id="a9974-1348">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="a9974-1348">fecha de venc</span></span>
- <span data-ttu-id="a9974-1349">vencimiento</span><span class="sxs-lookup"><span data-stu-id="a9974-1349">vencimiento</span></span>
- <span data-ttu-id="a9974-1350">válido hasta</span><span class="sxs-lookup"><span data-stu-id="a9974-1350">válido hasta</span></span>
- <span data-ttu-id="a9974-1351">valido hasta</span><span class="sxs-lookup"><span data-stu-id="a9974-1351">valido hasta</span></span>
- <span data-ttu-id="a9974-1352">vto</span><span class="sxs-lookup"><span data-stu-id="a9974-1352">vto</span></span>
- <span data-ttu-id="a9974-1353">data de expiração</span><span class="sxs-lookup"><span data-stu-id="a9974-1353">data de expiração</span></span>
- <span data-ttu-id="a9974-1354">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="a9974-1354">data de expiracao</span></span>
- <span data-ttu-id="a9974-1355">data em que expira</span><span class="sxs-lookup"><span data-stu-id="a9974-1355">data em que expira</span></span>
- <span data-ttu-id="a9974-1356">유효한 ade</span><span class="sxs-lookup"><span data-stu-id="a9974-1356">validade</span></span>
- <span data-ttu-id="a9974-1357">valor</span><span class="sxs-lookup"><span data-stu-id="a9974-1357">valor</span></span>
- <span data-ttu-id="a9974-1358">vencimento</span><span class="sxs-lookup"><span data-stu-id="a9974-1358">vencimento</span></span>
- <span data-ttu-id="a9974-1359">venc</span><span class="sxs-lookup"><span data-stu-id="a9974-1359">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="a9974-1360">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="a9974-1360">Keyword_cc_name</span></span>

- <span data-ttu-id="a9974-1361">amex</span><span class="sxs-lookup"><span data-stu-id="a9974-1361">amex</span></span>
- <span data-ttu-id="a9974-1362">american express</span><span class="sxs-lookup"><span data-stu-id="a9974-1362">american express</span></span>
- <span data-ttu-id="a9974-1363">americanexpress</span><span class="sxs-lookup"><span data-stu-id="a9974-1363">americanexpress</span></span>
- <span data-ttu-id="a9974-1364">Visa</span><span class="sxs-lookup"><span data-stu-id="a9974-1364">Visa</span></span>
- <span data-ttu-id="a9974-1365">mastercard</span><span class="sxs-lookup"><span data-stu-id="a9974-1365">mastercard</span></span>
- <span data-ttu-id="a9974-1366">master card</span><span class="sxs-lookup"><span data-stu-id="a9974-1366">master card</span></span>
- <span data-ttu-id="a9974-1367">mc</span><span class="sxs-lookup"><span data-stu-id="a9974-1367">mc</span></span> 
- <span data-ttu-id="a9974-1368">mastercards</span><span class="sxs-lookup"><span data-stu-id="a9974-1368">mastercards</span></span>
- <span data-ttu-id="a9974-1369">master cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1369">master cards</span></span>
- <span data-ttu-id="a9974-1370">diner's Club</span><span class="sxs-lookup"><span data-stu-id="a9974-1370">diner's Club</span></span>
- <span data-ttu-id="a9974-1371">diners club</span><span class="sxs-lookup"><span data-stu-id="a9974-1371">diners club</span></span>
- <span data-ttu-id="a9974-1372">dinersclub</span><span class="sxs-lookup"><span data-stu-id="a9974-1372">dinersclub</span></span>
- <span data-ttu-id="a9974-1373">discover card</span><span class="sxs-lookup"><span data-stu-id="a9974-1373">discover card</span></span>
- <span data-ttu-id="a9974-1374">discovercard</span><span class="sxs-lookup"><span data-stu-id="a9974-1374">discovercard</span></span>
- <span data-ttu-id="a9974-1375">discover cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1375">discover cards</span></span>
- <span data-ttu-id="a9974-1376">JCB</span><span class="sxs-lookup"><span data-stu-id="a9974-1376">JCB</span></span>
- <span data-ttu-id="a9974-1377">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="a9974-1377">japanese card bureau</span></span>
- <span data-ttu-id="a9974-1378">carte blanche</span><span class="sxs-lookup"><span data-stu-id="a9974-1378">carte blanche</span></span>
- <span data-ttu-id="a9974-1379">carteblanche</span><span class="sxs-lookup"><span data-stu-id="a9974-1379">carteblanche</span></span>
- <span data-ttu-id="a9974-1380">credit card</span><span class="sxs-lookup"><span data-stu-id="a9974-1380">credit card</span></span>
- <span data-ttu-id="a9974-1381">참조란</span><span class="sxs-lookup"><span data-stu-id="a9974-1381">cc#</span></span>
- <span data-ttu-id="a9974-1382">참조 #:</span><span class="sxs-lookup"><span data-stu-id="a9974-1382">cc#:</span></span>
- <span data-ttu-id="a9974-1383">expiration date</span><span class="sxs-lookup"><span data-stu-id="a9974-1383">expiration date</span></span>
- <span data-ttu-id="a9974-1384">exp date</span><span class="sxs-lookup"><span data-stu-id="a9974-1384">exp date</span></span>
- <span data-ttu-id="a9974-1385">expiry date</span><span class="sxs-lookup"><span data-stu-id="a9974-1385">expiry date</span></span>
- <span data-ttu-id="a9974-1386">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="a9974-1386">date d’expiration</span></span>
- <span data-ttu-id="a9974-1387">date d'exp</span><span class="sxs-lookup"><span data-stu-id="a9974-1387">date d'exp</span></span>
- <span data-ttu-id="a9974-1388">date expiration</span><span class="sxs-lookup"><span data-stu-id="a9974-1388">date expiration</span></span>
- <span data-ttu-id="a9974-1389">bank card</span><span class="sxs-lookup"><span data-stu-id="a9974-1389">bank card</span></span>
- <span data-ttu-id="a9974-1390">bankcard</span><span class="sxs-lookup"><span data-stu-id="a9974-1390">bankcard</span></span>
- <span data-ttu-id="a9974-1391">card number</span><span class="sxs-lookup"><span data-stu-id="a9974-1391">card number</span></span>
- <span data-ttu-id="a9974-1392">card num</span><span class="sxs-lookup"><span data-stu-id="a9974-1392">card num</span></span>
- <span data-ttu-id="a9974-1393">전화 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1393">cardnumber</span></span>
- <span data-ttu-id="a9974-1394">시 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1394">cardnumbers</span></span>
- <span data-ttu-id="a9974-1395">card numbers</span><span class="sxs-lookup"><span data-stu-id="a9974-1395">card numbers</span></span>
- <span data-ttu-id="a9974-1396">카드</span><span class="sxs-lookup"><span data-stu-id="a9974-1396">creditcard</span></span>
- <span data-ttu-id="a9974-1397">credit cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1397">credit cards</span></span>
- <span data-ttu-id="a9974-1398">creditcards</span><span class="sxs-lookup"><span data-stu-id="a9974-1398">creditcards</span></span>
- <span data-ttu-id="a9974-1399">ccn</span><span class="sxs-lookup"><span data-stu-id="a9974-1399">ccn</span></span>
- <span data-ttu-id="a9974-1400">card holder</span><span class="sxs-lookup"><span data-stu-id="a9974-1400">card holder</span></span>
- <span data-ttu-id="a9974-1401">소유자</span><span class="sxs-lookup"><span data-stu-id="a9974-1401">cardholder</span></span>
- <span data-ttu-id="a9974-1402">card holders</span><span class="sxs-lookup"><span data-stu-id="a9974-1402">card holders</span></span>
- <span data-ttu-id="a9974-1403">에이 홀더</span><span class="sxs-lookup"><span data-stu-id="a9974-1403">cardholders</span></span>
- <span data-ttu-id="a9974-1404">check card</span><span class="sxs-lookup"><span data-stu-id="a9974-1404">check card</span></span>
- <span data-ttu-id="a9974-1405">checkcard</span><span class="sxs-lookup"><span data-stu-id="a9974-1405">checkcard</span></span>
- <span data-ttu-id="a9974-1406">check cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1406">check cards</span></span>
- <span data-ttu-id="a9974-1407">checkcards</span><span class="sxs-lookup"><span data-stu-id="a9974-1407">checkcards</span></span>
- <span data-ttu-id="a9974-1408">debit card</span><span class="sxs-lookup"><span data-stu-id="a9974-1408">debit card</span></span>
- <span data-ttu-id="a9974-1409">debitcard</span><span class="sxs-lookup"><span data-stu-id="a9974-1409">debitcard</span></span>
- <span data-ttu-id="a9974-1410">debit cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1410">debit cards</span></span>
- <span data-ttu-id="a9974-1411">debitcards</span><span class="sxs-lookup"><span data-stu-id="a9974-1411">debitcards</span></span>
- <span data-ttu-id="a9974-1412">atm card</span><span class="sxs-lookup"><span data-stu-id="a9974-1412">atm card</span></span>
- <span data-ttu-id="a9974-1413">atmcard</span><span class="sxs-lookup"><span data-stu-id="a9974-1413">atmcard</span></span>
- <span data-ttu-id="a9974-1414">atm cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1414">atm cards</span></span>
- <span data-ttu-id="a9974-1415">atmcards</span><span class="sxs-lookup"><span data-stu-id="a9974-1415">atmcards</span></span>
- <span data-ttu-id="a9974-1416">enroute</span><span class="sxs-lookup"><span data-stu-id="a9974-1416">enroute</span></span>
- <span data-ttu-id="a9974-1417">en route</span><span class="sxs-lookup"><span data-stu-id="a9974-1417">en route</span></span>
- <span data-ttu-id="a9974-1418">card type</span><span class="sxs-lookup"><span data-stu-id="a9974-1418">card type</span></span>
- <span data-ttu-id="a9974-1419">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="a9974-1419">carte bancaire</span></span>
- <span data-ttu-id="a9974-1420">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="a9974-1420">carte de crédit</span></span>
- <span data-ttu-id="a9974-1421">carte de credit</span><span class="sxs-lookup"><span data-stu-id="a9974-1421">carte de credit</span></span>
- <span data-ttu-id="a9974-1422">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="a9974-1422">numéro de carte</span></span>
- <span data-ttu-id="a9974-1423">numero de carte</span><span class="sxs-lookup"><span data-stu-id="a9974-1423">numero de carte</span></span>
- <span data-ttu-id="a9974-1424">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="a9974-1424">nº de la carte</span></span>
- <span data-ttu-id="a9974-1425">nº de carte</span><span class="sxs-lookup"><span data-stu-id="a9974-1425">nº de carte</span></span>
- <span data-ttu-id="a9974-1426">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="a9974-1426">kreditkarte</span></span>
- <span data-ttu-id="a9974-1427">karte</span><span class="sxs-lookup"><span data-stu-id="a9974-1427">karte</span></span>
- <span data-ttu-id="a9974-1428">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="a9974-1428">karteninhaber</span></span>
- <span data-ttu-id="a9974-1429">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="a9974-1429">karteninhabers</span></span>
- <span data-ttu-id="a9974-1430">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="a9974-1430">kreditkarteninhaber</span></span>
- <span data-ttu-id="a9974-1431">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="a9974-1431">kreditkarteninstitut</span></span>
- <span data-ttu-id="a9974-1432">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="a9974-1432">kreditkartentyp</span></span>
- <span data-ttu-id="a9974-1433">eigentümername</span><span class="sxs-lookup"><span data-stu-id="a9974-1433">eigentümername</span></span>
- <span data-ttu-id="a9974-1434">kartennr</span><span class="sxs-lookup"><span data-stu-id="a9974-1434">kartennr</span></span> 
- <span data-ttu-id="a9974-1435">kartennummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1435">kartennummer</span></span>
- <span data-ttu-id="a9974-1436">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1436">kreditkartennummer</span></span>
- <span data-ttu-id="a9974-1437">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1437">kreditkarten-nummer</span></span>
- <span data-ttu-id="a9974-1438">carta di credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1438">carta di credito</span></span>
- <span data-ttu-id="a9974-1439">carta credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1439">carta credito</span></span>
- <span data-ttu-id="a9974-1440">카 ta</span><span class="sxs-lookup"><span data-stu-id="a9974-1440">carta</span></span>
- <span data-ttu-id="a9974-1441">n carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1441">n carta</span></span>
- <span data-ttu-id="a9974-1442">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="a9974-1442">nr.</span></span> <span data-ttu-id="a9974-1443">카 ta</span><span class="sxs-lookup"><span data-stu-id="a9974-1443">carta</span></span>
- <span data-ttu-id="a9974-1444">nr carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1444">nr carta</span></span>
- <span data-ttu-id="a9974-1445">numero carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1445">numero carta</span></span>
- <span data-ttu-id="a9974-1446">numero della carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1446">numero della carta</span></span>
- <span data-ttu-id="a9974-1447">numero di carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1447">numero di carta</span></span>
- <span data-ttu-id="a9974-1448">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1448">tarjeta credito</span></span>
- <span data-ttu-id="a9974-1449">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1449">tarjeta de credito</span></span>
- <span data-ttu-id="a9974-1450">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="a9974-1450">tarjeta crédito</span></span>
- <span data-ttu-id="a9974-1451">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="a9974-1451">tarjeta de crédito</span></span>
- <span data-ttu-id="a9974-1452">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="a9974-1452">tarjeta de atm</span></span>
- <span data-ttu-id="a9974-1453">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="a9974-1453">tarjeta atm</span></span>
- <span data-ttu-id="a9974-1454">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1454">tarjeta debito</span></span>
- <span data-ttu-id="a9974-1455">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1455">tarjeta de debito</span></span>
- <span data-ttu-id="a9974-1456">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="a9974-1456">tarjeta débito</span></span>
- <span data-ttu-id="a9974-1457">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="a9974-1457">tarjeta de débito</span></span>
- <span data-ttu-id="a9974-1458">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1458">nº de tarjeta</span></span>
- <span data-ttu-id="a9974-1459">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1459">no.</span></span> <span data-ttu-id="a9974-1460">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1460">de tarjeta</span></span>
- <span data-ttu-id="a9974-1461">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1461">no de tarjeta</span></span>
- <span data-ttu-id="a9974-1462">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1462">numero de tarjeta</span></span>
- <span data-ttu-id="a9974-1463">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1463">número de tarjeta</span></span>
- <span data-ttu-id="a9974-1464">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="a9974-1464">tarjeta no</span></span>
- <span data-ttu-id="a9974-1465">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="a9974-1465">tarjetahabiente</span></span>
- <span data-ttu-id="a9974-1466">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="a9974-1466">cartão de crédito</span></span>
- <span data-ttu-id="a9974-1467">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1467">cartão de credito</span></span>
- <span data-ttu-id="a9974-1468">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="a9974-1468">cartao de crédito</span></span>
- <span data-ttu-id="a9974-1469">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1469">cartao de credito</span></span>
- <span data-ttu-id="a9974-1470">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="a9974-1470">cartão de débito</span></span>
- <span data-ttu-id="a9974-1471">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="a9974-1471">cartao de débito</span></span>
- <span data-ttu-id="a9974-1472">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1472">cartão de debito</span></span>
- <span data-ttu-id="a9974-1473">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1473">cartao de debito</span></span>
- <span data-ttu-id="a9974-1474">débito automático</span><span class="sxs-lookup"><span data-stu-id="a9974-1474">débito automático</span></span>
- <span data-ttu-id="a9974-1475">debito automatico</span><span class="sxs-lookup"><span data-stu-id="a9974-1475">debito automatico</span></span>
- <span data-ttu-id="a9974-1476">número do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1476">número do cartão</span></span>
- <span data-ttu-id="a9974-1477">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1477">numero do cartão</span></span> 
- <span data-ttu-id="a9974-1478">número do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1478">número do cartao</span></span>
- <span data-ttu-id="a9974-1479">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1479">numero do cartao</span></span>
- <span data-ttu-id="a9974-1480">número de cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1480">número de cartão</span></span>
- <span data-ttu-id="a9974-1481">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1481">numero de cartão</span></span>
- <span data-ttu-id="a9974-1482">número de cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1482">número de cartao</span></span>
- <span data-ttu-id="a9974-1483">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1483">numero de cartao</span></span>
- <span data-ttu-id="a9974-1484">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1484">nº do cartão</span></span>
- <span data-ttu-id="a9974-1485">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1485">nº do cartao</span></span>
- <span data-ttu-id="a9974-1486">n º</span><span class="sxs-lookup"><span data-stu-id="a9974-1486">nº.</span></span> <span data-ttu-id="a9974-1487">do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1487">do cartão</span></span>
- <span data-ttu-id="a9974-1488">no do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1488">no do cartão</span></span>
- <span data-ttu-id="a9974-1489">no do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1489">no do cartao</span></span>
- <span data-ttu-id="a9974-1490">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1490">no.</span></span> <span data-ttu-id="a9974-1491">do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1491">do cartão</span></span>
- <span data-ttu-id="a9974-1492">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1492">no.</span></span> <span data-ttu-id="a9974-1493">do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1493">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="a9974-1494">크로아티아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1494">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1495">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1495">Format</span></span>

<span data-ttu-id="a9974-1496">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1496">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1497">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1497">Pattern</span></span>

<span data-ttu-id="a9974-1498">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1498">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1499">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1499">Checksum</span></span>

<span data-ttu-id="a9974-1500">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-1500">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1501">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1501">Definition</span></span>

<span data-ttu-id="a9974-1502">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1502">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1503">Func_croatia_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1503">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1504">Keyword_croatia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1504">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-1505">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1505">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="a9974-1506">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="a9974-1506">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="a9974-1507">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="a9974-1507">Croatian identity card</span></span>
- <span data-ttu-id="a9974-1508">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="a9974-1508">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="a9974-1509">크로아티아 개인 식별(OIB) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1509">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1510">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1510">Format</span></span>

<span data-ttu-id="a9974-1511">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1511">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1512">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1512">Pattern</span></span>

<span data-ttu-id="a9974-1513">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-1513">11 digits:</span></span>
- <span data-ttu-id="a9974-1514">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1514">10 digits</span></span> 
- <span data-ttu-id="a9974-1515">최종 자릿수는 국제 데이터 교환 목적을 위한 검사 숫자 이며, HR는 11 자리 숫자 앞에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1515">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1516">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1516">Checksum</span></span>

<span data-ttu-id="a9974-1517">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1517">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1518">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1518">Definition</span></span>

<span data-ttu-id="a9974-1519">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1519">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1520">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1520">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1521">Keyword_croatia_oib_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1521">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="a9974-1522">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1522">The checksum passes.</span></span>

<span data-ttu-id="a9974-1523">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1523">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1524">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1524">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1525">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1525">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1526">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1526">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="a9974-1527">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="a9974-1527">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="a9974-1528">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="a9974-1528">Personal Identification Number</span></span>
- <span data-ttu-id="a9974-1529">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="a9974-1529">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="a9974-1530">OIB</span><span class="sxs-lookup"><span data-stu-id="a9974-1530">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="a9974-1531">체코어 개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1531">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1532">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1532">Format</span></span>

<span data-ttu-id="a9974-1533">선택적 슬래시 (이전 형식)가 있는 9 자리 숫자와 슬래시 (새 형식)가 있는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1533">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1534">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1534">Pattern</span></span>

<span data-ttu-id="a9974-1535">9 자리 숫자 (이전 형식):</span><span class="sxs-lookup"><span data-stu-id="a9974-1535">Nine digits (old format):</span></span>
- <span data-ttu-id="a9974-1536">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1536">Nine digits</span></span>

<span data-ttu-id="a9974-1537">또는</span><span class="sxs-lookup"><span data-stu-id="a9974-1537">OR</span></span>

- <span data-ttu-id="a9974-1538">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1538">Six digits that represent date of birth</span></span>
- <span data-ttu-id="a9974-1539">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="a9974-1539">A forward slash</span></span>
- <span data-ttu-id="a9974-1540">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1540">Three digits</span></span>

<span data-ttu-id="a9974-1541">10 자리 숫자 (새 형식):</span><span class="sxs-lookup"><span data-stu-id="a9974-1541">10 digits (new format):</span></span>
- <span data-ttu-id="a9974-1542">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1542">10 digits</span></span>

<span data-ttu-id="a9974-1543">또는</span><span class="sxs-lookup"><span data-stu-id="a9974-1543">OR</span></span>

- <span data-ttu-id="a9974-1544">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1544">Six digits that represent date of birth</span></span>
- <span data-ttu-id="a9974-1545">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="a9974-1545">A forward slash</span></span> 
- <span data-ttu-id="a9974-1546">마지막 숫자가 검사 숫자인 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1546">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1547">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1547">Checksum</span></span>

<span data-ttu-id="a9974-1548">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1549">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1549">Definition</span></span>

<span data-ttu-id="a9974-1550">DLP 정책은 300 문자 근사에서 Func_czech_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="a9974-1551">Keyword_czech_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1551">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="a9974-1552">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1552">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="a9974-1553">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1553">Keywords</span></span>

- <span data-ttu-id="a9974-1554">체코어 개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1554">czech personal identity number</span></span>
- <span data-ttu-id="a9974-1555">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="a9974-1555">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="a9974-1556">덴마크 개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1556">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1557">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1557">Format</span></span>

<span data-ttu-id="a9974-1558">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1558">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1559">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1559">Pattern</span></span>

<span data-ttu-id="a9974-1560">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-1560">10 digits:</span></span>
- <span data-ttu-id="a9974-1561">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-1561">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="a9974-1562">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-1562">A hyphen</span></span> 
- <span data-ttu-id="a9974-1563">마지막 숫자가 검사 숫자인 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1563">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1564">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1564">Checksum</span></span>

<span data-ttu-id="a9974-1565">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1565">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1566">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1566">Definition</span></span>

<span data-ttu-id="a9974-1567">DLP 정책은 300 문자 (예: Regex_denmark_id)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1567">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="a9974-1568">Keyword_denmark_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1568">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="a9974-1569">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1569">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-1570">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1570">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="a9974-1571">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="a9974-1571">Keyword_denmark_id</span></span>

- <span data-ttu-id="a9974-1572">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="a9974-1572">Personal Identification Number</span></span>
- <span data-ttu-id="a9974-1573">CPR</span><span class="sxs-lookup"><span data-stu-id="a9974-1573">CPR</span></span>
- <span data-ttu-id="a9974-1574">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="a9974-1574">Det Centrale Personregister</span></span>
- <span data-ttu-id="a9974-1575">Personnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1575">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="a9974-1576">DEA(약물 집행 기구) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1576">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1577">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1577">Format</span></span>

<span data-ttu-id="a9974-1578">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1578">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1579">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1579">Pattern</span></span>

<span data-ttu-id="a9974-1580">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1580">Pattern must include all of the following:</span></span>
- <span data-ttu-id="a9974-1581">등록 코드에 해당하는 abcdefghjklmnprstux 중 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-1581">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="a9974-1582">등록자 성의 첫 문자에 해당하는 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-1582">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="a9974-1583">검사 숫자의 마지막 7개 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1583">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1584">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1584">Checksum</span></span>

<span data-ttu-id="a9974-1585">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1586">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1586">Definition</span></span>

<span data-ttu-id="a9974-1587">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1587">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1588">Func_dea_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1588">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1589">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1589">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-1590">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1590">Keywords</span></span>

<span data-ttu-id="a9974-1591">없음</span><span class="sxs-lookup"><span data-stu-id="a9974-1591">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="a9974-1592">유럽 직불 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1592">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1593">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1593">Format</span></span>

<span data-ttu-id="a9974-1594">16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1594">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1595">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1595">Pattern</span></span>

<span data-ttu-id="a9974-1596">매우 복잡하고 강력한 패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1596">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1597">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1597">Checksum</span></span>

<span data-ttu-id="a9974-1598">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1598">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1599">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1599">Definition</span></span>

<span data-ttu-id="a9974-1600">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1600">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1601">Func_eu_debit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1601">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1602">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1602">At least one of the following is true:</span></span>
    - <span data-ttu-id="a9974-1603">Keyword_eu_debit_card의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1603">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="a9974-1604">Keyword_card_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1604">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="a9974-1605">Keyword_card_security_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1605">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="a9974-1606">Keyword_card_expiration_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1606">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="a9974-1607">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1607">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="a9974-1608">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1608">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1609">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1609">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="a9974-1610">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="a9974-1610">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="a9974-1611">account number</span><span class="sxs-lookup"><span data-stu-id="a9974-1611">account number</span></span> 
- <span data-ttu-id="a9974-1612">card number</span><span class="sxs-lookup"><span data-stu-id="a9974-1612">card number</span></span> 
- <span data-ttu-id="a9974-1613">card no.</span><span class="sxs-lookup"><span data-stu-id="a9974-1613">card no.</span></span> 
- <span data-ttu-id="a9974-1614">security number</span><span class="sxs-lookup"><span data-stu-id="a9974-1614">security number</span></span> 
- <span data-ttu-id="a9974-1615">참조란</span><span class="sxs-lookup"><span data-stu-id="a9974-1615">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="a9974-1616">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="a9974-1616">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="a9974-1617">acct nbr</span><span class="sxs-lookup"><span data-stu-id="a9974-1617">acct nbr</span></span> 
- <span data-ttu-id="a9974-1618">acct num</span><span class="sxs-lookup"><span data-stu-id="a9974-1618">acct num</span></span> 
- <span data-ttu-id="a9974-1619">acct no</span><span class="sxs-lookup"><span data-stu-id="a9974-1619">acct no</span></span> 
- <span data-ttu-id="a9974-1620">american express</span><span class="sxs-lookup"><span data-stu-id="a9974-1620">american express</span></span> 
- <span data-ttu-id="a9974-1621">americanexpress</span><span class="sxs-lookup"><span data-stu-id="a9974-1621">americanexpress</span></span> 
- <span data-ttu-id="a9974-1622">americano espresso</span><span class="sxs-lookup"><span data-stu-id="a9974-1622">americano espresso</span></span> 
- <span data-ttu-id="a9974-1623">amex</span><span class="sxs-lookup"><span data-stu-id="a9974-1623">amex</span></span> 
- <span data-ttu-id="a9974-1624">atm card</span><span class="sxs-lookup"><span data-stu-id="a9974-1624">atm card</span></span> 
- <span data-ttu-id="a9974-1625">atm cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1625">atm cards</span></span> 
- <span data-ttu-id="a9974-1626">atm kaart</span><span class="sxs-lookup"><span data-stu-id="a9974-1626">atm kaart</span></span> 
- <span data-ttu-id="a9974-1627">atmcard</span><span class="sxs-lookup"><span data-stu-id="a9974-1627">atmcard</span></span> 
- <span data-ttu-id="a9974-1628">atmcards</span><span class="sxs-lookup"><span data-stu-id="a9974-1628">atmcards</span></span> 
- <span data-ttu-id="a9974-1629">atmkaart</span><span class="sxs-lookup"><span data-stu-id="a9974-1629">atmkaart</span></span> 
- <span data-ttu-id="a9974-1630">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="a9974-1630">atmkaarten</span></span> 
- <span data-ttu-id="a9974-1631">bancontact</span><span class="sxs-lookup"><span data-stu-id="a9974-1631">bancontact</span></span> 
- <span data-ttu-id="a9974-1632">bank card</span><span class="sxs-lookup"><span data-stu-id="a9974-1632">bank card</span></span> 
- <span data-ttu-id="a9974-1633">bankkaart</span><span class="sxs-lookup"><span data-stu-id="a9974-1633">bankkaart</span></span> 
- <span data-ttu-id="a9974-1634">card holder</span><span class="sxs-lookup"><span data-stu-id="a9974-1634">card holder</span></span> 
- <span data-ttu-id="a9974-1635">card holders</span><span class="sxs-lookup"><span data-stu-id="a9974-1635">card holders</span></span> 
- <span data-ttu-id="a9974-1636">card num</span><span class="sxs-lookup"><span data-stu-id="a9974-1636">card num</span></span> 
- <span data-ttu-id="a9974-1637">card number</span><span class="sxs-lookup"><span data-stu-id="a9974-1637">card number</span></span> 
- <span data-ttu-id="a9974-1638">card numbers</span><span class="sxs-lookup"><span data-stu-id="a9974-1638">card numbers</span></span> 
- <span data-ttu-id="a9974-1639">card type</span><span class="sxs-lookup"><span data-stu-id="a9974-1639">card type</span></span> 
- <span data-ttu-id="a9974-1640">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="a9974-1640">cardano numerico</span></span> 
- <span data-ttu-id="a9974-1641">소유자</span><span class="sxs-lookup"><span data-stu-id="a9974-1641">cardholder</span></span> 
- <span data-ttu-id="a9974-1642">에이 홀더</span><span class="sxs-lookup"><span data-stu-id="a9974-1642">cardholders</span></span> 
- <span data-ttu-id="a9974-1643">전화 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1643">cardnumber</span></span> 
- <span data-ttu-id="a9974-1644">시 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1644">cardnumbers</span></span> 
- <span data-ttu-id="a9974-1645">carta bianca</span><span class="sxs-lookup"><span data-stu-id="a9974-1645">carta bianca</span></span> 
- <span data-ttu-id="a9974-1646">carta credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1646">carta credito</span></span> 
- <span data-ttu-id="a9974-1647">carta di credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1647">carta di credito</span></span> 
- <span data-ttu-id="a9974-1648">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1648">cartao de credito</span></span> 
- <span data-ttu-id="a9974-1649">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="a9974-1649">cartao de crédito</span></span> 
- <span data-ttu-id="a9974-1650">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1650">cartao de debito</span></span> 
- <span data-ttu-id="a9974-1651">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="a9974-1651">cartao de débito</span></span> 
- <span data-ttu-id="a9974-1652">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="a9974-1652">carte bancaire</span></span> 
- <span data-ttu-id="a9974-1653">carte blanche</span><span class="sxs-lookup"><span data-stu-id="a9974-1653">carte blanche</span></span> 
- <span data-ttu-id="a9974-1654">carte bleue</span><span class="sxs-lookup"><span data-stu-id="a9974-1654">carte bleue</span></span> 
- <span data-ttu-id="a9974-1655">carte de credit</span><span class="sxs-lookup"><span data-stu-id="a9974-1655">carte de credit</span></span> 
- <span data-ttu-id="a9974-1656">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="a9974-1656">carte de crédit</span></span> 
- <span data-ttu-id="a9974-1657">carte di credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1657">carte di credito</span></span> 
- <span data-ttu-id="a9974-1658">carteblanche</span><span class="sxs-lookup"><span data-stu-id="a9974-1658">carteblanche</span></span> 
- <span data-ttu-id="a9974-1659">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1659">cartão de credito</span></span> 
- <span data-ttu-id="a9974-1660">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="a9974-1660">cartão de crédito</span></span> 
- <span data-ttu-id="a9974-1661">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1661">cartão de debito</span></span> 
- <span data-ttu-id="a9974-1662">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="a9974-1662">cartão de débito</span></span> 
- <span data-ttu-id="a9974-1663">cb</span><span class="sxs-lookup"><span data-stu-id="a9974-1663">cb</span></span> 
- <span data-ttu-id="a9974-1664">ccn</span><span class="sxs-lookup"><span data-stu-id="a9974-1664">ccn</span></span> 
- <span data-ttu-id="a9974-1665">check card</span><span class="sxs-lookup"><span data-stu-id="a9974-1665">check card</span></span> 
- <span data-ttu-id="a9974-1666">check cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1666">check cards</span></span> 
- <span data-ttu-id="a9974-1667">checkcard</span><span class="sxs-lookup"><span data-stu-id="a9974-1667">checkcard</span></span>
- <span data-ttu-id="a9974-1668">checkcards</span><span class="sxs-lookup"><span data-stu-id="a9974-1668">checkcards</span></span> 
- <span data-ttu-id="a9974-1669">chequekaart</span><span class="sxs-lookup"><span data-stu-id="a9974-1669">chequekaart</span></span> 
- <span data-ttu-id="a9974-1670">cirrus</span><span class="sxs-lookup"><span data-stu-id="a9974-1670">cirrus</span></span> 
- <span data-ttu-id="a9974-1671">cirrus-edc-maestro</span><span class="sxs-lookup"><span data-stu-id="a9974-1671">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="a9974-1672">controlekaart</span><span class="sxs-lookup"><span data-stu-id="a9974-1672">controlekaart</span></span> 
- <span data-ttu-id="a9974-1673">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="a9974-1673">controlekaarten</span></span> 
- <span data-ttu-id="a9974-1674">credit card</span><span class="sxs-lookup"><span data-stu-id="a9974-1674">credit card</span></span> 
- <span data-ttu-id="a9974-1675">credit cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1675">credit cards</span></span> 
- <span data-ttu-id="a9974-1676">카드</span><span class="sxs-lookup"><span data-stu-id="a9974-1676">creditcard</span></span> 
- <span data-ttu-id="a9974-1677">creditcards</span><span class="sxs-lookup"><span data-stu-id="a9974-1677">creditcards</span></span> 
- <span data-ttu-id="a9974-1678">debetkaart</span><span class="sxs-lookup"><span data-stu-id="a9974-1678">debetkaart</span></span> 
- <span data-ttu-id="a9974-1679">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="a9974-1679">debetkaarten</span></span> 
- <span data-ttu-id="a9974-1680">debit card</span><span class="sxs-lookup"><span data-stu-id="a9974-1680">debit card</span></span> 
- <span data-ttu-id="a9974-1681">debit cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1681">debit cards</span></span> 
- <span data-ttu-id="a9974-1682">debitcard</span><span class="sxs-lookup"><span data-stu-id="a9974-1682">debitcard</span></span> 
- <span data-ttu-id="a9974-1683">debitcards</span><span class="sxs-lookup"><span data-stu-id="a9974-1683">debitcards</span></span> 
- <span data-ttu-id="a9974-1684">debito automatico</span><span class="sxs-lookup"><span data-stu-id="a9974-1684">debito automatico</span></span> 
- <span data-ttu-id="a9974-1685">diners club</span><span class="sxs-lookup"><span data-stu-id="a9974-1685">diners club</span></span> 
- <span data-ttu-id="a9974-1686">dinersclub</span><span class="sxs-lookup"><span data-stu-id="a9974-1686">dinersclub</span></span> 
- <span data-ttu-id="a9974-1687">찾아보십시오</span><span class="sxs-lookup"><span data-stu-id="a9974-1687">discover</span></span> 
- <span data-ttu-id="a9974-1688">discover card</span><span class="sxs-lookup"><span data-stu-id="a9974-1688">discover card</span></span> 
- <span data-ttu-id="a9974-1689">discover cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1689">discover cards</span></span> 
- <span data-ttu-id="a9974-1690">discovercard</span><span class="sxs-lookup"><span data-stu-id="a9974-1690">discovercard</span></span> 
- <span data-ttu-id="a9974-1691">discovercards</span><span class="sxs-lookup"><span data-stu-id="a9974-1691">discovercards</span></span> 
- <span data-ttu-id="a9974-1692">débito automático</span><span class="sxs-lookup"><span data-stu-id="a9974-1692">débito automático</span></span>
- <span data-ttu-id="a9974-1693">edc</span><span class="sxs-lookup"><span data-stu-id="a9974-1693">edc</span></span> 
- <span data-ttu-id="a9974-1694">eigentümername</span><span class="sxs-lookup"><span data-stu-id="a9974-1694">eigentümername</span></span> 
- <span data-ttu-id="a9974-1695">european debit card</span><span class="sxs-lookup"><span data-stu-id="a9974-1695">european debit card</span></span> 
- <span data-ttu-id="a9974-1696">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="a9974-1696">hoofdkaart</span></span> 
- <span data-ttu-id="a9974-1697">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="a9974-1697">hoofdkaarten</span></span> 
- <span data-ttu-id="a9974-1698">in viaggio</span><span class="sxs-lookup"><span data-stu-id="a9974-1698">in viaggio</span></span> 
- <span data-ttu-id="a9974-1699">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="a9974-1699">japanese card bureau</span></span> 
- <span data-ttu-id="a9974-1700">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="a9974-1700">japanse kaartdienst</span></span> 
- <span data-ttu-id="a9974-1701">jcb</span><span class="sxs-lookup"><span data-stu-id="a9974-1701">jcb</span></span> 
- <span data-ttu-id="a9974-1702">kaart</span><span class="sxs-lookup"><span data-stu-id="a9974-1702">kaart</span></span> 
- <span data-ttu-id="a9974-1703">kaart num</span><span class="sxs-lookup"><span data-stu-id="a9974-1703">kaart num</span></span> 
- <span data-ttu-id="a9974-1704">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="a9974-1704">kaartaantal</span></span> 
- <span data-ttu-id="a9974-1705">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="a9974-1705">kaartaantallen</span></span> 
- <span data-ttu-id="a9974-1706">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="a9974-1706">kaarthouder</span></span> 
- <span data-ttu-id="a9974-1707">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="a9974-1707">kaarthouders</span></span> 
- <span data-ttu-id="a9974-1708">karte</span><span class="sxs-lookup"><span data-stu-id="a9974-1708">karte</span></span>  
- <span data-ttu-id="a9974-1709">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="a9974-1709">karteninhaber</span></span> 
- <span data-ttu-id="a9974-1710">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="a9974-1710">karteninhabers</span></span>
- <span data-ttu-id="a9974-1711">kartennr</span><span class="sxs-lookup"><span data-stu-id="a9974-1711">kartennr</span></span> 
- <span data-ttu-id="a9974-1712">kartennummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1712">kartennummer</span></span> 
- <span data-ttu-id="a9974-1713">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="a9974-1713">kreditkarte</span></span> 
- <span data-ttu-id="a9974-1714">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1714">kreditkarten-nummer</span></span> 
- <span data-ttu-id="a9974-1715">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="a9974-1715">kreditkarteninhaber</span></span> 
- <span data-ttu-id="a9974-1716">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="a9974-1716">kreditkarteninstitut</span></span> 
- <span data-ttu-id="a9974-1717">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1717">kreditkartennummer</span></span> 
- <span data-ttu-id="a9974-1718">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="a9974-1718">kreditkartentyp</span></span> 
- <span data-ttu-id="a9974-1719">maestro</span><span class="sxs-lookup"><span data-stu-id="a9974-1719">maestro</span></span> 
- <span data-ttu-id="a9974-1720">master card</span><span class="sxs-lookup"><span data-stu-id="a9974-1720">master card</span></span> 
- <span data-ttu-id="a9974-1721">master cards</span><span class="sxs-lookup"><span data-stu-id="a9974-1721">master cards</span></span> 
- <span data-ttu-id="a9974-1722">mastercard</span><span class="sxs-lookup"><span data-stu-id="a9974-1722">mastercard</span></span> 
- <span data-ttu-id="a9974-1723">mastercards</span><span class="sxs-lookup"><span data-stu-id="a9974-1723">mastercards</span></span> 
- <span data-ttu-id="a9974-1724">mc</span><span class="sxs-lookup"><span data-stu-id="a9974-1724">mc</span></span> 
- <span data-ttu-id="a9974-1725">mister cash</span><span class="sxs-lookup"><span data-stu-id="a9974-1725">mister cash</span></span> 
- <span data-ttu-id="a9974-1726">n carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1726">n carta</span></span> 
- <span data-ttu-id="a9974-1727">카 ta</span><span class="sxs-lookup"><span data-stu-id="a9974-1727">carta</span></span> 
- <span data-ttu-id="a9974-1728">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1728">no de tarjeta</span></span> 
- <span data-ttu-id="a9974-1729">no do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1729">no do cartao</span></span> 
- <span data-ttu-id="a9974-1730">no do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1730">no do cartão</span></span> 
- <span data-ttu-id="a9974-1731">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1731">no.</span></span> <span data-ttu-id="a9974-1732">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1732">de tarjeta</span></span> 
- <span data-ttu-id="a9974-1733">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1733">no.</span></span> <span data-ttu-id="a9974-1734">do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1734">do cartao</span></span> 
- <span data-ttu-id="a9974-1735">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1735">no.</span></span> <span data-ttu-id="a9974-1736">do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1736">do cartão</span></span> 
- <span data-ttu-id="a9974-1737">nr carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1737">nr carta</span></span> 
- <span data-ttu-id="a9974-1738">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="a9974-1738">nr.</span></span> <span data-ttu-id="a9974-1739">카 ta</span><span class="sxs-lookup"><span data-stu-id="a9974-1739">carta</span></span> 
- <span data-ttu-id="a9974-1740">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="a9974-1740">numeri di scheda</span></span> 
- <span data-ttu-id="a9974-1741">numero carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1741">numero carta</span></span> 
- <span data-ttu-id="a9974-1742">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1742">numero de cartao</span></span> 
- <span data-ttu-id="a9974-1743">numero de carte</span><span class="sxs-lookup"><span data-stu-id="a9974-1743">numero de carte</span></span> 
- <span data-ttu-id="a9974-1744">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1744">numero de cartão</span></span> 
- <span data-ttu-id="a9974-1745">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1745">numero de tarjeta</span></span>
- <span data-ttu-id="a9974-1746">numero della carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1746">numero della carta</span></span> 
- <span data-ttu-id="a9974-1747">numero di carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1747">numero di carta</span></span> 
- <span data-ttu-id="a9974-1748">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="a9974-1748">numero di scheda</span></span> 
- <span data-ttu-id="a9974-1749">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1749">numero do cartao</span></span> 
- <span data-ttu-id="a9974-1750">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1750">numero do cartão</span></span> 
- <span data-ttu-id="a9974-1751">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="a9974-1751">numéro de carte</span></span> 
- <span data-ttu-id="a9974-1752">nº carta</span><span class="sxs-lookup"><span data-stu-id="a9974-1752">nº carta</span></span> 
- <span data-ttu-id="a9974-1753">nº de carte</span><span class="sxs-lookup"><span data-stu-id="a9974-1753">nº de carte</span></span> 
- <span data-ttu-id="a9974-1754">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="a9974-1754">nº de la carte</span></span> 
- <span data-ttu-id="a9974-1755">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1755">nº de tarjeta</span></span> 
- <span data-ttu-id="a9974-1756">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1756">nº do cartao</span></span> 
- <span data-ttu-id="a9974-1757">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1757">nº do cartão</span></span> 
- <span data-ttu-id="a9974-1758">n º</span><span class="sxs-lookup"><span data-stu-id="a9974-1758">nº.</span></span> <span data-ttu-id="a9974-1759">do cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1759">do cartão</span></span> 
- <span data-ttu-id="a9974-1760">número de cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1760">número de cartao</span></span> 
- <span data-ttu-id="a9974-1761">número de cartão</span><span class="sxs-lookup"><span data-stu-id="a9974-1761">número de cartão</span></span> 
- <span data-ttu-id="a9974-1762">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="a9974-1762">número de tarjeta</span></span> 
- <span data-ttu-id="a9974-1763">número do cartao</span><span class="sxs-lookup"><span data-stu-id="a9974-1763">número do cartao</span></span> 
- <span data-ttu-id="a9974-1764">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="a9974-1764">scheda dell'assegno</span></span> 
- <span data-ttu-id="a9974-1765">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="a9974-1765">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="a9974-1766">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="a9974-1766">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="a9974-1767">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="a9974-1767">scheda della banca</span></span> 
- <span data-ttu-id="a9974-1768">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="a9974-1768">scheda di controllo</span></span> 
- <span data-ttu-id="a9974-1769">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1769">scheda di debito</span></span> 
- <span data-ttu-id="a9974-1770">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="a9974-1770">scheda matrice</span></span> 
- <span data-ttu-id="a9974-1771">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="a9974-1771">schede dell'atmosfera</span></span> 
- <span data-ttu-id="a9974-1772">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="a9974-1772">schede di controllo</span></span> 
- <span data-ttu-id="a9974-1773">schede di debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1773">schede di debito</span></span> 
- <span data-ttu-id="a9974-1774">schede matrici</span><span class="sxs-lookup"><span data-stu-id="a9974-1774">schede matrici</span></span> 
- <span data-ttu-id="a9974-1775">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="a9974-1775">scoprono la scheda</span></span> 
- <span data-ttu-id="a9974-1776">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="a9974-1776">scoprono le schede</span></span> 
- <span data-ttu-id="a9974-1777">분리</span><span class="sxs-lookup"><span data-stu-id="a9974-1777">solo</span></span> 
- <span data-ttu-id="a9974-1778">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="a9974-1778">supporti di scheda</span></span> 
- <span data-ttu-id="a9974-1779">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="a9974-1779">supporto di scheda</span></span> 
- <span data-ttu-id="a9974-1780">스위치</span><span class="sxs-lookup"><span data-stu-id="a9974-1780">switch</span></span> 
- <span data-ttu-id="a9974-1781">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="a9974-1781">tarjeta atm</span></span> 
- <span data-ttu-id="a9974-1782">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1782">tarjeta credito</span></span> 
- <span data-ttu-id="a9974-1783">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="a9974-1783">tarjeta de atm</span></span> 
- <span data-ttu-id="a9974-1784">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="a9974-1784">tarjeta de credito</span></span> 
- <span data-ttu-id="a9974-1785">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1785">tarjeta de debito</span></span> 
- <span data-ttu-id="a9974-1786">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="a9974-1786">tarjeta debito</span></span> 
- <span data-ttu-id="a9974-1787">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="a9974-1787">tarjeta no</span></span>
- <span data-ttu-id="a9974-1788">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="a9974-1788">tarjetahabiente</span></span> 
- <span data-ttu-id="a9974-1789">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="a9974-1789">tipo della scheda</span></span> 
- <span data-ttu-id="a9974-1790">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="a9974-1790">ufficio giapponese della</span></span> 
- <span data-ttu-id="a9974-1791">scheda</span><span class="sxs-lookup"><span data-stu-id="a9974-1791">scheda</span></span> 
- <span data-ttu-id="a9974-1792">v pay</span><span class="sxs-lookup"><span data-stu-id="a9974-1792">v pay</span></span> 
- <span data-ttu-id="a9974-1793">v-지급</span><span class="sxs-lookup"><span data-stu-id="a9974-1793">v-pay</span></span> 
- <span data-ttu-id="a9974-1794">visa</span><span class="sxs-lookup"><span data-stu-id="a9974-1794">visa</span></span> 
- <span data-ttu-id="a9974-1795">visa plus</span><span class="sxs-lookup"><span data-stu-id="a9974-1795">visa plus</span></span> 
- <span data-ttu-id="a9974-1796">visa electron</span><span class="sxs-lookup"><span data-stu-id="a9974-1796">visa electron</span></span> 
- <span data-ttu-id="a9974-1797">visto</span><span class="sxs-lookup"><span data-stu-id="a9974-1797">visto</span></span> 
- <span data-ttu-id="a9974-1798">visum</span><span class="sxs-lookup"><span data-stu-id="a9974-1798">visum</span></span> 
- <span data-ttu-id="a9974-1799">vpay</span><span class="sxs-lookup"><span data-stu-id="a9974-1799">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="a9974-1800">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="a9974-1800">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="a9974-1801">card identification number</span><span class="sxs-lookup"><span data-stu-id="a9974-1801">card identification number</span></span>
- <span data-ttu-id="a9974-1802">card verification</span><span class="sxs-lookup"><span data-stu-id="a9974-1802">card verification</span></span> 
- <span data-ttu-id="a9974-1803">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="a9974-1803">cardi la verifica</span></span> 
- <span data-ttu-id="a9974-1804">cid</span><span class="sxs-lookup"><span data-stu-id="a9974-1804">cid</span></span> 
- <span data-ttu-id="a9974-1805">cod seg</span><span class="sxs-lookup"><span data-stu-id="a9974-1805">cod seg</span></span> 
- <span data-ttu-id="a9974-1806">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1806">cod seguranca</span></span> 
- <span data-ttu-id="a9974-1807">cod segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1807">cod segurança</span></span> 
- <span data-ttu-id="a9974-1808">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="a9974-1808">cod sicurezza</span></span> 
- <span data-ttu-id="a9974-1809">cod.</span><span class="sxs-lookup"><span data-stu-id="a9974-1809">cod.</span></span> <span data-ttu-id="a9974-1810">seg</span><span class="sxs-lookup"><span data-stu-id="a9974-1810">seg</span></span> 
- <span data-ttu-id="a9974-1811">cod.</span><span class="sxs-lookup"><span data-stu-id="a9974-1811">cod.</span></span> <span data-ttu-id="a9974-1812">seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1812">seguranca</span></span> 
- <span data-ttu-id="a9974-1813">cod.</span><span class="sxs-lookup"><span data-stu-id="a9974-1813">cod.</span></span> <span data-ttu-id="a9974-1814">segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1814">segurança</span></span> 
- <span data-ttu-id="a9974-1815">cod.</span><span class="sxs-lookup"><span data-stu-id="a9974-1815">cod.</span></span> <span data-ttu-id="a9974-1816">sicurezza</span><span class="sxs-lookup"><span data-stu-id="a9974-1816">sicurezza</span></span> 
- <span data-ttu-id="a9974-1817">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="a9974-1817">codice di sicurezza</span></span> 
- <span data-ttu-id="a9974-1818">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="a9974-1818">codice di verifica</span></span> 
- <span data-ttu-id="a9974-1819">codigo</span><span class="sxs-lookup"><span data-stu-id="a9974-1819">codigo</span></span> 
- <span data-ttu-id="a9974-1820">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1820">codigo de seguranca</span></span> 
- <span data-ttu-id="a9974-1821">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1821">codigo de segurança</span></span> 
- <span data-ttu-id="a9974-1822">crittogramma</span><span class="sxs-lookup"><span data-stu-id="a9974-1822">crittogramma</span></span> 
- <span data-ttu-id="a9974-1823">cryptogram</span><span class="sxs-lookup"><span data-stu-id="a9974-1823">cryptogram</span></span> 
- <span data-ttu-id="a9974-1824">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="a9974-1824">cryptogramme</span></span> 
- <span data-ttu-id="a9974-1825">cv2</span><span class="sxs-lookup"><span data-stu-id="a9974-1825">cv2</span></span> 
- <span data-ttu-id="a9974-1826">cvc</span><span class="sxs-lookup"><span data-stu-id="a9974-1826">cvc</span></span> 
- <span data-ttu-id="a9974-1827">cvc2</span><span class="sxs-lookup"><span data-stu-id="a9974-1827">cvc2</span></span> 
- <span data-ttu-id="a9974-1828">cvn</span><span class="sxs-lookup"><span data-stu-id="a9974-1828">cvn</span></span> 
- <span data-ttu-id="a9974-1829">cvv</span><span class="sxs-lookup"><span data-stu-id="a9974-1829">cvv</span></span> 
- <span data-ttu-id="a9974-1830">cvv2</span><span class="sxs-lookup"><span data-stu-id="a9974-1830">cvv2</span></span> 
- <span data-ttu-id="a9974-1831">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1831">cód seguranca</span></span> 
- <span data-ttu-id="a9974-1832">cód segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1832">cód segurança</span></span> 
- <span data-ttu-id="a9974-1833">cód</span><span class="sxs-lookup"><span data-stu-id="a9974-1833">cód.</span></span> <span data-ttu-id="a9974-1834">seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1834">seguranca</span></span> 
- <span data-ttu-id="a9974-1835">cód</span><span class="sxs-lookup"><span data-stu-id="a9974-1835">cód.</span></span> <span data-ttu-id="a9974-1836">segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1836">segurança</span></span> 
- <span data-ttu-id="a9974-1837">código</span><span class="sxs-lookup"><span data-stu-id="a9974-1837">código</span></span> 
- <span data-ttu-id="a9974-1838">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="a9974-1838">código de seguranca</span></span> 
- <span data-ttu-id="a9974-1839">código de segurança</span><span class="sxs-lookup"><span data-stu-id="a9974-1839">código de segurança</span></span> 
- <span data-ttu-id="a9974-1840">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="a9974-1840">de kaart controle</span></span> 
- <span data-ttu-id="a9974-1841">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="a9974-1841">geeft nr uit</span></span> 
- <span data-ttu-id="a9974-1842">issue no</span><span class="sxs-lookup"><span data-stu-id="a9974-1842">issue no</span></span> 
- <span data-ttu-id="a9974-1843">issue number</span><span class="sxs-lookup"><span data-stu-id="a9974-1843">issue number</span></span> 
- <span data-ttu-id="a9974-1844">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1844">kaartidentificatienummer</span></span> 
- <span data-ttu-id="a9974-1845">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1845">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="a9974-1846">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1846">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="a9974-1847">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="a9974-1847">kwestieaantal</span></span> 
- <span data-ttu-id="a9974-1848">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1848">no.</span></span> <span data-ttu-id="a9974-1849">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="a9974-1849">dell'edizione</span></span> 
- <span data-ttu-id="a9974-1850">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1850">no.</span></span> <span data-ttu-id="a9974-1851">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="a9974-1851">di sicurezza</span></span> 
- <span data-ttu-id="a9974-1852">numero de securite</span><span class="sxs-lookup"><span data-stu-id="a9974-1852">numero de securite</span></span> 
- <span data-ttu-id="a9974-1853">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="a9974-1853">numero de verificacao</span></span> 
- <span data-ttu-id="a9974-1854">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="a9974-1854">numero dell'edizione</span></span> 
- <span data-ttu-id="a9974-1855">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="a9974-1855">numero di identificazione della</span></span> 
- <span data-ttu-id="a9974-1856">scheda</span><span class="sxs-lookup"><span data-stu-id="a9974-1856">scheda</span></span> 
- <span data-ttu-id="a9974-1857">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="a9974-1857">numero di sicurezza</span></span> 
- <span data-ttu-id="a9974-1858">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="a9974-1858">numero van veiligheid</span></span> 
- <span data-ttu-id="a9974-1859">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="a9974-1859">numéro de sécurité</span></span> 
- <span data-ttu-id="a9974-1860">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a9974-1860">nº autorizzazione</span></span> 
- <span data-ttu-id="a9974-1861">número de verificação</span><span class="sxs-lookup"><span data-stu-id="a9974-1861">número de verificação</span></span> 
- <span data-ttu-id="a9974-1862">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="a9974-1862">perno il blocco</span></span> 
- <span data-ttu-id="a9974-1863">pin block</span><span class="sxs-lookup"><span data-stu-id="a9974-1863">pin block</span></span> 
- <span data-ttu-id="a9974-1864">prufziffer</span><span class="sxs-lookup"><span data-stu-id="a9974-1864">prufziffer</span></span> 
- <span data-ttu-id="a9974-1865">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="a9974-1865">prüfziffer</span></span> 
- <span data-ttu-id="a9974-1866">security code</span><span class="sxs-lookup"><span data-stu-id="a9974-1866">security code</span></span> 
- <span data-ttu-id="a9974-1867">security no</span><span class="sxs-lookup"><span data-stu-id="a9974-1867">security no</span></span> 
- <span data-ttu-id="a9974-1868">security number</span><span class="sxs-lookup"><span data-stu-id="a9974-1868">security number</span></span> 
- <span data-ttu-id="a9974-1869">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="a9974-1869">sicherheits kode</span></span> 
- <span data-ttu-id="a9974-1870">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="a9974-1870">sicherheitscode</span></span> 
- <span data-ttu-id="a9974-1871">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1871">sicherheitsnummer</span></span> 
- <span data-ttu-id="a9974-1872">speldblok</span><span class="sxs-lookup"><span data-stu-id="a9974-1872">speldblok</span></span> 
- <span data-ttu-id="a9974-1873">veiligheid 번호:</span><span class="sxs-lookup"><span data-stu-id="a9974-1873">veiligheid nr</span></span> 
- <span data-ttu-id="a9974-1874">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="a9974-1874">veiligheidsaantal</span></span> 
- <span data-ttu-id="a9974-1875">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="a9974-1875">veiligheidscode</span></span> 
- <span data-ttu-id="a9974-1876">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1876">veiligheidsnummer</span></span> 
- <span data-ttu-id="a9974-1877">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="a9974-1877">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="a9974-1878">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="a9974-1878">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="a9974-1879">ablauf</span><span class="sxs-lookup"><span data-stu-id="a9974-1879">ablauf</span></span> 
- <span data-ttu-id="a9974-1880">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="a9974-1880">data de expiracao</span></span> 
- <span data-ttu-id="a9974-1881">data de expiração</span><span class="sxs-lookup"><span data-stu-id="a9974-1881">data de expiração</span></span> 
- <span data-ttu-id="a9974-1882">data del exp</span><span class="sxs-lookup"><span data-stu-id="a9974-1882">data del exp</span></span> 
- <span data-ttu-id="a9974-1883">data di exp</span><span class="sxs-lookup"><span data-stu-id="a9974-1883">data di exp</span></span> 
- <span data-ttu-id="a9974-1884">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="a9974-1884">data di scadenza</span></span> 
- <span data-ttu-id="a9974-1885">data em que expira</span><span class="sxs-lookup"><span data-stu-id="a9974-1885">data em que expira</span></span> 
- <span data-ttu-id="a9974-1886">data scad</span><span class="sxs-lookup"><span data-stu-id="a9974-1886">data scad</span></span> 
- <span data-ttu-id="a9974-1887">data scadenza</span><span class="sxs-lookup"><span data-stu-id="a9974-1887">data scadenza</span></span> 
- <span data-ttu-id="a9974-1888">date de validité</span><span class="sxs-lookup"><span data-stu-id="a9974-1888">date de validité</span></span> 
- <span data-ttu-id="a9974-1889">datum afloop</span><span class="sxs-lookup"><span data-stu-id="a9974-1889">datum afloop</span></span> 
- <span data-ttu-id="a9974-1890">datum van exp</span><span class="sxs-lookup"><span data-stu-id="a9974-1890">datum van exp</span></span> 
- <span data-ttu-id="a9974-1891">de afloop</span><span class="sxs-lookup"><span data-stu-id="a9974-1891">de afloop</span></span> 
- <span data-ttu-id="a9974-1892">espira</span><span class="sxs-lookup"><span data-stu-id="a9974-1892">espira</span></span> 
- <span data-ttu-id="a9974-1893">espira</span><span class="sxs-lookup"><span data-stu-id="a9974-1893">espira</span></span> 
- <span data-ttu-id="a9974-1894">exp date</span><span class="sxs-lookup"><span data-stu-id="a9974-1894">exp date</span></span> 
- <span data-ttu-id="a9974-1895">exp datum</span><span class="sxs-lookup"><span data-stu-id="a9974-1895">exp datum</span></span> 
- <span data-ttu-id="a9974-1896">행사</span><span class="sxs-lookup"><span data-stu-id="a9974-1896">expiration</span></span> 
- <span data-ttu-id="a9974-1897">예정</span><span class="sxs-lookup"><span data-stu-id="a9974-1897">expire</span></span> 
- <span data-ttu-id="a9974-1898">expires</span><span class="sxs-lookup"><span data-stu-id="a9974-1898">expires</span></span> 
- <span data-ttu-id="a9974-1899">만료</span><span class="sxs-lookup"><span data-stu-id="a9974-1899">expiry</span></span> 
- <span data-ttu-id="a9974-1900">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="a9974-1900">fecha de expiracion</span></span> 
- <span data-ttu-id="a9974-1901">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="a9974-1901">fecha de venc</span></span> 
- <span data-ttu-id="a9974-1902">gultig bis</span><span class="sxs-lookup"><span data-stu-id="a9974-1902">gultig bis</span></span> 
- <span data-ttu-id="a9974-1903">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="a9974-1903">gultigkeitsdatum</span></span> 
- <span data-ttu-id="a9974-1904">gültig bis</span><span class="sxs-lookup"><span data-stu-id="a9974-1904">gültig bis</span></span> 
- <span data-ttu-id="a9974-1905">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="a9974-1905">gültigkeitsdatum</span></span> 
- <span data-ttu-id="a9974-1906">la scadenza</span><span class="sxs-lookup"><span data-stu-id="a9974-1906">la scadenza</span></span> 
- <span data-ttu-id="a9974-1907">scadenza</span><span class="sxs-lookup"><span data-stu-id="a9974-1907">scadenza</span></span> 
- <span data-ttu-id="a9974-1908">valable</span><span class="sxs-lookup"><span data-stu-id="a9974-1908">valable</span></span> 
- <span data-ttu-id="a9974-1909">유효한 ade</span><span class="sxs-lookup"><span data-stu-id="a9974-1909">validade</span></span> 
- <span data-ttu-id="a9974-1910">valido hasta</span><span class="sxs-lookup"><span data-stu-id="a9974-1910">valido hasta</span></span> 
- <span data-ttu-id="a9974-1911">valor</span><span class="sxs-lookup"><span data-stu-id="a9974-1911">valor</span></span> 
- <span data-ttu-id="a9974-1912">venc</span><span class="sxs-lookup"><span data-stu-id="a9974-1912">venc</span></span> 
- <span data-ttu-id="a9974-1913">vencimento</span><span class="sxs-lookup"><span data-stu-id="a9974-1913">vencimento</span></span> 
- <span data-ttu-id="a9974-1914">vencimiento</span><span class="sxs-lookup"><span data-stu-id="a9974-1914">vencimiento</span></span> 
- <span data-ttu-id="a9974-1915">verloopt</span><span class="sxs-lookup"><span data-stu-id="a9974-1915">verloopt</span></span> 
- <span data-ttu-id="a9974-1916">vervaldag</span><span class="sxs-lookup"><span data-stu-id="a9974-1916">vervaldag</span></span> 
- <span data-ttu-id="a9974-1917">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="a9974-1917">vervaldatum</span></span> 
- <span data-ttu-id="a9974-1918">vto</span><span class="sxs-lookup"><span data-stu-id="a9974-1918">vto</span></span> 
- <span data-ttu-id="a9974-1919">válido hasta</span><span class="sxs-lookup"><span data-stu-id="a9974-1919">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="a9974-1920">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1920">EU Driver's License Number</span></span>

<span data-ttu-id="a9974-1921">자세한 내용은 [EU 운전 면허 번호 중요 정보 유형을](eu-driver-s-license-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a9974-1921">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="a9974-1922">EU 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1922">EU National Identification Number</span></span>

<span data-ttu-id="a9974-1923">자세한 내용은 [EU 국가 식별 번호 중요 한 정보 유형을](eu-national-identification-number.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a9974-1923">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="a9974-1924">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1924">EU Passport Number</span></span>

<span data-ttu-id="a9974-1925">자세한 내용은 [EU Passport 번호 중요 한 정보 유형을](eu-passport-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a9974-1925">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="a9974-1926">EU 주민 등록 번호 또는 동등한 ID</span><span class="sxs-lookup"><span data-stu-id="a9974-1926">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="a9974-1927">자세한 내용은 [EU 주민 등록 번호 또는 동등한 ID 중요 정보 유형을](eu-social-security-number-or-equivalent-id.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a9974-1927">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="a9974-1928">EU 세금 확인 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1928">EU Tax Identification Number</span></span>

<span data-ttu-id="a9974-1929">자세한 내용은 [EU 세금 식별 번호 중요 한 정보 유형을](eu-tax-identification-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a9974-1929">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="a9974-1930">핀란드 국가 ID</span><span class="sxs-lookup"><span data-stu-id="a9974-1930">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1931">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1931">Format</span></span>

<span data-ttu-id="a9974-1932">세기를 나타내는 6자리 숫자와 문자, 3자리 숫자와 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1932">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1933">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1933">Pattern</span></span>

<span data-ttu-id="a9974-1934">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1934">Pattern must include all of the following:</span></span>
- <span data-ttu-id="a9974-1935">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1935">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="a9974-1936">세기 표시('-', '+' 또는 'a')</span><span class="sxs-lookup"><span data-stu-id="a9974-1936">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="a9974-1937">3자리 개인 ID 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1937">Three-digit personal identification number</span></span> 
- <span data-ttu-id="a9974-1938">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-1938">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1939">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1939">Checksum</span></span>

<span data-ttu-id="a9974-1940">예</span><span class="sxs-lookup"><span data-stu-id="a9974-1940">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1941">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1941">Definition</span></span>

<span data-ttu-id="a9974-1942">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1942">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1943">Func_finnish_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1943">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1944">Keyword_finnish_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1944">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="a9974-1945">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1945">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-1946">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1946">Keywords</span></span>

- <span data-ttu-id="a9974-1947">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="a9974-1947">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="a9974-1948">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="a9974-1948">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="a9974-1949">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="a9974-1949">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="a9974-1950">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="a9974-1950">Personbeteckning</span></span>
- <span data-ttu-id="a9974-1951">Personnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-1951">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="a9974-1952">핀란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1952">Finland Passport Number</span></span>

<span data-ttu-id="a9974-1953">9 개의 문자 및 숫자 패턴 조합 형식 조합: 두 문자 (대/소문자 구분 안 함) 7 자리 체크섬 정의 없음 DLP 정책은이 유형의 중요 한 정보를 검색 한 것으로,이에 따라 300 문자의 근사: 정규식 Regex_finland_passport_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1953">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="a9974-1954">Keyword_finland_passport_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1954">A keyword from Keyword_finland_passport_number is found.</span></span>
<span data-ttu-id="a9974-1955"><!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="a9974-1955"></span></span>
<span data-ttu-id="a9974-1956">passport Keyword_finland_passport_number 키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1956">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="a9974-1957">프랑스 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1957">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1958">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1958">Format</span></span>

<span data-ttu-id="a9974-1959">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1959">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1960">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1960">Pattern</span></span>

<span data-ttu-id="a9974-1961">비슷한 패턴(예: 프랑스 전화 번호)을 무시하기 위한 유효성 검사 기능을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1961">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1962">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1962">Checksum</span></span>

<span data-ttu-id="a9974-1963">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-1963">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1964">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1964">Definition</span></span>

<span data-ttu-id="a9974-1965">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1965">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1966">Func_french_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1966">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-1967">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1967">At least one of the following is true:</span></span>
- <span data-ttu-id="a9974-1968">Keyword_french_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1968">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="a9974-1969">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1969">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-1970">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1970">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="a9974-1971">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="a9974-1971">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="a9974-1972">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a9974-1972">drivers licence</span></span>
- <span data-ttu-id="a9974-1973">drivers license</span><span class="sxs-lookup"><span data-stu-id="a9974-1973">drivers license</span></span>
- <span data-ttu-id="a9974-1974">driving licence</span><span class="sxs-lookup"><span data-stu-id="a9974-1974">driving licence</span></span>
- <span data-ttu-id="a9974-1975">driving license</span><span class="sxs-lookup"><span data-stu-id="a9974-1975">driving license</span></span>
- <span data-ttu-id="a9974-1976">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a9974-1976">permis de conduire</span></span>
- <span data-ttu-id="a9974-1977">licence number</span><span class="sxs-lookup"><span data-stu-id="a9974-1977">licence number</span></span>
- <span data-ttu-id="a9974-1978">license number</span><span class="sxs-lookup"><span data-stu-id="a9974-1978">license number</span></span>
- <span data-ttu-id="a9974-1979">licence numbers</span><span class="sxs-lookup"><span data-stu-id="a9974-1979">licence numbers</span></span>
- <span data-ttu-id="a9974-1980">license numbers</span><span class="sxs-lookup"><span data-stu-id="a9974-1980">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="a9974-1981">프랑스 국가 ID 카드(CNI)</span><span class="sxs-lookup"><span data-stu-id="a9974-1981">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1982">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1982">Format</span></span>

<span data-ttu-id="a9974-1983">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1983">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1984">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1984">Pattern</span></span>

<span data-ttu-id="a9974-1985">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1985">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-1986">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-1986">Checksum</span></span>

<span data-ttu-id="a9974-1987">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-1987">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-1988">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-1988">Definition</span></span>

<span data-ttu-id="a9974-1989">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1989">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-1990">Regex_france_cni 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-1990">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-1991">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-1991">Keywords</span></span>

<span data-ttu-id="a9974-1992">없음</span><span class="sxs-lookup"><span data-stu-id="a9974-1992">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="a9974-1993">프랑스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-1993">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-1994">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-1994">Format</span></span>

<span data-ttu-id="a9974-1995">9자리 숫자 및 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-1995">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-1996">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-1996">Pattern</span></span>

<span data-ttu-id="a9974-1997">9자리 숫자 및 문자:</span><span class="sxs-lookup"><span data-stu-id="a9974-1997">Nine digits and letters:</span></span>
- <span data-ttu-id="a9974-1998">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-1998">Two digits</span></span> 
- <span data-ttu-id="a9974-1999">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-1999">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-2000">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2000">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2001">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2001">Checksum</span></span>

<span data-ttu-id="a9974-2002">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2002">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2003">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2003">Definition</span></span>

<span data-ttu-id="a9974-2004">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2005">Func_fr_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2005">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2006">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2006">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2007">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2007">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="a9974-2008">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-2008">Keyword_passport</span></span>

- <span data-ttu-id="a9974-2009">Passport Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2009">Passport Number</span></span>
- <span data-ttu-id="a9974-2010">Passport No</span><span class="sxs-lookup"><span data-stu-id="a9974-2010">Passport No</span></span>
- <span data-ttu-id="a9974-2011">Passport #</span><span class="sxs-lookup"><span data-stu-id="a9974-2011">Passport #</span></span>
- <span data-ttu-id="a9974-2012">여권</span><span class="sxs-lookup"><span data-stu-id="a9974-2012">Passport#</span></span>
- <span data-ttu-id="a9974-2013">PassportID</span><span class="sxs-lookup"><span data-stu-id="a9974-2013">PassportID</span></span>
- <span data-ttu-id="a9974-2014">Passportno</span><span class="sxs-lookup"><span data-stu-id="a9974-2014">Passportno</span></span>
- <span data-ttu-id="a9974-2015">passportnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-2015">passportnumber</span></span>
- <span data-ttu-id="a9974-2016">パスポート</span><span class="sxs-lookup"><span data-stu-id="a9974-2016">パスポート</span></span>
- <span data-ttu-id="a9974-2017">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2017">パスポート番号</span></span>
- <span data-ttu-id="a9974-2018">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="a9974-2018">パスポートのNum</span></span>
- <span data-ttu-id="a9974-2019">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="a9974-2019">パスポート ＃</span></span> 
- <span data-ttu-id="a9974-2020">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a9974-2020">Numéro de passeport</span></span>
- <span data-ttu-id="a9974-2021">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="a9974-2021">Passeport n °</span></span>
- <span data-ttu-id="a9974-2022">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="a9974-2022">Passeport Non</span></span>
- <span data-ttu-id="a9974-2023">Passeport #</span><span class="sxs-lookup"><span data-stu-id="a9974-2023">Passeport #</span></span>
- <span data-ttu-id="a9974-2024">포트 #</span><span class="sxs-lookup"><span data-stu-id="a9974-2024">Passeport#</span></span>
- <span data-ttu-id="a9974-2025">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="a9974-2025">PasseportNon</span></span>
- <span data-ttu-id="a9974-2026">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="a9974-2026">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="a9974-2027">프랑스 사회 보장 번호(INSEE)</span><span class="sxs-lookup"><span data-stu-id="a9974-2027">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2028">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2028">Format</span></span>

<span data-ttu-id="a9974-2029">15자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2029">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2030">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2030">Pattern</span></span>

<span data-ttu-id="a9974-2031">다음 두 패턴 중 하나가 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2031">Must match one of two patterns:</span></span>
- <span data-ttu-id="a9974-2032">13 자리 숫자와 공백 다음 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2032">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="a9974-2033">또는</span><span class="sxs-lookup"><span data-stu-id="a9974-2033">or</span></span>
- <span data-ttu-id="a9974-2034">15자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2034">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2035">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2035">Checksum</span></span>

<span data-ttu-id="a9974-2036">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2036">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2037">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2037">Definition</span></span>

<span data-ttu-id="a9974-2038">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2038">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2039">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2039">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2040">Keyword_fr_insee의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2040">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="a9974-2041">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2041">The checksum passes.</span></span>

<span data-ttu-id="a9974-2042">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2042">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2043">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2043">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2044">Keyword_fr_insee의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2044">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="a9974-2045">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2045">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2046">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2046">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="a9974-2047">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="a9974-2047">Keyword_fr_insee</span></span>

- <span data-ttu-id="a9974-2048">insee</span><span class="sxs-lookup"><span data-stu-id="a9974-2048">insee</span></span>
- <span data-ttu-id="a9974-2049">securité sociale</span><span class="sxs-lookup"><span data-stu-id="a9974-2049">securité sociale</span></span>
- <span data-ttu-id="a9974-2050">securite sociale</span><span class="sxs-lookup"><span data-stu-id="a9974-2050">securite sociale</span></span>
- <span data-ttu-id="a9974-2051">national id</span><span class="sxs-lookup"><span data-stu-id="a9974-2051">national id</span></span>
- <span data-ttu-id="a9974-2052">national identification</span><span class="sxs-lookup"><span data-stu-id="a9974-2052">national identification</span></span>
- <span data-ttu-id="a9974-2053">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="a9974-2053">numéro d'identité</span></span>
- <span data-ttu-id="a9974-2054">no d'identité</span><span class="sxs-lookup"><span data-stu-id="a9974-2054">no d'identité</span></span>
- <span data-ttu-id="a9974-2055">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-2055">no.</span></span> <span data-ttu-id="a9974-2056">d'identité</span><span class="sxs-lookup"><span data-stu-id="a9974-2056">d'identité</span></span>
- <span data-ttu-id="a9974-2057">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="a9974-2057">numero d'identite</span></span>
- <span data-ttu-id="a9974-2058">no d'identite</span><span class="sxs-lookup"><span data-stu-id="a9974-2058">no d'identite</span></span>
- <span data-ttu-id="a9974-2059">아니요.</span><span class="sxs-lookup"><span data-stu-id="a9974-2059">no.</span></span> <span data-ttu-id="a9974-2060">d'identite</span><span class="sxs-lookup"><span data-stu-id="a9974-2060">d'identite</span></span>
- <span data-ttu-id="a9974-2061">social security number</span><span class="sxs-lookup"><span data-stu-id="a9974-2061">social security number</span></span>
- <span data-ttu-id="a9974-2062">social security code</span><span class="sxs-lookup"><span data-stu-id="a9974-2062">social security code</span></span>
- <span data-ttu-id="a9974-2063">social insurance number</span><span class="sxs-lookup"><span data-stu-id="a9974-2063">social insurance number</span></span>
- <span data-ttu-id="a9974-2064">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="a9974-2064">le numéro d'identification nationale</span></span>
- <span data-ttu-id="a9974-2065">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="a9974-2065">d'identité nationale</span></span>
- <span data-ttu-id="a9974-2066">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="a9974-2066">numéro de sécurité sociale</span></span>
- <span data-ttu-id="a9974-2067">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="a9974-2067">le code de la sécurité sociale</span></span>
- <span data-ttu-id="a9974-2068">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="a9974-2068">numéro d'assurance sociale</span></span>
- <span data-ttu-id="a9974-2069">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="a9974-2069">numéro de sécu</span></span>
- <span data-ttu-id="a9974-2070">code sécu</span><span class="sxs-lookup"><span data-stu-id="a9974-2070">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="a9974-2071">독일 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2071">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2072">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2072">Format</span></span>

<span data-ttu-id="a9974-2073">11자리 숫자와 문자 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-2073">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2074">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2074">Pattern</span></span>

<span data-ttu-id="a9974-2075">11자리 숫자와 문자(대/소문자 구분 안 함):</span><span class="sxs-lookup"><span data-stu-id="a9974-2075">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="a9974-2076">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-2076">A digit or letter</span></span> 
- <span data-ttu-id="a9974-2077">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2077">Two digits</span></span> 
- <span data-ttu-id="a9974-2078">6자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-2078">Six digits or letters</span></span> 
- <span data-ttu-id="a9974-2079">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2079">A digit</span></span> 
- <span data-ttu-id="a9974-2080">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-2080">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2081">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2081">Checksum</span></span>

<span data-ttu-id="a9974-2082">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2083">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2083">Definition</span></span>

<span data-ttu-id="a9974-2084">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2084">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2085">Func_german_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2085">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2086">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2086">At least one of the following is true:</span></span>
    - <span data-ttu-id="a9974-2087">Keyword_german_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2087">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="a9974-2088">Keyword_german_drivers_license_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2088">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="a9974-2089">Keyword_german_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2089">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="a9974-2090">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2090">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2091">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2091">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="a9974-2092">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2092">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="a9974-2093">Führerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2093">Führerschein</span></span>
- <span data-ttu-id="a9974-2094">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2094">Fuhrerschein</span></span>
- <span data-ttu-id="a9974-2095">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2095">Fuehrerschein</span></span>
- <span data-ttu-id="a9974-2096">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2096">Führerscheinnummer</span></span>
- <span data-ttu-id="a9974-2097">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2097">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="a9974-2098">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2098">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="a9974-2099">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="a9974-2099">Führerschein-</span></span> 
- <span data-ttu-id="a9974-2100">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="a9974-2100">Fuhrerschein-</span></span> 
- <span data-ttu-id="a9974-2101">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="a9974-2101">Fuehrerschein-</span></span> 
- <span data-ttu-id="a9974-2102">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="a9974-2102">FührerscheinnummerNr</span></span>
- <span data-ttu-id="a9974-2103">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="a9974-2103">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="a9974-2104">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="a9974-2104">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="a9974-2105">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2105">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="a9974-2106">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2106">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="a9974-2107">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2107">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="a9974-2108">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="a9974-2108">Führerschein- Nr</span></span>
- <span data-ttu-id="a9974-2109">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="a9974-2109">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="a9974-2110">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="a9974-2110">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="a9974-2111">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2111">Führerschein- Klasse</span></span> 
- <span data-ttu-id="a9974-2112">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2112">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="a9974-2113">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2113">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="a9974-2114">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="a9974-2114">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="a9974-2115">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="a9974-2115">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="a9974-2116">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="a9974-2116">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="a9974-2117">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2117">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="a9974-2118">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2118">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="a9974-2119">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2119">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="a9974-2120">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="a9974-2120">Führerschein- Nr</span></span> 
- <span data-ttu-id="a9974-2121">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="a9974-2121">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="a9974-2122">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="a9974-2122">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="a9974-2123">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2123">Führerschein- Klasse</span></span> 
- <span data-ttu-id="a9974-2124">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2124">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="a9974-2125">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2125">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="a9974-2126">DL</span><span class="sxs-lookup"><span data-stu-id="a9974-2126">DL</span></span> 
- <span data-ttu-id="a9974-2127">된다</span><span class="sxs-lookup"><span data-stu-id="a9974-2127">DLS</span></span>
- <span data-ttu-id="a9974-2128">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-2128">Driv Lic</span></span> 
- <span data-ttu-id="a9974-2129">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="a9974-2129">Driv Licen</span></span> 
- <span data-ttu-id="a9974-2130">Driv License</span><span class="sxs-lookup"><span data-stu-id="a9974-2130">Driv License</span></span>
- <span data-ttu-id="a9974-2131">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-2131">Driv Licenses</span></span> 
- <span data-ttu-id="a9974-2132">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-2132">Driv Licence</span></span> 
- <span data-ttu-id="a9974-2133">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-2133">Driv Licences</span></span> 
- <span data-ttu-id="a9974-2134">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-2134">Driv Lic</span></span> 
- <span data-ttu-id="a9974-2135">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="a9974-2135">Driver Licen</span></span> 
- <span data-ttu-id="a9974-2136">Driver License</span><span class="sxs-lookup"><span data-stu-id="a9974-2136">Driver License</span></span> 
- <span data-ttu-id="a9974-2137">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-2137">Driver Licenses</span></span> 
- <span data-ttu-id="a9974-2138">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-2138">Driver Licence</span></span> 
- <span data-ttu-id="a9974-2139">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-2139">Driver Licences</span></span> 
- <span data-ttu-id="a9974-2140">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-2140">Drivers Lic</span></span> 
- <span data-ttu-id="a9974-2141">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="a9974-2141">Drivers Licen</span></span> 
- <span data-ttu-id="a9974-2142">Drivers License</span><span class="sxs-lookup"><span data-stu-id="a9974-2142">Drivers License</span></span> 
- <span data-ttu-id="a9974-2143">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-2143">Drivers Licenses</span></span> 
- <span data-ttu-id="a9974-2144">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-2144">Drivers Licence</span></span> 
- <span data-ttu-id="a9974-2145">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-2145">Drivers Licences</span></span> 
- <span data-ttu-id="a9974-2146">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-2146">Driver's Lic</span></span> 
- <span data-ttu-id="a9974-2147">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="a9974-2147">Driver's Licen</span></span> 
- <span data-ttu-id="a9974-2148">Driver's License</span><span class="sxs-lookup"><span data-stu-id="a9974-2148">Driver's License</span></span> 
- <span data-ttu-id="a9974-2149">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-2149">Driver's Licenses</span></span> 
- <span data-ttu-id="a9974-2150">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-2150">Driver's Licence</span></span> 
- <span data-ttu-id="a9974-2151">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-2151">Driver's Licences</span></span> 
- <span data-ttu-id="a9974-2152">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-2152">Driving Lic</span></span> 
- <span data-ttu-id="a9974-2153">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="a9974-2153">Driving Licen</span></span> 
- <span data-ttu-id="a9974-2154">Driving License</span><span class="sxs-lookup"><span data-stu-id="a9974-2154">Driving License</span></span> 
- <span data-ttu-id="a9974-2155">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-2155">Driving Licenses</span></span> 
- <span data-ttu-id="a9974-2156">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="a9974-2156">Driving Licence</span></span> 
- <span data-ttu-id="a9974-2157">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="a9974-2157">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="a9974-2158">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="a9974-2158">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="a9974-2159">veiligheid-Führerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2159">Nr-Führerschein</span></span> 
- <span data-ttu-id="a9974-2160">veiligheid-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2160">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="a9974-2161">veiligheid-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2161">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="a9974-2162">Führerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2162">No-Führerschein</span></span> 
- <span data-ttu-id="a9974-2163">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2163">No-Fuhrerschein</span></span> 
- <span data-ttu-id="a9974-2164">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2164">No-Fuehrerschein</span></span> 
- <span data-ttu-id="a9974-2165">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2165">N-Führerschein</span></span> 
- <span data-ttu-id="a9974-2166">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2166">N-Fuhrerschein</span></span> 
- <span data-ttu-id="a9974-2167">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2167">N-Fuehrerschein</span></span>
- <span data-ttu-id="a9974-2168">veiligheid-Führerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2168">Nr-Führerschein</span></span> 
- <span data-ttu-id="a9974-2169">veiligheid-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2169">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="a9974-2170">veiligheid-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2170">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="a9974-2171">Führerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2171">No-Führerschein</span></span> 
- <span data-ttu-id="a9974-2172">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2172">No-Fuhrerschein</span></span> 
- <span data-ttu-id="a9974-2173">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2173">No-Fuehrerschein</span></span> 
- <span data-ttu-id="a9974-2174">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2174">N-Führerschein</span></span> 
- <span data-ttu-id="a9974-2175">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2175">N-Fuhrerschein</span></span> 
- <span data-ttu-id="a9974-2176">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="a9974-2176">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="a9974-2177">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="a9974-2177">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="a9974-2178">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="a9974-2178">ausstellungsdatum</span></span>
- <span data-ttu-id="a9974-2179">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="a9974-2179">ausstellungsort</span></span>
- <span data-ttu-id="a9974-2180">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="a9974-2180">ausstellende behöde</span></span>
- <span data-ttu-id="a9974-2181">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="a9974-2181">ausstellende behorde</span></span>
- <span data-ttu-id="a9974-2182">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="a9974-2182">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="a9974-2183">독일 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2183">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2184">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2184">Format</span></span>

<span data-ttu-id="a9974-2185">10자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-2185">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2186">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2186">Pattern</span></span>

<span data-ttu-id="a9974-2187">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2187">Pattern must include all of the following:</span></span>
- <span data-ttu-id="a9974-2188">첫 번째 문자는 숫자 또는 (C, F, G, H, J, K) 집합의 문자임</span><span class="sxs-lookup"><span data-stu-id="a9974-2188">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="a9974-2189">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2189">Three digits</span></span> 
- <span data-ttu-id="a9974-2190">5자리 숫자 또는 (C, -H, J-N, P, R, T, V-Z) 집합의 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-2190">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="a9974-2191">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2191">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2192">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2192">Checksum</span></span>

<span data-ttu-id="a9974-2193">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2194">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2194">Definition</span></span>

<span data-ttu-id="a9974-2195">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2196">Func_german_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2196">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2197">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2197">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="a9974-2198">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2198">The checksum passes.</span></span>

<span data-ttu-id="a9974-2199">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2199">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2200">Func_german_passport_data 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2200">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2201">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2201">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="a9974-2202">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2202">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2203">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2203">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="a9974-2204">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-2204">Keyword_german_passport</span></span>

- <span data-ttu-id="a9974-2205">reisepass</span><span class="sxs-lookup"><span data-stu-id="a9974-2205">reisepass</span></span>
- <span data-ttu-id="a9974-2206">reisepasse</span><span class="sxs-lookup"><span data-stu-id="a9974-2206">reisepasse</span></span>
- <span data-ttu-id="a9974-2207">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2207">reisepassnummer</span></span>
- <span data-ttu-id="a9974-2208">여권</span><span class="sxs-lookup"><span data-stu-id="a9974-2208">passport</span></span>
- <span data-ttu-id="a9974-2209">passports</span><span class="sxs-lookup"><span data-stu-id="a9974-2209">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="a9974-2210">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="a9974-2210">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="a9974-2211">ge삼 부, tsdatum</span><span class="sxs-lookup"><span data-stu-id="a9974-2211">geburtsdatum</span></span>
- <span data-ttu-id="a9974-2212">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="a9974-2212">ausstellungsdatum</span></span>
- <span data-ttu-id="a9974-2213">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="a9974-2213">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="a9974-2214">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2214">Keyword_german_passport_number</span></span>

<span data-ttu-id="a9974-2215">Reisepass veiligheid-Reisepass</span><span class="sxs-lookup"><span data-stu-id="a9974-2215">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="a9974-2216">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="a9974-2216">Keyword_german_passport1</span></span>

<span data-ttu-id="a9974-2217">Reisepass-veiligheid</span><span class="sxs-lookup"><span data-stu-id="a9974-2217">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="a9974-2218">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="a9974-2218">Keyword_german_passport2</span></span>

<span data-ttu-id="a9974-2219">bnationalit</span><span class="sxs-lookup"><span data-stu-id="a9974-2219">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="a9974-2220">독일 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2220">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2221">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2221">Format</span></span>

<span data-ttu-id="a9974-2222">2010 년 11 월 1 일 이후: 9 개 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2222">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="a9974-2223">1 월 1987 년 10 월 31 일 (2010:10 자리 숫자)</span><span class="sxs-lookup"><span data-stu-id="a9974-2223">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2224">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2224">Pattern</span></span>

<span data-ttu-id="a9974-2225">2010년 11월 1일 이후:</span><span class="sxs-lookup"><span data-stu-id="a9974-2225">Since 1 November 2010:</span></span>
- <span data-ttu-id="a9974-2226">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2226">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-2227">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2227">Eight digits</span></span>

<span data-ttu-id="a9974-2228">1 년 4 월 1987 일 ~ 10 월 31 일까 지:</span><span class="sxs-lookup"><span data-stu-id="a9974-2228">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="a9974-2229">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2229">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2230">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2230">Checksum</span></span>

<span data-ttu-id="a9974-2231">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2232">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2232">Definition</span></span>

<span data-ttu-id="a9974-2233">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2233">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2234">정규식 Regex_germany_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2234">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2235">Keyword_germany_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2235">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2236">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2236">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="a9974-2237">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="a9974-2237">Keyword_germany_id_card</span></span>

- <span data-ttu-id="a9974-2238">Identity Card</span><span class="sxs-lookup"><span data-stu-id="a9974-2238">Identity Card</span></span>
- <span data-ttu-id="a9974-2239">ID</span><span class="sxs-lookup"><span data-stu-id="a9974-2239">ID</span></span>
- <span data-ttu-id="a9974-2240">확인과</span><span class="sxs-lookup"><span data-stu-id="a9974-2240">Identification</span></span>
- <span data-ttu-id="a9974-2241">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="a9974-2241">Personalausweis</span></span>
- <span data-ttu-id="a9974-2242">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2242">Identifizierungsnummer</span></span>
- <span data-ttu-id="a9974-2243">ausweis</span><span class="sxs-lookup"><span data-stu-id="a9974-2243">Ausweis</span></span>
- <span data-ttu-id="a9974-2244">Identifikation</span><span class="sxs-lookup"><span data-stu-id="a9974-2244">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="a9974-2245">그리스 국가 ID 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2245">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2246">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2246">Format</span></span>

<span data-ttu-id="a9974-2247">7-8자리 문자 및 숫자와 대시의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-2247">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2248">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2248">Pattern</span></span>

<span data-ttu-id="a9974-2249">7자리 문자 및 숫자(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="a9974-2249">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="a9974-2250">1개 문자(그리스어 알파벳의 임의 문자) </span><span class="sxs-lookup"><span data-stu-id="a9974-2250">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="a9974-2251">대시 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-2251">A dash</span></span> 
- <span data-ttu-id="a9974-2252">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2252">Six digits</span></span>

<span data-ttu-id="a9974-2253">8자리 문자와 숫자(새로운 형식):</span><span class="sxs-lookup"><span data-stu-id="a9974-2253">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="a9974-2254">그리스어 및 라틴어 알파벳 둘 다에 해당 대문자가 포함된 2개 문자(ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="a9974-2254">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="a9974-2255">대시 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-2255">A dash</span></span> 
- <span data-ttu-id="a9974-2256">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2256">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2257">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2257">Checksum</span></span>

<span data-ttu-id="a9974-2258">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2258">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2259">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2259">Definition</span></span>

<span data-ttu-id="a9974-2260">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2261">정규식 Regex_greece_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2261">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2262">Keyword_greece_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2262">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2263">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2263">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="a9974-2264">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="a9974-2264">Keyword_greece_id_card</span></span>

- <span data-ttu-id="a9974-2265">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="a9974-2265">Greek identity Card</span></span>
- <span data-ttu-id="a9974-2266">Tautotita</span><span class="sxs-lookup"><span data-stu-id="a9974-2266">Tautotita</span></span>
- <span data-ttu-id="a9974-2267">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="a9974-2267">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="a9974-2268">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="a9974-2268">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="a9974-2269">HKID(홍콩 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2269">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2270">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2270">Format</span></span>

<span data-ttu-id="a9974-2271">8-9자리 문자 및 숫자와 마지막 문자를 선택적 괄호로 묶어서 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-2271">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2272">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2272">Pattern</span></span>

<span data-ttu-id="a9974-2273">8-9자리 문자 조합:</span><span class="sxs-lookup"><span data-stu-id="a9974-2273">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="a9974-2274">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2274">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-2275">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2275">Six digits</span></span> 
- <span data-ttu-id="a9974-2276">검사 숫자에 해당하고 선택적으로 괄호로 묶는 마지막 문자(임의 숫자 또는 문자 A)</span><span class="sxs-lookup"><span data-stu-id="a9974-2276">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2277">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2277">Checksum</span></span>

<span data-ttu-id="a9974-2278">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2278">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2279">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2279">Definition</span></span>

<span data-ttu-id="a9974-2280">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2281">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2281">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2282">Keyword_hong_kong_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2282">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="a9974-2283">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2283">The checksum passes.</span></span>

<span data-ttu-id="a9974-2284">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2284">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2285">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2285">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2286">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2286">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2287">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2287">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="a9974-2288">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="a9974-2288">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="a9974-2289">홍콩 특별 식별자 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2289">hong kong identity card</span></span>
- <span data-ttu-id="a9974-2290">HKIDC</span><span class="sxs-lookup"><span data-stu-id="a9974-2290">HKIDC</span></span>
- <span data-ttu-id="a9974-2291">id card</span><span class="sxs-lookup"><span data-stu-id="a9974-2291">id card</span></span>
- <span data-ttu-id="a9974-2292">identity card</span><span class="sxs-lookup"><span data-stu-id="a9974-2292">identity card</span></span>
- <span data-ttu-id="a9974-2293">zh-hk id 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2293">hk identity card</span></span>
- <span data-ttu-id="a9974-2294">홍콩 id</span><span class="sxs-lookup"><span data-stu-id="a9974-2294">hong kong id</span></span>
- <span data-ttu-id="a9974-2295">香港身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2295">香港身份證</span></span>
- <span data-ttu-id="a9974-2296">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2296">香港永久性居民身份證</span></span>
- <span data-ttu-id="a9974-2297">身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2297">身份證</span></span>
- <span data-ttu-id="a9974-2298">身份証</span><span class="sxs-lookup"><span data-stu-id="a9974-2298">身份証</span></span>
- <span data-ttu-id="a9974-2299">身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-2299">身分證</span></span>
- <span data-ttu-id="a9974-2300">身分証</span><span class="sxs-lookup"><span data-stu-id="a9974-2300">身分証</span></span>
- <span data-ttu-id="a9974-2301">香港身份証</span><span class="sxs-lookup"><span data-stu-id="a9974-2301">香港身份証</span></span>
- <span data-ttu-id="a9974-2302">香港身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-2302">香港身分證</span></span>
- <span data-ttu-id="a9974-2303">香港身分証</span><span class="sxs-lookup"><span data-stu-id="a9974-2303">香港身分証</span></span>
- <span data-ttu-id="a9974-2304">香港身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2304">香港身份證</span></span>
- <span data-ttu-id="a9974-2305">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2305">香港居民身份證</span></span>
- <span data-ttu-id="a9974-2306">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="a9974-2306">香港居民身份証</span></span>
- <span data-ttu-id="a9974-2307">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-2307">香港居民身分證</span></span>
- <span data-ttu-id="a9974-2308">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="a9974-2308">香港居民身分証</span></span>
- <span data-ttu-id="a9974-2309">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="a9974-2309">香港永久性居民身份証</span></span>
- <span data-ttu-id="a9974-2310">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-2310">香港永久性居民身分證</span></span>
- <span data-ttu-id="a9974-2311">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="a9974-2311">香港永久性居民身分証</span></span>
- <span data-ttu-id="a9974-2312">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2312">香港永久性居民身份證</span></span>
- <span data-ttu-id="a9974-2313">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2313">香港非永久性居民身份證</span></span>
- <span data-ttu-id="a9974-2314">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="a9974-2314">香港非永久性居民身份証</span></span>
- <span data-ttu-id="a9974-2315">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-2315">香港非永久性居民身分證</span></span>
- <span data-ttu-id="a9974-2316">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="a9974-2316">香港非永久性居民身分証</span></span>
- <span data-ttu-id="a9974-2317">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2317">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="a9974-2318">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="a9974-2318">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="a9974-2319">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-2319">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="a9974-2320">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="a9974-2320">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="a9974-2321">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-2321">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="a9974-2322">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="a9974-2322">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="a9974-2323">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-2323">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="a9974-2324">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="a9974-2324">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="a9974-2325">인도 PAN(영구 계정 번호)</span><span class="sxs-lookup"><span data-stu-id="a9974-2325">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2326">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2326">Format</span></span>

<span data-ttu-id="a9974-2327">10자리 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2327">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2328">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2328">Pattern</span></span>

<span data-ttu-id="a9974-2329">10자리 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2329">10 letters or digits:</span></span>
- <span data-ttu-id="a9974-2330">5개 문자(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="a9974-2330">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-2331">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2331">Four digits</span></span> 
- <span data-ttu-id="a9974-2332">알파벳 검사 숫자에 해당하는 문자 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-2332">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2333">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2333">Checksum</span></span>

<span data-ttu-id="a9974-2334">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2335">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2335">Definition</span></span>

<span data-ttu-id="a9974-2336">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2337">정규식 Regex_india_permanent_account_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2337">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2338">Keyword_india_permanent_account_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2338">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="a9974-2339">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2339">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2340">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2340">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="a9974-2341">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2341">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="a9974-2342">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2342">Permanent Account Number</span></span> 
- <span data-ttu-id="a9974-2343">확대</span><span class="sxs-lookup"><span data-stu-id="a9974-2343">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="a9974-2344">인도 고유 ID(Aadhaar) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2344">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2345">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2345">Format</span></span>

<span data-ttu-id="a9974-2346">선택적 공백 또는 대시를 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2346">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2347">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2347">Pattern</span></span>

<span data-ttu-id="a9974-2348">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2348">12 digits:</span></span>
- <span data-ttu-id="a9974-2349">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2349">Four digits</span></span> 
- <span data-ttu-id="a9974-2350">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="a9974-2350">An optional space or dash</span></span> 
- <span data-ttu-id="a9974-2351">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2351">Four digits</span></span> 
- <span data-ttu-id="a9974-2352">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="a9974-2352">An optional space or dash</span></span> 
- <span data-ttu-id="a9974-2353">검사 숫자에 해당하는 마지막 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2353">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2354">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2354">Checksum</span></span>

<span data-ttu-id="a9974-2355">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2355">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2356">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2356">Definition</span></span>

<span data-ttu-id="a9974-2357">DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2357">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="a9974-2358">Keyword_india_aadhar에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2358">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="a9974-2359">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2359">The checksum passes.</span></span>
<span data-ttu-id="a9974-2360">DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="a9974-2361">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2361">The checksum passes.</span></span>
<span data-ttu-id="a9974-2362"><!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="a9974-2362"></span></span>

### <a name="keywords"></a><span data-ttu-id="a9974-2363">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2363">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="a9974-2364">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="a9974-2364">Keyword_india_aadhar</span></span>
- <span data-ttu-id="a9974-2365">Aadhar</span><span class="sxs-lookup"><span data-stu-id="a9974-2365">Aadhar</span></span>
- <span data-ttu-id="a9974-2366">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="a9974-2366">Aadhaar</span></span>
- <span data-ttu-id="a9974-2367">UID</span><span class="sxs-lookup"><span data-stu-id="a9974-2367">UID</span></span>
- <span data-ttu-id="a9974-2368">आधार</span><span class="sxs-lookup"><span data-stu-id="a9974-2368">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="a9974-2369">인도네시아 ID 카드(KTP) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2369">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2370">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2370">Format</span></span>

<span data-ttu-id="a9974-2371">선택적으로 마침표를 포함하는 16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2371">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2372">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2372">Pattern</span></span>

<span data-ttu-id="a9974-2373">16자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2373">16 digits:</span></span>
- <span data-ttu-id="a9974-2374">2자리 시/도 코드 </span><span class="sxs-lookup"><span data-stu-id="a9974-2374">Two-digit province code</span></span> 
- <span data-ttu-id="a9974-2375">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="a9974-2375">A period (optional)</span></span> 
- <span data-ttu-id="a9974-2376">2자리 지역 또는 구/군/시 코드 </span><span class="sxs-lookup"><span data-stu-id="a9974-2376">Two-digit regency or city code</span></span> 
- <span data-ttu-id="a9974-2377">2자리 소구역 코드 </span><span class="sxs-lookup"><span data-stu-id="a9974-2377">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="a9974-2378">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="a9974-2378">A period (optional)</span></span> 
- <span data-ttu-id="a9974-2379">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-2379">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="a9974-2380">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="a9974-2380">A period (optional)</span></span> 
- <span data-ttu-id="a9974-2381">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2381">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2382">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2382">Checksum</span></span>

<span data-ttu-id="a9974-2383">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2383">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2384">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2384">Definition</span></span>

<span data-ttu-id="a9974-2385">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2386">정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2386">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2387">Keyword_indonesia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2387">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="a9974-2388">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2388">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2389">정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2389">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2390">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2390">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="a9974-2391">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="a9974-2391">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="a9974-2392">KTP</span><span class="sxs-lookup"><span data-stu-id="a9974-2392">KTP</span></span>
- <span data-ttu-id="a9974-2393">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="a9974-2393">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="a9974-2394">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="a9974-2394">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="a9974-2395">IBAN(국제 은행 계좌 번호)</span><span class="sxs-lookup"><span data-stu-id="a9974-2395">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2396">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2396">Format</span></span>

<span data-ttu-id="a9974-2397">국가 코드 (두 문자) + 검사 숫자 (2 자리 숫자)와 bban 숫자 (최대 30 자)</span><span class="sxs-lookup"><span data-stu-id="a9974-2397">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2398">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2398">Pattern</span></span>

<span data-ttu-id="a9974-2399">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2399">Pattern must include all of the following:</span></span>

- <span data-ttu-id="a9974-2400">두 글자로 된 국가 코드</span><span class="sxs-lookup"><span data-stu-id="a9974-2400">Two-letter country code</span></span>
- <span data-ttu-id="a9974-2401">두 개의 검사 숫자 (선택적 공백)</span><span class="sxs-lookup"><span data-stu-id="a9974-2401">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="a9974-2402">1-7 개 문자 또는 숫자의 그룹 (공백으로 구분 가능)</span><span class="sxs-lookup"><span data-stu-id="a9974-2402">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="a9974-2403">1-3 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2403">1-3 letters or digits</span></span>

<span data-ttu-id="a9974-2404">각 국가의 형식은 약간 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2404">The format for each country is slightly different.</span></span> <span data-ttu-id="a9974-2405">iban 중요 한 정보 유형은 다음과 같은 60 국가를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2405">The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="a9974-2406">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, kw, hu,, to,,, fr,,, i,,, ie, il, is,, l,, 5, 60, md, me, mk, e, mt, mu , nl-nl, no, pl, pt, ro, rs, sa, se, si,, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="a9974-2406">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2407">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2407">Checksum</span></span>

<span data-ttu-id="a9974-2408">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2408">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2409">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2409">Definition</span></span>

<span data-ttu-id="a9974-2410">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2410">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2411">Func_iban 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2411">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2412">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2412">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2413">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2413">Keywords</span></span>

<span data-ttu-id="a9974-2414">없음</span><span class="sxs-lookup"><span data-stu-id="a9974-2414">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="a9974-2415">IP 주소</span><span class="sxs-lookup"><span data-stu-id="a9974-2415">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2416">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2416">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="a9974-2417">IPv4</span><span class="sxs-lookup"><span data-stu-id="a9974-2417">IPv4:</span></span>
<span data-ttu-id="a9974-2418">IPv4 주소의 서식 있는 버전(마침표 있음) 및 서식 없는 버전(마침표 없음)으로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2418">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="a9974-2419">IPv6</span><span class="sxs-lookup"><span data-stu-id="a9974-2419">IPv6:</span></span>
<span data-ttu-id="a9974-2420">서식 있는(콜론 포함) IPv6 번호로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2420">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2421">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2421">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2422">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2422">Checksum</span></span>

<span data-ttu-id="a9974-2423">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2424">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2424">Definition</span></span>

<span data-ttu-id="a9974-2425">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2425">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2426">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2426">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2427">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2427">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="a9974-2428">IPv4의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2428">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2429">Regex_ipv4_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2429">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2430">Keyword_ipaddress의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2430">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="a9974-2431">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2431">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2432">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2432">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2433">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2433">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2434">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2434">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="a9974-2435">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="a9974-2435">Keyword_ipaddress</span></span>

- <span data-ttu-id="a9974-2436">IP(이 키워드는 대/소문자를 구분함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2436">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="a9974-2437">ip address</span><span class="sxs-lookup"><span data-stu-id="a9974-2437">ip address</span></span> 
- <span data-ttu-id="a9974-2438">ip addresses</span><span class="sxs-lookup"><span data-stu-id="a9974-2438">ip addresses</span></span>
- <span data-ttu-id="a9974-2439">internet protocol</span><span class="sxs-lookup"><span data-stu-id="a9974-2439">internet protocol</span></span>
- <span data-ttu-id="a9974-2440">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="a9974-2440">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="a9974-2441">Diseases의 국제 분류 (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="a9974-2441">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2442">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2442">Format</span></span>

<span data-ttu-id="a9974-2443">사전</span><span class="sxs-lookup"><span data-stu-id="a9974-2443">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2444">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2444">Pattern</span></span>

<span data-ttu-id="a9974-2445">Keyword</span><span class="sxs-lookup"><span data-stu-id="a9974-2445">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2446">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2446">Checksum</span></span>

<span data-ttu-id="a9974-2447">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2447">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2448">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2448">Definition</span></span>

<span data-ttu-id="a9974-2449">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2449">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2450">Dictionary_icd_10_cm에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2450">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="a9974-2451">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2451">Keywords</span></span>

<span data-ttu-id="a9974-2452">Dictionary_icd_10_cm 키워드 사전의 모든 용어 이며, [Diseases의 국제 분류, 10 번째 수정, 임상 수정 (icd-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604)을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2452">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="a9974-2453">이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2453">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="a9974-2454">Diseases의 국제 분류 (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="a9974-2454">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2455">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2455">Format</span></span>

<span data-ttu-id="a9974-2456">사전</span><span class="sxs-lookup"><span data-stu-id="a9974-2456">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2457">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2457">Pattern</span></span>

<span data-ttu-id="a9974-2458">Keyword</span><span class="sxs-lookup"><span data-stu-id="a9974-2458">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2459">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2459">Checksum</span></span>

<span data-ttu-id="a9974-2460">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2460">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2461">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2461">Definition</span></span>

<span data-ttu-id="a9974-2462">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2462">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2463">Dictionary_icd_9_cm에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2463">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2464">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2464">Keywords</span></span>

<span data-ttu-id="a9974-2465">[Diseases의 국가별 분류, 9 번째 버전의 임상 수정 (icd-9cm)](https://go.microsoft.com/fwlink/?linkid=852605)을 기반으로 하는 Dictionary_icd_9_cm 키워드 사전의 모든 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2465">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="a9974-2466">이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2466">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="a9974-2467">아일랜드 PPS(개인 공공 서비스) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2467">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2468">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2468">Format</span></span>

<span data-ttu-id="a9974-2469">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="a9974-2469">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="a9974-2470">7자리 숫자와 1-2개 문자 </span><span class="sxs-lookup"><span data-stu-id="a9974-2470">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="a9974-2471">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="a9974-2471">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="a9974-2472">7자리 숫자와 2개 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-2472">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2473">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2473">Pattern</span></span>

<span data-ttu-id="a9974-2474">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="a9974-2474">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="a9974-2475">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2475">Seven digits</span></span> 
- <span data-ttu-id="a9974-2476">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2476">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="a9974-2477">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="a9974-2477">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="a9974-2478">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2478">Seven digits</span></span> 
- <span data-ttu-id="a9974-2479">알파벳 검사 숫자에 해당하는 문자 1개(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="a9974-2479">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="a9974-2480">문자 "A" 또는 "H"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2480">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2481">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2481">Checksum</span></span>

<span data-ttu-id="a9974-2482">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2482">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2483">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2483">Definition</span></span>

<span data-ttu-id="a9974-2484">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2484">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2485">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2485">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2486">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2486">One of the following is true:</span></span>
    - <span data-ttu-id="a9974-2487">Keyword_ireland_pps에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2487">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="a9974-2488">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2488">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="a9974-2489">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2489">The checksum passes.</span></span>

<span data-ttu-id="a9974-2490">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2490">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2491">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2491">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2492">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2492">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2493">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2493">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="a9974-2494">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="a9974-2494">Keyword_ireland_pps</span></span>

- <span data-ttu-id="a9974-2495">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2495">Personal Public Service Number</span></span> 
- <span data-ttu-id="a9974-2496">PPS Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2496">PPS Number</span></span> 
- <span data-ttu-id="a9974-2497">PPS Num</span><span class="sxs-lookup"><span data-stu-id="a9974-2497">PPS Num</span></span> 
- <span data-ttu-id="a9974-2498">PPS No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2498">PPS No.</span></span> 
- <span data-ttu-id="a9974-2499">PPS #</span><span class="sxs-lookup"><span data-stu-id="a9974-2499">PPS #</span></span> 
- <span data-ttu-id="a9974-2500">.pps</span><span class="sxs-lookup"><span data-stu-id="a9974-2500">PPS#</span></span> 
- <span data-ttu-id="a9974-2501">ppsn</span><span class="sxs-lookup"><span data-stu-id="a9974-2501">PPSN</span></span> 
- <span data-ttu-id="a9974-2502">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="a9974-2502">Public Services Card</span></span> 
- <span data-ttu-id="a9974-2503">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="a9974-2503">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="a9974-2504">uimh</span><span class="sxs-lookup"><span data-stu-id="a9974-2504">Uimh.</span></span> <span data-ttu-id="a9974-2505">PSP</span><span class="sxs-lookup"><span data-stu-id="a9974-2505">PSP</span></span> 
- <span data-ttu-id="a9974-2506">PSP</span><span class="sxs-lookup"><span data-stu-id="a9974-2506">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="a9974-2507">이스라엘 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2507">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2508">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2508">Format</span></span>

<span data-ttu-id="a9974-2509">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2509">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2510">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2510">Pattern</span></span>

<span data-ttu-id="a9974-2511">서식이</span><span class="sxs-lookup"><span data-stu-id="a9974-2511">Formatted:</span></span>
- <span data-ttu-id="a9974-2512">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2512">Two digits</span></span> 
- <span data-ttu-id="a9974-2513">대시 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-2513">A dash</span></span> 
- <span data-ttu-id="a9974-2514">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2514">Three digits</span></span> 
- <span data-ttu-id="a9974-2515">대시 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-2515">A dash</span></span> 
- <span data-ttu-id="a9974-2516">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2516">Eight digits</span></span>

<span data-ttu-id="a9974-2517">서식</span><span class="sxs-lookup"><span data-stu-id="a9974-2517">Unformatted:</span></span>
- <span data-ttu-id="a9974-2518">13자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2518">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2519">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2519">Checksum</span></span>

<span data-ttu-id="a9974-2520">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2520">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2521">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2521">Definition</span></span>

<span data-ttu-id="a9974-2522">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2522">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2523">Regex_israel_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2523">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2524">Keyword_israel_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2524">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2525">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2525">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="a9974-2526">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2526">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="a9974-2527">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2527">Bank Account Number</span></span> 
- <span data-ttu-id="a9974-2528">Bank Account</span><span class="sxs-lookup"><span data-stu-id="a9974-2528">Bank Account</span></span> 
- <span data-ttu-id="a9974-2529">Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2529">Account Number</span></span> 
- <span data-ttu-id="a9974-2530">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="a9974-2530">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="a9974-2531">이스라엘 국가 ID</span><span class="sxs-lookup"><span data-stu-id="a9974-2531">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2532">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2532">Format</span></span>

<span data-ttu-id="a9974-2533">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2534">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2534">Pattern</span></span>

<span data-ttu-id="a9974-2535">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2536">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2536">Checksum</span></span>

<span data-ttu-id="a9974-2537">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2537">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2538">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2538">Definition</span></span>

<span data-ttu-id="a9974-2539">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2540">Func_israeli_national_id_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2540">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2541">Keyword_Israel_National_ID의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2541">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="a9974-2542">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2542">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2543">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2543">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="a9974-2544">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="a9974-2544">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="a9974-2545">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="a9974-2545">מספר זהות</span></span> 
- <span data-ttu-id="a9974-2546">National ID Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2546">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="a9974-2547">이탈리아 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2547">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2548">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2548">Format</span></span>

<span data-ttu-id="a9974-2549">10개의 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-2549">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2550">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2550">Pattern</span></span>

- <span data-ttu-id="a9974-2551">10개의 문자 및 숫자 조합:</span><span class="sxs-lookup"><span data-stu-id="a9974-2551">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="a9974-2552">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2552">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-2553">문자 "A" 또는 "V"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2553">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-2554">7개 문자(대/소문자 구분 안 함), 숫자 또는 밑줄 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-2554">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="a9974-2555">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2555">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2556">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2556">Checksum</span></span>

<span data-ttu-id="a9974-2557">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2557">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2558">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2558">Definition</span></span>

<span data-ttu-id="a9974-2559">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2559">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2560">Regex_italy_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2560">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2561">Keyword_italy_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2561">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2562">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2562">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="a9974-2563">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2563">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="a9974-2564">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="a9974-2564">numero di patente di guida</span></span> 
- <span data-ttu-id="a9974-2565">patente di guida</span><span class="sxs-lookup"><span data-stu-id="a9974-2565">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="a9974-2566">일본 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2566">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2567">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2567">Format</span></span>

<span data-ttu-id="a9974-2568">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2568">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2569">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2569">Pattern</span></span>

<span data-ttu-id="a9974-2570">은행 계좌 번호:</span><span class="sxs-lookup"><span data-stu-id="a9974-2570">Bank account number:</span></span>
- <span data-ttu-id="a9974-2571">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2571">Seven or eight digits</span></span>
- <span data-ttu-id="a9974-2572">은행 계좌 지점 코드:</span><span class="sxs-lookup"><span data-stu-id="a9974-2572">Bank account branch code:</span></span>
- <span data-ttu-id="a9974-2573">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2573">Four digits</span></span> 
- <span data-ttu-id="a9974-2574">공백 또는 대시(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a9974-2574">A space or dash (optional)</span></span> 
- <span data-ttu-id="a9974-2575">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2575">Three digits</span></span>

<span data-ttu-id="a9974-2576">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2576">Checksum</span></span>

<span data-ttu-id="a9974-2577">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2577">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2578">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2578">Definition</span></span>

<span data-ttu-id="a9974-2579">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2580">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2580">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2581">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2581">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="a9974-2582">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2582">One of the following is true:</span></span>
- <span data-ttu-id="a9974-2583">Func_jp_bank_account_branch_code 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2583">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2584">Keyword_jp_bank_branch_code의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2584">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="a9974-2585">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2586">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2586">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2587">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2587">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2588">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2588">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="a9974-2589">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="a9974-2589">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="a9974-2590">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2590">Checking Account Number</span></span> 
- <span data-ttu-id="a9974-2591">Checking Account</span><span class="sxs-lookup"><span data-stu-id="a9974-2591">Checking Account</span></span> 
- <span data-ttu-id="a9974-2592">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="a9974-2592">Checking Account #</span></span> 
- <span data-ttu-id="a9974-2593">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2593">Checking Acct Number</span></span> 
- <span data-ttu-id="a9974-2594">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="a9974-2594">Checking Acct #</span></span> 
- <span data-ttu-id="a9974-2595">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2595">Checking Acct No.</span></span> 
- <span data-ttu-id="a9974-2596">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2596">Checking Account No.</span></span> 
- <span data-ttu-id="a9974-2597">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2597">Bank Account Number</span></span> 
- <span data-ttu-id="a9974-2598">Bank Account</span><span class="sxs-lookup"><span data-stu-id="a9974-2598">Bank Account</span></span> 
- <span data-ttu-id="a9974-2599">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="a9974-2599">Bank Account #</span></span> 
- <span data-ttu-id="a9974-2600">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2600">Bank Acct Number</span></span> 
- <span data-ttu-id="a9974-2601">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="a9974-2601">Bank Acct #</span></span> 
- <span data-ttu-id="a9974-2602">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2602">Bank Acct No.</span></span> 
- <span data-ttu-id="a9974-2603">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2603">Bank Account No.</span></span> 
- <span data-ttu-id="a9974-2604">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2604">Savings Account Number</span></span> 
- <span data-ttu-id="a9974-2605">Savings Account</span><span class="sxs-lookup"><span data-stu-id="a9974-2605">Savings Account</span></span> 
- <span data-ttu-id="a9974-2606">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="a9974-2606">Savings Account #</span></span> 
- <span data-ttu-id="a9974-2607">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2607">Savings Acct Number</span></span> 
- <span data-ttu-id="a9974-2608">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="a9974-2608">Savings Acct #</span></span> 
- <span data-ttu-id="a9974-2609">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2609">Savings Acct No.</span></span> 
- <span data-ttu-id="a9974-2610">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2610">Savings Account No.</span></span> 
- <span data-ttu-id="a9974-2611">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2611">Debit Account Number</span></span> 
- <span data-ttu-id="a9974-2612">Debit Account</span><span class="sxs-lookup"><span data-stu-id="a9974-2612">Debit Account</span></span> 
- <span data-ttu-id="a9974-2613">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="a9974-2613">Debit Account #</span></span> 
- <span data-ttu-id="a9974-2614">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2614">Debit Acct Number</span></span> 
- <span data-ttu-id="a9974-2615">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="a9974-2615">Debit Acct #</span></span> 
- <span data-ttu-id="a9974-2616">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2616">Debit Acct No.</span></span> 
- <span data-ttu-id="a9974-2617">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2617">Debit Account No.</span></span> 
- <span data-ttu-id="a9974-2618">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="a9974-2618">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="a9974-2619">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="a9974-2619">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="a9974-2620">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="a9974-2620">＃勘定の確認</span></span> 
- <span data-ttu-id="a9974-2621">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="a9974-2621">勘定番号の確認</span></span> 
- <span data-ttu-id="a9974-2622">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="a9974-2622">口座番号の確認</span></span> 
- <span data-ttu-id="a9974-2623">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2623">銀行口座番号</span></span> 
- <span data-ttu-id="a9974-2624">銀行口座</span><span class="sxs-lookup"><span data-stu-id="a9974-2624">銀行口座</span></span> 
- <span data-ttu-id="a9974-2625">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="a9974-2625">銀行口座＃</span></span> 
- <span data-ttu-id="a9974-2626">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2626">銀行の勘定番号</span></span> 
- <span data-ttu-id="a9974-2627">銀行のacct #</span><span class="sxs-lookup"><span data-stu-id="a9974-2627">銀行のacct＃</span></span> 
- <span data-ttu-id="a9974-2628">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="a9974-2628">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="a9974-2629">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2629">銀行口座番号</span></span>
- <span data-ttu-id="a9974-2630">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2630">普通預金口座番号</span></span> 
- <span data-ttu-id="a9974-2631">預金口座</span><span class="sxs-lookup"><span data-stu-id="a9974-2631">預金口座</span></span> 
- <span data-ttu-id="a9974-2632">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="a9974-2632">貯蓄口座＃</span></span> 
- <span data-ttu-id="a9974-2633">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="a9974-2633">貯蓄勘定の数</span></span> 
- <span data-ttu-id="a9974-2634">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="a9974-2634">貯蓄勘定＃</span></span> 
- <span data-ttu-id="a9974-2635">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2635">貯蓄勘定番号</span></span> 
- <span data-ttu-id="a9974-2636">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2636">普通預金口座番号</span></span> 
- <span data-ttu-id="a9974-2637">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2637">引き落とし口座番号</span></span> 
- <span data-ttu-id="a9974-2638">口座番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2638">口座番号</span></span> 
- <span data-ttu-id="a9974-2639">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="a9974-2639">口座番号＃</span></span> 
- <span data-ttu-id="a9974-2640">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2640">デビットのacct番号</span></span> 
- <span data-ttu-id="a9974-2641">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="a9974-2641">デビット勘定＃</span></span> 
- <span data-ttu-id="a9974-2642">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2642">デビットACCTの番号</span></span> 
- <span data-ttu-id="a9974-2643">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2643">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="a9974-2644">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="a9974-2644">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="a9974-2645">Otemachi</span><span class="sxs-lookup"><span data-stu-id="a9974-2645">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="a9974-2646">일본 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2646">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2647">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2647">Format</span></span>

<span data-ttu-id="a9974-2648">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2648">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2649">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2649">Pattern</span></span>

<span data-ttu-id="a9974-2650">12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2650">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2651">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2651">Checksum</span></span>

<span data-ttu-id="a9974-2652">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2652">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2653">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2653">Definition</span></span>

<span data-ttu-id="a9974-2654">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2654">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2655">Func_jp_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2655">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2656">Keyword_jp_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2656">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2657">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2657">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="a9974-2658">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2658">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="a9974-2659">dl</span><span class="sxs-lookup"><span data-stu-id="a9974-2659">dl#</span></span> 
- <span data-ttu-id="a9974-2660">DL</span><span class="sxs-lookup"><span data-stu-id="a9974-2660">DL＃</span></span> 
- <span data-ttu-id="a9974-2661">된다</span><span class="sxs-lookup"><span data-stu-id="a9974-2661">dls#</span></span> 
- <span data-ttu-id="a9974-2662">된다</span><span class="sxs-lookup"><span data-stu-id="a9974-2662">DLS＃</span></span> 
- <span data-ttu-id="a9974-2663">driver license</span><span class="sxs-lookup"><span data-stu-id="a9974-2663">driver license</span></span> 
- <span data-ttu-id="a9974-2664">driver licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-2664">driver licenses</span></span> 
- <span data-ttu-id="a9974-2665">drivers license</span><span class="sxs-lookup"><span data-stu-id="a9974-2665">drivers license</span></span> 
- <span data-ttu-id="a9974-2666">driver's license</span><span class="sxs-lookup"><span data-stu-id="a9974-2666">driver's license</span></span> 
- <span data-ttu-id="a9974-2667">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-2667">drivers licenses</span></span> 
- <span data-ttu-id="a9974-2668">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-2668">driver's licenses</span></span> 
- <span data-ttu-id="a9974-2669">driving licence</span><span class="sxs-lookup"><span data-stu-id="a9974-2669">driving licence</span></span> 
- <span data-ttu-id="a9974-2670">lic</span><span class="sxs-lookup"><span data-stu-id="a9974-2670">lic#</span></span> 
- <span data-ttu-id="a9974-2671">LIC</span><span class="sxs-lookup"><span data-stu-id="a9974-2671">LIC＃</span></span> 
- <span data-ttu-id="a9974-2672">driver'lics</span><span class="sxs-lookup"><span data-stu-id="a9974-2672">lics#</span></span> 
- <span data-ttu-id="a9974-2673">state id</span><span class="sxs-lookup"><span data-stu-id="a9974-2673">state id</span></span> 
- <span data-ttu-id="a9974-2674">state identification</span><span class="sxs-lookup"><span data-stu-id="a9974-2674">state identification</span></span> 
- <span data-ttu-id="a9974-2675">state identification number</span><span class="sxs-lookup"><span data-stu-id="a9974-2675">state identification number</span></span> 
- <span data-ttu-id="a9974-2676">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="a9974-2676">低所得国＃</span></span> 
- <span data-ttu-id="a9974-2677">免許証</span><span class="sxs-lookup"><span data-stu-id="a9974-2677">免許証</span></span> 
- <span data-ttu-id="a9974-2678">状態ID</span><span class="sxs-lookup"><span data-stu-id="a9974-2678">状態ID</span></span>
- <span data-ttu-id="a9974-2679">状態の識別</span><span class="sxs-lookup"><span data-stu-id="a9974-2679">状態の識別</span></span> 
- <span data-ttu-id="a9974-2680">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2680">状態の識別番号</span></span> 
- <span data-ttu-id="a9974-2681">運転免許</span><span class="sxs-lookup"><span data-stu-id="a9974-2681">運転免許</span></span> 
- <span data-ttu-id="a9974-2682">運転免許証</span><span class="sxs-lookup"><span data-stu-id="a9974-2682">運転免許証</span></span> 
- <span data-ttu-id="a9974-2683">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2683">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="a9974-2684">일본 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2684">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2685">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2685">Format</span></span>

<span data-ttu-id="a9974-2686">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2686">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2687">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2687">Pattern</span></span>

<span data-ttu-id="a9974-2688">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2688">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2689">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2689">Checksum</span></span>

<span data-ttu-id="a9974-2690">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2690">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2691">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2691">Definition</span></span>

<span data-ttu-id="a9974-2692">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2692">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2693">Func_jp_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2693">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2694">Keyword_jp_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2694">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2695">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2695">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="a9974-2696">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-2696">Keyword_jp_passport</span></span>

- <span data-ttu-id="a9974-2697">パスポート</span><span class="sxs-lookup"><span data-stu-id="a9974-2697">パスポート</span></span> 
- <span data-ttu-id="a9974-2698">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2698">パスポート番号</span></span> 
- <span data-ttu-id="a9974-2699">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="a9974-2699">パスポートのNum</span></span> 
- <span data-ttu-id="a9974-2700">パスポート #</span><span class="sxs-lookup"><span data-stu-id="a9974-2700">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="a9974-2701">일본 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2701">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2702">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2702">Format</span></span>

<span data-ttu-id="a9974-2703">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2703">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2704">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2704">Pattern</span></span>

<span data-ttu-id="a9974-2705">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2705">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2706">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2706">Checksum</span></span>

<span data-ttu-id="a9974-2707">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2707">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2708">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2708">Definition</span></span>

<span data-ttu-id="a9974-2709">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2709">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2710">Func_jp_resident_registration_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2710">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2711">Keyword_jp_resident_registration_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2711">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2712">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2712">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="a9974-2713">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2713">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="a9974-2714">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2714">Resident Registration Number</span></span>
- <span data-ttu-id="a9974-2715">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2715">Resident Register Number</span></span> 
- <span data-ttu-id="a9974-2716">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2716">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="a9974-2717">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2717">Resident Registration No.</span></span> 
- <span data-ttu-id="a9974-2718">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2718">Resident Register No.</span></span> 
- <span data-ttu-id="a9974-2719">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2719">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="a9974-2720">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2720">Basic Resident Register No.</span></span> 
- <span data-ttu-id="a9974-2721">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="a9974-2721">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="a9974-2722">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2722">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="a9974-2723">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="a9974-2723">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="a9974-2724">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2724">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="a9974-2725">일본 SIN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="a9974-2725">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2726">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2726">Format</span></span>

<span data-ttu-id="a9974-2727">7-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2727">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2728">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2728">Pattern</span></span>

<span data-ttu-id="a9974-2729">7-12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2729">7-12 digits:</span></span>
- <span data-ttu-id="a9974-2730">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2730">Four digits</span></span> 
- <span data-ttu-id="a9974-2731">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a9974-2731">A hyphen (optional)</span></span> 
- <span data-ttu-id="a9974-2732">6 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="a9974-2732">Six digits OR</span></span>
- <span data-ttu-id="a9974-2733">7-12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2733">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2734">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2734">Checksum</span></span>

<span data-ttu-id="a9974-2735">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2736">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2736">Definition</span></span>

<span data-ttu-id="a9974-2737">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2737">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2738">Func_jp_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2738">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2739">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2739">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="a9974-2740">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2740">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2741">Func_jp_sin_pre_1997 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2741">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2742">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2742">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2743">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2743">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="a9974-2744">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="a9974-2744">Keyword_jp_sin</span></span>

- <span data-ttu-id="a9974-2745">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="a9974-2745">Social Insurance No.</span></span> 
- <span data-ttu-id="a9974-2746">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="a9974-2746">Social Insurance Num</span></span> 
- <span data-ttu-id="a9974-2747">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2747">Social Insurance Number</span></span> 
- <span data-ttu-id="a9974-2748">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="a9974-2748">社会保険のテンキー</span></span> 
- <span data-ttu-id="a9974-2749">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2749">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="a9974-2750">일본어 거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2750">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2751">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2751">Format</span></span>

<span data-ttu-id="a9974-2752">12 개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2752">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2753">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2753">Pattern</span></span>

<span data-ttu-id="a9974-2754">12 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2754">12 letters and digits:</span></span>
- <span data-ttu-id="a9974-2755">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2755">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="a9974-2756">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2756">Eight digits</span></span> 
- <span data-ttu-id="a9974-2757">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-2757">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2758">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2758">Checksum</span></span>

<span data-ttu-id="a9974-2759">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2759">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2760">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2760">Definition</span></span>

<span data-ttu-id="a9974-2761">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2761">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2762">정규식 Regex_jp_residence_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2762">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2763">Keyword_jp_residence_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2763">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2764">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2764">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="a9974-2765">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2765">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="a9974-2766">거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2766">Residence card number</span></span>
- <span data-ttu-id="a9974-2767">거주지 카드 아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2767">Residence card no</span></span>
- <span data-ttu-id="a9974-2768">거주지 카드 #</span><span class="sxs-lookup"><span data-stu-id="a9974-2768">Residence card #</span></span>
- <span data-ttu-id="a9974-2769">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="a9974-2769">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="a9974-2770">말레이시아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2770">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2771">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2771">Format</span></span>

<span data-ttu-id="a9974-2772">선택적으로 하이픈을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2772">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2773">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2773">Pattern</span></span>

<span data-ttu-id="a9974-2774">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2774">12 digits:</span></span>
- <span data-ttu-id="a9974-2775">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-2775">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="a9974-2776">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="a9974-2776">A dash (optional)</span></span> 
- <span data-ttu-id="a9974-2777">2개 문자로 이루어진 출생지 코드 </span><span class="sxs-lookup"><span data-stu-id="a9974-2777">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="a9974-2778">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="a9974-2778">A dash (optional)</span></span> 
- <span data-ttu-id="a9974-2779">임의의 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-2779">Three random digits</span></span> 
- <span data-ttu-id="a9974-2780">1자리 성별 코드</span><span class="sxs-lookup"><span data-stu-id="a9974-2780">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2781">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2781">Checksum</span></span>

<span data-ttu-id="a9974-2782">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2782">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2783">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2783">Definition</span></span>

<span data-ttu-id="a9974-2784">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2785">정규식 Regex_malaysia_id_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2785">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2786">Keyword_malaysia_id_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2786">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2787">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2787">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="a9974-2788">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2788">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="a9974-2789">디지털 응용 프로그램 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2789">digital application card</span></span>
- <span data-ttu-id="a9974-2790">i/c</span><span class="sxs-lookup"><span data-stu-id="a9974-2790">i/c</span></span>
- <span data-ttu-id="a9974-2791">i/c 아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2791">i/c no</span></span>
- <span data-ttu-id="a9974-2792">비용</span><span class="sxs-lookup"><span data-stu-id="a9974-2792">ic</span></span>
- <span data-ttu-id="a9974-2793">ic 아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2793">ic no</span></span>
- <span data-ttu-id="a9974-2794">id card</span><span class="sxs-lookup"><span data-stu-id="a9974-2794">id card</span></span>
- <span data-ttu-id="a9974-2795">식별 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2795">identification Card</span></span>
- <span data-ttu-id="a9974-2796">identity card</span><span class="sxs-lookup"><span data-stu-id="a9974-2796">identity card</span></span>
- <span data-ttu-id="a9974-2797">k/p</span><span class="sxs-lookup"><span data-stu-id="a9974-2797">k/p</span></span>
- <span data-ttu-id="a9974-2798">k/p 아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2798">k/p no</span></span>
- <span data-ttu-id="a9974-2799">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="a9974-2799">kad akuan diri</span></span>
- <span data-ttu-id="a9974-2800">kad aplikasi 디지털</span><span class="sxs-lookup"><span data-stu-id="a9974-2800">kad aplikasi digital</span></span>
- <span data-ttu-id="a9974-2801">kad pengenalan 말레이시아</span><span class="sxs-lookup"><span data-stu-id="a9974-2801">kad pengenalan malaysia</span></span>
- <span data-ttu-id="a9974-2802">kp</span><span class="sxs-lookup"><span data-stu-id="a9974-2802">kp</span></span>
- <span data-ttu-id="a9974-2803">kp 아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2803">kp no</span></span>
- <span data-ttu-id="a9974-2804">mykad</span><span class="sxs-lookup"><span data-stu-id="a9974-2804">mykad</span></span>
- <span data-ttu-id="a9974-2805">mykas</span><span class="sxs-lookup"><span data-stu-id="a9974-2805">mykas</span></span>
- <span data-ttu-id="a9974-2806">mykid</span><span class="sxs-lookup"><span data-stu-id="a9974-2806">mykid</span></span>
- <span data-ttu-id="a9974-2807">mypr</span><span class="sxs-lookup"><span data-stu-id="a9974-2807">mypr</span></span>
- <span data-ttu-id="a9974-2808">myta</span><span class="sxs-lookup"><span data-stu-id="a9974-2808">mytentera</span></span>
- <span data-ttu-id="a9974-2809">말레이시아 id 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2809">malaysia identity card</span></span>
- <span data-ttu-id="a9974-2810">말레이지아 id 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2810">malaysian identity card</span></span>
- <span data-ttu-id="a9974-2811">nric</span><span class="sxs-lookup"><span data-stu-id="a9974-2811">nric</span></span>
- <span data-ttu-id="a9974-2812">개인 식별 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2812">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="a9974-2813">네덜란드 시민 서비스(BSN) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2813">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2814">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2814">Format</span></span>

<span data-ttu-id="a9974-2815">선택적으로 공백을 포함하는 8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2815">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2816">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2816">Pattern</span></span>

<span data-ttu-id="a9974-2817">8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2817">8-9 digits:</span></span>
- <span data-ttu-id="a9974-2818">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2818">Three digits</span></span> 
- <span data-ttu-id="a9974-2819">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a9974-2819">A space (optional)</span></span> 
- <span data-ttu-id="a9974-2820">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2820">Three digits</span></span> 
- <span data-ttu-id="a9974-2821">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a9974-2821">A space (optional)</span></span> 
- <span data-ttu-id="a9974-2822">2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2822">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2823">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2823">Checksum</span></span>

<span data-ttu-id="a9974-2824">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2825">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2825">Definition</span></span>

<span data-ttu-id="a9974-2826">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2826">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2827">Func_netherlands_bsn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2827">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2828">Keyword_netherlands_bsn에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2828">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="a9974-2829">Func_eu_date2 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2829">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="a9974-2830">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2830">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2831">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2831">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="a9974-2832">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="a9974-2832">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="a9974-2833">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="a9974-2833">Citizen service number</span></span> 
- <span data-ttu-id="a9974-2834">BSN</span><span class="sxs-lookup"><span data-stu-id="a9974-2834">BSN</span></span> 
- <span data-ttu-id="a9974-2835">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2835">Burgerservicenummer</span></span> 
- <span data-ttu-id="a9974-2836">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2836">Sofinummer</span></span> 
- <span data-ttu-id="a9974-2837">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2837">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="a9974-2838">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2838">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="a9974-2839">뉴질랜드 보건부 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2839">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2840">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2840">Format</span></span>

<span data-ttu-id="a9974-2841">3개 문자, 공백 1개(선택 사항) 및 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2841">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2842">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2842">Pattern</span></span>

<span data-ttu-id="a9974-2843">3 개의 문자 (대/소문자 구분 안 함) 공백 (선택 사항) 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2843">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2844">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2844">Checksum</span></span>

<span data-ttu-id="a9974-2845">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2845">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2846">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2846">Definition</span></span>

<span data-ttu-id="a9974-2847">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2848">Func_new_zealand_ministry_of_health_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2848">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2849">Keyword_nz_terms의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2849">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="a9974-2850">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2850">The checksum passes.</span></span>

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

<span data-ttu-id="a9974-2851">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2851">Keywords</span></span>

<span data-ttu-id="a9974-2852">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="a9974-2852">Keyword_nz_terms</span></span>

- <span data-ttu-id="a9974-2853">nhi</span><span class="sxs-lookup"><span data-stu-id="a9974-2853">NHI</span></span> 
- <span data-ttu-id="a9974-2854">New Zealand</span><span class="sxs-lookup"><span data-stu-id="a9974-2854">New Zealand</span></span> 
- <span data-ttu-id="a9974-2855">상태</span><span class="sxs-lookup"><span data-stu-id="a9974-2855">Health</span></span> 
- <span data-ttu-id="a9974-2856">처리가</span><span class="sxs-lookup"><span data-stu-id="a9974-2856">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="a9974-2857">Norway Identification Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2857">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2858">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2858">Format</span></span>

<span data-ttu-id="a9974-2859">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2859">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2860">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2860">Pattern</span></span>

<span data-ttu-id="a9974-2861">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2861">11 digits:</span></span>
- <span data-ttu-id="a9974-2862">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-2862">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="a9974-2863">3자리 개인 번호 </span><span class="sxs-lookup"><span data-stu-id="a9974-2863">Three-digit individual number</span></span> 
- <span data-ttu-id="a9974-2864">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2864">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2865">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2865">Checksum</span></span>

<span data-ttu-id="a9974-2866">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2866">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2867">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2867">Definition</span></span>

<span data-ttu-id="a9974-2868">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2868">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2869">Func_norway_id_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2869">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2870">Keyword_norway_id_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2870">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="a9974-2871">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2871">The checksum passes.</span></span>
- <span data-ttu-id="a9974-2872">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2873">Func_norway_id_numbe 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2873">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2874">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2874">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2875">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2875">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="a9974-2876">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2876">Keyword_norway_id_number</span></span>

- <span data-ttu-id="a9974-2877">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="a9974-2877">Personal identification number</span></span>
- <span data-ttu-id="a9974-2878">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2878">Norwegian ID Number</span></span>
- <span data-ttu-id="a9974-2879">ID Number</span><span class="sxs-lookup"><span data-stu-id="a9974-2879">ID Number</span></span>
- <span data-ttu-id="a9974-2880">확인과</span><span class="sxs-lookup"><span data-stu-id="a9974-2880">Identification</span></span>
- <span data-ttu-id="a9974-2881">Personnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2881">Personnummer</span></span>
- <span data-ttu-id="a9974-2882">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="a9974-2882">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="a9974-2883">필리핀 통합 다목적 ID 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2883">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2884">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2884">Format</span></span>

<span data-ttu-id="a9974-2885">하이픈으로 구분된 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2885">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2886">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2886">Pattern</span></span>

<span data-ttu-id="a9974-2887">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2887">12 digits:</span></span>
- <span data-ttu-id="a9974-2888">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2888">Four digits</span></span> 
- <span data-ttu-id="a9974-2889">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-2889">A hyphen</span></span> 
- <span data-ttu-id="a9974-2890">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2890">Seven digits</span></span> 
- <span data-ttu-id="a9974-2891">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-2891">A hyphen</span></span> 
- <span data-ttu-id="a9974-2892">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2892">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2893">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2893">Checksum</span></span>

<span data-ttu-id="a9974-2894">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2894">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2895">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2895">Definition</span></span>

<span data-ttu-id="a9974-2896">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2896">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2897">정규식 Regex_philippines_unified_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2897">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2898">Keyword_philippines_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2898">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2899">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2899">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="a9974-2900">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="a9974-2900">Keyword_philippines_id</span></span>

- <span data-ttu-id="a9974-2901">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="a9974-2901">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="a9974-2902">UMID</span><span class="sxs-lookup"><span data-stu-id="a9974-2902">UMID</span></span> 
- <span data-ttu-id="a9974-2903">Identity Card</span><span class="sxs-lookup"><span data-stu-id="a9974-2903">Identity Card</span></span> 
- <span data-ttu-id="a9974-2904">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="a9974-2904">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="a9974-2905">폴란드 ID 카드</span><span class="sxs-lookup"><span data-stu-id="a9974-2905">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2906">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2906">Format</span></span>

<span data-ttu-id="a9974-2907">3개의 문자 및 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2907">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2908">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2908">Pattern</span></span>

<span data-ttu-id="a9974-2909">3개의 문자(대/소문자 구분 안 함)와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2909">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2910">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2910">Checksum</span></span>

<span data-ttu-id="a9974-2911">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2911">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2912">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2912">Definition</span></span>

<span data-ttu-id="a9974-2913">DLP 정책은 300 문자 근사에서 Func_polish_national_id 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2913">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="a9974-2914">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2914">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="a9974-2915">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2915">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2916">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2916">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="a9974-2917">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2917">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="a9974-2918">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="a9974-2918">Dowód osobisty</span></span>
- <span data-ttu-id="a9974-2919">u r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="a9974-2919">Numer dowodu osobistego</span></span>
- <span data-ttu-id="a9974-2920">Nazwa i u r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="a9974-2920">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="a9974-2921">Nazwa i veiligheid dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="a9974-2921">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="a9974-2922">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="a9974-2922">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="a9974-2923">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="a9974-2923">Dowód Tożsamości</span></span>
- <span data-ttu-id="a9974-2924">dow.</span><span class="sxs-lookup"><span data-stu-id="a9974-2924">dow.</span></span> <span data-ttu-id="a9974-2925">르.</span><span class="sxs-lookup"><span data-stu-id="a9974-2925">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="a9974-2926">폴란드 국가 ID(PESEL)</span><span class="sxs-lookup"><span data-stu-id="a9974-2926">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2927">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2927">Format</span></span>

<span data-ttu-id="a9974-2928">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2928">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2929">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2929">Pattern</span></span>

<span data-ttu-id="a9974-2930">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2930">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2931">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2931">Checksum</span></span>

<span data-ttu-id="a9974-2932">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2932">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2933">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2933">Definition</span></span>

<span data-ttu-id="a9974-2934">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2934">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2935">Func_pesel_identification_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2935">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2936">Keyword_pesel_identification_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2936">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="a9974-2937">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2937">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2938">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2938">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="a9974-2939">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2939">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="a9974-2940">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="a9974-2940">Nr PESEL</span></span>
- <span data-ttu-id="a9974-2941">PESEL</span><span class="sxs-lookup"><span data-stu-id="a9974-2941">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="a9974-2942">폴란드 여권</span><span class="sxs-lookup"><span data-stu-id="a9974-2942">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2943">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2943">Format</span></span>

<span data-ttu-id="a9974-2944">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2944">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2945">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2945">Pattern</span></span>

<span data-ttu-id="a9974-2946">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2946">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2947">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2947">Checksum</span></span>

<span data-ttu-id="a9974-2948">예</span><span class="sxs-lookup"><span data-stu-id="a9974-2948">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2949">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2949">Definition</span></span>

<span data-ttu-id="a9974-2950">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2950">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2951">Func_polish_passport_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2951">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2952">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2952">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="a9974-2953">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2953">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2954">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2954">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="a9974-2955">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="a9974-2955">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="a9974-2956">u r i (zportu)</span><span class="sxs-lookup"><span data-stu-id="a9974-2956">Numer paszportu</span></span>
- <span data-ttu-id="a9974-2957">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="a9974-2957">Nr.</span></span> <span data-ttu-id="a9974-2958">고 zportu</span><span class="sxs-lookup"><span data-stu-id="a9974-2958">Paszportu</span></span>
- <span data-ttu-id="a9974-2959">고 zport</span><span class="sxs-lookup"><span data-stu-id="a9974-2959">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="a9974-2960">포르투갈 시민 카드 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2960">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2961">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2961">Format</span></span>

<span data-ttu-id="a9974-2962">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2962">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2963">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2963">Pattern</span></span>

<span data-ttu-id="a9974-2964">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2964">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2965">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2965">Checksum</span></span>

<span data-ttu-id="a9974-2966">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2966">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2967">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2967">Definition</span></span>

<span data-ttu-id="a9974-2968">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2969">정규식 Regex_portugal_citizen_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2969">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2970">Keyword_portugal_citizen_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2970">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-2971">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2971">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="a9974-2972">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="a9974-2972">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="a9974-2973">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="a9974-2973">Citizen Card</span></span>
- <span data-ttu-id="a9974-2974">National ID Card</span><span class="sxs-lookup"><span data-stu-id="a9974-2974">National ID Card</span></span>
- <span data-ttu-id="a9974-2975">참조란</span><span class="sxs-lookup"><span data-stu-id="a9974-2975">CC</span></span>
- <span data-ttu-id="a9974-2976">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="a9974-2976">Cartão de Cidadão</span></span>
- <span data-ttu-id="a9974-2977">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="a9974-2977">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="a9974-2978">사우디 아라비아 국가 ID</span><span class="sxs-lookup"><span data-stu-id="a9974-2978">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2979">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2979">Format</span></span>

<span data-ttu-id="a9974-2980">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2980">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2981">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2981">Pattern</span></span>

<span data-ttu-id="a9974-2982">10자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2982">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-2983">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-2983">Checksum</span></span>

<span data-ttu-id="a9974-2984">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-2984">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-2985">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-2985">Definition</span></span>

<span data-ttu-id="a9974-2986">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-2987">Regex_saudi_arabia_national_id 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2987">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-2988">Keyword_saudi_arabia_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-2988">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-2989">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-2989">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="a9974-2990">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="a9974-2990">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="a9974-2991">Identification Card</span><span class="sxs-lookup"><span data-stu-id="a9974-2991">Identification Card</span></span> 
- <span data-ttu-id="a9974-2992">I card number</span><span class="sxs-lookup"><span data-stu-id="a9974-2992">I card number</span></span> 
- <span data-ttu-id="a9974-2993">ID number</span><span class="sxs-lookup"><span data-stu-id="a9974-2993">ID number</span></span> 
- <span data-ttu-id="a9974-2994">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="a9974-2994">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="a9974-2995">싱가포르 NRIC(국가 등록 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-2995">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-2996">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-2996">Format</span></span>

<span data-ttu-id="a9974-2997">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-2997">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-2998">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-2998">Pattern</span></span>

- <span data-ttu-id="a9974-2999">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-2999">Nine letters and digits:</span></span>
- <span data-ttu-id="a9974-3000">문자 "F", "G", "S" 또는 "T"(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="a9974-3000">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-3001">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3001">Seven digits</span></span> 
- <span data-ttu-id="a9974-3002">알파벳 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3002">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3003">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3003">Checksum</span></span>

<span data-ttu-id="a9974-3004">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3004">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3005">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3005">Definition</span></span>

<span data-ttu-id="a9974-3006">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3006">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3007">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3007">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3008">Keyword_singapore_nric에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3008">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="a9974-3009">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3009">The checksum passes.</span></span>

<span data-ttu-id="a9974-3010">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3010">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3011">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3011">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3012">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3012">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3013">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3013">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="a9974-3014">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="a9974-3014">Keyword_singapore_nric</span></span>

- <span data-ttu-id="a9974-3015">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="a9974-3015">National Registration Identity Card</span></span> 
- <span data-ttu-id="a9974-3016">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3016">Identity Card Number</span></span> 
- <span data-ttu-id="a9974-3017">NRIC</span><span class="sxs-lookup"><span data-stu-id="a9974-3017">NRIC</span></span> 
- <span data-ttu-id="a9974-3018">비용</span><span class="sxs-lookup"><span data-stu-id="a9974-3018">IC</span></span> 
- <span data-ttu-id="a9974-3019">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3019">Foreign Identification Number</span></span> 
- <span data-ttu-id="a9974-3020">삭제할</span><span class="sxs-lookup"><span data-stu-id="a9974-3020">FIN</span></span> 
- <span data-ttu-id="a9974-3021">身份证</span><span class="sxs-lookup"><span data-stu-id="a9974-3021">身份证</span></span> 
- <span data-ttu-id="a9974-3022">身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-3022">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="a9974-3023">남아프리카 공화국 식별 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3023">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3024">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3024">Format</span></span>

<span data-ttu-id="a9974-3025">공백을 포함할 수 있는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3025">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3026">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3026">Pattern</span></span>

<span data-ttu-id="a9974-3027">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3027">13 digits:</span></span>
- <span data-ttu-id="a9974-3028">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-3028">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="a9974-3029">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3029">Four digits</span></span> 
- <span data-ttu-id="a9974-3030">1자리 시민권 표시 </span><span class="sxs-lookup"><span data-stu-id="a9974-3030">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="a9974-3031">숫자 "8" 또는 "9" </span><span class="sxs-lookup"><span data-stu-id="a9974-3031">The digit "8" or "9"</span></span> 
- <span data-ttu-id="a9974-3032">체크섬 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3032">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3033">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3033">Checksum</span></span>

<span data-ttu-id="a9974-3034">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3034">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3035">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3035">Definition</span></span>

<span data-ttu-id="a9974-3036">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3036">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3037">Func_south_africa_identification_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3037">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3038">Keyword_south_africa_identification_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3038">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="a9974-3039">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3039">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3040">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3040">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="a9974-3041">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="a9974-3041">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="a9974-3042">Identity card</span><span class="sxs-lookup"><span data-stu-id="a9974-3042">Identity card</span></span>
- <span data-ttu-id="a9974-3043">ID</span><span class="sxs-lookup"><span data-stu-id="a9974-3043">ID</span></span>
- <span data-ttu-id="a9974-3044">확인과</span><span class="sxs-lookup"><span data-stu-id="a9974-3044">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="a9974-3045">한국 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3045">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3046">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3046">Format</span></span>

<span data-ttu-id="a9974-3047">하이픈을 포함하는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3047">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3048">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3048">Pattern</span></span>

<span data-ttu-id="a9974-3049">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3049">13 digits:</span></span>
- <span data-ttu-id="a9974-3050">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-3050">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="a9974-3051">하이픈</span><span class="sxs-lookup"><span data-stu-id="a9974-3051">A hyphen</span></span> 
- <span data-ttu-id="a9974-3052">세기 및 성별에 따라 결정되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-3052">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="a9974-3053">4자리 출생 지역 코드 </span><span class="sxs-lookup"><span data-stu-id="a9974-3053">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="a9974-3054">앞 번호가 동일한 사람을 구분하기 위해 사용되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="a9974-3054">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="a9974-3055">검사 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3055">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3056">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3056">Checksum</span></span>

<span data-ttu-id="a9974-3057">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3057">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3058">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3058">Definition</span></span>

<span data-ttu-id="a9974-3059">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3059">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3060">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3060">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3061">Keyword_south_korea_resident_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3061">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="a9974-3062">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3062">The checksum passes.</span></span>

<span data-ttu-id="a9974-3063">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3063">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3064">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3064">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3065">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3065">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3066">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3066">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="a9974-3067">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="a9974-3067">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="a9974-3068">National ID card</span><span class="sxs-lookup"><span data-stu-id="a9974-3068">National ID card</span></span> 
- <span data-ttu-id="a9974-3069">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3069">Citizen's Registration Number</span></span> 
- <span data-ttu-id="a9974-3070">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="a9974-3070">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="a9974-3071">RRN</span><span class="sxs-lookup"><span data-stu-id="a9974-3071">RRN</span></span> 
- <span data-ttu-id="a9974-3072">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3072">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="a9974-3073">스페인 SSN(사회 보장 번호)</span><span class="sxs-lookup"><span data-stu-id="a9974-3073">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3074">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3074">Format</span></span>

<span data-ttu-id="a9974-3075">11-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3075">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3076">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3076">Pattern</span></span>

<span data-ttu-id="a9974-3077">11-12 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3077">11-12 digits:</span></span>
- <span data-ttu-id="a9974-3078">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3078">Two digits</span></span> 
- <span data-ttu-id="a9974-3079">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a9974-3079">A forward slash (optional)</span></span> 
- <span data-ttu-id="a9974-3080">7-8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3080">7-8 digits</span></span> 
- <span data-ttu-id="a9974-3081">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a9974-3081">A forward slash (optional)</span></span> 
- <span data-ttu-id="a9974-3082">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3082">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3083">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3083">Checksum</span></span>

<span data-ttu-id="a9974-3084">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3084">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3085">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3085">Definition</span></span>

<span data-ttu-id="a9974-3086">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3086">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3087">Func_spanish_social_security_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3087">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3088">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3088">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3089">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3089">Keywords</span></span>

<span data-ttu-id="a9974-3090">없음</span><span class="sxs-lookup"><span data-stu-id="a9974-3090">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="a9974-3091">SQL Server 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="a9974-3091">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3092">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3092">Format</span></span>

<span data-ttu-id="a9974-3093">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "user id", "user id", "uid" 또는 "UserId"입니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3093">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3094">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3094">Pattern</span></span>

- <span data-ttu-id="a9974-3095">문자열 "user id", "User id", "uid" 또는 "UserId"</span><span class="sxs-lookup"><span data-stu-id="a9974-3095">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="a9974-3096">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-3096">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="a9974-3097">문자열 "Password" 또는 "pwd" (여기에서 "pwd" 앞에 소문자 문자가 오지 않음)</span><span class="sxs-lookup"><span data-stu-id="a9974-3097">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="a9974-3098">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-3098">An equal sign (=)</span></span>
- <span data-ttu-id="a9974-3099">달러 기호 ($), 백분율 기호 (%, >), 기호 (@), 따옴표 ("), 세미콜론 (;), 왼쪽 중괄호 ([) 또는 왼쪽 대괄호 ({))가 아닌 모든 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-3099">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="a9974-3100">세미콜론 (;), 슬래시 (/) 또는 따옴표 (")가 아닌 7-128 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-3100">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="a9974-3101">세미콜론 (;) 또는 따옴표 (")</span><span class="sxs-lookup"><span data-stu-id="a9974-3101">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3102">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3102">Checksum</span></span>

<span data-ttu-id="a9974-3103">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3103">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3104">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3104">Definition</span></span>

<span data-ttu-id="a9974-3105">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3105">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3106">정규식 CEP_Regex_SQLServerConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3106">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3107">CEP_GlobalFilter의 키워드를 찾을 수 **없습니다** .</span><span class="sxs-lookup"><span data-stu-id="a9974-3107">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="a9974-3108">CEP_PasswordPlaceHolder 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3108">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3109">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3109">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!---SQL Server Connection String>
<Entity id="e76b6205-d3cb-46f2-bd63-c90153f2f97d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_SQLServerConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_GlobalFilter" />
            <Match idRef="CEP_PasswordPlaceHolder" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3110">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3110">Keywords</span></span>

#### <a name="cepglobalfilter"></a><span data-ttu-id="a9974-3111">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="a9974-3111">CEP_GlobalFilter</span></span>

- <span data-ttu-id="a9974-3112">일부 암호</span><span class="sxs-lookup"><span data-stu-id="a9974-3112">some-password</span></span>
- <span data-ttu-id="a9974-3113">somepassword</span><span class="sxs-lookup"><span data-stu-id="a9974-3113">somepassword</span></span>
- <span data-ttu-id="a9974-3114">secretPassword</span><span class="sxs-lookup"><span data-stu-id="a9974-3114">secretPassword</span></span>
- <span data-ttu-id="a9974-3115">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3115">sample</span></span>

#### <a name="ceppasswordplaceholder"></a><span data-ttu-id="a9974-3116">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="a9974-3116">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="a9974-3117">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3117">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-3118">암호나 pwd에 0-2 공백, 등호 (=), 0-2 공백 및 별표 (\*)-----------------------</span><span class="sxs-lookup"><span data-stu-id="a9974-3118">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="a9974-3119">암호나 pwd 뒤에 다음이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3119">Password or pwd followed by:</span></span>
    - <span data-ttu-id="a9974-3120">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="a9974-3120">Equal sign (=)</span></span>
    - <span data-ttu-id="a9974-3121">보다 작음 기호 (<)</span><span class="sxs-lookup"><span data-stu-id="a9974-3121">Less than symbol (<)</span></span>
    - <span data-ttu-id="a9974-3122">대문자나 소문자, digits, 별표 (\*), 하이픈 (-), 밑줄 (_) 또는 공백 문자인 1-200 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-3122">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="a9974-3123">기호 보다 큼 (>)</span><span class="sxs-lookup"><span data-stu-id="a9974-3123">Greater than symbol (>)</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="a9974-3124">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="a9974-3124">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="a9974-3125">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3125">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="a9974-3126">극동</span><span class="sxs-lookup"><span data-stu-id="a9974-3126">contoso</span></span>
- <span data-ttu-id="a9974-3127">fabrikam</span><span class="sxs-lookup"><span data-stu-id="a9974-3127">fabrikam</span></span>
- <span data-ttu-id="a9974-3128">대양</span><span class="sxs-lookup"><span data-stu-id="a9974-3128">northwind</span></span>
- <span data-ttu-id="a9974-3129">샌드박스</span><span class="sxs-lookup"><span data-stu-id="a9974-3129">sandbox</span></span>
- <span data-ttu-id="a9974-3130">용 onebox</span><span class="sxs-lookup"><span data-stu-id="a9974-3130">onebox</span></span>
- <span data-ttu-id="a9974-3131">로컬</span><span class="sxs-lookup"><span data-stu-id="a9974-3131">localhost</span></span>
- <span data-ttu-id="a9974-3132">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="a9974-3132">127.0.0.1</span></span>
- <span data-ttu-id="a9974-3133">testacs입니다. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="a9974-3133">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="a9974-3134">s-int<!--no-hyperlink--></span><span class="sxs-lookup"><span data-stu-id="a9974-3134">s-int.<!--no-hyperlink-->net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="a9974-3135">스웨덴 국가 ID</span><span class="sxs-lookup"><span data-stu-id="a9974-3135">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3136">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3136">Format</span></span>

<span data-ttu-id="a9974-3137">10 또는 12자리 숫자와 선택적 구분 기호</span><span class="sxs-lookup"><span data-stu-id="a9974-3137">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3138">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3138">Pattern</span></span>

<span data-ttu-id="a9974-3139">10 또는 12자리 숫자와 선택적 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="a9974-3139">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="a9974-3140">2-4자리 숫자(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a9974-3140">2-4 digits (optional)</span></span> 
- <span data-ttu-id="a9974-3141">YYMMDD 날짜 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3141">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="a9974-3142">구분 기호 "-" 또는 "+"(선택 사항) 및</span><span class="sxs-lookup"><span data-stu-id="a9974-3142">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="a9974-3143">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3143">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3144">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3144">Checksum</span></span>

<span data-ttu-id="a9974-3145">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3145">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3146">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3146">Definition</span></span>

<span data-ttu-id="a9974-3147">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3147">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3148">Func_swedish_national_identifier 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3148">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3149">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3149">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3150">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3150">Keywords</span></span>

<span data-ttu-id="a9974-3151">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3151">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="a9974-3152">스웨덴 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3152">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3153">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3153">Format</span></span>

<span data-ttu-id="a9974-3154">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3154">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3155">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3155">Pattern</span></span>

<span data-ttu-id="a9974-3156">8자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3156">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3157">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3157">Checksum</span></span>

<span data-ttu-id="a9974-3158">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3158">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3159">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3159">Definition</span></span>

<span data-ttu-id="a9974-3160">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3160">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3161">Regex_sweden_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3161">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3162">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3162">One of the following is true:</span></span>
    - <span data-ttu-id="a9974-3163">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3163">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="a9974-3164">Keyword_sweden_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3164">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3165">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3165">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="a9974-3166">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-3166">Keyword_sweden_passport</span></span>

- <span data-ttu-id="a9974-3167">visa requirements</span><span class="sxs-lookup"><span data-stu-id="a9974-3167">visa requirements</span></span> 
- <span data-ttu-id="a9974-3168">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="a9974-3168">Alien Registration Card</span></span> 
- <span data-ttu-id="a9974-3169">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="a9974-3169">Schengen visas</span></span> 
- <span data-ttu-id="a9974-3170">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="a9974-3170">Schengen visa</span></span> 
- <span data-ttu-id="a9974-3171">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="a9974-3171">Visa Processing</span></span> 
- <span data-ttu-id="a9974-3172">Visa Type</span><span class="sxs-lookup"><span data-stu-id="a9974-3172">Visa Type</span></span> 
- <span data-ttu-id="a9974-3173">Single Entry</span><span class="sxs-lookup"><span data-stu-id="a9974-3173">Single Entry</span></span> 
- <span data-ttu-id="a9974-3174">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="a9974-3174">Multiple Entry</span></span> 
- <span data-ttu-id="a9974-3175">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="a9974-3175">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="a9974-3176">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-3176">Keyword_passport</span></span>

- <span data-ttu-id="a9974-3177">Passport Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3177">Passport Number</span></span> 
- <span data-ttu-id="a9974-3178">Passport No</span><span class="sxs-lookup"><span data-stu-id="a9974-3178">Passport No</span></span> 
- <span data-ttu-id="a9974-3179">Passport #</span><span class="sxs-lookup"><span data-stu-id="a9974-3179">Passport #</span></span> 
- <span data-ttu-id="a9974-3180">여권</span><span class="sxs-lookup"><span data-stu-id="a9974-3180">Passport#</span></span> 
- <span data-ttu-id="a9974-3181">PassportID</span><span class="sxs-lookup"><span data-stu-id="a9974-3181">PassportID</span></span> 
- <span data-ttu-id="a9974-3182">Passportno</span><span class="sxs-lookup"><span data-stu-id="a9974-3182">Passportno</span></span> 
- <span data-ttu-id="a9974-3183">passportnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-3183">passportnumber</span></span> 
- <span data-ttu-id="a9974-3184">パスポート</span><span class="sxs-lookup"><span data-stu-id="a9974-3184">パスポート</span></span> 
- <span data-ttu-id="a9974-3185">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="a9974-3185">パスポート番号</span></span> 
- <span data-ttu-id="a9974-3186">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="a9974-3186">パスポートのNum</span></span> 
- <span data-ttu-id="a9974-3187">パスポート #</span><span class="sxs-lookup"><span data-stu-id="a9974-3187">パスポート＃</span></span> 
- <span data-ttu-id="a9974-3188">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a9974-3188">Numéro de passeport</span></span> 
- <span data-ttu-id="a9974-3189">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="a9974-3189">Passeport n °</span></span> 
- <span data-ttu-id="a9974-3190">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="a9974-3190">Passeport Non</span></span> 
- <span data-ttu-id="a9974-3191">Passeport #</span><span class="sxs-lookup"><span data-stu-id="a9974-3191">Passeport #</span></span> 
- <span data-ttu-id="a9974-3192">포트 #</span><span class="sxs-lookup"><span data-stu-id="a9974-3192">Passeport#</span></span> 
- <span data-ttu-id="a9974-3193">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="a9974-3193">PasseportNon</span></span> 
- <span data-ttu-id="a9974-3194">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="a9974-3194">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="a9974-3195">SWIFT 코드</span><span class="sxs-lookup"><span data-stu-id="a9974-3195">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3196">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3196">Format</span></span>

<span data-ttu-id="a9974-3197">4개의 문자, 5-31개 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3197">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3198">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3198">Pattern</span></span>

<span data-ttu-id="a9974-3199">4개의 문자, 5-31개 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3199">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="a9974-3200">4문자 은행 코드(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-3200">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-3201">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-3201">An optional space</span></span> 
- <span data-ttu-id="a9974-3202">4-28개 문자 또는 숫자[BBAN(기본 은행 계좌 번호)]</span><span class="sxs-lookup"><span data-stu-id="a9974-3202">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="a9974-3203">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="a9974-3203">An optional space</span></span> 
- <span data-ttu-id="a9974-3204">1-3개 문자 또는 숫자(BBAN의 나머지)</span><span class="sxs-lookup"><span data-stu-id="a9974-3204">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3205">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3205">Checksum</span></span>

<span data-ttu-id="a9974-3206">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3206">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3207">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3207">Definition</span></span>

<span data-ttu-id="a9974-3208">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3208">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3209">Regex_swift 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3209">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3210">Keyword_swift의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3210">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3211">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3211">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="a9974-3212">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="a9974-3212">Keyword_swift</span></span>

- <span data-ttu-id="a9974-3213">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="a9974-3213">international organization for standardization 9362</span></span> 
- <span data-ttu-id="a9974-3214">iso 9362</span><span class="sxs-lookup"><span data-stu-id="a9974-3214">iso 9362</span></span> 
- <span data-ttu-id="a9974-3215">iso9362</span><span class="sxs-lookup"><span data-stu-id="a9974-3215">iso9362</span></span> 
- <span data-ttu-id="a9974-3216">swift\#</span><span class="sxs-lookup"><span data-stu-id="a9974-3216">swift\#</span></span> 
- <span data-ttu-id="a9974-3217">swiftcode</span><span class="sxs-lookup"><span data-stu-id="a9974-3217">swiftcode</span></span> 
- <span data-ttu-id="a9974-3218">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-3218">swiftnumber</span></span> 
- <span data-ttu-id="a9974-3219">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-3219">swiftroutingnumber</span></span> 
- <span data-ttu-id="a9974-3220">swift code</span><span class="sxs-lookup"><span data-stu-id="a9974-3220">swift code</span></span> 
- <span data-ttu-id="a9974-3221">swift number #</span><span class="sxs-lookup"><span data-stu-id="a9974-3221">swift number #</span></span> 
- <span data-ttu-id="a9974-3222">swift routing number</span><span class="sxs-lookup"><span data-stu-id="a9974-3222">swift routing number</span></span> 
- <span data-ttu-id="a9974-3223">bic number</span><span class="sxs-lookup"><span data-stu-id="a9974-3223">bic number</span></span> 
- <span data-ttu-id="a9974-3224">bic code</span><span class="sxs-lookup"><span data-stu-id="a9974-3224">bic code</span></span> 
- <span data-ttu-id="a9974-3225">bic\#</span><span class="sxs-lookup"><span data-stu-id="a9974-3225">bic \#</span></span> 
- <span data-ttu-id="a9974-3226">bic\#</span><span class="sxs-lookup"><span data-stu-id="a9974-3226">bic\#</span></span> 
- <span data-ttu-id="a9974-3227">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="a9974-3227">bank identifier code</span></span> 
- <span data-ttu-id="a9974-3228">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="a9974-3228">標準化9362</span></span> 
- <span data-ttu-id="a9974-3229">迅速 #</span><span class="sxs-lookup"><span data-stu-id="a9974-3229">迅速＃</span></span> 
- <span data-ttu-id="a9974-3230">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="a9974-3230">SWIFTコード</span></span> 
- <span data-ttu-id="a9974-3231">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="a9974-3231">SWIFT番号</span></span> 
- <span data-ttu-id="a9974-3232">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="a9974-3232">迅速なルーティング番号</span></span> 
- <span data-ttu-id="a9974-3233">BIC番号</span><span class="sxs-lookup"><span data-stu-id="a9974-3233">BIC番号</span></span> 
- <span data-ttu-id="a9974-3234">BICコード</span><span class="sxs-lookup"><span data-stu-id="a9974-3234">BICコード</span></span> 
- <span data-ttu-id="a9974-3235">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="a9974-3235">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="a9974-3236">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="a9974-3236">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="a9974-3237">rapide\#</span><span class="sxs-lookup"><span data-stu-id="a9974-3237">rapide \#</span></span> 
- <span data-ttu-id="a9974-3238">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="a9974-3238">code SWIFT</span></span> 
- <span data-ttu-id="a9974-3239">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="a9974-3239">le numéro de swift</span></span> 
- <span data-ttu-id="a9974-3240">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="a9974-3240">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="a9974-3241">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="a9974-3241">le numéro BIC</span></span> 
- <span data-ttu-id="a9974-3242">\#bic</span><span class="sxs-lookup"><span data-stu-id="a9974-3242">\# BIC</span></span> 
- <span data-ttu-id="a9974-3243">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="a9974-3243">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="a9974-3244">대만 국가 ID</span><span class="sxs-lookup"><span data-stu-id="a9974-3244">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3245">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3245">Format</span></span>

<span data-ttu-id="a9974-3246">1개의 문자, 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3246">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3247">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3247">Pattern</span></span>

<span data-ttu-id="a9974-3248">1개의 문자, 9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3248">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="a9974-3249">1개 문자(영문, 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-3249">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="a9974-3250">숫자 "1" 또는 "2"</span><span class="sxs-lookup"><span data-stu-id="a9974-3250">The digit "1" or "2"</span></span> 
- <span data-ttu-id="a9974-3251">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3251">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3252">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3252">Checksum</span></span>

<span data-ttu-id="a9974-3253">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3253">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3254">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3254">Definition</span></span>

<span data-ttu-id="a9974-3255">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3255">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3256">Func_taiwanese_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3256">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3257">Keyword_taiwanese_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3257">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="a9974-3258">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3258">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3259">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3259">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="a9974-3260">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="a9974-3260">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="a9974-3261">身份證字號</span><span class="sxs-lookup"><span data-stu-id="a9974-3261">身份證字號</span></span> 
- <span data-ttu-id="a9974-3262">身份證</span><span class="sxs-lookup"><span data-stu-id="a9974-3262">身份證</span></span> 
- <span data-ttu-id="a9974-3263">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="a9974-3263">身份證號碼</span></span> 
- <span data-ttu-id="a9974-3264">身份證號</span><span class="sxs-lookup"><span data-stu-id="a9974-3264">身份證號</span></span> 
- <span data-ttu-id="a9974-3265">身分證字號</span><span class="sxs-lookup"><span data-stu-id="a9974-3265">身分證字號</span></span> 
- <span data-ttu-id="a9974-3266">身分證</span><span class="sxs-lookup"><span data-stu-id="a9974-3266">身分證</span></span> 
- <span data-ttu-id="a9974-3267">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="a9974-3267">身分證號碼</span></span> 
- <span data-ttu-id="a9974-3268">身份證號</span><span class="sxs-lookup"><span data-stu-id="a9974-3268">身份證號</span></span> 
- <span data-ttu-id="a9974-3269">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="a9974-3269">身分證統一編號</span></span> 
- <span data-ttu-id="a9974-3270">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="a9974-3270">國民身分證統一編號</span></span> 
- <span data-ttu-id="a9974-3271">簽名</span><span class="sxs-lookup"><span data-stu-id="a9974-3271">簽名</span></span> 
- <span data-ttu-id="a9974-3272">蓋章</span><span class="sxs-lookup"><span data-stu-id="a9974-3272">蓋章</span></span> 
- <span data-ttu-id="a9974-3273">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="a9974-3273">簽名或蓋章</span></span> 
- <span data-ttu-id="a9974-3274">簽章</span><span class="sxs-lookup"><span data-stu-id="a9974-3274">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="a9974-3275">	대만 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3275">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3276">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3276">Format</span></span>

- <span data-ttu-id="a9974-3277">생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3277">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="a9974-3278">비-생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3278">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3279">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3279">Pattern</span></span>
<span data-ttu-id="a9974-3280">생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="a9974-3280">Biometric passport number:</span></span>
- <span data-ttu-id="a9974-3281">숫자 "3" </span><span class="sxs-lookup"><span data-stu-id="a9974-3281">The digit "3"</span></span> 
- <span data-ttu-id="a9974-3282">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3282">Eight digits</span></span>

<span data-ttu-id="a9974-3283">비-생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="a9974-3283">Non-biometric passport number:</span></span>
- <span data-ttu-id="a9974-3284">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3284">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3285">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3285">Checksum</span></span>

<span data-ttu-id="a9974-3286">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3287">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3287">Definition</span></span>

<span data-ttu-id="a9974-3288">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3289">정규식 Regex_taiwan_passport 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3289">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3290">Keyword_taiwan_passport에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3290">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3291">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3291">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="a9974-3292">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-3292">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="a9974-3293">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="a9974-3293">ROC passport number</span></span> 
- <span data-ttu-id="a9974-3294">Passport number</span><span class="sxs-lookup"><span data-stu-id="a9974-3294">Passport number</span></span> 
- <span data-ttu-id="a9974-3295">Passport no</span><span class="sxs-lookup"><span data-stu-id="a9974-3295">Passport no</span></span> 
- <span data-ttu-id="a9974-3296">Passport Num</span><span class="sxs-lookup"><span data-stu-id="a9974-3296">Passport Num</span></span> 
- <span data-ttu-id="a9974-3297">Passport #</span><span class="sxs-lookup"><span data-stu-id="a9974-3297">Passport #</span></span> 
- <span data-ttu-id="a9974-3298">护照</span><span class="sxs-lookup"><span data-stu-id="a9974-3298">护照</span></span> 
- <span data-ttu-id="a9974-3299">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="a9974-3299">中華民國護照</span></span> 
- <span data-ttu-id="a9974-3300">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="a9974-3300">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="a9974-3301">대만 거주 인증(ARC/TARC) 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3301">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3302">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3302">Format</span></span>

<span data-ttu-id="a9974-3303">10개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3303">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3304">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3304">Pattern</span></span>

<span data-ttu-id="a9974-3305">10개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3305">10 letters and digits:</span></span>
- <span data-ttu-id="a9974-3306">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-3306">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="a9974-3307">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3307">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3308">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3308">Checksum</span></span>

<span data-ttu-id="a9974-3309">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3309">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3310">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3310">Definition</span></span>

<span data-ttu-id="a9974-3311">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3311">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3312">정규식 Regex_taiwan_resident_certificate 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3312">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3313">Keyword_taiwan_resident_certificate에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3313">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3314">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3314">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="a9974-3315">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="a9974-3315">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="a9974-3316">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="a9974-3316">Resident Certificate</span></span> 
- <span data-ttu-id="a9974-3317">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="a9974-3317">Resident Cert</span></span> 
- <span data-ttu-id="a9974-3318">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="a9974-3318">Resident Cert.</span></span> 
- <span data-ttu-id="a9974-3319">Identification card</span><span class="sxs-lookup"><span data-stu-id="a9974-3319">Identification card</span></span> 
- <span data-ttu-id="a9974-3320">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="a9974-3320">Alien Resident Certificate</span></span> 
- <span data-ttu-id="a9974-3321">화살표</span><span class="sxs-lookup"><span data-stu-id="a9974-3321">ARC</span></span> 
- <span data-ttu-id="a9974-3322">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="a9974-3322">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="a9974-3323">TARC</span><span class="sxs-lookup"><span data-stu-id="a9974-3323">TARC</span></span> 
- <span data-ttu-id="a9974-3324">居留證</span><span class="sxs-lookup"><span data-stu-id="a9974-3324">居留證</span></span> 
- <span data-ttu-id="a9974-3325">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="a9974-3325">外僑居留證</span></span> 
- <span data-ttu-id="a9974-3326">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="a9974-3326">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="a9974-3327">태국어 인구 식별 코드</span><span class="sxs-lookup"><span data-stu-id="a9974-3327">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3328">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3328">Format</span></span>

<span data-ttu-id="a9974-3329">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3329">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3330">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3330">Pattern</span></span>

<span data-ttu-id="a9974-3331">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3331">13 digits:</span></span>
- <span data-ttu-id="a9974-3332">첫 번째 숫자가 0 또는 9가 아님</span><span class="sxs-lookup"><span data-stu-id="a9974-3332">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="a9974-3333">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3333">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3334">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3334">Checksum</span></span>

<span data-ttu-id="a9974-3335">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3335">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3336">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3336">Definition</span></span>

<span data-ttu-id="a9974-3337">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3337">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3338">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3338">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3339">Keyword_Thai_Citizen_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3339">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="a9974-3340">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3340">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3341">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3341">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3342">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3342">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="a9974-3343">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="a9974-3343">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="a9974-3344">ID Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3344">ID Number</span></span>
- <span data-ttu-id="a9974-3345">id 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3345">Identification Number</span></span>
- <span data-ttu-id="a9974-3346">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="a9974-3346">บัตรประชาชน</span></span>
- <span data-ttu-id="a9974-3347">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="a9974-3347">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="a9974-3348">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="a9974-3348">บัตรประชาชน</span></span>
- <span data-ttu-id="a9974-3349">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="a9974-3349">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="a9974-3350">터키어 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3350">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3351">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3351">Format</span></span>

<span data-ttu-id="a9974-3352">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3352">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3353">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3353">Pattern</span></span>

<span data-ttu-id="a9974-3354">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3354">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3355">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3355">Checksum</span></span>

<span data-ttu-id="a9974-3356">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3356">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3357">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3357">Definition</span></span>

<span data-ttu-id="a9974-3358">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3358">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3359">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3359">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3360">Keyword_Turkish_National_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3360">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="a9974-3361">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3362">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3362">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3363">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3363">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="a9974-3364">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="a9974-3364">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="a9974-3365">TC Kimlik 아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3365">TC Kimlik No</span></span>
- <span data-ttu-id="a9974-3366">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="a9974-3366">TC Kimlik numarası</span></span>
- <span data-ttu-id="a9974-3367">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="a9974-3367">Vatandaşlık numarası</span></span>
- <span data-ttu-id="a9974-3368">Vatandaşlık 아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3368">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="a9974-p141">영국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3371">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3371">Format</span></span>

<span data-ttu-id="a9974-3372">지정된 형식의 18개 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="a9974-3372">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3373">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3373">Pattern</span></span>

<span data-ttu-id="a9974-3374">18개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3374">18 letters and digits:</span></span>
- <span data-ttu-id="a9974-3375">5개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="a9974-3375">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="a9974-3376">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3376">One digit</span></span> 
- <span data-ttu-id="a9974-3377">생년월일에 대한 DDMMY 날짜 형식의 5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3377">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="a9974-3378">2개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="a9974-3378">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="a9974-3379">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3379">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3380">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3380">Checksum</span></span>

<span data-ttu-id="a9974-3381">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3382">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3382">Definition</span></span>

<span data-ttu-id="a9974-3383">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3383">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3384">Func_uk_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3384">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3385">Keyword_uk_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3385">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="a9974-3386">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3386">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3387">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3387">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="a9974-3388">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="a9974-3388">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="a9974-3389">dvla</span><span class="sxs-lookup"><span data-stu-id="a9974-3389">DVLA</span></span> 
- <span data-ttu-id="a9974-3390">light vans</span><span class="sxs-lookup"><span data-stu-id="a9974-3390">light vans</span></span> 
- <span data-ttu-id="a9974-3391">quadbikes</span><span class="sxs-lookup"><span data-stu-id="a9974-3391">quadbikes</span></span> 
- <span data-ttu-id="a9974-3392">motor cars</span><span class="sxs-lookup"><span data-stu-id="a9974-3392">motor cars</span></span> 
- <span data-ttu-id="a9974-3393">125cc</span><span class="sxs-lookup"><span data-stu-id="a9974-3393">125cc</span></span> 
- <span data-ttu-id="a9974-3394">sidecar</span><span class="sxs-lookup"><span data-stu-id="a9974-3394">sidecar</span></span> 
- <span data-ttu-id="a9974-3395">tricycles</span><span class="sxs-lookup"><span data-stu-id="a9974-3395">tricycles</span></span> 
- <span data-ttu-id="a9974-3396">motorcycles</span><span class="sxs-lookup"><span data-stu-id="a9974-3396">motorcycles</span></span> 
- <span data-ttu-id="a9974-3397">photocard licence</span><span class="sxs-lookup"><span data-stu-id="a9974-3397">photocard licence</span></span> 
- <span data-ttu-id="a9974-3398">learner drivers</span><span class="sxs-lookup"><span data-stu-id="a9974-3398">learner drivers</span></span> 
- <span data-ttu-id="a9974-3399">licence holder</span><span class="sxs-lookup"><span data-stu-id="a9974-3399">licence holder</span></span> 
- <span data-ttu-id="a9974-3400">licence holders</span><span class="sxs-lookup"><span data-stu-id="a9974-3400">licence holders</span></span> 
- <span data-ttu-id="a9974-3401">driving licences</span><span class="sxs-lookup"><span data-stu-id="a9974-3401">driving licences</span></span> 
- <span data-ttu-id="a9974-3402">driving licence</span><span class="sxs-lookup"><span data-stu-id="a9974-3402">driving licence</span></span> 
- <span data-ttu-id="a9974-3403">dual control car</span><span class="sxs-lookup"><span data-stu-id="a9974-3403">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="a9974-p142">영국 선거 롤 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3406">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3406">Format</span></span>

<span data-ttu-id="a9974-3407">2개의 문자, 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3407">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3408">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3408">Pattern</span></span>

<span data-ttu-id="a9974-3409">2개의 문자(대/소문자 구분 안 함)와 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3409">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3410">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3410">Checksum</span></span>

<span data-ttu-id="a9974-3411">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3411">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3412">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3412">Definition</span></span>

<span data-ttu-id="a9974-3413">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3413">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3414">Regex_uk_electoral 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3414">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3415">Keyword_uk_electoral의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3415">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3416">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3416">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="a9974-3417">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="a9974-3417">Keyword_uk_electoral</span></span>

- <span data-ttu-id="a9974-3418">council nomination</span><span class="sxs-lookup"><span data-stu-id="a9974-3418">council nomination</span></span> 
- <span data-ttu-id="a9974-3419">nomination form</span><span class="sxs-lookup"><span data-stu-id="a9974-3419">nomination form</span></span> 
- <span data-ttu-id="a9974-3420">electoral register</span><span class="sxs-lookup"><span data-stu-id="a9974-3420">electoral register</span></span> 
- <span data-ttu-id="a9974-3421">electoral roll</span><span class="sxs-lookup"><span data-stu-id="a9974-3421">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="a9974-p143">영국 국립 보건 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3424">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3424">Format</span></span>

<span data-ttu-id="a9974-3425">공백으로 구분된 10-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3425">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3426">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3426">Pattern</span></span>

<span data-ttu-id="a9974-3427">10-17자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="a9974-3427">10-17 digits:</span></span>
- <span data-ttu-id="a9974-3428">3 또는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3428">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="a9974-3429">공백</span><span class="sxs-lookup"><span data-stu-id="a9974-3429">A space</span></span> 
- <span data-ttu-id="a9974-3430">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3430">Three digits</span></span> 
- <span data-ttu-id="a9974-3431">공백</span><span class="sxs-lookup"><span data-stu-id="a9974-3431">A space</span></span> 
- <span data-ttu-id="a9974-3432">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3432">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3433">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3433">Checksum</span></span>

<span data-ttu-id="a9974-3434">예</span><span class="sxs-lookup"><span data-stu-id="a9974-3434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3435">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3435">Definition</span></span>

<span data-ttu-id="a9974-3436">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3437">Func_uk_nhs_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3437">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3438">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3438">One of the following is true:</span></span>
    - <span data-ttu-id="a9974-3439">Keyword_uk_nhs_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3439">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="a9974-3440">Keyword_uk_nhs_number1의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3440">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="a9974-3441">Keyword_uk_nhs_number_dob의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3441">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="a9974-3442">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3442">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3443">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3443">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="a9974-3444">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="a9974-3444">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="a9974-3445">국립 보건 서비스</span><span class="sxs-lookup"><span data-stu-id="a9974-3445">national health service</span></span> 
- <span data-ttu-id="a9974-3446">nhs</span><span class="sxs-lookup"><span data-stu-id="a9974-3446">nhs</span></span> 
- <span data-ttu-id="a9974-3447">health services authority</span><span class="sxs-lookup"><span data-stu-id="a9974-3447">health services authority</span></span> 
- <span data-ttu-id="a9974-3448">health authority</span><span class="sxs-lookup"><span data-stu-id="a9974-3448">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="a9974-3449">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="a9974-3449">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="a9974-3450">patient id</span><span class="sxs-lookup"><span data-stu-id="a9974-3450">patient id</span></span> 
- <span data-ttu-id="a9974-3451">patient identification</span><span class="sxs-lookup"><span data-stu-id="a9974-3451">patient identification</span></span> 
- <span data-ttu-id="a9974-3452">patient no</span><span class="sxs-lookup"><span data-stu-id="a9974-3452">patient no</span></span> 
- <span data-ttu-id="a9974-3453">patient number</span><span class="sxs-lookup"><span data-stu-id="a9974-3453">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="a9974-3454">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="a9974-3454">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="a9974-3455">g</span><span class="sxs-lookup"><span data-stu-id="a9974-3455">GP</span></span> 
- <span data-ttu-id="a9974-3456">dob</span><span class="sxs-lookup"><span data-stu-id="a9974-3456">DOB</span></span> 
- <span data-ttu-id="a9974-3457">D. O. B</span><span class="sxs-lookup"><span data-stu-id="a9974-3457">D.O.B</span></span> 
- <span data-ttu-id="a9974-3458">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="a9974-3458">Date of Birth</span></span> 
- <span data-ttu-id="a9974-3459">Birth Date</span><span class="sxs-lookup"><span data-stu-id="a9974-3459">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="a9974-p144">영국 NINO(국민 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="a9974-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3462">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3462">Format</span></span>

<span data-ttu-id="a9974-3463">공백 또는 대시로 구분 된 7 자 또는 9 자</span><span class="sxs-lookup"><span data-stu-id="a9974-3463">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3464">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3464">Pattern</span></span>

<span data-ttu-id="a9974-3465">다음과 같은 두 가지 패턴을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3465">Two possible patterns:</span></span>

- <span data-ttu-id="a9974-3466">두 문자 (유효한 NINOs이 접두사의 특정 문자만 사용 하며이 패턴의 유효성 검사는 대/소문자를 구분 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="a9974-3466">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="a9974-3467">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3467">Six digits</span></span>
- <span data-ttu-id="a9974-3468">' A ', ' B ', ' C ' 또는 ' d ' (접두사와 마찬가지로 접미사에서는 특정 문자만 허용 되며 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="a9974-3468">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="a9974-3469">또는</span><span class="sxs-lookup"><span data-stu-id="a9974-3469">OR</span></span>

- <span data-ttu-id="a9974-3470">2 개 문자</span><span class="sxs-lookup"><span data-stu-id="a9974-3470">Two letters</span></span>
- <span data-ttu-id="a9974-3471">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="a9974-3471">A space or dash</span></span>
- <span data-ttu-id="a9974-3472">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3472">Two digits</span></span>
- <span data-ttu-id="a9974-3473">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="a9974-3473">A space or dash</span></span>
- <span data-ttu-id="a9974-3474">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3474">Two digits</span></span>
- <span data-ttu-id="a9974-3475">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="a9974-3475">A space or dash</span></span>
- <span data-ttu-id="a9974-3476">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3476">Two digits</span></span>
- <span data-ttu-id="a9974-3477">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="a9974-3477">A space or dash</span></span>
- <span data-ttu-id="a9974-3478">' A ', ' B ', ' C ' 또는 ' d ' 중 하나</span><span class="sxs-lookup"><span data-stu-id="a9974-3478">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3479">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3479">Checksum</span></span>

<span data-ttu-id="a9974-3480">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3480">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3481">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3481">Definition</span></span>

<span data-ttu-id="a9974-3482">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3482">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3483">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3483">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3484">Keyword_uk_nino의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3484">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="a9974-3485">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3485">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3486">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3486">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3487">Keyword_uk_nino의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3487">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3488">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3488">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="a9974-3489">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="a9974-3489">Keyword_uk_nino</span></span>

- <span data-ttu-id="a9974-3490">national insurance number</span><span class="sxs-lookup"><span data-stu-id="a9974-3490">national insurance number</span></span> 
- <span data-ttu-id="a9974-3491">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="a9974-3491">national insurance contributions</span></span> 
- <span data-ttu-id="a9974-3492">protection act</span><span class="sxs-lookup"><span data-stu-id="a9974-3492">protection act</span></span> 
- <span data-ttu-id="a9974-3493">소유권</span><span class="sxs-lookup"><span data-stu-id="a9974-3493">insurance</span></span> 
- <span data-ttu-id="a9974-3494">social security number</span><span class="sxs-lookup"><span data-stu-id="a9974-3494">social security number</span></span> 
- <span data-ttu-id="a9974-3495">insurance application</span><span class="sxs-lookup"><span data-stu-id="a9974-3495">insurance application</span></span> 
- <span data-ttu-id="a9974-3496">medical application</span><span class="sxs-lookup"><span data-stu-id="a9974-3496">medical application</span></span> 
- <span data-ttu-id="a9974-3497">social insurance</span><span class="sxs-lookup"><span data-stu-id="a9974-3497">social insurance</span></span> 
- <span data-ttu-id="a9974-3498">medical attention</span><span class="sxs-lookup"><span data-stu-id="a9974-3498">medical attention</span></span> 
- <span data-ttu-id="a9974-3499">social security</span><span class="sxs-lookup"><span data-stu-id="a9974-3499">social security</span></span> 
- <span data-ttu-id="a9974-3500">great britain</span><span class="sxs-lookup"><span data-stu-id="a9974-3500">great britain</span></span> 
- <span data-ttu-id="a9974-3501">소유권</span><span class="sxs-lookup"><span data-stu-id="a9974-3501">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="a9974-p145">미국/영국 여권 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3504">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3504">Format</span></span>

<span data-ttu-id="a9974-3505">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3505">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3506">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3506">Pattern</span></span>

<span data-ttu-id="a9974-3507">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3507">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3508">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3508">Checksum</span></span>

<span data-ttu-id="a9974-3509">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3509">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3510">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3510">Definition</span></span>

<span data-ttu-id="a9974-3511">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3511">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3512">Func_usa_uk_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3512">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3513">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3513">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3514">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3514">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="a9974-3515">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="a9974-3515">Keyword_passport</span></span>

- <span data-ttu-id="a9974-3516">Passport Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3516">Passport Number</span></span> 
- <span data-ttu-id="a9974-3517">Passport No</span><span class="sxs-lookup"><span data-stu-id="a9974-3517">Passport No</span></span> 
- <span data-ttu-id="a9974-3518">Passport #</span><span class="sxs-lookup"><span data-stu-id="a9974-3518">Passport #</span></span> 
- <span data-ttu-id="a9974-3519">여권</span><span class="sxs-lookup"><span data-stu-id="a9974-3519">Passport#</span></span> 
- <span data-ttu-id="a9974-3520">PassportID</span><span class="sxs-lookup"><span data-stu-id="a9974-3520">PassportID</span></span> 
- <span data-ttu-id="a9974-3521">Passportno</span><span class="sxs-lookup"><span data-stu-id="a9974-3521">Passportno</span></span> 
- <span data-ttu-id="a9974-3522">passportnumber</span><span class="sxs-lookup"><span data-stu-id="a9974-3522">passportnumber</span></span> 
- <span data-ttu-id="a9974-3523">パスポート</span><span class="sxs-lookup"><span data-stu-id="a9974-3523">パスポート</span></span> 
- <span data-ttu-id="a9974-3524">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="a9974-3524">パスポート番号</span></span> 
- <span data-ttu-id="a9974-3525">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="a9974-3525">パスポートのNum</span></span> 
- <span data-ttu-id="a9974-3526">パスポート #</span><span class="sxs-lookup"><span data-stu-id="a9974-3526">パスポート＃</span></span> 
- <span data-ttu-id="a9974-3527">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="a9974-3527">Numéro de passeport</span></span> 
- <span data-ttu-id="a9974-3528">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="a9974-3528">Passeport n °</span></span> 
- <span data-ttu-id="a9974-3529">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="a9974-3529">Passeport Non</span></span> 
- <span data-ttu-id="a9974-3530">Passeport #</span><span class="sxs-lookup"><span data-stu-id="a9974-3530">Passeport #</span></span> 
- <span data-ttu-id="a9974-3531">포트 #</span><span class="sxs-lookup"><span data-stu-id="a9974-3531">Passeport#</span></span> 
- <span data-ttu-id="a9974-3532">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="a9974-3532">PasseportNon</span></span> 
- <span data-ttu-id="a9974-3533">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="a9974-3533">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="a9974-3534">미국 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3534">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3535">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3535">Format</span></span>

<span data-ttu-id="a9974-3536">8-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3536">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3537">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3537">Pattern</span></span>

<span data-ttu-id="a9974-3538">8-17자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3538">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3539">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3539">Checksum</span></span>

<span data-ttu-id="a9974-3540">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3540">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3541">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3541">Definition</span></span>

<span data-ttu-id="a9974-3542">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3542">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3543">Regex_usa_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3543">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3544">Keyword_usa_Bank_Account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3544">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a9974-3545">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3545">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="a9974-3546">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="a9974-3546">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="a9974-3547">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3547">Checking Account Number</span></span> 
- <span data-ttu-id="a9974-3548">Checking Account</span><span class="sxs-lookup"><span data-stu-id="a9974-3548">Checking Account</span></span> 
- <span data-ttu-id="a9974-3549">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="a9974-3549">Checking Account #</span></span> 
- <span data-ttu-id="a9974-3550">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3550">Checking Acct Number</span></span> 
- <span data-ttu-id="a9974-3551">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="a9974-3551">Checking Acct #</span></span> 
- <span data-ttu-id="a9974-3552">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="a9974-3552">Checking Acct No.</span></span> 
- <span data-ttu-id="a9974-3553">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="a9974-3553">Checking Account No.</span></span> 
- <span data-ttu-id="a9974-3554">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3554">Bank Account Number</span></span> 
- <span data-ttu-id="a9974-3555">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="a9974-3555">Bank Account #</span></span> 
- <span data-ttu-id="a9974-3556">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3556">Bank Acct Number</span></span> 
- <span data-ttu-id="a9974-3557">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="a9974-3557">Bank Acct #</span></span> 
- <span data-ttu-id="a9974-3558">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="a9974-3558">Bank Acct No.</span></span> 
- <span data-ttu-id="a9974-3559">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="a9974-3559">Bank Account No.</span></span> 
- <span data-ttu-id="a9974-3560">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3560">Savings Account Number</span></span> 
- <span data-ttu-id="a9974-3561">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="a9974-3561">Savings Account.</span></span> 
- <span data-ttu-id="a9974-3562">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="a9974-3562">Savings Account #</span></span> 
- <span data-ttu-id="a9974-3563">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3563">Savings Acct Number</span></span> 
- <span data-ttu-id="a9974-3564">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="a9974-3564">Savings Acct #</span></span> 
- <span data-ttu-id="a9974-3565">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="a9974-3565">Savings Acct No.</span></span> 
- <span data-ttu-id="a9974-3566">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="a9974-3566">Savings Account No.</span></span> 
- <span data-ttu-id="a9974-3567">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3567">Debit Account Number</span></span> 
- <span data-ttu-id="a9974-3568">Debit Account</span><span class="sxs-lookup"><span data-stu-id="a9974-3568">Debit Account</span></span> 
- <span data-ttu-id="a9974-3569">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="a9974-3569">Debit Account #</span></span> 
- <span data-ttu-id="a9974-3570">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="a9974-3570">Debit Acct Number</span></span> 
- <span data-ttu-id="a9974-3571">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="a9974-3571">Debit Acct #</span></span> 
- <span data-ttu-id="a9974-3572">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="a9974-3572">Debit Acct No.</span></span> 
- <span data-ttu-id="a9974-3573">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="a9974-3573">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="a9974-3574">미국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="a9974-3574">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3575">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3575">Format</span></span>

<span data-ttu-id="a9974-3576">주마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3576">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3577">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3577">Pattern</span></span>

<span data-ttu-id="a9974-3578">주마다 다릅니다(예: 뉴욕).</span><span class="sxs-lookup"><span data-stu-id="a9974-3578">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="a9974-3579">ddd ddd ddd와 같이 9 자리 숫자는 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3579">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="a9974-3580">ddddddddd와 같은 9 자리 숫자가 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3580">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3581">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3581">Checksum</span></span>

<span data-ttu-id="a9974-3582">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3582">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3583">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3583">Definition</span></span>

<span data-ttu-id="a9974-3584">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3585">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3585">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3586">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3586">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="a9974-3587">Keyword_us_drivers_license에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3587">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="a9974-3588">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3588">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3589">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3589">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3590">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3590">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="a9974-3591">Keyword_us_drivers_license_abbreviations의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3591">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="a9974-3592">Keyword_us_drivers_license의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3592">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3593">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3593">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="a9974-3594">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="a9974-3594">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="a9974-3595">DL</span><span class="sxs-lookup"><span data-stu-id="a9974-3595">DL</span></span> 
- <span data-ttu-id="a9974-3596">된다</span><span class="sxs-lookup"><span data-stu-id="a9974-3596">DLS</span></span> 
- <span data-ttu-id="a9974-3597">cdl</span><span class="sxs-lookup"><span data-stu-id="a9974-3597">CDL</span></span> 
- <span data-ttu-id="a9974-3598">cdls</span><span class="sxs-lookup"><span data-stu-id="a9974-3598">CDLS</span></span> 
- <span data-ttu-id="a9974-3599">ID</span><span class="sxs-lookup"><span data-stu-id="a9974-3599">ID</span></span> 
- <span data-ttu-id="a9974-3600">번호가</span><span class="sxs-lookup"><span data-stu-id="a9974-3600">IDs</span></span> 
- <span data-ttu-id="a9974-3601">DL</span><span class="sxs-lookup"><span data-stu-id="a9974-3601">DL#</span></span> 
- <span data-ttu-id="a9974-3602">된다</span><span class="sxs-lookup"><span data-stu-id="a9974-3602">DLS#</span></span> 
- <span data-ttu-id="a9974-3603">cdl #</span><span class="sxs-lookup"><span data-stu-id="a9974-3603">CDL#</span></span> 
- <span data-ttu-id="a9974-3604">cdls #</span><span class="sxs-lookup"><span data-stu-id="a9974-3604">CDLS#</span></span> 
- <span data-ttu-id="a9974-3605">i</span><span class="sxs-lookup"><span data-stu-id="a9974-3605">ID#</span></span>
- <span data-ttu-id="a9974-3606">번호가</span><span class="sxs-lookup"><span data-stu-id="a9974-3606">IDs#</span></span> 
- <span data-ttu-id="a9974-3607">ID number</span><span class="sxs-lookup"><span data-stu-id="a9974-3607">ID number</span></span> 
- <span data-ttu-id="a9974-3608">ID numbers</span><span class="sxs-lookup"><span data-stu-id="a9974-3608">ID numbers</span></span> 
- <span data-ttu-id="a9974-3609">LIC</span><span class="sxs-lookup"><span data-stu-id="a9974-3609">LIC</span></span> 
- <span data-ttu-id="a9974-3610">LIC</span><span class="sxs-lookup"><span data-stu-id="a9974-3610">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="a9974-3611">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="a9974-3611">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="a9974-3612">driverlic</span><span class="sxs-lookup"><span data-stu-id="a9974-3612">DriverLic</span></span> 
- <span data-ttu-id="a9974-3613">driverlics</span><span class="sxs-lookup"><span data-stu-id="a9974-3613">DriverLics</span></span> 
- <span data-ttu-id="a9974-3614">driverlicense</span><span class="sxs-lookup"><span data-stu-id="a9974-3614">DriverLicense</span></span> 
- <span data-ttu-id="a9974-3615">driverlicenses</span><span class="sxs-lookup"><span data-stu-id="a9974-3615">DriverLicenses</span></span> 
- <span data-ttu-id="a9974-3616">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-3616">Driver Lic</span></span> 
- <span data-ttu-id="a9974-3617">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-3617">Driver Lics</span></span> 
- <span data-ttu-id="a9974-3618">Driver License</span><span class="sxs-lookup"><span data-stu-id="a9974-3618">Driver License</span></span> 
- <span data-ttu-id="a9974-3619">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-3619">Driver Licenses</span></span> 
- <span data-ttu-id="a9974-3620">DriversLic</span><span class="sxs-lookup"><span data-stu-id="a9974-3620">DriversLic</span></span> 
- <span data-ttu-id="a9974-3621">driverslics</span><span class="sxs-lookup"><span data-stu-id="a9974-3621">DriversLics</span></span> 
- <span data-ttu-id="a9974-3622">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-3622">DriversLicense</span></span> 
- <span data-ttu-id="a9974-3623">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-3623">DriversLicenses</span></span> 
- <span data-ttu-id="a9974-3624">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-3624">Drivers Lic</span></span> 
- <span data-ttu-id="a9974-3625">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-3625">Drivers Lics</span></span> 
- <span data-ttu-id="a9974-3626">Drivers License</span><span class="sxs-lookup"><span data-stu-id="a9974-3626">Drivers License</span></span> 
- <span data-ttu-id="a9974-3627">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-3627">Drivers Licenses</span></span> 
- <span data-ttu-id="a9974-3628">driver' Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-3628">Driver'Lic</span></span> 
- <span data-ttu-id="a9974-3629">driver'lics</span><span class="sxs-lookup"><span data-stu-id="a9974-3629">Driver'Lics</span></span> 
- <span data-ttu-id="a9974-3630">driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="a9974-3630">Driver'License</span></span> 
- <span data-ttu-id="a9974-3631">driver'licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-3631">Driver'Licenses</span></span> 
- <span data-ttu-id="a9974-3632">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-3632">Driver' Lic</span></span> 
- <span data-ttu-id="a9974-3633">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-3633">Driver' Lics</span></span> 
- <span data-ttu-id="a9974-3634">Driver' License</span><span class="sxs-lookup"><span data-stu-id="a9974-3634">Driver' License</span></span> 
- <span data-ttu-id="a9974-3635">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-3635">Driver' Licenses</span></span>
- <span data-ttu-id="a9974-3636">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="a9974-3636">Driver'sLic</span></span> 
- <span data-ttu-id="a9974-3637">drivers (slics)</span><span class="sxs-lookup"><span data-stu-id="a9974-3637">Driver'sLics</span></span> 
- <span data-ttu-id="a9974-3638">driver'slicense</span><span class="sxs-lookup"><span data-stu-id="a9974-3638">Driver'sLicense</span></span> 
- <span data-ttu-id="a9974-3639">driver'slicenses</span><span class="sxs-lookup"><span data-stu-id="a9974-3639">Driver'sLicenses</span></span> 
- <span data-ttu-id="a9974-3640">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="a9974-3640">Driver's Lic</span></span> 
- <span data-ttu-id="a9974-3641">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="a9974-3641">Driver's Lics</span></span> 
- <span data-ttu-id="a9974-3642">Driver's License</span><span class="sxs-lookup"><span data-stu-id="a9974-3642">Driver's License</span></span> 
- <span data-ttu-id="a9974-3643">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="a9974-3643">Driver's Licenses</span></span> 
- <span data-ttu-id="a9974-3644">identification number</span><span class="sxs-lookup"><span data-stu-id="a9974-3644">identification number</span></span> 
- <span data-ttu-id="a9974-3645">identification numbers</span><span class="sxs-lookup"><span data-stu-id="a9974-3645">identification numbers</span></span> 
- <span data-ttu-id="a9974-3646">identification #</span><span class="sxs-lookup"><span data-stu-id="a9974-3646">identification #</span></span> 
- <span data-ttu-id="a9974-3647">id card</span><span class="sxs-lookup"><span data-stu-id="a9974-3647">id card</span></span> 
- <span data-ttu-id="a9974-3648">id cards</span><span class="sxs-lookup"><span data-stu-id="a9974-3648">id cards</span></span> 
- <span data-ttu-id="a9974-3649">identification card</span><span class="sxs-lookup"><span data-stu-id="a9974-3649">identification card</span></span> 
- <span data-ttu-id="a9974-3650">identification cards</span><span class="sxs-lookup"><span data-stu-id="a9974-3650">identification cards</span></span> 
- <span data-ttu-id="a9974-3651">driverlic #</span><span class="sxs-lookup"><span data-stu-id="a9974-3651">DriverLic#</span></span> 
- <span data-ttu-id="a9974-3652">driverlics #</span><span class="sxs-lookup"><span data-stu-id="a9974-3652">DriverLics#</span></span> 
- <span data-ttu-id="a9974-3653">driverlicense #</span><span class="sxs-lookup"><span data-stu-id="a9974-3653">DriverLicense#</span></span> 
- <span data-ttu-id="a9974-3654">driverlicenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-3654">DriverLicenses#</span></span> 
- <span data-ttu-id="a9974-3655">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-3655">Driver Lic#</span></span> 
- <span data-ttu-id="a9974-3656">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-3656">Driver Lics#</span></span> 
- <span data-ttu-id="a9974-3657">Driver License#</span><span class="sxs-lookup"><span data-stu-id="a9974-3657">Driver License#</span></span> 
- <span data-ttu-id="a9974-3658">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-3658">Driver Licenses#</span></span> 
- <span data-ttu-id="a9974-3659">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="a9974-3659">DriversLic#</span></span> 
- <span data-ttu-id="a9974-3660">driverslics #</span><span class="sxs-lookup"><span data-stu-id="a9974-3660">DriversLics#</span></span> 
- <span data-ttu-id="a9974-3661">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-3661">DriversLicense#</span></span> 
- <span data-ttu-id="a9974-3662">드라이버 라이선스 수</span><span class="sxs-lookup"><span data-stu-id="a9974-3662">DriversLicenses#</span></span> 
- <span data-ttu-id="a9974-3663">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-3663">Drivers Lic#</span></span> 
- <span data-ttu-id="a9974-3664">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-3664">Drivers Lics#</span></span> 
- <span data-ttu-id="a9974-3665">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="a9974-3665">Drivers License#</span></span> 
- <span data-ttu-id="a9974-3666">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-3666">Drivers Licenses#</span></span> 
- <span data-ttu-id="a9974-3667">driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="a9974-3667">Driver'Lic#</span></span> 
- <span data-ttu-id="a9974-3668">driver'lics #</span><span class="sxs-lookup"><span data-stu-id="a9974-3668">Driver'Lics#</span></span> 
- <span data-ttu-id="a9974-3669">driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="a9974-3669">Driver'License#</span></span> 
- <span data-ttu-id="a9974-3670">driver'licenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-3670">Driver'Licenses#</span></span> 
- <span data-ttu-id="a9974-3671">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-3671">Driver' Lic#</span></span> 
- <span data-ttu-id="a9974-3672">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-3672">Driver' Lics#</span></span> 
- <span data-ttu-id="a9974-3673">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="a9974-3673">Driver' License#</span></span> 
- <span data-ttu-id="a9974-3674">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-3674">Driver' Licenses#</span></span> 
- <span data-ttu-id="a9974-3675">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="a9974-3675">Driver'sLic#</span></span> 
- <span data-ttu-id="a9974-3676">drivers (slics #)</span><span class="sxs-lookup"><span data-stu-id="a9974-3676">Driver'sLics#</span></span> 
- <span data-ttu-id="a9974-3677">driver'slicense #</span><span class="sxs-lookup"><span data-stu-id="a9974-3677">Driver'sLicense#</span></span> 
- <span data-ttu-id="a9974-3678">driver'slicenses #</span><span class="sxs-lookup"><span data-stu-id="a9974-3678">Driver'sLicenses#</span></span> 
- <span data-ttu-id="a9974-3679">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="a9974-3679">Driver's Lic#</span></span> 
- <span data-ttu-id="a9974-3680">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="a9974-3680">Driver's Lics#</span></span> 
- <span data-ttu-id="a9974-3681">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="a9974-3681">Driver's License#</span></span> 
- <span data-ttu-id="a9974-3682">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="a9974-3682">Driver's Licenses#</span></span> 
- <span data-ttu-id="a9974-3683">id card#</span><span class="sxs-lookup"><span data-stu-id="a9974-3683">id card#</span></span> 
- <span data-ttu-id="a9974-3684">id cards#</span><span class="sxs-lookup"><span data-stu-id="a9974-3684">id cards#</span></span> 
- <span data-ttu-id="a9974-3685">identification card#</span><span class="sxs-lookup"><span data-stu-id="a9974-3685">identification card#</span></span> 
- <span data-ttu-id="a9974-3686">identification cards#</span><span class="sxs-lookup"><span data-stu-id="a9974-3686">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="a9974-3687">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="a9974-3687">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="a9974-3688">주 약어(예: "NY")</span><span class="sxs-lookup"><span data-stu-id="a9974-3688">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="a9974-3689">주 이름(예: "New York")</span><span class="sxs-lookup"><span data-stu-id="a9974-3689">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="a9974-3690">미국 ITIN(개인 납세자 번호)</span><span class="sxs-lookup"><span data-stu-id="a9974-3690">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3691">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3691">Format</span></span>

<span data-ttu-id="a9974-3692">"9"로 시작되고, "7" 또는 "8"을 4번째 숫자로 포함하고, 경우에 따라 공백이나 대시로 서식이 지정된 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3692">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3693">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3693">Pattern</span></span>

<span data-ttu-id="a9974-3694">서식이</span><span class="sxs-lookup"><span data-stu-id="a9974-3694">Formatted:</span></span>
- <span data-ttu-id="a9974-3695">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3695">The digit "9"</span></span> 
- <span data-ttu-id="a9974-3696">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3696">Two digits</span></span> 
- <span data-ttu-id="a9974-3697">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="a9974-3697">A space or dash</span></span> 
- <span data-ttu-id="a9974-3698">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="a9974-3698">A "7" or "8"</span></span> 
- <span data-ttu-id="a9974-3699">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3699">A digit</span></span> 
- <span data-ttu-id="a9974-3700">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="a9974-3700">A space, or dash</span></span> 
- <span data-ttu-id="a9974-3701">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3701">Four digits</span></span>

<span data-ttu-id="a9974-3702">서식</span><span class="sxs-lookup"><span data-stu-id="a9974-3702">Unformatted:</span></span>
- <span data-ttu-id="a9974-3703">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3703">The digit "9"</span></span> 
- <span data-ttu-id="a9974-3704">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3704">Two digits</span></span> 
- <span data-ttu-id="a9974-3705">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="a9974-3705">A "7" or "8"</span></span> 
- <span data-ttu-id="a9974-3706">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3706">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3707">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3707">Checksum</span></span>

<span data-ttu-id="a9974-3708">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3708">No</span></span>

### <a name="definition"></a><span data-ttu-id="a9974-3709">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3709">Definition</span></span>

<span data-ttu-id="a9974-3710">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3710">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3711">Func_formatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3711">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3712">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3712">At least one of the following is true:</span></span>
    - <span data-ttu-id="a9974-3713">Keyword_itin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3713">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="a9974-3714">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3714">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="a9974-3715">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3715">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="a9974-3716">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3716">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="a9974-3717">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3717">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3718">Func_unformatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3718">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3719">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3719">At least one of the following is true:</span></span>
    - <span data-ttu-id="a9974-3720">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3720">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="a9974-3721">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3721">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="a9974-3722">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3722">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3723">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3723">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="a9974-3724">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="a9974-3724">Keyword_itin</span></span>

- <span data-ttu-id="a9974-3725">taxpayer</span><span class="sxs-lookup"><span data-stu-id="a9974-3725">taxpayer</span></span> 
- <span data-ttu-id="a9974-3726">tax id</span><span class="sxs-lookup"><span data-stu-id="a9974-3726">tax id</span></span> 
- <span data-ttu-id="a9974-3727">tax identification</span><span class="sxs-lookup"><span data-stu-id="a9974-3727">tax identification</span></span> 
- <span data-ttu-id="a9974-3728">itin</span><span class="sxs-lookup"><span data-stu-id="a9974-3728">itin</span></span> 
- <span data-ttu-id="a9974-3729">ssn</span><span class="sxs-lookup"><span data-stu-id="a9974-3729">ssn</span></span> 
- <span data-ttu-id="a9974-3730">언급</span><span class="sxs-lookup"><span data-stu-id="a9974-3730">tin</span></span> 
- <span data-ttu-id="a9974-3731">social security</span><span class="sxs-lookup"><span data-stu-id="a9974-3731">social security</span></span> 
- <span data-ttu-id="a9974-3732">tax payer</span><span class="sxs-lookup"><span data-stu-id="a9974-3732">tax payer</span></span> 
- <span data-ttu-id="a9974-3733">itins</span><span class="sxs-lookup"><span data-stu-id="a9974-3733">itins</span></span> 
- <span data-ttu-id="a9974-3734">taxid</span><span class="sxs-lookup"><span data-stu-id="a9974-3734">taxid</span></span> 
- <span data-ttu-id="a9974-3735">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="a9974-3735">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="a9974-3736">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="a9974-3736">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="a9974-3737">License</span><span class="sxs-lookup"><span data-stu-id="a9974-3737">License</span></span> 
- <span data-ttu-id="a9974-3738">DL</span><span class="sxs-lookup"><span data-stu-id="a9974-3738">DL</span></span> 
- <span data-ttu-id="a9974-3739">dob</span><span class="sxs-lookup"><span data-stu-id="a9974-3739">DOB</span></span> 
- <span data-ttu-id="a9974-3740">생년월일</span><span class="sxs-lookup"><span data-stu-id="a9974-3740">Birthdate</span></span> 
- <span data-ttu-id="a9974-3741">생일</span><span class="sxs-lookup"><span data-stu-id="a9974-3741">Birthday</span></span> 
- <span data-ttu-id="a9974-3742">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="a9974-3742">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="a9974-3743">미국 SSN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="a9974-3743">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="a9974-3744">형식일</span><span class="sxs-lookup"><span data-stu-id="a9974-3744">Format</span></span>

<span data-ttu-id="a9974-3745">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="a9974-3745">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="a9974-3746">mid가 2011 이전에 실행 된 경우 SSN은 특정 범위 내에서 번호의 특정 부분이 유효한 지 확인 하는 강력한 서식을 사용 해야 하지만 검사 값은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3746">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="a9974-3747">패턴</span><span class="sxs-lookup"><span data-stu-id="a9974-3747">Pattern</span></span>

<span data-ttu-id="a9974-3748">다음의 네 가지 패턴에서 ssns를 검색 하는 함수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3748">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="a9974-3749">Func_ssn는 대시 또는 공백을 사용 하 여 서식이 지정 된 2011 이전의 고급 서식 (ddd-dd-dddd 또는 ddd dd dd)을 사용 하 여 ssns를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3749">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="a9974-3750">Func_unformatted_ssn는 형식이 지정 되지 않은 2011 이전 형식으로 서식이 지정 된 ssns를 찾습니다 (ddddddddd).</span><span class="sxs-lookup"><span data-stu-id="a9974-3750">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="a9974-3751">Func_randomized_formatted_ssn는 대시 또는 공백으로 서식이 지정 된 post-2011 ssns를 찾습니다 (ddd-dd-dddd 또는 ddd dd dddd).</span><span class="sxs-lookup"><span data-stu-id="a9974-3751">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="a9974-3752">Func_randomized_unformatted_ssn는 형식 없는 2011 ssns를 찾고, 서식이 없는 9 자리 숫자 (ddddddddd)를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3752">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="a9974-3753">제외</span><span class="sxs-lookup"><span data-stu-id="a9974-3753">Checksum</span></span>

<span data-ttu-id="a9974-3754">아니요</span><span class="sxs-lookup"><span data-stu-id="a9974-3754">No</span></span>


### <a name="definition"></a><span data-ttu-id="a9974-3755">정의</span><span class="sxs-lookup"><span data-stu-id="a9974-3755">Definition</span></span>

<span data-ttu-id="a9974-3756">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3757">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3757">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3758">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3758">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="a9974-3759">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3759">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3760">Func_unformatted_ssn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3760">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3761">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3761">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="a9974-3762">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3762">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3763">Func_randomized_formatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3763">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3764">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3764">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="a9974-3765">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3765">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="a9974-3766">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 55% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3766">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="a9974-3767">Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3767">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="a9974-3768">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3768">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="a9974-3769">Func_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9974-3769">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="a9974-3770">키워드</span><span class="sxs-lookup"><span data-stu-id="a9974-3770">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="a9974-3771">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="a9974-3771">Keyword_ssn</span></span>

- <span data-ttu-id="a9974-3772">Social Security</span><span class="sxs-lookup"><span data-stu-id="a9974-3772">Social Security</span></span> 
- <span data-ttu-id="a9974-3773">Social Security#</span><span class="sxs-lookup"><span data-stu-id="a9974-3773">Social Security#</span></span> 
- <span data-ttu-id="a9974-3774">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="a9974-3774">Soc Sec</span></span> 
- <span data-ttu-id="a9974-3775">SSN</span><span class="sxs-lookup"><span data-stu-id="a9974-3775">SSN</span></span> 
- <span data-ttu-id="a9974-3776">있는 ssn</span><span class="sxs-lookup"><span data-stu-id="a9974-3776">SSNS</span></span> 
- <span data-ttu-id="a9974-3777">SSN</span><span class="sxs-lookup"><span data-stu-id="a9974-3777">SSN#</span></span> 
- <span data-ttu-id="a9974-3778">대비</span><span class="sxs-lookup"><span data-stu-id="a9974-3778">SS#</span></span> 
- <span data-ttu-id="a9974-3779">생길</span><span class="sxs-lookup"><span data-stu-id="a9974-3779">SSID</span></span> 
   

