---
title: 최종 사용자 스팸 알림을 사용하여 스팸으로 격리된 메시지 릴리스 및 보고
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4b250bc9-0056-4426-8397-7b4398f1b026
ms.collection:
- M365-security-compliance
description: '격리 된 전자 메일에 대 한 관리자 로부터 최종 사용자 스팸 알림 메시지를 보는 사용자는 메시지에 대해 이러한 작업을 수행할 수 있습니다. '
ms.openlocfilehash: f9a8cdf21dfae631b311651aa2259af2f76d73b8
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30691977"
---
# <a name="use-end-user-spam-notifications-to-release-and-report-spam-quarantined-messages"></a>최종 사용자 스팸 알림을 사용하여 스팸으로 격리된 메시지 릴리스 및 보고

[![TechNet에서 support.office.com로 이동하는 콘텐츠에 대한 이미지 텍스트](media/ab7c897a-4798-4f31-8c84-f17a8409b133.png)](https://go.microsoft.com/fwlink/p/?LinkID=624152)
  
관리자가 최종 사용자 스팸 알림을 사용하도록 설정하는 경우 사서함으로 전송되지 않고 스팸으로 식별되어 격리된 메시지 목록이 포함된 알림 메시지를 수신하게 됩니다. 이 메시지에는 스팸 격리된 여러 메시지가 나열되어 있으며, 이 목록에는 마지막 메시지의 날짜와 시간(UTC(Universal Coordinated Time))이 포함됩니다. 이 목록에서 각 메시지에 대한 다음 정보를 확인할 수 있습니다. 
  
- **보낸 사람** 격리된 메시지의 보낸 사람 이름과 전자 메일 주소입니다. 
    
- **제목** 격리된 메시지의 제목 줄 텍스트입니다. 
    
- **날짜** 메시지가 격리된 날짜와 시간(UTC)입니다. 
    
- **크기** 격리된 메시지의 크기(KB)입니다. 
    
각 메시지에 대해 다음 작업을 수행할 수 있습니다.
  
- **받은 편지함으로 릴리스** 이 링크를 클릭하면 메시지를 볼 수 있는 받은 편지함으로 메시지가 전송됩니다. 
    
- **정크 메일 아님으로 보고** 이 링크를 클릭하면 분석을 위해 메시지 복사본이 Microsoft로 전송됩니다. 스팸 팀은 메시지를 평가 및 분석하고 분석 결과에 따라 메시지 통과를 허용하도록 스팸 방지 필터 규칙을 조정합니다. 
    
> [!NOTE]
>  메일 흐름 규칙 (a) 일치로 인해 격리 된 메시지는 최종 사용자 스팸 격리 메시지에 포함 되지 않습니다. 스팸 격리된 메시지만 나열됩니다. >  메시지를 릴리스하고 가양성으로(정크 아님) 한 번만 보고할 수 있습니다. 
  

