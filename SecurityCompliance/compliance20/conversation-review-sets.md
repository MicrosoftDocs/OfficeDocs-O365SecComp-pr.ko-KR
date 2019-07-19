---
title: Advanced eDiscovery에서 대화 검토
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f88bdcfc4ac7ed31ec44a7d18bd74cc2a1842bc5
ms.sourcegitcommit: 2560a3ecc6a5e3b8b79bbf56a157b66c7553682e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35795588"
---
# <a name="review-conversations-in-advanced-ediscovery"></a><span data-ttu-id="7a951-102">Advanced eDiscovery에서 대화 검토</span><span class="sxs-lookup"><span data-stu-id="7a951-102">Review conversations in Advanced eDiscovery</span></span> 

<span data-ttu-id="7a951-103">인스턴트 메시징은 편리 하 게 질문을 하거나, 아이디어를 공유 하거나, 대규모 대상 그룹에 빠르게 의견을 교환할 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-103">Instant messaging is a convenient way to ask questions, share ideas, or quickly communicate across large audiences.</span></span> <span data-ttu-id="7a951-104">Microsoft 팀과 같은 인스턴트 메시징 플랫폼은 기업 공동 작업을 핵심으로 수행 되므로, 조직은 eDiscovery 워크플로에서 이러한 새 형태의 통신 및 공동 작업을 처리 하는 방법을 평가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-104">As instant messaging platforms, like Microsoft Teams, become core to enterprise collaboration, organizations must evaluate how their eDiscovery workflow addresses these new forms of communication and collaboration.</span></span> 

<span data-ttu-id="7a951-105">고급 eDiscovery의 대화 재구성 기능은 상황별 콘텐츠를 식별 하 고 고유한 대화 보기를 생성 하는 데 도움을 주기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-105">The Conversation Reconstruction feature in Advanced eDiscovery is designed to help you identify contextual content and produce distinct conversation views.</span></span> <span data-ttu-id="7a951-106">이 기능을 사용 하면 Microsoft 팀과 같은 플랫폼에서 생성 되는 전체 인스턴트 메시지 대화 ( *스레드된 대화*라고도 함)를 효율적으로 검토 하 고 신속 하 게 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-106">This capability allows you to efficiently and rapidly review complete instant message conversations (also called *threaded conversations*) that are generated in platforms like Microsoft Teams.</span></span>

<span data-ttu-id="7a951-107">대화 재구성을 사용 하 여 기본 제공 기능을 통해 스레드 대화를 다시 생성, 검토 및 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-107">With Conversation Reconstruction, you can use built-in capabilities to reconstruct, review, and export threaded conversations.</span></span> <span data-ttu-id="7a951-108">Advanced eDiscovery 대화 재구성을 사용 하 여 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-108">Use Advanced eDiscovery Conversation Reconstruction to:</span></span>

- <span data-ttu-id="7a951-109">대화 내의 모든 메시지에 대해 고유한 메시지 수준 메타 데이터를 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-109">Preserve unique message-level metadata across all messages within a conversation.</span></span>

- <span data-ttu-id="7a951-110">검색 결과 주위에 상황별 메시지를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-110">Collect contextual messages around your search results.</span></span>

- <span data-ttu-id="7a951-111">스레드 대화를 검토 하 고, 주석을 달고, 교정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-111">Review, annotate, and redact threaded conversations.</span></span>

- <span data-ttu-id="7a951-112">개별 메시지 또는 스레드된 대화 내보내기</span><span class="sxs-lookup"><span data-stu-id="7a951-112">Export individual messages or threaded conversations</span></span>

## <a name="terminology"></a><span data-ttu-id="7a951-113">용어</span><span class="sxs-lookup"><span data-stu-id="7a951-113">Terminology</span></span>

<span data-ttu-id="7a951-114">다음은 대화 재구성 사용을 시작 하는 데 도움이 되는 몇 가지 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-114">Here are few definitions to help you get start using Conversation Reconstruction.</span></span>

- <span data-ttu-id="7a951-115">**메시지:** 대화의 최소 단위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-115">**Messages:** Represent the smallest unit of a conversation.</span></span> <span data-ttu-id="7a951-116">메시지 크기, 구조 및 메타 데이터에 따라 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-116">Messages may vary in size, structure, and metadata.</span></span> 

