---
title: Office 365, O365 전송, Office 365 스팸 문제, O365 가양성, 검색을 위한 전자 메일 전송, office 365에서 의심 스러운 전자 메일, 메일 검색, 365 피싱에 대 한 Microsoft 검색, Microsoft scan for 피싱, submit for 스팸, 제출 전자 메일, 메일 제출
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 08/06/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Office 365 테 넌 트에서 의심 스러운 전자 메일, 의심 스러운 메일, 스팸 및 기타 해로운 메시지, Url 및 파일을 검색을 위해 Microsoft에 제출 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 5a909e8b587e2a1265c1b2afbd5e063d46a04e2c
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230952"
---
# <a name="how-to-submit-suspected-spam-phish-urls-and-files-to-microsoft-for-office-365-scanning"></a><span data-ttu-id="ea407-103">Microsoft에 Office 365를 검색 하기 위해 의심 스러운 스팸, 피싱, Url 및 파일을 제출 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ea407-103">How to submit suspected spam, phish, URLs, and files to Microsoft for Office 365 scanning</span></span>

<span data-ttu-id="ea407-104">관리자는 Office 365에서 Microsoft가 검색을 위해 파일 또는 네트워크 메시지 ID, Url 및 파일을 사용 하 여 전자 메일을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-104">Admins can send emails by using file or network message ID, URLs, and files for scanning by Microsoft in Office 365.</span></span> <span data-ttu-id="ea407-105">업데이트 된 전송 섹션에도 사용자가 보고 한 메시지가 포함 되며, EOP을 사용 하는 모든 고객이 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-105">The updated submissions section still includes user reported messages and available to all customers using EOP.</span></span>

<span data-ttu-id="ea407-106">전자 메일을 제출 하면 메일에 포함 된 Url 및 첨부 파일을 검사 하는 것은 물론 수신 전자 메일을 허용 했을 수 있는 모든 정책에 대 한 정보를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-106">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="ea407-107">메일을 허용할 수 있는 정책에는 개인 사용자의 수신 허용-보낸 사람 목록 및 ETR 규칙과 같은 테 넌 트 수준 정책이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-107">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as ETR rules.</span></span> 

## <a name="how-to-submit-content-to-microsoft-for-office-365-scanning"></a><span data-ttu-id="ea407-108">Office 365 검색을 위해 Microsoft에 콘텐츠를 전송 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ea407-108">How to submit content to Microsoft for Office 365 scanning</span></span>

<span data-ttu-id="ea407-109">Microsoft로 콘텐츠를 전송 하려면 제출 페이지의 왼쪽 위에 있는 **새 제출** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-109">To submit content to Microsoft click the **New submission** button in the top left hand side of the submissions page.</span></span> <span data-ttu-id="ea407-110">전자 메일, URL 또는 파일을 전송 하는 옵션을 사용 하 여 페이지 오른쪽에 플라이 아웃이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-110">A flyout on the right side of the page appears with the option to submit either an email, URL, or file.</span></span> 

### <a name="submit-an-email-to-microsoft"></a><span data-ttu-id="ea407-111">Microsoft에 전자 메일 제출</span><span class="sxs-lookup"><span data-stu-id="ea407-111">Submit an email to Microsoft</span></span>
![전자 메일 전송 예](media/submission-flyout-email.PNG)
1. <span data-ttu-id="ea407-113">전자 메일을 제출 하려면 **전자 메일** 을 선택 하 고 전자 메일 **네트워크 메시지 ID** 를 지정 하거나 전자 메일 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-113">To submit an email, select **email** and specify the email **network message ID** or upload the email file.</span></span> 

2. <span data-ttu-id="ea407-114">정책 확인을 실행 하려는 받는 사람을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-114">Specify the recipient(s) that you would like to run the policy check against.</span></span> <span data-ttu-id="ea407-115">정책 확인은 사용자 또는 테 넌 트 수준 정책으로 인해 전자 메일에서 검색이 사용 되지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-115">The policy check will determine if the email bypassed scanning due to user or tenant level policies.</span></span> 

3. <span data-ttu-id="ea407-116">전자 메일이 차단 되었는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-116">Specify if the email should have been blocked or not.</span></span> <span data-ttu-id="ea407-117">전자 메일이 차단 되어야 하는 경우 스팸, 피싱 또는 맬웨어로 차단 되어야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-117">If the email should have been blocked, specify if it should have been blocked as Spam, Phishing, or Malware.</span></span> <span data-ttu-id="ea407-118">어떤 형식을 사용할 수 있는지 잘 모르는 경우에는 최상의 judgement를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-118">If you are not sure what type it might be, use your best judgement.</span></span>  

* <span data-ttu-id="ea407-119">전송 시 정책으로 인해 필터가 생략 되 면 해당 정책에 대 한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-119">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

* <span data-ttu-id="ea407-120">하나 이상의 정책으로 인해 필터가 무시 되지 않으면 몇 분 안에 검색이 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-120">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="ea407-121">상태 링크를 클릭 하 여 전송에 대 한 추가 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-121">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="ea407-122">여기에는 정책 확인 및 다시 검사 결과의 결과가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-122">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="ea407-123">참고 Office 365 ATP 전체 필터링 스택을 통해 전자 메일을 다시 실행 하지만 메일, URL 또는 파일의 특정 특성에 따라 부분 다시 검사를 실행 하는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-123">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span> 

4. <span data-ttu-id="ea407-124">**제출** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-124">Click the **Submit** button.</span></span>

### <a name="submit-a-url-to-microsoft"></a><span data-ttu-id="ea407-125">Microsoft에 URL 제출</span><span class="sxs-lookup"><span data-stu-id="ea407-125">Submit a URL to Microsoft</span></span>
![전자 메일 전송 예](media/submission-url-flyout.png)
1. <span data-ttu-id="ea407-127">URL을 제출 하려면 플라이 아웃에서 **url** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-127">To submit a URL select **URL** from the flyout.</span></span> <span data-ttu-id="ea407-128">프로토콜 (**https://**)을 포함 하 여 전체 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-128">Type in the full URL including the protocol (**https://**).</span></span> 

* <span data-ttu-id="ea407-129">**필터**를 선택한 경우 URL이 피싱 또는 맬웨어 인지 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-129">If you selected **Should have been filtered**, specify if the URL is phishing or malware.</span></span>

2. <span data-ttu-id="ea407-130">**제출** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-130">Click the **Submit** button.</span></span> 


### <a name="submit-a-file-to-microsoft"></a><span data-ttu-id="ea407-131">Microsoft로 파일 제출</span><span class="sxs-lookup"><span data-stu-id="ea407-131">Submit a file to Microsoft</span></span>
![전자 메일 전송 예](media/submission-file-flyout.PNG)
1. <span data-ttu-id="ea407-133">파일을 제출 하려면 플라이 아웃에서 **파일** 을 선택 하 고 검색할 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-133">To submit a file select **File** from the flyout and upload the file you would like to scan.</span></span> 

2. <span data-ttu-id="ea407-134">**제출** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea407-134">Click the **Submit** button.</span></span>


## <a name="related-topics"></a><span data-ttu-id="ea407-135">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ea407-135">Related topics</span></span>

[<span data-ttu-id="ea407-136">Office 365 Advanced Threat Protection 계획 2</span><span class="sxs-lookup"><span data-stu-id="ea407-136">Office 365 Advanced Threat Protection Plan 2</span></span>](office-365-ti.md)
  
[<span data-ttu-id="ea407-137">Office 365에서 위협 으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="ea407-137">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="ea407-138">Office 365 Advanced Threat Protection에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="ea407-138">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

