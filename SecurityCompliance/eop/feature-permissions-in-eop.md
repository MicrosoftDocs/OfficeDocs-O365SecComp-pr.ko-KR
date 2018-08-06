---
title: EOP의 기능 사용 권한
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/30/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 34674847-a6b7-4a7e-9eaa-b64f22bc150d
description: Microsoft EOP(Exchange Online Protection)를 관리하기 위한 작업을 수행하는 데 필요한 사용 권한은 관리 대상 기능에 따라 다릅니다.
ms.openlocfilehash: fe39403e60664b0340f01070ccec22b674b5bc62
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027475"
---
# <a name="feature-permissions-in-eop"></a>EOP의 기능 사용 권한

Microsoft EOP(Exchange Online Protection)를 관리하기 위한 작업을 수행하는 데 필요한 사용 권한은 관리 대상 기능에 따라 다릅니다. 
  
EOP를 설정하려면 Office 365 전역 관리자 또는 Exchange 회사 관리자(조직 관리 역할 그룹)여야 합니다.
  
## <a name="exchange-online-protection-permissions"></a>Exchange Online Protection 사용 권한

EOP 기능을 관리하는 데 필요한 사용 권한을 확인하려면 다음 표를 참조하세요. 하나의 기능에 둘 이상의 역할 그룹이 나열되는 경우 기능을 사용할 역할 그룹 중 하나만 할당되어야 합니다.
  
|**기능**|**필요한 권한**|
|:-----|:-----|
|맬웨어 방지  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|스팸 방지  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|메일 흐름 규칙  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Records Management](http://technet.microsoft.com/library/0e0c95ce-6109-4591-b86d-c6cfd44d21f5.aspx) <br/> |
|도메인  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> |
|고급 위협 보호 ATP)  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Office 365 커넥터  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> |
|메시지 추적  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> |
|조직 구성  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> |
|격리  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|사용자, 연락처 및 역할 그룹  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|메일 그룹 및 보안 그룹  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|보고서 보기  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) - 사용자가 메일 보호 보고서에 액세스할 수 있습니다.  <br/> [View-Only Recipients](http://technet.microsoft.com/library/37e66b92-81d3-412f-b7a9-e1bb8cbeb468.aspx) - 사용자가 메일 보호 보고서에 액세스할 수 있습니다.  <br/> [Compliance Management](http://technet.microsoft.com/library/b91b23a4-e9c7-4bd0-9ee3-ec5cb498da15.aspx) - 사용자가 메일 보호 보고서 및 구독에 DLP 기능이 있는 경우 DLP(데이터 손실 방지) 보고서에 액세스할 수 있습니다.  <br/> |
   

