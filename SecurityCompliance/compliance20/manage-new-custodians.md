---
title: Advanced eDiscovery 사례에서 custodians 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d9806ecbc23f46ee2d39f8d7e6be07af0d6a83e8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151620"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-case"></a>Advanced eDiscovery 사례에서 custodians 관리

Advanced eDiscovery의 Custodians 탭에는 사례에 추가 된 모든 Custodians의 목록이 포함 되어 있습니다. Custodians를 사례에 추가 하 고 나면 각 custodian에 대 한 세부 정보는 Azure Active Directory에서 자동으로 수집 되며 고급 eDiscovery로 볼 수 있습니다.

![Custodians 관리](../media/CustodianDetails.PNG)

## <a name="view-custodian-details"></a>Custodian 세부 정보 보기

Custodian에 대 한 세부 정보를 보려면 **Custodians** 탭의 목록에서 custodian을 클릭 합니다. 플라이 아웃 페이지가 표시 되 고 custodian에 대 한 다음 정보가 포함 됩니다.

- 연락처 정보

  - **표시 이름** -custodian 주소록에 표시 되는 이름입니다. 일반적으로 custodian 이름, 중간 이니셜 및 성의 조합입니다.
  
   - **Mail/SMTP** -custodian의 기본 SMTP 주소 (예: brianj@contoso.onmicrosoft.com)입니다. Custodian의 UPN (사용자 계정 이름)도 나열 됩니다.

  - **Title** -custodian의 직함입니다.

  - **부서** -custodian가 작동 하는 부서의 이름입니다.

  - **Manager** -custodian의 관리자입니다. 지정 된 관리자가이 custodian에 대 한 에스컬레이션 통신을 수신 합니다.
  
