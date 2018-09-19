---
title: Office 365에서 데이터 및 서비스에 대한 액세스 보호
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: O365 데이터 및 서비스에 대 한 액세스를 보호 하기 위해 페이지를 방문 합니다.
ms.openlocfilehash: 6ea617b1a7a7a34492689908d4816a851d58e776
ms.sourcegitcommit: 0ce722533d72fa8dcc1d8a58d3c649cb345b938d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "24009104"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a>Office 365에서 데이터 및 서비스에 대한 액세스 보호

Office 365 데이터 및 서비스에 대 한 액세스를 보호 하는 것은 인터넷 공격을 방어 하 고 데이터 손실을 예방 중요 합니다. 환경의 다른 SaaS 응용 프로그램에 동일한 보호를 적용할 수 및 Azure Active Directory 응용 프로그램 프록시를 사용 하 여 온-프레미스 응용 프로그램에도 게시 합니다.
  
## <a name="step-1-review-recommendations"></a>1 단계: 검토 권장 사항

Azure AD 응용프로그램 프록시를 사용하여 게시한 온-프레미스 응용 프로그램, Office 365 및 다른 SaaS 서비스에 액세스하는 ID 및 장치를 보호하기 위해 권장되는 기능입니다.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [더 많은 언어](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>2 단계: MFA 구성

이러한 리소스를 사용 하 여 MFA를 지정 하는 사용자가 직접 버전은 적합 한, 결정을 하 고 계획 하 고 MFA 사용자의 환경에 배포 합니다.
  
- [Azure 다단계 인증 이란?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Azure 다단계 인증 솔루션 선택](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Azure 다단계 인증을 얻는 방법](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Office 365 배포에 대 한 다중 요소 인증에 대 한 계획](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Office 365 사용자에 게 다단계 인증 설정](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [MFA, 클라우드 또는 온-프레미스 배포 위치 계획](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Azure 다단계 인증 설정 구성](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>3 단계: Azure AD 조건부 액세스 규칙으로 MFA 적용

Azure AD MFA를 사용 하는 경우 Office 365 및 환경에서 다른 SaaS 응용 프로그램에 대 한 액세스에 대 한 MFA를 요청 하는 조건부 액세스 규칙을 만듭니다.
  
- [Azure Active Directory에 대 한 조건부 액세스](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>4 단계: 액세스 권한을된 관리 구성

액세스 권한 관리 Office 365에서 권한이 부여 된 관리 작업을 통해 세분화 된 액세스 제어를 허용 합니다.  기존 관리자가 권한이 부여 된 사용자 계정은 중요 한 데이터에 대 한 순위 액세스 또는 중요 한 구성 설정에 대 한 액세스를 사용할 수 있는 침해에서 조직을 보호 하는 것이 도움이 됩니다.

- [권한 개요 액세스 관리](privileged-access-managment-overview.md)
- [액세스 권한을된 관리 구성](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>5 단계: SharePoint 장치 액세스 정책 구성

중요 한, 분류, 및 규제 데이터를 보호 하는 것에 대 한 SharePoint Online 및 비즈니스용 OneDrive에 대 한 장치 액세스 정책을 사용 하는 것이 좋습니다. 장치 액세스 정책을 개별 팀 사이트에 적용할 수 있는 기능을는 곧 제공 될 예정입니다.
  
- [관리되지 않는 장치에서 액세스 제어](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>6 단계: 장치에 대 한 응용 프로그램 및 데이터 보호를 구성 합니다.

모바일 장치 관리에 대 한 장치는 등록 되었는지 여부에 관계 없이 모바일 장치에서 응용 프로그램을 관리할 수 있습니다. 이 실수로 유출 메일 및 파일을 포함 하 여 Office 365의 데이터를 보호 합니다.
  
- IOS 및 Android: [Microsoft Intune를 사용한 응용 프로그램 보호 정책을 사용 하 여 응용 프로그램 데이터를 보호](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Windows 10에 대 한 Windows 정보 보호 (진행 중) 실수로 데이터 누출 방지 하기 위해를 구성 합니다.
  
- 관리 되는 장치에 대 한: [Microsoft Intune를 위한 Azure 포털을 사용 하 여 등록 정책 사용 하 여 Windows 정보 보호 (WIP) 만들기](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- 되지 않은 관리 되는 장치에 대 한: [만들기 진행 (Windows 정보 보호 중) 응용 프로그램 보호 정책을 Intune 사용한 배포 및](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>7 단계: Intune 사용 하 여 장치를 관리 합니다.

장치 관리를 사용 하면 사용자 환경에서 리소스에 대 한 액세스를 허용 하기 전에 정상 상태이 고 호환 되는지 확인 합니다. 장치 기반 규칙을 보장 공격자가 액세스할 수 없으므로 자원에 비관리 장치에서 조건부 액세스 합니다.
  
- [Intune의 관리 기능에 대 한 장치를 등록 합니다.](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>8 단계: 추가 Intune 정책 및 사용자 환경에 대 한 조건부 액세스 규칙 구성

엔터프라이즈 규모 또는 복잡 한 access 보안 시나리오에 대 한 시작 지점으로 권장 되는 구성에 사용 합니다.
  
- [전자 메일 보안 정책 및 구성](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

