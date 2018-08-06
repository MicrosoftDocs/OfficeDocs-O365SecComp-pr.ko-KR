---
title: Exchange Online Protection의 보고 및 메시지 추적
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: Microsoft EOP(Exchange Online Protection)에서는 조직의 전체 상태를 확인할 수 있는 다양한 보고서를 제공합니다. 받는 사람에게 메시지가 도착하지 않는 등 특정 이벤트에 대한 문제를 해결할 수 있는 도구와 규정 준수 요구 사항을 지원하는 감사 보고서도 있습니다. 다음 표에서는 EOP 관리자가 사용할 수 있는 보고서 및 문제 해결 도구를 설명합니다.
ms.openlocfilehash: 01a09b2b4b72161352af3793686c6cc888e44e29
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027145"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a><span data-ttu-id="80b07-105">Exchange Online Protection의 보고 및 메시지 추적</span><span class="sxs-lookup"><span data-stu-id="80b07-105">Reporting and message trace in Exchange Online Protection</span></span>

<span data-ttu-id="80b07-p102">Microsoft Exchange Online Protection (EOP)은 하는데 도움이 되는 여러 다른 보고서의 전반적인 상태 확인 하 여 조직의 제공 합니다. 또한 (예: 메시지의 받는 사람에 게 도착 하지), 특정 이벤트 문제를 해결 하는데 도움이 되는 도구 및 규정 준수 요구 사항을 지원 하기 위해 감사 보고서 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-p102">Microsoft Exchange Online Protection (EOP) offers many different reports that can help you determine the overall status and health of your organization. There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span> 

## <a name="usage-reports"></a><span data-ttu-id="80b07-108">사용 현황 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-108">Usage reports</span></span>

<span data-ttu-id="80b07-109">**Office 365 그룹 작업** 생성 하 고 사용 하는 Office 365 그룹의 수에 대 한 정보를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-109">**Office 365 groups activity** View information about the number of Office 365 groups that are created and used.</span></span>  

<span data-ttu-id="80b07-110">**전자 메일 활동** 전송, 받은 메일 및 전체 조직에서 하 고 특정 사용자가 읽은 메시지 수에 대 한 정보를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-110">**Email activity** View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>  

<span data-ttu-id="80b07-p103">**전자 메일 응용 프로그램 사용** 사용 되는 전자 메일 응용 프로그램에 대 한 정보를 봅니다. 여기에 각 응용 프로그램에 대 한 연결의 총 수와 연결 하는 버전의 Outlook 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-p103">**Email app usage** View information about the email apps that are used. This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>  

<span data-ttu-id="80b07-113">**사서함 사용량** 사용 되는 저장소에 대 한 정보, 할당량 소비, 항목 수 및 사서함에 대 한 마지막 활동 (보내기 또는 읽기 작업)을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-113">**Mailbox usage** View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="80b07-114">자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="80b07-114">See the following resources for more information:</span></span>

