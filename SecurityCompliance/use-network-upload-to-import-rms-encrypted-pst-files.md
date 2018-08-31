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
# <a name="use-network-upload-to-import-rms-encrypted-pst-files-to-office-365"></a><span data-ttu-id="c3b67-103">네트워크 업로드를 사용하여 RMS 암호화 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3b67-103">Use network upload to import RMS-encrypted PST files to Office 365</span></span>

<span data-ttu-id="c3b67-104">**이 문서는 관리자입니다. 자신의 사서함에 PST 파일을 가져올 하려고 합니까? [가져오기 전자 메일, 연락처 및 일정 Outlook.pst 파일에서](https://go.microsoft.com/fwlink/p/?LinkID=785075) 를 참조 하십시오.**</span><span class="sxs-lookup"><span data-stu-id="c3b67-104">**This article is for administrators. Are you trying to import PST files to your own mailbox? See [Import email, contacts, and calendar from an Outlook .pst file](https://go.microsoft.com/fwlink/p/?LinkID=785075)**</span></span>
   
<span data-ttu-id="c3b67-p101">네트워크를 사용 하 여 사용자 사서함에 PST 파일을 가져오려면 옵션 및 Office 365를 가져올 서비스에 업로드 합니다. 네트워크 업로드는 업로드 PST 파일 Microsoft 클라우드에서 임시 저장 영역을 의미 합니다. 그런 다음 Office 365 가져오기 서비스 대상 사용자 사서함에 저장 영역에서 PST 파일을 복사 합니다. 가져오기 서비스의 새로운 기능을 통해 업로드 하는 Microsoft 클라우드에 저장 하기 전에 PST 파일을 암호화할 수 있습니다. 이러한 파일을 사용자 사서함을 가져올 때 되지 않은 crypted 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p101">Use the network upload option and the Office 365 Import service to import PST files to user mailboxes. Network upload means that you upload the PST files a temporary storage area in the Microsoft cloud. Then the Office 365 Import service copies the PST files from the storage area to the target user mailboxes. A new feature of the Import service lets you encrypt your PST files before they are uploaded and stored on the Microsoft cloud. These files will be un-encrypted when they're imported to user mailboxes.</span></span> 
  
<span data-ttu-id="c3b67-110">암호화 하 여 Office 365 사서함에 PST 파일을 가져올 필요한 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-110">Here are the steps required to encrypt and import PST files to Office 365 mailboxes:</span></span>
  
[<span data-ttu-id="c3b67-111">1단계: PST 가져오기를 위한 Azure 권한 관리 설정 </span><span class="sxs-lookup"><span data-stu-id="c3b67-111">Step 1: Set up Azure Rights Management for PST Import</span></span>](#step-1-set-up-azure-rights-management-for-pst-import)

[<span data-ttu-id="c3b67-112">2단계: PST 가져오기를 위한 암호화 키 생성</span><span class="sxs-lookup"><span data-stu-id="c3b67-112">Step 2: Generate an encryption key for PST Import</span></span>](#step-2-generate-an-encryption-key-for-pst-import)

[<span data-ttu-id="c3b67-113">3 단계: RMS 테 넌 트 ID 및 라이선스 URL 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3b67-113">Step 3: Obtain RMS tenant ID and licensing URL</span></span>](#step-3-obtain-rms-tenant-id-and-licensing-url)

[<span data-ttu-id="c3b67-114">PST 가져오기 도구를 다운로드 하 고 SAS URL을 복사 하는 4 단계:</span><span class="sxs-lookup"><span data-stu-id="c3b67-114">Step 4: Download the PST Import tools and copy the SAS URL</span></span>](#step-4-download-the-pst-import-tools-and-copy-the-sas-url)

[<span data-ttu-id="c3b67-115">5 단계: 암호화 하 고 Office 365에 PST 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-115">Step 5: Encrypt and upload your PST files to Office 365</span></span>](#step-5-encrypt-and-upload-your-pst-files-to-office-365)

[<span data-ttu-id="c3b67-116">(선택 사항) Office 365에 보기 PST 파일의 목록이 업로드 6 단계:</span><span class="sxs-lookup"><span data-stu-id="c3b67-116">(Optional) Step 6: View a list of the PST files uploaded to Office 365</span></span>](#optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365)

[<span data-ttu-id="c3b67-117">7 단계: PST 가져오기 매핑 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="c3b67-117">Step 7: Create the PST Import mapping file</span></span>](#step-7-create-the-pst-import-mapping-file)

[<span data-ttu-id="c3b67-118">8단계: Office 365에서 PST 가져오기 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="c3b67-118">Step 8: Create a PST Import job in Office 365</span></span>](#step-8-create-a-pst-import-job-in-office-365)
  
> [!IMPORTANT]
> <span data-ttu-id="c3b67-p102">암호화 하 여 Office 365 사서함에 PST 파일을 가져올-를 설정 하 고 조직 구성 단계 4를 한번만 1 단계를 수행 해야 합니다. 다음이 단계를 수행 하 고 나면 단계 5 ~ 8 단계 암호화, 업로드 하 고, 가져올 PST 파일의 일괄 처리를 사용할 때마다를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p102">You have to perform Step 1 through Step 4 only once to set up and configure your organization to encrypt and import PST files to Office 365 mailboxes. After you perform these steps, follow Step 5 through Step 8 each time you want to encrypt, upload, and import a batch of PST files.</span></span> 
  
<span data-ttu-id="c3b67-121">Office 365로 데이터 가져오기 (영문) 하는 방법에 대 한 자세한 내용은 [Office 365로 조직 PST 파일 가져오기 (영문)의 개요](importing-pst-files-to-office-365.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-121">For more information about importing data to Office 365, see [Overview of importing your organization PST files to Office 365](importing-pst-files-to-office-365.md).</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="c3b67-122">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="c3b67-122">Before you begin</span></span>

- <span data-ttu-id="c3b67-p103">역할을 할당 사서함 가져오기 내보내기 Exchange 온라인 Office 365 사서함에 PST 파일을 가져오려면 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 다음 자신을 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹](https://go.microsoft.com/fwlink/p/?LinkId=730688)에 "역할 그룹 만들기" 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p103">You have to be assigned the Mailbox Import Export role in Exchange Online to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
    
    <span data-ttu-id="c3b67-128">또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-128">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
    
  - <span data-ttu-id="c3b67-p104">역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p104">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="c3b67-131">또는</span><span class="sxs-lookup"><span data-stu-id="c3b67-131">Or</span></span>
    
  - <span data-ttu-id="c3b67-132">Office 365 조직에서 전역 관리자 여야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-132">You have to be a global administrator in your Office 365 organization.</span></span>
    
  > [!TIP]
  > <span data-ttu-id="c3b67-p105">Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p105">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
- <span data-ttu-id="c3b67-p106">파일 서버 또는 조직에 있는 공유 폴더에서 Office 365로 가져올 PST 파일을 저장 해야 합니다. 5 단계에서에서 암호화 되며이 파일 서버에 저장 된 또는 Office 365에 폴더를 공유 하 고 PST 파일을 업로드 하는 Office 365 ImportTool를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p106">You need to store the PST files that you want to import to Office 365 on a file server or shared folder in your organization. In Step 5, you'll run the Office 365 ImportTool, which will encrypt and upload the PST files that are stored on this file server or shared folder to Office 365.</span></span>
    
- <span data-ttu-id="c3b67-p107">이 절차를 복사 하 고 암호화 키, 저장소 키 및 다양 한 식별 키와 Url의 복사본을 저장 하는 것입니다. 이 정보를 암호화 하 여 PST 파일을 업로드할 5 단계에서에서 사용 됩니다. 암호 또는 기타 보안 관련 정보를 보호 하는 동일 하 게 이러한 방금 보호 하기 위한 예방 조치를 수행 해야 합니다. 예: 암호로 보호 된 Microsoft Word 문서에 저장 또는 암호화 된 USB 드라이브에 저장 수 있습니다. 이러한 키, Id, 및 Url의 예에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p107">This procedure involves copying and saving a copy of an encryption key, a storage key, and a number of identification keys and URLs. This information will be used in Step 5 to encrypt and upload your PST files. Be sure to take precautions to protect these just like you would protect passwords or other security-related information. For example you might save them to a password-protected Microsoft Word document or save them to an encrypted USB drive. See the [More information](#more-information) section for an example of these keys, IDs, and URLs.</span></span> 
    
- <span data-ttu-id="c3b67-p108">Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니다. 비활성 사서함의 GUID를 지정 하 여이 작업을 수행 된 `Mailbox` PST 가져오기 매핑 파일에서 매개 변수입니다. 자세한 내용은 [7 단계를](#step-7-create-the-pst-import-mapping-file) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p108">You can import PST files to an inactive mailbox in Office 365. You do this by specifying the GUID of the inactive mailbox in the  `Mailbox` parameter in the PST Import mapping file. See [Step 7](#step-7-create-the-pst-import-mapping-file) for more information.</span></span> 
    
- <span data-ttu-id="c3b67-p109">Exchange 하이브리드 배포에서 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져올 수 있습니다. PST 가져오기 매핑 파일에서 다음을 수행 하 여이 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p109">In an Exchange hybrid deployment, you can import PST files to a cloud-based archive mailbox for a user whose primary mailbox is on-premises. You do this by doing the following in the PST Import mapping file:</span></span>
    
  - <span data-ttu-id="c3b67-147">사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 된 `Mailbox` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-147">Specify the email address for the user's on-premises mailbox in the  `Mailbox` parameter.</span></span> 
    
  - <span data-ttu-id="c3b67-148">**TRUE** 값을 지정 된 `IsArchive` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-148">Specify the **TRUE** value in the  `IsArchive` parameter.</span></span> 
    
    <span data-ttu-id="c3b67-149">자세한 내용은 [7 단계를](#step-7-create-the-pst-import-mapping-file) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-149">See [Step 7](#step-7-create-the-pst-import-mapping-file) for more information.</span></span> 
    
- <span data-ttu-id="c3b67-p110">PST 파일을 Office 365 사서함으로 가져온 후 사서함에 대 한 설정 보존 대기는 무기한 기간에 대 한 켜 집니다. 즉, 사서함에 할당 된 보존 정책 보존 보류 해제 하거나 보류를 해제 하려면 날짜를 설정할 때까지 처리 되지 않습니다. 이유 해야 할까요? 오래 된 메시지를 사서함으로 가져온 경우 이러한 수 영구적으로 삭제 됩니다 (비우기)가 보존 기간이 만료 되었기 때문에 사서함에 대해 구성 된 보존 설정에 따라 합니다. 사서함을 보존 대기 배치 이러한 새로 가져온 메시지 또는 사서함에 대 한 보존 설정을 변경 하려면 시간 부여를 관리 하는 사서함 소유자 시간을 제공 합니다. 보존 대기 상태를 관리 하는 방법에 대 한 제안에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p110">After PST files are imported to an Office 365 mailbox, the retention hold setting for the mailbox is turned on for an indefinite duration. This means that the retention policy assigned to the mailbox won't be processed until you turn off the retention hold or set a date to turn off the hold. Why do we do this? If messages imported to a mailbox are old, they might be permanently deleted (purged) because their retention period has expired based on the retention settings configured for the mailbox. Placing the mailbox on retention hold will give the mailbox owner time to manage these newly-imported messages or give you time to change the retention settings for the mailbox. See the [More information](#more-information) section for suggestions about managing the retention hold.</span></span> 
    
- <span data-ttu-id="c3b67-156">Office 365를 업로드 하기 전에 PST 파일을 암호화 하는데 필요 하지 않으면, [Office 365에 PST 파일을 가져오려면 업로드 사용 하 여 네트워크](use-network-upload-to-import-pst-files.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-156">If you don't need to encrypt your PST files before you upload them to Office 365, see [Use network upload to import PST files to Office 365](use-network-upload-to-import-pst-files.md).</span></span>
    
- <span data-ttu-id="c3b67-157">Office 365에 PST 파일을 가져오려면 네트워크 업로드를 사용 하는 방법에 대 한 질문과 대답 [PST 파일을 Office 365로 가져오기 (영문) 하는 방법에 대 한 FAQ](faqimporting-pst-files-to-office-365.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-157">For frequently asked questions about using network upload to import PST files to Office 365, see [FAQ about importing PST files to Office 365](faqimporting-pst-files-to-office-365.md).</span></span>
  
## <a name="step-1-set-up-azure-rights-management-for-pst-import"></a><span data-ttu-id="c3b67-158">1단계: PST 가져오기를 위한 Azure 권한 관리 설정 </span><span class="sxs-lookup"><span data-stu-id="c3b67-158">Step 1: Set up Azure Rights Management for PST Import</span></span>

<span data-ttu-id="c3b67-p111">PST 가져오기 Office 365에서 Azure 권한 관리 (Azure RMS) 서비스에서 제공 하는 암호화 기능을 사용 합니다. 이 통해 Office 365를 업로드 하기 전에 PST 파일을 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p111">PST Import uses the encryption functionality provided by the Azure Rights Management (Azure RMS) service in Office 365. This lets you to encrypt PST files before uploading them to Office 365.</span></span> 
  
<span data-ttu-id="c3b67-161">Azure RMS PST 가져오기에 대 한 구성 세 단계로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-161">Configuring Azure RMS for PST Import consists of three steps:</span></span>
  
- [<span data-ttu-id="c3b67-162">Azure RMS를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-162">Activating Azure RMS</span></span>](#activate-azure-rms)
    
- [<span data-ttu-id="c3b67-163">RMS in Exchange Online 구성</span><span class="sxs-lookup"><span data-stu-id="c3b67-163">Configuring RMS in Exchange Online</span></span>](#configure-rms-in-exchange-online)
    
- [<span data-ttu-id="c3b67-164">Active Directory의 RMS 클라이언트를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-164">Installing the Active Directory RMS Client</span></span>](#install-the-active-directory-rms-client)
    
### <a name="activating-azure-rms"></a><span data-ttu-id="c3b67-165">Azure RMS를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-165">Activating Azure RMS</span></span>

<span data-ttu-id="c3b67-p112">기본적으로 azure RMS 더이상 사용할 수 없지만 또는 다른 관리자가 조직에서 수 활성화 한 것입니다. 설치 하 고 Azure DRM을 활성화 하려면 [Azure 권한 관리 활성화](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p112">Azure RMS is disabled by default, but you or another administrator in your organization might have activated it. Follow instructions on [Activating Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) to install and activate Azure DRM.</span></span>
  
### <a name="configuring-rms-in-exchange-online"></a><span data-ttu-id="c3b67-168">RMS in Exchange Online 구성</span><span class="sxs-lookup"><span data-stu-id="c3b67-168">Configuring RMS in Exchange Online</span></span>

<span data-ttu-id="c3b67-p113">권한 관리 서비스를 활성화 한 후 다음 단계를 권한 관리 IRM (정보) Azure RMS를 사용 하 여 온라인 Exchange 설정 하는 것입니다. 자세한 내용은 [Azure 권한 관리를 사용 하 여 IRM 구성](https://go.microsoft.com/fwlink/p/?LinkId=394816)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p113">After you've activated the Rights Management service, the next step is to set up Information Rights Management (IRM) in Exchange Online to use Azure RMS. For more information, see [Configure IRM to use Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=394816).</span></span>
  
1. <span data-ttu-id="c3b67-171">[원격 PowerShell을 사용 하는 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkId=396554 )합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-171">[Connect to Exchange Online using Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554 ).</span></span>
    
2. <span data-ttu-id="c3b67-172">다음 명령을 실행하여 RMS 키 공유 URL을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-172">Run the following command to set the RMS key sharing URL.</span></span>
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation <RMS key sharing location>
    ```

    <span data-ttu-id="c3b67-173">다음 표를 사용하여 조직의 위치에 대한 올바른 RMS 키 공유 위치를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-173">Use the following table to determine the correct RMS key sharing location for the location of your organization.</span></span>
    
    |<span data-ttu-id="c3b67-174">**위치**</span><span class="sxs-lookup"><span data-stu-id="c3b67-174">**Location**</span></span>|<span data-ttu-id="c3b67-175">**RMS 키 공유 위치**</span><span class="sxs-lookup"><span data-stu-id="c3b67-175">**RMS key sharing location**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="c3b67-176">북미</span><span class="sxs-lookup"><span data-stu-id="c3b67-176">North America</span></span>  <br/> | `https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |<span data-ttu-id="c3b67-177">유럽 연합</span><span class="sxs-lookup"><span data-stu-id="c3b67-177">European Union</span></span>  <br/> | `https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |<span data-ttu-id="c3b67-178">아시아</span><span class="sxs-lookup"><span data-stu-id="c3b67-178">Asia</span></span>  <br/> | `https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |<span data-ttu-id="c3b67-179">남미</span><span class="sxs-lookup"><span data-stu-id="c3b67-179">South America</span></span>  <br/> | `https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |<span data-ttu-id="c3b67-180">Office 365 Government(정부 커뮤니티 클라우드)</span><span class="sxs-lookup"><span data-stu-id="c3b67-180">Office 365 for Government (Government Community Cloud)</span></span>  <br/> | <span data-ttu-id="c3b67-181">`https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="c3b67-181">`https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>1</sup></span></span> <br/> |
   
    > [!NOTE]
    > <span data-ttu-id="c3b67-182"><sup>1</sup> Government Sku (정부 커뮤니티 클라우드)에 대 한 Office 365를 구입한 고객만이 RMS 키 공유 위치를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-182"><sup>1</sup> Only customers who have purchased Office 365 for Government SKUs (Government Community Cloud) should use this RMS key sharing location.</span></span> 
  
    <span data-ttu-id="c3b67-183">예,이 명령은 RMS Online 키 공유 위치 Exchange 온라인 북미에 있는 고객에 대 한 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-183">For example, this command configures the RMS Online key sharing location in Exchange Online for a customer located in North America.</span></span>
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
    ```

3. <span data-ttu-id="c3b67-184">RMS Online에서 Office 365 조직에는 신뢰할 수 있는 도메인 TPD (게시)를 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-184">Run the following command to import a Trusted Publishing Domain (TPD) from RMS Online to your Office 365 organization.</span></span> 
    
    ```
    Import-RMSTrustedPublishingDomain -RMSOnline -Name "RMS Online"
    ```

    <span data-ttu-id="c3b67-185">TPD에는 PST 파일 암호화를 비롯하여 조직에서 RMS 기능을 사용하는 데 필요한 설정이 포함되어 있습니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-185">A TPD contains the settings needed to use RMS features in your organization, including encrypting PST files.</span></span> 
    
4. <span data-ttu-id="c3b67-186">Office 365 조직에 대 한 IRM을 사용 하도록 설정 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-186">Run the following command to enable IRM for your Office 365 organization.</span></span>
    
    ```
    Set-IRMConfiguration -InternalLicensingEnabled $true
    ```

### <a name="installing-the-active-directory-rms-client"></a><span data-ttu-id="c3b67-187">Active Directory의 RMS 클라이언트를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-187">Installing the Active Directory RMS Client</span></span>

<span data-ttu-id="c3b67-p114">이 섹션의 마지막 단계 2.1 서비스 RMS (권한 관리) 클라이언트를 다운로드 하는 것입니다. 이 소프트웨어 Azure RMS에 대 한 액세스를 보호 하는데 도움이 됩니다 및 정보를 암호화 하 여 5 단계에서에서 PST 파일을 업로드할 사용할 하는 동일한 컴퓨터에서 RMS 클라이언트 Azure RMS. 설치를 사용 하는 응용 프로그램을 통해 흐름을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p114">The last step in this section is to download the Rights Management Services (RMS) Client 2.1. This software helps protect access to Azure RMS and protects information flowing through applications that use Azure RMS. Install the RMS client on the same computer that you'll use to encrypt and upload PST files in Step 5.</span></span> 
  
1. <span data-ttu-id="c3b67-191">[권한 관리 서비스 클라이언트 2.1을](https://www.microsoft.com/en-us/download/details.aspx?id=38396)다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-191">Download [Rights Management Service Client 2.1](https://www.microsoft.com/en-us/download/details.aspx?id=38396).</span></span>
    
2. <span data-ttu-id="c3b67-192">Active Directory 권한 관리 서비스 클라이언트 2.1 마법사를 실행하여 클라이언트를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-192">Run the Active Directory Rights Management Service Client 2.1 wizard to install the client.</span></span>

## <a name="step-2-generate-an-encryption-key-for-pst-import"></a><span data-ttu-id="c3b67-193">2단계: PST 가져오기를 위한 암호화 키 생성</span><span class="sxs-lookup"><span data-stu-id="c3b67-193">Step 2: Generate an encryption key for PST Import</span></span>

<span data-ttu-id="c3b67-p115">Azure RMS 설정한 후 다음 단계에서는 Office 365에 업로드 하는 PST 파일을 암호화 하는데 사용 되는 (대칭 키 라고 함) 암호화 키를 생성 하는 것입니다. Azure Active Directory에서 사용자를 서비스로 PST 가져오기 서비스를 추가 하 여이 작업을 수행 합니다. 5 단계에서에서 Azure 저장소 위치로 PST 파일을 암호화 서비스 사용자를 업로드할 때 Azure Active Directory를 사용 하 여 직접 인증 PST 가져오기 서비스를 선택 하면으로이 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p115">After you've set up Azure RMS, the next step is to generate an encryption key (called a symmetric key) that will be used to encrypt the PST files that you upload to Office 365. You'll do this by adding the PST Import service as a service principal in Azure Active Directory. Adding this application as a service principal will allow the PST Import service to authenticate directly with Azure Active Directory when you upload encrypted the PST files to the Azure storage location in Step 5.</span></span>
  
1. <span data-ttu-id="c3b67-197">Windows PowerShell 용 Azure Active Directory 모듈을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-197">Start the Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="c3b67-198">다음 명령을 실행하여 Microsoft Online 서비스에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-198">Run the following command to connect to the Microsoft Online service.</span></span>
    
    ```
    Connect-MsolService
    ```

3. <span data-ttu-id="c3b67-199">Office 365 조직에서 관리자 계정에 대 한 자격 증명을 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-199">Enter the credentials for an administrator account in your Office 365 organization, and then click **OK**.</span></span>
    
4. <span data-ttu-id="c3b67-p116">다음 명령을 실행하여 암호화 키(대칭 키)를 생성합니다. 새 PST 암호화 보안 주체를 만들어 이 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p116">Run the following command to generate an encryption key (call a symmetric key). You'll do this by creating a new PST Encryption Principal.</span></span>
    
    ```
    New-MsolServicePrincipal -DisplayName PstEncryptionPrincipal
    ```

    <span data-ttu-id="c3b67-202">시스템에 새 PST 암호화 보안 주체에 대한 대칭 키 및 속성이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-202">The system displays the symmetric key and the properties for the new PST Encryption Principal.</span></span>
    
    ![표시되는 대칭 키 복사 및 저장](media/0003fdea-dace-41d2-b49d-f5c98c6230ca.png)
  
5. <span data-ttu-id="c3b67-p117">대칭 키를 텍스트 또는 Word 파일에 복사합니다. 앞서 설명한 것처럼 특별히 주의해서 이 파일을 보호해야 합니다. 대칭 키는 이 경우에만 표시되므로 이 창을 스크린샷으로 캡처한 후 같은 파일에 저장하는 것도 도움이 될 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-p117">Copy the symmetric key to a text or Word file. As previously stated, be sure to take precautions to protect this file. Because this is the only time that the symmetric key is displayed, you might also consider taking a screenshot of this window and saving it to the same file.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="c3b67-p118">PST 암호화 보안 주체를 만든 후에는 **Get-MsolServicePrincipal** cmdlet을 사용하여 대칭 키를 검색할 수 없습니다. 그래서 키를 저장해야 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p118">After you create the PST Encryption Principal, you won't be able to retrieve the symmetric key by using the **Get-MsolServicePrincipal** cmdlet. That's why it's important to save the key.</span></span> 
  
<span data-ttu-id="c3b67-p119">Open 및 Microsoft 온라인 서비스에 연결 된 Azure Active Directory 모듈에 대 한 Windows PowerShell을 유지 합니다. 명령을 실행 하는 다음 단계에서이 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p119">Keep the Azure Active Directory Module for Windows PowerShell open and connected to the Microsoft Online service. You'll run a command in this window in the next step.</span></span>

## <a name="step-3-obtain-rms-tenant-id-and-licensing-url"></a><span data-ttu-id="c3b67-211">3 단계: RMS 테 넌 트 ID 및 라이선스 URL 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3b67-211">Step 3: Obtain RMS tenant ID and licensing URL</span></span>

<span data-ttu-id="c3b67-p120">다음 단계는 ID와 조직에 대 한 Azure RMS 서비스에 대 한 라이선스 위치 URL 테 넌 트를 가져옵니다. 복사 하 고 2 단계에서에서 대칭 키가 포함 된 동일한 파일에이 정보를 저장 합니다. ID 및 URL는 PST 파일을 암호화 하려면 5 단계에서에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p120">The next step is to obtain the tenant ID and licensing location URL for the Azure RMS service for your organization. Copy and save this information to the same file that contains the symmetric key from Step 2. The ID and URL will be used in Step 5 to encrypt your PST files.</span></span>
  
1. <span data-ttu-id="c3b67-215">(Microsoft 온라인 서비스에 연결 된)는 Windows PowerShell 용 Azure Active Directory 모듈을 Office 365 조직에서 Azure RMS 서비스에 연결 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-215">In the Azure Active Directory Module for Windows PowerShell (which is connected to the Microsoft Online service), run the following command to connect to the Azure RMS service in your Office 365 organization.</span></span>
    
    ```
    Connect-AadrmService 
    ```

2. <span data-ttu-id="c3b67-216">Office 365 조직에서 관리자 계정에 대 한 자격 증명을 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-216">Enter the credentials for an administrator account in your Office 365 organization and then click **OK**.</span></span>
    
3. <span data-ttu-id="c3b67-217">Office 365 조직에서 Azure RMS 서비스에 대 한 테 넌 트 ID를 표시 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-217">Run the following command to display the tenant ID for the Azure RMS service in your Office 365 organization.</span></span>
    
    ```
    Get-AadrmConfiguration | FL BPOSId
    ```

    <span data-ttu-id="c3b67-218">복사 하 고 저장에 대 한 값은 `BPOSId` 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-218">Copy and save the value for the  `BPOSId` property.</span></span> 
    
4. <span data-ttu-id="c3b67-219">Azure RMS 서비스에 대 한 라이선스 위치를 표시 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-219">Run the following command to display the licensing location for your Azure RMS service.</span></span>
    
    ```
    Get-AadrmConfiguration | FL LicensingIntranetDistributionPointUrl
    ```

    <span data-ttu-id="c3b67-220">복사 하 고 저장에 대 한 값은 `LicensingIntranetDistributionPointUrl` 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-220">Copy and save the value for the  `LicensingIntranetDistributionPointUrl` property.</span></span> 

## <a name="step-4-download-the-pst-import-tools-and-copy-the-sas-url"></a><span data-ttu-id="c3b67-221">PST 가져오기 도구를 다운로드 하 고 SAS URL을 복사 하는 4 단계:</span><span class="sxs-lookup"><span data-stu-id="c3b67-221">Step 4: Download the PST Import tools and copy the SAS URL</span></span>

<span data-ttu-id="c3b67-p121">이제 Azure RMS를 구성 하 고 PST 파일을 암호화 하는 데 필요한 Id를 확보 했을 때 다음 단계를 사용 하도록 다운로드 하 고 Office 365를 암호화 하려면 5 단계에서에서 실행 되 고 업로드 PST 파일을 하는 도구를 설치 합니다. 이러한 도구는 Azure AzCopy 도구와 Office 365 데이터 암호화 도구는 합니다. 또한 조직에 대 한 SAS URL을 복사할 수 있습니다. 이 URL은 조직 및 공유 액세스 서명 (SAS) 키에 대 한 Microsoft 클라우드 Azure 저장소 위치에 대 한 네트워크 URL의 조합입니다. 이 키는 Azure 저장소 위치에 PST 파일을 업로드 하려면 필요한 권한을 제공 합니다. 저장 동일한 파일에는 다른 정보를 2 단계와 3 단계에서 복사한 합니다. 앞서 설명한 것 처럼 SAS URL을 보호 하기 위해 예방 조치를 취하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p121">Now that you've configured Azure RMS and obtained the IDs necessary to encrypt PST files, the next step is to download and install the tools that you will run in Step 5 to encrypt and upload PST files to Office 365. These tools are the Azure AzCopy tool and the Office 365 Data Encryption tool. You'll also copy the SAS URL for your organization. This URL is a combination of the network URL for the Azure storage location in the Microsoft cloud for your organization and a Shared Access Signature (SAS) key. This key provides you with the necessary permissions to upload PST files to your Azure storage location. Save it to the same file that you've copied the other information to in Step 2 and Step 3. As previously stated, take precautions to protect the SAS URL.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c3b67-p122">성공적으로 Azure 저장소 위치에 PST 파일을 업로드 하려면 Azure AzCopy 버전 5.0 사용 해야 합니다. 최신 버전의 AzCopy 도구는 Office 365에 PST 파일을 가져오기 위한 지원 되지 않습니다. 이 단계의 절차를 수행 하 여 **네트워크를 통해 파일 업로드** 페이지에서 AzCopy 도구를 다운로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p122">You have to use Azure AzCopy version 5.0 to successfully upload PST files to the Azure storage location. Newer versions of the AzCopy tool aren't supported for importing PST files to Office 365. Be sure to download the AzCopy tool from the **Upload files over the network** page by following the procedures in this step.</span></span> 
  
1. <span data-ttu-id="c3b67-232">이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-232">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="c3b67-233">Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-233">Sign in to Office 365 using the credentials for an administrator account in your Office 365 organization.</span></span>
    
3. <span data-ttu-id="c3b67-234">왼쪽된 창에서 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-234">In the left pane, click **Data governance** and then click **Import**.</span></span>
    
4. <span data-ttu-id="c3b67-235">**가져오기** 페이지에서 **가져오기 서비스로 이동**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-235">On the **Import** page, click **Go to the Import service**.</span></span>
    
5. <span data-ttu-id="c3b67-236">**Office 365로 데이터 가져오기** 페이지에서 **새 작업** 을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif), **업로드 전자 메일 메시지 (PST 파일)를**클릭 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-236">On the **Import data to Office 365** page, click **New job** ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then click **Upload email messages (PST files)**.</span></span>
    
6. <span data-ttu-id="c3b67-237">2 단계에서 **네트워크를 통해 파일 업로드** 페이지에서 **네트워크 업로드 SAS URL 표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-237">On the **Upload files over the network** page, in step 2, click **Show network upload SAS URL**.</span></span>
    
7. <span data-ttu-id="c3b67-p123">URL이 표시 되 면 복사 하 고 다른 키를 저장 하 여 파일에 저장 합니다. 전체 URL을 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p123">After the URL is displayed, copy it and save it in the file where you saved the other keys. Be sure to copy the entire URL.</span></span> 
    
8. <span data-ttu-id="c3b67-240">3 단계에서 다운로드 하 고 Azure AzCopy 도구를 설치 하려면 **Azure AzCopy 도구를 다운로드** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-240">In step 3, click **Download the Azure AzCopy tool** to download and install the Azure AzCopy tool.</span></span> 
    
9. <span data-ttu-id="c3b67-241">팝업 창에서 **실행**을 클릭하여 Azure AzCopy 도구를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-241">In the pop-up window, click **Run** to install the Azure AzCopy tool.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="c3b67-p124">기본 위치, 즉에서 Azure AzCopy 도구를 설치 해야 `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` 하는 컴퓨터에서 64 비트 Windows를 실행 합니다. 5 단계에서에서의 O365ImportTool.exe를 실행 하는 경우을 찾고이 위치에서 AzCopy 도구 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p124">Be sure to install the Azure AzCopy tool in the default location, which is `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` on a computer running 64-bit Windows. That's because when you run the O365ImportTool.exe in Step 5, it looks for the AzCopy tool in this location.</span></span> 
  
10. <span data-ttu-id="c3b67-244">Azure AzCopy 도구를 설치한 후에 **Office 365 데이터 암호화 및 가져오기 도구를 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-244">After you've installed the Azure AzCopy tool, click **Download the Office 365 Data Encryption and Import tool**.</span></span>
    
11. <span data-ttu-id="c3b67-245">팝업 창에서 **저장** 을 클릭 \> 로컬 컴퓨터의 폴더에 O365ImportTool.zip 파일을 저장 하려면 **로 저장** 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-245">In the pop-up window, click **Save** \> **Save as** to save the O365ImportTool.zip file to a folder on your local computer.</span></span> 
    
12. <span data-ttu-id="c3b67-246">O365ImportTool.zip 파일의 압축을 풉니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-246">Extract the O365ImportTool.zip file.</span></span>
    
13. <span data-ttu-id="c3b67-247">**네트워크를 통해 파일 업로드** 페이지를 닫으려면 **취소** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-247">Click **Cancel** to close the **Upload files over the network** page.</span></span> 
 
## <a name="step-5-encrypt-and-upload-your-pst-files-to-office-365"></a><span data-ttu-id="c3b67-248">5 단계: 암호화 하 고 Office 365에 PST 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-248">Step 5: Encrypt and upload your PST files to Office 365</span></span>

<span data-ttu-id="c3b67-p125">단계 1 ~ 4 단계를 완료 한 도구를 사용 하 여 O365ImportTool.exe를 암호화 하 여 Office 365에 PST 파일을 업로드할 준비가 된 것입니다. 이 도구 PST 파일을 암호화 하 고 업로드 하 고 Microsoft 클라우드에서는 Azure 저장소 위치에 저장 합니다. 이 단계를 완료 하려면 PST 파일에는 파일 공유 또는 조직에서 파일 서버에 배치 해야 합니다. 이 다음 절차에는 원본 디렉터리 이라고 합니다. O365ImportTool.exe 도구를 실행할 때마다 하겠습니다 지정할 수 있습니다 다른 원본 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p125">After you have completed Step 1 through Step 4, you're ready to use the O365ImportTool.exe tool to encrypt and upload PST files to Office 365. This tool encrypts your PST files and then uploads and stores them in an Azure storage location in the Microsoft cloud. To complete this step, the PST files have to be located in a file share or file server in your organization. This is known as the source directory in the following procedure. Each time you run the O365ImportTool.exe tool, you'll can specify a different source directory.</span></span> 
  
1. <span data-ttu-id="c3b67-254">로컬 컴퓨터에서 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-254">Open a Command Prompt on your local computer.</span></span>
    
2. <span data-ttu-id="c3b67-255">4단계에서 O365ImportTool.exe 도구를 설치한 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-255">Go to the directory where you installed the O365ImportTool.exe tool in Step 4.</span></span>
    
3. <span data-ttu-id="c3b67-256">암호화 하 고 Office 365에 PST 파일을 업로드 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-256">Run the following command to encrypt and upload PST files to Office 365.</span></span>
    
    ```
    O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL> /upload-destSAS:<SAS key>
    ```

    <span data-ttu-id="c3b67-p126">다음 표에서는 매개 변수와 해당 필수 값에 대해 설명합니다. 이전 단계에서 획득한 정보가 이러한 매개 변수의 값에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p126">The following table describes the parameters and their required values. Note that the information you obtained in the previous steps is used in the values for these parameters.</span></span>
    
    |<span data-ttu-id="c3b67-259">**매개 변수**</span><span class="sxs-lookup"><span data-stu-id="c3b67-259">**Parameter**</span></span>|<span data-ttu-id="c3b67-260">**설명**</span><span class="sxs-lookup"><span data-stu-id="c3b67-260">**Description**</span></span>|<span data-ttu-id="c3b67-261">**예제**</span><span class="sxs-lookup"><span data-stu-id="c3b67-261">**Example**</span></span>|
    |:-----|:-----|:-----|
    | `/srcdir:` <br/> |<span data-ttu-id="c3b67-262">Office 365로 업로드 됩니다 PST 파일을 포함 하 여 조직에서 원본 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-262">Specifies the source directory in your organization that contains the PST files that will be uploaded to Office 365.</span></span>  <br/> | `/srcdir:\\FILESERVER01\PSTs` <br/> |
    | `/protect-rmsserver:` <br/> |<span data-ttu-id="c3b67-p127">Azure RMS 서비스에 대 한 라이선스 위치를 지정합니다. 값을 사용 하는 `LicensingIntranetDistributionPointUrl` 3 단계에서에서 얻은 속성입니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("")</span><span class="sxs-lookup"><span data-stu-id="c3b67-p127">Specifies the licensing location for your Azure RMS service. Use the value of the  `LicensingIntranetDistributionPointUrl` property that you obtained in Step 3. Be sure to surround the value of this parameter with double-quotation marks (" ")  </span></span><br/> | `/protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing"` <br/> |
    | `/protect-tenantid:` <br/> |<span data-ttu-id="c3b67-p128">Azure RMS 조직의 id를 지정 합니다. 값을 사용 하는 `BPOSId` 3 단계에서에서 얻은 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p128">Specifies the identity of your Azure RMS organization. Use the value of the  `BPOSId` property that you obtained in Step 3.  </span></span><br/> | `/protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b` <br/> |
    | `/protect-key:` <br/> |<span data-ttu-id="c3b67-p129">2 단계에서에서 구한 대칭 키를 지정 합니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").</span><span class="sxs-lookup"><span data-stu-id="c3b67-p129">Specifies the symmetric key that you obtained in Step 2. Be sure to surround the value of this parameter with double-quotation marks (" ").</span></span>  <br/> | `/protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867="` <br/> |
    | `/transfer:` <br/> |<span data-ttu-id="c3b67-p130">네트워크를 통해 PST 파일을 업로드 또는 하드 드라이브에 보내줄 하 여부를 지정 합니다. 값 `upload` 네트워크를 통해이 파일을 업로드는 나타냅니다. 값 `drive` 하드 드라이브에는 Pst 제공를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p130">Specifies whether you upload PST files over the network or ship them on a hard drive. The value  `upload` indicates that you are uploading the files over the network. The value  `drive` indicates that you are shipping the PSTs on a hard drive.  </span></span><br/> | `/transfer:upload` <br/> |
    | `/upload-dest:` <br/> |<span data-ttu-id="c3b67-p131">Office 365; PST 파일은 업로드 하는 위치에서 대상 지정 조직에 대 한 Azure 저장소 위치입니다. 이 매개 변수에 대 한 값 4 단계에서에서 복사한 SAS URL에서 네트워크 업로드 URL로 구성 됩니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").</span><span class="sxs-lookup"><span data-stu-id="c3b67-p131">Specifies the destination in Office 365 where your PST files will be uploaded to; this is the Azure storage location for your organization. The value for this parameter consists of the network upload URL from the SAS URL that you copied in Step 4. Be sure to surround the value of this parameter with double-quotation marks (" ").  </span></span><br/><br/> <span data-ttu-id="c3b67-p132">**팁:** (선택 사항) 암호화 된 PST 파일을 업로드 하려면 Azure 저장소 위치에 하위 폴더를 지정할 수 있습니다. 네트워크 업로드 URL에 "ingestiondata") (이후 하위 폴더 위치를 추가 하 여이 작업을 수행 합니다. 첫번째 예제에서는; 하위 폴더를 지정 하지 않으면 즉, Azure 저장소 위치는 Pst ( *ingestiondata* 라는) 루트에 업로드 합니다. 두번째 예제 Azure 저장소 위치에서 ( *EncryptedPSTs* 라는) 하위 폴더에 PST 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p132">**Tip:** (Optional) You can specify a subfolder in the Azure storage location to upload the encrypted PST files to. You do this by adding a subfolder location (after "ingestiondata") in the network upload URL. The first example doesn't specify a subfolder; that means the PSTs will be uploaded to the root (named  *ingestiondata*  ) of the Azure storage location. The second example uploads the PST files to a subfolder (named  *EncryptedPSTs*  ) in the Azure storage location.</span></span>           | `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata"` <br/> <span data-ttu-id="c3b67-280">또는</span><span class="sxs-lookup"><span data-stu-id="c3b67-280">Or</span></span>  <br/>  `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs"` <br/> |
    | `/upload-destSAS:` <br/> |<span data-ttu-id="c3b67-p133">조직에 대 한 SAS 키를 지정합니다. 4 단계에서에서 복사한 SAS URL에서 SAS 키의 값이 매개이 변수에 대 한 구성 됩니다. SAS 키의 첫 문자는 물음표 ("?"). 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").</span><span class="sxs-lookup"><span data-stu-id="c3b67-p133">Specifies the SAS key for you organization. The value for this parameter consists of the SAS key from the SAS URL that you copied in Step 4. Note that first character in the SAS key is a question mark ("?"). Be sure to surround the value of this parameter with double-quotation marks (" ").</span></span>  <br/> | `/upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/recurse` <br/> |<span data-ttu-id="c3b67-285">이 선택적 스위치 O365ImportTool.exe 도구에서는로 지정 된 원본 디렉터리의 하위 폴더에 있는 Pst 파일을 복사 되도록 재귀 모드를 지정 된 `/srcdir:` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-285">This optional switch specifies the recursive mode so that the O365ImportTool.exe tool will copy PSTs files that are located in subfolders in the source directory that is specified by the  `/srcdir:` parameter.</span></span>  <br/><br/> <span data-ttu-id="c3b67-p134">**참고:** 이 스위치를 포함 하는 경우 하위 폴더에서 PST 파일 다른 파일 경로 이름에에서 갖습니다 Azure 저장소 위치는 업로드 하 고 나면. 7 단계에서에서 만든 CSV 파일의 정확한 파일 경로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p134">**Note:** If you include this switch, PST files in subfolders will have a different file pathname in the Azure storage location after they're uploaded. You'll have to specify the exact file pathname in the CSV file that you create in Step 7.</span></span>           | `/recurse` <br/> |
   
    <span data-ttu-id="c3b67-288">다음은 각 매개 변수의 실제 값을 사용하는 O365ImportTool.exe 도구의 구문 예입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-288">Here's an example of the syntax for the O365ImportTool.exe tool using actual values for each parameter:</span></span>
    
    ```
    O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b  /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
    ```

    <span data-ttu-id="c3b67-p135">이 명령을 실행하면 PST 파일의 암호화 및 업로드 진행률을 보여 주는 상태 메시지가 표시됩니다. 마지막 상태 메시지는 성공적으로 암호화 및 업로드된 파일의 총 수를 표시합니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-p135">After you run the command, status messages are displayed that show the progress of encrypting and uploading the PST files. A final status message shows the total number of files that were successfully encrypted and uploaded.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="c3b67-p136">성공적으로 O365ImportTool.exe 명령을 실행 하 고 매개 변수를 모두 올바른지 확인, 후 명령줄 구문 정보를 복사한 동일한 (보안) 파일의 복사본 저장 획득 이전 단계에서 합니다. 다음 복사 수 있으며를 암호화 하 여 Office 365에 PST 파일을 업로드할 O365ImportTool.exe 도구를 실행할 때마다 명령 프롬프트에서이 명령을 붙여넣습니다. 변경 해야할 유일한 값은에 대 한 것과 `/srcdir:` 및 `/upload-dest:` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p136">After you successfully run the O365ImportTool.exe command and verify that all the parameters are correct, save a copy of the command line syntax to the same (secured) file where you copied the information you obtained in the previous steps. Then you can copy and paste this command in a Command Prompt each time that you want to run the O365ImportTool.exe tool to encrypt and upload PST files to Office 365. The only values you might have to change are the ones for the  `/srcdir:` and  `/upload-dest:` parameters.</span></span> 
  
## <a name="optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365"></a><span data-ttu-id="c3b67-294">(선택 사항) Office 365에 보기 PST 파일의 목록이 업로드 6 단계:</span><span class="sxs-lookup"><span data-stu-id="c3b67-294">(Optional) Step 6: View a list of the PST files uploaded to Office 365</span></span>

<span data-ttu-id="c3b67-p137">단계는 선택 사항으로 설치 하 고 (즉, 무료, 공개 소스 도구) Microsoft Azure 저장소 탐색기를 사용 하 여 Azure blob에 업로드 했을 때 PST 파일의 목록을 볼 수 있습니다. 이 작업을 수행 하는 이유에 세 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p137">As an optional step, you can install and use the Microsoft Azure Storage Explorer (which is a free, open source tool) to view the list of the PST files that you've uploaded to the Azure blob. There are three good reasons to do this:</span></span>
  
- <span data-ttu-id="c3b67-297">공유 폴더 또는 조직에서 파일 서버에서 PST 파일은 Azure blob에 성공적으로 업로드 된 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-297">Verify that PST files from the shared folder or file server in your organization were successfully uploaded to the Azure blob.</span></span>

- <span data-ttu-id="c3b67-p138">PST 파일의 암호화를 확인 합니다. 암호화 된 PST 파일을 `.pfile` PST filename;에 추가 된 확장 예, `pilarp.pst.pfile`합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p138">Verify that the PST files are encrypted. Encrypted PST files have a  `.pfile` extension appended to the PST filename; for example,  `pilarp.pst.pfile`.</span></span>
    
- <span data-ttu-id="c3b67-p139">Azure blob를 업로드 한 각 PST 파일에 대 한 파일 이름 (및 하위 폴더 경로 이름을 하나를 포함 하는 경우)를 확인 합니다. 폴더 경로 각 PST 파일에 대 한 이름을 모두 지정 해야 하기 때문에 다음 단계에서 파일에 매핑 PST를 작성할 때 매우 유용 합니다. 이 이름 확인 (영문) PST 매핑 파일의 잠재적인 오류를 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p139">Verify the filename (and the subfolder pathname if you included one) for each PST file uploaded to the Azure blob. This is really helpful when you're creating the PST mapping file in the next step because you have to specify both the folder pathname and filename for each PST file. Verifying these names can help reduce potential errors in your PST mapping file.</span></span>
    
<span data-ttu-id="c3b67-303">Microsoft Azure 저장소 탐색기 미리 보기에서 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-303">The Microsoft Azure Storage Explorer is in Preview.</span></span> 
  
 > [!IMPORTANT]
>  <span data-ttu-id="c3b67-p140">Azure 저장소 탐색기를 사용 하 여 업로드 하거나 PST 파일을 수정 하려면 수는 없습니다. Office 365에 PST 파일을 가져오기 위한 유일한 방법은 지원된 AzCopy를 사용 하는 것입니다. 또한 Azure blob를 업로드 한 PST 파일을 삭제할 수 없습니다. PST 파일을 삭제 하려고 하는 경우 필요한 사용 권한을 있지 않은 경우에 대 한 오류가 표시 됩니다. 참고 모든 PST 파일 Azure 저장소 영역에서 자동으로 삭제 됩니다. 없는 경우 진행 상황을 **ingestiondata** 컨테이너에 있는 다음 모든 PST 파일에 가져오기 작업이 30 일 가장 최근의 가져오기 작업을 만든 후 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p140">You can't use the Azure Storage Explorer to upload or modify PST files. The only supported method for importing PST files to Office 365 is to use AzCopy. Also, you can't delete PST files that you've uploaded to the Azure blob. If you try to delete a PST file, you'll receive an error about not having the required permissions. Note that all PST files are automatically deleted from your Azure storage area. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created.</span></span> 
  
<span data-ttu-id="c3b67-310">Azure 저장소 탐색기를 설치 및 Azure 저장소 영역에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-310">To install the Azure Storage Explorer and connect to your Azure storage area:</span></span>
  
1. <span data-ttu-id="c3b67-311">다운로드 하 고 [Microsoft Azure 저장소 탐색기 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-311">Download and install the [Microsoft Azure Storage Explorer tool](https://go.microsoft.com/fwlink/p/?LinkId=544842).</span></span>
    
2. <span data-ttu-id="c3b67-312">Microsoft Azure 저장소 탐색기를 시작 하 고 왼쪽된 창에서 **계정 저장소를** 마우스 오른쪽 단추로 클릭 **Azure 저장소에 대 한 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-312">Start the Microsoft Azure Storage Explorer, right-click **Storage Accounts** in the left pane, and then click **Connect to Azure storage**.</span></span> 
    
    ![저장소 계정을 마우스 오른쪽 단추로 클릭 하 고 Azure 저장소에 연결을 클릭 한 다음](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. <span data-ttu-id="c3b67-314">**Azure 저장소에**연결 상자에서 4 단계에서에서 구한 SAS URL 붙여넣은 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-314">In the box under **Connect to Azure storage**, paste the SAS URL that you obtained in Step 4, and then click **Next**.</span></span> 
    
    ![SAS URL Azure 저장소 페이지에 연결 상자에 붙여넣기](media/5d034128-e087-48e1-9ebc-4c9fa262d5b7.png)
  
4. <span data-ttu-id="c3b67-316">**연결 요약** 페이지에서 연결 정보를 검토 하 고 **연결**을 클릭 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-316">On the **Connection summary** page, you can review the connection information, and then click **Connect**.</span></span> 
    
5. <span data-ttu-id="c3b67-317">**저장소 계정**아래에서 **서비스 SAS ()** 노드를 확장 하 고 **Blob 컨테이너** 노드를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-317">Under **Storage Accounts**, expand the **(Service SAS)** node, and then expand the **Blob Containers** node.</span></span> 
    
6. <span data-ttu-id="c3b67-318">**Ingestiondata**마우스 오른쪽 단추로 클릭 하 고 **Blob 컨테이너 편집기 열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-318">Right-click **ingestiondata**, and then click **Open Blob Container Editor**.</span></span>
    
    ![ingestiondata를 마우스 오른쪽 단추로 클릭한 다음 Blob 컨테이너 편집기 열기를 클릭합니다.](media/f50eee30-9202-4efc-904a-2895a0bc388d.png)
  
    <span data-ttu-id="c3b67-320">Azure 저장소 영역 5 단계에서에서 업로드 PST 파일의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-320">The Azure storage area, with a list of the PST files that you uploaded in Step 5 is displayed.</span></span>
    
    ![Azure 저장소 탐색기는 사용자가 업로드한 PST 파일 목록이 표시됩니다.](media/a448ae43-e744-4153-8304-22b59e93883c.png)
  
7. <span data-ttu-id="c3b67-p141">Microsoft Azure 저장소 탐색기를 사용 하 여이 끝나면 **ingestiondata**마우스 오른쪽 단추로 클릭 하 고 Azure 저장소 영역에서 연결을 끊으려면 **분리** 클릭 합니다. 그렇지 않은 경우 받게 오류가 다음에 연결 하려고 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p141">When you're finished using the Microsoft Azure Storage Explorer, right-click **ingestiondata**, and then click **Detach** to disconnect from your Azure storage area. Otherwise, you'll receive an error the next time you try to attach.</span></span> 
    
    ![수집을 마우스 오른쪽 단추로 클릭하고 분리를 클릭하여 Azure 저장소 영역에서 연결 끊기](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-7-create-the-pst-import-mapping-file"></a><span data-ttu-id="c3b67-325">7 단계: PST 가져오기 매핑 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="c3b67-325">Step 7: Create the PST Import mapping file</span></span>

<span data-ttu-id="c3b67-p142">PST 파일을 암호화 하 고 Office 365 조직에 대 한 Azure 저장소 위치에 업로드 한 후 다음 단계에 쉼표를 만들려는 구분 하 여 PST 파일을 가져올 수는 어떤 사용자 사서함을 지정 하는 값 (CSV) 파일입니다. PST 가져오기 작업을 만들 때에 다음 단계에는이 CSV 파일을 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p142">After the PST files have been encrypted and uploaded to the Azure storage location for your Office 365 organization, the next step is to create a comma separated value (CSV) file that specifies which user mailboxes the PST files will be imported to. You will submit this CSV file in the next step when you create a PST Import job.</span></span>
  
1. <span data-ttu-id="c3b67-328">[PST 가져오기 매핑 파일의 복사본을 다운로드](https://go.microsoft.com/fwlink/p/?LinkId=544717)합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-328">[Download a copy of the PST Import mapping file](https://go.microsoft.com/fwlink/p/?LinkId=544717).</span></span> 
    
2. <span data-ttu-id="c3b67-p143">CSV 파일을 열거나 로컬 컴퓨터에 저장합니다. 다음 예에서는 완료된 PST 가져오기 매핑 파일(메모장에서 열림)을 보여 줍니다. CSV 파일을 편집할 경우 Microsoft Excel을 사용하는 것이 훨씬 더 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p143">Open or save the CSV file to your local computer. The following example shows a completed PST Import mapping file (opened in NotePad). It's much easier to use Microsoft Excel to edit the CSV file.</span></span>
    
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

    <span data-ttu-id="c3b67-p144">첫째 행 또는 CSV 파일의 머리글 행을 사용자 사서함에 PST 파일을 가져오려면 PST 가져오기 서비스에서 사용 되는 매개 변수를 나열 합니다. 각 매개 변수 이름은 쉼표로 구분 됩니다. 각 행 머리글 행에서 특정 사서함에 PST 파일 가져오기 (영문)에 대 한 매개 변수 값을 나타냅니다. 가져올 사용자 사서함에는 각 PST 파일에 대 한 행을 할 수 있습니다. 실제 데이터와 매핑 파일의 개체 틀 데이터를 교체 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p144">The first row, or header row, of the CSV file lists the parameters that will be used by the PST Import service to import the PST files to user mailboxes. Each parameter name is separated by a comma. Each row under the header row represents the parameter values for importing a PST file to a specific mailbox. You will need a row for each PST file that you want to import to a user mailbox. Be sure to replace the placeholder data in the mapping file with your actual data.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c3b67-337">SharePoint 매개 변수를 포함하여 머리글 행의 어떤 내용도 변경하지 않도록 합니다. 변경한 내용은 PST 가져오기 프로세스 동안 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-337">Don't change anything in the header row, including the SharePoint parameters; they will be ignored during the PST Import process.</span></span> 
  
3. <span data-ttu-id="c3b67-338">다음 표의 정보를 사용하여 CSV 파일을 필요한 정보로 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-338">Use the information in the following table to populate the CSV file with the required information.</span></span>
    
    |<span data-ttu-id="c3b67-339">**매개 변수**</span><span class="sxs-lookup"><span data-stu-id="c3b67-339">**Parameter**</span></span>|<span data-ttu-id="c3b67-340">**설명**</span><span class="sxs-lookup"><span data-stu-id="c3b67-340">**Description**</span></span>|<span data-ttu-id="c3b67-341">**예제**</span><span class="sxs-lookup"><span data-stu-id="c3b67-341">**Example**</span></span>|
    |:-----|:-----|:-----|
    | `Workload` <br/> |<span data-ttu-id="c3b67-p145">데이터를 가져올 수는 Office 365 서비스를 지정 합니다. 사용자 사서함을 PST 파일을 가져오려면, 사용 `Exchange`합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p145">Specifies the Office 365 service that data will be imported to. To import PST files to user mailboxes, use  `Exchange`.  </span></span><br/> | `Exchange` <br/> |
    | `FilePath` <br/> |<span data-ttu-id="c3b67-344">5 단계에서에서 PST 파일을 업로드 하는 Azure 저장소 위치에 폴더 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-344">Specifies the folder location in the Azure storage location that you uploaded the PST files to in Step 5.</span></span>  <br/>  <span data-ttu-id="c3b67-p146">네트워크 URL에는 선택적 하위 폴더 이름을 포함 하지 않았으므로 하는 경우는 `/upload-dest:` 매개 변수 5 단계에서에서이 매개 변수를 비워둘 CSV 파일에 있습니다. 하위 폴더 이름을 포함 하는 경우이 매개 변수에서 지정 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다. 두 방법 모두에 대 한 값에 "ingestiondata"를 포함 *하지* 는 `FilePath` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p146">If you didn't include an optional subfolder name in the network URL in the  `/upload-dest:` parameter in Step 5, leave this parameter blank in the CSV file. If you included a subfolder name, specify it in this parameter. The value for this parameter is case sensitive. Either way,  *don't*  include "ingestiondata" in the value for the  `FilePath` parameter.  </span></span><br/> <br/><span data-ttu-id="c3b67-p147">**중요:** 파일 경로 이름에 대 한 대/소문자에 SAS URL에는 선택적 하위 폴더 이름을 포함 하는 경우를 사용 하는 동일한 대/소문자 여야 합니다.의 `/upload-dest:` 5 단계에서에서 매개 변수입니다. 예: 사용 하는 경우 `EncryptedPSTs` 하위 폴더에 대 한 5 단계에서에서 이름을 지정 하 고 다음을 사용 `encryptedpsts` 에 `FilePath` CSV 파일의 매개 변수, PST 파일에 대 한 가져오기가 실패 합니다. 두 경우 모두 동일한 대/소문자를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p147">**Important:** The case for the file path name must be the same case that you used if you included an optional subfolder name in the SAS URL in the  `/upload-dest:` parameter in Step 5. For example, if you used  `EncryptedPSTs` for the subfolder name in Step 5 and then use  `encryptedpsts` in the  `FilePath` parameter in CSV file, the import for the PST file will fail. Be sure to use the same case in both instances.</span></span>           |<span data-ttu-id="c3b67-352">(공백으로 둠)</span><span class="sxs-lookup"><span data-stu-id="c3b67-352">(leave blank)</span></span>  <br/> <span data-ttu-id="c3b67-353">또는</span><span class="sxs-lookup"><span data-stu-id="c3b67-353">Or</span></span>  <br/>  `EncryptedPSTs` <br/> |
    | `Name` <br/> |<span data-ttu-id="c3b67-p148">사용자 사서함에 가져올 PST 파일의 이름을 지정 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다. Azure 저장소 위치에 업로드 되는 PST 파일을 암호화 하기 때문에 `.pfile` 에 PST 파일 이름 확장명을 추가 합니다. 추가 해야는 `.pfile` CSV 파일에서 파일을 PST의 이름에 대 한 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p148">Specifies the name of the PST file that will be imported to the user mailbox. The value for this parameter is case sensitive. Because the PST files that are uploaded to the Azure storage location are encrypted, a  `.pfile` extension is added to the PST filename. You must add the  `.pfile` extension to the name of the PST files in the CSV file.  </span></span><br/><br/> <span data-ttu-id="c3b67-p149">**중요:** CSV 파일에서 PST 파일 이름에 대 한 대/소문자 5 단계에서에서 Azure 저장소 위치에 업로드 된 PST 파일로 동일 해야 합니다. 예: 사용 하는 경우 `annb.pst.pfile` 에 `Name` 하 여 CSV 파일을 하지만 실제 PST 파일의 이름에서 매개 변수는 `AnnB.pst`, 해당 PST 파일에 대 한 가져오기가 실패 합니다. CSV 파일의 PST의 이름이 동일한 대/소문자를 사용 하 여 실제 PST 파일로 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p149">**Important:** The case for the PST file name in the CSV file must be the same as the PST file that was uploaded to the Azure storage location in Step 5. For example, if you use  `annb.pst.pfile` in the  `Name` parameter in the CSV file, but the name of the actual PST file is  `AnnB.pst`, the import for that PST file will fail. Be sure that the name of the PST in the CSV file uses the same case as the actual PST file.</span></span>           | `annb.pst.pfile` <br/> |
    | `Mailbox` <br/> |<span data-ttu-id="c3b67-361">PST 파일을 가져올 사서함의 전자 메일 주소를 지정합니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-361">Specifies the email address of the mailbox that the PST file will be imported to.</span></span>  <br/> <span data-ttu-id="c3b67-p150">비활성 사서함을 PST 파일을 가져오려면,이 매개 변수에 대 한 사서함 GUID를 지정 해야 합니다. 이 GUID를 가져오려면 다음 PowerShell 명령을 Exchange Online에서 실행: ' Get-mailbox InactiveMailboxOnly<identity of inactive mailbox></span><span class="sxs-lookup"><span data-stu-id="c3b67-p150">To import a PST file to an inactive mailbox, you have to specify the mailbox GUID for this parameter. To obtain this GUID, run the following PowerShell command in Exchange Online:  \`Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox></span></span> | <span data-ttu-id="c3b67-364">FL Guid` <br/><br/> **Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-mailbox-<identity of active mailbox></span><span class="sxs-lookup"><span data-stu-id="c3b67-364">FL Guid` <br/><br/> **Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox - <identity of active mailbox></span></span> | <span data-ttu-id="c3b67-365">FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-mailbox- <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox</span><span class="sxs-lookup"><span data-stu-id="c3b67-365">FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-Mailbox - <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox</span></span> | <span data-ttu-id="c3b67-366">FL Guid'</span><span class="sxs-lookup"><span data-stu-id="c3b67-366">FL Guid\`</span></span>           | `annb@contoso.onmicrosoft.com` <br/> <span data-ttu-id="c3b67-367">또는</span><span class="sxs-lookup"><span data-stu-id="c3b67-367">Or</span></span>  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | <span data-ttu-id="c3b67-p151">PST 파일을 사용자의 보관 사서함으로 가져올 것인지 여부를 지정합니다. 다음 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p151">Specifies whether or not to import the PST file to the user's archive mailbox. There are two options:  </span></span><br/> <span data-ttu-id="c3b67-370">**False 이면** 사용자의 기본 사서함을 PST 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-370">**FALSE** Imports the PST file to the user's primary mailbox.</span></span>  <br/> <span data-ttu-id="c3b67-371">**True 이면** 사용자의 보관 사서함을 PST 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-371">**TRUE** Imports the PST file to the user's archive mailbox.</span></span>  <br/>  <span data-ttu-id="c3b67-372">이 매개 변수를 지정 하지 않으면 사용자의 기본 사서함에 PST 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-372">If you leave this parameter blank, the PST file is imported to the user's primary mailbox.</span></span>  <br/><br/> <span data-ttu-id="c3b67-373">**참고:** 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져오려면, 방금이 매개 변수에 대해 **true로** 지정 하 고 메일에 대 한 사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 된 `Mailbox` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-373">**Note:** To import a PST file to a cloud-based archive mailbox for a user whose primary mailbox is on-premises, just specify **TRUE** for this parameter and specify the email address for the user's on-premises mailbox for the  `Mailbox` parameter.</span></span>           | `FALSE` <br/> <span data-ttu-id="c3b67-374">또는</span><span class="sxs-lookup"><span data-stu-id="c3b67-374">Or</span></span>  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | <span data-ttu-id="c3b67-375">PST 파일을 가져온 사서함 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-375">Specifies the mailbox folder that the PST file is imported to.</span></span>  <br/>  <span data-ttu-id="c3b67-376">이 매개 변수를 지정 하지 않고 공백으로 두면 PST 명명 된 **가져온** (받은 편지함 폴더와 다른 기본 사서함 폴더와 동일한 수준) 사서함의 루트 수준에 있는 새 폴더를으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-376">If you leave this parameter blank, the PST will be imported to a new folder named **Imported** located at the root level of the mailbox (the same level as the Inbox folder and the other default mailbox folders).</span></span>  <br/>  <span data-ttu-id="c3b67-377">지정 하는 경우 `/`, PST 파일의 항목에에서 사용자의 받은 편지함 폴더에서 직접 가져올 수 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-377">If you specify  `/`, items in the PST file will be imported directly in to the user's Inbox folder.</span></span>  <br/>  <span data-ttu-id="c3b67-p152">지정 하는 경우 `/<foldername>`, 라는 하위 폴더를 가져올 PST 파일의 항목에에서 * \<foldername\> * 합니다. 예: 사용 하는 경우 `/ImportedPst`, **ImportedPst**라는 하위 폴더에 항목을 가져올 수는 있습니다. 이 하위 폴더에는 사용자의 받은 편지함 폴더에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p152">If you specify  `/<foldername>`, items in the PST file will be imported to a subfolder named  *\<foldername\>*  . For example, if you used  `/ImportedPst`, items would be imported to a subfolder named **ImportedPst**. This subfolder will be located in the user's Inbox folder.  </span></span><br/><br/> <span data-ttu-id="c3b67-381">**팁:** Pst 파일을 가져오려면 가장 적합 한 폴더 위치를 결정할 수 있도록이 매개 변수를 사용해 몇 테스트 일괄 처리를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-381">**Tip:** Consider running a few test batches to experiment with this parameter so you can determine the best folder location to import PSTs files to.</span></span>           |<span data-ttu-id="c3b67-382">(공백으로 둠)</span><span class="sxs-lookup"><span data-stu-id="c3b67-382">(leave blank)</span></span>  <br/> <span data-ttu-id="c3b67-383">또는</span><span class="sxs-lookup"><span data-stu-id="c3b67-383">Or</span></span>  <br/>  `/` <br/> <span data-ttu-id="c3b67-384">또는</span><span class="sxs-lookup"><span data-stu-id="c3b67-384">Or</span></span>  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |<span data-ttu-id="c3b67-p153">이 선택적 매개 변수는 ANSI 파일 형식에서 PST 파일을 가져오기 위해 사용 하 여 코드 페이지에 대 한 숫자 값을 지정 합니다. 이 매개 변수는 일반적으로 이러한 언어 문자 인코딩에 대 한 더블 바이트 문자 집합 (DBCS)을 사용 하기 때문에 중국어, 일본어 및 한국어 (CJK) 조직에서 PST 파일을 가져오기 위해 사용 됩니다. 이 매개 변수는 사서함 폴더 이름에 대 한 DBCS를 사용 하는 언어에 대 한 PST 파일을 가져오려면 사용 되지 않습니다, 하는 경우 폴더 이름은 가져온 후 왜곡 자주는 합니다. 이 매개 변수를 사용 하 여 지원 되는 값의 목록에 대 한 [코드 페이지 식별자](https://go.microsoft.com/fwlink/p/?LinkId=328514)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p153">This optional parameter specifies a numeric value for the code page to use for importing PST files in the ANSI file format. This parameter is used for importing PST files from Chinese, Japanese, and Korean (CJK) organizations because these languages typically use a double byte character set (DBCS) for character encoding. If this parameter isn't used to import PST files for languages that use DBCS for mailbox folder names, the folder names are often garbled after they're imported. For a list of supported values to use for this parameter, see [Code Page Identifiers](https://go.microsoft.com/fwlink/p/?LinkId=328514).  </span></span><br/><br/> <span data-ttu-id="c3b67-p154">**참고:** 앞부분에 명시 된,이 선택적 매개 변수 이며 CSV 파일에 포함할 필요가 없습니다. 또는 포함 하 고 하나 이상의 행에 대 한 값은 비워둡니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p154">**Note:** As previously stated, this is an optional parameter and you don't have to include it in the CSV file. Or you can include it and leave the value blank for one or more rows.</span></span>           |<span data-ttu-id="c3b67-391">(공백으로 둠)</span><span class="sxs-lookup"><span data-stu-id="c3b67-391">(leave blank)</span></span>  <br/> <span data-ttu-id="c3b67-392">또는</span><span class="sxs-lookup"><span data-stu-id="c3b67-392">Or</span></span>  <br/>  <span data-ttu-id="c3b67-393">`932`(ANSI/OEM 일본어에 대 한 코드 페이지 식별자는)</span><span class="sxs-lookup"><span data-stu-id="c3b67-393">`932` (which is the code page identifier for ANSI/OEM Japanese)</span></span>  <br/> |
    | `SPFileContainer` <br/> |<span data-ttu-id="c3b67-394">PST 가져오기의 경우 이 매개 변수를 비워 둡니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-394">For PST Import, leave this parameter blank.</span></span>  <br/> |<span data-ttu-id="c3b67-395">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c3b67-395">Not applicable</span></span>  <br/> |
    | `SPManifestContainer` <br/> |<span data-ttu-id="c3b67-396">PST 가져오기의 경우 이 매개 변수를 비워 둡니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-396">For PST Import, leave this parameter blank.</span></span>  <br/> |<span data-ttu-id="c3b67-397">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c3b67-397">Not applicable</span></span>  <br/> |
    | `SPSiteUrl` <br/> |<span data-ttu-id="c3b67-398">PST 가져오기의 경우 이 매개 변수를 비워 둡니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-398">For PST Import, leave this parameter blank.</span></span>  <br/> |<span data-ttu-id="c3b67-399">해당 없음</span><span class="sxs-lookup"><span data-stu-id="c3b67-399">Not applicable</span></span>  <br/> |
  
## <a name="step-8-create-a-pst-import-job-in-office-365"></a><span data-ttu-id="c3b67-400">8단계: Office 365에서 PST 가져오기 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="c3b67-400">Step 8: Create a PST Import job in Office 365</span></span>

<span data-ttu-id="c3b67-p155">마지막 단계에서는 Office 365에서 가져오기 서비스에서 PST 가져오기 작업을 만드는 것입니다. 앞에서 설명한 것 처럼 7 단계에서에서 만든 PST 가져오기 매핑 파일을 전송 됩니다. 가져오기 서비스에서 해제 하는 매핑 파일의 정보를 사용할 새 작업을 만든 후-암호화 하 고 지정 된 사용자 사서함에 (즉 5 단계에서에서 Office 365에 업로드 한) PST 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p155">The last step is to create the PST Import job in the Import service in Office 365. As previously explained, you will submit the PST Import mapping file that you created in Step 7. After you create the new job, the Import service will use the information in the mapping file to un-encrypt and import the PST files (that you uploaded to Office 365 in Step 5) to the specified user mailbox.</span></span> 
  
1. <span data-ttu-id="c3b67-404">이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-404">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="c3b67-405">Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-405">Sign in to Office 365 using the credentials for an administrator account in your Office 365 organization.</span></span>
    
3. <span data-ttu-id="c3b67-406">왼쪽된 창에서 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-406">In the left pane, click **Data governance** and then click **Import**.</span></span>
    
4. <span data-ttu-id="c3b67-407">**가져오기** 페이지에서 **가져오기 서비스로 이동**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-407">On the **Import** page, click **Go to the Import service**.</span></span>
    
5. <span data-ttu-id="c3b67-408">**Office 365로 데이터 가져오기** 페이지에서 **새 작업**을 클릭![아이콘 추가](media/ITPro-EAC-AddIcon.gif), **업로드 전자 메일 메시지 (PST 파일)를**클릭 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-408">On the **Import data to Office 365** page, click **New job**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then click **Upload email messages (PST files)**.</span></span>
    
6. <span data-ttu-id="c3b67-409">**네트워크를 통해 파일 업로드** 페이지에서 **내 파일 업로드를 완료했습니다.** 및 **매핑 파일에 대한 액세스 권한이 있습니다.** 확인란을 클릭하고 **다음**을 클릭합니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-409">On the **Upload files over the network** page, click the **I'm done uploading my files** and **I have access to the mapping file** check boxes, and then click **Next**.</span></span> 
    
7. <span data-ttu-id="c3b67-410">PST 가져오기 작업의 이름을 입력하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-410">Type a name for the PST Import job, and then click **Next**.</span></span>
    
8. <span data-ttu-id="c3b67-411">**추가** 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 7 단계에서에서 만든 PST 매핑 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-411">Click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) to select the PST Mapping file that you created in Step 7.</span></span> 
    
9. <span data-ttu-id="c3b67-412">CSV 파일의 이름이 목록에 나타나면 선택하고 **유효성 검사**를 클릭하여 CSV 파일에 오류가 있는지 확인합니다. </span><span class="sxs-lookup"><span data-stu-id="c3b67-412">After the name of the CSV file appears in the list, select it and then click **Validate** to check your CSV file for errors.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="c3b67-p156">PST 파일을 암호화 하는 경우의 설명으로 이전는 `.pfile` PST 파일 이름 확장명이 추가 됩니다. 추가 해야는 `.pfile` CSV 파일에서 파일을 PST의 이름에 대 한 확장 합니다. 이렇게 하지 않으면 CSV 파일의 유효성 검사 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p156">As previous explained, when the PST files are encrypted, a  `.pfile` extension is appended to the PST filename. You must add the  `.pfile` extension to the name of the PST files in the CSV file. If you don't, the validation of the CSV file will fail.</span></span> 
  
    <span data-ttu-id="c3b67-p157">PST 가져오기 작업을 만들려면 CSV 파일의 유효성 검사가 성공해야 합니다. 유효성 검사에 실패하는 경우 **상태** 열에서 **유효하지 않음** 링크를 클릭합니다. PST 가져오기 매핑 파일의 복사본이 열리고 실패한 파일의 각 행에 대해 오류 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p157">The CSV file has to be successfully validated to create a PST Import job. If the validation fails, click the **Invalid** link in the **Status** column. A copy of your PST Import mapping file is opened, with a error message for each row in the file that failed.</span></span> 
    
10. <span data-ttu-id="c3b67-419">PST 매핑 파일의 유효성 검사가 성공하면 사용 약관 문서를 읽고 해당 확인란을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-419">When the PST mapping file is successfully validated, read the terms and conditions document, and then click the checkbox.</span></span>
    
11. <span data-ttu-id="c3b67-420">**마침**을 클릭하여 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-420">Click **Finish** to submit the job.</span></span> 
    
    <span data-ttu-id="c3b67-421">작업의 **Office 365로 데이터 가져오기** 페이지에서 PST 가져오기 작업 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-421">The job is displayed in the list of PST Import jobs on the **Import data to Office 365** page.</span></span> 
    
12. <span data-ttu-id="c3b67-422">작업을 선택 하 고 **새로 고칠**을 클릭![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 표시 되는 상태 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-422">Select the job and click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the status information that's displayed in the details pane.</span></span> 
    
13. <span data-ttu-id="c3b67-423">세부 정보 창에서 **자세히 보기**를 클릭하여 선택한 작업에 대한 최신 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-423">In the details pane, click **View details** to get the latest status for the selected job.</span></span> 
 
## <a name="more-information"></a><span data-ttu-id="c3b67-424">추가 정보</span><span class="sxs-lookup"><span data-stu-id="c3b67-424">More information</span></span>

- <span data-ttu-id="c3b67-425">Office 365에 PST 파일을 가져올 이유?</span><span class="sxs-lookup"><span data-stu-id="c3b67-425">Why import PST files to Office 365?</span></span>
    
  - <span data-ttu-id="c3b67-426">Office 365에 조직의 전자 메일을 마이그레이션할 좋은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-426">It's a good way to migrate your organization's email to Office 365.</span></span>
    
  - <span data-ttu-id="c3b67-427">다음을 수행하여 조직의 준수 요구 사항을 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-427">It helps address compliance needs of your organization by letting you:</span></span>
    
  - <span data-ttu-id="c3b67-428">추가 사서함 저장 공간을 사용자에게 제공하도록 보관 사서함을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-428">Enable archive mailboxes to give users additional mailbox storage space.</span></span>
    
  - <span data-ttu-id="c3b67-429">콘텐츠를 보존하도록 보류 중인 사서함을 배치합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-429">Place mailboxes on hold to preserve content.</span></span>
    
  - <span data-ttu-id="c3b67-430">사서함의 콘텐츠를 검색하도록 Microsoft eDiscovery 도구를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-430">Use Microsoft eDiscovery tools to search for content in mailboxes.</span></span>
    
  - <span data-ttu-id="c3b67-431">보존 정책을 사용하여 사서함 콘텐츠 보존 기간을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-431">Use retention policies to control how long mailbox content is retained.</span></span>
    
  - <span data-ttu-id="c3b67-432">사서함과 관련 된 이벤트를 위한 Office 365 감사 로그를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-432">Search the Office 365 audit log for mailbox-related events.</span></span>
    
  - <span data-ttu-id="c3b67-p158">데이터 손실 방지 유용한 정보를 제공 합니다. 사용자의 컴퓨터에서 데이터를 저장 하지 않고 Exchange Online의 고가용성 기능을 상속 하는 PST 파일을 Office 365 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p158">It helps protect against data loss. PST files that are imported to Office 365 mailboxes inherit the high availability features of Exchange Online, as opposed to storing the data on a user's computer.</span></span>
    
  - <span data-ttu-id="c3b67-435">이러한 데이터는 클라우드에 저장되므로 모든 장치에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-435">The data is available to the user from all devices because it's stored in the cloud.</span></span>
    
- <span data-ttu-id="c3b67-p159">키, Id, 2, 3, 4 단계에서 구한 되는 Url의 예는 다음과 같습니다. 이 예제에는 암호화 하는 O365ImportTool.exe 도구에서 실행 하 고 업로드 PST 파일을 Office 365에는 명령에 대 한 구문을 들어 있습니다. 암호 또는 기타 보안 관련 정보를 보호 하는 동일 하 게 이러한 방금 보호 하기 위한 예방 조치를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p159">Here's an example of the keys, IDs, and URLs that are obtained in Steps 2, 3, and 4. This example also contains the syntax for the command that you run in the O365ImportTool.exe tool to encrypt and upload PST files to Office 365. Be sure to take precautions to protect these just like you would protect passwords or other security-related information.</span></span>
    
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

- <span data-ttu-id="c3b67-p160">앞에서 설명한 것 처럼 Office 365 가져오기 서비스 설정 (한 무기한 기간) 사서함에 PST 파일을 가져온 후 보존 대기 상태를 설정 합니다. 즉, *RentionHoldEnabled* 속성이로 설정 된 `True` 사서함에 할당 된 보존 정책 않습니다 처리할 수 있도록 합니다. 삭제 또는 보관 정책을 삭제 하거나 오래 된 메시지를 보관할 수 없도록 하 여 새로 가져온 메시지를 관리 하는 사서함 소유자 시간을 제공 합니다. 이 보존 대기 상태를 관리 하기 위해 수행할 수 있는 일부 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p160">As previously explained, the Office 365 Import service turns on the retention hold setting (for an indefinite duration) after PST files are imported to a mailbox. This means the  *RentionHoldEnabled*  property is set to  `True` so that the retention policy assigned to the mailbox won't be processed. This gives the mailbox owner time to manage the newly-imported messages by preventing a deletion or archive policy from deleting or archiving older messages. Here are some steps you can take to manage this retention hold:</span></span> 
    
  - <span data-ttu-id="c3b67-p161">특정 기간 동안 시간을 한 후 해제할 수 보존 대기를 실행 하 여는 `Set-Mailbox -RetentionHoldEnabled $false` 명령 합니다. 자세한 내용은 [사서함 보존에 원본 위치 유지](https://go.microsoft.com/fwlink/p/?LinkId=544749)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p161">After a certain period of time, you can turn off the retention hold by running the  `Set-Mailbox -RetentionHoldEnabled $false` command. For instructions, see [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/p/?LinkId=544749).</span></span>
    
  - <span data-ttu-id="c3b67-p162">나중에 일부 날짜 꺼져 있도록 보존 대기를 구성할 수 있습니다. 실행 하 여이 작업을 수행 된 `Set-Mailbox -EndDateForRetentionHold <date>` 명령 합니다. 예, 오늘 날짜가 2016 년 7 월 1 일이 고 30 일에서 해제 된 보존 대기 원하는 이라고 가정할 다음 명령을 실행 합니다: `Set-Mailbox -EndDateForRetentionHold 8/1/2016`합니다. 이 시나리오에서는 *RentionHoldEnabled* 속성을 설정 남게 `True`합니다. 자세한 내용은 [Set-mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p162">You can configure the retention hold so that it's turned off on some date in the future. You do this by running the  `Set-Mailbox -EndDateForRetentionHold <date>` command. For example, assuming that today's date is July 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. In this scenario, you would leave the  *RentionHoldEnabled*  property set to `True`. For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).</span></span>
    
  - <span data-ttu-id="c3b67-p163">오래 된 항목을 가져오지 않습니다 수 즉시 삭제 되거나 사용자의 보관 사서함으로 이동 되도록 사서함에 할당 된 보존 정책에 대 한 설정을 변경할 수 있습니다. 예, 사서함에 할당 된 삭제 또는 보관 정책에 대 한 보존 기간을 길게 수 있습니다. 이 시나리오에서는 있습니다 기능을 해제는 사서함에 보존 대기 상태에는 보존 정책의 설정을 변경한 후 합니다. 자세한 내용은 [Office 365 조직 내의 사서함에에서는 보관 및 삭제 정책 설정](set-up-an-archive-and-deletion-policy-for-mailboxes.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3b67-p163">You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).</span></span>
