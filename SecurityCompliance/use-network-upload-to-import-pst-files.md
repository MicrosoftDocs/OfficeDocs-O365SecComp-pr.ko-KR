---
title: 네트워크 업로드를 사용하여 조직의 PST 파일을 Office 365로 가져오기
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: '관리자: 네트워크 업로드를 사용하여 Office 365의 사용자 사서함으로 여러 PST 파일을 대량으로 가져오는 방법에 대해 알아봅니다.'
ms.openlocfilehash: bd15216df69e003a5aaddb2ec21ede4da5c5c312
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854822"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>네트워크 업로드를 사용하여 조직의 PST 파일을 Office 365로 가져오기

> [!NOTE]
> 이 문서는 관리자를 위해 작성되었습니다. PST 파일을 사서함으로 가져오려고 하나요? [Outlook .pst 파일에서 전자 메일, 연락처 및 일정 가져오기](https://go.microsoft.com/fwlink/p/?LinkID=785075)를 참조하세요.
  
다음은 네트워크 업로드를 사용하여 여러 PST 파일을 Office 365 사서함에 대량으로 가져오는 데 필요한 단계별 지침입니다. 네트워크 업로드를 사용하여 PST 파일을 Office 365 사서함으로 대량 가져오기에 대한 자주 묻는 질문과 대답은 [네트워크 업로드를 사용하여 PST 파일 가져오기에 대한 FAQ](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files)를 참조하세요.
  
[1단계 : SAS URL을 복사하고 Azure AzCopy 설치](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[2단계: Office 365에 PST 파일 업로드](#step-2-upload-your-pst-files-to-office-365)

[(옵션) 3단계: Office 365로 업로드된 PST 파일 목록 보기](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[4단계: PST 가져오기 매핑 파일 만들기](#step-4-create-the-pst-import-mapping-file)

[5단계: Office 365에서 PST 가져오기 작업 만들기](#step-5-create-a-pst-import-job-in-office-365)

[6단계: 데이터 필터링 및 PST 가져오기 작업 시작](#step-6-filter-data-and-start-the-pst-import-job)

Office 365 사서함으로 PST 파일을 가져오려면 1단계를 한 번만 수행 하면 됩니다. 이러한 단계를 수행한 후 PST 파일 배치를 업로드하고 가져오고 싶을 때마다 2~6단계를 수행합니다.

## <a name="before-you-begin"></a>시작하기 전에
  
- PST 파일을 Office 365 사서함으로 가져오려면 Exchange Online에서 사서함 가져오기/내보내기 역할을 할당받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떤 역할 그룹에도 할당되지 않습니다. 조직 관리 역할 그룹에 사서함 가져오기/내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들고, 사서함 가져오기/내보내기 역할을 할당한 다음 자기 자신을 구성원으로 추가할 수 있습니다. 자세한 내용은 [역할 그룹 관리](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 “역할 그룹에 역할 추가” 또는 “역할 그룹 만들기” 섹션을 참조하세요.
    
    또한 보안 & 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족되어야 합니다.
    
  - Exchange Online에서 메일 받는 사람 역할을 할당받아야 합니다. 기본적으로 이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당됩니다.
    
    또는
    
  - Office 365 조직의 전역 관리자여야 합니다.
    
  > [!TIP]
    > Exchange Online에서 PST 파일을 Office 365로 가져오기 위한 새로운 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한만 할당하려면 새 역할 그룹에 사서함 가져오기/내보내기 역할 및 메일 받는 사람 역할을 할당하고 구성원을 추가합니다. 
  
- PST 파일을 Office 365로 가져오는 데 사용할 수 있는 유일한 방법은 이 항목에 설명된 대로 Azure AzCopy 도구를 사용하는 것입니다. Azure 저장소 탐색기를 사용하여 PST 파일을 Azure 저장소 영역에 직접 업로드할 수 없습니다.
    
- 조직의 파일 서버에 있는 Office 365 또는 공유 폴더에 가져오려는 PST 파일을 저장해야 합니다. 2단계에서 이 파일 서버 또는 공유 폴더에 저장된 PST 파일을 Office 365로 업로드하는 Azure AzCopy 도구를 실행합니다.
    
- 이 절차에서는 선택키가 포함 된 URL의 복사와 저장이 진행됩니다. 이 정보는 2단계에서 PST 파일을 업로드하고 3단계에서 Office 365에 업로드 된 PST 파일 목록을 보는 데 사용됩니다. 암호나 기타 보안 관련 정보를 보호하는 것처럼 특히 주의해서 이 URL을 보호해야 합니다. 예를 들어 암호로 보호된 Microsoft Word 문서나 암호화된 USB 드라이브에 저장할 수 있습니다. 이러한 결합된 키와 URL의 예제를 보려면 [자세한 정보](#more-information) 섹션을 참조하세요. 
    
- Office 365의 비활성 사서함으로 PST 파일을 가져올 수 있습니다. PST 가져오기 매핑 파일의 `Mailbox` 매개 변수에 비활성 사서함의 GUID를 지정하여 이 작업을 수행합니다. 자세한 내용은 이 항목의 **지침**탭에 있는 4 단계를 참조하세요. 
    
- Exchange 하이브리드 배포에서는 기본 사서함이 온-프레미스인 사용자의 PST 파일을 클라우드 기반 보관 사서함으로 가져올 수 있습니다. PST 가져오기 매핑 파일에서 다음을 수행하여 이 작업을 수행합니다.
    
  - 사용자의 온-프레미스 사서함에 대한 전자 메일 주소를 `Mailbox`매개 변수에 지정합니다. 
    
  - `IsArchive`매개 변수에 **TRUE** 값을 지정합니다. 
    
    자세한 내용은 [4단계](#step-4-create-the-pst-import-mapping-file)를 참조하세요. 
    
- PST 파일을 Office 365 사서함으로 가져온 후에는 사서함의 보존 유지 설정이 무기한으로 설정됩니다. 즉, 보존 유지를 끄거나 날짜를 설정하여 보존을 해제할 때까지 사서함에 할당된 보존 정책은 처리되지 않습니다. 이렇게 하는 이유가 무엇인가요? 사서함으로 가져온 메시지가 오래된 경우 사서함에 대해 구성된 보존 설정에 따라 보존 기간이 만료되어 영구적으로 삭제 (제거) 될 수 있습니다. 사서함을 보존 상태로 두면 사서함 소유자가 새로 가져온 메시지를 관리 할 수 있는 시간을 제공하거나 사서함의 보존 설정을 변경할 시간을 제공합니다. 보존 유지 관리에 대한 제안 사항은 이 항목의 **추가 정보** 탭을 참조하세요. 
    
- 기본적으로 Office 365 사서함에서 받을 수 있는 최대 메시지 크기는 35MB입니다. 이는 사서함의 *MaxReceiveSize* 속성 기본값이 35MB로 설정되어 있기 때문입니다. 그러나 Office 365의 최대 메시지 수신 크기 제한은 150MB입니다. 따라서 35MB보다 큰 항목이 포함된 PST 파일을 가져오는 경우 Office 365 가져오기 서비스는 대상 사서함의 *MaxReceiveSize* 속성 값을 150MB로 자동 변경합니다. 이를 통해 최대 150MB의 메시지를 사용자 사서함으로 가져올 수 있습니다. 
    
    > [!TIP]
    > 사서함의 메시지 수신 크기를 확인하려면 Exchange Online PowerShell `Get-Mailbox <user mailbox> | FL MaxReceiveSize`에서 이 명령을 실행합니다. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>1단계 : SAS URL을 복사하고 Azure AzCopy 설치

첫 번째 단계는 2단계에서 PST 파일을 Office 365에 업로드하기 위해 실행할 도구인 Azure AzCopy 도구를 다운로드하여 설치하는 것입니다. 조직의 SAS URL도 복사합니다. 이 URL은 조직의 Microsoft 클라우드에서 Azure 저장소 위치에 대한 네트워크 URL과 SAS (공유 액세스 서명) 키의 조합입니다. 이 키는 PST 파일을 Azure 저장소 위치에 업로드하는 데 필요한 권한을 제공합니다. SAS URL을 보호하기 위해 예방 조치를 취하세요. 이는 조직마다 고유하며 2단계에서 사용됩니다.

> [!IMPORTANT]
> 네트워크 업로드 방법을 사용하여 PST 파일을 가져오려면 다음 절차의 6b단계에서 다운로드 가능한 Azure AzCopy 버전을 사용하는 것이 좋습니다.
  
1. Office 365 조직의 관리자 계정 자격 증명을 사용하여 [https://protection.office.com](https://protection.office.com)으로 이동하고 로그인합니다. 
    
2. 보안 및 규정 준수 센터의 왼쪽 창에서 **데이터 관리** \> **가져오기**를 클릭합니다.
    
    > [!NOTE]
    > 보안 및 준수 센터에서 **가져오기** 페이지에 액세스하려면 적절한 권한을 할당받아야 합니다. 자세한 내용은 **시작하기 전에** 섹션을 참조하세요. 
    
3. **가져오기** 페이지에서 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새 가져오기 작업**을 클릭합니다.
    
    가져오기 작업 마법사가 표시됩니다.
    
4. PST 가져오기 작업의 이름을 입력하고 **다음**을 클릭합니다. 소문자, 숫자, 하이픈 및 밑줄을 사용하세요. 이름에는 대문자를 사용하거나 공백을 포함할 수 없습니다.
    
5. **데이터를 업로드하거나 배송 하시겠습니까?** 페이지에서 **데이터 업로드**를 클릭한 후 **다음**을 클릭합니다.
    
    ![데이터 업로드를 클릭하여 네트워크 업로드 가져오기 작업을 작성하세요.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. **데이터 가져오기** 페이지에서 다음 두 가지를 수행합니다. 
    
    ![데이터 가져오기 페이지에서 SAS URL을 복사하고 Azure AzCopy 도구를 다운로드합니다.](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a. 2단계에서 **네트워크 업로드 SAS URL 표시**를 클릭합니다. SAS URL이 표시되면 **클립보드에 복사**를 클릭하고 붙여넣기한 다음 나중에 액세스할 수 있도록 파일에 저장합니다.
    
    b. 3단계에서 **Azure AzCopy 다운로드**를 클릭하여 Azure AzCopy 도구를 다운로드하고 설치합니다. 팝업 창에서 **실행**을 클릭하여 AzCopy를 설치합니다. 
    
> [!NOTE]
> **데이터 가져오기** 페이지를 열어 두거나 (SAS URL을 다시 복사해야하는 경우 대비) 또는 **취소**를 클릭하여 페이지를 닫을 수 있습니다. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>2단계: Office 365에 PST 파일 업로드

이제 AzCopy.exe 도구를 사용하여 PST 파일을 Office365에 업로드할 수 있습니다. 이 도구는 Microsoft 클라우드의 Azure 저장소 위치에 이 파일을 업로드하고 저장합니다. 앞서 설명한 것처럼 PST 파일을 업로드 하는 Azure 저장소 위치는 Office 365 조직이 있는 동일한 지역 Microsoft 데이터 센터에 있습니다. 이 단계를 완료하려면 PST 파일이 조직의 파일 공유 또는 파일 서버에 있어야 합니다. 다음 절차에서는 이것을 원본 디렉터리라고 합니다. AzCopy 도구를 실행할 때마다 다른 원본 디렉터리를 지정할 수 있습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트를 엽니다.
    
2. 1단계에서 AzCopy.exe 도구를 설치한 디렉터리로 이동합니다. 기본 위치에 도구를 설치한 경우 `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`로 이동합니다.
    
3. 다음 명령을 실행하여 PST 파일을 Office 365로 업로드합니다.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    > [!IMPORTANT] 
    > 이전 명령에서 원본 위치로 디렉터리를 지정해야 합니다. 개별 PST 파일은 지정할 수 없습니다. 원본 디렉터리에 있는 모든 PST 파일이 업로드 됩니다.
 
    다음 표에서는 AzCopy.exe 매개 변수와 해당 필수 값에 대해 설명합니다. 이전 단계에서 획득한 정보가 이러한 매개 변수의 값에 사용됩니다.
    
    |**매개 변수**|**설명**|**예**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |조직에서 Office 365로 업로드될 PST 파일이 들어 있는 원본 디렉터리를 지정합니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |1단계에서 획득한 SAS URL을 지정합니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> **팁**: (선택 사항) Azure 저장소 위치에서 하위 폴더를 지정하여 PST 파일을 업로드 할 수 있습니다. SAS URL에서 하위 폴더 위치 ( "ingestiondata" 뒤에)를 추가하면 됩니다. 첫 번째 예제에서는 하위 폴더를 지정하지 않습니다. 즉, PST가 Azure 저장소 위치의 루트 (*ingestiondata*)에 업로드 됩니다. 두 번째 예제에서는 PST 파일을 Azure 저장소 위치의 루트에 있는 하위 폴더 (*PSTFiles*)로 업로드 합니다.  <br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> 또는  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |자세한 상태 메시지를 로그 파일에 출력합니다. 기본적으로 자세한 로그 파일은 %LocalAppData%\Microsoft\Azure\AzCopy의 AzCopyVerbose.log로 지정됩니다. 이 옵션에 대한 기존 파일 위치를 지정하면 해당 파일에 자세한 로그 파일이 추가됩니다.  <br/> 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |이 선택적 스위치는 AzCopy 도구가 `/Source:` 매개 변수로 지정된 원본 디렉터리의 하위 폴더에 있는 PST 파일을 복사하도록 반복 모드를 지정합니다.  <br/> **참고:** 이 스위치를 포함하면 하위 폴더의 PST 파일은 업로드된 후에 Azure 저장 위치에서 다른 파일 경로 이름을 갖게 됩니다. 4단계에서 만드는 CSV 파일의 정확한 파일 경로 이름을 지정해야 합니다.  <br/> | `/S` <br/> |
    | `/Y` <br/> |이 필수 스위치를 사용하면 PST 파일을 Azure 저장소 위치에 업로드 할 때 쓰기 전용 SAS 토큰을 사용할 수 있습니다. 1 단계 (및 `/Dest:` 매개 변수에서 지정된)에서 획득한 SAS URL은 쓰기 전용 SAS URL이므로 이 스위치를 포함시켜야 합니다. 쓰기 전용 SAS URL을 사용하면 Azure 저장소 탐색기를 사용하여 Azure 저장소 위치에 업로드 된 PST 파일 목록을 볼 수 있습니다.  <br/> | `/Y` <br/> |
   
다음은 각 매개 변수에 대한 실제 값을 사용하는 AzCopy.exe 도구에 대한 구문 예입니다.
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

이 명령을 실행하면 PST 파일의 업로드 진행률을 보여 주는 상태 메시지가 표시됩니다. 마지막 상태 메시지에는 성공적으로 업로드된 파일의 총 수가 표시됩니다.

> [!TIP]
> AzCopy.exe 명령을 성공적으로 실행하고 모든 매개 변수가 올바른지 확인한 후에는 명령줄 구문 복사본을 1단계에서 획득한 정보를 복사한 것과 동일한(보안) 파일에 저장합니다. 그런 후 AzCopy.exe 도구를 실행하여 PST 파일을 Office 365에 업로드하려고 할 때마다 명령 프롬프트에서 이 명령을 복사한 후 붙여넣을 수 있습니다. 변경해야 하는 유일한 값은 `/Source:` 매개 변수에 대한 값뿐입니다. 이 값은 PST 파일이 있는 원본 디렉터리에 따라 다릅니다.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(옵션) 3단계: Office 365로 업로드된 PST 파일 목록 보기

선택적 단계로, Microsoft Azure 저장소 탐색기(무료 오픈 소스 도구)를 설치한 후 Azure blob에 업로드한 PST 파일 목록을 확인할 수 있습니다. 이 작업을 수행하면 좋은 이유로는 다음 두 가지가 있습니다.
  
- 조직의 공유 폴더 또는 파일 서버의 PST 파일이 Azure blob에 성공적으로 업로드되었는지 확인합니다.
    
- Azure blob에 업로드된 각 PST 파일의 파일 이름(및 하위 폴더 경로 이름이 포함된 경우 해당 이름)을 확인합니다. 다음 단계에서 PST 매핑 파일을 만들 때 각 PST 파일의 폴더 경로와 파일 이름을 모두 지정해야 하므로 이러한 정보를 유용하게 사용할 수 있습니다. 이러한 이름을 확인하면 PST 매핑 파일의 잠재적인 오류를 줄이는 데 도움이 될 수 있습니다.
    
Microsoft Azure 저장소 탐색기는 Preview에 있습니다. 
  
> [!IMPORTANT]
> PST 파일을 업로드하거나 수정하는 데 Azure 저장소 탐색기를 사용할 수 없습니다. PST 파일을 Office 365로 가져오는 유일한 지원 방법은 AzCopy를 사용하는 것입니다. 또한 Azure Blob에 업로드한 PST 파일을 삭제할 수 없습니다. PST 파일을 삭제하려고 하면 필요한 권한이 없다고 설명하는 오류가 표시됩니다. 모든 PST 파일이 Azure Storage 영역에서 자동으로 삭제되는 것이 정상입니다. 가져오기 작업이 진행 중이 아니라면 ** ingestiondata** 컨테이너에 포함된 모든 PST 파일이 가장 최근에 가져오기 작업이 생성된 날짜로부터 30일 후에 삭제됩니다.
  
Azure 저장소 탐색기를 설치하고 Azure 저장 영역에 연결하려면
  
1. [ Microsoft Azure 저장소 탐색기 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 다운로드 및 설치합니다.
    
2. Microsoft Azure 저장소 탐색기를 시작하고 왼쪽 창에서 **저장소 계정**을 마우스 오른쪽 단추로 클릭한 다음 **Azure 저장소에 연결**을 클릭합니다.
    
    ![저장소 계정을 마우스 오른쪽 단추로 클릭한 다음 Azure 저장소에 연결을 클릭합니다.](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. **SAS (공유 액세스 서명) URI 또는 연결 문자열 사용**을 클릭하고 **다음**을 클릭합니다.
    
4. **SAS URI 사용**을 클릭하고 1단계에서 획득한 SAS URL을 **URI** 아래의 상자에 붙여넣은 후 **다음**을 클릭합니다.
    
5. **연결 요약** 페이지에서 연결 정보를 검토한 후 **연결**을 클릭 할 수 있습니다.
    
    **ingestiondata** 컨테이너가 열립니다. 여기에는 2단계에서 업로드한 PST 파일이 포함됩니다. **ingestiondata** 컨테이너는 **저장소 계정**\> ** (SAS 연결 서비스)**\>** Blob 컨테이너** 아래에 있습니다. 
    
    ![Azure 저장소 탐색기는 사용자가 업로드한 PST 파일 목록이 표시됩니다.](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Microsoft Azure 저장소 탐색기 사용을 마치면 **ingestiondata**를 마우스 오른쪽 단추로 클릭한 다음 **분리**를 클릭하여 Azure 저장 영역 연결에서 연결을 끊습니다. 그렇지 않으면 다음 번 연결할 때 오류가 발생합니다. 
    
    ![ingestion을 마우스 오른쪽 단추로 클릭하고 분리를 클릭하여 Azure 저장소 영역에서 연결 끊기](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>4단계: PST 가져오기 매핑 파일 만들기

PST 파일을 Office 365 조직의 Azure 저장소 위치에 업로드한 후에는 PST 파일을 가져올 사용자 사서함을 지정하는 쉼표로 구분된 값(CSV) 파일을 만들어야 합니다. PST 가져오기 작업을 만드는 다음 단계에서 이 CSV 파일을 제출합니다.
  
1. [PST 가져오기 매핑 파일의 사본을 다운로드](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
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

   **참조:** SharePoint 매개 변수를 포함하여 머리글 행의 어떤 내용도 변경하지 않도록 합니다. 변경한 내용은 PST 가져오기 프로세스 동안 무시됩니다. 

 3. 다음 표의 정보를 사용하여 CSV 파일을 필요한 정보로 채웁니다.


    |**매개 변수**|**설명**|**예**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |데이터를 가져올 Office 365 서비스를 지정합니다. PST 파일을 사용자 사서함으로 가져오려면 `Exchange`를 사용합니다.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |2단계에서 PST 파일을 업로드한 Azure 저장소 위치의 폴더 위치를 지정합니다.   <br/> 2단계의 `/Dest:` 매개 변수에서 SAS URL에 선택적 하위 폴더 이름을 포함하지 않은 경우 CSV 파일에서 이 매개 변수를 비워 둡니다. 하위 폴더 이름을 포함한 경우 이 매개 변수에 이름을 지정합니다 (두 번째 예제 참조). 이 매개 변수의 값은 대/소문자를 구분합니다.  <br/> 어느 쪽이든 `FilePath` 매개 변수 값에 "ingestiondata"를 포함하지 *마세요*.  <br/><br/> **중요:** 2단계의 `/Dest:` 매개 변수에서 SAS URL에 선택적 하위 폴더 이름을 포함한 경우에는 파일 경로 이름의 대/소문자가 사용자의 경우와 동일해야 합니다. 예를 들어 2단계에서 `PSTFiles`로 하위 폴더 이름을 사용한 다음 CSV 파일의 `FilePath` 매개 변수에서 `pstfiles`를 사용한 경우에는 PST 파일 가져오기가 실패하게 됩니다. 두 가지 경우 모두 같은 대/소문자를 사용해야 합니다.  <br/> |(공백으로 둠)  <br/> 또는  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |사용자 사서함으로 가져올 PST 파일의 이름을 지정합니다. 이 매개 변수의 값은 대/소문자를 구분합니다.  <br/> <br/>**중요:** CSV 파일의 PST 파일 이름의 대/소문자는 2단계에서 Azure 저장소 위치에 업로드 된 PST 파일과 동일해야 합니다. 예를 들어 CSV 파일의 `Name` 매개 변수에서 `annb.pst`을 사용했지만 실제 PST 파일의 이름은 `AnnB.pst`인 경우 해당 PST 파일의 가져오기가 실패합니다. CSV 파일의 PST 이름은 실제 PST 파일과 동일한 대/소문자를 사용해야 합니다.  <br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |PST 파일을 가져올 사서함의 전자 메일 주소를 지정합니다. PST 가져오기 서비스는 공용 폴더에 PST 파일 가져오기를 지원하지 않으므로 공용 폴더를 지정할 수 없습니다.  <br/> PST 파일을 비활성 사서함으로 가져오려면 이 매개 변수의 사서함 GUID를 지정해야 합니다. 이 GUID를 얻으려면 Exchange Online에서 다음 PowerShell 명령을 실행합니다. `Get-Mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> <br/>**참고:** 경우에 따라 한 사서함은 활성 사서함이고 다른 사서함은 일시 삭제된 (또는 비활성) 상태인 경우, 동일한 전자 메일 주소에 여러 사서함이 있을 수 있습니다.  이러한 상황에서는 PST 파일을 가져올 사서함을 고유하게 식별하기 위해 사서함 GUID를 지정해야 합니다. 활성 사서함에 대한 GUID를 얻으려면 다음 PowerShell 명령을 실행합니다. `Get-Mailbox <identity of active mailbox> | FL Guid` 일시 삭제된 (또는 비활성) 사서함에 대한 GUID를 얻으려면 이 명령을 실행합니다. `Get-Mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`  <br/> | `annb@contoso.onmicrosoft.com` <br/> 또는  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | PST 파일을 사용자의 보관 사서함으로 가져올 것인지 여부를 지정합니다. 다음 두 가지 옵션이 있습니다.  <br/><br/>**FALSE** - PST 파일을 사용자의 기본 사서함으로 가져옵니다.  <br/> **TRUE** - PST 파일을 사용자의 보관 사서함으로 가져옵니다. [사용자의 보관 사서함이 활성화](enable-archive-mailboxes.md)되어 있다고 가정합니다. <br/><br/>사용자의 보관 사서함이 활성화되지 않은 상태에서 이 매개 변수를 `TRUE`로 설정하면 해당 사용자의 가져오기가 실패합니다. (보관 사서함이 활성화되지 않은 상태에서 매개 변수를 `TRUE`로 설정하여) 어느 한 사용자의 가져오기가 실패하더라도 다른 사용자의 가져오기 작업에는 영향을 주지 않습니다.  <br/>  매개 변수를 공란으로 두면 PST 파일을 사용자의 기본 사서함으로 가져옵니다.  <br/> <br/>**참고:** 기본 사서함이 온-프레미스에 존재하는 사용자에 대해 PST 파일을 클라우드 기반 보관 사서함으로 가져오려면 이 매개 변수를 `TRUE`로 설정하고 `Mailbox` 매개 변수에 대해 사용자의 온-프레미스 사서함의 전자 메일 주소를 지정합니다.  <br/> | `FALSE` <br/> 또는  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | PST 파일을 가져올 사서함 폴더를 지정합니다.  <br/>  이 매개 변수를 비워 두면 PST는 사서함의 루트 수준(받은 편지함 폴더 및 기타 기본 사서함 폴더와 같은 수준)에 있는 **가져온 파일**이라는 새 폴더로 가져오게 됩니다.  <br/>  `/`을 지정할 경우 PST 파일의 항목을 사용자의 받은 편지함 폴더로 직접 가져오게 됩니다.  <br/><br/>  `/<foldername>`을 지정할 경우 PST 파일의 항목을 *\<foldername\>* 이라는 폴더로 가져오게 됩니다. 예를 들어 을 사용하는 경우 항목을 **importedPst**라는 폴더로 가져오게 됩니다. 이 폴더는 받은 편지함 폴더와 같은 수준의 사용자 사서함에 있습니다.  <br/><br/> **팁:** PST 파일을 가져올 가장 적합한 폴더 위치를 결정할 수 있도록 몇 가지 테스트 배치를 실행하면서 이 매개 변수를 실험해볼 수 있습니다.   <br/> |(공백으로 둠)  <br/> 또는  <br/>  `/` <br/> 또는  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |이 선택적 매개 변수는 ANSI 파일 형식으로 PST 파일을 가져오는 데 사용할 코드 페이지의 숫자 값을 지정합니다. 이 매개 변수는 중국어, 일본어 및 한국어 (CJK) 조직에서 PST 파일을 가져오는 데 사용됩니다. 이러한 언어는 일반적으로 문자 인코딩에 2 바이트 문자 세트 (DBCS)를 사용하기 때문입니다. 사서함 폴더 이름으로 DBCS를 사용하는 언어의 PST 파일을 가져오는 데 이 매개 변수를 사용하지 않으면, 가져온 후에 폴더 이름이 왜곡되는 경우가 많습니다.  <br/><br/> 이 매개 변수를 사용하는 데 지원되는 값의 목록은 [코드 페이지 식별자](https://go.microsoft.com/fwlink/p/?LinkId=328514)를 참조하세요.  <br/> <br/>**참고:** 앞서 설명한 것처럼 이것은 선택적 매개 변수이며 CSV 파일에 포함하지 않아도 됩니다. 또는 포함하고 하나 이상의 행에 대해 값을 비워둘 수 있습니다.  <br/> |(공백으로 둠)  <br/> 또는  <br/>  `932` (ANSI/OEM 일본어에 대한 코드 페이지 식별자)  <br/> |
    | `SPFileContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.  <br/> |해당 없음  <br/> |
    | `SPManifestContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.  <br/> |해당 없음  <br/> |
    | `SPSiteUrl` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.  <br/> |해당 없음  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>5단계: Office 365에서 PST 가져오기 작업 만들기

다음 단계는 Office 365의 가져오기 서비스에서 PST 가져오기 작업을 만드는 것입니다. 앞서 설명한 것처럼 4단계에서 만든 PST 가져오기 매핑 파일을 전송합니다. 새 작업을 만든 후 Office 365는 PST 파일의 데이터를 분석한 다음 PST 가져오기 매핑 파일에 지정된 사서함으로 실제로 가져올 데이터를 필터링할 수 있는 기회를 제공합니다 ([6단계](#step-6-filter-data-and-start-the-pst-import-job) 참조).
  
1. Office 365 조직의 관리자 계정 자격 증명을 사용하여 [https://protection.office.com](https://protection.office.com)으로 이동하고 로그인합니다. 
    
2. 보안 및 준수 센터의 왼쪽 창에서 **데이터 관리**를 클릭한 다음 **가져오기**를 클릭합니다.
    
3. **가져오기** 페이지에서 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새 가져오기 작업**을 클릭합니다.
    
    **참고:** 새 가져오기 작업을 작성하려면 보안 및 준수 센터의 **가져오기** 페이지에 액세스 할 수 있는 적절한 권한을 할당받아야 합니다. 자세한 내용은 **시작하기 전에** 섹션을 참조하세요. 
    
4. PST 가져오기 작업의 이름을 입력하고 **다음**을 클릭합니다. 소문자, 숫자, 하이픈 및 밑줄을 사용하세요. 이름에는 대문자를 사용하거나 공백을 포함할 수 없습니다.
    
5. **데이터를 업로드하거나 배송 하시겠습니까?** 페이지에서 **데이터 업로드**를 클릭한 후 **다음**을 클릭합니다.
    
    ![데이터 업로드를 클릭하여 네트워크 업로드 가져오기 작업을 작성하세요.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. **데이터 가져오기** 페이지의 4단계에서 **내 파일 업로드를 완료했습니다.** 및 **매핑 파일에 대한 액세스 권한이 있습니다.** 확인란을 클릭하고 **다음**을 클릭합니다.
    
    ![4단계에서 두 개의 확인란을 클릭합니다.](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. **맵핑 파일 선택** 페이지에서 **맵핑 파일 선택**을 클릭하여 4단계에서 작성한 PST 가져오기 맵핑 파일을 제출합니다. 
    
    ![매핑 파일 선택을 클릭하여 가져오기 작업을 위해 만든 CSV 파일을 제출합니다.](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. CSV 파일 이름이 **매핑 파일 이름** 아래에 나타나면 **유효성 검사**를 클릭하여 CSV 파일에 오류가 있는지 확인합니다. 
    
    ![유효성 검사를 클릭하여 CSV 파일에 오류가 있는지 검사하기](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    PST 가져오기 작업을 만들려면 CSV 파일의 유효성 검사가 성공해야 합니다. 파일의 유효성을 검사하는 데 성공하면 파일 이름이 녹색으로 변경됩니다. 유효성 검사에 실패할 경우 **로그 보기** 링크를 클릭합니다. 실패한 파일의 각 행에 대한 오류 메시지를 포함한 유효성 검사 오류 보고서가 열립니다. 
    
9. PST 매핑 파일의 유효성 검사가 성공하면 사용 약관 문서를 읽고 확인란을 클릭합니다.
    
10. **저장**을 클릭하여 작업을 제출한 후 작업이 성공적으로 작성되면 **닫기**를 클릭합니다. 
    
    **분석이 진행 중** 상태를 포함한 플라이 아웃 페이지가 표시되고, 새 가져오기 작업이 **가져오기** 페이지의 목록에 표시됩니다. 
    
11. **새로 고침** ![새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif)을 클릭하여 **상태** 열에 표시되는 상태 정보를 업데이트합니다. 분석이 완료되고 데이터를 가져올 준비가 되면 상태가 **분석 완료**로 변경됩니다.
    
    가져오기 작업을 클릭하여 가져오기 작업에 대한 자세한 정보 (예: 매핑 파일에 나열된 각 PST 파일의 상태)를 포함하는 상태 플라이 아웃 페이지를 표시할 수 있습니다.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>6단계: 데이터 필터링 및 PST 가져오기 작업 시작

5단계에서 가져오기 작업을 만든 후에는 Office 365가 PST 파일에 포함된 항목의 경과 시간과 다양한 메시지 유형을 식별하여 안전한 방법으로 PST 파일의 데이터를 분석합니다. 분석이 완료되고 데이터를 가져올 준비가되면 PST 파일에 포함된 모든 데이터를 가져오거나 가져올 데이터를 제어하는 필터를 설정하여 가져온 데이터를 트리밍할 수 있습니다.
  
1. 보안 및 준수 센터의 **가져오기** 페이지에서 5단계에서 작성한 가져오기 작업에 대해 **Office 365로 가져오기 준비 완료**를 클릭합니다. 
    
    ![작성한 가져오기 작업 옆에 있는 Office 365로 가져오기 준비 완료를 클릭합니다.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    PST 파일에 대한 정보 및 가져오기 작업에 대한 기타 정보가 포함된 플라이 아웃 페이지가 표시됩니다.
    
2. 플라이 아웃 페이지에서 **Office 365로 가져오기**를 클릭합니다.
    
    데이터 필터링** 페이지가 표시됩니다. 여기에는 데이터 수명에 대한 정보를 포함하여 Office 365의 PST 파일에서 수행한 분석에서 얻은 데이터 인사이트가 포함되어 있습니다. 이 시점에서 모든 데이터를 그대로 가져 오거나 가져올 데이터를 필터링할 수 있습니다. 
    
    ![PST 파일의 데이터를 트리밍하거나 또는 모든 파일을 가져올 수 있습니다](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. 다음 중 하나를 수행합니다.
    
    a. 가져온 데이터를 트리밍하려면 **예, 가져오기 전에 필터링하고 싶습니다**를 클릭합니다.
    
    PST 파일에서 데이터를 필터링한 다음 가져오기 작업을 시작하는 방법에 대한 자세한 단계별 지침은 [PST 파일을 Office 365로 가져올 때 데이터 필터링](filter-data-when-importing-pst-files.md)을 참조합니다.
    
    또는
    
    b. PST 파일의 모든 데이터를 가져오려면 **아니오, 모든 것을 가져오겠습니다**를 클릭하고 **다음**을 클릭합니다.
    
4. 모든 데이터를 가져 오도록 선택한 경우 **데이터 가져오기**를 클릭하여 가져오기 작업을 시작합니다. 
    
    가져오기 작업의 상태는 **가져오기** 페이지에 표시됩니다. ![새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침**을 클릭하여 **상태** 열에 표시되는 상태 정보를 업데이트합니다. 가져오기 작업을 클릭하여 가져오는 각 PST 파일에 대한 상태 정보를 표시하는 상태 플라이 아웃 페이지를 표시합니다. 

## <a name="how-the-import-process-works"></a>가져오기 프로세스의 작동 방식
  
네트워크 업로드 옵션 및 Office 365 가져오기 서비스를 사용하여 PST 파일을 사용자 사서함에 대량으로 가져올 수 있습니다. 네트워크 업로드는 PST 파일을 Microsoft 클라우드의 임시 저장 영역으로 업로드하는 것을 의미합니다. 그런 다음 Office 365 가 오기 서비스는 저장 영역에서 대상 사용자 사서함으로 PST 파일을 복사합니다.
  
다음은 Office 365의 사서함으로 PST 파일을 가져오는 네트워크 업로드 프로세스에 대한 그림 및 설명입니다.
  
![PST 파일을 Office 365로 가져오기 위한 네트워크 업로드 프로세스의 워크플로](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **PST 가져오기 도구 및 키를 개인 Azure 저장소 위치로 다운로드** - 첫 번째 단계는 Azure AzCopy 명령줄 도구와 PST 파일을 Microsoft 클라우드의 Azure 저장소 위치에 업로드하는 데 사용되는 액세스 키를 다운로드하는 것입니다. 이는 보안 및 준수 센터의 **가져오기** 페이지에서 가져옵니다. 이 키 (SAS (Secure Access Signature) 키라고 함)는 사용자에게 비공개 보안 Azure 저장소 위치에 PST 파일을 업로드 하는 데 필요한 권한을 제공합니다. 이 액세스 키는 조직에 고유하며 PST 파일이 Microsoft 클라우드에 업로드된 후 PST 파일에대한 무단 액세스를 방지하는 데 도움이 됩니다. PST 파일을 Office 365로 가져오는 경우 조직에 별도의 Azure 구독을 사용할 필요가 없습니다. 
    
2. **Azure 저장소 위치에 PST 파일 업로드** - 다음 단계는 AzCopy.exe 도구 (1단계에서 다운로드)를 사용하여 사용자의 Office 365 조직 위치와 동일한 지역의 Microsoft 데이터 센터에 있는 Azure 저장소 위치에 PST 파일을 업로드하고 저장하는 것입니다. 파일을 업로드 하려면 Office 365로 가져오려는 PST 파일은 조직의 파일 공유 또는 파일 서버에 위치해야 합니다.
    
    PST 파일이 Azure 저장소 위치에 업로드 된 후 PST 파일 목록을 보기 위해 수행할 수 있는 선택적 단계가 있습니다.
    
3. **PST 가져오기 매핑 파일 만들기** - PST 파일을 Azure 저장소 위치에 업로드한 후의 다음 단계는 가져온 PST파일이 위치하게 될 사용자 사서함을 지정하는 쉼표로 구분 된 값 (CSV) 파일을 만드는 것입니다. (PST 파일은 사용자의 기본 사서함이나 보관 사서함으로 가져올 수 있습니다). Office 365 가져오기 서비스는 CSV 파일의 정보를 사용하여 PST 파일을 가져옵니다.
    
4. **PST 가져오기 작업 만들기** - 다음 단계는 보안 & 준수 센터의 **가져오기** 페이지에서 PST 가져오기 작업을 만들고 이전 단계에서 만든 PST 가져오기 매핑 파일을 제출하는 것입니다. 가져오기 작업을 만든 후 Office 365는 PST 파일의 데이터를 분석한 다음 PST 가져오기 매핑 파일에 지정된 사서함으로 실제로 가져올 데이터를 제어하는 필터를 설정할 수 있는 기회를 제공합니다. 
    
5. **사서함으로 가져올 PST 데이터 필터링** - 가져오기 작업이 만들어지고 시작된 후 Office 365에서 PST 파일의 데이터를 PST 파일에 포함된 다양한 메시지 유형과 항목의 보존 기간을 식별하는 방법으로 안전하고 꼼꼼하게 분석합니다. 분석이 완료되고 데이터를 가져올 준비가되면 PST 파일에 포함된 모든 데이터를 가져오거나 가져올 데이터를 제어하는 필터를 설정하여 가져온 데이터를 트리밍할 수 있습니다.
    
6. **PST 가져오기 작업 시작** - 가져오기 작업이 시작되면 Office 365는 PST 가져오기 매핑 파일의 정보를 사용하여 Azure 저장소 위치의 PST 파일을 사용자 사서함으로 가져옵니다. 가져오기 작업에 대한 상태정보 (가져오는 각 PST 파일에 대한 정보 포함)는 보안 & 준수 센터의 **가져오기** 페이지에 표시됩니다. 가져오기 작업이 완료되면 해당 작업의 상태가 **완료**로 설정됩니다.
  
## <a name="more-information"></a>추가 정보

- Office 365에 PST 파일 가져오는 이유
    
  - 조직에서 보관하는 메시징 데이터를 Office 365로 가져오는 것이 좋습니다.
    
  - 이러한 데이터는 클라우드에 저장되므로 모든 장치에서 사용할 수 있습니다.
    
  - 가져온 PST 파일의 데이터에 Office 365 규정 준수 기능을 적용하여 조직의 규정 준수 요구 사항을 해결하는 데 도움이 됩니다. 여기에는 다음이 포함됩니다.
    
  - [보관 사서함](enable-archive-mailboxes.md) 및 [자동 확장 보관](enable-unlimited-archiving.md)을 사용하면 사용자에게 가져온 데이터를 저장할 수 있는 추가적인 사서함 저장 공간이 제공됩니다. 
    
  - 사서함을 [소송 보존](https://go.microsoft.com/fwlink/?linkid=856286)에 배치하여 가져온 데이터를 유지합니다. 
    
  - Microsoft [eDiscovery 도구](search-for-content.md)를 사용하여 가져온 데이터를 검색합니다. 
    
  - [Office 365 보존 정책](retention-policies.md)을 사용하여 가져온 데이터가 보존되는 기간 및 보존 기간이 만료된 후 수행할 작업을 제어합니다. 
    
  - 가져온 데이터에 영향을 주는 사서함 관련 이벤트에 대한 [Office 365 감사 로그](search-the-audit-log-in-security-and-compliance.md)를 검색합니다. 
    
  - 데이터를 [비활성 사서함으로 가져와 규정 준수를 위해 데이터를 보관합니다. 
    
  - [데이터 손실 방지 정책](data-loss-prevention-policies.md)을 사용하여 중요한 데이터가 조직 외부로 유출되는 것을 방지합니다. 
  
- 다음은 1단계에서 획득한 SAS (공유 액세스 서명) URL의 예입니다. 이 예에서는 PST 파일을 Office 365에 업로드하기 위해 AzCopy.exe 도구에서 실행하는 명령 구문도 포함되어 있습니다. 암호 또는 기타 보안 관련 정보를 보호하는 것처럼 주의해서 SAS URL을 보호해야 합니다.

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
    
