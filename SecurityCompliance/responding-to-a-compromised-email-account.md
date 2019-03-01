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
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Office 365에서 손상 된 전자 메일 계정을 인식 하 고 응답 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 326ec01c570ad97b5f1eaf06dcfe1ad4e6ad76f4
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341099"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a><span data-ttu-id="1b417-103">Office 365에서 손상된 이메일 계정에 응답</span><span class="sxs-lookup"><span data-stu-id="1b417-103">Responding to a Compromised Email Account in Office 365</span></span>

<span data-ttu-id="1b417-104">**요약** Office 365에서 손상 된 전자 메일 계정을 인식 하 고이에 대응 하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-104">**Summary** Learn how to recognize and respond to a compromised email account in Office 365.</span></span>

## <a name="what-is-a-compromised-email-account-in-office-365"></a><span data-ttu-id="1b417-105">Office 365에서 손상 된 전자 메일 계정 이란?</span><span class="sxs-lookup"><span data-stu-id="1b417-105">What is a Compromised Email Account in Office 365?</span></span>
<span data-ttu-id="1b417-p101">Office 365 사서함, 데이터 및 기타 서비스에 대 한 액세스는 사용자 이름, 암호 또는 PIN과 같은 자격 증명을 사용 하 여 제어 합니다. 의도 하지 않은 사용자가 해당 자격 증명을 도용 하면 도난당 한 자격 증명이 손상 된 것으로 간주 됩니다. 이를 통해 공격자가 원래 사용자로 로그인 하 고 불법 작업을 수행할 수 있습니다. 도난 당한 자격 증명을 사용 하 여 공격자가 사용자의 Office 365 사서함, SharePoint 폴더 또는 사용자의 OneDrive에 있는 파일에 액세스할 수 있습니다. 일반적으로 공격자는 조직 내부 및 외부의 받는 사람에 게 전자 메일을 보내는 것으로 간주 됩니다. 공격자가 외부의 받는 사람에 게 데이터를 전자 메일로 보내는 경우이를 데이터 exfiltration 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p101">Access to Office 365 mailboxes, data and other services, is controlled through the use of credentials, for example a user name and password or PIN. When someone other than the intended user steals those credentials, the stolen credentials are considered to be compromised. With them the attacker can sign in as the original user and perform illicit actions. Using the stolen credentials, the attacker can access the user’s Office 365 mailbox, SharePoint folders, or files in the user's OneDrive. One action commonly seen is the attacker sending emails as the original user to recipients both inside and outside of the organization. When the attacker emails data to external recipients, this is called data exfiltration.</span></span>

