---
title: DLP 기능이 찾는 항목
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: 중요 한 정보 유형 특정 패턴을 살펴보고 적절 한 서식, 체크섬, 적용 (영문) 및 관련 된 키워드 또는 기타 정보에 대 한 자세한 내용은 수 있도록 하 여 corroborate 합니다. 이 기능 중 일부는 내부 함수에 의해 수행 됩니다. 이 항목에서는 이러한 함수 찾을 내용, 미리 정의 된 중요 한 정보 유형 작동 하는 방법을 이해 하는데 도움이 되에 대해 설명 합니다.
ms.openlocfilehash: 510f98e2b4e1d2480550f11026cf445be6ffc931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013762"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="1b0c0-105">DLP 기능이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="1b0c0-105">What the DLP functions look for</span></span>

<span data-ttu-id="1b0c0-p102">DLP(데이터 손실 방지)에는 DLP 정책에 사용할 수 있는 신용 카드 번호 및 EU 직불 카드 번호와 같은 중요한 정보 유형이 포함됩니다. 이러한 중요한 정보 유형은 특정 패턴을 찾은 후 서식이 올바른지 확인하고, 체크섬을 적용하고, 관련된 키워드 또는 기타 정보를 찾아 완전하게 확인합니다. 이 기능 중 일부는 내부 함수에 의해 수행됩니다. 예를 들어 신용 카드 번호 중요한 정보 유형은 만료일과 같은 형식의 날짜를 찾는 함수를 사용하여 숫자가 신용 카드 번호임을 입증하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p102">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="1b0c0-p103">이 항목에는 이러한 함수가 찾는 대상이 설명되어 있어 미리 정의된 중요한 정보 유형이 작동하는 방식을 이해할 수 있습니다. 자세한 내용은 [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p103">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work. For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="1b0c0-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="1b0c0-112">Func_us_date</span></span>

<span data-ttu-id="1b0c0-p104">이 함수는 미국에서 일반적으로 사용 되는 형식에서 날짜에 대 한 찾습니다. 형식 "월/일/년", "월-일-년" 및 "달 1 년 일"이 포함 됩니다. 이름 또는 월의 약어 대 소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p104">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ". The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="1b0c0-115">예제:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-115">Examples:</span></span>
  
- <span data-ttu-id="1b0c0-116">2016 년 12 월 2 일</span><span class="sxs-lookup"><span data-stu-id="1b0c0-116">December 2, 2016</span></span>
    
- <span data-ttu-id="1b0c0-117">2016 년 12 월 2 일</span><span class="sxs-lookup"><span data-stu-id="1b0c0-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="1b0c0-118">02 2016 년 12 월</span><span class="sxs-lookup"><span data-stu-id="1b0c0-118">dec 02 2016</span></span>
    
- <span data-ttu-id="1b0c0-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-119">12/2/2016</span></span>
    
- <span data-ttu-id="1b0c0-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-120">12/02/16</span></span>
    
- <span data-ttu-id="1b0c0-121">10 진수-2-2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="1b0c0-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-122">12-2-16</span></span>
    
<span data-ttu-id="1b0c0-123">허용되는 월 이름:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-123">Accepted month names:</span></span>
  
- <span data-ttu-id="1b0c0-124">영어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-124">English</span></span>
    
  - <span data-ttu-id="1b0c0-125">1 월, 년 2 월, 3 월, 4 월, 5 월, 년 6 월, 년 7 월, 년 8 월, 년 9 월, 10 월, 년 11 월, 년 12 월</span><span class="sxs-lookup"><span data-stu-id="1b0c0-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="1b0c0-126">1 월 2 월 3 월 4 월 6 월 7 월 8 월 9 월 10 월 11 월 10 진수 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="1b0c0-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="1b0c0-127">Func_eu_date</span></span>

