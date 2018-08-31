---
title: Office 365에 대한 보안 모범 사례
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: 이러한 권장된 모범 사례를 수행 하 여 데이터 위반 또는 손상 된 계정의 가능성을 최소화 합니다.
ms.openlocfilehash: 245302af0b08a4ee8183345fc386fe47985c93dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534060"
---
# <a name="security-best-practices-for-office-365"></a><span data-ttu-id="1e7b6-103">Office 365에 대한 보안 모범 사례</span><span class="sxs-lookup"><span data-stu-id="1e7b6-103">Security best practices for Office 365</span></span>

<span data-ttu-id="1e7b6-104">이러한 권장된 모범 사례를 수행 하 여 데이터 위반 또는 손상 된 계정의 가능성을 최소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-104">Minimize the potential of a data breach or a compromised account by following these recommended best practices.</span></span>
  
<span data-ttu-id="1e7b6-p101">이 문서는 빠른 목록이 모범 사례를 포함합니다. 자세한 심도 깊은 분석 및 보안 설정에 대 한 정보를 참조 하십시오. [Office 365 보안 로드맵: 처음 30 일, 90 일 동안 및 이외 우선순위 가지 주요](security-roadmap.md)합니다. 이 문서의 정보를 제공 합니다 실제 공격에 대 한 조사에 따라 위험을 평가 하 고 가장 중요 한 보안, 규정 준수, 및 정보를 구현 하는 방법에 코칭 위쪽 Microsoft Office 365 cybersecurity 전문가 들을 제공 하는 위치 Office 365 테 넌 트를 보호 하기 위해 보호 제어 합니다. 위협 우선순위를 지정 기술 전략에 대 한 위협 요소를 변환 하 고 다음 기능 및 컨트롤을 구현 하려면 체계적인 방법을 활용 하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-p101">This article contains a quick list of best practices. For more in-depth analysis and information on setting up security, see [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](security-roadmap.md). In that article, you'll find information based on investigations of real-world attacks, where our top Microsoft Office 365 cybersecurity experts provide coaching on how to assess risk and implement the most critical security, compliance, and information protection controls to protect your Office 365 tenant. You'll learn how to prioritize threats, translate threats into technical strategy, and then take a systematic approach to implementing features and controls.</span></span>
  
## <a name="use-office-365-secure-score"></a><span data-ttu-id="1e7b6-109">Office 365 보안 점수를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="1e7b6-109">Use Office 365 Secure Score</span></span>

