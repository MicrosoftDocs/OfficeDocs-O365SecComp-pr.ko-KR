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
# <a name="use-drive-shipping-to-import-your-organization-pst-files-to-office-365"></a><span data-ttu-id="72e45-103">드라이브 전달을 사용 하 여 Office 365로 조직 PST 파일을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="72e45-103">Use drive shipping to import your organization PST files to Office 365</span></span>

<span data-ttu-id="72e45-104">**이 문서는 관리자입니다. 자신의 사서함에 PST 파일을 가져올 하려고 합니까? [가져오기 전자 메일, 연락처 및 일정 Outlook.pst 파일에서](https://go.microsoft.com/fwlink/p/?LinkID=785075) 를 참조 하십시오.**</span><span class="sxs-lookup"><span data-stu-id="72e45-104">**This article is for administrators. Are you trying to import PST files to your own mailbox? See [Import email, contacts, and calendar from an Outlook .pst file](https://go.microsoft.com/fwlink/p/?LinkID=785075)**</span></span>
   
<span data-ttu-id="72e45-p101">Office 365를 가져올 서비스 및 대량 가져오기 PST 파일을 사용자 사서함에 전달 하는 드라이브를 사용 합니다. 드라이브 전달 PST 파일을 하드 디스크 드라이브에 복사 하 고 Microsoft에 드라이브를 물리적으로 제공 하는 것을 의미 합니다. Microsoft가 사용자의 하드 드라이브를 받으면 데이터 센터 담당자는 Microsoft 클라우드에서 저장소 영역에 데이터를 하드 드라이브에서 복사 됩니다. 그런 다음 데이터를 가져온 가져옵니다을 제어 하는 필터를 설정 하 여 가져올 대상 사서함에 실제로 PST 데이터 트리밍할 기회를 해야 합니다. 가져오기 작업을 시작한 후 가져오기 서비스 PST 데이터를 사용자 사서함에 저장 영역에서 가져옵니다. 드라이브 전달을 사용 하 여 사용자 사서함에 PST 파일을 가져오려면 Office 365에 조직의 전자 메일을 마이그레이션하는 한 가지 방법은 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p101">Use the Office 365 Import service and drive shipping to bulk-import PST files to user mailboxes. Drive shipping means that you copy the PST files to a hard disk drive and then physically ship the drive to Microsoft. When Microsoft receives your hard drive, data center personnel will copy the data from the hard drive to a storage area in the Microsoft cloud. Then you have the opportunity to trim the PST data that's actually imported to the target mailboxes by setting filters that control what data gets imported. After you start the import job, the Import service imports the PST data from the storage area to user mailboxes. Using drive shipping to import PST files to user mailboxes is one way to migrate your organization's email to Office 365.</span></span>
  
<span data-ttu-id="72e45-111">Office 365 사서함에 PST 파일을 가져오려면 드라이브 전달을 사용 하 여 필요한 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-111">Here are the steps required to use drive shipping to import PST files to Office 365 mailboxes:</span></span>
  
[<span data-ttu-id="72e45-112">1 단계: 보안 저장소 키 및 PST 가져오기 도구를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-112">Step 1: Download the secure storage key and PST Import tool</span></span>](#step-1-download-the-secure-storage-key-and-pst-import-tool)

[<span data-ttu-id="72e45-113">2 단계: PST 파일을 하드 드라이브에 복사</span><span class="sxs-lookup"><span data-stu-id="72e45-113">Step 2: Copy the PST files to the hard drive</span></span>](#step-2-copy-the-pst-files-to-the-hard-drive)

[<span data-ttu-id="72e45-114">3 단계: PST 가져오기 매핑 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="72e45-114">Step 3: Create the PST Import mapping file</span></span>](#step-3-create-the-pst-import-mapping-file)

[<span data-ttu-id="72e45-115">4단계: Office 365에서 PST 가져오기 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="72e45-115">Step 4: Create a PST Import job in Office 365</span></span>](#step-4-create-a-pst-import-job-in-office-365)

[<span data-ttu-id="72e45-116">5단계: Microsoft로 하드 드라이브 발송</span><span class="sxs-lookup"><span data-stu-id="72e45-116">Step 5: Ship the hard drive to Microsoft</span></span>](#step-5-ship-the-hard-drive-to-microsoft)

[<span data-ttu-id="72e45-117">6 단계: 데이터를 필터링 하 고 PST 가져오기 작업 시작</span><span class="sxs-lookup"><span data-stu-id="72e45-117">Step 6: Filter data and start the PST Import job</span></span>](#step-6-filter-data-and-start-the-pst-import-job)
  
> [!IMPORTANT]
> <span data-ttu-id="72e45-p102">아래로 보안 저장소 키 및 가져오기 도구를 로드 한 번 1 단계를 수행 해야 합니다. 다음이 단계를 수행한 후 6 단계를 통해 2 단계를 Microsoft 하드 드라이브를 제공 하려는 때마다를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p102">You have to perform Step 1 once to down load the secure storage key and the import tool. After you perform these steps, follow Step 2 through Step 6 each time you want to ship a hard drive to Microsoft.</span></span> 
  
<span data-ttu-id="72e45-120">자주에 대 한 Office 365로 PST 파일을 가져오는 [PST 파일을 가져오려면 전달 하는 드라이브를 사용 하는 것에 대 한 Faq](faqimporting-pst-files-to-office-365.md#using-drive-shipping-to-import-pst-files)를 참조 하십시오 전달 드라이브를 사용 하는 방법에 대 한 대답 (영문).</span><span class="sxs-lookup"><span data-stu-id="72e45-120">For frequently asked questions about using drive shipping to import PST files to Office 365, see [FAQs for using drive shipping to import PST files](faqimporting-pst-files-to-office-365.md#using-drive-shipping-to-import-pst-files).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="72e45-121">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="72e45-121">Before you begin</span></span>

- <span data-ttu-id="72e45-p103">역할을 할당 사서함 가져오기 내보내기 Exchange 온라인 Office 365 사서함에 PST 파일을 가져오려면 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 다음 자신을 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹](https://go.microsoft.com/fwlink/p/?LinkId=730688)에 "역할 그룹 만들기" 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p103">You have to be assigned the Mailbox Import Export role in Exchange Online to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
    
    <span data-ttu-id="72e45-127">또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-127">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
    
  - <span data-ttu-id="72e45-p104">역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p104">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="72e45-130">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-130">Or</span></span>
    
  - <span data-ttu-id="72e45-131">Office 365 조직에서 전역 관리자 여야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-131">You have to be a global administrator in your Office 365 organization.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="72e45-p105">Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p105">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
- <span data-ttu-id="72e45-p106">파일 서버 또는 조직에 있는 공유 폴더에는 하드 드라이브에 복사 하려는 PST 파일을 저장 해야 합니다. 2 단계에서에서 됩니다 도구를 실행 하면 Azure 가져오기 내보내기 (WAImportExport.exe)는이 파일 서버에 저장 된 하드 드라이브에 폴더를 공유 하거나 PST 파일에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p106">You need to store the PST files that you want to copy to a hard drive on a file server or shared folder in your organization. In Step 2, you'll run the Azure Import Export tool (WAImportExport.exe) that will copy the PST files that are stored on this file server or shared folder to the hard drive.</span></span>
    
- <span data-ttu-id="72e45-p107">2.5 인치만 반도체 드라이브 (Ssd) 또는 2.5 또는 3.5 인치 SATA II/III 내부 하드 드라이브에 Office 365 가져오기 서비스와 함께 사용할 수 있도록 지원 합니다. 하드 드라이브를 사용할 수 있는 최대 10TB 합니다. 가져오기 작업에 대 한 하드 드라이브에 첫번째 데이터 볼륨을 처리 됩니다. 데이터 볼륨 NTFS로 포맷 되어야 합니다. 하드 드라이브에 데이터를 복사, 2.5 인치 SSD를 사용 하 여 직접 연결할 수 있습니다 또는 2.5 또는 3.5 인치 SATA II/III 커넥터 또는 외부 2.5 인치 SSD를 사용 하 여 외부에서 또는 2.5 또는 3.5 인치 SATA II/III USB 어댑터를 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p107">Only 2.5 inch solid-state drives (SSDs) or 2.5 or 3.5 inch SATA II/III internal hard drives are supported for use with the Office 365 Import service. You can use hard drives up to 10 TB. For import jobs, only the first data volume on the hard drive will be processed. The data volume must be formatted with NTFS. When copying data to a hard drive, you can attach it directly using a 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III connector or you can attach it externally using an external 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III USB adaptor.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="72e45-p108">외부 하드 드라이브에 사용 된 기본 제공 된 USB 어댑터와 함께 제공 되는 Office 365 가져오기 서비스에서 지원 되지 않습니다. 또한 외부 하드 드라이브의 대/소문자 내부 디스크를 사용할 수 없습니다. 하드 드라이브에 외부 하십시오 제공 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-p108">External hard drives that come with an built-in USB adaptor aren't supported by the Office 365 Import service. Additionally, the disk inside the casing of an external hard drive can't be used. Please don't ship external hard drives.</span></span> 
  
- <span data-ttu-id="72e45-p109">PST 파일을 복사 하는 하드 드라이브 BitLocker로 암호화 해야 합니다. 2 단계에서에서 실행 되는 WAImportExport.exe 도구는 BitLocker을 설정 하는 데 도움이 됩니다. BitLocker 암호화 키를 데이터 센터 담당자 Microsoft 클라우드에서 Azure 저장소 영역에 PST 파일을 업로드 하려면 드라이브에 액세스를 사용 하 여 해당 Microsoft도 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p109">The hard drive that you copy the PST files to must be encrypted with BitLocker. The WAImportExport.exe tool that you run in Step 2 will help you set up BitLocker. It also generates a BitLocker encryption key that Microsoft data center personnel will use to access the drive to upload the PST files to the Azure storage area in the Microsoft cloud.</span></span>
    
- <span data-ttu-id="72e45-p110">드라이브 전달을을 통해 프로그램 Microsoft EA (기업 계약) 사용할 수 있습니다. 드라이브 전달 Microsoft 제품 및 서비스 계약 (MPSA)를 통해 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p110">Drive shipping is available through a Microsoft Enterprise Agreement (EA). Drive shipping isn't available through a Microsoft Products and Services Agreement (MPSA).</span></span>
    
- <span data-ttu-id="72e45-p111">드라이브 전달을 사용 하 여 Office 365 사서함을 PST 파일을 가져오려면 비용은 $2 달러 (미국) GB의 데이터입니다. 예, 1, 000 g B (1TB)의 PST 파일을 포함 하는 하드 드라이브를 제공 하는 경우는 비용은 $ 2, 000 USD입니다. 가져오기 요금을 지불 하는 파트너를 사용 하 여 작업할 수 있습니다. 파트너 찾기 (영문) 하는 방법에 대 한 정보를 [Office 365 파트너 또는 대리점 찾기](https://go.microsoft.com/fwlink/p/?LinkId=785197)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-p111">The cost to import PST files to Office 365 mailboxes using drive shipping is $2 USD per GB of data. For example, if you ship a hard drive that contains 1,000 GB (1TB) of PST files, the cost is $2,000 USD. You can work with a partner to pay the import fee. For information about finding a partner, see [Find your Office 365 partner or reseller](https://go.microsoft.com/fwlink/p/?LinkId=785197).</span></span>
    
- <span data-ttu-id="72e45-153">사용자나 조직은 FedEx 또는 DHL 계정이 있어야 합니다. </span><span class="sxs-lookup"><span data-stu-id="72e45-153">You or your organization must have an account with FedEx or DHL.</span></span>
    
  - <span data-ttu-id="72e45-154">미국, 브라질 및 유럽의 조직에서는 FedEx 계정을 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-154">Organizations in the United States, Brazil, and Europe must have FedEx accounts.</span></span>
    
  - <span data-ttu-id="72e45-155">조직에서 한국, 남동쪽 아시아, 일본, 대한민국, 및 오스트레일리아 DHL 계정을 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-155">Organizations in East Asia, Southeast Asia, Japan, Republic of Korea, and Australia must have DHL accounts.</span></span>
    
    <span data-ttu-id="72e45-156">Microsoft는 이 계정을 사용(및 충전)한 후 하드 드라이브를 사용자에게 반환합니다. </span><span class="sxs-lookup"><span data-stu-id="72e45-156">Microsoft will use (and charge) this account to return the hard drive back to you.</span></span>
    
- <span data-ttu-id="72e45-p112">Microsoft로 하드 드라이브를 발송하기 위해 국경을 통과해야 할 수 있습니다. 이러한 경우 하드 드라이브와 포함된 데이터를 관련 법률에 따라 수출 및/또는 수입해야 합니다. 하드 드라이브를 발송하기 전에 드라이브 및 데이터가 확인된 Microsoft 데이터 센터에 합법적으로 발송될 수 있는지를 관리자에게 문의하세요. 그래야 하드 드라이브가 적시에 Microsoft로 발송될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p112">The hard drive that you ship to Microsoft might have to cross international borders. If this is the case, you're responsible for ensuring that the hard drive and the data it contains are imported and/or exported in accordance with the applicable laws. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the identified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.</span></span>
    
- <span data-ttu-id="72e45-p113">이 절차 복사 하는 보안 저장소 키와 BitLocker 암호화 키를 저장 하는 작업이 포함 됩니다. 암호 또는 기타 보안 관련 정보를 보호 하는 동일 하 게 이러한 키를 보호 하기 위한 예방 조치를 수행 해야 합니다. 예 암호로 보호 된 Microsoft Word 문서에 저장 또는 암호화 된 USB 드라이브에 저장 수 있습니다. 이러한 키의 한 예에 대 한 [자세한 내용](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-p113">This procedure involves copying and saving a secure storage key and a BitLocker encryption key. Be sure to take precautions to protect these keys like you would protect passwords or other security-related information. For example, you might save them to a password-protected Microsoft Word document or save them to an encrypted USB drive. See the [More information](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) section for an example of these keys.</span></span> 
    
- <span data-ttu-id="72e45-p114">PST 파일을 Office 365 사서함으로 가져온 후 사서함에 대 한 설정 보존 대기는 무기한 기간에 대 한 켜 집니다. 즉, 사서함에 할당 된 보존 정책 보존 보류 해제 하거나 보류를 해제 하려면 날짜를 설정할 때까지 처리 되지 않습니다. 이유 해야 할까요? 오래 된 메시지를 사서함으로 가져온 경우 이러한 수 영구적으로 삭제 됩니다 (비우기)가 보존 기간이 만료 되었기 때문에 사서함에 대해 구성 된 보존 설정에 따라 합니다. 사서함을 보존 대기 배치 이러한 새로 가져온 메시지 또는 사서함에 대 한 보존 설정을 변경 하려면 시간 부여를 관리 하는 사서함 소유자 시간을 제공 합니다. 보존 대기 상태를 관리 하는 방법에 대 한 제안에 대 한 [자세한 내용](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-p114">After PST files are imported to an Office 365 mailbox, the retention hold setting for the mailbox is turned on for an indefinite duration. This means that the retention policy assigned to the mailbox won't be processed until you turn off the retention hold or set a date to turn off the hold. Why do we do this? If messages imported to a mailbox are old, they might be permanently deleted (purged) because their retention period has expired based on the retention settings configured for the mailbox. Placing the mailbox on retention hold will give the mailbox owner time to manage these newly-imported messages or give you time to change the retention settings for the mailbox. See the [More information](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) section for suggestions about managing the retention hold.</span></span> 
    
- <span data-ttu-id="72e45-p115">기본적으로 Office 365 사서함으로 받을 수 있는 최대 메시지 크기는 35 MB입니다. 사서함에 대 한 *MaxReceiveSize* 속성에 대 한 기본값을 35 MB 로설정하면 때문입니다. 그러나는 최대 메시지 크기를 Office 365에서 수신에 대 한 제한은 150MB입니다. 따라서 35 MB, 150MB를 대상 사서함에서 *MaxReceiveSize* 속성의 값을 자동으로 바뀝니다는 Office 365를 가져올 서비스 보다 큰 항목을 포함 하는 PST 파일을 가져오는 경우. 이 메시지를 통해 최대 150MB 사용자 사서함으로 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p115">By default, the maximum message size that can be received by an Office 365 mailbox is 35 MB. That's because the default value for the  *MaxReceiveSize*  property for a mailbox is set to 35 MB. However, the limit for the maximum message receive size in Office 365 is 150 MB. So if you import a PST file that contains an item larger than 35 MB, the Office 365 Import service we will automatically change the value of the  *MaxReceiveSize*  property on the target mailbox to 150 MB. This allows messages up to 150 MB to be imported to user mailboxes.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="72e45-176">메시지 수신 크기를 식별 하는 사서함에 대 한 Exchange Online PowerShell에서이 명령을 실행할 수: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-176">To identify the message receive size for a mailbox, you can run this command in Exchange Online PowerShell:  `Get-Mailbox <user mailbox> | FL MaxReceiveSize`.</span></span> 
  
- <span data-ttu-id="72e45-p116">Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니다. 비활성 사서함의 GUID를 지정 하 여이 작업을 수행 된 `Mailbox` PST 가져오기 매핑 파일에서 매개 변수입니다. 참조 [3 단계: PST 가져오기 매핑 파일을 만드는](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) 에 대 한 자세한 내용은 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p116">You can import PST files to an inactive mailbox in Office 365. You do this by specifying the GUID of the inactive mailbox in the  `Mailbox` parameter in the PST Import mapping file. See [Step 3: Create the PST Import mapping file](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) for more information.</span></span> 
    
- <span data-ttu-id="72e45-p117">Exchange 하이브리드 배포에서 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져올 수 있습니다. PST 가져오기 매핑 파일에서 다음을 수행 하 여이 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p117">In an Exchange hybrid deployment, you can import PST files to a cloud-based archive mailbox for a user whose primary mailbox is on-premises. You do this by doing the following in the PST Import mapping file:</span></span>
    
  - <span data-ttu-id="72e45-182">사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 된 `Mailbox` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-182">Specify the email address for the user's on-premises mailbox in the  `Mailbox` parameter.</span></span> 
    
  - <span data-ttu-id="72e45-183">**TRUE** 값을 지정 된 `IsArchive` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-183">Specify the **TRUE** value in the  `IsArchive` parameter.</span></span> 
    
    <span data-ttu-id="72e45-184">참조 [3 단계: PST 가져오기 매핑 파일을 만드는](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) 에 대 한 자세한 내용은 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-184">See [Step 3: Create the PST Import mapping file](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) for more information.</span></span> 

## <a name="step-1-download-the-secure-storage-key-and-pst-import-tool"></a><span data-ttu-id="72e45-185">1 단계: 보안 저장소 키 및 PST 가져오기 도구를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-185">Step 1: Download the secure storage key and PST Import tool</span></span>

<span data-ttu-id="72e45-186">첫번째 단계는 보안 저장소 키를 다운로드 하는 하 고 도구와 해당 사용자 2 단계에서에서 복사 PST 파일을 하드 드라이브에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-186">The first step is to download the secure storage key and the tool and that you will use in Step 2 to copy PST files to the hard drive.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="72e45-p118">성공적으로 드라이브 배송 메서드를 사용 하 여 PST 파일을 가져오려면 Azure 가져오기/내보내기 도구 버전 1 (WAimportExportV1)를 사용 해야 합니다. 버전 2의 Azure 가져오기/내보내기 도구 지원 되지 않습니다 및 가져오기 작업에 대해 올바르게 하드 드라이브를 준비 하기를 사용 하면 발생 합니다. 보안에서 Azure 가져오기/내보내기 도구를 다운로드 해야 &amp; 이 단계의 절차를 수행 하 여 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p118">You have to use Azure Import/Export tool version 1 (WAimportExportV1) to successfully import PST files by using the drive shipping method. Version 2 of the Azure Import/Export tool isn't supported and using it will result in incorrectly preparing the hard drive for the import job. Be sure to download the Azure Import/Export tool from the Security &amp; Compliance Center by following the procedures in this step.</span></span> 
  
1. <span data-ttu-id="72e45-190">이동 [https://protection.office.com/](https://protection.office.com/) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-190">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="72e45-191">보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **가져오기**.</span><span class="sxs-lookup"><span data-stu-id="72e45-191">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Import**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="72e45-192">듯이 보안에서 **가져오기** 페이지에 액세스 하려면 적절 한 사용 권한을 할당할 필요가 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-192">As previously stated, you have to be assigned the appropriate permissions to access the **Import** page in the Security &amp; Compliance Center.</span></span> 
  
3. <span data-ttu-id="72e45-193">**가져오기** 페이지에서 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새로 만들기 작업을 가져옵니다**.</span><span class="sxs-lookup"><span data-stu-id="72e45-193">On the **Import** page, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **New import job**.</span></span>
    
4. <span data-ttu-id="72e45-p119">가져오기 작업 마법사에서 PST 가져오기 작업에 대 한 이름을 입력 하 고 **** 을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄만 사용 합니다. 맞춤법 검사 시 대문자로 사용 하거나 이름에 공백을 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p119">In the import job wizard, type a name for the PST import job, and then click **Next**. Use lowercase letters, numbers, hyphens, and underscores. You can't use uppercase letters or include spaces in the name.</span></span>
    
5. <span data-ttu-id="72e45-197">**Choose 가져오기 작업 유형** 페이지에서 **이 실제 위치 중 하나로 배송 하드 드라이브** 를 클릭 하 고 **** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-197">On the **Choose import job type** page, click **Ship hard drives to one of our physical locations** and then click **Next**.</span></span>
    
    ![가져오기 작업을 전달 하는 드라이브를 만들기 위해이 실제 위치 중 하나로 배송 하드 드라이브를 클릭 합니다.](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. <span data-ttu-id="72e45-199">**데이터 가져오기** 페이지에서 다음 두 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-199">On the **Import data** page, do the following two things:</span></span> 
    
    ![보안 저장소 키를 복사 하 고 가져오기 데이터 페이지에서 Azure 가져오기 내보내기 도구를 다운로드](media/e22e0b48-e5ce-48e0-95bc-0490a2b3b983.png)
  
    <span data-ttu-id="72e45-p120">a. 2 단계에서 **보안 저장소 키에 복사**를 클릭 합니다. 저장소 키 표시 된 후 **클립보드에 복사** 를 클릭 하 고 붙여넣으십시오 하 고 나중에 액세스할 수 있도록 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p120">a. In step 2, click **Copy the secure storage key**. After the storage key is displayed, click **Copy to clipboard** and then paste it and save it to a file so you can access it later.</span></span>
    
    <span data-ttu-id="72e45-p121">b.에서 단계 3을 다운로드 하 고 Azure 가져오기/내보내기 (버전 1) 도구를 설치 하려면 **Azure 가져오기/내보내기 도구를 다운로드** 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p121">b. In step 3, **Download the Azure Import/Export tool** to download and install the Azure Import/Export (version 1) tool.</span></span>
    
    - <span data-ttu-id="72e45-206">팝업 창에서 **저장** 을 클릭 \> 로컬 컴퓨터의 폴더에 WaImportExportV1.zip 파일을 저장 하려면 **로 저장** 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-206">In the pop-up window, click **Save** \> **Save as** to save the WaImportExportV1.zip file to a folder on your local computer.</span></span> 
    
    - <span data-ttu-id="72e45-207">WaImportExportV1.zip 파일을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-207">Extract the WaImportExportV1.zip file.</span></span>
    
7. <span data-ttu-id="72e45-208">마법사를 닫으려면 **취소** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-208">Click **Cancel** to close the wizard.</span></span> 
    
    <span data-ttu-id="72e45-209">**가져오기** 페이지의 보안에서 돌아갈 게 &amp; 4 단계에서에서 가져오기 작업을 만들 때 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-209">You'll come back to the **Import** page in the Security &amp; Compliance Center when you create the import job in Step 4.</span></span> 

## <a name="step-2-copy-the-pst-files-to-the-hard-drive"></a><span data-ttu-id="72e45-210">2 단계: PST 파일을 하드 드라이브에 복사</span><span class="sxs-lookup"><span data-stu-id="72e45-210">Step 2: Copy the PST files to the hard drive</span></span>

<span data-ttu-id="72e45-p122">다음 단계에서는 PST 파일을 하드 드라이브에 복사 하려면 WAImportExport.exe 도구를 사용 하는 것입니다. 이 도구 BitLocker와 하드 드라이브를 암호화 하 고는 Pst 하드 드라이브에 복사 하는 복사 하는 프로세스에 대 한 정보를 저장 하는 저널 파일을 만듭니다. 이 단계를 완료 하려면 PST 파일에는 파일 공유 또는 조직에서 파일 서버에 배치 해야 합니다. 이 다음 절차에는 원본 디렉터리 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p122">The next step is to use the WAImportExport.exe tool to copy PST files to the hard drive. This tool encrypts the hard drive with BitLocker, copies the PSTs to the hard drive, and creates a journal file that stores information about the copy process. To complete this step, the PST files have to be located in a file share or file server in your organization. This is known as the source directory in the following procedure.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="72e45-p123">다른 프로그램 구문을 사용 하 여 해야 하드 드라이브에 처음으로 WAImportExport.exe 도구를 실행 한 후 그 이후에 시간입니다. 이 구문은 PST 파일을 하드 드라이브에 복사 하려면이 절차의 4 단계에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p123">After you run the WAImportExport.exe tool the first time for a hard drive, you have to use a different syntax each time after that. This syntax is explained in step 4 of this procedure to copy PST files to the hard drive.</span></span> 
  
1. <span data-ttu-id="72e45-217">로컬 컴퓨터에서 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-217">Open a Command Prompt on your local computer.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="72e45-p124">관리자 권한으로 명령 프롬프트를 실행하는 경우(열 때 "관리자 권한으로 실행" 선택) 명령 프롬프트 창에 오류 메시지가 표시됩니다. 이 메시지는 WAImportExport.exe 도구를 실행할 때 발생하는 문제를 해결하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p124">If you run the command prompt as an administrator (by selecting "Run as administrator" when you open it) error messages will be displayed in the command prompt window. This can help you troubleshoot problems running the WAImportExport.exe tool.</span></span> 
  
2. <span data-ttu-id="72e45-220">1단계에서 WAImportExport.exe 도구를 설치한 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-220">Go to the directory where you installed the WAImportExport.exe tool in Step 1.</span></span>
    
3. <span data-ttu-id="72e45-221">WAImportExport.exe를 사용하여 하드 드라이브에 PST 파일을 처음 복사할 때 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-221">Run the following command the first time that you use the WAImportExport.exe to copy PST files to a hard drive.</span></span>

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>
    ```

    <span data-ttu-id="72e45-222">다음 표에서는 매개 변수와 해당 필수 값에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-222">The following table describes the parameters and their required values.</span></span>
    
    |<span data-ttu-id="72e45-223">**매개 변수**</span><span class="sxs-lookup"><span data-stu-id="72e45-223">**Parameter**</span></span>|<span data-ttu-id="72e45-224">**설명**</span><span class="sxs-lookup"><span data-stu-id="72e45-224">**Description**</span></span>|<span data-ttu-id="72e45-225">**예제**</span><span class="sxs-lookup"><span data-stu-id="72e45-225">**Example**</span></span>|
    |:-----|:-----|:-----|
    | `/j:` <br/> |<span data-ttu-id="72e45-p125">저널 파일의 이름을 지정합니다. 이 파일은 WAImportExport.exe 도구가 있는 동일한 폴더에 저장됩니다. Microsoft로 발송하는 각 하드 드라이브에는 하나의 저널 파일이 있어야 합니다. WAImportTool.exe를 실행하여 PST 파일을 하드 드라이브에 복사할 때마다 해당 드라이브에 대한 저널 파일에 정보가 추가됩니다. 
</span><span class="sxs-lookup"><span data-stu-id="72e45-p125">Specifies the name of the journal file. This file is saved to the same folder where the WAImportExport.exe tool is located. Each hard drive you ship to Microsoft must have one journal file. Every time you run the WAImportTool.exe to copy PST files to a hard drive, information will be appended to the journal file for that drive.</span></span>  <br/> <span data-ttu-id="72e45-230">4 단계에서에서 만든 가져오기 작업 하드 드라이브에 연결 하 고 Microsoft 클라우드에서 Azure 저장소 영역에 PST 파일을 업로드 하려면 Microsoft 데이터 센터 담당자 저널 파일의 정보를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-230">Microsoft data center personnel will use the information in the journal file to associate the hard drive with the import job that you create in Step 4, and to upload the PST files to the Azure storage area in the Microsoft cloud.</span></span>  <br/> | `/j:PSTHDD1.jrn` <br/> |
    | `/t:` <br/> |<span data-ttu-id="72e45-231">로컬 컴퓨터에 연결될 때 하드 드라이브의 드라이브 문자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-231">Specifies the drive letter of the hard drive when it's connected to your local computer.</span></span>  <br/> | `/t:h` <br/> |
    | `/id:` <br/> |<span data-ttu-id="72e45-p126">복사 세션의 이름을 지정합니다. 세션은 WAImportExport.exe 도구를 실행하여 하드 드라이브에 파일을 복사할 때마다 정의됩니다. PST 파일이 이 매개 변수로 지정된 세션 이름의 폴더에 복사됩니다. </span><span class="sxs-lookup"><span data-stu-id="72e45-p126">Specifies the name of the copy session. A session is defined as each time you run the WAImportExport.exe tool to copy files to the hard drive. The PST files are copied to a folder named with the session name specified by this parameter.</span></span>  <br/> | `/id:driveship1` <br/> |
    | `/srcdir:` <br/> |<span data-ttu-id="72e45-p127">PST 파일을 복사 하는 세션 중을 포함 하는 조직에서 원본 디렉터리를 지정 합니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").</span><span class="sxs-lookup"><span data-stu-id="72e45-p127">Specifies the source directory in your organization that contains the PST files that will be copied during the session. Be sure to surround the value of this parameter with double-quotation marks (" ").</span></span>  <br/> | `/srcdir:"\\FILESERVER01\PSTs"` <br/> |
    | `/dstdir:` <br/> |<span data-ttu-id="72e45-p128">Pst 업로드 될 Microsoft 클라우드에서 Azure 저장소 영역에서 대상 디렉터리를 지정 합니다. 값을 사용 해야 `ingestiondata/`합니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").</span><span class="sxs-lookup"><span data-stu-id="72e45-p128">Specifies the destination directory in the Azure storage area in the Microsoft cloud where the PSTs will be uploaded. You must use the value  `ingestiondata/`. Be sure to surround the value of this parameter with double-quotation marks (" ").  </span></span><br/> <span data-ttu-id="72e45-p129">원하는 경우이 매개 변수의 값에도 추가 파일 경로 추가할 수 있습니다. 예 (URL 형식으로 변환 됨) 하는 하드 드라이브에에서 지정 된 원본 디렉터리의 파일 경로 사용할 수 있습니다는 `/srcdir:` 매개 변수입니다. 예, `\\FILESERVER01\PSTs` 로 변경 `FILESERVER01/PSTs`합니다. 이 경우에 포함 해야 `ingestiondata` 의 파일 경로입니다. 이 예제에서는 값에 대 한 그럴는 `/dstdir:` 매개 변수는 것 `"ingestiondata/FILESERVER01/PSTs"`합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p129">Optionally, you can also add an additional file path to the value of this parameter. For example, you can use the file path of the source directory on the hard drive (converted to a URL format) , which is specified in the  `/srcdir:` parameter. For example,  `\\FILESERVER01\PSTs` is changed to  `FILESERVER01/PSTs`. In this case, you still must include  `ingestiondata` in the file path. So in this example, the value for the  `/dstdir:` parameter would be  `"ingestiondata/FILESERVER01/PSTs"`.  </span></span><br/> <span data-ttu-id="72e45-245">추가 파일 경로 추가 하는 한 가지 이유는 파일 이름이 같은 Pst 파일을 포함 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="72e45-245">One reason to add the additional file path is if you have PSTs files with the same filename.</span></span>  <br/> <span data-ttu-id="72e45-p130">> [!NOTE]> Azure 저장소 영역으로 업로드 된 후 PST 파일에 대 한 네임 스페이스; PST 파일의 이름과 경로 이름이 포함 됩니다 선택적 pathname을 포함 하는 경우 예, `FILESERVER01/PSTs/annb.pst`합니다. 네임 스페이스는 PST 파일 이름만; 경로 이름을 포함 하지 않으면 예 `annb.pst`합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p130">> [!NOTE]> If you include the optional pathname, the namespace for a PST file after it's uploaded to the Azure storage area will include the pathname and the name of the PST file; for example,  `FILESERVER01/PSTs/annb.pst`. If you don't include a pathname, the namespace is only the PST filename; for example  `annb.pst`.</span></span>           | `/dstdir:"ingestiondata/"` <br/> <span data-ttu-id="72e45-248">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-248">Or</span></span>  <br/>  `/dstdir:"ingestiondata/FILESERVER01/PSTs"` <br/> |
    | `/sk:` <br/> |<span data-ttu-id="72e45-p131">1 단계에서에서 구한 저장소 계정 키를 지정 합니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").</span><span class="sxs-lookup"><span data-stu-id="72e45-p131">Specifies the storage account key that you obtained in Step 1. Be sure to surround the value of this parameter with double-quotation marks (" ").</span></span>  <br/> | `"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ=="` <br/> |
    | `/encrypt` <br/> |이 스위치는 하드 드라이브에 대해 BitLocker를 켭니다. 이 매개 변수는 WAImportExport.exe 도구를 처음 실행할 때 필요합니다.  <br/> <span data-ttu-id="72e45-p133">BitLocker 암호화 키 저널 파일 및 사용 하는 경우 생성 된 로그 파일에 복사 되는 `/logfile:` 매개 변수입니다. 앞에서 설명한 것 처럼 저널 파일 WAImportExport.exe 도구가 위치한 같은 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p133">The BitLocker encryption key is copied to the journal file and the log file that is created if you use the  `/logfile:` parameter. As previously explained, the journal file is saved to the same folder where the WAImportExport.exe tool is located.  </span></span><br/> | `/encrypt` <br/> |
    | `/logdir:` <br/> |<span data-ttu-id="72e45-p134">이 선택적 매개 변수는 로그 파일을 저장할 폴더를 지정 합니다. 지정 하지 않으면 로그 파일 WAImportExport.exe 도구가 위치한 동일한 폴더에 저장 됩니다. 주위에 큰따옴표 함께이 매개 변수의 값을 확인 ("").</span><span class="sxs-lookup"><span data-stu-id="72e45-p134">This optional parameter specifies a folder to save log files to. If not specified, the log files are save to the same folder where the WAImportExport.exe tool is located. Be sure to surround the value of this parameter with double-quotation marks (" ").</span></span>  <br/> | `/logdir:"c:\users\admin\desktop\PstImportLogs"` <br/> |
   
    <span data-ttu-id="72e45-258">다음은 각 매개 변수에 대한 실제 값을 사용하는 WAImportExport.exe 도구에 대한 구문 예입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-258">Here's an example of the syntax for the WAImportExport.exe tool using actual values for each parameter:</span></span>
    
    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER01\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"
    ```

    <span data-ttu-id="72e45-p135">이 명령을 실행한 후 하드 드라이브에 대한 PST 파일 복사 진행률을 보여 주는 상태 메시지가 표시됩니다. 마지막 상태 메시지에는 성공적으로 복사된 파일의 총 수가 표시됩니다. </span><span class="sxs-lookup"><span data-stu-id="72e45-p135">After you run the command, status messages are displayed that show the progress of copying the PST files to the hard drive. A final status message shows the total number of files that were successfully copied.</span></span>
    
4. <span data-ttu-id="72e45-261">WAImportExport.ext 도구를 실행하여 PST 파일을 동일한 하드 드라이브에 복사한 이후에 매번 이 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-261">Run this command each subsequent time you run the WAImportExport.ext tool to copy PST files to the same hard drive.</span></span>

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 
    ```

    <span data-ttu-id="72e45-262">다음은 PST 파일을 동일한 하드 드라이브에 복사하기 위한 후속 세션 실행 구문의 예입니다.  </span><span class="sxs-lookup"><span data-stu-id="72e45-262">Here's an example of the syntax for running subsequent sessions to copy PST files to the same hard drive.</span></span>

    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER01\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```

## <a name="step-3-create-the-pst-import-mapping-file"></a><span data-ttu-id="72e45-263">3 단계: PST 가져오기 매핑 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="72e45-263">Step 3: Create the PST Import mapping file</span></span>

<span data-ttu-id="72e45-p136">가져오기 서비스에서 PST는 사용자 사서함을 지정 하는 쉼표로 구분 된 값 (CSV) 파일을 PST 가져오기 매핑 파일에 정보를 사용할 Microsoft 데이터 센터 담당자 Azure 저장소 영역에는 하드 드라이브에서 PST 파일을 업로드 한 후 파일을 가져올 수 됩니다. PST 가져오기 작업을 만들 때에 다음 단계에는이 CSV 파일을 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p136">After Microsoft data center personnel upload the PST files from the hard drive to the Azure storage area, the Import service will use the information in the PST Import mapping file, which is a comma separated value (CSV) file, that specifies which user mailboxes the PST files will be imported to. You will submit this CSV file in the next step when you create a PST Import job.</span></span>
  
1. <span data-ttu-id="72e45-266">[PST 가져오기 매핑 파일의 복사본을 다운로드](https://go.microsoft.com/fwlink/p/?LinkId=544717)합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-266">[Download a copy of the PST Import mapping file](https://go.microsoft.com/fwlink/p/?LinkId=544717).</span></span>
    
2. <span data-ttu-id="72e45-p137">CSV 파일을 열거나 로컬 컴퓨터에 저장합니다. 다음 예에서는 완료된 PST 가져오기 매핑 파일(메모장에서 열림)을 보여 줍니다. CSV 파일을 편집할 경우 Microsoft Excel을 사용하는 것이 훨씬 더 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p137">Open or save the CSV file to your local computer. The following example shows a completed PST Import mapping file (opened in NotePad). It's much easier to use Microsoft Excel to edit the CSV file.</span></span>

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

    <span data-ttu-id="72e45-p138">첫째 행 또는 CSV 파일의 머리글 행을 사용자 사서함에 PST 파일을 가져오려면 PST 가져오기 서비스에서 사용 되는 매개 변수를 나열 합니다. 각 매개 변수 이름은 쉼표로 구분 됩니다. 각 행 머리글 행에서 특정 사서함에 PST 파일 가져오기 (영문)에 대 한 매개 변수 값을 나타냅니다. 하드 드라이브에 복사 된 각 PST 파일에 대 한 행을 할 수 있습니다. 실제 데이터와 매핑 파일의 개체 틀 데이터를 교체 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p138">The first row, or header row, of the CSV file lists the parameters that will be used by the PST Import service to import the PST files to user mailboxes. Each parameter name is separated by a comma. Each row under the header row represents the parameter values for importing a PST file to a specific mailbox. You will need a row for each PST file that was copied to the hard drive. Be sure to replace the placeholder data in the mapping file with your actual data.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72e45-275">SharePoint 매개 변수를 포함하여 머리글 행의 어떤 내용도 변경하지 않도록 합니다. 변경한 내용은 PST 가져오기 프로세스 동안 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-275">Don't change anything in the header row, including the SharePoint parameters; they will be ignored during the PST Import process.</span></span> 
  
3. <span data-ttu-id="72e45-276">다음 표의 정보를 사용하여 CSV 파일을 필요한 정보로 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-276">Use the information in the following table to populate the CSV file with the required information.</span></span>
    
    |<span data-ttu-id="72e45-277">**매개 변수**</span><span class="sxs-lookup"><span data-stu-id="72e45-277">**Parameter**</span></span>|<span data-ttu-id="72e45-278">**설명**</span><span class="sxs-lookup"><span data-stu-id="72e45-278">**Description**</span></span>|<span data-ttu-id="72e45-279">**예제**</span><span class="sxs-lookup"><span data-stu-id="72e45-279">**Example**</span></span>|
    |:-----|:-----|:-----|
    | `Workload` <br/> |<span data-ttu-id="72e45-p139">데이터를 가져올 수는 Office 365 서비스를 지정 합니다. 사용자 사서함을 PST 파일을 가져오려면, 사용 `Exchange`합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p139">Specifies the Office 365 service that data will be imported to. To import PST files to user mailboxes, use  `Exchange`.  </span></span><br/> | `Exchange` <br/> |
    | `FilePath` <br/> | <span data-ttu-id="72e45-282">PST 파일에 복사 됩니다를 하드 드라이브를 전달 하는 경우 Microsoft Azure 저장소 영역에서 폴더 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-282">Specifies the folder location in the Azure storage area that PST files will be copied to when the hard drive is shipped to Microsoft.</span></span>  <br/>  <span data-ttu-id="72e45-283">CSV 파일에이 열에 추가 기능에 지정한 것에 대 한 했는지에 따라는 `/dstdir:` 이전 단계에서 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-283">What you add in this column in the CSV file depends on what you specified in for the  `/dstdir:` parameter in the previous step.</span></span>  <br/>  <span data-ttu-id="72e45-284">사용 하는 경우 `/dstdir:"ingestiondata/"`, 다음이 매개 변수를 비워둘 CSV 파일에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-284">If you used  `/dstdir:"ingestiondata/"`, then leave this parameter blank in the CSV file.</span></span>  <br/>  <span data-ttu-id="72e45-p140">값에 대 한 경로 선택적 이름을 포함 하는 경우는 `/dstdir:` 매개 변수 (예 `/dstdir:"ingestiondata/FILESERVER01/PSTs"`, 다음 하 pathname ("ingestiondata" 제외)를 사용 하 여 CSV 파일에이 매개 변수에 대 한 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p140">If you included an optional pathname for the value of the  `/dstdir:` parameter (for example,  `/dstdir:"ingestiondata/FILESERVER01/PSTs"`, then use that pathname (not including "ingestiondata") for this parameter in the CSV file. The value for this parameter is case sensitive.  </span></span><br/>  <span data-ttu-id="72e45-p141">두 방법 모두에 대 한 값에 "ingestiondata"를 포함 *하지* 는 `FilePath` 매개 변수입니다. 이 매개 변수를 비워둘 또는 선택적 경로 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p141">Either way,  *don't*  include "ingestiondata" in the value for the  `FilePath` parameter. Leave this parameter blank or specify only the optional pathname.  </span></span><br/> <span data-ttu-id="72e45-p142">> [!IMPORTANT]> 파일 경로 이름에 대 한 경우에 지정 하는 동일한 대/소문자 여야 합니다.의 `/dstdir:` 이전 단계에서 매개 변수입니다. 예: 사용 하는 경우 `"ingestiondata/FILESERVER01/PSTs"` 이전 단계에서 하위 폴더 이름에 대 한 다음 사용 하지만 `fileserver01/psts` 에 `FilePath` CSV 파일의 매개 변수, PST 파일에 대 한 가져오기가 실패 합니다. 두 경우 모두 동일한 대/소문자를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p142">> [!IMPORTANT]>  The case for the file path name must be the same case that you specified in the  `/dstdir:` parameter in the previous step . For example, if you used  `"ingestiondata/FILESERVER01/PSTs"` for the subfolder name in the previous step, but then used  `fileserver01/psts` in the  `FilePath` parameter in CSV file, the import for the PST file will fail. Be sure to use the same case in both instances.</span></span>           |<span data-ttu-id="72e45-292">(공백으로 둠)</span><span class="sxs-lookup"><span data-stu-id="72e45-292">(leave blank)</span></span>  <br/> <span data-ttu-id="72e45-293">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-293">Or</span></span>  <br/>  `FILESERVER01/PSTs` <br/> |
    | `Name` <br/> |<span data-ttu-id="72e45-p143">사용자 사서함에 가져올 PST 파일의 이름을 지정 합니다. 이 매개 변수의 값은 대/소문자 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p143">Specifies the name of the PST file that will be imported to the user mailbox. The value for this parameter is case sensitive.  </span></span><br/> <span data-ttu-id="72e45-p144">> [!IMPORTANT]> CSV 파일에서 PST 파일 이름의 경우 2 단계에서에서 Azure 저장소 위치에 업로드 된 PST 파일로 동일 해야 합니다. 예: 사용 하는 경우 `annb.pst` 에 `Name` 하 여 CSV 파일을 하지만 실제 PST 파일의 이름에서 매개 변수는 `AnnB.pst`, 해당 PST 파일에 대 한 가져오기가 실패 합니다. CSV 파일의 PST의 이름이 동일한 대/소문자를 사용 하 여 실제 PST 파일로 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p144">> [!IMPORTANT]> The case for the PST file name in the CSV file must be the same as the PST file that was uploaded to the Azure storage location in Step 2. For example, if you use  `annb.pst` in the  `Name` parameter in the CSV file, but the name of the actual PST file is  `AnnB.pst`, the import for that PST file will fail. Be sure that the name of the PST in the CSV file uses the same case as the actual PST file.</span></span>           | `annb.pst` <br/> |
    | `Mailbox` <br/> |<span data-ttu-id="72e45-p145">PST 파일을 가져올 수는 사서함의 전자 메일 주소를 지정 합니다. 참고 PST 가져오기 서비스 공용 폴더에 PST 파일 가져오기 (영문)이 지원 되지 않으므로 공용 폴더를 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p145">Specifies the email address of the mailbox that the PST file will be imported to. Note that you can't specify a public folder because the PST Import Service doesn't support importing PST files to public folders.  </span></span><br/> <span data-ttu-id="72e45-p146">비활성 사서함을 PST 파일을 가져오려면,이 매개 변수에 대 한 사서함 GUID를 지정 해야 합니다. 이 GUID를 가져오려면 다음 PowerShell 명령을 Exchange Online에서 실행: ' Get-mailbox <identity of inactive mailbox> -InactiveMailboxOnly</span><span class="sxs-lookup"><span data-stu-id="72e45-p146">To import a PST file to an inactive mailbox, you have to specify the mailbox GUID for this parameter. To obtain this GUID, run the following PowerShell command in Exchange Online:  \`Get-Mailbox <identity of inactive mailbox> -InactiveMailboxOnly</span></span> | <span data-ttu-id="72e45-303">FL Guid` <br/> > [!NOTE]> In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-mailbox<identity of active mailbox></span><span class="sxs-lookup"><span data-stu-id="72e45-303">FL Guid` <br/> > [!NOTE]> In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox <identity of active mailbox></span></span> | <span data-ttu-id="72e45-304">FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command:  `Get-mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox</span><span class="sxs-lookup"><span data-stu-id="72e45-304">FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command:  `Get-Mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox</span></span> | <span data-ttu-id="72e45-305">FL Guid' 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-305">FL Guid\`.</span></span>           | `annb@contoso.onmicrosoft.com` <br/> <span data-ttu-id="72e45-306">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-306">Or</span></span>  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | <span data-ttu-id="72e45-p147">PST 파일을 사용자의 보관 사서함으로 가져올 것인지 여부를 지정합니다. 다음 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p147">Specifies whether or not to import the PST file to the user's archive mailbox. There are two options:  </span></span><br/> <span data-ttu-id="72e45-309">**False 이면** 사용자의 기본 사서함을 PST 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-309">**FALSE** Imports the PST file to the user's primary mailbox.</span></span>  <br/> <span data-ttu-id="72e45-p148">**True 이면** 사용자의 보관 사서함을 PST 파일을 가져옵니다. 이 가정 하는 [사용자의 보관 사서함 사용 하도록 설정](enable-archive-mailboxes.md)합니다. 이 매개 변수를 설정 하는 경우 `TRUE` 하 고 사용자의 보관 사서함 설정 되지 않은, 해당 사용자에 대 한 가져오기가 실패 합니다. 한 명의 사용자에 대 한 가져오기 실패 하는 경우 (자신의 아카이브를 사용할 수 없는 하 고이 속성은 설정 하기 때문에 `TRUE`), 가져오기 작업에서 다른 사용자가 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p148">**TRUE** Imports the PST file to the user's archive mailbox. This assumes that the [user's archive mailbox is enabled](enable-archive-mailboxes.md). If you set this parameter to  `TRUE` and the user's archive mailbox isn't enabled, the import for that user will fail. Note that if an import fails for one user (because their archive isn't enabled and this property is set to  `TRUE`), the other users in the import job won't be affected.  </span></span><br/>  <span data-ttu-id="72e45-314">이 매개 변수를 지정 하지 않으면 사용자의 기본 사서함에 PST 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-314">If you leave this parameter blank, the PST file is imported to the user's primary mailbox.</span></span>  <br/> <span data-ttu-id="72e45-315">**참고:** 기본 사서함이 있는 온-프레미스 사용자에 대해 클라우드 기반 보관 사서함에 PST 파일을 가져오려면, 방금 지정 `TRUE` 이 매개 변수에 대 한 메일에 대 한 사용자의 온-프레미스 사서함에 대 한 전자 메일 주소를 지정 하 고는 `Mailbox` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-315">**Note:** To import a PST file to a cloud-based archive mailbox for a user whose primary mailbox is on-premises, just specify  `TRUE` for this parameter and specify the email address for the user's on-premises mailbox for the  `Mailbox` parameter.</span></span>  <br/> | `FALSE` <br/> <span data-ttu-id="72e45-316">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-316">Or</span></span>  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | <span data-ttu-id="72e45-317">PST 파일을 가져온 사서함 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-317">Specifies the mailbox folder that the PST file is imported to.</span></span>  <br/>  <span data-ttu-id="72e45-318">이 매개 변수를 지정 하지 않고 공백으로 두면 PST 명명 된 **가져온** (받은 편지함 폴더와 다른 기본 사서함 폴더와 동일한 수준) 사서함의 루트 수준에 있는 새 폴더를으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-318">If you leave this parameter blank, the PST will be imported to a new folder named **Imported** located at the root level of the mailbox (the same level as the Inbox folder and the other default mailbox folders).</span></span>  <br/>  <span data-ttu-id="72e45-319">지정 하는 경우 `/`, PST 파일의 항목에에서 사용자의 받은 편지함 폴더에서 직접 가져올 수 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-319">If you specify  `/`, items in the PST file will be imported directly in to the user's Inbox folder.</span></span>  <br/>  <span data-ttu-id="72e45-p149">지정 하는 경우 `/<foldername>`, 라는 폴더를 가져올 PST 파일의 항목에에서 * \<foldername\> * 합니다. 예: 사용 하는 경우 `/ImportedPst`, **ImportedPst**라는 폴더에 항목을 가져올 수는 있습니다. 이 폴더는 받은 편지함 폴더와 같은 수준에 있는 사용자의 사서함에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p149">If you specify  `/<foldername>`, items in the PST file will be imported to a folder named  *\<foldername\>*  . For example, if you use  `/ImportedPst`, items would be imported to a folder named **ImportedPst**. This folder will be located in the user's mailbox at the same level as the Inbox folder.  </span></span><br/> |<span data-ttu-id="72e45-323">(공백으로 둠)</span><span class="sxs-lookup"><span data-stu-id="72e45-323">(leave blank)</span></span>  <br/> <span data-ttu-id="72e45-324">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-324">Or</span></span>  <br/>  `/` <br/> <span data-ttu-id="72e45-325">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-325">Or</span></span>  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |<span data-ttu-id="72e45-p150">이 선택적 매개 변수는 ANSI 파일 형식에서 PST 파일을 가져오기 위해 사용 하 여 코드 페이지에 대 한 숫자 값을 지정 합니다. 이 매개 변수는 일반적으로 이러한 언어 문자 인코딩에 대 한 더블 바이트 문자 집합 (DBCS)을 사용 하기 때문에 중국어, 일본어 및 한국어 (CJK) 조직에서 PST 파일을 가져오기 위해 사용 됩니다. 이 매개 변수는 사서함 폴더 이름에 대 한 DBCS를 사용 하는 언어에 대 한 PST 파일을 가져오려면 사용 되지 않습니다, 하는 경우 폴더 이름은 가져온 후 왜곡 자주는 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p150">This optional parameter specifies a numeric value for the code page to use for importing PST files in the ANSI file format. This parameter is used for importing PST files from Chinese, Japanese, and Korean (CJK) organizations because these languages typically use a double byte character set (DBCS) for character encoding. If this parameter isn't used to import PST files for languages that use DBCS for mailbox folder names, the folder names are often garbled after they're imported.  </span></span><br/> <span data-ttu-id="72e45-329">이 매개 변수를 사용 하 여 지원 되는 값의 목록에 대 한 [코드 페이지 식별자](https://go.microsoft.com/fwlink/p/?LinkId=328514)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-329">For a list of supported values to use for this parameter, see [Code Page Identifiers](https://go.microsoft.com/fwlink/p/?LinkId=328514).</span></span>  <br/> <span data-ttu-id="72e45-p151">> [!NOTE]> 앞부분에 명시 된,이 선택적 매개 변수 이며 CSV 파일에 포함할 필요가 없습니다. 또는 포함 하 고 하나 이상의 행에 대 한 값은 비워둡니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p151">> [!NOTE]> As previously stated, this is an optional parameter and you don't have to include it in the CSV file. Or you can include it and leave the value blank for one or more rows.</span></span>           |<span data-ttu-id="72e45-332">(공백으로 둠)</span><span class="sxs-lookup"><span data-stu-id="72e45-332">(leave blank)</span></span>  <br/> <span data-ttu-id="72e45-333">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-333">Or</span></span>  <br/>  <span data-ttu-id="72e45-334">`932`(ANSI/OEM 일본어에 대 한 코드 페이지 식별자는)</span><span class="sxs-lookup"><span data-stu-id="72e45-334">`932` (which is the code page identifier for ANSI/OEM Japanese)</span></span>  <br/> |
    | `SPFileContainer` <br/> |<span data-ttu-id="72e45-335">PST 가져오기의 경우 이 매개 변수를 비워 둡니다. </span><span class="sxs-lookup"><span data-stu-id="72e45-335">For PST Import, leave this parameter blank.</span></span>  <br/> |<span data-ttu-id="72e45-336">해당 없음</span><span class="sxs-lookup"><span data-stu-id="72e45-336">Not applicable</span></span>  <br/> |
    | `SPManifestContainer` <br/> |<span data-ttu-id="72e45-337">PST 가져오기의 경우 이 매개 변수를 비워 둡니다. </span><span class="sxs-lookup"><span data-stu-id="72e45-337">For PST Import, leave this parameter blank.</span></span>  <br/> |<span data-ttu-id="72e45-338">해당 없음</span><span class="sxs-lookup"><span data-stu-id="72e45-338">Not applicable</span></span>  <br/> |
    | `SPSiteUrl` <br/> |<span data-ttu-id="72e45-339">PST 가져오기의 경우 이 매개 변수를 비워 둡니다. </span><span class="sxs-lookup"><span data-stu-id="72e45-339">For PST Import, leave this parameter blank.</span></span>  <br/> |<span data-ttu-id="72e45-340">해당 없음</span><span class="sxs-lookup"><span data-stu-id="72e45-340">Not applicable</span></span>  <br/> |

## <a name="step-4-create-a-pst-import-job-in-office-365"></a><span data-ttu-id="72e45-341">4단계: Office 365에서 PST 가져오기 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="72e45-341">Step 4: Create a PST Import job in Office 365</span></span>

<span data-ttu-id="72e45-p152">다음 단계에서는 Office 365에서 가져오기 서비스에서 PST 가져오기 작업을 만드는 것입니다. 앞에서 설명한 것 처럼 3 단계에서에서 만든 PST 가져오기 매핑 파일을 전송 됩니다. 새 작업을 만든 후 가져오기 서비스는 PST 파일은 하드 드라이브에서 Azure 저장소 영역으로 복사 되 고 컨트롤을 만들고 가져오기 작업을 시작 후 지정 된 사용자 사서함을 PST 파일을 가져오려면 정보를 매핑 파일에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p152">The next step is to create the PST Import job in the Import service in Office 365. As previously explained, you will submit the PST Import mapping file that you created in Step 3. After you create the new job, the Import service will use the information in the mapping file to import the PST files to the specified user mailbox after the PST files are copied from the hard drive to the Azure storage area and you create and start the import job.</span></span>
  
1. <span data-ttu-id="72e45-345">이동 [https://protection.office.com](https://protection.office.com) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-345">Go to [https://protection.office.com](https://protection.office.com) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="72e45-346">보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-346">In the left pane of the Security &amp; Compliance Center, click **Data governance** and then click **Import**.</span></span>
    
3. <span data-ttu-id="72e45-347">**가져오기** 페이지에서 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새로 만들기 작업을 가져옵니다**.</span><span class="sxs-lookup"><span data-stu-id="72e45-347">On the **Import** page, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **New import job**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="72e45-348">듯이 보안에서 **가져오기** 페이지에 액세스 하려면 적절 한 사용 권한을 할당할 필요가 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-348">As previously stated, you have to be assigned the appropriate permissions to access the **Import** page in the Security &amp; Compliance Center.</span></span> 
  
4. <span data-ttu-id="72e45-p153">PST 가져오기 작업에 대 한 이름을 입력 하 고 **** 을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄만 사용 합니다. 맞춤법 검사 시 대문자로 사용 하거나 이름에 공백을 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p153">Type a name for the PST import job, and then click **Next**. Use lowercase letters, numbers, hyphens, and underscores. You can't use uppercase letters or include spaces in the name.</span></span>
    
5. <span data-ttu-id="72e45-352">**Choose 가져오기 작업 유형** 페이지에서 **이 실제 위치 중 하나로 배송 하드 드라이브** 를 클릭 하 고 **** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-352">On the **Choose import job type** page, click **Ship hard drives to one of our physical locations** and then click **Next**.</span></span>
    
    ![가져오기 작업을 전달 하는 드라이브를 만들기 위해이 실제 위치 중 하나로 배송 하드 드라이브를 클릭 합니다.](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. <span data-ttu-id="72e45-354">6 단계에서 및 **매핑 파일에 액세스할 수 있는** **I 했을 때 내 하드 드라이브에 사용 되 고 필요한 드라이브 저널 파일에 액세스할 수 있는** 확인란을 클릭 하 고 **** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-354">In step 6, click the **I've prepared my hard drives and have access to the necessary drive journal files** and **I have access to the mapping file** check boxes, and then click **Next**.</span></span>
    
    ![6 단계에서 두 확인란을 클릭 합니다.](media/fad43078-ea68-4acd-b2ed-75a800183262.png)
  
7. <span data-ttu-id="72e45-p154">**드라이브 파일 선택** 페이지에서 **드라이브 파일을 선택**을 클릭 하 고 WAImportExport.exe 도구가 위치한 동일한 폴더로 이동 합니다. 2 단계에서에서 만든 저널 파일이이 폴더에 복사 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p154">On the **Select the drive file** page, click **Select drive file**, and then go to the same folder where the WAImportExport.exe tool is located. The journal file that was created in Step 2 was copied to this folder.</span></span>
    
    ![드라이브를 선택 파일 WAImportExport.exe 도구를 실행 했을 때 만들어진 저널 파일을 제출 하려면 클릭](media/1ea35c04-bd88-4d7e-b7d9-dc390149d94f.png)
  
8. <span data-ttu-id="72e45-359">저널 파일;를 선택 합니다. 예, `PSTHDD1.jrn`합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-359">Select the journal file; for example, `PSTHDD1.jrn`.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="72e45-360">저널 파일의 이름으로 지정 된 2 단계에서에서 WAImportExport.exe 도구를 실행 했을 때의 `/j:` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-360">When you ran the WAImportExport.exe tool in Step 2, the name of the journal file was specified by the  `/j:` parameter.</span></span> 
  
9. <span data-ttu-id="72e45-361">드라이브 파일의 이름을 **드라이브에**파일 이름을 표시 한 후 드라이브 파일에서 오류를 확인 하려면 **유효성 검사** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-361">After the name of the drive file appears under **Drive file name**, click **Validate** to check your drive file for errors.</span></span> 
    
    ![선택한 드라이브 파일의 유효성을 검사 하려면 유효성 검사를 클릭 합니다.](media/4b707f5a-152a-4e74-b9f5-449c88d1fec4.png)
  
    <span data-ttu-id="72e45-p155">PST 가져오기 작업을 만들려면 성공적으로 유효성을 검사 하는 드라이브 파일. 참고 파일 이름은 유효성을 검사 성공적으로 후 녹색으로 변경 됩니다. 유효성 검사에 실패 하는 경우에 **로그 보기** 링크를 클릭 합니다. 유효성 검사 오류 보고서를 파일에 실패 한 이유 하는 방법에 대 한 정보가 포함 된 오류 메시지와 함께 열릴 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p155">The drive file has to be successfully validated to create a PST Import job. Note the file name is changed to green after it's successfully validated. If the validation fails, click the **View log** link. A validation error report is opened, with a error message with information about why the file failed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="72e45-367">추가 하 고 Microsoft에 제공 하는 각 하드 드라이브에 대 한 저널 파일의 유효성을 검사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-367">You must add and validate a journal file for each hard drive you ship to Microsoft.</span></span> 
  
10. <span data-ttu-id="72e45-368">추가 하 고 Microsoft에 제공 하는 각 하드 드라이브에 대 한 저널 파일 유효성 검사를 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-368">After adding and validating a journal file for each hard drive that you'll ship to Microsoft, click **Next**.</span></span>
    
11. <span data-ttu-id="72e45-369">클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 3 단계에서에서 만든 PST 가져오기 매핑 파일을 제출 **매핑 파일을 선택** 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-369">Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **Select mapping file** to submit the PST Import mapping file that you created in Step 3.</span></span> 
    
    ![가져오기 작업에 대해 만든 CSV 파일을 제출 선택 매핑 파일을 클릭 합니다.](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
12. <span data-ttu-id="72e45-371">CSV 이름 후 파일 아래에 표시 **파일 이름 매핑 (영문)** **유효성 검사** 오류에 대 한 CSV 파일을 확인 하려면를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-371">After the name of the CSV file appears under **Mapping file name**, click **Validate** to check your CSV file for errors.</span></span> 
    
    ![유효성 검사 오류에 대 한 CSV 파일을 확인 하려면 클릭](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    <span data-ttu-id="72e45-p156">PST 가져오기 작업을 만들려면 성공적으로 유효성을 검사 하려면 CSV 파일에 있습니다. 참고 파일 이름은 유효성을 검사 성공적으로 후 녹색으로 변경 됩니다. 유효성 검사에 실패 하는 경우에 **로그 보기** 링크를 클릭 합니다. 실패 한 파일의 각 행에 대 한 오류 메시지와 함께 유효성 검사 오류 보고서가 열릴 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p156">The CSV file has to be successfully validated to create a PST Import job. Note the file name is changed to green after it's successfully validated. If the validation fails, click the **View log** link. A validation error report is opened, with a error message for each row in the file that failed.</span></span> 
    
13. <span data-ttu-id="72e45-377">PST 매핑 파일을 성공적으로 확인 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-377">After the PST mapping file is successfully validated, click **Next**.</span></span>
    
14. <span data-ttu-id="72e45-378">**연락처 정보 제공** 페이지에서 해당 상자에 연락처 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-378">On the **Provide contact information** page, type your contact information in the applicable boxes.</span></span> 
    
    <span data-ttu-id="72e45-p157">메모를 하드 드라이브를 제공 하는 Microsoft 위치에 대 한 주소 표시 됩니다. Office 365 데이터 센터 위치에 따라 자동으로 생성 된이 주소에서 됩니다. 이 주소는 파일을 복사 하거나 스크린샷을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p157">Note that the address for the Microsoft location that you will ship your hard drives to is displayed. This address is auto-generated based on your Office 365 data center location. Copy this address to a file or take a screenshot.</span></span>
    
15. <span data-ttu-id="72e45-382">사용 약관 문서를 읽고 있는 확인란을 클릭 다음 가져오기 작업을 제출 하려면 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-382">Read the terms and conditions document, click the checkbox, and then click **Save** to submit the import job.</span></span> 
    
    <span data-ttu-id="72e45-383">가져오기 작업을 성공적으로 만들면 프로세스를 전달 하는 드라이브의 다음 단계를 설명 하는 상태 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-383">When the import job is successfully created, a status page is displayed that explains the next steps of the drive shipping process.</span></span>
    
16. <span data-ttu-id="72e45-p158">**가져오기** 페이지에서 다음을 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 를 **새로 고칠** 가져오기 작업의 목록에서 가져오기 작업을 전달 하는 새 드라이브를 표시 합니다. Note 상태가 **추적 번호에 대 한 대기**하는 상태로 설정 됩니다. 가져오기 작업에 대 한 자세한 정보를 포함 하는 상태 플라이 아웃 페이지를 표시 하려면 가져오기 작업을 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p158">On the **Import** page, click ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** to displayed the new drive shipping import job in the list of import jobs. Note that the status is set to **Waiting for tracking number**. You can also click the import job to display the status flyout page, which contains more detailed information about the import job.</span></span>
 
## <a name="step-5-ship-the-hard-drive-to-microsoft"></a><span data-ttu-id="72e45-387">5단계: Microsoft로 하드 드라이브 발송</span><span class="sxs-lookup"><span data-stu-id="72e45-387">Step 5: Ship the hard drive to Microsoft</span></span>

<span data-ttu-id="72e45-p159">다음 단계는 Microsoft로 하드 드라이브를 제공 하 고 다음 배송에 대 한 추적 번호를 제공 하 고 드라이브 전달 작업에 대 한 배송 정보를 반환 하는 것입니다. 드라이브를 Microsoft에서 받은 후 걸립니다 데이터에 대 한 7 10 비즈니스 일 사이의 조직에 대 한 Azure 저장소 영역에 PST 파일을 업로드 하려면 센터 담당자입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p159">The next step is to ship the hard drive to Microsoft, and then provide the tracking number for the shipment and return shipment information for the drive shipping job. After the drive is received by Microsoft, it will take between 7 and 10 business days for data center personnel to upload your PST files to the Azure storage area for your organization.</span></span>
  
> [!NOTE]
> <span data-ttu-id="72e45-p160">추적 번호 및 가져오기 작업 만들기 (영문)의 14 일 이내에 반환 배송 정보를 제공 하지 않으면 가져오기 작업 만료 됩니다. 가져오기 작업을 전달 하 여 새 드라이브를 만들려는 해야 이러한 상황이 발생 하는 경우 (참조 [4 단계: Office 365에서 PST 가져오기 작업 만들기](use-drive-shipping-to-import-pst-files-to-office-365.md#step4)) 및 드라이브 파일과 PST 가져오기 매핑 파일을 다시 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p160">If you don't provide the tracking number and return shipment information within 14 days of creating the import job, the import job will be expired. If this happens, you'll have to create a new drive shipping import job (see [Step 4: Create a PST Import job in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step4)) and re-submit the drive file and the PST import mapping file.</span></span> 
  
### <a name="ship-the-hard-drive"></a><span data-ttu-id="72e45-392">하드 드라이브 발송</span><span class="sxs-lookup"><span data-stu-id="72e45-392">Ship the hard drive</span></span>

<span data-ttu-id="72e45-393">Microsoft로 하드 드라이브를 발송할 때는 다음 사항에 유의하세요.</span><span class="sxs-lookup"><span data-stu-id="72e45-393">Keep the following things in mind when you ship hard drives to Microsoft:</span></span>
  
- <span data-ttu-id="72e45-394">SATA-USB 어댑터; 제공 하지 마십시오 하드 드라이브를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-394">Don't ship the SATA-to-USB adapter; you only have to ship the hard drive.</span></span>
    
- <span data-ttu-id="72e45-395">드라이브를 제대로 포장했는지 확인합니다(예: 정전기 방지 포장 백 또는 완충 비닐 사용).</span><span class="sxs-lookup"><span data-stu-id="72e45-395">Package the hard drive properly; for example, use an anti-static bag or bubble wrap.</span></span>
    
- <span data-ttu-id="72e45-396">선택한 배송업체를 사용하여 Microsoft로 하드 드라이브를 발송합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-396">Use a delivery carrier of your choice to ship the hard drive to Microsoft.</span></span>
    
- <span data-ttu-id="72e45-p161">4 단계에서에서 가져오기 작업을 만들 때 표시 된 Microsoft 위치에 대 한 주소 하드 드라이브를 제공 합니다. 배송 주소에서 "Office 365 가져오기 서비스"를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p161">Ship the hard drive to the address for the Microsoft location that was displayed when you created the import job in Step 4. Be sure to include "Office 365 Import Service" in the ship-to address.</span></span>
    
- <span data-ttu-id="72e45-p162">하드 드라이브를 발송한 후 추적 번호와 운송업체 이름을 적어 둡니다. 다음 단계에 이러한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p162">After you ship the hard drive, be sure to write down the name of the delivery carrier and the tracking number. You'll provide these in the next step.</span></span>
    
### <a name="enter-the-tracking-number-and-other-shipping-information"></a><span data-ttu-id="72e45-401">추적 번호 및 기타 발송 정보 입력</span><span class="sxs-lookup"><span data-stu-id="72e45-401">Enter the tracking number and other shipping information</span></span>

<span data-ttu-id="72e45-402">Microsoft에 하드 드라이브를 발송한 후 가져오기 서비스 페이지에서 다음 절차를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-402">After you've shipped the hard drive to Microsoft, complete the following procedure on the Import service page.</span></span>
  
1. <span data-ttu-id="72e45-403">이동 [https://protection.office.com](https://protection.office.com) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-403">Go to [https://protection.office.com](https://protection.office.com) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="72e45-404">왼쪽된 창에서 **데이터 관리** 를 클릭 한 다음 **가져오기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-404">In the left pane, click **Data governance** and then click **Import**.</span></span>
    
3. <span data-ttu-id="72e45-405">**가져오기** 페이지에 대 한 추적 번호를 입력 하려는 드라이브 배송에 대 한 작업을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-405">On the **Import** page, click the job for the drive shipment that you want to enter the tracking number for.</span></span> 
    
4. <span data-ttu-id="72e45-406">상태 플라이 아웃 페이지 **번호를 추적 하는 입력**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-406">On the status flyout page, click **Enter tracking number**.</span></span>
    
5. <span data-ttu-id="72e45-407">다음 발송 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-407">Provide the following shipping information:</span></span>
    
1. <span data-ttu-id="72e45-408">**배달 통신사업자** Microsoft에 하드 드라이브를 제공 하는데 사용 하는 배달 통신 회사의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-408">**Delivery carrier** Type the name of the delivery carrier that you used to ship the hard drive to Microsoft.</span></span> 
    
2. <span data-ttu-id="72e45-409">**추적 번호** 하드 드라이브 배송에 대 한 추적 번호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-409">**Tracking number** Type the tracking number for the hard drive shipment.</span></span> 
    
3. <span data-ttu-id="72e45-p163">**반환 통신사업자 계좌 번호** **통신사업자를 반환**하는 아래에 나열 하는 통신 회사에 대 한 조직의 계좌 번호를 입력 합니다. Microsoft는 사용 (및 청구)이이 계정에 다시 하드 드라이브를 제공 합니다. 참고 조직에서 미국 및 유럽, FedEx와 계정을 해 놓아야 합니다. 아시아 및 세계의 나머지 부분에서 조직 DHL와 계정을 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p163">**Return carrier account number** Type your organization's account number for the carrier that listed under **Return carrier**. Microsoft will use (and charge) this account to ship your hard drive back to you. Note that organizations in the USA and Europe, must have an account with FedEx. Organizations in Asia and the rest of the world, must have an account with DHL.</span></span>
    
6. <span data-ttu-id="72e45-414">**저장**을 클릭하여 가져오기 작업에 대한 이 정보를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-414">Click **Save** to save this information for the import job.</span></span> 
    
    <span data-ttu-id="72e45-p164">**가져오기** 페이지에서 다음을 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로고침** 가져오기 작업을 전달 하 여 드라이브에 대 한 정보를 업데이트 합니다. 상태에서 **전송 드라이브**로 설정 되어있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p164">On the **Import** page, click ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** to update the information for your drive shipping import job. Notice that status is now set to **Drives in transit**.</span></span>

## <a name="step-6-filter-data-and-start-the-pst-import-job"></a><span data-ttu-id="72e45-417">6 단계: 데이터를 필터링 하 고 PST 가져오기 작업 시작</span><span class="sxs-lookup"><span data-stu-id="72e45-417">Step 6: Filter data and start the PST Import job</span></span>

<span data-ttu-id="72e45-p165">하드 드라이브를 Microsoft에서 받은 후 **가져오기** 페이지에서 가져오기 작업에 대 한 상태 **받은 드라이브**를 변경 됩니다. 데이터 센터 담당자는 조직에 대 한 Azure 저장소 영역에 PST 파일을 업로드 하려면 저널 파일의 정보를 사용 합니다. 이 시점 상태 **가져오기-진행중**으로 변경 됩니다. 앞서 설명한 것 처럼 PST 파일을 업로드 하려면 하드 드라이브를 받은 후 7 ~ 10 일 사이의 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p165">After your hard drive is received by Microsoft, the status for the import job on the **Import** page will change to **Drives received**. Data center personnel will use the information in the journal file to upload your PST files to the Azure storage area for your organization. At this point, the status will change to **Import in-progress**. As previously stated, it will take between 7 to 10 business days after receiving your hard drive to upload the PST files.</span></span>
  
<span data-ttu-id="72e45-p166">PST 파일 Azure에 업로드 된 후 **진행중에서**분석의 상태가 변경 됩니다. 이 Office 365는를 분석 하 PST 파일의 데이터 (을 안전 하 게 방식으로) PST 파일에 포함 된 다양 한 메시지 형식과 항목의 보존 기간을 식별할 수를 나타냅니다. 분석이 완료 되 고 데이터를 가져올 준비가 되었습니다를 가져오기 작업에 대 한 상태는 **분석 완료**로 변경 됩니다. 이 시점 PST 파일에 포함 된 모든 데이터를 가져오려면 옵션이 제공 하거나 데이터를 가져온 가져옵니다을 제어 하는 필터를 설정 하 여 가져온 데이터를 자를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p166">After PST files are uploaded to Azure, the status is changed to **Analysis in progress**. This indicates that Office 365 is analyzing the data in the PST files (in a safe and secure manner) to identify the age of the items and the different message types included in the PST files. When the analysis is completed and the data is ready to import, the status for the import job is changed to **Analysis completed**. At this point, you have the option to import all the data contained in the PST files or you can trim the data that's imported by setting filters that control what data gets imported.</span></span>
  
1. <span data-ttu-id="72e45-426">이동 [https://protection.office.com](https://protection.office.com) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-426">Go to [https://protection.office.com](https://protection.office.com) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="72e45-427">왼쪽된 창에서 **데이터 관리**를 클릭 > **가져오기**.</span><span class="sxs-lookup"><span data-stu-id="72e45-427">In the left pane, click **Data governance** > **Import**.</span></span>
    
3. <span data-ttu-id="72e45-428">**가져오기** 페이지에서 4 단계에서에서 만든 가져오기 작업에 대 한 **Office 365로 가져올 준비** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-428">On the **Import** page, click **Ready to import to Office 365** for the import job that you created in Step 4.</span></span> 
    
    ![만든 가져오기 작업 옆에 있는 Office 365로 가져올 준비를 클릭 합니다.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    <span data-ttu-id="72e45-430">페이지 날아가기 PST 파일에 대 한 정보 및 가져오기 작업에 대 한 기타 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-430">A fly out page is displayed with information about the PST files and other information about the import job.</span></span>
    
4. <span data-ttu-id="72e45-431">**Office 365에 가져오기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-431">Click **Import to Office 365**.</span></span>
    
5. <span data-ttu-id="72e45-p167">**데이터를 필터링** 페이지가 표시 됩니다. Office 365를 데이터의 기간에 대 한 정보를 비롯 하 여 PST 파일에 수행 하 여 분석에서 발생 하는 데이터 인 사이트를 포함 합니다. 이 시점 그대로 모든 데이터를 가져오거나 가져올 하는 데이터를 필터링 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p167">The **Filter your data** page is displayed. It contains the data insights resulting from the analysis performed on the PST files by Office 365, including information about the age of the data. At this point, you have the option to filter the data that will be imported or import all the data as is.</span></span> 
    
    ![PST 파일의 데이터를 높이고 또는 모두를 가져올 수 있습니다.](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
6. <span data-ttu-id="72e45-436">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-436">Do one of the following:</span></span>
    
    <span data-ttu-id="72e45-p168">a. 가져올 데이터를 높이고, 하려면 **예를 가져오기 전에으로 필터링 합니다.** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p168">a. To trim the data that you import, click **Yes, I want to filter it before importing**.</span></span>
    
    <span data-ttu-id="72e45-439">PST 파일의 데이터를 필터링 하 고 다음 가져오기 작업을 시작 하는 방법에 대 한 자세한 단계별 지침은 [Office 365에 PST 파일을 가져올 때 데이터를 필터링](filter-data-when-importing-pst-files.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-439">For detailed step-by-step instructions about filtering the data in the PST files and then starting the import job, see [Filter data when importing PST files to Office 365](filter-data-when-importing-pst-files.md).</span></span>
    
    <span data-ttu-id="72e45-440">또는</span><span class="sxs-lookup"><span data-stu-id="72e45-440">Or</span></span>
    
    <span data-ttu-id="72e45-p169">b. PST 파일에서 모든 데이터를 가져오려면를 **아니오, 모든 작업을 가져오려면** 클릭 하 고 **** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p169">b. To import all data in the PST files, click **No, I want to import everything,** and click **Next**.</span></span>
    
7. <span data-ttu-id="72e45-443">모든 데이터를 가져오려면 선택한 경우에 가져오기 작업을 시작 하려면 **데이터 가져오기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-443">If you chose to import all the data, click **Import data** to start the import job.</span></span> 
    
    <span data-ttu-id="72e45-p170">가져오기 작업의 상태 **가져오기** 페이지에 표시 됩니다. 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로고침** **상태** 열에 표시 되는 상태 정보를 업데이트 합니다. 가져올 각 PST 파일에 대 한 상태 정보를 표시 하는 상태 플라이 아웃 페이지를 표시 하려면 가져오기 작업을 클릭 합니다. 가져오기가 완료 되 고 사용자 사서함에 PST 파일을 가져온를 상태가 **완료**로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p170">The status of the import job is displayed on the **Import** page. Click ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) **Refresh** to update the status information that's displayed in the **Status** column. Click the import job to display the status flyout page, which displays status information about each PST file being imported. When the import is complete and PST files have been imported to user mailboxes, the status will be changed to **Completed**.</span></span>

## <a name="view-a-list-of-the-pst-files-uploaded-to-office-365"></a><span data-ttu-id="72e45-448">Office 365에 업로드 된 PST 파일의 목록 보기</span><span class="sxs-lookup"><span data-stu-id="72e45-448">View a list of the PST files uploaded to Office 365</span></span>

<span data-ttu-id="72e45-p171">설치 하 고 (즉, 무료, 공개 소스 도구) Microsoft Azure 저장소 탐색기를 사용 하 여 되는 업로드 (Microsoft 데이터 센터 담당자) 하 여 조직에 대 한 Azure 저장소 영역으로 PST 파일의 목록을 볼 수 있습니다. Microsoft로 전송 하는 하드 드라이브에서 PST 파일은 Azure 저장소 영역에 성공적으로 업로드 된 확인 하려면이 옵션을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p171">You can install and use the Microsoft Azure Storage Explorer (which is a free, open source tool) to view the list of the PST files that we're uploaded (by Microsoft data center personnel) to the Azure storage area for your organization. You can do this to verify that PST files from the hard drives that you sent to Microsoft were successfully uploaded to the Azure storage area.</span></span>
  
<span data-ttu-id="72e45-451">Microsoft Azure 저장소 탐색기 미리 보기에서 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-451">The Microsoft Azure Storage Explorer is in Preview.</span></span>
  
 <span data-ttu-id="72e45-p172">**중요:** Azure 저장소 탐색기를 사용 하 여 업로드 하거나 PST 파일을 수정 하려면 수는 없습니다. Office 365에 PST 파일을 가져오기 위한 유일한 방법은 지원된 AzCopy를 사용 하는 것입니다. 또한 Azure blob를 업로드 한 PST 파일을 삭제할 수 없습니다. PST 파일을 삭제 하려고 하는 경우 필요한 사용 권한을 있지 않은 경우에 대 한 오류가 표시 됩니다. 참고 모든 PST 파일 Azure 저장소 영역에서 자동으로 삭제 됩니다. 진행 중인 가져오기 작업이 다음 모든 PST 파일의 경우는 * * ingestiondata * * 컨테이너 30 일 가장 최근의 가져오기 작업을 만든 후에 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p172">**Important:** You can't use the Azure Storage Explorer to upload or modify PST files. The only supported method for importing PST files to Office 365 is to use AzCopy. Also, you can't delete PST files that you've uploaded to the Azure blob. If you try to delete a PST file, you'll receive an error about not having the required permissions. Note that all PST files are automatically deleted from your Azure storage area. If there are no import jobs in progress, then all PST files in the ** ingestiondata ** container are deleted 30 days after the most recent import job was created.</span></span> 
  
<span data-ttu-id="72e45-458">Azure 저장소 탐색기를 설치 및 Azure 저장소 영역에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-458">To install the Azure Storage Explorer and connect to your Azure storage area:</span></span>
  
1. <span data-ttu-id="72e45-p173">조직에 대 한 공유 액세스 서명 (SAS) URL을 얻으려면 다음 단계를 수행 합니다. 이 URL은 조직 및 SAS 키에 대 한 Microsoft 클라우드 Azure 저장소 위치에 대 한 네트워크 URL의 조합입니다. 이 키를 조직의 Azure 저장소 위치에 액세스 하려면 필요한 권한을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p173">Perform the following steps to get the Shared Access Signature (SAS) URL for your organization. This URL is a combination of the network URL for the Azure storage location in the Microsoft cloud for your organization and an SAS key. This key provides you with the necessary permissions to access your organization's Azure storage location.</span></span>
    
1. <span data-ttu-id="72e45-462">이동 [https://protection.office.com/](https://protection.office.com/) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-462">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="72e45-463">보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **가져오기**.</span><span class="sxs-lookup"><span data-stu-id="72e45-463">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Import**.</span></span>
    
3. <span data-ttu-id="72e45-464">**가져오기** 페이지에서 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **새로 만들기 작업을 가져옵니다**.</span><span class="sxs-lookup"><span data-stu-id="72e45-464">On the **Import** page, click ![Add Icon](media/ITPro-EAC-AddIcon.gif) **New import job**.</span></span>
    
4. <span data-ttu-id="72e45-p174">가져오기 작업 마법사에서 PST 가져오기 작업에 대 한 이름을 입력 하 고 **** 을 클릭 합니다. 소문자, 숫자, 하이픈 및 밑줄만 사용 합니다. 맞춤법 검사 시 대문자로 사용 하거나 이름에 공백을 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p174">In the import job wizard, type a name for the PST import job, and then click **Next**. Use lowercase letters, numbers, hyphens, and underscores. You can't use uppercase letters or include spaces in the name.</span></span>
    
5. <span data-ttu-id="72e45-468">**Choose 가져오기 작업 유형** 페이지에서 **데이터를 업로드** 를 클릭 하 고 **** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-468">On the **Choose import job type** page, click **Upload your data** and then click **Next**.</span></span>
    
6. <span data-ttu-id="72e45-469">2 단계에서 **네트워크 업로드 SAS URL 표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-469">In step 2, click **Show network upload SAS URL**.</span></span>
    
7. <span data-ttu-id="72e45-p175">URL이 표시 되 면 복사 하 고 파일에 저장 합니다. 전체 URL을 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p175">After the URL is displayed, copy it and save it to a file. Be sure to copy the entire URL.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="72e45-p176">SAS URL을 보호 하기 위한 예방 조치를 수행 해야 합니다. 이 하는데 사용할 수 누구나 조직에 대 한 Azure 저장소 영역에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p176">Be sure to take precautions to protect the SAS URL. This can be used by anyone to access the Azure storage area for your organization.</span></span> 
  
8. <span data-ttu-id="72e45-474">가져오기 작업 마법사를 닫으려면 **취소** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-474">Click **Cancel** to close the import job wizard.</span></span> 
    
2. <span data-ttu-id="72e45-475">다운로드 하 고 [Microsoft Azure 저장소 탐색기 도구](https://go.microsoft.com/fwlink/p/?LinkId=544842)를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-475">Download and install the [Microsoft Azure Storage Explorer tool](https://go.microsoft.com/fwlink/p/?LinkId=544842).</span></span>
    
3. <span data-ttu-id="72e45-476">Microsoft Azure 저장소 탐색기를 시작 하 고 왼쪽된 창에서 **계정 저장소를** 마우스 오른쪽 단추로 클릭 **Azure 저장소에 대 한 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-476">Start the Microsoft Azure Storage Explorer, right-click **Storage Accounts** in the left pane, and then click **Connect to Azure storage**.</span></span>
    
    ![저장소 계정을 마우스 오른쪽 단추로 클릭 하 고 Azure 저장소에 연결을 클릭 한 다음](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
4. <span data-ttu-id="72e45-478">**공유 액세스 서명 (SAS) URI 또는 연결 문자열 사용** 을 클릭 하 고 **** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-478">Click **Use a shared access signature (SAS) URI or connection string** and click **Next**.</span></span>
    
5. <span data-ttu-id="72e45-479">**SAS URI를 사용**을 클릭 하 고 **URI**아래에 있는 상자에서를 1 단계에서 구한 SAS URL을 붙여넣습니다 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-479">Click **Use a SAS URI**, paste the SAS URL that you obtained in step 1 in to in the box under **URI**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="72e45-480">**연결 요약** 페이지에서 연결 정보를 검토 하 고 **연결**을 클릭 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-480">On the **Connection summary** page, you can review the connection information, and then click **Connect**.</span></span>
    
    <span data-ttu-id="72e45-p177">**Ingestiondata** 컨테이너를 열 수 있습니다. 하드 드라이브에서 PST 파일을 포함 합니다. **Ingestiondata** 컨테이너는 **저장소 계정** 아래에 \> **(SAS-Attached 서비스)** \> **Blob 컨테이너**입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p177">The **ingestiondata** container is opened; it contains the PST files from your hard drive. The **ingestiondata** container is located under **Storage Accounts** \> **(SAS-Attached Services)** \> **Blob Containers**.</span></span>
    
    ![Azure 저장소 탐색기는 사용자가 업로드한 PST 파일 목록이 표시됩니다.](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
7. <span data-ttu-id="72e45-p178">Microsoft Azure 저장소 탐색기를 사용 하 여이 끝나면 **ingestiondata**마우스 오른쪽 단추로 클릭 하 고 Azure 저장소 영역에서 연결을 끊으려면 **분리** 클릭 합니다. 그렇지 않은 경우 받게 오류가 다음에 연결 하려고 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p178">When you're finished using the Microsoft Azure Storage Explorer, right-click **ingestiondata**, and then click **Detach** to disconnect from your Azure storage area. Otherwise, you'll receive an error the next time you try to attach.</span></span> 
    
    ![수집을 마우스 오른쪽 단추로 클릭하고 분리를 클릭하여 Azure 저장소 영역에서 연결 끊기](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  

  
## <a name="troubleshooting-tips"></a><span data-ttu-id="72e45-487">문제 해결 팁</span><span class="sxs-lookup"><span data-stu-id="72e45-487">Troubleshooting tips</span></span>
<span data-ttu-id="72e45-488"><a name="troubleshootingtips"> </a></span><span class="sxs-lookup"><span data-stu-id="72e45-488"></span></span>

- <span data-ttu-id="72e45-p179">**PST 가져오기 CSV 매핑 파일에서 오류 때문에 가져오기 작업이 실패 하면 어떻게 됩니까?** 매핑 파일의 오류로 인해 실패 하면 가져오기 작업을 다시 새 가져오기 작업을 만들기 위해 Microsoft에 하드 드라이브를 제공할 필요가 없습니다. 조직에 대 한 Azure 저장소 영역에 이미 업로드 한 드라이브 전달 가져오기 작업에 대 한 하면가 제출 하는 하드 드라이브에서 PST 파일 때문입니다. 이 경우 방금 해야 PST 가져오기 CSV 매핑 파일에서 오류를 수정 하 고 다음 새 "네트워크 업로드" 가져오기 작업을 만들고 수정 된 CSV 매핑 파일을 전송 합니다. 참조를 만들고 새 네트워크 업로드 가져오기 작업을 시작 하려면 [5 단계: Office 365에서 PST 가져오기 작업 만들기](use-network-upload-to-import-pst-files.md#step-5-create-a-pst-import-job-in-office-365) 및 [6 단계: 데이터를 필터링 하 고 PST 가져오기 작업을 시작](use-network-upload-to-import-pst-files.md#step-6-filter-data-and-start-the-pst-import-job) 항목 "사용 하 여 네트워크 업로드 Office 365로 PST 파일을 가져올 수 있습니다."</span><span class="sxs-lookup"><span data-stu-id="72e45-p179">**What happens if the import job fails because of errors in the PST Import CSV mapping file?** If an import job fails because of errors in the mapping file, you don't have to re-ship the hard drive to Microsoft in order to create a new import job. That's because the PST files from the hard drive that you submitted for the drive shipping import job have already been uploaded to the Azure storage area for your organization. In this case, you just have to fix the errors in the PST Import CSV mapping file, and then create a new "network upload" import job and submit the revised CSV mapping file. To create and start a new network upload import job, see [Step 5: Create a PST Import job in Office 365](use-network-upload-to-import-pst-files.md#step-5-create-a-pst-import-job-in-office-365) and [Step 6: Filter data and start the PST Import job](use-network-upload-to-import-pst-files.md#step-6-filter-data-and-start-the-pst-import-job) in the topic "Use network upload to import PST files to Office 365."</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="72e45-p180">해결 하기 위해 PST 가져오기 CSV 매핑 파일을 [Azure 저장소 탐색기](#view-a-list-of-the-pst-files-uploaded-to-office-365) 도구를 사용 하 여 Azure 저장소 영역에 업로드 된 하드 드라이브에서 PST 파일에 대 한 **ingestiondata** 컨테이너에 폴더 구조를 볼 수 있습니다. FilePath 매개 변수에서 잘못 된 값 매핑 파일 오류는 일반적으로 발생 하 고 있습니다. 이 매개 변수는 Azure 저장소 영역에서 PST 파일의 위치를 지정합니다. FilePath 매개 변수에서 [3 단계에서](#step-3-create-the-pst-import-mapping-file)에서 테이블에 대 한 설명을 참조 하십시오. 앞에서 설명한 것 처럼 Azure 저장소 영역에서 PST 파일의 위치를 하 여 지정 된는 `/dstdir:` [2 단계에서](#step-2-copy-the-pst-files-to-the-hard-drive)에서 WAImportExport.exe 도구를 실행 했을 때 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p180">To help you troubleshoot the PST Import CSV mapping file, use the [Azure Storage Explorer](#view-a-list-of-the-pst-files-uploaded-to-office-365) tool to view the folder structure in the **ingestiondata** container for the PST files from your hard drive that were uploaded to the Azure storage area. Mapping file errors are typically caused by an incorrect value in the FilePath parameter. This parameter specifies the location of a PST file in the Azure storage area. See the description of the FilePath parameter in table in [Step 3](#step-3-create-the-pst-import-mapping-file). As previously explained, the location of PST files in the Azure storage area was specified by the  `/dstdir:` parameter when you ran the WAImportExport.exe tool in [Step 2](#step-2-copy-the-pst-files-to-the-hard-drive).</span></span> 
  

  
## <a name="more-information"></a><span data-ttu-id="72e45-499">추가 정보</span><span class="sxs-lookup"><span data-stu-id="72e45-499">More information</span></span>

- <span data-ttu-id="72e45-p181">드라이브 전달은 조직에 사용할 수 있는 규정 준수 기능을 활용 하는 Office 365에 많은 양의 보관 메시징 데이터를 가져올 수 있는 효과적인 방법입니다. 사용자 사서함에 보관 데이터를 가져온 후에 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p181">Drive shipping is an effective way to import large amounts of archival messaging data to Office 365 to take advantage of the compliance features that are available to your organization. After archival data is imported to user mailboxes, you can:</span></span>
    
  - <span data-ttu-id="72e45-502">[보관 사서함](enable-archive-mailboxes.md) 및 사용자에 게 추가 사서함 저장 공간 데이터에 대 한 [보관 자동 확장](enable-unlimited-archiving.md) 을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-502">Enable [archive mailboxes](enable-archive-mailboxes.md) and [auto-expanding archiving](enable-unlimited-archiving.md) to give users additional mailbox storage space for the data.</span></span> 
    
  - <span data-ttu-id="72e45-503">사서함 데이터를 유지할 [소송 보존](https://go.microsoft.com/fwlink/?linkid=856286) 에 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-503">Place mailboxes on [Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286) to retain the data.</span></span> 
    
  - <span data-ttu-id="72e45-504">Microsoft [eDiscovery 도구](search-for-content.md) 를 사용 하 여 데이터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-504">Use Microsoft [eDiscovery tools](search-for-content.md) to search the data.</span></span> 
    
  - <span data-ttu-id="72e45-505">데이터는 유지 하는 기간 및 보존 기간이 만료 후 수행할 동작을 제어 하려면 [Office 365 보존 정책](retention-policies.md) 을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-505">Apply [Office 365 retention policies](retention-policies.md) to control how long the data is retained, and what action to take after the retention period expires.</span></span> 
    
  - <span data-ttu-id="72e45-506">[Office 365 감사 로그](search-the-audit-log-in-security-and-compliance.md) 를 검색이이 데이터에 관련 된 이벤트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-506">Search the [Office 365 audit log](search-the-audit-log-in-security-and-compliance.md) for events related to this data.</span></span> 
    
  - <span data-ttu-id="72e45-507">규정 준수를 위해 데이터를 보관 하려면 [비활성 사서함](create-and-manage-inactive-mailboxes.md) 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-507">Import data to [inactive mailboxes](create-and-manage-inactive-mailboxes.md) to archive data for compliance purposes.</span></span> 
    
  - <span data-ttu-id="72e45-508">중요 한 정보의 [데이터](data-loss-prevention-policies.md) 손실을 조직을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-508">Protect your organization against [data loss](data-loss-prevention-policies.md) of sensitive information.</span></span> 
    
- <span data-ttu-id="72e45-p182">다음은 보안 저장소 계정 키와 BitLocker 암호화 키의 예입니다. 이 예에는 PST 파일을 하드 드라이브에 복사하기 위해 실행하는 WAImportExport.exe 명령 구문도 포함되어 있습니다. 암호나 기타 보안 관련 정보를 보호하는 것처럼 특히 주의해서 이러한 항목을 보호해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p182">Here's an example of the secure storage account key and a BitLocker encryption key. This example also contains the syntax for the WAImportExport.exe command that you run to copy PST files to a hard drive. Be sure to take precautions to protect these just like you would protect passwords or other security-related information.</span></span>
    

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
   
- <span data-ttu-id="72e45-p183">앞에서 설명한 것 처럼 Office 365 가져오기 서비스 설정 (한 무기한 기간) 사서함에 PST 파일을 가져온 후 보존 대기 상태를 설정 합니다. 즉, *RentionHoldEnabled* 속성이로 설정 된 `True` 사서함에 할당 된 보존 정책 않습니다 처리할 수 있도록 합니다. 삭제 또는 보관 정책을 삭제 하거나 오래 된 메시지를 보관할 수 없도록 하 여 새로 가져온 메시지를 관리 하는 사서함 소유자 시간을 제공 합니다. 이 보존 대기 상태를 관리 하기 위해 수행할 수 있는 일부 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="72e45-p183">As previously explained, the Office 365 Import service turns on the retention hold setting (for an indefinite duration) after PST files are imported to a mailbox. This means the  *RentionHoldEnabled*  property is set to  `True` so that the retention policy assigned to the mailbox won't be processed. This gives the mailbox owner time to manage the newly-imported messages by preventing a deletion or archive policy from deleting or archiving older messages. Here are some steps you can take to manage this retention hold:</span></span> 
    
  - <span data-ttu-id="72e45-p184">특정 기간 동안 시간을 한 후 해제할 수 보존 대기를 실행 하 여는 `Set-Mailbox -RetentionHoldEnabled $false` 명령 합니다. 자세한 내용은 [사서함 보존에 원본 위치 유지](https://go.microsoft.com/fwlink/p/?LinkId=544749)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-p184">After a certain period of time, you can turn off the retention hold by running the  `Set-Mailbox -RetentionHoldEnabled $false` command. For instructions, see [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/p/?LinkId=544749).</span></span>
    
  - <span data-ttu-id="72e45-p185">나중에 일부 날짜 꺼져 있도록 보존 대기를 구성할 수 있습니다. 실행 하 여이 작업을 수행 된 `Set-Mailbox -EndDateForRetentionHold <date>` 명령 합니다. 예, 오늘 날짜가 2016 년 7 월 1 일이 고 30 일에서 해제 된 보존 대기 원하는 이라고 가정할 다음 명령을 실행 합니다: `Set-Mailbox -EndDateForRetentionHold 8/1/2016`합니다. 이 시나리오에서는 *RentionHoldEnabled* 속성이 *True* 로 설정 남게 됩니다. 자세한 내용은 [Set-mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-p185">You can configure the retention hold so that it's turned off on some date in the future. You do this by running the  `Set-Mailbox -EndDateForRetentionHold <date>` command. For example, assuming that today's date is July 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. In this scenario, you would leave the  *RentionHoldEnabled*  property set to  *True*  . For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).</span></span>
    
  - <span data-ttu-id="72e45-p186">오래 된 항목을 가져오지 않습니다 수 즉시 삭제 되거나 사용자의 보관 사서함으로 이동 되도록 사서함에 할당 된 보존 정책에 대 한 설정을 변경할 수 있습니다. 예, 사서함에 할당 된 삭제 또는 보관 정책에 대 한 보존 기간을 길게 수 있습니다. 이 시나리오에서는 있습니다 기능을 해제는 사서함에 보존 대기 상태에는 보존 정책의 설정을 변경한 후 합니다. 자세한 내용은 [Office 365 조직 내의 사서함에에서는 보관 및 삭제 정책 설정](set-up-an-archive-and-deletion-policy-for-mailboxes.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e45-p186">You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).</span></span>
    

  

