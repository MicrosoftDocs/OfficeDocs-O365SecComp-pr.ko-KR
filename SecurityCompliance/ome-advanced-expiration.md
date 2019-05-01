---
title: Office 365 고급 메시지 암호화로 암호화 된 전자 메일에 대 한 만료 날짜 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: office 365 메시지 암호화 (OME)의 맨 위에 office 365 고급 메시지 암호화 기능을 사용 하 여 사용자 지정 브랜드 서식 파일을 통해 전자 메일에 만료 날짜를 설정 하 여 이메일 보안을 확장할 수 있습니다.
ms.openlocfilehash: c1fb876724bed970095e950906500ff551d93cee
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506730"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="6f9f1-103">Office 365 고급 메시지 암호화로 암호화 된 전자 메일에 대 한 만료 날짜 설정</span><span class="sxs-lookup"><span data-stu-id="6f9f1-103">Set an expiration date for email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="6f9f1-104">office 365에서는 특정 구독의 office 365 메시지 암호화 중 위에서 고급 메시지 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-104">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="6f9f1-105">고급 메시지 암호화는 [Microsoft 365 enterprise e5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise e5 및 Office 365 교육 A5에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-105">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="6f9f1-106">조직에 office 365 고급 메시지 암호화를 포함 하지 않는 office 365 구독이 있는 경우 고급 메시지 암호화는 advanced 준수 SKU의 E5 규격을 사용 하 여 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-106">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="6f9f1-107">사용자가 OME 포털을 사용 하 여 암호화 된 전자 메일에 액세스 하는 외부의 받는 사람에 게 보내는 전자 메일에 메시지 만료를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-107">You can use message expiration on emails that your users send to external recipients who use the OME Portal to access encrypted emails.</span></span> <span data-ttu-id="6f9f1-108">Windows Powershell에서 만료 날짜를 지정 하는 사용자 지정 브랜드 서식 파일을 사용 하 여 조직에서 보낸 암호화 된 전자 메일을 보고 회신할 때 받는 사람이 OME 포털을 사용 하도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-108">You force recipients to use the OME portal to view and reply to encrypted emails sent by your organization by using a custom branded template that specifies an expiration date in Windows Powershell.</span></span>

<span data-ttu-id="6f9f1-109">O365 전역 관리자 인 경우 회사 브랜딩을 적용 하 여 Office 365 조직의 전자 메일 메시지의 모양을 사용자 지정 하는 경우 이러한 전자 메일 메시지에 대 한 만료를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-109">As an O365 global administrator, when you apply your company branding to customize the look of your Office 365 organization's email messages, you can also specify an expiration for these email messages.</span></span> <span data-ttu-id="6f9f1-110">Office 365 고급 메시지 암호화를 사용 하면 조직에서 보내는 암호화 된 전자 메일용으로 여러 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-110">With Office 365 Advanced Message Encryption, you can create multiple templates for encrypted emails originating from your organization.</span></span> <span data-ttu-id="6f9f1-111">서식 파일을 사용 하면 받는 사람에 게 사용자가 보낸 메일에 대 한 액세스 권한이 있는 기간을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-111">Using a template, you can control how long recipients have access to mail sent by your users.</span></span>

<span data-ttu-id="6f9f1-112">최종 사용자가 만료 날짜가 설정 된 메일을 받는 경우 사용자는 래퍼 전자 메일에서 만료 날짜를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-112">When an end user receives mail that has an expiration date set, the user sees the expiration date in the wrapper email.</span></span> <span data-ttu-id="6f9f1-113">사용자가 만료 된 메일을 열려고 하면 OME 포털에 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-113">If a user tries to open an expired mail, an error appears in the OME portal.</span></span>

<span data-ttu-id="6f9f1-114">외부의 받는 사람에 대 한 전자 메일만 expirable 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-114">Only emails to external recipients are expirable.</span></span>

<span data-ttu-id="6f9f1-115">office 365 고급 메시지 암호화를 사용 하면 사용자 지정 브랜딩을 적용할 때마다 office 365에서 해당 래퍼를 서식 파일을 적용 하는 메일 흐름 규칙에 맞는 전자 메일에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-115">With Office 365 Advanced Message Encryption, any time you apply custom branding, the Office 365 applies the wrapper to email that fits the mail flow rule to which you apply the template.</span></span> <span data-ttu-id="6f9f1-116">또한 사용자 지정 브랜딩을 사용 하는 경우에만 만료를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-116">In addition, expiration can only be used if custom branding is used.</span></span>

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a><span data-ttu-id="6f9f1-117">PowerShell을 사용 하 여 메일 만료를 적용 하는 사용자 지정 브랜딩 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="6f9f1-117">Create a custom branding template to force mail expiration by using PowerShell</span></span>

1. <span data-ttu-id="6f9f1-118">Office 365 테 넌 트에서 전역 관리자 권한이 있는 계정을 사용 하 여 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-118">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="6f9f1-119">set-omeconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-119">Run the New-OMEConfiguration cmdlet.</span></span>

     ```powershell
     New-OMEConfiguration -Identity "Expire in 7 days" ExternalMailExpiryInDays 7
     ```

<span data-ttu-id="6f9f1-120">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-120">Where:</span></span>

- <span data-ttu-id="6f9f1-121">Identity는 사용자 지정 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-121">Identity is the name of the custom template.</span></span>

- <span data-ttu-id="6f9f1-122">ExternalMailExpiryInDays는 받는 사람이 만료 되기 전에 메일을 보존할 일 수를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-122">ExternalMailExpiryInDays identifies the number of days you want recipients to be able to keep mail before it expires.</span></span> <span data-ttu-id="6f9f1-123">1 ~ 730 일 사이의 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f1-123">You can use any value between 1 to 730 days.</span></span>

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="6f9f1-124">Office 365 고급 메시지 암호화에 대 한 추가 정보</span><span class="sxs-lookup"><span data-stu-id="6f9f1-124">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="6f9f1-125">Office 365 고급 메시지 암호화</span><span class="sxs-lookup"><span data-stu-id="6f9f1-125">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="6f9f1-126">Office 365 고급 메시지 암호화로 암호화 된 전자 메일 해지</span><span class="sxs-lookup"><span data-stu-id="6f9f1-126">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>](revoke-ome-encrypted-mail.md)

- [<span data-ttu-id="6f9f1-127">메시지 정책 및 규정 준수 서비스 설명</span><span class="sxs-lookup"><span data-stu-id="6f9f1-127">Message policy and compliance service description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)