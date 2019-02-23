---
title: Office 365에 대한 보안 모범 사례
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: 권장 되는 모범 사례를 수행 하 여 데이터 위반 이나 손상 된 계정을 최소화 합니다.
ms.openlocfilehash: d40fa5e4534bef1bb8389989022c44967a162aee
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212818"
---
# <a name="security-best-practices-for-office-365"></a><span data-ttu-id="34fa0-103">Office 365에 대한 보안 모범 사례</span><span class="sxs-lookup"><span data-stu-id="34fa0-103">Security best practices for Office 365</span></span>

<span data-ttu-id="34fa0-104">권장 되는 모범 사례를 수행 하 여 데이터 위반 이나 손상 된 계정을 최소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-104">Minimize the potential of a data breach or a compromised account by following these recommended best practices.</span></span>
  
<span data-ttu-id="34fa0-p101">이 문서에는 모범 사례에 대 한 간략 한 목록이 포함 되어 있습니다. 보안 설정에 대 한 자세한 분석 및 정보는 [Office 365 보안 로드맵: 처음 30 일, 90 일 및 그 이상에 대 한 최고 우선 순위](security-roadmap.md)를 참조 하세요. 이 문서에서는 cybersecurity 전문가가 위험을 평가 하 고 가장 중요 한 보안, 규정 준수 및 정보를 구현 하는 방법에 대 한 교육를 제공 하는 실제 세계 공격 조사를 기반으로 하는 정보를 찾을 수 있습니다. Office 365 테 넌 트를 보호 하기 위한 보호 제어 위협의 우선 순위를 지정 하 고 위협을 기술적 전략으로 번역 한 다음, 특징과 컨트롤을 구현 하는 체계적인 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-p101">This article contains a quick list of best practices. For more in-depth analysis and information on setting up security, see [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](security-roadmap.md). In that article, you'll find information based on investigations of real-world attacks, where our top Microsoft Office 365 cybersecurity experts provide coaching on how to assess risk and implement the most critical security, compliance, and information protection controls to protect your Office 365 tenant. You'll learn how to prioritize threats, translate threats into technical strategy, and then take a systematic approach to implementing features and controls.</span></span>
  
## <a name="use-office-365-secure-score"></a><span data-ttu-id="34fa0-109">Office 365 보안 점수 사용</span><span class="sxs-lookup"><span data-stu-id="34fa0-109">Use Office 365 Secure Score</span></span>

