---
title: Office 365에 대 한 모바일 장치 관리 (MDM) 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- O365M_MDMConfigDomains
- O365E_MDMConfigDomains
- ms.o365.cc.DevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: faa7d8e5-645d-4d59-839c-c8d4c1869e4a
description: 관리 하 고 Office 365에 대 한 모바일 장치 관리를 사용 하 여 Office 365 조직에 연결 하는 경우 모바일 장치 보안 수 있습니다. 직원이 자신의 업무를 어디에서 든 지 언제 어디서 든 수행를 얻을 수 있도록 중요 한 역할을 재생 하는 문서 및 스마트폰 및 태블릿 작업 전자 메일, 일정, 연락처, 액세스 하는데 사용 되는 모바일 장치 같은. 중요 한 사용자 장치를 사용 하는 경우 조직의 정보를 보호 데 도움이 되도록 합니다. 분실 또는 도난당는 자신이 하는 경우 모바일 장치를 초기화 하 고 장치 보안 정책 및 액세스 규칙을 설정 하려면 Office 365에 대 한 MDM를 사용할 수 있습니다.
ms.openlocfilehash: f06cef11b68ee0673f13c54738f07f4556495fdd
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272493"
---
# <a name="overview-of-mobile-device-management-mdm-for-office-365"></a>Office 365에 대 한 모바일 장치 관리 (MDM) 개요

관리 하 고 Office 365에 대 한 모바일 장치 관리를 사용 하 여 Office 365 조직에 연결 하는 경우 모바일 장치 보안 수 있습니다. 직원이 자신의 업무를 어디에서 든 지 언제 어디서 든 수행를 얻을 수 있도록 중요 한 역할을 재생 하는 문서 및 스마트폰 및 태블릿 작업 전자 메일, 일정, 연락처, 액세스 하는데 사용 되는 모바일 장치 같은. 중요 한 사용자 장치를 사용 하는 경우 조직의 정보를 보호 데 도움이 되도록 합니다. 분실 또는 도난당는 자신이 하는 경우 모바일 장치를 초기화 하 고 장치 보안 정책 및 액세스 규칙을 설정 하려면 Office 365에 대 한 MDM를 사용할 수 있습니다.
  
![Android 휴대폰에서 MDM](media/69b9a9f6-13ac-4e36-99ca-95e82e0375aa.png)
  
## <a name="what-types-of-devices-can-you-manage"></a>어떤 종류의 장치를 관리할 수 있습니까?

다양 한 유형의 Windows Phone, Android, iPhone, iPad와 같은 모바일 장치를 관리 하려면 Office 365에 대 한 MDM를 사용할 수 있습니다. 조직에서 사용자가 사용 되는 모바일 장치를 관리 하려면 각 사용자는 해당 Office 365 라이선스가 있어야 하 고 Office 365에 대 한 해당 장치를 MDM에 등록 해야 합니다. 
  
Office 365에 대 한 MDM에서는 각 유형의 장치에 대 한 지원, 참조 [기능의 모바일 장치에 대 한 관리 Office 365](capabilities-of-mobile-device-management.md).
  
## <a name="setup-steps-for-mdm"></a>MDM에 대 한 설치 단계

Office 365 전역 관리자는 활성화 하 고 Office 365에 대 한 MDM를 설정 하려면 다음 단계를 완료 해야 합니다. 자세한 단계를 보려면 [Office 365에 대 한 MDM 설정](set-up-mobile-device-management.md) 는 항목에 대 한 지침을 따릅니다. 간략히 요약 하면 다음과 같습니다. 
  
> 1 단계: [을 모바일 장치 관리 (MDM) Office 365에서 설정](set-up-mobile-device-management.md)의 단계를 수행 하 여 Office 365에 대 한 MDM를 활성화 합니다.
    
> 2 단계: 설정 MDM, 하 여 Office 365에 대 한 예 iOS 장치를 관리 하는 한 apn을 사용할 인증서를 만들고 Windows 전화를 지원 하기 위해 도메인에 대 한 시스템 DNS (Domain Name) 레코드를 추가 합니다.
    
> 3 단계: 장치 정책 만들기 및 사용자 그룹에 적용 합니다. 이렇게 하면 사용자 [장치에 등록 메시지](enroll-your-mobile-device.md)를 받습니다. 및 통해 장치 하 여 설정한 정책에 의해 제한 될 됩니다 등록을 완료 했을 때 있습니다.
    
    ![Creating an MDN device policy under Device security policies](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
## <a name="device-management-tasks"></a>장치 관리 작업

MDM를 설정 하는 Office 365에 대 한 얻은 했을 때 사용자가 장치를 등록 한 후 장치를 관리할 수,이 대 한 액세스를 차단 또는 필요한 경우 한 장치를 초기화 합니다. [몇가지 일반적인 장치 관리 작업](manage-devices-in-mdm.md)을 비롯 한 작업을 완료 하는 위치에 대 한 자세한 내용은 합니다.
  
## <a name="other-ways-to-manage-devices-and-apps"></a>장치 및 앱을 관리 하는 다른 방법

필요한 경우 Office 365에 대 한 MDM 보다 더 많은 기능 포함 Intune 구독은 조직의 요구를 충족 하는 경우를 확인 하려면이 [MDM 및 Microsoft Intune 기능 비교](choose-between-mdm-and-intune.md) 를 확인 하십시오. 
  
모바일 응용 프로그램 관리 (MAM) 하기만 하는 경우 아마도 자신의 장치에서 회사 프로젝트를 업데이트 하는 사용자에 대 한 Intune 제공를 등록 하 고 장치 관리 외에도 다른 옵션입니다. Intune 구독을 사용 하면 사용자의 장치 Intune에 등록 되지 않은 경우에 Azure 포털을 사용 하 여 MAM 정책을 설정할 수 있습니다. [MAM 정책을 사용 하 여 응용 프로그램 데이터를 보호를](https://go.microsoft.com/fwlink/?LinkId=825439)참조 하십시오. 
  
## <a name="see-also"></a>참고 항목

[MDM에서 관리 하는 장치에 대 한 정보를 봅니다.](get-details-about-mdm-managed-devices.md)

[Office 365에 대 한 MDM 설정](set-up-mobile-device-management.md)
  
[MDM의 모바일 장치 등록](enroll-your-mobile-device.md)
  
[MDM에 등록 하는 장치 관리](manage-devices-in-mdm.md)

