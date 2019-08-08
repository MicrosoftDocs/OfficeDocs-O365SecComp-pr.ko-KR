---
title: 중요 한 정보 형식을 찾습니다.
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 05/20/2019
audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 준비가 된 80 중요 한 정보 유형이 포함 되어 있습니다. 이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다.
ms.openlocfilehash: 7f5c879b35f77ef142b8c45965357715f577832e
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230382"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="d0622-104">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="d0622-104">What the sensitive information types look for</span></span>

<span data-ttu-id="d0622-105">Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 수 있는 중요 한 정보 유형이 많이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="d0622-106">이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="d0622-107">중요한 정보 유형은 정규식이나 함수로 식별될 수 있는 패턴으로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="d0622-108">또한 키워드 및 체크섬과 같은 확증적인 증거를 사용하여 중요한 정보 유형을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="d0622-109">이러한 평가 프로세스에서 신뢰 수준 및 근접성도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="d0622-110">ABA 라우팅 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-111">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-111">Format</span></span>

<span data-ttu-id="d0622-112">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-113">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-113">Pattern</span></span>

<span data-ttu-id="d0622-114">서식이</span><span class="sxs-lookup"><span data-stu-id="d0622-114">Formatted:</span></span>
- <span data-ttu-id="d0622-115">0, 1, 2, 3, 6, 7 또는 8로 시작하는 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="d0622-116">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-116">A hyphen</span></span>
- <span data-ttu-id="d0622-117">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-117">Four digits</span></span>
- <span data-ttu-id="d0622-118">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-118">A hyphen</span></span>
- <span data-ttu-id="d0622-119">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-119">A digit</span></span>

<span data-ttu-id="d0622-120">서식 없음: 0, 1, 2, 3, 6, 7 또는 8로 시작 하는 9 개의 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="d0622-121">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-121">Checksum</span></span>

<span data-ttu-id="d0622-122">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-123">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-123">Definition</span></span>

<span data-ttu-id="d0622-124">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-125">Func_aba_routing 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-126">Keyword_ABA_Routing의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="d0622-127">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="d0622-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="d0622-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="d0622-129">aba</span><span class="sxs-lookup"><span data-stu-id="d0622-129">aba</span></span>
- <span data-ttu-id="d0622-130">aba #</span><span class="sxs-lookup"><span data-stu-id="d0622-130">aba #</span></span>
- <span data-ttu-id="d0622-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="d0622-131">aba routing #</span></span>
- <span data-ttu-id="d0622-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="d0622-132">aba routing number</span></span>
- <span data-ttu-id="d0622-133">aba #</span><span class="sxs-lookup"><span data-stu-id="d0622-133">aba#</span></span>
- <span data-ttu-id="d0622-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="d0622-134">abarouting#</span></span>
- <span data-ttu-id="d0622-135">aba number</span><span class="sxs-lookup"><span data-stu-id="d0622-135">aba number</span></span>
- <span data-ttu-id="d0622-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-136">abaroutingnumber</span></span>
- <span data-ttu-id="d0622-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="d0622-137">american bank association routing #</span></span>
- <span data-ttu-id="d0622-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="d0622-138">american bank association routing number</span></span>
- <span data-ttu-id="d0622-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="d0622-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="d0622-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="d0622-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="d0622-141">bank routing number</span></span>
- <span data-ttu-id="d0622-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="d0622-142">bankrouting#</span></span>
- <span data-ttu-id="d0622-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-143">bankroutingnumber</span></span>
- <span data-ttu-id="d0622-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="d0622-144">routing transit number</span></span>
- <span data-ttu-id="d0622-145">RTN</span><span class="sxs-lookup"><span data-stu-id="d0622-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="d0622-146">아르헨티나 국가 ID(DNI) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-147">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-147">Format</span></span>

<span data-ttu-id="d0622-148">마침표로 구분된 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-149">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-149">Pattern</span></span>

<span data-ttu-id="d0622-150">8자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-150">Eight digits:</span></span>
- <span data-ttu-id="d0622-151">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-151">Two digits</span></span>
- <span data-ttu-id="d0622-152">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-152">A period</span></span>
- <span data-ttu-id="d0622-153">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-153">Three digits</span></span>
- <span data-ttu-id="d0622-154">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-154">A period</span></span>
- <span data-ttu-id="d0622-155">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-156">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-156">Checksum</span></span>

<span data-ttu-id="d0622-157">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-158">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-158">Definition</span></span>

<span data-ttu-id="d0622-159">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-160">정규식 Regex_argentina_national_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-161">Keyword_argentina_national_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-162">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="d0622-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="d0622-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="d0622-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="d0622-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="d0622-165">ID</span><span class="sxs-lookup"><span data-stu-id="d0622-165">Identity</span></span> 
- <span data-ttu-id="d0622-166">식별 국가 Id 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="d0622-167">DNI</span><span class="sxs-lookup"><span data-stu-id="d0622-167">DNI</span></span> 
- <span data-ttu-id="d0622-168">개인의 NIC 국내 레지스트리</span><span class="sxs-lookup"><span data-stu-id="d0622-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="d0622-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="d0622-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="d0622-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="d0622-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="d0622-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="d0622-171">Identidad</span></span> 
- <span data-ttu-id="d0622-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="d0622-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="d0622-173">호주 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-174">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-174">Format</span></span>

<span data-ttu-id="d0622-175">6-10자리 숫자(은행 지점 번호 포함 또는 제외)</span><span class="sxs-lookup"><span data-stu-id="d0622-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-176">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-176">Pattern</span></span>

<span data-ttu-id="d0622-177">계좌 번호는 6-10자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="d0622-178">호주 은행 지점 번호:</span><span class="sxs-lookup"><span data-stu-id="d0622-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="d0622-179">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-179">Three digits</span></span> 
- <span data-ttu-id="d0622-180">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-180">A hyphen</span></span> 
- <span data-ttu-id="d0622-181">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-182">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-182">Checksum</span></span>

<span data-ttu-id="d0622-183">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-184">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-184">Definition</span></span>

<span data-ttu-id="d0622-185">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-186">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="d0622-187">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="d0622-188">Regex_australia_bank_account_number_bsb 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="d0622-189">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-190">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="d0622-191">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-192">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="d0622-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="d0622-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="d0622-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="d0622-194">swift bank code</span></span>
- <span data-ttu-id="d0622-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="d0622-195">correspondent bank</span></span>
- <span data-ttu-id="d0622-196">base currency</span><span class="sxs-lookup"><span data-stu-id="d0622-196">base currency</span></span>
- <span data-ttu-id="d0622-197">usa account</span><span class="sxs-lookup"><span data-stu-id="d0622-197">usa account</span></span>
- <span data-ttu-id="d0622-198">holder address</span><span class="sxs-lookup"><span data-stu-id="d0622-198">holder address</span></span>
- <span data-ttu-id="d0622-199">bank address</span><span class="sxs-lookup"><span data-stu-id="d0622-199">bank address</span></span>
- <span data-ttu-id="d0622-200">information account</span><span class="sxs-lookup"><span data-stu-id="d0622-200">information account</span></span>
- <span data-ttu-id="d0622-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="d0622-201">fund transfers</span></span>
- <span data-ttu-id="d0622-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="d0622-202">bank charges</span></span>
- <span data-ttu-id="d0622-203">bank details</span><span class="sxs-lookup"><span data-stu-id="d0622-203">bank details</span></span>
- <span data-ttu-id="d0622-204">banking information</span><span class="sxs-lookup"><span data-stu-id="d0622-204">banking information</span></span>
- <span data-ttu-id="d0622-205">full names</span><span class="sxs-lookup"><span data-stu-id="d0622-205">full names</span></span>
- <span data-ttu-id="d0622-206">iaea</span><span class="sxs-lookup"><span data-stu-id="d0622-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="d0622-207">호주 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-208">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-208">Format</span></span>

<span data-ttu-id="d0622-209">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-210">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-210">Pattern</span></span>

<span data-ttu-id="d0622-211">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="d0622-212">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-213">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-213">Two digits</span></span> 
- <span data-ttu-id="d0622-214">5자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="d0622-215">또는</span><span class="sxs-lookup"><span data-stu-id="d0622-215">OR</span></span>

- <span data-ttu-id="d0622-216">1-2개의 선택적 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-217">4-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-217">4-9 digits</span></span>

<span data-ttu-id="d0622-218">또는</span><span class="sxs-lookup"><span data-stu-id="d0622-218">OR</span></span>

- <span data-ttu-id="d0622-219">9자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-220">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-220">Checksum</span></span>

<span data-ttu-id="d0622-221">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-222">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-222">Definition</span></span>

<span data-ttu-id="d0622-223">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-224">Regex_australia_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-225">Keyword_australia_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="d0622-226">Keyword_australia_drivers_license_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-227">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="d0622-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="d0622-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="d0622-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="d0622-229">international driving permits</span></span>
- <span data-ttu-id="d0622-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="d0622-230">australian automobile association</span></span>
- <span data-ttu-id="d0622-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="d0622-231">international driving permit</span></span>
- <span data-ttu-id="d0622-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="d0622-232">DriverLicence</span></span>
- <span data-ttu-id="d0622-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="d0622-233">DriverLicences</span></span>
- <span data-ttu-id="d0622-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-234">Driver Lic</span></span>
- <span data-ttu-id="d0622-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-235">Driver Licence</span></span>
- <span data-ttu-id="d0622-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-236">Driver Licences</span></span>
- <span data-ttu-id="d0622-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="d0622-237">DriversLic</span></span>
- <span data-ttu-id="d0622-238">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-238">DriversLicence</span></span>
- <span data-ttu-id="d0622-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="d0622-239">DriversLicences</span></span>
- <span data-ttu-id="d0622-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-240">Drivers Lic</span></span>
- <span data-ttu-id="d0622-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-241">Drivers Lics</span></span>
- <span data-ttu-id="d0622-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-242">Drivers Licence</span></span>
- <span data-ttu-id="d0622-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-243">Drivers Licences</span></span>
- <span data-ttu-id="d0622-244">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-244">Driver'Lic</span></span>
- <span data-ttu-id="d0622-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-245">Driver'Lics</span></span>
- <span data-ttu-id="d0622-246">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-246">Driver'Licence</span></span>
- <span data-ttu-id="d0622-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-247">Driver'Licences</span></span>
- <span data-ttu-id="d0622-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-248">Driver' Lic</span></span>
- <span data-ttu-id="d0622-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-249">Driver' Lics</span></span>
- <span data-ttu-id="d0622-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-250">Driver' Licence</span></span>
- <span data-ttu-id="d0622-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-251">Driver' Licences</span></span>
- <span data-ttu-id="d0622-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="d0622-252">Driver'sLic</span></span>
- <span data-ttu-id="d0622-253">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="d0622-253">Driver'sLics</span></span>
- <span data-ttu-id="d0622-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="d0622-254">Driver'sLicence</span></span>
- <span data-ttu-id="d0622-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="d0622-255">Driver'sLicences</span></span>
- <span data-ttu-id="d0622-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-256">Driver's Lic</span></span>
- <span data-ttu-id="d0622-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-257">Driver's Lics</span></span>
- <span data-ttu-id="d0622-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-258">Driver's Licence</span></span>
- <span data-ttu-id="d0622-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-259">Driver's Licences</span></span>
- <span data-ttu-id="d0622-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-260">DriverLic#</span></span>
- <span data-ttu-id="d0622-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="d0622-261">DriverLics#</span></span>
- <span data-ttu-id="d0622-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="d0622-262">DriverLicence#</span></span>
- <span data-ttu-id="d0622-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="d0622-263">DriverLicences#</span></span>
- <span data-ttu-id="d0622-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-264">Driver Lic#</span></span>
- <span data-ttu-id="d0622-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-265">Driver Lics#</span></span>
- <span data-ttu-id="d0622-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="d0622-266">Driver Licence#</span></span>
- <span data-ttu-id="d0622-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="d0622-267">Driver Licences#</span></span>
- <span data-ttu-id="d0622-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-268">DriversLic#</span></span>
- <span data-ttu-id="d0622-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="d0622-269">DriversLics#</span></span>
- <span data-ttu-id="d0622-270">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-270">DriversLicence#</span></span>
- <span data-ttu-id="d0622-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="d0622-271">DriversLicences#</span></span>
- <span data-ttu-id="d0622-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-272">Drivers Lic#</span></span>
- <span data-ttu-id="d0622-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-273">Drivers Lics#</span></span>
- <span data-ttu-id="d0622-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="d0622-274">Drivers Licence#</span></span>
- <span data-ttu-id="d0622-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="d0622-275">Drivers Licences#</span></span>
- <span data-ttu-id="d0622-276">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="d0622-276">Driver'Lic#</span></span>
- <span data-ttu-id="d0622-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="d0622-277">Driver'Lics#</span></span>
- <span data-ttu-id="d0622-278">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-278">Driver'Licence#</span></span>
- <span data-ttu-id="d0622-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="d0622-279">Driver'Licences#</span></span>
- <span data-ttu-id="d0622-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-280">Driver' Lic#</span></span>
- <span data-ttu-id="d0622-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-281">Driver' Lics#</span></span>
- <span data-ttu-id="d0622-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="d0622-282">Driver' Licence#</span></span>
- <span data-ttu-id="d0622-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="d0622-283">Driver' Licences#</span></span>
- <span data-ttu-id="d0622-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-284">Driver'sLic#</span></span>
- <span data-ttu-id="d0622-285">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="d0622-285">Driver'sLics#</span></span>
- <span data-ttu-id="d0622-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="d0622-286">Driver'sLicence#</span></span>
- <span data-ttu-id="d0622-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="d0622-287">Driver'sLicences#</span></span>
- <span data-ttu-id="d0622-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-288">Driver's Lic#</span></span>
- <span data-ttu-id="d0622-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-289">Driver's Lics#</span></span>
- <span data-ttu-id="d0622-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="d0622-290">Driver's Licence#</span></span>
- <span data-ttu-id="d0622-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="d0622-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="d0622-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="d0622-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="d0622-293">aaa</span><span class="sxs-lookup"><span data-stu-id="d0622-293">aaa</span></span>
- <span data-ttu-id="d0622-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="d0622-294">DriverLicense</span></span>
- <span data-ttu-id="d0622-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="d0622-295">DriverLicenses</span></span>
- <span data-ttu-id="d0622-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="d0622-296">Driver License</span></span>
- <span data-ttu-id="d0622-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-297">Driver Licenses</span></span>
- <span data-ttu-id="d0622-298">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-298">DriversLicense</span></span>
- <span data-ttu-id="d0622-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-299">DriversLicenses</span></span>
- <span data-ttu-id="d0622-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="d0622-300">Drivers License</span></span>
- <span data-ttu-id="d0622-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-301">Drivers Licenses</span></span>
- <span data-ttu-id="d0622-302">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-302">Driver'License</span></span>
- <span data-ttu-id="d0622-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-303">Driver'Licenses</span></span>
- <span data-ttu-id="d0622-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="d0622-304">Driver' License</span></span>
- <span data-ttu-id="d0622-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-305">Driver' Licenses</span></span>
- <span data-ttu-id="d0622-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="d0622-306">Driver'sLicense</span></span>
- <span data-ttu-id="d0622-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="d0622-307">Driver'sLicenses</span></span>
- <span data-ttu-id="d0622-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="d0622-308">Driver's License</span></span>
- <span data-ttu-id="d0622-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-309">Driver's Licenses</span></span>
- <span data-ttu-id="d0622-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="d0622-310">DriverLicense#</span></span>
- <span data-ttu-id="d0622-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-311">DriverLicenses#</span></span>
- <span data-ttu-id="d0622-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="d0622-312">Driver License#</span></span>
- <span data-ttu-id="d0622-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-313">Driver Licenses#</span></span>
- <span data-ttu-id="d0622-314">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-314">DriversLicense#</span></span>
- <span data-ttu-id="d0622-315">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-315">DriversLicenses#</span></span>
- <span data-ttu-id="d0622-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="d0622-316">Drivers License#</span></span>
- <span data-ttu-id="d0622-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-317">Drivers Licenses#</span></span>
- <span data-ttu-id="d0622-318">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-318">Driver'License#</span></span>
- <span data-ttu-id="d0622-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-319">Driver'Licenses#</span></span>
- <span data-ttu-id="d0622-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="d0622-320">Driver' License#</span></span>
- <span data-ttu-id="d0622-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-321">Driver' Licenses#</span></span>
- <span data-ttu-id="d0622-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="d0622-322">Driver'sLicense#</span></span>
- <span data-ttu-id="d0622-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="d0622-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="d0622-324">Driver's License#</span></span>
- <span data-ttu-id="d0622-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="d0622-326">호주 의료 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-327">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-327">Format</span></span>

<span data-ttu-id="d0622-328">10-11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-329">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-329">Pattern</span></span>

<span data-ttu-id="d0622-330">10-11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-330">10-11 digits:</span></span>
- <span data-ttu-id="d0622-331">첫 번째 숫자는 2-6 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="d0622-332">9번째 숫자는 검사 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="d0622-333">10번째 숫자는 문제 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="d0622-334">11번째 숫자(선택 사항)는 개인 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-335">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-335">Checksum</span></span>

<span data-ttu-id="d0622-336">예</span><span class="sxs-lookup"><span data-stu-id="d0622-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-337">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-337">Definition</span></span>

<span data-ttu-id="d0622-338">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-339">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-340">Keyword_Australia_Medical_Account_Number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="d0622-341">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-341">The checksum passes.</span></span>

<span data-ttu-id="d0622-342">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-343">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-344">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-345">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="d0622-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="d0622-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="d0622-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="d0622-347">bank account details</span></span>
- <span data-ttu-id="d0622-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="d0622-348">medicare payments</span></span>
- <span data-ttu-id="d0622-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="d0622-349">mortgage account</span></span>
- <span data-ttu-id="d0622-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="d0622-350">bank payments</span></span>
- <span data-ttu-id="d0622-351">information branch</span><span class="sxs-lookup"><span data-stu-id="d0622-351">information branch</span></span>
- <span data-ttu-id="d0622-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="d0622-352">credit card loan</span></span>
- <span data-ttu-id="d0622-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="d0622-353">department of human services</span></span>
- <span data-ttu-id="d0622-354">local service</span><span class="sxs-lookup"><span data-stu-id="d0622-354">local service</span></span>
- <span data-ttu-id="d0622-355">medicare</span><span class="sxs-lookup"><span data-stu-id="d0622-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="d0622-356">호주 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-357">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-357">Format</span></span>

<span data-ttu-id="d0622-358">문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-359">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-359">Pattern</span></span>

<span data-ttu-id="d0622-360">1개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-361">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-361">Checksum</span></span>

<span data-ttu-id="d0622-362">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-363">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-363">Definition</span></span>

<span data-ttu-id="d0622-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-365">Regex_australia_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-366">Keyword_passport 또는 Keyword_australia_passport_number의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-367">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="d0622-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-368">Keyword_passport</span></span>

- <span data-ttu-id="d0622-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="d0622-369">Passport Number</span></span>
- <span data-ttu-id="d0622-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="d0622-370">Passport No</span></span>
- <span data-ttu-id="d0622-371">Passport #</span><span class="sxs-lookup"><span data-stu-id="d0622-371">Passport #</span></span>
- <span data-ttu-id="d0622-372">여권 #</span><span class="sxs-lookup"><span data-stu-id="d0622-372">Passport#</span></span>
- <span data-ttu-id="d0622-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="d0622-373">PassportID</span></span>
- <span data-ttu-id="d0622-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="d0622-374">Passportno</span></span>
- <span data-ttu-id="d0622-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-375">passportnumber</span></span>
- <span data-ttu-id="d0622-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="d0622-376">パスポート</span></span>
- <span data-ttu-id="d0622-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="d0622-377">パスポート番号</span></span>
- <span data-ttu-id="d0622-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="d0622-378">パスポートのNum</span></span>
- <span data-ttu-id="d0622-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="d0622-379">パスポート ＃</span></span> 
- <span data-ttu-id="d0622-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d0622-380">Numéro de passeport</span></span>
- <span data-ttu-id="d0622-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="d0622-381">Passeport n °</span></span>
- <span data-ttu-id="d0622-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="d0622-382">Passeport Non</span></span>
- <span data-ttu-id="d0622-383">Passeport #</span><span class="sxs-lookup"><span data-stu-id="d0622-383">Passeport #</span></span>
- <span data-ttu-id="d0622-384">포트 #</span><span class="sxs-lookup"><span data-stu-id="d0622-384">Passeport#</span></span>
- <span data-ttu-id="d0622-385">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="d0622-385">PasseportNon</span></span>
- <span data-ttu-id="d0622-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="d0622-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="d0622-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="d0622-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="d0622-388">여권</span><span class="sxs-lookup"><span data-stu-id="d0622-388">passport</span></span>
- <span data-ttu-id="d0622-389">passport details</span><span class="sxs-lookup"><span data-stu-id="d0622-389">passport details</span></span>
- <span data-ttu-id="d0622-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="d0622-390">immigration and citizenship</span></span>
- <span data-ttu-id="d0622-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="d0622-391">commonwealth of australia</span></span>
- <span data-ttu-id="d0622-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="d0622-392">department of immigration</span></span>
- <span data-ttu-id="d0622-393">residential address</span><span class="sxs-lookup"><span data-stu-id="d0622-393">residential address</span></span>
- <span data-ttu-id="d0622-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="d0622-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="d0622-395">visa</span><span class="sxs-lookup"><span data-stu-id="d0622-395">visa</span></span>
- <span data-ttu-id="d0622-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="d0622-396">national identity card</span></span>
- <span data-ttu-id="d0622-397">passport number</span><span class="sxs-lookup"><span data-stu-id="d0622-397">passport number</span></span>
- <span data-ttu-id="d0622-398">travel document</span><span class="sxs-lookup"><span data-stu-id="d0622-398">travel document</span></span>
- <span data-ttu-id="d0622-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="d0622-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="d0622-400">호주 세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-401">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-401">Format</span></span>

<span data-ttu-id="d0622-402">8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-403">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-403">Pattern</span></span>

<span data-ttu-id="d0622-404">일반적으로 다음과 같이 공백과 함께 표시되는 8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="d0622-405">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-405">Three digits</span></span> 
- <span data-ttu-id="d0622-406">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-406">An optional space</span></span> 
- <span data-ttu-id="d0622-407">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-407">Three digits</span></span> 
- <span data-ttu-id="d0622-408">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-408">An optional space</span></span> 
- <span data-ttu-id="d0622-409">마지막 숫자가 검사 숫자인 2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-410">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-410">Checksum</span></span>

<span data-ttu-id="d0622-411">예</span><span class="sxs-lookup"><span data-stu-id="d0622-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-412">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-412">Definition</span></span>

<span data-ttu-id="d0622-413">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-414">Func_australian_tax_file_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-415">Keyword_Australia_Tax_File_Number 또는 Keyword_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="d0622-416">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-416">The checksum passes.</span></span>

