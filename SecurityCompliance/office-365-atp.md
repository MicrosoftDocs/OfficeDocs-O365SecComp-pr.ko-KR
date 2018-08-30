---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/1/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Office 365 고급 위협 보호 스푸핑 인텔리전스, 안전한 링크, 안전한 첨부 파일 및 고급 피싱 방지 기능을 포함합니다. 또한 고급 위협 보호 비즈니스 및 팀이 Microsoft에 대 한 SharePoint Online, OneDrive의 파일에 확장 되 고 됩니다.
ms.openlocfilehash: dbf604dfc6367ac225e57158e6b784952c081773
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533535"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

Office 365 고급 위협 보호 (ATP) 하 여 악의적인 공격 으로부터 조직을 보호 하는데 도움이 됩니다.
  
- [ATP 안전한 첨부 파일이](atp-safe-attachments.md) 포함 된 전자 메일 첨부 파일 검사
    
- 전자 메일 메시지와 [ATP 안전 링크](atp-safe-links.md) 를 사용 하 여 Office 문서에서 검사 웹 주소 (Url)
    
- 식별 하 고 [SharePoint, OneDrive 및 Microsoft 팀의 ATP](atp-for-spo-odb-and-teams.md) 와 온라인 라이브러리에 악의적인 파일을 차단
    
- [위장 하거나 정보를 바탕](learn-about-spoof-intelligence.md) 으로 무단 스푸핑에 대 한 전자 메일 메시지를 확인 합니다.
    
- [Office 365의 ATP 피싱 방지 기능](atp-anti-phishing.md) 을 사용 하면 조직의 사용자 지정 도메인 및 사용자를 가장 하 려 하는 경우 검색
    
Office 365 ATP를 통해 보호 조직의 보안 팀 안전한 링크, 안전한 첨부 파일 및 피싱 방지에 대 한 정의 하는 정책에 의해 결정 됩니다. [보고서는 사용할 수](view-reports-for-atp.md) 조직에 대 한 ATP가 작동 하는 방법을 표시 합니다. 및 [의심 스러운 파일 분석을 위해 Microsoft에 제출할](office-365-atp.md#submitlalware)수 있습니다.
  
> [!IMPORTANT]
> Office 365 ATP 구독, 예: Office 365 엔터프라이즈 e 5 및 Office 365 교육 A5 하 고, 2018, 4 월 30 기준도 [Microsoft 365 비즈니스 보안 기능](https://support.office.com/article/c123694a-1efb-459e-a8d5-2187975373dc)에 포함 됩니다. 조직에 Office 365 ATP를 포함 하지 않는 한 Office 365 구독을 하는 경우에 추가 기능으로 ATP을 잠재적으로 구입할 수 있습니다. 자세한 내용은 [Office 365 고급 위협 Protection Service Description](https://technet.microsoft.com/library/exchange-online-advanced-threat-protection-service-description.aspx)을 참조 하십시오. 
      
## <a name="get-office-365-atp"></a>Office 365 ATP 가져오기

1. 관리자는 전역 또는 보안으로 이동 [https://portal.office.com](https://portal.office.com) 와 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. 
    
2. **관리** 를 선택 \> **대금 청구** 현재 구독에 포함 된 항목을 볼 수 있습니다. 
    
    ![관리로 이동 하 고 전역 관리자로 로그인 portal.office.com에서 \> 대금 청구](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)
  
3. **Office 365 엔터프라이즈 e 5**, **Office 365 교육 A5**또는 **Microsoft 365 비즈니스**을 참조 하는 경우 조직에 ATP 합니다. 
    
    **Office 365 엔터프라이즈 E3** 또는 **Office 365 Enterprise E1**등의 다른 구독을 참조 하는 경우에 ATP를 추가 하는 것이 좋습니다. 이렇게 하려면 **+ 추가 구독을**선택 합니다.
    
ATP를 만든 후 다음 단계에서는 보안 팀이 [안전한 링크](atp-safe-links.md), [안전한 첨부 파일](atp-safe-attachments.md)및 [피싱 방지](set-up-atp-anti-phishing-policies.md) 보호에 대 한 정책을 정의입니다. 
  
[무슨 작업을 하고 싶으십니까?](office-365-atp.md#TOC)
  
## <a name="define-policies-for-atp"></a>ATP에 대 한 정책 정의

- 조직의 [차단 된 사용자 지정 Url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md) 및 [사용자 지정 "rewrite 수행" Url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 등을 **[Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)**
    
- **[ATP 안전한 첨부 파일을 Office 365의 정책 설정](set-up-atp-safe-attachments-policies.md)** [동적 배달 하 고 미리 보는](dynamic-delivery-and-previewing.md) 포함 될 수 있는
    
- 신뢰할 수 있는 사용자 또는 도메인에서 것 처럼 보이는 **[Office 365의 ATP 피싱 방지 정책 설정](set-up-atp-anti-phishing-policies.md)** 가장 기반 공격을 포함 하는 전자 메일 메시지를 보낼 사람 공격자 로부터 보호 하기 위해 
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>보고서를 확인 하 여 ATP가 작동 하는 방법을 참조 하십시오.

ATP 정책이 설정 되어, 후 보고서는 서비스가 작동 하는 방법을 표시를 사용할 수 있습니다.

[![보안 &amp; 준수 센터 대시보드 도울수 위협 보호 고급가 작동 하는 위치를 참조 하십시오.](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Office 365 전역 관리자, 보안 관리자 또는 보안 판독기 되는지 확인 합니다. (참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md).)
    
2. [고급 위협 보호 및 Exchange Online 보호에 대 한 보고서 보기](view-reports-for-atp.md)입니다.
    
3. 필요한 경우에 보안 정책에 대 한 조정 확인 합니다. 다음 리소스를 참조 합니다.
    
  - [Office 365의 ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md)
    
  - [Office 365의 ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md)
    
  - [Office 365의 ATP 피싱 방지 정책](set-up-atp-anti-phishing-policies.md)
    
[무슨 작업을 하고 싶으십니까?](office-365-atp.md)
  
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>분석을 위해 Microsoft에 의심 스러운 파일 전송

맬웨어 수 것으로 의심 되는 파일을 가져오는 경우에 분석을 위해 Microsoft에 해당 파일을 제출할 수 있습니다. [Windows Defender 보안 인텔리전스 제출 포털](https://go.microsoft.com/fwlink/?linkid=857185)을 참고 하십시오.
  
## <a name="related-topics"></a>관련 항목

[Office 365 보안 개요 &amp; 준수 센터](https://support.office.com/article/a5f2fd18-b029-4257-b5a8-ae83e7768c85)
  
[고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)
  
[Office 365 보안의 관리 위협 &amp; 준수 센터](threat-management.md)
  

