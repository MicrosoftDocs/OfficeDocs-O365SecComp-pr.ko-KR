---
title: eDiscovery 솔루션 계열 데이터 액체 엎질렀는지 여부 시나리오-검색 및 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d945f7dd-f62f-4ca7-b3e7-469824cfd493
description: Office 365 eDiscovery 및 검색 도구를 사용 하 여 관리 하 고 조직에서 문제가 발생 한 데이터 액체 엎질렀는지 여부에 응답 합니다.
ms.openlocfilehash: 4da8efdb6f5d129e08d85f9b6c94726a7d099cb3
ms.sourcegitcommit: dd58ed6fd424272e361bc3c109ecd6d63d673048
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2018
ms.locfileid: "25566879"
---
# <a name="ediscovery-solution-series-data-spillage-scenario---search-and-purge"></a>eDiscovery 솔루션 시리즈: 데이터 액체 엎질렀는지 여부 시나리오-검색 및 삭제

 **데이터 액체 엎질렀는지 여부 이란 무엇 이며 왜 문제를 고려해 야 합니까?** 신뢰할 수 없는 환경에 기밀 문서를 놓을 때 데이터 액체 엎질렀는지 여부 하 게 합니다. 데이터 액체 엎질렀는지 여부 문제를 검색 하는 경우에, 크기 및 위치는 액체 엎질렀는지 여부의 신속 하 게 평가 하 고,와 관련 된 사용자 활동을 검사 하 고, 다음 시스템에서 spilled 데이터를 영구적으로 제거 하는 것이 중요 합니다. 
  
## <a name="data-spillage-scenario"></a>데이터 액체 엎질렀는지 여부 시나리오

Contoso 잠재 고객 정보 보안 책임자 것입니다. 여기서 직원 모른 매우 기밀 문서와 공유 전자 메일을 통해 여러 사용자 데이터 액체 엎질렀는지 여부 상황의 알 수 있습니다. 내부 및 외부로이 문서를 받은 사람을 신속 하 게 평가 하려고 합니다. 을 식별 한 후에 사례 연구 결과 검토 하 고 다음 Office 365에서 데이터를 영구적으로 제거 하려면 다른 수 사관와 공유 하려고 합니다. 조사가 완료 되 면 모든 나중에 참조할 수에 대 한 증거 영구적으로 제거 하 고 다른 사례 세부 정보를와 보고서를 생성 하려고 합니다.
  
### <a name="scope-of-this-article"></a>이 문서의 범위

이 문서는 것이 액세스할 수 있는 또는 복구할 수 있도록 Office 365에서 메시지를 영구적으로 제거 하는 방법에 지침 목록이 제공 합니다. 메시지를 삭제 하 고 삭제 된 항목 보존 기간이 만료 될 때까지 복구할 수 있도록 하려면 [에 대 한 검색 및 Office 365 조직에서 전자 메일 메시지 삭제를](search-for-and-delete-messages-in-your-organization.md)참조 하십시오.
  
## <a name="workflow-for-managing-data-spillage-incidents"></a>데이터 액체 엎질렀는지 여부 사고 관리를 위한 워크플로

방법은 다음과 같습니다는 데이터 액체 엎질렀는지 여부 문제를 관리 하려면:

![데이터 액체 엎질렀는지 여부 문제를 관리 하기 위한 8 단계 워크플로](media/O365-eDiscoverySolutions-DataSpillage-workflow.png)
  