```
   <!-- Australia Tax File Number -->
    <Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Match idRef="Keyword_Australia_Tax_File_Number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_number_exclusions" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-417">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="d0622-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="d0622-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="d0622-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="d0622-419">australian business number</span></span>
- <span data-ttu-id="d0622-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="d0622-420">marginal tax rate</span></span>
- <span data-ttu-id="d0622-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="d0622-421">medicare levy</span></span>
- <span data-ttu-id="d0622-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="d0622-422">portfolio number</span></span>
- <span data-ttu-id="d0622-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="d0622-423">service veterans</span></span>
- <span data-ttu-id="d0622-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="d0622-424">withholding tax</span></span>
- <span data-ttu-id="d0622-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="d0622-425">individual tax return</span></span>
- <span data-ttu-id="d0622-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="d0622-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="d0622-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="d0622-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="d0622-428">00000000</span><span class="sxs-lookup"><span data-stu-id="d0622-428">00000000</span></span>
- <span data-ttu-id="d0622-429">11111111</span><span class="sxs-lookup"><span data-stu-id="d0622-429">11111111</span></span>
- <span data-ttu-id="d0622-430">22222222</span><span class="sxs-lookup"><span data-stu-id="d0622-430">22222222</span></span>
- <span data-ttu-id="d0622-431">33333333</span><span class="sxs-lookup"><span data-stu-id="d0622-431">33333333</span></span>
- <span data-ttu-id="d0622-432">44444444</span><span class="sxs-lookup"><span data-stu-id="d0622-432">44444444</span></span>
- <span data-ttu-id="d0622-433">55555555</span><span class="sxs-lookup"><span data-stu-id="d0622-433">55555555</span></span>
- <span data-ttu-id="d0622-434">66666666</span><span class="sxs-lookup"><span data-stu-id="d0622-434">66666666</span></span>
- <span data-ttu-id="d0622-435">77777777</span><span class="sxs-lookup"><span data-stu-id="d0622-435">77777777</span></span>
- <span data-ttu-id="d0622-436">88888888</span><span class="sxs-lookup"><span data-stu-id="d0622-436">88888888</span></span>
- <span data-ttu-id="d0622-437">99999999</span><span class="sxs-lookup"><span data-stu-id="d0622-437">99999999</span></span>
- <span data-ttu-id="d0622-438">000000000</span><span class="sxs-lookup"><span data-stu-id="d0622-438">000000000</span></span>
- <span data-ttu-id="d0622-439">111111111</span><span class="sxs-lookup"><span data-stu-id="d0622-439">111111111</span></span>
- <span data-ttu-id="d0622-440">222222222</span><span class="sxs-lookup"><span data-stu-id="d0622-440">222222222</span></span>
- <span data-ttu-id="d0622-441">333333333</span><span class="sxs-lookup"><span data-stu-id="d0622-441">333333333</span></span>
- <span data-ttu-id="d0622-442">444444444</span><span class="sxs-lookup"><span data-stu-id="d0622-442">444444444</span></span>
- <span data-ttu-id="d0622-443">555555555</span><span class="sxs-lookup"><span data-stu-id="d0622-443">555555555</span></span>
- <span data-ttu-id="d0622-444">666666666</span><span class="sxs-lookup"><span data-stu-id="d0622-444">666666666</span></span>
- <span data-ttu-id="d0622-445">777777777</span><span class="sxs-lookup"><span data-stu-id="d0622-445">777777777</span></span>
- <span data-ttu-id="d0622-446">888888888</span><span class="sxs-lookup"><span data-stu-id="d0622-446">888888888</span></span>
- <span data-ttu-id="d0622-447">999999999</span><span class="sxs-lookup"><span data-stu-id="d0622-447">999999999</span></span>
- <span data-ttu-id="d0622-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="d0622-448">0000000000</span></span>
- <span data-ttu-id="d0622-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="d0622-449">1111111111</span></span>
- <span data-ttu-id="d0622-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="d0622-450">2222222222</span></span>
- <span data-ttu-id="d0622-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="d0622-451">3333333333</span></span>
- <span data-ttu-id="d0622-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="d0622-452">4444444444</span></span>
- <span data-ttu-id="d0622-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="d0622-453">5555555555</span></span>
- <span data-ttu-id="d0622-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="d0622-454">6666666666</span></span>
- <span data-ttu-id="d0622-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="d0622-455">7777777777</span></span>
- <span data-ttu-id="d0622-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="d0622-456">8888888888</span></span>
- <span data-ttu-id="d0622-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="d0622-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="d0622-458">Azure DocumentDB 인증 키</span><span class="sxs-lookup"><span data-stu-id="d0622-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="d0622-459">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-459">Format</span></span>

<span data-ttu-id="d0622-460">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "DocumentDb" 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-461">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-461">Pattern</span></span>

- <span data-ttu-id="d0622-462">"DocumentDb" 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="d0622-463">3-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-464">보다 큼 기호 (>), 등호 (=), 따옴표 (") 또는 아포스트로피 (')</span><span class="sxs-lookup"><span data-stu-id="d0622-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="d0622-465">86의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="d0622-466">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-467">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-467">Checksum</span></span>

<span data-ttu-id="d0622-468">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-469">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-469">Definition</span></span>

<span data-ttu-id="d0622-470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-471">정규식 CEP_Regex_AzureDocumentDBAuthKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-472">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-473">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="d0622-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="d0622-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="d0622-475">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-476">극동</span><span class="sxs-lookup"><span data-stu-id="d0622-476">contoso</span></span>
- <span data-ttu-id="d0622-477">fabrikam</span><span class="sxs-lookup"><span data-stu-id="d0622-477">fabrikam</span></span>
- <span data-ttu-id="d0622-478">대양</span><span class="sxs-lookup"><span data-stu-id="d0622-478">northwind</span></span>
- <span data-ttu-id="d0622-479">샌드박스</span><span class="sxs-lookup"><span data-stu-id="d0622-479">sandbox</span></span>
- <span data-ttu-id="d0622-480">용 onebox</span><span class="sxs-lookup"><span data-stu-id="d0622-480">onebox</span></span>
- <span data-ttu-id="d0622-481">로컬</span><span class="sxs-lookup"><span data-stu-id="d0622-481">localhost</span></span>
- <span data-ttu-id="d0622-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d0622-482">127.0.0.1</span></span>
- <span data-ttu-id="d0622-483">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-484">ccw</span><span class="sxs-lookup"><span data-stu-id="d0622-484">com</span></span>
- <span data-ttu-id="d0622-485">s-int</span><span class="sxs-lookup"><span data-stu-id="d0622-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-486">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="d0622-487">Azure IAAS 데이터베이스 연결 문자열 및 Azure SQL 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="d0622-488">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-488">Format</span></span>

<span data-ttu-id="d0622-489">"Server", "server" 또는 "data source" 라는 문자열은 "cloudapp. azure"를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-490">com "또는" cloudapp.</span><span class="sxs-lookup"><span data-stu-id="d0622-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-491">net "또는" 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="d0622-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-492">net "과 문자열" Password "또는" password "또는" pwd "가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-493">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-493">Pattern</span></span>

- <span data-ttu-id="d0622-494">문자열 "Server", "Server" 또는 "data source"</span><span class="sxs-lookup"><span data-stu-id="d0622-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="d0622-495">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-496">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-496">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-497">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-498">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-499">문자열 "cloudapp.</span><span class="sxs-lookup"><span data-stu-id="d0622-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-500">com "," cloudapp.</span><span class="sxs-lookup"><span data-stu-id="d0622-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-501">net "또는" database.</span><span class="sxs-lookup"><span data-stu-id="d0622-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-502">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-502">net"</span></span>
- <span data-ttu-id="d0622-503">1-300에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-504">문자열 "Password", "password" 또는 "pwd"</span><span class="sxs-lookup"><span data-stu-id="d0622-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="d0622-505">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-506">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-506">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-507">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-508">세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')가 아닌 하나 이상의 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="d0622-509">세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')</span><span class="sxs-lookup"><span data-stu-id="d0622-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-510">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-510">Checksum</span></span>

<span data-ttu-id="d0622-511">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-512">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-512">Definition</span></span>

<span data-ttu-id="d0622-513">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-514">정규식 CEP_Regex_AzureConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-515">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-516">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="d0622-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="d0622-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="d0622-518">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-519">극동</span><span class="sxs-lookup"><span data-stu-id="d0622-519">contoso</span></span>
- <span data-ttu-id="d0622-520">fabrikam</span><span class="sxs-lookup"><span data-stu-id="d0622-520">fabrikam</span></span>
- <span data-ttu-id="d0622-521">대양</span><span class="sxs-lookup"><span data-stu-id="d0622-521">northwind</span></span>
- <span data-ttu-id="d0622-522">샌드박스</span><span class="sxs-lookup"><span data-stu-id="d0622-522">sandbox</span></span>
- <span data-ttu-id="d0622-523">용 onebox</span><span class="sxs-lookup"><span data-stu-id="d0622-523">onebox</span></span>
- <span data-ttu-id="d0622-524">로컬</span><span class="sxs-lookup"><span data-stu-id="d0622-524">localhost</span></span>
- <span data-ttu-id="d0622-525">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d0622-525">127.0.0.1</span></span>
- <span data-ttu-id="d0622-526">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-527">ccw</span><span class="sxs-lookup"><span data-stu-id="d0622-527">com</span></span>
- <span data-ttu-id="d0622-528">s-int</span><span class="sxs-lookup"><span data-stu-id="d0622-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-529">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="d0622-530">Azure IoT Connection 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="d0622-531">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-531">Format</span></span>

<span data-ttu-id="d0622-532">문자열 "HostName" 뒤에 "azure-devices" 라는 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-533">net "및" SharedAccessKey "</span><span class="sxs-lookup"><span data-stu-id="d0622-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-534">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-534">Pattern</span></span>

- <span data-ttu-id="d0622-535">문자열 "HostName"</span><span class="sxs-lookup"><span data-stu-id="d0622-535">The string "HostName"</span></span>
- <span data-ttu-id="d0622-536">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-537">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-537">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-538">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-539">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-540">문자열 "azure-장치</span><span class="sxs-lookup"><span data-stu-id="d0622-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-541">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-541">net"</span></span>
- <span data-ttu-id="d0622-542">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-543">"SharedAccessKey" 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="d0622-544">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-545">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-545">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-546">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-547">43의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="d0622-548">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-549">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-549">Checksum</span></span>

<span data-ttu-id="d0622-550">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-551">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-551">Definition</span></span>

<span data-ttu-id="d0622-552">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-553">정규식 CEP_Regex_AzureIoTConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-554">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-555">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="d0622-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="d0622-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="d0622-557">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-558">극동</span><span class="sxs-lookup"><span data-stu-id="d0622-558">contoso</span></span>
- <span data-ttu-id="d0622-559">fabrikam</span><span class="sxs-lookup"><span data-stu-id="d0622-559">fabrikam</span></span>
- <span data-ttu-id="d0622-560">대양</span><span class="sxs-lookup"><span data-stu-id="d0622-560">northwind</span></span>
- <span data-ttu-id="d0622-561">샌드박스</span><span class="sxs-lookup"><span data-stu-id="d0622-561">sandbox</span></span>
- <span data-ttu-id="d0622-562">용 onebox</span><span class="sxs-lookup"><span data-stu-id="d0622-562">onebox</span></span>
- <span data-ttu-id="d0622-563">로컬</span><span class="sxs-lookup"><span data-stu-id="d0622-563">localhost</span></span>
- <span data-ttu-id="d0622-564">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d0622-564">127.0.0.1</span></span>
- <span data-ttu-id="d0622-565">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-566">ccw</span><span class="sxs-lookup"><span data-stu-id="d0622-566">com</span></span>
- <span data-ttu-id="d0622-567">s-int</span><span class="sxs-lookup"><span data-stu-id="d0622-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-568">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="d0622-569">Azure 게시 설정 암호</span><span class="sxs-lookup"><span data-stu-id="d0622-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="d0622-570">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-570">Format</span></span>

<span data-ttu-id="d0622-571">문자열 "userpwd =" 다음에 영숫자 문자열이 나옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-572">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-572">Pattern</span></span>

- <span data-ttu-id="d0622-573">문자열 "userpwd ="</span><span class="sxs-lookup"><span data-stu-id="d0622-573">The string "userpwd="</span></span>
- <span data-ttu-id="d0622-574">60 대 문자와 숫자의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="d0622-575">큰따옴표 (")</span><span class="sxs-lookup"><span data-stu-id="d0622-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-576">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-576">Checksum</span></span>

<span data-ttu-id="d0622-577">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-578">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-578">Definition</span></span>

<span data-ttu-id="d0622-579">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-580">정규식 CEP_Regex_AzurePublishSettingPasswords 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-581">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


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

### <a name="keywords"></a><span data-ttu-id="d0622-582">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="d0622-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="d0622-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="d0622-584">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-585">극동</span><span class="sxs-lookup"><span data-stu-id="d0622-585">contoso</span></span>
- <span data-ttu-id="d0622-586">fabrikam</span><span class="sxs-lookup"><span data-stu-id="d0622-586">fabrikam</span></span>
- <span data-ttu-id="d0622-587">대양</span><span class="sxs-lookup"><span data-stu-id="d0622-587">northwind</span></span>
- <span data-ttu-id="d0622-588">샌드박스</span><span class="sxs-lookup"><span data-stu-id="d0622-588">sandbox</span></span>
- <span data-ttu-id="d0622-589">용 onebox</span><span class="sxs-lookup"><span data-stu-id="d0622-589">onebox</span></span>
- <span data-ttu-id="d0622-590">로컬</span><span class="sxs-lookup"><span data-stu-id="d0622-590">localhost</span></span>
- <span data-ttu-id="d0622-591">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d0622-591">127.0.0.1</span></span>
- <span data-ttu-id="d0622-592">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-593">ccw</span><span class="sxs-lookup"><span data-stu-id="d0622-593">com</span></span>
- <span data-ttu-id="d0622-594">s-int</span><span class="sxs-lookup"><span data-stu-id="d0622-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-595">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="d0622-596">Azure Redis 캐시 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="d0622-597">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-597">Format</span></span>

<span data-ttu-id="d0622-598">문자열 "redis.</span><span class="sxs-lookup"><span data-stu-id="d0622-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-599">net "문자열" password "또는" pwd "를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-600">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-600">Pattern</span></span>

- <span data-ttu-id="d0622-601">문자열 "redis.</span><span class="sxs-lookup"><span data-stu-id="d0622-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-602">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-602">net"</span></span>
- <span data-ttu-id="d0622-603">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-604">문자열 "password" 또는 "pwd"</span><span class="sxs-lookup"><span data-stu-id="d0622-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="d0622-605">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-606">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-606">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-607">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-608">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="d0622-609">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-610">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-610">Checksum</span></span>

<span data-ttu-id="d0622-611">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-612">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-612">Definition</span></span>

<span data-ttu-id="d0622-613">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-614">정규식 CEP_Regex_AzureRedisCacheConnectionString가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="d0622-615">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-616">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="d0622-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="d0622-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="d0622-618">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-619">극동</span><span class="sxs-lookup"><span data-stu-id="d0622-619">contoso</span></span>
- <span data-ttu-id="d0622-620">fabrikam</span><span class="sxs-lookup"><span data-stu-id="d0622-620">fabrikam</span></span>
- <span data-ttu-id="d0622-621">대양</span><span class="sxs-lookup"><span data-stu-id="d0622-621">northwind</span></span>
- <span data-ttu-id="d0622-622">샌드박스</span><span class="sxs-lookup"><span data-stu-id="d0622-622">sandbox</span></span>
- <span data-ttu-id="d0622-623">용 onebox</span><span class="sxs-lookup"><span data-stu-id="d0622-623">onebox</span></span>
- <span data-ttu-id="d0622-624">로컬</span><span class="sxs-lookup"><span data-stu-id="d0622-624">localhost</span></span>
- <span data-ttu-id="d0622-625">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d0622-625">127.0.0.1</span></span>
- <span data-ttu-id="d0622-626">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-627">ccw</span><span class="sxs-lookup"><span data-stu-id="d0622-627">com</span></span>
- <span data-ttu-id="d0622-628">s-int</span><span class="sxs-lookup"><span data-stu-id="d0622-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-629">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="d0622-630">Azure SAS</span><span class="sxs-lookup"><span data-stu-id="d0622-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="d0622-631">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-631">Format</span></span>

<span data-ttu-id="d0622-632">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 문자열 "sig"</span><span class="sxs-lookup"><span data-stu-id="d0622-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-633">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-633">Pattern</span></span>

- <span data-ttu-id="d0622-634">문자열 "sig"</span><span class="sxs-lookup"><span data-stu-id="d0622-634">The string "sig"</span></span>
- <span data-ttu-id="d0622-635">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-636">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-636">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-637">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-638">대/소문자, 숫자 또는 백분율 기호 (%)가 43-53 자 사이의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="d0622-639">문자열 "% 3d"</span><span class="sxs-lookup"><span data-stu-id="d0622-639">The string "%3d"</span></span>
- <span data-ttu-id="d0622-640">소문자 또는 대문자, 숫자 또는 백분율 기호 (%)가 아닌 모든 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-641">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-641">Checksum</span></span>

<span data-ttu-id="d0622-642">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-643">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-643">Definition</span></span>

<span data-ttu-id="d0622-644">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-645">정규식 CEP_Regex_AzureSAS 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="d0622-646">Azure Service Bus 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="d0622-647">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-647">Format</span></span>

<span data-ttu-id="d0622-648">문자열 "끝점" 뒤에 "servicebus" 라는 문자열을 포함 하 여 아래 패턴에 나와 있는 문자 및 문자열이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-649">net "및" SharedAccesKey "을 차례로 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-650">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-650">Pattern</span></span>

- <span data-ttu-id="d0622-651">문자열 "끝점"</span><span class="sxs-lookup"><span data-stu-id="d0622-651">The string "EndPoint"</span></span>
- <span data-ttu-id="d0622-652">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-653">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-653">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-654">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-655">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-656">문자열 "servicebus.</span><span class="sxs-lookup"><span data-stu-id="d0622-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-657">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-657">net"</span></span>
- <span data-ttu-id="d0622-658">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-659">"SharedAccessKey" 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="d0622-660">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-661">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-661">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-662">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-663">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="d0622-664">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-665">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-665">Checksum</span></span>

<span data-ttu-id="d0622-666">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-667">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-667">Definition</span></span>

<span data-ttu-id="d0622-668">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-669">정규식 CEP_Regex_AzureServiceBusConnectionString가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="d0622-670">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-671">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="d0622-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="d0622-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="d0622-673">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-674">극동</span><span class="sxs-lookup"><span data-stu-id="d0622-674">contoso</span></span>
- <span data-ttu-id="d0622-675">fabrikam</span><span class="sxs-lookup"><span data-stu-id="d0622-675">fabrikam</span></span>
- <span data-ttu-id="d0622-676">대양</span><span class="sxs-lookup"><span data-stu-id="d0622-676">northwind</span></span>
- <span data-ttu-id="d0622-677">샌드박스</span><span class="sxs-lookup"><span data-stu-id="d0622-677">sandbox</span></span>
- <span data-ttu-id="d0622-678">용 onebox</span><span class="sxs-lookup"><span data-stu-id="d0622-678">onebox</span></span>
- <span data-ttu-id="d0622-679">로컬</span><span class="sxs-lookup"><span data-stu-id="d0622-679">localhost</span></span>
- <span data-ttu-id="d0622-680">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d0622-680">127.0.0.1</span></span>
- <span data-ttu-id="d0622-681">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-682">ccw</span><span class="sxs-lookup"><span data-stu-id="d0622-682">com</span></span>
- <span data-ttu-id="d0622-683">s-int</span><span class="sxs-lookup"><span data-stu-id="d0622-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-684">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="d0622-685">Azure 저장소 계정 키</span><span class="sxs-lookup"><span data-stu-id="d0622-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="d0622-686">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-686">Format</span></span>

<span data-ttu-id="d0622-687">"DefaultEndpointsProtocol" 문자열은 "AccountKey" 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-688">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-688">Pattern</span></span>

- <span data-ttu-id="d0622-689">문자열 "DefaultEndpointsProtocol"</span><span class="sxs-lookup"><span data-stu-id="d0622-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="d0622-690">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-691">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-691">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-692">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-693">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-694">문자열 "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="d0622-694">The string "AccountKey"</span></span>
- <span data-ttu-id="d0622-695">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-696">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-696">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-697">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="d0622-698">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="d0622-699">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-700">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-700">Checksum</span></span>

<span data-ttu-id="d0622-701">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-702">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-702">Definition</span></span>

<span data-ttu-id="d0622-703">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-704">정규식 CEP_Regex_AzureStorageAccountKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-705">CEP_AzureEmulatorStorageAccountFilter 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-706">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-707">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="d0622-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="d0622-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="d0622-709">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="d0622-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="d0622-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="d0622-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="d0622-712">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-713">극동</span><span class="sxs-lookup"><span data-stu-id="d0622-713">contoso</span></span>
- <span data-ttu-id="d0622-714">fabrikam</span><span class="sxs-lookup"><span data-stu-id="d0622-714">fabrikam</span></span>
- <span data-ttu-id="d0622-715">대양</span><span class="sxs-lookup"><span data-stu-id="d0622-715">northwind</span></span>
- <span data-ttu-id="d0622-716">샌드박스</span><span class="sxs-lookup"><span data-stu-id="d0622-716">sandbox</span></span>
- <span data-ttu-id="d0622-717">용 onebox</span><span class="sxs-lookup"><span data-stu-id="d0622-717">onebox</span></span>
- <span data-ttu-id="d0622-718">로컬</span><span class="sxs-lookup"><span data-stu-id="d0622-718">localhost</span></span>
- <span data-ttu-id="d0622-719">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d0622-719">127.0.0.1</span></span>
- <span data-ttu-id="d0622-720">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-721">ccw</span><span class="sxs-lookup"><span data-stu-id="d0622-721">com</span></span>
- <span data-ttu-id="d0622-722">s-int</span><span class="sxs-lookup"><span data-stu-id="d0622-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-723">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="d0622-724">Azure 저장소 계정 키 (일반)</span><span class="sxs-lookup"><span data-stu-id="d0622-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-725">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-725">Format</span></span>

<span data-ttu-id="d0622-726">아래 패턴에 윤곽선이 있는 문자 앞 이나 뒤에 오는 86 문자의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-727">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-727">Pattern</span></span>

- <span data-ttu-id="d0622-728">보다 큼 기호 (>), 아포스트로피 ('), 등호 (=), 따옴표 (") 또는 숫자 기호 (#) 0-1</span><span class="sxs-lookup"><span data-stu-id="d0622-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="d0622-729">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="d0622-730">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="d0622-731">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-731">Checksum</span></span>

<span data-ttu-id="d0622-732">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-733">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-733">Definition</span></span>

<span data-ttu-id="d0622-734">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-735">정규식 CEP_Regex_AzureStorageAccountKeyGeneric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="d0622-736">벨기에 국가 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-737">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-737">Format</span></span>

<span data-ttu-id="d0622-738">11자리 숫자와 구분 기호</span><span class="sxs-lookup"><span data-stu-id="d0622-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-739">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-739">Pattern</span></span>

<span data-ttu-id="d0622-740">11자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="d0622-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="d0622-741">생년월일을 나타내는 YY.MM.DD 형식의 6자리 숫자와 마침표 2개 </span><span class="sxs-lookup"><span data-stu-id="d0622-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="d0622-742">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-742">A hyphen</span></span> 
- <span data-ttu-id="d0622-743">세 개의 순차적 숫자(남성의 경우 홀수, 여성의 경우 짝수) </span><span class="sxs-lookup"><span data-stu-id="d0622-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="d0622-744">마침표</span><span class="sxs-lookup"><span data-stu-id="d0622-744">A period</span></span> 
- <span data-ttu-id="d0622-745">검사 숫자에 해당하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-746">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-746">Checksum</span></span>

<span data-ttu-id="d0622-747">예</span><span class="sxs-lookup"><span data-stu-id="d0622-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-748">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-748">Definition</span></span>

<span data-ttu-id="d0622-749">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-750">Func_belgium_national_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-751">Keyword_belgium_national_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="d0622-752">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-752">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-753">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="d0622-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="d0622-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="d0622-755">ID</span><span class="sxs-lookup"><span data-stu-id="d0622-755">Identity</span></span>
- <span data-ttu-id="d0622-756">등록</span><span class="sxs-lookup"><span data-stu-id="d0622-756">Registration</span></span>
- <span data-ttu-id="d0622-757">확인과</span><span class="sxs-lookup"><span data-stu-id="d0622-757">Identification</span></span> 
- <span data-ttu-id="d0622-758">ID</span><span class="sxs-lookup"><span data-stu-id="d0622-758">ID</span></span> 
- <span data-ttu-id="d0622-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="d0622-759">Identiteitskaart</span></span>
- <span data-ttu-id="d0622-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="d0622-760">Registratie nummer</span></span> 
- <span data-ttu-id="d0622-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="d0622-761">Identificatie nummer</span></span> 
- <span data-ttu-id="d0622-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="d0622-762">Identiteit</span></span>
- <span data-ttu-id="d0622-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="d0622-763">Registratie</span></span>
- <span data-ttu-id="d0622-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="d0622-764">Identificatie</span></span> 
- <span data-ttu-id="d0622-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d0622-765">Carte d’identité</span></span> 
- <span data-ttu-id="d0622-766">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="d0622-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="d0622-767">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="d0622-767">numéro d'identification</span></span>
- <span data-ttu-id="d0622-768">identité</span><span class="sxs-lookup"><span data-stu-id="d0622-768">identité</span></span> 
- <span data-ttu-id="d0622-769">inscription</span><span class="sxs-lookup"><span data-stu-id="d0622-769">inscription</span></span> 
- <span data-ttu-id="d0622-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="d0622-770">Identifikation</span></span>
- <span data-ttu-id="d0622-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="d0622-771">Identifizierung</span></span>
- <span data-ttu-id="d0622-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-772">Identifikationsnummer</span></span>
- <span data-ttu-id="d0622-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="d0622-773">Personalausweis</span></span>
- <span data-ttu-id="d0622-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="d0622-774">Registrierung</span></span>
- <span data-ttu-id="d0622-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="d0622-776">브라질 CPF 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-777">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-777">Format</span></span>

<span data-ttu-id="d0622-778">서식이 있거나 서식이 없을 수 있는 검사 숫자를 포함하는 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-779">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-779">Pattern</span></span>

<span data-ttu-id="d0622-780">서식이</span><span class="sxs-lookup"><span data-stu-id="d0622-780">Formatted:</span></span>
- <span data-ttu-id="d0622-781">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-781">Three digits</span></span> 
- <span data-ttu-id="d0622-782">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-782">A period</span></span> 
- <span data-ttu-id="d0622-783">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-783">Three digits</span></span> 
- <span data-ttu-id="d0622-784">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-784">A period</span></span> 
- <span data-ttu-id="d0622-785">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-785">Three digits</span></span> 
- <span data-ttu-id="d0622-786">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-786">A hyphen</span></span> 
- <span data-ttu-id="d0622-787">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-787">Two digits which are check digits</span></span>

<span data-ttu-id="d0622-788">서식</span><span class="sxs-lookup"><span data-stu-id="d0622-788">Unformatted:</span></span>
- <span data-ttu-id="d0622-789">마지막 2자리 숫자가 검사 숫자인 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-790">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-790">Checksum</span></span>

<span data-ttu-id="d0622-791">예</span><span class="sxs-lookup"><span data-stu-id="d0622-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-792">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-792">Definition</span></span>

<span data-ttu-id="d0622-793">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-794">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-795">Keyword_brazil_cpf에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="d0622-796">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-796">The checksum passes.</span></span>

<span data-ttu-id="d0622-797">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-798">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-799">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-799">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-800">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="d0622-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="d0622-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="d0622-802">CPF</span><span class="sxs-lookup"><span data-stu-id="d0622-802">CPF</span></span>
- <span data-ttu-id="d0622-803">확인과</span><span class="sxs-lookup"><span data-stu-id="d0622-803">Identification</span></span>
- <span data-ttu-id="d0622-804">등록</span><span class="sxs-lookup"><span data-stu-id="d0622-804">Registration</span></span>
- <span data-ttu-id="d0622-805">별</span><span class="sxs-lookup"><span data-stu-id="d0622-805">Revenue</span></span>
- <span data-ttu-id="d0622-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="d0622-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="d0622-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="d0622-807">Imposto</span></span> 
- <span data-ttu-id="d0622-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="d0622-808">Identificação</span></span> 
- <span data-ttu-id="d0622-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="d0622-809">Inscrição</span></span> 
- <span data-ttu-id="d0622-810">고 eita</span><span class="sxs-lookup"><span data-stu-id="d0622-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="d0622-811">브라질 법인 번호(CNPJ)</span><span class="sxs-lookup"><span data-stu-id="d0622-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-812">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-812">Format</span></span>

<span data-ttu-id="d0622-813">등록 번호, 지점 번호, 검사 숫자 및 구분 기호를 포함하는 14자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-814">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-814">Pattern</span></span>
<span data-ttu-id="d0622-815">14자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="d0622-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="d0622-816">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-816">Two digits</span></span> 
- <span data-ttu-id="d0622-817">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-817">A period</span></span> 
- <span data-ttu-id="d0622-818">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-818">Three digits</span></span> 
- <span data-ttu-id="d0622-819">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-819">A period</span></span> 
- <span data-ttu-id="d0622-820">3자리 숫자(처음 8자리 숫자는 등록 번호임) </span><span class="sxs-lookup"><span data-stu-id="d0622-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="d0622-821">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="d0622-821">A forward slash</span></span> 
- <span data-ttu-id="d0622-822">4자리 지점 번호 </span><span class="sxs-lookup"><span data-stu-id="d0622-822">Four-digit branch number</span></span> 
- <span data-ttu-id="d0622-823">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-823">A hyphen</span></span> 
- <span data-ttu-id="d0622-824">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-825">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-825">Checksum</span></span>

<span data-ttu-id="d0622-826">예</span><span class="sxs-lookup"><span data-stu-id="d0622-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-827">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-827">Definition</span></span>

<span data-ttu-id="d0622-828">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-829">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-830">Keyword_brazil_cnpj에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="d0622-831">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-831">The checksum passes.</span></span>

<span data-ttu-id="d0622-832">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-833">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-834">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-834">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-835">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="d0622-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="d0622-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="d0622-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="d0622-837">CNPJ</span></span> 
- <span data-ttu-id="d0622-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="d0622-838">CNPJ/MF</span></span> 
- <span data-ttu-id="d0622-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="d0622-839">CNPJ-MF</span></span> 
- <span data-ttu-id="d0622-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="d0622-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="d0622-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="d0622-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="d0622-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="d0622-842">Legal entity</span></span> 
- <span data-ttu-id="d0622-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="d0622-843">Legal entities</span></span> 
- <span data-ttu-id="d0622-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="d0622-844">Registration Status</span></span> 
- <span data-ttu-id="d0622-845">비즈니스</span><span class="sxs-lookup"><span data-stu-id="d0622-845">Business</span></span> 
- <span data-ttu-id="d0622-846">Company</span><span class="sxs-lookup"><span data-stu-id="d0622-846">Company</span></span>
- <span data-ttu-id="d0622-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="d0622-847">CNPJ</span></span> 
- <span data-ttu-id="d0622-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="d0622-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="d0622-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="d0622-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="d0622-850">CGC</span><span class="sxs-lookup"><span data-stu-id="d0622-850">CGC</span></span> 
- <span data-ttu-id="d0622-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="d0622-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="d0622-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="d0622-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="d0622-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="d0622-853">Situação cadastral</span></span> 
- <span data-ttu-id="d0622-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="d0622-854">Inscrição</span></span> 
- <span data-ttu-id="d0622-855">포털</span><span class="sxs-lookup"><span data-stu-id="d0622-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="d0622-856">	브라질 국가 ID 카드(RG)</span><span class="sxs-lookup"><span data-stu-id="d0622-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-857">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-857">Format</span></span>

<span data-ttu-id="d0622-858">Registro Geral (이전 형식): 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="d0622-859">Registro de Identidade (RIC) (새 형식): 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-860">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-860">Pattern</span></span>

<span data-ttu-id="d0622-861">Registro Geral(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="d0622-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="d0622-862">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-862">Two digits</span></span> 
- <span data-ttu-id="d0622-863">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-863">A period</span></span> 
- <span data-ttu-id="d0622-864">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-864">Three digits</span></span> 
- <span data-ttu-id="d0622-865">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-865">A period</span></span> 
- <span data-ttu-id="d0622-866">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-866">Three digits</span></span> 
- <span data-ttu-id="d0622-867">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-867">A hyphen</span></span> 
- <span data-ttu-id="d0622-868">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-868">One digit which is a check digit</span></span>

<span data-ttu-id="d0622-869">Registro de Identidade (RIC) (새 형식):</span><span class="sxs-lookup"><span data-stu-id="d0622-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="d0622-870">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-870">10 digits</span></span> 
- <span data-ttu-id="d0622-871">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-871">A hyphen</span></span> 
- <span data-ttu-id="d0622-872">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-873">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-873">Checksum</span></span>

<span data-ttu-id="d0622-874">예</span><span class="sxs-lookup"><span data-stu-id="d0622-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-875">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-875">Definition</span></span>

<span data-ttu-id="d0622-876">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-877">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-878">Keyword_brazil_rg에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="d0622-879">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-879">The checksum passes.</span></span>

<span data-ttu-id="d0622-880">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-881">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-882">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-882">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-883">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="d0622-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="d0622-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="d0622-885">Cédula de identidade identity card 국립 id número de rregistro registro de Iidentidade registro geral RG (이 키워드는 대/소문자를 구분 함) RIC (이 키워드는 대/소문자를 구분 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="d0622-886">캐나다 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-887">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-887">Format</span></span>

<span data-ttu-id="d0622-888">7 또는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-889">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-889">Pattern</span></span>

<span data-ttu-id="d0622-890">캐나다 은행 계좌 번호는 7 또는 12자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="d0622-891">캐나다 은행 계좌 송금 번호:</span><span class="sxs-lookup"><span data-stu-id="d0622-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="d0622-892">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-892">Five digits</span></span> 
- <span data-ttu-id="d0622-893">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-893">A hyphen</span></span> 
- <span data-ttu-id="d0622-894">3 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="d0622-894">Three digits OR</span></span>
- <span data-ttu-id="d0622-895">"0"</span><span class="sxs-lookup"><span data-stu-id="d0622-895">A zero "0"</span></span> 
- <span data-ttu-id="d0622-896">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-897">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-897">Checksum</span></span>

<span data-ttu-id="d0622-898">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-899">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-899">Definition</span></span>

<span data-ttu-id="d0622-900">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-901">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-902">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="d0622-903">Regex_canada_bank_account_transit_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="d0622-904">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-905">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-906">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-907">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="d0622-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="d0622-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="d0622-909">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="d0622-909">canada savings bonds</span></span>
- <span data-ttu-id="d0622-910">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="d0622-910">canada revenue agency</span></span>
- <span data-ttu-id="d0622-911">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="d0622-911">canadian financial institution</span></span>
- <span data-ttu-id="d0622-912">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="d0622-912">direct deposit form</span></span>
- <span data-ttu-id="d0622-913">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="d0622-913">canadian citizen</span></span>
- <span data-ttu-id="d0622-914">legal representative</span><span class="sxs-lookup"><span data-stu-id="d0622-914">legal representative</span></span>
- <span data-ttu-id="d0622-915">notary public</span><span class="sxs-lookup"><span data-stu-id="d0622-915">notary public</span></span>
- <span data-ttu-id="d0622-916">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="d0622-916">commissioner for oaths</span></span>
- <span data-ttu-id="d0622-917">child care benefit</span><span class="sxs-lookup"><span data-stu-id="d0622-917">child care benefit</span></span>
- <span data-ttu-id="d0622-918">universal child care</span><span class="sxs-lookup"><span data-stu-id="d0622-918">universal child care</span></span>
- <span data-ttu-id="d0622-919">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="d0622-919">canada child tax benefit</span></span>
- <span data-ttu-id="d0622-920">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="d0622-920">income tax benefit</span></span>
- <span data-ttu-id="d0622-921">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="d0622-921">harmonized sales tax</span></span>
- <span data-ttu-id="d0622-922">social insurance number</span><span class="sxs-lookup"><span data-stu-id="d0622-922">social insurance number</span></span>
- <span data-ttu-id="d0622-923">income tax refund</span><span class="sxs-lookup"><span data-stu-id="d0622-923">income tax refund</span></span>
- <span data-ttu-id="d0622-924">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="d0622-924">child tax benefit</span></span>
- <span data-ttu-id="d0622-925">territorial payments</span><span class="sxs-lookup"><span data-stu-id="d0622-925">territorial payments</span></span>
- <span data-ttu-id="d0622-926">institution number</span><span class="sxs-lookup"><span data-stu-id="d0622-926">institution number</span></span>
- <span data-ttu-id="d0622-927">deposit request</span><span class="sxs-lookup"><span data-stu-id="d0622-927">deposit request</span></span>
- <span data-ttu-id="d0622-928">banking information</span><span class="sxs-lookup"><span data-stu-id="d0622-928">banking information</span></span>
- <span data-ttu-id="d0622-929">direct deposit</span><span class="sxs-lookup"><span data-stu-id="d0622-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="d0622-930">캐나다 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-931">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-931">Format</span></span>

<span data-ttu-id="d0622-932">지역마다 다름</span><span class="sxs-lookup"><span data-stu-id="d0622-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-933">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-933">Pattern</span></span>

<span data-ttu-id="d0622-934">앨버타, 브리티시 콜롬비아, 매니토바, 뉴브런즈윅, 뉴펀들랜드/래브라도, 노바스코샤, 온타리오, 프린스에드워드아일랜드, 퀘벡 및 서스캐처원을 포함하는 다양한 패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-935">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-935">Checksum</span></span>

<span data-ttu-id="d0622-936">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-937">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-937">Definition</span></span>

<span data-ttu-id="d0622-938">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-939">Func_[province_name]_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-940">Keyword_[province_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="d0622-941">Keyword_canada_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-942">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="d0622-943">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="d0622-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="d0622-944">시/도 약어(예: AB)</span><span class="sxs-lookup"><span data-stu-id="d0622-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="d0622-945">시/도 이름(예: 앨버타)</span><span class="sxs-lookup"><span data-stu-id="d0622-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="d0622-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d0622-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="d0622-947">DL</span><span class="sxs-lookup"><span data-stu-id="d0622-947">DL</span></span>
- <span data-ttu-id="d0622-948">된다</span><span class="sxs-lookup"><span data-stu-id="d0622-948">DLS</span></span>
- <span data-ttu-id="d0622-949">CDL</span><span class="sxs-lookup"><span data-stu-id="d0622-949">CDL</span></span>
- <span data-ttu-id="d0622-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="d0622-950">CDLS</span></span>
- <span data-ttu-id="d0622-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="d0622-951">DriverLic</span></span>
- <span data-ttu-id="d0622-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="d0622-952">DriverLics</span></span>
- <span data-ttu-id="d0622-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="d0622-953">DriverLicense</span></span>
- <span data-ttu-id="d0622-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="d0622-954">DriverLicenses</span></span>
- <span data-ttu-id="d0622-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="d0622-955">DriverLicence</span></span>
- <span data-ttu-id="d0622-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="d0622-956">DriverLicences</span></span>
- <span data-ttu-id="d0622-957">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-957">Driver Lic</span></span>
- <span data-ttu-id="d0622-958">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-958">Driver Lics</span></span>
- <span data-ttu-id="d0622-959">Driver License</span><span class="sxs-lookup"><span data-stu-id="d0622-959">Driver License</span></span>
- <span data-ttu-id="d0622-960">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-960">Driver Licenses</span></span>
- <span data-ttu-id="d0622-961">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-961">Driver Licence</span></span>
- <span data-ttu-id="d0622-962">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-962">Driver Licences</span></span>
- <span data-ttu-id="d0622-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="d0622-963">DriversLic</span></span>
- <span data-ttu-id="d0622-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="d0622-964">DriversLics</span></span>
- <span data-ttu-id="d0622-965">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-965">DriversLicence</span></span>
- <span data-ttu-id="d0622-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="d0622-966">DriversLicences</span></span>
- <span data-ttu-id="d0622-967">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-967">DriversLicense</span></span>
- <span data-ttu-id="d0622-968">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-968">DriversLicenses</span></span>
- <span data-ttu-id="d0622-969">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-969">Drivers Lic</span></span>
- <span data-ttu-id="d0622-970">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-970">Drivers Lics</span></span>
- <span data-ttu-id="d0622-971">Drivers License</span><span class="sxs-lookup"><span data-stu-id="d0622-971">Drivers License</span></span>
- <span data-ttu-id="d0622-972">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-972">Drivers Licenses</span></span>
- <span data-ttu-id="d0622-973">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-973">Drivers Licence</span></span>
- <span data-ttu-id="d0622-974">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-974">Drivers Licences</span></span>
- <span data-ttu-id="d0622-975">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-975">Driver'Lic</span></span>
- <span data-ttu-id="d0622-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-976">Driver'Lics</span></span>
- <span data-ttu-id="d0622-977">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-977">Driver'License</span></span>
- <span data-ttu-id="d0622-978">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-978">Driver'Licenses</span></span>
- <span data-ttu-id="d0622-979">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-979">Driver'Licence</span></span>
- <span data-ttu-id="d0622-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-980">Driver'Licences</span></span>
- <span data-ttu-id="d0622-981">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-981">Driver' Lic</span></span>
- <span data-ttu-id="d0622-982">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-982">Driver' Lics</span></span>
- <span data-ttu-id="d0622-983">Driver' License</span><span class="sxs-lookup"><span data-stu-id="d0622-983">Driver' License</span></span>
- <span data-ttu-id="d0622-984">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-984">Driver' Licenses</span></span>
- <span data-ttu-id="d0622-985">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-985">Driver' Licence</span></span>
- <span data-ttu-id="d0622-986">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-986">Driver' Licences</span></span>
- <span data-ttu-id="d0622-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="d0622-987">Driver'sLic</span></span>
- <span data-ttu-id="d0622-988">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="d0622-988">Driver'sLics</span></span>
- <span data-ttu-id="d0622-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="d0622-989">Driver'sLicense</span></span>
- <span data-ttu-id="d0622-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="d0622-990">Driver'sLicenses</span></span>
- <span data-ttu-id="d0622-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="d0622-991">Driver'sLicence</span></span>
- <span data-ttu-id="d0622-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="d0622-992">Driver'sLicences</span></span>
- <span data-ttu-id="d0622-993">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-993">Driver's Lic</span></span>
- <span data-ttu-id="d0622-994">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-994">Driver's Lics</span></span>
- <span data-ttu-id="d0622-995">Driver's License</span><span class="sxs-lookup"><span data-stu-id="d0622-995">Driver's License</span></span>
- <span data-ttu-id="d0622-996">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-996">Driver's Licenses</span></span>
- <span data-ttu-id="d0622-997">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-997">Driver's Licence</span></span>
- <span data-ttu-id="d0622-998">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-998">Driver's Licences</span></span>
- <span data-ttu-id="d0622-999">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="d0622-999">Permis de Conduire</span></span>
- <span data-ttu-id="d0622-1000">id</span><span class="sxs-lookup"><span data-stu-id="d0622-1000">id</span></span>
- <span data-ttu-id="d0622-1001">번호가</span><span class="sxs-lookup"><span data-stu-id="d0622-1001">ids</span></span>
- <span data-ttu-id="d0622-1002">idcard number</span><span class="sxs-lookup"><span data-stu-id="d0622-1002">idcard number</span></span>
- <span data-ttu-id="d0622-1003">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="d0622-1003">idcard numbers</span></span>
- <span data-ttu-id="d0622-1004">idcard #</span><span class="sxs-lookup"><span data-stu-id="d0622-1004">idcard #</span></span>
- <span data-ttu-id="d0622-1005">idcard #s</span><span class="sxs-lookup"><span data-stu-id="d0622-1005">idcard #s</span></span>
- <span data-ttu-id="d0622-1006">idcard card</span><span class="sxs-lookup"><span data-stu-id="d0622-1006">idcard card</span></span>
- <span data-ttu-id="d0622-1007">idcard cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1007">idcard cards</span></span>
- <span data-ttu-id="d0622-1008">idcard</span><span class="sxs-lookup"><span data-stu-id="d0622-1008">idcard</span></span>
- <span data-ttu-id="d0622-1009">identification number</span><span class="sxs-lookup"><span data-stu-id="d0622-1009">identification number</span></span>
- <span data-ttu-id="d0622-1010">identification numbers</span><span class="sxs-lookup"><span data-stu-id="d0622-1010">identification numbers</span></span>
- <span data-ttu-id="d0622-1011">identification #</span><span class="sxs-lookup"><span data-stu-id="d0622-1011">identification #</span></span>
- <span data-ttu-id="d0622-1012">identification #s</span><span class="sxs-lookup"><span data-stu-id="d0622-1012">identification #s</span></span>
- <span data-ttu-id="d0622-1013">identification card</span><span class="sxs-lookup"><span data-stu-id="d0622-1013">identification card</span></span>
- <span data-ttu-id="d0622-1014">identification cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1014">identification cards</span></span>
- <span data-ttu-id="d0622-1015">확인과</span><span class="sxs-lookup"><span data-stu-id="d0622-1015">identification</span></span> 
- <span data-ttu-id="d0622-1016">DL #</span><span class="sxs-lookup"><span data-stu-id="d0622-1016">DL#</span></span>
- <span data-ttu-id="d0622-1017">된다 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1017">DLS#</span></span> 
- <span data-ttu-id="d0622-1018">CDL #</span><span class="sxs-lookup"><span data-stu-id="d0622-1018">CDL#</span></span> 
- <span data-ttu-id="d0622-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="d0622-1019">CDLS#</span></span> 
- <span data-ttu-id="d0622-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-1020">DriverLic#</span></span> 
- <span data-ttu-id="d0622-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="d0622-1021">DriverLics#</span></span> 
- <span data-ttu-id="d0622-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="d0622-1022">DriverLicense#</span></span> 
- <span data-ttu-id="d0622-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="d0622-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="d0622-1024">DriverLicence#</span></span> 
- <span data-ttu-id="d0622-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="d0622-1025">DriverLicences#</span></span> 
- <span data-ttu-id="d0622-1026">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-1026">Driver Lic#</span></span>
- <span data-ttu-id="d0622-1027">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-1027">Driver Lics#</span></span> 
- <span data-ttu-id="d0622-1028">Driver License#</span><span class="sxs-lookup"><span data-stu-id="d0622-1028">Driver License#</span></span> 
- <span data-ttu-id="d0622-1029">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="d0622-1030">Driver License#</span><span class="sxs-lookup"><span data-stu-id="d0622-1030">Driver License#</span></span> 
- <span data-ttu-id="d0622-1031">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="d0622-1031">Driver Licences#</span></span> 
- <span data-ttu-id="d0622-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-1032">DriversLic#</span></span> 
- <span data-ttu-id="d0622-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="d0622-1033">DriversLics#</span></span> 
- <span data-ttu-id="d0622-1034">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1034">DriversLicense#</span></span> 
- <span data-ttu-id="d0622-1035">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="d0622-1036">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1036">DriversLicence#</span></span> 
- <span data-ttu-id="d0622-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="d0622-1037">DriversLicences#</span></span> 
- <span data-ttu-id="d0622-1038">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="d0622-1039">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="d0622-1040">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="d0622-1040">Drivers License#</span></span> 
- <span data-ttu-id="d0622-1041">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="d0622-1042">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="d0622-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="d0622-1043">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="d0622-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="d0622-1044">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="d0622-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="d0622-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="d0622-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="d0622-1046">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1046">Driver'License#</span></span> 
- <span data-ttu-id="d0622-1047">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="d0622-1048">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="d0622-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="d0622-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="d0622-1050">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="d0622-1051">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="d0622-1052">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="d0622-1052">Driver' License#</span></span> 
- <span data-ttu-id="d0622-1053">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="d0622-1054">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="d0622-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="d0622-1055">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="d0622-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="d0622-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="d0622-1057">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="d0622-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="d0622-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="d0622-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="d0622-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="d0622-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="d0622-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="d0622-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="d0622-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="d0622-1062">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="d0622-1063">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="d0622-1064">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="d0622-1064">Driver's License#</span></span> 
- <span data-ttu-id="d0622-1065">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="d0622-1066">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="d0622-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="d0622-1067">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="d0622-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="d0622-1068">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="d0622-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="d0622-1069">i #</span><span class="sxs-lookup"><span data-stu-id="d0622-1069">id#</span></span> 
- <span data-ttu-id="d0622-1070">번호가 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1070">ids#</span></span> 
- <span data-ttu-id="d0622-1071">idcard card#</span><span class="sxs-lookup"><span data-stu-id="d0622-1071">idcard card#</span></span> 
- <span data-ttu-id="d0622-1072">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="d0622-1072">idcard cards#</span></span> 
- <span data-ttu-id="d0622-1073">idcard #</span><span class="sxs-lookup"><span data-stu-id="d0622-1073">idcard#</span></span> 
- <span data-ttu-id="d0622-1074">identification card#</span><span class="sxs-lookup"><span data-stu-id="d0622-1074">identification card#</span></span> 
- <span data-ttu-id="d0622-1075">identification cards#</span><span class="sxs-lookup"><span data-stu-id="d0622-1075">identification cards#</span></span> 
- <span data-ttu-id="d0622-1076">확인과 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="d0622-1077">캐나다 건강 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1078">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1078">Format</span></span>

<span data-ttu-id="d0622-1079">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1080">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1080">Pattern</span></span>

<span data-ttu-id="d0622-1081">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1082">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1082">Checksum</span></span>

<span data-ttu-id="d0622-1083">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1084">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1084">Definition</span></span>

<span data-ttu-id="d0622-1085">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1086">Regex_canada_health_service_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1087">Keyword_canada_health_service_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1088">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="d0622-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="d0622-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="d0622-1090">personal health number</span><span class="sxs-lookup"><span data-stu-id="d0622-1090">personal health number</span></span>
- <span data-ttu-id="d0622-1091">patient information</span><span class="sxs-lookup"><span data-stu-id="d0622-1091">patient information</span></span>
- <span data-ttu-id="d0622-1092">health services</span><span class="sxs-lookup"><span data-stu-id="d0622-1092">health services</span></span>
- <span data-ttu-id="d0622-1093">speciality services</span><span class="sxs-lookup"><span data-stu-id="d0622-1093">speciality services</span></span>
- <span data-ttu-id="d0622-1094">automobile accident</span><span class="sxs-lookup"><span data-stu-id="d0622-1094">automobile accident</span></span>
- <span data-ttu-id="d0622-1095">patient hospital</span><span class="sxs-lookup"><span data-stu-id="d0622-1095">patient hospital</span></span>
- <span data-ttu-id="d0622-1096">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="d0622-1096">psychiatrist</span></span>
- <span data-ttu-id="d0622-1097">workers compensation</span><span class="sxs-lookup"><span data-stu-id="d0622-1097">workers compensation</span></span>
- <span data-ttu-id="d0622-1098">종류</span><span class="sxs-lookup"><span data-stu-id="d0622-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="d0622-1099">캐나다 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1100">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1100">Format</span></span>

<span data-ttu-id="d0622-1101">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1102">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1102">Pattern</span></span>

<span data-ttu-id="d0622-1103">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1104">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1104">Checksum</span></span>

<span data-ttu-id="d0622-1105">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1106">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1106">Definition</span></span>

<span data-ttu-id="d0622-1107">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1108">Regex_canada_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1109">Keyword_canada_passport_number 또는 Keyword_passport의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1110">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="d0622-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="d0622-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="d0622-1112">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="d0622-1112">canadian citizenship</span></span>
- <span data-ttu-id="d0622-1113">canadian passport</span><span class="sxs-lookup"><span data-stu-id="d0622-1113">canadian passport</span></span>
- <span data-ttu-id="d0622-1114">passport application</span><span class="sxs-lookup"><span data-stu-id="d0622-1114">passport application</span></span>
- <span data-ttu-id="d0622-1115">passport photos</span><span class="sxs-lookup"><span data-stu-id="d0622-1115">passport photos</span></span>
- <span data-ttu-id="d0622-1116">certified translator</span><span class="sxs-lookup"><span data-stu-id="d0622-1116">certified translator</span></span>
- <span data-ttu-id="d0622-1117">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="d0622-1117">canadian citizens</span></span>
- <span data-ttu-id="d0622-1118">processing times</span><span class="sxs-lookup"><span data-stu-id="d0622-1118">processing times</span></span>
- <span data-ttu-id="d0622-1119">renewal application</span><span class="sxs-lookup"><span data-stu-id="d0622-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="d0622-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-1120">Keyword_passport</span></span>

- <span data-ttu-id="d0622-1121">Passport Number</span><span class="sxs-lookup"><span data-stu-id="d0622-1121">Passport Number</span></span>
- <span data-ttu-id="d0622-1122">Passport No</span><span class="sxs-lookup"><span data-stu-id="d0622-1122">Passport No</span></span>
- <span data-ttu-id="d0622-1123">Passport #</span><span class="sxs-lookup"><span data-stu-id="d0622-1123">Passport #</span></span>
- <span data-ttu-id="d0622-1124">여권 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1124">Passport#</span></span>
- <span data-ttu-id="d0622-1125">PassportID</span><span class="sxs-lookup"><span data-stu-id="d0622-1125">PassportID</span></span>
- <span data-ttu-id="d0622-1126">Passportno</span><span class="sxs-lookup"><span data-stu-id="d0622-1126">Passportno</span></span>
- <span data-ttu-id="d0622-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-1127">passportnumber</span></span>
- <span data-ttu-id="d0622-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="d0622-1128">パスポート</span></span>
- <span data-ttu-id="d0622-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="d0622-1129">パスポート番号</span></span>
- <span data-ttu-id="d0622-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="d0622-1130">パスポートのNum</span></span>
- <span data-ttu-id="d0622-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="d0622-1131">パスポート＃</span></span>
- <span data-ttu-id="d0622-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d0622-1132">Numéro de passeport</span></span>
- <span data-ttu-id="d0622-1133">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="d0622-1133">Passeport n °</span></span>
- <span data-ttu-id="d0622-1134">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="d0622-1134">Passeport Non</span></span>
- <span data-ttu-id="d0622-1135">Passeport #</span><span class="sxs-lookup"><span data-stu-id="d0622-1135">Passeport #</span></span>
- <span data-ttu-id="d0622-1136">포트 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1136">Passeport#</span></span>
- <span data-ttu-id="d0622-1137">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="d0622-1137">PasseportNon</span></span>
- <span data-ttu-id="d0622-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="d0622-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="d0622-1139">캐나다 PHIN(개인 건강 식별 번호)</span><span class="sxs-lookup"><span data-stu-id="d0622-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1140">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1140">Format</span></span>

<span data-ttu-id="d0622-1141">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1142">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1142">Pattern</span></span>

<span data-ttu-id="d0622-1143">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1144">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1144">Checksum</span></span>

<span data-ttu-id="d0622-1145">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1146">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1146">Definition</span></span>

<span data-ttu-id="d0622-1147">DLP 정책은 300 문자 (예: Regex_canada_phin)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="d0622-1148">Keyword_canada_phin 또는 Keyword_canada_provinces의 키워드를 두 개 이상 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1149">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="d0622-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="d0622-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="d0622-1151">social insurance number</span><span class="sxs-lookup"><span data-stu-id="d0622-1151">social insurance number</span></span>
- <span data-ttu-id="d0622-1152">health information act</span><span class="sxs-lookup"><span data-stu-id="d0622-1152">health information act</span></span>
- <span data-ttu-id="d0622-1153">income tax information</span><span class="sxs-lookup"><span data-stu-id="d0622-1153">income tax information</span></span>
- <span data-ttu-id="d0622-1154">manitoba health</span><span class="sxs-lookup"><span data-stu-id="d0622-1154">manitoba health</span></span>
- <span data-ttu-id="d0622-1155">health registration</span><span class="sxs-lookup"><span data-stu-id="d0622-1155">health registration</span></span>
- <span data-ttu-id="d0622-1156">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="d0622-1156">prescription purchases</span></span>
- <span data-ttu-id="d0622-1157">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="d0622-1157">benefit eligibility</span></span>
- <span data-ttu-id="d0622-1158">personal health</span><span class="sxs-lookup"><span data-stu-id="d0622-1158">personal health</span></span>
- <span data-ttu-id="d0622-1159">power of attorney</span><span class="sxs-lookup"><span data-stu-id="d0622-1159">power of attorney</span></span>
- <span data-ttu-id="d0622-1160">registration number</span><span class="sxs-lookup"><span data-stu-id="d0622-1160">registration number</span></span>
- <span data-ttu-id="d0622-1161">personal health number</span><span class="sxs-lookup"><span data-stu-id="d0622-1161">personal health number</span></span>
- <span data-ttu-id="d0622-1162">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="d0622-1162">practitioner referral</span></span>
- <span data-ttu-id="d0622-1163">wellness professional</span><span class="sxs-lookup"><span data-stu-id="d0622-1163">wellness professional</span></span>
- <span data-ttu-id="d0622-1164">patient referral</span><span class="sxs-lookup"><span data-stu-id="d0622-1164">patient referral</span></span>
- <span data-ttu-id="d0622-1165">health and wellness</span><span class="sxs-lookup"><span data-stu-id="d0622-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="d0622-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="d0622-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="d0622-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="d0622-1167">Nunavut</span></span>
- <span data-ttu-id="d0622-1168">퀘벡</span><span class="sxs-lookup"><span data-stu-id="d0622-1168">Quebec</span></span>
- <span data-ttu-id="d0622-1169">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="d0622-1169">Northwest Territories</span></span>
- <span data-ttu-id="d0622-1170">온타리오</span><span class="sxs-lookup"><span data-stu-id="d0622-1170">Ontario</span></span>
- <span data-ttu-id="d0622-1171">British Columbia</span><span class="sxs-lookup"><span data-stu-id="d0622-1171">British Columbia</span></span>
- <span data-ttu-id="d0622-1172">앨버타</span><span class="sxs-lookup"><span data-stu-id="d0622-1172">Alberta</span></span>
- <span data-ttu-id="d0622-1173">서스캐처원</span><span class="sxs-lookup"><span data-stu-id="d0622-1173">Saskatchewan</span></span>
- <span data-ttu-id="d0622-1174">매니토바</span><span class="sxs-lookup"><span data-stu-id="d0622-1174">Manitoba</span></span>
- <span data-ttu-id="d0622-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="d0622-1175">Yukon</span></span>
- <span data-ttu-id="d0622-1176">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="d0622-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="d0622-1177">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="d0622-1177">New Brunswick</span></span>
- <span data-ttu-id="d0622-1178">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="d0622-1178">Nova Scotia</span></span>
- <span data-ttu-id="d0622-1179">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="d0622-1179">Prince Edward Island</span></span>
- <span data-ttu-id="d0622-1180">캐나다</span><span class="sxs-lookup"><span data-stu-id="d0622-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="d0622-1181">캐나다 사회 보험 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1182">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1182">Format</span></span>

<span data-ttu-id="d0622-1183">선택적 하이픈 또는 공백을 포함하는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1184">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1184">Pattern</span></span>

<span data-ttu-id="d0622-1185">서식이</span><span class="sxs-lookup"><span data-stu-id="d0622-1185">Formatted:</span></span>
- <span data-ttu-id="d0622-1186">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1186">Three digits</span></span> 
- <span data-ttu-id="d0622-1187">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="d0622-1187">A hyphen or space</span></span> 
- <span data-ttu-id="d0622-1188">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1188">Three digits</span></span> 
- <span data-ttu-id="d0622-1189">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="d0622-1189">A hyphen or space</span></span> 
- <span data-ttu-id="d0622-1190">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1190">Three digits</span></span>

<span data-ttu-id="d0622-1191">서식 없음: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1192">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1192">Checksum</span></span>

<span data-ttu-id="d0622-1193">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1194">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1194">Definition</span></span>

<span data-ttu-id="d0622-1195">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1196">Func_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1197">2개 이상의 다음 항목 조합:</span><span class="sxs-lookup"><span data-stu-id="d0622-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="d0622-1198">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="d0622-1199">Keyword_sin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="d0622-1200">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="d0622-1201">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1201">The checksum passes.</span></span>

<span data-ttu-id="d0622-1202">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1203">Func_unformatted_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1204">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="d0622-1205">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1205">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1206">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="d0622-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="d0622-1207">Keyword_sin</span></span>

- <span data-ttu-id="d0622-1208">sin</span><span class="sxs-lookup"><span data-stu-id="d0622-1208">sin</span></span> 
- <span data-ttu-id="d0622-1209">social insurance</span><span class="sxs-lookup"><span data-stu-id="d0622-1209">social insurance</span></span> 
- <span data-ttu-id="d0622-1210">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="d0622-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="d0622-1211">죄</span><span class="sxs-lookup"><span data-stu-id="d0622-1211">sins</span></span> 
- <span data-ttu-id="d0622-1212">ssn</span><span class="sxs-lookup"><span data-stu-id="d0622-1212">ssn</span></span> 
- <span data-ttu-id="d0622-1213">있는 ssn</span><span class="sxs-lookup"><span data-stu-id="d0622-1213">ssns</span></span> 
- <span data-ttu-id="d0622-1214">social security</span><span class="sxs-lookup"><span data-stu-id="d0622-1214">social security</span></span> 
- <span data-ttu-id="d0622-1215">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="d0622-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="d0622-1216">national identification number</span><span class="sxs-lookup"><span data-stu-id="d0622-1216">national identification number</span></span> 
- <span data-ttu-id="d0622-1217">national id</span><span class="sxs-lookup"><span data-stu-id="d0622-1217">national id</span></span> 
- <span data-ttu-id="d0622-1218">sin #</span><span class="sxs-lookup"><span data-stu-id="d0622-1218">sin#</span></span> 
- <span data-ttu-id="d0622-1219">soc ins</span><span class="sxs-lookup"><span data-stu-id="d0622-1219">soc ins</span></span> 
- <span data-ttu-id="d0622-1220">social ins</span><span class="sxs-lookup"><span data-stu-id="d0622-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="d0622-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="d0622-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="d0622-1222">driver's license</span><span class="sxs-lookup"><span data-stu-id="d0622-1222">driver's license</span></span> 
- <span data-ttu-id="d0622-1223">drivers license</span><span class="sxs-lookup"><span data-stu-id="d0622-1223">drivers license</span></span> 
- <span data-ttu-id="d0622-1224">driver's licence</span><span class="sxs-lookup"><span data-stu-id="d0622-1224">driver's licence</span></span> 
- <span data-ttu-id="d0622-1225">drivers licence</span><span class="sxs-lookup"><span data-stu-id="d0622-1225">drivers licence</span></span> 
- <span data-ttu-id="d0622-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="d0622-1226">DOB</span></span> 
- <span data-ttu-id="d0622-1227">생년월일</span><span class="sxs-lookup"><span data-stu-id="d0622-1227">Birthdate</span></span> 
- <span data-ttu-id="d0622-1228">생일</span><span class="sxs-lookup"><span data-stu-id="d0622-1228">Birthday</span></span> 
- <span data-ttu-id="d0622-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="d0622-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="d0622-1230">	칠레 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1231">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1231">Format</span></span>

<span data-ttu-id="d0622-1232">7-8 자리 숫자와 구분 기호 확인 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1233">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1233">Pattern</span></span>

<span data-ttu-id="d0622-1234">7-8자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="d0622-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="d0622-1235">1-2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1235">1-2 digits</span></span> 
- <span data-ttu-id="d0622-1236">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-1236">A period</span></span> 
- <span data-ttu-id="d0622-1237">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1237">Three digits</span></span> 
- <span data-ttu-id="d0622-1238">마침표 </span><span class="sxs-lookup"><span data-stu-id="d0622-1238">A period</span></span> 
- <span data-ttu-id="d0622-1239">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1239">Three digits</span></span> 
- <span data-ttu-id="d0622-1240">대시 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-1240">A dash</span></span> 
- <span data-ttu-id="d0622-1241">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1242">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1242">Checksum</span></span>

<span data-ttu-id="d0622-1243">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1244">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1244">Definition</span></span>

<span data-ttu-id="d0622-1245">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1246">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1247">Keyword_chile_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="d0622-1248">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1248">The checksum passes.</span></span>

<span data-ttu-id="d0622-1249">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1250">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1251">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1251">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1252">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="d0622-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="d0622-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="d0622-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="d0622-1254">National Identification Number</span></span> 
- <span data-ttu-id="d0622-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="d0622-1255">Identity card</span></span> 
- <span data-ttu-id="d0622-1256">ID</span><span class="sxs-lookup"><span data-stu-id="d0622-1256">ID</span></span> 
- <span data-ttu-id="d0622-1257">확인과</span><span class="sxs-lookup"><span data-stu-id="d0622-1257">Identification</span></span> 
- <span data-ttu-id="d0622-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="d0622-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="d0622-1259">실행</span><span class="sxs-lookup"><span data-stu-id="d0622-1259">RUN</span></span> 
- <span data-ttu-id="d0622-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="d0622-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="d0622-1261">RUT</span><span class="sxs-lookup"><span data-stu-id="d0622-1261">RUT</span></span> 
- <span data-ttu-id="d0622-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="d0622-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="d0622-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="d0622-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="d0622-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="d0622-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="d0622-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="d0622-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="d0622-1266">	중국 주민 ID 카드(PRC) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1267">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1267">Format</span></span>

<span data-ttu-id="d0622-1268">18자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1269">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1269">Pattern</span></span>

<span data-ttu-id="d0622-1270">18자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-1270">18 digits:</span></span>
- <span data-ttu-id="d0622-1271">주소 코드에 해당하는 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="d0622-1272">생년월일에 해당하는 YYYYMMDD 형식의 8자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="d0622-1273">주문 코드에 해당하는 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="d0622-1274">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1275">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1275">Checksum</span></span>

<span data-ttu-id="d0622-1276">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1277">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1277">Definition</span></span>

<span data-ttu-id="d0622-1278">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1279">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1280">Keyword_china_resident_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="d0622-1281">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1281">The checksum passes.</span></span>

<span data-ttu-id="d0622-1282">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1283">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1284">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1284">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1285">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="d0622-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="d0622-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="d0622-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="d0622-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="d0622-1288">중국</span><span class="sxs-lookup"><span data-stu-id="d0622-1288">PRC</span></span> 
- <span data-ttu-id="d0622-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="d0622-1289">National Identification Card</span></span> 
- <span data-ttu-id="d0622-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="d0622-1290">身份证</span></span> 
- <span data-ttu-id="d0622-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="d0622-1291">居民 身份证</span></span> 
- <span data-ttu-id="d0622-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="d0622-1292">居民身份证</span></span> 
- <span data-ttu-id="d0622-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="d0622-1293">鉴定</span></span> 
- <span data-ttu-id="d0622-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-1294">身分證</span></span> 
- <span data-ttu-id="d0622-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-1295">居民 身份證</span></span>
- <span data-ttu-id="d0622-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="d0622-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="d0622-1297">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1298">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1298">Format</span></span>

<span data-ttu-id="d0622-1299">서식이 있거나 서식이 없을 수 있는 16 자리 (dddddddddddddddd), Luhn 테스트를 통과 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1300">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1300">Pattern</span></span>

<span data-ttu-id="d0622-1301">Visa, MasterCard, Discover Card, JCB, American Express, 상품권 및 식사권을 비롯하여 전 세계 모든 주요 브랜드 카드를 검색하는 매우 복잡하고 강력한 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1302">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1302">Checksum</span></span>

<span data-ttu-id="d0622-1303">있음(Luhn 체크섬)</span><span class="sxs-lookup"><span data-stu-id="d0622-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1304">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1304">Definition</span></span>

<span data-ttu-id="d0622-1305">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1306">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1307">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1307">One of the following is true:</span></span>
    - <span data-ttu-id="d0622-1308">Keyword_cc_verification의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="d0622-1309">Keyword_cc_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="d0622-1310">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="d0622-1311">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1311">The checksum passes.</span></span>

<span data-ttu-id="d0622-1312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1313">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1314">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1314">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1315">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="d0622-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="d0622-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="d0622-1317">card verification</span><span class="sxs-lookup"><span data-stu-id="d0622-1317">card verification</span></span>
- <span data-ttu-id="d0622-1318">card identification number</span><span class="sxs-lookup"><span data-stu-id="d0622-1318">card identification number</span></span>
- <span data-ttu-id="d0622-1319">cvn</span><span class="sxs-lookup"><span data-stu-id="d0622-1319">cvn</span></span>
- <span data-ttu-id="d0622-1320">cid</span><span class="sxs-lookup"><span data-stu-id="d0622-1320">cid</span></span>
- <span data-ttu-id="d0622-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="d0622-1321">cvc2</span></span>
- <span data-ttu-id="d0622-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="d0622-1322">cvv2</span></span>
- <span data-ttu-id="d0622-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="d0622-1323">pin block</span></span>
- <span data-ttu-id="d0622-1324">security code</span><span class="sxs-lookup"><span data-stu-id="d0622-1324">security code</span></span>
- <span data-ttu-id="d0622-1325">security number</span><span class="sxs-lookup"><span data-stu-id="d0622-1325">security number</span></span>
- <span data-ttu-id="d0622-1326">security no</span><span class="sxs-lookup"><span data-stu-id="d0622-1326">security no</span></span>
- <span data-ttu-id="d0622-1327">issue number</span><span class="sxs-lookup"><span data-stu-id="d0622-1327">issue number</span></span>
- <span data-ttu-id="d0622-1328">issue no</span><span class="sxs-lookup"><span data-stu-id="d0622-1328">issue no</span></span>
- <span data-ttu-id="d0622-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="d0622-1329">cryptogramme</span></span>
- <span data-ttu-id="d0622-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="d0622-1330">numéro de sécurité</span></span>
- <span data-ttu-id="d0622-1331">numero de securite</span><span class="sxs-lookup"><span data-stu-id="d0622-1331">numero de securite</span></span>
- <span data-ttu-id="d0622-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="d0622-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="d0622-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="d0622-1334">prüfziffer</span></span>
- <span data-ttu-id="d0622-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="d0622-1335">prufziffer</span></span>
- <span data-ttu-id="d0622-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="d0622-1336">sicherheits Kode</span></span>
- <span data-ttu-id="d0622-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="d0622-1337">sicherheitscode</span></span>
- <span data-ttu-id="d0622-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="d0622-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="d0622-1339">verfalldatum</span></span>
- <span data-ttu-id="d0622-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="d0622-1340">codice di verifica</span></span>
- <span data-ttu-id="d0622-1341">cod.</span><span class="sxs-lookup"><span data-stu-id="d0622-1341">cod.</span></span> <span data-ttu-id="d0622-1342">sicurezza</span><span class="sxs-lookup"><span data-stu-id="d0622-1342">sicurezza</span></span>
- <span data-ttu-id="d0622-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="d0622-1343">cod sicurezza</span></span>
- <span data-ttu-id="d0622-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d0622-1344">n autorizzazione</span></span>
- <span data-ttu-id="d0622-1345">código</span><span class="sxs-lookup"><span data-stu-id="d0622-1345">código</span></span>
- <span data-ttu-id="d0622-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="d0622-1346">codigo</span></span>
- <span data-ttu-id="d0622-1347">cod.</span><span class="sxs-lookup"><span data-stu-id="d0622-1347">cod.</span></span> <span data-ttu-id="d0622-1348">seg</span><span class="sxs-lookup"><span data-stu-id="d0622-1348">seg</span></span>
- <span data-ttu-id="d0622-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="d0622-1349">cod seg</span></span>
- <span data-ttu-id="d0622-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1350">código de segurança</span></span>
- <span data-ttu-id="d0622-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1351">codigo de seguranca</span></span>
- <span data-ttu-id="d0622-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1352">codigo de segurança</span></span>
- <span data-ttu-id="d0622-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1353">código de seguranca</span></span>
- <span data-ttu-id="d0622-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="d0622-1354">cód.</span></span> <span data-ttu-id="d0622-1355">segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1355">segurança</span></span>
- <span data-ttu-id="d0622-1356">cod.</span><span class="sxs-lookup"><span data-stu-id="d0622-1356">cod.</span></span> <span data-ttu-id="d0622-1357">seguranca cod</span><span class="sxs-lookup"><span data-stu-id="d0622-1357">seguranca cod.</span></span> <span data-ttu-id="d0622-1358">segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1358">segurança</span></span>
- <span data-ttu-id="d0622-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="d0622-1359">cód.</span></span> <span data-ttu-id="d0622-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1360">seguranca</span></span>
- <span data-ttu-id="d0622-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1361">cód segurança</span></span>
- <span data-ttu-id="d0622-1362">cod seguranca cod segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="d0622-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1363">cód seguranca</span></span>
- <span data-ttu-id="d0622-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="d0622-1364">número de verificação</span></span>
- <span data-ttu-id="d0622-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="d0622-1365">numero de verificacao</span></span>
- <span data-ttu-id="d0622-1366">ablauf</span><span class="sxs-lookup"><span data-stu-id="d0622-1366">ablauf</span></span>
- <span data-ttu-id="d0622-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="d0622-1367">gültig bis</span></span>
- <span data-ttu-id="d0622-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="d0622-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="d0622-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="d0622-1369">gultig bis</span></span>
- <span data-ttu-id="d0622-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="d0622-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="d0622-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="d0622-1371">scadenza</span></span>
- <span data-ttu-id="d0622-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="d0622-1372">data scad</span></span>
- <span data-ttu-id="d0622-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="d0622-1373">fecha de expiracion</span></span>
- <span data-ttu-id="d0622-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="d0622-1374">fecha de venc</span></span>
- <span data-ttu-id="d0622-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="d0622-1375">vencimiento</span></span>
- <span data-ttu-id="d0622-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="d0622-1376">válido hasta</span></span>
- <span data-ttu-id="d0622-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="d0622-1377">valido hasta</span></span>
- <span data-ttu-id="d0622-1378">vto</span><span class="sxs-lookup"><span data-stu-id="d0622-1378">vto</span></span>
- <span data-ttu-id="d0622-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="d0622-1379">data de expiração</span></span>
- <span data-ttu-id="d0622-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="d0622-1380">data de expiracao</span></span>
- <span data-ttu-id="d0622-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="d0622-1381">data em que expira</span></span>
- <span data-ttu-id="d0622-1382">유효한 ade</span><span class="sxs-lookup"><span data-stu-id="d0622-1382">validade</span></span>
- <span data-ttu-id="d0622-1383">valor</span><span class="sxs-lookup"><span data-stu-id="d0622-1383">valor</span></span>
- <span data-ttu-id="d0622-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="d0622-1384">vencimento</span></span>
- <span data-ttu-id="d0622-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="d0622-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="d0622-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="d0622-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="d0622-1387">amex</span><span class="sxs-lookup"><span data-stu-id="d0622-1387">amex</span></span>
- <span data-ttu-id="d0622-1388">american express</span><span class="sxs-lookup"><span data-stu-id="d0622-1388">american express</span></span>
- <span data-ttu-id="d0622-1389">americanexpress</span><span class="sxs-lookup"><span data-stu-id="d0622-1389">americanexpress</span></span>
- <span data-ttu-id="d0622-1390">Visa</span><span class="sxs-lookup"><span data-stu-id="d0622-1390">Visa</span></span>
- <span data-ttu-id="d0622-1391">mastercard</span><span class="sxs-lookup"><span data-stu-id="d0622-1391">mastercard</span></span>
- <span data-ttu-id="d0622-1392">master card</span><span class="sxs-lookup"><span data-stu-id="d0622-1392">master card</span></span>
- <span data-ttu-id="d0622-1393">mc</span><span class="sxs-lookup"><span data-stu-id="d0622-1393">mc</span></span> 
- <span data-ttu-id="d0622-1394">mastercards</span><span class="sxs-lookup"><span data-stu-id="d0622-1394">mastercards</span></span>
- <span data-ttu-id="d0622-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1395">master cards</span></span>
- <span data-ttu-id="d0622-1396">diner's Club</span><span class="sxs-lookup"><span data-stu-id="d0622-1396">diner's Club</span></span>
- <span data-ttu-id="d0622-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="d0622-1397">diners club</span></span>
- <span data-ttu-id="d0622-1398">dinersclub</span><span class="sxs-lookup"><span data-stu-id="d0622-1398">dinersclub</span></span>
- <span data-ttu-id="d0622-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="d0622-1399">discover card</span></span>
- <span data-ttu-id="d0622-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="d0622-1400">discovercard</span></span>
- <span data-ttu-id="d0622-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1401">discover cards</span></span>
- <span data-ttu-id="d0622-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="d0622-1402">JCB</span></span>
- <span data-ttu-id="d0622-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="d0622-1403">japanese card bureau</span></span>
- <span data-ttu-id="d0622-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="d0622-1404">carte blanche</span></span>
- <span data-ttu-id="d0622-1405">carteblanche</span><span class="sxs-lookup"><span data-stu-id="d0622-1405">carteblanche</span></span>
- <span data-ttu-id="d0622-1406">credit card</span><span class="sxs-lookup"><span data-stu-id="d0622-1406">credit card</span></span>
- <span data-ttu-id="d0622-1407">참조란 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1407">cc#</span></span>
- <span data-ttu-id="d0622-1408">참조 #:</span><span class="sxs-lookup"><span data-stu-id="d0622-1408">cc#:</span></span>
- <span data-ttu-id="d0622-1409">expiration date</span><span class="sxs-lookup"><span data-stu-id="d0622-1409">expiration date</span></span>
- <span data-ttu-id="d0622-1410">exp date</span><span class="sxs-lookup"><span data-stu-id="d0622-1410">exp date</span></span>
- <span data-ttu-id="d0622-1411">expiry date</span><span class="sxs-lookup"><span data-stu-id="d0622-1411">expiry date</span></span>
- <span data-ttu-id="d0622-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="d0622-1412">date d’expiration</span></span>
- <span data-ttu-id="d0622-1413">date d'exp</span><span class="sxs-lookup"><span data-stu-id="d0622-1413">date d'exp</span></span>
- <span data-ttu-id="d0622-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="d0622-1414">date expiration</span></span>
- <span data-ttu-id="d0622-1415">bank card</span><span class="sxs-lookup"><span data-stu-id="d0622-1415">bank card</span></span>
- <span data-ttu-id="d0622-1416">bankcard</span><span class="sxs-lookup"><span data-stu-id="d0622-1416">bankcard</span></span>
- <span data-ttu-id="d0622-1417">card number</span><span class="sxs-lookup"><span data-stu-id="d0622-1417">card number</span></span>
- <span data-ttu-id="d0622-1418">card num</span><span class="sxs-lookup"><span data-stu-id="d0622-1418">card num</span></span>
- <span data-ttu-id="d0622-1419">전화 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1419">cardnumber</span></span>
- <span data-ttu-id="d0622-1420">시 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1420">cardnumbers</span></span>
- <span data-ttu-id="d0622-1421">card numbers</span><span class="sxs-lookup"><span data-stu-id="d0622-1421">card numbers</span></span>
- <span data-ttu-id="d0622-1422">카드</span><span class="sxs-lookup"><span data-stu-id="d0622-1422">creditcard</span></span>
- <span data-ttu-id="d0622-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1423">credit cards</span></span>
- <span data-ttu-id="d0622-1424">creditcards</span><span class="sxs-lookup"><span data-stu-id="d0622-1424">creditcards</span></span>
- <span data-ttu-id="d0622-1425">ccn</span><span class="sxs-lookup"><span data-stu-id="d0622-1425">ccn</span></span>
- <span data-ttu-id="d0622-1426">card holder</span><span class="sxs-lookup"><span data-stu-id="d0622-1426">card holder</span></span>
- <span data-ttu-id="d0622-1427">소유자</span><span class="sxs-lookup"><span data-stu-id="d0622-1427">cardholder</span></span>
- <span data-ttu-id="d0622-1428">card holders</span><span class="sxs-lookup"><span data-stu-id="d0622-1428">card holders</span></span>
- <span data-ttu-id="d0622-1429">에이 홀더</span><span class="sxs-lookup"><span data-stu-id="d0622-1429">cardholders</span></span>
- <span data-ttu-id="d0622-1430">check card</span><span class="sxs-lookup"><span data-stu-id="d0622-1430">check card</span></span>
- <span data-ttu-id="d0622-1431">checkcard</span><span class="sxs-lookup"><span data-stu-id="d0622-1431">checkcard</span></span>
- <span data-ttu-id="d0622-1432">check cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1432">check cards</span></span>
- <span data-ttu-id="d0622-1433">checkcards</span><span class="sxs-lookup"><span data-stu-id="d0622-1433">checkcards</span></span>
- <span data-ttu-id="d0622-1434">debit card</span><span class="sxs-lookup"><span data-stu-id="d0622-1434">debit card</span></span>
- <span data-ttu-id="d0622-1435">debitcard</span><span class="sxs-lookup"><span data-stu-id="d0622-1435">debitcard</span></span>
- <span data-ttu-id="d0622-1436">debit cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1436">debit cards</span></span>
- <span data-ttu-id="d0622-1437">debitcards</span><span class="sxs-lookup"><span data-stu-id="d0622-1437">debitcards</span></span>
- <span data-ttu-id="d0622-1438">atm card</span><span class="sxs-lookup"><span data-stu-id="d0622-1438">atm card</span></span>
- <span data-ttu-id="d0622-1439">atmcard</span><span class="sxs-lookup"><span data-stu-id="d0622-1439">atmcard</span></span>
- <span data-ttu-id="d0622-1440">atm cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1440">atm cards</span></span>
- <span data-ttu-id="d0622-1441">atmcards</span><span class="sxs-lookup"><span data-stu-id="d0622-1441">atmcards</span></span>
- <span data-ttu-id="d0622-1442">enroute</span><span class="sxs-lookup"><span data-stu-id="d0622-1442">enroute</span></span>
- <span data-ttu-id="d0622-1443">en route</span><span class="sxs-lookup"><span data-stu-id="d0622-1443">en route</span></span>
- <span data-ttu-id="d0622-1444">card type</span><span class="sxs-lookup"><span data-stu-id="d0622-1444">card type</span></span>
- <span data-ttu-id="d0622-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="d0622-1445">carte bancaire</span></span>
- <span data-ttu-id="d0622-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="d0622-1446">carte de crédit</span></span>
- <span data-ttu-id="d0622-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="d0622-1447">carte de credit</span></span>
- <span data-ttu-id="d0622-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="d0622-1448">numéro de carte</span></span>
- <span data-ttu-id="d0622-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="d0622-1449">numero de carte</span></span>
- <span data-ttu-id="d0622-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="d0622-1450">nº de la carte</span></span>
- <span data-ttu-id="d0622-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="d0622-1451">nº de carte</span></span>
- <span data-ttu-id="d0622-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="d0622-1452">kreditkarte</span></span>
- <span data-ttu-id="d0622-1453">karte</span><span class="sxs-lookup"><span data-stu-id="d0622-1453">karte</span></span>
- <span data-ttu-id="d0622-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="d0622-1454">karteninhaber</span></span>
- <span data-ttu-id="d0622-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="d0622-1455">karteninhabers</span></span>
- <span data-ttu-id="d0622-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="d0622-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="d0622-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="d0622-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="d0622-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="d0622-1458">kreditkartentyp</span></span>
- <span data-ttu-id="d0622-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="d0622-1459">eigentümername</span></span>
- <span data-ttu-id="d0622-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="d0622-1460">kartennr</span></span> 
- <span data-ttu-id="d0622-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1461">kartennummer</span></span>
- <span data-ttu-id="d0622-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1462">kreditkartennummer</span></span>
- <span data-ttu-id="d0622-1463">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="d0622-1464">carta di credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1464">carta di credito</span></span>
- <span data-ttu-id="d0622-1465">carta credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1465">carta credito</span></span>
- <span data-ttu-id="d0622-1466">카 ta</span><span class="sxs-lookup"><span data-stu-id="d0622-1466">carta</span></span>
- <span data-ttu-id="d0622-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1467">n carta</span></span>
- <span data-ttu-id="d0622-1468">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="d0622-1468">nr.</span></span> <span data-ttu-id="d0622-1469">카 ta</span><span class="sxs-lookup"><span data-stu-id="d0622-1469">carta</span></span>
- <span data-ttu-id="d0622-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1470">nr carta</span></span>
- <span data-ttu-id="d0622-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1471">numero carta</span></span>
- <span data-ttu-id="d0622-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1472">numero della carta</span></span>
- <span data-ttu-id="d0622-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1473">numero di carta</span></span>
- <span data-ttu-id="d0622-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1474">tarjeta credito</span></span>
- <span data-ttu-id="d0622-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1475">tarjeta de credito</span></span>
- <span data-ttu-id="d0622-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="d0622-1476">tarjeta crédito</span></span>
- <span data-ttu-id="d0622-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="d0622-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="d0622-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="d0622-1478">tarjeta de atm</span></span>
- <span data-ttu-id="d0622-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="d0622-1479">tarjeta atm</span></span>
- <span data-ttu-id="d0622-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1480">tarjeta debito</span></span>
- <span data-ttu-id="d0622-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1481">tarjeta de debito</span></span>
- <span data-ttu-id="d0622-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="d0622-1482">tarjeta débito</span></span>
- <span data-ttu-id="d0622-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="d0622-1483">tarjeta de débito</span></span>
- <span data-ttu-id="d0622-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1484">nº de tarjeta</span></span>
- <span data-ttu-id="d0622-1485">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1485">no.</span></span> <span data-ttu-id="d0622-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1486">de tarjeta</span></span>
- <span data-ttu-id="d0622-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1487">no de tarjeta</span></span>
- <span data-ttu-id="d0622-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1488">numero de tarjeta</span></span>
- <span data-ttu-id="d0622-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1489">número de tarjeta</span></span>
- <span data-ttu-id="d0622-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="d0622-1490">tarjeta no</span></span>
- <span data-ttu-id="d0622-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="d0622-1491">tarjetahabiente</span></span>
- <span data-ttu-id="d0622-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="d0622-1492">cartão de crédito</span></span>
- <span data-ttu-id="d0622-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1493">cartão de credito</span></span>
- <span data-ttu-id="d0622-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="d0622-1494">cartao de crédito</span></span>
- <span data-ttu-id="d0622-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1495">cartao de credito</span></span>
- <span data-ttu-id="d0622-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="d0622-1496">cartão de débito</span></span>
- <span data-ttu-id="d0622-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="d0622-1497">cartao de débito</span></span>
- <span data-ttu-id="d0622-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1498">cartão de debito</span></span>
- <span data-ttu-id="d0622-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1499">cartao de debito</span></span>
- <span data-ttu-id="d0622-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="d0622-1500">débito automático</span></span>
- <span data-ttu-id="d0622-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="d0622-1501">debito automatico</span></span>
- <span data-ttu-id="d0622-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1502">número do cartão</span></span>
- <span data-ttu-id="d0622-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1503">numero do cartão</span></span> 
- <span data-ttu-id="d0622-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1504">número do cartao</span></span>
- <span data-ttu-id="d0622-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1505">numero do cartao</span></span>
- <span data-ttu-id="d0622-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1506">número de cartão</span></span>
- <span data-ttu-id="d0622-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1507">numero de cartão</span></span>
- <span data-ttu-id="d0622-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1508">número de cartao</span></span>
- <span data-ttu-id="d0622-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1509">numero de cartao</span></span>
- <span data-ttu-id="d0622-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1510">nº do cartão</span></span>
- <span data-ttu-id="d0622-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1511">nº do cartao</span></span>
- <span data-ttu-id="d0622-1512">n º</span><span class="sxs-lookup"><span data-stu-id="d0622-1512">nº.</span></span> <span data-ttu-id="d0622-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1513">do cartão</span></span>
- <span data-ttu-id="d0622-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1514">no do cartão</span></span>
- <span data-ttu-id="d0622-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1515">no do cartao</span></span>
- <span data-ttu-id="d0622-1516">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1516">no.</span></span> <span data-ttu-id="d0622-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1517">do cartão</span></span>
- <span data-ttu-id="d0622-1518">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1518">no.</span></span> <span data-ttu-id="d0622-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="d0622-1520">크로아티아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1521">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1521">Format</span></span>

<span data-ttu-id="d0622-1522">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1523">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1523">Pattern</span></span>

<span data-ttu-id="d0622-1524">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1525">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1525">Checksum</span></span>

<span data-ttu-id="d0622-1526">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1527">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1527">Definition</span></span>

<span data-ttu-id="d0622-1528">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1529">Func_croatia_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1530">Keyword_croatia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-1531">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="d0622-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="d0622-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="d0622-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="d0622-1533">Croatian identity card</span></span>
- <span data-ttu-id="d0622-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="d0622-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="d0622-1535">크로아티아 개인 식별(OIB) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1536">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1536">Format</span></span>

<span data-ttu-id="d0622-1537">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1538">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1538">Pattern</span></span>

<span data-ttu-id="d0622-1539">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-1539">11 digits:</span></span>
- <span data-ttu-id="d0622-1540">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1540">10 digits</span></span> 
- <span data-ttu-id="d0622-1541">최종 자릿수는 국제 데이터 교환 목적을 위한 검사 숫자 이며, HR는 11 자리 숫자 앞에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1542">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1542">Checksum</span></span>

<span data-ttu-id="d0622-1543">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1544">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1544">Definition</span></span>

<span data-ttu-id="d0622-1545">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1546">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1547">Keyword_croatia_oib_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="d0622-1548">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1548">The checksum passes.</span></span>

<span data-ttu-id="d0622-1549">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1550">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1551">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1551">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1552">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="d0622-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="d0622-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="d0622-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="d0622-1554">Personal Identification Number</span></span>
- <span data-ttu-id="d0622-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="d0622-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="d0622-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="d0622-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="d0622-1557">체코어 개인 Id 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1558">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1558">Format</span></span>

<span data-ttu-id="d0622-1559">선택적 슬래시 (이전 형식)가 있는 9 자리 숫자와 슬래시 (새 형식)가 있는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1560">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1560">Pattern</span></span>

<span data-ttu-id="d0622-1561">9 자리 숫자 (이전 형식):</span><span class="sxs-lookup"><span data-stu-id="d0622-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="d0622-1562">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1562">Nine digits</span></span>

<span data-ttu-id="d0622-1563">또는</span><span class="sxs-lookup"><span data-stu-id="d0622-1563">OR</span></span>

- <span data-ttu-id="d0622-1564">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="d0622-1565">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="d0622-1565">A forward slash</span></span>
- <span data-ttu-id="d0622-1566">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1566">Three digits</span></span>

<span data-ttu-id="d0622-1567">10 자리 숫자 (새 형식):</span><span class="sxs-lookup"><span data-stu-id="d0622-1567">10 digits (new format):</span></span>
- <span data-ttu-id="d0622-1568">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1568">10 digits</span></span>

<span data-ttu-id="d0622-1569">또는</span><span class="sxs-lookup"><span data-stu-id="d0622-1569">OR</span></span>

- <span data-ttu-id="d0622-1570">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="d0622-1571">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="d0622-1571">A forward slash</span></span> 
- <span data-ttu-id="d0622-1572">마지막 숫자가 검사 숫자인 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1573">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1573">Checksum</span></span>

<span data-ttu-id="d0622-1574">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1575">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1575">Definition</span></span>

<span data-ttu-id="d0622-1576">DLP 정책은 300 문자 근사에서 Func_czech_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="d0622-1577">Keyword_czech_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="d0622-1578">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1578">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="d0622-1579">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1579">Keywords</span></span>

- <span data-ttu-id="d0622-1580">체코어 개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1580">czech personal identity number</span></span>
- <span data-ttu-id="d0622-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="d0622-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="d0622-1582">덴마크 개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1583">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1583">Format</span></span>

<span data-ttu-id="d0622-1584">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1585">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1585">Pattern</span></span>

<span data-ttu-id="d0622-1586">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-1586">10 digits:</span></span>
- <span data-ttu-id="d0622-1587">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="d0622-1588">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-1588">A hyphen</span></span> 
- <span data-ttu-id="d0622-1589">마지막 숫자가 검사 숫자인 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1590">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1590">Checksum</span></span>

<span data-ttu-id="d0622-1591">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1592">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1592">Definition</span></span>

<span data-ttu-id="d0622-1593">DLP 정책은 300 문자 (예: Regex_denmark_id)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="d0622-1594">Keyword_denmark_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="d0622-1595">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1595">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-1596">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="d0622-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="d0622-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="d0622-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="d0622-1598">Personal Identification Number</span></span>
- <span data-ttu-id="d0622-1599">CPR</span><span class="sxs-lookup"><span data-stu-id="d0622-1599">CPR</span></span>
- <span data-ttu-id="d0622-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="d0622-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="d0622-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="d0622-1602">DEA(약물 집행 기구) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1603">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1603">Format</span></span>

<span data-ttu-id="d0622-1604">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1605">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1605">Pattern</span></span>

<span data-ttu-id="d0622-1606">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="d0622-1607">등록 코드에 해당하는 abcdefghjklmnprstux 중 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="d0622-1608">등록자 성의 첫 문자에 해당하는 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="d0622-1609">검사 숫자의 마지막 7개 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1610">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1610">Checksum</span></span>

<span data-ttu-id="d0622-1611">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1612">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1612">Definition</span></span>

<span data-ttu-id="d0622-1613">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1614">Func_dea_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1615">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1615">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-1616">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1616">Keywords</span></span>

<span data-ttu-id="d0622-1617">없음</span><span class="sxs-lookup"><span data-stu-id="d0622-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="d0622-1618">유럽 직불 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1619">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1619">Format</span></span>

<span data-ttu-id="d0622-1620">16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1621">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1621">Pattern</span></span>

<span data-ttu-id="d0622-1622">매우 복잡하고 강력한 패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1623">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1623">Checksum</span></span>

<span data-ttu-id="d0622-1624">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1625">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1625">Definition</span></span>

<span data-ttu-id="d0622-1626">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1627">Func_eu_debit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1628">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="d0622-1629">Keyword_eu_debit_card의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="d0622-1630">Keyword_card_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="d0622-1631">Keyword_card_security_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="d0622-1632">Keyword_card_expiration_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="d0622-1633">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="d0622-1634">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1634">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1635">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="d0622-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="d0622-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="d0622-1637">account number</span><span class="sxs-lookup"><span data-stu-id="d0622-1637">account number</span></span> 
- <span data-ttu-id="d0622-1638">card number</span><span class="sxs-lookup"><span data-stu-id="d0622-1638">card number</span></span> 
- <span data-ttu-id="d0622-1639">card no.</span><span class="sxs-lookup"><span data-stu-id="d0622-1639">card no.</span></span> 
- <span data-ttu-id="d0622-1640">security number</span><span class="sxs-lookup"><span data-stu-id="d0622-1640">security number</span></span> 
- <span data-ttu-id="d0622-1641">참조란 #</span><span class="sxs-lookup"><span data-stu-id="d0622-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="d0622-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="d0622-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="d0622-1643">acct nbr</span><span class="sxs-lookup"><span data-stu-id="d0622-1643">acct nbr</span></span> 
- <span data-ttu-id="d0622-1644">acct num</span><span class="sxs-lookup"><span data-stu-id="d0622-1644">acct num</span></span> 
- <span data-ttu-id="d0622-1645">acct no</span><span class="sxs-lookup"><span data-stu-id="d0622-1645">acct no</span></span> 
- <span data-ttu-id="d0622-1646">american express</span><span class="sxs-lookup"><span data-stu-id="d0622-1646">american express</span></span> 
- <span data-ttu-id="d0622-1647">americanexpress</span><span class="sxs-lookup"><span data-stu-id="d0622-1647">americanexpress</span></span> 
- <span data-ttu-id="d0622-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="d0622-1648">americano espresso</span></span> 
- <span data-ttu-id="d0622-1649">amex</span><span class="sxs-lookup"><span data-stu-id="d0622-1649">amex</span></span> 
- <span data-ttu-id="d0622-1650">atm card</span><span class="sxs-lookup"><span data-stu-id="d0622-1650">atm card</span></span> 
- <span data-ttu-id="d0622-1651">atm cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1651">atm cards</span></span> 
- <span data-ttu-id="d0622-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="d0622-1652">atm kaart</span></span> 
- <span data-ttu-id="d0622-1653">atmcard</span><span class="sxs-lookup"><span data-stu-id="d0622-1653">atmcard</span></span> 
- <span data-ttu-id="d0622-1654">atmcards</span><span class="sxs-lookup"><span data-stu-id="d0622-1654">atmcards</span></span> 
- <span data-ttu-id="d0622-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="d0622-1655">atmkaart</span></span> 
- <span data-ttu-id="d0622-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="d0622-1656">atmkaarten</span></span> 
- <span data-ttu-id="d0622-1657">bancontact</span><span class="sxs-lookup"><span data-stu-id="d0622-1657">bancontact</span></span> 
- <span data-ttu-id="d0622-1658">bank card</span><span class="sxs-lookup"><span data-stu-id="d0622-1658">bank card</span></span> 
- <span data-ttu-id="d0622-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="d0622-1659">bankkaart</span></span> 
- <span data-ttu-id="d0622-1660">card holder</span><span class="sxs-lookup"><span data-stu-id="d0622-1660">card holder</span></span> 
- <span data-ttu-id="d0622-1661">card holders</span><span class="sxs-lookup"><span data-stu-id="d0622-1661">card holders</span></span> 
- <span data-ttu-id="d0622-1662">card num</span><span class="sxs-lookup"><span data-stu-id="d0622-1662">card num</span></span> 
- <span data-ttu-id="d0622-1663">card number</span><span class="sxs-lookup"><span data-stu-id="d0622-1663">card number</span></span> 
- <span data-ttu-id="d0622-1664">card numbers</span><span class="sxs-lookup"><span data-stu-id="d0622-1664">card numbers</span></span> 
- <span data-ttu-id="d0622-1665">card type</span><span class="sxs-lookup"><span data-stu-id="d0622-1665">card type</span></span> 
- <span data-ttu-id="d0622-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="d0622-1666">cardano numerico</span></span> 
- <span data-ttu-id="d0622-1667">소유자</span><span class="sxs-lookup"><span data-stu-id="d0622-1667">cardholder</span></span> 
- <span data-ttu-id="d0622-1668">에이 홀더</span><span class="sxs-lookup"><span data-stu-id="d0622-1668">cardholders</span></span> 
- <span data-ttu-id="d0622-1669">전화 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1669">cardnumber</span></span> 
- <span data-ttu-id="d0622-1670">시 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1670">cardnumbers</span></span> 
- <span data-ttu-id="d0622-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="d0622-1671">carta bianca</span></span> 
- <span data-ttu-id="d0622-1672">carta credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1672">carta credito</span></span> 
- <span data-ttu-id="d0622-1673">carta di credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1673">carta di credito</span></span> 
- <span data-ttu-id="d0622-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1674">cartao de credito</span></span> 
- <span data-ttu-id="d0622-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="d0622-1675">cartao de crédito</span></span> 
- <span data-ttu-id="d0622-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1676">cartao de debito</span></span> 
- <span data-ttu-id="d0622-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="d0622-1677">cartao de débito</span></span> 
- <span data-ttu-id="d0622-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="d0622-1678">carte bancaire</span></span> 
- <span data-ttu-id="d0622-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="d0622-1679">carte blanche</span></span> 
- <span data-ttu-id="d0622-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="d0622-1680">carte bleue</span></span> 
- <span data-ttu-id="d0622-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="d0622-1681">carte de credit</span></span> 
- <span data-ttu-id="d0622-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="d0622-1682">carte de crédit</span></span> 
- <span data-ttu-id="d0622-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1683">carte di credito</span></span> 
- <span data-ttu-id="d0622-1684">carteblanche</span><span class="sxs-lookup"><span data-stu-id="d0622-1684">carteblanche</span></span> 
- <span data-ttu-id="d0622-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1685">cartão de credito</span></span> 
- <span data-ttu-id="d0622-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="d0622-1686">cartão de crédito</span></span> 
- <span data-ttu-id="d0622-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1687">cartão de debito</span></span> 
- <span data-ttu-id="d0622-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="d0622-1688">cartão de débito</span></span> 
- <span data-ttu-id="d0622-1689">cb</span><span class="sxs-lookup"><span data-stu-id="d0622-1689">cb</span></span> 
- <span data-ttu-id="d0622-1690">ccn</span><span class="sxs-lookup"><span data-stu-id="d0622-1690">ccn</span></span> 
- <span data-ttu-id="d0622-1691">check card</span><span class="sxs-lookup"><span data-stu-id="d0622-1691">check card</span></span> 
- <span data-ttu-id="d0622-1692">check cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1692">check cards</span></span> 
- <span data-ttu-id="d0622-1693">checkcard</span><span class="sxs-lookup"><span data-stu-id="d0622-1693">checkcard</span></span>
- <span data-ttu-id="d0622-1694">checkcards</span><span class="sxs-lookup"><span data-stu-id="d0622-1694">checkcards</span></span> 
- <span data-ttu-id="d0622-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="d0622-1695">chequekaart</span></span> 
- <span data-ttu-id="d0622-1696">cirrus</span><span class="sxs-lookup"><span data-stu-id="d0622-1696">cirrus</span></span> 
- <span data-ttu-id="d0622-1697">cirrus-edc-maestro</span><span class="sxs-lookup"><span data-stu-id="d0622-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="d0622-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="d0622-1698">controlekaart</span></span> 
- <span data-ttu-id="d0622-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="d0622-1699">controlekaarten</span></span> 
- <span data-ttu-id="d0622-1700">credit card</span><span class="sxs-lookup"><span data-stu-id="d0622-1700">credit card</span></span> 
- <span data-ttu-id="d0622-1701">credit cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1701">credit cards</span></span> 
- <span data-ttu-id="d0622-1702">카드</span><span class="sxs-lookup"><span data-stu-id="d0622-1702">creditcard</span></span> 
- <span data-ttu-id="d0622-1703">creditcards</span><span class="sxs-lookup"><span data-stu-id="d0622-1703">creditcards</span></span> 
- <span data-ttu-id="d0622-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="d0622-1704">debetkaart</span></span> 
- <span data-ttu-id="d0622-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="d0622-1705">debetkaarten</span></span> 
- <span data-ttu-id="d0622-1706">debit card</span><span class="sxs-lookup"><span data-stu-id="d0622-1706">debit card</span></span> 
- <span data-ttu-id="d0622-1707">debit cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1707">debit cards</span></span> 
- <span data-ttu-id="d0622-1708">debitcard</span><span class="sxs-lookup"><span data-stu-id="d0622-1708">debitcard</span></span> 
- <span data-ttu-id="d0622-1709">debitcards</span><span class="sxs-lookup"><span data-stu-id="d0622-1709">debitcards</span></span> 
- <span data-ttu-id="d0622-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="d0622-1710">debito automatico</span></span> 
- <span data-ttu-id="d0622-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="d0622-1711">diners club</span></span> 
- <span data-ttu-id="d0622-1712">dinersclub</span><span class="sxs-lookup"><span data-stu-id="d0622-1712">dinersclub</span></span> 
- <span data-ttu-id="d0622-1713">찾아보십시오</span><span class="sxs-lookup"><span data-stu-id="d0622-1713">discover</span></span> 
- <span data-ttu-id="d0622-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="d0622-1714">discover card</span></span> 
- <span data-ttu-id="d0622-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1715">discover cards</span></span> 
- <span data-ttu-id="d0622-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="d0622-1716">discovercard</span></span> 
- <span data-ttu-id="d0622-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="d0622-1717">discovercards</span></span> 
- <span data-ttu-id="d0622-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="d0622-1718">débito automático</span></span>
- <span data-ttu-id="d0622-1719">edc</span><span class="sxs-lookup"><span data-stu-id="d0622-1719">edc</span></span> 
- <span data-ttu-id="d0622-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="d0622-1720">eigentümername</span></span> 
- <span data-ttu-id="d0622-1721">european debit card</span><span class="sxs-lookup"><span data-stu-id="d0622-1721">european debit card</span></span> 
- <span data-ttu-id="d0622-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="d0622-1722">hoofdkaart</span></span> 
- <span data-ttu-id="d0622-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="d0622-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="d0622-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="d0622-1724">in viaggio</span></span> 
- <span data-ttu-id="d0622-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="d0622-1725">japanese card bureau</span></span> 
- <span data-ttu-id="d0622-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="d0622-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="d0622-1727">jcb</span><span class="sxs-lookup"><span data-stu-id="d0622-1727">jcb</span></span> 
- <span data-ttu-id="d0622-1728">kaart</span><span class="sxs-lookup"><span data-stu-id="d0622-1728">kaart</span></span> 
- <span data-ttu-id="d0622-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="d0622-1729">kaart num</span></span> 
- <span data-ttu-id="d0622-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="d0622-1730">kaartaantal</span></span> 
- <span data-ttu-id="d0622-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="d0622-1731">kaartaantallen</span></span> 
- <span data-ttu-id="d0622-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="d0622-1732">kaarthouder</span></span> 
- <span data-ttu-id="d0622-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="d0622-1733">kaarthouders</span></span> 
- <span data-ttu-id="d0622-1734">karte</span><span class="sxs-lookup"><span data-stu-id="d0622-1734">karte</span></span>  
- <span data-ttu-id="d0622-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="d0622-1735">karteninhaber</span></span> 
- <span data-ttu-id="d0622-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="d0622-1736">karteninhabers</span></span>
- <span data-ttu-id="d0622-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="d0622-1737">kartennr</span></span> 
- <span data-ttu-id="d0622-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1738">kartennummer</span></span> 
- <span data-ttu-id="d0622-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="d0622-1739">kreditkarte</span></span> 
- <span data-ttu-id="d0622-1740">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="d0622-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="d0622-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="d0622-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="d0622-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="d0622-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="d0622-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="d0622-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="d0622-1745">maestro</span><span class="sxs-lookup"><span data-stu-id="d0622-1745">maestro</span></span> 
- <span data-ttu-id="d0622-1746">master card</span><span class="sxs-lookup"><span data-stu-id="d0622-1746">master card</span></span> 
- <span data-ttu-id="d0622-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="d0622-1747">master cards</span></span> 
- <span data-ttu-id="d0622-1748">mastercard</span><span class="sxs-lookup"><span data-stu-id="d0622-1748">mastercard</span></span> 
- <span data-ttu-id="d0622-1749">mastercards</span><span class="sxs-lookup"><span data-stu-id="d0622-1749">mastercards</span></span> 
- <span data-ttu-id="d0622-1750">mc</span><span class="sxs-lookup"><span data-stu-id="d0622-1750">mc</span></span> 
- <span data-ttu-id="d0622-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="d0622-1751">mister cash</span></span> 
- <span data-ttu-id="d0622-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1752">n carta</span></span> 
- <span data-ttu-id="d0622-1753">카 ta</span><span class="sxs-lookup"><span data-stu-id="d0622-1753">carta</span></span> 
- <span data-ttu-id="d0622-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1754">no de tarjeta</span></span> 
- <span data-ttu-id="d0622-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1755">no do cartao</span></span> 
- <span data-ttu-id="d0622-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1756">no do cartão</span></span> 
- <span data-ttu-id="d0622-1757">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1757">no.</span></span> <span data-ttu-id="d0622-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1758">de tarjeta</span></span> 
- <span data-ttu-id="d0622-1759">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1759">no.</span></span> <span data-ttu-id="d0622-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1760">do cartao</span></span> 
- <span data-ttu-id="d0622-1761">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1761">no.</span></span> <span data-ttu-id="d0622-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1762">do cartão</span></span> 
- <span data-ttu-id="d0622-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1763">nr carta</span></span> 
- <span data-ttu-id="d0622-1764">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="d0622-1764">nr.</span></span> <span data-ttu-id="d0622-1765">카 ta</span><span class="sxs-lookup"><span data-stu-id="d0622-1765">carta</span></span> 
- <span data-ttu-id="d0622-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="d0622-1766">numeri di scheda</span></span> 
- <span data-ttu-id="d0622-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1767">numero carta</span></span> 
- <span data-ttu-id="d0622-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1768">numero de cartao</span></span> 
- <span data-ttu-id="d0622-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="d0622-1769">numero de carte</span></span> 
- <span data-ttu-id="d0622-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1770">numero de cartão</span></span> 
- <span data-ttu-id="d0622-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1771">numero de tarjeta</span></span>
- <span data-ttu-id="d0622-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1772">numero della carta</span></span> 
- <span data-ttu-id="d0622-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1773">numero di carta</span></span> 
- <span data-ttu-id="d0622-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="d0622-1774">numero di scheda</span></span> 
- <span data-ttu-id="d0622-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1775">numero do cartao</span></span> 
- <span data-ttu-id="d0622-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1776">numero do cartão</span></span> 
- <span data-ttu-id="d0622-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="d0622-1777">numéro de carte</span></span> 
- <span data-ttu-id="d0622-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="d0622-1778">nº carta</span></span> 
- <span data-ttu-id="d0622-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="d0622-1779">nº de carte</span></span> 
- <span data-ttu-id="d0622-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="d0622-1780">nº de la carte</span></span> 
- <span data-ttu-id="d0622-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="d0622-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1782">nº do cartao</span></span> 
- <span data-ttu-id="d0622-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1783">nº do cartão</span></span> 
- <span data-ttu-id="d0622-1784">n º</span><span class="sxs-lookup"><span data-stu-id="d0622-1784">nº.</span></span> <span data-ttu-id="d0622-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1785">do cartão</span></span> 
- <span data-ttu-id="d0622-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1786">número de cartao</span></span> 
- <span data-ttu-id="d0622-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="d0622-1787">número de cartão</span></span> 
- <span data-ttu-id="d0622-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="d0622-1788">número de tarjeta</span></span> 
- <span data-ttu-id="d0622-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="d0622-1789">número do cartao</span></span> 
- <span data-ttu-id="d0622-1790">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="d0622-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="d0622-1791">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="d0622-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="d0622-1792">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="d0622-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="d0622-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="d0622-1793">scheda della banca</span></span> 
- <span data-ttu-id="d0622-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="d0622-1794">scheda di controllo</span></span> 
- <span data-ttu-id="d0622-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1795">scheda di debito</span></span> 
- <span data-ttu-id="d0622-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="d0622-1796">scheda matrice</span></span> 
- <span data-ttu-id="d0622-1797">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="d0622-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="d0622-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="d0622-1798">schede di controllo</span></span> 
- <span data-ttu-id="d0622-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1799">schede di debito</span></span> 
- <span data-ttu-id="d0622-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="d0622-1800">schede matrici</span></span> 
- <span data-ttu-id="d0622-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="d0622-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="d0622-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="d0622-1802">scoprono le schede</span></span> 
- <span data-ttu-id="d0622-1803">분리</span><span class="sxs-lookup"><span data-stu-id="d0622-1803">solo</span></span> 
- <span data-ttu-id="d0622-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="d0622-1804">supporti di scheda</span></span> 
- <span data-ttu-id="d0622-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="d0622-1805">supporto di scheda</span></span> 
- <span data-ttu-id="d0622-1806">스위치</span><span class="sxs-lookup"><span data-stu-id="d0622-1806">switch</span></span> 
- <span data-ttu-id="d0622-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="d0622-1807">tarjeta atm</span></span> 
- <span data-ttu-id="d0622-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1808">tarjeta credito</span></span> 
- <span data-ttu-id="d0622-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="d0622-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="d0622-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="d0622-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="d0622-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="d0622-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="d0622-1812">tarjeta debito</span></span> 
- <span data-ttu-id="d0622-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="d0622-1813">tarjeta no</span></span>
- <span data-ttu-id="d0622-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="d0622-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="d0622-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="d0622-1815">tipo della scheda</span></span> 
- <span data-ttu-id="d0622-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="d0622-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="d0622-1817">scheda</span><span class="sxs-lookup"><span data-stu-id="d0622-1817">scheda</span></span> 
- <span data-ttu-id="d0622-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="d0622-1818">v pay</span></span> 
- <span data-ttu-id="d0622-1819">v-지급</span><span class="sxs-lookup"><span data-stu-id="d0622-1819">v-pay</span></span> 
- <span data-ttu-id="d0622-1820">visa</span><span class="sxs-lookup"><span data-stu-id="d0622-1820">visa</span></span> 
- <span data-ttu-id="d0622-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="d0622-1821">visa plus</span></span> 
- <span data-ttu-id="d0622-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="d0622-1822">visa electron</span></span> 
- <span data-ttu-id="d0622-1823">visto</span><span class="sxs-lookup"><span data-stu-id="d0622-1823">visto</span></span> 
- <span data-ttu-id="d0622-1824">visum</span><span class="sxs-lookup"><span data-stu-id="d0622-1824">visum</span></span> 
- <span data-ttu-id="d0622-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="d0622-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="d0622-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="d0622-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="d0622-1827">card identification number</span><span class="sxs-lookup"><span data-stu-id="d0622-1827">card identification number</span></span>
- <span data-ttu-id="d0622-1828">card verification</span><span class="sxs-lookup"><span data-stu-id="d0622-1828">card verification</span></span> 
- <span data-ttu-id="d0622-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="d0622-1829">cardi la verifica</span></span> 
- <span data-ttu-id="d0622-1830">cid</span><span class="sxs-lookup"><span data-stu-id="d0622-1830">cid</span></span> 
- <span data-ttu-id="d0622-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="d0622-1831">cod seg</span></span> 
- <span data-ttu-id="d0622-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1832">cod seguranca</span></span> 
- <span data-ttu-id="d0622-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1833">cod segurança</span></span> 
- <span data-ttu-id="d0622-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="d0622-1834">cod sicurezza</span></span> 
- <span data-ttu-id="d0622-1835">cod.</span><span class="sxs-lookup"><span data-stu-id="d0622-1835">cod.</span></span> <span data-ttu-id="d0622-1836">seg</span><span class="sxs-lookup"><span data-stu-id="d0622-1836">seg</span></span> 
- <span data-ttu-id="d0622-1837">cod.</span><span class="sxs-lookup"><span data-stu-id="d0622-1837">cod.</span></span> <span data-ttu-id="d0622-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1838">seguranca</span></span> 
- <span data-ttu-id="d0622-1839">cod.</span><span class="sxs-lookup"><span data-stu-id="d0622-1839">cod.</span></span> <span data-ttu-id="d0622-1840">segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1840">segurança</span></span> 
- <span data-ttu-id="d0622-1841">cod.</span><span class="sxs-lookup"><span data-stu-id="d0622-1841">cod.</span></span> <span data-ttu-id="d0622-1842">sicurezza</span><span class="sxs-lookup"><span data-stu-id="d0622-1842">sicurezza</span></span> 
- <span data-ttu-id="d0622-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="d0622-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="d0622-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="d0622-1844">codice di verifica</span></span> 
- <span data-ttu-id="d0622-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="d0622-1845">codigo</span></span> 
- <span data-ttu-id="d0622-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="d0622-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1847">codigo de segurança</span></span> 
- <span data-ttu-id="d0622-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="d0622-1848">crittogramma</span></span> 
- <span data-ttu-id="d0622-1849">cryptogram</span><span class="sxs-lookup"><span data-stu-id="d0622-1849">cryptogram</span></span> 
- <span data-ttu-id="d0622-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="d0622-1850">cryptogramme</span></span> 
- <span data-ttu-id="d0622-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="d0622-1851">cv2</span></span> 
- <span data-ttu-id="d0622-1852">cvc</span><span class="sxs-lookup"><span data-stu-id="d0622-1852">cvc</span></span> 
- <span data-ttu-id="d0622-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="d0622-1853">cvc2</span></span> 
- <span data-ttu-id="d0622-1854">cvn</span><span class="sxs-lookup"><span data-stu-id="d0622-1854">cvn</span></span> 
- <span data-ttu-id="d0622-1855">cvv</span><span class="sxs-lookup"><span data-stu-id="d0622-1855">cvv</span></span> 
- <span data-ttu-id="d0622-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="d0622-1856">cvv2</span></span> 
- <span data-ttu-id="d0622-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1857">cód seguranca</span></span> 
- <span data-ttu-id="d0622-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1858">cód segurança</span></span> 
- <span data-ttu-id="d0622-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="d0622-1859">cód.</span></span> <span data-ttu-id="d0622-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1860">seguranca</span></span> 
- <span data-ttu-id="d0622-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="d0622-1861">cód.</span></span> <span data-ttu-id="d0622-1862">segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1862">segurança</span></span> 
- <span data-ttu-id="d0622-1863">código</span><span class="sxs-lookup"><span data-stu-id="d0622-1863">código</span></span> 
- <span data-ttu-id="d0622-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="d0622-1864">código de seguranca</span></span> 
- <span data-ttu-id="d0622-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="d0622-1865">código de segurança</span></span> 
- <span data-ttu-id="d0622-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="d0622-1866">de kaart controle</span></span> 
- <span data-ttu-id="d0622-1867">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="d0622-1867">geeft nr uit</span></span> 
- <span data-ttu-id="d0622-1868">issue no</span><span class="sxs-lookup"><span data-stu-id="d0622-1868">issue no</span></span> 
- <span data-ttu-id="d0622-1869">issue number</span><span class="sxs-lookup"><span data-stu-id="d0622-1869">issue number</span></span> 
- <span data-ttu-id="d0622-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="d0622-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="d0622-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="d0622-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="d0622-1873">kwestieaantal</span></span> 
- <span data-ttu-id="d0622-1874">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1874">no.</span></span> <span data-ttu-id="d0622-1875">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="d0622-1875">dell'edizione</span></span> 
- <span data-ttu-id="d0622-1876">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1876">no.</span></span> <span data-ttu-id="d0622-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="d0622-1877">di sicurezza</span></span> 
- <span data-ttu-id="d0622-1878">numero de securite</span><span class="sxs-lookup"><span data-stu-id="d0622-1878">numero de securite</span></span> 
- <span data-ttu-id="d0622-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="d0622-1879">numero de verificacao</span></span> 
- <span data-ttu-id="d0622-1880">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="d0622-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="d0622-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="d0622-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="d0622-1882">scheda</span><span class="sxs-lookup"><span data-stu-id="d0622-1882">scheda</span></span> 
- <span data-ttu-id="d0622-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="d0622-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="d0622-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="d0622-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="d0622-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="d0622-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="d0622-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d0622-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="d0622-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="d0622-1887">número de verificação</span></span> 
- <span data-ttu-id="d0622-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="d0622-1888">perno il blocco</span></span> 
- <span data-ttu-id="d0622-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="d0622-1889">pin block</span></span> 
- <span data-ttu-id="d0622-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="d0622-1890">prufziffer</span></span> 
- <span data-ttu-id="d0622-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="d0622-1891">prüfziffer</span></span> 
- <span data-ttu-id="d0622-1892">security code</span><span class="sxs-lookup"><span data-stu-id="d0622-1892">security code</span></span> 
- <span data-ttu-id="d0622-1893">security no</span><span class="sxs-lookup"><span data-stu-id="d0622-1893">security no</span></span> 
- <span data-ttu-id="d0622-1894">security number</span><span class="sxs-lookup"><span data-stu-id="d0622-1894">security number</span></span> 
- <span data-ttu-id="d0622-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="d0622-1895">sicherheits kode</span></span> 
- <span data-ttu-id="d0622-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="d0622-1896">sicherheitscode</span></span> 
- <span data-ttu-id="d0622-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="d0622-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="d0622-1898">speldblok</span></span> 
- <span data-ttu-id="d0622-1899">veiligheid 번호:</span><span class="sxs-lookup"><span data-stu-id="d0622-1899">veiligheid nr</span></span> 
- <span data-ttu-id="d0622-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="d0622-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="d0622-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="d0622-1901">veiligheidscode</span></span> 
- <span data-ttu-id="d0622-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="d0622-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="d0622-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="d0622-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="d0622-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="d0622-1905">ablauf</span><span class="sxs-lookup"><span data-stu-id="d0622-1905">ablauf</span></span> 
- <span data-ttu-id="d0622-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="d0622-1906">data de expiracao</span></span> 
- <span data-ttu-id="d0622-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="d0622-1907">data de expiração</span></span> 
- <span data-ttu-id="d0622-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="d0622-1908">data del exp</span></span> 
- <span data-ttu-id="d0622-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="d0622-1909">data di exp</span></span> 
- <span data-ttu-id="d0622-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="d0622-1910">data di scadenza</span></span> 
- <span data-ttu-id="d0622-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="d0622-1911">data em que expira</span></span> 
- <span data-ttu-id="d0622-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="d0622-1912">data scad</span></span> 
- <span data-ttu-id="d0622-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="d0622-1913">data scadenza</span></span> 
- <span data-ttu-id="d0622-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="d0622-1914">date de validité</span></span> 
- <span data-ttu-id="d0622-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="d0622-1915">datum afloop</span></span> 
- <span data-ttu-id="d0622-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="d0622-1916">datum van exp</span></span> 
- <span data-ttu-id="d0622-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="d0622-1917">de afloop</span></span> 
- <span data-ttu-id="d0622-1918">espira</span><span class="sxs-lookup"><span data-stu-id="d0622-1918">espira</span></span> 
- <span data-ttu-id="d0622-1919">espira</span><span class="sxs-lookup"><span data-stu-id="d0622-1919">espira</span></span> 
- <span data-ttu-id="d0622-1920">exp date</span><span class="sxs-lookup"><span data-stu-id="d0622-1920">exp date</span></span> 
- <span data-ttu-id="d0622-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="d0622-1921">exp datum</span></span> 
- <span data-ttu-id="d0622-1922">행사</span><span class="sxs-lookup"><span data-stu-id="d0622-1922">expiration</span></span> 
- <span data-ttu-id="d0622-1923">예정</span><span class="sxs-lookup"><span data-stu-id="d0622-1923">expire</span></span> 
- <span data-ttu-id="d0622-1924">expires</span><span class="sxs-lookup"><span data-stu-id="d0622-1924">expires</span></span> 
- <span data-ttu-id="d0622-1925">만료</span><span class="sxs-lookup"><span data-stu-id="d0622-1925">expiry</span></span> 
- <span data-ttu-id="d0622-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="d0622-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="d0622-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="d0622-1927">fecha de venc</span></span> 
- <span data-ttu-id="d0622-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="d0622-1928">gultig bis</span></span> 
- <span data-ttu-id="d0622-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="d0622-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="d0622-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="d0622-1930">gültig bis</span></span> 
- <span data-ttu-id="d0622-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="d0622-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="d0622-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="d0622-1932">la scadenza</span></span> 
- <span data-ttu-id="d0622-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="d0622-1933">scadenza</span></span> 
- <span data-ttu-id="d0622-1934">valable</span><span class="sxs-lookup"><span data-stu-id="d0622-1934">valable</span></span> 
- <span data-ttu-id="d0622-1935">유효한 ade</span><span class="sxs-lookup"><span data-stu-id="d0622-1935">validade</span></span> 
- <span data-ttu-id="d0622-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="d0622-1936">valido hasta</span></span> 
- <span data-ttu-id="d0622-1937">valor</span><span class="sxs-lookup"><span data-stu-id="d0622-1937">valor</span></span> 
- <span data-ttu-id="d0622-1938">venc</span><span class="sxs-lookup"><span data-stu-id="d0622-1938">venc</span></span> 
- <span data-ttu-id="d0622-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="d0622-1939">vencimento</span></span> 
- <span data-ttu-id="d0622-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="d0622-1940">vencimiento</span></span> 
- <span data-ttu-id="d0622-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="d0622-1941">verloopt</span></span> 
- <span data-ttu-id="d0622-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="d0622-1942">vervaldag</span></span> 
- <span data-ttu-id="d0622-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d0622-1943">vervaldatum</span></span> 
- <span data-ttu-id="d0622-1944">vto</span><span class="sxs-lookup"><span data-stu-id="d0622-1944">vto</span></span> 
- <span data-ttu-id="d0622-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="d0622-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="d0622-1946">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1946">EU Driver's License Number</span></span>

<span data-ttu-id="d0622-1947">자세한 내용은 [EU 운전 면허 번호 중요 정보 유형을](eu-driver-s-license-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d0622-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="d0622-1948">EU 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1948">EU National Identification Number</span></span>

<span data-ttu-id="d0622-1949">자세한 내용은 [EU 국가 식별 번호 중요 한 정보 유형을](eu-national-identification-number.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0622-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="d0622-1950">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1950">EU Passport Number</span></span>

<span data-ttu-id="d0622-1951">자세한 내용은 [EU Passport 번호 중요 한 정보 유형을](eu-passport-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d0622-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="d0622-1952">EU 주민 등록 번호 또는 동등한 ID</span><span class="sxs-lookup"><span data-stu-id="d0622-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="d0622-1953">자세한 내용은 [EU 주민 등록 번호 또는 동등한 ID 중요 정보 유형을](eu-social-security-number-or-equivalent-id.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d0622-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="d0622-1954">EU 세금 확인 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="d0622-1955">자세한 내용은 [EU 세금 식별 번호 중요 한 정보 유형을](eu-tax-identification-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d0622-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="d0622-1956">핀란드 국가 ID</span><span class="sxs-lookup"><span data-stu-id="d0622-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1957">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1957">Format</span></span>

<span data-ttu-id="d0622-1958">세기를 나타내는 6자리 숫자와 문자, 3자리 숫자와 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1959">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1959">Pattern</span></span>

<span data-ttu-id="d0622-1960">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="d0622-1961">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="d0622-1962">세기 표시('-', '+' 또는 'a')</span><span class="sxs-lookup"><span data-stu-id="d0622-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="d0622-1963">3자리 개인 ID 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="d0622-1964">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1965">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1965">Checksum</span></span>

<span data-ttu-id="d0622-1966">예</span><span class="sxs-lookup"><span data-stu-id="d0622-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1967">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1967">Definition</span></span>

<span data-ttu-id="d0622-1968">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1969">Func_finnish_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1970">Keyword_finnish_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="d0622-1971">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1971">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-1972">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1972">Keywords</span></span>

- <span data-ttu-id="d0622-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="d0622-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="d0622-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="d0622-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="d0622-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="d0622-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="d0622-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="d0622-1976">Personbeteckning</span></span>
- <span data-ttu-id="d0622-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="d0622-1978">핀란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1978">Finland Passport Number</span></span>

<span data-ttu-id="d0622-1979">9 개의 문자 및 숫자 패턴 조합 형식 조합: 두 문자 (대/소문자 구분 안 함) 7 자리 체크섬 정의 없음 DLP 75 정책은이 유형의 중요 한 정보를 검색 한 것으로,이에 따라 300 문자의 근사: 정규식 Regex_finland_passport_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="d0622-1980">Keyword_finland_passport_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="d0622-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="d0622-1981"></span></span>
<span data-ttu-id="d0622-1982">Passport Keyword_finland_passport_number 키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="d0622-1983">프랑스 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-1984">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-1984">Format</span></span>

<span data-ttu-id="d0622-1985">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-1986">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-1986">Pattern</span></span>

<span data-ttu-id="d0622-1987">비슷한 패턴(예: 프랑스 전화 번호)을 무시하기 위한 유효성 검사 기능을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-1988">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-1988">Checksum</span></span>

<span data-ttu-id="d0622-1989">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-1990">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-1990">Definition</span></span>

<span data-ttu-id="d0622-1991">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-1992">Func_french_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-1993">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="d0622-1994">Keyword_french_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="d0622-1995">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-1995">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-1996">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="d0622-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d0622-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="d0622-1998">drivers licence</span><span class="sxs-lookup"><span data-stu-id="d0622-1998">drivers licence</span></span>
- <span data-ttu-id="d0622-1999">drivers license</span><span class="sxs-lookup"><span data-stu-id="d0622-1999">drivers license</span></span>
- <span data-ttu-id="d0622-2000">driving licence</span><span class="sxs-lookup"><span data-stu-id="d0622-2000">driving licence</span></span>
- <span data-ttu-id="d0622-2001">driving license</span><span class="sxs-lookup"><span data-stu-id="d0622-2001">driving license</span></span>
- <span data-ttu-id="d0622-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="d0622-2002">permis de conduire</span></span>
- <span data-ttu-id="d0622-2003">licence number</span><span class="sxs-lookup"><span data-stu-id="d0622-2003">licence number</span></span>
- <span data-ttu-id="d0622-2004">license number</span><span class="sxs-lookup"><span data-stu-id="d0622-2004">license number</span></span>
- <span data-ttu-id="d0622-2005">licence numbers</span><span class="sxs-lookup"><span data-stu-id="d0622-2005">licence numbers</span></span>
- <span data-ttu-id="d0622-2006">license numbers</span><span class="sxs-lookup"><span data-stu-id="d0622-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="d0622-2007">프랑스 국가 ID 카드(CNI)</span><span class="sxs-lookup"><span data-stu-id="d0622-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2008">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2008">Format</span></span>

<span data-ttu-id="d0622-2009">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2010">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2010">Pattern</span></span>

<span data-ttu-id="d0622-2011">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2012">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2012">Checksum</span></span>

<span data-ttu-id="d0622-2013">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2014">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2014">Definition</span></span>

<span data-ttu-id="d0622-2015">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2016">Regex_france_cni 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2017">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2017">Keywords</span></span>

<span data-ttu-id="d0622-2018">없음</span><span class="sxs-lookup"><span data-stu-id="d0622-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="d0622-2019">프랑스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2020">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2020">Format</span></span>

<span data-ttu-id="d0622-2021">9자리 숫자 및 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2022">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2022">Pattern</span></span>

<span data-ttu-id="d0622-2023">9자리 숫자 및 문자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="d0622-2024">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2024">Two digits</span></span> 
- <span data-ttu-id="d0622-2025">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-2026">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2027">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2027">Checksum</span></span>

<span data-ttu-id="d0622-2028">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2029">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2029">Definition</span></span>

<span data-ttu-id="d0622-2030">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2031">Func_fr_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2032">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2032">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2033">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="d0622-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-2034">Keyword_passport</span></span>

- <span data-ttu-id="d0622-2035">Passport Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2035">Passport Number</span></span>
- <span data-ttu-id="d0622-2036">Passport No</span><span class="sxs-lookup"><span data-stu-id="d0622-2036">Passport No</span></span>
- <span data-ttu-id="d0622-2037">Passport #</span><span class="sxs-lookup"><span data-stu-id="d0622-2037">Passport #</span></span>
- <span data-ttu-id="d0622-2038">여권 #</span><span class="sxs-lookup"><span data-stu-id="d0622-2038">Passport#</span></span>
- <span data-ttu-id="d0622-2039">PassportID</span><span class="sxs-lookup"><span data-stu-id="d0622-2039">PassportID</span></span>
- <span data-ttu-id="d0622-2040">Passportno</span><span class="sxs-lookup"><span data-stu-id="d0622-2040">Passportno</span></span>
- <span data-ttu-id="d0622-2041">passportnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-2041">passportnumber</span></span>
- <span data-ttu-id="d0622-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="d0622-2042">パスポート</span></span>
- <span data-ttu-id="d0622-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2043">パスポート番号</span></span>
- <span data-ttu-id="d0622-2044">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="d0622-2044">パスポートのNum</span></span>
- <span data-ttu-id="d0622-2045">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2045">パスポート ＃</span></span> 
- <span data-ttu-id="d0622-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d0622-2046">Numéro de passeport</span></span>
- <span data-ttu-id="d0622-2047">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="d0622-2047">Passeport n °</span></span>
- <span data-ttu-id="d0622-2048">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="d0622-2048">Passeport Non</span></span>
- <span data-ttu-id="d0622-2049">Passeport #</span><span class="sxs-lookup"><span data-stu-id="d0622-2049">Passeport #</span></span>
- <span data-ttu-id="d0622-2050">포트 #</span><span class="sxs-lookup"><span data-stu-id="d0622-2050">Passeport#</span></span>
- <span data-ttu-id="d0622-2051">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="d0622-2051">PasseportNon</span></span>
- <span data-ttu-id="d0622-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="d0622-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="d0622-2053">프랑스 사회 보장 번호(INSEE)</span><span class="sxs-lookup"><span data-stu-id="d0622-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2054">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2054">Format</span></span>

<span data-ttu-id="d0622-2055">15자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2056">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2056">Pattern</span></span>

<span data-ttu-id="d0622-2057">다음 두 패턴 중 하나가 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="d0622-2058">13 자리 숫자와 공백 다음 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="d0622-2059">또는</span><span class="sxs-lookup"><span data-stu-id="d0622-2059">or</span></span>
- <span data-ttu-id="d0622-2060">15자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2061">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2061">Checksum</span></span>

<span data-ttu-id="d0622-2062">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2063">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2063">Definition</span></span>

<span data-ttu-id="d0622-2064">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2065">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2066">Keyword_fr_insee의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="d0622-2067">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2067">The checksum passes.</span></span>

<span data-ttu-id="d0622-2068">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2069">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2070">Keyword_fr_insee의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="d0622-2071">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2071">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2072">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="d0622-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="d0622-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="d0622-2074">insee</span><span class="sxs-lookup"><span data-stu-id="d0622-2074">insee</span></span>
- <span data-ttu-id="d0622-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="d0622-2075">securité sociale</span></span>
- <span data-ttu-id="d0622-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="d0622-2076">securite sociale</span></span>
- <span data-ttu-id="d0622-2077">national id</span><span class="sxs-lookup"><span data-stu-id="d0622-2077">national id</span></span>
- <span data-ttu-id="d0622-2078">national identification</span><span class="sxs-lookup"><span data-stu-id="d0622-2078">national identification</span></span>
- <span data-ttu-id="d0622-2079">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="d0622-2079">numéro d'identité</span></span>
- <span data-ttu-id="d0622-2080">no d'identité</span><span class="sxs-lookup"><span data-stu-id="d0622-2080">no d'identité</span></span>
- <span data-ttu-id="d0622-2081">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-2081">no.</span></span> <span data-ttu-id="d0622-2082">d'identité</span><span class="sxs-lookup"><span data-stu-id="d0622-2082">d'identité</span></span>
- <span data-ttu-id="d0622-2083">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="d0622-2083">numero d'identite</span></span>
- <span data-ttu-id="d0622-2084">no d'identite</span><span class="sxs-lookup"><span data-stu-id="d0622-2084">no d'identite</span></span>
- <span data-ttu-id="d0622-2085">아니요.</span><span class="sxs-lookup"><span data-stu-id="d0622-2085">no.</span></span> <span data-ttu-id="d0622-2086">d'identite</span><span class="sxs-lookup"><span data-stu-id="d0622-2086">d'identite</span></span>
- <span data-ttu-id="d0622-2087">social security number</span><span class="sxs-lookup"><span data-stu-id="d0622-2087">social security number</span></span>
- <span data-ttu-id="d0622-2088">social security code</span><span class="sxs-lookup"><span data-stu-id="d0622-2088">social security code</span></span>
- <span data-ttu-id="d0622-2089">social insurance number</span><span class="sxs-lookup"><span data-stu-id="d0622-2089">social insurance number</span></span>
- <span data-ttu-id="d0622-2090">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="d0622-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="d0622-2091">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="d0622-2091">d'identité nationale</span></span>
- <span data-ttu-id="d0622-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d0622-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="d0622-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d0622-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="d0622-2094">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="d0622-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="d0622-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="d0622-2095">numéro de sécu</span></span>
- <span data-ttu-id="d0622-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="d0622-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="d0622-2097">독일 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2098">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2098">Format</span></span>

<span data-ttu-id="d0622-2099">11자리 숫자와 문자 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2100">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2100">Pattern</span></span>

<span data-ttu-id="d0622-2101">11자리 숫자와 문자(대/소문자 구분 안 함):</span><span class="sxs-lookup"><span data-stu-id="d0622-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="d0622-2102">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-2102">A digit or letter</span></span> 
- <span data-ttu-id="d0622-2103">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2103">Two digits</span></span> 
- <span data-ttu-id="d0622-2104">6자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-2104">Six digits or letters</span></span> 
- <span data-ttu-id="d0622-2105">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2105">A digit</span></span> 
- <span data-ttu-id="d0622-2106">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2107">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2107">Checksum</span></span>

<span data-ttu-id="d0622-2108">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2109">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2109">Definition</span></span>

<span data-ttu-id="d0622-2110">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2111">Func_german_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2112">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="d0622-2113">Keyword_german_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="d0622-2114">Keyword_german_drivers_license_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="d0622-2115">Keyword_german_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="d0622-2116">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2116">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2117">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="d0622-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="d0622-2119">Führerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2119">Führerschein</span></span>
- <span data-ttu-id="d0622-2120">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2120">Fuhrerschein</span></span>
- <span data-ttu-id="d0622-2121">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2121">Fuehrerschein</span></span>
- <span data-ttu-id="d0622-2122">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="d0622-2123">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="d0622-2124">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="d0622-2125">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="d0622-2125">Führerschein-</span></span> 
- <span data-ttu-id="d0622-2126">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="d0622-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="d0622-2127">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="d0622-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="d0622-2128">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d0622-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="d0622-2129">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d0622-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="d0622-2130">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d0622-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="d0622-2131">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="d0622-2132">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="d0622-2133">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="d0622-2134">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="d0622-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="d0622-2135">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="d0622-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="d0622-2136">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="d0622-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="d0622-2137">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="d0622-2138">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="d0622-2139">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="d0622-2140">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d0622-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="d0622-2141">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d0622-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="d0622-2142">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="d0622-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="d0622-2143">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="d0622-2144">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="d0622-2145">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="d0622-2146">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="d0622-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="d0622-2147">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="d0622-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="d0622-2148">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="d0622-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="d0622-2149">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="d0622-2150">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="d0622-2151">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="d0622-2152">DL</span><span class="sxs-lookup"><span data-stu-id="d0622-2152">DL</span></span> 
- <span data-ttu-id="d0622-2153">된다</span><span class="sxs-lookup"><span data-stu-id="d0622-2153">DLS</span></span>
- <span data-ttu-id="d0622-2154">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-2154">Driv Lic</span></span> 
- <span data-ttu-id="d0622-2155">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="d0622-2155">Driv Licen</span></span> 
- <span data-ttu-id="d0622-2156">Driv License</span><span class="sxs-lookup"><span data-stu-id="d0622-2156">Driv License</span></span>
- <span data-ttu-id="d0622-2157">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-2157">Driv Licenses</span></span> 
- <span data-ttu-id="d0622-2158">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-2158">Driv Licence</span></span> 
- <span data-ttu-id="d0622-2159">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-2159">Driv Licences</span></span> 
- <span data-ttu-id="d0622-2160">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-2160">Driv Lic</span></span> 
- <span data-ttu-id="d0622-2161">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="d0622-2161">Driver Licen</span></span> 
- <span data-ttu-id="d0622-2162">Driver License</span><span class="sxs-lookup"><span data-stu-id="d0622-2162">Driver License</span></span> 
- <span data-ttu-id="d0622-2163">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-2163">Driver Licenses</span></span> 
- <span data-ttu-id="d0622-2164">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-2164">Driver Licence</span></span> 
- <span data-ttu-id="d0622-2165">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-2165">Driver Licences</span></span> 
- <span data-ttu-id="d0622-2166">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-2166">Drivers Lic</span></span> 
- <span data-ttu-id="d0622-2167">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="d0622-2167">Drivers Licen</span></span> 
- <span data-ttu-id="d0622-2168">Drivers License</span><span class="sxs-lookup"><span data-stu-id="d0622-2168">Drivers License</span></span> 
- <span data-ttu-id="d0622-2169">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="d0622-2170">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-2170">Drivers Licence</span></span> 
- <span data-ttu-id="d0622-2171">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-2171">Drivers Licences</span></span> 
- <span data-ttu-id="d0622-2172">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-2172">Driver's Lic</span></span> 
- <span data-ttu-id="d0622-2173">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="d0622-2173">Driver's Licen</span></span> 
- <span data-ttu-id="d0622-2174">Driver's License</span><span class="sxs-lookup"><span data-stu-id="d0622-2174">Driver's License</span></span> 
- <span data-ttu-id="d0622-2175">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="d0622-2176">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-2176">Driver's Licence</span></span> 
- <span data-ttu-id="d0622-2177">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-2177">Driver's Licences</span></span> 
- <span data-ttu-id="d0622-2178">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-2178">Driving Lic</span></span> 
- <span data-ttu-id="d0622-2179">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="d0622-2179">Driving Licen</span></span> 
- <span data-ttu-id="d0622-2180">Driving License</span><span class="sxs-lookup"><span data-stu-id="d0622-2180">Driving License</span></span> 
- <span data-ttu-id="d0622-2181">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-2181">Driving Licenses</span></span> 
- <span data-ttu-id="d0622-2182">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="d0622-2182">Driving Licence</span></span> 
- <span data-ttu-id="d0622-2183">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="d0622-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="d0622-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="d0622-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="d0622-2185">Veiligheid-Führerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="d0622-2186">Veiligheid-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="d0622-2187">Veiligheid-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="d0622-2188">Führerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2188">No-Führerschein</span></span> 
- <span data-ttu-id="d0622-2189">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="d0622-2190">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="d0622-2191">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2191">N-Führerschein</span></span> 
- <span data-ttu-id="d0622-2192">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="d0622-2193">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="d0622-2194">Veiligheid-Führerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="d0622-2195">Veiligheid-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="d0622-2196">Veiligheid-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="d0622-2197">Führerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2197">No-Führerschein</span></span> 
- <span data-ttu-id="d0622-2198">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="d0622-2199">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="d0622-2200">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2200">N-Führerschein</span></span> 
- <span data-ttu-id="d0622-2201">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="d0622-2202">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="d0622-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="d0622-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d0622-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="d0622-2204">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="d0622-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="d0622-2205">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="d0622-2205">ausstellungsort</span></span>
- <span data-ttu-id="d0622-2206">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="d0622-2206">ausstellende behöde</span></span>
- <span data-ttu-id="d0622-2207">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="d0622-2207">ausstellende behorde</span></span>
- <span data-ttu-id="d0622-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="d0622-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="d0622-2209">독일 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2210">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2210">Format</span></span>

<span data-ttu-id="d0622-2211">10자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2212">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2212">Pattern</span></span>

<span data-ttu-id="d0622-2213">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="d0622-2214">첫 번째 문자는 숫자 또는 (C, F, G, H, J, K) 집합의 문자임</span><span class="sxs-lookup"><span data-stu-id="d0622-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="d0622-2215">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2215">Three digits</span></span> 
- <span data-ttu-id="d0622-2216">5자리 숫자 또는 (C, -H, J-N, P, R, T, V-Z) 집합의 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="d0622-2217">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2218">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2218">Checksum</span></span>

<span data-ttu-id="d0622-2219">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2220">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2220">Definition</span></span>

<span data-ttu-id="d0622-2221">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2222">Func_german_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2223">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="d0622-2224">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2224">The checksum passes.</span></span>

<span data-ttu-id="d0622-2225">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2226">Func_german_passport_data 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2227">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="d0622-2228">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2228">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2229">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="d0622-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="d0622-2231">reisepass</span><span class="sxs-lookup"><span data-stu-id="d0622-2231">reisepass</span></span>
- <span data-ttu-id="d0622-2232">reisepasse</span><span class="sxs-lookup"><span data-stu-id="d0622-2232">reisepasse</span></span>
- <span data-ttu-id="d0622-2233">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2233">reisepassnummer</span></span>
- <span data-ttu-id="d0622-2234">여권</span><span class="sxs-lookup"><span data-stu-id="d0622-2234">passport</span></span>
- <span data-ttu-id="d0622-2235">passports</span><span class="sxs-lookup"><span data-stu-id="d0622-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="d0622-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="d0622-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="d0622-2237">ge삼 부, tsdatum</span><span class="sxs-lookup"><span data-stu-id="d0622-2237">geburtsdatum</span></span>
- <span data-ttu-id="d0622-2238">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="d0622-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="d0622-2239">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="d0622-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="d0622-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="d0622-2241">Reisepass Veiligheid-Reisepass</span><span class="sxs-lookup"><span data-stu-id="d0622-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="d0622-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="d0622-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="d0622-2243">Reisepass-Veiligheid</span><span class="sxs-lookup"><span data-stu-id="d0622-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="d0622-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="d0622-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="d0622-2245">bnationalit</span><span class="sxs-lookup"><span data-stu-id="d0622-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="d0622-2246">독일 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2247">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2247">Format</span></span>

<span data-ttu-id="d0622-2248">2010 년 11 월 1 일 이후: 9 개 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="d0622-2249">1 월 1987 년 10 월 31 일 (2010:10 자리 숫자)</span><span class="sxs-lookup"><span data-stu-id="d0622-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2250">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2250">Pattern</span></span>

<span data-ttu-id="d0622-2251">2010년 11월 1일 이후:</span><span class="sxs-lookup"><span data-stu-id="d0622-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="d0622-2252">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-2253">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2253">Eight digits</span></span>

<span data-ttu-id="d0622-2254">1 년 4 월 1987 일 ~ 10 2010 월 31 일까 지:</span><span class="sxs-lookup"><span data-stu-id="d0622-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="d0622-2255">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2256">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2256">Checksum</span></span>

<span data-ttu-id="d0622-2257">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2258">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2258">Definition</span></span>

<span data-ttu-id="d0622-2259">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2260">정규식 Regex_germany_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2261">Keyword_germany_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2262">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="d0622-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="d0622-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="d0622-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="d0622-2264">Identity Card</span></span>
- <span data-ttu-id="d0622-2265">ID</span><span class="sxs-lookup"><span data-stu-id="d0622-2265">ID</span></span>
- <span data-ttu-id="d0622-2266">확인과</span><span class="sxs-lookup"><span data-stu-id="d0622-2266">Identification</span></span>
- <span data-ttu-id="d0622-2267">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="d0622-2267">Personalausweis</span></span>
- <span data-ttu-id="d0622-2268">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="d0622-2269">Ausweis</span><span class="sxs-lookup"><span data-stu-id="d0622-2269">Ausweis</span></span>
- <span data-ttu-id="d0622-2270">Identifikation</span><span class="sxs-lookup"><span data-stu-id="d0622-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="d0622-2271">그리스 국가 ID 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2272">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2272">Format</span></span>

<span data-ttu-id="d0622-2273">7-8자리 문자 및 숫자와 대시의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2274">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2274">Pattern</span></span>

<span data-ttu-id="d0622-2275">7자리 문자 및 숫자(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="d0622-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="d0622-2276">1개 문자(그리스어 알파벳의 임의 문자) </span><span class="sxs-lookup"><span data-stu-id="d0622-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="d0622-2277">대시 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-2277">A dash</span></span> 
- <span data-ttu-id="d0622-2278">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2278">Six digits</span></span>

<span data-ttu-id="d0622-2279">8자리 문자와 숫자(새로운 형식):</span><span class="sxs-lookup"><span data-stu-id="d0622-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="d0622-2280">그리스어 및 라틴어 알파벳 둘 다에 해당 대문자가 포함된 2개 문자(ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="d0622-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="d0622-2281">대시 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-2281">A dash</span></span> 
- <span data-ttu-id="d0622-2282">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2283">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2283">Checksum</span></span>

<span data-ttu-id="d0622-2284">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2285">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2285">Definition</span></span>

<span data-ttu-id="d0622-2286">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2287">정규식 Regex_greece_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2288">Keyword_greece_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2289">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="d0622-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="d0622-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="d0622-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="d0622-2291">Greek identity Card</span></span>
- <span data-ttu-id="d0622-2292">Tautotita</span><span class="sxs-lookup"><span data-stu-id="d0622-2292">Tautotita</span></span>
- <span data-ttu-id="d0622-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="d0622-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="d0622-2294">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="d0622-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="d0622-2295">HKID(홍콩 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2296">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2296">Format</span></span>

<span data-ttu-id="d0622-2297">8-9자리 문자 및 숫자와 마지막 문자를 선택적 괄호로 묶어서 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2298">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2298">Pattern</span></span>

<span data-ttu-id="d0622-2299">8-9자리 문자 조합:</span><span class="sxs-lookup"><span data-stu-id="d0622-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="d0622-2300">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-2301">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2301">Six digits</span></span> 
- <span data-ttu-id="d0622-2302">검사 숫자에 해당하고 선택적으로 괄호로 묶는 마지막 문자(임의 숫자 또는 문자 A)</span><span class="sxs-lookup"><span data-stu-id="d0622-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2303">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2303">Checksum</span></span>

<span data-ttu-id="d0622-2304">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2305">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2305">Definition</span></span>

<span data-ttu-id="d0622-2306">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2307">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2308">Keyword_hong_kong_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="d0622-2309">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2309">The checksum passes.</span></span>

<span data-ttu-id="d0622-2310">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2311">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2312">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2312">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2313">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="d0622-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="d0622-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="d0622-2315">홍콩 특별 식별자 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2315">hong kong identity card</span></span>
- <span data-ttu-id="d0622-2316">HKIDC</span><span class="sxs-lookup"><span data-stu-id="d0622-2316">HKIDC</span></span>
- <span data-ttu-id="d0622-2317">id card</span><span class="sxs-lookup"><span data-stu-id="d0622-2317">id card</span></span>
- <span data-ttu-id="d0622-2318">identity card</span><span class="sxs-lookup"><span data-stu-id="d0622-2318">identity card</span></span>
- <span data-ttu-id="d0622-2319">zh-hk id 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2319">hk identity card</span></span>
- <span data-ttu-id="d0622-2320">홍콩 id</span><span class="sxs-lookup"><span data-stu-id="d0622-2320">hong kong id</span></span>
- <span data-ttu-id="d0622-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2321">香港身份證</span></span>
- <span data-ttu-id="d0622-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="d0622-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2323">身份證</span></span>
- <span data-ttu-id="d0622-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="d0622-2324">身份証</span></span>
- <span data-ttu-id="d0622-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-2325">身分證</span></span>
- <span data-ttu-id="d0622-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="d0622-2326">身分証</span></span>
- <span data-ttu-id="d0622-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="d0622-2327">香港身份証</span></span>
- <span data-ttu-id="d0622-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-2328">香港身分證</span></span>
- <span data-ttu-id="d0622-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="d0622-2329">香港身分証</span></span>
- <span data-ttu-id="d0622-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2330">香港身份證</span></span>
- <span data-ttu-id="d0622-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2331">香港居民身份證</span></span>
- <span data-ttu-id="d0622-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="d0622-2332">香港居民身份証</span></span>
- <span data-ttu-id="d0622-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-2333">香港居民身分證</span></span>
- <span data-ttu-id="d0622-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="d0622-2334">香港居民身分証</span></span>
- <span data-ttu-id="d0622-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="d0622-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="d0622-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="d0622-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="d0622-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="d0622-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="d0622-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="d0622-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="d0622-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="d0622-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="d0622-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="d0622-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="d0622-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="d0622-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="d0622-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="d0622-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="d0622-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="d0622-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="d0622-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="d0622-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="d0622-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="d0622-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="d0622-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="d0622-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="d0622-2351">인도 PAN(영구 계정 번호)</span><span class="sxs-lookup"><span data-stu-id="d0622-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2352">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2352">Format</span></span>

<span data-ttu-id="d0622-2353">10자리 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2354">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2354">Pattern</span></span>

<span data-ttu-id="d0622-2355">10자리 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2355">10 letters or digits:</span></span>
- <span data-ttu-id="d0622-2356">5개 문자(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="d0622-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-2357">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2357">Four digits</span></span> 
- <span data-ttu-id="d0622-2358">알파벳 검사 숫자에 해당하는 문자 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2359">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2359">Checksum</span></span>

<span data-ttu-id="d0622-2360">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2361">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2361">Definition</span></span>

<span data-ttu-id="d0622-2362">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2363">정규식 Regex_india_permanent_account_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2364">Keyword_india_permanent_account_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="d0622-2365">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2365">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2366">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="d0622-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="d0622-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="d0622-2369">확대</span><span class="sxs-lookup"><span data-stu-id="d0622-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="d0622-2370">인도 고유 ID(Aadhaar) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2371">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2371">Format</span></span>

<span data-ttu-id="d0622-2372">선택적 공백 또는 대시를 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2373">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2373">Pattern</span></span>

<span data-ttu-id="d0622-2374">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2374">12 digits:</span></span>
- <span data-ttu-id="d0622-2375">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2375">Four digits</span></span> 
- <span data-ttu-id="d0622-2376">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="d0622-2376">An optional space or dash</span></span> 
- <span data-ttu-id="d0622-2377">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2377">Four digits</span></span> 
- <span data-ttu-id="d0622-2378">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="d0622-2378">An optional space or dash</span></span> 
- <span data-ttu-id="d0622-2379">검사 숫자에 해당하는 마지막 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2380">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2380">Checksum</span></span>

<span data-ttu-id="d0622-2381">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2382">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2382">Definition</span></span>

<span data-ttu-id="d0622-2383">DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="d0622-2384">Keyword_india_aadhar에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="d0622-2385">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2385">The checksum passes.</span></span>
<span data-ttu-id="d0622-2386">DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="d0622-2387">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2387">The checksum passes.</span></span>
<!-- India Unique Identification (Aadhaar) number -->
<span data-ttu-id="d0622-2388"><Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="d0622-2388"></span></span>

### <a name="keywords"></a><span data-ttu-id="d0622-2389">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2389">Keywords</span></span>
   
#### <a name="keyword_india_aadhar"></a><span data-ttu-id="d0622-2390">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="d0622-2390">Keyword_india_aadhar</span></span>
- <span data-ttu-id="d0622-2391">Aadhar</span><span class="sxs-lookup"><span data-stu-id="d0622-2391">Aadhar</span></span>
- <span data-ttu-id="d0622-2392">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="d0622-2392">Aadhaar</span></span>
- <span data-ttu-id="d0622-2393">UID</span><span class="sxs-lookup"><span data-stu-id="d0622-2393">UID</span></span>
- <span data-ttu-id="d0622-2394">आधार</span><span class="sxs-lookup"><span data-stu-id="d0622-2394">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="d0622-2395">인도네시아 ID 카드(KTP) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2395">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2396">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2396">Format</span></span>

<span data-ttu-id="d0622-2397">선택적으로 마침표를 포함하는 16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2397">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2398">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2398">Pattern</span></span>

<span data-ttu-id="d0622-2399">16자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2399">16 digits:</span></span>
- <span data-ttu-id="d0622-2400">2자리 시/도 코드 </span><span class="sxs-lookup"><span data-stu-id="d0622-2400">Two-digit province code</span></span> 
- <span data-ttu-id="d0622-2401">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="d0622-2401">A period (optional)</span></span> 
- <span data-ttu-id="d0622-2402">2자리 지역 또는 구/군/시 코드 </span><span class="sxs-lookup"><span data-stu-id="d0622-2402">Two-digit regency or city code</span></span> 
- <span data-ttu-id="d0622-2403">2자리 소구역 코드 </span><span class="sxs-lookup"><span data-stu-id="d0622-2403">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="d0622-2404">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="d0622-2404">A period (optional)</span></span> 
- <span data-ttu-id="d0622-2405">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-2405">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="d0622-2406">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="d0622-2406">A period (optional)</span></span> 
- <span data-ttu-id="d0622-2407">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2407">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2408">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2408">Checksum</span></span>

<span data-ttu-id="d0622-2409">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2409">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2410">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2410">Definition</span></span>

<span data-ttu-id="d0622-2411">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2412">정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2412">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2413">Keyword_indonesia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2413">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="d0622-2414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2415">정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2415">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2416">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2416">Keywords</span></span>
   
#### <a name="keyword_indonesia_id_card"></a><span data-ttu-id="d0622-2417">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="d0622-2417">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="d0622-2418">KTP</span><span class="sxs-lookup"><span data-stu-id="d0622-2418">KTP</span></span>
- <span data-ttu-id="d0622-2419">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="d0622-2419">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="d0622-2420">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="d0622-2420">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="d0622-2421">IBAN(국제 은행 계좌 번호)</span><span class="sxs-lookup"><span data-stu-id="d0622-2421">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2422">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2422">Format</span></span>

<span data-ttu-id="d0622-2423">국가 코드 (두 문자) + 검사 숫자 (2 자리 숫자)와 bban 숫자 (최대 30 자)</span><span class="sxs-lookup"><span data-stu-id="d0622-2423">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2424">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2424">Pattern</span></span>

<span data-ttu-id="d0622-2425">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2425">Pattern must include all of the following:</span></span>

- <span data-ttu-id="d0622-2426">두 글자로 된 국가 코드</span><span class="sxs-lookup"><span data-stu-id="d0622-2426">Two-letter country code</span></span>
- <span data-ttu-id="d0622-2427">두 개의 검사 숫자 (선택적 공백)</span><span class="sxs-lookup"><span data-stu-id="d0622-2427">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="d0622-2428">1-7 개 문자 또는 숫자의 그룹 (공백으로 구분 가능)</span><span class="sxs-lookup"><span data-stu-id="d0622-2428">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="d0622-2429">1-3 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2429">1-3 letters or digits</span></span>

<span data-ttu-id="d0622-2430">각 국가의 형식은 약간 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2430">The format for each country is slightly different.</span></span> <span data-ttu-id="d0622-2431">IBAN 중요 한 정보 유형은 다음과 같은 60 국가를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2431">The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="d0622-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, kw, hu,, to,,, fr,,, i,,, ie, il, is,, l,, 5, 60, md, me, mk, e, mt, mu , nl-nl, no, pl, pt, ro, rs, sa, se, si,, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="d0622-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2433">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2433">Checksum</span></span>

<span data-ttu-id="d0622-2434">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2435">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2435">Definition</span></span>

<span data-ttu-id="d0622-2436">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2437">Func_iban 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2437">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2438">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2438">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2439">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2439">Keywords</span></span>

<span data-ttu-id="d0622-2440">없음</span><span class="sxs-lookup"><span data-stu-id="d0622-2440">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="d0622-2441">IP 주소</span><span class="sxs-lookup"><span data-stu-id="d0622-2441">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2442">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2442">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="d0622-2443">IPv4</span><span class="sxs-lookup"><span data-stu-id="d0622-2443">IPv4:</span></span>
<span data-ttu-id="d0622-2444">IPv4 주소의 서식 있는 버전(마침표 있음) 및 서식 없는 버전(마침표 없음)으로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2444">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="d0622-2445">IPv6</span><span class="sxs-lookup"><span data-stu-id="d0622-2445">IPv6:</span></span>
<span data-ttu-id="d0622-2446">서식 있는(콜론 포함) IPv6 번호로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2446">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2447">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2447">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2448">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2448">Checksum</span></span>

<span data-ttu-id="d0622-2449">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2449">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2450">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2450">Definition</span></span>

<span data-ttu-id="d0622-2451">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2451">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2452">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2452">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2453">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2453">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="d0622-2454">IPv4의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2454">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2455">Regex_ipv4_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2455">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2456">Keyword_ipaddress의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2456">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="d0622-2457">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2457">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2458">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2458">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2459">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2459">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2460">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2460">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="d0622-2461">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="d0622-2461">Keyword_ipaddress</span></span>

- <span data-ttu-id="d0622-2462">IP(이 키워드는 대/소문자를 구분함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2462">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="d0622-2463">ip address</span><span class="sxs-lookup"><span data-stu-id="d0622-2463">ip address</span></span> 
- <span data-ttu-id="d0622-2464">ip addresses</span><span class="sxs-lookup"><span data-stu-id="d0622-2464">ip addresses</span></span>
- <span data-ttu-id="d0622-2465">internet protocol</span><span class="sxs-lookup"><span data-stu-id="d0622-2465">internet protocol</span></span>
- <span data-ttu-id="d0622-2466">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="d0622-2466">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="d0622-2467">Diseases의 국제 분류 (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="d0622-2467">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2468">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2468">Format</span></span>

<span data-ttu-id="d0622-2469">사전</span><span class="sxs-lookup"><span data-stu-id="d0622-2469">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2470">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2470">Pattern</span></span>

<span data-ttu-id="d0622-2471">Keyword</span><span class="sxs-lookup"><span data-stu-id="d0622-2471">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2472">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2472">Checksum</span></span>

<span data-ttu-id="d0622-2473">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2474">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2474">Definition</span></span>

<span data-ttu-id="d0622-2475">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2476">Dictionary_icd_10_cm에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2476">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="d0622-2477">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2477">Keywords</span></span>

<span data-ttu-id="d0622-2478">Dictionary_icd_10_cm 키워드 사전의 모든 용어 이며, [Diseases의 국제 분류, 10 번째 수정, 임상 수정 (icd-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604)을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2478">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="d0622-2479">이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2479">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="d0622-2480">Diseases의 국제 분류 (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="d0622-2480">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2481">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2481">Format</span></span>

<span data-ttu-id="d0622-2482">사전</span><span class="sxs-lookup"><span data-stu-id="d0622-2482">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2483">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2483">Pattern</span></span>

<span data-ttu-id="d0622-2484">Keyword</span><span class="sxs-lookup"><span data-stu-id="d0622-2484">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2485">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2485">Checksum</span></span>

<span data-ttu-id="d0622-2486">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2486">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2487">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2487">Definition</span></span>

<span data-ttu-id="d0622-2488">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2488">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2489">Dictionary_icd_9_cm에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2489">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2490">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2490">Keywords</span></span>

<span data-ttu-id="d0622-2491">[Diseases의 국가별 분류, 9 번째 버전의 임상 수정 (icd-9CM)](https://go.microsoft.com/fwlink/?linkid=852605)을 기반으로 하는 Dictionary_icd_9_cm 키워드 사전의 모든 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2491">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="d0622-2492">이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2492">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="d0622-2493">아일랜드 PPS(개인 공공 서비스) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2493">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2494">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2494">Format</span></span>

<span data-ttu-id="d0622-2495">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="d0622-2495">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="d0622-2496">7자리 숫자와 1-2개 문자 </span><span class="sxs-lookup"><span data-stu-id="d0622-2496">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="d0622-2497">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="d0622-2497">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="d0622-2498">7자리 숫자와 2개 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-2498">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2499">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2499">Pattern</span></span>

<span data-ttu-id="d0622-2500">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="d0622-2500">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="d0622-2501">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2501">Seven digits</span></span> 
- <span data-ttu-id="d0622-2502">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2502">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="d0622-2503">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="d0622-2503">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="d0622-2504">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2504">Seven digits</span></span> 
- <span data-ttu-id="d0622-2505">알파벳 검사 숫자에 해당하는 문자 1개(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="d0622-2505">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="d0622-2506">문자 "A" 또는 "H"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2506">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2507">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2507">Checksum</span></span>

<span data-ttu-id="d0622-2508">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2508">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2509">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2509">Definition</span></span>

<span data-ttu-id="d0622-2510">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2511">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2511">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2512">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2512">One of the following is true:</span></span>
    - <span data-ttu-id="d0622-2513">Keyword_ireland_pps에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2513">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="d0622-2514">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2514">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="d0622-2515">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2515">The checksum passes.</span></span>

<span data-ttu-id="d0622-2516">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2516">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2517">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2517">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2518">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2518">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2519">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2519">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="d0622-2520">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="d0622-2520">Keyword_ireland_pps</span></span>

- <span data-ttu-id="d0622-2521">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2521">Personal Public Service Number</span></span> 
- <span data-ttu-id="d0622-2522">PPS Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2522">PPS Number</span></span> 
- <span data-ttu-id="d0622-2523">PPS Num</span><span class="sxs-lookup"><span data-stu-id="d0622-2523">PPS Num</span></span> 
- <span data-ttu-id="d0622-2524">PPS No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2524">PPS No.</span></span> 
- <span data-ttu-id="d0622-2525">PPS #</span><span class="sxs-lookup"><span data-stu-id="d0622-2525">PPS #</span></span> 
- <span data-ttu-id="d0622-2526">.PPS #</span><span class="sxs-lookup"><span data-stu-id="d0622-2526">PPS#</span></span> 
- <span data-ttu-id="d0622-2527">PPSN</span><span class="sxs-lookup"><span data-stu-id="d0622-2527">PPSN</span></span> 
- <span data-ttu-id="d0622-2528">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="d0622-2528">Public Services Card</span></span> 
- <span data-ttu-id="d0622-2529">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="d0622-2529">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="d0622-2530">Uimh</span><span class="sxs-lookup"><span data-stu-id="d0622-2530">Uimh.</span></span> <span data-ttu-id="d0622-2531">PSP</span><span class="sxs-lookup"><span data-stu-id="d0622-2531">PSP</span></span> 
- <span data-ttu-id="d0622-2532">PSP</span><span class="sxs-lookup"><span data-stu-id="d0622-2532">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="d0622-2533">이스라엘 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2533">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2534">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2534">Format</span></span>

<span data-ttu-id="d0622-2535">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2535">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2536">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2536">Pattern</span></span>

<span data-ttu-id="d0622-2537">서식이</span><span class="sxs-lookup"><span data-stu-id="d0622-2537">Formatted:</span></span>
- <span data-ttu-id="d0622-2538">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2538">Two digits</span></span> 
- <span data-ttu-id="d0622-2539">대시 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-2539">A dash</span></span> 
- <span data-ttu-id="d0622-2540">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2540">Three digits</span></span> 
- <span data-ttu-id="d0622-2541">대시 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-2541">A dash</span></span> 
- <span data-ttu-id="d0622-2542">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2542">Eight digits</span></span>

<span data-ttu-id="d0622-2543">서식</span><span class="sxs-lookup"><span data-stu-id="d0622-2543">Unformatted:</span></span>
- <span data-ttu-id="d0622-2544">13자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2544">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2545">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2545">Checksum</span></span>

<span data-ttu-id="d0622-2546">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2546">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2547">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2547">Definition</span></span>

<span data-ttu-id="d0622-2548">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2548">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2549">Regex_israel_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2549">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2550">Keyword_israel_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2550">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2551">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2551">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="d0622-2552">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2552">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="d0622-2553">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2553">Bank Account Number</span></span> 
- <span data-ttu-id="d0622-2554">Bank Account</span><span class="sxs-lookup"><span data-stu-id="d0622-2554">Bank Account</span></span> 
- <span data-ttu-id="d0622-2555">Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2555">Account Number</span></span> 
- <span data-ttu-id="d0622-2556">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="d0622-2556">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="d0622-2557">이스라엘 국가 ID</span><span class="sxs-lookup"><span data-stu-id="d0622-2557">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2558">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2558">Format</span></span>

<span data-ttu-id="d0622-2559">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2559">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2560">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2560">Pattern</span></span>

<span data-ttu-id="d0622-2561">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2561">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2562">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2562">Checksum</span></span>

<span data-ttu-id="d0622-2563">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2563">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2564">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2564">Definition</span></span>

<span data-ttu-id="d0622-2565">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2565">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2566">Func_israeli_national_id_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2566">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2567">Keyword_Israel_National_ID의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2567">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="d0622-2568">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2568">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2569">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2569">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="d0622-2570">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="d0622-2570">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="d0622-2571">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="d0622-2571">מספר זהות</span></span> 
- <span data-ttu-id="d0622-2572">National ID Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2572">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="d0622-2573">이탈리아 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2573">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2574">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2574">Format</span></span>

<span data-ttu-id="d0622-2575">10개의 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-2575">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2576">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2576">Pattern</span></span>

- <span data-ttu-id="d0622-2577">10개의 문자 및 숫자 조합:</span><span class="sxs-lookup"><span data-stu-id="d0622-2577">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="d0622-2578">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2578">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-2579">문자 "A" 또는 "V"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2579">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-2580">7개 문자(대/소문자 구분 안 함), 숫자 또는 밑줄 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-2580">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="d0622-2581">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2581">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2582">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2582">Checksum</span></span>

<span data-ttu-id="d0622-2583">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2583">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2584">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2584">Definition</span></span>

<span data-ttu-id="d0622-2585">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2586">Regex_italy_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2586">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2587">Keyword_italy_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2587">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2588">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2588">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="d0622-2589">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2589">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="d0622-2590">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="d0622-2590">numero di patente di guida</span></span> 
- <span data-ttu-id="d0622-2591">patente di guida</span><span class="sxs-lookup"><span data-stu-id="d0622-2591">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="d0622-2592">일본 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2592">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2593">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2593">Format</span></span>

<span data-ttu-id="d0622-2594">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2594">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2595">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2595">Pattern</span></span>

<span data-ttu-id="d0622-2596">은행 계좌 번호:</span><span class="sxs-lookup"><span data-stu-id="d0622-2596">Bank account number:</span></span>
- <span data-ttu-id="d0622-2597">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2597">Seven or eight digits</span></span>
- <span data-ttu-id="d0622-2598">은행 계좌 지점 코드:</span><span class="sxs-lookup"><span data-stu-id="d0622-2598">Bank account branch code:</span></span>
- <span data-ttu-id="d0622-2599">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2599">Four digits</span></span> 
- <span data-ttu-id="d0622-2600">공백 또는 대시(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="d0622-2600">A space or dash (optional)</span></span> 
- <span data-ttu-id="d0622-2601">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2601">Three digits</span></span>

<span data-ttu-id="d0622-2602">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2602">Checksum</span></span>

<span data-ttu-id="d0622-2603">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2603">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2604">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2604">Definition</span></span>

<span data-ttu-id="d0622-2605">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2605">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2606">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2606">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2607">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2607">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="d0622-2608">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2608">One of the following is true:</span></span>
- <span data-ttu-id="d0622-2609">Func_jp_bank_account_branch_code 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2609">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2610">Keyword_jp_bank_branch_code의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2610">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="d0622-2611">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2611">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2612">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2612">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2613">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2613">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2614">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2614">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="d0622-2615">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="d0622-2615">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="d0622-2616">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2616">Checking Account Number</span></span> 
- <span data-ttu-id="d0622-2617">Checking Account</span><span class="sxs-lookup"><span data-stu-id="d0622-2617">Checking Account</span></span> 
- <span data-ttu-id="d0622-2618">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="d0622-2618">Checking Account #</span></span> 
- <span data-ttu-id="d0622-2619">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2619">Checking Acct Number</span></span> 
- <span data-ttu-id="d0622-2620">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="d0622-2620">Checking Acct #</span></span> 
- <span data-ttu-id="d0622-2621">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2621">Checking Acct No.</span></span> 
- <span data-ttu-id="d0622-2622">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2622">Checking Account No.</span></span> 
- <span data-ttu-id="d0622-2623">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2623">Bank Account Number</span></span> 
- <span data-ttu-id="d0622-2624">Bank Account</span><span class="sxs-lookup"><span data-stu-id="d0622-2624">Bank Account</span></span> 
- <span data-ttu-id="d0622-2625">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="d0622-2625">Bank Account #</span></span> 
- <span data-ttu-id="d0622-2626">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2626">Bank Acct Number</span></span> 
- <span data-ttu-id="d0622-2627">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="d0622-2627">Bank Acct #</span></span> 
- <span data-ttu-id="d0622-2628">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2628">Bank Acct No.</span></span> 
- <span data-ttu-id="d0622-2629">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2629">Bank Account No.</span></span> 
- <span data-ttu-id="d0622-2630">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2630">Savings Account Number</span></span> 
- <span data-ttu-id="d0622-2631">Savings Account</span><span class="sxs-lookup"><span data-stu-id="d0622-2631">Savings Account</span></span> 
- <span data-ttu-id="d0622-2632">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="d0622-2632">Savings Account #</span></span> 
- <span data-ttu-id="d0622-2633">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2633">Savings Acct Number</span></span> 
- <span data-ttu-id="d0622-2634">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="d0622-2634">Savings Acct #</span></span> 
- <span data-ttu-id="d0622-2635">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2635">Savings Acct No.</span></span> 
- <span data-ttu-id="d0622-2636">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2636">Savings Account No.</span></span> 
- <span data-ttu-id="d0622-2637">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2637">Debit Account Number</span></span> 
- <span data-ttu-id="d0622-2638">Debit Account</span><span class="sxs-lookup"><span data-stu-id="d0622-2638">Debit Account</span></span> 
- <span data-ttu-id="d0622-2639">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="d0622-2639">Debit Account #</span></span> 
- <span data-ttu-id="d0622-2640">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2640">Debit Acct Number</span></span> 
- <span data-ttu-id="d0622-2641">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="d0622-2641">Debit Acct #</span></span> 
- <span data-ttu-id="d0622-2642">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2642">Debit Acct No.</span></span> 
- <span data-ttu-id="d0622-2643">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2643">Debit Account No.</span></span> 
- <span data-ttu-id="d0622-2644">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="d0622-2644">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="d0622-2645">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="d0622-2645">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="d0622-2646">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="d0622-2646">＃勘定の確認</span></span> 
- <span data-ttu-id="d0622-2647">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="d0622-2647">勘定番号の確認</span></span> 
- <span data-ttu-id="d0622-2648">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="d0622-2648">口座番号の確認</span></span> 
- <span data-ttu-id="d0622-2649">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2649">銀行口座番号</span></span> 
- <span data-ttu-id="d0622-2650">銀行口座</span><span class="sxs-lookup"><span data-stu-id="d0622-2650">銀行口座</span></span> 
- <span data-ttu-id="d0622-2651">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2651">銀行口座＃</span></span> 
- <span data-ttu-id="d0622-2652">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2652">銀行の勘定番号</span></span> 
- <span data-ttu-id="d0622-2653">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2653">銀行のacct＃</span></span> 
- <span data-ttu-id="d0622-2654">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="d0622-2654">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="d0622-2655">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2655">銀行口座番号</span></span>
- <span data-ttu-id="d0622-2656">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2656">普通預金口座番号</span></span> 
- <span data-ttu-id="d0622-2657">預金口座</span><span class="sxs-lookup"><span data-stu-id="d0622-2657">預金口座</span></span> 
- <span data-ttu-id="d0622-2658">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2658">貯蓄口座＃</span></span> 
- <span data-ttu-id="d0622-2659">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="d0622-2659">貯蓄勘定の数</span></span> 
- <span data-ttu-id="d0622-2660">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2660">貯蓄勘定＃</span></span> 
- <span data-ttu-id="d0622-2661">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2661">貯蓄勘定番号</span></span> 
- <span data-ttu-id="d0622-2662">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2662">普通預金口座番号</span></span> 
- <span data-ttu-id="d0622-2663">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2663">引き落とし口座番号</span></span> 
- <span data-ttu-id="d0622-2664">口座番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2664">口座番号</span></span> 
- <span data-ttu-id="d0622-2665">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2665">口座番号＃</span></span> 
- <span data-ttu-id="d0622-2666">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2666">デビットのacct番号</span></span> 
- <span data-ttu-id="d0622-2667">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2667">デビット勘定＃</span></span> 
- <span data-ttu-id="d0622-2668">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2668">デビットACCTの番号</span></span> 
- <span data-ttu-id="d0622-2669">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2669">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="d0622-2670">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="d0622-2670">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="d0622-2671">Otemachi</span><span class="sxs-lookup"><span data-stu-id="d0622-2671">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="d0622-2672">일본 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2672">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2673">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2673">Format</span></span>

<span data-ttu-id="d0622-2674">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2674">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2675">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2675">Pattern</span></span>

<span data-ttu-id="d0622-2676">12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2676">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2677">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2677">Checksum</span></span>

<span data-ttu-id="d0622-2678">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2678">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2679">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2679">Definition</span></span>

<span data-ttu-id="d0622-2680">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2681">Func_jp_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2681">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2682">Keyword_jp_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2682">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2683">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2683">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="d0622-2684">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2684">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="d0622-2685">dl #</span><span class="sxs-lookup"><span data-stu-id="d0622-2685">dl#</span></span> 
- <span data-ttu-id="d0622-2686">DL</span><span class="sxs-lookup"><span data-stu-id="d0622-2686">DL＃</span></span> 
- <span data-ttu-id="d0622-2687">된다 #</span><span class="sxs-lookup"><span data-stu-id="d0622-2687">dls#</span></span> 
- <span data-ttu-id="d0622-2688">된다</span><span class="sxs-lookup"><span data-stu-id="d0622-2688">DLS＃</span></span> 
- <span data-ttu-id="d0622-2689">driver license</span><span class="sxs-lookup"><span data-stu-id="d0622-2689">driver license</span></span> 
- <span data-ttu-id="d0622-2690">driver licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-2690">driver licenses</span></span> 
- <span data-ttu-id="d0622-2691">drivers license</span><span class="sxs-lookup"><span data-stu-id="d0622-2691">drivers license</span></span> 
- <span data-ttu-id="d0622-2692">driver's license</span><span class="sxs-lookup"><span data-stu-id="d0622-2692">driver's license</span></span> 
- <span data-ttu-id="d0622-2693">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-2693">drivers licenses</span></span> 
- <span data-ttu-id="d0622-2694">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-2694">driver's licenses</span></span> 
- <span data-ttu-id="d0622-2695">driving licence</span><span class="sxs-lookup"><span data-stu-id="d0622-2695">driving licence</span></span> 
- <span data-ttu-id="d0622-2696">lic #</span><span class="sxs-lookup"><span data-stu-id="d0622-2696">lic#</span></span> 
- <span data-ttu-id="d0622-2697">LIC</span><span class="sxs-lookup"><span data-stu-id="d0622-2697">LIC＃</span></span> 
- <span data-ttu-id="d0622-2698">driver'lics #</span><span class="sxs-lookup"><span data-stu-id="d0622-2698">lics#</span></span> 
- <span data-ttu-id="d0622-2699">state id</span><span class="sxs-lookup"><span data-stu-id="d0622-2699">state id</span></span> 
- <span data-ttu-id="d0622-2700">state identification</span><span class="sxs-lookup"><span data-stu-id="d0622-2700">state identification</span></span> 
- <span data-ttu-id="d0622-2701">state identification number</span><span class="sxs-lookup"><span data-stu-id="d0622-2701">state identification number</span></span> 
- <span data-ttu-id="d0622-2702">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2702">低所得国＃</span></span> 
- <span data-ttu-id="d0622-2703">免許証</span><span class="sxs-lookup"><span data-stu-id="d0622-2703">免許証</span></span> 
- <span data-ttu-id="d0622-2704">状態ID</span><span class="sxs-lookup"><span data-stu-id="d0622-2704">状態ID</span></span>
- <span data-ttu-id="d0622-2705">状態の識別</span><span class="sxs-lookup"><span data-stu-id="d0622-2705">状態の識別</span></span> 
- <span data-ttu-id="d0622-2706">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2706">状態の識別番号</span></span> 
- <span data-ttu-id="d0622-2707">運転免許</span><span class="sxs-lookup"><span data-stu-id="d0622-2707">運転免許</span></span> 
- <span data-ttu-id="d0622-2708">運転免許証</span><span class="sxs-lookup"><span data-stu-id="d0622-2708">運転免許証</span></span> 
- <span data-ttu-id="d0622-2709">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2709">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="d0622-2710">일본 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2710">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2711">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2711">Format</span></span>

<span data-ttu-id="d0622-2712">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2712">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2713">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2713">Pattern</span></span>

<span data-ttu-id="d0622-2714">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2714">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2715">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2715">Checksum</span></span>

<span data-ttu-id="d0622-2716">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2716">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2717">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2717">Definition</span></span>

<span data-ttu-id="d0622-2718">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2718">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2719">Func_jp_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2719">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2720">Keyword_jp_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2720">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2721">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2721">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="d0622-2722">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-2722">Keyword_jp_passport</span></span>

- <span data-ttu-id="d0622-2723">パスポート</span><span class="sxs-lookup"><span data-stu-id="d0622-2723">パスポート</span></span> 
- <span data-ttu-id="d0622-2724">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2724">パスポート番号</span></span> 
- <span data-ttu-id="d0622-2725">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="d0622-2725">パスポートのNum</span></span> 
- <span data-ttu-id="d0622-2726">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="d0622-2726">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="d0622-2727">일본 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2727">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2728">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2728">Format</span></span>

<span data-ttu-id="d0622-2729">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2729">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2730">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2730">Pattern</span></span>

<span data-ttu-id="d0622-2731">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2731">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2732">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2732">Checksum</span></span>

<span data-ttu-id="d0622-2733">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2733">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2734">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2734">Definition</span></span>

<span data-ttu-id="d0622-2735">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2736">Func_jp_resident_registration_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2736">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2737">Keyword_jp_resident_registration_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2737">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2738">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2738">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="d0622-2739">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2739">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="d0622-2740">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2740">Resident Registration Number</span></span>
- <span data-ttu-id="d0622-2741">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2741">Resident Register Number</span></span> 
- <span data-ttu-id="d0622-2742">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2742">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="d0622-2743">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2743">Resident Registration No.</span></span> 
- <span data-ttu-id="d0622-2744">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2744">Resident Register No.</span></span> 
- <span data-ttu-id="d0622-2745">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2745">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="d0622-2746">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2746">Basic Resident Register No.</span></span> 
- <span data-ttu-id="d0622-2747">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="d0622-2747">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="d0622-2748">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2748">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="d0622-2749">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="d0622-2749">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="d0622-2750">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2750">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="d0622-2751">일본 SIN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="d0622-2751">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2752">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2752">Format</span></span>

<span data-ttu-id="d0622-2753">7-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2753">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2754">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2754">Pattern</span></span>

<span data-ttu-id="d0622-2755">7-12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2755">7-12 digits:</span></span>
- <span data-ttu-id="d0622-2756">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2756">Four digits</span></span> 
- <span data-ttu-id="d0622-2757">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="d0622-2757">A hyphen (optional)</span></span> 
- <span data-ttu-id="d0622-2758">6 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="d0622-2758">Six digits OR</span></span>
- <span data-ttu-id="d0622-2759">7-12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2759">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2760">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2760">Checksum</span></span>

<span data-ttu-id="d0622-2761">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2761">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2762">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2762">Definition</span></span>

<span data-ttu-id="d0622-2763">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2763">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2764">Func_jp_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2764">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2765">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2765">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="d0622-2766">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2766">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2767">Func_jp_sin_pre_1997 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2767">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2768">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2768">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2769">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2769">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="d0622-2770">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="d0622-2770">Keyword_jp_sin</span></span>

- <span data-ttu-id="d0622-2771">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="d0622-2771">Social Insurance No.</span></span> 
- <span data-ttu-id="d0622-2772">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="d0622-2772">Social Insurance Num</span></span> 
- <span data-ttu-id="d0622-2773">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2773">Social Insurance Number</span></span> 
- <span data-ttu-id="d0622-2774">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="d0622-2774">社会保険のテンキー</span></span> 
- <span data-ttu-id="d0622-2775">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2775">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="d0622-2776">일본어 거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2776">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2777">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2777">Format</span></span>

<span data-ttu-id="d0622-2778">12 개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2778">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2779">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2779">Pattern</span></span>

<span data-ttu-id="d0622-2780">12 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2780">12 letters and digits:</span></span>
- <span data-ttu-id="d0622-2781">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2781">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="d0622-2782">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2782">Eight digits</span></span> 
- <span data-ttu-id="d0622-2783">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-2783">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2784">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2784">Checksum</span></span>

<span data-ttu-id="d0622-2785">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2785">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2786">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2786">Definition</span></span>

<span data-ttu-id="d0622-2787">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2788">정규식 Regex_jp_residence_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2788">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2789">Keyword_jp_residence_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2789">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2790">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2790">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="d0622-2791">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2791">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="d0622-2792">거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2792">Residence card number</span></span>
- <span data-ttu-id="d0622-2793">거주지 카드 아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2793">Residence card no</span></span>
- <span data-ttu-id="d0622-2794">거주지 카드 #</span><span class="sxs-lookup"><span data-stu-id="d0622-2794">Residence card #</span></span>
- <span data-ttu-id="d0622-2795">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="d0622-2795">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="d0622-2796">말레이시아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2796">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2797">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2797">Format</span></span>

<span data-ttu-id="d0622-2798">선택적으로 하이픈을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2798">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2799">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2799">Pattern</span></span>

<span data-ttu-id="d0622-2800">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2800">12 digits:</span></span>
- <span data-ttu-id="d0622-2801">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-2801">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="d0622-2802">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="d0622-2802">A dash (optional)</span></span> 
- <span data-ttu-id="d0622-2803">2개 문자로 이루어진 출생지 코드 </span><span class="sxs-lookup"><span data-stu-id="d0622-2803">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="d0622-2804">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="d0622-2804">A dash (optional)</span></span> 
- <span data-ttu-id="d0622-2805">임의의 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-2805">Three random digits</span></span> 
- <span data-ttu-id="d0622-2806">1자리 성별 코드</span><span class="sxs-lookup"><span data-stu-id="d0622-2806">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2807">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2807">Checksum</span></span>

<span data-ttu-id="d0622-2808">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2808">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2809">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2809">Definition</span></span>

<span data-ttu-id="d0622-2810">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2810">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2811">정규식 Regex_malaysia_id_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2811">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2812">Keyword_malaysia_id_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2812">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2813">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2813">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="d0622-2814">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2814">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="d0622-2815">디지털 응용 프로그램 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2815">digital application card</span></span>
- <span data-ttu-id="d0622-2816">i/c</span><span class="sxs-lookup"><span data-stu-id="d0622-2816">i/c</span></span>
- <span data-ttu-id="d0622-2817">i/c 아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2817">i/c no</span></span>
- <span data-ttu-id="d0622-2818">비용</span><span class="sxs-lookup"><span data-stu-id="d0622-2818">ic</span></span>
- <span data-ttu-id="d0622-2819">ic 아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2819">ic no</span></span>
- <span data-ttu-id="d0622-2820">id card</span><span class="sxs-lookup"><span data-stu-id="d0622-2820">id card</span></span>
- <span data-ttu-id="d0622-2821">식별 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2821">identification Card</span></span>
- <span data-ttu-id="d0622-2822">identity card</span><span class="sxs-lookup"><span data-stu-id="d0622-2822">identity card</span></span>
- <span data-ttu-id="d0622-2823">k/p</span><span class="sxs-lookup"><span data-stu-id="d0622-2823">k/p</span></span>
- <span data-ttu-id="d0622-2824">k/p 아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2824">k/p no</span></span>
- <span data-ttu-id="d0622-2825">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="d0622-2825">kad akuan diri</span></span>
- <span data-ttu-id="d0622-2826">kad aplikasi 디지털</span><span class="sxs-lookup"><span data-stu-id="d0622-2826">kad aplikasi digital</span></span>
- <span data-ttu-id="d0622-2827">kad pengenalan 말레이시아</span><span class="sxs-lookup"><span data-stu-id="d0622-2827">kad pengenalan malaysia</span></span>
- <span data-ttu-id="d0622-2828">kp</span><span class="sxs-lookup"><span data-stu-id="d0622-2828">kp</span></span>
- <span data-ttu-id="d0622-2829">kp 아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2829">kp no</span></span>
- <span data-ttu-id="d0622-2830">mykad</span><span class="sxs-lookup"><span data-stu-id="d0622-2830">mykad</span></span>
- <span data-ttu-id="d0622-2831">mykas</span><span class="sxs-lookup"><span data-stu-id="d0622-2831">mykas</span></span>
- <span data-ttu-id="d0622-2832">mykid</span><span class="sxs-lookup"><span data-stu-id="d0622-2832">mykid</span></span>
- <span data-ttu-id="d0622-2833">mypr</span><span class="sxs-lookup"><span data-stu-id="d0622-2833">mypr</span></span>
- <span data-ttu-id="d0622-2834">myta</span><span class="sxs-lookup"><span data-stu-id="d0622-2834">mytentera</span></span>
- <span data-ttu-id="d0622-2835">말레이시아 id 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2835">malaysia identity card</span></span>
- <span data-ttu-id="d0622-2836">말레이지아 id 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2836">malaysian identity card</span></span>
- <span data-ttu-id="d0622-2837">nric</span><span class="sxs-lookup"><span data-stu-id="d0622-2837">nric</span></span>
- <span data-ttu-id="d0622-2838">개인 식별 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2838">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="d0622-2839">네덜란드 시민 서비스(BSN) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2839">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2840">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2840">Format</span></span>

<span data-ttu-id="d0622-2841">선택적으로 공백을 포함하는 8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2841">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2842">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2842">Pattern</span></span>

<span data-ttu-id="d0622-2843">8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2843">8-9 digits:</span></span>
- <span data-ttu-id="d0622-2844">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2844">Three digits</span></span> 
- <span data-ttu-id="d0622-2845">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="d0622-2845">A space (optional)</span></span> 
- <span data-ttu-id="d0622-2846">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2846">Three digits</span></span> 
- <span data-ttu-id="d0622-2847">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="d0622-2847">A space (optional)</span></span> 
- <span data-ttu-id="d0622-2848">2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2848">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2849">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2849">Checksum</span></span>

<span data-ttu-id="d0622-2850">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2850">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2851">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2851">Definition</span></span>

<span data-ttu-id="d0622-2852">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2852">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2853">Func_netherlands_bsn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2853">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2854">Keyword_netherlands_bsn에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2854">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="d0622-2855">Func_eu_date2 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2855">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="d0622-2856">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2857">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2857">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="d0622-2858">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="d0622-2858">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="d0622-2859">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="d0622-2859">Citizen service number</span></span> 
- <span data-ttu-id="d0622-2860">BSN</span><span class="sxs-lookup"><span data-stu-id="d0622-2860">BSN</span></span> 
- <span data-ttu-id="d0622-2861">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2861">Burgerservicenummer</span></span> 
- <span data-ttu-id="d0622-2862">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2862">Sofinummer</span></span> 
- <span data-ttu-id="d0622-2863">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2863">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="d0622-2864">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2864">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="d0622-2865">뉴질랜드 보건부 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2865">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2866">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2866">Format</span></span>

<span data-ttu-id="d0622-2867">3개 문자, 공백 1개(선택 사항) 및 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2867">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2868">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2868">Pattern</span></span>

<span data-ttu-id="d0622-2869">3 개의 문자 (대/소문자 구분 안 함) 공백 (선택 사항) 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2869">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2870">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2870">Checksum</span></span>

<span data-ttu-id="d0622-2871">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2871">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2872">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2872">Definition</span></span>

<span data-ttu-id="d0622-2873">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2873">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2874">Func_new_zealand_ministry_of_health_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2874">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2875">Keyword_nz_terms의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2875">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="d0622-2876">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2876">The checksum passes.</span></span>

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

<span data-ttu-id="d0622-2877">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2877">Keywords</span></span>

<span data-ttu-id="d0622-2878">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="d0622-2878">Keyword_nz_terms</span></span>

- <span data-ttu-id="d0622-2879">NHI</span><span class="sxs-lookup"><span data-stu-id="d0622-2879">NHI</span></span> 
- <span data-ttu-id="d0622-2880">New Zealand</span><span class="sxs-lookup"><span data-stu-id="d0622-2880">New Zealand</span></span> 
- <span data-ttu-id="d0622-2881">상태</span><span class="sxs-lookup"><span data-stu-id="d0622-2881">Health</span></span> 
- <span data-ttu-id="d0622-2882">처리가</span><span class="sxs-lookup"><span data-stu-id="d0622-2882">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="d0622-2883">Norway Identification Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2883">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2884">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2884">Format</span></span>

<span data-ttu-id="d0622-2885">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2885">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2886">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2886">Pattern</span></span>

<span data-ttu-id="d0622-2887">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2887">11 digits:</span></span>
- <span data-ttu-id="d0622-2888">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-2888">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="d0622-2889">3자리 개인 번호 </span><span class="sxs-lookup"><span data-stu-id="d0622-2889">Three-digit individual number</span></span> 
- <span data-ttu-id="d0622-2890">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2890">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2891">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2891">Checksum</span></span>

<span data-ttu-id="d0622-2892">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2892">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2893">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2893">Definition</span></span>

<span data-ttu-id="d0622-2894">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2894">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2895">Func_norway_id_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2895">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2896">Keyword_norway_id_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2896">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="d0622-2897">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2897">The checksum passes.</span></span>
- <span data-ttu-id="d0622-2898">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2898">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2899">Func_norway_id_numbe 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2899">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2900">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2900">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2901">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2901">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="d0622-2902">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2902">Keyword_norway_id_number</span></span>

- <span data-ttu-id="d0622-2903">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="d0622-2903">Personal identification number</span></span>
- <span data-ttu-id="d0622-2904">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2904">Norwegian ID Number</span></span>
- <span data-ttu-id="d0622-2905">ID Number</span><span class="sxs-lookup"><span data-stu-id="d0622-2905">ID Number</span></span>
- <span data-ttu-id="d0622-2906">확인과</span><span class="sxs-lookup"><span data-stu-id="d0622-2906">Identification</span></span>
- <span data-ttu-id="d0622-2907">Personnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2907">Personnummer</span></span>
- <span data-ttu-id="d0622-2908">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="d0622-2908">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="d0622-2909">필리핀 통합 다목적 ID 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2909">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2910">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2910">Format</span></span>

<span data-ttu-id="d0622-2911">하이픈으로 구분된 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2911">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2912">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2912">Pattern</span></span>

<span data-ttu-id="d0622-2913">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-2913">12 digits:</span></span>
- <span data-ttu-id="d0622-2914">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2914">Four digits</span></span> 
- <span data-ttu-id="d0622-2915">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-2915">A hyphen</span></span> 
- <span data-ttu-id="d0622-2916">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2916">Seven digits</span></span> 
- <span data-ttu-id="d0622-2917">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-2917">A hyphen</span></span> 
- <span data-ttu-id="d0622-2918">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2918">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2919">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2919">Checksum</span></span>

<span data-ttu-id="d0622-2920">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2920">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2921">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2921">Definition</span></span>

<span data-ttu-id="d0622-2922">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2922">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2923">정규식 Regex_philippines_unified_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2923">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2924">Keyword_philippines_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2924">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2925">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2925">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="d0622-2926">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="d0622-2926">Keyword_philippines_id</span></span>

- <span data-ttu-id="d0622-2927">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="d0622-2927">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="d0622-2928">UMID</span><span class="sxs-lookup"><span data-stu-id="d0622-2928">UMID</span></span> 
- <span data-ttu-id="d0622-2929">Identity Card</span><span class="sxs-lookup"><span data-stu-id="d0622-2929">Identity Card</span></span> 
- <span data-ttu-id="d0622-2930">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="d0622-2930">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="d0622-2931">폴란드 ID 카드</span><span class="sxs-lookup"><span data-stu-id="d0622-2931">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2932">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2932">Format</span></span>

<span data-ttu-id="d0622-2933">3개의 문자 및 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2933">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2934">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2934">Pattern</span></span>

<span data-ttu-id="d0622-2935">3개의 문자(대/소문자 구분 안 함)와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2935">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2936">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2936">Checksum</span></span>

<span data-ttu-id="d0622-2937">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2937">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2938">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2938">Definition</span></span>

<span data-ttu-id="d0622-2939">DLP 정책은 300 문자 근사에서 Func_polish_national_id 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2939">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="d0622-2940">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2940">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="d0622-2941">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2941">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2942">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2942">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="d0622-2943">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2943">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="d0622-2944">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="d0622-2944">Dowód osobisty</span></span>
- <span data-ttu-id="d0622-2945">U r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="d0622-2945">Numer dowodu osobistego</span></span>
- <span data-ttu-id="d0622-2946">Nazwa i u r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="d0622-2946">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="d0622-2947">Nazwa i veiligheid dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="d0622-2947">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="d0622-2948">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="d0622-2948">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="d0622-2949">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="d0622-2949">Dowód Tożsamości</span></span>
- <span data-ttu-id="d0622-2950">dow.</span><span class="sxs-lookup"><span data-stu-id="d0622-2950">dow.</span></span> <span data-ttu-id="d0622-2951">르.</span><span class="sxs-lookup"><span data-stu-id="d0622-2951">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="d0622-2952">폴란드 국가 ID(PESEL)</span><span class="sxs-lookup"><span data-stu-id="d0622-2952">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2953">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2953">Format</span></span>

<span data-ttu-id="d0622-2954">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2954">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2955">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2955">Pattern</span></span>

<span data-ttu-id="d0622-2956">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2956">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2957">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2957">Checksum</span></span>

<span data-ttu-id="d0622-2958">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2958">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2959">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2959">Definition</span></span>

<span data-ttu-id="d0622-2960">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2960">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2961">Func_pesel_identification_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2961">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2962">Keyword_pesel_identification_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2962">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="d0622-2963">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2963">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2964">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2964">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="d0622-2965">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2965">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="d0622-2966">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="d0622-2966">Nr PESEL</span></span>
- <span data-ttu-id="d0622-2967">PESEL</span><span class="sxs-lookup"><span data-stu-id="d0622-2967">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="d0622-2968">폴란드 여권</span><span class="sxs-lookup"><span data-stu-id="d0622-2968">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2969">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2969">Format</span></span>

<span data-ttu-id="d0622-2970">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2970">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2971">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2971">Pattern</span></span>

<span data-ttu-id="d0622-2972">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2972">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2973">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2973">Checksum</span></span>

<span data-ttu-id="d0622-2974">예</span><span class="sxs-lookup"><span data-stu-id="d0622-2974">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2975">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2975">Definition</span></span>

<span data-ttu-id="d0622-2976">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2976">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2977">Func_polish_passport_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2977">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2978">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2978">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="d0622-2979">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2979">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-2980">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2980">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="d0622-2981">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="d0622-2981">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="d0622-2982">U r i (zportu)</span><span class="sxs-lookup"><span data-stu-id="d0622-2982">Numer paszportu</span></span>
- <span data-ttu-id="d0622-2983">Veiligheid.</span><span class="sxs-lookup"><span data-stu-id="d0622-2983">Nr.</span></span> <span data-ttu-id="d0622-2984">고 zportu</span><span class="sxs-lookup"><span data-stu-id="d0622-2984">Paszportu</span></span>
- <span data-ttu-id="d0622-2985">고 zport</span><span class="sxs-lookup"><span data-stu-id="d0622-2985">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="d0622-2986">포르투갈 시민 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-2986">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-2987">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-2987">Format</span></span>

<span data-ttu-id="d0622-2988">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2988">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-2989">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-2989">Pattern</span></span>

<span data-ttu-id="d0622-2990">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-2990">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-2991">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-2991">Checksum</span></span>

<span data-ttu-id="d0622-2992">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-2992">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-2993">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-2993">Definition</span></span>

<span data-ttu-id="d0622-2994">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2994">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-2995">정규식 Regex_portugal_citizen_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2995">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-2996">Keyword_portugal_citizen_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-2996">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-2997">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-2997">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="d0622-2998">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="d0622-2998">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="d0622-2999">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="d0622-2999">Citizen Card</span></span>
- <span data-ttu-id="d0622-3000">National ID Card</span><span class="sxs-lookup"><span data-stu-id="d0622-3000">National ID Card</span></span>
- <span data-ttu-id="d0622-3001">참조란</span><span class="sxs-lookup"><span data-stu-id="d0622-3001">CC</span></span>
- <span data-ttu-id="d0622-3002">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="d0622-3002">Cartão de Cidadão</span></span>
- <span data-ttu-id="d0622-3003">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="d0622-3003">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="d0622-3004">사우디 아라비아 국가 ID</span><span class="sxs-lookup"><span data-stu-id="d0622-3004">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3005">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3005">Format</span></span>

<span data-ttu-id="d0622-3006">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3006">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3007">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3007">Pattern</span></span>

<span data-ttu-id="d0622-3008">10자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3008">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3009">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3009">Checksum</span></span>

<span data-ttu-id="d0622-3010">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3010">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3011">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3011">Definition</span></span>

<span data-ttu-id="d0622-3012">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3012">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3013">Regex_saudi_arabia_national_id 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3013">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3014">Keyword_saudi_arabia_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3014">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3015">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3015">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="d0622-3016">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="d0622-3016">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="d0622-3017">Identification Card</span><span class="sxs-lookup"><span data-stu-id="d0622-3017">Identification Card</span></span> 
- <span data-ttu-id="d0622-3018">I card number</span><span class="sxs-lookup"><span data-stu-id="d0622-3018">I card number</span></span> 
- <span data-ttu-id="d0622-3019">ID number</span><span class="sxs-lookup"><span data-stu-id="d0622-3019">ID number</span></span> 
- <span data-ttu-id="d0622-3020">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="d0622-3020">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="d0622-3021">싱가포르 NRIC(국가 등록 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3021">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3022">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3022">Format</span></span>

<span data-ttu-id="d0622-3023">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3023">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3024">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3024">Pattern</span></span>

- <span data-ttu-id="d0622-3025">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3025">Nine letters and digits:</span></span>
- <span data-ttu-id="d0622-3026">문자 "F", "G", "S" 또는 "T"(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="d0622-3026">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-3027">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3027">Seven digits</span></span> 
- <span data-ttu-id="d0622-3028">알파벳 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3028">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3029">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3029">Checksum</span></span>

<span data-ttu-id="d0622-3030">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3030">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3031">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3031">Definition</span></span>

<span data-ttu-id="d0622-3032">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3032">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3033">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3033">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3034">Keyword_singapore_nric에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3034">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="d0622-3035">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3035">The checksum passes.</span></span>

<span data-ttu-id="d0622-3036">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3036">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3037">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3037">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3038">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3038">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3039">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3039">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="d0622-3040">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="d0622-3040">Keyword_singapore_nric</span></span>

- <span data-ttu-id="d0622-3041">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="d0622-3041">National Registration Identity Card</span></span> 
- <span data-ttu-id="d0622-3042">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3042">Identity Card Number</span></span> 
- <span data-ttu-id="d0622-3043">NRIC</span><span class="sxs-lookup"><span data-stu-id="d0622-3043">NRIC</span></span> 
- <span data-ttu-id="d0622-3044">비용</span><span class="sxs-lookup"><span data-stu-id="d0622-3044">IC</span></span> 
- <span data-ttu-id="d0622-3045">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3045">Foreign Identification Number</span></span> 
- <span data-ttu-id="d0622-3046">삭제할</span><span class="sxs-lookup"><span data-stu-id="d0622-3046">FIN</span></span> 
- <span data-ttu-id="d0622-3047">身份证</span><span class="sxs-lookup"><span data-stu-id="d0622-3047">身份证</span></span> 
- <span data-ttu-id="d0622-3048">身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-3048">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="d0622-3049">남아프리카 공화국 식별 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3049">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3050">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3050">Format</span></span>

<span data-ttu-id="d0622-3051">공백을 포함할 수 있는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3051">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3052">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3052">Pattern</span></span>

<span data-ttu-id="d0622-3053">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3053">13 digits:</span></span>
- <span data-ttu-id="d0622-3054">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-3054">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="d0622-3055">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3055">Four digits</span></span> 
- <span data-ttu-id="d0622-3056">1자리 시민권 표시 </span><span class="sxs-lookup"><span data-stu-id="d0622-3056">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="d0622-3057">숫자 "8" 또는 "9" </span><span class="sxs-lookup"><span data-stu-id="d0622-3057">The digit "8" or "9"</span></span> 
- <span data-ttu-id="d0622-3058">체크섬 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3058">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3059">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3059">Checksum</span></span>

<span data-ttu-id="d0622-3060">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3061">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3061">Definition</span></span>

<span data-ttu-id="d0622-3062">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3063">Func_south_africa_identification_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3063">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3064">Keyword_south_africa_identification_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3064">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="d0622-3065">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3065">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3066">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3066">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="d0622-3067">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="d0622-3067">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="d0622-3068">Identity card</span><span class="sxs-lookup"><span data-stu-id="d0622-3068">Identity card</span></span>
- <span data-ttu-id="d0622-3069">ID</span><span class="sxs-lookup"><span data-stu-id="d0622-3069">ID</span></span>
- <span data-ttu-id="d0622-3070">확인과</span><span class="sxs-lookup"><span data-stu-id="d0622-3070">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="d0622-3071">한국 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3071">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3072">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3072">Format</span></span>

<span data-ttu-id="d0622-3073">하이픈을 포함하는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3073">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3074">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3074">Pattern</span></span>

<span data-ttu-id="d0622-3075">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3075">13 digits:</span></span>
- <span data-ttu-id="d0622-3076">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-3076">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="d0622-3077">하이픈</span><span class="sxs-lookup"><span data-stu-id="d0622-3077">A hyphen</span></span> 
- <span data-ttu-id="d0622-3078">세기 및 성별에 따라 결정되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-3078">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="d0622-3079">4자리 출생 지역 코드 </span><span class="sxs-lookup"><span data-stu-id="d0622-3079">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="d0622-3080">앞 번호가 동일한 사람을 구분하기 위해 사용되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="d0622-3080">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="d0622-3081">검사 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3081">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3082">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3082">Checksum</span></span>

<span data-ttu-id="d0622-3083">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3083">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3084">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3084">Definition</span></span>

<span data-ttu-id="d0622-3085">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3085">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3086">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3086">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3087">Keyword_south_korea_resident_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3087">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="d0622-3088">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3088">The checksum passes.</span></span>

<span data-ttu-id="d0622-3089">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3089">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3090">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3090">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3091">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3091">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3092">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3092">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="d0622-3093">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="d0622-3093">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="d0622-3094">National ID card</span><span class="sxs-lookup"><span data-stu-id="d0622-3094">National ID card</span></span> 
- <span data-ttu-id="d0622-3095">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3095">Citizen's Registration Number</span></span> 
- <span data-ttu-id="d0622-3096">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="d0622-3096">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="d0622-3097">RRN</span><span class="sxs-lookup"><span data-stu-id="d0622-3097">RRN</span></span> 
- <span data-ttu-id="d0622-3098">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3098">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="d0622-3099">스페인 SSN(사회 보장 번호)</span><span class="sxs-lookup"><span data-stu-id="d0622-3099">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3100">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3100">Format</span></span>

<span data-ttu-id="d0622-3101">11-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3101">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3102">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3102">Pattern</span></span>

<span data-ttu-id="d0622-3103">11-12 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3103">11-12 digits:</span></span>
- <span data-ttu-id="d0622-3104">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3104">Two digits</span></span> 
- <span data-ttu-id="d0622-3105">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="d0622-3105">A forward slash (optional)</span></span> 
- <span data-ttu-id="d0622-3106">7-8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3106">7-8 digits</span></span> 
- <span data-ttu-id="d0622-3107">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="d0622-3107">A forward slash (optional)</span></span> 
- <span data-ttu-id="d0622-3108">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3108">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3109">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3109">Checksum</span></span>

<span data-ttu-id="d0622-3110">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3110">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3111">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3111">Definition</span></span>

<span data-ttu-id="d0622-3112">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3112">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3113">Func_spanish_social_security_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3113">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3114">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3114">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3115">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3115">Keywords</span></span>

<span data-ttu-id="d0622-3116">없음</span><span class="sxs-lookup"><span data-stu-id="d0622-3116">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="d0622-3117">SQL Server 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="d0622-3117">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3118">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3118">Format</span></span>

<span data-ttu-id="d0622-3119">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "User Id", "User ID", "uid" 또는 "UserId"입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3119">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3120">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3120">Pattern</span></span>

- <span data-ttu-id="d0622-3121">문자열 "User Id", "User ID", "uid" 또는 "UserId"</span><span class="sxs-lookup"><span data-stu-id="d0622-3121">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="d0622-3122">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-3122">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="d0622-3123">문자열 "Password" 또는 "pwd" (여기에서 "pwd" 앞에 소문자 문자가 오지 않음)</span><span class="sxs-lookup"><span data-stu-id="d0622-3123">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="d0622-3124">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-3124">An equal sign (=)</span></span>
- <span data-ttu-id="d0622-3125">달러 기호 ($), 백분율 기호 (%, 부등호 (>), 기호 (@), 따옴표 ("), 세미콜론 (;), 왼쪽 중괄호 ([) 또는 왼쪽 대괄호 ({))가 아닌 모든 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-3125">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="d0622-3126">세미콜론 (;), 슬래시 (/) 또는 따옴표 (")가 아닌 7-128 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-3126">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="d0622-3127">세미콜론 (;) 또는 따옴표 (")</span><span class="sxs-lookup"><span data-stu-id="d0622-3127">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3128">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3128">Checksum</span></span>

<span data-ttu-id="d0622-3129">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3129">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3130">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3130">Definition</span></span>

<span data-ttu-id="d0622-3131">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3131">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3132">정규식 CEP_Regex_SQLServerConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3132">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3133">CEP_GlobalFilter의 키워드를 찾을 수 **없습니다** .</span><span class="sxs-lookup"><span data-stu-id="d0622-3133">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="d0622-3134">CEP_PasswordPlaceHolder 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3134">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3135">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3135">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3136">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3136">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="d0622-3137">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="d0622-3137">CEP_GlobalFilter</span></span>

- <span data-ttu-id="d0622-3138">일부 암호</span><span class="sxs-lookup"><span data-stu-id="d0622-3138">some-password</span></span>
- <span data-ttu-id="d0622-3139">somepassword</span><span class="sxs-lookup"><span data-stu-id="d0622-3139">somepassword</span></span>
- <span data-ttu-id="d0622-3140">secretPassword</span><span class="sxs-lookup"><span data-stu-id="d0622-3140">secretPassword</span></span>
- <span data-ttu-id="d0622-3141">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3141">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="d0622-3142">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="d0622-3142">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="d0622-3143">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3143">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-3144">암호나 pwd에 0-2 공백, 등호 (=), 0-2 공백 및 별표 (\*)-----------------------</span><span class="sxs-lookup"><span data-stu-id="d0622-3144">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="d0622-3145">암호나 pwd 뒤에 다음이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3145">Password or pwd followed by:</span></span>
    - <span data-ttu-id="d0622-3146">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="d0622-3146">Equal sign (=)</span></span>
    - <span data-ttu-id="d0622-3147">보다 작음 기호 (<)</span><span class="sxs-lookup"><span data-stu-id="d0622-3147">Less than symbol (<)</span></span>
    - <span data-ttu-id="d0622-3148">대문자나 소문자, digits, 별표 (\*), 하이픈 (-), 밑줄 (_) 또는 공백 문자인 1-200 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-3148">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="d0622-3149">보다 큼 기호 (>)</span><span class="sxs-lookup"><span data-stu-id="d0622-3149">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="d0622-3150">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="d0622-3150">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="d0622-3151">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3151">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="d0622-3152">극동</span><span class="sxs-lookup"><span data-stu-id="d0622-3152">contoso</span></span>
- <span data-ttu-id="d0622-3153">fabrikam</span><span class="sxs-lookup"><span data-stu-id="d0622-3153">fabrikam</span></span>
- <span data-ttu-id="d0622-3154">대양</span><span class="sxs-lookup"><span data-stu-id="d0622-3154">northwind</span></span>
- <span data-ttu-id="d0622-3155">샌드박스</span><span class="sxs-lookup"><span data-stu-id="d0622-3155">sandbox</span></span>
- <span data-ttu-id="d0622-3156">용 onebox</span><span class="sxs-lookup"><span data-stu-id="d0622-3156">onebox</span></span>
- <span data-ttu-id="d0622-3157">로컬</span><span class="sxs-lookup"><span data-stu-id="d0622-3157">localhost</span></span>
- <span data-ttu-id="d0622-3158">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d0622-3158">127.0.0.1</span></span>
- <span data-ttu-id="d0622-3159">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3159">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-3160">ccw</span><span class="sxs-lookup"><span data-stu-id="d0622-3160">com</span></span>
- <span data-ttu-id="d0622-3161">s-int</span><span class="sxs-lookup"><span data-stu-id="d0622-3161">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="d0622-3162">투자</span><span class="sxs-lookup"><span data-stu-id="d0622-3162">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="d0622-3163">스웨덴 국가 ID</span><span class="sxs-lookup"><span data-stu-id="d0622-3163">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3164">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3164">Format</span></span>

<span data-ttu-id="d0622-3165">10 또는 12자리 숫자와 선택적 구분 기호</span><span class="sxs-lookup"><span data-stu-id="d0622-3165">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3166">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3166">Pattern</span></span>

<span data-ttu-id="d0622-3167">10 또는 12자리 숫자와 선택적 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="d0622-3167">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="d0622-3168">2-4자리 숫자(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="d0622-3168">2-4 digits (optional)</span></span> 
- <span data-ttu-id="d0622-3169">YYMMDD 날짜 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3169">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="d0622-3170">구분 기호 "-" 또는 "+"(선택 사항) 및</span><span class="sxs-lookup"><span data-stu-id="d0622-3170">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="d0622-3171">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3171">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3172">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3172">Checksum</span></span>

<span data-ttu-id="d0622-3173">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3173">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3174">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3174">Definition</span></span>

<span data-ttu-id="d0622-3175">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3175">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3176">Func_swedish_national_identifier 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3176">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3177">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3177">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3178">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3178">Keywords</span></span>

<span data-ttu-id="d0622-3179">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3179">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="d0622-3180">스웨덴 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3180">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3181">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3181">Format</span></span>

<span data-ttu-id="d0622-3182">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3182">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3183">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3183">Pattern</span></span>

<span data-ttu-id="d0622-3184">8자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3184">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3185">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3185">Checksum</span></span>

<span data-ttu-id="d0622-3186">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3186">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3187">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3187">Definition</span></span>

<span data-ttu-id="d0622-3188">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3188">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3189">Regex_sweden_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3189">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3190">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3190">One of the following is true:</span></span>
    - <span data-ttu-id="d0622-3191">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3191">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="d0622-3192">Keyword_sweden_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3192">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3193">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3193">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="d0622-3194">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-3194">Keyword_sweden_passport</span></span>

- <span data-ttu-id="d0622-3195">visa requirements</span><span class="sxs-lookup"><span data-stu-id="d0622-3195">visa requirements</span></span> 
- <span data-ttu-id="d0622-3196">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="d0622-3196">Alien Registration Card</span></span> 
- <span data-ttu-id="d0622-3197">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="d0622-3197">Schengen visas</span></span> 
- <span data-ttu-id="d0622-3198">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="d0622-3198">Schengen visa</span></span> 
- <span data-ttu-id="d0622-3199">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="d0622-3199">Visa Processing</span></span> 
- <span data-ttu-id="d0622-3200">Visa Type</span><span class="sxs-lookup"><span data-stu-id="d0622-3200">Visa Type</span></span> 
- <span data-ttu-id="d0622-3201">Single Entry</span><span class="sxs-lookup"><span data-stu-id="d0622-3201">Single Entry</span></span> 
- <span data-ttu-id="d0622-3202">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="d0622-3202">Multiple Entry</span></span> 
- <span data-ttu-id="d0622-3203">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="d0622-3203">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="d0622-3204">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-3204">Keyword_passport</span></span>

- <span data-ttu-id="d0622-3205">Passport Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3205">Passport Number</span></span> 
- <span data-ttu-id="d0622-3206">Passport No</span><span class="sxs-lookup"><span data-stu-id="d0622-3206">Passport No</span></span> 
- <span data-ttu-id="d0622-3207">Passport #</span><span class="sxs-lookup"><span data-stu-id="d0622-3207">Passport #</span></span> 
- <span data-ttu-id="d0622-3208">여권 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3208">Passport#</span></span> 
- <span data-ttu-id="d0622-3209">PassportID</span><span class="sxs-lookup"><span data-stu-id="d0622-3209">PassportID</span></span> 
- <span data-ttu-id="d0622-3210">Passportno</span><span class="sxs-lookup"><span data-stu-id="d0622-3210">Passportno</span></span> 
- <span data-ttu-id="d0622-3211">passportnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-3211">passportnumber</span></span> 
- <span data-ttu-id="d0622-3212">パスポート</span><span class="sxs-lookup"><span data-stu-id="d0622-3212">パスポート</span></span> 
- <span data-ttu-id="d0622-3213">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="d0622-3213">パスポート番号</span></span> 
- <span data-ttu-id="d0622-3214">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="d0622-3214">パスポートのNum</span></span> 
- <span data-ttu-id="d0622-3215">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="d0622-3215">パスポート＃</span></span> 
- <span data-ttu-id="d0622-3216">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d0622-3216">Numéro de passeport</span></span> 
- <span data-ttu-id="d0622-3217">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="d0622-3217">Passeport n °</span></span> 
- <span data-ttu-id="d0622-3218">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="d0622-3218">Passeport Non</span></span> 
- <span data-ttu-id="d0622-3219">Passeport #</span><span class="sxs-lookup"><span data-stu-id="d0622-3219">Passeport #</span></span> 
- <span data-ttu-id="d0622-3220">포트 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3220">Passeport#</span></span> 
- <span data-ttu-id="d0622-3221">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="d0622-3221">PasseportNon</span></span> 
- <span data-ttu-id="d0622-3222">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="d0622-3222">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="d0622-3223">SWIFT 코드</span><span class="sxs-lookup"><span data-stu-id="d0622-3223">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3224">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3224">Format</span></span>

<span data-ttu-id="d0622-3225">4개의 문자, 5-31개 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3225">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3226">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3226">Pattern</span></span>

<span data-ttu-id="d0622-3227">4개의 문자, 5-31개 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3227">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="d0622-3228">4문자 은행 코드(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-3228">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-3229">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-3229">An optional space</span></span> 
- <span data-ttu-id="d0622-3230">4-28개 문자 또는 숫자[BBAN(기본 은행 계좌 번호)]</span><span class="sxs-lookup"><span data-stu-id="d0622-3230">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="d0622-3231">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="d0622-3231">An optional space</span></span> 
- <span data-ttu-id="d0622-3232">1-3개 문자 또는 숫자(BBAN의 나머지)</span><span class="sxs-lookup"><span data-stu-id="d0622-3232">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3233">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3233">Checksum</span></span>

<span data-ttu-id="d0622-3234">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3234">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3235">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3235">Definition</span></span>

<span data-ttu-id="d0622-3236">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3236">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3237">Regex_swift 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3237">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3238">Keyword_swift의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3238">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3239">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3239">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="d0622-3240">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="d0622-3240">Keyword_swift</span></span>

- <span data-ttu-id="d0622-3241">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="d0622-3241">international organization for standardization 9362</span></span> 
- <span data-ttu-id="d0622-3242">iso 9362</span><span class="sxs-lookup"><span data-stu-id="d0622-3242">iso 9362</span></span> 
- <span data-ttu-id="d0622-3243">iso9362</span><span class="sxs-lookup"><span data-stu-id="d0622-3243">iso9362</span></span> 
- <span data-ttu-id="d0622-3244">swift\#</span><span class="sxs-lookup"><span data-stu-id="d0622-3244">swift\#</span></span> 
- <span data-ttu-id="d0622-3245">swiftcode</span><span class="sxs-lookup"><span data-stu-id="d0622-3245">swiftcode</span></span> 
- <span data-ttu-id="d0622-3246">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-3246">swiftnumber</span></span> 
- <span data-ttu-id="d0622-3247">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-3247">swiftroutingnumber</span></span> 
- <span data-ttu-id="d0622-3248">swift code</span><span class="sxs-lookup"><span data-stu-id="d0622-3248">swift code</span></span> 
- <span data-ttu-id="d0622-3249">swift number #</span><span class="sxs-lookup"><span data-stu-id="d0622-3249">swift number #</span></span> 
- <span data-ttu-id="d0622-3250">swift routing number</span><span class="sxs-lookup"><span data-stu-id="d0622-3250">swift routing number</span></span> 
- <span data-ttu-id="d0622-3251">bic number</span><span class="sxs-lookup"><span data-stu-id="d0622-3251">bic number</span></span> 
- <span data-ttu-id="d0622-3252">bic code</span><span class="sxs-lookup"><span data-stu-id="d0622-3252">bic code</span></span> 
- <span data-ttu-id="d0622-3253">bic\#</span><span class="sxs-lookup"><span data-stu-id="d0622-3253">bic \#</span></span> 
- <span data-ttu-id="d0622-3254">bic\#</span><span class="sxs-lookup"><span data-stu-id="d0622-3254">bic\#</span></span> 
- <span data-ttu-id="d0622-3255">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="d0622-3255">bank identifier code</span></span> 
- <span data-ttu-id="d0622-3256">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="d0622-3256">標準化9362</span></span> 
- <span data-ttu-id="d0622-3257">迅速＃</span><span class="sxs-lookup"><span data-stu-id="d0622-3257">迅速＃</span></span> 
- <span data-ttu-id="d0622-3258">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="d0622-3258">SWIFTコード</span></span> 
- <span data-ttu-id="d0622-3259">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="d0622-3259">SWIFT番号</span></span> 
- <span data-ttu-id="d0622-3260">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="d0622-3260">迅速なルーティング番号</span></span> 
- <span data-ttu-id="d0622-3261">BIC番号</span><span class="sxs-lookup"><span data-stu-id="d0622-3261">BIC番号</span></span> 
- <span data-ttu-id="d0622-3262">BICコード</span><span class="sxs-lookup"><span data-stu-id="d0622-3262">BICコード</span></span> 
- <span data-ttu-id="d0622-3263">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="d0622-3263">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="d0622-3264">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="d0622-3264">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="d0622-3265">rapide\#</span><span class="sxs-lookup"><span data-stu-id="d0622-3265">rapide \#</span></span> 
- <span data-ttu-id="d0622-3266">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="d0622-3266">code SWIFT</span></span> 
- <span data-ttu-id="d0622-3267">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="d0622-3267">le numéro de swift</span></span> 
- <span data-ttu-id="d0622-3268">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="d0622-3268">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="d0622-3269">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="d0622-3269">le numéro BIC</span></span> 
- <span data-ttu-id="d0622-3270">\#BIC</span><span class="sxs-lookup"><span data-stu-id="d0622-3270">\# BIC</span></span> 
- <span data-ttu-id="d0622-3271">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="d0622-3271">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="d0622-3272">대만 국가 ID</span><span class="sxs-lookup"><span data-stu-id="d0622-3272">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3273">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3273">Format</span></span>

<span data-ttu-id="d0622-3274">1개의 문자, 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3274">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3275">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3275">Pattern</span></span>

<span data-ttu-id="d0622-3276">1개의 문자, 9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3276">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="d0622-3277">1개 문자(영문, 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-3277">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="d0622-3278">숫자 "1" 또는 "2"</span><span class="sxs-lookup"><span data-stu-id="d0622-3278">The digit "1" or "2"</span></span> 
- <span data-ttu-id="d0622-3279">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3279">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3280">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3280">Checksum</span></span>

<span data-ttu-id="d0622-3281">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3281">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3282">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3282">Definition</span></span>

<span data-ttu-id="d0622-3283">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3283">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3284">Func_taiwanese_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3284">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3285">Keyword_taiwanese_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3285">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="d0622-3286">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3286">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3287">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3287">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="d0622-3288">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="d0622-3288">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="d0622-3289">身份證字號</span><span class="sxs-lookup"><span data-stu-id="d0622-3289">身份證字號</span></span> 
- <span data-ttu-id="d0622-3290">身份證</span><span class="sxs-lookup"><span data-stu-id="d0622-3290">身份證</span></span> 
- <span data-ttu-id="d0622-3291">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="d0622-3291">身份證號碼</span></span> 
- <span data-ttu-id="d0622-3292">身份證號</span><span class="sxs-lookup"><span data-stu-id="d0622-3292">身份證號</span></span> 
- <span data-ttu-id="d0622-3293">身分證字號</span><span class="sxs-lookup"><span data-stu-id="d0622-3293">身分證字號</span></span> 
- <span data-ttu-id="d0622-3294">身分證</span><span class="sxs-lookup"><span data-stu-id="d0622-3294">身分證</span></span> 
- <span data-ttu-id="d0622-3295">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="d0622-3295">身分證號碼</span></span> 
- <span data-ttu-id="d0622-3296">身份證號</span><span class="sxs-lookup"><span data-stu-id="d0622-3296">身份證號</span></span> 
- <span data-ttu-id="d0622-3297">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="d0622-3297">身分證統一編號</span></span> 
- <span data-ttu-id="d0622-3298">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="d0622-3298">國民身分證統一編號</span></span> 
- <span data-ttu-id="d0622-3299">簽名</span><span class="sxs-lookup"><span data-stu-id="d0622-3299">簽名</span></span> 
- <span data-ttu-id="d0622-3300">蓋章</span><span class="sxs-lookup"><span data-stu-id="d0622-3300">蓋章</span></span> 
- <span data-ttu-id="d0622-3301">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="d0622-3301">簽名或蓋章</span></span> 
- <span data-ttu-id="d0622-3302">簽章</span><span class="sxs-lookup"><span data-stu-id="d0622-3302">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="d0622-3303">	대만 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3303">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3304">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3304">Format</span></span>

- <span data-ttu-id="d0622-3305">생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3305">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="d0622-3306">비-생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3306">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3307">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3307">Pattern</span></span>
<span data-ttu-id="d0622-3308">생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="d0622-3308">Biometric passport number:</span></span>
- <span data-ttu-id="d0622-3309">숫자 "3" </span><span class="sxs-lookup"><span data-stu-id="d0622-3309">The digit "3"</span></span> 
- <span data-ttu-id="d0622-3310">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3310">Eight digits</span></span>

<span data-ttu-id="d0622-3311">비-생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="d0622-3311">Non-biometric passport number:</span></span>
- <span data-ttu-id="d0622-3312">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3312">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3313">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3313">Checksum</span></span>

<span data-ttu-id="d0622-3314">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3314">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3315">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3315">Definition</span></span>

<span data-ttu-id="d0622-3316">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3316">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3317">정규식 Regex_taiwan_passport 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3317">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3318">Keyword_taiwan_passport에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3318">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3319">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3319">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="d0622-3320">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-3320">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="d0622-3321">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="d0622-3321">ROC passport number</span></span> 
- <span data-ttu-id="d0622-3322">Passport number</span><span class="sxs-lookup"><span data-stu-id="d0622-3322">Passport number</span></span> 
- <span data-ttu-id="d0622-3323">Passport no</span><span class="sxs-lookup"><span data-stu-id="d0622-3323">Passport no</span></span> 
- <span data-ttu-id="d0622-3324">Passport Num</span><span class="sxs-lookup"><span data-stu-id="d0622-3324">Passport Num</span></span> 
- <span data-ttu-id="d0622-3325">Passport #</span><span class="sxs-lookup"><span data-stu-id="d0622-3325">Passport #</span></span> 
- <span data-ttu-id="d0622-3326">护照</span><span class="sxs-lookup"><span data-stu-id="d0622-3326">护照</span></span> 
- <span data-ttu-id="d0622-3327">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="d0622-3327">中華民國護照</span></span> 
- <span data-ttu-id="d0622-3328">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="d0622-3328">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="d0622-3329">대만 거주 인증(ARC/TARC) 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3329">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3330">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3330">Format</span></span>

<span data-ttu-id="d0622-3331">10개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3331">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3332">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3332">Pattern</span></span>

<span data-ttu-id="d0622-3333">10개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3333">10 letters and digits:</span></span>
- <span data-ttu-id="d0622-3334">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-3334">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="d0622-3335">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3335">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3336">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3336">Checksum</span></span>

<span data-ttu-id="d0622-3337">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3337">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3338">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3338">Definition</span></span>

<span data-ttu-id="d0622-3339">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3340">정규식 Regex_taiwan_resident_certificate 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3340">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3341">Keyword_taiwan_resident_certificate에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3341">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3342">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3342">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="d0622-3343">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="d0622-3343">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="d0622-3344">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="d0622-3344">Resident Certificate</span></span> 
- <span data-ttu-id="d0622-3345">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="d0622-3345">Resident Cert</span></span> 
- <span data-ttu-id="d0622-3346">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="d0622-3346">Resident Cert.</span></span> 
- <span data-ttu-id="d0622-3347">Identification card</span><span class="sxs-lookup"><span data-stu-id="d0622-3347">Identification card</span></span> 
- <span data-ttu-id="d0622-3348">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="d0622-3348">Alien Resident Certificate</span></span> 
- <span data-ttu-id="d0622-3349">화살표</span><span class="sxs-lookup"><span data-stu-id="d0622-3349">ARC</span></span> 
- <span data-ttu-id="d0622-3350">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="d0622-3350">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="d0622-3351">TARC</span><span class="sxs-lookup"><span data-stu-id="d0622-3351">TARC</span></span> 
- <span data-ttu-id="d0622-3352">居留證</span><span class="sxs-lookup"><span data-stu-id="d0622-3352">居留證</span></span> 
- <span data-ttu-id="d0622-3353">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="d0622-3353">外僑居留證</span></span> 
- <span data-ttu-id="d0622-3354">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="d0622-3354">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="d0622-3355">태국어 인구 식별 코드</span><span class="sxs-lookup"><span data-stu-id="d0622-3355">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3356">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3356">Format</span></span>

<span data-ttu-id="d0622-3357">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3357">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3358">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3358">Pattern</span></span>

<span data-ttu-id="d0622-3359">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3359">13 digits:</span></span>
- <span data-ttu-id="d0622-3360">첫 번째 숫자가 0 또는 9가 아님</span><span class="sxs-lookup"><span data-stu-id="d0622-3360">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="d0622-3361">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3361">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3362">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3362">Checksum</span></span>

<span data-ttu-id="d0622-3363">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3363">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3364">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3364">Definition</span></span>

<span data-ttu-id="d0622-3365">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3365">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3366">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3366">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3367">Keyword_Thai_Citizen_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3367">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="d0622-3368">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3368">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3369">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3369">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3370">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3370">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="d0622-3371">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="d0622-3371">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="d0622-3372">ID Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3372">ID Number</span></span>
- <span data-ttu-id="d0622-3373">Id 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3373">Identification Number</span></span>
- <span data-ttu-id="d0622-3374">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="d0622-3374">บัตรประชาชน</span></span>
- <span data-ttu-id="d0622-3375">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="d0622-3375">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="d0622-3376">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="d0622-3376">บัตรประชาชน</span></span>
- <span data-ttu-id="d0622-3377">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="d0622-3377">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="d0622-3378">터키어 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3378">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3379">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3379">Format</span></span>

<span data-ttu-id="d0622-3380">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3380">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3381">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3381">Pattern</span></span>

<span data-ttu-id="d0622-3382">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3382">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3383">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3383">Checksum</span></span>

<span data-ttu-id="d0622-3384">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3384">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3385">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3385">Definition</span></span>

<span data-ttu-id="d0622-3386">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3386">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3387">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3387">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3388">Keyword_Turkish_National_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3388">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="d0622-3389">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3390">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3390">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3391">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3391">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="d0622-3392">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="d0622-3392">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="d0622-3393">TC Kimlik 아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3393">TC Kimlik No</span></span>
- <span data-ttu-id="d0622-3394">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="d0622-3394">TC Kimlik numarası</span></span>
- <span data-ttu-id="d0622-3395">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="d0622-3395">Vatandaşlık numarası</span></span>
- <span data-ttu-id="d0622-3396">Vatandaşlık 아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3396">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="d0622-p142">영국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-p142">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3399">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3399">Format</span></span>

<span data-ttu-id="d0622-3400">지정된 형식의 18개 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="d0622-3400">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3401">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3401">Pattern</span></span>

<span data-ttu-id="d0622-3402">18개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3402">18 letters and digits:</span></span>
- <span data-ttu-id="d0622-3403">5개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="d0622-3403">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="d0622-3404">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3404">One digit</span></span> 
- <span data-ttu-id="d0622-3405">생년월일에 대한 DDMMY 날짜 형식의 5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3405">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="d0622-3406">2개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="d0622-3406">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="d0622-3407">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3407">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3408">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3408">Checksum</span></span>

<span data-ttu-id="d0622-3409">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3409">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3410">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3410">Definition</span></span>

<span data-ttu-id="d0622-3411">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3412">Func_uk_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3412">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3413">Keyword_uk_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3413">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="d0622-3414">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3414">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3415">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3415">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="d0622-3416">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d0622-3416">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="d0622-3417">DVLA</span><span class="sxs-lookup"><span data-stu-id="d0622-3417">DVLA</span></span> 
- <span data-ttu-id="d0622-3418">light vans</span><span class="sxs-lookup"><span data-stu-id="d0622-3418">light vans</span></span> 
- <span data-ttu-id="d0622-3419">quadbikes</span><span class="sxs-lookup"><span data-stu-id="d0622-3419">quadbikes</span></span> 
- <span data-ttu-id="d0622-3420">motor cars</span><span class="sxs-lookup"><span data-stu-id="d0622-3420">motor cars</span></span> 
- <span data-ttu-id="d0622-3421">125cc</span><span class="sxs-lookup"><span data-stu-id="d0622-3421">125cc</span></span> 
- <span data-ttu-id="d0622-3422">sidecar</span><span class="sxs-lookup"><span data-stu-id="d0622-3422">sidecar</span></span> 
- <span data-ttu-id="d0622-3423">tricycles</span><span class="sxs-lookup"><span data-stu-id="d0622-3423">tricycles</span></span> 
- <span data-ttu-id="d0622-3424">motorcycles</span><span class="sxs-lookup"><span data-stu-id="d0622-3424">motorcycles</span></span> 
- <span data-ttu-id="d0622-3425">photocard licence</span><span class="sxs-lookup"><span data-stu-id="d0622-3425">photocard licence</span></span> 
- <span data-ttu-id="d0622-3426">learner drivers</span><span class="sxs-lookup"><span data-stu-id="d0622-3426">learner drivers</span></span> 
- <span data-ttu-id="d0622-3427">licence holder</span><span class="sxs-lookup"><span data-stu-id="d0622-3427">licence holder</span></span> 
- <span data-ttu-id="d0622-3428">licence holders</span><span class="sxs-lookup"><span data-stu-id="d0622-3428">licence holders</span></span> 
- <span data-ttu-id="d0622-3429">driving licences</span><span class="sxs-lookup"><span data-stu-id="d0622-3429">driving licences</span></span> 
- <span data-ttu-id="d0622-3430">driving licence</span><span class="sxs-lookup"><span data-stu-id="d0622-3430">driving licence</span></span> 
- <span data-ttu-id="d0622-3431">dual control car</span><span class="sxs-lookup"><span data-stu-id="d0622-3431">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="d0622-p143">영국 선거 롤 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-p143">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3434">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3434">Format</span></span>

<span data-ttu-id="d0622-3435">2개의 문자, 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3435">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3436">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3436">Pattern</span></span>

<span data-ttu-id="d0622-3437">2개의 문자(대/소문자 구분 안 함)와 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3437">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3438">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3438">Checksum</span></span>

<span data-ttu-id="d0622-3439">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3439">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3440">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3440">Definition</span></span>

<span data-ttu-id="d0622-3441">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3441">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3442">Regex_uk_electoral 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3442">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3443">Keyword_uk_electoral의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3443">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3444">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3444">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="d0622-3445">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="d0622-3445">Keyword_uk_electoral</span></span>

- <span data-ttu-id="d0622-3446">council nomination</span><span class="sxs-lookup"><span data-stu-id="d0622-3446">council nomination</span></span> 
- <span data-ttu-id="d0622-3447">nomination form</span><span class="sxs-lookup"><span data-stu-id="d0622-3447">nomination form</span></span> 
- <span data-ttu-id="d0622-3448">electoral register</span><span class="sxs-lookup"><span data-stu-id="d0622-3448">electoral register</span></span> 
- <span data-ttu-id="d0622-3449">electoral roll</span><span class="sxs-lookup"><span data-stu-id="d0622-3449">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="d0622-p144">영국 국립 보건 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-p144">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3452">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3452">Format</span></span>

<span data-ttu-id="d0622-3453">공백으로 구분된 10-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3453">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3454">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3454">Pattern</span></span>

<span data-ttu-id="d0622-3455">10-17자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="d0622-3455">10-17 digits:</span></span>
- <span data-ttu-id="d0622-3456">3 또는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3456">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="d0622-3457">공백</span><span class="sxs-lookup"><span data-stu-id="d0622-3457">A space</span></span> 
- <span data-ttu-id="d0622-3458">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3458">Three digits</span></span> 
- <span data-ttu-id="d0622-3459">공백</span><span class="sxs-lookup"><span data-stu-id="d0622-3459">A space</span></span> 
- <span data-ttu-id="d0622-3460">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3460">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3461">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3461">Checksum</span></span>

<span data-ttu-id="d0622-3462">예</span><span class="sxs-lookup"><span data-stu-id="d0622-3462">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3463">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3463">Definition</span></span>

<span data-ttu-id="d0622-3464">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3464">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3465">Func_uk_nhs_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3465">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3466">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3466">One of the following is true:</span></span>
    - <span data-ttu-id="d0622-3467">Keyword_uk_nhs_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3467">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="d0622-3468">Keyword_uk_nhs_number1의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3468">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="d0622-3469">Keyword_uk_nhs_number_dob의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3469">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="d0622-3470">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3470">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3471">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3471">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="d0622-3472">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="d0622-3472">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="d0622-3473">국립 보건 서비스</span><span class="sxs-lookup"><span data-stu-id="d0622-3473">national health service</span></span> 
- <span data-ttu-id="d0622-3474">nhs</span><span class="sxs-lookup"><span data-stu-id="d0622-3474">nhs</span></span> 
- <span data-ttu-id="d0622-3475">health services authority</span><span class="sxs-lookup"><span data-stu-id="d0622-3475">health services authority</span></span> 
- <span data-ttu-id="d0622-3476">health authority</span><span class="sxs-lookup"><span data-stu-id="d0622-3476">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="d0622-3477">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="d0622-3477">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="d0622-3478">patient id</span><span class="sxs-lookup"><span data-stu-id="d0622-3478">patient id</span></span> 
- <span data-ttu-id="d0622-3479">patient identification</span><span class="sxs-lookup"><span data-stu-id="d0622-3479">patient identification</span></span> 
- <span data-ttu-id="d0622-3480">patient no</span><span class="sxs-lookup"><span data-stu-id="d0622-3480">patient no</span></span> 
- <span data-ttu-id="d0622-3481">patient number</span><span class="sxs-lookup"><span data-stu-id="d0622-3481">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="d0622-3482">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="d0622-3482">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="d0622-3483">G</span><span class="sxs-lookup"><span data-stu-id="d0622-3483">GP</span></span> 
- <span data-ttu-id="d0622-3484">DOB</span><span class="sxs-lookup"><span data-stu-id="d0622-3484">DOB</span></span> 
- <span data-ttu-id="d0622-3485">D. O. B</span><span class="sxs-lookup"><span data-stu-id="d0622-3485">D.O.B</span></span> 
- <span data-ttu-id="d0622-3486">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="d0622-3486">Date of Birth</span></span> 
- <span data-ttu-id="d0622-3487">Birth Date</span><span class="sxs-lookup"><span data-stu-id="d0622-3487">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="d0622-p145">영국 NINO(국민 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="d0622-p145">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3490">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3490">Format</span></span>

<span data-ttu-id="d0622-3491">공백 또는 대시로 구분 된 7 자 또는 9 자</span><span class="sxs-lookup"><span data-stu-id="d0622-3491">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3492">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3492">Pattern</span></span>

<span data-ttu-id="d0622-3493">다음과 같은 두 가지 패턴을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3493">Two possible patterns:</span></span>

- <span data-ttu-id="d0622-3494">두 문자 (유효한 NINOs이 접두사의 특정 문자만 사용 하며이 패턴의 유효성 검사는 대/소문자를 구분 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="d0622-3494">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="d0622-3495">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3495">Six digits</span></span>
- <span data-ttu-id="d0622-3496">' A ', ' B ', ' C ' 또는 ' d ' (접두사와 마찬가지로 접미사에서는 특정 문자만 허용 되며 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="d0622-3496">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="d0622-3497">또는</span><span class="sxs-lookup"><span data-stu-id="d0622-3497">OR</span></span>

- <span data-ttu-id="d0622-3498">2 개 문자</span><span class="sxs-lookup"><span data-stu-id="d0622-3498">Two letters</span></span>
- <span data-ttu-id="d0622-3499">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="d0622-3499">A space or dash</span></span>
- <span data-ttu-id="d0622-3500">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3500">Two digits</span></span>
- <span data-ttu-id="d0622-3501">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="d0622-3501">A space or dash</span></span>
- <span data-ttu-id="d0622-3502">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3502">Two digits</span></span>
- <span data-ttu-id="d0622-3503">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="d0622-3503">A space or dash</span></span>
- <span data-ttu-id="d0622-3504">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3504">Two digits</span></span>
- <span data-ttu-id="d0622-3505">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="d0622-3505">A space or dash</span></span>
- <span data-ttu-id="d0622-3506">' A ', ' B ', ' C ' 또는 ' d ' 중 하나</span><span class="sxs-lookup"><span data-stu-id="d0622-3506">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3507">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3507">Checksum</span></span>

<span data-ttu-id="d0622-3508">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3508">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3509">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3509">Definition</span></span>

<span data-ttu-id="d0622-3510">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3511">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3511">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3512">Keyword_uk_nino의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3512">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="d0622-3513">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3513">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3514">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3514">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3515">Keyword_uk_nino의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3515">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3516">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3516">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="d0622-3517">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="d0622-3517">Keyword_uk_nino</span></span>

- <span data-ttu-id="d0622-3518">national insurance number</span><span class="sxs-lookup"><span data-stu-id="d0622-3518">national insurance number</span></span> 
- <span data-ttu-id="d0622-3519">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="d0622-3519">national insurance contributions</span></span> 
- <span data-ttu-id="d0622-3520">protection act</span><span class="sxs-lookup"><span data-stu-id="d0622-3520">protection act</span></span> 
- <span data-ttu-id="d0622-3521">소유권</span><span class="sxs-lookup"><span data-stu-id="d0622-3521">insurance</span></span> 
- <span data-ttu-id="d0622-3522">social security number</span><span class="sxs-lookup"><span data-stu-id="d0622-3522">social security number</span></span> 
- <span data-ttu-id="d0622-3523">insurance application</span><span class="sxs-lookup"><span data-stu-id="d0622-3523">insurance application</span></span> 
- <span data-ttu-id="d0622-3524">medical application</span><span class="sxs-lookup"><span data-stu-id="d0622-3524">medical application</span></span> 
- <span data-ttu-id="d0622-3525">social insurance</span><span class="sxs-lookup"><span data-stu-id="d0622-3525">social insurance</span></span> 
- <span data-ttu-id="d0622-3526">medical attention</span><span class="sxs-lookup"><span data-stu-id="d0622-3526">medical attention</span></span> 
- <span data-ttu-id="d0622-3527">social security</span><span class="sxs-lookup"><span data-stu-id="d0622-3527">social security</span></span> 
- <span data-ttu-id="d0622-3528">great britain</span><span class="sxs-lookup"><span data-stu-id="d0622-3528">great britain</span></span> 
- <span data-ttu-id="d0622-3529">소유권</span><span class="sxs-lookup"><span data-stu-id="d0622-3529">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="d0622-p146">미국/영국 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-p146">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3532">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3532">Format</span></span>

<span data-ttu-id="d0622-3533">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3534">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3534">Pattern</span></span>

<span data-ttu-id="d0622-3535">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3536">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3536">Checksum</span></span>

<span data-ttu-id="d0622-3537">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3537">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3538">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3538">Definition</span></span>

<span data-ttu-id="d0622-3539">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3540">Func_usa_uk_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3540">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3541">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3541">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3542">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3542">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="d0622-3543">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="d0622-3543">Keyword_passport</span></span>

- <span data-ttu-id="d0622-3544">Passport Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3544">Passport Number</span></span> 
- <span data-ttu-id="d0622-3545">Passport No</span><span class="sxs-lookup"><span data-stu-id="d0622-3545">Passport No</span></span> 
- <span data-ttu-id="d0622-3546">Passport #</span><span class="sxs-lookup"><span data-stu-id="d0622-3546">Passport #</span></span> 
- <span data-ttu-id="d0622-3547">여권 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3547">Passport#</span></span> 
- <span data-ttu-id="d0622-3548">PassportID</span><span class="sxs-lookup"><span data-stu-id="d0622-3548">PassportID</span></span> 
- <span data-ttu-id="d0622-3549">Passportno</span><span class="sxs-lookup"><span data-stu-id="d0622-3549">Passportno</span></span> 
- <span data-ttu-id="d0622-3550">passportnumber</span><span class="sxs-lookup"><span data-stu-id="d0622-3550">passportnumber</span></span> 
- <span data-ttu-id="d0622-3551">パスポート</span><span class="sxs-lookup"><span data-stu-id="d0622-3551">パスポート</span></span> 
- <span data-ttu-id="d0622-3552">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="d0622-3552">パスポート番号</span></span> 
- <span data-ttu-id="d0622-3553">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="d0622-3553">パスポートのNum</span></span> 
- <span data-ttu-id="d0622-3554">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="d0622-3554">パスポート＃</span></span> 
- <span data-ttu-id="d0622-3555">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="d0622-3555">Numéro de passeport</span></span> 
- <span data-ttu-id="d0622-3556">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="d0622-3556">Passeport n °</span></span> 
- <span data-ttu-id="d0622-3557">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="d0622-3557">Passeport Non</span></span> 
- <span data-ttu-id="d0622-3558">Passeport #</span><span class="sxs-lookup"><span data-stu-id="d0622-3558">Passeport #</span></span> 
- <span data-ttu-id="d0622-3559">포트 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3559">Passeport#</span></span> 
- <span data-ttu-id="d0622-3560">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="d0622-3560">PasseportNon</span></span> 
- <span data-ttu-id="d0622-3561">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="d0622-3561">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="d0622-3562">미국 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3562">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3563">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3563">Format</span></span>

<span data-ttu-id="d0622-3564">8-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3564">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3565">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3565">Pattern</span></span>

<span data-ttu-id="d0622-3566">8-17자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3566">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3567">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3567">Checksum</span></span>

<span data-ttu-id="d0622-3568">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3568">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3569">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3569">Definition</span></span>

<span data-ttu-id="d0622-3570">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3571">Regex_usa_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3571">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3572">Keyword_usa_Bank_Account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3572">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d0622-3573">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3573">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="d0622-3574">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="d0622-3574">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="d0622-3575">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3575">Checking Account Number</span></span> 
- <span data-ttu-id="d0622-3576">Checking Account</span><span class="sxs-lookup"><span data-stu-id="d0622-3576">Checking Account</span></span> 
- <span data-ttu-id="d0622-3577">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="d0622-3577">Checking Account #</span></span> 
- <span data-ttu-id="d0622-3578">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3578">Checking Acct Number</span></span> 
- <span data-ttu-id="d0622-3579">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="d0622-3579">Checking Acct #</span></span> 
- <span data-ttu-id="d0622-3580">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="d0622-3580">Checking Acct No.</span></span> 
- <span data-ttu-id="d0622-3581">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="d0622-3581">Checking Account No.</span></span> 
- <span data-ttu-id="d0622-3582">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3582">Bank Account Number</span></span> 
- <span data-ttu-id="d0622-3583">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="d0622-3583">Bank Account #</span></span> 
- <span data-ttu-id="d0622-3584">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3584">Bank Acct Number</span></span> 
- <span data-ttu-id="d0622-3585">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="d0622-3585">Bank Acct #</span></span> 
- <span data-ttu-id="d0622-3586">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="d0622-3586">Bank Acct No.</span></span> 
- <span data-ttu-id="d0622-3587">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="d0622-3587">Bank Account No.</span></span> 
- <span data-ttu-id="d0622-3588">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3588">Savings Account Number</span></span> 
- <span data-ttu-id="d0622-3589">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="d0622-3589">Savings Account.</span></span> 
- <span data-ttu-id="d0622-3590">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="d0622-3590">Savings Account #</span></span> 
- <span data-ttu-id="d0622-3591">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3591">Savings Acct Number</span></span> 
- <span data-ttu-id="d0622-3592">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="d0622-3592">Savings Acct #</span></span> 
- <span data-ttu-id="d0622-3593">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="d0622-3593">Savings Acct No.</span></span> 
- <span data-ttu-id="d0622-3594">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="d0622-3594">Savings Account No.</span></span> 
- <span data-ttu-id="d0622-3595">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3595">Debit Account Number</span></span> 
- <span data-ttu-id="d0622-3596">Debit Account</span><span class="sxs-lookup"><span data-stu-id="d0622-3596">Debit Account</span></span> 
- <span data-ttu-id="d0622-3597">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="d0622-3597">Debit Account #</span></span> 
- <span data-ttu-id="d0622-3598">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="d0622-3598">Debit Acct Number</span></span> 
- <span data-ttu-id="d0622-3599">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="d0622-3599">Debit Acct #</span></span> 
- <span data-ttu-id="d0622-3600">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="d0622-3600">Debit Acct No.</span></span> 
- <span data-ttu-id="d0622-3601">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="d0622-3601">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="d0622-3602">미국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d0622-3602">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3603">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3603">Format</span></span>

<span data-ttu-id="d0622-3604">주마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3604">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3605">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3605">Pattern</span></span>

<span data-ttu-id="d0622-3606">주마다 다릅니다(예: 뉴욕).</span><span class="sxs-lookup"><span data-stu-id="d0622-3606">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="d0622-3607">Ddd ddd ddd와 같이 9 자리 숫자는 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3607">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="d0622-3608">Ddddddddd와 같은 9 자리 숫자가 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3608">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3609">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3609">Checksum</span></span>

<span data-ttu-id="d0622-3610">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3610">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3611">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3611">Definition</span></span>

<span data-ttu-id="d0622-3612">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3612">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3613">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3613">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3614">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3614">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="d0622-3615">Keyword_us_drivers_license에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3615">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="d0622-3616">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3616">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3617">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3617">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3618">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3618">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="d0622-3619">Keyword_us_drivers_license_abbreviations의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3619">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="d0622-3620">Keyword_us_drivers_license의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3620">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3621">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3621">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="d0622-3622">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="d0622-3622">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="d0622-3623">DL</span><span class="sxs-lookup"><span data-stu-id="d0622-3623">DL</span></span> 
- <span data-ttu-id="d0622-3624">된다</span><span class="sxs-lookup"><span data-stu-id="d0622-3624">DLS</span></span> 
- <span data-ttu-id="d0622-3625">CDL</span><span class="sxs-lookup"><span data-stu-id="d0622-3625">CDL</span></span> 
- <span data-ttu-id="d0622-3626">CDLS</span><span class="sxs-lookup"><span data-stu-id="d0622-3626">CDLS</span></span> 
- <span data-ttu-id="d0622-3627">ID</span><span class="sxs-lookup"><span data-stu-id="d0622-3627">ID</span></span> 
- <span data-ttu-id="d0622-3628">번호가</span><span class="sxs-lookup"><span data-stu-id="d0622-3628">IDs</span></span> 
- <span data-ttu-id="d0622-3629">DL #</span><span class="sxs-lookup"><span data-stu-id="d0622-3629">DL#</span></span> 
- <span data-ttu-id="d0622-3630">된다 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3630">DLS#</span></span> 
- <span data-ttu-id="d0622-3631">CDL #</span><span class="sxs-lookup"><span data-stu-id="d0622-3631">CDL#</span></span> 
- <span data-ttu-id="d0622-3632">CDLS #</span><span class="sxs-lookup"><span data-stu-id="d0622-3632">CDLS#</span></span> 
- <span data-ttu-id="d0622-3633">I #</span><span class="sxs-lookup"><span data-stu-id="d0622-3633">ID#</span></span>
- <span data-ttu-id="d0622-3634">번호가 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3634">IDs#</span></span> 
- <span data-ttu-id="d0622-3635">ID number</span><span class="sxs-lookup"><span data-stu-id="d0622-3635">ID number</span></span> 
- <span data-ttu-id="d0622-3636">ID numbers</span><span class="sxs-lookup"><span data-stu-id="d0622-3636">ID numbers</span></span> 
- <span data-ttu-id="d0622-3637">LIC</span><span class="sxs-lookup"><span data-stu-id="d0622-3637">LIC</span></span> 
- <span data-ttu-id="d0622-3638">LIC #</span><span class="sxs-lookup"><span data-stu-id="d0622-3638">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="d0622-3639">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="d0622-3639">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="d0622-3640">DriverLic</span><span class="sxs-lookup"><span data-stu-id="d0622-3640">DriverLic</span></span> 
- <span data-ttu-id="d0622-3641">DriverLics</span><span class="sxs-lookup"><span data-stu-id="d0622-3641">DriverLics</span></span> 
- <span data-ttu-id="d0622-3642">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="d0622-3642">DriverLicense</span></span> 
- <span data-ttu-id="d0622-3643">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="d0622-3643">DriverLicenses</span></span> 
- <span data-ttu-id="d0622-3644">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-3644">Driver Lic</span></span> 
- <span data-ttu-id="d0622-3645">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-3645">Driver Lics</span></span> 
- <span data-ttu-id="d0622-3646">Driver License</span><span class="sxs-lookup"><span data-stu-id="d0622-3646">Driver License</span></span> 
- <span data-ttu-id="d0622-3647">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-3647">Driver Licenses</span></span> 
- <span data-ttu-id="d0622-3648">DriversLic</span><span class="sxs-lookup"><span data-stu-id="d0622-3648">DriversLic</span></span> 
- <span data-ttu-id="d0622-3649">DriversLics</span><span class="sxs-lookup"><span data-stu-id="d0622-3649">DriversLics</span></span> 
- <span data-ttu-id="d0622-3650">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-3650">DriversLicense</span></span> 
- <span data-ttu-id="d0622-3651">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-3651">DriversLicenses</span></span> 
- <span data-ttu-id="d0622-3652">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-3652">Drivers Lic</span></span> 
- <span data-ttu-id="d0622-3653">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-3653">Drivers Lics</span></span> 
- <span data-ttu-id="d0622-3654">Drivers License</span><span class="sxs-lookup"><span data-stu-id="d0622-3654">Drivers License</span></span> 
- <span data-ttu-id="d0622-3655">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-3655">Drivers Licenses</span></span> 
- <span data-ttu-id="d0622-3656">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-3656">Driver'Lic</span></span> 
- <span data-ttu-id="d0622-3657">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-3657">Driver'Lics</span></span> 
- <span data-ttu-id="d0622-3658">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="d0622-3658">Driver'License</span></span> 
- <span data-ttu-id="d0622-3659">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-3659">Driver'Licenses</span></span> 
- <span data-ttu-id="d0622-3660">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-3660">Driver' Lic</span></span> 
- <span data-ttu-id="d0622-3661">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-3661">Driver' Lics</span></span> 
- <span data-ttu-id="d0622-3662">Driver' License</span><span class="sxs-lookup"><span data-stu-id="d0622-3662">Driver' License</span></span> 
- <span data-ttu-id="d0622-3663">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-3663">Driver' Licenses</span></span>
- <span data-ttu-id="d0622-3664">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="d0622-3664">Driver'sLic</span></span> 
- <span data-ttu-id="d0622-3665">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="d0622-3665">Driver'sLics</span></span> 
- <span data-ttu-id="d0622-3666">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="d0622-3666">Driver'sLicense</span></span> 
- <span data-ttu-id="d0622-3667">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="d0622-3667">Driver'sLicenses</span></span> 
- <span data-ttu-id="d0622-3668">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="d0622-3668">Driver's Lic</span></span> 
- <span data-ttu-id="d0622-3669">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="d0622-3669">Driver's Lics</span></span> 
- <span data-ttu-id="d0622-3670">Driver's License</span><span class="sxs-lookup"><span data-stu-id="d0622-3670">Driver's License</span></span> 
- <span data-ttu-id="d0622-3671">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="d0622-3671">Driver's Licenses</span></span> 
- <span data-ttu-id="d0622-3672">identification number</span><span class="sxs-lookup"><span data-stu-id="d0622-3672">identification number</span></span> 
- <span data-ttu-id="d0622-3673">identification numbers</span><span class="sxs-lookup"><span data-stu-id="d0622-3673">identification numbers</span></span> 
- <span data-ttu-id="d0622-3674">identification #</span><span class="sxs-lookup"><span data-stu-id="d0622-3674">identification #</span></span> 
- <span data-ttu-id="d0622-3675">id card</span><span class="sxs-lookup"><span data-stu-id="d0622-3675">id card</span></span> 
- <span data-ttu-id="d0622-3676">id cards</span><span class="sxs-lookup"><span data-stu-id="d0622-3676">id cards</span></span> 
- <span data-ttu-id="d0622-3677">identification card</span><span class="sxs-lookup"><span data-stu-id="d0622-3677">identification card</span></span> 
- <span data-ttu-id="d0622-3678">identification cards</span><span class="sxs-lookup"><span data-stu-id="d0622-3678">identification cards</span></span> 
- <span data-ttu-id="d0622-3679">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-3679">DriverLic#</span></span> 
- <span data-ttu-id="d0622-3680">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="d0622-3680">DriverLics#</span></span> 
- <span data-ttu-id="d0622-3681">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="d0622-3681">DriverLicense#</span></span> 
- <span data-ttu-id="d0622-3682">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-3682">DriverLicenses#</span></span> 
- <span data-ttu-id="d0622-3683">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-3683">Driver Lic#</span></span> 
- <span data-ttu-id="d0622-3684">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-3684">Driver Lics#</span></span> 
- <span data-ttu-id="d0622-3685">Driver License#</span><span class="sxs-lookup"><span data-stu-id="d0622-3685">Driver License#</span></span> 
- <span data-ttu-id="d0622-3686">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-3686">Driver Licenses#</span></span> 
- <span data-ttu-id="d0622-3687">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-3687">DriversLic#</span></span> 
- <span data-ttu-id="d0622-3688">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="d0622-3688">DriversLics#</span></span> 
- <span data-ttu-id="d0622-3689">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3689">DriversLicense#</span></span> 
- <span data-ttu-id="d0622-3690">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3690">DriversLicenses#</span></span> 
- <span data-ttu-id="d0622-3691">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-3691">Drivers Lic#</span></span> 
- <span data-ttu-id="d0622-3692">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-3692">Drivers Lics#</span></span> 
- <span data-ttu-id="d0622-3693">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="d0622-3693">Drivers License#</span></span> 
- <span data-ttu-id="d0622-3694">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-3694">Drivers Licenses#</span></span> 
- <span data-ttu-id="d0622-3695">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="d0622-3695">Driver'Lic#</span></span> 
- <span data-ttu-id="d0622-3696">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="d0622-3696">Driver'Lics#</span></span> 
- <span data-ttu-id="d0622-3697">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3697">Driver'License#</span></span> 
- <span data-ttu-id="d0622-3698">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-3698">Driver'Licenses#</span></span> 
- <span data-ttu-id="d0622-3699">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-3699">Driver' Lic#</span></span> 
- <span data-ttu-id="d0622-3700">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-3700">Driver' Lics#</span></span> 
- <span data-ttu-id="d0622-3701">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="d0622-3701">Driver' License#</span></span> 
- <span data-ttu-id="d0622-3702">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-3702">Driver' Licenses#</span></span> 
- <span data-ttu-id="d0622-3703">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="d0622-3703">Driver'sLic#</span></span> 
- <span data-ttu-id="d0622-3704">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="d0622-3704">Driver'sLics#</span></span> 
- <span data-ttu-id="d0622-3705">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="d0622-3705">Driver'sLicense#</span></span> 
- <span data-ttu-id="d0622-3706">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="d0622-3706">Driver'sLicenses#</span></span> 
- <span data-ttu-id="d0622-3707">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="d0622-3707">Driver's Lic#</span></span> 
- <span data-ttu-id="d0622-3708">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="d0622-3708">Driver's Lics#</span></span> 
- <span data-ttu-id="d0622-3709">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="d0622-3709">Driver's License#</span></span> 
- <span data-ttu-id="d0622-3710">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="d0622-3710">Driver's Licenses#</span></span> 
- <span data-ttu-id="d0622-3711">id card#</span><span class="sxs-lookup"><span data-stu-id="d0622-3711">id card#</span></span> 
- <span data-ttu-id="d0622-3712">id cards#</span><span class="sxs-lookup"><span data-stu-id="d0622-3712">id cards#</span></span> 
- <span data-ttu-id="d0622-3713">identification card#</span><span class="sxs-lookup"><span data-stu-id="d0622-3713">identification card#</span></span> 
- <span data-ttu-id="d0622-3714">identification cards#</span><span class="sxs-lookup"><span data-stu-id="d0622-3714">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="d0622-3715">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="d0622-3715">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="d0622-3716">주 약어(예: "NY")</span><span class="sxs-lookup"><span data-stu-id="d0622-3716">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="d0622-3717">주 이름(예: "New York")</span><span class="sxs-lookup"><span data-stu-id="d0622-3717">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="d0622-3718">미국 ITIN(개인 납세자 번호)</span><span class="sxs-lookup"><span data-stu-id="d0622-3718">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3719">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3719">Format</span></span>

<span data-ttu-id="d0622-3720">"9"로 시작되고, "7" 또는 "8"을 4번째 숫자로 포함하고, 경우에 따라 공백이나 대시로 서식이 지정된 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3720">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3721">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3721">Pattern</span></span>

<span data-ttu-id="d0622-3722">서식이</span><span class="sxs-lookup"><span data-stu-id="d0622-3722">Formatted:</span></span>
- <span data-ttu-id="d0622-3723">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3723">The digit "9"</span></span> 
- <span data-ttu-id="d0622-3724">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3724">Two digits</span></span> 
- <span data-ttu-id="d0622-3725">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="d0622-3725">A space or dash</span></span> 
- <span data-ttu-id="d0622-3726">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="d0622-3726">A "7" or "8"</span></span> 
- <span data-ttu-id="d0622-3727">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3727">A digit</span></span> 
- <span data-ttu-id="d0622-3728">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="d0622-3728">A space, or dash</span></span> 
- <span data-ttu-id="d0622-3729">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3729">Four digits</span></span>

<span data-ttu-id="d0622-3730">서식</span><span class="sxs-lookup"><span data-stu-id="d0622-3730">Unformatted:</span></span>
- <span data-ttu-id="d0622-3731">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3731">The digit "9"</span></span> 
- <span data-ttu-id="d0622-3732">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3732">Two digits</span></span> 
- <span data-ttu-id="d0622-3733">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="d0622-3733">A "7" or "8"</span></span> 
- <span data-ttu-id="d0622-3734">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3734">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3735">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3735">Checksum</span></span>

<span data-ttu-id="d0622-3736">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3736">No</span></span>

### <a name="definition"></a><span data-ttu-id="d0622-3737">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3737">Definition</span></span>

<span data-ttu-id="d0622-3738">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3738">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3739">Func_formatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3739">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3740">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3740">At least one of the following is true:</span></span>
    - <span data-ttu-id="d0622-3741">Keyword_itin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3741">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="d0622-3742">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3742">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="d0622-3743">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3743">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="d0622-3744">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3744">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="d0622-3745">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3745">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3746">Func_unformatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3746">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3747">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3747">At least one of the following is true:</span></span>
    - <span data-ttu-id="d0622-3748">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3748">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="d0622-3749">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3749">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="d0622-3750">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3750">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3751">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3751">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="d0622-3752">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="d0622-3752">Keyword_itin</span></span>

- <span data-ttu-id="d0622-3753">taxpayer</span><span class="sxs-lookup"><span data-stu-id="d0622-3753">taxpayer</span></span> 
- <span data-ttu-id="d0622-3754">tax id</span><span class="sxs-lookup"><span data-stu-id="d0622-3754">tax id</span></span> 
- <span data-ttu-id="d0622-3755">tax identification</span><span class="sxs-lookup"><span data-stu-id="d0622-3755">tax identification</span></span> 
- <span data-ttu-id="d0622-3756">itin</span><span class="sxs-lookup"><span data-stu-id="d0622-3756">itin</span></span> 
- <span data-ttu-id="d0622-3757">ssn</span><span class="sxs-lookup"><span data-stu-id="d0622-3757">ssn</span></span> 
- <span data-ttu-id="d0622-3758">언급</span><span class="sxs-lookup"><span data-stu-id="d0622-3758">tin</span></span> 
- <span data-ttu-id="d0622-3759">social security</span><span class="sxs-lookup"><span data-stu-id="d0622-3759">social security</span></span> 
- <span data-ttu-id="d0622-3760">tax payer</span><span class="sxs-lookup"><span data-stu-id="d0622-3760">tax payer</span></span> 
- <span data-ttu-id="d0622-3761">itins</span><span class="sxs-lookup"><span data-stu-id="d0622-3761">itins</span></span> 
- <span data-ttu-id="d0622-3762">taxid</span><span class="sxs-lookup"><span data-stu-id="d0622-3762">taxid</span></span> 
- <span data-ttu-id="d0622-3763">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="d0622-3763">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="d0622-3764">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="d0622-3764">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="d0622-3765">License</span><span class="sxs-lookup"><span data-stu-id="d0622-3765">License</span></span> 
- <span data-ttu-id="d0622-3766">DL</span><span class="sxs-lookup"><span data-stu-id="d0622-3766">DL</span></span> 
- <span data-ttu-id="d0622-3767">DOB</span><span class="sxs-lookup"><span data-stu-id="d0622-3767">DOB</span></span> 
- <span data-ttu-id="d0622-3768">생년월일</span><span class="sxs-lookup"><span data-stu-id="d0622-3768">Birthdate</span></span> 
- <span data-ttu-id="d0622-3769">생일</span><span class="sxs-lookup"><span data-stu-id="d0622-3769">Birthday</span></span> 
- <span data-ttu-id="d0622-3770">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="d0622-3770">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="d0622-3771">미국 SSN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="d0622-3771">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="d0622-3772">형식일</span><span class="sxs-lookup"><span data-stu-id="d0622-3772">Format</span></span>

<span data-ttu-id="d0622-3773">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="d0622-3773">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="d0622-3774">Mid가 2011 이전에 실행 된 경우 SSN은 특정 범위 내에서 번호의 특정 부분이 유효한 지 확인 하는 강력한 서식을 사용 해야 하지만 검사 값은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3774">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="d0622-3775">패턴</span><span class="sxs-lookup"><span data-stu-id="d0622-3775">Pattern</span></span>

<span data-ttu-id="d0622-3776">다음의 네 가지 패턴에서 SSNs를 검색 하는 함수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3776">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="d0622-3777">Func_ssn는 대시 또는 공백을 사용 하 여 서식이 지정 된 2011 이전의 고급 서식 (ddd-dd-dddd 또는 ddd dd dd)을 사용 하 여 SSNs를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3777">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="d0622-3778">Func_unformatted_ssn는 형식이 지정 되지 않은 2011 이전 형식으로 서식이 지정 된 SSNs를 찾습니다 (ddddddddd).</span><span class="sxs-lookup"><span data-stu-id="d0622-3778">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="d0622-3779">Func_randomized_formatted_ssn는 대시 또는 공백으로 서식이 지정 된 post-2011 SSNs를 찾습니다 (ddd-dd-dddd 또는 ddd dd dddd).</span><span class="sxs-lookup"><span data-stu-id="d0622-3779">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="d0622-3780">Func_randomized_unformatted_ssn는 형식 없는 2011 SSNs를 찾고, 서식이 없는 9 자리 숫자 (ddddddddd)를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3780">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="d0622-3781">제외</span><span class="sxs-lookup"><span data-stu-id="d0622-3781">Checksum</span></span>

<span data-ttu-id="d0622-3782">아니요</span><span class="sxs-lookup"><span data-stu-id="d0622-3782">No</span></span>


### <a name="definition"></a><span data-ttu-id="d0622-3783">정의</span><span class="sxs-lookup"><span data-stu-id="d0622-3783">Definition</span></span>

<span data-ttu-id="d0622-3784">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3785">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3785">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3786">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3786">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="d0622-3787">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3788">Func_unformatted_ssn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3788">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3789">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3789">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="d0622-3790">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3790">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3791">Func_randomized_formatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3791">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3792">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3792">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="d0622-3793">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3793">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="d0622-3794">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 55% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3794">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="d0622-3795">Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3795">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="d0622-3796">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3796">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="d0622-3797">Func_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0622-3797">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="d0622-3798">키워드</span><span class="sxs-lookup"><span data-stu-id="d0622-3798">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="d0622-3799">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="d0622-3799">Keyword_ssn</span></span>

- <span data-ttu-id="d0622-3800">Social Security</span><span class="sxs-lookup"><span data-stu-id="d0622-3800">Social Security</span></span> 
- <span data-ttu-id="d0622-3801">Social Security#</span><span class="sxs-lookup"><span data-stu-id="d0622-3801">Social Security#</span></span> 
- <span data-ttu-id="d0622-3802">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="d0622-3802">Soc Sec</span></span> 
- <span data-ttu-id="d0622-3803">SSN</span><span class="sxs-lookup"><span data-stu-id="d0622-3803">SSN</span></span> 
- <span data-ttu-id="d0622-3804">있는 SSN</span><span class="sxs-lookup"><span data-stu-id="d0622-3804">SSNS</span></span> 
- <span data-ttu-id="d0622-3805">SSN #</span><span class="sxs-lookup"><span data-stu-id="d0622-3805">SSN#</span></span> 
- <span data-ttu-id="d0622-3806">대비 #</span><span class="sxs-lookup"><span data-stu-id="d0622-3806">SS#</span></span> 
- <span data-ttu-id="d0622-3807">생길</span><span class="sxs-lookup"><span data-stu-id="d0622-3807">SSID</span></span> 
   

