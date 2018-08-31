---
title: Office 365 리소스 제한
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
ms.collection: Strat_O365_Enterprise
description: '요약: Office 365에서 다양 한 응용 프로그램에 대 한 리소스에 대 한 정보를 제한합니다.'
ms.openlocfilehash: a2e7ef42f9bf224363f3b10a5e450d6127f11585
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534163"
---
# <a name="resource-limits"></a><span data-ttu-id="01b43-103">리소스 제한 사항</span><span class="sxs-lookup"><span data-stu-id="01b43-103">Resource Limits</span></span>

<span data-ttu-id="01b43-p101">리소스 제한 할당량 (제한)를 사용 하 여 및 제한이 적용 됩니다. Azure Active Directory와 개별 Office 365 서비스 모두를 사용합니다. 제한은 서비스 관련 되며 새 기능이 추가 될 때 시간이 지남에 따라 변경 합니다. 다양 한 서비스에 대 한 현재 제한에 대 한 자세한 내용은, 다음 항목을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="01b43-p101">Resource limits are enforced using quotas (limits) and throttling. Azure Active Directory and the individual Office 365 services use both. Limits are service-specific and change over time as new capabilities are added. For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="01b43-108">Azure Active Directory 서비스 제한 및 제한 사항</span><span class="sxs-lookup"><span data-stu-id="01b43-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="01b43-109">Exchange Online 제한</span><span class="sxs-lookup"><span data-stu-id="01b43-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="01b43-110">Exchange Online Protection 제한</span><span class="sxs-lookup"><span data-stu-id="01b43-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="01b43-111">SharePoint Online 소프트웨어 경계 및 제한 사항</span><span class="sxs-lookup"><span data-stu-id="01b43-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="01b43-112">비즈니스 제한에 대 한 Skype</span><span class="sxs-lookup"><span data-stu-id="01b43-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="01b43-113">Yammer REST API 및 속도 제한</span><span class="sxs-lookup"><span data-stu-id="01b43-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="01b43-114">영향의 파일 크기 제한</span><span class="sxs-lookup"><span data-stu-id="01b43-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="01b43-p102">이러한 제한 외에도 몇가지 제한 메커니즘 Azure Active Directory 및 Office 365 전체에서 사용 됩니다. Microsoft의 데이터 센터의 네트워크 리소스는 서비스를 사용 하는 고객의 광범위 한 집합에 대해 최적화 된는 서비스 내에서 제한 하는 것이 특히 중요 합니다. 제한 메커니즘에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01b43-p102">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365. Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services. Throttling mechanisms include:</span></span>
- <span data-ttu-id="01b43-118">Azure Active Directory 및 Office 365 기능 사용자 수준 제한, 트랜잭션 또는 (스크립트 또는 코드)가 단일 사용자가 수행할 수 있는 동시 통화 수를 제한 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="01b43-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="01b43-p103">기본 제한 정책 PowerShell 테 넌 트를 만들 때 각 테 넌 트에 할당 됩니다. 이 설정은 한 명의 관리자가 열 수 있는 동시 PowerShell 세션의 최대 수 등의 다른 항목에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="01b43-p103">A default PowerShell throttling policy is assigned to each tenant at tenant creation. These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="01b43-121">각 Exchange Online 고객에 게 EWS 클라이언트 작업에 대 한 조정 하는 기본 Exchange 웹 서비스 (EWS) 정책을 모든 Outlook 클라이언트에 적용 하는 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="01b43-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
