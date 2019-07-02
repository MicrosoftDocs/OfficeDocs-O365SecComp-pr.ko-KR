---
title: Office 365 ATP 안전한 첨부 파일 정책 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
ms.collection:
- M365-security-compliance
description: 안전한 첨부 파일 정책을 정의 하 여 전자 메일의 악의적인 파일 로부터 조직을 보호 합니다.
ms.openlocfilehash: 532a4b6ab2d26506f10adb621a29718a32d52ff6
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34652701"
---
# <a name="set-up-office-365-atp-safe-attachments-policies"></a>Office 365 ATP 안전한 첨부 파일 정책 설정

> [!IMPORTANT]
> 이 문서는 [Office 365 Advanced Threat Protection](office-365-atp.md)을 사용 하는 비즈니스 고객을 위한 것입니다. Outlook에서 안전한 첨부 파일에 대 한 정보를 검색 하는 개인 사용자는 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하십시오.

사용자가 문서, 프레젠테이션, 스프레드시트 등의 첨부 파일을 정기적으로 보내고 받고 공유 합니다. 전자 메일 메시지를 확인 하기만 하면 첨부 파일이 안전한 지 또는 악의적 임을 쉽게 알 수 있습니다. 그리고 마지막으로는 조직에 대 한 wreaking havoc에 액세스할 수 있는 악의적인 첨부 파일이 됩니다. 다행히도 [Office 365 ATP (Advanced Threat Protection](office-365-atp.md) )가 도움이 될 수 있습니다. [ATP 안전한 첨부 파일](atp-safe-attachments.md) 정책을 설정 하 여 조직이 안전 하지 않은 전자 메일 첨부 파일을 통해 공격 으로부터 보호 되도록 할 수 있습니다. 
  
## <a name="what-to-do"></a>수행할 작업 
  
1. 필수 구성 요소 검토
    
2. ATP 안전한 첨부 파일 정책 설정
    
3. ATP 안전한 첨부 파일 정책 옵션에 대 한 자세한 정보
    
## <a name="step-1-review-the-prerequisites"></a>1 단계: 필수 구성 요소 검토

- 조직에 [Office 365 Advanced Threat Protection](office-365-atp.md)이 있는지 확인 합니다.
    
- 필요한 사용 권한이 있는지 확인 합니다. ATP 정책을 정의 하거나 편집 하려면 적절 한 역할이 할당 되어 있어야 합니다. 다음 표에서는 몇 가지 예를 설명 합니다. <br>

    |역할  |할당 된 위치/방법  |
    |---------|---------|
    |Office 365 전역 관리자 |Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.         |
    |보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
    |Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조) |
    
    역할 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.

