---
title: Office 365 고급 eDiscovery 검색 결과 준비
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportWithZoom
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0b6fac2d-8627-4b05-9df0-03609db6248b
description: Office 365 보안에서 콘텐츠 검색의 결과 준비 하는 방법에 알아봅니다 &amp; 고급 eDiscovery 도구를 사용 하 여 분석 추가 대 한 준수 센터입니다.
ms.openlocfilehash: c70eec691359170ae67e431f20e3b8ad389443f3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "27280171"
---
# <a name="prepare-search-results-for-office-365-advanced-ediscovery"></a>Office 365 고급 eDiscovery 검색 결과 준비

Office 365 보안에서 eDiscovery 사례와 관련 된 검색 한 후 &amp; 준수 센터 성공적으로 실행 된, 큰 분석할 수 있습니다, Office 365 고급 eDiscovery 사용 하 여 분석 추가 대 한 검색 결과 준비할 수 있습니다 구조화 되지 않은 데이터 설정 하 고 법적 사례와 관련 된 데이터의 양을 줄일 합니다. 고급 eDiscovery 기능은 다음과 같습니다.
  
- **광학 문자 인식** -자동으로 고급 eDiscovery, 광학 문자 인식 (OCR) 기능에 대 한 검색 결과 준비할 때는 이미지, 텍스트 추출 하 고이를 로드 되는 검색 결과 함께 포함 분석을 위해 고급 eDiscovery 합니다. 메뉴 및 도구 모음을 OCR 느슨한 파일에 대 한 지원 전자 메일 첨부 파일, 이미지를 포함 합니다. 이 옵션을 사용 하면 이미지 파일의 텍스트 콘텐츠 (중복 근처, 전자 메일 스레딩, 테마 및 예측 코딩) 고급 eDiscovery의 텍스트 분석 기능을 적용할 수 있습니다. 고급 eDiscovery OCR 이미지 파일에 대 한 다음과 같은 형식을 지원합니다.

    - GIF
    - JPEG
    - JPG
    - PNG
    - TIFF
    
- **거의 비슷한 검색** -그룹 비슷한 문서를 검토 하는 두 명 하므로 데이터 검토를 보다 효율적으로 구성 수 있습니다. 이렇게 하면 여러 검토자가 동일한 문서의 여러 버전을 볼 수 있는 것을 방지할 수 있습니다. 
    
- **전자 메일 스레딩** -각 메시지에 대 한 새 정보만에 초점을 맞출 수 있도록 전자 메일 스레드에서 고유한 메시지를 확인할 수 있습니다. 전자 메일 스레드 두번째 메시지는 첫번째 메시지를 포함 합니다. 마찬가지로, 이후 메시지 이전의 모든 메시지를 포함 합니다. 전자 메일 스레딩 전체 전자 메일 스레드에서 모든 메시지를 검토 하려면 필요를 제거 합니다. 
    
- **테마** -키워드 검색 통계 초과 하는 데이터에 대 한 중요 한 정보를 얻을 수 있습니다. 테마 컨텍스트에서 문서를 볼 수 있도록 관련된 문서를 그룹화 하 여 조사 하는 데 도움이 됩니다. 테마를 사용 하는 경우 문서 집합에 대 한 관련된 테마를 볼 하 고, 모든 겹치는 부분 확인 하 고, 다음 관련된 데이터의 횡단면을 식별할 수 있습니다. 
    
