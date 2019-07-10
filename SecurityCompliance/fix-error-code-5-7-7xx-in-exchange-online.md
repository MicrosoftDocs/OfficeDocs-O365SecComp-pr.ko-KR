---
title: Exchange Online에서 오류 코드 5.7.7 xx에 해당 하는 전자 메일 배달 문제 수정
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 06/11/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Exchange Online에서 오류 코드 5.7.7 xx의 전자 메일 문제를 해결 하는 방법에 대해 알아봅니다 (테 넌 트 차단 됨).
ms.openlocfilehash: d55bc1f8a051a7f9932528a75aac8f1efa18911c
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599334"
---
# <a name="fix-email-delivery-issues-for-error-code-577xx-in-exchange-online"></a><span data-ttu-id="0da71-103">Exchange Online에서 오류 코드 5.7.7 xx에 해당 하는 전자 메일 배달 문제 수정</span><span class="sxs-lookup"><span data-stu-id="0da71-103">Fix email delivery issues for error code 5.7.7xx in Exchange Online</span></span>

<span data-ttu-id="0da71-104">이 항목에서는 배달 못 함 보고서 (NDR, 바운스 메시지, 배달 상태 알림 또는 DSN이 라고도 함)에 상태 코드 550 5.7.7 xx가 표시 되는 경우에 수행할 수 있는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-104">This topic describes what you can do if you see status code 550 5.7.7xx in a non-delivery report (also known as an NDR, bounce message, delivery status notification, or DSN).</span></span> <span data-ttu-id="0da71-105">테 넌 트가 단방향 이나 다른 방법으로 전자 메일을 보낼 수 없도록 제한 되 면이 자동 알림을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-105">You'll see this automated notification when your tenant is restricted from sending email in one way or another.</span></span> <span data-ttu-id="0da71-106">이러한 오류 코드는 대개 705 또는 750로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-106">These error codes will usually come in as 705 or 750.</span></span>

## <a name="57705-tenant-has-exceeded-threshold-restriction-what-you-need-to-know"></a><span data-ttu-id="0da71-107">5.7.705: 테 넌 트가 임계값 제한을 초과 했습니다. 확인 해야 할 사항</span><span class="sxs-lookup"><span data-stu-id="0da71-107">5.7.705: Tenant has exceeded threshold restriction: What you need to know</span></span>

<span data-ttu-id="0da71-108">테 넌 트가 손상 된 경우 메일을 보내려고 할 때마다 내부 보낸 사람이이 NDR을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-108">Internal senders could see this NDR whenever you try to send mail if your tenant was compromised.</span></span> <span data-ttu-id="0da71-109">일반적으로 테 넌 트의 트래픽 대부분이 의심 스러운 것으로 감지 되어 테 넌 트에 대 한 보내기 기능을 사용할 수 없는 경우에 occus.</span><span class="sxs-lookup"><span data-stu-id="0da71-109">This usually occus when the majority of traffic from your tenant has been detected as suspicious and has resulted in a ban on sending ability for the tenant.</span></span> <span data-ttu-id="0da71-110">사용자가 Office 365에서 대량의 대량 메일을 보내는 경우에도이 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-110">This can also occur if your users send an large amount of bulk mail from Office 365.</span></span> <span data-ttu-id="0da71-111">서비스 설명에 명시 된 것 처럼 합법적인 대량 상업용 전자 메일 (예: 고객 회보)을 보내야 하는 Exchange Online 고객은 이러한 서비스를 전문적으로 제공 하는 타사 공급자를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-111">As stated in the service description, Exchange Online customers who need to send legitimate bulk commercial email (for example, customer newsletters) should use third-party providers that specialize in these services.</span></span>

<span data-ttu-id="0da71-112">사용자가 테 넌 트로 통칭 하 여 서비스를 통해 의심 스러운 메일을 보내면 모든 사용자가 문제를 해결할 때까지 메일을 보내지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-112">Once your users collectively, as a tenant, send a certain amount of suspicious mail through the service, all users can be prevented from sending any mail until the problem is fixed.</span></span> <span data-ttu-id="0da71-113">사용자에 게 다음과 같은 내용의 배달 못 함 보고서 (NDR)를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-113">Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="0da71-114">550 5.7.705 액세스 거부, 테 넌 트가 임계값을 초과 함</span><span class="sxs-lookup"><span data-stu-id="0da71-114">550 5.7.705 Access denied, tenant has exceeded threshold</span></span>

## <a name="57750-unregistered-domain-email-restriction-what-you-need-to-know"></a><span data-ttu-id="0da71-115">5.7.750: 등록 되지 않은 도메인 전자 메일 제한: 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="0da71-115">5.7.750: Unregistered Domain Email restriction: What you need to know</span></span>

