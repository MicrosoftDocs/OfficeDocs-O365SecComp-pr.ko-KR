---
title: Office 365의 자동화 된 조사 및 응답 (AIR)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Office 365 Advanced Threat Protection의 자동화 된 조사 및 응답 기능에 대해 알아봅니다.
ms.openlocfilehash: c6cfc03588e580382f673b2e9be8543bfcaf9ac1
ms.sourcegitcommit: f6073deec39a18581ed12abef18728417a52cdf4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/22/2019
ms.locfileid: "30747564"
---
# <a name="automated-investigation-and-response-air-with-office-365"></a>Office 365의 자동화 된 조사 및 응답 (AIR)

자동화 된 조사 및 응답 (AIR) ( [Office 365 위협 조사 및 응답 기능](office-365-ti.md)에 예정 됨)-오늘 발생 하는 잘 알려진 위협에 대해 자동 조사 및 업데이트를 실행할 수 있습니다. 이 문서를 읽으면 AIR의 개요를 확인 하 고 조직 및 보안 운영 팀이 위협을 보다 효율적이 고 효율적으로 완화 하는 데 도움을 주는 방법을 확인할 수 있습니다. AIR의 추가 기능을 사용할 수 있는 경우에 대 한 자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap)를 참조 하십시오.

## <a name="alerts"></a>경고