- <span data-ttu-id="7a951-117">**대화:** 하나 이상의 메시지를 그룹화 한 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-117">**Conversation:** Represents a grouping of one or more messages.</span></span> <span data-ttu-id="7a951-118">서로 다른 응용 프로그램에서 대화를 다양 한 방식으로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-118">Across different applications, conversations may be represented in different ways.</span></span> <span data-ttu-id="7a951-119">일부 응용 프로그램에는 기존 메시지에 회신할 수 있는 명시적인 작업이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-119">In some applications, there is an explicit action that results from replying to an existing message.</span></span> <span data-ttu-id="7a951-120">이 사용자 작업의 결과로 대화가 명시적으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-120">Conversations are formed explicitly as a result of this user action.</span></span> <span data-ttu-id="7a951-121">예를 들어 Microsoft 팀에서 채널 대화를 보여 주는 스크린샷은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-121">For example, here is a screenshot of a channel conversation in Microsoft Teams.</span></span>

   ![Microsoft 팀 채널 대화](../media/threadedchat.png)

   <span data-ttu-id="7a951-123">다른 앱 (예: 팀의 1xN 채팅 메시지)에서는 공식적인 회신 체인이 없으며, 대신 단일 스레드 내에서 메시지가 "플랫 강 합니다."로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-123">In other apps (such as 1xN chat messages in Teams), there is not a formal reply chain and instead messages appear as a "flat river of messages" within a single thread.</span></span> <span data-ttu-id="7a951-124">이러한 유형의 앱은 특정 시간 내에 발생 하는 메시지 그룹에서 대화를 유추 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-124">In these types apps, conversations are inferred from a group of messages that occur within a certain time.</span></span> <span data-ttu-id="7a951-125">이 "일시 그룹화" 메시지 (예를 들어, 회신 체인)는 관심 있는 특정 항목에 대 한 "앞뒤로 이동" 하는 대화를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-125">This "soft-grouping" of messages (as opposed to a reply chain) represent the "back and forth" conversation about a specific topic of interest.</span></span> 

## <a name="step-1-run-a-search"></a><span data-ttu-id="7a951-126">1 단계: 검색 실행</span><span class="sxs-lookup"><span data-stu-id="7a951-126">Step 1: Run a search</span></span>

