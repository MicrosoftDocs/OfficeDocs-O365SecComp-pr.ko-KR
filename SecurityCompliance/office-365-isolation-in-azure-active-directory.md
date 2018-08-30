---
title: Office 365 격리 및 Azure Active Directory에 대 한 액세스 제어
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
description: '요약: Azure Active Directory 내에서 작동 하는 격리 및 액세스 제어 하는 방식입니다.'
ms.openlocfilehash: db4fa0d026c6c608f09252c65bf1e0de5354f68c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534026"
---
# <a name="isolation-and-access-control-in-azure-active-directory"></a><span data-ttu-id="98e71-103">Azure Active Directory에서 격리 및 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="98e71-103">Isolation and Access Control in Azure Active Directory</span></span>

<span data-ttu-id="98e71-p101">Azure Active Directory 논리 데이터 격리를 통해 매우 안전한 방식으로 여러 테 넌 트를 호스팅할 수 있도록 디자인 되었습니다. Azure Active Directory에 대 한 액세스 권한 부여 계층에 의해 제어 됩니다. Azure Active Directory 콘텐츠 액세스 하거나 공동 테 넌 트에 의해 손상 수 있도록 고객의 콘텐츠를 보호 하기 위해 보안 경계도 테 넌 트 컨테이너를 사용 하는 고객을 격리 합니다. Azure Active Directory 권한 부여 계층에서 세 검사가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98e71-p101">Azure Active Directory was designed to host multiple tenants in a highly secure way through logical data isolation. Access to Azure Active Directory is gated by an authorization layer. Azure Active Directory isolates customers using tenant containers as security boundaries to safeguard a customer's content so that the content cannot be accessed or compromised by co-tenants. Three checks are performed by Azure Active Directory's authorization layer:</span></span>
- <span data-ttu-id="98e71-108">Azure Active Directory 테 넌 트에 대 한 액세스에 대 한 보안 주체를 사용 하 시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="98e71-108">Is the principal enabled for access to Azure Active Directory tenant?</span></span>
- <span data-ttu-id="98e71-109">이 테 넌이 트의 데이터에 대 한 액세스에 대 한 보안 주체를 사용 하 시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="98e71-109">Is the principal enabled for access to data in this tenant?</span></span>
- <span data-ttu-id="98e71-110">요청 된 데이터 액세스 유형에 대 한 권한이 부여 된이 테 넌이 트에는 사용자의 역할?</span><span class="sxs-lookup"><span data-stu-id="98e71-110">Is the principal's role in this tenant authorized for the type of data access requested?</span></span>

<span data-ttu-id="98e71-p102">없음 응용 프로그램, 사용자, 서버 또는 서비스는 적절 한 인증 및 토큰 또는 인증서 없이 Azure Active Directory에 액세스할 수 있습니다. 적절 한 자격 증명에 의해 포함할지 하지 하는 경우 요청은 거부 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98e71-p102">No application, user, server, or service can access Azure Active Directory without the proper authentication and token or certificate. Requests are rejected if they are not accompanied by proper credentials.</span></span>

<span data-ttu-id="98e71-113">효과적으로, Azure Active Directory 자체 보호 된 컨테이너에, 정책 및 하 고 전적으로 소유 하 고 테 넌 트 관리 하는 컨테이너에 있는 사용 권한을 사용 하 여 각 테 넌 트를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="98e71-113">Effectively, Azure Active Directory hosts each tenant in its own protected container, with policies and permissions to and within the container solely owned and managed by the tenant.</span></span>
 
![Azure 컨테이너](media/office-365-isolation-azure-container.png)

<span data-ttu-id="98e71-p103">테 넌 트 컨테이너의 개념 속 포털을 영구 저장소에서 모든 계층에서 디렉터리 서비스에 밀접 하 게 됩니다. 여러 Azure Active Directory에 대 한 테 넌 트 메타 데이터는 동일한 실제 디스크에 저장 되 면 하는 경우에 다음과 같은 간에 관계가 테 넌 트 관리자에 의해 지정 되는 디렉터리 서비스에 의해 정의 된 것이 아닌 컨테이너입니다. 있을 수 없는 직접 연결 Azure Active Directory 저장소에 모든 요청 하는 응용 프로그램 또는 권한 부여 계층을 통해 하지 않고도 서비스에서.</span><span class="sxs-lookup"><span data-stu-id="98e71-p103">The concept of tenant containers is deeply ingrained in the directory service at all layers, from portals all the way to persistent storage. Even when multiple Azure Active Directory tenant metadata is stored on the same physical disk, there is no relationship between the containers other than what is defined by the directory service, which in turn is dictated by the tenant administrator. There can be no direct connections to Azure Active Directory storage from any requesting application or service without first going through the authorization layer.</span></span>

