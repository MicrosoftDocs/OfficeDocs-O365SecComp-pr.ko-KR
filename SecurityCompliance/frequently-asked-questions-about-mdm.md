---
title: 질문과 대답 (영문) 모바일 장치 관리에 대 한 Office 365에 대 한
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 3871f99c-c9db-4a23-86f9-902c1b02f58d
description: 이 문서는 Office 365를 관리 하 고 Office 365의 모바일 장치를 보호 하는데 도움이 되는 기능에 대 한 자주 묻는 질문에 대 한 모바일 장치 관리 (MDM)를 포함 합니다.
ms.openlocfilehash: 6c4a5b3603d392b3d83769cd0f17450ce70565be
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272273"
---
# <a name="frequently-asked-questions-about-mobile-device-management-for-office-365"></a>질문과 대답 (영문) 모바일 장치 관리에 대 한 Office 365에 대 한

이 문서는 Office 365를 관리 하 고 Office 365의 모바일 장치를 보호 하는데 도움이 되는 기능에 대 한 자주 묻는 질문에 대 한 모바일 장치 관리 (MDM)를 포함 합니다.
  
## <a name="faqs"></a>FAQ

- [Office 365에 대 한 MDM를 어떻게 얻을 수 있습니까? Office 365 관리 센터에 표시 되지 않습니다.](#how-can-i-get-mdm-for-office-365-i-dont-see-it-in-the-office-365-admin-center)
    
- [어떻게 수 시작 MDM 장치 관리](#how-can-i-get-started-with-device-management-in-mdm)
    
- [MDM을 설정 하려고 하지만 걸린 것 처럼 보입니다. 잠시 자리를 "준비" Office 365 서비스 상태를 보여주는 되었습니다. 무엇을 도와드릴까요?](#im-trying-to-set-up-mdm-but-it-seems-stuck-the-office-365-service-health-has-been-showing-provisioning-for-a-while-what-can-i-do)
    
- [장치 등록에 실패 하는 경우 어떻게 해야 합니까?](#what-can-i-do-if-device-enrollment-fails)
    
- [Intune 및 Office 365에 대 한 MDM 간의 차이 무엇입니까?](#whats-the-difference-between-intune-and-mdm-for-office-365)
    
- [MDM에 대 한 정책은 어떻게 작동 합니까? 어떻게 수행 설정 하 시겠습니까? 없도록?](#how-do-policies-work-for-mdm-how-do-i-set-them-up-disable-them)
    
- [I 전환할 수 Exchange ActiveSync 장치 관리에서 MDM Office 365에 대 한?](#can-i-switch-from-exchange-activesync-device-management-to-mdm-for-office-365)
    
- [MDM 설정 하지만 제거 하려고 합니다. 단계는 무엇입니까?](#i-set-up-mdm-but-now-i-want-to-remove-it-what-are-the-steps)
    
- [추가 지원이 필요](#still-need-help)
    
## <a name="how-can-i-get-mdm-for-office-365-i-dont-see-it-in-the-office-365-admin-center"></a>Office 365에 대 한 MDM를 어떻게 얻을 수 있습니까? Office 365 관리 센터에 표시 되지 않습니다.

이 기능은 Office 365 고객에 게 제공을 완료 했습니다. **장치 관리** 탭에서 찾습니다는 [Office 365 보안으로 이동 &amp; 준수 센터](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8)합니다. 표시 되지 않으면 의견을 보내 주십시오. 참조 [여전히 도움이 필요 하십니까?](#still-need-help), 알아봅니다 시작 하 고 있습니다. 
  
## <a name="how-can-i-get-started-with-device-management-in-mdm"></a>어떻게 수 시작 MDM 장치 관리

Office 365 (세부 정보를 [모바일 장치 관리 (MDM) Office 365의 설정](set-up-mobile-device-management.md)에 대해 알아봅니다.)에 대 한 MDM 시작 하려면 다음 네 단계가 있습니다.
  
1. **MDM.를 활성화 합니다.** 이동 하는 [Office 365 보안으로 이동 &amp; 준수 센터](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) 하 고 **장치 관리**를 선택 합니다. **아래의 단계를 시작** 하는 정품 인증 프로세스를 시작 하기를 클릭 합니다. 
    
2. **MDM에 대 한 구성을 완료**합니다. 이 도메인에 대 한 한 apn을 사용할 인증서 구성 및 DNS 레코드에 대 한 업데이트를 요구 될 수 있습니다. 
    
3. **정책 만들기입니다**. 장치 관리 정책 만들기 및 [보안 그룹에 설정](create-device-security-policies.md)된 사용자 그룹에 적용 합니다. 소규모 테스트 그룹에 정책을 배포 하 여 시작 하는 것이 좋습니다. 보안에서 &amp; 준수 센터, **장치 보안 정책**을 선택 합니다.
    
4. **사용자가 장치를 등록 합니다.** (예: 자신의 전자 메일 클라이언트로 사용) 하 여 Office 365 데이터에 액세스 하려고 할 때 자신에 게 적용 되는 정책이 가진 사용자는 [통해 장치 등록](enroll-your-mobile-device.md) 하 라는 메시지가 표시 됩니다. 
    
## <a name="im-trying-to-set-up-mdm-but-it-seems-stuck-the-office-365-service-health-has-been-showing-provisioning-for-a-while-what-can-i-do"></a>MDM을 설정 하려고 하지만 걸린 것 처럼 보입니다. 잠시 자리를 "준비" Office 365 서비스 상태를 보여주는 되었습니다. 무엇을 도와드릴까요?

준비 하기 위해 서비스 하면 다소 시간이 걸릴 수 있습니다. 프로 비전 완료 되 면 Office 365 페이지에 대 한 모바일 장치 관리 표시 됩니다. 24 시간 기다린 상태는 여전히 **프로 비전**하는 경우를 참조 하십시오 [여전히 도움이 필요 하십니까?](#still-need-help) 하 고 문제를 파악 하는 것이 알아봅니다. 
  
## <a name="what-can-i-do-if-device-enrollment-fails"></a>장치 등록에 실패 하는 경우 어떻게 해야 합니까?

등록 하는 장치를 시작 하는데 문제가 경우는 먼저 다음 확인을 시도 합니다.
  
- 장치 Intune 등의 다른 모바일 장치 관리 공급자와 함께 이미 등록 되지 않은 있는지 확인 하십시오.
    
- 장치 올바른 날짜와 시간으로 설정 되어있는지 확인 합니다.
    
- 다른 Wi-fi 또는 장치에 셀룰러 네트워크로 전환
    
- Android 또는 iOS 장치에 대 한 제거 하 고 장치에 Intune 회사 포털 응용 프로그램을 다시 설치 합니다.
    
등록이 여전히 하는 경우 작동 [추가 문제해결 단계를 시도](troubleshoot-mdm.md)하지 않습니다.
  
## <a name="whats-the-difference-between-intune-and-mdm-for-office-365"></a>Intune 및 Office 365에 대 한 MDM 간의 차이 무엇입니까?

Office 365 및 Intune 두 MDM 조직에서 장치를 관리 하기 위한 클라우드 기반 솔루션을 제공 합니다. Intune 또는 MDM를 사용 하 여 Office 365에 대 한 하기에 가장 적합 한지 결정 하는데 도움이 되는 두 서비스의이 [-나란히 비교](choose-between-mdm-and-intune.md) 를 사용 합니다. 
  
## <a name="how-do-policies-work-for-mdm-how-do-i-set-them-up-disable-them"></a>MDM에 대 한 정책은 어떻게 작동 합니까? 어떻게 수행 설정 하 시겠습니까? 없도록?

Office 365를 하면 [정책을 만들고이 그룹의 사용자에 게 적용](create-device-security-policies.md) 에 대 한 MDM에 대 한 초기 설치를 완료 한 후 [Office 365 보안으로 이동 &amp; 준수 센터](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8)합니다. 정책에 적용 되는 사용자에 대 한 정책은 사용자가 장치를 사용 하 여 Office 365 데이터에 액세스할 수 있는 전에 Office 365에 대 한 MDM에 해당 장치를 등록 필요 합니다. 설정 하는 정책을 얼마나 자주 암호를 다시 설정 해야 예제 또는 데이터 암호화가 필요한 지 여부에 대 한 모바일 장치에 대 한 설정을 결정 합니다. 
  
[만들기 (영문) 및 장치 보안 정책 배포](create-device-security-policies.md)를 위한 단계별 지침을 제공 합니다. 보안에서 정책을 만들 &amp; 준수 센터 하 고 보안을 반환 하 여 하나 이상의 정책을 비활성화할 수 &amp; 적용 된 그룹을 제거 하려면 준수 센터 및 정책을 편집 하 고 있습니다. 또는를 정책을 완전히 제거 하지 않도록 선택할 수 있습니다.
  
사용자의 특정 그룹 정책에 의해 영향을 주지 않도록 제외 하려는 그룹을 제외 그룹에 추가할 수 있습니다. 보안에서 &amp; **장치** 탭에서 준수 센터 **장치 액세스 설정 관리**선택한 다음 그룹을 추가 **액세스 제어에서 제외 하려는 모든 보안 그룹 있습니까?** 섹션입니다. 
  
## <a name="can-i-switch-from-exchange-activesync-device-management-to-mdm-for-office-365"></a>I 전환할 수 Exchange ActiveSync 장치 관리에서 MDM Office 365에 대 한?

이미 [Exchange ActiveSync 정책](https://go.microsoft.com/fwlink/?LinkId=615145) 을 사용 하 여 모바일 장치를 관리 하는, 하는 경우 [를 모바일 장치 관리 (MDM) Office 365에서 설정](set-up-mobile-device-management.md)하는 단계를 수행 하 여 Office 365에 대 한 MDM를 사용 하 여 시작할 수 있습니다.
  
에서 만든 MDM 사용자 그룹으로 Office 365에 대 한 정책을 적용 하면 이러한 정책은 Exchange ActiveSync 모바일 장치 사서함 정책 및 해당 사용자에 대 한 Exchange 관리 센터에서 이전에 만든 장치 액세스 규칙을 무시 합니다. 
  
장치는 Office 365에 대 한 MDM에 등록 되, 후 Exchange ActiveSync 모바일 장치 사서함 정책 또는 장치 액세스 규칙을 모두 장치에 적용 되는 무시 됩니다.
  
## <a name="i-set-up-mdm-but-now-i-want-to-remove-it-what-are-the-steps"></a>MDM 설정 하지만 제거 하려고 합니다. 단계는 무엇입니까?

그러나 없습니다 단순히 "구축을 중단 하" MDM Office 365에 대 한을 설정한 후 합니다. 하지만 사용자 그룹을 위해 만든 장치 정책에서 사용자 보안 그룹을 제거 하 여 제거할 수 있습니다. 또는 원본 위치에 없는 되도록 강제 수행 되지 않고 장치 정책을 제거 하 여 모든 사용자에 대 한 비활성화 합니다. [Office 365의 모바일 장치 관리를 해제 하는 방법을](turn-off-mdm.md)참조 하십시오.
  
## <a name="still-need-help"></a>여전히 도움이 필요 하십니까?

[![Office 365 커뮤니티 포럼에서 도움말 보기](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![관리자: 서비스 요청 로그인 및 만들기](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![관리자: 지원 서비스 문의](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  

  

