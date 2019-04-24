---
title: Office 365 advanced eDiscovery에서 강조 표시 된 키워드 및 고급 옵션 정의
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 03cc4387-2c7d-4058-8a44-0deefb58f011
description: 'Office 365 Advanced eDiscovery에서 태그를 지정 하는 동안 관련 파일을 식별 하는 데 도움이 되는 사용자 정의 키워드와 관련성을 추가 하는 방법에 대해 알아보고 비용 매개 변수  '
ms.openlocfilehash: aec9efac91cc3fb48068fca9b6b7313f829f4fe2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257090"
---
# <a name="define-highlighted-keywords-and-advanced-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="8009c-103">Office 365 advanced eDiscovery에서 강조 표시 된 키워드 및 고급 옵션 정의</span><span class="sxs-lookup"><span data-stu-id="8009c-103">Define highlighted keywords and advanced options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="8009c-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="8009c-106">고급 eDiscovery에서는 태그를 지정 하는 동안 관련 파일을 식별 하는 데 도움이 되도록 사용자 정의 키워드를 관련성에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-106">In Advanced eDiscovery, it's possible to add user-defined keywords to Relevance in order to help you identify relevant files while tagging.</span></span> <span data-ttu-id="8009c-107">키워드는 **관련성 \> 태그**의 지정 된 색에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-107">Keywords will be displayed in the specified colors in **Relevance \> Tag**.</span></span> 
  
<span data-ttu-id="8009c-108">아래에 설명 된 대로 키워드 목록과 키워드 목록 및 관련 문제에 할당 된 색을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-108">As described below, keyword lists can be added, and colors assigned to the Keywords list and the related issues.</span></span> <span data-ttu-id="8009c-109">키워드에 대 한 설명이 있으면 이중 밑줄로 표시 되는 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-109">A tooltip displays the keyword's description, if one exists, as indicated by a double underline.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8009c-110">관련성을 강조 표시 하 고 관련 태그를 지정 하는 동안 문서 내에서 키워드 방문 횟수 결과를 볼 때 일본어, 중국어 및 한국어 더블 바이트 문자 집합에는 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-110">Hit highlighting in Relevance and viewing keyword hit results within documents during Relevance tagging does not work for the Japanese, Chinese, and Korean double-byte character sets.</span></span> 
  
## <a name="adding-highlighted-keywords"></a><span data-ttu-id="8009c-111">강조 표시 된 키워드 추가</span><span class="sxs-lookup"><span data-stu-id="8009c-111">Adding highlighted keywords</span></span>

1. <span data-ttu-id="8009c-112">\*\* \> 관련성 관련성 설정\*\* 탭에서 **강조 표시 된 키워드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-112">In the **Relevance \> Relevance setup** tab, select **Highlighted keywords**.</span></span>
    
2. <span data-ttu-id="8009c-113">키워드를 **+** 추가 하려면 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-113">Click the **+** icon to add keywords.</span></span> <span data-ttu-id="8009c-114">**새 키워드 추가** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-114">The **Add new keywords** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="8009c-115">키워드 \*\*\*\* 에 키워드 목록을 쉼표로 구분 하 여 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-115">In **Keywords**, type the keywords list, separating keywords with commas.</span></span> 
    
4. <span data-ttu-id="8009c-116">**색** 목록에서 색을 선택 하 여 입력 한 키워드 목록을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-116">In the **Color** list, select the color to highlight the entered keywords list.</span></span> 
    
5. <span data-ttu-id="8009c-117">**문제점 선택** 목록에서 "모든 문제" 또는 선택한 문제에 키워드 목록을 적용할지 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-117">In the **Select issue** list, select whether to apply the keywords list to "All issues" or to selected issues.</span></span> 
    
6. <span data-ttu-id="8009c-118">**설명**에 키워드 목록을 입력 합니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="8009c-118">In **Description**, type the keywords list (optional).</span></span>
    
    ![새 키워드를 추가 합니다.](media/1683a71f-0875-48fc-b4ef-01f3b0e8e8e9.png)
  
7. <span data-ttu-id="8009c-120">완료 되 면 **확인을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-120">Click **OK** when done.</span></span> <span data-ttu-id="8009c-121">만들어진 목록은 키워드 목록 테이블에 추가 되 고 편집 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-121">The created list is added to the keywords list table and can be edited or deleted.</span></span> 
    
    ![관련성 설정 키워드 목록](media/a05d5ec0-8bde-470d-97e2-456b169281d6.png)
  
<span data-ttu-id="8009c-123">사용자 정의 키워드는 관련성 \> 태그의 지정 된 색에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-123">The user-defined keywords will be displayed, in the specified colors in Relevance \> Tag.</span></span> 
  
## <a name="specifying-relevance-setup-advanced-settings"></a><span data-ttu-id="8009c-124">관련성 설정 고급 설정 지정</span><span class="sxs-lookup"><span data-stu-id="8009c-124">Specifying Relevance setup advanced settings</span></span>

<span data-ttu-id="8009c-125">이러한 설정은 트랙 및 결정 그래프에 관련성을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-125">These settings affect the Track and Decide graphs in Relevance.</span></span>
  
1. <span data-ttu-id="8009c-126">**관련성 \> 관련성 설정** 탭에서 **고급 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-126">In the **Relevance \> Relevance setup** tab, select **Advanced settings**.</span></span>
    
2. <span data-ttu-id="8009c-127">**비용 매개 변수** 대화 상자에서 다음을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-127">In the **Cost parameters** dialog, make the following selections:</span></span> 
    
1. <span data-ttu-id="8009c-128">**시간당 비용 검토** 목록에서 금액을 달러로 선택 하거나 기본값을 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-128">In the **Cost review per hour ($)** list, select the amount in dollars or accept the default.</span></span> 
    
2. <span data-ttu-id="8009c-129">**시간별로 검토 한 파일 수** 목록에서 크기를 선택 하거나 기본값을 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-129">In the **Number of files reviewed by hour** list, select the amount or accept the default.</span></span> 
    
    ![매개 변수 비용 관련성 설정](media/bab7b5b7-6297-4e7c-b0a6-ba5aa8b21787.png)
  
3. <span data-ttu-id="8009c-131">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-131">Click **Save**.</span></span> <span data-ttu-id="8009c-132">선택한 설정이 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8009c-132">The selected settings are saved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8009c-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8009c-133">See also</span></span>

[<span data-ttu-id="8009c-134">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8009c-134">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="8009c-135">문제 정의 및 사용자 할당</span><span class="sxs-lookup"><span data-stu-id="8009c-135">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="8009c-136">가져온 파일을 추가하도록 로드 설정</span><span class="sxs-lookup"><span data-stu-id="8009c-136">Setting up loads to add imported files</span></span>](set-up-loads-to-add-imported-files.md)

