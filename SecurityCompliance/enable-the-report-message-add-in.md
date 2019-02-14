---
title: 보고서 메시지 추가 기능을 사용하도록 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Outlook 및 Outlook에서 개별 사용자에 대 한 웹 또는 전체 조직에 대 한 보고서 메시지 추가 기능을 사용 하는 방법에 알아봅니다.
ms.openlocfilehash: 8c061d14d11aa868567487186c5dcca534b86215
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995159"
---
# <a name="enable-the-report-message-add-in"></a>보고서 메시지 추가 기능을 사용하도록 설정

## <a name="overview"></a>개요

보고서 메시지에서 추가 기능 Outlook 웹에서 Outlook에 대 한 사람들이 쉽게 misclassified 전자 메일 안전 또는 악의적인, 여부를 보고 Microsoft 및 그 계열사 분석을 위해 수 있도록 합니다. Microsoft의 전자 메일 보호 기술 효율성을 향상 시키기 위해 이러한 제출을 사용 합니다. 또한 사용자 조직에서 [Office 365 고급 위협 보호](office-365-atp.md) 또는 [Office 365 위협 인텔리전스](office-365-ti.md)를 사용 하는 경우 보고서 메시지에서 추가 기능을 제공 유용한 정보를 검토 하 여 업데이트를 사용할 수 있는 조직의 보안 팀 보안 정책입니다. 

등 사용자가 피싱으로 많은 메시지를 보고 하는 것으로 가정 합니다. 이 정보는 [보안 대시보드](security-dashboard.md) 및 기타 보고서에서 월등 합니다. 조직의 보안 팀이이 정보를 사용 하 여 피싱 방지 정책 업데이트 해야할 수도 있음을으로 수 있습니다. 또는 사용자는 많은 보고서 메시지 추가 기능을 사용 하 여 정크 메일 아님으로 정크 메일으로 플래그가 지정 된 메시지를 보고, 조직의 보안 팀 [스팸 방지 정책](configure-the-anti-spam-policies.md)을 조정 하려면 필요할 수 있습니다. 

보고서 메시지 추가 기능에서 Office 365 구독 및 다음 제품 작동합니다.
 - 웹용 Outlook
 - Outlook 2013 s p 1
 - Outlook 2016
 - Mac용 Outlook 2016
 - Office 365 ProPlus에 포함 된 outlook

> [!NOTE]
> 보고서 메시지에서 추가 기능 Outlook 및 웹에 있는 Outlook은 [Outlook 정크 메일 필터](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)동일한 작업 있지만 정크, 또는 피싱 시도 하지 정크, 전자 메일을 표시 하려면 모두를 사용할 수 있습니다. 보고서 메시지에서 추가 기능 Outlook 웹에서 Outlook에 대 한 Outlook 정크 메일 필터는 사용자의 사서함에서 전자 메일 메시지를 구성 하는 사용 되지만 misclassified 전자 메일에 대 한 Microsoft을 알립니다. 
  
