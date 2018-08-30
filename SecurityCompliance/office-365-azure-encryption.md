---
title: Azure의 office 365 암호화
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
description: '요약: Azure의 암호화의 설명 합니다.'
ms.openlocfilehash: 5e1d0fc02daa7fe057e14045d1948762612b3674
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533547"
---
# <a name="office-365-encryption-in-azure"></a>Azure의 office 365 암호화

## <a name="introduction"></a>소개
암호화 된 통신 및 운영 프로세스와 같은 Azure의 기술적 보호조치 도움말 데이터 보안을 유지 합니다. 추가 암호화 기능을 구현 하 고 암호화 키를 관리 하는 유연성을 수도 있습니다. 고객 구성에 관계 없이 Microsoft Azure의 고객 데이터를 보호 하기 위해 암호화를 적용 합니다. Microsoft도 사용 하면 다양 한 암호화를 제어 하 고 암호화 키를 관리 하는 고급 기술을 통해 Azure에서 호스팅되는 사용자 데이터를 제어 하는 데이터에 대 한 감사 및 제어 액세스 합니다. 또한 Azure 저장소는 포괄적인 집합이 함께 개발자가 더욱 안전한 응용 프로그램을 사용 하도록 설정 하는 보안 기능을 제공 합니다.

Azure 한 위치에서 다른 위치로 이동할 때 데이터를 보호 하기 위해 많은 메커니즘을 제공 합니다. Microsoft은 클라우드 서비스 및 고객 간에 이동 하는 경우 데이터를 보호 하기 위해 TLS를 사용 합니다. Microsoft의 데이터 센터 Azure 서비스에 연결 하는 클라이언트 시스템과 TLS 연결을 협상 합니다. 고유 키를 기준으로 Microsoft의 클라우드 서비스와 고객의 클라이언트 시스템 간의 연결을 보호 하는 전달 완전 보안 (PFS)입니다. 또한 연결 RSA 기반 2, 048 비트 암호화 키 길이 사용합니다. 이 조합은 하기 어려운 것 다른 사람에 대 한에서 전송 된 intercept 및 access 데이터를 합니다.

