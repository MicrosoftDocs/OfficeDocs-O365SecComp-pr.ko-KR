---
title: Office 365의 모바일 장치 관리에 등록 하는 장치 관리
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
- MBS150
- MET150
ms.assetid: 28dd276b-beeb-4c5b-8b22-7551186127fe
description: 모바일 장치 관리 (MDM) Office 365에서을 설정 하려면 다음이 단계를 수행 합니다.
ms.openlocfilehash: 3a84b6904b866e07eb4efabe0f39041b282d0ba9
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272313"
---
# <a name="manage-devices-enrolled-in-mobile-device-management-in-office-365"></a>Office 365의 모바일 장치 관리에 등록 하는 장치 관리

Office 365에 대 한 기본 제공 되는 모바일 장치 관리를 사용 하면 보안을 유지 하 고 Iphone, Ipad, Androids, 같은 사용자의 모바일 장치를 관리 하 고 Windows 전화 합니다. 첫번째 단계는 [Office 365에 대 한 MDM를 설정](set-up-mobile-device-management.md)하 고 Office 365에 로그인 할 것입니다. 
  
조직에서 사용자를 설정 했을 때 서비스에 [해당 장치를 등록](enroll-your-mobile-device.md) 해야 합니다. 다음 Office 365에 대 한 MDM 조직에서 장치를 관리 하는데 사용할 수 있습니다. 예, 장치 보안 정책 전자 메일 액세스 또는 기타 서비스 제한, 장치 보고서 보기 및 장치를 원격으로 초기화 하는데 사용할 수 있습니다. 일반적으로 이동 하는 [Office 365 보안으로 이동 &amp; 준수 센터](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) 을 이러한 작업을 수행 하기 위해 합니다. 
  
## <a name="device-management-tasks"></a>장치 관리 작업

장치 관리 패널을 가져오려면 다음이 단계를 수행 합니다. 
  
1. Office 365 관리 센터로 이동합니다.
    
2. 모바일 장치 관리에는 검색 필드에 입력 하 고 결과 목록에서 **모바일 장치 관리** 를 선택 합니다. 
    
    ![O365 검색 필드에 모바일 장치 관리자를 입력](media/e2e2f1c0-e543-431a-959b-e26c2ba328a7.png)
  
후 MDM를 설정 하는 Office 365에 대 한, 조직에서 모바일 장치를 관리 하는 방법을 다음과 같습니다. 
  
|**수행할 작업...**|**수행 작업**|
|:-----|:-----|
|장치 지우기  <br/> |장치 관리 패널에서 *장치 이름* , **전체 지우기** 모든 정보 또는 **선택적으로 닦아내기** 장치에만 조직의 정보를 삭제 하려면 삭제를 선택 합니다.  <br/> [Office 365의 장치 지우기 시도](wipe-a-mobile-device.md)참조 하십시오.  <br/> |
|Exchange ActiveSync를 사용하여 지원되지 않는 장치의 Exchange 전자 메일 액세스 차단  <br/> |장치 관리 패널에서 **블록**을 선택 합니다.  <br/> |
|암호 요구 사항 및 보안 설정 같은 장치 정책 설정  <br/> |장치 관리 패널에서 클릭 \> **장치 보안 정책** \> **추가 +** 합니다.  <br/> 참조 [만들기 및 장치 보안 정책 배포](create-device-security-policies.md)합니다.  <br/> |
|차단된 장치 목록 보기  <br/> |장치 관리 패널의 **보기 선택** 아래에서 **차단 됨**을 선택 합니다.  <br/> ||
|사용자 또는 사용자 그룹에 대해 비규격 또는 지원되지 않는 장치의 차단 해제  <br/> | 상황에 따라 준수 하지 않는 장치 여러가지 방법으로 차단을 해제할 수 있습니다. 다음 중 하나를 선택 합니다.<br/>  정책에 적용 된 보안 그룹에서 사용자 또는 사용자를 제거 합니다. **Office 365 관리** 센터로 이동 \> **그룹**을 클릭 한 다음 선택 * 그룹 이름 *. **구성원 및 관리자가 편집**을 클릭 합니다.<br/>  사용자가 장치 정책에서의 구성원 이어야 하는 보안 그룹을 제거 합니다. 이동 **보안 &amp; 준수 센터** \> **보안 정책** \> **장치 보안 정책**입니다. 선택 * 장치 정책 이름 *, **편집** 을 클릭 한 다음 ![편집 아이콘](media/O365_MDM_CreatePolicy_EditIcon.gif) \> **배포**합니다.<br/>  장치 정책에 대 한 모든 준수 하지 않는 장치를 차단 해제 합니다. 이동 **보안 &amp; 준수 센터** \> **보안 정책** \> **장치 보안 정책**입니다. *장치 정책 이름* 을 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/O365_MDM_CreatePolicy_EditIcon.gif) \> **액세스 요구 사항**입니다. **액세스 및 보고서 위반 허용**을 선택 합니다.<br/>  사용자 또는 사용자 그룹에 대 한 준수 하지 않는 또는 지원 하지 않는 장치에 차단 해제 하려면으로 이동 하십시오로 이동 **보안 &amp; 준수 센터** \> **보안 정책** \> **장치 관리** \> **장치 액세스 관리 설정 **. Office 365에 대 한 액세스를 차단 되 고에서 제외 하려는 구성원과 보안 그룹을 추가 합니다. [만들기, 편집 또는 Office 365 관리 센터에서 보안 그룹 삭제](https://support.office.com/article/55c96b32-e086-4c9e-948b-a018b44510cb)를 참조 하십시오.<br/> |
|조직에는 장치에 대 한 세부 정보 가져오기  <br/> |같은 장치는 등록 하 고 장치 보안 정책을 사용 하 여 규정을 준수 하는 세부 정보를 얻으려면 [MDM에서 관리 하는 장치에 대 한 세부 정보를 가져올](get-details-about-mdm-managed-devices.md)에 설명 된 단계를 수행 합니다.  <br/> |
|MDM 더이상 해당 장치는 관리 하는 하므로 사용자를 제거 합니다.  <br/> |사용자를 제거 하는 MDM에 대 한 장치 관리 정책에는 보안 그룹을 편집 합니다. [만들기, 편집 또는 Office 365 관리 센터에서 보안 그룹 삭제](https://support.office.com/article/55c96b32-e086-4c9e-948b-a018b44510cb)를 참조 하십시오.<br/> MDM에서 모든 Office 365 사용자를 제거 하려면 [Office 365의 모바일 장치 관리 해제](turn-off-mdm.md)를 참조 합니다.  <br/> |
   

