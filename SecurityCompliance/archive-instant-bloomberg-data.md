---
title: Office 365에서 인스턴트 Bloomberg 데이터를 보관 하는 커넥터 설정 (미리 보기)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 관리자는 기본 커넥터를 설정 하 여 인스턴트 Bloomberg 채팅 도구에서 Office 365로 데이터를 가져올 수 있습니다. 이렇게 하면 Office 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터를 관리할 수도 있습니다.
ms.openlocfilehash: 0b69ddaa21196bd0e149eba672fec104eabe2e5e
ms.sourcegitcommit: ab16ddf4c050a995471a058150767a0778be0b88
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35431611"
---
# <a name="set-up-a-connector-to-archive-instant-bloomberg-data-in-office-365-preview"></a><span data-ttu-id="75f27-104">Office 365에서 인스턴트 Bloomberg 데이터를 보관 하는 커넥터 설정 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="75f27-104">Set up a connector to archive Instant Bloomberg data in Office 365 (Preview)</span></span>

<span data-ttu-id="75f27-105">Office 365에서 인스턴트 Bloomberg 데이터를 보관 하는 커넥터 기능이 미리 보기에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-105">The connector feature to archive Instant Bloomberg data in Office 365 is in Preview.</span></span>

<span data-ttu-id="75f27-106">Office 365의 보안 & 준수 센터에서 네이티브 커넥터를 사용 하 여 [인스턴트 Bloomberg](https://www.bloomberg.com/professional/product/collaboration/) 공동 작업 도구에서 금융 서비스 채팅 데이터를 가져오고 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-106">Use a native connector in the Security & Compliance Center in Office 365 to import and archive financial services chat data from [Instant Bloomberg](https://www.bloomberg.com/professional/product/collaboration/) collaboration tool.</span></span> <span data-ttu-id="75f27-107">커넥터를 설정 하 고 구성한 후에는 조직에서 매월 Bloomberg 보안 FTP 사이트 (SFTP)에 연결 하 고, 채팅 메시지의 콘텐츠를 전자 메일 메시지 형식으로 변환한 다음, 해당 항목을 Office 365의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-107">After you set up and configure a connector, it connects to your organization's Bloomberg secure FTP site (SFTP) once every day, converts the content of chat messages to an email message format, and then imports those items to mailboxes in Office 365.</span></span>

<span data-ttu-id="75f27-108">인스턴트 Bloomberg 데이터를 사용자 사서함에 저장 한 후에는 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사 및 Office 365 고정 정책과 같은 Office 365 준수 기능을 인스턴트 Bloomberg 데이터에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-108">After Instant Bloomberg data is stored in user mailboxes, you can apply Office 365 compliance features such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies to Instant Bloomberg data.</span></span> <span data-ttu-id="75f27-109">예를 들어 콘텐츠 검색을 사용 하 여 인스턴트 Bloomberg 채팅 메시지를 검색 하거나, 고급 eDiscovery 사례의 custodian에 인스턴트 Bloomberg 데이터가 포함 된 사서함을 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-109">For example, you can search Instant Bloomberg chat messages using Content Search or associate the mailbox that contains the Instant Bloomberg data with a custodian in an Advanced eDiscovery case.</span></span> <span data-ttu-id="75f27-110">인스턴트 Bloomberg 커넥터를 사용 하 여 Office 365에서 데이터를 가져오고 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-110">Using an Instant Bloomberg connector to import and archive data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="overview-of-archiving-instant-bloomberg-data"></a><span data-ttu-id="75f27-111">인스턴트 Bloomberg 데이터 보관 개요</span><span class="sxs-lookup"><span data-stu-id="75f27-111">Overview of archiving Instant Bloomberg data</span></span>

<span data-ttu-id="75f27-112">다음 개요에서는 커넥터를 사용 하 여 Office 365에서 인스턴트 Bloomberg 채팅 데이터를 보관 하는 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-112">The following overview explains the process of using a connector to archive Instant Bloomberg chat data in Office 365.</span></span> 

![인스턴트 Bloomberg 가져오기 및 보관 프로세스](media/InstantBloombergDataArchiving.png)

1. <span data-ttu-id="75f27-114">조직에서 Bloomberg를 사용 하 여 Bloomberg SFTP 사이트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-114">Your organization works with Bloomberg to set up a Bloomberg SFTP site.</span></span> <span data-ttu-id="75f27-115">또한 Bloomberg을 사용 하 여 Bloomberg SFTP 사이트에 채팅 메시지를 복사 하도록 인스턴트 Bloomberg을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-115">You will also work with Bloomberg to configure Instant Bloomberg to copy chat messages to your Bloomberg SFTP site.</span></span>

2. <span data-ttu-id="75f27-116">24 시간 마다 한 번씩 인스턴트 Bloomberg의 채팅 메시지가 Bloomberg SFTP 사이트로 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-116">Once every 24 hours, chat messages from Instant Bloomberg are copied to the Bloomberg SFTP site.</span></span>
    
3. <span data-ttu-id="75f27-117">Security & 준수 센터에서 만든 인스턴트 Bloomberg 커넥터는 매일 Bloomberg SFTP 사이트에 연결 하 고 이전 24 시간에서 Microsoft 클라우드의 안전한 Azure Storage 영역으로 채팅 메시지를 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-117">The Instant Bloomberg connector that you create in the Security & Compliance Center connects to the Bloomberg SFTP site every day and transfers the chat messages from the previous 24 hours to a secure Azure Storage area in the Microsoft Cloud.</span></span> <span data-ttu-id="75f27-118">또한이 커넥터는 채팅 massage의 콘텐츠를 전자 메일 메시지 형식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-118">The connector also converts the content of a chat massage to an email message format.</span></span>
    
4. <span data-ttu-id="75f27-119">커넥터는 채팅 메시지 항목을 특정 사용자의 사서함 또는 대체 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-119">The connector imports the chat message items to the mailbox of a specific user or to an alternative mailbox.</span></span> <span data-ttu-id="75f27-120">커넥터에서 *CorporateEmailAddress* 속성 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-120">The connector does by using the value of the *CorporateEmailAddress* property.</span></span> <span data-ttu-id="75f27-121">모든 채팅 메시지에는 채팅 메시지의 모든 참가자의 전자 메일 주소로 채워지는이 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-121">Every chat message contains this property, which is populated with the email address of every participant of the chat message.</span></span> <span data-ttu-id="75f27-122">특정 사용자 사서함 또는 대체 사서함으로 항목을 가져올지 여부는 다음 기준에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-122">Whether an item is imported into a specific user mailbox or to the alternative mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="75f27-123">위한.</span><span class="sxs-lookup"><span data-stu-id="75f27-123">a.</span></span> <span data-ttu-id="75f27-124">**Office 365 사용자 계정에 해당 하는 CorporateEmailAddress 속성의 값** 이 있는 항목-커넥터가 *CorporateEmailAddress* 속성의 전자 메일 주소를 office 365의 특정 사용자 계정에 연결할 수 있는 경우 사용자 Office 365 사서함의 받은 편지함 폴더에 항목이 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-124">**Items that have a value in the CorporateEmailAddress property that corresponds to an Office 365 user account** – If the connector can associate the email address in the *CorporateEmailAddress* property to a specific user account in Office 365, the item is copied to the Inbox folder in the user's Office 365 mailbox.</span></span>
    
    <span data-ttu-id="75f27-125">b.</span><span class="sxs-lookup"><span data-stu-id="75f27-125">b.</span></span> <span data-ttu-id="75f27-126">**CorporateEmailAddress 속성의 값이 office 365 사용자 계정에 해당 하지 않는 항목** -커넥터가 *CorporateEmailAddress* 속성의 전자 메일 주소를 office의 특정 사용자 계정과 연결할 수 없는 경우 365에서 항목은 Office 365의 대체 "수신-전체" 사서함의 받은 편지함 폴더에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-126">**Items that have a value in the CorporateEmailAddress property that doesn't correspond to an Office 365 user account** – If the connector can't associate an email address in the *CorporateEmailAddress* property to a specific user account in Office 365, the item is copied to the Inbox folder of an alternative, "catch-all" mailbox in Office 365.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="75f27-127">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="75f27-127">Before you begin</span></span>

<span data-ttu-id="75f27-128">인스턴트 Bloomberg 데이터를 보관 하는 데 필요한 대부분의 구현 단계는 Office 365 외부에 있으므로 보안 & 준수 센터에서 커넥터를 만들기 전에 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-128">Many of the implementation steps required to archive Instant Bloomberg data are external to Office 365 and must be completed before you can create the connector in the Security & Compliance Center.</span></span>

- <span data-ttu-id="75f27-129">[Blooomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA)를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-129">Subscribe to [Blooomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA).</span></span> <span data-ttu-id="75f27-130">이는 Bloomberg Anywhere에 로그인 하 여 설정 하 고 구성 해야 하는 Bloomberg SFTP 사이트에 액세스할 수 있도록 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-130">This is required so that you can log in to Bloomberg Anywhere to access the Bloomberg SFTP site that you have to set up and configure.</span></span>

- <span data-ttu-id="75f27-131">Bloomberg SFTP (보안 파일 전송 프로토콜) 사이트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-131">Set up a Bloomberg SFTP (Secure file transfer protocol) site.</span></span> <span data-ttu-id="75f27-132">Bloomberg을 사용 하 여 SFTP 사이트를 설정한 후에는 인스턴트 Bloomberg의 데이터가 매일 SFTP 사이트로 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-132">After working with Bloomberg to set up the SFTP site, data from Instant Bloomberg is uploaded to the SFTP site every day.</span></span> <span data-ttu-id="75f27-133">2 단계에서 만든 커넥터가이 SFTP 사이트에 연결 되 고 채팅 데이터를 Office 365 사서함으로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-133">The connector you create in Step 2 connects to this SFTP site and transfers the chat data to Office 365 mailboxes.</span></span> <span data-ttu-id="75f27-134">또한 SFTP는 전송 프로세스 중에 Office 365 사서함으로 전송 되는 인스턴트 Bloomberg 채팅 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-134">SFTP also encrypts the Instant Bloomberg chat data that is sent to Office 365 mailboxes during the transfer process.</span></span>

    <span data-ttu-id="75f27-135">Bloomberg SFTP에 대 한 자세한 내용은 *BB-sftp*라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-135">For information about Bloomberg SFTP (also called *BB-SFTP*):</span></span>

    - <span data-ttu-id="75f27-136">[Bloomberg 지원](https://www.bloomberg.com/professional/support/documentation/)에서 "SFTP 연결 표준" 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="75f27-136">See the "SFTP Connectivity Standards" document at [Bloomberg Support](https://www.bloomberg.com/professional/support/documentation/).</span></span>
    
    - <span data-ttu-id="75f27-137">[Bloomberg 고객 지원](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc)에 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-137">Contact [Bloomberg customer support](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc).</span></span>

    <span data-ttu-id="75f27-138">Bloomberg을 사용 하 여 SFTP 사이트를 설정한 후 Bloomberg에서는 Bloomberg 구현 전자 메일 메시지에 응답 한 후 몇 가지 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-138">After you work with Bloomberg to set up an SFTP site, Bloomberg will provide some information to you after you respond to the Bloomberg implementation email message.</span></span> <span data-ttu-id="75f27-139">다음 정보의 복사본을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-139">Save a copy of the following information.</span></span> <span data-ttu-id="75f27-140">이 도구를 사용 하 여 3 단계에서 커넥터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-140">You use it to set up a connector in Step 3.</span></span>

    - <span data-ttu-id="75f27-141">기업 코드-조직의 ID 이며 Bloomberg SFTP 사이트에 로그인 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-141">Firm code, which is an ID for your organization and is used to log in to the Bloomberg SFTP site.</span></span>

    - <span data-ttu-id="75f27-142">Bloomberg SFTP 사이트의 암호</span><span class="sxs-lookup"><span data-stu-id="75f27-142">Password for your Bloomberg SFTP site</span></span>

    - <span data-ttu-id="75f27-143">Bloomberg SFTP 사이트의 URL (예: sftp.bloomberg.com)</span><span class="sxs-lookup"><span data-stu-id="75f27-143">URL for Bloomberg SFTP site (for example, sftp.bloomberg.com)</span></span>

    - <span data-ttu-id="75f27-144">Bloomberg SFTP 사이트의 포트 번호</span><span class="sxs-lookup"><span data-stu-id="75f27-144">Port number for Bloomberg SFTP site</span></span>

- <span data-ttu-id="75f27-145">조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-145">Your organization must consent to allow the Office 365 Import service to access mailbox data in your organization.</span></span> <span data-ttu-id="75f27-146">이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Office 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-146">To consent to this request, go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), sign in with the credentials of an Office 365 global admin, and then accept the request.</span></span> <span data-ttu-id="75f27-147">3 단계에서 인스턴트 Bloomberg 커넥터를 성공적으로 만들기 전에이 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-147">You have to complete this step before you can successfully create the Instant Bloomberg connector in Step 3.</span></span>

- <span data-ttu-id="75f27-148">3 단계에서 인스턴트 Bloomberg 커넥터를 만들고 1 단계에서 공개 키와 IP 주소를 다운로드 하는 사용자에 게 Exchange Online의 사서함 가져오기 내보내기 역할이 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-148">The user who creates an Instant Bloomberg connector in Step 3 (and who downloads the public keys and IP address in Step 1) must be assigned the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="75f27-149">이는 보안 & 준수 센터에서 **타사 데이터 보관** 페이지에 액세스 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-149">This is required to access the **Archive third-party data** page in the Security & Compliance Center.</span></span> <span data-ttu-id="75f27-150">기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-150">By default, this role isn't assigned to any role group in Exchange Online.</span></span> <span data-ttu-id="75f27-151">Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-151">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="75f27-152">또는 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-152">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="75f27-153">자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="75f27-153">For more information, see the  [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

## <a name="step-1-obtain-ssh-and-pgp-public-keys"></a><span data-ttu-id="75f27-154">1 단계: SSH 및 PGP 공개 키 획득</span><span class="sxs-lookup"><span data-stu-id="75f27-154">Step 1: Obtain SSH and PGP public keys</span></span>

<span data-ttu-id="75f27-155">첫 번째 단계는 SSH (Secure Shell) 용 공개 키와 PGP (매우 좋은 개인 정보)의 복사본을 가져오는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-155">The first step is to obtain a copy of the public keys for Secure Shell (SSH) and Pretty Good Privacy (PGP).</span></span> <span data-ttu-id="75f27-156">2 단계에서 이러한 키를 사용 하 여 3 단계에서 만든 커넥터에서 SFTP 사이트에 연결 하 고 인스턴트 Bloomberg 채팅 데이터를 Office 365 사서함으로 전송 하도록 Bloomberg SFTP 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-156">You use these keys in Step 2 to configure the Bloomberg SFTP site to allow the connector (that you create in Step 3) to connect to the SFTP site and transfer the Instant Bloomberg chat data to Office 365 mailboxes.</span></span> <span data-ttu-id="75f27-157">또한 Bloomberg SFTP 사이트를 구성할 때 사용 하는이 단계에서 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-157">You also obtain an IP address in this step, which you use when configuring the Bloomberg SFTP site.</span></span>

1. <span data-ttu-id="75f27-158">로 이동한 후 **데이터 거 버 넌 \> 스 가져오기를** 클릭 한 다음 **타사 데이터 보관**을 클릭 합니다. <https://protection.office.com></span><span class="sxs-lookup"><span data-stu-id="75f27-158">Go to <https://protection.office.com> and then click **Data governance \> Import** and then click **Archive third-party data**.</span></span>

2. <span data-ttu-id="75f27-159">**타사 데이터 보관** 페이지에서 **커넥터 추가**를 클릭 한 다음 **인스턴트 Bloomberg**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-159">On the **Archive third-party data** page, click **Add a connector**, and then click **Instant Bloomberg**.</span></span>

3. <span data-ttu-id="75f27-160">**서비스 약관** 페이지에서 **수락**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-160">On the **Terms of service** page, click **Accept**.</span></span>

4. <span data-ttu-id="75f27-161">1 단계 아래에 있는 **Bloomberg에 대 한 자격 증명 추가 사이트** 에서 **SSH 키 다운로드** 및 **PGP 키** 다운로드 링크 다운로드를 클릭 하 여 각 공개 키 파일의 복사본을 로컬 컴퓨터에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-161">On the **Add credentials for Bloomberg SFTP site** under step 1, click **Download SSH key** and **Download PGP key** download links to save a copy of each public key file to your local computer.</span></span> <span data-ttu-id="75f27-162">이러한 파일에는 2 단계에서 Bloomberg SFTP 사이트를 구성 하는 데 사용 되는 다음과 같은 항목이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-162">These files contain the following items that will be used to configure the Bloomberg SFTP site in Step 2:</span></span>

   - <span data-ttu-id="75f27-163">SSH 공개 키-이 키는 커넥터가 Bloomberg SFTP 사이트에 연결 될 때 보안 원격 로그인을 사용 하도록 허용 하도록 SSH (Secure Shell)를 구성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-163">SSH public key – This key will be used to configure Secure Shell (SSH) to enable a secure remote login when the connector connects to the Bloomberg SFTP site.</span></span>

   - <span data-ttu-id="75f27-164">PGP 공개 키-이 키는 Bloomberg SFTP 사이트에서 Office 365로 전송 되는 데이터의 암호화를 구성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-164">PGP public key – This key will be used to configure the encryption of data that's transferred from the Bloomberg SFTP site to Office 365.</span></span>

   - <span data-ttu-id="75f27-165">IP 주소-Bloomberg SFTP 사이트는 3 단계에서 만든 인스턴트 Bloomberg 커넥터에서 사용 하는이 IP 주소 로부터의 연결 요청만 수락 하도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-165">IP address – The Bloomberg SFTP site will be configured to accept a connection request only from this IP address, which is used by the Instant Bloomberg connector that you create in Step 3.</span></span> 

5. <span data-ttu-id="75f27-166">**취소** 를 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-166">Click **Cancel** to close the wizard.</span></span> <span data-ttu-id="75f27-167">3 단계의이 마법사로 돌아와서 커넥터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-167">You come back to this wizard in Step 3 to create the connector.</span></span>

## <a name="step-2-configure-the-bloomberg-sftp-site"></a><span data-ttu-id="75f27-168">2 단계: Bloomberg SFTP 사이트 구성</span><span class="sxs-lookup"><span data-stu-id="75f27-168">Step 2: Configure the Bloomberg SFTP site</span></span>

<span data-ttu-id="75f27-169">다음 단계에서는 1 단계에서 가져온 SSH 및 PGP 공개 키와 IP 주소를 사용 하 여 Bloomberg SFTP 사이트에 대 한 SSH 인증 및 PGP 암호화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-169">The next step is to use the SSH and PGP public keys and the IP address that you obtained in Step 1 to configure SSH authentication and PGP encryption for the Bloomberg SFTP site.</span></span> <span data-ttu-id="75f27-170">이렇게 하면 3 단계에서 만든 인스턴트 Bloomberg 커넥터를 사용 하 여 Bloomberg SFTP 사이트에 연결 하 고 인스턴트 Bloomberg 데이터를 Office 365에 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-170">This allows the Instant Bloomberg connector that you create in Step 3 to connect to the Bloomberg SFTP site and transfer Instant Bloomberg data to Office 365.</span></span> <span data-ttu-id="75f27-171">이 기능을 설정 하는 데 도움이 필요한 경우 [Bloomberg 고객 지원](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) 에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="75f27-171">Contact [Bloomberg customer support](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) if you need assistance setting this up.</span></span>

1. <span data-ttu-id="75f27-172">조직의 계정을 사용 하 여 Bloomberg CCNS 제어판에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-172">Log in to the Bloomberg CCNS control panel using an account for your organization.</span></span>

2. <span data-ttu-id="75f27-173">CCNS로 이동 하 여 **공개 키** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-173">Go to CCNS and click the **Public Keys** tab.</span></span>

3. <span data-ttu-id="75f27-174">SSH 인증을 사용 하도록 설정 하려면 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-174">To enable SSH authentication, click **Add**.</span></span>

4. <span data-ttu-id="75f27-175">**공개 키 추가** 창에서 **키 유형** 드롭다운 목록을 클릭 한 다음 **로그인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-175">In the **Add Public Key** window, click the **Key Type** dropdown list, and then click **Login**.</span></span>

5. <span data-ttu-id="75f27-176">1 단계에서 다운로드 한 전체 SSH 공개 키 (큰따옴표를 포함 하지 않고 큰따옴표로 묶은 모든 문자)를 복사 하 여이 필드에 붙여 넣은 다음 **제출을** 클릭 하 여 키를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-176">Copy the entire SSH public key (all characters between, but not including, the double quotation marks) that you downloaded in Step 1, paste it in this field, and then click **Submit** to save the key.</span></span>
 
    <span data-ttu-id="75f27-177">예를 들어 다음 SSH 공개 키를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-177">For example, you would copy the following SSH public key:</span></span>

    `
    ssh-rsa
    AAAAB3NzaC1yc2EAAAABIwAAAQEA1dxAyc0JzCmc5NzgyzRYhnj3FGHK5Kd9T2cwZNkmL/9nFhQupQor081rmuw9gACAmeot7y+V/fmijo/q4rxDe3Auu3hfLl1NpWlIssQJHzycms8zimtdQcXbMKwDQOnRthpEocF5ySs76KE72vaYQJTvclAamWWq0D75SUmXDFFr7afvEy57F7KgMD1ecg6lH7q8seSKbiiWxX1Ul0kL15fzpUyhjDP41owb1XC/dF7fJwAmCO1+HZfDLEp62q4tnApLpdd92KoR41LZTryO5dICKhk+S+JxPLkksxL0wm5YevOr2n4ScuRdsBV8mWKZ1Xw+cOss9O6L7cCcEiB3Ow==
    `

6. <span data-ttu-id="75f27-178">PGP 암호화를 사용 하도록 설정 하려면 **공개 키** 탭에서 다시 **추가** 를 클릭 하 고 **키 형식** 드롭다운 목록을 클릭 한 다음이 시간에 **암호화**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-178">To enable PGP encryption, click **Add** again on the **Public Keys** tab, click the **Key Type** dropdown list, and this time click **Encryption**.</span></span>

7. <span data-ttu-id="75f27-179">1 단계에서 다운로드 한 전체 PGP 공개 키 (큰따옴표를 포함 하지 않고 큰따옴표로 묶은 모든 문자)를 복사 하 여이 필드에 붙여 넣은 다음 **제출을** 클릭 하 여 키를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-179">Copy the entire PGP public key (all characters between, but not including, the double quotation marks) that you downloaded in Step 1, paste it in this field, and then click **Submit** to save the key.</span></span> 

    <span data-ttu-id="75f27-180">예를 들어 다음 PGP 공개 키를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-180">For example, you would copy the following PGP public key:</span></span>

    `
    -----BEGIN PGP PUBLIC KEY BLOCK-----
    Version: BCPG C# v1.7.4137.9688
    nmQENBFz+6UQBCACKC4ilYoVOP5b/F0CO+oQYbag79Ov4NZxM4EKW51lUAvKNExRM\nc1C/gwXm8bghht8GEODckXXqx8qSSXUEeA/ROweXNtD1u1kn7PgYEFUeD/qE739m\nm5lxXF9Vod26AtKQ9Y1EvYoQEltwztAaXg8K8LQzB+tzN079d1cxM5tbiRQLttAh\nOt5amLXuINt8+dWyNas3DfgIBUmwfkwCbUO0ElrIhvvO3A85K97SX9Q6Py0SkfkK\nQpnULuhdjSm+7k7qlVMf0s8e/9jUXYKbMFkxlOoMq052vV0l0VQNSeuKoC+m6+LT\nEPab89AMt6S4Ujum9wTUy1eWNx9vV0y/w8N7ABEBAAG0JDM5MjM4ZTg3LWI1YWIt\nNGVmNi1hNTU5LWFmNTRjNmIwN2I0MokBHAQQAQIABgUCXP7pRAAKCRAJQdjaG//S\nCy70B/wKrR2CcqtZx56yrGJFfVy3niEt16VEA3xJM3D9nX0gmgo85Nh5gkiY3ahH\nnNEmgW5vlCM1gcgFeoZWe8A80G4QoabslSUzLbq9HsHOOAQApsfhrhXpylrAVa4n\nI53XUOxWdOTa4xsOob8hSRADqJbwHPOsoAr2A87TvZ9LSi2Mii5omeTq416CLnoS\nPBAEhelZm+ruy5JhzA1yXvWYFH08wNqSHO3bskdES2yW5SyQmYlcoEztWE0Q0Z+G\nZT3kOa/W2MbcZovFCQIfqhwVfXtIzx5uYUmxgk5cFKUJJMlO0AZK/HwM22xuuIWe\ndMa6OMo/n8tvEBxrLQMdVPlz+hZ6
    =AwmP
    -----END PGP PUBLIC KEY BLOCK-----
    `
8. <span data-ttu-id="75f27-181">CCNS 제어판의 주 창에서 **여기에 IP 주소 추가**에 **주소 추가 필드**의 다음 Ip 주소 (1 단계에서 다운로드 한 Keys 파일에 포함 됨)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-181">Back on the main window of the CCNS control panel, under **Add your IP address here**, enter the following IP address (which is included in Keys.txt file that you downloaded in Step 1) in the **Add address field**.</span></span>

   `
   40.124.28.216
   `

## <a name="step-3-create-an-instant-bloomberg-connector"></a><span data-ttu-id="75f27-182">3 단계: 인스턴트 Bloomberg 커넥터 만들기</span><span class="sxs-lookup"><span data-stu-id="75f27-182">Step 3: Create an Instant Bloomberg connector</span></span>

<span data-ttu-id="75f27-183">마지막 단계는 보안 & 준수 센터에서 인스턴트 Bloomberg 커넥터를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-183">The last step is to create an Instant Bloomberg connector in the Security & Compliance Center.</span></span> <span data-ttu-id="75f27-184">커넥터는 제공 하는 정보를 사용 하 여 Bloomberg SFTP 사이트에 연결 하 고 채팅 메시지를 Office 365의 해당 사용자 사서함 상자로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-184">The connector uses the information you provide to connect to the Bloomberg SFTP site and transfer chat messages to the corresponding user mailbox boxes in Office 365.</span></span> 

1. <span data-ttu-id="75f27-185">로 이동한 후 **데이터 거 버 넌 \> 스 가져오기를** 클릭 한 다음 **타사 데이터 보관**을 클릭 합니다. <https://protection.office.com></span><span class="sxs-lookup"><span data-stu-id="75f27-185">Go to <https://protection.office.com> and then click **Data governance \> Import** and then click **Archive third-party data**.</span></span>

2. <span data-ttu-id="75f27-186">**타사 데이터 보관** 페이지에서 **커넥터 추가**를 클릭 한 다음 **인스턴트 Bloomberg**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-186">On the **Archive third-party data** page, click **Add a connector**, and then click **Instant Bloomberg**.</span></span>

3. <span data-ttu-id="75f27-187">**서비스 약관** 페이지에서 **수락**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-187">On the **Terms of service** page, click **Accept**.</span></span>

4. <span data-ttu-id="75f27-188">**BLOOMBERG SFTP 사이트에 대 한 자격 증명 추가** 페이지의 3 단계에서 다음 상자에 필요한 정보를 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-188">On the **Add credentials for Bloomberg SFTP site** page, under Step 3, enter the required information in the following boxes and then click **Next**.</span></span>

    - <span data-ttu-id="75f27-189">**회사 코드** – 조직의 ID 이며 Bloomberg SFTP 사이트의 사용자 이름으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-189">**Firm code** – The ID for your organization and used as the username for the Bloomberg SFTP site.</span></span>

    - <span data-ttu-id="75f27-190">**Password** -Bloomberg SFTP 사이트의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-190">**Password** – Password for Bloomberg SFTP site</span></span>

    - <span data-ttu-id="75f27-191">**SFTP url** -Bloomberg SFTP 사이트의 URL (예: sftp.bloomberg.com)입니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-191">**SFTP URL** – The URL for Bloomberg SFTP site (for example, sftp.bloomberg.com).</span></span>

    - <span data-ttu-id="75f27-192">**SFTP 포트** -Bloomberg SFTP 사이트의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-192">**SFTP port** – The port number for Bloomberg SFTP site.</span></span> <span data-ttu-id="75f27-193">커넥터는이를 사용 하 여 SFTP 사이트에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-193">The connector uses this to connect to the SFTP site.</span></span>

5. <span data-ttu-id="75f27-194">**대체 사서함** 페이지에서 조직의 사용자 사서함에 연결할 수 없는 인스턴트 Bloomberg 채팅 메시지를 저장 하는 데 사용 되는 사서함의 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-194">On the **Alternative mailbox** page, type the email address of a mailbox that will be used to store chat messages from Instant Bloomberg that can't be associated with a user mailbox in your organization.</span></span>

   > [!NOTE]
   > <span data-ttu-id="75f27-195">인스턴트 Bloomberg에 있는 모든 대화의 모든 채팅 메시지에는 채팅 참가자의 조직의 전자 메일 주소를 포함 하는 *CorporateEmailAddress*라는 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-195">Every chat message in every conversation in Instant Bloomberg includes a property called *CorporateEmailAddress*, which contains your organization's email address for the chat participant.</span></span> <span data-ttu-id="75f27-196">가져오기 프로세스 중에 커넥터는 *CorporateEmailAddress* 속성에 있는 것과 동일한 전자 메일 주소를 가진 Office 365의 사용자 사서함으로 채팅 메시지를 가져오려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-196">During the import process, the connector attempts to import chat messages to a user mailbox in Office 365 that has the same email addresses that matches the one in the *CorporateEmailAddress* property.</span></span> <span data-ttu-id="75f27-197">*CorporateEmailAddress* 속성에 있는 것과 같은 주소를 가진 Office 365 사서함이 없는 경우 커넥터는이 페이지에서 지정한 대체 사서함으로 채팅 메시지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-197">If the there isn't an Office 365 mailbox with the same address as the one in the *CorporateEmailAddress* property, the connector imports the chat message to the alternative mailbox that you specify on this page.</span></span> <span data-ttu-id="75f27-198">현재 대체 사서함에 보관 된 인스턴트 Bloomberg 채팅 메시지는 Office 365의 감독 정책에 의해 모니터링 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-198">At this time, Instant Bloomberg chat messages archived in the alternative mailbox aren't monitored by supervision policies in Office 365.</span></span>

6. <span data-ttu-id="75f27-199">**다음**을 클릭 하 고 설정을 검토 한 다음 **준비** 를 클릭 하 여 커넥터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-199">Click **Next**, review your settings, and then click **prepare** to create the connector.</span></span>

7. <span data-ttu-id="75f27-200">**타사 데이터 보관** 페이지로 이동 하 여 새 커넥터에 대 한 가져오기 프로세스의 진행 상황을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f27-200">Go to the **Archive third-party data** page to see the progress of the import process for the new connector.</span></span>
