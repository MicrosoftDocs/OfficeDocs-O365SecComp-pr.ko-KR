---
title: Advanced eDiscovery에서 AzCopy 문제 해결
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 2c8378cf7b9bd21f901b1babbebdcb0b69a8ed73
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151520"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery"></a><span data-ttu-id="460a4-102">Advanced eDiscovery에서 AzCopy 문제 해결</span><span class="sxs-lookup"><span data-stu-id="460a4-102">Troubleshoot AzCopy in Advanced eDiscovery</span></span>

<span data-ttu-id="460a4-103">고급 eDiscovery에서 오류 수정을 위해 Office가 아닌 365 데이터 또는 문서를 로드할 때 사용자 인터페이스는 업로드 하려는 파일이 저장 되는 위치 및 Azure 저장소에 있는 매개 변수를 포함 하는 Azure AzCopy 명령을 제공 합니다. 파일이 업로드 될 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-103">When loading non-Office 365 data or documents for error remediation in Advanced eDiscovery, the user interface supplies an Azure AzCopy command that contains parameters with the location of where the files that you want to upload are stored and the Azure storage location that the files will be uploaded to.</span></span> <span data-ttu-id="460a4-104">문서를 업로드 하려면 로컬 컴퓨터의 명령 프롬프트에서이 명령을 복사한 다음 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-104">To upload your documents, you copy this command and then run it in a Command Prompt on your local computer.</span></span>  <span data-ttu-id="460a4-105">다음 스크린샷에는 AzCopy 명령의 예가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-105">The follow screenshot shows an example of an AzCopy command:</span></span>

![Office 이외의 365 파일 업로드](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

<span data-ttu-id="460a4-107">대부분의 경우 제공 되는 명령은 실행 시 작동 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-107">In most cases, the command that's provided will work when you run it.</span></span> <span data-ttu-id="460a4-108">그러나 표시 된 명령이 정상적으로 실행 되지 않는 경우가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-108">However, there may be cases when the command that's displayed will not run successfully.</span></span> <span data-ttu-id="460a4-109">몇 가지 가능한 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-109">Here's a few possible reasons.</span></span>

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a><span data-ttu-id="460a4-110">AzCopy가 로컬 컴퓨터에 설치 되어 있지 않거나 기본 위치에 설치 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-110">AzCopy isn't installed on the local computer or it's not installed in the default location</span></span>

<span data-ttu-id="460a4-111">AzCopy가 설치 되어 있지 않거나 기본 설치 위치 (is `%ProgramFiles(x86)%`) 이외의 위치에 설치 되어 있는 경우 AzCopy 명령을 실행 하면 다음 오류 메시지가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-111">If AzCopy isn't installed or it's installed in a location other than the default install location (which is `%ProgramFiles(x86)%`), you may receive the following error when you run the AzCopy command:</span></span>

    The system cannot find the path specified.

<span data-ttu-id="460a4-112">AzCopy가 로컬 컴퓨터에 설치 되어 있지 않으면 여기에서 설치할 수 있습니다 (기본 위치에 설치 되어 있음) [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="460a4-112">If AzCopy isn't install on the local computer, you can install from here (being sure to install it in the default location): [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span></span>


<span data-ttu-id="460a4-113">AzCopy가 설치 되어 있지만 기본 위치와 다른 위치에 설치 되어 있는 경우 명령을 복사 하 여 텍스트 파일에 붙여 넣은 다음 AzCopy이 실제로 설치 된 위치에 대 한 경로를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-113">If AzCopy is installed, but it's installed in a location different than the default location, you can copy the command, paste it to a text file, and then change the path to the location where AzCopy is actually installed.</span></span> <span data-ttu-id="460a4-114">예를 들어 Azcopy가에 `%ProgramFiles%`있는 경우 명령의 첫 번째 부분 `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` 을로 `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-114">For example, if Azcopy is located in `%ProgramFiles%`, then you can change the first part of the command from `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` to `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`.</span></span> <span data-ttu-id="460a4-115">이 변경 작업을 수행한 후에는 텍스트 파일에서 복사한 다음 명령 프롬프트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-115">After you make this change, copy it from the text file and then run it a Command Prompt.</span></span>

> [!TIP]
> <span data-ttu-id="460a4-116">기본 설치 위치 이외의 위치에 AzCopy가 설치 되어 있으면 제거한 다음 기본 위치에 다시 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-116">If AzCopy is installed in a location other then the default install location, consider uninstalling it and then re-installing it in the default location.</span></span> <span data-ttu-id="460a4-117">이를 통해 나중에이 문제를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="460a4-117">This will help prevent this issue in the future.</span></span>