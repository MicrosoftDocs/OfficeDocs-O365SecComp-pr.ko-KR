---
title: 격리 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
description: 이 항목에서는 호스팅되는 격리에 대한 질문과 대답을 제공합니다.
ms.openlocfilehash: 6aebeadc5155cbdb8cbeeb73e29c8b8cb0d53767
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027085"
---
# <a name="quarantine-faq"></a>격리 FAQ

이 항목에서는 호스팅되는 격리에 대한 질문과 대답을 제공합니다. 대답은 Microsoft Exchange Online 및 Exchange Online Protection 고객에게 해당됩니다.
  
 **질문: 격리에서 맬웨어 격리 된 메시지를 관리 하려면는 어떻게**
  
보안을 사용 하 여 필요한 &amp; 보고 맬웨어를 포함 하기 때문에 격리로 전송 된 메시지와 함께 작업을 수행 하기 위해 준수 센터입니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 격리를](https://support.office.com/en-US/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b)참조 하십시오.
  
 **질문. 스팸으로 격리된 메시지를 격리로 보내도록 서비스를 구성하려면 어떻게 해야 합니까?**
  
A. 기본적으로 콘텐츠 필터링 된 메시지의 받는 사람에 게 정크 메일 폴더로 전송 됩니다. 그러나 관리자는 대신 격리로 스팸 격리 된 메시지를 보낼 콘텐츠 필터 정책을 구성할 수 있습니다. 콘텐츠 필터링 된 메시지에서 수행할 수 있는 다른 작업에 대 한 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오.
  
 **질문. 서비스에서 스팸으로 격리된 메시지를 관리자 및 최종 사용자가 관리할 수 있는 기능을 제공합니까?**
  
A. 관리자는 EAC(Exchange 관리 센터)에서 격리된 모든 전자 메일 메시지에 대한 세부 정보를 검색하고 볼 수 있습니다. 메시지를 찾은 후 특정 사용자에게 릴리스하고 원하는 경우 Microsoft 스팸 분석 팀에 가양성(정크 메일 아님)으로 보고할 수 있습니다. 자세한 내용은 [관리자로 격리된 메시지 찾기 및 릴리스](find-and-release-quarantined-messages-as-an-administrator.md)을 참조하세요.
  
최종 사용자는 다음을 통해 스팸 격리된 메시지를 관리할 수 있습니다. 
  
- 스팸 격리 사용자 인터페이스입니다. 자세한 내용은 [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx)을 참조하세요.
        
 **Q. 최종 사용자에게 스팸 격리소에 대한 액세스 권한을 부여하려면 어떻게 합니까?**
  
A. 하려면 최종 사용자 스팸 격리에 액세스, 최종 사용자에 게 유효한 Office 365 사용자 ID와 암호가 있어야 합니다. 온-프레미스 사서함을 보호 하는 EOP 고객 디렉터리 동기화 또는 EAC를 통해 만든 유효한 전자 메일 사용자 여야 합니다. 사용자를 관리 하는 방법에 대 한 자세한 내용은 EOP 관리자의 [EOP의 메일 사용자 관리를](eop/manage-mail-users-in-eop.md)참조할 수 있습니다. EOP 독립 실행형 고객을 위한 것이 좋습니다 디렉터리 동기화를 사용 하 고 디렉터리 기반 Edge 차단; 사용 하도록 설정 자세한 내용은 다음을 [사용 하 여 디렉터리 기반 Edge 차단 거부 잘못 된 받는 사람에 게 보낸 메시지를](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)을 참조 하십시오.
  
 **질문. 스팸 이외의 항목을 격리로 보낼 수 있습니까?**
  
대답. 전송 규칙과 일치하는 메시지도 관리자 격리로 보낼 수 있습니다(격리로 보내기가 구성된 작업인 경우). 최종 사용자 격리는 스팸 전용입니다.
  
 **질문. 메시지는 얼마 동안 격리에 보관됩니까?**
  
A. 기본적으로 스팸 격리 메시지를 전송 규칙과 일치 하는 격리 된 메시지는 7 일이에 대 한 사용자를 격리에 보관 되는 동안 15 일 동안 격리에 보관 됩니다. 이 기간 후 메시지가 삭제 되 고 검색할 수 없습니다. 전송 규칙과 일치 하는 격리 된 메시지에 대 한 보존 기간을 구성할 수는 없습니다. 그러나 콘텐츠 필터 정책에서 **보관 스팸 (일)에 대 한** 설정을 통해 스팸 격리 된 메시지에 대 한 보존 기간을 낮출 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오.
  
 **Q. 한 번에 2개 이상의 격리된 메시지를 해제하거나 보고할 수 있습니까?**
  
A.를 해제 하거나 한번에 여러 메시지를 보고 기능을 EAC 또는 최종 사용자 스팸 격리에서 현재 사용할 수 없는 경우 그러나 관리자가이 작업을 수행 하기 위해 원격 Windows PowerShell 스크립트를 만들 수 있습니다. 메시지를 검색 하려면 [Get-quarantinemessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet 및 해제 하는 [릴리스 QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet을 사용 합니다. 
  
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


