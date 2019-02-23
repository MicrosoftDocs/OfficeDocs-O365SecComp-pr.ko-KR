---
title: EOP 기능
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 599b8048-1056-457b-aae4-c063138fd319
description: 다음 표에는 EOP(Exchange 온라인 보호) 호스팅 전자 메일 필터링 서비스에서 사용할 수 있는 기능 목록이 나와 있습니다.
ms.openlocfilehash: 62d37f0faa45551c2932b415fdd691aecc2df1d4
ms.sourcegitcommit: 06d6e63225f912d0f3c6bb836c61eb11c1dbe97a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/22/2019
ms.locfileid: "30206661"
---
# <a name="eop-features"></a>EOP 기능

다음 표에는 EOP(Exchange 온라인 보호) 호스팅 전자 메일 필터링 서비스에서 사용할 수 있는 기능 목록이 나와 있습니다. 
  
> [!TIP]
> [업무용 Office 365 로드맵](https://office.microsoft.com/en-us/products/office-365-roadmap-FX104343353.aspx)에서는 예정된 새로운 기능에 대한 정보를 제공합니다. 여러 EOP 구독 계획에서 사용할 수 있는 기능에 대한 폭넓은 정보는 [Exchange 온라인 보호 서비스 설명](https://go.microsoft.com/fwlink/p/?LinkId=320619)에서 확인할 수 있습니다. 
  
|||
|:-----|:-----|
|**기능**|**설명**|
|**스팸 방지 보호 기능**||
|인바운드 스팸 검색|인바운드 스팸 방지 보호는 항상 사용되며, 사용하지 않도록 설정할 수 없습니다. 연결 필터 및 콘텐츠 필터 정책을 통해 사용자 지정 설정을 구성할 수 있습니다.  <br/> EOP 독립 실행형 고객의 경우: 기본적으로 EOP 콘텐츠 필터는 스팸 검색 메시지를 각 받는 사람의 정크 메일 폴더로 보냅니다. 그러나 온-프레미스 사서함에서 **정크 메일 폴더로 메시지 이동** 작업을 수행할 수 있도록 하려면 온-프레미스 서버에서 두 개의 Exchange 전송 규칙을 구성 하 여 EOP에서 추가 된 스팸 헤더를 검색 해야 합니다. 자세한 내용은 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되도록](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)합니다 .를 참조 하세요.|
|아웃바운드 스팸 검색|아웃 바운드 스팸 방지 보호는 항상 사용 하도록 설정 되므로 아웃 바운드 전자 메일을 보내는 데 서비스를 사용 하는 경우 서비스와 해당 받는 사람을 사용 하는 조직을 보호할 수 있습니다. 인바운드 필터링과 마찬가지로 아웃 바운드 스팸 필터링은 연결 필터링 및 콘텐츠 필터링으로 구성 됩니다. 아웃 바운드 스팸 필터링 설정은 구성할 수 없지만 의심 스 럽 고 차단 된 아웃 바운드 메시지에 대 한 관리자 알림을 구성 하는 데 사용 하는 아웃 바운드 스팸 정책 설정이 있습니다. 자세한 내용은 [아웃 바운드 스팸 정책 구성을](../configure-the-outbound-spam-policy.md)참조 하세요.|
|NDR 후방 산란 보호 기능|ndr 백 분산에 대 한 자세한 내용은 [고급 스팸 필터링 옵션](../advanced-spam-filtering-asf-options.md) 의 ndr 백 분산 설정 및 [후방 산란 메시지 및 EOP](../backscatter-messages-and-eop.md)을 참조 하십시오.|
|대량 메일 필터링|EOP에는 대량 전자 메일 메시지를 식별 하기 위한 향상 된 검색 방법이 있습니다. 사용자 인터페이스를 통해 대량 전자 메일 메시지를 표시 하도록 서비스를 구성할 수 있습니다. 대량 메일 메시지 헤더 스탬프를 검색 하 여 대량 메일을 보다 적극적으로 필터링 하는 전송 규칙을 만들 수도 있습니다. 대량 전자 메일에 대 한 자세한 내용은 [정크 메일과 대량 전자 메일의 차이점](../what-s-the-difference-between-junk-email-and-bulk-email.md) 및 관련 하위 주제를 참조 하세요.|
|악성 URL 차단 목록|EOP에서는 메시지 내에서 알려진 악성 링크를 검색하는 데 도움이 되는 여러 URL 차단 목록을 사용합니다.|
|피싱 방지 보호 기능|EOP에는 750,000개의 알려진 스팸 발송자 도메인이 포함되어 있습니다.|
|**스팸 관리**||
|연결 필터 IP 허용 및 IP 차단 목록을 구성하는 기능|연결 필터에 지정 된 ip 주소는 단일 IP 주소 및 CIDR IP 주소 범위에 적용 됩니다. 또한이 서비스는 IPv6 주소도 지원 합니다. 자세한 내용은 [Configure the connection filter policy](../configure-the-connection-filter-policy.md)을 참조 하십시오.|
|콘텐츠 필터 정책을 사용자, 그룹 또는 도메인별로 사용자 지정하는 기능|세분성을 높이기 위해 사용자 지정 콘텐츠 필터 정책을 만들어 조직의 지정 된 사용자, 그룹 또는 도메인에 적용할 수 있습니다. 사용자 지정 정책은 항상 기본 정책 보다 우선 하지만 사용자 지정 정책의 우선 순위 (즉, 실행 순서)를 변경할 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성을](../configure-your-spam-filter-policies.md)참조 하세요.|
|콘텐츠가 필터링된 메시지에 대한 작업을 구성하는 기능|구성할 수 있는 작업이 여러 개 있습니다. 예를 들어 콘텐츠가 필터링 된 메시지를 삭제 하거나 정크 메일 폴더 또는 격리로 보낼 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성을](../configure-your-spam-filter-policies.md)참조 하세요.|
|적극적인 스팸 필터링에 대한 고급 옵션을 구성하는 기능|자세한 내용은 [configure a 스팸 필터 정책](../configure-your-spam-filter-policies.md) (이를 구성 하는 경우) 및 [고급 스팸 필터링 옵션](../advanced-spam-filtering-asf-options.md) (각 옵션의 기능에 대 한 구체적인 세부 정보 제공)을 참조 하세요.|
|다국어 스팸 필터링|특정 언어로 작성 되었거나 특정 국가나 지역에서 보낸 메시지를 필터링 하도록 EOP를 구성할 수 있습니다. 최대 86의 다른 언어를 구성 하 고 250 지역을 다양 하 게 구성할 수 있습니다. 이 서비스는 높은 정확도 스팸에 대해 구성 된 작업을 적용 합니다. 자세한 내용은 [스팸 필터 정책 구성을](../configure-your-spam-filter-policies.md)참조 하세요.|
|outlook 또는 웹용 outlook을 통한 스팸 관리 (이전의 outlook web App)|관리자 및 최종 사용자가 안전한 보낸 사람 목록 및 차단된 보낸 사람 목록을 만들 수 있습니다. 자세한 내용은 다음을 참조하세요.  <br/> 웹용 Outlook: [차단 또는 허용 (정크 메일 설정)](https://go.microsoft.com/fwlink/p/?LinkId=294862)을 참조 하세요.  <br/> Outlook: [정크 메일 필터 개요](https://go.microsoft.com/fwlink/p/?LinkId=270065) 참조  <br/> EOP을 사용 하 여 온-프레미스 사서함을 보호 하는 경우 이러한 설정이 서비스와 동기화 되도록 디렉터리 동기화를 사용 해야 합니다. 디렉터리 동기화를 설정 하는 방법에 대 한 자세한 내용은 [manage mail users in EOP의](manage-mail-users-in-eop.md)"디렉터리 동기화를 사용 하 여 메일 사용자 관리"를 참조 하십시오.|
|Microsoft Office Outlook용 정크 메일 보고 추가 기능을 통한 스팸 전송|분석을 위해 Microsoft에 스팸 메시지를 제출할 수 있도록 하는 추가 기능을 Outlook에 다운로드할 수 있습니다. 이 도구를 다운로드 하 고 사용 하는 방법에 대 한 자세한 내용은 [보고서 메시지 추가 기능을 사용 하도록 설정을](https://support.office.com/article/4250c4bc-6102-420b-9e0a-a95064837676)참조 하십시오.<br/> Exchange Server 2013 이상 버전을 사용 하는 경우에는 웹용 outlook에서 [정크 메일 및 피싱 사기 보고 ](../report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)에 설명 된 대로 EOP를 웹에서 마우스 오른쪽 단추로 클릭 하 여 스팸 메시지를 제출할 수도 있습니다.|
|전자 메일 별칭을 통해 스팸 및 비스팸 전송|전자 메일을 통해 스팸 (정크) 및 스팸 아님 (정크 아님) 메시지를 Microsoft에 제출할 수 있습니다. 자세한 내용은 [분석을 위해 Microsoft에 스팸 및 스팸이 아닌 메시지 제출을](../submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)참조 하세요.|
|웹에서 Outlook을 통한 스팸 및 비 스팸 전송 정크 메일 보고|정크 메일 및 스팸이 아닌 메시지는 웹에서 Outlook을 통해 Microsoft에 제출할 수 있습니다. 자세한 내용은 [웹용 Outlook에서 정크 메일 및 피싱 사기 보고](../report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)를 참조 하세요.<br/> 이 기능은 현재 Exchange Server 2013 SP1 이상 사서함이 EOP에 의해 필터링 되는 웹 고객의 Outlook에서 사용할 수 있습니다. 웹에서 Exchange Online Outlook 고객 에게도이 기능이 곧 출시 될 예정입니다.|
|최종 사용자 스팸 격리 알림|최종 사용자는 자신의 스팸 격리 된 메시지를 릴리스하고, 필요한 경우 최종 사용자 스팸 알림 메시지를 통해이를 정크 메일 아님으로 보고할 수 있습니다. 이러한 알림 전자 메일은 [Exchange Online에서 최종 사용자 스팸 알림 구성](../configure-end-user-spam-notifications-in-exchange-online.md) 또는 [EOP에서 최종 사용자 스팸 알림 구성](../configure-end-user-spam-notifications-in-eop.md)에 설명 된 대로 관리자가 구성 하 고 사용 하도록 설정 해야 합니다.|
|최종 사용자 스팸 격리 알림 빈도|이 빈도는 기본적으로 3일이며, 1~15일로 구성할 수 있습니다.|
|관리자가 최종 사용자 스팸 격리 알림 언어를 구성하는 기능|이 기능은 최종 사용자 및 관리자가 사용할 수 있습니다. 자세한 내용은 [Find and release quarantined messages as an administrator](../find-and-release-quarantined-messages-as-an-administrator.md) 또는 [Find and Release Quarantined Messages as an End User](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx)를 참조하세요.  |
|웹 페이지를 통해 격리의 메시지 액세스 및 관리|이 기능은 최종 사용자 및 관리자가 사용할 수 있습니다. 자세한 내용은 [Find and release quarantined messages as an administrator](../find-and-release-quarantined-messages-as-an-administrator.md) 또는 [Find and Release Quarantined Messages as an End User](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx)를 참조하세요.  |
|격리를 검색하는 기능|격리에서 특정 스팸 메시지를 검색하는 기능은 관리자와 최종 사용자 모두 사용할 수 있습니다. 자세한 내용은 [Find and release quarantined messages as an administrator](../find-and-release-quarantined-messages-as-an-administrator.md) 또는 [Find and Release Quarantined Messages as an End User](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx)를 참조하세요.  |
|Exchange 관리 센터에서 스팸으로 격리된 메시지 헤더 보기|격리에서 메시지 헤더를 확인한 후 메시지 헤더 텍스트를 복사하여 메시지에 발생한 상황에 대한 정보를 제공하는 [메시지 헤더 분석기](https://testconnectivity.microsoft.com/?tabid=mha)에 붙여넣을 수도 있습니다.|
|**맬웨어 방지 보호 기능**||
|여러 엔진 맬웨어 방지 보호|여러 맬웨어 방지 엔진을 사용하여 자동으로 고객을 항상 보호할 수 있습니다.|
|맬웨어 필터링을 해제하는 옵션|Microsoft에서는 서비스를 통해 라우팅되는 모든 이메일 메시지에 대해 맬웨어 방지 검사를 적용하고 있으므로 사용자는 맬웨어 필터링을 사용하지 않도록 설정할 수 없습니다. Microsoft는 모든 고객에게 일관되고 엄격한 수준의 보호 기능을 제공하는 것이 이메일 메시징 환경을 보호하는 데 필요한 심층 방어 전략의 중요한 부분이라고 생각합니다. 따라서 모든 고객에 대해 맬웨어 필터링이 자동으로 사용하도록 설정됩니다.|
|메시지 본문 및 첨부 파일에 대한 맬웨어 검사|이 서비스는 메시지 본문 및 모든 메시지 첨부 파일의 활성 페이로드에서 맬웨어를 검사합니다.|
|기본 또는 사용자 지정 맬웨어 경고 알림|메시지가 맬웨어로 감지 되어 배달 되지 않는 경우 보낸 사람이 나 관리자에 게 알림 전자 메일 메시지를 보내는 옵션이 있습니다. 이러한 알림은 전체 메시지가 삭제 되는 경우에만 전송 됩니다. 자세한 내용은 [맬웨어 방지 정책 구성을](../configure-anti-malware-policies.md)참조 하세요.|
|맬웨어가 감지된 경우 첨부 파일을 제거하는 옵션|관리자는 전체 메시지를 삭제할지, 아니면 첨부 파일을 제거 하 고 사용자 지정 된 메시지를 받는 사람에 게 보낼지 선택할 수 있습니다. 자세한 내용은 [맬웨어 방지 정책 구성을](../configure-anti-malware-policies.md)참조 하세요.|
|스파이웨어 방지 보호 기능|맬웨어 방지 보호는 바이러스 백신 및 스파이웨어 방지를 포괄합니다.|
|맬웨어 필터 정책을 사용자, 그룹 또는 도메인별로 사용자 지정하는 기능|세분성을 높이기 위해 사용자 지정 맬웨어 필터 정책을 만들어 조직의 지정 된 사용자, 그룹 또는 도메인에 적용할 수 있습니다. 사용자 지정 정책은 항상 기본 정책 보다 우선 하지만 사용자 지정 정책의 우선 순위 (즉, 실행 순서)를 변경할 수 있습니다. 자세한 내용은 [맬웨어 방지 정책 구성을](../configure-anti-malware-policies.md)참조 하세요.|
|**메일 라우팅 및 커넥터**||
|조건부 메일 라우팅|자세한 내용은 [Create Connectors for Conditional Mail Routing](http://technet.microsoft.com/library/905dc235-1d2b-487e-a65a-516d92e88347.aspx)를 참조하세요.|
|편의적 또는 강제 TLS|커넥터에서 oplocks 또는 강제 TLS를 사용할 수 있습니다. oplocks tls는 tls 연결을 시도 하지만 tls 연결이 실패 하면 SMTP 연결을 사용 합니다. tls 연결을 강제 적용 하면 tls 연결이 실패 하는 경우 메시지가 거부 된다는 것을 의미 합니다. TLS, 보안 및 커넥터에 대 한 자세한 내용은 [파트너 조직과의 보안 메일 흐름에 대 한 커넥터 설정을](http://technet.microsoft.com/library/1ce4d6a4-41ba-4d1e-9ca9-e826252c1041.aspx)참조 하십시오.|
|국가별 라우팅(메일 흐름이 특정 지역으로 제한)|자세한 내용은 [Exchange Online Protection 개요](exchange-online-protection-overview.md)에서 "EOP 데이터 센터" 섹션을 참조하세요.|
|SMTP 연결 검사기 도구|이 도구를 사용하여 메일 흐름을 테스트하는 방법에 대한 자세한 내용은 [Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx)를 참조하세요.|
|하위 도메인 일치|허용된 도메인의 하위 도메인 내/외부로의 메일 흐름을 설정하는 방법에 대한 자세한 내용은 [EOP에서 하위 도메인에 대한 전자 메일 흐름 사용](http://technet.microsoft.com/library/b5684042-dadc-4111-95b3-c2fd06e368bf.aspx)을 참조하세요.|
|**전송 규칙**||
|정책 기반 필터링 및 작업|사용자 지정 정책은 Exchange 전송 규칙을 기반으로 합니다. 도메인, 키워드, 파일 이름, 파일 형식, 제목 줄, 메시지 본문, 보낸 사람, 받는 사람, 헤더 및 IP 주소를 기준으로 필터링 할 수 있습니다. 자세한 내용은 [Exchange Online Protection의 메일 흐름 규칙 (전송 규칙)](mail-flow-rules-transport-rules-0.md)을 참조 하세요.|
|텍스트 패턴을 기준으로 필터링|전송 규칙에서는 배열 또는 정규식을 사용하여 텍스트를 일치시킬 수 있습니다. 또한 하나의 문자열 또는 문자열 배열을 사용하여 주소, 제목, 본문 또는 첨부 파일 이름과 같은 여러 메시지 속성을 일치시킬 수 있습니다. 자세한 내용은 [Transport Rule Conditions (Predicates)](http://technet.microsoft.com/library/04edeaba-afd4-4207-b2cb-51bcc44e483c.aspx)을 참조하세요.|
|사용자 지정 사전|전송 규칙은 텍스트 및 키워드의 긴 목록을 포함할 수 있습니다. 이는 사용자 지정 사전과 동일한 기능을 제공합니다.|
|도메인별 정책 규칙|보낸 사람 또는 받는 사람 도메인 이름, IP 주소 범위, 주소 키워드 또는 패턴, 그룹 구성원 및 기타 조건에 맞게 전송 규칙 범위를 사용자 지정할 수 있습니다. 자세한 내용은 [Transport Rule Conditions (Predicates)](http://technet.microsoft.com/library/04edeaba-afd4-4207-b2cb-51bcc44e483c.aspx)을 참조하세요.  |
|첨부 파일 검색|첨부 파일의 파일 이름, 확장명 및 내용을 검색하도록 규칙을 만들 수 있습니다.|
|보낸 사람에게 정책 규칙 알림 보내기|메시지를 거부 하 고 **설명에 대 한 메시지 거부** 를 통해 보낸 사람에 게 배달 못 함 보고서 (NDR)를 보내거나 **확장 상태 코드 작업을 사용 하 여 메시지를 거부할** 수 있습니다. 자세한 내용은 [Transport rule actions](http://technet.microsoft.com/library/f8621ecb-a177-4025-9011-a6569999746a.aspx)을 참조 하십시오.|
|고정된 주소로 메시지 보내기(예: 메시지를 특정 주소로 리디렉션 또는 특정 복사)|전송 규칙은 리디렉션하고, 참조 또는 숨은 참조로 받는 사람을 추가하고, 받는 사람 및 기타 옵션을 추가할 수 있습니다. 자세한 내용은 [Transport rule actions](http://technet.microsoft.com/library/f8621ecb-a177-4025-9011-a6569999746a.aspx)을 참조하세요.|
|여러 규칙에서 규칙의 우선 순위를 쉽게 조정할 수 있는 기능|Exchange 관리 센터를 사용하여 규칙이 처리되는 순서를 변경할 수 있습니다. 자세한 내용은 [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx)를 참조하세요.  |
|메시지를 필터링한 다음 메시지의 속성 또는 라우팅을 변경하는 기능|다양 한 조건에 따라 메시지를 필터링 한 다음 각 메시지에 일련의 작업을 적용할 수 있습니다. 자세한 내용은 [Exchange Online Protection의 메일 흐름 규칙 (전송 규칙)](mail-flow-rules-transport-rules-0.md)을 참조 하세요.|
|규칙에 따라 메시지의 스팸 지수 변경|전송 중인 메시지를 검사 하 고 선택한 기준에 따라 스팸 지 수를 해당 수준에 할당할 수 있습니다. 자세한 내용은 [메일 흐름 규칙을 사용 하 여 메시지에서 SCL (스팸 지 수) 설정을](../use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)참조 하십시오.|
|메시지 첨부 파일 검사|첨부 파일의 내용 또는 첨부된 파일의 특성을 조사하고 발견된 항목에 따라 수행할 작업을 정의할 수 있습니다. 자세한 내용은 [Using transport rules to inspect message attachments](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)를 참조하세요.  |
|**관리**||
|웹 기반 관리|EOP 관리자는 60 언어에서 지원 되는 EAC (Exchange 관리 센터) 인터페이스를 통해 서비스를 관리할 수 있습니다. 자세한 내용은 exchange [Online Protection의 exchange 관리 센터 ](../exchange-admin-center-in-exchange-online-protection-eop.md)를 참조 하세요.|
|디렉터리 동기화|디렉터리 동기화는 Azure Active Directory 동기화 도구를 통해 사용할 수 있습니다. 자세한 내용은 [EOP에서 메일 사용자 관리](manage-mail-users-in-eop.md)에서 "디렉터리 동기화를 사용하여 메일 사용자 관리" 섹션을 참조하세요.  |
|DBEB(디렉터리 기반 Edge 차단)|DBEB 기능을 통해 서비스 네트워크 주변에서 잘못된 받는 사람에 대한 메시지를 거부할 수 있습니다. DBEB를 사용하면 메일 사용이 가능한 받는 사람을 Office 365에 추가하고 Office 365에 존재하지 않는 전자 메일로 전송되는 모든 메시지를 차단할 수 있습니다. DBEB 구성에 대한 자세한 내용은 [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)를 참조하세요.  |
|원격 Windows PowerShell 액세스|전체 EOP 기능을 원격 Windows PowerShell을 통해 사용할 수 있습니다. 자세한 내용은 [PowerShell in Exchange Online Protection](http://technet.microsoft.com/library/f7918a88-774a-405e-945b-bc2f5ee9f748.aspx)을 참조하세요.  |
|**보고 및 로깅**||
|메시지 추적|메시지 추적 기능을 사용하면 전자 메일 메시지가 서비스를 통과할 때 관리자로서 이를 추적할 수 있습니다. 이렇게 하면 서비스에서 대상 전자 메일 메시지를 수신, 거부, 지연 또는 배달했는지 여부를 확인하는 데 도움이 되며, 사용자의 질문에 효과적으로 답변하고, 메일 흐름 문제를 해결하고, 정책 변경의 유효성을 검사하고, 기술 지원팀에 문의해야 하는 수고를 덜어 줍니다. 자세한 내용은 [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)을 참조하세요.  |
|웹 기반 보고서|Office 365 관리 센터의 메일 보호 보고서는 메시징 데이터를 제공합니다. 예를 들어 일치되는 스팸 및 맬웨어의 양 또는 전송 규칙이 일치되는 빈도를 모니터링할 수 있습니다. 이러한 대화형 보고서를 사용하여 최대 90일 이전의 요약 데이터에 대한 시각적 보고서를 빠르게 보고 개별 메시지의 세부 정보를 드릴다운할 수 있습니다. 자세한 내용은 [Use mail protection reports in Office 365 to view data about malware, spam, and rule detections](http://technet.microsoft.com/library/bcef7984-4bfa-4ca8-9fa5-a65af8618f5d.aspx)를 참조하세요.  |
|Excel 보고 통합 문서를 통한 세부 보고|Excel 2013 보고 통합 문서의 전자 메일 보호 보고서도 사용할 수 있습니다. 그러나 이 보고서 대신 향상된 Office 365 관리 센터 보고서를 사용하는 것이 좋습니다. Excel 2013 보고 통합 문서는 향후 더 이상 사용되지 않을 예정입니다.|
|감사 로깅|EOP 관리에 관리자 역할 그룹 보고서 및 관리자 감사 로그를 사용할 수 있습니다. 자세한 내용은 [EOP의 감사 보고서](auditing-reports-in-eop.md)를 참조하세요.  |
|**SLA(서비스 수준 계약) 및 지원**||
|스팸 유효성 SLA|\>99%|
|가양성 비율 SLA|\<1:250,000|
|바이러스 검색 및 차단 SLA|알려진 바이러스의 100%|
|월별 작동 시간 SLA|99.999%|
|연중 무휴 24시간 전화 및 웹 기술 지원|EOP 도움말 및 지원 옵션에 대한 자세한 내용은 [EOP에 대한 도움말 및 지원](help-and-support-for-eop.md)을 참조하세요.|
|**기타 기능**||
|지역 중복 글로벌 서버 네트워크|EOP는 최상의 가용성을 제공하도록 설계된 데이터 센터의 전 세계 네트워크에서 실행됩니다. 자세한 내용은 [Exchange Online Protection 개요](exchange-online-protection-overview.md)에서 "EOP 데이터 센터" 섹션을 참조하세요.  |
|온-프레미스 서버가 메일을 수락할 수 없는 경우 메시지 큐 대기|지연 메시지는 2일간 큐에 남아 있습니다. 메시지 다시 시도는 받는 사람의 메일 시스템에서 다시 받은 오류를 기반으로 합니다. 평균적으로 5분마다 메시지가 다시 시도됩니다. 자세한 내용은 [EOP 대기, 지연 및 반송 메시지 FAQ](eop-queued-deferred-and-bounced-messages-faq.md)를 참조하세요.  |
|추가 서비스로 사용할 수 있는 Office 365 메시지 암호화|자세한 내용은 [Office 365의 암호화](https://technet.microsoft.com/en-us/library/dn569286.aspx)를 참조하세요.|
   

