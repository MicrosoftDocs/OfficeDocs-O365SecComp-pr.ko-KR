---
title: Office 365 메시지 암호화로 암호화된 전자 메일 취소
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Office 365 관리자 권한으로 Office 365 메시지 암호화를 사용 하 여 암호화 된 특정 전자 메일을 취소할 수 있습니다.
ms.openlocfilehash: 018f12105e19382372a8a4b3a91248bb60b228be
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696242"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="1ab7d-103">Office 365 메시지 암호화 전자 메일 해지</span><span class="sxs-lookup"><span data-stu-id="1ab7d-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="1ab7d-p101">이 문서는 [Office 365 메시지 암호화](ome.md)에 대 한 문서를 더 큰 시리즈의 일부입니다. 이제 오른쪽, 암호화 된 전자 메일 해지 미리 보기입니다. 예상 되는 업데이트 및 변경 된 기능 및 콘텐츠를 사용해 제공을 개선 하기 위해 계속 되는 대로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="1ab7d-p102">이미 보낸 전자 메일을 해지 하려면 하는 것이 더 필요할 수 있습니다. 전자 메일 Office 365 메시지 암호화를 사용 하 여 암호화 된 경우 Office 365 관리자는 특정 조건에서 전자 메일에 대 한이 수행할 수 있습니다. 이 문서에서 어떤 경우에이 작업이 가능 하 고 작업을 수행 하는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="1ab7d-110">해지할 수 있는 암호화 된 전자 메일</span><span class="sxs-lookup"><span data-stu-id="1ab7d-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="1ab7d-p103">받는 사람이 받은 프로그램 링크 기반 암호화 된 전자 메일을 브랜드 하는 경우에 암호화 된 전자 메일을 해지할 수 있습니다. 받는 사람이 네이티브 인라인 환경이 지원 되는 Outlook 클라이언트에서을 받은 경우 해당 전자 메일이 해지 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="1ab7d-p104">있는지 여부를 받는 수신 링크 기반 환경 또는 인라인 경험 받는 사람 id 형식에 따라 달라 집니다: Office 365와 Microsoft 계정 받는 사람 (예: outlook.com 사용자) 지원 되는 Outlook 클라이언트를 인라인 환경에서 확인할 수 있습니다. 모든 받는 사람 같은 다른 유형을 Gmail 받는 사람에 게 링크 기반 경험을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="1ab7d-p105">출시 예정 조직이 id가 받는 사람에 관계 없이 링크 기반 환경을 강제 실행 하는 기능입니다. 이와 같은 방식이으로 모든 받는 사람에 게 자신이 됩니다 수 있는 읽기 및 암호화 된 전자 메일에 회신 하는 Office 365 메시지 암호화 포털에 대 한 링크와 브랜드 전자 메일을 받습니다. 이러한 암호화 된 전자 메일 재생산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="1ab7d-118">해지 된 암호화 된 전자 메일 받는 사람 환경</span><span class="sxs-lookup"><span data-stu-id="1ab7d-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="1ab7d-119">전자 메일을 해지 되 면 받는 됩니다 오류가 발생 하는 Office 365 메시지 암호화 포털을 통해 암호화 된 전자 메일에 액세스 하려고 할 때: "메시지 해지 된 보낸 사람이" 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![해지 된 암호화 된 전자 메일을 보여주는 스크린샷](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="1ab7d-121">암호화 된 전자 메일을 해지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1ab7d-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="1ab7d-p106">1 단계입니다. 전자 메일의 메시지 ID를 가져오려면</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="1ab7d-p107">암호화 된 메일을 해지할 수 있습니다 전에 메일의 메시지 ID를 수집 하는 것이 해야 합니다. MessageId은 일반적으로 다음과 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="1ab7d-p108">여러 방법으로 해지 하려고 하는 전자 메일의 메시지 ID를 찾을 수 있습니다. 이 섹션에서는 메시지를 몇 옵션을 설명 하지만 ID를 제공 하는 모든 메서드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="1ab7d-128">보안에서 메시지 추적을 사용 하 여 해지 하려면 전자 메일의 메시지 ID를 확인 하려면 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="1ab7d-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="1ab7d-129">보낸 사람이 나 받는 사람이 [Office 365 보안 & 준수 센터에서에서 새 메시지 추적](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)을 사용 하 여 전자 메일을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="1ab7d-p109">찾았으면는 전자 메일 **메시지 추적 세부 정보** 창에서 불러올 수 선택 합니다. 메시지 id. 찾으려고 **추가 정보** 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="1ab7d-132">보안에서 Office 메시지 암호화 보고서를 사용 하 여 해지 하려면 전자 메일의 메시지 ID를 확인 하려면 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="1ab7d-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="1ab7d-133">보안에서 &amp; 준수 센터 **메시지 암호화 보고서**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="1ab7d-134">**세부 정보 보기** 테이블을 선택 하 고 해지 하려는 메시지를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="1ab7d-135">메시지 id. 메시지를 포함 하는 세부 정보 보기를 두번클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="1ab7d-p110">2 단계입니다. 메일 재생산할 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p110">Step 2. Verify that the mail is revocable</span></span>

<span data-ttu-id="1ab7d-138">특정 전자 메일 메시지를 해지할 수 있는지 여부를 확인 하려면 다음이 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="1ab7d-p111">Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="1ab7d-141">다음과 같이 설정 OMEMessageStatus cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="1ab7d-p112">이 메시지 및 메시지 재생산할 인지의 주제를 반환 합니다. 예를 들어</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p112">This returns the subject of the message and whether the message is revocable. For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="1ab7d-p113">3 단계입니다. 메일을 해지</span><span class="sxs-lookup"><span data-stu-id="1ab7d-p113">Step 3. Revoke the mail</span></span>  

<span data-ttu-id="1ab7d-146">해지, 하려는 전자 메일의 메시지 ID를 알고 있는 한번 하 고 메시지는 재생산할, 집합 OMEMessageRevocation cmdlet을 사용 하 여 전자 메일을 해지할 수 있는지 확인 한 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="1ab7d-147">[Exchange Online PowerShell에 연결합니다](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="1ab7d-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="1ab7d-148">다음과 같이 설정 OMEMessageRevocation cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="1ab7d-149">전자 메일이 해지 되었습니다 있는지 여부를 확인 하려면 다음과 같이 입력 하는 Get OMEMessageStatus cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="1ab7d-150">해지에 성공 하면 cmdlet은 다음과 같은 결과 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab7d-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
