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
# <a name="what-the-dlp-functions-look-for"></a>DLP 기능이 찾는 항목

DLP(데이터 손실 방지)에는 DLP 정책에 사용할 수 있는 신용 카드 번호 및 EU 직불 카드 번호와 같은 중요한 정보 유형이 포함됩니다. 이러한 중요한 정보 유형은 특정 패턴을 찾은 후 서식이 올바른지 확인하고, 체크섬을 적용하고, 관련된 키워드 또는 기타 정보를 찾아 완전하게 확인합니다. 이 기능 중 일부는 내부 함수에 의해 수행됩니다. 예를 들어 신용 카드 번호 중요한 정보 유형은 만료일과 같은 형식의 날짜를 찾는 함수를 사용하여 숫자가 신용 카드 번호임을 입증하는 데 도움을 줍니다.
  
이 항목에는 이러한 함수가 찾는 대상이 설명되어 있어 미리 정의된 중요한 정보 유형이 작동하는 방식을 이해할 수 있습니다. 자세한 내용은 [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md)을 참조하세요.
  
## <a name="funcusdate"></a>Func_us_date

이 함수는 미국에서 일반적으로 사용 되는 형식에서 날짜에 대 한 찾습니다. 형식 "월/일/년", "월-일-년" 및 "달 1 년 일"이 포함 됩니다. 이름 또는 월의 약어 대 소문자를 구분 하지 않습니다. 
  
예제:
  
- 2016 년 12 월 2 일
    
- 2016 년 12 월 2 일
    
- 02 2016 년 12 월
    
- 12/2/2016
    
- 12/02/16
    
- 10 진수-2-2016
    
- 12-2-16
    
허용되는 월 이름:
  
- 영어
    
  - 1 월, 년 2 월, 3 월, 4 월, 5 월, 년 6 월, 년 7 월, 년 8 월, 년 9 월, 10 월, 년 11 월, 년 12 월
    
  - 1 월 2 월 3 월 4 월 6 월 7 월 8 월 9 월 10 월 11 월 10 진수 초과할 수 있습니다.
    
## <a name="funceudate"></a>Func_eu_date

이 함수는 유럽 연합(및 미국 이외의 대부분의 지역)에서 일반적으로 사용되는 형식의 날짜를 찾습니다. 여기에는 "일/월/년", "일-월-년" 및 "일 월 년" 형식이 포함됩니다. 월 이름 또는 약어는 대/소문자를 구분하지 않습니다.
  
예:
  
- 2 년 12 월 2016
    
- 02 년 12 월 2016
    
- 2 년 12 월 16 일
    
- 2/12/2016
    
- 02/12/16
    
- 2-10 진수-2016
    
- 2-12-16
    
허용되는 월 이름:
  
- 영어
    
  - 1 월, 년 2 월, 3 월, 4 월, 5 월, 년 6 월, 년 7 월, 년 8 월, 년 9 월, 10 월, 년 11 월, 년 12 월
    
  - 1 월 2 월 3 월 4 월 6 월 7 월 8 월 9 월 10 월 11 월 10 진수 초과할 수 있습니다.
    
- 네덜란드어
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - 1 월 2 월 maart 월 mei 6 년 7 월 8 월 9 월 9 월 까지의 oct okt 년 11 월
    
- 프랑스어
    
  - janvier, février, mars, avril, 메일, juin juillet, août, septembre, octobre, novembre, décembre
    
  - janv 합니다. févr 합니다. avril 메일 juin juil 한층 다가가기 합니다. août 9 월 까지의 합니다. 10 년 11 월입니다. déc 합니다.
    
- 독일어
    
  - jänuar, februar, märz, 4 월, 메일, 8 월, 년 9 월, juni juli oktober, 11 월, dezember
    
  - 1 월. / Jän 합니다. 2 월 März 4 월 메일 Juni Juli 8 월 9 월 Okt 합니다. 11 월 Dez 합니다.
    
- 이탈리아어
    
  - gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre
    
  - genn 합니다. febbr 합니다. 3 월입니다. 2004 년 4 월 magg 합니다. giugno luglio ag 합니다. 설정할 합니다. ott 합니다. 11 월입니다. 사전 합니다.
    
- 포르투갈어
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - 1 월 fev 년 3 월 abr 메일 6 년 7 월 전 세우고 자 dez 년 11 월
    
