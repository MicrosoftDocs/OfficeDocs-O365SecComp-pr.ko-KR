---
title: Office 365에서 보안 팁 사용 여부 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
ms.collection:
- M365-security-compliance
description: 전자 메일 메시지에서 보안 팁을 사용 하거나 사용 하지 않도록 설정 하는 방법을 Office 365 및 EOP 관리자에 게 알립니다.
ms.openlocfilehash: 9be9c4cd7fc8e94208aac2ad8812c93a3465f58b
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693437"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a><span data-ttu-id="76a21-103">Office 365에서 보안 팁 사용 여부 설정</span><span class="sxs-lookup"><span data-stu-id="76a21-103">Enable or disable safety tips in Office 365</span></span>

<span data-ttu-id="76a21-104">EOP (Exchange Online Protection)는 배달 되는 전자 메일 메시지에 보안 팁을 추가 하거나 스탬프 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-104">Exchange Online Protection (EOP) adds, or stamps, a safety tip to email messages that it delivers.</span></span> <span data-ttu-id="76a21-105">이러한 보안 팁을 통해 받는 사람에 게는 메시지가 안전한 지 확인 하 고, 메시지가 Office 365에서 스팸으로 표시 되는 경우, 메시지에 피싱 사기와 같은 의심 스러운 항목이 포함 되어 있거나 외부 이미지에 있는 경우 메시지를 빠르게 확인할 수 있습니다. 차단 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-105">These safety tips provide recipients with a quick, visual way to determine if a message is from a safe, verified sender, if the message has been marked as spam by Office 365, if the message contains something suspicious such as a phishing scam, or if external images have been blocked.</span></span> <span data-ttu-id="76a21-106">Office 365 및 EOP 독립 실행형 관리자는 스팸 정책 설정을 편집 하 여 Outlook 및 기타 데스크톱 전자 메일 클라이언트에서 보안 팁이 전자 메일에 표시 되지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-106">Office 365 and EOP-standalone admins can edit a spam policy setting to enable or disable safety tips from being displayed in email in Outlook and other desktop email clients.</span></span> 
  
<span data-ttu-id="76a21-107">Office 365에서는 조직에 기본적으로 보안 팁을 사용할 수 있으며, 스팸 및 피싱 공격을 방지 하는 데 도움이 되도록 사용 하도록 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-107">Office 365 enables safety tips by default for your organization and we recommend that you leave them enabled to help combat spam and phishing attacks.</span></span> <span data-ttu-id="76a21-108">웹용 Outlook에 대 한 보안 팁은 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-108">You can't disable safety tips for Outlook on the web.</span></span>
  
<span data-ttu-id="76a21-109">예제를 확인 하 고 보안 팁에 표시 되는 정보에 대 한 자세한 내용은 [Office 365의 전자 메일 메시지에 있는 보안 팁](safety-tips-in-office-365.md) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="76a21-109">To see examples and to learn about the information displayed in safety tips, see [Safety tips in email messages in Office 365.](safety-tips-in-office-365.md)</span></span>
  
<span data-ttu-id="76a21-110">이 항목의 내용:</span><span class="sxs-lookup"><span data-stu-id="76a21-110">In this topic:</span></span>
  
