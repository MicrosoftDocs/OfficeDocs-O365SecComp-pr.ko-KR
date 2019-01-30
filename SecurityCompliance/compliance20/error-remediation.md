---
title: 데이터를 처리할 때 오류 수정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608174"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="1fd11-102">데이터를 처리할 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="1fd11-102">Error remediation when processing data</span></span>

<span data-ttu-id="1fd11-p101">오류 수정 eDiscovery 관리자 고급 eDiscovery (미리 보기) 콘텐츠를 제대로 처리 하지 못하도록 하는 데이터 문제를 해결 하는 기능을 허용 합니다. 예, 파일은 잠겨 되거나 암호화 된 이후 암호로 보호 된 파일을 처리할 수 없습니다. 오류 업데이트 관리를 사용 하 여 eDiscovery 관리자 수 이러한 오류와 함께 파일을 다운로드, 암호 보호를 제거 하 고 remediated 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-p101">Error remediation allows eDiscovery administrators the ability to rectify data issues which prevent Advanced eDiscovery (Preview) from properly processing the content. For example, files that are password protected cannot be processed since the files are locked or encrypted. Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="1fd11-106">다음과 같은 워크플로 사용 하 여 고급 eDiscovery (미리 보기)의 경우에는 오류와 함께 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-106">Use the following workflow to remediate files with errors in Advanced eDiscovery (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="1fd11-107">오류 처리와 함께 파일을 수정 하는 오류 수정 세션 만들기 (영문)</span><span class="sxs-lookup"><span data-stu-id="1fd11-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="1fd11-108">하는 경우의 오류 수정 마법사는 다음 절차 중 언제 든 지 닫혀를 반환할 수 있습니다 오류 수정 세션에 **처리** 탭에서 **보기** 에 대 한 드롭다운 메뉴에서에서 **오류 개선** 를 선택 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="1fd11-109">고급 eDiscovery (미리 보기) 사례 **처리** 탭에서 **보기** 에 대 한 드롭다운 메뉴에서에서 **오류** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-109">On the **Processing** tab in an Advanced eDiscovery (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="1fd11-p102">오류 유형 또는 파일 형식 옆에 있는 라디오 단추를 클릭 하 여 수정 하려는 오류를 선택 합니다.  다음 예제에서는 암호로 보호 된 파일을 수정 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-p102">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.  In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="1fd11-112">**+ 새 오류 업데이트 관리를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-112">Click **+ New error remediation**.</span></span>

    ![오류 수정](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="1fd11-114">오류 수정 세션이 시작로 시작 하 여 준비 단계는 오류가 발생 하는 파일은 이동 되는 위치 Azure 안전한 위치에 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![오류 수정 준비](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="1fd11-116">준비 완료 되 면 클릭 **다음: 파일을 다운로드** 다운로드 계속 진행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![파일 다운로드](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="1fd11-p103">파일을 다운로드 하려면 **다운로드에 대 한 대상 경로**;를 지정 합니다. 파일을 다운로드 하 여 로컬 컴퓨터에 있는 경로입니다.  기본 경로 %USERPROFILE%\Downloads\errors, 로그인 한 사용자의 다운로드 폴더; 가리키는 필요에 따라 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-p103">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.  The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="1fd11-120">최적의 성능을 위해 원격 네트워크 경로 하는 대신 로컬 파일 경로 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1fd11-121">AzCopy를 설치 하지 않은 경우 여기에서 설치할 수 있습니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="1fd11-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="1fd11-p104">**클립보드에 복사**를 클릭 하 여 미리 정의 된 명령에 복사 합니다. Windows 명령 프롬프트를 시작 하 고 명령에 붙여넣은 다음 **Enter**키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-p104">Copy the predefined command by clicking **Copy to clipboard**. Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="1fd11-124">파일 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-124">The files will be downloaded.</span></span>

    ![오류 수정 준비](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > <span data-ttu-id="1fd11-126">이 명령을 실행 하는 문제를 사용 하는 경우 참조 https://go.microsoft.com/fwlink/?linkid=2038117 문제해결 팁입니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-126">If you have issues running this command, see https://go.microsoft.com/fwlink/?linkid=2038117 for troubleshooting tips.</span></span>

7. <span data-ttu-id="1fd11-p105">파일을 다운로드 한 후 적절 한 수 있는 도구와 수정 수 있습니다. 암호로 보호 된 파일에 대 한 다양 한 암호 해독 도구를 사용할 수 있습니다. 파일에 대 한 암호를 알고 있는 경우에 열기 전에 수 있으며 암호 보호 기능을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-p105">After downloading the files, you can remediate them with an appropriate tool. For password protected files, there are a number of password cracking tools you can use. If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="1fd11-p106">IT은 그대로 유지 remediated 파일의 파일 이름과 디렉터리 구조를 유지 하는 것이 중요 합니다.  다운로드 한 파일에 사용 되는 모든 명명 규칙 및 폴더 수 있도록 원래 remdiated 파일에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-p106">IT is important that you retain the directory structure and file names of the remediated files in tact.  All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="1fd11-p107">이제, 고급 eDiscovery (미리 보기)를 반환 하 고 클릭 **다음: 파일을 업로드할**합니다.  파일을 지금 업로드할 수 있는 다음 단계로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-p107">Now, return to Advanced eDiscovery (Preview) and click **Next: Upload files**.  This will move to the next step where you can now upload the files.</span></span>

    ![파일 업로드](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="1fd11-135">**파일의 위치에 대 한 경로** 텍스트 상자에 remediated 파일의 위치를 지정 하기 위해 **clibpboard로 복사**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="1fd11-136">명령은 Windows 명령 프롬프트에 붙여넣은 파일을 업로드 하려면 **Enter** 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="1fd11-138">마지막으로 고급 eDiscovery (미리 보기)를 반환 하 고 클릭 **다음: 파일을 처리**합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-138">Finally, return to Advanced eDiscovery (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="1fd11-p108">처리가 완료 되 면  작업 집합을 반환할 수 있으며 remediated 파일을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1fd11-p108">When processing is complete.  You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="1fd11-141">파일은 설정을 할 때 수행 하는 작업</span><span class="sxs-lookup"><span data-stu-id="1fd11-141">What happens when files are remediated</span></span>

<span data-ttu-id="1fd11-142">설정을 파일 업로드 된 하는 경우에 다음 필드를 제외 하 고 원래 메타 데이터 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fd11-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="1fd11-143">DocumentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="1fd11-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="1fd11-144">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="1fd11-144">ExtractedTextSize</span></span>
- <span data-ttu-id="1fd11-145">HasText</span><span class="sxs-lookup"><span data-stu-id="1fd11-145">HasText</span></span>
- <span data-ttu-id="1fd11-146">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="1fd11-146">IsErrorRemediate</span></span>
- <span data-ttu-id="1fd11-147">IsParentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="1fd11-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="1fd11-148">ItemExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="1fd11-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="1fd11-149">LoadId</span><span class="sxs-lookup"><span data-stu-id="1fd11-149">LoadId</span></span>
- <span data-ttu-id="1fd11-150">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="1fd11-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="1fd11-151">상태</span><span class="sxs-lookup"><span data-stu-id="1fd11-151">ProcessingStatus</span></span>
- <span data-ttu-id="1fd11-152">텍스트</span><span class="sxs-lookup"><span data-stu-id="1fd11-152">Text</span></span>
- <span data-ttu-id="1fd11-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="1fd11-153">WordCount</span></span>
- <span data-ttu-id="1fd11-154">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="1fd11-154">WorkingsetId</span></span>

<span data-ttu-id="1fd11-155">고급 eDiscovery (미리 보기)의 모든 문서 메타 데이터 필드의 정의 [문서 메타 데이터 필드](document-metadata-fields.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1fd11-155">For a definition of all document metadata fields in Advanced eDiscovery (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>