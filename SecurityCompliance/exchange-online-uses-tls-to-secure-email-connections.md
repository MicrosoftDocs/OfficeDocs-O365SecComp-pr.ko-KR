---
title: Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 4cde0cda-3430-4dc0-b489-f2c0736c929f
description: 어떻게 Exchange Online 및 Office 365를 사용 하 여 전송 계층 보안 (TLS) 및 앞으로 완전 보안 (FS) 보안 전자 메일 통신에 알아봅니다. Exchange Online에 대 한 Microsoft에서 발급 한 인증서에 대 한 정보를 얻을 수도 있습니다.
ms.openlocfilehash: 079a6f574838f5710dbbbcb53726799abfae1d3a
ms.sourcegitcommit: ddfa0ac1f8ef95a78dcc1468241ef29363d56b5b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2018
ms.locfileid: "23520147"
---
# <a name="how-exchange-online-uses-tls-to-secure-email-connections-in-office-365"></a>Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법

어떻게 Exchange Online 및 Office 365를 사용 하 여 전송 계층 보안 (TLS) 및 앞으로 완전 보안 (FS) 보안 전자 메일 통신에 알아봅니다. 또한 Exchange Online에 대 한 Microsoft에서 발급 한 인증서에 대 한 정보를 제공 합니다.
  
## <a name="tls-basics-for-office-365-and-exchange-online"></a>Office 365 및 Exchange Online에 대한 TLS 기본 사항

전송 계층 보안 (TLS) 및 TLS를 하기 전에 있었던 SSL 하는 컴퓨터 간의 연결을 암호화 하려면 보안 인증서를 사용 하 여 네트워크를 통해 통신을 보호 하는 암호화 프로토콜. TLS Secure Sockets Layer (SSL)를 대체 하 고 SSL 3.1 이라고 합니다. Exchange Online에 대 한 명의 Exchange 서버와 온-프레미스 Exchange 서버 또는 받는 사람의 메일 서버와 같은 다른 서버 간의 명의 Exchange 서버와 연결 간의 연결을 암호화 하 TLS 사용 합니다. 연결 암호화 되 면 해당 연결을 통해 전송 되는 모든 데이터는 암호화 된 채널을 통해 전송 됩니다. 그러나 TLS 암호화 된 연결을 통해 전송 된 메시지를 전달 하는 경우에 해당 메시지 암호화 반드시 되지 않습니다. 이 때문 간단한 용어로 TLS 연결만 메시지를 암호화 하지 않습니다.
  
I메시지를 암호화하려는 경우 메시지 콘텐츠를 암호화하는 암호화 기술을 사용해야 합니다(예: Office Message Encryption). Office 365에서 메시지 암호화 옵션에 대한 내용은 [Email encryption in Office 365](email-encryption.md) 및 [Office 365 Message Encryption (OME)](ome.md)를 참조하세요. 
  
Office 365 및 온-프레미스 조직 또는 파트너 등의 다른 조직 사이 대응의 보안 채널 설정 하려는 경우에 TLS를 사용 하는 것이 좋습니다. Exchange Online 항상 전자 메일 보호 하기 위해 먼저 TLS를 사용 하 여 시도 있지만 수는 없습니다 항상이 경우 다른 당사자는 TLS 보안을 제공 하지 않습니다. *커넥터*를 사용 하 여 온-프레미스 서버 또는 중요 한 파트너에 대 한 모든 메일을 보호할 수는 방법을 알아보려면 읽기를 유지 합니다. 
  
## <a name="how-exchange-online-uses-tls-between-exchange-online-customers"></a>Exchange Online에서 Exchange Online 고객 간에 TLS를 사용하는 방법

Exchange Online 서버는 항상 TLS 1.2로 데이터 센터의 다른 Exchange Online 서버에 대한 연결을 암호화합니다. Office 365 조직 내에 있는 받는 사람에게 메일을 보낼 때 TLS를 사용하여 암호화된 연결을 통해 전자 메일이 자동으로 전송됩니다. 또한 다른 Office 365 고객에게 보내는 모든 전자 메일은 TLS를 사용하여 암호화되고 FS(Forward Secrecy)를 사용하여 보안되는 연결을 통해 전송됩니다.
  
## <a name="how-office-365-uses-tls-between-office-365-and-external-trusted-partners"></a>Office 365에서 Office 365와 외부, 신뢰할 수 있는 파트너 간의 TLS를 사용 하는 방법

