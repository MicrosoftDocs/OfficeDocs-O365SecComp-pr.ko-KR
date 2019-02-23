---
title: eDiscovery 솔루션 계열 데이터 유출 시나리오-검색 및 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d945f7dd-f62f-4ca7-b3e7-469824cfd493
description: Office 365 eDiscovery 및 검색 도구를 사용 하 여 조직의 데이터 유출 인시던트를 관리 하 고 대응 합니다.
ms.openlocfilehash: 0da49dfbe8104d89a1abf4a14adce51ec0ef25f1
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219428"
---
# <a name="ediscovery-solution-series-data-spillage-scenario---search-and-purge"></a>eDiscovery 솔루션 시리즈: 데이터 유출 시나리오-검색 및 삭제

 **데이터 유출 무엇 이며 주의 해야 하는 이유는 무엇 인가요?** 데이터 유출 기밀 문서가 신뢰할 수 없는 환경으로 릴리스될 때 발생 합니다. 데이터 유출 인시던트가 검색 되는 경우에는 유출의 크기와 위치를 신속 하 게 평가 하 고 그에 대 한 사용자 작업을 조사한 다음 시스템에서 분산 데이터를 영구적으로 제거 하는 것이 중요 합니다. 
  
## <a name="data-spillage-scenario"></a>데이터 유출 시나리오

Contoso의 잠재 고객 정보 보안 담당자입니다. 직원 들이 전자 메일을 통해 여러 사용자와 고도로 기밀 문서를 공유 하는 데이터 유출 상황에 대 한 정보를 제공 합니다. 내부적으로 또는 외부적으로이 문서를 받은 사람을 빠르게 평가 하려는 경우 확인 한 후 사례 결과를 다른 investigators와 공유 하 고 Office 365에서 데이터를 영구적으로 제거 하려고 합니다. 조사가 완료 된 후에는 나중에 참조할 수 있도록 영구 제거 증거 및 기타 사례 정보가 포함 된 보고서를 생성 하려고 합니다.
  
### <a name="scope-of-this-article"></a>이 문서의 범위

이 문서에서는 Office 365에서 메시지를 영구적으로 제거 하 여 액세스 하거나 복구할 수 없도록 하는 방법에 대 한 지침 목록을 제공 합니다. 삭제 된 항목 보존 기간이 만료 될 때까지 메시지를 삭제 하 고 복구할 수 있도록 하려면 [Office 365 조 직에서 전자 메일 메시지 검색 및 삭제](search-for-and-delete-messages-in-your-organization.md)를 참조 하세요.
  
## <a name="workflow-for-managing-data-spillage-incidents"></a>데이터 유출 인시던트를 관리 하기 위한 워크플로

데이터 유출 인시던트를 관리 하는 방법은 다음과 같습니다.

![데이터 유출 인시던트를 관리 하기 위한 8 단계 워크플로](media/O365-eDiscoverySolutions-DataSpillage-workflow.png)
  
