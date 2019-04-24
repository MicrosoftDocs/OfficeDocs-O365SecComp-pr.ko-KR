---
title: Office 365의 암호화에 대한 기술 관련 세부 정보
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 03/29/2019
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 862cbe93-4268-4ef9-ba79-277545ecf221
description: Office 365의 encyption에 대 한 기술 세부 정보를 확인 합니다.
ms.openlocfilehash: afe077fdedb3e01e5658d27a13e17ae3a3ab5929
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260296"
---
# <a name="technical-reference-details-about-encryption-in-office-365"></a>Office 365의 암호화에 대한 기술 관련 세부 정보

이 문서를 참조 하 여 [Office 365에서 암호화](encryption.md)에 사용 되는 인증서, 기술 및 TLS 암호 제품군에 대해 알아봅니다. 이 문서에서는 계획 된 사용 중단에 대 한 세부 정보도 제공 합니다.
  
- 개요 정보를 찾으려면 [Encryption in Office 365](encryption.md)을 참조 하세요.
- 설치 정보를 찾으려면 [Set up encryption in Office 365 Enterprise](set-up-encryption.md)를 참조 하세요.
- 특정 Windows 버전에서 지원 되는 암호 그룹에 대 한 자세한 내용은 [TLS/SSL (Schannel SSP)의 암호 그룹](https://docs.microsoft.com/windows/desktop/SecAuthN/cipher-suites-in-schannel)을 참조 하십시오.
    
## <a name="microsoft-office-365-certificate-ownership-and-management"></a>Microsoft Office 365 인증서 소유권 및 관리

Microsoft는 자체 인증서를 사용하므로 Office 365에 대한 인증서를 구입하거나 유지 관리할 필요가 없습니다.
  
## <a name="current-encryption-standards-and-planned-deprecations"></a>현재 암호화 표준 및 계획 된 사용 중단

Office 365에 대 한 모범 사례 암호화를 계속 해 서 제공 하기 위해 Microsoft는 지원 되는 암호화 표준을 정기적으로 검토 합니다. 경우에 따라 오래 된 표준을 유지 하 고 보안 수준이 더 낮은 경우에는 이전 표준과 사용 중지 야 합니다. 이 항목에서는 현재 지원 되는 암호 제품군 및 기타 표준과 계획 된 사용 중단에 대 한 세부 정보를 설명 합니다. 

## <a name="fips-compliance-for-office-365"></a>Office 365에 대 한 FIPS 준수
Office 365에서 지 원하는 모든 암호화 제품군은 FIPS 140-2에서 허용 되는 알고리즘을 사용 합니다. Office 365은 Windows에서 FIPS 유효성 검사를 상속 합니다 (Schannel을 통해). schannel에 대 한 자세한 내용은 [TLS/SSL (schannel SSP)의 암호 그룹](https://docs.microsoft.com/windows/desktop/SecAuthN/cipher-suites-in-schannel)을 참조 하세요.
  
## <a name="versions-of-tls-supported-by-office-365"></a>Office 365에서 지원하는 TLS 버전

TLS(전송 계층 보안) 및 TLS 이전의 SSL은 보안 인증서를 사용하여 컴퓨터 간 연결을 암호화함으로써 네트워크를 통한 통신을 보호하는 암호화 프로토콜입니다. Office 365에서는 다음을 비롯한 여러 TLS 버전을 지원합니다.
  
- TLS 버전 1.2(TLS 1.2)
    
- TLS 버전 1.1(TLS 1.1)
    
- TLS 버전 1.0(TLS 1.0)
    
 tls 1.0 및 tls 1.1 지원은 사용 되지 않음 10 월 31, 2018입니다. 자세한 내용은 [방식 support for TLS 1.0 및 1.1 및이](technical-reference-details-about-encryption.md#TLS11and12deprecation) 에 대 한 자세한 내용을 참조 하세요. 
  
## <a name="deprecating-support-for-tls-10-and-11-and-what-this-means-for-you"></a>TLS 1.0 및 1.1에 대 한 방식 지원 및 해당 의미
<a name="TLS11and12deprecation"> </a>

2018는 Office 365에서 더 이상 TLS 1.0 및 1.1을 지원 하지 않으므로 10 월 31 일 이후로 발생 합니다. 즉, Microsoft는 TLS 1.0 및 1.1을 사용 하 여 Office 365에 연결 되는 클라이언트, 장치 또는 서비스에서 발견 된 새로운 문제를 해결 하지 않습니다.

참고이는 Office 365에서 TLS 1.0 및 1.1 연결을 차단 한다는 의미는 아닙니다. tls 서비스에서 고객 연결을 위해 tls 1.0 및 1.1을 사용 하지 않도록 설정 하거나 제거 하는 공식 날짜는 제공 되지 않습니다. 최종 작동 중단 날짜는 고객 원격 분석에 따라 결정 되며 아직 알려진 것은 아닙니다. 결정이 완료 된 후에 알려진 손상에 대해 알고 있는 경우를 제외 하 고는 6 개월 이내에 알림을 받을 수 있으며,이 경우 서비스를 사용 하는 고객을 보호 하기 위해 6 개월 이내로 작업을 수행 해야 할 수 있습니다.

모든 클라이언트 서버와 브라우저 서버 조합에서 TLS 1.2 (이상 버전)를 사용 하 여 Office 365 서비스에 대 한 연결을 유지 하도록 해야 합니다. 특정 클라이언트-서버 및 브라우저 서버 조합을 업데이트 해야 할 수 있습니다. 이를 통해 영향을 주는 방법에 대 한 자세한 내용은 [Office 365에서 TLS 1.2의 필수 사용 준비](https://support.microsoft.com/en-us/help/4057306/preparing-for-tls-1-2-in-office-365)를 참조 하세요.
  
## <a name="deprecating-support-for-3des"></a>3des에 대 한 방식 지원
<a name="TLS11and12deprecation"> </a>

2018 년 10 월 31 일 이후로 office 365에서는 office 365로의 통신에 3des 암호 제품군을 사용 하는 것을 더 이상 지원 하지 않습니다. 보다 구체적으로 말하자면 Office 365에서는 더 이상 TLS_RSA_WITH_3DES_EDE_CBC_SHA 암호 제품군을 지원 하지 않습니다. 2019 년 2 월 28 일부 터이 암호 제품군은 Office 365에서 사용 하지 않도록 설정 됩니다. 이 날짜 후에 O365과 통신 하는 클라이언트 및 서버는이 항목에 나열 된 보안 암호 중 하나 이상을 지원 해야 합니다 ( [Office 365에서 지 원하는 TLS 암호 제품군](technical-reference-details-about-encryption.md#TLSCipherSuites)참조).
  
## <a name="deprecating-sha-1-certificate-support-in-office-365"></a>Office 365에서 SHA-1 인증서를 지원하지 않음
<a name="TLS11and12deprecation"> </a>

6 월 2016 일에 Office 365에서는 아웃 바운드 또는 인바운드 연결에 대 한 sha-1 인증서를 더 이상 받아들이지 않습니다. 현재 인증서 체인에서 s h a-1이 포함 된 인증서를 사용 하는 경우에는 sha-2 (보안 해시 알고리즘 2) 또는 보다 강력한 해싱 알고리즘을 사용 하도록 체인을 업데이트 해야 합니다.
  
## <a name="tls-cipher-suites-supported-by-office-365"></a>Office 365에서 지원 되는 TLS 암호 그룹
<a name="TLSCipherSuites"> </a>

암호화 제품군은 TLS에서 보안 연결을 설정하는 데 사용되는 암호화 알고리즘 모음입니다. 다음 표에는 Office 365에서 지 원하는 암호화 제품군과 가장 강력한 암호 제품군을 먼저 나열 된 수준 순으로 나열 되어 있습니다. Office 365에서 연결 요청을 받으면 Office 365는 제일 먼저 최상위 암호화 제품군을 사용하여 연결하려고 한 후, 해당 암호화 제품군이 실패하는 경우 목록의 두 번째 암호화 제품군을 시도하고 계속 아래로 내려가며 시도합니다. Office 365에서 다른 서버 또는 클라이언트에 연결 요청을 보낼 때 암호화 제품군을 선택하거나 적어도 TLS를 사용할지는 받는 서버 또는 클라이언트에 달려 있습니다.

> [!IMPORTANT]
> TLS 버전은 사용 중지, 더 이상 사용 되지 않는 버전은 최신 버전을 사용할 수 있는 경우 *사용 하지 않도록 해야* 합니다. 즉 tls 1.0, 1.1 및 1.2이 나열 된 위치에 있는 모든 위치에서 *최신* 버전 (tls 1.2)을 선택 합니다.
  
|**프로토콜인**|**암호 그룹 이름**|**키 교환 알고리즘/강도**|**전달 완전 완벽 지원**|**인증 알고리즘/강도**|**암호화/강도**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384  <br/> |ECDH/192  <br/> |예  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256  <br/> |ECDH/128  <br/> |예  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384_P384  <br/> |ECDH/192  <br/> |예  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256_P256  <br/> |ECDH/128  <br/> |예  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA_P384  <br/> |ECDH/192  <br/> |예  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA_P256  <br/> |ECDH/128  <br/> |예  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA256  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA256  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA  <br/> |RSA/112  <br/> |아니요  <br/> |RSA/112  <br/> |AES/128  <br/> |
   
## <a name="related-topics"></a>관련 항목
[Windows 10 v1607의 TLS 암호 그룹](https://docs.microsoft.com/windows/desktop/SecAuthN/tls-cipher-suites-in-windows-10-v1607)

[Office 365의 암호화](encryption.md)
  
[Office 365 Enterprise의 암호화 설정](set-up-encryption.md)
  
[Windows 보안 상태 업데이트에서 TLS 1.0의 Schannel 구현: 2015 년 11 월 24 일](https://support.microsoft.com/kb/3117336)
  
[TLS/SSL 암호화 향상 (Windows IT 센터)](https://technet.microsoft.com/en-us/library/cc766285%28v=ws.10%29.aspx)
  

