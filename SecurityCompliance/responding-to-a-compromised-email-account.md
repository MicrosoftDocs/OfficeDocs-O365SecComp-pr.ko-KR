---
title: Office 365에서 손상된 이메일 계정에 응답
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: 인식 하 고 Office 365에서 손상 된 전자 메일 계정에 응답 하는 방법을 설명 합니다.
ms.openlocfilehash: bf3350da88804639356100fb5be2403c76cbcec6
ms.sourcegitcommit: 17dda7ece5c9e884944a92ac0f842cf1e62ec506
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/14/2018
ms.locfileid: "23977593"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a><span data-ttu-id="e0f28-103">Office 365에서 손상된 이메일 계정에 응답</span><span class="sxs-lookup"><span data-stu-id="e0f28-103">Responding to a Compromised Email Account in Office 365</span></span>

<span data-ttu-id="e0f28-104">**요약** 인식 하 고 Office 365에서 손상 된 전자 메일 계정에 응답 하는 방법에 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-104">**Summary** Learn how to recognize and respond to a compromised email account in Office 365.</span></span>

## <a name="what-is-a-compromised-email-account-in-office-365"></a><span data-ttu-id="e0f28-105">Office 365에서 손상 된 전자 메일 계정 이란?</span><span class="sxs-lookup"><span data-stu-id="e0f28-105">What is a Compromised Email Account in Office 365?</span></span>
<span data-ttu-id="e0f28-p101">Office 365 사서함, 데이터 및 기타 서비스에 대 한 액세스, 사용자 이름 및 암호 또는 PIN 같은 자격 증명을 사용 하 여 제어 됩니다. 이러한 자격 증명을 훔쳐 의도 한 사용자가 아닌 다른 도난당 한 자격 증명 노출 되었을 수 있다고 간주 됩니다. 이러한 공격자는 원래 사용자로 로그인 작업을 수행할 수 불법 합니다. 공격자는 도난당 한 자격 증명을 사용 하 여 사용자의 Office 365 사서함, SharePoint 폴더 또는 파일은 사용자의 OneDrive에서 액세스할 수 있습니다. 일반적으로 표시 하는 하나의 작업은 내부와 조직 외부의 받는 사람에 게는 원래 사용자로 전자 메일을 보내는 공격자가 있습니다. 공격자가 외부 받는 사람에 게 데이터를 전자 메일, 데이터 exfiltration이 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p101">Access to Office 365 mailboxes, data and other services, is controlled through the use of credentials, for example a user name and password or PIN. When someone other than the intended user steals those credentials, the stolen credentials are considered to be compromised. With them the attacker can sign in as the original user and perform illicit actions. Using the stolen credentials, the attacker can access the user’s Office 365 mailbox, SharePoint folders, or files in the user's OneDrive. One action commonly seen is the attacker sending emails as the original user to recipients both inside and outside of the organization. When the attacker emails data to external recipients, this is called data exfiltration.</span></span>

