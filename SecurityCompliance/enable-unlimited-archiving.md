---
title: Office 365-관리자 도움말 무제한 보관을 사용 하도록 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: '관리자를 위한: Exchange Online 사서함에 대 한 무제한으로 저장 된 사용자에 게 제공 하는 Office 365의 보관 자동 확장을 사용 하는 방법을 설명 합니다. 특정 사용자만 또는 전체 조직에 대 한 보관 자동 확장을 사용 하도록 설정할 수 있습니다.'
ms.openlocfilehash: 6dd49433a1692d3a0ba23af57e7e2d9544f8a2b1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532916"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a><span data-ttu-id="6130d-104">Office 365-관리자 도움말 무제한 보관을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="6130d-104">Enable unlimited archiving in Office 365 - Admin Help</span></span>

<span data-ttu-id="6130d-p102">보관 사서함에 대 한 제한 없는 저장 공간을 사용 하도록 설정 하려면 Office 365의 Exchange Online 자동 확장 보관 기능을 사용할 수 있습니다. 보관 자동 확장 기능이 켜져은 추가 저장 공간 저장 용량 제한에 도달 하는 경우 사용자의 보관 사서함에 자동으로 추가 됩니다. 저장 용량 제한 없는 사서함이 반환이 됩니다. 자동 확장 하면 조직에서 모든 사용자에 대 한 이나 특정 사용자만 보관 설정할 수 있습니다. 자동 확장 하는 방법에 대 한 자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조 보관 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6130d-p102">You can use the Exchange Online auto-expanding archiving feature in Office 365 to enable unlimited storage space for archive mailboxes. When auto-expanding archiving is turned on, additional storage space is automatically added to a user's archive mailbox when it approaches the storage limit. The result is unlimited mailbox storage capacity. You can turn on auto-expanding archiving for everyone in your organization or just for specific users. For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="6130d-110">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="6130d-110">Before you begin</span></span>

- <span data-ttu-id="6130d-p103">Office 365 조직 또는 조직 전체 또는 특정 사용자에 대해 보관 자동 확장을 사용 하 여 Exchange Online 조직에서 조직 관리 역할 그룹의 구성원에 전역 관리자 여야 해야 합니다. 또는 특정 사용자에 대 한 보관 자동 확장을 사용 하 여 편지 병합 받는 사람 역할에 할당 된 역할 그룹의 구성원 이어야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p103">You have to be a global administrator in your Office 365 organization or a member of the Organization Management role group in your Exchange Online organization to enable auto-expanding archiving for your entire organization or for specific users. Alternately, you have to be a member of a role group that's assigned the Mail Recipients role to enable auto-expanding archiving for specific users.</span></span>
    
- <span data-ttu-id="6130d-p104">사용자의 보관 사서함에 보관 자동 확장을 설정 하기 전에 사용할 수 있습니다. 사용자의 보관 사서함을 사용 하도록 설정 하려면 Exchange Online 계획 2 라이선스를 할당 해야 합니다. Exchange Online 계획 1 라이선스를 할당 하면 사용자는 자신의 보관 사서함을 사용 하도록 설정 하는 별도 Exchange Online 보관 라이선스가 할당 해야 합니다. 참조 [Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터](enable-archive-mailboxes.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p104">A user's archive mailbox has to be enabled before you can enable auto-expanding archiving. A user must be assigned an Exchange Online Plan 2 license to enable the archive mailbox. If a user is assigned an Exchange Online Plan 1 license, you would have to assign them a separate Exchange Online Archiving license to enable their archive mailbox. See [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md).</span></span>
    
- <span data-ttu-id="6130d-p105">PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정 하려면 수도 있습니다. 조직에서 모든 사용자에 대 한 보관 사서함을 사용 하도록 설정 하는 데 사용할 수 있는 PowerShell 명령의 예에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6130d-p105">You can also use PowerShell to enable archive mailboxes. See the [More information](#more-information) section for an example of the PowerShell command that you can use to enable archive mailboxes for all users in your organization.</span></span> 
    
- <span data-ttu-id="6130d-p106">또한 보관 자동 확장 공유 사서함을 지원 합니다. 공유 사서함에 대 한 보관을 사용 하려면 Exchange Online 계획 2 라이선스 또는 Exchange Online 보관 라이선스를 사용 하 여 Exchange Online 계획 1 라이선스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p106">Auto-expanding archiving also supports shared mailboxes. To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span>
    
- <span data-ttu-id="6130d-p107">Exchange 관리 센터 또는 보안을 사용할 수 없습니다 &amp; 준수 센터 보관 자동 확장을 사용 하도록 설정 합니다. Exchange Online PowerShell을 사용 해야 합니다. 원격 PowerShell을 사용 하 여 Exchange Online 조직에 연결할 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/p/?linkid=396554)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6130d-p107">You can't use the Exchange admin center or the Security &amp; Compliance Center to enable auto-expanding archiving. You have to use Exchange Online PowerShell. To connect to your Exchange Online organization using remote PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a><span data-ttu-id="6130d-124">전체 조직에 대 한 보관 자동 확장을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="6130d-124">Enable auto-expanding archiving for your entire organization</span></span>

