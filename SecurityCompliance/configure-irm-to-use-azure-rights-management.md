---
title: Azure 권한 관리를 사용 하도록 IRM 구성
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/13/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 1b1f8c8b-f3b4-439b-910c-cf2f89a07a15
ms.collection:
- M365-security-compliance
description: Office 365 메시지 암호화 (OME)의 새로운 기능을 출시할 때 더 이상 IRM을 별도로 설정할 필요가 없습니다. Microsoft는 Azure 권한 관리와 함께 레거시 OME 및 IRM을 사용 하 여 새 배포를 설정 하는 것은 권장 하지 않습니다. 새 OME 기능에 대 한 자세한 내용은 Office 365 메시지 암호화 FAQ를 참조 하십시오. 조직 내에서 새 OME 기능을 사용할 준비가 되 면 Set up Office 365 Message Encryption capabilities for the Azure Information Protection를 참조 하세요.
ms.openlocfilehash: f98af39c9339743dc97ed26c1a866ba1f474882b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151420"
---
# <a name="configure-irm-to-use-azure-rights-management"></a><span data-ttu-id="6ec3c-106">Azure 권한 관리를 사용 하도록 IRM 구성</span><span class="sxs-lookup"><span data-stu-id="6ec3c-106">Configure IRM to use Azure Rights Management</span></span>

<span data-ttu-id="6ec3c-107">Office 365 메시지 암호화 (OME)의 새로운 기능을 출시할 때 더 이상 IRM을 별도로 설정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec3c-107">With the release of the new capabilities for Office 365 Message Encryption (OME), you no longer need to set up IRM separately.</span></span> <span data-ttu-id="6ec3c-108">Microsoft는 Azure 권한 관리와 함께 레거시 OME 및 IRM을 사용 하 여 새 배포를 설정 하는 것은 권장 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec3c-108">Microsoft does not recommend setting up new deployments using legacy OME and IRM with Azure Rights Management.</span></span> <span data-ttu-id="6ec3c-109">새 OME 기능에 대 한 자세한 내용은 [Office 365 메시지 암호화 FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6ec3c-109">For more information about the new OME capabilities, see the [Office 365 Message Encryption FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e).</span></span> <span data-ttu-id="6ec3c-110">조직 내에서 새 OME 기능을 사용할 준비가 [되 면 Set Up Office 365 Message Encryption capabilities for The Azure Information Protection](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ec3c-110">If you're ready to get started using the new OME capabilities within your organization, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e).</span></span>
  

