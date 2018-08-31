---
title: 네트워크 업로드를 사용하여 RMS 암호화 PST 파일을 Office 365로 가져오기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 84a595b8-cd77-4f66-ac52-57a33ddd4773
description: Office 365에서 사용자 사서함에 RMS 암호화 PST 파일을 가져오려면 네트워크 업로드를 사용 하는 방법에 알아봅니다.
ms.openlocfilehash: 6460512e2d6085df684841248dc286d39dbd9d87
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534114"
---
# <a name="use-network-upload-to-import-rms-encrypted-pst-files-to-office-365"></a>네트워크 업로드를 사용하여 RMS 암호화 PST 파일을 Office 365로 가져오기

**이 문서는 관리자입니다. 자신의 사서함에 PST 파일을 가져올 하려고 합니까? [가져오기 전자 메일, 연락처 및 일정 Outlook.pst 파일에서](https://go.microsoft.com/fwlink/p/?LinkID=785075) 를 참조 하십시오.**
   
네트워크를 사용 하 여 사용자 사서함에 PST 파일을 가져오려면 옵션 및 Office 365를 가져올 서비스에 업로드 합니다. 네트워크 업로드는 업로드 PST 파일 Microsoft 클라우드에서 임시 저장 영역을 의미 합니다. 그런 다음 Office 365 가져오기 서비스 대상 사용자 사서함에 저장 영역에서 PST 파일을 복사 합니다. 가져오기 서비스의 새로운 기능을 통해 업로드 하는 Microsoft 클라우드에 저장 하기 전에 PST 파일을 암호화할 수 있습니다. 이러한 파일을 사용자 사서함을 가져올 때 되지 않은 crypted 없게 됩니다. 
  
암호화 하 여 Office 365 사서함에 PST 파일을 가져올 필요한 단계는 다음과 같습니다.
  
[1단계: PST 가져오기를 위한 Azure 권한 관리 설정 ](#step-1-set-up-azure-rights-management-for-pst-import)

[2단계: PST 가져오기를 위한 암호화 키 생성](#step-2-generate-an-encryption-key-for-pst-import)

[3 단계: RMS 테 넌 트 ID 및 라이선스 URL 가져오기](#step-3-obtain-rms-tenant-id-and-licensing-url)

[PST 가져오기 도구를 다운로드 하 고 SAS URL을 복사 하는 4 단계:](#step-4-download-the-pst-import-tools-and-copy-the-sas-url)

[5 단계: 암호화 하 고 Office 365에 PST 파일을 업로드 합니다.](#step-5-encrypt-and-upload-your-pst-files-to-office-365)

[(선택 사항) Office 365에 보기 PST 파일의 목록이 업로드 6 단계:](#optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365)

[7 단계: PST 가져오기 매핑 파일 만들기](#step-7-create-the-pst-import-mapping-file)

[8단계: Office 365에서 PST 가져오기 작업 만들기](#step-8-create-a-pst-import-job-in-office-365)
  
> [!IMPORTANT]
> 암호화 하 여 Office 365 사서함에 PST 파일을 가져올-를 설정 하 고 조직 구성 단계 4를 한번만 1 단계를 수행 해야 합니다. 다음이 단계를 수행 하 고 나면 단계 5 ~ 8 단계 암호화, 업로드 하 고, 가져올 PST 파일의 일괄 처리를 사용할 때마다를 수행 합니다. 
  
Office 365로 데이터 가져오기 (영문) 하는 방법에 대 한 자세한 내용은 [Office 365로 조직 PST 파일 가져오기 (영문)의 개요](importing-pst-files-to-office-365.md)를 참조 하십시오.
  
## <a name="before-you-begin"></a>시작하기 전에

- 역할을 할당 사서함 가져오기 내보내기 Exchange 온라인 Office 365 사서함에 PST 파일을 가져오려면 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 다음 자신을 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹](https://go.microsoft.com/fwlink/p/?LinkId=730688)에 "역할 그룹 만들기" 섹션이 있습니다.
    
    또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.
    
  - 역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.
    
    또는
    
  - Office 365 조직에서 전역 관리자 여야 해야 합니다.
    
  > [!TIP]
  > Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다. 
  
- 파일 서버 또는 조직에 있는 공유 폴더에서 Office 365로 가져올 PST 파일을 저장 해야 합니다. 5 단계에서에서 암호화 되며이 파일 서버에 저장 된 또는 Office 365에 폴더를 공유 하 고 PST 파일을 업로드 하는 Office 365 ImportTool를 실행할 수 있습니다.
    
- 이 절차를 복사 하 고 암호화 키, 저장소 키 및 다양 한 식별 키와 Url의 복사본을 저장 하는 것입니다. 이 정보를 암호화 하 여 PST 파일을 업로드할 5 단계에서에서 사용 됩니다. 암호 또는 기타 보안 관련 정보를 보호 하는 동일 하 게 이러한 방금 보호 하기 위한 예방 조치를 수행 해야 합니다. 예: 암호로 보호 된 Microsoft Word 문서에 저장 또는 암호화 된 USB 드라이브에 저장 수 있습니다. 이러한 키, Id, 및 Url의 예에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 
    
- Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니다. 비활성 사서함의 GUID를 지정 하 여이 작업을 수행 된 `Mailbox` PST 가져오기 매핑 파일에서 매개 변수입니다. 자세한 내용은 [7 단계를](#step-7-create-the-pst-import-mapping-file) 참조 하십시오. 
    
- Exchange 하이브리드 배포에서 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져올 수 있습니다. PST 가져오기 매핑 파일에서 다음을 수행 하 여이 수행 합니다.
    
  - 사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 된 `Mailbox` 매개 변수입니다. 
    
  - **TRUE** 값을 지정 된 `IsArchive` 매개 변수입니다. 
    
    자세한 내용은 [7 단계를](#step-7-create-the-pst-import-mapping-file) 참조 하십시오. 
    
- PST 파일을 Office 365 사서함으로 가져온 후 사서함에 대 한 설정 보존 대기는 무기한 기간에 대 한 켜 집니다. 즉, 사서함에 할당 된 보존 정책 보존 보류 해제 하거나 보류를 해제 하려면 날짜를 설정할 때까지 처리 되지 않습니다. 이유 해야 할까요? 오래 된 메시지를 사서함으로 가져온 경우 이러한 수 영구적으로 삭제 됩니다 (비우기)가 보존 기간이 만료 되었기 때문에 사서함에 대해 구성 된 보존 설정에 따라 합니다. 사서함을 보존 대기 배치 이러한 새로 가져온 메시지 또는 사서함에 대 한 보존 설정을 변경 하려면 시간 부여를 관리 하는 사서함 소유자 시간을 제공 합니다. 보존 대기 상태를 관리 하는 방법에 대 한 제안에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 
    
- Office 365를 업로드 하기 전에 PST 파일을 암호화 하는데 필요 하지 않으면, [Office 365에 PST 파일을 가져오려면 업로드 사용 하 여 네트워크](use-network-upload-to-import-pst-files.md)를 참조 하십시오.
    
- Office 365에 PST 파일을 가져오려면 네트워크 업로드를 사용 하는 방법에 대 한 질문과 대답 [PST 파일을 Office 365로 가져오기 (영문) 하는 방법에 대 한 FAQ](faqimporting-pst-files-to-office-365.md)를 참조 하십시오.
  
## <a name="step-1-set-up-azure-rights-management-for-pst-import"></a>1단계: PST 가져오기를 위한 Azure 권한 관리 설정 

PST 가져오기 Office 365에서 Azure 권한 관리 (Azure RMS) 서비스에서 제공 하는 암호화 기능을 사용 합니다. 이 통해 Office 365를 업로드 하기 전에 PST 파일을 암호화할 수 있습니다. 
  
Azure RMS PST 가져오기에 대 한 구성 세 단계로 구성 됩니다.
  
- [Azure RMS를 활성화합니다.](#activate-azure-rms)
    
- [RMS in Exchange Online 구성](#configure-rms-in-exchange-online)
    
- [Active Directory의 RMS 클라이언트를 설치합니다.](#install-the-active-directory-rms-client)
    
### <a name="activating-azure-rms"></a>Azure RMS를 활성화합니다.

기본적으로 azure RMS 더이상 사용할 수 없지만 또는 다른 관리자가 조직에서 수 활성화 한 것입니다. 설치 하 고 Azure DRM을 활성화 하려면 [Azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) 지침을 따릅니다.
  
### <a name="configuring-rms-in-exchange-online"></a>RMS in Exchange Online 구성

권한 관리 서비스를 활성화 한 후 다음 단계를 권한 관리 IRM (정보) Azure RMS를 사용 하 여 온라인 Exchange 설정 하는 것입니다. 자세한 내용은 [Azure 권한 관리를 사용 하 여 IRM 구성](https://go.microsoft.com/fwlink/p/?LinkId=394816)을 참조 하십시오.
  
1. [원격 PowerShell을 사용 하는 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkId=396554 )합니다.
    
2. 다음 명령을 실행하여 RMS 키 공유 URL을 설정합니다.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation <RMS key sharing location>
    ```

    다음 표를 사용하여 조직의 위치에 대한 올바른 RMS 키 공유 위치를 확인합니다.
    
    |**위치**|**RMS 키 공유 위치**|
    |:-----|:-----|
    |북미  <br/> | `https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |유럽 연합  <br/> | `https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |아시아  <br/> | `https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |남미  <br/> | `https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Office 365 Government(정부 커뮤니티 클라우드)  <br/> | `https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>1</sup> <br/> |
   
    > [!NOTE]
    > <sup>1</sup> Government Sku (정부 커뮤니티 클라우드)에 대 한 Office 365를 구입한 고객만이 RMS 키 공유 위치를 사용 해야 합니다. 
  
    예,이 명령은 RMS Online 키 공유 위치 Exchange 온라인 북미에 있는 고객에 대 한 구성 합니다.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
    ```

3. RMS Online에서 Office 365 조직에는 신뢰할 수 있는 도메인 TPD (게시)를 가져오려면 다음 명령을 실행 합니다. 
    
    ```
    Import-RMSTrustedPublishingDomain -RMSOnline -Name "RMS Online"
    ```

    TPD에는 PST 파일 암호화를 비롯하여 조직에서 RMS 기능을 사용하는 데 필요한 설정이 포함되어 있습니다.  
    
4. Office 365 조직에 대 한 IRM을 사용 하도록 설정 하려면 다음 명령을 실행 합니다.
    
    ```
    Set-IRMConfiguration -InternalLicensingEnabled $true
    ```

### <a name="installing-the-active-directory-rms-client"></a>Active Directory의 RMS 클라이언트를 설치합니다.

이 섹션의 마지막 단계 2.1 서비스 RMS (권한 관리) 클라이언트를 다운로드 하는 것입니다. 이 소프트웨어 Azure RMS에 대 한 액세스를 보호 하는데 도움이 됩니다 및 정보를 암호화 하 여 5 단계에서에서 PST 파일을 업로드할 사용할 하는 동일한 컴퓨터에서 RMS 클라이언트 Azure RMS. 설치를 사용 하는 응용 프로그램을 통해 흐름을 보호 합니다. 
  
1. [권한 관리 서비스 클라이언트 2.1을](https://www.microsoft.com/en-us/download/details.aspx?id=38396)다운로드 합니다.
    
2. Active Directory 권한 관리 서비스 클라이언트 2.1 마법사를 실행하여 클라이언트를 설치합니다.

## <a name="step-2-generate-an-encryption-key-for-pst-import"></a>2단계: PST 가져오기를 위한 암호화 키 생성

Azure RMS 설정한 후 다음 단계에서는 Office 365에 업로드 하는 PST 파일을 암호화 하는데 사용 되는 (대칭 키 라고 함) 암호화 키를 생성 하는 것입니다. Azure Active Directory에서 사용자를 서비스로 PST 가져오기 서비스를 추가 하 여이 작업을 수행 합니다. 5 단계에서에서 Azure 저장소 위치로 PST 파일을 암호화 서비스 사용자를 업로드할 때 Azure Active Directory를 사용 하 여 직접 인증 PST 가져오기 서비스를 선택 하면으로이 응용 프로그램을 추가 합니다.
  
1. Windows PowerShell 용 Azure Active Directory 모듈을 시작 합니다.
    
2. 다음 명령을 실행하여 Microsoft Online 서비스에 연결합니다.
    
    ```
    Connect-MsolService
    ```

3. Office 365 조직에서 관리자 계정에 대 한 자격 증명을 입력 한 다음 **확인**을 클릭 합니다.
    
4. 다음 명령을 실행하여 암호화 키(대칭 키)를 생성합니다. 새 PST 암호화 보안 주체를 만들어 이 작업을 수행합니다.
    
    ```
    New-MsolServicePrincipal -DisplayName PstEncryptionPrincipal
    ```

    시스템에 새 PST 암호화 보안 주체에 대한 대칭 키 및 속성이 표시됩니다.
    
    ![표시되는 대칭 키 복사 및 저장](media/0003fdea-dace-41d2-b49d-f5c98c6230ca.png)
  
5. 대칭 키를 텍스트 또는 Word 파일에 복사합니다. 앞서 설명한 것처럼 특별히 주의해서 이 파일을 보호해야 합니다. 대칭 키는 이 경우에만 표시되므로 이 창을 스크린샷으로 캡처한 후 같은 파일에 저장하는 것도 도움이 될 수 있습니다.  
    
    > [!IMPORTANT]
    > PST 암호화 보안 주체를 만든 후에는 **Get-MsolServicePrincipal** cmdlet을 사용하여 대칭 키를 검색할 수 없습니다. 그래서 키를 저장해야 하는 것입니다. 
  
Open 및 Microsoft 온라인 서비스에 연결 된 Azure Active Directory 모듈에 대 한 Windows PowerShell을 유지 합니다. 명령을 실행 하는 다음 단계에서이 창에 표시 됩니다.

## <a name="step-3-obtain-rms-tenant-id-and-licensing-url"></a>3 단계: RMS 테 넌 트 ID 및 라이선스 URL 가져오기

다음 단계는 ID와 조직에 대 한 Azure RMS 서비스에 대 한 라이선스 위치 URL 테 넌 트를 가져옵니다. 복사 하 고 2 단계에서에서 대칭 키가 포함 된 동일한 파일에이 정보를 저장 합니다. ID 및 URL는 PST 파일을 암호화 하려면 5 단계에서에서 사용 됩니다.
  
1. (Microsoft 온라인 서비스에 연결 된)는 Windows PowerShell 용 Azure Active Directory 모듈을 Office 365 조직에서 Azure RMS 서비스에 연결 하려면 다음 명령을 실행 합니다.
    
    ```
    Connect-AadrmService 
    ```

2. Office 365 조직에서 관리자 계정에 대 한 자격 증명을 입력 한 다음 **확인**을 클릭 합니다.
    
3. Office 365 조직에서 Azure RMS 서비스에 대 한 테 넌 트 ID를 표시 하려면 다음 명령을 실행 합니다.
    
    ```
    Get-AadrmConfiguration | FL BPOSId
    ```

    복사 하 고 저장에 대 한 값은 `BPOSId` 속성입니다. 
    
4. Azure RMS 서비스에 대 한 라이선스 위치를 표시 하려면 다음 명령을 실행 합니다.
    
    ```
    Get-AadrmConfiguration | FL LicensingIntranetDistributionPointUrl
    ```

    복사 하 고 저장에 대 한 값은 `LicensingIntranetDistributionPointUrl` 속성입니다. 

## <a name="step-4-download-the-pst-import-tools-and-copy-the-sas-url"></a>PST 가져오기 도구를 다운로드 하 고 SAS URL을 복사 하는 4 단계:

이제 Azure RMS를 구성 하 고 PST 파일을 암호화 하는 데 필요한 Id를 확보 했을 때 다음 단계를 사용 하도록 다운로드 하 고 Office 365를 암호화 하려면 5 단계에서에서 실행 되 고 업로드 PST 파일을 하는 도구를 설치 합니다. 이러한 도구는 Azure AzCopy 도구와 Office 365 데이터 암호화 도구는 합니다. 또한 조직에 대 한 SAS URL을 복사할 수 있습니다. 이 URL은 조직 및 공유 액세스 서명 (SAS) 키에 대 한 Microsoft 클라우드 Azure 저장소 위치에 대 한 네트워크 URL의 조합입니다. 이 키는 Azure 저장소 위치에 PST 파일을 업로드 하려면 필요한 권한을 제공 합니다. 저장 동일한 파일에는 다른 정보를 2 단계와 3 단계에서 복사한 합니다. 앞서 설명한 것 처럼 SAS URL을 보호 하기 위해 예방 조치를 취하십시오. 
  
> [!IMPORTANT]
> 성공적으로 Azure 저장소 위치에 PST 파일을 업로드 하려면 Azure AzCopy 버전 5.0 사용 해야 합니다. 최신 버전의 AzCopy 도구는 Office 365에 PST 파일을 가져오기 위한 지원 되지 않습니다. 이 단계의 절차를 수행 하 여 **네트워크를 통해 파일 업로드** 페이지에서 AzCopy 도구를 다운로드 해야 합니다. 
  
1. 이동 [https://protection.office.com](https://protection.office.com)합니다.
    
2. Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 Office 365에 로그인 합니다.
    
3. 왼쪽된 창에서 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.
    
4. **가져오기** 페이지에서 **가져오기 서비스로 이동**을 클릭합니다.
    
5. **Office 365로 데이터 가져오기** 페이지에서 **새 작업** 을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif), **업로드 전자 메일 메시지 (PST 파일)를**클릭 하 고 있습니다.
    
6. 2 단계에서 **네트워크를 통해 파일 업로드** 페이지에서 **네트워크 업로드 SAS URL 표시**를 클릭 합니다.
    
7. URL이 표시 되 면 복사 하 고 다른 키를 저장 하 여 파일에 저장 합니다. 전체 URL을 복사 해야 합니다. 
    
8. 3 단계에서 다운로드 하 고 Azure AzCopy 도구를 설치 하려면 **Azure AzCopy 도구를 다운로드** 를 클릭 합니다. 
    
9. 팝업 창에서 **실행**을 클릭하여 Azure AzCopy 도구를 설치합니다. 
    
    > [!IMPORTANT]
    > 기본 위치, 즉에서 Azure AzCopy 도구를 설치 해야 `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` 하는 컴퓨터에서 64 비트 Windows를 실행 합니다. 5 단계에서에서의 O365ImportTool.exe를 실행 하는 경우을 찾고이 위치에서 AzCopy 도구 때문입니다. 
  
10. Azure AzCopy 도구를 설치한 후에 **Office 365 데이터 암호화 및 가져오기 도구를 다운로드**를 클릭 합니다.
    
11. 팝업 창에서 **저장** 을 클릭 \> 로컬 컴퓨터의 폴더에 O365ImportTool.zip 파일을 저장 하려면 **로 저장** 합니다. 
    
12. O365ImportTool.zip 파일의 압축을 풉니다.
    
13. **네트워크를 통해 파일 업로드** 페이지를 닫으려면 **취소** 를 클릭 합니다. 
 
## <a name="step-5-encrypt-and-upload-your-pst-files-to-office-365"></a>5 단계: 암호화 하 고 Office 365에 PST 파일을 업로드 합니다.

단계 1 ~ 4 단계를 완료 한 도구를 사용 하 여 O365ImportTool.exe를 암호화 하 여 Office 365에 PST 파일을 업로드할 준비가 된 것입니다. 이 도구 PST 파일을 암호화 하 고 업로드 하 고 Microsoft 클라우드에서는 Azure 저장소 위치에 저장 합니다. 이 단계를 완료 하려면 PST 파일에는 파일 공유 또는 조직에서 파일 서버에 배치 해야 합니다. 이 다음 절차에는 원본 디렉터리 이라고 합니다. O365ImportTool.exe 도구를 실행할 때마다 하겠습니다 지정할 수 있습니다 다른 원본 디렉터리입니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트를 엽니다.
    
2. 4단계에서 O365ImportTool.exe 도구를 설치한 디렉터리로 이동합니다.
    
3. 암호화 하 고 Office 365에 PST 파일을 업로드 하려면 다음 명령을 실행 합니다.
    
    ```
    O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL> /upload-destSAS:<SAS key>
    ```

    다음 표에서는 매개 변수와 해당 필수 값에 대해 설명합니다. 이전 단계에서 획득한 정보가 이러한 매개 변수의 값에 사용됩니다.
    
    |**매개 변수**|**설명**|**예제**|
    |:-----|:-----|:-----|
    | `/srcdir:` <br/> |Office 365로 업로드 됩니다 PST 파일을 포함 하 여 조직에서 원본 디렉터리를 지정 합니다.  <br/> | `/srcdir:\\FILESERVER01\PSTs` <br/> |
    | `/protect-rmsserver:` <br/> |Azure RMS 서비스에 대 한 라이선스 위치를 지정합니다. 값을 사용 하는 `LicensingIntranetDistributionPointUrl` 3 단계에서에서 얻은 속성입니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("")<br/> | `/protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing"` <br/> |
    | `/protect-tenantid:` <br/> |Azure RMS 조직의 id를 지정 합니다. 값을 사용 하는 `BPOSId` 3 단계에서에서 얻은 속성입니다.<br/> | `/protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b` <br/> |
    | `/protect-key:` <br/> |2 단계에서에서 구한 대칭 키를 지정 합니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").  <br/> | `/protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867="` <br/> |
    | `/transfer:` <br/> |네트워크를 통해 PST 파일을 업로드 또는 하드 드라이브에 보내줄 하 여부를 지정 합니다. 값 `upload` 네트워크를 통해이 파일을 업로드는 나타냅니다. 값 `drive` 하드 드라이브에는 Pst 제공를 나타냅니다.<br/> | `/transfer:upload` <br/> |
    | `/upload-dest:` <br/> |Office 365; PST 파일은 업로드 하는 위치에서 대상 지정 조직에 대 한 Azure 저장소 위치입니다. 이 매개 변수에 대 한 값 4 단계에서에서 복사한 SAS URL에서 네트워크 업로드 URL로 구성 됩니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").<br/><br/> **팁:** (선택 사항) 암호화 된 PST 파일을 업로드 하려면 Azure 저장소 위치에 하위 폴더를 지정할 수 있습니다. 네트워크 업로드 URL에 "ingestiondata") (이후 하위 폴더 위치를 추가 하 여이 작업을 수행 합니다. 첫번째 예제에서는; 하위 폴더를 지정 하지 않으면 즉, Azure 저장소 위치는 Pst ( *ingestiondata* 라는) 루트에 업로드 합니다. 두번째 예제 Azure 저장소 위치에서 ( *EncryptedPSTs* 라는) 하위 폴더에 PST 파일을 업로드 합니다.           | `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata"` <br/> 또는  <br/>  `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs"` <br/> |
    | `/upload-destSAS:` <br/> |조직에 대 한 SAS 키를 지정합니다. 4 단계에서에서 복사한 SAS URL에서 SAS 키의 값이 매개이 변수에 대 한 구성 됩니다. SAS 키의 첫 문자는 물음표 ("?"). 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").  <br/> | `/upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/recurse` <br/> |이 선택적 스위치 O365ImportTool.exe 도구에서는로 지정 된 원본 디렉터리의 하위 폴더에 있는 Pst 파일을 복사 되도록 재귀 모드를 지정 된 `/srcdir:` 매개 변수입니다.  <br/><br/> **참고:** 이 스위치를 포함 하는 경우 하위 폴더에서 PST 파일 다른 파일 경로 이름에에서 갖습니다 Azure 저장소 위치는 업로드 하 고 나면. 7 단계에서에서 만든 CSV 파일의 정확한 파일 경로 지정 해야 합니다.           | `/recurse` <br/> |
   
    다음은 각 매개 변수의 실제 값을 사용하는 O365ImportTool.exe 도구의 구문 예입니다.
    
    ```
    O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b  /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
    ```

    이 명령을 실행하면 PST 파일의 암호화 및 업로드 진행률을 보여 주는 상태 메시지가 표시됩니다. 마지막 상태 메시지는 성공적으로 암호화 및 업로드된 파일의 총 수를 표시합니다.  
    
    > [!TIP]
    > 성공적으로 O365ImportTool.exe 명령을 실행 하 고 매개 변수를 모두 올바른지 확인, 후 명령줄 구문 정보를 복사한 동일한 (보안) 파일의 복사본 저장 획득 이전 단계에서 합니다. 다음 복사 수 있으며를 암호화 하 여 Office 365에 PST 파일을 업로드할 O365ImportTool.exe 도구를 실행할 때마다 명령 프롬프트에서이 명령을 붙여넣습니다. 변경 해야할 유일한 값은에 대 한 것과 `/srcdir:` 및 `/upload-dest:` 매개 변수입니다. 
  
## <a name="optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(선택 사항) Office 365에 보기 PST 파일의 목록이 업로드 6 단계:

단계는 선택 사항으로 설치 하 고 (즉, 무료, 공개 소스 도구) Microsoft Azure 저장소 탐색기를 사용 하 여 Azure blob에 업로드 했을 때 PST 파일의 목록을 볼 수 있습니다. 이 작업을 수행 하는 이유에 세 가지가 있습니다.
  
- 공유 폴더 또는 조직에서 파일 서버에서 PST 파일은 Azure blob에 성공적으로 업로드 된 확인 합니다.

- PST 파일의 암호화를 확인 합니다. 암호화 된 PST 파일을 `.pfile` PST filename;에 추가 된 확장 예, `pilarp.pst.pfile`합니다.
    
- Azure blob를 업로드 한 각 PST 파일에 대 한 파일 이름 (및 하위 폴더 경로 이름을 하나를 포함 하는 경우)를 확인 합니다. 폴더 경로 각 PST 파일에 대 한 이름을 모두 지정 해야 하기 때문에 다음 단계에서 파일에 매핑 PST를 작성할 때 매우 유용 합니다. 이 이름 확인 (영문) PST 매핑 파일의 잠재적인 오류를 줄일 수 있습니다.
    
Microsoft Azure 저장소 탐색기 미리 보기에서 됩니다. 
  
 > [!IMPORTANT]
>  Azure 저장소 탐색기를 사용 하 여 업로드 하거나 PST 파일을 수정 하려면 수는 없습니다. Office 365에 PST 파일을 가져오기 위한 유일한 방법은 지원된 AzCopy를 사용 하는 것입니다. 또한 Azure blob를 업로드 한 PST 파일을 삭제할 수 없습니다. PST 파일을 삭제 하려고 하는 경우 필요한 사용 권한을 있지 않은 경우에 대 한 오류가 표시 됩니다. 참고 모든 PST 파일 Azure 저장소 영역에서 자동으로 삭제 됩니다. 없는 경우 진행 상황을 **ingestiondata** 컨테이너에 있는 다음 모든 PST 파일에 가져오기 작업이 30 일 가장 최근의 가져오기 작업을 만든 후 삭제 됩니다. 
  
Azure 저장소 탐색기를 설치 및 Azure 저장소 영역에 연결 합니다.
  
1. 다운로드 하 고 [Microsoft Azure 저장소 탐색기 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 설치 합니다.
    
2. Microsoft Azure 저장소 탐색기를 시작 하 고 왼쪽된 창에서 **계정 저장소를** 마우스 오른쪽 단추로 클릭 **Azure 저장소에 대 한 연결**을 클릭 합니다. 
    
    ![저장소 계정을 마우스 오른쪽 단추로 클릭 하 고 Azure 저장소에 연결을 클릭 한 다음](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. **Azure 저장소에**연결 상자에서 4 단계에서에서 구한 SAS URL 붙여넣은 **다음**을 클릭 합니다. 
    
    ![SAS URL Azure 저장소 페이지에 연결 상자에 붙여넣기](media/5d034128-e087-48e1-9ebc-4c9fa262d5b7.png)
  
4. **연결 요약** 페이지에서 연결 정보를 검토 하 고 **연결**을 클릭 수 있습니다. 
    
5. **저장소 계정**아래에서 **서비스 SAS ()** 노드를 확장 하 고 **Blob 컨테이너** 노드를 확장 합니다. 
    
6. **Ingestiondata**마우스 오른쪽 단추로 클릭 하 고 **Blob 컨테이너 편집기 열기**를 클릭 합니다.
    
    ![ingestiondata를 마우스 오른쪽 단추로 클릭한 다음 Blob 컨테이너 편집기 열기를 클릭합니다.](media/f50eee30-9202-4efc-904a-2895a0bc388d.png)
  
    Azure 저장소 영역 5 단계에서에서 업로드 PST 파일의 목록이 표시 됩니다.
    
    ![Azure 저장소 탐색기는 사용자가 업로드한 PST 파일 목록이 표시됩니다.](media/a448ae43-e744-4153-8304-22b59e93883c.png)
  
7. Microsoft Azure 저장소 탐색기를 사용 하 여이 끝나면 **ingestiondata**마우스 오른쪽 단추로 클릭 하 고 Azure 저장소 영역에서 연결을 끊으려면 **분리** 클릭 합니다. 그렇지 않은 경우 받게 오류가 다음에 연결 하려고 하면 됩니다. 
    
    ![수집을 마우스 오른쪽 단추로 클릭하고 분리를 클릭하여 Azure 저장소 영역에서 연결 끊기](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-7-create-the-pst-import-mapping-file"></a>7 단계: PST 가져오기 매핑 파일 만들기

PST 파일을 암호화 하 고 Office 365 조직에 대 한 Azure 저장소 위치에 업로드 한 후 다음 단계에 쉼표를 만들려는 구분 하 여 PST 파일을 가져올 수는 어떤 사용자 사서함을 지정 하는 값 (CSV) 파일입니다. PST 가져오기 작업을 만들 때에 다음 단계에는이 CSV 파일을 전송 됩니다.
  
1. [PST 가져오기 매핑 파일의 복사본을 다운로드](https://go.microsoft.com/fwlink/p/?LinkId=544717)합니다. 
    
2. CSV 파일을 열거나 로컬 컴퓨터에 저장합니다. 다음 예에서는 완료된 PST 가져오기 매핑 파일(메모장에서 열림)을 보여 줍니다. CSV 파일을 편집할 경우 Microsoft Excel을 사용하는 것이 훨씬 더 쉽습니다.
    
    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,,annb.pst.pfile,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,annb_archive.pst.pfile,annb@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,,donh.pst.pfile,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,donh_archive.pst.pfile,donh@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,pilarp.pst.pfile,pilarp@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,pilarp_archive.pst.pfile,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,tonyk.pst.pfile,tonyk@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,tonyk_archive.pst.pfile,tonyk@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,zrinkam.pst.pfile,zrinkam@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,zrinkam_archive.pst.pfile,zrinkam@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    ```

    첫째 행 또는 CSV 파일의 머리글 행을 사용자 사서함에 PST 파일을 가져오려면 PST 가져오기 서비스에서 사용 되는 매개 변수를 나열 합니다. 각 매개 변수 이름은 쉼표로 구분 됩니다. 각 행 머리글 행에서 특정 사서함에 PST 파일 가져오기 (영문)에 대 한 매개 변수 값을 나타냅니다. 가져올 사용자 사서함에는 각 PST 파일에 대 한 행을 할 수 있습니다. 실제 데이터와 매핑 파일의 개체 틀 데이터를 교체 해야 합니다.
    
    > [!NOTE]
    > SharePoint 매개 변수를 포함하여 머리글 행의 어떤 내용도 변경하지 않도록 합니다. 변경한 내용은 PST 가져오기 프로세스 동안 무시됩니다. 
  
3. 다음 표의 정보를 사용하여 CSV 파일을 필요한 정보로 채웁니다.
    
    |**매개 변수**|**설명**|**예제**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |데이터를 가져올 수는 Office 365 서비스를 지정 합니다. 사용자 사서함을 PST 파일을 가져오려면, 사용 `Exchange`합니다.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> |5 단계에서에서 PST 파일을 업로드 하는 Azure 저장소 위치에 폴더 위치를 지정 합니다.  <br/>  네트워크 URL에는 선택적 하위 폴더 이름을 포함 하지 않았으므로 하는 경우는 `/upload-dest:` 매개 변수 5 단계에서에서이 매개 변수를 비워둘 CSV 파일에 있습니다. 하위 폴더 이름을 포함 하는 경우이 매개 변수에서 지정 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다. 두 방법 모두에 대 한 값에 "ingestiondata"를 포함 *하지* 는 `FilePath` 매개 변수입니다.<br/> <br/>**중요:** 파일 경로 이름에 대 한 대/소문자에 SAS URL에는 선택적 하위 폴더 이름을 포함 하는 경우를 사용 하는 동일한 대/소문자 여야 합니다.의 `/upload-dest:` 5 단계에서에서 매개 변수입니다. 예: 사용 하는 경우 `EncryptedPSTs` 하위 폴더에 대 한 5 단계에서에서 이름을 지정 하 고 다음을 사용 `encryptedpsts` 에 `FilePath` CSV 파일의 매개 변수, PST 파일에 대 한 가져오기가 실패 합니다. 두 경우 모두 동일한 대/소문자를 사용 해야 합니다.           |(공백으로 둠)  <br/> 또는  <br/>  `EncryptedPSTs` <br/> |
    | `Name` <br/> |사용자 사서함에 가져올 PST 파일의 이름을 지정 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다. Azure 저장소 위치에 업로드 되는 PST 파일을 암호화 하기 때문에 `.pfile` 에 PST 파일 이름 확장명을 추가 합니다. 추가 해야는 `.pfile` CSV 파일에서 파일을 PST의 이름에 대 한 확장 합니다.<br/><br/> **중요:** CSV 파일에서 PST 파일 이름에 대 한 대/소문자 5 단계에서에서 Azure 저장소 위치에 업로드 된 PST 파일로 동일 해야 합니다. 예: 사용 하는 경우 `annb.pst.pfile` 에 `Name` 하 여 CSV 파일을 하지만 실제 PST 파일의 이름에서 매개 변수는 `AnnB.pst`, 해당 PST 파일에 대 한 가져오기가 실패 합니다. CSV 파일의 PST의 이름이 동일한 대/소문자를 사용 하 여 실제 PST 파일로 확인 해야 합니다.           | `annb.pst.pfile` <br/> |
    | `Mailbox` <br/> |PST 파일을 가져올 사서함의 전자 메일 주소를 지정합니다.   <br/> 비활성 사서함을 PST 파일을 가져오려면,이 매개 변수에 대 한 사서함 GUID를 지정 해야 합니다. 이 GUID를 가져오려면 다음 PowerShell 명령을 Exchange Online에서 실행: ' Get-mailbox InactiveMailboxOnly<identity of inactive mailbox> | FL Guid` <br/><br/> **Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-mailbox-<identity of active mailbox> | FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-mailbox- <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid'           | `annb@contoso.onmicrosoft.com` <br/> 또는  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | PST 파일을 사용자의 보관 사서함으로 가져올 것인지 여부를 지정합니다. 다음 두 가지 옵션이 있습니다.<br/> **False 이면** 사용자의 기본 사서함을 PST 파일을 가져옵니다.  <br/> **True 이면** 사용자의 보관 사서함을 PST 파일을 가져옵니다.  <br/>  이 매개 변수를 지정 하지 않으면 사용자의 기본 사서함에 PST 파일을 가져옵니다.  <br/><br/> **참고:** 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져오려면, 방금이 매개 변수에 대해 **true로** 지정 하 고 메일에 대 한 사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 된 `Mailbox` 매개 변수입니다.           | `FALSE` <br/> 또는  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | PST 파일을 가져온 사서함 폴더를 지정 합니다.  <br/>  이 매개 변수를 지정 하지 않고 공백으로 두면 PST 명명 된 **가져온** (받은 편지함 폴더와 다른 기본 사서함 폴더와 동일한 수준) 사서함의 루트 수준에 있는 새 폴더를으로 가져옵니다.  <br/>  지정 하는 경우 `/`, PST 파일의 항목에에서 사용자의 받은 편지함 폴더에서 직접 가져올 수 됩니다.  <br/>  지정 하는 경우 `/<foldername>`, 라는 하위 폴더를 가져올 PST 파일의 항목에에서 * \<foldername\> * 합니다. 예: 사용 하는 경우 `/ImportedPst`, **ImportedPst**라는 하위 폴더에 항목을 가져올 수는 있습니다. 이 하위 폴더에는 사용자의 받은 편지함 폴더에 배치 됩니다.<br/><br/> **팁:** Pst 파일을 가져오려면 가장 적합 한 폴더 위치를 결정할 수 있도록이 매개 변수를 사용해 몇 테스트 일괄 처리를 실행 하는 것이 좋습니다.           |(공백으로 둠)  <br/> 또는  <br/>  `/` <br/> 또는  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |이 선택적 매개 변수는 ANSI 파일 형식에서 PST 파일을 가져오기 위해 사용 하 여 코드 페이지에 대 한 숫자 값을 지정 합니다. 이 매개 변수는 일반적으로 이러한 언어 문자 인코딩에 대 한 더블 바이트 문자 집합 (DBCS)을 사용 하기 때문에 중국어, 일본어 및 한국어 (CJK) 조직에서 PST 파일을 가져오기 위해 사용 됩니다. 이 매개 변수는 사서함 폴더 이름에 대 한 DBCS를 사용 하는 언어에 대 한 PST 파일을 가져오려면 사용 되지 않습니다, 하는 경우 폴더 이름은 가져온 후 왜곡 자주는 합니다. 이 매개 변수를 사용 하 여 지원 되는 값의 목록에 대 한 [코드 페이지 식별자](https://go.microsoft.com/fwlink/p/?LinkId=328514)를 참조 하십시오.<br/><br/> **참고:** 앞부분에 명시 된,이 선택적 매개 변수 이며 CSV 파일에 포함할 필요가 없습니다. 또는 포함 하 고 하나 이상의 행에 대 한 값은 비워둡니다.           |(공백으로 둠)  <br/> 또는  <br/>  `932`(ANSI/OEM 일본어에 대 한 코드 페이지 식별자는)  <br/> |
    | `SPFileContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPManifestContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPSiteUrl` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
  
## <a name="step-8-create-a-pst-import-job-in-office-365"></a>8단계: Office 365에서 PST 가져오기 작업 만들기

마지막 단계에서는 Office 365에서 가져오기 서비스에서 PST 가져오기 작업을 만드는 것입니다. 앞에서 설명한 것 처럼 7 단계에서에서 만든 PST 가져오기 매핑 파일을 전송 됩니다. 가져오기 서비스에서 해제 하는 매핑 파일의 정보를 사용할 새 작업을 만든 후-암호화 하 고 지정 된 사용자 사서함에 (즉 5 단계에서에서 Office 365에 업로드 한) PST 파일을 가져옵니다. 
  
1. 이동 [https://protection.office.com](https://protection.office.com)합니다.
    
2. Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 Office 365에 로그인 합니다.
    
3. 왼쪽된 창에서 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.
    
4. **가져오기** 페이지에서 **가져오기 서비스로 이동**을 클릭합니다.
    
5. **Office 365로 데이터 가져오기** 페이지에서 **새 작업**을 클릭![아이콘 추가](media/ITPro-EAC-AddIcon.gif), **업로드 전자 메일 메시지 (PST 파일)를**클릭 하 고 있습니다.
    
6. **네트워크를 통해 파일 업로드** 페이지에서 **내 파일 업로드를 완료했습니다.** 및 **매핑 파일에 대한 액세스 권한이 있습니다.** 확인란을 클릭하고 **다음**을 클릭합니다.  
    
7. PST 가져오기 작업의 이름을 입력하고 **다음**을 클릭합니다.
    
8. **추가** 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 7 단계에서에서 만든 PST 매핑 파일을 선택 합니다. 
    
9. CSV 파일의 이름이 목록에 나타나면 선택하고 **유효성 검사**를 클릭하여 CSV 파일에 오류가 있는지 확인합니다.  
    
    > [!NOTE]
    > PST 파일을 암호화 하는 경우의 설명으로 이전는 `.pfile` PST 파일 이름 확장명이 추가 됩니다. 추가 해야는 `.pfile` CSV 파일에서 파일을 PST의 이름에 대 한 확장 합니다. 이렇게 하지 않으면 CSV 파일의 유효성 검사 실패 합니다. 
  
    PST 가져오기 작업을 만들려면 CSV 파일의 유효성 검사가 성공해야 합니다. 유효성 검사에 실패하는 경우 **상태** 열에서 **유효하지 않음** 링크를 클릭합니다. PST 가져오기 매핑 파일의 복사본이 열리고 실패한 파일의 각 행에 대해 오류 메시지가 표시됩니다. 
    
10. PST 매핑 파일의 유효성 검사가 성공하면 사용 약관 문서를 읽고 해당 확인란을 클릭합니다.
    
11. **마침**을 클릭하여 작업을 제출합니다. 
    
    작업의 **Office 365로 데이터 가져오기** 페이지에서 PST 가져오기 작업 목록에 표시 됩니다. 
    
12. 작업을 선택 하 고 **새로 고칠**을 클릭![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 표시 되는 상태 정보를 업데이트 합니다. 
    
13. 세부 정보 창에서 **자세히 보기**를 클릭하여 선택한 작업에 대한 최신 상태를 가져옵니다. 
 
## <a name="more-information"></a>추가 정보

- Office 365에 PST 파일을 가져올 이유?
    
  - Office 365에 조직의 전자 메일을 마이그레이션할 좋은 방법입니다.
    
  - 다음을 수행하여 조직의 준수 요구 사항을 해결할 수 있습니다.
    
  - 추가 사서함 저장 공간을 사용자에게 제공하도록 보관 사서함을 사용합니다.
    
  - 콘텐츠를 보존하도록 보류 중인 사서함을 배치합니다.
    
  - 사서함의 콘텐츠를 검색하도록 Microsoft eDiscovery 도구를 사용합니다.
    
  - 보존 정책을 사용하여 사서함 콘텐츠 보존 기간을 제어합니다.
    
  - 사서함과 관련 된 이벤트를 위한 Office 365 감사 로그를 검색 합니다.
    
  - 데이터 손실 방지 유용한 정보를 제공 합니다. 사용자의 컴퓨터에서 데이터를 저장 하지 않고 Exchange Online의 고가용성 기능을 상속 하는 PST 파일을 Office 365 사서함으로 가져옵니다.
    
  - 이러한 데이터는 클라우드에 저장되므로 모든 장치에서 사용할 수 있습니다.
    
- 키, Id, 2, 3, 4 단계에서 구한 되는 Url의 예는 다음과 같습니다. 이 예제에는 암호화 하는 O365ImportTool.exe 도구에서 실행 하 고 업로드 PST 파일을 Office 365에는 명령에 대 한 구문을 들어 있습니다. 암호 또는 기타 보안 관련 정보를 보호 하는 동일 하 게 이러한 방금 보호 하기 위한 예방 조치를 수행 해야 합니다.
    
  ```
  Symmetric key: l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=

  BPOSId: 42745b33-2a5c-4726-8a2a-ca43caa0f74b

  LicensingIntranetDistributionPointUrl (RMS licensing location): https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing
  
  SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D
  
  O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL from the SAS URL> /upload-destSAS:<SAS key from the SAS URL>
  
  EXAMPLES
  
  This example uploads PST files to the root of the Azure storage location:

  O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b /protect-ownerid:45beb445-4d06-47df-8e61-6ca1a88a080e /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
  
  This example uploads PST files to a subfolder named EncryptedPSTs  in the Azure storage location:
  
  O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b /protect-ownerid:45beb445-4d06-47df-8e61-6ca1a88a080e /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
  ```

- 앞에서 설명한 것 처럼 Office 365 가져오기 서비스 설정 (한 무기한 기간) 사서함에 PST 파일을 가져온 후 보존 대기 상태를 설정 합니다. 즉, *RentionHoldEnabled* 속성이로 설정 된 `True` 사서함에 할당 된 보존 정책 않습니다 처리할 수 있도록 합니다. 삭제 또는 보관 정책을 삭제 하거나 오래 된 메시지를 보관할 수 없도록 하 여 새로 가져온 메시지를 관리 하는 사서함 소유자 시간을 제공 합니다. 이 보존 대기 상태를 관리 하기 위해 수행할 수 있는 일부 단계는 다음과 같습니다. 
    
  - 특정 기간 동안 시간을 한 후 해제할 수 보존 대기를 실행 하 여는 `Set-Mailbox -RetentionHoldEnabled $false` 명령 합니다. 자세한 내용은 [사서함 보존에 원본 위치 유지](https://go.microsoft.com/fwlink/p/?LinkId=544749)를 참조 하십시오.
    
  - 나중에 일부 날짜 꺼져 있도록 보존 대기를 구성할 수 있습니다. 실행 하 여이 작업을 수행 된 `Set-Mailbox -EndDateForRetentionHold <date>` 명령 합니다. 예, 오늘 날짜가 2016 년 7 월 1 일이 고 30 일에서 해제 된 보존 대기 원하는 이라고 가정할 다음 명령을 실행 합니다: `Set-Mailbox -EndDateForRetentionHold 8/1/2016`합니다. 이 시나리오에서는 *RentionHoldEnabled* 속성을 설정 남게 `True`합니다. 자세한 내용은 [Set-mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317)를 참조 하십시오.
    
  - 오래 된 항목을 가져오지 않습니다 수 즉시 삭제 되거나 사용자의 보관 사서함으로 이동 되도록 사서함에 할당 된 보존 정책에 대 한 설정을 변경할 수 있습니다. 예, 사서함에 할당 된 삭제 또는 보관 정책에 대 한 보존 기간을 길게 수 있습니다. 이 시나리오에서는 있습니다 기능을 해제는 사서함에 보존 대기 상태에는 보존 정책의 설정을 변경한 후 합니다. 자세한 내용은 [Office 365 조직 내의 사서함에에서는 보관 및 삭제 정책 설정](set-up-an-archive-and-deletion-policy-for-mailboxes.md)을 참조 하십시오.
