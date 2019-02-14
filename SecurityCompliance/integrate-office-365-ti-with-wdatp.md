---
title: Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection: M365-security-compliance
description: 보다 자세한 위협 관리 정보를 보려면 Windows Defender 고급 위협 보호와 Office 365 고급 위협 보호를 통합 합니다.
ms.openlocfilehash: f8f5f50af10fb668aa67b68604e95e8dd19c9e69
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995209"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합

조직의 보안 팀의 일부인 경우에 Windows Defender 고급 위협 보호 된 Office 365 고급 위협 보호 및 위협 인텔리전스 기능을 통합할 수 있습니다. 이 신속 하 게 하는 경우 사용자의 컴퓨터를 위험이 Office 365에 대 한 위협 요소를 조사 하는 경우를 이해할 수 있습니다. 등의 통합을 사용 하는 사용 하도록 설정 하면 많은 최근 경고 Windows Defender 고급 위협 보호 있는 이러한 장치와 어떻게 검색 된 전자 메일 메시지의 받는 사람에 사용 되는 컴퓨터의 목록도 참조 할 수를 합니다.
  
다음 이미지에서 확인할 수 있는 Windows Defender 고급 위협 보호 통합을 사용 하도록 설정한 경우 표시 됩니다 **장치** 탭에서: 
  
![Windows Defender ATP 사용 하는 경우 알림 사용 하는 컴퓨터의 목록을 볼 수 있습니다.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
이 예제에서는 전자 메일 메시지의 받는 사람에 게 4 개의 장치 하 고 알림을 한 명 있는지 확인할 수 있습니다. 장치에 대 한 링크를 클릭 하는 Windows Defender 고급 위협 보호 포털에서 해당 페이지를 엽니다.
  
## <a name="requirements"></a>요구 사항

- 조직에 Office 365 위협 인텔리전스 및 Windows Defender ATP 있어야 합니다.
    
- Office 365 전역 관리자 이거나에 할당 된 보안 관리자 역할 (예: 보안 관리자)는 [보안 &amp; 준수 센터](https://protection.office.com)합니다. (참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md))
    
- Office 365 위협 인텔리전스와 Windows Defender 고급 위협 보호 포털에 액세스할 수 있어야 합니다.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Windows Defender ATP와 Office 365 위협 인텔리전스를 통합 하려면

규정 준수 센터 및 Windows Defender 고급 위협 보호 포털 Office 365 보안 &는 모두를 사용 하 여 Windows Defender 고급 위협 보호 된 Office 365 위협 인텔리전스 통합 (영문) 기능이 설정 됩니다.
  
1. Office 365 전역 관리자 또는 보안 관리자도로 이동 [https://protection.office.com](https://protection.office.com) 와 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. 
    
2. **위협 관리** 를 선택 \> **탐색기**입니다.<br>![위협 관리 메뉴에서 탐색기](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. 화면 오른쪽 위 모서리에서 **WDATP 설정**을 선택 합니다.
    
4. Windows Defender ATP 연결 대화 상자에서 Windows ATP에 연결을 설정 합니다.<br>![Windows Defender ATP 연결](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Windows Defender 고급 위협 보호에 대 한 연결을 사용 하도록 설정 합니다. [Windows Defender 고급 위협 보호 포털 사용](https://go.microsoft.com/fwlink/?linkid=859690)을 참조 하십시오.

  
## <a name="related-topics"></a>관련 항목

[Office 365 위협 인텔리전스](office-365-ti.md)
  
[Office 365 Advanced Threat Protection 방지](office-365-atp.md)
  

