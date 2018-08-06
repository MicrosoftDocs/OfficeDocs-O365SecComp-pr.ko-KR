---
title: EOP의 메일 흐름
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/13/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
description: EOP(Exchange Online Protection) 고객의 조직으로 전송되는 모든 메시지는 작업자에게 표시되기 전에 EOP를 통과합니다. 고객이 Exchange Online을 사용하여 클라우드에서 모든 사서함을 호스트하든, 기존 인프라를 계속 사용하기 위해 온-프레미스에서 사서함을 호스트하든(독립 실행형 시나리오) 관계없이 작업자의 받은 편지함으로 라우팅되기 전에 처리를 위해 EOP를 통과하는 메시지를 라우팅할 방법에 대한 옵션이 제공됩니다.
ms.openlocfilehash: d35e6f2fdbe7bb991ebf3d766fadae34638831ef
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027345"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="48534-104">EOP의 메일 흐름</span><span class="sxs-lookup"><span data-stu-id="48534-104">Mail flow in EOP</span></span>

<span data-ttu-id="48534-p102">EOP(Exchange Online Protection) 고객의 조직으로 전송되는 모든 메시지는 작업자에게 표시되기 전에 EOP를 통과합니다. 고객이 Exchange Online을 사용하여 클라우드에서 모든 사서함을 호스트하든, 기존 인프라를 계속 사용하기 위해 온-프레미스에서 사서함을 호스트하든(독립 실행형 시나리오) 관계없이 작업자의 받은 편지함으로 라우팅되기 전에 처리를 위해 EOP를 통과하는 메시지를 라우팅할 방법에 대한 옵션이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="48534-p102">As an Exchange Online Protection (EOP) customer, all messages sent to your organization pass through EOP before your workers see them. Whether you host all of your mailboxes in the cloud with Exchange Online, or you host your mailboxes on premises (called a standalone scenario), perhaps to continue taking advantage of your existing infrastructure, you have options about how to route messages that will pass through EOP for processing before they are routed to your worker inboxes.</span></span>
  
<span data-ttu-id="48534-p103">메시징이 비즈니스 요구 사항을 따르도록 사용자 지정 메일 라우팅을 구성할 수 있습니다. 예를 들어 정책 필터링 어플라이언스를 통해 모든 아웃바운드 메일을 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48534-p103">You may want to configure custom mail routing to conform your messaging to a business requirement. For instance, you can pass all of your outbound mail through a policy-filtering appliance.</span></span> 
  
## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="48534-109">메시지 및 메시지 액세스 옵션 사용</span><span class="sxs-lookup"><span data-stu-id="48534-109">Working with messages and message access options</span></span>

<span data-ttu-id="48534-p104">EOP는 매우 유동적인 메시지 라우팅 방식을 제공합니다. 다음 항목에서 메일 흐름 프로세스의 단계에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="48534-p104">EOP offers a lot of flexibility in how your messages are routed. The following topics explain steps in the mail flow process.</span></span>
  
<span data-ttu-id="48534-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) 서비스 네트워크 경계에서 잘못된 받는 사람에 대한 메시지를 거부할 수 있는 디렉터리 기반 Edge 차단 기능에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="48534-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span> 
  
<span data-ttu-id="48534-113">[View or Edit Managed Domains in EOP](http://technet.microsoft.com/library/69523bec-07ee-46f9-ae08-40437e39b87c.aspx)에서는 EOP 서비스와 연결된 도메인을 관리하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="48534-113">[View or Edit Managed Domains in EOP](http://technet.microsoft.com/library/69523bec-07ee-46f9-ae08-40437e39b87c.aspx) describes how to manage domains that are associated with your EOP service.</span></span> 
  
<span data-ttu-id="48534-p105">조직에 하위 도메인을 추가한 경우 EOP 서비스를 통해 관리할 수도 있습니다. 하위 도메인에 대한 자세한 내용은 [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="48534-p105">If you add subdomains to your organization, your EOP service can help you manage these too. Learn more about subdomains at [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span></span>
  
<span data-ttu-id="48534-p106">[Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx)에서는 커넥터에 대해 소개하고 이러한 커넥터를 통해 메일 라우팅을 사용자 지정하는 방법을 설명합니다. 또한 파트너 조직과의 통신을 보호하고 스마트 호스트를 설정하는 시나리오를 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="48534-p106">[Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) introduces connectors and shows how you can use them to customize mail routing. Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span> 
  
<span data-ttu-id="48534-p107">각 사용자의 정크 메일 폴더로 올바르게 정크 메일 라우팅되는지 되도록 몇 구성 단계를 수행 해야 합니다. 여기에서 자세히 설명 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)합니다. 각 사용자의 정크 메일 폴더로 메시지 이동 하지 않을 경우에 Exchange 관리 센터에서 콘텐츠 필터 정책을 편집 하 여 다른 작업을 선택할 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성](../configure-your-spam-filter-policies.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="48534-p107">To ensure that junk email is routed correctly to each user's junk-email folder, you must perform a couple configuration steps. These are detailed in [Ensure that spam is routed to each user's Junk Email folder](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). If you do not want to move messages to each user's junk-email folder, you may choose another action by editing your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](../configure-your-spam-filter-policies.md).</span></span>
  
## <a name="verify-mail-flow"></a><span data-ttu-id="48534-122">메일 흐름 확인</span><span class="sxs-lookup"><span data-stu-id="48534-122">Verify mail flow</span></span>

<span data-ttu-id="48534-p108">커넥터 구성을 비롯하여 EOP 설정이 제대로 작동하는지 확인하려면 [EOP 서비스 설정](set-up-your-eop-service.md)에서 "작동 여부는 어떻게 확인합니까?" 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="48534-p108">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](set-up-your-eop-service.md).</span></span> 
  
<span data-ttu-id="48534-125">[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx)에서는 메일 흐름이 올바르게 설정되었는지 테스트하는 지침을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="48534-125">[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) provides instructions for testing that your mail flow is set up correctly.</span></span> 
  

