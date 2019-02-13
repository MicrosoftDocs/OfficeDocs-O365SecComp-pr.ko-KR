---
title: 보안 강화를 위해 Office 365 테넌트 구성
ms.author: tracyp
author: BrendaCarter
manager: laurawi
ms.date: 10/11/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 8d274fe3-db51-4107-ba64-865e7155b355
description: Office 365 환경의 보안에 영향을 주는 테 넌 트 수준 설정에 대 한 권장된 구성을 안내 합니다. 보안 요구 사항을 더 많이 또는 적게 보안이 필요할 수 있습니다. 시작 지점으로 이러한 지침을 사용 합니다.
ms.openlocfilehash: 0ec9d739f1347eee55c4c49df2abfcb7178b6d05
ms.sourcegitcommit: 6bdba12c13c02f7d9a7297d3042933b100c4e481
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "29966202"
---
# <a name="configure-your-office-365-tenant-for-increased-security"></a>보안 강화를 위해 Office 365 테넌트 구성

이 항목에서는 Office 365 환경의 보안에 영향을 주는 테 넌 트 수준 설정에 대 한 권장된 구성을 안내 합니다. 보안 요구 사항을 더 많이 또는 적게 보안이 필요할 수 있습니다. 시작 지점으로 이러한 지침을 사용 합니다.
  
## <a name="check-office-365-secure-score"></a>Office 365 보안 점수를 확인 합니다.

Office 365 보안 점수 일반 작업 및 보안 설정에 따라 Office 365 조직의 보안을 분석 하 여 점수를 할당 합니다. 현재 점수가의 메모를 수행 하 여 시작 합니다. 일부 테 넌 트 수준의 설정을 조정 점수를 증가 합니다. 최대 점수를 달성 하기 위해 하지 하지만 사용자에 대 한 생산성 부정적인 영향을 하지 않는 환경을 보호 하기 위해 기회를 인식 하는 목표를 둡니다. [Office 365 보안 점수 소개 (영문)을](office-365-secure-score.md)참조 하십시오.
  
## <a name="tune-threat-management-policies-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안에서 위협 관리 정책 조정 &amp; 준수 센터

Office 365 보안 &amp; 준수 센터 환경을 보호 하는 기능을 포함 합니다. 보고서 및 대시보드를 모니터링 하 고 작업을 수행 하는데 사용할 수에 포함 됩니다. 일부 영역의 기본 정책 구성을 함께 제공 됩니다. 기본 정책 또는 규칙에는 일부 영역이 포함 되지 않습니다. 보다 안전한 환경에 대 한 위협 관리 설정을 조정 하려면 위협 관리에서 이러한 정책은 참고 하십시오. 
  
