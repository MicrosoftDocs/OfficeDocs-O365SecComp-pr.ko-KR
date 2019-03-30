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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: '관리자: 사용자에 게 Exchange Online 사서함에 대 한 무제한 저장소를 제공 하는 Office 365에서 자동 확장 보관을 사용 하도록 설정 하는 방법을 알아봅니다. 전체 조직 또는 특정 사용자만 자동 확장 보관을 사용 하도록 설정할 수 있습니다.'
ms.openlocfilehash: e41ebc0605b7e6ce2178791de27421a82e2b6cf6
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000851"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a><span data-ttu-id="47504-104">Office 365에서 무제한 보관을 사용 하도록 설정-관리자 도움말</span><span class="sxs-lookup"><span data-stu-id="47504-104">Enable unlimited archiving in Office 365 - Admin Help</span></span>

<span data-ttu-id="47504-105">Office 365에서 Exchange Online 자동 확장 보관 기능을 사용 하 여 보관 사서함에 대해 무제한 저장 공간을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-105">You can use the Exchange Online auto-expanding archiving feature in Office 365 to enable unlimited storage space for archive mailboxes.</span></span> <span data-ttu-id="47504-106">자동 확장 보관이 켜져 있는 경우 저장소 제한에 도달 하면 추가 저장소 공간이 사용자의 보관 사서함에 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-106">When auto-expanding archiving is turned on, additional storage space is automatically added to a user's archive mailbox when it approaches the storage limit.</span></span> <span data-ttu-id="47504-107">따라서 사서함 저장소 용량 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-107">The result is unlimited mailbox storage capacity.</span></span> <span data-ttu-id="47504-108">조직의 모든 사용자 또는 특정 사용자에 대해서만 자동 확장 보관을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-108">You can turn on auto-expanding archiving for everyone in your organization or just for specific users.</span></span> <span data-ttu-id="47504-109">자동 확장 보관에 대 한 자세한 내용은 [Office 365의 무제한 보관 개요](unlimited-archiving.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47504-109">For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="47504-110">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="47504-110">Before you begin</span></span>

- <span data-ttu-id="47504-111">전체 조직 또는 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하려면 Office 365 조직의 전역 관리자 이거나 Exchange Online 조직에서 조직 관리 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-111">You have to be a global administrator in your Office 365 organization or a member of the Organization Management role group in your Exchange Online organization to enable auto-expanding archiving for your entire organization or for specific users.</span></span> <span data-ttu-id="47504-112">또는 특정 사용자에 대 한 자동 확장 보관을 사용 하도록 설정 하려면 Mail Recipients 역할이 할당 된 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-112">Alternately, you have to be a member of a role group that's assigned the Mail Recipients role to enable auto-expanding archiving for specific users.</span></span>
    
- <span data-ttu-id="47504-113">자동 확장 보관을 사용 하도록 설정 하려면 먼저 사용자의 보관 사서함을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-113">A user's archive mailbox has to be enabled before you can enable auto-expanding archiving.</span></span> <span data-ttu-id="47504-114">보관 사서함을 사용 하도록 설정 하려면 사용자에 게 Exchange Online 계획 2 라이선스를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-114">A user must be assigned an Exchange Online Plan 2 license to enable the archive mailbox.</span></span> <span data-ttu-id="47504-115">사용자에 게 exchange online 계획 1 라이선스가 할당 된 경우 해당 보관 사서함을 사용 하도록 설정 하기 위해 별도의 exchange online 보관 라이선스를 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-115">If a user is assigned an Exchange Online Plan 1 license, you would have to assign them a separate Exchange Online Archiving license to enable their archive mailbox.</span></span> <span data-ttu-id="47504-116">[보안 & 준수 센터에서 보관 사서함 사용](enable-archive-mailboxes.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="47504-116">See [Enable archive mailboxes in the Security & Compliance Center](enable-archive-mailboxes.md).</span></span>
    
- <span data-ttu-id="47504-117">또한 PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-117">You can also use PowerShell to enable archive mailboxes.</span></span> <span data-ttu-id="47504-118">조직의 모든 사용자에 대해 보관 사서함을 사용 하도록 설정 하는 데 사용할 수 있는 PowerShell 명령의 예는 [추가 정보](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="47504-118">See the [More information](#more-information) section for an example of the PowerShell command that you can use to enable archive mailboxes for all users in your organization.</span></span> 
    
