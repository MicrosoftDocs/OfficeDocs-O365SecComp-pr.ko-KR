---
title: Office 365 ATP 안전 하 게 보호 첨부 파일
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 08/03/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
description: 안전한 첨부 파일 기능이 전자 메일 첨부 파일의 클릭 시간 증명 정보를 제공 합니다. 조직 파일 악의적인 사용자 로부터 보호 하기 위해 사용 하 여 안전한 첨부 파일 보내기 또는 전자 메일을 받을 합니다.
ms.openlocfilehash: 0a28923bff8aa2cd987159edd3cad77ed42f80f4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533497"
---
# <a name="office-365-atp-safe-attachments"></a><span data-ttu-id="783ce-104">Office 365 ATP 안전 하 게 보호 첨부 파일</span><span class="sxs-lookup"><span data-stu-id="783ce-104">Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="783ce-p102">[ATP 안전한 링크](atp-safe-links.md)) (함께 ATP 안전한 첨부 파일에는 [Office 365 고급 위협 보호](office-365-atp.md) (ATP)의 일부입니다. ATP 안전한 첨부 파일 기능이 악의적인, 전자 메일 첨부 파일이 있는지 확인 하 고 조직을 보호 하는 작업을 수행 합니다. ATP 안전한 첨부 파일 기능이 Office 365 전역 또는 보안 관리자가 설정 된 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 에 따라 조직을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p102">ATP Safe Attachments (along with [ATP Safe Links](atp-safe-links.md)) is part of [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP). The ATP Safe Attachments feature checks to see if email attachments are malicious, and then takes action to protect your organization. The ATP Safe Attachments feature protects your organization according to [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) that are set by your Office 365 global or security administrators.</span></span> 
  
<span data-ttu-id="783ce-p103">늦은 년 3 월 2018에서 하 고 다음 여러 주 동안 부터는 ATP 보호 확장 되 SharePoint Online, OneDrive의 파일에 비즈니스 및 팀이 Microsoft에 대 한 합니다. 자세한 내용은, [SharePoint, OneDrive 및 팀이 Microsoft Office 365 고급 위협 보호](atp-for-spo-odb-and-teams.md)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p103">Beginning in late March 2018 and over the next several weeks, ATP protection is being extended to files in SharePoint Online, OneDrive for Business, and Microsoft Teams. To learn more, see [Office 365 Advanced Threat Protection for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>
       
## <a name="how-it-works"></a><span data-ttu-id="783ce-110">작업 방법</span><span class="sxs-lookup"><span data-stu-id="783ce-110">How it works</span></span>

<span data-ttu-id="783ce-p104">ATP 안전한 첨부 파일 기능이 조직의 사용자에 대 한 전자 메일 첨부 파일을 확인합니다. ATP 안전한 첨부 파일 정책이 적용 된 하 고 정책에서는 Office 365 수 있는 전자 메일에서 다루는 다른 사용자를 자신의 전자 메일 첨부 파일을 확인 하 고 ATP 안전한 첨부 파일 정책에 따라 적절 한 동작이 수행 됩니다. 정책에 정의 되는 방법에 따라 사용자를 몰라도 전혀 악의적인 파일 전송 되었는지 작업을 계속할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p104">The ATP Safe Attachments feature checks email attachments for people in your organization. When an ATP Safe Attachments policy is in place and someone covered by that policy views their email in Office 365, their email attachments are checked and appropriate actions are taken, based on your ATP Safe Attachments policies. Depending on how your policies are defined, people can continue working without ever knowing they were sent malicious files.</span></span>
  
<span data-ttu-id="783ce-114">회사에서 ATP 안전한 첨부 파일의 두 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-114">Here are two examples of ATP Safe Attachments at work.</span></span>
  
