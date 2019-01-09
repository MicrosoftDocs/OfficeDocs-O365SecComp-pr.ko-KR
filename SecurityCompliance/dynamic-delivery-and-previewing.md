---
title: 동적 배달 하 고 Office 365 ATP 안전한 첨부 파일 미리 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: ATP 안전한 첨부 파일 정책에 연결을 설정할 때 동적 배달 메시지 지연을 방지 하 고 사용자 검색 되는 첨부 파일 미리 보기를 사용 하도록 설정 하려면 선택 합니다.
ms.openlocfilehash: 95c270e871c3febb13eef8c4374d996fc763315b
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769832"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="40b40-103">동적 배달 하 고 Office 365 ATP 안전한 첨부 파일 미리 보기</span><span class="sxs-lookup"><span data-stu-id="40b40-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="40b40-p101">**요약**: 동적 배달 [ATP 안전한 첨부 파일](atp-safe-attachments.md)에 대해 선택할 수 있는 옵션입니다. 동적 배달 및 [Office 365의 ATP 안전한 첨부 파일](atp-safe-attachments.md)의 첨부 파일 미리 보기 기능에 대해 자세히 알아보려면이 문서를 읽어보십시오.</span><span class="sxs-lookup"><span data-stu-id="40b40-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="40b40-p102">때 [ATP 안전한 첨부 파일 정책을 설정](set-up-atp-safe-attachments-policies.md) 하면 조직에 대 한 가지는 전자 메일 첨부 파일을 처리 하는 방법에 대 한 여러 옵션이 있습니다. **블록**, **교체**, 및 **동적 배달**포함 됩니다. ATP 안전한 첨부 파일 정책 구성 되는 방법에 따라 해당 첨부 파일 검사 하는 동안 전자 메일 받는 사람에 게 전자 메일 배달에 약간 지연을 발생할 수 있습니다. 메시지 지연을 방지 하려면 **동적 배달**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="40b40-110">동적 배달의 작동 방식</span><span class="sxs-lookup"><span data-stu-id="40b40-110">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="40b40-p103">동적 배달 각 전자 메일 첨부 파일에 대 한 자리 표시자와 받는 사람에 게를 통해 전자 메일 메시지의 본문을 발송 하 여 전자 메일 지연을 제거 합니다. 개체 틀에는 첨부 파일의 복사본을를 검사 하 고 안전 하 게 하려면 [ATP 안전한 첨부 파일](atp-safe-attachments.md)에 따른 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="40b40-113">각 첨부 파일을 선택 취소 하면 것을 열거나 다운로드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-113">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="40b40-114">첨부 파일이 악성 코드가 포함 될를 확인 하는 경우 해당로 보내집니다 격리, [Office 365에서 격리 된 메시지를 관리할](manage-quarantined-messages-and-files.md)수 (예: Office 365 전역 관리자 또는 보안 관리자) 조직의 보안 팀에 다른 사용자.</span><span class="sxs-lookup"><span data-stu-id="40b40-114">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="40b40-p104">대부분의 Pdf 및 Office 진행 중인 ATP 검사 하는 동안 안전 모드에서 문서를 미리볼 수 있습니다. 첨부 파일이 동적 배달 미리 보기와 호환 되지 않아, ATP 안전한 첨부 파일 검사 완료 될 때까지 전자 메일 받는 사람에 게는 첨부 파일 개체 틀을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

<span data-ttu-id="40b40-117">동적 배달 된 사용자 읽고 해당 첨부 파일을 분석 하는 동안 바로 자신의 전자 메일 메시지에 응답할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-117">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="40b40-p105">ATP 안전한 첨부 파일 검사 가져오고 Office 365 데이터가 있는 동일한 영역에 배치 합니다. 데이터 센터 지역에 대 한 자세한 내용은 참조 [가 다음에 있는 데이터?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="40b40-p105">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="40b40-120">첨부 파일을 포함 하는 전자 메일 전달 누군가가 때 어떻게 됩니까?</span><span class="sxs-lookup"><span data-stu-id="40b40-120">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="40b40-p106">조직의 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md)에 대 한 동적 배달을 사용 하는 첨부 파일을 포함 하는 전자 메일 받는 사람이 가정해 보겠습니다. 이제 다른 사람에 게 전자 메일 메시지를 전달 하는 그 사람 경우를 가정해 보겠습니다. 어떻게 해야 할까요? 받는 사람을 추가로 ATP 안전한 첨부 파일 정책에 포함 되는지 여부에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-p106">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person forwards the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="40b40-125">동적 배달 옵션을 사용 하는 ATP 안전한 첨부 파일 정책에 포함 되는 받는 사람을 받는 호환 파일을 미리 보고 하는 기능 개체 틀을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-125">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="40b40-126">받는 사람 ATP 안전한 첨부 파일 정책에 의해 다루지 않습니다, 하는 경우 다음 전자 메일 및 첨부 파일 들어갈 수를 통해 검색 ATP 안전한 첨부 파일 또는 첨부 파일 개체 틀 하지 않고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-126">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="40b40-127">동적 배달 작동 하기 위해 필요한 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="40b40-127">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="40b40-128">조직에는 [Office 365 고급 위협 보호](office-365-atp.md) 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-128">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="40b40-129">동적 배달 옵션 (참조 [Office 365의 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md))를 사용 하 여 ATP 안전한 첨부 파일에 대 한 정책 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-129">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="40b40-130">조직의 전자 메일을 Office 365에서 호스팅되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-130">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="40b40-131">시나리오를 동적 배달이 사용할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="40b40-131">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="40b40-p107">특정 시나리오가 동적 배달 지원 되지 않습니다. 이러한 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="40b40-p107">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="40b40-134">공용 폴더에 있는 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="40b40-134">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="40b40-135">전자 메일 메시지의 아웃 라우팅되는 한 후 사용자 지정 규칙을 사용 하 여 사용자의 사서함에 다시</span><span class="sxs-lookup"><span data-stu-id="40b40-135">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="40b40-136">이동 (자동 또는 수동) 호스팅된 사서함 로그 아웃 하 고 보관 폴더를 포함 하 여 다른 위치에 있는 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="40b40-136">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="40b40-137">삭제 된 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="40b40-137">Email messages that are deleted</span></span>
    
- <span data-ttu-id="40b40-138">오류 상태에 있는 사용자의 사서함 검색 폴더</span><span class="sxs-lookup"><span data-stu-id="40b40-138">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="40b40-p108">Exchange Online 관리자가 Exclaimer를 활성화 하는 환경입니다. 이 해결 하려면 참조 [ATP 동적 배달 및 Exclaimer 사용 되는 경우 첨부 파일이 있는 메시지 배달 되지 않습니다](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span><span class="sxs-lookup"><span data-stu-id="40b40-p108">Environments in which an Exchange Online admin has enabled Exclaimer. To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="40b40-141">메시지 [(S/MIME) 기업이 Internet Mail Extensions](s-mime-for-message-signing-and-encryption.md)를 사용 하 여 암호화)</span><span class="sxs-lookup"><span data-stu-id="40b40-141">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>
    
