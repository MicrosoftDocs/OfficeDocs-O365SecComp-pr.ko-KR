---
title: Office 365 ATP 안전 하 게 보호 첨부 파일
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/05/2019
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
description: 안전한 첨부 파일 기능이 전자 메일 첨부 파일의 클릭 시간 증명 정보를 제공 합니다. 조직 파일 악의적인 사용자 로부터 보호 하기 위해 사용 하 여 안전한 첨부 파일 보내기 또는 전자 메일을 받을 합니다.
ms.openlocfilehash: 3717c0d278aaba4fce25cb196ebef9e277921408
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741131"
---
# <a name="office-365-atp-safe-attachments"></a>Office 365 ATP 안전 하 게 보호 첨부 파일

## <a name="overview-of-office-365-atp-safe-attachments"></a>Office 365 ATP 안전 하 게 보호 첨부 파일의 개요 (영문)

[ATP 안전한 링크](atp-safe-links.md)) (함께 ATP 안전한 첨부 파일에는 [Office 365 고급 위협 보호](office-365-atp.md) (ATP)의 일부입니다. ATP 안전한 첨부 파일 기능이 악의적인, 전자 메일 첨부 파일이 있는지 확인 하 고 조직을 보호 하는 작업을 수행 합니다. ATP 안전한 첨부 파일 기능이 Office 365 전역 또는 보안 관리자가 설정 된 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 에 따라 조직을 보호 합니다. 
  
또한 ATP 보호 비즈니스, 및 Microsoft 팀의 SharePoint Online, OneDrive에서 파일을 확장할 수 있습니다. 자세한 내용은, [SharePoint, OneDrive 및 팀이 Microsoft Office 365 고급 위협 보호](atp-for-spo-odb-and-teams.md)를 참조 합니다.
       
## <a name="how-it-works"></a>작동 방법

ATP 안전한 첨부 파일 기능이 조직의 사용자에 대 한 전자 메일 첨부 파일을 확인합니다. ATP 안전한 첨부 파일 정책이 적용 된 하 고 정책에서는 Office 365 수 있는 전자 메일에서 다루는 다른 사용자를 자신의 전자 메일 첨부 파일을 확인 하 고 ATP 안전한 첨부 파일 정책에 따라 적절 한 동작이 수행 됩니다. 정책에 정의 되는 방법에 따라 사용자를 몰라도 전혀 악의적인 파일 전송 되었는지 작업을 계속할 수 있습니다.
  
회사에서 ATP 안전한 첨부 파일의 두 예제는 다음과 같습니다.
  
- **예제 1: 첨부 파일을 전자 메일** Lee 첨부 파일이 포함 된 전자 메일 메시지를 받는 경우를 가정해 보겠습니다. 않은 Lee 수 있다는 사실을 여부 첨부 파일은 안전 또는 실제로 백화점 ㈜의 사용자 자격 증명을 훔쳐 하도록 설계 맬웨어를 포함 합니다. 백화점 ㈜의 조직에서 보안 관리자 며칠 전 ATP 안전한 첨부 파일 정책을 정의 합니다. ATP 안전한 첨부 파일 기능을 전자 메일 첨부 파일 열리고 Lee이를 받기 전에 가상 환경에서 테스트 됩니다. 첨부 파일 악성 코드가 포함 될를 확인 하는 경우 자동으로 제거 됩니다. 첨부 파일을 안전 하는 경우 Lee 클릭할 때 정상적으로 열립니다. 
    
- **예 2: SharePoint Online에서 파일** Jean 파일을 수신 하 고 SharePoint Online의 라이브러리로 업로드 한 경우를 가정해 보겠습니다. Jean 파일에 대 한 링크와 공유를 사용 하는 팀의 나머지는 파일을 실제로 악의적인 정확히 모르는 합니다. 놓기만 [ATP SharePoint, OneDrive 및 Microsoft 팀의](atp-for-spo-odb-and-teams.md) 악의적인 파일을 감지 하 고 되지 않도록 차단 합니다. 몇 일이 지난 후 문서를 여는데 Chris 이동 합니다. 이 파일은 다음과 같은 Chris 볼 수 있지만 Chris 열거나 악의적인 파일에서 Chris의 컴퓨터와 다른 사용자를 방지 하는 것을 공유할 수 없습니다. 
    
ATP 안전한 첨부 파일 검사 가져오고 Office 365 데이터가 있는 동일한 영역에 배치 합니다. 데이터 센터 지역에 대 한 자세한 내용은 참조 [가 다음에 있는 데이터?](https://products.office.com/where-is-your-data-located?geo=All) 

ATP 안전한 첨부 파일 정책은 특정 사용자 또는 조직 전체에서 그룹 또는 전체 도메인에 적용할 수 있습니다. 또한 ATP 안전한 첨부 파일 정책은 실제 첨부 파일을 검색 하는 동안 개체 틀 첨부 파일을 사용 하 여 구성할 수 있습니다. 자세한 내용은 **[Office 365의 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)** 을 참조 합니다. 
  
## <a name="how-to-get-atp-safe-attachments"></a>ATP 안전한 첨부 파일을 얻는 방법

먼저, 구독 [고급 위협 보호](office-365-atp.md)를 포함 해야 합니다. ATP에 [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home)"," [Microsoft 365 비즈니스](https://www.microsoft.com/microsoft-365/business)"," Office 365 엔터프라이즈 e 5 "," Office 365 교육 A5 "," 등의 구독에 포함 됩니다. 조직에 Office 365 ATP를 포함 하지 않는 한 Office 365 구독을 하는 경우에 추가 기능으로 ATP을 잠재적으로 구입할 수 있습니다. 자세한 내용은 [Office 365 고급 위협 Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 참조 하십시오. 

다음으로, ATP 안전한 첨부 파일 정책에 정의 된 확인 합니다. ( [Office 365 ATP 안전한 첨부 정책 설정](set-up-atp-safe-attachments-policies.md)참조) ATP 안전한 첨부 파일 기능은 현재 경우:
  
- ATP 안전한 첨부 파일 정책은 설정 합니다. ( [Office 365의 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)참조).
    
- 사용자가 자신의 작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 됩니다. ( [Office 또는 Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)참조).

ATP 정책, 정의 (또는 편집)를 할당 되어 있어야 다음 표에 설명 된 역할 중 하나:

|역할  |Where/방법 할당  |
|---------|---------|
|Office 365 전역 관리자 |Office 365를 구매 하 여를 로그인 하는 사람 이름은 기본적으로 전역 admin입니다. (자세한 내용은 [Office 365에 대 한 관리자 역할](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 참조 하십시오.)         |
|Office 365 보안 관리자 |관리 센터 ([https://aka.ms/admincenter](https://aka.ms/admincenter))|
|Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>ATP 안전한 첨부 파일 보호 전체에서 인지 확인 하는 방법

[ATP 안전한 첨부 파일 정책에 정의 된 (또는 검토)을](set-up-atp-safe-attachments-policies.md)설치한 후 서비스가 작동 하는 방법을 보려면 하나의 좋은 방법은 [고급 위협 보호에 대 한 보고서를 확인](view-reports-for-atp.md)하 여 것입니다.
  
다음 표에서 일부 예제 시나리오를 설명합니다. 모든이 경우에는 조직에는 고급 위협 보호를 포함 하는 Office 365 구독을 가정 합니다.
  
|**시나리오 예**|**ATP 안전한 첨부 파일 보호는이 경우에 적용 여부**|
|:-----|:-----|
|Pat의 조직에 Office 365 Enterprise E5, 있지만 아무도 정의 된 모든 정책을 ATP 안전한 첨부 파일에 대 한 아직 합니다.  <br/> |아니요. 기능을 사용할 수 있지만 적어도 하나의 ATP 안전한 첨부 파일 정책이 원본 위치에 있는 것으로 ATP 안전한 첨부 파일 보호에 대 한 순서로 정의 되어야 합니다.  <br/> |
|Lee contoso 영업 부서의 직원입니다. 백화점 ㈜의 조직에 재무 직원 들의 경우에 적용 되는 위치에는 ATP 안전한 첨부 파일 정책이 있습니다.  <br/> |아니요. 이 경우 finance 직원 ATP 안전한 첨부 파일 보호 떨어지기 않지만 다른 직원, 영업 부서를 포함 하 여 이러한 그룹을 포함 하는 정책 정의 된 때까지 하지 합니다.  <br/> |
|어제, Jean의 조직에서 Office 365 관리자가 모든 직원에 게 적용 되는 ATP 안전한 첨부 파일 정책을 설정 합니다. 지금 바로 이전 Jean 첨부 파일이 포함 된 전자 메일 메시지를 받았습니다.  <br/> |예입니다. 이 예제에서는 Jean 라이선스 고급 위협 보호를 위한 있으며 Jean를 포함 하는 ATP 안전한 첨부 파일 정책이 정의 되었습니다. 일반적으로 데이터 센터; 적용 하려면 새 정책에 대 한 약 30 분 걸리는 하루에이 경우을 통과 하므로 정책을 적용 해야 합니다.  <br/> |
|Chris의 조직에는 조직에서 모든 사용자에 대 한 전체 ATP 안전한 첨부 파일 정책을 사용 하 여 Office 365 Enterprise e 5에 있습니다. Chris 첨부 파일, 있으며 조직 외부에 있는 다른 사용자에 게 메시지를 전달 하는 전자 메일을 받습니다.  <br/> |ATP 안전한 첨부 파일 보호 Chris 받는 메시지에 대 한 마련 되었습니다. 받는 사람의 조직 전체에서 ATP 안전한 첨부 파일 정책 권한도, 하는 경우 다음 Chris 전달 된 메시지 것 해당 정책의 영향을 받습니다 전달 된 메시지가 도착 했을 때입니다.  <br/> |
|자원이 조직 장소에 ATP 안전한 첨부 파일 정책 있으며 [SharePoint, OneDrive 및 Microsoft 팀의 ATP](atp-for-spo-odb-and-teams.md) 설정 되었는지 합니다. 자원이는 SharePoint Online에서 모든 파일 검사 된를 열거나 다운로드 안전 되었다고 가정 합니다.<br/> |ATP 안전한 첨부 파일 보호, 정의 된 정책에 따라 전체에는 그러나 모든 단일 파일 SharePoint Online, 회사 또는 Microsoft 팀의 비즈니스용 OneDrive의 검색은이 아닙니다. (자세한 내용은 참조 [SharePoint, OneDrive 및 Microsoft 팀의 ATP](atp-for-spo-odb-and-teams.md).)<br/> |
   
## <a name="submitting-files-for-malware-analysis"></a>맬웨어 분석을 위해 파일 전송

- 분석 하는 Microsoft를 요청 하려는 파일을 받은 경우 [제출을 맬웨어 분석을 위해 파일을](https://aka.ms/wdsi/submit)참고 하십시오.

- 분석을 위해 Microsoft에 전송 하려는 전자 메일 메시지 (또는 없는 첨부 파일)을 수신 하는 경우에 사용 [보고서 메시지의 추가 기능](enable-the-report-message-add-in.md).
  
