---
title: Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AdminRoleGroups
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: d10608af-7934-490a-818e-e68f17d0e9c1
description: Office 365 보안 &amp; 준수 센터에서는 장치 관리, 데이터 손실 방지, eDiscovery, 보존 및 등과 같은 준수 작업을 수행 하는 사람에 게 권한을 부여할 수 있습니다. 이 사용자 들이 명시적으로 권한을 부여 하면에 액세스할 수 있는 작업만 수행할 수 있습니다. 보안에 액세스 하려면 &amp; 준수 센터, 사용자가 Office 365 전역 관리자 또는 하나 이상의 보안의 구성원 일 필요가 &amp; 준수 센터 역할 그룹입니다.
ms.openlocfilehash: e393bad7c3a57b0734835e56fcd781cc31327c18
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013432"
---
# <a name="permissions-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터

Office 365 보안 &amp; 준수 센터에서는 장치 관리, 데이터 손실 방지, eDiscovery, 보존 및 등과 같은 준수 작업을 수행 하는 사람에 게 권한을 부여할 수 있습니다. 이 사용자 들이 명시적으로 권한을 부여 하면에 액세스할 수 있는 작업만 수행할 수 있습니다. 보안에 액세스 하려면 &amp; 준수 센터, 사용자가 Office 365 전역 관리자 또는 하나 이상의 보안의 구성원 일 필요가 &amp; 준수 센터 역할 그룹입니다.
  
보안에 대 한 사용 권한을 &amp; 준수 센터에 대 한 액세스 제어 RBAC (역할 기반) 사용 권한 모델에 기반 합니다. 이것은 Exchange에서 사용 되는 동일한 사용 권한 모델 Exchange에 익숙한 경우 보안에 대 한 사용 권한을 부여 하므로 &amp; 준수 센터와 매우 유사 됩니다. 단, 해당 Exchange 역할을 고려해 야 그룹 및 보안 &amp; 준수 센터 역할 그룹 멤버 자격 또는 사용 권한 공유 하지 않습니다. 조직 관리 역할 그룹에 있는 모두 하는 동안 아니더라도 동일 합니다. 사용 권한을 부여 하 고 역할 그룹의 구성원은 서로 다릅니다. 보안 목록은 &amp; 아래 준수 센터 역할 그룹입니다.
  
![Office 365 보안의 사용 권한 페이지 &amp; 준수 센터](media/992c20ca-e82e-497c-9c8d-6fab212deb80.png)
  
## <a name="relationship-of-members-roles-and-role-groups"></a>구성원, 역할 및 역할 그룹의 관계

**역할**은 특정 작업 집합을 수행하기 위한 권한을 부여합니다. 예를 들어 사례 관리 역할은 eDiscovery 사례를 사용할 수 있도록 합니다. 
  
**역할 그룹** 집합을 역할의 보안을 통해 자신의 작업을 수행 하는 사람들은 &amp; 준수 센터; 예, 규정 준수 관리자 역할 그룹을 해당 작업을 수행 하기 위해 해당 작업에 대 한 사용 권한을 사용자에 게는 규정 준수 관리 필요 하므로 역할 사례 관리, 콘텐츠 검색 및 조직 구성 (및 다른 사용자에 게)에 대 한 포함 합니다. 
  
보안 &amp; 준수 센터는 가장 일반적인 작업 및 사용자를 할당 해야 하는 함수에 대 한 기본 역할 그룹을 포함 합니다. 단순히 기본 역할 그룹에 **구성원** 으로 개별 사용자를 추가 하는 것이 좋습니다. 
  
![역할 그룹에 역할 및 멤버의 관계를 보여 주는 다이어그램](media/2a16d200-968c-4755-98ec-f1862d58cb8b.png)
  
편집 하거나 기존 역할 그룹을 삭제할 수 있지만 하지 것이 좋습니다. 기본 역할 그룹을 편집 하는 대신 복사, 수정 및 다음 다른 이름으로 저장 수 있습니다.
  
## <a name="permissions-needed-to-use-features-in-the-security-amp-compliance-center"></a>보안에서 기능을 사용 하 여 필요한 사용 권한 &amp; 준수 센터

