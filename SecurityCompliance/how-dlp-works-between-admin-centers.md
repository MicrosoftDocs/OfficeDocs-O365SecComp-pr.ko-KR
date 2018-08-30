---
title: DLP 보안 간에 작동 하는 방법 &amp; 준수 센터 및 Exchange 관리 센터
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: 설명 어떻게 DLP 보안에 대 한 &amp; 준수 센터의 Exchange 관리 센터에서 DLP 및 전송 규칙을 통해 작동 합니다.
ms.openlocfilehash: bc7494f504c2c0ffa668562d6e64b9f29992e24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533775"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a>DLP 보안 간에 작동 하는 방법 &amp; 준수 센터 및 Exchange 관리 센터

Office 365에서 두 서로 다른 관리 센터에서 데이터 손실 방지 (DLP) 정책을 만들 수 있습니다.
  
- **보안 &amp; 준수 센터**, SharePoint, OneDrive 및 Exchange의 콘텐츠를 보호 하는 단일 DLP 정책을 만들 수 있습니다. 가능한 경우에 여기에 DLP 정책을 만들 수는 하는 것이 좋습니다. 자세한 내용은 참조 [DLP 보안에 대 한 &amp; 준수 센터](data-loss-prevention-policies.md)합니다.
    
- **Exchange 관리 센터**Exchange에만 콘텐츠를 보호 하는 DLP 정책을 만들 수 있습니다. 이 정책은 하려면 기타 옵션을 특정 전자 메일을 처리 않았으므로 Exchange 전송 규칙을 사용할 수 있습니다. 자세한 내용은 [DLP Exchange 관리 센터에 대 한](https://go.microsoft.com/fwlink/?linkid=852311)참조입니다.
    
DLP 정책 이러한 관리에서 만든 센터 작동 나란히-이 항목에 설명 방법입니다.
  
![보안 및 규정 준수 센터 및 Exchange 관리 센터에서 DLP 페이지](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a>어떻게 DLP 보안에 대 한 &amp; Exchange 관리 센터에서 DLP 및 전송 규칙을 통해 작동 하는 준수 센터

보안에서 DLP 정책을 만든 후 &amp; 정책을 준수 센터의 모든 정책에 포함 된 위치에 배포 됩니다. 정책 Exchange Online을 포함 하는 경우 정책의 다음과 같은 동기화 및 Exchange 관리 센터에서 만든 DLP 정책으로 동일한 방식으로 정확 하 게 적용 합니다. 
  
DLP 정책에서 Exchange 관리 센터를 만들고 나면 하는 경우 해당 정책이 계속 작동 보안에서 만든 전자 메일에 대 한 모든 정책 나란히 &amp; 준수 센터입니다. 그러나 Exchange 관리 센터에서 만든 규칙 우선 합니다. 모든 Exchange 전송 규칙은 먼저 처리 하 고 보안에서는 DLP 규칙은 다음 &amp; 준수 센터 처리 됩니다.
  
의미합니다.
  
- Exchange 전송 규칙에 의해 차단 되는 메시지 보안에서 만든 DLP 규칙에 의해 검색 되지 않음 &amp; 준수 센터입니다.
    
- Exchange 전송 규칙 보안에서 DLP 정책과 일치 하도록 할 수 있는 방식으로 메시지를 수정 하는 경우 &amp; 추가 외부 사용자에 게-다음 DLP 규칙에서이 발견 하 고 필요에 따라 정책을 적용 하는 등의 준수 센터-합니다.
    
Exchange 전송 규칙 "처리를 중지" 매크로 함수를 사용 하는 DLP의 처리에 영향을 주지 메모 보안에서 규칙은 또한 &amp; 준수 센터-처리 계속 표시 됩니다.
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a>정책 팁 (영문) 보안에서 &amp; 준수 센터 Exchange 관리 센터와 비교

정책 팁 수 DLP 정책 중 하나를 사용 하 고 메일 흐름 규칙 또는 보안에서 만든 DLP 정책을 사용 하 여 Exchange 관리 센터에서 만든 &amp; 준수 센터 하지만 둘 중 하나입니다. 단일 위치에서만 정책 팁을 그릴 수 있지만 이러한 정책은 다른 위치에 저장 된 때문입니다.
  
Exchange 관리 센터에서 보안을 구성 하는 모든 정책 팁의 정책 팁을 구성한 경우 &amp; 준수 센터 웹에 있는 Outlook 및 Outlook 2013 및 Exchange 관리 센터의 팁을 끌 때까지 이상에서 사용자에 게 표시 되지 않습니다. 이렇게 하면 하 여 현재 Exchange 전송 규칙을 계속 작동을 통해 보안을 전환 하도록 선택할 때까지 &amp; 준수 센터입니다.
  
정책 팁을 단일 위치 에서만에서 그릴 수 하는 동안 알림 전자 메일을 하는 내용의 항상 전송, 모두 보안에서 DLP 정책을 사용 하는 경우에 &amp; 준수 센터 및 Exchange 관리 센터입니다.
  

