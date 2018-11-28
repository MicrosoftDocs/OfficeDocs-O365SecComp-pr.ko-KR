---
title: Office 365 Cloud App Security 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'Office 365 클라우드 응용 프로그램 보안을 사용 하면 의심 스러운 활동 대 한 통찰력의 Office 365는 잠재적인 문제를 가진 하 고 필요한 경우 보안 문제를 해결 하는 작업을 수행 하는 상황을 조사할 수 있도록 합니다. '
ms.openlocfilehash: b146512c22cbe86ce3aef95c5916de6959341578
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706402"
---
# <a name="overview-of-office-365-cloud-app-security"></a>Office 365 Cloud App Security 개요
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|여기는!  <br/> [다음 단계](get-ready-for-office-365-cas.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |[배포를 시작 합니다.](turn-on-office-365-cas.md) <br/> |[활용 하 여 시작](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> Office 365 클라우드 App 보안은 Office 365 Enterprise e 5에 사용할 수 있습니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 Office 365 클라우드 앱 보안 추가 기능으로 구입할 수 있습니다. (전역 관리자는 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다. 
  
Office 365 클라우드 앱 보안 제공 의심 스러운 활동에 대 한 통찰력 Office 365에는 잠재적인 문제를 가진 하 고 필요한 경우 보안 문제를 해결 하는 작업을 수행 하는 상황을 조사할 수 있도록 합니다. Office 365 클라우드 응용 프로그램 보안을 함께 트리거된 알림 예외적인 또는 의심 스러운 활동에 대 한 알림을 받을, 어떻게 Office 365에서 조직의 데이터를 액세스 하 고 사용 하 고, 사용자 계정을 현상이 의심 스러운 작업을 일시 중단 하 고 필요 수 있습니다. 사용자가 로그인 할 알림을 트리거한 된 후에 Office 365 응용 프로그램을 백업 합니다. Office 365 클라우드 응용 프로그램 보안 기능을 대략적를이 문서를 읽어보십시오.
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a>Office 365 클라우드 응용 프로그램 보안 포털을 찾는 방법

> [!NOTE]
> Office 365 클라우드 응용 프로그램 보안 포털에 액세스 하려면 전역 관리자, 보안 관리자 또는 보안 판독기 이어야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. 
  
Office 365 보안을 통해 Office 365 클라우드 응용 프로그램 보안 포털을 얻을 수 &amp; 준수 센터입니다. 작업을 수행 하는 한 가지 좋은 방법은 다음과 같습니다.
  
1. 이동 [https://security.microsoft.com](https://security.microsoft.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. (이렇게 하면 보안 &amp; 준수 센터.) 
    
2. 보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다. <br/>![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>(하는 경우 Office 365 클라우드 앱 보안 아직 활성화 되지 않으면 및 [Office 365 클라우드 응용 프로그램 보안 설정](turn-on-office-365-cas.md)전역 관리자 여야 합니다.)
    
3. **Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다. 
    
## <a name="policies"></a>Policies(정책)

Office 365 조직에 대해 정의 된 정책에 작동 하는 클라우드 응용 프로그램 보안 Office 365 클라우드 앱 보안이 포함 된 조직 10 개의 미리 정의 된 예외 탐지 정책 및 활동 정책에 대 한 여러 서식 파일을 가져옵니다. 이러한 정책은 일반 예외 사항을 검색, 위험한 IP 주소에서 로그인 하는 사용자를 식별, ransomware 활동 감지 감지 하 고, 회사 비 IP 주소 등에서 관리자 작업 하도록 디자인 되었습니다.
  
![CAS 포털에서 컨트롤 선택 \> 서식 파일을 보거나 정책 서식 파일을 만들려면](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
Office 365 클라우드 응용 프로그램 보안 포털에서 정책 서식 파일을 보기/사용을 **제어** 이동 \> **서식 파일**입니다. 
  
![O365 CAS 포털에서 컨트롤 선택](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
정책에 대 한 자세한 내용은 다음 리소스를 참조 합니다.
  
- [Office 365 Cloud App Security 활동 정책 및 알림](activity-policies-and-alerts.md)
    
- [Office 365 Cloud App Security 변칙 검색 정책](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a>알림

정책 정의 된 경우에 검색 된 의심 스러운 또는 예외적인 활동에 대 한 알려줄 알림 나타납니다. 조직에 대 한 경고를 보려면 화면 위쪽 탐색 모음에서 **알림** 을 선택 합니다. 
  
![경고 페이지에서 경고를 트리거한 된 및 수행 하는 모든 작업을 볼 수 있습니다.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
경고가 트리거되는 대로 들어갈 기능에 대 한 자세한 내용을 보려면 해당를 검토할 수 있습니다. 그런 다음 활동 여전히 의심 스러운 있으면 작업을 회수할 수 있습니다. 예는 문제에 대 한 사용자에 게 알릴 수 있습니다에서 Office 365에 로그인 한 사용자를 일시 중단 또는 사용자가 Office 365 응용 프로그램을 다시 로그인 해야 합니다.
  
경고 하는 방법에 대 한 자세한 내용은 다음 리소스를 참조 합니다.
  
- [Office 365 Cloud App Security 활동 정책 및 알림](activity-policies-and-alerts.md)
    
- [Office 365 Cloud App Security 변칙 검색 정책](anomaly-detection-policies-in-ocas.md)
    
- [검토 하 고 Office 365 클라우드 응용 프로그램 보안 경고에서 작업 수행](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a>활동 로그

Office 365 클라우드 응용 프로그램 보안의 활동 로그 페이지에서 사용자 작업에 대 한 정보 보기
  
![O365 CAS 포털에서 조사 선택 \> 활동 로그](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
Office 365 클라우드 응용 프로그램 보안 포털에서이 페이지로 이동 하려면 **조사** 로 이동 \> **활동 로그**합니다. 
  
![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
Office 365 클라우드 응용 프로그램 보안 너무 웹 트래픽 로그를 사용할 수 있습니다. 이러한에 포함 된 자세한 내용은 로그 파일, 사용자 작업을가 더 나은 표시 합니다. Barracuda, 파란색 코트, 검사점, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, 팔로 알토, Sophos, 들면 Squid, Websence, Zscaler, 등의 로그 파일을 사용할 수 있습니다.
  
[Office 365 클라우드 응용 프로그램 보안에 대 한 웹 트래픽 로그 및 데이터 원본에 대 한 설명](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="app-permissions"></a>응용 프로그램 사용 권한

Office 365 클라우드 응용 프로그램 보안을 허용 하거나 Office 365의 데이터에 액세스 하는 타사 응용 프로그램을 사용 하 여 조직에서 사람들이 것을 방지 수 있습니다.
  
![O365 CAS 조사 메뉴에서 앱 사용 권한 관리 페이지를 액세스할 수 있습니다.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
이 페이지를 보려면, **조사** 로 이동 \> **App 사용 권한**입니다. 
  
![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[Office 365 Cloud App Security을 사용하여 앱 사용 권한 관리](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a>클라우드 검색 대시보드

조직 내에서 클라우드 앱 사용 현황에 대 한 정보를 표시 하는 **클라우드 검색 대시보드**를 **생산성 응용 프로그램 검색**라고도 합니다. 앱, 사용자, 트래픽, 거래 등이 대시보드를 사용 하는 방법에 대 한 정보를 볼 수 있습니다. 클라우드 검색 대시보드는 다음 이미지와 유사합니다. 
  
![Office 365 CAS 포털에서 검색을 선택 \> 클라우드 검색 대시보드](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
Office 365 클라우드 응용 프로그램 보안 포털에서이 대시보드를 **검색** 하려면 이동 \> **클라우드 검색 대시보드**합니다. 
  
![Office 365 CAS 포털에서 검색을 선택](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a>다음 단계

- [Office 365 클라우드 응용 프로그램 보안 사용 사례 및 사용 가이드](https://aka.ms/O365CASGuide)
    
- [Office 365 Cloud App Security 시작하기](get-ready-for-office-365-cas.md)
    

