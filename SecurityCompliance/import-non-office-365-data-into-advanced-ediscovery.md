---
title: 고급 eDiscovery 분석을 위해 비 Office 365 콘텐츠 가져오기
ms.author: chrfox
author: chrfox
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: AeD로 분석할 수 있도록 O365에 저장 되지 않은 콘텐츠를 Azure blob로 가져오는 방법에 대해 설명 하는 방법
ms.openlocfilehash: 1c971c9f95d03d05db76f80344adeb93b0a72c06
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152690"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a><span data-ttu-id="6246f-103">고급 eDiscovery 분석을 위해 비 Office 365 콘텐츠 가져오기</span><span class="sxs-lookup"><span data-stu-id="6246f-103">Import non-Office 365 content for Advanced eDiscovery analysis</span></span>

<span data-ttu-id="6246f-104">Office 365 Advanced eDiscovery를 사용 하 여 분석 해야 하는 모든 문서는 Office 365에 살고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-104">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="6246f-105">고급 eDiscovery의 Office가 아닌 365 콘텐츠 가져오기 기능을 사용 하는 경우 PST 파일을 제외한 Office 365에 없는 문서를 연결 된 Azure storage blob에 업로드 하 고 고급 eDiscovery로 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-105">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 (except PST files) into a case linked, Azure storage blob and analyze them with Advanced eDiscovery.</span></span> <span data-ttu-id="6246f-106">이 절차에서는 분석을 위해 비 Office 365 문서를 고급 eDiscovery로 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-106">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6246f-p102">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6246f-109">Office가 아닌 365 콘텐츠에 대 한 Office 365 Advanced eDiscovery 데이터 저장소 추가 기능 구독을 구매할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-109">You can purchase an Office 365 Advanced eDiscovery data storage add-on subscription for your non-Office 365 content.</span></span> <span data-ttu-id="6246f-110">이 기능은 고급 eDiscovery를 사용 하 여 분석 되는 콘텐츠에 대해서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-110">This is exclusively available for content that is to be analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="6246f-111">[비즈니스용 office 365에 대 한 구매 또는 편집 및 추가 기능](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) 의 단계를 따르고 Office 365 Advanced eDiscovery 저장소 추가 기능을 구입 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-111">Follow the steps in [Buy or edit and add-on for Office 365 for business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) and purchase the Office 365 Advanced eDiscovery storage add-on.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="6246f-112">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="6246f-112">Before you begin</span></span>

<span data-ttu-id="6246f-113">이 절차에 설명 된 대로 Office 이외에 업로드 365 기능을 사용 하려면 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-113">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
  
- <span data-ttu-id="6246f-114">고급 규정 준수 추가 기능 또는 E5 구독이 포함 된 Office 365 E3</span><span class="sxs-lookup"><span data-stu-id="6246f-114">An Office 365 E3 with Advanced Compliance add-on or E5 subscription</span></span>
    
- <span data-ttu-id="6246f-115">비 Office 365 콘텐츠가 업로드 되는 모든 custodians에는 고급 준수 추가 기능 또는 E5 라이선스가 포함 된 E3이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-115">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses</span></span>
    
- <span data-ttu-id="6246f-116">기존 eDiscovery 사례</span><span class="sxs-lookup"><span data-stu-id="6246f-116">An existing eDiscovery case</span></span>
    
- <span data-ttu-id="6246f-117">업로드 하기 위한 모든 파일은 custodian 마다 폴더가 하나이 고 폴더 이름이이 형식 *별칭 @ domainname* 에 있는 폴더로 수집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-117">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format  *alias@domainname*  .</span></span> <span data-ttu-id="6246f-118">*Alias @ domainname* 은 사용자의 Office 365 별칭 및 도메인 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-118">The  *alias@domainname*  must be users Office 365 alias and domain.</span></span> <span data-ttu-id="6246f-119">모든 *alias @ domainname* 폴더를 루트 폴더로 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-119">You can collect all the  *alias@domainname*  folders into a root folder.</span></span> <span data-ttu-id="6246f-120">루트 폴더에는 *별칭 @ domainname* 폴더만 포함할 수 있으며 루트 폴더에는 느슨한 파일이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-120">The root folder can only contain the  *alias@domainname*  folders, there must be no loose files in the root folder</span></span> 
    
- <span data-ttu-id="6246f-121">EDiscovery 관리자 또는 eDiscovery 관리자 인 계정</span><span class="sxs-lookup"><span data-stu-id="6246f-121">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>
    
