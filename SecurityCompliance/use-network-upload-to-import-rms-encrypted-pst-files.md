---
title: 네트워크 업로드를 사용하여 RMS 암호화 PST 파일을 Office 365로 가져오기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 84a595b8-cd77-4f66-ac52-57a33ddd4773
description: 네트워크 업로드를 사용 하 여 RMS 암호화 PST 파일을 Office 365의 사용자 사서함으로 가져오는 방법에 대해 알아봅니다.
ms.openlocfilehash: 46f77f3fe173da23e08284884bb85c69ab53f710
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263708"
---
# <a name="use-network-upload-to-import-rms-encrypted-pst-files-to-office-365"></a>네트워크 업로드를 사용하여 RMS 암호화 PST 파일을 Office 365로 가져오기

**이 문서는 관리자를 위한 것입니다. PST 파일을 자체 사서함으로 가져오시겠습니까? [Outlook .pst 파일에서 전자 메일, 연락처 및 일정 가져오기를](https://go.microsoft.com/fwlink/p/?LinkID=785075) 참조 하세요.**
   
네트워크 업로드 옵션 및 Office 365 가져오기 서비스를 사용 하 여 PST 파일을 사용자 사서함으로 가져옵니다. 네트워크 업로드는 Microsoft 클라우드의 임시 저장소 영역에 PST 파일을 업로드 하는 것을 의미 합니다. 그런 다음 Office 365 가져오기 서비스가 저장소 영역의 PST 파일을 대상 사용자 사서함으로 복사 합니다. 가져오기 서비스의 새로운 기능을 사용 하면 PST 파일이 업로드 되 고 Microsoft 클라우드에서 저장 되기 전에 암호화할 수 있습니다. 이러한 파일은 사용자 사서함으로 가져올 때 암호화 해제됩니다. 
  
PST 파일을 암호화 하 고 Office 365 사서함으로 가져오는 데 필요한 단계는 다음과 같습니다.
  
[1 단계: PST 가져오기를 위한 Azure 권한 관리 설정](#step-1-set-up-azure-rights-management-for-pst-import)

[2단계: PST 가져오기를 위한 암호화 키 생성](#step-2-generate-an-encryption-key-for-pst-import)

[3 단계: RMS 테 넌 트 ID 및 라이선스 URL 획득](#step-3-obtain-rms-tenant-id-and-licensing-url)

[4 단계: PST 가져오기 도구 다운로드 및 SAS URL 복사](#step-4-download-the-pst-import-tools-and-copy-the-sas-url)

[5 단계: PST 파일 암호화 및 Office 365 업로드](#step-5-encrypt-and-upload-your-pst-files-to-office-365)

[반드시 6 단계: Office 365에 업로드 된 PST 파일 목록 보기](#optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365)

[7 단계: PST 가져오기 매핑 파일 만들기](#step-7-create-the-pst-import-mapping-file)

[8단계: Office 365에서 PST 가져오기 작업 만들기](#step-8-create-a-pst-import-job-in-office-365)
  
> [!IMPORTANT]
> PST 파일을 암호화 하 고 Office 365 사서함으로 가져오기 위해 1 ~ 4 단계를 한 번만 수행 하면 됩니다. 이러한 단계를 수행한 후에는 PST 파일의 일괄 처리를 암호화, 업로드 및 가져올 때마다 5 단계부터 8 단계를 수행 합니다. 
  
office 365로 데이터를 가져오는 방법에 대 한 자세한 내용은 [Overview to 조직 PST 파일을 office 365로 가져오기 개요](importing-pst-files-to-office-365.md)를 참조 하세요.
  
## <a name="before-you-begin"></a>시작하기 전에

- PST 파일을 Office 365 사서함으로 가져오려면 Exchange Online의 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. 자세한 내용은 [Manage role groups](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하십시오.
    
    또한 보안 & 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.
    
  - Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    또는
    
  - Office 365 조 직의 전역 관리자 여야 합니다.
    
  > [!TIP]
  > Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다. 
  
- 조직의 파일 서버나 공유 폴더에서 Office 365로 가져오려는 PST 파일을 저장 해야 합니다. 5 단계에서는이 파일 서버 또는 공유 폴더에 저장 된 PST 파일을 office 365에 암호화 하 고 업로드 하는 office 365 importtool을 실행 합니다.
    
- 이 절차 중에 암호화 키, 저장소 키 및 다양한 확인 키와 URL이 복사되고 사본이 저장됩니다. 이 정보는 5 단계에서 PST 파일을 암호화 및 업로드 하는 데 사용 됩니다. 암호나 기타 보안 관련 정보를 보호하는 것처럼 특히 주의해서 이러한 항목을 보호해야 합니다. 예를 들어 암호로 보호된 Microsoft Word 문서에 저장하거나 암호화된 USB 드라이브에 저장할 수 있습니다. 이러한 키, ID 및 URL의 예를 보려면 [자세한 정보](#more-information) 섹션을 참조하세요. 
    
- PST 파일을 Office 365의 비활성 사서함으로 가져올 수 있습니다. PST 가져오기 매핑 파일의 `Mailbox` 매개 변수에 비활성 사서함의 GUID를 지정 하 여이 작업을 수행 합니다. 자세한 내용은 [7 단계](#step-7-create-the-pst-import-mapping-file) 를 참조 하세요. 
    
- Exchange 하이브리드 배포에서는 기본 사서함이 온-프레미스 인 사용자에 대해 PST 파일을 클라우드 기반 보관 사서함으로 가져올 수 있습니다. PST 가져오기 매핑 파일에서 다음을 수행 하 여이 작업을 수행 합니다.
    
  - `Mailbox` 매개 변수의 사용자 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 합니다. 
    
  - `IsArchive` 매개 변수에 **TRUE** 값을 지정 합니다. 
    
    자세한 내용은 [7 단계](#step-7-create-the-pst-import-mapping-file) 를 참조 하세요. 
    
- PST 파일을 Office 365 사서함으로 가져온 후에는 사서함에 대 한 보존 설정이 무기한 유지 되도록 설정 됩니다. 즉, 보존 보류를 해제 하거나 보류를 해제 하기 위해 날짜를 설정할 때까지 사서함에 할당 된 보존 정책이 처리 되지 않습니다. 이 작업을 수행 하는 이유는 무엇 인가요? 사서함으로 가져온 메시지가 오래 된 경우 사서함에 대해 구성 된 보존 설정에 따라 보존 기간이 만료 되어 영구적으로 삭제 (제거) 될 수 있습니다. 사서함을 보존 상태로 두면 사서함 소유자가 새로 가져온 메시지를 관리할 수 있는 시간을 제공 하거나 사서함의 보존 설정을 변경할 수 있는 시간을 제공 합니다. 보존 유지 관리에 대 한 제안은 [More information](#more-information) 섹션을 참조 하세요. 
    
- pst 파일을 office 365에 업로드 하기 전에 암호화할 필요가 없는 경우 [네트워크 업로드를 사용 하 여 pst 파일을 office 365에 가져오기](use-network-upload-to-import-pst-files.md)를 참조 하세요.
    
- 네트워크 업로드를 사용 하 여 pst 파일을 office 365로 가져오는 방법에 대 한 질문과 대답은 [office 365로 pst 파일 가져오기에 대 한 FAQ](faqimporting-pst-files-to-office-365.md)를 참조 하세요.
  
## <a name="step-1-set-up-azure-rights-management-for-pst-import"></a>1단계: PST 가져오기를 위한 Azure 권한 관리 설정 

PST 가져오기는 Office 365의 azure RMS (권한 관리) 서비스에서 제공 하는 암호화 기능을 사용 합니다. 이렇게 하면 PST 파일을 Office 365에 업로드 하기 전에 암호화할 수 있습니다. 
  
PST 가져오기에 대해 Azure RMS를 구성 하는 작업은 다음 세 단계로 구성 됩니다.
  
- [Azure RMS 활성화](#activating-azure-rms)
    
- [Exchange Online에서 RMS 구성](#configuring-rms-in-exchange-online)
    
- [Active Directory RMS 클라이언트 설치](#installing-the-active-directory-rms-client)
    
### <a name="activating-azure-rms"></a>Azure RMS 활성화

Azure RMS는 기본적으로 사용 하지 않도록 설정 되어 있지만, 사용자나 조직의 다른 관리자가 활성화 했을 수 있습니다. azure [권한 관리를 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) 하 여 azure DRM을 설치 및 정품 인증 하기 위한 지침을 따릅니다.
  
### <a name="configuring-rms-in-exchange-online"></a>Exchange Online에서 RMS 구성

권한 관리 서비스를 활성화 한 후에는 Azure RMS를 사용 하도록 Exchange Online에서 IRM (정보 권한 관리)을 설정 해야 합니다. 자세한 내용은 [Azure 권한 관리를 사용 하도록 IRM 구성을](https://go.microsoft.com/fwlink/p/?LinkId=394816)참조 하십시오.
  
1. [원격 PowerShell을 사용 하 여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkId=396554 )합니다.
    
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
    |Office 365 Government(정부 커뮤니티 클라우드)  <br/> | `https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>개</sup> <br/> |
   
    > [!NOTE]
    > <sup>1</sup> 정부 sku 용 Office 365 (정부 커뮤니티 클라우드)를 구입한 고객만이 RMS 키 공유 위치를 사용 해야 합니다. 
  
    예를 들어이 명령은 북미에 있는 고객을 위해 Exchange online에서 RMS online 키 공유 위치를 구성 합니다.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
    ```

3. 다음 명령을 실행 하 여 RMS Online에서 Office 365 조직으로의 TPD (트러스트 된 게시 도메인)를 가져옵니다. 
    
    ```
    Import-RMSTrustedPublishingDomain -RMSOnline -Name "RMS Online"
    ```

    TPD에는 PST 파일 암호화를 비롯하여 조직에서 RMS 기능을 사용하는 데 필요한 설정이 포함되어 있습니다.  
    
4. 다음 명령을 실행 하 여 Office 365 조 직에 대해 IRM을 사용 하도록 설정 합니다.
    
    ```
    Set-IRMConfiguration -InternalLicensingEnabled $true
    ```

### <a name="installing-the-active-directory-rms-client"></a>Active Directory RMS 클라이언트 설치

이 섹션의 마지막 단계에서는 RMS(권한 관리 서비스) 클라이언트 2.1을 다운로드하는 것입니다. 이 소프트웨어는 azure rms에 대 한 액세스를 보호 하 고 azure rms를 사용 하는 응용 프로그램을 통한 정보 흐름을 보호 합니다. 5 단계에서 PST 파일을 암호화 하 고 업로드 하는 데 사용할 컴퓨터에 RMS 클라이언트를 설치 합니다. 
  
1. [권한 관리 서비스 클라이언트 2.1](https://www.microsoft.com/en-us/download/details.aspx?id=38396)을 다운로드 합니다.
    
2. Active Directory 권한 관리 서비스 클라이언트 2.1 마법사를 실행하여 클라이언트를 설치합니다.

## <a name="step-2-generate-an-encryption-key-for-pst-import"></a>2단계: PST 가져오기를 위한 암호화 키 생성

Azure RMS를 설정한 후에는 Office 365에 업로드 하는 PST 파일을 암호화 하는 데 사용 되는 암호화 키 (대칭 키)를 생성 해야 합니다. 이 작업을 수행 하려면 PST 가져오기 서비스를 Azure Active Directory의 서비스 주체로 추가 합니다. 이 응용 프로그램을 서비스 주체로 추가 하면 암호화 된 pst 파일을 5 단계에서 azure storage 위치에 업로드할 때 pst 가져오기 서비스가 azure Active Directory를 통해 직접 인증할 수 있습니다.
  
1. Windows PowerShell 용 Azure Active Directory 모듈을 시작 합니다.
    
2. 다음 명령을 실행하여 Microsoft Online 서비스에 연결합니다.
    
    ```
    Connect-MsolService
    ```

3. Office 365 조 직의 관리자 계정에 대 한 자격 증명을 입력 하 고 **확인**을 클릭 합니다.
    
4. 다음 명령을 실행하여 암호화 키(대칭 키)를 생성합니다. 새 PST 암호화 보안 주체를 만들어 이 작업을 수행합니다.
    
    ```
    New-MsolServicePrincipal -DisplayName PstEncryptionPrincipal
    ```

    시스템에 새 PST 암호화 보안 주체에 대한 대칭 키 및 속성이 표시됩니다.
    
    ![표시되는 대칭 키 복사 및 저장](media/0003fdea-dace-41d2-b49d-f5c98c6230ca.png)
  
5. 대칭 키를 텍스트 또는 Word 파일에 복사합니다. 앞서 설명한 것처럼 특별히 주의해서 이 파일을 보호해야 합니다. 대칭 키는 이 경우에만 표시되므로 이 창을 스크린샷으로 캡처한 후 같은 파일에 저장하는 것도 도움이 될 수 있습니다.  
    
    > [!IMPORTANT]
    > PST 암호화 보안 주체를 만든 후에는 **Get-MsolServicePrincipal** cmdlet을 사용하여 대칭 키를 검색할 수 없습니다. 그래서 키를 저장해야 하는 것입니다. 
  
Windows PowerShell 용 Azure Active Directory 모듈을 열어 두고 Microsoft Online 서비스에 연결 합니다. 다음 단계에서는 이 창에서 명령을 실행합니다.

## <a name="step-3-obtain-rms-tenant-id-and-licensing-url"></a>3 단계: RMS 테 넌 트 ID 및 라이선스 URL 획득

다음 단계에서는 조직의 Azure RMS 서비스에 대 한 테 넌 트 ID 및 라이선스 위치 URL을 가져옵니다. 이 정보를 복사하고 2단계의 대칭 키가 포함된 동일한 파일에 저장합니다. ID 및 URL은 5 단계에서 PST 파일을 암호화 하는 데 사용 됩니다.
  
1. Windows PowerShell 용 azure Active Directory 모듈 (Microsoft Online 서비스에 연결 됨)에서 다음 명령을 실행 하 여 Office 365 조직의 azure RMS 서비스에 연결 합니다.
    
    ```
    Connect-AadrmService 
    ```

2. Office 365 조 직의 관리자 계정에 대 한 자격 증명을 입력 하 고 **확인**을 클릭 합니다.
    
3. 다음 명령을 실행 하 여 Office 365 조직의 Azure RMS 서비스에 대 한 테 넌 트 ID를 표시 합니다.
    
    ```
    Get-AadrmConfiguration | FL BPOSId
    ```

    `BPOSId` 속성 값을 복사 하 여 저장 합니다. 
    
4. 다음 명령을 실행 하 여 Azure RMS 서비스의 라이선스 위치를 표시 합니다.
    
    ```
    Get-AadrmConfiguration | FL LicensingIntranetDistributionPointUrl
    ```

    `LicensingIntranetDistributionPointUrl` 속성 값을 복사 하 여 저장 합니다. 

## <a name="step-4-download-the-pst-import-tools-and-copy-the-sas-url"></a>4 단계: PST 가져오기 도구 다운로드 및 SAS URL 복사

Azure RMS를 구성 하 고 pst 파일을 암호화 하는 데 필요한 id를 가져왔는지 확인 한 후에는 5 단계에서 실행할 도구를 다운로드 하 고 설치 하 여 pst 파일을 암호화 하 고 Office 365에 업로드 합니다. 이러한 도구는 Azure AzCopy 도구 및 Office 365 데이터 암호화 도구입니다. 조직의 SAS URL도 복사 합니다. 이 URL은 조직에 대 한 Microsoft 클라우드의 Azure 저장소 위치 및 공유 액세스 서명 (SAS) 키에 대 한 네트워크 URL의 조합입니다. 이 키를 사용 하 여 Azure 저장소 위치에 PST 파일을 업로드 하는 데 필요한 권한을 제공 합니다. 2 단계와 3 단계에서 다른 정보를 복사한 것과 같은 파일에 저장 합니다. 앞에서 설명한 것 처럼, SAS URL을 보호 하기 위한 예방 조치를 취합니다. 
  
> [!IMPORTANT]
> azure 저장소 위치에 PST 파일을 업로드 하려면 azure AzCopy 버전 5.0를 사용 해야 합니다. 최신 버전의 AzCopy 도구는 PST 파일을 Office 365로 가져올 때 지원 되지 않습니다. 이 단계의 절차를 수행 하 여 네트워크를 **통해 파일 업로드** 페이지에서 AzCopy 도구를 다운로드 해야 합니다. 
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. office 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 office 365에 로그인 합니다.
    
3. 왼쪽 창에서 **데이터 관리** 를 클릭 하 고 **가져오기를**클릭 합니다.
    
4. **가져오기** 페이지에서 **가져오기 서비스로 이동**을 클릭합니다.
    
5. **Office로 데이터 가져오기 365** 페이지에서 **새 작업** ![추가 아이콘](media/ITPro-EAC-AddIcon.gif)을 클릭 한 다음 **전자 메일 메시지 (PST 파일) 업로드**를 클릭 합니다.
    
6. 네트워크를 **통해 파일 업로드** 페이지의 2 단계에서 **네트워크 업로드 SAS URL 표시**를 클릭 합니다.
    
7. URL이 표시 되 면 복사 하 여 다른 키를 저장 한 파일에 저장 합니다. 전체 URL을 복사해야 합니다. 
    
8. 3 단계에서 **azure AzCopy tool 다운로드** 를 클릭 하 여 azure AzCopy 도구를 다운로드 하 고 설치 합니다. 
    
9. 팝업 창에서 **실행**을 클릭하여 Azure AzCopy 도구를 설치합니다. 
    
    > [!IMPORTANT]
    > 64 비트 Windows를 실행 하는 컴퓨터 `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` 의 기본 위치에 Azure AzCopy 도구를 설치 해야 합니다. 이는 5 단계에서 o365importtool.zip를 실행 하는 경우 AzCopy 도구를 찾아서이 위치에서 찾는 것 이기 때문입니다. 
  
10. Azure AzCopy 도구를 설치한 후에 **는 Office 365 데이터 암호화 및 가져오기 도구 다운로드**를 클릭 합니다.
    
11. 팝업 창에서 다른 **** \> **이름으로 저장** 을 클릭 하 여 로컬 컴퓨터의 폴더에 o365importtool.zip 파일을 저장 합니다. 
    
12. O365ImportTool.zip 파일의 압축을 풉니다.
    
13. **취소** 를 클릭 하 여 **네트워크를 통해 파일 업로드** 페이지를 닫습니다. 
 
## <a name="step-5-encrypt-and-upload-your-pst-files-to-office-365"></a>5 단계: PST 파일 암호화 및 Office 365 업로드

1-4 단계를 완료 한 후에는 o365importtool.zip 도구를 사용 하 여 PST 파일을 암호화 하 고 Office 365에 업로드할 수 있습니다. 이 도구는 PST 파일을 암호화 한 다음 Microsoft 클라우드의 Azure 저장소 위치에 업로드 하 고 저장 합니다. 이 단계를 완료하려면 PST 파일이 조직의 파일 공유 또는 파일 서버에 있어야 합니다. 다음 절차에서는 이것을 원본 디렉터리라고 합니다. O365ImportTool.exe 도구를 실행할 때마다 다른 원본 디렉터리를 지정할 수 있습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트를 엽니다.
    
2. 4단계에서 O365ImportTool.exe 도구를 설치한 디렉터리로 이동합니다.
    
3. 다음 명령을 실행 하 여 PST 파일을 암호화 하 고 Office 365에 업로드 합니다.
    
    ```
    O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL> /upload-destSAS:<SAS key>
    ```

    다음 표에서는 매개 변수와 해당 필수 값에 대해 설명합니다. 이전 단계에서 획득한 정보가 이러한 매개 변수의 값에 사용됩니다.
    
    |**매개 변수**|**설명**|**예제**|
    |:-----|:-----|:-----|
    | `/srcdir:` <br/> |Office 365로 업로드 될 PST 파일이 들어 있는 조직의 원본 디렉터리를 지정 합니다.  <br/> | `/srcdir:\\FILESERVER01\PSTs` <br/> |
    | `/protect-rmsserver:` <br/> |Azure RMS 서비스의 라이선스 위치를 지정 합니다. 3 단계에서 구한 `LicensingIntranetDistributionPointUrl` 속성 값을 사용 합니다. 이 매개 변수의 값을 큰따옴표 ("")로 묶어야 합니다.  <br/> | `/protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing"` <br/> |
    | `/protect-tenantid:` <br/> |Azure RMS 조직의 id를 지정 합니다. 3 단계에서 구한 `BPOSId` 속성 값을 사용 합니다.  <br/> | `/protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b` <br/> |
    | `/protect-key:` <br/> |2단계에서 획득한 대칭 키를 지정합니다. 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> | `/protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867="` <br/> |
    | `/transfer:` <br/> |네트워크를 통해 PST 파일을 업로드할지 또는 하드 드라이브를 통해 발송할지를 지정합니다. 이 값 `upload` 은 네트워크를 통해 파일을 업로드 하 고 있음을 나타냅니다. 이 값 `drive` 은 pst를 하드 드라이브에 공급 중임을 나타냅니다.  <br/> | `/transfer:upload` <br/> |
    | `/upload-dest:` <br/> |PST 파일이 업로드 되는 Office 365의 대상을 지정 합니다. 조직의 Azure 저장소 위치입니다. 이 매개 변수의 값은 4 단계에서 복사한 SAS url의 네트워크 업로드 url로 구성 됩니다. 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/><br/> **팁:** 반드시 Azure storage 위치에 하위 폴더를 지정 하 여 암호화 된 PST 파일을 업로드할 수 있습니다. 이렇게 하려면 네트워크 업로드 URL에 하위 폴더 위치 ("ingestiondata")를 추가 합니다. 첫 번째 예에서는 하위 폴더를 지정 하지 않습니다. 즉, pst가 Azure 저장소 위치의 루트 ( *ingestiondata* )로 업로드 됩니다. 두 번째 예에서는 PST 파일을 Azure 저장소 위치에 *encryptedpsts* 라는 하위 폴더에 업로드 합니다.           | `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata"` <br/> 또는  <br/>  `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs"` <br/> |
    | `/upload-destSAS:` <br/> |조직의 SAS 키를 지정 합니다. 이 매개 변수의 값은 4 단계에서 복사한 sas URL의 sas 키로 구성 됩니다. SAS 키의 첫 번째 문자는 물음표 ("?")입니다. 이 매개 변수의 값을 큰따옴표(" ")로 묶으세요.  <br/> | `/upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/recurse` <br/> |이 선택적 스위치는 o365importtool.zip 도구에서 `/srcdir:` 매개 변수로 지정 된 원본 디렉터리의 하위 폴더에 있는 pst 파일을 복사 하도록 재귀 모드를 지정 합니다.  <br/><br/> **참고:** 이 스위치를 포함 하는 경우 하위 폴더의 PST 파일은 업로드 된 후 Azure 저장소 위치에서 파일 경로 이름이 다릅니다. 7단계에서 만드는 CSV 파일의 정확한 파일 경로 이름을 지정해야 합니다.           | `/recurse` <br/> |
   
    다음은 각 매개 변수의 실제 값을 사용하는 O365ImportTool.exe 도구의 구문 예입니다.
    
    ```
    O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b  /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
    ```

    이 명령을 실행하면 PST 파일의 암호화 및 업로드 진행률을 보여 주는 상태 메시지가 표시됩니다. 마지막 상태 메시지는 성공적으로 암호화 및 업로드된 파일의 총 수를 표시합니다.  
    
    > [!TIP]
    > O365ImportTool.exe 명령을 성공적으로 실행하고 모든 매개 변수가 올바른지 확인한 후에는 명령줄 구문 복사본을 이전 단계에서 획득한 정보를 복사한 것과 동일한(보안) 파일에 저장합니다. 그런 다음 o365importtool.zip 도구를 실행 하 여 PST 파일을 암호화 하 고 Office 365에 업로드 하려고 할 때마다 명령 프롬프트에이 명령을 복사 하 여 붙여 넣을 수 있습니다. 변경 해야 할 수 있는 값은 `/srcdir:` and `/upload-dest:` 매개 변수에 대 한 값일 뿐입니다. 
  
## <a name="optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>반드시 6 단계: Office 365에 업로드 된 PST 파일 목록 보기

선택적 단계로 Microsoft azure Storage Explorer (무료 오픈 소스 도구)를 설치 하 고 사용 하 여 azure blob에 업로드 한 PST 파일의 목록을 볼 수 있습니다. 이 작업을 수행 하는 데는 세 가지 좋은 이유가 있습니다.
  
- 조직의 공유 폴더 또는 파일 서버에 있는 PST 파일이 Azure blob에 성공적으로 업로드 되었는지 확인 합니다.

- PST 파일이 암호화 되어 있는지 확인 합니다. 암호화 된 pst 파일의 `.pfile` 확장명은 PST 파일 이름에 추가 됩니다. 예를 `pilarp.pst.pfile`들면입니다.
    
- Azure blob에 업로드 된 각 PST 파일에 대해 파일 이름 (및 포함 된 경우 하위 폴더 경로 이름)이 있는지 확인 합니다. 다음 단계에서 PST 매핑 파일을 만들 때 각 PST 파일의 폴더 경로와 파일 이름을 모두 지정해야 하므로 이러한 정보를 유용하게 사용할 수 있습니다. 이러한 이름을 확인하면 PST 매핑 파일의 잠재적인 오류를 줄이는 데 도움이 될 수 있습니다.
    
Microsoft Azure Storage Explorer가 미리 보기에 있습니다. 
  
 > [!IMPORTANT]
>  Azure 저장소 탐색기를 사용 하 여 PST 파일을 업로드 하거나 수정할 수 없습니다. PST 파일을 Office 365로 가져오는 유일한 방법은 AzCopy을 사용 하는 것입니다. 또한 Azure blob에 업로드 한 PST 파일은 삭제할 수 없습니다. PST 파일을 삭제 하려고 하면 필요한 사용 권한이 없다는 오류 메시지가 표시 됩니다. 모든 PST 파일이 Azure 저장소 영역에서 자동으로 삭제 됩니다. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created. 
  
azure 저장소 탐색기를 설치 하 고 azure storage 영역에 연결 하려면 다음을 수행 합니다.
  
1. [Microsoft Azure 저장소 탐색기 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 다운로드 하 고 설치 합니다.
    
2. Microsoft Azure 저장소 탐색기를 시작 하 고 왼쪽 창에서 **저장소 계정을** 마우스 오른쪽 단추로 클릭 한 다음 **Azure Storage에 연결**을 클릭 합니다. 
    
    ![저장소 계정을 마우스 오른쪽 단추로 클릭 한 다음 Azure Storage에 연결을 클릭 합니다.](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. **Azure storage에 연결**아래의 상자에서 4 단계에서 얻은 SAS URL을 붙여넣은 후 **다음**을 클릭 합니다. 
    
    ![Azure Storage에 연결 페이지의 상자에 SAS URL을 붙여 넣습니다.](media/5d034128-e087-48e1-9ebc-4c9fa262d5b7.png)
  
4. **연결 요약** 페이지에서 연결 정보를 검토 하 고 **연결**을 클릭할 수 있습니다. 
    
5. **저장소 계정**에서 **(서비스 SAS)** 노드를 확장 하 고 **Blob 컨테이너** 노드를 확장 합니다. 
    
6. **ingestiondata**를 마우스 오른쪽 단추로 클릭한 다음 **Blob 컨테이너 편집기 열기**를 클릭합니다.
    
    ![ingestiondata를 마우스 오른쪽 단추로 클릭한 다음 Blob 컨테이너 편집기 열기를 클릭합니다.](media/f50eee30-9202-4efc-904a-2895a0bc388d.png)
  
    5 단계에서 업로드 한 PST 파일 목록이 포함 된 Azure storage 영역이 표시 됩니다.
    
    ![Azure 저장소 탐색기는 사용자가 업로드한 PST 파일 목록이 표시됩니다.](media/a448ae43-e744-4153-8304-22b59e93883c.png)
  
7. Microsoft Azure 저장소 탐색기 사용을 마친 후 **ingestiondata**를 마우스 오른쪽 단추로 클릭 하 고 **분리** 를 클릭 하 여 Azure 저장소 영역에서 연결을 끊습니다. 그러지 않으면 다음 번에 연결할 때 오류가 발생합니다. 
    
    ![수집을 마우스 오른쪽 단추로 클릭하고 분리를 클릭하여 Azure 저장소 영역에서 연결 끊기](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-7-create-the-pst-import-mapping-file"></a>7 단계: PST 가져오기 매핑 파일 만들기

pst 파일을 암호화 하 고 Office 365 조 직의 Azure 저장 위치로 업로드 한 후에는 pst 파일을 가져올 사용자 사서함을 지정 하는 CSV (쉼표로 구분 된 값) 파일을 만듭니다. PST 가져오기 작업을 만드는 다음 단계에서 이 CSV 파일을 제출합니다.
  
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

    CSV 파일의 첫 번째 행 또는 머리글 행은 PST 가져오기 서비스에서 PST 파일을 사용자 사서함으로 가져오는 데 사용하는 매개 변수를 나열합니다. 각 매개 변수 이름은 쉼표로 구분됩니다. 머리글 행 아래의 각 행은 PST 파일을 특정 사서함으로 가져오기 위한 매개 변수 값을 나타냅니다. 사용자 사서함에 가져올 각 PST 파일에 대해 하나의 행이 필요합니다. 매핑 파일의 자리 표시자 데이터를 실제 데이터로 바꾸어야 합니다.
    
    > [!NOTE]
    > SharePoint 매개 변수를 포함하여 머리글 행의 어떤 내용도 변경하지 않도록 합니다. 변경한 내용은 PST 가져오기 프로세스 동안 무시됩니다. 
  
3. 다음 표의 정보를 사용하여 CSV 파일을 필요한 정보로 채웁니다.
    
    |**매개 변수**|**설명**|**예제**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |데이터를 가져올 Office 365 서비스를 지정 합니다. PST 파일을 사용자 사서함으로 가져오려면을 사용 `Exchange`합니다.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |5 단계에서 PST 파일을 업로드 한 Azure 저장소 위치의 폴더 위치를 지정 합니다.  <br/>  5 단계에 있는 `/upload-dest:` 매개 변수의 네트워크 URL에 선택적 하위 폴더 이름을 포함 하지 않은 경우 CSV 파일에서이 매개 변수를 비워 둡니다. 하위 폴더 이름을 포함 하는 경우이 매개 변수에 지정 합니다. 이 매개 변수의 값은 대/소문자를 구분 합니다. 두 방법 중 어느 것이 든 `FilePath` 매개 변수의 값에 "ingestiondata"를 포함 *하지 마십시오* .  <br/> <br/>**중요:** 파일 경로 이름의 대/소문자는 5 단계의 `/upload-dest:` 매개 변수에 SAS URL에 선택적 하위 폴더 이름을 포함 한 경우에 사용한 경우와 동일 해야 합니다. 예를 들어 5 단계의 하위 `EncryptedPSTs` 폴더 이름에 대해 CSV 파일의 `encryptedpsts` `FilePath` 매개 변수를 사용 하는 경우 PST 파일에 대 한 가져오기가 실패 합니다. 두 인스턴스에서 같은 대/소문자를 사용 해야 합니다.           |(공백으로 둠)  <br/> 또는  <br/>  `EncryptedPSTs` <br/> |
    | `Name` <br/> |사용자 사서함으로 가져올 PST 파일의 이름을 지정합니다. 이 매개 변수의 값은 대/소문자를 구분 합니다. Azure 저장소 위치로 업로드 되는 pst 파일은 암호화 되므로 pst 파일 이름에 `.pfile` 확장명이 추가 됩니다. CSV 파일의 PST `.pfile` 파일 이름에 확장을 추가 해야 합니다.  <br/><br/> **중요:** CSV 파일의 pst 파일 이름에 대 한 사례는 5 단계에서 Azure 저장소 위치로 업로드 된 pst 파일과 동일 해야 합니다. 예를 들어 CSV 파일의 `annb.pst.pfile` `Name` 매개 변수에서 사용 하는 경우 실제 PST 파일 `AnnB.pst`의 이름은 해당 pst 파일에 대 한 가져오기가 실패 합니다. CSV 파일의 PST 이름에 실제 PST 파일과 동일한 대/소문자가 사용 되는지 확인해 보십시오.           | `annb.pst.pfile` <br/> |
    | `Mailbox` <br/> |PST 파일을 가져올 사서함의 전자 메일 주소를 지정합니다.   <br/> PST 파일을 비활성 사서함으로 가져오려면이 매개 변수의 사서함 GUID를 지정 해야 합니다. 이 GUID를 얻으려면 Exchange Online에서 다음 PowerShell 명령을 실행 합니다.`Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL Guid` <br/><br/> **참고:** 경우에 따라 전자 메일 주소가 같은 여러 개의 사서함이 있고, 하나의 사서함이 활성 사서함이 고, 다른 사서함이 일시 삭제 (또는 비활성) 상태인 경우에만 가능 합니다. 이러한 상황에서는 PST 파일을 가져올 사서함을 고유 하 게 식별 하는 사서함 GUID를 지정 해야 합니다. 활성 사서함에 대해이 GUID를 가져오려면 다음 PowerShell 명령을 실행 `Get-Mailbox - <identity of active mailbox> | FL Guid`합니다. 일시 삭제 된 (또는 비활성) 사서함의 GUID를 가져오려면 다음 명령을 실행 합니다.`Get-Mailbox - <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`           | `annb@contoso.onmicrosoft.com` <br/> 또는  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | PST 파일을 사용자의 보관 사서함으로 가져올 것인지 여부를 지정합니다. 다음 두 가지 옵션이 있습니다.  <br/> **FALSE** PST 파일을 사용자의 기본 사서함으로 가져옵니다.  <br/> **TRUE** PST 파일을 사용자의 보관 사서함으로 가져옵니다.  <br/>  If you leave this parameter blank, the PST file is imported to the user's primary mailbox.  <br/><br/> **참고:** 기본 사서함이 온-프레미스 사용자의 클라우드 기반 보관 사서함으로 PST 파일을 가져오려면이 매개 변수에 대해 **TRUE** 를 지정 하 고 해당 `Mailbox` 매개 변수의 사용자 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 하면 됩니다.           | `FALSE` <br/> 또는  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | PST 파일을 가져올 사서함 폴더를 지정 합니다.  <br/>  이 매개 변수를 비워 두면 PST를 사서함의 루트 수준 (받은 편지함 폴더 및 **** 다른 기본 사서함 폴더와 같은 수준)에 있는 새 폴더로 가져오게 됩니다.  <br/>  지정 `/`하는 경우 PST 파일의 항목을 사용자의 받은 편지함 폴더로 직접 가져옵니다.  <br/>  지정 `/<foldername>`하는 경우 PST 파일의 항목을 * \<foldername\> * 이라는 하위 폴더로 가져옵니다. 예를 들어를 사용 하 `/ImportedPst`는 경우에는 항목을 **importedpst**라는 하위 폴더로 가져옵니다. 이 하위 폴더는 사용자의 받은 편지함 폴더에 배치 됩니다.  <br/><br/> **팁:** pst 파일을 가져올 가장 적합 한 폴더 위치를 결정할 수 있도록 몇 가지 테스트 일괄 처리를 실행 하 여이 매개 변수를 시험해 보십시오.           |(공백으로 둠)  <br/> 또는  <br/>  `/` <br/> 또는  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |이 선택적 매개 변수는 ANSI 파일 형식으로 PST 파일을 가져오는 데 사용할 코드 페이지의 숫자 값을 지정 합니다. 이 매개 변수는 일반적으로 문자 인코딩에 DBCS (더블 바이트 문자 집합)를 사용 하므로 중국어, 일본어 및 한국어 (CJK) 조직에서 PST 파일을 가져오는 데 사용 됩니다. 이 매개 변수를 사용 하 여 사서함 폴더 이름에 DBCS를 사용 하는 언어에 대 한 PST 파일을 가져오지 않으면 가져온 후 폴더 이름이 왜곡 되는 경우가 많습니다. 이 매개 변수에 사용할 지원 되는 값의 목록은 [코드 페이지 식별자](https://go.microsoft.com/fwlink/p/?LinkId=328514)를 참조 하십시오.  <br/><br/> **참고:** 앞에서 설명한 것 처럼이 매개 변수는 선택적으로 사용할 수 있으며 CSV 파일에 포함 하지 않아도 됩니다. 또는 하나 이상의 행에 대해 값을 비워 두면 됩니다.           |(공백으로 둠)  <br/> 또는  <br/>  `932`(ANSI/OEM 일본어에 대 한 코드 페이지 식별자)  <br/> |
    | `SPFileContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPManifestContainer` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
    | `SPSiteUrl` <br/> |PST 가져오기의 경우 이 매개 변수를 비워 둡니다.   <br/> |해당 없음  <br/> |
  
## <a name="step-8-create-a-pst-import-job-in-office-365"></a>8단계: Office 365에서 PST 가져오기 작업 만들기

마지막 단계는 Office 365에서 가져오기 서비스에 PST 가져오기 작업을 만드는 것입니다. 앞서 설명한 것처럼 7단계에서 만든 PST 가져오기 매핑 파일을 전송합니다. 새 작업을 만든 후에는 가져오기 서비스에서 매핑 파일의 정보를 사용 하 여 암호화를 취소 하 고, 5 단계에서 Office 365로 업로드 한 PST 파일을 지정 된 사용자 사서함으로 가져옵니다. 
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. office 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 office 365에 로그인 합니다.
    
3. 왼쪽 창에서 **데이터 관리** 를 클릭 하 고 **가져오기를**클릭 합니다.
    
4. **가져오기** 페이지에서 **가져오기 서비스로 이동**을 클릭합니다.
    
5. **Office로 데이터 가져오기 365** 페이지에서 **새 작업**![추가 아이콘](media/ITPro-EAC-AddIcon.gif)을 클릭 한 다음 **전자 메일 메시지 (PST 파일) 업로드**를 클릭 합니다.
    
6. **네트워크를 통해 파일 업로드** 페이지에서 **내 파일 업로드를 완료했습니다.** 및 **매핑 파일에 대한 액세스 권한이 있습니다.** 확인란을 클릭하고 **다음**을 클릭합니다.  
    
7. PST 가져오기 작업의 이름을 입력하고 **다음**을 클릭합니다.
    
8. 추가 아이콘](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 하 여 7 단계에서 만든 PST 매핑 파일을 선택 합니다. **** ![ 
    
9. CSV 파일의 이름이 목록에 나타나면 선택하고 **유효성 검사**를 클릭하여 CSV 파일에 오류가 있는지 확인합니다.  
    
    > [!NOTE]
    > 앞에서 설명한 것 처럼 pst 파일이 암호화 되 면 pst 파일 `.pfile` 이름에 확장명이 추가 됩니다. CSV 파일의 PST `.pfile` 파일 이름에 확장을 추가 해야 합니다. 이렇게 하지 않으면 CSV 파일의 유효성 검사가 실패합니다. 
  
    PST 가져오기 작업을 만들려면 CSV 파일의 유효성 검사가 성공해야 합니다. 유효성 검사에 실패하는 경우 **상태** 열에서 **유효하지 않음** 링크를 클릭합니다. PST 가져오기 매핑 파일의 복사본이 열리고 실패한 파일의 각 행에 대해 오류 메시지가 표시됩니다. 
    
10. PST 매핑 파일의 유효성 검사가 성공하면 사용 약관 문서를 읽고 해당 확인란을 클릭합니다.
    
11. **마침**을 클릭하여 작업을 제출합니다. 
    
    작업은 **Office로 데이터 가져오기 365** 의 PST 가져오기 작업 목록에 표시 됩니다. 
    
12. 작업을 선택 하 고 새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침**![을 클릭 하 여 세부 정보 창에 표시 되는 상태 정보를 업데이트 합니다. 
    
13. 세부 정보 창에서 **자세히 보기**를 클릭하여 선택한 작업에 대한 최신 상태를 가져옵니다. 
 
## <a name="more-information"></a>추가 정보

- PST 파일을 Office 365로 가져오는 이유는 무엇 인가요?
    
  - 조직의 전자 메일을 Office 365로 마이그레이션하는 것이 좋은 방법입니다.
    
  - 다음을 수행하여 조직의 준수 요구 사항을 해결할 수 있습니다.
    
  - 추가 사서함 저장 공간을 사용자에게 제공하도록 보관 사서함을 사용합니다.
    
  - 콘텐츠를 보존하도록 보류 중인 사서함을 배치합니다.
    
  - 사서함의 콘텐츠를 검색하도록 Microsoft eDiscovery 도구를 사용합니다.
    
  - 보존 정책을 사용하여 사서함 콘텐츠 보존 기간을 제어합니다.
    
  - 사서함 관련 이벤트에 대 한 Office 365 감사 로그를 검색 합니다.
    
  - 데이터 손실로부터 보호하는 데 도움이 됩니다. Office 365 사서함으로 가져오는 PST 파일은 사용자 컴퓨터에 데이터를 저장 하는 것이 아니라 Exchange Online의 고가용성 기능을 상속 합니다.
    
  - 이러한 데이터는 클라우드에 저장되므로 모든 장치에서 사용할 수 있습니다.
    
- 다음은 2, 3, 4 단계에서 얻은 키, id 및 url의 예입니다. 또한이 예제에는 o365importtool.zip 도구에서 실행 하 여 PST 파일을 암호화 하 고 Office 365에 업로드 하는 명령에 대 한 구문도 포함 되어 있습니다. 암호나 기타 보안 관련 정보를 보호하는 것처럼 특히 주의해서 이러한 항목을 보호해야 합니다.
    
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

- 앞에서 설명한 것 처럼 Office 365 가져오기 서비스는 PST 파일을 사서함으로 가져온 후 보존 보류 설정 (무기한 지속)을 설정 합니다. 즉, 사서함 ** 에 할당 된 보존 정책이 `True` 처리 되지 않도록 RentionHoldEnabled 속성이로 설정 됩니다. 이렇게 하면 삭제 또는 보관 정책이 이전 메시지를 삭제 하거나 보관할 수 없도록 하 여 사서함 소유자가 새로 가져온 메시지를 관리 하 게 됩니다. 이 보존 상태를 관리 하기 위해 수행할 수 있는 몇 가지 단계는 다음과 같습니다. 
    
  - 일정 기간이 지난 후에는 `Set-Mailbox -RetentionHoldEnabled $false` 명령을 실행 하 여 보존 상태를 해제할 수 있습니다. 자세한 내용은 [사서함을 보존 상태로 두기](https://go.microsoft.com/fwlink/p/?LinkId=544749)를 참조 하십시오.
    
  - 나중에 특정 날짜에 해제 되도록 보존 기능을 구성할 수 있습니다. `Set-Mailbox -EndDateForRetentionHold <date>` 명령을 실행 하 여이 작업을 수행 합니다. 예를 들어 오늘 날짜가 6 월 1 일, 30 일 이내에 보존을 해제 하려는 경우에는 다음 명령을 실행 합니다 `Set-Mailbox -EndDateForRetentionHold 7/1/2016`. 이 시나리오에서는 *RentionHoldEnabled* 속성을로 `True`설정 합니다. 자세한 내용은 [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317)를 참조 하십시오.
    
  - 사서함에 할당 된 보존 정책의 설정을 변경 하 여 가져온 이전 항목을 즉시 삭제 하거나 사용자의 보관 사서함으로 이동할 수는 없습니다. 예를 들어 사서함에 할당 된 삭제 또는 보관 정책의 보존 기간을 늘릴 수 있습니다. 이 시나리오에서는 보존 정책 설정을 변경한 후 사서함에 대 한 보존을 해제 합니다. 자세한 내용은 [Office 365 조 직에서 사서함에 대 한 보관 및 삭제 정책 설정을](set-up-an-archive-and-deletion-policy-for-mailboxes.md)참조 하십시오.
