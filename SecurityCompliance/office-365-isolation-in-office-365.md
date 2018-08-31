---
title: Office 365 격리 및 Office 365의에서 액세스 제어
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
description: '요약: Office 365의 다양 한 응용 프로그램 내에서 격리 및 액세스 제어의 설명 합니다.'
ms.openlocfilehash: c1989bc546df357740ea963a1a241dfa14557931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534050"
---
# <a name="isolation-and-access-control-in-office-365"></a>Office 365에서 격리 및 액세스 제어

Azure Active Directory 및 Office 365 서비스, 엔터티, 수백 수십을 포함 하는 매우 복잡 한 데이터 모델을 사용 하 여 다양 한 관계 및 매우 많은 수의 특성 (엔터티, 관계와 특성은 주로 응용 프로그램별). 높은 수준에서 Azure Active Directory 및 서비스 디렉터리는 테 넌 트 및 받는 사람 컨테이너 하 고 동기화 상태 기반 복제 프로토콜을 사용 하 여 유지 됩니다. 디렉터리 정보, Azure Active Directory에 보관 하는 외에도 각 서비스도 인프라가 자신의 디렉터리 서비스 (예: Exchange 온라인 디렉터리 서비스, SharePoint 온라인 디렉터리 서비스 등). 
 
![Office 365 테 넌 트 데이터 동기화](media/office-365-isolation-tenant-data-sync.png)

이 모델에서는 디렉터리 데이터의 단일 원본 없음는 있습니다. 데이터의 모든 개별 요소 특정 시스템에 의해 소유 하 고 있지만 모든 데이터를 보유 하는 단일 시스템이 없습니다. Office 365 서비스 데이터 모델을 실현 하기 위해 Azure Active Directory와 상호 운용 됩니다. Azure Active Directory는 일반적으로 모든 서비스에 의해 자주 사용 되는 작은 및 정적 데이터는 공유 데이터에 대 한 "사실 시스템" 됩니다. Office 365와 Azure Active Directory 내에서 사용 하 여 페더레이션된 모델 데이터의 공유 보기를 제공 합니다.

Office 365 실제 저장소와 Azure 클라우드 저장소를 사용합니다. Exchange Online (Exchange Online Protection 포함) 및 Skype 비즈니스를 위한 고객 데이터에 대 한 고유한 저장소를 사용 합니다. SharePoint Online의 SQL Server 저장소 및 저장소 수준에서 고객 데이터의 추가 격리에 대 한 요구를 필요로 하는 Azure 저장소를 활용 합니다.

## <a name="exchange-online"></a>Exchange Online
Exchange Online 사서함 데이터베이스를 호출 하는 확장 가능한 저장소 엔진 (ESE) 데이터베이스 내에서 호스팅되는 사서함 내에서 고객 데이터를 저장 합니다. 사용자 사서함, 연결 된 사서함, 공유 사서함 및 공용 폴더 사서함이 포함 됩니다. 사용자 사서함에 저장 된 Skype 대화 기록 등의 비즈니스 콘텐츠에 대 한 포함 될 수도 있습니다. 사용자 사서함 콘텐츠를 전자 메일 및 전자 메일 첨부 파일, 일정 및 약속 있음/없음 정보, 연락처, 작업, 메모, 그룹 및 유추 데이터를 포함 합니다.

Exchange Online 내에서 각 사서함 데이터베이스에는 여러 테 넌 트에서 사서함을 포함합니다. 모든 사서함은 테 넌 시 내 포함 되는 권한 부여 코드에 의해 보호 됩니다. 으로 Exchange와의 온-프레미스 배포를 기본적으로 할당 된 사용자만 액세스를 권한이 사서함입니다. 사서함의 보안을 유지 하는 액세스 제어 목록 (ACL) 테 넌 트 수준에서 Azure Active Directory를 통해 인증 하는 id를 포함 합니다. 지정 된 테 넌 트에 대 한 사서함 해당 테 넌 트의 사용자만 포함 하는 id가 해당 테 넌 트의 인증 공급자에 대해 인증으로 제한 됩니다. TenantA에 속하는 콘텐츠 어떤 식으로도 얻을 수 없습니다 TenantB, 사용자가 명시적으로 TenantA가 승인 하지 않은 경우.

## <a name="skype-for-business"></a>비즈니스용 Skype
비즈니스를 위한 Skype에서는 다양 한 위치에서에서 데이터를 저장합니다.
- 비즈니스 데이터베이스에 대 한 다양 한 Skype에 있는 뿐만 아니라 비즈니스 Active Directory 서버에 대 한 Skype에 저장 된 사용자 및 계정 정보 연결 끝점, 테 넌 트 Id 포함 하는 다이얼 플랜, 설정, 현재 상태, 대화 상대 목록, 등 로밍 서버입니다. 대화 상대 목록은 사용 하는 경우 사용자는 두 제품 모두에 대해 또는 Skype 비즈니스 서버에 대 한 사용자가 아닌 경우 사용자의 Exchange Online 사서함에 저장 됩니다. Skype 비즈니스 데이터베이스 서버에 대 한 분할 된 당-테 넌 트, 아니지만 데이터의 다중 테 넌 트 격리 RBAC를 통해 적용 됩니다.
- 비즈니스 모임에 대 한 Skype 하는 동안 사용자가 콘텐츠를 업로드와 같은 모임 콘텐츠, 분산 파일 시스템 공유에 저장 됩니다. 보관을 사용 하도록 설정 하는 제공 Exchange Online에서이 콘텐츠를 보관할 수도 있습니다. DFS 공유를 하지 않고 분할 된 당-테 넌 트 하지만 Acl로 콘텐츠를 보호 하는 다중 테 넌 트 RBAC를 통해 적용 됩니다.
- 통화 기록, IM 세션, 응용 프로그램 공유, IM 기록, 등의 작업 기록, 통화 정보 기록 Exchange Online에 저장할 수 있지만 대부분 통화 정보 레코드는 일시적으로 통화 정보 레코드 (CDR) 서버에 저장 됩니다. 콘텐츠는 테 넌 트 당 분할 되지 않지만 다중 테 넌 트 RBAC를 통해 적용 됩니다.