기본적으로 Exchange Online 항상 사용 편의적 TLS 됩니다. 즉, Exchange Online 항상 TLS의 가장 안전한 버전와의 연결을 먼저 암호화 하려고 한 다음의 두 당사자 동의할 수 하나를 찾을 때까지 해당 방법을 사용 하 여 목록에서 아래로 TLS 암호화의 작동 합니다. 전송 확인 하는 메시지를 받는 사람에 게는 보안 연결을 통해 Exchange Online 구성 하지 않으면 다음 기본적으로 메시지 전송 됩니다 암호화 되지 않은 경우 받는 사람 조직에서 TLS 암호화를 지원 하지 않습니다. 편의적 TLS는 대부분의 기업에 대 한 충분 한입니다. 그러나 의료 등 규정 준수 요구 사항을, 금융, 또는 정부 조직에 있는 회사에 대 한 Exchange Online을 요구 하도록 구성 하거나 강제로, TLS 수 있습니다. 자세한 내용은 [Office 365의 커넥터를 사용 하 여 구성을 메일 흐름](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx)을 참조 하십시오.
  
조직 및 신뢰할 수 있는 파트너 조직 간의 TLS를 구성 하려는 경우 Exchange Online TLS를 사용할 수 강제 적용 된 통신의 신뢰할 수 있는 채널을 만들 수 있습니다. 강제 적용 된 TLS 파트너 조직에 인증 하려면 Exchange Online 보안 인증서를 포함 한 메일을 보낼 하기 위해 필요 합니다. 파트너는이 작업을 수행 하기 위해 자신의 인증서를 관리 해야 합니다. Exchange Online에서 받는 사람의 전자 메일 공급자에 도착 하기 전에 무단으로 액세스에서 보내는 메시지를 보호 하기 위해 커넥터 사용 합니다. 커넥터를 사용 하 여 메일 흐름을 구성 하는 내용은 [Office 365의 커넥터를 사용 하 여 구성을 메일 흐름](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx)을 참조 하십시오.
  
## <a name="tls-and-hybrid-exchange-server-deployments"></a>TLS 및 하이브리드 Exchange 서버 배포

