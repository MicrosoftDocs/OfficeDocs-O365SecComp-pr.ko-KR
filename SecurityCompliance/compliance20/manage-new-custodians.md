---
title: Advanced eDiscovery (미리 보기)의 경우 custodians 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 0c33335ecc103a97090dacaa769315ad9413b3c6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214978"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a>Advanced eDiscovery (미리 보기)의 경우 custodians 관리

Custodians 탭에는 사례에 있는 모든 Custodians의 정렬 가능한 목록이 포함 되어 있습니다. custodians를 사례에 추가 하면 각 custodian에 대 한 세부 정보가 Azure Active Directory에서 자동으로 수집 됩니다.

## <a name="viewing-custodian-details"></a>custodian 세부 정보 보기

custodian 세부 정보가 포함 된 플라이 아웃 페이지는 사례에 custodian을 추가한 후에 표시 되 고 **Custodians** 탭의 목록에서 선택 합니다. 여기에서 해당 custodian 관련 된 모든 세부 정보를 볼 수 있습니다. 플라이 아웃 페이지에는 다음과 같은 필드가 있습니다.

- 연락처 정보

  - **표시 이름**: custodian 주소록에 표시 되는 이름입니다. 일반적으로 custodian의 이름, 중간 이니셜 및 성이 조합 된 이름입니다.
  - **메일/SMTP**: custodian에 대 한 SMTP 주소 (예 jeff@contoso.onmicrosoft.com)입니다.  
  - **제목**: custodian의 직위입니다.
  - **부서**: custodian가 작동 하는 부서의 이름입니다.
  - **관리자**: custodian의 관리자입니다. 지정 된 관리자가이 custodian에 대 한 에스컬레이션 통신을 수신 합니다.
  
