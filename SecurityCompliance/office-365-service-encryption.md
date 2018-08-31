---
title: Office 365 서비스 암호화
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
description: '요약: Microsoft Office 365에서 데이터 복구를 이해 합니다.'
ms.openlocfilehash: 1273cd5556bf51dcdac9bbde1b3e8003ab818811
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533501"
---
# <a name="office-365-service-encryption"></a><span data-ttu-id="510dd-103">Office 365 서비스 암호화</span><span class="sxs-lookup"><span data-stu-id="510dd-103">Office 365 Service Encryption</span></span>

<span data-ttu-id="510dd-p101">Exchange Online 볼륨 수준 암호화를 사용 하 여 외에도 비즈니스, SharePoint Online 및 비즈니스용 OneDrive에 대 한 Skype 고객 데이터를 암호화 서비스 암호화 사용 합니다. 두 키 관리 옵션에 대 한 서비스 암호화 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="510dd-p101">In addition to using volume-level encryption, Exchange Online, Skype for Business, SharePoint Online, and OneDrive for Business also use Service Encryption to encrypt customer data. Service Encryption allows for two key management options:</span></span>
- <span data-ttu-id="510dd-p102">Microsoft는 모든 암호화 키를 관리합니다. (이 옵션은 현재 SharePoint Online, 비즈니스용 OneDrive 및 비즈니스를 위한 Skype에서 사용할 수 있습니다. 켜져 현재 Exchange Online에 대 한 로드맵.)</span><span class="sxs-lookup"><span data-stu-id="510dd-p102">Microsoft manages all cryptographic keys. (This option is currently available in SharePoint Online, OneDrive for Business, and Skype for Business. It is currently on the roadmap for Exchange Online.)</span></span>
- <span data-ttu-id="510dd-p103">고객 서비스 암호화와 함께 사용 되는 루트 키를 제공 하 고 고객 Azure 키 추적용을 사용 하 여 이러한 키를 관리 합니다. Microsoft는 다른 모든 키를 관리합니다. 이 옵션을 고객 키를 호출 하 고 Exchange Online, SharePoint Online 및 비즈니스용 OneDrive에 대 한 현재 사용할 수 있습니다. (이전의 BYOK 사용 하 여 고급 암호화 합니다. 참조 [확장 투명도 및 Office 365 고객에 대 한 제어](http://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) 원래 알림.)</span><span class="sxs-lookup"><span data-stu-id="510dd-p103">The customer supplies root keys used with service encryption and the customer manages these keys using Azure Key Vault. Microsoft manages all other keys. This option is called Customer Key, and it is currently available for Exchange Online, SharePoint Online, and OneDrive for Business. (Previously referred to as Advanced Encryption with BYOK. See [Enhancing transparency and control for Office 365 customers](http://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) for the original announcement.)</span></span>

<span data-ttu-id="510dd-p104">서비스 암호화 여러 이점이 있습니다. 예: 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="510dd-p104">Service encryption provides multiple benefits. For example, it:</span></span>
- <span data-ttu-id="510dd-116">권한 강력한 암호화 보호 맨 위쪽 보호 및 관리 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="510dd-116">provides rights protection and management features on top of strong encryption protection.</span></span>
- <span data-ttu-id="510dd-117">다중 테 넌 트 당-테 넌 트 키 관리를 제공 하는 서비스를 사용 하는 고객 키 옵션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="510dd-117">includes a Customer Key option that enables multi-tenant services to provide per-tenant key management.</span></span>
- <span data-ttu-id="510dd-118">저장 또는 운영 체제에서 처리 하는 고객 데이터에 액세스에서 Windows 운영 체제 관리자의 분리를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="510dd-118">provides separation of Windows operating system administrators from access to customer data stored or processed by the operating system.</span></span>
- <span data-ttu-id="510dd-119">암호화에 대 한 규정 준수 요구 사항이 적용 하는 고객의 요구 사항을 만족 하는 Office 365의 기능을 향상 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="510dd-119">enhances the ability of Office 365 to meet the demands of customers that have compliance requirements regarding encryption.</span></span>

## <a name="customer-key"></a><span data-ttu-id="510dd-120">고객 키</span><span class="sxs-lookup"><span data-stu-id="510dd-120">Customer Key</span></span>
<span data-ttu-id="510dd-p105">고객 키를 사용 하는 온-프레미스 HSM 또는 Azure 키 추적용 중 하나를 사용 하 여 직접 암호화 키를 생성할 수 있습니다. 키가 생성 하는 방법에 관계 없이 고객 Azure 키 추적용을 사용 하 여 제어 하 고 Office 365에서 사용 되는 암호화 키를 관리 합니다. 키에 Azure 키 볼트에 저장 된 후 Exchange Online 및 SharePoint Online과 같은 작업에 할당 된 고 수를 사용 하 여 파일 및 사서함 데이터를 암호화 하는데 사용 되는 키 집합의 루트로 합니다. 고객 키를 사용 하 여 다른 이점 중 하나는 고객 데이터를 처리 하는 Microsoft의 기능을 제어 하는 것입니다. Office 365 (예: 때 고객 Microsoft와 서비스를 종료 또는 클라우드에 저장 된 데이터의 부분을 제거)에서 데이터를 제거 하려는 고객 그렇게 하 고 기술 컨트롤로 고객 키를 사용 하 여 확인 하는 수 있도록 존재 하는이 기능 액세스 하거나 데이터를 처리할 수 있는 Microsoft를 포함 합니다. Microsoft 담당자 고객 데이터에 대 한 액세스 제어를 사용할 수 있는 고객 Lockbox 기능에 더하기 (및 보완)입니다.</span><span class="sxs-lookup"><span data-stu-id="510dd-p105">Using Customer Key, you can generate your own cryptographic keys using either an on-premises HSM or Azure Key Vault. Regardless of how the key is generated, customers use Azure Key Vault to control and manage the cryptographic keys used by Office 365. Once your keys are stored in Azure Key Vault, they can be assigned to workloads such as Exchange Online and SharePoint Online and used to as the root of the keychain used to encrypt your mailbox data and files. One of the other benefits of using Customer Key is to control the ability of Microsoft to process customer data. This capability exists so that a customer that wants to remove data from Office 365 (such as when a customer terminates service with Microsoft or removes a portion of data stored in the cloud) can do so and use Customer Key as a technical control to ensure that no one, including Microsoft, can access or process the data. This is in addition (and a complement) to the Customer Lockbox feature that can be used to control access to customer data by Microsoft personnel.</span></span>

<span data-ttu-id="510dd-p106">Exchange Online에 대 한 Office 365에 대 한 고객 키를 설정 하는 방법을 알아보려면 Skype 비즈니스, SharePoint Online 및, 비즈니스용 OneDrive에 대 한 [고객 키를 사용 하 여 Office 365에서 데이터를 제어](https://support.office.com/article/Controlling-your-data-in-Office-365-using-Customer-Key-f2cd475a-e592-46cf-80a3-1bfb0fa17697)를 참조 합니다. 자세한 내용은 [Office 365 FAQ에 대 한 고객 키](https://support.office.com/article/Customer-Key-for-Office-365-FAQ-41ae293a-bd5c-4083-acd8-e1a2b4329da6)및 [고객 키로 데이터를 준수를 충족 하는 데 도움이 필요한 관리 및 제어를](https://techcommunity.microsoft.com/t5/Microsoft-Ignite-Content-2017/Manage-and-control-your-data-to-help-meet-compliance-needs-with/td-p/117580)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="510dd-p106">To learn how to set up Customer Key for Office 365 for Exchange Online, Skype for Business, SharePoint Online, and OneDrive for Business, see [Controlling your data in Office 365 using Customer Key](https://support.office.com/article/Controlling-your-data-in-Office-365-using-Customer-Key-f2cd475a-e592-46cf-80a3-1bfb0fa17697). For additional information, see the [Customer Key for Office 365 FAQ](https://support.office.com/article/Customer-Key-for-Office-365-FAQ-41ae293a-bd5c-4083-acd8-e1a2b4329da6), and [Manage and control your data to help meet compliance needs with Customer Key](https://techcommunity.microsoft.com/t5/Microsoft-Ignite-Content-2017/Manage-and-control-your-data-to-help-meet-compliance-needs-with/td-p/117580).</span></span>
