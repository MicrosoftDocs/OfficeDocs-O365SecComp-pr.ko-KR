---
title: Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4cde0cda-3430-4dc0-b489-f2c0736c929f
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: Exchange Online 및 Office 365에서 TLS (전송 계층 보안)를 사용 하 여 전자 메일 통신의 보안을 유지 하는 방법을 알아봅니다. 또한 Exchange Online에 대해 Microsoft에서 발급 한 인증서에 대 한 정보도 확인 하세요.
ms.openlocfilehash: e80f477c807f3a7ad5f751e0987b191024c816d9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255636"
---
# <a name="how-exchange-online-uses-tls-to-secure-email-connections-in-office-365"></a>Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법

Exchange Online 및 Office 365에서 TLS (전송 계층 보안)를 사용 하 여 전자 메일 통신의 보안을 유지 하는 방법을 알아봅니다. 또한 Exchange Online용으로 Microsoft에서 발급한 인증서에 대한 정보도 제공합니다.
  
## <a name="tls-basics-for-office-365-and-exchange-online"></a>Office 365 및 Exchange Online에 대한 TLS 기본 사항

TLS(전송 계층 보안) 및 TLS 이전의 SSL은 보안 인증서를 사용하여 컴퓨터 간 연결을 암호화함으로써 네트워크를 통한 통신을 보호하는 암호화 프로토콜입니다. TLS는 ssl (Secure Sockets layer)을 대체 하며, 흔히 ssl 3.1이 라고도 합니다. exchange Online의 경우 TLS를 사용 하 여 exchange 서버와 exchange 서버 간의 연결과 온-프레미스 exchange 서버 또는 받는 사람의 메일 서버 간의 연결을 암호화 합니다. 연결이 암호화 되 면 해당 연결을 통해 전송 되는 모든 데이터는 암호화 된 채널을 통해 전송 됩니다. 그러나 TLS로 암호화 된 연결을 통해 전송 된 메시지를 전달 하는 경우 해당 메시지가 반드시 암호화 되지 않은 것입니다. 이는 단순한 용어로 TLS에서 메시지를 암호화 하지 않고 연결만을 사용 하기 때문입니다.
  
메시지를 암호화 하려면 메시지 콘텐츠를 암호화 하는 암호화 기술 (예: Office 메시지 암호화 등)을 사용 해야 합니다. office 365의 메시지 암호화 옵션에 대 한 자세한 내용은 office 365 및 [office 365 메시지 암호화 (OME)](ome.md) [의 전자 메일 암호화](email-encryption.md) 를 참조 하세요. 
  
Office 365와 온-프레미스 조직 또는 파트너와 같은 다른 조직 간에 보안 채널을 설정 하려는 경우에는 TLS를 사용 하는 것이 좋습니다. Exchange Online은 항상 tls를 사용 하 여 전자 메일을 보호 하지만 다른 당사자가 tls 보안을 제공 하지 않을 경우에는 항상이 작업을 수행할 수는 없습니다. *커넥터*를 사용 하 여 온-프레미스 서버 또는 중요 파트너에 게 모든 메일을 보호 하는 방법을 알아보려면 계속 읽어 보세요. 
  
## <a name="how-exchange-online-uses-tls-between-exchange-online-customers"></a>exchange online에서 exchange online 고객 간에 TLS를 사용 하는 방법

Exchange online 서버는 항상 TLS 1.2을 사용 하 여 데이터 센터의 다른 Exchange Online 서버에 대 한 연결을 암호화 합니다. Office 365 조직 내의 받는 사람에 게 메일을 보내면 해당 전자 메일은 TLS를 사용 하 여 암호화 된 연결을 통해 자동으로 전송 됩니다. 또한 다른 Office 365 고객에 게 보내는 모든 전자 메일은 TLS를 사용 하 여 암호화 되 고 전달 보안을 사용 하 여 보호 되는 연결을 통해 전송 됩니다.
  
## <a name="how-office-365-uses-tls-between-office-365-and-external-trusted-partners"></a>office 365이 office 365와 외부의 신뢰할 수 있는 파트너 간에 TLS를 사용 하는 방법

