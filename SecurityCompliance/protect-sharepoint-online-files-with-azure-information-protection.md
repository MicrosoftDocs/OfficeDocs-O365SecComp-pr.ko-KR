---
title: Azure Information Protection을 사용한 SharePoint Online 파일 보호
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/29/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 5b9c8e41-25d2-436d-89bb-9aecb9ec2b80
description: '요약: Azure Information Protection을 적용하여 극비 SharePoint Online 팀 사이트의 파일을 보호합니다.'
ms.openlocfilehash: 4be30059192bb954a1c2d07d34ece76bb339d7dc
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265850"
---
# <a name="protect-sharepoint-online-files-with-azure-information-protection"></a>Azure Information Protection을 사용한 SharePoint Online 파일 보호

 **요약:** Azure Information Protection을 적용하여 극비 SharePoint Online 팀 사이트의 파일을 보호합니다.
  
이 문서의 단계를 사용하여 파일에 대해 암호화 및 사용 권한을 제공하도록 Azure Information Protection을 구성합니다. 이러한 파일은 극비 보호용으로 구성된 SharePoint 라이브러리에 추가되거나, 사이트에서 직접 파일을 열고 Azure Information Protection 클라이언트를 사용하여 암호화를 추가할 수 있습니다. 암호화 및 사용 권한 보호 기능은 사이트에서 다운로드된 파일에 적용됩니다. 

다음 단계는 이러한 사이트 내에서 SharePoint 사이트 및 파일에 대해 극비 보호를 구성하기 위한 보다 큰 솔루션의 일부입니다. 자세한 내용은 [SharePoint Online 사이트 및 파일 보호](secure-sharepoint-online-sites-and-files.md)를 참조하세요. 

SharePoint Online의 파일에 대해 Azure Information Protection을 사용하는 것이 모든 고객에게 권장되는 것은 아니지만 일부 파일에 대해 이러한 수준의 보호가 필요한 고객에게는 적절할 수 있습니다.

이 솔루션에 대한 몇 가지 중요 참고 사항은 다음과 같습니다.
- Office 365에 저장된 파일에 Azure Information Protection 암호화가 적용되어 있으면 이 파일의 내용을 처리할 수 없습니다. 즉 공동 작성, eDiscovery, 검색, Delve 및 기타 공동 작업 기능이 작동하지 않습니다. DLP(데이터 손실 방지) 정책은 메타데이터(Office 365 레이블 포함)에만 작동할 수 있지만 파일의 내용(예: 파일 내의 신용 카드 번호)에는 작동할 수 없습니다.