- 스페인어
    
  - enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre
    
  - 2 월 enero 합니다. marzo abr. mayo jun. 년 7 월입니다. agosto 9 월/집합입니다. 10 년 11 월입니다. 사전 합니다.
    
## <a name="funceudate1-deprecated"></a>Func_eu_date1(더 이상 사용되지 않음)

> [!NOTE]
> 이제에 포함 된 포르투갈어 월 이름만 지원 하기 때문에이 함수는 사용 되지 않습니다는 `Func_eu_date` 위의 함수입니다. 
  
이 함수는 포르투갈어에서 일반적으로 사용 되는 형식에서 날짜를 찾습니다. 이 함수에 대 한 형식이 같을 `Func_eu_date`, 사용 되는 언어에만 다릅니다.
  
예제:
  
- 2 Dez 2016
    
- 02 dez 2016
    
- 2 Dez 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-Dez-2016
    
- 2-12-16
    
허용되는 월 이름:
  
- 포르투갈어
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - 1 월 fev 년 3 월 abr 메일 6 년 7 월 전 세우고 자 dez 년 11 월
    
## <a name="funceudate2-deprecated"></a>Func_eu_date2(더 이상 사용되지 않음)

> [!NOTE]
> 이제에 포함 된 네덜란드어 월 이름만 지원 하기 때문에이 함수는 사용 되지 않습니다는 `Func_eu_date` 위의 함수입니다. 
  
이 함수는 네덜란드어에서 일반적으로 사용 되는 형식에서 날짜를 찾습니다. 이 함수에 대 한 형식이 같을 `Func_eu_date`, 사용 되는 언어에만 다릅니다.
  
예제:
  
- 2 Mei 2016
    
- 02 mei 2016
    
- 2 Mei 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-Mei-2016
    
- 2-12-16
    
허용되는 월 이름:
  
- 네덜란드어
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - 1 월 2 월 maart 월 mei 6 년 7 월 8 월 9 월 9 월 까지의 oct okt 년 11 월
    
## <a name="funcexpirationdate"></a>Func_expiration_date

이 함수에서 신용 카드와 직불 카드, 개월 로드를 위해 일을 제외 하는 일반적으로 사용 하는 형식에서 날짜를 찾습니다. 이 함수는 시작 날짜 "월/년 형식으로", "월-년", "[달 이름] 년" 및 "[월 약어] 년"의 일치 합니다. 이름 또는 월의 약어 대 소문자를 구분 하지 않습니다.
  
예제:
  
- MM/YY - 예를 들어 01/11 또는 1/11
    
- MM/YYYY - 예를 들어 01/2011, 1/2011 등
    
- MM-YY -- 예를 들어 01-22 또는 1-11
    
- MM-YYYY -- 예를 들어 01-2000 또는 1-2000
    
다음 형식은 YY 또는 YYYY를 지원합니다.
  
- Month-YYYY -- 예를 들어 Jan-2010, january-2010, Jan-10 또는 january-10
    
- Month YYYY -- 예를 들어 'january 2010', 'Jan 2010', 'january 10' 또는 'Jan 10'
    
- MonthYYYY -- 예를 들어 'january2010', 'Jan2010', 'january10' 또는 'Jan10'
    
- 월/YYYY-예: ' 년 1 월/2010 ' 또는 ' Jan/2010 ' 또는 ' 년 1 월 10' 또는 ' 1 월 10'
    
허용되는 월 이름:
  
- 영어
    
  - 1 월, 년 2 월, 3 월, 4 월, 5 월, 년 6 월, 년 7 월, 년 8 월, 년 9 월, 10 월, 년 11 월, 년 12 월
    
  - 1 월 2 월 3 월 4 년 6 월 7 월 8 월 9 월 까지의 Oct 년 11 월 10 진수를 수 있습니다.
    
## <a name="funcusaddress"></a>Func_us_address

이 함수는 우편 주소에 사용되는 것과 같이 미국 주 이름 또는 주 약어와 유효한 우편 번호를 찾습니다. 우편 번호는 미국 주 이름 또는 약어와 관련된 올바른 우편 번호 중 하나여야 합니다. 미국 주 이름과 우편 번호를 문장 부호나 문자로 구분할 수 없습니다.
  
예:
  
- Washington 98052
    
- Washington 98052-9998
    
- WA 98052
    
- WA 98052-9998
    