[클라이언트쪽 암호화](https://docs.microsoft.com/azure/storage/storage-client-side-encryption), HTTPS, 또는 SMB 3.0을 사용 하 여 전송 되는 응용 프로그램 및 Azure 사이 데이터를 보호할 수 있습니다. 사용자 고유의 Vm (가상 컴퓨터)와 사용자 간의 트래픽에 대 한 암호화를 사용할 수 있습니다. [Azure 가상 네트워크](https://azure.microsoft.com/services/virtual-network/)회사 VPN 게이트웨이 및 Azure 가상 네트워크에 있는 Vm 사이와 같이 간의 트래픽을 암호화 하는 업계 표준 IPsec 프로토콜을 사용할 수 있습니다.

보관 된 데이터, Azure이 제공 하 AES-256에 대 한 지원 등의 많은 암호화 옵션을 사용자의 요구 사항에 가장 적합 한 데이터 저장소 시나리오를 선택 하려면 유연성을 제공 합니다. [저장소 서비스 암호화](https://docs.microsoft.com/azure/storage/storage-service-encryption)사용 하 여 Azure 저장소에 기록 데이터 자동으로 암호화 될 수 및 운영 체제와 Vm에서 사용 되는 데이터 디스크 [Azure 디스크 암호화](https://docs.microsoft.com/azure/security/azure-security-disk-encryption)를 사용 하 여 암호화할 수 있습니다. 또한 [공유 액세스 서명을](https://docs.microsoft.com/azure/storage/storage-dotnet-shared-access-signature-part-1)사용 하 여 Azure 저장소에서 데이터 개체에 대 한 위임 된 액세스를 부여할 수 있습니다. 또한 azure [Azure SQL 데이터베이스 및 데이터 웨어하우스에 투명 한 데이터 암호화](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-azure-sql)를 사용 하 여 보관 된 데이터에 대 한 암호화를 제공 합니다.

Azure의 암호화에 대 한 자세한 내용은 [Azure 데이터 암호화-에서-Rest](https://docs.microsoft.com/azure/security/azure-security-encryption-atrest)및 [Azure 암호화 개요](https://docs.microsoft.com/azure/security/security-azure-encryption-overview) 를 참조 하십시오.

## <a name="azure-disk-encryption"></a>Azure 디스크 암호화
[Azure 디스크 암호화](https://docs.microsoft.com/azure/security/azure-security-disk-encryption) 를 사용 하면 Windows 및 Linux 인프라 (IaaS) VM 서비스로 암호화 디스크입니다. Azure 디스크 암호화 Windows의 BitLocker 기능 및 운영 체제 및 데이터 디스크에 대 한 볼륨 수준 암호화를 제공 하는 Linux의 DM 암호화 기능을 활용 합니다. 또한 Azure 저장소의 나머지 부분에서 VM 디스크에 있는 모든 데이터가 암호화 되는 보장 합니다. Azure 디스크 암호화 제어, 관리 및 암호화 키 및 비밀 사용을 감사 하는 데 도움이 되는 Azure 키 Vault와 통합 됩니다.

자세한 내용은 [Azure 디스크 암호화에 대 한 Windows 및 Linux IaaS Vm을](https://docs.microsoft.com/azure/security/azure-security-disk-encryption)참조 하십시오.

## <a name="azure-storage-service-encryption"></a>Azure 저장소 서비스 암호화
[Azure 저장소 서비스 암호화](https://docs.microsoft.com/azure/storage/storage-service-encryption)함께 Azure 저장소 자동으로 데이터를 암호화 유지할 수 있도록 하기 전에 검색 하기 전에 데이터를 저장 하 고 암호 해독 되도록 합니다. 암호화, 암호 해독, 및 키 관리 프로세스는 사용자에 게 완전히 투명 하 게 합니다. [Azure Blob 저장소](https://azure.microsoft.com/services/storage/blobs/) 및 [Azure 파일](https://azure.microsoft.com/services/storage/files/)에 대 한 azure 저장소 서비스 암호화를 사용할 수 있습니다. Azure 저장소 서비스 암호화 기능을 Microsoft에서 관리 되는 암호화 키를 사용할 수도 있습니다 또는 직접 암호화 키를 사용할 수 있습니다. (고유한 키를 사용 하 여 정보를 [고객을 사용 하 여 저장소 서비스 암호화 키 Azure 키 볼트의 관리 되는](https://docs.microsoft.com/azure/storage/common/storage-service-encryption-customer-managed-keys)참조 합니다. Microsoft에서 관리 하는 키를 사용 하는 방법에 대 한 정보를 참조 [보관 된 데이터에 대 한 저장소 서비스 암호화](https://docs.microsoft.com/azure/storage/storage-service-encryption).) 또한 암호화 사용을 자동화할 수 있습니다. 예, 프로그래밍 방식으로 활성화 하거나 비활성화할 수 있습니다 저장소 서비스 암호화 [Azure 저장소 리소스 공급자 REST API](https://msdn.microsoft.com/library/azure/mt163683.aspx), [.NET을 위한 저장소 리소스 공급자 클라이언트 라이브러리](https://msdn.microsoft.com/library/azure/mt131037.aspx), [Azure PowerShell](https://docs.microsoft.com/powershell/azureps-cmdlets-docs)사용 하 여 저장소 계정에 또는 [Azure CLI](https://docs.microsoft.com/azure/storage/storage-azure-cli)합니다.

일부 Office 365 서비스 Azure를 사용 하 여 데이터를 저장 합니다. SharePoint Online 및 비즈니스용 OneDrive Azure Blob 저장소에 데이터를 저장 하 고 테이블, blob, 큐 및 큐에는 채팅 서비스에 대 한 데이터를 저장 하는 Microsoft 팀의 예입니다. 또한 서비스를 신뢰 포털의 규정 준수 관리자 기능 [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/database-encryption-at-rest), (PaaS), 다중-모델 전체적으로 배포 된 데이터베이스를 서비스로 서 플랫폼에서에서 암호화 된 형식으로 저장 하는 고객을 입력 한 데이터를 저장 합니다. Azure 저장소 서비스 암호화 및 테이블, Azure Blob 저장소에 저장 된 데이터를 암호화 하 고 Azure 디스크 암호화 큐도 운영 체제에 대 한 볼륨 암호화를 제공 하려면 Windows 및 IaaS 가상 컴퓨터 디스크 및 데이터 디스크에서 데이터를 암호화 합니다. 솔루션 Azure 저장소의 나머지 부분에서 가상 컴퓨터 디스크에 있는 모든 데이터가 암호화 되는 것을 확인 합니다. [Azure Cosmos DB의 나머지 부분에서 암호화](https://docs.microsoft.com/azure/cosmos-db/database-encryption-at-rest) 키 보안 저장소 시스템, 암호화 된 네트워크 및 암호화 Api를 포함 하 여 여러 보안 기술를 사용 하 여 구현 됩니다.

## <a name="azure-key-vault"></a>Azure Key Vault
보안 키 관리 모범 사례를 암호화 하는 행위를 방금 핵심 아닙니다. 클라우드에서 데이터를 보호 하는 것에 대 한 필수적인 이기도 합니다. [Azure 키 추적용](https://docs.microsoft.com/azure/key-vault/key-vault-whatis) 키 및 하드웨어 보안 모듈 (Hsm)에 저장 된 키를 사용 하는 암호와 같은 작은 기밀 정보를 암호화 하는데 사용 됩니다. Azure 키 추적용은 Microsoft의 권장된 솔루션 관리 및 클라우드 서비스에서 사용 되는 암호화 키에 대 한 액세스를 제어 합니다. 키에 액세스할 수 있는 권한은 서비스 또는 Azure Active Directory 계정 가진 사용자에 게 할당할 수 있습니다. Azure 키 추적용 사용을 구성 하 고 패치를 적용, Hsm 및 키 관리 소프트웨어를 유지 관리 필요가의 조직에서는 필요가 없습니다. Azure 키 추적용와 Microsoft 키에 게 표시 되지 않음 및 응용 프로그램; 자신에 게 직접 액세스할 수 없는 컨트롤을 유지 합니다. 또한 가져오기 또는 Hsm.에서 키를 생성 수 Azure 정보 보호를 포함 하는 구독 하는 조직에서는 자신의 Azure 정보 보호 테 넌 트 (BYOK) [직접 키를 가져올](https://docs.microsoft.com/information-protection/plan-design/byok-price-restrictions) 고객 관리 되는 키를 사용 하 여 구성할 수) 및 [로그 해당 사용법](https://docs.microsoft.com/information-protection/deploy-use/log-analyze-usage)합니다.
