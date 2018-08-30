---
title: Office 365의 메일 흐름 인텔리전스
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/27/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: '일반적으로 커넥터를 사용 하는 메시지를 라우팅할 Office 365 조직에서 온-프레미스 메시징 환경을 합니다. 수도 커넥터를 사용 하는 메시지를 라우팅할 Office 365에서 파트너 조직에 합니다. Office 365 커넥터를 통해 이러한 메시지를 배달할 수 없는, 하는 경우 Office 365에서 큐에 대기는 있습니다. '
ms.openlocfilehash: 4effbb783d6ba8f3b33d0aed446e031193d2f2a3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002729"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="b7376-105">Office 365의 메일 흐름 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="b7376-105">Mail flow intelligence in Office 365</span></span>
  
<span data-ttu-id="b7376-p102">일반적으로 커넥터를 사용 하는 메시지를 라우팅할 Office 365 조직에서 온-프레미스 메시징 환경을 합니다. 수도 커넥터를 사용 하는 메시지를 라우팅할 Office 365에서 파트너 조직에 합니다. Office 365 커넥터를 통해 이러한 메시지를 배달할 수 없는, 하는 경우 Office 365에서 큐에 대기는 있습니다. Office 365 48 시간에 대 한 각 메시지에 대 한 배달 다시 시도를 계속 됩니다. 48 시간 후 큐에 대기 중인된 메시지 만료 됩니다 하 고 메시지 배달 못함 보고서 (라고도 하는 NDR 또는 튀어오르 메시지로)에서 원래 보낸사람에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p102">Typically, you use a connector to route messages from your Office 365 organization to your on-premises messaging environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>
  
<span data-ttu-id="b7376-p103">Office 365 커넥터를 사용 하 여 메시지를 배달할 수 없는 경우에 오류가 발생 합니다. 가장 일반적인 오류 및 그 솔루션이이 항목에서 설명 합니다. 전체적으로, 큐 및 알림 오류 커넥터를 통해 전송 된 배달할 수 없는 메시지에 대 한 메일 흐름 인텔리전스 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p103">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as mailflow intelligence.</span></span>
  
 <span data-ttu-id="b7376-114">**목차**</span><span class="sxs-lookup"><span data-stu-id="b7376-114">**Contents**</span></span>
  
