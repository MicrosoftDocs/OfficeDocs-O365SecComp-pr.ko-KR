---
title: Office 365의 메일 흐름 인텔리전스
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: 관리자는 메일 흐름 인텔리전스 라고도 하는 Office 365의 커넥터를 사용 하 여 메시지 배달과 관련 된 오류 코드에 대해 알아볼 수 있습니다.
ms.openlocfilehash: a679a3a50c2333a9f66509b69ec06ee96960bc83
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218718"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="e407b-103">Office 365의 메일 흐름 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="e407b-103">Mail flow intelligence in Office 365</span></span>

<span data-ttu-id="e407b-p101">일반적으로는 커넥터를 사용 하 여 Office 365 조직에서 온-프레미스 전자 메일 환경으로 전자 메일 메시지를 라우팅합니다. 또한 커넥터를 사용 하 여 Office 365에서 파트너 조직으로 메시지를 라우팅할 수 있습니다. office 365에서 커넥터를 통해 이러한 메시지를 배달할 수 없으면 office 365에서 큐에 대기 됩니다. Office 365에서는 각 메시지에 대해 48 시간 동안 계속 해 서 배달을 다시 시도 합니다. 48 시간이 지난 후에 대기 된 메시지는 만료 되며 메시지는 배달 못 함 보고서 (NDR 또는 바운스 메시지로도 알려짐)의 원래 보낸 사람에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p101">Typically, you use a connector to route email messages from your Office 365 organization to your on-premises email environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>

<span data-ttu-id="e407b-p102">커넥터를 사용 하 여 메시지를 배달할 수 없으면 Office 365에서 오류가 발생 합니다. 이 항목에서는 가장 일반적인 오류와 해결 방법에 대해 설명 합니다. 커넥터를 통해 전송 되는 배달할 수 없는 메시지에 대 한 큐 및 알림 오류를 집합적으로 _메일 흐름 인텔리전스_라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p102">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as _mail flow intelligence_.</span></span>

## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="e407b-112">오류 코드: 450 4.4.312 DNS 쿼리 실패</span><span class="sxs-lookup"><span data-stu-id="e407b-112">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="e407b-p103">일반적으로이 오류는 Office 365이 커넥터에 지정 된 스마트 호스트에 연결 하려고 했지만 스마트 호스트의 IP 주소를 찾기 위한 DNS 쿼리가 실패 했음을 의미 합니다. 이 오류는 다음과 같은 경우에 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p103">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host's IP addresses failed. The possible causes for this error are:</span></span>

- <span data-ttu-id="e407b-115">도메인의 DNS 호스팅 서비스 (도메인에 대해 신뢰할 수 있는 이름 서버를 유지 관리 하는 당사자)에 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-115">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>

- <span data-ttu-id="e407b-116">최근에 도메인 만료로 인해 MX 레코드를 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-116">Your domain has recently expired, so the MX record can't be retrieved.</span></span>

- <span data-ttu-id="e407b-117">도메인의 MX 레코드가 최근에 변경 되었으며 Office 365 dns 서버에 도메인에 대 한 이전에 캐시 된 dns 정보가 여전히 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-117">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>

### <a name="how-do-i-fix-error-code-450-44312"></a><span data-ttu-id="e407b-118">오류 코드 450 4.4.312를 수정 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="e407b-118">How do I fix error code 450 4.4.312?</span></span>

- <span data-ttu-id="e407b-119">DNS 호스팅 서비스를 사용 하 여 도메인 문제를 식별 하 고 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-119">Work with your DNS hosting service to identify and fix the problem with your domain.</span></span>

- <span data-ttu-id="e407b-120">타사 클라우드 서비스 공급자와 같은 파트너 조직에서 오류가 발생 한 경우에는 해당 파트너에 문의 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-120">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="e407b-121">오류 코드: 450 4.4.315 연결 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-121">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="e407b-p104">일반적으로이는 Office 365에서 대상 전자 메일 서버에 연결할 수 없음을 의미 합니다. 오류 세부 정보에 문제에 대 한 설명이 나와 있습니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e407b-p104">Typically, this means Office 365 can't connect to the destination email server. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="e407b-125">온-프레미스 전자 메일 서버가 다운 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-125">Your on-premises email server is down.</span></span>

