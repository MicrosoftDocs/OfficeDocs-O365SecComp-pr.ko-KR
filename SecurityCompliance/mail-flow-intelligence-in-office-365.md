---
title: Office 365의 메일 흐름 인텔리전스
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: 관리자가 커넥터를 사용 하 여 Office 365 (로 알려져 메일 흐름 인텔리전스)의 메시지 배달과 관련 된 오류 코드를 알 수 있습니다.
ms.openlocfilehash: 9f27dfd4c265eb62028d68c27764183202692ef4
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327090"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="a3016-103">Office 365의 메일 흐름 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="a3016-103">Mail flow intelligence in Office 365</span></span>

<span data-ttu-id="a3016-p101">일반적으로 사용 하 여 커넥터를 온-프레미스 전자 메일 환경에 Office 365 조직에서 전자 메일 메시지를 라우팅합니다. 수도 커넥터를 사용 하는 메시지를 라우팅할 Office 365에서 파트너 조직에 합니다. Office 365 커넥터를 통해 이러한 메시지를 배달할 수 없는, 하는 경우 Office 365에서 큐에 대기는 있습니다. Office 365 48 시간에 대 한 각 메시지에 대 한 배달 다시 시도를 계속 됩니다. 48 시간 후 큐에 대기 중인된 메시지 만료 됩니다 하 고 메시지 배달 못함 보고서 (라고도 하는 NDR 또는 튀어오르 메시지로)에서 원래 보낸사람에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p101">Typically, you use a connector to route email messages from your Office 365 organization to your on-premises email environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>

<span data-ttu-id="a3016-p102">Office 365 커넥터를 사용 하 여 메시지를 배달할 수 없는 경우에 오류가 발생 합니다. 가장 일반적인 오류 및 그 솔루션이이 항목에서 설명 합니다. 전체적으로, 큐 및 알림 오류 커넥터를 통해 전송 된 배달할 수 없는 메시지에 대 한 _메일 흐름 인텔리전스_이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p102">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as _mail flow intelligence_.</span></span>

## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="a3016-112">오류 코드: 450 4.4.312 DNS 쿼리가 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-112">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="a3016-p103">일반적으로이 오류는 Office 365에서 연결선을 하지만 실패 스마트 호스트의 IP 주소를 찾으려면 DNS 쿼리 변수에 지정 된 스마트 호스트에 연결 하려고을 의미 합니다. 이 오류에 대 한 가능한 원인은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p103">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host's IP addresses failed. The possible causes for this error are:</span></span>

- <span data-ttu-id="a3016-115">도메인의 DNS 호스팅 서비스 (도메인에 대 한 신뢰할 수 있는 이름 서버를 유지 관리 하는 사용자)에 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-115">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>

- <span data-ttu-id="a3016-116">도메인 최근에 만료 MX 레코드를 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-116">Your domain has recently expired, so the MX record can't be retrieved.</span></span>

- <span data-ttu-id="a3016-117">도메인의 MX 레코드 최근에 변경 하 고 Office 365 DNS 서버 여전히 이전에 캐시 되지 않은 도메인에 대 한 DNS 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-117">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>

### <a name="how-do-i-fix-error-code-450-44312"></a><span data-ttu-id="a3016-118">오류 코드 450 4.4.312를 해결 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="a3016-118">How do I fix error code 450 4.4.312?</span></span>

- <span data-ttu-id="a3016-119">식별 하 고 도메인 문제를 해결 하려면 DNS 호스팅 서비스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-119">Work with your DNS hosting service to identify and fix the problem with your domain.</span></span>

- <span data-ttu-id="a3016-120">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-120">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="a3016-121">오류 코드: 450 4.4.315 연결 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-121">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="a3016-p104">일반적으로, 즉, Office 365 대상 전자 메일 서버에 연결할 수 없습니다. 오류 세부 정보는 문제에 설명 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a3016-p104">Typically, this means Office 365 can't connect to the destination email server. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="a3016-125">온-프레미스 전자 메일 서버 작동이 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-125">Your on-premises email server is down.</span></span>

- <span data-ttu-id="a3016-126">Office 365가 잘못 된 IP 주소에 연결 하려고 하므로 커넥터의 스마트 호스트 설정에는 오류가입니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-126">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>

### <a name="how-do-i-fix-error-code-450-44315"></a><span data-ttu-id="a3016-127">오류 코드 450 4.4.315를 해결 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="a3016-127">How do I fix error code 450 4.4.315?</span></span>

- <span data-ttu-id="a3016-p105">사용자에 게 적용 시나리오 확인 하 고 필요한 내용을 수정 합니다. 예, 메일 흐름에 된 제대로 작동 하는 경우 커넥터 설정을 변경 하지 않은 해야하는 서버 작동이 중지, 또는 모든 변경 사항이 네트워크 인프라에 (예: 하는 경우를 확인합니다 하려면 온-프레미스 전자 메일 환경을 확인합니다 변경한 후 인터넷 서비스 공급자 수 있도록 이제 다른 IP 주소)입니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p105">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises email environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed internet service providers, so you now have different IP addresses).</span></span>