|영역 * * *|기본 정책 * 포함|권장 사항 * * *|
|:-----|:-----|:-----|
|**피싱 방지** <br/> |예  <br/> | 사용자 지정 도메인을 설치한 경우에 CEO, 예: 가장 중요 한 사용자의 전자 메일 계정을 보호 하기 위해 및 도메인을 보호 하기 위해 피싱 방지 정책을 만듭니다. [피싱 방지 정책 설정](set-up-anti-phishing-policies.md) 검토 하 고이 예제에서는 지침으로 사용 하 여 정책을 만들려면: "예제: 사용자 및 도메인을 보호 하기 위해 피싱 방지 정책."|
|**맬웨어 방지 엔진** <br/> |예  <br/> | 기본 정책을 편집 합니다.  <br/> &ensp;&ensp;• 일반적인 첨부 파일 필터 형식 —에서 선택  <br/><br>  사용자 지정 맬웨어 필터 정책을 만들 하 고 조직에 지정 된 사용자, 그룹 또는 도메인에 적용 수도 있습니다.  <br/> <br> 추가 정보:  <br/> &ensp;&ensp;• [맬웨어 방지 보호 기능](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx) <br/> &ensp;&ensp;• [맬웨어 방지 정책 구성](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |
|**ATP 안전한 첨부 파일** <br/> |아니요  <br/> | 안전한 첨부 파일에 대 한 기본 페이지에서이 확인란을 선택 하 여 SharePoint, OneDrive 및 Microsoft 팀의 파일을 보호 합니다.  <br/>  &ensp;&ensp;SharePoint, OneDrive 및 Microsoft 팀의 ATP • 설정  <br/> <br> 이러한 설정을 사용 하 여 새 안전한 첨부 파일 정책을 추가 합니다.  <br/>  &ensp;&ensp;• 블록 — 현재 및 미래의 전자 메일 및 검색 된 맬웨어를 가진 첨부 파일 차단 (이 옵션을 선택 합니다.)  <br/>  &ensp;&ensp;• 사용 리디렉션-(이 확인란을 선택 하 고 관리자 또는 격리 계정 등의 전자 메일 주소를 입력 합니다.)  <br/>  &ensp;&ensp;• 맬웨어 첨부 파일에 대 한 검사 시간 초과 또는 오류가 발생 하는 경우 위의 선택 영역을 적용 (이 상자를 선택)  <br/>  &ensp;&ensp;•에 적용 된 — 도메인은 (선택) 도메인의 받는 사람  <br/>  <br>자세한 내용은: [Office 365 ATP 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md) <br/> |
|**ATP 안전한 링크** <br/> |예  <br/> | 이 설정은 전체 조직에 대 한 기본 정책에 추가 합니다.  <br/> &ensp;&ensp;• 사용에 안전 링크: Office 365 ProPlus, iOS에 대 한 Office 및 Android (이 옵션을 선택 합니다.).  <br/> <br>특정 받는 사람에 대 한 권장된 하는 정책:  <br/>  &ensp;&ensp;• Url 다시 작성 하 고 사용자가 링크를 클릭할 때의 알려진된 악의적인 링크 목록에 대해 확인 됩니다 (이 옵션을 선택 합니다.).  <br/>  &ensp;&ensp;• 사용 하 여 안전한의 첨부 파일을 다운로드할 수 있는 콘텐츠를 검사 (이 확인란을).  <br/>  &ensp;&ensp;•에 적용 된 — 도메인은 (선택) 도메인의 받는 사람입니다.  <br/> <br> 자세한 내용은: [Office 365 ATP 안전한 링크](atp-safe-links.md)입니다.  <br/> |
|**스팸 방지 (메일 필터링)** <br/> |예  <br/> | 로깅으로 인 한 한 내용:  <br/>  &ensp;&ensp;• 너무 많이 스팸-사용자 지정 설정을 선택 하 고 기본 스팸 필터 정책을 편집 합니다.  <br/>  &ensp;&ensp;• 스푸핑 인텔리전스 — 도메인 스푸핑는 보낸사람을 검토 합니다. 차단 또는 이러한 보낸사람 허용 합니다.<br/>  <br>자세한 내용은: [Office 365 전자 메일 스팸 방지 보호 기능](anti-spam-protection.md)입니다.  <br/> |
|***전자 메일 인증*** <br/> |예  <br/> |전자 메일 인증 도메인 이름 시스템 (DNS)를 사용 하 여 전자 메일의 보낸사람에 대 한 전자 메일 메시지를 확인할 수 있는 정보를 추가 합니다. 해당 기본 도메인 (onmicrosoft.com)에 대 한 전자 메일 인증을 설정 하는 office 365 이지만 Office 365 관리자가 사용자 지정 도메인에 대 한 전자 메일 인증을 사용할 수도 있습니다. 세가지 인증 방법은 사용 됩니다.<br/> <br> &ensp;&ensp;• 보낸 사람이 정책 프레임 워크 (또는 SPF)입니다.<br/>&ensp;&ensp;&ensp;&ensp;-설치 프로그램에 대 한 [스푸핑을 방지 하기 위해 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)을 참조 하십시오. <br/> &ensp;&ensp;• DomainKeys 메일 (DKIM)를 식별 합니다. <br/> &ensp;&ensp;&ensp;&ensp;- [Office 365에서 사용자 지정 도메인의 전자 메일에 대 한 사용 DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)를 참조 하십시오. <br>&ensp;&ensp;&ensp;&ensp;-DKIM을 구성한 후에 보안 사용 &amp; 준수 센터입니다.<br/> &ensp;&ensp;• 도메인 기반 메시지 인증, 보고 및 적합성 (DMARC). </br> &ensp;&ensp;&ensp;&ensp;-DMARC에 대 한 [Office 365의 전자 메일의 유효성을 검사를 사용 하 여 DMARC](use-dmarc-to-validate-email.md)를 설치 합니다.<br/>  <br/>
|

> [!NOTE]
> SPF의 비표준 배포, 하이브리드 배포 하 고 문제를 해결 하는 것에 대 한: [Office 365 어떻게 스푸핑을 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)를 사용](how-office-365-uses-spf-to-prevent-spoofing.md)합니다.