<span data-ttu-id="1b0c0-p105">이 함수는 유럽 연합(및 미국 이외의 대부분의 지역)에서 일반적으로 사용되는 형식의 날짜를 찾습니다. 여기에는 "일/월/년", "일-월-년" 및 "일 월 년" 형식이 포함됩니다. 월 이름 또는 약어는 대/소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p105">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="1b0c0-132">예:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-132">Examples:</span></span>
  
- <span data-ttu-id="1b0c0-133">2 년 12 월 2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="1b0c0-134">02 년 12 월 2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-134">02 dec 2016</span></span>
    
- <span data-ttu-id="1b0c0-135">2 년 12 월 16 일</span><span class="sxs-lookup"><span data-stu-id="1b0c0-135">2 Dec 16</span></span>
    
- <span data-ttu-id="1b0c0-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-136">2/12/2016</span></span>
    
- <span data-ttu-id="1b0c0-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-137">02/12/16</span></span>
    
- <span data-ttu-id="1b0c0-138">2-10 진수-2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="1b0c0-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-139">2-12-16</span></span>
    
<span data-ttu-id="1b0c0-140">허용되는 월 이름:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-140">Accepted month names:</span></span>
  
- <span data-ttu-id="1b0c0-141">영어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-141">English</span></span>
    
  - <span data-ttu-id="1b0c0-142">1 월, 년 2 월, 3 월, 4 월, 5 월, 년 6 월, 년 7 월, 년 8 월, 년 9 월, 10 월, 년 11 월, 년 12 월</span><span class="sxs-lookup"><span data-stu-id="1b0c0-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="1b0c0-143">1 월 2 월 3 월 4 월 6 월 7 월 8 월 9 월 10 월 11 월 10 진수 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="1b0c0-144">네덜란드어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-144">Dutch</span></span>
    
  - <span data-ttu-id="1b0c0-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="1b0c0-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="1b0c0-146">1 월 2 월 maart 월 mei 6 년 7 월 8 월 9 월 9 월 까지의 oct okt 년 11 월</span><span class="sxs-lookup"><span data-stu-id="1b0c0-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="1b0c0-147">프랑스어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-147">French</span></span>
    
  - <span data-ttu-id="1b0c0-148">janvier, février, mars, avril, 메일, juin juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="1b0c0-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="1b0c0-p106">janv 합니다. févr 합니다. avril 메일 juin juil 한층 다가가기 합니다. août 9 월 까지의 합니다. 10 년 11 월입니다. déc 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p106">janv. févr. mars avril mai juin juil. août sept. oct. nov. déc.</span></span>
    
- <span data-ttu-id="1b0c0-156">독일어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-156">German</span></span>
    
  - <span data-ttu-id="1b0c0-157">jänuar, februar, märz, 4 월, 메일, 8 월, 년 9 월, juni juli oktober, 11 월, dezember</span><span class="sxs-lookup"><span data-stu-id="1b0c0-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="1b0c0-p107">1 월. / Jän 합니다. 2 월 März 4 월 메일 Juni Juli 8 월 9 월 Okt 합니다. 11 월 Dez 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span></span>
    
- <span data-ttu-id="1b0c0-161">이탈리아어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-161">Italian</span></span>
    
  - <span data-ttu-id="1b0c0-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span><span class="sxs-lookup"><span data-stu-id="1b0c0-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="1b0c0-p108">genn 합니다. febbr 합니다. 3 월입니다. 2004 년 4 월 magg 합니다. giugno luglio ag 합니다. 설정할 합니다. ott 합니다. 11 월입니다. 사전 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p108">genn. febbr. mar. apr. magg. giugno luglio ag. sett. ott. nov. dic.</span></span>
    
