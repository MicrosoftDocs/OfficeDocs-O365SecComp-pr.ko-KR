---
title: 보안 &amp; 및 준수 센터에서 위협 탐색기 사용
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/10/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: 보안 &amp; 및 준수 센터의 Explorer (위협 탐색기 라고도 함)에 대해 알아봅니다.
ms.openlocfilehash: 626d827712760aa0b7b6faf75d94f525cfe38dc2
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30524012"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="6da16-103">보안 &amp; 및 준수 센터에서 위협 탐색기 사용</span><span class="sxs-lookup"><span data-stu-id="6da16-103">Use Threat Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="6da16-104">조직에 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)가 있고 필요한 사용 권한이 있는 경우 위협 탐색기를 사용 하 여 위협을 식별 하 고 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-104">If your organization has [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md), and you have the necessary permissions, you can use Threat Explorer to identify and analyze threats.</span></span> <span data-ttu-id="6da16-105">예를 들어 배달 된 악성 전자 메일을 식별 하 고 삭제할 수 있으며, Office 365 보안 기능으로 인해 발견 된 맬웨어를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-105">For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features.</span></span> <span data-ttu-id="6da16-106">위협 탐색기 (탐색기 라고도 함)는 보안 운영 팀에서 보안 &amp; 및 준수 센터의 위협에 대해 조사 하 고 대응 하는 데 도움이 되는 강력한 거의 실시간 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-106">Threat Explorer (also referred to as Explorer) is a powerful near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span>
  