## <a name="view-dashboards-and-reports-in-the-security-amp-compliance-center"></a>보안에서 대시보드 및 보고서를 보려면 &amp; 준수 센터

이러한 보고서 및 대시보드 환경의 상태에 대 한 자세한 정보를 참고 하십시오. 이러한 보고서의 데이터를 Office 365 서비스를 사용 하는 조직으로 다양 한 될 수 있습니다. 이제 기능을 모니터링 하는 조치를 취할 잘 알고 있어야 합니다. 자세한 내용은 참조: [Office 365 보안에서 보고서 &amp; 준수 센터](reports-in-security-and-compliance.md)합니다.
  
|대시보드 * * *|****Description****|
|:-----|:-----|
|위협 관리 대시보드  <br/> |보안 위협 관리 섹션에서 &amp; 준수 센터, 보안 위협 인텔리전스 이미 수행 기능에 비즈니스 의사 결정자를 보고용 이미 처리 하는 참조 위협에 대 한 편리한 도구로이 대시보드를 사용 하면 비즈니스 합니다.  <br/> |
|위협 탐색기  <br/> |보안 위협 관리 섹션에도 &amp; 준수 센터입니다. 조사 또는 Office 365 테 넌 트에 대해 공격이 발생 하는 경우에 위협 탐색기를 사용 하 여 위협 요소를 분석 합니다. 위협 탐색기에 표시 되는 볼륨 공격을 시간이 지남에 따라 및 위협 제품군을 공격자가 인프라 하 여이 데이터를 분석할 수 있습니다. 인시던트 목록에 대 한 모든 의심 스러운 전자 메일을 표시할 수도 있습니다.  <br/> |
|보고서-대시보드  <br/> |보안 보고서 섹션에서 &amp; SharePoint Online 및 Exchange Online 조직에 대 한 준수 센터 보기 감사 보고 합니다. 또한 보고서에 액세스할 수 Azure Active Directory (AD) 사용자 로그인, 사용자 활동 보고서 및 보기 보고서 페이지에서 Azure AD 감사 로그 합니다.  <br/> |
   
![보안 &amp; 준수 센터 대시보드](media/870ab776-36d2-49c7-b615-93b2bc42fce5.png)
  
## <a name="configure-additional-exchange-online-tenant-wide-settings"></a>추가 Exchange Online 테 넌 트 수준 설정 구성

다양 한 Exchange 관리 센터의 보안 및 보호에 대 한 컨트롤 보안 및 규정 준수 센터에도 포함 됩니다. 양쪽 모두에 이러한 구성할 필요가 없습니다. 권장 되는 추가 설정 몇 다음과 같습니다. 
  
