---
title: Overview of Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'office 365 Cloud App Security에서는 office 365의 의심 스러운 활동에 대 한 정보를 제공 하므로 문제가 발생할 가능성이 있는 상황을 조사 하 고, 필요한 경우 보안 문제 해결에 대 한 조치를 취할 수 있습니다. '
ms.openlocfilehash: 960e4c75a4da13e1a0365f75d290cd18587abd58
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263082"
---
# <a name="overview-of-office-365-cloud-app-security"></a>Overview of Office 365 Cloud App Security
  
|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|사용자가 여기 있어!  <br/> [다음 단계](get-ready-for-office-365-cas.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |[배포 시작](turn-on-office-365-cas.md) <br/> |[활용 시작](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> office 365 Cloud App Security는 office 365 Enterprise E5에서 사용할 수 있습니다. 조직에서 다른 office 365 Enterprise 구독을 사용 하는 경우 office 365 Cloud App Security를 추가 기능으로 구입할 수 있습니다. (전역 관리자 인 경우 Microsoft 365 관리 센터에서 **청구** \> **구독 추가**를 선택 합니다.) 자세한 내용은 [office 365 플랫폼 서비스 설명: office 365 보안 &amp; 및 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) 및 [비즈니스용 office 365 용 추가 기능 구입 또는 편집](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on)을 참조 하세요. 
  
office 365 Cloud App Security에서는 문제가 발생할 가능성이 있는 상황을 조사 하 고, 필요한 경우 보안 문제 해결에 대 한 조치를 취할 수 있도록 office 365의 의심 스러운 활동에 대해 설명 합니다. office 365 Cloud App Security를 사용 하 여 이례적인 또는 의심 스러운 활동에 대 한 트리거된 알림의 알림을 받을 수 있으며, office 365에서 조직의 데이터를 액세스 하 여 사용 하는 방법, 사용자 계정 일시 중단 활동이 발생 하는 방식 및 요구 사항을 참조 하세요. 경고가 트리거된 후 Office 365 앱에 다시 로그인 하는 사용자입니다. 이 문서를 읽으면 Office 365 Cloud App Security 기능 및 기능에 대 한 개요를 확인할 수 있습니다.
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a>Office 365 Cloud App Security 포털을 찾는 방법

> [!NOTE]
> office 365 Cloud App Security 포털에 액세스 하려면 office 365 전역 관리자, 보안 관리자 또는 보안 판독기 여야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요. 
  
Office 365 Cloud App Security portal로 이동 [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) 하 여 로그인 해 볼 수 있습니다. 

Office 365 보안 &amp; 및 준수 센터에서 찾을 수도 있습니다. 이 작업을 수행 하는 좋은 방법은 다음과 같습니다.
  
1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다. (보안 &amp; 및 준수 센터로 이동 합니다.)
    
2. 보안 &amp; 및 준수 센터에서 **경고** \> **고급 알림 관리**를 선택 합니다. <br/>![Office 365 Cloud App Security로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>(office 365 cloud app security이 아직 사용 하도록 설정 되어 있지 않고 전역 관리자 인 경우 [office 365 Cloud App Security를 켜십시오](turn-on-office-365-cas.md).)
    
3. **Office 365 Cloud App Security로 이동을**선택 합니다. 
    
## <a name="policies"></a>정책도

Office 365 Cloud App Security는 조직에 대해 정의 된 정책에 따라 작동 합니다. Office 365 Cloud App Security를 사용 하는 경우 조직에는 몇 가지 미리 정의 된 변칙 검색 정책과 활동 정책에 대 한 여러 서식 파일이 포함 됩니다. 이러한 정책은 일반적인 예외를 감지 하 고 위험한 ip 주소에서 로그인 하는 사용자를 식별 하며, 랜 섬 웨어 활동을 감지 하 고, 회사 이외의 IP 주소에서 관리자 활동을 검색 하는 등의 작업을 지원 합니다.
  
![CAS 포털에서 정책 템플릿을 보거나 만들 \> 컨트롤 템플릿을 선택 합니다.](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
정책 템플릿을 보거나 사용 하려면 Office 365 Cloud App Security 포털에서 **Control** \> **templates**로 이동 합니다. 
  
![O365 CAS 포털에서 Control을 선택 합니다.](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
정책에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.
  
- [Office 365 Cloud App Security 활동 정책 및 알림](activity-policies-and-alerts.md)
    
- [Office 365 Cloud App Security 변칙 검색 정책](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a>경고

정책이 정의 되 면 감지 된 의심 스러운 활동 또는 이례적인 작업에 대 한 알림을 받습니다. 조직의 알림을 보려면 화면 맨 위에 있는 탐색 모음에서 **경고** 를 선택 합니다. 
  
![알림 페이지에서 트리거된 알림과 수행한 모든 작업을 확인할 수 있습니다.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
알림이 트리거되면 알림을 검토 하 여 진행 중인 작업에 대해 자세히 알아볼 수 있습니다. 그런 다음 활동이 여전히 의심 스 러 되 면 조치를 취할 수 있습니다. 예를 들어 사용자에 게 문제를 알리거나, 사용자가 office 365에 로그인 하지 못하도록 일시 중단 하거나, 사용자가 office 365 앱에 다시 로그인 하도록 요구할 수 있습니다.
  
경고에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.
  
- [Office 365 Cloud App Security 활동 정책 및 알림](activity-policies-and-alerts.md)
    
- [Office 365 Cloud App Security 변칙 검색 정책](anomaly-detection-policies-in-ocas.md)
    
- [Office 365 Cloud App Security alerts에 대 한 검토 및 조치 수행](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a>활동 로그

Office 365 Cloud App Security의 활동 로그 페이지에 있는 사용자 작업에 대 한 정보를 확인 합니다.
  
![O365 CAS 포털에서 작업 로그 조사 \> 를 선택 합니다.](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
이 페이지에 액세스 하려면 Office 365 Cloud App Security 포털에서 **활동 로그** **조사** \> 로 이동 합니다. 
  
![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
Office 365 Cloud App Security와 함께 웹 트래픽 로그를 사용할 수 있습니다. 이러한 로그 파일에 포함 된 자세한 내용은 사용자 작업에 대 한 가시성을 향상 시킵니다. Barracuda, 파랑 코트, 확인 지점, Cisco, Clavister, Dell SonicWALL, Fortinet, 곱 향나무, McAfee, Microsoft, Palo Alto, Sophos, Squid, websence, Zscaler 등의 로그 파일을 사용할 수 있습니다.
  
[Office 365 Cloud App Security에 대 한 웹 트래픽 로그 및 데이터 원본에 대해 자세히 알아보기](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="oauth-apps"></a>OAuth 앱

office 365 Cloud App Security를 사용 하 여 조직의 사용자가 office 365의 데이터에 액세스 하는 타사 앱을 사용 하도록 허용 하거나 금지할 수 있습니다.
  
![O365 CAS에서는 조사 메뉴에서 OAuth 앱 관리 페이지에 액세스할 수 있습니다.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
이 페이지에 액세스 하려면 **OAuth 앱** **조사** \> 로 이동 합니다. 
  
![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[Office 365 Cloud App Security를 사용하여 OAuth 앱 관리](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a>클라우드 검색 대시보드

**생산성 앱 검색이**라고도 하는 **클라우드 검색 대시보드**는 조직 내 클라우드 앱 사용에 대 한 정보를 표시 합니다. 이 대시보드를 사용 하 여 앱, 사용자, 트래픽, 트랜잭션 등에 대 한 정보를 볼 수 있습니다. 클라우드 검색 대시보드는 다음과 같은 이미지와 비슷합니다. 
  
![Office 365 CAS 포털에서 클라우드 검색 대시보드 검색 \> 을 선택 합니다.](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
이 대시보드에 액세스 하려면 Office 365 cloud App Security 포털에서 **** \> **클라우드 검색 대시보드로**이동 합니다. 
  
![Office 365 CAS 포털에서 검색을 선택 합니다.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a>다음 단계

- [Office 365 Cloud App Security 사용 사례 및 사용 가이드](https://aka.ms/O365CASGuide) 받기
    
- [Office 365 Cloud App Security 시작](get-ready-for-office-365-cas.md)
    