<span data-ttu-id="1e7b6-p102">보안 점수는 할 수 있는 추가 위험을 줄이는 것을 권장 하는 보안 분석 도구입니다. 보안 점수 Office 365 설정 및 작업을 확인 하 고 Microsoft에 의해 설정 된 초기 계획을 비교 합니다. 최상의 보안 방법으로는 어떻게 정렬 기준으로 점수를 얻을 수 있습니다. 보안 점수를 가져오고를 사용 하 여 Office 365 조직의 보안을 강화 하는 방법에 대 한 자세한 내용은 [Office 365 보안 점수 소개 (영문)을](office-365-secure-score.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-p102">Secure Score is a security analytics tool that recommends what you can do to further reduce risk. Secure Score looks at your Office 365 settings and activities and compares them to a baseline established by Microsoft. You'll get a score based on how aligned you are with best security practices. For more information about how to get Secure Score and use it to increase the security of your Office 365 organization, see [Introducing the Office 365 Secure Score](office-365-secure-score.md).</span></span>
  
<span data-ttu-id="1e7b6-114">보안 점수를 사용해 싶으십니까?</span><span class="sxs-lookup"><span data-stu-id="1e7b6-114">Want to try out Secure Score?</span></span>
  
<span data-ttu-id="1e7b6-115">[Office 365에 로그인](https://www.office.com/signin)Office 365 [대 한 Office 365 관리자 역할](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) 역할에 할당 된 작업이 나 교육용 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-115">Using a work or school account that has been assigned the Office 365 [About Office 365 admin roles](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) role, [sign in to Office 365](https://www.office.com/signin).</span></span>
  
<span data-ttu-id="1e7b6-116">Access 보안에서 점수 [https://SecureScore.office.com](https://SecureScore.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-116">Access Secure Score at [https://SecureScore.office.com](https://SecureScore.office.com).</span></span>
  
## <a name="use-multi-factor-authentication-mfa"></a><span data-ttu-id="1e7b6-117">다단계 인증 (MFA)를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="1e7b6-117">Use multi-factor authentication (MFA)</span></span>

<span data-ttu-id="1e7b6-p103">MFA는 사용자를 전화 통화, 텍스트 메시지 또는 올바르게 자신의 암호를 입력 한 후 스마트 전화기에서 전자 app 알림을 확인을 요구 하 여 강력한 암호 전략에 추가 계층의 보호를 추가 합니다. Office 365 사용자 계정 전체에서 MFA와 여전히 사용자의 암호가 손상 된 경우에 무단된 액세스 로부터 보호 됩니다. 계정 추가 시도 충족 된 후 액세스까지 계정에 부여 하지 않기 때문에 보호 됩니다. 손상 된 또는 도난당 한 암호 충분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-p103">MFA adds an additional layer of protection to a strong password strategy by requiring users to acknowledge a phone call, text message, or an app notification on their smart phone after correctly entering their password. With MFA in place, Office 365 user accounts are still protected against unauthorized access even if a user's password is compromised. Accounts are protected because access is not granted to an account until after the additional challenge has been satisfied. A compromised or stolen password is not enough.</span></span>
  
- [<span data-ttu-id="1e7b6-122">Office 365 배포에 대 한 다중 요소 인증에 대 한 계획</span><span class="sxs-lookup"><span data-stu-id="1e7b6-122">Plan for multi-factor authentication for Office 365 Deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="1e7b6-123">Office 365 사용자에 게 다단계 인증 설정</span><span class="sxs-lookup"><span data-stu-id="1e7b6-123">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a><span data-ttu-id="1e7b6-124">Office 365 클라우드 응용 프로그램 보안을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="1e7b6-124">Use Office 365 Cloud App Security</span></span>

<span data-ttu-id="1e7b6-p104">비정상적인 활동을 추적 및 작업을 수행 하 여 비즈니스 요구 사항에 따라 정책을 설정 합니다. 여러 번 시도 로그인 또는 로그인 시 알 수 없거나 위험한 IP 주소에서 실패 한 관리자가 많은 양의 데이터를 다운로드 하는 등의 비정상 또는 위험한 사용자 작업을 검토할 수 있도록 Office 365 클라우드 응용 프로그램 보안 경고를 설정 합니다. Office 365 Enterprise E5 플랜과 조직용 귀하가 Office 365 클라우드 응용 프로그램 보안을 사용 하 여 시작할 수 있습니다. 다른 엔터프라이즈 계획을 설치한 경우에 추가 기능으로 Office 365 클라우드 응용 프로그램 보안을 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-p104">Set up policies based on your business needs to track anomalous activity and act on it. Set up alerts with Office 365 Cloud App Security so that admins can review unusual or risky user activity, such as downloading large amounts of data, multiple failed sign-in attempts, or sign-ins from an unknown or dangerous IP address. For organizations with an Office 365 Enterprise E5 plan, you can start using Office 365 Cloud App Security right away. If you have a different enterprise plan, you can purchase Office 365 Cloud App Security as an add-on.</span></span>
  
- [<span data-ttu-id="1e7b6-129">O 365 클라우드 앱 보안 개요</span><span class="sxs-lookup"><span data-stu-id="1e7b6-129">Overview of O365 Cloud App Security</span></span>](office-365-cas-overview.md)
    
- [<span data-ttu-id="1e7b6-130">Office 365 Cloud App Security 켜기</span><span class="sxs-lookup"><span data-stu-id="1e7b6-130">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a><span data-ttu-id="1e7b6-131">보안 메일 흐름</span><span class="sxs-lookup"><span data-stu-id="1e7b6-131">Secure mail flow</span></span>

<span data-ttu-id="1e7b6-132">전자 메일을 통해 전송 되는 풍부한 기능 집합에서 Exchange Online 보호 하 고 각 전자 메일 메시지의 보낸 사람의 id에 대 한 큰 보증을 확보 합니다.를 보호 하 고 알 수 없는 맬웨어, 바이러스 및 악의적인 Url 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-132">Implement the rich feature set in Exchange Online Protection and gain greater assurance about the identity of the sender of each email message, and protect against unknown malware, viruses, and malicious URLs transmitted through emails.</span></span>
  
- <span data-ttu-id="1e7b6-133">조직에 대 한 [Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md) 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-133">Configure [Office 365 Email Anti-Spam Protection](anti-spam-protection.md) policies for your organization.</span></span> 
    
- <span data-ttu-id="1e7b6-134">소개 하 고 [안전한 첨부 파일 및 안전 링크에 대 한 고급 위협 보호](https://technet.microsoft.com/library/mt148491.aspx)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-134">Learn about and then use [Advanced threat protection for safe attachments and safe links](https://technet.microsoft.com/library/mt148491.aspx).</span></span>
    
- <span data-ttu-id="1e7b6-135">[조직에 맬웨어 방지 보호 기능을 추가](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-135">[Add anti-malware protection to your organization](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).</span></span>
    
- <span data-ttu-id="1e7b6-136">소개 하 고 사용자를 위한 [Office 365에서 전자 메일 메시지에 안전 팁](safety-tips-in-office-365.md) 를 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-136">Learn about and enable [Safety tips in email messages in Office 365](safety-tips-in-office-365.md) for your users.</span></span> 
    
- <span data-ttu-id="1e7b6-137">Office 365의 조직에 대 한 사용자 지정 도메인을 사용 중인 경우 조직에서 보낸 메일의 유효성을 검사 하 고 스푸핑을 방지 하는 데 도움이 SPF, DKIM, 및 DMARC를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-137">If you're using a custom domain for your organization in Office 365, set up SPF, DKIM, and then DMARC to validate mail sent by your organization and to help prevent spoofing:</span></span>
    
  - <span data-ttu-id="1e7b6-138">[SPF 스푸핑을 방지 하기 위해 Office 365에서 설정](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-138">[Set up SPF in Office 365 to help prevent spoofing](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx).</span></span>
    
  - <span data-ttu-id="1e7b6-139">[Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-139">[Use DKIM to validate outbound email sent from your custom domain in Office 365](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx).</span></span>
    
  - <span data-ttu-id="1e7b6-140">[Office 365의 전자 메일의 유효성을 검사를 사용 하 여 DMARC](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-140">[Use DMARC to validate email in Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span></span>
    
## <a name="enable-mailbox-audit-logging"></a><span data-ttu-id="1e7b6-141">사서함 감사 로깅 사용</span><span class="sxs-lookup"><span data-stu-id="1e7b6-141">Enable mailbox audit logging</span></span>

<span data-ttu-id="1e7b6-p105">일부 감사 로깅이 Office 365; 하면 자동으로 활성화 되는지 그러나 사서함 감사 로깅 기본적으로 켜져 있지 됩니다. Exchange Online PowerShell을 사용 하 여 Office 365의 모든 사용자 사서함에 대 한 감사 로깅을 설정 합니다. 내용은 [Office 365의 감사 사서함 사용](https://go.microsoft.com/fwlink/p/?LinkID=626109)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-p105">Some audit logging is automatically enabled for you in Office 365; however, mailbox audit logging is not turned on by default. You turn on audit logging for all user mailboxes in Office 365 by using Exchange Online PowerShell. For information, see [Enable mailbox auditing in Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).</span></span>
  
<span data-ttu-id="1e7b6-p106">감사 로그를 사용 하면 수 활성화 한 후 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md) 사용자가 보낸 메시지 및 기타 작업에 사서함 소유자, 위임된 된 사용자에 의해 수행 하 여 사용자 사서함에 로그인 확인 하려면 또는 관리자입니다. Office 365에 포함 된 사서함 활동의 목록에 대 한 감사 로그를 기본적으로 [Exchange 사서함 활동](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-p106">After you've enabled audit logging you can [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md) to find out who has logged into your user mailboxes, sent messages, and other activities performed by the mailbox owner, a delegated user, or an administrator. For a list of mailbox activities that are included in the Office 365 audit log by default, see [Exchange mailbox activities](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).</span></span>
  
<span data-ttu-id="1e7b6-147">감사 로그는 감사 로그 항목을 저장 하는 시간을 변경 하는 등로 수행할 수 있는 다른 작업에 대 한 내용은 [Exchange 2016에서 로깅 사서함 감사](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-147">For information about other actions you can perform with the audit log, such as changing the amount of time to save entries in the audit log, see [Mailbox audit logging in Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).</span></span>
  
## <a name="configure-data-loss-prevention-dlp"></a><span data-ttu-id="1e7b6-148">데이터 손실 방지 (DLP) 구성</span><span class="sxs-lookup"><span data-stu-id="1e7b6-148">Configure Data Loss Prevention (DLP)</span></span>

<span data-ttu-id="1e7b6-p107">DLP를 사용 하면 중요 한 데이터를 식별 하 고 사용자가 실수로 또는 의도적으로 데이터를 공유 하는 것을 방지 하는 정책을 만들 수 있습니다. DLP은 사용자에 게 잃지 규격 유지할 수 있도록 Exchange Online, SharePoint Online 및 OneDrive를 포함 하 여 Office 365에서 작동 합니다. 자세한 내용은 [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-p107">DLP allows you to identify sensitive data and create policies that help prevent your users from accidentally or intentionally sharing the data. DLP works across Office 365 including Exchange Online, SharePoint Online, and OneDrive so that your users can stay compliant without interrupting their workflow. For more information, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
## <a name="use-customer-lockbox"></a><span data-ttu-id="1e7b6-152">고객 Lockbox를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="1e7b6-152">Use Customer Lockbox</span></span>

<span data-ttu-id="1e7b6-p108">Office 365 관리자를으로 Microsoft 기술 지원 엔지니어 도움말 세션 중에 데이터에 액세스 하는 방법을 제어 하려면 고객 Lockbox를 사용할 수 있습니다. 엔지니어가 문제를 해결 하 고 문제를 해결 하 여 데이터에 대 한 액세스를 필요로 하는의 경우, 고객 Lockbox를 사용 하면 승인 하거나 거부 하는 액세스 요청 수 있습니다. 를 승인 하는 경우는 엔지니어 데이터에 액세스할 수 있습니다. 각 요청에 만료 시간이 있어서는 하 고 문제를 해결 한 후 요청을 닫고 access가 해지 되었습니다. Office 365 Enterprise 5 계획에 포함 된 고객 Lockbox 또는 다른 Office 365 enterprise 플랜과 별도 구독을 구입할 수 있습니다. 내용은 [Office 365 고객 Lockbox 요청](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-p108">As an Office 365 admin, you can use Customer Lockbox to control how a Microsoft support engineer accesses your data during a help session. In cases where the engineer requires access to your data to troubleshoot and fix an issue, Customer Lockbox allows you to approve or reject the access request. If you approve it, the engineer can access the data. Each request has an expiration time, and once the issue is resolved, the request is closed and access is revoked. Customer Lockbox is included in the Office 365 Enterprise 5 plan, or you can purchase a separate subscription with any other Office 365 enterprise plan. For information, see [Office 365 Customer Lockbox Requests](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).</span></span>
  
## <a name="try-it-yourself"></a><span data-ttu-id="1e7b6-159">사용자가 직접 사용해 보기</span><span class="sxs-lookup"><span data-stu-id="1e7b6-159">Try it yourself</span></span>
<span data-ttu-id="1e7b6-160"><a name="SecureScore"> </a></span><span class="sxs-lookup"><span data-stu-id="1e7b6-160"></span></span>

<span data-ttu-id="1e7b6-161">프로덕션 환경에서이 채택 하기 전에 Office 365 평가판 구독에서 작업 하는 이러한 보안 기능을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-161">See these security features working in an Office 365 trial subscription prior to adopting them in production.</span></span>
  
- [<span data-ttu-id="1e7b6-162">Office 365 평가판 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="1e7b6-162">Create an Office 365 trial subscription</span></span>](https://technet.microsoft.com/library/mt736406.aspx)
    
- [<span data-ttu-id="1e7b6-163">구성 하 고 MFA 사용자 계정에 대 한 테스트</span><span class="sxs-lookup"><span data-stu-id="1e7b6-163">Configure and test MFA for a user account</span></span>](https://technet.microsoft.com/library/mt492459.aspx)
    
- [<span data-ttu-id="1e7b6-164">구성 및 테스트 사용자에 게 알리도록 전역 관리자 활동의 Office 365 클라우드 응용 프로그램 보안</span><span class="sxs-lookup"><span data-stu-id="1e7b6-164">Configure and test Office 365 Cloud App Security to notify you of global admin activity</span></span>](https://technet.microsoft.com/library/mt757250.aspx)
    
- [<span data-ttu-id="1e7b6-165">구성 하 고 ATP 의심 스러운 전자 메일에 대 한 테스트</span><span class="sxs-lookup"><span data-stu-id="1e7b6-165">Configure and test ATP for suspicious email</span></span>](https://technet.microsoft.com/library/mt490479.aspx)
    
- <span data-ttu-id="1e7b6-166">위의 단계를 각각에 대 한 평가판 구독에 대 한 [Office 365 보안 점수](https://securescore.office.com/) 를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7b6-166">Check the [Office 365 Secure Score](https://securescore.office.com/) for your trial subscription for each of the above steps</span></span> 
    

