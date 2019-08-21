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
ms.openlocfilehash: d486510c35aaf147e6d63e28d1df36ef689e3975
ms.sourcegitcommit: a5a7e43822336ed18d8f5879167766686cf6b2a3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2019
ms.locfileid: "36478257"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="eee87-104">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="eee87-104">What the sensitive information types look for</span></span>

<span data-ttu-id="eee87-105">Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 수 있는 중요 한 정보 유형이 많이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="eee87-106">이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="eee87-107">중요한 정보 유형은 정규식이나 함수로 식별될 수 있는 패턴으로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="eee87-108">또한 키워드 및 체크섬과 같은 확증적인 증거를 사용하여 중요한 정보 유형을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="eee87-109">이러한 평가 프로세스에서 신뢰 수준 및 근접성도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="eee87-110">ABA 라우팅 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-111">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-111">Format</span></span>

<span data-ttu-id="eee87-112">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-113">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-113">Pattern</span></span>

<span data-ttu-id="eee87-114">서식이</span><span class="sxs-lookup"><span data-stu-id="eee87-114">Formatted:</span></span>
- <span data-ttu-id="eee87-115">0, 1, 2, 3, 6, 7 또는 8로 시작하는 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="eee87-116">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-116">A hyphen</span></span>
- <span data-ttu-id="eee87-117">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-117">Four digits</span></span>
- <span data-ttu-id="eee87-118">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-118">A hyphen</span></span>
- <span data-ttu-id="eee87-119">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-119">A digit</span></span>

<span data-ttu-id="eee87-120">서식 없음: 0, 1, 2, 3, 6, 7 또는 8로 시작 하는 9 개의 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="eee87-121">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-121">Checksum</span></span>

<span data-ttu-id="eee87-122">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-123">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-123">Definition</span></span>

<span data-ttu-id="eee87-124">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-125">Func_aba_routing 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-126">Keyword_ABA_Routing의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```xml
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="eee87-127">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="eee87-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="eee87-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="eee87-129">aba</span><span class="sxs-lookup"><span data-stu-id="eee87-129">aba</span></span>
- <span data-ttu-id="eee87-130">aba #</span><span class="sxs-lookup"><span data-stu-id="eee87-130">aba #</span></span>
- <span data-ttu-id="eee87-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="eee87-131">aba routing #</span></span>
- <span data-ttu-id="eee87-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="eee87-132">aba routing number</span></span>
- <span data-ttu-id="eee87-133">aba #</span><span class="sxs-lookup"><span data-stu-id="eee87-133">aba#</span></span>
- <span data-ttu-id="eee87-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="eee87-134">abarouting#</span></span>
- <span data-ttu-id="eee87-135">aba number</span><span class="sxs-lookup"><span data-stu-id="eee87-135">aba number</span></span>
- <span data-ttu-id="eee87-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-136">abaroutingnumber</span></span>
- <span data-ttu-id="eee87-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="eee87-137">american bank association routing #</span></span>
- <span data-ttu-id="eee87-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="eee87-138">american bank association routing number</span></span>
- <span data-ttu-id="eee87-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="eee87-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="eee87-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="eee87-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="eee87-141">bank routing number</span></span>
- <span data-ttu-id="eee87-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="eee87-142">bankrouting#</span></span>
- <span data-ttu-id="eee87-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-143">bankroutingnumber</span></span>
- <span data-ttu-id="eee87-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="eee87-144">routing transit number</span></span>
- <span data-ttu-id="eee87-145">RTN</span><span class="sxs-lookup"><span data-stu-id="eee87-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="eee87-146">아르헨티나 국가 ID(DNI) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-147">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-147">Format</span></span>

<span data-ttu-id="eee87-148">마침표로 구분된 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-149">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-149">Pattern</span></span>

<span data-ttu-id="eee87-150">8자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-150">Eight digits:</span></span>
- <span data-ttu-id="eee87-151">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-151">Two digits</span></span>
- <span data-ttu-id="eee87-152">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-152">A period</span></span>
- <span data-ttu-id="eee87-153">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-153">Three digits</span></span>
- <span data-ttu-id="eee87-154">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-154">A period</span></span>
- <span data-ttu-id="eee87-155">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-156">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-156">Checksum</span></span>

<span data-ttu-id="eee87-157">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-158">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-158">Definition</span></span>

<span data-ttu-id="eee87-159">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-160">정규식 Regex_argentina_national_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-161">Keyword_argentina_national_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-162">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="eee87-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="eee87-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="eee87-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="eee87-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="eee87-165">ID</span><span class="sxs-lookup"><span data-stu-id="eee87-165">Identity</span></span> 
- <span data-ttu-id="eee87-166">식별 국가 Id 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="eee87-167">DNI</span><span class="sxs-lookup"><span data-stu-id="eee87-167">DNI</span></span> 
- <span data-ttu-id="eee87-168">개인의 NIC 국내 레지스트리</span><span class="sxs-lookup"><span data-stu-id="eee87-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="eee87-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="eee87-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="eee87-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="eee87-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="eee87-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="eee87-171">Identidad</span></span> 
- <span data-ttu-id="eee87-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="eee87-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="eee87-173">호주 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-174">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-174">Format</span></span>

<span data-ttu-id="eee87-175">6-10자리 숫자(은행 지점 번호 포함 또는 제외)</span><span class="sxs-lookup"><span data-stu-id="eee87-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-176">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-176">Pattern</span></span>

<span data-ttu-id="eee87-177">계좌 번호는 6-10자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="eee87-178">호주 은행 지점 번호:</span><span class="sxs-lookup"><span data-stu-id="eee87-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="eee87-179">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-179">Three digits</span></span> 
- <span data-ttu-id="eee87-180">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-180">A hyphen</span></span> 
- <span data-ttu-id="eee87-181">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-182">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-182">Checksum</span></span>

<span data-ttu-id="eee87-183">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-184">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-184">Definition</span></span>

<span data-ttu-id="eee87-185">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-186">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="eee87-187">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="eee87-188">Regex_australia_bank_account_number_bsb 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="eee87-189">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-190">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="eee87-191">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-192">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="eee87-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="eee87-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="eee87-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="eee87-194">swift bank code</span></span>
- <span data-ttu-id="eee87-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="eee87-195">correspondent bank</span></span>
- <span data-ttu-id="eee87-196">base currency</span><span class="sxs-lookup"><span data-stu-id="eee87-196">base currency</span></span>
- <span data-ttu-id="eee87-197">usa account</span><span class="sxs-lookup"><span data-stu-id="eee87-197">usa account</span></span>
- <span data-ttu-id="eee87-198">holder address</span><span class="sxs-lookup"><span data-stu-id="eee87-198">holder address</span></span>
- <span data-ttu-id="eee87-199">bank address</span><span class="sxs-lookup"><span data-stu-id="eee87-199">bank address</span></span>
- <span data-ttu-id="eee87-200">information account</span><span class="sxs-lookup"><span data-stu-id="eee87-200">information account</span></span>
- <span data-ttu-id="eee87-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="eee87-201">fund transfers</span></span>
- <span data-ttu-id="eee87-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="eee87-202">bank charges</span></span>
- <span data-ttu-id="eee87-203">bank details</span><span class="sxs-lookup"><span data-stu-id="eee87-203">bank details</span></span>
- <span data-ttu-id="eee87-204">banking information</span><span class="sxs-lookup"><span data-stu-id="eee87-204">banking information</span></span>
- <span data-ttu-id="eee87-205">full names</span><span class="sxs-lookup"><span data-stu-id="eee87-205">full names</span></span>
- <span data-ttu-id="eee87-206">iaea</span><span class="sxs-lookup"><span data-stu-id="eee87-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="eee87-207">호주 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-208">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-208">Format</span></span>

<span data-ttu-id="eee87-209">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-210">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-210">Pattern</span></span>

<span data-ttu-id="eee87-211">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="eee87-212">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-213">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-213">Two digits</span></span> 
- <span data-ttu-id="eee87-214">5자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="eee87-215">또는</span><span class="sxs-lookup"><span data-stu-id="eee87-215">OR</span></span>

- <span data-ttu-id="eee87-216">1-2개의 선택적 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-217">4-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-217">4-9 digits</span></span>

<span data-ttu-id="eee87-218">또는</span><span class="sxs-lookup"><span data-stu-id="eee87-218">OR</span></span>

- <span data-ttu-id="eee87-219">9자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-220">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-220">Checksum</span></span>

<span data-ttu-id="eee87-221">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-222">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-222">Definition</span></span>

<span data-ttu-id="eee87-223">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-224">Regex_australia_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-225">Keyword_australia_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="eee87-226">Keyword_australia_drivers_license_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-227">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="eee87-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="eee87-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="eee87-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="eee87-229">international driving permits</span></span>
- <span data-ttu-id="eee87-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="eee87-230">australian automobile association</span></span>
- <span data-ttu-id="eee87-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="eee87-231">international driving permit</span></span>
- <span data-ttu-id="eee87-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="eee87-232">DriverLicence</span></span>
- <span data-ttu-id="eee87-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="eee87-233">DriverLicences</span></span>
- <span data-ttu-id="eee87-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-234">Driver Lic</span></span>
- <span data-ttu-id="eee87-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-235">Driver Licence</span></span>
- <span data-ttu-id="eee87-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-236">Driver Licences</span></span>
- <span data-ttu-id="eee87-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="eee87-237">DriversLic</span></span>
- <span data-ttu-id="eee87-238">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-238">DriversLicence</span></span>
- <span data-ttu-id="eee87-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="eee87-239">DriversLicences</span></span>
- <span data-ttu-id="eee87-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-240">Drivers Lic</span></span>
- <span data-ttu-id="eee87-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-241">Drivers Lics</span></span>
- <span data-ttu-id="eee87-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-242">Drivers Licence</span></span>
- <span data-ttu-id="eee87-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-243">Drivers Licences</span></span>
- <span data-ttu-id="eee87-244">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-244">Driver'Lic</span></span>
- <span data-ttu-id="eee87-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-245">Driver'Lics</span></span>
- <span data-ttu-id="eee87-246">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-246">Driver'Licence</span></span>
- <span data-ttu-id="eee87-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-247">Driver'Licences</span></span>
- <span data-ttu-id="eee87-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-248">Driver' Lic</span></span>
- <span data-ttu-id="eee87-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-249">Driver' Lics</span></span>
- <span data-ttu-id="eee87-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-250">Driver' Licence</span></span>
- <span data-ttu-id="eee87-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-251">Driver' Licences</span></span>
- <span data-ttu-id="eee87-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="eee87-252">Driver'sLic</span></span>
- <span data-ttu-id="eee87-253">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="eee87-253">Driver'sLics</span></span>
- <span data-ttu-id="eee87-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="eee87-254">Driver'sLicence</span></span>
- <span data-ttu-id="eee87-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="eee87-255">Driver'sLicences</span></span>
- <span data-ttu-id="eee87-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-256">Driver's Lic</span></span>
- <span data-ttu-id="eee87-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-257">Driver's Lics</span></span>
- <span data-ttu-id="eee87-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-258">Driver's Licence</span></span>
- <span data-ttu-id="eee87-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-259">Driver's Licences</span></span>
- <span data-ttu-id="eee87-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-260">DriverLic#</span></span>
- <span data-ttu-id="eee87-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="eee87-261">DriverLics#</span></span>
- <span data-ttu-id="eee87-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="eee87-262">DriverLicence#</span></span>
- <span data-ttu-id="eee87-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="eee87-263">DriverLicences#</span></span>
- <span data-ttu-id="eee87-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-264">Driver Lic#</span></span>
- <span data-ttu-id="eee87-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-265">Driver Lics#</span></span>
- <span data-ttu-id="eee87-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="eee87-266">Driver Licence#</span></span>
- <span data-ttu-id="eee87-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="eee87-267">Driver Licences#</span></span>
- <span data-ttu-id="eee87-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-268">DriversLic#</span></span>
- <span data-ttu-id="eee87-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="eee87-269">DriversLics#</span></span>
- <span data-ttu-id="eee87-270">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-270">DriversLicence#</span></span>
- <span data-ttu-id="eee87-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="eee87-271">DriversLicences#</span></span>
- <span data-ttu-id="eee87-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-272">Drivers Lic#</span></span>
- <span data-ttu-id="eee87-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-273">Drivers Lics#</span></span>
- <span data-ttu-id="eee87-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="eee87-274">Drivers Licence#</span></span>
- <span data-ttu-id="eee87-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="eee87-275">Drivers Licences#</span></span>
- <span data-ttu-id="eee87-276">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="eee87-276">Driver'Lic#</span></span>
- <span data-ttu-id="eee87-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="eee87-277">Driver'Lics#</span></span>
- <span data-ttu-id="eee87-278">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-278">Driver'Licence#</span></span>
- <span data-ttu-id="eee87-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="eee87-279">Driver'Licences#</span></span>
- <span data-ttu-id="eee87-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-280">Driver' Lic#</span></span>
- <span data-ttu-id="eee87-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-281">Driver' Lics#</span></span>
- <span data-ttu-id="eee87-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="eee87-282">Driver' Licence#</span></span>
- <span data-ttu-id="eee87-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="eee87-283">Driver' Licences#</span></span>
- <span data-ttu-id="eee87-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-284">Driver'sLic#</span></span>
- <span data-ttu-id="eee87-285">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="eee87-285">Driver'sLics#</span></span>
- <span data-ttu-id="eee87-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="eee87-286">Driver'sLicence#</span></span>
- <span data-ttu-id="eee87-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="eee87-287">Driver'sLicences#</span></span>
- <span data-ttu-id="eee87-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-288">Driver's Lic#</span></span>
- <span data-ttu-id="eee87-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-289">Driver's Lics#</span></span>
- <span data-ttu-id="eee87-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="eee87-290">Driver's Licence#</span></span>
- <span data-ttu-id="eee87-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="eee87-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="eee87-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="eee87-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="eee87-293">aaa</span><span class="sxs-lookup"><span data-stu-id="eee87-293">aaa</span></span>
- <span data-ttu-id="eee87-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="eee87-294">DriverLicense</span></span>
- <span data-ttu-id="eee87-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="eee87-295">DriverLicenses</span></span>
- <span data-ttu-id="eee87-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="eee87-296">Driver License</span></span>
- <span data-ttu-id="eee87-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-297">Driver Licenses</span></span>
- <span data-ttu-id="eee87-298">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-298">DriversLicense</span></span>
- <span data-ttu-id="eee87-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-299">DriversLicenses</span></span>
- <span data-ttu-id="eee87-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="eee87-300">Drivers License</span></span>
- <span data-ttu-id="eee87-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-301">Drivers Licenses</span></span>
- <span data-ttu-id="eee87-302">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-302">Driver'License</span></span>
- <span data-ttu-id="eee87-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-303">Driver'Licenses</span></span>
- <span data-ttu-id="eee87-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="eee87-304">Driver' License</span></span>
- <span data-ttu-id="eee87-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-305">Driver' Licenses</span></span>
- <span data-ttu-id="eee87-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="eee87-306">Driver'sLicense</span></span>
- <span data-ttu-id="eee87-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="eee87-307">Driver'sLicenses</span></span>
- <span data-ttu-id="eee87-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="eee87-308">Driver's License</span></span>
- <span data-ttu-id="eee87-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-309">Driver's Licenses</span></span>
- <span data-ttu-id="eee87-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="eee87-310">DriverLicense#</span></span>
- <span data-ttu-id="eee87-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-311">DriverLicenses#</span></span>
- <span data-ttu-id="eee87-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="eee87-312">Driver License#</span></span>
- <span data-ttu-id="eee87-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-313">Driver Licenses#</span></span>
- <span data-ttu-id="eee87-314">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-314">DriversLicense#</span></span>
- <span data-ttu-id="eee87-315">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-315">DriversLicenses#</span></span>
- <span data-ttu-id="eee87-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="eee87-316">Drivers License#</span></span>
- <span data-ttu-id="eee87-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-317">Drivers Licenses#</span></span>
- <span data-ttu-id="eee87-318">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-318">Driver'License#</span></span>
- <span data-ttu-id="eee87-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-319">Driver'Licenses#</span></span>
- <span data-ttu-id="eee87-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="eee87-320">Driver' License#</span></span>
- <span data-ttu-id="eee87-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-321">Driver' Licenses#</span></span>
- <span data-ttu-id="eee87-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="eee87-322">Driver'sLicense#</span></span>
- <span data-ttu-id="eee87-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="eee87-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="eee87-324">Driver's License#</span></span>
- <span data-ttu-id="eee87-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="eee87-326">호주 의료 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-327">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-327">Format</span></span>

<span data-ttu-id="eee87-328">10-11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-329">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-329">Pattern</span></span>

<span data-ttu-id="eee87-330">10-11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-330">10-11 digits:</span></span>
- <span data-ttu-id="eee87-331">첫 번째 숫자는 2-6 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="eee87-332">9번째 숫자는 검사 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="eee87-333">10번째 숫자는 문제 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="eee87-334">11번째 숫자(선택 사항)는 개인 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-335">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-335">Checksum</span></span>

<span data-ttu-id="eee87-336">예</span><span class="sxs-lookup"><span data-stu-id="eee87-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-337">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-337">Definition</span></span>

<span data-ttu-id="eee87-338">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-339">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-340">Keyword_Australia_Medical_Account_Number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="eee87-341">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-341">The checksum passes.</span></span>

<span data-ttu-id="eee87-342">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-343">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-344">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-344">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-345">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="eee87-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="eee87-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="eee87-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="eee87-347">bank account details</span></span>
- <span data-ttu-id="eee87-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="eee87-348">medicare payments</span></span>
- <span data-ttu-id="eee87-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="eee87-349">mortgage account</span></span>
- <span data-ttu-id="eee87-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="eee87-350">bank payments</span></span>
- <span data-ttu-id="eee87-351">information branch</span><span class="sxs-lookup"><span data-stu-id="eee87-351">information branch</span></span>
- <span data-ttu-id="eee87-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="eee87-352">credit card loan</span></span>
- <span data-ttu-id="eee87-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="eee87-353">department of human services</span></span>
- <span data-ttu-id="eee87-354">local service</span><span class="sxs-lookup"><span data-stu-id="eee87-354">local service</span></span>
- <span data-ttu-id="eee87-355">medicare</span><span class="sxs-lookup"><span data-stu-id="eee87-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="eee87-356">호주 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-357">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-357">Format</span></span>

<span data-ttu-id="eee87-358">문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-359">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-359">Pattern</span></span>

<span data-ttu-id="eee87-360">1개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-361">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-361">Checksum</span></span>

<span data-ttu-id="eee87-362">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-363">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-363">Definition</span></span>

<span data-ttu-id="eee87-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-365">Regex_australia_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-366">Keyword_passport 또는 Keyword_australia_passport_number의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-367">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="eee87-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-368">Keyword_passport</span></span>

- <span data-ttu-id="eee87-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="eee87-369">Passport Number</span></span>
- <span data-ttu-id="eee87-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="eee87-370">Passport No</span></span>
- <span data-ttu-id="eee87-371">Passport #</span><span class="sxs-lookup"><span data-stu-id="eee87-371">Passport #</span></span>
- <span data-ttu-id="eee87-372">여권 #</span><span class="sxs-lookup"><span data-stu-id="eee87-372">Passport#</span></span>
- <span data-ttu-id="eee87-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="eee87-373">PassportID</span></span>
- <span data-ttu-id="eee87-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="eee87-374">Passportno</span></span>
- <span data-ttu-id="eee87-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-375">passportnumber</span></span>
- <span data-ttu-id="eee87-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="eee87-376">パスポート</span></span>
- <span data-ttu-id="eee87-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="eee87-377">パスポート番号</span></span>
- <span data-ttu-id="eee87-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="eee87-378">パスポートのNum</span></span>
- <span data-ttu-id="eee87-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="eee87-379">パスポート ＃</span></span> 
- <span data-ttu-id="eee87-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="eee87-380">Numéro de passeport</span></span>
- <span data-ttu-id="eee87-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="eee87-381">Passeport n °</span></span>
- <span data-ttu-id="eee87-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="eee87-382">Passeport Non</span></span>
- <span data-ttu-id="eee87-383">Passeport #</span><span class="sxs-lookup"><span data-stu-id="eee87-383">Passeport #</span></span>
- <span data-ttu-id="eee87-384">포트 #</span><span class="sxs-lookup"><span data-stu-id="eee87-384">Passeport#</span></span>
- <span data-ttu-id="eee87-385">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="eee87-385">PasseportNon</span></span>
- <span data-ttu-id="eee87-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="eee87-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="eee87-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="eee87-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="eee87-388">여권</span><span class="sxs-lookup"><span data-stu-id="eee87-388">passport</span></span>
- <span data-ttu-id="eee87-389">passport details</span><span class="sxs-lookup"><span data-stu-id="eee87-389">passport details</span></span>
- <span data-ttu-id="eee87-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="eee87-390">immigration and citizenship</span></span>
- <span data-ttu-id="eee87-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="eee87-391">commonwealth of australia</span></span>
- <span data-ttu-id="eee87-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="eee87-392">department of immigration</span></span>
- <span data-ttu-id="eee87-393">residential address</span><span class="sxs-lookup"><span data-stu-id="eee87-393">residential address</span></span>
- <span data-ttu-id="eee87-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="eee87-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="eee87-395">visa</span><span class="sxs-lookup"><span data-stu-id="eee87-395">visa</span></span>
- <span data-ttu-id="eee87-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="eee87-396">national identity card</span></span>
- <span data-ttu-id="eee87-397">passport number</span><span class="sxs-lookup"><span data-stu-id="eee87-397">passport number</span></span>
- <span data-ttu-id="eee87-398">travel document</span><span class="sxs-lookup"><span data-stu-id="eee87-398">travel document</span></span>
- <span data-ttu-id="eee87-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="eee87-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="eee87-400">호주 세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-401">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-401">Format</span></span>

<span data-ttu-id="eee87-402">8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-403">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-403">Pattern</span></span>

<span data-ttu-id="eee87-404">일반적으로 다음과 같이 공백과 함께 표시되는 8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="eee87-405">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-405">Three digits</span></span> 
- <span data-ttu-id="eee87-406">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-406">An optional space</span></span> 
- <span data-ttu-id="eee87-407">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-407">Three digits</span></span> 
- <span data-ttu-id="eee87-408">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-408">An optional space</span></span> 
- <span data-ttu-id="eee87-409">마지막 숫자가 검사 숫자인 2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-410">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-410">Checksum</span></span>

<span data-ttu-id="eee87-411">예</span><span class="sxs-lookup"><span data-stu-id="eee87-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-412">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-412">Definition</span></span>

<span data-ttu-id="eee87-413">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-414">Func_australian_tax_file_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-415">Keyword_Australia_Tax_File_Number 또는 Keyword_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="eee87-416">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-416">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-417">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="eee87-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="eee87-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="eee87-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="eee87-419">australian business number</span></span>
- <span data-ttu-id="eee87-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="eee87-420">marginal tax rate</span></span>
- <span data-ttu-id="eee87-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="eee87-421">medicare levy</span></span>
- <span data-ttu-id="eee87-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="eee87-422">portfolio number</span></span>
- <span data-ttu-id="eee87-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="eee87-423">service veterans</span></span>
- <span data-ttu-id="eee87-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="eee87-424">withholding tax</span></span>
- <span data-ttu-id="eee87-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="eee87-425">individual tax return</span></span>
- <span data-ttu-id="eee87-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="eee87-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="eee87-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="eee87-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="eee87-428">00000000</span><span class="sxs-lookup"><span data-stu-id="eee87-428">00000000</span></span>
- <span data-ttu-id="eee87-429">11111111</span><span class="sxs-lookup"><span data-stu-id="eee87-429">11111111</span></span>
- <span data-ttu-id="eee87-430">22222222</span><span class="sxs-lookup"><span data-stu-id="eee87-430">22222222</span></span>
- <span data-ttu-id="eee87-431">33333333</span><span class="sxs-lookup"><span data-stu-id="eee87-431">33333333</span></span>
- <span data-ttu-id="eee87-432">44444444</span><span class="sxs-lookup"><span data-stu-id="eee87-432">44444444</span></span>
- <span data-ttu-id="eee87-433">55555555</span><span class="sxs-lookup"><span data-stu-id="eee87-433">55555555</span></span>
- <span data-ttu-id="eee87-434">66666666</span><span class="sxs-lookup"><span data-stu-id="eee87-434">66666666</span></span>
- <span data-ttu-id="eee87-435">77777777</span><span class="sxs-lookup"><span data-stu-id="eee87-435">77777777</span></span>
- <span data-ttu-id="eee87-436">88888888</span><span class="sxs-lookup"><span data-stu-id="eee87-436">88888888</span></span>
- <span data-ttu-id="eee87-437">99999999</span><span class="sxs-lookup"><span data-stu-id="eee87-437">99999999</span></span>
- <span data-ttu-id="eee87-438">000000000</span><span class="sxs-lookup"><span data-stu-id="eee87-438">000000000</span></span>
- <span data-ttu-id="eee87-439">111111111</span><span class="sxs-lookup"><span data-stu-id="eee87-439">111111111</span></span>
- <span data-ttu-id="eee87-440">222222222</span><span class="sxs-lookup"><span data-stu-id="eee87-440">222222222</span></span>
- <span data-ttu-id="eee87-441">333333333</span><span class="sxs-lookup"><span data-stu-id="eee87-441">333333333</span></span>
- <span data-ttu-id="eee87-442">444444444</span><span class="sxs-lookup"><span data-stu-id="eee87-442">444444444</span></span>
- <span data-ttu-id="eee87-443">555555555</span><span class="sxs-lookup"><span data-stu-id="eee87-443">555555555</span></span>
- <span data-ttu-id="eee87-444">666666666</span><span class="sxs-lookup"><span data-stu-id="eee87-444">666666666</span></span>
- <span data-ttu-id="eee87-445">777777777</span><span class="sxs-lookup"><span data-stu-id="eee87-445">777777777</span></span>
- <span data-ttu-id="eee87-446">888888888</span><span class="sxs-lookup"><span data-stu-id="eee87-446">888888888</span></span>
- <span data-ttu-id="eee87-447">999999999</span><span class="sxs-lookup"><span data-stu-id="eee87-447">999999999</span></span>
- <span data-ttu-id="eee87-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="eee87-448">0000000000</span></span>
- <span data-ttu-id="eee87-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="eee87-449">1111111111</span></span>
- <span data-ttu-id="eee87-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="eee87-450">2222222222</span></span>
- <span data-ttu-id="eee87-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="eee87-451">3333333333</span></span>
- <span data-ttu-id="eee87-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="eee87-452">4444444444</span></span>
- <span data-ttu-id="eee87-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="eee87-453">5555555555</span></span>
- <span data-ttu-id="eee87-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="eee87-454">6666666666</span></span>
- <span data-ttu-id="eee87-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="eee87-455">7777777777</span></span>
- <span data-ttu-id="eee87-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="eee87-456">8888888888</span></span>
- <span data-ttu-id="eee87-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="eee87-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="eee87-458">Azure DocumentDB 인증 키</span><span class="sxs-lookup"><span data-stu-id="eee87-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="eee87-459">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-459">Format</span></span>

<span data-ttu-id="eee87-460">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "DocumentDb" 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-461">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-461">Pattern</span></span>

- <span data-ttu-id="eee87-462">"DocumentDb" 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="eee87-463">3-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-464">보다 큼 기호 (>), 등호 (=), 따옴표 (") 또는 아포스트로피 (')</span><span class="sxs-lookup"><span data-stu-id="eee87-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="eee87-465">86의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="eee87-466">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-467">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-467">Checksum</span></span>

<span data-ttu-id="eee87-468">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-469">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-469">Definition</span></span>

<span data-ttu-id="eee87-470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-471">정규식 CEP_Regex_AzureDocumentDBAuthKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-472">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-473">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="eee87-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="eee87-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="eee87-475">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-476">극동</span><span class="sxs-lookup"><span data-stu-id="eee87-476">contoso</span></span>
- <span data-ttu-id="eee87-477">fabrikam</span><span class="sxs-lookup"><span data-stu-id="eee87-477">fabrikam</span></span>
- <span data-ttu-id="eee87-478">대양</span><span class="sxs-lookup"><span data-stu-id="eee87-478">northwind</span></span>
- <span data-ttu-id="eee87-479">샌드박스</span><span class="sxs-lookup"><span data-stu-id="eee87-479">sandbox</span></span>
- <span data-ttu-id="eee87-480">용 onebox</span><span class="sxs-lookup"><span data-stu-id="eee87-480">onebox</span></span>
- <span data-ttu-id="eee87-481">로컬</span><span class="sxs-lookup"><span data-stu-id="eee87-481">localhost</span></span>
- <span data-ttu-id="eee87-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="eee87-482">127.0.0.1</span></span>
- <span data-ttu-id="eee87-483">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-484">ccw</span><span class="sxs-lookup"><span data-stu-id="eee87-484">com</span></span>
- <span data-ttu-id="eee87-485">s-int</span><span class="sxs-lookup"><span data-stu-id="eee87-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-486">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="eee87-487">Azure IAAS 데이터베이스 연결 문자열 및 Azure SQL 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="eee87-488">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-488">Format</span></span>

<span data-ttu-id="eee87-489">"Server", "server" 또는 "data source" 라는 문자열은 "cloudapp. azure"를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-490">com "또는" cloudapp.</span><span class="sxs-lookup"><span data-stu-id="eee87-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-491">net "또는" 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="eee87-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-492">net "과 문자열" Password "또는" password "또는" pwd "가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-493">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-493">Pattern</span></span>

- <span data-ttu-id="eee87-494">문자열 "Server", "Server" 또는 "data source"</span><span class="sxs-lookup"><span data-stu-id="eee87-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="eee87-495">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-496">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-496">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-497">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-498">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-499">문자열 "cloudapp.</span><span class="sxs-lookup"><span data-stu-id="eee87-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-500">com "," cloudapp.</span><span class="sxs-lookup"><span data-stu-id="eee87-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-501">net "또는" database.</span><span class="sxs-lookup"><span data-stu-id="eee87-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-502">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-502">net"</span></span>
- <span data-ttu-id="eee87-503">1-300에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-504">문자열 "Password", "password" 또는 "pwd"</span><span class="sxs-lookup"><span data-stu-id="eee87-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="eee87-505">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-506">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-506">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-507">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-508">세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')가 아닌 하나 이상의 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="eee87-509">세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')</span><span class="sxs-lookup"><span data-stu-id="eee87-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-510">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-510">Checksum</span></span>

<span data-ttu-id="eee87-511">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-512">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-512">Definition</span></span>

<span data-ttu-id="eee87-513">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-514">정규식 CEP_Regex_AzureConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-515">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-516">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="eee87-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="eee87-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="eee87-518">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-519">극동</span><span class="sxs-lookup"><span data-stu-id="eee87-519">contoso</span></span>
- <span data-ttu-id="eee87-520">fabrikam</span><span class="sxs-lookup"><span data-stu-id="eee87-520">fabrikam</span></span>
- <span data-ttu-id="eee87-521">대양</span><span class="sxs-lookup"><span data-stu-id="eee87-521">northwind</span></span>
- <span data-ttu-id="eee87-522">샌드박스</span><span class="sxs-lookup"><span data-stu-id="eee87-522">sandbox</span></span>
- <span data-ttu-id="eee87-523">용 onebox</span><span class="sxs-lookup"><span data-stu-id="eee87-523">onebox</span></span>
- <span data-ttu-id="eee87-524">로컬</span><span class="sxs-lookup"><span data-stu-id="eee87-524">localhost</span></span>
- <span data-ttu-id="eee87-525">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="eee87-525">127.0.0.1</span></span>
- <span data-ttu-id="eee87-526">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-527">ccw</span><span class="sxs-lookup"><span data-stu-id="eee87-527">com</span></span>
- <span data-ttu-id="eee87-528">s-int</span><span class="sxs-lookup"><span data-stu-id="eee87-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-529">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="eee87-530">Azure IoT Connection 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="eee87-531">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-531">Format</span></span>

<span data-ttu-id="eee87-532">문자열 "HostName" 뒤에 "azure-devices" 라는 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-533">net "및" SharedAccessKey "</span><span class="sxs-lookup"><span data-stu-id="eee87-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-534">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-534">Pattern</span></span>

- <span data-ttu-id="eee87-535">문자열 "HostName"</span><span class="sxs-lookup"><span data-stu-id="eee87-535">The string "HostName"</span></span>
- <span data-ttu-id="eee87-536">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-537">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-537">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-538">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-539">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-540">문자열 "azure-장치</span><span class="sxs-lookup"><span data-stu-id="eee87-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-541">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-541">net"</span></span>
- <span data-ttu-id="eee87-542">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-543">"SharedAccessKey" 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="eee87-544">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-545">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-545">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-546">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-547">43의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="eee87-548">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-549">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-549">Checksum</span></span>

<span data-ttu-id="eee87-550">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-551">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-551">Definition</span></span>

<span data-ttu-id="eee87-552">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-553">정규식 CEP_Regex_AzureIoTConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-554">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-555">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="eee87-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="eee87-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="eee87-557">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-558">극동</span><span class="sxs-lookup"><span data-stu-id="eee87-558">contoso</span></span>
- <span data-ttu-id="eee87-559">fabrikam</span><span class="sxs-lookup"><span data-stu-id="eee87-559">fabrikam</span></span>
- <span data-ttu-id="eee87-560">대양</span><span class="sxs-lookup"><span data-stu-id="eee87-560">northwind</span></span>
- <span data-ttu-id="eee87-561">샌드박스</span><span class="sxs-lookup"><span data-stu-id="eee87-561">sandbox</span></span>
- <span data-ttu-id="eee87-562">용 onebox</span><span class="sxs-lookup"><span data-stu-id="eee87-562">onebox</span></span>
- <span data-ttu-id="eee87-563">로컬</span><span class="sxs-lookup"><span data-stu-id="eee87-563">localhost</span></span>
- <span data-ttu-id="eee87-564">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="eee87-564">127.0.0.1</span></span>
- <span data-ttu-id="eee87-565">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-566">ccw</span><span class="sxs-lookup"><span data-stu-id="eee87-566">com</span></span>
- <span data-ttu-id="eee87-567">s-int</span><span class="sxs-lookup"><span data-stu-id="eee87-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-568">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="eee87-569">Azure 게시 설정 암호</span><span class="sxs-lookup"><span data-stu-id="eee87-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="eee87-570">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-570">Format</span></span>

<span data-ttu-id="eee87-571">문자열 "userpwd =" 다음에 영숫자 문자열이 나옵니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-572">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-572">Pattern</span></span>

- <span data-ttu-id="eee87-573">문자열 "userpwd ="</span><span class="sxs-lookup"><span data-stu-id="eee87-573">The string "userpwd="</span></span>
- <span data-ttu-id="eee87-574">60 대 문자와 숫자의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="eee87-575">큰따옴표 (")</span><span class="sxs-lookup"><span data-stu-id="eee87-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-576">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-576">Checksum</span></span>

<span data-ttu-id="eee87-577">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-578">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-578">Definition</span></span>

<span data-ttu-id="eee87-579">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-580">정규식 CEP_Regex_AzurePublishSettingPasswords 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-581">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-582">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="eee87-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="eee87-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="eee87-584">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-585">극동</span><span class="sxs-lookup"><span data-stu-id="eee87-585">contoso</span></span>
- <span data-ttu-id="eee87-586">fabrikam</span><span class="sxs-lookup"><span data-stu-id="eee87-586">fabrikam</span></span>
- <span data-ttu-id="eee87-587">대양</span><span class="sxs-lookup"><span data-stu-id="eee87-587">northwind</span></span>
- <span data-ttu-id="eee87-588">샌드박스</span><span class="sxs-lookup"><span data-stu-id="eee87-588">sandbox</span></span>
- <span data-ttu-id="eee87-589">용 onebox</span><span class="sxs-lookup"><span data-stu-id="eee87-589">onebox</span></span>
- <span data-ttu-id="eee87-590">로컬</span><span class="sxs-lookup"><span data-stu-id="eee87-590">localhost</span></span>
- <span data-ttu-id="eee87-591">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="eee87-591">127.0.0.1</span></span>
- <span data-ttu-id="eee87-592">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-593">ccw</span><span class="sxs-lookup"><span data-stu-id="eee87-593">com</span></span>
- <span data-ttu-id="eee87-594">s-int</span><span class="sxs-lookup"><span data-stu-id="eee87-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-595">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="eee87-596">Azure Redis 캐시 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="eee87-597">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-597">Format</span></span>

<span data-ttu-id="eee87-598">문자열 "redis.</span><span class="sxs-lookup"><span data-stu-id="eee87-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-599">net "문자열" password "또는" pwd "를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-600">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-600">Pattern</span></span>

- <span data-ttu-id="eee87-601">문자열 "redis.</span><span class="sxs-lookup"><span data-stu-id="eee87-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-602">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-602">net"</span></span>
- <span data-ttu-id="eee87-603">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-604">문자열 "password" 또는 "pwd"</span><span class="sxs-lookup"><span data-stu-id="eee87-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="eee87-605">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-606">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-606">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-607">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-608">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="eee87-609">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-610">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-610">Checksum</span></span>

<span data-ttu-id="eee87-611">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-612">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-612">Definition</span></span>

<span data-ttu-id="eee87-613">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-614">정규식 CEP_Regex_AzureRedisCacheConnectionString가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="eee87-615">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-616">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="eee87-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="eee87-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="eee87-618">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-619">극동</span><span class="sxs-lookup"><span data-stu-id="eee87-619">contoso</span></span>
- <span data-ttu-id="eee87-620">fabrikam</span><span class="sxs-lookup"><span data-stu-id="eee87-620">fabrikam</span></span>
- <span data-ttu-id="eee87-621">대양</span><span class="sxs-lookup"><span data-stu-id="eee87-621">northwind</span></span>
- <span data-ttu-id="eee87-622">샌드박스</span><span class="sxs-lookup"><span data-stu-id="eee87-622">sandbox</span></span>
- <span data-ttu-id="eee87-623">용 onebox</span><span class="sxs-lookup"><span data-stu-id="eee87-623">onebox</span></span>
- <span data-ttu-id="eee87-624">로컬</span><span class="sxs-lookup"><span data-stu-id="eee87-624">localhost</span></span>
- <span data-ttu-id="eee87-625">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="eee87-625">127.0.0.1</span></span>
- <span data-ttu-id="eee87-626">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-627">ccw</span><span class="sxs-lookup"><span data-stu-id="eee87-627">com</span></span>
- <span data-ttu-id="eee87-628">s-int</span><span class="sxs-lookup"><span data-stu-id="eee87-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-629">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="eee87-630">Azure SAS</span><span class="sxs-lookup"><span data-stu-id="eee87-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="eee87-631">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-631">Format</span></span>

<span data-ttu-id="eee87-632">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 문자열 "sig"</span><span class="sxs-lookup"><span data-stu-id="eee87-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-633">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-633">Pattern</span></span>

- <span data-ttu-id="eee87-634">문자열 "sig"</span><span class="sxs-lookup"><span data-stu-id="eee87-634">The string "sig"</span></span>
- <span data-ttu-id="eee87-635">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-636">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-636">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-637">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-638">대/소문자, 숫자 또는 백분율 기호 (%)가 43-53 자 사이의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="eee87-639">문자열 "% 3d"</span><span class="sxs-lookup"><span data-stu-id="eee87-639">The string "%3d"</span></span>
- <span data-ttu-id="eee87-640">소문자 또는 대문자, 숫자 또는 백분율 기호 (%)가 아닌 모든 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-641">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-641">Checksum</span></span>

<span data-ttu-id="eee87-642">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-643">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-643">Definition</span></span>

<span data-ttu-id="eee87-644">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-645">정규식 CEP_Regex_AzureSAS 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```xml
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="eee87-646">Azure Service Bus 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="eee87-647">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-647">Format</span></span>

