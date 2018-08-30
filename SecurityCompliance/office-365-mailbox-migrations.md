---
title: Office 365 사서함 마이그레이션
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Office 365 사서함 마이그레이션에 사용 되는 cmdlet에 대 한 간략 한 요약입니다.
ms.openlocfilehash: 86896d956072b5c11e3b3292363bb32312ff1187
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533752"
---
# <a name="office-365-mailbox-migrations"></a><span data-ttu-id="f1c2a-103">Office 365 사서함 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="f1c2a-103">Office 365 Mailbox Migrations</span></span>
<span data-ttu-id="f1c2a-p101">Exchange 기반 하이브리드 배포, 고객 [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) 조직에 온-프레미스 Exchange 사서함으로 이동 하거나 [Exchange 온-프레미스](https://docs.microsoft.com/Exchange/exchange-server) 조직으로 Exchange Online 사서함 이동 하도록 선택할 수 있습니다. 마이그레이션 일괄 처리는 온-프레미스 조직과 Exchange Online 조직 간에 사서함을 이동할 때 사용 됩니다. 고객 통계 및 다음 cmdlet을 사용 하 여 사서함 마이그레이션에 대 한 기타 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-p101">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization. Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations. Customers can review statistics and other information about mailbox migrations using the following cmdlets:</span></span>

- <span data-ttu-id="f1c2a-107">[Get-moverequeststatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) -제공 상태, 사서함 크기를 포함 하는 사용자 사서함에 대 한 기본 통계 보관 사서함 크기 및 백분율을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size and percentage complete.</span></span>
- <span data-ttu-id="f1c2a-108">[Get-mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) -사서함 개체 및 특성은 조직에서의 요약 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="f1c2a-109">[Get-받는 사람](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) -사서함, 메일 사용자, 연락처 및 메일 그룹 등 기존 메일 사용이 가능한 개체의 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts and distribution groups.</span></span>
- <span data-ttu-id="f1c2a-110">[Get-moverequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) -진행 중인 사서함 마이그레이션의 자세한 상태를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="f1c2a-111">[Get-migrationuser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) -이동 및 마이그레이션 사용자의 사서함에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="f1c2a-112">[Get-migrationbatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) -현재 마이그레이션 일괄 처리의 상태 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="f1c2a-113">[Get-migrationuserstatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) -특정 사용자에 대 한 마이그레이션 상태에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="f1c2a-114">[Get-mailboxstatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) -크기, 메시지, 수, 마지막 액세스 시간 등의 사서함에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="f1c2a-115">추가 cmdlet에 대 한 자세한 내용은 [Exchange Online의 이동 및 마이그레이션 cmdlet](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f1c2a-115">For more information on additional cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