개별 사용자 인 경우에 [자신에 대 한 보고서 메시지 추가 기능을 사용](#get-the-report-message-add-in-for-yourself)할 수 있습니다. 
  
Office 365 전역 관리자 또는 Exchange Online 관리자, 자신이 Exchange OAuth 인증을 사용 하도록 구성 된 경우에 [조직에 대 한 보고서 메시지 추가 기능을 사용](#get-and-enable-the-report-message-add-in-for-your-organization)할 수 있습니다. 보고서 메시지 추가 기능에 [중앙 집중화 배포](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins)를 통해 사용할 수 있는 이제 합니다.
    
## <a name="get-the-report-message-add-in-for-yourself"></a>메시지가 표시 되는 보고서 추가 기능에서 자신에 대 한

1. [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps) [보고서 메시지 추가 기능에](https://appsource.microsoft.com/product/office/wa104381180)대 한 검색 합니다.
    
2. 선택 **가져올 이제 IT**합니다.<br/>![메시지를 보고-지금 신청](media/ReportMessageGETITNOW.png)<br/> 
    
3. 사용 및 개인정보 보호 정책 약관을 검토 합니다. 다음 **계속**을 선택 합니다. 
    
4. 진행 중인 작업 또는 학교 계정 (업무용) 또는 Microsoft 계정 (개인용)를 사용 하 여 Office 365에 로그인 합니다.
    
추가 기능에 설치 및 활성화, 후 다음과 같은 아이콘이 표시 됩니다. 

- Outlook에서 아이콘은 다음과 같습니다. <br/> ![Outlook에 대 한 아이콘 추가 기능에 대 한 메시지를 보고 합니다.](media/OutlookReportMessageIcon.png)<br/>
- Outlook Web App (또는 웹에 있는 Outlook)에서 아이콘은 다음과 같습니다.<br/>![Outlook에서 보고서 메시지 추가 기능에 대 한 웹 아이콘](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> 다음 단계에 대해 알아봅니다 [보고서 메시지 추가 기능을 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)하는 방법입니다.
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>조직에 대 한 보고서 메시지 추가 기능을 사용 하 고 확인

> [!IMPORTANT]
> 이 작업을 완료 하려면 Office 365 전역 관리자 또는 Exchange Online 관리자 여야 합니다. 또한 Exchange 자세한 내용은 [Exchange 요구 사항 (추가 기능 배포에 집중)를](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements)참조 하십시오 OAuth 인증을 사용 하도록 구성 되어야 합니다. 

1. Microsoft 365 관리 센터에서 [서비스 & 추가 기능 페이지](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) 로 이동 합니다.<br/>![새 Microsoft 365 관리 센터에서 서비스 및 추가 기능 페이지](media/ServicesAddInsPageNewM365AdminCenter.png)<br/> 
    
2. **+ 추가 기능 배포**를 선택 합니다.<br/>![선택 추가 기능 배포](media/ServicesAddIns-ChooseDeployAddIn.png)<br/> 
    
3. **새 추가 기능에** 화면에서 정보를 검토 하 고 **** 을 선택 합니다.<br/>![새 추가 기능에서 세부 정보](media/NewAddInScreen1.png)<br/>
    
4. **Office 스토어에서 추가 기능을 추가 하려고 하는 경우**선택 하 고 **** 을 선택 합니다.<br/>![새 추가 기능을 추가 하려는 경우](media/NewAddInScreen2.png)<br/> 
    
5. 검색 **보고서 메시지**대 한 및 결과는 **보고서 메시지에 추가 기능**옆에 있는 목록에서 **추가**선택 합니다.<br/>![보고서 메시지를 검색 하 고 추가 선택 합니다](media/NewAddInScreen3.png)<br/>
    
6. **보고서 메시지** 화면에서 정보를 검토 하 고 **** 을 선택 합니다.<br/>![메시지 세부 정보를 보고 합니다.](media/ReportMessageAdd-InNewScreen4.png)<br/>

7. Outlook에 대 한 사용자 기본 설정을 지정 하 고 **** 을 선택 합니다.<br/>![Outlook에 대 한 기본 설정을 메시지를 보고 합니다.](media/ReportMessageOptionsScreen5.png)<br/>

8. 보고서 메시지에서 추가 기능, 누가 지정 하 고 **저장**을 선택 합니다. <br/>![인원 보고서 메시지의 추가 기능](media/ReportMessageOptionsScreen6.png)<br/>

> [!TIP]
> [사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙을 설정값](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)이 좋습니다.

추가 기능에 (단계 7-8 위에)를 설정 하는 경우 선택한 기능에 따라 조직의 사용자는 [보고서 메시지 추가 기능에서](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) 사용할 수 있는 갖습니다. 조직의 사용자는 다음과 같은 아이콘이 표시 됩니다. 

- Outlook에서 아이콘은 다음과 같습니다. <br/> ![Outlook에 대 한 보고서에서 메시지 추가 아이콘](media/OutlookReportMessageIcon.png)<br/>
- Outlook Web App (또는 웹에 있는 Outlook)에서 아이콘은 다음과 같습니다.<br/>![Outlook에서 웹 보고서 메시지 추가 아이콘](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> 보고서 메시지 추가 기능에 대 한 사용자에 게 알릴 있습니다 [을 사용 하 여 보고서 메시지 추가 기능](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)에 대 한 링크를 포함 합니다.

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙을 설정 합니다.

> [!IMPORTANT]
> 이 작업을 수행 하려면 Exchange Online 관리자 여야 합니다.
  
조직에서 사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙을 설정할 수 있습니다. 다운로드 하 고 조직에 대 한 보고서 메시지 추가 기능을 활성화 한 후이 작업을 수행 합니다.
  
1. Exchange 관리 센터에서 **메일 흐름** 선택 \> **규칙**입니다. 
    
2. 선택 **+** \> **새 규칙 만들기**. 
    
3. **이름** 상자에 제출 등의 이름을 입력 합니다.
    
4. **이 규칙 적용 대상** 목록에서 **받는 사람 주소... 포함**을 선택 합니다. 
    
5. **단어 또는 구 지정** 화면에서 추가 `junk@office365.microsoft.com` 및 `phish@office365.microsoft.com`을 선택한 다음 **확인**을 선택 합니다.<br/>![규칙에 대 한 정크 및 phish 전자 메일 주소를 지정 합니다.](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)<br/>
  
6. **다음 작업을 수행...** 목록에서 선택 **숨은 참조 메시지를...** 합니다. 
    
7. 전역 관리자, 보안 관리자 및/또는 사용자를 Microsoft에 보고 하는 각 전자 메일 메시지의 복사본을 받고 다음 **확인**을 선택 해야 보안 읽기 권한자를 추가 합니다.<br/>![보고 된 각 메시지의 복사본을 수신 하도록 글로벌 또는 보안 관리자 추가](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)<br/>
  
8. **감사 심각도 수준으로이 규칙**선택 하 고 **미디어**를 선택 합니다. 
    
9. **선택이 규칙에 대 한 모드** **적용**을 선택 합니다.<br/>![보고 된 각 메시지의 복사본을 가져오시겠습니까 규칙을 설정 합니다.](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)<br/>
  
10. **Save(저장)** 를 선택합니다. 
    
현재 위치에서이 규칙을 사용할 경우 보고서 메시지에서 추가 기능을 사용 하 여 전자 메일 메시지를 보고 하는 다른 사용자가 조직에서 때마다에 전역 관리자, 보안 관리자 및/또는 보안 판독기 복사본을 받게 됩니다 해당 메시지의 합니다. 이 정보를 사용 하면 설정 또는 정책, 예: [Office 365 ATP 안전한 링크](atp-safe-links.md) 정책 또는 [스팸 방지](anti-spam-protection.md) 설정 조정 수 있습니다. 

## <a name="learn-how-to-use-the-report-message-add-in"></a>보고서 메시지 추가 기능을 사용 하는 방법을 설명 합니다.

[보고서 메시지에서 추가 기능 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 참조 하십시오.

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a>검토 또는 보고서 메시지 추가 기능에 대 한 설정 편집

검토 수 있으며는 보고서 메시지 추가 기능에 대 한 [서비스 & 추가 기능 페이지](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns)에서 기본 설정을 편집할 수 있습니다. 

> [!IMPORTANT]
> 이 작업을 완료 하려면 Office 365 전역 관리자 또는 Exchange Online 관리자 여야 합니다.
    
1. Microsoft 365 관리 센터에서 [서비스 & 추가 기능 페이지](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) 로 이동 합니다.<br/>![새 Microsoft 365 관리 센터에서 서비스 및 추가 기능 페이지](media/ServicesAddInsPageNewM365AdminCenter.png)<br/>

2. 찾기 및 보고서 메시지 추가 기능을 선택 합니다.<br/>![보고서 메시지 추가 기능을 선택 하 고 찾기](media/FindReportMessageAddIn.png)<br/> 
    
3. 보고서 메시지 화면을 검토 하 고 조직에 적절 하 게 설정 편집 합니다.<br/>![보고서 메시지 추가 기능에 대 한 설정](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a>관련 항목

[보고서 메시지 추가 기능을 사용 하 여](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터](view-email-security-reports.md)

[Office 365 고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)

[탐색기를 사용 하 여 보안에서 &amp; 준수 센터](use-explorer-in-security-and-compliance.md)
  

