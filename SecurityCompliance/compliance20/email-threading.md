---
title: 전자 메일 스레드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d4328971a6b13c60c4d8b9f5b6db310d72a5b215
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29705999"
---
# <a name="email-threading"></a><span data-ttu-id="f0510-102">전자 메일 스레드</span><span class="sxs-lookup"><span data-stu-id="f0510-102">Email threading</span></span>

<span data-ttu-id="f0510-p101">진행 하는 동안에 대 한 전자 메일 대화를 고려해 야 합니다. 대부분의 경우에서 스레드에서 마지막 전자 메일에는 모든 위 전자 메일;의 내용이 포함 됩니다. 마지막 전자 메일을 검토에서 발생 한 스레드에서 대화의 전체 컨텍스트를 제공 합니다. 전자 메일 스레딩 검토자가 모든 상황에 맞는 손실 하지 않고 빠르게 수집 된 문서를 검토할 수 있도록 이러한 전자 메일을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0510-p101">Consider an email conversation that has been going on for a while. In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread. Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="f0510-106">전자 메일 스레딩 기능은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="f0510-106">What does email threading do?</span></span>

<span data-ttu-id="f0510-p102">각 전자 메일 및 desconstructs 구문 분석 하 여 전자 메일 스레딩 개별 메시지; 되도록 각 전자 메일은 개별 메시지의 체인입니다. 그런 다음, 체인 완전히 다른 전자 메일에 포함 된 경우 또는 전자 메일에 고유한 콘텐츠 있는지 여부를 확인 하려면 작업 집합에서 모든 전자 메일을 분석 합니다. 끝에서 전자 메일 4 개의 범주로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0510-p102">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages. Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email. In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="f0510-110">**포괄 시간**: 전자 메일에는 마지막으로 메시지에 고유한 콘텐츠 및 전자 메일에는 콘텐츠 완전히 포함 된이 전자 메일에 다른 전자 메일에 포함 된 첨부 파일의 모든 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0510-110">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>


- <span data-ttu-id="f0510-111">**빼기 포괄 시간**: 전자 메일에는 마지막으로 메시지에 고유한 콘텐츠 있지만 전자 메일의 하는 콘텐츠 완전히 포함 된이 전자 메일에 다른 전자 메일에 포함 된 첨부 파일의 일부를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0510-111">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="f0510-112">**(포함) 복사본**:는 (포함) / (포함)에서 전자 메일을 뺀 값의 정확한 복사본</span><span class="sxs-lookup"><span data-stu-id="f0510-112">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="f0510-113">**None**:이 전자 메일의 내용을 (포함) 사이의 빼기도 표시 되는 하나 이상의 전자 메일에 완전히 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0510-113">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="f0510-114">차이점은 Outlook에서 대화에서?</span><span class="sxs-lookup"><span data-stu-id="f0510-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="f0510-p103">한눈 소리이 Outlook의 대화 그룹화와 매우 유사 합니다. 그러나 일부 중요 한 차이가 있습니다. 궁금한 점을 두 대화;로 분기 된 전자 메일 대화를 고려 합니다. 예, 다른 사용자에 응답 한 전자 메일 되지 않으므로 최신 정보는 대화에 고유한 콘텐츠를 갖추고 대화의 마지막 두 전자 메일을 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0510-p103">At a glance, this sounds very similar to conversation groupings in Outlook. However, there are some important distinctions. Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="f0510-p104">Outlook은 단일 대화;에 전자 메일 그룹 여전히 마지막 전자 메일 읽기도 고유한 콘텐츠를 포함 하는 2-마지막 전자 메일의 상황에 맞는 누락 된 것을 의미 합니다. 전자 메일 스레딩 각 전자 메일을 개별 구성 요소로 구문 분석 하 고 비교 합니다, 때문에 전자 메일 스레딩으로 표시 하면 마지막 두 전자 메일을 모두 inclusives, 모든 전자 메일이 표시 같이 (포함)의 내용을으로 모든 상황에 맞는 놓치지 않습니다 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0510-p104">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content. Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>