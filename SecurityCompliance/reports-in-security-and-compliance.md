---
title: Office 365 보안에서 보고서 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/1/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: 'Office 365 보안을 사용 하 여 &amp; SharePoint Online 및 Exchange Online 조직에 대 한 다양 한 보고서를 가져올 준수 센터 + Azure Active Directory를 보고 합니다.  '
ms.openlocfilehash: 019ccc49352db1aaf392287f62fa63f66913e293
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038341"
---
# <a name="reports-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안에서 보고서 &amp; 준수 센터

**보고서 보기** 페이지를 사용 하 여 Office 365 보안에서 수 &amp; 준수 센터 SharePoint Online 및 Exchange Online 조직에 대 한 감사 보고서를 신속 하 게 액세스할 수 있습니다. 또한 보고서에 액세스할 수 Azure Active Directory (AD) 사용자 로그인, 사용자 활동 보고서 및 Azure AD 감사 로그 **보고서 보기** 페이지에서 합니다. 이 유료 Office 365 구독 Microsoft Azure에 대 한 무료 구독을 포함 합니다. 처음으로 이러한 Azure 보고서에 액세스 하려고 하는 일회성 등록 프로세스를 완료 해야 합니다. 
  
> [!TIP]
> Office 365 조직에서 작업 하는 방법에 대 한 추가 보고서를 보려면 [Office 365 관리 센터에서 활동 보고서](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263)를 참조 하십시오. 
  
 **시작하기 전에**
  
보안에서 보고서를 보려면 다음 사용 권한이 필요 &amp; 준수 센터입니다.
  
- Exchange 관리 센터의 보안에서 보고서를 보려면 (EAC)에서 보안 판독기 역할을 할당 해야하는 &amp; 준수 센터입니다. 기본적으로이 역할은 EAC에서 조직 관리 및 보안 판독기 역할 그룹에 할당 됩니다.
    
- 보안에서 DLP 규정 준수 관리 역할을 할당 해야하는 &amp; 보안에서 DLP 보고서 (및 DLP 정책)를 보려면 준수 센터 &amp; 준수 센터입니다. 기본적으로이 역할의 보안에서 규정 준수 관리자, 조직 관리 및 보안 관리자 역할 그룹에 할당 된 &amp; 준수 센터입니다.
    
또한이 해야 DLP 보고서 (및 DLP 정책)를 볼 수 EAC에서 데이터 손실 방지 역할을 할당 받을 EAC에서. 기본적으로이 역할은 EAC에서 규정 준수 관리 및 조직 관리 역할 그룹에 할당 됩니다.
  
 **보안에서 보기 보고서 페이지를 열려면 &amp; 준수 센터:**
  
1. [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports)으로 이동합니다.
    
2. Office 365 조직에서 사용자 계정에 대 한 자격 증명을 사용 하 여 Office 365에 로그인 합니다.
    
**보고서 보기** 페이지에서 다음과 같은 종류의 보고서를 볼 수 있습니다. 
  
- [EOP의 감사 보고서](#auditing-reports)
- [감독 검토 보고서](#supervisory-review-report)
- [데이터 손실 방지 역할](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>감사 보고서

다음 표에서 보안에서 **보고서 보기** 페이지에서 보고서의 **감사** 섹션에 설명 &amp; 준수 센터입니다. 
  
|**보고서**|**설명**|
|:-----|:-----|
|**Office 365 감사 로그 보고서** <br/> |Office 365 조직에서 사용자 및 관리자 작업에 대 한 Office 365 감사 로그를 검색할 수 있습니다. 보고서는 비즈니스 및 Office 365에 대 한 디렉터리 서비스에 해당 하는 Azure Active Directory에 대 한 Exchange Online, SharePoint Online, OneDrive에서 사용자 및 관리자 작업 항목을 포함 합니다. 자세한 내용은 참조 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md)합니다.<br/> |
|**Azure 광고 보고서** <br/> |활동에 대 한 특별 한 또는 의심 스러운 로그인 Office 365 조직에서 찾을, 로그인 하 고 작업을 사용할 수 Microsoft Azure의 보고서입니다. Azure AD 감사 로그에 이벤트를 볼 수 있습니다. Azure에 보고서를 보려면 방금 **보고서를 볼 Azure AD**클릭 합니다. 자세한 내용은 다음을 참조 합니다.<br/><br/>[Office 365의 무료 Azure Active Directory 구독에 사용](use-your-free-azure-ad-subscription-in-office-365.md)합니다. <br/> [액세스 및 사용 현황 보고서 보기](http://go.microsoft.com/fwlink/p/?LinkId=506902)입니다.  <br/> |
|**Exchange 감사 보고서** <br/> | 조직의 관리자가 Exchange Online 구성에 대 한 변경 내용을 추적 하려면 Office 365의 감사 기능을 사용할 수 있습니다. Microsoft 데이터 센터 관리자에 의해 또는 위임 된 관리자가 Exchange Online 조직에 대 한 변경 내용은 로그에 기록 됩니다. Exchange Online 관리자 감사에 대 한을 켜는 아무 작업도 수행 하지 않아도 되므로 로깅은 기본적으로 사용 됩니다. Exchange Online 사서함 감사 로깅 사서함 소유자 이외의 사용자가 사서함에 대 한 액세스를 추적할 수로 제공 합니다. 비 소유자 액세스를 추적 하려는 각 사서함에 대 한 로깅 사서함 감사를 사용 하도록 설정 해야 합니다.<br/>  관리자와 사서함에 대 한 감사 로깅, 감사 로그 항목을 보려면 감사 보고서를 실행할 수 있습니다. 전자 메일 메시지에 첨부 된 XML 파일의 24 시간 내에서 전송 되는 사서함 및 관리자 감사 로그를 내보낼 수도 있습니다.<br/><br/>감사 로그 내보내기 (영문) 하는 방법에 대 한 자세한 내용은 다음을 참조 합니다.  <br/><br/> [사서함 감사 로그 내보내기](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [보기 및 데이터 센터 관리 감사 로그 내보내기](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [역할 그룹 변경 내용을 검색 또는 관리자 감사 로그](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Exchange 감사 보고서](http://go.microsoft.com/fwlink/p/?LinkID=395232)입니다.  <br/> |
   
## <a name="supervisory-review-report"></a>감독 검토 보고서

감독 검토 보고서와 함께 조직에서 모든 감독 검토 정책의 상태를 볼 수 있습니다. 자세한 내용은 [Configure 감독 검토 하면 조직에 대 한 정책을](configure-supervision-policies.md)참조 하십시오.
  
## <a name="data-loss-prevention-reports"></a>데이터 손실 방지 역할

DLP 정책에 대 한 정보를 포함 하 고 Office 365 조직에 중요 한 데이터를 포함 하는 내용에 적용 된 규칙을 보고 하는 데이터 손실 방지 (DLP)입니다. DLP 정책 및 규칙에 따라 된 DLP 작업에 대 한 정보를 표시 하도록 보고서를 구성할 수도 있습니다. 자세한 내용은 [데이터 손실 방지에 대 한 보고서 보기](view-the-dlp-reports.md)를 참조 하십시오.
