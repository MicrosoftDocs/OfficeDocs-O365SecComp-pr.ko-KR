---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/27/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Office 365 Advanced Threat Protection에는 스푸핑 인텔리전스, 안전한 링크, 안전한 첨부 파일 및 고급 피싱 방지 기능이 포함되어 있습니다. Advanced Threat Protection은 SharePoint Online, 비즈니스용 OneDrive 및 Microsoft Teams 파일로도 확장됩니다.
ms.openlocfilehash: c147fde4e470b998a66a2cb456be71f635db25d7
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706312"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

## <a name="overview"></a>개요

Office 365 ATP(Advanced Threat Protection)는 다음을 통해 악의적인 공격으로부터 조직을 보호합니다.
  
- [ATP 안전한 첨부 파일](atp-safe-attachments.md)로 맬웨어에 대해 전자 메일 첨부 파일 스캔
    
- [ATP 안전한 링크](atp-safe-links.md)로 전자 메일 메시지 및 Office 문서의 웹 주소(URL) 스캔
    
- [SharePoint, OneDrive 및 Microsoft Teams에 대한 ATP](atp-for-spo-odb-and-teams.md)로 온라인 라이브러리의 악성 파일 식별 및 차단
    
- [스푸핑 인텔리전스](learn-about-spoof-intelligence.md)로 권한이 없는 스푸핑에 대한 전자 메일 메시지 확인
    
- [Office 365의 ATP 피싱 방지 기능](atp-anti-phishing.md)으로 다른 사람이 사용자 및 조직의 사용자 지정 도메인을 대리 실행하려는 시도 감지
    
**Office 365 ATP를 통한 보호는 조직의 보안 팀이 안전한 링크, 안전한 첨부 파일 및 피싱 방지에 대해 정의한 정책에 의해 결정됩니다**. 주기적으로 정책을 검토하고 수정하여 최신 상태로 유지하고 서비스에 추가된 새로운 기능을 활용하는 것이 중요합니다. [보고서를 통해](view-reports-for-atp.md) 조직에서 ATP가 작동하는 방식을 표시할 수 있습니다. 이러한 보고서는 정책을 검토하고 업데이트해야 하는 영역도 표시합니다. 또한 맬웨어가 아니지만 맬웨어로 표시되는 파일이나 Microsoft에서 검사할 파일이 있는 경우 [분석을 위해 Microsoft에 파일을 제출](#submit-a-suspicious-file-to-microsoft-for-analysis)할 수 있습니다.

## <a name="new-features-are-continually-being-added-to-atp"></a>ATP에 계속 새로운 기능 추가

Office 365에 ATP가 포함된 새로운 기능을 계속 추가하고 있습니다. 다음은 몇 가지 새로운 기능의 목록으로, 일부 기능에서는 ATP 정책을 검토하고 업데이트합니다. ATP(또는 Microsoft 365)에 제공되는 새 기능에 대한 자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap?filters=O365)을 참조하세요.
  
- 2017년10 월 말부터 ATP 안전한 링크 보호가 확장되어 Windows의 Word, Excel, PowerPoint 및 Visio와 같은 Office 365 ProPlus 문서의 URL과 iOS 및 Android 장치의 Office 앱의 URL뿐만 아니라 전자 메일의 URL에도 적용됩니다.([Office 최신 인증](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)을 사용하고 있는지 확인하세요.)
    
- 2018년 3월부터 ATP 안전한 링크 보호가 확장되어 조직 내의 사용자 사이에 전송되는 전자 메일에 적용됩니다. ([ATP 안전한 링크 정책 검토 및 편집](set-up-atp-safe-links-policies.md)을 확인하세요.)

- 2018년 5월 말부터 보안 &amp; 규정 준수 센터의 [검역](quarantine-email-messages.md) 기능이 [SharePoint Online, 비즈니스용 OneDrive 및 Microsoft Teams 를 위한 ATP](atp-for-spo-odb-and-teams.md)로 확장됩니다.
 
- 2018년 하반기부터 ATP 안전한 보호 보호가 Office Online(Word Online, Excel Online, PowerPoint Online 및 OneNote Online) 및 Mac의 Office 365 ProPlus에서 URL에 적용되도록 확장되었습니다.([ATP 안전한 링크 정책 검토 및 편집](set-up-atp-safe-links-policies.md)을 확인하세요.)