## <a name="symptoms-of-a-compromised-office-365-email-account"></a><span data-ttu-id="1b417-112">손상 된 Office 365 전자 메일 계정의 현상</span><span class="sxs-lookup"><span data-stu-id="1b417-112">Symptoms of a Compromised Office 365 Email Account</span></span>
<span data-ttu-id="1b417-p102">사용자가 Office 365 사서함에서 이상한 활동을 확인 하 고 보고할 수 있습니다. 일반적인 몇 가지 증상은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p102">Users might notice and report unusual activity in their Office 365 mailboxes. Here are some common symptoms:</span></span>
- <span data-ttu-id="1b417-115">누락 되었거나 삭제 된 전자 메일 같은 의심 스러운 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-115">Suspicious activity, such as missing or deleted emails.</span></span>
- <span data-ttu-id="1b417-116">다른 사용자가 보낸 사람의 **보낸 편지함** 폴더에 해당 하는 전자 메일을 사용 하지 않고 손상 된 계정의 전자 메일을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-116">Other users might receive emails from the compromised account without the corresponding email existing in the **Sent Items** folder of the sender.</span></span>
- <span data-ttu-id="1b417-p103">의도 한 사용자 또는 관리자가 만들지 않은 받은 편지함 규칙이 있는지 여부 이러한 규칙은 전자 메일을 알 수 없는 주소로 자동 전달 하거나 **Notes**, **정크 메일**또는 **RSS 구독** 폴더로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p103">The presence of inbox rules that weren't created by the intended user or the administrator. These rules may automatically forward emails to unknown addresses or move them to the **Notes**, **Junk Email**, or **RSS Subscriptions** folders.</span></span>
- <span data-ttu-id="1b417-119">사용자의 표시 이름이 전체 주소 목록에서 변경 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-119">The user's display name might be changed in the Global Address List.</span></span>
- <span data-ttu-id="1b417-120">사용자의 사서함이 차단 된 전자 메일을 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-120">The user's mailbox is blocked from sending email.</span></span>
- <span data-ttu-id="1b417-121">Microsoft outlook 또는 웹용 outlook (이전의 outlook web App)에 있는 보낸 편지함 또는 지운 편지함 폴더에는 일반적인 해킹 당한 계정 메시지 (예: "London에 걸려 온 금액 보내기")가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-121">The Sent or Deleted Items folders in Microsoft Outlook or Outlook on the web (formerly known as Outlook Web App) contain common hacked-account messages, such as "I'm stuck in London, send money."</span></span>
- <span data-ttu-id="1b417-122">이름, 전화 번호 또는 우편 번호와 같은 이상한 프로필 변경 내용이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-122">Unusual profile changes, such as the name, the telephone number, or the postal code were updated.</span></span>
- <span data-ttu-id="1b417-123">암호를 여러 번 변경 하는 등의 예외적인 자격 증명을 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-123">Unusual credential changes, such as multiple password changes are required.</span></span>
- <span data-ttu-id="1b417-124">메일 전달이 최근에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-124">Mail forwarding was recently added.</span></span>
- <span data-ttu-id="1b417-125">가짜 은행 서명 또는) 마약 서명과 같은 이상한 서명이 최근에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-125">An unusual signature was recently added, such as a fake banking signature or a prescription drug signature.</span></span>

<span data-ttu-id="1b417-p104">사용자가 위의 증상 중 하나를 보고 하면 자세히 조사를 수행 해야 합니다. Office 365 Security & 준수 센터 및 Azure Portal은 손상 된 것으로 의심 되는 사용자 계정의 작업을 조사 하는 데 도움이 되는 도구를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p104">If a user reports any of the above symptoms, you should perform further investigation. The Office 365 Security & Compliance Center and the Azure Portal offer tools to help you investigate the activity of a user account that you suspect may be compromised.</span></span>
- <span data-ttu-id="1b417-p105">Office 365 보안 & 준수 센터의 통합 감사 로그-의심 스러운 활동이 발생 하기 직전부터 현재 날짜까지까지 영향을 받은 날짜 범위에 대 한 결과를 필터링 하 여 의심 스러운 계정에 대 한 모든 활동을 검토 합니다. 검색 중에는 작업을 필터링 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p105">Office 365 Unified Audit Logs in the Security & Compliance Center - Review all the activities for the suspected account by filtering the results for the date range spanning from immediately before the suspicious activity occurred to the current date. Do not filter on the activities during the search.</span></span>
- <span data-ttu-id="1b417-p106">azure ad 포털에서 사용할 수 있는 azure ad 로그인 로그 및 기타 위험 보고서를 사용 합니다. 다음 열에 있는 값을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p106">Use the Azure AD Sign-in logs and other risk reports that are available in the Azure AD portal. Examine the values in these columns:</span></span>
    - <span data-ttu-id="1b417-132">IP 주소 검토</span><span class="sxs-lookup"><span data-stu-id="1b417-132">Review IP address</span></span>
    - <span data-ttu-id="1b417-133">로그인 위치</span><span class="sxs-lookup"><span data-stu-id="1b417-133">sign-in locations</span></span>
    - <span data-ttu-id="1b417-134">로그인 시간</span><span class="sxs-lookup"><span data-stu-id="1b417-134">sign-in times</span></span>
    - <span data-ttu-id="1b417-135">로그인 성공 또는 실패</span><span class="sxs-lookup"><span data-stu-id="1b417-135">sign-in success or failure</span></span>

## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a><span data-ttu-id="1b417-136">의심 스러운 Office 365 계정 및 사서함으로 전자 메일 기능을 보호 하 고 복원 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1b417-136">How to secure and restore email function to a suspected compromised Office 365 account and mailbox</span></span>

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

