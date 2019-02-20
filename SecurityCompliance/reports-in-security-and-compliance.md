---
title: Office 365 보안 및 준수 센터의 보고서
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: 'Office 365 Security & 준수 센터를 사용 하 여 SharePoint online 및 Exchange Online 조직에 대 한 다양 한 보고서 및 Azure Active Directory 보고서를 확인할 수 있습니다.  '
ms.openlocfilehash: 36e6d3efce1758d52cd30451a2b60b19f4654056
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087307"
---
# <a name="reports-in-the-office-365-security--compliance-center"></a>Office 365 보안 및 준수 센터의 보고서

Office 365 Security & 준수 센터의 **보고서 보기** 페이지를 사용 하 여 SharePoint online 및 Exchange Online 조직에 대 한 감사 보고서에 빠르게 액세스할 수 있습니다. **보고서 보기** 페이지에서 azure Active Directory (AD) 사용자 로그인 보고서, 사용자 활동 보고서 및 azure ad audit 로그에 액세스할 수도 있습니다. 이는 유료 Office 365 구독에 Microsoft Azure에 대 한 무료 구독이 포함 되어 있기 때문입니다. 이러한 Azure 보고서에 처음 액세스 하려고 하면 일회성 등록 프로세스를 완료 해야 합니다. 
  
> [!TIP]
> office 365 조직의 활동에 대 한 추가 보고서를 보려면 [office 365 관리 센터의 활동 보고서](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263)를 참조 하세요. 
  
 **시작하기 전에**
  
보안 & 준수 센터에서 보고서를 보려면 다음 사용 권한이 필요 합니다.
  
- 보안 & 준수 센터에서 보고서를 보려면 EAC (Exchange 관리 센터)에서 보안 독자 역할을 할당 받아야 합니다. 기본적으로이 역할은 EAC의 조직 관리 및 보안 독자 역할 그룹에 할당 됩니다.
    
- 보안 & 준수 센터에서 dlp 보고서를 보려면 security & 준수 센터에서 보기 전용 DLP 준수 관리 역할을 할당 받아야 합니다. 기본적으로이 역할은 보안 & 준수 센터의 준수 관리자, 조직 관리, 보안 관리자 및 보안 독자 역할 그룹에 할당 됩니다.

- 또한 eac에서 보기 전용 받는 사람 역할을 할당 하 여 eac에서 DLP 보고서를 볼 수 있습니다. 기본적으로이 역할은 EAC의 준수 관리, 조직 관리 및 보기 전용 조직 관리 역할 그룹에 할당 됩니다.
  
 **보안 & 준수 센터에서 보고서 보기 페이지를 열려면**
  
1. [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports)으로 이동합니다.
    
2. office 365 조직의 사용자 계정에 대 한 자격 증명을 사용 하 여 office 365에 로그인 합니다.
    
**보고서 보기** 페이지에서 다음과 같은 유형의 보고서를 볼 수 있습니다. 
  
- [EOP의 감사 보고서](#auditing-reports)
- [관리 검토 보고서](#supervisory-review-report)
- [데이터 손실 방지 역할](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>감사 보고서

다음 표에서는 Security & 준수 센터의 **보고서 보기** 페이지에 있는 **감사** 섹션의 보고서에 대해 설명 합니다. 
  
|**보고서**|**설명**|
|:-----|:-----|
|**Office 365 감사 로그 보고서** <br/> |office 365 조직에서 사용자 및 관리자 활동에 대 한 office 365 감사 로그를 검색할 수 있습니다. 이 보고서에는 Office 365의 디렉터리 서비스인 Exchange online, SharePoint online, 비즈니스용 OneDrive 및 Azure Active Directory의 항목 사용자 및 관리자 작업이 포함 되어 있습니다. 자세한 내용은 [Office 365 Security & 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.<br/> |
|**Azure 광고 보고서** <br/> |Office 365 조직에서 비정상적인 또는 의심 스러운 로그인 활동을 확인 하려면 Microsoft Azure에서 로그인 및 활동 보고서를 사용할 수 있습니다. Azure AD audit 로그에서 이벤트를 볼 수도 있습니다. azure에서 보고서를 보려면 **azure AD 보고서 보기**를 클릭 하면 됩니다. 자세한 내용은 다음 항목을 참조 하십시오.<br/><br/>[Office 365에서 무료 Azure Active Directory 구독을 사용](use-your-free-azure-ad-subscription-in-office-365.md)합니다. <br/> [액세스 및 사용 현황 보고서를 봅니다](http://go.microsoft.com/fwlink/p/?LinkId=506902).  <br/> |
|**Exchange 감사 보고서** <br/> | Office 365의 감사 기능을 사용 하 여 조직의 관리자가 Exchange Online 구성에 수행한 변경 내용을 추적할 수 있습니다. Microsoft 데이터 센터 관리자 또는 위임 된 관리자가 Exchange Online 조직에 대해 수행한 변경 내용도 로깅됩니다. Exchange Online의 경우 관리자 감사 로깅은 기본적으로 사용 하도록 설정 되므로 모든 작업을 수행 하지 않아도 됩니다. 또한 Exchange Online은 사서함 소유자가 아닌 다른 사용자가 사서함에 대 한 액세스를 추적할 수 있도록 사서함 감사 로깅을 제공 합니다. 비 소유자 액세스를 추적 하려는 각 사서함에 대해 사서함 감사 로깅을 사용 하도록 설정 해야 합니다.<br/>  관리자 및 사서함 감사 로깅 둘 다에 대해 감사 보고서를 실행 하 여 감사 로그 항목을 볼 수 있습니다. 전자 메일 메시지에 첨부 된 XML 파일에서 24 시간 내에 전송 되는 사서함 및 관리자 감사 로그를 내보낼 수도 있습니다.<br/><br/>감사 로그를 내보내는 방법에 대 한 자세한 내용은 다음을 참조 하십시오.  <br/><br/> [사서함 감사 로그 내보내기](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [데이터 센터 관리자 감사 로그 보기 및 내보내기](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [역할 그룹 변경 또는 관리자 감사 로그 검색](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Exchange 감사 보고서](http://go.microsoft.com/fwlink/p/?LinkID=395232)  <br/> |
   
## <a name="supervisory-review-report"></a>관리 검토 보고서

관리 검토 보고서를 사용 하 여 조직의 모든 관리 검토 정책 상태를 확인할 수 있습니다. 자세한 내용은 [Configure 관리 review 정책도 조직에 대해](configure-supervision-policies.md)참조 하십시오.
  
## <a name="data-loss-prevention-reports"></a>데이터 손실 방지 역할

dlp (데이터 손실 방지) 보고서에는 dlp 정책에 대 한 정보가 포함 되 고 콘텐츠에 적용 된 규칙에는 Office 365 조직에서 중요 한 데이터가 포함 됩니다. dlp 정책 및 규칙을 기반으로 하는 dlp 작업에 대 한 정보를 표시 하도록 보고서를 구성할 수도 있습니다. 자세한 내용은 [데이터 손실 방지에 대 한 보고서 보기](view-the-dlp-reports.md)를 참조 하세요.
