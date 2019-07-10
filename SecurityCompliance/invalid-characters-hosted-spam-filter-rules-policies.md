---
title: 스팸 필터 규칙 및 스팸 필터 정책에 잘못 된 문자 방지
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 09/24/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: 스팸 방지 구성에 잘못 된 문자가 있는 관리자가 보안 &amp; 및 준수 센터를 사용 하려고 할 때 문제를 해결 하는 데 도움이 되는 정보를 제공 합니다.
ms.openlocfilehash: c5ac6a262c80bc54a970dbef43684755e6d61e6a
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598964"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="bdc5a-103">스팸 필터 규칙 및 스팸 필터 정책에 잘못 된 문자 방지</span><span class="sxs-lookup"><span data-stu-id="bdc5a-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="bdc5a-104">이전에 Office 365 관리자는 EAC (Exchange 관리 센터)를 사용 하 여 스팸 필터 규칙 및 스팸 필터 정책을 설정 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-104">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange admin center (EAC).</span></span> <span data-ttu-id="bdc5a-105">이제 보안 &amp; 및 준수 센터를 사용 하 여 스팸 방지 구성을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-105">Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration.</span></span> <span data-ttu-id="bdc5a-106">다음 문자는 EAC에서 지원 되지만 보안 &amp; 및 준수 센터에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-106">The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="bdc5a-107">**잘못 된 문자:**</span><span class="sxs-lookup"><span data-stu-id="bdc5a-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="bdc5a-108">스팸 필터 규칙 또는 스팸 필터 정책에 잘못 된 문자가 포함 된 경우 다음과 같은 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="bdc5a-109">보안 &amp; 및 준수 센터에서 정책이 나 규칙을 찾지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="bdc5a-110">Windows PowerShell을 사용 하 여 규칙 또는 정책을 가져오려고 하면 오류가 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="bdc5a-111">정책이 나 설정이 제대로 실행 되지 않거나 예상 대로 수행 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="bdc5a-112">스팸 필터 정책 및 규칙에서 잘못 된 문자 제거</span><span class="sxs-lookup"><span data-stu-id="bdc5a-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="bdc5a-113">잘못 된 문자를 포함 하는 정책 및 규칙을 식별 한 후에는 Windows PowerShell cmdlet을 사용 하 여 이름을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="bdc5a-114">[원격 PowerShell을 사용 하 여 Exchange Online에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)합니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="bdc5a-115">스팸 필터 정책의 이름을 변경 하려면 다음과 같이 Get-hostedcontentfilterpolicy cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="bdc5a-116">스팸 필터 규칙의 이름을 변경 하려면 다음과 같이 Disable-hostedcontentfilterrule cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdc5a-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="bdc5a-117">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="bdc5a-117">For more information</span></span>

[<span data-ttu-id="bdc5a-118">보안 &amp; 및 준수 센터의 위협 관리</span><span class="sxs-lookup"><span data-stu-id="bdc5a-118">Threat management in the Security &amp; Compliance Center</span></span>](threat-management.md)
  
[<span data-ttu-id="bdc5a-119">Get-hostedcontentfilterpolicy</span><span class="sxs-lookup"><span data-stu-id="bdc5a-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[<span data-ttu-id="bdc5a-120">Disable-hostedcontentfilterrule</span><span class="sxs-lookup"><span data-stu-id="bdc5a-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
