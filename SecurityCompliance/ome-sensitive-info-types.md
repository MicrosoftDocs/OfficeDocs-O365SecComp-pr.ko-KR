---
title: 중요 한 정보에 대 한 Office 365 메시지 암호화 정책
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: 중요 한 정보 유형에 대 한 Office 365 메시지 암호화 정책을 지금 사용할 수 있습니다.'
ms.openlocfilehash: 99cb7a9f94c9cf4036c11b74a5208ddf0e819ceb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261266"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="2bb75-103">중요 한 정보에 대 한 Office 365 메시지 암호화 정책</span><span class="sxs-lookup"><span data-stu-id="2bb75-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="2bb75-104">업데이트 (1/30/19): 10 월 2018에서는 특정 중요 한 정보 유형을 기반으로 중요 한 전자 메일을 자동으로 암호화 하 여 보호를 단순화할 수 있는지를 이해 하기 위한 소수의 고객 예제로 노력 했습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-104">Update (1/30/19): In October 2018, we worked with a small sample of customers to understand if we can simplify protection by automatically encrypting sensitive emails based on certain sensitive information types.</span></span> <span data-ttu-id="2bb75-105">이 샘플의 긍정적인 피드백을 기반으로 하 여 12 월 2018에 보다 다양 한 테 넌 트 프로필을 확장 하기로 결정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-105">Based on positive feedback from this sample, we decided to expand to a more diverse profile of tenants in December 2018.</span></span> <span data-ttu-id="2bb75-106">다음 롤오버를 통신 하 여 테 넌 트를 선택 하면 사용자 의견을 수렴 하 고 복잡 한 환경이 있는 고객이 규칙을 보다 주의 깊게 구현 하기를 원했습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-106">After communicating the next roll-out to select tenants, we listened to your feedback and determined that customers with more complex environments wanted to implement the rules more cautiously, and we are therefore adjusting our plans.</span></span>

<span data-ttu-id="2bb75-107">조직이 롤업을 사용 하도록 선택한 경우 2019 년 1 월 15 일부터 시작 하는 경우 자동 정책이 배포 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-107">If your organization was selected for the roll-out starting January 15, 2019, we will not roll out the automatic policy.</span></span> <span data-ttu-id="2bb75-108">대신이 문서에서 롤아웃 yourselves을 완료 하는 방법에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-108">Instead, we are providing instructions in this article on how you can complete the roll-out yourselves.</span></span> <span data-ttu-id="2bb75-109">정보를 계속 확인 하 여 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-109">Keep reading to find out how.</span></span>

||
|:-----|
|<span data-ttu-id="2bb75-110">이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-110">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="2bb75-111">이 문서는 관리자와 itpros 전문가를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-111">This article is intended for administrators and ITPros.</span></span> <span data-ttu-id="2bb75-112">암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요.</span><span class="sxs-lookup"><span data-stu-id="2bb75-112">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a><span data-ttu-id="2bb75-113">테 넌 트에 대 한 중요 한 정보 유형 정책을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="2bb75-113">How to create the sensitive information type policy for your tenant</span></span>

<span data-ttu-id="2bb75-114">Exchange 메일 흐름 규칙 또는 Office 365 DLP (데이터 손실 방지)를 사용 하 여 중요 한 정보 유형 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-114">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create the sensitive information type policy.</span></span> <span data-ttu-id="2bb75-115">exchange 메일 흐름 규칙을 만들려면 EAC (exchange 관리 센터) 또는 PowerShell을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-115">To create an Exchange mail flow rule you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="2bb75-116">EAC에서 메일 흐름 규칙을 사용 하 여 정책을 만들려면</span><span class="sxs-lookup"><span data-stu-id="2bb75-116">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="2bb75-117">EAC (Exchange 관리 센터)에 로그인 하 고 **메일 흐름** > **규칙**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-117">Sign-in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**.</span></span> <span data-ttu-id="2bb75-118">여기에는 메시지 또는 첨부 파일에 특정 키워드나 중요 한 정보 유형이 존재 하는 등의 조건에 따라 Office 365 메시지 암호화를 적용 하는 규칙이 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-118">There, create a rule that applies Office 365 Message Encryption based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="2bb75-119">PowerShell에서 메일 흐름 규칙을 사용 하 여 정책을 만들려면</span><span class="sxs-lookup"><span data-stu-id="2bb75-119">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="2bb75-120">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-120">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="2bb75-121">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2bb75-121">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span> <span data-ttu-id="2bb75-122">TransporRule cmdlet을 사용 하 여 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-122">Use the Set-IRMConfiguration and New-TransporRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="2bb75-123">PowerShell로 만든 메일 흐름 규칙 예제</span><span class="sxs-lookup"><span data-stu-id="2bb75-123">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="2bb75-124">PowerShell에서 다음 명령을 실행 하 여 전자 메일 또는 첨부 파일에 다음과 같은 중요 한 정보가 포함 되어 있는 경우 *암호화 전용* 정책을 사용 하 여 조직 외부의 전자 메일을 자동으로 암호화 하는 Exchange 메일 흐름 규칙 만들기 정보 유형:</span><span class="sxs-lookup"><span data-stu-id="2bb75-124">Running the following commands in PowerShell create an Exchange mail flow rule that automatically encrypts emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="2bb75-125">ABA 라우팅 번호</span><span class="sxs-lookup"><span data-stu-id="2bb75-125">ABA routing number</span></span>
- <span data-ttu-id="2bb75-126">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="2bb75-126">Credit card Number</span></span>
- <span data-ttu-id="2bb75-127">DEA (약품 집행 기관) 번호</span><span class="sxs-lookup"><span data-stu-id="2bb75-127">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="2bb75-128">미국/영국</span><span class="sxs-lookup"><span data-stu-id="2bb75-128">U.S. / U.K.</span></span> <span data-ttu-id="2bb75-129">passport number</span><span class="sxs-lookup"><span data-stu-id="2bb75-129">passport number</span></span>
- <span data-ttu-id="2bb75-130">미국 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="2bb75-130">U.S. bank account number</span></span>
- <span data-ttu-id="2bb75-131">미국 ITIN(개인 납세자 번호)</span><span class="sxs-lookup"><span data-stu-id="2bb75-131">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="2bb75-132">미국 SSN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="2bb75-132">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="2bb75-133">받는 사람이 첨부 파일에 액세스 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2bb75-133">How recipients access attachments</span></span>

