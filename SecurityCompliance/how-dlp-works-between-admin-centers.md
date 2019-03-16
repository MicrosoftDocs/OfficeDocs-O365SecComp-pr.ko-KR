---
title: 보안 & 준수 센터와 Exchange 관리 센터 간에 DLP가 작동 하는 방식
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Exchange 관리 센터에서 dlp 및 메일 흐름 규칙 (전송 규칙)을 통해 보안 & 준수 센터의 dlp가 작동 하는 방식을 알아봅니다.
ms.openlocfilehash: 66dceb447e02eb01810997c23644c76f68795844
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/16/2019
ms.locfileid: "30639005"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a>보안 & 준수 센터와 Exchange 관리 센터 간에 DLP가 작동 하는 방식

Office 365에서는 다음과 같은 두 가지 다른 관리 센터에서 DLP (데이터 손실 방지) 정책을 만들 수 있습니다.
  
- **보안 & 준수 센터**에서는 SharePoint, OneDrive 및 Exchange의 콘텐츠를 보호 하는 데 도움이 되는 단일 DLP 정책을 만들 수 있습니다. 가능한 경우 여기에서 DLP 정책을 만드는 것이 좋습니다. 자세한 내용은 [Security & 준수 센터의 DLP](data-loss-prevention-policies.md)를 참조 하세요.
    
- **exchange 관리 센터**에서는 exchange 에서만 콘텐츠를 보호 하는 데 필요한 DLP 정책을 만들 수 있습니다. 이 정책은 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 사용 하 여 전자 메일을 처리 하는 데 관련 된 추가 옵션을 사용할 수 있습니다. 자세한 내용은 [Exchange 관리 센터의 DLP](https://go.microsoft.com/fwlink/?linkid=852311)를 참조 하세요.
    
이 관리 센터에서 만든 DLP 정책은 나란히 있습니다 .이 항목에서는 방법에 대해 설명 합니다.
  
![보안 및 준수 센터 및 Exchange 관리 센터의 DLP 페이지](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a>Exchange 관리 센터에서 dlp 및 메일 흐름 규칙을 사용 하 여 보안 & 준수 센터의 dlp가 작동 하는 방식

Security & 준수 센터에서 DLP 정책을 만들면 정책이 정책에 포함 된 모든 위치에 배포 됩니다. 정책에 exchange Online이 포함 되어 있는 경우 정책이 exchange 관리 센터에서 만든 DLP 정책과 정확히 같은 방식으로 동기화 되 고 적용 됩니다. 
  
Exchange 관리 센터에서 DLP 정책을 만든 경우 이러한 정책은 계속 해 서 보안 & 준수 센터에서 만드는 전자 메일에 대 한 정책과 함께 나란히 작동 합니다. 그러나 Exchange 관리 센터에서 만든 규칙이 우선적으로 적용 됩니다. 모든 Exchange 메일 흐름 규칙이 먼저 처리 된 다음 Security & 준수 센터의 DLP 규칙이 처리 됩니다.
  
즉, 다음을 의미 합니다.
  
- Exchange 메일 흐름 규칙에 의해 차단 된 메시지는 Security & 준수 센터에서 만든 DLP 규칙으로 검색 되지 않습니다.
    
- Exchange 메일 흐름 규칙에서 메시지를 수정 하 여 외부 사용자 추가와 같은 보안 & 준수 센터의 dlp 정책과 일치 하도록 하는 경우 dlp 규칙이이를 감지 하 고 필요에 따라 정책을 적용 합니다.
    
또한 "처리 중지" 작업을 사용 하는 Exchange 메일 흐름 규칙은 보안 & 준수 센터의 DLP 규칙 처리에 영향을 주지 않으며 여전히 처리 됩니다.
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a>보안 & 준수 센터 및 Exchange 관리 센터의 정책 팁

정책 팁은 Exchange 관리 센터에서 만든 dlp 정책 및 메일 흐름 규칙 또는 보안 & 준수 센터에서 만든 dlp 정책을 사용 하거나 둘 다 사용할 수 없습니다. 이러한 정책은 서로 다른 위치에 저장 되어 있지만 정책 팁은 단일 위치 에서만 그릴 수 있기 때문입니다.
  
exchange 관리 센터에서 정책 팁을 구성한 경우 보안 & 준수 센터에서 구성한 정책 팁은 웹 및 outlook 2013에서 outlook의 사용자에 게 표시 되지 않으며 Exchange 관리 센터에서 팁을 해제할 때까지 적용 됩니다. 이렇게 하면 보안 & 준수 센터로 전환 하도록 선택할 때까지 현재 Exchange 메일 흐름 규칙이 계속 작동 합니다.
  
정책 팁은 단일 위치 에서만 그릴 수 있지만, 보안 & 준수 센터와 Exchange 관리 센터 둘 다에서 DLP 정책을 사용 하는 경우에도 전자 메일 알림이 항상 전송 됩니다.
  

