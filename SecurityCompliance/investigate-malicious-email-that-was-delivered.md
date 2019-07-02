---
title: 배달 된 악성 전자 메일 찾기 및 조사 (Office 365 위협 조사 및 응답)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: 위협 조사 및 응답 기능을 사용 하 여 악성 전자 메일을 찾고 조사 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: febcf6704b1ba9dc23bf4e698715fb4b929b998b
ms.sourcegitcommit: d3b2bffa8af5f19d97fe9771068c80705b890e85
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/01/2019
ms.locfileid: "35414808"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a>배달 된 악성 전자 메일 찾기 및 조사 (Office 365 Advanced Threat Protection 요금제 2)

[Office 365 Advanced Threat Protection](office-365-atp.md) 을 사용 하면 사용자에 게 위험을 주는 작업을 조사 하 고 조직을 보호 하기 위한 조치를 취할 수 있습니다. 예를 들어 조직의 보안 팀에 속한 경우 사용자에 게 배달 된 의심 스러운 전자 메일 메시지를 찾아서 조사할 수 있습니다. [위협 탐색기 (또는 실시간 검색)](threat-explorer.md)를 사용 하 여이 작업을 수행할 수 있습니다.
  
## <a name="before-you-begin"></a>시작 하기 전에

다음 조건이 충족되었는지 확인하세요.
  
- 조직에 [Office 365 Advanced Threat Protection](office-365-atp.md) (계획 1 또는 계획 2)이 있고 [사용자에 게 라이선스가 할당 되어](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users)있습니다.
    
- [Office 365](turn-audit-log-search-on-or-off.md) 조직에 대해 감사 로깅이 설정 됩니다. 
    
- 조직에 스팸 방지, 맬웨어 방지, 피싱 방지 등을 위한 정책이 정의 되어 있습니다. [Office 365에서 위협 으로부터 보호를](protect-against-threats.md)참조 하세요.
    
