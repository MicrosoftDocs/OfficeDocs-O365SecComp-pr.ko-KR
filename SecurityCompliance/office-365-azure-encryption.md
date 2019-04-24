---
title: Azure의 Office 365 암호화
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: '요약: Azure의 암호화에 대 한 설명입니다.'
ms.openlocfilehash: b8980b3979ada9ac02232065a27a7891936aa945
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265880"
---
# <a name="office-365-encryption-in-azure"></a>Azure의 Office 365 암호화

## <a name="introduction"></a>소개

암호화 된 통신 및 운영 프로세스와 같은 Azure의 기술 보호책은 데이터를 안전 하 게 유지 하는 데 도움이 됩니다. 또한 추가 암호화 기능을 구현 하 고 자체 암호화 키를 관리할 수 있는 유연성을 제공 합니다. Microsoft는 고객 구성에 관계 없이 Azure에서 고객 데이터를 보호 하기 위해 암호화를 적용 합니다. 또한 Microsoft에서는 암호화 키를 암호화, 제어 및 관리 하 고 데이터에 대 한 액세스를 제어 하 고 감사 하기 위한 고급 기술 범위를 통해 Azure에서 호스트 되는 데이터를 제어할 수 있습니다. 또한 Azure Storage는 개발자가 안전한 응용 프로그램을 작성할 수 있도록 하는 광범위 한 보안 기능 집합을 제공 합니다.

Azure는 한 위치에서 다른 위치로 이동 될 때 데이터를 보호 하기 위한 다양 한 메커니즘을 제공 합니다. Microsoft는 클라우드 서비스와 고객 간에 이동할 때 TLS를 사용 하 여 데이터를 보호 합니다. Microsoft의 데이터 센터는 Azure services에 연결 되는 클라이언트 시스템과의 TLS 연결을 협상 합니다. PFS (전달 완전 보안)는 고유한 키에 따라 고객의 클라이언트 시스템과 Microsoft 클라우드 서비스 간의 연결을 보호 합니다. 또한 연결에서는 RSA 기반 2048 비트 암호화 키 길이를 사용 합니다. 이 조합을 사용 하면 누군가가 전송 중인 데이터를 가로채 고 액세스 하기가 어려워집니다.

