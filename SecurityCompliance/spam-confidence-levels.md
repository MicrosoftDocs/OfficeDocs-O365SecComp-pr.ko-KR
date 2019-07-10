---
title: 스팸 지수
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 10/02/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: 전자 메일 메시지가 스팸 필터링을 통과 하면 스팸 점수가 할당 됩니다. 이 점수는 개별 SCL (스팸 지 수) 등급에 매핑되며 X-헤더에 스탬프 처리 됩니다. 이 서비스는 SCL 등급의 스팸 신뢰 해석에 따라 메시지에 대 한 작업을 수행 합니다. 다음 표에서는 각 등급에 대 한 인바운드 메시지에 대해 수행 되는 필터 및 각 SCL 등급이 해석 되는 방식을 보여 줍니다.
ms.openlocfilehash: beb322341f4d0de25d7bac9681c0beed93c48e5f
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600878"
---
# <a name="spam-confidence-levels"></a>스팸 지수

전자 메일 메시지가 스팸 필터링을 통과 하면 스팸 점수가 할당 됩니다. 이 점수는 개별 SCL (스팸 지 수) 등급에 매핑되며 X-헤더에 스탬프 처리 됩니다. 이 서비스는 SCL 등급의 스팸 신뢰 해석에 따라 메시지에 대 한 작업을 수행 합니다. 다음 표에서는 각 등급에 대 한 인바운드 메시지에 대해 수행 되는 필터 및 각 SCL 등급이 해석 되는 방식을 보여 줍니다.
  
|**SCL 등급**|**Scl (스팸 지 수) 해석**|**기본 작업**|
|:-----|:-----|:-----|
|-1|수신 허용-보낸 사람, 수신 허용-받는 사람 또는 안전한 것으로 표시 된 IP 주소 (신뢰할 수 있는 파트너)에서 오는 스팸 방지|받는 사람의 받은 편지 함으로 메시지를 배달 합니다.|
|0, 1|메시지가 검사 되었으며 깨끗 한 것으로 확인 되었기 때문에 스팸 아님|받는 사람의 받은 편지 함으로 메시지를 배달 합니다.|
|5, 6|스팸|받는 사람의 정크 메일 폴더로 메시지를 배달 합니다.|
|7, 8, 9|높은 정확도 스팸|받는 사람의 정크 메일 폴더로 메시지를 배달 합니다.|
   
> [!TIP]
> 2, 3, 4, 7 및 8의 SCL 등급이 서비스에 의해 설정 되지 않습니다. SCL 등급 5 또는 6은 스팸이 아닌 것으로 간주 되며, SCL 등급 9 보다 스팸을 덜 하 여 특정 스팸으로 간주 됩니다. 스팸 및 높은 신뢰도 스팸에 대 한 다양 한 작업은 Exchange 관리 센터에서 콘텐츠 필터 정책을 통해 구성할 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요. 또한 [메일 흐름 규칙을 사용 하 여 메시지에 scl (스팸 지 수)을 설정 하는 방법](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)에 설명 된 대로 메일 흐름 규칙 (전송 규칙이 라고도 함)을 사용 하 여 특정 조건과 일치 하는 메시지에 대 한 SCL 등급을 설정할 수 있습니다. 메일 흐름 규칙을 사용 하 여 SCL 7, 8 또는 9를 설정 하는 경우 메시지가 높은 신뢰도 스팸으로 취급 됩니다. 
  
||
|:-----|
|![LinkedIn Learning용 단축 아이콘](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Office 365를 처음 사용하시나요?**         LinkedIn Learning에서 제공하는 **Office 365 admins and IT pros**의 무료 비디오 과정을 확인해보세요.|
   

