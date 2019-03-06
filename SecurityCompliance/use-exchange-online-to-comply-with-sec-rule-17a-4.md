---
title: SEC Rule 17a-4를 준수하기 위해 Exchange Online과 보안 및 준수 센터 사용
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: Cohasset Associates는 Exchange Online 및 Security & Compliance Center가 권장대로 구성되어 있으면 CFTC 규칙 1.31 (c) - (d), FINRA 규칙 4511 및 SEC 규칙 17a-4의 관련 저장소 요구 사항을 충족함을 확인했습니다. 평가판을 다운로드할 수 있습니다.
ms.openlocfilehash: b0c2a54aab8f011605a285d4dabfb4091612b17a
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410513"
---
# <a name="use-exchange-online-and-the-security--compliance-center-to-comply-with-sec-rule-17a-4"></a>SEC Rule 17a-4를 준수하기 위해 Exchange Online과 보안 및 준수 센터 사용

조직에서 데이터 보존 을위한 규제 표준을 준수해야하는 경우 Office 365 보안 및 준수 센터는 Exchange Online에서 데이터 수명주기를 관리하는 기능을 제공합니다. 여기에는 데이터를 보존, 감사, 검색 및 내보내기 기능이 포함됩니다. 이러한 기능은 대부분의 조직의 요구를 충족하기에 충분합니다.

그러나 고도로 규제된 산업 분야의 일부 조직은 더 엄격한 규제 요건의 적용을 받습니다. 예를 들어, 은행이나 중개인과 같은 금융 기관은 증권 거래위원회 (SEC)에서 발급한 규칙 17a-4의 적용을 받습니다. 규칙 17a-4는 기록 보존의 기간, 형식, 품질, 가용성 및 책임과 같은 기록 관리의 여러 측면을 포함하여 전자 데이터 저장에 대한 특정 요구 사항을 규정하고 있습니다.

이러한 조직이 보안 및 준수 센터가 Exchange online에 대한 규정 의무, 특히 규칙 17a-4 요구 사항을 충족하기 위해 어떻게 활용될 수 있는지 더 잘 이해할 수 있도록 Cohasset Associates와의 파트너십을 통해 평가를 발표했습니다.

Cohasset은 Exchange Online 및 Security & Compliance Center가 권장대로 구성될 떄 CFTC 규칙 1.31 (c) - (d), FINRA 규칙 4511 및 SEC 규칙 17a-4의 관련 저장소 요구 사항을 충족하는 것을 확인했습니다. 우리는 금융 기관에 대한 기록 보존을 위해 전 세계적으로 가장 규범력이 강한 지침을 제시하기 때문에 이 규칙을 목표로 정했습니다.

## <a name="download-the-cohasset-assessment"></a>Cohasset 평가판 다운로드

[Cohasset 평가판을 여기에서 다운로드](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)할 수 있습니다.

![Cohasset Associates의 다운로드 가능한 평가의 제목 페이지](media/cohasset-associates-assessment.png)

## <a name="this-assessment-is-specific-to-exchange-online"></a>이 평가는 Exchange Online에만 적용됩니다.

이 평가는 Exchange Online에만 적용됩니다. 이 평가에는 SharePoint Online 또는 비즈니스용 OneDrive와 같은 다른 Office 365 서비스는 포함되지 않지만 향후에는 SEC 17a-4와 관련하여 해당 서비스에 대한 지원을 계획하고 있습니다.

Skype 비즈니스 및 팀도 Exchange Online에 데이터를 저장한다는 사실을 이해하는 것이 중요합니다. 따라서 평가는 Skype for Business의 메시지와 팀의 채널 및 채팅 메시지를 포함합니다.

## <a name="using-preservation-lock-is-key-to-the-recommended-configuration"></a>보존 잠금을 사용하는 것이 권장 구성의 핵심입니다.

고도로 규제된 산업은 종종 WORM(write once, read many) 요구사항을 충족시키기 위해 전자통신을 저장해야합니다. WORM 요구 사항은 레코드가 포함되어 있어야 하는 저장소 솔루션을 지정합니다.

- 보존 기간을 줄이면 보존할 수 있지만 보존 기간만 연장됩니다.
- 불변이란 필요한 보존 기간동안 해당 레코드를 덮어 쓰거나 지우거나 변경할 수 없음을 의미합니다.

Exchange Online에서 [보존 정책](retention-policies.md)이 사용자의 사서함에 적용되면 정책의 기준에 따라 모든 사용자의 콘텐츠가 유지됩니다. 실제로 사용자가 전자 메일을 삭제 또는 수정하려고하면 변경되기 전의 전자 메일 복사본이 사용자의 사서함에 있는 숨겨진 안전한 위치에 보존됩니다. 보존 정책을 사용하면 조직에서 전자 통신을 유지할 수 있지만 이러한 정책은 수정될 수 있습니다.

보존 정책에 보존 잠금을 설정하면 정책을 수정할 수 없습니다. 실제로 보존 정책에 보존 잠금이 적용된 후에는 다음과 같은 작업이 제한됩니다.

- 정책의 보존 기간은 단축되지 않고 늘릴 수 있습니다.
- 사용자를 정책에 추가할 수는 있지만 사용자를 제거할 수는 없습니다.
- 보존 정책은 관리자가 삭제할 수 없습니다.

보존 잠금 장치는 SEC 17a-4 규정 요구사항을 충족하는 데 도움이 됩니다.

## <a name="how-to-set-up-preservation-lock"></a>보존 잠금을 설정하는 방법

PowerShell을 사용하여 보존 정책을 잠글 수 있습니다. 자세한 내용은 [ 보관 정책 잠금 ](retention-policies.md#locking-a-retention-policy)을 참조하십시오.

## <a name="known-limitations"></a>알려진 제한

Exchange Online의 몇 가지 제한 사항을 알고 있습니다. 저희은 이를 적극적으로 작업 중이며 2019년 7월에 이러한 시나리오에 대한 지원을 제공할 예정입니다.

- 항목 수준 감사는 Office 365 그룹 사서함에서 사용할 수 없습니다.
- 팀 채팅 및 채널 메시지의 경우 스레드 통신을 사용할 수 없습니다.
- 팀 채팅 및 채널 메시지에 좋아요는 포함되어 있지 않습니다.