|영역 * * *|기본 정책 * 포함|권장 사항 * * *|
|:-----|:-----|:-----|
|**메일 흐름** (전송 규칙)  <br/> |아니요  <br/> | Ransomware 로부터 보호 하는 메일 흐름 규칙을 추가 합니다. 이 블로그 (영문) 문서에서 "Exchange 전송 규칙을 사용 하 여 추적 또는 ransomware에서 사용 하는 파일 확장명을 가진 전자 메일을 차단 하는 방법"을 참조: [ransomware을 처리 하는 방법](https://blogs.technet.microsoft.com/office365security/how-to-deal-with-ransomware/)입니다.<br><br/> 외부 도메인에 전자 메일의 자동 착신 전환을 방지 하기 위해 전송 규칙을 만듭니다. 자세한 내용은 [Rules](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/)를 참조 완화 클라이언트 외부 착신 전환 점수가 보안을 유지 합니다.<br/> <br>자세한 내용은: [메일 흐름 규칙 (전송 규칙) Exchange Online](https://technet.microsoft.com/en-us/library/jj919238%28v=exchg.150%29.aspx) <br/> |
|**현대 인증을 사용 하도록 설정** <br/> |아니요  <br/> | Office 365의 최신 인증 필요 하다는 사실을 다단계 인증 (MFA)를 사용 합니다. MFA 전자 메일을 포함 하 여 클라우드 리소스에 대 한 액세스를 보호 하기 위한 것이 좋습니다.<br/>  <br>다음이 항목을 참조 합니다.  <br/> • [사용 하거나 사용 하지 않도록 현대 인증 Exchange 온라인](https://support.office.com/article/58018196-f918-49cd-8238-56f57f38d662) <br/> • [비즈니스 온라인 용 Skype: 현대 인증에 대 한 테 넌 트를 사용 하도록 설정](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br/>  <br>현대 인증이 Office 2016 클라이언트, SharePoint Online 및 비즈니스용 OneDrive에 대 한 기본적으로 사용 됩니다.  <br/>  <br>자세한 내용은: [Office 클라이언트를 사용 하 여 Office 365를 사용 하 여 최신 인증](https://support.office.com/article/776c0036-66fd-41cb-8928-5495c0f9168a) <br/> |
   
## <a name="configure-tenant-wide-sharing-policies-in-sharepoint-admin-center"></a>SharePoint 관리 센터에서 테 넌 트 수준의 공유 정책 구성

초기 계획 보호로 시작 하 여 보호 수준을 활용 하는 동시에 SharePoint 팀 사이트를 구성 하기 위한 권장 합니다. 자세한 내용은 [SharePoint Online 보안 사이트 및 파일을](https://docs.microsoft.com/microsoft-365-enterprise/secure-sharepoint-online-sites-and-files) 참조 하십시오.
  
초기 계획 수준에서 구성 된 SharePoint 팀 사이트 링크 익명 액세스를 사용 하 여 외부 사용자와 파일 공유를 허용 합니다. 전자 메일에 파일을 전송 하는 대신이 방법을 사용 하는 것이 좋습니다. 
  
초기 계획 보호를 위한 목표를 지원 하기 위해 여기서 권장 하는 대로 테 넌 트 수준의 공유 정책을 구성 합니다. 개별 사이트에 대 한 설정을 공유 하는 것은 더 하지 허용 하지만이 테 넌 트 수준 정책 보다 제한적인 수 있습니다. 
  
|영역 * * *|기본 정책 * 포함|권장 사항 * * *|
|:-----|:-----|:-----|
|**공유** (SharePoint Online 및 비즈니스용 OneDrive)  <br/> |예  <br/> | 외부 공유는 기본적으로 활성화 됩니다. 이러한 설정은 사용 하는 것이 좋습니다.<br/>  • 인증 된 외부 사용자를 공유 하 고 익명 액세스 링크 (기본 설정)를 사용 하 여 허용 합니다.  <br/>  • 익명 액세스 링크 동안 일 후에 만료 됩니다. 30 일 등 원하는 경우 번호를 입력 합니다.<br/>  • 기본 링크 형식-내부 (조직 내 사용자에만 해당)를 선택 합니다. 익명 링크를 사용 하 여 공유 하려는 사용자는 공유 메뉴에서이 옵션을 선택 해야 합니다.<br/>  <br>자세한 정보: [외부 공유 개요 (영문)](https://support.office.com/article/c8a462eb-0723-4b0b-8d0a-70feafe4be85) <br/> |
   
SharePoint 관리 센터 및 비즈니스 관리 센터에 대 한 OneDrive 동일한 설정을 포함 합니다. 두 관리 센터에서 설정을 모두에 적용 됩니다.
  
## <a name="configure-settings-in-azure-active-directory"></a>Azure Active Directory의 설정 구성

보다 안전한 환경에 대 한 테 넌 트 전체 설치를 완료 하기 위해 Azure Active Directory에서 이러한 두 영역을 방문 해야 합니다.
  
### <a name="configure-named-locations-under-conditional-access"></a>(조건부 액세스)에서 명명 된 위치를 구성 합니다.

조직의 보안 네트워크 액세스 권한이 있는 사무실을 포함 하는 경우는 명명 된 위치로 Azure Active Directory에 신뢰할 수 있는 IP 주소 범위를 추가 합니다. 이 기능에 대 한 로그인 위험 이벤트가 가양성 보고 된 횟수를 줄일 수 있습니다. 
  
참조: [Azure Active Directory에서 명명 된 위치](https://docs.microsoft.com/azure/active-directory/active-directory-named-locations)
  
### <a name="block-apps-that-dont-support-modern-authentication"></a>현대 인증을 지원 하지 않는 앱 차단

다단계 인증 현대 인증을 지 원하는 앱 필요 합니다. 현대 인증을 지원 하지 않는 앱 조건부 액세스 규칙을 사용 하 여 차단할 수 없습니다.
  
보안 환경에 대 한 최신 인증을 지원 하지 않는 응용 프로그램에 대 한 인증을 사용 하지 않도록 설정 해야 합니다. 출시 예정 하는 컨트롤과 함께 Azure Active Directory에서 수행할 수 있습니다.
  
SharePoint Online 및 비즈니스용 OneDrive에 대 한이 수행 하기 위해 다음 방법 중 하나를 사용 동시에:
  
- PowerShell을 사용 하 여 [최신 인증을 사용 하지 않는 앱 차단을](https://docs.microsoft.com/intune-classic/deploy-use/block-apps-with-no-modern-authentication)참조 하십시오.
    
- SharePoint 관리 센터에서이 구성의 "장치 액세스 페이지-"현대 인증을 사용 하지 않는 응용 프로그램에서의 액세스를 제어 합니다." 블록 선택 합니다. 
    
## <a name="get-started-with-cloud-app-security-or-office-365-cloud-app-security"></a>클라우드 앱 보안 또는 Office 365 클라우드 앱 보안 시작 하기

Office 365 클라우드 응용 프로그램 보안을 사용 하 여 의심 스러운 활동에 대 한 경고를 위험을 평가 하 고 자동으로 작업도 하지 않습니다. Office 365 e 5 계획을 해야합니다.
  
또는 Microsoft 클라우드 응용 프로그램 보안을 사용 하 여 심도 있는 액세스 권한을 부여 한 후에, 포괄적인 컨트롤 및 모든 클라우드 등 응용 프로그램 Office 365에 대 한 향상 된 보호를 얻으려고 합니다. 
  
이 솔루션을 EMS e 5 계획 권장, 때문에 사용할 수 있도록이 다른 SaaS 응용 프로그램과 사용자 환경에서 클라우드 앱 보안이 설정 된 시작 하는 것이 좋습니다. 기본 정책 및 설정으로 시작 합니다.
  
추가 정보:
  
- [Cloud App Security 배포](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)
    
- [Microsoft Cloud App Security에 대한 자세한 정보](https://www.microsoft.com/en-us/cloud-platform/cloud-app-security)
    
- [Office 365 Cloud App Security 개요](office-365-cas-overview.md)
    
![Cloud App Security 대시보드](media/1fb2aa65-54b8-4746-9f5e-c187d339e9f5.png)
  
## <a name="additional-resources"></a>추가 리소스

이러한 문서와 가이드 Office 365 환경 보호를 위한 추가 규정 정보를 제공 합니다.
  
- [정치적 캠페인, 비영리, 및 기타 민첩 한 조직에 대 한 Microsoft 보안 지침](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance) (모든 환경, 특히 클라우드 전용 환경에서에서 이러한 권장 사항 사용할 수) 
    
- [권장 보안 정책 및 id 및 장치에 대 한 구성](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-365-policies-configurations) (이러한 권장 사항 AD FS 환경에 대 한 도움말을 포함) 
    

