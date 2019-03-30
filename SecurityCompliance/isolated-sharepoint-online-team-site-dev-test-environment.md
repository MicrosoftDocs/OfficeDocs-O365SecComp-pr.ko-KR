---
title: 격리된 SharePoint Online 팀 사이트 개발/테스트 환경
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: d1795031-beef-49ea-a6fc-5da5450d320d
description: '요약: Office 365 개발/테스트 환경에서 조직의 나머지 부분과 격리 된 SharePoint Online 팀 사이트를 구성 합니다.'
ms.openlocfilehash: 56c10b1a3871014f26a4d2fd98d9b4139d19ac47
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000231"
---
# <a name="isolated-sharepoint-online-team-site-devtest-environment"></a>격리된 SharePoint Online 팀 사이트 개발/테스트 환경

 **요약:** Office 365 개발/테스트 환경에서 조직의 나머지 부분과 격리 된 SharePoint Online 팀 사이트를 구성 합니다.
  
Office 365의 SharePoint Online 팀 사이트는 공통 문서 라이브러리, OneNote 전자 필기장 및 기타 서비스를 사용 하는 공동 작업을 위한 위치입니다. 대부분의 경우 부서나 조직 간에 폭넓은 액세스 및 공동 작업을 수행할 수 있습니다. 그러나 경우에 따라 소규모 사용자 그룹 간에 공동 작업 하는 데 필요한 액세스 및 사용 권한을 강력 하 게 제어 하려는 경우도 있습니다.
  
sharepoint Online 팀 사이트에 대 한 액세스 및 사용자가 수행할 수 있는 작업은 sharepoint 그룹 및 사용 권한 수준에 의해 제어 됩니다. 기본적으로 SharePoint Online 사이트에는 다음과 같은 세 가지 수준의 액세스 권한이 있습니다.
  
- **구성원**-사이트의 리소스를 보고, 만들고, 수정할 수 있습니다.
    
- **소유자**-사용 권한 변경 기능을 비롯 하 여 사이트에 대 한 모든 권한이 있습니다.
    
- **방문자**-사이트의 리소스만 볼 수 있습니다.
    
이 문서에서는 projectx 라는 기밀 조사 프로젝트에 대 한 격리 된 SharePoint Online 팀 사이트의 구성을 단계별로 안내 합니다. 액세스 요구 사항은 다음과 같습니다.
  
- 프로젝트의 구성원만 사이트 및 해당 콘텐츠 (문서, OneNote 전자 필기장, 페이지)에 액세스할 수 있으며, 그룹 구성원을 통해 제어 되는 SharePoint 사용 권한 수준이 편집 및 보기입니다.
    
- 사이트 작성자 및 사이트에 대 한 관리자 그룹의 구성원만 사이트 수준 사용 권한 수정을 포함 하는 사이트 관리를 수행할 수 있습니다.
    
Office 365 개발/테스트 환경에서 격리 된 SharePoint Online 팀 사이트를 설정 하는 세 가지 단계는 다음과 같습니다.
  
1. Office 365 개발/테스트 환경을 만듭니다.
    
2. projectx에 대 한 사용자 및 그룹을 만듭니다.
    
3. 새 projectx SharePoint Online 팀 사이트를 만들고 격리 합니다.
    