- <span data-ttu-id="783ce-p105">**예제 1: 첨부 파일을 전자 메일** Lee 첨부 파일이 포함 된 전자 메일 메시지를 받는 경우를 가정해 보겠습니다. 않은 Lee 수 있다는 사실을 여부 첨부 파일은 안전 또는 실제로 백화점 ㈜의 사용자 자격 증명을 훔쳐 하도록 설계 맬웨어를 포함 합니다. 백화점 ㈜의 조직에서 보안 관리자 며칠 전 ATP 안전한 첨부 파일 정책을 정의 합니다. ATP 안전한 첨부 파일 기능을 전자 메일 첨부 파일 열리고 Lee이를 받기 전에 가상 환경에서 테스트 됩니다. 첨부 파일 악성 코드가 포함 될를 확인 하는 경우 자동으로 제거 됩니다. 첨부 파일을 안전 하는 경우 Lee 클릭할 때 정상적으로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p105">**Example 1: Email attachment** Suppose that Lee receives an email message that has an attachment. It is not obvious to Lee whether that attachment is safe or actually contains malware designed to steal the Lee's user credentials. In Lee's organization, a security administrator defined an ATP Safe Attachments policy a few days ago. With the ATP Safe Attachments feature, the email attachment is opened and tested in a virtual environment before Lee receives it. If the attachment is determined to be malicious, it will be removed automatically. If the attachment is safe, it will open as expected when Lee clicks on it.</span></span> 
    
- <span data-ttu-id="783ce-p106">**예 2: SharePoint Online에서 파일** Jean 파일을 수신 하 고 SharePoint Online의 라이브러리로 업로드 한 경우를 가정해 보겠습니다. Jean 파일에 대 한 링크와 공유를 사용 하는 팀의 나머지는 파일을 실제로 악의적인 정확히 모르는 합니다. 놓기만 [ATP SharePoint, OneDrive 및 Microsoft 팀의](atp-for-spo-odb-and-teams.md) 악의적인 파일을 감지 하 고 되지 않도록 차단 합니다. 몇 일이 지난 후 문서를 여는데 Chris 이동 합니다. 이 파일은 다음과 같은 Chris 볼 수 있지만 Chris 열거나 악의적인 파일에서 Chris의 컴퓨터와 다른 사용자를 방지 하는 것을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p106">**Example 2: File in SharePoint Online** Suppose that Jean received a file and uploaded it into a library in SharePoint Online. Jean shares the link to the file with the rest of the team, not knowing that the file is actually malicious. Fortunately, [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) detects the malicious file and blocks it. A few days later, Chris goes to open the document. Although Chris can see the file is there, Chris cannot open or share it, which prevents Chris's computer and others from the malicious file.</span></span> 
    
<span data-ttu-id="783ce-p107">ATP 안전한 첨부 파일 정책은 특정 사용자 또는 조직 전체에서 그룹 또는 전체 도메인에 적용할 수 있습니다. 자세한 내용은 **[Office 365의 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)** 을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p107">ATP Safe Attachments policies can be applied to specific people or groups in your organization, or to your entire domain. To learn more, see **[Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md)**.</span></span> 
  
## <a name="how-to-get-atp-safe-attachments"></a><span data-ttu-id="783ce-128">ATP 안전한 첨부 파일을 얻는 방법</span><span class="sxs-lookup"><span data-stu-id="783ce-128">How to get ATP Safe Attachments</span></span>

<span data-ttu-id="783ce-p108">ATP 안전한 첨부 파일 기능에는 Office 365 Enterprise e 5에 포함 된 고급 위협 보호의 일부입니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 고급 위협 보호 추가 기능으로 구입할 수 있습니다. (전역 관리자는 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p108">The ATP Safe Attachments feature is part of Advanced Threat Protection, which is included in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Advanced Threat Protection can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span>
  
<span data-ttu-id="783ce-132">ATP 안전한 첨부 파일 기능을 적용 하는 경우:</span><span class="sxs-lookup"><span data-stu-id="783ce-132">The ATP Safe Attachments feature applies when:</span></span>
  
- <span data-ttu-id="783ce-p109">ATP 안전한 첨부 파일 정책은 설정 합니다. ( [Office 365의 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)참조).</span><span class="sxs-lookup"><span data-stu-id="783ce-p109">ATP Safe Attachments policies are set up. (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md).)</span></span>
    