## <a name="symptoms-of-a-compromised-office-365-email-account"></a><span data-ttu-id="e0f28-112">손상 된 Office 365 전자 메일 계정에 대 한 현상</span><span class="sxs-lookup"><span data-stu-id="e0f28-112">Symptoms of a Compromised Office 365 Email Account</span></span>
<span data-ttu-id="e0f28-p102">사용자는 것을 알 하 고 Office 365 사서함에서 비정상적인 동작을 보고 될 수 있습니다. 다음은 일반적인 몇가지 증상입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p102">Users might notice and report unusual activity in their Office 365 mailboxes. Here are some common symptoms:</span></span>
- <span data-ttu-id="e0f28-115">누락 되거나 삭제 된 전자 메일 같은 의심 스러운 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-115">Suspicious activity, such as missing or deleted emails.</span></span>
- <span data-ttu-id="e0f28-116">다른 사용자에 게 보낸의 **보낸편지함** 폴더에 기존 해당 전자 메일 없이 손상 된 계정에서 전자 메일을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-116">Other users might receive emails from the compromised account without the corresponding email existing in the **Sent Items** folder of the sender.</span></span>
- <span data-ttu-id="e0f28-p103">원하는 사용자 또는 관리자가 만든 받지는 받은 편지함 규칙의 현재 상태입니다. 이러한 규칙 자동으로 알 수 없는 주소로 전자 메일을 전달할 수도 있습니다 슬라이드 **노트**, **정크 메일**또는 **RSS 구독** 폴더를으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p103">The presence of inbox rules that weren't created by the intended user or the administrator. These rules may automatically forward emails to unknown addresses or move them to the **Notes**, **Junk Email**, or **RSS Subscriptions** folders.</span></span>
- <span data-ttu-id="e0f28-119">전체 주소 목록에서 사용자의 표시 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-119">The user's display name might be changed in the Global Address List.</span></span>
- <span data-ttu-id="e0f28-120">사용자의 사서함에서 전자 메일을 보낼 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-120">The user's mailbox is blocked from sending email.</span></span>
- <span data-ttu-id="e0f28-121">Microsoft Outlook Web App 또는 Microsoft Outlook에서 보낸 편지함 또는 지운 편지함 폴더 "런던, 보내기 money에서에서 문의할 팔 I."와 같은 일반적인 해킹 계정 메시지를 포함</span><span class="sxs-lookup"><span data-stu-id="e0f28-121">The Sent or Deleted Items folders in Microsoft Outlook or in Microsoft Outlook Web App contain common hacked-account messages, such as "I'm stuck in London, send money."</span></span>
- <span data-ttu-id="e0f28-122">예: 이름, 전화번호, 또는 우편번호 비정상적인 프로필 변경 사항이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-122">Unusual profile changes, such as the name, the telephone number, or the postal code were updated.</span></span>
- <span data-ttu-id="e0f28-123">특수 한 자격 증명을 여러 번 암호 변경 같은 변경이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-123">Unusual credential changes, such as multiple password changes are required.</span></span>
- <span data-ttu-id="e0f28-124">메일 전달 최근에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-124">Mail forwarding was recently added.</span></span>
- <span data-ttu-id="e0f28-125">예: 위조 금융 서명 또는 처방전 약물 서명을 비정상적인 서명 최근에, 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-125">An unusual signature was recently added, such as a fake banking signature or a prescription drug signature.</span></span>

<span data-ttu-id="e0f28-p104">사용자가 보고 위의 증상 중 하나를 수행 해야 추가로 조사 합니다. Office 365 보안 및 규정 준수 센터와 Azure 포털 생길 수 있는 것으로 의심 되는 사용자 계정에 대 한 작업을 검사 하는데 도움이 되는 도구를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p104">If a user reports any of the above symptoms, you should perform further investigation. The Office 365 Security & Compliance Center and the Azure Portal offer tools to help you investigate the activity of a user account that you suspect may be compromised.</span></span>
- <span data-ttu-id="e0f28-p105">보안 및 규정 준수 센터-office 365 통합 감사 로그의 날짜 범위에 걸쳐에서 의심 스러운 작업이 현재 날짜를 발생 하기 직전에 대 한 결과 필터링 하 여 의심 되는 계정에 대 한 모든 작업을 검토 합니다. 필터링 하지 않습니다 활동에서 검색 하는 동안.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p105">Office 365 Unified Audit Logs in the Security & Compliance Center - Review all the activities for the suspected account by filtering the results for the date range spanning from immediately before the suspicious activity occurred to the current date. Do not filter on the activities during the search.</span></span>
- <span data-ttu-id="e0f28-p106">Azure AD 로그인 로그와 Azure AD 포털에서 사용할 수 있는 다른 위험 보고서를 사용 합니다. 이러한 열에서 값을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p106">Use the Azure AD Sign-in logs and other risk reports that are available in the Azure AD portal. Examine the values in these columns:</span></span>
    - <span data-ttu-id="e0f28-132">IP 주소를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-132">Review IP address</span></span>
    - <span data-ttu-id="e0f28-133">로그인 위치</span><span class="sxs-lookup"><span data-stu-id="e0f28-133">sign-in locations</span></span>
    - <span data-ttu-id="e0f28-134">로그인 시간</span><span class="sxs-lookup"><span data-stu-id="e0f28-134">sign-in times</span></span>
    - <span data-ttu-id="e0f28-135">로그인 성공 또는 실패</span><span class="sxs-lookup"><span data-stu-id="e0f28-135">sign-in success or failure</span></span>



## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a><span data-ttu-id="e0f28-136">보안을 유지 하 고 전자 메일 함수는 의심 되는 복원 하는 방법에는 Office 365 계정 및 사서함이 손상 된</span><span class="sxs-lookup"><span data-stu-id="e0f28-136">How to secure and restore email function to a suspected compromised Office 365 account and mailbox</span></span>

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

