---
title: 정크 메일과 대량 전자 메일의 차이점
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/7/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
description: 고객 askwhat 정크 메일과 대량 전자 메일 메시지의 차이점을의 하는 경우가 있습니까? 이 항목의 목적은 차이 파악 하 고 Exchange Online 및 Exchange Online Protection (EOP)에서 모두에 대해 사용할 수 있는 다양 한 옵션에 대 한 정보를 제공 합니다.
ms.openlocfilehash: 2cd9d9d91cf44af910983c045192ed7639d27417
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026245"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a>정크 메일과 대량 전자 메일의 차이점

고객이 "정크 메일 메시지와 대량 전자 메일 메시지 간의 차이점"을 물어보는 경우가 있습니다. 이 항목에서는 차이점을 설명하고 Exchange Online과 EOP(Exchange Online Protection) 둘 다에서 사용 가능한 여러 옵션에 대해 알아봅니다.
  
 **정크 메일이란?**
  
정크 메일 메시지는 서비스에 의해 필터링되는 원치 않는(그리고 일반적으로 불필요한) 이메일 메시지인 "스팸" 메시지입니다. 기본적으로 서비스에서는 보내는 IP 주소의 신뢰도에 따라 스팸 메시지를 거부합니다. 그러나 IP 검사를 통과했지만 콘텐츠 필터에 의해 스팸으로 분류된 메시지는 지정된 받는 사람의 정크 메일 폴더로 전송됩니다. 
  
> [!NOTE]
> 콘텐츠 필터링 된 메시지에서 수행 되는 작업은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에서 설명한 것 처럼 Exchange 관리 센터 (EAC)에서 콘텐츠 필터 정책을 통해 구성할 수 있습니다. 또한 스팸 분류와 동의할 수 없는 경우에 [전송 스팸, 스팸이 아닌 및 분석을 위해 Microsoft에 피싱 사기 메시지에서](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)설명한 대로 스팸 또는 스팸이 아닌 Microsoft에 다양 한 방식에서에 고려 하는 메시지를 보고할 수 있습니다. 
  
 **대량 전자 메일이란?**
  
그레이 메일이라고도 하는 대량 전자 메일은 보다 분류하기 어려운 유형의 전자 메일 메시지입니다. 정크 메일은 지속적인 위협인 반면, 대량 전자 메일은 대개 반복적으로 수신되지 않는 광고 또는 마케팅 메시지로 구성됩니다. 사용자에 따라 대량 전자 메일을 원하는 경우(실제로 이들은 이러한 메시지를 받도록 의도적으로 등록함)도 있고 이러한 유형의 메시지를 스팸으로 간주하는 경우도 있습니다. 예를 들어 어떤 사용자는 Contoso Corporation의 광고 전자 메일 또는 사이버 위협에 대한 예정된 회의의 초대를 받기를 원하지만 그렇지 않은 사용자는 이러한 전자 메일을 스팸으로 간주합니다.
  
## <a name="how-to-manage-bulk-email"></a>대량 전자 메일을 관리하는 방법

대량 전자 메일을 관리하는 방법은 하나로 단정지을 수 없습니다. 모든 대량 전자 메일이 스팸으로 분류된 경우 이러한 전자 메일을 원하는 사용자는 불만이 있을 수 있으며 이를 스팸으로 잘못 표시된 가양성(스팸 아님) 메시지로 제출할 수 있습니다. 반면, 모든 대량 전자 메일이 허용되는 경우 이러한 전자 메일을 원치 않는 사용자는 불만이 있을 수 있으며 이를 자신의 받은 편지함에 잘못 도착한 누락된 스팸 메시지(거짓 부정)로 제출할 수 있습니다.
  
### <a name="enable-bulk-mail-sensitivity-control-in-the-content-filter-policy"></a>콘텐츠 필터 정책에 대량 메일 민감도 제어를 사용 하도록 설정

대량 전자 메일 메시지에 회사의 정책에 따라 관리자 대량 전자 메일을 할당 하는 임계값을 선택할 수 있습니다. 설정 하는 것은 EAC에서 콘텐츠 필터 정책을 통해 구성할 수 있습니다. [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)체크아웃)의 단계에 대 한 합니다. 1-9, 여기서 1 스팸으로, 대부분 대량 전자 메일을 표시 하 고 9 허용 배달 하지 대부분 대량 전자 메일에서에서 임계값 설정을 선택할 수 있습니다. 서비스에서 받는 사람의 정크 메일 폴더로 메시지를 보내는 것과 같은 구성된 작업을 수행 합니다. 
  