<span data-ttu-id="7a951-127">관련 custodians 및 콘텐츠 위치를 확인 한 후에는 검색을 만들어 관련 된 콘텐츠를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-127">After you have identified relevant custodians and content locations, you can create a search to find potentially relevant content.</span></span> <span data-ttu-id="7a951-128">고급 eDiscovery 사례의 **검색** 탭에서 **새 검색** 을 클릭 하 고 마법사를 수행 하 여 검색을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-128">On the **Searches** tab in the Advanced eDiscovery case, you can create a search by clicking **New search** and following the wizard.</span></span> <span data-ttu-id="7a951-129">검색을 만들고 검색 쿼리를 작성 하 고 검색 결과를 확인 하는 방법에 대 한 자세한 내용은 [사례에 대 한 데이터 수집](create-search-to-collect-data.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7a951-129">For information about how you can create a search, build a search query, and view the search results, see [Collect data for a case](create-search-to-collect-data.md).</span></span>

## <a name="step-2-create-a-conversation-review-set"></a><span data-ttu-id="7a951-130">2 단계: 대화 검토 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="7a951-130">Step 2: Create a conversation review set</span></span>

<span data-ttu-id="7a951-131">검토 집합에서 문서, 전자 메일 메시지 및 채팅 대화를 검색 하 고 태그를 지정 하 고 주석을 달고 교정 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-131">In a review set, you can search, tag, annotate, and redact documents, email messages, and chat conversations.</span></span> <span data-ttu-id="7a951-132">고급 eDiscovery에서는 개별 메시지 또는 스레드 대화에 따라 대화 검토를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-132">In Advanced eDiscovery, you can customize your review of conversations, based in individual messages or threaded conversations.</span></span> <span data-ttu-id="7a951-133">이는 1 단계에서 만든 검색 결과를 추가 하는 검토 집합 유형에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-133">This is determined by the type of review set that you add the results of the search created in Step 1 to.</span></span> <span data-ttu-id="7a951-134">검토 집합에는 다음과 같은 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-134">There are two different types of review sets:</span></span> 
  
  - <span data-ttu-id="7a951-135">**표준 검토 집합:** 대화의 메시지는 처리 되 고 개별 항목으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-135">**Standard review sets:** Messages in conversations are processed and displayed as individual items.</span></span> 
  
  -  <span data-ttu-id="7a951-136">**대화 검토 집합:** 대화의 메시지는 개별적으로 처리 되지만 대화 보기에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-136">**Conversation review sets:** Messages in conversations are processed individually but displayed in a conversation view.</span></span> <span data-ttu-id="7a951-137">대화 검토 집합에서 스레드 대화 보기의 메시지에 주석을 달고 태그를 지정 하 고이를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-137">In a conversation review set, you can annotate, tag, and redact messages in a threaded conversation view.</span></span> 

<span data-ttu-id="7a951-138">검토 집합에서 콘텐츠를 검토 하 고 관리 하는 방법에 대 한 자세한 내용은 [검토 집합 관리](managing-review-sets.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7a951-138">For more information about how to review and manage content in a review set, see [Manage review sets](managing-review-sets.md).</span></span> 

## <a name="step-3-enable-conversation-retrieval-options"></a><span data-ttu-id="7a951-139">3 단계: 대화 검색 옵션을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="7a951-139">Step 3: Enable conversation retrieval options</span></span>

<span data-ttu-id="7a951-140">검색 쿼리를 검토 하 고 완료 한 후에는 검색 결과를 검토 집합에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-140">After you have reviewed and finalized your search query, you can add the search results to a review set.</span></span> <span data-ttu-id="7a951-141">검색 결과를 검토 집합에 추가 하면 검토 및 분석 프로세스를 용이 하 게 하기 위해 원본 데이터가 Azure 저장소 영역에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-141">When you add your search results into a review set, the original data is copied to an Azure Storage area to facilitate the review and analysis process.</span></span> <span data-ttu-id="7a951-142">검색 결과를 검토 집합에 추가 하는 방법에 대 한 자세한 내용은 [검토 집합에 검색 결과 추가](add-data-to-review-set.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a951-142">For more information about adding search results to a review set, see [Add search results to a review set](add-data-to-review-set.md).</span></span> 

<span data-ttu-id="7a951-143">대화에서 데이터를 검토 집합에 추가할 때 대화 검색 옵션을 사용 하 여 검색을 확장 하 고 상황별 메시지를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-143">When you add data from conversations to a review set, you can use the conversation retrieval options to expand your search and include contextual messages.</span></span> <span data-ttu-id="7a951-144">대화 검색 옵션을 설정 하면 다음과 같은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-144">After you set the conversation retrieval options, the following things can happen:</span></span>

  ![대화 검색](../media/messagesandconversations.png)
  
1. <span data-ttu-id="7a951-146">키워드 및 날짜 범위 쿼리를 사용 하 여 검색에서 *메시지 3*의 방문 횟수를 반환 했습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-146">Using a keyword and date range query, the search returned a hit on *Message 3*.</span></span> <span data-ttu-id="7a951-147">이 메시지는 *CRC1*에 설명 된 보다 큰 대화의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-147">This message was part of a larger conversation, illustrated by *CRC1*.</span></span> 
  
2. <span data-ttu-id="7a951-148">검토 집합에 데이터를 추가 하 고 대화 검색 옵션을 사용 하도록 설정 하면 Advanced eDiscovery는 뒤로 이동 하 여 *CRC1*의 다른 항목을 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-148">When you add the data into a review set and enable the conversation retrieval options, Advanced eDiscovery will go back and collect other items in *CRC1*.</span></span> 
  
3. <span data-ttu-id="7a951-149">항목이 검토 집합에 추가 된 후에는 *CRC1*에서 모든 개별 메시지를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-149">After the items have been added to the review set, you can review all the individual messages from *CRC1*.</span></span> 



<span data-ttu-id="7a951-150">대화 검색을 사용 하도록 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="7a951-150">To enable conversation retrieval:</span></span>
  
1. <span data-ttu-id="7a951-151">고급 eDiscovery 사례의 **검색** 탭에서 검색을 선택 하 고 플라이 아웃 페이지에서 **설정을 검토 하려면 추가를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-151">On the **Searches** tab in the Advanced eDiscovery case, select a search, and then click **Add to review set** on the flyout page.</span></span>
  
2. <span data-ttu-id="7a951-152">기존 검토 집합을 선택 하거나 검토 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-152">Select an existing review set or create a review set.</span></span> <span data-ttu-id="7a951-153">표준 또는 대화 검토 집합에 검색 결과를 추가할 때 검색 옵션을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-153">You can configure retrieval options when adding search results to a standard or a conversation review set.</span></span>
  
3. <span data-ttu-id="7a951-154">**모음 옵션**에서 검색 시 확장할 콘텐츠 원본에 대 한 대화 검색 옵션을 구성한 다음 **추가** 를 클릭 하 여 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-154">Under **Collection options**, configure the conversation retrieval options for the content sources that you want to expand in your search, and then click **Add** to start the process.</span></span>  
  
4. <span data-ttu-id="7a951-155">**작업** 탭에서 **집합을 검토 하도록 추가** 작업을 완료 한 후에는 대화 검토를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-155">After the **Add to review set** job on the **Jobs** tab has finished, you can start reviewing the conversations.</span></span>

## <a name="step-4-review-conversations-in-the-review-set"></a><span data-ttu-id="7a951-156">4 단계: 검토 집합의 대화 검토</span><span class="sxs-lookup"><span data-stu-id="7a951-156">Step 4: Review conversations in the review set</span></span>

<span data-ttu-id="7a951-157">콘텐츠를 처리 하 고 검토 집합에 추가한 후에는 검토 집합에서 데이터 검토를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-157">After the content has been processed and added to the review set, you can start reviewing the data in the review set.</span></span> <span data-ttu-id="7a951-158">검토 기능은 콘텐츠가 표준 검토 설정 또는 대화 검토 집합에 추가 되었는지 여부에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-158">The review capabilities are different depending on whether the content was added to a standard review set or a conversation review set.</span></span> 

### <a name="reviewing-conversations-in-a-standard-review-set"></a><span data-ttu-id="7a951-159">표준 검토 집합의 대화 검토</span><span class="sxs-lookup"><span data-stu-id="7a951-159">Reviewing conversations in a standard review set</span></span>

<span data-ttu-id="7a951-160">표준 검토 집합에서 메시지가 사서함 폴더에 저장 되는 방식과 마찬가지로 개별 항목으로 처리 되 고 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-160">In a standard review set, messages are processed and displayed as individual items, similar to how they're stored in a mailbox folder.</span></span> <span data-ttu-id="7a951-161">이 워크플로에서 각 메시지는 개별 항목으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-161">In this workflow, each message is processed as a separate item.</span></span> <span data-ttu-id="7a951-162">따라서 표준 검토 집합에서는 스레드 요약 및 내보내기 옵션을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-162">As a result, the threaded summary and export options aren't available in a standard review set.</span></span> 

  ![표준 검토 설정](../media/standardrs.PNG)

### <a name="reviewing-conversations-in-a-conversation-review-set"></a><span data-ttu-id="7a951-164">대화 검토 설정에서 대화 검토</span><span class="sxs-lookup"><span data-stu-id="7a951-164">Reviewing conversations in a conversation review set</span></span>

<span data-ttu-id="7a951-165">대화 검토 집합에서 개별 메시지는 함께 스레드된 다음 대화로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-165">In a conversation review set, individual messages are threaded together and presented as conversations.</span></span> <span data-ttu-id="7a951-166">이렇게 하면 상황별 대화를 검토 하 고 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-166">This lets you review and export contextual conversations.</span></span> 

  ![대화 검토 설정](../media/ConversationRSOptions.PNG)

<span data-ttu-id="7a951-168">다음 섹션에서는 대화 검토 집합의 대화를 검토 하 고 내보내는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-168">The following sections describe reviewing and exporting conversations in a conversation review set.</span></span>

#### <a name="reviewing-conversations"></a><span data-ttu-id="7a951-169">대화 검토</span><span class="sxs-lookup"><span data-stu-id="7a951-169">Reviewing conversations</span></span>

<span data-ttu-id="7a951-170">대화 검토 집합에서 다음 옵션을 사용 하 여 검토 프로세스를 쉽게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-170">In a conversation review set, you can use the following options to facilitate the review process.</span></span>

- <span data-ttu-id="7a951-171">**대화 별 그룹화:** 사용자가 검토 프로세스를 간소화 하 고 빠르게 수행할 수 있도록 같은 대화 내의 메시지를 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-171">**Group by conversation:** Groups messages within the same conversation together to help users simplify and expedite their review process.</span></span> 

- <span data-ttu-id="7a951-172">**요약 보기:** 스레드 대화를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-172">**Summary view:** Displays the threaded conversation.</span></span> <span data-ttu-id="7a951-173">이 보기에서는 전체 대화를 볼 수 있으며 개별 메시지에 대 한 메타 데이터에 액세스할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-173">In this view, you can see the entire conversation and also access the metadata for each individual message.</span></span>  
  
   - <span data-ttu-id="7a951-174">개별 메시지에 대 한 메타 데이터 보기</span><span class="sxs-lookup"><span data-stu-id="7a951-174">View metadata for individual messages</span></span>
   
   - <span data-ttu-id="7a951-175">개별 메시지 다운로드</span><span class="sxs-lookup"><span data-stu-id="7a951-175">Download individual messages</span></span>

- <span data-ttu-id="7a951-176">**텍스트 보기:** 전체 대화에 대해 추출 된 텍스트를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-176">**Text view:** Provides the extracted text for the entire conversation.</span></span> 

- <span data-ttu-id="7a951-177">**주석 보기:** 대화의 스레드된 보기에 대 한 피드백을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-177">**Annotate view:** Lets you markup a threaded view of the conversation.</span></span> <span data-ttu-id="7a951-178">대화의 모든 메시지는 같은 주석이 달린 문서를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-178">All messages in the conversation share the same annotated document.</span></span>

- <span data-ttu-id="7a951-179">**태그 지정:** 검토 집합의 대화를 볼 때 코딩 패널에서 태그 지정 **패널** 을 클릭 하 여 태그를 확인 하 고 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-179">**Tagging:** When viewing conversations in a review set, you can view and apply tags by clicking **Tagging panel** in the Coding panel.</span></span>

- <span data-ttu-id="7a951-180">**대화 내용 변환을 다시 실행 합니다.** 메시지가 대화 검토 설정에 추가 되 면 변환 작업이 자동으로 실행 되어 스레드 요약을 만들고 보기에 주석을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-180">**Rerun conversation conversion:** When messages are added to a conversation review set, a conversion job is automatically run to create the threaded summary and annotate views.</span></span> <span data-ttu-id="7a951-181">대화 재구성 작업이 실패 하면 검토 설정에서 **대화 Pdf 만들기 > 실행** 을 클릭 하 여이 작업을 다시 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-181">If the Conversation Reconstruction job fails, you can rerun this job by clicking **Action > Create conversation PDFs** in the review set.</span></span>


#### <a name="exporting-conversations"></a><span data-ttu-id="7a951-182">대화 내보내기</span><span class="sxs-lookup"><span data-stu-id="7a951-182">Exporting conversations</span></span>

<span data-ttu-id="7a951-183">대화 검토 집합에서 다음 옵션을 설정 하 여 대화를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-183">In a conversation review set, you can set the following options to export conversations:</span></span>

![내보내기](../media/export.png)

<span data-ttu-id="7a951-185">위한.</span><span class="sxs-lookup"><span data-stu-id="7a951-185">a.</span></span> <span data-ttu-id="7a951-186">메타 데이터 옵션</span><span class="sxs-lookup"><span data-stu-id="7a951-186">Metadata options</span></span>

   - <span data-ttu-id="7a951-187">**파일 로드:** 각 개별 메시지, 전자 메일 및 문서에 대 한 메타 데이터가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-187">**Load file:** Metadata is included for each individual message, email, and document.</span></span> <span data-ttu-id="7a951-188">대화에서 각 메시지에 대 한 행이 하나씩 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-188">There is one row for each message in a conversation.</span></span> 

   - <span data-ttu-id="7a951-189">**태그:** 검토 프로세스의 태그가 메타 데이터 파일에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-189">**Tags:** Tags from your review process are included in the metadata file.</span></span> <span data-ttu-id="7a951-190">대화에서 메시지는 같은 태그를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-190">Messages in a conversation share the same tags.</span></span> 

<span data-ttu-id="7a951-191">b.</span><span class="sxs-lookup"><span data-stu-id="7a951-191">b.</span></span> <span data-ttu-id="7a951-192">대화 옵션</span><span class="sxs-lookup"><span data-stu-id="7a951-192">Conversation options</span></span>
  
   - <span data-ttu-id="7a951-193">**대화 파일:** 대화 파일을 내보낼 때 주석 보기가 PDF 파일로 변환 되 고 내보내기 폴더로 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-193">**Conversation files:** When you export conversation files, the annotated view is converted to a PDF file and downloaded to the export folder.</span></span> <span data-ttu-id="7a951-194">한 대화 파일의 메시지는 동일한 대화 파일의 PDF 버전을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-194">Messages in one conversation file point to the PDF version of the same conversation file.</span></span>  
  
   - <span data-ttu-id="7a951-195">**개별 채팅 메시지:** 개별 메시지를 내보낼 때 대화의 각 고유 메시지를 독립 실행형 항목으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-195">**Individual chat messages:** When you export individual messages, each unique message in the conversation is exported as a standalone item.</span></span> <span data-ttu-id="7a951-196">이 파일은 사서함에 저장 된 것과 같은 형식으로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-196">The file is exported in the same format that it was saved as in the mailbox.</span></span> <span data-ttu-id="7a951-197">특정 대화의 경우 여러 .msg 파일이 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-197">For a specific conversation, you receive multiple .msg files.</span></span> 

     >[!NOTE]
     > <span data-ttu-id="7a951-198">대화 파일에 주석을 적용 한 경우 이러한 주석은 개별 메시지로 전송 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-198">If you applied annotations to the conversation file, these annotations won't be transferred to the individual messages.</span></span> 

<span data-ttu-id="7a951-199">&.</span><span class="sxs-lookup"><span data-stu-id="7a951-199">c.</span></span> <span data-ttu-id="7a951-200">기타 옵션</span><span class="sxs-lookup"><span data-stu-id="7a951-200">Other options</span></span>

   - <span data-ttu-id="7a951-201">**내보낸 모든 콘텐츠에 대 한 텍스트 파일 생성:** 검토 집합에서 내보낸 각 대화에 대해 텍스트 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-201">**Generate text files for all exported content:** Generates a text file for each conversation exported from the review set.</span></span> 

   - <span data-ttu-id="7a951-202">**내보낸 콘텐츠를 Redacted pdf로 바꾸기:** 검토 프로세스 중에 redacted 대화 파일이 생성 되 면 내보내는 동안 이러한 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-202">**Replace exported content with redacted PDFs:** If redacted conversation files are generated during the review process, then these files are available during export.</span></span> <span data-ttu-id="7a951-203">이 옵션을 선택 하지 않으면 서 네이티브 파일만 내보낼지 아니면 네이티브 파일을 redacted 버전 (이 옵션을 선택 하면)로 대체 하 여 PDF 파일로 내보내지는 지 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a951-203">You can decided whether to export only the native files (by not selecting this option) or to replace the native files with the redacted versions of the native files (by selecting this option), which are exported as PDF files.</span></span>

## <a name="more-information"></a><span data-ttu-id="7a951-204">추가 정보</span><span class="sxs-lookup"><span data-stu-id="7a951-204">More information</span></span>

<span data-ttu-id="7a951-205">Advanced eDiscovery에서 사례 데이터를 검토 하는 방법에 대 한 자세한 내용은 다음 문서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7a951-205">To learn more about how to review case data in Advanced eDiscovery, see the following articles:</span></span>

- [<span data-ttu-id="7a951-206">사례 데이터 보기</span><span class="sxs-lookup"><span data-stu-id="7a951-206">View case data</span></span>](view-documents-in-review-set.md) 

- [<span data-ttu-id="7a951-207">대/소문자 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="7a951-207">Analyze case data</span></span>](analyzing-data-in-review-set.md)

- [<span data-ttu-id="7a951-208">사례 데이터 내보내기</span><span class="sxs-lookup"><span data-stu-id="7a951-208">Export case data</span></span>](exporting-data-ediscover20.md)
