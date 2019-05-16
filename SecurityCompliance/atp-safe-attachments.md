---
title: Office 365 ATP 안전한 첨부 파일
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.date: 04/04/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
ms.collection:
- M365-security-compliance
description: 안전한 첨부 파일 기능은 전자 메일 첨부 파일을 클릭 하 여 확인할 시간을 제공 합니다. 안전한 첨부 파일을 사용 하 여 사용자가 전자 메일로 보내거나 받는 악의적인 파일 로부터 조직을 보호 합니다.
ms.openlocfilehash: fd3fc7f790870330f0f69fc4cca59e1b8c58ce00
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077534"
---
# <a name="office-365-atp-safe-attachments"></a>Office 365 ATP 안전한 첨부 파일

## <a name="overview-of-office-365-atp-safe-attachments"></a>Office 365 ATP 안전한 첨부 파일 개요

Atp 안전한 첨부 파일 ( [Atp 안전한 링크](atp-safe-links.md)포함)은 [Office 365 ATP (Advanced Threat Protection](office-365-atp.md) )의 일부입니다. ATP 안전한 첨부 파일 기능은 전자 메일 첨부 파일이 악성 인지 확인 한 다음 조직을 보호 하기 위해 조치를 취합니다. ATP 안전한 첨부 파일 기능은 Office 365 전역 또는 보안 관리자가 설정한 [Atp 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 에 따라 조직을 보호 합니다. 
  
ATP 보호는 SharePoint Online, 비즈니스용 OneDrive 및 Microsoft 팀의 파일로도 확장할 수 있습니다. 자세한 내용은 [SharePoint, OneDrive 및 Microsoft 팀에 대 한 Office 365 Advanced Threat Protection](atp-for-spo-odb-and-teams.md)를 참조 하세요.

## <a name="how-it-works"></a>작업 방법

ATP 안전한 첨부 파일 기능은 조직의 사용자에 대해 전자 메일 첨부 파일을 확인 합니다. ATP 안전한 첨부 파일 정책이 적용 되 고 해당 정책에서 다루는 누군가가 Office 365의 전자 메일을 볼 때, 해당 전자 메일 첨부 파일을 확인 하 고 ATP 안전한 첨부 파일 정책에 따라 적절 한 조치를 취할 수 있습니다. 정책이 정의 된 방식에 따라 사용자가 악성 파일을 보낸 것을 알지 못하면 작업을 계속할 수 있습니다.
  
다음은 직장의 ATP 안전 첨부 파일에 대 한 두 가지 예입니다.
  
- **예 1: 전자 메일 첨부 파일** Lee에서 첨부 파일이 있는 전자 메일 메시지를 수신 한다고 가정 합니다. 해당 첨부 파일이 안전한 지 아니면 실제로 Lee의 사용자 자격 증명을 도용 하도록 설계 된 맬웨어가 있는지를 Lee는 것은 분명 하지 않습니다. Lee의 조직에서는 보안 관리자가 ATP 안전한 첨부 파일 정책을 며칠 전에 정의 했습니다. ATP 안전한 첨부 파일 기능을 사용 하 여 Lee가 수신 되기 전에 전자 메일 첨부 파일을 가상 환경에서 열고 테스트 합니다. 첨부 파일이 악성 인 것으로 확인 되 면 자동으로 제거 됩니다. 안전 하지 않은 첨부 파일은 Lee 클릭 하면 예상 대로 열립니다.

- **예 2: SharePoint Online의 파일** Jean에서 파일을 받아 SharePoint Online의 라이브러리에 업로드 했다고 가정 합니다. Jean는 파일에 대 한 링크를 나머지 팀과 공유 하 여 실제로 악성 프로그램 인지를 알지 못합니다. 다행 스럽게도 [SharePoint, OneDrive 및 Microsoft 팀](atp-for-spo-odb-and-teams.md) 은 악성 파일을 검색 하 고 차단 합니다. 며칠 후에 Chris가 문서를 엽니다. Chris가 파일을 볼 수는 있지만, chris의 컴퓨터와 악의 있는 파일을 보호 하는 공유를 열거나 공유할 수 없습니다.

ATP 안전한 첨부 파일 정책은 조직의 특정 사용자 또는 그룹이 나 전체 도메인에 적용할 수 있습니다. 또한 ATP 안전한 첨부 파일 정책은 실제 첨부 파일을 검색 하는 동안 자리 표시자 첨부 파일을 사용 하도록 구성할 수 있습니다. 자세한 내용은 **[Office 365에서 ATP 안전한 첨부 파일 정책 설정을](set-up-atp-safe-attachments-policies.md)** 참조 하십시오.

> [!NOTE]
> ATP 안전한 첨부 파일 검사는 Office 365 데이터가 있는 동일한 지역에서 발생 합니다. 데이터 센터 지역에 대 한 자세한 내용은 [어디에 있습니까?](https://products.office.com/where-is-your-data-located?geo=All) 를 참조 하세요. 

  
## <a name="how-to-get-atp-safe-attachments"></a>ATP 안전한 첨부 파일을 가져오는 방법

먼저 구독에 [Advanced Threat Protection](office-365-atp.md)이 포함 되어 있는지 확인 합니다. ATP는 [microsoft 365 enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 Enterprise E5, office 365 교육용 A5 등 구독에 포함 되어 있습니다. 조직에서 Office 365 ATP를 포함 하지 않는 Office 365 구독을 사용 하는 경우 ATP를 추가 기능으로 구매할 수 있습니다. 자세한 내용은 [office 365 Advanced Threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 Advanced Threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요. 

다음으로 ATP의 안전한 첨부 파일 정책이 정의 되어 있는지 확인 합니다. ( [Office 365 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)참조) ATP 안전한 첨부 파일 기능은 다음과 같은 경우에 활성화 됩니다.
  
- ATP 안전한 첨부 파일 정책이 설정 됩니다. ( [Office 365에서 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)참조)

- 사용자가 회사 또는 학교 계정을 사용 하 여 Office 365에 로그인 했습니다. ( [Office 또는 office 365에 로그인을](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)참조 하세요.)

ATP 정책을 정의 하거나 편집 하려면 적절 한 역할이 할당 되어 있어야 합니다. 다음 표에서는 몇 가지 예를 설명 합니다.

|역할  |할당 된 위치/방법  |
|---------|---------|
|Office 365 전역 관리자 |Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.         |
|보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조) |

## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>ATP 안전한 첨부 파일 보호가 현재 위치에 있는지 여부를 확인 하는 방법

[ATP 안전한 첨부 파일 정책을 정의 하거나 검토](set-up-atp-safe-attachments-policies.md)한 후에는 [Advanced Threat Protection에 대 한 보고서](view-reports-for-atp.md)를 확인 하 여 서비스가 작동 하는 방식을 확인할 수 있습니다.
  
다음 표에서는 몇 가지 예제 시나리오에 대해 설명 합니다. 이러한 모든 경우에는 조직이 Advanced Threat Protection을 포함 하는 Office 365 구독을 갖는 것으로 가정 합니다.
  
|**시나리오 예**|**이 경우 ATP에서 안전한 첨부 파일 보호가 적용 됩니까?**|
|:-----|:-----|
|Pat 조직에 Office 365 Enterprise E5가 있지만, ATP 안전한 첨부 파일에 대 한 정책을 아직 정의 하지 않은 경우  <br/> |아니요. 이 기능을 사용할 수는 있지만 ATP 안전한 첨부 파일 보호를 적용 하려면 atp 안전 첨부 파일 정책을 하나 이상 정의 해야 합니다.  <br/> |
|Lee은 Contoso의 판매 부서에 있는 직원입니다. Lee의 조직에는 재무 직원 에게만 적용 되는 ATP 안전 첨부 파일 정책이 포함 됩니다.  <br/> |아니요. 이 경우 금융 직원은 안전한 첨부 파일 보호를 제공 하지만 영업부를 비롯 한 다른 직원은 이러한 그룹을 포함 하는 정책을 정의할 때까지 하지 않습니다.  <br/> |
|어제 Jean 조직의 Office 365 관리자가 모든 직원에 게 적용 되는 ATP 안전 첨부 파일 정책을 설정 합니다. 이전 버전 Jean에는 첨부 파일이 포함 된 전자 메일 메시지가 수신 되었습니다.  <br/> |예. 이 예에서는 Jean에 Advanced Threat Protection 라이선스가 있고 Jean을 포함 하는 ATP 안전 첨부 파일 정책이 정의 되어 있습니다. 일반적으로 새 정책이 데이터 센터 전체에 적용 되는 데 약 30 분이 걸립니다. 이 경우에는 요일이 전달 된 것 이므로 정책이 적용 되어야 합니다.  <br/> |
|Chris의 조직에는 조직의 모든 사용자에 대해 ATP 안전한 첨부 파일 정책이 있는 Office 365 Enterprise E5가 있습니다. Chris는 첨부 파일이 있는 전자 메일을 받은 다음 조직 외부에 있는 다른 사람에 게 메시지를 전달 합니다.  <br/> |ATP에서 안전한 첨부 파일 보호는 Chris가 받는 메시지에 적용 됩니다. 받는 사람의 조직에서 ATP 안전한 첨부 파일 정책도 현재 위치에 저장 되어 있는 경우 Chris가 전달 하는 메시지는 전달 메시지가 도착할 때 해당 정책의 적용을 받습니다.  <br/> |
|자원의 조직에 안전한 첨부 파일 정책이 마련 되어 있고 [SharePoint, OneDrive 및 Microsoft 팀에 대 한 atp](atp-for-spo-odb-and-teams.md) 가 설정 되었습니다. 자원 SharePoint Online의 모든 파일을 검색 하 여 열거나 다운로드 해도 안전한 것으로 가정 합니다.  <br/> |ATP 안전한 첨부 파일 보호는 정의 된 정책에 따라 적절 하 게 적용 됩니다. 그러나 SharePoint Online, 비즈니스용 OneDrive 또는 Microsoft 팀의 모든 파일을 검색 하는 것은 아닙니다. 자세한 내용은 [SharePoint, OneDrive 및 Microsoft 팀에 대 한 ATP](atp-for-spo-odb-and-teams.md)를 참조 하세요.  <br/> |

## <a name="submitting-files-for-malware-analysis"></a>맬웨어 분석용 파일 제출

- Microsoft에 분석할 파일을 받은 경우 [맬웨어 분석용 파일 제출을](https://aka.ms/wdsi/submit)참조 하세요.

- 분석을 위해 Microsoft에 제출 하려는 전자 메일 메시지 (첨부 파일 포함 또는 제외)가 수신 되는 경우 [보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 합니다.
