---
title: Office 365의 ATP 피싱 방지 기능
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
ms.collection:
- M365-security-compliance
description: ATP 피싱 방지는 Office 365 Advanced Threat Protection의 일부입니다. ATP 바이러스 방지는 상품 및 스피어 피싱 공격에 대 한 보호를 제공 하기 위해 들어오는 메시지에 대 한 가장 검색 알고리즘과 함께 기계 학습 모델 집합을 적용 합니다. 모든 메시지는 다양 한 사용자 및 도메인 가장 공격을 방지 하는 데 사용 되는 고급 알고리즘 집합과 함께 피싱 메시지를 검색 하기 위해 교육 된 다양 한 기계 학습 모델 집합의 영향을 받습니다.
ms.openlocfilehash: 25e7845ab7d16b0766636006f2c55debfee2f9f9
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276378"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>Office 365의 ATP 피싱 방지 기능

ATP 피싱 방지는 [Office 365 Advanced Threat Protection](office-365-atp.md)의 일부입니다. ATP 바이러스 방지는 상품 및 스피어 피싱 공격에 대 한 보호를 제공 하기 위해 들어오는 메시지에 대 한 가장 검색 알고리즘과 함께 기계 학습 모델 집합을 적용 합니다. 모든 메시지는 다양 한 사용자 및 도메인 가장 공격을 방지 하는 데 사용 되는 고급 알고리즘 집합과 함께 피싱 메시지를 검색 하기 위해 교육 된 다양 한 기계 학습 모델 집합의 영향을 받습니다. ATP 피싱 방지는 Office 365 글로벌 또는 보안 관리자가 설정한 정책에 따라 조직을 보호 합니다.
  
자세한 내용은 [Office 365에서 피싱 방지 정책 설정을](set-up-anti-phishing-policies.md)참조 하세요.
  
