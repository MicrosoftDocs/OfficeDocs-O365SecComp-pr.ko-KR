---
title: Office 365로 전송한 문제 해결 메일
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 05/02/2016
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
ms.collection:
- M365-security-compliance
description: 이 문서에서는 Office 365의 받은 편지함에 전자 메일을 보내려고 할 때 문제가 발생 하는 보낸 사람에 대 한 문제 해결 정보와 Office 365 고객에 게 대량 메일을 전송 하기 위한 모범 사례를 제공 합니다.
ms.openlocfilehash: 9f4b5e8073c173da6638c30ccc5f123dc3b7a2a6
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600334"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a><span data-ttu-id="9624d-103">Office 365로 전송한 문제 해결 메일</span><span class="sxs-lookup"><span data-stu-id="9624d-103">Troubleshooting mail sent to Office 365</span></span>

<span data-ttu-id="9624d-104">이 문서에서는 Office 365의 받은 편지함에 전자 메일을 보내려고 할 때 문제가 발생 하는 보낸 사람에 대 한 문제 해결 정보와 Office 365 고객에 게 대량 메일을 전송 하기 위한 모범 사례를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-104">This article provides troubleshooting information for senders who are experiencing issues when trying to send email to inboxes in Office 365 and best practices for bulk mailing to Office 365 customers.</span></span>
  
## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a><span data-ttu-id="9624d-105">Office 365에 대 한 메일 배달과 관련 된 일반적인 문제 해결</span><span class="sxs-lookup"><span data-stu-id="9624d-105">Troubleshooting common problems with mail delivery to Office 365</span></span>

<span data-ttu-id="9624d-106">일반적으로 발생 하는 몇 가지 문제 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-106">Choose from one of these commonly encountered issues.</span></span>
  