기본적으로 Exchange Online은 항상 oplocks TLS를 사용 합니다. 즉, Exchange Online은 항상 가장 안전한 TLS 버전을 사용 하 여 연결을 암호화 한 다음 두 당사자가 모두 동의할 수 있는 것을 찾을 때까지 tls 암호 목록에서 해당 방식으로 작동 합니다. 해당 받는 사람에 대 한 메시지가 안전한 연결을 통해서만 전송 되도록 Exchange Online을 구성 하지 않은 경우에는 받는 사람 조직에서 TLS 암호화를 지원 하지 않는 경우 기본적으로 메시지를 암호화 하지 않습니다. 대부분의 비즈니스에서 oplocks에 충분 합니다. 그러나 의료, 은행, 정부 조직과 같은 규정 준수 요구 사항이 있는 비즈니스의 경우에는 TLS를 요구 하거나 강제 적용 하도록 Exchange Online을 구성할 수 있습니다. 자세한 내용은 [Office 365에서 커넥터를 사용 하 여 메일 흐름 구성을](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx)참조 하세요.
  
조직과 트러스트 된 파트너 조직 간에 TLS를 구성 하기로 결정 한 경우 Exchange Online은 강제 TLS를 사용 하 여 신뢰할 수 있는 통신 채널을 만듭니다. 강제 TLS를 사용 하려면 파트너 조직이 보안 인증서를 사용 하 여 Exchange Online에서 인증을 받아야 사용자에 게 메일을 보낼 수 있습니다. 이 작업을 수행 하기 위해서는 파트너가 자체 인증서를 관리 해야 합니다. Exchange Online에서는 커넥터를 사용 하 여 받는 사람의 전자 메일 공급자에 게 도착 하기 전에 무단 액세스 로부터 보내는 메시지를 보호 합니다. 커넥터를 사용 하 여 메일 흐름을 구성 하는 방법에 대 한 내용은 [Office 365에서 커넥터를 사용 하 여 메일 흐름 구성을](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx)참조 하세요.
  
## <a name="tls-and-hybrid-exchange-server-deployments"></a>TLS 및 하이브리드 Exchange 서버 배포

