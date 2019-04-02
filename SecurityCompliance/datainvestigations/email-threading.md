---
title: 전자 메일 스레드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: ca4823ecfc06ddc0ef6f6840ad55fec492ac472c
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030343"
---
# <a name="email-threading"></a><span data-ttu-id="b72ba-102">전자 메일 스레드</span><span class="sxs-lookup"><span data-stu-id="b72ba-102">Email threading</span></span>

<span data-ttu-id="b72ba-103">잠시 동안 진행 되 고 있는 전자 메일 대화를 생각해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-103">Consider an email conversation that has been going on for a while.</span></span> <span data-ttu-id="b72ba-104">대부분의 경우 스레드의 마지막 전자 메일에는 위의 모든 전자 메일의 내용이 포함 됩니다. 마지막 전자 메일을 검토 하면 해당 스레드에서 발생 한 대화의 전체 컨텍스트를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-104">In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread.</span></span> <span data-ttu-id="b72ba-105">전자 메일 스레딩에서는 검토자가 컨텍스트 손실 없이 수집 된 문서를 분수로 검토할 수 있도록 이러한 전자 메일이 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-105">Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="b72ba-106">전자 메일 스레딩의 기능</span><span class="sxs-lookup"><span data-stu-id="b72ba-106">What does email threading do?</span></span>

<span data-ttu-id="b72ba-107">전자 메일 스레딩은 각 전자 메일을 분석 하 고 개별 메시지에 desconstructs 합니다. 각 전자 메일은 개별 메시지의 연쇄입니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-107">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages.</span></span> <span data-ttu-id="b72ba-108">그런 다음 작업 집합의 모든 전자 메일을 분석 하 여 전자 메일이 고유한 콘텐츠를 포함 하는지 또는 체인이 다른 전자 메일에 완전히 포함 되어 있는지를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-108">Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email.</span></span> <span data-ttu-id="b72ba-109">최종 전자 메일은 다음 네 가지 범주로 나뉩니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-109">In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="b72ba-110">**포함**: 전자 메일의 마지막 메시지에는 고유한 콘텐츠가 있으며 전자 메일에는 해당 콘텐츠가 완전히이 전자 메일에 포함 된 다른 전자 메일에 포함 된 첨부 파일이 모두 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-110">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>


- <span data-ttu-id="b72ba-111">**포함 빼기**: 전자 메일의 마지막 메시지에는 고유한 콘텐츠가 있지만 전자 메일에는 해당 콘텐츠가 완전히이 전자 메일에 포함 된 다른 전자 메일에 포함 된 첨부 파일이 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-111">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="b72ba-112">**포함 복사본**: 포함/포괄 되는 전자 메일의 정확한 복사본</span><span class="sxs-lookup"><span data-stu-id="b72ba-112">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="b72ba-113">**없음**:이 전자 메일의 콘텐츠는 포함/포괄으로 표시 되는 하나 이상의 전자 메일에 완전히 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-113">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="b72ba-114">Outlook의 대화와는 다른 이유는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="b72ba-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="b72ba-115">이는 한 눈에 볼 때 Outlook의 대화 그룹과 매우 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-115">At a glance, this sounds very similar to conversation groupings in Outlook.</span></span> <span data-ttu-id="b72ba-116">그러나 몇 가지 중요 한 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-116">However, there are some important distinctions.</span></span> <span data-ttu-id="b72ba-117">두 개의 대화에 분기 있는 전자 메일 대화를 생각해 보십시오. 예를 들어 사용자가 대화에서 최신 상태가 아닌 전자 메일에 응답 하 여 대화의 마지막 두 전자 메일이 모두 고유한 콘텐츠를 가지도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-117">Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="b72ba-118">Outlook에서는 전자 메일을 단일 대화로 그룹화 하는 것도 가능 합니다. 마지막 전자 메일만 읽으면 고유한 콘텐츠가 포함 된 두 번째-마지막 전자 메일의 컨텍스트가 손실 된다는 뜻입니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-118">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content.</span></span> <span data-ttu-id="b72ba-119">전자 메일 스레딩은 각 전자 메일을 개별 구성 요소로 구문 분석 하 고 비교 하므로 전자 메일 스레딩은 마지막 두 개의 전자 메일을 모두 inclusives으로 표시 하 여 포함으로 표시 된 모든 전자 메일을 읽을 때 컨텍스트를 놓치지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b72ba-119">Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>