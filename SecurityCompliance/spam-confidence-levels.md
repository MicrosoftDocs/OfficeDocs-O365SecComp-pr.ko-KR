---
title: 스팸 신뢰 수준
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
description: 스팸 필터링을 통해 전자 메일 메시지를 이동할 때 스팸 점수를 할당 됩니다. 해당 점수는 개별 스팸 SCL () 등급이에 매핑된 이며 X-헤더에 스탬프 처리 합니다. 서비스는 SCL 등급의 스팸 신뢰 해석에 따라 메시지에 따라 작업을 수행 합니다. 다음 표에서 서로 다른 메시지에 SCL 등급 필터와 각 등급에 대 한 인바운드 메시지에 소요 되는 기본 작업으로 해석 되는 방법을 보여줍니다.
ms.openlocfilehash: cd33f440828761ab8cb496d9eff07288d974514c
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026285"
---
# <a name="spam-confidence-levels"></a>스팸 신뢰 수준

스팸 필터링을 통해 전자 메일 메시지를 이동할 때 스팸 점수를 할당 됩니다. 해당 점수는 개별 스팸 SCL () 등급이에 매핑된 이며 X-헤더에 스탬프 처리 합니다. 서비스는 SCL 등급의 스팸 신뢰 해석에 따라 메시지에 따라 작업을 수행 합니다. 다음 표에서 서로 다른 메시지에 SCL 등급 필터와 각 등급에 대 한 인바운드 메시지에 소요 되는 기본 작업으로 해석 되는 방법을 보여줍니다.
  
|**SCL 등급**|**스팸 지 해석**|**기본 작업**|
|:-----|:-----|:-----|
|-1  <br/> |스팸이 아닌 수신 허용-보낸사람에서 들리는 수신 허용-받는 사람 또는 안전 하 게 보호 나열 된 IP 주소 (신뢰할 수 있는 파트너)  <br/> |받는 사람의 받은 편지 함으로 메시지를 배달 합니다.  <br/> |
|0, 1  <br/> |비-스팸 메시지를 검사 하 고 새로 것으로 확인 하기 때문에  <br/> |받는 사람의 받은 편지 함으로 메시지를 배달 합니다.  <br/> |
|5, 6  <br/> | 스팸  <br/> |받는 사람의 정크 메일 폴더로 메시지를 배달 합니다.  <br/> |
|7, 8, 9  <br/> |높은 정확도 스팸  <br/> |받는 사람의 정크 메일 폴더로 메시지를 배달 합니다.  <br/> |
   
> [!TIP]
> 2, 3, 4, 7 및 8의 메시지에 SCL 등급 서비스에 의해 설정 되지 않습니다. 5 또는 6 인치로의 SCL 등급이 특정 스팸 것으로 간주 되는 9의 SCL 등급이 보다 스팸일 불확실해 의심 되는 스팸 것으로 간주 됩니다. Exchange 관리 센터에서 콘텐츠 필터 정책을 통해 스팸 및 높은 정확도 스팸에 대 한 다른 작업을 구성할 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오. [신뢰도 scl (스팸) 메시지에 설정 하려면 사용 하 여 메일 흐름 규칙](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)의 설명에 따라 전송 규칙을 사용 하 여 특정 조건에 맞는 메시지에 대 한 SCL 등급을 설정할 수도 있습니다. 7, 8, 9의 SCL을 설정 하는 전송 규칙을 사용 하는 경우에 메시지 높은 정확도 스팸으로 처리 됩니다. 
  
||
|:-----|
|![LinkedIn Learning용 단축 아이콘](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Office 365를 처음 사용하시나요?**         LinkedIn Learning에서 제공하는 **Office 365 admins and IT pros**의 무료 비디오 과정을 확인해보세요. |
   