하이브리드 Exchange 배포를 관리 하는 경우 Office 365에만 사서함 받는 사람에 게 메일을 전송 하기 위해 보안 인증서를 사용 하 여 Office 365에 인증 하는 온-프레미스 Exchange 서버 요구 됩니다. 따라서 온-프레미스 Exchange 서버에 대 한 고유한 보안 인증서를 관리 해야 합니다. 또한 안전 하 게 저장 하 고 이러한 서버 인증서를 유지 관리 해야 합니다. 하이브리드 배포에서 인증서를 관리 하는 방법에 대 한 자세한 내용은 [하이브리드 배포에 대 한 인증서 요구 사항](https://technet.microsoft.com/library/hh563848%28v=exchg.150%29.aspx)을 참조 하십시오.
  
## <a name="how-to-set-up-forced-tls-for-exchange-online-in-office-365"></a>Office 365에서 Exchange Online에 강제 적용된 TLS를 설정하는 방법

Exchange Online 고객을 위한 작동 하도록 강제 적용 된 TLS에 대 한 순서 대로 모든 보내고 받은 전자 메일을 보호 하기 위해 해야 TLS 필요로 하는 둘 이상의 커넥터를 설정 합니다. 사용자 사서함 및 사용자 사서함에서 보낸 전자 메일에 대 한 다른 커넥터에 보낸 전자 메일에 대 한 연결선을 한 필요 합니다. Office 365의 Exchange 관리 센터에서 이러한 커넥터를 만듭니다. 자세한 내용은 [Office 365의 커넥터를 사용 하 여 구성을 메일 흐름](https://technet.microsoft.com/library/ms.exch.eac.connectorselection%28v=exchg.150%29.aspx)을 참조 하십시오.
  
## <a name="tls-certificate-information-for-exchange-online"></a>Exchange Online에 대한 TLS 인증서 정보

Exchange Online에서 사용 되는 인증서 정보는 다음 표에 설명 되어있습니다. 비즈니스 파트너는 자신의 전자 메일 서버에서 TLS를 강제 적용된을 설정 하는 경우에 자신에 게이 정보를 제공 해야 합니다. 보안상의 이유로 인증서 바뀌지 때때로 유의 합니다. 데이터 센터 내에서 인증서에 대 한 업데이트 롤아웃가 우리 합니다. 새 인증서 2018 년 9 월 3에서 유효합니다.
  
 **현재 2018 년 9 월 3에서 유효한 인증서 정보**
  
|**Attribute(특성)**|**값**|
|:-----|:-----|
|인증 기관 루트 발급자  <br/> |GlobalSign 루트 CA-R1 <br/> |
|인증서 이름  <br/> |mail.protection.outlook.com  <br/> |
|조직  <br/> |Microsoft Corporation  <br/> |
|조직 구성 단위  <br/> |  <br/> |
|인증서 키 강도  <br/> |2048  <br/> |
   
 **유효 종료 2018 년 9 월 3을 사용 하지 않는 인증서 정보**
  
그러나을 원활 하 게 전환을 보장 하기 위해 일정 시간 동안 참조할 수 있도록 이전 인증서 정보를 제공 하려면 계속 될 예정 지금부터 현재 인증서 정보를 사용 해야 합니다.
  
****

|**Attribute(특성)**|**값**|
|:-----|:-----|
|인증 기관 루트 발급자  <br/> |Baltimore CyberTrust Root  <br/> |
|인증서 이름  <br/> |mail.protection.outlook.com  <br/> |
|조직  <br/> |Microsoft Corporation  <br/> |
|조직 구성 단위  <br/> |Microsoft Corporation  <br/> |
|인증서 키 강도  <br/> |2048  <br/> |
   
## <a name="prepare-for-the-new-exchange-online-certificate"></a>새 Exchange Online 인증서에 대 한 준비

새 인증서는 Exchange Online에서 사용 되는 이전 인증서에서 서로 다른 인증 기관 (CA)에서 발급 됩니다. 결과적으로, 새 인증서를 사용 하기 위해 일부 작업을 수행 해야할 수 있습니다.

새 인증서 유효성을 검사 하는 인증서의 일부로 새 CA의 끝점에 연결 해야 합니다. 이렇게 하려면 부정적인 영향을 받지 메일 흐름 될 수 있습니다. 메일 서버 수만 있도록 방화벽이 있는 서버에 특정 대상으로 연결 하 여 메일을 보호 하는 경우 서버에 새 인증서의 유효성을 검사 수 인지 여부를 확인 해야 합니다. 서버에 새 인증서를 사용할 수 있는지를 확인 하려면 다음이 단계를 완료 합니다.

1. Windows PowerShell을 사용 하 여 로컬 Exchange 서버에 연결 하 고 다음 명령을 실행 합니다.  
  `certutil -URL http://crl.globalsign.com/gsorganizationvalsha2g3.crl`
2. 표시 되는 창에서 **검색**을 선택 합니다.
3. 이 유틸리티에는 해당 검사 완료 되 면 상태를 반환 합니다. 상태 **확인**를 표시 하는 경우 메일 서버에는 새 인증서 성공적으로 확인할 수 있습니다. 그렇지 않은 경우에 실패에 대 한 연결에 영향을 주는 원인을 확인 해야 합니다. 대부분의 경우, 방화벽의 설정을 업데이트 해야 합니다. 액세스 해야하는 끝점의 전체 목록은 다음과 같습니다.
    - ocsp.globalsign.com
     - crl.globalsign.com
     - secure.globalsign.com   

일반적으로 Windows Update를 통해 자동으로 루트 인증서로 업데이트를 수신 합니다. 그러나 일부 배포 전체 이러한 업데이트가 자동으로 발생 하는 것을 금지 하는 추가적인 보안은 있습니다. Windows Update 수 없는 자동으로 업데이트할 수 없는 루트 인증서의 이러한 잠겨있는 배포에서는 이러한 단계를 완료 하 여 올바른 루트 CA 인증서가 설치 되었는지 확인 해야 합니다.
1.  Windows PowerShell을 사용 하 여 로컬 Exchange 서버에 연결 하 고 다음 명령을 실행 합니다.  
  `certmgr.msc`
2. **신뢰할 수 있는 루트 인증 기관/인증서**새 인증서가 표시 되는지 확인 합니다.

## <a name="get-more-information-about-tls-and-office-365"></a>TLS 및 Office 365에 대한 자세한 정보 얻기

지원 되는 암호 제품군 목록은 [Office 365의 암호화에 대 한 자세한 내용은 기술 참조 (영문)을](technical-reference-details-about-encryption.md)참조 하십시오.
  
[파트너 조직과의 보안 메일 흐름을 위한 커넥터 설정](https://technet.microsoft.com/library/dn751021%28v=exchg.150%29.aspx)
  
[향상 된 전자 메일 보안을 사용 하 여 연결선](https://technet.microsoft.com/library/261d92e4-7371-4555-b781-2062b5bb5278.aspx)
  
[Office 365의 암호화](encryption.md)
  