- <span data-ttu-id="783ce-p110">사용자가 자신의 작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 됩니다. ( [Office 또는 Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)참조).</span><span class="sxs-lookup"><span data-stu-id="783ce-p110">Users have signed into Office 365 using their work or school account. (See [Sign in to Office or Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)</span></span>
    
## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a><span data-ttu-id="783ce-137">ATP 안전한 첨부 파일 보호 전체에서 인지 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="783ce-137">How to know if ATP Safe Attachments protection is in place</span></span>

 <span data-ttu-id="783ce-138">원본 위치에 있는 것으로 ATP 안전한 첨부 파일 보호에 대 한 순서로 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 정의 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-138">[ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) must be defined in order for ATP Safe Attachments protection to be in place.</span></span> 
  
<span data-ttu-id="783ce-139">서비스가 작동 하는 방법을 보려면 하나 좋은 방법은 [고급 위협 보호에 대 한 보고서를 확인](view-reports-for-atp.md)하 여는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-139">One good way to see how the service is working is by [viewing reports for Advanced Threat Protection](view-reports-for-atp.md).</span></span>
  
<span data-ttu-id="783ce-p111">또한 다음 표에서 일부 예제 시나리오에 설명 합니다. 모든이 경우에는 조직에는 고급 위협 보호를 포함 하는 Office 365 Enterprise E5 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p111">In addition, the following table describes some example scenarios. In all of these cases, we assume the organization has Office 365 Enterprise E5, which includes Advanced Threat Protection.</span></span>
  
|<span data-ttu-id="783ce-142">**시나리오 예**</span><span class="sxs-lookup"><span data-stu-id="783ce-142">**Example scenario**</span></span>|<span data-ttu-id="783ce-143">**ATP 안전한 첨부 파일 보호는이 경우에 적용 여부**</span><span class="sxs-lookup"><span data-stu-id="783ce-143">**Does ATP Safe Attachments protection apply in this case?**</span></span>|
|:-----|:-----|
|<span data-ttu-id="783ce-144">Pat의 조직에 Office 365 Enterprise E5, 있지만 아무도 정의 된 모든 정책을 ATP 안전한 첨부 파일에 대 한 아직 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-144">Pat's organization has Office 365 Enterprise E5, but no one has defined any policies for ATP Safe Attachments yet.</span></span>  <br/> |<span data-ttu-id="783ce-p112">아니요. 기능을 사용할 수 있지만 적어도 하나의 ATP 안전한 첨부 파일 정책이 원본 위치에 있는 것으로 ATP 안전한 첨부 파일 보호에 대 한 순서로 정의 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p112">No. Although the feature is available, at least one ATP Safe Attachments policy must be defined in order for ATP Safe Attachments protection to be in place.</span></span>  <br/> |
|<span data-ttu-id="783ce-p113">Lee contoso 영업 부서의 직원입니다. 백화점 ㈜의 조직에 재무 직원 들의 경우에 적용 되는 위치에는 ATP 안전한 첨부 파일 정책이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p113">Lee is an employee in the sales department at Contoso. Lee's organization has an ATP Safe Attachments policy in place that applies to finance employees only.</span></span>  <br/> |<span data-ttu-id="783ce-p114">아니요. 이 경우 finance 직원 ATP 안전한 첨부 파일 보호 떨어지기 않지만 다른 직원, 영업 부서를 포함 하 여 이러한 그룹을 포함 하는 정책 정의 된 때까지 하지 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p114">No. In this case, finance employees would have ATP Safe Attachments protection, but other employees, including the sales department, would not until policies that include those groups are defined.</span></span>  <br/> |
|<span data-ttu-id="783ce-p115">어제, Jean의 조직에서 Office 365 관리자가 모든 직원에 게 적용 되는 ATP 안전한 첨부 파일 정책을 설정 합니다. 지금 바로 이전 Jean 첨부 파일이 포함 된 전자 메일 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p115">Yesterday, an Office 365 administrator at Jean's organization set up an ATP Safe Attachments policy that applies to all employees. Earlier today, Jean received an email message that includes an attachment.</span></span>  <br/> |<span data-ttu-id="783ce-p116">예입니다. 이 예제에서는 Jean 라이선스 고급 위협 보호를 위한 있으며 Jean를 포함 하는 ATP 안전한 첨부 파일 정책이 정의 되었습니다. 일반적으로 데이터 센터; 적용 하려면 새 정책에 대 한 약 30 분 걸리는 하루에이 경우을 통과 하므로 정책을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p116">Yes. In this example, Jean has a license for Advanced Threat Protection, and an ATP Safe Attachments policy that includes Jean has been defined. It typically takes about 30 minutes for a new policy to take effect across datacenters; since a day has passed in this case, the policy should be in effect.</span></span>  <br/> |
|<span data-ttu-id="783ce-p117">Chris의 조직에는 조직에서 모든 사용자에 대 한 전체 ATP 안전한 첨부 파일 정책을 사용 하 여 Office 365 Enterprise e 5에 있습니다. Chris 첨부 파일, 있으며 조직 외부에 있는 다른 사용자에 게 메시지를 전달 하는 전자 메일을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p117">Chris's organization has Office 365 Enterprise E5 with ATP Safe Attachments policies in place for everyone in the organization. Chris receives an email that has an attachment, and forwards the message to others who are outside the organization.</span></span>  <br/> |<span data-ttu-id="783ce-p118">ATP 안전한 첨부 파일 보호 Chris 받는 메시지에 대 한 마련 되었습니다. 받는 사람의 조직 전체에서 ATP 안전한 첨부 파일 정책 권한도, 하는 경우 다음 Chris 전달 된 메시지 것 해당 정책의 영향을 받습니다 전달 된 메시지가 도착 했을 때입니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p118">ATP Safe Attachments protection is in place for messages that Chris receives. If the recipients' organizations also have ATP Safe Attachments policies in place, then the message that Chris forwards would be subject to those policies when the forwarded message arrives.</span></span>  <br/> |
|<span data-ttu-id="783ce-p119">자원이 조직 장소에 ATP 안전한 첨부 파일 정책 있으며 [SharePoint, OneDrive 및 Microsoft 팀의 ATP](atp-for-spo-odb-and-teams.md) 설정 되었는지 합니다. 자원이는 SharePoint Online에서 모든 파일 검사 된를 열거나 다운로드 안전 되었다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="783ce-p119">Jamie's organization has ATP Safe Attachments policies in place, and [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) has been turned on. Jamie assumes that every file in SharePoint Online has been scanned and is safe to open or download.  </span></span><br/> |<span data-ttu-id="783ce-p120">ATP 안전한 첨부 파일 보호, 정의 된 정책에 따라 전체에는 그러나 모든 단일 파일 SharePoint Online, 회사 또는 Microsoft 팀의 비즈니스용 OneDrive의 검색은이 아닙니다. (자세한 내용은 참조 [SharePoint, OneDrive 및 Microsoft 팀의 ATP](atp-for-spo-odb-and-teams.md).)</span><span class="sxs-lookup"><span data-stu-id="783ce-p120">ATP Safe Attachments protection is in place according to the policies that are defined; however, this does not mean that every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams is scanned. (To learn more, see [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md).)  </span></span><br/> |
   
## <a name="submitting-files-for-malware-analysis"></a><span data-ttu-id="783ce-164">맬웨어 분석을 위해 파일 전송</span><span class="sxs-lookup"><span data-stu-id="783ce-164">Submitting files for malware analysis</span></span>

<span data-ttu-id="783ce-165">분석 하는 Microsoft를 요청 하려는 파일을 받은 경우 [제출을 맬웨어 분석을 위해 파일을](https://aka.ms/wdsi/submit)참고 하십시오.</span><span class="sxs-lookup"><span data-stu-id="783ce-165">If you receive a file that you want to ask Microsoft to analyze, visit [Submit a file for malware analysis](https://aka.ms/wdsi/submit).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="783ce-166">관련 항목</span><span class="sxs-lookup"><span data-stu-id="783ce-166">Related topics</span></span>

[<span data-ttu-id="783ce-167">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="783ce-167">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="783ce-168">Office 365의 ATP 안전한 첨부 파일 정책 설정</span><span class="sxs-lookup"><span data-stu-id="783ce-168">Set up ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
  
[<span data-ttu-id="783ce-169">SharePoint, OneDrive 및 Microsoft 팀의 ATP</span><span class="sxs-lookup"><span data-stu-id="783ce-169">ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](atp-for-spo-odb-and-teams.md)
  
[<span data-ttu-id="783ce-170">Office 365의에서 ATP 안전 하 게 보호 링크</span><span class="sxs-lookup"><span data-stu-id="783ce-170">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="783ce-171">Office 365의 ATP 피싱 방지 기능</span><span class="sxs-lookup"><span data-stu-id="783ce-171">ATP anti-phishing capabilities in Office 365</span></span>](atp-anti-phishing.md)
  
[<span data-ttu-id="783ce-172">고급 위협 보호에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="783ce-172">View the reports for Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

