---
title: Exchange Online Protection의 보고 및 메시지 추적
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: Microsoft EOP(Exchange Online Protection)에서는 조직의 전체 상태를 확인할 수 있는 다양한 보고서를 제공합니다. 받는 사람에게 메시지가 도착하지 않는 등 특정 이벤트에 대한 문제를 해결할 수 있는 도구와 규정 준수 요구 사항을 지원하는 감사 보고서도 있습니다. 다음 표에서는 EOP 관리자가 사용할 수 있는 보고서 및 문제 해결 도구를 설명합니다.
ms.openlocfilehash: 0dcacec586408bf98ad4c67c11ae3bde3a8e9315
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154620"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a><span data-ttu-id="b7c9c-105">Exchange Online Protection의 보고 및 메시지 추적</span><span class="sxs-lookup"><span data-stu-id="b7c9c-105">Reporting and message trace in Exchange Online Protection</span></span>

<span data-ttu-id="b7c9c-106">Microsoft EOP(Exchange Online Protection)에서는 조직의 전체 상태를 확인할 수 있는 다양한 보고서를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-106">Microsoft Exchange Online Protection (EOP) offers many different reports that can help you determine the overall status and health of your organization.</span></span> <span data-ttu-id="b7c9c-107">받는 사람에게 메시지가 도착하지 않는 등 특정 이벤트에 대한 문제를 해결할 수 있는 도구와 규정 준수 요구 사항을 지원하는 감사 보고서도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-107">There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span> 

## <a name="usage-reports"></a><span data-ttu-id="b7c9c-108">사용 현황 보고서</span><span class="sxs-lookup"><span data-stu-id="b7c9c-108">Usage reports</span></span>

<span data-ttu-id="b7c9c-109">**Office 365 그룹 활동** 만들어지고 사용 되는 Office 365 그룹의 수에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-109">**Office 365 groups activity** View information about the number of Office 365 groups that are created and used.</span></span>  

<span data-ttu-id="b7c9c-110">**전자 메일 활동** 전체 조직에서 전송, 수신 및 읽은 메시지 수 및 특정 사용자에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-110">**Email activity** View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>  

<span data-ttu-id="b7c9c-111">**전자 메일 앱 사용 현황** 사용 되는 전자 메일 앱에 대 한 정보를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-111">**Email app usage** View information about the email apps that are used.</span></span> <span data-ttu-id="b7c9c-112">여기에는 각 앱에 대 한 총 연결 수와 연결 중인 Outlook의 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-112">This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>  

<span data-ttu-id="b7c9c-113">**사서함 사용 현황** 사서함에 사용 되는 저장소, 할당량 소비, 항목 수 및 마지막 활동 (보내기 또는 읽기 작업)에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-113">**Mailbox usage** View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="b7c9c-114">자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-114">See the following resources for more information:</span></span>

