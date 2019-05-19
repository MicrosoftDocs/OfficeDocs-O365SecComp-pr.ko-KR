---
title: 고급 eDiscovery 사례에 custodians 추가
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
ms.openlocfilehash: 8cc3d7db959c31c4657bb8c0d270f014e598e143
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155340"
---
# <a name="add-custodians-to-an-advanced-ediscovery-case"></a>고급 eDiscovery 사례에 custodians 추가

고급 eDiscovery의 기본 제공 custodian 관리 도구를 사용 하 여 custodians 관리를 위한 워크플로를 조정 하 고 사례와 연결 된 관련 custodial 데이터 원본을 식별 합니다. Custodian를 추가 하면 시스템에서 Exchange 사서함 및 비즈니스용 OneDrive 계정을 자동으로 식별 하 고 유지 합니다. 조사 프로세스를 진행 하는 동안 custodian에서 액세스 하거나 참여 하는 추가 데이터 원본 (예: 사서함, 사이트 또는 팀)을 식별할 수도 있습니다. 이러한 상황에서는 custodian 관리 도구를 사용 하 여 해당 데이터 원본을 특정 custodian에 연결할 수 있습니다. Custodians를 사례에 추가 하 고 다른 데이터 원본을 이러한 원본과 연결한 후에는 데이터를 빠르게 보존 하 고 custodial 데이터를 검색할 수 있습니다.

고급 eDiscovery 사례에서 custodians을 추가 하 고 관리 하려면 다음 워크플로를 사용 합니다. 

![Custodian 관리 탭](../media/CustodianMgtPage.png)

## <a name="before-you-begin"></a>시작하기 전에

Custodians를 사례에 추가 하려면 eDiscovery 관리자 역할 그룹의 구성원 이어야 합니다. 이렇게 하면 custodians를 사례에 추가 하 고 custodial 데이터 원본에 대 한 보류를 수행 하는 데 필요한 권한이 제공 됩니다.


## <a name="step-1-add-potential-custodians"></a>1 단계: 잠재 custodians 추가

첫 번째 단계는 custodians를 식별 하 고 사례에 추가 하는 것입니다.

1. **고급 eDiscovery** 홈 페이지에서 custodians를 추가할 사례를 클릭 합니다. 
 
2. **Custodians** 탭을 클릭 하 고 **+ 추가 Custodians**를 클릭 합니다.

3. 사례에 추가할 custodians를 찾습니다. 조직의 Azure Active Directory에서 사용자를 표시 하려면 사용자 이름의 첫 부분을 입력 합니다. 올바른 사용자를 찾았으면 이름을 클릭 하 여 목록에 추가 합니다.

   ![잠재 Custodians 확인](../media/AddCustodianStep1.png)
 
4. 관련 custodians를 모두 추가한 후 **다음** 을 클릭 하 여 custodians의 기본 데이터 원본을 선택 합니다.
  
## <a name="step-2-select-custodian-data-sources"></a>2 단계: custodian 데이터 원본 선택

Custodians을 추가한 후에는 custodian 도구를 통해 각 custodian에서 소유 하는 기본 데이터 원본을 확인할 수 있습니다. 특히 이러한 데이터 위치는 custodian의 Exchange 사서함 및 OneDrive 계정입니다. 

Custodian 데이터 원본을 확인 하려면 다음을 수행 합니다. 

1. 모든 custodians에 대 한 Exchange 사서함을 선택 하려면 열 맨 위에 있는 **exchange** 확인란을 클릭 합니다. 그런 다음 특정 custodian의 확인란을 선택 취소 하 여 사서함을 custodial 위치로 제거할 수 있습니다. 또는 열 맨 위에 있는 **Exchange** 확인란을 선택 하지 않은 채로 둔 다음 개별 custodians에 대 한 확인란을 선택할 수 있습니다. 
 
   ![Custodial 데이터 원본 선택](../media/AddCustodianStep2.png)
 
2. Custodians의 OneDrive 계정에 대해 동일한 작업을 반복 합니다. 

    Custodian 데이터 원본을 선택한 후에는 자동으로 이러한 데이터 원본을 식별 하 고 확인 한 다음 custodians와 연결 된 데이터 원본으로이를 사례에 추가 합니다.
 
4. **다음** 을 클릭 하 여 대/소문자를 구분 하 여 추가 데이터 원본을 custodians에 연결 합니다.

## <a name="step-3-associate-additional-data-sources-to-a-custodian"></a>3 단계: 추가 데이터 원본을 custodian에 연결

조사 중인 사례에 따라 특정 custodian에 액세스할 수 있는 사서함, custodian가 현재 속해 있는 Office 365 그룹 또는 custodian에도 액세스 한 사이트에 대 한 콘텐츠를 검색 하 고 보존 해야 할 수도 있습니다. 따라서 이전 단계에서 지정한 기본 custodian 데이터 원본 외에, 사례에서 추가 Office 365 데이터 원본을 custodian에 연결할 수도 있습니다. 

사서함, 사이트 또는 팀을 특정 custodian에 매핑하려면 다음을 수행 합니다.