- <span data-ttu-id="47504-119">자동 확장 보관 기능은 공유 사서함도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-119">Auto-expanding archiving also supports shared mailboxes.</span></span> <span data-ttu-id="47504-120">공유 사서함에 대 한 보관 함을 사용 하도록 설정 하려면 exchange online 계획 2 라이선스 또는 교환 라이선스가 있는 exchange online 계획 1 라이선스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-120">To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span>
    
- <span data-ttu-id="47504-121">Exchange 관리 센터 또는 Security & 준수 센터를 사용 하 여 자동 확장 보관을 사용 하도록 설정할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-121">You can't use the Exchange admin center or the Security & Compliance Center to enable auto-expanding archiving.</span></span> <span data-ttu-id="47504-122">Exchange Online PowerShell을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-122">You have to use Exchange Online PowerShell.</span></span> <span data-ttu-id="47504-123">원격 PowerShell을 사용 하 여 exchange online 조직에 연결 하려면 [exchange online PowerShell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47504-123">To connect to your Exchange Online organization using remote PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a><span data-ttu-id="47504-124">전체 조직에 대해 자동 확장 보관을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="47504-124">Enable auto-expanding archiving for your entire organization</span></span>

<span data-ttu-id="47504-125">전체 조직에 대해 자동 확장 보관을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-125">You can enable auto-expanding archiving for your entire organization.</span></span> <span data-ttu-id="47504-126">이 기능을 켜면 기존 사용자 사서함과 새로 만든 사용자 사서함에 대해 자동 확장 보관이 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-126">After you turn it on, auto-expanding archiving will be enabled for existing user mailboxes and for new user mailboxes that are created.</span></span> <span data-ttu-id="47504-127">새 사용자 사서함을 만들 때는 사용자의 기본 보관 사서함을 사용 하도록 설정 하 여 새 사용자 사서함에 대해 자동 확장 보관 기능을 사용할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-127">When you create new user mailboxes, be sure to enable the user's main archive mailbox so the auto-expanding archiving feature will work for the new user mailbox.</span></span>
  
1. [<span data-ttu-id="47504-128">Exchange Online PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="47504-128">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. <span data-ttu-id="47504-129">Exchange Online PowerShell에서 다음 명령을 실행 하 여 전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-129">Run the following command in Exchange Online PowerShell to enable auto-expanding archiving for your entire organization.</span></span>

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a><span data-ttu-id="47504-130">특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="47504-130">Enable auto-expanding archiving for specific users</span></span>

<span data-ttu-id="47504-131">조직의 모든 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하는 대신 특정 사용자 에게만 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-131">Instead of enabling auto-expanding archiving for every user in your organization, you can just enable it for specific users.</span></span> <span data-ttu-id="47504-132">이 작업을 수행 하는 경우에는 일부 사용자 에게만 대용량 보관 저장소를 사용할 필요가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-132">You might do this because only some users might have a need for a very large archive storage.</span></span>
  
<span data-ttu-id="47504-133">특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하 고 보류 중이거나 Office 365 보존 정책에 할당 된 사용자의 사서함에 대해 다음 두 가지 구성 변경이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-133">When you enable auto-expanding archiving for a specific user and the user's mailbox in on hold or assigned to an Office 365 retention policy, the following two configurations changes are made:</span></span>
  
- <span data-ttu-id="47504-134">사용자의 기본 보관 사서함에 대 한 저장소 할당량을 10gb로 증가 시킵니다 (100에서 110 g b까지).</span><span class="sxs-lookup"><span data-stu-id="47504-134">The storage quota for the user's primary archive mailbox is increased by 10 GB (from 100 GB to 110 GB).</span></span> <span data-ttu-id="47504-135">보관 경고 할당량은 10gb (90에서 100 gb까지)로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-135">The archive warning quota is also increased by 10 GB (from 90 GB to 100 GB).</span></span>
    
- <span data-ttu-id="47504-136">사용자의 기본 사서함에 있는 복구 가능한 항목 폴더의 저장소 할당량은 10gb로 증가 합니다 (100에서 110 g b까지).</span><span class="sxs-lookup"><span data-stu-id="47504-136">The storage quota for the Recoverable Items folder in the user's primary mailbox is increased by 10 GB (also from 100 GB to 110 GB).</span></span> <span data-ttu-id="47504-137">복구 가능한 항목 경고 할당량은 10gb (90에서 100 gb까지)로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-137">The Recoverable Items warning quota is also increased by 10 GB (from 90 GB to 100 GB).</span></span> <span data-ttu-id="47504-138">이러한 변경 내용은 사서함이 보류 되거나 Office 365 보존 정책에 할당 된 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-138">These changes are applicable only if the mailbox in on hold or assigned to an Office 365 retention policy.</span></span>
    
<span data-ttu-id="47504-139">이 추가 공간은 자동 확장 보관이 구축 되기 전에 발생할 수 있는 저장 문제를 방지 하기 위해 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-139">This additional space is added to prevent any storage issues that may occur before the auto-expanding archive is provisioned.</span></span> <span data-ttu-id="47504-140">이전 섹션에 설명 된 대로 전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 하면 추가 저장 공간이 추가 *되지 않습니다* .</span><span class="sxs-lookup"><span data-stu-id="47504-140">Note that additional storage space  *is not*  added when you enable auto-expanding archiving for your entire organization, as described in the previous section.</span></span> 
  
1. [<span data-ttu-id="47504-141">Exchange Online PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="47504-141">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. <span data-ttu-id="47504-142">Exchange Online PowerShell에서 다음 명령을 실행 하 여 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-142">Run the following command in Exchange Online PowerShell to enable auto-expanding archiving for a specific user.</span></span> <span data-ttu-id="47504-143">앞에서 설명한 것 처럼 사용자의 보관 사서함 (기본 보관 함)을 사용 하도록 설정 해야 해당 사용자에 대해 자동 확장 보관을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-143">As previously explained, the user's archive mailbox (main archive) must be enabled before you can turn on auto-expanding archiving for that user.</span></span>
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> <span data-ttu-id="47504-144">Exchange 하이브리드 배포에서는 기본 사서함이 온-프레미스이 고 보관 사서함이 클라우드 기반 인 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하기 위해 **AutoExpandingArchive** 명령을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-144">In an Exchange hybrid deployment, you can't use the **Enable-Mailbox -AutoExpandingArchive** command to enable auto-expanding archiving for specific a user whose primary mailbox is on premises and their archive mailbox is cloud-based.</span></span> <span data-ttu-id="47504-145">exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하려면 exchange Online PowerShell에서 **set-organizationconfig-AutoExpandingArchive** 명령을 실행 하 여 자동 확장 보관을 사용 하도록 설정 해야 합니다. 전체 조직</span><span class="sxs-lookup"><span data-stu-id="47504-145">To enable auto-expanding archiving for cloud-based archive mailboxes in an Exchange hybrid deployment, you have to run the **Set-OrganizationConfig -AutoExpandingArchive** command in Exchange Online PowerShell to enable auto-expanding archiving for the entire organization.</span></span> <span data-ttu-id="47504-146">사용자의 기본 및 보관 사서함이 둘 다 클라우드 기반 인 경우에는 **AutoExpandingArchive** 명령을 사용 하 여 해당 특정 사용자에 대 한 자동 확장 보관을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-146">If a user's primary and archive mailboxes are both cloud-based, then you can use the **Enable-Mailbox -AutoExpandingArchive** command to enable auto-expanding archiving for that specific user.</span></span> 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a><span data-ttu-id="47504-147">자동 확장 보관이 사용 되도록 설정 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="47504-147">Verify that auto-expanding archiving is enabled</span></span>

<span data-ttu-id="47504-148">조직에 대해 자동 확장 보관을 사용 하도록 설정 되어 있는지 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-148">To verify that auto-expanding archiving is enabled for your organization, run the following command in Exchange Online PowerShell.</span></span>

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

<span data-ttu-id="47504-149">값은 조직 `True` 에 대해 자동 확장 보관을 사용 하도록 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="47504-149">A value of  `True` indicates that auto-expanding archiving is enabled for the organization.</span></span> 
  
<span data-ttu-id="47504-150">특정 사용자가 자동 확장 보관을 사용 하도록 설정 되어 있는지 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-150">To verify that auto-expanding archiving is enable for a specific user, run the following command in Exchange Online PowerShell.</span></span>
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
<span data-ttu-id="47504-151">값은 사용자 `True` 에 대해 자동 확장 보관을 사용 하도록 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="47504-151">A value of  `True` indicates that auto-expanding archiving is enabled for the user.</span></span> 
  
<span data-ttu-id="47504-152">자동 확장 보관을 사용 하도록 설정한 후에는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47504-152">Keep the following things in mind after you enable auto-expanding archiving:</span></span>
  
- <span data-ttu-id="47504-153">**set-organizationconfig-AutoExpandingArchive** 명령을 실행 하 여 조직에 대해 자동 확장 보관을 사용 하도록 설정 하는 경우에는 개별 사서함에서 **enable-AutoExpandingArchive** 를 실행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-153">If you run the **Set-OrganizationConfig -AutoExpandingArchive** command to enable auto-expanding archiving for your organization, you don't have to run the **Enable-Mailbox -AutoExpandingArchive** on individual mailboxes.</span></span> <span data-ttu-id="47504-154">**set-organizationconfig** cmdlet을 실행 하 여 조직에 대해 자동 확장 보관을 사용 하도록 설정 해도 사용자 사서함의 *AutoExpandingArchiveEnabled* 속성은로 `True`변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-154">Note that running the **Set-OrganizationConfig** cmdlet to enable auto-expanding archiving for your organization doesn't change the  *AutoExpandingArchiveEnabled*  property on user mailboxes to  `True`.</span></span>
    
- <span data-ttu-id="47504-155">마찬가지로 자동 확장 보관을 사용 하도록 설정 하면 *ArchiveQuota* 및 *ArchiveWarningQuota* 사서함 속성의 값이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-155">Similarly, the values for the  *ArchiveQuota*  and  *ArchiveWarningQuota*  mailbox properties aren't changed when you enable auto-expanding archiving.</span></span> <span data-ttu-id="47504-156">실제로 사용자 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하 고 *AutoExpandingArchiveEnabled* `True`속성을로 설정 하면 *ArchiveQuota* 및 *ArchiveWarningQuota* 속성이 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-156">In fact, when you enable auto-expanding archiving for a user mailbox and the  *AutoExpandingArchiveEnabled*  property is set to  `True`, the  *ArchiveQuota*  and  *ArchiveWarningQuota*  properties are just ignored.</span></span> <span data-ttu-id="47504-157">다음은 사용자 사서함에 대해 자동 확장 보관을 사용 하도록 설정한 후 이러한 사서함 속성의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="47504-157">Here's an example of these mailbox properties after auto-expanding archiving is enabled for a user's mailbox.</span></span> 
    
    ![자동 확장 보관을 사용 하도록 설정한 후에는 ArchiveQuota 및 ArchiveWarningQuota 속성이 무시 됩니다.](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a><span data-ttu-id="47504-159">추가 정보</span><span class="sxs-lookup"><span data-stu-id="47504-159">More information</span></span>

- <span data-ttu-id="47504-160">또한 PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-160">You can also use PowerShell to enable archive mailboxes.</span></span> <span data-ttu-id="47504-161">예를 들어 Exchange Online PowerShell에서 다음 명령을 실행 하 여 보관 사서함이 아직 사용 하도록 설정 되지 않은 모든 사용자에 대해 보관 사서함을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-161">For example, you can run the following command in Exchange Online PowerShell to enable archive mailboxes for all users whose archive mailbox isn't already enabled.</span></span>

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- <span data-ttu-id="47504-162">조직 또는 특정 사용자에 대해 자동 확장 보관을 설정 하면 보관 사서함 (복구 가능한 항목 폴더 포함)이 90 GB에 도달할 때 보관 사서함이 자동 확장 아카이브로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-162">After you turn on auto-expanding archiving for your organization or for a specific user, an archive mailbox is converted to an auto-expanding archive when the archive mailbox (including the Recoverable Items folder) reaches 90 GB.</span></span> <span data-ttu-id="47504-163">추가 저장 공간을 프로 비전 하는 데 최대 30 일이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-163">It can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
- <span data-ttu-id="47504-164">자동 확장 보관을 설정한 후에는 끌 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-164">After you turn on auto-expanding archiving, it can't be turned off.</span></span>
    
- <span data-ttu-id="47504-165">온-프레미스 기본 사서함이 있는 사용자의 경우 Exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대해 자동 확장 보관이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-165">Auto-expanding archiving is supported for cloud-based archive mailboxes in an Exchange hybrid deployment for users who have an on-premises primary mailbox.</span></span> <span data-ttu-id="47504-166">그러나 클라우드 기반 보관 사서함에 대해 자동 확장 보관을 사용 하도록 설정한 후에는 온-프레미스 Exchange 조직으로 사서함을 다시 보관 하는 보드를 끌 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-166">However, after auto-expanding archiving is enabled for a cloud-based archive mailbox, you can't off-board that archive mailbox back to the on-premises Exchange organization.</span></span> <span data-ttu-id="47504-167">Exchange Server 2010의 온-프레미스 사서함에 대해서는 자동 확장 보관이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-167">Note that auto-expanding archiving isn't supported for on-premises mailboxes in Exchange Server 2010.</span></span>
    
- <span data-ttu-id="47504-168">사용자가 보관 사서함의 추가 저장소 영역에 있는 항목에 액세스 하는 데 사용할 수 있는 outlook 클라이언트 목록은 [Office 365의 무제한 보관](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) 에 대 한 개요의 "자동 확장 된 보관 함 항목에 액세스 하기 위한 Outlook 요구 사항" 섹션을 참조 하세요. .</span><span class="sxs-lookup"><span data-stu-id="47504-168">For a list of Outlook clients that users can use to access items in the additional storage area in their archive mailbox, see the "Outlook requirements for accessing items in an auto-expanded archive" section in [Overview of unlimited archiving in Office 365](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive).</span></span>
    
- <span data-ttu-id="47504-169">앞에서 설명한 것 처럼, **AutoExpandingArchive** 명령을 실행할 때 사용자의 기본 보관 사서함 및 사서함이 대기 중인 경우 복구 가능한 항목 폴더의 저장소 할당량에 10gb가 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-169">As previously explained, 10 GB is added to the storage quota of the user's primary archive mailbox (and to the Recoverable Items folder if the mailbox is on hold) when you run the **Enable-Mailbox -AutoExpandingArchive** command.</span></span> <span data-ttu-id="47504-170">이렇게 하면 자동 확장 된 저장소 공간이 프로 비전 될 때까지 (최대 30 일이 걸릴 수 있음) 추가 저장소가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-170">This provides additional storage until the auto-expanded storage space is provisioned (which can take up to 30 days).</span></span> <span data-ttu-id="47504-171">**set-organizationconfig-AutoExpandingArchive** 을 실행 하 여 조직의 모든 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하면이 추가 저장소 공간이 추가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-171">This additional storage space isn't added when you run the **Set-OrganizationConfig -AutoExpandingArchive** to enable auto-expanding archiving for all mailboxes in your organization.</span></span> <span data-ttu-id="47504-172">전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 했지만 특정 사용자에 게 10gb의 추가 저장 공간을 추가 해야 하는 경우 해당 사서함에서 **AutoExpandingArchive** 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-172">If you enabled auto-expanding archiving for the entire organization, but need to add the additional 10 GB of storage space for a specific user, you can run the **Enable-Mailbox -AutoExpandingArchive** command on that mailbox.</span></span> <span data-ttu-id="47504-173">자동 확장 보관이 이미 사용 하도록 설정 되었지만 추가 저장 공간이 사서함에 추가 된다는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-173">Note that you will receive an error saying that auto-expanding archiving has already been enabled, but the additional storage space will be added to the mailbox.</span></span> 

- <span data-ttu-id="47504-174">관리자가 저장소 할당량을 조정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-174">Administrators can't adjust the storage quota.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47504-175">자동 확장 보관은 일별 크기가 1gb를 넘지 않는 개별 사용자 또는 공유 사서함에 사용 되는 사서함에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47504-175">Auto-expanding archiving is only supported for mailboxes used for individual users or shared mailboxes with a growth rate that doesn't exceed 1 GB per day.</span></span> <span data-ttu-id="47504-176">보관을 목적으로 저널링, 전송 규칙 또는 자동 전달 규칙을 사용 하 여 보관 사서함에 메시지를 복사할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-176">Using journaling, transport rules, or auto-forwarding rules to copy messages to an archive mailbox for the purposes of archiving is not permitted.</span></span> <span data-ttu-id="47504-177">사용자의 보관 사서함은 해당 사용자만을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="47504-177">A user's archive mailbox is intended for just that user.</span></span> <span data-ttu-id="47504-178">Microsoft는 사용자의 보관 사서함이 다른 사용자의 보관 데이터를 저장하는데 사용되는 경우 인스턴스의 무제한 보관을 거부할 권리를 가지고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47504-178">Microsoft reserves the right to deny unlimited archiving in instances where a user's archive mailbox is used to store archive data for other users.</span></span>