- [<span data-ttu-id="80b07-115">Office 365 관리 센터-Office 365의에서 보고서 그룹</span><span class="sxs-lookup"><span data-stu-id="80b07-115">Office 365 Reports in the admin center - Office 365 groups</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [<span data-ttu-id="80b07-116">Office 365 관리 센터-전자 메일 활동에에서는 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-116">Office 365 Reports in the Admin Center - Email activity</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [<span data-ttu-id="80b07-117">관리 센터-전자 메일 응용 프로그램 사용에서에서 office 365 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-117">Office 365 Reports in the Admin Center - Email apps usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [<span data-ttu-id="80b07-118">Office 365 관리 센터-사서함 사용량에에서는 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-118">Office 365 Reports in the Admin Center - Mailbox usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-office-365-admin-center"></a><span data-ttu-id="80b07-119">보안 &amp; Office 365 관리 센터에서 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-119">Security &amp; compliance reports in the Office 365 admin center</span></span>

<span data-ttu-id="80b07-120">이러한 향상 된 보고서 요약 정보 및 자세한 내용은 드릴 다운 하는 기능을 포함 하는 EOP 관리자의 경우에 대 한 대화형 보고 경험을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-120">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>  

<span data-ttu-id="80b07-121">**고급 위협 보호 ATP)** 안전한 링크 및 ATP의 일부인 안전한 첨부 파일에 대 한 정보를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-121">**Advanced Threat Protection (ATP)** View information about safe links and safe attachments that are part of ATP.</span></span>  

<span data-ttu-id="80b07-122">**EOP** 맬웨어 감지, 위장 된 메일, 스팸 감지 및 조직에서 메일 흐름을 하는 방법에 대 한 정보를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-122">**EOP** View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>  

[<span data-ttu-id="80b07-123">고급 위협 보호 및 Exchange Online Protection에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="80b07-123">View reports for Advanced Threat Protection and Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="80b07-124">다음은 Microsoft Graph를 사용 하 여 사용자 지정 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-124">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="80b07-125">프로그래밍 방식으로 Microsoft Graph 참조를 사용 하 여 Office 365 관리 센터에서 사용할 수 있는 보고서를 [Microsoft Graph에서 Office 365 사용 현황 보고서 사용 (영문)](https://go.microsoft.com/fwlink/p/?linkid=865135) 의 하위 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="80b07-125">Programmatically create reports that are available in the Office 365 admin center by using Microsoft Graph  See the subtopics of [Working with Office 365 usage reports in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span></span> 

##<a name="custom-reports-using-reporting-web-services"></a><span data-ttu-id="80b07-126">보고 웹 서비스를 사용한 사용자 지정 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-126">Custom reports using reporting web services</span></span>

<span data-ttu-id="80b07-127">프로그래밍 방식으로 사용할 수 있는 Exchange Online 보호 PowerShell REST/ODATA2 쿼리 필터링을 사용 하 여 보고 cmdlet에서에서 보고서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-127">Programmatically create reports from the available Exchange Online Protection PowerShell reporting cmdlets by using REST/ODATA2 query filtering.</span></span>

<span data-ttu-id="80b07-128">[Office 365 보고 웹 서비스](https://go.microsoft.com/fwlink/p/?LinkId=279926) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="80b07-128">See [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span></span> 

##<a name="message-trace"></a><span data-ttu-id="80b07-129">메시지 추적</span><span class="sxs-lookup"><span data-stu-id="80b07-129">Message trace</span></span>

<span data-ttu-id="80b07-p104">EOP를 통해 이동 되 전자 메일 메시지를 다음과 합니다. 전자 메일 메시지 수신, 거부, 지연, 또는 서비스에 의해 전달 되는 경우를 확인할 수 있습니다. 또한 최종 상태에 도달 하기 전에 메시지에 어떤 작업을 수행 했는지를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-p104">Follows email messages as they travel through EOP. You can determine if an email message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>  

<span data-ttu-id="80b07-133">효율적으로 사용자의 질문에 대답, 메일 흐름 문제를 해결, 정책 변경의 유효성을 검사 하려면이 정보를 사용할 수 및 지원에 대 한 기술 지원 서비스에 문의 필요가 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-133">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>  

<span data-ttu-id="80b07-134">[전자 메일 메시지 추적](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx) 참조</span><span class="sxs-lookup"><span data-stu-id="80b07-134">See [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span></span> 

## <a name="audit-logging"></a><span data-ttu-id="80b07-135">감사 로깅</span><span class="sxs-lookup"><span data-stu-id="80b07-135">Audit logging</span></span>

<span data-ttu-id="80b07-p105">관리자가 수행한 조직의 특정 변경 내용을 추적 합니다. 이러한 보고서 구성 문제를 해결 하거나 보안 또는 규정 준수 관련 문제를의 원인을 찾을 수 있습니다.  [EOP에서 감사 보고서](auditing-reports-in-eop.md) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="80b07-p105">Tracks specific changes made by admins to your organization. These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.  see [Auditing reports in EOP](auditing-reports-in-eop.md)</span></span> 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="80b07-139">보고 및 메시지 추적 데이터 사용 가능 여부 및 대기 시간</span><span class="sxs-lookup"><span data-stu-id="80b07-139">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="80b07-140">다음 표에는 EOP 보고 및 메시지 추적 데이터를 사용할 수 있는 시기와 기간에 대한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-140">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="80b07-141">**보고서 유형**</span><span class="sxs-lookup"><span data-stu-id="80b07-141">**Report type**</span></span> <br/> |<span data-ttu-id="80b07-142">**데이터 사용 가능 기간(확인 기간)**</span><span class="sxs-lookup"><span data-stu-id="80b07-142">**Data available for (look back period)**</span></span> <br/> |<span data-ttu-id="80b07-143">**대기 시간**</span><span class="sxs-lookup"><span data-stu-id="80b07-143">**Latency**</span></span> <br/> |
|<span data-ttu-id="80b07-144">메일 보호 요약 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-144">Mail protection summary reports</span></span>  <br/> |<span data-ttu-id="80b07-145">90일</span><span class="sxs-lookup"><span data-stu-id="80b07-145">90 days</span></span>  <br/> |<span data-ttu-id="80b07-p106">메시지 데이터 집계는 대부분 24~48시간 이내에 완료됩니다. 일부 사소한 증분 집계 변경의 경우 5일까지 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>  <br/> |
|<span data-ttu-id="80b07-148">메일 보호 상세 보고서</span><span class="sxs-lookup"><span data-stu-id="80b07-148">Mail protection detail reports</span></span>  <br/> |<span data-ttu-id="80b07-149">90일</span><span class="sxs-lookup"><span data-stu-id="80b07-149">90 days</span></span>  <br/> |<span data-ttu-id="80b07-p107">7일 미만의 세부 데이터는 24시간 이내에 표시되지만 48시간이 될 때까지 완료되지 않을 수 있습니다. 일부 사소한 증분 변경의 경우 5일까지 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span>  <br/> <span data-ttu-id="80b07-152">7일이 지난 메시지에 대한 상세 보고서를 보려면 결과가 표시되는 데 최대 몇 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-152">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
|<span data-ttu-id="80b07-153">메시지 추적 데이터</span><span class="sxs-lookup"><span data-stu-id="80b07-153">Message trace data</span></span>  <br/> |<span data-ttu-id="80b07-154">90일</span><span class="sxs-lookup"><span data-stu-id="80b07-154">90 days</span></span>  <br/> |<span data-ttu-id="80b07-155">7일 미만의 메시지에 대해 메시지 추적을 실행하면 메시지가 5~30분 이내에 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-155">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span>  <br/> <span data-ttu-id="80b07-156">7일이 지난 메시지에 대해 메시지 추적을 실행하면 결과가 표시되는 데 최대 몇 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80b07-156">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="80b07-157">데이터 사용 가능 여부 및 대기 시간은 Office 365 관리 센터 또는 원격 PowerShell을 통해 요청 여부.</span><span class="sxs-lookup"><span data-stu-id="80b07-157">Data availability and latency is the same whether requested via the Office 365 admin center or remote PowerShell.</span></span> 
  

