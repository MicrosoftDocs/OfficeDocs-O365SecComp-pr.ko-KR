---
title: 고급 eDiscovery (미리 보기) 사례에 custodians 추가
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: fe208f4a9f7927d8481d5c6ec8b901baafb98626
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243584"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a>고급 eDiscovery (미리 보기) 사례에 custodians 추가

고급 eDiscovery (미리 보기)를 사용 하 여 기본 제공 custodian 관리 도구를 활용 하 여 custodians 관리와 관련 하 여 워크플로를 조정 하 고 사례 내에서 custodial 데이터 원본의 관련성을 식별할 수 있습니다. custodian를 추가 하는 경우 시스템에서 기본 Exchange 사서함 및 비즈니스용 OneDrive 사이트를 자동으로 식별 하 고 유지를 배치할 수 있습니다. 검색을 수행 하는 동안 custodian가 오늘 구성원 인 더 이상 custodian에 액세스 한 추가 사서함 또는 사이트를 찾아서 매핑할 수도 있습니다.

다음 워크플로를 사용 하 여 보안 & 준수 센터 내의 고급 eDiscovery (미리 보기)에서 custodians을 추가 하 고 관리 합니다. 

![Custodian 관리 탭](../media/CustodianMgtPage.png)


## <a name="step-1-identify-potential-custodians"></a>1 단계: 잠재 custodians 식별

첫 번째 단계는 사용자에 게 적합 한 custodians를 식별 하는 것입니다. custodians를 사례에 추가 하려면 ediscovery 관리자 또는 ediscovery 관리자 역할 그룹의 구성원 이어야 합니다.   

![잠재 Custodians 확인](../media/AddCustodianStep1.png)

기존 Advanced eDiscovery (Preview) 사례에 custodians를 추가 하려면 다음을 수행 합니다.

1. **고급 eDiscovery (미리 보기)** 페이지에서 해당 사례로 이동 합니다.
 
2. 사례를 선택한 후에는 **Custodians** 탭으로 이동 하 고 **+ 추가 Custodian**를 클릭 합니다. 
 
3. 사례에 추가 하려는 custodians를 선택 합니다. 입력을 시작 하 여 조직의 Azure Active Directory에서 사용자를 검색 하 고 선택할 수 있습니다.
 
4. custodians 목록을 완성 한 후에는 **다음** 을 클릭 하 여 잠재적 데이터 원본의 식별을 시작 합니다. 
  
## <a name="optional-step-2-select-custodian-data-sources"></a>반드시 2 단계: custodian 데이터 원본 선택

custodians를 사례에 추가한 후에는 Office 365을 활용 하 여 기본 custodian 데이터 원본을 식별 하 고 보존 하는 데 도움을 받을 수 있습니다. 이 워크플로의 다음 단계는 1 단계에서 지정한 custodians 소유한 데이터 원본을 선택 하는 것입니다. 

![Custodial 데이터 원본 선택](../media/AddCustodianStep2.png)

custodian 데이터 원본을 확인 하려면 다음을 수행 합니다. 

1. 각 custodian에 대해 시스템에서 custodian의 기본 exchange 사서함을 자동으로 식별 하 고 추가 하도록 하려면 **Exchange** 를 선택 합니다. 
 
2. 각 custodian에 대해 시스템에서 custodian의 기본 onedrive URL을 자동으로 식별 하 고 추가 하도록 하려면 **OneDrive** 를 선택 합니다. 

    선택한 후에는 자동으로 데이터 원본을 식별 하 고이를 사례에 추가 하려고 합니다.
 
4. **다음** 을 클릭 하 여 추가 데이터 원본을 custodian에 매핑합니다.

## <a name="optional-step-3-map-additional-data-sources"></a>반드시 3 단계: 추가 데이터 원본 매핑

사용자의 사례에 따라 지정 된 custodian에 사용 되었을 수 있는 사서함, custodian가 현재 구성원으로 속해 있는 그룹 또는 custodian가 이전에 액세스 한 사이트를 추가 해야 할 수도 있습니다. 기본 custodian 데이터 원본 외에도 office 365 데이터 원본을 custodian에 추가 하거나 office 365을 활용 하 여 관련 데이터 원본을 식별 하는 데 도움을 줄 수 있습니다. 

![추가 데이터 원본 매핑](../media/AddCustodianStep3.PNG)