[경고](alert-policies.md#viewing-alerts) 는 보안 운영 팀 워크플로에서 문제를 대응 하기 위한 트리거를 나타냅니다. 조사에 대 한 적절 한 알림 집합의 우선 순위를 지정 하 여 위협에 대 한 위협이 발생 하지 않도록 합니다. 경고에 대 한 조사가 수동으로 수행 되 면 보안 운영 팀이 엔터티 (예: 콘텐츠, 장치 및 사용자)를 위협 으로부터 찾아서 상호 연결 해야 합니다. 이러한 작업과 워크플로는 시간을 많이 소비 하며 여러 도구와 시스템을 포함 합니다. AIR을 사용 하는 경우 조사 및 응답은 보안 대응 playbook 자동으로 트리거하는 주요 보안 및 위협 관리 경고로 자동화 됩니다. 

2019 년 4 월 초기 릴리스에서는 다음 단일 이벤트에서 생성 된 경고가 자동으로 조사 됩니다. 

1. 잠재적으로 악의적인 URL 클릭이 검색 되었습니다.
2. 사용자가 피싱으로 보고 한 전자 메일
3. 배달 후 제거 된 맬웨어를 포함 하는 전자 메일 메시지 *
4. 배달 후 제거 된 피싱 url을 포함 하는 전자 메일 메시지 *

* 참고:이 경고에는 전자 메일 알림이 해제 된 보안 및 준수 센터 내의 각 경고 정책에 "정보" 심각도가 할당 되어 있습니다. 이러한 구성은 경고 정책 구성을 통해 설정할 수 있습니다.

알림을 보려면 Office 365 보안 & 준수 센터에서 경고 **** > **보기 경고**를 선택 합니다. 알림을 선택 하 여 세부 정보를 확인 하 고, **보기 조사** 링크를 사용 하 여 해당 [조사](#investigation-graph)로 이동 합니다.

![조사로 연결 되는 경고](media/air-alerts-page-details.png) 


## <a name="security-playbooks"></a>보안 playbook

보안 playbook는 Microsoft Threat Protection의 자동화 핵심에 있는 백 엔드 정책입니다. AIR에서 제공 되는 보안 playbook은 일반적인 실제 보안 시나리오를 기반으로 합니다. 조직 내에서 경고가 트리거될 때 보안 playbook 자동으로 실행 됩니다. 알림이 트리거되어 연결 된 playbook 자동으로 실행 됩니다. playbook에서 조사를 실행 하 여 연결 된 모든 메타 데이터 (전자 메일 메시지, 사용자, 제목, 보낸 사람 등)를 보고, 결과에 따라 조직의 보안 팀이 제어 및 완화할 수 있는 일련의 작업을 권장 합니다. 위협입니다. 

AIR에서 제공 하는 보안 playbook은 조직이 현재 직면 하 고 있는 가장 빈번한 위협을 처리 하도록 설계 되었습니다. Microsoft 및 고객 자산을 보호 하는 데 도움이 되는 사용자를 비롯 하 여 보안 작업 및 사건 대응 팀의 입력을 기반으로 합니다.

### <a name="security-playbooks-are-rolling-out-in-phases"></a>보안 playbook가 단계별로 롤아웃 됨

AIR의 일환으로 보안 playbook가 단계별로 배포 됨

- **1 단계 (2019 년 4 월)**: playbooks에는 보안 관리자가 검토 하 고 승인할 작업에 대 한 권장 사항이 포함 되어 있습니다. 

- **2 단계 (6 월 2019)**: 보안 관리자는 관리 상호 작용 없이 작업을 자동으로 수행할 수 있도록 보안을 구성 하는 옵션을 사용할 수 있습니다.

1 단계에는 다음과 같은 playbooks가 포함 됩니다.
- 사용자가 보고 한 피싱 메시지
- URL 결과 변경 클릭 
- 맬웨어 배달 후 검색 (맬웨어 ZAP)
- 피싱 검색 된 배달 후 zap (피싱 ZAP)
- 위협 탐색기를 사용 하 여 수동 전자 메일 조사

다른 몇 가지 playbook에 대해서는 2 단계에 계획 되어 있습니다.

### <a name="playbooks-include-investigation-and-recommendations"></a>playbooks에는 조사 및 권장 사항이 포함 되어 있습니다.

각 playbook에는 다음이 포함 됩니다. 
- 루트 조사를 
- 다른 잠재적 위협을 식별 및 상호 연결 하기 위해 수행 되는 단계 
- 권장 되는 위협 재구성 작업

각 상위 단계에는 위협에 대 한 심층적이 고 자세한 응답을 제공 하기 위해 실행 되는 여러 하위 단계가 포함 됩니다.

## <a name="example-user-reported-phish-message"></a>예: 사용자가 보고 한 피싱 메시지

조직의 사용자가 전자 메일 메시지를 전송 하 고 [outlook 또는 outlook Web Access 용 보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 Microsoft에 보고 하는 경우 이는 조사 playbook를 자동으로 시작 하는 시스템 기반 정보 알림을 트리거합니다.

루트 조사 단계에서는 전자 메일의 다양 한 측면을 평가 합니다. 다음과 같은 다양한 알고리즘과 방법이 있습니다.
- 사용할 수 있는 위협의 유형에 대 한 결정
- 보낸 사람
- 전자 메일이 전송 되는 위치 (보내는 인프라)
- 전자 메일의 다른 인스턴스가 배달 되거나 차단 되었는지 여부
- 분석가의 평가
- 전자 메일이 알려진 캠페인과 연결 되어 있는지 여부
- 등이 있습니다.

루트 조사가 완료 된 후에는 playbook에서 수행할 권장 작업 목록을 제공 합니다.
  
다음으로 몇 가지 위협 조사 및 사냥 단계가 실행 됩니다.

- 다른 전자 메일 클러스터의 유사한 전자 메일 메시지가 검색 됩니다.
- 신호가 [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection)와 같은 다른 플랫폼과 공유 됩니다.
- 사용자가 의심 스러운 전자 메일 메시지에 있는 링크를 클릭 했는지 여부가 결정 됩니다.
- 확인은 office 365 Exchange Online protection ([EOP]) (EOP/exchange-online-EOP) 및 office 365 Advanced  for protection ([ATP]) (office-365-atp.md)을 통해 사용자가 보고 하는 다른 유사한 메시지가 있는지 확인 합니다.
- 사용자가 손상 되었는지 확인 하는 검사를 수행 합니다. 이 검사는 [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) 및 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory)간의 신호를 활용 하 여 관련 된 사용자 활동에 대 한 예외를 모두 연관 시킵니다. 

사냥 단계에서는 위험과 위협이 다양 한 구하기 단계에 할당 됩니다.  

재구성은 playbook의 마지막 단계입니다. 이 단계에서는 조사 및 구하기 단계를 기반으로 하 여 수정 단계를 수행 합니다.  

## <a name="getting-started"></a>시작

office 365 전역 관리자, 보안 관리자 또는 보안 읽기 권한자로 조사에 액세스 하려면 office 365 security & 준수 센터 ([https://protection.office.com](https://protection.office.com))로 이동 하 여 로그인 합니다. 다음 중 하나를 수행합니다.

- 왼쪽 탐색에서 **위협 관리** > **조사**로 이동 합니다.

    또는

- 보안 & 준수 센터에서 **위협 관리** > **대시보드로**이동 하 여 위협 관리 대시보드를 방문 합니다.

![AIR 위젯](media/air-widgets.png)

무선 위젯은 [보안 대시보드의](security-dashboard.md)위쪽에 표시 됩니다. 시작 하려면 위젯을 선택 합니다.

관련 경고에서 직접 invesitgation에 액세스할 수도 있습니다.

### <a name="automated-investigations"></a>자동화 된 조사

자동화 된 조사 페이지에 조직의 조사 및 현재 상태가 표시 됩니다.

![AIR의 주 조사 페이지](media/air-maininvestigationpage.png) 
  
예를 들어 다음을 수행할 수 있습니다.
- 조사로 직접 이동 합니다 ( **조사 ID**선택).
- 필터를 적용 합니다. **조사 유형**, **시간 범위**, **상태**또는 이들의 조합 중에서 선택 합니다.
- 데이터를 CSV 파일로 내보냅니다.

### <a name="investigation-graph"></a>조사 그래프

특정 조사를 열면 조사 그래프 페이지가 표시 됩니다. 이 페이지에는 전자 메일 메시지, 사용자 (및 해당 활동), 트리거된 알림의 일부로 자동 조사 되는 장치 등의 다양 한 엔터티가 모두 표시 됩니다.

![AIR 조사 그래프 페이지](media/air-investigationgraphpage.png)

예를 들어 다음을 수행할 수 있습니다.
- 현재 조사에 대 한 시각적 개요를 볼 수 있습니다.
- 조사 시간에 대 한 요약을 봅니다.
- 시각화에서 노드를 선택 하 여 해당 노드의 세부 정보를 확인 합니다.
- 위쪽에서 탭을 선택 하 여 해당 탭의 세부 정보를 확인 합니다.

### <a name="alert-investigation"></a>경고 조사

조사에 대 한 **알림** 탭에서 조사와 관련 된 경고를 볼 수 있습니다. 세부 정보에는 조사를 트리거한 경고와 확인에 상관 된 위험한 로그인, 대량 다운로드 등의 기타 알림이 포함 됩니다. 이 페이지에서는 보안 분석가가 개별 경고에 대 한 추가 세부 정보를 볼 수도 있습니다.

![AIR 알림 페이지](media/air-investigationalertspage.png)

예를 들어 다음을 수행할 수 있습니다.
- 현재 트리거하는 경고 및 관련 경고에 대 한 시각적 개요를 볼 수 있습니다.
- 목록에서 알림을 선택 하 여 전체 알림 세부 정보를 표시 하는 플라이 아웃 페이지를 엽니다.

### <a name="email-investigation"></a>전자 메일 조사

조사를 위해 **전자 메일** 탭에서 조사 중에 식별 된 모든 전자 메일 클러스터를 볼 수 있습니다. 

조직의 사용자가 보내고 받는 전자 메일 양이 주어 지 면 
- 메시지 헤더, 본문, URL 및 첨부 파일의 비슷한 특성에 따라 전자 메일 메시지를 클러스터링 합니다. 
- 악성 전자 메일과 좋은 전자 메일을 구분 합니다. 한 
- 악성 전자 메일 메시지에 대 한 작업 수행 

몇 시간 정도 걸릴 수 있습니다. 이제 AIR에서이 프로세스를 자동화 하 여 조직의 보안 팀 시간과 노력을 절약 합니다. 

예를 들어 다음과 같은 시나리오를 가정해 봅니다. 세 개의 전자 메일 메시지 중 첫 번째 클러스터는 피싱 것으로 간주 됩니다. 이러한 항목 중 일부는 초기 검색을 수행 하는 동안 피싱으로 식별 되었기 때문에 같은 IP 및 주체를 포함 하는 비슷한 메시지의 다른 클러스터가 발견 되어 악성으로 간주 되었습니다. 

![AIR 전자 메일 조사 페이지](media/air-investigationemailpage.png)

예를 들어 다음을 수행할 수 있습니다.
- 현재 클러스터링 결과 및 발견 된 위협에 대 한 시각적 개요를 볼 수 있습니다.
- 클러스터 엔터티 또는 위협 목록을 클릭 하 여 전체 알림 세부 정보를 표시 하는 플라이 아웃 페이지를 엽니다.

![플라이 아웃 세부 정보를 사용한 AIR 조사 전자 메일](media/air-investigationemailpageflyoutdetails.png)

* 참고: 전자 메일 컨텍스트에서 조사 중에 볼륨 변칙 위협 표면을 볼 수 있습니다. 볼륨 변칙은 이전에 나온 시간과 비교 하 여 조사 이벤트에 대 한 유사한 전자 메일의 스파이크를 나타냅니다. 전자 메일 트래픽 (예: 제목 및 보낸 사람 도메인, 본문 유사성 및 보낸 사람 IP)이 비슷한 방식으로 전자 메일을 사용 하는 것이 일반적입니다. 그러나 시간에도 대량 및 spom 전자 메일 캠페인을 통해 이러한 특성을 공유할 수 있습니다. 볼륨 예외는 잠재적 위협을 나타내므로, 바이러스 백신 엔진, 샌드 박싱 또는 악의적인 평판을 사용 하 여 식별 된 맬웨어 또는 피싱 위협과 비교 하는 것이 더 심각 하지 않습니다.

### <a name="user-investigation"></a>사용자 조사

**사용자** 탭에서는 조사의 일부로 식별 된 모든 사용자를 볼 수 있습니다. 

예를 들어 다음 이미지에서 AIR은 생성 된 새 받은 편지함 규칙을 기반으로 하는 손상 및 예외 표시등을 식별 했습니다. 조사에 대 한 자세한 내용은이 탭 내의 자세한 보기를 통해 확인할 수 있습니다. 손상 및 변칙에 대 한 표시기에는 [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)의 변칙 검색이 포함 될 수도 있습니다.

![AIR 조사 사용자 페이지](media/air-investigationuserspage.png)

예를 들어 다음을 수행할 수 있습니다.
- 발견 된 사용자 결과 및 위험에 대 한 시각적 개요를 확인 하세요.
- 전체 알림 세부 정보를 표시 하는 플라이 아웃 페이지를 열 사용자를 선택 합니다.

### <a name="machine-investigation"></a>컴퓨터 조사

**컴퓨터** 탭에서 조사 과정으로 식별 된 모든 컴퓨터를 볼 수 있습니다. 

![AIR 조사 컴퓨터 페이지](media/air-investigationmachinepage.png)

조사 과정에서 AIR은 전자 메일 위협의 상관 관계를 장치에 맞게 합니다. 예를 들어 조사를 통해 조사를 위해 [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) 에 파일 해시를 전달 합니다. 이렇게 하면 사용자에 대 한 관련 시스템을 자동으로 조사 하 고 클라우드 및 장치 전체에서 위협이 해결 되도록 할 수 있습니다. 

예를 들어 다음을 수행할 수 있습니다.
- 발견 된 현재 컴퓨터 및 위협에 대 한 시각적 개요를 볼 수 있습니다.
- 컴퓨터를 선택 하 여 windows defender atp 보안 센터에서 관련 [Windows defender atp 조사](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection) 로 연결 되는 보기를 엽니다.

### <a name="entity-investigation"></a>엔터티 조사

**엔터티** 탭에서 조사 중에 식별 된 모든 컴퓨터를 볼 수 있습니다. 

여기에서 조사 된 엔터티를 볼 수 있습니다. 전자 메일 메시지, 클러스터, IP 주소, 사용자 등의 엔터티 유형에 대 한 세부 정보를 볼 수 있습니다. 또한 분석 된 엔터티 수와 각 엔터티가 연결 된 위협을 볼 수 있습니다. 

![AIR 조사 엔터티 페이지](media/air-investigationentitiespage.png)

예를 들어 다음을 수행할 수 있습니다.
- 발견 된 조사 엔터티 및 위협에 대 한 시각적 개요를 확인 하세요.
- 엔터티를 선택 하 여 관련 엔터티 세부 정보를 표시 하는 플라이 아웃 페이지를 엽니다.

![AIR 조사 엔터티 세부 정보](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>Playbook 로그

**로그** 탭에서는 조사 중에 발생 한 모든 playbook 단계를 볼 수 있습니다. 로그에는 AIR의 일부로 서 Office 365 자동 조사 기능을 통해 완료 된 모든 작업의 전체 인벤토리가 캡처됩니다. 작업 자체, 설명, 실제 시작 날짜를 포함 하 여 수행 된 모든 단계를 명확 하 게 확인할 수 있습니다. 

![AIR 조사 로그 페이지](media/air-investigationlogpage.png)

예를 들어 다음을 수행할 수 있습니다.
- playbook 수행 된 단계에 대 한 시각적 개요를 참조 하세요.
- 결과를 CSV 파일로 내보냅니다.
- 보기를 필터링 합니다.

### <a name="recommended-actions"></a>권장 작업

조사가 완료 된 후에 수정이 권장 되는 모든 playbook 작업을 **작업** 탭에서 확인할 수 있습니다. 

작업 조사를 마칠 때까지 수행 하는 것이 권장 되는 단계를 캡처합니다. 하나 이상의 작업을 선택 하 여 여기에서 수정 작업을 수행할 수 있습니다. **승인을** 클릭 하면 재구성을 시작할 수 있습니다. 적절 한 사용 권한이 필요 합니다. 예를 들어 보안 독자는 작업을 볼 수 있지만 승인 하지는 않습니다.  

![AIR 조사 작업 페이지](media/air-investigationactionspage.png)

예를 들어 다음을 수행할 수 있습니다.
- playbook 권장 작업에 대 한 시각적 개요를 볼 수 있습니다.
- 단일 작업 또는 여러 작업을 선택 합니다.
- 설명으로 권장 작업을 승인 하거나 거부 합니다.
- 결과를 CSV 파일로 내보냅니다.
- 보기를 필터링 합니다.

## <a name="how-to-get-air"></a>공기를 얻는 방법

현재 Office 365 AIR이 미리 보기에 있습니다. Office 365 AIR은 다음 구독에 포함 될 예정입니다.

- Microsoft 365 Enterprise E5
- Office 365 Enterprise E5
- Microsoft Threat Protection
- Office 365 Advanced Threat Protection 계획 2

기능 가용성에 대 한 자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap)를 참조 하세요.
