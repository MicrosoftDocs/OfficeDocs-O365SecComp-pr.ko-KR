---
title: Office 365 보안 &amp; 및 준수 센터의 사용 권한
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AdminRoleGroups
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d10608af-7934-490a-818e-e68f17d0e9c1
description: Office 365 보안 &amp; 및 준수 센터를 사용 하면 장치 관리, 데이터 손실 방지, eDiscovery, 보존 등의 규정 준수 작업을 수행 하는 사용자에 게 사용 권한을 부여할 수 있습니다. 이러한 사용자는 자신에 게 명시적으로 액세스 권한을 부여 하는 작업만 수행할 수 있습니다. 보안 &amp; 및 준수 센터에 액세스 하려면 사용자가 Office 365 전역 관리자 이거나 하나 이상의 보안 &amp; 준수 센터 역할 그룹의 구성원 이어야 합니다.
ms.openlocfilehash: e935c71f9324dbce8e0b359bfe723b93ff500b0a
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341359"
---
# <a name="permissions-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안 &amp; 및 준수 센터의 사용 권한

Office 365 보안 &amp; 및 준수 센터를 사용 하면 장치 관리, 데이터 손실 방지, eDiscovery, 보존 등의 규정 준수 작업을 수행 하는 사용자에 게 사용 권한을 부여할 수 있습니다. 이러한 사용자는 자신에 게 명시적으로 액세스 권한을 부여 하는 작업만 수행할 수 있습니다. 보안 &amp; 및 준수 센터에 액세스 하려면 사용자가 Office 365 전역 관리자 이거나 하나 이상의 보안 &amp; 준수 센터 역할 그룹의 구성원 이어야 합니다.
  
보안 &amp; 및 준수 센터의 사용 권한은 RBAC (역할 기반 액세스 제어) 권한 모델을 기반으로 합니다. 이는 exchange에 사용 되는 것과 동일한 사용 권한 모델로, exchange에 익숙한 경우 보안 &amp; 및 준수 센터에서 사용 권한을 부여 하는 것은 매우 유사 합니다. 그러나 Exchange 역할 그룹과 보안 &amp; 준수 센터 역할 그룹은 구성원 또는 사용 권한을 공유 하지 않는다는 점에 유의 해야 합니다. 둘 다 조직 관리 역할 그룹을 갖는 동시에 동일 하지는 않습니다. 사용자가 부여 하는 사용 권한 및 역할 그룹의 구성원은 서로 다릅니다. 아래에는 보안 &amp; 및 준수 센터 역할 그룹의 목록이 있습니다.
  
