---
title: 사서함을 소송 자료 보존으로 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: '사서함에 소송 보존을 적용 하 여 삭제 된 항목 및 수정 된 항목의 원본 버전을 비롯 한 모든 사서함 콘텐츠를 유지 합니다. '
ms.openlocfilehash: b2d2a60fddb51aa310d01a765c1ebbbf127ecd19
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296981"
---
# <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="9e2bc-103">사서함을 소송 자료 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="9e2bc-103">Place a mailbox on Litigation Hold</span></span>
 
<span data-ttu-id="9e2bc-p101">사서함에 소송 보존을 적용 하 여 삭제 된 항목 및 수정 된 항목의 원본 버전을 비롯 한 모든 사서함 콘텐츠를 유지 합니다. 사용자 사서함에 소송 보존을 적용 하면 사용자의 보관 사서함에 있는 콘텐츠 (사용 하도록 설정 된 경우)도 보존 됩니다. 삭제 되 고 수정 된 항목은 지정 된 기간 동안 또는 소송 보존에서 사서함을 제거할 때까지 보존 됩니다. 이러한 모든 사서함 항목은 원본 [위치 eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) 검색에서 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p101">Place a mailbox on Litigation Hold to preserve all mailbox content, including deleted items and original versions of modified items. When you place a user' mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also placed on hold. Deleted and modified items are preserved for a specified period, or until you remove the mailbox from Litigation Hold. All such mailbox items are returned in an [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) search.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9e2bc-p102">소송 보존은 사용자 사서함의 복구 가능한 항목 폴더에 있는 항목을 보존 합니다. 삭제 되거나 수정 된 항목의 수와 크기에 따라 사서함의 복구 가능한 항목 폴더 크기가 빠르게 증가할 수 있습니다. 복구 가능한 항목 폴더는 기본적으로 높은 할당량을 사용 하 여 구성 됩니다. Exchange Online에서 사서함을 소송 보존 상태로 설정 하면이 할당량이 자동으로 증가 합니다. Exchange Server 2013에서는 주 단위로 소송 보존 상태로 설정 된 사서함을 모니터링 하 여 복구 가능한 항목 할당량의 제한에 도달 하지 않았는지 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p102">Litigation Hold preserves items in the Recoverable Items folder in the user's mailbox. Depending on number and size of items deleted or modified, the size of the Recoverable Items folder of the mailbox may increase quickly. The Recoverable Items folder is configured with a high quota by default. In Exchange Online, this quota is automatically increased when you place a mailbox on Litigation Hold. In Exchange Server 2013, we recommend that you monitor mailboxes that are placed on Litigation Hold on a weekly basis to ensure they don't reach the limits of the Recoverable Items quotas.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9e2bc-113">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="9e2bc-113">What do you need to know before you begin?</span></span>
<span data-ttu-id="9e2bc-114"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="9e2bc-114"></span></span>

- <span data-ttu-id="9e2bc-115">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="9e2bc-115">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="9e2bc-116">소송 보존 설정이 적용 되려면 최대 60 분이 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-116">The Litigation Hold setting may take up to 60 minutes to take effect.</span></span>
    
- <span data-ttu-id="9e2bc-p103">이 절차를 수행 하려면 먼저 사용 권한을 할당 받아야 합니다. 필요한 사용 권한을 확인 하려면 [메시징 정책 및 규정 준수 권한](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) 항목의 "원본 위치 유지" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "In-Place Hold" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="9e2bc-p104">exchange online 사서함에 소송 보존을 적용 하려면 exchange online (요금제 2) 라이선스를 할당 받아야 합니다. 사서함에 Exchange online (요금제 1) 라이선스가 할당 되는 경우이를 보류 상태로 설정 하려면 별도의 exchange online 보관 라이선스를 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p104">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online (Plan 2) license. If a mailbox is assigned an Exchange Online (Plan 1) license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    
- <span data-ttu-id="9e2bc-p105">앞에서 설명한 것 처럼 사용자 사서함에 소송 보존을 적용 하면 사용자의 보관 사서함에 포함 된 콘텐츠도 보존 됩니다. Exchange 하이브리드 배포에서 온-프레미스 기본 사서함에 소송 보존을 적용 하면 클라우드 기반 보관 사서함 (사용 하도록 설정 된 경우)도 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p105">As previously explained, when you place a Litigation Hold on a user's mailbox, content in the user's archive mailbox is also placed on hold. If you place a Litigation Hold on an on-premises primary mailbox in an Exchange hybrid deployment, the cloud-based archive mailbox (if enabled) is also placed on hold.</span></span>
    
