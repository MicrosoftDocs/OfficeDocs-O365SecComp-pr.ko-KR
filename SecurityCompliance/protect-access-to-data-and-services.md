---
title: Office 365에서 데이터 및 서비스에 대한 액세스 보호
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: O365 데이터 및 서비스에 대 한 액세스를 보호 하기 위한 랜딩 페이지
ms.openlocfilehash: 95933c5a7bc95f9fd70e8f3470055b57193971d4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213538"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a>Office 365에서 데이터 및 서비스에 대한 액세스 보호

Office 365 데이터 및 서비스에 대 한 액세스를 보호 하는 것은 사이버 공격을 방지 하 고 데이터 손실 로부터 보호 하는 데 매우 중요 합니다. 해당 환경의 다른 SaaS 응용 프로그램 및 Azure Active Directory 응용 프로그램 프록시를 사용 하 여 게시 된 온-프레미스 응용 프로그램에도 동일한 보호를 적용할 수 있습니다.
  
## <a name="step-1-review-recommendations"></a>1 단계: 권장 사항 검토

Azure AD 애플리케이션 프록시를 사용하여 게시한 온-프레미스 응용 프로그램, Office 365 및 다른 SaaS 서비스에 액세스하는 ID 및 디바이스를 보호하기 위해 권장되는 기능입니다.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [더 많은 언어](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>2 단계: MFA 구성

이러한 리소스를 사용 하 여 MFA를 선택 하 고, 사용자에 게 적합 한 버전을 결정 한 다음, 사용자 환경에 대 한 MFA를 계획 및 배포 합니다.
  
- [Azure multi-factor authentication 이란?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Azure multi-factor authentication 솔루션 선택](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Azure multi-factor authentication을 가져오는 방법](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Office 365 배포에 대 한 다단계 인증 계획](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Office 365에 대한 다단계 인증 설정](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)하려면
    
- [MFA, 클라우드 또는 온-프레미스를 배포할 위치 계획](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Azure multi-factor authentication 설정 구성](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>3 단계: Azure AD 조건부 액세스 규칙을 사용 하 여 MFA 적용

Azure AD MFA를 사용 하는 경우 해당 환경의 Office 365 및 기타 SaaS 앱에 액세스 하기 위해 MFA를 요구 하는 조건부 액세스 규칙을 만듭니다.
  
- [Azure Active Directory에서 조건부 액세스](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>4 단계: 권한 있는 액세스 관리 구성

권한이 부여 된 액세스 관리를 통해 Office 365의 권한 있는 관리 작업을 세부적으로 제어할 수 있습니다.  중요 한 데이터에 대 한 액세스 권한이 나 중요 한 구성 설정에 대 한 액세스 권한이 있는 기존 권한 관리 계정을 사용 하는 보안 침해 로부터 조직을 보호 하는 데 도움이 될 수 있습니다.

- [권한 있는 액세스 관리 개요](privileged-access-management-overview.md)
- [권한이 부여된 액세스 관리 구성](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>5 단계: SharePoint 장치 액세스 정책 구성

SharePoint Online 및 비즈니스용 OneDrive에 대 한 장치 액세스 정책은 중요, 분류 및 규제 데이터를 보호 하는 데 권장 됩니다. 출시 예정은 개별 팀 사이트에 장치 액세스 정책을 적용 하는 기능입니다.
  
- [관리되지 않는 장치에서 액세스 제어](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>6 단계: 장치에 대 한 앱 및 데이터 보호 구성

장치가 모바일 장치 관리에 등록 되었는지 여부에 관계 없이 모바일 장치에서 응용 프로그램을 관리할 수 있습니다. 이렇게 하면 메일 및 파일을 포함 하 여 Office 365에서 데이터가 실수로 누출 되지 않도록 보호 됩니다.
  
- iOS 및 Android의 경우: [Microsoft Intune에서 앱 보호 정책을 사용 하 여 앱 데이터 보호](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
windows 10의 경우 우발적 데이터 누출을 방지 하도록 WIP (windows Information Protection)를 구성 합니다.
  
- 관리 되는 장치: [Microsoft Intune 용 Azure portal을 사용 하 여 등록 정책으로 WIP (Windows Information Protection) 만들기](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- 관리 되지 않는 장치: [Intune을 사용 하 여 WIP (Windows Information protection) 앱 보호 정책 만들기 및 배포](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>7 단계: Intune을 사용 하 여 장치 관리

장치를 관리 하면 해당 환경의 리소스에 대 한 액세스를 허용 하기 전에 정상 및 호환이 가능 하도록 할 수 있습니다. 장치 기반 조건부 액세스 규칙은 공격자가 관리 되지 않는 장치에서 리소스에 대 한 액세스 권한을 얻을 수 없도록 지원 합니다.
  
- [Intune에서 관리용 장치 등록](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>8 단계: 사용자 환경에 대 한 추가 Intune 정책 및 조건부 액세스 규칙 구성

이러한 권장 구성을 엔터프라이즈 확장 또는 정교한 액세스 보안 시나리오의 시작 지점으로 사용 합니다.
  
- [전자 메일 정책 및 구성 보안](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

