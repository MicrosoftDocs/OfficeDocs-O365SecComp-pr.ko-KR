---
title: Office 365의 모바일 장치 관리를 해제 하는 방법
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- GPA150
- MET150
ms.assetid: 2709cafb-0a8b-44bc-8494-7e2fccfa2b19
description: Office 365 조직에서 모바일 장치에 적용 되 고의 MDM 정책을 중지 하려면 다음이 단계를 수행 합니다.
ms.openlocfilehash: 6b8f0036ed999b10263f5cc074df27175769e604
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272223"
---
# <a name="how-to-turn-off-mobile-device-management-in-office-365"></a>Office 365의 모바일 장치 관리를 해제 하는 방법

효과적으로 해제 하려면 MDM Office 365에 대 한 장치 관리 정책에서 사용자 (보안 그룹에 의해 정의 된)의 그룹을 제거 하거나 정책 자체를 제거 합니다. 
  
- 만들었고 장치 정책에서 사용자 보안 그룹을 제거 하 여 사용자 그룹을 제거 합니다. 
    
- 모든 MDM 장치 정책을 제거 하 여 모든 사용자에 대 한 MDM를 비활성화 합니다. 
    
이러한 옵션에는 조직에서 장치에 대 한 MDM 적용을 제거 됩니다. 그러나 없습니다 단순히 "구축을 중단 하" MDM Office 365에 대 한을 설정한 후 합니다.
  
> [!IMPORTANT]
> 주의 사용자의 장치에 미치는 영향의 사용자 보안 그룹 정책에서 제거 하거나 정책 자체를 제거 하는 경우. 예, 프로필 전자 메일 및 장치에 따라 캐시 된 전자 메일에 제거, 될 수 있습니다. 참조: [서로 다른 장치 유형에 대 한 보안 정책의 영향을 란?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)
  
## <a name="remove-user-security-groups-from-mdm-device-policies"></a>MDM 장치 정책에서 사용자 보안 그룹을 제거 합니다.

1. 이동 **보안 &amp; 준수 센터** \> **데이터 손실 방지** \> **장치 보안 정책**입니다.
    
2. 장치 정책을 선택 하 고 클릭 ![편집 아이콘](media/O365-MDM-CreatePolicy-EditIcon.gif) **정책을 편집**합니다.
    
3. **배포** **-제거**를 클릭 합니다.
    
    **그룹**보안 그룹을 선택 합니다.
    
4.  **제거**를 클릭합니다.
    
5. **저장**을 클릭합니다.
    
## <a name="remove-mdm-device-policies"></a>MDM 장치 정책 제거

1. 이동 **보안 &amp; 준수 센터** \> **보안 정책** \> **장치 보안 정책**입니다.
    
2. 장치 정책을 선택 하 고 다음을 클릭 ![휴지통의 이미지 아이콘을 수 있습니다. ](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **정책을 삭제**합니다.
    
3. **경고** 대화 상자에서 **예**를 클릭 합니다. 
    

