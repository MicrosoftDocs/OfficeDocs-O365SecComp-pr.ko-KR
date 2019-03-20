---
title: 격리 FAQ
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
ms.collection:
- M365-security-compliance
description: 이 항목에서는 호스팅되는 격리에 대한 질문과 대답을 제공합니다.
ms.openlocfilehash: 9a9673b3360a9a8b6bf837e09b49aca7a38e2172
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693267"
---
# <a name="quarantine-faq"></a>격리 FAQ

이 항목에서는 호스팅되는 격리에 대한 질문과 대답을 제공합니다. 대답은 Microsoft Exchange Online 및 Exchange Online Protection 고객에게 해당됩니다.
  
 **q. 격리에서 맬웨어 격리 메시지를 관리 하려면 어떻게 해야 하나요?**
  
격리로 전송 된 메시지를 &amp; 보고 작업 하려면 보안 준수 센터를 사용 해야 합니다 (맬웨어 포함). 자세한 내용은 [Office 365에서 전자 메일 메시지 격리](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b)를 참조 하세요.
  
 **질문. 스팸으로 격리된 메시지를 격리로 보내도록 서비스를 구성하려면 어떻게 해야 합니까?**
  
대답. 기본적으로 콘텐츠가 필터링된 메시지는 받는 사람의 정크 메일 폴더로 전송됩니다. 그러나 관리자는 스팸으로 격리된 메시지를 격리로 대신 보내도록 콘텐츠 필터 정책을 구성할 수 있습니다. 콘텐츠가 필터링 된 메시지에 대해 수행할 수 있는 다양 한 작업에 대 한 자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하십시오.
  
 **질문. 서비스에서 스팸으로 격리된 메시지를 관리자 및 최종 사용자가 관리할 수 있는 기능을 제공합니까?**
  
A. 관리자는 EAC(Exchange 관리 센터)에서 격리된 모든 전자 메일 메시지에 대한 세부 정보를 검색하고 볼 수 있습니다. 메시지를 찾은 후 특정 사용자에게 릴리스하고 원하는 경우 Microsoft 스팸 분석 팀에 가양성(정크 메일 아님)으로 보고할 수 있습니다. 자세한 내용은 [관리자로 격리된 메시지 찾기 및 릴리스](find-and-release-quarantined-messages-as-an-administrator.md)을 참조하세요.
  
최종 사용자는 다음을 통해 스팸 격리된 메시지를 관리할 수 있습니다. 
  
- 스팸 격리 사용자 인터페이스입니다. 자세한 내용은 [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx)을 참조하세요.
        
 **Q. 최종 사용자에게 스팸 격리소에 대한 액세스 권한을 부여하려면 어떻게 합니까?**
  
대답. 최종 사용자 스팸 격리에 액세스 하려면 최종 사용자에 게 유효한 Office 365 사용자 ID 및 암호가 있어야 합니다. 온-프레미스 사서함을 보호 하는 EOP 고객은 디렉터리 동기화 또는 EAC를 통해 만든 유효한 전자 메일 사용자 여야 합니다. 사용자를 관리 하는 방법에 대 한 자세한 내용은 EOP 관리자가 [EOP에서 메일 사용자 관리](eop/manage-mail-users-in-eop.md)를 참조할 수 있습니다. EOP 독립 실행형 고객의 경우 디렉터리 동기화 및 디렉터리 기반 Edge 차단을 사용 하는 것이 좋습니다. 자세한 내용은 [디렉터리 기반 Edge 차단을 사용 하 여 잘못 된 받는 사람에 게 보낸 메시지 거부](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)를 참조 하세요.
  
 **질문. 스팸 이외의 항목을 격리로 보낼 수 있습니까?**
  
대답. 메일 흐름 규칙 (전송 규칙이 라고도 함)과 일치 하는 메시지는 구성 된 작업 인 경우에도 관리자 격리로 보낼 수 있습니다. 최종 사용자 격리는 스팸 전용입니다.
  
 **질문. 메시지는 얼마 동안 격리에 보관됩니까?**
  
대답. 기본적으로 스팸 격리 메시지는 30 일 동안 격리 된 상태로 유지 되 고, 메일 흐름 규칙과 일치 하는 격리 된 메시지는 7 일 동안 격리 됩니다. 이 기간 후에 메시지는 삭제되며 검색할 수 없게 됩니다. 메일 흐름 규칙과 일치 하는 격리 된 메시지의 보존 기간은 구성할 수 없습니다. 그렇지만 스팸 격리 메시지의 보존 기간은 콘텐츠 필터 정책의 **스팸 보존 기간(일)** 설정을 통해 줄일 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.
  
 **Q. 한 번에 2개 이상의 격리된 메시지를 해제하거나 보고할 수 있습니까?**
  
A. 한 번에 여러 메시지를 릴리스 하거나 보고 하는 기능은 현재 EAC 또는 최종 사용자 스팸 격리에서 제공 되지 않습니다. 그렇지만 관리자는 이 작업을 수행하는 원격 Windows PowerShell 스크립트를 만들 수 있습니다. [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet을 사용하여 메시지를 검색하고 [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet을 사용하여 메시지를 해제할 수 있습니다. 
  
 **질문. 격리된 메시지 검색 시 와일드카드가 지원됩니까? 특정 도메인에 대해 격리된 메시지를 검색할 수 있습니까?**
  
대답. Exchange 관리 센터에서 검색 조건을 지정할 때는 와일드카드가 지원되지 않습니다. 예를 들어 보낸 사람을 검색할 때는 전체 전자 메일 주소를 지정해야 합니다.
  
원격 Windows PowerShell을 통해 관리자는 [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet을 지정하여 contoso.com과 같은 특정 도메인에 대해 격리된 메시지를 검색할 수 있습니다. 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

이 결과는 [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet으로 전달될 수 있습니다. 메시지를 모든 받는 사람에게 릴리스하려면 -ReleaseToAll 매개 변수를 포함합니다. 메시지를 릴리스한 후에는 다시 릴리스할 수 없습니다. 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```


