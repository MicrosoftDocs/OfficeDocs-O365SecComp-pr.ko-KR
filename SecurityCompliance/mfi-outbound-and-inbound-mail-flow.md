---
title: 아웃 바운드 및 인바운드 메일 흐름
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: 관리자는 아웃 바운드 및 인바운드 메일 흐름 위젯 Office 365 보안 & 준수 센터에서에서 메일 흐름 대시보드에서 알 수 있습니다.
ms.openlocfilehash: 57792c0347490b40f97a8b92945a9c809484ba4f
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685576"
---
# <a name="outbound-and-inbound-mail-flow"></a>아웃 바운드 및 인바운드 메일 흐름

**아웃 바운드 및 인바운드 메일 흐름** 위젯 **커넥터 보고서** 하 고 한곳에서 이전 **TLS 개요 (영문) 보고서** 에서 정보를 결합합니다.

![Office 365 보안 & 준수 센터의에서 메일 흐름 대시보드에서 아웃 바운드 및 인바운드 메일 흐름 보고서](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

위젯의 정보는 커넥터 및 Office 365에서 TLS 메시지 보호 관련이 있습니다. 자세한 내용은 다음이 항목을 참조 합니다.

- [Configure mail flow using connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a>메시지 (TLS)에 의해 전송 보호

Office 365 조직 간에 메시지를 전달 되는 경우 연결에 사용 되는 TLS 암호화를 표시 하는 **아웃 바운드 및 인바운드 메일 흐름** 위젯 합니다. 다른 전자 메일 서비스 설정 하는 연결에서 TLS 양쪽으로 제공 되 면 TLS로 암호화 됩니다. 위젯 메일 흐름의 마지막 주의 스냅숏을 제공합니다. **자세히 보기를**클릭 하면 **메시지 전송 (TLS) 하 여 보호 된** 플라이 아웃을 입력 하 고 조직에서 나가는 메시지에 대 한 TLS 보호를 표시 됩니다.

![Office 365 보안 & 준수 센터의에서 플라이 아웃 (TLS) 하 여 전송 중에에서 보호 된 메시지](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

현재, TLS 1.2는 Office 365에서 제공 하는 TLS의 가장 안전한 버전입니다. 자주, 규정 준수 감사에 사용 되는 TLS 암호화를 알고 필요 합니다. 아마도 대부분의 원본 및 대상 전자 메일 서버 (소유 하 고 어느 역할 Microsoft)와 직접 관계 없는 이러한 서버에서 사용 되는 TLS 암호화를 개선 하기 위해 다양 한 옵션 필요가 없습니다.

하지만 가장 사용할 수 있는 TLS 보호 전자 메일 서버와 Office 365 사이 전송 된 메시지를 확인 하려면 [커넥터](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) 를 사용할 수 있습니다. Office 365와 직접 전자 메일 서버 또는 파트너에 속하는 서버 간의 메일 흐름은 대개 더 중요 하 고 일반 메시지, 해당 메시지에 추가 보안 및 경계를 적용 하려는 되므로 보다 중요 합니다. 업그레이드 또는 사용 중인 또는 동일한 작업을 수행 하 여 파트너에 게 연락 하는 TLS 암호화를 개선 하기 위해 해당 하는 전자 메일 서버를 수정 수 있습니다. **커넥터 보고서** 에 메일 흐름 볼륨 및 Office 365 커넥터를 사용 하는 메시지에 대 한 TLS 암호화를 모두 표시 됩니다.

## <a name="connector-report"></a>커넥터 보고서

**전송 중 (TLS) 하 여 보호 된 메시지** 플라이 아웃에서 **커넥터 보고서** 링크를 클릭 하면 보고서 커넥터를 사용 하 여 Office 365 조직 간에 전달 되는 메시지에 대 한 정보를 표시 합니다. 커넥터를 사용 하 여 자신의 전자 메일 서버 및 Office 365 또는 파트너의 서버 및 Office 365 사이입니다. 각 커넥터에 대 한 메시지 볼륨 및 연결에 TLS 암호화를 사용할 수 있습니다. 또한 전송 또는 커넥터를 사용 하지 않고 Office 365에서 수신 된 메시지에 대 한 데이터를 볼 수 있습니다.

**메일 흐름** 보기 지난 주에 대 한 커넥터를 통해 메시지의 볼륨을 표시합니다. **필터** 를 최대 30 일의 범위를 늘릴 수 있습니다를 선택 하 여 날짜 범위를 변경할 수 있습니다. 모든 메일 흐름을 하 고 있는 모든 연결선을 통해 Office 365 조직에서 **모든 메일 흐름** 보기 표시 합니다. 드롭다운 메뉴에서에서 이름으로 특정 커넥터를 선택할 수 있습니다.

TLS 보호 (영문) 커넥터를 통해 메시지를 분석 하는 참조까지 아래로 드롭다운에서 **TLS 배정 현황** 보기에서 선택할 수 있습니다. **TLS 개요 보고서** 보고서와 함께 하이 보기는 다양 한 TLS 버전의 백분율을 표시 됩니다. TLS 1.0 연결에 대 한 전자 메일 서버를 파악 필요 하거나 파트너의 서버를 업그레이드 하거나 TLS 1.0 지원 결국 Office 365에서 지원이 중단 된 경우 문제를 방지 하기 위해 고정 합니다. 자세한 내용은 [Office 365의 암호화에 대 한 자세한 내용은 기술 참조 (영문)을](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221)참조 하십시오.

인 사이트 커넥터에 대 한 잠재적 TLS 암호화 문제를 하시기 바랍니다 도움말에 대 한 커넥터를 가리킵니다. 정보는: **No TLS가 넘는 25%** 또는 **50% 초과 하는 TLS 1.0**. 이러한 정보를 표시 하는 경우는 커넥터와 연결 된 또는 파트너 조직에 도달 하 여 되는 전자 메일 서버를 조사 해야 합니다.
