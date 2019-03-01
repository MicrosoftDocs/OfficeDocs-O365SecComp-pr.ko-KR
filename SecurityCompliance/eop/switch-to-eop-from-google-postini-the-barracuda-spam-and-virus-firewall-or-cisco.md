---
title: Google Postini, Barracuda Spam and Virus Firewall 또는 Cisco IronPor에서 EOP로 전환
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 81b75194-3b04-48da-8b81-951afbabedde
description: 이 항목의 목표는 온-프레미스 전자 메일 방역 어플라이언스나 클라우드 기반 보호 서비스에서 EOP(Exchange Online Protection)로 전환하는 프로세스를 이해하고 EOP를 시작하는 데 필요한 도움말 리소스를 제공하는 것입니다.
ms.openlocfilehash: a1fa7b63dfc1e6eb193d458545722c4b5331bc48
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30340759"
---
# <a name="switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco-ironport"></a>Google Postini, Barracuda Spam and Virus Firewall 또는 Cisco IronPor에서 EOP로 전환

 이 항목의 목표는 온-프레미스 전자 메일 방역 어플라이언스나 클라우드 기반 보호 서비스에서 EOP(Exchange Online Protection)로 전환하는 프로세스를 이해하고 EOP를 시작하는 데 필요한 도움말 리소스를 제공하는 것입니다. 여러 개의 스팸 필터링 솔루션이 있지만 EOP로 전환하는 프로세스는 대부분 비슷합니다.
  
EOP를 처음 사용하는 경우 전환을 결정하기 전에 EOP의 기능에 대해 간략하게 읽어보려면 TechNet에서 [Exchange Online Protection 개요](exchange-online-protection-overview.md)를 참조하십시오. 
  
EOP로 전환하기 전에 EOP 보호 사서함을 클라우드 시나리오에서 호스트할지, Exchange Online 시나리오에서 호스트할지, 온-프레미스 시나리오에서 호스트할지 또는 하이브리드 시나리오에서 호스트할지 생각해보는 것이 중요합니다. 하이브리드는 일부 사서함은 온-프레미스에서 호스팅되고 또 다른 일부 사서함은 Exchange Online에서 호스팅되는 것을 의미합니다. 클라우드, 온-프레미스, 하이브리드 등 이러한 각 호스트 시나리오가 가능하지만 설치 단계는 다를 수 있습니다. 다음은 적합한 배포를 선택하는 데 도움이 되는 몇 가지 고려 사항입니다.
  
