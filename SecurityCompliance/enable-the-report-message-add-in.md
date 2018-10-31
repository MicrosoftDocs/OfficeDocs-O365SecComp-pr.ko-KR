---
title: 보고서 메시지 추가 기능을 사용하도록 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/18/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Outlook 및 Outlook에서 개별 사용자에 대 한 웹 또는 전체 조직에 대 한 보고서 메시지 추가 기능을 사용 하는 방법에 알아봅니다.
ms.openlocfilehash: 8c9853c78a42d6eecd0989475ef8f0a44345f812
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857266"
---
# <a name="enable-the-report-message-add-in"></a>보고서 메시지 추가 기능을 사용하도록 설정

## <a name="overview"></a>개요

보고서 메시지에서 추가 기능 Outlook 웹에서 Outlook에 대 한 사람들이 쉽게 misclassified 전자 메일 안전 또는 악의적인, 여부를 보고 Microsoft 및 그 계열사 분석을 위해 수 있도록 합니다. Microsoft의 전자 메일 보호 기술 효율성을 향상 시키기 위해 이러한 제출을 사용 합니다. 또한 사용자 조직에서 [Office 365 고급 위협 보호](office-365-atp.md) 또는 [Office 365 위협 인텔리전스](office-365-ti.md)를 사용 하는 경우 보고서 메시지에서 추가 기능을 제공 유용한 정보를 검토 하 여 업데이트를 사용할 수 있는 조직의 보안 팀 보안 정책입니다. 

등 사용자가 피싱으로 많은 메시지를 보고 하는 것으로 가정 합니다. 이 정보는 [보안 대시보드](security-dashboard.md) 및 기타 보고서에서 월등 합니다. 조직의 보안 팀이이 정보를 사용 하 여 피싱 방지 정책 업데이트 해야할 수도 있음을으로 수 있습니다. 또는 사용자는 많은 보고서 메시지 추가 기능을 사용 하 여 정크 메일 아님으로 정크 메일으로 플래그가 지정 된 메시지를 보고, 조직의 보안 팀 [스팸 방지 정책](configure-the-anti-spam-policies.md)을 조정 하려면 필요할 수 있습니다. 

보고서 메시지 추가 기능에서 Office 365 구독 및 다음 제품 작동합니다.
 - 웹에 있는 outlook
 - Outlook 2013 s p 1
 - Outlook 2016
 - Mac용 Outlook 2016
 - Office 365 ProPlus에 포함 된 outlook
  
