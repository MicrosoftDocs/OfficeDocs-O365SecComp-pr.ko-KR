---
title: 메일 루프 파악
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: cb801985-3c89-4979-9c18-17829a4cb563
description: 관리자는 Office 365 보안 & 준수 센터의 메일 흐름 대시보드에서 메일 루프 통찰력에 대해 알아볼 수 있습니다.
ms.openlocfilehash: babf102e7645de26d4af0a947319856468ccf755
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455240"
---
# <a name="mail-loop-insight"></a><span data-ttu-id="e98c6-103">메일 루프 파악</span><span class="sxs-lookup"><span data-stu-id="e98c6-103">Mail loop insight</span></span>

<span data-ttu-id="e98c6-104">메일 루프는 시스템 리소스를 낭비 하 고 조직의 메일 볼륨 할당량을 소비 하며, ndr 또는 바운스 메시지가 라고도 하는 혼동 하지 않는 보고서를 원래 보낸 사람에 게 전송 하므로 잘못 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e98c6-104">A mail loop is bad because it wastes system resources, consumes your organization's mail volume quota, and sends confusing non-delivery reports (also known as NDRs or bounce messages) to the original senders.</span></span> <span data-ttu-id="e98c6-105">이 통찰력은 조직에서 메일 루프가 발견 되는 시기, 루프에 포함 된 전자 메일 도메인, 그리고 루프에 있던 이전 날짜의 메시지 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e98c6-105">This insight reports when a mail loop is found in your organization, the email domains that are involved in the loop, and the number of messages from the previous day that were in the loop.</span></span>

![Office 365 보안 & 준수 센터의 메일 흐름 대시보드에 있는 메일 루프 통찰력](media/c3f707cb-4c89-4e88-989c-81ce1d1d6b99.png)

<span data-ttu-id="e98c6-107">**세부 정보 보기** 를 클릭 하 여 플라이 아웃 창에서 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e98c6-107">You can click **View details** to see the details in a flyout pane.</span></span> <span data-ttu-id="e98c6-108">또한 가장 일반적인 루프 시나리오를 파악 하 고 루프를 수정 하는 데 권장 되는 작업 (사용 가능한 경우)을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e98c6-108">We also identify the most common loop scenarios and provide the recommended actions (if available) to fix the loop.</span></span>

![메일 흐름 대시보드에서 잘못 된 루프 통찰력에서 세부 정보 보기를 클릭 한 후 플라이 아웃 창](media/f7e21300-c62f-41ec-853f-4a2775cd8aa7.png)