<span data-ttu-id="1b417-137">사용자의 계정에 대 한 액세스를 다시 받은 후에도 공격자가 백도어 항목을 추가 하 여 공격자가 계정에 대 한 제어권을 계속 해 서 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-137">Even after you've regained access to your account, the attacker may have added back-door entries that enable the attacker to resume control of the account.</span></span>

<span data-ttu-id="1b417-p107">hijacker에서 사용자의 계정을 계속 제어 하지 않도록 하려면 다음 단계를 모두 수행 하 여 계정에 다시 액세스 하는 것이 좋습니다. 이러한 단계는 hijacker에서 계정에 추가 했을 수 있는 모든 백도어 항목을 제거 하는 데 도움이 됩니다. 이러한 단계를 수행한 후에는 컴퓨터가 손상 되지 않았는지 확인 하기 위해 바이러스 검사를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p107">You must perform all the following steps to regain access to your account the sooner the better to make sure that the hijacker doesn't resume control your account. These steps help you remove any back-door entries that the hijacker may have added to your account. After you perform these steps, we recommend that you run a virus scan to make sure that your computer isn't compromised.</span></span>

### <a name="step-1-reset-the-users-password"></a><span data-ttu-id="1b417-141">1 단계 사용자 암호 다시 설정</span><span class="sxs-lookup"><span data-stu-id="1b417-141">Step 1 Reset the user's password</span></span>
> [!WARNING]
> <span data-ttu-id="1b417-142">지금은 공격자가 사서함에 액세스할 수 있으므로 전자 메일을 통해 원하는 사용자에 게 새 암호를 보내지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-142">Do not send the new password to the intended user through email as the attacker still has access to the mailbox at this point.</span></span>

1. <span data-ttu-id="1b417-143">관리자에 게 [office 365 business 암호 재설정](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c) 의 다른 사용자를 위해 office 365 business 암호 재설정을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-143">Follow the Reset an Office 365 business password for someone else procedures in [Admins: Reset Office 365 business passwords](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)</span></span>

<span data-ttu-id="1b417-144">**참고:**</span><span class="sxs-lookup"><span data-stu-id="1b417-144">**Notes:**</span></span>
- <span data-ttu-id="1b417-145">암호가 강력 하 고 암호에 대 문자와 소문자, 숫자가 하나 이상, 특수 문자가 하나 이상 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-145">Make sure that the password is strong and that it contains upper and lowercase letters, at least one number, and at least one special character.</span></span> 
- <span data-ttu-id="1b417-p108">마지막 암호 5 개를 다시 사용 하지 마십시오. 암호 기록 요구 사항에 의해 더 최근 암호를 다시 사용할 수 있더라도 공격자가 추측할 수 없는 항목을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p108">Don't reuse any of your last five passwords. Even though the password history requirement lets you reuse a more recent password, you should select something that the attacker can't guess.</span></span>
- <span data-ttu-id="1b417-148">온-프레미스 id가 Office 365에 페더레이션 되어 있는 경우 온-프레미스에 암호를 변경 해야 하며, 관리자에 게 해당 사용자의 손상을 알려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-148">If your on-premises identity is federated with Office 365, you must change your password on-premises, and then you must notify your administrator of the compromise.</span></span>

> [!TIP]
> <span data-ttu-id="1b417-p109">특히 관리 권한이 있는 계정에 대 한 손상을 방지 하기 위해 MFA (multi-factor Authentication)를 사용 하는 것이 좋습니다.  [여기](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6)에서 자세히 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p109">It is highly recommended that you enable Multi-Factor Authentication (MFA) in order to prevent compromise, especially for accounts with administrative privileges.  You can learn more [here](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).</span></span>

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a><span data-ttu-id="1b417-151">2 단계 의심 스러운 전자 메일 전달 주소 제거</span><span class="sxs-lookup"><span data-stu-id="1b417-151">Step 2 Remove suspicious email forwarding addresses</span></span>
1. <span data-ttu-id="1b417-152">**Office 365 관리 센터 > Active Users**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-152">Open the **Office 365 Admin Center > Active Users**.</span></span>
2. <span data-ttu-id="1b417-153">해당 하는 사용자 계정을 찾아 **메일 설정을**확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-153">Find the user account in question and expand **Mail Settings**.</span></span>
3. <span data-ttu-id="1b417-154">**전자 메일 전달**에 대해 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-154">For **Email forwarding**, click **Edit**.</span></span>
4. <span data-ttu-id="1b417-155">의심 스러운 전달 주소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-155">Remove any suspicious forwarding addresses.</span></span>

