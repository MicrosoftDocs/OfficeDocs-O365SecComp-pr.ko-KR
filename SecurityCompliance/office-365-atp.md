---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection에는 스푸핑 인텔리전스, 안전한 링크, 안전한 첨부 파일, 고급 피싱 방지 기능 및 위협 인텔리전스가 포함 됩니다.
ms.openlocfilehash: d78b37ca048187a298b6e083b54ad68b949638ef
ms.sourcegitcommit: 2af6c3e8a74995294a67429530af8f085e6ca136
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "30051179"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

## <a name="overview-of-office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection 개요

> [!IMPORTANT]
> 이 문서는 비즈니스 고객을 위한 것입니다. Outlook의 안전한 링크에 대 한 정보를 검색 하는 개인 사용자는 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하십시오.

Office 365 ATP(Advanced Threat Protection)는 다음을 통해 악의적인 공격으로부터 조직을 보호합니다.
  
- [ATP 안전한 첨부 파일](atp-safe-attachments.md)로 맬웨어에 대해 전자 메일 첨부 파일 스캔
    
- [ATP 안전한 링크](atp-safe-links.md)로 전자 메일 메시지 및 Office 문서의 웹 주소(URL) 스캔
    
- [SharePoint, OneDrive 및 Microsoft Teams에 대한 ATP](atp-for-spo-odb-and-teams.md)로 온라인 라이브러리의 악성 파일 식별 및 차단
    
- [스푸핑 인텔리전스](learn-about-spoof-intelligence.md)로 권한이 없는 스푸핑에 대한 전자 메일 메시지 확인
    
- [Office 365의 ATP 피싱 방지 기능](atp-anti-phishing.md)으로 다른 사람이 사용자 및 조직의 사용자 지정 도메인을 대리 실행하려는 시도 감지
    
**Office 365 ATP를 통한 보호 기능은 조직의 보안 팀이 안전한 링크, 안전한 첨부 파일 및 피싱 방지를 위해 정의 하는 정책에 따라 결정 됩니다**. 정책을 정의 하 고 해당 정책을 주기적으로 검토 및 수정 하 여 최신 상태를 유지 하 고 서비스에 추가 되는 새로운 기능을 활용 하는 것이 중요 합니다. 

조직에서 ATP가 작동 하는 방식을 표시 하는 [보고서를 사용할 수](view-reports-for-atp.md) 있습니다. 이러한 보고서에는 정책을 검토 하 고 업데이트 해야 하는 영역도 표시 될 수 있습니다. 또한 맬웨어가 아닌 것으로 표시 된 파일이 나 Microsoft에서 검사 하려는 파일을 포함 하는 경우에는 [분석을 위해 microsoft에 파일을 제출할](#submit-a-suspicious-file-to-microsoft-for-analysis)수 있습니다.

## <a name="new-features-are-continually-being-added-to-atp"></a>ATP에 계속 새로운 기능 추가

Office 365에 ATP가 포함된 새로운 기능을 계속 추가하고 있습니다. 다음은 몇 가지 새로운 기능의 목록으로, 일부 기능에서는 ATP 정책을 검토하고 업데이트합니다. ATP(또는 Microsoft 365)에 제공되는 새 기능에 대한 자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap?filters=O365)을 참조하세요.


|기능 업데이트  |작업 항목  |
|---------|---------|
|2019 년 2 월에 시작 해 서 몇 개월 후에 위협 인텔리전스 기능이 ATP에 추가 됩니다. 또한 조직에서 atp가 현재 없는 경우 atp 계획 1 및 atp 계획 2를 포함 하 여 새로운 옵션을 고려할 수 있습니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요. |조직의 구독을 검토 하 고, 필요한 경우 [추가 기능을 구입 하거나 편집](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on)합니다.  |
|사용자가 outlook 또는 OWA (outlook Web Application)를 사용 하는 경우, ATP 안전한 링크는 다시 작성 된 url이 아니라 원래 url을 렌더링 하기 때문에 지난 몇 개월 동안 롤아웃 (이 네이티브 링크 렌더링을 호출 합니다.)<br>조직에서 기본 링크 렌더링을 사용할 수 있는 경우이 기능은 Outlook 365 (간편 실행) 및 OWA에서 작동 합니다.|없음         |
|2018년 9월부터 [Office 365 ATP 경고 페이지](atp-safe-links-warning-pages.md)에 새 색 구성표, 자세한 내용 및 기존 경고 및 권장 사항에도 불구하고 사이트를 계속 유지하는 기능이 제공됩니다. |없음         |
|2018의 두 번째 절반에서 시작 하 여 ATP 안전한 링크 보호는 office online (Word online, Excel online, PowerPoint online, OneNote online) 및 office 365 ProPlus의 url에 적용 되도록 확장 됩니다.   |[ATP 안전한 링크 정책 검토 및 편집](set-up-atp-safe-links-policies.md)  |
|2018년 5월 말부터 보안 &amp; 규정 준수 센터의 [검역](quarantine-email-messages.md) 기능이 [SharePoint Online, 비즈니스용 OneDrive 및 Microsoft Teams 를 위한 ATP](atp-for-spo-odb-and-teams.md)로 확장됩니다. |[ATP 안전한 첨부 파일 정책 검토 및 편집](set-up-atp-safe-attachments-policies.md) |
|2018 년 3 월부터 ATP 안전한 링크 보호는 조직 내 사용자 간에 전송 되는 전자 메일에 적용 되도록 확장 됩니다. |[ATP 안전한 링크 정책 검토 및 편집](set-up-atp-safe-links-policies.md) |
|2017 년 10 월 말부터 ATP 안전한 링크 보호는 iOS 및 Android 장치의 office 앱은 물론 Word, Excel, PowerPoint, Visio 등의 office 365 ProPlus 문서에 있는 url 뿐만 아니라 전자 메일의 url에도 적용 되도록 확장 되었습니다.  |[최신 Office 인증](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) 을 사용 하 고 있는지 확인 |

