---
title: Office 365 Cloud App Security에 대한 웹 트래픽 로그 및 데이터 원본
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 290b02bf-a988-4fb9-88b2-34e408216ac8
description: Office 365 Cloud App Security는 광범위 한 공급자의 웹 트래픽 로그에서 작동 합니다. 이 문서를 읽으면 Office 365 Cloud App Security에 대 한 웹 트래픽 로그 및 지원 되는 데이터 원본에 대해 자세히 알아볼 수 있습니다.
ms.openlocfilehash: 67246ded0e3d39c81b5b906f753b91298309d1d8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32266853"
---
# <a name="web-traffic-logs-and-data-sources-for-office-365-cloud-app-security"></a>Office 365 Cloud App Security에 대한 웹 트래픽 로그 및 데이터 원본
  
|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |[배포 시작](turn-on-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](#next-steps) <br/> |
  
Office 365 Cloud App Security를 사용 하 여 광범위 한 웹 트래픽 로그 파일 및 데이터 원본을 사용할 수 있습니다. 그러나 웹 트래픽 로그 파일에는 특정 정보가 포함 되어야 하며, Office 365 cloud app 보안 앱 검색 보고서 및 클라우드 검색 대시보드와 함께 작동 하도록 특정 방식으로 서식을 지정 해야 합니다. 이 문서를 Office 365 Cloud App Security와 함께 사용할 웹 트래픽 로그 및 데이터 원본에 대 한 참조 가이드로 사용 하십시오.
  
> [!NOTE]
> 보안 &amp; 및 준수 센터 및 Office 365 Cloud App security 포털에 액세스 하려면 전역 관리자, 보안 관리자 또는 보안 독자 여야 합니다. [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요. 
  
## <a name="web-traffic-log-requirements"></a>웹 트래픽 로그 요구 사항

Office 365 Cloud App Security는 웹 트래픽 로그의 데이터를 사용 하 여 조직의 사용자가 사용 하는 앱을 파악할 수 있도록 합니다. 로그 파일에 포함 된 자세한 내용은 사용자 작업에 대 한 가시성을 향상 시킵니다.
  
다음 섹션에서는 Office 365 Cloud App Security에서 웹 트래픽 로그가 올바르게 작동 하기 위해 필요한 특성 및 추가 요구 사항에 대해 설명 합니다.

### <a name="attributes"></a>특성만

Office 365 Cloud App Security에서는 웹 트래픽 로그에 포함 되지 않은 특성을 표시 하거나 분석할 수 없습니다. 예를 들어 Cisco global.asa 방화벽의 표준 로그 형식에는 트랜잭션 당 업로드 된 바이트 수, 사용자 이름 또는 대상 URL (대상 IP만)이 포함 되어 있지 않습니다. 따라서 이러한 특성은 클라우드 검색 데이터에 표시 되지 않으며 클라우드 앱에 대 한 표시는 제한 됩니다. Cisco global.asa 방화벽의 경우 정보 수준을 6으로 설정 해야 합니다. 

웹 트래픽 로그에는 다음과 같은 특성이 포함 되어야 합니다.

- 트랜잭션 날짜
- 원본 IP
- 원본 사용자 (권장)
- 대상 IP 주소
- 대상 URL (권장; url은 IP 주소 보다 클라우드 앱 검색에 더 높은 정확도를 제공 합니다.
- 총 데이터 양 (권장, 데이터 정보가 매우 귀중 함)
- 업로드 또는 다운로드 한 데이터의 양 (권장; 클라우드 앱 사용 패턴에 대 한 정보 제공)
- 수행 된 작업 (허용 또는 차단 됨)

### <a name="additional-requirements"></a>추가 요구 사항 

이 문서 앞부분에 나와 있는 특성을 포함 하는 것 외에도 웹 트래픽 로그가 다음 요구 사항을 충족 해야 합니다.

- 로그 파일에 대 한 데이터 원본을 지원 해야 합니다.
- 로그 파일에서 사용 하는 형식은 표준 형식과 일치 해야 합니다. 파일이 업로드 되 면 앱 검색에서이를 확인 합니다.
- 로그의 이벤트가 90 일 이내에 수행 되어야 합니다.
- 로그 파일에는 네트워크 활동을 위해 분석할 수 있는 아웃 바운드 트래픽 정보가 포함 되어야 합니다.
  
## <a name="data-attributes-for-different-vendors"></a>각 공급 업체에 대 한 데이터 특성

다음 표에서는 다양 한 공급 업체의 웹 트래픽 로그에 있는 정보를 요약 하 여 보여 줍니다. **공급 업체에 문의 하 여 최신 정보를 확인 해야 합니다.**


|                 데이터 원본                  |    대상 앱 URL    |    대상 응용 프로그램 IP     |       사용자 이름       |      원본 IP       |    총 트래픽     |    업로드 된 바이트    |
|----------------------------------------------|----------------------|----------------------|----------------------|----------------------|----------------------|----------------------|
|                  Barracuda                   | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |          아니요          |          아니요          |
|                  푸른 코트                   | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                  포인트                  |          아니요          | <strong>예</strong> |          아니요          | <strong>예</strong> |          아니요          |          아니요          |
|              Cisco global.asa (Syslog)              |          아니요          | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> |          아니요          |
|           Cisco global.asa (FirePOWER 포함)           | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                  Cisco FWSM                  |          아니요          | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> |          아니요          |
|              Cisco ironpor WSA              | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                 Cisco Meraki                 | <strong>예</strong> | <strong>예</strong> |          아니요          | <strong>예</strong> |          아니요          |          아니요          |
|           Clavister NGFW (Syslog)            | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                SonicWall (이전 Dell)                | <strong>예</strong> | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|            디지털 미술 i 필터             | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                  fortigate                   |          아니요          | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                 곱 향나무 srx                  |          아니요          | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                 곱 향나무 ssg                  |          아니요          | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                  McAfee swg                  | <strong>예</strong> |          아니요          |          아니요          | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                    MS TMG                    | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|              Palo Alto 네트워크              |          아니요          | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                    Sophos                    | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |          아니요          |
|                Squid (Common)                | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> |          아니요          | <strong>예</strong> |
|                Squid (네이티브)                | <strong>예</strong> |          아니요          | <strong>예</strong> | <strong>예</strong> |          아니요          | <strong>예</strong> |
| websense-CSV (조사 detail report) | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|    websense-cef (인터넷 활동 로그)    | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
|                   Zscaler                    | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> | <strong>예</strong> |
   
## <a name="supported-vendor-firewalls-and-proxies"></a>지원 되는 공급 업체 방화벽 및 프록시

Office 365 Cloud App Security에서는 다음과 같은 방화벽과 프록시를 지원 합니다.
  
- Barracuda-W3C (웹 앱 방화벽)  
- 푸른 코트 프록시 SG-Access log (W3C)
- 확인 점
- Cisco global.asa 방화벽 (정보 수준을 6으로 설정 했는지 확인)
- Cisco global.asa (FirePOWER 포함)   
- Cisco ironpor WSA
- Cisco scansafe
- Cisco Merkai-url 로그
- Clavister NGFW (Syslog)
- 디지털 미술 i 필터
- Fortinet fortigate
- iboss 보안 클라우드 게이트웨이
- 곱 향나무 srx
- 곱 향나무 ssg
- McAfee 보안 웹 게이트웨이
- Microsoft Forefront (위협 관리 게이트웨이)
- Palo Alto 시리즈 방화벽
- Sonicwall (이전 Dell)   
- Sophos SG
- Sophos xg
- Sophos Cyberoam
- Squid (Common)
- Squid (네이티브)
- websense-웹 보안 솔루션-CSV (조사 detail report)
- websense-웹 보안 솔루션-cef (인터넷 활동 로그)
- Zscaler
    
> [!NOTE]
> 사용 하려는 데이터 원본이 여기에 포함 되어 있지 않은 경우 앱 검색에 추가 되도록 요청할 수 있습니다. 이렇게 하려면 보고서를 만들 때 **데이터 원본**에 대해 **기타** 를 선택 합니다. 그런 다음 업로드 하려는 데이터 원본의 이름을 입력 합니다. 로그를 검토 하 고 해당 로그 유형에 대 한 지원을 추가할 것인지를 알려 드리겠습니다. 또는 형식과 일치 하는 [사용자 지정 파서를 정의할](https://docs.microsoft.com/cloud-app-security/custom-log-parser) 수 있습니다. 
  
## <a name="troubleshoot-errors-when-log-files-are-uploaded"></a>로그 파일을 업로드할 때 오류 해결

웹 트래픽 로그 파일을 업로드 한 후에는 거 버 넌 스 로그를 검사 하 여 오류가 있는지 확인 합니다. 오류가 있는 경우 다음 표의 정보를 사용 하 여 이러한 오류를 해결 합니다.
  
|**오류**|**설명**|**해결 방법**|
|:-----|:-----|:-----|
|지원 되지 않는 파일 형식  <br/> |업로드 한 파일이 유효한 로그 파일이 아닙니다. 예를 들면 이미지 파일입니다.  <br/> |방화벽 또는 프록시에서 직접 내보낸 텍스트, zip 또는 gzip 파일을 업로드 합니다.  <br/> |
|내부 오류  <br/> |내부 리소스 오류가 검색 되었습니다.  <br/> |**다시 시도** 를 클릭 하 여 작업을 다시 실행 합니다.  <br/> |
|로그 형식이 일치 하지 않습니다.  <br/> |업로드 한 로그 형식이이 데이터 원본에 대 한 예상 로그 형식과 일치 하지 않습니다.  <br/> |
로그가 손상 되지 않았는지 확인 합니다. 로그 파일 형식을 업로드 페이지에 표시 된 예제 형식으로 비교 하 여 일치 시킵니다. |
|트랜잭션이 90 일 보다 오래 되었습니다.  <br/> |모든 트랜잭션이 90 일 보다 오래 되었으며, 따라서 무시 됩니다.  <br/> |최근 이벤트로 새 로그를 내보내고 다시 업로드 합니다.  <br/> |
|카탈로그에 대 한 트랜잭션 없음 클라우드 앱  <br/> |인식 된 클라우드 앱에 대 한 어떠한 트랜잭션도 로그에서 찾을 수 없습니다.  <br/> |로그에 아웃 바운드 트래픽 정보가 포함 되어 있는지 확인 합니다.  <br/> |
|지원 되지 않는 로그 유형  <br/> |**데이터 원본 = 기타 (지원 되지 않음)** 를 선택 하면 로그가 구문 분석 되지 않습니다. 대신 [Microsoft Cloud App Security](https://aka.ms/whatiscas) 기술 팀에 게 검토를 위해 전송 됩니다.  <br/> |[Microsoft Cloud App Security](https://aka.ms/whatiscas) 기술 팀은 각 데이터 원본에 대 한 전용 파서를 작성 합니다. 가장 인기 있는 데이터 원본은 이미 지원 됩니다. 지원 되지 않는 데이터 원본이 업로드 되 면 검토 되 고 잠재적인 새 데이터 원본 파서 목록에 추가 됩니다.  <br/> 새 파서가 기능에 추가 되 면 Microsoft Cloud App Security release notes에 알림이 포함 됩니다.  <br/> |
   
## <a name="next-steps"></a>다음 단계

- [경고 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
- [앱 검색 보고서 만들기](create-app-discovery-reports-in-ocas.md)
    
- [앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
    
- [Office 365 Cloud App Security에 대 한 사용률 작업 검토](utilization-activities-for-ocas.md)
    