<span data-ttu-id="e0f28-137">사용자의 계정에 대 한 액세스를 재설정 했을 때, 한 후에 공격자가 추가한 항목이 있을 수 백 도어 계정의 제어를 다시 시작 하는 공격자가 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-137">Even after you've regained access to your account, the attacker may have added back-door entries that enable the attacker to resume control of the account.</span></span>

<span data-ttu-id="e0f28-p107">가로채기 프로그램 다시 시작 되지 않으면 되도록 좋음 계정을 제어 하는 빨리 계정에 대 한 액세스를 다시 사용 하려면 다음 단계를 모두 수행 해야 합니다. 이러한 단계는 가로채기 프로그램 계정에 추가 될 수 있습니다 백 도어 항목을 제거 하는데 도움이 됩니다. 다음이 단계를 수행 하 고 나면 컴퓨터 손상 되지 되도록 바이러스 검사를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p107">You must perform all the following steps to regain access to your account the sooner the better to make sure that the hijacker doesn't resume control your account. These steps help you remove any back-door entries that the hijacker may have added to your account. After you perform these steps, we recommend that you run a virus scan to make sure that your computer isn't compromised.</span></span>

### <a name="step-1-reset-the-users-password"></a><span data-ttu-id="e0f28-141">1 단계는 사용자의 암호를 다시 설정</span><span class="sxs-lookup"><span data-stu-id="e0f28-141">Step 1 Reset the user's password</span></span>
> [!WARNING]
> <span data-ttu-id="e0f28-142">공격자가 계속 액세스할 수 있으면 사서함이 시점에서 전자 메일을 통해 의도 한 사용자에 게 새 암호를 보내기를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-142">Do not send the new password to the intended user through email as the attacker still has access to the mailbox at this point.</span></span>

1. <span data-ttu-id="e0f28-143">다른 사용자에 대 한 암호는 재설정 Office 365 비즈니스에 따라 다른 절차에서는 [관리자: 비즈니스 암호 다시 설정 하는 Office 365](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)</span><span class="sxs-lookup"><span data-stu-id="e0f28-143">Follow the Reset an Office 365 business password for someone else procedures in [Admins: Reset Office 365 business passwords](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)</span></span>

<span data-ttu-id="e0f28-144">**참고:**</span><span class="sxs-lookup"><span data-stu-id="e0f28-144">**Notes:**</span></span>
- <span data-ttu-id="e0f28-145">암호가 강력한 지 대 / 소문자, 하나 이상의 번호 및 특수 문자를 하나 이상 포함 되어있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-145">Make sure that the password is strong and that it contains upper and lowercase letters, at least one number, and at least one special character.</span></span> 
- <span data-ttu-id="e0f28-p108">다시 사용 하면 마지막 5 개의 암호입니다. 암호 기록 요구 사항을 보다 최근 암호를 다시 사용할 수 있습니다를 하는 경우에 공격자가 예상할 수 있음을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p108">Don't reuse any of your last five passwords. Even though the password history requirement lets you reuse a more recent password, you should select something that the attacker can't guess.</span></span>
- <span data-ttu-id="e0f28-148">온-프레미스 사용자의 id는 Office 365와 페더레이션 되어있는지, 암호에서 온-프레미스를 변경 해야 하 고 손상의 관리자에 게 문의 알려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-148">If your on-premises identity is federated with Office 365, you must change your password on-premises, and then you must notify your administrator of the compromise.</span></span>

> [!TIP]
> <span data-ttu-id="e0f28-p109">관리 권한 가진 계정에 대 한 특히 손상을 방지 하기 위해 다단계 인증 (MFA)를 사용 하는 것이 좋습니다.  자세한 내용은 [여기](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6)합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p109">It is highly recommended that you enable Multi-Factor Authentication (MFA) in order to prevent compromise, especially for accounts with administrative priviledges.  You can learn more [here](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).</span></span>

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a><span data-ttu-id="e0f28-151">단계 2 제거 의심 스러운 전자 메일 전달 주소</span><span class="sxs-lookup"><span data-stu-id="e0f28-151">Step 2 Remove suspicious email forwarding addresses</span></span>
1. <span data-ttu-id="e0f28-152">열기는 **Office 365 관리 센터 > 활성 사용자**합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-152">Open the **Office 365 Admin Center > Active Users**.</span></span>
2. <span data-ttu-id="e0f28-153">문제의 사용자 계정을 찾아서 **메일 설정**을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-153">Find the user account in question and expand **Mail Settings**.</span></span>
3. <span data-ttu-id="e0f28-154">**전자 메일 전달**, **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-154">For **Email forwarding**, click **Edit**.</span></span>
4. <span data-ttu-id="e0f28-155">의심 스러운 전달 주소를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-155">Remove any suspicious forwarding addresses.</span></span>

