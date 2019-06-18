---
title: Office 365에서 타사 데이터 보관
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: '관리자는 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 Office 365 조 직의 사서함으로 타사 데이터를 가져올 수 있습니다. 이를 통해 Office 365의 Facebook, Twitter 및 기타 타사 데이터 원본에서 데이터를 보관할 수 있습니다. 그런 다음 타사 데이터에 대해 Office 365 준수 기능 (예: 법적 보존, eDiscovery, 원본 위치 보관 및 보존 정책)을 사용 하 여 적용할 수 있습니다.'
ms.openlocfilehash: 796ad0314374dca60d1ff5f6b9317be491b757a1
ms.sourcegitcommit: f2798d46acfbd56314e809cd3fe0350be807e420
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/17/2019
ms.locfileid: "35014607"
---
# <a name="archive-third-party-data-in-office-365"></a><span data-ttu-id="7e7d6-105">Office 365에서 타사 데이터 보관</span><span class="sxs-lookup"><span data-stu-id="7e7d6-105">Archive third-party data in Office 365</span></span>

<span data-ttu-id="7e7d6-106">관리자는 office 365을 사용 하 여 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 타사 데이터를 가져오고 Office 365 조직의 사서함으로 보관할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-106">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization.</span></span> <span data-ttu-id="7e7d6-107">Office 365로 가져올 수 있는 타사 데이터 원본의 예에는 다음 서비스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-107">Examples of third-party data sources that you can import to Office 365 include the following services:</span></span> 
  
- <span data-ttu-id="7e7d6-108">**소셜** – Facebook, LinkedIn, Twitter 및 Yammer</span><span class="sxs-lookup"><span data-stu-id="7e7d6-108">**Social** – Facebook, LinkedIn, Twitter, and Yammer</span></span> 
    
- <span data-ttu-id="7e7d6-109">**인스턴트 메시징** – Yahoo Messenger, GoogleTalk 및 Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="7e7d6-109">**Instant messaging** – Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="7e7d6-110">**문서 공동 작업** – Box 및 DropBox</span><span class="sxs-lookup"><span data-stu-id="7e7d6-110">**Document collaboration** – Box and DropBox</span></span> 
    
- <span data-ttu-id="7e7d6-111">**세로 산업** -고객 관계 관리 (예: Salesforce Chatter) 및 금융 서비스 (예: Bloomberg 및: Thomson Reuters)</span><span class="sxs-lookup"><span data-stu-id="7e7d6-111">**Vertical industries** – Customer Relationship Management (such as Salesforce Chatter) and Financial Services (such as Bloomberg and Thomson Reuters)</span></span> 
    
- <span data-ttu-id="7e7d6-112">**SMS/텍스트 메시징** – BlackBerry</span><span class="sxs-lookup"><span data-stu-id="7e7d6-112">**SMS/text messaging** – BlackBerry</span></span> 
    
<span data-ttu-id="7e7d6-113">타사 데이터를 가져온 후에는이 데이터에 소송 보존, eDiscovery, 원본 위치 보관, 감사, 감독 및 Office 365 보존 정책 등의 Office 365 준수 기능을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-113">After third-party data is imported, you can apply Office 365 compliance features — such as Litigation Hold, eDiscovery, In-Place Archiving, Auditing, Supervision, and Office 365 retention policies — to this data.</span></span> <span data-ttu-id="7e7d6-114">예를 들어 사서함에 소송 보존이 적용되면 타사 데이터가 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-114">For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved.</span></span> <span data-ttu-id="7e7d6-115">Microsoft eDiscovery 도구를 사용 하 여 타사 데이터를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-115">You can search third-party data by using Microsoft eDiscovery tools.</span></span> <span data-ttu-id="7e7d6-116">또는 Microsoft 데이터의 경우처럼 타사 데이터에도 보관 및 삭제 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-116">Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data.</span></span> <span data-ttu-id="7e7d6-117">간단히 말해서 Office 365에서 타사 데이터를 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-117">In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>

<span data-ttu-id="7e7d6-118">Office 365에서는 두 가지 방법으로 타사 데이터를 가져오고 보관할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-118">There are two ways to import and archive third-party data in Office 365:</span></span>