- <span data-ttu-id="1b0c0-173">포르투갈어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-173">Portuguese</span></span>
    
  - <span data-ttu-id="1b0c0-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="1b0c0-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="1b0c0-175">1 월 fev 년 3 월 abr 메일 6 년 7 월 전 세우고 자 dez 년 11 월</span><span class="sxs-lookup"><span data-stu-id="1b0c0-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="1b0c0-176">스페인어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-176">Spanish</span></span>
    
  - <span data-ttu-id="1b0c0-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="1b0c0-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="1b0c0-p109">2 월 enero 합니다. marzo abr. mayo jun. 년 7 월입니다. agosto 9 월/집합입니다. 10 년 11 월입니다. 사전 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p109">enero feb. marzo abr. mayo jun. jul. agosto sept./set. oct. nov. dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="1b0c0-186">Func_eu_date1(더 이상 사용되지 않음)</span><span class="sxs-lookup"><span data-stu-id="1b0c0-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="1b0c0-187">이제에 포함 된 포르투갈어 월 이름만 지원 하기 때문에이 함수는 사용 되지 않습니다는 `Func_eu_date` 위의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="1b0c0-p110">이 함수는 포르투갈어에서 일반적으로 사용 되는 형식에서 날짜를 찾습니다. 이 함수에 대 한 형식이 같을 `Func_eu_date`, 사용 되는 언어에만 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p110">This function looks for a date in the format commonly used in Portuguese. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="1b0c0-190">예제:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-190">Examples:</span></span>
  
- <span data-ttu-id="1b0c0-191">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="1b0c0-192">02 dez 2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-192">02 dez 2016</span></span>
    
- <span data-ttu-id="1b0c0-193">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-193">2 Dez 16</span></span>
    
- <span data-ttu-id="1b0c0-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-194">2/12/2016</span></span>
    
- <span data-ttu-id="1b0c0-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-195">02/12/16</span></span>
    
- <span data-ttu-id="1b0c0-196">2-Dez-2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="1b0c0-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-197">2-12-16</span></span>
    
<span data-ttu-id="1b0c0-198">허용되는 월 이름:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-198">Accepted month names:</span></span>
  
- <span data-ttu-id="1b0c0-199">포르투갈어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-199">Portuguese</span></span>
    
  - <span data-ttu-id="1b0c0-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="1b0c0-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="1b0c0-201">1 월 fev 년 3 월 abr 메일 6 년 7 월 전 세우고 자 dez 년 11 월</span><span class="sxs-lookup"><span data-stu-id="1b0c0-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="1b0c0-202">Func_eu_date2(더 이상 사용되지 않음)</span><span class="sxs-lookup"><span data-stu-id="1b0c0-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="1b0c0-203">이제에 포함 된 네덜란드어 월 이름만 지원 하기 때문에이 함수는 사용 되지 않습니다는 `Func_eu_date` 위의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="1b0c0-p111">이 함수는 네덜란드어에서 일반적으로 사용 되는 형식에서 날짜를 찾습니다. 이 함수에 대 한 형식이 같을 `Func_eu_date`, 사용 되는 언어에만 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p111">This function looks for a date in the format commonly used in Dutch. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="1b0c0-206">예제:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-206">Examples:</span></span>
  
- <span data-ttu-id="1b0c0-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="1b0c0-208">02 mei 2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-208">02 mei 2016</span></span>
    
- <span data-ttu-id="1b0c0-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-209">2 Mei 16</span></span>
    
- <span data-ttu-id="1b0c0-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-210">2/12/2016</span></span>
    
- <span data-ttu-id="1b0c0-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-211">02/12/16</span></span>
    
- <span data-ttu-id="1b0c0-212">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="1b0c0-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="1b0c0-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="1b0c0-213">2-12-16</span></span>
    
<span data-ttu-id="1b0c0-214">허용되는 월 이름:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-214">Accepted month names:</span></span>
  
- <span data-ttu-id="1b0c0-215">네덜란드어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-215">Dutch</span></span>
    
  - <span data-ttu-id="1b0c0-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="1b0c0-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="1b0c0-217">1 월 2 월 maart 월 mei 6 년 7 월 8 월 9 월 9 월 까지의 oct okt 년 11 월</span><span class="sxs-lookup"><span data-stu-id="1b0c0-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="1b0c0-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="1b0c0-218">Func_expiration_date</span></span>

