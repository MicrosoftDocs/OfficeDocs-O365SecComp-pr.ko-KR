---
title: Office 365의 ATP 피싱 방지 기능
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
description: ATP 피싱 방지 Office 365 고급 위협 보호의 일부분으로 제공 됩니다. ATP 피싱 방지 보호 (영문) 상품 및 창 피싱 공격을 제공 하기 위해 받는 메시지를 가장 감지 알고리즘와 함께 컴퓨터 학습 모델의 집합을 적용 합니다. 모든 메시지는 다양 한 사용자 및 도메인 가장 공격 으로부터 보호 하기 위해 사용 되는 고급 알고리즘 집합이 함께 피싱 메시지를 검색 교육을 받은 컴퓨터 학습 모델의 다양 한 집합에 따라 달라 집니다. ATP 피싱 방지 보호 하는 조직에 따라 Office 365 전역 또는 보안 관리자가 설정 된 정책에 있습니다.
ms.openlocfilehash: e7bb4c4a28109c40bf745a25c9c8366558cf2ac7
ms.sourcegitcommit: ba2175e394d0cb9f8ede9206aabb44b5b677fa0a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2018
ms.locfileid: "25496892"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>Office 365의 ATP 피싱 방지 기능

ATP 피싱 방지 [Office 365 고급 위협 보호](https://technet.microsoft.com/en-us/library/exchange-online-advanced-threat-protection-service-description.aspx)의 일부분으로 제공 됩니다. ATP 피싱 방지 보호 (영문) 상품 및 창 피싱 공격을 제공 하기 위해 받는 메시지를 가장 감지 알고리즘와 함께 컴퓨터 학습 모델의 집합을 적용 합니다. 모든 메시지는 다양 한 사용자 및 도메인 가장 공격 으로부터 보호 하기 위해 사용 되는 고급 알고리즘 집합이 함께 피싱 메시지를 검색 교육을 받은 컴퓨터 학습 모델의 다양 한 집합에 따라 달라 집니다. ATP 피싱 방지 보호 하는 조직에 따라 Office 365 전역 또는 보안 관리자가 설정 된 정책에 있습니다.
  
자세한 내용은 [Office 365의 피싱 방지 정책 설정](set-up-anti-phishing-policies.md)을 참조 합니다.
  
> [!NOTE]
> ATP 피싱 방지는 에서만 고급 위협 보호, Office 365 Enterprise e 5에서 사용할 수 있는 사용할 수 있습니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 고급 위협 보호 추가 기능으로 구입할 수 있습니다. (전역 관리자도 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 계획 옵션에 대 한 자세한 내용은 [비즈니스 계획에 대 한 모든 Office 365 비교](https://go.microsoft.com/fwlink/?linkid=844053)를 참조 하십시오. 
    
## <a name="how-atp-anti-phishing-works"></a>ATP 피싱 방지의 작동 방식
<a name="Howantiphishworks"> </a>

ATP 피싱 방지 메시지 피싱 될 수 있다는 지표에 대 한 들어오는 메시지를 확인 합니다. 들어오는 메시지 하는 경우 메시지에 적용 하는 정책 및 적절 한 작업을 결정 하는 메시지를 분석 하는 모델을 학습 하는 여러 컴퓨터에 의해 계산 되는 ATP 정책 (안전한 첨부 파일, 안전한 링크 또는 피싱 방지)에 포함 되는 사용자 때마다 구성 된 정책에 따라를 수행 합니다.
  
ATP 피싱 방지 Office 365 전역 관리자 또는 보안 관리자 사용자 또는 도메인의 가장을 포함 하는 피싱 공격 으로부터 보호 기능을 제공 하는 정책을 정의할 수 있습니다. (또는 둘 모두)입니다. Office 365 전역 관리자 또는 보안 관리자가 정의 사용자 및 도메인 중 하나를 사용 하 여 가장 공격 으로부터 보호 해야 정책 내에서 사용자 또는 도메인의 또는 사서함 인텔리전스를 사용 하 여 고정된 목록입니다. 사서함 인텔리전스는 사용자의 전자 메일 거 및 개인 연락처에 대 한 고급 이해 합니다. ATP 각 개별 사용자는 조직 내부 및 외부 다른 사용자와 통신 하 고 이러한 관계의 맵을 빌드하 하는 방법을 알아냅니다. 이 맵을 오른쪽 메시지 가장으로 식별 된 확인 하는 방법에 대 한 자세한 내용은 이해 하는 ATP 수 있습니다.
  
ATP 피싱 방지 정책 또는 전체 도메인 또는 사용자 지정 도메인의 모든 사용자 또는 그룹에 조직 전체에서 특정 집합에 적용할 수 있습니다. 자세한 내용은 [Office 365의 피싱 방지 정책 설정](set-up-anti-phishing-policies.md)을 참조 합니다.
  
## <a name="how-to-get-atp-anti-phishing"></a>ATP 피싱 방지 하는 방법
<a name="Howtogetantiphish"> </a>

ATP 피싱 방지는 Office 365 Enterprise e 5에 포함 된 고급 위협 보호의 일부입니다. 고급 위협 보호 Office 365 Enterprise E1 또는 Office 365 Enterprise E3 추가 기능으로 구입할 수 있습니다. 계획 옵션에 대 한 자세한 내용은 [비즈니스 계획에 대 한 모든 Office 365 비교](https://go.microsoft.com/fwlink/?linkid=844053)를 참조 하십시오.
  
ATP 피싱 방지 때는 피싱 방지 정책 적용 하는 가장 기반 정책 설정 등 합니다. ( [Office 365의 피싱 방지 정책 설정](set-up-anti-phishing-policies.md)참조).
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>ATP 피싱 방지 전체에서 인지 확인 하는 방법
<a name="IsantiphishOn"> </a>

ATP 피싱 방지 정책 활성 상태 여야 하는 보호 기능에 대 한 순서로 정의 해야 합니다. ATP 피싱 방지 컴퓨터 학습 모델에 대 한 사용자에 대 한 활성화 될, 해당 사용자 정의 된 안전한 첨부 파일, 안전한 링크 또는 피싱 방지 정책의 일부 여야 합니다. 다음 표에서 몇가지 예제 시나리오를 설명합니다. 이 예제에서는 각 조직 고급 위협 보호를 포함 하는 Office 365 Enterprise E5 사용 중입니다.
  
|**시나리오 예**|**ATP 피싱 방지이 경우에 적용지 않습니다?**|
|:-----|:-----|
|Pat의 조직에 Office 365 Enterprise E5, 있지만 아무도 자가 ATP 안전한 첨부 파일을 아직 피싱 고급 ATP 또는 ATP 안전한 링크에 대 한 정책을 정의 합니다.|아니요. 기능을 사용할 수 있지만 적어도 하나의 ATP 정책이 작동 하도록 모델 학습 ATP 컴퓨터에 대 한 순서 대로 정의 되어야 합니다. 가장을 위한 ATP 피싱 방지 정책에는 전체에서 수도 있어야 합니다.|
|Lee contoso 영업 부서의 직원입니다. 백화점 ㈜의 조직에 재무 직원 들의 경우에 적용 되는 위치에는 ATP 피싱 방지 정책이 있습니다.|아니요. 이 경우 ATP 피싱 방지 (컴퓨터 모델 및 가장 보호) 재무 직원에 게 적용 됩니다 하지만 다른 직원, 영업 부서를 포함 하 여 선택할 수도 있습니다.|
|어제, Jean의 조직에서 Office 365 관리자가 모든 직원에 게 적용 되는 ATP 피싱 방지 정책을 설정 합니다. 지금 바로 이전 Jean 정책에 의해 설명 하는 가장 포함 된 전자 메일 메시지를 받았습니다.|예입니다. 이 예제에서는 Jean 라이선스 고급 위협 보호에 대 한 있으며 Jean를 포함 하는 ATP 피싱 방지 정책을 정의 되었습니다. 일반적으로 데이터 센터; 적용 하려면 새 정책에 대 한 약 30 분 걸리는 하루에이 경우을 통과 하므로 정책을 적용 해야 합니다.|
   
## <a name="related-topics"></a>관련 항목
<a name="IsantiphishOn"> </a>

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Office 365의 피싱 방지 보호 기능](anti-phishing-protection.md)
  
[Office 365의 피싱 방지 정책 설정](set-up-anti-phishing-policies.md)
  
[Office 365의 ATP 안전한 링크](atp-safe-links.md)
  
[Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)
  
[Office 365의 ATP 안전한 첨부 파일](atp-safe-attachments.md)
  
[Office 365의 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)
  
[고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)
  

