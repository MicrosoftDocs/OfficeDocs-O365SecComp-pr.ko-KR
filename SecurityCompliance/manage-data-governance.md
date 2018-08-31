---
title: Office 365의 관리 방식 데이터를 관리 합니다.
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 5/9/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 48064107-fed2-4db0-9e5c-aa5ddd5ccb09
description: 데이터 관리 방식은 모두에 대 한 필요할 때 중심으로 데이터를 유지 하 고 가져오는 제거할 그렇지 않은 경우. Office 365의 관리 방식 데이터를 유지 하 고 끝에 콘텐츠를 영구적으로 삭제 하는 정책을 작성을 시작 부분에 데이터를 저장 하 고 가져오기 (영문)에서 전체 콘텐츠 수명 주기를 관리할 수 있습니다.
ms.openlocfilehash: ca3443c3b90a067bf171ddf89be604d262a7b9a4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534016"
---
# <a name="manage-data-governance-in-office-365"></a><span data-ttu-id="268b5-104">Office 365의 관리 방식 데이터를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-104">Manage data governance in Office 365</span></span>

<span data-ttu-id="268b5-p102">데이터 관리 방식은 모두에 대 한 필요할 때 중심으로 데이터를 유지 하 고 가져오는 제거할 그렇지 않은 경우. Office 365의 관리 방식 데이터를 유지 하 고 끝에 콘텐츠를 영구적으로 삭제 하는 정책을 작성을 시작 부분에 데이터를 저장 하 고 가져오기 (영문)에서 전체 콘텐츠 수명 주기를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-p102">Data governance is all about keeping your data around when you need it and getting rid of it when you don't. With data governance in Office 365, you can manage the full content lifecycle, from importing and storing data at the beginning, to creating policies that retain and then permanently delete content at the end.</span></span>
  
## <a name="import"></a><span data-ttu-id="268b5-107">가져오기</span><span class="sxs-lookup"><span data-stu-id="268b5-107">Import</span></span>

<span data-ttu-id="268b5-p103">데이터의 일부 클라우드, 온-프레미스 서버와 같이 또는 타사 응용 프로그램의 외부 위치에 저장 될 수 있습니다. 가져오기 서비스를 사용 하면 쉽게 메시징, SharePoint 및 OneDrive 비즈니스 데이터에 대 한 네트워크를 통해 직접 업로드 하거나 정보를 보면는 암호화 된 드라이브를 전달 하 여 Office 365로 가져올 수 있습니다. 대상 사서함에 실제로 가져온 PST 파일에 항목을 필터링 하는 가져오기 서비스에서 지능형 가져오기 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-p103">Some of your data might be stored in places outside the cloud, like on-premises servers or in third-party apps. The Import service makes it easy to bring your messaging, SharePoint, and OneDrive for Business data into Office 365, either by uploading it directly over the network or shipping an encrypted drive to us. You can also use the Intelligent Import feature in the Import service to filter the items in PST files that actually get imported to the target mailboxes.</span></span> 
  
- [<span data-ttu-id="268b5-111">Office 365에 PST 파일 가져오기 (영문)의 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="268b5-111">Overview of importing PST files to Office 365</span></span>](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84)
    