하이브리드 exchange 배포를 관리 하는 경우에는 온-프레미스 exchange 서버에서 보안 인증서를 사용 하 여 office 365에서 인증 해야 사서함이 office 365에만 있는 받는 사람에 게 메일을 보낼 수 있습니다. 따라서 온-프레미스 Exchange 서버에 대 한 자체 보안 인증서를 관리 해야 합니다. 또한 이러한 서버 인증서를 안전 하 게 저장 하 고 유지 관리 해야 합니다. 하이브리드 배포에서 인증서를 관리 하는 방법에 대 한 자세한 내용은 [하이브리드 배포에 대 한 인증서 요구 사항을](https://technet.microsoft.com/library/hh563848%28v=exchg.150%29.aspx)참조 하세요.
  
## <a name="how-to-set-up-forced-tls-for-exchange-online-in-office-365"></a>Office 365에서 Exchange Online에 대해 강제 TLS를 설정 하는 방법

Exchange Online 고객의 경우 강제 tls가 전송 및 수신 전자 메일을 모두 보호 하려면 tls가 필요한 커넥터를 둘 이상 설정 해야 합니다. 사용자 사서함에 전송 되는 전자 메일에 대 한 커넥터와 사용자 사서함에서 보내는 전자 메일에 대 한 다른 커넥터를 사용 해야 합니다. Office 365의 Exchange 관리 센터에서 이러한 커넥터를 만듭니다. 자세한 내용은 [Office 365에서 커넥터를 사용 하 여 메일 흐름 구성을](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx)참조 하세요.
  
## <a name="tls-certificate-information-for-exchange-online"></a>Exchange Online에 대 한 TLS 인증서 정보

다음 표에는 Exchange Online에서 사용 되는 인증서 정보에 대 한 설명이 나와 있습니다. 비즈니스 파트너가 전자 메일 서버에서 강제 TLS를 설정 하는 경우에는이 정보를 해당 사용자에 게 제공 해야 합니다. 보안상의 이유로 인증서는 시간에 따라 변경 됩니다. microsoft는 데이터 센터 내에서 인증서에 대 한 업데이트를 롤업 했습니다. 새 인증서는 2018 년 9 월 3 일에서 유효 합니다.
  
 **현재 인증서 정보는 2018 년 9 월 3 일에서 유효 합니다.**
  
|**Attribute(특성)**|**값**|
|:-----|:-----|
|인증 기관 루트 발급자  <br/> |globalsign Root CA – R1 <br/> |
|인증서 이름  <br/> |mail.protection.outlook.com  <br/> |
|조직  <br/> |Microsoft Corporation  <br/> |
|조직 구성 단위  <br/> |  <br/> |
|인증서 키 강도  <br/> |2048  <br/> |
   
 **사용 되지 않는 인증서 정보는 2018 년 9 월 3 일까 지 유효 합니다.**
  
원활한 전환을 위해 계속 해 서 참조에 대 한 이전 인증서 정보를 제공 하는 것이 좋지만 지금은 현재 인증서 정보를 사용 해야 합니다.
  
****

|**Attribute(특성)**|**값**|
|:-----|:-----|
|인증 기관 루트 발급자  <br/> |Baltimore CyberTrust Root  <br/> |
|인증서 이름  <br/> |mail.protection.outlook.com  <br/> |
|조직  <br/> |Microsoft Corporation  <br/> |
|조직 구성 단위  <br/> |Microsoft Corporation  <br/> |
|인증서 키 강도  <br/> |2048  <br/> |
   
## <a name="prepare-for-the-new-exchange-online-certificate"></a>새 Exchange Online 인증서 준비

새 인증서는 Exchange Online에서 사용 하는 이전 인증서의 다른 CA (인증 기관)에서 발급 합니다. 따라서 새 인증서를 사용 하기 위해 몇 가지 작업을 수행 해야 할 수 있습니다.

새 인증서를 사용 하려면 인증서 유효성 검사의 일환으로 새 CA의 끝점에 연결 해야 합니다. 이렇게 하지 않으면 메일 흐름에 부정적인 영향을 줄 수 있습니다. 메일 서버를 특정 대상에만 연결 하도록 하는 방화벽을 사용 하 여 메일 서버를 보호 하는 경우 서버에서 새 인증서를 확인할 수 있는지 확인 해야 합니다. 서버에서 새 인증서를 사용할 수 있는지 확인 하려면 다음 단계를 완료 합니다.

1. Windows PowerShell을 사용 하 여 로컬 Exchange 서버에 연결한 후 다음 명령을 실행 합니다.  
  `certutil -URL http://crl.globalsign.com/gsorganizationvalsha2g3.crl`
2. 표시 된 창에서 **검색**을 선택 합니다.
3. 유틸리티가 확인을 완료 하면 상태를 반환 합니다. 상태에 **OK**가 표시 되 면 메일 서버에서 새 인증서의 유효성을 검사할 수 있습니다. 그렇지 않은 경우에는 연결이 실패 하는 원인을 확인 해야 합니다. 대개 방화벽 설정을 업데이트 해야 합니다. 액세스 해야 하는 끝점의 전체 목록은 다음과 같습니다.
    - ocsp.globalsign.com
     - crl.globalsign.com
     - secure.globalsign.com   

일반적으로 Windows Update를 통해 루트 인증서에 대 한 업데이트가 자동으로 수신 됩니다. 그러나 일부 배포에는 이러한 업데이트가 자동으로 수행 되지 않는 추가 보안이 적용 됩니다. Windows Update에서 루트 인증서를 자동으로 업데이트할 수 없는 이러한 잠겨진 배포에서는 다음 단계를 완료 하 여 올바른 루트 CA 인증서가 설치 되어 있는지 확인 해야 합니다.
1.  Windows PowerShell을 사용 하 여 로컬 Exchange 서버에 연결한 후 다음 명령을 실행 합니다.  
  `certmgr.msc`
2. **신뢰할 수 있는 루트 인증 기관/인증서**에서 새 인증서가 나열 되는지 확인 합니다.

## <a name="get-more-information-about-tls-and-office-365"></a>TLS 및 Office 365에 대 한 자세한 내용 보기

지원 되는 암호 제품군 목록은 [Office 365의 암호화에 대 한 기술 참조 세부 정보](technical-reference-details-about-encryption.md)를 참조 하세요.
  
[파트너 조직과의 보안 메일 흐름을 위한 커넥터 설정](https://technet.microsoft.com/library/dn751021%28v=exchg.150%29.aspx)
  
[전자 메일 보안이 강화 된 커넥터](https://technet.microsoft.com/library/261d92e4-7371-4555-b781-2062b5bb5278.aspx)
  
[Office 365의 암호화](encryption.md)
  

