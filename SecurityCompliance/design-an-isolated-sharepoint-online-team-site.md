---
title: 격리된 SharePoint Online 팀 사이트 디자인
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: '요약: 격리 된 SharePoint Online 팀 사이트에 대 한 디자인 프로세스를 단계별로 안내 합니다.'
ms.openlocfilehash: 09748fcc22a4a48efc4346ff75a225db612a0ef4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257184"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a>격리된 SharePoint Online 팀 사이트 디자인

 **요약:** 격리 된 SharePoint Online 팀 사이트에 대 한 디자인 프로세스를 단계별로 안내 합니다.
  
이 문서에서는 격리 된 SharePoint Online 팀 사이트를 만들기 전에 수행 해야 하는 주요 디자인 결정 사항에 대해 설명 합니다.
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a>1 단계: SharePoint 그룹 및 권한 수준 결정

모든 sharepoint Online 팀 사이트는 기본적으로 다음과 같은 SharePoint 그룹을 사용 하 여 만들어집니다.
  
- \<사이트 name> 구성원
    
- \<사이트 name> 방문자
    
- \<사이트 name> 소유자
    
이러한 그룹은 Office 365 및 Azure Active Directory (AD) 그룹과는 별개 이며 사이트의 리소스에 대 한 사용 권한을 할당 하기 위한 기본이 됩니다.
  
SharePoint 그룹의 구성원이 사이트에서 수행할 수 있는 작업을 결정 하는 특정 사용 권한 집합은 사용 권한 수준입니다. SharePoint Online 팀 사이트에 대 한 세 가지 사용 권한 수준에는 기본적으로 편집, 읽기 및 모든 권한이 있습니다. 다음 표에서는 SharePoint 그룹 및 할당 된 사용 권한 수준에 대 한 기본 상관 관계를 보여 줍니다.
  
|**SharePoint 그룹**|**권한 수준**|
|:-----|:-----|
|\<사이트 name> 구성원  <br/> |편집  <br/> |
|\<사이트 name> 방문자  <br/> |읽기  <br/> |
|\<사이트 name> 소유자  <br/> |모든 권한  <br/> |
   
 **모범 사례:** 추가 SharePoint 그룹 및 권한 수준을 만들 수 있습니다. 그러나 격리 된 sharepoint Online 사이트에 대 한 기본 sharepoint 그룹 및 사용 권한 수준을 사용 하는 것이 좋습니다.
  
다음은 기본 SharePoint 그룹 및 사용 권한 수준입니다.
  