### <a name="step-3-disable-any-suspicious-inbox-rules"></a><span data-ttu-id="e0f28-156">3 단계는 의심 스러운 받은 편지함 규칙을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="e0f28-156">Step 3 Disable any suspicious inbox rules</span></span>
1. <span data-ttu-id="e0f28-157">Outlook Web App (OWA)를 사용 하 여 사용자의 사서함에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-157">Sign in to the user's mailbox using Outlook Web App (OWA).</span></span>
2. <span data-ttu-id="e0f28-158">기어 아이콘 누르고 **메일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-158">Click on the gear icon and click **Mail**.</span></span>
3. <span data-ttu-id="e0f28-159">**받은 편지함과 스위프 규칙** 을 클릭 하 고 규칙을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-159">Click **Inbox and sweep rules** and review the rules.</span></span>
4. <span data-ttu-id="e0f28-160">사용 하지 않거나 의심 스러운 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-160">Disable or delete suspicious rules.</span></span>

### <a name="step-4-unblock-the-user-from-sending-mail"></a><span data-ttu-id="e0f28-161">4 단계 차단 해제에서 메일을 보내는 사용자</span><span class="sxs-lookup"><span data-stu-id="e0f28-161">Step 4 Unblock the user from sending mail</span></span>
<span data-ttu-id="e0f28-162">스팸 전자 메일을 보낼 의심 되는 손상 된 사서함이 불법 사용 된 경우 호스팅되고 사서함에서 메일을 보낼 차단 되었다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-162">If the suspected compromised mailbox was used illicitly to send spam email, it is likely that the mailbox has been blocked from sending mail.</span></span>
1. <span data-ttu-id="e0f28-163">메일을 보내는에서 사서함을 차단을 해제 하려면 [사용자, 도메인 또는 스팸 전자 메일을 보낸 후 차단 목록에서 IP 주소를 제거](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email )의 절차를 따르십시오.</span><span class="sxs-lookup"><span data-stu-id="e0f28-163">To unblock a mailbox from sending mail, follow the procedures in [Removing a user, domain, or IP Address from a block list after sending spam email](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email ).</span></span>

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a><span data-ttu-id="e0f28-164">5 단계 선택 사항: 사용자 계정을에서 서명에서 차단</span><span class="sxs-lookup"><span data-stu-id="e0f28-164">Step 5 Optional: Block the user account from signing-in</span></span>
> [!IMPORTANT]
> <span data-ttu-id="e0f28-165">서명 기능에 대 한 액세스를 다시 사용 하도록 설정 해도 안전 합니다 판단 되는 경우 때까지에서 손상된 된 의심 되는 계정을 차단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-165">You can block the suspected compromised account from signing-in until you believe it is safe to re-enable access.</span></span>

