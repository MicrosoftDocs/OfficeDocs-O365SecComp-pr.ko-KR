---
title: Office 365 고객 관리 되는 암호화 기능
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
ms.openlocfilehash: e835587e07246154cd700555cc7263370bde8755
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532908"
---
# <a name="customer-managed-encryption-features-in-office-365"></a>Office 365의 고객 관리 되는 암호화 기능

Microsoft에서 관리 하는 Office 365의 암호화 기술와 함께 Office 365도를 관리 하 고 다음과 같이 구성 하는 추가 암호화 기술과 함께 작동 합니다.
- [Azure 권한 관리](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms)
- [Multipurpose Internet Mail 확장 보안](http://blogs.technet.com/b/exchange/archive/2014/12/15/how-to-configure-s-mime-in-office-365.aspx)
- [Office 365 메시지 암호화](http://products.office.com/en-us/exchange/office-365-message-encryption)
- [파트너 조직의 보안 메일 흐름](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-for-secure-mail-flow-with-a-partner)

[Office 365 서비스 설명](https://technet.microsoft.com/en-us/library/office-365-service-descriptions.aspx)에 이러한 기술에 대 한 추가 정보를 확인할 수도 있습니다.

## <a name="azure-rights-management"></a>Azure 권한 관리
[Azure 권한 관리](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms) Azure RMS ()는 [Azure 정보 보호](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection)에서 사용 하는 보호 기술입니다. 암호화, id 및 권한 부여 정책 보호 하 여 파일 여러 플랫폼 및 장치에서 전자 메일을 사용 하 여-전화, 태블릿 및 Pc. 정보를 보호할 수 내부 및 외부 조직 보호 전적 하기 때문에 데이터입니다. Azure RMS 모든 파일 형식의 영구 보호 기능을 제공 하 고 보호 하는 모든 곳에 파일, 기업 간 공동 작업 및 전체 Windows 범위 및 비 Windows 장치를 지원 합니다. Azure RMS 보호 [데이터 손실 방지 (DLP) 정책](https://docs.microsoft.com/exchange/security-and-compliance/data-loss-prevention/data-loss-prevention)확대 수도 있습니다. 자세한 하는 방법에 대 한 응용 프로그램 및 서비스 사용할 수 있는 정보는 Azure 권한 관리 서비스에서 Azure 정보 보호, [응용 프로그램에서 Azure 권한 관리 서비스를 지원 하는 방법](https://docs.microsoft.com/information-protection/understand-explore/applications-support)을 참조 하십시오.

Azure RMS에는 Office 365와 통합 하 고 모든 Office 365 고객에 게 사용할 수는 있습니다. Azure RMS를 사용 하 여 Office 365를 구성 하려면을 참조 [Azure 권한 관리 및 집합을 사용 하 여 IRM 구성 SharePoint 관리 센터에서 정보 권한 관리 (IRM) 위로](https://technet.microsoft.com/en-us/library/dn151475(v=exchg.150).aspx)합니다. 온-프레미스 Active Directory (AD) RMS 서버를 작동 이면도 수 [온-프레미스를 사용 하도록 IRM 구성 AD RMS 서버](https://docs.microsoft.com/office365/SecurityCompliance/configure-irm-to-use-an-on-premises-ad-rms-server), 좋습니다 하면 다른 보안 공동 작업의 새로운 기능을 사용 하 여 [Azure RMS로 마이그레이션할](https://docs.microsoft.com/azure/information-protection/migrate-from-ad-rms-to-azure-rms) 수 있지만 조직입니다.

Azure RMS를 사용 하 여 고객 데이터를 보호 하는 경우 Azure RMS 2048 비트 RSA 비대칭 키 무결성을 위해 s h A-256 해시 알고리즘으로 사용 하 여 데이터를 암호화 합니다. Office 문서 및 전자 메일에 대 한 대칭 키는 AES 128 비트 (PKCS #7 안쪽 여백을 사용 하 여 CBC 모드)입니다. 각 문서 또는 Azure RMS로 보호 되는 전자 메일에 대 한 Azure RMS는 단일 AES 키 ("콘텐츠")를 만들고 해당 키는 문서에 포함 될 수 있으며 문서 버전을 통해 지속 합니다. 다음은 문서의 정책의 일부로 콘텐츠 키가 조직의 RSA 키 ("Azure 정보 보호 테 넌 트 키")로 보호 되 하 고 문서의 만든이가 정책에도 서명 합니다. 이 테 넌 트 키가 있는 모든 문서와 조직에 대 한 Azure RMS에 의해 보호 되는 전자 메일에 공통적으로 하 고 조직에는 고객 관리 되는 테 넌 트 키를 사용 하는 경우이 키 Azure 정보 보호 관리자가 변경할만 있습니다. Azure RMS에서 사용 하는 암호화 컨트롤에 대 한 자세한 내용은 참조 [어떻게 Azure RMS 작동 합니까? 세부 정보](https://docs.microsoft.com/information-protection/understand-explore/how-does-it-work)합니다.

기본 Azure RMS 구현에서 Microsoft를 생성 하 고 있는 각 테 넌 트에 대해 고유한 루트 키를 관리 합니다. 고객 [가져올 사용자 고유의 키 (BYOK)](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key) 라는 키 관리 메서드를 사용 하 여 Azure 키 추적용 서비스와 함께 Azure RMS에서 자신의 루트 키의 수명 주기를 관리할 수) 온-프레미스 Hsm에서 사용자의 키를 생성 한 후이 키의 컨트롤의 상태를 유지 하는 수 있게 해 주는 Microsoft의 FIPS 140-2 수준 2-유효성을 검사 Hsm.에 대 한 액세스 루트 키 전송 키를 내보낼 or 보호 하는 하드웨어 보안 모듈에서 추출한 없습니다로 모든 직원에 게 제공 되지 않습니다. 또한 언제 든 지 루트 키에 대 한 모든 액세스를 표시 하는 거의 실시간 로그를 액세스할 수 있습니다. 자세한 내용은 [로깅 및 Azure 권한 관리 사용 현황 분석](https://docs.microsoft.com/azure/information-protection/log-analyze-usage)을 참조 하십시오.

Azure 권한 관리를 통해 wire-tapping, 메시지 가로채기 중간 공격, 데이터 도난 및 조직 공유 정책 위반 하는 의도 하지 않은 예: 위협을 완화 합니다. 같은 시간에 전송에서 고객 데이터의 불필요 한 모든 액세스 또는 뒤에 잘못 된에 참가 하는 해당 데이터의 위험을 완화 함으로써 데이터 중 하나를 전달 하는 정책을 통해 금지는 적절 한 사용 권한을 갖고 있지 않은 권한이 없는 사용자가 보관 또는 모른 데이터 손실 방지 기능을 제공 하 고 있습니다. Azure 정보 보호의 일부분으로 사용 하는 경우 Azure RMS 제공 데이터 분류 하 고 기능, 콘텐츠 표시, 문서 액세스 추적 및 액세스 해지 기능에 레이블을 지정 합니다. 이러한 기능에 대 한 자세한 내용은 [Azure 정보 보호 이란](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection), [Azure 정보 보호 배포 로드맵](https://docs.microsoft.com/information-protection/plan-design/deployment-roadmap)및 [Azure 정보 보호를 위한 빠른 시작 자습서](https://docs.microsoft.com/information-protection/get-started/infoprotect-quick-start-tutorial)를 참조 하십시오.

## <a name="secure-multipurpose-internet-mail-extension"></a>Multipurpose Internet Mail 확장 보안
Secure/Multipurpose Internet Mail Extensions (S/MIME)는 공개 키 암호화 및 MIME 데이터의 디지털 서명에 대 한 표준입니다. S/MIME 3370, Rfc 3369에 정의 된 3850, 3851, 다른 사용자에 게 하 고 있습니다. 사용자를 전자 메일을 암호화 하 고 전자 메일에 디지털 서명 수 있습니다. S/MIME을 사용 하 여 암호화 된 전자 메일만 해당 받는 사람에 게 사용할 수 있는 개인 키를 사용 하 여 전자 메일의 받는 사람이 해독할 수만 있습니다. 이와 같이 전자 메일은 전자 메일의 받는 사람 이외의 누구나 해독할 수 없습니다.

[Microsoft Office 365에서 S/MIME을 지원](http://blogs.technet.com/b/exchange/archive/2014/12/15/how-to-configure-s-mime-in-office-365.aspx)합니다. 공용 인증서는 고객의 온-프레미스 Active Directory에 게 배포 하 고는 Office 365 테 넌 트에 복제할 수 있는 특성에 저장 합니다. 공용 키에 해당 하는 개인 키 온-프레미스를 유지 하 고 Office 365로 전송 되지 않으므로 됩니다. 사용자 수는 작성, 암호화, 암호를 해독, 읽기, 및 Outlook, 웹 및 Exchange ActiveSync 클라이언트에서 Outlook을 사용 하 여 조직에서 두 사용자 간에 전자 메일에 디지털 서명 합니다. 자세한 내용은 [Office 365에서 이제 S/MIME 암호화](http://blogs.office.com/2014/02/26/smime-encryption-now-in-office-365/)를 참조 하십시오.

## <a name="office-365-message-encryption"></a>Office 365 메시지 암호화
[Office 365 메시지 암호화](https://products.office.com/en-us/exchange/office-365-message-encryption) (OME) 암호화를 보낼 수 있습니다 하 고 모든 사용자에 게 권한으로 보호 된 메일 [Azure 정보 보호](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection) (AIP) 사용 하면 기반으로 구축 됩니다. OME는 wire-tapping 및 메시지 가로채기 중간 공격 같은 위협 및 불필요 한 적절 한 사용 권한을 갖고 있지 않은 권한이 없는 사용자가 데이터 액세스와 같은 기타 위험을 완화 합니다. Azure 정보 보호 위쪽에 구축 된 간단 하 고, 더 직관적 안전한 전자 메일 경험을 제공 하는 투자를 해 왔습니다. 내부 또는 조직 외부 사람에 게 Office 365에서 보낸 메시지를 보호할 수 있습니다. Azure Active Directory, Microsoft 계정 및 Google Id를 포함 하 여 모든 id를 사용 하 여 메일 클라이언트의 집합에서 다양 한 이러한 메시지를 볼 수 있습니다. 조직 암호화 된 메시지를 사용 하는 방법에 대 한 자세한 내용은 [Office 365 메시지 암호화](https://support.office.com/article/F87CB016-7876-4317-AE3C-9169B311FF8A)를 참조 하십시오.

## <a name="transport-layer-security"></a>전송 계층 보안
파트너와의 보안 통신을 확인 하려는 경우에 보안 및 메시지 무결성 제공 인바운드 및 아웃 바운드 커넥터를 사용할 수 있습니다. 인증서를 사용 하 여 각 커넥터에서 인바운드 및 아웃 바운드 TLS를 강제 적용된을 구성할 수 있습니다. 암호화 된 SMTP 채널을 사용 하는 메시지 가로채기 중간 공격을 통해 도난 으로부터 데이터를 방지할 수 있습니다. 자세한 내용은 [보안 전자 메일 연결에 TLS를 사용 하 여 어떻게 Exchange Online](https://support.office.com/article/How-Exchange-Online-uses-TLS-to-secure-email-connections-in-Office-365-4CDE0CDA-3430-4DC0-B489-F2C0736C929F)을 참조 하십시오.

## <a name="domain-keys-identified-mail"></a>도메인 키 메일 식별
Exchange Online Protection (EOP) 및 Exchange Online 도메인 키 식별 된 메일 (DKIM) 메시지의 인바운드 유효성 검사를 지원 합니다. DKIM은에서 시작 됨이 표시 되는 도메인에서 보낸 메시지를 하 고 다른 사용자에 의해 하지 위장 된의 유효성을 검사 하는 방법입니다. 전자 메일 메시지를 전송 하는 일을 담당 하는 조직에 연결 하 고 전자 메일 암호화의 더 큰 패러다임의 일부입니다. 이 패러다임의 세 부분에 대 한 자세한 내용은 다음을 참조 합니다.
- [스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)
- [DKIM를 사용 하 여 Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하려면](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)
- [DMARC를 사용 하 여 Office 365의 전자 메일의 유효성을 검사 하려면](https://https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)