- [<span data-ttu-id="268b5-112">네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="268b5-112">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
    
- [<span data-ttu-id="268b5-113">드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="268b5-113">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- [<span data-ttu-id="268b5-114">PST 컬렉션 도구를 사용 하 여 찾기, 복사 및 조직에서 PST 파일을 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="268b5-114">Use the PST Collection Tool to find, copy, and delete PST files in your organization</span></span>](find-copy-and-delete-pst-files-in-your-organization.md)
    
- [<span data-ttu-id="268b5-115">Office 365에 PST 파일을 가져올 때 데이터를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-115">Filter data when importing PST files to Office 365</span></span>](filter-data-when-importing-pst-files.md)
    
- [<span data-ttu-id="268b5-116">PowerShell cmdlet을 사용하여 SharePoint Online에 온-프레미스 콘텐츠 업로드</span><span class="sxs-lookup"><span data-stu-id="268b5-116">Upload on-premises content to SharePoint Online using PowerShell cmdlets</span></span>](https://support.office.com/article/555049c6-15ef-45a6-9a1f-a1ef673b867c)
    
## <a name="govern-i-store-data"></a><span data-ttu-id="268b5-117">I: 저장소 데이터를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-117">Govern I: Store data</span></span>

<span data-ttu-id="268b5-p104">데이터를 가져온 후 저장소가 증가 해야할 수 있습니다. (호출 자동 확장 보관) Office 365의 무제한 보관 기능의 보관 사서함에 저장 무제한 금액을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-p104">After you import data, you might need to increase your storage. The unlimited archiving feature in Office 365 (called auto-expanding archiving) provides an unlimited amount of storage in archive mailboxes.</span></span>
  
- [<span data-ttu-id="268b5-120">Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="268b5-120">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>](enable-archive-mailboxes.md)

- [<span data-ttu-id="268b5-121">Office 365 무제한 보관의 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="268b5-121">Overview of unlimited archiving in Office 365</span></span>](unlimited-archiving.md)
    
- [<span data-ttu-id="268b5-122">Office 365 무제한 보관을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="268b5-122">Enable unlimited archiving in Office 365</span></span>](enable-unlimited-archiving.md)
    

    
## <a name="govern-ii-create-policies-and-labels-to-retain-content"></a><span data-ttu-id="268b5-123">정책 및 콘텐츠를 유지 하려면 레이블 만들기 II를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-123">Govern II: Create policies and labels to retain content</span></span>

<span data-ttu-id="268b5-p105">보존 정책 준수 사전 업계 규정 및 내부 정책 보다 더 이상 하지만 필요에 따라 같이 긴 콘텐츠를 보관할 수 있도록 하 여 하는데 도움이 됩니다. 단일 보존 정책에는 전체 조직에 나타날 수 있습니다. 또한 관리 방식에 대 한 조직 전체에서 데이터를 분류 하 고 다음 해당 분류에 따라 보존 규칙을 적용 하 여 파일 계획을 구현 하려면 레이블을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-p105">A retention policy helps you to comply proactively with industry regulations and internal policies by ensuring that you retain content as long as required but no longer than that. A single retention policy can cover your entire organization. In addition, you can use labels to implement a file plan by classifying data across your organization for governance, and then enforcing retention rules based on that classification.</span></span>
  
- [<span data-ttu-id="268b5-127">보존 정책 개요</span><span class="sxs-lookup"><span data-stu-id="268b5-127">Overview of retention policies</span></span>](retention-policies.md)
    
- [<span data-ttu-id="268b5-128">레이블 개요</span><span class="sxs-lookup"><span data-stu-id="268b5-128">Overview of labels</span></span>](labels.md)
    
- [<span data-ttu-id="268b5-129">대량 만들기 및 PowerShell을 사용 하 여 레이블을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-129">Bulk create and publish labels by using PowerShell</span></span>](https://support.office.com/article/8986701b-ffa1-46ec-8fd0-8f7e81d5b25f.aspx)
    
- [<span data-ttu-id="268b5-130">처리 검토 개요</span><span class="sxs-lookup"><span data-stu-id="268b5-130">Overview of disposition reviews</span></span>](disposition-reviews.md)
    
- [<span data-ttu-id="268b5-131">이벤트 구동 보존 개요</span><span class="sxs-lookup"><span data-stu-id="268b5-131">Overview of event-driven retention</span></span>](event-driven-retention.md)
    
## <a name="govern-iii-retain-the-email-of-former-employees"></a><span data-ttu-id="268b5-132">이전 직원의 전자 메일을 유지 III를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-132">Govern III: Retain the email of former employees</span></span>

<span data-ttu-id="268b5-p106">사용자 조직에서 나가는 경우 비활성 사서함을 만들어 전자 메일을 유지할 수 있습니다. 사서함을 소송 보존을 Office 365 보존 정책, 비활성화 됩니다 또는 다른 유형의 보류에 적용 되 하 고 해당 Office 365 사용자 계정을 삭제 합니다. 비활성 사서함의 항목은 보류 또는 보존 정책 비활성 적용 되기 전에 사서함에 설정 된 기간 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-p106">When a person leaves your organization, you can retain their email by creating an inactive mailbox. A mailbox becomes inactive when a Litigation Hold, Office 365 retention policy, or other type of hold is applied to it, and then the corresponding Office 365 user account is deleted. Items in an inactive mailbox are retained for the duration of the hold or retention policy that was placed on the mailbox before it was made inactive.</span></span>
  
- [<span data-ttu-id="268b5-136">Office 365에서 비활성 사서함의 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="268b5-136">Overview of inactive mailboxes in Office 365</span></span>](inactive-mailboxes-in-office-365.md)
    
- [<span data-ttu-id="268b5-137">Office 365에서 비활성 사서함 만들기 및 관리</span><span class="sxs-lookup"><span data-stu-id="268b5-137">Create and manage inactive mailboxes in Office 365</span></span>](create-and-manage-inactive-mailboxes.md)

- [<span data-ttu-id="268b5-138">Office 365에서 비활성 사서함에 대 한 보존 기간 변경</span><span class="sxs-lookup"><span data-stu-id="268b5-138">Change the hold duration for an inactive mailbox in Office 365</span></span>](change-the-hold-duration-for-an-inactive-mailbox.md)
  
- [<span data-ttu-id="268b5-139">Office 365에서 비활성 사서함 복구</span><span class="sxs-lookup"><span data-stu-id="268b5-139">Recover an inactive mailbox in Office 365</span></span>](recover-an-inactive-mailbox.md)
 
- [<span data-ttu-id="268b5-140">Office 365에서 비활성 사서함 복원</span><span class="sxs-lookup"><span data-stu-id="268b5-140">Restore an inactive mailbox in Office 365</span></span>](restore-an-inactive-mailbox.md)

- [<span data-ttu-id="268b5-141">Office 365에서 비활성 사서함 삭제</span><span class="sxs-lookup"><span data-stu-id="268b5-141">Delete an inactive mailbox in Office 365</span></span>](delete-an-inactive-mailbox.md)

## <a name="monitor"></a><span data-ttu-id="268b5-142">모니터링</span><span class="sxs-lookup"><span data-stu-id="268b5-142">Monitor</span></span>

<span data-ttu-id="268b5-p107">감독 내부 또는 외부 검토자가 검사할 수 있도록 전자 메일 및 조직에서 타사 통신 캡처 하는 정책을 정의할 수 있습니다. 검토자가 이러한 통신을 분류, 그들은 조직의 정책 준수 하는지 확인 하 고 수 필요한 경우 의심 스러운 자료를 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-p107">Supervision lets you define policies that capture email and 3rd-party communications in your organization so they can be examined by internal or external reviewers. Reviewers can then classify these communications, make sure they're compliant with your organization's policies, and escalate questionable material if necessary.</span></span>
  
<span data-ttu-id="268b5-145">레이블을 의도 한 대로 콘텐츠에 적용 되는 모니터링 데이터 관리 보고서 및 레이블 활동 탐색기를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268b5-145">You can also use the data governance reports and the Label Activity Explorer to monitor that your labels are being applied to content as you intended.</span></span>
  
- [<span data-ttu-id="268b5-146">조직에 대한 감독 정책 구성</span><span class="sxs-lookup"><span data-stu-id="268b5-146">Configure supervision policies for your organization</span></span>](configure-supervision-policies.md)
    
- [<span data-ttu-id="268b5-147">감독 보고서</span><span class="sxs-lookup"><span data-stu-id="268b5-147">Supervision reports</span></span>](supervision-reports.md)
    
- [<span data-ttu-id="268b5-148">문서에 대한 레이블 활동 보기</span><span class="sxs-lookup"><span data-stu-id="268b5-148">View label activity for documents</span></span>](view-label-activity-for-documents.md)
    
- [<span data-ttu-id="268b5-149">데이터 거버넌스 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="268b5-149">View the data governance reports</span></span>](view-the-data-governance-reports.md)
    
## <a name="more-information"></a><span data-ttu-id="268b5-150">추가 정보</span><span class="sxs-lookup"><span data-stu-id="268b5-150">More information</span></span>

- [<span data-ttu-id="268b5-151">Microsoft 데이터 관리 팀의 비디오 보기</span><span class="sxs-lookup"><span data-stu-id="268b5-151">Watch videos from the Microsoft Data Governance team</span></span>](https://go.microsoft.com/fwlink/?linkid=867039)
    
- [<span data-ttu-id="268b5-152">Office 365에서 데이터 관리 방식 개요 비디오 시청</span><span class="sxs-lookup"><span data-stu-id="268b5-152">Watch an overview of data governance in Office 365</span></span>](https://go.microsoft.com/fwlink/?linkid=852644)
    
- [<span data-ttu-id="268b5-153">Office 365 보안 &amp; 준수 센터 cmdlet</span><span class="sxs-lookup"><span data-stu-id="268b5-153">Office 365 Security &amp; Compliance Center cmdlets</span></span>](https://go.microsoft.com/fwlink/?linkid=852310)
    