![sharepoint Online 사이트에 대 한 기본 sharepoint 그룹 및 사용 권한 수준입니다.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a>2 단계: 액세스 그룹을 사용 하 여 사용자에 게 사용 권한 할당

사용자 계정이 구성원으로 속해 있는 Office 365 또는 Azure AD 그룹을 SharePoint 그룹에 추가 하는 방식으로 사용자에 게 사용 권한을 할당할 수 있습니다. office 365 또는 Azure AD 그룹의 멤버 자격을 통해 직접 또는 간접적으로 office 365 사용자 계정을 추가한 후에는 SharePoint 그룹과 연결 된 사용 권한 수준에 할당 됩니다.
  
기본 SharePoint 그룹을 예로 사용 합니다.
  
- 사용자 계정 및 그룹을 모두 포함할 수 있는 ** \<site name> members** SharePoint 그룹의 구성원에 게는 **편집** 권한 수준이 할당 됩니다.
    
- 사용자 계정 및 그룹을 모두 포함할 수 있는 ** \<사이트 name> 방문자** SharePoint 그룹의 구성원에 게는 **읽기** 권한 수준이 할당 됩니다.
    
- 사용자 계정 및 그룹을 모두 포함할 수 있는 ** \<site name>** owner SharePoint 그룹의 구성원에 게는 **모든** 권한 수준이 할당 됩니다.
    
 **모범 사례:** 개별 사용자 계정을 통해 사용 권한을 관리할 수는 있지만 대신 액세스 그룹 이라고 하는 단일 Azure AD 그룹을 사용 하는 것이 좋습니다. 이를 통해 각 SharePoint 그룹의 사용자 계정 목록을 관리 하는 것이 아니라 액세스 그룹의 구성원을 통해 사용 권한을 쉽게 관리할 수 있습니다.
  
office 365의 Azure AD 그룹은 office 365 그룹과는 다릅니다. Azure AD 그룹은 해당 **유형이** **보안** 으로 설정 되 고 전자 메일 주소가 없는 Office 관리 센터에 표시 됩니다. Azure AD 그룹은 다음 내에서 관리할 수 있습니다.
  
- Windows Server Active Directory (AD)
    
    온-프레미스 Windows Server AD 인프라에 만들어져 Office 365 구독과 동기화 된 그룹입니다. Office 관리 센터에서 이러한 그룹의 **상태** 는 **active directory와 동기화**되어 있습니다.
    
- Office 365
    
    Office 관리 센터, Azure portal 또는 Microsoft PowerShell 중 하나를 사용 하 여 만든 그룹입니다. Office 관리 센터에서 이러한 그룹의 **상태** 는 **Cloud**입니다.
    
 **모범 사례:** windows server ad 온-프레미스를 사용 중이 고 Office 365 구독과 동기화 하는 경우 windows server ad에서 사용자 및 그룹 관리를 수행 합니다.
  
격리 된 SharePoint Online 팀 사이트의 경우 권장 되는 그룹 구조는 다음과 같습니다.
  
|**SharePoint 그룹**|**Azure AD 기반 액세스 그룹**|**권한 수준**|
|:-----|:-----|:-----|
|\<사이트 name> 구성원  <br/> |\<사이트 name> 구성원  <br/> |편집  <br/> |
|\<사이트 name> 방문자  <br/> |\<사이트 name> 뷰어  <br/> |읽기  <br/> |
|\<사이트 name> 소유자  <br/> |\<사이트 name> 관리자  <br/> |모든 권한  <br/> |
   
 **모범 사례:** Office 365 또는 Azure AD 그룹을 SharePoint 그룹의 구성원으로 사용할 수는 있지만 azure ad 그룹을 사용 하는 것이 좋습니다. Windows Server AD 또는 Office 365를 통해 관리 되는 Azure AD 그룹은 중첩 된 그룹을 보다 유연 하 게 사용 하 여 사용 권한을 할당할 수 있습니다.
  
Azure AD 기반 액세스 그룹을 사용 하도록 구성 된 기본 SharePoint 그룹은 다음과 같습니다.
  
![access 그룹을 기본 SharePoint Online 사이트 그룹의 구성원으로 사용 합니다.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
세 개의 액세스 그룹을 디자인할 때는 다음 사항을 염두에 두어야 합니다.
  
- 팀 사이트를 관리 하는 소수의 SharePoint Online 관리자에 게 해당 하는 ** \<사이트 name> Admins** 액세스 그룹의 구성원은 몇 명만 있어야 합니다.
    
- 대부분의 사이트 구성원은 ** \<사이트 name> members** 또는 ** \<site name> viewer** 액세스 그룹에 있습니다. site ** \<name> members** 액세스 그룹의 사이트 구성원은 사이트의 리소스를 삭제 하거나 수정할 수 있기 때문에 멤버 자격을 신중 하 게 고려해 야 합니다. 확실 하지 않은 경우 사이트 구성원을 ** \<사이트 name> viewer** 액세스 그룹에 추가 합니다.
    
다음은 projectx 라는 격리 된 사이트에 대 한 SharePoint 그룹 및 액세스 그룹의 예입니다.
  
![projectx 라는 SharePoint Online 사이트에 대 한 액세스 그룹을 사용 하는 방법의 예입니다.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a>3 단계: 중첩 된 Azure AD 그룹 사용

소수의 사용자로 한정 된 프로젝트의 경우 사이트의 SharePoint 그룹에 추가 되는 단일 수준의 Azure AD 기반 액세스 그룹이 대부분의 시나리오에 적합 합니다. 그러나 사용자 수가 많고 해당 사용자가 이미 설정 된 Azure AD 그룹의 구성원 인 경우에는 중첩 그룹 또는 다른 그룹을 구성원으로 포함 하는 그룹을 사용 하 여 SharePoint 권한을 보다 쉽게 할당할 수 있습니다.
  
예를 들어 영업, 마케팅, 엔지니어링, 법률 및 지원 부서의 임원 및 해당 부서에서 임원 사용자 계정을 사용 하는 자체 그룹을 공동 작업용으로 사용할 수 있도록 격리 된 SharePoint online 팀 사이트를 만들려고 합니다. 멤버 자격. 새 사이트 구성원에 대해 새 그룹을 만들고 모든 개별 executive 사용자 계정을 배치 하는 것이 아니라 새 그룹의 각 부서에 대 한 기존 임원 그룹을 배치 합니다.
  
 여러 조직 간에 Office 365 구독을 공유 하는 경우 사용자 계정 수가 많기 때문에 조직에 대해 격리 된 사이트에 대 한 단일 그룹 구성원 자격이 관리 하기가 어려울 수 있습니다. 이 경우 조직 내에서 그룹을 포함 하는 각 조직에 대해 중첩 된 Azure AD 그룹을 사용 하 여 사용 권한을 관리할 수 있습니다.
  
중첩 된 Azure AD 그룹을 사용 하려면:
  
1. 사용자 계정을 포함 하는 Azure AD 그룹을 식별 하거나 만들고 해당 사용자 계정을 구성원으로 추가 합니다.
    
2. 다른 azure ad 그룹을 포함 하는 컨테이너 Azure ad 기반 액세스 그룹을 만들고 해당 그룹을 구성원으로 추가 합니다.
    
3.  컨테이너 액세스 그룹에 대 한 적절 한 액세스 수준에 대해 SharePoint 그룹 및 해당 권한 수준을 식별 합니다.
    
> [!NOTE]
> 중첩 된 Office 365 그룹은 사용할 수 없습니다. 
  
다음은 projectx 구성원 액세스 그룹에 대 한 중첩 된 Azure AD 그룹의 예입니다.
  
![projectx 사이트의 구성원 액세스 그룹에 대해 중첩 된 액세스 그룹을 사용 하는 방법의 예입니다.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
연구, 엔지니어링 및 프로젝트 리더 팀의 모든 사용자 계정이 사이트 구성원 이므로 Azure AD 그룹을 projectx members access 그룹에 추가 하는 것이 더 쉽습니다.
  
## <a name="next-step"></a>다음 단계

격리 된 사이트를 만들고 프로덕션 환경에 구성할 준비가 되 면 [격리 SharePoint Online 팀 사이트 배포](deploy-an-isolated-sharepoint-online-team-site.md)를 참조 하세요.
  
## <a name="see-also"></a>참고 항목

[격리된 SharePoint Online 팀 사이트](isolated-sharepoint-online-team-sites.md)
  
[격리된 SharePoint Online 팀 사이트 관리](manage-an-isolated-sharepoint-online-team-site.md)

[격리된 SharePoint Online 팀 사이트 배포](deploy-an-isolated-sharepoint-online-team-site.md)



