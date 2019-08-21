---
title: Office 365에서 파트너와 협력 하 여 타사 데이터 보관
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 조직에서 Microsoft 파트너와 협력 하 여 Salesforce Chatter, Yahoo Messenger 또는 Yammer와 같은 데이터 원본의 타사 데이터를 가져올 사용자 지정 커넥터를 설정할 수 있습니다. 이를 통해 Office 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 Office 365 규정 준수 기능을 사용 하 여 조직의 타사 데이터를 관리 하는 방법을 관리할 수도 있습니다.
ms.openlocfilehash: a22b4226efb582969072bbd92149080cca9b749c
ms.sourcegitcommit: 59039d3bf479c4b2c1d2e2556a0adc755f431a1f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2019
ms.locfileid: "36473428"
---
# <a name="work-with-a-partner-to-archive-third-party-data-in-office-365"></a><span data-ttu-id="cd6a2-104">Office 365에서 파트너와 협력 하 여 타사 데이터 보관</span><span class="sxs-lookup"><span data-stu-id="cd6a2-104">Work with a partner to archive third-party data in Office 365</span></span>

<span data-ttu-id="cd6a2-105">Microsoft 파트너와 협력 하 여 타사 데이터 원본의 데이터를 가져와 Office 365에 보관할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-105">You can work with a Microsoft Partner to import and archive data from a third-party data source to Office 365.</span></span> <span data-ttu-id="cd6a2-106">파트너는 타사 데이터 원본에서 정기적으로 항목을 추출 하 고 해당 항목을 Office 365로 가져오는 사용자 지정 커넥터를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-106">A partner can provide you with a custom connector that is configured to extract items from the third-party data source (on a regular basis) and then import those items to Office 365.</span></span> <span data-ttu-id="cd6a2-107">파트너 커넥터는 항목의 콘텐츠를 데이터 원본에서 전자 메일 메시지 형식으로 변환한 다음 Office 365에서 사서함에 항목을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-107">The partner connector converts the content of an item from the data source to an email message format and then stores the items in mailboxes in Office 365.</span></span> <span data-ttu-id="cd6a2-108">타사 데이터를 가져온 후에는이 데이터에 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사 및 Office 365 고정 정책과 같은 Office 365 준수 기능을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-108">After third-party data is imported, you can apply Office 365 compliance features such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies to this data.</span></span>
  
<span data-ttu-id="cd6a2-109">타사 데이터를 Office 365로 가져오기 위해 Microsoft 파트너와 함께 작업 하는 데 필요한 프로세스 및 단계의 개요는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-109">Here's an overview of the process and the steps necessary to work with a Microsoft Partner to import third-party data to Office 365.</span></span>

