---
title: Office 365에서 스팸 메일을 줄이는 방법
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 06/07/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: 07824c51-2c45-4005-8596-03c0d7c4ff2a
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- Strat_O365_IP
description: Office 365에서 스팸 및 정크 메일을 줄이는 데 도움이 되는 가장 일반적인 방법을 알아봅니다.
ms.openlocfilehash: d99b5e1452c60be713f0f4cfbab965d30eeeb8ef
ms.sourcegitcommit: bc25ea19c0b6d318751eadc4f27902b0054d5e2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/01/2019
ms.locfileid: "36054710"
---
# <a name="how-to-reduce-spam-email-in-office-365"></a>Office 365에서 스팸 메일을 줄이는 방법

 **Office 365에서 스팸이 너무 많이 늘어나나요? 그렇다면 다음을 수행하세요.**
  
필터 개선을 위해서 [보고서 메시지 추가 기능 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 사용하여 거짓 부정 메시지를 보고하는 것을 강력히 권장합니다. 또한, [제출 탐색기](admin-submission.md)를 사용하여 메시지를 제출할 수도 있습니다.

> [!TIP]
> 이 메시지가 정크 메일이며 정크 메일 폴더에 있으면 문제가 아닙니다. 어떤 사서함에도 들어 있지 않으면 메시지를 격리하도록 스팸 방지 정책을 변경해야 합니다. 메시지 격리에 대한 자세한 내용은 [Office 365에서 전자 메일 메시지 격리](quarantine-email-messages.md)에서 찾을 수 있습니다.

## <a name="fixing-allowed-spam"></a>허용된 스팸 해결

잘못된 구성으로 인해 고객의 받은 편지함으로 정크 메일이 들어오는 경우가 많습니다. 가장 일반적인 경우는 메일 흐름 규칙(전송 규칙이라고도 함)의 도메인이 필터를 무시하도록 구성하거나 사용자 도메인이 허용/수신 허용 - 보낸 사람 목록에 포함되는 경우입니다. 이러한 메시지는 스팸 필터링에 걸리지 않고 받은 편지함에 들어올 수 있으므로 바람직하지 않습니다.  

## <a name="solutions-to-other-common-causes-of-getting-too-much-spam"></a>스팸을 너무 많이 증가하는 다른 일반적인 원인에 대한 해결 방법

스팸이 너무 많이 증가하지 않도록 하기 위해 EOP(Exchange Online Protection)는 관리자가 몇 가지 작업을 완료하도록 요구합니다. Office 365 테넌트의 관리자가 아니며 스팸이 너무 많이 발생하는 경우 관리자와 함께 이러한 문제를 해결할 수 있습니다. 그렇지 않은 경우 사용자 작업으로 건너뛸 수 있습니다.
  
### <a name="for-admins"></a>관리자

- **Office 365를 가리키도록 DNS 레코드 지정** EOP를 통해 최상의 보호를 제공하려면 모든 도메인의 MX(메일 교환기)가 Office 365만 가리켜야 합니다. [DNS 레코드를 관리할 때 Office 365용 DNS 레코드 만들기](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)를 참조하세요.
    
- **모든 사서함에서 정크 메일 규칙 사용** 기본적으로 스팸 필터링 작업은 **정크 메일 폴더로 메시지 이동**으로 설정되어 있습니다. 이것이 기본 설정 및 현재 스팸 정책 작업인 경우 각 사서함에서 [정크 메일 규칙도 사용되도록 설정](https://support.office.com/ko-KR/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)되어야 합니다. 이를 확인하려면 하나 이상의 사서함에 대해 Get-MailboxJunkEmailConfiguration cmdlet을 실행할 수 있습니다. 예를 들어, Get-MailboxJunkEmailConfiguration -Identity \* | Where {$_.Enabled -eq $false}를 실행하여 모든 사서함에 대해 이러한 설정을 확인할 수 있습니다.
    
    결과에서 Enable 속성이 True로 설정되어야 합니다. False로 설정된 경우 다음과 같이 Set-MailboxJunkEmailConfiguration을 실행하여 True로 변경할 수 있습니다. Set-MailboxJunkEmailConfiguration -Identity $values.UserPrincipalName -Enabled $true.
    
- **온-프레미스 Exchange Server에서 메일 흐름 규칙 만들기** Exchange Online Protection을 사용하지만 사서함 이 온-프레미스 Exchange 서버에 있는 경우 온-프레미스 Exchange Server에서 몇 가지 메일 흐름 규칙을 만들어야 합니다. [EOP 전용 지침](https://docs.microsoft.com/previous-versions/exchange-server/exchange-150/jj900470(v=exchg.150))을 참조하세요.
    
- **대량 전자 메일을 스팸으로 표시** 대량 전자 메일은 사용자가 등록했을 수 있지만 여전히 원치 않을 수 있는 전자 메일입니다. 메시지 헤더에서 X-Microsoft-Antispam 헤더의 BCL(대량 불만 수준) 속성을 찾으세요. BCL 값이 스팸 필터에 설정된 임계값보다 낮으면 이러한 유형의 대량 메시지를 스팸으로 대신 표시하도록 임계값을 조정할 수 있습니다. 사용자마다 [대량 전자 메일을 처리하는 방법](https://docs.microsoft.com/ko-KR/office365/SecurityCompliance/bulk-complaint-level-values)에 대해 다른 임계값 및 기본 설정을 사용할 수 있습니다. 사용자 기본 설정마다 다른 정책 또는 규칙을 만들 수 있습니다. 
    
- **보낸 사람 즉시 차단** 보낸 사람을 즉시 차단해야 하는 경우, 전자 메일 주소, 도메인 또는 IP 주소에 따라 차단할 수 있습니다. [Office 365에서 차단할 보낸 사람 목록 만들기](create-block-sender-lists-in-office-365.md)를 참조하세요. 최종 사용자의 허용 목록에 있는 항목은 관리자가 설정한 차단에 따라 재정의될 수 있습니다.
    
- **사용자용 보고서 메시지 추가 기능 설정** [사용자용 보고서 메시지 추가 기능을 사용하도록 설정](enable-the-report-message-add-in.md)하는 것을 강력히 권장합니다.

- **[제출 탐색기](admin-submission.md)사용** 관리자는 파일이나 네트워크 메시지 ID, URL, Office 365에서 Microsoft가 검색한 파일을 사용하여 전자 메일을 보낼 수 있습니다.  관리자는 사용자가 보내는 피드백을 보고, 패턴을 사용하여 문제를 발생시킬 수 있는 설정을 조정할 수도 있습니다.

- **[DKIM](use-dkim-to-validate-outbound-email.md)** 을 사용해 모든 아웃 바운드 메시지에 서명하여 도메인 및 테넌트의 보안을 강화하십시오.
 > [!TIP]
> DKIM을 활성화한 후에는 DKIM 및 SPF가 올바르게 작동할 경우 이 레코드가 유효성을 검사하므로 [DMARC](use-dkim-to-validate-outbound-email.md)를 활성화해야 하고, O365가 개인 및 공개 대칭 키를 관리하므로 일반적으로 스푸핑 전자 메일에 서명이 없습니다.
    
### <a name="for-users"></a>사용자

- **정크 메일 규칙 사용 및 허용 목록 확인** 정크 메일 작업 규칙이 사용되도록 설정되어 있는지와 보낸 사람 또는 보낸 사람 도메인이 개인 허용 목록에서 우회되도록 설정되어 있지 않은지 확인합니다. 이러한 설정에 액세스하는 가장 좋은 방법은 [차단 또는 허용(정크 전자 메일 설정)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46)을 사용하는 것입니다. 여기에서 보낸 사람의 전자 메일 주소 또는 도메인을 차단 하도록 선택할 수도 있습니다.
    
- **Microsoft에 스팸 신고** [보고서 메시지 추가 기능 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 사용하여 Microsoft에 스팸 메시지를 보고합니다.
       
- **대량 전자 메일에서 구독 취소** 사용자가 등록한 메시지이지만(뉴스레터, 제품 알림 등) 신뢰할 수 있는 원본에서 구독 취소 링크가 포함된 경우 구독을 간단히 취소할 수 있습니다. Office 365는 일반적으로 메시지를 스팸으로 처리하지 않습니다. 보낸 사람을 차단하도록 선택할 수도 있고, 관리자에게 모든 대량 메일을 스팸으로 처리하도록 설정 변경을 요청할 수도 있습니다.
