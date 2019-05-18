---
title: 아웃바운드 및 인바운드 메일 흐름
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: 관리자는 Security & 준수 센터의 메일 흐름 대시보드의 아웃 바운드 및 인바운드 메일 흐름 위젯에 대 한 정보를 확인할 수 있습니다.
ms.openlocfilehash: 629599f6a71c1b871abb819ae4cdd339ffa5e56b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158730"
---
# <a name="outbound-and-inbound-mail-flow"></a>아웃바운드 및 인바운드 메일 흐름

**아웃 바운드 및 인바운드 메일 흐름** 위젯은 **커넥터 보고서** 와 이전의 **TLS 개요 보고서** 의 정보를 한 곳에 결합 합니다.

![Security & 준수 센터의 메일 흐름 대시보드의 아웃 바운드 및 인바운드 메일 흐름 보고서](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

위젯의 정보는 커넥터 및 Office 365의 TLS 메시지 보호와 관련이 있습니다. 자세한 내용은 다음 항목을 참조 하십시오.

- [Configure mail flow using connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a>메시지가 전송 중에 보호 됨 (TLS에서)

**아웃 바운드 및 인바운드 메일 흐름** 위젯은 Office 365 조직에서 메시지를 배달할 때 연결에 사용 되는 TLS 암호화를 표시 합니다. 두 쪽에서 모두 TLS를 제공 하는 경우 다른 전자 메일 서비스와 함께 설정 되는 연결은 TLS에 의해 암호화 됩니다. 이 위젯은 메일 흐름의 마지막 주에 대 한 스냅숏을 제공 합니다. **자세히 보기**를 클릭 하면 **전송 (TLS) 플라이 아웃에서 보호 된 메시지가** 조직에 들어오고 나가는 메시지에 대 한 TLS 보호 기능을 표시 합니다.

![보안 & 준수 센터의 전송 (TLS) 플라이 아웃에서 보호 되는 메시지](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

현재 TLS 1.2는 Office 365에서 제공 하는 가장 안전한 버전의 TLS입니다. 준수 감사에 사용 되는 TLS 암호화를 알아야 하는 경우가 많습니다. 대부분의 원본 및 대상 전자 메일 서버 (사용자가 소유 하지 않으며 Microsoft는 사용 하지 않음)와 직접 관계가 없을 수도 있으므로 이러한 서버에서 사용한 TLS 암호화를 향상 시킬 수 있는 여러 옵션이 없습니다.

그러나 [커넥터](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) 를 사용 하 여 전자 메일 서버와 Office 365 간에 전송 되는 메시지에 대 한 최선의 사용 가능 TLS 보호를 보장할 수 있습니다. 일반 메시지 보다 Office 365와 자체 전자 메일 서버 또는 서버 간의 메일 흐름은 일반적으로 중요도가 더 중요 하며 이러한 메시지에는 추가 보안과 감시를 적용 하는 것이 좋습니다. 자체 전자 메일 서버를 업그레이드 하거나 수정 하 여 사용 중인 TLS 암호화를 개선 하거나, 파트너에 게 연락 하 여 동일한 작업을 수행 하도록 할 수 있습니다. **커넥터 보고서** 에는 Office 365 커넥터를 사용 하는 메시지에 대 한 메일 흐름 볼륨과 TLS 암호화가 모두 표시 됩니다.

## <a name="connector-report"></a>커넥터 보고서

**전송 (TLS에서) 플라이 아웃에서 보호 된 메시지** 의 **커넥터 보고서** 링크를 클릭 하면 보고서에 커넥터를 사용 하 여 Office 365 조직으로 배달 되는 메시지에 대 한 정보가 표시 됩니다. 자체 전자 메일 서버와 Office 365 또는 파트너의 서버와 Office 365 사이에 커넥터를 사용 합니다. 각 커넥터의 메시지 볼륨과 연결에 대 한 TLS 암호화를 사용할 수 있습니다. 또한 커넥터를 사용 하지 않고 Office 365에서 보내거나 받은 메시지에 대 한 데이터를 볼 수도 있습니다.

**메일 흐름** 보기에는 지난 주에 대 한 커넥터를 통한 메시지 양이 표시 됩니다. 범위를 최대 30 일로 늘릴 수 있는 **필터** 를 선택 하 여 날짜 범위를 변경할 수 있습니다. **모든 메일 흐름** 보기에는 모든 커넥터를 통해 Office 365 조직에서 주고 나가는 모든 메일이 표시 됩니다. 드롭다운 메뉴에서 이름을 기준으로 특정 커넥터를 선택할 수 있습니다.

드롭다운에서 **tls 사용** 보기를 선택 하 여 커넥터를 통한 메시지에 대 한 tls 보호 분석을 확인할 수 있습니다. **Tls 개요 보고서** 보고서와 마찬가지로이 보기에는 서로 다른 TLS 버전의 백분율이 표시 됩니다. TLS 1.0 연결의 경우 실제로 Office 365에서 TLS 1.0 지원이 더 이상 사용 되지 않는 경우 문제를 방지 하기 위해 전자 메일 서버 또는 파트너의 서버를 업그레이드 하거나 수정 해야 합니다. 자세한 내용은 [Office 365의 암호화에 대 한 기술 참조 세부 정보](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221)를 참조 하세요.

Insights 커넥터에 대 한 잠재적 TLS 암호화 문제를 강조할 수 있도록 커넥터를 가리킵니다. 이 정보는 다음과 같습니다. **tls가 25%를 초과** 하거나 **tls 1.0이 50%** 이상입니다. 이러한 정보가 표시 되 면 커넥터와 연결 된 전자 메일 서버를 조사 해야 하거나 파트너 조직에 연결 하는 것이 좋습니다.

## <a name="see-also"></a>참고 항목

메일 흐름 대시보드의 다른 메일 흐름 정보에 대 한 자세한 내용은 [Security _AMP_ 준수 센터의 메일 흐름 정보](mail-flow-insights.md)를 참조 하십시오.
