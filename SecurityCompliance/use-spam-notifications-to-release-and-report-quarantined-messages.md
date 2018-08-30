---
title: Office 365에서 사용자 스팸 알림을 사용하여 격리된 메시지 릴리스 및 보고
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
description: 사용자 관리를 사용자에 대 한 알림을 사용 하도록 설정 하는 경우에 스팸, 대량, 또는 피싱 메시지도 식별 된 사서함에 보낸 메시지를 나열 하는 알림 메시지를 받게 됩니다. 릴리스 수도 있고 알리지 후 메시지를 보고할 수 있습니다.
ms.openlocfilehash: e355a94af5ac295503a8e205b1a896afc1c54fb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533244"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="b6444-104">Office 365에서 사용자 스팸 알림을 사용하여 격리된 메시지 릴리스 및 보고</span><span class="sxs-lookup"><span data-stu-id="b6444-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="b6444-105">사용자 관리를 사용자에 대 한 스팸 알림을 사용 하도록 설정 하는 경우에 스팸으로 식별 되어 대신 격리 된 사서함에 게 보내는 메시지를 나열 하는 알림 메시지를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="b6444-106">이 기능을 사용 하도록 설정 하 고 관리자 인 경우에 옵션을 선택할 수는 경우 [기본 스팸 방지 정책을 수정](https://go.microsoft.com/fwlink/?LinkId=800313)합니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="b6444-p102">받은 메시지의 목록에서 스팸 격리 된 메시지를 날짜 및 시간 (협정 세계시 또는 UTC)는 마지막으로 메시지의 수를 포함 합니다. 목록에는 각 메시지에 대 한 다음 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-p102">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list. The list includes the following for each message:</span></span>
  
- <span data-ttu-id="b6444-109">**보낸사람** 격리 된 메시지의 보내기 이름 및 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="b6444-110">**제목** 격리된 메시지의 제목 줄 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="b6444-111">**날짜** 메시지가 격리된 날짜와 시간(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="b6444-112">**크기** 크기 (kb) 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="b6444-113">현재, 격리 된 메시지에 적용할 수 있는 두 작업 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="b6444-114">**받은 편지 함으로 릴리스** 볼 수 있는 받은 편지함에 메시지를 보내려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="b6444-p103">**정크 메일 아님으로 보고서** 분석을 위해 Microsoft에 메시지의 복사본을 보내려면이 옵션을 선택 합니다. 스팸 팀을 평가 하 고 메시지를 분석 하 여 하 고, 분석의 결과 따라 조정 하는 스팸 방지 필터 규칙을 통해 메시지를 허용 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-p103">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis. The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="b6444-117">다음에 유의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="b6444-p104">메일 흐름 규칙 일치 하기 때문에 격리 된 메시지 사용자 격리 된 메시지에 포함 되지 않습니다. 스팸 격리 된 메시지만 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-p104">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages. Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="b6444-120">메시지를 릴리스하고 가양성으로(정크 아님) 한 번만 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6444-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

