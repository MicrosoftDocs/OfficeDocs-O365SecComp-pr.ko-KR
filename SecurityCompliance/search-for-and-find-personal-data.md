---
title: 개인 데이터 검색 및 찾기
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 2/7/2018
ms.audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- GDPR
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Office 365에서 개인 데이터를 검색하고 찾는 방법을 알아봅니다.
ms.openlocfilehash: 3c2981116e2abb3518a132084a697618ef3261cc
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265340"
---
# <a name="search-for-and-find-personal-data"></a><span data-ttu-id="d71de-103">개인 데이터 검색 및 찾기</span><span class="sxs-lookup"><span data-stu-id="d71de-103">Search for and find personal data</span></span>

<span data-ttu-id="d71de-104">개인 데이터는 EU(유럽 연합)에 거주하는 식별되었거나 식별 가능한 자연인과 관련된 데이터로서 GDPR에서 매우 광범위하게 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-104">Personal data is defined very broadly under the GDPR as any data that relates to an identified or identifiable natural person that is a resident of the European Union (EU).</span></span>

<span data-ttu-id="d71de-105">문서 4 - 정의</span><span class="sxs-lookup"><span data-stu-id="d71de-105">Article 4 – Definitions</span></span>

> <span data-ttu-id="d71de-106">'개인 데이터'는 식별되었거나 식별 가능한 자연인(‘데이터 주체’)과 관련된 정보를 의미합니다. 식별 가능한 자연인은 직간접적으로, 특히 이름, 식별 번호, 위치 데이터, 온라인 식별자 또는 해당 자연인의 신체적, 생리적, 유전적, 정신적, 경제적, 문화적 또는 사회적 ID와 같은 식별자를 참조하여 식별될 수 있는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-106">‘personal data’ means any information relating to an identified or identifiable natural person (‘data subject’); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural or social identity of that natural person;</span></span>

<span data-ttu-id="d71de-107">이 문서에서는 SharePoint Online 및 비즈니스용 OneDrive에 저장된 개인 데이터를 찾는 방법을 보여 줍니다(모든 Office 365 그룹 및 Microsoft Teams 사이트 포함) </span><span class="sxs-lookup"><span data-stu-id="d71de-107">This article demonstrates how to find personal data stored in SharePoint Online and OneDrive for Business (which includes the sites for all Office 365 groups and Microsoft Teams).</span></span>

<span data-ttu-id="d71de-p101">Office 365에서 GDPR이 적용되는 개인 데이터를 찾으려면 중요한 정보 유형을 사용해야 합니다. 이 과정에서 자동화된 서비스가 의료 서비스 번호 및 신용 카드 번호와 같은 특정 정보 유형을 인식하는 방식이 정의됩니다. 현재, 휴지 상태의 Exchange 사서함에서 데이터를 찾는 데는 이러한 정보를 사용할 수 없습니다. 그렇지만 중요한 정보 유형을 데이터 손실 방지 정책과 함께 사용하여 전송 중인 메일에서 개인 데이터를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-p101">Finding personal data subject to GDPR relies on using sensitive information types in Office 365. These define how the automated process recognizes specific information types such as health service numbers and credit card numbers. At this time these cannot be used to find data in Exchange mailboxes at rest. However, sensitive information types can be used with data loss prevention policies to find personal data in mail while in transit.</span></span>

<span data-ttu-id="d71de-112">따라서 현재는 콘텐츠 검색을 사용하여 Exchange Online 사서함의 휴지 상태의 개인 데이터를 찾을 수 없지만, GDPR에 맞게 조정한 중요한 정보 유형을 사용하여 전자 메일을 통해 전송되는 개인 정보를 찾아 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-112">So, while you can’t currently use Content Search to find personal data at rest in Exchange Online mailboxes, you can use the sensitive information types you curate for GDPR to find and protect personal information as it is sent through email.</span></span>

## <a name="use-content-search-to-find-personal-data"></a><span data-ttu-id="d71de-113">콘텐츠 검색을 사용하여 개인 데이터 찾기</span><span class="sxs-lookup"><span data-stu-id="d71de-113">Use Content Search to find personal data</span></span>

