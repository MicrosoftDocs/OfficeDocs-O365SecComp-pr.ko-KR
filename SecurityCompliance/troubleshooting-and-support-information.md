---
title: 문제 해결 및 지원 정보
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5d9f75f5-bb7f-458c-ad30-5c8eae0b0e4e
ms.collection:
- M365-security-compliance
description: 이 항목에서는 최종 사용자 및 관리자를 위한 문제 해결 단계 및 기술 지원 서비스에 문의하는 방법에 대해 설명합니다.
ms.openlocfilehash: 43af048a457835ef16e36c8587f811cb0963bc97
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670483"
---
# <a name="troubleshooting-and-support-information"></a>문제 해결 및 지원 정보

이 항목에서는 최종 사용자 및 관리자를 위한 문제 해결 단계 및 기술 지원 서비스에 문의하는 방법에 대해 설명합니다.
  
## <a name="troubleshooting-for-users"></a>사용자를 위한 문제 해결

경우에 따라 정크 메일 보고 추가 기능을 추가한 후 Microsoft Office Outlook에 문제가 발생할 수 있습니다. 아래에 발생할 수 있는 문제 및 이러한 문제를 해결하는 팁이 나와 있습니다. 
  
- **정크 메일 보고**를 클릭해도 아무 작업도 수행되지 않음
    
- 전자 메일 메시지를 선택한 후 Outlook의 응답이 중지됨
    
- "배달 불능" 응답으로 인해 보고된 정크 메일을 배달할 수 없음
    
### <a name="troubleshooting-tip"></a>문제 해결 팁

1. Microsoft Office Outlook을 닫았다가 다시 시작합니다.
    
2. 테스트 메시지를 만들고 보낼 수 있는지 확인합니다. 이렇게 하려면 테스트 메시지를 사용자의 다른 전자 메일 계정으로 보낸 다음 이 전자 메일 메시지가 수신되었는지 확인하면 됩니다.
    
문제가 계속되면 IT 관리자에게 문의하십시오.
  
> [!TIP]
> 또한 스팸 메시지는 전자 메일 주소 [junk@office365.microsoft.com](mailto:junk@office365.microsoft.com)으로, 그리고 가양성 메시지는 [not_junk@office365.microsoft.com](mailto: not_junk@office365.microsoft.com)으로 Microsoft에 직접 제출할 수도 있습니다. 자세한 내용은 [분석을 위해 Microsoft에 스팸 및 스팸이 아닌 메시지 제출을](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)참조 하세요. 
  
## <a name="troubleshooting-for-administrators"></a>관리자를 위한 문제 해결

Microsoft Office Outlook용 정크 메일 신고 추가 기능을 관리자로서 사용하는 사용자에게 문제가 발생할 수 있습니다. 아래에 이러한 문제를 해결하는 일부 팁이 나와 있습니다. 
  
 **문제:** 시스템 관리자에게 문의하라는 오류 메시지가 사용자에게 계속해서 표시됩니다. 
  
### <a name="troubleshooting-tip"></a>문제 해결 팁

1. 다음 레지스트리 키 값을 "Verbose"로 설정합니다.
    
  - **32비트 운영 체제에 설치된 32비트 Outlook:**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
  - **64비트 운영 체제에 설치된 32비트 Outlook:**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
  - **64비트 Outlook(항상 64비트 운영 체제에 설치됨):**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
2. Microsoft Office Outlook을 다시 시작하고 오류 메시지가 표시되면 다시 보고하도록 사용자에게 요청합니다.
    
3. 다음 위치에 있는 로그 정보를 수집합니다. 
    
    %LOCALAPPDATA%\Microsoft\Junk Email Reporting Add-in\SpamReporterAddinLog.txt
    
4. Exchange Online Protection 기술 지원 서비스에 문의하여 로그 정보를 제공합니다. 
    
 **문제:** 사용자가 정크 메일로 전자 메일을 보낼 때 확인을 수신하지 않도록 선택했지만 다시 확인을 수신하려고 합니다. 
  
### <a name="troubleshooting-tip"></a>문제 해결 팁

1. 다음 레지스트리 키 값을 "True"로 설정합니다. HKEY_CURRENT_USER\Software\Microsoft\Junk E-mail Reporting\Preferences\ConfirmReportJunk
    
2. Microsoft Office Outlook을 다시 시작합니다.
    
## <a name="support-information"></a>지원 정보

추가 기능의 설치, 구성 또는 제거에 대 한 도움이 필요한 경우 Microsoft 365 관리 센터의 지원 페이지에서 새 서비스 요청 링크를 사용 하 여 기술 지원에 문의 하세요. 전화 및 자가 지원 옵션을 통해 서비스 요청을 제출 하는 등의 추가 옵션을 보려면 [EOP에 대 한 도움말 및 지원을](eop/help-and-support-for-eop.md)참조 하십시오.
  
## <a name="for-more-information"></a>자세한 내용

[보고서 메시지 추가 기능을 사용하도록 설정](https://support.office.com/article/4250c4bc-6102-420b-9e0a-a95064837676)
  
[Microsoft에 정크 메일 메시지 보고](report-junk-email-messages-to-microsoft.md)
  

