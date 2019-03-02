---
title: Skype, OneDrive, SharePoint 및 Exchange에 대 한 Office 365 암호화
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
description: '요약: Skype, OneDrive, SharePoint 및 Exchange Online의 암호화에 대 한 설명입니다.'
ms.openlocfilehash: 55141f671e6cb3d7ea837bfcf9701e37a18fb7ba
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357569"
---
# <a name="office-365-encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-and-exchange-online"></a>비즈니스용 Skype, 비즈니스용 OneDrive, SharePoint online 및 Exchange Online에 대 한 Office 365 암호화

Office 365은 실제 데이터 센터 보안, 네트워크 보안, 액세스 보안, 응용 프로그램 보안, 데이터 보안 등 다양 한 계층에 광범위 한 보호를 제공 하는 강력한 보안 환경입니다.

## <a name="skype-for-business"></a>비즈니스용 Skype

비즈니스용 Skype 고객 데이터는 모임 참가자가 업로드 한 파일 또는 프레젠테이션 형식으로 나머지 위치에 저장 될 수 있습니다. 웹 회의 서버는 256 비트 키와 함께 AES를 사용 하 여 고객 데이터를 암호화 합니다. 암호화 된 고객 데이터는 파일 공유에 저장 됩니다. 각 고객 데이터는 임의로 생성 되는 서로 다른 256 비트 키를 사용 하 여 암호화 됩니다. 회의에서 고객 데이터를 공유 하는 경우 웹 회의 서버는 회의 클라이언트에 게 HTTPS를 통해 암호화 된 고객 데이터를 다운로드 하도록 지시 합니다. 고객 데이터의 암호를 해독할 수 있도록 해당 키를 클라이언트에 전송 합니다. 또한 웹 회의 서버는 클라이언트에서 전화 회의 고객 데이터에 액세스할 수 있도록 하기 전에 회의 클라이언트를 인증 합니다. 웹 회의에 참가 하는 경우 각 회의 클라이언트는 먼저 TLS를 통해 프런트 엔드 서버 내부에서 실행 되는 회의 포커스 구성 요소가 있는 SIP 대화 상자를 설정 합니다. 회의 포커스가 웹 회의 서버에서 생성 된 인증 쿠키를 회의 클라이언트에 전달 합니다. 그러면 회의 클라이언트가 서버에서 인증을 받기 위해 인증 쿠키를 제공 하는 웹 회의 서버에 연결 합니다.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online 및 비즈니스용 OneDrive

SharePoint Online의 모든 고객 파일은 항상 단일 테 넌 트로 단독으로 사용 되는 고유한 각 파일당 키로 보호 됩니다. 이 키는 SharePoint Online 서비스에서 만들거나 관리 하거나 고객 키를 사용 하 고 고객을 위해 만들고 관리 하는 경우입니다. 파일이 업로드 되 면 Azure storage로 전송 되기 전에 업로드 요청의 컨텍스트 내에서 SharePoint Online에 의해 암호화가 수행 됩니다. 파일을 다운로드 하면 SharePoint Online은 고유한 문서 식별자를 기반으로 Azure storage에서 암호화 된 고객 데이터를 검색 하 고 사용자에 게 보내기 전에 해당 고객 데이터의 암호를 해독 합니다. Azure storage에는 고객 데이터를 해독 하거나 식별 하거나 이해할 수 있는 기능이 없습니다. 모든 암호화 및 암호 해독은 Azure Active Directory 및 SharePoint Online 인 테 넌 트 격리를 적용 하는 동일한 시스템에서 수행 됩니다.

Office 365의 여러 작업은 sharepoint online의 모든 파일을 저장 하는 Microsoft 팀을 비롯 하 여 sharepoint online에 데이터를 저장 하 고, 저장소에는 sharepoint online을 사용 하는 비즈니스용 OneDrive를 포함 합니다. SharePoint Online에 저장 된 모든 고객 데이터는 다음에 해당 하는 하나 이상의 AES 256 비트 키를 사용 하 여 암호화 되 고 데이터 센터 전체에 분산 됩니다. 이 암호화 프로세스의 모든 단계는 FIPS 140-2 수준 2 유효성 검사입니다. fips 140-2 준수에 대 한 자세한 내용은 [fips 140-2 준수](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))를 참조 하십시오.

