---
title: Office 365의 암호화에 대한 기술 참조 세부 정보
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 862cbe93-4268-4ef9-ba79-277545ecf221
description: Office 365의 암호화에 대 한 기술 세부 정보를 봅니다.
ms.openlocfilehash: 69365b66479ab89a9c036fe489b4087d327460eb
ms.sourcegitcommit: e4ebef6aaf756eefb86c9f3a602cf75f5d344271
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026525"
---
# <a name="technical-reference-details-about-encryption-in-office-365"></a>Office 365의 암호화에 대한 기술 참조 세부 정보

[Office 365의 암호화](encryption.md)에 사용 되는 암호화 제품군 인증서, 기술 및 TLS 하는 방법에 대 한 내용은이 문서를 참조 하십시오. 이 문서는 또한 계획 된 사용이 중단 된 하는 방법에 대 한 세부 정보를 제공합니다.
  
- 개요 정보를 찾고 하는 경우 [Office 365에서 암호화](encryption.md)를 참조 하십시오.
    
- 설치 정보를 찾고 하는 경우에 [Office 365 Enterprise의 암호화 설정](set-up-encryption.md)참조 하십시오.
    
## <a name="microsoft-office-365-certificate-ownership-and-management"></a>Microsoft Office 365 인증서 소유권 및 관리

Microsoft는 자체 인증서를 사용하므로 Office 365에 대한 인증서를 구입하거나 유지 관리할 필요가 없습니다.
  
## <a name="current-encryption-standards-and-planned-deprecations"></a>현재 암호화 표준 및 계획 된 사용이 중단 된

Office 365에 대 한 최고의에서 암호화를 제공 하려면 계속 하기 위해 Microsoft는 지원 되는 암호화 표준 정기적으로 검토 합니다. 경우에 따라 오래 및 보안 수준이 낮습니다 따라서 계속 이전 표준을 사용 중지 해야 합니다. 이 항목에서는 계획 된 사용이 중단 된 하는 방법에 대 한 현재 지원 되는 암호 제품군 및 기타 표준으로 세부 정보를 설명 합니다.
  
## <a name="versions-of-tls-supported-by-office-365"></a>Office 365에서 지원하는 TLS 버전

TLS(전송 계층 보안) 및 TLS 이전의 SSL은 보안 인증서를 사용하여 컴퓨터 간 연결을 암호화함으로써 네트워크를 통한 통신을 보호하는 암호화 프로토콜입니다. Office 365에서는 다음을 비롯한 여러 TLS 버전을 지원합니다.
  
- TLS 버전 1.2(TLS 1.2)
    
- TLS 버전 1.1(TLS 1.1)
    