<span data-ttu-id="0da71-116">Office 365을 사용 하면 테 넌 트에서 Exchange Online Protection (EOP)을 통해 일부 메시지를 릴레이할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-116">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP).</span></span> <span data-ttu-id="0da71-117">이 예에서는 사용자가 Office 365 사서함을 사용 하 고 외부 사용자가 전자 메일을 보낼 때 전자 메일 전달이 구성 되는 경우를 예로 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-117">One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox.</span></span> <span data-ttu-id="0da71-118">이는 학생 들이 자신의 개인 전자 메일 인터페이스를 활용 하지만 학교와 관련 된 전자 메일이 전송 되는 교육 환경에서 가장 자주 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-118">This is most common in education environments where students want to leverage their personal email interface but still get emails related to school.</span></span> <span data-ttu-id="0da71-119">다른 예로는 고객이 하이브리드 시나리오에 있고 EOP에서 전자 메일을 보내는 온-프레미스 서버가 있는 경우를 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-119">Another example is when customers are in a hybrid scenario and have on-premises servers that send email out of EOP.</span></span>

### <a name="problems-with-unregistered-domains"></a><span data-ttu-id="0da71-120">등록 되지 않은 도메인 문제</span><span class="sxs-lookup"><span data-stu-id="0da71-120">Problems with unregistered domains</span></span>

<span data-ttu-id="0da71-121">이 문제는 온-프레미스 서버가 손상 되 고 종료 되 면 많은 양의 스팸을 EOP에서 릴레이할 때 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-121">The problem is when on-premises servers get compromised and end up relaying a large volume of spam out of EOP.</span></span> <span data-ttu-id="0da71-122">거의 모든 경우에 적절 한 커넥터를 설정 했지만 등록 되지 않은 도메인에서 전자 메일을 전송 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-122">In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains.</span></span> <span data-ttu-id="0da71-123">Office 365을 사용 하면 등록 되지 않은 도메인에서 합당 한 메일을 가져올 수 있지만, 허용 도메인은 외부에서 송신을 수행 하려는 각 도메인에 대해 관리 센터에서 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-123">Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="0da71-124">일단 손상 되 면 테 넌 트에서 등록 되지 않은 도메인에 대 한 아웃 바운드 메일을 보낼 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-124">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains.</span></span> <span data-ttu-id="0da71-125">사용자에 게 다음과 같은 내용의 배달 못 함 보고서 (NDR)를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-125">Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="0da71-126">550 5.7.750 서비스를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-126">550 5.7.750 Service unavailable.</span></span> <span data-ttu-id="0da71-127">클라이언트가 등록 되지 않은 도메인에서 보내지 못하도록 차단 됨</span><span class="sxs-lookup"><span data-stu-id="0da71-127">Client blocked from sending from unregistered domains</span></span>

## <a name="how-to-unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="0da71-128">다시 보내기 위해 테 넌 트의 차단을 해제 하는 방법</span><span class="sxs-lookup"><span data-stu-id="0da71-128">How to unblocking tenant in order to send again</span></span>

<span data-ttu-id="0da71-129">전자 메일을 보내기 위해 테 넌 트가 차단 된 경우에는 몇 가지 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-129">There are several things you need to do if your tenant get blocked for sending email:</span></span>

1. <span data-ttu-id="0da71-130">모든 도메인을 Microsoft 365 관리 센터에 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-130">Make sure that you register all of your domains in Microsoft 365 admin center.</span></span> <span data-ttu-id="0da71-131">자세한 내용은 [여기](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-131">More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="0da71-132">비정상적인 커넥터를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-132">Look for unusual connectors.</span></span> <span data-ttu-id="0da71-133">악의적인 행위자는 종종 Office 365 테 넌 트에서 새 인바운드 커넥터를 만들어 스팸을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-133">Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam.</span></span> <span data-ttu-id="0da71-134">커넥터를 확인 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-134">More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="0da71-135">온-프레미스 서버를 잠그고 해당 서버가 손상 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-135">Lock down your on-premises servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="0da71-136">특히 타사 서버인 경우에는 여기에 포함 되는 여러 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-136">There are many factors involved here, especially if these are third-party servers.</span></span> <span data-ttu-id="0da71-137">서버에서 나가는 모든 메일을 사용할 수 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-137">Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="0da71-138">작업이 완료 되 면 Microsoft 지원 서비스에 문의 하 여 등록 되지 않은 도메인에서 다시 보내기 위해 테 넌 트의 차단 해제를 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-138">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.</span></span>  <span data-ttu-id="0da71-139">오류 코드를 제공 하는 것이 도움이 되지만 환경이 보호 되 고 스팸이 다시 보내지지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-139">Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again.</span></span> <span data-ttu-id="0da71-140">지원 사례를 여는 방법에 대 한 자세한 내용은 [여기](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-140">More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="0da71-141">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="0da71-141">For more information</span></span>

[<span data-ttu-id="0da71-142">Office 365 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="0da71-142">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="0da71-143">Office 365의 전자 메일 배달 못 함 보고서(NDR)</span><span class="sxs-lookup"><span data-stu-id="0da71-143">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="0da71-144">사서함의 전자 메일 전달 구성</span><span class="sxs-lookup"><span data-stu-id="0da71-144">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="0da71-145">Office 365를 사용하여 전자 메일을 보내도록 다기능 장치 또는 응용 프로그램을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="0da71-145">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="0da71-146">[Exchange Online에서 허용 도메인을 관리](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)합니다.</span><span class="sxs-lookup"><span data-stu-id="0da71-146">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
