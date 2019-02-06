---
title: Office 365 ATP 안전한 첨부 정책 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/05/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
description: 조직에서 전자 메일의 악의적인 파일 보호 하기 위해 안전한 첨부 파일 정책을 정의 합니다.
ms.openlocfilehash: 229f5eb4ec1af4302f724151f599bd33b15055e1
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741121"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a>Office 365 ATP 안전한 첨부 정책 설정

사용자가 정기적으로 보내기, 수신, 및 문서, 프레젠테이션, 스프레드시트, 등의 첨부 파일을 공유 합니다. 항상 쉽게 첨부 파일이 안전 또는 악의적인 전자 메일 메시지를 확인 하 여 방금 인지 여부를 알 수 있는 것은 아닙니다. 하며 원하는 마지막으로 성능을 저하 시키는 조직에 대 한 프로그램을 통과해 서, 악의적인 첨부 파일입니다. 놓기만 [Office 365 고급 위협 보호](office-365-atp.md) (ATP) 데 도움이 됩니다. 조직은 저작권법과 공격 으로부터 안전 하지 않은 전자 메일 첨부 파일을 보장 하기 [ATP 안전한 첨부 파일](atp-safe-attachments.md) 정책을 설정할 수 있습니다. 
  
## <a name="what-to-do"></a>수행할 작업 
  
