---
title: Office 365 스팸 방지 보호
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
description: 스팸 방지 설정 및 도움이 되는 필터에 대 한 Exchange Online 및 Office 365에서 스팸 방지에 대해 알아봅니다. Office 365의 스팸이 너무 많이 효과적으로 활용? 스팸 필터 및 스팸 방지 정책 설정을 사용자 지정할 수 있습니다.
ms.openlocfilehash: 5547904633a0be9ad57fa7431aeddf1267871662
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533531"
---
# <a name="office-365-email-anti-spam-protection"></a>Office 365 스팸 방지 보호

Office 365의 스팸이 너무 많이 하는 방법에 대 한 관련 되어 있습니까? 첫번째 메시지를 수신 하는 시점부터 전자 메일 보호 되어 있으므로 여러 스팸 필터 기본는 Office 365 또는 Exchange Online Protection (EOP) 서비스를 제공 했을 때 합니다. Office 365의 스팸을 방지 하기 위해 조직에서 특정 문제를 처리 하는 보호 설정을 변경 하려면 수-특정 보낸에서 예 스팸 많은 수신 하 라고 표시-단순히 미세 하 여 설정을 수 있도록 조정 또는 최상의 모임에 맞게 조정 하 여 조직의 요구 사항입니다. 이 위해 Office 365 보안에서 스팸 방지 설정을 변경할 수 있습니다 &amp; 준수 센터입니다.
  
