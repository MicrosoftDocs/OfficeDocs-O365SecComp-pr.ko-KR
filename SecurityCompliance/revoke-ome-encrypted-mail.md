---
title: Office 365 고급 메시지 암호화로 암호화된 전자 메일 취소
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: Office 365 관리자는 Office 365 고급 메시지 암호화로 암호화 된 특정 전자 메일을 해지할 수 있습니다.
ms.openlocfilehash: e55129f68c7add589bd973b36f069d7cdbf631cf
ms.sourcegitcommit: 5a93c2f3df35d06a59a7fbaff5c91f7afde11781
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34857618"
---
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="e9588-103">Office 365 고급 메시지 암호화로 암호화된 전자 메일 취소</span><span class="sxs-lookup"><span data-stu-id="e9588-103">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="e9588-104">전자 메일 해지가 Office 365 Advanced Message 암호화의 일부로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="e9588-105">Office 365에서는 특정 구독의 Office 365 메시지 암호화 중 위에서 고급 메시지 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-105">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="e9588-106">고급 메시지 암호화는 [Microsoft 365 Enterprise e5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5 및 Office 365 교육 A5에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-106">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="e9588-107">조직에 Office 365 고급 메시지 암호화를 포함 하지 않는 Office 365 구독이 있는 경우 고급 메시지 암호화는 Advanced 준수 SKU의 E5 규격을 사용 하 여 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-107">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="e9588-108">이 문서는 [Office 365 메시지 암호화](ome.md)에 대 한 보다 광범위 한 문서에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-108">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="e9588-109">Office 365 고급 메시지 암호화를 사용 하 여 메시지를 암호화 했으며 Office 365 관리자 인 경우 특정 조건에서 메시지를 해지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-109">If a message was encrypted using Office 365 Advanced Message Encryption, and you are an Office 365 admin, you can do revoke the message under certain conditions.</span></span> <span data-ttu-id="e9588-110">이 문서에서는 해지가 가능한 상황 및 수행 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-110">This article describes the circumstances under which revocation is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="e9588-111">해지할 수 있는 암호화 된 전자 메일</span><span class="sxs-lookup"><span data-stu-id="e9588-111">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="e9588-112">받는 사람이 링크 기반 브랜드의 암호화 된 전자 메일을 받은 경우 암호화 된 전자 메일을 해지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-112">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="e9588-113">받는 사람이 지원 되는 Outlook 클라이언트에서 기본 인라인 환경을 받은 경우 해당 전자 메일을 해지할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-113">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="e9588-114">받는 사람이 링크 기반 환경이 나 인라인 환경을 수신 하는지 여부는 받는 사람 id 유형에 따라 다릅니다. Office 365 및 Microsoft 계정 받는 사람 (예: outlook.com users)은 지원 되는 Outlook 클라이언트에서 인라인 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-114">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="e9588-115">Gmail 받는 사람과 같은 다른 모든 받는 사람 유형은 링크 기반 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-115">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="e9588-116">해지 된 암호화 전자 메일에 대 한 받는 사람 환경</span><span class="sxs-lookup"><span data-stu-id="e9588-116">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="e9588-117">전자 메일이 해지 되 면 Office 365 메시지 암호화 포털: "보낸 사람이 메시지를 철회 했습니다." 라는 오류가 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-117">Once an email has been revoked, the recipient receives an error when they access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![암호화 된 전자 메일을 해지 한 것을 보여 주는 스크린샷](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="e9588-119">암호화 된 전자 메일을 해지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="e9588-119">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="e9588-120">1단계.</span><span class="sxs-lookup"><span data-stu-id="e9588-120">Step 1.</span></span> <span data-ttu-id="e9588-121">전자 메일의 메시지 ID 가져오기</span><span class="sxs-lookup"><span data-stu-id="e9588-121">Obtain the Message ID of the email</span></span>