1. <span data-ttu-id="e0f28-166">Office 365 관리 센터로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-166">Go to the Office 365 admin center.</span></span>
2. <span data-ttu-id="e0f28-167">Office 365 관리 센터에서 **사용자**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-167">In the Office 365 admin center, select **Users**.</span></span>
3. <span data-ttu-id="e0f28-168">차단할 직원을 선택 하 고 사용자 창에서 **로그인 상태** 옆에 있는 **편집** 을 선택 합니다</span><span class="sxs-lookup"><span data-stu-id="e0f28-168">Select the employee that you want to block, and then choose **Edit** next to **Sign-in status** in the user pane</span></span>
4. <span data-ttu-id="e0f28-169">**로그인 상태** 창에서 **로그인 차단 됨** 을 선택한 다음 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-169">On the **Sign-in status** pane, choose **Sign-in blocked** and then **Save**.</span></span> 
5. <span data-ttu-id="e0f28-170">Office 365 관리 센터의 왼쪽 탐색 창에서 **관리 센터** 를 확장 하 고 **Exchange**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-170">In the Office 365 admin center, in the lower-left navigation pane, expand **Admin Centers** and select **Exchange**.</span></span>
6. <span data-ttu-id="e0f28-171">Exchange 관리 센터에서 이동 **받는 사람 > 사서함**합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-171">In the Exchange admin center, navigate to **Recipients > Mailboxes**.</span></span>
7. <span data-ttu-id="e0f28-172">사용자를 선택 하 고 사용자 속성 페이지에서 **모바일 장치** **Exchange ActivcSync 사용 하지 않도록 설정** 하 고 **장치용 OWA 사용 하지 않도록 설정** 를클릭하고 모두에 **예라고** 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-172">Select the user, and on the user properties page, under **Mobile Devices**, click **Disable Exchange ActivcSync** and **Disable OWA for Devices** and answer **yes** to both.</span></span>
8. <span data-ttu-id="e0f28-173">**전자 메일 연결**, **사용 하지 않도록 설정** 하 고 응답 **예**입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-173">Under **Email Connectivity**, **Disable** and answer **yes**.</span></span> 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a><span data-ttu-id="e0f28-174">6 단계 선택 사항: 모든 관리 역할 그룹에서 손상된 된 의심 되는 계정 제거</span><span class="sxs-lookup"><span data-stu-id="e0f28-174">Step 6 Optional: Remove the suspected compromised account from all administrative role groups</span></span>
> [!NOTE]
> <span data-ttu-id="e0f28-175">계정 보호 된 후에 관리 역할 그룹 구성원 자격을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-175">Administrative role group membership can be restored after the account has been secured.</span></span>

1. <span data-ttu-id="e0f28-176">전역 관리자 계정 사용 하 여 Office 365 관리 센터에 로그인 하 고 **활성 사용자**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-176">Sign in to the Office 365 Admin Center with a global administrator account and open **Active Users**.</span></span>
2. <span data-ttu-id="e0f28-177">의심 되는 계정 손상 및 계정에 할당 된 모든 관리 역할이 있는지를 수동으로 확인를 찾아보십시오.</span><span class="sxs-lookup"><span data-stu-id="e0f28-177">Find the suspected compromised account and manually check to see if there are any administrative roles assigned to the account.</span></span>
3. <span data-ttu-id="e0f28-178">**보안 및 규정 준수 센터를**엽니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-178">Open the **Security & Compliance Center**.</span></span>
4. <span data-ttu-id="e0f28-179">**사용 권한**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-179">Click **Permissions**.</span></span>
5. <span data-ttu-id="e0f28-p110">수동으로 확인 하려면는 의심 되는 손상 된 계정 하에 소속 역할 그룹을 검토 합니다.  하다 면: a. 역할 그룹을 클릭 하 고 **역할 그룹 편집**을 클릭 합니다.  b. 역할 그룹에서 사용자를 제거 하려면 **선택한 구성원** 및 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p110">Manually review the role groups to see if the suspected compromised account is a member of any of them.  If it is:  a. Click the role group and click **Edit Role Group**.  b. Click **Chose Members** and **Edit** to remove the user from the role group.</span></span>
6. <span data-ttu-id="e0f28-185">**Exchange 관리 센터** 를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-185">Open the **Exchange Admin Center**</span></span>
7. <span data-ttu-id="e0f28-186">**사용 권한**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-186">Click **Permissions**.</span></span>
8. <span data-ttu-id="e0f28-p111">수동으로 확인 하려면는 의심 되는 손상 된 계정 하에 소속 역할 그룹을 검토 합니다. 하다 면: a. 역할 그룹을 클릭 하 고 **편집**을 클릭 합니다.  b. 역할 그룹에서 사용자를 제거 하려면 **구성원** 섹션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p111">Manually review the role groups to see if the suspected compromised account is a member of any of them. If it is:  a. Click the role group and click **Edit**.  b. Use the **members** section to remove the user from the role group.</span></span>