- **온-프레미스 사서함의 EOP 보호** 이 시나리오는 사용할 기존의 메일 호스트 인프라를 가지고 있는 경우 또는 사서함을 온-프레미스로 유지해야 하는 비즈니스 요구 사항이 있고 EOP의 클라우드 기반 이메일 보호를 원하는 경우에 적합합니다. [EOP 독립 실행형으로 전환](#BKMK_SwitchStandalone.md)에서 이 시나리오에 대해 보다 자세하게 설명합니다. 
    
- **Exchange Online 사서함의 EOP 보호** 이 시나리오는 EOP 보호를 원하고 모든 사서함이 클라우드에서 호스팅되는 경우에 적합합니다. 이 시나리오에서는 온-프레미스 메시징 서버를 유지 관리하지 않아도 되므로 복잡성이 줄어듭니다. [Exchange Online으로 전환](switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco.md#BKMK_SwitchEXO)에서 이 시나리오에 대해 보다 자세하게 설명합니다. 
    
- **하이브리드 사서함의 EOP 보호** 클라우드 사서함을 원하지만 일부 사용자의 사서함을 온-프레미스로 유지해야 하는 경우에 적합합니다. 일부 사서함은 온-프레미스에서 호스팅하고 또 다른 일부 사서함은 Exchange Online에서 호스팅하려는 경우에 이 시나리오를 선택합니다. [하이브리드 솔루션으로 전환](#BKMK_SwitchHybrid.md)에서 이 시나리오에 대해 보다 자세하게 설명합니다. 
    
## <a name="switch-to-eop-standalone"></a>EOP 독립 실행형으로 전환
<a name="BKMK_SwitchStandalone"> </a>

현재 온-프레미스에서 사서함을 호스트하고 온-프레미스 보호 어플라이언스나 클라우드 메시징 보호 서비스를 사용하는 경우 EOP로 전환하면 EOP 보호 기능 및 가용성을 사용할 수 있습니다. EOP를 독립 실행형 시나리오로 설정하려면(즉 온-프레미스로 사서함을 호스트하고 EOP를 사용하여 전자 메일 보호 기능 제공) [EOP 서비스 설정](set-up-your-eop-service.md)에 설명된 단계를 수행하면 됩니다. 이 항목에는 등록, 도메인 추가 및 커넥터로 메일 흐름을 설정하는 등 EOP 보호를 설정하는 단계가 설명되어 있습니다.
  
## <a name="switch-to-exchange-online"></a>Exchange Online으로 전환
<a name="BKMK_SwitchEXO"> </a>

온-프레미스 어플라이언스에 의해 보호되는 온-프레미스 사서함이 있고 Exchange Online 클라우스 호스팅 사서함 및 EOP 보호로 이동하여 Office 365 클라우드 메시징 및 보호 기능을 사용하려고 합니다. 시작하려면 Office 365에 등록하고 도메인을 추가합니다. 이 시나리오에서는 온-프레미스 사서함으로 라우팅하지 않으므로 커넥터를 설치할 필요가 없습니다. [Office 365 등록 페이지](https://www.microsoft.com/en-us/office365/online-software.aspx)에서 시작합니다 ([Office 365 시작](https://go.microsoft.com/fwlink/p/?LinkId=275407)에 Office 365 기능을 쉽게 알 수 있도록 도와주는 리소스가 제공됨). 
  
Office 365 설치 프로세스 동안 클라우드 기반 사서함 사용자를 만듭니다.
  
## <a name="switch-to-a-hybrid-solution"></a>하이브리드 솔루션으로 전환
<a name="BKMK_SwitchHybrid"> </a>

업무 요구 사항이나 규정 고려 사항 등으로 인해 사서함 일부만 클라우드로 이동해야 할 수 있습니다. 하이브리드 시나리오를 배포하면 업무 요구 사항에 맞게 사서함을 클라우드로 이동할 수 있습니다. EOP 보호가 포함된 하이브리드 시나리오로 마이그레이션하는 작업은 모든 클라우드 시나리오로 이동하는 작업보다 복잡할 수 있지만 Microsoft는 하이브리드로 간편하게 이동할 수 있도록 완벽한 하이브리드 지원 및 다양한 리소스를 제공합니다.
  
하이브리드 배포를 고려하는 경우 이 배포를 시작하기 위한 최적의 공간은 [Exchange Server 2013 Hybrid Deployments](http://technet.microsoft.com/library/59e32000-4fcf-417f-a491-f1d8f9aeef9b.aspx)입니다. 또한 하이브리드 시나리오에서 메일을 라우팅할 수 있는 여러 방법이 있으며, 이러한 방법은 반드시 이해해야 합니다. [Transport Routing in Exchange 2013 Hybrid Deployments](http://technet.microsoft.com/library/36c2cea3-2e2f-40ac-88bd-7e1b6bd27828.aspx)에는 업무 요구 사항에 맞게 최적의 라우팅 시나리오를 선택할 수 있도록 각 유형에 대해 설명되어 있습니다. 
  
## <a name="migration-planning"></a>마이그레이션 계획
<a name="sectionSection3"> </a>

EOP로 전환하도록 결정한 경우 다음 영역을 특별히 고려해야 합니다.
  
- **사용자 지정 필터링 규칙** 특정 스팸을 catch 하는 사용자 지정 필터링 또는 비즈니스 정책 규칙이 있는 경우 규칙을 마이그레이션하기 전에 기본 설정을 사용 하 여 EOP을 시도 하는 것이 좋습니다. EOP는 기본 설정을 사용 하 여 엔터프라이즈 수준의 스팸 보호를 제공 하므로 규칙 일부를 EOP로 마이그레이션하지 않아도 될 수 있습니다. 물론 특정 사용자 지정 비즈니스 정책을 적용 하는 규칙이 있는 경우 해당 규칙을 만들 수 있습니다. [Exchange Online Protection의 메일 흐름 규칙 (전송 규칙)](mail-flow-rules-transport-rules-0.md) EOP에서 메일 흐름 규칙을 만드는 방법에 대 한 자세한 지침을 제공 합니다. 
    
- **ip 허용 목록 및 ip 차단 목록** 사용자별 허용 목록 및 차단 목록이 있는 경우 설치 프로세스의 일부로이 목록을 EOP에 복사 하는 데 시간이 오래 걸릴 수 있습니다. ip 허용 목록 및 ip 차단 목록에 대 한 자세한 내용은 [Configure the connection filter policy](../configure-the-connection-filter-policy.md)을 참조 하십시오.
    
- **보안 통신** 암호화된 메시징을 필요로 하는 파트너가 있는 경우 Exchange 관리 센터에서 보안 통신을 설정하는 것이 좋습니다. 이 시나리오를 구성하려면 [Create connectors for a secure mail channel using transport layer security (TLS)](http://technet.microsoft.com/library/1ce4d6a4-41ba-4d1e-9ca9-e826252c1041.aspx)를 참조하세요.
    
> [!TIP]
> 온-프레미스 어플라이언스에서 EOP로 전환할 경우 비즈니스 규칙 검사를 수행하는 어플라이언스나 서버를 그대로 둘 수 있습니다. 예를 들어 어플라이언스가 아웃바운드 메일에서 사용자 지정 필터링을 수행하고 있으며, 계속해서 수행하기를 원하는 경우 메일을 인터넷으로 라우팅하기 전에 추가 필터링을 위해 어플라이언스로 메일을 직접 보내도록 EOP를 구성할 수 있습니다. [Exchange Online Protection Connectors - Outbound Smart Host Scenario](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx)에는 이 경우 메일 흐름을 설정하는 방법에 나와 있습니다. 
  

