---
title: SMTP 인증 클라이언트 보고서
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: 관리자는 Security & 준수 센터의 메일 흐름 대시보드에서 SMTP 인증 클라이언트 보고서에 대해 알아볼 수 있습니다.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: b6698345a89edf52e4ee14cea144cb88ff080583
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998711"
---
# <a name="smtp-auth-clients-report"></a><span data-ttu-id="675fc-103">SMTP 인증 클라이언트 보고서</span><span class="sxs-lookup"><span data-stu-id="675fc-103">SMTP Auth clients report</span></span>

> [!NOTE]
> <span data-ttu-id="675fc-104">이 항목에서 설명 하는 기능은 모든 Office 365 조직에 배포 되지 않으며 변경 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="675fc-105">**smtp 인증 클라이언트** 보고서는 조직의 사용자 또는 시스템 계정으로 smtp 인증 클라이언트 전송 프로토콜을 사용 하는 것을 강조 합니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-105">The **SMTP Auth clients** report highlights the use of the SMTP Auth client submission protocol by users or system accounts in your organization.</span></span> <span data-ttu-id="675fc-106">끝점 smtp.office365.com를 사용 하는이 레거시 프로토콜은 기본 인증만 제공 하며 손상 된 계정에서 전자 메일을 보내기 위해 사용 하는 것이 취약 합니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-106">This legacy protocol (which uses the endpoint smtp.office365.com) only offers Basic authentication, and is susceptible to being used by compromised accounts to send email.</span></span>  <span data-ttu-id="675fc-107">이 보고서를 사용 하면 비정상적인 활동을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-107">This report allows you to check for unusual activity.</span></span> <span data-ttu-id="675fc-108">또한 SMTP 인증을 사용 하는 클라이언트나 장치에 대 한 TLS 사용 현황 데이터를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-108">It also shows the TLS usage data for clients or devices using SMTP Auth.</span></span>

<span data-ttu-id="675fc-109">메일 흐름 대시보드에 표시 되는 위젯은 지난 7 일 이내에 SMTP 인증 프로토콜을 사용한 사용자 또는 서비스 계정 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-109">The widget that's shown in the Mail Flow dashboard indicates the number of users or service accounts that have used the SMTP Auth protocol in the last 7 days.</span></span>

![Security & 준수 센터의 메일 흐름 대시보드에서 SMTP 인증 클라이언트 보고서](media/smtp-auth-clients-report-selected.png)

<span data-ttu-id="675fc-111">위젯을 클릭 하면 지난 주에 대 한 TLS 사용 및 볼륨의 집계 된 보기를 제공 하는 플라이 아웃이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-111">Clicking on the widget opens a flyout that provides an aggregated view of the TLS usage and volumes for the last week.</span></span>

![SMTP 인증 클라이언트 보고서의 플라이 아웃](media/smtp-auth-clients-flyout.png)

<span data-ttu-id="675fc-113">**SMTP 인증 클라이언트 보고서** 링크를 클릭 하면 두 개의 기본 데이터 피벗 및 두 개의 데이터 보기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-113">When you click on the **SMTP Auth Clients Report** link, you'll see two main data pivots and two data views.</span></span> <span data-ttu-id="675fc-114">데이터 피벗은 **보내는 볼륨과** **TLS 사용**입니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-114">The data pivots are the **Sending Volume** and **TLS Usage**.</span></span> <span data-ttu-id="675fc-115">데이터 보기는 차트 및 세부 정보 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-115">The data views are the chart and the details table.</span></span>

<span data-ttu-id="675fc-116">**보내는 볼륨** 보기에는 지정 된 시간 범위 동안 SMTP 인증을 사용 하 여 보낸 메시지 수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-116">The **Sending Volume** view shows the number of messages that were sent using SMTP Auth for the specified time range.</span></span> <span data-ttu-id="675fc-117">**필터**를 클릭 하 여 범위를 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-117">You can adjust the range by clicking **Filters**.</span></span> <span data-ttu-id="675fc-118">차트가 보낸 사람 도메인으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-118">The chart is organized by sender domain.</span></span> <span data-ttu-id="675fc-119">드롭다운 **에 대 한 데이터 표시** 에서 도메인을 선택 하 여 각 도메인에 대해 개별 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-119">You can see separate data for each domain by selecting the domain in the **Show data for** drop down.</span></span>

![SMTP 인증 클라이언트 보고서의 보내는 볼륨](media/smtp-auth-clients-report-sending-volume.png)

<span data-ttu-id="675fc-121">**세부 정보 표 보기**를 클릭 하 여 보낸 사람 및 해당 메시지 수에 대 한 자세한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-121">You can view detailed information about the senders and their message counts by clicking **View details table**.</span></span> <span data-ttu-id="675fc-122">차트로 돌아가려면 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-122">To return to the chart, click **View report**.</span></span>

![SMTP 인증 클라이언트 보고서의 전송 볼륨에 대 한 정보 테이블](media/smtp-auth-clients-report-details-sending-volume.png)

<span data-ttu-id="675fc-124">**tls 사용** 피벗은 Office 365에서 tls 1.0 및 tls 1.1의 출시로 인해 중요 한 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-124">The **TLS Usage** pivot is important due to the upcoming deprecation of TLS1.0 and TLS1.1 in Office 365.</span></span> <span data-ttu-id="675fc-125">대부분의 레거시 장치 및 응용 프로그램은 SMTP 인증에서 tls 1.0을 사용할 수 있는 경우에만 전자 메일을 보낼 수 있습니다. 이 피벗은 이전 버전의 TLS를 사용 하는 사용자 및 시스템 계정을 식별 하 고이에 대 한 작업을 수행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-125">Many legacy devices and applications will be unable to send email if they are only capable of using TLS1.0 with SMTP Auth. This pivot allows you to identify and take action on users and system accounts that are still using older versions of TLS.</span></span>

![SMTP 인증 클라이언트 보고서의 TLS 사용](media/smtp-auth-clients-report-tls-usage.png)

<span data-ttu-id="675fc-127">보낸 사람에 대 한 자세한 정보, SMTP 인증을 사용 하는 TLS 버전, 그리고 **정보 테이블 보기**를 클릭 하 여 해당 메시지 개수를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-127">You can view detailed information about the senders, the versions of TLS they are using with SMTP Auth, and their message counts by clicking **View details table**.</span></span> <span data-ttu-id="675fc-128">차트로 돌아가려면 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-128">To return to the chart, click **View report**.</span></span>

<span data-ttu-id="675fc-129">보고서 요청을 클릭 하 여 자세한 보고서 버전을 다운로드할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="675fc-129">You can also download a more detailed version of the report by clicking Request report.</span></span>

![SMTP 인증 클라이언트 보고서의 TLS 사용에 대 한 정보 테이블](media/smtp-auth-clients-report-details-tls-usage.png)

## <a name="see-also"></a><span data-ttu-id="675fc-131">참고 항목</span><span class="sxs-lookup"><span data-stu-id="675fc-131">See also</span></span>

<span data-ttu-id="675fc-132">메일 흐름 대시보드의 다른 메일 흐름 정보에 대 한 자세한 내용은 [Security & 준수 센터의 메일 흐름 정보](mail-flow-insights-v2.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="675fc-132">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
