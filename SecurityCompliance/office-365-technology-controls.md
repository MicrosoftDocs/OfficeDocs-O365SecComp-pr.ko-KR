---
title: Office 365 기술 컨트롤
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: '요약: Office 365에 대 한 Microsoft의 기술 제어 관행에 대 한 개요입니다.'
ms.openlocfilehash: 77dee44ec648ea2aa1dab61776089bf7d9e2580a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220378"
---
# <a name="office-365-technology-controls"></a>Office 365 기술 컨트롤 

Microsoft는 다양 한 도구와 기술을 사용 하 여 Lockbox 및 고객 lockbox, 다단계 인증 등을 포함 하 여 Exchange online 및 SharePoint online에서 고객 데이터에 대 한 액세스를 제어, 관리 및 감사 합니다. yammer enterprise는 [yammer enterprise Access 컨트롤](office-365-yammer-enterprise-access-controls.md)에 설명 된 것 처럼 비슷한 컨트롤을 사용 합니다.

office 365 엔지니어가 office 365 고객 데이터에 계속 액세스할 수 있으며, 고객이 Exchange online 및 SharePoint online에 대 한 고객 Lockbox 기능에 라이선스를 제공 하는 경우 Microsoft와-를 모두 포함 하는 승인 프로세스를 거쳐야 함-고객 승인-서비스 작업에 대 한 고객 데이터에 대 한 액세스를 수행할 수 있습니다. 승인이 부여 되 면 서비스 요청에 필요한 작업을 수행 하는 데 충분 한 액세스 권한이 있는 경우에만 작업별 관리 계정이 프로 비전 됩니다.

## <a name="lockbox-and-customer-lockbox"></a>lockbox 및 고객 lockbox
매우 드문 경우 지만 고객은 microsoft의 지원을 요청 하 여 microsoft에 문제를 지원 하기 위해 고객에 게 제공할 수 있습니다. 사용자의 사서함에 저장 된 비즈니스용 skype 데이터를 포함 하는 Exchange Online에 대 한 액세스를 제어 하려면 (비즈니스용 skype 수신에는 비즈니스용 skype 모임 브로드캐스트 또는 사용자가 모임에 업로드 한 콘텐츠는 포함 하지 않음), SharePoint online ( 비즈니스용 OneDrive 포함) Microsoft에서는 Lockbox 라는 액세스 제어 시스템을 사용 합니다. Microsoft 엔지니어가 모든 Exchange online 또는 SharePoint online 시스템 또는 데이터에 액세스할 수 있으려면 먼저 Lockbox를 사용 하 여 액세스 요청을 제출 해야 합니다. Exchange online 또는 SharePoint online에 대 한 모든 권한 상승에는 Lockbox를 사용 해야 합니다.

Lockbox는 엔지니어에 게 서비스 내에서 운영 및 관리 기능을 수행할 수 있는 권한을 부여 하는 요청을 처리 합니다. 엔지니어가 고객 데이터에 액세스 하는 기능을 얻기 위해 관리자가 승인 해야 하는 Lockbox를 통해 요청을 제출 합니다. 관리자가 승인을 받은 엔지니어는 시간 제한 되 고 고객 데이터에 대 한 제한 된 액세스를 통해 고객의 문제를 해결할 수 있습니다.

