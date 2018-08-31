---
title: Office 365 Cloud App Security에 대한 웹 트래픽 로그 및 데이터 원본
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: Office 365 클라우드 앱 보안 웹 트래픽 로그 다양 한 범위의 공급자에서 작동합니다. 웹 트래픽 로그에 대 한 자세한 내용은이 문서를 읽고 Office 365 클라우드 응용 프로그램 보안에 대 한 데이터 원본을 지원 합니다.
ms.openlocfilehash: 09b0358e0d8b9a6ed59393d8771237f7eaf8bb98
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533593"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Office 365 Cloud App Security에 대한 웹 트래픽 로그 및 데이터 원본
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |[배포를 시작 합니다.](turn-on-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](#next-steps) <br/> |
  
Office 365 클라우드 앱 보안이 포함 된 다양 한 범위의 웹 트래픽 로그 파일 및 데이터 원본에 사용할 수 있습니다. 그러나 웹 트래픽 로그 파일 특정 정보를 포함 해야 하 고 Office 365 클라우드 응용 프로그램 보안 app 검색 보고서 및 클라우드 검색 대시보드 함께 작동할 수 있도록 특정 한 방법으로 포맷 합니다. 웹 트래픽 로그 및 Office 365 클라우드 응용 프로그램 보안 사용할 데이터 원본에 대 한 참조 가이드로이 문서를 사용 합니다.
  
> [!NOTE]
> 보안에 액세스 하려면 전역 관리자, 보안 관리자 또는 보안 판독기 이어야 &amp; 준수 센터 및 Office 365 클라우드 응용 프로그램 보안 포털 합니다. 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. 
  
## <a name="web-traffic-log-requirements"></a>웹 트래픽 로그 요구 사항

조직에서 사용자는 앱을 쉽게 이해할 수 있도록 웹 트래픽 로그에서 office 365 클라우드 응용 프로그램 보안 사용 하 여 데이터를 사용 하는 합니다. 사용자 작업을 더 나은 가시성 해야 로그 파일에 포함 된 더 많은 세부 정보입니다.
  
다음 표에서 요구 사항 및 Office 365 클라우드 응용 프로그램 보안에서는 제대로 작동 하 여 웹 트래픽 로그에 대 한 필요한 특성을 나열 합니다.
  
|**특성**|**추가 요구 사항 **|
|:-----|:-----|
| 트랜잭션의 날짜  <br/>  원본 IP  <br/>  원본 사용자 (권장)  <br/>  대상 IP 주소  <br/>  대상 URL (권장: IP 주소 보다 클라우드 앱 검색에 대 한 높은 정확도 제공 하는 Url)  <br/>  (권장) 하는 데이터의 총 크기  <br/>  양의 업로드 또는 데이터를 다운로드 (권장: 앱 사용 패턴 클라우드 하는 방법에 대 한 정보를 제공 합니다.)  <br/>  (허용 또는 차단 된)에 수행할 작업  <br/> | 로그 파일에 대 한 데이터 원본을 지원 되어야 합니다.  <br/>  로그 파일을 사용 하는 형식에는 표준 형식을 일치 해야 합니다. 파일을 업로드 하는 경우 응용 프로그램 검색이를 확인 합니다.  <br/>  로그에 이벤트 해야 라인으로 전환한 전체 개 이하의 90 일이 경과 하지 않았습니다.  <br/>  로그 파일에 대 한 네트워크 활동 분석할 수 있는 아웃 바운드 트래픽을 정보를 포함 해야 합니다.  <br/> |
   
특성 로드 되는 로그에 포함 되지 않으면 Office 365 클라우드 응용 프로그램 보안을 표시 하거나 수에 대 한 정보를 분석할 수는 없습니다. 예, Cisco ASA 방화벽 표준 로그 형식 트랜잭션, 사용자 이름, 또는 대상 URL (만 대상 IP) 당 업로드 된 바이트의 크기를 포함 되지 않습니다. Cisco 로그 파일에 해당 정보가 아니므로 Office 365 클라우드 응용 프로그램 보안 되지 않음 것 때 포함 조직의 네트워크 트래픽을 분석 합니다.
  
> [!NOTE]
> 일부 유형의 방화벽에 대 한 필수 특성을 포함 하도록 웹 트래픽 로그에 대 한 정보 수준을 설정 해야 합니다. 등 Cisco ASA 방화벽 정보 수준을 6으로 설정 되어 있어야 합니다. 방화벽 웹 트래픽 로그에 올바른 정보를 제공 하도록 설정 되었는지 확인 하려면 있는지 확인 합니다. 
  
## <a name="data-attributes-for-different-vendors"></a>서로 다른 공급 업체에 대 한 데이터 특성
<a name="BKMK_LogAndData"> </a>

다음 표에서 다양 한 공급 업체 로부터 웹 트래픽 로그의 정보를 요약 합니다. **공급 업체에 대 한 최신 정보를 확인 해야 합니다.**
  
|**데이터 원본**|**대상 응용 프로그램 URL**|**대상 응용 프로그램 IP**|**Username**|**원본 IP**|**총 트래픽**|**업로드 된 바이트**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Barracuda  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |아니요  <br/> |
|파란색 코트  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|검사점  <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |아니요  <br/> |
|Cisco ASA  <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |
|Cisco FWSM  <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |
|Cisco Ironport WSA  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Cisco Meraki  <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |아니요  <br/> |
|Clavister NGFW (Syslog)  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Dell SonicWall  <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Fortigate  <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Juniper SRX  <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Juniper SSG  <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|McAfee SWG  <br/> |**예** <br/> |아니요  <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Meraki (Cisco)  <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |아니요  <br/> |아니요  <br/> |
|Microsoft Threat Management Gateway  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|팔로 알토 네트워크  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Sophos  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |
|들면 squid (공통)  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |
|들면 squid (기본)  <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |**예** <br/> |아니요  <br/> |**예** <br/> |
|Websense-조사 세부 정보 보고서 (CSV)  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Websense-인터넷 활동 로그 (CEF)  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
|Zscaler  <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |**예** <br/> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>지원 되는 공급 업체 방화벽 및 프록시
<a name="BKMK_Supported"> </a>

Office 365 클라우드 앱 보안 다음 방화벽 및 프록시를 지원합니다.
  
- Barracuda-웹 응용 프로그램 방화벽 (W3C)
    
- 파랑 코트 프록시 SG-액세스 로그 (W3C)
    
- 검사점
    
- Cisco ASA 방화벽 (6 정보 수준을 설정 해야 하면 메모)
    
- Cisco IronPort WSA
    
- Cisco ScanSafe
    
- Cisco Merkai-Url 로그
    
- Dell Sonicwall
    
- Fortinet Fortigate
    
- Juniper SRX
    
- Juniper SSG
    
- McAfee 보안 웹 게이트웨이
    
- Microsoft Forefront Threat Management Gateway (W3C)
    
- 팔로 알토 시리즈 방화벽
    
- Sophos SG
    
- Sophos Cyberoam
    
- 들면 squid (공통)
    
- 들면 squid (기본)
    
- Websense-웹 보안 솔루션-조사 세부 정보 보고서 (CSV)
    
- Websense-웹 보안 솔루션-인터넷 활동 로그 (CEF)
    
- Zscaler
    
> [!NOTE]
> 사용 하 여 원하는 데이터 원본을 포함 하지 않으면 여기 하는 경우 검색 응용 프로그램에 추가할 수 있는지를 요청할 수 있습니다. 이렇게 하려면, 보고서를 만드는 경우 선택 **다른** **데이터 원본**에 대 한 합니다. 업로드 하려는 데이터 원본의 이름을 입력 합니다. 로그를 검토 하 고 사용 하는 로그 종류에 대 한 지원을 추가 하는 경우를 알 수 수는 합니다. 
  
## <a name="troubleshoot-errors-when-log-files-are-uploaded"></a>로그 파일이 업로드 되 면 오류 해결

웹 트래픽 로그 파일을 업로드 한 후에 오류가 없었는지 확인 하려면 거 버 넌 스 로그를 확인 합니다. 오류가 있는 경우는 이러한 오류를 해결 하려면 다음 표의 정보를 사용 합니다.
  
|**오류**|**설명**|**문제 해결 방법**|
|:-----|:-----|:-----|
|지원 되지않는 파일 형식  <br/> |업로드 된 파일 유효한 로그 파일이 아닙니다. 예: 이미지 파일입니다.  <br/> |텍스트, zip, 또는 방화벽 또는 프록시에서 직접 내보낸 gzip 파일을 업로드 합니다.  <br/> |
|내부 오류  <br/> |내부 리소스 오류가 발견 되었습니다.  <br/> |다시 실행 하는 작업을 **다시 시도** 클릭 합니다.  <br/> |
|로그 형식이 일치 하지 않습니다.  <br/> |업로드 한 로그 형식에이 데이터 원본에 대 한 예상된 로그 형식을 일치 하지 않습니다.  <br/> |
로그가 손상 되지 않았는지 확인 합니다. 비교 하 고 업로드 페이지에 표시 된 예제 형식으로 로그 파일 형식과 일치 합니다. |
|트랜잭션은 90 일이 지난  <br/> |모든 트랜잭션 90 일이 지난 되며 무시 되 고 됩니다.  <br/> |최근 이벤트와 함께 새 로그를 내보내고 업로드 하십시오.  <br/> |
|클라우드 앱 카탈로그에 없음 트랜잭션  <br/> |모든 인식 된 클라우드 앱에 없는 트랜잭션 로그에서 발견 되 합니다.  <br/> |로그 아웃 바운드 트래픽을 정보에 들어 있는지 확인 합니다.  <br/> |
|지원 되지않는 로그 종류  <br/> |선택 하면 **데이터 원본 다른 (지원 하지 않는) =**, 로그를 구문 분석 하지. [Microsoft 클라우드 응용 프로그램 보안](https://aka.ms/whatiscas) 기술 팀에 게 검토를 위해 전송 됩니다.<br/> |[Microsoft 클라우드 응용 프로그램 보안](https://aka.ms/whatiscas) 기술 팀의 각 데이터 원본에 대 한 전용된 파서를 만듭니다. 가장 인기 있는 데이터 원본은 이미 지원 합니다. 지원 되지않는 데이터 원본 업로드할 때 검토 이며 잠재적인 새 데이터 원본 파서의 목록에 추가 합니다.<br/> 새 파서 기능에 추가 되 면 알림은 Microsoft 클라우드 응용 프로그램 보안 릴리스 정보에 포함 됩니다.  <br/> |
   
## <a name="next-steps"></a>다음 단계

- [검토 및 알림 작업을 수행 합니다.](review-office-365-cas-alerts.md)
    
- [응용 프로그램 검색 보고서 만들기](create-app-discovery-reports-in-ocas.md)
    
- [응용 프로그램 검색 결과 검토 합니다.](review-app-discovery-findings-in-ocas.md)
    
- [Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동을 검토 합니다.](utilization-activities-for-ocas.md)
    

