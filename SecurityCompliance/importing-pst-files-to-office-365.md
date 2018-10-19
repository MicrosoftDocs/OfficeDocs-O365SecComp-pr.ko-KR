---
title: Office 365로 조직 PST 파일 가져오기 (영문)의 개요 (영문)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.IngestionHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: '관리자를 위한: Office 365 보안에서 가져오기 서비스를 사용 하는 방법에 대 한 설명 &amp; 전자 메일 데이터 (PST 파일)을 Exchange Online의 사용자 사서함으로 대량 가져오기에 대 한 준수 센터입니다. 이 항목 Faq를 제공 하 고 PST 가져오기 프로세스의 작동 방식에 대해 설명 합니다.'
ms.openlocfilehash: 3a6c3db966513be5c63588dac75643ffc1962323
ms.sourcegitcommit: 8294182d4dd124f035a221de0b90159ef7eec4ae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/19/2018
ms.locfileid: "25639677"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a><span data-ttu-id="927f9-104">Office 365로 조직 PST 파일 가져오기 (영문)의 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="927f9-104">Overview of importing your organization PST files to Office 365</span></span>

> [!NOTE]
> <span data-ttu-id="927f9-p102">이 문서는 관리자입니다. 자신의 사서함에 PST 파일을 가져올 하려고 합니까? [가져오기 전자 메일, 연락처 및 일정 Outlook.pst 파일에서](https://go.microsoft.com/fwlink/p/?LinkID=785075) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="927f9-p102">This article is for administrators. Are you trying to import PST files to your own mailbox? See [Import email, contacts, and calendar from an Outlook .pst file](https://go.microsoft.com/fwlink/p/?LinkID=785075)</span></span>

<span data-ttu-id="927f9-p103">Office 365 보안에서 가져오기 서비스를 사용 하려면 &amp; 준수 센터를 신속 하 게 대량 가져오기 PST 파일을 Office 365 조직에서 Exchange Online 사서함에 있습니다. 두 가지 방법으로 Office 365에 PST 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p103">You can use the Import service in the Office 365 Security &amp; Compliance Center to quickly bulk-import PST files to Exchange Online mailboxes in your Office 365 organization. There are two ways you can import PST files to Office 365:</span></span>
   
- <span data-ttu-id="927f9-p104">**네트워크 업로드** ![클라우드 업로드](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) -Microsoft 클라우드에서 임시 Azure 저장소 위치를 네트워크를 통해 PST 파일을 업로드 합니다. 그런 다음 Office 365 조직에서 사서함에 PST 데이터를 가져오려면 Office 365를 가져올 서비스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p104">**Network upload** ![Cloud upload](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) - Upload the PST files over the network to a temporary Azure storage location in the Microsoft cloud. Then you use the Office 365 Import service to import the PST data to mailboxes in your Office 365 organization.</span></span> 

- <span data-ttu-id="927f9-p105">**배송 드라이브** ![하드 디스크](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) -BitLocker 암호화 된 하드 드라이브에 PST 파일을 복사 하 고 Microsoft에 드라이브를 물리적으로 제공 합니다. Microsoft 하드 드라이브를 받으면 데이터 센터 담당자 Microsoft 클라우드에서 임시 Azure 저장소 위치에 데이터를 업로드 합니다. 그런 다음 Office 365 조직에서 사서함에 데이터를 가져오려면 Office 365를 가져올 서비스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p105">**Drive shipping** ![Hard disk](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) - Copy the PST files to a BitLocker-encrypted hard drive and then physically ship the drive to Microsoft. When Microsoft receives the hard drive, data center personnel upload the data to a temporary Azure storage location in the Microsoft cloud. Then you use the Office 365 Import service to import the data to mailboxes in your Office 365 organization.</span></span>

## <a name="step-by-step-instructions"></a><span data-ttu-id="927f9-115">단계별 지침</span><span class="sxs-lookup"><span data-stu-id="927f9-115">Step-by-step instructions</span></span>
  
<span data-ttu-id="927f9-116">대량 가져오기 Office 365에 조직의 PST 파일에 대 한 자세한, 대 한 단계별 지침은 다음 항목 중 하나를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="927f9-116">See one of the following topics for detailed, step-by-step instructions for bulk-importing your organization's PST files to Office 365.</span></span> 
   
- [<span data-ttu-id="927f9-117">네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="927f9-117">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
- [<span data-ttu-id="927f9-118">드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="927f9-118">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a><span data-ttu-id="927f9-119">PST 파일 가져오기 (영문)의 작동 방식</span><span class="sxs-lookup"><span data-stu-id="927f9-119">How importing PST files works</span></span>

<span data-ttu-id="927f9-p106">그림 및 전체 PST 가져오기 프로세스에 이르는 다음과 같습니다. 그림 기본 워크플로 표시 하 고 네트워크 업로드 및 드라이브 운송 방법 간의 차이점을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p106">Here's an illustration and description of the complete PST import process. The illustration shows the primary workflow and highlights the differences between the network upload and drive shipping methods.</span></span>
  
![PST 가져오기 프로세스의 워크플로](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. <span data-ttu-id="927f9-p107">**다운로드 PST 가져오기 도구와 개인 키 Azure 저장소 위치** -하는 첫번째 단계는를 사용 하 고 PST 파일을 업로드 하거나 하드 드라이브에 복사 하는 도구 및 액세스 키를 다운로드 합니다. Office 365 보안에서 **가져오기** 페이지에서 이러한 가져올 &amp; 준수 센터입니다. 키 개인 및 보안 Azure 저장소 위치에 PST 파일을 업로드 하려면 필요한 권한을 가진 사용자 (또는 드라이브 전달의 경우 Microsoft 데이터 센터 담당자)를 제공 합니다. 이 액세스 키 조직에 고유 하 고 Microsoft 클라우드로 업로드 하려는 하 고 나면 PST 파일에 무단으로 액세스를 방지할 수 있습니다. 참고 Office 365에 PST 파일 가져오기 (영문)을 별도 Azure 구독을 조직 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p107">**Download the PST import tools and key to private Azure storage location** - The first step is to download the tool and access key used to upload the PST files or copy them to a hard drive. You obtain these from the **Import** page in the Office 365 Security &amp; Compliance Center. The key provides you (or Microsoft data center personnel in the case of drive shipping) with the necessary permissions to upload PST files to a private and secure Azure storage location. This access key is unique to your organization and helps prevent unauthorized access to your PST files after they're uploaded to the Microsoft cloud. Note that importing PST files to Office 365 doesn't require your organization to have a separate Azure subscription.</span></span> 
    
2. <span data-ttu-id="927f9-p108">**업로드 또는 복사 PST 파일** -다음 단계에서는 PST 파일을 가져오려면 드라이브 전달 또는 네트워크 업로드를 사용 하는 여부에 따라 달라 집니다. 도구 및 이전 단계에서 얻은 보안 저장소 키를 사용 하 여 두 경우 모두 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p108">**Upload or copy the PST files** - The next step depends on whether you're using network upload or drive shipping to import PST files. In both cases, you'll use the tool and secure storage key that you obtained in the previous step.</span></span>
    
    - <span data-ttu-id="927f9-p109">**네트워크 업로드** (1 단계에서 다운로드 한) AzCopy.exe 도구 업로드 하 고 Microsoft 클라우드에서는 Azure 저장소 위치에 PST 파일을 저장 하는데 사용 됩니다. Azure 저장소 위치를 PST 파일을 업로드 하는 동일한 지역 Microsoft 데이터 센터에서 Office 365 조직 위치한 상주 하는 메모 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p109">**Network upload**The AzCopy.exe tool (downloaded in step 1) is used to upload and store your PST files in an Azure storage location in the Microsoft cloud. Note that the Azure storage location that you upload your PST files to resides in the same regional Microsoft datacenter where your Office 365 organization is located.</span></span> 
    
      <span data-ttu-id="927f9-132">Office 365로 가져올 PST 파일을 업로드 하려면 파일 공유 또는 조직에서 파일 서버에 배치할 수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-132">To upload them, the PST files that you want to import to Office 365 have to be located in a file share or file server in your organization.</span></span>
    
    - <span data-ttu-id="927f9-p110">**배송 드라이브** (1 단계에서 다운로드 한) WAImportExport.exe 도구는 하드 드라이브에 PST 파일을 복사 하는데 사용 됩니다. 이 도구는 BitLocker 사용 하 여 하드 드라이브를 암호화 하 고 Pst는 하드 드라이브에 복사 하는 것입니다. 네트워크 업로드와 같은 PST 파일을 하드 드라이브에 복사 하려면 파일 공유 또는 조직에서 파일 서버에 배치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p110">**Drive shipping**The WAImportExport.exe tool (downloaded in step 1) is used to copy your PST files to the hard drive. This tool encrypts the hard drive with BitLocker and then copies the PSTs to the hard drive. Like network upload, the PST files that you want to copy to the hard drive have to be located in a file share or file server in your organization.</span></span>
    
3. <span data-ttu-id="927f9-p111">어떤 사용자 사서함은 PST 파일에 이식 될를 지정 하는 쉼표로 구분 된 값 (CSV) 파일을 만들려면 다음 단계는 **PST 가져오기 매핑 파일을 만드는** -PST 파일 Azure 저장소 위치에 업로드 되거나 하드 드라이브에 복사 된 후, (a nd PST 파일을 가져올 수는 사용자의 기본 사서함 또는 보관 사서함에). Office 365를 가져올 서비스 정보를 사용 하 여 PST 파일을 가져오려면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p111">**Create a PST import mapping file** - After the PST files have been uploaded to the Azure storage location or copied to a hard drive, the next step is to create a comma separated value (CSV) file that specifies which user mailboxes the PST files will be imported to (and a PST file can be imported to a user's primary mailbox or their archive mailbox). The Office 365 Import service will use the information to import the PST files.</span></span> 
    
4. <span data-ttu-id="927f9-p112">**PST 만들기 작업 가져오기** -다음 단계는 보안에서 **가져오기** 페이지에서 PST 가져오기 작업을 만들려면 &amp; 준수 센터 및 이전 단계에서 만든 PST 가져오기 매핑 파일을 제출 합니다. 네트워크 업로드에 대 한 (하기 때문에 PST 파일 Azure에 업로드 된) Office 365 PST 파일의 데이터를 분석 하 고 데이터를 실제로 PST 가져오기 매핑 파일에 지정 된 사서함에 가져온 가져옵니다을 제어 하는 필터를 설정할 수 있는 기회를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p112">**Create a PST import job** - The next step is to create a PST import job on the **Import** page in the Security &amp; Compliance Center and submit the PST import mapping file created in the previous step. For network upload (because the PST files have been uploaded to Azure) Office 365 analyzes the data in the PST files and then gives you an opportunity to set filters that control what data actually gets imported to the mailboxes specified in the PST import mapping file.</span></span> 
    
    <span data-ttu-id="927f9-140">드라이브 전달에 대 한 몇가지 추가 작업을 하는 프로세스에 지정 된이 위치에 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-140">For drive shipping, a few additional things happen at this point in the process.</span></span>
    
    - <span data-ttu-id="927f9-141">Microsoft 데이터 센터 (Microsoft 데이터 센터에 대 한 전달 주소는 가져오기 작업을 만들 때 표시 됨)에 하드 드라이브를 물리적으로 제공</span><span class="sxs-lookup"><span data-stu-id="927f9-141">You physically ship the hard drive to a Microsoft data center (the shipping address for the Microsoft data center is displayed when the import job is created)</span></span>
    
    - <span data-ttu-id="927f9-p113">Microsoft 하드 드라이브를 받으면 데이터 센터 담당자 조직에 대 한 Azure 저장소 위치로 하드 드라이브에 Pst 파일을 업로드 합니다. 앞에서 설명한 것 처럼 PST 파일 위치로 Azure 저장소 동일한 지역 Microsoft 데이터 센터에 있는 Office 365 조직 위치한 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p113">When Microsoft receives the hard drive, data center personnel will upload the PSTs files on the hard drive to the Azure storage location for your organization. As previously explained, your PST files are uploaded to a Azure storage location that resides in the same regional Microsoft datacenter where your Office 365 organization is located.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="927f9-144">PST 파일을 하드 드라이브에 7-10 일 이내 Microsoft 하드 드라이브를 받은 후 Azure에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-144">The PST files on the hard drive are uploaded to Azure within 7 to 10 business days after Microsoft receives the hard drive.</span></span> 
  
      <span data-ttu-id="927f9-145">그런 다음 네트워크 업로드 프로세스와 같은 Office 365는 PST 파일의 데이터를 분석 하 고 데이터는 실제로 PST 가져오기 매핑 파일에 지정 된 사서함에 가져온 가져옵니다을 제어 하는 필터를 설정할 수 있는 기회를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-145">Like the network upload process, Office 365 then analyzes the data in the PST files and gives you an opportunity to set filters that control what data actually gets imported to the mailboxes specified in the PST import mapping file.</span></span>
    
    - <span data-ttu-id="927f9-146">Microsoft는 다시 하드 드라이브를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-146">Microsoft ships the hard drive back to you.</span></span> 
    
5. <span data-ttu-id="927f9-p114">**필터 사서함으로 가져올 PST 데이터** -Office 365 (안전 하 고 안전 하 게)에서 PST 파일의 데이터를 분석 가져오기 작업을 만들었으면 (및 드라이브 전달 작업에서 PST 파일 Azure 저장소 위치에 업로드 된 후) PST 파일에 포함 된 다양 한 메시지 형식과 항목의 보존 기간을 식별 합니다. 분석이 완료 되 고 데이터를 가져올 준비가 되었습니다, PST 파일에 포함 된 모든 데이터를 가져올 수 있는 옵션 했거나 데이터를 가져온 가져옵니다을 제어 하는 필터를 설정 하 여 가져온 데이터를 자를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p114">**Filter the PST data that will be imported to mailboxes** - After the import job is created (and after the PST files from a drive shipping job are uploaded to the Azure storage location) Office 365 analyzes the data in the PST files (safely and securely) by identifying the age of the items and the different message types included in the PST files. When the analysis is completed and the data is ready to import, you have the option to import all the data contained in the PST files or you can trim the data that's imported by setting filters that control what data gets imported.</span></span> 
    
6. <span data-ttu-id="927f9-p115">**PST 가져오기 작업을 시작** -가져오기 작업이 시작 된 후, Office 365 정보를 사용 하는 PST 가져오기 매핑 파일에 사용자 사서함에 그 Azure 저장소 위치에서 Pst 파일을 가져옵니다. 보안에서 **가져오기** 페이지에 표시 됩니다 (가져올 각 PST 파일에 대 한 정보를 포함 하 여) 가져오기 작업에 대 한 상태 정보 &amp; 준수 센터입니다. 가져오기 작업이 완료 되 면 작업에 대 한 상태가 **완료**로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p115">**Start the PST import job** - After the import job is started, Office 365 uses the information in the PST import mapping file to import the PSTs files from the he Azure storage location to user mailboxes. Status information about the import job (including information about each PST file being imported) is displayed on the **Import** page in the Security &amp; Compliance Center. When the import job is finished, the status for the job is set to **Complete**.</span></span>
  
## <a name="why-import-email-data-to-office-365"></a><span data-ttu-id="927f9-152">Office 365로 전자 메일 데이터를 가져올 이유?</span><span class="sxs-lookup"><span data-stu-id="927f9-152">Why import email data to Office 365?</span></span>

- <span data-ttu-id="927f9-153">Office 365에 조직의 전자 메일을 마이그레이션하는 한 가지 방법은 사용자 사서함에 PST 파일 가져오기 (영문).</span><span class="sxs-lookup"><span data-stu-id="927f9-153">Importing PST files to user mailboxes is one way to migrate your organization's email to Office 365.</span></span>
    
- <span data-ttu-id="927f9-p116">대상 사서함에 실제로 가져온 PST 파일에 항목을 필터링 하려면 [지능형 가져오기](filter-data-when-importing-pst-files.md) 기능을 사용할 수 있습니다. 이 사용 하는 필터를 설정 하 여 가져온 데이터를 높이고 제어 가져온 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p116">You can use the [Intelligent Import](filter-data-when-importing-pst-files.md) feature to filter the items in PST files that actually get imported to the target mailboxes. This lets you trim the data that's imported by setting filters that control what data gets imported.</span></span> 
    
- <span data-ttu-id="927f9-156">Office 365로 전자 메일 데이터 가져오기 (영문)는 조직의 규정 준수 요구를 충족 하도록 하 여 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-156">Importing email data to Office 365 helps address compliance needs of your organization by letting you:</span></span>
    
  - <span data-ttu-id="927f9-157">[보관 사서함](enable-archive-mailboxes.md) 및 사용자에 게 추가 사서함 저장 공간 [무제한 보관](unlimited-archiving.md) 을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-157">Enable [archive mailboxes](enable-archive-mailboxes.md) and [unlimited archiving](unlimited-archiving.md) to give users additional mailbox storage space.</span></span> 
    
  - <span data-ttu-id="927f9-158">[소송 보존으로 설정](https://go.microsoft.com/fwlink/?linkid=841243) 콘텐츠를 유지 하려면 사서함을 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-158">Place mailboxes on [Litigation Hold](https://go.microsoft.com/fwlink/?linkid=841243) to retain content.</span></span> 
    
  - <span data-ttu-id="927f9-159">[콘텐츠 검색 도구](content-search.md) 를 사용 하 여 사서함 콘텐츠를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-159">Use the [Content Search tool](content-search.md) to search for mailbox content.</span></span> 
    
  - <span data-ttu-id="927f9-160">조직의 법적 조사 [eDiscovery 사례](ediscovery-cases.md) 관리를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="927f9-160">Use [eDiscovery cases](ediscovery-cases.md) to mange your organization's legal investigations</span></span> 
    
  - <span data-ttu-id="927f9-161">보안에서 [보존 정책을](retention-policies.md) 사용 하 여 &amp; 사서함 콘텐츠를 보존 하는 기간을 제어 하려면 준수 센터 및 보존 기간이 만료 후 콘텐츠를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-161">Use [retention policies](retention-policies.md) in the Security &amp; Compliance Center to control how long mailbox content is retained, and then delete content after the retention period expires.</span></span> 
    
- <span data-ttu-id="927f9-p117">Office 365로 데이터 가져오기 (영문)을 사용 하면 데이터 손실을 보호할 수 있습니다. Office 365로 가져온 전자 메일 데이터 Exchange Online의 고가용성 기능을 상속 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p117">Importing data to Office 365 helps protect against data loss. Email data that's imported to Office 365 inherits the high availability features of Exchange Online.</span></span>
    
- <span data-ttu-id="927f9-164">Office 365의 전자 메일 데이터는 클라우드에 저장 되기 때문에 모든 장치에서 사용자에 게 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-164">Email data in Office 365 is available to users from all devices because it's stored in the cloud.</span></span>
    
## <a name="importing-sharepoint-data-to-office-365"></a><span data-ttu-id="927f9-165">Office 365를 SharePoint 데이터 가져오기 (영문)</span><span class="sxs-lookup"><span data-stu-id="927f9-165">Importing SharePoint data to Office 365</span></span>

<span data-ttu-id="927f9-p118">Office 365 조직에서 SharePoint 사이트 및 OneDrive 계정에 파일 및 문서도 가져올 수 있습니다. 자세한 내용은 다음 문서를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p118">You can also import files and documents to SharePoint sites and OneDrive accounts in your Office 365 organization. For more information, see the following articles:</span></span>

- [<span data-ttu-id="927f9-168">SharePoint Online으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="927f9-168">Migrate to SharePoint Online</span></span>](https://docs.microsoft.com/sharepointmigration/migrate-to-sharepoint-online)

- [<span data-ttu-id="927f9-169">SharePoint 마이그레이션 도구 소개</span><span class="sxs-lookup"><span data-stu-id="927f9-169">Introducing the SharePoint Migration Tool</span></span>](https://docs.microsoft.com/sharepointmigration/introducing-the-sharepoint-migration-tool)

- [<span data-ttu-id="927f9-170">PowerShell을 사용하여 SharePoint Online으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="927f9-170">Migrate to SharePoint Online using PowerShell</span></span>](https://docs.microsoft.com/sharepointmigration/overview-spmt-ps-cmdlets)

- [<span data-ttu-id="927f9-171">SharePoint online Azure 데이터 상자를 사용 하 여 파일 공유 콘텐츠 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="927f9-171">Migrate your file share content to SharePoint Online using the Azure Data Box</span></span>](https://docs.microsoft.com/sharepointmigration/how-to-migrate-file-share-content-to-spo-using-azuredatabox)


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a><span data-ttu-id="927f9-172">Office 365에 PST 파일 가져오기 (영문) 하는 방법에 대 한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="927f9-172">Frequently asked questions about importing PST files to Office 365</span></span>
  
<span data-ttu-id="927f9-173">다음은 대량 가져오기 PST 파일을 Office 365 사서함을 Office 365를 가져올 서비스를 사용 하는 방법에 대 한 몇가지 질문과 대답입니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-173">Here are some frequently asked questions about using the Office 365 Import service to bulk-import PST files to Office 365 mailboxes.</span></span> 
  
- [<span data-ttu-id="927f9-174">네트워크 업로드를 사용 하 여 PST 파일을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="927f9-174">Using network upload to import PST files</span></span>](#using-network-upload-to-import-pst-files)
  
- [<span data-ttu-id="927f9-175">드라이브 전달을 사용 하 여 PST 파일을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="927f9-175">Using drive shipping to import PST files</span></span>](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a><span data-ttu-id="927f9-176">네트워크 업로드를 사용 하 여 PST 파일을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="927f9-176">Using network upload to import PST files</span></span>

 <span data-ttu-id="927f9-177">**Office 365 가져오기 서비스에서 가져오기 작업을 만들 필요가 권한은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-177">**What permissions are required to create import jobs in the Office 365 Import Service?**</span></span>
  
<span data-ttu-id="927f9-p119">역할을 할당 사서함 가져오기 내보내기 Exchange 온라인 Office 365 사서함에 PST 파일을 가져오려면 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 사용자가 직접 또는 다른 사용자가 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹 Exchange Online의](https://go.microsoft.com/fwlink/p/?LinkId=730688)"역할 그룹 만들기" 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p119">You have to be assigned the Mailbox Import Export role in Exchange Online to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
  
<span data-ttu-id="927f9-183">또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-183">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
  
- <span data-ttu-id="927f9-p120">역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p120">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="927f9-186">또는</span><span class="sxs-lookup"><span data-stu-id="927f9-186">Or</span></span>
    
- <span data-ttu-id="927f9-187">Office 365 조직에서 전역 관리자 여야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-187">You have to be a global administrator in your Office 365 organization.</span></span>
    
> [!TIP]
> <span data-ttu-id="927f9-p121">Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p121">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
 <span data-ttu-id="927f9-190">**네트워크 업로드는 사용할 수 있는 어디 입니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-190">**Where is network upload available?**</span></span>
  
<span data-ttu-id="927f9-p122">네트워크 업로드는 미국, 캐나다, 브라질, 영국, 유럽, 인도, 한국, 남동쪽 아시아, 일본, 대한민국, 및 오스트레일리아에서 현재 사용할 수 있습니다. 네트워크 업로드 곧 사용할 수 있는 더 많은 지역에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p122">Network upload is currently available in the United States, Canada, Brazil, the United Kingdom, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Network upload will be available in more regions soon.</span></span>
  
 <span data-ttu-id="927f9-193">**네트워크 업로드를 사용 하 여 PST 파일을 가져오기 위한 가격 이란 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-193">**What is the pricing for importing PST files by using network upload?**</span></span>
  
<span data-ttu-id="927f9-194">네트워크 업로드를 사용 하 여 PST 파일을 가져올 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-194">Using network upload to import PST files is free.</span></span>
  
<span data-ttu-id="927f9-p123">즉,는 Azure 저장소 영역에서 PST 파일을 삭제 하 고, 후 더이상 표시 Office 365 관리 센터에서 완료 된 가져오기 작업에 대 한 파일의 목록입니다. 가져오기 작업은 **Office 365로 데이터 가져오기** 페이지에서 계속 표시 될 수 있습니다, 하지만 오래 된 가져오기 작업의 세부 정보를 볼 때에 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p123">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Office 365 admin center. Although an import job might still be listed on the **Import data to Office 365** page, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="927f9-197">**PST 파일 형식의 어떤 버전은 Office 365로 가져오기에 대 한 지원 합니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-197">**What version of the PST file format is supported for importing to Office 365?**</span></span>
  
<span data-ttu-id="927f9-p124">PST 파일 형식의 두 버전이: ANSI 및 유니코드 합니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 ANSI PST 파일 형식 더블 바이트 문자를 사용 하는 언어에 대 한 예를 사용 하는 파일 (DBCS) 설정, Office 365로 가져올 수도 있습니다. ANSI PST 파일 가져오기 (영문) 하는 방법에 대 한 자세한 내용은 [Office 365에 PST 파일을 가져오려면 업로드 사용 하 여 네트워크](https://go.microsoft.com/fwlink/p/?LinkId=823074)에서 4 단계를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="927f9-p124">There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. However, files that use the ANSI PST file format, such as those for languages that use a double-byte character set (DBCS), can also be imported to Office 365. For more information about importing ANSI PST files, see Step 4 in [Use network upload to import PST files to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=823074).</span></span>
  
<span data-ttu-id="927f9-202">또한 Office 365로 Outlook 2007 및 그 이후 버전에서 PST 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-202">Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.</span></span>
  
 <span data-ttu-id="927f9-203">**Azure 저장소 영역 내 PST 파일을 업로드 하 한 후 얼마나 오래 자신이에 보관 되는 Azure 삭제 되기 전에?**</span><span class="sxs-lookup"><span data-stu-id="927f9-203">**After I upload my PST files to the Azure storage area, how long are they kept in Azure before they're deleted?**</span></span>
  
<span data-ttu-id="927f9-p125">PST 파일을 가져오려면 네트워크 업로드 메서드를 사용 하면 **ingestiondata**라는 Azure blob 컨테이너에 업로드 있습니다. 에 없는 경우 가져오기 작업이 진행 중인 **가져오기** 페이지에서 보안을 &amp; 준수 센터), Azure의 **ingestiondata** 컨테이너에 있는 모든 PST 파일 30 일 &amp;준수 센터입니다. 보안에서 새 가져오기 작업을 만들 필요가 의미 &amp; Azure에 파일을 업로드 PST의 30 일 이내에 준수 센터 (네트워크 업로드 지침의 5 단계에에서 설명 된).</span><span class="sxs-lookup"><span data-stu-id="927f9-p125">When you use the network upload method to import PST files, you upload them to an Azure blob container named **ingestiondata**. If there are no import jobs in progress on the **Import** page in the Security &amp; Compliance Center), then all PST files in the **ingestiondata** container in Azure are deleted 30 days after the most recent import job was created in the Security &amp; Compliance Center. That also means you have to create a new import job in the Security &amp; Compliance Center (described in Step 5 in the network upload instructions) within 30 days of uploading PST files to Azure.</span></span> 
  
<span data-ttu-id="927f9-p126">즉, Azure 저장소 영역에서 PST 파일을 삭제 하 고, 후 자신이 더이상 표시 되는지의 보안에서 완료 된 가져오기 작업에 대 한 파일 목록에서 &amp; 준수 센터입니다. 가져오기 작업 **가져오기** 페이지의 보안에 계속 표시 될 수 있습니다 있지만 &amp; 준수 센터 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p126">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Security &amp; Compliance Center. Although an import job might still be listed on the **Import** page in the Security &amp; Compliance Center, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="927f9-209">**걸리는 사서함에 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-209">**How long does it take to import a PST file to a mailbox?**</span></span>
  
<span data-ttu-id="927f9-p127">네트워크 용량에 따라 달라 집니다 있지만 조직에 대 한 Azure 저장소 영역에 업로드 하는 데이터의 각 테라바이트 (테라바이트)에 대 한 몇 시간이 오래 걸립니다. PST 파일은 Azure 저장소 영역을 복사한 후 하루 24GB 이상인의 속도로 Office 365 사서함에는 PST 파일을 가져옵니다. 이 속도가 하지 사용자의 요구를 충족 하는 경우에 Office 365로 전자 메일 데이터를 마이그레이션하기 위한 다른 방법을 좋습니다. 자세한 내용은 [Office 365에 여러 전자 메일 계정으로 마이그레이션하는 방법](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="927f9-p127">It depends on the capacity of your network, but it typically takes several hours for each terabyte (TB) of data to be uploaded to the Azure storage area for your organization. After the PST files are copied to the Azure storage area, a PST file is imported to an Office 365 mailbox at a rate of at least 24 GB per day. If this rate doesn't meet your needs, you might consider other methods for migrating email data to Office 365. For more information, see [Ways to migrate multiple email accounts to Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).</span></span>
  
<span data-ttu-id="927f9-p128">가져오기 프로세스 병렬로; 발생 서로 다른 대상 사서함에 다른 PST 파일을 가져오는 경우 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로, 동일한 사서함에 여러 PST 파일을 가져오는 경우 자신이 됩니다 동시에 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p128">If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Likewise, if multiple PST files are imported to the same mailbox, they will be simultaneously imported.</span></span>
  
 <span data-ttu-id="927f9-216">**메시지 크기 제한을 PST 파일을 가져올 때 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-216">**Is there a message size limit when importing PST files?**</span></span>
  
<span data-ttu-id="927f9-p129">예입니다. PST 파일 150MB 보다 큰 사서함 항목을 포함 하는 경우 항목 가져오기 프로세스를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p129">Yes. If a PST file contains a mailbox item that is larger than 150 MB, the item will be skipped during the import process.</span></span>
  
 <span data-ttu-id="927f9-219">**메시지를 보내거나 받은, 받는 사람 목록과 기타 속성을 Office 365 사서함에 PST 파일을 가져올 때 유지 하는 경우와 같은 메시지 속성은?**</span><span class="sxs-lookup"><span data-stu-id="927f9-219">**Are message properties, such as when the message was sent or received, the list of recipients and other properties, preserved when PST files are imported to an Office 365 mailbox?**</span></span>
  
<span data-ttu-id="927f9-p130">예입니다. 원본 메시지 메타 데이터 가져오기 과정에서 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p130">Yes. The original message metadata isn't changed during the import process.</span></span>
  
 <span data-ttu-id="927f9-222">**이 사서함에 가져오려는 PST 파일에 대 한 폴더 계층 구조에 있는 수준 수에 제한이 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-222">**Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**</span></span>
  
<span data-ttu-id="927f9-p131">예입니다. 중첩 된 폴더의 300 개 이상인 수준이 있는 PST 파일을 가져올 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p131">Yes. You can't import a PST file that has 300 or more levels of nested folders.</span></span>
  
 <span data-ttu-id="927f9-225">**네트워크 업로드를 사용 하 여 Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-225">**Can I use network upload to import PST files to an inactive mailbox in Office 365?**</span></span>
  
<span data-ttu-id="927f9-226">예, 이제이 기능은 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-226">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="927f9-227">**네트워크 업로드를 사용 하 여 Exchange 하이브리드 배포에서 온라인 보관 사서함을 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-227">**Can I use network upload to import PST files to an online archive mailbox in an Exchange hybrid deployment?**</span></span>
  
<span data-ttu-id="927f9-228">예, 이제이 기능은 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-228">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="927f9-229">**네트워크 업로드를 사용 하 여 Exchange Online에서 공용 폴더에 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-229">**Can I use network upload to import PST files to public folders in Exchange Online?**</span></span>
  
<span data-ttu-id="927f9-230">아니요, 공용 폴더에는 PST 파일을 가져올 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-230">No, you can't import PST files to public folders.</span></span>
  
### <a name="using-drive-shipping-to-import-pst-files"></a><span data-ttu-id="927f9-231">드라이브 전달을 사용 하 여 PST 파일을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="927f9-231">Using drive shipping to import PST files</span></span>

 <span data-ttu-id="927f9-232">**Office 365 가져오기 서비스에서 가져오기 작업을 만들 필요가 권한은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-232">**What permissions are required to create import jobs in the Office 365 Import Service?**</span></span>
  
<span data-ttu-id="927f9-p132">Office 365 사서함에 PST 파일을 가져오려면 사서함 가져오기 내보내기 역할을 할당 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 사용자가 직접 또는 다른 사용자가 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹 Exchange Online의](https://go.microsoft.com/fwlink/p/?LinkId=730688)"역할 그룹 만들기" 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p132">You have to be assigned the Mailbox Import Export role to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
  
<span data-ttu-id="927f9-238">또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-238">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
  
- <span data-ttu-id="927f9-p133">역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p133">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="927f9-241">또는</span><span class="sxs-lookup"><span data-stu-id="927f9-241">Or</span></span>
    
- <span data-ttu-id="927f9-242">Office 365 조직에서 전역 관리자 여야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-242">You have to be a global administrator in your Office 365 organization.</span></span>
    
> [!TIP]
> <span data-ttu-id="927f9-p134">Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p134">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
 <span data-ttu-id="927f9-245">**여기서 제공 되는 드라이브 사용할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-245">**Where is drive shipping available?**</span></span>
  
<span data-ttu-id="927f9-p135">드라이브 전달은 미국, 캐나다, 브라질, 영국, 유럽, 인도, 한국, 남동쪽 아시아, 일본, 대한민국, 및 오스트레일리아 현재 사용할 수 있습니다. 드라이브 전달 곧 사용할 수 있는 더 많은 지역에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p135">Drive shipping is currently available in the United States, Canada, Brazil, the United Kingdom, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Drive shipping will be available in more regions soon.</span></span>
  
 <span data-ttu-id="927f9-248">**어떤 상업용 라이선스 계약 드라이브 전달이 지원 합니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-248">**What commercial licensing agreements support drive shipping?**</span></span>
  
<span data-ttu-id="927f9-p136">Office 365에 PST 파일을 가져오려면 전달 하는 드라이브를 사용할 수를 통해는 Microsoft EA (기업 계약). 드라이브 전달 Microsoft 제품 및 서비스 계약 (MPSA)를 통해 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p136">Drive shipping to import PST files to Office 365 is available through a Microsoft Enterprise Agreement (EA). Drive shipping isn't available through a Microsoft Products and Services Agreement (MPSA).</span></span>
  
 <span data-ttu-id="927f9-251">**Office 365에 PST 파일을 가져오려면 전달 하는 드라이브를 사용 하는 것에 대 한 가격 이란 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-251">**What is the pricing for using drive shipping to import PST files to Office 365?**</span></span>
  
<span data-ttu-id="927f9-p137">Office 365 사서함에 PST 파일을 가져오려면 드라이브 전달을 사용 하 여 비용은 $2 달러 (미국) GB의 데이터입니다. 예, 1, 000 g B (1TB)의 PST 파일을 포함 하는 하드 드라이브를 제공 하는 경우는 비용은 $ 2, 000 USD입니다. 가져오기 요금을 지불 하는 파트너를 사용 하 여 작업할 수 있습니다. 파트너 찾기 (영문) 하는 방법에 대 한 정보를 [Office 365 파트너 또는 대리점 찾기](https://go.microsoft.com/fwlink/p/?LinkId=785197)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="927f9-p137">The cost to use drive shipping to import PST files to Office 365 mailboxes is $2 USD per GB of data. For example, if you ship a hard drive that contains 1,000 GB (1 TB) of PST files, the cost is $2,000 USD. You can work with a partner to pay the import fee. For information about finding a partner, see [Find your Office 365 partner or reseller](https://go.microsoft.com/fwlink/p/?LinkId=785197).</span></span>
  
 <span data-ttu-id="927f9-256">**어떤 종류의 하드 드라이브 드라이브 전달에 대 한 지원 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-256">**What kind of hard drives are supported for drive shipping?**</span></span>
  
<span data-ttu-id="927f9-p138">2.5 인치만 반도체 드라이브 (Ssd) 또는 2.5 또는 3.5 인치 SATA II/III 내부 하드 드라이브에 Office 365 가져오기 서비스와 함께 사용할 수 있도록 지원 합니다. 하드 드라이브를 사용할 수 있는 최대 10TB 합니다. 가져오기 작업에 대 한 하드 드라이브에 첫번째 데이터 볼륨을 처리 됩니다. 데이터 볼륨 NTFS로 포맷 되어야 합니다. 하드 드라이브에 데이터를 복사, 2.5 인치 SSD를 사용 하 여 직접 연결할 수 있습니다 또는 2.5 또는 3.5 인치 SATA II/III 커넥터 또는 외부 2.5 인치 SSD를 사용 하 여 외부에서 또는 2.5 또는 3.5 인치 SATA II/III USB 어댑터를 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p138">Only 2.5 inch solid-state drives (SSDs) or 2.5 or 3.5 inch SATA II/III internal hard drives are supported for use with the Office 365 Import service. You can use hard drives up to 10 TB. For import jobs, only the first data volume on the hard drive will be processed. The data volume must be formatted with NTFS. When copying data to a hard drive, you can attach it directly using a 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III connector or you can attach it externally using an external 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III USB adaptor.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="927f9-p139">외부 하드 드라이브에 사용 된 기본 제공 된 USB 어댑터와 함께 제공 되는 Office 365 가져오기 서비스에서 지원 되지 않습니다. 또한 외부 하드 드라이브의 대/소문자 내부 디스크를 사용할 수 없습니다. 하드 드라이브에 외부 하십시오 제공 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="927f9-p139">External hard drives that come with an built-in USB adaptor aren't supported by the Office 365 Import service. Additionally, the disk inside the casing of an external hard drive can't be used. Please don't ship external hard drives.</span></span> 
  
 <span data-ttu-id="927f9-265">**단일 가져오기 작업에 대 한 제공할 수 하드 드라이브에 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-265">**How many hard drives can I ship for a single import job?**</span></span>
  
<span data-ttu-id="927f9-266">단일 가져오기 작업에 대 한 하드 드라이브에 10의 최대를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-266">You can ship a maximum of 10 hard drives for a single import job.</span></span>
  
 <span data-ttu-id="927f9-267">**후 내 하드 드라이브를 제공 하는 소요 Microsoft 데이터 센터를?**</span><span class="sxs-lookup"><span data-stu-id="927f9-267">**After I ship my hard drive, how long does it take to get to the Microsoft data center?**</span></span>
  
<span data-ttu-id="927f9-p140">Microsoft 데이터 센터에 근접 하 여 같은 몇가지 작업에 따라 다릅니다 하 고 사용자의 하드 드라이브 (예: 다음 일 배송, 2 일 배달 날짜 또는 밑면 배달)를 제공 하는 데 사용 전달 옵션의 종류입니다. 대부분 shippers와 프로그램 배달의 상태를 추적 하려면 추적 번호를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p140">That depends on a few things, such as your proximity to the Microsoft data center and what kind of shipping option you used to ship your hard drive (such as, next-day delivery, two-day delivery, or ground-delivery). With most shippers, you can use the tracking number to track the status of your delivery.</span></span>
  
 <span data-ttu-id="927f9-270">**Microsoft 데이터 센터에 도착 하면 내 하드 드라이브는 걸리는 Azure에 내 PST 파일을 업로드할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-270">**After my hard drive arrives at the Microsoft data center, how long does it take to upload my PST files to Azure?**</span></span>
  
<span data-ttu-id="927f9-p141">하드 드라이브에 Microsoft 데이터 센터를 받은 후에 조직에 대 한 Microsoft Azure 저장소 영역에 PST 파일을 업로드 하려면 7 ~ 10 일 사이의 수행 됩니다. 명명 된 Azure blob 컨테이너에 PST 파일은 업로드 `ingestiondata`합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p141">After your hard drive is received at the Microsoft data center, it will take between 7 to 10 business days to upload the PST files to the Microsoft Azure storage area for your organization. The PST files will be uploaded to a Azure blob container named `ingestiondata`.</span></span> 
  
 <span data-ttu-id="927f9-273">**걸리는 사서함에 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-273">**How long does it take to import a PST file to a mailbox?**</span></span>
  
<span data-ttu-id="927f9-p142">PST 파일 Azure 저장소 영역으로 업로드 된 후 Office 365를 분석 PST 파일의 데이터 (을 안전 하 게 방식으로)를 다양 한 메시지 형식과 PST 파일에 포함 된 항목의 보존 기간을 식별 합니다. 이 분석 완료 되 면 PST 파일에 있는 모든 데이터를 가져올 수 있는 옵션 해야 또는 하는 필터 설정 제어 가져온 데이터를 가져옵니다. 가져오기 작업을 시작한 후 하루 24GB 이상인의 속도로 Office 365 사서함에는 PST 파일을 가져옵니다. 이 속도가 하지 사용자의 요구를 충족 하는 경우에 Office 365로 전자 메일 데이터를 가져오기 위한 다른 방법을 좋습니다. 자세한 내용은 [Office 365에 여러 전자 메일 계정으로 마이그레이션하는 방법](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="927f9-p142">After the PST files are uploaded to the Azure storage area, Office 365 analyzes the data in the PST files (in a safe and secure manner) to identify the age of the items and the different message types included in the PST files. When this analysis is complete, you'll have the option to import all the data in the PST files or set filters to that control what data gets imported. After you start the import job, a PST file is imported to an Office 365 mailbox at a rate of at least 24 GB per day. If this rate doesn't meet your needs, you might consider other methods for importing email data to Office 365. For more information, see [Ways to migrate multiple email accounts to Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).</span></span>
  
<span data-ttu-id="927f9-p143">가져오기 프로세스 병렬로; 발생 서로 다른 대상 사서함에 다른 PST 파일을 가져오는 경우 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로, 동일한 사서함에 여러 PST 파일을 가져오는 경우 자신이 됩니다 동시에 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p143">If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Likewise, if multiple PST files are imported to the same mailbox, they will be simultaneously imported.</span></span>
  
 <span data-ttu-id="927f9-281">**Microsoft Azure에 내 PST 파일을 업로드, 후 얼마나 오래 자신이에 보관 되는 Azure 삭제 되기 전에?**</span><span class="sxs-lookup"><span data-stu-id="927f9-281">**After Microsoft uploads my PST files to Azure, how long are they kept in Azure before they're deleted?**</span></span>
  
<span data-ttu-id="927f9-282">조직에 대 한 Azure 저장소 위치에 있는 모든 PST 파일 (라는 blob 컨테이너에 `ingestiondata`), 30 일 **가져오기** 페이지의 보안에서 가장 최근의 가져오기 작업이 만들어진 후에 삭제 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-282">All PST files in the Azure storage location for your organization (in blob container named `ingestiondata`), are deleted 30 days after the most recent import job was created on the **Import** page in the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="927f9-p144">즉, Azure 저장소 영역에서 PST 파일을 삭제 하 고, 후 자신이 더이상 표시 되는지의 보안에서 완료 된 가져오기 작업에 대 한 파일 목록에서 &amp; 준수 센터입니다. 가져오기 작업 **가져오기** 페이지의 보안에 계속 표시 될 수 있습니다 있지만 &amp; 준수 센터 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p144">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Security &amp; Compliance Center. Although an import job might still be listed on the **Import** page in the Security &amp; Compliance Center, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="927f9-285">**PST 파일 형식의 어떤 버전은 Office 365로 가져오기에 대 한 지원 합니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-285">**What version of the PST file format is supported for importing to Office 365?**</span></span>
  
<span data-ttu-id="927f9-p145">PST 파일 형식의 두 버전이: ANSI 및 유니코드 합니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 ANSI PST 파일 형식 더블 바이트 문자를 사용 하는 언어에 대 한 예를 사용 하는 파일 (DBCS) 설정, Office 365로 가져올 수도 있습니다. ANSI PST 파일 가져오기 (영문) 하는 방법에 대 한 자세한 내용은 [Office 365로 조직 PST 파일을 가져오려면 전달 하는 드라이브를 사용 하 여](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file)에서 3 단계를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="927f9-p145">There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. However, files that use the ANSI PST file format, such as those for languages that use a double-byte character set (DBCS), can also be imported to Office 365. For more information about importing ANSI PST files, see Step 3 in [Use drive shipping to import your organization PST files to Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).</span></span>
  
<span data-ttu-id="927f9-290">또한 Office 365로 Outlook 2007 및 그 이후 버전에서 PST 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-290">Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.</span></span>
  
 <span data-ttu-id="927f9-291">**메시지 크기 제한을 PST 파일을 가져올 때 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-291">**Is there a message size limit when importing PST files?**</span></span>
  
<span data-ttu-id="927f9-p146">예입니다. PST 파일 150MB 보다 큰 사서함 항목을 포함 하는 경우 항목 가져오기 프로세스를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p146">Yes. If a PST file contains a mailbox item that is larger than 150 MB, the item will be skipped during the import process.</span></span>
  
 <span data-ttu-id="927f9-294">**메시지를 보내거나 받은, 받는 사람 목록과 기타 속성을 Office 365 사서함에 PST 파일을 가져올 때 유지 하는 경우와 같은 메시지 속성은?**</span><span class="sxs-lookup"><span data-stu-id="927f9-294">**Are message properties, such as when the message was sent or received, the list of recipients and other properties, preserved when PST files are imported to an Office 365 mailbox?**</span></span>
  
<span data-ttu-id="927f9-p147">예입니다. 가져오기 프로세스 중에 원본 메시지 메타 데이터 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p147">Yes. The original message metadata isn't changed during the import process</span></span>
  
 <span data-ttu-id="927f9-297">**이 사서함에 가져오려는 PST 파일에 대 한 폴더 계층 구조에 있는 수준 수에 제한이 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-297">**Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**</span></span>
  
<span data-ttu-id="927f9-p148">예입니다. 중첩 된 폴더의 300 개 이상인 수준이 있는 PST 파일을 가져올 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p148">Yes. You can't import a PST file that has 300 or more levels of nested folders.</span></span>
  
 <span data-ttu-id="927f9-300">**드라이브 전달을 사용 하 여 Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-300">**Can I use drive shipping to import PST files to an inactive mailbox in Office 365?**</span></span>
  
<span data-ttu-id="927f9-301">예, 이제이 기능은 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-301">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="927f9-302">**드라이브 전달을 사용 하 여 Exchange 하이브리드 배포에서 온라인 보관 사서함을 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-302">**Can I use drive shipping to import PST files to an online archive mailbox in an Exchange hybrid deployment?**</span></span>
  
<span data-ttu-id="927f9-303">예, 이제이 기능은 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-303">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="927f9-304">**드라이브 전달을 사용 하 여 Exchange Online에서 공용 폴더에 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-304">**Can I use drive shipping to import PST files to public folders in Exchange Online?**</span></span>
  
<span data-ttu-id="927f9-305">아니요, 공용 폴더에는 PST 파일을 가져올 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-305">No, you can't import PST files to public folders.</span></span>
  
 <span data-ttu-id="927f9-306">**Microsoft 본인에 게 다시 제공 될 전에 내 하드 드라이브 지우기 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-306">**Can Microsoft wipe my hard drive before they ship it back to me?**</span></span>
  
<span data-ttu-id="927f9-p149">아니요, Microsoft 고객에 게이 제공 하기 전에 하드 드라이브를 지울 수 없습니다. 하드 드라이브 시점의 Microsoft에서 수신 되는 동일한 상태에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p149">No, Microsoft can't wipe hard drives before shipping them back to customers. Hard drives are returned to you in the same state they were in when they were received by Microsoft.</span></span>
  
 <span data-ttu-id="927f9-309">**Microsoft 본인에 게 다시 전달 하는 대신 내 하드 드라이브를 구입 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-309">**Can Microsoft shred my hard drive instead of shipping it back to me?**</span></span>
  
<span data-ttu-id="927f9-p150">아니요, Microsoft 하드 드라이브를 삭제할 수 없습니다. 하드 드라이브 시점의 Microsoft에서 수신 되는 동일한 상태에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p150">No, Microsoft can't destroy your hard drive. Hard drives are returned to you in the same state they were in when they were received by Microsoft.</span></span>
  
 <span data-ttu-id="927f9-312">**어떤 courier 서비스 반환 전달에 대 한 지원 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-312">**What courier services are supported for return shipping?**</span></span>
  
<span data-ttu-id="927f9-p151">미국 또는 유럽 고객 인 경우 Microsoft FedEx을 사용 하 여 사용자의 하드 드라이브를 반환 합니다. 다른 모든 지역에 대 한 Microsoft DHL를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p151">If you're a customer in the United States or Europe, Microsoft uses FedEx to return your hard drive. For all other regions, Microsoft uses DHL.</span></span>
  
 <span data-ttu-id="927f9-315">**반환 운송 비용 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-315">**What are the return shipping costs?**</span></span>
  
<span data-ttu-id="927f9-p152">운송 비용에 따라 다를 Microsoft 데이터 센터에 하드 드라이브를 전달 하는 근접 하 여 반환 합니다. Microsoft는 사용자의 하드 드라이브를 반환 하려면 FedEx 또는 DHL 계정을 청구 됩니다. 반환 배송 비용은 귀하의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p152">Return shipping costs vary, depending on your proximity to the Microsoft data center that you shipped your hard drive to. Microsoft will bill your FedEx or DHL account to return your hard drive. The cost of return shipping is your responsibility.</span></span>
  
 <span data-ttu-id="927f9-319">**FedEx 사용자 지정 전달 등 사용자 지정 courier 배송 서비스를 사용 하 여 Microsoft에 내 하드 드라이브를 제공 하려면 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-319">**Can I use a custom courier shipping service, such as FedEx Custom Shipping, to ship my hard drive to Microsoft?**</span></span>
  
<span data-ttu-id="927f9-320">예.</span><span class="sxs-lookup"><span data-stu-id="927f9-320">Yes.</span></span>
  
 <span data-ttu-id="927f9-321">**다른 국가에 내 하드 드라이브 제공 있으면는 사항이 취해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="927f9-321">**If I have to ship my hard drive to another country, is there anything I need to do?**</span></span>
  
<span data-ttu-id="927f9-p153">Microsoft에 제공 되는 하드 드라이브 국제 테두리를 교차 하 게 될 수 있습니다. 이 경우에 하드 드라이브와 포함 된 데이터는 가져온 및/또는 관련 법률에 따라를 내보낼 수 있는지 확인 하는 일을 담당 것입니다. 하드 드라이브를 전달 하기 전에 드라이브와 데이터 합법적으로 전달할 수 있습니다. 지정 된 Microsoft 데이터 센터를 확인 하 여 문에 확인. 이 적시에 Microsoft에 도달 하기 위해 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="927f9-p153">The hard drive that you ship to Microsoft might have to cross international borders. If this is the case, you're responsible for ensuring that the hard drive and the data it contains are imported and/or exported in accordance with the applicable laws. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the specified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.</span></span>
