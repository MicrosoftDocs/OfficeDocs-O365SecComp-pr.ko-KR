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
description: office 365 Cloud App Security를 사용 하 여 보고서를 만들면 조직의 사용자가 office 365 및 기타 앱을 사용 하는 방법을 이해할 수 있습니다.
ms.openlocfilehash: e0d515ddd9b08aa4a70276177060f273cc89949e
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087297"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="5630b-103">Office 365 Cloud App Security을 사용하여 앱 검색 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="5630b-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="5630b-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5630b-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="5630b-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5630b-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="5630b-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="5630b-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="5630b-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5630b-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="5630b-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="5630b-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="5630b-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="5630b-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="5630b-110">배포 시작</span><span class="sxs-lookup"><span data-stu-id="5630b-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="5630b-111">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="5630b-111">You are here!</span></span>  <br/> [<span data-ttu-id="5630b-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="5630b-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="5630b-p101">Office 365 cloud App security는 전역 관리자, 보안 관리자 및 보안 독자에 게 조직에서 사용 중인 클라우드 서비스에 대 한 통찰력을 제공 합니다. 예를 들어 사용자가 문서를 저장 하 고 공동으로 작업 하는 위치와 Office 365 외부에 있는 앱 또는 서비스에 업로드 되는 데이터의 양을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="5630b-115">앱 검색 보고서를 생성 하려면 방화벽과 프록시에서 웹 트래픽 로그 파일을 수동으로 업로드 한 다음 Office 365 Cloud app Security에서 해당 파일을 구문 분석 하 고 분석 하 여 보고서를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-115">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5630b-p102">이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자, 보안 관리자 또는 보안 독자 여야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5630b-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="5630b-118">앱 검색을 사용 하 여 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="5630b-118">Create a report with app discovery</span></span>

<span data-ttu-id="5630b-119">앱 검색 보고서를 만들려면 분석 하려는 로그 파일의 공급 업체 데이터 원본을 식별 하 고, 로그 파일을 선택한 다음, 보고서를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-119">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5630b-120">최대 트래픽 기간을 포함 하는 웹 트래픽 로그 파일을 사용 하 여 조직에서 사용을 최상의 방법으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-120">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="5630b-121">[Office 365 Cloud App Security에 대 한 웹 트래픽 로그 및 데이터 원본을](web-traffic-logs-and-data-sources-for-ocas.md)수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-121">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="5630b-122">Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="5630b-123">**새 보고서 만들기** **검색** \> 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-123">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="5630b-124">![Office 365 CAS 포털에서 검색을 선택 합니다.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="5630b-124">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="5630b-125">보고서의 이름과 설명을 지정한 다음 **데이터 원본** 목록에서 웹 트래픽 로그의 데이터 원본을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-125">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="5630b-126">![O365 CAS에서 새 보고서 만들기 \> 검색을 선택 합니다.](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="5630b-126">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="5630b-p103">사용 하려는 데이터 원본이 나열 되지 않으면 추가 되도록 요청할 수 있습니다. **데이터 원본**에 대해 **기타** 를 선택한 다음 업로드 하려는 데이터 원본의 이름을 입력 합니다. 로그를 검토 하 고이를 생성 한 데이터 원본에 대 한 지원을 추가할 것인지를 알려 드리겠습니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="5630b-p104">수집한 로그 파일의 위치로 이동 하 여 해당 파일을 선택 합니다. 보고서에 대해 선택한 데이터 원본에서 로그 파일을 생성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="5630b-132">**만들기** 를 클릭 하 여 보고서 생성 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-132">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="5630b-p105">보고서의 상태를 보려면 **스냅숏 보고서 관리**를 클릭 합니다. 보고서가 준비 되 면 **보고서 보기** 옵션이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5630b-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="5630b-135">다음 단계</span><span class="sxs-lookup"><span data-stu-id="5630b-135">Next steps</span></span>

- [<span data-ttu-id="5630b-136">경고 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="5630b-136">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="5630b-137">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="5630b-137">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="5630b-138">[Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토</span><span class="sxs-lookup"><span data-stu-id="5630b-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

