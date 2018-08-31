---
title: Office 365 암호화 위험 및 보호
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
description: '요약: Microsoft Office 365에서 데이터 복구를 이해 합니다.'
ms.openlocfilehash: 69956c5f32f74a93b2101d2651ef7de03ad1094f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534104"
---
# <a name="encryption-risks-and-protections"></a>암호화 위험 및 보호

Microsoft은 Office 365 서비스 및 고객 데이터를 위험에 중점을 두고는 통제 및 규정 준수 프레임 워크는 다음과 같습니다. Microsoft는 이러한 위험을 완화 하기 위해 다양 한 기술 및 프로세스 기반 메서드 (컨트롤 라고 함)를 구현 합니다. 식별, 평가 및 컨트롤을 통해 위험 완화 함으로써 연속 프로세스입니다. 시설, 네트워크, 서버, 응용 프로그램, 사용자 (예: Microsoft 관리자) 및 데이터와 같은 클라우드 서비스에 대 한 다양 한 계층 내에서 컨트롤의 구현 심층 방어 전략을 구성 합니다. 이 전략에 키는 많은 다른 컨트롤은 동일한 또는 이와 유사한 버전 위험 시나리오 보호 하기 위해 다양 한 계층에서 구현 됩니다. 컨트롤의 일부 오류로 실패 하는 경우이 다중 계층된 접근 방법 안전한 보호를 제공 합니다. 일부 위험이 있는 시나리오 및 완화 하는 현재 사용할 수 있는 암호화 기술 아래 나열 됩니다. 이러한 시나리오는 대부분의 경우 Office 365에서 구현 하는 다른 컨트롤을 통해 완화도 있습니다.

| 암호화 기술 | 서비스 | 키 관리 | 위험 시나리오 | 값 |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitLocker | Exchange Online, SharePoint Online, 및 비즈니스를 위한 Skype | Microsoft | 디스크 또는 Office 365의 서버 도난 또는 재활용 부적절 하 게 합니다. | BitLocker 도난 또는 부적절 하 게 재활용 하드웨어 (서버/디스크)으로 인해 데이터 손실 보호 하기 위해 안전한 방법을 제공 합니다. |
| 서비스 암호화 | SharePoint Online, 비즈니스, 용 Skype 및; 비즈니스용 OneDrive Exchange 온라인 (로드맵) | Microsoft | 내부 또는 외부 해커 blob으로 개별 파일/데이터에 액세스 하려고 시도 합니다. | 키에 액세스 하지 않고 암호화 된 데이터를 해독할 수 없습니다. 데이터에 액세스 하는 해커의 위험을 완화 하는데 도움이 됩니다. |
| 고객 키 | SharePoint Online, 비즈니스, Exchange Online, 및 Skype 비즈니스용 OneDrive | 고객 | N/A (이 기능은 규정 준수 기능으로, 모든 위험을 완화 방법으로 하지 않습니다.) | 내부 규정 준수 의무 및 Office 365 서비스를 그대로 유지 하 고 데이터에 대 한 Microsoft의 액세스를 해지 하는 기능을 충족 하는 고객 도움이 됩니다. |
| Office 365와 클라이언트 간의 TLS | Exchange Online, SharePoint Online, 비즈니스용 OneDrive, 비즈니스, 팀 및 Yammer 용 Skype | Microsoft에서는 고객 | 메시지 가로채기 중간 또는 다른 공격을 인터넷을 통해 Office 365와 클라이언트 컴퓨터 간의 데이터 흐름을 누릅니다. | 이 구현을 Microsoft 및 고객에 모두 값을 제공 하 고 Office 365와 클라이언트 사이 전달 데이터 무결성을 보장 합니다. |
| Microsoft 데이터 센터 간의 TLS | Exchange Online, SharePoint Online, 비즈니스용 OneDrive 및 비즈니스를 위한 Skype | Microsoft | 메시지 가로채기 중간 또는 다른 공격을 서로 다른 Microsoft 데이터 센터에 있는 Office 365 서버 간의 고객 데이터 흐름을 누릅니다. | 이 구현 하는 Microsoft 데이터 센터 간의 공격 으로부터 데이터를 보호 하기 위해 다른 방법입니다. |
| Azure 권한 관리 (Office 365 또는 Azure 정보 보호에 포함) | Exchange Online, SharePoint Online, 및 비즈니스용 OneDrive | 고객 | 데이터는 데이터에 대 한 액세스 권한이 없는 사용자의 전달에 속합니다. | Azure 정보 보호 암호화, id 및 권한 부여 정책 도움말 보안 파일 및 여러 장치에서 전자 메일을 사용 하 여 고객에 게 값을 제공 하는 Azure RMS를 사용 합니다. Azure RMS 같은 암호화할 로그 다른 받는 사람에 게 전송 하기 전에 (즉, 모든 전자 메일이 특정 주소로) 특정 조건에 일치 하는 Office 365에서 발생 한 모든 메일을 자동으로 수는 있습니다 고객에 게 값을 제공 합니다. |
| S/MIME | Exchange Online | 고객 | 전자 메일 받는 사람된에 게가 아닌 사용자의 전달에 속합니다. | S/MIME 고객에 게 전자 메일 S/MIME을 사용 하 여 암호화는 전자 메일의 직접 받는 사람이 해독할 수를 확인 하 여 값을 제공 합니다. |
| Office 365 메시지 암호화 | Exchange Online, SharePoint Online | 고객 | 제한 된 첨부 파일을 포함 하는 전자 메일 내에서 또는 Office 365 외부 전자 메일의 의도 한 수신자가 아닌 사용자의 전달에 속합니다. | OME (즉, 모든 전자 메일이 특정 주소로) 특정 조건에 일치 하는 Office 365에서 발생 한 모든 전자 로그 내부 간에 전송 하기 전에 암호화 자동으로 고객에 게 값을 제공 하거나 외부 받는 사람입니다. |
| 파트너 조직으로 SMTP TLS | Exchange Online | 고객 | 전자 메일에서 다른 파트너 조직에는 Office 365 테 넌 트에서 전송 하는 동안 메시지 가로채기 중간 또는 기타 공격을 통해 가로채 됩니다. | 이 시나리오 대로 수 보내기/받기 자신의 Office 365 테 넌 트 및 암호화 된 SMTP 채널 내 해당 파트너의 전자 메일 조직 간의 모든 전자 메일이 되도록 고객에 게 값을 제공 합니다. |

