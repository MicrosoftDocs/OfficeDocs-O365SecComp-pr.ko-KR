---
title: 검토 집합에 비 Office 365 데이터 로드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 고급 eDiscovery 사례에서 Office 이외 365 데이터를 검토 집합으로 가져옵니다.
ms.openlocfilehash: d7609c774e7c8a42e24b22a87fbed271a12a97f5
ms.sourcegitcommit: 73dcdafb15b462223d1a670c781db260eb73c2f5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/01/2019
ms.locfileid: "36048110"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="7d6e3-103">검토 집합에 비 Office 365 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="7d6e3-103">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="7d6e3-104">고급 eDiscovery에서 분석 하는 데 필요한 모든 문서가 Office 365에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-104">Not all documents that you need to analyze in Advanced eDiscovery are located in Office 365.</span></span> <span data-ttu-id="7d6e3-105">고급 eDiscovery의 비 Office 365 데이터 가져오기 기능을 사용 하 여 Office 365에 없는 문서를 검토 집합에 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-105">With the non-Office 365 data import feature in Advanced eDiscovery, you can upload documents that aren't located in Office 365 to a review set.</span></span> <span data-ttu-id="7d6e3-106">이 문서에서는 분석을 위해 비 Office 365 문서를 고급 eDiscovery로 가져오는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-106">This article shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="7d6e3-107">고급 eDiscovery에는 조직에 대 한 Microsoft 365 또는 Office 365 E5 구독 또는 고급 준수 추가 기능 구독이 포함 된 E3 구독이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-107">Advanced eDiscovery requires an Microsoft 365 or Office 365 E5 subscription for your organization or an E3 subscription with the Advanced Compliance add-on subscription.</span></span> <span data-ttu-id="7d6e3-108">고급 eDiscovery를 만들려고 하는 계획이 없는 경우 Office 365 Enterprise E5의 평가판에 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-108">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="7d6e3-109">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="7d6e3-109">Before you begin</span></span>

<span data-ttu-id="7d6e3-110">이 문서에서 설명 하는 Office 이외 365 업로드 기능을 사용 하려면 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-110">Using the upload non-Office 365 feature described in this article requires that you have the following:</span></span>

- <span data-ttu-id="7d6e3-111">비 Office 365 콘텐츠를 연결 하려는 모든 custodians에는 E5 라이선스 또는 고급 준수 추가 기능 라이선스가 포함 된 E3 라이선스가 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-111">All custodians that you want to associate non-Office 365 content to must be assigned an E5 license, or an E3 license with an Advanced Compliance add-on license.</span></span>

- <span data-ttu-id="7d6e3-112">기존 고급 eDiscovery 사례</span><span class="sxs-lookup"><span data-stu-id="7d6e3-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="7d6e3-113">비 Office 365 데이터를 업로드 하 고 여기에 연결 하려면 Custodians를 사례에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-113">Custodians must be added to the case before you can upload and associate the non-Office 365 data to them.</span></span>

- <span data-ttu-id="7d6e3-114">Office가 아닌 365 데이터는 고급 eDiscovery에서 지 원하는 파일 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-114">Non-Office 365 data must be a file type that's supported by Advanced eDiscovery.</span></span> <span data-ttu-id="7d6e3-115">자세한 내용은 [Advanced eDiscovery에서 지원 되는 파일 형식을](supported-filetypes-ediscovery20.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-115">For more information, see [Supported file types in Advanced eDiscovery](supported-filetypes-ediscovery20.md).</span></span>