<span data-ttu-id="6130d-p108">전체 조직에 대 한 보관 자동 확장을 사용 하도록 설정할 수 있습니다. 설정한 후 보관 자동을 확장 하면 사용할 수 있고 기존 사용자 사서함에 대 한 및 만들어지는 새 사용자 사서함에 대 한. 새 사용자 사서함을 만들 때에 새 사용자 사서함에 대 한 자동 확장 하는 보관 기능이 작동할 되므로 사용자의 기본 보관 사서함을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p108">You can enable auto-expanding archiving for your entire organization. After you turn it on, auto-expanding archiving will be enabled for existing user mailboxes and for new user mailboxes that are created. When you create new user mailboxes, be sure to enable the user's main archive mailbox so the auto-expanding archiving feature will work for the new user mailbox.</span></span>
  
1. [<span data-ttu-id="6130d-128">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="6130d-128">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. <span data-ttu-id="6130d-129">전체 조직에 대 한 보관 자동 확장을 사용 하는 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-129">Run the following command in Exchange Online PowerShell to enable auto-expanding archiving for your entire organization.</span></span>

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a><span data-ttu-id="6130d-130">특정 사용자에 대 한 보관 자동 확장을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="6130d-130">Enable auto-expanding archiving for specific users</span></span>

<span data-ttu-id="6130d-p109">조직에서 모든 사용자에 대 한 보관 자동 확장을 사용 하는 대신 특정 사용자에 대 한 것만 설정할 수 있습니다. 일부 사용자만 매우 큰 보관 저장소에 대 한 요구가 있을 수 있으므로이 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p109">Instead of enabling auto-expanding archiving for every user in your organization, you can just enable it for specific users. You might do this because only some users might have a need for a very large archive storage.</span></span>
  
<span data-ttu-id="6130d-133">특정 사용자에 대 한 보관 자동 확장을 사용 하는 경우는 다음과 같은 두 구성도 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-133">When you enable auto-expanding archiving for a specific user, the following two configurations changes are also made:</span></span>
  
- <span data-ttu-id="6130d-134">사용자의 기본 보관 사서함에 대 한 저장소 할당량은 (110 g B에 100GB)에서 10 g B 씩 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-134">The storage quota for the user's primary archive mailbox is increased by 10 GB (from 100 GB to 110 GB).</span></span>
    
- <span data-ttu-id="6130d-p110">사용자의 기본 사서함의 복구 가능한 항목 폴더에 대 한 저장소 할당량은 (도 110 g B에 100GB)에서 10 g B 씩 증가 합니다. 이 변경에 있는 사서함에서 보유 하는 경우에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p110">The storage quota for the Recoverable Items folder in the user's primary mailbox is increased by 10 GB (also from 100 GB to 110 GB). This change is applicable only if the mailbox in on hold.</span></span>
    
<span data-ttu-id="6130d-p111">이 추가 공간 자동 확장 보관 구축 하기 전에 발생할 수 있는 저장소 문제를 방지 하기 위해 추가 됩니다. Note 해당 추가 저장 공간이 *없는* 이전 섹션에서 설명한 것 처럼 전체 조직에 대 한 보관 자동 확장을 사용 하는 경우 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p111">This additional space is added to prevent any storage issues that may occur before the auto-expanding archive is provisioned. Note that additional storage space  *is not*  added when you enable auto-expanding archiving for your entire organization, as described in the previous section.</span></span> 
  
1. [<span data-ttu-id="6130d-139">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="6130d-139">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. <span data-ttu-id="6130d-p112">특정 사용자에 대 한 보관 자동 확장을 사용 하는 Exchange Online PowerShell에서 다음 명령을 실행 합니다. 앞에서 설명한 것 처럼 사용자의 보관 사서함 (기본 보관 함)를 사용 하려면 먼저 자동-을 확장 하면 해당 사용자에 대 한 보관 활성화 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p112">Run the following command in Exchange Online PowerShell to enable auto-expanding archiving for a specific user. As previously explained, the user's archive mailbox (main archive) must be enabled before you can turn on auto-expanding archiving for that user.</span></span>
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> <span data-ttu-id="6130d-p113">Exchange 하이브리드 배포에서 자동 확장 기본 사서함이 있는 온-프레미스 사용자를 특정에 대 한 보관을 사용 하도록 설정 하려면 **Enable-mailbox AutoExpandingArchive** 명령을 사용할 수 없습니다 및 클라우드 기반 보관 사서함은 합니다. 명령을 실행 하 여 **Set-organizationconfig AutoExpandingArchive** Exchange Online에 대 한 보관 자동 확장을 사용 하는 PowerShell 해야하는 Exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대 한 보관 자동 확장을 사용 하려면 전체 조직입니다. 사용자의 기본 보관 사서함이 클라우드 기반 모두 하는 경우 해당 특정 사용자에 대 한 보관 자동 확장을 사용 하도록 **Enable-mailbox AutoExpandingArchive** 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p113">In an Exchange hybrid deployment, you can't use the **Enable-Mailbox -AutoExpandingArchive** command to enable auto-expanding archiving for specific a user whose primary mailbox is on premises and their archive mailbox is cloud-based. To enable auto-expanding archiving for cloud-based archive mailboxes in an Exchange hybrid deployment, you have to run the **Set-OrganizationConfig -AutoExpandingArchive** command in Exchange Online PowerShell to enable auto-expanding archiving for the entire organization. If a user's primary and archive mailboxes are both cloud-based, then you can use the **Enable-Mailbox -AutoExpandingArchive** command to enable auto-expanding archiving for that specific user.</span></span> 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a><span data-ttu-id="6130d-145">보관 자동 확장을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-145">Verify that auto-expanding archiving is enabled</span></span>

<span data-ttu-id="6130d-146">조직에 대 한 보관 자동을 확장 하면가 사용 하도록 설정 되어있는지를 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-146">To verify that auto-expanding archiving is enabled for your organization, run the following command in Exchange Online PowerShell.</span></span>

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

<span data-ttu-id="6130d-147">값이 `True` 는 조직에 대 한 보관 자동 확장을 사용할지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-147">A value of  `True` indicates that auto-expanding archiving is enabled for the organization.</span></span> 
  
<span data-ttu-id="6130d-148">보관 자동을 확장 하면 특정 사용자에 대 한 사용 인지를 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-148">To verify that auto-expanding archiving is enable for a specific user, run the following command in Exchange Online PowerShell.</span></span>
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
<span data-ttu-id="6130d-149">값이 `True` 사용자에 대 한 보관 자동 확장을 사용할지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-149">A value of  `True` indicates that auto-expanding archiving is enabled for the user.</span></span> 
  
<span data-ttu-id="6130d-150">자동 확장 보관을 활성화 한 후 다음 사항에 주의 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-150">Keep the following things in mind after you enable auto-expanding archiving:</span></span>
  
- <span data-ttu-id="6130d-p114">조직에 대 한 보관 자동 확장을 사용 하도록 설정 하려면 **Set-organizationconfig AutoExpandingArchive** 명령을 실행 하는 경우에 개별 사서함에서 **Enable-mailbox AutoExpandingArchive** 를 실행할 필요가 없습니다. 해당 조직에 사용자 사서함에서 *AutoExpandingArchiveEnabled* 속성은 바뀌지 않습니다에 대 한 보관 자동 확장을 사용 하도록 설정 하려면 **Set-organizationconfig** cmdlet을 실행 하는 참고 `True`합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p114">If you run the **Set-OrganizationConfig -AutoExpandingArchive** command to enable auto-expanding archiving for your organization, you don't have to run the **Enable-Mailbox -AutoExpandingArchive** on individual mailboxes. Note that running the **Set-OrganizationConfig** cmdlet to enable auto-expanding archiving for your organization doesn't change the  *AutoExpandingArchiveEnabled*  property on user mailboxes to  `True`.</span></span>
    
- <span data-ttu-id="6130d-p115">마찬가지로, 보관 자동 확장을 사용 하는 경우 *ArchiveQuota* 및 *ArchiveWarningQuota* 사서함 속성에 대 한 값이 변경 되지 않습니다. 실제로 때 사용자 사서함에 대 한 보관 자동 확장을 사용 하 고 *AutoExpandingArchiveEnabled* 속성이로 설정 된 `True`, 방금 *ArchiveQuota* 및 *ArchiveWarningQuota* 속성은 무시 됩니다. 사용자의 사서함에 대 한 자동 확장 보관이 설정 된 후 이러한 사서함 속성의 예로 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p115">Similarly, the values for the  *ArchiveQuota*  and  *ArchiveWarningQuota*  mailbox properties aren't changed when you enable auto-expanding archiving. In fact, when you enable auto-expanding archiving for a user mailbox and the  *AutoExpandingArchiveEnabled*  property is set to  `True`, the  *ArchiveQuota*  and  *ArchiveWarningQuota*  properties are just ignored. Here's an example of these mailbox properties after auto-expanding archiving is enabled for a user's mailbox.</span></span> 
    
    ![자동 확장 보관을 활성화 한 후 ArchiveQuota 및 ArchiveWarningQuota 속성은 무시 합니다.](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a><span data-ttu-id="6130d-157">추가 정보</span><span class="sxs-lookup"><span data-stu-id="6130d-157">More information</span></span>

- <span data-ttu-id="6130d-p116">PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정 하려면 수도 있습니다. 예 있습니다 명령을 실행할 수는 다음 Exchange 온라인 보관 사서함 이미 설정 되지 않은 모든 사용자에 대 한 보관 사서함을 사용 하도록 설정 하는 PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p116">You can also use PowerShell to enable archive mailboxes. For example, you can run the following command in Exchange Online PowerShell to enable archive mailboxes for all users whose archive mailbox isn't already enabled.</span></span>

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- <span data-ttu-id="6130d-p117">자동 확장 특정 사용자 또는 조직에 대 한 보관을 설정한 후 (복구 가능한 항목 폴더 포함)의 보관 사서함에 90 g B에 도달 하면가 자동 확장 보관 보관 사서함 변환 됩니다. 프로 비전 할 추가 저장 공간에 대 한 최대 30 일 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p117">After you turn on auto-expanding archiving for your organization or for a specific user, an archive mailbox is converted to an auto-expanding archive when the archive mailbox (including the Recoverable Items folder) reaches 90 GB. It can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
- <span data-ttu-id="6130d-162">자동 확장 보관을 설정한 후 해당 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-162">After you turn on auto-expanding archiving, it can't be turned off.</span></span>
    
- <span data-ttu-id="6130d-p118">온-프레미스 기본 사서함을 가진 사용자에 대 한 Exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대 한 보관 자동 확장 지원 됩니다. 그러나 보관 자동 확장 클라우드 기반 보관 사서함에 대해 설정 된 후 하면 수는 없습니다 오프-보드 온-프레미스 Exchange 조직에 다시 보관 사서함에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p118">Auto-expanding archiving is supported for cloud-based archive mailboxes in an Exchange hybrid deployment for users who have an on-premises primary mailbox. However, after auto-expanding archiving is enabled for a cloud-based archive mailbox, you can't off-board that archive mailbox back to the on-premises Exchange organization.</span></span>
    
- <span data-ttu-id="6130d-165">사용자가 자신의 보관 사서함에 추가 저장소 영역에 있는 항목에 액세스 하는데 사용할 수 있는 Outlook 클라이언트의 목록, [Office 365의 보관 무제한의 개요 (영문)](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) 에서 "자동 확장 보관 위치에 있는 항목에 액세스할 수 있도록 Outlook의 요구 사항" 섹션을 참조 하십시오. .</span><span class="sxs-lookup"><span data-stu-id="6130d-165">For a list of Outlook clients that users can use to access items in the additional storage area in their archive mailbox, see the "Outlook requirements for accessing items in an auto-expanded archive" section in [Overview of unlimited archiving in Office 365](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive).</span></span>
    
- <span data-ttu-id="6130d-p119">이전에 설명, 사용자의 기본 보관 사서함의 저장소 할당량을 10GB 추가 됩니다 (하 고 복구 가능한 항목 폴더에는 사서함이 하는 경우 대기)으로 **Enable-mailbox AutoExpandingArchive** 명령을 실행 하면 됩니다. 이 자동 확장 된 저장 공간 (에 30 일 분까지 걸릴 수) 구축 될 때까지 추가 저장소를 제공 합니다. 조직에서 모든 사서함에 대 한 보관 자동 확장을 사용 하도록 설정 하려면 **Set-organizationconfig AutoExpandingArchive** 를 실행 하는 경우이 추가 저장 공간 추가 되지 않습니다. 전체 조직에 대 한 보관 자동 확장을 설정 하 고 특정 사용자에 대 한 저장 공간이 10GB 추가 추가 해야하는 해당 사서함에 **Enable-mailbox AutoExpandingArchive** 명령을 실행할 수 있습니다. 자동 확장 보관이 이미 설정 되었는지, 하지만 사서함에 추가할 추가 저장 공간 이라는 오류가 나타나면 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="6130d-p119">As previously explained, 10 GB is added to the storage quota of the user's primary archive mailbox (and to the Recoverable Items folder if the mailbox is on hold) when you run the **Enable-Mailbox -AutoExpandingArchive** command. This provides additional storage until the auto-expanded storage space is provisioned (which can take up to 30 days). This additional storage space isn't added when you run the **Set-OrganizationConfig -AutoExpandingArchive** to enable auto-expanding archiving for all mailboxes in your organization. If you enabled auto-expanding archiving for the entire organization, but need to add the additional 10 GB of storage space for a specific user, you can run the **Enable-Mailbox -AutoExpandingArchive** command on that mailbox. Note that you will receive an error saying that auto-expanding archiving has already been enabled, but the additional storage space will be added to the mailbox.</span></span> 
