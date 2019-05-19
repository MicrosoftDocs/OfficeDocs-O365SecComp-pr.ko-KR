---
title: 네트워크 업로드를 사용 하 여 조직 PST 파일을 Office 365로 가져오기
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: '관리자: 네트워크 업로드를 사용 하 여 여러 PST 파일을 Office 365의 사용자 사서함으로 대량 가져오는 방법에 대해 알아봅니다.'
ms.openlocfilehash: fb64eecdbeac40aa597d17459f06525b8859fb1f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156170"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>네트워크 업로드를 사용 하 여 조직 PST 파일을 Office 365로 가져오기

> [!NOTE]
> 이 문서는 관리자를 위한 것입니다. PST 파일을 자체 사서함으로 가져오시겠습니까? [Outlook .pst 파일에서 전자 메일, 연락처 및 일정 가져오기를](https://go.microsoft.com/fwlink/p/?LinkID=785075) 참조 하세요.
  
다음은 네트워크 업로드를 사용 하 여 여러 PST 파일을 Office 365 사서함으로 대량 가져오는 데 필요한 단계별 지침입니다. 네트워크 업로드를 사용 하 여 Office 365 사서함에 PST 파일을 대량으로 가져오는 방법에 대 한 질문과 대답은 [faq for network upload to a pst files](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files)를 참조 하십시오.
  
[1 단계: SAS URL을 복사 하 고 Azure AzCopy을 설치 합니다.](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[2 단계: Office 365에 PST 파일 업로드](#step-2-upload-your-pst-files-to-office-365)

[반드시 3 단계: Office 365에 업로드 된 PST 파일 목록 보기](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[4 단계: PST 가져오기 매핑 파일 만들기](#step-4-create-the-pst-import-mapping-file)

[5 단계: Office 365에서 PST 가져오기 작업 만들기](#step-5-create-a-pst-import-job-in-office-365)

[6 단계: 데이터 필터링 및 PST 가져오기 작업 시작](#step-6-filter-data-and-start-the-pst-import-job)

PST 파일을 Office 365 사서함으로 가져오려면 1 단계를 한 번만 수행 하면 됩니다. 이러한 단계를 수행한 후에는 PST 파일의 일괄 처리를 업로드 하 고 가져올 때마다 2-3 단계를 수행 합니다.

## <a name="before-you-begin"></a>시작하기 전에
  
- PST 파일을 Office 365 사서함으로 가져오려면 Exchange Online의 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. 자세한 내용은 [Manage role groups](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하십시오.
    
    또한 보안 & 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.
    
  - Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    또는
    
  - Office 365 조 직의 전역 관리자 여야 합니다.
    
  > [!TIP]
    > Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다. 
  
- PST 파일을 Office 365로 가져오는 유일한 방법은이 항목에 설명 된 대로 Azure AzCopy 도구를 사용 하는 것입니다. Azure 저장소 탐색기를 사용 하 여 PST 파일을 Azure storage 영역에 직접 업로드할 수는 없습니다.
    
- 조직의 파일 서버나 공유 폴더에서 Office 365로 가져오려는 PST 파일을 저장 해야 합니다. 2 단계에서는이 파일 서버 또는 공유 폴더에 저장 된 PST 파일을 Office 365에 업로드 하는 Azure AzCopy 도구를 실행 합니다.
    
- 이 절차에서는 선택 키를 포함 하는 URL의 복사본을 복사 하 고 저장 합니다. 이 정보는 2 단계에서 PST 파일을 업로드 하는 데 사용 되며, 3 단계에서는 Office 365에 업로드 된 PST 파일 목록을 확인 합니다. 암호나 기타 보안 관련 정보를 보호 하는 것 처럼이 URL을 보호 하는 예방 조치를 취해야 합니다. 예를 들어 암호로 보호 된 Microsoft Word 문서 또는 암호화 된 USB 드라이브에 파일을 저장할 수 있습니다. 이 결합 된 URL 및 키의 예는 [추가 정보](#more-information) 섹션을 참조 하십시오. 
    
- PST 파일을 Office 365의 비활성 사서함으로 가져올 수 있습니다. PST 가져오기 매핑 파일의 `Mailbox` 매개 변수에 비활성 사서함의 GUID를 지정 하 여이 작업을 수행 합니다. 자세한 내용은이 항목의 **지침** 탭에서 4 단계를 참조 하세요. 
    
- Exchange 하이브리드 배포에서는 기본 사서함이 온-프레미스 인 사용자에 대해 PST 파일을 클라우드 기반 보관 사서함으로 가져올 수 있습니다. PST 가져오기 매핑 파일에서 다음을 수행 하 여이 작업을 수행 합니다.
    
  - `Mailbox` 매개 변수의 사용자 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 합니다. 
    
  - `IsArchive` 매개 변수에 **TRUE** 값을 지정 합니다. 
    
    자세한 내용은 [4 단계](#step-4-create-the-pst-import-mapping-file) 를 참조 하세요. 
    
- PST 파일을 Office 365 사서함으로 가져온 후에는 사서함에 대 한 보존 설정이 무기한 유지 되도록 설정 됩니다. 즉, 보존 보류를 해제 하거나 보류를 해제 하기 위해 날짜를 설정할 때까지 사서함에 할당 된 보존 정책이 처리 되지 않습니다. 이 작업을 수행 하는 이유는 무엇 인가요? 사서함으로 가져온 메시지가 오래 된 경우 사서함에 대해 구성 된 보존 설정에 따라 보존 기간이 만료 되어 영구적으로 삭제 (제거) 될 수 있습니다. 사서함을 보존 상태로 두면 사서함 소유자가 새로 가져온 메시지를 관리할 수 있는 시간을 제공 하거나 사서함의 보존 설정을 변경할 수 있는 시간을 제공 합니다. 보존 유지 관리에 대 한 제안은이 항목의 **추가 정보** 탭을 참조 하세요. 
    
- 기본적으로 Office 365 사서함에서 받을 수 있는 최대 메시지 크기는 35 MB입니다. 사서함에 대 한 *MaxReceiveSize* 속성의 기본값은 35 MB로 설정 되어 있기 때문입니다. 그러나 Office 365의 최대 메시지 수신 크기 제한은 150 MB입니다. 따라서 35 보다 큰 항목을 포함 하는 PST 파일을 가져올 경우 Office 365 가져오기 서비스는 대상 사서함의 *MaxReceiveSize* 속성 값을 150 mb로 자동 변경 합니다. 이를 통해 최대 150 MB까지 메시지를 사용자 사서함으로 가져올 수 있습니다. 
    
    > [!TIP]
    > 사서함에 대 한 메시지 수신 크기를 확인 하려면 Exchange Online PowerShell에서이 명령을 실행 하면 `Get-Mailbox <user mailbox> | FL MaxReceiveSize`됩니다. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>1 단계: SAS URL을 복사 하 고 Azure AzCopy을 설치 합니다.

첫 번째 단계는 2 단계에서 Office 365에 PST 파일을 업로드 하는 데 사용할 수 있는 도구인 Azure AzCopy 도구를 다운로드 하 여 설치 하는 것입니다. 조직의 SAS URL도 복사 합니다. 이 URL은 조직에 대 한 Microsoft 클라우드의 Azure 저장소 위치 및 공유 액세스 서명 (SAS) 키에 대 한 네트워크 URL의 조합입니다. 이 키를 사용 하 여 Azure 저장소 위치에 PST 파일을 업로드 하는 데 필요한 권한을 제공 합니다. SAS URL을 보호 하기 위한 예방 조치를 취해야 합니다. 조직에서 고유 하며 2 단계에서 사용 됩니다.

> [!IMPORTANT]
> 네트워크 업로드 방법을 사용 하 여 PST 파일을 가져오려면 다음 절차의 6b 단계에서 다운로드할 수 있는 Azure AzCopy 버전을 사용 하는 것이 좋습니다.
  
1. 으로 이동 [https://protection.office.com](https://protection.office.com) 하 고 Office 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 보안 & 준수 센터의 왼쪽 창에서 **데이터 거 버 넌 스** \> **가져오기를**클릭 합니다.
    
    > [!NOTE]
    > 보안 & 준수 센터의 **가져오기** 페이지에 액세스 하기 위한 적절 한 사용 권한이 할당 되어야 합니다. 자세한 내용은 **시작 하기 전에** 섹션을 참조 하세요. 
    
3. **가져오기** ![페이지에서 아이콘](media/ITPro-EAC-AddIcon.gif) 추가 **새 가져오기 작업**을 클릭 합니다.
    
    작업 가져오기 마법사가 표시 됩니다.
    
4. PST 가져오기 작업의 이름을 입력 하 고 **다음**을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄을 사용 합니다. 이름에는 대문자를 사용 하거나 공백을 포함할 수 없습니다.
    
5. 데이터를 **업로드 하거나 배송** 하 시겠습니까? 페이지에서 **데이터 업로드** 를 클릭 한 후 **다음**을 클릭 합니다.
    
    ![네트워크 업로드 가져오기 작업을 만들려면 데이터 업로드를 클릭 합니다.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. **데이터 가져오기** 페이지에서 다음 두 가지 작업을 수행 합니다. 
    
    ![데이터 가져오기 페이지에서 SAS URL을 복사 하 고 Azure AzCopy 도구 다운로드](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    위한. 2 단계에서 **네트워크 업로드 SAS URL 표시**를 클릭 합니다. SAS URL이 표시 되 면 **클립보드에 복사** 를 클릭 하 여 붙여 넣은 다음 나중에 액세스할 수 있도록 파일에 저장 합니다.
    
    b. 3 단계에서 **Azure AzCopy 다운로드** 를 클릭 하 여 azure AzCopy 도구를 다운로드 하 고 설치 합니다. 팝업 창에서 **실행** 을 클릭 하 여 AzCopy을 설치 합니다. 
    
> [!NOTE]
> **데이터 가져오기** 페이지를 열어 둔 채로, 즉 SAS URL을 다시 복사 해야 할 경우에는 **취소** 를 클릭 하 여 닫아야 합니다. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>2 단계: Office 365에 PST 파일 업로드

이제 AzCopy 도구를 사용 하 여 PST 파일을 Office 365에 업로드할 수 있습니다. 이 도구는 Microsoft 클라우드의 Azure 저장소 위치에 업로드 하 고 저장 합니다. 앞에서 설명한 것 처럼 PST 파일을 업로드 하는 Azure 저장소 위치는 Office 365 조직이 있는 동일한 지역 Microsoft 데이터 센터에 저장 됩니다. 이 단계를 완료하려면 PST 파일이 조직의 파일 공유 또는 파일 서버에 있어야 합니다. 다음 절차에서는 이것을 원본 디렉터리라고 합니다. AzCopy 도구를 실행할 때마다 다른 원본 디렉터리를 지정할 수 있습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트를 엽니다.
    
2. 1단계에서 AzCopy.exe 도구를 설치한 디렉터리로 이동합니다. 기본 위치에 도구를 설치한 경우로 `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`이동 합니다.
    
3. 다음 명령을 실행 하 여 PST 파일을 Office 365에 업로드 합니다.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    > [!IMPORTANT] 
    > 디렉터리를 이전 명령에서 원본 위치로 지정 해야 합니다. 개별 PST 파일은 지정할 수 없습니다. 원본 디렉터리의 모든 PST 파일이 업로드 됩니다.
 
    다음 표에는 AzCopy 매개 변수와 해당 필수 값에 대 한 설명이 나와 있습니다. 이전 단계에서 얻은 정보는 이러한 매개 변수의 값에 사용 됩니다.
    
    |**매개 변수**|**설명**|**예제**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Office 365로 업로드 될 PST 파일이 들어 있는 조직의 원본 디렉터리를 지정 합니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |1 단계에서 구한 SAS URL을 지정 합니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> **팁:** 반드시 PST 파일을 업로드할 Azure 저장소 위치에 하위 폴더를 지정할 수 있습니다. 이 작업은 SAS URL에 하위 폴더 위치 ("ingestiondata")를 추가 하 여 수행 합니다. 첫 번째 예에서는 하위 폴더를 지정 하지 않습니다. 즉, Pst가 Azure 저장소 위치의 루트 ( *ingestiondata* )로 업로드 됩니다. 두 번째 예에서는 PST 파일을 Azure 저장소 위치의 루트에 있는 하위 폴더 ( *PSTFiles* )에 업로드 합니다.  <br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> 또는  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |자세한 상태 메시지를 로그 파일에 출력합니다. 기본적으로 자세한 로그 파일은 %LocalAppData%\Microsoft\Azure\AzCopy의 AzCopyVerbose.log로 지정됩니다. 이 옵션에 대한 기존 파일 위치를 지정하면 해당 파일에 자세한 로그 파일이 추가됩니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |이 선택적 스위치는 AzCopy 도구가 `/Source:` 매개 변수로 지정 된 원본 디렉터리의 하위 폴더에 있는 pst 파일을 복사 하도록 재귀 모드를 지정 합니다.  <br/> **참고:** 이 스위치를 포함 하는 경우 하위 폴더의 PST 파일은 업로드 된 후 Azure 저장소 위치에서 파일 경로 이름이 다릅니다. 4 단계에서 만든 CSV 파일의 정확한 파일 경로 이름을 지정 해야 합니다.  <br/> | `/S` <br/> |
    | `/Y` <br/> |이 필수 스위치를 사용 하면 Azure 저장소 위치에 PST 파일을 업로드할 때 쓰기 전용 SAS 토큰을 사용할 수 있습니다. 1 단계에서 구한 다음 `/Dest:` 매개 변수에 지정 된 sas url은 쓰기 전용 sas url 이므로이 스위치를 포함 해야 합니다. 쓰기 전용 SAS URL을 사용 하는 경우 azure 저장소 탐색기를 통해 Azure 저장소 위치로 업로드 되는 PST 파일의 목록을 볼 수 있습니다.  <br/> | `/Y` <br/> |
   
다음은 각 매개 변수에 대한 실제 값을 사용하는 AzCopy.exe 도구에 대한 구문 예입니다.
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

이 명령을 실행하면 PST 파일의 업로드 진행률을 보여 주는 상태 메시지가 표시됩니다. 마지막 상태 메시지에는 성공적으로 업로드된 파일의 총 수가 표시됩니다. 

> [!TIP]
> AzCopy 명령을 성공적으로 실행 하 여 모든 매개 변수가 올바른지 확인 한 후에는 1 단계에서 가져온 정보를 복사한 것과 동일한 (보안 된) 파일에 명령줄 구문의 복사본을 저장 합니다. 그런 다음 AzCopy 도구를 실행 하 여 PST 파일을 Office 365에 업로드 하려고 할 때마다 명령 프롬프트에이 명령을 복사 하 여 붙여 넣을 수 있습니다. `/Source:` 매개 변수에 대 한 값만 변경 해야 할 수 있습니다. 이 값은 PST 파일이 있는 원본 디렉터리에 따라 다릅니다.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>반드시 3 단계: Office 365에 업로드 된 PST 파일 목록 보기

선택적 단계로 Microsoft Azure Storage Explorer (무료 오픈 소스 도구)를 설치 하 고 사용 하 여 Azure blob에 업로드 한 PST 파일의 목록을 볼 수 있습니다. 이 작업을 수행하면 좋은 이유로는 다음 두 가지가 있습니다.
  
- 조직의 공유 폴더 또는 파일 서버에 있는 PST 파일이 Azure blob에 성공적으로 업로드 되었는지 확인 합니다.
    
- Azure blob에 업로드 된 각 PST 파일에 대해 파일 이름 (및 포함 된 경우 하위 폴더 경로 이름)이 있는지 확인 합니다. 다음 단계에서 PST 매핑 파일을 만들 때 각 PST 파일의 폴더 경로와 파일 이름을 모두 지정해야 하므로 이러한 정보를 유용하게 사용할 수 있습니다. 이러한 이름을 확인하면 PST 매핑 파일의 잠재적인 오류를 줄이는 데 도움이 될 수 있습니다.
    
Microsoft Azure Storage Explorer가 미리 보기에 있습니다.
  
> [!IMPORTANT]
> Azure 저장소 탐색기를 사용 하 여 PST 파일을 업로드 하거나 수정할 수 없습니다. PST 파일을 Office 365로 가져오는 유일한 방법은 AzCopy을 사용 하는 것입니다. 또한 Azure blob에 업로드 한 PST 파일은 삭제할 수 없습니다. PST 파일을 삭제 하려고 하면 필요한 사용 권한이 없다는 오류 메시지가 표시 됩니다. 모든 PST 파일이 Azure 저장소 영역에서 자동으로 삭제 됩니다. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created.
  
Azure 저장소 탐색기를 설치 하 고 Azure storage 영역에 연결 하려면 다음을 수행 합니다.
  
1. [Microsoft Azure 저장소 탐색기 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 다운로드 하 고 설치 합니다.
    
2. Microsoft Azure 저장소 탐색기를 시작 하 고 왼쪽 창에서 **저장소 계정을** 마우스 오른쪽 단추로 클릭 한 다음 **Azure Storage에 연결**을 클릭 합니다.
    
    ![저장소 계정을 마우스 오른쪽 단추로 클릭 한 다음 Azure Storage에 연결을 클릭 합니다.](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. **SAS (공유 액세스 서명) URI 또는 연결 문자열 사용** 을 클릭 하 고 **다음**을 클릭 합니다.
    
4. **SAS URI 사용**을 클릭 하 고 1 단계에서 얻은 sas URL을 **URI**아래의 상자에 붙여 넣은 후 **다음**을 클릭 합니다.
    
5. **연결 요약** 페이지에서 연결 정보를 검토 하 고 **연결**을 클릭할 수 있습니다.
    
    **Ingestiondata** 컨테이너가 열려 있습니다. 2 단계에서 업로드 한 PST 파일이 들어 있습니다. **Ingestiondata** 컨테이너는 **저장소 계정** \> **(SAS 연결 서비스)** \> **Blob 컨테이너**에 있습니다. 
    
    ![Azure 저장소 탐색기는 사용자가 업로드한 PST 파일 목록이 표시됩니다.](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Microsoft Azure 저장소 탐색기 사용을 마친 후 **ingestiondata**를 마우스 오른쪽 단추로 클릭 하 고 **분리** 를 클릭 하 여 Azure 저장소 영역에서 연결을 끊습니다. 그러지 않으면 다음 번에 연결할 때 오류가 발생합니다. 
    
    ![수집을 마우스 오른쪽 단추로 클릭하고 분리를 클릭하여 Azure 저장소 영역에서 연결 끊기](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>4 단계: PST 가져오기 매핑 파일 만들기

PST 파일을 Office 365 조 직의 Azure 저장 위치에 업로드 한 후에는 PST 파일을 가져올 사용자 사서함을 지정 하는 CSV (쉼표로 구분 된 값) 파일을 만듭니다. PST 가져오기 작업을 만들 때 다음 단계에서이 CSV 파일을 제출 합니다.
  
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
    CSV 파일의 첫 번째 행 또는 머리글 행은 PST 가져오기 서비스에서 PST 파일을 사용자 사서함으로 가져오는 데 사용하는 매개 변수를 나열합니다. 각 매개 변수 이름은 쉼표로 구분됩니다. 머리글 행 아래의 각 행은 PST 파일을 특정 사서함으로 가져오기 위한 매개 변수 값을 나타냅니다. 사용자 사서함에 가져올 각 PST 파일에 대해 하나의 행이 필요합니다. 매핑 파일의 자리 표시자 데이터를 실제 데이터로 바꾸어야 합니다.

   **참고:** SharePoint 매개 변수를 포함 하 여 머리글 행에서 어떤 항목도 변경 하지 마세요. PST 가져오기 프로세스 중에는 무시 됩니다. 

 3. 다음 표의 정보를 사용하여 CSV 파일을 필요한 정보로 채웁니다.


    |**매개 변수**|**설명**|**예제**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |데이터를 가져올 Office 365 서비스를 지정 합니다. PST 파일을 사용자 사서함으로 가져오려면을 사용 `Exchange`합니다.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |2 단계에서 PST 파일을 업로드 한 Azure 저장소 위치의 폴더 위치를 지정 합니다.  <br/> 2 단계에 있는 `/Dest:` 매개 변수의 SAS URL에 선택적 하위 폴더 이름을 포함 하지 않은 경우 CSV 파일에서이 매개 변수를 비워 둡니다. 하위 폴더 이름을 포함 하는 경우이 매개 변수에 지정 합니다 (두 번째 예제 참조). 이 매개 변수의 값은 대/소문자를 구분 합니다.  <br/> 두 방법 중 어느 것이 든 `FilePath` 매개 변수의 값에 "ingestiondata"를 포함 *하지 마십시오* .  <br/><br/> **중요:** 파일 경로 이름의 대/소문자는 2 단계의 `/Dest:` 매개 변수에 SAS URL에 선택적 하위 폴더 이름을 포함 한 경우에 사용한 사례와 같아야 합니다. 예를 들어 2 단계의 하위 `PSTFiles` 폴더 이름에 대해 CSV 파일의 `pstfiles` `FilePath` 매개 변수를 사용 하는 경우 PST 파일에 대 한 가져오기가 실패 합니다. 두 인스턴스에서 같은 대/소문자를 사용 해야 합니다.  <br/> |(공백으로 둠)  <br/> 또는  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |사용자 사서함으로 가져올 PST 파일의 이름을 지정합니다. 이 매개 변수의 값은 대/소문자를 구분 합니다.  <br/> <br/>**중요:** CSV 파일의 PST 파일 이름에 대 한 사례는 2 단계에서 Azure 저장소 위치로 업로드 된 PST 파일과 동일 해야 합니다. 예를 들어 CSV 파일의 `annb.pst` `Name` 매개 변수에서 사용 하는 경우 실제 PST 파일 `AnnB.pst`의 이름은 해당 pst 파일에 대 한 가져오기가 실패 합니다. CSV 파일의 PST 이름에 실제 PST 파일과 동일한 대/소문자가 사용 되는지 확인해 보십시오.  <br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |PST 파일을 가져올 사서함의 전자 메일 주소를 지정합니다.  PST 가져오기 서비스는 공용 폴더에 PST 파일 가져오기를 지원하지 않으므로 공용 폴더를 지정할 수 없습니다.  <br/> PST 파일을 비활성 사서함으로 가져오려면이 매개 변수의 사서함 GUID를 지정 해야 합니다. 이 GUID를 얻으려면 Exchange Online에서 다음 PowerShell 명령을 실행 합니다.`Get-Mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> <br/>**참고:** 경우에 따라 전자 메일 주소가 같은 여러 개의 사서함이 있고, 하나의 사서함이 활성 사서함이 고, 다른 사서함이 일시 삭제 (또는 비활성) 상태인 경우에만 가능 합니다. 이러한 상황에서는 PST 파일을 가져올 사서함을 고유 하 게 식별 하는 사서함 GUID를 지정 해야 합니다. 활성 사서함에 대해이 GUID를 가져오려면 다음 PowerShell 명령을 실행 `Get-Mailbox <identity of active mailbox> | FL Guid`합니다. 일시 삭제 된 (또는 비활성) 사서함의 GUID를 가져오려면이 명령을 `Get-Mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`실행 합니다.  <br/> | `annb@contoso.onmicrosoft.com` <br/> 또는  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | PST 파일을 사용자의 보관 사서함으로 가져올 것인지 여부를 지정합니다. 다음 두 가지 옵션이 있습니다.  <br/><br/>**FALSE** -PST 파일을 사용자의 기본 사서함으로 가져옵니다.  <br/> **TRUE** -PST 파일을 사용자의 보관 사서함으로 가져옵니다. This assumes that the [user's archive mailbox is enabled](enable-archive-mailboxes.md). <br/><br/>이 매개 변수를로 `TRUE` 설정 하 고 사용자의 보관 사서함을 사용할 수 없는 경우 해당 사용자에 대 한 가져오기가 실패 합니다. 해당 보관이 설정 되지 않고이 속성이로 `TRUE`설정 되어 있기 때문에 한 사용자에 대 한 가져오기가 실패 하면 가져오기 작업의 다른 사용자에 게 영향을 주지 않습니다.  <br/>  If you leave this parameter blank, the PST file is imported to the user's primary mailbox.  <br/> <br/>**참고:** 기본 사서함이 온-프레미스에 있는 사용자의 클라우드 기반 보관 사서함으로 PST 파일을 가져오려면이 매개 변수를 지정 `TRUE` 하 고 `Mailbox` 매개 변수의 사용자 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 하면 됩니다.  <br/> | `FALSE` <br/> 또는  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | PST 파일을 가져올 사서함 폴더를 지정 합니다.  <br/>  이 매개 변수를 비워 두면 PST를 사서함의 루트 수준 (받은 편지함 폴더 및 **** 다른 기본 사서함 폴더와 같은 수준)에 있는 새 폴더로 가져오게 됩니다.  <br/>  지정 `/`하는 경우 PST 파일의 항목을 사용자의 받은 편지함 폴더로 직접 가져옵니다.  <br/><br/>  지정 `/<foldername>`하는 경우 PST 파일의 항목을 * \<foldername\> * 이라는 폴더로 가져옵니다. 예를 들어를 사용 `/ImportedPst`하는 경우에는 항목을 **importedpst**라는 폴더로 가져옵니다. 이 폴더는 받은 편지함 폴더와 같은 수준에 있는 사용자의 사서함에 배치 됩니다.  <br/><br/> **팁:** Pst 파일을 가져올 가장 적합 한 폴더 위치를 결정할 수 있도록 몇 가지 테스트 일괄 처리를 실행 하 여이 매개 변수를 시험해 보십시오.  <br/> |(공백으로 둠)  <br/> 또는  <br/>  `/` <br/> 또는  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |이 선택적 매개 변수는 ANSI 파일 형식으로 PST 파일을 가져오는 데 사용할 코드 페이지의 숫자 값을 지정 합니다. 이 매개 변수는 일반적으로 문자 인코딩에 DBCS (더블 바이트 문자 집합)를 사용 하므로 중국어, 일본어 및 한국어 (CJK) 조직에서 PST 파일을 가져오는 데 사용 됩니다. 이 매개 변수를 사용 하 여 사서함 폴더 이름에 DBCS를 사용 하는 언어에 대 한 PST 파일을 가져오지 않으면 가져온 후 폴더 이름이 왜곡 되는 경우가 많습니다.  <br/><br/> 이 매개 변수에 사용할 지원 되는 값의 목록은 [코드 페이지 식별자](https://go.microsoft.com/fwlink/p/?LinkId=328514)를 참조 하십시오.  <br/> <br/>**참고:** 앞에서 설명한 것 처럼이 매개 변수는 선택적으로 사용할 수 있으며 CSV 파일에 포함 하지 않아도 됩니다. 또는 하나 이상의 행에 대해 값을 비워 두면 됩니다.  <br/> |(공백으로 둠)  <br/> 또는  <br/>  `932`(ANSI/OEM 일본어에 대 한 코드 페이지 식별자)  <br/> |
    | `SPFileContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPManifestContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPSiteUrl` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>5 단계: Office 365에서 PST 가져오기 작업 만들기

다음 단계에서는 Office 365의 가져오기 서비스에 PST 가져오기 작업을 만듭니다. 앞에서 설명한 것 처럼 4 단계에서 만든 PST 가져오기 매핑 파일을 제출 합니다. 새 작업을 만든 후에는 Office 365에서 PST 파일의 데이터를 분석 하 고, 실제로는 PST 가져오기 매핑 파일에 지정 된 사서함으로 가져온 데이터를 필터링 할 수 있는 기회를 제공 합니다 ( [6 단계](#step-6-filter-data-and-start-the-pst-import-job)참조).
  
1. 으로 이동 [https://protection.office.com](https://protection.office.com) 하 고 Office 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 보안 & 준수 센터의 왼쪽 창에서 **데이터 관리** 를 클릭 하 고 **가져오기를**클릭 합니다.
    
3. **가져오기** ![페이지에서 아이콘](media/ITPro-EAC-AddIcon.gif) 추가 **새 가져오기 작업**을 클릭 합니다.
    
    **참고:** 새 가져오기 작업을 만들려면 Security & 준수 센터의 **가져오기** 페이지에 액세스 하는 데 필요한 사용 권한을 할당 받아야 합니다. 자세한 내용은 **시작 하기 전에** 섹션을 참조 하세요. 
    
4. PST 가져오기 작업의 이름을 입력 하 고 **다음**을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄을 사용 합니다. 이름에는 대문자를 사용 하거나 공백을 포함할 수 없습니다.
    
5. 데이터를 **업로드 하거나 배송** 하 시겠습니까? 페이지에서 **데이터 업로드** 를 클릭 한 후 **다음**을 클릭 합니다.
    
    ![네트워크 업로드 가져오기 작업을 만들려면 데이터 업로드를 클릭 합니다.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. **데이터 가져오기** 페이지의 4 단계에서 **내 파일 업로드를 완료** 했으며, **매핑 파일에 액세스할 수 있음** 확인란을 클릭 한 후 **다음**을 클릭 합니다.
    
    ![4 단계에서 두 확인란을 클릭 합니다.](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. **매핑 파일 선택** 페이지에서 **매핑 파일 선택을** 클릭 하 여 4 단계에서 만든 PST 가져오기 매핑 파일을 제출 합니다. 
    
    ![매핑 파일 선택을 클릭 하 여 가져오기 작업을 위해 만든 CSV 파일을 제출 합니다.](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. CSV 파일 이름이 **매핑 파일 이름**아래에 표시 되 면 **유효성 검사** 를 클릭 하 여 csv 파일에 오류가 있는지 확인 합니다. 
    
    ![유효성 검사를 클릭 하 여 CSV 파일에서 오류를 확인 합니다.](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    PST 가져오기 작업을 만들려면 CSV 파일의 유효성 검사가 성공해야 합니다. 참고 유효성 검사가 성공적으로 완료 되 면 파일 이름이 녹색으로 변경 됩니다. 유효성 검사에 실패할 경우 **로그 보기** 링크를 클릭 합니다. 실패 한 파일의 각 행에 대 한 오류 메시지와 함께 유효성 검사 오류 보고서가 열립니다. 
    
9. PST 매핑 파일의 유효성 검사가 완료 되 면 사용 약관 문서를 읽고 해당 확인란을 클릭 합니다.
    
10. **저장** 을 클릭 하 여 작업을 제출 하 고 작업을 성공적으로 만든 후 **닫기를** 클릭 합니다. 
    
    상태 플라이 아웃 페이지가 표시 되 고, **분석 상태가 진행** 중 이며 새 가져오기 작업이 **가져오기** 페이지의 목록에 표시 됩니다. 
    
11. 새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침** ![을 클릭 하 여 **상태** 열에 표시 되는 상태 정보를 업데이트 합니다. 분석이 완료 되 고 데이터를 가져올 준비가 되 면 상태가 **분석 완료**로 변경 됩니다.
    
    가져오기 작업을 클릭 하 여 매핑 파일에 나열 된 각 PST 파일의 상태와 같은 가져오기 작업에 대 한 자세한 정보가 포함 된 상태 플라이 아웃 페이지를 표시할 수 있습니다.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>6 단계: 데이터 필터링 및 PST 가져오기 작업 시작

365 5 단계에서 가져오기 작업을 만든 후에는 항목의 보존 기간을 확인 하 고 pst 파일에 포함 된 다양 한 메시지 유형을 식별 하 여 pst 파일의 데이터를 안전 하 고 안전한 방식으로 분석 합니다. 분석이 완료 되 고 데이터를 가져올 준비가 되 면 PST 파일에 포함 된 모든 데이터를 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하 여 가져온 데이터를 트리밍하는 옵션을 사용할 수 있습니다.
  
1. 보안 & 준수 센터의 **가져오기** 페이지에서 준비를 클릭 하 여 5 단계에서 만든 가져오기 작업에 대 한 **Office 365로 가져옵니다** . 
    
    ![만든 가져오기 작업 옆에 있는 Office 365로 가져오려면 준비를 클릭 합니다.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    가져오기 작업에 대 한 기타 정보 및 PST 파일에 대 한 정보가 포함 된 플라이 아웃 페이지가 표시 됩니다.
    
2. 플라이 아웃 페이지에서 **Office 365로 가져오기를**클릭 합니다.
    
    **데이터 필터링** 페이지가 표시 됩니다. 여기에는 데이터의 기간에 대 한 정보를 포함 하 여 Office 365에서 PST 파일에 대해 수행 된 분석 결과의 데이터 insights가 포함 되어 있습니다. 이때 가져올 데이터를 필터링 하는 옵션과 모든 데이터를 그대로 가져올 수 있는 옵션이 있습니다. 
    
    ![PST 파일의 데이터를 트리밍하고 모두 가져올 수 있습니다.](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. 다음 중 하나를 수행합니다.
    
    위한. 가져오는 데이터를 트리밍하려면 **예, 가져오기 전에 필터링**합니다 .를 클릭 합니다.
    
    PST 파일의 데이터를 필터링 한 다음 가져오기 작업을 시작 하는 방법에 대 한 자세한 단계별 지침은 [pst 파일을 Office 365로 가져올 때 데이터 필터링](filter-data-when-importing-pst-files.md)을 참조 하십시오.
    
    또는
    
    b. PST 파일에 있는 모든 데이터를 가져오려면 **아니요, 모든 항목을 가져옵니다** .를 클릭 하 고 **다음**을 클릭 합니다.
    
4. 모든 데이터를 가져오도록 선택한 경우 **데이터 가져오기를** 클릭 하 여 가져오기 작업을 시작 합니다. 
    
    가져오기 작업의 상태가 **가져오기** 페이지에 표시 됩니다. 아이콘 ![](media/O365-MDM-Policy-RefreshIcon.gif) **새로** 고침 새로 고침을 클릭 하 여 **상태** 열에 표시 되는 상태 정보를 업데이트 합니다. 가져오기 작업을 클릭 하 여 가져올 각 PST 파일에 대 한 상태 정보를 표시 하는 상태 플라이 아웃 페이지를 표시 합니다. 

## <a name="how-the-import-process-works"></a>가져오기 프로세스의 작동 방식
  
네트워크 업로드 옵션 및 Office 365 가져오기 서비스를 사용 하 여 PST 파일을 사용자 사서함으로 대량 가져올 수 있습니다. 네트워크 업로드는 Microsoft 클라우드의 임시 저장소 영역에 PST 파일을 업로드 하는 것을 의미 합니다. 그런 다음 Office 365 가져오기 서비스가 저장소 영역의 PST 파일을 대상 사용자 사서함으로 복사 합니다.
  
다음은 PST 파일을 Office 365의 사서함에 가져오는 네트워크 업로드 프로세스에 대 한 설명입니다.
  
![PST 파일을 Office 365로 가져오기 위한 네트워크 업로드 프로세스의 워크플로](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Pst 가져오기 도구 및 키를 사설 Azure 저장소 위치로 다운로드** -Microsoft 클라우드의 azure 저장소 위치에 pst 파일을 업로드 하는 데 사용 되는 첫 번째 단계는 azure AzCopy 명령줄 도구와 액세스 키를 다운로드 하는 것입니다. 보안 & 준수 센터의 **가져오기** 페이지에서이를 가져옵니다. 키 (SA (보안 액세스 서명) 키 라고 함)는 개인 및 안전한 Azure 저장소 위치에 PST 파일을 업로드 하는 데 필요한 권한을 제공 합니다. 이 선택 키는 조직에서 고유 하며, Microsoft 클라우드로 업로드 된 후에 해당 PST 파일에 대 한 무단 액세스를 방지 하는 데 도움이 됩니다. PST 파일을 Office 365로 가져오는 경우 조직에서 별도의 Azure 구독을 사용할 필요가 없습니다. 
    
2. **Azure storage location에 pst 파일 업로드** -1 단계에서 다운로드 한 AzCopy 도구를 사용 하 여 pst 파일을 업로드 하 고 Office 365에서 동일한 지역 Microsoft 데이터 센터에 있는 Azure 저장소 위치에 저장 합니다. 조직이 있습니다. 이를 업로드 하려면 Office 365로 가져올 PST 파일이 조직의 파일 공유 또는 파일 서버에 있어야 합니다.
    
    Azure 저장소 위치로 업로드 된 후 PST 파일 목록을 확인 하기 위해 수행할 수 있는 단계는 선택적입니다.
    
3. **Pst 가져오기 매핑 파일 만들기** -pst 파일을 Azure 저장소 위치로 업로드 한 후에는 pst 파일을 가져올 사용자 사서함을 지정 하는 CSV (쉼표로 구분 된 값) 파일을 만들기 위해 pst 파일을 사용할 수 있는지 확인 합니다.  사용자의 기본 사서함 또는 해당 보관 사서함으로 가져옵니다. Office 365 가져오기 서비스에서는 CSV 파일의 정보를 사용 하 여 PST 파일을 가져옵니다.
    
4. **Pst 가져오기 작업 만들기** -다음 단계는 Security _AMP_ 준수 센터의 **가져오기** 페이지에서 pst 가져오기 작업을 만들고 이전 단계에서 만든 pst 가져오기 매핑 파일을 제출 하는 것입니다. 가져오기 작업을 만든 후에는 Office 365에서 PST 파일의 데이터를 분석 한 다음 PST 가져오기 매핑 파일에 지정 된 사서함으로 실제로 가져오는 데이터를 제어 하는 필터를 설정할 수 있습니다. 
    
5. **사서함으로 가져올 PST 데이터 필터링** -가져오기 작업을 만들고 시작한 후에 Office 365에서 항목의 보존 기간 및 pst 파일에 포함 된 다양 한 메시지 유형을 식별 하 여 pst 파일의 데이터를 분석 합니다. . 분석이 완료 되 고 데이터를 가져올 준비가 되 면 PST 파일에 포함 된 모든 데이터를 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하 여 가져온 데이터를 트리밍하는 옵션을 사용할 수 있습니다.
    
6. **Pst 가져오기 작업 시작** -가져오기 작업을 시작한 후에 Office 365은 pst 가져오기 매핑 파일의 정보를 사용 하 여 Azure 저장소 위치에서 사용자 사서함으로 pst 파일을 가져옵니다. 가져오기 작업에 대 한 상태 정보 (가져올 각 PST 파일에 대 한 정보 포함)가 Security & 준수 센터의 **가져오기** 페이지에 표시 됩니다. 가져오기 작업이 완료 되 면 작업 상태가 **완료**로 설정 됩니다.
  
## <a name="more-information"></a>추가 정보

- PST 파일을 Office 365로 가져오는 이유는 무엇 인가요?
    
  - 조직의 보관 메시징 데이터를 Office 365로 가져오는 것이 좋은 방법입니다.
    
  - 이러한 데이터는 클라우드에 저장되므로 모든 장치에서 사용할 수 있습니다.
    
  - 가져온 PST 파일의 데이터에 Office 365 준수 기능을 적용 하 여 조직의 준수 요구 사항을 해결 하는 데 도움이 됩니다. 성능 저하를 줄여주는 방법에는 다음이 포함됩니다.
    
  - [보관 사서함](enable-archive-mailboxes.md) 및 [자동 확장 보관](enable-unlimited-archiving.md) 을 사용 하도록 설정 하 여 사용자에 게 가져온 데이터를 저장 하기 위한 추가 사서함 저장 공간을 제공 합니다. 
    
  - 가져온 데이터를 보존 하기 위해 사서함을 [소송 보존 상태로](https://go.microsoft.com/fwlink/?linkid=856286) 둡니다. 
    
  - Microsoft [eDiscovery 도구](search-for-content.md) 를 사용 하 여 가져온 데이터를 검색 합니다. 
    
  - [Office 365 보존 정책을](retention-policies.md) 사용 하 여 가져온 데이터가 보존 되는 기간을 제어 하 고 보존 기간이 만료 된 후에 수행할 작업을 제어할 수 있습니다. 
    
  - 가져온 데이터에 영향을 주는 사서함 관련 이벤트에 대 한 [Office 365 감사 로그](search-the-audit-log-in-security-and-compliance.md) 를 검색 합니다. 
    
  - 규정 준수를 위해 데이터를 보관 하기 위해 [비활성 사서함](create-and-manage-inactive-mailboxes.md) 으로 데이터 가져오기 
    
  - [데이터 손실 방지 정책을](data-loss-prevention-policies.md) 사용 하 여 조직 외부에서 중요 한 데이터가 누출 되지 않도록 합니다. 
  
- 다음은 1 단계에서 구한 SAS (공유 액세스 서명) URL의 예입니다. 또한이 예제에는 AzCopy 도구에서 실행 하 여 PST 파일을 Office 365에 업로드 하는 명령에 대 한 구문도 포함 되어 있습니다. 암호나 기타 보안 관련 정보를 보호 하는 것 처럼 SAS URL을 보호 하기 위한 예방 조치를 취해야 합니다.

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
    
   - You can configure the retention hold so that it's turned off on some date in the future. You do this by running the **Set-Mailbox -EndDateForRetentionHold *date*** command. For example, assuming that today's date is June 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  **Set-Mailbox -EndDateForRetentionHold 7/1/2016**. In this scenario, you would leave the  **RetentionHoldEnabled**  property set to  *True*. For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
   - You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    
