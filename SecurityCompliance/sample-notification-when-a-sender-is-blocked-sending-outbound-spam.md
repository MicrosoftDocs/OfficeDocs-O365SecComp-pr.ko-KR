---
title: 보낸 사람이 아웃 바운드 스팸을 보내는 것이 차단 된 경우의 예제 알림
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/02/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c33fd406-a4c8-4ac8-ad85-123996c5cded
ms.collection:
- M365-security-compliance
description: 아웃 바운드 스팸 보내기로 인해 서비스에서 보낸 사람이 차단 되는 경우 아웃 바운드 스팸 정책을 구성할 때 지정한 도메인 관리자는 다음과 같은 알림 전자 메일을 받게 됩니다.
ms.openlocfilehash: 1733b291a57dc006d52883ba72160dbc4135d8db
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35601055"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a><span data-ttu-id="688a0-103">보낸 사람이 아웃 바운드 스팸을 보내는 것이 차단 된 경우의 예제 알림</span><span class="sxs-lookup"><span data-stu-id="688a0-103">Sample notification when a sender is blocked sending outbound spam</span></span>

<span data-ttu-id="688a0-104">아웃 바운드 스팸 보내기로 인해 서비스에서 보낸 사람이 차단 되는 경우 [아웃 바운드 스팸 정책을 구성할](configure-the-outbound-spam-policy.md) 때 지정한 도메인 관리자는 다음과 같은 알림 전자 메일을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-104">When a sender is blocked from the service due to sending outbound spam, the domain admin specified when you [Configure the outbound spam policy](configure-the-outbound-spam-policy.md) will receive a notification email similar to the following:</span></span> 
  
 <span data-ttu-id="688a0-105">**보낸 사람 주소:** spamalerts@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="688a0-105">**Sender address:** spamalerts@microsoft.com</span></span> 
  
 <span data-ttu-id="688a0-106">**제목:** 아웃 바운드 스팸 알림 \<-아웃 바운드 메일을 보낼 때 차단 되는 *계정 이름* \>    </span><span class="sxs-lookup"><span data-stu-id="688a0-106">**Subject:** Outbound spam notification - \<  *account name*  \> blocked from sending outbound mail</span></span> 
  
 <span data-ttu-id="688a0-107">**본문:** 이 메시지는 Exchange Online Protection 스팸 분석 시스템에서 자동화 된 회신입니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-107">**Body:** This is an automated reply from the Exchange Online Protection Spam Analysis System.</span></span> 
  
<span data-ttu-id="688a0-108">스팸으로 표시 된 대량의 전자 메일 또는 조직에서 보낸 기타 의심 스러운 동작을 검색 했기 때문에 연락을 받고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-108">You are being contacted because we have detected high volumes of email marked as spam, or other suspicious behavior, originating from your organization.</span></span> <span data-ttu-id="688a0-109">다음 전자 메일 계정이 전자 메일을 보내지 못하도록 차단 되었습니다 (전자 메일이 계속 수신 될 수 있음).</span><span class="sxs-lookup"><span data-stu-id="688a0-109">The following email accounts have been blocked from sending email (they can still receive email):</span></span>
  
<span data-ttu-id="688a0-110">\<*계정 이름*  \></span><span class="sxs-lookup"><span data-stu-id="688a0-110">\< *account name*  \></span></span> 
  
<span data-ttu-id="688a0-111">이 전자 메일 계정이 손상 되었을 가능성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-111">It is likely that this email account has been compromised.</span></span> <span data-ttu-id="688a0-112">다음 단계를 수행 하세요.</span><span class="sxs-lookup"><span data-stu-id="688a0-112">Please follow these steps:</span></span>
  
1. <span data-ttu-id="688a0-113">다음을 통해이 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-113">Resolve this issue on your side by:</span></span>
    
  - <span data-ttu-id="688a0-114">계정의 암호 변경</span><span class="sxs-lookup"><span data-stu-id="688a0-114">Changing the password of the account.</span></span>
    
  - <span data-ttu-id="688a0-115">계정이 손상 된 방식을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-115">Determining how the account was compromised.</span></span>
    
  - <span data-ttu-id="688a0-116">이 취약점이 다시 악용 되지 않도록 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-116">Taking precautions to ensure that this vulnerability will not be exploited again.</span></span>
    
  - <span data-ttu-id="688a0-117">아웃 바운드 메일 큐가 모든 잘못 된 메시지를 지우도록 확인</span><span class="sxs-lookup"><span data-stu-id="688a0-117">Confirming that your outbound mail queue has been cleared of all offending messages.</span></span>
    
2. <span data-ttu-id="688a0-118">일반 연락처 채널을 사용 하 여 Microsoft 지원에 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-118">Contact Microsoft support by using your regular contact channel.</span></span>
    
3. <span data-ttu-id="688a0-119">메일을 보낼 수 없도록 차단 되 고 문제가 처리 되었음을 사용자에 게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-119">Explain that you have a user that is blocked from sending mail and that the problem has been dealt with.</span></span>
    
4. <span data-ttu-id="688a0-120">에이전트는 사용자가 제공한 정보를 사용 하 여 지원 티켓을 만들고이를 에스컬레이션 하 여 전자 메일 주소 또는 도메인이 차단 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-120">The agent will create a support ticket with the information that you provide and escalate it to have the email address or domain unblocked.</span></span>
    
5. <span data-ttu-id="688a0-121">주소가 차단 해제 되 고 다른 문제가 보류 되지 않은 후에는 연결 되 고 차단 해제에 대 한 경고가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-121">After the address has been unblocked, and pending no other issues, you will be contacted and alerted to the unblocking.</span></span>
    
<span data-ttu-id="688a0-122">원치 않는 전자 메일 제어에 대 한 microsoft의 지원 주셔서 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-122">Thank you for assisting us in controlling unwanted email.</span></span>
  
<span data-ttu-id="688a0-123">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="688a0-123">Exchange Online Protection.</span></span>
  
<span data-ttu-id="688a0-124">\*\*참고-이 전자 메일을 모니터링 되지 않은 주소로 전송 하 여이 이메일에 응답 하지 마세요.\*\*</span><span class="sxs-lookup"><span data-stu-id="688a0-124">\*\*NOTE - Please do not respond to this email as it is sent from an unmonitored address\*\*</span></span>
  
> [!TIP]
> <span data-ttu-id="688a0-125">또한 [도움말 및 EOP 지원](eop/help-and-support-for-eop.md)에서 설명 하는 옵션을 통해 지원에 문의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="688a0-125">You can also contact support via the options documented at [Help and support for EOP](eop/help-and-support-for-eop.md).</span></span> 
  