## <a name="get-office-365-atp"></a>Office 365 ATP 받기

office 365 ATP는 [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5 및 office 365 교육용 A5와 같은 구독에 포함 되어 있습니다. 조직에서 office 365 ATP를 포함 하지 않는 office 365 구독을 사용 하는 경우 ATP를 추가 기능으로 구매할 수 있습니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요. 

## <a name="define-policies-for-atp"></a>ATP에 대한 정책 정의

ATP 정책을 정의 하거나 편집 하려면 다음 표에 설명 된 역할 중 하나를 할당 받아야 합니다.

|역할  |할당 된 위치/방법  |
|---------|---------|
|Office 365 전역 관리자 |Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.         |
|보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조) |

> [!TIP]
> 역할 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.

몇 가지 유형의 ATP 정책을 정의 하 고 주기적으로 검토 합니다.

1. 가장 기반 공격을 포함 하 여 **[Office 365에서 ATP 피싱 방지 정책을 설정](set-up-anti-phishing-policies.md)** 하 여 신뢰할 수 있는 사용자 또는 도메인에서 보낸 것으로 표시 되는 전자 메일 메시지를 보내는 공격자 로부터 보호 합니다. 

2. 조직의 [사용자 지정 차단 된 url 목록과](set-up-a-custom-blocked-urls-list-wtih-atp.md) [사용자 지정 "다시 쓰지 않음" url 목록을](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)포함 하 여 **[Office 365에서 ATP 안전한 링크 정책을 설정](set-up-atp-safe-links-policies.md)** 합니다.
    
3. **[Office 365에서 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)** 및 [동적 배달 및 미리 보기](dynamic-delivery-and-previewing.md)와 같은 여러 옵션 중에서 선택 합니다.
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>보고서를 확인하여 ATP 작동 방식 보기

ATP 정책이 마련 되 면 서비스가 작동 하는 방식을 보여 주는 보고서를 사용할 수 있습니다. (Office 365 Security & 준수 센터에서 **보고서** > **대시보드로**이동 합니다.)

[![보안&amp; 규정 준수 센터 대시보드는 Advanced Threat Protection이 작업 중인 위치를 확인할 수 있도록 도와줍니다](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Office 365 전역 관리자, 보안 관리자 또는 보안 독자 (으 [https://protection.office.com](https://protection.office.com) )로 이동 하 여 로그인 합니다.
    
2. **보고서** > **대시보드로**이동 합니다. 이러한 보고서에 [대 한 지원을 받으려면 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)를 참조 하세요.
    
3. 필요한 경우 보안 정책을 조정 합니다. 이에 대 한 도움말을 보려면 다음 리소스를 참조 하세요.
    - [ATP 피싱 방지 정책](set-up-anti-phishing-policies.md)
    - [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md)
    - [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>분석을 위해 Microsoft에 의심스러운 파일 제출

- 맬웨어라고 의심되는 파일을 가져온 경우 분석을 위해 해당 파일을 Microsoft에 제출할 수 있습니다. [Windows Defender 보안 인텔리전스 제출 포털](https://go.microsoft.com/fwlink/?linkid=857185)을 방문합니다.

- 분석을 위해 Microsoft에 제출하려는 전자 메일 메시지(첨부 파일 포함 또는 제외)가 있는 경우 [보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용합니다. 
  

