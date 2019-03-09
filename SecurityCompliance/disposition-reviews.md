---
title: 처리 검토 개요
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Office 365에서 콘텐츠를 보존 하는 보존 레이블을 만들 때 보존 기간이 끝나면 처리 검토를 트리거하도록 선택할 수 있습니다.
ms.openlocfilehash: 5c55b842045eefd42745486c603e34f6498b3bac
ms.sourcegitcommit: 07a4f9a8888756e05cd67ca24f6121b2a4e9f464
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/09/2019
ms.locfileid: "30512663"
---
# <a name="overview-of-disposition-reviews"></a>처리 검토 개요

콘텐츠가 보존 기간의 끝에 도달 하면 해당 콘텐츠를 검토 하 여 안전 하 게 삭제할 수 있는지 여부 ("삭제 된")를 결정 해야 하는 몇 가지 이유가 있습니다. 예를 들어 다음을 수행 해야 할 수 있습니다.
  
- 소송 또는 감사의 경우 관련 콘텐츠의 삭제 ("처리")를 일시 중단 합니다.
    
- 처리 목록에서 콘텐츠를 제거 하 여 해당 콘텐츠에 조사 또는 기록 값이 있는 경우 보관 사서함에 저장 합니다.
    
- 원래 정책이 임시 또는 provisional 솔루션 인 경우 콘텐츠에 다른 보존 기간을 할당 합니다.
    
- 콘텐츠를 클라이언트에 반환 하거나 다른 조직으로 전송 합니다.
    
Office 365에서 보존 레이블을 만들 때 보존 기간이 끝나면 처리 검토를 트리거하도록 선택할 수 있습니다. 처리 검토에서 다음을 수행 합니다.
  
- 선택한 사용자는 검토할 콘텐츠가 있는 전자 메일 알림을 받습니다. 이러한 검토자는 개별 사용자, 메일 그룹 또는 Office 365 그룹이 될 수 있습니다. 알림은 주 단위로 전송 됩니다.
    
- 검토자가 보안 &amp; 및 준수 센터의 **처리** 페이지로 이동 하 여 콘텐츠를 검토 합니다. 검토자는 처리를 위해 대기 중인 각 보존 레이블의 수를 확인 한 다음 보존 레이블을 선택 하 여 해당 레이블이 있는 모든 콘텐츠를 볼 수 있습니다.
    
- 각 문서 또는 전자 메일에 대해 검토자는 다음을 수행할 수 있습니다.
    
  - 다른 보존 레이블을 적용 합니다.
    
  - 보존 기간을 연장 합니다.
    
  - 영구적으로 삭제 합니다.
    
- 검토자가 보류 중 또는 완료 된 dispositions를 보고 해당 목록을 .csv 파일로 내보낼 수 있습니다.

> [!NOTE]
> 처리 검토에는 Office 365 Enterprise E5 구독이 필요 합니다.
  
처리 검토에는 Exchange 사서함, SharePoint 사이트, OneDrive 계정 및 Office 365 그룹의 콘텐츠가 포함 될 수 있습니다. 해당 위치에서 처리 검토를 대기 중인 콘텐츠는 검토자가 콘텐츠를 영구적으로 삭제 하도록 선택한 후에만 삭제 됩니다.
  
![보안 및 준수 센터의 Dispositions 페이지](media/Retention_Dispositions_v2_page.png)

## <a name="setting-up-the-disposition-review-by-creating-a-retention-label"></a>보존 레이블을 만들어 처리 검토 설정

이 워크플로는 처리 검토를 설정 하는 기본 워크플로입니다. 이 흐름은 보존 레이블을 게시 한 다음 사용자가 수동으로 적용 하는 것을 보여 줍니다. 또는 처리 검토를 트리거하는 보존 레이블을 콘텐츠에 자동으로 적용할 수 있습니다.
  
