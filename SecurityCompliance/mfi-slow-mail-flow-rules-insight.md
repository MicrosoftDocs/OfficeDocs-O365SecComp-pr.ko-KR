---
title: 느린 메일 흐름 규칙 파악
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 5/3/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
description: 관리자는 Security & 준수 센터의 메일 흐름 대시보드에서 느린 메일 흐름 규칙에 대 한 정보를 확인할 수 있습니다.
ms.openlocfilehash: ede12e14f287599cab0e5f39aaf71c38ed519276
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32267230"
---
# <a name="slow-mail-flow-rules-insight"></a><span data-ttu-id="83857-103">느린 메일 흐름 규칙 파악</span><span class="sxs-lookup"><span data-stu-id="83857-103">Slow mail flow rules insight</span></span>

<span data-ttu-id="83857-104">비효율적인 메일 흐름 규칙 (전송 규칙이 라고도 함)은 조직에 대 한 메일 흐름 지연을 야기할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83857-104">Inefficient mail flow rules (also known as transport rules) can lead to mail flow delays for your organization.</span></span> <span data-ttu-id="83857-105">이 통찰력은 조직의 메일 흐름에 영향을 주는 메일 흐름 규칙을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="83857-105">This insight reports mail flow rules that have an impact on your organization's mail flow.</span></span> <span data-ttu-id="83857-106">이러한 규칙 유형의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="83857-106">Examples of these types of rules are:</span></span>

- <span data-ttu-id="83857-107">이를 사용 하는 조건은 대규모 그룹 **의 구성원** 입니다.</span><span class="sxs-lookup"><span data-stu-id="83857-107">Conditions that use **Is member of** for large groups.</span></span>

- <span data-ttu-id="83857-108">정규식 (regex) 패턴 일치를 사용 하는 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="83857-108">Conditions that use complex regular expression (regex) pattern matching.</span></span>

- <span data-ttu-id="83857-109">첨부 파일에서 콘텐츠 검사를 사용 하는 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="83857-109">Conditions that use content checking in attachments.</span></span>

<span data-ttu-id="83857-110">이러한 통찰력은 메일 흐름 규칙을 식별 하 고 미세 조정 하 여 메일 흐름이 지연 되는 것을 줄이는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83857-110">The insight will help you to identify and fine-tune mail flow rules to help reduce mail flow delays.</span></span>

![보안 & 준수 센터의 메일 흐름 대시보드를 통한 메일 흐름 규칙에 대 한 자세한 정보](media/1dd90faa-f065-4b10-8b47-d35dc127fc26.png)

<span data-ttu-id="83857-112">**자세히 보기**를 클릭 하면 규칙을 검토할 수 있는 플라이 아웃 창이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="83857-112">When you click **View details**, a flyout pane appears where you can review the rule.</span></span> <span data-ttu-id="83857-113">플라이 아웃 창에서 **예제 메시지 보기** 를 클릭 하 여 규칙의 영향을 받는 메시지 종류를 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83857-113">In the flyout pane, can also click **view sample messages** to see what kind of messages are impacted by the rule.</span></span>

![메일 흐름 대시보드의 느린 메일 흐름 규칙 이해에서 세부 정보 보기를 클릭 한 후의 플라이 아웃 창](media/2cbd43b7-1f21-4338-a70c-7b50de5c69cd.png)

## <a name="see-also"></a><span data-ttu-id="83857-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="83857-115">See also</span></span>

<span data-ttu-id="83857-116">메일 흐름 대시보드의 다른 메일 흐름 정보에 대 한 자세한 내용은 [Security & 준수 센터의 메일 흐름 정보](mail-flow-insights.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="83857-116">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights.md).</span></span>
