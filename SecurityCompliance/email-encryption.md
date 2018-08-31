---
title: Office 365의 전자 메일 암호화
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/22/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
description: Office OME (메시지 암호화), S/MIME, 정보 권한 관리 (IRM)를 포함 하 여 Office 365의 암호화 옵션을 비교 하 고 전송 계층 보안 (TLS)에 대 한 설명입니다.
ms.openlocfilehash: a705637b85e73c6d1e5bcb3595dcd0b7766411e2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533585"
---
# <a name="email-encryption-in-office-365"></a>Office 365의 전자 메일 암호화

이 문서는 Office OME (메시지 암호화), S/MIME, 정보 권한 관리 (IRM)를 포함 하 여 Office 365의 암호화 옵션을 비교 하 고 전송 계층 보안 (TLS)을 소개 합니다.
  
Office 365 사용자의 전자 메일 보안에 대 한 비즈니스 요구를 충족 하기 위해 여러 암호화 옵션을 제공 합니다. 이 문서에서는 Office 365의 전자 메일을 암호화 하는 세가지 방법에 설명 합니다. Office 365의 모든 보안 기능에 대 한 자세한 내용은 [Office 365 보안 센터](http://go.microsoft.com/fwlink/p/?LinkID=282470)를 방문 하십시오. 이 문서에서는 세가지 유형의 Office 365에서 전자 메일 보안을 위해 Office 365 관리자가 사용할 수 있는 암호화를 소개 합니다.
  
- OME(Office 메시지 암호화)
    
- S/MIME(Secure/Multipurpose Internet Mail Extensions)
    
- IRM(정보 권한 관리)
    
## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a>전자 메일 암호화란 무엇이며 Office 365가 그 기능을 어떻게 사용하나요?

암호화는 있는 정보는로 인코딩된 권한이 부여 된 받는 사람만 디코딩할 하 고 정보를 사용할 수 있도록 하는 프로세스입니다. Office 365 암호화를 사용 하 여 두 방식에서: 고객 컨트롤로 하 고, 서비스에 있습니다. 서비스에서 암호화 Office 365에서 기본적으로 사용 됩니다. 아무것도 구성할 필요가 없습니다. 등 Office 365를 사용 하 여 전송 계층 보안 (TLS) 연결, 또는 두 대의 서버 간의 세션을 암호화 합니다. 
  
일반적으로 전자 메일 암호화 방식 다음과 같습니다.
  
- 메시지는 암호화 또는 일반 텍스트에서 변환 됨에 따라 보낸 사람의 컴퓨터에서 또는 중앙 서버에서 읽을 수 없는 암호화 텍스트 메시지 전송 되는 동안 합니다.
    
- 메시지는 메시지가 차단 되는 경우를 대비 읽지 못하도록 보호 하기 위해 전송 되는 동안 암호화 텍스트에 남아 있습니다.
    
- 받는 사람이 메시지를 받으면 다음 두 가지 방법 중 하나를 통해 메시지가 읽을 수 있는 일반 텍스트 형식으로 다시 변환됩니다.
    
  - 받는 사람의 컴퓨터 키를 사용 하 여 메시지를 암호를 해독 하거나
    
  - 중앙 서버 받는 사람의 id를 확인 한 후 받는 사람을 대신 하 여 메시지의 암호를 해독 합니다.
    
Office 365 서버 간의 통신을 보호 하는 방법에 대 한 자세한 내용은 같은 Office 365 내에서 또는 Office 365 및 Office 365 외부의 신뢰할 수 있는 비즈니스 파트너 조직 간의 [어떻게 Exchange Online을 참조를 사용 하 여 TLS 전자 메일 보안 Office 365의 연결](exchange-online-uses-tls-to-secure-email-connections.md)합니다.
  
[Office 365의 암호화](https://www.youtube.com/watch?v=KmfxCd5ublI)에 대 한 소개이 비디오를 보고 합니다.
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Office 365에서 사용할 수 있는 전자 메일 암호화 옵션 비교

||**        ![OME를 설명하는 개념 아트워크](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)                 **|**        ![IRM을 설명하는 개념 아트워크](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)                 **|**        ![SMIME를 설명하는 개념 아트워크](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)                 **|
|:-----|:-----|:-----|:-----|
|OME(Office 365 메시지 암호화)란 무엇입니까?  <br/> |OME(Office 365 메시지 암호화)는 Azure RMS(권한 관리)를 기반으로 구축된 서비스로, 대상의 전자 메일 주소(Gmail, Yahoo! Mail, Outlook.com 등)에 상관없이 사용자 조직 내부 또는 외부 사람에게 암호화된 전자 메일을 보낼 수 있습니다.  <br/> 관리자는 암호화 조건을 정의하는 전송 규칙을 설정할 수 있습니다. 사용자가 규칙에 맞는 메시지를 보내면 암호화가 자동으로 적용됩니다.  <br/> 암호화 된 메시지를 보려면 받는 사람에 게 일회용 암호, Microsoft 계정 사용 하 여 로그인 또는 로그인 한 작업을 사용 하 여 get 또는 Office 365와 연결 된 계정 학교 수 있습니다. 받는 사람에 게 암호화 된 회신을 보낼 수도 있습니다. 암호화 된 메시지를 보거나 암호화 된 회신을 보낼는 Office 365 구독이 불필요 합니다.  <br/> |IRM은 전자 메일 메시지에 사용 제한을 적용하는 암호화 솔루션입니다. 권한이 없는 사용자가 중요한 정보를 인쇄, 전달 또는 복사하는 것을 방지할 수 있습니다.  <br/> Office 365의 IRM 기능은 Azure RMS(Azure 권한 관리)를 사용합니다. 
  <br/> |S/MIME는 모두 암호화 및 메시지에 디지털 서명을 할 수 있는 암호화 인증서 기반 솔루션입니다. 메시지 암호화 소음이 의도 한 수신자만 열고 하 고 메시지를 읽을 수 있습니다. 받는 사람이 보낸 사람의 id의 유효성을 검사를 사용 하는 디지털 서명이 있습니다.  <br/> 디지털 서명과 메시지 암호화 둘 모두는 디지털 서명을 확인하고 메시지를 암호화 또는 암호 해독하는 키가 포함된 고유한 디지털 인증서를 사용하여 가능해졌습니다.  <br/> S/MIME을 사용 하려면 있어야 공용 키 파일에 각각의 받는 사람입니다. 받는 사람에 게 보안 유지 되어야 하는 자신의 개인 키를 유지 관리 해야 합니다. 받는 사람의 개인 키가 손상 된 경우 받는 사람 새 개인 키를 가져오고 모든 잠재적 보낸사람에 대 한 공용 키를 다시 배포 해야 합니다.  <br/> |
|어떤 작업을 수행하나요?  <br/> | OME:  <br/>  내부 또는 외부 받는 사람에게 보내는 메시지를 암호화합니다.  <br/>  사용자가 Outlook.com, Yahoo! Mail, Gmail 등의 전자 메일 주소로 암호화된 메시지를 보낼 수 있습니다.  <br/>  보기 포털 조직의 브랜드를 반영 하는 전자 메일을 사용자 지정 할는 관리자, 수 있습니다.  <br/>  Microsoft는 안전 하 게 관리 하 고 하지 않아도 되므로, 키를 저장 합니다.  <br/>  브라우저에서 암호화된 메시지(HTML 첨부 파일로 전송)를 열 수 있는 한 특별한 클라이언트 쪽 소프트웨어가 필요하지 않습니다.  <br/> | IRM:  <br/>  암호화 및 사용 제한을 사용하여 전자 메일 메시지 및 첨부 파일을 온라인/오프라인으로 보호합니다.  <br/>  관리자가 전송 규칙 또는 Outlook 보호 규칙을 설정할 수 있도록 함으로써 IRM을 자동으로 적용하여 메시지를 선택할 수 있습니다.  <br/>  Outlook 또는 Outlook Web App에서 템플릿을 수동으로 적용할 수 있도록 합니다.  <br/> |S/MIME는 디지털 서명으로 기밀성 보낸사람 인증을 확인하고 암호화로 메시지 기밀을 확인합니다.  <br/> |
|어떤 작업을 하지 않나요?  <br/> |OME 사용 제한을 메시지에 적용 하면 하지 않습니다. 예, 착신 전환 또는 암호화 된 메시지를 인쇄에서 받는 사람을 중지 하려면 사용할 수 없습니다.  <br/> |일부 응용 프로그램은 모든 장치에서 IRM 전자 메일을 지원 하지 않습니다. 이러한 기능 및 IRM 전자 메일을 지 원하는 기타 제품에 대 한 자세한 내용은 [클라이언트 장치 기능](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities)을 참조 하십시오.<br/> |S/MIME를 검색 하 여 맬웨어, 스팸, 또는 정책에 대 한 암호화 된 메시지를 허용 하지 않습니다.  <br/> |
|권장 사항 및 예제 시나리오  <br/> | 에 관계 없이 소비자 또는 다른 비즈니스 조직 외부 사람에 게 중요 한 비즈니스 정보를 전송 하려는 경우에 OME를 사용 하는 것이 좋습니다. 예를 들어:  <br/>  은행 직원이 고객에게 신용 카드 청구서를 보내는 경우  <br/>  의료 레코드는 환자를 보내는 상황의 office  <br/>  한 변호사가 다른 변호사에게 기밀 법적 정보를 보내는 경우  <br/> | 사용 제한뿐만 아니라 암호화도 적용하려는 경우 IRM을 사용하는 것이 좋습니다. 예를 들면 다음과 같습니다.  <br/>  새 제품에 대 한 대화 팀에 게 기밀 정보를 보내는 관리자 "전달 하지 않음" 옵션을 적용 합니다.  <br/>  임원이 Office 365를 사용하는 파트너의 첨부 파일이 포함된 입찰 제안서를 다른 회사와 공유해야 하는데 전자 메일과 첨부 파일이 모두 보호되어야 하는 경우  <br/> | 조직이 나 받는 사람의 조직 true 피어-투-피어 암호화가 필요할 때 S/MIME을 사용 하는 것이 좋습니다.  <br/>  S/MIME는 다음과 같은 시나리오에서 가장 많이 사용됩니다.  <br/>  정부 기관이 다른 정부 기관과 통신하는 경우  <br/>  기업이 정부 기관과 통신하는 경우  <br/> |
   
## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a>내 Office 365 구독에 대해 사용할 수 있는 암호화 옵션은 무엇이 있나요?

Office 365 구독에 대 한 전자 메일 암호화 옵션에 대 한 내용은 [Exchange Online 서비스 설명](https://technet.microsoft.com/en-us/library/exchange-online-service-description.aspx)을 참조 하십시오. 여기에 다음과 같은 암호화 기능에 대 한 정보를 찾을 수 있습니다.
  
- IRM 기능 및 OME 모두를 비롯한 Azure RMS
    
- S/MIME
    
- TLS
    
- BitLocker를 통한 보관된 데이터 암호화
    
## <a name="what-about-encryption-for-data-at-rest"></a>보관된 데이터의 암호화는 어떻게 하나요?

"보관 된 데이터" 적극적으로 전송 중에 포함 되지 않은 데이터를 가리킵니다. Office 365의 보관 된 전자 메일 데이터 BitLocker 드라이브 암호화를 사용 하 여 암호화 됩니다. BitLocker 무단으로 액세스에 대 한 향상 된 보호를 제공 하는 Office 365 데이터 센터의 하드 드라이브를 암호화 합니다. 자세한 내용은, [BitLocker 개요](https://go.microsoft.com/fwlink/p/?LinkId=394737)를 참조 하십시오.
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a>Office 365의 전자 메일 암호화 옵션에 대한 자세한 내용

이 문서와 TLS에서의 전자 메일 암호화 옵션에 대한 자세한 내용은 다음 문서를 참조하세요.
  
 **OME**
  
[Office 365 메시지 암호화 (OME)](ome.md)
  
 **IRM**
  
[Exchange Online의 정보 권한 관리](https://technet.microsoft.com/en-us/library/jj983436%28v=exchg.150%29.aspx)
  
[Azure 권한 관리 이란?](https://technet.microsoft.com/library/jj585026)
  
 **S/MIME**
  
[메시지 서명 및 암호화를 위한 S/MIME](https://technet.microsoft.com/library/dn626158)
  
[S/MIME 이해](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[공개 키 암호화 이해 (영문)](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
 **TLS**
  
[Office 365에서 커넥터를 사용 하 여 사용자 지정 메일 흐름 구성](https://technet.microsoft.com/en-us/library/jj723138%28v=exchg.150%29.aspx)
  

