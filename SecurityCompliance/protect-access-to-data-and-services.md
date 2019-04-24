---
title: 사용자 및 장치 액세스 보호
ms.author: bcarter
author: brendacarter
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
ms.openlocfilehash: e1b529a641d25f82521c40d0df9d091e0ebb5d90
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265230"
---
# <a name="protect-user-and-device-access"></a>사용자 및 장치 액세스 보호

Office 365 데이터 및 서비스에 대 한 액세스를 보호 하는 것은 사이버 공격을 방지 하 고 데이터 손실 로부터 보호 하는 데 매우 중요 합니다. 해당 환경의 다른 SaaS 응용 프로그램 및 Azure Active Directory 응용 프로그램 프록시를 사용 하 여 게시 된 온-프레미스 응용 프로그램에도 동일한 보호를 적용할 수 있습니다.
  
## <a name="step-1-review-recommendations"></a>1 단계: 권장 사항 검토

Azure AD 애플리케이션 프록시를 사용하여 게시한 온-프레미스 응용 프로그램, Office 365 및 다른 SaaS 서비스에 액세스하는 ID 및 디바이스를 보호하기 위해 권장되는 기능입니다.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [더 많은 언어](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-protect-administrator-accounts-and-access"></a>2 단계: 관리자 계정 보호 및 액세스
Office 365 환경을 관리 하는 데 사용 하는 관리 계정에 상승 된 권한이 포함 되어 있습니다. 해커 및 사이버 범죄자에 게 유용한 목표입니다. 

먼저 관리용 관리자 계정만 사용 합니다. 관리자에 게는 관리 작업과 관련 된 일반 사용을 위한 별도의 사용자 계정이 있어야 하며, 해당 작업 기능과 연결 되는 작업을 완료 하는 데 필요한 경우에만 해당 관리자 계정을 사용 해야 합니다.

multi-factor authentication 및 조건부 액세스를 사용 하 여 관리자 계정을 보호 합니다. 자세한 내용은 [관리자 계정 보호](https://docs.microsoft.com/en-us/microsoft-365/enterprise/identity-access-prerequisites#protecting-administrator-accounts)를 참조 하세요. 

다음으로, Office 365에서 권한이 부여 된 액세스 관리를 구성 합니다. 권한이 부여 된 액세스 관리를 통해 Office 365의 권한 있는 관리 작업을 세부적으로 제어할 수 있습니다. 중요 한 데이터에 대 한 액세스 권한이 나 중요 한 구성 설정에 대 한 액세스 권한이 있는 기존 권한 관리 계정을 사용 하는 보안 침해 로부터 조직을 보호 하는 데 도움이 될 수 있습니다.

- [권한 있는 액세스 관리 개요](privileged-access-management-overview.md)
- [권한이 부여된 액세스 관리 구성](privileged-access-management-configuration.md)

또 다른 주요 권장 사항은 관리 작업을 위해 특별히 구성 된 워크스테이션을 사용 하는 것입니다. 관리 작업에만 사용 되는 전용 장치입니다. [권한 있는 액세스 보호](https://docs.microsoft.com/en-us/windows-server/identity/securing-privileged-access/securing-privileged-access)를 참조 하세요.

마지막으로, 테 넌 트에서 두 개 이상의 응급 액세스 계정을 만들어 실수로 관리 액세스가 부족 하다는 영향을 완화할 수 있습니다. [Azure AD에서 긴급 액세스 계정 관리를](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-emergency-access)참조 하세요. 

## <a name="step-3-configure-recommended-identity-and-device-access-policies"></a>3 단계: 권장 되는 id 및 장치 액세스 정책 구성
MFA (multi-factor authentication) 및 조건부 액세스 정책은 손상 된 계정 및 무단 액세스를 완화 하기 위한 강력한 도구입니다. 함께 테스트 된 정책 집합을 구현 하는 것이 좋습니다. 배포 단계를 비롯 한 자세한 내용은 [id 및 장치 액세스 구성](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations)를 참조 하세요.

 이러한 정책은 다음과 같은 기능을 구현 합니다.
- 여러 요소 인증
- 조건부 액세스
- Intune 앱 보호 (장치용 앱 및 데이터 보호)
- Intune 장치 준수
- Azure AD ID 보호

Implemetning Intune 장치 준수에는 장치 등록이 필요 합니다. 장치를 관리 하면 해당 환경의 리소스에 대 한 액세스를 허용 하기 전에 정상 및 호환이 가능 하도록 할 수 있습니다. [Intune에서 관리용 장치 등록](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune) 을 참조 하세요.

## <a name="step-4-configure-sharepoint-device-access-policies"></a>4 단계: SharePoint 장치 액세스 정책 구성

Microsoft는 장치 액세스 제어를 통해 중요 하 고 규제 된 콘텐츠를 사용 하 여 SharePoint 사이트의 콘텐츠를 보호 하는 것이 좋습니다. 자세한 내용은 [SharePoint 사이트 및 파일을 보호 하기 위한 정책 권장 사항을](https://docs.microsoft.com/en-us/microsoft-365/enterprise/sharepoint-file-access-policies)참조 하세요.



    

