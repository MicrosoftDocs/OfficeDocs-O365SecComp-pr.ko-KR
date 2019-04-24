---
title: 웹용 Outlook에서 정크 메일 보고 해제
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
ms.collection:
- M365-security-compliance
description: Office 365 관리자는 사용자가 전자 메일을 정크 메일로 보고 하는 기능을 해제할 수 있습니다.
ms.openlocfilehash: f3e8a8cf837e7923d3c7241852ab2acd375492b8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264170"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="62402-103">웹용 Outlook에서 정크 메일 보고 해제</span><span class="sxs-lookup"><span data-stu-id="62402-103">Turn off junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="62402-104">웹용 outlook [의 정크 메일 및 피싱 사기 보고 ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)에 설명 된 대로, 웹용 outlook (이전의 outlook web App이 라고도 함) 정크 메일 보고 옵션을 사용 하 여 정크, 피싱 및 정크 메시지를 분석을 위해 Microsoft에 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62402-104">You can send junk, phishing, and not junk messages to Microsoft for analysis using the Outlook on the web (formerly known as Outlook Web App) junk email reporting options, as described in [Report junk email and phishing scams in Outlook on the web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md).</span></span> <span data-ttu-id="62402-105">이러한 옵션을 사용 하지 않으려는 경우 관리자는 [set-owamailboxpolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet을 통해이를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62402-105">If you don't want to use these options,admins can turn them off via the [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="62402-106">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="62402-106">What do you need to know before you begin?</span></span>
<span data-ttu-id="62402-107"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="62402-107"></span></span>

- <span data-ttu-id="62402-108">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="62402-108">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="62402-109">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="62402-109">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="62402-110">필요한 사용 권한을 확인 하려면 [웹 사용 권한](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) 항목의 outlook에서 "웹 사서함 정책의 outlook" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="62402-110">To see what permissions you need, see the "Outlook on the web mailbox policies" entry in the [Outlook on the web permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) topic.</span></span> 

- <span data-ttu-id="62402-111">Exchange Online PowerShell에 연결하려면 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="62402-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a><span data-ttu-id="62402-112">Microsoft에 대 한 정크 메일, 피싱 및 정크 메일 아님 보고 해제</span><span class="sxs-lookup"><span data-stu-id="62402-112">Turn off junk, phishing, and not junk reporting to Microsoft</span></span>
<span data-ttu-id="62402-113"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="62402-113"></span></span>

<span data-ttu-id="62402-114">먼저 다음 명령을 실행 하 여 웹 사서함 정책에서 사용 가능한 Outlook 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62402-114">First, run the following command to get the names of your available Outlook on the web mailbox policies:</span></span>
  
```
Get-OwaMailboxPolicy | Format-Table Name
```

<span data-ttu-id="62402-115">다음 구문을 사용 하 여 웹용 Outlook에서 정크 및 정크 메일 아님 보고를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62402-115">Next, use the following syntax to enable or disable junk and not junk reporting to Microsoft in Outlook on the web:</span></span>
  
```
Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
```

<span data-ttu-id="62402-116">다음은 기본 Outlook web app 사서함 정책에서 보고 기능을 해제 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="62402-116">This example turns off reporting in the default Outlook web app mailbox policy:</span></span>
  
```
Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
```

<span data-ttu-id="62402-117">구문과 매개 변수에 대 한 자세한 내용은 [set-owamailboxpolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) 및 [set-owamailboxpolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="62402-117">For detailed syntax and parameter information, see [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) and [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx).</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="62402-118">작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="62402-118">How do you know this worked?</span></span>
<span data-ttu-id="62402-119"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="62402-119"></span></span>

<span data-ttu-id="62402-120">**set-owamailboxpolicy** 를 실행 하 여 매개 변수 값을 확인 한 다음 웹에서 outlook을 열어 해당 사용자에 게 적용 되는 웹 사서함 정책을 사용 하는 outlook을 연 다음 정크, 피싱 및 정크 메일을 보고 하는 옵션을 사용할 수 없는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="62402-120">Run **Get-OWAMailboxPolicy** to check the parameter values, and then open Outlook on the web for an affected user (who has the Outlook on the web mailbox policy applied to them) and verify that the options to report junk, phishing, and not junk are not available.</span></span> <span data-ttu-id="62402-121">메시지를 정크 메일 이나 피싱이 아닌 메시지로 표시할 수는 있지만 보고할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="62402-121">You'll still be able to mark messages as junk, phishing, and not junk, but you won't be able to report them.</span></span> 