![처리가 작동 하는 방식 흐름을 보여 주는 차트](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
처리 검토는 Office 365에서 보존 레이블을 만들 때 사용할 수 있는 옵션입니다. 이 옵션은 보존 정책에서는 사용할 수 없지만 콘텐츠를 보존 하도록 구성 된 보존 레이블만 사용 하는 것이 좋습니다.
  
보존 레이블에 대 한 자세한 내용은 [보존 레이블 개요](labels.md)를 참조 하세요.
  
![레이블에 대 한 보존 설정](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a>콘텐츠 삭제

콘텐츠를 검토할 준비가 된 전자 메일로 검토자에 게 알림을 받으면 보안 &amp; 및 준수 센터의 **처리** 페이지로 이동할 수 있습니다. 검토자는 처리를 위해 대기 중인 각 보존 레이블의 수를 확인 한 다음 보존 레이블을 선택 하 여 해당 레이블이 있는 모든 콘텐츠를 볼 수 있습니다.

보존 레이블을 선택한 후에는 다음 페이지에 해당 레이블에 대 한 모든 보류 중인 dispositions 표시 됩니다.

![처리 옵션](media/Retention_Disposition_options_v2.png)

검토자는 다음과 같은 작업을 수행할 수 있습니다. 
  
- 다른 보존 레이블을 적용 합니다.
    
- 보존 기간을 연장 합니다.
    
- 항목을 영구적으로 삭제 합니다.

검토자가 여러 항목을 선택 하 고 동시에 삭제할 수 있습니다.
    
검토자가 해당 위치에 대 한 사용 권한이 있는 경우 검토자는 링크를 사용 하 여 원래 위치에서 문서를 볼 수도 있습니다. 처리 검토 중에는 콘텐츠가 원래 위치에서 이동 하지 않으며, 검토자가이를 선택 하기 전 까지는 삭제 되지 않습니다.
  
전자 메일 알림은 매주 검토자에 게 자동으로 전송 됩니다. 따라서 콘텐츠가 보존 기간의 끝에 도달 하면 검토자가 콘텐츠 처리를 기다리고 있는 전자 메일 알림을 받는 데 최대 7 일이 걸릴 수 있습니다.
  
또한 모든 처리 작업이 감사 된다는 점에 유의 하십시오. 이를 위해 첫 번째 처리 작업의 최소 1 일 전에 감사를 설정 해야 함-자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오. 
  
## <a name="permissions-for-disposition"></a>처리 권한

**처리** 페이지에 대 한 액세스 권한을 얻으려면 검토자가 **처리 관리** 역할 및 **보기 전용 감사 로그** 역할의 구성원 이어야 합니다. 처리 검토자 라는 새 역할 그룹을 만들고이 두 역할을 해당 역할 그룹에 추가한 다음 역할 그룹에 구성원을 추가 하는 것이 좋습니다. 
  
자세한 내용은 [사용자에 게 Office 365 보안 &amp; 및 준수 센터에 대 한 액세스 권한 부여](grant-access-to-the-security-and-compliance-center.md) 를 참조 하세요.
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a>삭제 된 콘텐츠가 영구적으로 삭제 될 때 까지의 기간

처리 검토를 기다리는 콘텐츠는 검토자가 콘텐츠를 영구적으로 삭제 하도록 선택한 후에만 삭제 됩니다. 검토자가이 옵션을 선택 하면 SharePoint 사이트 또는 OneDrive 계정의 콘텐츠가이 섹션에서 설명 하는 표준 정리 프로세스를 수행할 수 있습니다. [보존 정책이 현재 위치에서 콘텐츠에 작동 하는 방식](retention-policies.md#how-a-retention-policy-works-with-content-in-place)입니다.
  
즉, 다음을 의미 합니다.
  
- 문서 라이브러리의 콘텐츠는 처리 후 **7 일 이내** 에 1 단계 휴지통으로 이동 되 고 그 후에 영구적으로 삭제 됩니다 **** . 휴지통이 검색을 통해 인덱싱되지 않으므로 eDiscovery 보류에서 해당 콘텐츠를 사용할 수 없습니다.

- 보존 보류 라이브러리의 콘텐츠는 처리의 **7 일 이내** 에 영구적으로 삭제 됩니다.

- Exchange 사서함의 항목은 처리의 **14 일 이내** 에 영구적으로 삭제 됩니다. 14 일은 기본 설정 이지만 30 일까지 구성 될 수 있습니다.
    
## <a name="view-pending-dispositions-and-disposed-items"></a>보류 중인 dispositions 및 삭제 한 항목 보기

**보류 중인 처리** 페이지에서 특정 보존 레이블의 보류 중 및 완료 된 dispositions를 모두 볼 수 있습니다. 
  
- **보류 중인 처리** 에는 보존 기간 끝에 도달 하 여 처리 검토가 필요한 항목이 표시 됩니다. 각 항목을 검토 한 후에 다른 보존 레이블을 적용할지 여부를 결정 하거나, 보존 기간을 연장 하거나, 영구적으로 삭제 합니다. 여러 항목을 선택할 수 있습니다.
    
- **삭제 된 항목** 탭에는 처리 검토 중에 삭제를 승인 하 고, 이제 영구적으로 삭제 되는 프로세스에 dispositions 표시 됩니다. 다른 보존 레이블이 적용 된 항목이 나 검토 중에 확장 한 보존 기간은 여기에 표시 되지 않습니다.

![처리 탭](media/Retention_Disposition_tabs.png)
    
### <a name="filter-the-disposition-views"></a>처리 보기 필터링

보존 레이블 또는 시간 범위로 이러한 보기를 필터링 할 수 있습니다. 보류 중인 dispositions의 경우 시간 범위는 만료 날짜를 기준으로 합니다. 삭제 된 항목의 경우에는 시간 범위가 삭제 날짜를 기준으로 합니다.
  
![처리 필터 옵션](media/Retention_filter_options.png)

### <a name="export-the-disposition-items"></a>처리 항목 내보내기

또한 두 보기의 항목을 Excel에서 열 수 있는 .csv 파일로 내보낼 수도 있습니다.
  
![Excel에서 내보낸 처리 데이터](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

