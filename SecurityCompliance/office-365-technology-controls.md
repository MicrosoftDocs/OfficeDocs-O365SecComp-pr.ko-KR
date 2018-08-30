---
title: Office 365 기술 컨트롤
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: Office 365에 대 한 Microsoft의 기술 제어 사례의 개요'
ms.openlocfilehash: 2ef04b558f5fa82075d9aa602b83d437aa4b2ee6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533387"
---
# <a name="office-365-technology-controls"></a>Office 365 기술 컨트롤 

Microsoft는 여러 도구 및 제어, 관리 및 Exchange Online 고객 데이터에 대 한 액세스를 감사 하는 기술 및 SharePoint Online, Lockbox 및 고객 Lockbox, 다단계 인증을 등을 사용 합니다. [Yammer Enterprise 액세스 제어](office-365-yammer-enterprise-access-controls.md)의 설명에 따라 Enterprise 비슷한 컨트롤을 사용 하 여 yammer 합니다.

Office 365 엔지니어 Office 365 고객 데이터에 0 순위 액세스할 수 있으며 Microsoft와 – 하는 경우 고객이 라이선스를 제공 고객 Lockbox 기능 Exchange Online 및 SharePoint Online-를 모두 포함 하는 승인 프로세스를 통해 야 고객 승인 전에 서비스 작업에 대 한 고객 데이터에 대 한 액세스에 발생할 수 있습니다. 승인 권한이 부여 되 면 서비스 관련 관리 계정 프로 비전 된-just-in-time 서비스 요청에 필요한 작업을 수행할 수 만큼 액세스 됩니다.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox 및 고객 Lockbox
매우 드문 수도 있지만 고객 문제에 대해 지원 하 고 고객의 콘텐츠를 Microsoft 엔지니어를 노출할 수 있는 Microsoft의 도움을 요청 수입니다. Exchange Online에 대 한 액세스를 제어 하려면 (사용자의 사서함에 저장 된 비즈니스 데이터에 대 한 모든 Skype를 포함 하는 (비즈니스 검사를 위한 Skype 포함 하지 않음 Skype 모임 브로드캐스트 녹음/녹화 또는 사용자가 모임에 업로드 된 콘텐츠가)) 및 SharePoint Online ( 비즈니스용 OneDrive 포함), Microsoft Lockbox를 호출 하는 액세스 제어 시스템을 사용 합니다. 모든 Microsoft 엔지니어는 모든 Exchange Online 또는 SharePoint Online 시스템 또는 데이터에 액세스 하기 전에 Lockbox를 사용 하 여 액세스 요청을 제출 해야 있습니다. Lockbox를 사용 하 여 Exchange Online 또는 SharePoint Online에 대 한 모든 상승 된 액세스에 대 한 필요 합니다.

Lockbox는 엔지니어 서비스 내에서 운영 및 관리 작업을 수행할 수 있는 기능을 부여 하는 사용 권한에 대 한 요청을 처리 합니다. 고객 데이터에 액세스 하는 기능을 사용할 수 있는 엔지니어 하기 전에 관리자가 승인 해야 하는 Lockbox 통해 엔지니어 전송 요청 수입니다. 관리자 승인 시 엔지니어는 고객의 문제에서 작동 하도록 고객 데이터에 대 한 시간 제한 및 범위를 제한 된 액세스를 있습니다.

