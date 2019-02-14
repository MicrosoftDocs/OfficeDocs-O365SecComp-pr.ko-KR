---
title: 찾기 및 악의적인 전자 메일 (Office 365 위협 인텔리전스) 지정 된 배달 하 게 조사
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection: M365-security-compliance
description: 위협 인텔리전스를 사용 하 여를 찾아 악의적인 전자 메일을 조사 하는 방법에 알아봅니다.
ms.openlocfilehash: c7492ccf2a7fa5d67b256264c6ed6fbdb06bcbc8
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995189"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a><span data-ttu-id="3b4a1-103">찾기 및 악의적인 전자 메일 (Office 365 위협 인텔리전스) 지정 된 배달 하 게 조사</span><span class="sxs-lookup"><span data-stu-id="3b4a1-103">Find and investigate malicious email that was delivered (Office 365 Threat Intelligence)</span></span>

<span data-ttu-id="3b4a1-p101">[Office 365 위협 인텔리전스](office-365-ti.md) 를 사용 하면 위험에 사용자를 배치 하 고 조직을 보호 하는 작업을 수행 하는 활동을 조사할 수 있습니다. 등 조직의 보안 팀의 일부인 경우 찾기 및 의심 스러운 전자 메일 메시지를 사용자에 게 배달 된를 조사할 수 있습니다. [위협 탐색기](get-started-with-ti.md#threat-explorer)를 사용 하 여이 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p101">[Office 365 Threat Intelligence](office-365-ti.md) enables you to investigate activities that put your users at risk and take action to protect your organization. For example, if you are part of your organization's security team, you can find and investigate suspicious email messages that were delivered to your users. You can do this by using [Threat Explorer](get-started-with-ti.md#threat-explorer).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3b4a1-p102">2019 년 2 월에에서 시작 하 고 향후 몇 개월 동안 롤아웃, Office 365 위협 인텔리전스는 되 고 Office 365 고급 위협 보호 계획 2, 추가 위협 보호 기능을 사용 합니다. 자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 고급 위협 Protection 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p102">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="3b4a1-109">시작 하기 전에...</span><span class="sxs-lookup"><span data-stu-id="3b4a1-109">Before you begin...</span></span>

<span data-ttu-id="3b4a1-110">다음 조건이 충족되었는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-110">Make sure that the following requirements are met:</span></span>
  
- <span data-ttu-id="3b4a1-111">조직이 [Office 365 위협 인텔리전스](office-365-ti.md) 및 [비즈니스를 위한 Office 365에서 사용자에 게 라이선스를 할당](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc)합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-111">Your organization has [Office 365 Threat Intelligence](office-365-ti.md) and [Assign licenses to users in Office 365 for business](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).</span></span>
    
- <span data-ttu-id="3b4a1-112">조직에 대 한 [office 365 감사 로깅](turn-audit-log-search-on-or-off.md) 기능이 켜 집니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-112">[Office 365 audit logging](turn-audit-log-search-on-or-off.md) is turned on for your organization.</span></span> 
    
- <span data-ttu-id="3b4a1-p103">조직에 스팸 방지, 맬웨어 방지, 피싱 방지 등에 대 한 정의 된 정책입니다. 참조 [관리 Office 365 보안에서 위협 &amp; 준수 센터](threat-management.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p103">Your organization has policies defined for anti-spam, anti-malware, anti-phishing, and so on. See [Threat management in the Office 365 Security &amp; Compliance Center](threat-management.md).</span></span>
    
- <span data-ttu-id="3b4a1-p104">사용자가 Office 365 전역 관리자, 있어야 하거나, 보안 관리자 또는 보안에서 할당 된 검색 및 삭제 역할 &amp; 준수 센터입니다. 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p104">You are an Office 365 global administrator, or you have either the Security Administrator or the Search and Purge role assigned in the Security &amp; Compliance Center. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="dealing-with-suspicious-emails"></a><span data-ttu-id="3b4a1-117">의심 스러운 전자 메일이 처리</span><span class="sxs-lookup"><span data-stu-id="3b4a1-117">Dealing with suspicious emails</span></span>

<span data-ttu-id="3b4a1-p105">악의적인 공격자가 자격 증명 시도 하는 사용자 및 phish에 게 메일을 보내는 하 고 기업 비밀 내용에 액세스할 수 있습니다! 이러한 문제를 방지 하기 위해 Exchange Online Protection 및 고급 위협 보호를 포함 하 여 Office 365에서 제공 하는 위협 보호 서비스를 사용 해야 합니다. 그러나 공격자 수 URL이 포함 된 사용자에 게 메일을 보낼 하 고 나중에 해당 URL 지점 (맬웨어 등) 악의적인 콘텐츠를 확인 하는 경우에 경우가 있습니다. 또는 있습니다 것을 느낄 수 너무 늦게 조직에서 사용자가 손상 된 하 고 해당 사용자가 손상 된 동안 공격자 계정을 사용 하는 해당 회사에 다른 사용자에 게 전자 메일을 보낼 수 있습니다. 이러한 시나리오 모두를 정리 하 고의 일부로 사용자의 받은 편지함에서 전자 메일 메시지를 제거 하는 것이 좋습니다. 다음과 같은 상황에서 검색 하 고 해당 전자 메일 메시지를 제거할 위협 탐색기를 활용할 수 있습니다!</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p105">Malicious attackers may be sending mail to your users to try and phish their credentials and gain access to your corporate secrets! In order to prevent this, you should use the threat protection services offered by Office 365, including Exchange Online Protection and Advanced Threat Protection. However, there are times when an attacker could send mail to your users containing a URL and only later on make that URL point to malicious content (malware, etc.). Alternatively, you may realize too late that a user in your organization has been compromised, and while that user was compromised, an attacker used that account to send email to other users in your company. As part of cleaning up both of these scenarios, you may want to remove email messages from user inboxes. In situations like these, you can leverage Threat Explorer to find and remove those email messages!</span></span>
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a><span data-ttu-id="3b4a1-124">찾기 및 지정 된 배달 하는 의심 스러운 전자 메일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-124">Find and delete suspicious email that was delivered</span></span>

> [!TIP]
> <span data-ttu-id="3b4a1-p106">[위협 탐색기](get-started-with-ti.md#threat-explorer) (탐색기 라고도 함) 강력한 보고서는 찾기 (영문) 및 메시지를 삭제 한 악의적인 전자 메일 보낸 사람의 IP 주소를 식별 하 또는 자세한 조사를 위해 인시던트를 시작 등의 여러 용도로 사용할 수 있습니다. 다음 절차는 탐색기를 사용 하 여 검색 하 고 악의적인 전자 메일 받는 사람 사서함에서 삭제할에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p106">[Threat Explorer](get-started-with-ti.md#threat-explorer) (also referred to as Explorer), is a powerful report that can serve multiple purposes, such as finding and deleting messages, identifying the IP address of a malicious email sender, or starting an incident for further investigation. The following procedure focuses on using Explorer to find and delete malicious email from recipients mailboxes.</span></span> 
  
1. <span data-ttu-id="3b4a1-p107">이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. 이렇게 하면 보안 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p107">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. This takes you to the Security &amp; Compliance Center.</span></span> 
    
2. <span data-ttu-id="3b4a1-129">왼쪽 탐색 영역에서 **위협 관리** 를 선택 \> **탐색기**입니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-129">In the left navigation, choose **Threat management** \> **Explorer**.</span></span>
    
3. <span data-ttu-id="3b4a1-130">보기 메뉴에서 **모든 전자 메일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-130">In the View menu, choose **All email**.</span></span><br/><span data-ttu-id="3b4a1-131">![보기 메뉴를 사용 하 여 전자 메일 및 콘텐츠 보고서 중 하나를 선택합니다](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)</span><span class="sxs-lookup"><span data-stu-id="3b4a1-131">![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)</span></span>
  
4. <span data-ttu-id="3b4a1-132">예: **배달 된**, **알 수 없는**또는 **정크에 게 배달**보고서에 표시 되는 레이블 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-132">Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.</span></span><br/><span data-ttu-id="3b4a1-133">![모든 전자 메일에 대 한 데이터를 표시 하는 위협 탐색기](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)</span><span class="sxs-lookup"><span data-stu-id="3b4a1-133">![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)</span></span><br/><span data-ttu-id="3b4a1-134">(조직에 대 한 전자 메일 메시지에서 작성 하는 작업에 따라 볼 수 있습니다 다른 레이블, 예: **차단 됨** 또는 **대체 되었습니다**.)</span><span class="sxs-lookup"><span data-stu-id="3b4a1-134">(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)</span></span>
    
5. <span data-ttu-id="3b4a1-135">보고서에서 사용자의 받은 편지함에는 결국 하는 전자 메일만 볼 수 있는 **전달 됨** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-135">In the report, choose **Delivered** to view only emails that ended up in users' inboxes.</span></span><br/><span data-ttu-id="3b4a1-136">!["정크에 전달"를 클릭 하면 보기에서 해당 데이터 제거](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)</span><span class="sxs-lookup"><span data-stu-id="3b4a1-136">![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)</span></span>
  
6. <span data-ttu-id="3b4a1-137">다음은 차트 아래 차트 아래에 있는 **전자 메일** 목록을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-137">Below the chart, review the **Email** list below the chart.</span></span><br/><span data-ttu-id="3b4a1-138">![다음은 차트 아래 검색 된 전자 메일 메시지의 목록 보기](media/dfb60590-1236-499d-97da-86c68621e2bc.png)</span><span class="sxs-lookup"><span data-stu-id="3b4a1-138">![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)</span></span>
  
7. <span data-ttu-id="3b4a1-p108">목록에서 해당 전자 메일 메시지에 대 한 자세한 정보를 보려면 항목을 선택 합니다. 예, 보낸사람, 받는 사람, 첨부 파일 및 기타 유사한 전자 메일 메시지에 대 한 정보를 보려면 제목줄 클릭 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p108">In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.</span></span><br/>![세부 정보 및 모든 첨부 파일을 포함 하 여 항목에 대 한 추가 정보를 볼 수 있습니다.](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. <span data-ttu-id="3b4a1-142">전자 메일 메시지에 대 한 정보를 검토 한 후 **+ 작업을**활성화 하려면 목록에서 하나 이상의 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-142">After viewing information about email messages, select one or more items in the list to activate **+ Actions**.</span></span>
    
9. <span data-ttu-id="3b4a1-p109">**+ 작업** 목록을 사용 하 여 항목 **삭제를 이동** 하는 등의 작업을 적용 합니다. 선택한 메시지를 받는 사람의 사서함에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b4a1-p109">Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.</span></span><br/><span data-ttu-id="3b4a1-145">![하나 이상의 전자 메일 메시지를 선택 하면 여러 사용 가능한 작업에서 선택할 수 있습니다.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)</span><span class="sxs-lookup"><span data-stu-id="3b4a1-145">![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="3b4a1-146">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3b4a1-146">Related topics</span></span>

[<span data-ttu-id="3b4a1-147">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="3b4a1-147">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="3b4a1-148">Office 365에서 위협으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="3b4a1-148">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="3b4a1-149">Office 365 고급 위협 보호에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="3b4a1-149">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