<span data-ttu-id="d71de-p102">Office 365에서 개인 데이터를 찾는 위한 3단계 접근 방식이 권장됩니다. 이 항목의 나머지 부분에서는 이러한 각 단계에 대한 지침을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-p102">Microsoft recommends a three-stage approach to finding personal data in Office 365. The rest of this topic provides guidance for each of these stages.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d71de-116"><strong>단계</strong></span><span class="sxs-lookup"><span data-stu-id="d71de-116"><strong>Step</strong></span></span></th>
<th align="left"><span data-ttu-id="d71de-117"><strong>설명</strong></span><span class="sxs-lookup"><span data-stu-id="d71de-117"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d71de-118">1. 중요한 정보 유형 검색</span><span class="sxs-lookup"><span data-stu-id="d71de-118">1. Search for sensitive information types</span></span></p></td>
<td align="left"><p><span data-ttu-id="d71de-p103">먼저 중요한 정보 유형을 사용하여 개인 데이터를 찾습니다. 각각의 중요한 정보 유형에 대해 콘텐츠 검색 쿼리를 만듭니다. 쿼리를 실행한 후 결과를 분석합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-p103">Start by using sensitive information types to find personal data. Create a Content Search query for each sensitive information type. Run the query and analyze the results.</span></span></p>
<span data-ttu-id="d71de-122">필요에 따라 가양성을 줄이기 위해 쿼리에 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-122">If needed, add parameters to the query to reduce false positives:</span></span> <li><span data-ttu-id="d71de-123">개수 범위</span><span class="sxs-lookup"><span data-stu-id="d71de-123">Count range</span></span></li>
    <li><span data-ttu-id="d71de-124">신뢰도 범위</span><span class="sxs-lookup"><span data-stu-id="d71de-124">Confidence range</span></span></li>
    <li><span data-ttu-id="d71de-125">좀 더 복잡한 쿼리를 위한 기타 속성 또는 연산자</span><span class="sxs-lookup"><span data-stu-id="d71de-125">Other properties or operators for more complex queries</span></span></li>
<p><span data-ttu-id="d71de-126">필요한 경우 조직에 맞게 정확도를 향상시키도록 중요한 정보 유형을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-126">If necessary, modify a sensitive information type to improve accuracy for your organization:</span></span></p>
<p><li><span data-ttu-id="d71de-127">XML에서 직접 신뢰 수준을 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-127">Adjust the confidence level directly in the XML.</span></span></li></p>
<p><li><span data-ttu-id="d71de-128">키워드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-128">Add key words.</span></span></li></p>
<p><li><span data-ttu-id="d71de-129">키워드에 대한 근접 요구 사항을 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-129">Adjust the proximity requirements for keywords.</span></span></li></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d71de-130">2. KQL(키워드 쿼리 언어)을 사용하여 작업 환경에서 추가 개인 데이터 찾기</span><span class="sxs-lookup"><span data-stu-id="d71de-130">2. Use Keyword Query Language (KQL) to find additional personal data in your environment</span></span></p></td>
<td align="left"><p><span data-ttu-id="d71de-131">중요한 정보 유형에 포함되지 데이터를 찾으려면 KQL 쿼리 언어를 사용하여 사용자 지정 쿼리를 개발합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-131">To find data not included in sensitive information types, use the KQL query language to develop custom queries.</span></span></p>
<p><span data-ttu-id="d71de-132">이러한 검색의 결과를 테스트하고 예상된 결과를 얻을 때까지 KQL 쿼리 문자열을 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-132">Test the results of these searches and adjust the KQL query string until you achieve the expected result.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d71de-133">3. KQL 쿼리를 사용하여 새 사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="d71de-133">3. Create new custom sensitive information types using the KQL queries</span></span></p></td>
<td align="left"><span data-ttu-id="d71de-p104">KQL 쿼리를 최적화하여 대상 데이터를 찾은 후 이러한 쿼리를 사용하여 새 사용자 지정 중요한 정보 유형을 만듭니다. 그런 후 DLP 정책 및 기타 도구와 다른 KQL 쿼리 내에서 콘텐츠 검색에 이러한 사용자 지정 중요한 정보 유형을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-p104">After optimizing KQL queries to find target data, create new custom sensitive information types using these queries. You can then use these custom sensitive information types with Content Search, in DLP policies and other tools, and within other KQL queries.</span></span></td>
</tr>
</tbody>
</table>