### <a name="step-3-disable-any-suspicious-inbox-rules"></a><span data-ttu-id="1b417-156">3 단계 의심 되는 받은 편지함 규칙을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="1b417-156">Step 3 Disable any suspicious inbox rules</span></span>
1. <span data-ttu-id="1b417-157">웹용 Outlook을 사용 하 여 사용자의 사서함에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-157">Sign in to the user's mailbox using Outlook on the web.</span></span>
2. <span data-ttu-id="1b417-158">톱니 바퀴 아이콘을 클릭 하 고 **메일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-158">Click on the gear icon and click **Mail**.</span></span>
3. <span data-ttu-id="1b417-159">**받은 편지함 및 비우기 규칙** 을 클릭 하 고 규칙을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-159">Click **Inbox and sweep rules** and review the rules.</span></span>
4. <span data-ttu-id="1b417-160">의심 스러운 규칙을 사용 하지 않도록 설정 하거나 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-160">Disable or delete suspicious rules.</span></span>

### <a name="step-4-unblock-the-user-from-sending-mail"></a><span data-ttu-id="1b417-161">4 단계 사용자의 메일 보내기 차단 해제</span><span class="sxs-lookup"><span data-stu-id="1b417-161">Step 4 Unblock the user from sending mail</span></span>
<span data-ttu-id="1b417-162">의심 스러운 사서함을 사용 하 여 스팸 전자 메일을 illicitly 경우 사서함이 메일을 보낼 수 없도록 차단 되었을 가능성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-162">If the suspected compromised mailbox was used illicitly to send spam email, it is likely that the mailbox has been blocked from sending mail.</span></span>
1. <span data-ttu-id="1b417-163">메일을 보내지 못하도록 사서함의 차단을 해제 하려면 [스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소 제거](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email )절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-163">To unblock a mailbox from sending mail, follow the procedures in [Removing a user, domain, or IP Address from a block list after sending spam email](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email ).</span></span>

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a><span data-ttu-id="1b417-164">5 단계 옵션: 로그인에서 사용자 계정 차단</span><span class="sxs-lookup"><span data-stu-id="1b417-164">Step 5 Optional: Block the user account from signing-in</span></span>
> [!IMPORTANT]
> <span data-ttu-id="1b417-165">액세스를 다시 사용 하도록 설정 하는 것이 안전 하다 고 확신할 때까지 의심 스러운 손상 된 계정을 로그인에서 차단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-165">You can block the suspected compromised account from signing-in until you believe it is safe to re-enable access.</span></span>

