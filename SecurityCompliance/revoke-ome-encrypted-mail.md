---
title: Office 365 메시지 암호화로 암호화된 전자 메일 취소
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: office 365 관리자는 office 365 메시지 암호화로 암호화 된 특정 전자 메일을 해지할 수 있습니다.
ms.openlocfilehash: 75b5e46e25f447ddac0de5a7911d0df8385da6b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214898"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="7578c-103">Office 365 메시지 암호화 전자 메일 해지</span><span class="sxs-lookup"><span data-stu-id="7578c-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="7578c-p101">이 문서는 [Office 365 메시지 암호화](ome.md)에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 현재 암호화 된 전자 메일 해지가 미리 보기에 있습니다. 계속 해 서 제공 되는 기능 및 콘텐츠에 대 한 업데이트 및 변경 내용이 기대 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="7578c-p102">이미 전송 된 전자 메일을 해지 해야 할 수 있습니다. office 365 메시지 암호화를 사용 하 여 전자 메일을 암호화 했으며 office 365 관리자 인 경우 특정 조건에 따라 전자 메일에 대해이 작업을 수행할 수 있습니다. 이 문서에서는 가능한 상황 및이를 수행 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="7578c-110">해지할 수 있는 암호화 된 전자 메일</span><span class="sxs-lookup"><span data-stu-id="7578c-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="7578c-p103">받는 사람이 링크 기반 브랜드의 암호화 된 전자 메일을 받은 경우 암호화 된 전자 메일을 해지할 수 있습니다. 받는 사람이 지원 되는 Outlook 클라이언트에서 기본 인라인 환경을 받은 경우 해당 전자 메일을 해지할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="7578c-p104">받는 사람이 링크 기반 환경이 나 인라인 환경을 수신 하는지 여부는 받는 사람 id 유형에 따라 다릅니다. Office 365 및 Microsoft 계정 받는 사람 (예: outlook.com users)은 지원 되는 outlook 클라이언트에서 인라인 환경을 가져옵니다. Gmail 받는 사람과 같은 다른 모든 받는 사람 유형은 링크 기반 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="7578c-p105">곧 조직에서 받는 사람 id에 관계 없이 링크 기반 환경을 강제 적용 하는 기능이 제공 될 예정입니다. 이러한 방식으로 모든 받는 사람은 암호화 된 전자 메일을 읽고 회신할 수 있는 Office 365 메시지 암호화 포털에 대 한 링크를 포함 하는 브랜드 전자 메일을 받게 됩니다. 이러한 모든 암호화 된 전자 메일은 revocable 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="7578c-118">해지 된 암호화 전자 메일에 대 한 받는 사람 환경</span><span class="sxs-lookup"><span data-stu-id="7578c-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="7578c-119">전자 메일이 해지 되 면 받는 사람이 Office 365 메시지 암호화 포털: "보낸 사람이 메시지를 철회 했습니다."를 통해 암호화 된 전자 메일에 액세스 하려고 할 때 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![암호화 된 전자 메일을 해지 한 것을 보여 주는 스크린샷](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="7578c-121">암호화 된 전자 메일을 해지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="7578c-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="7578c-p106">1 단계 전자 메일의 메시지 ID 가져오기</span><span class="sxs-lookup"><span data-stu-id="7578c-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="7578c-p107">암호화 된 메일을 해지 하려면 먼저 메일의 메시지 ID를 수집 해야 합니다. MessageId는 대개 다음 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="7578c-p108">해지할 전자 메일의 메시지 ID를 확인 하는 방법에는 여러 가지가 있습니다. 이 섹션에서는 몇 가지 옵션에 대해 설명 하지만 ID를 제공 하는 모든 메서드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="7578c-128">보안 &amp; 및 준수 센터에서 메시지 추적을 사용 하 여 해지할 전자 메일의 메시지 ID를 식별 하려면</span><span class="sxs-lookup"><span data-stu-id="7578c-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="7578c-129">[Office 365 Security & 준수 센터의 새 메시지 추적을](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)사용 하 여 보낸 사람 또는 받는 사람에 대 한 전자 메일을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="7578c-p109">전자 메일을 찾은 후에는 **메시지 추적 세부 정보** 창을 표시 하도록 선택 합니다. **자세한 정보** 를 확장 하 여 메시지 ID를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="7578c-132">보안 &amp; 및 준수 센터에서 Office 메시지 암호화 보고서를 사용 하 여 해지할 전자 메일의 메시지 ID를 식별 하려면</span><span class="sxs-lookup"><span data-stu-id="7578c-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="7578c-133">보안 &amp; 및 준수 센터에서 **메시지 암호화 보고서**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="7578c-134">**정보 보기** 테이블을 선택 하 고 해지할 메시지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="7578c-135">메시지를 두 번 클릭 하 여 메시지 ID를 포함 하는 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="7578c-p110">2 단계 메일이 revocable 확인</span><span class="sxs-lookup"><span data-stu-id="7578c-p110">Step 2. Verify that the mail is revocable</span></span>

<span data-ttu-id="7578c-138">특정 전자 메일 메시지를 해지할 수 있는지 여부를 확인 하려면 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="7578c-p111">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7578c-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="7578c-141">다음과 같이 OMEMessageStatus cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="7578c-p112">메시지의 제목과 메시지의 revocable 여부를 반환 합니다. 예를 들어</span><span class="sxs-lookup"><span data-stu-id="7578c-p112">This returns the subject of the message and whether the message is revocable. For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="7578c-p113">3 단계 메일 해지</span><span class="sxs-lookup"><span data-stu-id="7578c-p113">Step 3. Revoke the mail</span></span>  

<span data-ttu-id="7578c-146">해지할 전자 메일의 메시지 ID를 알고 있고 메시지가 revocable 확인 되 면 OMEMessageRevocation cmdlet을 사용 하 여 전자 메일을 해지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="7578c-147">[Exchange Online PowerShell에 연결합니다](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="7578c-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="7578c-148">다음과 같이 OMEMessageRevocation cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="7578c-149">전자 메일이 해지 되었는지 확인 하려면 다음과 같이 OMEMessageStatus cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="7578c-150">해지가 성공한 경우 cmdlet은 다음 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7578c-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