- <span data-ttu-id="6246f-122">Office가 아닌 365 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 설치 된 [Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) 입니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-122">[Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) installed on a computer that has access to the non-Office 365 content folder structure.</span></span> 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="6246f-123">Office 이외의 365 콘텐츠를 고급 eDiscovery에 업로드</span><span class="sxs-lookup"><span data-stu-id="6246f-123">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="6246f-124">Ediscovery 관리자 또는 eDiscovery 관리자로 서 **ediscovery**를 열고 비 Office 365 데이터가 업로드 될 사례를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-124">As an eDiscovery Manager or eDiscovery Administrator, open **eDiscovery**, and open the case that the non-Office 365 data will be uploaded to.</span></span> <span data-ttu-id="6246f-125">사례를 만들어야 하는 경우 [에는 Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례 관리](manage-ediscovery-cases.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6246f-125">If you need to create a case, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md)</span></span>
    
2. <span data-ttu-id="6246f-126">**고급 eDiscovery로 전환을 클릭 합니다** .</span><span class="sxs-lookup"><span data-stu-id="6246f-126">Click **Switch to Advanced eDiscovery**</span></span>
    
3. <span data-ttu-id="6246f-127">**원본 형식** 아래에서 **비 Office 365 데이터**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-127">Under **Source type** select **Non-Office 365 data**.</span></span>
    
4. <span data-ttu-id="6246f-128">**컨테이너 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-128">Click **Add container**.</span></span> <span data-ttu-id="6246f-129">컨테이너의 이름을 입력 하 고 설명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-129">Name the container and add a description.</span></span>
    
5. <span data-ttu-id="6246f-130">컨테이너 목록에서 새로 추가 된 컨테이너를 선택 하 고 컨테이너 세부 정보 창에 표시 되는 URL을 복사한 다음 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-130">Select the newly added container from the container list and copy the URL that appears in the container details pane and then close the pane</span></span>
    
6. <span data-ttu-id="6246f-131">관리자 권한으로 명령 프롬프트를 열고 AzCopy이 설치 된 폴더로 디렉터리를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-131">Open a command prompt as an administrator and change directory to folder where you have AzCopy installed..</span></span>
    
7. <span data-ttu-id="6246f-132">AzCopy 명령줄을 구성 하 여 다음과 같은 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-132">Construct the AzCopy command line to upload the files like this:</span></span>
    
    <span data-ttu-id="6246f-133">AzCopy/Source: " *로컬 컴퓨터의 루트 폴더* 에 대 한 전체 경로"/dest: " *컨테이너 URL까지* (으)로 이동 하 고?</span><span class="sxs-lookup"><span data-stu-id="6246f-133">AzCopy /Source:" *full path to root folder on local machine*  " /Dest:"  *container URL up to but not including the ?*</span></span>  <span data-ttu-id="6246f-134">"/DestSAS:"의 *컨테이너 url의 나머지 부분은? 끝* "/S.</span><span class="sxs-lookup"><span data-stu-id="6246f-134">" /DestSAS:"  *remainder of the container url from the ? to the end*  " /S.</span></span> 
    
    <span data-ttu-id="6246f-135">예를 들어 다음 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-135">For example, using these values:</span></span> 
    
  - <span data-ttu-id="6246f-136">루트 폴더-C:\Collected 데이터</span><span class="sxs-lookup"><span data-stu-id="6246f-136">root folder - C:\Collected Data</span></span> 
    
  - <span data-ttu-id="6246f-137">컨테이너 url- https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;Si = NonOfficeData15% 7C0&amp;sig = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA% 3d</span><span class="sxs-lookup"><span data-stu-id="6246f-137">container url - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D</span></span>
    
    <span data-ttu-id="6246f-138">AzCopy 명령줄 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-138">the AzCopy command line syntax would be:</span></span>
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    <span data-ttu-id="6246f-139">Azcopy 구문에 대 한 자세한 내용은 [Windows의 Azcopy을 사용 하 여 데이터 전송](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6246f-139">For more information on Azcopy syntax see, [Transfer data with the AzCopy on Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6246f-140">사용자 마다 루트 폴더가 1 개 있어야 하며 폴더 이름은 *alias @ domainname* 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-140">There must be one root folder per user and the folder name must be in the  *alias@domainname*  format.</span></span> 
  
8. <span data-ttu-id="6246f-141">폴더 업로드가 완료 되 면 고급 eDiscovery로 다시 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-141">Once the folders have finished uploading, switch back to Advanced eDiscovery.</span></span> <span data-ttu-id="6246f-142">업로드 한 폴더의 콘텐츠를 이제 고급 eDiscovery에서 처리할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-142">The content in the folders you uploaded is now ready to be processed in Advanced eDiscovery.</span></span> <span data-ttu-id="6246f-143">컨테이너를 선택 하 고 처리 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-143">Select the container and click the Process button.</span></span> <span data-ttu-id="6246f-144">고급 eDiscovery 처리에 대 한 자세한 내용은 [Office 365 Advanced ediscovery에서 프로세스 모듈 실행 및 데이터 로드](run-the-process-module-and-load-data-in-advanced-ediscovery.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6246f-144">For more details on Advanced eDiscovery Processing see, [Run the Process module and load data in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="6246f-145">고급 eDiscovery에서 컨테이너를 성공적으로 처리 하면 더 이상 Azure의 SAS 저장소에 새 콘텐츠를 추가할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-145">Once the container is successfully processed in Advanced eDiscovery, you will no longer be able to add new content to the SAS storage in Azure.</span></span> <span data-ttu-id="6246f-146">추가 콘텐츠를 수집 하 고 고급 eDiscovery 분석을 위해 사례에 추가 하려는 경우에는 365 Office가 아닌 새 데이터 컨테이너를 만들고이 절차를 반복 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-146">If you collect additional content and you want to add it to the case for Advanced eDiscovery analysis, you must create a new **Non-Office 365 data** container and repeat this procedure.</span></span> 
  
    > [!NOTE]
    > <span data-ttu-id="6246f-147">*폴더 명명 문제로 인해 컨테이너가 제대로 처리 되지* 않는 경우 문제를 해결 하는 경우에도이 문서의 절차에 따라 새 컨테이너를 만들고 다시 연결 하 고 업로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6246f-147">If the container  *does not process successfully due to folder naming issues*  and you then fix the issues, you will still have to create a new container and the reconnect and upload again using the procedures in this article.</span></span> 
  

