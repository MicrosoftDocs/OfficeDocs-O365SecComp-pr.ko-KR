---
title: Office 365 advanced eDiscovery에서 분석 고급 설정에 대 한 설정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a797682f-ad85-4c08-a354-3850ba2237ee
description: 'Office 365 advanced eDiscovery의 분석 프로세스에 대해 거의 중복, 전자 메일 스레드 및 테마를 포함 하 여 고급 설정을 구성 하는 방법을 알아봅니다. '
ms.openlocfilehash: d8dfb9f3ecfcda0f267dfccdc716eda40fe450b2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260864"
---
# <a name="set-analyze-advanced-settings-in-office-365-advanced-ediscovery"></a><span data-ttu-id="3e4f5-103">Office 365 advanced eDiscovery에서 분석 고급 설정에 대 한 설정</span><span class="sxs-lookup"><span data-stu-id="3e4f5-103">Set Analyze advanced settings in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="3e4f5-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="3e4f5-106">advanced eDiscovery는 모듈 설정 분석을 위한 기본 고급 매개 변수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-106">Advanced eDiscovery provides default advanced parameters for Analyze module settings.</span></span> <span data-ttu-id="3e4f5-107">다음 절차에서는 지정할 수 있는 설정에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-107">The following procedure describes settings that can be specified.</span></span>
  
1. <span data-ttu-id="3e4f5-108">**설치 분석 \> \> 준비** 탭에서 **고급 설정** (페이지 맨 아래)을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-108">In the **Prepare \> Analyze \> Setup** tab, click **Advanced settings** (at the bottom of the page).</span></span> <span data-ttu-id="3e4f5-109">다음 패널이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-109">The following panel is displayed.</span></span> 
    
    ![고급 설정 설정 분석](media/c9ea3017-e19a-456b-a742-c3d07121a3f6.png)
  
2. <span data-ttu-id="3e4f5-111">**거의 중복 항목 및 전자 메일 스레드 매개 변수**에서 필요에 따라 다음에 대 한 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-111">In **Near-duplicates and Email threads parameters**, select values for the following as necessary:</span></span>
    
  - <span data-ttu-id="3e4f5-112">**최소 단어 수**: 아래의 파일은 거의 중복 된 분석을 위해 제출 되지 않는 단어의 최소 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-112">**Minimum number of words**: Minimum number for words, below which a file is not submitted for Near-duplicate analysis.</span></span> 
    
  - <span data-ttu-id="3e4f5-113">**최대 단어 수**: 위 단어의 최대 수, 즉 파일을 거의 중복 된 분석용으로 전송 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-113">**Maximum number of words**: Maximum number for words, above which a file is not submitted for Near-duplicate analysis.</span></span>
    
  - <span data-ttu-id="3e4f5-114">**전자 메일 유사**: 두 개의 전자 메일을 유사한 것으로 간주 하는 최소 resemblance 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-114">**Email similarity**: Minimal level of resemblance for two emails to be considered similar.</span></span> <span data-ttu-id="3e4f5-115">값은 항상 문서 유사성 보다 크거나 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-115">Value is always equal to, or larger than document similarity.</span></span> <span data-ttu-id="3e4f5-116">기본값은 90%입니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-116">Default is 90%.</span></span>
    
3. <span data-ttu-id="3e4f5-117">분석 중에 테마를 처리 하는 데 숫자를 포함 하려면 **테마 매개 변수**에서 **숫자를 테마 분석에 포함** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-117">In **Themes parameters**, select the **Include numbers in theme analysis** check box to include numbers in the processing of Themes during Analyze.</span></span> 
    
4. <span data-ttu-id="3e4f5-118">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3e4f5-118">Click **Save**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3e4f5-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3e4f5-119">See also</span></span>

[<span data-ttu-id="3e4f5-120">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="3e4f5-120">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="3e4f5-121">문서 유사성 이해</span><span class="sxs-lookup"><span data-stu-id="3e4f5-121">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3e4f5-122">분석 옵션 설정</span><span class="sxs-lookup"><span data-stu-id="3e4f5-122">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3e4f5-123">무시 텍스트 설정</span><span class="sxs-lookup"><span data-stu-id="3e4f5-123">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3e4f5-124">분석 결과 보기</span><span class="sxs-lookup"><span data-stu-id="3e4f5-124">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

