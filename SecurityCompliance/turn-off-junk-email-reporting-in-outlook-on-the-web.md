---
title: 정크 메일 웹에 있는 Outlook에서 보고 해제
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: Office 365 관리자를 해제할 수 있습니다 기능 보고서 전자 메일을 사용자에 대 한 정크 메일로 합니다.
ms.openlocfilehash: 8ee5ff87408b80c443e4cf950ce49f624096becb
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272043"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="d2d5a-103">정크 메일 웹에 있는 Outlook에서 보고 해제</span><span class="sxs-lookup"><span data-stu-id="d2d5a-103">Turn off junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="d2d5a-p101">[보고서 정크 메일 및 피싱 메일 웹에 있는 outlook에서 ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)에서 설명한 대로 웹 정크 메일 옵션을 보고에 Outlook을 사용 하 여 분석을 위해 Microsoft에 정크, 피싱, 및 정크 메일이 아닌 메시지를 보낼 수 있습니다. 이러한 옵션을 사용 하 여 않으려면 관리자가 해제할 수 하 [Set-owamailboxpolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet을 통해.</span><span class="sxs-lookup"><span data-stu-id="d2d5a-p101">You can send junk, phishing, and not junk messages to Microsoft for analysis using the Outlook on the web junk email reporting options, as described in [Report junk email and phishing scams in Outlook on the web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). If you don't want to use these options,admins can turn them off via the [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d2d5a-106">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="d2d5a-106">What do you need to know before you begin?</span></span>
<span data-ttu-id="d2d5a-107"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="d2d5a-107"></span></span>

- <span data-ttu-id="d2d5a-108">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="d2d5a-108">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="d2d5a-p102">이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [Outlook Web App 사용 권한](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) 항목의 "Outlook Web App 사서함 정책" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d2d5a-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Outlook Web App mailbox policies" entry in the [Outlook Web App permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) topic.</span></span> 
    
- <span data-ttu-id="d2d5a-111">정크 메일 보고를 해제 하는 데 필요한 cmdlet를 실행 하기 전에 [Get-owamailboxpolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) 및 [Set-owamailboxpolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) 항목에 대 한 참조 정보를 검토 하려면 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2d5a-111">Before you run the cmdlets required to turn off junk email reporting, it might be helpful to review the reference information in the [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) and [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) topics.</span></span> 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a><span data-ttu-id="d2d5a-112">정크, 피싱 끄고 Microsoft에 보고를 정크 메일 아님</span><span class="sxs-lookup"><span data-stu-id="d2d5a-112">Turn off junk, phishing, and not junk reporting to Microsoft</span></span>
<span data-ttu-id="d2d5a-113"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="d2d5a-113"></span></span>

<span data-ttu-id="d2d5a-114">먼저, 다음 cmdlet을 실행하여 보고를 해제할 가상 디렉터리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2d5a-114">First, run the following cmdlet to get the virtual directories for which you want to turn off reporting:</span></span>
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

<span data-ttu-id="d2d5a-115">다음 cmdlet을 실행하여 Microsoft에 대한 정크 및 정크 아님 보고를 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="d2d5a-115">Next, run the following cmdlet to turn off junk and not junk reporting to Microsoft:</span></span>
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

<span data-ttu-id="d2d5a-116">예를 들어 다음 cmdlet은 가상 디렉터리 Contoso\owa에 대한 보고를 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="d2d5a-116">For example, the following cmdlet turns off reporting for virtual directory Contoso\owa:</span></span>
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="d2d5a-117">작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="d2d5a-117">How do you know this worked?</span></span>
<span data-ttu-id="d2d5a-118"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="d2d5a-118"></span></span>

<span data-ttu-id="d2d5a-p103">Get-owamailboxpolicy 매개 변수 값을 확인 하 고 웹에서 Outlook에 액세스 한 다음을 실행 하 고 정크, 피싱, 보고 및 정크 메일 아님 하는 옵션을 사용할 수 있는지 확인 합니다. 정크, 피싱으로 메시지를 표시할 수 및 정크 메일 아님으로 여전히 수 있지만 보고할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d2d5a-p103">Run Get-OWAMailboxPolicy to check the parameter values, and then access Outlook on the web and verify that the options to report junk, phishing, and not junk are not available. You'll still be able to mark messages as junk, phishing, and not junk, but you won't be able to report them.</span></span> 
  