다음 표에서 보안에서 사용할 수 있는 기본 역할 그룹을 나열 &amp; 준수 센터입니다. 적절 한 보안 추가 규정 준수 작업을 수행 하려면 사용자에 게 권한을 부여 하려면 &amp; 준수 센터 역할 그룹입니다.
  
보안에 대 한 사용 권한 관리 &amp; 준수 센터만 액세스할 수 있게 보안 내에서 사용할 수 있는 규정 준수 기능을 &amp; 자체 규정 준수 센터입니다. 보안에서 되지 않은 다른 규정 준수 기능에 사용 권한을 부여 하려면 &amp; Exchange 전송 규칙 등의 준수 센터 Exchange 관리 센터를 사용 해야 합니다.
  
보안에 대 한 액세스 권한을 부여 하는 방법을 보려면 &amp; 준수 센터, [Office 365 규정 준수 관리 센터에 대 한 사용자 액세스를 제공](grant-access-to-the-security-and-compliance-center.md)하는 작업을 체크아웃 합니다.
  
|**역할 그룹**|**설명**|
|:-----|:-----|
|**규정 준수 관리자** <sup>1</sup> <br/> |구성원 장치 관리, 데이터 손실 방지, 보고서 및 보존에 대 한 설정을 관리할 수 있습니다.  <br/> |
|**eDiscovery 관리자** <br/> | 구성원은 사서함, SharePoint Online 사이트 및 비즈니스용 OneDrive 위치에서 검색을 수행하고 원본 위치를 유지할 수 있습니다. 또한 구성원은 eDiscovery 사례를 만들고 관리하고, 사례에서 구성원을 추가 및 제거하고, 사례와 연결된 콘텐츠 검색을 만들고 편집할 수 있습니다. <br/>  eDiscovery 관리자는 추가 사용 권한이 할당된 eDiscovery 관리자 역할 그룹의 구성원입니다. eDiscovery 관리자는 다음 작업을 수행할 수 있습니다.<br/>  조직의 모든 eDiscovery 사례를 봅니다.  <br/>  본인을 사례의 구성원으로 추가한 후에 eDiscovery 사례를 관리합니다.  <br/>  Office 365 고급 eDiscovery를 액세스 합니다. 즉, eDiscovery 관리자 고급 eDiscovery의 관리자로 자동으로 추가 됩니다. 참고 eDiscovery 보안에서 관리자를 사용할 필요가 &amp; 준수 센터 고급 eDiscovery 액세스할 수 있습니다. EDiscovery 관리자가 사용자를 요청 하는 방법에 대 한 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사례 &amp; 준수 센터](https://go.microsoft.com/fwlink/p/?LinkId=780738)합니다.<br/> 고급 eDiscovery의 사용자 관리 권한을 부여 하지만 보안에서 eDiscovery 관리자를 확인 하지 않으려고 하려는 경우 &amp; 준수 센터 있습니다 수 eDiscovery 관리자 역할 그룹에 추가 하 고 다음에 대 한 관리자로 추가할 고급 eDiscovery 합니다. 자세한 내용은 [사용자 및 Office 365 고급 ediscovery에서 사례에 대 한 설정](https://go.microsoft.com/fwlink/p/?LinkId=780696)을 참조 하십시오.           |
|**조직 관리** <sup>1</sup> <br/> |구성원의 보안 기능에 액세스할 수 있도록 사용 권한을 제어할 수 &amp; 준수 센터도 장치 관리, 데이터 손실 방지, 보고서 및 보존에 대 한 설정을 관리 하 고 있습니다.  <br/> Office 365에 대 한 MDM 하 여 관리 되는 장치 목록을 보려면 전역 관리자가 아닌 사용자에 대 한 순서 대로 사항에 유의 하 고 이러한 장치에서 작업을 수행할 MDM에서 Office 365에 대 한 장치를 회수, 예: 사용자는 Exchange 관리자 여야 합니다.  <br/> Office 365 전역 관리자는이 역할 그룹의 구성원으로 자동으로 추가 됩니다.           |
|**Records Management** <br/> |구성원을 관리 하 고 레코드 콘텐츠를 삭제할 수 있습니다.  <br/> |
|**Reviewer** <br/> |구성원 보안에서 eDiscovery의 경우 페이지의 경우 목록을 볼 수 &amp; 준수 센터입니다. 자신이 만들거나 수 없습니다, 열기, eDiscovery 사례 관리 합니다. 이 역할 그룹의 주요 목적은 구성원이 보기 및 액세스를 허용 하는 경우 고급 eDiscovery의 데이터입니다.  <br/> 이 역할 그룹은 가장 제한적인 eDiscovery 관련 사용 권한을 갖습니다.  <br/> |
|**보안 관리자** <br/> |이 역할 그룹의 구성원 이어야 서비스 간에 동기화 되며 중앙에서 관리 됩니다. 이 역할 그룹은 관리자가 포털을 통해 관리가 용이 아닙니다. 이 역할 그룹의 구성원 간 서비스 관리자가 외부 파트너 그룹 및 Microsoft 기술 지원 서비스에 포함 될 수 있습니다. 기본적으로이 그룹 수 할당 되지 모든 역할입니다. 그러나 보안 관리자 역할 그룹의 구성원 이어야 합니다 하 고 해당 역할 그룹의 기능을 상속 합니다.  <br/> 모든 보안 독자 역할와 다양 한 동일한 서비스에 대 한 추가 관리 권한 읽기 전용 권한을: Azure 정보 보호, Identity 보호 센터, 권한이 부여 된 Id 관리, 모니터링 Office 365 서비스 상태 및 Office 365 보안 &amp; 준수 센터입니다.  <br/> |
|**보안 읽기 권한자** <br/> |구성원에 게 다양 한 Identity 보호 센터, 권한이 부여 된 Id 관리, Office 365 서비스 상태를 모니터링, 및 Office 365 보안의 보안 기능에 대 한 읽기 전용 액세스 &amp; 준수 센터입니다.  <br/> 이 역할 그룹의 구성원 이어야 서비스 간에 동기화 되며 중앙에서 관리 됩니다. 이 역할 그룹은 관리자가 포털을 통해 관리가 용이 아닙니다. 이 역할 그룹의 구성원 간 서비스 관리자가 외부 파트너 그룹 및 Microsoft 기술 지원 서비스에 포함 될 수 있습니다. 기본적으로이 그룹 수 할당 되지 모든 역할입니다. 그러나 보안 판독기 역할 그룹의 구성원 수 및 해당 역할 그룹의 기능을 상속 합니다.  <br/> |
|**서비스 보증 사용자** <br/> |구성원 Office 365 보안에서 서비스 보증 섹션에 액세스할 수 &amp; 준수 센터입니다. 서비스 보증 보고서 및 Office 365에 저장 된 고객 데이터에 대 한 Microsoft의 보안 사례를 설명 하는 문서를 제공 합니다. 또한 Office 365에 독립적으로 제 3 자 감사 보고서를 제공 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 보증 서비스 &amp; 준수 센터](http://go.microsoft.com/fwlink/p/?LinkID=717765)합니다.<br/> |
|**감독 검토** <br/> |구성원 만들고 정의 하는 정책을 관리할 수 통신은 조직에서 검토에 따라 달라 집니다. 자세한 내용은 [Configure 감독 검토 하면 조직에 대 한 정책을](configure-supervision-policies.md)참조 하십시오.<br/> |
   
> [!NOTE]
> <sup>1</sup> 이 역할 그룹 하지 구성원 할당 Office 365 감사 로그를 검색 하거나 DLP 또는 ATP 보고서와 같은 Exchange 데이터를 포함할 수 있는 모든 보고서를 사용 하 여 필요한 사용 권한입니다. 감사 로그를 검색 하거나 모든 보고서를 보려면 사용자가 Exchange Online의 사용 권한을 할당 받아야 합니다. 감사 로그를 검색 하는 데 사용 하는 원본으로 사용 cmdlet은 Exchange Online cmdlet 때문입니다. Office 365 전역 관리자 감사 로그를 검색 하 고 자동으로 추가 조직 관리 역할 그룹의 구성원으로 Exchange Online 때문에 모든 보고서를 볼 수 있습니다. 자세한 내용은 참조 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](https://go.microsoft.com/fwlink/p/?LinkID=708432)합니다. 
  

