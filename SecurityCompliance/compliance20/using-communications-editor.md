---
title: 통신 편집기를 사용 하 여
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
ms.openlocfilehash: 107f45510bcf70942c6f03bdfed0a9090f1d83c0
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608139"
---
# <a name="using-the-communications-editor"></a><span data-ttu-id="491e9-102">통신 편집기를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="491e9-102">Using the Communications Editor</span></span>
<span data-ttu-id="491e9-103">포털 콘텐츠의 콘텐츠를 정의 하면 알림 및 미리 알림/에스컬레이션 관련된 법률 유지, 서식을 지정 하 고 동적으로 콘텐츠를 사용자 지정 하는 통신 편집기를 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="491e9-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="491e9-104">서식 있는 텍스트 편집기</span><span class="sxs-lookup"><span data-stu-id="491e9-104">Rich-Text Editor</span></span> 

<span data-ttu-id="491e9-p101">통신 편집기를 사용 하면 편집기 옵션을 사용 하 여 텍스트를 사용자 지정할 수 있습니다. 예, 사용자가 글꼴 종류를 변경, 글머리 기호 목록, 강조 콘텐츠를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="491e9-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

<<include screenshot>>

## <a name="merge-field-variables"></a><span data-ttu-id="491e9-107">필드 변수를 병합 합니다.</span><span class="sxs-lookup"><span data-stu-id="491e9-107">Merge Field Variables</span></span>

<span data-ttu-id="491e9-p102">전자 메일 병합 변수 통신의 본문 텍스트를 사용자 지정 된 더불어 특성을 포함 하 통신 편집기에서 활용할 수 있습니다. 더불어를 전송 하는 경우 해당 필드와 병합 필드가 채워집니다. 예 더불어 John Smith에 게 전송, 병합 필드 [더불어 이름]는 해당 이름의 번역 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="491e9-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="491e9-p103">서식 있는 텍스트 편집기 컨트롤 맨 위의 **병합 필드** 아이콘을 선택 하 여 전자 메일 병합 필드를 사용할 수 있습니다. 개체 틀 해제 사용자의 커서의 위치를 기반으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="491e9-p103">You can use email merge fields by selecting the **Merge Field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="491e9-113">병합 필드 변수 목록</span><span class="sxs-lookup"><span data-stu-id="491e9-113">List of Merge Field Variables</span></span>
| <span data-ttu-id="491e9-114">필드 이름</span><span class="sxs-lookup"><span data-stu-id="491e9-114">Field Name</span></span>                  | <span data-ttu-id="491e9-115">필드 세부 정보</span><span class="sxs-lookup"><span data-stu-id="491e9-115">Field Details</span></span> | 
| :------------------- | :-------------------: |
| <span data-ttu-id="491e9-116">표시 이름</span><span class="sxs-lookup"><span data-stu-id="491e9-116">Display Name</span></span>  | <span data-ttu-id="491e9-117">더불어의 성과 이름</span><span class="sxs-lookup"><span data-stu-id="491e9-117">Custodian's first and last name</span></span> | 
| <span data-ttu-id="491e9-118">승인 링크</span><span class="sxs-lookup"><span data-stu-id="491e9-118">Acknowledgement Link</span></span>                 | <span data-ttu-id="491e9-119">각 더불어 승인 기록 하려면 사용자 지정 된 링크</span><span class="sxs-lookup"><span data-stu-id="491e9-119">Customized link to record each custodian's acknowledgement</span></span>                 |
| <span data-ttu-id="491e9-120">포털 링크</span><span class="sxs-lookup"><span data-stu-id="491e9-120">Portal Link</span></span>     | <span data-ttu-id="491e9-121">더불어의 규정 준수 포털에 대 한 사용자 지정 된 링크</span><span class="sxs-lookup"><span data-stu-id="491e9-121">Customized link for the custodian's Compliance Portal</span></span>                 |
| <span data-ttu-id="491e9-122">담당자가 발급</span><span class="sxs-lookup"><span data-stu-id="491e9-122">Issuing Officer</span></span>                   | <span data-ttu-id="491e9-123">지정한 발급 담당자의 전자 메일 주소</span><span class="sxs-lookup"><span data-stu-id="491e9-123">Email address of the specified issuing officer</span></span>                   |
| <span data-ttu-id="491e9-124">발급 날짜</span><span class="sxs-lookup"><span data-stu-id="491e9-124">Issuing Date</span></span>                   | <span data-ttu-id="491e9-125">(UTC), 알림을 발급 된 날짜</span><span class="sxs-lookup"><span data-stu-id="491e9-125">date that the notice was issued (UTC)</span></span>              |