---
title: Office 365에서 위협에 대 한 자동 조사 및 응답
keywords: AIR, autoIR, ATP, 자동화, 조사, 대응, 재구성, 위협, 고급, 위협, 보호
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/09/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Office 365 Advanced Threat Protection 계획 2의 자동 보안 문제 대응 기능 사용을 시작 하세요.
ms.openlocfilehash: a7cec69fc7f739e065503121e456cc9bb3a34b31
ms.sourcegitcommit: ff370e93b792204547694139ef99bc0848304570
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36852760"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a>Office 365에서 위협에 대 한 자동 조사 및 응답

## <a name="overview"></a>개요

[Office 365 Advanced Threat Protection](office-365-atp.md) 요금제 2에는 경고 및 위협 처리에 대 한 보안 작업 팀의 시간과 노력을 줄일 수 있는 자동 인시던트 응답 (AIR) 기능이 포함 되어 있습니다. 이 문서를 읽으면 Office 365의 AIR 기능 사용을 시작할 수 있습니다. AIR의 작동 방식에 대 한 자세한 내용은 [Office 365에서 자동 인시던트 응답 (AIR)](automated-investigation-response-office.md)을 참조 하세요.

AIR을 사용 하 여 특정 알림이 트리거되면 하나 이상의 보안 playbook가 시작 되 고 자동 조사가 시작 됩니다. 자동화 된 조사 프로세스 중 및 후에 관리자와 보안 운영 팀은 다음을 수행할 수 있습니다.