- <span data-ttu-id="a3016-130">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-130">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="a3016-131">오류 코드: 450 4.4.316 연결이 거부 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-131">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="a3016-p106">일반적으로이 오류는 대상 전자 메일 서버에 연결 하려고 할 때 연결 오류가 발생 하는 Office 365를 의미 합니다. 이 오류에 대 한 가능성이 원인은 방화벽은 Office 365 IP 주소에서 연결을 차단 하는 것입니다. 또는 온-프레미스 Office 365에 시스템으로 전자 메일 및 온-프레미스 전자 메일 환경을 종료 마이그레이션된 완전히 했을 때 경우 디자인 하 여이 오류가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p106">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination email server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises email system to Office 365 and shut down your on-premises email environment.</span></span>

### <a name="how-do-i-fix-error-code-450-44316"></a><span data-ttu-id="a3016-135">오류 코드 450 4.4.316를 해결 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="a3016-135">How do I fix error code 450 4.4.316?</span></span>

- <span data-ttu-id="a3016-p107">온-프레미스 환경에서 사서함을 설치한 경우 TCP 포트 25에서 Office 365 IP 주소에서 온-프레미스 전자 메일 서버에 연결을 허용 하도록 방화벽 설정을 수정 해야 합니다. Office 365 IP 주소 목록, [Office 365 Url 및 IP 주소 범위를](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a3016-p107">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises email servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span></span>

- <span data-ttu-id="a3016-p108">온-프레미스 환경에 더 이상 메시지가 전달 해야을 하는 경우 클릭 **지금 수정** 알림에서 Office 365 잘못 된 받는 사람으로 메시지를 거부 즉시 수 있도록 합니다. 이렇게 하면 기본 메시지 배달에 영향을 줄 수 있는 잘못 된 받는 사람에 대 한 조직의 할당량을 초과 하는 위험을 줄일 수 있습니다. 또는 다음 지침을 사용 하 여 수동으로 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p108">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span>

  - <span data-ttu-id="a3016-141">Office 365에서 [Exchange 관리 센터 (EAC)를](https://docs.microsoft.com/Exchange/exchange-admin-center) 사용 하지 않도록 설정 하거나 온-프레미스 전자 메일 환경에 Office 365에서 전자 메일을 제공 하는 커넥터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-141">In the [Exchange admin center (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365, disable or delete the connector that delivers email from Office 365 to your on-premises email environment:</span></span>

    1. <span data-ttu-id="a3016-142">EAC에서 **메일 흐름** 으로 이동 \> **커넥터**입니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-142">In the EAC, go to **Mail flow** \> **Connectors**.</span></span>

    2. <span data-ttu-id="a3016-143">**Office 365** 의 **에서** 값을 가진 커넥터 및 **조직의 전자 메일 서버** 값을 \*\*\*\* 선택한 다음 단계 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-143">Select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server** and do one of the following steps:</span></span>

       - <span data-ttu-id="a3016-144">**삭제** 를 클릭 하 여 커넥터를 삭제 ![제거 아이콘](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span><span class="sxs-lookup"><span data-stu-id="a3016-144">Delete the connector by clicking **Delete** ![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span></span>

       - <span data-ttu-id="a3016-145">**편집** 을 클릭 하 여 커넥터를 사용 하지 않도록 설정 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **켜는**선택을 취소 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-145">Disable the connector by clicking **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) and unchecking **Turn it on**.</span></span>

  - <span data-ttu-id="a3016-p109">Office 365에 연결 된 **신뢰할**수 있음으로 **내부 릴레이** 에서 온-프레미스 전자 메일 환경에서 허용된 도메인을 변경 합니다. 자세한 내용은 [관리 허용 도메인 Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a3016-p109">Change the accepted domain in Office 365 that's associated with your on-premises email environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span></span>

  <span data-ttu-id="a3016-p110">**참고**: 일반적으로 이러한 변경은 1 시간 30 분 사이 내용을 적용 합니다. 1 시간 후 오류 더이상 수신 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p110">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>

- <span data-ttu-id="a3016-150">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-150">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="a3016-151">오류 코드: 450 4.4.317 원격 서버에 연결할 수 없음</span><span class="sxs-lookup"><span data-stu-id="a3016-151">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="a3016-p111">일반적으로이 오류는 대상 전자 메일 서버에 연결 된 Office 365 되지만 서버는 즉시 오류가 발생 하 여 응답 한 또는 연결 요구 사항에 맞지 않는 의미 합니다. 오류 세부 정보는 문제에 설명 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a3016-p111">Typically, this error means Office 365 connected to the destination email server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="a3016-155">대상 전자 메일 서버 응답 "서비스를 사용할 수 없습니다." 오류를 Office 365와의 통신을 유지할 수는 하는 서버를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-155">The destination email server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>

- <span data-ttu-id="a3016-156">커넥터가 TLS를 요구 하도록 구성 되어 있지만 대상 전자 메일 서버에서 TLS를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-156">The connector is configured to require TLS, but the destination email server doesn't support TLS.</span></span>

### <a name="how-do-i-fix-error-code-450-44317"></a><span data-ttu-id="a3016-157">오류 코드 450 4.4.317를 해결 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="a3016-157">How do I fix error code 450 4.4.317?</span></span>

- <span data-ttu-id="a3016-158">TLS 설정 및 온-프레미스 전자 메일 서버에 인증서 및 커넥터에 TLS 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-158">Verify the TLS settings and certificates on your on-premises email servers, and the TLS settings on the connector.</span></span>

- <span data-ttu-id="a3016-159">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-159">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="a3016-160">오류 코드: 연결이 갑자기 닫혔습니다 450 4.4.318</span><span class="sxs-lookup"><span data-stu-id="a3016-160">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="a3016-p112">일반적으로이 오류는 Office 365 문제가 연결이 끊어졌습니다 있으므로 온-프레미스 전자 메일 환경을와 통신을 의미 합니다. 이 오류에 대 한 가능한 원인은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p112">Typically, this error means Office 365 is having difficulty communicating with your on-premises email environment, so the connection was dropped. The possible causes for this error are:</span></span>

- <span data-ttu-id="a3016-163">SMTP 패킷 검사 규칙을 사용 하 여 방화벽 및 이러한 규칙 정상적으로 작동 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-163">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>

- <span data-ttu-id="a3016-164">온-프레미스 전자 메일 서버에 대상으로 작업 올바르게 (예:, 서비스 중단, 작동 중단, 또는 시스템 리소스가 부족) 서버 시간 초과를 발생 하는 없으며 Office 365에 대 한 연결을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-164">Your on-premises email server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>

- <span data-ttu-id="a3016-165">온-프레미스 환경과 Office 365 간에 네트워크 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-165">There are network issues between your on-premises environment and Office 365.</span></span>

### <a name="how-do-i-fix-error-code-450-44318"></a><span data-ttu-id="a3016-166">오류 코드 450 4.4.318를 해결 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="a3016-166">How do I fix error code 450 4.4.318?</span></span>

- <span data-ttu-id="a3016-167">사용자에 게 적용 시나리오 확인 하 고 필요한 내용을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-167">Find out which scenario applies to you, and make the necessary corrections.</span></span>

- <span data-ttu-id="a3016-168">온-프레미스 환경과 Office 365 간의 네트워크 문제로 인해 문제가 발생 하는 경우이 문제를 해결 하 여 네트워크 팀에 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-168">If the problem is caused by network issues between your on-premises environment and Office 365, contact your network team to troubleshoot the issue.</span></span>

- <span data-ttu-id="a3016-169">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-169">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="a3016-170">오류 코드: 450 4.7.320 인증서 유효성 검사 실패</span><span class="sxs-lookup"><span data-stu-id="a3016-170">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="a3016-p113">일반적으로이 오류는 대상 전자 메일 서버 인증서의 유효성을 검사 하는 동안 오류가 발생 하는 Office 365를 의미 합니다. 오류 세부 정보는 오류를 설명 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a3016-p113">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination email server. The error details will explain the error. For example:</span></span>

- <span data-ttu-id="a3016-174">인증서 만료</span><span class="sxs-lookup"><span data-stu-id="a3016-174">Certificate expired</span></span>

- <span data-ttu-id="a3016-175">인증서 주체 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-175">Certificate subject mismatch</span></span>

- <span data-ttu-id="a3016-176">인증서는 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-176">Certificate is no longer valid</span></span>

### <a name="how-do-i-fix-error-code-450-47320"></a><span data-ttu-id="a3016-177">오류 코드 450 4.7.320를 해결 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="a3016-177">How do I fix error code 450 4.7.320?</span></span>

- <span data-ttu-id="a3016-178">인증서를 수정 하거나 커넥터에 대 한 설정을 Office 365에서 메시지 큐에서 대기를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-178">Fix the certificate or the settings on the connector so that queued messages in Office 365 can be delivered.</span></span>

- <span data-ttu-id="a3016-179">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="other-error-codes"></a><span data-ttu-id="a3016-180">기타 오류 코드</span><span class="sxs-lookup"><span data-stu-id="a3016-180">Other error codes</span></span>

<span data-ttu-id="a3016-p114">Office 365에서 온-프레미스에 메시지를 배달 문제가 또는 파트너 관계를 전자 메일 서버입니다. 오류 메시지에 **대상 서버** 정보를 사용 하 여 사용자 환경에서 문제를 검사 하거나 구성 오류가 있을 경우 커넥터를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-p114">Office 365 is having difficulty delivering messages to your on-premises or partner email server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 

<span data-ttu-id="a3016-183">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3016-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