- [<span data-ttu-id="b7c9c-115">관리 센터의 office 365 보고서-Office 365 그룹</span><span class="sxs-lookup"><span data-stu-id="b7c9c-115">Office 365 Reports in the admin center - Office 365 groups</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [<span data-ttu-id="b7c9c-116">관리 센터의 Office 365 보고서-전자 메일 활동</span><span class="sxs-lookup"><span data-stu-id="b7c9c-116">Office 365 Reports in the Admin Center - Email activity</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [<span data-ttu-id="b7c9c-117">관리 센터의 Office 365 보고서-전자 메일 앱 사용</span><span class="sxs-lookup"><span data-stu-id="b7c9c-117">Office 365 Reports in the Admin Center - Email apps usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [<span data-ttu-id="b7c9c-118">관리 센터의 Office 365 보고서-사서함 사용량</span><span class="sxs-lookup"><span data-stu-id="b7c9c-118">Office 365 Reports in the Admin Center - Mailbox usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-microsoft-365-admin-center"></a><span data-ttu-id="b7c9c-119">Microsoft &amp; 365 관리 센터의 보안 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="b7c9c-119">Security &amp; compliance reports in the Microsoft 365 admin center</span></span>

<span data-ttu-id="b7c9c-120">이러한 향상 된 보고서는 요약 정보와 자세한 정보를 드릴 다운 하는 기능을 포함 하는 EOP 관리자에 게 대화형 보고 환경을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-120">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>  

<span data-ttu-id="b7c9c-121">**ATP (Advanced Threat Protection)** ATP의 일부인 안전한 링크 및 안전한 첨부 파일에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-121">**Advanced Threat Protection (ATP)** View information about safe links and safe attachments that are part of ATP.</span></span>  

<span data-ttu-id="b7c9c-122">**EOP** 조직에서 보내고 보낸 맬웨어 감지, 스푸핑된 메일, 스팸 감지 및 메일 흐름에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-122">**EOP** View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>  

[<span data-ttu-id="b7c9c-123">Advanced Threat Protection 및 Exchange Online Protection에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="b7c9c-123">View reports for Advanced Threat Protection and Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="b7c9c-124">Microsoft Graph를 사용한 사용자 지정 보고서</span><span class="sxs-lookup"><span data-stu-id="b7c9c-124">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="b7c9c-125">Microsoft Graph를 사용 하 여 Microsoft 365 관리 센터에서 사용할 수 있는 보고서를 프로그래밍 방식으로 만들기 microsoft [graph에서 Office 365 사용 현황 보고서 작업](https://go.microsoft.com/fwlink/p/?linkid=865135) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-125">Programmatically create reports that are available in the Microsoft 365 admin center by using Microsoft Graph  See the subtopics of [Working with Office 365 usage reports in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span></span> 

##<a name="custom-reports-using-reporting-web-services"></a><span data-ttu-id="b7c9c-126">보고 웹 서비스를 사용한 사용자 지정 보고서</span><span class="sxs-lookup"><span data-stu-id="b7c9c-126">Custom reports using reporting web services</span></span>

<span data-ttu-id="b7c9c-127">REST/ODATA2 쿼리 필터링을 사용 하 여 사용 가능한 Exchange Online Protection PowerShell 보고 cmdlet에서 프로그래밍 방식으로 보고서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-127">Programmatically create reports from the available Exchange Online Protection PowerShell reporting cmdlets by using REST/ODATA2 query filtering.</span></span>

<span data-ttu-id="b7c9c-128">[Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926) 참조</span><span class="sxs-lookup"><span data-stu-id="b7c9c-128">See [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span></span> 

##<a name="message-trace"></a><span data-ttu-id="b7c9c-129">Message trace</span><span class="sxs-lookup"><span data-stu-id="b7c9c-129">Message trace</span></span>

<span data-ttu-id="b7c9c-130">EOP를 통과하는 전자 메일 메시지를 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-130">Follows email messages as they travel through EOP.</span></span> <span data-ttu-id="b7c9c-131">이를 통해 서비스에서 전자 메일 메시지를 수신, 거부, 지연 또는 배달했는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-131">You can determine if an email message was received, rejected, deferred, or delivered by the service.</span></span> <span data-ttu-id="b7c9c-132">또한 최종 상태에 도달 하기 전에 메시지에 대해 수행 된 작업을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-132">It also shows what actions were taken on the message before it reached its final status.</span></span>  

<span data-ttu-id="b7c9c-133">이 정보를 사용 하 여 사용자의 질문에 효과적으로 응답 하 고, 메일 흐름 문제를 해결 하며, 정책 변경을 확인 하 고, 기술 지원 서비스에 문의 하 여 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-133">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>  

<span data-ttu-id="b7c9c-134">[전자 메일 메시지 추적](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx) 참조</span><span class="sxs-lookup"><span data-stu-id="b7c9c-134">See [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span></span> 

## <a name="audit-logging"></a><span data-ttu-id="b7c9c-135">감사 로깅</span><span class="sxs-lookup"><span data-stu-id="b7c9c-135">Audit logging</span></span>

<span data-ttu-id="b7c9c-136">조직 관리자가 변경한 특정 내용을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-136">Tracks specific changes made by admins to your organization.</span></span> <span data-ttu-id="b7c9c-137">이러한 보고서를 사용하면 구성 문제를 해결하거나 보안 또는 규정 준수 관련 문제의 원인을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-137">These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.</span></span>  <span data-ttu-id="b7c9c-138">[EOP에서 감사 보고서](auditing-reports-in-eop.md) 참조</span><span class="sxs-lookup"><span data-stu-id="b7c9c-138">see [Auditing reports in EOP](auditing-reports-in-eop.md)</span></span> 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="b7c9c-139">보고 및 메시지 추적 데이터 사용 가능 여부 및 대기 시간</span><span class="sxs-lookup"><span data-stu-id="b7c9c-139">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="b7c9c-140">다음 표에는 EOP 보고 및 메시지 추적 데이터를 사용할 수 있는 시기와 기간에 대한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-140">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="b7c9c-141">**보고서 유형**</span><span class="sxs-lookup"><span data-stu-id="b7c9c-141">**Report type**</span></span> <br/> |<span data-ttu-id="b7c9c-142">**데이터 사용 가능 기간(확인 기간)**</span><span class="sxs-lookup"><span data-stu-id="b7c9c-142">**Data available for (look back period)**</span></span> <br/> |<span data-ttu-id="b7c9c-143">**대기 시간**</span><span class="sxs-lookup"><span data-stu-id="b7c9c-143">**Latency**</span></span> <br/> |
|<span data-ttu-id="b7c9c-144">메일 보호 요약 보고서</span><span class="sxs-lookup"><span data-stu-id="b7c9c-144">Mail protection summary reports</span></span>  <br/> |<span data-ttu-id="b7c9c-145">90일</span><span class="sxs-lookup"><span data-stu-id="b7c9c-145">90 days</span></span>  <br/> |<span data-ttu-id="b7c9c-p106">메시지 데이터 집계는 대부분 24~48시간 이내에 완료됩니다. 일부 사소한 증분 집계 변경의 경우 5일까지 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>  <br/> |
|<span data-ttu-id="b7c9c-148">메일 보호 세부 정보 보고서</span><span class="sxs-lookup"><span data-stu-id="b7c9c-148">Mail protection detail reports</span></span>  <br/> |<span data-ttu-id="b7c9c-149">90일</span><span class="sxs-lookup"><span data-stu-id="b7c9c-149">90 days</span></span>  <br/> |<span data-ttu-id="b7c9c-p107">7일 미만의 세부 데이터는 24시간 이내에 표시되지만 48시간이 될 때까지 완료되지 않을 수 있습니다. 일부 사소한 증분 변경의 경우 5일까지 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span>  <br/> <span data-ttu-id="b7c9c-152">7일이 지난 메시지에 대한 상세 보고서를 보려면 결과가 표시되는 데 최대 몇 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-152">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
|<span data-ttu-id="b7c9c-153">메시지 추적 데이터</span><span class="sxs-lookup"><span data-stu-id="b7c9c-153">Message trace data</span></span>  <br/> |<span data-ttu-id="b7c9c-154">90일</span><span class="sxs-lookup"><span data-stu-id="b7c9c-154">90 days</span></span>  <br/> |<span data-ttu-id="b7c9c-155">7일 미만의 메시지에 대해 메시지 추적을 실행하면 메시지가 5~30분 이내에 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-155">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span>  <br/> <span data-ttu-id="b7c9c-156">7일이 지난 메시지에 대해 메시지 추적을 실행하면 결과가 표시되는 데 최대 몇 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-156">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b7c9c-157">데이터 사용 가능 여부 및 대기 시간은 Microsoft 365 관리 센터 또는 원격 PowerShell을 통해 요청 된 경우와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-157">Data availability and latency is the same whether requested via the Microsoft 365 admin center or remote PowerShell.</span></span> 
  