## <a name="sharepoint-online"></a>SharePoint Online
여러 독립적 메커니즘은 SharePoint online 데이터 격리를 제공 하는 고유 합니다. SharePoint Online 응용 프로그램 데이터베이스 내에서 추상화 된 코드로 개체를 저장합니다. 등 SharePoint Online에 파일을 업로드 하는 사용자 때 해당 파일은 분해 하 고 응용 프로그램 코드로 변환 하 고 여러 데이터베이스에 걸쳐 여러 테이블에 저장 합니다.

사용자 데이터를 포함 하는 저장소에 직접 액세스할 수 있습니다, 콘텐츠 휴먼 또는 SharePoint Online이 아닌 모든 시스템으로 해석할 것입니다. 이러한 메커니즘 보안 액세스 제어 및 속성을 포함 합니다. 위에서 설명한 모든 SharePoint Online 리소스는 권한 부여 코드 및 RBAC 정책에는 테 넌 트 내의 포함 하 여 보안이 유지 됩니다. 자원의 보안을 유지 하는 액세스 제어 목록 (ACL) 테 넌 트 수준에서 인증 하는 id를 포함 합니다. 와 마찬가지로 Exchange Online, SharePoint Online에서 지정 된 테 넌 트에 대 한 데이터는 테 넌 트의 사용자만 포함 하는 id가 해당 테 넌 트의 인증 공급자에 대해 인증으로 제한 됩니다.

Acl을 외에도 테 넌 트 수준 (즉, 테 넌 트 관련 Azure Active Directory) 인증 공급자를 지정 하는 한번에 작성 됩니다 속성과 설정 되 면 변경할 수 없습니다. 테 넌 트에 대 한 인증 공급자 테 넌 트 속성을 설정 테 넌 트에 노출 되는 Api를 사용 하 여 변경할 수 없습니다.

각 테 넌 트에 대 한 고유 *구독 Id* 도 사용 됩니다. 모든 고객 사이트 테 넌 트 자가 소유 하며 테 넌 트를 *구독 Id* 고유한 할당 됩니다. 사이트 *구독 Id* 속성은 한번에 작성 됩니다 하 고 변경할 수 없습니다. 사이트는 테 넌 트에 할당 된, 나중에 콘텐츠 저장소 API를 사용 하 여 다른 테 넌 트를 이동할 수 없습니다. *구독 Id* 인증 공급자에 대 한 보안 범위를 만드는데 사용 되 고 테 넌 트에 연결 되는 키 이기도 합니다.

SharePoint Online 콘텐츠를 저장 하는 것에 대 한 SQL Server 및 Azure 저장소를 사용 합니다. SQL 수준에서 콘텐츠 저장소에 대 한 파티션 키 *SiteId*됩니다. SQL 쿼리를 실행 하는 경우 SharePoint Online 판명 된 *SiteId* 일부로 사용에 대 한 테 넌 트 수준의 *구독 Id* 검사 합니다.

SharePoint Online Microsoft Azure에서 파일 이진 blob (예: 파일 스트림)를 저장합니다. 각 SharePoint Online 팜에는 자체 Microsoft Azure 계정 하 고 Azure에 저장 된 모든 blob가 개별적으로 SQL 콘텐츠 저장소에 저장 된 키를 사용 하 여 암호화 됩니다. 암호화 키를 최종 사용자에 게 직접 노출 되지 않습니다 및 권한 부여 계층에서 코드에서 보호 됩니다. 마지막으로, SharePoint Online은 HTTP 요청을 읽거나 둘 이상의 테 넌 트에 대 한 데이터를 기록 하는 시점을 감지 하는 전체에서 실시간 모니터링 합니다. 액세스 되는 리소스의 *구독 Id* 에 대 한 요청 id의 *구독 Id* 를 추적 하 여 수행 합니다. 최종 사용자가 둘 이상의 테 넌 트의 리소스에 액세스 하는 요청을 실행할 수 없습니다. 발생할 수 있습니다는 다중 테 넌 트 환경에서 서비스 요청에 대 한 개별 정책을 합니다. 예, 검색 크롤러 전체 데이터베이스에 대 한 콘텐츠 변경 내용을 한번에 모든으로 끌어옵니다. 일반적으로 사이트 효율성에 대 한 작업을 수행 하는 단일 서비스 요청에 둘 이상의 테 넌 트의 쿼리 단계입니다.
