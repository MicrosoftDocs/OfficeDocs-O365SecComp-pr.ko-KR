---
title: 격리된 SharePoint Online 팀 사이트 배포
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/14/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 3033614b-e23b-4f68-9701-f62525eafaab
description: '요약: 다음 단계별 지침을 사용 하 여 격리 된 SharePoint Online 팀 사이트를 새로 배포 합니다.'
ms.openlocfilehash: e59c92ff488f82f4ea042364d742f7418da50167
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000190"
---
# <a name="deploy-an-isolated-sharepoint-online-team-site"></a>격리된 SharePoint Online 팀 사이트 배포

 **요약:** 다음 단계별 지침을 사용 하 여 격리 된 SharePoint Online 팀 사이트를 새로 배포 합니다.
  
이 문서는 Microsoft Office 365에서 격리 된 SharePoint Online 팀 사이트를 만들고 구성 하기 위한 단계별 배포 가이드입니다. 이러한 단계에서는 각 액세스 수준에 대해 단일 Azure Active Directory (AD) 기반 액세스 그룹을 사용 하 여 세 가지 기본 SharePoint 그룹 및 해당 사용 권한 수준을 사용할 것으로 가정 합니다.
  
## <a name="phase-1-create-and-populate-the-team-site-access-groups"></a>1 단계: 팀 사이트 액세스 그룹 만들기 및 채우기

이 단계에서는 세 가지 기본 SharePoint 그룹에 대 한 세 개의 Azure AD 기반 액세스 그룹을 만들고 적절 한 사용자 계정으로 채웁니다.
  
> [!NOTE]
> 다음 단계에서는 필요한 모든 사용자 계정이 이미 있고 해당 라이선스가 할당 된 것으로 가정 합니다. 그렇지 않은 경우 1 단계를 진행 하기 전에 추가 하 고 라이선스를 할당 하세요. 
  
### <a name="step-1-list-the-sharepoint-online-admins-for-the-site"></a>1 단계: 사이트에 대 한 SharePoint Online 관리자 나열

격리 된 팀 사이트에 대 한 SharePoint Online 관리자에 해당 하는 사용자 계정 집합을 확인 합니다.
  
Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 Windows PowerShell을 사용 하려면 upn (사용자 계정 이름) 목록 (예: belindan@contoso.com)을 만듭니다.
  
### <a name="step-2-list-the-members-for-the-site"></a>2 단계: 사이트 구성원 나열

사이트 내에 저장 된 리소스에 대해 공동으로 작업할 격리 된 팀 사이트의 구성원에 해당 하는 사용자 계정 집합을 확인 합니다.
  
Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 PowerShell을 사용 하려면 upn 목록을 만듭니다. 사이트 구성원이 많은 경우에는 upn 목록을 텍스트 파일에 저장 하 고 모두 단일 PowerShell 명령을 사용 하 여 추가할 수 있습니다.
  
### <a name="step-3-list-the-viewers-for-the-site"></a>3 단계: 사이트에 대 한 보는 사람 나열

격리 된 팀 사이트의 보는 사람에 해당 하는 사용자 계정 집합 (사이트에 저장 된 리소스를 볼 수는 있지만 수정 하거나 콘텐츠를 직접 공동으로 작업 하지는 않는 경우)을 결정 합니다.
  
Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 PowerShell을 사용 하려면 upn 목록을 만듭니다. 사이트 구성원이 많은 경우에는 upn 목록을 텍스트 파일에 저장 하 고 모두 단일 PowerShell 명령을 사용 하 여 추가할 수 있습니다.
  
사이트 보기에는 임원 관리, 법률 자문 위원 또는 부서별 부서 간 이해 관계자가 포함 될 수 있습니다.
  
### <a name="step-4-create-the-three-access-groups-for-the-site-in-azure-ad"></a>4 단계: Azure AD에서 사이트에 대 한 세 개의 액세스 그룹 만들기

