---
title: 고급 eDiscovery (미리 보기) (영문) Microsoft 365 개요
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 이 문서에서는 Microsoft 365의 고급 eDiscovery (미리 보기)의 새 버전에 설명 합니다.
ms.openlocfilehash: cb82541037983ca21cefbefb7f72fffa3b054373
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706159"
---
# <a name="overview-of-advanced-ediscovery-preview-in-microsoft-365"></a>고급 eDiscovery (미리 보기) (영문) Microsoft 365 개요

Microsoft은 Office 365의 기존 eDiscovery 기능에 구축할 수 있는 업데이트 된 고급 eDiscovery 도구의 미리 보기 버전을 릴리스 방금 했습니다. *고급 eDiscovery (미리 보기)* 이라고 하는이 미리 보기 버전을 보존, 수집, 검토, 분석 및 콘텐츠는 조직의 내부 및 외부 조사에 응답 하는 내보내기 끝-워크플로 제공 합니다. 

## <a name="alignment-with-edrm"></a>EDRM와 맞춤

고급 eDiscovery (미리 보기)의 기본 제공 워크플로 전자 검색 참조 모델 (EDRM)에서 설명한 eDiscovery 프로세스에 맞춥니다. 

![전자 검색 참조 모델 EDRM)](../media/EDRMv1.png)

(Edrm.net의 관례 대로 이미지 원본입니다. 소스 이미지 사용 가능 했지만 창의적인 일반 특성이 3.0 Unported 라이선스에 따라.)

다음 방법을 고급 eDiscovery 높은 수준 (미리 보기) EDRM 워크플로 지원 합니다.

- **식별** -조사에 관심 잠재적 장애인을 식별 한 후 다음을 추가할 수 있습니다 (라고도 함 *데이터 custodians*조사와 관련 된 정보가 소유 수 있으므로) custodians로는 고급 eDiscovery (미리 보기) 대문자로 표시 합니다. 사용자가 custodians로 추가한 후 보존, 수집 및 더불어 문서를 검토 하기 쉽습니다.

- **보존** -을 보존 하 고는 조사와 관련 된 데이터를 보호 하려면 eDiscovery (미리 보기) 사용 할 수 있습니다 법적 보유 경우에서 custodians 연관 된 데이터 원본에 고급 합니다. 또한 대기 custodial 아닌 데이터를 배치할 수 있습니다. 또한 고급 eDiscovery (미리 보기)는 기본 제공 통신 워크플로 custodians를 법적 보유 알림을 보낼 하 고 해당 승인 과정을 추적할 수 있도록 합니다.

- **컬렉션** -하 한 후 식별 (보존) 조사와 관련 된 데이터 원본, custodial 데이터 원본의 (및 비 custodial에 대 한 고급 eDiscovery (미리 보기) 검색 하 고 라이브 데이터 수집에 기본 제공 검색 도구를 사용할 수 있습니다. 데이터 원본에 해당 하는 경우)는 대/소문자와 관련 될 수 있습니다.

- **처리** -대/소문자에 관련 된 모든 데이터를 수집한 후, 다음 단계는 프로세스를 추가 검토 및 분석을 위해 합니다. 고급 eDiscovery (미리 보기), 수집 단계에서 식별 하는 전체 데이터는 위치로 복사 Azure 저장소 ( *집합 (영문)*)을 사례 데이터의 정적 뷰를 제공 하는 것을 의미 합니다. 
 
- **검토** -데이터를 작업에 추가 된 후 설정, 특정 문서를 볼 하 고 추가 쿼리를 실행할 수 있습니다.  
 
- **분석** -고급 eDiscovery (미리 보기) 수를 결정 하는 작업 집합의 데이터를 cull 하는데 도움이 되는 통합 된 분석 도구 조사와 관련이 없습니다를 제공 합니다. 관련 데이터의 양은 감소, 화면 전환 eDiscovery (미리 보기)를 통해 쉽고 더 효율적으로 검토 과정을 확인 하는 콘텐츠를 구성할 수 있도록 하 여 법률 검토 비용을 저장할 수 있습니다.

- **프로덕션** 및 **프레젠테이션** -준비 되 면 법률 검토를 위해 작업 집합에서 문서를 내보낼 수 있습니다. 제 3 자 검토 응용 프로그램으로 가져올 수 있도록 하는 EDRM 지정 된 형식 또는 원시 형식으로 문서를 내보낼 수 있습니다.

## <a name="advanced-ediscovery-preview-workflow"></a>고급 eDiscovery (미리 보기) 워크플로

다음 섹션에서는 고급 eDiscovery (미리 보기)의 기본 제공 워크플로의 각 단계에 설명 합니다. 다음 스크린샷은 *제품 책임 2019002*라는 하는 경우의 **홈** 탭 모양을 보여줍니다. Note 페이지의 위쪽에 워크플로 탭에 EDRM 프로세스에 맞춰 정렬 됩니다. 