이 문서는 Office 365 관리자를 위한 대상입니다. 관리자, 자신이 하지만 Office 365 사용자는 한 경우를 수신 하는 스팸 처리 하는 방법을 설명 찾는 문서 되지 않습니다. 대신, PC에 대 한 Outlook 또는 Outlook for Mac 사용 하는 경우 [정크 메일 필터의 개요](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)를 시작 합니다. 웹에서 Outlook을 사용 하는 경우에 [정크 메일 및 피싱에 대 한 설명](https://support.office.com/article/86c1d76f-4d5a-4967-9647-35665dc17c31)으로 시작 합니다.
  
## <a name="these-options-help-you-prevent-spam-in-office-365"></a>이러한 옵션 Office 365의 스팸 방지 하는 데

 **연결 필터링.** 연결 필터링을 사용 하는 경우 Office 365을 통과해 서 메시지를 허용 하기 전에 보낸 사람의 신뢰도 확인 합니다. 허용 목록 또는 특정 IP 주소 또는 IP 주소 범위를 보낸 모든 메시지를 받을 수 있는지 확인 하려면 수신 허용 목록에서 만들 수 있습니다. 또한 차단 목록 이라는 메시지를 차단할 수 있는 IP 주소 목록을 만들 수 있습니다. 자세한 내용은 [연결 필터 정책 구성](https://technet.microsoft.com/library/jj200718%28v=exchg.150%29.aspx)을 참조 하십시오. Office 365의 스팸에 대 한 관심이 있다면 스팸 방지 하도록 연결 필터링을 사용 합니다.
  
Office 365 엔터프라이즈 e 5 또는 고급 위협 보호 (ATP) 라이선스를 구입한 고객, 연결 필터링이 사용 하 여 스푸핑 인텔리전스 만들려는 허용 및 차단 도메인 스푸핑는 발신자의 목록입니다. 자세한 내용은 [스푸핑 인텔리전스에 대 한 자세한 설명](https://go.microsoft.com/fwlink/?LinkID=735009)을 참조 하십시오.
  
 **스팸 필터링.** Office 365 메시지 특성이 스팸과 스팸 필터링을 사용 하 여 확인 합니다. 스팸으로 식별 된 메시지에 대해 수행 하 고 특정 언어로 작성 된 또는 특정 국가 또는 지역에서 보낸 메시지를 필터링 하 여부를 선택 하기 위한 어떤 작업을 변경할 수 있습니다. 고급 스팸 필터링 옵션을 따라야 스팸 필터링 하는 전체 업그레이드 방법을 사용할 경우에 설정할 수 있습니다. 또한 사용자에 게 알리기 의도 한 것 메시지 격리로 전송 된 경우 대신 최종 사용자 스팸 알림을 구성할 수 있습니다. (격리로 메시지를 보내는 경우 구성 가능한 작업 중 하나) 이러한 알림을에서 최종 사용자를 릴리스하고 가양성, 분석을 위해 Microsoft에 보고 합니다. 자세한 내용은 [스팸 필터 정책 구성](https://go.microsoft.com/fwlink/p/?LinkId=617147)을 참조 하십시오. Office 365의 스팸 방지, Office 365의 스팸이 너무 많이 하는 방법에 대 한 확실 하지 않으면 스팸 필터링을 사용 하 여 도움말, 하기 위해 스팸 방지 하도록 연결 필터링을 사용 합니다.
  
> [!NOTE]
> EOP 독립 실행형 고객을 위한: 기본적으로 EOP 스팸 필터 각 받는 사람의 정크 메일 폴더로 감지 된 스팸 메시지를 보낼 합니다. 그러나 **정크 메일 폴더로 메시지 이동** 작업 온-프레미스 사서함이 있는 작동 하는지 확인 하십시오 하려면 EOP에서 추가 된 스팸 헤더를 검색 하 여 온-프레미스 서버에서 두 Exchange 전송 규칙을 구성 해야 있습니다. 자세한 내용은 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인](https://technet.microsoft.com/library/jj837173%28v=exchg.150%29.aspx)을 참조 하십시오. 
  
## <a name="extra-information-if-you-receive-too-much-spam-in-office-365"></a>Office 365에서 너무 많은 스팸을 수신 하는 경우 추가 정보

다음 비디오 구성 스팸 필터링 EOP에 대 한 개요를 제공 합니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/608be94c-d763-4c47-af94-99e7cb277713?autoplay=false]
  
자세한 내용은 [스팸 필터 정책 구성](https://go.microsoft.com/fwlink/p/?LinkId=617147) 항목을 참조 하세요. 
  
## <a name="check-your-outgoing-messages-to-prevent-spam-in-office-365"></a>Office 365의 스팸 방지 하기 위해 보내는 메시지를 확인 합니다.

 **아웃 바운드 필터링.** Office 365도 확인 하는 사용자가 스팸을 보내지 있는지 확인 합니다. 예: 사용자의 컴퓨터를 우리가 구축 *아웃 바운드 필터링* 을 호출 하는 보호 되므로 스팸 메시지를 보내도록 되도록 지정 하는 맬웨어 감염 얻을 수 있습니다. 아웃 바운드 필터링을 해제할 수 없습니다 하지만 [아웃 바운드 스팸 정책 구성](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx)에 설명 된 설정을 구성할 수 있습니다. Office 365의 스팸이 너무 많이 하는 방법에 대 한 확실 하지 않으면 Exchange Online의 스팸 방지 아웃 바운드 필터링을 사용 합니다.
  
## <a name="beyond-the-basics-more-ways-to-prevent-spam-in-office-365"></a>고급 기능: Office 365의 스팸 방지 하는 방법
<a name="BeyondBasics"> </a>

 **메일 흐름 규칙.** 기반 비즈니스 정책, *[메일 흐름 규칙](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx)* , 라고도 함 *전송 규칙* 으로, 되는 사용자 지정 규칙을 기본 제공 스팸 필터링 이상의 하려는 경우 도움이 되는 다른 필터 Office 365의 스팸을 방지 합니다. 예 [는 신뢰도 scl (스팸) 메시지에서 설정 하는 메일 흐름 규칙을 사용 하 여](https://technet.microsoft.com/library/dn798345%28v=exchg.150%29.aspx)의 설명에 따라 특정 조건에 맞는 메시지에 대 한 스팸 신뢰 수준 (SCL) 값을 설정 하려면 메일 흐름 규칙을 사용할 수 있습니다. 
  
 **전자 메일 인증.** 전자 메일 메시지를 보낸 사람이 하는 방법에 대 한 전자 메일 메시지를 확인할 수 있는 정보를 추가 하려면 (DNS (Domain Name System)를 사용 하는 방법에는 전자 메일 인증을 이라고 합니다. 고급 Office 365 관리자가 가능 이러한 전자 메일 인증 방법을 사용: 
  
- **보낸 사람이 정책 프레임 워크 (SPF).** SPF을 보내는 도메인의 공식된 소유자에 대해 보낸 사람의 IP 주소를 확인 하 여 전자 메일 메시지의 출처의 유효성을 검사 합니다. SPF를 신속 하 게 구성 된 것을 간략하게 소개 합니다 [스푸핑을 방지 하기 위해 Office 365에서 SPF 설정](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx)을 참조 하십시오. Office 365 SPF를 사용 하는 방법에 대 한 더 자세히 이해 또는 하이브리드 배포와 같은 문제해결 또는 비표준 배포에 대 한 [스푸핑을 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)을 사용 하 여 Office 365 방식](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx)으로 시작 합니다.
    
- **DomainKeys 메일 (DKIM)를 식별 합니다.** DKIM를 사용 하면 디지털 서명을 보내는 전자 메일 메시지 헤더에 전자 메일 메시지에 첨부할 수 있습니다. 디지털 서명이 사용 하 여 받는 전자 메일을 받은 하는 합법적인 인지 확인 하는 도메인에서 전자 메일을 수신 하는 전자 메일 시스템. DKIM 및 Office 365에 대 한 정보를 [사용 하 여 Office 365에서 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하는 DKIM](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx)을 참조 하십시오.
    
- **도메인 기반 메시지 인증, 보고 및 적합성 (DMARC).** 메일 시스템을 수신 하는 DMARC 도움이 SPF 또는 DKIM 검사에 실패 하 고 전자 메일 파트너에 대 한 다른 높은 수준의 보안을 제공 하는 메시지와 함께 수행할 작업을 결정 합니다. DMARC 설정에 대 한 정보를 [Office 365의 전자 메일의 유효성을 검사를 사용 하 여 DMARC](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx)를 참조 하십시오.
    
스팸, 피싱, 및 Office 365에서 스푸핑 하는 방법에 대 한 관심이 있다면 SPF, DKIM, 및 DMARC는 함께 사용할 스팸 및 원치 않는 위조를 방지 합니다.
  
 **최종 사용자 관리 되는 설정입니다.** 최종 사용자가 자신의 스팸 설정을 관리할 수는 방법에 대 한 정보를 찾고 하는 경우 [정크 메일 필터 개요](https://go.microsoft.com/fwlink/?LinkId=270065) (Microsoft Outlook 사용자의 경우) 또는 [정크 메일 및 피싱에 대 한 설명](https://go.microsoft.com/fwlink/?LinkId=270068) (Outlook에 대 한 웹 사용자에 게) 체크아웃 합니다. EOP가 온-프레미스 사서함을 보호 하기 위해 사용 하는 경우에 디렉터리 동기화를 사용 하 여 이러한 설정을 서비스에 동기화 되었는지 확인 해야 합니다. 디렉터리 동기화를 설정 하는 방법에 대 한 자세한 내용은 [EOP의 메일 사용자 관리에서](https://technet.microsoft.com/library/dn636911%28v=exchg.150%29.aspx)에서 "사용 하 여 디렉터리 동기화를 메일 사용자 관리"를 참조 하십시오.
  
## <a name="for-more-information"></a>자세한 내용
<a name="BeyondBasics"> </a>

[블로그: 이유는 스팸 및 피싱으로부터 얻을 Office 365를 통해?](https://go.microsoft.com/fwlink/?LinkId=528179 )
  
[스팸 방지 보호 기능 FAQ](https://technet.microsoft.com/library/jj937231%28v=exchg.150%29.aspx)
  
[False 이면 양의 전자 메일을 수신 허용 목록 또는 기타 기술을 스팸으로 표시 방지](prevent-email-from-being-marked-as-spam-0.md)
  
[Office 365 스팸 필터링 정크 메일 메시지를 차단 하는 데 도움이을 설정 하는 방법](block-email-spam-to-prevent-false-negatives.md)
  
[정크 메일과 대량 전자 메일의 차이점은 무엇입니까?](https://technet.microsoft.com/library/dn720441%28v=exchg.150%29.aspx)
  
[스팸 방지 메시지 헤더](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)
  
[후방 분산 메시지 및 EOP](https://technet.microsoft.com/library/dn499795%28v=exchg.150%29.aspx)
  
## <a name="still-need-help"></a>여전히 도움이 필요 하십니까?
<a name="BeyondBasics"> </a>

[![Office 365 커뮤니티 포럼에서 도움말 보기](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![관리자: 서비스 요청 로그인 및 만들기](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![관리자: 지원 서비스 문의](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  

