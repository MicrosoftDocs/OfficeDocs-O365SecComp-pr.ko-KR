---
title: Office 365에 대 한 mdm 장치 등록 문제를 해결합니다
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/17/2015
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c863b2bf-45f3-483a-ba05-29fc7f4d6434
description: Office 365에 대 한 장치에서 모바일 장치 관리 (MDM)을 등록 하려고 하는 경우 문제를 실행 하는 경우 문제를 추적 하려면 여기에 나열 된 단계를 시도 합니다. 일반적인 단계는이 문제를 해결 하지 장치 유형에 대 한 특정 단계와 뒷부분에 나오는 섹션 중 하나를 참조 합니다.
ms.openlocfilehash: 490259fc623b38ab5ad6cf8553c5074c77b77426
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272113"
---
# <a name="troubleshoot-device-enrollment-with-mdm-for-office-365"></a>Office 365에 대 한 mdm 장치 등록 문제를 해결합니다

Office 365에 대 한 장치에서 모바일 장치 관리 (MDM)을 등록 하려고 하는 경우 문제를 실행 하는 경우 문제를 추적 하려면 여기에 나열 된 단계를 시도 합니다. 일반적인 단계는이 문제를 해결 하지 장치 유형에 대 한 특정 단계와 뒷부분에 나오는 섹션 중 하나를 참조 합니다.
  
## <a name="steps-to-try-first"></a>먼저 시도 하는 단계

를 시작 하려면 다음을 확인 합니다.
  
- 장치 Intune 등의 다른 모바일 장치 관리 공급자와 함께 이미 등록 되지 않은 있는지 확인 하십시오.
    
- 장치 올바른 날짜와 시간으로 설정 되어있는지 확인 합니다.
    
- 다른 Wi-fi 또는 장치에 셀룰러 네트워크로 전환
    
- Android 또는 iOS 장치에 대 한 제거 하 고 장치에 Intune 회사 포털 응용 프로그램을 다시 설치 합니다.
    
## <a name="ios-phone-or-tablet"></a>iOS 휴대폰 또는 태블릿

- [한 apn을 사용할 인증서를 설정](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7)했을 때 있는지 확인 하십시오.
    
- **설정** 에서 \> **일반** \> **프로필** (또는 **장치 관리**), **관리 프로 파일** 을 아직 설치 되지 않은 있는지 확인 합니다. 인 경우이 제거 합니다. 
    
- "장치를 등록 하려면 실패" 오류 메시지를 표시 하는 경우 Office 365에 로그인 하 고 사용자가 장치에 로그인의 Exchange Online을 포함 하는 라이선스가 할당 된 있는지 확인 합니다.
    
- "프로필을 설치 하려면 실패" 오류 메시지를 표시 하는 경우 다음 중 하나를 수행 합니다.
    
  - Safari 장치에서 기본 브라우저 인지 하 고 쿠키가 비활성화 되어 있는지 확인 하십시오.
    
  - 장치를 다시 부팅 한 다음 portal.manage.microsoft.com로 이동, Office 365 사용자 ID 및 암호를 사용 하 여 로그인 및 프로필을 수동으로 설치 하려고 합니다.
    
## <a name="windows-rt-tablet"></a>Windows RT 태블릿

- 도메인 [MDM 함께 작동 하도록 Office 365에서 설정](set-up-mobile-device-management.md)인지 확인 합니다.
    
- 사용자가 **설정에서** 선택 하지 않고 **참가**선택 되어있는지 확인 합니다.
    
## <a name="windows-phone"></a>Windows Phone

- 도메인 [MDM 함께 작동 하도록 Office 365에서 설정](set-up-mobile-device-management.md)인지 확인 합니다.
    
- 장치가 Windows 8.1 이상을 실행 중인지 확인 합니다.
    
## <a name="android-phone-or-tablet"></a>Android 휴대폰 또는 태블릿

- 장치 Android 4.0 이상 실행 중인지 확인 합니다.
    
- "이이 장치는 등록할 수 없습니다." 오류 메시지를 표시 하는 경우 Office 365에 로그인 하 고 사용자가 장치에 로그인의 Exchange Online을 포함 하는 라이선스가 할당 된 있는지 확인 합니다.
    
- 필요한 최종 사용자 작업이 보류 중인, 있는지 확인 하는 장치에서 **알림 영역** 확인 하 고 동일한 경우 작업을 완료 합니다. 
    