[<span data-ttu-id="cd6a2-110">Step 1: Find a third-party data partner</span><span class="sxs-lookup"><span data-stu-id="cd6a2-110">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="cd6a2-111">Step 2: Create and configure a third-party data mailbox in Office 365</span><span class="sxs-lookup"><span data-stu-id="cd6a2-111">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="cd6a2-112">Step 3: Configure user mailboxes for third-party data</span><span class="sxs-lookup"><span data-stu-id="cd6a2-112">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="cd6a2-113">4단계: 파트너에게 정보 제공</span><span class="sxs-lookup"><span data-stu-id="cd6a2-113">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="cd6a2-114">5 단계: Azure Active Directory에서 타사 데이터 커넥터 등록</span><span class="sxs-lookup"><span data-stu-id="cd6a2-114">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="cd6a2-115">타사 데이터 가져오기 프로세스의 작동 방식</span><span class="sxs-lookup"><span data-stu-id="cd6a2-115">How the third-party data import process works</span></span>

<span data-ttu-id="cd6a2-116">다음 그림 및 설명은 파트너와 함께 작업 하는 경우 타사 데이터 가져오기 프로세스의 작동 방식에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-116">The following illustration and description explain how the third-party data import process works when working with a partner.</span></span>
  
![타사 데이터 가져오기 프로세스의 작동 방식](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="cd6a2-118">고객은 선택한 파트너와 함께 작업 하 여 타사 데이터 원본에서 항목을 추출 하 고 해당 항목을 Office 365로 가져오는 커넥터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-118">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="cd6a2-119">파트너 커넥터가 타사 API (예약 또는 구성 된 기준)를 통해 타사 데이터 원본에 연결 하 고 데이터 원본에서 항목을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-119">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source.</span></span> <span data-ttu-id="cd6a2-120">파트너 커넥터는 항목의 내용을 전자 메일 메시지 형식으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-120">The partner connector converts the content of an item to an email message format.</span></span> <span data-ttu-id="cd6a2-121">메시지 형식 스키마에 대 한 [자세한 내용은 More information](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-121">See the [More information](#more-information) section for a description of the message-format schema.</span></span> 
    
3. <span data-ttu-id="cd6a2-122">파트너 커넥터는 잘 알려진 끝점을 통해 EWS (Exchange 웹 서비스)를 사용 하 여 Office 365의 Azure 서비스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-122">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="cd6a2-p104">항목은 특정 사용자의 사서함 또는 "범용" 타사 데이터 사서함으로 가져오기됩니다. 항목을 특정 사용자 사서함으로 가져올지 또는 타사 데이터 사서함으로 가져올지는 다음 기준을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-p104">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="cd6a2-125">위한.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-125">a.</span></span> <span data-ttu-id="cd6a2-126">**Office 365 사용자 계정에 해당 하는 사용자 ID가 있는 항목:** 파트너 커넥터가 타사 데이터 원본 항목의 사용자 ID를 Office 365의 특정 사용자 ID에 매핑할 수 있는 경우 해당 항목은 사용자의 복구 가능한 항목 폴더에 있는 **제거** 폴더에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-126">**Items that have a user ID that corresponds to an Office 365 user account:** If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder.</span></span> <span data-ttu-id="cd6a2-127">제거 폴더의 항목에는 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-127">Users can't access items in the Purges folder.</span></span> <span data-ttu-id="cd6a2-128">그러나 Office 365 eDiscovery 도구를 사용 하 여 제거 폴더에서 항목을 검색할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-128">However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="cd6a2-129">b.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-129">b.</span></span> <span data-ttu-id="cd6a2-130">**Office 365 사용자 계정에 해당 하는 사용자 ID가 없는 항목:** 파트너 커넥터가 항목의 사용자 ID를 Office 365의 특정 사용자 ID에 매핑할 수 없는 경우 항목은 타사 데이터 사서함의 **받은 편지함** 폴더에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-130">**Items that don't have a user ID that corresponds to an Office 365 user account:** If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox.</span></span> <span data-ttu-id="cd6a2-131">받은 편지함에 항목을 가져올 수 있으면 관리자 또는 조직의 누군가가 타사 사서함에 로그인하여 이러한 항목을 보고 관리할 수 있으며 파트너 커넥터 구성을 조정해야 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-131">Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="cd6a2-132">1단계: 타사 데이터 파트너 찾기</span><span class="sxs-lookup"><span data-stu-id="cd6a2-132">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="cd6a2-133">Office 365에서 타사 데이터를 보관 하기 위한 주요 구성 요소는 타사 데이터 원본에서 데이터를 캡처하고 Office 365로 가져오는 Microsoft 파트너를 찾고 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-133">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365.</span></span> <span data-ttu-id="cd6a2-134">데이터를 가져온 후에는 조직의 다른 Microsoft 데이터 (예: Exchange의 전자 메일, SharePoint의 문서 및 비즈니스용 OneDrive)와 함께 보관 하 고 보존할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-134">After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business.</span></span> <span data-ttu-id="cd6a2-135">파트너는 조직의 타사 데이터 원본 (예: BlackBerry, Facebook, Google +,: Thomson Reuters, Twitter)에서 데이터를 추출 하는 커넥터를 만들고 해당 데이터를 Exchange 사서함으로 항목을 가져오는 Office 365 API에 전달 합니다. 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="cd6a2-135">A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="cd6a2-136">다음 섹션에는 Office 365에서 타사 데이터를 보관 하기 위한 프로그램에 참여 하는 Microsoft 파트너 (지원 되는 타사 데이터 원본)이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-136">The following sections list the Microsoft partners (and the third-party data sources they support) that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="cd6a2-137">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="cd6a2-137">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="cd6a2-138">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="cd6a2-138">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="cd6a2-139">Globanet</span><span class="sxs-lookup"><span data-stu-id="cd6a2-139">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="cd6a2-140">OpenText</span><span class="sxs-lookup"><span data-stu-id="cd6a2-140">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="cd6a2-141">Smarsh</span><span class="sxs-lookup"><span data-stu-id="cd6a2-141">Smarsh</span></span>](#smarsh)

[<span data-ttu-id="cd6a2-142">Verba</span><span class="sxs-lookup"><span data-stu-id="cd6a2-142">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="cd6a2-143">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="cd6a2-143">17a-4 LLC</span></span>

<span data-ttu-id="cd6a2-144">[17a-4 LLC](https://www.17a-4.com) 에서는 다음 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-144">[17a-4 LLC](https://www.17a-4.com) supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="cd6a2-145">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="cd6a2-145">BlackBerry</span></span>
    
- <span data-ttu-id="cd6a2-146">Bloomberg Data Streams</span><span class="sxs-lookup"><span data-stu-id="cd6a2-146">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="cd6a2-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="cd6a2-147">Cisco Jabber</span></span>
    
- <span data-ttu-id="cd6a2-148">FactSet</span><span class="sxs-lookup"><span data-stu-id="cd6a2-148">FactSet</span></span>
    
- <span data-ttu-id="cd6a2-149">HipChat</span><span class="sxs-lookup"><span data-stu-id="cd6a2-149">HipChat</span></span>
    
- <span data-ttu-id="cd6a2-150">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="cd6a2-150">InvestEdge</span></span>
    
- <span data-ttu-id="cd6a2-151">LivePerson</span><span class="sxs-lookup"><span data-stu-id="cd6a2-151">LivePerson</span></span>
    
- <span data-ttu-id="cd6a2-152">MessageLabs Data Streams</span><span class="sxs-lookup"><span data-stu-id="cd6a2-152">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="cd6a2-153">OpenText</span><span class="sxs-lookup"><span data-stu-id="cd6a2-153">OpenText</span></span>
    
- <span data-ttu-id="cd6a2-154">Oracle/ATG 'click-to-call' Live Help</span><span class="sxs-lookup"><span data-stu-id="cd6a2-154">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="cd6a2-155">Pivot IMTRADER</span><span class="sxs-lookup"><span data-stu-id="cd6a2-155">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="cd6a2-156">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="cd6a2-156">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="cd6a2-157">MindAlign</span><span class="sxs-lookup"><span data-stu-id="cd6a2-157">MindAlign</span></span>
    
- <span data-ttu-id="cd6a2-158">Sitrion One(Newsgator)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-158">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="cd6a2-159">비즈니스용 Skype(Lync/OCS)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-159">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="cd6a2-160">비즈니스용 Skype Online(Lync Online)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-160">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="cd6a2-161">SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="cd6a2-161">SQL Databases</span></span>
    
- <span data-ttu-id="cd6a2-162">Squawker</span><span class="sxs-lookup"><span data-stu-id="cd6a2-162">Squawker</span></span>
    
- <span data-ttu-id="cd6a2-163">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="cd6a2-163">Thomson Reuters Eikon Messenger</span></span>
  

  
### <a name="archivesocial"></a><span data-ttu-id="cd6a2-164">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="cd6a2-164">ArchiveSocial</span></span>

<span data-ttu-id="cd6a2-165">[ArchiveSocial](https://www.archivesocial.com) 에서는 다음의 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-165">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="cd6a2-166">Facebook</span><span class="sxs-lookup"><span data-stu-id="cd6a2-166">Facebook</span></span>
    
- <span data-ttu-id="cd6a2-167">Flickr</span><span class="sxs-lookup"><span data-stu-id="cd6a2-167">Flickr</span></span>
    
- <span data-ttu-id="cd6a2-168">명령이 있는 agram</span><span class="sxs-lookup"><span data-stu-id="cd6a2-168">Instagram</span></span>
    
- <span data-ttu-id="cd6a2-169">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="cd6a2-169">LinkedIn</span></span>
    
- <span data-ttu-id="cd6a2-170">유 이율</span><span class="sxs-lookup"><span data-stu-id="cd6a2-170">Pinterest</span></span>
    
- <span data-ttu-id="cd6a2-171">Twitter</span><span class="sxs-lookup"><span data-stu-id="cd6a2-171">Twitter</span></span>
    
- <span data-ttu-id="cd6a2-172">YouTube</span><span class="sxs-lookup"><span data-stu-id="cd6a2-172">YouTube</span></span>
    
- <span data-ttu-id="cd6a2-173">Vimeo</span><span class="sxs-lookup"><span data-stu-id="cd6a2-173">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="cd6a2-174">Globanet</span><span class="sxs-lookup"><span data-stu-id="cd6a2-174">Globanet</span></span>

<span data-ttu-id="cd6a2-175">[Globanet](https://www.globanet.com) 에서는 다음의 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-175">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="cd6a2-176">AOL with Pivot Client </span><span class="sxs-lookup"><span data-stu-id="cd6a2-176">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="cd6a2-177">BlackBerry Call Logs(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-177">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="cd6a2-178">BlackBerry Messenger(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-178">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="cd6a2-179">BlackBerry PIN(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-179">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="cd6a2-180">BlackBerry SMS(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-180">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="cd6a2-181">Bloomberg Chat</span><span class="sxs-lookup"><span data-stu-id="cd6a2-181">Bloomberg Chat</span></span>
    
- <span data-ttu-id="cd6a2-182">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="cd6a2-182">Bloomberg Mail</span></span>
    
- <span data-ttu-id="cd6a2-183">Box</span><span class="sxs-lookup"><span data-stu-id="cd6a2-183">Box</span></span>
    
- <span data-ttu-id="cd6a2-184">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="cd6a2-184">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="cd6a2-185">Cisco IM &amp; 현재 상태 서버 (v10, v 10.5.1 SU1, v 11.0, v 11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-185">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="cd6a2-186">Cisco Webex 팀</span><span class="sxs-lookup"><span data-stu-id="cd6a2-186">Cisco Webex Teams</span></span>

- <span data-ttu-id="cd6a2-187">Citrix 작업 &amp; 영역 sharefile</span><span class="sxs-lookup"><span data-stu-id="cd6a2-187">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="cd6a2-188">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="cd6a2-188">CrowdCompass</span></span>

- <span data-ttu-id="cd6a2-189">사용자 지정 구분 텍스트 파일</span><span class="sxs-lookup"><span data-stu-id="cd6a2-189">Custom-delimited text files</span></span>
    
- <span data-ttu-id="cd6a2-190">사용자 지정 XML 파일</span><span class="sxs-lookup"><span data-stu-id="cd6a2-190">Custom XML files</span></span>
    
- <span data-ttu-id="cd6a2-191">Facebook (페이지)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-191">Facebook (Pages)</span></span>
    
- <span data-ttu-id="cd6a2-192">Factset</span><span class="sxs-lookup"><span data-stu-id="cd6a2-192">Factset</span></span>
    
- <span data-ttu-id="cd6a2-193">FXConnect</span><span class="sxs-lookup"><span data-stu-id="cd6a2-193">FXConnect</span></span>
    
- <span data-ttu-id="cd6a2-194">ICE Chat/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="cd6a2-194">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="cd6a2-195">Jive</span><span class="sxs-lookup"><span data-stu-id="cd6a2-195">Jive</span></span>
    
- <span data-ttu-id="cd6a2-196">Macgregor XIP</span><span class="sxs-lookup"><span data-stu-id="cd6a2-196">Macgregor XIP</span></span>

- <span data-ttu-id="cd6a2-197">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="cd6a2-197">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="cd6a2-198">Microsoft 비즈니스용 OneDrive</span><span class="sxs-lookup"><span data-stu-id="cd6a2-198">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="cd6a2-199">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cd6a2-199">Microsoft Teams</span></span>
       
- <span data-ttu-id="cd6a2-200">Microsoft Yammer</span><span class="sxs-lookup"><span data-stu-id="cd6a2-200">Microsoft Yammer</span></span>
    
- <span data-ttu-id="cd6a2-201">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="cd6a2-201">Mobile Guard</span></span>
    
- <span data-ttu-id="cd6a2-202">Pivot</span><span class="sxs-lookup"><span data-stu-id="cd6a2-202">Pivot</span></span>
    
- <span data-ttu-id="cd6a2-203">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="cd6a2-203">Salesforce Chatter</span></span>

- <span data-ttu-id="cd6a2-204">비즈니스용 Skype Online</span><span class="sxs-lookup"><span data-stu-id="cd6a2-204">Skype for Business Online</span></span>
    
- <span data-ttu-id="cd6a2-205">비즈니스용 Skype, 버전 2007 R2 - 2016(온-프레미스)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-205">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="cd6a2-206">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="cd6a2-206">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="cd6a2-207">Symphony</span><span class="sxs-lookup"><span data-stu-id="cd6a2-207">Symphony</span></span>
    
- <span data-ttu-id="cd6a2-208">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="cd6a2-208">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="cd6a2-209">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="cd6a2-209">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="cd6a2-210">Thomson Reuters Dealings 3000 / FX Trading</span><span class="sxs-lookup"><span data-stu-id="cd6a2-210">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="cd6a2-211">Twitter</span><span class="sxs-lookup"><span data-stu-id="cd6a2-211">Twitter</span></span>
    
- <span data-ttu-id="cd6a2-212">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="cd6a2-212">UBS Chat</span></span>
    
- <span data-ttu-id="cd6a2-213">YouTube</span><span class="sxs-lookup"><span data-stu-id="cd6a2-213">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="cd6a2-214">OpenText</span><span class="sxs-lookup"><span data-stu-id="cd6a2-214">OpenText</span></span>

<span data-ttu-id="cd6a2-215">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) 에서는 다음의 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-215">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="cd6a2-216">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="cd6a2-216">Axs Encrypted</span></span>
    
- <span data-ttu-id="cd6a2-217">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="cd6a2-217">Axs Exchange</span></span>
    
- <span data-ttu-id="cd6a2-218">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="cd6a2-218">Axs Local Archive</span></span>
    
- <span data-ttu-id="cd6a2-219">Axs PlaceHolder</span><span class="sxs-lookup"><span data-stu-id="cd6a2-219">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="cd6a2-220">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="cd6a2-220">Axs Signed</span></span>
    
- <span data-ttu-id="cd6a2-221">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="cd6a2-221">Bloomberg</span></span>
    
- <span data-ttu-id="cd6a2-222">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="cd6a2-222">Thomson Reuters</span></span>
  
### <a name="smarsh"></a><span data-ttu-id="cd6a2-223">Smarsh</span><span class="sxs-lookup"><span data-stu-id="cd6a2-223">Smarsh</span></span>

<span data-ttu-id="cd6a2-224">[Smarsh](https://www.smarsh.com) 에서는 다음의 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-224">[Smarsh](https://www.smarsh.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="cd6a2-225">AIM</span><span class="sxs-lookup"><span data-stu-id="cd6a2-225">AIM</span></span>
    
- <span data-ttu-id="cd6a2-226">American Idol</span><span class="sxs-lookup"><span data-stu-id="cd6a2-226">American Idol</span></span>
    
- <span data-ttu-id="cd6a2-227">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-227">Apple Juice</span></span>
    
- <span data-ttu-id="cd6a2-228">AOL with Pivot client</span><span class="sxs-lookup"><span data-stu-id="cd6a2-228">AOL with Pivot client</span></span>
    
- <span data-ttu-id="cd6a2-229">Ares</span><span class="sxs-lookup"><span data-stu-id="cd6a2-229">Ares</span></span>
    
- <span data-ttu-id="cd6a2-230">Bazaar Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-230">Bazaar Voice</span></span>
    
- <span data-ttu-id="cd6a2-231">Bear Share</span><span class="sxs-lookup"><span data-stu-id="cd6a2-231">Bear Share</span></span>
    
- <span data-ttu-id="cd6a2-232">Bit Torrent</span><span class="sxs-lookup"><span data-stu-id="cd6a2-232">Bit Torrent</span></span>
    
- <span data-ttu-id="cd6a2-233">BlackBerry Call Logs(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-233">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="cd6a2-234">BlackBerry Messenger(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-234">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="cd6a2-235">BlackBerry PIN(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-235">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="cd6a2-236">BlackBerry SMS(v5, v10, v12)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-236">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="cd6a2-237">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="cd6a2-237">Bloomberg Mail</span></span>
    
- <span data-ttu-id="cd6a2-238">셀 신뢰</span><span class="sxs-lookup"><span data-stu-id="cd6a2-238">CellTrust</span></span>
    
- <span data-ttu-id="cd6a2-239">Chat Import</span><span class="sxs-lookup"><span data-stu-id="cd6a2-239">Chat Import</span></span>
    
- <span data-ttu-id="cd6a2-240">Chat Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="cd6a2-240">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="cd6a2-241">Chatter</span><span class="sxs-lookup"><span data-stu-id="cd6a2-241">Chatter</span></span>
    
- <span data-ttu-id="cd6a2-242">Cisco IM &amp; 현재 상태 서버 (v 9.0.1, v 9.1, v 9.1.1 SU1, v10, v 10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-242">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="cd6a2-243">Cisco Unified Presence Server(v8.6.3, v8.6.4, v8.6.5)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-243">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="cd6a2-244">Collaboration Import</span><span class="sxs-lookup"><span data-stu-id="cd6a2-244">Collaboration Import</span></span>
    
- <span data-ttu-id="cd6a2-245">Collaboration Real Time Logging</span><span class="sxs-lookup"><span data-stu-id="cd6a2-245">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="cd6a2-246">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="cd6a2-246">Direct Connect</span></span>
    
- <span data-ttu-id="cd6a2-247">Facebook</span><span class="sxs-lookup"><span data-stu-id="cd6a2-247">Facebook</span></span>
    
- <span data-ttu-id="cd6a2-248">FactSet</span><span class="sxs-lookup"><span data-stu-id="cd6a2-248">FactSet</span></span>
    
- <span data-ttu-id="cd6a2-249">FastTrack</span><span class="sxs-lookup"><span data-stu-id="cd6a2-249">FastTrack</span></span>
    
- <span data-ttu-id="cd6a2-250">Gnutella</span><span class="sxs-lookup"><span data-stu-id="cd6a2-250">Gnutella</span></span>
    
- <span data-ttu-id="cd6a2-251">Google +</span><span class="sxs-lookup"><span data-stu-id="cd6a2-251">Google+</span></span>
    
- <span data-ttu-id="cd6a2-252">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="cd6a2-252">GoToMyPC</span></span>
    
- <span data-ttu-id="cd6a2-253">Hopster</span><span class="sxs-lookup"><span data-stu-id="cd6a2-253">Hopster</span></span>
    
- <span data-ttu-id="cd6a2-254">HubConnex</span><span class="sxs-lookup"><span data-stu-id="cd6a2-254">HubConnex</span></span>
    
- <span data-ttu-id="cd6a2-255">IBM Connections(v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-255">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="cd6a2-256">IBM Connections Chat Cloud</span><span class="sxs-lookup"><span data-stu-id="cd6a2-256">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="cd6a2-257">IBM Connections Social Cloud</span><span class="sxs-lookup"><span data-stu-id="cd6a2-257">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="cd6a2-258">IBM SameTime Advanced 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="cd6a2-258">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="cd6a2-259">IBM SameTime Communicate 9.0</span><span class="sxs-lookup"><span data-stu-id="cd6a2-259">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="cd6a2-260">IBM SameTime Community(v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-260">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="cd6a2-261">IBM SameTime Complete 9.0</span><span class="sxs-lookup"><span data-stu-id="cd6a2-261">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="cd6a2-262">IBM SameTime Conference 9.0</span><span class="sxs-lookup"><span data-stu-id="cd6a2-262">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="cd6a2-263">IBM SameTime Meeting 8.5.2 IFR1</span><span class="sxs-lookup"><span data-stu-id="cd6a2-263">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="cd6a2-264">아이스/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="cd6a2-264">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="cd6a2-265">IM Import</span><span class="sxs-lookup"><span data-stu-id="cd6a2-265">IM Import</span></span>
    
- <span data-ttu-id="cd6a2-266">IM Real Time Logging and Policy</span><span class="sxs-lookup"><span data-stu-id="cd6a2-266">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="cd6a2-267">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="cd6a2-267">Indii Messenger</span></span>
    
- <span data-ttu-id="cd6a2-268">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="cd6a2-268">Instant Bloomberg</span></span>
    
- <span data-ttu-id="cd6a2-269">IRC</span><span class="sxs-lookup"><span data-stu-id="cd6a2-269">IRC</span></span>
    
- <span data-ttu-id="cd6a2-270">Jive</span><span class="sxs-lookup"><span data-stu-id="cd6a2-270">Jive</span></span>
    
- <span data-ttu-id="cd6a2-271">Jive 6 Real Time Logging(v6, v7)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-271">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="cd6a2-272">Jive Import</span><span class="sxs-lookup"><span data-stu-id="cd6a2-272">Jive Import</span></span>
    
- <span data-ttu-id="cd6a2-273">JXTA</span><span class="sxs-lookup"><span data-stu-id="cd6a2-273">JXTA</span></span>
    
- <span data-ttu-id="cd6a2-274">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="cd6a2-274">LinkedIn</span></span>
    
- <span data-ttu-id="cd6a2-275">Microsoft Lync(2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-275">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="cd6a2-276">MFTP</span><span class="sxs-lookup"><span data-stu-id="cd6a2-276">MFTP</span></span>
    
- <span data-ttu-id="cd6a2-277">Microsoft Lync 2013 Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-277">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="cd6a2-278">Microsoft SharePoint(2010, 2013)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-278">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="cd6a2-279">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="cd6a2-279">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="cd6a2-280">Microsoft UC(Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-280">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="cd6a2-281">MindAlign</span><span class="sxs-lookup"><span data-stu-id="cd6a2-281">MindAlign</span></span>
    
- <span data-ttu-id="cd6a2-282">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="cd6a2-282">Mobile Guard</span></span>
    
- <span data-ttu-id="cd6a2-283">수신</span><span class="sxs-lookup"><span data-stu-id="cd6a2-283">MSN</span></span>
    
- <span data-ttu-id="cd6a2-284">My Space</span><span class="sxs-lookup"><span data-stu-id="cd6a2-284">My Space</span></span>
    
- <span data-ttu-id="cd6a2-285">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="cd6a2-285">NEONetwork</span></span>
    
- <span data-ttu-id="cd6a2-286">Office 365 Lync Dedicated</span><span class="sxs-lookup"><span data-stu-id="cd6a2-286">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="cd6a2-287">Office 365 Shared IM</span><span class="sxs-lookup"><span data-stu-id="cd6a2-287">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="cd6a2-288">유 이율</span><span class="sxs-lookup"><span data-stu-id="cd6a2-288">Pinterest</span></span>
    
- <span data-ttu-id="cd6a2-289">Pivot</span><span class="sxs-lookup"><span data-stu-id="cd6a2-289">Pivot</span></span>
    
- <span data-ttu-id="cd6a2-290">QQ</span><span class="sxs-lookup"><span data-stu-id="cd6a2-290">QQ</span></span>
    
- <span data-ttu-id="cd6a2-291">비즈니스용 Skype 2015</span><span class="sxs-lookup"><span data-stu-id="cd6a2-291">Skype for Business 2015</span></span>
    
- <span data-ttu-id="cd6a2-292">SoftEther</span><span class="sxs-lookup"><span data-stu-id="cd6a2-292">SoftEther</span></span>
    
- <span data-ttu-id="cd6a2-293">Symphony</span><span class="sxs-lookup"><span data-stu-id="cd6a2-293">Symphony</span></span>
    
- <span data-ttu-id="cd6a2-294">Thomson Reuters Eikon</span><span class="sxs-lookup"><span data-stu-id="cd6a2-294">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="cd6a2-295">Thomson Reuters Messenger</span><span class="sxs-lookup"><span data-stu-id="cd6a2-295">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="cd6a2-296">한자</span><span class="sxs-lookup"><span data-stu-id="cd6a2-296">Tor</span></span>
    
- <span data-ttu-id="cd6a2-297">TTT</span><span class="sxs-lookup"><span data-stu-id="cd6a2-297">TTT</span></span>
    
- <span data-ttu-id="cd6a2-298">Twitter</span><span class="sxs-lookup"><span data-stu-id="cd6a2-298">Twitter</span></span>
    
- <span data-ttu-id="cd6a2-299">WinMX</span><span class="sxs-lookup"><span data-stu-id="cd6a2-299">WinMX</span></span>
    
- <span data-ttu-id="cd6a2-300">Winny</span><span class="sxs-lookup"><span data-stu-id="cd6a2-300">Winny</span></span>
    
- <span data-ttu-id="cd6a2-301">Yahoo</span><span class="sxs-lookup"><span data-stu-id="cd6a2-301">Yahoo</span></span>
    
- <span data-ttu-id="cd6a2-302">Yammer</span><span class="sxs-lookup"><span data-stu-id="cd6a2-302">Yammer</span></span>
    
- <span data-ttu-id="cd6a2-303">YouTube</span><span class="sxs-lookup"><span data-stu-id="cd6a2-303">YouTube</span></span>
    

### <a name="verba"></a><span data-ttu-id="cd6a2-304">Verba</span><span class="sxs-lookup"><span data-stu-id="cd6a2-304">Verba</span></span>

<span data-ttu-id="cd6a2-305">[Verba](https://www.verba.com) 는 다음 타사 데이터 원본을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-305">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="cd6a2-306">Avaya Aura Video</span><span class="sxs-lookup"><span data-stu-id="cd6a2-306">Avaya Aura Video</span></span>
    
- <span data-ttu-id="cd6a2-307">Avaya Aura Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-307">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="cd6a2-308">Avtec Radio</span><span class="sxs-lookup"><span data-stu-id="cd6a2-308">Avtec Radio</span></span>
    
- <span data-ttu-id="cd6a2-309">Bosch/Telex Radio</span><span class="sxs-lookup"><span data-stu-id="cd6a2-309">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="cd6a2-310">BroadSoft Video</span><span class="sxs-lookup"><span data-stu-id="cd6a2-310">BroadSoft Video</span></span>
    
- <span data-ttu-id="cd6a2-311">BroadSoft Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-311">BroadSoft Voice</span></span>
    
- <span data-ttu-id="cd6a2-312">Centile Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-312">Centile Voice</span></span>
    
- <span data-ttu-id="cd6a2-313">Cisco Jabber IM</span><span class="sxs-lookup"><span data-stu-id="cd6a2-313">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="cd6a2-314">Cisco UC Video</span><span class="sxs-lookup"><span data-stu-id="cd6a2-314">Cisco UC Video</span></span>
    
- <span data-ttu-id="cd6a2-315">Cisco UC Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-315">Cisco UC Voice</span></span>
    
- <span data-ttu-id="cd6a2-316">Cisco c s p/c h i v 비디오</span><span class="sxs-lookup"><span data-stu-id="cd6a2-316">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="cd6a2-317">Cisco c s p/c h 음성</span><span class="sxs-lookup"><span data-stu-id="cd6a2-317">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="cd6a2-318">ESChat Radio</span><span class="sxs-lookup"><span data-stu-id="cd6a2-318">ESChat Radio</span></span>
    
- <span data-ttu-id="cd6a2-319">Geoman Contact Expert</span><span class="sxs-lookup"><span data-stu-id="cd6a2-319">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="cd6a2-320">IP Trade Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-320">IP Trade Voice</span></span>
    
- <span data-ttu-id="cd6a2-321">Luware LUCS Contact Center</span><span class="sxs-lookup"><span data-stu-id="cd6a2-321">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="cd6a2-322">Microsoft UC(Unified Communications)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-322">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="cd6a2-323">Mitel MiContact Center for Lync(prairieFyre)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-323">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="cd6a2-324">Oracle/Acme Packet Session Border Controller Video</span><span class="sxs-lookup"><span data-stu-id="cd6a2-324">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="cd6a2-325">Oracle/Acme Packet Session Border Controller Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-325">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="cd6a2-326">Singtel Mobile Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-326">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="cd6a2-327">SIPREC Video</span><span class="sxs-lookup"><span data-stu-id="cd6a2-327">SIPREC Video</span></span>
    
-  <span data-ttu-id="cd6a2-328">SIPREC Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-328">SIPREC Voice</span></span> 
    
- <span data-ttu-id="cd6a2-329">비즈니스용 Skype/Lync IM</span><span class="sxs-lookup"><span data-stu-id="cd6a2-329">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="cd6a2-330">비즈니스용 Skype/Lync Video</span><span class="sxs-lookup"><span data-stu-id="cd6a2-330">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="cd6a2-331">비즈니스용 Skype/Lync Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-331">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="cd6a2-332">Speakerbus Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-332">Speakerbus Voice</span></span>
    
- <span data-ttu-id="cd6a2-333">Standard SIP/H.323 Video</span><span class="sxs-lookup"><span data-stu-id="cd6a2-333">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="cd6a2-334">Standard SIP/H.323 Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-334">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="cd6a2-335">Truphone Voice</span><span class="sxs-lookup"><span data-stu-id="cd6a2-335">Truphone Voice</span></span>
    
- <span data-ttu-id="cd6a2-336">TwistedPair Radio</span><span class="sxs-lookup"><span data-stu-id="cd6a2-336">TwistedPair Radio</span></span>
    
- <span data-ttu-id="cd6a2-337">Windows 데스크톱 컴퓨터 화면</span><span class="sxs-lookup"><span data-stu-id="cd6a2-337">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="cd6a2-338">2단계: Office 365에서 타사 데이터 사서함 만들기 및 구성</span><span class="sxs-lookup"><span data-stu-id="cd6a2-338">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="cd6a2-339">다음은 Office 365로 데이터를 가져오기 위한 타사 데이터 사서함을 만들고 구성 하는 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-339">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365.</span></span> <span data-ttu-id="cd6a2-340">앞에서 설명한 것 처럼 파트너 커넥터에서 항목의 사용자 ID를 Office 365 사용자 계정에 매핑할 수 없는 경우에는이 사서함으로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-340">As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="cd6a2-341">**Microsoft 365 관리 센터에서이 작업 완료**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-341">**Complete these tasks in the Microsoft 365 admin center**</span></span>
  
1. <span data-ttu-id="cd6a2-342">Office 365에서 사용자 계정을 만들고이 계정에 Exchange Online 계획 2 라이선스를 할당 합니다. [Office 365에 사용자 추가를](https://go.microsoft.com/fwlink/p/?LinkId=692098)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-342">Create a user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098).</span></span> <span data-ttu-id="cd6a2-343">계획 2 라이선스는 사서함을 소송 보존 상태로 설정 하거나 저장소 할당량이 무제한 인 보관 사서함을 사용 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-343">A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="cd6a2-344">타사 데이터 사서함에 대 한 사용자 계정을 Office 365의 **Exchange 관리자** 관리자 역할에 추가 합니다. [Office 365에서 관리자 역할 할당을](https://go.microsoft.com/fwlink/p/?LinkId=532393)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-344">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="cd6a2-345">이 사용자 계정의 자격 증명을 기록해 둡니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-345">Write down the credentials for this user account.</span></span> <span data-ttu-id="cd6a2-346">4단계에서 설명한 것처럼 파트너에게 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-346">You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="cd6a2-347">**Exchange 관리 센터에서 다음 작업 완료**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-347">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="cd6a2-348">조직의 주소록 및 기타 주소 목록에서 타사 데이터 사서함을 숨깁니다. [사용자 사서함 관리](https://go.microsoft.com/fwlink/p/?LinkId=616058)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-348">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058).</span></span> <span data-ttu-id="cd6a2-349">또는 다음 PowerShell 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-349">Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="cd6a2-350">Administrators 또는 규정 준수 관리자가 Outlook 데스크톱 클라이언트에서 타사 데이터 사서함을 열 수 있도록 타사 데이터 사서함에 대 한 **FullAccess** 권한을 할당 합니다. [받는 사람의 사용 권한 관리를](https://go.microsoft.com/fwlink/p/?LinkId=692104)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-350">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="cd6a2-351">타사 데이터 사서함에 대해 다음과 같은 준수 관련 Office 365 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-351">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="cd6a2-352">보관 사서함을 사용 하도록 설정 합니다. [보관 사서함 사용](enable-archive-mailboxes.md) 및 [무제한 보관 사용](enable-unlimited-archiving.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-352">Enable the archive mailbox; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span> <span data-ttu-id="cd6a2-353">이렇게 하면 타사 데이터 항목을 보관 사서함으로 이동 하는 보관 정책을 설정 하 여 기본 사서함의 저장 공간을 확보할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-353">This lets you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox.</span></span> <span data-ttu-id="cd6a2-354">이를 통해 타사 데이터에 대해 무제한 저장소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-354">This provides you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="cd6a2-355">타사 데이터 사서함에 소송 보존을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-355">Place the third-party data mailbox on Litigation Hold.</span></span> <span data-ttu-id="cd6a2-356">보안 및 준수 센터에서 Office 365 보존 정책을 적용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-356">You can also apply an Office 365 retention policy in the security and compliance center.</span></span> <span data-ttu-id="cd6a2-357">이 사서함을 보류 상태로 두면 타사 데이터 항목 (무기한 또는 지정 된 기간 동안)이 유지 되 고 사서함에서 제거 되는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-357">Placing this mailbox on hold retains third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox.</span></span> <span data-ttu-id="cd6a2-358">다음 항목 중 하나를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-358">See one of the following topics:</span></span>
    
      - [<span data-ttu-id="cd6a2-359">사서함을 소송 자료 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="cd6a2-359">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="cd6a2-360">Office 365의 보존 정책 개요</span><span class="sxs-lookup"><span data-stu-id="cd6a2-360">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="cd6a2-361">타사 데이터 사서함에 대 한 소유자, 대리인 및 관리자 액세스에 대 한 사서함 감사 로깅을 사용 하도록 설정 합니다. [Office 365에서 사서함 감사 사용을](enable-mailbox-auditing.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-361">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md).</span></span> <span data-ttu-id="cd6a2-362">이렇게 하면 타사 데이터 사서함에 대 한 액세스 권한이 있는 모든 사용자가 수행한 모든 작업을 감사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-362">This allows you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="cd6a2-363">3단계: 타사 데이터에 대한 사용자 사서함 구성</span><span class="sxs-lookup"><span data-stu-id="cd6a2-363">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="cd6a2-364">다음 단계는 타사 데이터를 지원하도록 사용자 사서함을 구성하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-364">The next step is to configure user mailboxes to support third-party data.</span></span> <span data-ttu-id="cd6a2-365">Exchange 관리 센터를 사용 하거나 해당 Windows PowerShell cmdlet을 사용 하 여 이러한 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-365">Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="cd6a2-366">각 사용자에 대해 보관 사서함을 사용 하도록 설정 합니다. [보관 사서함 사용](enable-archive-mailboxes.md) 및 [무제한 보관 사용](enable-unlimited-archiving.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-366">Enable the archive mailbox for each user; see [Enable archive mailboxes](enable-archive-mailboxes.md) and [Enable unlimited archiving](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="cd6a2-367">사용자 사서함을 소송 보존으로 설정 하거나 Office 365 보관 정책을 적용 합니다. 다음 항목 중 하나를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-367">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="cd6a2-368">사서함을 소송 자료 보존으로 설정</span><span class="sxs-lookup"><span data-stu-id="cd6a2-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="cd6a2-369">Office 365의 보존 정책 개요</span><span class="sxs-lookup"><span data-stu-id="cd6a2-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="cd6a2-370">앞서 언급한 것처럼 사서함을 보존하면 타사 데이터 원본의 항목을 보존하는 기간을 설정하거나 항목을 무기한 보존하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-370">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="cd6a2-371">4단계: 파트너에게 정보 제공</span><span class="sxs-lookup"><span data-stu-id="cd6a2-371">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="cd6a2-372">마지막 단계는 Office 365 조직에 연결하여 사용자 사서함이나 타사 데이터 사서함으로 데이터를 가져오도록 커넥터를 구성할 수 있게 파트너에게 다음 정보를 제공하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-372">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="cd6a2-373">Office 365에서 Azure 서비스에 연결 하는 데 사용 되는 끝점:</span><span class="sxs-lookup"><span data-stu-id="cd6a2-373">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="cd6a2-374">2 단계에서 만든 타사 데이터 사서함의 로그인 자격 증명 (Office 365 사용자 ID 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-374">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2.</span></span> <span data-ttu-id="cd6a2-375">이러한 자격 증명은 파트너 커넥터가 항목을 액세스하고 사용자 사서함 및 타사 데이터 사서함으로 가져올 수 있도록 하는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-375">These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="cd6a2-376">5 단계: Azure Active Directory에서 타사 데이터 커넥터 등록</span><span class="sxs-lookup"><span data-stu-id="cd6a2-376">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="cd6a2-377">2018 년 9 월 30 일부부터 Office 365의 Azure service는 Exchange Online의 최신 인증을 사용 하 여 데이터를 가져오기 위해 Office 365 조직에 연결을 시도 하는 타사 데이터 커넥터를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-377">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data.</span></span> <span data-ttu-id="cd6a2-378">이러한 변경이 발생 하는 이유는 최신 인증이 이전에 설명한 끝점을 사용 하 여 Azure 서비스에 연결 하는 허용 목록이 타사 커넥터를 기반으로 하는 현재 방법 보다 더 많은 보안 기능을 제공 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-378">The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="cd6a2-379">최신 인증 방법을 사용 하 여 타사 데이터 커넥터가 Office 365에 연결 되도록 하려면 Office 365 조직의 관리자가 해당 커넥터를 Azure Active Directory의 신뢰할 수 있는 서비스 응용 프로그램으로 등록 하는 것이 동의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-379">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory.</span></span> <span data-ttu-id="cd6a2-380">이 작업은 사용 권한 요청을 수락 하 여 커넥터가 Azure Active Directory에서 조직의 데이터에 액세스할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-380">This is done by accepting a permission request to allow the connector to access your organization's data in Azure Active Directory.</span></span> <span data-ttu-id="cd6a2-381">이 요청을 수락 하면 타사 데이터 커넥터가 엔터프라이즈 응용 프로그램으로 Azure Active Directory에 추가 되 고 서비스 사용자로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-381">After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal.</span></span> <span data-ttu-id="cd6a2-382">승인 프로세스에 대 한 자세한 내용은 [테 넌 트 관리자 동의](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-382">For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="cd6a2-383">커넥터 등록을 위한 요청에 액세스 하 고 수락 하는 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-383">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="cd6a2-384">[이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) 이동 하 여 Office 365 전역 관리자의 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-384">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="cd6a2-385">다음 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-385">The following dialog box is displayed.</span></span> <span data-ttu-id="cd6a2-386">Carets를 확장 하 여 커넥터에 할당 되는 사용 권한을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-386">You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="cd6a2-387">![사용 권한 요청 대화 상자가 표시 됩니다.](media/O365-ThirdPartyDataConnector-OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="cd6a2-387">![The permissions request dialog is displayed](media/O365-ThirdPartyDataConnector-OptIn1.png)</span></span>
2. <span data-ttu-id="cd6a2-388">**Accept(동의함)** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-388">Click **Accept**.</span></span>

<span data-ttu-id="cd6a2-389">요청을 수락 하면 [Azure portal](https://portal.azure.com) 이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-389">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed.</span></span> <span data-ttu-id="cd6a2-390">조직의 응용 프로그램 목록을 보려면 **Azure Active Directory** > **Enterprise 응용 프로그램**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-390">To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**.</span></span> <span data-ttu-id="cd6a2-391">Office 365 타사 데이터 커넥터가 **엔터프라이즈 응용 프로그램** 블레이드에서 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-391">The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd6a2-392">Azure Active Directory에 타사 데이터 커넥터를 등록 하지 않으면, 2018 년 9 월 30 일 이후에는 타사 데이터를 조직의 사서함으로 가져올 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-392">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory.</span></span> <span data-ttu-id="cd6a2-393">참고 5 단계에 나와 있는 절차에 따라 기존 타사 데이터 커넥터 (9 월 30 일 이전에는 2018)도 Azure Active Directory에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-393">Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="cd6a2-394">타사 데이터 커넥터에 대 한 동의 해지</span><span class="sxs-lookup"><span data-stu-id="cd6a2-394">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="cd6a2-395">조직이 Azure Active Directory에서 타사 데이터 커넥터를 등록 하기 위해 권한 요청을 consents 후에는 조직에서 언제 든 지 해당 동의를 해지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-395">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time.</span></span> <span data-ttu-id="cd6a2-396">그러나 커넥터에 대 한 동의를 취소 하는 것은 타사 데이터 원본의 데이터를 더 이상 Office 365로 가져올 수 없다는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-396">However, revoking the consent for a connector means that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="cd6a2-397">타사 데이터 커넥터에 대 한 동의를 해지 하려면 Azure portal에서 **엔터프라이즈 응용 프로그램** 블레이드를 사용 하 여 Azure Active Directory에서 해당 서비스 사용자를 삭제 하거나, 다음을 [사용 하 여 응용 프로그램을 삭제 하면 됩니다. Remove-(New-msolserviceprincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) In Office 365 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-397">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell.</span></span> <span data-ttu-id="cd6a2-398">Azure Active Directory PowerShell에서 [AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-398">You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="cd6a2-399">추가 정보</span><span class="sxs-lookup"><span data-stu-id="cd6a2-399">More information</span></span>

- <span data-ttu-id="cd6a2-400">앞서 설명한 것처럼 타사 데이터 원본의 항목을 Exchange 사서함에 전자 메일 메시지로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-400">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages.</span></span> <span data-ttu-id="cd6a2-401">파트너 커넥터는 Office 365 API에 필요한 스키마를 사용 하 여 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-401">The partner connector imports the item using a schema required by the Office 365 API.</span></span> <span data-ttu-id="cd6a2-402">다음 표에서는 타사 데이터 원본 항목을 Exchange 사서함에 전자 메일 메시지로 가져온 후, 타사 데이터 원본 항목에 대한 메시지 속성을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-402">The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message.</span></span> <span data-ttu-id="cd6a2-403">또한 이 표는 메시지 속성이 필수인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-403">The table also indicates if the message property is mandatory.</span></span> <span data-ttu-id="cd6a2-404">필수 속성은 채워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-404">Mandatory properties must be populated.</span></span> <span data-ttu-id="cd6a2-405">항목에 필수 속성이 없는 경우에는 Office 365로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-405">If an item is missing a mandatory property, it won't be imported to Office 365.</span></span> <span data-ttu-id="cd6a2-406">가져오기 프로세스를 진행 하면 항목을 가져오지 못한 이유와 해당 속성이 누락 된 이유를 설명 하는 오류 메시지가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-406">The import process returns an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="cd6a2-407">**메시지 속성**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-407">**Message property**</span></span>|<span data-ttu-id="cd6a2-408">**강제?**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-408">**Mandatory?**</span></span>|<span data-ttu-id="cd6a2-409">**설명**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-409">**Description**</span></span>|<span data-ttu-id="cd6a2-410">**예제 값**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-410">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="cd6a2-411">**보낸 사람**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-411">**FROM**</span></span> <br/> |<span data-ttu-id="cd6a2-412">예</span><span class="sxs-lookup"><span data-stu-id="cd6a2-412">Yes</span></span>  <br/> |<span data-ttu-id="cd6a2-413">타사 데이터 원본 항목을 처음 만들었거나 보낸 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-413">The user who originally created or sent the item in the third-party data source.</span></span> <span data-ttu-id="cd6a2-414">파트너 커넥터는 원본 항목 (예: Twitter 핸들)의 사용자 ID를 모든 참가자 (시작 및 대상 필드의 사용자)에 대 한 Office 365 사용자 계정으로 매핑하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-414">The partner connector attempts to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields).</span></span> <span data-ttu-id="cd6a2-415">메시지 복사본을 모든 참가자의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-415">A copy of the message will be imported to the mailbox of every participant.</span></span> <span data-ttu-id="cd6a2-416">항목의 참가자가 Office 365 사용자 계정에 매핑할 수 없는 경우에는 Office 365에서 타사 보관 사서함으로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-416">If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.</span></span>  <br/> <br/> <span data-ttu-id="cd6a2-417">항목을 보낸 사람으로 식별 된 참석자는 해당 항목을 가져올 Office 365 조직의 활성 사서함이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-417">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to.</span></span> <span data-ttu-id="cd6a2-418">보낸 사람에게 활성 사서함이 없으면 다음과 같은 오류가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-418">If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="cd6a2-419">**받는 사람**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-419">**TO**</span></span> <br/> |<span data-ttu-id="cd6a2-420">예</span><span class="sxs-lookup"><span data-stu-id="cd6a2-420">Yes</span></span>  <br/> |<span data-ttu-id="cd6a2-421">데이터 원본의 항목을 받은 사람입니다(해당되는 경우).</span><span class="sxs-lookup"><span data-stu-id="cd6a2-421">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="cd6a2-422">**제목**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-422">**SUBJECT**</span></span> <br/> |<span data-ttu-id="cd6a2-423">아니요</span><span class="sxs-lookup"><span data-stu-id="cd6a2-423">No</span></span>  <br/> |<span data-ttu-id="cd6a2-424">원본 항목의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-424">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="cd6a2-425">**종료일**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-425">**DATE**</span></span> <br/> |<span data-ttu-id="cd6a2-426">예</span><span class="sxs-lookup"><span data-stu-id="cd6a2-426">Yes</span></span>  <br/> |<span data-ttu-id="cd6a2-427">항목이 처음으로 작성 되거나 고객 데이터 원본에 게시 된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-427">The date the item was originally created or posted in the customer data source.</span></span> <span data-ttu-id="cd6a2-428">예를 들어, Twitter 메시지가 tweeted 된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-428">For example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="cd6a2-429">**보내기**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-429">**BODY**</span></span> <br/> |<span data-ttu-id="cd6a2-430">아니요</span><span class="sxs-lookup"><span data-stu-id="cd6a2-430">No</span></span>  <br/> |<span data-ttu-id="cd6a2-431">메시지 또는 게시물의 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-431">The contents of the message or post.</span></span> <span data-ttu-id="cd6a2-432">일부 데이터 원본의 경우 이 속성의 콘텐츠는 **SUBJECT** 속성의 콘텐츠와 같을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-432">For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property.</span></span> <span data-ttu-id="cd6a2-433">가져오기 프로세스 중에 파트너 커넥터는 가능한 한 콘텐츠 원본에서 완전 한 충실도를 유지 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-433">During the import process, the partner connector attempts to maintain full fidelity from the content source as possible.</span></span> <span data-ttu-id="cd6a2-434">가능한 경우 원본 항목의 본문에서 가져온 파일, 그래픽 또는 기타 콘텐츠가 이 속성에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-434">If possible files, graphics, or other content from the body of the source item is included in this property.</span></span> <span data-ttu-id="cd6a2-435">그렇지 않은 경우 원본 항목의 콘텐츠가 **ATTACHMENT** 속성에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-435">Otherwise, content from the source item is included in the **ATTACHMENT** property.</span></span> <span data-ttu-id="cd6a2-436">이 속성의 내용은 파트너 커넥터와 원본 플랫폼의 기능에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-436">The contents of this property depends on the partner connector and on the capability of the source platform.</span></span>  <br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="cd6a2-437">**덧붙인**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-437">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="cd6a2-438">아니요</span><span class="sxs-lookup"><span data-stu-id="cd6a2-438">No</span></span>  <br/> |<span data-ttu-id="cd6a2-439">데이터 원본의 항목 (예: Twitter 또는 인스턴트 메시징 대화에 있는 tweet)에 첨부 된 파일이 있거나 이미지를 포함 하는 경우, 파트너 연결에서는 먼저 **BODY** 속성에 첨부 파일을 포함 하 려 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-439">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property.</span></span> <span data-ttu-id="cd6a2-440">이것이 가능 하지 않으면 \* \* ATTACHMENT \* \* 속성에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-440">If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property.</span></span> <span data-ttu-id="cd6a2-441">첨부 파일의 다른 예로는 Facebook의 좋아요, 콘텐츠 원본의 메타데이터, 메시지 또는 게시물에 대한 응답이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-441">Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.</span></span>  <br/> | `image.gif` <br/> |
    |<span data-ttu-id="cd6a2-442">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="cd6a2-442">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="cd6a2-443">예</span><span class="sxs-lookup"><span data-stu-id="cd6a2-443">Yes</span></span>  <br/> | <span data-ttu-id="cd6a2-444">파트너 커넥터가 만들어서 채우는 다중 값 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-444">This is a multi-value property, which is created and populated by partner connector.</span></span> <span data-ttu-id="cd6a2-445">이 속성의 형식은 `IPM.NOTE.Source.Event`입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-445">The format of this property is  `IPM.NOTE.Source.Event`.</span></span> <span data-ttu-id="cd6a2-446">(이 속성은로 `IPM.NOTE`시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-446">(This property must begin with  `IPM.NOTE`.</span></span> <span data-ttu-id="cd6a2-447">이 형식은 `IPM.NOTE.X` 메시지 클래스의 형식과 유사 합니다. 이 속성에는 다음 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-447">This format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:</span></span>  <br/><br/><span data-ttu-id="cd6a2-448">`Source`: 타사 데이터 원본을 나타냅니다. 예: Twitter, Facebook 또는 BlackBerry를 예로 들 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-448">`Source`: Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="cd6a2-449">`Event`: 항목을 생성 한 타사 데이터 원본에서 수행한 작업의 유형을 나타냅니다. 예를 들어, Twitter에 있는 tweet 또는 Facebook의 게시물입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-449">`Event`: Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook.</span></span> <span data-ttu-id="cd6a2-450">이벤트는 데이터 원본에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-450">Events are specific to the data source.</span></span>  <br/> <br/>  <span data-ttu-id="cd6a2-451">이 속성의 한 가지 목적은 항목이 시작된 데이터 원본이나 이벤트의 유형에 따라 특정 항목을 필터링하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-451">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event.</span></span> <span data-ttu-id="cd6a2-452">예를 들어 eDiscovery 검색에서 특정 사용자가 게시한 모든 트윗을 찾는 검색 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-452">For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.</span></span>  <br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="cd6a2-453">Office 365에서 사서함에 항목을 성공적으로 가져오면 고유한 식별자가 HTTP 응답의 일부로 다시 발신자에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-453">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response.</span></span> <span data-ttu-id="cd6a2-454">이 식별자 `x-IngestionCorrelationID`는 종단 간 항목 추적을 위해 파트너의 후속 문제 해결을 위해 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-454">This identifier, called  `x-IngestionCorrelationID`, can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items.</span></span> <span data-ttu-id="cd6a2-455">파트너는 이 정보를 수집하고 적절하게 기록해두는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-455">It's recommended that partners capture this information and log it accordingly at their end.</span></span> <span data-ttu-id="cd6a2-456">이 식별자를 나타내는 HTTP 응답의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-456">Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="cd6a2-457">보안 및 준수 센터의 콘텐츠 검색 도구를 사용 하 여 타사 데이터 원본에서 Office 365의 사서함으로 가져온 항목을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-457">You can use the Content Search tool in the security and compliance center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="cd6a2-458">이러한 가져온 항목을 구체적으로 검색 하려면 콘텐츠 검색의 키워드 상자에 다음과 같은 메시지 속성-값 쌍을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-458">To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search.</span></span>
    
  - <span data-ttu-id="cd6a2-459">**`kind:externaldata`**:이 속성-값 쌍을 사용 하 여 모든 타사 데이터 형식을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-459">**`kind:externaldata`**: Use this property-value pair to search all third-party data types.</span></span> <span data-ttu-id="cd6a2-460">예를 들어 타사 데이터 원본에서 가져온 항목과 가져온 항목의 Subject 속성에 "contoso" 라는 단어가 포함 된 항목을 검색 하려면 keyword 쿼리 `kind:externaldata AND subject:contoso`를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-460">For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="cd6a2-461">**`itemclass:ipm.externaldata.<third-party data type>`**:이 속성-값 쌍을 사용 하 여 지정 된 타사 데이터 형식만 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-461">**`itemclass:ipm.externaldata.<third-party data type>`**: Use this property-value pair to only search a specify type of third-party data.</span></span> <span data-ttu-id="cd6a2-462">예를 들어 Subject 속성에서 "contoso" 라는 단어가 포함 된 Facebook 데이터만 검색 하려면 keyword 쿼리 `itemclass:ipm.externaldata.Facebook* AND subject:contoso`를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-462">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="cd6a2-463">`itemclass` 속성의 타사 데이터 형식에 사용할 값의 전체 목록은 [Office 365로 가져온 타사 데이터 검색을 사용 하 여 콘텐츠 검색](use-content-search-to-search-third-party-data-that-was-imported.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-463">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="cd6a2-464">콘텐츠 검색 사용 및 키워드 검색 쿼리를 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6a2-464">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="cd6a2-465">Office 365의 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="cd6a2-465">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="cd6a2-466">콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건</span><span class="sxs-lookup"><span data-stu-id="cd6a2-466">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
