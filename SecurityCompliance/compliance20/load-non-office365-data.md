---
title: 검토 집합에 비 Office 365 데이터 로드
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
ms.openlocfilehash: 60775002d5ebec83aacbec350a044b9d6ffeb461
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834965"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="9076b-102">검토 집합에 비 Office 365 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="9076b-102">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="9076b-103">Office 365 Advanced eDiscovery를 사용 하 여 분석 해야 하는 모든 문서는 Office 365에 살고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-103">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="9076b-104">고급 eDiscovery의 Office가 아닌 365 콘텐츠 가져오기 기능을 사용 하는 경우 Office 365에 없는 문서를 검토 집합에 업로드 하 여 고급 eDiscovery로 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-104">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a review set so it is analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="9076b-105">이 절차에서는 분석을 위해 비 Office 365 문서를 고급 eDiscovery로 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-105">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="9076b-106">고급 eDiscovery를 사용 하려면 조직의 고급 준수 추가 기능 또는 E5 구독에 Office 365 E3이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-106">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="9076b-107">고급 eDiscovery를 만들려고 하는 계획이 없는 경우 Office 365 Enterprise E5의 평가판에 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-107">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="9076b-108">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="9076b-108">Before you begin</span></span>

<span data-ttu-id="9076b-109">이 문서에 설명 된 것 처럼 Office가 아닌 업로드 365 기능을 사용 하려면 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-109">Using the upload Non-Office 365 feature as described in this article requires that you have the following:</span></span>

- <span data-ttu-id="9076b-110">고급 준수 추가 기능 구독이 포함 된 Office 365 또는 Microsoft 365 E5 구독 또는 E3 구독</span><span class="sxs-lookup"><span data-stu-id="9076b-110">An Office 365 or Microsoft 365 E5 subscription or an E3 subscription with the Advanced Compliance add-on subscription.</span></span>

- <span data-ttu-id="9076b-111">비 Office 365 콘텐츠가 업로드 되는 모든 custodians에는 고급 준수 추가 기능 라이선스가 있는 E3 라이선스가 있거나 E5 라이선스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-111">All custodians whose non-Office 365 content will be uploaded must have E3 license with an Advanced Compliance add-on license or have an E5 license.</span></span>

- <span data-ttu-id="9076b-112">기존 고급 eDiscovery 사례</span><span class="sxs-lookup"><span data-stu-id="9076b-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="9076b-113">Custodians에 연결 된 비 Office 365 데이터를 업로드 하기 전에 케이스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-113">Custodians must be added to the case before you upload the non-Office 365 data that's associated to them.</span></span>