- 2018년 9월부터 [Office 365 ATP 경고 페이지](atp-safe-links-warning-pages.md)에 새 색 구성표, 자세한 내용 및 기존 경고 및 권장 사항에도 불구하고 사이트를 계속 유지하는 기능이 제공됩니다. 
 
- 2018년 10월과 이후 몇 개월에 걸쳐 사용자가 OWA(Outlook Web Application) 또는 Outlook을 사용할 때 ATP 안전한 링크에서 다시 작성한 URL이 아닌 원래 URL을 렌더링합니다. (이 기본 링크를 표시 유형이라고 합니다.)

      
## <a name="get-office-365-atp"></a>Office 365 ATP 받기

> [!IMPORTANT]
> Office 365 ATP의 경우 Microsoft 365 Enterprise, Office 365 Enterprise E5, Office 365 Education A5 및 [Microsoft 365 Business](https://docs.microsoft.com/ko-KR/microsoft-365/business/security-features)와 같은 구독에 포함됩니다. 조직에서 Office 365 ATP가 포함되지 않은 Office 365를 구독하는 경우 추가 기능으로 ATP를 구입할 수 있습니다. 자세한 내용은 [Office 365 Advanced Threat Protection 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 참조하세요. 

1. 전역 또는 보안 관리자 인 경우 [https://portal.office.com](https://portal.office.com)으로 이동하고 Office 365에 대한 회사 또는 학교 계정으로 로그인합니다. 
    
2. **관리자 ** \> ** 청구**을 선택하여 현재 구독에 포함된 내용을 확인합니다. <br/>![전역 관리자인 경우 portal.office.com에 로그인하고 관리자 \> 청구](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)로 이동합니다.
  
3. **Office 365 Enterprise E5**, **Office 365 Education A5** 또는 **Microsoft 365 Business**가 표시되는 경우 조직에 ATP가 제공니다. <br/>**Office 365 Enterprise E3** 또는 **Office 365 Enterprise E1**과 같은 다른 구독이 표시되는 경우 ATP를 추가하는 것이 좋습니다. 이렇게 하려면 **+ 구독 추가**을 선택합니다.
    
ATP가 있으면 다음 단계는 보안 팀이 정책을 정의하는 것입니다. 
  
## <a name="define-policies-for-atp"></a>ATP에 대한 정책 정의

- 신뢰할 수 있는 사람 또는 도메인에서 온 것처럼 표시하는 전자 메일 메시지를 보내는 공격자로부터 보호하기 위한 가장 기반 공격을 포함하여 **[Office 365에서 ATP 피싱 방지 정책 설정](set-up-anti-phishing-policies.md)** 

- 조직의 [차단한 URL 목록 사용자 지정](set-up-a-custom-blocked-urls-list-wtih-atp.md) 및 ["URL 다시 쓰지 않음" 목록 사용자 지정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)을 포함하여 **[Office 365에서 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)**
    
- [동적 배달 및 미리보기](dynamic-delivery-and-previewing.md)를 포함할 수 있는 **[Office 365에서 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)**
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>보고서를 확인하여 ATP 작동 방식 보기

ATP 정책이 적용된 후에는 서비스 작동 방식을 표시하는 보고서를 사용할 수 있습니다.

[![보안&amp; 규정 준수 센터 대시보드는 Advanced Threat Protection이 작업 중인 위치를 확인할 수 있도록 도와줍니다](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Office 365 전역 관리자, 보안 관리자 또는 보안 독자인지 확인합니다 ([Office 365 보안 &amp; 규정 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)을 참조하세요.)
    
2. [Advanced Threat Protection 보고서를 봅니다](view-reports-for-atp.md).
    
3. 필요에 따라 보안 정책을 조정합니다. 다음 리소스를 참조하세요.

  - [Office 365 ATP 피싱 방지 정책](set-up-anti-phishing-policies.md)
    
  - [Office 365 ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md)
    
  - [Office 365 ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>분석을 위해 Microsoft에 의심스러운 파일 제출

- 맬웨어라고 의심되는 파일을 가져온 경우 분석을 위해 해당 파일을 Microsoft에 제출할 수 있습니다. [Windows Defender 보안 인텔리전스 제출 포털](https://go.microsoft.com/fwlink/?linkid=857185)을 방문합니다.

- 분석을 위해 Microsoft에 제출하려는 전자 메일 메시지(첨부 파일 포함 또는 제외)가 있는 경우 [보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용합니다. 
  