- 위치 정보

  - **구/군/** 시: custodian가 있는 구/군/시입니다.
  - **상태**: custodian 주소의 시/도입니다.
  - **국가/지역**: custodian가 있는 국가/지역입니다. 예를 들어 "US" 또는 "영국"을 예로 들 있습니다.
  - **office**: custodian의 비즈니스 장소에 있는 사무실 위치입니다.

- 사례 정보

  - **보류 상태**: custodian를 보류 했는지 여부를 나타냅니다. 
  - **통신 상태**: custodian에 보류 알림이 발급 되었는지 여부를 나타냅니다. custodian에 공지 사항이 발급 된 경우이는 *게시*된 것으로 표시 됩니다. custodian에 알림이 발급 되지 않은 경우이 상태가 *게시 취소*됩니다. 
  - **상태**: 사례 내의 custodian 상태입니다. 이는 custodian가 계속 유지 되 고 있는 경우 *활성화* 됩니다. custodian가 사례에서 제거 되 면 해당 상태가 ' *출시*됨 '으로 변경 됩니다. 

- 처리 상태

  - **인덱싱 상태**: 딥 인덱싱 작업의 상태를 나타냅니다.  
  - **인덱싱 마지막 업데이트 시간**: 딥 Indexing 작업이 마지막으로 트리거된 날짜에 대 한 datestamp를 나타냅니다.
  - **데이터 원본**: custodian으로 선택 된 사서함, 사이트 및 팀의 수를 표시 합니다.

## <a name="updating-a-custodian"></a>custodian 업데이트

사례가 진행 됨에 따라 특정 custodian & 관련 된 추가 데이터 원본이 있을 수 있습니다. 다른 시나리오에서는 검토 되었으며 관련성이 없는 것으로 간주 되는 특정 데이터 원본을 제거할 수 있습니다.

custodian 및 선택한 데이터 원본을 업데이트 하려면:

1. **eDiscovery > Advanced eDiscovery (Preview)** 에서 기존 사례를 선택 합니다.
  
2. 경우에는 **Custodians** 탭을 클릭 합니다.
  
3. 목록에서 custodian를 선택 하 고 **원본 편집**을 클릭 합니다.
  
4. **데이터 원본 선택을**클릭 하 여 Exchange 및 OneDrive 위치에 대 한 선택 항목을 업데이트 합니다.
  
5. **추가 데이터 원본을 선택**하 여 사용자를 매핑한 팀, SharePoint 또는 Exchange 사서함을 추가 하거나 제거 합니다. custodian에 데이터 원본을 매핑하는 방법에 대 한 자세한 내용은 [Add custodians to a case](add-custodians-to-case.md)를 참조 하십시오.
  
6. custodian 보류 상태를 업데이트 하려면 **위치 custodial 보류**를 클릭 하 고 custodians에 대해 보류를 사용 하거나 사용 하지 않도록 설정 합니다.

> [!TIP]
> 여러 custodians을 선택 하 여 custodians 집합의 다시 인덱싱, 릴리스 또는 편집과 같은 대량 작업을 수행할 수 있습니다.

## <a name="resolving-custodian-processing-errors"></a>custodian 처리 오류 해결

대부분의 법적 워크플로에서는 특정 조사에 대 한 custodians가 추가 된 후 사용자 데이터의 하위 집합이 검색 됩니다. 파일 크기가 크거나 손상으로 인해 custodians의 데이터 원본에 있는 일부 항목이 부분적으로 인덱싱될 수 있습니다. 고급 eDiscovery (미리 보기) 심층 인덱싱 기능을 사용 하면 요청 시 이러한 항목을 다시 크롤링하고 다시 사용 하 여 이러한 부분 색인화 된 항목을 자동으로 수정할 수 있습니다. 

custodian가 사례에 추가 되 면 데이터는 자동으로 "deep 인덱싱될"로 유지 되므로 사용자는 Office 365 외부에서 검색을 다운로드, 수정 및 다시 실행 하는 대신 이러한 부분 인덱싱된 항목을 즉시 사용할 수 있습니다. 사례 수명 주기 동안 사용자는 지정 된 custodian에 대해 항목을 수정 하거나 새 데이터 원본을 추가할 수 있습니다. 이 경우 Custodian 인덱스를 업데이트 해야 할 수 있습니다. 

재 인덱싱 프로세스를 트리거하여 부분적으로 인덱싱된 항목을 처리 하려면 다음을 수행 합니다.

1. **eDiscovery > Advanced eDiscovery (Preview)** 로 이동 하 여 기존 사례를 선택 합니다.

2. 경우에는 **Custodians 탭**을 클릭 합니다. 

3. 다시 인덱싱되는 데 필요한 custodian를 선택 하 고 플라이 아웃 페이지에서 **인덱스 업데이트** 를 클릭 합니다.

4. **Custodians** 탭의 **인덱싱 작업 상태** 열에 있는 링크를 클릭 하 여 custodian 인덱스의 상태를 확인 합니다.  

5. 또한 **작업** 탭에서 다시 인덱싱 프로세스의 상태를 추적할 수 있습니다.

부분 인덱싱된 항목 다시 인덱싱 및 수정에 대 한 자세한 내용은 [문제 해결 오류 수정을](processing-data-for-case.md)참조 하십시오.

## <a name="releasing-a-custodian-from-a-case"></a>사례에서 custodian 해제

사례가 마감 되거나, custodian가 사례에 대 한 콘텐츠를 보존 하기 위해 더 이상 의무를 받지 않거나, 특정 사례와 더 이상 관련이 없는 것으로 간주 되는 경우에는 custodian가 릴리스됩니다. 

보존 공지가 게시 된 후에 custodian를 해제 하면 릴리스 알림이 custodian로 전송 됩니다. 또한 릴리스된 custodians에 대 한 특성을 보유 한 모든 custodial 제거 됩니다.

custodian가 법적 보존 알림을 발급 하지 않은 자동 보존 상태로 설정 된 경우에는 릴리스된 custodians에 사용 되는 모든 custodial이 제거 됩니다.  

custodian를 해제 하려면 다음을 수행 합니다. 

1.  **Custodians** 탭으로 이동 합니다.

2.  목록에서 custodian를 선택 하 고 플라이 아웃 페이지에서 **custodians 릴리스** 를 클릭 합니다.

    **Custodians** 탭에 있는 custodian의 상태가 " **해제** "로 설정 되 고 플라이 아웃 페이지의 **보류 상태가** **비활성**으로 변경 됩니다. 

> [!TIP]
> custodian에는 여러 법적 보존 문제가 동시에 포함 될 수 있습니다. custodian가 사례에서 해제 되 면 다른 중요 한 보존 및 알림이 영향을 받지 않습니다.

## <a name="related-information"></a>관련 정보

 - [데이터를 처리할 때 오류 수정](error-remediation.md) 
- [커뮤니케이션을 통한 작업](managing-custodian-communications.md)
