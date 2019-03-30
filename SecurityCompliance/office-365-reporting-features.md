---
title: Office 365 보고 기능
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
description: Office 365 내의 보고 기능에 대 한 설명입니다.
ms.openlocfilehash: 5e765045982d6788ee93550fa8041a52efb306c0
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000251"
---
# <a name="office-365-reporting-features"></a>Office 365 보고 기능 

## <a name="introduction"></a>소개
Office 365의 Reports 기능은 Azure AD (Active Directory), Exchange Online, 장치 관리, 관리 검토 및 DLP (데이터 손실 방지)에 대 한 다양 한 감사 보고서를 제공 합니다. 이러한 기능은 Office 365 활동 보고서와는 별개 이며 서로 다릅니다.

## <a name="office-365-reports-dashboard"></a>Office 365 보고서 대시보드
Microsoft 365 관리 센터 미리 보기의 보고서 대시보드에는 Office 365에서 사용 작업이 표시 됩니다. Office 365 전역 관리자 또는 Exchange online, SharePoint online 또는 비즈니스용 Skype 관리자는 해당 서비스의 사용에 대 한 세부적인 통찰력을 얻을 수 있습니다. 보고서는 특정 office 365 서비스를 소비 하는 사용자 수, Office Professional Plus가 정품 인증 된 사용자 수 및 조직 전체에 전송 되는 메일의 양을 비롯 하 여 정보를 제공 합니다. 보고서는 최근 7, 30, 90 및 180 일 동안 사용할 수 있습니다.