- <span data-ttu-id="7d6e3-116">검토 집합에 업로드 되는 모든 파일은 각 폴더가 특정 custodian 연결 되는 폴더에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-116">All files that are uploaded to a review set must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="7d6e3-117">이러한 폴더의 이름은 *alias @ domainname*을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-117">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="7d6e3-118">Alias @ domainname은 사용자의 Office 365 별칭 및 도메인 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-118">The alias@domainname must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="7d6e3-119">루트 폴더에 있는 모든 alias @ domainname 폴더를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-119">You can collect all the alias@domainname folders in a root folder.</span></span> <span data-ttu-id="7d6e3-120">루트 폴더에는 alias @ domainname 폴더만 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-120">The root folder can only contain the alias@domainname folders.</span></span> <span data-ttu-id="7d6e3-121">루트 폴더의 느슨한 파일은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-121">Loose files in the root folder aren't supported.</span></span>

   <span data-ttu-id="7d6e3-122">업로드할 비 Office 365 데이터에 대 한 폴더 구조는 다음 예와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-122">The folder structure for the non-Office 365 data that you want to upload would be similar to the following example:</span></span>

   - <span data-ttu-id="7d6e3-123">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7d6e3-123">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="7d6e3-124">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7d6e3-124">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="7d6e3-125">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7d6e3-125">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="7d6e3-126">여기서 abraham.mcmahon@contoso.com, jewell.gordon@contoso.com 및 staci.gonzalez@contoso.com는 대/소문자에서 custodians의 SMTP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-126">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Office가 아닌 365 데이터 업로드 폴더 구조](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="7d6e3-128">EDiscovery 관리자 역할 그룹에 할당 되 고 eDiscovery 관리자로 추가 된 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-128">An account that is assigned to the eDiscovery Manager role group (and added as eDiscovery Administrator).</span></span>

- <span data-ttu-id="7d6e3-129">Office가 아닌 365 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 설치 된 AzCopy v 8.1 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-129">The AzCopy v8.1 tool installed on a computer that has access to the non-Office 365 content folder structure.</span></span> <span data-ttu-id="7d6e3-130">AzCopy을 설치 하려면 [Windows의 AzCopy v 8.1을 사용 하 여 데이터 전송을](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-130">To install AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="7d6e3-131">기본 위치인 **% ProgramFiles (x86)% \ Microsoft SDKs\Azure\AzCopy**에 AzCopy을 (를) 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-131">Be sure to install AzCopy in the default location, which is **%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy**.</span></span> <span data-ttu-id="7d6e3-132">AzCopy v 8.1을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-132">You must use AzCopy v8.1.</span></span> <span data-ttu-id="7d6e3-133">고급 eDiscovery에서 비 Office 365 데이터를 로드할 때 다른 버전의 AzCopy 작동 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-133">Other versions of AzCopy may not work when loading non-Office 365 data in Advanced eDiscovery.</span></span>


## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="7d6e3-134">Office 이외의 365 콘텐츠를 고급 eDiscovery에 업로드</span><span class="sxs-lookup"><span data-stu-id="7d6e3-134">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="7d6e3-135">EDiscovery 관리자 또는 eDiscovery 관리자로 서, 고급 eDiscovery를 열고 비 Office 365 데이터가 업로드 되는 사례를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-135">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  

2. <span data-ttu-id="7d6e3-136">**검토 집합**을 클릭 한 다음 검토 집합을 선택 하 여 비 Office 365 데이터를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-136">Click **Review sets**, and then select the review set to upload the non-Office 365 data to.</span></span>  <span data-ttu-id="7d6e3-137">검토 집합이 없는 경우에는 해당 집합을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-137">If you don't have a review set, you can create one.</span></span> 
 
3. <span data-ttu-id="7d6e3-138">검토 집합에서 **검토 설정 관리**를 클릭 한 다음 **비 Office 365 데이터** 타일에서 **업로드 보기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-138">In the review set, click **Manage review set**, and then click **View uploads** on the **Non-Office 365 data** tile.</span></span>

4. <span data-ttu-id="7d6e3-139">**파일 업로드** 를 클릭 하 여 비 Office 365 데이터 가져오기 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-139">Click **Upload files** to start the Non-Office 365 data import wizard.</span></span>

   ![파일 업로드](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

   <span data-ttu-id="7d6e3-141">마법사의 첫 번째 단계에서는 Microsoft에서 제공한 안전한 Azure 저장소 위치를 준비 하 여 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-141">The first step in the wizard prepares a secure Microsoft-provided Azure Storage location to upload the files to.</span></span>  <span data-ttu-id="7d6e3-142">준비가 완료 되 면 **다음: 파일 업로드** 단추가 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-142">When the preparation is completed, the **Next: Upload files** button becomes active.</span></span>

   ![비 Office 365 가져오기: 준비](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
5. <span data-ttu-id="7d6e3-144">**다음: 파일 업로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-144">Click **Next: Upload files**.</span></span>

6. <span data-ttu-id="7d6e3-145">**파일 업로드** 페이지에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-145">On the **Upload files** page, do the following:</span></span>

   ![비 Office 365 가져오기: 파일 업로드](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   <span data-ttu-id="7d6e3-147">위한.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-147">a.</span></span> <span data-ttu-id="7d6e3-148">**파일 위치 경로** 상자에서 업로드 하려는 비 Office 365 데이터를 저장 한 루트 폴더의 위치를 확인 하거나 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-148">In the **Path to location of files** box, verify or type the location of the root folder where you've stored the non-Office 365 data you want to upload.</span></span> <span data-ttu-id="7d6e3-149">예를 들어 **시작 하기 전에 구역**에 표시 된 예제 파일의 위치에는 **%USERPROFILE\Downloads\nonO365**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-149">For example, for the location of the example files shown in the **Before you begin section**, you would type **%USERPROFILE\Downloads\nonO365**.</span></span> <span data-ttu-id="7d6e3-150">올바른 위치를 제공 하면 경로 아래의 상자에 표시 되는 AzCopy 명령이 제대로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-150">Providing the correct location ensures the AzCopy command displayed in box under the path is properly updated.</span></span>

   <span data-ttu-id="7d6e3-151">b.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-151">b.</span></span> <span data-ttu-id="7d6e3-152">상자에 표시 된 명령을 복사 하려면 **클립보드에 복사** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-152">Click **Copy to clipboard** to copy the command that is displayed in the box.</span></span>

7. <span data-ttu-id="7d6e3-153">Windows 명령 프롬프트를 시작 하 고 이전 단계에서 복사한 명령을 붙여 넣은 다음 enter 키를 눌러 AzCopy \*\*\*\* 명령을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-153">Start a Windows command prompt, paste the command that you copied in the previous step, and then press **Enter** to start the AzCopy command.</span></span>  <span data-ttu-id="7d6e3-154">명령을 시작한 후에는 Office가 아닌 365 파일이 4 단계에서 준비 된 Azure 저장소 위치로 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-154">After you start the command, the non-Office 365 files will be uploaded to the Azure Storage location that was prepared in step 4.</span></span>

   ![비 Office 365 가져오기: AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="7d6e3-156">앞에서 설명한 것 처럼 AzCopy v 8.1을 사용 하 여 **파일 업로드** 페이지에 제공 된 명령을 성공적으로 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-156">As previously stated, you must use AzCopy v8.1 to successfully use the command that's provided on the **Upload files** page.</span></span> <span data-ttu-id="7d6e3-157">제공 된 AzCopy 명령이 실패 하면 [Advanced eDiscovery에서 AzCopy 문제 해결](troubleshooting-azcopy.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-157">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

8. <span data-ttu-id="7d6e3-158">보안 & 준수 센터로 돌아간 후 **다음: 마법사에서 프로세스 파일** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-158">Go back to the Security & Compliance Center, and click **Next: Process files** in the wizard.</span></span>  <span data-ttu-id="7d6e3-159">이렇게 하면 Azure 저장소 위치로 업로드 된 비 Office 365 파일의 처리, 텍스트 추출 및 인덱싱이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-159">This initiates processing, text extraction, and indexing of the non-Office 365 files that were uploaded to the Azure Storage location.</span></span>  

9. <span data-ttu-id="7d6e3-160">**검토 집합에 365 부재 중 365 데이터를 추가**하는 작업을 확인 하 여 **프로세스 파일** 페이지 또는 **작업** 탭에서 office 이외 범위의 파일 처리 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-160">Track the progress of processing the non-Office 365 files on the **Process files** page or on the **Jobs** tab by viewing a job named **Adding non-Office 365 data to a review set**.</span></span>  <span data-ttu-id="7d6e3-161">작업이 완료 되 면 검토 집합에서 새 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-161">After the job is finished, the new files will be available in the review set.</span></span>

   ![비 Office 365 가져오기: 프로세스 파일](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

10. <span data-ttu-id="7d6e3-163">처리가 완료 되 면 마법사를 닫을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d6e3-163">After the processing is finished, you can close the wizard.</span></span>