<span data-ttu-id="2bb75-134">메시지가 암호화 되 면 받는 사람은 액세스 하 여 암호화 된 전자 메일을 여는 경우 첨부 파일에 무제한으로 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-134">Once a message is encrypted, recipients will have unrestricted access to attachments once they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="2bb75-135">이 변경 내용을 준비 하려면</span><span class="sxs-lookup"><span data-stu-id="2bb75-135">To prepare for this change</span></span>

<span data-ttu-id="2bb75-136">해당 하는 최종 사용자 설명서 및 교육 자료를 업데이트 하 여 조직의 사용자가이 변경 내용을 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-136">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span> <span data-ttu-id="2bb75-137">다음 Office 365 메시지 암호화 리소스를 사용자와 적절 하 게 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-137">Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="2bb75-138">PC 용 Outlook에서 암호화 된 메시지 보내기, 확인 및 회신</span><span class="sxs-lookup"><span data-stu-id="2bb75-138">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="2bb75-139">office 365 Essentials 동영상: office 메시지 암호화</span><span class="sxs-lookup"><span data-stu-id="2bb75-139">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="2bb75-140">감사 로그에서 이러한 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-140">View these changes in the Audit log</span></span>

<span data-ttu-id="2bb75-141">이 활동은 감사 되며 Office 365 관리자가 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-141">This activity is audited and is available to Office 365 administrators.</span></span> <span data-ttu-id="2bb75-142">이 작업은 ' New-new-transportrule ' 이며, 보안 & 준수 센터의 감사 로그 검색의 예제 감사 항목의 코드 조각이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bb75-142">The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="2bb75-143">*{"CreationTime": "2018-11-28t23:35:01", "Id": "a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c", "Operation": "New-new-transportrule", "조직 id": "123456-221d-12345", "RecordType": 1, "resultstatus": "True", "userkey": "Microsoft Operator", " UserType ": 3," Version ": 1," 작업 부하 ":" Exchange "," ClientIP ":" 123.456.147.68:17584 "," ObjectId ":" "," UserId ":" Microsoft Operator","OrganizationName":"contoso ":" OriginatingServer ( 15.20.1382.008) "," 매개 변수 ": {" Name ":" 조직 "," 값 ":" 123456-221d-"ApplyRightsProtectionTemplate", "value", "12346": "", "" name "," value ":" 아웃 바운드 중요 한 전자 메일을 암호화 합니다 (box 규칙을 벗어났습니다. "}, {" Name ":" MessageContainsDataClassifications "... 기타.*</span><span class="sxs-lookup"><span data-stu-id="2bb75-143">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span> |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="2bb75-144">중요 한 정보 유형 정책을 사용 하지 않도록 설정 하거나 사용자 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="2bb75-144">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="2bb75-145">exchange 메일 흐름 규칙을 만든 후에는 EAC (exchange 관리 센터)의 **메일 흐름** > **규칙** 으로 이동 하 여 [규칙을 사용 하지 않도록 설정 하거나 편집할](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) 수 있으며 "*아웃 바운드 중요 한 전자 메일 암호화 (box 규칙을 초과* 함" 규칙을 사용 하지 않도록 설정 합니다. ".</span><span class="sxs-lookup"><span data-stu-id="2bb75-145">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