- <span data-ttu-id="7e7d6-119">**보안 & 준수 센터에서 타사 데이터 커넥터 사용** -Office 365의 보안 & 준수 센터에서 사용할 수 있는 사용자 지정 데이터 커넥터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-119">**Use a third-party data connector in the Security & Compliance Center** – Use a custom data connector that's available in the Security & Compliance Center in Office 365.</span></span> <span data-ttu-id="7e7d6-120">커넥터를 설정 하 고 구성한 후에는 타사 데이터 원본에 연결 하 고, 항목의 콘텐츠를 전자 메일 메시지 형식으로 변환한 다음 Office 365에서 사서함으로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-120">After you set up and configure the connector, it connects to the third-party data source, converts the content of an item to an email message format, and then imports the item to a mailbox in Office 365.</span></span> <span data-ttu-id="7e7d6-121">이 경우에는 Facebook Business pages, 회사 Twitter 계정, 인스턴트 Bloomberg 및 LinkedIn에서 데이터를 가져오고 보관 하기 위한 커넥터를 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-121">At this time, you can implement connectors to import and archive data from Facebook Business pages, corporate Twitter accounts, Instant Bloomberg, and LinkedIn.</span></span> <span data-ttu-id="7e7d6-122">커넥터를 설정 하는 단계별 지침은 다음 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-122">For the step-by-step instructions to set up a connector, see:</span></span>
   
   - <span data-ttu-id="7e7d6-123">**Facebook** - [예제 커넥터를 사용 하 여 Office 365에서 Facebook 데이터 보관](archive-facebook-data-with-sample-connector.md)</span><span class="sxs-lookup"><span data-stu-id="7e7d6-123">**Facebook** – [Use a sample connector to archive Facebook data in Office 365](archive-facebook-data-with-sample-connector.md)</span></span>
  
   - <span data-ttu-id="7e7d6-124">**Twitter** - [샘플 커넥터를 사용 하 여 Office 365에서 Twitter 데이터를 보관 합니다](archive-twitter-data-with-sample-connector.md) .</span><span class="sxs-lookup"><span data-stu-id="7e7d6-124">**Twitter** – [Use a sample connector to archive Twitter data in Office 365](archive-twitter-data-with-sample-connector.md)</span></span>
    
   - <span data-ttu-id="7e7d6-125">**LinkedIn** - [Office 365에서 LinkedIn 데이터를 보관 하는 커넥터 설정](archive-linkedin-data.md)</span><span class="sxs-lookup"><span data-stu-id="7e7d6-125">**LinkedIn** – [Set up a connector to archive LinkedIn data in Office 365](archive-linkedin-data.md)</span></span>

- <span data-ttu-id="7e7d6-126">**Microsoft 파트너와 공동 작업** -조직에서 타사 데이터 원본에서 항목을 추출 하도록 구성 되는 사용자 지정 커넥터를 제공 하는 microsoft 파트너와 함께 작동 하며, 다음을 수행 하 여 microsoft 클라우드에 연결 합니다. 타사 API를 사용 하 여 Office 365로 해당 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-126">**Work with a Microsoft partner** – Your organization works with a Microsoft Partner who will provide a custom connector that will be configured to extract items from the third-party data source (on a regular basis) and then connect to the Microsoft cloud by a third-party API and import those items to Office 365.</span></span> <span data-ttu-id="7e7d6-127">또한 파트너 커넥터는 타사 데이터 원본에서 전자 메일 메시지로 항목의 콘텐츠를 변환한 다음 Office 365에서 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-127">The partner connector also converts the content of an item from the third-party data source to an email message and then imports them to a mailbox in Office 365.</span></span> <span data-ttu-id="7e7d6-128">사용할 수 있는 파트너의 목록과이 방법의 단계별 프로세스에 대 한 자세한 내용은 [Office 365에서 파트너와 협력 하 여 타사 데이터 보관](work-with-partner-to-archive-third-party-data.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-128">For a list of partners that you can work with and the step-by-step process for this method, see [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md).</span></span>