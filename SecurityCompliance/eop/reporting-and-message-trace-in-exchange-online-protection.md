---
title: Exchange Online Protection의 보고 및 메시지 추적
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: Microsoft EOP(Exchange Online Protection)에서는 조직의 전체 상태를 확인할 수 있는 다양한 보고서를 제공합니다. 받는 사람에게 메시지가 도착하지 않는 등 특정 이벤트에 대한 문제를 해결할 수 있는 도구와 규정 준수 요구 사항을 지원하는 감사 보고서도 있습니다. 다음 표에서는 EOP 관리자가 사용할 수 있는 보고서 및 문제 해결 도구를 설명합니다.
ms.openlocfilehash: 01a09b2b4b72161352af3793686c6cc888e44e29
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027145"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a>Exchange Online Protection의 보고 및 메시지 추적

Microsoft Exchange Online Protection (EOP)은 하는데 도움이 되는 여러 다른 보고서의 전반적인 상태 확인 하 여 조직의 제공 합니다. 또한 (예: 메시지의 받는 사람에 게 도착 하지), 특정 이벤트 문제를 해결 하는데 도움이 되는 도구 및 규정 준수 요구 사항을 지원 하기 위해 감사 보고서 있습니다. 

## <a name="usage-reports"></a>사용 현황 보고서

**Office 365 그룹 작업** 생성 하 고 사용 하는 Office 365 그룹의 수에 대 한 정보를 봅니다.  

**전자 메일 활동** 전송, 받은 메일 및 전체 조직에서 하 고 특정 사용자가 읽은 메시지 수에 대 한 정보를 봅니다.  

**전자 메일 응용 프로그램 사용** 사용 되는 전자 메일 응용 프로그램에 대 한 정보를 봅니다. 여기에 각 응용 프로그램에 대 한 연결의 총 수와 연결 하는 버전의 Outlook 포함 합니다.  

**사서함 사용량** 사용 되는 저장소에 대 한 정보, 할당량 소비, 항목 수 및 사서함에 대 한 마지막 활동 (보내기 또는 읽기 작업)을 봅니다.

자세한 내용은 다음 리소스를 참조 하십시오.

- [Office 365 관리 센터-Office 365의에서 보고서 그룹](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [Office 365 관리 센터-전자 메일 활동에에서는 보고서](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [관리 센터-전자 메일 응용 프로그램 사용에서에서 office 365 보고서](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [Office 365 관리 센터-사서함 사용량에에서는 보고서](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-office-365-admin-center"></a>보안 &amp; Office 365 관리 센터에서 준수 보고서

이러한 향상 된 보고서 요약 정보 및 자세한 내용은 드릴 다운 하는 기능을 포함 하는 EOP 관리자의 경우에 대 한 대화형 보고 경험을 제공 합니다.  

**고급 위협 보호 ATP)** 안전한 링크 및 ATP의 일부인 안전한 첨부 파일에 대 한 정보를 봅니다.  

**EOP** 맬웨어 감지, 위장 된 메일, 스팸 감지 및 조직에서 메일 흐름을 하는 방법에 대 한 정보를 봅니다.  

[고급 위협 보호 및 Exchange Online Protection에 대 한 보고서 보기](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a>다음은 Microsoft Graph를 사용 하 여 사용자 지정 보고서

프로그래밍 방식으로 Microsoft Graph 참조를 사용 하 여 Office 365 관리 센터에서 사용할 수 있는 보고서를 [Microsoft Graph에서 Office 365 사용 현황 보고서 사용 (영문)](https://go.microsoft.com/fwlink/p/?linkid=865135) 의 하위 항목 만들기 

##<a name="custom-reports-using-reporting-web-services"></a>보고 웹 서비스를 사용한 사용자 지정 보고서

프로그래밍 방식으로 사용할 수 있는 Exchange Online 보호 PowerShell REST/ODATA2 쿼리 필터링을 사용 하 여 보고 cmdlet에서에서 보고서를 만듭니다.

[Office 365 보고 웹 서비스](https://go.microsoft.com/fwlink/p/?LinkId=279926) 를 참조 하십시오. 

##<a name="message-trace"></a>메시지 추적

EOP를 통해 이동 되 전자 메일 메시지를 다음과 합니다. 전자 메일 메시지 수신, 거부, 지연, 또는 서비스에 의해 전달 되는 경우를 확인할 수 있습니다. 또한 최종 상태에 도달 하기 전에 메시지에 어떤 작업을 수행 했는지를 보여줍니다.  

효율적으로 사용자의 질문에 대답, 메일 흐름 문제를 해결, 정책 변경의 유효성을 검사 하려면이 정보를 사용할 수 및 지원에 대 한 기술 지원 서비스에 문의 필요가 줄어듭니다.  

[전자 메일 메시지 추적](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx) 참조 

## <a name="audit-logging"></a>감사 로깅

관리자가 수행한 조직의 특정 변경 내용을 추적 합니다. 이러한 보고서 구성 문제를 해결 하거나 보안 또는 규정 준수 관련 문제를의 원인을 찾을 수 있습니다.  [EOP에서 감사 보고서](auditing-reports-in-eop.md) 를 참조 하십시오. 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a>보고 및 메시지 추적 데이터 사용 가능 여부 및 대기 시간

다음 표에는 EOP 보고 및 메시지 추적 데이터를 사용할 수 있는 시기와 기간에 대한 설명이 나와 있습니다.
  
||||
|:-----|:-----|:-----|
|**보고서 유형** <br/> |**데이터 사용 가능 기간(확인 기간)** <br/> |**대기 시간** <br/> |
|메일 보호 요약 보고서  <br/> |90일  <br/> |메시지 데이터 집계는 대부분 24~48시간 이내에 완료됩니다. 일부 사소한 증분 집계 변경의 경우 5일까지 소요될 수 있습니다.  <br/> |
|메일 보호 상세 보고서  <br/> |90일  <br/> |7일 미만의 세부 데이터는 24시간 이내에 표시되지만 48시간이 될 때까지 완료되지 않을 수 있습니다. 일부 사소한 증분 변경의 경우 5일까지 소요될 수 있습니다.  <br/> 7일이 지난 메시지에 대한 상세 보고서를 보려면 결과가 표시되는 데 최대 몇 시간이 걸릴 수 있습니다.  <br/> |
|메시지 추적 데이터  <br/> |90일  <br/> |7일 미만의 메시지에 대해 메시지 추적을 실행하면 메시지가 5~30분 이내에 표시되어야 합니다.  <br/> 7일이 지난 메시지에 대해 메시지 추적을 실행하면 결과가 표시되는 데 최대 몇 시간이 걸릴 수 있습니다.  <br/> |
   
> [!NOTE]
> 데이터 사용 가능 여부 및 대기 시간은 Office 365 관리 센터 또는 원격 PowerShell을 통해 요청 여부. 
  

