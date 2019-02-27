---
title: Office 365에서 타사 데이터 보관
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: '관리자는 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 Office 365 조 직의 사서함으로 타사 데이터를 가져올 수 있습니다. 이를 통해 Office 365의 Facebook, Twitter 및 데이터 원본에서 데이터를 보관할 수 있습니다. 그런 다음 Office 365 규정 준수 기능 (예: 법적 보존, 콘텐츠 검색 및 보존 정책)을 타사 데이터에 추가할 수 있습니다.'
ms.openlocfilehash: 0f9f8b5a4ce5b4359430a3b15acc7bf16b2f0290
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296681"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="6715c-105">Office 365에서 타사 데이터 보관</span><span class="sxs-lookup"><span data-stu-id="6715c-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="6715c-p102">관리자는 office 365을 사용 하 여 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 타사 데이터를 가져오고 office 365 조직의 사서함으로 보관할 수 있습니다. Office 365로 가져올 수 있는 타사 데이터 원본의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="6715c-108">**교류** -Twitter, Facebook, Yammer 및 LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6715c-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="6715c-109">**인스턴트 메시징** -Yahoo Messenger, GoogleTalk 및 Cisco jabber</span><span class="sxs-lookup"><span data-stu-id="6715c-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="6715c-110">**문서 공동 작업** 상자 및 DropBox</span><span class="sxs-lookup"><span data-stu-id="6715c-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="6715c-111">**세로 산업** -고객 관계 관리 (예: Salesforce Chatter) 및 Financials (예:: thomson reuters 및 Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="6715c-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="6715c-112">**SMS/텍스트 메시징** -BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6715c-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="6715c-p103">타사 데이터를 가져온 후에는이 데이터에 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사 및 office 365 보존 정책 등의 office 365 준수 기능을 적용할 수 있습니다. 예를 들어 사서함이 소송 보존 상태로 설정 되 면 타사 데이터가 보존 됩니다. 콘텐츠 검색을 사용 하 여 타사 데이터를 검색할 수 있습니다. 또는 Microsoft 데이터의 경우와 마찬가지로 보관 및 보존 정책을 타사 데이터에 적용할 수도 있습니다. 간단히 말해서 Office 365에서 타사 데이터를 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="6715c-118">타사 데이터를 Office 365로 가져오는 데 필요한 프로세스 및 단계의 개요는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="6715c-119">1단계: 타사 데이터 파트너 찾기</span><span class="sxs-lookup"><span data-stu-id="6715c-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="6715c-120">2단계: Office 365에서 타사 데이터 사서함 만들기 및 구성</span><span class="sxs-lookup"><span data-stu-id="6715c-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="6715c-121">3단계: 타사 데이터에 대한 사용자 사서함 구성</span><span class="sxs-lookup"><span data-stu-id="6715c-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="6715c-122">4단계: 파트너에게 정보 제공</span><span class="sxs-lookup"><span data-stu-id="6715c-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="6715c-123">5 단계: Azure Active Directory에서 타사 데이터 커넥터 등록</span><span class="sxs-lookup"><span data-stu-id="6715c-123">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="6715c-124">타사 데이터 가져오기 프로세스의 works></span><span class="sxs-lookup"><span data-stu-id="6715c-124">How the third-party data import process works></span></span>

<span data-ttu-id="6715c-125">다음 그림과 설명은 타사 데이터 가져오기 프로세스의 작동 방식에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-125">The following illustration and description explain how the third-party data import process works.</span></span>
  
![타사 데이터 가져오기 프로세스의 작동 방식](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="6715c-127">고객은 선택한 파트너와 함께 작업 하 여 타사 데이터 원본에서 항목을 추출 하 고 해당 항목을 Office 365로 가져오는 커넥터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-127">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="6715c-p104">파트너 커넥터가 타사 API (예약 또는 구성 된 기준)를 통해 타사 데이터 원본에 연결 하 고 데이터 원본에서 항목을 추출 합니다. 파트너 커넥터는 항목의 콘텐츠를 전자 메일 메시지 형식으로 변환 합니다. 메시지 형식 스키마에 대 한 [자세한 내용은 More information](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6715c-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="6715c-131">파트너 커넥터는 잘 알려진 끝점을 통해 EWS (Exchange 웹 서비스)를 사용 하 여 Office 365의 Azure 서비스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-131">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="6715c-p105">항목은 특정 사용자의 사서함 또는 "범용" 타사 데이터 사서함으로 가져오기됩니다. 항목을 특정 사용자 사서함으로 가져올지 또는 타사 데이터 사서함으로 가져올지는 다음 기준을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="6715c-p106">a: **office 365 사용자 계정에 해당 하는 사용자 id** 가 있는 항목-파트너 커넥터가 타사 데이터 원본 항목의 사용자 id를 Office 365의 특정 사용자 id에 매핑할 수 있는 경우 해당 항목은 사용자의 **제거** 폴더에 복사 됩니다. 복구 가능한 항목 폴더 사용자가 제거 폴더의 항목에 액세스할 수 없습니다. 그러나 Office 365 eDiscovery 도구를 사용 하 여 제거 폴더에서 항목을 검색할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="6715c-p107">b. **office 365 사용자 계정에 해당 하는 사용자 id** 가 없는 항목-파트너 커넥터가 항목의 사용자 id를 office 365의 특정 사용자 id에 매핑할 수 없는 경우 항목은 타사 데이터 사서함의 **받은 편지함** 폴더에 복사 됩니다. 항목을 받은 편지 함으로 가져오면 조직의 사용자가 타사 사서함에 로그인 하 여 이러한 항목을 보고 관리 하 고 파트너 커넥터 구성에서 조정 해야 하는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="6715c-141">1단계: 타사 데이터 파트너 찾기</span><span class="sxs-lookup"><span data-stu-id="6715c-141">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="6715c-p108">office 365에서 타사 데이터를 보관 하기 위한 주요 구성 요소는 타사 데이터 원본에서 데이터를 캡처하고 office 365로 가져오는 Microsoft 파트너를 찾고 사용 하는 것입니다. 데이터를 가져온 후에는 조직의 다른 Microsoft 데이터 (예: Exchange의 전자 메일, SharePoint의 문서 및 비즈니스용 OneDrive)와 함께 보관 하 고 보존할 수 있습니다. 파트너는 조직의 타사 데이터 원본 (예: BlackBerry, Facebook, Google +,: thomson reuters, Twitter)에서 데이터를 추출 하는 커넥터를 만들고 해당 데이터를 Exchange 사서함으로 항목을 가져오는 Office 365 API에 전달 합니다. 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="6715c-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="6715c-145">다음 섹션에서는 Office 365에서 타사 데이터를 보관 하기 위한 프로그램에 참여 하는 Microsoft 파트너 및 지원 되는 타사 데이터 원본에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-145">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="6715c-146">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="6715c-146">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="6715c-147">Actiance</span><span class="sxs-lookup"><span data-stu-id="6715c-147">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="6715c-148">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="6715c-148">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="6715c-149">Globanet</span><span class="sxs-lookup"><span data-stu-id="6715c-149">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="6715c-150">OpenText</span><span class="sxs-lookup"><span data-stu-id="6715c-150">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="6715c-151">Verba</span><span class="sxs-lookup"><span data-stu-id="6715c-151">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="6715c-152">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="6715c-152">17a-4 LLC</span></span>

<span data-ttu-id="6715c-153">17a-4 LLC에서는 다음의 타사 데이터 원본을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-153">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="6715c-154">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6715c-154">BlackBerry</span></span>
    
- <span data-ttu-id="6715c-155">Bloomberg Data Streams</span><span class="sxs-lookup"><span data-stu-id="6715c-155">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="6715c-156">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="6715c-156">Cisco Jabber</span></span>
    
- <span data-ttu-id="6715c-157">FactSet</span><span class="sxs-lookup"><span data-stu-id="6715c-157">FactSet</span></span>
    
- <span data-ttu-id="6715c-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="6715c-158">HipChat</span></span>
    
- <span data-ttu-id="6715c-159">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="6715c-159">InvestEdge</span></span>
    
- <span data-ttu-id="6715c-160">LivePerson</span><span class="sxs-lookup"><span data-stu-id="6715c-160">LivePerson</span></span>
    
- <span data-ttu-id="6715c-161">
MessageLabs Data Streams
</span><span class="sxs-lookup"><span data-stu-id="6715c-161">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="6715c-162">OpenText</span><span class="sxs-lookup"><span data-stu-id="6715c-162">OpenText</span></span>
    
- <span data-ttu-id="6715c-163">Oracle/ATG 'click-to-call' Live Help
</span><span class="sxs-lookup"><span data-stu-id="6715c-163">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="6715c-164">Pivot IMTRADER
</span><span class="sxs-lookup"><span data-stu-id="6715c-164">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="6715c-165">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="6715c-165">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="6715c-166">MindAlign</span><span class="sxs-lookup"><span data-stu-id="6715c-166">MindAlign</span></span>
    
- <span data-ttu-id="6715c-167">Sitrion One(Newsgator)</span><span class="sxs-lookup"><span data-stu-id="6715c-167">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="6715c-168">
비즈니스용 Skype(Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="6715c-168">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="6715c-169">
비즈니스용 Skype Online(Lync Online)
</span><span class="sxs-lookup"><span data-stu-id="6715c-169">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="6715c-170">SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="6715c-170">SQL Databases</span></span>
    
- <span data-ttu-id="6715c-171">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="6715c-171">Squawker</span></span>
    
- <span data-ttu-id="6715c-172">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="6715c-172">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="6715c-173">Actiance</span><span class="sxs-lookup"><span data-stu-id="6715c-173">Actiance</span></span>

<span data-ttu-id="6715c-174">[Actiance](https://www.actiance.com) 에서는 다음의 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-174">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6715c-175">AIM</span><span class="sxs-lookup"><span data-stu-id="6715c-175">AIM</span></span>
    
- <span data-ttu-id="6715c-176">American Idol</span><span class="sxs-lookup"><span data-stu-id="6715c-176">American Idol</span></span>
    
- <span data-ttu-id="6715c-177">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="6715c-177">Apple Juice</span></span>
    
- <span data-ttu-id="6715c-178">
AOL with Pivot client
</span><span class="sxs-lookup"><span data-stu-id="6715c-178">AOL with Pivot client</span></span>
    
- <span data-ttu-id="6715c-179">Ares</span><span class="sxs-lookup"><span data-stu-id="6715c-179">Ares</span></span>
    
- <span data-ttu-id="6715c-180">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="6715c-180">Bazaar Voice</span></span>
    
- <span data-ttu-id="6715c-181">Bear Share</span><span class="sxs-lookup"><span data-stu-id="6715c-181">Bear Share</span></span>
    
- <span data-ttu-id="6715c-182">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="6715c-182">Bit Torrent</span></span>
    
- <span data-ttu-id="6715c-183">BlackBerry Call Logs(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6715c-183">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6715c-184">BlackBerry Messenger(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6715c-184">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6715c-185">BlackBerry PIN(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6715c-185">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6715c-186">BlackBerry SMS(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6715c-186">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6715c-187">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="6715c-187">Bloomberg Mail</span></span>
    
- <span data-ttu-id="6715c-188">셀 신뢰</span><span class="sxs-lookup"><span data-stu-id="6715c-188">CellTrust</span></span>
    
- <span data-ttu-id="6715c-189">Chat Import
</span><span class="sxs-lookup"><span data-stu-id="6715c-189">Chat Import</span></span>
    
- <span data-ttu-id="6715c-190">Chat Real Time Logging and Policy
</span><span class="sxs-lookup"><span data-stu-id="6715c-190">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="6715c-191">Chatter
</span><span class="sxs-lookup"><span data-stu-id="6715c-191">Chatter</span></span>
    
- <span data-ttu-id="6715c-192">Cisco IM &amp; 현재 상태 서버 (v 9.0.1, v 9.1, v 9.1.1 SU1, v10, v 10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="6715c-192">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="6715c-193">Cisco Unified Presence Server(v8.6.3, v8.6.4, v8.6.5)
</span><span class="sxs-lookup"><span data-stu-id="6715c-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="6715c-194">Collaboration Import
</span><span class="sxs-lookup"><span data-stu-id="6715c-194">Collaboration Import</span></span>
    
- <span data-ttu-id="6715c-195">Collaboration Real Time Logging
</span><span class="sxs-lookup"><span data-stu-id="6715c-195">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="6715c-196">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="6715c-196">Direct Connect</span></span>
    
- <span data-ttu-id="6715c-197">Facebook</span><span class="sxs-lookup"><span data-stu-id="6715c-197">Facebook</span></span>
    
- <span data-ttu-id="6715c-198">FactSet</span><span class="sxs-lookup"><span data-stu-id="6715c-198">FactSet</span></span>
    
- <span data-ttu-id="6715c-199">FastTrack</span><span class="sxs-lookup"><span data-stu-id="6715c-199">FastTrack</span></span>
    
- <span data-ttu-id="6715c-200">Gnutella</span><span class="sxs-lookup"><span data-stu-id="6715c-200">Gnutella</span></span>
    
- <span data-ttu-id="6715c-201">Google+
</span><span class="sxs-lookup"><span data-stu-id="6715c-201">Google+</span></span>
    
- <span data-ttu-id="6715c-202">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="6715c-202">GoToMyPC</span></span>
    
- <span data-ttu-id="6715c-203">Hopster</span><span class="sxs-lookup"><span data-stu-id="6715c-203">Hopster</span></span>
    
- <span data-ttu-id="6715c-204">HubConnex</span><span class="sxs-lookup"><span data-stu-id="6715c-204">HubConnex</span></span>
    
- <span data-ttu-id="6715c-205">IBM Connections(v3.0.1, v4.0, v4.5, v4.5 CR3, v5)
</span><span class="sxs-lookup"><span data-stu-id="6715c-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="6715c-206">IBM Connections Chat Cloud
</span><span class="sxs-lookup"><span data-stu-id="6715c-206">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="6715c-207">IBM Connections Social Cloud
</span><span class="sxs-lookup"><span data-stu-id="6715c-207">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="6715c-208">IBM SameTime Advanced 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="6715c-208">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="6715c-209">IBM SameTime Communicate 9.0
</span><span class="sxs-lookup"><span data-stu-id="6715c-209">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="6715c-210">IBM SameTime Community(v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)
</span><span class="sxs-lookup"><span data-stu-id="6715c-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="6715c-211">IBM SameTime Complete 9.0
</span><span class="sxs-lookup"><span data-stu-id="6715c-211">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="6715c-212">IBM SameTime Conference 9.0
</span><span class="sxs-lookup"><span data-stu-id="6715c-212">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="6715c-213">IBM SameTime Meeting 8.5.2 IFR1
</span><span class="sxs-lookup"><span data-stu-id="6715c-213">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="6715c-214">아이스/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="6715c-214">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="6715c-215">IM Import
</span><span class="sxs-lookup"><span data-stu-id="6715c-215">IM Import</span></span>
    
- <span data-ttu-id="6715c-216">IM Real Time Logging and Policy
</span><span class="sxs-lookup"><span data-stu-id="6715c-216">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="6715c-217">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="6715c-217">Indii Messenger</span></span>
    
- <span data-ttu-id="6715c-218">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="6715c-218">Instant Bloomberg</span></span>
    
- <span data-ttu-id="6715c-219">IRC</span><span class="sxs-lookup"><span data-stu-id="6715c-219">IRC</span></span>
    
- <span data-ttu-id="6715c-220">Jive
</span><span class="sxs-lookup"><span data-stu-id="6715c-220">Jive</span></span>
    
- <span data-ttu-id="6715c-221">Jive 6 Real Time Logging(v6, v7)
</span><span class="sxs-lookup"><span data-stu-id="6715c-221">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="6715c-222">Jive Import</span><span class="sxs-lookup"><span data-stu-id="6715c-222">Jive Import</span></span>
    
- <span data-ttu-id="6715c-223">JXTA</span><span class="sxs-lookup"><span data-stu-id="6715c-223">JXTA</span></span>
    
- <span data-ttu-id="6715c-224">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6715c-224">LinkedIn</span></span>
    
- <span data-ttu-id="6715c-225">
Microsoft Lync(2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="6715c-225">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="6715c-226">MFTP</span><span class="sxs-lookup"><span data-stu-id="6715c-226">MFTP</span></span>
    
- <span data-ttu-id="6715c-227">Microsoft Lync 2013 Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-227">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="6715c-228">Microsoft SharePoint(2010, 2013)
</span><span class="sxs-lookup"><span data-stu-id="6715c-228">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="6715c-229">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6715c-229">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="6715c-230">Microsoft UC(Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="6715c-230">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="6715c-231">MindAlign</span><span class="sxs-lookup"><span data-stu-id="6715c-231">MindAlign</span></span>
    
- <span data-ttu-id="6715c-232">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="6715c-232">Mobile Guard</span></span>
    
- <span data-ttu-id="6715c-233">MSN</span><span class="sxs-lookup"><span data-stu-id="6715c-233">MSN</span></span>
    
- <span data-ttu-id="6715c-234">My Space</span><span class="sxs-lookup"><span data-stu-id="6715c-234">My Space</span></span>
    
- <span data-ttu-id="6715c-235">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="6715c-235">NEONetwork</span></span>
    
- <span data-ttu-id="6715c-236">Office 365 Lync Dedicated
</span><span class="sxs-lookup"><span data-stu-id="6715c-236">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="6715c-237">Office 365 Shared IM
</span><span class="sxs-lookup"><span data-stu-id="6715c-237">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="6715c-238">Pinterest</span><span class="sxs-lookup"><span data-stu-id="6715c-238">Pinterest</span></span>
    
- <span data-ttu-id="6715c-239">Pivot</span><span class="sxs-lookup"><span data-stu-id="6715c-239">Pivot</span></span>
    
- <span data-ttu-id="6715c-240">QQ</span><span class="sxs-lookup"><span data-stu-id="6715c-240">QQ</span></span>
    
- <span data-ttu-id="6715c-241">비즈니스용 Skype 2015</span><span class="sxs-lookup"><span data-stu-id="6715c-241">Skype for Business 2015</span></span>
    
- <span data-ttu-id="6715c-242">SoftEther</span><span class="sxs-lookup"><span data-stu-id="6715c-242">SoftEther</span></span>
    
- <span data-ttu-id="6715c-243">Symphony
</span><span class="sxs-lookup"><span data-stu-id="6715c-243">Symphony</span></span>
    
- <span data-ttu-id="6715c-244">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="6715c-244">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="6715c-245">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="6715c-245">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="6715c-246">Tor</span><span class="sxs-lookup"><span data-stu-id="6715c-246">Tor</span></span>
    
- <span data-ttu-id="6715c-247">TTT</span><span class="sxs-lookup"><span data-stu-id="6715c-247">TTT</span></span>
    
- <span data-ttu-id="6715c-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="6715c-248">Twitter</span></span>
    
- <span data-ttu-id="6715c-249">winmx</span><span class="sxs-lookup"><span data-stu-id="6715c-249">WinMX</span></span>
    
- <span data-ttu-id="6715c-250">Winny</span><span class="sxs-lookup"><span data-stu-id="6715c-250">Winny</span></span>
    
- <span data-ttu-id="6715c-251">Yahoo
</span><span class="sxs-lookup"><span data-stu-id="6715c-251">Yahoo</span></span>
    
- <span data-ttu-id="6715c-252">Yammer</span><span class="sxs-lookup"><span data-stu-id="6715c-252">Yammer</span></span>
    
- <span data-ttu-id="6715c-253">YouTube</span><span class="sxs-lookup"><span data-stu-id="6715c-253">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="6715c-254">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="6715c-254">ArchiveSocial</span></span>

<span data-ttu-id="6715c-255">[ArchiveSocial](https://www.archivesocial.com) 에서는 다음의 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-255">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6715c-256">Facebook</span><span class="sxs-lookup"><span data-stu-id="6715c-256">Facebook</span></span>
    
- <span data-ttu-id="6715c-257">Flickr
</span><span class="sxs-lookup"><span data-stu-id="6715c-257">Flickr</span></span>
    
- <span data-ttu-id="6715c-258">Instagram
</span><span class="sxs-lookup"><span data-stu-id="6715c-258">Instagram</span></span>
    
- <span data-ttu-id="6715c-259">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6715c-259">LinkedIn</span></span>
    
- <span data-ttu-id="6715c-260">Pinterest</span><span class="sxs-lookup"><span data-stu-id="6715c-260">Pinterest</span></span>
    
- <span data-ttu-id="6715c-261">Twitter</span><span class="sxs-lookup"><span data-stu-id="6715c-261">Twitter</span></span>
    
- <span data-ttu-id="6715c-262">YouTube</span><span class="sxs-lookup"><span data-stu-id="6715c-262">YouTube</span></span>
    
- <span data-ttu-id="6715c-263">Vimeo</span><span class="sxs-lookup"><span data-stu-id="6715c-263">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="6715c-264">Globanet</span><span class="sxs-lookup"><span data-stu-id="6715c-264">Globanet</span></span>

<span data-ttu-id="6715c-265">[Globanet](https://www.globanet.com) 에서는 다음의 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-265">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6715c-266">AOL with Pivot Client </span><span class="sxs-lookup"><span data-stu-id="6715c-266">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="6715c-267">BlackBerry Call Logs(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6715c-267">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6715c-268">BlackBerry Messenger(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6715c-268">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6715c-269">BlackBerry PIN(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6715c-269">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6715c-270">BlackBerry SMS(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="6715c-270">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="6715c-271">Bloomberg Chat
</span><span class="sxs-lookup"><span data-stu-id="6715c-271">Bloomberg Chat</span></span>
    
- <span data-ttu-id="6715c-272">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="6715c-272">Bloomberg Mail</span></span>
    
- <span data-ttu-id="6715c-273">Box</span><span class="sxs-lookup"><span data-stu-id="6715c-273">Box</span></span>
    
- <span data-ttu-id="6715c-274">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="6715c-274">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="6715c-275">Cisco IM &amp; 현재 상태 서버 (v10, v 10.5.1 SU1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="6715c-275">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="6715c-276">Cisco Webex 팀</span><span class="sxs-lookup"><span data-stu-id="6715c-276">Cisco Webex Teams</span></span>

- <span data-ttu-id="6715c-277">Citrix 작업 &amp; 영역 sharefile</span><span class="sxs-lookup"><span data-stu-id="6715c-277">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="6715c-278">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="6715c-278">CrowdCompass</span></span>

- <span data-ttu-id="6715c-279">사용자 지정 구분 텍스트 파일
</span><span class="sxs-lookup"><span data-stu-id="6715c-279">Custom delimited text files</span></span>
    
- <span data-ttu-id="6715c-280">사용자 지정 XML 파일
</span><span class="sxs-lookup"><span data-stu-id="6715c-280">Custom XML files</span></span>
    
- <span data-ttu-id="6715c-281">Facebook (페이지)</span><span class="sxs-lookup"><span data-stu-id="6715c-281">Facebook (Pages)</span></span>
    
- <span data-ttu-id="6715c-282">Factset
</span><span class="sxs-lookup"><span data-stu-id="6715c-282">Factset</span></span>
    
- <span data-ttu-id="6715c-283">FXConnect</span><span class="sxs-lookup"><span data-stu-id="6715c-283">FXConnect</span></span>
    
- <span data-ttu-id="6715c-284">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="6715c-284">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="6715c-285">Jive
</span><span class="sxs-lookup"><span data-stu-id="6715c-285">Jive</span></span>
    
- <span data-ttu-id="6715c-286">Macgregor XIP
</span><span class="sxs-lookup"><span data-stu-id="6715c-286">Macgregor XIP</span></span>

- <span data-ttu-id="6715c-287">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="6715c-287">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="6715c-288">Microsoft 비즈니스용 OneDrive</span><span class="sxs-lookup"><span data-stu-id="6715c-288">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="6715c-289">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6715c-289">Microsoft Teams</span></span>
       
- <span data-ttu-id="6715c-290">Microsoft Yammer
</span><span class="sxs-lookup"><span data-stu-id="6715c-290">Microsoft Yammer</span></span>
    
- <span data-ttu-id="6715c-291">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="6715c-291">Mobile Guard</span></span>
    
- <span data-ttu-id="6715c-292">Pivot</span><span class="sxs-lookup"><span data-stu-id="6715c-292">Pivot</span></span>
    
- <span data-ttu-id="6715c-293">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="6715c-293">Salesforce Chatter</span></span>

- <span data-ttu-id="6715c-294">비즈니스용 Skype Online</span><span class="sxs-lookup"><span data-stu-id="6715c-294">Skype for Business Online</span></span>
    
- <span data-ttu-id="6715c-295">비즈니스용 Skype, 버전 2007 R2 - 2016(온-프레미스)
</span><span class="sxs-lookup"><span data-stu-id="6715c-295">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="6715c-296">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="6715c-296">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="6715c-297">Symphony
</span><span class="sxs-lookup"><span data-stu-id="6715c-297">Symphony</span></span>
    
- <span data-ttu-id="6715c-298">Thomson Reuters Eikon
</span><span class="sxs-lookup"><span data-stu-id="6715c-298">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="6715c-299">Thomson Reuters Messenger
</span><span class="sxs-lookup"><span data-stu-id="6715c-299">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="6715c-300">Thomson Reuters Dealings 3000 / FX Trading
</span><span class="sxs-lookup"><span data-stu-id="6715c-300">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="6715c-301">Twitter</span><span class="sxs-lookup"><span data-stu-id="6715c-301">Twitter</span></span>
    
- <span data-ttu-id="6715c-302">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="6715c-302">UBS Chat</span></span>
    
- <span data-ttu-id="6715c-303">YouTube</span><span class="sxs-lookup"><span data-stu-id="6715c-303">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="6715c-304">OpenText</span><span class="sxs-lookup"><span data-stu-id="6715c-304">OpenText</span></span>

<span data-ttu-id="6715c-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) 에서는 다음의 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6715c-306">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="6715c-306">Axs Encrypted</span></span>
    
- <span data-ttu-id="6715c-307">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="6715c-307">Axs Exchange</span></span>
    
- <span data-ttu-id="6715c-308">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="6715c-308">Axs Local Archive</span></span>
    
- <span data-ttu-id="6715c-309">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="6715c-309">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="6715c-310">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="6715c-310">Axs Signed</span></span>
    
- <span data-ttu-id="6715c-311">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="6715c-311">Bloomberg</span></span>
    
- <span data-ttu-id="6715c-312">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="6715c-312">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="6715c-313">Verba</span><span class="sxs-lookup"><span data-stu-id="6715c-313">Verba</span></span>

<span data-ttu-id="6715c-314">[verba](https://www.verba.com) 는 다음 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-314">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="6715c-315">Avaya Aura Video
</span><span class="sxs-lookup"><span data-stu-id="6715c-315">Avaya Aura Video</span></span>
    
- <span data-ttu-id="6715c-316">Avaya Aura Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-316">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="6715c-317">Avtec Radio
</span><span class="sxs-lookup"><span data-stu-id="6715c-317">Avtec Radio</span></span>
    
- <span data-ttu-id="6715c-318">Bosch/Telex Radio
</span><span class="sxs-lookup"><span data-stu-id="6715c-318">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="6715c-319">BroadSoft Video
</span><span class="sxs-lookup"><span data-stu-id="6715c-319">BroadSoft Video</span></span>
    
- <span data-ttu-id="6715c-320">BroadSoft Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-320">BroadSoft Voice</span></span>
    
- <span data-ttu-id="6715c-321">Centile Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-321">Centile Voice</span></span>
    
- <span data-ttu-id="6715c-322">Cisco Jabber IM
</span><span class="sxs-lookup"><span data-stu-id="6715c-322">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="6715c-323">Cisco UC Video
</span><span class="sxs-lookup"><span data-stu-id="6715c-323">Cisco UC Video</span></span>
    
- <span data-ttu-id="6715c-324">Cisco UC Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-324">Cisco UC Voice</span></span>
    
- <span data-ttu-id="6715c-325">Cisco c s p/c h i v 비디오</span><span class="sxs-lookup"><span data-stu-id="6715c-325">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="6715c-326">Cisco c s p/c h 음성</span><span class="sxs-lookup"><span data-stu-id="6715c-326">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="6715c-327">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="6715c-327">ESChat Radio</span></span>
    
- <span data-ttu-id="6715c-328">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="6715c-328">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="6715c-329">IP Trade Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-329">IP Trade Voice</span></span>
    
- <span data-ttu-id="6715c-330">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="6715c-330">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="6715c-331">Microsoft UC(Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="6715c-331">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="6715c-332">Mitel MiContact Center for Lync(prairieFyre) 
</span><span class="sxs-lookup"><span data-stu-id="6715c-332">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="6715c-333">Oracle/Acme Packet Session Border Controller Video  
</span><span class="sxs-lookup"><span data-stu-id="6715c-333">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="6715c-334">Oracle/Acme Packet Session Border Controller Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-334">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="6715c-335">Singtel Mobile Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-335">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="6715c-336">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="6715c-336">SIPREC Video</span></span>
    
-  <span data-ttu-id="6715c-337">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="6715c-337">SIPREC Voice</span></span> 
    
- <span data-ttu-id="6715c-338">비즈니스용 Skype/Lync IM
</span><span class="sxs-lookup"><span data-stu-id="6715c-338">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="6715c-339">비즈니스용 Skype/Lync Video
</span><span class="sxs-lookup"><span data-stu-id="6715c-339">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="6715c-340">비즈니스용 Skype/Lync Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-340">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="6715c-341">Speakerbus Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-341">Speakerbus Voice</span></span>
    
- <span data-ttu-id="6715c-342">Standard SIP/H.323 Video 
</span><span class="sxs-lookup"><span data-stu-id="6715c-342">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="6715c-343">Standard SIP/H.323 Voice 
</span><span class="sxs-lookup"><span data-stu-id="6715c-343">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="6715c-344">Truphone Voice
</span><span class="sxs-lookup"><span data-stu-id="6715c-344">Truphone Voice</span></span>
    
- <span data-ttu-id="6715c-345">TwistedPair Radio
</span><span class="sxs-lookup"><span data-stu-id="6715c-345">TwistedPair Radio</span></span>
    
- <span data-ttu-id="6715c-346">Windows 데스크톱 컴퓨터 화면 
</span><span class="sxs-lookup"><span data-stu-id="6715c-346">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="6715c-347">2단계: Office 365에서 타사 데이터 사서함 만들기 및 구성</span><span class="sxs-lookup"><span data-stu-id="6715c-347">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="6715c-p109">다음은 Office 365로 데이터를 가져오기 위한 타사 데이터 사서함을 만들고 구성 하는 단계입니다. 앞에서 설명한 것 처럼 파트너 커넥터에서 항목의 사용자 ID를 Office 365 사용자 계정에 매핑할 수 없는 경우에는이 사서함으로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="6715c-350">**Office 365 관리 센터에서 다음 작업 완료**</span><span class="sxs-lookup"><span data-stu-id="6715c-350">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="6715c-p110">Office 365에서 새 사용자 계정을 만들고이 계정에 Exchange Online 계획 2 라이선스를 할당 합니다. [Office 365에 사용자 추가를](https://go.microsoft.com/fwlink/p/?LinkId=692098)참조 하세요. 계획 2 라이선스는 사서함을 소송 보존 상태로 설정 하거나 저장소 할당량이 무제한 인 보관 사서함을 사용 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="6715c-353">타사 데이터 사서함에 대 한 사용자 계정을 Office 365의 **Exchange 관리자** 관리자 역할에 추가 합니다. [Office 365에서 관리자 역할 할당을](https://go.microsoft.com/fwlink/p/?LinkId=532393)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6715c-353">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="6715c-p111">이 사용자 계정의 자격 증명을 기록해 둡니다. 4단계에서 설명한 것처럼 파트너에게 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="6715c-356">**Exchange 관리 센터에서 다음 작업 완료**</span><span class="sxs-lookup"><span data-stu-id="6715c-356">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="6715c-p112">조직의 주소록 및 기타 주소 목록에서 타사 데이터 사서함을 숨깁니다. [사용자 사서함 관리](https://go.microsoft.com/fwlink/p/?LinkId=616058)를 참조 하세요. 또는 다음 PowerShell 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="6715c-359">administrators 또는 규정 준수 관리자가 Outlook 데스크톱 클라이언트에서 타사 데이터 사서함을 열 수 있도록 타사 데이터 사서함에 대 한 **FullAccess** 권한을 할당 합니다. [받는 사람의 사용 권한 관리를](https://go.microsoft.com/fwlink/p/?LinkId=692104)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6715c-359">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="6715c-360">타사 데이터 사서함에 대해 다음과 같은 준수 관련 Office 365 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-360">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="6715c-p113">보관 사서함을 사용 하도록 설정 합니다. office [365 보안 &amp; 및 준수 센터에서 보관 사서함 사용](enable-archive-mailboxes.md) 및 [office 365에서 무제한 보관 사용](enable-unlimited-archiving.md)을 참조 하세요. 이렇게 하면 타사 데이터 항목을 보관 사서함으로 이동 하는 보관 정책을 설정 하 여 기본 사서함에서 저장소 공간을 확보할 수 있습니다. 이렇게 하면 타사 데이터에 대 한 무제한 저장소를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="6715c-p114">타사 데이터 사서함을 소송 보존으로 설정 합니다. office 365 보안 &amp; 및 준수 센터에서 office 365 보존 정책을 적용할 수도 있습니다. 이 사서함을 보존 상태로 두면 타사 데이터 항목 (무기한 또는 지정 된 기간 동안)이 유지 되 고 사서함에서 해당 항목이 제거 되는 것을 방지할 수 있습니다. 다음 항목 중 하나를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6715c-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="6715c-368">사서함을 소송 자료 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="6715c-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="6715c-369">Office 365의 보존 정책 개요</span><span class="sxs-lookup"><span data-stu-id="6715c-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="6715c-p115">타사 데이터 사서함에 대 한 소유자, 대리인 및 관리자 액세스에 대 한 사서함 감사 로깅을 사용 하도록 설정 합니다. [Office 365에서 사서함 감사 사용을](enable-mailbox-auditing.md)참조 하세요. 이렇게 하면 타사 데이터 사서함에 대 한 액세스 권한이 있는 모든 사용자가 수행한 모든 작업을 감사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="6715c-372">3단계: 타사 데이터에 대한 사용자 사서함 구성</span><span class="sxs-lookup"><span data-stu-id="6715c-372">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="6715c-p116">다음 단계에서는 타사 데이터를 지원 하도록 사용자 사서함을 구성 합니다. Exchange 관리 센터를 사용 하거나 해당 Windows PowerShell cmdlet을 사용 하 여 이러한 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="6715c-375">각 사용자에 대해 보관 사서함을 사용 하도록 설정 합니다. office [365 보안 &amp; 및 준수 센터에서 보관 사서함 사용](enable-archive-mailboxes.md) 및 [office 365에서 무제한 보관 사용](enable-unlimited-archiving.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6715c-375">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="6715c-376">사용자 사서함을 소송 보존으로 설정 하거나 Office 365 보관 정책을 적용 합니다. 다음 항목 중 하나를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6715c-376">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="6715c-377">사서함을 소송 자료 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="6715c-377">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="6715c-378">Office 365의 보존 정책 개요</span><span class="sxs-lookup"><span data-stu-id="6715c-378">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="6715c-379">앞서 언급한 것처럼 사서함을 보존하면 타사 데이터 원본의 항목을 보존하는 기간을 설정하거나 항목을 무기한 보존하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-379">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="6715c-380">4단계: 파트너에게 정보 제공</span><span class="sxs-lookup"><span data-stu-id="6715c-380">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="6715c-381">마지막 단계는 Office 365 조직에 연결하여 사용자 사서함이나 타사 데이터 사서함으로 데이터를 가져오도록 커넥터를 구성할 수 있게 파트너에게 다음 정보를 제공하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-381">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="6715c-382">Office 365에서 Azure 서비스에 연결 하는 데 사용 되는 끝점:</span><span class="sxs-lookup"><span data-stu-id="6715c-382">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="6715c-p117">2 단계에서 만든 타사 데이터 사서함의 로그인 자격 증명 (Office 365 사용자 ID 및 암호)입니다. 이러한 자격 증명은 파트너 커넥터가 사용자 사서함 및 타사 데이터 사서함으로 항목에 액세스 하 고 가져올 수 있도록 하기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="6715c-385">5 단계: Azure Active Directory에서 타사 데이터 커넥터 등록</span><span class="sxs-lookup"><span data-stu-id="6715c-385">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="6715c-p118">2018 년 9 월 30 일부부터 office 365의 Azure service는 Exchange Online의 최신 인증을 사용 하 여 데이터를 가져오기 위해 office 365 조직에 연결을 시도 하는 타사 데이터 커넥터를 인증 합니다. 이러한 변경이 발생 하는 이유는 최신 인증이 이전에 설명한 끝점을 사용 하 여 Azure 서비스에 연결 하는 허용 목록이 타사 커넥터를 기반으로 하는 현재 방법 보다 더 많은 보안 기능을 제공 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p118">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data. The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="6715c-p119">최신 인증 방법을 사용 하 여 타사 데이터 커넥터가 office 365에 연결 되도록 하려면 office 365 조직의 관리자가 해당 커넥터를 Azure Active Directory의 신뢰할 수 있는 서비스 응용 프로그램으로 등록 하는 것이 동의 해야 합니다. 이 작업은 사용 권한 요청을 수락 하 여 커넥터가 Azure Active Directory에서 조직의 데이터에 액세스할 수 있도록 허용 합니다. 이 요청을 수락 하면 타사 데이터 커넥터가 엔터프라이즈 응용 프로그램으로 Azure Active Directory에 추가 되 고 서비스 사용자로 표시 됩니다. 승인 프로세스에 대 한 자세한 내용은 [테 넌 트 관리자 동의](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6715c-p119">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory. This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory. After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal. For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="6715c-392">커넥터 등록을 위한 요청에 액세스 하 고 수락 하는 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-392">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="6715c-393">[이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) 이동 하 여 Office 365 전역 관리자의 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-393">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="6715c-p120">다음 대화 상자가 표시 됩니다. carets를 확장 하 여 커넥터에 할당 되는 사용 권한을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p120">The following dialog box is displayed. You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="6715c-396">![사용 권한 요청 대화 상자가 표시 됩니다.](media/O365_ThirdPartyDataConnector_OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="6715c-396">![The permissions request dialog is displayed](media/O365_ThirdPartyDataConnector_OptIn1.png)</span></span>
2. <span data-ttu-id="6715c-397">**수락**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-397">Click **Accept**.</span></span>

<span data-ttu-id="6715c-p121">요청을 수락 하면 [Azure portal](https://portal.azure.com) 이 표시 됩니다. 조직의 응용 프로그램 목록을 보려면 **Azure Active Directory** > **Enterprise 응용 프로그램**을 클릭 합니다. Office 365 타사 데이터 커넥터가 **엔터프라이즈 응용 프로그램** 블레이드에서 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p121">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed. To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**. The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6715c-p122">Azure Active Directory에 타사 데이터 커넥터를 등록 하지 않으면, 2018 년 9 월 30 일 이후에는 타사 데이터를 조직의 사서함으로 가져올 수 없게 됩니다. 참고 5 단계에 나와 있는 절차에 따라 기존 타사 데이터 커넥터 (9 월 30 일 이전에는 2018)도 Azure Active Directory에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p122">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory. Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="6715c-403">타사 데이터 커넥터에 대 한 동의 해지</span><span class="sxs-lookup"><span data-stu-id="6715c-403">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="6715c-p123">조직이 Azure Active Directory에서 타사 데이터 커넥터를 등록 하기 위해 권한 요청을 consents 후에는 조직에서 언제 든 지 해당 동의를 해지할 수 있습니다. 그러나 커넥터에 대 한 동의를 취소 하면 타사 데이터 원본의 데이터를 더 이상 Office 365로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p123">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time. However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="6715c-p124">타사 데이터 커넥터에 대 한 동의를 해지 하려면 azure portal에서 **엔터프라이즈 응용 프로그램** 블레이드를 사용 하 여 azure Active Directory에서 해당 서비스 사용자를 삭제 하거나, 다음을 [사용 하 여 응용 프로그램을 삭제 하면 됩니다. Remove-(new-msolserviceprincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. Azure Active Directory PowerShell에서 [AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p124">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="6715c-408">추가 정보</span><span class="sxs-lookup"><span data-stu-id="6715c-408">More information</span></span>

- <span data-ttu-id="6715c-p125">앞에서 설명한 것 처럼 타사 데이터 원본의 항목은 Exchange 사서함에 전자 메일 메시지로 가져오게 됩니다. 파트너 커넥터는 Office 365 API에 필요한 스키마를 사용 하 여 항목을 가져옵니다. 다음 표에는 Exchange 사서함에 전자 메일 메시지로 가져온 후 타사 데이터 원본에서 항목의 메시지 속성에 대 한 설명이 나와 있습니다. 이 표에는 message 속성이 필수 인지 여부도 표시 됩니다. 필수 속성을 채워야 합니다. 항목에 필수 속성이 없는 경우에는 Office 365로 가져올 수 없습니다. 가져오기 프로세스에서는 항목을 가져오지 못한 이유와 해당 속성을 누락 하는 이유를 설명 하는 오류 메시지가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p125">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="6715c-416">**메시지 속성**</span><span class="sxs-lookup"><span data-stu-id="6715c-416">**Message property**</span></span>|<span data-ttu-id="6715c-417">**강제?**</span><span class="sxs-lookup"><span data-stu-id="6715c-417">**Mandatory?**</span></span>|<span data-ttu-id="6715c-418">**설명**</span><span class="sxs-lookup"><span data-stu-id="6715c-418">**Description**</span></span>|<span data-ttu-id="6715c-419">**예제 값**</span><span class="sxs-lookup"><span data-stu-id="6715c-419">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6715c-420">**FROM**</span><span class="sxs-lookup"><span data-stu-id="6715c-420">**FROM**</span></span> <br/> |<span data-ttu-id="6715c-421">예</span><span class="sxs-lookup"><span data-stu-id="6715c-421">Yes</span></span>  <br/> |<span data-ttu-id="6715c-p126">타사 데이터 원본에서 처음으로 항목을 만들었거나 보낸 사용자입니다. 파트너 커넥터는 원본 항목 (예: Twitter 핸들)의 사용자 ID를 모든 참가자 (시작 및 대상 필드의 사용자)에 대 한 Office 365 사용자 계정에 매핑하도록 시도 합니다. 메시지 복사본은 모든 참가자의 사서함으로 가져옵니다. 항목의 참가자가 office 365 사용자 계정에 매핑할 수 없는 경우에는 office 365에서 타사 보관 사서함으로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p126">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="6715c-p127">항목을 보낸 사람으로 식별 된 참석자는 해당 항목을 가져올 Office 365 조직의 활성 사서함이 있어야 합니다. 보낸 사람에 게 활성 사서함이 없으면 다음 오류가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p127">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="6715c-428">**TO**</span><span class="sxs-lookup"><span data-stu-id="6715c-428">**TO**</span></span> <br/> |<span data-ttu-id="6715c-429">예</span><span class="sxs-lookup"><span data-stu-id="6715c-429">Yes</span></span>  <br/> |<span data-ttu-id="6715c-430">데이터 원본의 항목을 받은 사람입니다(해당되는 경우).</span><span class="sxs-lookup"><span data-stu-id="6715c-430">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="6715c-431">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="6715c-431">**SUBJECT**</span></span> <br/> |<span data-ttu-id="6715c-432">아니요</span><span class="sxs-lookup"><span data-stu-id="6715c-432">No</span></span>  <br/> |<span data-ttu-id="6715c-433">원본 항목의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-433">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="6715c-434">**종료일**</span><span class="sxs-lookup"><span data-stu-id="6715c-434">**DATE**</span></span> <br/> |<span data-ttu-id="6715c-435">예</span><span class="sxs-lookup"><span data-stu-id="6715c-435">Yes</span></span>  <br/> |<span data-ttu-id="6715c-436">항목을 처음 만들었거나 고객 데이터 원본에 게시한 날짜입니다. 예로 Twitter 메시지가 트윗된 날짜가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-436">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="6715c-437">**BODY**</span><span class="sxs-lookup"><span data-stu-id="6715c-437">**BODY**</span></span> <br/> |<span data-ttu-id="6715c-438">아니요</span><span class="sxs-lookup"><span data-stu-id="6715c-438">No</span></span>  <br/> |<span data-ttu-id="6715c-p128">메시지 또는 게시물의 내용입니다. 일부 데이터 원본의 경우이 속성의 내용은 **SUBJECT** 속성의 내용과 같을 수 있습니다. 가져오기 프로세스 중에 파트너 커넥터는 가능한 한 콘텐츠 원본에서 전체 충실도를 유지 관리 합니다. 가능 하면 원본 항목의 본문에 있는 파일, 그래픽 또는 기타 콘텐츠가이 속성에 포함 됩니다. 그렇지 않으면 원본 항목의 콘텐츠가 **ATTACHMENT** 속성에 포함 됩니다. 이 속성의 내용은 파트너 커넥터와 원본 플랫폼의 기능에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p128">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="6715c-445">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="6715c-445">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="6715c-446">아니요</span><span class="sxs-lookup"><span data-stu-id="6715c-446">No</span></span>  <br/> |<span data-ttu-id="6715c-p129">데이터 원본의 항목 (예: Twitter 또는 인스턴트 메시징 대화에 있는 tweet)에 첨부 된 파일이 있거나 이미지를 포함 하는 경우, 파트너 연결에서는 먼저 **BODY** 속성에 첨부 파일을 포함 하 려 합니다. 이것이 가능 하지 않으면 \* \* ATTACHMENT \* \* 속성에 추가 됩니다. 첨부 파일의 기타 예로는 Facebook의 좋아요, 콘텐츠 원본의 메타 데이터, 메시지 또는 게시물에 대 한 응답 등이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p129">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="6715c-450">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="6715c-450">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="6715c-451">예</span><span class="sxs-lookup"><span data-stu-id="6715c-451">Yes</span></span>  <br/> | <span data-ttu-id="6715c-p130">이 속성은 파트너 커넥터에서 생성 되 고 채워지는 다중 값 등록 방법입니다. 이 속성의 형식은 `IPM.NOTE.Source.Event`입니다. (이 속성은 다음으로 `IPM.NOTE`시작 해야 합니다 .이 형식은 `IPM.NOTE.X` message 클래스의 형식과 유사 합니다.) 이 속성에는 다음 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p130">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="6715c-455">`Source`-타사 데이터 원본을 나타냅니다. 예: Twitter, Facebook 또는 BlackBerry를 예로 들 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-455">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="6715c-p131">`Event`-항목을 생성 한 타사 데이터 원본에서 수행한 작업 유형을 나타냅니다. 예를 들어, Twitter에 있는 tweet 또는 Facebook의 게시물입니다. 이벤트는 데이터 원본에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p131">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="6715c-p132">이 속성의 용도 중 하나는 항목이 시작 된 위치 또는 이벤트 형식을 기반으로 하는 데이터 원본에 따라 특정 항목을 필터링 하는 것입니다. 예를 들어 eDiscovery 검색에서는 특정 사용자가 게시 한 모든 트 윗를 찾기 위한 검색 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p132">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="6715c-p133">Office 365에서 사서함에 항목을 성공적으로 가져오면 고유한 식별자가 HTTP 응답의 일부로 다시 발신자에 게 반환 됩니다. 이 식별자 `x-IngestionCorrelationID`는 종단 간 항목 추적을 위해 파트너가 제공 하는 후속 문제 해결을 위해 사용 될 수 있습니다. 파트너가이 정보를 캡처하고 그에 따라 끝에 기록 하는 것이 좋습니다. 다음은이 식별자를 보여 주는 HTTP 응답의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p133">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="6715c-p134">office 365 보안 &amp; 및 준수 센터의 콘텐츠 검색 도구를 사용 하 여 타사 데이터 원본에서 office 365의 사서함으로 가져온 항목을 검색할 수 있습니다. 이러한 가져온 항목을 구체적으로 검색 하려면 콘텐츠 검색의 키워드 상자에 다음과 같은 메시지 속성-값 쌍을 사용할 수 있습니다. .</span><span class="sxs-lookup"><span data-stu-id="6715c-p134">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="6715c-p135">**`kind:externaldata`**-이 속성-값 쌍을 사용 하 여 모든 타사 데이터 형식을 검색 합니다. 예를 들어 타사 데이터 원본에서 가져온 항목과 가져온 항목의 Subject 속성에 "contoso" 라는 단어가 포함 된 항목을 검색 하려면 keyword 쿼리 `kind:externaldata AND subject:contoso`를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p135">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="6715c-p136">**`itemclass:ipm.externaldata.<third-party data type>`**-이 속성-값 쌍을 사용 하 여 지정 된 타사 데이터 형식만 검색 합니다. 예를 들어 Subject 속성에서 "contoso" 라는 단어가 포함 된 Facebook 데이터만 검색 하려면 keyword 쿼리 `itemclass:ipm.externaldata.Facebook* AND subject:contoso`를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6715c-p136">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="6715c-471">`itemclass` 속성의 타사 데이터 형식에 사용할 값의 전체 목록은 [Office 365로 가져온 타사 데이터 검색을 사용 하 여 콘텐츠 검색](use-content-search-to-search-third-party-data-that-was-imported.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6715c-471">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="6715c-472">콘텐츠 검색 사용 및 키워드 검색 쿼리를 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6715c-472">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="6715c-473">Office 365의 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="6715c-473">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="6715c-474">콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건</span><span class="sxs-lookup"><span data-stu-id="6715c-474">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