- 파일 크기에 따라 각 파일은 하나 이상의 청크로 분할 됩니다. 각 청크는 고유한 AES 256 비트 키를 사용 하 여 암호화 됩니다.
- 파일이 업데이트 되 면 변경 내용이 하나 이상의 청크로 분할 되 고 각 청크가 별도의 고유 키를 사용 하 여 암호화 됩니다.
- 이러한 청크-파일, 파일 조각 및 업데이트 델타는 여러 azure 저장소 계정에 무작위로 분산 되는 azure 저장소의 blob로 저장 됩니다.
- 이러한 고객 데이터 청크의 암호화 키 집합은 자체 암호화 됩니다.

    - blob를 암호화 하는 데 사용 되는 키는 SharePoint Online 콘텐츠 데이터베이스에 저장 됩니다.
    - 콘텐츠 데이터베이스는 휴지 상태의 데이터베이스 액세스 제어 및 암호화로 보호 됩니다. [Azure SQL 데이터베이스](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview)에서 tde ( [투명 한 데이터 암호화](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-tde) )를 사용 하 여 암호화를 수행 합니다. azure SQL Database는 관계형 데이터, JSON, 공간 및 XML과 같은 구조를 지 원하는 Microsoft Azure의 범용 관계형 데이터베이스 서비스입니다. 이러한 비밀은 테 넌 트 수준이 아니라 SharePoint Online의 서비스 수준에 있습니다. 이러한 비밀 (마스터 키 라고도 함)은 키 저장소 라는 별도의 보안 리포지토리에 저장 됩니다. tde는 활성 데이터베이스와 데이터베이스 백업 및 트랜잭션 로그 모두에 대해 rest 보안을 제공 합니다.
    - 고객이 선택적 키를 입력 하면 해당 고객 키가 Azure key Vault에 저장 되 고, 서비스는이 키를 사용 하 여 사이트 키를 암호화 하는 데 사용 되는 테 넌 트 키를 암호화 한 다음 파일 수준 키를 암호화 하는 데 사용 됩니다. 기본적으로 고객은 키를 제공할 때 새 키 계층 구조가 도입 됩니다.
- 파일을 다시 어셈블하는 데 사용 되는 맵은 암호화 된 키와 함께 콘텐츠 데이터베이스에 저장 되며 암호를 해독 하는 데 필요한 마스터 키와는 별개입니다.
- 각 Azure storage 계정에는 액세스 유형별 고유 자격 증명 (읽기, 쓰기, 열거 및 삭제)이 있습니다. 각 자격 증명 집합은 보안 키 저장소에 보관 되며 주기적으로 새로 고쳐집니다. 위에서 설명한 것 처럼 서로 다른 세 가지 유형의 저장소가 있으며 각 저장소에는 고유한 기능이 있습니다.
    - 고객 데이터는 Azure storage에 암호화 된 blob로 저장 됩니다. 각 고객 데이터 청크에 대 한 키는 암호화 되 고 콘텐츠 데이터베이스에 별도로 저장 됩니다. 고객 데이터 자체에는 암호를 해독 하는 방법에 대 한 단서가 포함 되지 않습니다.
    - 콘텐츠 데이터베이스는 SQL Server 데이터베이스입니다. Azure storage에 저장 된 고객 데이터 blob 및 해당 blob를 암호화 하는 데 필요한 키를 찾아서 다시 조립 하는 데 필요한 맵을 포함 합니다. 그러나 키 집합 자체는 위에 설명 된 대로 암호화 되며 별도의 키 저장소에 보관 됩니다.
    - 키 저장소는 콘텐츠 데이터베이스 및 Azure 저장소와 물리적으로 구분 됩니다. 여기에는 각 Azure storage 컨테이너에 대 한 자격 증명과 콘텐츠 데이터베이스에 저장 된 암호화 키 집합에 대 한 마스터 키가 포함 됩니다.

이러한 세 가지 저장소 구성 요소 (Azure blob 저장소, 콘텐츠 데이터베이스 및 키 저장소)는 물리적으로 구분 됩니다. 구성 요소 중 하나에 저장 된 정보는 자체적으로 사용할 수 없습니다. 세 가지 모두에 대 한 액세스 권한이 없는 경우에는 청크에 키를 검색 하거나, 키를 해독 하 여 사용할 수 있도록 하거나, 키를 해당 청크에 연결 하거나, 각 청크의 암호를 해독 하거나, 문서를 구성 된 청크에서 다시 생성 하는 것이 불가능 합니다.

데이터 센터의 컴퓨터에서 실제 디스크 볼륨을 보호 하는 BitLocker 인증서는 팜 키에 의해 보호 되는 보안 리포지토리 (SharePoint Online secret store)에 저장 됩니다.

각 blob 키를 보호 하는 tde 키는 다음 두 위치에 저장 됩니다.

