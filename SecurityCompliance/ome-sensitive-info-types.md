---
title: 중요 한 정보에 대 한 새 Office 365 메시지 암호화 정책
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/16/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 요약:는 자동으로 모든 테 넌 트에 제공 하는 중요 한 정보 형식에 대 한 Office 365 메시지 암호화 정책을 적용 합니다.
ms.openlocfilehash: f83bf0fe572586b3becf2dd53395e611bdaaea24
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614382"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="fd5f7-103">중요 한 정보에 대 한 office 365 메시지 암호화 정책</span><span class="sxs-lookup"><span data-stu-id="fd5f7-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="fd5f7-p101">선택 그룹은 조직의 크기와 메일 흐름의 복잡성에 따라 테 넌 트에 대해 특정 유형의 자체는 포함 된 전자 메일을 Office 365 메시지 암호화 적용 되는 Office 365 테 넌 트의 새로운 자동 정책의 느린 roll 아웃 수행 하는 정보입니다. 이 테 넌 트의 작은 그룹과 테스트 하는 합니다. 이 정책은 하지 롤아웃 될 모든 조직 및 조직 크기와 같은 고려 사항 및 메일 흐름의 복잡도 사용 하 여이 롤아웃을 대 한 자격을 결정 하는 합니다. 이 롤아웃을 대 한 조직 선택 알림을 기반이이 자동 정책이 만들어질 및 최소한 30 일 공지와 옵트아웃 옵션이 제공 됩니다 날짜를 알리는 Office 365 메시지 센터에서 받습니다. 이 정책을 만들려면 Microsoft 때까지 기다리는 하지 않으려고 그렇게 하려고 하는 경우 Exchange 메일 흐름 규칙을 사용 하 여이 자동 정책을 만들 수 자기 자신을 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5f7-p101">For a select group of tenants, based on their organization size and complexity of mail flow, we are doing a slow roll-out of a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to emails that contain certain types of sensitive information. We are testing this with a small group of tenants. This policy will not be rolled out to all organizations and considerations such as organization size and complexity of mail flow will be used to determine the eligibility for this roll-out. If your organization is selected for this roll-out, you will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created and you will be given at least a 30-day notice and the option to opt-out. If you don't want to wait for Microsoft to create this policy and would like to do so yourselves, you can create this automatic policy using Exchange Mail Flow rules.</span></span>

## <a name="when-to-expect-the-update-for-your-tenant"></a><span data-ttu-id="fd5f7-107">테 넌 트에 대 한 업데이트를 것으로 예상 되는 경우</span><span class="sxs-lookup"><span data-stu-id="fd5f7-107">When to expect the update for your tenant</span></span>

<span data-ttu-id="fd5f7-p102">조직에는 자동이 정책을 테 넌 트에 작성 되는 날짜를 알리는 Office 365 메시지 센터에는 알림을 받게 됩니다. 30 일 알림의 부여 하 고 옵션 옵트아웃을 갖습니다. 잠재적으로 옵트아웃할 하려면 하는 시나리오를 위한 타사 데이터 손실 방지 솔루션 이미 중요 한 형식에 대 한 검색을 하는 경우 것입니다. 옵트아웃 하는 방법에 대 한 자세한 내용은이 문서의 뒷부분에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd5f7-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types. More details on how to opt-out are available later in this article.</span></span>

## <a name="sensitive-information-type-policy-details"></a><span data-ttu-id="fd5f7-111">중요 한 정보 유형 정책 세부 정보</span><span class="sxs-lookup"><span data-stu-id="fd5f7-111">Sensitive information type policy details</span></span>