1. **추가 데이터 원본 선택** 페이지에서 특정 custodian 행에 **추가** 를 클릭 합니다. 
  
   ![추가 데이터 원본 매핑](../media/AddCustodianStep3.PNG)

2. 플라이 아웃 페이지에서 다음 Office 365 서비스의 데이터 원본을 지정할 수 있습니다.
  
   -  **Exchange 전자 메일** - **사용자, 그룹 또는 팀 선택을** 클릭 한 다음 **사용자, 그룹 또는 팀 선택을** 클릭 합니다. 검색 상자를 사용 하 여 custodian와 연결할 사서함을 찾습니다. 선택한 custodian에 할당할 사서함을 지정 하려면 검색 상자를 사용 하 여 사용자 사서함 및 메일 그룹을 찾습니다. 또한 Office 365 그룹 또는 Microsoft 팀에 연결 된 사서함을 할당할 수 있습니다. 사용자, 그룹, 팀 확인란을 선택 하 고 **선택을**클릭 한 후 **완료**를 클릭 합니다.

        > [!NOTE]
        > 사용자, 그룹 또는 팀 선택을 클릭 하 여 사서함을 지정 하는 경우 표시 되는 사서함 선택은 비어 있습니다. 이것은 성능을 향상시키기 위한 것입니다. 이 목록에 사서함을 추가 하려면 검색 상자에 이름 또는 별칭 (최소 3 자)을 입력 합니다.
     
     - **Sharepoint 사이트** - **사이트 선택을** 클릭 한 다음 **사이트 선택을** 다시 클릭 하 여 조직의 SharePoint 사이트 목록을 표시 합니다. 사이트를 custodian와 연결 하려면 목록에서 사이트를 선택 하거나, Office 365 그룹, Microsoft 팀 또는 OneDrive 계정과 연결 된 사이트 또는 다른 사이트의 URL을 입력할 수 있습니다.
     
     - **팀** - **팀 선택을** 클릭 한 다음 **팀 선택을** 다시 클릭 하 여 Custodian가 현재 구성원 인 Microsoft 팀 목록을 표시 합니다. Custodian에 추가할 팀을 선택 합니다. 선택한 후에는 시스템에서 자동으로 &를 확인 하 여 해당 Microsoft 팀과 연결 된 SharePoint 사이트 및 그룹 사서함을 선택 합니다. **선택을**클릭 하 고 **완료**를 클릭 합니다.

       ![데이터 원본 매핑](../media/AddCustodianStep4.PNG)
        
      > [!NOTE]
      > 추가 팀을 custodian에 연결 하려면 **Exchange 메일** 및 **SharePoint 사이트** 위치를 사용 하 여 팀과 연결 된 사서함과 사이트를 개별적으로 추가 해야 합니다.

추가 데이터 원본을 custodians와 연결한 후에는 **추가 데이터 원본 선택 페이지**에서 각 custodian와 연관 된 사서함, 사이트 및 팀의 총 수를 볼 수 있습니다. 특정 custodian 관련 데이터 원본을 완료 하면이 연결이 유지 관리 되 고 eDiscovery 워크플로의 컬렉션, 처리 및 검토 단계 중에 사용 됩니다.

## <a name="step-4-place-custodians-on-hold"></a>4 단계: custodians를 보류에 배치

사례에 추가할 custodians 및 데이터 원본을 완성 한 후에는 필요에 따라 custodians 중 일부 또는 전체를 보류할 수 있습니다. Custodian을 보류할 때 custodian에 연결 된 모든 콘텐츠 위치의 모든 콘텐츠는 보류를 제거 하거나에서 custodian를 해제할 때까지 보존 됩니다. 경우에 따라 custodians를 보류 하지 않고 대/소문자에 추가할 수 있습니다.

Custodians 및 데이터 원본을 보류 하려면 다음을 수행 합니다.

1. **선택한 custodians** 페이지를 유지 하려면 열 맨 위에 있는 **보류** 확인란을 클릭 하 여 모든 custodians을 보류 상태로 둡니다. 그런 다음 보류에서 제거할 특정 custodian의 확인란을 선택 취소할 수 있습니다. 또는 열 맨 위에 있는 **보류** 확인란을 선택 하지 않은 상태로 둔 다음 개별 custodians에 대 한 확인란을 선택할 수 있습니다. 
 
   ![위치 유지](../media/AddCustodianStep5.PNG)

2. Custodian 보류 선택 사항을 확인 하 고 **완료**를 클릭 합니다.

A custodian를 설치 하지 않으면 custodian 및 연결 된 데이터 원본이 사례에 추가 되지만 해당 데이터 원본의 콘텐츠가 보존 되지 않습니다.

Custodian가 보존 된 후에는 모든 custodial 원본이 포함 된 custodian 보류 정책이 자동으로 만들어집니다. 이 정책을 보려면 다음을 수행 합니다.

1. 사례 **홈** 페이지에서 **보류** 탭을 클릭 한 다음 **CustodianHold**를 클릭 합니다.  

2. 플라이 아웃 페이지에서 **보류 편집** 을 클릭 하 여 보류 된 모든 custodian 데이터 원본을 확인 합니다.