- 보안 저장소-BitLocker 인증서를 보관 하며 팜 키로 보호 됩니다. 한
- Azure SQL Database에서 관리 하는 보안 저장소에 있습니다.

Azure 저장소 컨테이너에 액세스 하는 데 사용 되는 자격 증명은 sharepoint online 보안 저장소에도 보관 되며 필요에 따라 각 sharepoint online 팜에 위임 됩니다. 이러한 자격 증명은 데이터를 읽거나 쓰는 데 사용 되는 별도의 자격 증명을 가진 Azure storage SAS 서명이 며, 정책은 60 일 마다 자동으로 만료 되도록 정책이 적용 됩니다. 서로 다른 자격 증명을 사용 하 여 데이터를 읽거나 쓰고 (둘 다 아님) SharePoint Online 팜에서 열거할 수 있는 권한이 부여 되지 않습니다.

> [!NOTE]
> Office 365 미국 정부 고객의 경우 데이터 blob은 Azure U.S. 정부 저장소에 저장 됩니다. 또한 office 365 미국 정부의 SharePoint Online 키에 대 한 액세스는 특별히 스크린 된 office 365 직원으로 제한 됩니다. Azure 미국 정부 운영 인력은 데이터 blob를 암호화 하는 데 사용 되는 SharePoint Online 키 저장소에 액세스할 수 없습니다.

SharePoint Online 및 비즈니스용 onedrive의 데이터 암호화에 대 한 자세한 내용은 [비즈니스용 onedrive 및 sharepoint online의 데이터 암호화](https://technet.microsoft.com/en-us/library/dn905447.aspx)를 참조 하세요.

### <a name="list-items-in-sharepoint-online"></a>SharePoint Online의 목록 항목

목록 항목은 임시 생성 되는 고객 데이터의 작은 청크 이며, 사용자가 만든 목록의 행, sharepoint online 블로그의 개별 게시물 또는 sharepoint online 위 키 페이지의 항목 등 사이트 내에서 동적으로 추가 될 수 있습니다. 목록 항목은 콘텐츠 데이터베이스 (Azure SQL 데이터베이스)에 저장 되며 tde로 보호 됩니다.

## <a name="encryption-of-data-in-transit"></a>전송 중인 데이터 암호화

비즈니스용 OneDrive 및 SharePoint Online에는 데이터 센터를 시작 및 종료하는 데이터에 대한 두 가지 시나리오가 있습니다.

- 인터넷을 통한 비즈니스용 OneDrive **와의 클라이언트 통신** 은 SSL/TLS 연결을 사용 합니다. 모든 SSL 연결은 2048 비트 키를 사용 하 여 설정 됩니다.
- 데이터 **센터 간에 데이터가** 이동 하는 가장 중요 한 이유는 데이터 센터 간에 데이터가 변경 되는 주된 이유는 재해 복구를 사용 하도록 설정 하는 것입니다. 예를 들어이 파이프에 따라 SQL Server 트랜잭션 로그 및 blob 저장소 델타 이동 이 데이터는 개인 네트워크를 사용 하 여 이미 전송 되었지만 고급 암호화로 더 보호 됩니다.

## <a name="exchange-online"></a>Exchange Online

Exchange Online은 모든 사서함 데이터에 대해 bitlocker를 사용 하며 bitlocker 구성은 [암호화를 위해 bitlocker](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)에 설명 되어 있습니다. 서비스 수준 암호화는 사서함 수준에서 모든 사서함 데이터를 암호화 합니다. 

서비스 암호화 외에 Office 365은 서비스 암호화를 기반으로 구축 된 고객 키를 지원 합니다. 고객 키는 microsoft의 로드맵에도 해당 하는 Exchange Online 서비스 암호화에 대 한 microsoft 관리 키 옵션입니다. 이 암호화 방법은 서버 관리자와 데이터의 암호를 해독 하는 데 필요한 암호화 키를 분리 하는 것을 제공 하 고 암호화가 데이터에 직접 적용 되므로 ( 논리적 디스크 볼륨에 암호화를 적용 하는 BitLocker와 대조) Exchange 서버에서 복사한 고객 데이터는 암호화 된 상태로 유지 됩니다.

exchange online 서비스 암호화의 범위는 exchange online 내에서 rest에 저장 되는 고객 데이터입니다. (비즈니스용 Skype에는 거의 모든 사용자 생성 콘텐츠가 사용자의 exchange online 사서함에 저장 되므로 exchange online의 서비스 암호화 기능을 상속 합니다.)