사서함, 사이트 또는 팀을 특정 custodian에 매핑하려면 다음을 수행 합니다.
1. **추가** 를 선택 하 여 사서함, 사이트 및 팀과 같은 콘텐츠 위치를 특정 custodian에 할당 합니다. 

2. 플라이 아웃에서 다음을 지정 합니다. ![데이터 원본 매핑](../media/AddCustodianStep4.PNG)
  -  **Exchange 사서함** - **사용자, 그룹 또는 팀 선택을** 클릭 한 다음 **사용자, 그룹 또는 팀** 선택을 클릭 합니다. 선택한 custodian에 할당할 사서함을 지정 하려면 검색 상자를 사용 하 여 사용자 사서함 및 메일 그룹을 찾습니다. 또한 Office 365 그룹 또는 Microsoft 팀에 연결 된 사서함을 할당할 수 있습니다. 사용자, 그룹, 팀 확인란을 선택 하 고 **선택을**클릭 한 후 **완료**를 클릭 합니다.

        > [!NOTE]
        > 사용자, 그룹 또는 팀 선택을 클릭 하 여 사서함을 지정 하는 경우 표시 되는 사서함 선택은 비어 있습니다. 이것은 성능을 향상시키기 위한 것입니다. 이 목록에 사용자를 추가 하려면 검색 상자에 이름 (최소 3 자)을 입력 합니다.
     
     - **SharePoint 사이트** - **사이트 선택을** 클릭 한 다음 **사이트 선택을** 클릭 하 여 선택한 custodian에 할당할 추가 SharePoint 및 비즈니스용 OneDrive 사이트를 지정 합니다. 또한 Office 365 그룹 또는 Microsoft 팀에 대 한 SharePoint 사이트의 URL을 추가할 수 있습니다. 할당 하려는 각 사이트의 URL을 입력 합니다. **선택을**클릭 하 고 **완료**를 클릭 합니다.
     - **microsoft 팀** - **팀 선택을** 클릭 한 다음 **팀 선택을** 다시 클릭 하 여 custodian가 오늘 구성원 인 Microsoft 팀 그룹의 목록을 확인 합니다. custodian에 추가할 팀을 선택 합니다. 선택한 후에는 시스템에서 자동으로 &를 확인 하 여 해당 Microsoft 팀과 연결 된 SharePoint 사이트 및 그룹 사서함을 선택 합니다. **선택을**클릭 하 고 **완료**를 클릭 합니다.
        
      > [!NOTE]
      > Microsoft 팀을 더 추가 하려면 위에 표시 된 대로 사서함 및 SharePoint 사이트를 별도로 추가 해야 합니다.

출처를 매핑한 후에는 방금 추가한 custodians의 총 사서함, 사이트 및 팀을 볼 수 있습니다. 특정 custodian 관련 데이터 원본을 완성 하면이 매핑이 유지 관리 되 고 eDiscovery 컬렉션, 처리 및 검토 워크플로로 확장 됩니다. 

## <a name="optional-step-4-place-custodians-on-hold"></a>반드시 4 단계: custodians를 보류에 배치

![위치 유지](../media/AddCustodianStep5.PNG)

사례에 추가 하려는 custodians 및 데이터 원본을 완성 한 후에는 custodians의 일부 또는 전체를 보류에 추가할 수 있습니다. custodian를 보류 상태로 설정 하면 custodian을 해제할 때까지 해당 사용자에 게 매핑된 콘텐츠가 유지 됩니다. 경우에 따라 custodians를 보류 하지 않고 대/소문자에 추가할 수 있습니다. 

선택한 custodians 및 데이터 원본을 보류 상태로 설정 하려면 다음을 수행 합니다.

1. custodian 선택 사항을 확인 하 고 각 custodian 보류에 대 한 확인란을 선택 합니다. custodian가 보존 된 후에는 모든 custodial 원본이 포함 된 custodian 보류 정책이 자동으로 만들어집니다. 옵션을 선택 하지 않으면 custodian 및 선택한 데이터 원본이 사례에 추가 되 고 콘텐츠는 보존 되지 않습니다.

2. **보류** 탭으로 이동 하 여 **Custodian 보류 정책을**선택 합니다. 

3. **편집** 을 클릭 하 여 선택한 모든 custodian 데이터 원본을 확인 합니다.

   
