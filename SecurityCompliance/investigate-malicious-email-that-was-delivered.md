---
title: 찾기 및 악의적인 전자 메일 (Office 365 위협 인텔리전스) 지정 된 배달 하 게 조사
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 8/6/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
description: 위협 인텔리전스를 사용 하 여를 찾아 악의적인 전자 메일을 조사 하는 방법에 알아봅니다.
ms.openlocfilehash: b6d4f8a5d1fcfce4461b91796b1264f94d1eb4d1
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014920"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a>찾기 및 악의적인 전자 메일 (Office 365 위협 인텔리전스) 지정 된 배달 하 게 조사

[Office 365 위협 인텔리전스](office-365-ti.md) 를 사용 하면 위험에 사용자를 배치 하 고 조직을 보호 하는 작업을 수행 하는 활동을 조사할 수 있습니다. 등 조직의 보안 팀의 일부인 경우 찾기 및 의심 스러운 전자 메일 메시지를 사용자에 게 배달 된를 조사할 수 있습니다. [위협 탐색기](get-started-with-ti.md#threat-explorer)를 사용 하 여이 수행할 수 있습니다.
  
> [!NOTE]
> Office 365 위협 인텔리전스 Office 365 Enterprise e 5에서 제공 됩니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 Office 365 위협 인텔리전스 추가 기능으로 구입할 수 있습니다. (전역 관리자는 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다. 
  
## <a name="before-you-begin"></a>시작 하기 전에...

다음 조건이 충족되었는지 확인하세요.
  
- 조직이 [Office 365 위협 인텔리전스](office-365-ti.md) 및 [비즈니스를 위한 Office 365에서 사용자에 게 라이선스를 할당](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc)합니다.
    
- 조직에 대 한 [office 365 감사 로깅](turn-audit-log-search-on-or-off.md) 기능이 켜 집니다. 
    
- 조직에 스팸 방지, 맬웨어 방지, 피싱 방지 등에 대 한 정의 된 정책입니다. 참조 [관리 Office 365 보안에서 위협 &amp; 준수 센터](threat-management.md)합니다.
    
- 사용자가 Office 365 전역 관리자, 있어야 하거나, 보안 관리자 또는 보안에서 할당 된 검색 및 삭제 역할 &amp; 준수 센터입니다. 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.
    
## <a name="dealing-with-suspicious-emails"></a>의심 스러운 전자 메일이 처리

악의적인 공격자가 자격 증명 시도 하는 사용자 및 phish에 게 메일을 보내는 하 고 기업 비밀 내용에 액세스할 수 있습니다! 이러한 문제를 방지 하기 위해 Exchange Online Protection 및 고급 위협 보호를 포함 하 여 Office 365에서 제공 하는 위협 보호 서비스를 사용 해야 합니다. 그러나 공격자 수 URL이 포함 된 사용자에 게 메일을 보낼 하 고 나중에 해당 URL 지점 (맬웨어 등) 악의적인 콘텐츠를 확인 하는 경우에 경우가 있습니다. 또는 있습니다 것을 느낄 수 너무 늦게 조직에서 사용자가 손상 된 하 고 해당 사용자가 손상 된 동안 공격자 계정을 사용 하는 해당 회사에 다른 사용자에 게 전자 메일을 보낼 수 있습니다. 이러한 시나리오 모두를 정리 하 고의 일부로 사용자의 받은 편지함에서 전자 메일 메시지를 제거 하는 것이 좋습니다. 다음과 같은 상황에서 검색 하 고 해당 전자 메일 메시지를 제거할 위협 탐색기를 활용할 수 있습니다!
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>찾기 및 지정 된 배달 하는 의심 스러운 전자 메일을 삭제 합니다.

> [!TIP]
> [위협 탐색기](get-started-with-ti.md#threat-explorer) (탐색기 라고도 함) 강력한 보고서는 찾기 (영문) 및 메시지를 삭제 한 악의적인 전자 메일 보낸 사람의 IP 주소를 식별 하 또는 자세한 조사를 위해 인시던트를 시작 등의 여러 용도로 사용할 수 있습니다. 다음 절차는 탐색기를 사용 하 여 검색 하 고 악의적인 전자 메일 받는 사람 사서함에서 삭제할에 중점을 둡니다. 
  
1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. 이렇게 하면 보안 &amp; 준수 센터입니다. 
    
2. 왼쪽 탐색 영역에서 **위협 관리** 를 선택 \> **탐색기**입니다.
    
3. 보기 메뉴에서 **모든 전자 메일**을 선택 합니다.<br/>![보기 메뉴를 사용 하 여 전자 메일 및 콘텐츠 보고서 중 하나를 선택합니다](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. 예: **배달 된**, **알 수 없는**또는 **정크에 게 배달**보고서에 표시 되는 레이블 알 수 있습니다.<br/>![모든 전자 메일에 대 한 데이터를 표시 하는 위협 탐색기](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(조직에 대 한 전자 메일 메시지에서 작성 하는 작업에 따라 볼 수 있습니다 다른 레이블, 예: **차단 됨** 또는 **대체 되었습니다**.)
    
5. 보고서에서 사용자의 받은 편지함에는 결국 하는 전자 메일만 볼 수 있는 **전달 됨** 을 선택 합니다.<br/>!["정크에 전달"를 클릭 하면 보기에서 해당 데이터 제거](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. 다음은 차트 아래 차트 아래에 있는 **전자 메일** 목록을 검토 합니다.<br/>![다음은 차트 아래 검색 된 전자 메일 메시지의 목록 보기](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. 목록에서 해당 전자 메일 메시지에 대 한 자세한 정보를 보려면 항목을 선택 합니다. 예, 보낸사람, 받는 사람, 첨부 파일 및 기타 유사한 전자 메일 메시지에 대 한 정보를 보려면 제목줄 클릭 수 있습니다.<br/>![세부 정보 및 모든 첨부 파일을 포함 하 여 항목에 대 한 추가 정보를 볼 수 있습니다.](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. 전자 메일 메시지에 대 한 정보를 검토 한 후 **+ 작업을**활성화 하려면 목록에서 하나 이상의 항목을 선택 합니다.
    
9. **+ 작업** 목록을 사용 하 여 항목 **삭제를 이동** 하는 등의 작업을 적용 합니다. 선택한 메시지를 받는 사람의 사서함에서 삭제 됩니다.<br/>![하나 이상의 전자 메일 메시지를 선택 하면 여러 사용 가능한 작업에서 선택할 수 있습니다.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>관련 항목

[Office 365 위협 인텔리전스](office-365-ti.md)
  
[Office 365에서 위협으로부터 보호](protect-against-threats.md)
  
[Office 365 고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)
  

