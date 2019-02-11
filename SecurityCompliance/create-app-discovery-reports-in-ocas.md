---
title: Office 365 Cloud App Security을 사용하여 앱 검색 보고서 만들기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Office 365 및 다른 응용 프로그램 사용자 조직에서 사용 하는 방법을 이해할 수 있도록 하는 Office 365 클라우드 앱 보안이 포함 된 보고서를 만듭니다.
ms.openlocfilehash: 543a194ec9d441a4feea97b8ad49022094565d7a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603719"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="5efee-103">Office 365 Cloud App Security을 사용하여 앱 검색 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="5efee-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

<span data-ttu-id="5efee-104">Office 365 고급 보안 관리 Office 365 클라우드 응용 프로그램 보안 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="5efee-105">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5efee-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="5efee-106">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5efee-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="5efee-107">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5efee-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="5efee-108">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5efee-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="5efee-109">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="5efee-110">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="5efee-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="5efee-111">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="5efee-112">여기는!</span><span class="sxs-lookup"><span data-stu-id="5efee-112">You are here!</span></span>  <br/> [<span data-ttu-id="5efee-113">다음 단계</span><span class="sxs-lookup"><span data-stu-id="5efee-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="5efee-p101">Office 365 클라우드 앱 보안 전역 관리자, 보안 관리자 및 보안 독자 사용자가 조직에서 사용 하는 클라우드 서비스에 대 한 정보를 얻을 수 있습니다. 예 및 데이터의 양을 앱 또는 Office 365 외부에 있는 서비스에 업로드 되는 사용자를 저장 하 고 문서에서 공동 작업을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="5efee-116">앱 검색 보고서를 생성 하려면 수동으로 웹 트래픽 로그 파일에서 방화벽 및 프록시를가 업로드 하 고 Office 365 클라우드 앱 보안 구문 분석 하 고 보고서에 대 한 해당 파일을 분석 하 여 다음 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-116">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5efee-p102">이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자, 보안 관리자 또는 보안 판독기 이어야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="5efee-119">응용 프로그램 검색을 사용 하 여 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="5efee-119">Create a report with app discovery</span></span>

<span data-ttu-id="5efee-120">응용 프로그램 검색 보고서를 만들려면를 분석 로그 파일을 선택한 다음 보고서를 요청 하려는 로그 파일에 대 한 공급 업체 데이터 소스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-120">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5efee-121">조직에서 사용 현황의 최상의 표현을 가져올 최대 트래픽을 기간을 포함 하는 웹 트래픽 로그 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-121">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="5efee-122">사용자 [웹 트래픽 로그 및 Office 365 클라우드 응용 프로그램 보안에 대 한 데이터 원본을](web-traffic-logs-and-data-sources-for-ocas.md)수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-122">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="5efee-123">클라우드 응용 프로그램 보안 포털에 이동 ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))에 로그인 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-123">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="5efee-124">**검색** 을 선택 \> **새 보고서 만들기**.</span><span class="sxs-lookup"><span data-stu-id="5efee-124">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="5efee-125">![Office 365 CAS 포털에서 검색을 선택](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="5efee-125">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="5efee-126">이름 및 사용자 보고서에 대 한 설명을 지정 하 고 **데이터 원본** 목록에서 웹 트래픽 로그에 대 한 데이터 원본을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-126">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="5efee-127">![O365 CA에서 검색을 선택 \> 새 보고서 만들기](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="5efee-127">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="5efee-p103">사용 하 여 원하는 데이터 원본 목록에 없는 경우 추가 될 요청할 수 있습니다. **데이터 원본**대 한 **기타** 를 선택 하 고 업로드 하려는 데이터 원본의 이름을 입력 합니다. 로그를 검토 하 고 사용 하는 것을 생성 하는 데이터 원본에 대 한 지원을 추가 하는 경우 알 수 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="5efee-p104">수집한 로그 파일의 위치를 찾아 해당 파일을 선택 합니다. 로그 파일은 보고서에 대해 선택한 데이터 원본에 의해 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="5efee-133">보고서 만들기 프로세스를 시작 하려면 **만들기** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-133">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="5efee-p105">다음은 보고서의 상태를 보려면 **Manage 스냅숏 보고서**를 클릭 합니다. 보고서 준비 되 면 **보고서 보기** 옵션을 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="5efee-136">다음 단계</span><span class="sxs-lookup"><span data-stu-id="5efee-136">Next steps</span></span>

- [<span data-ttu-id="5efee-137">검토 및 알림 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-137">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="5efee-138">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="5efee-138">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="5efee-139">[Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="5efee-139">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