Azure AD에서 다음 액세스 그룹을 만들어야 합니다.
  
- 사이트 관리자 (1 단계에서 목록이 포함 됨)
    
- 사이트 구성원 (2 단계에서 목록이 포함 됨)
    
- 사이트 뷰어 (3 단계의 목록이 포함 됨)
    
1. 브라우저에서 Azure 포털로 이동한 [https://portal.azure.com](https://portal.azure.com) 후 사용자 관리 관리자 또는 회사 관리자 역할로 할당 된 계정의 자격 증명을 사용 하 여 로그인 합니다.
    
2. Azure Portal에서 **Azure Active Directory > 그룹**을 차례로 클릭합니다.
    
3. **그룹 - 모든 그룹** 블레이드에서 **+ 새 그룹**을 클릭합니다.
    
4. **그룹** 블레이드에서:
    
  - **그룹 유형**에서 **Office 365**를 선택합니다.
    
  - **이름**에 그룹 이름을 입력 합니다.
    
  - 그룹 **설명**에 그룹에 대 한 설명을 입력 합니다.
    
  - **멤버 유형**에서 **할당됨**을 선택합니다.
    
5. **만들기**를 클릭한 다음 **그룹** 블레이드를 닫습니다.
    
6. 추가 그룹에 대해 3-5 단계를 반복 합니다.
    
> [!NOTE]
> Office 기능을 사용 하도록 설정 하려면 Azure portal을 사용 하 여 그룹을 만들어야 합니다. SharePoint Online 격리 사이트가 나중에 Azure Information Protection (aip) 레이블을 사용 하 여 파일을 암호화 하 고 특정 그룹에 사용 권한을 할당 하는 고도로 기밀 사이트로 구성 된 경우에는 허용 되는 그룹이 Office 기능을 사용 하 여 만들어진 것 이어야 합니다. 된. Azure AD 그룹을 만든 후에는 Office 기능 설정을 변경할 수 없습니다. 
  
다음은 세 개의 사이트 액세스 그룹이 포함 된 결과 구성입니다.
  
![격리 된 SharePoint Online 사이트 배포에 대 한 세 가지 액세스 그룹](media/c2557f61-478b-4494-95e9-d79fe5909e8b.png)
  
### <a name="step-5-add-the-user-accounts-to-the-access-groups"></a>5단계. 액세스 그룹에 사용자 계정 추가

이 단계에서는 다음을 수행 합니다.
  
1. 1 단계의 사용자 목록을 site admins 액세스 그룹에 추가 합니다.
    
2. 2 단계의 사용자 목록을 사이트 구성원 액세스 그룹에 추가
    
3. 3 단계의 사용자 목록을 사이트 뷰어 액세스 그룹에 추가 합니다.
    
Windows server ad를 통해 사용자 계정 및 그룹을 관리 하는 경우에는 일반 Windows server ad 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 액세스 그룹에 사용자를 추가 하 고 Office 365 구독과의 동기화를 기다립니다.
  
office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 office 관리 센터 또는 PowerShell을 사용할 수 있습니다. 액세스 그룹의 그룹 이름이 중복 된 경우 Office 관리 센터를 사용 해야 합니다.
  
Office 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 적절 한 액세스 그룹에 적절 한 사용자 계정 및 그룹을 추가 합니다.
  
PowerShell의 경우 먼저 [Azure Active Directory V2 PowerShell 모듈을 사용 하 여 연결](https://go.microsoft.com/fwlink/?linkid=842218)합니다.
  
다음으로, 다음 명령 블록을 사용 하 여 액세스 그룹에 개별 사용자 계정을 추가 합니다.
  
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> 모든 powershell 명령 및 그룹 및 사용자 계정 이름에 따라 powershell 명령을 생성 하는 Excel 구성 워크시트가 포함 된 텍스트 파일의 경우 [격리 된 SharePoint Online 팀 사이트 배포 키트](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907)를 다운로드 합니다. 
  
텍스트 파일의 액세스 그룹에 대 한 사용자 계정의 upn을 저장 한 경우 다음 PowerShell 명령 블록을 사용 하 여 모든 항목을 한 번에 추가할 수 있습니다.
  
```
$grpName="<display name of the access group>"
$fileName="<path and name of the file containing the list of account UPNs>"
$grpID=(Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
Get-Content $fileName | ForEach { $userUPN=$_; Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID $grpID }
```

PowerShell의 경우 다음 명령 블록을 사용 하 여 액세스 그룹에 개별 그룹을 추가 합니다.
  
```
$nestedGrpName="<display name of the group to add to the access group>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $nestedGrpName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID

```

결과는 다음과 같아야 합니다.
  
- site admins Azure AD 그룹에는 사이트 관리자 사용자 계정 또는 그룹이 포함 되어 있습니다.
    
- 사이트 구성원 Azure AD 그룹에는 사이트 구성원 사용자 계정 또는 그룹이 포함 됩니다.
    
- 사이트 뷰어 Azure AD 그룹에는 사이트 콘텐츠만 볼 수 있는 사용자 계정 또는 그룹이 포함 됩니다.
    
Office 관리 센터를 사용 하거나 다음 PowerShell 명령 블록을 사용 하 여 각 액세스 그룹의 그룹 구성원 목록을 확인 합니다.
  
```
$grpName="<display name of the access group>"
Get-AzureADGroupMember -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID | Sort UserPrincipalName | Select UserPrincipalName,DisplayName,UserType
```

다음은 사용자 계정이 나 그룹으로 채워진 3 개의 사이트 액세스 그룹이 포함 된 결과 구성입니다.
  
![세 개의 액세스 그룹은 사용자 계정으로 채워집니다.](media/2320107c-dad6-4c8f-94e5-f6427c125e71.png)
  
## <a name="phase-2-create-and-configure-the-isolated-team-site"></a>2 단계: 격리 된 팀 사이트 만들기 및 구성

이 단계에서는 격리 된 sharepoint online 사이트를 만들고 기본 sharepoint online 권한 수준에 대 한 사용 권한을 구성 하 여 새 Azure AD 기반 액세스 그룹을 사용 합니다.
  
먼저 다음 단계를 사용 하 여 SharePoint Online 팀 사이트를 만듭니다.
  
1. sharepoint online 팀 사이트 (sharepoint online 관리자)를 관리 하는 데 사용 되는 계정을 사용 하 여 관리 센터에 로그인 합니다. 도움을 받으려면 [Office 365에 로그인하는 위치](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4)를 참조하세요.
    
2. 타일 목록에서 **SharePoint**를 클릭합니다.
    
3. 브라우저의 새 **SharePoint 탭**에서 + **사이트 만들기**를 클릭합니다.
    
4. **사이트 만들기** 페이지에서 **팀 사이트**를 클릭합니다.
    
5. **사이트 이름**에 팀 사이트의 이름을 입력 합니다. 
    
6. **팀 사이트 설명** 에서 사이트의 용도에 대 한 설명을 입력 합니다 (선택 사항).
    
7. **개인 정보 설정**에서 **비공개 – 구성원만 이 사이트에 액세스할 수 있습니다.** 를 선택하고 **다음**을 클릭합니다.
    
8. **어떤 사람을 추가하시겠습니까?** 창에서 **마침**을 클릭합니다.
    
다음으로, 새 SharePoint Online 팀 사이트에서 사용 권한을 구성 합니다.
  
1. 도구 모음에서 설정 아이콘을 클릭한 다음, **사이트 권한**을 클릭합니다.
    
2. **사이트 권한** 창에서 **고급 권한 설정**을 클릭합니다.
    
3. 브라우저의 새 **권한** 탭에서 **액세스 요청 설정**을 클릭합니다.
    
4. **액세스 요청 설정** 대화 상자에서 **구성원이 사이트 및 개별 파일 및 폴더를 공유 하도록 허용** 을 선택 취소 하 고 세 확인란이 모두 선택 취소 되도록 **액세스 요청을 허용한** 다음 **확인**을 클릭 합니다.
    
5. 브라우저의 **사용 권한** 탭에 있는 목록에서 ** \<사이트 name> 구성원** 을 클릭 합니다.
    
6. **사용자 및 그룹**에서 **새로 만들기**를 클릭합니다.
    
7. **공유** 대화 상자에서 사이트 구성원 액세스 그룹의 이름을 입력 하 고,이를 선택한 다음, **공유**를 클릭 합니다.
    
8. 브라우저에서 뒤로 단추를 클릭합니다.
    
9. 목록에서 ** \<사이트 name> 소유자** 를 클릭 합니다.
    
10. **사용자 및 그룹**에서 **새로 만들기**를 클릭합니다.
    
11. **공유** 대화 상자에서 site admins 액세스 그룹의 이름을 입력 하 고,이를 선택한 다음, **공유**를 클릭 합니다.
    
12. 브라우저에서 뒤로 단추를 클릭합니다.
    
13. 목록에서 ** \<사이트 name> 방문자** 를 클릭 합니다.
    
14. **사용자 및 그룹**에서 **새로 만들기**를 클릭합니다.
    
15. **공유** 대화 상자에서 사이트 뷰어 액세스 그룹의 이름을 입력 하 고,이를 선택한 다음, **공유**를 클릭 합니다.
    
16. 브라우저의 **권한** 탭을 닫습니다.
    
이러한 권한 설정의 결과는 다음과 같습니다.
  
- site name> owner SharePoint 그룹에는 모든 구성원이 모든 권한 수준을 갖는 사이트 관리자 액세스 그룹이 포함 되어 있습니다 **** . ** \<**
    
- site name> Members SharePoint 그룹에는 모든 구성원이 **편집** 권한 수준을 갖는 사이트 구성원 액세스 그룹이 포함 되어 있습니다. ** \<**
    
- site name> 방문자 SharePoint 그룹에는 모든 구성원이 **읽기** 권한 수준을 갖는 사이트 뷰어 액세스 그룹이 포함 되어 있습니다. ** \<**
    
- 구성원이 다른 구성원을 초대 하거나 구성원이 아닌 사람에 게 액세스를 요청 하는 기능은 사용 하지 않도록 설정 됩니다.
    
다음은 사용자 계정 또는 Azure AD 그룹으로 채워지는 세 개의 액세스 그룹을 사용 하도록 구성 된 사이트에 대 한 세 가지 SharePoint 그룹의 구성 결과입니다.
  
![액세스 그룹과 사용자 계정을 사용 하는 격리 된 SharePoint Online 사이트의 최종 구성](media/e7618971-06ab-447b-90ff-d8be3790fe63.png)
  
액세스 그룹 중 하나의 그룹 구성원 자격을 통해 사이트의 구성원은 이제 사이트의 리소스를 사용 하 여 공동 작업을 수행할 수 있습니다.
  
## <a name="next-step"></a>다음 단계

사이트 액세스 그룹 구성원 자격을 변경 하거나 사용자 지정 사용 권한이 있는 문서 폴더를 만들려면 [격리 된 SharePoint Online 팀 사이트 관리](manage-an-isolated-sharepoint-online-team-site.md)를 참조 하세요.
  
## <a name="see-also"></a>참고 항목

[격리된 SharePoint Online 팀 사이트](isolated-sharepoint-online-team-sites.md)
  
[격리된 SharePoint Online 팀 사이트 디자인](design-an-isolated-sharepoint-online-team-site.md)
  
[격리된 SharePoint Online 팀 사이트 관리](manage-an-isolated-sharepoint-online-team-site.md)
  