<span data-ttu-id="1b0c0-p112">이 함수에서 신용 카드와 직불 카드, 개월 로드를 위해 일을 제외 하는 일반적으로 사용 하는 형식에서 날짜를 찾습니다. 이 함수는 시작 날짜 "월/년 형식으로", "월-년", "[달 이름] 년" 및 "[월 약어] 년"의 일치 합니다. 이름 또는 월의 약어 대 소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p112">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months. This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="1b0c0-222">예제:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-222">Examples:</span></span>
  
- <span data-ttu-id="1b0c0-223">MM/YY - 예를 들어 01/11 또는 1/11</span><span class="sxs-lookup"><span data-stu-id="1b0c0-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="1b0c0-224">MM/YYYY - 예를 들어 01/2011, 1/2011 등</span><span class="sxs-lookup"><span data-stu-id="1b0c0-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="1b0c0-225">MM-YY -- 예를 들어 01-22 또는 1-11</span><span class="sxs-lookup"><span data-stu-id="1b0c0-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="1b0c0-226">MM-YYYY -- 예를 들어 01-2000 또는 1-2000</span><span class="sxs-lookup"><span data-stu-id="1b0c0-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="1b0c0-227">다음 형식은 YY 또는 YYYY를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="1b0c0-228">Month-YYYY -- 예를 들어 Jan-2010, january-2010, Jan-10 또는 january-10</span><span class="sxs-lookup"><span data-stu-id="1b0c0-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="1b0c0-229">Month YYYY -- 예를 들어 'january 2010', 'Jan 2010', 'january 10' 또는 'Jan 10'</span><span class="sxs-lookup"><span data-stu-id="1b0c0-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="1b0c0-230">MonthYYYY -- 예를 들어 'january2010', 'Jan2010', 'january10' 또는 'Jan10'</span><span class="sxs-lookup"><span data-stu-id="1b0c0-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="1b0c0-231">월/YYYY-예: ' 년 1 월/2010 ' 또는 ' Jan/2010 ' 또는 ' 년 1 월 10' 또는 ' 1 월 10'</span><span class="sxs-lookup"><span data-stu-id="1b0c0-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="1b0c0-232">허용되는 월 이름:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-232">Accepted month names:</span></span>
  
- <span data-ttu-id="1b0c0-233">영어</span><span class="sxs-lookup"><span data-stu-id="1b0c0-233">English</span></span>
    
  - <span data-ttu-id="1b0c0-234">1 월, 년 2 월, 3 월, 4 월, 5 월, 년 6 월, 년 7 월, 년 8 월, 년 9 월, 10 월, 년 11 월, 년 12 월</span><span class="sxs-lookup"><span data-stu-id="1b0c0-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="1b0c0-235">1 월 2 월 3 월 4 년 6 월 7 월 8 월 9 월 까지의 Oct 년 11 월 10 진수를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="1b0c0-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="1b0c0-236">Func_us_address</span></span>

<span data-ttu-id="1b0c0-p113">이 함수는 우편 주소에 사용되는 것과 같이 미국 주 이름 또는 주 약어와 유효한 우편 번호를 찾습니다. 우편 번호는 미국 주 이름 또는 약어와 관련된 올바른 우편 번호 중 하나여야 합니다. 미국 주 이름과 우편 번호를 문장 부호나 문자로 구분할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0c0-p113">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="1b0c0-240">예:</span><span class="sxs-lookup"><span data-stu-id="1b0c0-240">Examples:</span></span>
  
- <span data-ttu-id="1b0c0-241">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="1b0c0-241">Washington 98052</span></span>
    
- <span data-ttu-id="1b0c0-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="1b0c0-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="1b0c0-243">WA 98052</span><span class="sxs-lookup"><span data-stu-id="1b0c0-243">WA 98052</span></span>
    
- <span data-ttu-id="1b0c0-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="1b0c0-244">WA 98052-9998</span></span>
    

