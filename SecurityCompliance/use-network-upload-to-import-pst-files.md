---
title: 네트워크 업로드를 사용 하 여 Office 365를 조직 PST 파일을 가져오려면
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: '관리자를 위한: 대량 가져오기 Office 365에서 사용자 사서함에 여러 PST 파일을 네트워크 업로드를 사용 하는 방법에 알아봅니다.'
ms.openlocfilehash: 81c799a8c820e9d9287f4792fe463d6a99b90e36
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666158"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>네트워크 업로드를 사용 하 여 Office 365를 조직 PST 파일을 가져오려면

> [!NOTE]
> 이 문서는 관리자입니다. 자신의 사서함에 PST 파일을 가져올 하려고 합니까? [가져오기 전자 메일, 연락처 및 일정 Outlook.pst 파일에서](https://go.microsoft.com/fwlink/p/?LinkID=785075) 를 참조 하십시오.
  
대량 가져오기 Office 365 사서함에 여러 PST 파일을 네트워크 업로드를 사용 하 여 필요한 단계별 지침은 다음과 같습니다. 에 대 한 네트워크 업로드를 사용 하 여 PST 파일을 Office 365 사서함으로 대량 가져오기, [PST 파일을 가져오려면 네트워크 업로드 사용에 대 한 Faq](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files)를 참조 하는 방법에 대 한 질문과 대답입니다.
  
[1 단계: SAS URL을 복사 하 고 Azure AzCopy를 설치 합니다.](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[2 단계: Office 365에 PST 파일을 업로드](#step-2-upload-your-pst-files-to-office-365)

[(선택 사항) Office 365에 보기 PST 파일의 목록이 업로드 3 단계:](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[4 단계: PST 가져오기 매핑 파일 만들기](#step-4-create-the-pst-import-mapping-file)

[5단계: Office 365에서 PST 가져오기 작업 만들기](#step-5-create-a-pst-import-job-in-office-365)

[6 단계: 데이터를 필터링 하 고 PST 가져오기 작업 시작](#step-6-filter-data-and-start-the-pst-import-job)

Note Office 365 사서함에 PST 파일을 가져오려면 한번만 1 단계를 수행 해야 합니다. 다음이 단계를 수행한 후 6 단계를 통해 2 단계를 업로드 하 고 PST 파일의 일괄 가져오기 사용할 때마다를 수행 합니다.

## <a name="before-you-begin"></a>시작하기 전에
  
- 역할을 할당 사서함 가져오기 내보내기 Exchange 온라인 Office 365 사서함에 PST 파일을 가져오려면 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 다음 자신을 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹](https://go.microsoft.com/fwlink/p/?LinkId=730688)에 "역할 그룹 만들기" 섹션이 있습니다.
    
    또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.
    
  - 역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.
    
    또는
    
  - Office 365 조직에서 전역 관리자 여야 해야 합니다.
    
  > [!TIP]
    > Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다. 
  
- 이 항목의 설명에 따라 Office 365에 PST 파일을 가져오기 위한 유일한 방법은 지원된 Azure AzCopy 도구를 사용 하는 합니다. Azure 저장소 탐색기를 사용 하 여 Azure 저장소 영역에 직접 PST 파일을 업로드할 수 없습니다.
    
- 파일 서버 또는 조직에 있는 공유 폴더에서 Office 365로 가져올 PST 파일을 저장 해야 합니다. 2 단계에서에서이 파일 서버에 저장 된 또는 Office 365에 폴더를 공유 하는 PST 파일을 업로드 하는 Azure AzCopy 도구를 실행 합니다.
    
- 이 절차를 복사 하 고 액세스 키가 포함 된 URL의 복사본을 저장 해야 합니다. 이 정보를 사용할 PST 파일을 업로드 하려면 2 단계 및 3 단계에서에서 Office 365에 업로드 된 PST 파일의 목록을 보려면 하려는 경우. 암호 또는 기타 보안 관련 정보를 보호 하는 동일 하 게이 URL을 보호 하기 위한 예방 조치를 수행 해야 합니다. 예는 암호화 된 USB 드라이브 또는 암호로 보호 된 Microsoft Word 문서에 저장할 수 있습니다. 이 예에 대 한 [자세한 내용](#more-information) 은 섹션 결합 된 URL 및 키를 참조 합니다. 
    
- Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니다. 비활성 사서함의 GUID를 지정 하 여이 작업을 수행 된 `Mailbox` PST 가져오기 매핑 파일에서 매개 변수입니다. 자세한 내용은이 항목의 **지침** 탭에서 4 단계를 참조 하십시오. 
    
- Exchange 하이브리드 배포에서 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져올 수 있습니다. PST 가져오기 매핑 파일에서 다음을 수행 하 여이 수행 합니다.
    
  - 사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 된 `Mailbox` 매개 변수입니다. 
    
  - **TRUE** 값을 지정 된 `IsArchive` 매개 변수입니다. 
    
    자세한 내용은 [4 단계를](#step-4-create-the-pst-import-mapping-file) 참조 하십시오. 
    
- PST 파일을 Office 365 사서함으로 가져온 후 사서함에 대 한 설정 보존 대기는 무기한 기간에 대 한 켜 집니다. 즉, 사서함에 할당 된 보존 정책 보존 보류 해제 하거나 보류를 해제 하려면 날짜를 설정할 때까지 처리 되지 않습니다. 이유 해야 할까요? 오래 된 메시지를 사서함으로 가져온 경우 이러한 수 영구적으로 삭제 됩니다 (비우기)가 보존 기간이 만료 되었기 때문에 사서함에 대해 구성 된 보존 설정에 따라 합니다. 사서함을 보존 대기 배치 이러한 새로 가져온 메시지 또는 사서함에 대 한 보존 설정을 변경 하려면 시간 부여를 관리 하는 사서함 소유자 시간을 제공 합니다. 보존 대기 상태를 관리 하는 방법에 대 한 제안에 대 한이 항목에서 **더 많은 정보** 탭을 참조 하십시오. 
    
- 기본적으로 Office 365 사서함으로 받을 수 있는 최대 메시지 크기는 35 MB입니다. 사서함에 대 한 *MaxReceiveSize* 속성에 대 한 기본값을 35 MB 로설정하면 때문입니다. 그러나는 최대 메시지 크기를 Office 365에서 수신에 대 한 제한은 150MB입니다. 따라서 35 MB, 150MB를 대상 사서함에서 *MaxReceiveSize* 속성의 값을 자동으로 바뀝니다는 Office 365를 가져올 서비스 보다 큰 항목을 포함 하는 PST 파일을 가져오는 경우. 이 메시지를 통해 최대 150MB 사용자 사서함으로 가져올 수 있도록 합니다. 
    
    > [!TIP]
    > 메시지 수신 크기를 식별 하는 사서함에 대 한 Exchange Online PowerShell에서이 명령을 실행할 수: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`합니다. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>1 단계: SAS URL을 복사 하 고 Azure AzCopy를 설치 합니다.

첫 단계를 다운로드 하는 Office 365에 PST 파일을 업로드 하려면 2 단계에서에서 실행 하는 도구는 Azure AzCopy 도구를 설치 하는 것입니다. 또한 조직에 대 한 SAS URL을 복사할 수 있습니다. 이 URL은 조직 및 공유 액세스 서명 (SAS) 키에 대 한 Microsoft 클라우드 Azure 저장소 위치에 대 한 네트워크 URL의 조합입니다. 이 키는 Azure 저장소 위치에 PST 파일을 업로드 하려면 필요한 권한을 제공 합니다. SAS URL을 보호 하기 위한 예방 조치를 수행 해야 합니다. 조직에 고유 하 고 2 단계에서에서 사용 됩니다.

> [!IMPORTANT]
> PST를 가져오려면 네트워크를 사용 하 여 파일 업로드 방법, 다음 절차의 단계 6b에서 다운로드할 수 있는 Azure AzCopy의 버전을 사용 하는 것이 좋습니다.
  
1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **가져오기**.
    
    > [!NOTE]
    > 보안에서 **가져오기** 페이지에 액세스 하려면 적절 한 사용 권한을 할당할 필요가 &amp; 준수 센터입니다. 자세한 내용은 **시작 하기 전에** 섹션을 참조 하십시오. 
    
3. **가져오기** 페이지에서 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새로 만들기 작업을 가져옵니다**.
    
    가져오기 작업 마법사가 표시 됩니다.
    
4. PST 가져오기 작업에 대 한 이름을 입력 하 고 **** 을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄만 사용 합니다. 맞춤법 검사 시 대문자로 사용 하거나 이름에 공백을 포함할 수 없습니다.
    
5. **업로드 하거나 데이터를 제공 하 시겠습니까?** 페이지, **데이터 업로드** 를 클릭 한 다음 **다음**을 클릭 합니다.
    
    ![네트워크 업로드를 만들려는 데이터 가져오기 작업 업로드를 클릭 합니다.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. **데이터 가져오기** 페이지에서 다음 두 작업을 수행 합니다. 
    
    ![SAS URL을 복사 하 고 가져오기 데이터 페이지에서 Azure AzCopy 도구를 다운로드](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a. 2 단계에서 **네트워크 업로드 SAS URL 표시**를 클릭 합니다. SAS URL 표시 된 후 **클립보드에 복사** 를 클릭 하 고 붙여넣으십시오 하 고 나중에 액세스할 수 있도록 파일에 저장 합니다.
    
    b. 3 단계에서 다운로드 하 고 Azure AzCopy 도구를 설치 하려면 **Azure AzCopy 다운로드** 클릭 합니다. 팝업 창의 AzCopy를 설치 하려면 **실행** 을 클릭 합니다. 
    
> [!NOTE]
> **데이터 가져오기** 페이지 열기으로 남길 수 (대비 SAS URL을 다시 복사 해야할) 하거나 닫으려면 **취소** 를 클릭 합니다. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>2 단계: Office 365에 PST 파일을 업로드

이제 AzCopy.exe 도구를 사용 하 여 Office 365에 PST 파일을 업로드 하려면 준비가 되었습니다. 이 도구는 업로드 하 고 Microsoft 클라우드에서는 Azure 저장소 위치에 저장 합니다. 앞에서 설명한 것 처럼 Azure 저장소 위치를 PST 파일을 업로드 하는 동일한 지역 Microsoft 데이터 센터에서 Office 365 조직 위치한가 있어야 합니다. 이 단계를 완료 하려면 PST 파일에는 파일 공유 또는 조직에서 파일 서버에 배치 해야 합니다. 이 다음 절차에는 원본 디렉터리 이라고 합니다. AzCopy 도구를 실행할 때마다 서로 다른 원본 디렉터리를 지정할 수 있습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트를 엽니다.
    
2. 1 단계에서에서 설치한 AzCopy.exe 도구 디렉터리로 이동 합니다. 로 이동 하는 기본 위치에는 도구를 설치 하는 경우 `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`합니다.
    
3. Office 365에 PST 파일을 업로드 하려면 다음 명령을 실행 합니다.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    다음 표에서 매개 변수 및 해당 필수 값을 설명합니다. 참고 이러한 매개 변수에 대 한 이전 단계에서 얻은 정보는 값에 사용 됩니다.
    
    |**매개 변수**|**설명**|**예**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Office 365로 업로드 됩니다 PST 파일을 포함 하 여 조직에서 원본 디렉터리를 지정 합니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |1 단계에서에서 구한 SAS URL을 지정 합니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> **팁:** (선택 사항) PST 파일을 업로드 하려면 Azure 저장소 위치에 하위 폴더를 지정할 수 있습니다. SAS URL에서 "ingestiondata") (이후 하위 폴더 위치를 추가 하 여이 작업을 수행 합니다. 첫번째 예제에서는; 하위 폴더를 지정 하지 않으면 즉, Azure 저장소 위치는 Pst ( *ingestiondata* 라는) 루트에 업로드 합니다. 두번째 예제 Azure 저장소 위치의 루트에서 ( *PSTFiles* 라는) 하위 폴더에 PST 파일을 업로드 합니다.<br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> 또는  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |자세한 상태 메시지를 로그 파일에 출력합니다. 기본적으로 자세한 로그 파일은 %LocalAppData%\Microsoft\Azure\AzCopy의 AzCopyVerbose.log로 지정됩니다. 이 옵션에 대한 기존 파일 위치를 지정하면 해당 파일에 자세한 로그 파일이 추가됩니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |이 선택적 스위치 AzCopy 도구에서는로 지정 된 원본 디렉터리의 하위 폴더에 있는 Pst 파일을 복사 되도록 재귀 모드를 지정 된 `/Source:` 매개 변수입니다.  <br/> **참고:** 이 스위치를 포함 하는 경우 하위 폴더에서 PST 파일 다른 파일 경로 이름에에서 갖습니다 Azure 저장소 위치는 업로드 하 고 나면. 4 단계에서에서 만든 CSV 파일의 정확한 파일 경로 지정 해야 합니다.<br/> | `/S` <br/> |
    | `/Y` <br/> |이 필요한 스위치 Azure 저장소 위치에 PST 파일을 업로드 하면 쓰기 전용 SAS 토큰의 사용을 허용 합니다. 1 단계에서 얻은 SAS URL (에 지정 하 고 `/Dest:` 매개 변수)은이 스위치를 포함 해야 하는 이유는 쓰기 전용 SAS URL을 합니다. 참고는 쓰기 전용 SAS URL에 관여 하지 않으므로 Azure 저장소 탐색기를 사용 하 여 Azure 저장소 위치에 업로드 된 PST 파일의 목록을 볼 수 있습니다.<br/> | `/Y` <br/> |
   
다음은 각 매개 변수에 대한 실제 값을 사용하는 AzCopy.exe 도구에 대한 구문 예입니다.
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

이 명령을 실행하면 PST 파일의 업로드 진행률을 보여 주는 상태 메시지가 표시됩니다. 마지막 상태 메시지에는 성공적으로 업로드된 파일의 총 수가 표시됩니다. 

> [!TIP]
> 성공적으로 AzCopy.exe 명령을 실행 하 고 매개 변수를 모두 올바른지 확인 합니다 명령줄 구문 정보를 복사한 동일한 (보안) 파일의 복사본을 저장 하면 1 단계에서에서 구한 합니다. 다음 복사 수 있으며이 명령은 명령 프롬프트에서 Office 365에 PST 파일을 업로드 하려면 AzCopy.exe 도구를 실행할 때마다 붙여넣습니다. 변경 해야할 유일한 값에 대 한 가지는 `/Source:` 매개 변수입니다. 이 PST 파일의 위치는 원본 디렉터리에 따라 달라 집니다.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(선택 사항) Office 365에 보기 PST 파일의 목록이 업로드 3 단계:

단계는 선택 사항으로 설치 하 고 (즉, 무료, 공개 소스 도구) Microsoft Azure 저장소 탐색기를 사용 하 여 Azure blob에 업로드 했을 때 PST 파일의 목록을 볼 수 있습니다. 이 작업을 수행 하는 이유에 두 가지가 있습니다.
  
- 공유 폴더 또는 조직에서 파일 서버에서 PST 파일은 Azure blob에 성공적으로 업로드 된 확인 합니다.
    
- Azure blob를 업로드 한 각 PST 파일에 대 한 파일 이름 (및 하위 폴더 경로 이름을 하나를 포함 하는 경우)를 확인 합니다. 폴더 경로 각 PST 파일에 대 한 이름을 모두 지정 해야 하기 때문에 다음 단계에서 파일에 매핑 PST를 작성할 때 매우 유용 합니다. 이 이름 확인 (영문) PST 매핑 파일의 잠재적인 오류를 줄일 수 있습니다.
    
Microsoft Azure 저장소 탐색기 미리 보기에서 됩니다.
  
> [!IMPORTANT]
> Azure 저장소 탐색기를 사용 하 여 업로드 하거나 PST 파일을 수정 하려면 수는 없습니다. Office 365에 PST 파일을 가져오기 위한 유일한 방법은 지원된 AzCopy를 사용 하는 것입니다. 또한 Azure blob를 업로드 한 PST 파일을 삭제할 수 없습니다. PST 파일을 삭제 하려고 하는 경우 필요한 사용 권한을 있지 않은 경우에 대 한 오류가 표시 됩니다. 참고 모든 PST 파일 Azure 저장소 영역에서 자동으로 삭제 됩니다. 없는 경우 진행 상황을 **ingestiondata** 컨테이너에 있는 다음 모든 PST 파일에 가져오기 작업이 30 일 가장 최근의 가져오기 작업을 만든 후 삭제 됩니다.
  
Azure 저장소 탐색기를 설치 및 Azure 저장소 영역에 연결 합니다.
  
1. 다운로드 하 고 [Microsoft Azure 저장소 탐색기 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 설치 합니다.
    
2. Microsoft Azure 저장소 탐색기를 시작 하 고 왼쪽된 창에서 **계정 저장소를** 마우스 오른쪽 단추로 클릭 **Azure 저장소에 대 한 연결**을 클릭 합니다.
    
    ![저장소 계정을 마우스 오른쪽 단추로 클릭 하 고 Azure 저장소에 연결을 클릭 한 다음](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. **공유 액세스 서명 (SAS) URI 또는 연결 문자열 사용** 을 클릭 하 고 **** 을 클릭 합니다.
    
4. **SAS URI를 사용**을 클릭 하 고 **URI**아래에 있는 상자에 1 단계에서에서 구한 SAS URL을 붙여넣습니다 **다음**을 클릭 합니다.
    
5. **연결 요약** 페이지에서 연결 정보를 검토 하 고 **연결**을 클릭 수 있습니다.
    
    **Ingestiondata** 컨테이너를 열 수 있습니다. 2 단계에서에서 업로드 PST 파일을 포함 합니다. **Ingestiondata** 컨테이너는 **저장소 계정** 아래에 \> **(SAS-Attached 서비스)** \> **Blob 컨테이너**입니다. 
    
    ![Azure 저장소 탐색기는 사용자가 업로드한 PST 파일 목록이 표시됩니다.](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Microsoft Azure 저장소 탐색기를 사용 하 여이 끝나면 **ingestiondata**마우스 오른쪽 단추로 클릭 하 고 Azure 저장소 영역에서 연결을 끊으려면 **분리** 클릭 합니다. 그렇지 않은 경우 받게 오류가 다음에 연결 하려고 하면 됩니다. 
    
    ![수집을 마우스 오른쪽 단추로 클릭하고 분리를 클릭하여 Azure 저장소 영역에서 연결 끊기](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>4 단계: PST 가져오기 매핑 파일 만들기

Office 365 조직에 대 한 Azure 저장소 위치로 PST 파일을 업로드 한 후 다음 단계에 쉼표를 만들려는 구분 하 여 PST 파일을 가져올 수는 어떤 사용자 사서함을 지정 하는 값 (CSV) 파일입니다. PST 가져오기 작업을 만들 때 다음 단계에는이 CSV 파일을 제출할 수 있습니다.
  
1. [PST 가져오기 매핑 파일의 복사본을 다운로드](https://go.microsoft.com/fwlink/p/?LinkId=544717)합니다.
    
2. CSV 파일을 열거나 로컬 컴퓨터에 저장합니다. 다음 예에서는 완료된 PST 가져오기 매핑 파일(메모장에서 열림)을 보여 줍니다. CSV 파일을 편집할 경우 Microsoft Excel을 사용하는 것이 훨씬 더 쉽습니다.


    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,,annb.pst,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,annb_archive.pst,annb@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,,donh.pst,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,donh_archive.pst,donh@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,PSTFiles,pilarp.pst,pilarp@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,PSTFiles,pilarp_archive.pst,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,PSTFiles,tonyk.pst,tonyk@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,PSTFiles,tonyk_archive.pst,tonyk@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,PSTFiles,zrinkam.pst,zrinkam@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,PSTFiles,zrinkam_archive.pst,zrinkam@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    ```
    첫째 행 또는 CSV 파일의 머리글 행을 사용자 사서함에 PST 파일을 가져오려면 PST 가져오기 서비스에서 사용 되는 매개 변수를 나열 합니다. 각 매개 변수 이름은 쉼표로 구분 됩니다. 각 행 머리글 행에서 특정 사서함에 PST 파일 가져오기 (영문)에 대 한 매개 변수 값을 나타냅니다. 가져올 사용자 사서함에는 각 PST 파일에 대 한 행을 할 수 있습니다. 실제 데이터와 매핑 파일의 개체 틀 데이터를 교체 해야 합니다.

   **참고:** SharePoint 매개 변수를 포함 하는 머리글 행에서 아무것도 변경 하지 마십시오 PST 가져오기 과정에서 무시 됩니다. 

 3. 다음 표의 정보를 사용하여 CSV 파일을 필요한 정보로 채웁니다.


    |**매개 변수**|**설명**|**예**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |데이터를 가져올 수는 Office 365 서비스를 지정 합니다. 사용자 사서함을 PST 파일을 가져오려면, 사용 `Exchange`합니다.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> |2 단계에서에서 PST 파일을 업로드 하는 Azure 저장소 위치에 폴더 위치를 지정 합니다.  <br/> SAS URL에는 선택적 하위 폴더 이름을 포함 하지 않았으므로 하는 경우는 `/Dest:` 매개 변수 2 단계에서에서이 매개 변수를 비워둘 CSV 파일에 있습니다. 하위 폴더 이름을 포함 하는 경우이 매개 변수에서 지정 (합니다 두번째 예제 참조). 이 매개 변수의 값은 대/소문자 구분 됩니다.<br/> 두 방법 모두에 대 한 값에 "ingestiondata"를 포함 *하지* 는 `FilePath` 매개 변수입니다.  <br/><br/> **중요:** 파일 경로 이름에 대 한 대/소문자에 SAS URL에는 선택적 하위 폴더 이름을 포함 하는 경우를 사용 하는 경우와 동일 해야는 `/Dest:` 2 단계에서에서 매개 변수입니다. 예: 사용 하는 경우 `PSTFiles` 하위 폴더에 대 한 2 단계에서에서 이름을 지정 하 고 다음을 사용 `pstfiles` 에 `FilePath` CSV 파일의 매개 변수, PST 파일에 대 한 가져오기가 실패 합니다. 두 경우 모두 동일한 대/소문자를 사용 해야 합니다.<br/> |(공백으로 둠)  <br/> 또는  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |사용자 사서함에 가져올 PST 파일의 이름을 지정 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다.<br/> <br/>**중요:** CSV 파일에서 PST 파일 이름에 대 한 대/소문자 2 단계에서에서 Azure 저장소 위치에 업로드 된 PST 파일로 동일 해야 합니다. 예: 사용 하는 경우 `annb.pst` 에 `Name` 하 여 CSV 파일을 하지만 실제 PST 파일의 이름에서 매개 변수는 `AnnB.pst`, 해당 PST 파일에 대 한 가져오기가 실패 합니다. CSV 파일의 PST의 이름이 동일한 대/소문자를 사용 하 여 실제 PST 파일로 확인 해야 합니다.<br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |PST 파일을 가져올 수는 사서함의 전자 메일 주소를 지정 합니다. 참고 PST 가져오기 서비스 공용 폴더에 PST 파일 가져오기 (영문)이 지원 되지 않으므로 공용 폴더를 지정할 수 없습니다.<br/> 비활성 사서함을 PST 파일을 가져오려면,이 매개 변수에 대 한 사서함 GUID를 지정 해야 합니다. 이 GUID를 가져오려면 다음 PowerShell 명령을 Exchange Online에서 실행: ' Get-mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> <br/>**Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-mailbox<identity of active mailbox> | FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid' 합니다.  <br/> | `annb@contoso.onmicrosoft.com` <br/> 또는  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | PST 파일을 사용자의 보관 사서함으로 가져올 것인지 여부를 지정합니다. 다음 두 가지 옵션이 있습니다.<br/><br/>**FALSE** -사용자의 기본 사서함을 PST 파일을 가져옵니다.  <br/> **TRUE** -사용자의 보관 사서함을 PST 파일을 가져옵니다. 이 가정 하는 [사용자의 보관 사서함 사용 하도록 설정](enable-archive-mailboxes.md)합니다.<br/><br/>이 매개 변수를 설정 하는 경우 `TRUE` 하 고 사용자의 보관 사서함 설정 되지 않은, 해당 사용자에 대 한 가져오기가 실패 합니다. 한 명의 사용자에 대 한 가져오기 실패 하는 경우 (자신의 아카이브를 사용할 수 없는 하 고이 속성은 설정 하기 때문에 `TRUE`), 가져오기 작업에서 다른 사용자가 영향을 받지 않습니다.<br/>  이 매개 변수를 지정 하지 않으면 사용자의 기본 사서함에 PST 파일을 가져옵니다.  <br/> <br/>**참고:** 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져오려면, 방금 지정 `TRUE` 이 매개 변수에 대 한 메일에 대 한 사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 하 고는 `Mailbox` 매개 변수입니다.  <br/> | `FALSE` <br/> 또는  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | PST 파일을 가져온 사서함 폴더를 지정 합니다.  <br/>  이 매개 변수를 지정 하지 않고 공백으로 두면 PST 명명 된 **가져온** (받은 편지함 폴더와 다른 기본 사서함 폴더와 동일한 수준) 사서함의 루트 수준에 있는 새 폴더를으로 가져옵니다.  <br/>  지정 하는 경우 `/`, PST 파일의 항목에에서 사용자의 받은 편지함 폴더에서 직접 가져올 수 됩니다.  <br/><br/>  지정 하는 경우 `/<foldername>`, 라는 폴더를 가져올 PST 파일의 항목에에서 * \<foldername\> * 합니다. 예: 사용 하는 경우 `/ImportedPst`, **ImportedPst**라는 폴더에 항목을 가져올 수는 있습니다. 이 폴더는 받은 편지함 폴더와 같은 수준에 있는 사용자의 사서함에 배치 됩니다.<br/><br/> **팁:** Pst 파일을 가져오려면 가장 적합 한 폴더 위치를 결정할 수 있도록이 매개 변수를 사용해 몇 테스트 일괄 처리를 실행 하는 것이 좋습니다.  <br/> |(공백으로 둠)  <br/> 또는  <br/>  `/` <br/> 또는  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |이 선택적 매개 변수는 ANSI 파일 형식에서 PST 파일을 가져오기 위해 사용 하 여 코드 페이지에 대 한 숫자 값을 지정 합니다. 이 매개 변수는 일반적으로 이러한 언어 문자 인코딩에 대 한 더블 바이트 문자 집합 (DBCS)을 사용 하기 때문에 중국어, 일본어 및 한국어 (CJK) 조직에서 PST 파일을 가져오기 위해 사용 됩니다. 이 매개 변수는 사서함 폴더 이름에 대 한 DBCS를 사용 하는 언어에 대 한 PST 파일을 가져오려면 사용 되지 않습니다, 하는 경우 폴더 이름은 가져온 후 왜곡 자주는 합니다.<br/><br/> 이 매개 변수를 사용 하 여 지원 되는 값의 목록에 대 한 [코드 페이지 식별자](https://go.microsoft.com/fwlink/p/?LinkId=328514)를 참조 하십시오.  <br/> <br/>**참고:** 앞부분에 명시 된,이 선택적 매개 변수 이며 CSV 파일에 포함할 필요가 없습니다. 또는 포함 하 고 하나 이상의 행에 대 한 값은 비워둡니다.<br/> |(공백으로 둠)  <br/> 또는  <br/>  `932`(ANSI/OEM 일본어에 대 한 코드 페이지 식별자는)  <br/> |
    | `SPFileContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPManifestContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPSiteUrl` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>5단계: Office 365에서 PST 가져오기 작업 만들기

다음 단계에서는 Office 365에서 가져오기 서비스에서 PST 가져오기 작업을 만드는 것입니다. 앞에서 설명한 것 처럼 4 단계에서에서 만든 PST 가져오기 매핑 파일을 전송 됩니다. 새 작업을 만든 후 Office 365 PST 파일의 데이터를 분석 하 고이 다음 PST 가져오기 매핑 파일에 지정 된 사서함에 실제로 가져온 가져옵니다 데이터를 필터링 하는 기회를 제공 하는 ( [6 단계](#step-6-filter-data-and-start-the-pst-import-job)참조).
  
1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.
    
3. **가져오기** 페이지에서 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새로 만들기 작업을 가져옵니다**.
    
    **참고:** 보안에서 **가져오기** 페이지에 액세스 하려면 적절 한 사용 권한을 할당할 필요가 &amp; 준수 센터 새 가져오기 작업을 만들 수 있습니다. 자세한 내용은 **시작 하기 전에** 섹션을 참조 하십시오. 
    
4. PST 가져오기 작업에 대 한 이름을 입력 하 고 **** 을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄만 사용 합니다. 맞춤법 검사 시 대문자로 사용 하거나 이름에 공백을 포함할 수 없습니다.
    
5. **업로드 하거나 데이터를 제공 하 시겠습니까?** 페이지, **데이터 업로드** 를 클릭 한 다음 **다음**을 클릭 합니다.
    
    ![네트워크 업로드를 만들려는 데이터 가져오기 작업 업로드를 클릭 합니다.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. **데이터 가져오기** 페이지에서 4 단계에서 클릭는 **간단 하죠 내 파일 업로드** 및 **매핑 파일에 액세스할 수 있는 I** 확인란을 선택한 후 **다음**을 클릭 합니다.
    
    ![4 단계에서 두 확인란을 클릭 합니다.](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. **매핑 파일 선택** 페이지에서 4 단계에서에서 만든 PST 가져오기 매핑 파일을 제출 **매핑 파일을 선택** 합니다.를 클릭 합니다. 
    
    ![가져오기 작업에 대해 만든 CSV 파일을 제출 선택 매핑 파일을 클릭 합니다.](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. CSV 이름 후 파일 아래에 표시 **파일 이름 매핑 (영문)** **유효성 검사** 오류에 대 한 CSV 파일을 확인 하려면를 클릭 합니다. 
    
    ![유효성 검사 오류에 대 한 CSV 파일을 확인 하려면 클릭](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    PST 가져오기 작업을 만들려면 성공적으로 유효성을 검사 하려면 CSV 파일에 있습니다. 참고 파일 이름은 유효성을 검사 성공적으로 후 녹색으로 변경 됩니다. 유효성 검사에 실패 하는 경우에 **로그 보기** 링크를 클릭 합니다. 실패 한 파일의 각 행에 대 한 오류 메시지와 함께 유효성 검사 오류 보고서가 열릴 합니다. 
    
9. PST 매핑 파일을 성공적으로 확인 한 후 사용 약관 문서 읽고 확인란을 클릭 합니다.
    
10. 작업을 제출 하려면 **저장** 을 클릭 하 고 작업이 성공적으로 만들어지면 **Close** 를 클릭 합니다. 
    
    **진행 중인 분석** 의 상태가 상태 플라이 아웃 페이지가 표시 됩니다 하 고 새 가져오기 작업 **가져오기** 페이지의 목록에 표시 됩니다. 
    
11. **새로 고칠** 을 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **상태** 열에 표시 되는 상태 정보를 업데이트 합니다. 분석이 완료 되는 데이터를 가져올 수 있도록 준비 하는 경우에 상태 **분석 완료**로 변경 됩니다.
    
    매핑 파일에 나열 된 각 PST 파일의 상태와 같은 가져오기 작업에 대 한 자세한 정보를 포함 하는 상태 플라이 아웃 페이지를 표시 하려면 가져오기 작업을 클릭 수 있습니다.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>6 단계: 데이터를 필터링 하 고 PST 가져오기 작업 시작

5 단계에서에서 가져오기 작업을 만든 후 Office 365을 분석 하 여 PST 파일의 데이터 (을 안전 하 게 방식으로)에서 다양 한 메시지 형식과 PST 파일에 포함 된 항목의 보존 기간을 식별 하 여 합니다. 분석이 완료 되 고 데이터를 가져올 준비가 되었습니다, PST 파일에 포함 된 모든 데이터를 가져올 수 있는 옵션 했거나 데이터를 가져온 가져옵니다을 제어 하는 필터를 설정 하 여 가져온 데이터를 자를 수 있습니다.
  
1. 보안에서 **가져오기** 페이지에서 &amp; 준수 센터 5 단계에서에서 만든 가져오기 작업에 대 한 **Office 365로 가져올 준비** 를 클릭 합니다. 
    
    ![만든 가져오기 작업 옆에 있는 Office 365로 가져올 준비를 클릭 합니다.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    페이지 날아가기 PST 파일에 대 한 정보 및 가져오기 작업에 대 한 기타 정보가 표시 됩니다.
    
2. 플라이 아웃 페이지에서 **Office 365에는 가져오기**를 클릭 합니다.
    
    **데이터를 필터링** 페이지가 표시 됩니다. Office 365를 데이터의 기간에 대 한 정보를 비롯 하 여 PST 파일에 수행 하 여 분석에서 발생 하는 데이터 인 사이트를 포함 합니다. 이 시점 그대로 모든 데이터를 가져오거나 가져올 하는 데이터를 필터링 옵션이 제공 됩니다. 
    
    ![PST 파일의 데이터를 높이고 또는 모두를 가져올 수 있습니다.](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. 다음 중 하나를 수행합니다.
    
    a. 가져올 데이터를 높이고, 하려면 **예를 가져오기 전에으로 필터링 합니다.** 를 클릭 합니다.
    
    PST 파일의 데이터를 필터링 하 고 다음 가져오기 작업을 시작 하는 방법에 대 한 자세한 단계별 지침은 [Office 365에 PST 파일을 가져올 때 데이터를 필터링](filter-data-when-importing-pst-files.md)을 참조 하십시오.
    
    또는
    
    b. PST 파일에서 모든 데이터를 가져오려면를 **아니오, 모든 작업을 가져오려면** 클릭 하 고 **** 을 클릭 합니다.
    
4. 모든 데이터를 가져오려면 선택한 경우에 가져오기 작업을 시작 하려면 **데이터 가져오기** 를 클릭 합니다. 
    
    가져오기 작업의 상태가 **가져오기** 페이지에서 표시 됩니다. 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로고침** **상태** 열에 표시 되는 상태 정보를 업데이트 합니다. 가져올 각 PST 파일에 대 한 상태 정보를 표시 하는 상태 플라이 아웃 페이지를 표시 하려면 가져오기 작업을 클릭 합니다. 

## <a name="how-the-import-process-works"></a>가져오기 프로세스의 작동 방식
  
대량 가져오기 사용자 사서함에 PST 파일을 Office 365를 가져올 서비스와 네트워크 업로드 옵션을 사용할 수 있습니다. 네트워크 업로드는 업로드 PST 파일 Microsoft 클라우드에서 임시 저장 영역을 의미 합니다. 그런 다음 Office 365 가져오기 서비스 대상 사용자 사서함에 저장 영역에서 PST 파일을 복사 합니다.
  
그림 및 Office 365에서 사서함에 PST 파일을 가져오려면 네트워크 업로드 프로세스 설명은 다음과 같습니다.
  
![워크플로 네트워크의 Office 365에 PST 파일을 가져오려면 프로세스 업로드](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **다운로드 PST 가져오기 도구와 개인 키 Azure 저장소 위치** -첫번째 단계는 Azure AzCopy 명령줄 도구 및 Microsoft 클라우드에서 Azure 저장소 위치에 PST 파일을 업로드 하는 데 사용 하는 선택 키를 다운로드 합니다. Office 365 보안에서 **가져오기** 페이지에서 이러한 가져올 &amp; 준수 센터입니다. 키 (보안 액세스 (SAS) 서명 키 라는, 개인을 PST 파일을 업로드 하려면 필요한 권한을 제공 하 고 보호 Azure 저장소 위치입니다. 이 액세스 키 조직에 고유 하 고 Microsoft 클라우드로 업로드 하려는 하 고 나면 PST 파일에 무단으로 액세스를 방지할 수 있습니다. 참고 Office 365에 PST 파일 가져오기 (영문)을 별도 Azure 구독을 조직 필요 하지 않습니다. 
    
2. (1 단계에서 다운로드 한) AzCopy.exe 도구를 사용 하 여를 업로드 하 고 동일한 지역 Microsoft 데이터 센터에 상주 하는 Azure 저장소 위치에 PST 파일을 저장 하는 것을 **Azure 저장소 위치에 PST 파일을 업로드할** -다음 단계를 Office 365 조직에 있는 경우 Office 365로 가져올 PST 파일을 업로드 하려면 파일 공유 또는 조직에서 파일 서버에 배치할 수 해야 합니다.
    
    Azure 저장소 위치로 업로드 하려는 하 고 나면 PST 파일의 목록을 보려면 수행할 수 있는 단계는 선택 사항 인지 note 합니다.
    
3. 어떤 사용자 사서함 PST 파일은 가져올 PST 파일을 사용할 수를 지정 하는 쉼표로 구분 된 값 (CSV) 파일을 만들려면 다음 단계는 **PST 가져오기 매핑 파일을 만드는** -Azure 저장소 위치에 PST 파일을 업로드 된 후,  사용자의 기본 사서함 또는 보관 사서함으로 가져옵니다. Office 365를 가져올 서비스 CSV 파일의 정보를 사용 하 여 PST 파일을 가져올 수 있습니다.
    
4. **PST 만들기 작업 가져오기** -다음 단계는 보안에서 **가져오기** 페이지에서 PST 가져오기 작업을 만들려면 &amp; 준수 센터 및 이전 단계에서 만든 PST 가져오기 매핑 파일을 제출 합니다. 가져오기 작업을 만든 후에 Office 365 PST 파일의 데이터를 분석 하 고 데이터를 실제로 PST 가져오기 매핑 파일에 지정 된 사서함에 가져온 가져옵니다을 제어 하는 필터를 설정할 수 있는 기회를 제공 합니다. 
    
5. **필터 사서함으로 가져올 PST 데이터** -가져오기 작업을 만들고 시작 후, Office 365을 분석 하 여 PST 파일의 데이터 (안전 하 고 안전 하 게) PST 파일에 포함 된 다양 한 메시지 형식과 항목의 보존 기간을 식별 하 여 . 분석이 완료 되 고 데이터를 가져올 준비가 되었습니다, PST 파일에 포함 된 모든 데이터를 가져올 수 있는 옵션 했거나 데이터를 가져온 가져옵니다을 제어 하는 필터를 설정 하 여 가져온 데이터를 자를 수 있습니다.
    
6. **PST 가져오기 작업을 시작** -가져오기 작업이 시작 된 후, Office 365 정보를 사용 하는 PST 가져오기 매핑 파일에 사용자 사서함에 그 Azure 저장소 위치에서 Pst 파일을 가져옵니다. 보안에서 **가져오기** 페이지에 표시 됩니다 (가져올 각 PST 파일에 대 한 정보를 포함 하 여) 가져오기 작업에 대 한 상태 정보 &amp; 준수 센터입니다. 가져오기 작업이 완료 되 면 작업에 대 한 상태가 **완료**로 설정 됩니다.
  
## <a name="more-information"></a>추가 정보

- Office 365에 PST 파일을 가져올 이유?
    
  - Office 365를 조직의 보관 메시징 데이터를 가져오려면 좋은 방법입니다.
    
  - 이러한 데이터는 클라우드에 저장되므로 모든 장치에서 사용할 수 있습니다.
    
  - Office 365 규정 준수 기능을 가져온 PST 파일에서 데이터에 적용할 수 있도록 하 여 조직의 규정 준수 요구를 충족 도움이 됩니다. 이는 다음이 포함 됩니다.
    
  - [보관 사서함](enable-archive-mailboxes.md) 및 사용자에 게 가져온 데이터를 저장할 추가 사서함 저장 공간 [보관 자동 확장](enable-unlimited-archiving.md) 을 사용 하도록 설정 합니다. 
    
  - 가져온 데이터를 유지할 [소송 보존으로 설정](https://go.microsoft.com/fwlink/?linkid=856286) 에서 사서함을 배치 합니다. 
    
  - Microsoft [eDiscovery 도구](search-for-content.md) 를 사용 하 여 가져온 데이터를 검색 합니다. 
    
  - [Office 365 보존 정책을](retention-policies.md) 사용 하 여 가져온 데이터를 보존 기간, 및 보존 기간이 만료 후 수행할 동작을 제어 합니다. 
    
  - [Office 365 감사 로그에](search-the-audit-log-in-security-and-compliance.md) 대 한 가져온 데이터에 영향을 주는 사서함과 관련 된 이벤트를 검색 합니다. 
    
  - 규정 준수를 위해 데이터를 보관 하려면 [비활성 사서함](create-and-manage-inactive-mailboxes.md) 데이터를 가져오려고 합니다. 
    
  - [데이터 손실 방지 정책](data-loss-prevention-policies.md) 를 사용 하 여 중요 한 데이터 조직 외부에 누출 하지 못하도록 합니다. 
  
- 1 단계에서에서 얻은 공유 액세스 서명 (SAS) URL의 예는 다음과 같습니다. 이 예제에는 Office 365에 PST 파일을 업로드 하는 AzCopy.exe 도구에서 실행 하는 명령에 대 한 구문을 들어 있습니다. 암호 또는 기타 보안 관련 정보를 보호 하는 것 처럼 SAS URL을 보호 하기 위한 예방 조치를 수행 해야 합니다.

    ```
    SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D

    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y

    EXAMPLES

    This example uploads PST files to the root of the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
    
    This example uploads PST files to a subfolder named PSTFiles  in the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
``

- As previously explained, the Office 365 Import service turns on the retention hold setting (for an indefinite duration) after PST files are imported to a mailbox. This means the  *RetentionHoldEnabled*  property is set to  **True** so that the retention policy assigned to the mailbox won't be processed. This gives the mailbox owner time to manage the newly-imported messages by preventing a deletion or archive policy from deleting or archiving older messages. Here are some steps you can take to manage this retention hold: 
    
    - After a certain period of time, you can turn off the retention hold by running the **Set-Mailbox -RetentionHoldEnabled $false** command. For instructions, see [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
   - You can configure the retention hold so that it's turned off on some date in the future. You do this by running the **Set-Mailbox -EndDateForRetentionHold *date*** command. For example, assuming that today's date is July 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  **Set-Mailbox -EndDateForRetentionHold 8/1/2016**. In this scenario, you would leave the  **RetentionHoldEnabled**  property set to  *True*. For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
   - You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    