- TLS 버전 1.0(TLS 1.0)
    
 TLS 1.0 및 TLS 1.1 지원 2018 년 10 월 31, 되지 것입니다. 자세한 내용은 [TLS 1.0 및 1.1 하면이 의미에 대 한 Deprecating 지원을](technical-reference-details-about-encryption.md#TLS11and12deprecation) 참조 하십시오. 
  
## <a name="deprecating-support-for-tls-10-and-11-and-what-this-means-for-you"></a>TLS 1.0 및 1.1 하면이 의미에 대 한 지원을 삭제 합니다.
<a name="TLS11and12deprecation"> </a>

Office 365가 2018, 10 월 31 이후로 TLS 1.0 및 1.1 더이상 지원할 합니다. 즉, Microsoft 클라이언트, 장치, 또는 TLS 1.0 및 1.1을 사용 하 여 Office 365에 연결 하는 서비스에서 발견 되는 새로운 문제를 수정 하지 않습니다.

Note 그렇다고 해 TLS 1.0 및 1.1 연결 Office 365 차단 됩니다. 사용 하지 않도록 설정 하거나 고객 연결에 TLS 서비스에서 TLS 1.0 및 1.1을 제거 하기 위한 공식 날짜가 없습니다. 최종 사용 하지 않는 날짜 고객 원격 분석에 의해 결정 됩니다 및 아직 알 수 없습니다. 결정 한 후 있을 것 알림을 6 개월 사전에 될 알려진된 손상을 인식 하지 않는 한,이 경우 서비스를 사용 하는 고객을 보호 하기 위해 6 개월 보다 작은에서 작업을 수행할 수 있을 수 있습니다.

모든 클라이언트-서버와 브라우저 서버 조합을 사용 하는 TLS 1.2 (또는 이상 버전) 연결을 유지 하기 위해 Office 365 서비스에 있는지 확인 해야 합니다. 특정 클라이언트-서버와 브라우저 서버 조합을 업데이트 해야할 수 있습니다. 방식에 영향을 주는 경우 하는 방법에 대 한 정보를 [Office 365에서 TLS 1.2의 필수 사용 준비](https://support.microsoft.com/en-us/help/4057306/preparing-for-tls-1-2-in-office-365)를 참조 하십시오.
  
## <a name="deprecating-support-for-3des"></a>3DES에 대 한 지원을 삭제합니다.
<a name="TLS11and12deprecation"> </a>

2018, 10 월 31 기준 더이상 Office 365 Office 365에 대 한 통신에 대 한 3DES 암호화 제품군의 사용을 지원 합니다. 더 구체적으로 Office 365 TLS_RSA_WITH_3DES_EDE_CBC_SHA 암호화 제품군을 지원할 나타나지 않습니다. 이 항목에 나열 된 클라이언트 및이 날짜 보다 안전한 암호화 중 적어도 하나를 지원 해야 후 O365와 통신 하는 서버 ( [TLS 암호화 된 Office 365에서 지 원하는 제품군](technical-reference-details-about-encryption.md#TLSCipherSuites)참조).
  
## <a name="deprecating-sha-1-certificate-support-in-office-365"></a>Office 365에서 SHA-1 인증서를 지원하지 않음
<a name="TLS11and12deprecation"> </a>

6 월 2016를 기준으로 Office 365 더이상 인바운드 또는 아웃 바운드 연결에 대 한 sha-1 인증서를 허용합니다. 현재 사용 하는 인증서를 s h A 1의 인증서 체인에을 하는 경우에 s h A-2 (보안 해시 알고리즘 2) 또는 보다 강력한 해시 알고리즘을 사용 하 여 체인 업데이트 해야 합니다.
  
## <a name="deprecating-rc4-support-in-office-365"></a>Office 365에서 RC4를 지원하지 않음
<a name="TLS11and12deprecation"> </a>

2015년 7월부터 다음 RC4 암호화 제품군에 대한 지원이 중단됩니다.
  
- TLS_RSA_WITH_RC4_128_SHA
    
- TLS_RSA_WITH_RC4_128_MD5
    
## <a name="deprecating-secure-sockets-layer-ssl-30-support-in-office-365"></a>Office 365의 Secure Sockets Layer (SSL) 3.0 지원을 삭제합니다.
<a name="TLS11and12deprecation"> </a>

2014 년 12 월 1 일, 시작 Office 365 시작 된 지원에 대 한 Layer SSL (Secure Sockets) 3.0, TLS 선행 작업을 사용 하지 않도록 설정 합니다. 자세한 내용은 [보안 권고 3009008을](https://technet.microsoft.com/library/security/3009008.aspx)참조 하십시오. 확인 하는 방법에 대 한 지침은 클라이언트 1.0 이상 TLS를 사용 하는 하 고 SSL 3.0을 사용 하지 않도록 설정 하려면 [SSL 3.0 보호 취약점](http://blogs.office.com/2014/10/29/protecting-ssl-3-0-vulnerability/)을 참조 합니다.
  
## <a name="tls-cipher-suites-supported-by-office-365"></a>Office 365에서 지원 되는 TLS 암호화 제품군
<a name="TLSCipherSuites"> </a>

암호화 제품군은 TLS에서 보안 연결을 설정하는 데 사용되는 암호화 알고리즘 모음입니다. Office 365에서 지원하는 암호화 제품군은 강력한 암호화 제품군의 순서대로 제일 강력한 제품군부터 먼저 다음 표에 나열됩니다. Office 365에서 연결 요청을 받으면 Office 365는 먼저 최상위 암호화 제품군을 사용하여 연결하려고 한 후, 해당 암호화 제품군이 실패하는 경우 목록의 두 번째 암호화 제품군을 시도하고 계속 아래로 내려가며 시도합니다. Office 365에서 다른 서버 또는 클라이언트에 연결 요청을 보낼 때 암호화 제품군을 선택하거나 적어도 TLS를 사용할지는 받는 서버 또는 클라이언트에 달려 있습니다.
  
|**프로토콜**|**암호 그룹 이름**|**키 교환 알고리즘/강도**|**PFS(Perfect Forward Secrecy) 지원**|**인증 알고리즘/강도**|**암호화/강도**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384_P384  <br/> |ECDH/192  <br/> |예  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256_P256  <br/> |ECDH/128  <br/> |예  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA_P384  <br/> |ECDH/192  <br/> |예  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA_P256  <br/> |ECDH/128  <br/> |예  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA256  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA256  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_3DES_EDE_CBC_SHA  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |3DES/192  <br/> |
   
## <a name="related-topics"></a>관련 항목
<a name="TLSCipherSuites"> </a>

[Office 365의 암호화](encryption.md)
  
[Office 365 Enterprise의 암호화 설정](set-up-encryption.md)
  
[Windows 보안 상태 업데이트에서 TLS 1.0의 Schannel 구현을: 2015 년 11 월 24,](https://support.microsoft.com/kb/3117336)
  
[향상 된 암호화 하는 TLS/SSL (Windows IT 센터)](https://technet.microsoft.com/en-us/library/cc766285%28v=ws.10%29.aspx)
  