1. <span data-ttu-id="1b417-166">Office 365 관리 센터로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-166">Go to the Office 365 admin center.</span></span>
2. <span data-ttu-id="1b417-167">Office 365 관리 센터에서 **사용자** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-167">In the Office 365 admin center, select **Users**.</span></span>
3. <span data-ttu-id="1b417-168">차단할 직원을 선택한 다음 사용자 창의 **로그인 상태** 옆에 있는 **편집** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-168">Select the employee that you want to block, and then choose **Edit** next to **Sign-in status** in the user pane</span></span>
4. <span data-ttu-id="1b417-169">**로그인 상태** 창에서 **로그인 차단됨** 을 선택한 다음 **저장** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-169">On the **Sign-in status** pane, choose **Sign-in blocked** and then **Save**.</span></span> 
5. <span data-ttu-id="1b417-170">Office 365 관리 센터의 왼쪽 아래 탐색 창에서 **관리 센터** 를 확장 하 고 **Exchange**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-170">In the Office 365 admin center, in the lower-left navigation pane, expand **Admin Centers** and select **Exchange**.</span></span>
6. <span data-ttu-id="1b417-171">Exchange 관리 센터에서 **받는 사람 > 사서함**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-171">In the Exchange admin center, navigate to **Recipients > Mailboxes**.</span></span>
7. <span data-ttu-id="1b417-172">사용자를 선택 하 고 사용자 속성 페이지의 **모바일 장치**에서 **Exchange activcsync 사용 안 함을** 클릭 하 고 **장치용 OWA를 사용 하지 않도록 설정** 하 고 두 가지 모두에 대해 **예** 로 대답 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-172">Select the user, and on the user properties page, under **Mobile Devices**, click **Disable Exchange ActivcSync** and **Disable OWA for Devices** and answer **yes** to both.</span></span>
8. <span data-ttu-id="1b417-173">**전자 메일 연결**에서 **예**를 **사용 하지 않도록 설정** 하 고 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-173">Under **Email Connectivity**, **Disable** and answer **yes**.</span></span> 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a><span data-ttu-id="1b417-174">6 단계 (선택 사항): 모든 관리 역할 그룹에서 의심 스러운 계정 제거</span><span class="sxs-lookup"><span data-stu-id="1b417-174">Step 6 Optional: Remove the suspected compromised account from all administrative role groups</span></span>
> [!NOTE]
> <span data-ttu-id="1b417-175">계정을 보호 한 후에는 관리 역할 그룹 구성원을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-175">Administrative role group membership can be restored after the account has been secured.</span></span>

1. <span data-ttu-id="1b417-176">전역 관리자 계정을 사용 하 여 Office 365 관리 센터에 로그인 하 고 **활성 사용자**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-176">Sign in to the Office 365 Admin Center with a global administrator account and open **Active Users**.</span></span>
2. <span data-ttu-id="1b417-177">의심 스러운 계정의 손상 된 계정을 찾고 해당 계정에 할당 된 관리 역할이 있는지 수동으로 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-177">Find the suspected compromised account and manually check to see if there are any administrative roles assigned to the account.</span></span>
3. <span data-ttu-id="1b417-178">**Security & 준수 센터**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-178">Open the **Security & Compliance Center**.</span></span>
4. <span data-ttu-id="1b417-179">**사용 권한을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-179">Click **Permissions**.</span></span>
5. <span data-ttu-id="1b417-p110">역할 그룹을 수동으로 검토 하 여 의심 스러운 계정이 해당 계정의 구성원 인지 확인 합니다.  다음의 경우: 역할 그룹을 클릭 하 고 **역할 그룹 편집**을 클릭 합니다.  b. **선택한 구성원** 및 **편집** 을 클릭 하 여 역할 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p110">Manually review the role groups to see if the suspected compromised account is a member of any of them.  If it is:  a. Click the role group and click **Edit Role Group**.  b. Click **Chose Members** and **Edit** to remove the user from the role group.</span></span>
6. <span data-ttu-id="1b417-185">**Exchange 관리 센터** 열기</span><span class="sxs-lookup"><span data-stu-id="1b417-185">Open the **Exchange admin center**</span></span>
7. <span data-ttu-id="1b417-186">**사용 권한을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-186">Click **Permissions**.</span></span>
8. <span data-ttu-id="1b417-p111">역할 그룹을 수동으로 검토 하 여 의심 스러운 계정이 해당 계정의 구성원 인지 확인 합니다. If: a. 역할 그룹을 클릭 하 고 **편집**을 클릭 합니다.  b. **members** 섹션을 사용 하 여 역할 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p111">Manually review the role groups to see if the suspected compromised account is a member of any of them. If it is:  a. Click the role group and click **Edit**.  b. Use the **members** section to remove the user from the role group.</span></span>

