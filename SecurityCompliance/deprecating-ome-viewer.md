---
title: 방식 Office 365 메시지 암호화 뷰어 앱
ms.author: krowley
author: kccross
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6336cabb-b06e-402f-9e85-8bb9eb4ce68f
ms.collection:
- M365-security-compliance
description: 2018 년 8 월 15 일에는 Android 및 Apple 스토어에서 Office 365 메시지 암호화 (OME) 뷰어 모바일 앱을 제거 합니다. Apple 및 Android 휴대폰에서 이전 버전의 OME을 사용 하 여 암호화 된 전자 메일 메시지 및 첨부 파일을 읽으려면 Office 365 메시지 암호화 뷰어 모바일 앱이 필요 합니다. OME Viewer 앱을 제거 하는 것 외에도 이전 버전의 OME는 다른 방법으로 변경 하지 않습니다.
ms.openlocfilehash: 0aa8ef0f2610284c1e897290c3f337804d78185b
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/28/2019
ms.locfileid: "30936678"
---
# <a name="deprecating-office-365-message-encryption-viewer-app"></a>방식 Office 365 메시지 암호화 뷰어 앱

2018 년 8 월 15 일에는 Android 및 Apple 스토어에서 Office 365 메시지 암호화 (OME) 뷰어 모바일 앱을 제거 합니다. Apple 및 Android 휴대폰에서 이전 버전의 OME을 사용 하 여 암호화 된 전자 메일 메시지 및 첨부 파일을 읽으려면 Office 365 메시지 암호화 뷰어 모바일 앱이 필요 합니다. OME Viewer 앱을 제거 하는 것 외에도 이전 버전의 OME는 다른 방법으로 변경 하지 않습니다.
  
## <a name="changes-beginning-august-2018"></a>8 월 2018부터 변경 되는 내용

지난 9 월에 발표 된 것 처럼, 사용자가 모바일 앱을 요구 하지 않고 조직 내부 또는 외부 사람에 게 암호화 된 메시지를 보낼 수 있도록 새 버전의 [Office 365 메시지 암호화](https://aka.ms/ome2017) 가 출시 되었습니다. 이후에는 다음과 같은 기능을 추가 했습니다. 
  
- [암호화 전용 서식 파일](https://aka.ms/encryptonly)
    
- [첨부 파일의 암호를 해독 하는 컨트롤](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Admin-control-for-attachments-now-available-in-Office-365/ba-p/204007)
    
이렇게 변경 하면 사용자가 8 월 1 일부 터 Office 365 메시지 암호화 뷰어 모바일 앱을 더 이상 다운로드할 수 없게 됩니다. 따라서 일부 Android 및 Apple 모바일 장치에서 메일 받는 사람은 이전 버전의 OME으로 암호화 된 메시지를 읽지 못할 수 있습니다. 그러나 데스크톱 브라우저를 통해 개인 컴퓨터에서 이러한 메시지를 계속 읽을 수 있습니다. 앱을 이미 다운로드 한 사용자는 계속 사용할 수 있습니다.
  
## <a name="why-this-change-was-made"></a>변경이 수행 된 이유

새 버전의 OME에서는 보호 된 전자 메일 메시지 및 첨부 파일을 읽기 위해 모바일 앱이 더 이상 필요 하지 않습니다. office 365 새 OME 기능을 사용 하는 고객은 Outlook mobile 및 비 Office 365 고객의 보호 된 메시지를 볼 수 있습니다 브라우저에서 보호 된 메시지를 볼 수 있습니다.
  
사용자가 모바일 앱을 다운로드 하도록 요구 하는 것은 고객이 보호 된 메시지를 볼 수 있는 또 다른 hurdle입니다. 새로운 Office 365 메시지 암호화 기능은 모바일 환경을 향상 시킵니다.
  
## <a name="can-i-still-use-the-previous-version-of-office-365-message-encryption"></a>이전 버전의 Office 365 메시지 암호화를 계속 사용할 수 있나요?

이전 버전의 office 365 메시지 암호화는 더 이상 사용 되지 않을 예정 이지만, 새 버전의 office 365 메시지 암호화를 크게 개선 하 여 중요 한 데이터를 더 쉽게 암호화 하 고 권한을 보호할 수 있도록 합니다. 그리고 Office 365 사용자가 Outlook에서 직접 보호 된 메시지를 읽을 수 있는 기능을 포함 하는 모든 장치 (데스크톱, 모바일 및 웹) 
  
## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a>이 변경 사항을 준비 하기 위해 수행 해야 하는 작업

현재 조직에서 OME Viewer 앱이 필요한 받는 사람에 게 암호화 된 첨부 파일을 보내는 경우 설명서 및 교육 리소스를 업데이트 해야 합니다.
  
조직이 최신 버전의 OME를 사용 하 여 새로운 기능과 향상 된 기능을 활용할 수 있도록 기존 Exchange 메일 흐름 규칙을 업데이트 하는 것이 좋습니다. 새 OME 기능을 설정한 후에는 받는 사람에 게 OME Viewer 앱이 모바일 장치에서 암호화 된 메시지를 읽을 필요가 없습니다.
  
조직에 적합 한 시기에 새 OME 기능으로 바로 이동 하는 계획을 수립 하는 것이 좋습니다. 자세한 내용은 [Office 365 메시지 암호화 기능 새로 만들기](set-up-new-message-encryption-capabilities.md)를 참조 하세요. 새 기능이 먼저 작동 하는 방식에 대해 자세히 알아보려면 [Office 365 메시지 암호화](ome.md)를 참조 하세요.
  

