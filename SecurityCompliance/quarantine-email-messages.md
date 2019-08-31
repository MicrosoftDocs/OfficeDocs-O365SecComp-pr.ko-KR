---
title: Office 365 전자 메일 메시지 격리
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 6/29/2018
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 4c234874-015e-4768-8495-98fcccfc639b
ms.collection:
- M365-security-compliance
description: 스팸, 대량, 피싱 메일 및 맬웨어로 필터링 된 받는 전자 메일 메시지를 나중에 검토할 수 있도록 Office 365에서 받는 전자 메일 메시지에 대 한 격리를 설정할 수 있습니다.
ms.openlocfilehash: 5590c9de9ff596c359910b5b1793004ae1913365
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699139"
---
# <a name="quarantine-email-messages-in-office-365"></a><span data-ttu-id="8aa7c-103">Office 365 전자 메일 메시지 격리</span><span class="sxs-lookup"><span data-stu-id="8aa7c-103">Quarantine email messages in Office 365</span></span>

<span data-ttu-id="8aa7c-104">스팸, 대량 메일, 피싱 메일, 맬웨어를 포함 하는 전자 메일, 지정 된 메일 흐름 규칙과 일치 하는 메일을 나중에 검토할 수 있도록 Office 365에서 받는 전자 메일 메시지에 대 한 격리를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-104">You can set up quarantine for incoming email messages in Office 365 where messages that have been filtered as spam, bulk mail, phishing mail, mail that contains malware, and mail that matched a specified mail flow rule can be kept for later review.</span></span>
  
<span data-ttu-id="8aa7c-105">기본적으로 필터링 된 메시지는 격리에 기본적으로 전송 되는 맬웨어가 포함 된 메일을 제외 하 고는 받는 사람의 정크 메일 폴더로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-105">By default, filtered messages are sent to the recipients' Junk Email folder, except for mail that contains malware which is sent to quarantine by default.</span></span> <span data-ttu-id="8aa7c-106">관리자는 대신 필터링 된 모든 메시지를 격리로 보내도록 콘텐츠 필터 정책을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-106">As an admin, you can set up content filter policies to send all filtered messages to quarantine instead.</span></span> <span data-ttu-id="8aa7c-107">콘텐츠 필터링 메시지에 대해 수행할 수 있는 여러 가지 작업은 [스팸 필터 구성 정책](configure-your-spam-filter-policies.md)에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-107">The different actions that you can take for content-filtered messages depend on the [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
<span data-ttu-id="8aa7c-108">사용자와 관리자가 격리 된 메시지를 사용 하 여 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-108">Both users and admins can work with quarantined messages.</span></span> <span data-ttu-id="8aa7c-109">사용자는 격리에서 필터링 된 메시지를 사용 하 여 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-109">Users can work with just their own filtered messages in quarantine.</span></span> <span data-ttu-id="8aa7c-110">관리자는 모든 사용자에 대해 격리 된 메시지를 검색 하 고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-110">Admins can search for and manage quarantined messages for all users.</span></span>

> [!NOTE]
> <span data-ttu-id="8aa7c-111">피싱 메시지 및 메일 흐름 규칙 (전송 규칙이 라고도 함)에 의해 격리 된 메시지는 관리자 격리 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-111">Phish messages and messages quarantined by mail flow rule (also known as transport rule) actions are only available in the admin quarantine.</span></span>
  
<span data-ttu-id="8aa7c-112">격리 된 메시지 작업에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="8aa7c-112">Learn more about working with quarantined messages:</span></span>
  
- [<span data-ttu-id="8aa7c-113">관리자로 격리 된 메시지 관리</span><span class="sxs-lookup"><span data-stu-id="8aa7c-113">Manage quarantined messages as an administrator</span></span>](manage-quarantined-messages-and-files.md)

- [<span data-ttu-id="8aa7c-114">사용자로 격리된 메시지 찾기 및 릴리스</span><span class="sxs-lookup"><span data-stu-id="8aa7c-114">Find and release quarantined messages as a user</span></span>](find-and-release-quarantined-messages-as-a-user.md)

- [<span data-ttu-id="8aa7c-115">사용자 스팸 알림을 사용 하 여 스팸 격리 된 메시지 릴리스 및 보고</span><span class="sxs-lookup"><span data-stu-id="8aa7c-115">Use user spam notifications to release and report spam-quarantined messages</span></span>](use-spam-notifications-to-release-and-report-quarantined-messages.md)

- [<span data-ttu-id="8aa7c-116">격리 FAQ</span><span class="sxs-lookup"><span data-stu-id="8aa7c-116">Quarantine FAQ</span></span>](quarantine-faq.md)
