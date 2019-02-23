---
title: Office 365에서 무제한 보관을 사용 하도록 설정-관리자 도움말
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: '관리자: 사용자에 게 Exchange Online 사서함에 대 한 무제한 저장소를 제공 하는 Office 365에서 자동 확장 보관을 사용 하도록 설정 하는 방법을 알아봅니다. 전체 조직 또는 특정 사용자만 자동 확장 보관을 사용 하도록 설정할 수 있습니다.'
ms.openlocfilehash: 39098ffc78d0379436cafb20e5a484ec0e7aa283
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215398"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a><span data-ttu-id="c1dc7-104">Office 365에서 무제한 보관을 사용 하도록 설정-관리자 도움말</span><span class="sxs-lookup"><span data-stu-id="c1dc7-104">Enable unlimited archiving in Office 365 - Admin Help</span></span>

<span data-ttu-id="c1dc7-p102">Office 365에서 Exchange Online 자동 확장 보관 기능을 사용 하 여 보관 사서함에 대해 무제한 저장 공간을 사용 하도록 설정할 수 있습니다. 자동 확장 보관이 켜져 있는 경우 저장소 제한에 도달 하면 추가 저장소 공간이 사용자의 보관 사서함에 자동으로 추가 됩니다. 따라서 사서함 저장소 용량 제한이 없습니다. 조직의 모든 사용자 또는 특정 사용자에 대해서만 자동 확장 보관을 설정할 수 있습니다. 자동 확장 보관에 대 한 자세한 내용은 [Office 365의 무제한 보관 개요](unlimited-archiving.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p102">You can use the Exchange Online auto-expanding archiving feature in Office 365 to enable unlimited storage space for archive mailboxes. When auto-expanding archiving is turned on, additional storage space is automatically added to a user's archive mailbox when it approaches the storage limit. The result is unlimited mailbox storage capacity. You can turn on auto-expanding archiving for everyone in your organization or just for specific users. For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="c1dc7-110">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="c1dc7-110">Before you begin</span></span>

- <span data-ttu-id="c1dc7-p103">전체 조직 또는 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하려면 Office 365 조직의 전역 관리자 이거나 Exchange Online 조직에서 조직 관리 역할 그룹의 구성원 이어야 합니다. 또는 특정 사용자에 대 한 자동 확장 보관을 사용 하도록 설정 하려면 Mail Recipients 역할이 할당 된 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p103">You have to be a global administrator in your Office 365 organization or a member of the Organization Management role group in your Exchange Online organization to enable auto-expanding archiving for your entire organization or for specific users. Alternately, you have to be a member of a role group that's assigned the Mail Recipients role to enable auto-expanding archiving for specific users.</span></span>
    
- <span data-ttu-id="c1dc7-p104">자동 확장 보관을 사용 하도록 설정 하려면 먼저 사용자의 보관 사서함을 사용 하도록 설정 해야 합니다. 보관 사서함을 사용 하도록 설정 하려면 사용자에 게 Exchange Online 계획 2 라이선스를 할당 받아야 합니다. 사용자에 게 exchange online 계획 1 라이선스가 할당 된 경우 해당 보관 사서함을 사용 하도록 설정 하기 위해 별도의 exchange online 보관 라이선스를 할당 해야 합니다. [Office 365 보안 &amp; 및 준수 센터에서 보관 사서함 사용](enable-archive-mailboxes.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p104">A user's archive mailbox has to be enabled before you can enable auto-expanding archiving. A user must be assigned an Exchange Online Plan 2 license to enable the archive mailbox. If a user is assigned an Exchange Online Plan 1 license, you would have to assign them a separate Exchange Online Archiving license to enable their archive mailbox. See [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md).</span></span>
    
- <span data-ttu-id="c1dc7-p105">또한 PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다. 조직의 모든 사용자에 대해 보관 사서함을 사용 하도록 설정 하는 데 사용할 수 있는 PowerShell 명령의 예는 [추가 정보](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p105">You can also use PowerShell to enable archive mailboxes. See the [More information](#more-information) section for an example of the PowerShell command that you can use to enable archive mailboxes for all users in your organization.</span></span> 
    
- <span data-ttu-id="c1dc7-p106">자동 확장 보관은 공유 사서함도 지원 합니다. 공유 사서함에 대 한 보관 함을 사용 하도록 설정 하려면 exchange online 계획 2 라이선스 또는 교환 라이선스가 있는 exchange online 계획 1 라이선스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p106">Auto-expanding archiving also supports shared mailboxes. To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span>
    
- <span data-ttu-id="c1dc7-p107">Exchange 관리 센터 또는 보안 &amp; 및 준수 센터를 사용 하 여 자동 확장 보관을 사용 하도록 설정할 수는 없습니다. Exchange Online PowerShell을 사용 해야 합니다. 원격 PowerShell을 사용 하 여 exchange online 조직에 연결 하려면 [exchange online PowerShell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p107">You can't use the Exchange admin center or the Security &amp; Compliance Center to enable auto-expanding archiving. You have to use Exchange Online PowerShell. To connect to your Exchange Online organization using remote PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a><span data-ttu-id="c1dc7-124">전체 조직에 대해 자동 확장 보관을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="c1dc7-124">Enable auto-expanding archiving for your entire organization</span></span>

<span data-ttu-id="c1dc7-p108">전체 조직에 대해 자동 확장 보관을 사용 하도록 설정할 수 있습니다. 이 기능을 켜면 기존 사용자 사서함과 새로 만든 사용자 사서함에 대해 자동 확장 보관이 사용 하도록 설정 됩니다. 새 사용자 사서함을 만들 때는 사용자의 기본 보관 사서함을 사용 하도록 설정 하 여 새 사용자 사서함에 대해 자동 확장 보관 기능을 사용할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p108">You can enable auto-expanding archiving for your entire organization. After you turn it on, auto-expanding archiving will be enabled for existing user mailboxes and for new user mailboxes that are created. When you create new user mailboxes, be sure to enable the user's main archive mailbox so the auto-expanding archiving feature will work for the new user mailbox.</span></span>
  
1. [<span data-ttu-id="c1dc7-128">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="c1dc7-128">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. <span data-ttu-id="c1dc7-129">Exchange Online PowerShell에서 다음 명령을 실행 하 여 전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-129">Run the following command in Exchange Online PowerShell to enable auto-expanding archiving for your entire organization.</span></span>

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a><span data-ttu-id="c1dc7-130">특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="c1dc7-130">Enable auto-expanding archiving for specific users</span></span>

<span data-ttu-id="c1dc7-p109">조직의 모든 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하는 대신 특정 사용자 에게만 사용 하도록 설정할 수 있습니다. 이 작업을 수행 하는 경우에는 일부 사용자 에게만 대용량 보관 저장소를 사용할 필요가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p109">Instead of enabling auto-expanding archiving for every user in your organization, you can just enable it for specific users. You might do this because only some users might have a need for a very large archive storage.</span></span>
  
<span data-ttu-id="c1dc7-133">특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하 고 보류 중이거나 Office 365 보존 정책에 할당 된 사용자의 사서함에 대해 다음 두 가지 구성 변경이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-133">When you enable auto-expanding archiving for a specific user and the user's mailbox in on hold or assigned to an Office 365 retention policy, the following two configurations changes are made:</span></span>
  
- <span data-ttu-id="c1dc7-p110">사용자의 기본 보관 사서함에 대 한 저장소 할당량을 10gb로 증가 시킵니다 (100에서 110 g b까지). 보관 경고 할당량은 10gb (90에서 100 gb까지)로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p110">The storage quota for the user's primary archive mailbox is increased by 10 GB (from 100 GB to 110 GB). The archive warning quota is also increased by 10 GB (from 90 GB to 100 GB).</span></span>
    
- <span data-ttu-id="c1dc7-p111">사용자의 기본 사서함에 있는 복구 가능한 항목 폴더의 저장소 할당량은 10gb로 증가 합니다 (100에서 110 g b까지). 복구 가능한 항목 경고 할당량은 10gb (90에서 100 gb까지)로 증가 합니다. 이러한 변경 내용은 사서함이 보류 되거나 Office 365 보존 정책에 할당 된 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p111">The storage quota for the Recoverable Items folder in the user's primary mailbox is increased by 10 GB (also from 100 GB to 110 GB). The Recoverable Items warning quota is also increased by 10 GB (from 90 GB to 100 GB). These changes are applicable only if the mailbox in on hold or assigned to an Office 365 retention policy.</span></span>
    
<span data-ttu-id="c1dc7-p112">이 추가 공간은 자동 확장 보관이 구축 되기 전에 발생할 수 있는 저장 문제를 방지 하기 위해 추가 됩니다. 이전 섹션에 설명 된 대로 전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 하면 추가 저장 공간이 추가 *되지 않습니다* .</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p112">This additional space is added to prevent any storage issues that may occur before the auto-expanding archive is provisioned. Note that additional storage space  *is not*  added when you enable auto-expanding archiving for your entire organization, as described in the previous section.</span></span> 
  
1. [<span data-ttu-id="c1dc7-141">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="c1dc7-141">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. <span data-ttu-id="c1dc7-p113">Exchange Online PowerShell에서 다음 명령을 실행 하 여 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 합니다. 앞에서 설명한 것 처럼 사용자의 보관 사서함 (기본 보관 함)을 사용 하도록 설정 해야 해당 사용자에 대해 자동 확장 보관을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p113">Run the following command in Exchange Online PowerShell to enable auto-expanding archiving for a specific user. As previously explained, the user's archive mailbox (main archive) must be enabled before you can turn on auto-expanding archiving for that user.</span></span>
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> <span data-ttu-id="c1dc7-p114">Exchange 하이브리드 배포에서는 기본 사서함이 온-프레미스이 고 보관 사서함이 클라우드 기반 인 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하기 위해 **AutoExpandingArchive** 명령을 사용할 수 없습니다. exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하려면 exchange Online PowerShell에서 **set-organizationconfig-AutoExpandingArchive** 명령을 실행 하 여 자동 확장 보관을 사용 하도록 설정 해야 합니다. 전체 조직 사용자의 기본 및 보관 사서함이 둘 다 클라우드 기반 인 경우에는 **AutoExpandingArchive** 명령을 사용 하 여 해당 특정 사용자에 대 한 자동 확장 보관을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p114">In an Exchange hybrid deployment, you can't use the **Enable-Mailbox -AutoExpandingArchive** command to enable auto-expanding archiving for specific a user whose primary mailbox is on premises and their archive mailbox is cloud-based. To enable auto-expanding archiving for cloud-based archive mailboxes in an Exchange hybrid deployment, you have to run the **Set-OrganizationConfig -AutoExpandingArchive** command in Exchange Online PowerShell to enable auto-expanding archiving for the entire organization. If a user's primary and archive mailboxes are both cloud-based, then you can use the **Enable-Mailbox -AutoExpandingArchive** command to enable auto-expanding archiving for that specific user.</span></span> 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a><span data-ttu-id="c1dc7-147">자동 확장 보관이 사용 되도록 설정 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="c1dc7-147">Verify that auto-expanding archiving is enabled</span></span>

<span data-ttu-id="c1dc7-148">조직에 대해 자동 확장 보관을 사용 하도록 설정 되어 있는지 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-148">To verify that auto-expanding archiving is enabled for your organization, run the following command in Exchange Online PowerShell.</span></span>

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

<span data-ttu-id="c1dc7-149">값은 조직 `True` 에 대해 자동 확장 보관을 사용 하도록 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-149">A value of  `True` indicates that auto-expanding archiving is enabled for the organization.</span></span> 
  
<span data-ttu-id="c1dc7-150">특정 사용자가 자동 확장 보관을 사용 하도록 설정 되어 있는지 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-150">To verify that auto-expanding archiving is enable for a specific user, run the following command in Exchange Online PowerShell.</span></span>
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
<span data-ttu-id="c1dc7-151">값은 사용자 `True` 에 대해 자동 확장 보관을 사용 하도록 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-151">A value of  `True` indicates that auto-expanding archiving is enabled for the user.</span></span> 
  
<span data-ttu-id="c1dc7-152">자동 확장 보관을 사용 하도록 설정한 후에는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-152">Keep the following things in mind after you enable auto-expanding archiving:</span></span>
  
- <span data-ttu-id="c1dc7-p115">**set-organizationconfig-AutoExpandingArchive** 명령을 실행 하 여 조직에 대해 자동 확장 보관을 사용 하도록 설정 하는 경우에는 개별 사서함에서 **enable-AutoExpandingArchive** 를 실행할 필요가 없습니다. **set-organizationconfig** cmdlet을 실행 하 여 조직에 대해 자동 확장 보관을 사용 하도록 설정 해도 사용자 사서함의 *AutoExpandingArchiveEnabled* 속성은로 `True`변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p115">If you run the **Set-OrganizationConfig -AutoExpandingArchive** command to enable auto-expanding archiving for your organization, you don't have to run the **Enable-Mailbox -AutoExpandingArchive** on individual mailboxes. Note that running the **Set-OrganizationConfig** cmdlet to enable auto-expanding archiving for your organization doesn't change the  *AutoExpandingArchiveEnabled*  property on user mailboxes to  `True`.</span></span>
    
- <span data-ttu-id="c1dc7-p116">마찬가지로 자동 확장 보관을 사용 하도록 설정 하면 *ArchiveQuota* 및 *ArchiveWarningQuota* 사서함 속성의 값이 변경 되지 않습니다. 실제로 사용자 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하 고 *AutoExpandingArchiveEnabled* `True`속성을로 설정 하면 *ArchiveQuota* 및 *ArchiveWarningQuota* 속성이 무시 됩니다. 다음은 사용자 사서함에 대해 자동 확장 보관을 사용 하도록 설정한 후 이러한 사서함 속성의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p116">Similarly, the values for the  *ArchiveQuota*  and  *ArchiveWarningQuota*  mailbox properties aren't changed when you enable auto-expanding archiving. In fact, when you enable auto-expanding archiving for a user mailbox and the  *AutoExpandingArchiveEnabled*  property is set to  `True`, the  *ArchiveQuota*  and  *ArchiveWarningQuota*  properties are just ignored. Here's an example of these mailbox properties after auto-expanding archiving is enabled for a user's mailbox.</span></span> 
    
    ![자동 확장 보관을 사용 하도록 설정한 후에는 ArchiveQuota 및 ArchiveWarningQuota 속성이 무시 됩니다.](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a><span data-ttu-id="c1dc7-159">추가 정보</span><span class="sxs-lookup"><span data-stu-id="c1dc7-159">More information</span></span>

- <span data-ttu-id="c1dc7-p117">또한 PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다. 예를 들어 Exchange Online PowerShell에서 다음 명령을 실행 하 여 보관 사서함이 아직 사용 하도록 설정 되지 않은 모든 사용자에 대해 보관 사서함을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p117">You can also use PowerShell to enable archive mailboxes. For example, you can run the following command in Exchange Online PowerShell to enable archive mailboxes for all users whose archive mailbox isn't already enabled.</span></span>

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- <span data-ttu-id="c1dc7-p118">조직 또는 특정 사용자에 대해 자동 확장 보관을 설정 하면 보관 사서함 (복구 가능한 항목 폴더 포함)이 90 GB에 도달할 때 보관 사서함이 자동 확장 아카이브로 변환 됩니다. 추가 저장 공간을 프로 비전 하는 데 최대 30 일이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p118">After you turn on auto-expanding archiving for your organization or for a specific user, an archive mailbox is converted to an auto-expanding archive when the archive mailbox (including the Recoverable Items folder) reaches 90 GB. It can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
- <span data-ttu-id="c1dc7-164">자동 확장 보관을 설정한 후에는 끌 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-164">After you turn on auto-expanding archiving, it can't be turned off.</span></span>
    
- <span data-ttu-id="c1dc7-p119">온-프레미스 기본 사서함이 있는 사용자의 경우 Exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대해 자동 확장 보관이 지원 됩니다. 그러나 클라우드 기반 보관 사서함에 대해 자동 확장 보관을 사용 하도록 설정한 후에는 온-프레미스 Exchange 조직으로 사서함을 다시 보관 하는 보드를 끌 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p119">Auto-expanding archiving is supported for cloud-based archive mailboxes in an Exchange hybrid deployment for users who have an on-premises primary mailbox. However, after auto-expanding archiving is enabled for a cloud-based archive mailbox, you can't off-board that archive mailbox back to the on-premises Exchange organization.</span></span>
    
- <span data-ttu-id="c1dc7-167">사용자가 보관 사서함의 추가 저장소 영역에 있는 항목에 액세스 하는 데 사용할 수 있는 outlook 클라이언트 목록은 [Office 365의 무제한 보관](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) 에 대 한 개요의 "자동 확장 된 보관 함 항목에 액세스 하기 위한 Outlook 요구 사항" 섹션을 참조 하세요. .</span><span class="sxs-lookup"><span data-stu-id="c1dc7-167">For a list of Outlook clients that users can use to access items in the additional storage area in their archive mailbox, see the "Outlook requirements for accessing items in an auto-expanded archive" section in [Overview of unlimited archiving in Office 365](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive).</span></span>
    
- <span data-ttu-id="c1dc7-p120">앞에서 설명한 것 처럼, **AutoExpandingArchive** 명령을 실행할 때 사용자의 기본 보관 사서함 및 사서함이 대기 중인 경우 복구 가능한 항목 폴더의 저장소 할당량에 10gb가 추가 됩니다. 이렇게 하면 자동 확장 된 저장소 공간이 프로 비전 될 때까지 (최대 30 일이 걸릴 수 있음) 추가 저장소가 제공 됩니다. **set-organizationconfig-AutoExpandingArchive** 을 실행 하 여 조직의 모든 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하면이 추가 저장소 공간이 추가 되지 않습니다. 전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 했지만 특정 사용자에 게 10gb의 추가 저장 공간을 추가 해야 하는 경우 해당 사서함에서 **AutoExpandingArchive** 명령을 실행할 수 있습니다. 자동 확장 보관이 이미 사용 하도록 설정 되었지만 추가 저장 공간이 사서함에 추가 된다는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc7-p120">As previously explained, 10 GB is added to the storage quota of the user's primary archive mailbox (and to the Recoverable Items folder if the mailbox is on hold) when you run the **Enable-Mailbox -AutoExpandingArchive** command. This provides additional storage until the auto-expanded storage space is provisioned (which can take up to 30 days). This additional storage space isn't added when you run the **Set-OrganizationConfig -AutoExpandingArchive** to enable auto-expanding archiving for all mailboxes in your organization. If you enabled auto-expanding archiving for the entire organization, but need to add the additional 10 GB of storage space for a specific user, you can run the **Enable-Mailbox -AutoExpandingArchive** command on that mailbox. Note that you will receive an error saying that auto-expanding archiving has already been enabled, but the additional storage space will be added to the mailbox.</span></span> 
