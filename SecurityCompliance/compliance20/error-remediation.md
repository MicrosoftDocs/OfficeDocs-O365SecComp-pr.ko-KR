---
title: 데이터를 처리할 때 오류 수정
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
description: ''
ms.openlocfilehash: 5168196dcac8a2cb3809f43fabb470c0f64cd0f7
ms.sourcegitcommit: 73dcdafb15b462223d1a670c781db260eb73c2f5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/01/2019
ms.locfileid: "36048167"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="19583-102">데이터를 처리할 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="19583-102">Error remediation when processing data</span></span>

<span data-ttu-id="19583-103">오류 수정을 통해 eDiscovery 관리자는 고급 eDiscovery가 콘텐츠를 제대로 처리 하지 못하게 하는 데이터 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="19583-104">예를 들어 암호로 보호 된 파일은 파일을 잠그거나 암호화 한 후에 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="19583-105">오류 수정을 사용 하는 경우 eDiscovery 관리자는 이러한 오류와 함께 파일을 다운로드 하 고 암호 보호를 제거한 다음 재구성 된 파일을 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="19583-106">다음 워크플로를 사용 하 여 고급 eDiscovery 사례에서 오류가 발생 한 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="19583-107">처리 오류가 있는 파일을 수정 하는 오류 업데이트 관리 세션 만들기</span><span class="sxs-lookup"><span data-stu-id="19583-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="19583-108">다음 절차 중에 오류 수정 마법사를 언제 든 지 닫을 경우, **보기** 드롭다운 메뉴에서 **오류 remediations** 를 선택 하 여 **처리** 탭에서 오류 수정 세션으로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="19583-109">고급 eDiscovery 사례의 **처리** 탭에서 **보기** 드롭다운 메뉴의 **오류** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop-down menu.</span></span>

2. <span data-ttu-id="19583-110">오류 유형 또는 파일 형식 옆의 라디오 단추를 클릭 하 여 수정할 오류를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="19583-111">다음 예제에서는 암호로 보호 된 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="19583-112">**새 오류 수정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-112">Click **New error remediation**.</span></span>

    ![오류 수정](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="19583-114">오류 업데이트 관리 세션은 오류가 발생 한 파일을 Microsoft에서 제공한 Azure 저장소 위치로 복사 하 여 로컬 컴퓨터에 다운로드 하 여 수정 하는 준비 단계에서 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19583-114">The error remediation session starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![오류 수정 준비](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="19583-116">준비가 완료 되 면 **다음: 파일 다운로드** 를 클릭 하 여 다운로드를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![파일 다운로드](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="19583-118">파일을 다운로드 하려면 **다운로드 대상 경로**를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="19583-119">파일을 다운로드 하는 로컬 컴퓨터의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="19583-119">This is a path on your local computer where the file will be downloaded.</span></span>  <span data-ttu-id="19583-120">기본 경로인%USERPROFILE%\Downloads\errors는 로그인 한 사용자의 다운로드 폴더를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="19583-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="19583-121">필요한 경우이 경로를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-121">You can change this path if necessary.</span></span> <span data-ttu-id="19583-122">이 작업을 변경 하는 경우에는 원격 네트워크 경로 대신 로컬 파일 경로를 사용 하 여 성능을 최적화 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-122">If you do change it, we recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

6. <span data-ttu-id="19583-123">**클립보드에 복사를**클릭 하 여 미리 정의 된 명령을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-123">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="19583-124">Windows 명령 프롬프트를 시작 하 고 명령을 붙여 넣은 다음 enter 키 \*\*\*\* 를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="19583-124">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="19583-125">파일이 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19583-125">The files are downloaded.</span></span>

    ![오류 수정 준비](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="19583-127">**파일 다운로드** 페이지에 제공 된 명령을 정상적으로 사용 하려면 AzCopy v 8.1을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-127">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="19583-128">또한 아래의 10 단계에서 AzCopy v 8.1을 사용 하 여 파일을 업로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-128">You also must use AzCopy v8.1 to upload the files in step 10 below.</span></span> <span data-ttu-id="19583-129">이 버전의 AzCopy을 설치 하려면 [Windows의 AzCopy v 8.1을 사용 하 여 데이터 전송을](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19583-129">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="19583-130">제공 된 AzCopy 명령이 실패 하면 [Advanced eDiscovery에서 AzCopy 문제 해결](troubleshooting-azcopy.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19583-130">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="19583-131">파일을 다운로드 한 후에는 적절 한 도구를 사용 하 여 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-131">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="19583-132">암호로 보호 된 파일의 경우에는 여러 가지 암호 해독 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-132">For password-protected files, there several password cracking tools you can use.</span></span> <span data-ttu-id="19583-133">파일에 대 한 암호를 알고 있으면 열고 암호 보호 기능을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-133">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="19583-134">Tact에서 재구성 된 파일의 디렉터리 구조와 파일 이름은 유지 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-134">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="19583-135">다운로드 한 파일 및 폴더에 사용 되는 모든 명명 규칙을 통해 remdiated 파일을 다시 원본에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-135">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="19583-136">이제 고급 eDiscovery로 돌아간 후 **다음: 파일 업로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-136">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="19583-137">이렇게 하면 이제 파일을 업로드할 수 있는 다음 단계로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-137">This will move to the next step where you can now upload the files.</span></span>

    ![파일 업로드](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="19583-139">**파일 위치 경로** 텍스트 상자에 재구성 된 파일의 위치를 지정 하 고 **클립보드에 복사를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-139">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="19583-140">Windows 명령 프롬프트에 명령을 붙여 넣고 enter 키를 \*\*\*\* 눌러 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-140">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6-.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="19583-142">Advanced eDiscovery로 돌아간 후 **다음: 프로세스 파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19583-142">Return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="19583-143">처리가 완료 되 면</span><span class="sxs-lookup"><span data-stu-id="19583-143">When processing is complete.</span></span>  <span data-ttu-id="19583-144">검토 집합으로 돌아가 재구성 된 파일을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19583-144">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="19583-145">파일을 수정 하는 경우 수행 되는 작업</span><span class="sxs-lookup"><span data-stu-id="19583-145">What happens when files are remediated</span></span>

<span data-ttu-id="19583-146">재구성 한 파일을 업로드 하면 다음 필드를 제외 하 고 원래 메타 데이터가 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19583-146">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="19583-147">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="19583-147">ExtractedTextSize</span></span>
- <span data-ttu-id="19583-148">HasText</span><span class="sxs-lookup"><span data-stu-id="19583-148">HasText</span></span>
- <span data-ttu-id="19583-149">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="19583-149">IsErrorRemediate</span></span>
- <span data-ttu-id="19583-150">LoadId</span><span class="sxs-lookup"><span data-stu-id="19583-150">LoadId</span></span>
- <span data-ttu-id="19583-151">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="19583-151">ProcessingErrorMessage</span></span>
- <span data-ttu-id="19583-152">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="19583-152">ProcessingStatus</span></span>
- <span data-ttu-id="19583-153">텍스트</span><span class="sxs-lookup"><span data-stu-id="19583-153">Text</span></span>
- <span data-ttu-id="19583-154">WordCount</span><span class="sxs-lookup"><span data-stu-id="19583-154">WordCount</span></span>
- <span data-ttu-id="19583-155">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="19583-155">WorkingsetId</span></span>

<span data-ttu-id="19583-156">Advanced eDiscovery의 모든 문서 메타 데이터 필드에 대 한 정의는 [문서 메타 데이터 필드](document-metadata-fields.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="19583-156">For a definition of all document metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
