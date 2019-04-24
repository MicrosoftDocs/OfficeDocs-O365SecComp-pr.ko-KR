---
title: 배달 된 악성 전자 메일 찾기 및 조사 (Office 365 위협 조사 및 응답)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
ms.audience: ITPro
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
ms.openlocfilehash: d19833a5d2acf69b79cca7e58c5796d967337c9f
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254654"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a>배달 된 악성 전자 메일 찾기 및 조사 (Office 365 Advanced Threat Protection 요금제 2)

[Office 365 Advanced Threat Protection 계획 2](office-365-ti.md) 에서는 사용자에 게 위험을 주는 작업을 조사 하 여 조직을 보호 하기 위한 조치를 취할 수 있습니다. 예를 들어 조직의 보안 팀에 속한 경우 사용자에 게 배달 된 의심 스러운 전자 메일 메시지를 찾아서 조사할 수 있습니다. [위협 탐색기](get-started-with-ti.md#threat-explorer)를 사용 하 여이 작업을 수행할 수 있습니다.
  
> [!IMPORTANT]
> office 365 위협 인텔리전스는 이제 추가 위협 방지 기능과 함께 office 365 Advanced Threat protection 계획 2를 제공 합니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.
  
## <a name="before-you-begin"></a>시작 하기 전에

다음 조건이 충족되었는지 확인하세요.
  
- 조직에 [office 365 Advanced Threat Protection 계획 2](office-365-ti.md) 가 있고 [비즈니스용 office 365에서 사용자에 게 라이선스를 할당](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc)합니다.
    
- [Office 365](turn-audit-log-search-on-or-off.md) 조직에 대해 감사 로깅이 설정 됩니다. 
    
- 조직에 스팸 방지, 맬웨어 방지, 피싱 방지 등을 위한 정책이 정의 되어 있습니다. [Office 365 Advanced Threat Protection](office-365-atp.md)를 참조 하세요.
    
- Office 365 전역 관리자 이거나 보안 관리자 또는 보안 &amp; 및 준수 센터에서 할당 된 검색 및 제거 역할 중 하나를 사용할 수 있습니다. [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.
    
## <a name="dealing-with-suspicious-emails"></a>의심 스러운 전자 메일 처리

악의적인 공격자가 사용자에 게 메일을 보내 자격 증명을 피싱 회사 비밀에 대 한 액세스를 시도할 수 있습니다. 이를 방지 하기 위해 Exchange Online protection 및 Advanced threat protection을 포함 하 여 Office 365에서 제공 하는 위협 방지 서비스를 사용 해야 합니다. 그러나 공격자가 url을 포함 하는 사용자에 게 메일을 보낼 수 있으며 나중에 해당 url이 악성 콘텐츠를 가리키도록 설정 합니다 (맬웨어 등). 또는 조직에 있는 사용자가 손상 된 경우, 해당 사용자가 손상 된 경우 공격자가 해당 계정을 사용 하 여 회사의 다른 사용자에 게 전자 메일을 보낼 수 있습니다. 이러한 두 시나리오를 정리 하는 과정에서 사용자의 받은 편지함에서 전자 메일 메시지를 제거할 수 있습니다. 이와 같은 경우에는 위협 탐색기를 통해 이러한 전자 메일 메시지를 찾아서 제거할 수 있습니다.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>배달 된 의심 스러운 전자 메일 찾기 및 삭제

> [!TIP]
> [위협 탐색기](get-started-with-ti.md#threat-explorer) (탐색기 라고도 함)은 메시지 찾기 및 삭제, 악의적인 전자 메일 보낸 사람에 대 한 IP 주소 식별, 추가 조사를 위해 인시던트 시작 등의 다양 한 용도로 사용할 수 있는 강력한 보고서입니다. 다음 절차에서는 Explorer를 사용 하 여 받는 사람 사서함에서 악성 전자 메일을 찾아서 삭제 하는 방법에 대해 중점적으로 설명 합니다 
  
1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다. 이렇게 하면 보안 &amp; 및 준수 센터로 이동 합니다. 
    
2. 왼쪽 탐색 영역에서 **Threat management** \> **Explorer**를 선택 합니다.
    
3. 보기 메뉴에서 **모든 전자 메일**을 선택 합니다.<br/>![보기 메뉴를 사용 하 여 전자 메일 및 콘텐츠 보고서 중에서 선택](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. **배달**하거나 **알 수**없거나 **정크 메일에 배달**된 것과 같이 보고서에 표시 되는 레이블을 확인 합니다.<br/>![모든 전자 메일에 대 한 데이터를 표시 하는 위협 탐색기](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>조직에 대 한 전자 메일 메시지에 대해 수행 된 작업에 따라 추가 레이블 (예: **차단** 또는 **교체**)이 표시 될 수 있습니다.
    
5. 사용자의 받은 편지 함으로 끝난 전자 메일만 표시 되도록 보고서에 **배달** 을 선택 합니다.<br/>!["정크로 배달"을 클릭 하면 보기에서 해당 데이터가 제거 됨](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. 차트 아래에서 차트 아래에 있는 **전자 메일** 목록을 검토 합니다.<br/>![차트 아래에서 검색 된 전자 메일 메시지의 목록 보기](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. 목록에서 항목을 선택 하 여 해당 전자 메일 메시지에 대 한 세부 정보를 확인 합니다. 예를 들어 제목 줄을 클릭 하 여 보낸 사람, 받는 사람, 첨부 파일 및 기타 유사한 전자 메일 메시지에 대 한 정보를 볼 수 있습니다.<br/>![세부 정보 및 첨부 파일을 포함 하 여 항목에 대 한 추가 정보를 볼 수 있습니다.](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. 전자 메일 메시지에 대 한 정보를 확인 한 후에는 목록에서 하나 이상의 항목을 선택 하 여 **+ 작업**을 활성화 합니다.
    
9. **+ 작업** 목록을 사용 하 여 **지운 편지함으로 이동** 등의 작업을 적용 합니다. 이 경우 선택한 메시지가 받는 사람의 사서함에서 삭제 됩니다.<br/>![하나 이상의 전자 메일 메시지를 선택 하면 사용 가능한 여러 작업 중에서 선택할 수 있습니다.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>관련 항목

[Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)
  
[Office 365에서 위협 으로부터 보호](protect-against-threats.md)
  
[Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)
  

