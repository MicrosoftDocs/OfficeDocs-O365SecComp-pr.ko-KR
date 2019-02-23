---
title: Office 365 Advanced eDiscovery에서 사용자 및 사례 설정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: 'Office 365 Advanced eDiscovery에서 사용자 역할을 구성 하 고 사례를 만들고 사용자를 사례에 할당 하는 방법에 대해 알아봅니다.  '
ms.openlocfilehash: f393c59a9726baa6d7423eacb33543ae7adf5065
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212992"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 사용자 및 사례 설정

이 항목에서는 Office 365 Advanced eDiscovery에 대 한 사용자 및 사례를 설정 하는 방법에 대해 설명 합니다.
  
> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="prerequisites"></a>필수 구성 요소

고급 eDiscovery에서 사례와 사용자를 설정 하기 전에 다음을 수행 해야 합니다.
  
- 고급 eDiscovery를 사용 하 여 사용자 데이터를 분석 하려면 데이터의 custodian 사용자에 게 Office 365 E5 라이선스를 할당 해야 합니다. 또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자에 게 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다. 서비스 케이스에 할당 되 고 고급 eDiscovery를 사용 하 여 데이터를 분석 하는 관리자 및 규정 준수 직원은 E5 라이선스가 필요 하지 않습니다. 
    
- ediscovery 사례를 만들고 여기에 구성원을 추가 하려면 Office 365 보안 &amp; 및 준수 센터에서 ediscovery 관리자 역할 그룹의 구성원 이어야 합니다. 보안 &amp; 및 준수 센터에서 eDiscovery 관리자 역할 그룹에 자신을 추가 하려면 Office 365 조 직의 전역 관리자 여야 합니다. 전역 관리자가 아닌 경우에는 전역 관리자에 게 사용자를 eDiscovery 관리자 역할 그룹에 추가 해 달라고 요청 해야 합니다. 자세한 내용은 다음 항목을 참조 하십시오.
    
  - [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)
    
  - [Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 권한 할당](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a>1 단계: 사용자 eDiscovery 권한 할당

첫 번째 단계는 사용자가 eDiscovery 사례의 구성원으로 추가할 수 있도록 &amp; 보안 및 준수 센터의 요구 사항 사용 권한을 할당 하는 것입니다. 보안 &amp; 및 준수 센터에서 사례 구성원으로 추가 된 사용자는 고급 eDiscovery의 사례에 액세스할 수 있습니다.
  
사용자에 게 eDiscovery 사례의 구성원으로 추가할 수 있는 필요한 권한을 할당 하려면 [Office 365 보안 &amp; 및 준수 센터의 eDiscovery 사례](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members)에서 1 단계를 참조 하십시오.
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a>2 단계: eDiscovery 사례 만들기 및 구성원 추가

다음 단계에서는 보안 &amp; 및 준수 센터에서 새 eDiscovery 사례를 만들고 구성원을 추가 합니다. 그러면 사례 구성원이 Advanced eDiscovery의 사례에 액세스할 수 있게 됩니다.
  
1. 새 eDiscovery 사례를 만들려면 [Office 365 보안 &amp; 및 준수 센터의 eDiscovery 사례](ediscovery-cases.md#step-2-create-a-new-case)에서 2 단계를 참조 하십시오.
    
2. ediscovery 사례에 구성원을 추가 하려면 [Office 365 보안 &amp; 및 준수 센터의 eDiscovery 사례](ediscovery-cases.md#step-3-add-members-to-a-case) 에서 3 단계를 참조 하세요.
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a>3 단계: Advanced eDiscovery에서 사례 이동

eDiscovery 사례를 만들고 구성원을 추가 하 고 나면 사용자 (또는 사례 구성원)가 Advanced eDiscovery의 해당 사례에 액세스할 수 있습니다. Advanced eDiscovery의 사례에 액세스 하려면 [Office 365 보안 &amp; 및 준수 센터의 eDiscovery 사례](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery)에서 8 단계를 참조 하세요.
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[데이터 준비](prepare-data-for-advanced-ediscovery.md)
 