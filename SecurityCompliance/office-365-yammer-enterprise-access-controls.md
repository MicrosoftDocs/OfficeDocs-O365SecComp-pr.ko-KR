---
title: Office 365 Yammer Enterprise 액세스 제어
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: '요약: 프로덕션 환경의 Yammer Enterprise 액세스 제어에 대 한 간략 한 요약입니다.'
ms.openlocfilehash: 33126ee6acf42a97148c12917855535a8578e8cf
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090730"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="bef89-103">Yammer Enterprise 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="bef89-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="bef89-p101">Yammer 프로덕션 환경에 대 한 물리적 및 논리적 액세스 모두는 소수의 사용자 (인프라 및 작업)로 제한 됩니다. 다른 Office 365 엔지니어와 마찬가지로 Yammer 엔지니어는 고객 데이터에 대 한 액세스를 영 없이 사용할 수 있습니다. Lockbox와 유사한 승인 기반 just-in-time 액세스 제어 시스템을 사용 하 여 액세스를 요청 해야 하며, 승인자 수가 제한 됩니다. 승인자는 요청을 확인 하 고 (예: 필요에 따라 요청이 합법적인 지를 확인 한 다음 요청을 승인 하거나 거부 합니다.) 요청이 승인 되 면 정의 되 고 제한 된 시간에 JIT 액세스가 부여 되 고 그 이후에는 자동으로 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bef89-p101">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations). As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data. Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers. Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request. If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="bef89-p102">다른 Office 365 서비스와 마찬가지로 Yammer 프로덕션 환경에 대 한 모든 액세스에서 다단계 인증을 활용 합니다. 모든 액세스 및 명령 기록은 사용자에 게 특성을 사용 하며 Yammer 보안 팀에서 정기적으로 기록 및 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef89-p102">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication. All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="bef89-111">yammer 관리 및 관리에 대 한 자세한 내용은 [yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bef89-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>