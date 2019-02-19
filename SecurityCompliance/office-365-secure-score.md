---
title: Office 365 보안 점수
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Office 365에서 조직이 어떻게 보호 되는지 궁금 하십니까? 보안 점수가 여기에 해당 합니다. 보안 점수는 Office 365의 일반 활동 및 보안 설정에 따라 조직의 보안을 분석 하 고 점수를 할당 합니다.
ms.openlocfilehash: cf272869981dd73e1ceb4bd7180cc16acaed0516
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/19/2019
ms.locfileid: "29992362"
---
# <a name="office-365-secure-score"></a>Office 365 보안 점수

**요약** Office 365에서 조직이 어떻게 보호 되는지 궁금 하십니까? 보안 점수가 여기에 해당 합니다. 보안 점수는 Office 365의 일반 활동 및 보안 설정에 따라 조직의 보안을 분석 하 고 점수를 할당 합니다. 이 문서를 읽으면 보안 점수에 대 한 개요를 확인 하 고 사용 하는 방법을 확인할 수 있습니다.
  
## <a name="how-to-get-to-secure-score"></a>보안 점수에 액세스 하는 방법

조직에 [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 business](https://docs.microsoft.com/microsoft-365/business/)또는 Office 365 business Premium이 포함 된 구독이 있고 [필요한 사용 권한이](#required-permissions)있는 경우에는 방문 하 여 조직의 보안 점수를 볼 수 있습니다. [https://securescore.office.com](https://securescore.office.com). 

또는 보안 & 준수 센터 ([https://protection.office.com](https://protection.office.com))를 방문 하 여 현재 점수를 제공 하는 보안 점수 위젯을 찾을 수도 있습니다.

![보안 점수 위젯](media/SecureScoreWidget-o365.png)

위젯에는 보안 점수 대시보드에 대 한 링크가 포함 되어 있습니다.

![보안 점수 대시보드](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a>작업 방법

보안 점수 사용 중인 Office 365 서비스 (예: OneDrive, SharePoint, Exchange)를 결정 하 고 설정 및 작업을 Microsoft에서 설정한 기준에 맞게 비교 합니다. 조직이 보안 모범 사례와 일치 하는 방식에 따라 점수가 부여 됩니다. 또한 조직의 점수를 높이기 위해 수행할 수 있는 단계에 대 한 권장 사항도 제공 됩니다. 
  
![Office 365 보안 점수 도구에 있는 작업 큐](media/SecureScore-ActionsToTake.png)
  
보안 점수는 구매한 서비스에 따라 점수를 계산 합니다. 예를 들어 Exchange online 요금제만 구매한 경우에는 SharePoint online 보안 기능에 대 한 점수가 매겨지지 않습니다. 점수의 분모는 구매한 제품에 적용 되는 컨트롤에 대 한 모든 초기 계획의 합계입니다. 분자는 해당 컨트롤을 완료 하거나 부분적으로 완료 한 모든 컨트롤의 합계입니다.

작업을 확장 하 여 수행 해야 하는 단계, 사용자 로부터 보호 하는 데 도움이 되는 위협 및 권장 사항에 따라 점수가 증가 하는 점수를 확인할 수 있습니다.
  
![Office 365 보안 점수 도구에 확장 된 작업](media/SecureScore-DetailedActionToTake.png)
  
조직의 보안에 대 한 작업의 영향을 확인 하려면 **점수 분석기** 탭을 선택 하 고 기록을 검토 합니다. 
  
![Office 365 보안 점수 도구의 점수 분석기 탭](media/SecureScore-ScoreAnalyzer-7days.png)
  
차트 아래에 범주별 점수 및 작업 목록이 표시 됩니다. 
  
![선택한 데이터 요소를 표시 하는 점수 분석기 탭의 그래프](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
**[점수가 없음]** 으로 레이블이 지정 된 작업은 조직에 대해 수행할 수 있는 것으로, 보안 점수에 연결 되어 있지 않으므로 점수가 매겨지지 않습니다.  

**점수 분석기** 페이지에서 특정 날짜에 대 한 데이터 요소를 클릭 한 다음 아래로 스크롤하여 해당 요일의 완료 및 완료 되지 않은 작업을 확인 하 여 변경 된 내용을 확인 합니다. 점수는 하루에 한 번 계산 됩니다 (1:00 AM PST 기준). 측정 된 작업을 변경 하면 점수가 다음 날에 자동으로 업데이트 됩니다. 변경 내용이 점수에 반영 되는 데 최대 48 시간이 걸릴 수 있습니다.

보안 점수가 위반 되는 정도를 절대적으로 측정 하는 것은 아닙니다. 이는 침해 위험을 오프셋할 수 있는 기능을 채택한 범위를 나타냅니다. 어떤 서비스도 위반 되지 않도록 보장할 수 있으며 보안 점수는 어떤 식으로든 보증으로 해석 되어서는 안 됩니다.
 
## <a name="how-secure-score-helps"></a>보안 점수가 어떻게 도움이 되는가

보안 점수를 사용 하 여 Office 365의 기본 제공 보안 기능을 사용 하 여 조직의 보안을 향상 시킬 수 있습니다 (이미 구매한 반면, 사용자가 알고 있지 않을 수도 있음). 이러한 기능에 대해 자세히 알고 있으면 위협 으로부터 조직을 보호 하기 위해 적절 한 단계를 수행 하는 데 도움이 될 수 있습니다.
  
하지만이 문서에 대 한 단어만 사용 하면 됩니다. 보안 점수를 사용 하는 고객은 해당 점수를 사용 하지 않는 고객 보다 5 배의 시간이 더 증가 한 것으로 나타났습니다. (점수가 증가 하는 것은 조직에서 사용 되는 보안 기능에 해당 합니다.)
  
> [!NOTE]
> 보안 점수가 위반 되는 정도를 절대적으로 측정 하는 것은 아닙니다. 이는 위반 위험을 오프셋할 수 있는 컨트롤을 채택한 범위를 나타냅니다. 어떤 서비스도 위반 되지 않도록 보장할 수 있으며 보안 점수는 어떤 식으로든 보증으로 해석 되어서는 안 됩니다. 
  
## <a name="required-permissions"></a>필요한 사용 권한

보안 점수 대시보드를 보고 사용 하려면 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles)에서 다음 역할 중 하나를 할당 받아야 합니다.
- 전역 관리자
- 대금 청구 관리자
- 사용자 관리자
- 암호 관리자
- 보안 관리자
- 보안 독자
- Exchange 관리자
- SharePoint 관리자

 관리자 역할이 할당 되지 않은 사용자는 보안 점수에 액세스할 수 없습니다.

## <a name="related-topics"></a>관련 항목

[보안 대시보드 개요](security-dashboard.md)

[내가 구독한 것은 무엇인가요?](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