### <a name="step-7-optional-additional-precautionary-steps"></a><span data-ttu-id="1b417-192">7 단계 (선택 사항): 추가 준비 단계</span><span class="sxs-lookup"><span data-stu-id="1b417-192">Step 7 Optional: Additional precautionary steps</span></span>
1. <span data-ttu-id="1b417-p112">보낸 항목을 확인 해야 합니다. 사용자의 계정이 손상 되었음을 대화 상대 목록에 알려야 할 수도 있습니다. 예를 들어 공격자는 다른 국가에서 나 필요한 비용으로 남겨진 것을 요구 하거나 공격자가 바이러스를 보내 컴퓨터를 가로챌 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p112">Make sure that you verify your sent items. You may have to inform people on your contacts list that your account was compromised. The attacker may have asked them for money, spoofing, for example, that you were stranded in a different country and needed money, or the attacker may send them a virus to also hijack their computers.</span></span>
2. <span data-ttu-id="1b417-p113">이 Exchange 계정을 대체 전자 메일 계정으로 사용한 다른 서비스가 손상 되었을 수 있습니다. 먼저 Office 365 구독에 대해 이러한 단계를 수행한 다음 다른 계정에 대해 이러한 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p113">Any other service that used this Exchange account as its alternative email account may have been compromised. First, perform these steps for your Office 365 subscription, and then perform these steps for your other accounts.</span></span>
3. <span data-ttu-id="1b417-198">전화 번호, 주소 등의 연락처 정보가 올바른지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-198">Make sure that your contact information, such as telephone numbers and addresses, is correct.</span></span>

## <a name="secure-office-365-like-a-cybersecurity-pro"></a><span data-ttu-id="1b417-199">cybersecurity pro와 같은 Office 365 보호</span><span class="sxs-lookup"><span data-stu-id="1b417-199">Secure Office 365 like a cybersecurity pro</span></span>
<span data-ttu-id="1b417-p114">Office 365 구독에는 데이터와 사용자를 보호 하는 데 사용할 수 있는 강력한 보안 기능 집합이 포함 되어 있습니다.  office 365 보안 로드맵: office 365 테 넌 트를 보호 하기 위한 Microsoft 권장 모범 사례를 구현 하는 데 [처음 30 일, 90 일 및 그 이상에 대 한 주요 우선 순위](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p114">Your Office 365 subscription comes with a powerful set of security capabilities that you can use to protect your data and your users.  Use the [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) to implement Microsoft recommended best practices for securing your Office 365 tenant.</span></span>
- <span data-ttu-id="1b417-p115">처음 30 일 이내에 수행 해야 하는 작업입니다.  이러한 설정은 즉시 영향을 미치며 사용자에 게 미치는 영향이 낮습니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p115">Tasks to accomplish in the first 30 days.  These have immediate affect and are low-impact to your users.</span></span>
- <span data-ttu-id="1b417-p116">90 일 이내에 수행할 작업입니다. 이러한 작업은 계획 하 고 구현 하는 데 다소 시간이 걸리고 보안 환경을 크게 향상 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p116">Tasks to accomplish in 90 days. These take a bit more time to plan and implement but greatly improve your security posture.</span></span>
- <span data-ttu-id="1b417-p117">90 일을 초과 합니다. 처음 90 일의 향상 된 기능 빌드는 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b417-p117">Beyond 90 days. These enhancements build in your first 90 days work.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b417-208">참고 항목:</span><span class="sxs-lookup"><span data-stu-id="1b417-208">See also:</span></span>
- [<span data-ttu-id="1b417-209">Office 365에 대한 보안 모범 사례</span><span class="sxs-lookup"><span data-stu-id="1b417-209">Security best practices for Office 365</span></span>](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [<span data-ttu-id="1b417-210">Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격 감지 및 재구성</span><span class="sxs-lookup"><span data-stu-id="1b417-210">Detect and Remediate Outlook Rules and Custom Forms Injections Attacks in Office 365</span></span>](detect-and-remediate-outlook-rules-forms-attack.md)
- [<span data-ttu-id="1b417-211">인터넷 범죄 불만 센터</span><span class="sxs-lookup"><span data-stu-id="1b417-211">Internet Crime Complaint Center</span></span>](http://www.ic3.gov/preventiontips.aspx)
- [<span data-ttu-id="1b417-212">증권 및 Exchange 위원회-"피싱" 사기</span><span class="sxs-lookup"><span data-stu-id="1b417-212">Securities and Exchange Commission - "Phishing" Fraud</span></span>](http://www.sec.gov/investor/pubs/phishing.htm)