고객 Lockbox for Office 365는 명시적 데이터 액세스 권한 부여를 위한 절차가 필요한 경우 FedRAMP 및 HIPAA에 나와 있는 준수 의무를 충족 하는 데 도움이 될 수 있습니다. 드문 경우이 든 Microsoft 서비스 엔지니어가 데이터에 액세스 해야 하는 경우에는 문제를 해결 하는 데 필요한 데이터에만 액세스 권한을 부여 하 고 제한 된 시간에만 해당 합니다. 지원 엔지니어가 수행 하는 작업은 감사 목적으로 기록 되며, [Office 365 관리 활동 API](https://msdn.microsoft.com/library/office/dn707383.aspx) 와 [보안 및 준수 센터](http://protection.office.com/)를 통해 액세스할 수 있습니다. 고객 lockbox는 해당 고객을 Lockbox 승인 프로세스에 삽입 하 고 서비스 작업을 위해 Exchange online 또는 SharePoint online 콘텐츠에 대 한 Microsoft 액세스 권한 부여를 제어할 수 있는 기능을 제공 합니다.

>**참고**: 고객 Lockbox는 [office 365 Enterprise E5](https://products.office.com/business/office-365-enterprise-e5-business-software) 및 추가 기능 구매에서 사용할 수 있지만 수동 작업은 office 365 관리 센터 (서비스 설정 |)에서 수행 해야 합니다. 고객 Lockbox)를 사용 하도록 설정 합니다. 자세한 내용은 [Office 365 고객 Lockbox 요청](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)을 참조 하세요.

Exchange online 및 SharePoint online에 대 한 모든 서비스 요청은 Lockbox 시스템에서 처리 됩니다. 그리고 고객 Lockbox를 사용 하 여 고객 데이터에 대 한 노출을 통해 이러한 서비스에 액세스 하는 모든 서비스 작업은 Lockbox 승인 프로세스를 통과 한 다음 고객이 해당 요청을 승인 하거나 거부할 수 있습니다.
 
*그림 1-고객 Lockbox 워크플로*

고객이 요청을 거부 한 경우 Microsoft 엔지니어가 고객의 콘텐츠에 액세스할 수 없으며 서비스 작업을 완료 하지 못합니다. 고객이 요청을 승인 하는 경우 Microsoft 엔지니어가 모니터링 및 제한 된 관리 인터페이스를 통해 고객 콘텐츠에 대 한 just-in-time 액세스를 제한할 수 있습니다. lockbox와 고객 lockbox를 모두 사용 하 여 모든 승인 된 액세스를 고유 사용자에 게 추적할 수 있으므로 엔지니어가 고객 데이터를 처리 하는 데 책임이 있습니다.

## <a name="just-in-time-access"></a>just-in-time 액세스
Microsoft는 Office 365에 대 한 JIT (just-in-time) 액세스 원칙을 사용 하 여 자격 증명 무단 변경 및 측면 공격의 위험을 더 완화 합니다. JIT는 서비스에 대 한 영구 관리 액세스를 제거 하 고 이러한 권한을 요청 시 해당 역할에 상승 시키는 기능으로 대체 합니다. 관리자 로부터 영구 권한을 제거 하면 자격 증명은 필요한 경우에만 사용할 수 있으며 자격 증명 도난을 발생 하는 경우 회사에 게 야기 되는 위험을 제거 합니다.

JIT 액세스 모델을 사용 하려면 엔지니어 들이 제한 된 기간 동안 관리 업무를 수행 하도록 관리자 권한을 요청 해야 합니다. 또한 oces는 시스템에서 생성 된 복잡 한 암호를 사용 하 여 만들고 필요한 작업을 수행 하도록 허용 하는 역할만 부여 하는 임시 계정을 사용할 수 있습니다. 예를 들어 Lockbox에서 부여 된 관리 액세스는 시간에 바인딩되며, 액세스 허용 되는 시간은 요청 되는 역할에 따라 달라 집니다. 엔지니어는 Lockbox 시스템에 요청을 수행 하는 동안 필요한 시간 액세스 기간을 지정 합니다. Lockbox 시스템은 요청 된 시간이 권한 상승의 최대 허용 시간을 초과 하는 요청을 거부 합니다. 권한 상승 요청이 만료 되 면 관리 액세스가 제거 되 고 임시 계정이 만료 됩니다.

예를 들어 시스템 디버깅을 위해 액세스 권한이 부여 되 고 승인 된 경우 엔지니어는 높은 수준의 액세스에 대 한 요청이 승인 될 때마다 인증 시스템에서 생성 한 일회성 사용 관리 암호를 받습니다. 이 암호는 엔지니어가 암호를 안전 하 게 보호 하 고, Microsoft 기업 환경에 대 한 엔지니어의 자격 증명과는 별도로, 상승 된 액세스를 승인한 세션에만 적합 합니다.

## <a name="constrained-management-interfaces"></a>제한 된 관리 인터페이스
oces 두 가지 관리 인터페이스를 사용 하 여 관리 작업 (보안 터미널 서비스 게이트웨이 (TSGs) 및 원격 PowerShell을 통해 원격 데스크톱)을 수행 합니다. 이러한 관리 인터페이스 내에는 실행할 수 있는 응용 프로그램 및 사용할 수 있는 명령 및 cmdlet에 대 한 중요 한 제한을 적용 하는 소프트웨어 정책 및 액세스 컨트롤이 있습니다. 

Office 365 서버가 동시 세션을 서버당 하나의 세션 (서버당) 별로 제한 합니다. TSGs는 사용자에 대해 단일 동시 세션만 허용 하도록 구성 되며 여러 세션을 허용 하지 않습니다. TSGs는 Office 365 서비스 팀 관리자가 서버당 단일 세션을 사용 하 여 동시에 여러 서버에 연결할 수 있도록 하 여 관리자가 해당 작업을 효과적으로 수행 하도록 허용 합니다. 서비스 팀 관리자에 게는 TSGs 자체에 대 한 권한이 없습니다. TSG는 MFA (multi-factor authentication) 및 암호화 요구 사항을 적용 하는 경우에만 사용 됩니다. 서비스 팀 관리자가 TSG를 통해 특정 서버에 연결 되 면 특정 서버는 관리자 당 하나의 세션 제한을 적용 합니다.

Active Directory 그룹 정책에 의해 Office 365 담당자에 대 한 사용 제한 및 연결 및 구성 요구 사항이 설정 됩니다. 이러한 정책에는 다음과 같은 특징이 있습니다.
- TSGs [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2 유효성 검사 암호화만 사용 하도록 구성 되어 있습니다.
- TSG 세션이 30 분 정도 비활성 후 연결을 끊도록 구성 됩니다.
- 24 시간 후에 자동으로 로그 오프 되도록 TSG 세션을 구성 합니다.

또한 TSGs에 연결 하려면 별도의 실제 스마트 카드와 엔지니어의 Microsoft 회사 자격 증명과 별개인 계정을 사용 하 여 MFA를 요구 합니다. 엔지니어는 다양 한 플랫폼에 대해 서로 다른 스마트 카드를 발급 하며, 암호 관리 플랫폼은 자격 증명을 안전 하 게 저장 하는 데 사용 됩니다. TSGs에서는 Active Directory 그룹 정책을 사용 하 여 원격 서버에 로그인 할 수 있는 사람, 허용 되는 세션 수 및 유휴 시간 제한 설정을 제어 합니다. 허용 되는 응용 프로그램에 대 한 액세스를 제한 하 고 인터넷 액세스를 제한 하기 위한 추가 정책이 적용 됩니다.

원격 액세스 외에도 특별히 구성 된 TSGs를 사용 하는 경우 Exchange Online에서는 서비스 엔지니어 작업 역할이 있는 사용자가 원격 PowerShell을 사용 하 여 프로덕션 서버의 특정 관리 기능에 액세스할 수 있도록 허용 합니다. 이 작업을 수행 하려면 사용자에 게 Office 365 프로덕션 환경에 대 한 읽기 전용 (디버그) 액세스 권한이 있어야 합니다. 권한 상승 기능은 Lockbox 프로세스를 사용 하는 TSGs와 동일한 방식으로 사용 하도록 설정 됩니다.

원격 액세스의 경우 단일 액세스 지점으로 사용 되는 각 데이터 센터에 부하가 분산 된 가상 IP가 있습니다. 실행할 수 있는 원격 PowerShell cmdlet은 인증 하는 동안 가져온 액세스 클레임에서 식별 된 권한 수준을 기반으로 합니다. 이러한 cmdlet은이 방법을 사용 하 여 연결 하는 사용자가 액세스 하 고 실행할 수 있는 유일한 관리 기능입니다. 원격 PowerShell을 사용 하 여 엔지니어가 사용할 수 있는 명령 범위를 제한 하 고, Lockbox 프로세스를 통해 부여 되는 액세스 수준을 기반으로 합니다. 예를 들어 Exchange Online에서는 Get 사서함을 사용할 수 있지만 설정 된 사서함은 사용 하지 못할 수 있습니다.