> [!TIP]
> [여기](http://aka.ms/catlgstack)를 클릭하여 One Microsoft 클라우드 테스트 랩 가이드 스택의 모든 문서에 대한 가상 맵을 확인할 수 있습니다.
  
## <a name="phase-1-build-out-your-lightweight-or-simulated-enterprise-office-365-devtest-environment"></a>1단계: 경량 또는 시뮬레이트된 엔터프라이즈 Office 365 개발/테스트 환경을 구축합니다.

최소 요구 사항과 함께 간단한 방식으로 격리 된 SharePoint Online 팀 사이트를 만들려는 경우에는 [Office 365 개발/테스트 환경의](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)2, 3 단계의 지침을 따릅니다.
  
시뮬레이트된 엔터프라이즈 구성에서 격리 된 SharePoint Online 팀 사이트를 만들려면 [Office 365 개발/테스트 환경용 DirSync](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment)의 지침을 따릅니다.
  
> [!NOTE]
> 격리 된 SharePoint Online 사이트를 만드는 경우에는 Windows Server AD 포리스트의 인터넷 및 디렉터리 동기화에 연결 된 시뮬레이트된 인트라넷을 포함 하는 시뮬레이트된 엔터프라이즈 개발/테스트 환경이 필요 하지 않습니다. 격리 된 SharePoint Online 사이트를 테스트 하 고 일반적인 조직을 나타내는 환경에서 테스트해 볼 수 있도록 여기에서 옵션으로 제공 됩니다. 
  
## <a name="phase-2-create-user-accounts-and-access-groups"></a>2 단계: 사용자 계정 및 액세스 그룹 만들기

[office 365 PowerShell에 연결](https://technet.microsoft.com/library/dn975125.aspx) 의 지침을 사용 하 여 다음 위치에서 전역 관리자 계정을 사용 하 여 office 365 트레일 구독에 연결 합니다.
  
- 사용하는 컴퓨터(경량 Office 365 개발/테스트 환경)
    
- CLIENT1 가상 컴퓨터(시뮬레이트된 엔터프라이즈 Office 365 개발/테스트 환경)
    
projectx SharePoint Online 팀 사이트에 대 한 새 액세스 그룹을 만들려면 windows PowerShell 프롬프트에 대 한 windows Azure Active Directory 모듈에서 다음 명령을 실행 합니다.
  
```
$groupName="ProjectX-Members"
$groupDesc="People allowed to collaborate for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Admins"
$groupDesc="People allowed to administer SharePoint for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Viewers"
$groupDesc="People allowed to view the SharePoint resources for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
```

> [!TIP]
> 이 문서의 PowerShell 명령을 모두 포함 하는 텍스트 파일을 보려면 [여기](https://gallery.technet.microsoft.com/PowerShell-commands-for-an-b2608df1) 를 클릭 하십시오.
  
조직 이름(예: contosotoycompany), 위치에 대한 2자리 국가 코드를 입력한 후 Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.
  
```
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$licAssignment= $orgName + ":ENTERPRISEPREMIUM"
$userName= "designer@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Designer" -FirstName Lead -LastName Designer -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

**get-msoluser** 명령을 표시 하 고 나면 잠재 고객 디자이너 계정에 대해 생성 된 암호를 확인 하 여 안전한 위치에 기록 합니다.
  
Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.
  
```
$userName= "researcher@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Researcher" -FirstName Lead -LastName Researcher -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

**get-msoluser** 명령을 표시할 때 잠재 고객 리서치 도구 계정에 대해 생성 된 암호를 확인 하 고 안전한 위치에 기록 합니다.
  
Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.
  
```
$userName= "devvp@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Development VP" -FirstName Development -LastName VP -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

**get-msoluser** 명령을 표시할 때 개발 VP 계정에 대해 생성 된 암호를 확인 하 고 안전한 위치에 기록 합니다.
  
다음으로 새 액세스 그룹에 새 계정을 추가 하려면 windows powershell 프롬프트에 대 한 windows Azure Active Directory 모듈에서 다음 PowerShell 명령을 실행 합니다.
  
```
$grpName="ProjectX-Members"
$userUPN="designer@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$userUPN="researcher@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Admins"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userCredential.UserName }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Viewers"
$userUPN="devvp@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
```

검색
  
- projectx 구성원 액세스 그룹에는 잠재 고객 디자이너 및 잠재 고객 리서치 도구 사용자 계정이 포함 됩니다.
    
- projectx-Admins 액세스 그룹에는 평가판 구독에 대 한 전역 관리자 계정이 포함 되어 있습니다.
    
- projectx-뷰어 액세스 그룹에는 개발 VP 사용자 계정이 포함 되어 있습니다.
    
그림 1에는 액세스 그룹 및 해당 구성원 자격이 나와 있습니다.
  
**그림 1**

![격리 된 SharePoint Online 그룹 사이트에 대 한 Office 365 그룹 및 해당 구성원 자격](media/5b7373b9-2a80-4880-afe5-63ffb17237e6.png)
  
## <a name="phase-3-create-a-new-projectx-sharepoint-online-team-site-and-isolate-it"></a>3 단계: 새 projectx SharePoint Online 팀 사이트를 만들고 격리 합니다.

projectx에 대 한 SharePoint Online 팀 사이트를 만들려면 다음을 수행 합니다.
  
1. 로컬 컴퓨터 (경량 구성) 또는 CLIENT1 (시뮬레이트된 엔터프라이즈 구성)에서 브라우저를 사용 하 여 전역 관리자 계정을 사용 하 여 Office 365 포털 ([https://admin.microsoft.com](https://admin.microsoft.com))에 로그인 합니다.
    
2. 타일 목록에서 **SharePoint**를 클릭합니다.
    
3. 브라우저의 새 SharePoint 탭에서 **+ 사이트 만들기**를 클릭합니다.
    
4. **팀 사이트 이름**에서 **projectx**를 입력 합니다. **개인 정보 설정**에서 **비공개-구성원만이 사이트에 액세스할 수 있습니다**.를 선택 합니다.
    
5. **팀 사이트 설명**에서 **projectx에 대 한 SharePoint 사이트**를 입력 하 고 **다음**을 클릭 합니다.
    
6. **누가 추가**하 시겠습니까? 창에서 **마침을**클릭 합니다.
    
7. 브라우저의 새 **projectx** 에 있는 도구 모음에서 설정 아이콘을 클릭 한 다음 **사이트 사용 권한을**클릭 합니다.
    
8. **사이트 권한** 창에서 **고급 권한 설정**을 클릭합니다.
    
9. 브라우저의 새 **사용 권한: 프로젝트 X** 탭에서 **액세스 요청 설정을**클릭 합니다.
    
10. **액세스 요청 설정** 대화 상자에서 **구성원이 사이트 및 개별 파일 및 폴더 공유를 허용** 하 고 **액세스 요청 허용** (3 개의 확인란이 모두 선택 취소 됨) 하 고 **확인**을 클릭 합니다.
    
11. 목록에서 **projectx Members** 를 클릭 합니다.
    
12. **사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.
    
13. **공유** 대화 상자에서 **projectx-Members**를 입력 하 고, 해당 구성원을 선택한 다음, **공유**를 클릭 합니다.
    
14. 브라우저에서 뒤로 단추를 클릭합니다.
    
15. 목록에서 **projectx 소유자** 를 클릭 합니다.
    
16. **사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.
    
17. **공유** 대화 상자에서 **projectx-Admins**를 입력 하 고, 해당 파일을 선택한 다음, **공유**를 클릭 합니다.
    
18. 브라우저에서 뒤로 단추를 클릭합니다.
    
19. 목록에서 **projectx 방문자** 를 클릭 합니다.
    
20. **사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.
    
21. **공유** 대화 상자에서 **projectx-뷰어**를 입력 하 고 선택 하 고 **공유**를 클릭 합니다.
    
22. 브라우저에서 **사용자 및 그룹** 탭을 닫고 브라우저에서 **projectx-Home** 탭을 클릭 한 다음, **사이트 권한** 창을 닫습니다.
    
권한 구성의 결과는 다음과 같습니다.
  
- projectx members SharePoint 그룹에는 projectx-Members 액세스 그룹 (잠재 고객 디자이너 및 잠재 고객 연구원 사용자 계정만 포함)과 projectx 그룹 (전역 관리자 사용자 계정만 포함)만 포함 됩니다.
    
- projectx 소유자 SharePoint 그룹에는 projectx-Admins 액세스 그룹 (전역 관리자 사용자 계정만 포함)만 포함 됩니다.
    
- projectx 방문자 SharePoint 그룹에는 projectx-뷰어 액세스 그룹 (개발 VP 사용자 계정만 포함)만 포함 됩니다.
    
- 구성원은 사이트 수준 권한을 수정할 수 없습니다 (이 작업은 projectx-Admins 그룹의 구성원만 수행할 수 있음).
    
- 다른 사용자 계정은 사이트 또는 해당 리소스에 액세스하거나 사이트에 대한 액세스를 요청할 수 없습니다.
    
그림 2는 SharePoint 그룹 및 해당 구성원 자격을 보여 줍니다.
  
**그림 2**

![sharepoint online 그룹 및 격리 된 sharepoint online 그룹 사이트에 대 한 구성원 자격](media/595abff4-64f9-49de-a37a-c70c6856936b.png)
  
이제 수석 디자이너 사용자 계정을 사용 하 여 액세스 방법을 살펴보겠습니다.
  
1. 브라우저에서 **projectx-home** 탭을 닫고 브라우저에서 **Microsoft Office Home** 탭을 클릭 합니다.
    
2. 전역 관리자의 이름을 클릭 하 고 **로그 아웃**을 클릭 합니다.
    
3. 잠재 고객 디자이너 계정 이름 및 암호를[https://admin.microsoft.com](https://admin.microsoft.com)사용 하 여 Office 365 portal ()에 로그인 합니다.
    
4. 타일 목록에서 **SharePoint**를 클릭합니다.
    
5. 브라우저의 새 **SharePoint** 탭에 있는 검색 상자에 **projectx** 를 입력 하 고 검색을 활성화 한 다음 **projectx** 팀 사이트를 클릭 합니다. projectx 팀 사이트에 대 한 브라우저에 새 탭이 표시 되어야 합니다.
    
6. 설정 아이콘을 클릭 합니다. **사이트 사용 권한에**대 한 옵션이 없는 것을 알 수 있습니다. projectxadmins 그룹의 구성원만이 사이트에 대 한 사용 권한을 수정할 수 있기 때문에 이것은 올바릅니다.
    
7. 메모장 또는 원하는 텍스트 편집기를 엽니다.
    
8. projectx 팀 사이트의 URL을 복사 하 여 메모장 이나 텍스트 편집기에서 새 줄에 붙여 넣습니다.
    
9. 브라우저의 새 **projectx-홈** 탭에서 **문서**를 클릭 합니다.
    
10. projectx documents 폴더의 URL을 복사 하 여 메모장 이나 텍스트 편집기에서 새 줄에 붙여 넣습니다.
    
11. 브라우저의 새 **projectx-문서** 탭에서 **새 > Word 문서**를 클릭 합니다.
    
12. **Word Online** 페이지에서 텍스트를 입력 하 고 상태를 **저장할**때까지 기다렸다가 브라우저에서 뒤로 단추를 클릭 한 다음 페이지를 새로 고칩니다. **문서** 폴더에 새 **문서 .docx** 가 표시 됩니다.
    
13. **문서 .docx** 문서의 줄임표를 클릭 한 다음 **링크 가져오기를**클릭 합니다.
    
14. **공유의 ' 문서 .docx '** 대화 상자에 URL을 복사 하 여 메모장 이나 텍스트 편집기에서 새 줄에 붙여 넣은 다음 **공유 ' 문서 .docx '** 대화 상자를 닫습니다.
    
15. 브라우저에서 **projectx-문서** 및 **SharePoint** 탭을 닫고 **Microsoft Office 홈** 탭을 클릭 합니다.
    
16. **잠재 고객 디자이너** 이름을 클릭 하 고 **로그 아웃**을 클릭 합니다.
    
이제 개발 VP 사용자 계정을 사용 하 여 액세스 방법을 살펴보겠습니다.
  
1. 개발 VP 계정 이름 및 암호를 사용[https://admin.microsoft.com](https://admin.microsoft.com)하 여 Office 365 portal ()에 로그인 합니다.
    
2. 타일 목록에서 **SharePoint**를 클릭합니다.
    
3. 브라우저의 새 **SharePoint** 탭에 있는 검색 상자에 **projectx** 를 입력 하 고 검색을 활성화 한 다음 **projectx** 팀 사이트를 클릭 합니다. projectx 팀 사이트에 대 한 브라우저에 새 탭이 표시 되어야 합니다.
    
4. **문서**를 클릭 한 다음 **문서 .docx** 파일을 클릭 합니다.
    
5. 브라우저의 **.docx** 탭에서 텍스트를 수정 합니다. **이 문서는 읽기 전용** 이라는 메시지가 표시 됩니다. 이는 개발 VP 사용자 계정에 사이트에 대 한 보기 권한만 있다는 이유로 예상 됩니다.
    
6. 브라우저에서 **문서 .docx**, **projectx-문서**및 **SharePoint** 탭을 닫습니다.
    
7. **Microsoft Office 홈** 탭을 클릭 하 고 **개발 VP** 이름을 클릭 한 다음 **로그 아웃**을 클릭 합니다.
    
이제 사용 권한이 없는 사용자 계정을 사용 하 여 액세스 하는 방법을 알아보겠습니다.
  
1. 사용자 3 계정 이름 및 암호를 사용[https://admin.microsoft.com](https://admin.microsoft.com)하 여 Office 365 portal ()에 로그인 합니다.
    
2. 타일 목록에서 **SharePoint**를 클릭합니다.
    
3. 브라우저의 새 **SharePoint** 탭에 있는 검색 상자에 **projectx** 를 입력 한 다음 검색을 활성화 합니다. **검색 조건과 일치** 하는 메시지가 없는 것을 볼 수 있습니다.
    
4. 메모장의 열린 인스턴스나 텍스트 편집기에서 projectx 사이트의 URL을 브라우저의 주소 표시줄에 복사한 다음 enter 키를 누릅니다. **** **액세스 거부** 페이지가 표시 됩니다.
    
5. 메모장 이나 텍스트 편집기에서 projectx Documents 폴더의 URL을 브라우저의 주소 표시줄에 복사 하 고 enter 키를 누릅니다. **** **액세스 거부** 페이지가 표시 됩니다.
    
6. 메모장 이나 텍스트 편집기에서 문서 .docx 파일의 URL을 브라우저의 주소 표시줄에 복사한 다음 enter 키를 누릅니다. **** **액세스 거부** 페이지가 표시 됩니다.
    
7. 브라우저에서 **SharePoint** 탭을 닫고 **Microsoft Office 홈** 탭을 클릭 한 다음 **사용자 3** 이름을 클릭 하 고 **로그 아웃**을 클릭 합니다.
    
이제 격리 된 SharePoint Online 사이트에 대 한 추가 실험 준비가 완료 되었습니다.
  
## <a name="next-step"></a>다음 단계

프로덕션 환경에 격리된 SharePoint Online 팀 사이트를 배포할 준비가 되면 [격리된 SharePoint Online 팀 사이트 디자인](design-an-isolated-sharepoint-online-team-site.md)에서 단계별 디자인 고려 사항을 참조하세요.
  
## <a name="see-also"></a>참고 항목

[격리된 SharePoint Online 팀 사이트](isolated-sharepoint-online-team-sites.md)
  
[클라우드 도입 TLG(테스트 랩 가이드)](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[기본 구성 개발/테스트 환경](https://docs.microsoft.com/office365/enterprise/base-configuration-dev-test-environment)
  
[Office 365 개발/테스트 환경](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)
  
[클라우드 도입 및 하이브리드 솔루션](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