- <span data-ttu-id="9076b-114">업로드 될 모든 파일은 각 폴더가 특정 custodian 연결 된 폴더에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-114">All files that will be uploaded must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="9076b-115">이러한 폴더의 이름은 *alias @ domainname*을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-115">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="9076b-116">*Alias @ Domainname* 은 사용자의 Office 365 별칭 및 도메인 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-116">The *alias@domainname* must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="9076b-117">모든 *alias @ domainname* 폴더를 루트 폴더로 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-117">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="9076b-118">루트 폴더에는 *alias @ domainname* 폴더만 포함할 수 있습니다. 루트 폴더에는 느슨한 파일을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-118">The root folder can only contain the *alias@domainname* folders; loose files aren't allowed in the root folder.</span></span>

   <span data-ttu-id="9076b-119">예를 들어 업로드 하려는 비 Office 365 데이터의 폴더 구조는 다음과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-119">For example, the folder structure for the non-Office 365 data that you want to upload would be similar to the following:</span></span>

   - <span data-ttu-id="9076b-120">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9076b-120">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="9076b-121">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9076b-121">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="9076b-122">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9076b-122">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="9076b-123">여기서 abraham.mcmahon@contoso.com, jewell.gordon@contoso.com 및 staci.gonzalez@contoso.com는 대/소문자에서 custodians의 SMTP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-123">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Office가 아닌 365 데이터 업로드 폴더 구조](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="9076b-125">EDiscovery 관리자 또는 eDiscovery 관리자 인 계정</span><span class="sxs-lookup"><span data-stu-id="9076b-125">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>

- <span data-ttu-id="9076b-126">Office가 아닌 365 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 설치 된 Microsoft Azure Storage Tools입니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-126">Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="9076b-127">다음에서 수행할 수 있는 AzCopy을 설치 합니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="9076b-127">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="9076b-128">Office 이외의 365 콘텐츠를 고급 eDiscovery에 업로드</span><span class="sxs-lookup"><span data-stu-id="9076b-128">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="9076b-129">EDiscovery 관리자 또는 eDiscovery 관리자로 서, 고급 eDiscovery를 열고 비 Office 365 데이터가 업로드 되는 사례를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-129">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="9076b-130">**검토 집합** 탭을 클릭 한 다음 비 Office 365 데이터를 로드할 검토 집합을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-130">Click the **review sets** tab, then select the review set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="9076b-131">아직 검토 집합을 만들지 않은 경우 지금 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-131">If you have not already created a review set, you can do so now.</span></span>  <span data-ttu-id="9076b-132">마지막으로 **검토 설정 관리** 를 클릭 한 다음 \* \* 비 Office 365 데이터 타일에서 **업로드 보기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-132">Finally, click **Manage review set** and then click **View uploads** in the \*\*Non-Office 365 data tile.</span></span>

2. <span data-ttu-id="9076b-133">**파일 업로드** 단추를 클릭 하 여 비 Office 365 데이터 가져오기 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-133">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

   ![파일 업로드](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="9076b-135">마법사의 첫 번째 단계에서는 업로드할 파일에 대 한 안전한 Azure blob만 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-135">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="9076b-136">준비가 완료 되 면 **다음: 파일 업로드** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-136">Once preparation is completed, click the **Next: Upload files** button.</span></span>

   ![비 Office 365 가져오기-준비](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="9076b-138">**파일 업로드** 단계에서 **파일의 위치에 대 한 경로**를 지정 합니다. 여기서는 가져오기에 사용 하는 비 Office 365 데이터가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-138">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="9076b-139">올바른 위치를 설정 하면 AzCopy 명령이 제대로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-139">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

   > [!NOTE]
   > <span data-ttu-id="9076b-140">AzCopy을 아직 설치 하지 않은 경우 여기에서이 작업을 수행할 수 있습니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="9076b-140">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="9076b-141">**클립보드에 복사** 링크를 클릭 하 여 미리 정의 된 명령을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-141">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="9076b-142">Windows 명령 프롬프트를 시작 하 고 명령을 붙여 넣은 다음 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-142">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="9076b-143">파일이 보안 Azure blob 저장소에 업로드 되 고 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-143">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

   ![Office가 아닌 365 가져오기-업로드 파일](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   ![비 Office 365 가져오기-AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="9076b-146">제공 된 AzCopy 명령이 실패 하면 [Advanced eDiscovery에서 AzCopy 문제 해결](troubleshooting-azcopy.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9076b-146">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span></span>

6. <span data-ttu-id="9076b-147">마지막으로 보안 & 규정 준수로 돌아간 후 **다음: 프로세스 파일** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-147">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="9076b-148">이렇게 하면 업로드 된 파일의 처리, 텍스트 추출 및 인덱싱이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-148">This will initiate processing, text extraction and indexing of the uploaded files.</span></span>  <span data-ttu-id="9076b-149">여기에서 처리의 진행 상황과 **작업** 탭을 추적할 수 있습니다.  완료 되 면 새 파일을 검토 집합에서 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-149">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the review set.</span></span>  <span data-ttu-id="9076b-150">처리가 완료 되 면 마법사를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9076b-150">Once processing is complete, you can dismiss the wizard.</span></span>

   ![Office가 아닌 365 가져오기 프로세스 파일](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

