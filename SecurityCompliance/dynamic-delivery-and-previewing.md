---
title: 동적 배달 및 Office 365 ATP 안전한 첨부 파일로 미리 보기
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 04/19/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
ms.collection:
- M365-security-compliance
description: ATP 안전한 첨부 파일 정책을 설정할 때 메시지 지연을 방지 하 고 사용자가 검색 중인 첨부 파일을 미리 볼 수 있도록 동적 전달을 선택 합니다.
ms.openlocfilehash: 2f965c119e9c4fca15e43d281dfc2d00d2c79c23
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599904"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="1da54-103">동적 배달 및 Office 365 ATP 안전한 첨부 파일로 미리 보기</span><span class="sxs-lookup"><span data-stu-id="1da54-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

## <a name="overview"></a><span data-ttu-id="1da54-104">개요</span><span class="sxs-lookup"><span data-stu-id="1da54-104">Overview</span></span>

<span data-ttu-id="1da54-105">동적 배달은 [ATP 안전한 첨부 파일](atp-safe-attachments.md)에 대해 선택할 수 있는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-105">Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="1da54-106">이 문서를 읽으면 [Office 365에서 ATP 안전한 첨부 파일](atp-safe-attachments.md)의 동적 배달 및 첨부 파일 미리 보기 기능에 대해 자세히 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-106">Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="1da54-107">[ATP 안전한 첨부 파일 정책이](set-up-atp-safe-attachments-policies.md) 조직에 대해 설정 된 경우 전자 메일 첨부 파일을 처리 하는 방법에 대 한 몇 가지 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-107">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled.</span></span> <span data-ttu-id="1da54-108">여기에는 **Block**, **Replace**및 **Dynamic Delivery**가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-108">These include **Block**, **Replace**, and **Dynamic Delivery**.</span></span> <span data-ttu-id="1da54-109">ATP Safe 첨부 파일 정책이 구성 되는 방식에 따라 전자 메일 받는 사람이 첨부 파일을 검색 하는 동안 전자 메일을 배달 하는 동안 약간의 지연이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-109">Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned.</span></span> <span data-ttu-id="1da54-110">메시지 지연을 방지 하려면 **동적 배달을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-110">To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="1da54-111">동적 배달이 작동 하는 방식</span><span class="sxs-lookup"><span data-stu-id="1da54-111">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="1da54-112">동적 배달은 각 전자 메일 첨부 파일에 대 한 자리 표시자를 사용 하 여 전자 메일 메시지의 본문을 받는 사람에 게 보내 전자 메일 지연을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-112">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment.</span></span> <span data-ttu-id="1da54-113">자리 표시자는 [ATP 안전한 첨부 파일](atp-safe-attachments.md)에서 첨부 파일의 복사본을 검색 하 고 안전한 것으로 확인 될 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-113">The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="1da54-114">각 첨부 파일을 지우면 파일이 열리거나 다운로드 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-114">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="1da54-115">첨부 파일이 악성으로 확인 되 면 조직의 보안 팀 (예: Office 365 전역 관리자 또는 보안 관리자)에 있는 사용자가 [office 365에서 격리 된 메시지를 관리할](manage-quarantined-messages-and-files.md)수 있는 격리로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-115">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="1da54-116">ATP 검색이 진행 되는 동안 대부분의 Pdf 및 Office 문서를 안전 모드에서 미리 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-116">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway.</span></span> <span data-ttu-id="1da54-117">첨부 파일이 동적 배달 미리 보기와 호환 되지 않는 경우 ATP 안전한 첨부 파일 검색이 완료 될 때까지 전자 메일 받는 사람은 첨부 파일 자리 표시자를 보게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-117">If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

> [!TIP]
> <span data-ttu-id="1da54-118">모바일 장치를 사용 하 고 있고 Pdf가 동적 배달 미리 보기에서 처음에 렌더링 되지 않는 경우에는 모바일 브라우저를 사용 하 여 Office 365에 로그인 해 보세요.</span><span class="sxs-lookup"><span data-stu-id="1da54-118">If you're using a mobile device, and PDFs are not rendering in Dynamic Delivery previewer at first, try signing into Office 365 using your mobile browser.</span></span>