[(선택 사항) 1 단계: 관리 대/소문자에 액세스 하 고 규정 준수 경계를 설정할 수 있는 사람](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)<br/>
[2 단계: eDiscovery 사례 만들기](#step-2-create-an-ediscovery-case)<br/>
[Spilled 데이터에 대 한 3 단계: 검색](#step-3-search-for-the-spilled-data)<br/>
[4 단계: 검토 및 사례 연구 결과 유효성을 검사합니다](#step-4-review-and-validate-case-findings)<br/>
[5 단계: 데이터 넘어가 방법을 확인 하려면 사용 하 여 메시지 추적 로그 공유](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)<br/>
[6 단계: 사서함 준비](#step-6-prepare-the-mailboxes)<br/>
[7 단계: spilled 데이터를 영구적으로 삭제](#step-7-permanently-delete-the-spilled-data)<br/>
[8 단계: 확인, 삭제, 증명을 제공 하 고 감사](#step-8-verify-provide-a-proof-of-deletion-and-audit)<br/>

## <a name="things-to-know-before-you-start"></a>시작 하기 전에 알아야할 사항

- 보류에 사서함이 있는 경우에 삭제 된 메시지 보존 기간이 만료 되거나 보류 해제 될 때까지 복구 가능한 항목 폴더에 남아 있습니다. [6 단계](#step-6-prepare-the-mailboxes) 에서는 사서함에서 보류를 제거 하는 방법에 설명 합니다. 보류를 제거 하기 전에 레코드 관리 또는 법률 부서를 확인 합니다. 조직에 사서함에 보존 여부를 정의 하는 정책을 사용할 수 있습니다 또는 데이터 액체 엎질렀는지 여부 문제가 발생 한 설정이 우선 합니다. 
    
- 어떤 사용자 사서함을 제어 하는 데이터 액체 엎질렀는지 여부 조사 하는 사람을 검색 하 고 대/소문자를 액세스할 수 있는 사용자를 관리, 규정 준수 경계를 설정 하 고 [1 단계에서](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)에서 설명 하는 사용자 지정 역할 그룹을 만들 수 있습니다. 이 작업을 수행 하려면 조직 관리 역할 그룹의 구성원 이거나 역할 관리 역할을 할당 해야 합니다. 하는 경우 하면 또는 조직에서 관리자에서이 이미 설정 준수 경계, 1 단계를 건너뛸 수 있습니다.
    
- 사례를 만들려면, eDiscovery 관리자 역할 그룹의 구성원 이거나 사례 관리 역할에 할당 된 사용자 지정 역할 그룹의 구성원 이어야 합니다. 구성원 모르는 경우에 Office 365 관리자를 [추가 하면 eDiscovery 관리자 역할 그룹에](assign-ediscovery-permissions.md)문의 하십시오.
    
- 조직에 전달 되는 데이터를 삭제 하려면 Exchange Online PowerShell에서 [사서함 검색 DeleteContent](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox?view=exchange-ps) 명령을 사용 해야 합니다. 또한 *DeleteContent* 매개 변수를 사용 하려면 또한 해야 Exchange Online 사서함 가져오기 내보내기 역할 할당의 역할 그룹의 구성원 이어야 합니다. [관리 역할 그룹](https://technet.microsoft.com/library/jj657480%28v=exchg.150%29.aspx)의 "역할을 역할 그룹에 게 추가" 섹션을 참조 하십시오.
    
- 8 단계에서에서 eDiscovery 작업은 Office 365 감사 로그를 검색 하려면 감사 설정 해야 조직에 대 한 합니다. 지난 90 일 동안 수행 된 활동을 검색할 수 있습니다. 설정 하 고 감사를 사용 하는 방법에 대 한 자세한 내용은 8 단계에서에서 [데이터 액체 엎질렀는지 여부 조사 프로세스 감사](#auditing-the-data-spillage-investigation-process) 섹션을 참조 하십시오. 
    
## <a name="optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries"></a>(선택 사항) 1 단계: 관리 대/소문자에 액세스 하 고 규정 준수 경계를 설정할 수 있는 사람

사용자 조직 구성 방법에 따라 데이터 액체 엎질렀는지 여부 문제를 조사 하 고 규정 준수 경계를 설정 하는 데 사용 하는 eDiscovery 사례에 액세스할 수 있는 사용자를 제어 해야 합니다. 이 작업을 수행 쉬운 방법은 수 사관 Office 365 보안 및 규정 준수 센터의 기존 역할 그룹의 구성원으로 추가 하 고 다음 eDiscovery 사례의 구성원으로 역할 그룹을 추가 하는 것입니다. 기본 제공 eDiscovery 역할 그룹 및 eDiscovery 사례에 구성원을 추가 하는 방법에 대 한 정보를 참조 하십시오. [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.
  
사용자가 조직의 필요에 맞는 새 역할 그룹을 만들 수도 있습니다. 예, 그룹에 액세스 하 고 모든 데이터 액체 엎질렀는지 여부 경우에서 공동 작업을 수행 하 여 조직에서 데이터 액체 엎질렀는지 여부 수 사관 좋습니다. "데이터 액체 엎질렀는지 여부 에이전트용" 역할 그룹을 만들고, (내보내기, RMS 암호 해독, 검토, 미리 보기, 규정 준수 검색 및 사례 관리) 적절 한 역할을 할당, 역할 그룹에 데이터 액체 엎질렀는지 여부 수 사관 추가 (영문) 한 다음 추가 하 여 수행할 수 있는 작업은 데이터 액체 엎질렀는지 여부 eDiscovery 사례의 구성원으로 역할 그룹입니다. 이 작업을 수행 하는 방법에 대 한 자세한 내용은 [Office 365의 eDiscovery 조사에 대 한 준수 경계 설정](set-up-compliance-boundaries.md) 을 참조 하십시오. 
  
## <a name="step-2-create-an-ediscovery-case"></a>2 단계: eDiscovery 사례 만들기

EDiscovery 사례 사용자 데이터 액체 엎질렀는지 여부 조사를 관리 하는 효과적인 방법을 제공 합니다. 1 단계에서에서 만든 역할 그룹에 구성원을 추가, 역할 그룹의 새로운 eDiscovery 사례 구성원으로 spilled 데이터를 찾을, 공유, 대/소문자를의 상태를 추적 하는 보고서를 내보냅니다를 반복적인 검색을 수행을 추가한 다음 다시 c의 세부 정보를 참조 필요한 경우 ase 합니다. 데이터 액체 엎질렀는지 여부 사고에 사용 되는 eDiscovery 사례에 대 한 명명 규칙을 설정 하는 것이 좋습니다. 하 고 찾을 하 고 필요한 경우를 나중에 참조할 수 있도록 사례 이름 및 설명 수 만큼 정보를 제공 합니다.
  
새 사례를 만들려면 보안에서 eDiscovery를 사용할 수 &amp; 준수 센터입니다. [Office 365 보안 및 규정 준수 센터의 eDiscovery 사례](ediscovery-cases.md#step-2-create-a-new-case)에서 "새 사례 만들기"를 참조 하십시오.
  
## <a name="step-3-search-for-the-spilled-data"></a>Spilled 데이터에 대 한 3 단계: 검색

대/소문자 및 관리 되는 액세스를 만들고 나면 했으므로 spilled 데이터를 찾아 spilled 데이터를 포함 하는 사서함을 식별을 반복 해 서 검색에 대/소문자를 사용할 수 있습니다. [7 단계에서](#step-7-permanently-delete-the-spilled-data)에서 이러한 같은 메시지를 삭제 하는 전자 메일 메시지를 찾는 데 사용 하는 동일한 검색 쿼리를 사용 합니다.
  
EDiscovery 사례와 연결 된 검색 만들기 콘텐츠를 [Office 365 보안 및 규정 준수 센터의 eDiscovery 사례](ediscovery-cases.md#step-5-create-and-run-a-content-search-associated-with-a-case)에서 "만들기 및 실행 사례와 연결 된 콘텐츠 검색"를 참조 하십시오.
  
 **중요:** 검색 쿼리에 사용 하 여 키워드에 대 한 검색 하는 실제 spilled 데이터를 포함할 수 있습니다. 예를 사용 하는 경우를 사회보장 번호와 사용자를 포함 하는 문서에 대 한 검색 키워드를 검색 하는 대로 it, 액체 엎질렀는지 여부를 방지 하려면 나중에 쿼리를 삭제 해야 합니다. 8 단계에서에서 [검색 쿼리를 삭제](#deleting-the-search-query) 를 참조 하십시오. 
  
## <a name="step-4-review-and-validate-case-findings"></a>4 단계: 검토 및 사례 연구 결과 유효성을 검사합니다

콘텐츠 검색을 만든 후 검토 하 고 검색 결과 및 삭제할 수 있어야 하는 전자 메일 메시지의만 구성 자신이 확인의 유효성을 검사 해야 합니다. 콘텐츠 검색, 데이터 액체 엎질렀는지 여부를 방지 하려면 검색 결과 내보내기 (영문) 하지 않고 1, 000 전자 메일 메시지의 임의 샘플링을 미리볼 수 있습니다. 자세한 내용은에서 미리 보기 제한 하는 방법에 대 한 [콘텐츠 검색 Office 365 보안에 대 한 제한 &amp; 준수 센터](limits-for-content-search.md)합니다.
  
추가 키워드 또는 날짜 범위 또는 보낸사람/받는 사람 같은 조건을 사용 하 여 여러 검색 초기 검색 나누는 하 고 각 검색의 결과 검토할 수를 검토 하는 사서함 당 1, 000 개 이상의 사서함 또는 전자 메일 메시지에 100 개가 넘는 경우 개별적으로 합니다. [7 단계에서](#step-7-permanently-delete-the-spilled-data)에서 메시지를 삭제할 때 사용 하 여 모든 검색 쿼리를 기록해에 있는지 확인 합니다.

더불어 또는 최종 사용자는 Office 36 E5 라이선스를 할당 하는 경우에 Office 365 고급 eDiscovery를 사용 하 여 한번에 최대 10, 000 검색 결과 검토할 수 있습니다. 검토를 10, 000 개 이상의 전자 메일 메시지 인 경우에 날짜 범위에서 검색 쿼리를 나눌 수 있으며 결과 날짜별으로 정렬 하는 검색-개별적으로 각 결과 검토 수 있습니다. 고급 eDiscovery의 미리 보기 패널의 **레이블** 기능을 사용 하 여 검색 결과 태그 지정 수 있으며 레이블이 지정 하는 태그 하 여 검색 결과 필터링 수 있습니다. 보조 검토자와 공동 작업할 때 유용 합니다. 광학 문자 인식, 전자 메일 스레딩 및 예측 코딩와 같은 고급 eDiscovery의 추가 분석 도구를 사용 하 여 신속 하 게 처리 하 고 다양 한 메시지를 검토 하 수 추가 검토를 위해 태그를 지정 하 합니다. [Office 365 고급 eDiscovery에 대 한 빠른 설치](quick-setup-for-advanced-ediscovery.md)를 참조 하십시오.

넘어가 데이터가 포함 된 전자 메일 메시지를 찾았으면 외부에서 공유를 결정 하는 메시지의 받는 사람을 확인 합니다. 추가 추적 하는 메시지를 수집할 수 있습니다 발신자 정보 및 날짜 범위 [5 단계에서](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)에서 설명 하는 메시지 추적 로그를 사용할 수 있도록 합니다.

시작한 후 검색 결과 확인, 보조 검토를 위해 다른 사용자와 그 결과 공유 하려는 수 있습니다. 1 단계에서에서 대/소문자에 할당 하는 사람 eDiscovery 및 고급 eDiscovery 모두의 경우 콘텐츠를 검토 하 고 사례 연구 결과 승인할 수 있습니다. 실제 콘텐츠 내보내기 (영문) 하지 않고 보고서를 생성할 수도 있습니다. [8 단계에서](#step-8-verify-provide-a-proof-of-deletion-and-audit)에서 설명 하는 삭제 증명으로이 같은 보고서를 사용할 수도 있습니다.
  
 **보고서를 생성 통계:**
  
1. EDiscovery 사례에 **검색** 페이지로 이동 하 고 검색에 대 한 보고서를 생성 하려면을 클릭 합니다. 
    
2. 플라이 아웃 페이지에서 다음을 클릭 **더 > 보고서 내보내기**합니다.
 
      내보내기 보고서 페이지가 표시 됩니다.

    ![검색을 선택 하 고 기타를 클릭 한 다음 > 플라이 아웃 페이지에서 보고서를 내보내려면](media/O365-eDiscoverySolutions-DataSpillage-ExportReport1.png)
    
3. **모든 항목을 인식할 수 없는 형식 내용이 있는 글꼴로 포함 하 여 암호화 된 또는 다른 이유로 인덱싱된 받지** 를 선택 하 고 **생성 보고서**를 클릭 합니다.

4. EDiscovery 사례 내보내기 작업의 목록을 표시 하려면 **내보내기** 를 클릭 합니다. 방금 만든 내보내기 작업을 표시 하도록 목록을 업데이트를 **새로 고칠** 클릭 해야할 수 있습니다.

5. 내보내기 작업을 클릭 하 고 플라이 아웃 페이지에서 보고서 **다운로드** 를 클릭 합니다.
 
    ![내보내기 페이지에서 내보내기를 클릭 하 고 "보고서 다운로드"를 클릭 한 다음](media/O365-eDiscoverySolutions-DataSpillage-ExportReport2.png)

**내보내기 요약** 보고서의 결과와 검색 결과의 크기를 찾을 위치 번호를 포함 합니다. 삭제 한 후 생성 된 보고서와 비교 하 고 삭제 증명으로 제공 하려면 다음과 같이 사용할 수 있습니다. **결과** 보고서 제목, 보낸사람, 받는 사람, 전자 메일을 읽은 경우, 날짜 및 각 메시지의 크기를 포함 하 여 검색 결과의 자세한 요약을 포함 합니다. 이 보고서에서 세부 정보 중 하나를 포함 하 여 실제 spilled 데이터, 하는 경우에 조사가 완료 되 면 Results.csv 파일을 영구적으로 삭제 해야 합니다.

보고서 내보내기 (영문) 하는 방법에 대 한 자세한 내용은 [콘텐츠 검색 보고서 내보내기](export-a-content-search-report.md)를 참조 하십시오.
    
## <a name="step-5-use-message-trace-log-to-check-how-spilled-data-was-shared"></a>5 단계: 데이터 넘어가 방법을 확인 하려면 사용 하 여 메시지 추적 로그 공유

전자 메일 넘어가 데이터와 공유 하는 경우를 더 자세히 조사를 필요에 따라 발신자 정보 및 4 단계에서에서 수집 하는 날짜 범위 정보를 사용 하 여 메시지 추적 로그를 쿼리할 수 있습니다. 메시지 추적에 대 한 보존 기간 실시간 데이터에 대 한 및 기록 데이터에 대 한 일이 30 일 인지 note 합니다.
  
보안 및 규정 준수 센터의 메시지 추적을 사용 하거나 cmdlet 사용 하 여 해당 Exchange Online PowerShell 수 있습니다. 메시지 추적 반환 되는 데이터의 완전 한 정도에 전체 보증을 제공 하지 않으면 참고을 고려해 야 합니다. 메시지 추적을 사용 하는 방법에 대 한 자세한 내용은 다음을 참조 합니다. 
  
- [Office 365 보안에서 추적 메시지 &amp; 준수 센터](https://support.office.com/article/3e64f99d-ac33-4aba-91c5-9cb4ca476803.aspx)
    
- [Office 365 보안에서 새 메시지 추적 &amp; 준수 센터](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)
    
## <a name="step-6-prepare-the-mailboxes"></a>6 단계: 사서함 준비

검토 하 고 검색 결과 삭제 해야 하는 메시지에만 포함 되어있는지 확인 한 후에 **검색 사서함 DeleteContent** 명령을 실행 하면 7 단계에서에서 사용 하 여 영향을 받는 사서함의 전자 메일 주소 목록을 수집 해야 합니다. Spilled 데이터를 포함 하거나에 하나라도 해당 사서함의 경우 유지 하는 사서함에서 단일 항목 복구 사용 가능 여부에 따라 전자 메일 메시지를 영구적으로 삭제할 수 전에 사서함을 준비 해야할 수 있습니다.
  
### <a name="get-a-list-of-addresses-of-mailboxes-with-spilled-data"></a>넘어가 데이터로 사서함의 주소 목록을 가져오기

두 가지 방법으로 넘어가 데이터로 사서함의 전자 메일 주소 목록을 수집할 수 있습니다.

**옵션 1: 넘어가 데이터로 사서함의 주소 목록을 가져오려면**

1. EDiscovery 사례를 열고 **검색** 페이지로 이동 하려면 적절 한 콘텐츠 검색을 선택 합니다. 
    
2. 플라이 아웃 페이지에서 **결과 보기를**클릭 합니다.
    
3. **개별 결과** 드롭다운 목록에서에서 **검색 통계**를 클릭 합니다.
    
4. **유형** 드롭다운 목록에서에서 **위쪽 위치**를 클릭 합니다.
    
    ![검색 통계에 위쪽 위치 페이지에서 검색 결과 포함 하는 사서함의 목록을 가져오려면](media/O365-eDiscoverySolutions-DataSpillage-TopLocations.png)

    검색 결과 포함 하는 사서함의 목록이 표시 됩니다. 검색 쿼리와 일치 하는 각 사서함의 항목 수가 표시 됩니다.
    
5. 목록에서 정보를 복사 하 고 파일에 저장 하거나 CSV 파일에 정보를 다운로드 하려면 **다운로드** 를 클릭 합니다. 
    
**옵션 2: 내보내기 보고서에서 사서함 위치 가져오기**

[4 단계에서](#step-4-review-and-validate-case-findings)에서 다운로드 한 내보내기 요약 보고서를 엽니다. 보고서의 첫 번째 열에서 각 사서함의 전자 메일 주소 **위치**아래 나열 됩니다.
  
### <a name="prepare-the-mailboxes-so-you-can-delete-the-spilled-data"></a>사서함을 spilled 데이터를 삭제할 수 있도록 준비

단일 항목 복구를 사용 하는 경우 또는 사서함 보류에 배치 되 면 복구 가능한 항목 폴더에서 영구적으로 삭제 된 (비워진된) 메시지를 유지 됩니다. 따라서 전에 넘어가 데이터를 제거할 수 필요가 있습니다 기존 사서함 구성을 확인 하 고 단일 항목 복구를 사용 하지 않도록 설정 하 고 모든 보류 또는 Office 365 보존 정책을 제거 합니다. 한번에 하나 이상의 사서함을 준비 하 고 다음 다른 사서함에서 동일한 명령을 실행 하거나 만들 수 있습니다 동시에 여러 사서함을 준비 하는 PowerShell 스크립트에 유의 합니다.

- 참조 "1 단계: 사서함에 대 한 정보를 수집" [폴더에 있는 클라우드 기반 사서함의 대기 복구 가능한 항목에서 항목을 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-1-collect-information-about-the-mailbox) 하는 경우 단일 항목 복구를 사용할 수는 경우 사서함에 배치 하거나 유지 하거나에 할당 된 확인 하는 방법에 대 한 지침은에 보존 정책입니다. 
    
- 참조 "2 단계: 사서함 준비"에 대 한 단일 항목 복구를 사용 하지 않도록 설정 하는 방법에 대 한 자세한 내용 [은 폴더에 있는 클라우드 기반 사서함의 대기 복구 가능한 항목에서 항목을 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-2-prepare-the-mailbox) 합니다. 
    
- 참조 "3 단계: 사서함에서 모든 보류를 제거"에 대 한 사서함에서 보류 또는 보존 정책을 제거 하는 방법에 대 한 자세한 내용 [은 폴더에 있는 클라우드 기반 사서함의 대기 복구 가능한 항목에서 항목을 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-3-remove-all-holds-from-the-mailbox) 합니다. 

- 참조 "4 단계: 사서함에서 유지 하는 지연 제거"에 대 한 모든 유형의 보류에서 제거 된 후 사서함에 배치 되는 지연 보류를 제거 하는 방법에 대 한 자세한 내용 [은 폴더에 있는 클라우드 기반 사서함의 대기 복구 가능한 항목에서 항목을 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-4-remove-the-delay-hold-from-the-mailbox) 합니다.
    
 **중요:** 보류 또는 보존 정책을 제거 하기 전에 레코드 관리 또는 법률 부서를 확인 합니다. 조직에서 사서함에 보존 여부를 정의 하는 정책을 이미 또는 데이터 액체 엎질렀는지 여부 문제가 발생 한 설정이 우선 합니다. 
  
Spilled 데이터 영구적으로 삭제 되었는지 확인 한 후 이전 구성에 사서함을 되돌리려면 확인 해야 합니다. [7 단계에서](#step-7-permanently-delete-the-spilled-data)에서 세부 정보를 참조 하십시오.

## <a name="step-7-permanently-delete-the-spilled-data"></a>7 단계: spilled 데이터를 영구적으로 삭제

수집 하 고 6 단계 및 검색 쿼리 생성 되어 spilled 데이터를 포함 하는 전자 메일 메시지를 찾으려면 3 단계에서에서 구체화를 준비 하는 사서함 위치를 사용 하 여 지금 영구적으로 삭제할 수 spilled 데이터. 앞에서 설명한 것 처럼 사서함 가져오기 내보내기 역할 Exchange Online에 할당한 다음 절차를 사용 하 여 메시지를 삭제 해야 합니다.
  
1. [Exchange Online PowerShell에 연결합니다](https://go.microsoft.com/fwlink/?linkid=396554).
    
2. 다음 명령을 실행합니다.
    
    ```
    Search-Mailbox -Identity <mailbox identity> -SearchDumpster -DeleteContent $true -SearchQuery <search query>
    ```
  
3. Identity 매개 변수는;에 대 한 값을 대체 하 여 spilled 데이터를 포함 하는 각 사서함에 대 한 이전 명령을 다시 실행 예를 들어:

    ```
    Search-Mailbox -Identity sarad@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

    ```
    Search-Mailbox -Identity janets@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

   ```
   Search-Mailbox -Identity pilarp@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
   ```
  
앞서 설명한 것 처럼 [powershell 스크립트](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6) 를 만들 하 고 각 사서함에 spilled 데이터를 삭제 하는 스크립트 있도록 사서함의 목록에 대해 실행 합니다.
  
## <a name="step-8-verify-provide-a-proof-of-deletion-and-audit"></a>8 단계: 확인, 삭제, 증명을 제공 하 고 감사

데이터 액체 엎질렀는지 여부 문제를 관리 하 여 워크플로에서 마지막 단계는 eDiscovery 사례에 64로 이동한 다음 사항을 확인합니다 하려면 해당 데이터 없음 결과 월드 라는 삭제 하는데 사용 된 동일한 검색 쿼리를 다시 실행 하 여 spilled 데이터 된 사서함에서 영구적으로 제거 확인 e 반환 됩니다. Spilled 데이터 파일이 영구적으로 제거를 확인 한 후 보고서를 내보낼 수 있으며 삭제 증명으로 원래 보고서) (함께 포함할 수 있습니다. 그런 다음 [닫기를 대/소문자가](ediscovery-cases.md#optional-step-9-close-a-case)참조 하는 경우 해당 나중에 다시 열 수 있도록 하는 수 있습니다. 사서함도 되돌릴 수는 또한 이전 상태로 spilled 데이터를 확인 하 고 데이터 액체 엎질렀는지 여부 인시던트를 관리할 때 수행할 작업의 레코드를 감사에 대 한 검색에 사용 되는 검색 쿼리를 삭제 합니다. 
  
### <a name="reverting-the-mailboxes-to-their-previous-state"></a>사서함을 이전 상태로 되돌리는

Spilled 데이터를 삭제 하기 직전에 사서함을 준비 하려면 6 단계에서에서 모든 사서함 구성을 변경 하는 경우에 이전 상태로 되돌리려면 해야 합니다. 참조 "6 단계: 사서함을 이전 상태로 되돌리기"에서 [복구 가능한 항목 폴더에 있는 클라우드 기반 사서함의 보류에서 항목을 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-6-revert-the-mailbox-to-its-previous-state)합니다.
  
### <a name="deleting-the-search-query"></a>검색 쿼리를 삭제합니다.

만들고 3 단계에서에서 사용 하는 검색 쿼리에서 키워드를 포함 하는 실제 spilled 데이터의 전부 또는 일부를 하는 경우에 추가 방지 하기 위해 데이터 액체 엎질렀는지 여부 검색 쿼리를 삭제 해야 합니다.
  
1. 보안 및 규정 준수 센터, eDiscovery 사례, 열고 **검색** 페이지로 이동 적절 한 콘텐츠 검색을 선택 합니다.
    
2. 플라이 아웃 페이지에서 **삭제**를 클릭 합니다.

    ![검색을 선택 하 고 플라이 아웃 페이지에서 삭제를 클릭 한 다음](media/O365-eDiscoverySolutions-DataSpillage-DeleteSearch.png)
    
### <a name="auditing-the-data-spillage-investigation-process"></a>감사 데이터 액체 엎질렀는지 여부 조사 프로세스

조사 하는 동안 수행 된 eDiscovery 활동에 대 한 Office 365 감사 로그를 검색할 수 있습니다. 또한 spilled 데이터를 삭제 하는 **사서함 검색 DeleteContent** 명령을 실행 했을 때 만들어진 감사 레코드를 반환 하는 감사 로그를 검색할 수 있습니다. 자세한 내용은 다음을 참조 합니다.

- [Office 365 보안 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)

- [Office 365 감사 로그에서 eDiscovery 활동에 대 한 검색](search-for-ediscovery-activities-in-the-audit-log.md)

- Exchange Online의 cmdlet을 실행 하려면 관련 된 감사 레코드를 검색 하는 방법에 대 한 지침은 [Office 365 보안 및 규정 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#audited-activities) 에 "활동-Exchange 관리자 감사 로그 감사" 섹션을 참조 하십시오.
  