- 위치 정보

  - **구/** 군/시-custodian가 있는 구/군/시입니다.

  - **State** -custodian 주소의 시/도입니다.

  - **국가/지역** -custodian가 있는 국가/지역입니다.

  - **Office** -custodian의 비즈니스 장소에 있는 사무실 위치입니다.

- 사례 정보

  - **보류 상태** -custodian를 보류 했는지 여부를 나타냅니다. 

  - **통신 상태**: custodian에 보류 알림이 발급 되었는지 여부를 나타냅니다. Custodian에 알림이 발급 된 경우이 속성의 값이 **게시**됩니다. Custodian에 알림이 발급 되지 않은 경우 상태가 **게시 취소**됩니다. 

  - **Status** -사례 내에 있는 custodian의 상태입니다. 상태가 **활성** 이면 custodian가 사례에 포함 됨을 나타냅니다. Custodian가 사례에서 해제 되 면 상태가 ' **릴리즈됨**'으로 변경 됩니다. 

- 데이터 원본 및 인덱싱 정보

    - **데이터 원본** -custodian와 연결 된 데이터 원본 수와 유형 (사서함, 사이트 및 팀)을 표시 하며 사례에 포함 됩니다.

    - **인덱스 업데이트 시간** -고급 인덱싱 작업이 마지막으로 트리거된 시간 및 날짜를 나타냅니다. 이 속성은 고급 인덱싱 프로세스가 현재 진행 되 고 있는 경우에도 표시 됩니다.


## <a name="edit-a-custodian"></a>Custodian 편집

사례가 진행 됨에 따라 특정 custodian & 관련 된 추가 데이터 원본이 있을 수 있습니다. 다른 시나리오에서는 검토 되었으며 관련성이 없는 것으로 간주 되는 특정 데이터 원본을 제거할 수 있습니다.

Custodian와 연결 된 데이터 원본을 업데이트 하려면 다음을 수행 합니다.

1. **EDiscovery _GT_ Advanced ediscovery** 로 이동 하 여 사례를 엽니다.
  
2. **Custodians** 탭을 클릭 합니다.
  
3. 목록에서 custodian를 선택 하 고 플라이 아웃 페이지에서 **편집** 을 클릭 합니다.

    ![데이터 원본 편집](../media/EditCustodianDataSource.PNG)
  
4. **데이터 원본 선택** 탭을 클릭 하 여 Custodian의 Exchange 사서함 및 OneDrive 계정에 대 한 설정을 변경 하 고 **데이터 원본 선택을**클릭 합니다.
  
5. **추가 데이터 원본 선택** 탭을 클릭 하 여 custodian에 연결 된 팀, SharePoint 또는 Exchange 사서함을 추가 하거나 제거 합니다. 

    Custodian와 연결 된 데이터 원본에 대 한 자세한 내용은 [Add custodians](add-custodians-to-case.md#step-3-associate-additional-data-sources-to-a-custodian)in a custodian에서 "3 단계: 추가 데이터 원본을 a에 연결 합니다."를 참조 하십시오. 
  
6. Custodian에 대해 보류를 사용 하거나 사용 하지 않도록 설정 하려면 **custodial 보존** 을 클릭 합니다.

## <a name="resolve-custodian-processing-errors"></a>Custodian 처리 오류 해결

법적 조사를 위한 대부분의 eDiscovery 워크플로에서 custodian가 법적 사례에 추가 된 후 custodian 데이터의 하위 집합을 검색 합니다. 파일 크기나 데이터 손상 가능성이 매우 크므로 custodian과 연결 된 데이터 원본에 있는 일부 항목을 부분적으로 인덱싱할 수 있습니다. 고급 eDiscovery의 [고급 인덱싱](indexing-custodian-data.md) 기능을 사용 하는 경우에는 이러한 항목을 요청 시 다시 인덱싱하여 대부분의 부분적으로 인덱싱된 항목을 자동으로 수정할 수 있습니다.

Custodian가 사례에 추가 되 면 custodian와 연결 된 데이터 원본에 있는 데이터는 고급 인덱싱 프로세스에 의해 자동으로 다시 인덱싱됩니다. 즉, 데이터를 다운로드 하 여 수정 하 고 오프 라인으로 검색할 필요 없이 전체 위치에 유지할 수 있습니다. 그러나 법적 사례의 수명 주기 중 새 데이터 원본이 custodian에 연결 될 수 있습니다. 이 경우에는 고급 인덱싱 프로세스를 다시 실행 하 여 custodian 데이터의 인덱스를 다시 만들어 부분적으로 인덱싱된 항목을 수정 하 고 custodian의 데이터에 대 한 인덱스를 업데이트 합니다.

재 인덱싱 프로세스를 트리거하여 부분적으로 인덱싱된 항목을 처리 하려면 다음을 수행 합니다.

1. **EDiscovery _GT_ Advanced ediscovery** 로 이동 하 여 사례를 엽니다.

2. **Custodians 탭**을 클릭 한 다음 데이터를 reindexed 해야 하는 custodian을 선택 합니다. 

3. 플라이 아웃 페이지에서 **인덱스 업데이트**를 클릭 합니다.

   인덱스 작업을 만들었기를 알리는 대화 상자가 표시 됩니다.

Custodian 데이터를 다시 인덱싱하려면 장기 실행 프로세스입니다. 만들어진 해당 작업을 **custodian 데이터 다시 인덱싱**이라는 이름이 지정 됩니다. **인덱싱 작업 상태** 열에서 상태를 모니터링 하 여 **작업** 탭 이나 **Custodians** 탭의 진행 상황을 추적할 수 있습니다.

자세한 내용은 다음을 참조하세요.

- [오류 처리 작업](processing-data-for-case.md)

- [작업 관리](managing-jobs-ediscovery20.md)

## <a name="release-a-custodian-from-a-case"></a>사례에서 custodian 릴리스

사례가 마감 되거나, custodian가 사례에 대 한 콘텐츠를 보존 하기 위해 더 이상 의무를 받지 않거나, custodian이 사례와 더 이상 관련이 없는 것으로 간주 되는 경우에 custodian이 릴리스됩니다. 

보존 공지가 게시 된 후에 custodian를 해제 하면 릴리스 알림이 custodian로 전송 됩니다. 또한 custodian와 연결 된 데이터 원본에 대해 저장 된 모든 보류는 제거 됩니다. Custodian이 *자동 보존 상태로*설정 되 면 법적 보존 알림이 실행 되지 않은 경우 릴리스 알림이 전송 되지 않지만 해당 custodian와 연결 된 데이터 원본에 적용 되는 모든 보류는 제거 됩니다.

Custodian를 해제 하려면 다음을 수행 합니다. 

1. **EDiscovery _GT_ Advanced ediscovery** 로 이동 하 여 사례를 엽니다.

2.  **Custodians** 탭으로 이동 합니다.

3.  **Custodians 탭**을 클릭 한 다음 사례에서 출시 되는 custodian을 선택 합니다.

4. 플라이 아웃 페이지에서 **Custodian 릴리스**를 클릭 합니다.

   Custodian과 연결 된 데이터 원본에 보류가 설정 되 고 보류가 제거 되 고 다른 고급 eDiscovery 사례와 관련 된 다른 보류에도 적용 되는 경우를 설명 하는 경고 페이지가 표시 됩니다. 여기에는 office 365 보존 정책과 같은 Office 365의 다른 유형의 보존 및 보존 기능이 포함 되어 있습니다.

5. **예** 를 클릭 하 여 custodian 릴리스를 확인 합니다. 

    **Custodians** 탭에서이 사용자의 상태는 **릴리즈됨** 으로 설정 되 고 플라이 아웃 페이지의 **보류 상태** 는 **False**로 변경 됩니다. 

> [!NOTE]
> Custodian는 몇 가지 법적 사례와 동시에 포함 될 수 있습니다. Custodian가 사례에서 해제 되 면 다른 중요 한 보존 및 알림에는 영향을 받지 않습니다.

## <a name="bulk-edit-custodians"></a>Custodians 대량 편집

대량 편집기를 사용 하 여 여러 custodians을 동시에 편집할 수 있습니다. 이 작업을 수행 하려면 **custodians** 탭에서 custodians를 두 개 이상 선택 하 여 벌크 편집기를 표시 한 다음 작업 중 하나를 클릭 하면 됩니다.

![여러 custodians 설정을 편집 하기 위한 플라이 아웃 페이지](../media/AeDBulkEditCustodians.png)