## <a name="search-for-sensitive-information-types-using-content-search"></a><span data-ttu-id="d71de-136">콘텐츠 검색을 사용하여 중요한 정보 유형 검색</span><span class="sxs-lookup"><span data-stu-id="d71de-136">Search for sensitive information types using Content Search</span></span>

<span data-ttu-id="d71de-137">Office 365에 포함된 중요한 정보 유형을 사용하여 개인 데이터 검색을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-137">Begin searching for personal data by using the sensitive information types that are included with Office 365.</span></span> <span data-ttu-id="d71de-138">보안 센터 및 규정 준수 센터의 분류에 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-138">These are listed under Classification in the security center and compliance center.</span></span>

<span data-ttu-id="d71de-139">이 주제에는 유럽 연합 시민에게 적용되는 일부 중요한 정보 유형 목록이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-139">This topic includes a list of some sensitive information types that apply to citizens in the European Union.</span></span> <span data-ttu-id="d71de-140">GDPR 규정 준수에 도움이 될 수 있는 추가 사항은 보안 센터 또는 규정 준수 센터를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="d71de-140">Check the security center or the compliance center for new additions that can help with GDPR compliance.</span></span>

<span data-ttu-id="d71de-141">또한 [중요한 정보 유형 및 각 유형이 확인하는 내용 목록](https://support.office.com/ko-KR/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d71de-141">Also see this article: [List of sensitive information types and what each one looks for](https://support.office.com/ko-KR/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b).</span></span>

<span data-ttu-id="d71de-p107">중요한 정보 유형은 정규식이나 함수로 식별될 수 있는 패턴으로 정의됩니다. 또한 키워드 및 체크섬과 같은 확증적인 증거를 사용하여 중요한 정보 유형을 식별할 수 있습니다. 이러한 평가 프로세스에서 신뢰 수준 및 근접성도 사용됩니다. 중요한 정보 유형은 정규식이나 함수로 식별될 수 있는 패턴으로 정의됩니다. 또한 키워드 및 체크섬과 같은 보완적 증거를 사용하여 중요한 정보 유형을 식별할 수 있습니다. 신뢰도 및 근접성도 평가 프로세스에서 활용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-p107">Sensitive information types define how the automated process recognizes specific information types such as bank account numbers, health service numbers, and credit card numbers. Sensitive information types are also referred to as conditions. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>

<span data-ttu-id="d71de-147">현재, 사서함에서 휴지 상태의 데이터를 찾는 데는 중요한 정보 유형을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-147">At this time sensitive information types cannot be used to find data at rest in mailboxes.</span></span>

### <a name="using-content-search-with-sensitive-information-types"></a><span data-ttu-id="d71de-148">중요한 정보 유형에 콘텐츠 검색 사용</span><span class="sxs-lookup"><span data-stu-id="d71de-148">Using Content Search with sensitive information types</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d71de-149"><strong>단계</strong></span><span class="sxs-lookup"><span data-stu-id="d71de-149"><strong>Step</strong></span></span></th>
<th align="left"><span data-ttu-id="d71de-150"><strong>추가 정보</strong></span><span class="sxs-lookup"><span data-stu-id="d71de-150"><strong>More information</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd"><td align="left"><p><span data-ttu-id="d71de-151">보안 및 준수 센터에서 콘텐츠 검색으로 이동</span><span class="sxs-lookup"><span data-stu-id="d71de-151">Go to Content Search in the Security and Compliance Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="d71de-152">보안 및 준수 센터의 왼쪽 창에서 **검색 및 조사** &gt; **콘텐츠 검색**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-152">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** &gt; **Content search**.</span></span></p>
<p><span data-ttu-id="d71de-153">
  <a href="https://support.office.com/en-us/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a">Office 365 보안 및 준수 센터에서 콘텐츠 검색 실행</a>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d71de-153">See <a href="https://support.office.com/en-us/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a">Run a Content Search in the Office 365 Security &amp; Compliance Center</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d71de-154">각 중요한 정보 유형에 대해 새 검색 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="d71de-154">Create a new search item for each sensitive information type</span></span></p></td>
<td align="left"><p><span data-ttu-id="d71de-155">다음 구문을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-155">Use the following syntax:</span></span></p>
<blockquote>
<p><span data-ttu-id="d71de-156">SensitiveType:”&lt;type&gt;”</span><span class="sxs-lookup"><span data-stu-id="d71de-156">SensitiveType:”&lt;type&gt;”</span></span></p>
</blockquote>
<p><span data-ttu-id="d71de-157">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-157">For example:</span></span></p>
<blockquote>
<p><span data-ttu-id="d71de-158">SensitiveType:&quot;France Passport Number&quot;</span><span class="sxs-lookup"><span data-stu-id="d71de-158">SensitiveType:&quot;France Passport Number&quot;</span></span></p>
</blockquote>
<p><span data-ttu-id="d71de-p108">검색 범위를 SharePoint(비즈니스용 OneDrive 포함)으로 지정합니다. 구문이 정확한지와 불필요한 공백이나 입력 오류가 없는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-p108">Scope the search to SharePoint (includes OneDrive for Business). Make sure the syntax is exact and there are no extra spaces or typos.</span></span></p>
<p><span data-ttu-id="d71de-161"><a href="https://support.office.com/ko-KR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836">사이트에 저장된 중요한 데이터를 찾기 위한 쿼리 작성</a>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d71de-161">See <a href="https://support.office.com/ko-KR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836">Form a query to find sensitive data stored on sites</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d71de-162">각 검색에 대한 결과 검토</span><span class="sxs-lookup"><span data-stu-id="d71de-162">Review the results for each search</span></span></p></td>
<td align="left"><p><span data-ttu-id="d71de-163">다음 유형의 문제를 찾아 쿼리 정확도가 원하는 수준인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-163">Look for these types of issues to determine if the query accuracy is on target:</span></span></p>
<p><li><span data-ttu-id="d71de-164">많은 가양성</span><span class="sxs-lookup"><span data-stu-id="d71de-164">Many false positives</span></span></li></p>
<p><li><span data-ttu-id="d71de-165">누락된 데이터의 알려진 인스턴스</span><span class="sxs-lookup"><span data-stu-id="d71de-165">Missing known instances of data</span></span></li></p>
<p><span data-ttu-id="d71de-166">
  <a href="https://support.office.com/en-us/article/Export-Content-Search-results-from-the-Office-365-Security-Compliance-Center-ed48d448-3714-4c42-85f5-10f75f6a4278">Office 365 보안 및 준수 센터에서 콘텐츠 검색 결과 내보내기</a>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d71de-166">See <a href="https://support.office.com/en-us/article/Export-Content-Search-results-from-the-Office-365-Security-Compliance-Center-ed48d448-3714-4c42-85f5-10f75f6a4278">Export Content Search results from the Office 365 Security &amp; Compliance Center</a>.</span></span></p>
<p><span data-ttu-id="d71de-167">참고: Mozilla Firefox 또는 Chrome을 사용하는 경우 필요한 추가 기능을 설치하기 위해 먼저 Internet Explorer 또는 Edge를 사용하여 보고서를 다운로드해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-167">Note: if you’re using Mozilla Firefox or Chrome, you might need to first download reports using Internet Explorer or Edge in order to install the required add-in.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="sensitive-information-types-for-eu-citizen-data"></a><span data-ttu-id="d71de-168">EU 거주민 데이터에 대한 중요한 정보 유형</span><span class="sxs-lookup"><span data-stu-id="d71de-168">Sensitive information types for EU citizen data</span></span>

<span data-ttu-id="d71de-p109">이러한 중요한 정보 유형으로 시작합니다. EU 국가의 개인 데이터에 대한 더 많은 중요한 정보 유형이 곧 제공될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-p109">Start with these sensitive information types. Many more sensitive information types are coming soon for personal data in EU countries.</span></span>

> <span data-ttu-id="d71de-171">벨기에 국가 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-171">Belgium National Number</span></span>
>
> <span data-ttu-id="d71de-172">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-172">Credit Card Number</span></span>
>
> <span data-ttu-id="d71de-173">크로아티아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-173">Croatia Identity Card Number</span></span>
>
> <span data-ttu-id="d71de-174">크로아티아 개인 식별(OIB) 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-174">Croatia Personal Identification (OIB) Number</span></span>
>
> <span data-ttu-id="d71de-175">체코 국가 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-175">Czech National Identity Card Number</span></span>
>
> <span data-ttu-id="d71de-176">덴마크 개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-176">Denmark Personal Identification Number</span></span>
>
> <span data-ttu-id="d71de-177">유럽 직불 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-177">EU Debit Card Number</span></span>
>
> <span data-ttu-id="d71de-178">핀란드 국가 ID</span><span class="sxs-lookup"><span data-stu-id="d71de-178">Finland National ID</span></span>
>
> <span data-ttu-id="d71de-179">핀란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-179">Finland Passport Number</span></span>
>
> <span data-ttu-id="d71de-180">프랑스 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-180">France Driver's License Number</span></span>
>
> <span data-ttu-id="d71de-181">프랑스 국가 ID 카드(CNI)</span><span class="sxs-lookup"><span data-stu-id="d71de-181">France National ID Card (CNI)</span></span>
>
> <span data-ttu-id="d71de-182">프랑스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-182">France Passport Number</span></span>
>
> <span data-ttu-id="d71de-183">프랑스 사회 보장 번호(INSEE)</span><span class="sxs-lookup"><span data-stu-id="d71de-183">France Social Security Number (INSEE)</span></span>
>
> <span data-ttu-id="d71de-184">독일 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-184">German Driver’s License Number</span></span>
>
> <span data-ttu-id="d71de-185">독일 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-185">Germany Identity Card Number</span></span>
>
> <span data-ttu-id="d71de-186">독일 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-186">German Passport Number</span></span>
>
> <span data-ttu-id="d71de-187">그리스 국가 ID 카드</span><span class="sxs-lookup"><span data-stu-id="d71de-187">Greece National ID Card</span></span>
>
> <span data-ttu-id="d71de-188">IBAN(국제 은행 계좌 번호)</span><span class="sxs-lookup"><span data-stu-id="d71de-188">International Banking Account Number (IBAN)</span></span>
>
> <span data-ttu-id="d71de-189">IP 주소</span><span class="sxs-lookup"><span data-stu-id="d71de-189">IP Address</span></span>
>
> <span data-ttu-id="d71de-190">아일랜드 PPS(개인 공공 서비스) 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-190">Ireland Personal Public Service (PPS) Number</span></span>
>
> <span data-ttu-id="d71de-191">이탈리아 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-191">Italy’s Driver’s License Number</span></span>
>
> <span data-ttu-id="d71de-192">네덜란드 시민 서비스(BSN) 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-192">Netherlands Citizen’s Service (BSN) Number</span></span>
>
> <span data-ttu-id="d71de-193">노르웨이 ID 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-193">Norway Identity Number</span></span>
>
> <span data-ttu-id="d71de-194">폴란드 ID 카드</span><span class="sxs-lookup"><span data-stu-id="d71de-194">Poland Identity Card</span></span>
>
> <span data-ttu-id="d71de-195">폴란드 국가 ID(PESEL)</span><span class="sxs-lookup"><span data-stu-id="d71de-195">Poland National ID (PESEL)</span></span>
>
> <span data-ttu-id="d71de-196">폴란드 여권</span><span class="sxs-lookup"><span data-stu-id="d71de-196">Poland Passport</span></span>
>
> <span data-ttu-id="d71de-197">포르투갈 시민 카드 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-197">Portugal Citizen Card Number</span></span>
>
> <span data-ttu-id="d71de-198">스페인 SSN(사회 보장 번호)</span><span class="sxs-lookup"><span data-stu-id="d71de-198">Spain Social Security Number (SSN)</span></span>
>
> <span data-ttu-id="d71de-199">스웨덴 국가 ID</span><span class="sxs-lookup"><span data-stu-id="d71de-199">Sweden National ID</span></span>
>
> <span data-ttu-id="d71de-200">스웨덴 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-200">Sweden Passport Number</span></span>
>
> <span data-ttu-id="d71de-p110">영국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-p110">U.K. Driver’s License Number</span></span>
>
> <span data-ttu-id="d71de-p111">영국 선거 롤 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-p111">U.K. Electoral Roll Number</span></span>
>
> <span data-ttu-id="d71de-p112">영국 국립 보건 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-p112">U.K. National Health Service Number</span></span>
>
> <span data-ttu-id="d71de-p113">영국 NINO(국민 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="d71de-p113">U.K. National Insurance Number (NINO)</span></span>
>
> <span data-ttu-id="d71de-p114">미국/영국 여권 번호</span><span class="sxs-lookup"><span data-stu-id="d71de-p114">U.S./U.K. Passport Number</span></span>

## <a name="add-parameters-to-a-sensitive-information-type-query-to-hone-the-results"></a><span data-ttu-id="d71de-211">중요한 정보 유형 쿼리에 매개 변수를 추가하여 결과 조정</span><span class="sxs-lookup"><span data-stu-id="d71de-211">Add parameters to a sensitive information type query to hone the results</span></span>

<span data-ttu-id="d71de-212">중요한 정보 유형 쿼리에 다음 매개 변수를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-212">You can add these parameters to a sensitive information type query:</span></span>

-   <span data-ttu-id="d71de-213">개수 범위 - 문서가 쿼리 결과에 포함되기 위해 포함해야 하는 중요한 정보가 나오는 횟수를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-213">Count range — define the number of occurrences of sensitive information a document needs to contain before it’s included in the query results.</span></span>

-   <span data-ttu-id="d71de-214">신뢰도 범위 - 검색된 중요한 유형이 실제로 일치하는 신뢰도 수준[예: 85(85%)]을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-214">Confidence range — the level of confidence that the detected sensitive type is actually a match, such as 85 (85%).</span></span>

<span data-ttu-id="d71de-215">구문:</span><span class="sxs-lookup"><span data-stu-id="d71de-215">Syntax:</span></span>

-   <span data-ttu-id="d71de-216">SensitiveType:”\<type\>|\<count range\>|\<confidence range\>”</span><span class="sxs-lookup"><span data-stu-id="d71de-216">SensitiveType:”\<type\>|\<count range\>|\<confidence range\>”</span></span>

<span data-ttu-id="d71de-217">예제:</span><span class="sxs-lookup"><span data-stu-id="d71de-217">Examples:</span></span>

-   <span data-ttu-id="d71de-218">SensitiveType:“Credit Card Number|5” (정확히 5개의 카드 번호와 일치하는 문서만 반환)</span><span class="sxs-lookup"><span data-stu-id="d71de-218">SensitiveType:“Credit Card Number|5” (return only documents that contain exactly five credit card numbers)</span></span>

-   <span data-ttu-id="d71de-p115">SensitiveType:“Credit Card Number|\*|85..” (신뢰도 범위는 85% 이상임)</span><span class="sxs-lookup"><span data-stu-id="d71de-p115">SensitiveType:“Credit Card Number|\*|85..” (confidence range is 85 percent or higher)</span></span>

<span data-ttu-id="d71de-221">참고: "SensitiveType"은 대/소문자를 구분하지만 쿼리의 나머지 부분은 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d71de-221">Note: “SensitiveType” is case sensitive, but the rest of the query is not.</span></span>

<span data-ttu-id="d71de-p116">또한 속성 및 연산자를 사용하여 쿼리를 구체화하는 방법을 보여줄 수도 있습니다. 자세한 내용 및 예제에 대해서는 [사이트에 저장된 중요한 데이터를 찾기 위한 쿼리 작성](https://support.office.com/ko-KR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d71de-p116">You can also use properties, and operators to illustrate how you can refine your queries. For more information and examples, see [Form a query to find sensitive data stored on sites](https://support.office.com/ko-KR/article/Form-a-query-to-find-sensitive-data-stored-on-sites-3019fbc5-7f15-4972-8d0e-dc182dc7f836).</span></span>
