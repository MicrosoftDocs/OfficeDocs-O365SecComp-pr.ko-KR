---
title: 조사를 위해 데이터를 처리할 때의 오류 수정
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
ms.openlocfilehash: b78a8e45ffb0833dec5116ff637cd0930387ebfe
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258866"
---
# <a name="error-remediation-when-processing-data-for-an-investigation"></a><span data-ttu-id="72e8a-102">조사를 위해 데이터를 처리할 때의 오류 수정</span><span class="sxs-lookup"><span data-stu-id="72e8a-102">Error remediation when processing data for an investigation</span></span>

<span data-ttu-id="72e8a-103">오류 수정을 통해 데이터 조사 (미리 보기)가 콘텐츠를 제대로 처리 하지 않도록 하는 데이터 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-103">Error remediation allows investigators the ability to rectify data issues which prevent Data Investigations (Preview) from properly processing the content.</span></span> <span data-ttu-id="72e8a-104">예를 들어 암호로 보호 된 파일은 파일을 잠그거나 암호화 한 후에 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-104">For example, files that are password protected cannot be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="72e8a-105">오류 수정을 사용 하 여 investigators에서 이러한 오류가 발생 한 파일을 다운로드 하 고, 암호 보호를 제거 하 고, 재구성 된 파일을 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-105">Using error remediation, investigators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="72e8a-106">다음 워크플로를 사용 하 여 데이터 조사 (미리 보기) 사례에서 오류가 발생 한 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-106">Use the following workflow to remediate files with errors in Data Investigations (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="72e8a-107">처리 오류가 발생 한 파일을 수정 하기 위한 오류 업데이트 관리 세션 만들기</span><span class="sxs-lookup"><span data-stu-id="72e8a-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="72e8a-108">다음 절차 중에 오류 수정 마법사를 언제 든 지 닫을 경우, **보기** 드롭다운 메뉴에서 **오류 remediations** 를 선택 하 여 **처리** 탭에서 오류 수정 세션으로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="72e8a-109">데이터 조사 (미리 보기) 사례의 **처리** 탭에 있는 **보기** 드롭다운 메뉴에서 **오류** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-109">On the **Processing** tab in an Data Investigations (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="72e8a-110">오류 유형 또는 파일 형식 옆의 라디오 단추를 클릭 하 여 수정할 오류를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="72e8a-111">다음 예제에서는 암호로 보호 된 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="72e8a-112">**+ 새 오류 수정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-112">Click **+ New error remediation**.</span></span>

    ![오류 수정](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="72e8a-114">errored 파일을 다운로드 하기 위한 안전한 Azure 위치로 이동 하는 준비 단계부터 시작 하 여 오류 업데이트 관리 세션이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![오류 수정 준비](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="72e8a-116">준비가 완료 되 면 **다음: 파일 다운로드** 를 클릭 하 여 다운로드를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![파일 다운로드](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="72e8a-118">파일을 다운로드 하려면 **다운로드할 대상 경로**를 지정 합니다. 로컬 컴퓨터에서 파일을 다운로드 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-118">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.</span></span>  <span data-ttu-id="72e8a-119">기본 경로인%USERPROFILE%\Downloads\errors은 로그인 한 사용자의 다운로드 폴더를 가리킵니다. 이는 필요에 따라 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-119">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="72e8a-120">최적의 성능을 위해 원격 네트워크 경로 대신 로컬 파일 경로를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72e8a-121">AzCopy을 설치 하지 않은 경우 여기에서 설치할 수 있습니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="72e8a-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="72e8a-122">**클립보드에 복사를**클릭 하 여 미리 정의 된 명령을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-122">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="72e8a-123">windows 명령 프롬프트를 시작 하 고 명령을 붙여 넣은 다음 enter 키 \*\*\*\* 를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-123">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="72e8a-124">파일이 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-124">The files will be downloaded.</span></span>

    ![오류 수정 준비](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > <span data-ttu-id="72e8a-126">이 명령을 실행 하는 데 문제가 있는 경우 https://go.microsoft.com/fwlink/?linkid=2038117 문제 해결 팁을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e8a-126">If you have issues running this command, see https://go.microsoft.com/fwlink/?linkid=2038117 for troubleshooting tips.</span></span>

7. <span data-ttu-id="72e8a-127">파일을 다운로드 한 후에는 적절 한 도구를 사용 하 여 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-127">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="72e8a-128">암호로 보호 된 파일의 경우에는 다양 한 암호 해독 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-128">For password protected files, there are a number of password cracking tools you can use.</span></span> <span data-ttu-id="72e8a-129">파일에 대 한 암호를 알고 있으면 열고 암호 보호 기능을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-129">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="72e8a-130">tact에서 재구성 된 파일의 디렉터리 구조와 파일 이름은 유지 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-130">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="72e8a-131">다운로드 한 파일 및 폴더에 사용 되는 모든 명명 규칙을 통해 remdiated 파일을 다시 원본에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-131">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="72e8a-132">이제 데이터 조사 (미리 보기)로 돌아가 **다음: 파일 업로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-132">Now, return to Data Investigations (Preview) and click **Next: Upload files**.</span></span>  <span data-ttu-id="72e8a-133">이렇게 하면 이제 파일을 업로드할 수 있는 다음 단계로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-133">This will move to the next step where you can now upload the files.</span></span>

    ![파일 업로드](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="72e8a-135">**파일 위치 경로** 텍스트 상자에 재구성 된 파일의 위치를 지정한 다음 **clibpboard에 복사를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="72e8a-136">Windows 명령 프롬프트에 명령을 붙여 넣고 enter 키를 \*\*\*\* 눌러 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6-.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="72e8a-138">마지막으로 데이터 조사 (미리 보기)로 돌아가 **다음: 프로세스 파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-138">Finally, return to Data Investigations (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="72e8a-139">처리가 완료 되 면</span><span class="sxs-lookup"><span data-stu-id="72e8a-139">When processing is complete.</span></span>  <span data-ttu-id="72e8a-140">작업 집합으로 돌아가 재구성 된 파일을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-140">You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="72e8a-141">파일을 수정 하는 경우 수행 되는 작업</span><span class="sxs-lookup"><span data-stu-id="72e8a-141">What happens when files are remediated</span></span>

<span data-ttu-id="72e8a-142">재구성 한 파일을 업로드 하면 다음 필드를 제외 하 고 원래 메타 데이터가 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e8a-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="72e8a-143">DocumentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="72e8a-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="72e8a-144">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="72e8a-144">ExtractedTextSize</span></span>
- <span data-ttu-id="72e8a-145">HasText</span><span class="sxs-lookup"><span data-stu-id="72e8a-145">HasText</span></span>
- <span data-ttu-id="72e8a-146">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="72e8a-146">IsErrorRemediate</span></span>
- <span data-ttu-id="72e8a-147">IsParentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="72e8a-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="72e8a-148">ItemExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="72e8a-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="72e8a-149">LoadId</span><span class="sxs-lookup"><span data-stu-id="72e8a-149">LoadId</span></span>
- <span data-ttu-id="72e8a-150">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="72e8a-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="72e8a-151">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="72e8a-151">ProcessingStatus</span></span>
- <span data-ttu-id="72e8a-152">텍스트</span><span class="sxs-lookup"><span data-stu-id="72e8a-152">Text</span></span>
- <span data-ttu-id="72e8a-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="72e8a-153">WordCount</span></span>
- <span data-ttu-id="72e8a-154">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="72e8a-154">WorkingsetId</span></span>

<span data-ttu-id="72e8a-155">데이터 조사 (미리 보기)의 모든 문서 메타 데이터 필드에 대 한 정의를 보려면 [문서 메타 데이터 필드](document-metadata-fields.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e8a-155">For a definition of all document metadata fields in Data Investigations (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>