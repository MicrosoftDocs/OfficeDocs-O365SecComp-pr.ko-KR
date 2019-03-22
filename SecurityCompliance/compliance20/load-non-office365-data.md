---
title: 작업 집합에 비 Office 365 데이터 로드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 7a27da4b8932d9bef268de897d9a992d8b87bdef
ms.sourcegitcommit: cf9d9b545a7c153d314aa9c08c7fb16fcd785b3e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30737668"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="a7f9e-102">작업 집합에 비 Office 365 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="a7f9e-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="a7f9e-103">office 365 Advanced eDiscovery를 사용 하 여 분석 해야 하는 모든 문서는 office 365에 살고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-103">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="a7f9e-104">고급 ediscovery의 office가 아닌 365 콘텐츠 가져오기 기능을 사용 하 여 office 365에 없는 문서를 고급 ediscovery로 분석 하도록 작업 집합에 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-104">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="a7f9e-105">이 절차에서는 분석을 위해 비 Office 365 문서를 고급 eDiscovery로 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-105">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="a7f9e-106">고급 eDiscovery를 사용 하려면 조직의 고급 준수 추가 기능 또는 E5 구독에 Office 365 E3이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-106">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="a7f9e-107">고급 eDiscovery를 만들려고 하는 계획이 없는 경우 Office 365 Enterprise E5의 평가판에 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-107">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="a7f9e-108">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="a7f9e-108">Before you begin</span></span>
<span data-ttu-id="a7f9e-109">이 절차에 설명 된 대로 Office 이외에 업로드 365 기능을 사용 하려면 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="a7f9e-110">고급 규정 준수 추가 기능 또는 E5 구독을 포함 하는 Office 365 E3</span><span class="sxs-lookup"><span data-stu-id="a7f9e-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="a7f9e-111">비 Office 365 콘텐츠가 업로드 되는 모든 custodians에는 고급 규정 준수 추가 기능 또는 E5 라이선스가 포함 된 E3이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="a7f9e-112">기존 eDiscovery 사례</span><span class="sxs-lookup"><span data-stu-id="a7f9e-112">An existing eDiscovery case.</span></span>

- <span data-ttu-id="a7f9e-113">업로드 하기 위한 모든 파일은 custodian 마다 폴더가 하나이 고 폴더 이름이이 형식 *별칭 @ domainname* 에 있는 폴더로 수집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-113">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* .</span></span> <span data-ttu-id="a7f9e-114">*alias @ domainname* 은 사용자의 Office 365 별칭 및 도메인 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-114">The *alias@domainname* must be users Office 365 alias and domain.</span></span> <span data-ttu-id="a7f9e-115">모든 *alias @ domainname* 폴더를 루트 폴더로 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-115">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="a7f9e-116">루트 폴더에는 *별칭 @ domainname* 폴더만 포함할 수 있으며 루트 폴더에는 느슨한 파일이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-116">The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

   <span data-ttu-id="a7f9e-117">업로드할 계획인 비 Office 365 데이터에 대 한 폴더 구조는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-117">The folder structure for the non-Office 365 data you plan to upload should look something like the following:</span></span>

   - <span data-ttu-id="a7f9e-118">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="a7f9e-118">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="a7f9e-119">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="a7f9e-119">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="a7f9e-120">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="a7f9e-120">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="a7f9e-121">여기서 abraham.mcmahon@contoso.com, jewell.gordon@contoso.com 및 staci.gonzalez@contoso.com는 custodians의 SMTP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-121">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are SMTP addresses of custodians in the case.</span></span>

- <span data-ttu-id="a7f9e-122">비 Office 365 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 ediscovery 관리자 또는 ediscovery 관리자 Microsoft Azure Storage Tools가 설치 되어 있는 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-122">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="a7f9e-123">다음에서 수행할 수 있는 AzCopy을 설치 합니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="a7f9e-123">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="a7f9e-124">Office 이외의 365 콘텐츠를 고급 eDiscovery에 업로드</span><span class="sxs-lookup"><span data-stu-id="a7f9e-124">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="a7f9e-125">ediscovery 관리자 또는 ediscovery 관리자로 서, 고급 eDiscovery를 열고 비 Office 365 데이터가 업로드 되는 사례를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-125">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="a7f9e-126">**작업 집합** 탭을 클릭 한 다음 비 Office 365 데이터를 로드할 작업 집합을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-126">Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="a7f9e-127">작업 집합을 아직 만들지 않은 경우 지금 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-127">If you have not already created a working set, you can do so now.</span></span>  <span data-ttu-id="a7f9e-128">마지막으로, 기능 **설정 관리** 를 클릭 한 다음 비 Office 365 데이터 섹션에서 **업로드 보기**</span><span class="sxs-lookup"><span data-stu-id="a7f9e-128">Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="a7f9e-129">**파일 업로드** 단추를 클릭 하 여 비 Office 365 데이터 가져오기 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-129">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![파일 업로드](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="a7f9e-131">마법사의 첫 번째 단계에서는 업로드할 파일에 대 한 안전한 Azure blob만 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-131">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="a7f9e-132">준비가 완료 되 면 **다음: 파일 업로드** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-132">Once preparation is compelted, click the **Next: Upload files** button.</span></span>

![비 Office 365 가져오기-준비](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="a7f9e-134">**파일 업로드** 단계에서 **파일의 위치에 대 한 경로**를 지정 합니다. 여기서는 가져오기에 사용 하는 비 Office 365 데이터가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-134">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="a7f9e-135">올바른 위치를 설정 하면 AzCopy 명령이 제대로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-135">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="a7f9e-136">AzCopy을 아직 설치 하지 않은 경우 여기에서이 작업을 수행할 수 있습니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="a7f9e-136">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="a7f9e-137">**클립보드에 복사** 링크를 클릭 하 여 미리 정의 된 명령을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-137">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="a7f9e-138">windows 명령 프롬프트를 시작 하 고 명령을 붙여 넣은 다음 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-138">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="a7f9e-139">파일이 보안 Azure blob 저장소에 업로드 되 고 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-139">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Office가 아닌 365 가져오기-업로드 파일](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![비 Office 365 가져오기-AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

> [!NOTE]
> <span data-ttu-id="a7f9e-142">제공 된 AzCopy 명령이 실패 하면 [Advanced eDiscovery (Preview)에서 AzCopy 문제 해결](troubleshooting-azcopy.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-142">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery (Preview)](troubleshooting-azcopy.md)</span></span>

6. <span data-ttu-id="a7f9e-143">마지막으로 보안 & 규정 준수로 돌아간 후 **다음: 프로세스 파일** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-143">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="a7f9e-144">이렇게 하면 업로드 된 파일의 처리, 텍스트 추출 및 인덱싱이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-144">This will initiate processing, text extraction and indexing of the uploaded files.</span></span>  <span data-ttu-id="a7f9e-145">여기에서 처리의 진행 상황과 **작업** 탭을 추적할 수 있습니다.  완료 되 면 새 파일을 작업 집합에서 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-145">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.</span></span>  <span data-ttu-id="a7f9e-146">처리가 완료 되 면 마법사를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-146">Once processing is complete, you can dismiss the wizard.</span></span>

![Office가 아닌 365 가져오기 프로세스 파일](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