개별 사용자 인 경우에 [자신에 대 한 보고서 메시지 추가 기능을 사용](#get-the-report-message-add-in-for-yourself)할 수 있습니다. 
  
Exchange Online의 관리자 인 경우에 [조직에 대 한 보고서 메시지 추가 기능을 사용](#get-and-enable-the-report-message-add-in-for-your-organization)할 수 있습니다.
    
## <a name="get-the-report-message-add-in-for-yourself"></a>메시지가 표시 되는 보고서 추가 기능에서 자신에 대 한

1. [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps) [보고서 메시지 추가 기능에](https://appsource.microsoft.com/product/office/wa104381180)대 한 검색 합니다.
    
2. 선택 **가져올 이제 IT**합니다.<br/>![메시지를 보고-지금 신청](media/ReportMessageGETITNOW.png)<br/> 
    
3. 사용 및 개인정보 보호 정책 약관을 검토 합니다. 다음 **계속**을 선택 합니다. 
    
4. 진행 중인 작업 또는 학교 계정 (업무용) 또는 Microsoft 계정 (개인용)를 사용 하 여 Office 365 전자 메일에 로그인 합니다.
    

추가 기능에 설치 및 활성화, 후 다음과 같은 아이콘이 표시 됩니다. 

- Outlook에서 아이콘은 다음과 같습니다. <br/> ![Outlook에 대 한 보고서에서 메시지 추가 아이콘](media/OutlookReportMessageIcon.png)<br/>
- Outlook Web App에서 아이콘은 다음과 같습니다.<br/>![Outlook에서 웹 보고서 메시지 추가 아이콘](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

다음 단계에 대해 알아봅니다 [보고서 메시지 추가 기능을 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)하는 방법입니다.
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>조직에 대 한 보고서 메시지 추가 기능을 사용 하 고 확인

> [!IMPORTANT]
> 이 작업을 완료 하려면 Office 365 전역 관리자 또는 Exchange Online 관리자 여야 합니다.

1. 이동 [https://portal.office.com](https://portal.office.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다. 
    
2. **관리자** 가 관리 센터로 이동을 선택 합니다. 
    
3. **관리 센터** 를 선택 \> 하도록 **Exchange** 를 Exchange 관리 센터 (EAC)로 이동 합니다. 
    
4. **조직** 선택 \> **추가 기능**입니다. 
    
5. 선택 **+**  >  **Office 스토어에서 추가**합니다.<br/>![선택 Office 스토어에서 추가](media/EAC-Org-AddFromOfficeStore.png)<br/>그러면 Office 스토어 웹 브라우저에서 열립니다.
    
6. 보고서 메시지를 검색 합니다.<br/>![보고서 메시지에 대 한 검색](media/ReportMessageSearchOfficeStore.png)<br/>
    
7. **앱** 목록에서 **보고서 메시지**를 선택 하 고 **IT 가져오기 시작**을 선택 합니다.<br/>![선택 하면 이제 IT](media/ReportMessageGETITNOW.png)<br/> 
    
8. 사용 및 개인정보 보호 정책 약관을 검토 합니다. 다음 **계속**을 선택 합니다. 
    
    ![개인정보 보호 정책 계약에 동의 하려면 계속을 클릭](media/ReportMessageTermsAndConditions.png)
  
9. 보고서 메시지 추가 기능 검토의 정보를 구성 하 고 계속 하려면 **다음** 을 선택 하는데 도움이 되는 마법사가 열립니다.<br/>![Office 365에 대 한 마법사 추가 기능에서 메시지를 보고 합니다.](media/ReportMessageAdminInstallUI.png)<br/> 

10. 보고서 메시지 추가 기능에 대 한 사용자가 원하는 기본 설정을 지정 합니다.<br/>![보고서 메시지 추가 기능에 대 한 기본 설정 지정](media/ReportMessageUserOptionsAdminsSet.png)<br/>
    
11. 추가 기능에서 보고서 메시지를 누가 지정 합니다. <br/>![추가 기능에서 보고서 메시지를 누가 지정](media/ReportMessageChooseWhoGetsItAdminSettings.png)<br/>

12. **Save(저장)** 를 선택합니다. <br/>
> [!TIP]
> [사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙 설정](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users) 좋습니다.

어떤 사용자가 선택한 마법사를 사용 하 여를 따라 조직의 사용자는 [보고서 메시지 추가 기능에서](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) 사용할 수 있는 갖습니다. 조직의 사용자는 다음과 같은 아이콘이 표시 됩니다. 

- Outlook에서 아이콘은 다음과 같습니다. <br/> ![Outlook에 대 한 보고서에서 메시지 추가 아이콘](media/OutlookReportMessageIcon.png)<br/>
- Outlook Web App에서 아이콘은 다음과 같습니다.<br/>![Outlook에서 웹 보고서 메시지 추가 아이콘](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙을 설정 합니다.

> [!IMPORTANT]
> 이 작업을 수행 하려면 Exchange Online 관리자 여야 합니다.
  
조직에서 사용자가 보고 하는 전자 메일 메시지의 복사본을 가져오시겠습니까 규칙을 설정할 수 있습니다. 다운로드 하 고 조직에 대 한 보고서 메시지 추가 기능을 활성화 한 후이 작업을 수행 합니다.
  
1. EAC에서 **메일 흐름** 선택 \> **규칙**입니다. 
    
2. 선택 **+** \> **새 규칙 만들기**. 
    
3. **이름** 상자에 제출 등의 이름을 입력 합니다.
    
4. **이 규칙 적용 대상** 목록에서 **받는 사람 주소... 포함**을 선택 합니다. 
    
5. **단어 또는 구 지정** 화면에서 junk@office365.microsoft.com 및 phish@office365.microsoft.com를 추가 하 고 **확인**을 선택 합니다. 
    
    ![규칙에 대 한 정크 및 phish 전자 메일 주소를 지정 합니다.](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)
  
6. **다음 작업을 수행...** 목록에서 선택 **숨은 참조 메시지를...** 합니다. 
    
7. 전역 관리자, 보안 관리자 및/또는 사용자를 Microsoft에 보고 하는 각 전자 메일 메시지의 복사본을 받고 다음 **확인**을 선택 해야 보안 읽기 권한자를 추가 합니다. 
    
    ![보고 된 각 메시지의 복사본을 수신 하도록 글로벌 또는 보안 관리자 추가](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)
  
8. **감사 심각도 수준으로이 규칙**선택 하 고 **미디어**를 선택 합니다. 
    
9. **선택이 규칙에 대 한 모드** **적용**을 선택 합니다. 
    
    ![보고 된 각 메시지의 복사본을 가져오시겠습니까 규칙을 설정 합니다.](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)
  
10. **Save(저장)** 를 선택합니다. 
    
현재 위치에서이 규칙을 사용할 경우 보고서 메시지에서 추가 기능을 사용 하 여 전자 메일 메시지를 보고 하는 다른 사용자가 조직에서 때마다에 전역 관리자, 보안 관리자 및/또는 보안 판독기 복사본을 받게 됩니다 해당 메시지의 합니다. 이 정보를 사용 하면 설정 또는 정책, 예: [Office 365 ATP 안전한 링크](atp-safe-links.md) 정책 조정 수 있습니다. 

## <a name="review-or-edit-the-default-settings-for-the-report-message-add-in"></a>검토 또는 보고서 메시지 추가 기능에 대 한 기본 설정 편집

검토 수 있으며 보고서 메시지에서 추가 기능 관리 센터를 사용 하 여 기본 설정을 편집할 수 있습니다. 

> [!IMPORTANT]
> 이 작업을 완료 하려면 Office 365 전역 관리자 또는 Exchange Online 관리자 여야 합니다.
    
1. 방금 설치한 경우 보고서 메시지 추가 기능에서 조직에 대 한, 이미 수 서비스 및 추가 기능 페이지에서. 이동 하 고, [여기서](https://portal.office.com/adminportal/home#/Settings/ServicesAndAddIns) 와 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다.

2. **보고서 메시지**찾아 선택 합니다.<br/>![Office 365에 대 한 추가 기능 및 서비스](media/ReportMessage-o365servicesaddins.png)<br/> 
    
3. 창에는 배포 중에 보고서 메시지 추가 기능에 대해 선택 하는 설정을 표시 하는 열립니다.<br/>![보고서 메시지 추가 기능에 대 한 설정](media/ReportMessage-reviewaddinsettings.png)<br/> 

4. 검토 하 고 필요한 경우는 보고서 메시지에 추가 기능에 대 한 설정을 편집 하 고 변경 내용을 저장 합니다.
    
## <a name="learn-how-to-use-the-report-message-add-in"></a>보고서 메시지 추가 기능을 사용 하는 방법을 설명 합니다.

[보고서 메시지에서 추가 기능 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 참조 하십시오.
  
## <a name="related-topics"></a>관련 항목

[보고서 메시지 추가 기능을 사용 하 여](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터](view-email-security-reports.md)

[Office 365 고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)

[탐색기를 사용 하 여 보안에서 &amp; 준수 센터](use-explorer-in-security-and-compliance.md)
  

