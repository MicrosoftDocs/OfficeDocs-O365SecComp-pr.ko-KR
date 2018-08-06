---
title: Office 365로 전송 메일 문제해결
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/2/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
description: 이 문서에서는 Office 365 및 Office 365 고객에 게 대량 메일로 대 한 모범 사례에 받은 편지함에 전자 메일을 보내려고 할 때 문제를 발생 하는 발신자에 대 한 문제해결 정보를 제공 합니다.
ms.openlocfilehash: 29c30787f493c69eb7d42b8025b25c86acddfff9
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026415"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a><span data-ttu-id="11bc8-103">Office 365로 전송 메일 문제해결</span><span class="sxs-lookup"><span data-stu-id="11bc8-103">Troubleshooting mail sent to Office 365</span></span>

<span data-ttu-id="11bc8-104">이 문서에서는 Office 365 및 Office 365 고객에 게 대량 메일로 대 한 모범 사례에 받은 편지함에 전자 메일을 보내려고 할 때 문제를 발생 하는 발신자에 대 한 문제해결 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-104">This article provides troubleshooting information for senders who are experiencing issues when trying to send email to inboxes in Office 365 and best practices for bulk mailing to Office 365 customers.</span></span>
  
## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a><span data-ttu-id="11bc8-105">Office 365에 대 한 메일 배달의 일반적인 문제를 해결</span><span class="sxs-lookup"><span data-stu-id="11bc8-105">Troubleshooting common problems with mail delivery to Office 365</span></span>

<span data-ttu-id="11bc8-106">이러한 일반적으로 발생 한 문제 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-106">Choose from one of these commonly encountered issues.</span></span>
  
