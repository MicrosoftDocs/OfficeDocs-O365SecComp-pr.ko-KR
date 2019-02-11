---
title: Office 365 Advanced eDiscovery에서 사용자 및 사례 설정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: '사용자 역할 구성의 경우 만들고 Office 365 고급 ediscovery에서 사례에 사용자를 할당 하는 방법에 알아봅니다.  '
ms.openlocfilehash: 4c0043b7651cc82272492e19faf01041c6f67932
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559061"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 사용자 및 사례 설정

이 항목에서는 사용자와 Office 365 고급 ediscovery 사례를 설정 하는 방법에 설명 합니다.
  
> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="prerequisites"></a>필수 구성 요소

사례 및 고급 eDiscovery의 사용자를 설정 하기 전에 다음이 필요 합니다.
  
- 고급 eDiscovery를 사용 하 여 사용자의 데이터를 분석 하려면 (데이터의 더불어) 사용자는 Office 365 E5 라이선스를 할당 합니다. 또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자의 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다. 관리자 및 규정 준수 관리자의 경우에 할당 된 및 고급 eDiscovery를 사용 하 여 데이터를 분석 하 게 e 5 라이선스가 필요는 없습니다. 
    
- Office 365 보안에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하는 &amp; 준수 센터를 eDiscovery 사례를 만들고에 구성원을 추가 합니다. 보안에 사용자가 직접 eDiscovery 관리자 역할 그룹에 추가 하려면 &amp; 준수 센터 해야 Office 365 조직에서 전역 관리자 여야 합니다. 전역 관리자를 모르는 경우를 eDiscovery 관리자 역할 그룹에 추가 하면 전역 관리자에 게 문의 해야 합니다. 자세한 내용은 다음을 참조 합니다.
    
  - [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)
    
  - [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a>1 단계: 사용자를 eDiscovery 사용 권한 할당

첫번째 단계는 사용자의 보안 요구 사항 사용 권한을 할당 하는 &amp; 준수 센터 eDiscovery 사례의 구성원으로 추가 나에 게 수 있도록 합니다. 사용자는 보안의 경우의 구성원으로 추가 된 후 &amp; 준수 센터 할 것 고급 eDiscovery의 대/소문자에 액세스할 수 있습니다.
  
참조에서 1 단계에 사용자 할당 하려면 필요한 권한을 eDiscovery 사례의 구성원으로 추가할 수 있도록, [Office 365 보안에서 eDiscovery 사례 &amp; 준수 센터](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members)합니다.
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a>2 단계: eDiscovery 사례를 만들고 구성원 추가

보안에서 새 eDiscovery 사례를 만들려면 다음 단계는 &amp; 준수 센터 및 구성원을 추가 합니다. 대/소문자의 구성원 고급 eDiscovery의 대/소문자를 액세스할 수 없게 됩니다.
  
1. 새 eDiscovery 사례를 만들려면에서 2 단계 참조 [Office 365 보안에서 eDiscovery 사례 &amp; 준수 센터](ediscovery-cases.md#step-2-create-a-new-case)합니다.
    
2. EDiscovery 사례에 구성원을 추가 하려면의 3 단계 참조 [Office 365 보안에서 eDiscovery 사례 &amp; 준수 센터](ediscovery-cases.md#step-3-add-members-to-a-case)
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a>3 단계: 고급 ediscovery에서 사례 이동

EDiscovery 사례를 만들고 구성원을 추가 하는 후 사용자 (또는 대/소문자의 모든 구성원) 고급 eDiscovery에 해당 하는 경우에 액세스할 수 있습니다. 고급 ediscovery에서 사례에 액세스 하려면에서 8 단계를 참조 [Office 365 보안에서 eDiscovery 사례 &amp; 준수 센터](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery)합니다.
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[데이터 준비](prepare-data-for-advanced-ediscovery.md)
 