<span data-ttu-id="fd5f7-112">조직에서 사용 하 여 조직의 외부로 나가는 전자 메일을 자동으로 암호화 하는 Exchange 메일 흐름 규칙을 만들는 *암호화 전용* 정책 전자 메일 또는 해당 첨부 파일에 다음과 같은 중요 한 정보 유형 포함 되는 경우:</span><span class="sxs-lookup"><span data-stu-id="fd5f7-112">An Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="fd5f7-113">ABA 라우팅 번호</span><span class="sxs-lookup"><span data-stu-id="fd5f7-113">ABA routing number</span></span>
- <span data-ttu-id="fd5f7-114">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="fd5f7-114">Credit card Number</span></span>
- <span data-ttu-id="fd5f7-115">약물 적용 기관 (DEA) 번호</span><span class="sxs-lookup"><span data-stu-id="fd5f7-115">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="fd5f7-p103">미국 / 영국 여권 번호</span><span class="sxs-lookup"><span data-stu-id="fd5f7-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="fd5f7-118">미국 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="fd5f7-118">U.S. bank account number</span></span>
- <span data-ttu-id="fd5f7-119">미국 ITIN(개인 납세자 번호)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-119">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="fd5f7-120">미국 SSN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-120">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="fd5f7-121">정확 하 게 중요 한 형식 조직의 로캘에 의해 다를 수 있습니다 및 메시지 센터 알림 영역에서 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd5f7-121">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="fd5f7-122">준비 하기 위해이 변경을 수행 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="fd5f7-122">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="fd5f7-p104">업데이트 하거나이 새로운 변경 하기 전에 모든 기존 Office 365 구성 설정을 수정할 필요가 없습니다. 그러나 다음 모든 해당 최종 사용자 설명서 및 교육 자료 (영문)이이 변경에 대 한 조직의 사용자에 게 준비를 업데이트 하는 것이 좋습니다. 필요에 따라 사용자와 이러한 Office 365 메시지 암호화 리소스를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5f7-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="fd5f7-126">전송 하 고, 보고, PC에 대 한 Outlook에서 암호화 된 메시지에 회신</span><span class="sxs-lookup"><span data-stu-id="fd5f7-126">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="fd5f7-127">Office 365 Essentials 비디오: Office 메시지 암호화</span><span class="sxs-lookup"><span data-stu-id="fd5f7-127">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="fd5f7-128">이 변경 내용을 표시 되는 방법을 감사 로그에 있습니까?</span><span class="sxs-lookup"><span data-stu-id="fd5f7-128">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="fd5f7-p105">이 작업은 감사 및 고객에 게 표시 됩니다.  이 작업은 ' New-transportrule ' 이며 보안 & 준수 센터의에서 감사 로그 검색에서 예제 감사 항목의 코드 조각을 아래:</span><span class="sxs-lookup"><span data-stu-id="fd5f7-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="fd5f7-131">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 월 1 일, "ResultStatus": "True", "UserKey": "Microsoft 연산자"," UserType": 3,"버전": 월 1 일,"작업":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":""," UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX ( 15.20.1382.008)","Parameters": {"Name":"조직","값":" 123456 221 d-12346"{"Name":"ApplyRightsProtectionTemplate","값":"암호화"}, {"Name":"이름","값":"(로그 아웃 상자 규칙) 중요 한 아웃 바운드 전자 메일이 암호화"}, {"Name":" MessageContainsDataClassifications"등입니다.*</span><span class="sxs-lookup"><span data-stu-id="fd5f7-131">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="fd5f7-132">어떻게 수행 합니까 옵트아웃?</span><span class="sxs-lookup"><span data-stu-id="fd5f7-132">How do I opt-out?</span></span>

<span data-ttu-id="fd5f7-133">옵트아웃이 변경 하려는 경우에 다음이 단계를 수행 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd5f7-133">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="fd5f7-p106">Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd5f7-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>
2. <span data-ttu-id="fd5f7-136">다음과 같이 Set-irmconfiguration cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5f7-136">Run the Set-IRMConfiguration cmdlet as follows:</span></span>

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-or-customize-the-automatic-policy"></a><span data-ttu-id="fd5f7-137">사용 하지 않도록 설정 하거나 자동 정책을 사용자 지정 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="fd5f7-137">How do I disable or customize the automatic policy?</span></span>

<span data-ttu-id="fd5f7-138">[사용 하지 않거나 규칙을 편집](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) **메일 흐름**으로 이동 하 여 수 하면 하지 않았으므로 옵트아웃이 변경 하 고 Exchange 메일 흐름 규칙을 이미 만든 경우 > **규칙** 에서 Exchange 관리 센터 (EAC) 및 "*암호화 규칙을 사용 하지 않도록 설정 (로그 아웃 상자 규칙) 중요 한 아웃 바운드 전자 메일이*"입니다.</span><span class="sxs-lookup"><span data-stu-id="fd5f7-138">If you didn’t opt-out of this change and the Exchange mail flow rule has already been created, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
