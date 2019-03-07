---
title: DLP 정책 권장 시작
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/7/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
description: 이 통찰력 기반 권장 사항은 조직에서 DLP 정책 적용 범위에 가능한 간격이 있을 때 사용자에 게이를 알리는 방식으로 중요 한 콘텐츠를 저장 하 고 Office 365에서 공유할 때 안전 하 게 유지 하는 데 도움이 됩니다. 문서에 가장 일반적인 유형의 중요 한 주요 정보가 포함 되어 있지만 &amp; DLP 정책에 의해 보호 되지 않는 경우에는 보안 및 준수 센터의 홈 페이지에서이 권장 사항을 확인할 수 있습니다.
ms.openlocfilehash: aabd1e6b3ce8ea4754192bd7b6f80262d9e83cf7
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455120"
---
# <a name="get-started-with-dlp-policy-recommendations"></a>DLP 정책 권장 시작

이 통찰력 기반 권장 사항은 조직에서 DLP 정책 적용 범위에 가능한 간격이 있을 때 사용자에 게이를 알리는 방식으로 중요 한 콘텐츠를 저장 하 고 Office 365에서 공유할 때 안전 하 게 유지 하는 데 도움이 됩니다. 문서에 가장 일반적인 유형의 중요 한 **** 주요 정보가 포함 되어 있지만 &amp; DLP (데이터 손실 방지) 정책으로 보호 되지 않는 경우에는 보안 및 준수 센터의 홈 페이지에이 권장 사항이 표시 됩니다. 
  
이 위젯을 사용 하 여 한 번에 사용자 지정 된 dlp 정책을 빠르게 만들 수 있으며,이 dlp 정책을 만든 후에는 완전히 사용자 지정이 가능 합니다. 처음에는 권장 사항이 표시 되지 않으면 **권장** 섹션의 아래쪽에서 **+ 자세히** 를 클릭 해 보세요. 
  
![보호 되지 않는 중요 한 정보 라는 위젯](media/91bc04d2-6eff-4294-8b73-b2d56d26ffc4.png)
  
## <a name="create-the-recommended-dlp-policy"></a>권장 DLP 정책 만들기

위젯에 보호 되지 않은 중요 한 정보가 표시 되 면 아래쪽에서 **시작** 을 선택 하 여 DLP 정책을 빠르게 만듭니다. 
  
중요 한 정보를 보호 하기 위해이 DLP 정책은 다음과 같습니다.
  
- 보호 되지 않는 중요 한 정보 유형 중 하나를 포함 하는 Exchange, SharePoint 및 OneDrive의 콘텐츠가 조직 외부의 사용자와 공유 되는 경우를 감지 합니다.
    
- 조직 외부의 사용자와 콘텐츠를 공유한 사용자를 추적할 수 있도록 자세한 활동 보고서를 생성 합니다. [dlp 보고서](view-the-dlp-reports.md) 및 [감사 로그 데이터](search-the-audit-log-in-security-and-compliance.md) (여기서 **활동** = **DLP**)를 사용 하 여이 정보를 볼 수 있습니다.
    
또한 다음과 같이 DLP 정책을 사용할 수도 있습니다.
  
- 사용자가 조직 외부의 사용자와 많은 중요 한 정보를 공유 하는 경우 문제 보고서 전자 메일을 보냅니다.
    
- 다른 사용자를 전자 메일 문제 보고서에 추가 합니다.
    
- 정책 팁을 표시 하 고이 중요 한 정보를 조직 외부의 사용자와 공유 하려고 할 때 사용자에 게 전자 메일 알림을 보냅니다. 이러한 옵션에 대 한 자세한 내용은 [DLP 정책에 대 한 전자 메일 알림 보내기 및 정책 팁 보기](use-notifications-and-policy-tips.md)를 참조 하세요.
    
나중에 이러한 옵션을 변경 하려는 경우에는 DLP 정책이 만들어진 후에 해당 정책을 편집할 수 있습니다. 예를 들어, 사용자가 첫 번째 위치에서 중요 한 정보를 포함 하는 콘텐츠를 공유 하지 못하도록 차단 하 여 정책을 보다 제한적으로 만들 수 있습니다-다음 섹션을 참조 하세요.
  
![보호 되지 않는 중요 한 정보 라는 위젯의 설정](media/b6106cbd-1bed-4582-aaef-b678de470c9b.png)
  
## <a name="edit-the-recommended-dlp-policy"></a>권장 DLP 정책 편집

위젯을 사용 하 여 DLP 정책을 만든 후에는 보안 &amp; 및 준수 센터의 **정책** 페이지에서 **데이터 손실 방지** 에 해당 정책이 표시 됩니다. 
  
기본적으로 **중요 한 정보를 공유 하려면 정책을 System 권장 정책**이라고 합니다. 이 정책은 처음부터 직접 만든 DLP 정책과 동일한 방법으로 완전히 사용자 지정할 수 있습니다. 예를 들어 widget을 사용할 때 문제 보고서와 정책 팁을 설정 하지 않기로 결정 한 경우 언제 든 지 정책을 편집 하 고 이러한 옵션을 설정할 수 있습니다.
  
![중요 한 정보를 공유 하기 위한 시스템 권장 정책](media/2fc49f25-ec25-4433-add4-d60f73888f13.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>위젯이 수행 되 고 표시 되지 않는 경우

**보호 되지 않는 중요 정보** 라는 위젯은 &amp; 보안 및 준수 센터 **홈페이지의 홈** 페이지에서 **권장 되** 는 섹션에 표시 됩니다. 
  
이 위젯은 다음과 같은 경우에만 표시 됩니다.
  
- 가장 일반적인 5 가지 유형의 중요 정보 중 하나를 포함 하는 새 문서는 SharePoint 또는 지난 30 일간의 OneDrive에서 검색 됩니다.
    
- 중요 한 정보는 기존 DLP 정책에 의해 보호 되지 않습니다.
    
지속적으로 데이터를 검색 하는 dlp 정책과 달리이 권장 사항은 새 콘텐츠가 업로드 된 후 2 일까지 완료 되어 추천이 표시 될 수 있습니다.
  
마지막으로, 위젯을 사용 하 여 권장 DLP 정책을 만든 후에는 **홈** 페이지에서 위젯이 사라집니다. 
  

