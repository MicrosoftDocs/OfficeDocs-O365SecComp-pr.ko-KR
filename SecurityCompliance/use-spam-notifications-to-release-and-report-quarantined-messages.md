---
title: Office 365에서 사용자 스팸 알림을 사용하여 격리된 메시지 릴리스 및 보고
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
description: 관리자가 사용자에 게 알림을 사용 하도록 설정 하는 경우 사서함에 전송 된 메시지를 스팸, 대량 또는 피싱 메시지로 식별 하는 알림 메시지가 표시 됩니다. 알림을 받은 후에는 메시지를 해제 하거나 보고할 수 있습니다.
ms.openlocfilehash: eb51d8f73ff00781b74cfba4e580668710ce7a76
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216398"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a>Office 365에서 사용자 스팸 알림을 사용하여 격리된 메시지 릴리스 및 보고

관리자가 사용자에 대 한 스팸 알림을 사용 하도록 설정 하는 경우 사서함으로 주소가 지정 되어 스팸으로 식별 되 고 대신 격리 된 메시지를 나열 하는 알림 메시지가 수신 됩니다.
  
> [!TIP]
> 관리자가이 기능을 사용 하도록 설정 하려는 경우에는 [기본 스팸 방지 정책을 수정](https://go.microsoft.com/fwlink/?LinkId=800313)하는 경우 옵션을 선택할 수 있습니다. 
  
수신 되는 메시지에는 스팸 격리 된 메시지의 수와 목록에 있는 마지막 메시지의 날짜와 시간 (utc (Universal 협정 세계시))이 포함 됩니다. 이 목록에는 각 메시지에 대 한 다음이 포함 됩니다.
  
- **보낸 사람** 격리 된 메시지의 보내기 이름 및 전자 메일 주소입니다. 
    
- **제목** 격리된 메시지의 제목 줄 텍스트입니다. 
    
- **날짜** 메시지가 격리된 날짜와 시간(UTC)입니다. 
    
- **크기** kb (kb) 단위의 메시지 크기입니다. 
    
현재 격리 된 메시지를 사용 하 여 수행할 수 있는 작업은 다음 두 가지입니다.
  
- **받은 편지 함으로 릴리스** 메시지를 볼 수 있는 받은 편지 함으로 보내려면이 방법을 선택 합니다. 
    
- **정크 메일 아님으로 보고** 분석을 위해 Microsoft에 메시지 복사본을 보내려면이 방법을 선택 합니다. 스팸 팀은 메시지를 평가 및 분석 하 고 분석 결과에 따라 메시지 통과를 허용 하도록 스팸 방지 필터 규칙을 조정 합니다. 
    
다음에 대해 숙지 합니다.
  
- 메일 흐름 규칙과 일치 하기 때문에 격리 된 메시지는 사용자 격리 된 메시지에 포함 되지 않습니다. 스팸 격리 된 메시지만 나열 됩니다.
    
- 메시지를 릴리스하고 가양성으로(정크 아님) 한 번만 보고할 수 있습니다.
    