[반드시 1 단계: 사례에 액세스 하 고 준수 경계를 설정할 수 있는 사용자 관리](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)<br/>
[2 단계: eDiscovery 사례 만들기](#step-2-create-an-ediscovery-case)<br/>
[3 단계: 분산 된 데이터 검색](#step-3-search-for-the-spilled-data)<br/>
[4 단계: 사례 결과 검토 및 유효성 검사](#step-4-review-and-validate-case-findings)<br/>
[5 단계: 메시지 추적 로그를 사용 하 여 데이터의 공유 방식 확인](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)<br/>
[6 단계: 사서함 준비](#step-6-prepare-the-mailboxes)<br/>
[7 단계: 데이터를 영구적으로 삭제](#step-7-permanently-delete-the-spilled-data)<br/>
[8 단계: 확인, 삭제 증거 제공 및 감사](#step-8-verify-provide-a-proof-of-deletion-and-audit)<br/>

## <a name="things-to-know-before-you-start"></a>시작 하기 전에 알아야 할 사항

- 사서함이 대기 중일 때 삭제 된 메시지는 보존 기간이 만료 되거나 보류가 릴리스될 때까지 복구 가능한 항목 폴더에 남아 있습니다. [6 단계](#step-6-prepare-the-mailboxes) 사서함에서 보존을 제거 하는 방법에 대해 설명 합니다. 보류를 제거 하기 전에 레코드 관리 또는 법률 부서에 문의 하세요. 조직에 보류 중인 사서함 또는 데이터 유출 인시던트가 우선적으로 적용 되는지 여부를 정의 하는 정책이 있을 수 있습니다. 
    
- 데이터 유출 investigator에서 액세스할 수 있는 사람을 검색 하 고 관리할 수 있는 사용자 사서함을 제어 하려면 준수 경계를 설정 하 고 [1 단계](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)에서 설명 하는 사용자 지정 역할 그룹을 만들 수 있습니다. 이 작업을 수행 하려면 조직 관리 역할 그룹의 구성원 이거나 역할 관리 역할을 할당 받아야 합니다. 조직의 관리자가 이미 준수 경계를 설정한 경우에는 1 단계를 생략할 수 있습니다.
    
- 사례를 만들려면 eDiscovery 관리자 역할 그룹의 구성원 이거나 사례 관리 역할이 할당 된 사용자 지정 역할 그룹의 구성원 이어야 합니다. 구성원이 아닌 경우 Office 365 관리자에 게 [eDiscovery 관리자 역할 그룹에 추가](assign-ediscovery-permissions.md)해 달라고 요청 하세요.
    
- 조직에 분산 된 데이터를 삭제 하려면 Exchange Online PowerShell에서 [검색-DeleteContent](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox?view=exchange-ps) 명령을 사용 해야 합니다. 또한 *DeleteContent* 매개 변수를 사용 하려면 사서함 가져오기 내보내기 역할이 할당 된 Exchange Online의 역할 그룹 구성원 이어야 합니다. [역할 그룹 관리](https://technet.microsoft.com/library/jj657480%28v=exchg.150%29.aspx)의 "역할 그룹에 역할 추가" 섹션을 참조 하세요.
    
- 8 단계에서 Office 365 감사 로그 eDiscovery 활동을 검색 하려면 조직에 대 한 감사가 설정 되어 있어야 합니다. 지난 90 일 이내에 수행 된 활동을 검색할 수 있습니다. 감사를 사용 하도록 설정 하 고 사용 하는 방법에 대 한 자세한 내용은 8 단계에서 [데이터 유출 조사 프로세스 감사](#auditing-the-data-spillage-investigation-process) 섹션을 참조 하십시오. 
    
## <a name="optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries"></a>반드시 1 단계: 사례에 액세스 하 고 준수 경계를 설정할 수 있는 사용자 관리

조직의 관행에 따라 데이터 유출 인시던트를 조사 하 고 준수 경계를 설정 하는 데 사용 되는 eDiscovery 사례에 액세스할 수 있는 사용자를 제어 해야 합니다. 이 작업을 수행 하는 가장 쉬운 방법은 investigators를 Office 365 Security & 준수 센터에서 기존 역할 그룹의 구성원으로 추가 하 고이 역할 그룹을 eDiscovery 사례의 구성원으로 추가 하는 것입니다. 기본 제공 ediscovery 역할 그룹 및 eDiscovery 사례에 구성원을 추가 하는 방법에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 ediscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.
  
조직 요구 사항에 맞게 새 역할 그룹을 만들 수도 있습니다. 예를 들어 조직에서 데이터 유출 investigators 그룹을 사용 하 여 모든 데이터 유출 사례에 액세스 하 고 공동 작업을 수행할 수 있습니다. 이 작업을 수행 하려면 "data 유출 Investigator" 역할 그룹을 만들고, 해당 역할 (내보내기, RMS 암호 해독, 검토, 미리 보기, 준수 검색 및 사례 관리)을 할당 하 고, 데이터 유출 investigators를 역할 그룹에 추가한 다음 데이터 유출 eDiscovery 사례에 대 한 구성원으로 서의 역할 그룹 이 작업을 수행 하는 방법에 대 한 자세한 내용은 [Office 365에서 eDiscovery 조사에 대 한 준수 경계 설정을](set-up-compliance-boundaries.md) 참조 하십시오. 
  
## <a name="step-2-create-an-ediscovery-case"></a>2 단계: eDiscovery 사례 만들기

eDiscovery 사례는 데이터 유출 조사를 효과적으로 관리 하는 방법을 제공 합니다. 1 단계에서 만든 역할 그룹에 구성원을 추가 하 고, 역할 그룹을 새로 eDiscovery 사례의 구성원으로 추가 하 고, 반복 검색을 수행 하 여 분산 된 데이터를 찾고, 보고서를 공유로 내보내고, 사례 상태를 추적 하 고, 대/소문자를 추적할 수 있습니다. ase 필요한 경우 데이터 유출 인시던트에 사용 되는 eDiscovery 사례에 대 한 명명 규칙을 설정 하 고, 사례 이름 및 설명에 최대한 많은 정보를 제공 하 여 필요한 경우이를 찾고 참조할 수 있습니다.
  
새 사례를 만들려면 보안 &amp; 및 준수 센터에서 eDiscovery를 사용할 수 있습니다. [Office 365 Security & 준수 센터의 eDiscovery 사례](ediscovery-cases.md#step-2-create-a-new-case)에서 "새 사례 만들기"를 참조 하세요.
  
## <a name="step-3-search-for-the-spilled-data"></a>3 단계: 분산 된 데이터 검색

사례 및 관리 되는 액세스 권한을 만들었으므로 이제 사례를 사용 하 여 데이터를 반복적으로 검색 하 고 분산 된 데이터를 포함 하는 사서함을 식별할 수 있습니다. 전자 메일 메시지를 검색 하는 데 사용한 것과 동일한 검색 쿼리를 사용 하 여 [7 단계](#step-7-permanently-delete-the-spilled-data)에서 같은 메시지를 삭제 합니다.
  
ediscovery 사례와 연결 된 콘텐츠 검색을 만들려면 [Office 365 Security & 준수 센터의 eDiscovery 사례](ediscovery-cases.md#step-5-create-and-run-a-content-search-associated-with-a-case)에서 "사례와 연결 된 콘텐츠 검색 만들기 및 실행"을 참조 하십시오.
  
 **중요:** 검색 쿼리에 사용 하는 키워드에는 검색 중인 실제 데이터 데이터가 포함 될 수 있습니다. 예를 들어 주민 등록 번호를 포함 하는 문서를 검색 하는 경우이를 검색 키워드로 사용 하려면 나중에 쿼리를 삭제 하 여 더 이상 유출을 방지 해야 합니다. 8 단계에서 [검색 쿼리 삭제](#deleting-the-search-query) 를 참조 하세요. 
  
## <a name="step-4-review-and-validate-case-findings"></a>4 단계: 사례 결과 검토 및 유효성 검사

콘텐츠 검색을 만든 후에는 검색 결과를 검토 하 고 유효성을 검사 하 여 삭제 해야 하는 전자 메일 메시지에 대해서만 구성 되는지 확인 해야 합니다. 콘텐츠 검색에서는 검색 결과를 내보내지 않고 1000 전자 메일 메시지의 임의 샘플링을 미리 볼 수 있으므로 더 이상 데이터 유출 되지 않습니다. [Office 365 보안 &amp; 및 준수 센터의 콘텐츠 검색 제한](limits-for-content-search.md)에서 미리 보기 제한 사항에 대 한 자세한 내용을 확인할 수 있습니다.
  
사서함이 1000 개 보다 많은 사서함이 있거나 검토 하기 위해 전자 메일 메시지 수가 100 개 보다 많은 경우에는 날짜 범위 또는 보낸 사람/받는 사람과 같은 추가 키워드나 조건을 사용 하 여 초기 검색을 여러 검색으로 나누고 각 검색의 결과를 검토할 수 있습니다. 개별적으로. [7 단계](#step-7-permanently-delete-the-spilled-data)에서 메시지를 삭제할 때 사용할 모든 검색 쿼리를 기록해 두어야 합니다.

custodian 또는 최종 사용자에 게 office 36 E5 라이선스가 할당 된 경우 office 365 Advanced eDiscovery를 사용 하 여 한 번에 최대 1만의 검색 결과를 확인할 수 있습니다. 검토 해야 하는 전자 메일 메시지가 1만 개 보다 많으면 검색 쿼리를 날짜별로 나누고 검색 결과가 날짜별로 정렬 되어 개별적으로 각 결과를 검토할 수 있습니다. 고급 eDiscovery에서는 미리 보기 패널에서 **레이블** 표시 기능을 사용 하 여 검색 결과에 태그를 지정 하 고, 해당 태그에 따라 검색 결과를 필터링 할 수 있습니다. 이 기능은 보조 검토자와 공동 작업할 때 유용 합니다. 고급 eDiscovery에서 광학 인식, 전자 메일 스레딩 및 예측 코딩 같은 추가 분석 도구를 사용 하 여 수천 개의 메시지를 빠르게 처리 및 검토 하 고 추가 검토를 위해 태그를 지정할 수 있습니다. [Office 365 Advanced eDiscovery에 대 한 빠른 설치를](quick-setup-for-advanced-ediscovery.md)참조 하세요.

데이터를 포함 하는 전자 메일 메시지를 찾을 때 메시지를 받는 사람에 게 외부 공유 여부를 확인 합니다. 메시지를 추가로 추적 하기 위해 보낸 사람 정보 및 날짜 범위를 수집 하 여 [5 단계](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)에서 설명 하는 메시지 추적 로그를 사용할 수 있습니다.

검색 결과를 확인 하 고 나면 보조 검토를 위해 다른 사람들과 의견을 공유할 수 있습니다. 1 단계에서 사례에 할당 한 사용자는 eDiscovery 및 Advanced eDiscovery에서 사례 콘텐츠를 검토 하 고 사례 결과를 승인할 수 있습니다. 실제 콘텐츠를 내보내지 않고 보고서를 생성할 수도 있습니다. 또한 [8 단계](#step-8-verify-provide-a-proof-of-deletion-and-audit)에서 설명 하는이 보고서를 삭제 했을 때와 동일 하 게 사용할 수 있습니다.
  
 **통계 보고서를 생성 하려면:**
  
1. eDiscovery 사례의 **검색** 페이지로 이동한 후 보고서를 생성할 검색을 클릭 합니다. 
    
2. 플라이 아웃 페이지에서 **기타 > 내보내기 보고서**를 클릭 합니다.
 
      보고서 내보내기 페이지가 표시 됩니다.

    ![검색을 선택 하 고 플라이 아웃 페이지에서 자세한 > 내보내기 보고서를 클릭 합니다.](media/O365-eDiscoverySolutions-DataSpillage-ExportReport1.png)
    
3. **형식을 인식할 수 없거나 암호화 되었거나 다른 이유로 인덱싱되지 않은 항목을 포함 하 여 모두** 선택 하 고 **보고서 생성**을 클릭 합니다.

4. eDiscovery 사례에서 **내보내기를** 클릭 하 여 내보내기 작업 목록을 표시 합니다. **새로 고침** 을 클릭 하 여 방금 만든 내보내기 작업을 표시 하도록 목록을 업데이트 해야 할 수 있습니다.

5. 내보내기 작업을 클릭 한 다음 플라이 아웃 페이지에서 보고서 **다운로드** 를 클릭 합니다.
 
    ![내보내기 페이지에서 내보내기를 클릭 하 고 "보고서 다운로드"를 클릭 합니다.](media/O365-eDiscoverySolutions-DataSpillage-ExportReport2.png)

**내보내기 요약** 보고서에는 결과를 포함 하는 위치 수와 검색 결과 크기가 포함 됩니다. 이를 사용 하 여 삭제 후 생성 되는 보고서와 비교 하 고 삭제 증명으로 제공 합니다. **결과** 보고서에는 제목, 보낸 사람, 받는 사람, 전자 메일을 읽은 경우 각 메시지의 날짜 및 크기를 포함 하 여 검색 결과에 대 한 보다 자세한 요약이 포함 되어 있습니다. 이 보고서의 세부 정보가 해당 실제 데이터를 포함 하는 경우 조사가 완료 되 면 결과 .csv 파일을 영구적으로 삭제 해야 합니다.

보고서를 내보내는 방법에 대 한 자세한 내용은 [Export a Content Search report](export-a-content-search-report.md)를 참조 하십시오.
    
## <a name="step-5-use-message-trace-log-to-check-how-spilled-data-was-shared"></a>5 단계: 메시지 추적 로그를 사용 하 여 데이터의 공유 방식 확인

데이터를 전송 하는 전자 메일이 공유 되었는지 자세히 확인 하려면 필요에 따라 보낸 사람 정보 및 4 단계에서 수집한 날짜 범위 정보를 사용 하 여 메시지 추적 로그를 쿼리할 수 있습니다. 메시지 추적의 보존 기간은 실시간 데이터의 경우 30 일 이며, 기록 데이터의 경우 90 일입니다.
  
보안 & 준수 센터에서 메시지 추적을 사용 하거나 Exchange Online PowerShell의 해당 cmdlet을 사용할 수 있습니다. 메시지 추적은 반환 되는 데이터의 완성도를 완벽 하 게 보장 하지 않는다는 점에 유의 해야 합니다. 메시지 추적을 사용 하는 방법에 대 한 자세한 내용은 다음을 참조 하십시오. 
  
- [Office 365 보안 &amp; 및 준수 센터의 메시지 추적](https://support.office.com/article/3e64f99d-ac33-4aba-91c5-9cb4ca476803.aspx)
    
- [Office 365 보안 &amp; 및 준수 센터의 새 메시지 추적](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)
    
## <a name="step-6-prepare-the-mailboxes"></a>6 단계: 사서함 준비

검색 결과에 삭제 해야 하는 메시지만 포함 되어 있는지 검토 하 고 확인 한 후에는 **검색 사서함-DeleteContent** 명령을 실행할 때 7 단계에서 사용할 영향을 받는 사서함의 전자 메일 주소 목록을 수집 해야 합니다. 또한 분산 된 데이터를 포함 하는 사서함에 대해 단일 항목 복구를 사용할 수 있는지 또는 해당 사서함이 보류 상태 인지에 따라 전자 메일 메시지를 영구적으로 삭제 하기 전에 사서함을 준비 해야 할 수 있습니다.
  
### <a name="get-a-list-of-addresses-of-mailboxes-with-spilled-data"></a>데이터가 분산 된 사서함의 주소 목록 가져오기

두 가지 방법으로 사서함의 전자 메일 주소 목록을 분산 된 데이터로 수집할 수 있습니다.

**옵션 1: 데이터가 분산 된 사서함의 주소 목록 가져오기**

1. eDiscovery 사례를 열고 **검색** 페이지로 이동한 후 적절 한 콘텐츠 검색을 선택 합니다. 
    
2. 플라이 아웃 페이지에서 **결과 보기**를 클릭 합니다.
    
3. **개별 결과** 드롭다운 목록에서 **검색 통계**를 클릭 합니다.
    
4. **형식** 드롭다운 목록에서 **상위 위치**를 클릭 합니다.
    
    ![검색 통계의 최상위 위치 페이지에서 검색 결과를 포함 하는 사서함 목록 가져오기](media/O365-eDiscoverySolutions-DataSpillage-TopLocations.png)

    검색 결과를 포함 하는 사서함 목록이 표시 됩니다. 검색 쿼리와 일치 하는 각 사서함의 항목 수도 표시 됩니다.
    
5. 목록의 정보를 복사 하 여 파일에 저장 하거나 **다운로드** 를 클릭 하 여 CSV 파일에 정보를 다운로드 합니다. 
    
**옵션 2: 내보내기 보고서에서 사서함 위치 가져오기**

[4 단계](#step-4-review-and-validate-case-findings)에서 다운로드 한 내보내기 요약 보고서를 엽니다. 보고서의 첫 번째 열에 각 사서함의 전자 메일 주소가 **위치**아래에 나열 됩니다.
  
### <a name="prepare-the-mailboxes-so-you-can-delete-the-spilled-data"></a>분산 데이터를 삭제할 수 있도록 사서함 준비

단일 항목 복구를 사용 하거나 사서함을 보류 중인 경우 영구 삭제 된 메시지를 복구 가능한 항목 폴더에 보존 됩니다. 따라서 분산 된 데이터를 제거 하려면 기존 사서함 구성을 확인 하 고 단일 항목 복구를 사용 하지 않도록 설정 하 고 보류 또는 Office 365 보존 정책을 제거 해야 합니다. 한 번에 하나의 사서함을 준비한 다음 서로 다른 사서함에서 동일한 명령을 실행 하거나 PowerShell 스크립트를 만들어 여러 사서함을 동시에 준비할 수 있다는 점에 유의 하세요.

- 단일 항목 복구를 사용할 수 있는지 확인 하는 방법에 대 한 지침을 보려면 [보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에 있는 항목 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-1-collect-information-about-the-mailbox) 의 "1 단계: 사서함에 대 한 정보 수집"을 참조 하세요. 보존 정책 
    
- 단일 항목 복구를 사용 하지 않도록 설정 하는 방법에 대 한 지침은 [보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-2-prepare-the-mailbox) 의 "2 단계: 사서함 준비"를 참조 하세요. 
    
- 사서함에서 보류 또는 보존 정책을 제거 하는 방법에 대 한 자세한 내용은 [보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에 있는 항목 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-3-remove-all-holds-from-the-mailbox) 의 "3 단계: 사서함에서 모든 보류 제거"를 참조 하세요. 

- 모든 유형의 보존을 제거한 후 사서함에 적용 되는 지연 대기를 제거 하는 방법에 대 한 지침은 "4 단계: [보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더의 항목 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-4-remove-the-delay-hold-from-the-mailbox) "를 참조 하세요.
    
 **중요:** 보류 또는 보존 정책을 제거 하기 전에 레코드 관리 또는 법률 부서에 문의 하세요. 조직에 보류 중인 사서함 또는 데이터 유출 인시던트가 우선 하는지 여부를 정의 하는 정책이 있을 수 있습니다. 
  
분산 된 데이터가 영구적으로 삭제 되었는지 확인 한 후 사서함을 이전 구성으로 되돌려야 합니다. [7 단계](#step-7-permanently-delete-the-spilled-data)에 나와 있는 세부 정보를 참조 하세요.

## <a name="step-7-permanently-delete-the-spilled-data"></a>7 단계: 데이터를 영구적으로 삭제

전송 된 데이터를 포함 하는 전자 메일을 찾기 위해 3 단계에서 작성 하 고 준비한 검색 쿼리와 6 단계에서 수집한 사서함 위치를 사용 하 여 데이터를 영구적으로 삭제할 수 있습니다. 앞에서 설명한 것 처럼 다음 절차를 사용 하 여 메시지를 삭제 하려면 Exchange Online의 사서함 가져오기 내보내기 역할을 할당 받아야 합니다.
  
1. [Exchange Online PowerShell에 연결합니다](https://go.microsoft.com/fwlink/?linkid=396554).
    
2. 다음 명령을 실행합니다.
    
    ```
    Search-Mailbox -Identity <mailbox identity> -SearchDumpster -DeleteContent $true -SearchQuery <search query>
    ```
  
3. Identity 매개 변수의 값을 바꿔서, 분산 된 데이터를 포함 하는 각 사서함에 대해 이전 명령을 다시 실행 합니다. 예를 들어:

    ```
    Search-Mailbox -Identity sarad@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

    ```
    Search-Mailbox -Identity janets@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

   ```
   Search-Mailbox -Identity pilarp@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
   ```
  
앞에서 설명한 것 처럼 [powershell 스크립트](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6) 를 만들어 사서함 목록에 대해 실행 하 여 스크립트가 각 사서함에서 분산 데이터를 삭제할 수도 있습니다.
  
## <a name="step-8-verify-provide-a-proof-of-deletion-and-audit"></a>8 단계: 확인, 삭제 증거 제공 및 감사

데이터 유출 인시던트를 관리 하기 위한 워크플로의 마지막 단계는, eDiscovery 사례로 이동 하 여 해당 데이터를 삭제 하는 데 사용 된 것과 동일한 검색 쿼리를 다시 실행 하 고 결과 ar가 없음을 확인 하 여 해당 데이터를 사서함에서 영구적으로 제거 했는지 확인 하는 것입니다. e 반환 데이터를 영구적으로 제거 했는지 확인 한 후에는 보고서를 내보낸 후 원본 보고서와 함께 삭제 증명으로 포함할 수 있습니다. 그런 다음 나중에 참조 하는 경우이를 다시 열 수 있도록 하는 [사례를 닫을](ediscovery-cases.md#optional-step-9-close-a-case)수 있습니다. 또한 사서함을 이전 상태로 되돌리고, 분산 된 데이터를 찾는 데 사용 되는 검색 쿼리를 삭제 하 고, 데이터 유출 인시던트를 관리할 때 수행 되는 작업의 감사 기록을 검색할 수도 있습니다. 
  
### <a name="reverting-the-mailboxes-to-their-previous-state"></a>사서함을 이전 상태로 되돌리기

6 단계의 사서함 구성을 변경 하 여 커넥터 된 데이터가 삭제 되기 전에 사서함을 준비한 경우에는 이전 상태로 되돌려야 합니다. [보류 중인 클라우드 기반 사서함의 복구할 수 있는 항목 폴더에 있는 항목을 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-6-revert-the-mailbox-to-its-previous-state)하려면 "6 단계: 사서함을 이전 상태로 되돌리기"를 참조 하세요.
  
### <a name="deleting-the-search-query"></a>검색 쿼리 삭제

3 단계에서 만들어 사용한 검색 쿼리의 키워드에 실제 데이터를 모두 포함 하는 경우에는 검색 쿼리를 삭제 하 여 더 이상 데이터 유출 방지 해야 합니다.
  
1. 보안 & 준수 센터에서 eDiscovery 사례를 열고 **검색** 페이지로 이동한 다음 적절 한 콘텐츠 검색을 선택 합니다.
    
2. 플라이 아웃 페이지에서 **삭제**를 클릭 합니다.

    ![검색을 선택 하 고 플라이 아웃 페이지에서 삭제를 클릭 합니다.](media/O365-eDiscoverySolutions-DataSpillage-DeleteSearch.png)
    
### <a name="auditing-the-data-spillage-investigation-process"></a>데이터 유출 조사 프로세스 감사

조사 중에 수행 된 eDiscovery 활동에 대 한 Office 365 감사 로그를 검색할 수 있습니다. 또한 **검색 사서함-DeleteContent** 명령을 실행 하 여 데이터를 삭제할 때 만든 감사 레코드를 반환 하도록 감사 로그를 검색할 수 있습니다. 자세한 내용은 다음 항목을 참조 하십시오.

- [Office 365 보안 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)

- [Office 365 감사 로그에서 eDiscovery 활동 검색](search-for-ediscovery-activities-in-the-audit-log.md)

- Exchange Online에서 실행 중인 cmdlet과 관련 된 감사 레코드를 검색 하는 방법에 대 한 지침은 [Office 365 보안 & 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#audited-activities) 의 "감사 된 활동-Exchange 관리자 감사 로그" 섹션을 참조 하십시오.
  