- 이 솔루션을 사용하려면 Azure Information Protection의 보호를 적용하는 레이블을 선택해야 합니다. 파일을 인덱싱하고 조사하기 위해 SharePoint 기능 및 자동 암호화가 필요한 경우 SharePoint Online의 IRM(정보 권한 관리)을 사용하는 것이 좋습니다. IRM에 대해 SharePoint 라이브러리를 구성하면 편집을 위해 파일을 다운로드할 때 파일이 자동으로 암호화됩니다. SharePoint IRM에는 의사 결정에 영향을 줄 수 있는 제한 사항이 포함되어 있습니다. 자세한 내용은 [SharePoint 관리 센터에서 의 IRM(정보 권한 관리) 설정](https://support.office.com/article/Set-up-Information-Rights-Management-IRM-in-SharePoint-admin-center-239CE6EB-4E81-42DB-BF86-A01362FED65C)을 참조하세요.

## <a name="admin-setup"></a>관리자 설정
먼저 [Office 365 구독을 위해 Microsoft Office 365 관리 센터에서 Azure RMS 활성화](https://docs.microsoft.com/information-protection/deploy-use/activate-office365)의 지침을 사용합니다.
  
그런 다음, 극비 SharePoint Online 팀 사이트에 대한 보호 및 권한을 위한 새로운 범위 지정 정책 및 하위 레이블로 Azure Information Protection을 구성합니다.
  
1. 보안 관리자 또는 회사 관리자 역할이 있는 계정으로 로그인합니다. 도움을 받으려면 [Office 365에 로그인하는 위치](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4)를 참조하세요.
    
2. 브라우저의 별도 탭에서 Azure Portal([https://portal.azure.com](https://portal.azure.com))로 이동합니다.
    
3. 처음으로 Azure Information Protection을 구성하는 경우 다음 [지침](https://docs.microsoft.com/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time)을 참조하세요.

4. 목록 창에서 **모든 서비스**를 클릭하고 **정보**를 입력한 다음, **Azure Information Protection**을 클릭합니다.

5. **레이블**을 클릭합니다.
    
6. **기밀** 레이블을 마우스 오른쪽 단추로 클릭하고 **하위 레이블 추가**를 클릭합니다.
    
7. **이름**에 하위 레이블의 이름을 입력하고 **설명**에 레이블에 대한 설명을 입력합니다.
    
8. **이 레이블을 포함하는 문서 및 전자 메일에 대한 권한 설정**에서 **보호**를 클릭합니다.
    
9. **보호** 섹션에서 **Azure(클라우드 키)** 를 클릭합니다.
    
10. **보호** 블레이드의 **보호 설정** 아래에서 **권한 추가**를 클릭합니다.
    
11. **권한 추가** 블레이드의 **사용자 및 그룹 지정** 아래에서 **디렉터리 찾아보기**를 클릭합니다.
    
12. **AAD 사용자 및 그룹** 창에서 극비 SharePoint Online 팀 사이트에 대한 사이트 멤버 액세스 그룹을 선택하고 **선택**을 클릭합니다.
    
13. **미리 설정된 또는 설정된 사용자 지정에서 권한 선택**에서 **사용자 지정**을 클릭한 다음 **권한 보기**, **콘텐츠 편집**, **저장**, **회신** 및 **모두 회신** 확인란을 차례로 클릭합니다.
    
14. **확인**를 두 번 차례로 클릭합니다.
    
15. **하위 레이블** 블레이드에서 **저장**을 클릭하고 **확인**을 클릭합니다.

16. **Azure Information Protection** 블레이드에서 **정책 > + 새 정책 추가**를 클릭합니다.
    
17. **정책 이름**에 새 정책의 이름을 입력하고 **설명**에 설명을 입력합니다.
    
18. **이 정책을 가져올 사용자 또는 그룹을 선택합니다 > 사용자/그룹**을 클릭한 후 극비 SharePoint Online 팀 사이트에 대한 사이트 멤버 액세스 그룹을 선택합니다.
    
19. **선택 > 확인**을 클릭합니다.

20. **레이블 추가 또는 제거**를 클릭합니다. **정책: 레이블 추가 또는 제거** 창에서 새 하위 레이블의 이름을 클릭하고 **확인**을 클릭합니다.   

21. **저장**을 클릭한 다음 **확인**을 클릭합니다.
 
## <a name="client-setup"></a>클라이언트 설치
이제 문서를 작성하고 Azure Information Protection 및 새로운 레이블을 사용하여 해당 문서를 보호할 준비가 완료되었습니다.
  
사용자의 장치 또는 Windows 기반 컴퓨터 [Azure Information Protection 클라이언트](https://docs.microsoft.com/information-protection/rms-client/install-client-app)를 설치해야 합니다. 스크립트를 작성하여 설치를 자동화하거나 사용자가 클라이언트를 수동으로 설치할 수 있습니다. 다음 리소스를 참조하세요.
  
- [Azure Information Protection의 클라이언트 측면](https://docs.microsoft.com/information-protection/rms-client/use-client)
    
- [Azure Information Protection 클라이언트 설치](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide)
    
- [수동 설치를 위한 다운로드 페이지](https://www.microsoft.com/download/details.aspx?id=53018)
    
설치된 후 사용자가 Office 365 계정을 가진 Office 응용 프로그램(Microsoft Word )에서 실행한 다음 로그인할 수 있습니다. 새 **Information Protection** 표시줄에서 새 레이블이 선택할 수 있습니다. 극비 파일을 보호하려면 SharePoint Online 팀 사이트와 사용할 레이블을 알아야 합니다.
  
> [!NOTE]
> 극비 SharePoint Online 팀 사이트가 여러 개인 경우, 각 하위 레이블에 대한 권한을 특정 SharePoint Online 팀 사이트의 사이트 멤버 액세스 그룹으로 설정하고 위의 설정을 사용하여 하위 레이블이 포함된 Azure Information Protection 범위 지정 정책 여러 개를 만들어야 합니다. 
  
## <a name="adding-permissions-for-external-users"></a>외부 사용자에 대한 권한 추가
Azure Information Protection으로 보호된 파일에 대한 액세스 권한을 외부 사용자에게 부여할 수 있는 두 가지 방법이 있습니다. 이 두 가지 방법에서는 모두 Azure AD 계정이 외부 사용자에게 있어야 합니다. 외부 사용자가 Azure AD를 사용하는 조직의 구성원이 아닌 경우 [https://aka.ms/aip-signup](https://aka.ms/aip-signup) 등록 페이지를 사용하여 Azure AD 계정을 개별로 가져올 수 있습니다.

 - 레이블 보호를 구성하는 데 사용되는 외부 사용자를 Azure AD 그룹에 추가 먼저 디렉터리에 계정을 B2B 사용자로 추가해야 합니다. [Azure Rights Management에서 그룹 구성원 자격을 캐시](https://docs.microsoft.com/azure/information-protection/plan-design/prepare#group-membership-caching-by-azure-information-protection)하는 데 몇 시간이 걸릴 수 있습니다.  
 - 레이블 보호에 외부 사용자를 직접 추가합니다. 조직(예: Fabrikam.com), Azure AD 그룹(조직 내의 재무 그룹) 또는 사용자의 모든 사용자를 추가할 수 있습니다. 예를 들어 조절기의 외부 팀을 레이블 보호에 추가할 수 있습니다.

## <a name="see-also"></a>참고 항목

[SharePoint Online 사이트 및 파일 보호](secure-sharepoint-online-sites-and-files.md)
  
[정치적 캠페인, 비영리 조직 및 기타 기밀 조직을 위한 Microsoft 보안 지침](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[클라우드 도입 및 하이브리드 솔루션](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