<span data-ttu-id="eee87-648">문자열 "끝점" 뒤에 "servicebus" 라는 문자열을 포함 하 여 아래 패턴에 나와 있는 문자 및 문자열이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-649">net "및" SharedAccesKey "을 차례로 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-650">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-650">Pattern</span></span>

- <span data-ttu-id="eee87-651">문자열 "끝점"</span><span class="sxs-lookup"><span data-stu-id="eee87-651">The string "EndPoint"</span></span>
- <span data-ttu-id="eee87-652">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-653">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-653">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-654">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-655">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-656">문자열 "servicebus.</span><span class="sxs-lookup"><span data-stu-id="eee87-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-657">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-657">net"</span></span>
- <span data-ttu-id="eee87-658">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-659">"SharedAccessKey" 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="eee87-660">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-661">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-661">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-662">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-663">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="eee87-664">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-665">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-665">Checksum</span></span>

<span data-ttu-id="eee87-666">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-667">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-667">Definition</span></span>

<span data-ttu-id="eee87-668">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-669">정규식 CEP_Regex_AzureServiceBusConnectionString가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="eee87-670">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-671">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="eee87-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="eee87-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="eee87-673">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-674">극동</span><span class="sxs-lookup"><span data-stu-id="eee87-674">contoso</span></span>
- <span data-ttu-id="eee87-675">fabrikam</span><span class="sxs-lookup"><span data-stu-id="eee87-675">fabrikam</span></span>
- <span data-ttu-id="eee87-676">대양</span><span class="sxs-lookup"><span data-stu-id="eee87-676">northwind</span></span>
- <span data-ttu-id="eee87-677">샌드박스</span><span class="sxs-lookup"><span data-stu-id="eee87-677">sandbox</span></span>
- <span data-ttu-id="eee87-678">용 onebox</span><span class="sxs-lookup"><span data-stu-id="eee87-678">onebox</span></span>
- <span data-ttu-id="eee87-679">로컬</span><span class="sxs-lookup"><span data-stu-id="eee87-679">localhost</span></span>
- <span data-ttu-id="eee87-680">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="eee87-680">127.0.0.1</span></span>
- <span data-ttu-id="eee87-681">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-682">ccw</span><span class="sxs-lookup"><span data-stu-id="eee87-682">com</span></span>
- <span data-ttu-id="eee87-683">s-int</span><span class="sxs-lookup"><span data-stu-id="eee87-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-684">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="eee87-685">Azure 저장소 계정 키</span><span class="sxs-lookup"><span data-stu-id="eee87-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="eee87-686">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-686">Format</span></span>

<span data-ttu-id="eee87-687">"DefaultEndpointsProtocol" 문자열은 "AccountKey" 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-688">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-688">Pattern</span></span>

- <span data-ttu-id="eee87-689">문자열 "DefaultEndpointsProtocol"</span><span class="sxs-lookup"><span data-stu-id="eee87-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="eee87-690">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-691">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-691">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-692">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-693">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-694">문자열 "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="eee87-694">The string "AccountKey"</span></span>
- <span data-ttu-id="eee87-695">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-696">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-696">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-697">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="eee87-698">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="eee87-699">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-700">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-700">Checksum</span></span>

<span data-ttu-id="eee87-701">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-702">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-702">Definition</span></span>

<span data-ttu-id="eee87-703">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-704">정규식 CEP_Regex_AzureStorageAccountKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-705">CEP_AzureEmulatorStorageAccountFilter 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-706">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-707">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="eee87-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="eee87-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="eee87-709">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="eee87-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="eee87-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="eee87-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="eee87-712">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-713">극동</span><span class="sxs-lookup"><span data-stu-id="eee87-713">contoso</span></span>
- <span data-ttu-id="eee87-714">fabrikam</span><span class="sxs-lookup"><span data-stu-id="eee87-714">fabrikam</span></span>
- <span data-ttu-id="eee87-715">대양</span><span class="sxs-lookup"><span data-stu-id="eee87-715">northwind</span></span>
- <span data-ttu-id="eee87-716">샌드박스</span><span class="sxs-lookup"><span data-stu-id="eee87-716">sandbox</span></span>
- <span data-ttu-id="eee87-717">용 onebox</span><span class="sxs-lookup"><span data-stu-id="eee87-717">onebox</span></span>
- <span data-ttu-id="eee87-718">로컬</span><span class="sxs-lookup"><span data-stu-id="eee87-718">localhost</span></span>
- <span data-ttu-id="eee87-719">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="eee87-719">127.0.0.1</span></span>
- <span data-ttu-id="eee87-720">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-721">ccw</span><span class="sxs-lookup"><span data-stu-id="eee87-721">com</span></span>
- <span data-ttu-id="eee87-722">s-int</span><span class="sxs-lookup"><span data-stu-id="eee87-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-723">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="eee87-724">Azure 저장소 계정 키 (일반)</span><span class="sxs-lookup"><span data-stu-id="eee87-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-725">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-725">Format</span></span>

<span data-ttu-id="eee87-726">아래 패턴에 윤곽선이 있는 문자 앞 이나 뒤에 오는 86 문자의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-727">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-727">Pattern</span></span>