고급 eDiscovery (미리 보기)의 끝-워크플로 하는 방법에 대 한 자세한 내용은이 [비디오 Microsoft 메커니즘](https://go.microsoft.com/fwlink/?linkid=2066133)을 참조 하십시오. 

![EDRM 워크플로 수행 하는 고급 eDiscovery (미리 보기)의 탭](../media/aedisco-homepage-1.png)

## <a name="managing-custodians"></a>보유자 관리

추가 하 고 대/소문자에 관계가 사용자에 게로 식별 한 사람을 관리 하려면 **Custodians** 탭을 사용 합니다. Custodians에 추가할 때 신속 하 게 작업을 수행할 수 더불어 관련 된 법적 방법 더불어 데이터 원본에 배치 하는 등, 예: 사서함 및 OneDrive 계정 custodians와 통신 및 콘텐츠를 수집 하려면 더불어 데이터 원본 검색 하는 대/소문자와 관련이 있습니다. 사례 진행률 파일로 새 custodians를 추가 하거나 대/소문자에서 custodians 릴리스 하기 쉽습니다. 자세한 내용은 [고급 eDiscovery (미리 보기)에서 custodians와 함께 작동](managing-custodians.md)을 참조 하십시오.

## <a name="managing-legal-hold-notifications"></a>법적 보유 알림 관리

**Communications** 탭을 사용 하 여 경우에서 custodians와 통신 하는 프로세스를 관리 합니다. 법적 보유 통지 대/소문자와 관련 될 수 있는 모든 콘텐츠를 유지 하기 위해 custodians에 지시 합니다. 법적 팀 수 통지를 수신, 읽기, 및 custodians 하 여 승인 된가 추적할 수 있어야 합니다. 고급 eDiscovery (미리 보기)의 통신 워크플로 만들기 및 보류 알림을 승인할 custodians 실패 하는 경우 초기 알림, 미리 알림, 릴리스 통지 및 에스컬레이션을 보낼 수 있습니다. 자세한 내용은 [고급 eDiscovery (미리 보기)의 통신 사용](managing-custodian-communications.md)을 참조 합니다.

## <a name="managing-content-preservation"></a>콘텐츠 보존 관리

사례에 대 한 더불어를 추가할 때 custodial 데이터에 대 한 보류 시키려면 옵션도 있습니다. 사용을 **포함 하 고** 탭 만든 custodians를 추가 하 고 추가 법률을 관리 하는 경우 보류를 관리 하는 대/소문자; 연관 포함 하 고 예, 확인 하 고 custodial 아닌 데이터 원본에 보류를 배치 하 수 있습니다. 또한 경우에 모든 보류를 편집 하 고 수 있도록 쿼리 기반 보존 대기; 쿼리와 일치 하는 콘텐츠만 놓입니다 수 있습니다. 예, 특정 날짜의 범위 내에서 만든 콘텐츠만 보존 되도록 날짜 범위를 보류에 추가할 수 있습니다. 보류 중인 콘텐츠에 대 한 통계를 가져올 하 하거나 되었을 때 더이상 경우에는 관련 된 후 보류를 제거 삭제할 수도 없습니다. 자세한 내용은 [고급 eDiscovery (미리 보기)에서 유지 관리를](managing-holds.md)참조 하십시오.

## <a name="indexing-custodian-data"></a>인덱싱 더불어 데이터

사례에 대 한 더불어 및 해당 하는 custodial 데이터 원본의 추가할 때 더불어 데이터 원본의 모든 부분적으로 인덱싱된 항목은 다시 (사용 하 여 인덱싱된 *인덱싱 고급*이라는 프로세스). 이 통해 custodial 콘텐츠 예: 이미지, 지원 되지않는 파일 형식 및 기타 잠재적으로 인덱싱되지 않은 콘텐츠는 대/소문자와 관련이 있는 데이터를 수집 하도록 검색을 실행 하는 경우 완벽 하 게 검색할 수 있습니다. **처리** 탭을 사용 하 여 고급 인덱싱 및 (사용 하 여 오류 프로세스 calle *오류 수정*합니다.)를 처리 하는 수정 프로그램의 상태를 모니터링 합니다. 자세한 내용은 [고급 eDiscovery (미리 보기)에서 처리 오류를 해결](processing-data-for-case.md)을 참조 하십시오.

## <a name="collecting-case-data"></a>사례 데이터 수집하기

**검색** 탭을 사용 하 여 Office 365의 대/소문자와 관련 된 콘텐츠에 대 한 전체 custodial를 검색 하려면 검색 및 custodial 아닌 데이터 원본을 만들 수 있습니다. 만들 수 있으며 집합 전자 메일 메시지를 식별 하 (키워드와 조건을 사용 하 여) 하는 쿼리 기반 검색을 실행 하 고 대/소문자와의 사용자와 관련 된 문서를 검토 한 자세한 내용은 및 eDiscovery 워크플로의 이후 단계에서 분석 해야 합니다. 대/소문자와 관련 된 하나 이상의 검색을 만들 수 있습니다. 또한 예제 문서 미리 보기를 검색 도구를 사용할 수 있으며 도움이 될 수 있는 보기 검색 통계 구체화 하 고 검색 결과 개선 합니다. 한번 하면 검색 결과 포함 된 모든 데이터를 대/소문자와 관련이 있는지, 추가 검토, 분석에 대 한 작업 집합을 검색 결과 추가 충족 하 고 필요한 경우 컬링을 합니다. 자세한 내용은 [고급 eDiscovery (미리 보기)의 경우에 대 한 데이터 수집](collecting-data-for-ediscovery.md)을 참조 하십시오.

## <a name="reviewing-and-analyzing-case-data"></a>검토 및 사례 데이터 분석

**집합 (영문)** 탭을 사용 하 여 또는 검토 하 고 라이브 시스템에서 수집 하 고 작업 집합에 추가 되었는지 여부를 지정 하는 콘텐츠를 분석 합니다. Custodial 데이터의 정적 컬렉션 (즉, 오프 라인 복사본 수 있음)은 *작업 집합* (해당 되는 경우 및 custodial 아닌 데이터) eDiscovery 워크플로의 이전 단계에서 수집 된 합니다. 작업 집합을 검색 결과 추가할 때 컨테이너에서 파일을 추출 하 고 메타 데이터를 추출 하 여 텍스트를 추출 하는 프로세스를 트리거됩니다. 이 프로세스가 완료 되 면 시스템 custodians에서 수집 하 고 작업 집합에 추가 된 모든 데이터의 새 인덱스를 구축 합니다. 데이터 작업 집합에 추가 되 면 사례 데이터 범위를 좁힐, 텍스트 또는 기본 파일 형식에서 데이터를 볼 및 주석을 달, 교정, 추가 쿼리를 실행할 수 및 대리인으로 작업에서 태그 문서 설정 합니다. 또한 문서 중복 식별, 스레딩, 전자 메일을 같은 및 테마 고급 분석을 수행할 수 있습니다. 데이터를 대/소문자와 관련이 란만 컬링 했을 때, 되 면 다운로드 문서를 직접 다운로드 또는 파일 메타 데이터, 주석 및 모든 태그와 함께 내보낼 수 있습니다. 자세한 내용은 다음을 참조 합니다.

  - [고급 eDiscovery (미리 보기)의 경우 데이터를 검토 합니다.](reviewing-data-in-working-set.md)
  - [고급 eDiscovery (미리 보기)에서 작업 집합의 데이터를 분석 합니다.](analyzing-data-in-working-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>검토 및 표시에 대 한 데이터 내보내기 (영문)

작업 집합에서 데이터를 내보낸 후 내보내기 작업을 관리 하 고 작업 집합에서 데이터를 다운로드 하려면 **내보내기** 탭을 사용 합니다. 작업 집합을 내보낼 때 데이터 Azure 저장소 위치로 업로드 이며 다음 로컬 컴퓨터에 다운로드할 수 있습니다. 위치를 받아 저장소 **내보내기** 탭에서 내보낸된 데이터를 다운로드 하는 데 필요한 키를 평가 합니다. 자세한 내용은 [고급 eDiscovery (미리 보기)의 경우 데이터를 내보냅니다](exporting-data-ediscover20.md)를 참조 하십시오.

## <a name="managing-jobs"></a>작업 관리

**작업** 탭을 사용 하 여 시작 했을 때 된 사례 관련 작업, 검색으로 다시 인덱싱, 검색 및 내보내기에 대 한 장기 실행 프로세스를 모니터링 합니다. 예, 많은 수의 데이터 원본 포함 하는 **검색** 탭에서 새 검색을 만들 수 있습니다. 이 검색 프로세스의 상태는 **작업** 탭에 표시 됩니다. 자세한 내용은 [고급 eDiscovery (미리 보기)에서 관리 작업](managing-jobs-ediscovery20.md)을 참조 하십시오.

## <a name="configuring-case-settings"></a>사례 설정 구성

**설정** 탭을 사용 하 여 사례 수준 설정을 구성 합니다. 이 사례를 닫는 또는 사례를 삭제 하 고, 검색 및 분석 기능과 동작을 구성에 구성원 추가 (영문)를 포함 합니다. 자세한 내용은 [고급 eDiscovery (미리 보기)의 경우 설정 구성을](configuring-case-settings-ediscovery20.md)참조 하십시오.