![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="6da16-108">Explorer를 &amp; 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6da16-109">office 365 위협 인텔리전스는 이제 추가 위협 방지 기능을 사용 하 여 office 365 Advanced Threat protection 계획 2에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-109">Office 365 Threat Intelligence is now part of Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities.</span></span> <span data-ttu-id="6da16-110">자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6da16-110">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="6da16-111">탐색기 개요</span><span class="sxs-lookup"><span data-stu-id="6da16-111">Explorer overview</span></span>

<span data-ttu-id="6da16-112">탐색기에는 조직에 대 한 기타 보안 위협 및 위험 뿐 아니라 전자 메일 및 Office 365의 파일에 있는 의심 스러운 맬웨어 및 피싱에 대 한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-112">Explorer displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span> <span data-ttu-id="6da16-113">처음으로 탐색기를 열면 기본 보기에는 최근 7 일간의 전자 메일 맬웨어 검색이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-113">When you first open Explorer, the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="6da16-114">또한 Explorer는 [안전한 링크](atp-safe-links.md) 및 [안전한 첨부 파일](atp-safe-attachments.md) 을 포함 하 여 Office 365의 보안 보호 기능을 표시할 수 있으며, 이전의 30 일간의 데이터를 표시 하도록 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-114">Explorer can also show security protection features in Office 365, including [Safe Links](atp-safe-links.md) and [Safe Attachments](atp-safe-attachments.md) and can be modified to show data for the past 30 days.</span></span> <span data-ttu-id="6da16-115">office 365 Advanced Threat Protection 계획 2 또는 Office 365 E5에 대 한 평가판 subcription 있는 경우에는 최근 7 일간의 검색 및 전자 메일 데이터만 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-115">If you have a trial subcription for Office 365 Advanced Threat Protection Plan 2 or Office 365 E5, you will only see detections and email data for the past 7 days.</span></span>
  
![Explorer에는 가장 많이 사용한 맬웨어 및 대상 사용자에 대 한 정보가 표시 됩니다.](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
<span data-ttu-id="6da16-117">표시 되는 정보를 변경 하려면 보기 메뉴를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-117">Use the View menu to change what information is displayed.</span></span>
  
![탐색기에 대 한 보기 메뉴](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
<span data-ttu-id="6da16-119">Explorer에는 상위 대상 사용자, 최고 맬웨어 제품군, 검색 기술 등의 세부 정보를 확인할 수 있는 다양 한 필터링 및 쿼리 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-119">Explorer has several filtering and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="6da16-120">각 보고서 종류에서는 다양 한 방식으로 데이터를 보고 탐색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-120">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6da16-121">별표 (\*) 또는 물음표 (?)와 같은 와일드 카드 문자는 탐색기에서 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="6da16-121">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), with Explorer.</span></span> <span data-ttu-id="6da16-122">전자 메일 메시지의 제목 필드를 검색 하면 Explorer는 부분 일치를 수행 하 고 와일드 카드 검색과 비슷한 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-122">When you search on the Subject field for email messages, Explorer will perform partial matching and yield results similar to a wildcard search.</span></span>

## <a name="email--malware"></a><span data-ttu-id="6da16-123">전자 \> 메일 맬웨어</span><span class="sxs-lookup"><span data-stu-id="6da16-123">Email \> Malware</span></span>

<span data-ttu-id="6da16-124">이 보기에는 맬웨어를 포함 하는 것으로 확인 된 전자 메일 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-124">This view shows email messages identified as containing malware.</span></span>  

<span data-ttu-id="6da16-125">맬웨어 제품군, 보낸 사람 도메인, 보낸 사람 IP, 보호 상태 (Office 365의 위협 보호 기능 및 정책에 의해 수행 된 작업) 및 검색 기술 (맬웨어 검색 방법)에 따라 차트의 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-125">View information in the chart by malware family, sender domain, sender IP, protection status (actions taken by your threat protection features and policies in Office 365), and detection technology (how the malware was detected).</span></span>  

![검색 된 맬웨어에 대 한 데이터 보기](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

<span data-ttu-id="6da16-127">차트 아래에서 주요 맬웨어 패밀리, 상위 대상 사용자 및 특정 메시지에 대 한 세부 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-127">Below the chart, view details about top malware families, top targeted users, and more details about specific messages.</span></span> 

## <a name="email--phish"></a><span data-ttu-id="6da16-128">전자 \> 메일 피싱</span><span class="sxs-lookup"><span data-stu-id="6da16-128">Email \> Phish</span></span>

<span data-ttu-id="6da16-129">이 보기에는 피싱 시도로 식별 된 전자 메일 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-129">This view shows email messages identified as phishing attempts.</span></span>  

<span data-ttu-id="6da16-130">보낸 사람 도메인, 보낸 사람 IP 및 보호 상태 (Office 365의 위협 보호 기능 및 정책에 의해 수행 된 작업) 별로 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-130">View information by sender domain, sender IP, and protection status (actions taken by your threat protection features and policies in Office 365).</span></span> 

![피싱 시도로 식별 된 전자 메일에 대 한 데이터 보기](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

<span data-ttu-id="6da16-132">차트 아래에서 특정 메시지에 대 한 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-132">Below the chart, view more details about specific messages.</span></span> 

## <a name="email--user-reported"></a><span data-ttu-id="6da16-133">전자 \> 메일 사용자가 보고 됨</span><span class="sxs-lookup"><span data-stu-id="6da16-133">Email \> User-reported</span></span>

<span data-ttu-id="6da16-134">이 보기에는 사용자가 정크 메일로 보고 되거나, 정크 메일, 피싱 전자 메일이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-134">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>  

<span data-ttu-id="6da16-135">정보 보기 (사용자가 전자 메일을 정크 메일로, 정크 메일이 아님, 또는 피싱를 결정 함), 배달 사유 (스팸 필터 정책, 메일 흐름 규칙, 수신 거부 목록, 수신 허용-보낸 사람 목록 등을 사용 하 여 전자 메일을 특정 위치로 이동 해야 하는 이유) 등)</span><span class="sxs-lookup"><span data-stu-id="6da16-135">View information by report type (the user's determination that the email was junk, not junk, or phish), and by delivery reason (reasons why email went to a specific location, such as a spam filter policy, a mail flow rule, a blocked-senders list, a safe-senders list, etc.).</span></span>  

![정크 메일로 보고 된 전자 메일 사용자에 대 한 데이터 보기, 정크 메일 또는 피싱 사기](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

<span data-ttu-id="6da16-137">차트 아래에 있는 특정 전자 메일 메시지에 대 한 세부 정보 (예: 제목 줄, 보낸 사람의 IP 주소, 메시지를 정크로 보고 한 사용자, 정크 메일, 피싱 등)를 자세히 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-137">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

## <a name="email--all-mail"></a><span data-ttu-id="6da16-138">전자 \> 메일 모든 메일</span><span class="sxs-lookup"><span data-stu-id="6da16-138">Email \> All mail</span></span>

<span data-ttu-id="6da16-139">이 보기에는 모든 비 악성 메일 (일반 전자 메일, 스팸 및 대량 메일)과 마찬가지로 피싱 또는 맬웨어로 인 한 악성 전자 메일을 비롯 한 전자 메일 활동의 모든 보기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-139">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="6da16-140">**너무 많은 데이터를 표시 하는 데**오류가 발생 하는 경우 필터를 추가 하 고 필요한 경우 보고 있는 날짜 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-140">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="6da16-141">필터를 적용 하려면 **보낸 사람**을 선택 하 고 목록에서 항목을 선택한 다음 새로 고침 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-141">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="6da16-142">이 예제에서는 **검색 기술을** 필터로 사용 했으며 몇 가지 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-142">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="6da16-143">보낸 사람, 보낸 사람의 도메인, 받는 사람, 제목, 첨부 파일 이름, 맬웨어 제품군, 보호 상태 (Office 365의 위협 보호 기능 및 정책에 따라 수행 된 작업), 검색 기술 (맬웨어 감지 방법) 및 자세한.</span><span class="sxs-lookup"><span data-stu-id="6da16-143">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![검색 기술을 통해 검색 된 전자 메일에 대 한 데이터 보기](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="6da16-145">차트 아래에 제목 줄, 받는 사람, 보낸 사람, 상태 등의 특정 전자 메일 메시지에 대 한 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-145">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="6da16-146">콘텐츠 \> 맬웨어</span><span class="sxs-lookup"><span data-stu-id="6da16-146">Content \> Malware</span></span>

<span data-ttu-id="6da16-147">이 보기는 SharePoint Online, 비즈니스용 OneDrive 및 Microsoft 팀의 Office 365 Advanced Threat Protection에서 악의적으로 식별 된 파일을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-147">This view shows files that were identified as malicious by Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="6da16-148">맬웨어 제품군, 검색 기술 (맬웨어가 감지 된 방법) 및 작업 (OneDrive, SharePoint 또는 팀)을 통해 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-148">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![검색 된 맬웨어에 대 한 데이터 보기](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="6da16-150">차트 아래에서 첨부 파일 이름, 작업, 파일 크기, 파일을 마지막으로 수정한 사용자 등 특정 파일에 대 한 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-150">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="new-click-to-filter-capabilities"></a><span data-ttu-id="6da16-151">(새로운 방법!) 간편 필터 기능</span><span class="sxs-lookup"><span data-stu-id="6da16-151">(New!) Click-to-filter capabilities</span></span>

<span data-ttu-id="6da16-152">새로 만들기 Explorer를 클릭 하 여 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-152">New to Explorer is the ability to click to filter.</span></span> <span data-ttu-id="6da16-153">범례에서 항목을 클릭 하면 해당 항목이 보고서에 대 한 필터가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-153">When you click an item in the legend, that item becomes a filter for the report.</span></span> <span data-ttu-id="6da16-154">예를 들어 Explorer에서 맬웨어 보기를 보고 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-154">For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="6da16-156">이 차트에서 **ATP 샌드 박싱** 를 클릭 하면 다음과 같은 보기가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-156">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![탐색기가 필터링 되어 ATO 샌드 박싱 결과만 표시 합니다.](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="6da16-158">이 보기에서는 [Office 365 ATP 안전한 첨부](atp-safe-attachments.md)파일에서 열 된 파일에 대 한 데이터를 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-158">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="6da16-159">이 차트 아래에서 ATP 안전한 첨부 파일에 의해 검색 된 첨부 파일이 있는 특정 전자 메일 메시지에 대 한 세부 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-159">Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![검색 된 첨부 파일이 있는 전자 메일 메시지에 대 한 구체적인 세부 정보](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="6da16-161">항목을 하나 이상 선택 하면 선택한 항목에 대해 선택할 수 있는 여러 선택 항목이 제공 되는 **작업** 메뉴가 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-161">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![항목을 선택 하면 작업 메뉴가 활성화 됩니다.](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="6da16-163">클릭 하 고 특정 세부 정보로 탐색 하는 기능을 통해 위협을 조사 하는 데 많은 시간을 절약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-163">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>
  
## <a name="how-do-i-get-explorer"></a><span data-ttu-id="6da16-164">탐색기를 가져오려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="6da16-164">How do I get Explorer?</span></span>

<span data-ttu-id="6da16-165">Explorer는 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-165">Explorer is included in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span></span> 

<span data-ttu-id="6da16-166">Explorer를 보고 사용 하려면 보안 관리자 또는 보안 판독기에 부여 된 것과 같은 적절 한 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da16-166">You must have appropriate permissions, such as those granted to a security administrator or security reader, in order to view and use Explorer.</span></span> <span data-ttu-id="6da16-167">자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6da16-167">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="6da16-168">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6da16-168">Related topics</span></span>

[<span data-ttu-id="6da16-169">Office 365 보안 &amp; 및 준수 센터의 보고서 및 정보</span><span class="sxs-lookup"><span data-stu-id="6da16-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="6da16-170">배달 된 악성 전자 메일 찾기 및 조사 (Office 365 Threat Invesitgation 및 응답)</span><span class="sxs-lookup"><span data-stu-id="6da16-170">Find and investigate malicious email that was delivered (Office 365 Threat Invesitgation and Response)</span></span>](investigate-malicious-email-that-was-delivered.md)
  
[<span data-ttu-id="6da16-171">Office 365의 스팸 방지 및 맬웨어 방지 보호</span><span class="sxs-lookup"><span data-stu-id="6da16-171">Anti-spam and anti-malware protection in Office 365</span></span>](anti-spam-and-anti-malware-protection.md)
  

