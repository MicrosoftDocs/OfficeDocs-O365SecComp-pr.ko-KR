---
title: 스팸 필터 규칙과 스팸 필터 정책에 잘못 된 문자가 방지
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: 자신의 스팸 방지 구성에 잘못 된 문자를 포함 하 고 문제를 실행 하는 보안을 사용 하려고 할 때 관리자에 게에 대 한 도움말을 제공 &amp; 준수 센터입니다.
ms.openlocfilehash: ca409b4daa7bec01417adb7cbfdfa2a128929e81
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018737"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="5d3df-103">필터 정책 스팸 및 스팸 필터 규칙의 잘못 된 문자를 방지</span><span class="sxs-lookup"><span data-stu-id="5d3df-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="5d3df-p101">이전에 Office 365 관리자를 설정 하 고 (EAC (Exchange 관리 센터)를 사용 하 여 스팸 필터 규칙 및 스팸 필터 정책을 구성 합니다. 보안을 사용 하는 이제 &amp; 준수 센터를 관리 하는 스팸 방지 구성 합니다. 다음 문자는 EAC에서 지원 되지만 보안에서 사용 하기 위해 지원 되지 않습니다 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-p101">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange Admin Center (EAC). Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration. The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="5d3df-107">**잘못 된 문자 수:**</span><span class="sxs-lookup"><span data-stu-id="5d3df-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="5d3df-108">스팸 필터 규칙 또는 스팸 필터 정책에 따라 잘못 된 문자 중 하나가 포함 하는 경우에 이러한 문제 중 일부 또는 전부를 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="5d3df-109">보안에서 정책 또는 규칙을 찾을 수 없습니다 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="5d3df-110">Windows PowerShell을 사용 하 여 규칙 또는 정책을 가져오려면 하려고 할 때 오류를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="5d3df-111">정책 또는 설정 하거나 하지 않으면 실행 예상 대로 수행을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="5d3df-112">스팸 필터 정책 및 규칙에서 잘못 된 문자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="5d3df-113">정책 및 잘못 된 문자를 포함 하는 규칙을 식별 한 후에 Windows PowerShell cmdlet을 사용 하 여 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="5d3df-114">[원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="5d3df-115">스팸 필터 정책의 이름을 변경 하려면 다음과 같이 Set-hostedcontentfilterpolicy cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="5d3df-116">스팸 필터 규칙의 이름을 변경 하려면 다음과 같이 Set-hostedcontentfilterrule cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3df-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="5d3df-117">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="5d3df-117">For more information</span></span>

[<span data-ttu-id="5d3df-118">보안에서 관리 위협 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="5d3df-118">Threat management in the Security &amp; Compliance Center</span></span>](threat-management.md)
  
[<span data-ttu-id="5d3df-119">Set-hostedcontentfilterpolicy</span><span class="sxs-lookup"><span data-stu-id="5d3df-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[<span data-ttu-id="5d3df-120">Set-hostedcontentfilterrule</span><span class="sxs-lookup"><span data-stu-id="5d3df-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