[클라이언트 쪽 암호화](https://docs.microsoft.com/azure/storage/storage-client-side-encryption), HTTPS 또는 SMB 3.0을 사용 하 여 응용 프로그램 및 Azure 간의 전송으로 데이터를 보호할 수 있습니다. 자체 vm (가상 컴퓨터)과 사용자 간의 트래픽에 대해 암호화를 사용 하도록 설정할 수 있습니다. [Azure 가상 네트워크](https://azure.microsoft.com/services/virtual-network/)를 사용 하는 경우 업계 표준 IPsec 프로토콜을 통해 회사 VPN 게이트웨이와 Azure와 가상 네트워크에 있는 vm 간에 트래픽을 암호화할 수 있습니다.

데이터를 보관 하는 경우 Azure는 AES-256 지원 등의 다양 한 암호화 옵션을 제공 하므로 사용자의 요구에 가장 적합 한 데이터 저장소 시나리오를 유연 하 게 선택할 수 있습니다. [저장소 서비스 암호화](https://docs.microsoft.com/azure/storage/storage-service-encryption)를 사용 하 여 azure storage에 기록 되는 데이터를 자동으로 암호화할 수 있으며, vm에서 사용 되는 운영 체제 및 데이터 디스크를 [azure 디스크 암호화](https://docs.microsoft.com/azure/security/azure-security-disk-encryption)를 사용 하 여 암호화할 수 있습니다. 또한 [공유 액세스 서명을](https://docs.microsoft.com/azure/storage/storage-dotnet-shared-access-signature-part-1)사용 하 여 Azure 저장소의 데이터 개체에 대 한 위임 된 액세스 권한을 부여할 수 있습니다. 또한 azure는 [azure SQL Database 및 data Warehouse에 대해 투명 한 데이터 암호화](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-azure-sql)를 사용 하 여 휴지 데이터에 대 한 암호화를 제공 합니다.

azure의 암호화에 대 한 자세한 내용은 [azure 암호화 개요](https://docs.microsoft.com/azure/security/security-azure-encryption-overview) 및 [azure Data encryption-Rest](https://docs.microsoft.com/azure/security/azure-security-encryption-atrest)를 참조 하세요.

## <a name="azure-disk-encryption"></a>Azure 디스크 암호화

[Azure 디스크 암호화](https://docs.microsoft.com/azure/security/azure-security-disk-encryption) 를 사용 하면 Windows 및 Linux 인프라를 IaaS (Infrastructure as a Service) VM 디스크로 암호화할 수 있습니다. Azure 디스크 암호화는 Windows의 BitLocker 기능과 Linux의 DM 기능을 활용 하 여 운영 체제 및 데이터 디스크에 볼륨 수준 암호화를 제공 합니다. 또한 VM 디스크의 모든 데이터가 Azure storage의 나머지 부분에서 암호화 되도록 합니다. azure 디스크 암호화는 azure Key Vault와 통합 되어 암호화 키 및 비밀의 사용을 제어, 관리 및 감사 하는 데 도움이 됩니다.

자세한 내용은 [Windows 및 Linux IaaS vm 용 Azure 디스크 암호화](https://docs.microsoft.com/azure/security/azure-security-disk-encryption)를 참조 하세요.

## <a name="azure-storage-service-encryption"></a>Azure Storage Service 암호화

[azure storage Service Encryption](https://docs.microsoft.com/azure/storage/storage-service-encryption)을 사용 하는 경우 azure storage는 데이터를 저장 하기 전에 자동으로 암호화 하 고 검색 하기 전에 데이터를 해독 합니다. 암호화, 암호 해독 및 키 관리 프로세스는 사용자에 게 전혀 드러나지 않습니다. azure storage Service 암호화는 [azure Blob Storage](https://azure.microsoft.com/services/storage/blobs/) 및 [azure 파일](https://azure.microsoft.com/services/storage/files/)에 사용 될 수 있습니다. Azure Storage Service 암호화를 사용 하 여 Microsoft에서 관리 하는 암호화 키를 사용할 수도 있고, 자체 암호화 키를 사용할 수도 있습니다. 사용자의 키를 사용 하는 방법에 대 한 자세한 내용은 [Azure Key Vault에서 customer 관리 키를 사용 하 여 Storage Service Encryption](https://docs.microsoft.com/azure/storage/common/storage-service-encryption-customer-managed-keys)를 참조 하세요. Microsoft 관리 키를 사용 하는 방법에 대 한 자세한 내용은 [Rest 데이터에 대 한 저장소 서비스 암호화](https://docs.microsoft.com/azure/storage/storage-service-encryption)를 참조 하세요. 또한 암호화 사용을 자동화할 수 있습니다. 예를 들어 [azure storage resource provider REST API](https://msdn.microsoft.com/library/azure/mt163683.aspx), [.net 용 저장소 리소스 공급자 클라이언트 라이브러리](https://msdn.microsoft.com/library/azure/mt131037.aspx)또는 [azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs)을 사용 하 여 저장소 계정에서 저장소 서비스 암호화를 프로그래밍 방식으로 사용 하거나 사용 하지 않도록 설정할 수 있습니다. [Azure CLI](https://docs.microsoft.com/azure/storage/storage-azure-cli)

일부 Office 365 서비스는 데이터를 저장 하는 데 Azure를 사용 합니다. 예를 들어 Azure Blob storage의 SharePoint Online 및 비즈니스용 OneDrive 저장소 데이터의 경우, Microsoft 팀은 해당 채팅 서비스에 대 한 데이터를 테이블, blob 및 큐에 저장 합니다. 또한 서비스 신뢰 포털의 준수 관리자 기능에는 사용자가 입력 한 데이터를 [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/database-encryption-at-rest), PaaS (Platform as a Service), 전역적으로 분산 된 다중 모델 데이터베이스에 저장 하는 고객에 게 저장할 수 있는 데이터가 저장 됩니다. azure storage Service Encryption azure Blob Storage 및 테이블에 저장 된 데이터를 암호화 하 고 azure 디스크 암호화는 큐의 데이터 및 Windows 및 IaaS 가상 컴퓨터 디스크를 암호화 하 여 운영 체제 및 데이터 디스크에 대 한 볼륨 암호화를 제공 합니다. 이 솔루션은 가상 컴퓨터 디스크의 모든 데이터가 Azure 저장소의 나머지 부분에서 암호화 되도록 합니다. [Azure Cosmos DB의 나머지 암호화](https://docs.microsoft.com/azure/cosmos-db/database-encryption-at-rest) 는 보안 키 저장소 시스템, 암호화 된 네트워크 및 암호화 api를 비롯 한 몇 가지 보안 기술을 사용 하 여 구현 됩니다.

## <a name="azure-key-vault"></a>Azure Key Vault

보안 키 관리는 암호화 모범 사례를 위한 핵심이 아닙니다. 또한 클라우드에서 데이터를 보호 하는 데도 필수적입니다. [Azure 키 자격 증명 모음](https://docs.microsoft.com/azure/key-vault/key-vault-whatis) 을 통해 hsm (하드웨어 보안 모듈)에 저장 된 키를 사용 하는 암호와 같은 키 및 작은 암호를 암호화할 수 있습니다. Azure 키 자격 증명은 클라우드 서비스에서 사용 되는 암호화 키에 대 한 액세스를 관리 및 제어 하기 위한 Microsoft의 권장 솔루션입니다. 키 액세스 권한은 Azure Active Directory 계정이 있는 서비스 또는 사용자에 게 할당 될 수 있습니다. Azure 키 보관소는 hsm 및 키 관리 소프트웨어를 구성, 패치 및 유지 관리 해야 하는 조직입니다. Azure 키 자격 증명 모음을 사용 하는 경우 Microsoft는 사용자의 키를 볼 수 없으며 응용 프로그램에 직접 액세스 하지 않습니다. 제어를 유지 관리 합니다. hsm에서 키를 가져오거나 생성할 수도 있습니다. azure information protection이 포함 된 구독이 있는 조직은 [자신의 키](https://docs.microsoft.com/information-protection/plan-design/byok-price-restrictions) (byok)를 사용 하 여 자신의 Azure information protection 테 넌 트를 구성 하 고 [해당 용도를 기록할](https://docs.microsoft.com/information-protection/deploy-use/log-analyze-usage)수 있습니다.