- [조사 세부 정보 보기](#view-details-of-an-investigation)

- [조사 결과로 작업 검토 및 승인](#review-and-approve-actions) 

- [조사와 관련 된 경고에 대 한 세부 정보 보기](#view-details-about-an-alert-related-to-an-investigation)

> [!NOTE]
> 이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자, 보안 관리자, 보안 운영자 또는 보안 독자 여야 합니다. 자세한 내용은 [Microsoft 365 보안 센터: 역할 및 사용 권한을](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions)참조 하세요.

## <a name="view-details-of-an-investigation"></a>조사 세부 정보 보기

1. Office 365 전역 관리자, 보안 관리자 또는 보안 독자 (으 [https://protection.office.com](https://protection.office.com) )로 이동 하 여 로그인 합니다. 그러면 보안 & 준수 센터로 이동 합니다.

2. 다음 중 하나를 수행합니다.

    - **위협 관리** > **대시보드로**이동 합니다. 그러면 [보안 대시보드가](security-dashboard.md)이동 합니다. [보안 대시보드](security-dashboard.md)위쪽에 AIR widget이 표시 됩니다. **조사 요약과**같은 위젯을 선택 합니다.

    - **위협 관리** > **조사**로 이동 합니다. 

    어느 방법을 사용 하 든 조사 목록이 표시 됩니다.

    ![AIR의 주 조사 페이지](media/air-maininvestigationpage.png) 

3. 조사 목록에서 **ID** 열의 항목을 선택 합니다. 그러면 조사 그래프부터 시작 하 여 조사 세부 정보 페이지가 열립니다.

    ![AIR 조사 그래프 페이지](media/air-investigationgraphpage.png)

4. 여러 탭을 사용 하 여 조사에 대해 자세히 알아보세요.

## <a name="review-and-approve-actions"></a>작업 검토 및 승인

Office 365에서 자동화 된 조사는 일반적으로 하나 이상의 권장 작업을 수행 합니다. 그러나 보안 운영 팀이 승인 해야 작업을 수행할 수 있습니다. 다음 절차에 따라 작업을 검토 하 고 승인 합니다.

1. Office 365 전역 관리자, 보안 관리자 또는 보안 독자 (으 [https://protection.office.com](https://protection.office.com) )로 이동 하 여 로그인 합니다. 

2. **위협 관리** > **조사**로 이동 합니다.

3. 조사 목록에서 **ID** 열의 항목을 선택 합니다. 

3. 조사 세부 정보 보기에서 **작업** 탭을 선택 합니다. 승인 보류 중인 모든 작업은 여기에 나열 됩니다.

4. 목록에서 항목을 선택 합니다.

5. 권장 작업을 수행 하려면 **승인** 을 선택 하 고 아니면 작업을 수행 하지 않고 조사를 닫기 위해 **거부** 를 클릭 합니다.

## <a name="view-details-about-an-alert-related-to-an-investigation"></a>조사와 관련 된 경고에 대 한 세부 정보 보기

특정 유형의 경고는 Office 365에서 자동화 된 조사를 트리거합니다. 자세한 내용은 [Alerts](automated-investigation-response-office.md#alerts)를 참조 하십시오. 다음 절차에 따라 자동화 된 조사에 연결 된 경고에 대 한 세부 정보를 확인 합니다.

1. Office 365 전역 관리자, 보안 관리자 또는 보안 독자 (으 [https://protection.office.com](https://protection.office.com) )로 이동 하 여 로그인 합니다. 그러면 보안 & 준수 센터로 이동 합니다.

2. **위협 관리** > **조사**로 이동 합니다.

3. 조사 목록에서 **ID** 열의 항목을 선택 합니다. 

4. 조사에 대 한 세부 정보를 연 상태에서 **알림** 탭을 선택 합니다. 조사를 트리거한 모든 경고가 여기에 나열 됩니다.

5. 목록에서 항목을 선택 합니다. 플라이 아웃이 열리고 경고에 대 한 세부 정보와 추가 정보 및 작업에 대 한 링크가 제공 됩니다.

6. 플라이 아웃에 대 한 정보를 검토 하 고, 특정 경고에 따라 사용자에 대 한 **해결**, **억제**또는 **알림**등의 작업을 수행 합니다. 

    - **확인** 은 경고를 닫는 것과 동일 합니다.
    
    - 정책이 지정 된 기간에 대해 알림을 트리거하지 **않도록 설정 합니다** .
    
    - **사용자에** 게 사용자의 전자 메일 주소가 이미 입력 된 전자 메일을 시작 하 고, 보안 운영 팀에서 해당 사용자에 게 메시지를 입력할 수 있도록 합니다. 이는 [위협 탐색기](threat-explorer.md)를 사용 하 여 받는 사람에 게 메시지를 보내는 것과 비슷합니다.  

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a>사용자 지정 또는 타사 보고 솔루션에 Office 365 관리 활동 API 사용

조직에서 사용자 지정 또는 타사 보고 솔루션을 사용 하는 경우에는 Office 365 관리 활동 API를 사용 하 여 해당 솔루션의 자동화 된 조사에 대 한 정보를 볼 수 있습니다.

다음 리소스를 사용 하 여이를 설정할 수 있습니다.

|리소스  |설명  |
|---------|---------|
|[Office 365 관리 Api 개요](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)     |Office 365 관리 활동 API는 Office 365 및 Azure Active Directory 활동 로그에서 다양 한 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 제공 합니다.         |
|[Office 365 관리 Api 시작 하기](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |Office 365 관리 API는 Azure AD를 사용 하 여 응용 프로그램에서 Office 365 데이터에 액세스 하는 데 필요한 인증 서비스를 제공 합니다. 이 문서에서 설명 하는 단계에 따라 설정 합니다.          |
|[Office 365 관리 활동 API 참조](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |Office 365 관리 활동 API를 사용 하 여 Office 365 및 Azure AD 활동 로그에서 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 검색할 수 있습니다. 이 문서를 읽으면 작동 방식에 대해 자세히 알아볼 수 있습니다.        |
|[Office 365 관리 활동 API 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |Office 365 관리 활동 API를 통해 사용할 수 있는 특정 종류의 데이터에 대 한 자세한 내용은 [일반 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) 및 [Office 365 ATP 및 위협 조사 및 응답 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) 개요를 확인 하세요.         |

## <a name="next-steps"></a>다음 단계

[알림에 대해 자세히 알아보기](alert-policies.md)

[Office 365에서 제공 된 악성 전자 메일을 수동으로 찾아서 조사](investigate-malicious-email-that-was-delivered.md)

[Microsoft Defender ATP의 AIR에 대해 자세히 알아보기](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

[Microsoft 365 로드맵를 방문 하 여 곧 제공 되는 항목을 확인 하 고 롤아웃](https://www.microsoft.com/microsoft-365/roadmap?filters=)