- Office 365 전역 관리자 이거나 보안 관리자 또는 보안 &amp; 및 준수 센터에서 할당 된 검색 및 제거 역할 중 하나를 사용할 수 있습니다. [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.
    
## <a name="dealing-with-suspicious-emails"></a>의심 스러운 전자 메일 처리

악의적인 공격자가 사용자에 게 메일을 보내 자격 증명을 피싱 회사 비밀에 대 한 액세스를 시도할 수 있습니다. 이를 방지 하려면 [Exchange Online protection](eop/exchange-online-protection-overview.md) 및 [Advanced threat protection](office-365-atp.md)을 포함 하 여 Office 365의 위협 보호 서비스를 사용 해야 합니다. 그러나 공격자가 URL을 포함 하는 사용자에 게 메일을 보낼 수 있으며 나중에 해당 URL이 악성 콘텐츠를 가리키도록 설정 합니다 (맬웨어 등). 또는 조직의 사용자가 손상 된 경우, 해당 사용자가 손상 된 경우 공격자가 해당 계정을 사용 하 여 회사의 다른 사용자에 게 전자 메일을 보내는 것을 너무 늦 었을 수 있습니다. 이러한 두 시나리오를 정리 하는 과정에서 사용자의 받은 편지함에서 전자 메일 메시지를 제거할 수 있습니다. 이러한 경우 이러한 전자 메일 메시지를 검색 하 고 제거 하려면 [위협 탐색기 (또는 실시간 검색)](threat-explorer.md) 를 활용할 수 있습니다.

## <a name="where-re-routed-emails-are-located-after-actions-are-taken"></a>다시 라우팅된 전자 메일은 작업을 수행한 후의 위치

위협 탐색기 실시간 검색이 배달 상태 대신 배달 작업 및 배달 위치 필드를 추가 했습니다. 이로 인해 전자 메일이 위치 하는 위치가 더 완벽 하 게 향상 됩니다. 이러한 변경 목표의 일환으로는 보안 Ops 사용자에 게 더 쉽게 사냥을 사용할 수 있지만,이는 네트워크 결과에서 문제 전자 메일의 위치를 한눈에 파악 하는 것입니다.

배달 상태는 이제 다음과 같은 두 개의 열로 나뉩니다.

- **배달 작업** -이 전자 메일의 상태는 무엇입니까?
- **배달 위치** -이 전자 메일의 경로가 어떻게 설정 되었습니까?

배달 작업은 기존 정책 또는 검색으로 인해 전자 메일에 대해 수행 되는 작업입니다. 다음은 전자 메일에 사용할 수 있는 작업입니다.

1. **배달** 됨-전자 메일이 사용자의 받은 편지함 또는 폴더에 배달 되어 사용자가 직접 액세스할 수 있습니다.
2. **Junked** -사용자의 정크 메일 폴더 또는 지운 편지함에 전자 메일이 전송 되 고 사용자가 정크 또는 삭제 된 폴더의 전자 메일에 액세스할 수 있습니다.
3. **차단 됨** -격리 됨, 실패 또는 삭제 된 전자 메일입니다. 사용자가이를 완전히 액세스할 수 없습니다.
4. **대체** 됨-첨부 파일이 악성 인 .txt 파일로 악성 첨부 파일이 교체 되는 모든 전자 메일입니다.
 
배달 위치는 배달 후 실행 되는 정책 및 검색의 결과를 표시 합니다. 배달 작업에 연결 됩니다. 이 필드는 문제 메일을 찾은 경우 수행 되는 작업에 대 한 통찰력을 제공 하기 위해 추가 되었습니다. 배달 위치의 가능한 값은 다음과 같습니다.

1. **받은 편지함 또는 폴더** -전자 메일이 받은 편지함 또는 폴더 (전자 메일 규칙에 따라 다름)에 있습니다.
2. **온-프레미스 또는 external** -사서함이 클라우드에는 없지만 온-프레미스에 있는 경우
3. **정크 폴더** -사용자의 정크 폴더에 있는 전자 메일입니다.
4. **지운 편지함 폴더** -사용자의 지운 편지함 폴더에 있는 전자 메일입니다.
5. **격리** -전자 메일을 격리 하 고 사용자의 사서함에 있지 않습니다.
6. **Failed** – 전자 메일이 사서함에 연결 하지 못했습니다.
7. **삭제** 됨-전자 메일이 메일 흐름의 어딘가에 손실 됩니다.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>배달 된 의심 스러운 전자 메일 찾기 및 삭제

> [!TIP]
> Explorer 라고도 하는 위협 탐색기는 메시지 찾기 및 삭제, 악의적인 전자 메일 보낸 사람에 대 한 IP 주소 식별, 추가 조사를 위해 인시던트 시작 등의 여러 용도로 사용할 수 있는 강력한 보고서입니다. 다음 절차에서는 Explorer를 사용 하 여 받는 사람 사서함에서 악성 전자 메일을 찾아서 삭제 하는 방법에 대해 중점적으로 설명 합니다

이전 배달 상태 필드의 변경 내용을 확인 하려면 (현재 배달 작업 및 배달 위치) 다음을 수행 합니다. 

1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다. 이렇게 하면 보안 &amp; 및 준수 센터로 이동 합니다. 
    
2. 왼쪽 탐색 영역에서 **Threat management** \> **Explorer**를 선택 합니다.
<!--Comment>
![Threat Explorer with Delivery Action and Delivery Location fields.](media/ThreatExFields.PNG)

    
3. In the View menu, choose **All email**.<br/>![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.<br/>![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)
    
5. In the report, choose **Delivered** to view only emails that ended up in users' inboxes.<br/>![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Below the chart, review the **Email** list below the chart.<br/>![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.<br/>![You can view additional information about an item, including details and any attachments](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. After viewing information about email messages, select one or more items in the list to activate **+ Actions**.
    
9. Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.<br/>![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
-->
## <a name="related-topics"></a>관련 항목

[Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)
  
[Office 365에서 위협 으로부터 보호](protect-against-threats.md)
  
[Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)
  

