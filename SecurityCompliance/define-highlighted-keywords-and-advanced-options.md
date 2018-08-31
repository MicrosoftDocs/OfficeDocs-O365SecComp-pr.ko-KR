---
title: Office 365 Advanced eDiscovery에서 강조 표시된 키워드 및 고급 옵션 정의
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 03cc4387-2c7d-4058-8a44-0deefb58f011
description: '관련성 비용 매개 변수를 지정 하 고 Office 365 고급 eDiscovery에 태그를 지정 하는 동안 관련 파일을 식별할 수 있도록 하려면 사용자 정의 키워드를 추가 하는 방법에 알아봅니다.  '
ms.openlocfilehash: c7e16fc18ba724d5b778b42e3782e04df10c50ec
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533332"
---
# <a name="define-highlighted-keywords-and-advanced-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="c2af4-103">Office 365 Advanced eDiscovery에서 강조 표시된 키워드 및 고급 옵션 정의</span><span class="sxs-lookup"><span data-stu-id="c2af4-103">Define highlighted keywords and advanced options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="c2af4-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="c2af4-p102">고급 eDiscovery에 태그를 지정 하는 동안 관련 파일을 식별 하기 위해 관련성을 사용자 정의 키워드를 추가 하는 것이 같습니다. 키워드에 지정 된 색에 표시할 **관련성 \> 태그**합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-p102">In Advanced eDiscovery, it's possible to add user-defined keywords to Relevance in order to help you identify relevant files while tagging. Keywords will be displayed in the specified colors in **Relevance \> Tag**.</span></span> 
  
<span data-ttu-id="c2af4-p103">아래와 같이 키워드 목록을 추가할 수 및 키워드 목록 및 관련된 문제에 할당 된 색입니다. 도구 설명 표시 하는 키워드의 설명, 있는 경우 이중 밑줄을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-p103">As described below, keyword lists can be added, and colors assigned to the Keywords list and the related issues. A tooltip displays the keyword's description, if one exists, as indicated by a double underline.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c2af4-110">적중 관련성에 강조 표시 및 키워드 보기 적중 결과 관련성 중 문서 내에서 태그 지정 작동 하지 않음 일본어, 중국어 및 한국어 더블 바이트 문자 집합에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-110">Hit highlighting in Relevance and viewing keyword hit results within documents during Relevance tagging does not work for the Japanese, Chinese, and Korean double-byte character sets.</span></span> 
  
## <a name="adding-highlighted-keywords"></a><span data-ttu-id="c2af4-111">강조 표시 된 키워드 추가 (영문)</span><span class="sxs-lookup"><span data-stu-id="c2af4-111">Adding highlighted keywords</span></span>

1. <span data-ttu-id="c2af4-112">**관련성 \> 관련성 설치** 탭 **강조 키워드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-112">In the **Relevance \> Relevance setup** tab, select **Highlighted keywords**.</span></span>
    
2. <span data-ttu-id="c2af4-p104">클릭 하 고 **+** 키워드를 추가 하는 아이콘입니다. **새 키워드 추가** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-p104">Click the **+** icon to add keywords. The **Add new keywords** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="c2af4-115">**키워드**키워드 쉼표로 구분 된 키워드 목록을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-115">In **Keywords**, type the keywords list, separating keywords with commas.</span></span> 
    
4. <span data-ttu-id="c2af4-116">**색** 목록에서 입력 한 키워드 목록 강조 표시 색상을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-116">In the **Color** list, select the color to highlight the entered keywords list.</span></span> 
    
5. <span data-ttu-id="c2af4-117">**문제를 선택** 목록에서 "모든 문제" 또는 선택한 문제 키워드 목록 적용할 것인지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-117">In the **Select issue** list, select whether to apply the keywords list to "All issues" or to selected issues.</span></span> 
    
6. <span data-ttu-id="c2af4-118">**설명**키워드 목록 (선택 사항)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-118">In **Description**, type the keywords list (optional).</span></span>
    
    ![새 키워드를 추가 합니다.](media/1683a71f-0875-48fc-b4ef-01f3b0e8e8e9.png)
  
7. <span data-ttu-id="c2af4-p105">작업을 마치면 **확인** 을 클릭 합니다. 만든된 목록 키워드 목록 테이블에 추가 되 편집 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-p105">Click **OK** when done. The created list is added to the keywords list table and can be edited or deleted.</span></span> 
    
    ![관련성 설정 키워드 목록](media/a05d5ec0-8bde-470d-97e2-456b169281d6.png)
  
<span data-ttu-id="c2af4-123">사용자 정의 키워드 표시할 관련성에 지정 된 색에 \> 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-123">The user-defined keywords will be displayed, in the specified colors in Relevance \> Tag.</span></span> 
  
## <a name="specifying-relevance-setup-advanced-settings"></a><span data-ttu-id="c2af4-124">고급 설정 지정 관련성 설치</span><span class="sxs-lookup"><span data-stu-id="c2af4-124">Specifying Relevance setup advanced settings</span></span>

<span data-ttu-id="c2af4-125">이러한 설정은 관련성에 추적 하 고 판단 그래프를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-125">These settings affect the Track and Decide graphs in Relevance.</span></span>
  
1. <span data-ttu-id="c2af4-126">**관련성 \> 관련성 설치** 탭에서 **고급 설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-126">In the **Relevance \> Relevance setup** tab, select **Advanced settings**.</span></span>
    
2. <span data-ttu-id="c2af4-127">**비용 매개 변수** 대화 상자에서 다음 선택 항목을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-127">In the **Cost parameters** dialog, make the following selections:</span></span> 
    
1. <span data-ttu-id="c2af4-128">**검토 ($) 시간당 비용** 목록에서 달러 선택 하거나 기본값을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-128">In the **Cost review per hour ($)** list, select the amount in dollars or accept the default.</span></span> 
    
2. <span data-ttu-id="c2af4-129">**파일을 검토 하 여 시간 수가** 목록에서 크기를 선택 하거나 기본값을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-129">In the **Number of files reviewed by hour** list, select the amount or accept the default.</span></span> 
    
    ![매개 변수 비용 관련성 설정](media/bab7b5b7-6297-4e7c-b0a6-ba5aa8b21787.png)
  
3. <span data-ttu-id="c2af4-p106">**저장**을 클릭 합니다. 선택한 설정이 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-p106">Click **Save**. The selected settings are saved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2af4-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c2af4-133">See also</span></span>

[<span data-ttu-id="c2af4-134">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="c2af4-134">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="c2af4-135">문제를 정의 하 고 사용자를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-135">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="c2af4-136">가져온된 파일에 추가 하려면 부하를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2af4-136">Setting up loads to add imported files</span></span>](set-up-loads-to-add-imported-files.md)

