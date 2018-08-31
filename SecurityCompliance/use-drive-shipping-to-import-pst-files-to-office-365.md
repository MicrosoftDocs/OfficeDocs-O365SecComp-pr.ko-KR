---
title: 드라이브 전달을 사용 하 여 Office 365로 조직 PST 파일을 가져오려면
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 40829b57-793c-4d41-b171-e9270129173d
description: '관리자를 위한: Office 365 사서함에 조직의 PST 파일을 하드 드라이브에 PST 파일을 복사 하 고 다음을 Microsoft에 전달 하 여 대량 가져오기 하는 방법을 설명 합니다. '
ms.openlocfilehash: ebe88918b6c25e18562db7817d22fbf71f05e4c7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533413"
---
# <a name="use-drive-shipping-to-import-your-organization-pst-files-to-office-365"></a>드라이브 전달을 사용 하 여 Office 365로 조직 PST 파일을 가져오려면

**이 문서는 관리자입니다. 자신의 사서함에 PST 파일을 가져올 하려고 합니까? [가져오기 전자 메일, 연락처 및 일정 Outlook.pst 파일에서](https://go.microsoft.com/fwlink/p/?LinkID=785075) 를 참조 하십시오.**
   
Office 365를 가져올 서비스 및 대량 가져오기 PST 파일을 사용자 사서함에 전달 하는 드라이브를 사용 합니다. 드라이브 전달 PST 파일을 하드 디스크 드라이브에 복사 하 고 Microsoft에 드라이브를 물리적으로 제공 하는 것을 의미 합니다. Microsoft가 사용자의 하드 드라이브를 받으면 데이터 센터 담당자는 Microsoft 클라우드에서 저장소 영역에 데이터를 하드 드라이브에서 복사 됩니다. 그런 다음 데이터를 가져온 가져옵니다을 제어 하는 필터를 설정 하 여 가져올 대상 사서함에 실제로 PST 데이터 트리밍할 기회를 해야 합니다. 가져오기 작업을 시작한 후 가져오기 서비스 PST 데이터를 사용자 사서함에 저장 영역에서 가져옵니다. 드라이브 전달을 사용 하 여 사용자 사서함에 PST 파일을 가져오려면 Office 365에 조직의 전자 메일을 마이그레이션하는 한 가지 방법은 합니다.
  
Office 365 사서함에 PST 파일을 가져오려면 드라이브 전달을 사용 하 여 필요한 단계는 다음과 같습니다.
  
[1 단계: 보안 저장소 키 및 PST 가져오기 도구를 다운로드 합니다.](#step-1-download-the-secure-storage-key-and-pst-import-tool)

[2 단계: PST 파일을 하드 드라이브에 복사](#step-2-copy-the-pst-files-to-the-hard-drive)

[3 단계: PST 가져오기 매핑 파일 만들기](#step-3-create-the-pst-import-mapping-file)

[4단계: Office 365에서 PST 가져오기 작업 만들기](#step-4-create-a-pst-import-job-in-office-365)

[5단계: Microsoft로 하드 드라이브 발송](#step-5-ship-the-hard-drive-to-microsoft)

[6 단계: 데이터를 필터링 하 고 PST 가져오기 작업 시작](#step-6-filter-data-and-start-the-pst-import-job)
  
> [!IMPORTANT]
> 아래로 보안 저장소 키 및 가져오기 도구를 로드 한 번 1 단계를 수행 해야 합니다. 다음이 단계를 수행한 후 6 단계를 통해 2 단계를 Microsoft 하드 드라이브를 제공 하려는 때마다를 따릅니다. 
  
자주에 대 한 Office 365로 PST 파일을 가져오는 [PST 파일을 가져오려면 전달 하는 드라이브를 사용 하는 것에 대 한 Faq](faqimporting-pst-files-to-office-365.md#using-drive-shipping-to-import-pst-files)를 참조 하십시오 전달 드라이브를 사용 하는 방법에 대 한 대답 (영문). 
  
## <a name="before-you-begin"></a>시작하기 전에

- 역할을 할당 사서함 가져오기 내보내기 Exchange 온라인 Office 365 사서함에 PST 파일을 가져오려면 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 다음 자신을 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹](https://go.microsoft.com/fwlink/p/?LinkId=730688)에 "역할 그룹 만들기" 섹션이 있습니다.
    
    또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.
    
  - 역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.
    
    또는
    
  - Office 365 조직에서 전역 관리자 여야 해야 합니다.
    
    > [!TIP]
    > Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다. 
  
- 파일 서버 또는 조직에 있는 공유 폴더에는 하드 드라이브에 복사 하려는 PST 파일을 저장 해야 합니다. 2 단계에서에서 됩니다 도구를 실행 하면 Azure 가져오기 내보내기 (WAImportExport.exe)는이 파일 서버에 저장 된 하드 드라이브에 폴더를 공유 하거나 PST 파일에 복사 됩니다.
    
- 2.5 인치만 반도체 드라이브 (Ssd) 또는 2.5 또는 3.5 인치 SATA II/III 내부 하드 드라이브에 Office 365 가져오기 서비스와 함께 사용할 수 있도록 지원 합니다. 하드 드라이브를 사용할 수 있는 최대 10TB 합니다. 가져오기 작업에 대 한 하드 드라이브에 첫번째 데이터 볼륨을 처리 됩니다. 데이터 볼륨 NTFS로 포맷 되어야 합니다. 하드 드라이브에 데이터를 복사, 2.5 인치 SSD를 사용 하 여 직접 연결할 수 있습니다 또는 2.5 또는 3.5 인치 SATA II/III 커넥터 또는 외부 2.5 인치 SSD를 사용 하 여 외부에서 또는 2.5 또는 3.5 인치 SATA II/III USB 어댑터를 연결할 수 있습니다.
    
    > [!IMPORTANT]
    > 외부 하드 드라이브에 사용 된 기본 제공 된 USB 어댑터와 함께 제공 되는 Office 365 가져오기 서비스에서 지원 되지 않습니다. 또한 외부 하드 드라이브의 대/소문자 내부 디스크를 사용할 수 없습니다. 하드 드라이브에 외부 하십시오 제공 하지 마십시오. 
  
- PST 파일을 복사 하는 하드 드라이브 BitLocker로 암호화 해야 합니다. 2 단계에서에서 실행 되는 WAImportExport.exe 도구는 BitLocker을 설정 하는 데 도움이 됩니다. BitLocker 암호화 키를 데이터 센터 담당자 Microsoft 클라우드에서 Azure 저장소 영역에 PST 파일을 업로드 하려면 드라이브에 액세스를 사용 하 여 해당 Microsoft도 생성 됩니다.
    
- 드라이브 전달을을 통해 프로그램 Microsoft EA (기업 계약) 사용할 수 있습니다. 드라이브 전달 Microsoft 제품 및 서비스 계약 (MPSA)를 통해 사용할 수 없습니다.
    
- 드라이브 전달을 사용 하 여 Office 365 사서함을 PST 파일을 가져오려면 비용은 $2 달러 (미국) GB의 데이터입니다. 예, 1, 000 g B (1TB)의 PST 파일을 포함 하는 하드 드라이브를 제공 하는 경우는 비용은 $ 2, 000 USD입니다. 가져오기 요금을 지불 하는 파트너를 사용 하 여 작업할 수 있습니다. 파트너 찾기 (영문) 하는 방법에 대 한 정보를 [Office 365 파트너 또는 대리점 찾기](https://go.microsoft.com/fwlink/p/?LinkId=785197)를 참조 하십시오.
    
- 사용자나 조직은 FedEx 또는 DHL 계정이 있어야 합니다. 
    
  - 미국, 브라질 및 유럽의 조직에서는 FedEx 계정을 있어야 합니다.
    
  - 조직에서 한국, 남동쪽 아시아, 일본, 대한민국, 및 오스트레일리아 DHL 계정을 있어야 합니다.
    
    Microsoft는 이 계정을 사용(및 충전)한 후 하드 드라이브를 사용자에게 반환합니다. 
    
- Microsoft로 하드 드라이브를 발송하기 위해 국경을 통과해야 할 수 있습니다. 이러한 경우 하드 드라이브와 포함된 데이터를 관련 법률에 따라 수출 및/또는 수입해야 합니다. 하드 드라이브를 발송하기 전에 드라이브 및 데이터가 확인된 Microsoft 데이터 센터에 합법적으로 발송될 수 있는지를 관리자에게 문의하세요. 그래야 하드 드라이브가 적시에 Microsoft로 발송될 수 있습니다.
    
- 이 절차 복사 하는 보안 저장소 키와 BitLocker 암호화 키를 저장 하는 작업이 포함 됩니다. 암호 또는 기타 보안 관련 정보를 보호 하는 동일 하 게 이러한 키를 보호 하기 위한 예방 조치를 수행 해야 합니다. 예 암호로 보호 된 Microsoft Word 문서에 저장 또는 암호화 된 USB 드라이브에 저장 수 있습니다. 이러한 키의 한 예에 대 한 [자세한 내용](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) 은 섹션을 참조 하십시오. 
    
- PST 파일을 Office 365 사서함으로 가져온 후 사서함에 대 한 설정 보존 대기는 무기한 기간에 대 한 켜 집니다. 즉, 사서함에 할당 된 보존 정책 보존 보류 해제 하거나 보류를 해제 하려면 날짜를 설정할 때까지 처리 되지 않습니다. 이유 해야 할까요? 오래 된 메시지를 사서함으로 가져온 경우 이러한 수 영구적으로 삭제 됩니다 (비우기)가 보존 기간이 만료 되었기 때문에 사서함에 대해 구성 된 보존 설정에 따라 합니다. 사서함을 보존 대기 배치 이러한 새로 가져온 메시지 또는 사서함에 대 한 보존 설정을 변경 하려면 시간 부여를 관리 하는 사서함 소유자 시간을 제공 합니다. 보존 대기 상태를 관리 하는 방법에 대 한 제안에 대 한 [자세한 내용](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) 은 섹션을 참조 하십시오. 
    
- 기본적으로 Office 365 사서함으로 받을 수 있는 최대 메시지 크기는 35 MB입니다. 사서함에 대 한 *MaxReceiveSize* 속성에 대 한 기본값을 35 MB 로설정하면 때문입니다. 그러나는 최대 메시지 크기를 Office 365에서 수신에 대 한 제한은 150MB입니다. 따라서 35 MB, 150MB를 대상 사서함에서 *MaxReceiveSize* 속성의 값을 자동으로 바뀝니다는 Office 365를 가져올 서비스 보다 큰 항목을 포함 하는 PST 파일을 가져오는 경우. 이 메시지를 통해 최대 150MB 사용자 사서함으로 가져올 수 있도록 합니다. 
    
    > [!TIP]
    > 메시지 수신 크기를 식별 하는 사서함에 대 한 Exchange Online PowerShell에서이 명령을 실행할 수: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`합니다. 
  
- Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니다. 비활성 사서함의 GUID를 지정 하 여이 작업을 수행 된 `Mailbox` PST 가져오기 매핑 파일에서 매개 변수입니다. 참조 [3 단계: PST 가져오기 매핑 파일을 만드는](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) 에 대 한 자세한 내용은 합니다. 
    
- Exchange 하이브리드 배포에서 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져올 수 있습니다. PST 가져오기 매핑 파일에서 다음을 수행 하 여이 수행 합니다.
    
  - 사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 된 `Mailbox` 매개 변수입니다. 
    
  - **TRUE** 값을 지정 된 `IsArchive` 매개 변수입니다. 
    
    참조 [3 단계: PST 가져오기 매핑 파일을 만드는](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) 에 대 한 자세한 내용은 합니다. 

## <a name="step-1-download-the-secure-storage-key-and-pst-import-tool"></a>1 단계: 보안 저장소 키 및 PST 가져오기 도구를 다운로드 합니다.

첫번째 단계는 보안 저장소 키를 다운로드 하는 하 고 도구와 해당 사용자 2 단계에서에서 복사 PST 파일을 하드 드라이브에 사용 됩니다.
  
> [!IMPORTANT]
> 성공적으로 드라이브 배송 메서드를 사용 하 여 PST 파일을 가져오려면 Azure 가져오기/내보내기 도구 버전 1 (WAimportExportV1)를 사용 해야 합니다. 버전 2의 Azure 가져오기/내보내기 도구 지원 되지 않습니다 및 가져오기 작업에 대해 올바르게 하드 드라이브를 준비 하기를 사용 하면 발생 합니다. 보안에서 Azure 가져오기/내보내기 도구를 다운로드 해야 &amp; 이 단계의 절차를 수행 하 여 준수 센터입니다. 
  
1. 이동 [https://protection.office.com/](https://protection.office.com/) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **가져오기**.
    
    > [!NOTE]
    > 듯이 보안에서 **가져오기** 페이지에 액세스 하려면 적절 한 사용 권한을 할당할 필요가 &amp; 준수 센터입니다. 
  
3. **가져오기** 페이지에서 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새로 만들기 작업을 가져옵니다**.
    
4. 가져오기 작업 마법사에서 PST 가져오기 작업에 대 한 이름을 입력 하 고 **** 을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄만 사용 합니다. 맞춤법 검사 시 대문자로 사용 하거나 이름에 공백을 포함할 수 없습니다.
    
5. **Choose 가져오기 작업 유형** 페이지에서 **이 실제 위치 중 하나로 배송 하드 드라이브** 를 클릭 하 고 **** 을 클릭 합니다.
    
    ![가져오기 작업을 전달 하는 드라이브를 만들기 위해이 실제 위치 중 하나로 배송 하드 드라이브를 클릭 합니다.](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. **데이터 가져오기** 페이지에서 다음 두 작업을 수행 합니다. 
    
    ![보안 저장소 키를 복사 하 고 가져오기 데이터 페이지에서 Azure 가져오기 내보내기 도구를 다운로드](media/e22e0b48-e5ce-48e0-95bc-0490a2b3b983.png)
  
    a. 2 단계에서 **보안 저장소 키에 복사**를 클릭 합니다. 저장소 키 표시 된 후 **클립보드에 복사** 를 클릭 하 고 붙여넣으십시오 하 고 나중에 액세스할 수 있도록 파일에 저장 합니다.
    
    b.에서 단계 3을 다운로드 하 고 Azure 가져오기/내보내기 (버전 1) 도구를 설치 하려면 **Azure 가져오기/내보내기 도구를 다운로드** 합니다.
    
    - 팝업 창에서 **저장** 을 클릭 \> 로컬 컴퓨터의 폴더에 WaImportExportV1.zip 파일을 저장 하려면 **로 저장** 합니다. 
    
    - WaImportExportV1.zip 파일을 추출 합니다.
    
7. 마법사를 닫으려면 **취소** 를 클릭 합니다. 
    
    **가져오기** 페이지의 보안에서 돌아갈 게 &amp; 4 단계에서에서 가져오기 작업을 만들 때 준수 센터입니다. 

## <a name="step-2-copy-the-pst-files-to-the-hard-drive"></a>2 단계: PST 파일을 하드 드라이브에 복사

다음 단계에서는 PST 파일을 하드 드라이브에 복사 하려면 WAImportExport.exe 도구를 사용 하는 것입니다. 이 도구 BitLocker와 하드 드라이브를 암호화 하 고는 Pst 하드 드라이브에 복사 하는 복사 하는 프로세스에 대 한 정보를 저장 하는 저널 파일을 만듭니다. 이 단계를 완료 하려면 PST 파일에는 파일 공유 또는 조직에서 파일 서버에 배치 해야 합니다. 이 다음 절차에는 원본 디렉터리 이라고 합니다. 
  
> [!IMPORTANT]
> 다른 프로그램 구문을 사용 하 여 해야 하드 드라이브에 처음으로 WAImportExport.exe 도구를 실행 한 후 그 이후에 시간입니다. 이 구문은 PST 파일을 하드 드라이브에 복사 하려면이 절차의 4 단계에서 설명 합니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트를 엽니다.
    
    > [!TIP]
    > 관리자 권한으로 명령 프롬프트를 실행하는 경우(열 때 "관리자 권한으로 실행" 선택) 명령 프롬프트 창에 오류 메시지가 표시됩니다. 이 메시지는 WAImportExport.exe 도구를 실행할 때 발생하는 문제를 해결하는 데 도움이 됩니다. 
  
2. 1단계에서 WAImportExport.exe 도구를 설치한 디렉터리로 이동합니다.
    
3. WAImportExport.exe를 사용하여 하드 드라이브에 PST 파일을 처음 복사할 때 다음 명령을 실행합니다.

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>
    ```

    다음 표에서는 매개 변수와 해당 필수 값에 대해 설명합니다.
    
    |**매개 변수**|**설명**|**예제**|
    |:-----|:-----|:-----|
    | `/j:` <br/> |저널 파일의 이름을 지정합니다. 이 파일은 WAImportExport.exe 도구가 있는 동일한 폴더에 저장됩니다. Microsoft로 발송하는 각 하드 드라이브에는 하나의 저널 파일이 있어야 합니다. WAImportTool.exe를 실행하여 PST 파일을 하드 드라이브에 복사할 때마다 해당 드라이브에 대한 저널 파일에 정보가 추가됩니다. 
  <br/> 4 단계에서에서 만든 가져오기 작업 하드 드라이브에 연결 하 고 Microsoft 클라우드에서 Azure 저장소 영역에 PST 파일을 업로드 하려면 Microsoft 데이터 센터 담당자 저널 파일의 정보를 사용 합니다.  <br/> | `/j:PSTHDD1.jrn` <br/> |
    | `/t:` <br/> |로컬 컴퓨터에 연결될 때 하드 드라이브의 드라이브 문자를 지정합니다.  <br/> | `/t:h` <br/> |
    | `/id:` <br/> |복사 세션의 이름을 지정합니다. 세션은 WAImportExport.exe 도구를 실행하여 하드 드라이브에 파일을 복사할 때마다 정의됩니다. PST 파일이 이 매개 변수로 지정된 세션 이름의 폴더에 복사됩니다.   <br/> | `/id:driveship1` <br/> |
    | `/srcdir:` <br/> |PST 파일을 복사 하는 세션 중을 포함 하는 조직에서 원본 디렉터리를 지정 합니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").  <br/> | `/srcdir:"\\FILESERVER01\PSTs"` <br/> |
    | `/dstdir:` <br/> |Pst 업로드 될 Microsoft 클라우드에서 Azure 저장소 영역에서 대상 디렉터리를 지정 합니다. 값을 사용 해야 `ingestiondata/`합니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").<br/> 원하는 경우이 매개 변수의 값에도 추가 파일 경로 추가할 수 있습니다. 예 (URL 형식으로 변환 됨) 하는 하드 드라이브에에서 지정 된 원본 디렉터리의 파일 경로 사용할 수 있습니다는 `/srcdir:` 매개 변수입니다. 예, `\\FILESERVER01\PSTs` 로 변경 `FILESERVER01/PSTs`합니다. 이 경우에 포함 해야 `ingestiondata` 의 파일 경로입니다. 이 예제에서는 값에 대 한 그럴는 `/dstdir:` 매개 변수는 것 `"ingestiondata/FILESERVER01/PSTs"`합니다.<br/> 추가 파일 경로 추가 하는 한 가지 이유는 파일 이름이 같은 Pst 파일을 포함 하는 경우.  <br/> > [!NOTE]> Azure 저장소 영역으로 업로드 된 후 PST 파일에 대 한 네임 스페이스; PST 파일의 이름과 경로 이름이 포함 됩니다 선택적 pathname을 포함 하는 경우 예, `FILESERVER01/PSTs/annb.pst`합니다. 네임 스페이스는 PST 파일 이름만; 경로 이름을 포함 하지 않으면 예 `annb.pst`합니다.           | `/dstdir:"ingestiondata/"` <br/> 또는  <br/>  `/dstdir:"ingestiondata/FILESERVER01/PSTs"` <br/> |
    | `/sk:` <br/> |1 단계에서에서 구한 저장소 계정 키를 지정 합니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").  <br/> | `"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ=="` <br/> |
    | `/encrypt` <br/> |이 스위치는 하드 드라이브에 대해 BitLocker를 켭니다. 이 매개 변수는 WAImportExport.exe 도구를 처음 실행할 때 필요합니다.  <br/> BitLocker 암호화 키 저널 파일 및 사용 하는 경우 생성 된 로그 파일에 복사 되는 `/logfile:` 매개 변수입니다. 앞에서 설명한 것 처럼 저널 파일 WAImportExport.exe 도구가 위치한 같은 폴더에 저장 됩니다.<br/> | `/encrypt` <br/> |
    | `/logdir:` <br/> |이 선택적 매개 변수는 로그 파일을 저장할 폴더를 지정 합니다. 지정 하지 않으면 로그 파일 WAImportExport.exe 도구가 위치한 동일한 폴더에 저장 됩니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").  <br/> | `/logdir:"c:\users\admin\desktop\PstImportLogs"` <br/> |
   
    다음은 각 매개 변수에 대한 실제 값을 사용하는 WAImportExport.exe 도구에 대한 구문 예입니다.
    
    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER01\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"
    ```

    이 명령을 실행한 후 하드 드라이브에 대한 PST 파일 복사 진행률을 보여 주는 상태 메시지가 표시됩니다. 마지막 상태 메시지에는 성공적으로 복사된 파일의 총 수가 표시됩니다. 
    
4. WAImportExport.ext 도구를 실행하여 PST 파일을 동일한 하드 드라이브에 복사한 이후에 매번 이 명령을 실행합니다.

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 
    ```

    다음은 PST 파일을 동일한 하드 드라이브에 복사하기 위한 후속 세션 실행 구문의 예입니다.  

    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER01\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```

## <a name="step-3-create-the-pst-import-mapping-file"></a>3 단계: PST 가져오기 매핑 파일 만들기

가져오기 서비스에서 PST는 사용자 사서함을 지정 하는 쉼표로 구분 된 값 (CSV) 파일을 PST 가져오기 매핑 파일에 정보를 사용할 Microsoft 데이터 센터 담당자 Azure 저장소 영역에는 하드 드라이브에서 PST 파일을 업로드 한 후 파일을 가져올 수 됩니다. PST 가져오기 작업을 만들 때에 다음 단계에는이 CSV 파일을 전송 됩니다.
  
1. [PST 가져오기 매핑 파일의 복사본을 다운로드](https://go.microsoft.com/fwlink/p/?LinkId=544717)합니다.
    
2. CSV 파일을 열거나 로컬 컴퓨터에 저장합니다. 다음 예에서는 완료된 PST 가져오기 매핑 파일(메모장에서 열림)을 보여 줍니다. CSV 파일을 편집할 경우 Microsoft Excel을 사용하는 것이 훨씬 더 쉽습니다.

    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,FILESERVER01/PSTs,annb.pst,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,annb_archive.pst,annb@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,FILESERVER01/PSTs,donh.pst,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,donh_archive.pst,donh@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,FILESERVER01/PSTs,pilarp.pst,pilarp@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,pilarp_archive.pst,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,,tonyk.pst,tonyk@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,tonyk_archive.pst,tonyk@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,,zrinkam.pst,zrinkam@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,zrinkam_archive.pst,zrinkam@contoso.onmicrosoft.com,TRUE,,,,,
    ```

    첫째 행 또는 CSV 파일의 머리글 행을 사용자 사서함에 PST 파일을 가져오려면 PST 가져오기 서비스에서 사용 되는 매개 변수를 나열 합니다. 각 매개 변수 이름은 쉼표로 구분 됩니다. 각 행 머리글 행에서 특정 사서함에 PST 파일 가져오기 (영문)에 대 한 매개 변수 값을 나타냅니다. 하드 드라이브에 복사 된 각 PST 파일에 대 한 행을 할 수 있습니다. 실제 데이터와 매핑 파일의 개체 틀 데이터를 교체 해야 합니다.

    > [!NOTE]
    > SharePoint 매개 변수를 포함하여 머리글 행의 어떤 내용도 변경하지 않도록 합니다. 변경한 내용은 PST 가져오기 프로세스 동안 무시됩니다. 
  
3. 다음 표의 정보를 사용하여 CSV 파일을 필요한 정보로 채웁니다.
    
    |**매개 변수**|**설명**|**예제**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |데이터를 가져올 수는 Office 365 서비스를 지정 합니다. 사용자 사서함을 PST 파일을 가져오려면, 사용 `Exchange`합니다.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> | PST 파일에 복사 됩니다를 하드 드라이브를 전달 하는 경우 Microsoft Azure 저장소 영역에서 폴더 위치를 지정 합니다.  <br/>  CSV 파일에이 열에 추가 기능에 지정한 것에 대 한 했는지에 따라는 `/dstdir:` 이전 단계에서 매개 변수입니다.  <br/>  사용 하는 경우 `/dstdir:"ingestiondata/"`, 다음이 매개 변수를 비워둘 CSV 파일에 있습니다.  <br/>  값에 대 한 경로 선택적 이름을 포함 하는 경우는 `/dstdir:` 매개 변수 (예 `/dstdir:"ingestiondata/FILESERVER01/PSTs"`, 다음 하 pathname ("ingestiondata" 제외)를 사용 하 여 CSV 파일에이 매개 변수에 대 한 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다.<br/>  두 방법 모두에 대 한 값에 "ingestiondata"를 포함 *하지* 는 `FilePath` 매개 변수입니다. 이 매개 변수를 비워둘 또는 선택적 경로 이름을 지정 합니다.<br/> > [!IMPORTANT]> 파일 경로 이름에 대 한 경우에 지정 하는 동일한 대/소문자 여야 합니다.의 `/dstdir:` 이전 단계에서 매개 변수입니다. 예: 사용 하는 경우 `"ingestiondata/FILESERVER01/PSTs"` 이전 단계에서 하위 폴더 이름에 대 한 다음 사용 하지만 `fileserver01/psts` 에 `FilePath` CSV 파일의 매개 변수, PST 파일에 대 한 가져오기가 실패 합니다. 두 경우 모두 동일한 대/소문자를 사용 해야 합니다.           |(공백으로 둠)  <br/> 또는  <br/>  `FILESERVER01/PSTs` <br/> |
    | `Name` <br/> |사용자 사서함에 가져올 PST 파일의 이름을 지정 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다.<br/> > [!IMPORTANT]> CSV 파일에서 PST 파일 이름의 경우 2 단계에서에서 Azure 저장소 위치에 업로드 된 PST 파일로 동일 해야 합니다. 예: 사용 하는 경우 `annb.pst` 에 `Name` 하 여 CSV 파일을 하지만 실제 PST 파일의 이름에서 매개 변수는 `AnnB.pst`, 해당 PST 파일에 대 한 가져오기가 실패 합니다. CSV 파일의 PST의 이름이 동일한 대/소문자를 사용 하 여 실제 PST 파일로 확인 해야 합니다.           | `annb.pst` <br/> |
    | `Mailbox` <br/> |PST 파일을 가져올 수는 사서함의 전자 메일 주소를 지정 합니다. 참고 PST 가져오기 서비스 공용 폴더에 PST 파일 가져오기 (영문)이 지원 되지 않으므로 공용 폴더를 지정할 수 없습니다.<br/> 비활성 사서함을 PST 파일을 가져오려면,이 매개 변수에 대 한 사서함 GUID를 지정 해야 합니다. 이 GUID를 가져오려면 다음 PowerShell 명령을 Exchange Online에서 실행: ' Get-mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> > [!NOTE]> In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-mailbox<identity of active mailbox> | FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command:  `Get-mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid' 합니다.           | `annb@contoso.onmicrosoft.com` <br/> 또는  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | PST 파일을 사용자의 보관 사서함으로 가져올 것인지 여부를 지정합니다. 다음 두 가지 옵션이 있습니다.<br/> **False 이면** 사용자의 기본 사서함을 PST 파일을 가져옵니다.  <br/> **True 이면** 사용자의 보관 사서함을 PST 파일을 가져옵니다. 이 가정 하는 [사용자의 보관 사서함 사용 하도록 설정](enable-archive-mailboxes.md)합니다. 이 매개 변수를 설정 하는 경우 `TRUE` 하 고 사용자의 보관 사서함 설정 되지 않은, 해당 사용자에 대 한 가져오기가 실패 합니다. 한 명의 사용자에 대 한 가져오기 실패 하는 경우 (자신의 아카이브를 사용할 수 없는 하 고이 속성은 설정 하기 때문에 `TRUE`), 가져오기 작업에서 다른 사용자가 영향을 받지 않습니다.<br/>  이 매개 변수를 지정 하지 않으면 사용자의 기본 사서함에 PST 파일을 가져옵니다.  <br/> **참고:** 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져오려면, 방금 지정 `TRUE` 이 매개 변수에 대 한 메일에 대 한 사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 하 고는 `Mailbox` 매개 변수입니다.  <br/> | `FALSE` <br/> 또는  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | PST 파일을 가져온 사서함 폴더를 지정 합니다.  <br/>  이 매개 변수를 지정 하지 않고 공백으로 두면 PST 명명 된 **가져온** (받은 편지함 폴더와 다른 기본 사서함 폴더와 동일한 수준) 사서함의 루트 수준에 있는 새 폴더를으로 가져옵니다.  <br/>  지정 하는 경우 `/`, PST 파일의 항목에에서 사용자의 받은 편지함 폴더에서 직접 가져올 수 됩니다.  <br/>  지정 하는 경우 `/<foldername>`, 라는 폴더를 가져올 PST 파일의 항목에에서 * \<foldername\> * 합니다. 예: 사용 하는 경우 `/ImportedPst`, **ImportedPst**라는 폴더에 항목을 가져올 수는 있습니다. 이 폴더는 받은 편지함 폴더와 같은 수준에 있는 사용자의 사서함에 배치 됩니다.<br/> |(공백으로 둠)  <br/> 또는  <br/>  `/` <br/> 또는  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |이 선택적 매개 변수는 ANSI 파일 형식에서 PST 파일을 가져오기 위해 사용 하 여 코드 페이지에 대 한 숫자 값을 지정 합니다. 이 매개 변수는 일반적으로 이러한 언어 문자 인코딩에 대 한 더블 바이트 문자 집합 (DBCS)을 사용 하기 때문에 중국어, 일본어 및 한국어 (CJK) 조직에서 PST 파일을 가져오기 위해 사용 됩니다. 이 매개 변수는 사서함 폴더 이름에 대 한 DBCS를 사용 하는 언어에 대 한 PST 파일을 가져오려면 사용 되지 않습니다, 하는 경우 폴더 이름은 가져온 후 왜곡 자주는 합니다.<br/> 이 매개 변수를 사용 하 여 지원 되는 값의 목록에 대 한 [코드 페이지 식별자](https://go.microsoft.com/fwlink/p/?LinkId=328514)를 참조 하십시오.  <br/> > [!NOTE]> 앞부분에 명시 된,이 선택적 매개 변수 이며 CSV 파일에 포함할 필요가 없습니다. 또는 포함 하 고 하나 이상의 행에 대 한 값은 비워둡니다.           |(공백으로 둠)  <br/> 또는  <br/>  `932`(ANSI/OEM 일본어에 대 한 코드 페이지 식별자는)  <br/> |
    | `SPFileContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPManifestContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPSiteUrl` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |

## <a name="step-4-create-a-pst-import-job-in-office-365"></a>4단계: Office 365에서 PST 가져오기 작업 만들기

다음 단계에서는 Office 365에서 가져오기 서비스에서 PST 가져오기 작업을 만드는 것입니다. 앞에서 설명한 것 처럼 3 단계에서에서 만든 PST 가져오기 매핑 파일을 전송 됩니다. 새 작업을 만든 후 가져오기 서비스는 PST 파일은 하드 드라이브에서 Azure 저장소 영역으로 복사 되 고 컨트롤을 만들고 가져오기 작업을 시작 후 지정 된 사용자 사서함을 PST 파일을 가져오려면 정보를 매핑 파일에 사용 됩니다.
  
1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.
    
3. **가져오기** 페이지에서 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새로 만들기 작업을 가져옵니다**.
    
    > [!NOTE]
    > 듯이 보안에서 **가져오기** 페이지에 액세스 하려면 적절 한 사용 권한을 할당할 필요가 &amp; 준수 센터입니다. 
  
4. PST 가져오기 작업에 대 한 이름을 입력 하 고 **** 을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄만 사용 합니다. 맞춤법 검사 시 대문자로 사용 하거나 이름에 공백을 포함할 수 없습니다.
    
5. **Choose 가져오기 작업 유형** 페이지에서 **이 실제 위치 중 하나로 배송 하드 드라이브** 를 클릭 하 고 **** 을 클릭 합니다.
    
    ![가져오기 작업을 전달 하는 드라이브를 만들기 위해이 실제 위치 중 하나로 배송 하드 드라이브를 클릭 합니다.](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. 6 단계에서 및 **매핑 파일에 액세스할 수 있는** **I 했을 때 내 하드 드라이브에 사용 되 고 필요한 드라이브 저널 파일에 액세스할 수 있는** 확인란을 클릭 하 고 **** 을 클릭 합니다.
    
    ![6 단계에서 두 확인란을 클릭 합니다.](media/fad43078-ea68-4acd-b2ed-75a800183262.png)
  
7. **드라이브 파일 선택** 페이지에서 **드라이브 파일을 선택**을 클릭 하 고 WAImportExport.exe 도구가 위치한 동일한 폴더로 이동 합니다. 2 단계에서에서 만든 저널 파일이이 폴더에 복사 되었습니다.
    
    ![드라이브를 선택 파일 WAImportExport.exe 도구를 실행 했을 때 만들어진 저널 파일을 제출 하려면 클릭](media/1ea35c04-bd88-4d7e-b7d9-dc390149d94f.png)
  
8. 저널 파일;를 선택 합니다. 예, `PSTHDD1.jrn`합니다.
    
    > [!TIP]
    > 저널 파일의 이름으로 지정 된 2 단계에서에서 WAImportExport.exe 도구를 실행 했을 때의 `/j:` 매개 변수입니다. 
  
9. 드라이브 파일의 이름을 **드라이브에**파일 이름을 표시 한 후 드라이브 파일에서 오류를 확인 하려면 **유효성 검사** 클릭 합니다. 
    
    ![선택한 드라이브 파일의 유효성을 검사 하려면 유효성 검사를 클릭 합니다.](media/4b707f5a-152a-4e74-b9f5-449c88d1fec4.png)
  
    PST 가져오기 작업을 만들려면 성공적으로 유효성을 검사 하는 드라이브 파일. 참고 파일 이름은 유효성을 검사 성공적으로 후 녹색으로 변경 됩니다. 유효성 검사에 실패 하는 경우에 **로그 보기** 링크를 클릭 합니다. 유효성 검사 오류 보고서를 파일에 실패 한 이유 하는 방법에 대 한 정보가 포함 된 오류 메시지와 함께 열릴 합니다. 
    
    > [!NOTE]
    > 추가 하 고 Microsoft에 제공 하는 각 하드 드라이브에 대 한 저널 파일의 유효성을 검사 해야 합니다. 
  
10. 추가 하 고 Microsoft에 제공 하는 각 하드 드라이브에 대 한 저널 파일 유효성 검사를 한 후 **다음**을 클릭 합니다.
    
11. 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 3 단계에서에서 만든 PST 가져오기 매핑 파일을 제출 **매핑 파일을 선택** 합니다. 
    
    ![가져오기 작업에 대해 만든 CSV 파일을 제출 선택 매핑 파일을 클릭 합니다.](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
12. CSV 이름 후 파일 아래에 표시 **파일 이름 매핑 (영문)** **유효성 검사** 오류에 대 한 CSV 파일을 확인 하려면를 클릭 합니다. 
    
    ![유효성 검사 오류에 대 한 CSV 파일을 확인 하려면 클릭](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    PST 가져오기 작업을 만들려면 성공적으로 유효성을 검사 하려면 CSV 파일에 있습니다. 참고 파일 이름은 유효성을 검사 성공적으로 후 녹색으로 변경 됩니다. 유효성 검사에 실패 하는 경우에 **로그 보기** 링크를 클릭 합니다. 실패 한 파일의 각 행에 대 한 오류 메시지와 함께 유효성 검사 오류 보고서가 열릴 합니다. 
    
13. PST 매핑 파일을 성공적으로 확인 한 후 **다음**을 클릭 합니다.
    
14. **연락처 정보 제공** 페이지에서 해당 상자에 연락처 정보를 입력 합니다. 
    
    메모를 하드 드라이브를 제공 하는 Microsoft 위치에 대 한 주소 표시 됩니다. Office 365 데이터 센터 위치에 따라 자동으로 생성 된이 주소에서 됩니다. 이 주소는 파일을 복사 하거나 스크린샷을 수행 합니다.
    
15. 사용 약관 문서를 읽고 있는 확인란을 클릭 다음 가져오기 작업을 제출 하려면 **저장** 을 클릭 합니다. 
    
    가져오기 작업을 성공적으로 만들면 프로세스를 전달 하는 드라이브의 다음 단계를 설명 하는 상태 페이지가 표시 됩니다.
    
16. **가져오기** 페이지에서 다음을 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 를 **새로 고칠** 가져오기 작업의 목록에서 가져오기 작업을 전달 하는 새 드라이브를 표시 합니다. Note 상태가 **추적 번호에 대 한 대기**하는 상태로 설정 됩니다. 가져오기 작업에 대 한 자세한 정보를 포함 하는 상태 플라이 아웃 페이지를 표시 하려면 가져오기 작업을 선택할 수도 있습니다.
 
## <a name="step-5-ship-the-hard-drive-to-microsoft"></a>5단계: Microsoft로 하드 드라이브 발송

다음 단계는 Microsoft로 하드 드라이브를 제공 하 고 다음 배송에 대 한 추적 번호를 제공 하 고 드라이브 전달 작업에 대 한 배송 정보를 반환 하는 것입니다. 드라이브를 Microsoft에서 받은 후 걸립니다 데이터에 대 한 7 10 비즈니스 일 사이의 조직에 대 한 Azure 저장소 영역에 PST 파일을 업로드 하려면 센터 담당자입니다.
  
> [!NOTE]
> 추적 번호 및 가져오기 작업 만들기 (영문)의 14 일 이내에 반환 배송 정보를 제공 하지 않으면 가져오기 작업 만료 됩니다. 가져오기 작업을 전달 하 여 새 드라이브를 만들려는 해야 이러한 상황이 발생 하는 경우 (참조 [4 단계: Office 365에서 PST 가져오기 작업 만들기](use-drive-shipping-to-import-pst-files-to-office-365.md#step4)) 및 드라이브 파일과 PST 가져오기 매핑 파일을 다시 제출 합니다. 
  
### <a name="ship-the-hard-drive"></a>하드 드라이브 발송

Microsoft로 하드 드라이브를 발송할 때는 다음 사항에 유의하세요.
  
- SATA-USB 어댑터; 제공 하지 마십시오 하드 드라이브를 제공 해야 합니다.
    
- 드라이브를 제대로 포장했는지 확인합니다(예: 정전기 방지 포장 백 또는 완충 비닐 사용).
    
- 선택한 배송업체를 사용하여 Microsoft로 하드 드라이브를 발송합니다.
    
- 4 단계에서에서 가져오기 작업을 만들 때 표시 된 Microsoft 위치에 대 한 주소 하드 드라이브를 제공 합니다. 배송 주소에서 "Office 365 가져오기 서비스"를 포함 해야 합니다.
    
- 하드 드라이브를 발송한 후 추적 번호와 운송업체 이름을 적어 둡니다. 다음 단계에 이러한 정보를 제공합니다.
    
### <a name="enter-the-tracking-number-and-other-shipping-information"></a>추적 번호 및 기타 발송 정보 입력

Microsoft에 하드 드라이브를 발송한 후 가져오기 서비스 페이지에서 다음 절차를 완료합니다.
  
1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 왼쪽된 창에서 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.
    
3. **가져오기** 페이지에 대 한 추적 번호를 입력 하려는 드라이브 배송에 대 한 작업을 클릭 합니다. 
    
4. 상태 플라이 아웃 페이지 **번호를 추적 하는 입력**을 클릭 합니다.
    
5. 다음 발송 정보를 제공합니다.
    
1. **배달 통신사업자** Microsoft에 하드 드라이브를 제공 하는데 사용 하는 배달 통신 회사의 이름을 입력 합니다. 
    
2. **추적 번호** 하드 드라이브 배송에 대 한 추적 번호를 입력 합니다. 
    
3. **반환 통신사업자 계좌 번호** **통신사업자를 반환**하는 아래에 나열 하는 통신 회사에 대 한 조직의 계좌 번호를 입력 합니다. Microsoft는 사용 (및 청구)이이 계정에 다시 하드 드라이브를 제공 합니다. 참고 조직에서 미국 및 유럽, FedEx와 계정을 해 놓아야 합니다. 아시아 및 세계의 나머지 부분에서 조직 DHL와 계정을 있어야 합니다.
    
6. **저장**을 클릭하여 가져오기 작업에 대한 이 정보를 저장합니다. 
    
    **가져오기** 페이지에서 다음을 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로고침** 가져오기 작업을 전달 하 여 드라이브에 대 한 정보를 업데이트 합니다. 상태에서 **전송 드라이브**로 설정 되어있는지 확인 합니다.

## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>6 단계: 데이터를 필터링 하 고 PST 가져오기 작업 시작

하드 드라이브를 Microsoft에서 받은 후 **가져오기** 페이지에서 가져오기 작업에 대 한 상태 **받은 드라이브**를 변경 됩니다. 데이터 센터 담당자는 조직에 대 한 Azure 저장소 영역에 PST 파일을 업로드 하려면 저널 파일의 정보를 사용 합니다. 이 시점 상태 **가져오기-진행중**으로 변경 됩니다. 앞서 설명한 것 처럼 PST 파일을 업로드 하려면 하드 드라이브를 받은 후 7 ~ 10 일 사이의 걸립니다.
  
PST 파일 Azure에 업로드 된 후 **진행중에서**분석의 상태가 변경 됩니다. 이 Office 365는를 분석 하 PST 파일의 데이터 (을 안전 하 게 방식으로) PST 파일에 포함 된 다양 한 메시지 형식과 항목의 보존 기간을 식별할 수를 나타냅니다. 분석이 완료 되 고 데이터를 가져올 준비가 되었습니다를 가져오기 작업에 대 한 상태는 **분석 완료**로 변경 됩니다. 이 시점 PST 파일에 포함 된 모든 데이터를 가져오려면 옵션이 제공 하거나 데이터를 가져온 가져옵니다을 제어 하는 필터를 설정 하 여 가져온 데이터를 자를 수 있습니다.
  
1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 왼쪽된 창에서 **데이터 관리**를 클릭 > **가져오기**.
    
3. **가져오기** 페이지에서 4 단계에서에서 만든 가져오기 작업에 대 한 **Office 365로 가져올 준비** 를 클릭 합니다. 
    
    ![만든 가져오기 작업 옆에 있는 Office 365로 가져올 준비를 클릭 합니다.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    페이지 날아가기 PST 파일에 대 한 정보 및 가져오기 작업에 대 한 기타 정보가 표시 됩니다.
    
4. **Office 365에 가져오기**를 클릭 합니다.
    
5. **데이터를 필터링** 페이지가 표시 됩니다. Office 365를 데이터의 기간에 대 한 정보를 비롯 하 여 PST 파일에 수행 하 여 분석에서 발생 하는 데이터 인 사이트를 포함 합니다. 이 시점 그대로 모든 데이터를 가져오거나 가져올 하는 데이터를 필터링 옵션이 제공 됩니다. 
    
    ![PST 파일의 데이터를 높이고 또는 모두를 가져올 수 있습니다.](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
6. 다음 중 하나를 수행합니다.
    
    a. 가져올 데이터를 높이고, 하려면 **예를 가져오기 전에으로 필터링 합니다.** 를 클릭 합니다.
    
    PST 파일의 데이터를 필터링 하 고 다음 가져오기 작업을 시작 하는 방법에 대 한 자세한 단계별 지침은 [Office 365에 PST 파일을 가져올 때 데이터를 필터링](filter-data-when-importing-pst-files.md)을 참조 하십시오.
    
    또는
    
    b. PST 파일에서 모든 데이터를 가져오려면를 **아니오, 모든 작업을 가져오려면** 클릭 하 고 **** 을 클릭 합니다.
    
7. 모든 데이터를 가져오려면 선택한 경우에 가져오기 작업을 시작 하려면 **데이터 가져오기** 를 클릭 합니다. 
    
    가져오기 작업의 상태 **가져오기** 페이지에 표시 됩니다. 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로고침** **상태** 열에 표시 되는 상태 정보를 업데이트 합니다. 가져올 각 PST 파일에 대 한 상태 정보를 표시 하는 상태 플라이 아웃 페이지를 표시 하려면 가져오기 작업을 클릭 합니다. 가져오기가 완료 되 고 사용자 사서함에 PST 파일을 가져온를 상태가 **완료**로 변경 됩니다.

## <a name="view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Office 365에 업로드 된 PST 파일의 목록 보기

설치 하 고 (즉, 무료, 공개 소스 도구) Microsoft Azure 저장소 탐색기를 사용 하 여 되는 업로드 (Microsoft 데이터 센터 담당자) 하 여 조직에 대 한 Azure 저장소 영역으로 PST 파일의 목록을 볼 수 있습니다. Microsoft로 전송 하는 하드 드라이브에서 PST 파일은 Azure 저장소 영역에 성공적으로 업로드 된 확인 하려면이 옵션을 수행할 수 있습니다.
  
Microsoft Azure 저장소 탐색기 미리 보기에서 됩니다.
  
 **중요:** Azure 저장소 탐색기를 사용 하 여 업로드 하거나 PST 파일을 수정 하려면 수는 없습니다. Office 365에 PST 파일을 가져오기 위한 유일한 방법은 지원된 AzCopy를 사용 하는 것입니다. 또한 Azure blob를 업로드 한 PST 파일을 삭제할 수 없습니다. PST 파일을 삭제 하려고 하는 경우 필요한 사용 권한을 있지 않은 경우에 대 한 오류가 표시 됩니다. 참고 모든 PST 파일 Azure 저장소 영역에서 자동으로 삭제 됩니다. 진행 중인 가져오기 작업이 다음 모든 PST 파일의 경우는 * * ingestiondata * * 컨테이너 30 일 가장 최근의 가져오기 작업을 만든 후에 삭제 됩니다. 
  
Azure 저장소 탐색기를 설치 및 Azure 저장소 영역에 연결 합니다.
  
1. 조직에 대 한 공유 액세스 서명 (SAS) URL을 얻으려면 다음 단계를 수행 합니다. 이 URL은 조직 및 SAS 키에 대 한 Microsoft 클라우드 Azure 저장소 위치에 대 한 네트워크 URL의 조합입니다. 이 키를 조직의 Azure 저장소 위치에 액세스 하려면 필요한 권한을 제공 합니다.
    
1. 이동 [https://protection.office.com/](https://protection.office.com/) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **가져오기**.
    
3. **가져오기** 페이지에서 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새로 만들기 작업을 가져옵니다**.
    
4. 가져오기 작업 마법사에서 PST 가져오기 작업에 대 한 이름을 입력 하 고 **** 을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄만 사용 합니다. 맞춤법 검사 시 대문자로 사용 하거나 이름에 공백을 포함할 수 없습니다.
    
5. **Choose 가져오기 작업 유형** 페이지에서 **데이터를 업로드** 를 클릭 하 고 **** 을 클릭 합니다.
    
6. 2 단계에서 **네트워크 업로드 SAS URL 표시**를 클릭 합니다.
    
7. URL이 표시 되 면 복사 하 고 파일에 저장 합니다. 전체 URL을 복사 해야 합니다.
    
    > [!IMPORTANT]
    > SAS URL을 보호 하기 위한 예방 조치를 수행 해야 합니다. 이 하는데 사용할 수 누구나 조직에 대 한 Azure 저장소 영역에 액세스 합니다. 
  
8. 가져오기 작업 마법사를 닫으려면 **취소** 를 클릭 합니다. 
    
2. 다운로드 하 고 [Microsoft Azure 저장소 탐색기 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 설치 합니다.
    
3. Microsoft Azure 저장소 탐색기를 시작 하 고 왼쪽된 창에서 **계정 저장소를** 마우스 오른쪽 단추로 클릭 **Azure 저장소에 대 한 연결**을 클릭 합니다.
    
    ![저장소 계정을 마우스 오른쪽 단추로 클릭 하 고 Azure 저장소에 연결을 클릭 한 다음](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
4. **공유 액세스 서명 (SAS) URI 또는 연결 문자열 사용** 을 클릭 하 고 **** 을 클릭 합니다.
    
5. **SAS URI를 사용**을 클릭 하 고 **URI**아래에 있는 상자에서를 1 단계에서 구한 SAS URL을 붙여넣습니다 **다음**을 클릭 합니다.
    
6. **연결 요약** 페이지에서 연결 정보를 검토 하 고 **연결**을 클릭 수 있습니다.
    
    **Ingestiondata** 컨테이너를 열 수 있습니다. 하드 드라이브에서 PST 파일을 포함 합니다. **Ingestiondata** 컨테이너는 **저장소 계정** 아래에 \> **(SAS-Attached 서비스)** \> **Blob 컨테이너**입니다.
    
    ![Azure 저장소 탐색기는 사용자가 업로드한 PST 파일 목록이 표시됩니다.](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
7. Microsoft Azure 저장소 탐색기를 사용 하 여이 끝나면 **ingestiondata**마우스 오른쪽 단추로 클릭 하 고 Azure 저장소 영역에서 연결을 끊으려면 **분리** 클릭 합니다. 그렇지 않은 경우 받게 오류가 다음에 연결 하려고 하면 됩니다. 
    
    ![수집을 마우스 오른쪽 단추로 클릭하고 분리를 클릭하여 Azure 저장소 영역에서 연결 끊기](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  

  
## <a name="troubleshooting-tips"></a>문제 해결 팁
<a name="troubleshootingtips"> </a>

- **PST 가져오기 CSV 매핑 파일에서 오류 때문에 가져오기 작업이 실패 하면 어떻게 됩니까?** 매핑 파일의 오류로 인해 실패 하면 가져오기 작업을 다시 새 가져오기 작업을 만들기 위해 Microsoft에 하드 드라이브를 제공할 필요가 없습니다. 조직에 대 한 Azure 저장소 영역에 이미 업로드 한 드라이브 전달 가져오기 작업에 대 한 하면가 제출 하는 하드 드라이브에서 PST 파일 때문입니다. 이 경우 방금 해야 PST 가져오기 CSV 매핑 파일에서 오류를 수정 하 고 다음 새 "네트워크 업로드" 가져오기 작업을 만들고 수정 된 CSV 매핑 파일을 전송 합니다. 참조를 만들고 새 네트워크 업로드 가져오기 작업을 시작 하려면 [5 단계: Office 365에서 PST 가져오기 작업 만들기](use-network-upload-to-import-pst-files.md#step-5-create-a-pst-import-job-in-office-365) 및 [6 단계: 데이터를 필터링 하 고 PST 가져오기 작업을 시작](use-network-upload-to-import-pst-files.md#step-6-filter-data-and-start-the-pst-import-job) 항목 "사용 하 여 네트워크 업로드 Office 365로 PST 파일을 가져올 수 있습니다." 
    
    > [!NOTE]
    > 해결 하기 위해 PST 가져오기 CSV 매핑 파일을 [Azure 저장소 탐색기](#view-a-list-of-the-pst-files-uploaded-to-office-365) 도구를 사용 하 여 Azure 저장소 영역에 업로드 된 하드 드라이브에서 PST 파일에 대 한 **ingestiondata** 컨테이너에 폴더 구조를 볼 수 있습니다. FilePath 매개 변수에서 잘못 된 값 매핑 파일 오류는 일반적으로 발생 하 고 있습니다. 이 매개 변수는 Azure 저장소 영역에서 PST 파일의 위치를 지정합니다. FilePath 매개 변수에서 [3 단계에서](#step-3-create-the-pst-import-mapping-file)에서 테이블에 대 한 설명을 참조 하십시오. 앞에서 설명한 것 처럼 Azure 저장소 영역에서 PST 파일의 위치를 하 여 지정 된는 `/dstdir:` [2 단계에서](#step-2-copy-the-pst-files-to-the-hard-drive)에서 WAImportExport.exe 도구를 실행 했을 때 매개 변수입니다. 
  

  
## <a name="more-information"></a>추가 정보

- 드라이브 전달은 조직에 사용할 수 있는 규정 준수 기능을 활용 하는 Office 365에 많은 양의 보관 메시징 데이터를 가져올 수 있는 효과적인 방법입니다. 사용자 사서함에 보관 데이터를 가져온 후에 다음을 수행할 수 있습니다.
    
  - [보관 사서함](enable-archive-mailboxes.md) 및 사용자에 게 추가 사서함 저장 공간 데이터에 대 한 [보관 자동 확장](enable-unlimited-archiving.md) 을 사용 하도록 설정 합니다. 
    
  - 사서함 데이터를 유지할 [소송 보존](https://go.microsoft.com/fwlink/?linkid=856286) 에 배치 합니다. 
    
  - Microsoft [eDiscovery 도구](search-for-content.md) 를 사용 하 여 데이터를 검색 합니다. 
    
  - 데이터는 유지 하는 기간 및 보존 기간이 만료 후 수행할 동작을 제어 하려면 [Office 365 보존 정책](retention-policies.md) 을 적용 합니다. 
    
  - [Office 365 감사 로그](search-the-audit-log-in-security-and-compliance.md) 를 검색이이 데이터에 관련 된 이벤트가 있습니다. 
    
  - 규정 준수를 위해 데이터를 보관 하려면 [비활성 사서함](create-and-manage-inactive-mailboxes.md) 데이터를 가져옵니다. 
    
  - 중요 한 정보의 [데이터](data-loss-prevention-policies.md) 손실을 조직을 보호 합니다. 
    
- 다음은 보안 저장소 계정 키와 BitLocker 암호화 키의 예입니다. 이 예에는 PST 파일을 하드 드라이브에 복사하기 위해 실행하는 WAImportExport.exe 명령 구문도 포함되어 있습니다. 암호나 기타 보안 관련 정보를 보호하는 것처럼 특히 주의해서 이러한 항목을 보호해야 합니다.
    

    ```
    Secure storage account key: 

    yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==

    BitLocker encryption key:

    397386-221353-718905-535249-156728-127017-683716-083391

  COMMAND SYNTAX

  First time:

  WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>

  Subsequent times:

  WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 

  EXAMPLES

  First time:

  WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER1\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"

  Subsequent times:

  WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER1\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```
   
- 앞에서 설명한 것 처럼 Office 365 가져오기 서비스 설정 (한 무기한 기간) 사서함에 PST 파일을 가져온 후 보존 대기 상태를 설정 합니다. 즉, *RentionHoldEnabled* 속성이로 설정 된 `True` 사서함에 할당 된 보존 정책 않습니다 처리할 수 있도록 합니다. 삭제 또는 보관 정책을 삭제 하거나 오래 된 메시지를 보관할 수 없도록 하 여 새로 가져온 메시지를 관리 하는 사서함 소유자 시간을 제공 합니다. 이 보존 대기 상태를 관리 하기 위해 수행할 수 있는 일부 단계는 다음과 같습니다. 
    
  - 특정 기간 동안 시간을 한 후 해제할 수 보존 대기를 실행 하 여는 `Set-Mailbox -RetentionHoldEnabled $false` 명령 합니다. 자세한 내용은 [사서함 보존에 원본 위치 유지](https://go.microsoft.com/fwlink/p/?LinkId=544749)를 참조 하십시오.
    
  - 나중에 일부 날짜 꺼져 있도록 보존 대기를 구성할 수 있습니다. 실행 하 여이 작업을 수행 된 `Set-Mailbox -EndDateForRetentionHold <date>` 명령 합니다. 예, 오늘 날짜가 2016 년 7 월 1 일이 고 30 일에서 해제 된 보존 대기 원하는 이라고 가정할 다음 명령을 실행 합니다: `Set-Mailbox -EndDateForRetentionHold 8/1/2016`합니다. 이 시나리오에서는 *RentionHoldEnabled* 속성이 *True* 로 설정 남게 됩니다. 자세한 내용은 [Set-mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317)를 참조 하십시오.
    
  - 오래 된 항목을 가져오지 않습니다 수 즉시 삭제 되거나 사용자의 보관 사서함으로 이동 되도록 사서함에 할당 된 보존 정책에 대 한 설정을 변경할 수 있습니다. 예, 사서함에 할당 된 삭제 또는 보관 정책에 대 한 보존 기간을 길게 수 있습니다. 이 시나리오에서는 있습니다 기능을 해제는 사서함에 보존 대기 상태에는 보존 정책의 설정을 변경한 후 합니다. 자세한 내용은 [Office 365 조직 내의 사서함에에서는 보관 및 삭제 정책 설정](set-up-an-archive-and-deletion-policy-for-mailboxes.md)을 참조 하십시오.
    

  