- <span data-ttu-id="eee87-728">보다 큼 기호 (>), 아포스트로피 ('), 등호 (=), 따옴표 (") 또는 숫자 기호 (#) 0-1</span><span class="sxs-lookup"><span data-stu-id="eee87-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="eee87-729">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="eee87-730">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="eee87-731">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-731">Checksum</span></span>

<span data-ttu-id="eee87-732">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-733">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-733">Definition</span></span>

<span data-ttu-id="eee87-734">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-735">정규식 CEP_Regex_AzureStorageAccountKeyGeneric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="eee87-736">벨기에 국가 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-737">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-737">Format</span></span>

<span data-ttu-id="eee87-738">11자리 숫자와 구분 기호</span><span class="sxs-lookup"><span data-stu-id="eee87-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-739">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-739">Pattern</span></span>

<span data-ttu-id="eee87-740">11자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="eee87-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="eee87-741">생년월일을 나타내는 YY.MM.DD 형식의 6자리 숫자와 마침표 2개 </span><span class="sxs-lookup"><span data-stu-id="eee87-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="eee87-742">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-742">A hyphen</span></span> 
- <span data-ttu-id="eee87-743">세 개의 순차적 숫자(남성의 경우 홀수, 여성의 경우 짝수) </span><span class="sxs-lookup"><span data-stu-id="eee87-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="eee87-744">마침표</span><span class="sxs-lookup"><span data-stu-id="eee87-744">A period</span></span> 
- <span data-ttu-id="eee87-745">검사 숫자에 해당하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-746">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-746">Checksum</span></span>

<span data-ttu-id="eee87-747">예</span><span class="sxs-lookup"><span data-stu-id="eee87-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-748">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-748">Definition</span></span>

<span data-ttu-id="eee87-749">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-750">Func_belgium_national_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-751">Keyword_belgium_national_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="eee87-752">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-752">The checksum passes.</span></span>

```xml
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-753">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="eee87-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="eee87-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="eee87-755">ID</span><span class="sxs-lookup"><span data-stu-id="eee87-755">Identity</span></span>
- <span data-ttu-id="eee87-756">등록</span><span class="sxs-lookup"><span data-stu-id="eee87-756">Registration</span></span>
- <span data-ttu-id="eee87-757">확인과</span><span class="sxs-lookup"><span data-stu-id="eee87-757">Identification</span></span> 
- <span data-ttu-id="eee87-758">ID</span><span class="sxs-lookup"><span data-stu-id="eee87-758">ID</span></span> 
- <span data-ttu-id="eee87-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="eee87-759">Identiteitskaart</span></span>
- <span data-ttu-id="eee87-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="eee87-760">Registratie nummer</span></span> 
- <span data-ttu-id="eee87-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="eee87-761">Identificatie nummer</span></span> 
- <span data-ttu-id="eee87-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="eee87-762">Identiteit</span></span>
- <span data-ttu-id="eee87-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="eee87-763">Registratie</span></span>
- <span data-ttu-id="eee87-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="eee87-764">Identificatie</span></span> 
- <span data-ttu-id="eee87-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="eee87-765">Carte d’identité</span></span> 
- <span data-ttu-id="eee87-766">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="eee87-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="eee87-767">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="eee87-767">numéro d'identification</span></span>
- <span data-ttu-id="eee87-768">identité</span><span class="sxs-lookup"><span data-stu-id="eee87-768">identité</span></span> 
- <span data-ttu-id="eee87-769">inscription</span><span class="sxs-lookup"><span data-stu-id="eee87-769">inscription</span></span> 
- <span data-ttu-id="eee87-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="eee87-770">Identifikation</span></span>
- <span data-ttu-id="eee87-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="eee87-771">Identifizierung</span></span>
- <span data-ttu-id="eee87-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-772">Identifikationsnummer</span></span>
- <span data-ttu-id="eee87-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="eee87-773">Personalausweis</span></span>
- <span data-ttu-id="eee87-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="eee87-774">Registrierung</span></span>
- <span data-ttu-id="eee87-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="eee87-776">브라질 CPF 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-777">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-777">Format</span></span>

<span data-ttu-id="eee87-778">서식이 있거나 서식이 없을 수 있는 검사 숫자를 포함하는 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-779">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-779">Pattern</span></span>

<span data-ttu-id="eee87-780">서식이</span><span class="sxs-lookup"><span data-stu-id="eee87-780">Formatted:</span></span>
- <span data-ttu-id="eee87-781">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-781">Three digits</span></span> 
- <span data-ttu-id="eee87-782">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-782">A period</span></span> 
- <span data-ttu-id="eee87-783">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-783">Three digits</span></span> 
- <span data-ttu-id="eee87-784">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-784">A period</span></span> 
- <span data-ttu-id="eee87-785">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-785">Three digits</span></span> 
- <span data-ttu-id="eee87-786">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-786">A hyphen</span></span> 
- <span data-ttu-id="eee87-787">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-787">Two digits which are check digits</span></span>

<span data-ttu-id="eee87-788">서식</span><span class="sxs-lookup"><span data-stu-id="eee87-788">Unformatted:</span></span>
- <span data-ttu-id="eee87-789">마지막 2자리 숫자가 검사 숫자인 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-790">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-790">Checksum</span></span>

<span data-ttu-id="eee87-791">예</span><span class="sxs-lookup"><span data-stu-id="eee87-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-792">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-792">Definition</span></span>

<span data-ttu-id="eee87-793">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-794">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-795">Keyword_brazil_cpf에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="eee87-796">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-796">The checksum passes.</span></span>

<span data-ttu-id="eee87-797">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-798">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-799">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-799">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-800">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="eee87-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="eee87-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="eee87-802">CPF</span><span class="sxs-lookup"><span data-stu-id="eee87-802">CPF</span></span>
- <span data-ttu-id="eee87-803">확인과</span><span class="sxs-lookup"><span data-stu-id="eee87-803">Identification</span></span>
- <span data-ttu-id="eee87-804">등록</span><span class="sxs-lookup"><span data-stu-id="eee87-804">Registration</span></span>
- <span data-ttu-id="eee87-805">별</span><span class="sxs-lookup"><span data-stu-id="eee87-805">Revenue</span></span>
- <span data-ttu-id="eee87-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="eee87-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="eee87-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="eee87-807">Imposto</span></span> 
- <span data-ttu-id="eee87-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="eee87-808">Identificação</span></span> 
- <span data-ttu-id="eee87-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="eee87-809">Inscrição</span></span> 
- <span data-ttu-id="eee87-810">고 eita</span><span class="sxs-lookup"><span data-stu-id="eee87-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="eee87-811">브라질 법인 번호(CNPJ)</span><span class="sxs-lookup"><span data-stu-id="eee87-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-812">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-812">Format</span></span>

<span data-ttu-id="eee87-813">등록 번호, 지점 번호, 검사 숫자 및 구분 기호를 포함하는 14자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-814">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-814">Pattern</span></span>
<span data-ttu-id="eee87-815">14자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="eee87-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="eee87-816">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-816">Two digits</span></span> 
- <span data-ttu-id="eee87-817">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-817">A period</span></span> 
- <span data-ttu-id="eee87-818">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-818">Three digits</span></span> 
- <span data-ttu-id="eee87-819">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-819">A period</span></span> 
- <span data-ttu-id="eee87-820">3자리 숫자(처음 8자리 숫자는 등록 번호임) </span><span class="sxs-lookup"><span data-stu-id="eee87-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="eee87-821">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="eee87-821">A forward slash</span></span> 
- <span data-ttu-id="eee87-822">4자리 지점 번호 </span><span class="sxs-lookup"><span data-stu-id="eee87-822">Four-digit branch number</span></span> 
- <span data-ttu-id="eee87-823">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-823">A hyphen</span></span> 
- <span data-ttu-id="eee87-824">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-825">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-825">Checksum</span></span>

<span data-ttu-id="eee87-826">예</span><span class="sxs-lookup"><span data-stu-id="eee87-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-827">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-827">Definition</span></span>

<span data-ttu-id="eee87-828">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-829">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-830">Keyword_brazil_cnpj에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="eee87-831">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-831">The checksum passes.</span></span>

<span data-ttu-id="eee87-832">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-833">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-834">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-834">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-835">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="eee87-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="eee87-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="eee87-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="eee87-837">CNPJ</span></span> 
- <span data-ttu-id="eee87-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="eee87-838">CNPJ/MF</span></span> 
- <span data-ttu-id="eee87-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="eee87-839">CNPJ-MF</span></span> 
- <span data-ttu-id="eee87-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="eee87-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="eee87-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="eee87-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="eee87-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="eee87-842">Legal entity</span></span> 
- <span data-ttu-id="eee87-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="eee87-843">Legal entities</span></span> 
- <span data-ttu-id="eee87-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="eee87-844">Registration Status</span></span> 
- <span data-ttu-id="eee87-845">비즈니스</span><span class="sxs-lookup"><span data-stu-id="eee87-845">Business</span></span> 
- <span data-ttu-id="eee87-846">Company</span><span class="sxs-lookup"><span data-stu-id="eee87-846">Company</span></span>
- <span data-ttu-id="eee87-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="eee87-847">CNPJ</span></span> 
- <span data-ttu-id="eee87-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="eee87-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="eee87-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="eee87-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="eee87-850">CGC</span><span class="sxs-lookup"><span data-stu-id="eee87-850">CGC</span></span> 
- <span data-ttu-id="eee87-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="eee87-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="eee87-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="eee87-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="eee87-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="eee87-853">Situação cadastral</span></span> 
- <span data-ttu-id="eee87-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="eee87-854">Inscrição</span></span> 
- <span data-ttu-id="eee87-855">포털</span><span class="sxs-lookup"><span data-stu-id="eee87-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="eee87-856">	브라질 국가 ID 카드(RG)</span><span class="sxs-lookup"><span data-stu-id="eee87-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-857">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-857">Format</span></span>

<span data-ttu-id="eee87-858">Registro Geral (이전 형식): 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="eee87-859">Registro de Identidade (RIC) (새 형식): 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-860">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-860">Pattern</span></span>

<span data-ttu-id="eee87-861">Registro Geral(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="eee87-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="eee87-862">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-862">Two digits</span></span> 
- <span data-ttu-id="eee87-863">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-863">A period</span></span> 
- <span data-ttu-id="eee87-864">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-864">Three digits</span></span> 
- <span data-ttu-id="eee87-865">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-865">A period</span></span> 
- <span data-ttu-id="eee87-866">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-866">Three digits</span></span> 
- <span data-ttu-id="eee87-867">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-867">A hyphen</span></span> 
- <span data-ttu-id="eee87-868">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-868">One digit which is a check digit</span></span>

<span data-ttu-id="eee87-869">Registro de Identidade (RIC) (새 형식):</span><span class="sxs-lookup"><span data-stu-id="eee87-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="eee87-870">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-870">10 digits</span></span> 
- <span data-ttu-id="eee87-871">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-871">A hyphen</span></span> 
- <span data-ttu-id="eee87-872">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-873">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-873">Checksum</span></span>

<span data-ttu-id="eee87-874">예</span><span class="sxs-lookup"><span data-stu-id="eee87-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-875">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-875">Definition</span></span>

<span data-ttu-id="eee87-876">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-877">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-878">Keyword_brazil_rg에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="eee87-879">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-879">The checksum passes.</span></span>

<span data-ttu-id="eee87-880">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-881">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-882">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-882">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-883">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="eee87-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="eee87-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="eee87-885">Cédula de identidade identity card 국립 id número de rregistro registro de Iidentidade registro geral RG (이 키워드는 대/소문자를 구분 함) RIC (이 키워드는 대/소문자를 구분 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="eee87-886">캐나다 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-887">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-887">Format</span></span>

<span data-ttu-id="eee87-888">7 또는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-889">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-889">Pattern</span></span>

<span data-ttu-id="eee87-890">캐나다 은행 계좌 번호는 7 또는 12자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="eee87-891">캐나다 은행 계좌 송금 번호:</span><span class="sxs-lookup"><span data-stu-id="eee87-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="eee87-892">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-892">Five digits</span></span> 
- <span data-ttu-id="eee87-893">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-893">A hyphen</span></span> 
- <span data-ttu-id="eee87-894">3 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="eee87-894">Three digits OR</span></span>
- <span data-ttu-id="eee87-895">"0"</span><span class="sxs-lookup"><span data-stu-id="eee87-895">A zero "0"</span></span> 
- <span data-ttu-id="eee87-896">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-897">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-897">Checksum</span></span>

<span data-ttu-id="eee87-898">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-899">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-899">Definition</span></span>

<span data-ttu-id="eee87-900">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-901">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-902">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="eee87-903">Regex_canada_bank_account_transit_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="eee87-904">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-905">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-906">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-907">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="eee87-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="eee87-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="eee87-909">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="eee87-909">canada savings bonds</span></span>
- <span data-ttu-id="eee87-910">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="eee87-910">canada revenue agency</span></span>
- <span data-ttu-id="eee87-911">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="eee87-911">canadian financial institution</span></span>
- <span data-ttu-id="eee87-912">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="eee87-912">direct deposit form</span></span>
- <span data-ttu-id="eee87-913">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="eee87-913">canadian citizen</span></span>
- <span data-ttu-id="eee87-914">legal representative</span><span class="sxs-lookup"><span data-stu-id="eee87-914">legal representative</span></span>
- <span data-ttu-id="eee87-915">notary public</span><span class="sxs-lookup"><span data-stu-id="eee87-915">notary public</span></span>
- <span data-ttu-id="eee87-916">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="eee87-916">commissioner for oaths</span></span>
- <span data-ttu-id="eee87-917">child care benefit</span><span class="sxs-lookup"><span data-stu-id="eee87-917">child care benefit</span></span>
- <span data-ttu-id="eee87-918">universal child care</span><span class="sxs-lookup"><span data-stu-id="eee87-918">universal child care</span></span>
- <span data-ttu-id="eee87-919">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="eee87-919">canada child tax benefit</span></span>
- <span data-ttu-id="eee87-920">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="eee87-920">income tax benefit</span></span>
- <span data-ttu-id="eee87-921">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="eee87-921">harmonized sales tax</span></span>
- <span data-ttu-id="eee87-922">social insurance number</span><span class="sxs-lookup"><span data-stu-id="eee87-922">social insurance number</span></span>
- <span data-ttu-id="eee87-923">income tax refund</span><span class="sxs-lookup"><span data-stu-id="eee87-923">income tax refund</span></span>
- <span data-ttu-id="eee87-924">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="eee87-924">child tax benefit</span></span>
- <span data-ttu-id="eee87-925">territorial payments</span><span class="sxs-lookup"><span data-stu-id="eee87-925">territorial payments</span></span>
- <span data-ttu-id="eee87-926">institution number</span><span class="sxs-lookup"><span data-stu-id="eee87-926">institution number</span></span>
- <span data-ttu-id="eee87-927">deposit request</span><span class="sxs-lookup"><span data-stu-id="eee87-927">deposit request</span></span>
- <span data-ttu-id="eee87-928">banking information</span><span class="sxs-lookup"><span data-stu-id="eee87-928">banking information</span></span>
- <span data-ttu-id="eee87-929">direct deposit</span><span class="sxs-lookup"><span data-stu-id="eee87-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="eee87-930">캐나다 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-931">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-931">Format</span></span>

<span data-ttu-id="eee87-932">지역마다 다름</span><span class="sxs-lookup"><span data-stu-id="eee87-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-933">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-933">Pattern</span></span>

<span data-ttu-id="eee87-934">앨버타, 브리티시 콜롬비아, 매니토바, 뉴브런즈윅, 뉴펀들랜드/래브라도, 노바스코샤, 온타리오, 프린스에드워드아일랜드, 퀘벡 및 서스캐처원을 포함하는 다양한 패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-935">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-935">Checksum</span></span>

<span data-ttu-id="eee87-936">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-937">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-937">Definition</span></span>

<span data-ttu-id="eee87-938">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-939">Func_[province_name]_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-940">Keyword_[province_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="eee87-941">Keyword_canada_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-942">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="eee87-943">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="eee87-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="eee87-944">시/도 약어(예: AB)</span><span class="sxs-lookup"><span data-stu-id="eee87-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="eee87-945">시/도 이름(예: 앨버타)</span><span class="sxs-lookup"><span data-stu-id="eee87-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="eee87-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="eee87-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="eee87-947">DL</span><span class="sxs-lookup"><span data-stu-id="eee87-947">DL</span></span>
- <span data-ttu-id="eee87-948">된다</span><span class="sxs-lookup"><span data-stu-id="eee87-948">DLS</span></span>
- <span data-ttu-id="eee87-949">CDL</span><span class="sxs-lookup"><span data-stu-id="eee87-949">CDL</span></span>
- <span data-ttu-id="eee87-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="eee87-950">CDLS</span></span>
- <span data-ttu-id="eee87-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="eee87-951">DriverLic</span></span>
- <span data-ttu-id="eee87-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="eee87-952">DriverLics</span></span>
- <span data-ttu-id="eee87-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="eee87-953">DriverLicense</span></span>
- <span data-ttu-id="eee87-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="eee87-954">DriverLicenses</span></span>
- <span data-ttu-id="eee87-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="eee87-955">DriverLicence</span></span>
- <span data-ttu-id="eee87-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="eee87-956">DriverLicences</span></span>
- <span data-ttu-id="eee87-957">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-957">Driver Lic</span></span>
- <span data-ttu-id="eee87-958">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-958">Driver Lics</span></span>
- <span data-ttu-id="eee87-959">Driver License</span><span class="sxs-lookup"><span data-stu-id="eee87-959">Driver License</span></span>
- <span data-ttu-id="eee87-960">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-960">Driver Licenses</span></span>
- <span data-ttu-id="eee87-961">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-961">Driver Licence</span></span>
- <span data-ttu-id="eee87-962">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-962">Driver Licences</span></span>
- <span data-ttu-id="eee87-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="eee87-963">DriversLic</span></span>
- <span data-ttu-id="eee87-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="eee87-964">DriversLics</span></span>
- <span data-ttu-id="eee87-965">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-965">DriversLicence</span></span>
- <span data-ttu-id="eee87-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="eee87-966">DriversLicences</span></span>
- <span data-ttu-id="eee87-967">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-967">DriversLicense</span></span>
- <span data-ttu-id="eee87-968">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-968">DriversLicenses</span></span>
- <span data-ttu-id="eee87-969">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-969">Drivers Lic</span></span>
- <span data-ttu-id="eee87-970">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-970">Drivers Lics</span></span>
- <span data-ttu-id="eee87-971">Drivers License</span><span class="sxs-lookup"><span data-stu-id="eee87-971">Drivers License</span></span>
- <span data-ttu-id="eee87-972">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-972">Drivers Licenses</span></span>
- <span data-ttu-id="eee87-973">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-973">Drivers Licence</span></span>
- <span data-ttu-id="eee87-974">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-974">Drivers Licences</span></span>
- <span data-ttu-id="eee87-975">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-975">Driver'Lic</span></span>
- <span data-ttu-id="eee87-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-976">Driver'Lics</span></span>
- <span data-ttu-id="eee87-977">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-977">Driver'License</span></span>
- <span data-ttu-id="eee87-978">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-978">Driver'Licenses</span></span>
- <span data-ttu-id="eee87-979">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-979">Driver'Licence</span></span>
- <span data-ttu-id="eee87-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-980">Driver'Licences</span></span>
- <span data-ttu-id="eee87-981">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-981">Driver' Lic</span></span>
- <span data-ttu-id="eee87-982">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-982">Driver' Lics</span></span>
- <span data-ttu-id="eee87-983">Driver' License</span><span class="sxs-lookup"><span data-stu-id="eee87-983">Driver' License</span></span>
- <span data-ttu-id="eee87-984">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-984">Driver' Licenses</span></span>
- <span data-ttu-id="eee87-985">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-985">Driver' Licence</span></span>
- <span data-ttu-id="eee87-986">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-986">Driver' Licences</span></span>
- <span data-ttu-id="eee87-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="eee87-987">Driver'sLic</span></span>
- <span data-ttu-id="eee87-988">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="eee87-988">Driver'sLics</span></span>
- <span data-ttu-id="eee87-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="eee87-989">Driver'sLicense</span></span>
- <span data-ttu-id="eee87-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="eee87-990">Driver'sLicenses</span></span>
- <span data-ttu-id="eee87-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="eee87-991">Driver'sLicence</span></span>
- <span data-ttu-id="eee87-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="eee87-992">Driver'sLicences</span></span>
- <span data-ttu-id="eee87-993">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-993">Driver's Lic</span></span>
- <span data-ttu-id="eee87-994">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-994">Driver's Lics</span></span>
- <span data-ttu-id="eee87-995">Driver's License</span><span class="sxs-lookup"><span data-stu-id="eee87-995">Driver's License</span></span>
- <span data-ttu-id="eee87-996">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-996">Driver's Licenses</span></span>
- <span data-ttu-id="eee87-997">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-997">Driver's Licence</span></span>
- <span data-ttu-id="eee87-998">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-998">Driver's Licences</span></span>
- <span data-ttu-id="eee87-999">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="eee87-999">Permis de Conduire</span></span>
- <span data-ttu-id="eee87-1000">id</span><span class="sxs-lookup"><span data-stu-id="eee87-1000">id</span></span>
- <span data-ttu-id="eee87-1001">번호가</span><span class="sxs-lookup"><span data-stu-id="eee87-1001">ids</span></span>
- <span data-ttu-id="eee87-1002">idcard number</span><span class="sxs-lookup"><span data-stu-id="eee87-1002">idcard number</span></span>
- <span data-ttu-id="eee87-1003">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="eee87-1003">idcard numbers</span></span>
- <span data-ttu-id="eee87-1004">idcard #</span><span class="sxs-lookup"><span data-stu-id="eee87-1004">idcard #</span></span>
- <span data-ttu-id="eee87-1005">idcard #s</span><span class="sxs-lookup"><span data-stu-id="eee87-1005">idcard #s</span></span>
- <span data-ttu-id="eee87-1006">idcard card</span><span class="sxs-lookup"><span data-stu-id="eee87-1006">idcard card</span></span>
- <span data-ttu-id="eee87-1007">idcard cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1007">idcard cards</span></span>
- <span data-ttu-id="eee87-1008">idcard</span><span class="sxs-lookup"><span data-stu-id="eee87-1008">idcard</span></span>
- <span data-ttu-id="eee87-1009">identification number</span><span class="sxs-lookup"><span data-stu-id="eee87-1009">identification number</span></span>
- <span data-ttu-id="eee87-1010">identification numbers</span><span class="sxs-lookup"><span data-stu-id="eee87-1010">identification numbers</span></span>
- <span data-ttu-id="eee87-1011">identification #</span><span class="sxs-lookup"><span data-stu-id="eee87-1011">identification #</span></span>
- <span data-ttu-id="eee87-1012">identification #s</span><span class="sxs-lookup"><span data-stu-id="eee87-1012">identification #s</span></span>
- <span data-ttu-id="eee87-1013">identification card</span><span class="sxs-lookup"><span data-stu-id="eee87-1013">identification card</span></span>
- <span data-ttu-id="eee87-1014">identification cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1014">identification cards</span></span>
- <span data-ttu-id="eee87-1015">확인과</span><span class="sxs-lookup"><span data-stu-id="eee87-1015">identification</span></span> 
- <span data-ttu-id="eee87-1016">DL #</span><span class="sxs-lookup"><span data-stu-id="eee87-1016">DL#</span></span>
- <span data-ttu-id="eee87-1017">된다 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1017">DLS#</span></span> 
- <span data-ttu-id="eee87-1018">CDL #</span><span class="sxs-lookup"><span data-stu-id="eee87-1018">CDL#</span></span> 
- <span data-ttu-id="eee87-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="eee87-1019">CDLS#</span></span> 
- <span data-ttu-id="eee87-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-1020">DriverLic#</span></span> 
- <span data-ttu-id="eee87-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="eee87-1021">DriverLics#</span></span> 
- <span data-ttu-id="eee87-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="eee87-1022">DriverLicense#</span></span> 
- <span data-ttu-id="eee87-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="eee87-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="eee87-1024">DriverLicence#</span></span> 
- <span data-ttu-id="eee87-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="eee87-1025">DriverLicences#</span></span> 
- <span data-ttu-id="eee87-1026">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-1026">Driver Lic#</span></span>
- <span data-ttu-id="eee87-1027">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-1027">Driver Lics#</span></span> 
- <span data-ttu-id="eee87-1028">Driver License#</span><span class="sxs-lookup"><span data-stu-id="eee87-1028">Driver License#</span></span> 
- <span data-ttu-id="eee87-1029">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="eee87-1030">Driver License#</span><span class="sxs-lookup"><span data-stu-id="eee87-1030">Driver License#</span></span> 
- <span data-ttu-id="eee87-1031">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="eee87-1031">Driver Licences#</span></span> 
- <span data-ttu-id="eee87-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-1032">DriversLic#</span></span> 
- <span data-ttu-id="eee87-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="eee87-1033">DriversLics#</span></span> 
- <span data-ttu-id="eee87-1034">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1034">DriversLicense#</span></span> 
- <span data-ttu-id="eee87-1035">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="eee87-1036">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1036">DriversLicence#</span></span> 
- <span data-ttu-id="eee87-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="eee87-1037">DriversLicences#</span></span> 
- <span data-ttu-id="eee87-1038">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="eee87-1039">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="eee87-1040">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="eee87-1040">Drivers License#</span></span> 
- <span data-ttu-id="eee87-1041">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="eee87-1042">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="eee87-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="eee87-1043">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="eee87-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="eee87-1044">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="eee87-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="eee87-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="eee87-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="eee87-1046">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1046">Driver'License#</span></span> 
- <span data-ttu-id="eee87-1047">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="eee87-1048">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="eee87-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="eee87-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="eee87-1050">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="eee87-1051">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="eee87-1052">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="eee87-1052">Driver' License#</span></span> 
- <span data-ttu-id="eee87-1053">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="eee87-1054">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="eee87-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="eee87-1055">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="eee87-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="eee87-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="eee87-1057">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="eee87-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="eee87-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="eee87-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="eee87-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="eee87-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="eee87-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="eee87-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="eee87-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="eee87-1062">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="eee87-1063">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="eee87-1064">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="eee87-1064">Driver's License#</span></span> 
- <span data-ttu-id="eee87-1065">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="eee87-1066">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="eee87-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="eee87-1067">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="eee87-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="eee87-1068">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="eee87-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="eee87-1069">i #</span><span class="sxs-lookup"><span data-stu-id="eee87-1069">id#</span></span> 
- <span data-ttu-id="eee87-1070">번호가 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1070">ids#</span></span> 
- <span data-ttu-id="eee87-1071">idcard card#</span><span class="sxs-lookup"><span data-stu-id="eee87-1071">idcard card#</span></span> 
- <span data-ttu-id="eee87-1072">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="eee87-1072">idcard cards#</span></span> 
- <span data-ttu-id="eee87-1073">idcard #</span><span class="sxs-lookup"><span data-stu-id="eee87-1073">idcard#</span></span> 
- <span data-ttu-id="eee87-1074">identification card#</span><span class="sxs-lookup"><span data-stu-id="eee87-1074">identification card#</span></span> 
- <span data-ttu-id="eee87-1075">identification cards#</span><span class="sxs-lookup"><span data-stu-id="eee87-1075">identification cards#</span></span> 
- <span data-ttu-id="eee87-1076">확인과 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="eee87-1077">캐나다 건강 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1078">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1078">Format</span></span>

<span data-ttu-id="eee87-1079">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1080">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1080">Pattern</span></span>

<span data-ttu-id="eee87-1081">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1082">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1082">Checksum</span></span>

<span data-ttu-id="eee87-1083">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1084">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1084">Definition</span></span>

<span data-ttu-id="eee87-1085">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1086">Regex_canada_health_service_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1087">Keyword_canada_health_service_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1088">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="eee87-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="eee87-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="eee87-1090">personal health number</span><span class="sxs-lookup"><span data-stu-id="eee87-1090">personal health number</span></span>
- <span data-ttu-id="eee87-1091">patient information</span><span class="sxs-lookup"><span data-stu-id="eee87-1091">patient information</span></span>
- <span data-ttu-id="eee87-1092">health services</span><span class="sxs-lookup"><span data-stu-id="eee87-1092">health services</span></span>
- <span data-ttu-id="eee87-1093">speciality services</span><span class="sxs-lookup"><span data-stu-id="eee87-1093">speciality services</span></span>
- <span data-ttu-id="eee87-1094">automobile accident</span><span class="sxs-lookup"><span data-stu-id="eee87-1094">automobile accident</span></span>
- <span data-ttu-id="eee87-1095">patient hospital</span><span class="sxs-lookup"><span data-stu-id="eee87-1095">patient hospital</span></span>
- <span data-ttu-id="eee87-1096">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="eee87-1096">psychiatrist</span></span>
- <span data-ttu-id="eee87-1097">workers compensation</span><span class="sxs-lookup"><span data-stu-id="eee87-1097">workers compensation</span></span>
- <span data-ttu-id="eee87-1098">종류</span><span class="sxs-lookup"><span data-stu-id="eee87-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="eee87-1099">캐나다 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1100">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1100">Format</span></span>

<span data-ttu-id="eee87-1101">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1102">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1102">Pattern</span></span>

<span data-ttu-id="eee87-1103">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1104">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1104">Checksum</span></span>

<span data-ttu-id="eee87-1105">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1106">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1106">Definition</span></span>

<span data-ttu-id="eee87-1107">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1108">Regex_canada_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1109">Keyword_canada_passport_number 또는 Keyword_passport의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

```xml 
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

### <a name="keywords"></a><span data-ttu-id="eee87-1110">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="eee87-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="eee87-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="eee87-1112">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="eee87-1112">canadian citizenship</span></span>
- <span data-ttu-id="eee87-1113">canadian passport</span><span class="sxs-lookup"><span data-stu-id="eee87-1113">canadian passport</span></span>
- <span data-ttu-id="eee87-1114">passport application</span><span class="sxs-lookup"><span data-stu-id="eee87-1114">passport application</span></span>
- <span data-ttu-id="eee87-1115">passport photos</span><span class="sxs-lookup"><span data-stu-id="eee87-1115">passport photos</span></span>
- <span data-ttu-id="eee87-1116">certified translator</span><span class="sxs-lookup"><span data-stu-id="eee87-1116">certified translator</span></span>
- <span data-ttu-id="eee87-1117">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="eee87-1117">canadian citizens</span></span>
- <span data-ttu-id="eee87-1118">processing times</span><span class="sxs-lookup"><span data-stu-id="eee87-1118">processing times</span></span>
- <span data-ttu-id="eee87-1119">renewal application</span><span class="sxs-lookup"><span data-stu-id="eee87-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="eee87-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-1120">Keyword_passport</span></span>

- <span data-ttu-id="eee87-1121">Passport Number</span><span class="sxs-lookup"><span data-stu-id="eee87-1121">Passport Number</span></span>
- <span data-ttu-id="eee87-1122">Passport No</span><span class="sxs-lookup"><span data-stu-id="eee87-1122">Passport No</span></span>
- <span data-ttu-id="eee87-1123">Passport #</span><span class="sxs-lookup"><span data-stu-id="eee87-1123">Passport #</span></span>
- <span data-ttu-id="eee87-1124">여권 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1124">Passport#</span></span>
- <span data-ttu-id="eee87-1125">PassportID</span><span class="sxs-lookup"><span data-stu-id="eee87-1125">PassportID</span></span>
- <span data-ttu-id="eee87-1126">Passportno</span><span class="sxs-lookup"><span data-stu-id="eee87-1126">Passportno</span></span>
- <span data-ttu-id="eee87-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-1127">passportnumber</span></span>
- <span data-ttu-id="eee87-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="eee87-1128">パスポート</span></span>
- <span data-ttu-id="eee87-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="eee87-1129">パスポート番号</span></span>
- <span data-ttu-id="eee87-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="eee87-1130">パスポートのNum</span></span>
- <span data-ttu-id="eee87-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="eee87-1131">パスポート＃</span></span>
- <span data-ttu-id="eee87-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="eee87-1132">Numéro de passeport</span></span>
- <span data-ttu-id="eee87-1133">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="eee87-1133">Passeport n °</span></span>
- <span data-ttu-id="eee87-1134">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="eee87-1134">Passeport Non</span></span>
- <span data-ttu-id="eee87-1135">Passeport #</span><span class="sxs-lookup"><span data-stu-id="eee87-1135">Passeport #</span></span>
- <span data-ttu-id="eee87-1136">포트 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1136">Passeport#</span></span>
- <span data-ttu-id="eee87-1137">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="eee87-1137">PasseportNon</span></span>
- <span data-ttu-id="eee87-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="eee87-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="eee87-1139">캐나다 PHIN(개인 건강 식별 번호)</span><span class="sxs-lookup"><span data-stu-id="eee87-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1140">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1140">Format</span></span>

<span data-ttu-id="eee87-1141">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1142">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1142">Pattern</span></span>

<span data-ttu-id="eee87-1143">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1144">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1144">Checksum</span></span>

<span data-ttu-id="eee87-1145">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1146">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1146">Definition</span></span>

<span data-ttu-id="eee87-1147">DLP 정책은 300 문자 (예: Regex_canada_phin)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="eee87-1148">Keyword_canada_phin 또는 Keyword_canada_provinces의 키워드를 두 개 이상 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1149">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="eee87-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="eee87-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="eee87-1151">social insurance number</span><span class="sxs-lookup"><span data-stu-id="eee87-1151">social insurance number</span></span>
- <span data-ttu-id="eee87-1152">health information act</span><span class="sxs-lookup"><span data-stu-id="eee87-1152">health information act</span></span>
- <span data-ttu-id="eee87-1153">income tax information</span><span class="sxs-lookup"><span data-stu-id="eee87-1153">income tax information</span></span>
- <span data-ttu-id="eee87-1154">manitoba health</span><span class="sxs-lookup"><span data-stu-id="eee87-1154">manitoba health</span></span>
- <span data-ttu-id="eee87-1155">health registration</span><span class="sxs-lookup"><span data-stu-id="eee87-1155">health registration</span></span>
- <span data-ttu-id="eee87-1156">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="eee87-1156">prescription purchases</span></span>
- <span data-ttu-id="eee87-1157">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="eee87-1157">benefit eligibility</span></span>
- <span data-ttu-id="eee87-1158">personal health</span><span class="sxs-lookup"><span data-stu-id="eee87-1158">personal health</span></span>
- <span data-ttu-id="eee87-1159">power of attorney</span><span class="sxs-lookup"><span data-stu-id="eee87-1159">power of attorney</span></span>
- <span data-ttu-id="eee87-1160">registration number</span><span class="sxs-lookup"><span data-stu-id="eee87-1160">registration number</span></span>
- <span data-ttu-id="eee87-1161">personal health number</span><span class="sxs-lookup"><span data-stu-id="eee87-1161">personal health number</span></span>
- <span data-ttu-id="eee87-1162">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="eee87-1162">practitioner referral</span></span>
- <span data-ttu-id="eee87-1163">wellness professional</span><span class="sxs-lookup"><span data-stu-id="eee87-1163">wellness professional</span></span>
- <span data-ttu-id="eee87-1164">patient referral</span><span class="sxs-lookup"><span data-stu-id="eee87-1164">patient referral</span></span>
- <span data-ttu-id="eee87-1165">health and wellness</span><span class="sxs-lookup"><span data-stu-id="eee87-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="eee87-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="eee87-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="eee87-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="eee87-1167">Nunavut</span></span>
- <span data-ttu-id="eee87-1168">퀘벡</span><span class="sxs-lookup"><span data-stu-id="eee87-1168">Quebec</span></span>
- <span data-ttu-id="eee87-1169">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="eee87-1169">Northwest Territories</span></span>
- <span data-ttu-id="eee87-1170">온타리오</span><span class="sxs-lookup"><span data-stu-id="eee87-1170">Ontario</span></span>
- <span data-ttu-id="eee87-1171">British Columbia</span><span class="sxs-lookup"><span data-stu-id="eee87-1171">British Columbia</span></span>
- <span data-ttu-id="eee87-1172">앨버타</span><span class="sxs-lookup"><span data-stu-id="eee87-1172">Alberta</span></span>
- <span data-ttu-id="eee87-1173">서스캐처원</span><span class="sxs-lookup"><span data-stu-id="eee87-1173">Saskatchewan</span></span>
- <span data-ttu-id="eee87-1174">매니토바</span><span class="sxs-lookup"><span data-stu-id="eee87-1174">Manitoba</span></span>
- <span data-ttu-id="eee87-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="eee87-1175">Yukon</span></span>
- <span data-ttu-id="eee87-1176">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="eee87-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="eee87-1177">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="eee87-1177">New Brunswick</span></span>
- <span data-ttu-id="eee87-1178">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="eee87-1178">Nova Scotia</span></span>
- <span data-ttu-id="eee87-1179">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="eee87-1179">Prince Edward Island</span></span>
- <span data-ttu-id="eee87-1180">캐나다</span><span class="sxs-lookup"><span data-stu-id="eee87-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="eee87-1181">캐나다 사회 보험 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1182">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1182">Format</span></span>

<span data-ttu-id="eee87-1183">선택적 하이픈 또는 공백을 포함하는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1184">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1184">Pattern</span></span>

<span data-ttu-id="eee87-1185">서식이</span><span class="sxs-lookup"><span data-stu-id="eee87-1185">Formatted:</span></span>
- <span data-ttu-id="eee87-1186">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1186">Three digits</span></span> 
- <span data-ttu-id="eee87-1187">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="eee87-1187">A hyphen or space</span></span> 
- <span data-ttu-id="eee87-1188">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1188">Three digits</span></span> 
- <span data-ttu-id="eee87-1189">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="eee87-1189">A hyphen or space</span></span> 
- <span data-ttu-id="eee87-1190">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1190">Three digits</span></span>

<span data-ttu-id="eee87-1191">서식 없음: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1192">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1192">Checksum</span></span>

<span data-ttu-id="eee87-1193">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1194">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1194">Definition</span></span>

<span data-ttu-id="eee87-1195">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1196">Func_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1197">2개 이상의 다음 항목 조합:</span><span class="sxs-lookup"><span data-stu-id="eee87-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="eee87-1198">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="eee87-1199">Keyword_sin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="eee87-1200">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-1201">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1201">The checksum passes.</span></span>

<span data-ttu-id="eee87-1202">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1203">Func_unformatted_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1204">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="eee87-1205">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1205">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1206">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="eee87-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="eee87-1207">Keyword_sin</span></span>

- <span data-ttu-id="eee87-1208">sin</span><span class="sxs-lookup"><span data-stu-id="eee87-1208">sin</span></span> 
- <span data-ttu-id="eee87-1209">social insurance</span><span class="sxs-lookup"><span data-stu-id="eee87-1209">social insurance</span></span> 
- <span data-ttu-id="eee87-1210">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="eee87-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="eee87-1211">죄</span><span class="sxs-lookup"><span data-stu-id="eee87-1211">sins</span></span> 
- <span data-ttu-id="eee87-1212">ssn</span><span class="sxs-lookup"><span data-stu-id="eee87-1212">ssn</span></span> 
- <span data-ttu-id="eee87-1213">있는 ssn</span><span class="sxs-lookup"><span data-stu-id="eee87-1213">ssns</span></span> 
- <span data-ttu-id="eee87-1214">social security</span><span class="sxs-lookup"><span data-stu-id="eee87-1214">social security</span></span> 
- <span data-ttu-id="eee87-1215">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="eee87-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="eee87-1216">national identification number</span><span class="sxs-lookup"><span data-stu-id="eee87-1216">national identification number</span></span> 
- <span data-ttu-id="eee87-1217">national id</span><span class="sxs-lookup"><span data-stu-id="eee87-1217">national id</span></span> 
- <span data-ttu-id="eee87-1218">sin #</span><span class="sxs-lookup"><span data-stu-id="eee87-1218">sin#</span></span> 
- <span data-ttu-id="eee87-1219">soc ins</span><span class="sxs-lookup"><span data-stu-id="eee87-1219">soc ins</span></span> 
- <span data-ttu-id="eee87-1220">social ins</span><span class="sxs-lookup"><span data-stu-id="eee87-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="eee87-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="eee87-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="eee87-1222">driver's license</span><span class="sxs-lookup"><span data-stu-id="eee87-1222">driver's license</span></span> 
- <span data-ttu-id="eee87-1223">drivers license</span><span class="sxs-lookup"><span data-stu-id="eee87-1223">drivers license</span></span> 
- <span data-ttu-id="eee87-1224">driver's licence</span><span class="sxs-lookup"><span data-stu-id="eee87-1224">driver's licence</span></span> 
- <span data-ttu-id="eee87-1225">drivers licence</span><span class="sxs-lookup"><span data-stu-id="eee87-1225">drivers licence</span></span> 
- <span data-ttu-id="eee87-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="eee87-1226">DOB</span></span> 
- <span data-ttu-id="eee87-1227">생년월일</span><span class="sxs-lookup"><span data-stu-id="eee87-1227">Birthdate</span></span> 
- <span data-ttu-id="eee87-1228">생일</span><span class="sxs-lookup"><span data-stu-id="eee87-1228">Birthday</span></span> 
- <span data-ttu-id="eee87-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="eee87-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="eee87-1230">	칠레 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1231">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1231">Format</span></span>

<span data-ttu-id="eee87-1232">7-8 자리 숫자와 구분 기호 확인 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1233">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1233">Pattern</span></span>

<span data-ttu-id="eee87-1234">7-8자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="eee87-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="eee87-1235">1-2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1235">1-2 digits</span></span> 
- <span data-ttu-id="eee87-1236">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-1236">A period</span></span> 
- <span data-ttu-id="eee87-1237">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1237">Three digits</span></span> 
- <span data-ttu-id="eee87-1238">마침표 </span><span class="sxs-lookup"><span data-stu-id="eee87-1238">A period</span></span> 
- <span data-ttu-id="eee87-1239">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1239">Three digits</span></span> 
- <span data-ttu-id="eee87-1240">대시 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-1240">A dash</span></span> 
- <span data-ttu-id="eee87-1241">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1242">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1242">Checksum</span></span>

<span data-ttu-id="eee87-1243">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1244">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1244">Definition</span></span>

<span data-ttu-id="eee87-1245">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1246">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1247">Keyword_chile_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="eee87-1248">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1248">The checksum passes.</span></span>

<span data-ttu-id="eee87-1249">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1250">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1251">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1251">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1252">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="eee87-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="eee87-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="eee87-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="eee87-1254">National Identification Number</span></span> 
- <span data-ttu-id="eee87-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="eee87-1255">Identity card</span></span> 
- <span data-ttu-id="eee87-1256">ID</span><span class="sxs-lookup"><span data-stu-id="eee87-1256">ID</span></span> 
- <span data-ttu-id="eee87-1257">확인과</span><span class="sxs-lookup"><span data-stu-id="eee87-1257">Identification</span></span> 
- <span data-ttu-id="eee87-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="eee87-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="eee87-1259">실행</span><span class="sxs-lookup"><span data-stu-id="eee87-1259">RUN</span></span> 
- <span data-ttu-id="eee87-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="eee87-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="eee87-1261">RUT</span><span class="sxs-lookup"><span data-stu-id="eee87-1261">RUT</span></span> 
- <span data-ttu-id="eee87-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="eee87-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="eee87-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="eee87-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="eee87-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="eee87-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="eee87-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="eee87-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="eee87-1266">	중국 주민 ID 카드(PRC) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1267">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1267">Format</span></span>

<span data-ttu-id="eee87-1268">18자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1269">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1269">Pattern</span></span>

<span data-ttu-id="eee87-1270">18자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-1270">18 digits:</span></span>
- <span data-ttu-id="eee87-1271">주소 코드에 해당하는 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="eee87-1272">생년월일에 해당하는 YYYYMMDD 형식의 8자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="eee87-1273">주문 코드에 해당하는 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="eee87-1274">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1275">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1275">Checksum</span></span>

<span data-ttu-id="eee87-1276">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1277">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1277">Definition</span></span>

<span data-ttu-id="eee87-1278">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1279">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1280">Keyword_china_resident_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="eee87-1281">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1281">The checksum passes.</span></span>

<span data-ttu-id="eee87-1282">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1283">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1284">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1284">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1285">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="eee87-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="eee87-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="eee87-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="eee87-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="eee87-1288">중국</span><span class="sxs-lookup"><span data-stu-id="eee87-1288">PRC</span></span> 
- <span data-ttu-id="eee87-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="eee87-1289">National Identification Card</span></span> 
- <span data-ttu-id="eee87-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="eee87-1290">身份证</span></span> 
- <span data-ttu-id="eee87-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="eee87-1291">居民 身份证</span></span> 
- <span data-ttu-id="eee87-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="eee87-1292">居民身份证</span></span> 
- <span data-ttu-id="eee87-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="eee87-1293">鉴定</span></span> 
- <span data-ttu-id="eee87-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-1294">身分證</span></span> 
- <span data-ttu-id="eee87-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-1295">居民 身份證</span></span>
- <span data-ttu-id="eee87-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="eee87-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="eee87-1297">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1298">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1298">Format</span></span>

<span data-ttu-id="eee87-1299">서식이 있거나 서식이 없을 수 있는 16 자리 (dddddddddddddddd), Luhn 테스트를 통과 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1300">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1300">Pattern</span></span>

<span data-ttu-id="eee87-1301">Visa, MasterCard, Discover Card, JCB, American Express, 상품권 및 식사권을 비롯하여 전 세계 모든 주요 브랜드 카드를 검색하는 매우 복잡하고 강력한 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1302">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1302">Checksum</span></span>

<span data-ttu-id="eee87-1303">있음(Luhn 체크섬)</span><span class="sxs-lookup"><span data-stu-id="eee87-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1304">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1304">Definition</span></span>

<span data-ttu-id="eee87-1305">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1306">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1307">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1307">One of the following is true:</span></span>
    - <span data-ttu-id="eee87-1308">Keyword_cc_verification의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="eee87-1309">Keyword_cc_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="eee87-1310">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-1311">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1311">The checksum passes.</span></span>

<span data-ttu-id="eee87-1312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1313">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1314">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1314">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1315">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="eee87-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="eee87-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="eee87-1317">card verification</span><span class="sxs-lookup"><span data-stu-id="eee87-1317">card verification</span></span>
- <span data-ttu-id="eee87-1318">card identification number</span><span class="sxs-lookup"><span data-stu-id="eee87-1318">card identification number</span></span>
- <span data-ttu-id="eee87-1319">cvn</span><span class="sxs-lookup"><span data-stu-id="eee87-1319">cvn</span></span>
- <span data-ttu-id="eee87-1320">cid</span><span class="sxs-lookup"><span data-stu-id="eee87-1320">cid</span></span>
- <span data-ttu-id="eee87-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="eee87-1321">cvc2</span></span>
- <span data-ttu-id="eee87-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="eee87-1322">cvv2</span></span>
- <span data-ttu-id="eee87-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="eee87-1323">pin block</span></span>
- <span data-ttu-id="eee87-1324">security code</span><span class="sxs-lookup"><span data-stu-id="eee87-1324">security code</span></span>
- <span data-ttu-id="eee87-1325">security number</span><span class="sxs-lookup"><span data-stu-id="eee87-1325">security number</span></span>
- <span data-ttu-id="eee87-1326">security no</span><span class="sxs-lookup"><span data-stu-id="eee87-1326">security no</span></span>
- <span data-ttu-id="eee87-1327">issue number</span><span class="sxs-lookup"><span data-stu-id="eee87-1327">issue number</span></span>
- <span data-ttu-id="eee87-1328">issue no</span><span class="sxs-lookup"><span data-stu-id="eee87-1328">issue no</span></span>
- <span data-ttu-id="eee87-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="eee87-1329">cryptogramme</span></span>
- <span data-ttu-id="eee87-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="eee87-1330">numéro de sécurité</span></span>
- <span data-ttu-id="eee87-1331">numero de securite</span><span class="sxs-lookup"><span data-stu-id="eee87-1331">numero de securite</span></span>
- <span data-ttu-id="eee87-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="eee87-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="eee87-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="eee87-1334">prüfziffer</span></span>
- <span data-ttu-id="eee87-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="eee87-1335">prufziffer</span></span>
- <span data-ttu-id="eee87-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="eee87-1336">sicherheits Kode</span></span>
- <span data-ttu-id="eee87-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="eee87-1337">sicherheitscode</span></span>
- <span data-ttu-id="eee87-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="eee87-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="eee87-1339">verfalldatum</span></span>
- <span data-ttu-id="eee87-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="eee87-1340">codice di verifica</span></span>
- <span data-ttu-id="eee87-1341">cod.</span><span class="sxs-lookup"><span data-stu-id="eee87-1341">cod.</span></span> <span data-ttu-id="eee87-1342">sicurezza</span><span class="sxs-lookup"><span data-stu-id="eee87-1342">sicurezza</span></span>
- <span data-ttu-id="eee87-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="eee87-1343">cod sicurezza</span></span>
- <span data-ttu-id="eee87-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="eee87-1344">n autorizzazione</span></span>
- <span data-ttu-id="eee87-1345">código</span><span class="sxs-lookup"><span data-stu-id="eee87-1345">código</span></span>
- <span data-ttu-id="eee87-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="eee87-1346">codigo</span></span>
- <span data-ttu-id="eee87-1347">cod.</span><span class="sxs-lookup"><span data-stu-id="eee87-1347">cod.</span></span> <span data-ttu-id="eee87-1348">seg</span><span class="sxs-lookup"><span data-stu-id="eee87-1348">seg</span></span>
- <span data-ttu-id="eee87-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="eee87-1349">cod seg</span></span>
- <span data-ttu-id="eee87-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1350">código de segurança</span></span>
- <span data-ttu-id="eee87-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1351">codigo de seguranca</span></span>
- <span data-ttu-id="eee87-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1352">codigo de segurança</span></span>
- <span data-ttu-id="eee87-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1353">código de seguranca</span></span>
- <span data-ttu-id="eee87-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="eee87-1354">cód.</span></span> <span data-ttu-id="eee87-1355">segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1355">segurança</span></span>
- <span data-ttu-id="eee87-1356">cod.</span><span class="sxs-lookup"><span data-stu-id="eee87-1356">cod.</span></span> <span data-ttu-id="eee87-1357">seguranca cod</span><span class="sxs-lookup"><span data-stu-id="eee87-1357">seguranca cod.</span></span> <span data-ttu-id="eee87-1358">segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1358">segurança</span></span>
- <span data-ttu-id="eee87-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="eee87-1359">cód.</span></span> <span data-ttu-id="eee87-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1360">seguranca</span></span>
- <span data-ttu-id="eee87-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1361">cód segurança</span></span>
- <span data-ttu-id="eee87-1362">cod seguranca cod segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="eee87-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1363">cód seguranca</span></span>
- <span data-ttu-id="eee87-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="eee87-1364">número de verificação</span></span>
- <span data-ttu-id="eee87-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="eee87-1365">numero de verificacao</span></span>
- <span data-ttu-id="eee87-1366">ablauf</span><span class="sxs-lookup"><span data-stu-id="eee87-1366">ablauf</span></span>
- <span data-ttu-id="eee87-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="eee87-1367">gültig bis</span></span>
- <span data-ttu-id="eee87-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="eee87-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="eee87-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="eee87-1369">gultig bis</span></span>
- <span data-ttu-id="eee87-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="eee87-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="eee87-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="eee87-1371">scadenza</span></span>
- <span data-ttu-id="eee87-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="eee87-1372">data scad</span></span>
- <span data-ttu-id="eee87-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="eee87-1373">fecha de expiracion</span></span>
- <span data-ttu-id="eee87-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="eee87-1374">fecha de venc</span></span>
- <span data-ttu-id="eee87-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="eee87-1375">vencimiento</span></span>
- <span data-ttu-id="eee87-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="eee87-1376">válido hasta</span></span>
- <span data-ttu-id="eee87-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="eee87-1377">valido hasta</span></span>
- <span data-ttu-id="eee87-1378">vto</span><span class="sxs-lookup"><span data-stu-id="eee87-1378">vto</span></span>
- <span data-ttu-id="eee87-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="eee87-1379">data de expiração</span></span>
- <span data-ttu-id="eee87-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="eee87-1380">data de expiracao</span></span>
- <span data-ttu-id="eee87-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="eee87-1381">data em que expira</span></span>
- <span data-ttu-id="eee87-1382">유효한 ade</span><span class="sxs-lookup"><span data-stu-id="eee87-1382">validade</span></span>
- <span data-ttu-id="eee87-1383">valor</span><span class="sxs-lookup"><span data-stu-id="eee87-1383">valor</span></span>
- <span data-ttu-id="eee87-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="eee87-1384">vencimento</span></span>
- <span data-ttu-id="eee87-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="eee87-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="eee87-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="eee87-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="eee87-1387">amex</span><span class="sxs-lookup"><span data-stu-id="eee87-1387">amex</span></span>
- <span data-ttu-id="eee87-1388">american express</span><span class="sxs-lookup"><span data-stu-id="eee87-1388">american express</span></span>
- <span data-ttu-id="eee87-1389">americanexpress</span><span class="sxs-lookup"><span data-stu-id="eee87-1389">americanexpress</span></span>
- <span data-ttu-id="eee87-1390">Visa</span><span class="sxs-lookup"><span data-stu-id="eee87-1390">Visa</span></span>
- <span data-ttu-id="eee87-1391">mastercard</span><span class="sxs-lookup"><span data-stu-id="eee87-1391">mastercard</span></span>
- <span data-ttu-id="eee87-1392">master card</span><span class="sxs-lookup"><span data-stu-id="eee87-1392">master card</span></span>
- <span data-ttu-id="eee87-1393">mc</span><span class="sxs-lookup"><span data-stu-id="eee87-1393">mc</span></span> 
- <span data-ttu-id="eee87-1394">mastercards</span><span class="sxs-lookup"><span data-stu-id="eee87-1394">mastercards</span></span>
- <span data-ttu-id="eee87-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1395">master cards</span></span>
- <span data-ttu-id="eee87-1396">diner's Club</span><span class="sxs-lookup"><span data-stu-id="eee87-1396">diner's Club</span></span>
- <span data-ttu-id="eee87-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="eee87-1397">diners club</span></span>
- <span data-ttu-id="eee87-1398">dinersclub</span><span class="sxs-lookup"><span data-stu-id="eee87-1398">dinersclub</span></span>
- <span data-ttu-id="eee87-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="eee87-1399">discover card</span></span>
- <span data-ttu-id="eee87-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="eee87-1400">discovercard</span></span>
- <span data-ttu-id="eee87-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1401">discover cards</span></span>
- <span data-ttu-id="eee87-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="eee87-1402">JCB</span></span>
- <span data-ttu-id="eee87-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="eee87-1403">japanese card bureau</span></span>
- <span data-ttu-id="eee87-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="eee87-1404">carte blanche</span></span>
- <span data-ttu-id="eee87-1405">carteblanche</span><span class="sxs-lookup"><span data-stu-id="eee87-1405">carteblanche</span></span>
- <span data-ttu-id="eee87-1406">credit card</span><span class="sxs-lookup"><span data-stu-id="eee87-1406">credit card</span></span>
- <span data-ttu-id="eee87-1407">참조란 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1407">cc#</span></span>
- <span data-ttu-id="eee87-1408">참조 #:</span><span class="sxs-lookup"><span data-stu-id="eee87-1408">cc#:</span></span>
- <span data-ttu-id="eee87-1409">expiration date</span><span class="sxs-lookup"><span data-stu-id="eee87-1409">expiration date</span></span>
- <span data-ttu-id="eee87-1410">exp date</span><span class="sxs-lookup"><span data-stu-id="eee87-1410">exp date</span></span>
- <span data-ttu-id="eee87-1411">expiry date</span><span class="sxs-lookup"><span data-stu-id="eee87-1411">expiry date</span></span>
- <span data-ttu-id="eee87-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="eee87-1412">date d’expiration</span></span>
- <span data-ttu-id="eee87-1413">date d'exp</span><span class="sxs-lookup"><span data-stu-id="eee87-1413">date d'exp</span></span>
- <span data-ttu-id="eee87-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="eee87-1414">date expiration</span></span>
- <span data-ttu-id="eee87-1415">bank card</span><span class="sxs-lookup"><span data-stu-id="eee87-1415">bank card</span></span>
- <span data-ttu-id="eee87-1416">bankcard</span><span class="sxs-lookup"><span data-stu-id="eee87-1416">bankcard</span></span>
- <span data-ttu-id="eee87-1417">card number</span><span class="sxs-lookup"><span data-stu-id="eee87-1417">card number</span></span>
- <span data-ttu-id="eee87-1418">card num</span><span class="sxs-lookup"><span data-stu-id="eee87-1418">card num</span></span>
- <span data-ttu-id="eee87-1419">전화 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1419">cardnumber</span></span>
- <span data-ttu-id="eee87-1420">시 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1420">cardnumbers</span></span>
- <span data-ttu-id="eee87-1421">card numbers</span><span class="sxs-lookup"><span data-stu-id="eee87-1421">card numbers</span></span>
- <span data-ttu-id="eee87-1422">카드</span><span class="sxs-lookup"><span data-stu-id="eee87-1422">creditcard</span></span>
- <span data-ttu-id="eee87-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1423">credit cards</span></span>
- <span data-ttu-id="eee87-1424">creditcards</span><span class="sxs-lookup"><span data-stu-id="eee87-1424">creditcards</span></span>
- <span data-ttu-id="eee87-1425">ccn</span><span class="sxs-lookup"><span data-stu-id="eee87-1425">ccn</span></span>
- <span data-ttu-id="eee87-1426">card holder</span><span class="sxs-lookup"><span data-stu-id="eee87-1426">card holder</span></span>
- <span data-ttu-id="eee87-1427">소유자</span><span class="sxs-lookup"><span data-stu-id="eee87-1427">cardholder</span></span>
- <span data-ttu-id="eee87-1428">card holders</span><span class="sxs-lookup"><span data-stu-id="eee87-1428">card holders</span></span>
- <span data-ttu-id="eee87-1429">에이 홀더</span><span class="sxs-lookup"><span data-stu-id="eee87-1429">cardholders</span></span>
- <span data-ttu-id="eee87-1430">check card</span><span class="sxs-lookup"><span data-stu-id="eee87-1430">check card</span></span>
- <span data-ttu-id="eee87-1431">checkcard</span><span class="sxs-lookup"><span data-stu-id="eee87-1431">checkcard</span></span>
- <span data-ttu-id="eee87-1432">check cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1432">check cards</span></span>
- <span data-ttu-id="eee87-1433">checkcards</span><span class="sxs-lookup"><span data-stu-id="eee87-1433">checkcards</span></span>
- <span data-ttu-id="eee87-1434">debit card</span><span class="sxs-lookup"><span data-stu-id="eee87-1434">debit card</span></span>
- <span data-ttu-id="eee87-1435">debitcard</span><span class="sxs-lookup"><span data-stu-id="eee87-1435">debitcard</span></span>
- <span data-ttu-id="eee87-1436">debit cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1436">debit cards</span></span>
- <span data-ttu-id="eee87-1437">debitcards</span><span class="sxs-lookup"><span data-stu-id="eee87-1437">debitcards</span></span>
- <span data-ttu-id="eee87-1438">atm card</span><span class="sxs-lookup"><span data-stu-id="eee87-1438">atm card</span></span>
- <span data-ttu-id="eee87-1439">atmcard</span><span class="sxs-lookup"><span data-stu-id="eee87-1439">atmcard</span></span>
- <span data-ttu-id="eee87-1440">atm cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1440">atm cards</span></span>
- <span data-ttu-id="eee87-1441">atmcards</span><span class="sxs-lookup"><span data-stu-id="eee87-1441">atmcards</span></span>
- <span data-ttu-id="eee87-1442">enroute</span><span class="sxs-lookup"><span data-stu-id="eee87-1442">enroute</span></span>
- <span data-ttu-id="eee87-1443">en route</span><span class="sxs-lookup"><span data-stu-id="eee87-1443">en route</span></span>
- <span data-ttu-id="eee87-1444">card type</span><span class="sxs-lookup"><span data-stu-id="eee87-1444">card type</span></span>
- <span data-ttu-id="eee87-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="eee87-1445">carte bancaire</span></span>
- <span data-ttu-id="eee87-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="eee87-1446">carte de crédit</span></span>
- <span data-ttu-id="eee87-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="eee87-1447">carte de credit</span></span>
- <span data-ttu-id="eee87-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="eee87-1448">numéro de carte</span></span>
- <span data-ttu-id="eee87-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="eee87-1449">numero de carte</span></span>
- <span data-ttu-id="eee87-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="eee87-1450">nº de la carte</span></span>
- <span data-ttu-id="eee87-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="eee87-1451">nº de carte</span></span>
- <span data-ttu-id="eee87-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="eee87-1452">kreditkarte</span></span>
- <span data-ttu-id="eee87-1453">karte</span><span class="sxs-lookup"><span data-stu-id="eee87-1453">karte</span></span>
- <span data-ttu-id="eee87-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="eee87-1454">karteninhaber</span></span>
- <span data-ttu-id="eee87-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="eee87-1455">karteninhabers</span></span>
- <span data-ttu-id="eee87-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="eee87-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="eee87-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="eee87-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="eee87-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="eee87-1458">kreditkartentyp</span></span>
- <span data-ttu-id="eee87-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="eee87-1459">eigentümername</span></span>
- <span data-ttu-id="eee87-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="eee87-1460">kartennr</span></span> 
- <span data-ttu-id="eee87-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1461">kartennummer</span></span>
- <span data-ttu-id="eee87-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1462">kreditkartennummer</span></span>
- <span data-ttu-id="eee87-1463">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="eee87-1464">carta di credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1464">carta di credito</span></span>
- <span data-ttu-id="eee87-1465">carta credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1465">carta credito</span></span>
- <span data-ttu-id="eee87-1466">카 ta</span><span class="sxs-lookup"><span data-stu-id="eee87-1466">carta</span></span>
- <span data-ttu-id="eee87-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1467">n carta</span></span>
- <span data-ttu-id="eee87-1468">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="eee87-1468">nr.</span></span> <span data-ttu-id="eee87-1469">카 ta</span><span class="sxs-lookup"><span data-stu-id="eee87-1469">carta</span></span>
- <span data-ttu-id="eee87-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1470">nr carta</span></span>
- <span data-ttu-id="eee87-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1471">numero carta</span></span>
- <span data-ttu-id="eee87-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1472">numero della carta</span></span>
- <span data-ttu-id="eee87-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1473">numero di carta</span></span>
- <span data-ttu-id="eee87-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1474">tarjeta credito</span></span>
- <span data-ttu-id="eee87-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1475">tarjeta de credito</span></span>
- <span data-ttu-id="eee87-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="eee87-1476">tarjeta crédito</span></span>
- <span data-ttu-id="eee87-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="eee87-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="eee87-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="eee87-1478">tarjeta de atm</span></span>
- <span data-ttu-id="eee87-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="eee87-1479">tarjeta atm</span></span>
- <span data-ttu-id="eee87-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1480">tarjeta debito</span></span>
- <span data-ttu-id="eee87-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1481">tarjeta de debito</span></span>
- <span data-ttu-id="eee87-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="eee87-1482">tarjeta débito</span></span>
- <span data-ttu-id="eee87-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="eee87-1483">tarjeta de débito</span></span>
- <span data-ttu-id="eee87-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1484">nº de tarjeta</span></span>
- <span data-ttu-id="eee87-1485">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1485">no.</span></span> <span data-ttu-id="eee87-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1486">de tarjeta</span></span>
- <span data-ttu-id="eee87-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1487">no de tarjeta</span></span>
- <span data-ttu-id="eee87-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1488">numero de tarjeta</span></span>
- <span data-ttu-id="eee87-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1489">número de tarjeta</span></span>
- <span data-ttu-id="eee87-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="eee87-1490">tarjeta no</span></span>
- <span data-ttu-id="eee87-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="eee87-1491">tarjetahabiente</span></span>
- <span data-ttu-id="eee87-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="eee87-1492">cartão de crédito</span></span>
- <span data-ttu-id="eee87-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1493">cartão de credito</span></span>
- <span data-ttu-id="eee87-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="eee87-1494">cartao de crédito</span></span>
- <span data-ttu-id="eee87-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1495">cartao de credito</span></span>
- <span data-ttu-id="eee87-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="eee87-1496">cartão de débito</span></span>
- <span data-ttu-id="eee87-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="eee87-1497">cartao de débito</span></span>
- <span data-ttu-id="eee87-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1498">cartão de debito</span></span>
- <span data-ttu-id="eee87-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1499">cartao de debito</span></span>
- <span data-ttu-id="eee87-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="eee87-1500">débito automático</span></span>
- <span data-ttu-id="eee87-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="eee87-1501">debito automatico</span></span>
- <span data-ttu-id="eee87-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1502">número do cartão</span></span>
- <span data-ttu-id="eee87-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1503">numero do cartão</span></span> 
- <span data-ttu-id="eee87-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1504">número do cartao</span></span>
- <span data-ttu-id="eee87-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1505">numero do cartao</span></span>
- <span data-ttu-id="eee87-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1506">número de cartão</span></span>
- <span data-ttu-id="eee87-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1507">numero de cartão</span></span>
- <span data-ttu-id="eee87-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1508">número de cartao</span></span>
- <span data-ttu-id="eee87-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1509">numero de cartao</span></span>
- <span data-ttu-id="eee87-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1510">nº do cartão</span></span>
- <span data-ttu-id="eee87-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1511">nº do cartao</span></span>
- <span data-ttu-id="eee87-1512">n º</span><span class="sxs-lookup"><span data-stu-id="eee87-1512">nº.</span></span> <span data-ttu-id="eee87-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1513">do cartão</span></span>
- <span data-ttu-id="eee87-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1514">no do cartão</span></span>
- <span data-ttu-id="eee87-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1515">no do cartao</span></span>
- <span data-ttu-id="eee87-1516">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1516">no.</span></span> <span data-ttu-id="eee87-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1517">do cartão</span></span>
- <span data-ttu-id="eee87-1518">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1518">no.</span></span> <span data-ttu-id="eee87-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="eee87-1520">크로아티아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1521">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1521">Format</span></span>

<span data-ttu-id="eee87-1522">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1523">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1523">Pattern</span></span>

<span data-ttu-id="eee87-1524">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1525">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1525">Checksum</span></span>

<span data-ttu-id="eee87-1526">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1527">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1527">Definition</span></span>

<span data-ttu-id="eee87-1528">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1529">Func_croatia_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1530">Keyword_croatia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```xml
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-1531">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="eee87-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="eee87-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="eee87-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="eee87-1533">Croatian identity card</span></span>
- <span data-ttu-id="eee87-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="eee87-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="eee87-1535">크로아티아 개인 식별(OIB) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1536">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1536">Format</span></span>

<span data-ttu-id="eee87-1537">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1538">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1538">Pattern</span></span>

<span data-ttu-id="eee87-1539">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-1539">11 digits:</span></span>
- <span data-ttu-id="eee87-1540">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1540">10 digits</span></span> 
- <span data-ttu-id="eee87-1541">최종 자릿수는 국제 데이터 교환 목적을 위한 검사 숫자 이며, HR는 11 자리 숫자 앞에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1542">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1542">Checksum</span></span>

<span data-ttu-id="eee87-1543">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1544">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1544">Definition</span></span>

<span data-ttu-id="eee87-1545">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1546">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1547">Keyword_croatia_oib_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="eee87-1548">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1548">The checksum passes.</span></span>

<span data-ttu-id="eee87-1549">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1550">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1551">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1551">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1552">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="eee87-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="eee87-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="eee87-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="eee87-1554">Personal Identification Number</span></span>
- <span data-ttu-id="eee87-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="eee87-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="eee87-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="eee87-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="eee87-1557">체코어 개인 Id 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1558">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1558">Format</span></span>

<span data-ttu-id="eee87-1559">선택적 슬래시 (이전 형식)가 있는 9 자리 숫자와 슬래시 (새 형식)가 있는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1560">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1560">Pattern</span></span>

<span data-ttu-id="eee87-1561">9 자리 숫자 (이전 형식):</span><span class="sxs-lookup"><span data-stu-id="eee87-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="eee87-1562">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1562">Nine digits</span></span>

<span data-ttu-id="eee87-1563">또는</span><span class="sxs-lookup"><span data-stu-id="eee87-1563">OR</span></span>

- <span data-ttu-id="eee87-1564">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="eee87-1565">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="eee87-1565">A forward slash</span></span>
- <span data-ttu-id="eee87-1566">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1566">Three digits</span></span>

<span data-ttu-id="eee87-1567">10 자리 숫자 (새 형식):</span><span class="sxs-lookup"><span data-stu-id="eee87-1567">10 digits (new format):</span></span>
- <span data-ttu-id="eee87-1568">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1568">10 digits</span></span>

<span data-ttu-id="eee87-1569">또는</span><span class="sxs-lookup"><span data-stu-id="eee87-1569">OR</span></span>

- <span data-ttu-id="eee87-1570">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="eee87-1571">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="eee87-1571">A forward slash</span></span> 
- <span data-ttu-id="eee87-1572">마지막 숫자가 검사 숫자인 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1573">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1573">Checksum</span></span>

<span data-ttu-id="eee87-1574">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1575">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1575">Definition</span></span>

<span data-ttu-id="eee87-1576">DLP 정책은 300 문자 근사에서 Func_czech_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="eee87-1577">Keyword_czech_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="eee87-1578">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1578">The checksum passes.</span></span>

```xml
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="eee87-1579">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1579">Keywords</span></span>

- <span data-ttu-id="eee87-1580">체코어 개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1580">czech personal identity number</span></span>
- <span data-ttu-id="eee87-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="eee87-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="eee87-1582">덴마크 개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1583">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1583">Format</span></span>

<span data-ttu-id="eee87-1584">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1585">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1585">Pattern</span></span>

<span data-ttu-id="eee87-1586">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-1586">10 digits:</span></span>
- <span data-ttu-id="eee87-1587">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="eee87-1588">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-1588">A hyphen</span></span> 
- <span data-ttu-id="eee87-1589">마지막 숫자가 검사 숫자인 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1590">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1590">Checksum</span></span>

<span data-ttu-id="eee87-1591">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1592">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1592">Definition</span></span>

<span data-ttu-id="eee87-1593">DLP 정책은 300 문자 (예: Regex_denmark_id)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="eee87-1594">Keyword_denmark_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="eee87-1595">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1595">The checksum passes.</span></span>

```xml
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-1596">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="eee87-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="eee87-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="eee87-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="eee87-1598">Personal Identification Number</span></span>
- <span data-ttu-id="eee87-1599">CPR</span><span class="sxs-lookup"><span data-stu-id="eee87-1599">CPR</span></span>
- <span data-ttu-id="eee87-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="eee87-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="eee87-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="eee87-1602">DEA(약물 집행 기구) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1603">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1603">Format</span></span>

<span data-ttu-id="eee87-1604">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1605">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1605">Pattern</span></span>

<span data-ttu-id="eee87-1606">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="eee87-1607">등록 코드에 해당하는 abcdefghjklmnprstux 중 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="eee87-1608">등록자 성의 첫 문자에 해당하는 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="eee87-1609">검사 숫자의 마지막 7개 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1610">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1610">Checksum</span></span>

<span data-ttu-id="eee87-1611">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1612">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1612">Definition</span></span>

<span data-ttu-id="eee87-1613">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1614">Func_dea_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1615">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1615">The checksum passes.</span></span>

```xml
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-1616">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1616">Keywords</span></span>

<span data-ttu-id="eee87-1617">없음</span><span class="sxs-lookup"><span data-stu-id="eee87-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="eee87-1618">유럽 직불 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1619">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1619">Format</span></span>

<span data-ttu-id="eee87-1620">16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1621">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1621">Pattern</span></span>

<span data-ttu-id="eee87-1622">매우 복잡하고 강력한 패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1623">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1623">Checksum</span></span>

<span data-ttu-id="eee87-1624">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1625">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1625">Definition</span></span>

<span data-ttu-id="eee87-1626">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1627">Func_eu_debit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1628">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="eee87-1629">Keyword_eu_debit_card의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="eee87-1630">Keyword_card_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="eee87-1631">Keyword_card_security_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="eee87-1632">Keyword_card_expiration_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="eee87-1633">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-1634">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1634">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1635">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="eee87-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="eee87-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="eee87-1637">account number</span><span class="sxs-lookup"><span data-stu-id="eee87-1637">account number</span></span> 
- <span data-ttu-id="eee87-1638">card number</span><span class="sxs-lookup"><span data-stu-id="eee87-1638">card number</span></span> 
- <span data-ttu-id="eee87-1639">card no.</span><span class="sxs-lookup"><span data-stu-id="eee87-1639">card no.</span></span> 
- <span data-ttu-id="eee87-1640">security number</span><span class="sxs-lookup"><span data-stu-id="eee87-1640">security number</span></span> 
- <span data-ttu-id="eee87-1641">참조란 #</span><span class="sxs-lookup"><span data-stu-id="eee87-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="eee87-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="eee87-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="eee87-1643">acct nbr</span><span class="sxs-lookup"><span data-stu-id="eee87-1643">acct nbr</span></span> 
- <span data-ttu-id="eee87-1644">acct num</span><span class="sxs-lookup"><span data-stu-id="eee87-1644">acct num</span></span> 
- <span data-ttu-id="eee87-1645">acct no</span><span class="sxs-lookup"><span data-stu-id="eee87-1645">acct no</span></span> 
- <span data-ttu-id="eee87-1646">american express</span><span class="sxs-lookup"><span data-stu-id="eee87-1646">american express</span></span> 
- <span data-ttu-id="eee87-1647">americanexpress</span><span class="sxs-lookup"><span data-stu-id="eee87-1647">americanexpress</span></span> 
- <span data-ttu-id="eee87-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="eee87-1648">americano espresso</span></span> 
- <span data-ttu-id="eee87-1649">amex</span><span class="sxs-lookup"><span data-stu-id="eee87-1649">amex</span></span> 
- <span data-ttu-id="eee87-1650">atm card</span><span class="sxs-lookup"><span data-stu-id="eee87-1650">atm card</span></span> 
- <span data-ttu-id="eee87-1651">atm cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1651">atm cards</span></span> 
- <span data-ttu-id="eee87-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="eee87-1652">atm kaart</span></span> 
- <span data-ttu-id="eee87-1653">atmcard</span><span class="sxs-lookup"><span data-stu-id="eee87-1653">atmcard</span></span> 
- <span data-ttu-id="eee87-1654">atmcards</span><span class="sxs-lookup"><span data-stu-id="eee87-1654">atmcards</span></span> 
- <span data-ttu-id="eee87-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="eee87-1655">atmkaart</span></span> 
- <span data-ttu-id="eee87-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="eee87-1656">atmkaarten</span></span> 
- <span data-ttu-id="eee87-1657">bancontact</span><span class="sxs-lookup"><span data-stu-id="eee87-1657">bancontact</span></span> 
- <span data-ttu-id="eee87-1658">bank card</span><span class="sxs-lookup"><span data-stu-id="eee87-1658">bank card</span></span> 
- <span data-ttu-id="eee87-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="eee87-1659">bankkaart</span></span> 
- <span data-ttu-id="eee87-1660">card holder</span><span class="sxs-lookup"><span data-stu-id="eee87-1660">card holder</span></span> 
- <span data-ttu-id="eee87-1661">card holders</span><span class="sxs-lookup"><span data-stu-id="eee87-1661">card holders</span></span> 
- <span data-ttu-id="eee87-1662">card num</span><span class="sxs-lookup"><span data-stu-id="eee87-1662">card num</span></span> 
- <span data-ttu-id="eee87-1663">card number</span><span class="sxs-lookup"><span data-stu-id="eee87-1663">card number</span></span> 
- <span data-ttu-id="eee87-1664">card numbers</span><span class="sxs-lookup"><span data-stu-id="eee87-1664">card numbers</span></span> 
- <span data-ttu-id="eee87-1665">card type</span><span class="sxs-lookup"><span data-stu-id="eee87-1665">card type</span></span> 
- <span data-ttu-id="eee87-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="eee87-1666">cardano numerico</span></span> 
- <span data-ttu-id="eee87-1667">소유자</span><span class="sxs-lookup"><span data-stu-id="eee87-1667">cardholder</span></span> 
- <span data-ttu-id="eee87-1668">에이 홀더</span><span class="sxs-lookup"><span data-stu-id="eee87-1668">cardholders</span></span> 
- <span data-ttu-id="eee87-1669">전화 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1669">cardnumber</span></span> 
- <span data-ttu-id="eee87-1670">시 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1670">cardnumbers</span></span> 
- <span data-ttu-id="eee87-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="eee87-1671">carta bianca</span></span> 
- <span data-ttu-id="eee87-1672">carta credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1672">carta credito</span></span> 
- <span data-ttu-id="eee87-1673">carta di credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1673">carta di credito</span></span> 
- <span data-ttu-id="eee87-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1674">cartao de credito</span></span> 
- <span data-ttu-id="eee87-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="eee87-1675">cartao de crédito</span></span> 
- <span data-ttu-id="eee87-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1676">cartao de debito</span></span> 
- <span data-ttu-id="eee87-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="eee87-1677">cartao de débito</span></span> 
- <span data-ttu-id="eee87-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="eee87-1678">carte bancaire</span></span> 
- <span data-ttu-id="eee87-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="eee87-1679">carte blanche</span></span> 
- <span data-ttu-id="eee87-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="eee87-1680">carte bleue</span></span> 
- <span data-ttu-id="eee87-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="eee87-1681">carte de credit</span></span> 
- <span data-ttu-id="eee87-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="eee87-1682">carte de crédit</span></span> 
- <span data-ttu-id="eee87-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1683">carte di credito</span></span> 
- <span data-ttu-id="eee87-1684">carteblanche</span><span class="sxs-lookup"><span data-stu-id="eee87-1684">carteblanche</span></span> 
- <span data-ttu-id="eee87-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1685">cartão de credito</span></span> 
- <span data-ttu-id="eee87-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="eee87-1686">cartão de crédito</span></span> 
- <span data-ttu-id="eee87-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1687">cartão de debito</span></span> 
- <span data-ttu-id="eee87-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="eee87-1688">cartão de débito</span></span> 
- <span data-ttu-id="eee87-1689">cb</span><span class="sxs-lookup"><span data-stu-id="eee87-1689">cb</span></span> 
- <span data-ttu-id="eee87-1690">ccn</span><span class="sxs-lookup"><span data-stu-id="eee87-1690">ccn</span></span> 
- <span data-ttu-id="eee87-1691">check card</span><span class="sxs-lookup"><span data-stu-id="eee87-1691">check card</span></span> 
- <span data-ttu-id="eee87-1692">check cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1692">check cards</span></span> 
- <span data-ttu-id="eee87-1693">checkcard</span><span class="sxs-lookup"><span data-stu-id="eee87-1693">checkcard</span></span>
- <span data-ttu-id="eee87-1694">checkcards</span><span class="sxs-lookup"><span data-stu-id="eee87-1694">checkcards</span></span> 
- <span data-ttu-id="eee87-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="eee87-1695">chequekaart</span></span> 
- <span data-ttu-id="eee87-1696">cirrus</span><span class="sxs-lookup"><span data-stu-id="eee87-1696">cirrus</span></span> 
- <span data-ttu-id="eee87-1697">cirrus-edc-maestro</span><span class="sxs-lookup"><span data-stu-id="eee87-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="eee87-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="eee87-1698">controlekaart</span></span> 
- <span data-ttu-id="eee87-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="eee87-1699">controlekaarten</span></span> 
- <span data-ttu-id="eee87-1700">credit card</span><span class="sxs-lookup"><span data-stu-id="eee87-1700">credit card</span></span> 
- <span data-ttu-id="eee87-1701">credit cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1701">credit cards</span></span> 
- <span data-ttu-id="eee87-1702">카드</span><span class="sxs-lookup"><span data-stu-id="eee87-1702">creditcard</span></span> 
- <span data-ttu-id="eee87-1703">creditcards</span><span class="sxs-lookup"><span data-stu-id="eee87-1703">creditcards</span></span> 
- <span data-ttu-id="eee87-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="eee87-1704">debetkaart</span></span> 
- <span data-ttu-id="eee87-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="eee87-1705">debetkaarten</span></span> 
- <span data-ttu-id="eee87-1706">debit card</span><span class="sxs-lookup"><span data-stu-id="eee87-1706">debit card</span></span> 
- <span data-ttu-id="eee87-1707">debit cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1707">debit cards</span></span> 
- <span data-ttu-id="eee87-1708">debitcard</span><span class="sxs-lookup"><span data-stu-id="eee87-1708">debitcard</span></span> 
- <span data-ttu-id="eee87-1709">debitcards</span><span class="sxs-lookup"><span data-stu-id="eee87-1709">debitcards</span></span> 
- <span data-ttu-id="eee87-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="eee87-1710">debito automatico</span></span> 
- <span data-ttu-id="eee87-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="eee87-1711">diners club</span></span> 
- <span data-ttu-id="eee87-1712">dinersclub</span><span class="sxs-lookup"><span data-stu-id="eee87-1712">dinersclub</span></span> 
- <span data-ttu-id="eee87-1713">찾아보십시오</span><span class="sxs-lookup"><span data-stu-id="eee87-1713">discover</span></span> 
- <span data-ttu-id="eee87-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="eee87-1714">discover card</span></span> 
- <span data-ttu-id="eee87-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1715">discover cards</span></span> 
- <span data-ttu-id="eee87-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="eee87-1716">discovercard</span></span> 
- <span data-ttu-id="eee87-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="eee87-1717">discovercards</span></span> 
- <span data-ttu-id="eee87-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="eee87-1718">débito automático</span></span>
- <span data-ttu-id="eee87-1719">edc</span><span class="sxs-lookup"><span data-stu-id="eee87-1719">edc</span></span> 
- <span data-ttu-id="eee87-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="eee87-1720">eigentümername</span></span> 
- <span data-ttu-id="eee87-1721">european debit card</span><span class="sxs-lookup"><span data-stu-id="eee87-1721">european debit card</span></span> 
- <span data-ttu-id="eee87-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="eee87-1722">hoofdkaart</span></span> 
- <span data-ttu-id="eee87-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="eee87-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="eee87-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="eee87-1724">in viaggio</span></span> 
- <span data-ttu-id="eee87-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="eee87-1725">japanese card bureau</span></span> 
- <span data-ttu-id="eee87-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="eee87-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="eee87-1727">jcb</span><span class="sxs-lookup"><span data-stu-id="eee87-1727">jcb</span></span> 
- <span data-ttu-id="eee87-1728">kaart</span><span class="sxs-lookup"><span data-stu-id="eee87-1728">kaart</span></span> 
- <span data-ttu-id="eee87-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="eee87-1729">kaart num</span></span> 
- <span data-ttu-id="eee87-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="eee87-1730">kaartaantal</span></span> 
- <span data-ttu-id="eee87-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="eee87-1731">kaartaantallen</span></span> 
- <span data-ttu-id="eee87-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="eee87-1732">kaarthouder</span></span> 
- <span data-ttu-id="eee87-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="eee87-1733">kaarthouders</span></span> 
- <span data-ttu-id="eee87-1734">karte</span><span class="sxs-lookup"><span data-stu-id="eee87-1734">karte</span></span>  
- <span data-ttu-id="eee87-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="eee87-1735">karteninhaber</span></span> 
- <span data-ttu-id="eee87-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="eee87-1736">karteninhabers</span></span>
- <span data-ttu-id="eee87-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="eee87-1737">kartennr</span></span> 
- <span data-ttu-id="eee87-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1738">kartennummer</span></span> 
- <span data-ttu-id="eee87-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="eee87-1739">kreditkarte</span></span> 
- <span data-ttu-id="eee87-1740">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="eee87-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="eee87-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="eee87-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="eee87-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="eee87-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="eee87-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="eee87-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="eee87-1745">maestro</span><span class="sxs-lookup"><span data-stu-id="eee87-1745">maestro</span></span> 
- <span data-ttu-id="eee87-1746">master card</span><span class="sxs-lookup"><span data-stu-id="eee87-1746">master card</span></span> 
- <span data-ttu-id="eee87-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="eee87-1747">master cards</span></span> 
- <span data-ttu-id="eee87-1748">mastercard</span><span class="sxs-lookup"><span data-stu-id="eee87-1748">mastercard</span></span> 
- <span data-ttu-id="eee87-1749">mastercards</span><span class="sxs-lookup"><span data-stu-id="eee87-1749">mastercards</span></span> 
- <span data-ttu-id="eee87-1750">mc</span><span class="sxs-lookup"><span data-stu-id="eee87-1750">mc</span></span> 
- <span data-ttu-id="eee87-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="eee87-1751">mister cash</span></span> 
- <span data-ttu-id="eee87-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1752">n carta</span></span> 
- <span data-ttu-id="eee87-1753">카 ta</span><span class="sxs-lookup"><span data-stu-id="eee87-1753">carta</span></span> 
- <span data-ttu-id="eee87-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1754">no de tarjeta</span></span> 
- <span data-ttu-id="eee87-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1755">no do cartao</span></span> 
- <span data-ttu-id="eee87-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1756">no do cartão</span></span> 
- <span data-ttu-id="eee87-1757">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1757">no.</span></span> <span data-ttu-id="eee87-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1758">de tarjeta</span></span> 
- <span data-ttu-id="eee87-1759">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1759">no.</span></span> <span data-ttu-id="eee87-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1760">do cartao</span></span> 
- <span data-ttu-id="eee87-1761">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1761">no.</span></span> <span data-ttu-id="eee87-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1762">do cartão</span></span> 
- <span data-ttu-id="eee87-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1763">nr carta</span></span> 
- <span data-ttu-id="eee87-1764">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="eee87-1764">nr.</span></span> <span data-ttu-id="eee87-1765">카 ta</span><span class="sxs-lookup"><span data-stu-id="eee87-1765">carta</span></span> 
- <span data-ttu-id="eee87-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="eee87-1766">numeri di scheda</span></span> 
- <span data-ttu-id="eee87-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1767">numero carta</span></span> 
- <span data-ttu-id="eee87-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1768">numero de cartao</span></span> 
- <span data-ttu-id="eee87-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="eee87-1769">numero de carte</span></span> 
- <span data-ttu-id="eee87-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1770">numero de cartão</span></span> 
- <span data-ttu-id="eee87-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1771">numero de tarjeta</span></span>
- <span data-ttu-id="eee87-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1772">numero della carta</span></span> 
- <span data-ttu-id="eee87-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1773">numero di carta</span></span> 
- <span data-ttu-id="eee87-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="eee87-1774">numero di scheda</span></span> 
- <span data-ttu-id="eee87-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1775">numero do cartao</span></span> 
- <span data-ttu-id="eee87-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1776">numero do cartão</span></span> 
- <span data-ttu-id="eee87-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="eee87-1777">numéro de carte</span></span> 
- <span data-ttu-id="eee87-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="eee87-1778">nº carta</span></span> 
- <span data-ttu-id="eee87-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="eee87-1779">nº de carte</span></span> 
- <span data-ttu-id="eee87-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="eee87-1780">nº de la carte</span></span> 
- <span data-ttu-id="eee87-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="eee87-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1782">nº do cartao</span></span> 
- <span data-ttu-id="eee87-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1783">nº do cartão</span></span> 
- <span data-ttu-id="eee87-1784">n º</span><span class="sxs-lookup"><span data-stu-id="eee87-1784">nº.</span></span> <span data-ttu-id="eee87-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1785">do cartão</span></span> 
- <span data-ttu-id="eee87-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1786">número de cartao</span></span> 
- <span data-ttu-id="eee87-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="eee87-1787">número de cartão</span></span> 
- <span data-ttu-id="eee87-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="eee87-1788">número de tarjeta</span></span> 
- <span data-ttu-id="eee87-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="eee87-1789">número do cartao</span></span> 
- <span data-ttu-id="eee87-1790">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="eee87-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="eee87-1791">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="eee87-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="eee87-1792">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="eee87-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="eee87-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="eee87-1793">scheda della banca</span></span> 
- <span data-ttu-id="eee87-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="eee87-1794">scheda di controllo</span></span> 
- <span data-ttu-id="eee87-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1795">scheda di debito</span></span> 
- <span data-ttu-id="eee87-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="eee87-1796">scheda matrice</span></span> 
- <span data-ttu-id="eee87-1797">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="eee87-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="eee87-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="eee87-1798">schede di controllo</span></span> 
- <span data-ttu-id="eee87-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1799">schede di debito</span></span> 
- <span data-ttu-id="eee87-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="eee87-1800">schede matrici</span></span> 
- <span data-ttu-id="eee87-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="eee87-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="eee87-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="eee87-1802">scoprono le schede</span></span> 
- <span data-ttu-id="eee87-1803">분리</span><span class="sxs-lookup"><span data-stu-id="eee87-1803">solo</span></span> 
- <span data-ttu-id="eee87-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="eee87-1804">supporti di scheda</span></span> 
- <span data-ttu-id="eee87-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="eee87-1805">supporto di scheda</span></span> 
- <span data-ttu-id="eee87-1806">스위치</span><span class="sxs-lookup"><span data-stu-id="eee87-1806">switch</span></span> 
- <span data-ttu-id="eee87-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="eee87-1807">tarjeta atm</span></span> 
- <span data-ttu-id="eee87-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1808">tarjeta credito</span></span> 
- <span data-ttu-id="eee87-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="eee87-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="eee87-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="eee87-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="eee87-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="eee87-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="eee87-1812">tarjeta debito</span></span> 
- <span data-ttu-id="eee87-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="eee87-1813">tarjeta no</span></span>
- <span data-ttu-id="eee87-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="eee87-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="eee87-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="eee87-1815">tipo della scheda</span></span> 
- <span data-ttu-id="eee87-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="eee87-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="eee87-1817">scheda</span><span class="sxs-lookup"><span data-stu-id="eee87-1817">scheda</span></span> 
- <span data-ttu-id="eee87-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="eee87-1818">v pay</span></span> 
- <span data-ttu-id="eee87-1819">v-지급</span><span class="sxs-lookup"><span data-stu-id="eee87-1819">v-pay</span></span> 
- <span data-ttu-id="eee87-1820">visa</span><span class="sxs-lookup"><span data-stu-id="eee87-1820">visa</span></span> 
- <span data-ttu-id="eee87-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="eee87-1821">visa plus</span></span> 
- <span data-ttu-id="eee87-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="eee87-1822">visa electron</span></span> 
- <span data-ttu-id="eee87-1823">visto</span><span class="sxs-lookup"><span data-stu-id="eee87-1823">visto</span></span> 
- <span data-ttu-id="eee87-1824">visum</span><span class="sxs-lookup"><span data-stu-id="eee87-1824">visum</span></span> 
- <span data-ttu-id="eee87-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="eee87-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="eee87-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="eee87-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="eee87-1827">card identification number</span><span class="sxs-lookup"><span data-stu-id="eee87-1827">card identification number</span></span>
- <span data-ttu-id="eee87-1828">card verification</span><span class="sxs-lookup"><span data-stu-id="eee87-1828">card verification</span></span> 
- <span data-ttu-id="eee87-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="eee87-1829">cardi la verifica</span></span> 
- <span data-ttu-id="eee87-1830">cid</span><span class="sxs-lookup"><span data-stu-id="eee87-1830">cid</span></span> 
- <span data-ttu-id="eee87-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="eee87-1831">cod seg</span></span> 
- <span data-ttu-id="eee87-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1832">cod seguranca</span></span> 
- <span data-ttu-id="eee87-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1833">cod segurança</span></span> 
- <span data-ttu-id="eee87-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="eee87-1834">cod sicurezza</span></span> 
- <span data-ttu-id="eee87-1835">cod.</span><span class="sxs-lookup"><span data-stu-id="eee87-1835">cod.</span></span> <span data-ttu-id="eee87-1836">seg</span><span class="sxs-lookup"><span data-stu-id="eee87-1836">seg</span></span> 
- <span data-ttu-id="eee87-1837">cod.</span><span class="sxs-lookup"><span data-stu-id="eee87-1837">cod.</span></span> <span data-ttu-id="eee87-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1838">seguranca</span></span> 
- <span data-ttu-id="eee87-1839">cod.</span><span class="sxs-lookup"><span data-stu-id="eee87-1839">cod.</span></span> <span data-ttu-id="eee87-1840">segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1840">segurança</span></span> 
- <span data-ttu-id="eee87-1841">cod.</span><span class="sxs-lookup"><span data-stu-id="eee87-1841">cod.</span></span> <span data-ttu-id="eee87-1842">sicurezza</span><span class="sxs-lookup"><span data-stu-id="eee87-1842">sicurezza</span></span> 
- <span data-ttu-id="eee87-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="eee87-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="eee87-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="eee87-1844">codice di verifica</span></span> 
- <span data-ttu-id="eee87-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="eee87-1845">codigo</span></span> 
- <span data-ttu-id="eee87-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="eee87-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1847">codigo de segurança</span></span> 
- <span data-ttu-id="eee87-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="eee87-1848">crittogramma</span></span> 
- <span data-ttu-id="eee87-1849">cryptogram</span><span class="sxs-lookup"><span data-stu-id="eee87-1849">cryptogram</span></span> 
- <span data-ttu-id="eee87-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="eee87-1850">cryptogramme</span></span> 
- <span data-ttu-id="eee87-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="eee87-1851">cv2</span></span> 
- <span data-ttu-id="eee87-1852">cvc</span><span class="sxs-lookup"><span data-stu-id="eee87-1852">cvc</span></span> 
- <span data-ttu-id="eee87-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="eee87-1853">cvc2</span></span> 
- <span data-ttu-id="eee87-1854">cvn</span><span class="sxs-lookup"><span data-stu-id="eee87-1854">cvn</span></span> 
- <span data-ttu-id="eee87-1855">cvv</span><span class="sxs-lookup"><span data-stu-id="eee87-1855">cvv</span></span> 
- <span data-ttu-id="eee87-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="eee87-1856">cvv2</span></span> 
- <span data-ttu-id="eee87-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1857">cód seguranca</span></span> 
- <span data-ttu-id="eee87-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1858">cód segurança</span></span> 
- <span data-ttu-id="eee87-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="eee87-1859">cód.</span></span> <span data-ttu-id="eee87-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1860">seguranca</span></span> 
- <span data-ttu-id="eee87-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="eee87-1861">cód.</span></span> <span data-ttu-id="eee87-1862">segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1862">segurança</span></span> 
- <span data-ttu-id="eee87-1863">código</span><span class="sxs-lookup"><span data-stu-id="eee87-1863">código</span></span> 
- <span data-ttu-id="eee87-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="eee87-1864">código de seguranca</span></span> 
- <span data-ttu-id="eee87-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="eee87-1865">código de segurança</span></span> 
- <span data-ttu-id="eee87-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="eee87-1866">de kaart controle</span></span> 
- <span data-ttu-id="eee87-1867">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="eee87-1867">geeft nr uit</span></span> 
- <span data-ttu-id="eee87-1868">issue no</span><span class="sxs-lookup"><span data-stu-id="eee87-1868">issue no</span></span> 
- <span data-ttu-id="eee87-1869">issue number</span><span class="sxs-lookup"><span data-stu-id="eee87-1869">issue number</span></span> 
- <span data-ttu-id="eee87-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="eee87-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="eee87-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="eee87-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="eee87-1873">kwestieaantal</span></span> 
- <span data-ttu-id="eee87-1874">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1874">no.</span></span> <span data-ttu-id="eee87-1875">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="eee87-1875">dell'edizione</span></span> 
- <span data-ttu-id="eee87-1876">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1876">no.</span></span> <span data-ttu-id="eee87-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="eee87-1877">di sicurezza</span></span> 
- <span data-ttu-id="eee87-1878">numero de securite</span><span class="sxs-lookup"><span data-stu-id="eee87-1878">numero de securite</span></span> 
- <span data-ttu-id="eee87-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="eee87-1879">numero de verificacao</span></span> 
- <span data-ttu-id="eee87-1880">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="eee87-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="eee87-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="eee87-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="eee87-1882">scheda</span><span class="sxs-lookup"><span data-stu-id="eee87-1882">scheda</span></span> 
- <span data-ttu-id="eee87-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="eee87-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="eee87-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="eee87-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="eee87-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="eee87-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="eee87-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="eee87-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="eee87-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="eee87-1887">número de verificação</span></span> 
- <span data-ttu-id="eee87-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="eee87-1888">perno il blocco</span></span> 
- <span data-ttu-id="eee87-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="eee87-1889">pin block</span></span> 
- <span data-ttu-id="eee87-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="eee87-1890">prufziffer</span></span> 
- <span data-ttu-id="eee87-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="eee87-1891">prüfziffer</span></span> 
- <span data-ttu-id="eee87-1892">security code</span><span class="sxs-lookup"><span data-stu-id="eee87-1892">security code</span></span> 
- <span data-ttu-id="eee87-1893">security no</span><span class="sxs-lookup"><span data-stu-id="eee87-1893">security no</span></span> 
- <span data-ttu-id="eee87-1894">security number</span><span class="sxs-lookup"><span data-stu-id="eee87-1894">security number</span></span> 
- <span data-ttu-id="eee87-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="eee87-1895">sicherheits kode</span></span> 
- <span data-ttu-id="eee87-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="eee87-1896">sicherheitscode</span></span> 
- <span data-ttu-id="eee87-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="eee87-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="eee87-1898">speldblok</span></span> 
- <span data-ttu-id="eee87-1899">veiligheid 번호:</span><span class="sxs-lookup"><span data-stu-id="eee87-1899">veiligheid nr</span></span> 
- <span data-ttu-id="eee87-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="eee87-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="eee87-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="eee87-1901">veiligheidscode</span></span> 
- <span data-ttu-id="eee87-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="eee87-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="eee87-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="eee87-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="eee87-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="eee87-1905">ablauf</span><span class="sxs-lookup"><span data-stu-id="eee87-1905">ablauf</span></span> 
- <span data-ttu-id="eee87-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="eee87-1906">data de expiracao</span></span> 
- <span data-ttu-id="eee87-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="eee87-1907">data de expiração</span></span> 
- <span data-ttu-id="eee87-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="eee87-1908">data del exp</span></span> 
- <span data-ttu-id="eee87-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="eee87-1909">data di exp</span></span> 
- <span data-ttu-id="eee87-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="eee87-1910">data di scadenza</span></span> 
- <span data-ttu-id="eee87-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="eee87-1911">data em que expira</span></span> 
- <span data-ttu-id="eee87-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="eee87-1912">data scad</span></span> 
- <span data-ttu-id="eee87-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="eee87-1913">data scadenza</span></span> 
- <span data-ttu-id="eee87-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="eee87-1914">date de validité</span></span> 
- <span data-ttu-id="eee87-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="eee87-1915">datum afloop</span></span> 
- <span data-ttu-id="eee87-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="eee87-1916">datum van exp</span></span> 
- <span data-ttu-id="eee87-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="eee87-1917">de afloop</span></span> 
- <span data-ttu-id="eee87-1918">espira</span><span class="sxs-lookup"><span data-stu-id="eee87-1918">espira</span></span> 
- <span data-ttu-id="eee87-1919">espira</span><span class="sxs-lookup"><span data-stu-id="eee87-1919">espira</span></span> 
- <span data-ttu-id="eee87-1920">exp date</span><span class="sxs-lookup"><span data-stu-id="eee87-1920">exp date</span></span> 
- <span data-ttu-id="eee87-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="eee87-1921">exp datum</span></span> 
- <span data-ttu-id="eee87-1922">행사</span><span class="sxs-lookup"><span data-stu-id="eee87-1922">expiration</span></span> 
- <span data-ttu-id="eee87-1923">예정</span><span class="sxs-lookup"><span data-stu-id="eee87-1923">expire</span></span> 
- <span data-ttu-id="eee87-1924">expires</span><span class="sxs-lookup"><span data-stu-id="eee87-1924">expires</span></span> 
- <span data-ttu-id="eee87-1925">만료</span><span class="sxs-lookup"><span data-stu-id="eee87-1925">expiry</span></span> 
- <span data-ttu-id="eee87-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="eee87-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="eee87-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="eee87-1927">fecha de venc</span></span> 
- <span data-ttu-id="eee87-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="eee87-1928">gultig bis</span></span> 
- <span data-ttu-id="eee87-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="eee87-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="eee87-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="eee87-1930">gültig bis</span></span> 
- <span data-ttu-id="eee87-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="eee87-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="eee87-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="eee87-1932">la scadenza</span></span> 
- <span data-ttu-id="eee87-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="eee87-1933">scadenza</span></span> 
- <span data-ttu-id="eee87-1934">valable</span><span class="sxs-lookup"><span data-stu-id="eee87-1934">valable</span></span> 
- <span data-ttu-id="eee87-1935">유효한 ade</span><span class="sxs-lookup"><span data-stu-id="eee87-1935">validade</span></span> 
- <span data-ttu-id="eee87-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="eee87-1936">valido hasta</span></span> 
- <span data-ttu-id="eee87-1937">valor</span><span class="sxs-lookup"><span data-stu-id="eee87-1937">valor</span></span> 
- <span data-ttu-id="eee87-1938">venc</span><span class="sxs-lookup"><span data-stu-id="eee87-1938">venc</span></span> 
- <span data-ttu-id="eee87-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="eee87-1939">vencimento</span></span> 
- <span data-ttu-id="eee87-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="eee87-1940">vencimiento</span></span> 
- <span data-ttu-id="eee87-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="eee87-1941">verloopt</span></span> 
- <span data-ttu-id="eee87-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="eee87-1942">vervaldag</span></span> 
- <span data-ttu-id="eee87-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="eee87-1943">vervaldatum</span></span> 
- <span data-ttu-id="eee87-1944">vto</span><span class="sxs-lookup"><span data-stu-id="eee87-1944">vto</span></span> 
- <span data-ttu-id="eee87-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="eee87-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="eee87-1946">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1946">EU Driver's License Number</span></span>

<span data-ttu-id="eee87-1947">자세한 내용은 [EU 운전 면허 번호 중요 정보 유형을](eu-driver-s-license-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="eee87-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="eee87-1948">EU 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1948">EU National Identification Number</span></span>

<span data-ttu-id="eee87-1949">자세한 내용은 [EU 국가 식별 번호 중요 한 정보 유형을](eu-national-identification-number.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eee87-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="eee87-1950">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1950">EU Passport Number</span></span>

<span data-ttu-id="eee87-1951">자세한 내용은 [EU Passport 번호 중요 한 정보 유형을](eu-passport-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="eee87-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="eee87-1952">EU 주민 등록 번호 또는 동등한 ID</span><span class="sxs-lookup"><span data-stu-id="eee87-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="eee87-1953">자세한 내용은 [EU 주민 등록 번호 또는 동등한 ID 중요 정보 유형을](eu-social-security-number-or-equivalent-id.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="eee87-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="eee87-1954">EU 세금 확인 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="eee87-1955">자세한 내용은 [EU 세금 식별 번호 중요 한 정보 유형을](eu-tax-identification-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="eee87-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="eee87-1956">핀란드 국가 ID</span><span class="sxs-lookup"><span data-stu-id="eee87-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1957">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1957">Format</span></span>

<span data-ttu-id="eee87-1958">세기를 나타내는 6자리 숫자와 문자, 3자리 숫자와 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1959">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1959">Pattern</span></span>

<span data-ttu-id="eee87-1960">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="eee87-1961">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="eee87-1962">세기 표시('-', '+' 또는 'a')</span><span class="sxs-lookup"><span data-stu-id="eee87-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="eee87-1963">3자리 개인 ID 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="eee87-1964">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1965">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1965">Checksum</span></span>

<span data-ttu-id="eee87-1966">예</span><span class="sxs-lookup"><span data-stu-id="eee87-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1967">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1967">Definition</span></span>

<span data-ttu-id="eee87-1968">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1969">Func_finnish_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1970">Keyword_finnish_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="eee87-1971">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1971">The checksum passes.</span></span>

```xml
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-1972">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1972">Keywords</span></span>

- <span data-ttu-id="eee87-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="eee87-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="eee87-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="eee87-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="eee87-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="eee87-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="eee87-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="eee87-1976">Personbeteckning</span></span>
- <span data-ttu-id="eee87-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="eee87-1978">핀란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1978">Finland Passport Number</span></span>

<span data-ttu-id="eee87-1979">9 개의 문자 및 숫자 패턴 조합 형식 조합: 두 문자 (대/소문자 구분 안 함) 7 자리 체크섬 정의 없음 DLP 75 정책은이 유형의 중요 한 정보를 검색 한 것으로,이에 따라 300 문자의 근사: 정규식 Regex_finland_passport_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="eee87-1980">Keyword_finland_passport_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="eee87-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="eee87-1981"></span></span>
<span data-ttu-id="eee87-1982">Passport Keyword_finland_passport_number 키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="eee87-1983">프랑스 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-1984">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-1984">Format</span></span>

<span data-ttu-id="eee87-1985">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-1986">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-1986">Pattern</span></span>

<span data-ttu-id="eee87-1987">비슷한 패턴(예: 프랑스 전화 번호)을 무시하기 위한 유효성 검사 기능을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-1988">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-1988">Checksum</span></span>

<span data-ttu-id="eee87-1989">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-1990">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-1990">Definition</span></span>

<span data-ttu-id="eee87-1991">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-1992">Func_french_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-1993">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="eee87-1994">Keyword_french_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="eee87-1995">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-1995">The function Func_eu_date finds a date in the right date format.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-1996">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="eee87-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="eee87-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="eee87-1998">drivers licence</span><span class="sxs-lookup"><span data-stu-id="eee87-1998">drivers licence</span></span>
- <span data-ttu-id="eee87-1999">drivers license</span><span class="sxs-lookup"><span data-stu-id="eee87-1999">drivers license</span></span>
- <span data-ttu-id="eee87-2000">driving licence</span><span class="sxs-lookup"><span data-stu-id="eee87-2000">driving licence</span></span>
- <span data-ttu-id="eee87-2001">driving license</span><span class="sxs-lookup"><span data-stu-id="eee87-2001">driving license</span></span>
- <span data-ttu-id="eee87-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="eee87-2002">permis de conduire</span></span>
- <span data-ttu-id="eee87-2003">licence number</span><span class="sxs-lookup"><span data-stu-id="eee87-2003">licence number</span></span>
- <span data-ttu-id="eee87-2004">license number</span><span class="sxs-lookup"><span data-stu-id="eee87-2004">license number</span></span>
- <span data-ttu-id="eee87-2005">licence numbers</span><span class="sxs-lookup"><span data-stu-id="eee87-2005">licence numbers</span></span>
- <span data-ttu-id="eee87-2006">license numbers</span><span class="sxs-lookup"><span data-stu-id="eee87-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="eee87-2007">프랑스 국가 ID 카드(CNI)</span><span class="sxs-lookup"><span data-stu-id="eee87-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2008">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2008">Format</span></span>

<span data-ttu-id="eee87-2009">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2010">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2010">Pattern</span></span>

<span data-ttu-id="eee87-2011">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2012">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2012">Checksum</span></span>

<span data-ttu-id="eee87-2013">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2014">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2014">Definition</span></span>

<span data-ttu-id="eee87-2015">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2016">Regex_france_cni 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```xml
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2017">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2017">Keywords</span></span>

<span data-ttu-id="eee87-2018">없음</span><span class="sxs-lookup"><span data-stu-id="eee87-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="eee87-2019">프랑스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2020">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2020">Format</span></span>

<span data-ttu-id="eee87-2021">9자리 숫자 및 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2022">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2022">Pattern</span></span>

<span data-ttu-id="eee87-2023">9자리 숫자 및 문자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="eee87-2024">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2024">Two digits</span></span> 
- <span data-ttu-id="eee87-2025">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-2026">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2027">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2027">Checksum</span></span>

<span data-ttu-id="eee87-2028">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2029">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2029">Definition</span></span>

<span data-ttu-id="eee87-2030">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2031">Func_fr_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2032">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2032">A keyword from Keyword_passport is found.</span></span>

```xml
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2033">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="eee87-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-2034">Keyword_passport</span></span>

- <span data-ttu-id="eee87-2035">Passport Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2035">Passport Number</span></span>
- <span data-ttu-id="eee87-2036">Passport No</span><span class="sxs-lookup"><span data-stu-id="eee87-2036">Passport No</span></span>
- <span data-ttu-id="eee87-2037">Passport #</span><span class="sxs-lookup"><span data-stu-id="eee87-2037">Passport #</span></span>
- <span data-ttu-id="eee87-2038">여권 #</span><span class="sxs-lookup"><span data-stu-id="eee87-2038">Passport#</span></span>
- <span data-ttu-id="eee87-2039">PassportID</span><span class="sxs-lookup"><span data-stu-id="eee87-2039">PassportID</span></span>
- <span data-ttu-id="eee87-2040">Passportno</span><span class="sxs-lookup"><span data-stu-id="eee87-2040">Passportno</span></span>
- <span data-ttu-id="eee87-2041">passportnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-2041">passportnumber</span></span>
- <span data-ttu-id="eee87-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="eee87-2042">パスポート</span></span>
- <span data-ttu-id="eee87-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2043">パスポート番号</span></span>
- <span data-ttu-id="eee87-2044">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="eee87-2044">パスポートのNum</span></span>
- <span data-ttu-id="eee87-2045">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2045">パスポート ＃</span></span> 
- <span data-ttu-id="eee87-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="eee87-2046">Numéro de passeport</span></span>
- <span data-ttu-id="eee87-2047">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="eee87-2047">Passeport n °</span></span>
- <span data-ttu-id="eee87-2048">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="eee87-2048">Passeport Non</span></span>
- <span data-ttu-id="eee87-2049">Passeport #</span><span class="sxs-lookup"><span data-stu-id="eee87-2049">Passeport #</span></span>
- <span data-ttu-id="eee87-2050">포트 #</span><span class="sxs-lookup"><span data-stu-id="eee87-2050">Passeport#</span></span>
- <span data-ttu-id="eee87-2051">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="eee87-2051">PasseportNon</span></span>
- <span data-ttu-id="eee87-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="eee87-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="eee87-2053">프랑스 사회 보장 번호(INSEE)</span><span class="sxs-lookup"><span data-stu-id="eee87-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2054">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2054">Format</span></span>

<span data-ttu-id="eee87-2055">15자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2056">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2056">Pattern</span></span>

<span data-ttu-id="eee87-2057">다음 두 패턴 중 하나가 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="eee87-2058">13 자리 숫자와 공백 다음 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="eee87-2059">또는</span><span class="sxs-lookup"><span data-stu-id="eee87-2059">or</span></span>
- <span data-ttu-id="eee87-2060">15자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2061">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2061">Checksum</span></span>

<span data-ttu-id="eee87-2062">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2063">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2063">Definition</span></span>

<span data-ttu-id="eee87-2064">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2065">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2066">Keyword_fr_insee의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="eee87-2067">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2067">The checksum passes.</span></span>

<span data-ttu-id="eee87-2068">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2069">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2070">Keyword_fr_insee의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="eee87-2071">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2071">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2072">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="eee87-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="eee87-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="eee87-2074">insee</span><span class="sxs-lookup"><span data-stu-id="eee87-2074">insee</span></span>
- <span data-ttu-id="eee87-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="eee87-2075">securité sociale</span></span>
- <span data-ttu-id="eee87-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="eee87-2076">securite sociale</span></span>
- <span data-ttu-id="eee87-2077">national id</span><span class="sxs-lookup"><span data-stu-id="eee87-2077">national id</span></span>
- <span data-ttu-id="eee87-2078">national identification</span><span class="sxs-lookup"><span data-stu-id="eee87-2078">national identification</span></span>
- <span data-ttu-id="eee87-2079">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="eee87-2079">numéro d'identité</span></span>
- <span data-ttu-id="eee87-2080">no d'identité</span><span class="sxs-lookup"><span data-stu-id="eee87-2080">no d'identité</span></span>
- <span data-ttu-id="eee87-2081">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-2081">no.</span></span> <span data-ttu-id="eee87-2082">d'identité</span><span class="sxs-lookup"><span data-stu-id="eee87-2082">d'identité</span></span>
- <span data-ttu-id="eee87-2083">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="eee87-2083">numero d'identite</span></span>
- <span data-ttu-id="eee87-2084">no d'identite</span><span class="sxs-lookup"><span data-stu-id="eee87-2084">no d'identite</span></span>
- <span data-ttu-id="eee87-2085">아니요.</span><span class="sxs-lookup"><span data-stu-id="eee87-2085">no.</span></span> <span data-ttu-id="eee87-2086">d'identite</span><span class="sxs-lookup"><span data-stu-id="eee87-2086">d'identite</span></span>
- <span data-ttu-id="eee87-2087">social security number</span><span class="sxs-lookup"><span data-stu-id="eee87-2087">social security number</span></span>
- <span data-ttu-id="eee87-2088">social security code</span><span class="sxs-lookup"><span data-stu-id="eee87-2088">social security code</span></span>
- <span data-ttu-id="eee87-2089">social insurance number</span><span class="sxs-lookup"><span data-stu-id="eee87-2089">social insurance number</span></span>
- <span data-ttu-id="eee87-2090">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="eee87-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="eee87-2091">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="eee87-2091">d'identité nationale</span></span>
- <span data-ttu-id="eee87-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="eee87-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="eee87-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="eee87-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="eee87-2094">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="eee87-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="eee87-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="eee87-2095">numéro de sécu</span></span>
- <span data-ttu-id="eee87-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="eee87-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="eee87-2097">독일 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2098">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2098">Format</span></span>

<span data-ttu-id="eee87-2099">11자리 숫자와 문자 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2100">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2100">Pattern</span></span>

<span data-ttu-id="eee87-2101">11자리 숫자와 문자(대/소문자 구분 안 함):</span><span class="sxs-lookup"><span data-stu-id="eee87-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="eee87-2102">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-2102">A digit or letter</span></span> 
- <span data-ttu-id="eee87-2103">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2103">Two digits</span></span> 
- <span data-ttu-id="eee87-2104">6자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-2104">Six digits or letters</span></span> 
- <span data-ttu-id="eee87-2105">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2105">A digit</span></span> 
- <span data-ttu-id="eee87-2106">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2107">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2107">Checksum</span></span>

<span data-ttu-id="eee87-2108">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2109">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2109">Definition</span></span>

<span data-ttu-id="eee87-2110">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2111">Func_german_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2112">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="eee87-2113">Keyword_german_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="eee87-2114">Keyword_german_drivers_license_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="eee87-2115">Keyword_german_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="eee87-2116">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2116">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2117">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="eee87-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="eee87-2119">Führerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2119">Führerschein</span></span>
- <span data-ttu-id="eee87-2120">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2120">Fuhrerschein</span></span>
- <span data-ttu-id="eee87-2121">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2121">Fuehrerschein</span></span>
- <span data-ttu-id="eee87-2122">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="eee87-2123">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="eee87-2124">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="eee87-2125">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="eee87-2125">Führerschein-</span></span> 
- <span data-ttu-id="eee87-2126">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="eee87-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="eee87-2127">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="eee87-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="eee87-2128">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="eee87-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="eee87-2129">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="eee87-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="eee87-2130">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="eee87-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="eee87-2131">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="eee87-2132">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="eee87-2133">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="eee87-2134">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="eee87-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="eee87-2135">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="eee87-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="eee87-2136">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="eee87-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="eee87-2137">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="eee87-2138">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="eee87-2139">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="eee87-2140">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="eee87-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="eee87-2141">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="eee87-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="eee87-2142">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="eee87-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="eee87-2143">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="eee87-2144">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="eee87-2145">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="eee87-2146">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="eee87-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="eee87-2147">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="eee87-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="eee87-2148">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="eee87-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="eee87-2149">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="eee87-2150">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="eee87-2151">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="eee87-2152">DL</span><span class="sxs-lookup"><span data-stu-id="eee87-2152">DL</span></span> 
- <span data-ttu-id="eee87-2153">된다</span><span class="sxs-lookup"><span data-stu-id="eee87-2153">DLS</span></span>
- <span data-ttu-id="eee87-2154">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-2154">Driv Lic</span></span> 
- <span data-ttu-id="eee87-2155">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="eee87-2155">Driv Licen</span></span> 
- <span data-ttu-id="eee87-2156">Driv License</span><span class="sxs-lookup"><span data-stu-id="eee87-2156">Driv License</span></span>
- <span data-ttu-id="eee87-2157">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-2157">Driv Licenses</span></span> 
- <span data-ttu-id="eee87-2158">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-2158">Driv Licence</span></span> 
- <span data-ttu-id="eee87-2159">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-2159">Driv Licences</span></span> 
- <span data-ttu-id="eee87-2160">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-2160">Driv Lic</span></span> 
- <span data-ttu-id="eee87-2161">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="eee87-2161">Driver Licen</span></span> 
- <span data-ttu-id="eee87-2162">Driver License</span><span class="sxs-lookup"><span data-stu-id="eee87-2162">Driver License</span></span> 
- <span data-ttu-id="eee87-2163">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-2163">Driver Licenses</span></span> 
- <span data-ttu-id="eee87-2164">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-2164">Driver Licence</span></span> 
- <span data-ttu-id="eee87-2165">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-2165">Driver Licences</span></span> 
- <span data-ttu-id="eee87-2166">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-2166">Drivers Lic</span></span> 
- <span data-ttu-id="eee87-2167">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="eee87-2167">Drivers Licen</span></span> 
- <span data-ttu-id="eee87-2168">Drivers License</span><span class="sxs-lookup"><span data-stu-id="eee87-2168">Drivers License</span></span> 
- <span data-ttu-id="eee87-2169">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="eee87-2170">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-2170">Drivers Licence</span></span> 
- <span data-ttu-id="eee87-2171">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-2171">Drivers Licences</span></span> 
- <span data-ttu-id="eee87-2172">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-2172">Driver's Lic</span></span> 
- <span data-ttu-id="eee87-2173">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="eee87-2173">Driver's Licen</span></span> 
- <span data-ttu-id="eee87-2174">Driver's License</span><span class="sxs-lookup"><span data-stu-id="eee87-2174">Driver's License</span></span> 
- <span data-ttu-id="eee87-2175">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="eee87-2176">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-2176">Driver's Licence</span></span> 
- <span data-ttu-id="eee87-2177">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-2177">Driver's Licences</span></span> 
- <span data-ttu-id="eee87-2178">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-2178">Driving Lic</span></span> 
- <span data-ttu-id="eee87-2179">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="eee87-2179">Driving Licen</span></span> 
- <span data-ttu-id="eee87-2180">Driving License</span><span class="sxs-lookup"><span data-stu-id="eee87-2180">Driving License</span></span> 
- <span data-ttu-id="eee87-2181">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-2181">Driving Licenses</span></span> 
- <span data-ttu-id="eee87-2182">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="eee87-2182">Driving Licence</span></span> 
- <span data-ttu-id="eee87-2183">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="eee87-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="eee87-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="eee87-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="eee87-2185">Veiligheid-Führerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="eee87-2186">Veiligheid-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="eee87-2187">Veiligheid-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="eee87-2188">Führerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2188">No-Führerschein</span></span> 
- <span data-ttu-id="eee87-2189">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="eee87-2190">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="eee87-2191">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2191">N-Führerschein</span></span> 
- <span data-ttu-id="eee87-2192">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="eee87-2193">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="eee87-2194">Veiligheid-Führerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="eee87-2195">Veiligheid-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="eee87-2196">Veiligheid-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="eee87-2197">Führerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2197">No-Führerschein</span></span> 
- <span data-ttu-id="eee87-2198">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="eee87-2199">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="eee87-2200">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2200">N-Führerschein</span></span> 
- <span data-ttu-id="eee87-2201">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="eee87-2202">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="eee87-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="eee87-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="eee87-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="eee87-2204">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="eee87-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="eee87-2205">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="eee87-2205">ausstellungsort</span></span>
- <span data-ttu-id="eee87-2206">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="eee87-2206">ausstellende behöde</span></span>
- <span data-ttu-id="eee87-2207">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="eee87-2207">ausstellende behorde</span></span>
- <span data-ttu-id="eee87-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="eee87-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="eee87-2209">독일 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2210">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2210">Format</span></span>

<span data-ttu-id="eee87-2211">10자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2212">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2212">Pattern</span></span>

<span data-ttu-id="eee87-2213">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="eee87-2214">첫 번째 문자는 숫자 또는 (C, F, G, H, J, K) 집합의 문자임</span><span class="sxs-lookup"><span data-stu-id="eee87-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="eee87-2215">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2215">Three digits</span></span> 
- <span data-ttu-id="eee87-2216">5자리 숫자 또는 (C, -H, J-N, P, R, T, V-Z) 집합의 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="eee87-2217">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2218">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2218">Checksum</span></span>

<span data-ttu-id="eee87-2219">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2220">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2220">Definition</span></span>

<span data-ttu-id="eee87-2221">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2222">Func_german_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2223">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="eee87-2224">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2224">The checksum passes.</span></span>

<span data-ttu-id="eee87-2225">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2226">Func_german_passport_data 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2227">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="eee87-2228">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2228">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2229">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="eee87-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="eee87-2231">reisepass</span><span class="sxs-lookup"><span data-stu-id="eee87-2231">reisepass</span></span>
- <span data-ttu-id="eee87-2232">reisepasse</span><span class="sxs-lookup"><span data-stu-id="eee87-2232">reisepasse</span></span>
- <span data-ttu-id="eee87-2233">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2233">reisepassnummer</span></span>
- <span data-ttu-id="eee87-2234">여권</span><span class="sxs-lookup"><span data-stu-id="eee87-2234">passport</span></span>
- <span data-ttu-id="eee87-2235">passports</span><span class="sxs-lookup"><span data-stu-id="eee87-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="eee87-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="eee87-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="eee87-2237">ge삼 부, tsdatum</span><span class="sxs-lookup"><span data-stu-id="eee87-2237">geburtsdatum</span></span>
- <span data-ttu-id="eee87-2238">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="eee87-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="eee87-2239">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="eee87-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="eee87-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="eee87-2241">Reisepass Veiligheid-Reisepass</span><span class="sxs-lookup"><span data-stu-id="eee87-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="eee87-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="eee87-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="eee87-2243">Reisepass-Veiligheid</span><span class="sxs-lookup"><span data-stu-id="eee87-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="eee87-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="eee87-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="eee87-2245">bnationalit</span><span class="sxs-lookup"><span data-stu-id="eee87-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="eee87-2246">독일 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2247">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2247">Format</span></span>

<span data-ttu-id="eee87-2248">2010 년 11 월 1 일 이후: 9 개 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="eee87-2249">1 월 1987 년 10 월 31 일 (2010:10 자리 숫자)</span><span class="sxs-lookup"><span data-stu-id="eee87-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2250">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2250">Pattern</span></span>

<span data-ttu-id="eee87-2251">2010년 11월 1일 이후:</span><span class="sxs-lookup"><span data-stu-id="eee87-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="eee87-2252">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-2253">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2253">Eight digits</span></span>

<span data-ttu-id="eee87-2254">1 년 4 월 1987 일 ~ 10 2010 월 31 일까 지:</span><span class="sxs-lookup"><span data-stu-id="eee87-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="eee87-2255">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2256">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2256">Checksum</span></span>

<span data-ttu-id="eee87-2257">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2258">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2258">Definition</span></span>

<span data-ttu-id="eee87-2259">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2260">정규식 Regex_germany_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2261">Keyword_germany_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```xml
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2262">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="eee87-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="eee87-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="eee87-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="eee87-2264">Identity Card</span></span>
- <span data-ttu-id="eee87-2265">ID</span><span class="sxs-lookup"><span data-stu-id="eee87-2265">ID</span></span>
- <span data-ttu-id="eee87-2266">확인과</span><span class="sxs-lookup"><span data-stu-id="eee87-2266">Identification</span></span>
- <span data-ttu-id="eee87-2267">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="eee87-2267">Personalausweis</span></span>
- <span data-ttu-id="eee87-2268">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="eee87-2269">Ausweis</span><span class="sxs-lookup"><span data-stu-id="eee87-2269">Ausweis</span></span>
- <span data-ttu-id="eee87-2270">Identifikation</span><span class="sxs-lookup"><span data-stu-id="eee87-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="eee87-2271">그리스 국가 ID 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2272">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2272">Format</span></span>

<span data-ttu-id="eee87-2273">7-8자리 문자 및 숫자와 대시의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2274">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2274">Pattern</span></span>

<span data-ttu-id="eee87-2275">7자리 문자 및 숫자(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="eee87-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="eee87-2276">1개 문자(그리스어 알파벳의 임의 문자) </span><span class="sxs-lookup"><span data-stu-id="eee87-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="eee87-2277">대시 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-2277">A dash</span></span> 
- <span data-ttu-id="eee87-2278">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2278">Six digits</span></span>

<span data-ttu-id="eee87-2279">8자리 문자와 숫자(새로운 형식):</span><span class="sxs-lookup"><span data-stu-id="eee87-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="eee87-2280">그리스어 및 라틴어 알파벳 둘 다에 해당 대문자가 포함된 2개 문자(ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="eee87-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="eee87-2281">대시 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-2281">A dash</span></span> 
- <span data-ttu-id="eee87-2282">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2283">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2283">Checksum</span></span>

<span data-ttu-id="eee87-2284">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2285">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2285">Definition</span></span>

<span data-ttu-id="eee87-2286">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2287">정규식 Regex_greece_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2288">Keyword_greece_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```xml
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2289">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="eee87-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="eee87-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="eee87-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="eee87-2291">Greek identity Card</span></span>
- <span data-ttu-id="eee87-2292">Tautotita</span><span class="sxs-lookup"><span data-stu-id="eee87-2292">Tautotita</span></span>
- <span data-ttu-id="eee87-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="eee87-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="eee87-2294">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="eee87-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="eee87-2295">HKID(홍콩 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2296">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2296">Format</span></span>

<span data-ttu-id="eee87-2297">8-9자리 문자 및 숫자와 마지막 문자를 선택적 괄호로 묶어서 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2298">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2298">Pattern</span></span>

<span data-ttu-id="eee87-2299">8-9자리 문자 조합:</span><span class="sxs-lookup"><span data-stu-id="eee87-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="eee87-2300">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-2301">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2301">Six digits</span></span> 
- <span data-ttu-id="eee87-2302">검사 숫자에 해당하고 선택적으로 괄호로 묶는 마지막 문자(임의 숫자 또는 문자 A)</span><span class="sxs-lookup"><span data-stu-id="eee87-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2303">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2303">Checksum</span></span>

<span data-ttu-id="eee87-2304">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2305">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2305">Definition</span></span>

<span data-ttu-id="eee87-2306">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2307">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2308">Keyword_hong_kong_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="eee87-2309">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2309">The checksum passes.</span></span>

<span data-ttu-id="eee87-2310">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2311">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2312">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2312">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2313">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="eee87-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="eee87-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="eee87-2315">홍콩 특별 식별자 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2315">hong kong identity card</span></span>
- <span data-ttu-id="eee87-2316">HKIDC</span><span class="sxs-lookup"><span data-stu-id="eee87-2316">HKIDC</span></span>
- <span data-ttu-id="eee87-2317">id card</span><span class="sxs-lookup"><span data-stu-id="eee87-2317">id card</span></span>
- <span data-ttu-id="eee87-2318">identity card</span><span class="sxs-lookup"><span data-stu-id="eee87-2318">identity card</span></span>
- <span data-ttu-id="eee87-2319">zh-hk id 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2319">hk identity card</span></span>
- <span data-ttu-id="eee87-2320">홍콩 id</span><span class="sxs-lookup"><span data-stu-id="eee87-2320">hong kong id</span></span>
- <span data-ttu-id="eee87-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2321">香港身份證</span></span>
- <span data-ttu-id="eee87-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="eee87-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2323">身份證</span></span>
- <span data-ttu-id="eee87-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="eee87-2324">身份証</span></span>
- <span data-ttu-id="eee87-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-2325">身分證</span></span>
- <span data-ttu-id="eee87-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="eee87-2326">身分証</span></span>
- <span data-ttu-id="eee87-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="eee87-2327">香港身份証</span></span>
- <span data-ttu-id="eee87-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-2328">香港身分證</span></span>
- <span data-ttu-id="eee87-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="eee87-2329">香港身分証</span></span>
- <span data-ttu-id="eee87-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2330">香港身份證</span></span>
- <span data-ttu-id="eee87-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2331">香港居民身份證</span></span>
- <span data-ttu-id="eee87-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="eee87-2332">香港居民身份証</span></span>
- <span data-ttu-id="eee87-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-2333">香港居民身分證</span></span>
- <span data-ttu-id="eee87-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="eee87-2334">香港居民身分証</span></span>
- <span data-ttu-id="eee87-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="eee87-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="eee87-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="eee87-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="eee87-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="eee87-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="eee87-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="eee87-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="eee87-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="eee87-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="eee87-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="eee87-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="eee87-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="eee87-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="eee87-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="eee87-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="eee87-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="eee87-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="eee87-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="eee87-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="eee87-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="eee87-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="eee87-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="eee87-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="eee87-2351">인도 PAN(영구 계정 번호)</span><span class="sxs-lookup"><span data-stu-id="eee87-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2352">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2352">Format</span></span>

<span data-ttu-id="eee87-2353">10자리 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2354">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2354">Pattern</span></span>

<span data-ttu-id="eee87-2355">10자리 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2355">10 letters or digits:</span></span>
- <span data-ttu-id="eee87-2356">5개 문자(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="eee87-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-2357">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2357">Four digits</span></span> 
- <span data-ttu-id="eee87-2358">알파벳 검사 숫자에 해당하는 문자 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2359">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2359">Checksum</span></span>

<span data-ttu-id="eee87-2360">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2361">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2361">Definition</span></span>

<span data-ttu-id="eee87-2362">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2363">정규식 Regex_india_permanent_account_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2364">Keyword_india_permanent_account_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="eee87-2365">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2365">The checksum passes.</span></span>

```xml
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2366">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="eee87-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="eee87-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="eee87-2369">확대</span><span class="sxs-lookup"><span data-stu-id="eee87-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="eee87-2370">인도 고유 ID(Aadhaar) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2371">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2371">Format</span></span>

<span data-ttu-id="eee87-2372">선택적 공백 또는 대시를 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2373">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2373">Pattern</span></span>

<span data-ttu-id="eee87-2374">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2374">12 digits:</span></span>
- <span data-ttu-id="eee87-2375">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2375">Four digits</span></span> 
- <span data-ttu-id="eee87-2376">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="eee87-2376">An optional space or dash</span></span> 
- <span data-ttu-id="eee87-2377">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2377">Four digits</span></span> 
- <span data-ttu-id="eee87-2378">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="eee87-2378">An optional space or dash</span></span> 
- <span data-ttu-id="eee87-2379">검사 숫자에 해당하는 마지막 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2380">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2380">Checksum</span></span>

<span data-ttu-id="eee87-2381">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2382">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2382">Definition</span></span>

<span data-ttu-id="eee87-2383">DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="eee87-2384">Keyword_india_aadhar에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="eee87-2385">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2385">The checksum passes.</span></span>
<span data-ttu-id="eee87-2386">DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="eee87-2387">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2387">The checksum passes.</span></span>
```xml
<!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_india_aadhaar"/>
     <Match idRef="Keyword_india_aadhar"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_india_aadhaar"/>
  </Pattern>
</Entity>

### Keywords
   
#### Keyword_india_aadhar
- Aadhar
- Aadhaar
- UID
- आधार
   
## Indonesia Identity Card (KTP) Number

### Format

16 digits containing optional periods

### Pattern

16 digits:
- Two-digit province code 
- A period (optional) 
- Two-digit regency or city code 
- Two-digit subdistrict code 
- A period (optional) 
- Six digits in the format DDMMYY which are the date of birth 
- A period (optional) 
- Four digits

### Checksum

No

### Definition

A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The regular expression Regex_indonesia_id_card finds content that matches the pattern.
- A keyword from Keyword_indonesia_id_card is found.

A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The regular expression Regex_indonesia_id_card finds content that matches the pattern.

```
<!-- Indonesia Identity Card (KTP) Number -->
<span data-ttu-id="eee87-2388"><Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Regex_indonesia_id_card"/> <Match idRef="Keyword_indonesia_id_card"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_indonesia_id_card"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="eee87-2388"></span></span>
```

### Keywords
   
#### Keyword_indonesia_id_card

- KTP
- Kartu Tanda Penduduk 
- Nomor Induk Kependudukan 
   
## International Banking Account Number (IBAN)

### Format

Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)

### Pattern

Pattern must include all of the following:

- Two-letter country code
- Two check digits (followed by an optional space) 
- 1-7 groups of four letters or digits (can be separated by spaces)
- 1-3 letters or digits

The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:

ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg

### Checksum

Yes

### Definition

A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The function Func_iban finds content that matches the pattern.
- The checksum passes.

```xml
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2389">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2389">Keywords</span></span>

<span data-ttu-id="eee87-2390">없음</span><span class="sxs-lookup"><span data-stu-id="eee87-2390">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="eee87-2391">IP 주소</span><span class="sxs-lookup"><span data-stu-id="eee87-2391">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2392">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2392">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="eee87-2393">IPv4</span><span class="sxs-lookup"><span data-stu-id="eee87-2393">IPv4:</span></span>
<span data-ttu-id="eee87-2394">IPv4 주소의 서식 있는 버전(마침표 있음) 및 서식 없는 버전(마침표 없음)으로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2394">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="eee87-2395">IPv6</span><span class="sxs-lookup"><span data-stu-id="eee87-2395">IPv6:</span></span>
<span data-ttu-id="eee87-2396">서식 있는(콜론 포함) IPv6 번호로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2396">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2397">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2397">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2398">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2398">Checksum</span></span>

<span data-ttu-id="eee87-2399">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2399">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2400">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2400">Definition</span></span>

<span data-ttu-id="eee87-2401">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2401">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2402">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2402">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2403">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2403">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="eee87-2404">IPv4의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2404">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2405">Regex_ipv4_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2405">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2406">Keyword_ipaddress의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2406">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="eee87-2407">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2407">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2408">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2408">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2409">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2409">No keyword from Keyword_ipaddress is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2410">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2410">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="eee87-2411">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="eee87-2411">Keyword_ipaddress</span></span>

- <span data-ttu-id="eee87-2412">IP(이 키워드는 대/소문자를 구분함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2412">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="eee87-2413">ip address</span><span class="sxs-lookup"><span data-stu-id="eee87-2413">ip address</span></span> 
- <span data-ttu-id="eee87-2414">ip addresses</span><span class="sxs-lookup"><span data-stu-id="eee87-2414">ip addresses</span></span>
- <span data-ttu-id="eee87-2415">internet protocol</span><span class="sxs-lookup"><span data-stu-id="eee87-2415">internet protocol</span></span>
- <span data-ttu-id="eee87-2416">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="eee87-2416">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="eee87-2417">Diseases의 국제 분류 (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="eee87-2417">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2418">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2418">Format</span></span>

<span data-ttu-id="eee87-2419">사전</span><span class="sxs-lookup"><span data-stu-id="eee87-2419">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2420">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2420">Pattern</span></span>

<span data-ttu-id="eee87-2421">Keyword</span><span class="sxs-lookup"><span data-stu-id="eee87-2421">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2422">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2422">Checksum</span></span>

<span data-ttu-id="eee87-2423">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2424">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2424">Definition</span></span>

<span data-ttu-id="eee87-2425">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2425">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2426">Dictionary_icd_10_cm에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2426">A keyword from Dictionary_icd_10_cm is found.</span></span>

```xml
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="eee87-2427">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2427">Keywords</span></span>

<span data-ttu-id="eee87-2428">Dictionary_icd_10_cm 키워드 사전의 모든 용어 이며, [Diseases의 국제 분류, 10 번째 수정, 임상 수정 (icd-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604)을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2428">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="eee87-2429">이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2429">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="eee87-2430">Diseases의 국제 분류 (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="eee87-2430">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2431">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2431">Format</span></span>

<span data-ttu-id="eee87-2432">사전</span><span class="sxs-lookup"><span data-stu-id="eee87-2432">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2433">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2433">Pattern</span></span>

<span data-ttu-id="eee87-2434">Keyword</span><span class="sxs-lookup"><span data-stu-id="eee87-2434">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2435">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2435">Checksum</span></span>

<span data-ttu-id="eee87-2436">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2436">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2437">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2437">Definition</span></span>

<span data-ttu-id="eee87-2438">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2438">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2439">Dictionary_icd_9_cm에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2439">A keyword from Dictionary_icd_9_cm is found.</span></span>

```xml
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2440">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2440">Keywords</span></span>

<span data-ttu-id="eee87-2441">[Diseases의 국가별 분류, 9 번째 버전의 임상 수정 (icd-9CM)](https://go.microsoft.com/fwlink/?linkid=852605)을 기반으로 하는 Dictionary_icd_9_cm 키워드 사전의 모든 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2441">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="eee87-2442">이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2442">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="eee87-2443">아일랜드 PPS(개인 공공 서비스) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2443">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2444">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2444">Format</span></span>

<span data-ttu-id="eee87-2445">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="eee87-2445">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="eee87-2446">7자리 숫자와 1-2개 문자 </span><span class="sxs-lookup"><span data-stu-id="eee87-2446">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="eee87-2447">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="eee87-2447">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="eee87-2448">7자리 숫자와 2개 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-2448">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2449">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2449">Pattern</span></span>

<span data-ttu-id="eee87-2450">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="eee87-2450">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="eee87-2451">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2451">Seven digits</span></span> 
- <span data-ttu-id="eee87-2452">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2452">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="eee87-2453">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="eee87-2453">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="eee87-2454">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2454">Seven digits</span></span> 
- <span data-ttu-id="eee87-2455">알파벳 검사 숫자에 해당하는 문자 1개(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="eee87-2455">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="eee87-2456">문자 "A" 또는 "H"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2456">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2457">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2457">Checksum</span></span>

<span data-ttu-id="eee87-2458">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2458">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2459">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2459">Definition</span></span>

<span data-ttu-id="eee87-2460">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2461">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2461">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2462">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2462">One of the following is true:</span></span>
    - <span data-ttu-id="eee87-2463">Keyword_ireland_pps에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2463">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="eee87-2464">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2464">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-2465">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2465">The checksum passes.</span></span>

<span data-ttu-id="eee87-2466">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2467">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2467">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2468">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2468">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2469">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2469">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="eee87-2470">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="eee87-2470">Keyword_ireland_pps</span></span>

- <span data-ttu-id="eee87-2471">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2471">Personal Public Service Number</span></span> 
- <span data-ttu-id="eee87-2472">PPS Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2472">PPS Number</span></span> 
- <span data-ttu-id="eee87-2473">PPS Num</span><span class="sxs-lookup"><span data-stu-id="eee87-2473">PPS Num</span></span> 
- <span data-ttu-id="eee87-2474">PPS No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2474">PPS No.</span></span> 
- <span data-ttu-id="eee87-2475">PPS #</span><span class="sxs-lookup"><span data-stu-id="eee87-2475">PPS #</span></span> 
- <span data-ttu-id="eee87-2476">.PPS #</span><span class="sxs-lookup"><span data-stu-id="eee87-2476">PPS#</span></span> 
- <span data-ttu-id="eee87-2477">PPSN</span><span class="sxs-lookup"><span data-stu-id="eee87-2477">PPSN</span></span> 
- <span data-ttu-id="eee87-2478">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="eee87-2478">Public Services Card</span></span> 
- <span data-ttu-id="eee87-2479">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="eee87-2479">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="eee87-2480">Uimh</span><span class="sxs-lookup"><span data-stu-id="eee87-2480">Uimh.</span></span> <span data-ttu-id="eee87-2481">PSP</span><span class="sxs-lookup"><span data-stu-id="eee87-2481">PSP</span></span> 
- <span data-ttu-id="eee87-2482">PSP</span><span class="sxs-lookup"><span data-stu-id="eee87-2482">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="eee87-2483">이스라엘 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2483">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2484">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2484">Format</span></span>

<span data-ttu-id="eee87-2485">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2485">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2486">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2486">Pattern</span></span>

<span data-ttu-id="eee87-2487">서식이</span><span class="sxs-lookup"><span data-stu-id="eee87-2487">Formatted:</span></span>
- <span data-ttu-id="eee87-2488">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2488">Two digits</span></span> 
- <span data-ttu-id="eee87-2489">대시 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-2489">A dash</span></span> 
- <span data-ttu-id="eee87-2490">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2490">Three digits</span></span> 
- <span data-ttu-id="eee87-2491">대시 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-2491">A dash</span></span> 
- <span data-ttu-id="eee87-2492">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2492">Eight digits</span></span>

<span data-ttu-id="eee87-2493">서식</span><span class="sxs-lookup"><span data-stu-id="eee87-2493">Unformatted:</span></span>
- <span data-ttu-id="eee87-2494">13자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2494">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2495">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2495">Checksum</span></span>

<span data-ttu-id="eee87-2496">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2496">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2497">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2497">Definition</span></span>

<span data-ttu-id="eee87-2498">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2499">Regex_israel_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2499">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2500">Keyword_israel_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2500">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2501">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2501">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="eee87-2502">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2502">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="eee87-2503">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2503">Bank Account Number</span></span> 
- <span data-ttu-id="eee87-2504">Bank Account</span><span class="sxs-lookup"><span data-stu-id="eee87-2504">Bank Account</span></span> 
- <span data-ttu-id="eee87-2505">Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2505">Account Number</span></span> 
- <span data-ttu-id="eee87-2506">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="eee87-2506">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="eee87-2507">이스라엘 국가 ID</span><span class="sxs-lookup"><span data-stu-id="eee87-2507">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2508">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2508">Format</span></span>

<span data-ttu-id="eee87-2509">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2509">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2510">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2510">Pattern</span></span>

<span data-ttu-id="eee87-2511">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2511">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2512">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2512">Checksum</span></span>

<span data-ttu-id="eee87-2513">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2514">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2514">Definition</span></span>

<span data-ttu-id="eee87-2515">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2515">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2516">Func_israeli_national_id_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2516">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2517">Keyword_Israel_National_ID의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2517">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="eee87-2518">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2518">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2519">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2519">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="eee87-2520">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="eee87-2520">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="eee87-2521">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="eee87-2521">מספר זהות</span></span> 
- <span data-ttu-id="eee87-2522">National ID Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2522">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="eee87-2523">이탈리아 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2523">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2524">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2524">Format</span></span>

<span data-ttu-id="eee87-2525">10개의 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-2525">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2526">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2526">Pattern</span></span>

- <span data-ttu-id="eee87-2527">10개의 문자 및 숫자 조합:</span><span class="sxs-lookup"><span data-stu-id="eee87-2527">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="eee87-2528">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2528">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-2529">문자 "A" 또는 "V"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2529">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-2530">7개 문자(대/소문자 구분 안 함), 숫자 또는 밑줄 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-2530">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="eee87-2531">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2531">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2532">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2532">Checksum</span></span>

<span data-ttu-id="eee87-2533">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2533">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2534">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2534">Definition</span></span>

<span data-ttu-id="eee87-2535">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2536">Regex_italy_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2536">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2537">Keyword_italy_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2537">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2538">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2538">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="eee87-2539">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2539">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="eee87-2540">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="eee87-2540">numero di patente di guida</span></span> 
- <span data-ttu-id="eee87-2541">patente di guida</span><span class="sxs-lookup"><span data-stu-id="eee87-2541">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="eee87-2542">일본 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2542">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2543">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2543">Format</span></span>

<span data-ttu-id="eee87-2544">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2544">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2545">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2545">Pattern</span></span>

<span data-ttu-id="eee87-2546">은행 계좌 번호:</span><span class="sxs-lookup"><span data-stu-id="eee87-2546">Bank account number:</span></span>
- <span data-ttu-id="eee87-2547">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2547">Seven or eight digits</span></span>
- <span data-ttu-id="eee87-2548">은행 계좌 지점 코드:</span><span class="sxs-lookup"><span data-stu-id="eee87-2548">Bank account branch code:</span></span>
- <span data-ttu-id="eee87-2549">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2549">Four digits</span></span> 
- <span data-ttu-id="eee87-2550">공백 또는 대시(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="eee87-2550">A space or dash (optional)</span></span> 
- <span data-ttu-id="eee87-2551">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2551">Three digits</span></span>

<span data-ttu-id="eee87-2552">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2552">Checksum</span></span>

<span data-ttu-id="eee87-2553">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2553">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2554">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2554">Definition</span></span>

<span data-ttu-id="eee87-2555">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2555">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2556">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2556">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2557">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2557">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="eee87-2558">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2558">One of the following is true:</span></span>
- <span data-ttu-id="eee87-2559">Func_jp_bank_account_branch_code 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2559">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2560">Keyword_jp_bank_branch_code의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2560">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="eee87-2561">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2561">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2562">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2562">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2563">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2563">A keyword from Keyword_jp_bank_account is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2564">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2564">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="eee87-2565">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="eee87-2565">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="eee87-2566">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2566">Checking Account Number</span></span> 
- <span data-ttu-id="eee87-2567">Checking Account</span><span class="sxs-lookup"><span data-stu-id="eee87-2567">Checking Account</span></span> 
- <span data-ttu-id="eee87-2568">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="eee87-2568">Checking Account #</span></span> 
- <span data-ttu-id="eee87-2569">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2569">Checking Acct Number</span></span> 
- <span data-ttu-id="eee87-2570">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="eee87-2570">Checking Acct #</span></span> 
- <span data-ttu-id="eee87-2571">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2571">Checking Acct No.</span></span> 
- <span data-ttu-id="eee87-2572">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2572">Checking Account No.</span></span> 
- <span data-ttu-id="eee87-2573">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2573">Bank Account Number</span></span> 
- <span data-ttu-id="eee87-2574">Bank Account</span><span class="sxs-lookup"><span data-stu-id="eee87-2574">Bank Account</span></span> 
- <span data-ttu-id="eee87-2575">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="eee87-2575">Bank Account #</span></span> 
- <span data-ttu-id="eee87-2576">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2576">Bank Acct Number</span></span> 
- <span data-ttu-id="eee87-2577">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="eee87-2577">Bank Acct #</span></span> 
- <span data-ttu-id="eee87-2578">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2578">Bank Acct No.</span></span> 
- <span data-ttu-id="eee87-2579">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2579">Bank Account No.</span></span> 
- <span data-ttu-id="eee87-2580">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2580">Savings Account Number</span></span> 
- <span data-ttu-id="eee87-2581">Savings Account</span><span class="sxs-lookup"><span data-stu-id="eee87-2581">Savings Account</span></span> 
- <span data-ttu-id="eee87-2582">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="eee87-2582">Savings Account #</span></span> 
- <span data-ttu-id="eee87-2583">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2583">Savings Acct Number</span></span> 
- <span data-ttu-id="eee87-2584">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="eee87-2584">Savings Acct #</span></span> 
- <span data-ttu-id="eee87-2585">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2585">Savings Acct No.</span></span> 
- <span data-ttu-id="eee87-2586">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2586">Savings Account No.</span></span> 
- <span data-ttu-id="eee87-2587">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2587">Debit Account Number</span></span> 
- <span data-ttu-id="eee87-2588">Debit Account</span><span class="sxs-lookup"><span data-stu-id="eee87-2588">Debit Account</span></span> 
- <span data-ttu-id="eee87-2589">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="eee87-2589">Debit Account #</span></span> 
- <span data-ttu-id="eee87-2590">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2590">Debit Acct Number</span></span> 
- <span data-ttu-id="eee87-2591">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="eee87-2591">Debit Acct #</span></span> 
- <span data-ttu-id="eee87-2592">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2592">Debit Acct No.</span></span> 
- <span data-ttu-id="eee87-2593">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2593">Debit Account No.</span></span> 
- <span data-ttu-id="eee87-2594">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="eee87-2594">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="eee87-2595">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="eee87-2595">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="eee87-2596">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="eee87-2596">＃勘定の確認</span></span> 
- <span data-ttu-id="eee87-2597">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="eee87-2597">勘定番号の確認</span></span> 
- <span data-ttu-id="eee87-2598">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="eee87-2598">口座番号の確認</span></span> 
- <span data-ttu-id="eee87-2599">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2599">銀行口座番号</span></span> 
- <span data-ttu-id="eee87-2600">銀行口座</span><span class="sxs-lookup"><span data-stu-id="eee87-2600">銀行口座</span></span> 
- <span data-ttu-id="eee87-2601">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2601">銀行口座＃</span></span> 
- <span data-ttu-id="eee87-2602">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2602">銀行の勘定番号</span></span> 
- <span data-ttu-id="eee87-2603">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2603">銀行のacct＃</span></span> 
- <span data-ttu-id="eee87-2604">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="eee87-2604">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="eee87-2605">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2605">銀行口座番号</span></span>
- <span data-ttu-id="eee87-2606">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2606">普通預金口座番号</span></span> 
- <span data-ttu-id="eee87-2607">預金口座</span><span class="sxs-lookup"><span data-stu-id="eee87-2607">預金口座</span></span> 
- <span data-ttu-id="eee87-2608">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2608">貯蓄口座＃</span></span> 
- <span data-ttu-id="eee87-2609">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="eee87-2609">貯蓄勘定の数</span></span> 
- <span data-ttu-id="eee87-2610">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2610">貯蓄勘定＃</span></span> 
- <span data-ttu-id="eee87-2611">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2611">貯蓄勘定番号</span></span> 
- <span data-ttu-id="eee87-2612">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2612">普通預金口座番号</span></span> 
- <span data-ttu-id="eee87-2613">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2613">引き落とし口座番号</span></span> 
- <span data-ttu-id="eee87-2614">口座番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2614">口座番号</span></span> 
- <span data-ttu-id="eee87-2615">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2615">口座番号＃</span></span> 
- <span data-ttu-id="eee87-2616">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2616">デビットのacct番号</span></span> 
- <span data-ttu-id="eee87-2617">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2617">デビット勘定＃</span></span> 
- <span data-ttu-id="eee87-2618">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2618">デビットACCTの番号</span></span> 
- <span data-ttu-id="eee87-2619">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2619">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="eee87-2620">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="eee87-2620">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="eee87-2621">Otemachi</span><span class="sxs-lookup"><span data-stu-id="eee87-2621">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="eee87-2622">일본 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2622">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2623">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2623">Format</span></span>

<span data-ttu-id="eee87-2624">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2624">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2625">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2625">Pattern</span></span>

<span data-ttu-id="eee87-2626">12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2626">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2627">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2627">Checksum</span></span>

<span data-ttu-id="eee87-2628">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2628">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2629">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2629">Definition</span></span>

<span data-ttu-id="eee87-2630">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2630">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2631">Func_jp_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2631">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2632">Keyword_jp_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2632">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```xml
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2633">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2633">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="eee87-2634">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2634">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="eee87-2635">dl #</span><span class="sxs-lookup"><span data-stu-id="eee87-2635">dl#</span></span> 
- <span data-ttu-id="eee87-2636">DL</span><span class="sxs-lookup"><span data-stu-id="eee87-2636">DL＃</span></span> 
- <span data-ttu-id="eee87-2637">된다 #</span><span class="sxs-lookup"><span data-stu-id="eee87-2637">dls#</span></span> 
- <span data-ttu-id="eee87-2638">된다</span><span class="sxs-lookup"><span data-stu-id="eee87-2638">DLS＃</span></span> 
- <span data-ttu-id="eee87-2639">driver license</span><span class="sxs-lookup"><span data-stu-id="eee87-2639">driver license</span></span> 
- <span data-ttu-id="eee87-2640">driver licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-2640">driver licenses</span></span> 
- <span data-ttu-id="eee87-2641">drivers license</span><span class="sxs-lookup"><span data-stu-id="eee87-2641">drivers license</span></span> 
- <span data-ttu-id="eee87-2642">driver's license</span><span class="sxs-lookup"><span data-stu-id="eee87-2642">driver's license</span></span> 
- <span data-ttu-id="eee87-2643">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-2643">drivers licenses</span></span> 
- <span data-ttu-id="eee87-2644">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-2644">driver's licenses</span></span> 
- <span data-ttu-id="eee87-2645">driving licence</span><span class="sxs-lookup"><span data-stu-id="eee87-2645">driving licence</span></span> 
- <span data-ttu-id="eee87-2646">lic #</span><span class="sxs-lookup"><span data-stu-id="eee87-2646">lic#</span></span> 
- <span data-ttu-id="eee87-2647">LIC</span><span class="sxs-lookup"><span data-stu-id="eee87-2647">LIC＃</span></span> 
- <span data-ttu-id="eee87-2648">driver'lics #</span><span class="sxs-lookup"><span data-stu-id="eee87-2648">lics#</span></span> 
- <span data-ttu-id="eee87-2649">state id</span><span class="sxs-lookup"><span data-stu-id="eee87-2649">state id</span></span> 
- <span data-ttu-id="eee87-2650">state identification</span><span class="sxs-lookup"><span data-stu-id="eee87-2650">state identification</span></span> 
- <span data-ttu-id="eee87-2651">state identification number</span><span class="sxs-lookup"><span data-stu-id="eee87-2651">state identification number</span></span> 
- <span data-ttu-id="eee87-2652">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2652">低所得国＃</span></span> 
- <span data-ttu-id="eee87-2653">免許証</span><span class="sxs-lookup"><span data-stu-id="eee87-2653">免許証</span></span> 
- <span data-ttu-id="eee87-2654">状態ID</span><span class="sxs-lookup"><span data-stu-id="eee87-2654">状態ID</span></span>
- <span data-ttu-id="eee87-2655">状態の識別</span><span class="sxs-lookup"><span data-stu-id="eee87-2655">状態の識別</span></span> 
- <span data-ttu-id="eee87-2656">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2656">状態の識別番号</span></span> 
- <span data-ttu-id="eee87-2657">運転免許</span><span class="sxs-lookup"><span data-stu-id="eee87-2657">運転免許</span></span> 
- <span data-ttu-id="eee87-2658">運転免許証</span><span class="sxs-lookup"><span data-stu-id="eee87-2658">運転免許証</span></span> 
- <span data-ttu-id="eee87-2659">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2659">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="eee87-2660">일본 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2660">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2661">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2661">Format</span></span>

<span data-ttu-id="eee87-2662">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2662">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2663">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2663">Pattern</span></span>

<span data-ttu-id="eee87-2664">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2664">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2665">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2665">Checksum</span></span>

<span data-ttu-id="eee87-2666">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2666">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2667">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2667">Definition</span></span>

<span data-ttu-id="eee87-2668">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2668">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2669">Func_jp_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2669">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2670">Keyword_jp_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2670">A keyword from Keyword_jp_passport is found.</span></span>

```xml
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2671">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2671">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="eee87-2672">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-2672">Keyword_jp_passport</span></span>

- <span data-ttu-id="eee87-2673">パスポート</span><span class="sxs-lookup"><span data-stu-id="eee87-2673">パスポート</span></span> 
- <span data-ttu-id="eee87-2674">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2674">パスポート番号</span></span> 
- <span data-ttu-id="eee87-2675">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="eee87-2675">パスポートのNum</span></span> 
- <span data-ttu-id="eee87-2676">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="eee87-2676">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="eee87-2677">일본 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2677">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2678">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2678">Format</span></span>

<span data-ttu-id="eee87-2679">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2679">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2680">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2680">Pattern</span></span>

<span data-ttu-id="eee87-2681">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2681">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2682">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2682">Checksum</span></span>

<span data-ttu-id="eee87-2683">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2683">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2684">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2684">Definition</span></span>

<span data-ttu-id="eee87-2685">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2685">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2686">Func_jp_resident_registration_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2686">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2687">Keyword_jp_resident_registration_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2687">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```xml
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2688">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2688">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="eee87-2689">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2689">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="eee87-2690">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2690">Resident Registration Number</span></span>
- <span data-ttu-id="eee87-2691">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2691">Resident Register Number</span></span> 
- <span data-ttu-id="eee87-2692">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2692">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="eee87-2693">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2693">Resident Registration No.</span></span> 
- <span data-ttu-id="eee87-2694">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2694">Resident Register No.</span></span> 
- <span data-ttu-id="eee87-2695">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2695">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="eee87-2696">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2696">Basic Resident Register No.</span></span> 
- <span data-ttu-id="eee87-2697">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="eee87-2697">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="eee87-2698">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2698">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="eee87-2699">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="eee87-2699">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="eee87-2700">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2700">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="eee87-2701">일본 SIN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="eee87-2701">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2702">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2702">Format</span></span>

<span data-ttu-id="eee87-2703">7-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2703">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2704">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2704">Pattern</span></span>

<span data-ttu-id="eee87-2705">7-12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2705">7-12 digits:</span></span>
- <span data-ttu-id="eee87-2706">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2706">Four digits</span></span> 
- <span data-ttu-id="eee87-2707">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="eee87-2707">A hyphen (optional)</span></span> 
- <span data-ttu-id="eee87-2708">6 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="eee87-2708">Six digits OR</span></span>
- <span data-ttu-id="eee87-2709">7-12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2709">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2710">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2710">Checksum</span></span>

<span data-ttu-id="eee87-2711">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2711">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2712">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2712">Definition</span></span>

<span data-ttu-id="eee87-2713">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2713">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2714">Func_jp_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2714">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2715">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2715">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="eee87-2716">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2716">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2717">Func_jp_sin_pre_1997 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2717">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2718">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2718">A keyword from Keyword_jp_sin is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2719">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2719">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="eee87-2720">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="eee87-2720">Keyword_jp_sin</span></span>

- <span data-ttu-id="eee87-2721">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="eee87-2721">Social Insurance No.</span></span> 
- <span data-ttu-id="eee87-2722">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="eee87-2722">Social Insurance Num</span></span> 
- <span data-ttu-id="eee87-2723">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2723">Social Insurance Number</span></span> 
- <span data-ttu-id="eee87-2724">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="eee87-2724">社会保険のテンキー</span></span> 
- <span data-ttu-id="eee87-2725">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2725">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="eee87-2726">일본어 거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2726">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2727">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2727">Format</span></span>

<span data-ttu-id="eee87-2728">12 개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2728">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2729">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2729">Pattern</span></span>

<span data-ttu-id="eee87-2730">12 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2730">12 letters and digits:</span></span>
- <span data-ttu-id="eee87-2731">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2731">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="eee87-2732">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2732">Eight digits</span></span> 
- <span data-ttu-id="eee87-2733">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-2733">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2734">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2734">Checksum</span></span>

<span data-ttu-id="eee87-2735">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2736">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2736">Definition</span></span>

<span data-ttu-id="eee87-2737">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2737">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2738">정규식 Regex_jp_residence_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2738">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2739">Keyword_jp_residence_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2739">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```xml
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2740">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2740">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="eee87-2741">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2741">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="eee87-2742">거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2742">Residence card number</span></span>
- <span data-ttu-id="eee87-2743">거주지 카드 아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2743">Residence card no</span></span>
- <span data-ttu-id="eee87-2744">거주지 카드 #</span><span class="sxs-lookup"><span data-stu-id="eee87-2744">Residence card #</span></span>
- <span data-ttu-id="eee87-2745">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="eee87-2745">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="eee87-2746">말레이시아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2746">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2747">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2747">Format</span></span>

<span data-ttu-id="eee87-2748">선택적으로 하이픈을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2748">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2749">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2749">Pattern</span></span>

<span data-ttu-id="eee87-2750">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2750">12 digits:</span></span>
- <span data-ttu-id="eee87-2751">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-2751">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="eee87-2752">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="eee87-2752">A dash (optional)</span></span> 
- <span data-ttu-id="eee87-2753">2개 문자로 이루어진 출생지 코드 </span><span class="sxs-lookup"><span data-stu-id="eee87-2753">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="eee87-2754">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="eee87-2754">A dash (optional)</span></span> 
- <span data-ttu-id="eee87-2755">임의의 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-2755">Three random digits</span></span> 
- <span data-ttu-id="eee87-2756">1자리 성별 코드</span><span class="sxs-lookup"><span data-stu-id="eee87-2756">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2757">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2757">Checksum</span></span>

<span data-ttu-id="eee87-2758">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2758">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2759">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2759">Definition</span></span>

<span data-ttu-id="eee87-2760">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2760">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2761">정규식 Regex_malaysia_id_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2761">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2762">Keyword_malaysia_id_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2762">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```xml
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2763">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2763">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="eee87-2764">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2764">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="eee87-2765">디지털 응용 프로그램 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2765">digital application card</span></span>
- <span data-ttu-id="eee87-2766">i/c</span><span class="sxs-lookup"><span data-stu-id="eee87-2766">i/c</span></span>
- <span data-ttu-id="eee87-2767">i/c 아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2767">i/c no</span></span>
- <span data-ttu-id="eee87-2768">비용</span><span class="sxs-lookup"><span data-stu-id="eee87-2768">ic</span></span>
- <span data-ttu-id="eee87-2769">ic 아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2769">ic no</span></span>
- <span data-ttu-id="eee87-2770">id card</span><span class="sxs-lookup"><span data-stu-id="eee87-2770">id card</span></span>
- <span data-ttu-id="eee87-2771">식별 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2771">identification Card</span></span>
- <span data-ttu-id="eee87-2772">identity card</span><span class="sxs-lookup"><span data-stu-id="eee87-2772">identity card</span></span>
- <span data-ttu-id="eee87-2773">k/p</span><span class="sxs-lookup"><span data-stu-id="eee87-2773">k/p</span></span>
- <span data-ttu-id="eee87-2774">k/p 아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2774">k/p no</span></span>
- <span data-ttu-id="eee87-2775">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="eee87-2775">kad akuan diri</span></span>
- <span data-ttu-id="eee87-2776">kad aplikasi 디지털</span><span class="sxs-lookup"><span data-stu-id="eee87-2776">kad aplikasi digital</span></span>
- <span data-ttu-id="eee87-2777">kad pengenalan 말레이시아</span><span class="sxs-lookup"><span data-stu-id="eee87-2777">kad pengenalan malaysia</span></span>
- <span data-ttu-id="eee87-2778">kp</span><span class="sxs-lookup"><span data-stu-id="eee87-2778">kp</span></span>
- <span data-ttu-id="eee87-2779">kp 아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2779">kp no</span></span>
- <span data-ttu-id="eee87-2780">mykad</span><span class="sxs-lookup"><span data-stu-id="eee87-2780">mykad</span></span>
- <span data-ttu-id="eee87-2781">mykas</span><span class="sxs-lookup"><span data-stu-id="eee87-2781">mykas</span></span>
- <span data-ttu-id="eee87-2782">mykid</span><span class="sxs-lookup"><span data-stu-id="eee87-2782">mykid</span></span>
- <span data-ttu-id="eee87-2783">mypr</span><span class="sxs-lookup"><span data-stu-id="eee87-2783">mypr</span></span>
- <span data-ttu-id="eee87-2784">myta</span><span class="sxs-lookup"><span data-stu-id="eee87-2784">mytentera</span></span>
- <span data-ttu-id="eee87-2785">말레이시아 id 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2785">malaysia identity card</span></span>
- <span data-ttu-id="eee87-2786">말레이지아 id 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2786">malaysian identity card</span></span>
- <span data-ttu-id="eee87-2787">nric</span><span class="sxs-lookup"><span data-stu-id="eee87-2787">nric</span></span>
- <span data-ttu-id="eee87-2788">개인 식별 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2788">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="eee87-2789">네덜란드 시민 서비스(BSN) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2789">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2790">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2790">Format</span></span>

<span data-ttu-id="eee87-2791">선택적으로 공백을 포함하는 8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2791">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2792">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2792">Pattern</span></span>

<span data-ttu-id="eee87-2793">8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2793">8-9 digits:</span></span>
- <span data-ttu-id="eee87-2794">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2794">Three digits</span></span> 
- <span data-ttu-id="eee87-2795">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="eee87-2795">A space (optional)</span></span> 
- <span data-ttu-id="eee87-2796">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2796">Three digits</span></span> 
- <span data-ttu-id="eee87-2797">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="eee87-2797">A space (optional)</span></span> 
- <span data-ttu-id="eee87-2798">2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2798">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2799">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2799">Checksum</span></span>

<span data-ttu-id="eee87-2800">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2801">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2801">Definition</span></span>

<span data-ttu-id="eee87-2802">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2803">Func_netherlands_bsn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2803">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2804">Keyword_netherlands_bsn에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2804">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="eee87-2805">Func_eu_date2 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2805">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-2806">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2806">The checksum passes.</span></span>

```xml
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2807">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2807">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="eee87-2808">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="eee87-2808">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="eee87-2809">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="eee87-2809">Citizen service number</span></span> 
- <span data-ttu-id="eee87-2810">BSN</span><span class="sxs-lookup"><span data-stu-id="eee87-2810">BSN</span></span> 
- <span data-ttu-id="eee87-2811">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2811">Burgerservicenummer</span></span> 
- <span data-ttu-id="eee87-2812">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2812">Sofinummer</span></span> 
- <span data-ttu-id="eee87-2813">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2813">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="eee87-2814">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2814">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="eee87-2815">뉴질랜드 보건부 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2815">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2816">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2816">Format</span></span>

<span data-ttu-id="eee87-2817">3개 문자, 공백 1개(선택 사항) 및 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2817">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2818">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2818">Pattern</span></span>

<span data-ttu-id="eee87-2819">3 개의 문자 (대/소문자 구분 안 함) 공백 (선택 사항) 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2819">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2820">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2820">Checksum</span></span>

<span data-ttu-id="eee87-2821">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2821">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2822">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2822">Definition</span></span>

<span data-ttu-id="eee87-2823">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2823">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2824">Func_new_zealand_ministry_of_health_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2824">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2825">Keyword_nz_terms의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2825">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="eee87-2826">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2826">The checksum passes.</span></span>

```xml
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

<span data-ttu-id="eee87-2827">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2827">Keywords</span></span>

<span data-ttu-id="eee87-2828">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="eee87-2828">Keyword_nz_terms</span></span>

- <span data-ttu-id="eee87-2829">NHI</span><span class="sxs-lookup"><span data-stu-id="eee87-2829">NHI</span></span> 
- <span data-ttu-id="eee87-2830">New Zealand</span><span class="sxs-lookup"><span data-stu-id="eee87-2830">New Zealand</span></span> 
- <span data-ttu-id="eee87-2831">상태</span><span class="sxs-lookup"><span data-stu-id="eee87-2831">Health</span></span> 
- <span data-ttu-id="eee87-2832">처리가</span><span class="sxs-lookup"><span data-stu-id="eee87-2832">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="eee87-2833">Norway Identification Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2833">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2834">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2834">Format</span></span>

<span data-ttu-id="eee87-2835">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2835">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2836">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2836">Pattern</span></span>

<span data-ttu-id="eee87-2837">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2837">11 digits:</span></span>
- <span data-ttu-id="eee87-2838">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-2838">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="eee87-2839">3자리 개인 번호 </span><span class="sxs-lookup"><span data-stu-id="eee87-2839">Three-digit individual number</span></span> 
- <span data-ttu-id="eee87-2840">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2840">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2841">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2841">Checksum</span></span>

<span data-ttu-id="eee87-2842">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2842">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2843">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2843">Definition</span></span>

<span data-ttu-id="eee87-2844">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2844">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2845">Func_norway_id_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2845">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2846">Keyword_norway_id_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2846">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="eee87-2847">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2847">The checksum passes.</span></span>
- <span data-ttu-id="eee87-2848">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2848">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2849">Func_norway_id_numbe 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2849">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2850">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2850">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2851">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2851">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="eee87-2852">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2852">Keyword_norway_id_number</span></span>

- <span data-ttu-id="eee87-2853">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="eee87-2853">Personal identification number</span></span>
- <span data-ttu-id="eee87-2854">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2854">Norwegian ID Number</span></span>
- <span data-ttu-id="eee87-2855">ID Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2855">ID Number</span></span>
- <span data-ttu-id="eee87-2856">확인과</span><span class="sxs-lookup"><span data-stu-id="eee87-2856">Identification</span></span>
- <span data-ttu-id="eee87-2857">Personnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2857">Personnummer</span></span>
- <span data-ttu-id="eee87-2858">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="eee87-2858">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="eee87-2859">필리핀 통합 다목적 ID 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2859">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2860">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2860">Format</span></span>

<span data-ttu-id="eee87-2861">하이픈으로 구분된 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2861">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2862">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2862">Pattern</span></span>

<span data-ttu-id="eee87-2863">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2863">12 digits:</span></span>
- <span data-ttu-id="eee87-2864">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2864">Four digits</span></span> 
- <span data-ttu-id="eee87-2865">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-2865">A hyphen</span></span> 
- <span data-ttu-id="eee87-2866">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2866">Seven digits</span></span> 
- <span data-ttu-id="eee87-2867">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-2867">A hyphen</span></span> 
- <span data-ttu-id="eee87-2868">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2868">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2869">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2869">Checksum</span></span>

<span data-ttu-id="eee87-2870">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2870">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2871">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2871">Definition</span></span>

<span data-ttu-id="eee87-2872">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2873">정규식 Regex_philippines_unified_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2873">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2874">Keyword_philippines_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2874">A keyword from Keyword_philippines_id is found.</span></span>

```xml
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2875">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2875">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="eee87-2876">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="eee87-2876">Keyword_philippines_id</span></span>

- <span data-ttu-id="eee87-2877">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="eee87-2877">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="eee87-2878">UMID</span><span class="sxs-lookup"><span data-stu-id="eee87-2878">UMID</span></span> 
- <span data-ttu-id="eee87-2879">Identity Card</span><span class="sxs-lookup"><span data-stu-id="eee87-2879">Identity Card</span></span> 
- <span data-ttu-id="eee87-2880">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="eee87-2880">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="eee87-2881">폴란드 ID 카드</span><span class="sxs-lookup"><span data-stu-id="eee87-2881">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2882">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2882">Format</span></span>

<span data-ttu-id="eee87-2883">3개의 문자 및 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2883">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2884">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2884">Pattern</span></span>

<span data-ttu-id="eee87-2885">3개의 문자(대/소문자 구분 안 함)와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2885">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2886">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2886">Checksum</span></span>

<span data-ttu-id="eee87-2887">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2887">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2888">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2888">Definition</span></span>

<span data-ttu-id="eee87-2889">DLP 정책은 300 문자 근사에서 Func_polish_national_id 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2889">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="eee87-2890">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2890">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="eee87-2891">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2891">The checksum passes.</span></span>

```xml
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2892">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2892">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="eee87-2893">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2893">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="eee87-2894">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="eee87-2894">Dowód osobisty</span></span>
- <span data-ttu-id="eee87-2895">U r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="eee87-2895">Numer dowodu osobistego</span></span>
- <span data-ttu-id="eee87-2896">Nazwa i u r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="eee87-2896">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="eee87-2897">Nazwa i veiligheid dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="eee87-2897">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="eee87-2898">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="eee87-2898">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="eee87-2899">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="eee87-2899">Dowód Tożsamości</span></span>
- <span data-ttu-id="eee87-2900">dow.</span><span class="sxs-lookup"><span data-stu-id="eee87-2900">dow.</span></span> <span data-ttu-id="eee87-2901">르.</span><span class="sxs-lookup"><span data-stu-id="eee87-2901">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="eee87-2902">폴란드 국가 ID(PESEL)</span><span class="sxs-lookup"><span data-stu-id="eee87-2902">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2903">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2903">Format</span></span>

<span data-ttu-id="eee87-2904">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2904">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2905">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2905">Pattern</span></span>

<span data-ttu-id="eee87-2906">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2906">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2907">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2907">Checksum</span></span>

<span data-ttu-id="eee87-2908">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2908">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2909">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2909">Definition</span></span>

<span data-ttu-id="eee87-2910">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2910">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2911">Func_pesel_identification_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2911">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2912">Keyword_pesel_identification_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2912">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="eee87-2913">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2913">The checksum passes.</span></span>

```xml
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2914">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2914">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="eee87-2915">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2915">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="eee87-2916">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="eee87-2916">Nr PESEL</span></span>
- <span data-ttu-id="eee87-2917">PESEL</span><span class="sxs-lookup"><span data-stu-id="eee87-2917">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="eee87-2918">폴란드 여권</span><span class="sxs-lookup"><span data-stu-id="eee87-2918">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2919">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2919">Format</span></span>

<span data-ttu-id="eee87-2920">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2920">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2921">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2921">Pattern</span></span>

<span data-ttu-id="eee87-2922">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2922">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2923">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2923">Checksum</span></span>

<span data-ttu-id="eee87-2924">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2924">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2925">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2925">Definition</span></span>

<span data-ttu-id="eee87-2926">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2926">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2927">Func_polish_passport_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2927">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2928">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2928">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="eee87-2929">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2929">The checksum passes.</span></span>

```xml
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2930">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2930">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="eee87-2931">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="eee87-2931">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="eee87-2932">U r i (zportu)</span><span class="sxs-lookup"><span data-stu-id="eee87-2932">Numer paszportu</span></span>
- <span data-ttu-id="eee87-2933">Veiligheid.</span><span class="sxs-lookup"><span data-stu-id="eee87-2933">Nr.</span></span> <span data-ttu-id="eee87-2934">고 zportu</span><span class="sxs-lookup"><span data-stu-id="eee87-2934">Paszportu</span></span>
- <span data-ttu-id="eee87-2935">고 zport</span><span class="sxs-lookup"><span data-stu-id="eee87-2935">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="eee87-2936">포르투갈 시민 카드 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2936">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2937">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2937">Format</span></span>

<span data-ttu-id="eee87-2938">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2938">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2939">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2939">Pattern</span></span>

<span data-ttu-id="eee87-2940">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2940">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2941">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2941">Checksum</span></span>

<span data-ttu-id="eee87-2942">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2942">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2943">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2943">Definition</span></span>

<span data-ttu-id="eee87-2944">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2944">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2945">정규식 Regex_portugal_citizen_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2945">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2946">Keyword_portugal_citizen_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2946">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```xml
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-2947">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2947">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="eee87-2948">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="eee87-2948">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="eee87-2949">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="eee87-2949">Citizen Card</span></span>
- <span data-ttu-id="eee87-2950">National ID Card</span><span class="sxs-lookup"><span data-stu-id="eee87-2950">National ID Card</span></span>
- <span data-ttu-id="eee87-2951">참조란</span><span class="sxs-lookup"><span data-stu-id="eee87-2951">CC</span></span>
- <span data-ttu-id="eee87-2952">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="eee87-2952">Cartão de Cidadão</span></span>
- <span data-ttu-id="eee87-2953">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="eee87-2953">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="eee87-2954">사우디 아라비아 국가 ID</span><span class="sxs-lookup"><span data-stu-id="eee87-2954">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2955">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2955">Format</span></span>

<span data-ttu-id="eee87-2956">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2956">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2957">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2957">Pattern</span></span>

<span data-ttu-id="eee87-2958">10자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2958">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2959">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2959">Checksum</span></span>

<span data-ttu-id="eee87-2960">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-2960">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2961">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2961">Definition</span></span>

<span data-ttu-id="eee87-2962">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2962">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2963">Regex_saudi_arabia_national_id 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2963">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2964">Keyword_saudi_arabia_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2964">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2965">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2965">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="eee87-2966">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="eee87-2966">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="eee87-2967">Identification Card</span><span class="sxs-lookup"><span data-stu-id="eee87-2967">Identification Card</span></span> 
- <span data-ttu-id="eee87-2968">I card number</span><span class="sxs-lookup"><span data-stu-id="eee87-2968">I card number</span></span> 
- <span data-ttu-id="eee87-2969">ID number</span><span class="sxs-lookup"><span data-stu-id="eee87-2969">ID number</span></span> 
- <span data-ttu-id="eee87-2970">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="eee87-2970">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="eee87-2971">싱가포르 NRIC(국가 등록 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2971">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-2972">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-2972">Format</span></span>

<span data-ttu-id="eee87-2973">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2973">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-2974">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-2974">Pattern</span></span>

- <span data-ttu-id="eee87-2975">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-2975">Nine letters and digits:</span></span>
- <span data-ttu-id="eee87-2976">문자 "F", "G", "S" 또는 "T"(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="eee87-2976">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-2977">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2977">Seven digits</span></span> 
- <span data-ttu-id="eee87-2978">알파벳 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-2978">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-2979">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-2979">Checksum</span></span>

<span data-ttu-id="eee87-2980">예</span><span class="sxs-lookup"><span data-stu-id="eee87-2980">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-2981">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-2981">Definition</span></span>

<span data-ttu-id="eee87-2982">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2982">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2983">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2983">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2984">Keyword_singapore_nric에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2984">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="eee87-2985">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2985">The checksum passes.</span></span>

<span data-ttu-id="eee87-2986">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-2987">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2987">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-2988">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-2988">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-2989">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-2989">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="eee87-2990">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="eee87-2990">Keyword_singapore_nric</span></span>

- <span data-ttu-id="eee87-2991">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="eee87-2991">National Registration Identity Card</span></span> 
- <span data-ttu-id="eee87-2992">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2992">Identity Card Number</span></span> 
- <span data-ttu-id="eee87-2993">NRIC</span><span class="sxs-lookup"><span data-stu-id="eee87-2993">NRIC</span></span> 
- <span data-ttu-id="eee87-2994">비용</span><span class="sxs-lookup"><span data-stu-id="eee87-2994">IC</span></span> 
- <span data-ttu-id="eee87-2995">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="eee87-2995">Foreign Identification Number</span></span> 
- <span data-ttu-id="eee87-2996">삭제할</span><span class="sxs-lookup"><span data-stu-id="eee87-2996">FIN</span></span> 
- <span data-ttu-id="eee87-2997">身份证</span><span class="sxs-lookup"><span data-stu-id="eee87-2997">身份证</span></span> 
- <span data-ttu-id="eee87-2998">身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-2998">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="eee87-2999">남아프리카 공화국 식별 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-2999">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3000">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3000">Format</span></span>

<span data-ttu-id="eee87-3001">공백을 포함할 수 있는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3001">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3002">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3002">Pattern</span></span>

<span data-ttu-id="eee87-3003">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3003">13 digits:</span></span>
- <span data-ttu-id="eee87-3004">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-3004">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="eee87-3005">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3005">Four digits</span></span> 
- <span data-ttu-id="eee87-3006">1자리 시민권 표시 </span><span class="sxs-lookup"><span data-stu-id="eee87-3006">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="eee87-3007">숫자 "8" 또는 "9" </span><span class="sxs-lookup"><span data-stu-id="eee87-3007">The digit "8" or "9"</span></span> 
- <span data-ttu-id="eee87-3008">체크섬 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3008">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3009">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3009">Checksum</span></span>

<span data-ttu-id="eee87-3010">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3010">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3011">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3011">Definition</span></span>

<span data-ttu-id="eee87-3012">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3012">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3013">Func_south_africa_identification_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3013">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3014">Keyword_south_africa_identification_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3014">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="eee87-3015">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3015">The checksum passes.</span></span>

```xml
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3016">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3016">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="eee87-3017">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="eee87-3017">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="eee87-3018">Identity card</span><span class="sxs-lookup"><span data-stu-id="eee87-3018">Identity card</span></span>
- <span data-ttu-id="eee87-3019">ID</span><span class="sxs-lookup"><span data-stu-id="eee87-3019">ID</span></span>
- <span data-ttu-id="eee87-3020">확인과</span><span class="sxs-lookup"><span data-stu-id="eee87-3020">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="eee87-3021">한국 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3021">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3022">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3022">Format</span></span>

<span data-ttu-id="eee87-3023">하이픈을 포함하는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3023">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3024">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3024">Pattern</span></span>

<span data-ttu-id="eee87-3025">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3025">13 digits:</span></span>
- <span data-ttu-id="eee87-3026">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-3026">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="eee87-3027">하이픈</span><span class="sxs-lookup"><span data-stu-id="eee87-3027">A hyphen</span></span> 
- <span data-ttu-id="eee87-3028">세기 및 성별에 따라 결정되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-3028">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="eee87-3029">4자리 출생 지역 코드 </span><span class="sxs-lookup"><span data-stu-id="eee87-3029">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="eee87-3030">앞 번호가 동일한 사람을 구분하기 위해 사용되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="eee87-3030">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="eee87-3031">검사 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3031">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3032">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3032">Checksum</span></span>

<span data-ttu-id="eee87-3033">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3033">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3034">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3034">Definition</span></span>

<span data-ttu-id="eee87-3035">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3035">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3036">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3036">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3037">Keyword_south_korea_resident_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3037">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="eee87-3038">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3038">The checksum passes.</span></span>

<span data-ttu-id="eee87-3039">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3039">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3040">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3040">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3041">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3041">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3042">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3042">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="eee87-3043">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="eee87-3043">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="eee87-3044">National ID card</span><span class="sxs-lookup"><span data-stu-id="eee87-3044">National ID card</span></span> 
- <span data-ttu-id="eee87-3045">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3045">Citizen's Registration Number</span></span> 
- <span data-ttu-id="eee87-3046">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="eee87-3046">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="eee87-3047">RRN</span><span class="sxs-lookup"><span data-stu-id="eee87-3047">RRN</span></span> 
- <span data-ttu-id="eee87-3048">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3048">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="eee87-3049">스페인 SSN(사회 보장 번호)</span><span class="sxs-lookup"><span data-stu-id="eee87-3049">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3050">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3050">Format</span></span>

<span data-ttu-id="eee87-3051">11-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3051">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3052">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3052">Pattern</span></span>

<span data-ttu-id="eee87-3053">11-12 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3053">11-12 digits:</span></span>
- <span data-ttu-id="eee87-3054">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3054">Two digits</span></span> 
- <span data-ttu-id="eee87-3055">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="eee87-3055">A forward slash (optional)</span></span> 
- <span data-ttu-id="eee87-3056">7-8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3056">7-8 digits</span></span> 
- <span data-ttu-id="eee87-3057">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="eee87-3057">A forward slash (optional)</span></span> 
- <span data-ttu-id="eee87-3058">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3058">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3059">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3059">Checksum</span></span>

<span data-ttu-id="eee87-3060">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3061">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3061">Definition</span></span>

<span data-ttu-id="eee87-3062">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3063">Func_spanish_social_security_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3063">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3064">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3064">The checksum passes.</span></span>

```xml
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3065">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3065">Keywords</span></span>

<span data-ttu-id="eee87-3066">없음</span><span class="sxs-lookup"><span data-stu-id="eee87-3066">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="eee87-3067">SQL Server 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="eee87-3067">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3068">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3068">Format</span></span>

<span data-ttu-id="eee87-3069">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "User Id", "User ID", "uid" 또는 "UserId"입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3069">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3070">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3070">Pattern</span></span>

- <span data-ttu-id="eee87-3071">문자열 "User Id", "User ID", "uid" 또는 "UserId"</span><span class="sxs-lookup"><span data-stu-id="eee87-3071">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="eee87-3072">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-3072">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="eee87-3073">문자열 "Password" 또는 "pwd" (여기에서 "pwd" 앞에 소문자 문자가 오지 않음)</span><span class="sxs-lookup"><span data-stu-id="eee87-3073">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="eee87-3074">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-3074">An equal sign (=)</span></span>
- <span data-ttu-id="eee87-3075">달러 기호 ($), 백분율 기호 (%, 부등호 (>), 기호 (@), 따옴표 ("), 세미콜론 (;), 왼쪽 중괄호 ([) 또는 왼쪽 대괄호 ({))가 아닌 모든 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-3075">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="eee87-3076">세미콜론 (;), 슬래시 (/) 또는 따옴표 (")가 아닌 7-128 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-3076">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="eee87-3077">세미콜론 (;) 또는 따옴표 (")</span><span class="sxs-lookup"><span data-stu-id="eee87-3077">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3078">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3078">Checksum</span></span>

<span data-ttu-id="eee87-3079">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3079">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3080">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3080">Definition</span></span>

<span data-ttu-id="eee87-3081">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3081">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3082">정규식 CEP_Regex_SQLServerConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3082">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3083">CEP_GlobalFilter의 키워드를 찾을 수 **없습니다** .</span><span class="sxs-lookup"><span data-stu-id="eee87-3083">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="eee87-3084">CEP_PasswordPlaceHolder 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3084">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3085">CEP_CommonExampleKeywords 정규식이 해당 패턴과 \*\*\*\* 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3085">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```sql
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

### <a name="keywords"></a><span data-ttu-id="eee87-3086">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3086">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="eee87-3087">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="eee87-3087">CEP_GlobalFilter</span></span>

- <span data-ttu-id="eee87-3088">일부 암호</span><span class="sxs-lookup"><span data-stu-id="eee87-3088">some-password</span></span>
- <span data-ttu-id="eee87-3089">somepassword</span><span class="sxs-lookup"><span data-stu-id="eee87-3089">somepassword</span></span>
- <span data-ttu-id="eee87-3090">secretPassword</span><span class="sxs-lookup"><span data-stu-id="eee87-3090">secretPassword</span></span>
- <span data-ttu-id="eee87-3091">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3091">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="eee87-3092">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="eee87-3092">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="eee87-3093">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3093">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-3094">암호나 pwd에 0-2 공백, 등호 (=), 0-2 공백 및 별표 (\*)-----------------------</span><span class="sxs-lookup"><span data-stu-id="eee87-3094">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="eee87-3095">암호나 pwd 뒤에 다음이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3095">Password or pwd followed by:</span></span>
    - <span data-ttu-id="eee87-3096">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="eee87-3096">Equal sign (=)</span></span>
    - <span data-ttu-id="eee87-3097">보다 작음 기호 (<)</span><span class="sxs-lookup"><span data-stu-id="eee87-3097">Less than symbol (<)</span></span>
    - <span data-ttu-id="eee87-3098">대문자나 소문자, digits, 별표 (\*), 하이픈 (-), 밑줄 (_) 또는 공백 문자인 1-200 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-3098">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="eee87-3099">보다 큼 기호 (>)</span><span class="sxs-lookup"><span data-stu-id="eee87-3099">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="eee87-3100">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="eee87-3100">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="eee87-3101">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3101">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="eee87-3102">극동</span><span class="sxs-lookup"><span data-stu-id="eee87-3102">contoso</span></span>
- <span data-ttu-id="eee87-3103">fabrikam</span><span class="sxs-lookup"><span data-stu-id="eee87-3103">fabrikam</span></span>
- <span data-ttu-id="eee87-3104">대양</span><span class="sxs-lookup"><span data-stu-id="eee87-3104">northwind</span></span>
- <span data-ttu-id="eee87-3105">샌드박스</span><span class="sxs-lookup"><span data-stu-id="eee87-3105">sandbox</span></span>
- <span data-ttu-id="eee87-3106">용 onebox</span><span class="sxs-lookup"><span data-stu-id="eee87-3106">onebox</span></span>
- <span data-ttu-id="eee87-3107">로컬</span><span class="sxs-lookup"><span data-stu-id="eee87-3107">localhost</span></span>
- <span data-ttu-id="eee87-3108">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="eee87-3108">127.0.0.1</span></span>
- <span data-ttu-id="eee87-3109">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3109">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-3110">ccw</span><span class="sxs-lookup"><span data-stu-id="eee87-3110">com</span></span>
- <span data-ttu-id="eee87-3111">s-int</span><span class="sxs-lookup"><span data-stu-id="eee87-3111">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="eee87-3112">투자</span><span class="sxs-lookup"><span data-stu-id="eee87-3112">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="eee87-3113">스웨덴 국가 ID</span><span class="sxs-lookup"><span data-stu-id="eee87-3113">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3114">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3114">Format</span></span>

<span data-ttu-id="eee87-3115">10 또는 12자리 숫자와 선택적 구분 기호</span><span class="sxs-lookup"><span data-stu-id="eee87-3115">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3116">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3116">Pattern</span></span>

<span data-ttu-id="eee87-3117">10 또는 12자리 숫자와 선택적 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="eee87-3117">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="eee87-3118">2-4자리 숫자(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="eee87-3118">2-4 digits (optional)</span></span> 
- <span data-ttu-id="eee87-3119">YYMMDD 날짜 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3119">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="eee87-3120">구분 기호 "-" 또는 "+"(선택 사항) 및</span><span class="sxs-lookup"><span data-stu-id="eee87-3120">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="eee87-3121">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3121">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3122">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3122">Checksum</span></span>

<span data-ttu-id="eee87-3123">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3123">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3124">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3124">Definition</span></span>

<span data-ttu-id="eee87-3125">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3125">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3126">Func_swedish_national_identifier 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3126">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3127">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3127">The checksum passes.</span></span>

```xml
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3128">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3128">Keywords</span></span>

<span data-ttu-id="eee87-3129">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3129">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="eee87-3130">스웨덴 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3130">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3131">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3131">Format</span></span>

<span data-ttu-id="eee87-3132">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3132">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3133">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3133">Pattern</span></span>

<span data-ttu-id="eee87-3134">8자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3134">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3135">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3135">Checksum</span></span>

<span data-ttu-id="eee87-3136">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3136">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3137">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3137">Definition</span></span>

<span data-ttu-id="eee87-3138">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3139">Regex_sweden_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3139">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3140">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3140">One of the following is true:</span></span>
    - <span data-ttu-id="eee87-3141">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3141">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="eee87-3142">Keyword_sweden_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3142">A keyword from Keyword_sweden_passport is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3143">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3143">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="eee87-3144">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-3144">Keyword_sweden_passport</span></span>

- <span data-ttu-id="eee87-3145">visa requirements</span><span class="sxs-lookup"><span data-stu-id="eee87-3145">visa requirements</span></span> 
- <span data-ttu-id="eee87-3146">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="eee87-3146">Alien Registration Card</span></span> 
- <span data-ttu-id="eee87-3147">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="eee87-3147">Schengen visas</span></span> 
- <span data-ttu-id="eee87-3148">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="eee87-3148">Schengen visa</span></span> 
- <span data-ttu-id="eee87-3149">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="eee87-3149">Visa Processing</span></span> 
- <span data-ttu-id="eee87-3150">Visa Type</span><span class="sxs-lookup"><span data-stu-id="eee87-3150">Visa Type</span></span> 
- <span data-ttu-id="eee87-3151">Single Entry</span><span class="sxs-lookup"><span data-stu-id="eee87-3151">Single Entry</span></span> 
- <span data-ttu-id="eee87-3152">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="eee87-3152">Multiple Entry</span></span> 
- <span data-ttu-id="eee87-3153">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="eee87-3153">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="eee87-3154">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-3154">Keyword_passport</span></span>

- <span data-ttu-id="eee87-3155">Passport Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3155">Passport Number</span></span> 
- <span data-ttu-id="eee87-3156">Passport No</span><span class="sxs-lookup"><span data-stu-id="eee87-3156">Passport No</span></span> 
- <span data-ttu-id="eee87-3157">Passport #</span><span class="sxs-lookup"><span data-stu-id="eee87-3157">Passport #</span></span> 
- <span data-ttu-id="eee87-3158">여권 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3158">Passport#</span></span> 
- <span data-ttu-id="eee87-3159">PassportID</span><span class="sxs-lookup"><span data-stu-id="eee87-3159">PassportID</span></span> 
- <span data-ttu-id="eee87-3160">Passportno</span><span class="sxs-lookup"><span data-stu-id="eee87-3160">Passportno</span></span> 
- <span data-ttu-id="eee87-3161">passportnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-3161">passportnumber</span></span> 
- <span data-ttu-id="eee87-3162">パスポート</span><span class="sxs-lookup"><span data-stu-id="eee87-3162">パスポート</span></span> 
- <span data-ttu-id="eee87-3163">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="eee87-3163">パスポート番号</span></span> 
- <span data-ttu-id="eee87-3164">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="eee87-3164">パスポートのNum</span></span> 
- <span data-ttu-id="eee87-3165">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="eee87-3165">パスポート＃</span></span> 
- <span data-ttu-id="eee87-3166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="eee87-3166">Numéro de passeport</span></span> 
- <span data-ttu-id="eee87-3167">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="eee87-3167">Passeport n °</span></span> 
- <span data-ttu-id="eee87-3168">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="eee87-3168">Passeport Non</span></span> 
- <span data-ttu-id="eee87-3169">Passeport #</span><span class="sxs-lookup"><span data-stu-id="eee87-3169">Passeport #</span></span> 
- <span data-ttu-id="eee87-3170">포트 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3170">Passeport#</span></span> 
- <span data-ttu-id="eee87-3171">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="eee87-3171">PasseportNon</span></span> 
- <span data-ttu-id="eee87-3172">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="eee87-3172">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="eee87-3173">SWIFT 코드</span><span class="sxs-lookup"><span data-stu-id="eee87-3173">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3174">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3174">Format</span></span>

<span data-ttu-id="eee87-3175">4개의 문자, 5-31개 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3175">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3176">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3176">Pattern</span></span>

<span data-ttu-id="eee87-3177">4개의 문자, 5-31개 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3177">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="eee87-3178">4문자 은행 코드(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-3178">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-3179">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-3179">An optional space</span></span> 
- <span data-ttu-id="eee87-3180">4-28개 문자 또는 숫자[BBAN(기본 은행 계좌 번호)]</span><span class="sxs-lookup"><span data-stu-id="eee87-3180">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="eee87-3181">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="eee87-3181">An optional space</span></span> 
- <span data-ttu-id="eee87-3182">1-3개 문자 또는 숫자(BBAN의 나머지)</span><span class="sxs-lookup"><span data-stu-id="eee87-3182">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3183">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3183">Checksum</span></span>

<span data-ttu-id="eee87-3184">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3185">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3185">Definition</span></span>

<span data-ttu-id="eee87-3186">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3186">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3187">Regex_swift 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3187">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3188">Keyword_swift의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3188">A keyword from Keyword_swift is found.</span></span>

```xml
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3189">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3189">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="eee87-3190">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="eee87-3190">Keyword_swift</span></span>

- <span data-ttu-id="eee87-3191">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="eee87-3191">international organization for standardization 9362</span></span> 
- <span data-ttu-id="eee87-3192">iso 9362</span><span class="sxs-lookup"><span data-stu-id="eee87-3192">iso 9362</span></span> 
- <span data-ttu-id="eee87-3193">iso9362</span><span class="sxs-lookup"><span data-stu-id="eee87-3193">iso9362</span></span> 
- <span data-ttu-id="eee87-3194">swift\#</span><span class="sxs-lookup"><span data-stu-id="eee87-3194">swift\#</span></span> 
- <span data-ttu-id="eee87-3195">swiftcode</span><span class="sxs-lookup"><span data-stu-id="eee87-3195">swiftcode</span></span> 
- <span data-ttu-id="eee87-3196">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-3196">swiftnumber</span></span> 
- <span data-ttu-id="eee87-3197">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-3197">swiftroutingnumber</span></span> 
- <span data-ttu-id="eee87-3198">swift code</span><span class="sxs-lookup"><span data-stu-id="eee87-3198">swift code</span></span> 
- <span data-ttu-id="eee87-3199">swift number #</span><span class="sxs-lookup"><span data-stu-id="eee87-3199">swift number #</span></span> 
- <span data-ttu-id="eee87-3200">swift routing number</span><span class="sxs-lookup"><span data-stu-id="eee87-3200">swift routing number</span></span> 
- <span data-ttu-id="eee87-3201">bic number</span><span class="sxs-lookup"><span data-stu-id="eee87-3201">bic number</span></span> 
- <span data-ttu-id="eee87-3202">bic code</span><span class="sxs-lookup"><span data-stu-id="eee87-3202">bic code</span></span> 
- <span data-ttu-id="eee87-3203">bic\#</span><span class="sxs-lookup"><span data-stu-id="eee87-3203">bic \#</span></span> 
- <span data-ttu-id="eee87-3204">bic\#</span><span class="sxs-lookup"><span data-stu-id="eee87-3204">bic\#</span></span> 
- <span data-ttu-id="eee87-3205">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="eee87-3205">bank identifier code</span></span> 
- <span data-ttu-id="eee87-3206">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="eee87-3206">標準化9362</span></span> 
- <span data-ttu-id="eee87-3207">迅速＃</span><span class="sxs-lookup"><span data-stu-id="eee87-3207">迅速＃</span></span> 
- <span data-ttu-id="eee87-3208">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="eee87-3208">SWIFTコード</span></span> 
- <span data-ttu-id="eee87-3209">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="eee87-3209">SWIFT番号</span></span> 
- <span data-ttu-id="eee87-3210">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="eee87-3210">迅速なルーティング番号</span></span> 
- <span data-ttu-id="eee87-3211">BIC番号</span><span class="sxs-lookup"><span data-stu-id="eee87-3211">BIC番号</span></span> 
- <span data-ttu-id="eee87-3212">BICコード</span><span class="sxs-lookup"><span data-stu-id="eee87-3212">BICコード</span></span> 
- <span data-ttu-id="eee87-3213">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="eee87-3213">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="eee87-3214">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="eee87-3214">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="eee87-3215">rapide\#</span><span class="sxs-lookup"><span data-stu-id="eee87-3215">rapide \#</span></span> 
- <span data-ttu-id="eee87-3216">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="eee87-3216">code SWIFT</span></span> 
- <span data-ttu-id="eee87-3217">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="eee87-3217">le numéro de swift</span></span> 
- <span data-ttu-id="eee87-3218">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="eee87-3218">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="eee87-3219">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="eee87-3219">le numéro BIC</span></span> 
- <span data-ttu-id="eee87-3220">\#BIC</span><span class="sxs-lookup"><span data-stu-id="eee87-3220">\# BIC</span></span> 
- <span data-ttu-id="eee87-3221">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="eee87-3221">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="eee87-3222">대만 국가 ID</span><span class="sxs-lookup"><span data-stu-id="eee87-3222">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3223">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3223">Format</span></span>

<span data-ttu-id="eee87-3224">1개의 문자, 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3224">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3225">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3225">Pattern</span></span>

<span data-ttu-id="eee87-3226">1개의 문자, 9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3226">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="eee87-3227">1개 문자(영문, 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-3227">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="eee87-3228">숫자 "1" 또는 "2"</span><span class="sxs-lookup"><span data-stu-id="eee87-3228">The digit "1" or "2"</span></span> 
- <span data-ttu-id="eee87-3229">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3229">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3230">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3230">Checksum</span></span>

<span data-ttu-id="eee87-3231">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3231">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3232">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3232">Definition</span></span>

<span data-ttu-id="eee87-3233">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3233">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3234">Func_taiwanese_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3234">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3235">Keyword_taiwanese_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3235">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="eee87-3236">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3236">The checksum passes.</span></span>

```xml
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3237">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3237">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="eee87-3238">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="eee87-3238">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="eee87-3239">身份證字號</span><span class="sxs-lookup"><span data-stu-id="eee87-3239">身份證字號</span></span> 
- <span data-ttu-id="eee87-3240">身份證</span><span class="sxs-lookup"><span data-stu-id="eee87-3240">身份證</span></span> 
- <span data-ttu-id="eee87-3241">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="eee87-3241">身份證號碼</span></span> 
- <span data-ttu-id="eee87-3242">身份證號</span><span class="sxs-lookup"><span data-stu-id="eee87-3242">身份證號</span></span> 
- <span data-ttu-id="eee87-3243">身分證字號</span><span class="sxs-lookup"><span data-stu-id="eee87-3243">身分證字號</span></span> 
- <span data-ttu-id="eee87-3244">身分證</span><span class="sxs-lookup"><span data-stu-id="eee87-3244">身分證</span></span> 
- <span data-ttu-id="eee87-3245">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="eee87-3245">身分證號碼</span></span> 
- <span data-ttu-id="eee87-3246">身份證號</span><span class="sxs-lookup"><span data-stu-id="eee87-3246">身份證號</span></span> 
- <span data-ttu-id="eee87-3247">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="eee87-3247">身分證統一編號</span></span> 
- <span data-ttu-id="eee87-3248">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="eee87-3248">國民身分證統一編號</span></span> 
- <span data-ttu-id="eee87-3249">簽名</span><span class="sxs-lookup"><span data-stu-id="eee87-3249">簽名</span></span> 
- <span data-ttu-id="eee87-3250">蓋章</span><span class="sxs-lookup"><span data-stu-id="eee87-3250">蓋章</span></span> 
- <span data-ttu-id="eee87-3251">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="eee87-3251">簽名或蓋章</span></span> 
- <span data-ttu-id="eee87-3252">簽章</span><span class="sxs-lookup"><span data-stu-id="eee87-3252">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="eee87-3253">	대만 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3253">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3254">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3254">Format</span></span>

- <span data-ttu-id="eee87-3255">생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3255">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="eee87-3256">비-생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3256">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3257">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3257">Pattern</span></span>
<span data-ttu-id="eee87-3258">생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="eee87-3258">Biometric passport number:</span></span>
- <span data-ttu-id="eee87-3259">숫자 "3" </span><span class="sxs-lookup"><span data-stu-id="eee87-3259">The digit "3"</span></span> 
- <span data-ttu-id="eee87-3260">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3260">Eight digits</span></span>

<span data-ttu-id="eee87-3261">비-생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="eee87-3261">Non-biometric passport number:</span></span>
- <span data-ttu-id="eee87-3262">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3262">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3263">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3263">Checksum</span></span>

<span data-ttu-id="eee87-3264">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3264">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3265">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3265">Definition</span></span>

<span data-ttu-id="eee87-3266">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3266">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3267">정규식 Regex_taiwan_passport 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3267">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3268">Keyword_taiwan_passport에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3268">A keyword from Keyword_taiwan_passport is found.</span></span>

```xml
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3269">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3269">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="eee87-3270">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-3270">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="eee87-3271">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="eee87-3271">ROC passport number</span></span> 
- <span data-ttu-id="eee87-3272">Passport number</span><span class="sxs-lookup"><span data-stu-id="eee87-3272">Passport number</span></span> 
- <span data-ttu-id="eee87-3273">Passport no</span><span class="sxs-lookup"><span data-stu-id="eee87-3273">Passport no</span></span> 
- <span data-ttu-id="eee87-3274">Passport Num</span><span class="sxs-lookup"><span data-stu-id="eee87-3274">Passport Num</span></span> 
- <span data-ttu-id="eee87-3275">Passport #</span><span class="sxs-lookup"><span data-stu-id="eee87-3275">Passport #</span></span> 
- <span data-ttu-id="eee87-3276">护照</span><span class="sxs-lookup"><span data-stu-id="eee87-3276">护照</span></span> 
- <span data-ttu-id="eee87-3277">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="eee87-3277">中華民國護照</span></span> 
- <span data-ttu-id="eee87-3278">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="eee87-3278">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="eee87-3279">대만 거주 인증(ARC/TARC) 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3279">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3280">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3280">Format</span></span>

<span data-ttu-id="eee87-3281">10개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3281">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3282">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3282">Pattern</span></span>

<span data-ttu-id="eee87-3283">10개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3283">10 letters and digits:</span></span>
- <span data-ttu-id="eee87-3284">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-3284">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="eee87-3285">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3285">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3286">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3286">Checksum</span></span>

<span data-ttu-id="eee87-3287">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3287">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3288">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3288">Definition</span></span>

<span data-ttu-id="eee87-3289">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3289">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3290">정규식 Regex_taiwan_resident_certificate 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3290">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3291">Keyword_taiwan_resident_certificate에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3291">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```xml
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3292">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3292">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="eee87-3293">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="eee87-3293">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="eee87-3294">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="eee87-3294">Resident Certificate</span></span> 
- <span data-ttu-id="eee87-3295">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="eee87-3295">Resident Cert</span></span> 
- <span data-ttu-id="eee87-3296">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="eee87-3296">Resident Cert.</span></span> 
- <span data-ttu-id="eee87-3297">Identification card</span><span class="sxs-lookup"><span data-stu-id="eee87-3297">Identification card</span></span> 
- <span data-ttu-id="eee87-3298">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="eee87-3298">Alien Resident Certificate</span></span> 
- <span data-ttu-id="eee87-3299">화살표</span><span class="sxs-lookup"><span data-stu-id="eee87-3299">ARC</span></span> 
- <span data-ttu-id="eee87-3300">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="eee87-3300">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="eee87-3301">TARC</span><span class="sxs-lookup"><span data-stu-id="eee87-3301">TARC</span></span> 
- <span data-ttu-id="eee87-3302">居留證</span><span class="sxs-lookup"><span data-stu-id="eee87-3302">居留證</span></span> 
- <span data-ttu-id="eee87-3303">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="eee87-3303">外僑居留證</span></span> 
- <span data-ttu-id="eee87-3304">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="eee87-3304">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="eee87-3305">태국어 인구 식별 코드</span><span class="sxs-lookup"><span data-stu-id="eee87-3305">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3306">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3306">Format</span></span>

<span data-ttu-id="eee87-3307">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3307">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3308">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3308">Pattern</span></span>

<span data-ttu-id="eee87-3309">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3309">13 digits:</span></span>
- <span data-ttu-id="eee87-3310">첫 번째 숫자가 0 또는 9가 아님</span><span class="sxs-lookup"><span data-stu-id="eee87-3310">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="eee87-3311">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3311">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3312">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3312">Checksum</span></span>

<span data-ttu-id="eee87-3313">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3314">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3314">Definition</span></span>

<span data-ttu-id="eee87-3315">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3315">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3316">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3316">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3317">Keyword_Thai_Citizen_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3317">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="eee87-3318">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3318">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3319">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3319">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3320">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3320">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="eee87-3321">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="eee87-3321">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="eee87-3322">ID Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3322">ID Number</span></span>
- <span data-ttu-id="eee87-3323">Id 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3323">Identification Number</span></span>
- <span data-ttu-id="eee87-3324">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="eee87-3324">บัตรประชาชน</span></span>
- <span data-ttu-id="eee87-3325">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="eee87-3325">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="eee87-3326">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="eee87-3326">บัตรประชาชน</span></span>
- <span data-ttu-id="eee87-3327">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="eee87-3327">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="eee87-3328">터키어 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3328">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3329">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3329">Format</span></span>

<span data-ttu-id="eee87-3330">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3330">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3331">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3331">Pattern</span></span>

<span data-ttu-id="eee87-3332">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3332">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3333">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3333">Checksum</span></span>

<span data-ttu-id="eee87-3334">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3335">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3335">Definition</span></span>

<span data-ttu-id="eee87-3336">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3337">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3337">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3338">Keyword_Turkish_National_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3338">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="eee87-3339">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3340">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3340">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3341">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3341">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="eee87-3342">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="eee87-3342">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="eee87-3343">TC Kimlik 아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3343">TC Kimlik No</span></span>
- <span data-ttu-id="eee87-3344">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="eee87-3344">TC Kimlik numarası</span></span>
- <span data-ttu-id="eee87-3345">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="eee87-3345">Vatandaşlık numarası</span></span>
- <span data-ttu-id="eee87-3346">Vatandaşlık 아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3346">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="eee87-p141">영국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3349">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3349">Format</span></span>

<span data-ttu-id="eee87-3350">지정된 형식의 18개 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="eee87-3350">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3351">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3351">Pattern</span></span>

<span data-ttu-id="eee87-3352">18개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3352">18 letters and digits:</span></span>
- <span data-ttu-id="eee87-3353">5개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="eee87-3353">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="eee87-3354">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3354">One digit</span></span> 
- <span data-ttu-id="eee87-3355">생년월일에 대한 DDMMY 날짜 형식의 5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3355">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="eee87-3356">2개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="eee87-3356">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="eee87-3357">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3357">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3358">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3358">Checksum</span></span>

<span data-ttu-id="eee87-3359">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3359">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3360">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3360">Definition</span></span>

<span data-ttu-id="eee87-3361">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3362">Func_uk_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3362">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3363">Keyword_uk_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3363">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="eee87-3364">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3364">The checksum passes.</span></span>

```xml
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3365">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3365">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="eee87-3366">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="eee87-3366">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="eee87-3367">DVLA</span><span class="sxs-lookup"><span data-stu-id="eee87-3367">DVLA</span></span> 
- <span data-ttu-id="eee87-3368">light vans</span><span class="sxs-lookup"><span data-stu-id="eee87-3368">light vans</span></span> 
- <span data-ttu-id="eee87-3369">quadbikes</span><span class="sxs-lookup"><span data-stu-id="eee87-3369">quadbikes</span></span> 
- <span data-ttu-id="eee87-3370">motor cars</span><span class="sxs-lookup"><span data-stu-id="eee87-3370">motor cars</span></span> 
- <span data-ttu-id="eee87-3371">125cc</span><span class="sxs-lookup"><span data-stu-id="eee87-3371">125cc</span></span> 
- <span data-ttu-id="eee87-3372">sidecar</span><span class="sxs-lookup"><span data-stu-id="eee87-3372">sidecar</span></span> 
- <span data-ttu-id="eee87-3373">tricycles</span><span class="sxs-lookup"><span data-stu-id="eee87-3373">tricycles</span></span> 
- <span data-ttu-id="eee87-3374">motorcycles</span><span class="sxs-lookup"><span data-stu-id="eee87-3374">motorcycles</span></span> 
- <span data-ttu-id="eee87-3375">photocard licence</span><span class="sxs-lookup"><span data-stu-id="eee87-3375">photocard licence</span></span> 
- <span data-ttu-id="eee87-3376">learner drivers</span><span class="sxs-lookup"><span data-stu-id="eee87-3376">learner drivers</span></span> 
- <span data-ttu-id="eee87-3377">licence holder</span><span class="sxs-lookup"><span data-stu-id="eee87-3377">licence holder</span></span> 
- <span data-ttu-id="eee87-3378">licence holders</span><span class="sxs-lookup"><span data-stu-id="eee87-3378">licence holders</span></span> 
- <span data-ttu-id="eee87-3379">driving licences</span><span class="sxs-lookup"><span data-stu-id="eee87-3379">driving licences</span></span> 
- <span data-ttu-id="eee87-3380">driving licence</span><span class="sxs-lookup"><span data-stu-id="eee87-3380">driving licence</span></span> 
- <span data-ttu-id="eee87-3381">dual control car</span><span class="sxs-lookup"><span data-stu-id="eee87-3381">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="eee87-p142">영국 선거 롤 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3384">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3384">Format</span></span>

<span data-ttu-id="eee87-3385">2개의 문자, 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3385">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3386">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3386">Pattern</span></span>

<span data-ttu-id="eee87-3387">2개의 문자(대/소문자 구분 안 함)와 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3387">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3388">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3388">Checksum</span></span>

<span data-ttu-id="eee87-3389">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3389">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3390">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3390">Definition</span></span>

<span data-ttu-id="eee87-3391">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3391">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3392">Regex_uk_electoral 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3392">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3393">Keyword_uk_electoral의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3393">A keyword from Keyword_uk_electoral is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3394">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3394">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="eee87-3395">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="eee87-3395">Keyword_uk_electoral</span></span>

- <span data-ttu-id="eee87-3396">council nomination</span><span class="sxs-lookup"><span data-stu-id="eee87-3396">council nomination</span></span> 
- <span data-ttu-id="eee87-3397">nomination form</span><span class="sxs-lookup"><span data-stu-id="eee87-3397">nomination form</span></span> 
- <span data-ttu-id="eee87-3398">electoral register</span><span class="sxs-lookup"><span data-stu-id="eee87-3398">electoral register</span></span> 
- <span data-ttu-id="eee87-3399">electoral roll</span><span class="sxs-lookup"><span data-stu-id="eee87-3399">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="eee87-p143">영국 국립 보건 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3402">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3402">Format</span></span>

<span data-ttu-id="eee87-3403">공백으로 구분된 10-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3403">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3404">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3404">Pattern</span></span>

<span data-ttu-id="eee87-3405">10-17자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="eee87-3405">10-17 digits:</span></span>
- <span data-ttu-id="eee87-3406">3 또는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3406">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="eee87-3407">공백</span><span class="sxs-lookup"><span data-stu-id="eee87-3407">A space</span></span> 
- <span data-ttu-id="eee87-3408">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3408">Three digits</span></span> 
- <span data-ttu-id="eee87-3409">공백</span><span class="sxs-lookup"><span data-stu-id="eee87-3409">A space</span></span> 
- <span data-ttu-id="eee87-3410">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3410">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3411">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3411">Checksum</span></span>

<span data-ttu-id="eee87-3412">예</span><span class="sxs-lookup"><span data-stu-id="eee87-3412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3413">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3413">Definition</span></span>

<span data-ttu-id="eee87-3414">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3415">Func_uk_nhs_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3415">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3416">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3416">One of the following is true:</span></span>
    - <span data-ttu-id="eee87-3417">Keyword_uk_nhs_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3417">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="eee87-3418">Keyword_uk_nhs_number1의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3418">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="eee87-3419">Keyword_uk_nhs_number_dob의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3419">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="eee87-3420">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3420">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3421">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3421">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="eee87-3422">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="eee87-3422">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="eee87-3423">국립 보건 서비스</span><span class="sxs-lookup"><span data-stu-id="eee87-3423">national health service</span></span> 
- <span data-ttu-id="eee87-3424">nhs</span><span class="sxs-lookup"><span data-stu-id="eee87-3424">nhs</span></span> 
- <span data-ttu-id="eee87-3425">health services authority</span><span class="sxs-lookup"><span data-stu-id="eee87-3425">health services authority</span></span> 
- <span data-ttu-id="eee87-3426">health authority</span><span class="sxs-lookup"><span data-stu-id="eee87-3426">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="eee87-3427">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="eee87-3427">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="eee87-3428">patient id</span><span class="sxs-lookup"><span data-stu-id="eee87-3428">patient id</span></span> 
- <span data-ttu-id="eee87-3429">patient identification</span><span class="sxs-lookup"><span data-stu-id="eee87-3429">patient identification</span></span> 
- <span data-ttu-id="eee87-3430">patient no</span><span class="sxs-lookup"><span data-stu-id="eee87-3430">patient no</span></span> 
- <span data-ttu-id="eee87-3431">patient number</span><span class="sxs-lookup"><span data-stu-id="eee87-3431">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="eee87-3432">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="eee87-3432">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="eee87-3433">G</span><span class="sxs-lookup"><span data-stu-id="eee87-3433">GP</span></span> 
- <span data-ttu-id="eee87-3434">DOB</span><span class="sxs-lookup"><span data-stu-id="eee87-3434">DOB</span></span> 
- <span data-ttu-id="eee87-3435">D. O. B</span><span class="sxs-lookup"><span data-stu-id="eee87-3435">D.O.B</span></span> 
- <span data-ttu-id="eee87-3436">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="eee87-3436">Date of Birth</span></span> 
- <span data-ttu-id="eee87-3437">Birth Date</span><span class="sxs-lookup"><span data-stu-id="eee87-3437">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="eee87-p144">영국 NINO(국민 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="eee87-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3440">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3440">Format</span></span>

<span data-ttu-id="eee87-3441">공백 또는 대시로 구분 된 7 자 또는 9 자</span><span class="sxs-lookup"><span data-stu-id="eee87-3441">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3442">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3442">Pattern</span></span>

<span data-ttu-id="eee87-3443">다음과 같은 두 가지 패턴을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3443">Two possible patterns:</span></span>

- <span data-ttu-id="eee87-3444">두 문자 (유효한 NINOs이 접두사의 특정 문자만 사용 하며이 패턴의 유효성 검사는 대/소문자를 구분 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="eee87-3444">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="eee87-3445">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3445">Six digits</span></span>
- <span data-ttu-id="eee87-3446">' A ', ' B ', ' C ' 또는 ' d ' (접두사와 마찬가지로 접미사에서는 특정 문자만 허용 되며 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="eee87-3446">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="eee87-3447">또는</span><span class="sxs-lookup"><span data-stu-id="eee87-3447">OR</span></span>

- <span data-ttu-id="eee87-3448">2 개 문자</span><span class="sxs-lookup"><span data-stu-id="eee87-3448">Two letters</span></span>
- <span data-ttu-id="eee87-3449">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="eee87-3449">A space or dash</span></span>
- <span data-ttu-id="eee87-3450">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3450">Two digits</span></span>
- <span data-ttu-id="eee87-3451">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="eee87-3451">A space or dash</span></span>
- <span data-ttu-id="eee87-3452">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3452">Two digits</span></span>
- <span data-ttu-id="eee87-3453">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="eee87-3453">A space or dash</span></span>
- <span data-ttu-id="eee87-3454">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3454">Two digits</span></span>
- <span data-ttu-id="eee87-3455">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="eee87-3455">A space or dash</span></span>
- <span data-ttu-id="eee87-3456">' A ', ' B ', ' C ' 또는 ' d ' 중 하나</span><span class="sxs-lookup"><span data-stu-id="eee87-3456">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3457">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3457">Checksum</span></span>

<span data-ttu-id="eee87-3458">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3458">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3459">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3459">Definition</span></span>

<span data-ttu-id="eee87-3460">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3461">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3461">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3462">Keyword_uk_nino의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3462">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="eee87-3463">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3464">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3464">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3465">Keyword_uk_nino의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3465">No keyword from Keyword_uk_nino is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3466">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3466">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="eee87-3467">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="eee87-3467">Keyword_uk_nino</span></span>

- <span data-ttu-id="eee87-3468">national insurance number</span><span class="sxs-lookup"><span data-stu-id="eee87-3468">national insurance number</span></span> 
- <span data-ttu-id="eee87-3469">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="eee87-3469">national insurance contributions</span></span> 
- <span data-ttu-id="eee87-3470">protection act</span><span class="sxs-lookup"><span data-stu-id="eee87-3470">protection act</span></span> 
- <span data-ttu-id="eee87-3471">소유권</span><span class="sxs-lookup"><span data-stu-id="eee87-3471">insurance</span></span> 
- <span data-ttu-id="eee87-3472">social security number</span><span class="sxs-lookup"><span data-stu-id="eee87-3472">social security number</span></span> 
- <span data-ttu-id="eee87-3473">insurance application</span><span class="sxs-lookup"><span data-stu-id="eee87-3473">insurance application</span></span> 
- <span data-ttu-id="eee87-3474">medical application</span><span class="sxs-lookup"><span data-stu-id="eee87-3474">medical application</span></span> 
- <span data-ttu-id="eee87-3475">social insurance</span><span class="sxs-lookup"><span data-stu-id="eee87-3475">social insurance</span></span> 
- <span data-ttu-id="eee87-3476">medical attention</span><span class="sxs-lookup"><span data-stu-id="eee87-3476">medical attention</span></span> 
- <span data-ttu-id="eee87-3477">social security</span><span class="sxs-lookup"><span data-stu-id="eee87-3477">social security</span></span> 
- <span data-ttu-id="eee87-3478">great britain</span><span class="sxs-lookup"><span data-stu-id="eee87-3478">great britain</span></span> 
- <span data-ttu-id="eee87-3479">소유권</span><span class="sxs-lookup"><span data-stu-id="eee87-3479">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="eee87-p145">미국/영국 여권 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3482">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3482">Format</span></span>

<span data-ttu-id="eee87-3483">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3483">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3484">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3484">Pattern</span></span>

<span data-ttu-id="eee87-3485">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3485">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3486">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3486">Checksum</span></span>

<span data-ttu-id="eee87-3487">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3487">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3488">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3488">Definition</span></span>

<span data-ttu-id="eee87-3489">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3489">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3490">Func_usa_uk_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3490">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3491">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3491">A keyword from Keyword_passport is found.</span></span>

```xml
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3492">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3492">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="eee87-3493">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="eee87-3493">Keyword_passport</span></span>

- <span data-ttu-id="eee87-3494">Passport Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3494">Passport Number</span></span> 
- <span data-ttu-id="eee87-3495">Passport No</span><span class="sxs-lookup"><span data-stu-id="eee87-3495">Passport No</span></span> 
- <span data-ttu-id="eee87-3496">Passport #</span><span class="sxs-lookup"><span data-stu-id="eee87-3496">Passport #</span></span> 
- <span data-ttu-id="eee87-3497">여권 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3497">Passport#</span></span> 
- <span data-ttu-id="eee87-3498">PassportID</span><span class="sxs-lookup"><span data-stu-id="eee87-3498">PassportID</span></span> 
- <span data-ttu-id="eee87-3499">Passportno</span><span class="sxs-lookup"><span data-stu-id="eee87-3499">Passportno</span></span> 
- <span data-ttu-id="eee87-3500">passportnumber</span><span class="sxs-lookup"><span data-stu-id="eee87-3500">passportnumber</span></span> 
- <span data-ttu-id="eee87-3501">パスポート</span><span class="sxs-lookup"><span data-stu-id="eee87-3501">パスポート</span></span> 
- <span data-ttu-id="eee87-3502">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="eee87-3502">パスポート番号</span></span> 
- <span data-ttu-id="eee87-3503">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="eee87-3503">パスポートのNum</span></span> 
- <span data-ttu-id="eee87-3504">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="eee87-3504">パスポート＃</span></span> 
- <span data-ttu-id="eee87-3505">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="eee87-3505">Numéro de passeport</span></span> 
- <span data-ttu-id="eee87-3506">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="eee87-3506">Passeport n °</span></span> 
- <span data-ttu-id="eee87-3507">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="eee87-3507">Passeport Non</span></span> 
- <span data-ttu-id="eee87-3508">Passeport #</span><span class="sxs-lookup"><span data-stu-id="eee87-3508">Passeport #</span></span> 
- <span data-ttu-id="eee87-3509">포트 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3509">Passeport#</span></span> 
- <span data-ttu-id="eee87-3510">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="eee87-3510">PasseportNon</span></span> 
- <span data-ttu-id="eee87-3511">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="eee87-3511">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="eee87-3512">미국 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3512">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3513">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3513">Format</span></span>

<span data-ttu-id="eee87-3514">8-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3514">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3515">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3515">Pattern</span></span>

<span data-ttu-id="eee87-3516">8-17자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3516">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3517">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3517">Checksum</span></span>

<span data-ttu-id="eee87-3518">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3518">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3519">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3519">Definition</span></span>

<span data-ttu-id="eee87-3520">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3521">Regex_usa_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3521">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3522">Keyword_usa_Bank_Account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3522">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```xml
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3523">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3523">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="eee87-3524">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="eee87-3524">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="eee87-3525">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3525">Checking Account Number</span></span> 
- <span data-ttu-id="eee87-3526">Checking Account</span><span class="sxs-lookup"><span data-stu-id="eee87-3526">Checking Account</span></span> 
- <span data-ttu-id="eee87-3527">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="eee87-3527">Checking Account #</span></span> 
- <span data-ttu-id="eee87-3528">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3528">Checking Acct Number</span></span> 
- <span data-ttu-id="eee87-3529">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="eee87-3529">Checking Acct #</span></span> 
- <span data-ttu-id="eee87-3530">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="eee87-3530">Checking Acct No.</span></span> 
- <span data-ttu-id="eee87-3531">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="eee87-3531">Checking Account No.</span></span> 
- <span data-ttu-id="eee87-3532">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3532">Bank Account Number</span></span> 
- <span data-ttu-id="eee87-3533">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="eee87-3533">Bank Account #</span></span> 
- <span data-ttu-id="eee87-3534">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3534">Bank Acct Number</span></span> 
- <span data-ttu-id="eee87-3535">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="eee87-3535">Bank Acct #</span></span> 
- <span data-ttu-id="eee87-3536">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="eee87-3536">Bank Acct No.</span></span> 
- <span data-ttu-id="eee87-3537">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="eee87-3537">Bank Account No.</span></span> 
- <span data-ttu-id="eee87-3538">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3538">Savings Account Number</span></span> 
- <span data-ttu-id="eee87-3539">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="eee87-3539">Savings Account.</span></span> 
- <span data-ttu-id="eee87-3540">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="eee87-3540">Savings Account #</span></span> 
- <span data-ttu-id="eee87-3541">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3541">Savings Acct Number</span></span> 
- <span data-ttu-id="eee87-3542">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="eee87-3542">Savings Acct #</span></span> 
- <span data-ttu-id="eee87-3543">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="eee87-3543">Savings Acct No.</span></span> 
- <span data-ttu-id="eee87-3544">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="eee87-3544">Savings Account No.</span></span> 
- <span data-ttu-id="eee87-3545">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3545">Debit Account Number</span></span> 
- <span data-ttu-id="eee87-3546">Debit Account</span><span class="sxs-lookup"><span data-stu-id="eee87-3546">Debit Account</span></span> 
- <span data-ttu-id="eee87-3547">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="eee87-3547">Debit Account #</span></span> 
- <span data-ttu-id="eee87-3548">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="eee87-3548">Debit Acct Number</span></span> 
- <span data-ttu-id="eee87-3549">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="eee87-3549">Debit Acct #</span></span> 
- <span data-ttu-id="eee87-3550">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="eee87-3550">Debit Acct No.</span></span> 
- <span data-ttu-id="eee87-3551">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="eee87-3551">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="eee87-3552">미국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="eee87-3552">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3553">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3553">Format</span></span>

<span data-ttu-id="eee87-3554">주마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3554">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3555">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3555">Pattern</span></span>

<span data-ttu-id="eee87-3556">주마다 다릅니다(예: 뉴욕).</span><span class="sxs-lookup"><span data-stu-id="eee87-3556">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="eee87-3557">Ddd ddd ddd와 같이 9 자리 숫자는 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3557">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="eee87-3558">Ddddddddd와 같은 9 자리 숫자가 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3558">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3559">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3559">Checksum</span></span>

<span data-ttu-id="eee87-3560">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3560">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3561">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3561">Definition</span></span>

<span data-ttu-id="eee87-3562">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3562">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3563">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3563">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3564">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3564">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="eee87-3565">Keyword_us_drivers_license에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3565">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="eee87-3566">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3566">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3567">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3567">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3568">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3568">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="eee87-3569">Keyword_us_drivers_license_abbreviations의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3569">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="eee87-3570">Keyword_us_drivers_license의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3570">No keyword from Keyword_us_drivers_license is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3571">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3571">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="eee87-3572">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="eee87-3572">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="eee87-3573">DL</span><span class="sxs-lookup"><span data-stu-id="eee87-3573">DL</span></span> 
- <span data-ttu-id="eee87-3574">된다</span><span class="sxs-lookup"><span data-stu-id="eee87-3574">DLS</span></span> 
- <span data-ttu-id="eee87-3575">CDL</span><span class="sxs-lookup"><span data-stu-id="eee87-3575">CDL</span></span> 
- <span data-ttu-id="eee87-3576">CDLS</span><span class="sxs-lookup"><span data-stu-id="eee87-3576">CDLS</span></span> 
- <span data-ttu-id="eee87-3577">ID</span><span class="sxs-lookup"><span data-stu-id="eee87-3577">ID</span></span> 
- <span data-ttu-id="eee87-3578">번호가</span><span class="sxs-lookup"><span data-stu-id="eee87-3578">IDs</span></span> 
- <span data-ttu-id="eee87-3579">DL #</span><span class="sxs-lookup"><span data-stu-id="eee87-3579">DL#</span></span> 
- <span data-ttu-id="eee87-3580">된다 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3580">DLS#</span></span> 
- <span data-ttu-id="eee87-3581">CDL #</span><span class="sxs-lookup"><span data-stu-id="eee87-3581">CDL#</span></span> 
- <span data-ttu-id="eee87-3582">CDLS #</span><span class="sxs-lookup"><span data-stu-id="eee87-3582">CDLS#</span></span> 
- <span data-ttu-id="eee87-3583">I #</span><span class="sxs-lookup"><span data-stu-id="eee87-3583">ID#</span></span>
- <span data-ttu-id="eee87-3584">번호가 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3584">IDs#</span></span> 
- <span data-ttu-id="eee87-3585">ID number</span><span class="sxs-lookup"><span data-stu-id="eee87-3585">ID number</span></span> 
- <span data-ttu-id="eee87-3586">ID numbers</span><span class="sxs-lookup"><span data-stu-id="eee87-3586">ID numbers</span></span> 
- <span data-ttu-id="eee87-3587">LIC</span><span class="sxs-lookup"><span data-stu-id="eee87-3587">LIC</span></span> 
- <span data-ttu-id="eee87-3588">LIC #</span><span class="sxs-lookup"><span data-stu-id="eee87-3588">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="eee87-3589">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="eee87-3589">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="eee87-3590">DriverLic</span><span class="sxs-lookup"><span data-stu-id="eee87-3590">DriverLic</span></span> 
- <span data-ttu-id="eee87-3591">DriverLics</span><span class="sxs-lookup"><span data-stu-id="eee87-3591">DriverLics</span></span> 
- <span data-ttu-id="eee87-3592">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="eee87-3592">DriverLicense</span></span> 
- <span data-ttu-id="eee87-3593">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="eee87-3593">DriverLicenses</span></span> 
- <span data-ttu-id="eee87-3594">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-3594">Driver Lic</span></span> 
- <span data-ttu-id="eee87-3595">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-3595">Driver Lics</span></span> 
- <span data-ttu-id="eee87-3596">Driver License</span><span class="sxs-lookup"><span data-stu-id="eee87-3596">Driver License</span></span> 
- <span data-ttu-id="eee87-3597">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-3597">Driver Licenses</span></span> 
- <span data-ttu-id="eee87-3598">DriversLic</span><span class="sxs-lookup"><span data-stu-id="eee87-3598">DriversLic</span></span> 
- <span data-ttu-id="eee87-3599">DriversLics</span><span class="sxs-lookup"><span data-stu-id="eee87-3599">DriversLics</span></span> 
- <span data-ttu-id="eee87-3600">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-3600">DriversLicense</span></span> 
- <span data-ttu-id="eee87-3601">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-3601">DriversLicenses</span></span> 
- <span data-ttu-id="eee87-3602">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-3602">Drivers Lic</span></span> 
- <span data-ttu-id="eee87-3603">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-3603">Drivers Lics</span></span> 
- <span data-ttu-id="eee87-3604">Drivers License</span><span class="sxs-lookup"><span data-stu-id="eee87-3604">Drivers License</span></span> 
- <span data-ttu-id="eee87-3605">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-3605">Drivers Licenses</span></span> 
- <span data-ttu-id="eee87-3606">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-3606">Driver'Lic</span></span> 
- <span data-ttu-id="eee87-3607">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-3607">Driver'Lics</span></span> 
- <span data-ttu-id="eee87-3608">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="eee87-3608">Driver'License</span></span> 
- <span data-ttu-id="eee87-3609">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-3609">Driver'Licenses</span></span> 
- <span data-ttu-id="eee87-3610">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-3610">Driver' Lic</span></span> 
- <span data-ttu-id="eee87-3611">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-3611">Driver' Lics</span></span> 
- <span data-ttu-id="eee87-3612">Driver' License</span><span class="sxs-lookup"><span data-stu-id="eee87-3612">Driver' License</span></span> 
- <span data-ttu-id="eee87-3613">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-3613">Driver' Licenses</span></span>
- <span data-ttu-id="eee87-3614">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="eee87-3614">Driver'sLic</span></span> 
- <span data-ttu-id="eee87-3615">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="eee87-3615">Driver'sLics</span></span> 
- <span data-ttu-id="eee87-3616">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="eee87-3616">Driver'sLicense</span></span> 
- <span data-ttu-id="eee87-3617">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="eee87-3617">Driver'sLicenses</span></span> 
- <span data-ttu-id="eee87-3618">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="eee87-3618">Driver's Lic</span></span> 
- <span data-ttu-id="eee87-3619">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="eee87-3619">Driver's Lics</span></span> 
- <span data-ttu-id="eee87-3620">Driver's License</span><span class="sxs-lookup"><span data-stu-id="eee87-3620">Driver's License</span></span> 
- <span data-ttu-id="eee87-3621">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="eee87-3621">Driver's Licenses</span></span> 
- <span data-ttu-id="eee87-3622">identification number</span><span class="sxs-lookup"><span data-stu-id="eee87-3622">identification number</span></span> 
- <span data-ttu-id="eee87-3623">identification numbers</span><span class="sxs-lookup"><span data-stu-id="eee87-3623">identification numbers</span></span> 
- <span data-ttu-id="eee87-3624">identification #</span><span class="sxs-lookup"><span data-stu-id="eee87-3624">identification #</span></span> 
- <span data-ttu-id="eee87-3625">id card</span><span class="sxs-lookup"><span data-stu-id="eee87-3625">id card</span></span> 
- <span data-ttu-id="eee87-3626">id cards</span><span class="sxs-lookup"><span data-stu-id="eee87-3626">id cards</span></span> 
- <span data-ttu-id="eee87-3627">identification card</span><span class="sxs-lookup"><span data-stu-id="eee87-3627">identification card</span></span> 
- <span data-ttu-id="eee87-3628">identification cards</span><span class="sxs-lookup"><span data-stu-id="eee87-3628">identification cards</span></span> 
- <span data-ttu-id="eee87-3629">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-3629">DriverLic#</span></span> 
- <span data-ttu-id="eee87-3630">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="eee87-3630">DriverLics#</span></span> 
- <span data-ttu-id="eee87-3631">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="eee87-3631">DriverLicense#</span></span> 
- <span data-ttu-id="eee87-3632">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-3632">DriverLicenses#</span></span> 
- <span data-ttu-id="eee87-3633">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-3633">Driver Lic#</span></span> 
- <span data-ttu-id="eee87-3634">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-3634">Driver Lics#</span></span> 
- <span data-ttu-id="eee87-3635">Driver License#</span><span class="sxs-lookup"><span data-stu-id="eee87-3635">Driver License#</span></span> 
- <span data-ttu-id="eee87-3636">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-3636">Driver Licenses#</span></span> 
- <span data-ttu-id="eee87-3637">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-3637">DriversLic#</span></span> 
- <span data-ttu-id="eee87-3638">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="eee87-3638">DriversLics#</span></span> 
- <span data-ttu-id="eee87-3639">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3639">DriversLicense#</span></span> 
- <span data-ttu-id="eee87-3640">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3640">DriversLicenses#</span></span> 
- <span data-ttu-id="eee87-3641">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-3641">Drivers Lic#</span></span> 
- <span data-ttu-id="eee87-3642">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-3642">Drivers Lics#</span></span> 
- <span data-ttu-id="eee87-3643">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="eee87-3643">Drivers License#</span></span> 
- <span data-ttu-id="eee87-3644">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-3644">Drivers Licenses#</span></span> 
- <span data-ttu-id="eee87-3645">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="eee87-3645">Driver'Lic#</span></span> 
- <span data-ttu-id="eee87-3646">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="eee87-3646">Driver'Lics#</span></span> 
- <span data-ttu-id="eee87-3647">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3647">Driver'License#</span></span> 
- <span data-ttu-id="eee87-3648">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-3648">Driver'Licenses#</span></span> 
- <span data-ttu-id="eee87-3649">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-3649">Driver' Lic#</span></span> 
- <span data-ttu-id="eee87-3650">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-3650">Driver' Lics#</span></span> 
- <span data-ttu-id="eee87-3651">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="eee87-3651">Driver' License#</span></span> 
- <span data-ttu-id="eee87-3652">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-3652">Driver' Licenses#</span></span> 
- <span data-ttu-id="eee87-3653">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="eee87-3653">Driver'sLic#</span></span> 
- <span data-ttu-id="eee87-3654">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="eee87-3654">Driver'sLics#</span></span> 
- <span data-ttu-id="eee87-3655">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="eee87-3655">Driver'sLicense#</span></span> 
- <span data-ttu-id="eee87-3656">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="eee87-3656">Driver'sLicenses#</span></span> 
- <span data-ttu-id="eee87-3657">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="eee87-3657">Driver's Lic#</span></span> 
- <span data-ttu-id="eee87-3658">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="eee87-3658">Driver's Lics#</span></span> 
- <span data-ttu-id="eee87-3659">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="eee87-3659">Driver's License#</span></span> 
- <span data-ttu-id="eee87-3660">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="eee87-3660">Driver's Licenses#</span></span> 
- <span data-ttu-id="eee87-3661">id card#</span><span class="sxs-lookup"><span data-stu-id="eee87-3661">id card#</span></span> 
- <span data-ttu-id="eee87-3662">id cards#</span><span class="sxs-lookup"><span data-stu-id="eee87-3662">id cards#</span></span> 
- <span data-ttu-id="eee87-3663">identification card#</span><span class="sxs-lookup"><span data-stu-id="eee87-3663">identification card#</span></span> 
- <span data-ttu-id="eee87-3664">identification cards#</span><span class="sxs-lookup"><span data-stu-id="eee87-3664">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="eee87-3665">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="eee87-3665">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="eee87-3666">주 약어(예: "NY")</span><span class="sxs-lookup"><span data-stu-id="eee87-3666">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="eee87-3667">주 이름(예: "New York")</span><span class="sxs-lookup"><span data-stu-id="eee87-3667">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="eee87-3668">미국 ITIN(개인 납세자 번호)</span><span class="sxs-lookup"><span data-stu-id="eee87-3668">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3669">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3669">Format</span></span>

<span data-ttu-id="eee87-3670">"9"로 시작되고, "7" 또는 "8"을 4번째 숫자로 포함하고, 경우에 따라 공백이나 대시로 서식이 지정된 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3670">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3671">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3671">Pattern</span></span>

<span data-ttu-id="eee87-3672">서식이</span><span class="sxs-lookup"><span data-stu-id="eee87-3672">Formatted:</span></span>
- <span data-ttu-id="eee87-3673">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3673">The digit "9"</span></span> 
- <span data-ttu-id="eee87-3674">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3674">Two digits</span></span> 
- <span data-ttu-id="eee87-3675">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="eee87-3675">A space or dash</span></span> 
- <span data-ttu-id="eee87-3676">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="eee87-3676">A "7" or "8"</span></span> 
- <span data-ttu-id="eee87-3677">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3677">A digit</span></span> 
- <span data-ttu-id="eee87-3678">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="eee87-3678">A space, or dash</span></span> 
- <span data-ttu-id="eee87-3679">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3679">Four digits</span></span>

<span data-ttu-id="eee87-3680">서식</span><span class="sxs-lookup"><span data-stu-id="eee87-3680">Unformatted:</span></span>
- <span data-ttu-id="eee87-3681">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3681">The digit "9"</span></span> 
- <span data-ttu-id="eee87-3682">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3682">Two digits</span></span> 
- <span data-ttu-id="eee87-3683">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="eee87-3683">A "7" or "8"</span></span> 
- <span data-ttu-id="eee87-3684">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3684">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3685">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3685">Checksum</span></span>

<span data-ttu-id="eee87-3686">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3686">No</span></span>

### <a name="definition"></a><span data-ttu-id="eee87-3687">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3687">Definition</span></span>

<span data-ttu-id="eee87-3688">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3689">Func_formatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3689">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3690">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3690">At least one of the following is true:</span></span>
    - <span data-ttu-id="eee87-3691">Keyword_itin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3691">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="eee87-3692">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3692">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="eee87-3693">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3693">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="eee87-3694">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3694">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="eee87-3695">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3695">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3696">Func_unformatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3696">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3697">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3697">At least one of the following is true:</span></span>
    - <span data-ttu-id="eee87-3698">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3698">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="eee87-3699">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3699">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="eee87-3700">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3700">The function Func_us_date finds a date in the right date format.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="eee87-3701">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3701">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="eee87-3702">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="eee87-3702">Keyword_itin</span></span>

- <span data-ttu-id="eee87-3703">taxpayer</span><span class="sxs-lookup"><span data-stu-id="eee87-3703">taxpayer</span></span> 
- <span data-ttu-id="eee87-3704">tax id</span><span class="sxs-lookup"><span data-stu-id="eee87-3704">tax id</span></span> 
- <span data-ttu-id="eee87-3705">tax identification</span><span class="sxs-lookup"><span data-stu-id="eee87-3705">tax identification</span></span> 
- <span data-ttu-id="eee87-3706">itin</span><span class="sxs-lookup"><span data-stu-id="eee87-3706">itin</span></span> 
- <span data-ttu-id="eee87-3707">ssn</span><span class="sxs-lookup"><span data-stu-id="eee87-3707">ssn</span></span> 
- <span data-ttu-id="eee87-3708">언급</span><span class="sxs-lookup"><span data-stu-id="eee87-3708">tin</span></span> 
- <span data-ttu-id="eee87-3709">social security</span><span class="sxs-lookup"><span data-stu-id="eee87-3709">social security</span></span> 
- <span data-ttu-id="eee87-3710">tax payer</span><span class="sxs-lookup"><span data-stu-id="eee87-3710">tax payer</span></span> 
- <span data-ttu-id="eee87-3711">itins</span><span class="sxs-lookup"><span data-stu-id="eee87-3711">itins</span></span> 
- <span data-ttu-id="eee87-3712">taxid</span><span class="sxs-lookup"><span data-stu-id="eee87-3712">taxid</span></span> 
- <span data-ttu-id="eee87-3713">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="eee87-3713">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="eee87-3714">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="eee87-3714">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="eee87-3715">License</span><span class="sxs-lookup"><span data-stu-id="eee87-3715">License</span></span> 
- <span data-ttu-id="eee87-3716">DL</span><span class="sxs-lookup"><span data-stu-id="eee87-3716">DL</span></span> 
- <span data-ttu-id="eee87-3717">DOB</span><span class="sxs-lookup"><span data-stu-id="eee87-3717">DOB</span></span> 
- <span data-ttu-id="eee87-3718">생년월일</span><span class="sxs-lookup"><span data-stu-id="eee87-3718">Birthdate</span></span> 
- <span data-ttu-id="eee87-3719">생일</span><span class="sxs-lookup"><span data-stu-id="eee87-3719">Birthday</span></span> 
- <span data-ttu-id="eee87-3720">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="eee87-3720">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="eee87-3721">미국 SSN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="eee87-3721">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="eee87-3722">형식일</span><span class="sxs-lookup"><span data-stu-id="eee87-3722">Format</span></span>

<span data-ttu-id="eee87-3723">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="eee87-3723">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="eee87-3724">Mid가 2011 이전에 실행 된 경우 SSN은 특정 범위 내에서 번호의 특정 부분이 유효한 지 확인 하는 강력한 서식을 사용 해야 하지만 검사 값은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3724">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="eee87-3725">패턴</span><span class="sxs-lookup"><span data-stu-id="eee87-3725">Pattern</span></span>

<span data-ttu-id="eee87-3726">다음의 네 가지 패턴에서 SSNs를 검색 하는 함수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3726">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="eee87-3727">Func_ssn는 대시 또는 공백을 사용 하 여 서식이 지정 된 2011 이전의 고급 서식 (ddd-dd-dddd 또는 ddd dd dd)을 사용 하 여 SSNs를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3727">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="eee87-3728">Func_unformatted_ssn는 형식이 지정 되지 않은 2011 이전 형식으로 서식이 지정 된 SSNs를 찾습니다 (ddddddddd).</span><span class="sxs-lookup"><span data-stu-id="eee87-3728">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="eee87-3729">Func_randomized_formatted_ssn는 대시 또는 공백으로 서식이 지정 된 post-2011 SSNs를 찾습니다 (ddd-dd-dddd 또는 ddd dd dddd).</span><span class="sxs-lookup"><span data-stu-id="eee87-3729">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="eee87-3730">Func_randomized_unformatted_ssn는 형식 없는 2011 SSNs를 찾고, 서식이 없는 9 자리 숫자 (ddddddddd)를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3730">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="eee87-3731">제외</span><span class="sxs-lookup"><span data-stu-id="eee87-3731">Checksum</span></span>

<span data-ttu-id="eee87-3732">아니요</span><span class="sxs-lookup"><span data-stu-id="eee87-3732">No</span></span>


### <a name="definition"></a><span data-ttu-id="eee87-3733">정의</span><span class="sxs-lookup"><span data-stu-id="eee87-3733">Definition</span></span>

<span data-ttu-id="eee87-3734">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3735">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3735">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3736">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3736">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="eee87-3737">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3737">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-3738">Func_us_address 함수가 올바른 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3738">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="eee87-3739">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3739">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3740">Func_unformatted_ssn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3740">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3741">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3741">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="eee87-3742">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3742">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-3743">Func_us_address 함수가 올바른 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3743">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="eee87-3744">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3744">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3745">Func_randomized_formatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3745">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3746">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3746">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="eee87-3747">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3747">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-3748">Func_us_address 함수가 올바른 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3748">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="eee87-3749">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 55% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3749">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3750">Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3750">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3751">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3751">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="eee87-3752">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3752">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="eee87-3753">Func_us_address 함수가 올바른 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3753">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="eee87-3754">DLP 정책은 300 문자에 근접 한 경우이 유형의 중요 한 정보를 검색 한다는 것을 40% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3754">A DLP policy is 40% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="eee87-3755">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3755">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3756">Func_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3756">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3757">Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3757">The function Func_randomized_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3758">Keyword_ssn의 키워드를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3758">A keyword from Keyword_ssn is not found.</span></span>
 
<span data-ttu-id="eee87-3759">또는</span><span class="sxs-lookup"><span data-stu-id="eee87-3759">Or</span></span>

- <span data-ttu-id="eee87-3760">Func_randomized_formatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3760">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3761">Func_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3761">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3762">Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3762">The function Func_randomized_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="eee87-3763">Keyword_ssn의 키워드를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eee87-3763">A keyword from Keyword_ssn is not found.</span></span>

```xml
<!-- U.S. Social Security Number (SSN) -->
  <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Any minMatches="1">
          <Match idRef="Keyword_ssn" />
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="1">
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Any minMatches="1">
          <Match idRef="Keyword_ssn" />
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="1">
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="40">
        <IdMatch idRef="Func_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
          <Match idRef="Func_randomized_unformatted_ssn" />
          <Match idRef="Keyword_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="40">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
          <Match idRef="Func_randomized_unformatted_ssn" />
          <Match idRef="Keyword_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="eee87-3764">키워드</span><span class="sxs-lookup"><span data-stu-id="eee87-3764">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="eee87-3765">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="eee87-3765">Keyword_ssn</span></span>

- <span data-ttu-id="eee87-3766">Social Security</span><span class="sxs-lookup"><span data-stu-id="eee87-3766">Social Security</span></span> 
- <span data-ttu-id="eee87-3767">Social Security#</span><span class="sxs-lookup"><span data-stu-id="eee87-3767">Social Security#</span></span> 
- <span data-ttu-id="eee87-3768">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="eee87-3768">Soc Sec</span></span> 
- <span data-ttu-id="eee87-3769">SSN</span><span class="sxs-lookup"><span data-stu-id="eee87-3769">SSN</span></span> 
- <span data-ttu-id="eee87-3770">있는 SSN</span><span class="sxs-lookup"><span data-stu-id="eee87-3770">SSNS</span></span> 
- <span data-ttu-id="eee87-3771">SSN #</span><span class="sxs-lookup"><span data-stu-id="eee87-3771">SSN#</span></span> 
- <span data-ttu-id="eee87-3772">대비 #</span><span class="sxs-lookup"><span data-stu-id="eee87-3772">SS#</span></span> 
- <span data-ttu-id="eee87-3773">생길</span><span class="sxs-lookup"><span data-stu-id="eee87-3773">SSID</span></span> 
   