Office 365에 대 한 고객 Lockbox은 명시적 데이터 액세스 권한 부여를 위한 전체에서 절차를 필요한 경우 FedRAMP 및 HIPAA에서 발견 된 연결과 같이 규정 준수 의무를 충족 하는 데 도움이 됩니다. 특수 한 인스턴스에 Microsoft 서비스 엔지니어, 데이터에 액세스 해야 하는 경우 문제를 해결 하려면 필요한 데이터에만 하 고 제한 된 기간에 대 한 액세스를 부여 합니다. 기술 지원 엔지니어가 수행한 작업 감사 목적에 대 한 기록 되 고 [Office 365 관리 활동 API](https://msdn.microsoft.com/library/office/dn707383.aspx) 와 [보안 및 규정 준수 센터를](http://protection.office.com/)통해 액세스할 수 있습니다. 고객 Lockbox Lockbox 승인 프로세스에는 고객을 삽입 하 고 서비스 작업에 대 한 해당 Exchange Online 또는 SharePoint Online 콘텐츠를 Microsoft access의 권한 부여를 제어할 수 있는 기능과를 제공 합니다.

>**참고**: 고객 Lockbox는 [Office 365 엔터프라이즈 e 5](https://products.office.com/business/office-365-enterprise-e5-business-software) 에서 및 추가 기능을 구입 하는으로 사용할 수 있지만 Office 365 관리 센터에서 수동 작업을 수행 해야 (서비스 설정에서 | 고객 Lockbox) 사용 하도록 설정 합니다. 자세한 내용은 [Office 365 고객 Lockbox 요청](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)을 참조 하십시오.

Exchange Online 및 SharePoint Online에 대 한 모든 서비스 요청 Lockbox 시스템에 의해 처리 됩니다. 및 고객 Lockbox와 고객 데이터에 대 한 노출와 이러한 서비스에 대 한 액세스를 하기 하며 모든 서비스 작업 Lockbox 승인 프로세스를 통과 한 다음 승인 또는 그 이후에 요청을 거부 하는 고객을 활성화 합니다.
 
*그림 1-고객 Lockbox 워크플로*

요청은 고객에 의해 거부, Microsoft 엔지니어 고객의 내용에 대 한 액세스 하지 있고 서비스 작업을 완료할 수 없습니다. 요청에 대 한 고객 승인 되 면 적시에 콘텐츠에 대 한 액세스는 고객의 모니터링 및 제한 된 관리 인터페이스를 통해 Microsoft 엔지니어 제한 됩니다. Lockbox 및 고객 Lockbox를 사용 하 여 모든 승인 된 액세스를 엔지니어 고객 데이터는 자신의 처리에 대 한 책임이 있는 요청을 고유 사용자에 게 추적할 수 있습니다.

## <a name="just-in-time-access"></a>적시에 액세스
Microsoft은 Office 365에 대 한 적시에 (JIT) 액세스 원칙을 사용 하 여 추가로 자격 증명 변조 및 바꾸기를 공격 위험을 완화 하기 위해 합니다. JIT은 서비스에 대 한 영구 관리 액세스를 제거 하 고 필요에 따라 이러한 역할에 상승 하는 기능에 이러한 권리를 바꿉니다. 관리자에서 영구 권한 제거를 통해 자격 증명 사용할 수 있고 경우에 이러한 필요한 자격 증명 도난의 경우에는 회사를 야기 되는 위험을 제거 합니다.

JIT 액세스 모델에는 상승 된 권한 관리 업무를 수행 하는 제한 된 기간에 대 한 요청에 따라 엔지니어 필요 합니다. 또한 OCEs 시스템에서 생성 된 복잡 한 암호를 사용 하 여 만든 임시 계정을 사용 하 고 필요한 작업을 수행 하도록 허용 하는 해당 역할을 부여 합니다. 예, Lockbox로 부여 되는 관리 액세스 시간 제한이 이며 액세스 권한을 부여 하는 시간 요청 되는 역할에 따라 달라 집니다. 엔지니어는 Lockbox 시스템을 요청 하는 동안 필요한 시간 액세스의 기간을 지정 합니다. Lockbox 시스템은 상승에 대 한 시간을 허용 하는 최대 요청 시간을 초과 하는 요청을 거부 합니다. 권한 상승 요청의 만료, 후 관리 액세스 제거 되며 임시 계정이 만료 됩니다.

권한이 부여 된 경우 (예: 시스템 디버그) 액세스에 대 한 승인 엔지니어는 상승 된 액세스에 대 한 요청을 승인 때마다 권한 부여 시스템에서 생성 되는 암호는 일회성 사용 관리를 받습니다. 메뉴 및 도구 모음을이 암호 안전한 암호는 엔지니어 값으로 복사 되 Microsoft 기업 환경에 대 한 자격 증명은 엔지니어와 별도로 관리자 권한으로 액세스 하는 작업에 대 한 승인 된 세션에 대해서만 유용 합니다.

## <a name="constrained-management-interfaces"></a>제한 된 관리 인터페이스
OCEs 두 관리 인터페이스를 사용 하 여 관리 작업을 수행 하려면: 보안된 터미널 서비스 게이트웨이 (Tsg) 및 원격 PowerShell을 통해 원격 데스크톱 합니다. 이러한 관리 내에서 다음과 같은 소프트웨어 정책 및 액세스 제어 명령을 실행할 수 있는 응용 프로그램에 대 한 중요 한 제한을 cmdlet를 배치 하는 인터페이스 수 있습니다. 

Office 365 서버에 대 한 세션 서비스 당 팀 관리자를 동시 세션 제한 서버당 합니다. Tsg는 단일 동시 세션에만 적용 하는 사용자에 대 한 허용 하도록 구성 하 고 여러 세션을 허용 하지 않습니다. Tsg은 Office 365 서비스 팀 관리자가 관리자가 자신의 의무를 효과적으로 수행할 수 있도록 서버당, 단일 세션을 사용 하 여 동시에 여러 서버에 연결 하도록 허용 합니다. 서비스 팀 관리자가 자신 Tsg에 사용 권한을 모두를 갖지 않습니다. TSG 다단계 인증 (MFA) 및 암호화 요구 사항을 적용 하려면만 사용 됩니다. 서비스 팀 관리자는 TSG 통해 특정 서버에 연결 되 면 관리자 당 하나의 세션 제한 특정 서버에 적용 됩니다.

사용 제한 및 Office 365 담당자에 대 한 연결 및 구성 요구 사항 Active Directory 그룹 정책에 의해 설정 됩니다. 이러한 정책은 다음과 같은 특징을 다음과 같습니다.
- Tsg은 [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2 유효성이 검사 된 암호화를 사용 하도록 구성 된
- TSG 세션 비활성 30 분 후의 연결을 해제 하도록 구성 된
- TSG 세션 구성 된 자동으로 로그 오프 24 시간 후

Tsg에 대 한 연결에는 별도 물리적 스마트 카드와 엔지니어의 Microsoft 회사 자격 증명에서 별도 계정을 사용 하 여 MFA도 필요 합니다. 엔지니어는 다양 한 플랫폼에 대 한 서로 다른 스마트 카드를 발급 하 고 비밀 관리 플랫폼 자격 증명의 보안 저장소를 확인 하는데 사용 됩니다. Tsg 제어 허용 된 세션 및 유휴 시간 제한 설정을 수가 원격 서버에 로그인 할 수 있는 Active Directory 그룹 정책을 사용 합니다. 추가 정책 응용 프로그램을 허용 하 고 인터넷 액세스를 제한 하는 액세스를 제한 하기 위해 적용에서 됩니다.

특수 하 게 구성 된 Tsg를 사용 하 여 원격 액세스 외에도 Exchange Online 사용자 서비스 엔지니어 작업 역할을 가진 액세스할 수 있도록 원격 PowerShell을 사용 하 여 프로덕션 서버의 특정 관리 기능입니다. 이 작업을 수행 하려면 사용자는 Office 365 프로덕션 환경에 대 한 읽기 전용 (디버그) 액세스에 대 한 권한이 부여 되어야 합니다. 권한 상승 Lockbox 프로세스를 사용 하 여 Tsg에 대해 사용 하도록 설정에 관계 없이 동일한 방식으로 활성화 됩니다.

원격 액세스에 대 한 액세스의 단일 지점으로 사용 하는 각 데이터 센터에 부하 분산 된 가상 IP를이 없습니다. 실행 될 수 있는 원격 PowerShell cmdlet에 대해 인증 하는 동안 얻은 사용 하 여 액세스 클레임에서 식별 된 권한 수준을 기반으로 합니다. 이러한 cmdlet는 액세스 하 고이 메서드를 사용 하 여 연결 하는 사용자가 실행할 수 있는 관리 기능입니다. 원격 PowerShell 엔지니어, Lockbox 프로세스를 통해 부여 된 액세스 수준에 따라이를 사용할 수 있는 명령의 범위를 제한 하는데 사용 됩니다. 등 Exchange Online에서 Get 사서함을 사용할 수 있습니다 하지만 Set-mailbox 설정 되지 않습니다.