<span data-ttu-id="98e71-118">아래 예제에서는 Contoso와 Fabrikam에는 모두 내용이 별도, 전용 컨테이너, 그리고 이러한 컨테이너 동일한 기본 인프라 서버 및 저장소, 등의 일부를 공유할 수 있는 경우에 때는 계속 별도 하 고, 서로 격리에 의해 제어 권한 부여 및 액세스 제어의 레이어 합니다.</span><span class="sxs-lookup"><span data-stu-id="98e71-118">In the example below, Contoso and Fabrikam both have separate, dedicated containers, and even though those containers may share some of the same underlying infrastructure, such as servers and storage, they remain separate and isolated from each other, and gated by layers of authorization and access control.</span></span>
 
![Azure 전용된 컨테이너](media/office-365-isolation-azure-dedicated-containers.png)

<span data-ttu-id="98e71-120">그리고 Azure Active Directory 내에서 실행할 수 있는 없는 응용 프로그램 구성 요소는 하나의 테 넌 트 강제로 다른 테 넌 트의 무결성을 위반 하 고, 다른 테 넌 트의 암호화 키에 액세스 하거나, 서버에서 원시 데이터를 읽을 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98e71-120">In addition, there are no application components that can execute from within Azure Active Directory, and it is not possible for one tenant to forcibly breach the integrity of another tenant, access encryption keys of another tenant, or read raw data from the server.</span></span>

<span data-ttu-id="98e71-p104">기본적으로 Azure Active Directory에는 다른 테 넌 트의 id가 발급 하는 모든 작업 수 없도록 합니다. 각 테 넌 트 클레임 기반 액세스 제어를 통해 Azure Active Directory 내에서 논리적으로 격리 됩니다. 읽기 및 쓰기 데이터 테 넌 트 컨테이너도 범위가 지정 되며 함께 보안 경계를 사용 하 여으로 테 넌 트를 적용 하는 내부 추상 계층 및 역할 기반 액세스 제어 (rbac 역할) 계층에 의해 제어 디렉터리의. 모든 디렉터리 데이터 액세스 요청 이러한 계층에 의해 처리 되 고 Office 365의 모든 액세스 요청은 위의 논리에 의해 policed 합니다.</span><span class="sxs-lookup"><span data-stu-id="98e71-p104">By default, Azure Active Directory disallows all operations issued by identities in other tenants. Each tenant is logically isolated within Azure Active Directory through claims-based access controls. Reads and writes of directory data are scoped to tenant containers, and gated by an internal abstraction layer and a role-based access control (RBAC) layer, which together enforce the tenant as the security boundary. Every directory data access request is processed by these layers and every access request in Office 365 is policed by the logic above.</span></span>

<span data-ttu-id="98e71-p105">Azure Active Directory에는 북미, 미국 정부, 독일, 유럽 연합, 및 World Wide 파티션이 합니다. 테 넌 트에 있는 경우 단일 파티션을 있으며 파티션 여러 테 넌 트 포함 될 수 있습니다. 사용자 로부터 추출 하는 파티션 정보는 합니다. 지정한 파티션에 (그 안에 있는 모든 테 넌 트 포함)는 여러 데이터 센터에 복제 됩니다. 테 넌 트에 대 한 파티션 테 넌 트 (예: 국가 코드)의 속성을 기준으로 선택 됩니다. 비밀 및 각 파티션에서 다른 중요 한 정보는 전용된 키로 암호화 됩니다. 키 새 파티션을 만들 때 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98e71-p105">Azure Active Directory has North America, U.S. Government, European Union, Germany, and World Wide partitions. A tenant exists in a single partition, and partitions can contain multiple tenants. Partition information is abstracted away from users. A given partition (including all the tenants within it) is replicated to multiple datacenters. The partition for a tenant is chosen based on properties of the tenant (e.g., the country code). Secrets and other sensitive information in each partition is encrypted with a dedicated key. The keys are generated automatically when a new partition is created.</span></span>

<span data-ttu-id="98e71-p106">Azure Active Directory 시스템 기능에는 각 사용자 세션에 고유한 인스턴스는 합니다. 또한 Azure Active Directory를 사용 하 여 암호화 기술 정보의 무단 및 의도 하지 않은 전송을 방지 하기 위해 네트워크 수준에서 공유 시스템 리소스의 격리를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="98e71-p106">Azure Active Directory system functionalities are a unique instance to each user session. In addition, Azure Active Directory uses encryption technologies to provide isolation of shared system resources at the network level to prevent unauthorized and unintended transfer of information.</span></span>
