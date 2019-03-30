---
title: Office 365에서 법적 조사 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e
description: 조직의 법적 조사를 관리 하려면 Office 365의 Security & 준수 센터에서 eDiscovery 사례를 사용 합니다. E5 구독이 있는 경우에는 고급 eDiscovery의 텍스트 분석, 기계 학습 및 예측 코딩 기능을 사용 하 여 사례 데이터를 보다 자세히 분석할 수 있습니다.
ms.openlocfilehash: 5bfa4719f2bb065a7064e7dc9d02778a4d032da8
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999921"
---
# <a name="manage-legal-investigations-in-office-365"></a><span data-ttu-id="95e30-104">Office 365에서 법적 조사 관리</span><span class="sxs-lookup"><span data-stu-id="95e30-104">Manage legal investigations in Office 365</span></span>

<span data-ttu-id="95e30-105">조직에는 조직의 특정 임원 또는 다른 직원과 관련 된 법적 사례에 대응 해야 하는 여러 가지 이유가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-105">Organizations have many reasons to respond to a legal case involving certain executives or other employees in your organization.</span></span> <span data-ttu-id="95e30-106">이 작업을 수행 하는 동안에는 해당 일상 업무 작업에 사람들이 사용 하는 전자 메일, 문서, 인스턴트 메시징 대화 및 기타 콘텐츠 위치에서 특정 정보를 빠르게 찾고 보존 하는 작업이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-106">This might involve quickly finding and retaining for further investigation specific information in email, documents, instant messaging conversations, and other content locations used by people in their day-to-day work tasks.</span></span> <span data-ttu-id="95e30-107">보안 & 준수 센터의 eDiscovery 사례 도구를 사용 하 여 이러한 작업과 비슷한 여러 가지 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-107">You can perform these and many other similar activities by using the eDiscovery case tools in the Security & Compliance Center.</span></span>
  
