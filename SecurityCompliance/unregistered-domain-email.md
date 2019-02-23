---
title: 등록 되지 않은 도메인 전자 메일
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: 등록 되지 않은 도메인 전자 메일을 대량 전송 하는 경우 전자 메일 차단 위험이 실행 됩니다. 자세한 내용은이 문서를 참조 하세요.
ms.openlocfilehash: bef39780438a6d9669354bddaed391b2364badf8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220778"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="850b5-104">등록 되지 않은 도메인 전자 메일: 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="850b5-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="850b5-p102">Office 365을 사용 하면 테 넌 트에서 Exchange Online Protection (EOP)을 통해 일부 메시지를 릴레이할 수 있습니다. 이 예에서는 사용자가 Office 365 사서함을 사용 하 고 외부 사용자가 전자 메일을 보낼 때 전자 메일 전달이 구성 되는 경우를 예로 들 수 있습니다. 이는 학생 들이 자신의 개인 전자 메일 인터페이스를 활용 하지만 학교와 관련 된 전자 메일이 전송 되는 교육 환경에서 가장 자주 발생 합니다. 다른 예로는 고객이 하이브리드 시나리오에 있고 EOP에서 전자 메일을 보내는 온-프레미스 서버가 있는 경우를 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-p102">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP). One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox. This is most common in education environments where students want to leverage their personal email interface but still get emails related to school. Another example is when customers are in a hybrid scenario and have on-premises servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="850b5-109">등록 되지 않은 도메인 문제</span><span class="sxs-lookup"><span data-stu-id="850b5-109">Problems with unregistered domains</span></span>

<span data-ttu-id="850b5-p103">이 문제는 온-프레미스 서버가 손상 되 고 종료 되 면 많은 양의 스팸을 EOP에서 릴레이할 때 발생 합니다. 거의 모든 경우에 적절 한 커넥터를 설정 했지만 등록 되지 않은 도메인에서 전자 메일을 전송 하 고 있습니다. Office 365을 사용 하면 등록 되지 않은 도메인에서 합당 한 메일을 가져올 수 있지만, 허용 도메인은 외부에서 송신을 수행 하려는 각 도메인에 대해 관리 센터에서 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-p103">The problem is when on-premises servers get compromised and end up relaying a large volume of spam out of EOP. In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains. Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="850b5-p104">일단 손상 되 면 테 넌 트에서 등록 되지 않은 도메인에 대 한 아웃 바운드 메일을 보낼 수 없게 됩니다. 사용자에 게 다음과 같은 내용의 배달 못 함 보고서 (NDR)를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-p104">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains. Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="850b5-p105">550 5.7.750 서비스를 사용할 수 없습니다. 클라이언트가 등록 되지 않은 도메인에서 보내지 못하도록 차단 됨</span><span class="sxs-lookup"><span data-stu-id="850b5-p105">550 5.7.750 Service unavailable. Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="850b5-117">다시 보내기 위해 테 넌 트 차단 해제</span><span class="sxs-lookup"><span data-stu-id="850b5-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="850b5-118">등록 되지 않은 도메인에서 보내기를 차단 하면 몇 가지 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="850b5-p106">모든 도메인을 Office 365 관리 센터에 등록 해야 합니다. 자세한 내용은 [여기](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-p106">Make sure that you register all of your domains in Office 365 admin center. More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="850b5-p107">비정상적인 커넥터를 찾습니다. 악의적인 행위자는 종종 Office 365 테 넌 트에서 새 인바운드 커넥터를 만들어 스팸을 보냅니다. 커넥터를 확인 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-p107">Look for unusual connectors. Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam. More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="850b5-124">온-프레미스 서버를 잠그고 해당 서버가 손상 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-124">Lock down your on-premises servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="850b5-p108">특히 타사 서버인 경우에는 여기에 포함 되는 여러 요소가 있습니다. 서버에서 나가는 모든 메일을 사용할 수 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-p108">There are many factors involved here, especially if these are third-party servers. Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="850b5-p109">작업이 완료 되 면 Microsoft 지원 서비스에 문의 하 여 등록 되지 않은 도메인에서 다시 보내기 위해 테 넌 트의 차단 해제를 요청 해야 합니다.  오류 코드를 제공 하는 것이 도움이 되지만 환경이 보호 되 고 스팸이 다시 보내지지 않도록 해야 합니다. 지원 사례를 여는 방법에 대 한 자세한 내용은 [여기](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-p109">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.  Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again. More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="850b5-130">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="850b5-130">For more information</span></span>

[<span data-ttu-id="850b5-131">Office 365 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="850b5-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="850b5-132">Office 365의 전자 메일 배달 못 함 보고서(NDR)</span><span class="sxs-lookup"><span data-stu-id="850b5-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="850b5-133">사서함의 전자 메일 전달 구성</span><span class="sxs-lookup"><span data-stu-id="850b5-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="850b5-134">Office 365를 사용하여 전자 메일을 보내도록 다기능 장치 또는 응용 프로그램을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="850b5-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="850b5-135">[Exchange Online에서 허용 도메인을 관리](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)합니다.</span><span class="sxs-lookup"><span data-stu-id="850b5-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
