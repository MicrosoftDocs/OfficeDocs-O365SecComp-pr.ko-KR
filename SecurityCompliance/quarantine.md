---
title: 격리
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: e9eecdde-dcc2-4283-a820-98d1e740e4f
ms.collection:
- M365-security-compliance
description: exchange online 및 exchange online Protection에 대 한 호스팅된 격리에 대해 알아봅니다.
ms.openlocfilehash: 9d0f00f5305838f1862eebdc649de0205679d282
ms.sourcegitcommit: 173936324ea015d788703440924ec8a9fb0db88b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/08/2019
ms.locfileid: "30510215"
---
# <a name="quarantine"></a><span data-ttu-id="81107-103">격리</span><span class="sxs-lookup"><span data-stu-id="81107-103">Quarantine</span></span>

<span data-ttu-id="81107-104">다음 항목에서는 Exchange Online 및 EOP(Exchange Online Protection) 관리자와 최종 사용자에게 적용되는 호스팅된 격리에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="81107-104">The following topics provide information about the hosted quarantine for both Exchange Online and Exchange Online Protection (EOP) admins and end users:</span></span>
  
- <span data-ttu-id="81107-105">[격리 FAQ](quarantine-faq.md) - 관리자와 최종 사용자 모두에게 적용되는 격리에 대한 일반적인 질문과 대답을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="81107-105">[Quarantine FAQ](quarantine-faq.md) - Provides general questions and answers about the quarantine for both admins and end users</span></span> 
    
- <span data-ttu-id="81107-106">[관리자로 격리된 메시지 찾기 및 릴리스](find-and-release-quarantined-messages-as-an-administrator.md) - 관리자가 EAC(Exchange 관리 센터)의 격리에 상주하는 메시지를 찾아서 릴리스하고, 필요한 경우 이를 가양성(정크 메일 아님) 메시지로 Microsoft에 보고하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="81107-106">[Find and release quarantined messages as an administrator](find-and-release-quarantined-messages-as-an-administrator.md) - Describes how admins can find and release any message that resides in the quarantine in the Exchange admin center (EAC), and optionally report it as a false positive (not junk) message to Microsoft.</span></span> 
    
- <span data-ttu-id="81107-107">[찾기 및 릴리스 격리 된 메시지 (최종 사용자)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx) -최종 사용자가 스팸 격리 사용자 인터페이스에서 자신의 스팸 격리 메시지를 찾아서 릴리스하고이를 정크 메일 아님으로 Microsoft에 보고 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="81107-107">[Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx) - Describes how end users can find and release their own spam-quarantined messages in the spam quarantine user interface, and report them as not junk to Microsoft.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="81107-108">최종 사용자 스팸 격리에 액세스 하려면 최종 사용자에 게 유효한 Office 365 사용자 ID 및 암호가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81107-108">In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password.</span></span> <span data-ttu-id="81107-109">온-프레미스 사서함을 보호 하는 EOP 고객은 디렉터리 동기화 또는 EAC를 통해 만든 유효한 전자 메일 사용자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81107-109">EOP customers protecting on-premises mailboxes must be valid email users created via directory synchronization or the EAC.</span></span> <span data-ttu-id="81107-110">사용자를 관리 하는 방법에 대 한 자세한 내용은 EOP 관리자가 [EOP에서 메일 사용자 관리](eop/manage-mail-users-in-eop.md)를 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81107-110">For more information about managing users, EOP admins can refer to [Manage mail users in EOP](eop/manage-mail-users-in-eop.md).</span></span> <span data-ttu-id="81107-111">EOP 독립 실행형 고객의 경우 디렉터리 동기화 및 디렉터리 기반 Edge 차단을 사용 하는 것이 좋습니다. 자세한 내용은 [디렉터리 기반 Edge 차단을 사용 하 여 잘못 된 받는 사람에 게 보낸 메시지 거부](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="81107-111">For EOP standalone customers, we recommend using directory synchronization and enabling Directory Based Edge Blocking; for more information, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span> 
  
    

