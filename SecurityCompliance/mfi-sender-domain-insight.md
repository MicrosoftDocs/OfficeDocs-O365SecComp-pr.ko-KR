---
title: 보낸 사람 도메인 정보 문제 해결
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: 관리자는 보안 & 준수 센터의 메일 흐름 대시보드에서 보낸 사람 도메인에 대 한 정보를 수정 하는 방법에 대해 알아볼 수 있습니다.
ms.openlocfilehash: 89c94616d612fa02c067e0bc2a89f5a3be704ed5
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598064"
---
# <a name="fix-sender-domain-insight"></a><span data-ttu-id="5104f-103">보낸 사람 도메인 정보 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5104f-103">Fix sender domain insight</span></span>

<span data-ttu-id="5104f-104">Office 365에서는 특정 보안 조건을 충족 하기 위해 내부 온-프레미스 전자 메일 환경에서 Office 365로 메시지를 전송 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-104">Office 365 requires messages sending from internal on-premises email environments to Office 365 to meet certain security criteria:</span></span>

- <span data-ttu-id="5104f-105">원본 IP 주소 또는 인증서를 사용 하 여 온-프레미스 전자 메일 서버에서 SMTP 연결을 인증 하기 위해 Office 365의 인바운드 커넥터를 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-105">You've created an inbound connector in Office 365 to authenticate SMTP connections from your on-premises email server by using the source IP address or a certificate.</span></span>

- <span data-ttu-id="5104f-106">Office 365을 통해 외부 세계를 통해 전자 메일을 릴레이 하도록 온-프레미스 전자 메일 서버를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-106">You've configured your on-premises email server to relay email via Office 365 to external world.</span></span>

- <span data-ttu-id="5104f-107">구성에서 다음 문 중 하나에 해당 하는 경우:</span><span class="sxs-lookup"><span data-stu-id="5104f-107">In your configuration, one of the following statements is true:</span></span>

  - <span data-ttu-id="5104f-108">보낸 사람의 전자 메일 도메인이 Office 365 조직에 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-108">The sender's email domain is registered in your Office 365 organization.</span></span> <span data-ttu-id="5104f-109">자세한 내용은 Office 365에서 도메인 추가를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5104f-109">For more information, see Add Domains in Office 365.</span></span>

  - <span data-ttu-id="5104f-110">온-프레미스 전자 메일 서버는 인증서를 사용 하 여 office 365에 전자 메일을 보내거나, 인증서에 Office 365에 등록 한 도메인 이름과 정확히 일치 하거나, 인증서 기반 365 커넥터를 만든 사용자가이를 포함 하도록 구성 됩니다. 도메인별.</span><span class="sxs-lookup"><span data-stu-id="5104f-110">Your on-premises email server is configured to use a certificate to send email to Office 365, the certificate contains or exactly matches a domain name that you've registered in Office 365, and you've created a certificate based connector in Office 365 with that domain.</span></span> 

<span data-ttu-id="5104f-111">조건을 충족 하지 않는 메시지는 조직에 대 한 특성을 사용 하지 않으며 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-111">Messages that don't meet the criteria will not be attributed to the organization and could be rejected.</span></span>

<span data-ttu-id="5104f-112">**Fix sender domain** 통찰력은 온-프레미스 환경에서 조건을 충족 하지 않는 전자 메일을 표시 하 고, 온-프레미스 전자 메일 환경에서 잠재적으로 손상 된 컴퓨터와 사용자 계정을 식별 하 고, 작업을 수행 하는 데 도움이 됩니다. 수정 작업</span><span class="sxs-lookup"><span data-stu-id="5104f-112">The **Fix sender domain** insight shows you email from your on-premises environment that doesn't meet the criteria, helps you to identify potentially compromised machines and user accounts in your on-premises email environment, and helps you to take remediation actions.</span></span>

![보안 & 준수 센터의 메일 흐름 대시보드에서 보낸 사람 도메인 통찰력 수정](media/sender-domain-insight-selected.png)

<span data-ttu-id="5104f-114">**자세히 보기**를 클릭 하면 다음 다이어그램에 나와 있는 것과 같이 다른 widget이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-114">When you click **View details**, you are taken to another widget with more details as shown in the following diagram:</span></span>

![보낸 사람 도메인 문제 해결의 세부 정보 위젯](media/sender-domain-view-details.png)

<span data-ttu-id="5104f-116">메시지를 Office 365로 배달 하는 데 사용 된 인바운드 커넥터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-116">You'll see the inbound connector that was used to deliver the messages to Office 365.</span></span> <span data-ttu-id="5104f-117">**예제 메시지 id 보기** 를 클릭 하 여 온-프레미스 전자 메일 환경에서 전송 된 메시지에 대 한 세부 정보를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-117">You can also click **view sample message IDs** to see details for the messages that were sent from your on-premises email environment.</span></span> <span data-ttu-id="5104f-118">이러한 메시지는 Office 365에서 거부 되었기 때문에 메시지 추적을 사용할 수는 없지만, 샘플 메시지 id를 사용 하 여 온-프레미스 전자 메일 환경에서 메시지를 추적할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5104f-118">Because these messages were rejected by Office 365, you can't use message trace, but you can use the sample message ids to track the messages in your on-premises email environment.</span></span>

![보낸 사람 도메인 정보 수정에서 예제 메시지 id 보기](media/sender-domain-view-sample-message-ids.png)

## <a name="see-also"></a><span data-ttu-id="5104f-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5104f-120">See also</span></span>

<span data-ttu-id="5104f-121">메일 흐름 대시보드의 다른 메일 흐름 정보에 대 한 자세한 내용은 [Security & 준수 센터의 메일 흐름 정보](mail-flow-insights-v2.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="5104f-121">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
