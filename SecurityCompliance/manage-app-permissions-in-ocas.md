---
title: Office 365 Cloud App Security를 사용하여 OAuth 앱 관리
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: office 365의 OAuth 앱-Cloud App Security는 사용자가 Office 365 데이터와 함께 사용할 수 있도록 다운로드 하는 앱을 관리 하는 데 도움이 됩니다.
ms.openlocfilehash: 0d9916414d55abb73fd99eaf30c3b6df0648b191
ms.sourcegitcommit: 1658be51e2c21ed23bc4467a98af74300a45b975
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/26/2019
ms.locfileid: "30862590"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a>Office 365 Cloud App Security를 사용하여 OAuth 앱 관리

|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |[배포 시작](turn-on-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](#next-steps)<br/> |
   
사용자가 자주 사용 하는 앱을 선호 하며, 특히 회사 또는 학교 정보를 쉽게 확인할 수 있도록 하 여 시간을 절약 하는 것이 좋습니다. 그러나 일부 앱은 액세스 하는 정보 및 해당 정보를 처리 하는 방법에 따라 조직에 보안 위험이 있을 수 있습니다. [Office 365 Cloud App Security](office-365-cas-overview.md)를 사용 하 여 전역 또는 보안 관리자 인 경우 조직에 대 한 OAuth 앱을 관리할 수 있습니다. 사용자가 Office 365 데이터와 함께 사용 하는 앱, 해당 앱에 포함 된 사용 권한 등을 확인할 수 있습니다. 
  
이 문서에서는 OAuth 앱 관리, 앱 승인, 금지 또는 보고 방법, 앱 쿼리를 만드는 방법에 대해 설명 합니다.
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a>OAuth 앱 관리 페이지를 찾는 방법

> [!NOTE]
> OAuth 앱은 Office 365 Cloud App Security 포털에서 관리 됩니다. 다음 작업을 수행 하려면 전역 관리자 이거나 보안 관리자 여야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요. 
  
1. Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.
  
2. **OAuth 앱** **조사** \> 를 선택 합니다.<br/>![O365 CAS 포털에서 조사를 선택 합니다.](media/OCAS-OAuthApps.png)<br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a>OAuth 앱 관리 페이지에 표시 되는 항목

다음 표에서는 OAuth 앱 관리 페이지에서 사용할 수 있는 컨트롤 및 옵션에 대해 설명 합니다.
  
|**항목**|**설명**|
|:-----|:-----|
|앱 쿼리 표시줄의 기본 아이콘  <br/> ![쿼리에 대 한 기본 쿼리 보기를 나타내는 아이콘](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|고급 보기로 전환 하려면이 옵션을 선택 합니다.  <br/> ( **기본**을 참조 하는 경우 고급 보기를 사용 하는 경우)  <br/> |
|앱 쿼리 모음의 고급 아이콘  <br/> ![쿼리에 대 한 고급 쿼리 보기를 나타내는 아이콘](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|기본 보기로 전환 하려면이를 선택 합니다.  <br/> **고급**을 표시 하는 경우 기본 보기를 사용 하 고 있는 것입니다.  <br/> |
|앱 목록에서 모든 세부 정보 아이콘 열기 또는 닫기  <br/> ![모든 앱에 대 한 모든 세부 정보를 열거나 닫으려면이 아이콘을 클릭 합니다.](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|각 앱에 대 한 세부 정보를 자세히 보거나 줄이려면이 아이콘을 선택 합니다.  <br/> |
|앱 목록의 내보내기 아이콘  <br/> ![모든 앱의 csv 파일을 내보내려면이 아이콘을 클릭 합니다.](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|앱 목록, 각 앱에 대 한 사용자 수, 앱, 사용 권한 수준, 앱 상태 및 커뮤니티 사용 수준에 연결 된 사용 권한을 포함 하는 CSV 파일을 내보내려면이 아이콘을 선택 합니다.  <br/> |
|Name  <br/> |이를 사용 하 여 앱의 이름을 확인 합니다. 설명, 게시자, 앱 웹 사이트 및 앱 ID와 같은 추가 정보를 보려면 이름을 선택 합니다.  <br/> |
|권한 부여 기준  <br/> |이 방법을 사용 하 여 Office 365 계정에 액세스 하기 위해 앱이 인증 된 사용자의 수를 확인할 수 있습니다. 사용자 계정 목록과 같은 자세한 정보를 보려면 번호를 선택 합니다.  <br/> |
|사용 권한 수준  <br/> ![앱에 대 한 permisiions 수준을 나타내는 아이콘](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|이를 통해 Office 365 데이터에 대 한 앱의 액세스 정도를 확인할 수 있습니다. 사용 권한 수준은 **낮음**, **중간**또는 **높음을**지정 하며, **** 이는 앱이 사용자의 프로필 및 이름에만 액세스 함을 나타낼 수 있습니다. 앱에 부여 된 사용 권한, 커뮤니티 사용 및 [거 버 넌 스 로그](suspend-or-restore-an-account-in-ocas.md)에서 관련 활동 등의 자세한 정보를 보려면 수준을 선택 합니다.  <br/> |
|마지막 권한 <br/> |이 방법을 사용 하 여 OAuth 앱이 조직의 Office 365 데이터에 액세스 하기 위해 마지막으로 권한이 부여 된 날짜 및 시간을 확인할 수 있습니다. <br/>  |
|동작<br/>![OAuth 앱](media/OCAS-OAuthAppApproveBanReport.png)<br/> |앱을 승인 되거나 금지 된 상태로 표시 하거나, Microsoft에 OAuth 앱을 보고 하거나, 지정 하지 않은 상태로 두려면이를 사용 합니다.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>앱을 승인 된 것으로 표시

**OAuth 앱 관리** 페이지에서 승인할 앱을 찾은 다음 **앱을 승인 된 것으로 표시** 아이콘을 선택 합니다. 
  
![앱을 승인 된 것으로 표시 아이콘을 선택 합니다.](media/OCAS-MarkOAuthApproved.png)
  
아이콘이 녹색으로 바뀌고 앱이 모든 Office 365 사용자에 대해 승인 됩니다.
  
> [!NOTE]
> 앱을 승인 된 것으로 표시 하면 최종 사용자에 게 영향을 주지 않습니다. 승인 된 앱을 시각적으로 표시 하면 아직 검토 하지 않은 앱과이를 분리할 수 있습니다. 
  
## <a name="ban-an-app"></a>앱 금지

1. **OAuth 앱 관리** 페이지에서 금지 하려는 앱을 찾은 다음 **앱을 금지 된 것으로 표시** 아이콘을 선택 합니다.<br/>![앱을 차단 된 것으로 표시 아이콘을 선택 합니다.](media/OCAS-MarkOAuthBanned.png)
  
2. 알림 메시지 상자에서 기존 텍스트를 그대로 유지 하거나 텍스트를 사용자 지정 합니다. 사용자에 게 앱이 금지 되었음을 알리는 것을 허용할 것인지 여부를 선택 합니다. <br/>![금지 된 앱에 대 한 메일 서식 파일](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. **앱 금지**를 선택 합니다.

## <a name="report-an-oauth-app-to-microsoft"></a>Microsoft에 OAuth 앱 보고

분석을 위해 Microsoft에 OAuth 앱을 제출 하려면 해당 앱을 보고 하면 됩니다.

1. **OAuth 앱 관리** 페이지에서 분석을 위해 제출할 앱을 찾습니다.

2. 줄임표 (열)를 선택 하 고 **보고서 앱 ...** 을 선택 합니다.<br/>![OAuth 앱 보고](media/OCAS-MarkOAuthReported.png)<br/>

3. **이 앱 보고서** 대화 상자에서 드롭다운 목록을 사용 하 여 관심 있는 사항을 표시 합니다. 기본적으로 **이 앱은 악성** 으로 선택 되어 있습니다. 그러나 사용할 수 있는 다른 옵션 중 하나를 선택할 수 있습니다. <br/>![OAuth 앱 보고](media/OCAS-ReportOAuthApp.png)<br/>

4. 는 선택한 대화 상대에 게 옵션을 유지 하 고 나열 된 전자 메일 주소를 확인 하거나 편집 합니다.

5. Choose **Submit**. 
    
## <a name="create-an-app-query"></a>앱 쿼리 만들기

다음과 같은 고급 보기를 사용 하는 것이 좋습니다. 

![고급 보기](media/OCAS-OAuthAppsAdvQueryView.png)

앱 쿼리 표시줄에서 **Advanced**가 표시 되 면 기본 보기를 사용 하 고 있는 것입니다. advanced를 클릭 하거나 탭 **** 하 여 고급 보기로 이동 합니다. 

![기본 보기](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. 쿼리 모음에서 **필터 선택** 목록을 사용 하 여 옵션을 선택 합니다. 
    - **앱** 특정 이름을 가진 앱
    - **앱 상태** 해당 상태를 기반으로 하는 앱 (승인, 금지 또는 결정 되지 않음)
    - **커뮤니티 사용** 커뮤니티 사용 수준 (드문, 드문, 공용)을 기반으로 하는 앱
    - **사용 권한 수준** 특정 권한 수준을 기반으로 하는 앱 
    - **사용 권한** 특정 권한이 필요한 앱
    - **Publisher**  특정 게시자의 앱
    - **사용자** 특정 사용자가 권한을 부여 받은 앱
   
2. **같음** 또는 **같지**않음을 선택한 다음 필터에 대 한 값을 지정 합니다.
    
3. 필터를 더 추가 하려면 더하기 기호 (![앱 쿼리를 위한 필터 아이콘 추가](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg))을 선택한 다음 2 단계와 3 단계로 반복 합니다.
    
4. 필터를 제거 하려면 x를 선택 합니다 (![앱 쿼리를 위한 필터 아이콘 제거](media/5339277f-555d-4749-8dcc-d2574250556e.jpg))를 필터 이름 옆에 둘 수 있습니다.
    
필터는 자동으로 적용 되며 앱 목록은 그에 따라 업데이트 됩니다.
  
## <a name="next-steps"></a>다음 단계

- [경고 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
- [Office 365 Cloud App Security에 대 한 웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 검토
    
- [Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토
    

