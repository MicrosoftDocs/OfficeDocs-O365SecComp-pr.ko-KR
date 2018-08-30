---
title: IOS 장치에 대 한 한 apn을 사용할 인증서를 만들려면
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Office 365에 대 한 모바일 장치 관리에는 Iphone 및 iPad와 같은 iOS 장치를 관리 하려면 먼저 한 apn을 사용할 인증서를 만들려면 다음이 단계를 수행 합니다.
ms.openlocfilehash: 28e8888d7dd57c3052cdcb5994725f11a5f0445f
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272053"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>IOS 장치에 대 한 한 apn을 사용할 인증서를 만들려면

 Office 365에 대 한 모바일 장치 관리에는 Iphone 및 iPad와 같은 iOS 장치를 관리 하려면 한 apn을 사용할 인증서를 만들어야 합니다. 
  
이 작업을 수행 하려면 포털 페이지에서 **설정** 링크에서 단계를 수행 합니다. (이동 **보안 &amp; 준수 센터** \> **보안 정책** \> **장치 관리** \> **관리 설정**합니다.)
  
![권장 되는 단계 및 필요한 모바일 장치 관리 설정](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. **IOS 장치에 대 한 한 apn을 사용할 인증서 구성**옆에 있는 **설정**을 선택 합니다.
    
2. **CSR 파일 다운로드** 를 선택 하 고 인증서 서명 요청을 곳에 저장 기억할 수 있는 컴퓨터에 있습니다. 
    
    ![APN 인증서 대화 상자를 설치 합니다.](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. **다음**을 선택 합니다.
    
4. APN 인증서를 만듭니다.
    
  - **Apple 한 apn을 사용할 포털** Apple 푸시 인증서 포털을 선택 합니다. 
    
    ![Apple 한 apn을 사용할 포털을 선택 된 APN 알림 인증서 대화 상자를 설치 합니다.](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Apple ID를 사용 하 여 로그인
    
    > [!IMPORTANT]
    > Apple ID 관리 하는 계정 사용자를 떠날 하는 경우에 사용자의 조직과 상태로 유지 되는 전자 메일 계정과 연결 된 회사를 사용 합니다. 인증서를 갱신 하는 경우 동일한 ID를 사용 하 여 수행 해야 하기 때문에이 ID를 저장 합니다. 
  
  - **인증서 만들기** 를 선택 하 고 **사용 약관에**동의 합니다.
    
  - Office 365 및 **업로드**선택에서 사용자 컴퓨터로 다운로드 한 인증서 서명 요청 **이동** 합니다.
    
  - APN 인증서는 Apple 푸시 인증서 포털에서 사용자의 컴퓨터에 만든 **다운로드** 합니다. 
    
    > [!TIP]
    > 인증서를 다운로드 하는데 문제가 경우 브라우저를 새로 고쳐 합니다. 
  
5. Office 365로 다시 이동 하 고 **다음** **한 apn을 업로드 하는 사용할 인증서** 페이지를 선택 합니다. 
    
6. Apple 푸시 인증서 포털에서 다운로드 한 APN 인증서로 이동 합니다.
    
    ![Apple에서 다운로드 한 apn을 사용할 인증서를 선택 하려면 찾아보기 단추를 클릭 합니다.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. **완료 날짜**를 선택 합니다.
    
으로 돌아가 **보안 &amp; 준수 센터** \> **보안 정책** \> **장치 관리** \> **설정 관리** 설치를 완료 합니다. 
  