### <a name="step-7-optional-additional-precautionary-steps"></a><span data-ttu-id="e0f28-192">사전 단계를 추가 하는 7 단계 선택 사항:</span><span class="sxs-lookup"><span data-stu-id="e0f28-192">Step 7 Optional: Additional precautionary steps</span></span>
1. <span data-ttu-id="e0f28-p112">보낸된 항목을 확인 하 고 있는지 확인 하십시오. 사용자 계정이 손상 된 대화 상대 목록에서 사용자에 게 알리기 해야할 수 있습니다. 공격자가 될 수 있습니다 있을 것을 요청 비용에 대 한 스푸핑, 등 다른 국가에 남아 된 및 비용, 필요 하거나 공격자가 바이러스도 자신의 컴퓨터를 무단로 전송 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p112">Make sure that you verify your sent items. You may have to inform people on your contacts list that your account was compromised. The attacker may have asked them for money, spoofing, for example, that you were stranded in a different country and needed money, or the attacker may send them a virus to also hijack their computers.</span></span>
2. <span data-ttu-id="e0f28-p113">다른 서비스를 해당 대체 전자 메일 계정 손상 된이 Exchange 계정을 사용 합니다. 먼저, Office 365 구독에 대해 이러한 단계를 수행 하 고 다른 계정에 대해 이러한 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p113">Any other service that used this Exchange account as its alternative email account may have been compromised. First, perform these steps for your Office 365 subscription, and then perform these steps for your other accounts.</span></span>
3. <span data-ttu-id="e0f28-198">전화번호 및 주소와 같은 연락처 정보, 정확한 지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-198">Make sure that your contact information, such as telephone numbers and addresses, is correct.</span></span>

## <a name="secure-office-365-like-a-cybersecurity-pro"></a><span data-ttu-id="e0f28-199">Office 365 전문가 cybersecurity와 같은 보안</span><span class="sxs-lookup"><span data-stu-id="e0f28-199">Secure Office 365 like a cybersecurity pro</span></span>
<span data-ttu-id="e0f28-p114">Office 365 구독 강력한 데이터 및 사용자를 보호 하기 위해 사용할 수 있는 보안 기능 집합을 함께 제공 됩니다.  사용 하는 [Office 365 보안 로드맵: 처음 30 일, 90 일 동안 및 이외 우선순위 가지 주요](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) Microsoft Office 365 테 넌 트를 보호 하기 위한 최상의 방법을 구현 하 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p114">Your Office 365 subscription comes with a powerful set of security capabilities that you can use to protect your data and your users.  Use the [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) to implement Microsoft recommended best practices for securing your Office 365 tenant.</span></span>
- <span data-ttu-id="e0f28-p115">처음 30 일에서 수행 하는 작업입니다.  낮은 영향 및 영향을 주지는 즉시 이러한 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p115">Tasks to accomplish in the first 30 days.  These have immediate affect and are low-impact to your users.</span></span>
- <span data-ttu-id="e0f28-p116">90 일에서을 수행 하는 작업입니다. 이러한 계획 및 구현 하지만 보안 환경을 크게 개선 하는 약간 더 많은 시간이 걸릴.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p116">Tasks to accomplish in 90 days. These take a bit more time to plan and implement but greatly improve your security posture.</span></span>
- <span data-ttu-id="e0f28-p117">90 일 이상. 이러한 향상 된 첫번째 90 일이 작업의에서 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f28-p117">Beyond 90 days. These enhancements build in your first 90 days work.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0f28-208">참고 항목:</span><span class="sxs-lookup"><span data-stu-id="e0f28-208">See also:</span></span>
- [<span data-ttu-id="e0f28-209">Office 365에 대한 보안 모범 사례</span><span class="sxs-lookup"><span data-stu-id="e0f28-209">Security best practices for Office 365</span></span>](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [<span data-ttu-id="e0f28-210">Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격 감지 및 재구성</span><span class="sxs-lookup"><span data-stu-id="e0f28-210">Detect and Remediate Outlook Rules and Custom Forms Injections Attacks in Office 365</span></span>](detect-and-remediate-outlook-rules-forms-attack.md)
- [<span data-ttu-id="e0f28-211">인터넷 범죄 불만 센터</span><span class="sxs-lookup"><span data-stu-id="e0f28-211">Internet Crime Complaint Center</span></span>](http://www.ic3.gov/preventiontips.aspx)
- [<span data-ttu-id="e0f28-212">유가 증권의 and Exchange 수수료-"피싱" 사기</span><span class="sxs-lookup"><span data-stu-id="e0f28-212">Securities and Exchange Commission - "Phishing" Fraud</span></span>](http://www.sec.gov/investor/pubs/phishing.htm)