- <span data-ttu-id="9e2bc-p106">Exchange Online에서 사서함을 소송 보존 상태로 설정 하면 복구 가능한 항목 폴더에 대 한 할당량이 자동으로 100 GB로 증가 합니다. 이 폴더의 기본 크기는 30gb입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p106">In Exchange Online, the quota for the Recoverable Items folder is automatically increased to 100 GB when you place a mailbox on Litigation Hold. The default size of this folder is 30 GB.</span></span>
    
- <span data-ttu-id="9e2bc-p107">소송 보존은 삭제 된 항목을 보존 하 고 보존을 제거할 때까지 수정한 항목의 원래 버전도 보존 합니다. 원하는 경우 보존 기간을 지정 하 여 지정 된 기간 동안 사서함 항목을 보존할 수 있습니다. 보존 기간을 지정 하는 경우에는 메시지가 수신 되거나 사서함 항목이 만들어진 날짜부터 계산 됩니다. 지정 된 조건을 충족 하는 항목을 보존 하려면 원본 위치 유지를 사용 하 여 쿼리 기반 보존을 만듭니다. 자세한 내용은 원본 [위치 유지 만들기 또는 제거](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p107">Litigation Hold preserves deleted items and also preserves original versions of modified items until the hold is removed. You can optionally specify a hold duration, which preserves a mailbox item for the specified duration period. If you specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created. To preserve items that meet your specified criteria, use an In-Place Hold to create a query-based hold. For details, see [Create or Remove an In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span></span>
    
- <span data-ttu-id="9e2bc-p108">셸을 사용 하 여 exchange online 사서함을 보류 상태로 설정 하려면 exchange online PowerShell을 사용 해야 합니다. 자세한 내용은 [원격 PowerShell을 사용 하 여 Exchange Online에 연결](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p108">To use the Shell to place an Exchange Online mailbox on hold, you have to use Exchange Online PowerShell. For more information, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="9e2bc-p109">공용 폴더 사서함에 소송 보존을 설정 하는 것은 지원 되지 않습니다. 원본 위치 유지를 사용 하 여 공용 폴더를 보존 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p109">Placing a Litigation Hold on a public folder mailbox isn't supported. You have to use In-Place Hold to place a hold on public folders.</span></span>
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="9e2bc-134">EAC를 사용 하 여 사서함을 소송 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="9e2bc-134">Use the EAC to place a mailbox on Litigation Hold</span></span>
<span data-ttu-id="9e2bc-135"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="9e2bc-135"></span></span>

1. <span data-ttu-id="9e2bc-136">**받는 사람** \> **사서함**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-136">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="9e2bc-137">사용자 사서함 목록에서 소송 보존에 추가할 사서함을 클릭 한 다음 편집 아이콘](media/ITPro-EAC-EditIcon.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-137">In the list of user mailboxes, click the mailbox that you want to place on Litigation Hold, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif).</span></span>
    
3. <span data-ttu-id="9e2bc-138">사서함 속성 페이지에서 **사서함 기능을 클릭 합니다.**</span><span class="sxs-lookup"><span data-stu-id="9e2bc-138">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="9e2bc-139">**소송 보존: 사용 안 함**에서 **사용** 을 클릭 하 여 사서함을 소송 보존 상태로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-139">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span> 
    
5. <span data-ttu-id="9e2bc-140">**소송 보존** 페이지에서 다음 선택적 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-140">On the **Litigation Hold** page, enter the following optional information:</span></span> 
    
  - <span data-ttu-id="9e2bc-p110">**소송 보존 기간 (일)** 이 상자를 사용 하 여 사서함이 소송 보존 상태에 있을 때 사서함 항목이 보관 되는 기간을 지정 합니다. 기간은 사서함 항목을 받거나 만든 날짜 로부터 계산 됩니다. 이 상자를 비워 두면 항목이 무기한으로 또는 보존이 제거 될 때까지 유지 됩니다. 기간을 지정 하려면 days를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p110">**Litigation hold duration (days)** Use this box to specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span> 
    
  - <span data-ttu-id="9e2bc-p111">**참고 사항** 이 상자를 사용 하 여 사서함이 소송 보존 상태 인지를 사용자에 게 알립니다. 메모는 Outlook 2010 이상 버전을 사용 하는 경우 사용자의 사서함에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p111">**Note** Use this box to inform the user their mailbox is on Litigation Hold. The note will appear in the user's mailbox if they're using Outlook 2010 or later.</span></span> 
    
  - <span data-ttu-id="9e2bc-p112">**URL** 이 상자를 사용 하 여 소송 보존에 대 한 자세한 내용을 보려면 웹 사이트에 사용자를 안내 합니다. 이 URL은 사용자의 사서함에 Outlook 2010 이상 버전을 사용 하는 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p112">**URL** Use this box to direct the user to a website for more information about Litigation Hold. This URL appears in the user's mailbox if they are using Outlook 2010 or later.</span></span> 
    
6. <span data-ttu-id="9e2bc-149">**소송 보존** 페이지에서 **저장** 을 클릭 한 다음 사서함 속성 페이지에서 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-149">Click **Save** on the **Litigation Hold** page, and then click **Save** on the mailbox properties page.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a><span data-ttu-id="9e2bc-150">셸을 사용 하 여 사서함에 소송 보존을 무제한으로 설정</span><span class="sxs-lookup"><span data-stu-id="9e2bc-150">Use the Shell to place a mailbox on Litigation Hold indefinitely</span></span>
<span data-ttu-id="9e2bc-151"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="9e2bc-151"></span></span>

<span data-ttu-id="9e2bc-p113">이 예에서는 사서함 bsuneja@contoso.com에 소송 보존을 설정 합니다. 사서함의 항목은 무기한으로 또는 보류가 제거 될 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p113">This example places the mailbox bsuneja@contoso.com on Litigation Hold. Items in the mailbox are held indefinitely or until the hold is removed.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> <span data-ttu-id="9e2bc-154">일정 기간을 지정 하지 않고 사서함에 소송 보존을 적용 하면 _LitigationHoldDuration_ 속성 사서함의 값이로 `Unlimited`설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-154">When you place a mailbox on Litigation Hold indefinitely (by not specifying a duration period), the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a><span data-ttu-id="9e2bc-155">셸을 사용 하 여 사서함을 소송 보존 상태로 설정 하 고 지정 된 기간 동안 항목을 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-155">Use the Shell to place a mailbox on Litigation Hold and preserve items for a specified duration</span></span>
<span data-ttu-id="9e2bc-156"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="9e2bc-156"></span></span>

<span data-ttu-id="9e2bc-157">이 예에서는 사서함 bsuneja@contoso.com에 소송 보존을 설정 하 고 2555 일 (약 7 년) 동안 항목을 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-157">This example places the mailbox bsuneja@contoso.com on Litigation Hold and preserves items for 2555 days (approximately 7 years).</span></span> 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a><span data-ttu-id="9e2bc-158">셸을 사용 하 여 지정 된 기간 동안 모든 사서함을 소송 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="9e2bc-158">Use the Shell to place all mailboxes on Litigation Hold for a specified duration</span></span>
<span data-ttu-id="9e2bc-159"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="9e2bc-159"></span></span>

<span data-ttu-id="9e2bc-p114">조직에서 일정 기간 동안 모든 사서함 데이터를 보존 해야 할 수도 있습니다. 조직의 모든 사서함을 소송 보존으로 설정 하기 전에 다음을 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p114">Your organization may require that all mailbox data be preserved for a specific period of time. Before you place all mailboxes in an organization on Litigation Hold, consider the following:</span></span>
  
<span data-ttu-id="9e2bc-162">이 예에서는 1 년 (365 일) 동안 조직의 모든 사용자 사서함에 소송 보존을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-162">This example places all user mailboxes in the organization on Litigation Hold for one year (365 days).</span></span>
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

<span data-ttu-id="9e2bc-163">이 예에서는 [Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet을 사용 하 여 조직의 모든 사서함을 검색 하 고, 모든 사용자 사서함이 포함 된 받는 사람 필터를 지정 하 고, 사서함 목록을 [사서함](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet으로 파이프 하 여 소송 보존을 사용 하도록 설정 하 고, 보존 기간</span><span class="sxs-lookup"><span data-stu-id="9e2bc-163">The example uses the [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet to retrieve all mailboxes in the organization, specifies a recipient filter to include all user mailboxes, and then pipes the list of mailboxes to the [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet to enable the Litigation Hold and hold duration.</span></span> 
  
<span data-ttu-id="9e2bc-164">모든 사용자 사서함을 무기한 보존 상태로 설정 하려면 이전 명령을 실행 하 되 _LitigationHoldDuration_ 매개 변수는 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-164">To place all user mailboxes on an indefinite hold, run the previous command but don't include the  _LitigationHoldDuration_ parameter.</span></span> 
  
<span data-ttu-id="9e2bc-165">필터에 다른 받는 사람 속성을 사용 하 여 하나 이상의 사서함을 포함 하거나 제외 하는 방법에 대 한 예는 [추가 정보](#moreinfo.md) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-165">See the [More information](#moreinfo.md) section for examples of using other recipient properties in a filter to include or exclude one or more mailboxes.</span></span> 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a><span data-ttu-id="9e2bc-166">셸을 사용 하 여 사서함이 소송 보존 상태에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-166">Use the Shell to remove a mailbox from Litigation Hold</span></span>
<span data-ttu-id="9e2bc-167"><a name="sectionSection5"> </a></span><span class="sxs-lookup"><span data-stu-id="9e2bc-167"></span></span>

<span data-ttu-id="9e2bc-168">이 예에서는 사서함 bsuneja@contoso.com에서 소송 보존을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-168">This example removes the mailbox bsuneja@contoso.com from Litigation Hold.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

<span data-ttu-id="9e2bc-169">P</span><span class="sxs-lookup"><span data-stu-id="9e2bc-169">P</span></span>
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="9e2bc-170">작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="9e2bc-170">How do you know this worked?</span></span>
<span data-ttu-id="9e2bc-171"><a name="sectionSection6"> </a></span><span class="sxs-lookup"><span data-stu-id="9e2bc-171"></span></span>

<span data-ttu-id="9e2bc-172">사서함이 소송 보존 상태 인지 확인 하려면 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-172">To verify that you have successfully placed a mailbox on Litigation Hold, do the one of the following:</span></span>
  
- <span data-ttu-id="9e2bc-173">EAC에서:</span><span class="sxs-lookup"><span data-stu-id="9e2bc-173">In the EAC:</span></span>
    
1. <span data-ttu-id="9e2bc-174">**받는 사람** \> **사서함**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-174">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="9e2bc-175">사용자 사서함 목록에서 소송 보존 설정을 확인 하려는 사서함을 클릭 한 다음 편집 아이콘](media/ITPro-EAC-EditIcon.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-175">In the list of user mailboxes, click the mailbox that you want to verify Litigation Hold settings for, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif).</span></span>
    
3. <span data-ttu-id="9e2bc-176">사서함 속성 페이지에서 **사서함 기능을 클릭 합니다.**</span><span class="sxs-lookup"><span data-stu-id="9e2bc-176">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="9e2bc-177">**소송 보존**에서 보류가 사용 되도록 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-177">Under **Litigation hold**, verify that hold is enabled.</span></span>
    
5. <span data-ttu-id="9e2bc-p115">**세부 정보 보기** 를 클릭 하 여 사서함이 소송 보존 및 해당 담당자에 게 들어간 시기를 확인 합니다. 선택적 **소송 보존 기간 (일)**, **메모**및 **URL** 상자의 값을 확인 하거나 변경할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p115">Click **View details** to verify when the mailbox was placed on Litigation Hold and by whom. You can also verify or change the values in the optional **Litigation hold duration (days)**, **Note**, and **URL** boxes.</span></span> 
    
- <span data-ttu-id="9e2bc-180">셸에서 다음 명령 중 하나를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-180">In the Shell, run one of the following commands:</span></span>
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    <span data-ttu-id="9e2bc-181">또는</span><span class="sxs-lookup"><span data-stu-id="9e2bc-181">or</span></span>
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    <span data-ttu-id="9e2bc-182">사서함이 소송 보존 상태로 유지 되는 경우 _LitigationHoldDuration_ 속성 사서함의 값이로 `Unlimited`설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-182">If a mailbox is placed on Litigation Hold indefinitely, the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span>
    
## <a name="more-information"></a><span data-ttu-id="9e2bc-183">추가 정보</span><span class="sxs-lookup"><span data-stu-id="9e2bc-183">More information</span></span>
<span data-ttu-id="9e2bc-184"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="9e2bc-184"></span></span>

- <span data-ttu-id="9e2bc-185">조직에서 모든 사서함 데이터를 특정 기간 동안 보존 해야 하는 경우 조직의 모든 사서함을 소송 보존 상태로 설정 하기 전에 다음을 고려 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-185">If your organization requires that all mailbox data has to preserved for a specific period of time, consider the following before you place all mailboxes in an organization on Litigation Hold.</span></span>
    
  - <span data-ttu-id="9e2bc-p116">이전 명령을 사용 하 여 조직의 모든 사서함 (또는 지정 된 받는 사람 필터와 일치 하는 사서함의 하위 집합)을 유지 하는 경우 명령을 실행 하는 시점에 있는 사서함만 보류 됩니다. 나중에 새 사서함을 만드는 경우이 명령을 다시 실행 하 여 새 사서함을 보류 상태로 설정 해야 합니다. 새 사서함을 자주 만드는 경우에는 필요한 만큼 명령을 예약 된 작업으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p116">When you use the previous command to place a hold on all mailboxes in an organization (or a subset of mailboxes matching a specified recipient filter) only mailboxes that exist at the time that you run the command are placed on hold. If you create new mailboxes later, you have to run the command again to place the new mailboxes on hold. If you create new mailboxes often, you can run the command as a scheduled task as frequently as required.</span></span>
    
  - <span data-ttu-id="9e2bc-p117">모든 사서함을 소송 보존으로 두면 사서함 크기에 큰 영향을 줄 수 있습니다. Exchange Server 2013 조직에서 조직의 보존 요구 사항에 맞는 적절 한 저장소를 계획 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p117">Placing all mailboxes on Litigation Hold can significantly impact mailbox sizes. In an Exchange Server 2013 organization, plan for adequate storage to meet your organization's preservation requirements.</span></span>
    
  - <span data-ttu-id="9e2bc-p118">복구 가능한 항목 폴더에는 고유한 저장 제한이 있으므로 폴더의 항목이 사서함 저장 용량 한도를 초과 하지 않도록 합니다. 앞에서 설명한 것 처럼 오랫동안 사서함 데이터를 보존 하면 사용자 사서함에 복구 가능한 항목 폴더가 증가 하 게 됩니다. Exchange Online의 이러한 증가에 맞게 사서함을 소송 보존 상태로 설정 하면 복구 가능한 항목 폴더에 대 한 할당량이 자동으로 30gb에서 100 GB로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p118">The Recoverable Items folder has its own storage limit, so items in the folder don't count towards the mailbox storage limit. As previously explained, preserving mailbox data for a long period of time will result in growth of the Recoverable Items folder in a user's mailbox and archive. To accommodate for this increase in Exchange Online, the quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when you place a mailbox on Litigation Hold.</span></span> 
    
    <span data-ttu-id="9e2bc-p119">Exchange Server 2013에서는 복구 가능한 항목 폴더에 대 한 기본 저장 제한도 30gb입니다. 이 폴더의 크기를 주기적으로 모니터링 하 여 제한에 도달 하지 않았는지 확인 하는 것이 좋습니다. 자세한 내용은 [복구 가능한 항목 폴더](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p119">In Exchange Server 2013, the default storage limit for the Recoverable Items folder is also 30 GB. We recommend that you periodically monitor the size of this folder to ensure it doesn't reach the limit. For more information, see [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span></span>
    
- <span data-ttu-id="9e2bc-p120">모든 사서함에 대 한 보류를 설정 하는 이전 명령은 모든 사용자 사서함을 반환 하는 받는 사람 필터를 사용 합니다. 다른 받는 사람 속성을 사용 하 여 사서함 cmdlet을 파이프 하 여 해당 사서함에 소송 보존을 **설정할** 수 있는 특정 사서함 목록을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p120">The previous command to place a hold on all mailboxes uses a recipient filter that returns all user mailboxes. You can use other recipient properties to return a list of specific mailboxes that you can then pipe to the **Set-Mailbox** cmdlet to place a Litigation Hold on those mailboxes.</span></span> 
    
    <span data-ttu-id="9e2bc-p121">다음은 일반 사용자 또는 사서함 속성에 따라 사서함의 하위 집합을 반환 하기 위해 **get-Mailbox** 및 **Recipient** cmdlet을 사용 하는 몇 가지 예입니다. 이러한 예에서는 _customattributen_ 또는 _부서_와 같은 관련 사서함 속성이 채워져 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p121">Here are some examples of using the **Get-Mailbox** and **Get-Recipient** cmdlets to return a subset of mailboxes based on common user or mailbox properties. These examples assume that relevant mailbox properties (such as  _CustomAttributeN_ or  _Department_) have been populated.</span></span>
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    <span data-ttu-id="9e2bc-p122">필터에 다른 사용자 사서함 속성을 사용 하 여 사서함을 포함 하거나 제외할 수 있습니다. 자세한 내용은 [-Filter 매개 변수의 필터링 할 수 있는 속성](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-p122">You can use other user mailbox properties in a filter to include or exclude mailboxes. For details, see [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span></span>
    

