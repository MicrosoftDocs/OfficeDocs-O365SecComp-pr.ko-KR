---
title: Exchange Online Protection의 보고 및 메시지 추적
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 12/18/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: Microsoft EOP(Exchange Online Protection)에서는 조직의 전체 상태를 확인할 수 있는 다양한 보고서를 제공합니다. 받는 사람에게 메시지가 도착하지 않는 등 특정 이벤트에 대한 문제를 해결할 수 있는 도구와 규정 준수 요구 사항을 지원하는 감사 보고서도 있습니다. 다음 표에서는 EOP 관리자가 사용할 수 있는 보고서 및 문제 해결 도구를 설명합니다.
ms.openlocfilehash: 39ac70c401cb4a630b95fab89fe3a145495c29eb
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676568"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a>Exchange Online Protection의 보고 및 메시지 추적

Microsoft EOP(Exchange Online Protection)에서는 조직의 전체 상태를 확인할 수 있는 다양한 보고서를 제공합니다. 받는 사람에게 메시지가 도착하지 않는 등 특정 이벤트에 대한 문제를 해결할 수 있는 도구와 규정 준수 요구 사항을 지원하는 감사 보고서도 있습니다.

## <a name="usage-reports"></a>사용 현황 보고서

**Office 365 그룹 활동**: 만들어지고 사용 되는 office 365 그룹 수에 대 한 정보를 확인 합니다.  

**전자 메일 활동**: 전체 조직에서 전송, 수신 및 읽은 메시지 수와 특정 사용자에 대 한 정보를 확인 합니다.  

**전자 메일 앱 사용 현황**: 사용 되는 전자 메일 앱에 대 한 정보를 볼 수 있습니다. 여기에는 각 앱에 대 한 총 연결 수와 연결 중인 Outlook의 버전이 포함 됩니다.  

**사서함 사용량**: 사서함에 사용 되는 저장소, 할당량 소비, 항목 수 및 마지막 활동 (보내기 또는 읽기 작업)에 대 한 정보를 확인 합니다.

자세한 내용은 다음 리소스를 참조 하십시오.

- [관리 센터의 office 365 보고서-Office 365 그룹](https://go.microsoft.com/fwlink/p/?linkid=861610)

- [관리 센터의 Office 365 보고서-전자 메일 활동](https://go.microsoft.com/fwlink/p/?linkid=859706)

- [관리 센터의 Office 365 보고서-전자 메일 앱 사용](https://go.microsoft.com/fwlink/p/?linkid=859707)

- [관리 센터의 Office 365 보고서-사서함 사용량](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security--compliance-reports-in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터의 보안 & 준수 보고서

이러한 향상 된 보고서는 요약 정보와 자세한 정보를 드릴 다운 하는 기능을 포함 하는 EOP 관리자에 게 대화형 보고 환경을 제공 합니다.  

**Atp (Advanced Threat Protection)**: atp에 속하는 안전한 링크 및 안전한 첨부 파일에 대 한 정보를 확인 합니다.  

**EOP**: 조직에서 보내고 보낸 맬웨어 감지, 스푸핑된 메일, 스팸 감지 및 메일 흐름에 대 한 정보를 확인 합니다.  

[Advanced Threat Protection 및 Exchange Online Protection에 대 한 보고서 보기](https://go.microsoft.com/fwlink/p/?linkid=852409)

## <a name="custom-reports-using-microsoft-graph"></a>Microsoft Graph를 사용한 사용자 지정 보고서

Microsoft Graph를 사용 하 여 Microsoft 365 관리 센터에서 사용할 수 있는 보고서를 프로그래밍 방식으로 만들기 microsoft [graph에서 Office 365 사용 현황 보고서 작업](https://go.microsoft.com/fwlink/p/?linkid=865135) 을 참조 하세요.

## <a name="custom-reports-using-reporting-web-services"></a>보고 웹 서비스를 사용한 사용자 지정 보고서

REST/ODATA2 쿼리 필터링을 사용 하 여 사용 가능한 Exchange Online Protection PowerShell 보고 cmdlet에서 프로그래밍 방식으로 보고서를 만듭니다.

[Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926) 참조

## <a name="message-trace"></a>Message trace

EOP를 통과하는 전자 메일 메시지를 추적합니다. 이를 통해 서비스에서 전자 메일 메시지를 수신, 거부, 지연 또는 배달했는지 여부를 확인할 수 있습니다. 또한 최종 상태에 도달 하기 전에 메시지에 대해 수행 된 작업을 보여 줍니다.  

이 정보를 사용 하 여 사용자의 질문에 효과적으로 응답 하 고, 메일 흐름 문제를 해결 하며, 정책 변경을 확인 하 고, 기술 지원 서비스에 문의 하 여 도움을 받을 수 있습니다.  

[전자 메일 메시지 추적](https://docs.microsoft.com/exchange/monitoring/trace-an-email-message/trace-an-email-message) 참조

## <a name="audit-logging"></a>감사 로깅

조직 관리자가 변경한 특정 내용을 추적합니다. 이러한 보고서를 사용하면 구성 문제를 해결하거나 보안 또는 규정 준수 관련 문제의 원인을 찾을 수 있습니다. [EOP의 감사 보고서를](auditing-reports-in-eop.md)참조 하세요.

## <a name="reporting-and-message-trace-data-availability-and-latency"></a>보고 및 메시지 추적 데이터 사용 가능 여부 및 대기 시간

다음 표에는 EOP 보고 및 메시지 추적 데이터를 사용할 수 있는 시기와 기간에 대한 설명이 나와 있습니다.
  
||||
|:-----|:-----|:-----|
|**보고서 유형**|**데이터 사용 가능 기간(확인 기간)**|**대기 시간**|
|메일 보호 요약 보고서|90일|메시지 데이터 집계는 대부분 24~48시간 이내에 완료됩니다. 일부 사소한 증분 집계 변경의 경우 5일까지 소요될 수 있습니다.|
|메일 보호 세부 정보 보고서|90일|7일 미만의 세부 데이터는 24시간 이내에 표시되지만 48시간이 될 때까지 완료되지 않을 수 있습니다. 일부 사소한 증분 변경의 경우 5일까지 소요될 수 있습니다. <br/><br/> 7일이 지난 메시지에 대한 상세 보고서를 보려면 결과가 표시되는 데 최대 몇 시간이 걸릴 수 있습니다.|
|메시지 추적 데이터|90일|7일 미만의 메시지에 대해 메시지 추적을 실행하면 메시지가 5~30분 이내에 표시되어야 합니다.<br/><br/> 7일이 지난 메시지에 대해 메시지 추적을 실행하면 결과가 표시되는 데 최대 몇 시간이 걸릴 수 있습니다.|

> [!NOTE]
> 데이터 사용 가능 여부 및 대기 시간은 Microsoft 365 관리 센터 또는 원격 PowerShell을 통해 요청 된 경우와 동일 합니다. 