- [<span data-ttu-id="b7376-115">오류 코드: 450 4.4.312 DNS 쿼리가 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-115">Error code: 450 4.4.312 DNS query failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44312)
    
- [<span data-ttu-id="b7376-116">오류 코드: 450 4.4.315 연결 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-116">Error code: 450 4.4.315 Connection timed out</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44315)
    
- [<span data-ttu-id="b7376-117">오류 코드: 450 4.4.316 연결이 거부 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-117">Error code: 450 4.4.316 Connection refused</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44316)
    
- [<span data-ttu-id="b7376-118">오류 코드: 450 4.4.317 원격 서버에 연결할 수 없음</span><span class="sxs-lookup"><span data-stu-id="b7376-118">Error code: 450 4.4.317 Cannot connect to remote server</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44317)
    
- [<span data-ttu-id="b7376-119">오류 코드: 연결이 갑자기 닫혔습니다 450 4.4.318</span><span class="sxs-lookup"><span data-stu-id="b7376-119">Error code: 450 4.4.318 Connection was closed abruptly</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44318)
    
- [<span data-ttu-id="b7376-120">오류 코드: 450 4.7.320 인증서 유효성 검사 실패</span><span class="sxs-lookup"><span data-stu-id="b7376-120">Error code: 450 4.7.320 Certificate validation failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode47320)
    
## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="b7376-121">오류 코드: 450 4.4.312 DNS 쿼리가 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-121">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="b7376-p104">이 오류는 Office 365의 커넥터에 지정 된 스마트 호스트에 연결 하려고 하지만 DNS 쿼리를 찾으려면 스마트 호스트 IP 주소를 의미 일반적으로 실패 합니다. 이 오류에 대 한 가능한 원인은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p104">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host IP addresses failed. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="b7376-124">도메인의 DNS 호스팅 서비스 (도메인에 대 한 신뢰할 수 있는 이름 서버를 유지 관리 하는 사용자)에 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-124">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>
    
- <span data-ttu-id="b7376-125">도메인 최근에 만료 MX 레코드를 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-125">Your domain has recently expired, so the MX record can't be retrieved.</span></span>
    
- <span data-ttu-id="b7376-126">도메인의 MX 레코드 최근에 변경 하 고 Office 365 DNS 서버 여전히 이전에 캐시 되지 않은 도메인에 대 한 DNS 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-126">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>
    
<span data-ttu-id="b7376-127">DNS 호스팅 서비스를 사용 하 여 DNS 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-127">You need to fix the DNS issue by working with your DNS hosting service.</span></span>
  
<span data-ttu-id="b7376-128">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-128">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="b7376-129">오류 코드: 450 4.4.315 연결 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-129">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="b7376-p105">일반적으로, 즉, Office 365 대상 메시징 서버에 연결할 수 없습니다. 오류 세부 정보는 문제에 설명 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="b7376-p105">Typically, this means Office 365 can't connect to the destination messaging server. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="b7376-133">온-프레미스 메시징 서버가 다운 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-133">Your on-premises messaging server is down.</span></span>
    
- <span data-ttu-id="b7376-134">Office 365가 잘못 된 IP 주소에 연결 하려고 하므로 커넥터의 스마트 호스트 설정에는 오류가입니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-134">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>
    
<span data-ttu-id="b7376-p106">사용자에 게 적용 시나리오 확인 하 고 필요한 내용을 수정 합니다. 예, 메일 흐름에 된 제대로 작동 하는 경우 커넥터 설정을 변경 되지 않았는지 확인 해야 온-프레미스 메시징 환경을 서버 작동이 중지, 또는 모든 변경 사항이 네트워크 인프라에 (예: 하는 경우를 확인 변경한 후 인터넷 서비스 공급자 수 있도록 이제 다른 IP 주소)입니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p106">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises messaging environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed Internet service providers, so you now have different IP addresses).</span></span>
  
<span data-ttu-id="b7376-137">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-137">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="b7376-138">오류 코드: 450 4.4.316 연결이 거부 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-138">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="b7376-p107">일반적으로이 오류는 대상 메시징 서버에 연결 하려고 할 때 연결 오류가 발생 하는 Office 365를 의미 합니다. 이 오류에 대 한 가능성이 원인은 방화벽은 Office 365 IP 주소에서 연결을 차단 하는 것입니다. 온-프레미스 메시징 시스템을 Office 365 및 온-프레미스 종료 마이그레이션된 완전히 했을 때 하는 경우이 오류가 디자인 여 될 수 또는 메시징 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p107">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination messaging server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises messaging system to Office 365 and shut down your on-premises messaging environment..</span></span>
  
- <span data-ttu-id="b7376-p108">온-프레미스에 TCP 포트 25에서 Office 365 IP 주소에서 연결을 허용 하도록 방화벽 설정을 수정 해야 온-프레미스 환경에서 사서함을 설치한 경우 메시징 서버. Office 365 IP 주소 목록, [Office 365 Url 및 IP 주소 범위를](https://go.microsoft.com/fwlink/p/?linkid=228887)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b7376-p108">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises messaging servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=228887).</span></span>
    
- <span data-ttu-id="b7376-p109">온-프레미스 환경에 더 이상 메시지가 전달 해야을 하는 경우 클릭 **지금 수정** 알림에서 Office 365 잘못 된 받는 사람으로 메시지를 거부 즉시 수 있도록 합니다. 이렇게 하면 기본 메시지 배달에 영향을 줄 수 있는 잘못 된 받는 사람에 대 한 조직의 할당량을 초과 하는 위험을 줄일 수 있습니다. 또는 다음 지침을 사용 하 여 수동으로 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p109">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span> 
    
  - <span data-ttu-id="b7376-p110">사용 하지 않거나 온-프레미스 환경에 Office 365에서 연결선을 삭제: Office 365 관리 센터 \> **관리 센터** \> **Exchange** \> **메일 흐름** \> **커넥터** \> 선택은 **Office 365** 의 **에서** 값을 가진 커넥터 및 **를** **조직의 전자 메일 서버**값입니다. **삭제**를 클릭 하 여 커넥터를 삭제![삭제 아이콘](media/ITPro-EAC-DeleteIcon.gif), **편집** 을 클릭 하 여 커넥터를 사용 하지 않도록 설정 하거나 ![편집 아이콘](media/ITPro-EAC-EditIcon.gif) **켜는**선택을 취소 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p110">Disable or delete the connector from Office 365 to your on-premises environment: Office 365 admin center \> **Admin centers** \> **Exchange** \> **Mail flow** \> **Connectors** \> select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server**. Delete the connector by clicking **Delete**![Delete icon](media/ITPro-EAC-DeleteIcon.gif), or disable the connector by clicking **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif) and unchecking **Turn it on**.</span></span>
    
  - <span data-ttu-id="b7376-p111">온-프레미스와 관련 된 Office 365에서 허용된 도메인을 변경 **신뢰할**수 있음으로 메시징 환경에서 **내부 릴레이** 합니다. 자세한 내용은 [Exchange Online에서 허용 도메인 관리](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b7376-p111">Change the accepted domain in Office 365 that's associated with your on-premises messaging environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span></span>
    
    <span data-ttu-id="b7376-p112">**참고**: 일반적으로 이러한 변경은 1 시간 30 분 사이 내용을 적용 합니다. 1 시간 후 오류 더이상 수신 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p112">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>
    
<span data-ttu-id="b7376-153">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-153">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="b7376-154">오류 코드: 450 4.4.317 원격 서버에 연결할 수 없음</span><span class="sxs-lookup"><span data-stu-id="b7376-154">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="b7376-p113">일반적으로이 오류는 대상 메시징 서버에 연결 된 Office 365 되지만 서버는 즉시 오류가 발생 하 여 응답 한 또는 연결 요구 사항에 맞지 않는 의미 합니다. 오류 세부 정보는 문제에 설명 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="b7376-p113">Typically, this error means Office 365 connected to the destination messaging server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="b7376-158">대상 메시징 서버는 "서비스를 사용할 수 없음" 오류가 발생 하 여 응답 한 Office 365와의 통신을 유지할 수는 하는 서버를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-158">The destination messaging server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>
    
- <span data-ttu-id="b7376-159">커넥터가 TLS를 요구 하도록 구성 되어 있지만 대상 메시징 서버에서 TLS를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-159">The connector is configured to require TLS, but the destination messaging server doesn't support TLS.</span></span>
    
<span data-ttu-id="b7376-160">TLS 설정 및 온-프레미스에 인증서를 확인 메시징 서버 및 커넥터에 TLS 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-160">Verify the TLS settings and certificates on your on-premises messaging servers, and the TLS settings on the connector.</span></span>
  
<span data-ttu-id="b7376-161">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-161">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="b7376-162">오류 코드: 연결이 갑자기 닫혔습니다 450 4.4.318</span><span class="sxs-lookup"><span data-stu-id="b7376-162">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="b7376-p114">일반적으로이 오류는 의미 Office 365 문제가 온-프레미스와의 통신 메시징 환경을 하므로 연결이 끊어졌습니다. 이 오류에 대 한 가능한 원인은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p114">Typically, this error means Office 365 is having difficulty communicating with your on-premises messaging environment, so the connection was dropped. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="b7376-165">SMTP 패킷 검사 규칙을 사용 하 여 방화벽 및 이러한 규칙 정상적으로 작동 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-165">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>
    
- <span data-ttu-id="b7376-166">온-프레미스 메시징 서버가 작동 하지 않으면 올바르게 (예: 서비스 중단, 작동 중단, 또는 시스템 리소스가 부족)는 Office 365에 대 한 연결을 닫고 서버 시간 초과 인해 생깁니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-166">Your on-premises messaging server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>
    
- <span data-ttu-id="b7376-p115">온-프레미스 환경과 Office 365 간에 네트워크 문제가 있습니다. 문제가 계속 되 면이 문제를 해결 하 여 네트워크 팀에 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p115">There are network issues between your on-premises environment and Office 365. If the problem persists, contact your network team to troubleshoot the issue.</span></span>
    
<span data-ttu-id="b7376-169">사용자에 게 적용 시나리오 확인 하 고 필요한 내용을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-169">Find out which scenario applies to you, and make the necessary corrections.</span></span>
  
<span data-ttu-id="b7376-170">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-170">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="b7376-171">오류 코드: 450 4.7.320 인증서 유효성 검사 실패</span><span class="sxs-lookup"><span data-stu-id="b7376-171">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="b7376-p116">일반적으로이 오류는 대상 메시징 서버 인증서의 유효성을 검사 하는 동안 오류가 발생 하는 Office 365를 의미 합니다. 오류 세부 정보는 오류를 설명 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="b7376-p116">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination messaging server. The error details will explain the error. For example:</span></span>
  
- <span data-ttu-id="b7376-175">인증서 만료</span><span class="sxs-lookup"><span data-stu-id="b7376-175">Certificate expired</span></span>
    
- <span data-ttu-id="b7376-176">인증서 주체 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-176">Certificate subject mismatch</span></span>
    
- <span data-ttu-id="b7376-177">인증서는 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-177">Certificate is no longer valid</span></span>
    
<span data-ttu-id="b7376-178">수정 하십시오 인증서 또는 커넥터 Office 365can에서 큐에 대기 중인된 메시지를 배달할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-178">Please fix the certificate or the connector so that queued messages in Office 365can be delivered.</span></span>
  
<span data-ttu-id="b7376-179">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="other-error-codes"></a><span data-ttu-id="b7376-180">기타 오류 코드</span><span class="sxs-lookup"><span data-stu-id="b7376-180">Other error codes</span></span>

<span data-ttu-id="b7376-p117">Office 365는 온-프레미스 또는 파트너 메시징 서버를 시도해봅니다 전달 메시지 것입니다. 오류 메시지에 **대상 서버** 정보를 사용 하 여 사용자 환경에서 문제를 검사 하거나 구성 오류가 있을 경우 커넥터를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-p117">Office 365 is having difficulty delivering messages to your on-premises or partner messaging server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 
  
<span data-ttu-id="b7376-183">파트너 조직 (예는 타사 클라우드 서비스 공급자)에서 오류가 발생 한 것을 하는 경우 문제를 해결 하 여 파트너에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7376-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  