- <span data-ttu-id="e407b-126">커넥터의 스마트 호스트 설정에 오류가 발생 하 여 Office 365에서 잘못 된 IP 주소에 연결 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-126">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>

### <a name="how-do-i-fix-error-code-450-44315"></a><span data-ttu-id="e407b-127">오류 코드 450 4.4.315를 수정 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="e407b-127">How do I fix error code 450 4.4.315?</span></span>

- <span data-ttu-id="e407b-p105">사용자에 게 적용 되는 시나리오를 확인 하 고 필요한 사항을 수정 합니다. 예를 들어 메일 흐름이 정상적으로 작동 하 고 커넥터 설정을 변경 하지 않은 경우에는 온-프레미스 전자 메일 환경을 확인 하 여 서버가 다운 되었는지, 아니면 네트워크 인프라가 변경 되었는지 여부 (예: 인터넷 서비스 공급자를 변경 했으므로 이제 다른 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p105">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises email environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed internet service providers, so you now have different IP addresses).</span></span>

- <span data-ttu-id="e407b-130">타사 클라우드 서비스 공급자와 같은 파트너 조직에서 오류가 발생 한 경우에는 해당 파트너에 문의 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-130">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="e407b-131">오류 코드: 450 4.4.316 연결이 거부 됨</span><span class="sxs-lookup"><span data-stu-id="e407b-131">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="e407b-p106">일반적으로이 오류는 대상 전자 메일 서버에 연결 하려고 할 때 Office 365에서 연결 오류가 발생 했음을 의미 합니다. 이 오류는 방화벽이 Office 365 IP 주소 로부터의 연결을 차단 하는 경우에 발생할 수 있습니다. 또는 온-프레미스 전자 메일 시스템을 Office 365로 완전히 마이그레이션하고 온-프레미스 전자 메일 환경을 종료 한 경우이 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p106">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination email server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises email system to Office 365 and shut down your on-premises email environment.</span></span>

### <a name="how-do-i-fix-error-code-450-44316"></a><span data-ttu-id="e407b-135">오류 코드 450 4.4.316를 수정 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="e407b-135">How do I fix error code 450 4.4.316?</span></span>

- <span data-ttu-id="e407b-p107">온-프레미스 환경에 사서함이 있는 경우 TCP 포트 25의 Office 365 IP 주소에서 온-프레미스 전자 메일 서버에 연결할 수 있도록 방화벽 설정을 수정 해야 합니다. office 365 ip 주소 목록은 [office 365 url 및 IP 주소 범위](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e407b-p107">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises email servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span></span>

- <span data-ttu-id="e407b-p108">온-프레미스 환경으로 더 이상 메시지를 배달 하지 않을 경우에는 알림에서 **지금 해결** 을 클릭 하 여 Office 365에서 잘못 된 받는 사람이 있는 메시지를 즉시 거부할 수 있도록 합니다. 이렇게 하면 정상적인 메시지 배달에 영향을 줄 수 있는 잘못 된 받는 사람에 대 한 조직의 할당량을 초과할 위험이 줄어듭니다. 또는 다음 지침을 사용 하 여 문제를 수동으로 해결할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p108">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span>

  - <span data-ttu-id="e407b-141">office 365의 [EAC (Exchange 관리 센터)](https://docs.microsoft.com/Exchange/exchange-admin-center) 에서 office 365에서 온-프레미스 전자 메일 환경으로 전자 메일을 배달 하는 커넥터를 사용 하지 않도록 설정 하거나 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-141">In the [Exchange admin center (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365, disable or delete the connector that delivers email from Office 365 to your on-premises email environment:</span></span>

    1. <span data-ttu-id="e407b-142">EAC에서 **메일 흐름** \> **커넥터로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-142">In the EAC, go to **Mail flow** \> **Connectors**.</span></span>

    2. <span data-ttu-id="e407b-143">**From** 값 **Office 365** 과 **To** 값이 포함 된 커넥터를 선택 하 고 **조직의 전자 메일 서버** 를 선택한 후 다음 단계 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-143">Select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server** and do one of the following steps:</span></span>

       - <span data-ttu-id="e407b-144">**삭제** ![아이콘 제거를 클릭 하 여 커넥터를 삭제 합니다.](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span><span class="sxs-lookup"><span data-stu-id="e407b-144">Delete the connector by clicking **Delete** ![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span></span>

       - <span data-ttu-id="e407b-145">편집 아이콘 \*\*\*\* ![](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) 편집 및 선택 취소를 클릭 하 여 \*\*\*\* 커넥터를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-145">Disable the connector by clicking **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) and unchecking **Turn it on**.</span></span>

  - <span data-ttu-id="e407b-p109">온-프레미스 전자 메일 환경과 연결 된 Office 365의 허용 도메인을 **내부 중계** 에서 **신뢰할**수 있는 것으로 변경 합니다. 자세한 내용은 [Exchange Online에서 허용 도메인 관리](https://go.microsoft.com/fwlink/p/?linkid=785428)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e407b-p109">Change the accepted domain in Office 365 that's associated with your on-premises email environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span></span>

  <span data-ttu-id="e407b-p110">**참고**: 일반적으로 이러한 변경 내용은 30 분에서 1 시간 마다 적용 됩니다. 1 시간 후에 오류가 더 이상 표시 되지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p110">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>

- <span data-ttu-id="e407b-150">타사 클라우드 서비스 공급자와 같은 파트너 조직에서 오류가 발생 한 경우에는 파트너에 문의 하 여 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-150">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="e407b-151">오류 코드: 450 4.4.317 원격 서버에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-151">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="e407b-p111">일반적으로이 오류는 Office 365이 대상 전자 메일 서버에 연결 되어 있지만 서버에서 즉각적인 오류가 발생 하거나 연결 요구 사항을 충족 하지 않는 것을 의미 합니다. 오류 세부 정보에 문제에 대 한 설명이 나와 있습니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e407b-p111">Typically, this error means Office 365 connected to the destination email server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="e407b-155">대상 전자 메일 서버가 "서비스를 사용할 수 없습니다." 라는 오류와 함께 응답 하 여 서버가 Office 365과의 통신을 유지할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-155">The destination email server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>

- <span data-ttu-id="e407b-156">커넥터가 tls를 요구 하도록 구성 되었지만 대상 전자 메일 서버에서 tls를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-156">The connector is configured to require TLS, but the destination email server doesn't support TLS.</span></span>

### <a name="how-do-i-fix-error-code-450-44317"></a><span data-ttu-id="e407b-157">오류 코드 450 4.4.317를 수정 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="e407b-157">How do I fix error code 450 4.4.317?</span></span>

- <span data-ttu-id="e407b-158">온-프레미스 전자 메일 서버 및 커넥터의 tls 설정에 대 한 tls 설정 및 인증서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-158">Verify the TLS settings and certificates on your on-premises email servers, and the TLS settings on the connector.</span></span>

- <span data-ttu-id="e407b-159">타사 클라우드 서비스 공급자와 같은 파트너 조직에서 오류가 발생 한 경우에는 파트너에 문의 하 여 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-159">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="e407b-160">오류 코드: 450 4.4.318 연결이 갑자기 닫혔습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-160">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="e407b-p112">일반적으로이 오류는 Office 365이 온-프레미스 전자 메일 환경과 통신 하는 데 어려움이 있어 연결이 끊어진 것을 의미 합니다. 이 오류는 다음과 같은 경우에 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p112">Typically, this error means Office 365 is having difficulty communicating with your on-premises email environment, so the connection was dropped. The possible causes for this error are:</span></span>

- <span data-ttu-id="e407b-163">방화벽은 SMTP 패킷 검사 규칙을 사용 하며, 이러한 규칙은 제대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-163">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>

- <span data-ttu-id="e407b-164">온-프레미스 전자 메일 서버가 제대로 작동 하지 않습니다 (예: 서비스 멈춤, 크래시 또는 낮은 시스템 리소스) .이로 인해 서버가 시간 초과 되어 Office 365에 대 한 연결을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-164">Your on-premises email server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>

- <span data-ttu-id="e407b-165">온-프레미스 환경과 Office 365 간에 네트워크 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-165">There are network issues between your on-premises environment and Office 365.</span></span>

### <a name="how-do-i-fix-error-code-450-44318"></a><span data-ttu-id="e407b-166">오류 코드 450 4.4.318를 수정 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="e407b-166">How do I fix error code 450 4.4.318?</span></span>

- <span data-ttu-id="e407b-167">사용자에 게 적용 되는 시나리오를 확인 하 고 필요한 사항을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-167">Find out which scenario applies to you, and make the necessary corrections.</span></span>

- <span data-ttu-id="e407b-168">문제가 온-프레미스 환경과 Office 365 간의 네트워크 문제로 인해 발생 하는 경우 네트워크 팀에 연락 하 여 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-168">If the problem is caused by network issues between your on-premises environment and Office 365, contact your network team to troubleshoot the issue.</span></span>

- <span data-ttu-id="e407b-169">타사 클라우드 서비스 공급자와 같은 파트너 조직에서 오류가 발생 한 경우에는 파트너에 문의 하 여 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-169">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="e407b-170">오류 코드: 450 4.7.320 인증서 유효성 검사 실패</span><span class="sxs-lookup"><span data-stu-id="e407b-170">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="e407b-p113">일반적으로이 오류는 대상 전자 메일 서버의 인증서 유효성을 검사 하는 동안 Office 365에서 오류가 발생 했음을 의미 합니다. 오류 세부 정보에 오류 설명이 나와 있습니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e407b-p113">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination email server. The error details will explain the error. For example:</span></span>

- <span data-ttu-id="e407b-174">인증서가 만료 됨</span><span class="sxs-lookup"><span data-stu-id="e407b-174">Certificate expired</span></span>

- <span data-ttu-id="e407b-175">인증서 주체가 일치 하지 않음</span><span class="sxs-lookup"><span data-stu-id="e407b-175">Certificate subject mismatch</span></span>

- <span data-ttu-id="e407b-176">인증서가 더 이상 유효 하지 않음</span><span class="sxs-lookup"><span data-stu-id="e407b-176">Certificate is no longer valid</span></span>

### <a name="how-do-i-fix-error-code-450-47320"></a><span data-ttu-id="e407b-177">오류 코드 450 4.7.320를 수정 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="e407b-177">How do I fix error code 450 4.7.320?</span></span>

- <span data-ttu-id="e407b-178">Office 365에서 대기 중인 메시지를 배달할 수 있도록 커넥터의 설정 또는 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-178">Fix the certificate or the settings on the connector so that queued messages in Office 365 can be delivered.</span></span>

- <span data-ttu-id="e407b-179">타사 클라우드 서비스 공급자와 같은 파트너 조직에서 오류가 발생 한 경우에는 파트너에 문의 하 여 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="other-error-codes"></a><span data-ttu-id="e407b-180">기타 오류 코드</span><span class="sxs-lookup"><span data-stu-id="e407b-180">Other error codes</span></span>

<span data-ttu-id="e407b-p114">Office 365에서 온-프레미스 또는 파트너 전자 메일 서버에 메시지를 배달 하는 데 어려움이 있습니다. 오류의 **대상 서버** 정보를 사용 하 여 사용자 환경의 문제를 확인 하거나, 구성 오류가 있으면 커넥터를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-p114">Office 365 is having difficulty delivering messages to your on-premises or partner email server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 

<span data-ttu-id="e407b-183">타사 클라우드 서비스 공급자와 같은 파트너 조직에서 오류가 발생 한 경우에는 파트너에 문의 하 여 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e407b-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