![Office 365 보안 &amp; 및 준수 센터의 사용 권한 페이지](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>구성원, 역할 및 역할 그룹의 관계

**역할**은 특정 작업 집합을 수행하기 위한 권한을 부여합니다. 예를 들어 사례 관리 역할은 eDiscovery 사례를 사용할 수 있도록 합니다. 
  
**역할 그룹** 은 사용자가 보안 &amp; 및 준수 센터에서 작업을 수행할 수 있도록 하는 역할 집합입니다. 예를 들어 준수 관리자 역할 그룹에는 대/소문자 관리, 콘텐츠 검색 및 조직 구성에 대 한 역할 (다른 사용자가 포함)이 있는데,이 관리자에 게는 해당 작업에 대 한 사용 권한이 있어야 작업을 수행할 수 있습니다. 
  
보안 &amp; 및 준수 센터에는 사용자를 할당 하는 데 필요한 가장 일반적인 작업 및 기능에 대 한 기본 역할 그룹이 포함 되어 있습니다. 개별 사용자를 기본 역할 그룹에 **구성원** 으로 추가 하는 것이 좋습니다. 
  
![역할 그룹에 역할 및 멤버의 관계를 보여 주는 다이어그램](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
기존 역할 그룹을 편집 하거나 삭제할 수는 있지만이 방법을 권장 하지는 않습니다. 기본 역할 그룹을 편집 하는 대신 복사 하 여 수정한 후 다른 이름으로 저장할 수 있습니다.
  
## <a name="permissions-needed-to-use-features-in-the-security-amp-compliance-center"></a>보안 &amp; 및 준수 센터에서 기능을 사용 하는 데 필요한 사용 권한

다음 표에서는 보안 &amp; 및 준수 센터에서 사용할 수 있는 기본 역할 그룹을 보여 줍니다. 준수 작업을 수행할 수 있는 권한을 사용자에 게 부여 하려면 해당 보안 &amp; 및 준수 센터 역할 그룹에 추가 합니다.
  
보안 &amp; 및 준수 센터에서 사용 권한을 관리 하면 보안 &amp; 및 준수 센터 자체 내에서 사용할 수 있는 준수 기능에 대 한 액세스 권한만 제공 됩니다. exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)과 같이 보안 &amp; 및 준수 센터에 없는 다른 규정 준수 기능에 대 한 사용 권한을 부여 하려는 경우 exchange 관리 센터를 사용 해야 합니다.
  
보안 &amp; 및 준수 센터에 대 한 액세스 권한을 부여 하는 방법을 확인 하려면 [사용자에 게 Office 365 준수 관리 센터에](grant-access-to-the-security-and-compliance-center.md)대 한 액세스 권한 부여를 참조 하세요.
  
|**역할 그룹**|**설명**|
|:-----|:-----|
|**준수 관리자** <sup>1</sup> <br/> |구성원은 장치 관리, 데이터 손실 방지, 보고서 및 보존에 대 한 설정을 관리할 수 있습니다.  <br/> |
|**eDiscovery 관리자** <br/> | 구성원은 검색을 수행 하 고 사서함, SharePoint Online 사이트 및 비즈니스용 OneDrive 위치에 보관할 수 있습니다. 또한 구성원은 eDiscovery 사례를 만들고 관리 하 고, 사례에 구성원을 추가 및 제거 하 고, 사례와 연결 된 콘텐츠 검색을 만들고 편집 하 고, Office 365 Advanced eDiscovery에서 사례 데이터에 액세스할 수 있습니다.<br/><br/>ediscovery 관리자는 추가 권한이 할당 된 ediscovery 관리자 역할 그룹의 구성원입니다. ediscovery 관리자가 수행할 수 있는 작업 외에 다음과 같은 방법을 사용할 수 있습니다.<br/><br/>  • 조직의 모든 eDiscovery 사례를 봅니다.  <br/>  • 사례를 대/소문자 구성원으로 추가한 후 eDiscovery 사례를 관리 합니다.  <br/><br/>ediscovery 관리자와 ediscovery 관리자의 주요 차이점은 ediscovery 관리자가 보안 &amp; 및 준수 센터의 **ediscovery 사례** 페이지에 나열 된 모든 경우에 액세스할 수 있다는 것입니다. eDiscovery 관리자는 자신이 만들었거나 사례를 구성원으로 사용 하는 경우에만 액세스할 수 있습니다.  사용자를 eDiscovery 관리자로 설정 하는 방법에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 ediscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.<br/>           |
|**조직 관리** <sup>1</sup> <br/> |구성원은 보안 &amp; 및 준수 센터의 기능에 액세스 하기 위한 권한을 제어 하 고 장치 관리, 데이터 손실 방지, 보고서 및 보존에 대 한 설정도 관리할 수 있습니다.  <br/> 전역 관리자가 아닌 사용자가 office * 용 mdm에서 관리 되는 장치 목록을 확인 하 고 이러한 장치에 대 한 작업을 수행 하는 경우 (예: office 365 용 mdm에서 장치를 사용 하지 않도록 설정한 경우) 사용자는 Exchange 관리자 여야 합니다.  <br/> Office 365 전역 관리자는이 역할 그룹의 구성원으로 자동 추가 됩니다.           |
|**Records Management** <br/> |구성원은 레코드 콘텐츠를 관리 하 고 삭제할 수 있습니다.  <br/> |
|**Reviewer** <br/> |구성원은 보안 &amp; 및 준수 센터의 eDiscovery 사례 페이지에 있는 사례 목록만 볼 수 있습니다. eDiscovery 사례를 만들거나 열거나 관리할 수는 없습니다. 이 역할 그룹의 기본 목적은 구성원이 고급 eDiscovery에서 사례 데이터를 보고 액세스 하도록 허용 하는 것입니다.  <br/> 이 역할 그룹은 가장 제한적인 eDiscovery 관련 사용 권한을 갖습니다.  <br/> |
|**보안 관리자** <br/> |이 역할 그룹의 구성원은 외부 파트너 그룹 및 Microsoft 지원 뿐만 아니라 서비스 간 관리자도 포함할 수 있습니다. 기본적으로이 그룹에는 역할이 할당 되지 않을 수 있습니다. 그러나 Azure Active Directory에서 보안 관리자 역할의 구성원이 되며 해당 역할의 기능이 상속 됩니다. 중앙에서 사용 권한을 관리 하려면 azure active directory 관리 센터에서이 역할을 변경 합니다-자세한 내용은 [azure active directory의 관리자 역할 사용 권한을](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)참조 하세요. 보안 & 준수 센터에서이 역할 그룹을 편집 하는 경우 이러한 변경 내용은 보안 & 준수 센터에만 적용 되 고 다른 서비스는 변경 되지 않지만, Azure Active Directory 관리 센터에서 변경한 내용은 모든 서비스에 영향을 줍니다.<br/> 보안 독자 역할의 모든 읽기 전용 권한 및 같은 서비스에 대 한 다양 한 추가 관리 권한 (Azure Information protection, id 보호 센터, 권한이 부여 된 id 관리, Office 365 서비스 모니터링) 상태 및 Office 365 보안 &amp; 및 준수 센터  <br/> |
|**보안 독자** <br/> |구성원에 게는 id 보호 센터의 여러 보안 기능, 권한이 부여 된 id 관리, office 365 서비스 상태 모니터링 및 office 365 보안 &amp; 준수 센터에 대 한 읽기 전용 액세스 권한이 있습니다.  <br/> 이 역할 그룹의 구성원은 서비스 간에 동기화 되 고 중앙에서 관리 됩니다. 이 역할 그룹의 구성원은 외부 파트너 그룹 및 Microsoft 지원 뿐만 아니라 서비스 간 관리자도 포함할 수 있습니다. 기본적으로이 그룹에는 역할이 할당 되지 않을 수 있습니다. 그러나 Azure Active Directory에서 보안 독자 역할의 구성원이 되며 해당 역할의 기능이 상속 됩니다. 중앙에서 사용 권한을 관리 하려면 azure active directory 관리 센터에서이 역할을 변경 합니다-자세한 내용은 [azure active directory의 관리자 역할 사용 권한을](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)참조 하세요. 보안 & 준수 센터에서이 역할 그룹을 편집 하는 경우 이러한 변경 내용은 보안 & 준수 센터에만 적용 되 고 다른 서비스는 변경 되지 않지만, Azure Active Directory 관리 센터에서 변경한 내용은 모든 서비스에 영향을 줍니다.<br/> |
|**서비스 보증 사용자** <br/> |구성원은 Office 365 보안 &amp; 및 준수 센터의 서비스 보증 섹션에 액세스할 수 있습니다. 서비스 보증은 Office 365에 저장 된 고객 데이터에 대 한 Microsoft의 보안 방법을 설명 하는 보고서와 문서를 제공 합니다. 또한 Office 365에 대 한 독립 타사 감사 보고서도 제공 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 서비스 보증](http://go.microsoft.com/fwlink/p/?LinkID=717765)를 참조 하세요.<br/> |
|**관리 검토** <br/> |구성원은 조직에서 검토할 대상이 되는 통신을 정의 하는 정책을 만들고 관리할 수 있습니다. 자세한 내용은 [Configure 관리 review 정책도 조직에 대해](configure-supervision-policies.md)참조 하십시오.<br/> |
   
> [!NOTE]
> <sup>1</sup> 이 역할 그룹은 Office 365 감사 로그를 검색 하는 데 필요한 사용 권한을 구성원에 게 할당 하지 않으며 DLP 또는 ATP 보고서와 같은 Exchange 데이터를 포함할 수 있는 모든 보고서를 사용 합니다. 감사 로그를 검색 하거나 모든 보고서를 보려면 Exchange Online에서 사용자에 게 사용 권한을 할당 해야 합니다. 이는 감사 로그를 검색 하는 데 사용 되는 기본 cmdlet이 Exchange Online cmdlet 이기 때문입니다. Office 365 전역 관리자는 감사 로그를 검색 하 고 Exchange Online에서 조직 관리 역할 그룹의 구성원으로 자동 추가 되므로 모든 보고서를 볼 수 있습니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색](https://go.microsoft.com/fwlink/p/?LinkID=708432)을 참조 하세요. 
  