- [<span data-ttu-id="76a21-111">Office 365 보안 &amp; 및 준수 센터를 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="76a21-111">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [<span data-ttu-id="76a21-112">PowerShell을 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="76a21-112">To enable or disable safety tips by using PowerShell</span></span>](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="76a21-113">Office 365 보안 &amp; 및 준수 센터를 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="76a21-113">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>
<span data-ttu-id="76a21-114"><a name="SandCCsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="76a21-114"></span></span>

1. <span data-ttu-id="76a21-115">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-115">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="76a21-116">회사 또는 학교 계정으로 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-116">Sign in to Office 365 with your work or school account.</span></span>
    
3. <span data-ttu-id="76a21-117">**위협 관리** \> **정책을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-117">Choose **Threat Management** \> **Policy**.</span></span> 
    
4. <span data-ttu-id="76a21-118">**정책** 페이지에서 **스팸 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-118">On the **Policy** page, choose **Anti-Spam**.</span></span>
    
    ![이 스크린샷에서는 보안 &amp; 및 준수 센터의 스팸 방지 설정 페이지로 이동 하는 방법을 보여 줍니다.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. <span data-ttu-id="76a21-120">**스팸 방지 설정** 페이지에서 **사용자 지정** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-120">On the **Anti-spam settings** page choose the **Custom** tab.</span></span> 
    
    ![이 스크린샷에서는 보안 &amp; 및 준수 센터의 스팸 방지 설정 페이지에 있는 사용자 지정 탭의 위치를 보여 줍니다.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. <span data-ttu-id="76a21-122">필요한 경우 사용자 지정 **설정** 스위치를 선택 하 여 사용자 지정 설정을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-122">If necessary, choose the **Custom settings** switch to turn on custom settings.</span></span> <span data-ttu-id="76a21-123">사용자 지정 설정 스위치를 **Off**로 설정 하면 스팸 필터 정책을 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-123">If the custom settings switch is set to **Off**, you won't be able to modify spam filter policies.</span></span>
    
    ![이 스크린샷에는 해제 된 사용자 지정 스팸 방지 필터 정책 설정이 표시 됩니다.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. <span data-ttu-id="76a21-125">수정 하려는 스팸 정책을 확장 한 다음 **정책 편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-125">Expand the spam policy you want to modify and then choose **Edit policy**.</span></span> <span data-ttu-id="76a21-126">예를 들어 **기본 스팸 필터 정책**옆에 있는 아래쪽 화살표를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-126">For example, choose the down arrow next to **Default spam filter policy**.</span></span> <span data-ttu-id="76a21-127">또는 원하는 경우 **정책 추가**를 선택 하 여 새 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-127">Or, if you want, you can create a new policy by choosing **Add a policy**.</span></span>
    
8. <span data-ttu-id="76a21-128">**스팸 및 대량 작업을** 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-128">Expand **Spam and bulk** actions.</span></span> 
    
9. <span data-ttu-id="76a21-129">보안 팁을 사용 하도록 설정 하려면 **안전 팁**에서 설정 \*\*\*\* 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-129">To enable safety tips, under **Safety Tips**, check the **On** checkbox.</span></span> <span data-ttu-id="76a21-130">보안 팁을 사용 하지 않으려면 설정 \*\*\*\* 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-130">To disable safety tips, clear the **On** checkbox.</span></span> 
    
10. <span data-ttu-id="76a21-131">**저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-131">Choose **Save**.</span></span>
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a><span data-ttu-id="76a21-132">PowerShell을 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="76a21-132">To enable or disable safety tips by using PowerShell</span></span>
<span data-ttu-id="76a21-133"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="76a21-133"></span></span>

<span data-ttu-id="76a21-134">관리자는 Exchange Online PowerShell을 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-134">Admins can use Exchange Online PowerShell to enable or disable safety tips.</span></span> <span data-ttu-id="76a21-135">get-hostedcontentfilterpolicy cmdlet을 사용 하면 스팸 필터 정책에서 보안 팁을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-135">Use the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips in a spam filter policy.</span></span>
  
1. <span data-ttu-id="76a21-136">Exchange Online PowerShell에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-136">Connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="76a21-137">자세한 내용은 [Exchange Online PowerShell에 연결을](http://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76a21-137">For information, see [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="76a21-138">get-hostedcontentfilterpolicy cmdlet을 실행 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-138">Run the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips:</span></span>
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

<span data-ttu-id="76a21-139">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-139">Where:</span></span>
    
  -  <span data-ttu-id="76a21-140">*정책 이름은* 수정할 정책의 이름입니다 (예: **기본값**).</span><span class="sxs-lookup"><span data-stu-id="76a21-140">*policy name*  is the name of the policy you want to modify, for example **default**.</span></span>
    
  -  <span data-ttu-id="76a21-141">`$true`스팸 필터 정책에 대 한 보안 팁을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-141">`$true` enables safety tips for the spam filter policy.</span></span> 
    
  -  <span data-ttu-id="76a21-142">`$false`스팸 필터 정책에 대 한 보안 팁을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-142">`$false` disables safety tips for the spam filter policy.</span></span> 
    
    <span data-ttu-id="76a21-143">예를 들어 기본 스팸 필터 정책에 대 한 보안 팁을 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-143">For example, to disable safety tips for the default spam filter policy, run the following command:</span></span>
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

<span data-ttu-id="76a21-144">이 cmdlet에 대 한 자세한 내용은 [get-hostedcontentfilterpolicy](https://technet.microsoft.com/library/jj200781.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="76a21-144">For more information about this cmdlet, see [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span></span>
    
## <a name="still-need-help"></a><span data-ttu-id="76a21-145">여전히 도움이 필요하세요?</span><span class="sxs-lookup"><span data-stu-id="76a21-145">Still need help?</span></span>
<span data-ttu-id="76a21-146"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="76a21-146"></span></span>

<span data-ttu-id="76a21-147">보안 팁을 사용 하지 않도록 설정 했지만 여전히 전자 메일 메시지에 표시 하려면 다음 항목을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="76a21-147">If you disabled safety tips but are still seeing them in your email messages, check these things:</span></span>
  
- <span data-ttu-id="76a21-148">웹용 Outlook에 대 한 보안 팁은 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-148">You can't disable safety tips for Outlook on the web.</span></span> <span data-ttu-id="76a21-149">Outlook과 같은 다른 클라이언트에서 같은 전자 메일을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="76a21-149">Try viewing the same email in another client, such as Outlook.</span></span>
    
- <span data-ttu-id="76a21-150">보안 팁은 EOP를 사용 하는 모든 사용자에 대해 기본적으로 설정 되며, 여기에는 Office 365이 있는 모든 사람이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-150">Safety tips are on by default for every one who uses EOP, this includes everyone who has Office 365.</span></span> <span data-ttu-id="76a21-151">전자 메일에 보안 팁이 표시 되지 않도록 하려면이 항목에서 설명 하는 대로 스팸 필터 정책을 사용 하 여 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-151">In order to disable safety tips from showing up in email, you must disable them by using a spam filter policy as described in this topic.</span></span> <span data-ttu-id="76a21-152">정책을 설정한 후에는 사용 하도록 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="76a21-152">Once you've set up the policy, ensure that it is enabled.</span></span> <span data-ttu-id="76a21-153">스팸 필터 정책을 사용 하는 방법에 대 한 자세한 내용은 [스팸 필터 정책 구성을](https://technet.microsoft.com/library/jj200684.aspx)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76a21-153">For information on enabling spam filter policies, see [Configure your spam filter policies](https://technet.microsoft.com/library/jj200684.aspx).</span></span>
    
<span data-ttu-id="76a21-154">스팸 및 피싱 사기를 방지 하는 자세한 방법은 [Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76a21-154">For more ways to combat spam and phishing, see [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span></span>
  