> [!NOTE]
> ATP 피싱 방지 기능은 [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 Enterprise E5, office 365 교육용 A5 등 구독에 포함 된 Advanced Threat Protection 에서만 사용할 수 있습니다. 조직에서 office 365 ATP를 포함 하지 않는 office 365 구독을 사용 하는 경우 ATP를 추가 기능으로 구매할 수 있습니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.

## <a name="how-atp-anti-phishing-works"></a>ATP 피싱 방지 작동 방식

ATP 피싱 방지는 메시지가 피싱 일 수 있음을 나타내는 표시기에 대 한 수신 메시지를 확인 합니다. 사용자에 게 ATP 정책 (안전한 첨부 파일, 안전한 링크 또는 피싱 방지)이 포함 될 때마다 메시지를 분석 하는 여러 기계 학습 모델이 수신 메시지를 평가 하 여 정책이 메시지에 적용 되는지와 적절 한 작업을 수행 하는지 확인 합니다. 구성 된 정책을 기반으로 수행 됩니다.
  
ATP 피싱 방지를 통해 Office 365 전역 관리자 또는 보안 관리자는 사용자 또는 도메인의 가장을 포함 하 여 피싱 공격 으로부터 보호 하는 정책을 정의할 수 있습니다. 또는 둘 다 있습니다. Office 365 전역 관리자 또는 보안 관리자는 사용자와 도메인이 고정 된 사용자 또는 도메인 목록을 사용 하거나 사서함 인텔리전스를 사용 하 여 가장 공격 으로부터 보호 해야 하는 정책 내에서 정의 합니다. 사서함 인텔리전스는 사용자의 전자 메일 습관과 개인 연락처를 상세하게 이해 합니다. ATP는 각 개별 사용자가 조직 내부 및 외부에 있는 다른 사용자와 통신 하 고 이러한 관계의 맵을 구축 하는 방법을 학습 합니다. 이 맵을 사용 하면 ATP가 올바른 메시지를 가장으로 식별 하는 방법에 대 한 자세한 정보를 파악할 수 있습니다.
  
ATP 피싱 방지 정책은 조직의 특정 사용자 또는 그룹 집합 또는 전체 도메인 또는 모든 사용자 지정 도메인에 적용할 수 있습니다. 자세한 내용은 [Office 365에서 피싱 방지 정책 설정을](set-up-anti-phishing-policies.md)참조 하세요.
  
## <a name="how-to-get-atp-anti-phishing"></a>ATP가 피싱 방지를 받는 방법

ATP 피싱 방지 기능은 [Advanced Threat Protection](office-365-atp.md)의 일부입니다. 그러나 ATP 피싱 방지 보호는 피싱 방지 정책이 정의 된 경우에 적용 됩니다. 예를 들어 가장 기반 정책 중 하나를 예로 들 수 있습니다. [Office 365에서 피싱 방지 정책 설정을](set-up-anti-phishing-policies.md)참조 하세요.
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>ATP 피싱 방지가 현재 위치에 있는지 여부를 확인 하는 방법

보호 기능을 적용 하려면 ATP 피싱 방지 정책을 정의 해야 합니다. 먼저이를 확인 하 여 보호가 적용 되었는지 확인 합니다.

또한 보고서를 사용 하 여 조직에서 서비스가 작동 하는 방식을 표시할 수 있습니다. 자세한 내용은 [Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)를 참조 하세요.

atp 피싱 방지 기계 학습 모델을 특정 사용자에 대해 활성화 하려면 해당 사용자는 정의 된 [ATP 안전한 첨부 파일](atp-safe-attachments.md), [atp 안전한 링크](atp-safe-links.md)또는 atp 피싱 방지 정책의 일부 여야 합니다. 

다음 표에서는 몇 가지 예제 시나리오에 대해 설명 합니다. 이러한 각 예제에서 조직은 Advanced Threat Protection이 포함 된 Office 365 Enterprise E5를 사용 하 고 있습니다.
  
|**시나리오 예**|**이 경우 ATP가 피싱 방지를 적용 하나요?**|
|:-----|:-----|
|Pat 조직에 Office 365 Enterprise E5가 있지만, atp 안전한 첨부 파일, atp 안전한 링크 또는 atp advanced 피싱에 대 한 정책을 정의 하지 않은 경우|아니요. 이 기능을 사용할 수 있지만 atp 기계 학습 모델이 작동 하려면 하나 이상의 atp 정책을 정의 해야 합니다. 가장의 경우 ATP 피싱 방지 정책도 적절 하 게 수행 해야 합니다.|
|Lee은 Contoso의 판매 부서에 있는 직원입니다. Lee의 조직에는 재무 직원 에게만 적용 되는 ATP 피싱 방지 정책이 포함 되어 있습니다.|아니요. 이 경우 ATP 피싱 방지 (시스템 모델 및 가장 보호)는 재무 직원에 게 적용 되지만 영업 부서를 비롯 한 다른 직원은이를 사용 하지 않습니다.|
|어제 Jean 조직의 Office 365 관리자는 모든 직원에 게 적용 되는 ATP 피싱 방지 정책을 설정 합니다. 지금까지 Jean에서는 정책에 포함 된 가장을 포함 하는 전자 메일 메시지를 받습니다.|예. 이 예에서는 Jean에 Advanced Threat Protection 라이선스가 있고 Jean을 포함 하는 ATP 피싱 방지 정책이 정의 되어 있습니다. 일반적으로 새 정책이 데이터 센터 전체에 적용 되는 데 약 30 분이 걸립니다. 이 경우에는 요일이 전달 된 것 이므로 정책이 적용 되어야 합니다.|

## <a name="related-topics"></a>관련 항목

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Office 365의 피싱 방지 보호 기능](anti-phishing-protection.md)
  
[Office 365에서 피싱 방지 정책 설정](set-up-anti-phishing-policies.md)
  
[Office 365 ATP 안전한 링크](atp-safe-links.md)
  
[Office 365에서 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)
  
[Office 365의 ATP 안전한 첨부 파일](atp-safe-attachments.md)
  
[Office 365에서 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)
  
[Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)