1. [필수 구성 요소를 검토 합니다.](#review-the-prerequisites)
    
2. [ATP 안전한 첨부 파일 정책 설정](#set-up-an-atp-safe-attachments-policy)
    
3. [ATP 안전한 첨부 파일 정책 옵션에 알아보기](#learn-about-atp-safe-attachments-policy-options)
    
## <a name="step-1-review-the-prerequisites"></a>1 단계: 필수 구성 요소를 검토 합니다.

- 조직에 [Office 365 고급 위협 보호](office-365-atp.md)있는지 확인 합니다.
    
- 필요한 사용 권한이 있는지 확인 합니다. ATP 정책, 정의 (또는 편집)를 할당 되어 있어야 다음 표에 설명 된 역할 중 하나: <br>

    |역할  |Where/방법 할당  |
    |---------|---------|
    |Office 365 전역 관리자 |Office 365를 구매 하 여를 로그인 하는 사람 이름은 기본적으로 전역 admin입니다. (자세한 내용은 [Office 365에 대 한 관리자 역할](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 참조 하십시오.)         |
    |Office 365 보안 관리자 |관리 센터 ([https://aka.ms/admincenter](https://aka.ms/admincenter))|
    |Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
- [ATP 안전한 첨부 파일 정책 옵션에 대 한 설명](#learn-about-atp-safe-attachments-policy-options) (이 문서의). 모니터] 또는 [바꾸기 옵션 등의 일부 옵션 첨부 파일 검사 하는 동안 전자 메일의 약간 지연 될 수 있습니다. 메시지 지연을 방지 하려면 [동적 배달 및 미리 보기](dynamic-delivery-and-previewing.md)를 사용 하는 것이 좋습니다.
    
- 모든 Office 365 데이터 센터에 분산 하 여 신규 또는 업데이트 된 정책에 대 한 최대 30 분을 허용 합니다.
    
## <a name="step-2-set-up-or-edit-an-atp-safe-attachments-policy"></a>2 단계: 설정 (또는 편집) ATP 안전한 첨부 파일 정책
  
1. 이동 [https://protection.office.com](https://protection.office.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다. 
    
2. Office 365 보안에서 &amp; 준수 센터 왼쪽된 탐색 창의 **위협 관리** **정책** 을 선택 \> **안전한 첨부 파일**입니다.
    
3. **SharePoint, OneDrive 및 Microsoft 팀의 ATP를 설정**하는 것이 표시를 하는 경우에이 옵션을 선택 하는 것이 좋습니다. 이렇게 하면 Office 365 환경에 대 한 [SharePoint, OneDrive 및 팀이 Microsoft Office 365 고급 위협 보호](atp-for-spo-odb-and-teams.md) 활성화 됩니다. 
    
4. **새로 만들기** 를 선택 (새로 만들기 단추 유사한 더하기 기호 ( **+**)) 정책 만들기를 시작 합니다.
    
5. 이름, 설명 및 정책에 대 한 설정을 지정 합니다.<br/><br/>**예제:** 모든 사람의 메시지를 즉시 배달 하 고 검사는 자신이 후 첨부 파일을 다음가 다시 연결 하는 "지연 없음" 이라는 정책을 설정 하려면 다음 설정을 지정할 수 있습니다. 
    
      - **이름** 상자에 없는 지연을 입력 합니다.
    
      - **설명** 상자에 검색 한 후 바로 제공 메시지와 첨부 파일이 다시 연결 같은 대 한 설명을 입력 합니다.
    
      - 응답 섹션에서 **동적 배달** 옵션을 선택 합니다. ([동적 배달 하 고 ATP 안전한 첨부 파일 미리 보기에 대 한 자세한 설명](dynamic-delivery-and-previewing.md)입니다.)
    
      - **리디렉션 첨부 파일** 섹션에서 리디렉션을 사용 하도록 설정 하 고 Office 365 전역 관리자, 보안 관리자 또는 보안 분석가 악의적인 첨부 파일을 조사 하는 사용자의 전자 메일 주소를 입력 하는 옵션을 선택 합니다. 
    
      - **적용 된** 섹션에서 **받는 사람 도메인은**선택 하 고 도메인을 선택 합니다. **추가**선택 하 고 **확인**을 선택 합니다.
    
6. **Save(저장)** 를 선택합니다.
    
조직에 대 한 여러 ATP 안전한 첨부 파일 정책 설정을 것이 좋습니다. 이러한 정책은 **ATP 안전한 첨부 파일** 페이지에 나열 된 순서 대로 적용 됩니다. 정책을 정의 했거나 편집한 후 허용에 대 한 최소 30 분의 전체 Microsoft 데이터 센터에서 적용 하려면 정책을 합니다. 
  
## <a name="step-3-learn-about-atp-safe-attachments-policy-options"></a>3 단계: ATP 안전한 첨부 파일 정책 옵션에 알아보기

ATP 안전한 첨부 파일 정책에 설정 하면 모니터, 차단, 바꾸기, 동적 배달 및 등을 비롯 한 여러 옵션 중에서 선택 합니다. 이러한 옵션 기능을 수행 하는 방법에 대 한 궁금할 하는 경우 다음 표에 각 하 고 영향을 주기 합니다.
  
|**옵션**|**영향**|**사용 하려는 경우:**|
|:-----|:-----|:-----|
|**Off** <br/> |맬웨어에 대 한 첨부 파일을 검색 하지 않습니다.  <br/> 메시지 배달이 연기 하지 않습니다.  <br/> |내부 보낸사람, 스캐너, 팩스, 또는 알려진, 좋은 첨부 파일을 보내기만 됩니다 스마트 호스트에 대 한 검색을 해제합니다  <br/> 내부 메일을 라우팅하도록 불필요 한 지연을 방지합니다  <br/> **이 옵션은 대부분의 사용자에 대 한 권장 되지 않습니다. 내부 보낸 사람의 소규모 그룹에 대해 ATP 안전한 첨부 파일 검사를 해제 수 있습니다.**           |
|**모니터링** <br/> |첨부 파일이 있는 메시지를 전달 하 고 검색 된 맬웨어와 수행 하는 작업을 추적합니다  <br/> |조직에서 검색 된 맬웨어 이동 하는 위치를 참조 하십시오.  <br/> |
|**블록** <br/> |시계에서 검색 된 맬웨어 첨부 파일이 있는 메시지를 차단합니다.  <br/> [Office 365의 격리](manage-quarantined-messages-and-files.md) 여기에서 보안 관리자 또는 분석가 수를 검토 하 고 릴리스 (또는 삭제) 해당 메시지를 검색 된 맬웨어가 포함 된 메시지를 보냅니다.  <br/> 향후 메시지와 첨부 파일을 자동으로 차단  <br/> |조직 동일한 맬웨어 첨부 파일을 사용 하 여 반복 해 서 공격 으로부터 보호  <br/> |
|**바꾸기** <br/> |제거는 맬웨어 첨부 파일 검색  <br/> 첨부 파일이 제거 된 받는 사람에 게 알리는  <br/> [Office 365의 격리](manage-quarantined-messages-and-files.md) 여기에서 보안 관리자 또는 분석가 수를 검토 하 고 릴리스 (또는 삭제) 해당 메시지를 검색 된 맬웨어가 포함 된 메시지를 보냅니다.  <br/> |받는 사람에 게 검색 된 맬웨어로 인해 제거 된 첨부 파일에 대 한 가시성을 발생 시킵니다.  <br/> |
|**동적 배달** <br/> |메시지를 바로 전달  <br/> 검색 완료 되며 없는 맬웨어가 탐지 되는 경우 첨부 파일을 다음가 다시 연결 될 때까지 개체 틀 파일 첨부 파일을 바꿉니다.  <br/> 대부분의 Pdf 및 Office에 대 한 기능을 미리 보는 첨부 파일 포함 파일 검사 중  <br/> 검색 된 맬웨어 있는 메시지를 격리 여기에서 보안 관리자 또는 분석가 수를 검토 하 고 릴리스 (또는 삭제) 해당 메시지를 보냅니다.  <br/> [동적 배달 하 고 ATP 안전한 첨부 파일 미리 보기에 대 한 설명](dynamic-delivery-and-previewing.md) <br/> |악의적인 파일에서 받는 사람을 보호 하는 동안 메시지 지연을 방지합니다  <br/> 받는 사람에 게 검사를 수행 하는 동안 안전 모드에서 첨부 파일 미리 보기를 사용 하도록 설정  <br/> |
|**리디렉션 사용** <br/> |적용 하는 모니터, 차단 또는 바꾸기 옵션을 선택 하는 경우  <br/> 보안 관리자 또는 분석가 조사할 수의 첨부 파일을 지정 된 전자 메일 주소를 보냅니다.  <br/> |보안 관리자 및 분석가 의심 스러운 첨부 파일 조사를 사용 하도록 설정  <br/> |
   
## <a name="next-steps"></a>다음 단계

ATP 안전한 첨부 파일 정책이 설정 되어, 되 면 조직에 대 한 보고서를 확인 하 여 ATP가 작동 하는 방법을 확인할 수 있습니다. 자세한 내용은 다음 리소스를 참조 하십시오.
- [Office 365 고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)
- [탐색기를 사용 하 여 보안에서 &amp; 준수 센터](use-explorer-in-security-and-compliance.md)

ATP 연결 되는 새로운 기능을 세워야 합니다. [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) 를 방문 하 고 [ATP에 추가 되는 새로운 기능](office-365-atp.md#new-features-are-continually-being-added-to-atp)에 대해 알아봅니다.
 