- [<span data-ttu-id="9624d-107">IP 및 도메인의 전송 신뢰도를 관리 하 고 있나요?</span><span class="sxs-lookup"><span data-stu-id="9624d-107">Are you managing your IP and domain's sending reputation?</span></span>](troubleshooting-mail-sent-to-office-365.md#ManageRep)
    
- [<span data-ttu-id="9624d-108">새 IP 주소에서 전자 메일을 보내시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="9624d-108">Are you sending email from new IP addresses?</span></span>](troubleshooting-mail-sent-to-office-365.md#NewIPs)
    
- [<span data-ttu-id="9624d-109">DNS가 올바르게 설정 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="9624d-109">Confirm that your DNS is set up correctly</span></span>](troubleshooting-mail-sent-to-office-365.md#ConfirmDNSsetup)
    
- [<span data-ttu-id="9624d-110">사용자를 라우팅할 수 없는 IP로 알리지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-110">Ensure that you do not advertise yourself as a non-routable IP</span></span>](troubleshooting-mail-sent-to-office-365.md#NoReverseDNS)
    
- [<span data-ttu-id="9624d-111">Office 365에서 사용자에 게 전자 메일을 보낼 때 배달 못 함 보고서 (NDR)를 받은 경우</span><span class="sxs-lookup"><span data-stu-id="9624d-111">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>](troubleshooting-mail-sent-to-office-365.md#NDRInbound)
    
- [<span data-ttu-id="9624d-112">EOP의 받는 사람 정크 폴더에 있는 내 전자 메일 마법사로 돌아갑니다</span><span class="sxs-lookup"><span data-stu-id="9624d-112">My email landed in the recipient's junk folder in EOP</span></span>](troubleshooting-mail-sent-to-office-365.md#JunkMailBox)
    
- [<span data-ttu-id="9624d-113">내 IP 주소의 트래픽이 EOP에 의해 제한 됨</span><span class="sxs-lookup"><span data-stu-id="9624d-113">Traffic from my IP address is throttled by EOP</span></span>](troubleshooting-mail-sent-to-office-365.md#AllowEOPIPs)
    
### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a><span data-ttu-id="9624d-114">IP 및 도메인의 전송 신뢰도를 관리 하 고 있나요?</span><span class="sxs-lookup"><span data-stu-id="9624d-114">Are you managing your IP and domain's sending reputation?</span></span>
<span data-ttu-id="9624d-115"><a name="ManageRep"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-115"></span></span>

<span data-ttu-id="9624d-116">EOP 필터링 기술은 Microsoft Office 365에 대 한 스팸 방지 보호 기능 뿐 아니라 Exchange Server, Microsoft Office Outlook 및 Windows Live Mail과 같은 다른 Microsoft 제품을 제공 하도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-116">EOP filtering technologies are designed to provide anti-spam protections for Microsoft Office 365 as well as other Microsoft products like Exchange Server, Microsoft Office Outlook, and Windows Live Mail.</span></span> <span data-ttu-id="9624d-117">또한 SPF, DKIM 및 DMARC을 활용 합니다. 전자 메일을 보내는 도메인에 대해 권한이 부여 되었는지 확인 하 여 스푸핑 및 피싱 문제를 해결 하는 데 도움이 되는 전자 메일 인증 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-117">We also leverage SPF, DKIM, and DMARC; email authentication technologies that help address the problem of spoofing and phishing by verifying that the domain sending the email is authorized to do so.</span></span> <span data-ttu-id="9624d-118">EOP 필터링은 보내는 IP, 도메인, 인증, 목록 정확성, 불만 율, 콘텐츠 등에 관련 된 여러 요인의 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-118">EOP filtering is influenced by a number of factors related to the sending IP, domain, authentication, list accuracy, complaint rates, content and more.</span></span> <span data-ttu-id="9624d-119">이러한 방법 중 하나는 보낸 사람의 신뢰도를 추진 하는 보안 주체 요소와 전자 메일을 배달 하는 기능은 정크 메일 불만 률입니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-119">Of these, one of the principal factors in driving down a sender's reputation and their ability to deliver email is their junk email complaint rate.</span></span> 
  
### <a name="are-you-sending-email-from-new-ip-addresses"></a><span data-ttu-id="9624d-120">새 IP 주소에서 전자 메일을 보내시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="9624d-120">Are you sending email from new IP addresses?</span></span>
<span data-ttu-id="9624d-121"><a name="NewIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-121"></span></span>

<span data-ttu-id="9624d-122">전자 메일을 보내는 데 이전에 사용 되지 않은 IP 주소는 일반적으로 시스템에 신뢰가 구축 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-122">IP addresses not previously used to send email typically don't have any reputation built up in our systems.</span></span> <span data-ttu-id="9624d-123">따라서 새 Ip 로부터의 전자 메일에 배달 문제가 발생할 가능성이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-123">As a result, emails from new IPs are more likely to experience delivery issues.</span></span> <span data-ttu-id="9624d-124">IP가 스팸을 보내지 않는 신뢰도를 구축한 후에는 일반적으로 EOP에서 더 나은 전자 메일 배달 환경을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-124">Once the IP has built a reputation for not sending spam, EOP will typically allow for a better email delivery experience.</span></span>
  
<span data-ttu-id="9624d-125">기존 SPF 레코드에서 인증 된 도메인에 대해 추가 되는 새 Ip는 일반적으로 도메인의 전송 신뢰도 중 일부를 상속 하는 이점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-125">New IPs that are added for domains that are authenticated under existing SPF records typically experience the added benefit of inheriting some of the domain's sending reputation.</span></span> <span data-ttu-id="9624d-126">도메인에 신뢰도가 높은 새 Ip가 있으면 더 빠른 속도로 진입 하는 데 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-126">If your domain has a good sending reputation new IPs may experience a faster ramp up time.</span></span> <span data-ttu-id="9624d-127">새 IP는 볼륨, 목록 정확성 및 정크 메일 불만 율에 따라 몇 주 이내에 완전히 ramped 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-127">A new IP can expect to be fully ramped within a couple of weeks or sooner depending on volume, list accuracy, and junk email complaint rates.</span></span>
  
### <a name="confirm-that-your-dns-is-set-up-correctly"></a><span data-ttu-id="9624d-128">DNS가 올바르게 설정 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="9624d-128">Confirm that your DNS is set up correctly</span></span>
<span data-ttu-id="9624d-129"><a name="ConfirmDNSsetup"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-129"></span></span>

<span data-ttu-id="9624d-130">메일 라우팅에 필요한 MX 레코드를 포함 하 여 DNS 레코드를 만들고 유지 관리 하는 방법에 대 한 지침을 보려면 DNS 호스팅 공급자에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-130">For instructions about how to create and maintain DNS records, including the MX record required for mail routing, you will need to contact your DNS hosting provider.</span></span>
  
### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a><span data-ttu-id="9624d-131">사용자를 라우팅할 수 없는 IP로 알리지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-131">Ensure that you do not advertise yourself as a non-routable IP</span></span>
<span data-ttu-id="9624d-132"><a name="NoReverseDNS"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-132"></span></span>

<span data-ttu-id="9624d-133">역방향 DNS 조회에 실패 한 보낸 사람의 전자 메일은 수락 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-133">We may not accept email from senders who fail a reverse-DNS lookup.</span></span> <span data-ttu-id="9624d-134">경우에 따라 합법적인 보낸 사람이 EOP에 대 한 연결을 열려고 시도할 때 인터넷 라우팅 불가능 IP로 자신을 잘못 알리는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-134">In some cases, legitimate senders advertise themselves incorrectly as a non-internet routable IP when attempting to open a connection to EOP.</span></span> <span data-ttu-id="9624d-135">개인 (라우팅 불가능) 네트워킹에 대해 예약 된 IP 주소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-135">IP addresses that are reserved for private (non-routable) networking include:</span></span>
  
- <span data-ttu-id="9624d-136">192.168.0.0/16 (또는 192.168.0.0-192.168.255.255)</span><span class="sxs-lookup"><span data-stu-id="9624d-136">192.168.0.0/16 (or 192.168.0.0 - 192.168.255.255)</span></span>
    
- <span data-ttu-id="9624d-137">10.0.0.0/8 (또는 10.0.0.0-10.255.255.255)</span><span class="sxs-lookup"><span data-stu-id="9624d-137">10.0.0.0/8 (or 10.0.0.0 - 10.255.255.255)</span></span>
    
- <span data-ttu-id="9624d-138">172.16.0.0/11 (또는 172.16.0.0-172.31.255.255)</span><span class="sxs-lookup"><span data-stu-id="9624d-138">172.16.0.0/11 (or 172.16.0.0 - 172.31.255.255)</span></span>
    
### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a><span data-ttu-id="9624d-139">Office 365에서 사용자에 게 전자 메일을 보낼 때 배달 못 함 보고서 (NDR)를 받은 경우</span><span class="sxs-lookup"><span data-stu-id="9624d-139">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>
<span data-ttu-id="9624d-140"><a name="NDRInbound"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-140"></span></span>

<span data-ttu-id="9624d-141">Microsoft가 보낸 사람의 IP 주소를 차단 했거나, 사용자 계정이 이전 스팸 활동으로 인해 금지 된 보낸 사람으로 식별 되었기 때문에 일부 배달 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-141">Some delivery issues are the result of the sender's IP address being blocked by Microsoft or because the user account is identified as banned sender due to previous spam activity.</span></span> <span data-ttu-id="9624d-142">오류가 발생 한 NDR을 받은 것으로 생각 되 면 먼저 NDR 메시지의 지침을 따라 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-142">If you believe that you have received the NDR in error, first follow any instructions in the NDR message to resolve the issue.</span></span> 
  
<span data-ttu-id="9624d-143">수신 된 오류에 대 한 자세한 내용은 [온-프레미스 Exchange 2013 및 Office 365의 dsn 및 ndr](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx)의 전체 SMTP 오류 코드 목록을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9624d-143">For more information about the error you received, see the complete list of SMTP error codes in [DSNs and NDRs in On-Premises Exchange 2013 and Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).</span></span>
  
 <span data-ttu-id="9624d-144">예를 들어 다음 NDR이 수신 되는 경우 보내는 IP 주소가 Microsoft에 의해 차단 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-144">For example, if you receive the following NDR, it indicates that the sending IP address was blocked by Microsoft.</span></span> 
  
 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`
  
<span data-ttu-id="9624d-145">이 목록에서 제거를 요청 하려면 [목록 해제 포털을 사용 하 여 Office 365 수신 거부 목록에서 자신을 제거할](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-145">To request removal from this list, you can [Use the delist portal to remove yourself from the Office 365 blocked senders list](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span></span>
  
### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a><span data-ttu-id="9624d-146">EOP의 받는 사람 정크 폴더에 있는 내 전자 메일 마법사로 돌아갑니다</span><span class="sxs-lookup"><span data-stu-id="9624d-146">My email landed in the recipient's junk folder in EOP</span></span>
<span data-ttu-id="9624d-147"><a name="JunkMailBox"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-147"></span></span>

<span data-ttu-id="9624d-148">메시지가 EOP의 스팸으로 잘못 식별 된 경우 받는 사람과 협력 하 여 메시지를 평가 하 고 분석할 Microsoft 스팸 분석 팀에 게이 가양성 메시지를 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-148">If a message was incorrectly identified as spam by EOP, you can work with the recipient to submit this false positive message to the Microsoft Spam Analysis Team, who will evaluate and analyze the message.</span></span> <span data-ttu-id="9624d-149">분석 결과에 따라 메시지 통과를 허용하도록 서비스 전체적으로 스팸 콘텐츠 필터 규칙이 조정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-149">Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through.</span></span> <span data-ttu-id="9624d-150">전자 메일을 사용 하 여 스팸으로 분류 되어서는 안 되는 메시지를 Microsoft로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-150">You use email to submit messages to Microsoft that should not be classified as spam.</span></span> <span data-ttu-id="9624d-151">이 경우 다음 절차의 단계를 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-151">When doing so, be sure to use the steps in the following procedure.</span></span>
  
### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a><span data-ttu-id="9624d-152">전자 메일을 사용 하 여 Microsoft 스팸 분석 팀에 허위 긍정 메시지를 전송 하려면</span><span class="sxs-lookup"><span data-stu-id="9624d-152">To use email to submit false positive messages to the Microsoft Spam Analysis Team</span></span>

1. <span data-ttu-id="9624d-153">전송 하려는 메시지를 스팸이 아닌 것으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-153">Save the message you want to submit as non-spam.</span></span>
    
2. <span data-ttu-id="9624d-154">비어 있는 새 메시지를 작성하여 스팸이 아니라는 메시지를 첨부합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-154">Create a new, blank message and attach the non-spam message to it.</span></span>
    
    <span data-ttu-id="9624d-155">필요한 경우 스팸이 아닌 메시지를 여러 개 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-155">You can attach multiple non-spam messages if needed.</span></span>
    
3. <span data-ttu-id="9624d-156">원본 메시지의 제목 줄을 복사하여 새 메시지의 제목 줄에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-156">Copy and paste the original message subject line into the new message subject line.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="9624d-157">새 메시지의 본문은 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-157">Leave the body of the new message empty.</span></span> 
  
4. <span data-ttu-id="9624d-158">새 메시지를 [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com)으로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-158">Send your new message to [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).</span></span>
    
### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a><span data-ttu-id="9624d-159">내 IP 주소의 트래픽이 EOP에 의해 제한 됨</span><span class="sxs-lookup"><span data-stu-id="9624d-159">Traffic from my IP address is throttled by EOP</span></span>
<span data-ttu-id="9624d-160"><a name="AllowEOPIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-160"></span></span>

<span data-ttu-id="9624d-161">IP 주소가 EOP에 의해 제한 됨을 나타내는 EOP에서 NDR을 수신 하는 경우 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-161">If you receive an NDR from EOP that indicates that your IP address is being throttled by EOP, for example:</span></span>
  
 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`
  
<span data-ttu-id="9624d-162">IP 주소에서 의심 스러운 작업이 검색 되었으며 더 이상 평가 되는 동안 일시적으로 제한 되었기 때문에 NDR을 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-162">You received the NDR because suspicious activity has been detected from the IP address and it has been temporarily restricted while it is being further evaluated.</span></span> <span data-ttu-id="9624d-163">평가를 통해 suspicion를 지우면이 제한이 곧 리프트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-163">If the suspicion is cleared through evaluation, this restriction will be lifted shortly.</span></span>
  
### <a name="i-cant-receive-email-from-senders-in-office-365"></a><span data-ttu-id="9624d-164">Office 365의 보낸 사람 으로부터 전자 메일을 받을 수 없음</span><span class="sxs-lookup"><span data-stu-id="9624d-164">I can't receive email from senders in Office 365</span></span>
<span data-ttu-id="9624d-165"><a name="AllowEOPIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-165"></span></span>

 <span data-ttu-id="9624d-166">사용자가 보낸 메시지를 수신 하려면 네트워크에서 EOP에 사용 하는 IP 주소에서 연결을 허용 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-166">In order to receive messages from our users, make sure your network allows connections from the IP addresses that EOP uses in our datacenters.</span></span> <span data-ttu-id="9624d-167">자세한 내용은 [Exchange Online PROTECTION IP 주소](eop/exchange-online-protection-ip-addresses.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9624d-167">For more information, see [Exchange Online Protection IP addresses](eop/exchange-online-protection-ip-addresses.md).</span></span> 
  
## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a><span data-ttu-id="9624d-168">Office 365 사용자에 게 대량으로 전자 메일을 보내는 최상의 방법</span><span class="sxs-lookup"><span data-stu-id="9624d-168">Best practices for bulk emailing to Office 365 users</span></span>
<span data-ttu-id="9624d-169"><a name="BulkMailer"> </a></span><span class="sxs-lookup"><span data-stu-id="9624d-169"></span></span>

<span data-ttu-id="9624d-170">Office 365 사용자에 게 대량 전자 메일 캠페인을 자주 수행 하 고 전자 메일이 안전한 시간 및 시기 적절 하 게 도착 하는지 확인 하려면이 섹션의 팁을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-170">If you often conduct bulk email campaigns to Office 365 users and want to ensure that your emails arrive in a safe and timely manner, follow the tips in this section.</span></span>
  
### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a><span data-ttu-id="9624d-171">보낸 사람: 이름이 메시지를 보내는 사용자를 반영 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-171">Ensure that the From: name reflects who is sending the message</span></span>

<span data-ttu-id="9624d-172">제목은 메시지의 내용에 대 한 간략 한 요약으로, 메시지 본문은 명확 하 고 succinctly 제공, 서비스 또는 제품에 대 한 정보를 나타내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-172">The Subject should be a brief summary of what the message is about, and the message body should clearly and succinctly indicate what the offering, service, or product is about.</span></span> <span data-ttu-id="9624d-173">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-173">For example:</span></span>
  
<span data-ttu-id="9624d-174">맞는</span><span class="sxs-lookup"><span data-stu-id="9624d-174">Correct</span></span>
  
 ` From: marketing@shoppershandbag.com `
  
 `Subject: Updated catalog for the Christmas season!`
  
<span data-ttu-id="9624d-175">틀린</span><span class="sxs-lookup"><span data-stu-id="9624d-175">Incorrect</span></span>
  
 `From: someone@outlook.com`
  
 `Subject: Catalogs`
  
<span data-ttu-id="9624d-176">사용자가 사용자의 상황 및 수행 하는 작업을 쉽게 파악할 수 있도록 하므로 대부분의 스팸 필터를 통해 배달 하기가 더 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-176">The easier you make it for people to know who you are and what you are doing, the less difficulty you will have delivering through most spam filters.</span></span>
  
### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a><span data-ttu-id="9624d-177">캠페인 전자 메일에 항상 구독 취소 옵션 포함</span><span class="sxs-lookup"><span data-stu-id="9624d-177">Always include an unsubscribe option in campaign emails</span></span>

<span data-ttu-id="9624d-178">마케팅 전자 메일, 특히 뉴스레터에는 이후의 전자 메일에 대 한 구독 취소 방법이 항상 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-178">Marketing emails, especially newsletters, should always include a way of unsubscribing from future emails.</span></span> <span data-ttu-id="9624d-179">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-179">For example:</span></span>
  
 `This email was sent to example@contoso.com by sender@fabrikam.com.`
  
 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`
  
<span data-ttu-id="9624d-180">일부 보낸 사람에 게는 받는 사람이 제목에 "구독 취소"를 사용 하 여 특정 별칭으로 전자 메일을 보내도록 요청 하 여이 옵션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-180">Some senders include this option by requiring recipients to send an email to a certain alias with "Unsubscribe" in the subject.</span></span> <span data-ttu-id="9624d-181">위의 예를 클릭 하는 것이 더 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-181">This is not preferable to the one-click example above.</span></span> <span data-ttu-id="9624d-182">받는 사람이 메일을 보내도록 해야 하는 경우에는 해당 사용자가 링크를 클릭할 때 모든 필수 필드가 미리 채워져 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-182">If you do choose to require recipients to send a mail, ensure that when they click the link, all the required fields are pre-populated.</span></span>
  
### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a><span data-ttu-id="9624d-183">마케팅 전자 메일 또는 뉴스레터 등록에 이중 옵트인 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-183">Use the double opt-in option for marketing email or newsletter registration</span></span>

<span data-ttu-id="9624d-184">회사에서 제품 또는 서비스에 액세스 하기 위해 사용자의 연락처 정보를 등록 해야 하는 경우에는이 업계 모범 사례를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-184">This industry best practice is recommended if your company requires or encourages users to register their contact information in order to access your product or services.</span></span> <span data-ttu-id="9624d-185">일부 회사에서는 등록 프로세스 중에 마케팅 전자 메일 또는 전자 뉴스레터의 사용자를 자동으로 등록 하는 것이 좋지만,이는 전자 메일 필터링 분야에서 문제가 의심 스러운 마케팅 관행으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-185">Some companies make it a practice to automatically sign up their users for marketing emails or e-newsletters during the registration process, but this is considered a questionable marketing practice in the world of email filtering.</span></span>
  
<span data-ttu-id="9624d-186">등록 프로세스 중에 "예, 뉴스레터를 보내 주세요." 또는 "예, 특별 혜택을 보내 주시기 바랍니다." 확인란을 기본적으로 선택 되어 있는 경우, 근접 주의를 기울여야 하는 사용자는 실수로 마케팅 전자 메일 또는 뉴스레터에 등록할 수 있습니다. 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-186">During the registration process, if the "Yes, please send me your newsletter" or "Yes, please send me special offers" checkbox is selected by default, users who do not pay close attention may unintentionally sign up for marketing email or newsletters that they do not want to receive.</span></span>
  
 <span data-ttu-id="9624d-187">기본적으로 마케팅 전자 메일 또는 뉴스레터에 대 한 확인란을 선택 취소 하는 대신 이중 옵트인 옵션을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-187">We recommend the double opt-in option instead, which means that the checkbox for marketing emails or newsletters is unchecked by default.</span></span> <span data-ttu-id="9624d-188">또한 등록 양식이 전송 되 면 확인 전자 메일이 사용자에 게 마케팅 전자 메일 수신 결정을 확인할 수 있는 URL을 사용 하 여 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-188">Additionally, once the registration form has been submitted, a verification email is sent to the user with a URL that allows them to confirm their decision to receive marketing emails.</span></span> 
  
 <span data-ttu-id="9624d-189">이를 통해 마케팅 전자 메일을 받으려는 사용자만 전자 메일에 등록 되어 있으며, 이후에는 의심 스러운 전자 메일 마케팅 방법의 보호 회사를 지울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-189">This helps ensure that only those users who want to receive marketing email are signed up for the emails, subsequently clearing the sending company of any questionable email marketing practices.</span></span> 
  
### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a><span data-ttu-id="9624d-190">전자 메일 메시지 콘텐츠가 투명 하 고 추적 가능한 지 확인</span><span class="sxs-lookup"><span data-stu-id="9624d-190">Ensure that email message content is transparent and traceable</span></span>

<span data-ttu-id="9624d-191">전자 메일이 전송 되는 방식은 여기에 포함 된 콘텐츠에 따라 중요 한 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-191">Just as important as the way the emails are sent is the content they contain.</span></span> <span data-ttu-id="9624d-192">전자 메일 콘텐츠를 만들 때 다음과 같은 모범 사례를 사용 하 여 전자 메일 필터링 서비스에 의해 플래그가 지정 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-192">When creating email content, use the following best practices to ensure that your emails will not be flagged by email filtering services:</span></span>
  
- <span data-ttu-id="9624d-193">전자 메일 메시지가 받는 사람이 보낸 사람을 주소록에 추가 하도록 요청 하면 해당 작업을 수행 해도 배달이 보장 되지 않는다는 것을 명확 하 게 명시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-193">When the email message requests that recipients add the sender to the address book, it should clearly state that such action is not a guarantee of delivery.</span></span>
    
- <span data-ttu-id="9624d-194">메시지 본문에 포함 되는 리디렉션은 유사 하 고 일관적 이어야 하며, 여러 가지 및 다양화와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-194">Redirects included in the body of the message should be similar and consistent, and not multiple and varied.</span></span> <span data-ttu-id="9624d-195">이 컨텍스트의 리디렉션은 링크 및 문서와 같이 메시지를 벗어나는 모든 것을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-195">A redirect in this context is anything that points away from the message, such as links and documents.</span></span> <span data-ttu-id="9624d-196">알림 또는 구독 취소 링크가 많거나 프로필 링크를 업데이트 하는 경우 모두 같은 도메인을 가리켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-196">If you have a lot of advertising or Unsubscribe links or Update the Profile links, they should all point to the same domain.</span></span> <span data-ttu-id="9624d-197">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-197">For example:</span></span>
    
    <span data-ttu-id="9624d-198">맞는</span><span class="sxs-lookup"><span data-stu-id="9624d-198">Correct</span></span>
    
     `unsubscribe.bulkmailer.com`
    
     `profile.bulkmailer.com`
    
     `options.bulkmailer.com`
    
    <span data-ttu-id="9624d-199">틀린</span><span class="sxs-lookup"><span data-stu-id="9624d-199">Incorrect</span></span>
    
     `unsubscribe.bulkmailer.com`
    
     `profiles.excite.com`
    
     `options.yahoo.com`
    
- <span data-ttu-id="9624d-200">이미지 및 첨부 파일이 큰 콘텐츠 또는 이미지로만 구성 된 메시지를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-200">Avoid content with large images and attachments, or messages that are solely composed of an image.</span></span>
    
- <span data-ttu-id="9624d-201">공개 개인 정보 또는 P3P 설정에 따라 픽셀 추적 (웹 버그 또는 탐지 장치)이 있음을 명확 하 게 명시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-201">Your public privacy or P3P settings should clearly state the presence of tracking pixels (web bugs or beacons).</span></span>
    
### <a name="remove-incorrect-email-aliases-from-your-databases"></a><span data-ttu-id="9624d-202">데이터베이스에서 잘못 된 전자 메일 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="9624d-202">Remove incorrect email aliases from your databases</span></span>

<span data-ttu-id="9624d-203">데이터베이스에서 바운스를 만드는 모든 전자 메일 별칭은 불필요 하며 전자 메일 필터링 서비스를 통해 아웃 바운드 전자 메일을 통해 더 조사 하기 위해 위험에 들어갑니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-203">Any email alias in your database that creates a bounce-back is unnecessary and puts your outbound emails at risk for further scrutiny by email filtering services.</span></span> <span data-ttu-id="9624d-204">전자 메일 데이터베이스가 최신 상태 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9624d-204">Ensure that your email database is up-to-date.</span></span>
  

