---
title: 스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: EOP 고객의 기본 스팸 방지 작업은 스팸 메시지를 받는 사람의 정크 메일 폴더로 이동 하는 것입니다. 온-프레미스 사서함에서이 작업을 수행 하려면 EOP에서 추가한 스팸 헤더를 검색 하도록 온-프레미스에 지 또는 허브 서버에서 Exchange 전송 규칙을 구성 해야 합니다. 이러한 전송 규칙은 각 사서함의 정크 메일 폴더로 스팸을 이동 하도록 set-organizationconfig cmdlet의 SclJunkThreshold 속성에서 사용 하는 SCL (스팸 지 수)을 설정 합니다.
ms.openlocfilehash: d0ae9637ce95a1a8f0d4d241b3aef928c84ba3fa
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221028"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인

> [!IMPORTANT]
> 이 항목은 하이브리드 배포에서 온-프레미스에 사서함을 호스트 하는 EOP (Exchange Online Protection) 고객 에게만 적용 됩니다. 해당 사서함이 Office 365에서 완전히 호스트 되는 Exchange Online 고객은 이러한 명령을 실행할 필요가 없습니다. 
  
EOP 고객의 기본 스팸 방지 작업은 스팸 메시지를 받는 사람의 정크 메일 폴더로 이동 하는 것입니다. 온-프레미스 사서함에서이 작업을 수행 하려면 EOP에서 추가한 스팸 헤더를 검색 하도록 온-프레미스에 지 또는 허브 서버에서 Exchange 전송 규칙을 구성 해야 합니다. 이러한 전송 규칙은 각 사서함의 정크 메일 폴더로 스팸을 이동 하도록 set-organizationconfig cmdlet의 SclJunkThreshold 속성에서 사용 하는 SCL (스팸 지 수)을 설정 합니다. 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>Windows PowerShell을 사용 하 여 스팸이 정크 메일 폴더로 이동 되도록 전송 규칙을 추가 하려면

1. 온-프레미스 exchange server에 대 한 Exchange 관리 셸에 액세스 합니다. 온-프레미스 exchange 조직에서 Exchange 관리 셸을 여는 방법에 대 한 자세한 내용은 **open the Shell**을 참조 하십시오.
    
2. 다음 명령을 실행하여 콘텐츠가 필터링된 스팸 메시지를 정크 메일 폴더로 라우팅합니다.
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    여기서 _nameforrule_ 은 새 규칙의 이름 (예: JunkContentFilteredMail)입니다. 
    
3. 다음 명령을 실행하여 스팸으로 표시된 메시지를 콘텐츠 필터에 도달하기 전에 정크 메일 폴더로 라우팅합니다.
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    여기서 _nameforrule_ 은 새 규칙의 이름 (예: JunkMailBeforeReachingContentFilter)입니다. 
    
4. 다음 명령을 실행 하 여 **보낸 사람 차단** 목록과 같은 스팸 필터 정책의 차단 목록에 있는 보낸 사람의 메시지가 정크 메일 폴더로 라우팅됩니다. 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    여기서 _nameforrule_ 은 새 규칙의 이름 (예: JunkMailInSenderBlockList)입니다. 
    
**정크 메일 폴더로 메시지 이동** 작업을 사용 하지 않으려면 Exchange 관리 센터에서 콘텐츠 필터 정책에서 다른 작업을 선택 하면 됩니다. 자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요. 메시지 헤더의 이러한 필드에 대 한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조 하십시오.
  
## <a name="see-also"></a>참고 항목

[new-transportrule cmdlet](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