- [<span data-ttu-id="11bc8-107">신뢰도 보내는 IP 및 도메인의 관리 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="11bc8-107">Are you managing your IP and domain's sending reputation?</span></span>](troubleshooting-mail-sent-to-office-365.md#ManageRep)
    
- [<span data-ttu-id="11bc8-108">새 IP 주소에서 보내는 메일 적용 되어 있습니까?</span><span class="sxs-lookup"><span data-stu-id="11bc8-108">Are you sending email from new IP addresses?</span></span>](troubleshooting-mail-sent-to-office-365.md#NewIPs)
    
- [<span data-ttu-id="11bc8-109">DNS가 올바르게 설정 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-109">Confirm that your DNS is set up correctly</span></span>](troubleshooting-mail-sent-to-office-365.md#ConfirmDNSsetup)
    
- [<span data-ttu-id="11bc8-110">하면 보급 안함 사용자가 직접 라우팅할 수 없는 IP로 확인</span><span class="sxs-lookup"><span data-stu-id="11bc8-110">Ensure that you do not advertise yourself as a non-routable IP</span></span>](troubleshooting-mail-sent-to-office-365.md#NoReverseDNS)
    
- [<span data-ttu-id="11bc8-111">받은 배달 못함 보고서 (NDR) 전자 메일을 보낼 때 Office 365에서 사용자에 게</span><span class="sxs-lookup"><span data-stu-id="11bc8-111">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>](troubleshooting-mail-sent-to-office-365.md#NDRInbound)
    
- [<span data-ttu-id="11bc8-112">EOP에서 받는 사람의 정크 메일 폴더에 착륙 내 전자 메일</span><span class="sxs-lookup"><span data-stu-id="11bc8-112">My email landed in the recipient's junk folder in EOP</span></span>](troubleshooting-mail-sent-to-office-365.md#JunkMailBox)
    
- [<span data-ttu-id="11bc8-113">내 IP 주소에서 보낸 트래픽에 EOP에 의해 제한</span><span class="sxs-lookup"><span data-stu-id="11bc8-113">Traffic from my IP address is throttled by EOP</span></span>](troubleshooting-mail-sent-to-office-365.md#AllowEOPIPs)
    
### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a><span data-ttu-id="11bc8-114">신뢰도 보내는 IP 및 도메인의 관리 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="11bc8-114">Are you managing your IP and domain's sending reputation?</span></span>
<span data-ttu-id="11bc8-115"><a name="ManageRep"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-115"></span></span>

<span data-ttu-id="11bc8-p101">EOP 필터링 기술은 Microsoft Office 365 Exchange 서버, Microsoft Office Outlook 및 Windows Live 메일 같은 다른 Microsoft 제품에 대 한 스팸 방지 보호 기능을 제공 하도록 디자인 되었습니다. 활용 SPF, DKIM, 및 DMARC;는 주소는 데 도움이 되는 인증 기술 스푸핑 및 피싱 문제 그렇게 전자 메일을 보내는 도메인에 있는 권한이 있는지 확인 하 여 전자 메일. 다양 한 요인 보내는 IP, 도메인, 인증, 목록 정확성, 불만 속도, 콘텐츠 및 자세한 관련 하 여 EOP 필터링 하는 영향을 받습니다. 이러한, 주체의 하나 영향을 미치는 보낸 사람의 신뢰도 운전 하 고 전자 메일을 제공 하는 능력은 자신의 정크 메일 불만 속도입니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p101">EOP filtering technologies are designed to provide anti-spam protections for Microsoft Office 365 as well as other Microsoft products like Exchange Server, Microsoft Office Outlook, and Windows Live Mail. We also leverage SPF, DKIM, and DMARC; email authentication technologies that help address the problem of spoofing and phishing by verifying that the domain sending the email is authorized to do so. EOP filtering is influenced by a number of factors related to the sending IP, domain, authentication, list accuracy, complaint rates, content and more. Of these, one of the principal factors in driving down a sender's reputation and their ability to deliver email is their junk email complaint rate.</span></span> 
  
### <a name="are-you-sending-email-from-new-ip-addresses"></a><span data-ttu-id="11bc8-120">새 IP 주소에서 보내는 메일 적용 되어 있습니까?</span><span class="sxs-lookup"><span data-stu-id="11bc8-120">Are you sending email from new IP addresses?</span></span>
<span data-ttu-id="11bc8-121"><a name="NewIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-121"></span></span>

<span data-ttu-id="11bc8-p102">적이 없는 전자 메일을 보낼 일반적으로 사용 하는 IP 주소는 시스템에서 구축 된 신뢰도 필요는 없습니다. 결과적으로, 새 Ip에서 보내는 전자 메일은 배달 문제가 발생할 가능성이 높습니다. IP가 스팸을 보내지 않으려면에 대 한 신뢰도 작성 되 면 EOP 더 나은 전자 메일 배달 경험에 대 한 일반적으로 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p102">IP addresses not previously used to send email typically don't have any reputation built up in our systems. As a result, emails from new IPs are more likely to experience delivery issues. Once the IP has built a reputation for not sending spam, EOP will typically allow for a better email delivery experience.</span></span>
  
<span data-ttu-id="11bc8-p103">일반적으로 기존 SPF 레코드에서 인증 하는 도메인에 대 한 추가 되는 새 Ip 상속 하는 도메인의 보내는 신뢰도 중 일부의 이점도 경험이 있어야 합니다. 도메인에 좋은 경우 신뢰도 보내는 새 Ip 발생할 수는 더 빠른 시간 향상. 새 IP 수 완벽 하 게 단계적 몇 주 또는 볼륨, 목록 정확성 및 정크 메일 불만 비율에 따라 빨리 내에서 예상할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p103">New IPs that are added for domains that are authenticated under existing SPF records typically experience the added benefit of inheriting some of the domain's sending reputation. If your domain has a good sending reputation new IPs may experience a faster ramp up time. A new IP can expect to be fully ramped within a couple of weeks or sooner depending on volume, list accuracy, and junk email complaint rates.</span></span>
  
### <a name="confirm-that-your-dns-is-set-up-correctly"></a><span data-ttu-id="11bc8-128">DNS가 올바르게 설정 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-128">Confirm that your DNS is set up correctly</span></span>
<span data-ttu-id="11bc8-129"><a name="ConfirmDNSsetup"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-129"></span></span>

<span data-ttu-id="11bc8-130">만들고 메일 라우팅에 필요한 MX 레코드를 포함 하는 DNS 레코드를 유지 관리 하는 방법에 대 한 지침은 DNS 호스팅 공급자에 게 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-130">For instructions about how to create and maintain DNS records, including the MX record required for mail routing, you will need to contact your DNS hosting provider.</span></span>
  
### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a><span data-ttu-id="11bc8-131">하면 보급 안함 사용자가 직접 라우팅할 수 없는 IP로 확인</span><span class="sxs-lookup"><span data-stu-id="11bc8-131">Ensure that you do not advertise yourself as a non-routable IP</span></span>
<span data-ttu-id="11bc8-132"><a name="NoReverseDNS"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-132"></span></span>

<span data-ttu-id="11bc8-p104">역방향 DNS 조회 실패 사람이 보낸 전자 메일을 허용 하지 않습니다 했습니다. 일부 경우에 적법 한 보낸 사람이 광고 하지 자신 올바르게 인터넷 간 라우팅 가능한 IP로 EOP에 대 한 연결을 열려고 시도할 때 합니다. 개인 (라우팅할 수 없는) 네트워킹에 대 한 예약 된 IP 주소에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p104">We may not accept email from senders who fail a reverse-DNS lookup. In some cases, legitimate senders advertise themselves incorrectly as a non-internet routable IP when attempting to open a connection to EOP. IP addresses that are reserved for private (non-routable) networking include:</span></span>
  
- <span data-ttu-id="11bc8-136">192.168.0.0/16 (또는 192.168.0.0-192.168.255.255)</span><span class="sxs-lookup"><span data-stu-id="11bc8-136">192.168.0.0/16 (or 192.168.0.0 - 192.168.255.255)</span></span>
    
- <span data-ttu-id="11bc8-137">10.0.0.0/8 (또는 10.0.0.0-10.255.255.255)</span><span class="sxs-lookup"><span data-stu-id="11bc8-137">10.0.0.0/8 (or 10.0.0.0 - 10.255.255.255)</span></span>
    
- <span data-ttu-id="11bc8-138">172.16.0.0/11 (또는 172.16.0.0-172.31.255.255)</span><span class="sxs-lookup"><span data-stu-id="11bc8-138">172.16.0.0/11 (or 172.16.0.0 - 172.31.255.255)</span></span>
    
### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a><span data-ttu-id="11bc8-139">받은 배달 못함 보고서 (NDR) 전자 메일을 보낼 때 Office 365에서 사용자에 게</span><span class="sxs-lookup"><span data-stu-id="11bc8-139">You received a non-delivery report (NDR) when sending email to a user in Office 365</span></span>
<span data-ttu-id="11bc8-140"><a name="NDRInbound"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-140"></span></span>

<span data-ttu-id="11bc8-p105">일부 배달 문제는 보낸 사람의 IP 주소가 Microsoft에 의해 차단 되 고 발생 했거나 사용자 계정은 이전 스팸 활동으로 인해 차단된 sender로 식별 됩니다. 오류는 NDR 받았는지 생각 되는 경우 먼저 문제를 해결 하려면 NDR 메시지의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p105">Some delivery issues are the result of the sender's IP address being blocked by Microsoft or because the user account is identified as banned sender due to previous spam activity. If you believe that you have received the NDR in error, first follow any instructions in the NDR message to resolve the issue.</span></span> 
  
<span data-ttu-id="11bc8-143">받은 오류에 대 한 자세한 내용은 [온-프레미스 Exchange 2013 및 Office 365의 Dsn 및 Ndr에](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx)SMTP 오류 코드의 전체 목록은 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="11bc8-143">For more information about the error you received, see the complete list of SMTP error codes in [DSNs and NDRs in On-Premises Exchange 2013 and Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).</span></span>
  
 <span data-ttu-id="11bc8-144">예는 다음과 같은 NDR을 수신 하는 경우 나타냅니다 보내는 IP 주소가 Microsoft에 의해 차단 된는.</span><span class="sxs-lookup"><span data-stu-id="11bc8-144">For example, if you receive the following NDR, it indicates that the sending IP address was blocked by Microsoft.</span></span> 
  
 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`
  
<span data-ttu-id="11bc8-145">이 목록에서 제거를 요청 하려면 [Office 365 수신된 거부 목록에서 자신을 제거 하려면 delist 포털을 사용할](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-145">To request removal from this list, you can [Use the delist portal to remove yourself from the Office 365 blocked senders list](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).</span></span>
  
### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a><span data-ttu-id="11bc8-146">EOP에서 받는 사람의 정크 메일 폴더에 착륙 내 전자 메일</span><span class="sxs-lookup"><span data-stu-id="11bc8-146">My email landed in the recipient's junk folder in EOP</span></span>
<span data-ttu-id="11bc8-147"><a name="JunkMailBox"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-147"></span></span>

<span data-ttu-id="11bc8-p106">메시지를 올바르게 하지 스팸으로 식별 EOP에 의해, 받는 사람에 게 평가 하 고 메시지를 분석 Microsoft 스팸 분석 팀에 게이 false 이면 가양성 메시지 제출 작업할 수 있습니다. 분석의 결과 따라 서비스 수준 스팸 콘텐츠 필터 규칙을 통해 메시지를 허용 하도록 조정 될 수 있습니다. 전자 메일을 사용 하 여 스팸으로 분류 되지 않도록 해야 하는 Microsoft에 게 메시지를 전송할 수 있습니다. 이렇게 하는 경우에 다음 절차의 단계를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p106">If a message was incorrectly identified as spam by EOP, you can work with the recipient to submit this false positive message to the Microsoft Spam Analysis Team, who will evaluate and analyze the message. Depending on the results of the analysis, the service-wide spam content filter rules may be adjusted to allow the message through. You use email to submit messages to Microsoft that should not be classified as spam. When doing so, be sure to use the steps in the following procedure.</span></span>
  
### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a><span data-ttu-id="11bc8-152">사용 하 여 전자 메일을 Microsoft 스팸 분석 팀 가양성 메시지 전송</span><span class="sxs-lookup"><span data-stu-id="11bc8-152">To use email to submit false positive messages to the Microsoft Spam Analysis Team</span></span>

1. <span data-ttu-id="11bc8-153">스팸이 아닌으로 전송 하려는 메시지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-153">Save the message you want to submit as non-spam.</span></span>
    
2. <span data-ttu-id="11bc8-154">비어 있는 새 메시지를 작성하여 스팸이 아니라는 메시지를 첨부합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-154">Create a new, blank message and attach the non-spam message to it.</span></span>
    
    <span data-ttu-id="11bc8-155">필요한 경우에 여러 스팸이 아닌 메시지를 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-155">You can attach multiple non-spam messages if needed.</span></span>
    
3. <span data-ttu-id="11bc8-156">원본 메시지의 제목 줄을 복사하여 새 메시지의 제목 줄에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-156">Copy and paste the original message subject line into the new message subject line.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="11bc8-157">새 메시지의 본문은 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-157">Leave the body of the new message empty.</span></span> 
  
4. <span data-ttu-id="11bc8-158">새 메시지를 [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com)으로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-158">Send your new message to [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).</span></span>
    
### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a><span data-ttu-id="11bc8-159">내 IP 주소에서 보낸 트래픽에 EOP에 의해 제한</span><span class="sxs-lookup"><span data-stu-id="11bc8-159">Traffic from my IP address is throttled by EOP</span></span>
<span data-ttu-id="11bc8-160"><a name="AllowEOPIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-160"></span></span>

<span data-ttu-id="11bc8-161">하 고 있음을 나타내는 EOP에서 NDR을 수신 하는 경우 사용자의 IP 주소는 되 고 제한 EOP에 의해 예:</span><span class="sxs-lookup"><span data-stu-id="11bc8-161">If you receive an NDR from EOP that indicates that your IP address is being throttled by EOP, for example:</span></span>
  
 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`
  
<span data-ttu-id="11bc8-p107">IP 주소에서 의심 스러운 작업에서 발견 하 고 확인 되는 추가 하는 동안에 일시적으로 제한 된가 때문에 NDR을 수신 합니다. 평가 통해의 생각을 선택 취소 하면이 제한 사항은 잠시 후에 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p107">You received the NDR because suspicious activity has been detected from the IP address and it has been temporarily restricted while it is being further evaluated. If the suspicion is cleared through evaluation, this restriction will be lifted shortly.</span></span>
  
### <a name="i-cant-receive-email-from-senders-in-office-365"></a><span data-ttu-id="11bc8-164">Office 365에 있는 사람이 보낸 전자 메일을 받을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-164">I can't receive email from senders in Office 365</span></span>
<span data-ttu-id="11bc8-165"><a name="AllowEOPIPs"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-165"></span></span>

 <span data-ttu-id="11bc8-p108">사용자에 게에서 메시지를 수신 하기 위해 네트워크 EOP 데이터 센터에서 사용 하는 IP 주소에서 연결을 허용 하는지 확인 합니다. 자세한 내용은 [Exchange Online Protection IP 주소](eop/exchange-online-protection-ip-addresses.md)를 참조 하십시오. 모든 IP의 레코드에 대 한 추가 된 주소 변경 또는 [EOP IP 주소에 대 한 변경 알림](eop/change-notification-for-eop-ip-addresses.md)참조 작년 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p108">In order to receive messages from our users, make sure your network allows connections from the IP addresses that EOP uses in our datacenters. For more information, see [Exchange Online Protection IP addresses](eop/exchange-online-protection-ip-addresses.md). For a record of all IP addresses that have been added, changed, or deprecated in the past year, see [Change notification for EOP IP addresses](eop/change-notification-for-eop-ip-addresses.md).</span></span>
  
## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a><span data-ttu-id="11bc8-169">Office 365 사용자에 게 대량 전자 메일 보내기에 대 한 모범 사례</span><span class="sxs-lookup"><span data-stu-id="11bc8-169">Best practices for bulk emailing to Office 365 users</span></span>
<span data-ttu-id="11bc8-170"><a name="BulkMailer"> </a></span><span class="sxs-lookup"><span data-stu-id="11bc8-170"></span></span>

<span data-ttu-id="11bc8-171">자주 Office 365 사용자에 게 대량 전자 메일 캠페인을 수행 하 고 안전 하 고 시기 적절 한 방식으로 사용자 전자 메일 도착 되었는지 확인 하려면, 하는 경우이 섹션의 팁을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-171">If you often conduct bulk email campaigns to Office 365 users and want to ensure that your emails arrive in a safe and timely manner, follow the tips in this section.</span></span>
  
### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a><span data-ttu-id="11bc8-172">From 확인: 메시지를 보내는 사람 이름 반영</span><span class="sxs-lookup"><span data-stu-id="11bc8-172">Ensure that the From: name reflects who is sending the message</span></span>

<span data-ttu-id="11bc8-p109">어떤 메시지의 간단한 요약의, 및 메시지 본문 명확 하 게 하 고 간결 하 게 나타내야 구축, 서비스 또는 제품 란에 대 한 제목 여야 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="11bc8-p109">The Subject should be a brief summary of what the message is about, and the message body should clearly and succinctly indicate what the offering, service, or product is about. For example:</span></span>
  
<span data-ttu-id="11bc8-175">맞는</span><span class="sxs-lookup"><span data-stu-id="11bc8-175">Correct</span></span>
  
 ` From: marketing@shoppershandbag.com `
  
 `Subject: Updated catalog for the Christmas season!`
  
<span data-ttu-id="11bc8-176">잘못 된</span><span class="sxs-lookup"><span data-stu-id="11bc8-176">Incorrect</span></span>
  
 `From: someone@outlook.com`
  
 `Subject: Catalogs`
  
<span data-ttu-id="11bc8-177">사용자는 누구에 게 쉽게 하 고 수행 중인, 덜 난이도 대부분의 스팸 필터를 통해 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-177">The easier you make it for people to know who you are and what you are doing, the less difficulty you will have delivering through most spam filters.</span></span>
  
### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a><span data-ttu-id="11bc8-178">항상 캠페인 전자 메일에서 구독 취소 옵션을 포함</span><span class="sxs-lookup"><span data-stu-id="11bc8-178">Always include an unsubscribe option in campaign emails</span></span>

<span data-ttu-id="11bc8-p110">특히 뉴스레터를 전자 메일: 마케팅 하 향후 전자 메일에서 구독을 취소 하는 방법의 항상 포함 되어야 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="11bc8-p110">Marketing emails, especially newsletters, should always include a way of unsubscribing from future emails. For example:</span></span>
  
 `This email was sent to example@contoso.com by sender@fabrikam.com.`
  
 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`
  
<span data-ttu-id="11bc8-p111">일부 보낸사람을 특정 별칭으로 "취소"와 제목에 전자 메일을 보낼 받는 사람을 요구 하 여이 옵션을 포함 합니다. 위의 한번 클릭 예제를 원합니다 아닙니다. 메일을 보낼 받는 사람을 요구 하도록 수행 하려는 경우에 사용자에 대 한 링크를 클릭 하면 모든 필수 필드는 미리 채워진 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p111">Some senders include this option by requiring recipients to send an email to a certain alias with "Unsubscribe" in the subject. This is not preferable to the one-click example above. If you do choose to require recipients to send a mail, ensure that when they click the link, all the required fields are pre-populated.</span></span>
  
### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a><span data-ttu-id="11bc8-184">이중 옵트인 옵션을 사용 하 여 마케팅 전자 메일 또는 뉴스레터 등록</span><span class="sxs-lookup"><span data-stu-id="11bc8-184">Use the double opt-in option for marketing email or newsletter registration</span></span>

<span data-ttu-id="11bc8-p112">회사 필요 하거나 제품 또는 서비스에 액세스 하기 위해 사용자 연락처 정보를 등록을 권장 하는 경우에이 업계 모범 사례는 것이 좋습니다. 일부 회사에서는 쉽게 사용자에 게 전자 메일 마케팅에 자동으로 등록 하는 방법 또는 e-뉴스레터 등록 프로세스 하지만이 하는 동안에 전자 메일 필터링의 세계에서 의심 스러운 마케팅 연습 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p112">This industry best practice is recommended if your company requires or encourages users to register their contact information in order to access your product or services. Some companies make it a practice to automatically sign up their users for marketing emails or e-newsletters during the registration process, but this is considered a questionable marketing practice in the world of email filtering.</span></span>
  
<span data-ttu-id="11bc8-187">등록 하는 동안 하는 경우는 "예, 보내 주시기 바랍니다 회보" 또는 "예, 보내 주시기 바랍니다 특수 제공" 확인란이 선택 되어 기본적으로, 사용자에 게 닫기 주의 하지 마케팅 전자 메일 또는 하지 않는 뉴스레터 등록 실수로 될 수 있습니다 수신 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-187">During the registration process, if the "Yes, please send me your newsletter" or "Yes, please send me special offers" checkbox is selected by default, users who do not pay close attention may unintentionally sign up for marketing email or newsletters that they do not want to receive.</span></span>
  
 <span data-ttu-id="11bc8-p113">것이 좋습니다 이중 옵트인 옵션을 대신 하는 마케팅 전자 메일 또는 회보의 확인란은 기본적으로 선택 하지 것을 의미 합니다. 또한 등록 양식이 제출 되 면 확인 전자 메일을 자신의 결정 마케팅 전자 메일을 받을 수를 확인 하도록 허용 하는 URL 가진 사용자에 게 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p113">We recommend the double opt-in option instead, which means that the checkbox for marketing emails or newsletters is unchecked by default. Additionally, once the registration form has been submitted, a verification email is sent to the user with a URL that allows them to confirm their decision to receive marketing emails.</span></span> 
  
 <span data-ttu-id="11bc8-190">그러면이 있는 마케팅 전자 메일을 받도록 하려는 사용자만 서명는 전자 메일에 대 한 이후에 사례 마케팅 하는 의심 스러운 전자 메일의 보내는 회사의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-190">This helps ensure that only those users who want to receive marketing email are signed up for the emails, subsequently clearing the sending company of any questionable email marketing practices.</span></span> 
  
### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a><span data-ttu-id="11bc8-191">전자 메일 메시지 콘텐츠를 투명 하 게 하 고 추적 가능한 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="11bc8-191">Ensure that email message content is transparent and traceable</span></span>

<span data-ttu-id="11bc8-p114">것도 마찬가지로 중요 전자 메일 전송 하는 방법을 포함 하는 콘텐츠를 그대로 합니다. 전자 메일 콘텐츠를 만들 때 다음과 같은 모범 사례를 사용 하 여 확인 전자 메일 서비스를 필터링 하 여 사용자 전자 메일을 플래그가 지정 수 되지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p114">Just as important as the way the emails are sent is the content they contain. When creating email content, use the following best practices to ensure that your emails will not be flagged by email filtering services:</span></span>
  
- <span data-ttu-id="11bc8-194">전자 메일 메시지는 받는 사람에 게 주소록에 보낸사람 추가를 명확 하 게 명시 해야 것을 요청 하는 경우 이러한 작업은 하지 배달이 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-194">When the email message requests that recipients add the sender to the address book, it should clearly state that such action is not a guarantee of delivery.</span></span>
    
- <span data-ttu-id="11bc8-p115">유사 하 고 일관 되 고 있지 여러 메시지의 본문에 포함 된 리디렉션하거나 수 있어야 하 고 다양 한 합니다. 이 컨텍스트에서 리디렉션 링크 및 문서와 같은 메시지 로부터 가리키는 되는 합니다. 광고 또는 구독 취소 링크의 많은 했거나 프로필 파일에 대 한 링크를 업데이트 하는 경우 모든 가리켜야 동일한 도메인에 있습니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="11bc8-p115">Redirects included in the body of the message should be similar and consistent, and not multiple and varied. A redirect in this context is anything that points away from the message, such as links and documents. If you have a lot of advertising or Unsubscribe links or Update the Profile links, they should all point to the same domain. For example:</span></span>
    
    <span data-ttu-id="11bc8-199">맞는</span><span class="sxs-lookup"><span data-stu-id="11bc8-199">Correct</span></span>
    
     `unsubscribe.bulkmailer.com`
    
     `profile.bulkmailer.com`
    
     `options.bulkmailer.com`
    
    <span data-ttu-id="11bc8-200">잘못 된</span><span class="sxs-lookup"><span data-stu-id="11bc8-200">Incorrect</span></span>
    
     `unsubscribe.bulkmailer.com`
    
     `profiles.excite.com`
    
     `options.yahoo.com`
    
- <span data-ttu-id="11bc8-201">큰 이미지 및 첨부 파일, 또는 이미지로 구성 된 메시지를 사용 하 여 콘텐츠를 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-201">Avoid content with large images and attachments, or messages that are solely composed of an image.</span></span>
    
- <span data-ttu-id="11bc8-202">공개 개인정보 또는 P3P 설정 추적 픽셀 (웹 버그 또는 탐지 장치)의 현재를 상태 명확 하 게 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-202">Your public privacy or P3P settings should clearly state the presence of tracking pixels (web bugs or beacons).</span></span>
    
### <a name="remove-incorrect-email-aliases-from-your-databases"></a><span data-ttu-id="11bc8-203">데이터베이스에서 잘못 된 전자 메일 별칭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-203">Remove incorrect email aliases from your databases</span></span>

<span data-ttu-id="11bc8-p116">튀어오르 저장에서 만들어지는 데이터베이스의 모든 전자 메일 별칭 필요 하지 않으며 사용자 아웃 바운드 전자 메일이 추가 조사를 수행 하는 위험에 전자 메일 서비스를 필터링 하 여 내리지 못할 수 있습니다. 전자 메일 데이터베이스 최신 상태 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="11bc8-p116">Any email alias in your database that creates a bounce-back is unnecessary and puts your outbound emails at risk for further scrutiny by email filtering services. Ensure that your email database is up-to-date.</span></span>
  