- [ATP 안전한 첨부 파일 정책 옵션에 대 한 자세한](#step-3-learn-about-atp-safe-attachments-policy-options) 정보 이 문서에서 설명 합니다. 일부 옵션 (예: 모니터 또는 바꾸기 옵션)을 사용할 경우 첨부 파일을 검색 하는 동안 전자 메일이 약간 지연 될 수 있습니다. 메시지 지연을 방지 하려면 [동적 배달 및 미리 보기](dynamic-delivery-and-previewing.md)를 사용 하는 것이 좋습니다.
    
- 새 정책이 나 업데이트 된 정책을 모든 Office 365 데이터 센터에 전파 하는 데 최대 30 분 정도 걸릴 수 있습니다.
    
## <a name="step-2-set-up-or-edit-an-atp-safe-attachments-policy"></a>2 단계: ATP 안전한 첨부 파일 정책 설정 (또는 편집)
  
1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 회사 또는 학교 계정으로 로그인 합니다. 
    
2. Office 365 보안 &amp; 및 준수 센터의 왼쪽 탐색 창에 있는 **위협 관리**에서 **정책** \> **안전한 첨부 파일**을 선택 합니다.
    
3. **SharePoint, OneDrive 및 Microsoft 팀에 대 한 ATP 끄기를**참조 하는 경우이 옵션을 선택 하는 것이 좋습니다. 이를 통해 Office 365 환경에 대 한 [SharePoint, OneDrive 및 Microsoft 팀에 office 365 Advanced Threat Protection](atp-for-spo-odb-and-teams.md) 을 사용 하도록 설정 합니다. 
    
4. 정책 만들기를 시작 하려면 **새로 만들기** (더하기 기호 ( **+**)와 유사)를 선택 합니다.
    
5. 정책에 대 한 이름, 설명 및 설정을 지정 합니다.<br/><br/>**예:** 모든 사람의 메시지를 즉시 배달 하는 "지연 없음" 이라는 정책을 설정 하 고, 검색 후에 첨부 파일을가 다음 설정을 지정할 수 있습니다. 
    
      - **이름** 상자에 지연 없음을 입력 합니다.
    
      - **설명** 상자에 메시지를 즉시 배달 하 고가 첨부 파일을 검색 한 다음 설명으로 입력 합니다.
    
      - 응답 섹션에서 **동적 배달** 옵션을 선택 합니다. [동적 배달에 대해 자세히 알아보고 ATP 안전한 첨부 파일을 사용 하 여 미리 봅니다](dynamic-delivery-and-previewing.md).
    
      - **첨부 파일 리디렉션** 섹션에서 리디렉션을 사용 하도록 설정 하는 옵션을 선택 하 고 사용자가 악의적 첨부 파일을 조사할 Office 365 전역 관리자, 보안 관리자 또는 보안 분석가의 전자 메일 주소를 입력 합니다. 
    
      - **적용 대상** 섹션에서 **받는 사람 도메인**을 선택한 다음 도메인을 선택 합니다. **추가**를 선택한 다음 **확인**을 선택 합니다.
    
6. **저장**을 선택합니다.
    
조직에 대해 여러 ATP 안전 첨부 파일 정책을 설정 하는 것이 좋습니다. 이러한 정책은 **ATP 안전한 첨부 파일** 페이지에 나열 된 순서 대로 적용 됩니다. 정책을 정의 하거나 편집한 후에는 정책이 Microsoft 데이터 센터 전체를 적용 하는 데 30 분 이상 걸릴 수 있습니다. 
  
## <a name="step-3-learn-about-atp-safe-attachments-policy-options"></a>3 단계: ATP 안전 첨부 파일 정책 옵션에 대해 알아보기

ATP 안전한 첨부 파일 정책을 설정 하는 경우 모니터, 차단, 교체, 동적 배달 등의 다양 한 옵션 중에서 선택할 수 있습니다. 다음 표에는 이러한 옵션의 기능에 대 한 설명이 나와 있으며 각 작업의 결과를 요약 하 여 설명 합니다.
  
|**옵션**|**효과**|**다음 작업을 수행할 때 사용 합니다.**|
|:-----|:-----|:-----|
|**해제** <br/> |맬웨어 용 첨부 파일을 검색 하지 않음  <br/> 메시지 배달을 연기 하지 않음  <br/> |알려진 양호한 첨부 파일만 전송 하는 내부 보낸 사람, 스캐너, 팩스 또는 스마트 호스트에 대 한 검사 해제  <br/> 내부 메일 라우팅의 불필요 한 지연 방지  <br/> **이 옵션은 대부분의 사용자에 게 권장 되지 않습니다. 이를 통해 소수의 내부 보낸 사람 그룹에 대해 ATP 안전 첨부 파일 검색 기능을 해제할 수 있습니다.**           |
|**모니터링** <br/> |첨부 파일이 있는 메시지를 배달 하 고 검색 된 맬웨어로부터 발생 하는 결과를 추적 합니다.  <br/> |조직에서 검색 된 맬웨어가 이동 하는 위치 확인  <br/> |
|**정책의** <br/> |검색 된 맬웨어 첨부 파일이 있는 메시지를 계속 진행 하지 않음  <br/> 보안 관리자 또는 분석가가 해당 메시지를 검토 하 고 릴리스 (또는 삭제할 수 있음)가 검색 된 맬웨어가 있는 메시지를 [365 격리](manage-quarantined-messages-and-files.md) 로 전송 합니다.  <br/> 나중에 메시지와 첨부 파일을 자동으로 차단 합니다.  <br/> |동일한 맬웨어 첨부 파일을 사용 하 여 조직에서 반복 되는 공격 으로부터 보호  <br/> |
|**바꾸기** <br/> |검색 된 맬웨어 첨부 파일을 제거 합니다.  <br/> 첨부 파일이 제거 되었음을 받는 사람에 게 알립니다.  <br/> 보안 관리자 또는 분석가가 해당 메시지를 검토 하 고 릴리스 (또는 삭제할 수 있음)가 검색 된 맬웨어가 있는 메시지를 [365 격리](manage-quarantined-messages-and-files.md) 로 전송 합니다.  <br/> |검색 된 맬웨어로 인해 첨부 파일이 제거 된 받는 사람에 대 한 가시성을 높입니다.  <br/> |
|**동적 배달** <br/> |메시지를 즉시 배달  <br/> 검색이 완료 될 때까지 첨부 파일을 자리 표시자 파일로 바꾼 다음, 맬웨어가 감지 되지 않으면 첨부 파일을가.  <br/> 검색 중 대부분의 Pdf 및 Office 파일에 대 한 첨부 파일 미리 보기 기능을 포함 합니다.  <br/> 검색 된 맬웨어가 있는 메시지를 격리로 전송 하 여 보안 관리자 또는 분석가가 해당 메시지를 검토 하 고 릴리스 (또는 삭제할 수 있음)  <br/> [동적 배달 및 ATP 안전한 첨부 파일로 미리 보는 방법 알아보기](dynamic-delivery-and-previewing.md) <br/> |악성 파일에서 받는 사람을 보호 하는 동안 메시지 지연 방지  <br/> 검색을 수행 하는 동안 받는 사람이 안전 모드에서 첨부 파일을 미리 볼 수 있도록 허용  <br/> |
|**리디렉션 사용** <br/> |모니터, 차단 또는 바꾸기 옵션을 선택한 경우에 적용 됩니다.  <br/> 보안 관리자 또는 분석가가 조사를 수행할 수 있는 지정 된 전자 메일 주소로 첨부 파일을 보냅니다.  <br/> |보안 관리자 및 분석가가 의심 스러운 첨부 파일을 연구할 수 있도록 설정  <br/> |
   
## <a name="next-steps"></a>다음 단계

ATP 안전한 첨부 파일 정책이 마련 되 면 보고서를 확인 하 여 ATP가 조직에 어떻게 작동 하는지 확인할 수 있습니다. 자세히 알아보려면 다음 리소스를 참조 하세요.
- [Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)
- [보안 &amp; 및 준수 센터에서 탐색기 사용](use-explorer-in-security-and-compliance.md)

ATP에 게 제공 되는 새로운 기능에 대해서는 계속 제공 합니다. [Microsoft 365 로드맵을](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) 방문 하 여 [ATP에 추가 되는 새로운 기능](office-365-atp.md#new-features-in-office-365-atp)에 대해 알아보세요.
 