<span data-ttu-id="e9588-122">암호화 된 메일을 해지 하려면 먼저 메일의 메시지 ID를 수집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-122">Before you can revoke an encrypted mail you gather the Message ID of the mail.</span></span> <span data-ttu-id="e9588-123">MessageId는 대개 다음 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-123">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="e9588-124">해지할 전자 메일의 메시지 ID를 확인 하는 방법에는 여러 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-124">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="e9588-125">이 섹션에서는 몇 가지 옵션에 대해 설명 하지만 ID를 제공 하는 모든 메서드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-125">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="e9588-126">보안 &amp; 및 준수 센터에서 메시지 추적을 사용 하 여 해지할 전자 메일의 메시지 ID를 식별 하려면</span><span class="sxs-lookup"><span data-stu-id="e9588-126">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="e9588-127">[Office 365 보안 & 준수 센터의 새 메시지 추적을](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)사용 하 여 보낸 사람 또는 받는 사람에 대 한 전자 메일을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-127">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="e9588-128">전자 메일을 찾은 후에는이를 선택 하 여 **메시지 추적 세부 정보** 창을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-128">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="e9588-129">**자세한 정보** 를 확장 하 여 메시지 ID를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-129">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="e9588-130">보안 &amp; 및 준수 센터에서 Office 메시지 암호화 보고서를 사용 하 여 해지할 전자 메일의 메시지 ID를 식별 하려면</span><span class="sxs-lookup"><span data-stu-id="e9588-130">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="e9588-131">보안 &amp; 및 준수 센터에서 **메시지 암호화 보고서**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-131">In the Security &amp; Compliance Center, navigate to the **Message encryption report**.</span></span> <span data-ttu-id="e9588-132">이 보고서에 대 한 자세한 내용은 [보안 &amp; 및 준수 센터의 전자 메일 보안 보고서 보기](view-email-security-reports.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e9588-132">For information on this report, see [View email security reports in the Security &amp; Compliance Center](view-email-security-reports.md).</span></span>

2. <span data-ttu-id="e9588-133">**정보 보기** 테이블을 선택 하 고 해지할 메시지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-133">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="e9588-134">메시지를 두 번 클릭 하 여 메시지 ID를 포함 하는 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-134">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="e9588-135">2단계.</span><span class="sxs-lookup"><span data-stu-id="e9588-135">Step 2.</span></span> <span data-ttu-id="e9588-136">메일이 revocable 확인</span><span class="sxs-lookup"><span data-stu-id="e9588-136">Verify that the mail is revocable</span></span>

<span data-ttu-id="e9588-137">메시지를 취소할 수 있는지 여부를 확인 하려면 보안 &amp; 및 준수 센터의 Details ( **정보** ) 테이블에서 암호화 보고서에 해지 상태 필드를 표시할지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-137">To verify whether you can revoke a message, check whether the Revocation Status field is visible in the Encryption report, in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="e9588-138">Windows Powershell을 사용 하 여 특정 전자 메일 메시지를 해지할 수 있는지 여부를 확인 하려면 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-138">To verify whether you can revoke a particular email message by using Windows Powershell, complete these steps.</span></span>

1. <span data-ttu-id="e9588-139">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="e9588-140">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e9588-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="e9588-141">다음과 같이 OMEMessageStatus cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-141">Run the Get-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="e9588-142">메시지의 제목과 메시지의 revocable 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="e9588-143">For example,</span><span class="sxs-lookup"><span data-stu-id="e9588-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="e9588-144">3단계.</span><span class="sxs-lookup"><span data-stu-id="e9588-144">Step 3.</span></span> <span data-ttu-id="e9588-145">메일 해지</span><span class="sxs-lookup"><span data-stu-id="e9588-145">Revoke the mail</span></span>

<span data-ttu-id="e9588-146">해지할 전자 메일의 메시지 ID를 알고 있고 메시지가 revocable 확인 되 면 보안 &amp; 준수 센터 또는 Windows Powershell을 사용 하 여 전자 메일을 해지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email using the Security &amp; Compliance Center or Windows Powershell.</span></span>

<span data-ttu-id="e9588-147">보안 &amp; 및 준수 센터를 사용 하 여 메시지를 해지 하려면</span><span class="sxs-lookup"><span data-stu-id="e9588-147">To revoke the message using the Security &amp; Compliance Center</span></span>

<span data-ttu-id="e9588-148">보안 &amp; 및 준수 센터에서 전자 메일을 해지 하려면 암호화 보고서의 메시지에 대 한 **세부 정보** 테이블에서 **메시지 해지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-148">To revoke the email in the Security &amp; Compliance Center, in the Encryption report, in the **Details** table for the message, choose **Revoke message**.</span></span>

<span data-ttu-id="e9588-149">OMEMessageRevocation cmdlet을 사용 하 여 Windows Powershell을 사용 하 여 전자 메일을 해지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-149">You can revoke an email by using Windows Powershell by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="e9588-150">[Exchange Online PowerShell에 연결합니다](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="e9588-150">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="e9588-151">다음과 같이 OMEMessageRevocation cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-151">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="e9588-152">전자 메일이 해지 되었는지 확인 하려면 다음과 같이 OMEMessageStatus cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-152">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="e9588-153">해지가 성공한 경우 cmdlet은 다음 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9588-153">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="e9588-154">Office 365 고급 메시지 암호화에 대 한 추가 정보</span><span class="sxs-lookup"><span data-stu-id="e9588-154">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="e9588-155">Office 365 고급 메시지 암호화</span><span class="sxs-lookup"><span data-stu-id="e9588-155">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="e9588-156">Office 365 고급 메시지 암호화-전자 메일 만료</span><span class="sxs-lookup"><span data-stu-id="e9588-156">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="e9588-157">메시지 정책 및 규정 준수 서비스 설명</span><span class="sxs-lookup"><span data-stu-id="e9588-157">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