[<span data-ttu-id="95e30-108">eDiscovery 사례를 사용 하 여 법적 조사 관리</span><span class="sxs-lookup"><span data-stu-id="95e30-108">Manage legal investigations with eDiscovery cases</span></span>](#manage-legal-investigations-with-ediscovery-cases)
  
[<span data-ttu-id="95e30-109">Office 365 Advanced eDiscovery를 사용 하 여 사례 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="95e30-109">Analyze case data using Office 365 Advanced eDiscovery</span></span>](#analyze-case-data-using-office-365-advanced-ediscovery)
  
<span data-ttu-id="95e30-110">**Microsoft에서 eDiscovery 조사를 관리 하는 방법을 알고 싶으십니까?**</span><span class="sxs-lookup"><span data-stu-id="95e30-110">**Want to know how Microsoft manages its eDiscovery investigations?**</span></span> <span data-ttu-id="95e30-111">이 문서에서는 내부 eDiscovery 워크플로를 관리 하기 위해 동일한 Office 365 검색 및 조사 도구를 사용 하는 방법에 대해 설명 하는 [기술 백서](https://go.microsoft.com/fwlink/?linkid=852161) 를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-111">Here's a [technical white paper](https://go.microsoft.com/fwlink/?linkid=852161) you can download that explains how we use the same Office 365 search and investigation tools to manage our internal eDiscovery workflow.</span></span>
   
## <a name="manage-legal-investigations-with-ediscovery-cases"></a><span data-ttu-id="95e30-112">eDiscovery 사례를 사용 하 여 법적 조사 관리</span><span class="sxs-lookup"><span data-stu-id="95e30-112">Manage legal investigations with eDiscovery cases</span></span>

<span data-ttu-id="95e30-113">ediscovery 사례를 사용 하면 조직에서 ediscovery 사례를 만들고, 액세스 하 고, 관리할 수 있는 사용자를 제어할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-113">eDiscovery cases let you control who can create, access, and manage eDiscovery cases in your organization.</span></span> <span data-ttu-id="95e30-114">사례를 사용 하 여 구성원을 추가 하 고 수행할 수 있는 작업 유형을 제어 하 고, 법적 사례와 관련 된 콘텐츠 위치를 유지 하 고, 콘텐츠 검색 도구를 사용 하 여 해당 사례에 응답할 수 있는 콘텐츠에 대해 보류 중인 위치를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-114">Use cases to add members and control what types of actions they can perform, place a hold on content locations relevant to a legal case, and use the Content Search tool to search the locations on hold for content that might be responsive to your case.</span></span> <span data-ttu-id="95e30-115">그런 다음 외부 검토자의 추가 조사를 위해 해당 결과를 내보내고 다운로드할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-115">Then you can also export and download those results for further investigation by external reviewers.</span></span> <span data-ttu-id="95e30-116">Office 365 조직에 E5 구독이 있는 경우 고급 eDiscovery에서 분석에 대 한 검색 결과를 준비할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-116">If your Office 365 organization has an E5 subscription, you can also prepare search results for analysis in Advanced eDiscovery.</span></span>
  
- <span data-ttu-id="95e30-117">조직이 수행 해야 하는 모든 법률 조사에 대해 ediscovery 사례를 만들고 사용 하 여 [ediscovery 워크플로를 관리 합니다](ediscovery-cases.md) .</span><span class="sxs-lookup"><span data-stu-id="95e30-117">[Manage your eDiscovery workflow](ediscovery-cases.md) by creating and using eDiscovery cases for every legal investigation your organization has to undertake</span></span> 
    
- <span data-ttu-id="95e30-118">조직에서 ediscovery 사례를 만들고 관리할 수 있는 사용자를 제어 하기 위해 [ediscovery 권한 할당](assign-ediscovery-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="95e30-118">[Assign eDiscovery permissions](assign-ediscovery-permissions.md) to control who can create and manage eDiscovery cases in your organization</span></span> 
    
- <span data-ttu-id="95e30-119">eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치를 제어 하는 [준수 경계를 설정](set-up-compliance-boundaries.md) 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-119">[Set up compliance boundaries](set-up-compliance-boundaries.md) to control the user content locations that eDiscovery managers can search</span></span> 
    
- <span data-ttu-id="95e30-120">조직의 [콘텐츠 검색](search-for-content.md)</span><span class="sxs-lookup"><span data-stu-id="95e30-120">[Search for content](search-for-content.md) in your organization</span></span> 
    
- <span data-ttu-id="95e30-121">advanced [ediscovery에 대 한 사례 콘텐츠 준비](prepare-search-results-for-advanced-ediscovery.md) 고급 ediscovery의 강력한 분석 도구 (예: 광학 인식, 전자 메일 스레딩 및 예측 코딩)를 사용 하 여 분석을 수행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-121">[Prepare case content for Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md) so you can perform analysis using Advanced eDiscovery's powerful analytic tools, such as optical character recognition, email threading, and predictive coding</span></span> 
    
### <a name="use-scripts-for-advanced-scenarios"></a><span data-ttu-id="95e30-122">고급 시나리오에 스크립트 사용</span><span class="sxs-lookup"><span data-stu-id="95e30-122">Use scripts for advanced scenarios</span></span>

<span data-ttu-id="95e30-123">콘텐츠 검색 시나리오에 대 한 스크립트를 나열 하는 이전 섹션에서와 마찬가지로 eDiscovery 사례를 관리 하는 데 도움이 되는 몇 가지 보안 & 준수 센터 PowerShell 스크립트도 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-123">Like the previous section that listed scripts for content search scenarios, we've also created some Security & Compliance Center PowerShell scripts to help you manage eDiscovery cases.</span></span>
  
- <span data-ttu-id="95e30-124">조직의 ediscovery 사례와 관련 된 모든 보류에 대 한 정보가 포함 된 [eDiscovery 보류 보고서를 만듭니다](create-a-report-on-holds-in-ediscovery-cases.md) .</span><span class="sxs-lookup"><span data-stu-id="95e30-124">[Create a eDiscovery hold report](create-a-report-on-holds-in-ediscovery-cases.md) that contains information about all holds associated with eDiscovery cases in your organization</span></span> 
    
- <span data-ttu-id="95e30-125">eDiscovery 보류에 사용자 목록에 대 한 [사서함 및 OneDrive 위치 추가](use-a-script-to-add-users-to-a-hold-in-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="95e30-125">[Add mailboxes and OneDrive locations](use-a-script-to-add-users-to-a-hold-in-ediscovery.md) for a list of users to an eDiscovery hold</span></span> 
  
## <a name="analyze-case-data-using-office-365-advanced-ediscovery"></a><span data-ttu-id="95e30-126">Office 365 Advanced eDiscovery를 사용 하 여 사례 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="95e30-126">Analyze case data using Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="95e30-127">Office 365 Advanced eDiscovery는 이전 섹션에서 설명한 콘텐츠 검색 및 eDiscovery 기능을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-127">Office 365 Advanced eDiscovery builds on the content search and eDiscovery capabilities described in the previous sections.</span></span> <span data-ttu-id="95e30-128">eDiscovery 사례를 만들고 custodian 위치를 보류 한 후 사례에 응답할 수 있는 데이터를 수집 하 고 나면 텍스트 분석, 기계 학습 및 고급의 예측 코딩 기능을 사용 하 여 데이터를 상세히 분석할 수 있습니다. eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="95e30-128">After you create an eDiscovery case, place custodian locations on hold, and collect data that might be responsive to the case, you can then further analyze the data by using the text analytics, machine learning, and the predictive coding capabilities of Advanced eDiscovery.</span></span> <span data-ttu-id="95e30-129">이를 통해 조직에서 수천 개의 전자 메일 메시지, 문서 및 기타 종류의 데이터를 빠르게 처리 하 여 특정 사례와 관련성이 가장 높은 항목을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-129">This can help your organization quickly process thousands of email messages, documents, and other kinds of data to find those items that are most likely relevant to a specific case.</span></span> <span data-ttu-id="95e30-130">또한 보안 & 준수 센터에서 동일한 대/소문자를 완벽 하 게 관리할 수 있도록 통합 사례 관리 및 고급 eDiscovery가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-130">And, we've unified case management and Advanced eDiscovery so that you can seamlessly manage the same case within the Security & Compliance Center.</span></span>
  
> [!NOTE]
> <span data-ttu-id="95e30-131">고급 eDiscovery를 사용 하 여 사용자 데이터를 분석 하려면 데이터의 custodian 사용자에 게 Office 365 E5 라이선스를 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-131">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license.</span></span> <span data-ttu-id="95e30-132">또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자에 게 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-132">Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license.</span></span> <span data-ttu-id="95e30-133">서비스 케이스에 할당 되 고 고급 eDiscovery를 사용 하 여 데이터를 분석 하는 관리자 및 규정 준수 직원은 E5 라이선스가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-133">Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
  
### <a name="get-started"></a><span data-ttu-id="95e30-134">시작</span><span class="sxs-lookup"><span data-stu-id="95e30-134">Get started</span></span>

<span data-ttu-id="95e30-135">고급 ediscovery를 시작 하는 가장 빠른 방법은 사례를 만들고 보안 & 준수 센터에서 검색 결과를 준비한 후 advanced ediscovery에서 결과를 로드 한 다음, 빠른 분석을 실행 하 여 사례 데이터를 분석 하 고 결과를 내보내는 것입니다. 외부 리뷰에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-135">The quickest way to get started with Advanced eDiscovery is to create a case and prepare search results in Security & Compliance Center, load those results in Advanced eDiscovery, and then run Express analysis to analyze that case data and then export the results for external review.</span></span>
  
- <span data-ttu-id="95e30-136">고급 eDiscovery 워크플로에 대 한 [간략 한 개요 보기](quick-setup-for-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="95e30-136">[Get a quick overview](quick-setup-for-advanced-ediscovery.md) of the Advanced eDiscovery workflow</span></span> 
    
- <span data-ttu-id="95e30-137">보안 & 준수 센터를 사용 하 여 사례를 만들고, eDiscovery 권한을 할당 하 고, 사례 구성원을 추가 하 여 고급 eDiscovery에 대 한 [사용자 및 사례를 설정](set-up-users-and-cases-in-advanced-ediscovery.md) 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-137">[Set up users and cases](set-up-users-and-cases-in-advanced-ediscovery.md) for Advanced eDiscovery by creating a case, assigning eDiscovery permissions, and adding case members, all by using the Security & Compliance Center</span></span> 
    
- <span data-ttu-id="95e30-138">Advanced eDiscovery에서 사례에 대 한 [검색 데이터 준비 및 로드](prepare-data-for-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="95e30-138">[Prepare and load search data](prepare-data-for-advanced-ediscovery.md) in to the case in Advanced eDiscovery</span></span> 
    
- <span data-ttu-id="95e30-139">고급 eDiscovery에서 분석을 위해 [비 Office 365 데이터](import-non-office-365-data-into-advanced-ediscovery.md) 를 사례에 로드</span><span class="sxs-lookup"><span data-stu-id="95e30-139">[Load non-Office 365 data](import-non-office-365-data-into-advanced-ediscovery.md) in to a case to analyze it in Advanced eDiscovery</span></span> 
    
- <span data-ttu-id="95e30-140">[빠른 분석을 사용](use-express-analysis-in-advanced-ediscovery.md) 하 여 사례에서 데이터를 빠르게 분석 한 다음 결과를 쉽게 내보내기</span><span class="sxs-lookup"><span data-stu-id="95e30-140">[Use Express analysis](use-express-analysis-in-advanced-ediscovery.md) to quickly analyze the data in a case and then easily export the results</span></span> 
    
### <a name="analyze-data"></a><span data-ttu-id="95e30-141">데이터 분석</span><span class="sxs-lookup"><span data-stu-id="95e30-141">Analyze data</span></span>

<span data-ttu-id="95e30-142">고급 eDiscovery의 사례에 검색 데이터를 로드 한 후에는 Analyze 모듈을 사용 하 여 분석을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-142">After search data is loaded into the case in Advanced eDiscovery, you'll use the Analyze module to start analyzing it.</span></span> <span data-ttu-id="95e30-143">분석 프로세스의 첫 번째 부분은 파일을 고유한 파일 그룹, 중복 항목 및 거의 모든 이름 (문서 유사성으로 인식)으로 구성 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-143">The first part of the analysis process consists of organizing files into groups of unique files, duplicates, and near-duplicates (also know as document similarity).</span></span> <span data-ttu-id="95e30-144">그런 다음 데이터를 계층적으로 구성 된 전자 메일 스레드 및 테마 그룹으로 구성 하 고 필요에 따라 ignore 텍스트 필터를 설정 하 여 특정 텍스트를 분석에서 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-144">Then you'll organize the data again into hierarchically structured groups of email threads and themes and, optionally, set ignore text filters to exclude certain text from analysis.</span></span> <span data-ttu-id="95e30-145">그런 다음 분석을 실행 하 고 결과를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-145">Then you'll run the analysis and view the results.</span></span>
  
- <span data-ttu-id="95e30-146">고급 eDiscovery에서 데이터를 분석 하기 위한 준비를 위해 [문서 유사성에 대해 자세히 알아봅니다](understand-document-similarity-in-advanced-ediscovery.md) .</span><span class="sxs-lookup"><span data-stu-id="95e30-146">[Learn about document similarity](understand-document-similarity-in-advanced-ediscovery.md) to prepare you for analyzing data in Advanced eDiscovery</span></span> 
    
- <span data-ttu-id="95e30-147">유사 복제, 테마 및 전자 메일 스레딩에 대 한 [옵션을 설정](set-analyze-options-in-advanced-ediscovery.md) 하 고 Analyze 모듈을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-147">[Set up the options](set-analyze-options-in-advanced-ediscovery.md) for near-duplicates, themes, and email threading and then run the Analyze module</span></span> 
    
- <span data-ttu-id="95e30-148">[무시 텍스트 필터를 설정](set-ignore-text-in-advanced-ediscovery.md) 하 여 텍스트 및 텍스트 문자열이 분석 되지 않도록 합니다. 관련성 분석을 실행 하면 이러한 필터도 텍스트를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-148">[Set up Ignore Text filters](set-ignore-text-in-advanced-ediscovery.md) to exclude text and text strings from being analyzed; these filters will also ignore text when you run Relevance analysis</span></span> 
    
- <span data-ttu-id="95e30-149">분석 프로세스 [결과 보기](view-analyze-results-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="95e30-149">[View the results](view-analyze-results-in-advanced-ediscovery.md) of the analysis process</span></span> 
    
- <span data-ttu-id="95e30-150">분석 프로세스에 대 한 [고급 설정 구성](set-analyze-advanced-settings-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="95e30-150">[Configure advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for the analysis process</span></span> 
    
### <a name="set-up-relevance-training"></a><span data-ttu-id="95e30-151">관련성 교육 설정</span><span class="sxs-lookup"><span data-stu-id="95e30-151">Set up Relevance training</span></span>

<span data-ttu-id="95e30-152">고급 eDiscovery에서 예측 코딩 (관련성 이라고 함)은 소수의 문서 집합에 대 한 결정을 내릴 수 있도록 하 여 원하는 내용을 시스템에 교육 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-152">Predictive coding (called Relevance) in Advanced eDiscovery lets you train the system on what you're looking for by letting you to make decisions (about whether something is relevant or not) on a small set of documents.</span></span>
  
- <span data-ttu-id="95e30-153">관련성 교육 설정, 사례와 관련 된 파일 태그 지정 및 사례 문제 정의 [에 대해 자세히 알아보기](manage-relevance-setup-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="95e30-153">[Learn about setting up Relevance training](manage-relevance-setup-in-advanced-ediscovery.md) , tagging files that are relevant to a case, and defining case issues</span></span> 
    
- <span data-ttu-id="95e30-154">[사례 문제를 정의](define-issues-and-assign-users.md) 하 고 파일을 교육할 사용자에 게 각 문제를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-154">[Define case issues](define-issues-and-assign-users.md) and assign each issue to a user who will train the files</span></span> 
    
- <span data-ttu-id="95e30-155">[가져온 파일을 관련성 교육에 추가할 현재 또는 새 부하에 추가](set-up-loads-to-add-imported-files.md) 합니다. 부하는 사례에 추가 된 다음 관련성 성향 습득에 사용 되는 새로운 파일 배치입니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-155">[Add imported files to current or new load](set-up-loads-to-add-imported-files.md) that will be added to the Relevance training; a load is a new batch of files that are added to a case and then used for Relevance training</span></span> 
    
- <span data-ttu-id="95e30-156">관련성 교육에 추가할 수 있는 [강조 표시 된 키워드를 정의](define-highlighted-keywords-and-advanced-options.md) 합니다. 이를 통해 사례와 관련 된 파일을 보다 효율적으로 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-156">[Define highlighted keywords](define-highlighted-keywords-and-advanced-options.md) that can be added to the Relevance training; this helps you better identify files that are relevant to a case</span></span> 
    
### <a name="run-the-relevance-module"></a><span data-ttu-id="95e30-157">관련성 모듈 실행</span><span class="sxs-lookup"><span data-stu-id="95e30-157">Run the Relevance module</span></span>

<span data-ttu-id="95e30-158">교육을 설정 하 고 나면 관련성 모듈을 실행 하 고 교육 설정의 효과를 평가할 수 있습니다 .이로 인해 추가 교육을 수행 해야 할지 아니면 파일 태그 지정을 시작할 준비가 되었는지 여부를 결정 하는 데 도움이 되는 관련성 순위가 지정 됩니다. 사용자 사례와 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-158">After set up training, you're ready to run the Relevance module and assess the effectiveness of the training settings This results in a relevance ranking that helps you decide if you need to perform additional training or if you're ready to start tagging files as relevant to your case.</span></span>
  
- <span data-ttu-id="95e30-159">샘플 파일 집합을 기반으로 하는 관련성 프로세스 및 평가, 태그 지정, 추적 및 다시 교육 프로세스 [에 대해 알아봅니다](use-relevance-in-advanced-ediscovery.md) .</span><span class="sxs-lookup"><span data-stu-id="95e30-159">[Learn about the Relevance process](use-relevance-in-advanced-ediscovery.md) and the iterative process of assessment, tagging, tracking, and re-training based on sample set of files</span></span> 
    
- <span data-ttu-id="95e30-160">사례에 익숙한 전문가가 사례 파일 집합을 검토 하 고 관련성 교육의 효율성을 확인 하는 [평가에 대해 알아봅니다](assessment-in-relevance-in-advanced-ediscovery.md) .</span><span class="sxs-lookup"><span data-stu-id="95e30-160">[Learn about assessment](assessment-in-relevance-in-advanced-ediscovery.md) , where a expert familiar with the case reviews a set of case files and determines the effectiveness of the Relevance training</span></span> 
    
- <span data-ttu-id="95e30-161">[사례 파일을 평가](tagging-and-assessment-in-advanced-ediscovery.md) 하 여 교육 설정의 효율성 ( *다양성* )을 계산 하 고 해당 사례와 관련성이 있거나 관련이 없는 파일에 태그를 적용 합니다. 이렇게 하면 현재 교육이 충분 한지 또는 교육 설정을 조정 해야 하는지 쉽게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-161">[Assess case files](tagging-and-assessment-in-advanced-ediscovery.md) to calculate the effectiveness (called  *richness*  ) of training settings, and then tag files as relevant or not relevant to your case; this helps you determine if the current training is sufficient or if you should adjust the training settings.</span></span> 
    
- <span data-ttu-id="95e30-162">평가가 완료 된 후 [관련성 교육을 수행한](tagging-and-relevance-training-in-advanced-ediscovery.md) 다음, 사례에 대해 정의한 문제와 관련이 있거나 관련성이 없는 파일을 다시 태그 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-162">[Perform the relevance training](tagging-and-relevance-training-in-advanced-ediscovery.md) after assessment is complete, and then once again tag files as relevant or not relevant to the issues you've defined for the case</span></span> 
    
- <span data-ttu-id="95e30-163">관련성 분석 프로세스를 추적 하 여 관련성 교육이 평가 대상 ( *안정적인 교육 상태* 라고 함)을 달성 했는지, 더 많은 교육이 필요한 지를 확인 [합니다](track-relevance-analysis-in-advanced-ediscovery.md) . 또한 각 사례 문제에 대 한 관련성 결과를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-163">[Track the Relevance analysis](track-relevance-analysis-in-advanced-ediscovery.md) process to determine if Relevance training has achieved your assessment target (known as a  *stable training status*  ) or whether more training is needed; you can also view the Relevance results for each case issue</span></span> 
    
- <span data-ttu-id="95e30-164">검토를 위해 내보낼 수 있는 사례 파일의 결과 집합 크기를 결정 하기 위한 [관련성 분석에 따라 결정](decision-based-on-the-results-in-advanced-ediscovery.md) 을 내립니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-164">[Make decisions based on Relevance analysis](decision-based-on-the-results-in-advanced-ediscovery.md) to determine the size of the resulting set of case files that can be exported for review</span></span> 
    
- <span data-ttu-id="95e30-165">관련성 [분석의 품질을 테스트](test-relevance-analysis-in-advanced-ediscovery.md) 하 여 관련성 프로세스 중에 수행 된 culling 결정 사항 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="95e30-165">[Test the quality of the Relevance analysis](test-relevance-analysis-in-advanced-ediscovery.md) to validate the culling decisions made during the Relevance process</span></span> 
    
### <a name="export-results"></a><span data-ttu-id="95e30-166">결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="95e30-166">Export results</span></span>

<span data-ttu-id="95e30-167">Advanced eDiscovery에서 사례 데이터를 분석 하는 마지막 단계는 외부 검토에 대 한 분석 결과를 내보내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-167">The final step in analyzing case data in Advanced eDiscovery is to export results of the analysis for external review.</span></span>
  
- [<span data-ttu-id="95e30-168">사례 데이터 내보내기에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="95e30-168">Learn about exporting case data</span></span>](export-case-data-in-advanced-ediscovery.md)
    
- [<span data-ttu-id="95e30-169">사례 데이터 내보내기</span><span class="sxs-lookup"><span data-stu-id="95e30-169">Export case data</span></span>](export-results-in-advanced-ediscovery.md)
    
- [<span data-ttu-id="95e30-170">일괄 처리 기록 보기 및 이전 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="95e30-170">View batch history and export past results</span></span>](view-batch-history-and-export-past-results.md)
    
- [<span data-ttu-id="95e30-171">보고서 필드 내보내기</span><span class="sxs-lookup"><span data-stu-id="95e30-171">Export report fields</span></span>](export-report-fields-in-advanced-ediscovery.md)
    
### <a name="other-advanced-ediscovery-tools"></a><span data-ttu-id="95e30-172">기타 고급 eDiscovery 도구</span><span class="sxs-lookup"><span data-stu-id="95e30-172">Other Advanced eDiscovery tools</span></span>

<span data-ttu-id="95e30-173">고급 eDiscovery에서는 사례 데이터, 관련성 분석 및 데이터 내보내기에 대 한 추가 도구 및 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="95e30-173">Advanced eDiscovery provides additional tools and capabilities beyond analyzing case data, relevance analysis, and exporting data.</span></span>
  
- [<span data-ttu-id="95e30-174">고급 eDiscovery 보고서 실행</span><span class="sxs-lookup"><span data-stu-id="95e30-174">Run Advanced eDiscovery reports</span></span>](run-reports-in-advanced-ediscovery.md)
    
- [<span data-ttu-id="95e30-175">사례 및 테 넌 트 설정 정의</span><span class="sxs-lookup"><span data-stu-id="95e30-175">Define case and tenant settings</span></span>](define-case-and-tenant-settings-in-advanced-ediscovery.md)
    
- [<span data-ttu-id="95e30-176">고급 eDiscovery 유틸리티</span><span class="sxs-lookup"><span data-stu-id="95e30-176">Advanced eDiscovery utilities</span></span>](use-advanced-ediscovery-utilities.md)