- 시스템에서 원하는 항목을 대 한 자료 인지 여부와 관련) (약 결정을 내릴 수 있도록 하 여 교육 수 **예측 코딩** -작은 문서 집합에 있습니다. 고급 eDiscovery (에 대 한 지침에 따라) 해당 학습을 적용 하는 모든 데이터 집합에 있는 문서를 분석 하는 경우. 어떤 문서를 검토 하는 일 가능성이 가장 높은 경우에 적절 한 것으로 어떤 문서를 기반으로 결정할 수 있도록 관련성 순위 고급 eDiscovery 제공 해당 학습을 기반으로 합니다. 
    
- **응용 프로그램을 검토 하는 내보내기 데이터에 대 한** -분석을 완성 하 고 데이터 집합을 축소 한 후 고급 eDiscovery 및 Office 365에서 데이터를 내보낼 수 있습니다. 내보내기 패키지에서 내보낸된 콘텐츠 및 분석 메타 데이터 속성을 포함 된 CSV 파일을 포함 합니다. EDiscovery 검토 응용 프로그램에이 내보내기 패키지를 가져올 수 있습니다. 
    
## <a name="before-you-begin"></a>시작하기 전에

- 고급 eDiscovery를 사용 하 여 사용자의 데이터를 분석 하려면 (데이터의 더불어) 사용자는 Office 365 E5 라이선스를 할당 합니다. 또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자의 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다. 관리자 및 규정 준수 관리자의 경우에 할당 된 및 고급 eDiscovery를 사용 하 여 데이터를 분석 하 게 e 5 라이선스가 필요는 없습니다. 
    
- EDiscovery 관리자 또는 eDiscovery Office 365 보안의 관리자 여야 &amp; 준수 센터 고급 ediscovery 검색 결과 준비를 합니다. EDiscovery 관리자는 eDiscovery 관리자 역할 그룹의 구성원입니다. EDiscovery 관리자도 eDiscovery 관리자 역할 그룹의 구성원 이지만 추가 eDiscovery 권한을 할당 합니다. EDiscovery 관리자 권한을 할당 하는 방법에 대 한 지침에 대 한 [Office 365 보안 & 준수 센터의에서 eDiscovery 사례](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members)에서 1 단계를 참조 하십시오.
    
## <a name="step-1-prepare-search-results-for-advanced-ediscovery"></a>1 단계: 준비 고급 eDiscovery에 대 한 결과 검색 합니다.

EDiscovery 사례와 관련 된 검색의 결과 준비할 수 있습니다. 고급 ediscovery 검색 결과 준비 하는 경우 데이터 업로드를 업데이트 하 고 Microsoft 클라우드에서 고유한 Windows Azure 저장소 영역에 일시적으로 저장 됩니다. 이 시점 것 OCR 기능 검색 결과에서 이미지에서 텍스트를 추출 합니다. [2 단계](#step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery),이 텍스트와 다른 검색에서 고급 eDiscovery의 대/소문자를 결과 데이터에 로드 됩니다.
  
1. 보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다. 
    
2. 고급 eDiscovery에 대 한 분석을 위해 검색 결과 준비 하려는 경우 다음 **열기** 를 클릭 합니다. 
    
3. 대/소문자에 대 한 **홈** 페이지에서 **검색**을 클릭 하 고 검색을 선택 합니다.
    
4. 세부 정보 창에서 **고급 eDiscovery 사용 하 여 분석 결과**얻으려면 아래에서 **분석을 위해 준비 결과**클릭 합니다.
    
    > [!NOTE]
    > 검색 결과가 7일보다 오래된 경우 검색을 다시 시작하여 검색 결과를 새로 고치라는 메시지가 표시됩니다. 
  
5. **결과 분석 준비** 페이지에서 다음을 수행합니다.  
    
    - 인덱싱된 항목, 인덱스 및 인덱싱되지 않은 항목 또는 인덱싱되지 않은 항목에 대해서만 고급 eDiscovery에 대 한 분석을 위해 준비 하려면이 옵션을 선택 합니다.
    
    - 문서 검색 조건을 충족 하는 SharePoint에서 찾은 모든 버전을 포함할지 여부를 선택 합니다. 이 옵션은 검색에 대 한 콘텐츠 원본 사이트를 포함 하는 경우에 나타납니다.
    
    - 알림 메시지를 보낸 (또는 복사) 준비 프로세스가 완료 되 면 사람에 게 및 데이터는 고급 ediscovery에서 처리할 준비가 할지 여부를 지정 합니다.
    
6. **준비**를 클릭합니다.
    
    검색 결과 고급 eDiscovery 사용 하 여 분석에 대 한 준비를 합니다.
    
7. 세부 정보 창에서 준비 프로세스에 대 한 정보를 표시 하도록 **준비 상태 확인** 을 클릭 합니다. 준비 프로세스가 완료 되 면 하는 경우에 분석을 위해 데이터를 처리 하는 고급 ediscovery에서 사례에 이동할 수 있습니다. 
    
## <a name="step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery"></a>고급 ediscovery에서 사례에 검색 결과 데이터를 추가 하는 2 단계:
<a name="step2"> </a>

준비 완료 되 면 다음 단계에서는 고급 eDiscovery로 이동 하 고 고급 eDiscovery의 대/소문자 (하는 Microsoft 클라우드에서 Azure 저장소 영역에 업로드 한) 검색 결과 데이터를 로드 하는 합니다. EDiscovery 보안에서 관리자 여야 하는 고급 eDiscovery에 액세스 하려면 앞부분에 설명 &amp; 준수 센터 또는 고급 ediscovery에서 관리자입니다.
  
> [!NOTE]
> 보안에서 데이터에 대 한 걸리는 시간 &amp; 준수 센터의 고급 eDiscovery 사례에 추가할 수는 eDiscovery 검색 결과의 크기에 따라 달라 집니다. 
  
1. 보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다. 
    
2. 고급 ediscovery에서로 데이터 로드 하려는 경우 다음 **열기** 를 클릭 합니다. 
    
3. 사례에 대한 **홈** 페이지에서 **Advanced eDiscovery**를 클릭합니다. 
    
    ![고급 eDiscovery의 대/소문자를 열려면 고급 ediscovery 스위치를 클릭 합니다.](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    **고급 ediscovery 연결** 진행률 표시줄이 표시 됩니다. 고급 eDiscovery에 연결 하는 경우 대/소문자에 대 한 설치 페이지에서 컨테이너의 목록이 표시 됩니다. 
    
    ![대/소문자 고급 eDiscovery에 표시 됩니다.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     이러한 컨테이너 고급 eDiscovery (영문) 1 단계에서에서 분석을 위해 준비 하는 검색 결과를 나타냅니다. 참고 하는 컨테이너의 이름 이름이 같은 검색의 보안의 경우에서 &amp; 준수 센터입니다. 목록에서 컨테이너는 준비한 메시지입니다. 다른 사용자, 고급 ediscovery 검색 결과 준비 하는 경우 해당 컨테이너 목록에 포함 되지 않습니다. 
    
4. 검색 결과 데이터를 컨테이너에서 고급 eDiscovery의 대/소문자를 로드 하려면 컨테이너를 선택 하 고 **프로세스**를 클릭 합니다.
    
## <a name="next-steps"></a>다음 단계

EDiscovery의 결과 후 검색 데이터를 분석 하 고는 특정 법률 사례에 응답 하는 콘텐츠를 식별 하는 고급 eDiscovery 도구를 사용 하 여 다음 단계는 경우에 추가 됩니다. 고급 eDiscovery를 사용 하는 방법에 대 한 정보를 [Office 365 고급 eDiscovery](office-365-advanced-ediscovery.md)를 참조 하십시오.
  
## <a name="more-information"></a>추가 정보

고급 eDiscovery에 대 한 분석을 위해 준비 하는 경우 검색 결과에 포함 된 모든 RMS 암호화 된 전자 메일 메시지의 암호를 해독할 수 됩니다. 이 암호 해독 기능 eDiscovery 관리자 역할 그룹의 구성원에 대해 기본적으로 사용 됩니다. 즉,이 역할 그룹에는 RMS 암호 해독 관리 역할 할당 됩니다. 전자 메일 메시지의 암호를 해독 하는 방법에 대 한 염두에 다음과 같은 사항에 유의 하십시오.
  
- 현재이 암호 해독 기능 비즈니스 사이트에 대 한 SharePoint 및 OneDrive에서 암호화 된 콘텐츠를 포함 되지 않습니다. RMS 암호화 된 전자 메일 메시지에만 해당를 내보낼 때 암호가 해독 되도록 합니다.
    
- RMS 암호화 된 전자 메일 메시지에도 암호화 됩니다 (예: 문서 또는 다른 전자 메일 메시지) 첨부 파일, 최상위 전자 메일 메시지에만 암호가 해독 되도록 합니다.
    
- (기본 제공 eDiscovery 관리자 역할 그룹을 복사 하는) 하 여 사용자 지정 역할 그룹을 만들고 다음 RMS를 제거 하려면 해야 다른 사용자가 고급 eDiscovery에 대 한 분석을 위해 검색 결과 준비 하는 경우 RMS 암호화 된 메시지의 암호를 해독 하지 못하도록 해야 하는 경우 관리 역할의 사용자 지정 역할 그룹에서 암호를 해독 합니다. 사용자 지정 역할 그룹의 구성원으로 메시지를 암호 해독 하려면 사용자를 추가 합니다.
