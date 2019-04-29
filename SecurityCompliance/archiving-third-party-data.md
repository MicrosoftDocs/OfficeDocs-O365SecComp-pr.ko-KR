---
title: Office 365에서 타사 데이터 보관
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: '관리자는 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 Office 365 조 직의 사서함으로 타사 데이터를 가져올 수 있습니다. 이를 통해 Office 365의 Facebook, Twitter 및 기타 타사 데이터 원본에서 데이터를 보관할 수 있습니다. 그런 다음 타사 데이터에 대해 Office 365 준수 기능 (예: 법적 보존, eDiscovery, 원본 위치 보관 및 보존 정책)을 사용 하 여 적용할 수 있습니다.'
ms.openlocfilehash: b96c4852c3c9226219120a1be014ea3988cf91a2
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402916"
---
# <a name="archive-third-party-data-in-office-365"></a>Office 365에서 타사 데이터 보관

관리자는 office 365을 사용 하 여 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 타사 데이터를 가져오고 office 365 조직의 사서함으로 보관할 수 있습니다. Office 365로 가져올 수 있는 타사 데이터 원본의 예는 다음과 같습니다. 
  
- **교류** -Twitter, Facebook, Yammer 및 LinkedIn 
    
- **인스턴트 메시징** -Yahoo Messenger, GoogleTalk 및 Cisco jabber 
    
- **문서 공동 작업** 상자 및 DropBox 
    
- **세로 산업** -고객 관계 관리 (예: Salesforce Chatter) 및 금융 서비스 (예: Bloomberg 및: thomson reuters) 
    
- **SMS/텍스트 메시징** -BlackBerry 
    
타사 데이터를 가져온 후에는이 데이터에 소송 보존, eDiscovery, 원본 위치 보관, 감사, 감독 및 Office 365 보존 정책 등의 Office 365 준수 기능을 적용할 수 있습니다. 예를 들어 사서함에 소송 보존이 적용되면 타사 데이터가 보존됩니다. Microsoft eDiscovery 도구를 사용 하 여 타사 데이터를 검색할 수 있습니다. 또는 Microsoft 데이터의 경우처럼 타사 데이터에도 보관 및 삭제 정책을 적용할 수 있습니다. 간단히 말해서 Office 365에서 타사 데이터를 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.

Office 365에서는 두 가지 방법으로 타사 데이터를 가져오고 보관할 수 있습니다.

- **보안 & 준수 센터의 타사 데이터 커넥터를 사용** 하 여 Office 365의 보안 & 준수 센터에서 사용할 수 있는 사용자 지정 데이터 커넥터를 사용 합니다. 커넥터를 설정 하 고 구성한 후에는 타사 데이터 원본에 연결 하 고, 항목의 콘텐츠를 전자 메일 메시지 형식으로 변환한 다음 Office 365에서 사서함으로 항목을 가져옵니다. 이러한 커넥터에서 지원 되는 타사 데이터 원본 및 커넥터를 설정 하는 단계별 프로세스에 대 한 자세한 내용은 [Office 365 (Preview)에서 예제 커넥터를 사용 하 여 타사 데이터 보관을](archive-third-party-data-with-sample-connector.md)참조 하십시오.

- **microsoft 파트너와 공동 작업** 조직에서는 타사 데이터 원본에서 항목을 추출 하도록 구성 되는 사용자 지정 커넥터를 제공 하는 microsoft 파트너와 함께 작동 하며, 다음을 수행 하 여 microsoft 클라우드에 연결 합니다. 타사 API를 사용 하 여 Office 365로 해당 항목을 가져옵니다. 또한 파트너 커넥터는 타사 데이터 원본에서 전자 메일 메시지로 항목의 콘텐츠를 변환한 다음 Office 365에서 사서함으로 가져옵니다. 사용할 수 있는 파트너의 목록과이 방법의 단계별 프로세스에 대 한 자세한 내용은 [Office 365에서 파트너와 협력 하 여 타사 데이터 보관](work-with-partner-to-archive-third-party-data.md)을 참조 하십시오.