다음과 같은 보고서를 사용할 수 있습니다.
- [전자 메일 활동 보고서](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office 정품 인증 보고서](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Online 사이트 사용 현황 보고서](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [비즈니스용 OneDrive 사용 현황 보고서](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Yammer 활동 보고서](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [비즈니스용 Skype 활동 보고서](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [비즈니스용 Skype 피어-투-피어 활동 보고서](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [비즈니스용 Skype 전화 회의 구성 보고서](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [비즈니스용 Skype 전화 회의 참가자 활동 보고서](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

자세한 내용은 [Microsoft 365 관리 센터의 활동 보고서](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263)를 참조 하세요.


## <a name="azure-active-directory-reports"></a>Azure Active Directory 보고서
Office 365에서는 인증 및 id 관리를 위해 Azure AD를 사용 합니다. Office 365 관리자는 Azure에서 생성 된 보고서를 사용 하 여 비정상적인 작업 및 해당 데이터에 대 한 무단 액세스를 확인할 수 있습니다. Azure AD의 액세스 및 사용 현황 보고서를 사용 하 여 조직의 디렉터리 무결성 및 보안을 확인할 수 있습니다. 이 정보를 사용 하 여 관리자는 가능한 보안 위험이 있을 수 있는 위치를 보다 잘 파악 하 여 이러한 위험을 완화 하도록 계획할 수 있습니다.

Azure AD 보고서를 Microsoft Excel로 내보내고, 감사 로그 검색 결과와 같은 Office 365의 다른 데이터와 상호 연결 하 여 액세스, 인증 및 응용 프로그램 수준 작업에 대 한 통찰력을 제공 합니다. Azure AD Premium을 사용 하는 경우 고급 변칙 및 리소스 사용 현황 보고서를 사용할 수 있습니다. 이러한 고급 보고서는 조직의 보안 환경을 개선 하 고 조직에서 장치 액세스 및 응용 프로그램 사용에 대 한 분석을 활용 하 여 잠재적 위협에 대처 하도록 도와줍니다. 자세한 내용은 [Azure Active Directory 보고](https://docs.microsoft.com/azure/active-directory/reports-monitoring/overview-reports/)를 참조 하세요.

## <a name="exchange-online-audit-reports"></a>Exchange Online 감사 보고서
exchange online 감사 보고서에는 사서함 액세스에 대 한 세부 정보와 관리자가 조직의 Exchange online 테 넌 트에 대 한 변경 내용이 포함 됩니다. 사서함 감사를 사용 하도록 설정한 후에는 다음 표의 작업을 사용 하 여 보고서를 실행 하 고 Exchange Online 감사 로그를 내보낼 수 있습니다.

>**참고**: 감사 된 이벤트가 해당 사서함에 대 한 감사 로그에 저장 되도록 각 사서함에 대해 사서함 감사 로깅을 사용 하도록 설정 해야 합니다. 사서함에 대해 사서함 감사 로깅을 사용 하도록 설정 되지 않은 경우 해당 사서함에 대 한 이벤트는 감사 로그에 저장 되지 않으며 사서함 감사 보고서에 나타나지 않습니다. 자세한 내용은 [사서함 감사 사용](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918)을 참조 하십시오.

| 작업 | 설명 |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [비 소유자 사서함 액세스 보고서 실행](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | 사서함의 소유자가 아닌 다른 사용자가 액세스 한 사서함 목록을 표시 합니다. 이 보고서에는 사서함에 액세스 한 사람, 사서함에서 수행한 작업 및 작업이 성공 했는지 여부에 대 한 정보가 포함 됩니다. |
| [사서함 감사 로그 내보내기](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | 사서함 감사 로그에는 사서함 소유자가 아닌 다른 사용자가 수행한 사서함의 액세스 및 작업에 대 한 정보가 포함 됩니다. 관리자는 날짜 범위와 함께 사서함을 지정 하 여 보고서를 생성할 수 있습니다. 로그는 메시지에 첨부 되 고 관리자가 결정 한 특정 사용자에 게 전송 되는 XML로 내보내집니다. |
| [관리자 역할 그룹 보고서 실행](https://docs.microsoft.com/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | 관리자 역할 그룹은 사용자에 게 관리 권한을 할당 하는 데 사용 됩니다. 이러한 권한을 통해 사용자는 암호 다시 설정, 사서함 만들기 또는 수정, 다른 사용자에 게 관리자 권한 할당 등의 관리 작업을 수행할 수 있습니다. 관리자 역할 그룹 보고서에는 구성원 추가 또는 제거를 비롯 하 여 역할 그룹에 대 한 변경 내용이 표시 됩니다. |
| [관리자 감사 로그 보기](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | 관리 감사 로그 보고서에는 Exchange Online의 관리자가 수행한 모든 만들기, 업데이트 및 삭제 기능이 나열 됩니다. 로그 항목은 실행 된 cmdlet, 사용 된 매개 변수, cmdlet을 실행 한 사용자 및 영향을 받은 개체에 대 한 정보를 제공 합니다. |
| [사서함 콘텐츠 검색 및 유지](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | 사서함의 원본 위치 eDiscovery 또는 원본 위치 유지 설정에 대 한 자세한 정보를 제공 합니다. |
| [관리자 감사 로그 내보내기](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | 관리자 감사 로그에는 Exchange Online의 만들기, 업데이트, 삭제 등의 특정 관리 작업이 기록 됩니다. 로그의 결과가 XML로 내보내지고 관리자가이 로그를 사용자 집합에 보내도록 선택할 수 있습니다. |
| [사서함 단위 소송 보존 보고서 실행](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | 사서함에 대 한 소송 보존 설정의 변경 사항에 대해 설명 합니다. |
| [외부 관리자 감사 로그 보기 및 내보내기](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | 외부 관리자가 수행한 작업에 대 한 세부 정보를 포함 합니다. 이 항목은 실행 된 cmdlet, 사용 된 매개 변수, Exchange Online에서 개체를 생성, 수정 또는 삭제 하는 모든 작업에 대 한 정보를 제공 합니다. |

## <a name="device-compliance-reports"></a>장치 준수 보고서
office 365 모바일 장치 관리 (MDM)를 사용 하 여 office 365 조직에 연결 되어 있을 때 모바일 장치를 관리 하 고 보호할 수 있습니다. 회사 전자 메일, 일정, 연락처 및 문서에 액세스 하는 데 사용 되는 스마트폰 및 태블릿과 같은 모바일 장치는 직원이 언제 어디서 나 작업을 수행할 수 있도록 하 고 어디에서 든 지 하 고 있어야 합니다. 따라서 조직의 정보를 보호 하는 것이 중요 합니다. Office 365 MDM을 사용 하 여 장치 보안 정책 및 액세스 규칙을 설정 하 고, 분실 하거나 도난당 한 모바일 장치를 지울 수 있습니다.

MDM 준수 보고서는 Office 365 데이터에 액세스 하는 모바일 장치를 보호 하기 위해 조직에서 설정한 정책에 대 한 개요를 제공 합니다. 이 보고서를 통해 준수 상태, 보고 된 위반, 차단 된 장치 및 보안 정책의 결과로 초기화 되는 장치 수를 기준으로 디바이스를 필터링 할 수 있습니다. 자세한 내용은 [Overview for Office 365의 모바일 장치 관리 개요](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)를 참조 하세요.

## <a name="data-loss-prevention"></a>데이터 손실 방지
DLP 정책은 조직의 정보 보안 및 흐름을 관리 하는 데 도움이 됩니다. 응용 프로그램 DLP 정책 팁을 사용 하 여 콘텐츠에 대 한 액세스를 차단 하거나, 데이터를 암호화 하거나, 정책 및 정책 위반을 사용자에 게 알리기 위해 정책을 설정할 수 있습니다. DLP 보고서는 정책 및 규칙 일치, 재정의 및 가양성의 수에 대 한 통찰력을 제공 합니다.

Microsoft 365 관리 센터를 사용 하 여 그래픽 차트나 테이블 형식으로 DLP 정책에 의해 검색 된 메시지 수에 대 한 정보를 볼 수 있습니다. 특히, 전송 및 수신 메일에 대 한 dlp 정책은 일치 하며, 송신 및 받은 메일에 대 한 dlp 규칙 일치 항목에 해당 합니다. 또한 Exchange 관리 센터를 사용 하 여 지난 24 시간 내 각 정책에 대 한 일치, 재정의 및 가양성의 수를 확인할 수 있습니다. 그러나 이 데이터는 차트로는 제공되지 않습니다. Excel에서 사용할 보고서를 다운로드 하는 경우 메시지를 보낸 사람, 요일 및 트리거된 정책 일치 항목 등 보다 자세한 정보를 볼 수 있습니다. 자세한 내용은 [DLP 정책 검색에 대 한 보고서 보기](https://technet.microsoft.com/en-us/library/jj889415(v=exchg.150).aspx)를 참조 하세요.

## <a name="auditing-in-yammer-enterprise"></a>Yammer Enterprise에서의 감사
yammer Enterprise는 관리자에 게 yammer [데이터 내보내기 API](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)를 통해 yammer 네트워크에서 사용자 활동 데이터를 내보내거나 yammer network administration page를 통해 수동으로 내보낼 수 있는 기능을 제공 합니다. 로그를 내보내는 기능은 Yammer의 네트워크 관리자만 사용할 수 있습니다. (모든 Office 365 전역 관리자는 Yammer 네트워크 관리자입니다.)

다음 데이터를 내보낼 수 있습니다.

| 파일 이름 | 설명 |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | 네트워크의 모든 신규, 보류 중 및 일시 중단 된 사용자 |
| Messages.csv | 네트워크의 모든 메시지 |
| 파일 .csv (메타 데이터) | 파일 이름, 파일 API URL, 업 로더 ID, 업로드 위치 등의 메타 데이터 |
| 파일 .csv (원본 파일) | 사용자가 Yammer에 업로드 한 원본 파일의 Zip 파일 |
| Topics.csv | 네트워크에 만들어지는 항목 |
| Pages.csv | 네트워크에서 사용자가 만든 페이지 (메모) |
| Admins.csv | 네트워크의 모든 확인 된 관리자 |
| Networks.csv | 모든 Yammer 외부 네트워크 |

*표 3-고객이 내보낼 수 있는 Yammer 네트워크 데이터 파일*

Yammer Enterprise 데이터는 Office 365 활동 보고서를 통해서도 사용할 수 있습니다. 또한 Yammer는 Office 365 관리 활동 API를 통해 추가 로깅을 제공 하 고 Power BI를 사용 하 여 데이터에 대 한 이유를 제공 합니다. 이러한 기능에 대 한 자세한 내용은 [Office 로드맵](https://fasttrack.microsoft.com/roadmap?filters=yammer) 를 참조 하세요.