<span data-ttu-id="1da54-119">동적 배달의 경우 사용자는 첨부 파일을 분석 하는 동안 즉시 전자 메일 메시지를 읽고 응답할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-119">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="1da54-120">ATP 안전한 첨부 파일 검사는 Office 365 데이터가 있는 동일한 지역에서 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-120">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides.</span></span> <span data-ttu-id="1da54-121">데이터 센터 지역에 대 한 자세한 내용은 [어디에 있습니까?](https://products.office.com/where-is-your-data-located?geo=All) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1da54-121">For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="1da54-122">첨부 파일이 포함 된 전자 메일을 다른 사용자가 전달 하면 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="1da54-122">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="1da54-123">조직에서 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md)에 대 한 동적 전달을 사용 하 고 있고 첨부 파일이 포함 된 전자 메일을 받는 사람도 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-123">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment.</span></span> <span data-ttu-id="1da54-124">이제 해당 사용자가 다른 사람에 게 전자 메일 메시지를 전달 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-124">Now suppose that person forwards the email message to someone else.</span></span> <span data-ttu-id="1da54-125">어떤 일이 발생 하나요?</span><span class="sxs-lookup"><span data-stu-id="1da54-125">What happens?</span></span> <span data-ttu-id="1da54-126">이는 추가 받는 사람이 ATP 안전한 첨부 파일 정책에 포함 되어 있는지 여부에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-126">It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="1da54-127">받는 사람이 동적 배달 옵션을 사용 하 여 ATP 안전 첨부 파일 정책에 포함 되는 경우에는 받는 사람에 게 상호 자리 표시자를 보게 되며 호환 되는 파일을 미리 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-127">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="1da54-128">받는 사람이 ATP 안전한 첨부 파일 정책에 포함 되지 않는 경우 전자 메일 및 첨부 파일은 ATP가 안전한 첨부 파일 검색 또는 첨부 파일 자리 표시자 없이 진행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-128">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without any ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="1da54-129">동적 배달이 작동 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="1da54-129">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="1da54-130">조직에 [Office 365 Advanced Threat Protection](office-365-atp.md) 이 있어야 함</span><span class="sxs-lookup"><span data-stu-id="1da54-130">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="1da54-131">동적 배달 옵션을 사용 하 여 ATP 안전한 첨부 파일에 정책을 정의 해야 합니다 ( [Office 365에서 Atp 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)참조).</span><span class="sxs-lookup"><span data-stu-id="1da54-131">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="1da54-132">조직의 전자 메일이 Office 365에서 호스팅되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-132">Your organization's email must be hosted in Office 365.</span></span> <span data-ttu-id="1da54-133">[Office 365 Advanced Threat Protection은 모든 SMTP 메일 전송 에이전트](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#requirements-for-office-365-advanced-threat-protection-atp) (예: Exchange Server)와 함께 사용할 수 있지만, ATP Safe 첨부 파일에 대 한 동적 배달 옵션을 사용 하려면 조직의 전자 메일이 Office 365에 호스트 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-133">Although [Office 365 Advanced Threat Protection can be used with any SMTP mail transfer agent](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#requirements-for-office-365-advanced-threat-protection-atp) (such as Exchange Server), the Dynamic Delivery option for ATP Safe Attachments requires that your organization's email be hosted in Office 365.</span></span> <span data-ttu-id="1da54-134">전자 메일이 Office 365에서 호스트 되지 않는 경우 **Block**과 같은 다른 [ATP 안전 첨부 파일 정책 옵션](set-up-atp-safe-attachments-policies.md#step-3-learn-about-atp-safe-attachments-policy-options)을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-134">If your email is not hosted in Office 365, choose a different [ATP Safe Attachments policy option](set-up-atp-safe-attachments-policies.md#step-3-learn-about-atp-safe-attachments-policy-options), such as **Block**.</span></span>
    
## <a name="additional-considerations"></a><span data-ttu-id="1da54-135">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="1da54-135">Additional considerations</span></span>

<span data-ttu-id="1da54-136">동적 배달이 지원 되지 않는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-136">There are certain scenarios in which Dynamic Delivery is not supported.</span></span> <span data-ttu-id="1da54-137">이러한 경계 및 제한은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-137">These include the following:</span></span>
  
- <span data-ttu-id="1da54-138">공용 폴더에 있는 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="1da54-138">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="1da54-139">사용자 지정 규칙을 사용 하 여 외부에서 라우팅된 다음 사용자의 사서함으로 다시 전송 되는 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="1da54-139">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="1da54-140">호스팅된 사서함에서 또는 보관 폴더를 비롯 한 다른 위치로 자동 또는 수동으로 이동 되는 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="1da54-140">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="1da54-141">삭제 된 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="1da54-141">Email messages that are deleted</span></span>
    
- <span data-ttu-id="1da54-142">오류 상태의 사용자 사서함 검색 폴더</span><span class="sxs-lookup"><span data-stu-id="1da54-142">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="1da54-143">Exchange Online 관리자가 Exclaimer를 사용 하도록 설정한 환경</span><span class="sxs-lookup"><span data-stu-id="1da54-143">Environments in which an Exchange Online admin has enabled Exclaimer.</span></span> <span data-ttu-id="1da54-144">이 문제를 해결 하려면 [ATP 동적 배달 및 Exclaimer을 사용할 때 첨부 파일이 포함 된 메시지가 배달 되지 않음](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery) 을 참고 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1da54-144">To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="1da54-145">[Secure/다목적 인터넷 메일 확장명 (S/MIME)](s-mime-for-message-signing-and-encryption.md)을 사용 하 여 암호화 된 메시지</span><span class="sxs-lookup"><span data-stu-id="1da54-145">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>

- <span data-ttu-id="1da54-146">동적 배달이 지원 되지 않는 경우 ATP 안전한 첨부 파일은 전자 메일 메시지를 검사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-146">In cases where Dynamic Delivery is not supported, ATP Safe Attachments will not scan email messages.</span></span> <span data-ttu-id="1da54-147">그러나 [ATP 안전한 링크 정책이](set-up-atp-safe-links-policies.md) 구성 되는 방식에 따라 url이 포함 된 첨부 파일을 사용 하 여 전자 메일 메시지를 배달 하는 방법을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-147">However, delivering email messages with attachments that contain URLs will be checked, depending on how your [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured.</span></span> <span data-ttu-id="1da54-148">이러한 경우 전자 메일 메시지 및 Office 파일의 Url을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1da54-148">In these cases, URLs in email messages and Office files are checked.</span></span>