<span data-ttu-id="34fa0-p102">보안 점수는 위험을 더 완화 하기 위해 수행할 수 있는 작업을 권장 하는 보안 분석 도구입니다. 보안 점수가 Office 365 설정 및 활동을 살펴보고 Microsoft에서 설정한 기준과 비교 합니다. 최선의 보안 관례에 따라 정렬 된 방식을 기준으로 점수를 얻게 됩니다. 보안 점수를 얻고이를 사용 하 여 office 365 조 직의 보안을 강화 하는 방법에 대 한 자세한 내용은 [office 365 보안 점수 소개](office-365-secure-score.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="34fa0-p102">Secure Score is a security analytics tool that recommends what you can do to further reduce risk. Secure Score looks at your Office 365 settings and activities and compares them to a baseline established by Microsoft. You'll get a score based on how aligned you are with best security practices. For more information about how to get Secure Score and use it to increase the security of your Office 365 organization, see [Introducing the Office 365 Secure Score](office-365-secure-score.md).</span></span>
  
<span data-ttu-id="34fa0-114">보안 점수를 보 시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="34fa0-114">Want to try out Secure Score?</span></span>
  
<span data-ttu-id="34fa0-115">office 365- [office 365 관리자 역할 역할에](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) 할당 된 회사 또는 학교 계정을 사용 하 여 [office 365에 로그인](https://www.office.com/signin)합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-115">Using a work or school account that has been assigned the Office 365 [About Office 365 admin roles](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) role, [sign in to Office 365](https://www.office.com/signin).</span></span>
  
<span data-ttu-id="34fa0-116">보안 점수에 [https://SecureScore.office.com](https://SecureScore.office.com)액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-116">Access Secure Score at [https://SecureScore.office.com](https://SecureScore.office.com).</span></span>
  
## <a name="use-multi-factor-authentication-mfa"></a><span data-ttu-id="34fa0-117">MFA (multi-factor authentication) 사용</span><span class="sxs-lookup"><span data-stu-id="34fa0-117">Use multi-factor authentication (MFA)</span></span>

<span data-ttu-id="34fa0-p103">MFA는 사용자가 자신의 암호를 올바르게 입력 한 후 전화 통화, 문자 메시지 또는 스마트 전화에서 앱 알림을 승인 하도록 요구 하 여 강력한 암호 전략에 추가 보호 계층을 추가 합니다. 현재 위치에서 MFA를 사용 하는 경우 Office 365 사용자 계정은 사용자의 암호가 노출 되더라도 무단으로 액세스 하지 못하도록 보호 됩니다. 추가 챌린지를 만족할 때까지 계정에 대 한 액세스가 허용 되지 않으므로 계정이 보호 됩니다. 손상 되었거나 도난당 한 암호가 충분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-p103">MFA adds an additional layer of protection to a strong password strategy by requiring users to acknowledge a phone call, text message, or an app notification on their smart phone after correctly entering their password. With MFA in place, Office 365 user accounts are still protected against unauthorized access even if a user's password is compromised. Accounts are protected because access is not granted to an account until after the additional challenge has been satisfied. A compromised or stolen password is not enough.</span></span>
  
- [<span data-ttu-id="34fa0-122">Office 365 배포의 다단계 인증 계획</span><span class="sxs-lookup"><span data-stu-id="34fa0-122">Plan for multi-factor authentication for Office 365 Deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- <span data-ttu-id="34fa0-123">[Office 365에 대한 다단계 인증 설정](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)하려면</span><span class="sxs-lookup"><span data-stu-id="34fa0-123">[Set up multi-factor authentication for Office 365 users](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span></span>
    
## <a name="use-office-365-cloud-app-security"></a><span data-ttu-id="34fa0-124">Office 365 Cloud App Security 사용</span><span class="sxs-lookup"><span data-stu-id="34fa0-124">Use Office 365 Cloud App Security</span></span>

<span data-ttu-id="34fa0-p104">비즈니스 요구 사항에 따라 정책을 설정 하 여 비정상적인 활동을 추적 하 고 작업을 수행 합니다. 관리자가 많은 양의 데이터를 다운로드 하거나, 로그인을 여러 번 수행 하거나, 알 수 없는 또는 위험한 IP 주소에서 로그인 하는 등의 비정상적 이거나 위험한 사용자 활동을 검토 하도록 Office 365 Cloud App Security를 사용 하 여 알림을 설정 합니다. office 365 Enterprise E5 요금제를 사용 하는 조직의 경우 즉시 Office 365 Cloud App Security를 사용 하 여 시작할 수 있습니다. 다른 enterprise 요금제를 사용 하는 경우 Office 365 Cloud App Security를 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-p104">Set up policies based on your business needs to track anomalous activity and act on it. Set up alerts with Office 365 Cloud App Security so that admins can review unusual or risky user activity, such as downloading large amounts of data, multiple failed sign-in attempts, or sign-ins from an unknown or dangerous IP address. For organizations with an Office 365 Enterprise E5 plan, you can start using Office 365 Cloud App Security right away. If you have a different enterprise plan, you can purchase Office 365 Cloud App Security as an add-on.</span></span>
  
- [<span data-ttu-id="34fa0-129">O365 Cloud App Security 개요</span><span class="sxs-lookup"><span data-stu-id="34fa0-129">Overview of O365 Cloud App Security</span></span>](office-365-cas-overview.md)
    
- [<span data-ttu-id="34fa0-130">Office 365 Cloud App Security 켜기</span><span class="sxs-lookup"><span data-stu-id="34fa0-130">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a><span data-ttu-id="34fa0-131">보안 메일 흐름</span><span class="sxs-lookup"><span data-stu-id="34fa0-131">Secure mail flow</span></span>

<span data-ttu-id="34fa0-132">Exchange Online Protection에서 다양 한 기능 집합을 구현 하 고 각 전자 메일 메시지의 보낸 사람 id에 대 한 보다 강력한 보증을 얻고 전자 메일을 통해 전송 되는 알려지지 않은 맬웨어, 바이러스 및 악의적인 url을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-132">Implement the rich feature set in Exchange Online Protection and gain greater assurance about the identity of the sender of each email message, and protect against unknown malware, viruses, and malicious URLs transmitted through emails.</span></span>
  
- <span data-ttu-id="34fa0-133">조직에 대 한 [Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md) 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-133">Configure [Office 365 Email Anti-Spam Protection](anti-spam-protection.md) policies for your organization.</span></span> 
    
- <span data-ttu-id="34fa0-134">[안전한 첨부 파일 및 안전한 링크에](https://technet.microsoft.com/library/mt148491.aspx)대 한 자세한 내용을 알아보고 Advanced threat protection을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-134">Learn about and then use [Advanced threat protection for safe attachments and safe links](https://technet.microsoft.com/library/mt148491.aspx).</span></span>
    
- <span data-ttu-id="34fa0-135">[조직에 맬웨어 방지 보호 기능을 추가](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-135">[Add anti-malware protection to your organization](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).</span></span>
    
- <span data-ttu-id="34fa0-136">사용자를 위해 [Office 365의 전자 메일 메시지에 대 한 보안 팁](safety-tips-in-office-365.md) 을 알아보고 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-136">Learn about and enable [Safety tips in email messages in Office 365](safety-tips-in-office-365.md) for your users.</span></span> 
    
- <span data-ttu-id="34fa0-137">Office 365에서 조직에 대 한 사용자 지정 도메인을 사용 하는 경우에는 SPF, dkim을 설정한 다음 DMARC이 조직에서 보낸 메일의 유효성을 검사 하 고 스푸핑을 방지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-137">If you're using a custom domain for your organization in Office 365, set up SPF, DKIM, and then DMARC to validate mail sent by your organization and to help prevent spoofing:</span></span>
    
  - <span data-ttu-id="34fa0-138">[스푸핑 방지를 위해 Office 365에서 SPF를 설정](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-138">[Set up SPF in Office 365 to help prevent spoofing](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span></span>
    
  - <span data-ttu-id="34fa0-139">[dkim을 사용 하 여 Office 365의 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-139">[Use DKIM to validate outbound email sent from your custom domain in Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span></span>
    
  - <span data-ttu-id="34fa0-140">[DMARC을 사용 하 여 Office 365의 전자 메일 유효성을 검사](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-140">[Use DMARC to validate email in Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span></span>
    
## <a name="enable-mailbox-audit-logging"></a><span data-ttu-id="34fa0-141">사서함 감사 로깅 사용</span><span class="sxs-lookup"><span data-stu-id="34fa0-141">Enable mailbox audit logging</span></span>

<span data-ttu-id="34fa0-p105">일부 감사 로깅은 Office 365에서 자동으로 사용 하도록 설정 됩니다. 그러나 사서함 감사 로깅은 기본적으로 설정 되지 않습니다. Exchange Online PowerShell을 사용 하 여 Office 365에서 모든 사용자 사서함에 대 한 감사 로깅을 설정 합니다. 자세한 내용은 [Office 365에서 사서함 감사 사용](https://go.microsoft.com/fwlink/p/?LinkID=626109)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="34fa0-p105">Some audit logging is automatically enabled for you in Office 365; however, mailbox audit logging is not turned on by default. You turn on audit logging for all user mailboxes in Office 365 by using Exchange Online PowerShell. For information, see [Enable mailbox auditing in Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).</span></span>
  
<span data-ttu-id="34fa0-p106">감사 로깅을 사용 하도록 설정한 후 [Office 365 보안 &amp; 및 준수 센터에서 감사 로그를 검색](search-the-audit-log-in-security-and-compliance.md) 하 여 사용자 사서함에 로그인 한 사람, 보낸 메시지 및 사서함 소유자가 수행한 기타 작업을 확인할 수 있습니다. 관리자에 게 문의 하십시오. 기본적으로 Office 365 감사 로그에 포함 된 사서함 활동 목록은 [Exchange 사서함 활동](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="34fa0-p106">After you've enabled audit logging you can [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md) to find out who has logged into your user mailboxes, sent messages, and other activities performed by the mailbox owner, a delegated user, or an administrator. For a list of mailbox activities that are included in the Office 365 audit log by default, see [Exchange mailbox activities](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).</span></span>
  
<span data-ttu-id="34fa0-147">감사 로그를 사용 하 여 수행할 수 있는 기타 작업에 대 한 자세한 내용은 [Exchange 2016에서 사서함 감사 로깅](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="34fa0-147">For information about other actions you can perform with the audit log, such as changing the amount of time to save entries in the audit log, see [Mailbox audit logging in Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).</span></span>
  
## <a name="configure-data-loss-prevention-dlp"></a><span data-ttu-id="34fa0-148">DLP (데이터 손실 방지) 구성</span><span class="sxs-lookup"><span data-stu-id="34fa0-148">Configure Data Loss Prevention (DLP)</span></span>

<span data-ttu-id="34fa0-p107">DLP를 사용 하면 중요 한 데이터를 식별 하 고 사용자가 실수로 또는 의도적으로 데이터를 공유 하지 못하게 하는 정책을 만들 수 있습니다. DLP는 Exchange online, SharePoint Online 및 OneDrive를 포함 하는 Office 365에서 작동 하 여 사용자가 워크플로를 중단 하지 않고 준수 상태를 유지할 수 있도록 합니다. 자세한 내용은 [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="34fa0-p107">DLP allows you to identify sensitive data and create policies that help prevent your users from accidentally or intentionally sharing the data. DLP works across Office 365 including Exchange Online, SharePoint Online, and OneDrive so that your users can stay compliant without interrupting their workflow. For more information, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
## <a name="use-customer-lockbox"></a><span data-ttu-id="34fa0-152">고객 Lockbox 사용</span><span class="sxs-lookup"><span data-stu-id="34fa0-152">Use Customer Lockbox</span></span>

<span data-ttu-id="34fa0-p108">Office 365 관리자는 고객 Lockbox를 사용 하 여 Microsoft 기술 지원 엔지니어가 도움말 세션 중에 데이터에 액세스 하는 방법을 제어할 수 있습니다. 엔지니어가 문제를 해결 하기 위해 데이터에 액세스 해야 하는 경우에는 고객 Lockbox를 사용 하 여 액세스 요청을 승인 하거나 거부할 수 있습니다. 이를 승인 하면 엔지니어가 데이터에 액세스할 수 있습니다. 각 요청에는 만료 시간이 있으며 문제가 해결 되 면 요청이 닫히고 액세스가 해지 됩니다. 고객 Lockbox가 office 365 enterprise E5 계획에 포함 되어 있거나 다른 Office 365 Enterprise 요금제를 사용 하 여 별도의 구독을 구입할 수도 있습니다. 자세한 내용은 [Office 365 고객 Lockbox 요청](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="34fa0-p108">As an Office 365 admin, you can use Customer Lockbox to control how a Microsoft support engineer accesses your data during a help session. In cases where the engineer requires access to your data to troubleshoot and fix an issue, Customer Lockbox allows you to approve or reject the access request. If you approve it, the engineer can access the data. Each request has an expiration time, and once the issue is resolved, the request is closed and access is revoked. Customer Lockbox is included in the Office 365 Enterprise E5 plan, or you can purchase a separate subscription with any other Office 365 enterprise plan. For information, see [Office 365 Customer Lockbox Requests](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).</span></span>
  
## <a name="try-it-yourself"></a><span data-ttu-id="34fa0-159">직접 사용해 보기</span><span class="sxs-lookup"><span data-stu-id="34fa0-159">Try it yourself</span></span>
<span data-ttu-id="34fa0-160"><a name="SecureScore"> </a></span><span class="sxs-lookup"><span data-stu-id="34fa0-160"></span></span>

<span data-ttu-id="34fa0-161">프로덕션 환경에 Office 365 평가판 구독을 채택 하기 전에 이러한 보안 기능을 통해 작동 하는 방법을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="34fa0-161">See these security features working in an Office 365 trial subscription prior to adopting them in production.</span></span>
  
- [<span data-ttu-id="34fa0-162">Office 365 평가판 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="34fa0-162">Create an Office 365 trial subscription</span></span>](https://technet.microsoft.com/library/mt736406.aspx)
    
- [<span data-ttu-id="34fa0-163">사용자 계정에 대 한 MFA 구성 및 테스트</span><span class="sxs-lookup"><span data-stu-id="34fa0-163">Configure and test MFA for a user account</span></span>](https://technet.microsoft.com/library/mt492459.aspx)
    
- [<span data-ttu-id="34fa0-164">전역 관리자 활동을 알리기 위해 Office 365 Cloud App Security를 구성 하 고 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-164">Configure and test Office 365 Cloud App Security to notify you of global admin activity</span></span>](https://technet.microsoft.com/library/mt757250.aspx)
    
- [<span data-ttu-id="34fa0-165">의심 스러운 전자 메일에 대 한 ATP 구성 및 테스트</span><span class="sxs-lookup"><span data-stu-id="34fa0-165">Configure and test ATP for suspicious email</span></span>](https://technet.microsoft.com/library/mt490479.aspx)
    
- <span data-ttu-id="34fa0-166">위의 각 단계에 대 한 [Office 365 보안 점수](https://securescore.office.com/) 에서 평가판 구독을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fa0-166">Check the [Office 365 Secure Score](https://securescore.office.com/) for your trial subscription for each of the above steps</span></span> 
    