다음 표에서 Office 365 다중 테 넌 트 및 정부 클라우드 커뮤니티 환경에서 사용할 수 있는 암호화 기술 간단히 설명합니다.

| 암호화 기술 | 에 의해 구현 | 키 교환 알고리즘 및 보안 수준 | 키 관리 * | FIPS 140-2 유효성을 검사 |
|----------------------------------------------------------------------------------|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| BitLocker | Exchange Online | AES 128-비트 + | AES 외부 키에 비밀 안전 하 고 Exchange server의 레지스트리에 저장 됩니다. 비밀 Safe는 높은 수준의 권한 상승 및 승인 액세스 필요로 하는 보안된 저장소입니다. 액세스 요청 하 고만 Lockbox를 호출 하는 내부 도구를 사용 하 여 승인 수 있습니다. AES 외부 키가 서버에 있는 신뢰할 수 있는 플랫폼 모듈에도 저장 됩니다. 48 자리 숫자 암호를 Active Directory에 저장 하 고 Lockbox에 의해 보호 됩니다. | 256 AES를 사용 하는 서버에 대 한 예,-비트 * * |
|  | SharePoint Online | 256 비트 AES | AES 외부 키 비밀 안전에 저장 됩니다. 비밀 Safe는 높은 수준의 권한 상승 및 승인 액세스 필요로 하는 보안된 저장소입니다. 액세스 요청 하 고만 Lockbox를 호출 하는 내부 도구를 사용 하 여 승인 수 있습니다. AES 외부 키가 서버에 있는 신뢰할 수 있는 플랫폼 모듈에도 저장 됩니다. 48 자리 숫자 암호를 Active Directory에 저장 하 고 Lockbox에 의해 보호 됩니다. | 예 |
|  | 비즈니스용 Skype | 256 비트 AES | AES 외부 키 비밀 안전에 저장 됩니다. 비밀 Safe는 높은 수준의 권한 상승 및 승인 액세스 필요로 하는 보안된 저장소입니다. 액세스 요청 하 고만 Lockbox를 호출 하는 내부 도구를 사용 하 여 승인 수 있습니다. AES 외부 키가 서버에 있는 신뢰할 수 있는 플랫폼 모듈에도 저장 됩니다. 48 자리 숫자 암호를 Active Directory에 저장 하 고 Lockbox에 의해 보호 됩니다. | 예 |
| 서비스 암호화 | SharePoint Online | 256 비트 AES | 사용 하 고 blob가 암호화 키 SharePoint Online 콘텐츠 데이터베이스에 저장 됩니다. SharePoint Online 콘텐츠 데이터베이스는 데이터베이스 액세스 제어 및 보관 암호화로 보호 됩니다. 암호화는 TDE를 사용 하 여 Azure SQL 데이터베이스에서 수행 됩니다. SharePoint Online에 테 넌 트 수준이 아니라 서비스 수준에서 이러한 암호는. (마스터 키 이라고 함) 이러한 비밀 키 저장소 라는 별도 보안 저장소에 저장 됩니다. TDE 활성 데이터베이스 및 데이터베이스 백업 및 트랜잭션 로그의 나머지 부분에서 보안을 제공합니다. 선택적 키를 제공 하는 고객, Azure 키 볼트에 고객 키가 저장 하 고 서비스는 키를 사용 하 여 다음 파일 수준 키를 암호화 하는데 사용 되는 사이트 키를 암호화 하는데 사용 되는 테 넌 트 키를 암호화 하 합니다. 기본적으로, 고객 키를 제공 하는 경우 새 키 계층 구조 도입 됩니다. | 예 |
|  | 비즈니스용 Skype | 256 비트 AES | 데이터의 각 요소가 서로 다른 임의로 생성 된 256 비트 키를 사용 하 여 암호화 됩니다. 암호화 키도 회의 당 마스터 키로 암호화 되는 해당 메타 데이터 XML 파일에 저장 됩니다. 회의 당 마스터 키를 한번도 임의로 생성 됩니다. | 예 |
|  | Exchange Online | 256 비트 AES | 각 사서함 (고객 키를 사용 하는) 하는 경우 (로드맵)에 microsoft 또는 고객에 의해 제어 되는 암호화 키를 사용 하는 데이터 암호화 정책을 사용 하 여 암호화 됩니다. | 예 |
| Office 365와 클라이언트/파트너 간의 TLS | Exchange Online | [여러 암호화 제품군을 지 원하는 편의적 TLS](https://technet.microsoft.com/en-us/library/mt163898.aspx) | Exchange Online (outlook.office.com)에 대 한 TLS 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. | 예, 256 비트 암호화 강도 가진 TLS 1.2를 사용 하는 경우 |
|  |  |  | Exchange Online에 대 한 TLS 루트 인증서는 2048 비트 SHA1RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
|  | SharePoint Online | AES 256 TLS 1.2 | SharePoint Online에 대 한 TLS 인증서 (*. sharepoint.com)는 2048 비트 SHA256RSA 볼티모어 CyberTrust 루트에서 발급 한 인증서입니다. | 예 |
|  |  | [비즈니스용 OneDrive 및 SharePoint Online에서의 데이터 암호화](https://technet.microsoft.com/en-us/library/dn905447.aspx) | SharePoint Online에 대 한 TLS 루트 인증서는 2048 비트 SHA1RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
|  | 비즈니스용 Skype | [SIP 통신 및 PSOM 데이터 공유 세션에 대 한 TLS](https://support.office.com/article/Set-up-your-network-for-Skype-for-Business-Online-d21f89b0-3afc-432e-b735-036b2432fdbf) | 비즈니스를 위한 Skype에 대 한 TLS 인증서 (*. lync.com)는 2048 비트 SHA256RSA 볼티모어 CyberTrust 루트에서 발급 한 인증서입니다. | 예 |
|  |  |  | 비즈니스를 위한 Skype에 대 한 TLS 루트 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
|  | Microsoft Teams | AES 256 TLS 1.2 | Microsoft 팀의 (teams.microsoft.com, edge.skype.com)에 대 한 TLS 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. | 예 |
|  |  | [질문과 대답 (영문) Microsoft 팀의 – 하는 방법에 대 한 관리 지원](https://docs.microsoft.com/MicrosoftTeams/teams-overview) | Microsoft 팀에 대 한 TLS 루트 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
| Microsoft 데이터 센터 간의 TLS | 모든 Office 365 서비스 | AES 256 TLS 1.2 | Microsoft는 내부적으로 관리 하 고 배포 된 인증 기관을 사용 하 여 Microsoft 데이터 센터 간의 서버-서버 통신 합니다. | 예 |
|  |  | Secure Real-time Transport Protocol (SRTP) |  |  |
| Azure 권한 관리 (Office 365 또는 Azure 정보 보호에 포함) | Exchange Online | [암호화 모드 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10)), 업데이트 및 향상 된 RMS 암호화 구현을 지원합니다. 서명 및 암호화 및 s h A-256 RSA 2048 서명에 해시를 위한 지원합니다. | [Microsoft에서 관리](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)됩니다. | 예 |
|  | SharePoint Online | [암호화 모드 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10)), 업데이트 및 향상 된 RMS 암호화 구현을 지원합니다. 서명에 대 한 서명 및 암호화 및 s h A-256 RSA 2048을 지원합니다. | [Microsoft에서 관리 하는](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)기본 설정인; 또는 | 예 |
|  |  |  | Microsoft에서 관리 하는 키 하는 대신은 고객 관리 합니다. IT 관리 Azure 구독이 있는 조직 BYOK을 사용 하 고 추가 비용 없이 해당 사용법을 기록할 수 있습니다. 자세한 내용은 [직접 키를 가져올 구현 하려면](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)을 참조 하십시오. 이 구성에서 Thales Hsm 키를 보호 하기 위해 사용 됩니다. 자세한 내용은 [Thales Hsm 및 Azure RMS를](http://www.thales-esecurity.com/msrms/cloud)참조 하십시오. |  |
| S/MIME | Exchange Online | 암호화 메시지 구문 표준 1.5 (PKCS #7) | 고객 관리 되는 공용 키 인프라 배포에 따라 다릅니다. 키 관리는 고객에 의해 수행 됩니다 및 Microsoft을 전혀 서명 및 암호 해독에 사용 되는 개인 키에 액세스할 수 있습니다. | 예, 3DES 또는 AES256 보내는 메시지를 암호화 하도록 구성 하는 경우 |
| Office 365 메시지 암호화 | Exchange Online | Azure RMS ([암호화 모드 2](https://technet.microsoft.com/en-us/library/dn569290.aspx) -서명 및 암호화에 대 한 RSA 2048 및 s h A-256 서명에 대)와 동일 | Azure 정보 보호를 사용 하 여 해당 암호화 인프라도 합니다. 사용 되는 암호화 방법을 암호화 및 메시지를 암호 해독에 사용 되는 RMS 키를 가져올 위치에 따라 달라 집니다. | 예 |
| 파트너 조직으로 SMTP TLS | Exchange Online | AES 256 TLS 1.2 | Exchange Online (outlook.office.com)에 대 한 TLS 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. | 예, 256 비트 암호화 강도 가진 TLS 1.2를 사용 하는 경우 |
|  |  |  | Exchange Online에 대 한 TLS 루트 인증서는 2048 비트 SHA1RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |

**이 테이블에서 참조 되는 TLS 인증서는 미국 데이터 센터입니다. 미국 이외의 데이터 센터는 또한 2048 비트 SHA256RSA 인증서를 사용합니다.*

***Exchange Online 다중 테 넌 트 환경에서 대부분의 서버 bitlocker AES 256 비트 암호화와 함께 배포 되었습니다. AES 128 비트를 사용 하 여 서버 단계적으로 제거 되 고 됩니다.*

| 암호화 기술 | 에 의해 구현 | 키 교환 알고리즘 및 보안 수준 | 키 관리 * | FIPS 140-2 유효성을 검사 |
|---------------------------------------------|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| BitLocker | Exchange Online | 256 비트 AES | AES 외부 키에 비밀 안전 하 고 Exchange server의 레지스트리에 저장 됩니다. 비밀 Safe는 높은 수준의 권한 상승 및 승인 액세스 필요로 하는 보안된 저장소입니다. 액세스 요청 하 고만 Lockbox를 호출 하는 내부 도구를 사용 하 여 승인 수 있습니다. AES 외부 키가 서버에 있는 신뢰할 수 있는 플랫폼 모듈에도 저장 됩니다. 48 자리 숫자 암호를 Active Directory에 저장 하 고 Lockbox에 의해 보호 됩니다. | 예 |
|  | SharePoint Online | 256 비트 AES | AES 외부 키 비밀 안전에 저장 됩니다. 비밀 Safe는 높은 수준의 권한 상승 및 승인 액세스 필요로 하는 보안된 저장소입니다. 액세스 요청 하 고만 Lockbox를 호출 하는 내부 도구를 사용 하 여 승인 수 있습니다. AES 외부 키가 서버에 있는 신뢰할 수 있는 플랫폼 모듈에도 저장 됩니다. 48 자리 숫자 암호를 Active Directory에 저장 하 고 Lockbox에 의해 보호 됩니다. | 예 |
|  | 비즈니스용 Skype | 256 비트 AES | AES 외부 키 비밀 안전에 저장 됩니다. 비밀 Safe는 높은 수준의 권한 상승 및 승인 액세스 필요로 하는 보안된 저장소입니다. 액세스 요청 하 고만 Lockbox를 호출 하는 내부 도구를 사용 하 여 승인 수 있습니다. AES 외부 키가 서버에 있는 신뢰할 수 있는 플랫폼 모듈에도 저장 됩니다. 48 자리 숫자 암호를 Active Directory에 저장 하 고 Lockbox에 의해 보호 됩니다. | 예 |
| 서비스 암호화 | SharePoint Online | 256 비트 AES | 사용 하 고 blob가 암호화 키 SharePoint Online 콘텐츠 데이터베이스에 저장 됩니다. SharePoint Online 콘텐츠 데이터베이스는 데이터베이스 액세스 제어 및 보관 암호화로 보호 됩니다. 암호화는 TDE를 사용 하 여 Azure SQL 데이터베이스에서 수행 됩니다. SharePoint Online에 테 넌 트 수준이 아니라 서비스 수준에서 이러한 암호는. (마스터 키 이라고 함) 이러한 비밀 키 저장소 라는 별도 보안 저장소에 저장 됩니다. TDE 활성 데이터베이스 및 데이터베이스 백업 및 트랜잭션 로그의 나머지 부분에서 보안을 제공합니다. 선택적 키를 제공 하는 고객, Azure 키 볼트에 고객 키가 저장 하 고 서비스는 키를 사용 하 여 다음 파일 수준 키를 암호화 하는데 사용 되는 사이트 키를 암호화 하는데 사용 되는 테 넌 트 키를 암호화 하 합니다. 기본적으로, 고객 키를 제공 하는 경우 새 키 계층 구조 도입 됩니다. | 예 |
|  | 비즈니스용 Skype | 256 비트 AES | 데이터의 각 요소가 서로 다른 임의로 생성 된 256 비트 키를 사용 하 여 암호화 됩니다. 암호화 키도 회의 당 마스터 키로 암호화 되는 해당 메타 데이터 XML 파일에 저장 됩니다. 회의 당 마스터 키를 한번도 임의로 생성 됩니다. | 예 |
|  | Exchange Online | 256 비트 AES | 각 사서함 (고객 키를 사용 하는) 하는 경우 microsoft 또는 고객에 의해 제어 되는 암호화 키를 사용 하는 데이터 암호화 정책을 사용 하 여 암호화 됩니다. | 예 |
| Office 365와 클라이언트/파트너 간의 TLS | Exchange Online | [여러 암호화 제품군을 지 원하는 편의적 TLS](https://technet.microsoft.com/en-us/library/mt163898.aspx) | Exchange Online (outlook.office.com)에 대 한 TLS 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. | 예, 256 비트 암호화 강도 가진 TLS 1.2를 사용 하는 경우 |
|  |  |  | Exchange Online에 대 한 TLS 루트 인증서는 2048 비트 SHA1RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
|  | SharePoint Online | AES 256 TLS 1.2 | SharePoint Online에 대 한 TLS 인증서 (*. sharepoint.com)는 2048 비트 SHA256RSA 볼티모어 CyberTrust 루트에서 발급 한 인증서입니다. | 예 |
|  |  |  | SharePoint Online에 대 한 TLS 루트 인증서는 2048 비트 SHA1RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
|  | 비즈니스용 Skype | SIP 통신 및 PSOM 데이터 공유 세션에 대 한 TLS | 비즈니스를 위한 Skype에 대 한 TLS 인증서 (*. lync.com)는 2048 비트 SHA256RSA 볼티모어 CyberTrust 루트에서 발급 한 인증서입니다. | 예 |
|  |  |  | 비즈니스를 위한 Skype에 대 한 TLS 루트 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
|  | Microsoft Teams | [질문과 대답 (영문) Microsoft 팀의 – 하는 방법에 대 한 관리 지원](https://docs.microsoft.com/MicrosoftTeams/teams-overview) | Microsoft 팀의 (teams.microsoft.com; edge.skype.com)에 대 한 TLS 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. | 예 |
|  |  |  | Microsoft 팀에 대 한 TLS 루트 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
| Microsoft 데이터 센터 간의 TLS | Exchange Online, SharePoint Online, 비즈니스를 위한 Skype | AES 256 TLS 1.2 | Microsoft는 내부적으로 관리 하 고 배포 된 인증 기관을 사용 하 여 Microsoft 데이터 센터 간의 서버-서버 통신 합니다. | 예 |
|  |  | Secure Real-time Transport Protocol (SRTP) |  |  |
| Azure 권한 관리 서비스 | Exchange Online | [암호화 모드 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10)), 업데이트 및 향상 된 RMS 암호화 구현을 지원합니다. 서명 및 암호화 및 s h A-256 RSA 2048 서명에 해시를 위한 지원합니다. | [Microsoft에서 관리](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)됩니다. | 예 |
|  | SharePoint Online | [암호화 모드 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10)), 업데이트 및 향상 된 RMS 암호화 구현을 지원합니다. 서명 및 암호화 및 s h A-256 RSA 2048 서명에 해시를 위한 지원합니다. | [Microsoft에서 관리 하는](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)기본 설정인; 또는 | 예 |
|  |  |  | 고객 관리 (명시적 BYOK)은 Microsoft에서 관리 하는 키를 대신 합니다. IT 관리 Azure 구독이 있는 조직 BYOK을 사용 하 고 추가 비용 없이 해당 사용법을 기록할 수 있습니다. 자세한 내용은 [직접 키를 가져올 구현 하려면](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)을 참조 하십시오. |  |
|  |  |  | BYOK 시나리오에서는 Thales Hsm 키를 보호 하기 위해 사용 됩니다. 자세한 내용은 [Thales Hsm 및 Azure RMS를](http://www.thales-esecurity.com/msrms/cloud)참조 하십시오. |  |
| S/MIME | Exchange Online | 암호화 메시지 구문 표준 1.5 (PKCS #7) | 배포 하는 공용 키 인프라에 따라 다릅니다. | 예, 3DES 또는 AES 256 보내는 메시지를 암호화 하도록 구성 하는 경우입니다. |
| Office 365 메시지 암호화 | Exchange Online | Azure RMS ([암호화 모드 2](https://technet.microsoft.com/en-us/library/dn569290.aspx) -서명 및 암호화에 대 한 RSA 2048 및 서명에서 해시를 위한 s h A-256)와 동일 | Azure RMS 암호화 인프라로 사용합니다. 사용 되는 암호화 방법을 암호화 및 메시지를 암호 해독에 사용 되는 RMS 키를 가져올 위치에 따라 달라 집니다. | 예 |
|  |  |  | Microsoft Azure RMS 키 받기를 사용 하 여 암호화 모드 2 사용 됩니다. Active Directory (AD) RMS 키 받기를 사용 하 여 암호화 모드 1 또는 암호화 모드 2 중 하나만 사용 됩니다. 온-프레미스에 사용 하는 방법에 따라 달라 집니다 AD RMS 배포 합니다. 암호화 모드 1은 원래 AD RMS 암호화를 구현 합니다. RSA 1024 서명 및 암호화를 위한 지원 하 고 서명에 대 한 s h A-1을 지원 합니다. 이 모드 에서도 계속 Hsm을 사용 하는 BYOK 구성을 제외 하 고 RMS의 모든 현재 버전에서 지원 됩니다. |  |
| 파트너 조직으로 SMTP TLS | Exchange Online | AES 256 TLS 1.2 | Exchange Online (outlook.office.com)에 대 한 TLS 인증서는 2048 비트 SHA256RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. | 예 |
|  |  |  | Exchange Online에 대 한 TLS 루트 인증서는 2048 비트 sha1RSA 인증서 볼티모어 CyberTrust 루트에서 발급 합니다. |  |
|  |  |  | *보안상의 이유로 인증서 바뀌지 때때로 유의 합니다.* |  |

**이 테이블에서 참조 되는 TLS 인증서는 미국 데이터 센터입니다. 미국 이외의 데이터 센터는 또한 2048 비트 SHA256RSA 인증서를 사용합니다.*