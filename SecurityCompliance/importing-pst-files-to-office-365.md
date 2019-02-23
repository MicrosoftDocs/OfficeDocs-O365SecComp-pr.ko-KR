---
title: Overview of importing your organization PST files to Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.IngestionHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: '관리자: Office 365 보안 &amp; 및 준수 센터에서 가져오기 서비스를 사용 하 여 Exchange Online의 사용자 사서함에 대 한 전자 메일 데이터 (PST 파일)를 대량으로 가져오는 방법에 대해 알아봅니다. 이 항목에서는 faq를 제공 하 고 PST 가져오기 프로세스의 작동 방식에 대해 설명 합니다.'
ms.openlocfilehash: b6f32a6b5552773c197003ddac41c138539bb6ef
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218048"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a><span data-ttu-id="c3bfb-104">Overview of importing your organization PST files to Office 365</span><span class="sxs-lookup"><span data-stu-id="c3bfb-104">Overview of importing your organization PST files to Office 365</span></span>

> [!NOTE]
> <span data-ttu-id="c3bfb-p102">이 문서는 관리자를 위한 것입니다. PST 파일을 자체 사서함으로 가져오시겠습니까? [Outlook .pst 파일에서 전자 메일, 연락처 및 일정 가져오기를](https://go.microsoft.com/fwlink/p/?LinkID=785075) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p102">This article is for administrators. Are you trying to import PST files to your own mailbox? See [Import email, contacts, and calendar from an Outlook .pst file](https://go.microsoft.com/fwlink/p/?LinkID=785075)</span></span>

<span data-ttu-id="c3bfb-p103">office 365 보안 &amp; 및 준수 센터의 가져오기 서비스를 사용 하 여 office 365 조직의 Exchange Online 사서함으로 PST 파일을 빠르게 대량으로 가져올 수 있습니다. PST 파일을 Office 365로 가져오는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p103">You can use the Import service in the Office 365 Security &amp; Compliance Center to quickly bulk-import PST files to Exchange Online mailboxes in your Office 365 organization. There are two ways you can import PST files to Office 365:</span></span>
   
- <span data-ttu-id="c3bfb-p104">**네트워크 업로드** ![클라우드 업로드](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) -네트워크를 통해 PST 파일을 Microsoft 클라우드의 임시 Azure 저장소 위치로 업로드 합니다. 그런 다음 office 365 가져오기 서비스를 사용 하 여 office 365 조직의 사서함으로 PST 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p104">**Network upload** ![Cloud upload](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) - Upload the PST files over the network to a temporary Azure storage location in the Microsoft cloud. Then you use the Office 365 Import service to import the PST data to mailboxes in your Office 365 organization.</span></span> 

- <span data-ttu-id="c3bfb-p105">**드라이브 전달** ![하드 디스크](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) -PST 파일을 BitLocker로 암호화 된 하드 드라이브에 복사한 다음 물리적으로 Microsoft에 드라이브를 배송 합니다. microsoft는 하드 드라이브를 수신 하는 경우 데이터 센터 직원은 microsoft 클라우드의 임시 Azure 저장소 위치에 데이터를 업로드 합니다. 그런 다음 office 365 가져오기 서비스를 사용 하 여 office 365 조직의 사서함으로 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p105">**Drive shipping** ![Hard disk](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) - Copy the PST files to a BitLocker-encrypted hard drive and then physically ship the drive to Microsoft. When Microsoft receives the hard drive, data center personnel upload the data to a temporary Azure storage location in the Microsoft cloud. Then you use the Office 365 Import service to import the data to mailboxes in your Office 365 organization.</span></span>

## <a name="step-by-step-instructions"></a><span data-ttu-id="c3bfb-115">단계별 지침</span><span class="sxs-lookup"><span data-stu-id="c3bfb-115">Step-by-step instructions</span></span>
  
<span data-ttu-id="c3bfb-116">조직의 PST 파일을 Office 365로 대량 가져오는 방법에 대 한 단계별 지침을 보려면 다음 항목 중 하나를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-116">See one of the following topics for detailed, step-by-step instructions for bulk-importing your organization's PST files to Office 365.</span></span> 
   
- [<span data-ttu-id="c3bfb-117">네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3bfb-117">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
- [<span data-ttu-id="c3bfb-118">드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3bfb-118">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a><span data-ttu-id="c3bfb-119">PST 파일을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="c3bfb-119">How importing PST files works</span></span>

<span data-ttu-id="c3bfb-p106">다음은 전체 PST 가져오기 프로세스에 대 한 설명입니다. 다음 그림에서는 기본 워크플로를 보여 주고 네트워크 업로드 및 드라이브 전달 방법 간의 차이점을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p106">Here's an illustration and description of the complete PST import process. The illustration shows the primary workflow and highlights the differences between the network upload and drive shipping methods.</span></span>
  
![PST 가져오기 프로세스 워크플로](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. <span data-ttu-id="c3bfb-p107">**pst 가져오기 도구 및 키를 사설 Azure 저장소 위치로 다운로드** -pst 파일을 업로드 하거나 하드 드라이브에 복사 하는 데 사용 되는 도구 및 액세스 키를 다운로드 하는 첫 번째 단계입니다. Office 365 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서이를 가져옵니다. 키를 사용 하면 개인 및 안전한 Azure storage 위치에 PST 파일을 업로드 하는 데 필요한 사용 권한 (또는 드라이브 전달의 경우 Microsoft data center 직원)이 제공 됩니다. 이 선택 키는 조직에서 고유 하며, Microsoft 클라우드로 업로드 된 후에 해당 PST 파일에 대 한 무단 액세스를 방지 하는 데 도움이 됩니다. PST 파일을 Office 365로 가져오는 경우 조직에서 별도의 Azure 구독을 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p107">**Download the PST import tools and key to private Azure storage location** - The first step is to download the tool and access key used to upload the PST files or copy them to a hard drive. You obtain these from the **Import** page in the Office 365 Security &amp; Compliance Center. The key provides you (or Microsoft data center personnel in the case of drive shipping) with the necessary permissions to upload PST files to a private and secure Azure storage location. This access key is unique to your organization and helps prevent unauthorized access to your PST files after they're uploaded to the Microsoft cloud. Note that importing PST files to Office 365 doesn't require your organization to have a separate Azure subscription.</span></span> 
    
2. <span data-ttu-id="c3bfb-p108">**pst 파일 업로드 또는 복사** -다음 단계는 네트워크 업로드 또는 드라이브 전달을 사용 하 여 pst 파일을 가져올지 여부에 따라 달라 집니다. 두 경우 모두 이전 단계에서 얻은 도구 및 보안 저장소 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p108">**Upload or copy the PST files** - The next step depends on whether you're using network upload or drive shipping to import PST files. In both cases, you'll use the tool and secure storage key that you obtained in the previous step.</span></span>
    
    - <span data-ttu-id="c3bfb-p109">**네트워크 업로드** 1 단계에서 다운로드 한 AzCopy 도구는 Microsoft 클라우드의 Azure 저장소 위치에 PST 파일을 업로드 하 고 저장 하는 데 사용 됩니다. PST 파일을 업로드 하는 Azure 저장소 위치는 Office 365 조직이 있는 동일한 지역 Microsoft 데이터 센터에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p109">**Network upload**The AzCopy.exe tool (downloaded in step 1) is used to upload and store your PST files in an Azure storage location in the Microsoft cloud. Note that the Azure storage location that you upload your PST files to resides in the same regional Microsoft datacenter where your Office 365 organization is located.</span></span> 
    
      <span data-ttu-id="c3bfb-132">이를 업로드 하려면 Office 365로 가져올 PST 파일이 조직의 파일 공유 또는 파일 서버에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-132">To upload them, the PST files that you want to import to Office 365 have to be located in a file share or file server in your organization.</span></span>
    
    - <span data-ttu-id="c3bfb-p110">**드라이브 전달** 1 단계에서 다운로드 한 waimportexport 도구는 PST 파일을 하드 드라이브에 복사 하는 데 사용 됩니다. 이 도구는 BitLocker로 하드 드라이브를 암호화 한 다음 pst를 하드 드라이브에 복사 합니다. 네트워크 업로드와 마찬가지로 하드 드라이브에 복사할 PST 파일을 조직의 파일 공유 또는 파일 서버에 배치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p110">**Drive shipping**The WAImportExport.exe tool (downloaded in step 1) is used to copy your PST files to the hard drive. This tool encrypts the hard drive with BitLocker and then copies the PSTs to the hard drive. Like network upload, the PST files that you want to copy to the hard drive have to be located in a file share or file server in your organization.</span></span>
    
3. <span data-ttu-id="c3bfb-p111">**pst 가져오기 매핑 파일 만들기** -pst 파일이 Azure 저장 위치로 업로드 되거나 하드 드라이브에 복사 된 후에는 pst 파일을 가져올 사용자 사서함을 지정 하는 CSV (쉼표로 구분 된 값) 파일을 만듭니다 ( nd PST 파일을 사용자의 기본 사서함 이나 보관 사서함으로 가져올 수 있습니다. Office 365 가져오기 서비스는이 정보를 사용 하 여 PST 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p111">**Create a PST import mapping file** - After the PST files have been uploaded to the Azure storage location or copied to a hard drive, the next step is to create a comma separated value (CSV) file that specifies which user mailboxes the PST files will be imported to (and a PST file can be imported to a user's primary mailbox or their archive mailbox). The Office 365 Import service will use the information to import the PST files.</span></span> 
    
4. <span data-ttu-id="c3bfb-p112">**pst 가져오기 작업 만들기** -다음 단계는 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서 pst 가져오기 작업을 만들고 이전 단계에서 만든 pst 가져오기 매핑 파일을 제출 하는 것입니다. 네트워크 업로드의 경우 (pst 파일이 Azure에 업로드 되었기 때문에) Office 365에서 pst 파일의 데이터를 분석 한 다음, 실제로 pst 가져오기 매핑 파일에 지정 된 사서함으로 가져오는 데이터를 제어 하는 필터를 설정할 수 있는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p112">**Create a PST import job** - The next step is to create a PST import job on the **Import** page in the Security &amp; Compliance Center and submit the PST import mapping file created in the previous step. For network upload (because the PST files have been uploaded to Azure) Office 365 analyzes the data in the PST files and then gives you an opportunity to set filters that control what data actually gets imported to the mailboxes specified in the PST import mapping file.</span></span> 
    
    <span data-ttu-id="c3bfb-140">드라이브 전달 시에는 프로세스의이 시점에서 몇 가지 추가 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-140">For drive shipping, a few additional things happen at this point in the process.</span></span>
    
    - <span data-ttu-id="c3bfb-141">microsoft 데이터 센터에 실제로 하드 드라이브를 배송 하는 경우 (가져오기 작업을 만들 때 microsoft 데이터 센터의 배송 주소가 표시 됨)</span><span class="sxs-lookup"><span data-stu-id="c3bfb-141">You physically ship the hard drive to a Microsoft data center (the shipping address for the Microsoft data center is displayed when the import job is created)</span></span>
    
    - <span data-ttu-id="c3bfb-p113">Microsoft에서 하드 드라이브를 받으면 데이터 센터 직원은 하드 드라이브에 있는 pst 파일을 조직의 Azure storage 위치에 업로드 합니다. 앞에서 설명한 것 처럼 PST 파일은 Office 365 조직이 있는 동일한 지역 Microsoft 데이터 센터에 있는 Azure 저장소 위치로 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p113">When Microsoft receives the hard drive, data center personnel will upload the PSTs files on the hard drive to the Azure storage location for your organization. As previously explained, your PST files are uploaded to a Azure storage location that resides in the same regional Microsoft datacenter where your Office 365 organization is located.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="c3bfb-144">하드 드라이브에 있는 PST 파일은 Microsoft가 하드 드라이브를 수신 하는 동안 7 일에서 영업일까지 Azure에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-144">The PST files on the hard drive are uploaded to Azure within 7 to 10 business days after Microsoft receives the hard drive.</span></span> 
  
      <span data-ttu-id="c3bfb-145">네트워크 업로드 프로세스와 마찬가지로, Office 365은 pst 파일의 데이터를 분석 하 고, 실제로 pst 가져오기 매핑 파일에 지정 된 사서함으로 가져오는 데이터를 제어 하는 필터를 설정할 수 있는 기회를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-145">Like the network upload process, Office 365 then analyzes the data in the PST files and gives you an opportunity to set filters that control what data actually gets imported to the mailboxes specified in the PST import mapping file.</span></span>
    
    - <span data-ttu-id="c3bfb-146">Microsoft는 하드 드라이브를 사용자에 게 다시 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-146">Microsoft ships the hard drive back to you.</span></span> 
    
5. <span data-ttu-id="c3bfb-p114">**사서함으로 가져올 pst 데이터** -가져오기 작업을 만든 후에, 즉 드라이브 전달 작업에서 pst 파일을 Azure 저장 위치로 업로드 한 후에는 Office 365에서 pst 파일의 데이터를 안전 하 고 안전 하 게 분석 합니다. 항목의 보존 기간 및 PST 파일에 포함 된 다양 한 메시지 유형을 식별 합니다. 분석이 완료 되 고 데이터를 가져올 준비가 되 면 PST 파일에 포함 된 모든 데이터를 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하 여 가져온 데이터를 트리밍하는 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p114">**Filter the PST data that will be imported to mailboxes** - After the import job is created (and after the PST files from a drive shipping job are uploaded to the Azure storage location) Office 365 analyzes the data in the PST files (safely and securely) by identifying the age of the items and the different message types included in the PST files. When the analysis is completed and the data is ready to import, you have the option to import all the data contained in the PST files or you can trim the data that's imported by setting filters that control what data gets imported.</span></span> 
    
6. <span data-ttu-id="c3bfb-p115">**pst 가져오기 작업 시작** -가져오기 작업을 시작한 후에 Office 365은 pst 가져오기 매핑 파일의 정보를 사용 하 여 Azure 저장소 위치에서 사용자 사서함으로 pst 파일을 가져옵니다. 가져오기 작업에 대 한 상태 정보 (가져올 각 PST 파일에 대 한 정보 포함)는 보안 \*\*\*\* &amp; 및 준수 센터의 가져오기 페이지에 표시 됩니다. 가져오기 작업이 완료 되 면 작업 상태가 **완료**로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p115">**Start the PST import job** - After the import job is started, Office 365 uses the information in the PST import mapping file to import the PSTs files from the he Azure storage location to user mailboxes. Status information about the import job (including information about each PST file being imported) is displayed on the **Import** page in the Security &amp; Compliance Center. When the import job is finished, the status for the job is set to **Complete**.</span></span>
  
## <a name="why-import-email-data-to-office-365"></a><span data-ttu-id="c3bfb-152">전자 메일 데이터를 Office 365로 가져오는 이유는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="c3bfb-152">Why import email data to Office 365?</span></span>

- <span data-ttu-id="c3bfb-153">PST 파일을 사용자 사서함으로 가져오는 것은 조직의 전자 메일을 Office 365로 마이그레이션하는 한 가지 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-153">Importing PST files to user mailboxes is one way to migrate your organization's email to Office 365.</span></span>
    
- <span data-ttu-id="c3bfb-p116">[지능형 가져오기](filter-data-when-importing-pst-files.md) 기능을 사용 하 여 실제로 대상 사서함으로 가져온 PST 파일의 항목을 필터링 할 수 있습니다. 이렇게 하면 가져올 데이터를 제어 하는 필터를 설정 하 여 가져온 데이터를 트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p116">You can use the [Intelligent Import](filter-data-when-importing-pst-files.md) feature to filter the items in PST files that actually get imported to the target mailboxes. This lets you trim the data that's imported by setting filters that control what data gets imported.</span></span> 
    
- <span data-ttu-id="c3bfb-156">전자 메일 데이터를 Office 365로 가져오면 조직의 준수 요구 사항에 따라 다음과 같은 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-156">Importing email data to Office 365 helps address compliance needs of your organization by letting you:</span></span>
    
  - <span data-ttu-id="c3bfb-157">[보관 사서함](enable-archive-mailboxes.md) 및 [무제한 보관](unlimited-archiving.md) 을 사용 하도록 설정 하 여 사용자에 게 사서함 저장소 공간을 추가로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-157">Enable [archive mailboxes](enable-archive-mailboxes.md) and [unlimited archiving](unlimited-archiving.md) to give users additional mailbox storage space.</span></span> 
    
  - <span data-ttu-id="c3bfb-158">콘텐츠를 보존 하려면 사서함을 [소송 보존 상태로](https://go.microsoft.com/fwlink/?linkid=841243) 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-158">Place mailboxes on [Litigation Hold](https://go.microsoft.com/fwlink/?linkid=841243) to retain content.</span></span> 
    
  - <span data-ttu-id="c3bfb-159">[콘텐츠 검색 도구](content-search.md) 를 사용 하 여 사서함 콘텐츠를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-159">Use the [Content Search tool](content-search.md) to search for mailbox content.</span></span> 
    
  - <span data-ttu-id="c3bfb-160">[eDiscovery 사례](ediscovery-cases.md) 를 사용 하 여 조직의 법적 조사 관리</span><span class="sxs-lookup"><span data-stu-id="c3bfb-160">Use [eDiscovery cases](ediscovery-cases.md) to mange your organization's legal investigations</span></span> 
    
  - <span data-ttu-id="c3bfb-161">보안 &amp; 및 준수 센터에서 [보존 정책을](retention-policies.md) 사용 하 여 사서함 콘텐츠가 보존 되는 기간을 제어 하 고 보존 기간이 만료 된 후에 콘텐츠를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-161">Use [retention policies](retention-policies.md) in the Security &amp; Compliance Center to control how long mailbox content is retained, and then delete content after the retention period expires.</span></span> 
    
- <span data-ttu-id="c3bfb-p117">데이터를 Office 365로 가져오면 데이터 손실을 방지할 수 있습니다. Office 365로 가져오는 전자 메일 데이터는 Exchange Online의 고가용성 기능을 상속 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p117">Importing data to Office 365 helps protect against data loss. Email data that's imported to Office 365 inherits the high availability features of Exchange Online.</span></span>
    
- <span data-ttu-id="c3bfb-164">Office 365의 전자 메일 데이터는 클라우드에 저장 되므로 모든 장치에서 사용자에 게 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-164">Email data in Office 365 is available to users from all devices because it's stored in the cloud.</span></span>
    
## <a name="importing-sharepoint-data-to-office-365"></a><span data-ttu-id="c3bfb-165">Office 365로 SharePoint 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3bfb-165">Importing SharePoint data to Office 365</span></span>

<span data-ttu-id="c3bfb-p118">Office 365 조 직에서 SharePoint 사이트 및 OneDrive 계정으로 파일 및 문서를 가져올 수도 있습니다. 자세한 내용은 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p118">You can also import files and documents to SharePoint sites and OneDrive accounts in your Office 365 organization. For more information, see the following articles:</span></span>

- [<span data-ttu-id="c3bfb-168">SharePoint Online으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="c3bfb-168">Migrate to SharePoint Online</span></span>](https://docs.microsoft.com/sharepointmigration/migrate-to-sharepoint-online)

- [<span data-ttu-id="c3bfb-169">SharePoint 마이그레이션 도구 소개</span><span class="sxs-lookup"><span data-stu-id="c3bfb-169">Introducing the SharePoint Migration Tool</span></span>](https://docs.microsoft.com/sharepointmigration/introducing-the-sharepoint-migration-tool)

- [<span data-ttu-id="c3bfb-170">PowerShell을 사용하여 SharePoint Online으로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="c3bfb-170">Migrate to SharePoint Online using PowerShell</span></span>](https://docs.microsoft.com/sharepointmigration/overview-spmt-ps-cmdlets)

- [<span data-ttu-id="c3bfb-171">Azure Data Box를 사용 하 여 SharePoint Online으로 파일 공유 콘텐츠 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="c3bfb-171">Migrate your file share content to SharePoint Online using the Azure Data Box</span></span>](https://docs.microsoft.com/sharepointmigration/how-to-migrate-file-share-content-to-spo-using-azuredatabox)


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a><span data-ttu-id="c3bfb-172">PST 파일을 Office 365로 가져오는 방법에 대 한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="c3bfb-172">Frequently asked questions about importing PST files to Office 365</span></span>
  
<span data-ttu-id="c3bfb-173">다음은 office 365 가져오기 서비스를 사용 하 여 PST 파일을 office 365 사서함으로 대량으로 가져오는 방법에 대 한 몇 가지 질문과 대답입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-173">Here are some frequently asked questions about using the Office 365 Import service to bulk-import PST files to Office 365 mailboxes.</span></span> 
  
- [<span data-ttu-id="c3bfb-174">네트워크 업로드를 사용 하 여 PST 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3bfb-174">Using network upload to import PST files</span></span>](#using-network-upload-to-import-pst-files)
  
- [<span data-ttu-id="c3bfb-175">드라이브 전달을 사용 하 여 PST 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3bfb-175">Using drive shipping to import PST files</span></span>](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a><span data-ttu-id="c3bfb-176">네트워크 업로드를 사용 하 여 PST 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3bfb-176">Using network upload to import PST files</span></span>

 <span data-ttu-id="c3bfb-177">**Office 365 가져오기 서비스에서 가져오기 작업을 만드는 데 필요한 사용 권한은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-177">**What permissions are required to create import jobs in the Office 365 Import Service?**</span></span>
  
<span data-ttu-id="c3bfb-p119">PST 파일을 Office 365 사서함으로 가져오려면 Exchange Online의 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 자신 또는 다른 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p119">You have to be assigned the Mailbox Import Export role in Exchange Online to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
  
<span data-ttu-id="c3bfb-183">또한 Office 365 보안 &amp; 및 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-183">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
  
- <span data-ttu-id="c3bfb-p120">Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p120">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="c3bfb-186">또는</span><span class="sxs-lookup"><span data-stu-id="c3bfb-186">Or</span></span>
    
- <span data-ttu-id="c3bfb-187">Office 365 조 직의 전역 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-187">You have to be a global administrator in your Office 365 organization.</span></span>
    
> [!TIP]
> <span data-ttu-id="c3bfb-p121">Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p121">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
 <span data-ttu-id="c3bfb-190">**네트워크 업로드를 사용할 수 있는 위치**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-190">**Where is network upload available?**</span></span>
  
<span data-ttu-id="c3bfb-p122">네트워크 업로드는 현재 미국, 캐나다, 브라질, 영국, 유럽, 인도, 동부 아시아, 동남 아시아, 일본, 한국, 호주 및 오스트레일리아에서 사용할 수 있습니다. 네트워크 업로드가 곧 더 많은 지역에서 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p122">Network upload is currently available in the United States, Canada, Brazil, the United Kingdom, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Network upload will be available in more regions soon.</span></span>
  
 <span data-ttu-id="c3bfb-193">**네트워크 업로드를 사용 하 여 PST 파일을 가져오기 위한 가격은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-193">**What is the pricing for importing PST files by using network upload?**</span></span>
  
<span data-ttu-id="c3bfb-194">네트워크 업로드를 사용 하 여 PST 파일을 가져오는 것은 무료입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-194">Using network upload to import PST files is free.</span></span>
  
<span data-ttu-id="c3bfb-p123">또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 Office 365 관리 센터의 완료 된 가져오기 작업에 대 한 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 **Office로 데이터 가져오기 365** 페이지에 표시 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p123">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Office 365 admin center. Although an import job might still be listed on the **Import data to Office 365** page, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="c3bfb-197">**Office 365로 가져올 때 지원 되는 PST 파일 형식의 버전은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-197">**What version of the PST file format is supported for importing to Office 365?**</span></span>
  
<span data-ttu-id="c3bfb-p124">PST 파일 형식에는 ANSI 및 Unicode의 두 가지 버전이 있습니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 DBCS (더블 바이트 문자 집합)를 사용 하는 언어와 같이 ANSI PST 파일 형식을 사용 하는 파일은 Office 365로도 가져올 수 있습니다. ANSI PST 파일을 가져오는 방법에 대 한 자세한 내용은 네트워크 업로드 사용의 4 단계에서 [PST 파일을 Office 365로 가져오기](https://go.microsoft.com/fwlink/p/?LinkId=823074)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p124">There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. However, files that use the ANSI PST file format, such as those for languages that use a double-byte character set (DBCS), can also be imported to Office 365. For more information about importing ANSI PST files, see Step 4 in [Use network upload to import PST files to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=823074).</span></span>
  
<span data-ttu-id="c3bfb-202">또한 Outlook 2007 이상 버전의 PST 파일을 Office 365로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-202">Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.</span></span>
  
 <span data-ttu-id="c3bfb-203">**azure storage 영역에 내 PST 파일을 업로드 한 후 삭제 하기 전에 azure에 보관 되는 기간**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-203">**After I upload my PST files to the Azure storage area, how long are they kept in Azure before they're deleted?**</span></span>
  
<span data-ttu-id="c3bfb-p125">네트워크 업로드 방법을 사용 하 여 PST 파일을 가져올 때는 **ingestiondata**이라는 Azure blob 컨테이너에 업로드 합니다. 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서 가져오기 작업이 진행 중이 아니면 Azure의 **ingestiondata** 컨테이너에 있는 모든 PST 파일이 보안 &amp;준수 센터 또한 PST 파일을 Azure에 업로드 하는 30 일 이내에 보안 &amp; 및 준수 센터 (네트워크 업로드 지침의 5 단계에 설명 됨)에서 새 가져오기 작업을 만들어야 한다는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p125">When you use the network upload method to import PST files, you upload them to an Azure blob container named **ingestiondata**. If there are no import jobs in progress on the **Import** page in the Security &amp; Compliance Center), then all PST files in the **ingestiondata** container in Azure are deleted 30 days after the most recent import job was created in the Security &amp; Compliance Center. That also means you have to create a new import job in the Security &amp; Compliance Center (described in Step 5 in the network upload instructions) within 30 days of uploading PST files to Azure.</span></span> 
  
<span data-ttu-id="c3bfb-p126">또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 보안 &amp; 및 준수 센터에서 완료 된 가져오기 작업의 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 보안 &amp; 준수 센터의 **가져오기** 페이지에 나열 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p126">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Security &amp; Compliance Center. Although an import job might still be listed on the **Import** page in the Security &amp; Compliance Center, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="c3bfb-209">**PST 파일을 사서함에 가져오는 데 소요 되는 시간**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-209">**How long does it take to import a PST file to a mailbox?**</span></span>
  
<span data-ttu-id="c3bfb-p127">네트워크 용량에 따라 다르지만 일반적으로 각 테라바이트 (tb)의 데이터를 조직의 Azure storage 영역에 업로드 하는 데 몇 시간 정도 걸립니다. pst 파일이 Azure storage 영역에 복사 된 후에는 pst 파일을 하루 중 24gb 이상으로 Office 365 사서함으로 가져옵니다. 이 속도가 사용자의 요구를 충족 하지 않는 경우 전자 메일 데이터를 Office 365로 마이그레이션하는 다른 방법을 고려할 수 있습니다. 자세한 내용은 [여러 전자 메일 계정을 Office 365로 마이그레이션하는 방법을](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p127">It depends on the capacity of your network, but it typically takes several hours for each terabyte (TB) of data to be uploaded to the Azure storage area for your organization. After the PST files are copied to the Azure storage area, a PST file is imported to an Office 365 mailbox at a rate of at least 24 GB per day. If this rate doesn't meet your needs, you might consider other methods for migrating email data to Office 365. For more information, see [Ways to migrate multiple email accounts to Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).</span></span>
  
<span data-ttu-id="c3bfb-p128">서로 다른 PST 파일을 다른 대상 사서함으로 가져오는 경우 가져오기 프로세스는 동시에 수행 됩니다. 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로 여러 PST 파일을 같은 사서함으로 가져오는 경우 동시에 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p128">If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Likewise, if multiple PST files are imported to the same mailbox, they will be simultaneously imported.</span></span>
  
 <span data-ttu-id="c3bfb-216">**PST 파일을 가져올 때 메시지 크기 제한이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-216">**Is there a message size limit when importing PST files?**</span></span>
  
<span data-ttu-id="c3bfb-p129">예로. PST 파일에 150 보다 큰 사서함 항목이 포함 되어 있으면 가져오기 프로세스 중에 해당 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p129">Yes. If a PST file contains a mailbox item that is larger than 150 MB, the item will be skipped during the import process.</span></span>
  
 <span data-ttu-id="c3bfb-219">**메시지를 보내거나 받은 경우와 같이 PST 파일을 Office 365 사서함으로 가져올 때 받는 사람 및 기타 속성 목록이 보존 되는 메시지 속성입니다.**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-219">**Are message properties, such as when the message was sent or received, the list of recipients and other properties, preserved when PST files are imported to an Office 365 mailbox?**</span></span>
  
<span data-ttu-id="c3bfb-p130">예로. 원본 메시지 메타 데이터는 가져오기 프로세스 중에 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p130">Yes. The original message metadata isn't changed during the import process.</span></span>
  
 <span data-ttu-id="c3bfb-222">**사서함으로 가져오려는 PST 파일에 대 한 폴더 계층 구조의 수준 수에 제한이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-222">**Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**</span></span>
  
<span data-ttu-id="c3bfb-p131">예로. 300 개 이상의 중첩 된 폴더를 포함 하는 PST 파일은 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p131">Yes. You can't import a PST file that has 300 or more levels of nested folders.</span></span>
  
 <span data-ttu-id="c3bfb-225">**네트워크 업로드를 사용 하 여 PST 파일을 Office 365의 비활성 사서함으로 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-225">**Can I use network upload to import PST files to an inactive mailbox in Office 365?**</span></span>
  
<span data-ttu-id="c3bfb-226">예, 이제이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-226">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="c3bfb-227">**네트워크 업로드를 사용 하 여 Exchange 하이브리드 배포의 온라인 보관 사서함으로 PST 파일을 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-227">**Can I use network upload to import PST files to an online archive mailbox in an Exchange hybrid deployment?**</span></span>
  
<span data-ttu-id="c3bfb-228">예, 이제이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-228">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="c3bfb-229">**네트워크 업로드를 사용 하 여 PST 파일을 Exchange Online의 공용 폴더에 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-229">**Can I use network upload to import PST files to public folders in Exchange Online?**</span></span>
  
<span data-ttu-id="c3bfb-230">아니요, PST 파일을 공용 폴더로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-230">No, you can't import PST files to public folders.</span></span>
  
### <a name="using-drive-shipping-to-import-pst-files"></a><span data-ttu-id="c3bfb-231">드라이브 전달을 사용 하 여 PST 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3bfb-231">Using drive shipping to import PST files</span></span>

 <span data-ttu-id="c3bfb-232">**Office 365 가져오기 서비스에서 가져오기 작업을 만드는 데 필요한 사용 권한은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-232">**What permissions are required to create import jobs in the Office 365 Import Service?**</span></span>
  
<span data-ttu-id="c3bfb-p132">PST 파일을 Office 365 사서함으로 가져오려면 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 자신 또는 다른 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p132">You have to be assigned the Mailbox Import Export role to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
  
<span data-ttu-id="c3bfb-238">또한 Office 365 보안 &amp; 및 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-238">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
  
- <span data-ttu-id="c3bfb-p133">Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p133">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="c3bfb-241">또는</span><span class="sxs-lookup"><span data-stu-id="c3bfb-241">Or</span></span>
    
- <span data-ttu-id="c3bfb-242">Office 365 조 직의 전역 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-242">You have to be a global administrator in your Office 365 organization.</span></span>
    
> [!TIP]
> <span data-ttu-id="c3bfb-p134">Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p134">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
 <span data-ttu-id="c3bfb-245">**드라이브 배송을 사용할 수 있는 위치**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-245">**Where is drive shipping available?**</span></span>
  
<span data-ttu-id="c3bfb-p135">드라이브 전달은 미국, 캐나다, 브라질, 영국, 유럽, 인도, 동부 아시아, 동남 아시아, 일본, 한국, 호주, 오스트레일리아 이제 더 많은 지역에서 드라이브 전달을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p135">Drive shipping is currently available in the United States, Canada, Brazil, the United Kingdom, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Drive shipping will be available in more regions soon.</span></span>
  
 <span data-ttu-id="c3bfb-248">**드라이브 전달을 지 원하는 상업적 라이선스 계약은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-248">**What commercial licensing agreements support drive shipping?**</span></span>
  
<span data-ttu-id="c3bfb-p136">Office 365로 PST 파일을 가져오기 위한 드라이브 전달은 EA (Microsoft 엔터프라이즈 계약)를 통해 제공 됩니다. Microsoft 제품 및 서비스 계약 (mpsa)을 통해서는 드라이브 전달을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p136">Drive shipping to import PST files to Office 365 is available through a Microsoft Enterprise Agreement (EA). Drive shipping isn't available through a Microsoft Products and Services Agreement (MPSA).</span></span>
  
 <span data-ttu-id="c3bfb-251">**드라이브 전달을 사용 하 여 PST 파일을 Office 365로 가져올 때의 가격은 얼마 인가요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-251">**What is the pricing for using drive shipping to import PST files to Office 365?**</span></span>
  
<span data-ttu-id="c3bfb-p137">드라이브 전달을 사용 하 여 PST 파일을 Office 365 사서함으로 가져오는 비용은 데이터의 GB 당 $2 USD입니다. 예를 들어, 1000 기가바이트 (1tb)의 PST 파일을 포함 하는 하드 드라이브를 제공 하는 경우 비용은 $2000 USD입니다. 파트너와 협력 하 여 가져오기 비용을 지불 해 볼 수 있습니다. 파트너를 찾는 방법에 대 한 자세한 내용은 [Office 365 파트너 또는 대리점 찾기를](https://go.microsoft.com/fwlink/p/?LinkId=785197)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p137">The cost to use drive shipping to import PST files to Office 365 mailboxes is $2 USD per GB of data. For example, if you ship a hard drive that contains 1,000 GB (1 TB) of PST files, the cost is $2,000 USD. You can work with a partner to pay the import fee. For information about finding a partner, see [Find your Office 365 partner or reseller](https://go.microsoft.com/fwlink/p/?LinkId=785197).</span></span>
  
 <span data-ttu-id="c3bfb-256">**드라이브 전달에 대해 지원 되는 하드 드라이브 종류는 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-256">**What kind of hard drives are supported for drive shipping?**</span></span>
  
<span data-ttu-id="c3bfb-p138">Office 365 가져오기 서비스와 함께 사용할 경우에는 2.5 인치 ssd (고체 드라이브) 또는 2.5 또는 3.5 인치 SATA II/III 내부 하드 드라이브만 지원 됩니다. 하드 드라이브는 최대 10mb까지 사용할 수 있습니다. 가져오기 작업의 경우에는 하드 드라이브의 첫 번째 데이터 볼륨만 처리 됩니다. 데이터 볼륨은 NTFS로 포맷 해야 합니다. 데이터를 하드 드라이브에 복사 하는 경우, 2.5 인치 ssd 또는 2.5 또는 3.5 인치 sata ii/iii 커넥터를 사용 하 여 직접 연결 하거나 외부 2.5 cm SSD 또는 2.5 또는 3.5 인치 sata ii/iii USB 어댑터를 사용 하 여 외부에서 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p138">Only 2.5 inch solid-state drives (SSDs) or 2.5 or 3.5 inch SATA II/III internal hard drives are supported for use with the Office 365 Import service. You can use hard drives up to 10 TB. For import jobs, only the first data volume on the hard drive will be processed. The data volume must be formatted with NTFS. When copying data to a hard drive, you can attach it directly using a 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III connector or you can attach it externally using an external 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III USB adaptor.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c3bfb-p139">기본 제공 USB 어댑터와 함께 제공 되는 외부 하드 드라이브는 Office 365 가져오기 서비스에서 지원 되지 않습니다. 또한 외부 하드 드라이브 대/소문자 내의 디스크는 사용할 수 없습니다. 외부 하드 드라이브를 배송 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p139">External hard drives that come with an built-in USB adaptor aren't supported by the Office 365 Import service. Additionally, the disk inside the casing of an external hard drive can't be used. Please don't ship external hard drives.</span></span> 
  
 <span data-ttu-id="c3bfb-265">**단일 가져오기 작업에 사용할 수 있는 하드 드라이브는 몇 개입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-265">**How many hard drives can I ship for a single import job?**</span></span>
  
<span data-ttu-id="c3bfb-266">단일 가져오기 작업에 최대 10 개의 하드 드라이브를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-266">You can ship a maximum of 10 hard drives for a single import job.</span></span>
  
 <span data-ttu-id="c3bfb-267">**하드 드라이브를 배송 하 고 나 서 Microsoft 데이터 센터에 액세스 하는 데 어느 정도의 시간이 걸립니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-267">**After I ship my hard drive, how long does it take to get to the Microsoft data center?**</span></span>
  
<span data-ttu-id="c3bfb-p140">Microsoft 데이터 센터와 같이 하드 드라이브를 제공 하는 데 사용 하는 배송 옵션 (예:, 다음 영업일 배송, 2 일 배송 또는 지상 배달)과 같은 몇 가지 사항에 따라 달라 집니다. 대부분의 운송 업체에서는 추적 번호를 사용 하 여 배달 상태를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p140">That depends on a few things, such as your proximity to the Microsoft data center and what kind of shipping option you used to ship your hard drive (such as, next-day delivery, two-day delivery, or ground-delivery). With most shippers, you can use the tracking number to track the status of your delivery.</span></span>
  
 <span data-ttu-id="c3bfb-270">**Microsoft 데이터 센터에 하드 드라이브가 도착 한 후 Azure에 내 PST 파일을 업로드 하는 데 얼마나 걸립니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-270">**After my hard drive arrives at the Microsoft data center, how long does it take to upload my PST files to Azure?**</span></span>
  
<span data-ttu-id="c3bfb-p141">microsoft 데이터 센터에서 하드 드라이브를 받은 후에는 해당 조직의 microsoft Azure storage 영역에 PST 파일을 업로드 하기 위해 7 일에서 10 일까 지를 담당 합니다. PST 파일이 라는 `ingestiondata`Azure blob 컨테이너에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p141">After your hard drive is received at the Microsoft data center, it will take between 7 to 10 business days to upload the PST files to the Microsoft Azure storage area for your organization. The PST files will be uploaded to a Azure blob container named `ingestiondata`.</span></span> 
  
 <span data-ttu-id="c3bfb-273">**PST 파일을 사서함에 가져오는 데 소요 되는 시간**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-273">**How long does it take to import a PST file to a mailbox?**</span></span>
  
<span data-ttu-id="c3bfb-p142">pst 파일이 Azure storage 영역에 업로드 된 후에 Office 365는 pst 파일의 데이터를 안전 하 고 안전한 방식으로 분석 하 여 항목의 보존 기간 및 pst 파일에 포함 된 다양 한 메시지 유형을 식별 합니다. 이 분석이 완료 되 면 PST 파일의 모든 데이터를 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하는 옵션을 사용할 수 있습니다. 가져오기 작업을 시작한 후에는 PST 파일을 하루 중 24gb 이상으로 Office 365 사서함으로 가져옵니다. 이 속도가 사용자의 요구를 충족 하지 않는 경우 전자 메일 데이터를 Office 365로 가져오는 다른 방법을 고려할 수 있습니다. 자세한 내용은 [여러 전자 메일 계정을 Office 365로 마이그레이션하는 방법을](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p142">After the PST files are uploaded to the Azure storage area, Office 365 analyzes the data in the PST files (in a safe and secure manner) to identify the age of the items and the different message types included in the PST files. When this analysis is complete, you'll have the option to import all the data in the PST files or set filters to that control what data gets imported. After you start the import job, a PST file is imported to an Office 365 mailbox at a rate of at least 24 GB per day. If this rate doesn't meet your needs, you might consider other methods for importing email data to Office 365. For more information, see [Ways to migrate multiple email accounts to Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).</span></span>
  
<span data-ttu-id="c3bfb-p143">서로 다른 PST 파일을 다른 대상 사서함으로 가져오는 경우 가져오기 프로세스는 동시에 수행 됩니다. 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로 여러 PST 파일을 같은 사서함으로 가져오는 경우 동시에 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p143">If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Likewise, if multiple PST files are imported to the same mailbox, they will be simultaneously imported.</span></span>
  
 <span data-ttu-id="c3bfb-281">**Microsoft에서 내 PST 파일을 azure로 업로드 한 후 삭제 하기 전에 azure에 보관 되는 기간**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-281">**After Microsoft uploads my PST files to Azure, how long are they kept in Azure before they're deleted?**</span></span>
  
<span data-ttu-id="c3bfb-282">조직의 Azure 저장소 위치에 있는 모든 PST 파일 (blob 컨테이너 `ingestiondata`)에서 최근 가져오기 작업은 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서 만든 후 30 일이 지나면 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-282">All PST files in the Azure storage location for your organization (in blob container named `ingestiondata`), are deleted 30 days after the most recent import job was created on the **Import** page in the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="c3bfb-p144">또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 보안 &amp; 및 준수 센터에서 완료 된 가져오기 작업의 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 보안 &amp; 준수 센터의 **가져오기** 페이지에 나열 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p144">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Security &amp; Compliance Center. Although an import job might still be listed on the **Import** page in the Security &amp; Compliance Center, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="c3bfb-285">**Office 365로 가져올 때 지원 되는 PST 파일 형식의 버전은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-285">**What version of the PST file format is supported for importing to Office 365?**</span></span>
  
<span data-ttu-id="c3bfb-p145">PST 파일 형식에는 ANSI 및 Unicode의 두 가지 버전이 있습니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 DBCS (더블 바이트 문자 집합)를 사용 하는 언어와 같이 ANSI PST 파일 형식을 사용 하는 파일은 Office 365로도 가져올 수 있습니다. ANSI PST 파일 가져오기에 대 한 자세한 내용은 on [drive 발송을 사용 하 여 조직 PST 파일을 Office 365로 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file)의 3 단계를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p145">There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. However, files that use the ANSI PST file format, such as those for languages that use a double-byte character set (DBCS), can also be imported to Office 365. For more information about importing ANSI PST files, see Step 3 in [Use drive shipping to import your organization PST files to Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).</span></span>
  
<span data-ttu-id="c3bfb-290">또한 Outlook 2007 이상 버전의 PST 파일을 Office 365로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-290">Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.</span></span>
  
 <span data-ttu-id="c3bfb-291">**PST 파일을 가져올 때 메시지 크기 제한이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-291">**Is there a message size limit when importing PST files?**</span></span>
  
<span data-ttu-id="c3bfb-p146">예로. PST 파일에 150 보다 큰 사서함 항목이 포함 되어 있으면 가져오기 프로세스 중에 해당 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p146">Yes. If a PST file contains a mailbox item that is larger than 150 MB, the item will be skipped during the import process.</span></span>
  
 <span data-ttu-id="c3bfb-294">**메시지를 보내거나 받은 경우와 같이 PST 파일을 Office 365 사서함으로 가져올 때 받는 사람 및 기타 속성 목록이 보존 되는 메시지 속성입니다.**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-294">**Are message properties, such as when the message was sent or received, the list of recipients and other properties, preserved when PST files are imported to an Office 365 mailbox?**</span></span>
  
<span data-ttu-id="c3bfb-p147">예로. 원본 메시지 메타 데이터는 가져오기 프로세스 중에 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p147">Yes. The original message metadata isn't changed during the import process</span></span>
  
 <span data-ttu-id="c3bfb-297">**사서함으로 가져오려는 PST 파일에 대 한 폴더 계층 구조의 수준 수에 제한이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-297">**Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**</span></span>
  
<span data-ttu-id="c3bfb-p148">예로. 300 개 이상의 중첩 된 폴더를 포함 하는 PST 파일은 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p148">Yes. You can't import a PST file that has 300 or more levels of nested folders.</span></span>
  
 <span data-ttu-id="c3bfb-300">**Office 365에서 드라이브 전달을 사용 하 여 PST 파일을 비활성 사서함으로 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-300">**Can I use drive shipping to import PST files to an inactive mailbox in Office 365?**</span></span>
  
<span data-ttu-id="c3bfb-301">예, 이제이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-301">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="c3bfb-302">**드라이브 전달을 사용 하 여 PST 파일을 Exchange 하이브리드 배포의 온라인 보관 사서함으로 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-302">**Can I use drive shipping to import PST files to an online archive mailbox in an Exchange hybrid deployment?**</span></span>
  
<span data-ttu-id="c3bfb-303">예, 이제이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-303">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="c3bfb-304">**드라이브 전달을 사용 하 여 PST 파일을 Exchange Online의 공용 폴더로 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-304">**Can I use drive shipping to import PST files to public folders in Exchange Online?**</span></span>
  
<span data-ttu-id="c3bfb-305">아니요, PST 파일을 공용 폴더로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-305">No, you can't import PST files to public folders.</span></span>
  
 <span data-ttu-id="c3bfb-306">**Microsoft에서 내 하드 드라이브를 초기화 한 후에 다시 출하 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-306">**Can Microsoft wipe my hard drive before they ship it back to me?**</span></span>
  
<span data-ttu-id="c3bfb-p149">아니요, Microsoft는 고객에 게 다시 배송 하기 전에 하드 드라이브를 제거할 수 없습니다. 하드 드라이브를 Microsoft에서 받은 것과 같은 상태로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p149">No, Microsoft can't wipe hard drives before shipping them back to customers. Hard drives are returned to you in the same state they were in when they were received by Microsoft.</span></span>
  
 <span data-ttu-id="c3bfb-309">**Microsoft에서 내 하드 드라이브를 다시 배송 하지 않고 shred 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-309">**Can Microsoft shred my hard drive instead of shipping it back to me?**</span></span>
  
<span data-ttu-id="c3bfb-p150">아니요, Microsoft에서 하드 드라이브를 삭제할 수 없습니다. 하드 드라이브를 Microsoft에서 받은 것과 같은 상태로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p150">No, Microsoft can't destroy your hard drive. Hard drives are returned to you in the same state they were in when they were received by Microsoft.</span></span>
  
 <span data-ttu-id="c3bfb-312">**반품 상품을 위해 지원 되는 courier services는 무엇 인가요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-312">**What courier services are supported for return shipping?**</span></span>
  
<span data-ttu-id="c3bfb-p151">미국 또는 유럽의 고객 인 경우 Microsoft는 FedEx을 사용 하 여 하드 드라이브를 반환 합니다. 다른 모든 지역에 대해 Microsoft는 DHL를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p151">If you're a customer in the United States or Europe, Microsoft uses FedEx to return your hard drive. For all other regions, Microsoft uses DHL.</span></span>
  
 <span data-ttu-id="c3bfb-315">**반품 배송 비용은 얼마 입니까?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-315">**What are the return shipping costs?**</span></span>
  
<span data-ttu-id="c3bfb-p152">반품 비용은 하드 드라이브를 전달한 Microsoft 데이터 센터에 따라 달라 집니다. Microsoft는 하드 드라이브를 반환 하기 위해 FedEx 또는 DHL 계정을 청구할 것입니다. 반품 비용은 귀하의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p152">Return shipping costs vary, depending on your proximity to the Microsoft data center that you shipped your hard drive to. Microsoft will bill your FedEx or DHL account to return your hard drive. The cost of return shipping is your responsibility.</span></span>
  
 <span data-ttu-id="c3bfb-319">**FedEx 사용자 지정 운송과 같은 사용자 지정 courier 선적 서비스를 사용 하 여 Microsoft에 하드 드라이브를 제공할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-319">**Can I use a custom courier shipping service, such as FedEx Custom Shipping, to ship my hard drive to Microsoft?**</span></span>
  
<span data-ttu-id="c3bfb-320">예.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-320">Yes.</span></span>
  
 <span data-ttu-id="c3bfb-321">**하드 드라이브를 다른 국가로 배송 해야 하는 경우에는 필요한 모든 작업을 수행 해야 하나요?**</span><span class="sxs-lookup"><span data-stu-id="c3bfb-321">**If I have to ship my hard drive to another country, is there anything I need to do?**</span></span>
  
<span data-ttu-id="c3bfb-p153">Microsoft에 제공 하는 하드 드라이브는 해외 테두리를 교차 해야 할 수도 있습니다. 이 경우 해당 하는 법률에 따라 하드 드라이브와 해당 파일에 포함 된 데이터를 가져오고/또는 내보내도록 합니다. 하드 드라이브를 출시 하기 전에 관리자에 게 문의 하 여 드라이브 및 데이터가 지정 된 Microsoft 데이터 센터로 합법적으로 전달 될 수 있는지 확인 합니다. 이렇게 하면 Microsoft에 적시에 도달 하는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3bfb-p153">The hard drive that you ship to Microsoft might have to cross international borders. If this is the case, you're responsible for ensuring that the hard drive and the data it contains are imported and/or exported in accordance with the applicable laws. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the specified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.</span></span>
