---
title: PST 파일을 Office 365로 가져오기에 대 한 FAQ
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 2fe71b05-f5a2-4182-ade7-4dc5cabdfd51
description: 'office 365 가져오기 서비스를 사용 하 여 office 365 사서함으로 organizaiton의 PST 파일을 가져오는 관리자에 대 한 질문과 대답을 자주 묻는 질문입니다. '
ms.openlocfilehash: 9ca2e206a1d06c1398181c51e41b4dc68d8d965c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218408"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a><span data-ttu-id="ebcf6-103">PST 파일을 Office 365로 가져오기에 대 한 FAQ</span><span class="sxs-lookup"><span data-stu-id="ebcf6-103">FAQ about importing PST files to Office 365</span></span>

<span data-ttu-id="ebcf6-104">**이 문서는 관리자를 위한 것입니다. PST 파일을 자체 사서함으로 가져오시겠습니까? [Outlook .pst 파일에서 전자 메일, 연락처 및 일정 가져오기를](https://go.microsoft.com/fwlink/p/?LinkID=785075) 참조 하세요.**|</span><span class="sxs-lookup"><span data-stu-id="ebcf6-104">**This article is for administrators. Do you want to import PST files to your own mailbox? See [Import email, contacts, and calendar from an Outlook .pst file](https://go.microsoft.com/fwlink/p/?LinkID=785075)**|</span></span>
   
<span data-ttu-id="ebcf6-p101">다음은 office 365 가져오기 서비스를 사용 하 여 PST 파일을 office 365 사서함으로 대량으로 가져오는 방법에 대 한 몇 가지 질문과 대답입니다. pst 파일을 가져오는 방법에 대 한 자세한 내용은 [pst 파일을 Office 365로 가져오기 개요](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p101">Here are some frequently asked questions about using the Office 365 Import Service to bulk-import PST files to Office 365 mailboxes. For more information about how to import PST files, see [Overview of importing PST files to Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84).</span></span>
  
## <a name="using-network-upload-to-import-pst-files"></a><span data-ttu-id="ebcf6-107">네트워크 업로드를 사용 하 여 PST 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="ebcf6-107">Using network upload to import PST files</span></span>

<span data-ttu-id="ebcf6-108">단계별 지침은 [네트워크 업로드를 사용 하 여 PST 파일을 Office 365에 가져오기](use-network-upload-to-import-pst-files.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-108">For step-by-step instructions, see [Use network upload to import PST files to Office 365](use-network-upload-to-import-pst-files.md).</span></span>
  
 <span data-ttu-id="ebcf6-109">**Office 365 가져오기 서비스에서 가져오기 작업을 만드는 데 필요한 사용 권한은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-109">**What permissions are required to create import jobs in the Office 365 Import Service?**</span></span>
  
<span data-ttu-id="ebcf6-p102">PST 파일을 Office 365 사서함으로 가져오려면 Exchange Online의 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 자신 또는 다른 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p102">You have to be assigned the Mailbox Import Export role in Exchange Online to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
  
<span data-ttu-id="ebcf6-115">또한 Office 365 보안 &amp; 및 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-115">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
  
- <span data-ttu-id="ebcf6-p103">Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p103">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="ebcf6-118">또는</span><span class="sxs-lookup"><span data-stu-id="ebcf6-118">Or</span></span>
    
- <span data-ttu-id="ebcf6-119">Office 365 조 직의 전역 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-119">You have to be a global administrator in your Office 365 organization.</span></span>
    
> [!TIP]
> <span data-ttu-id="ebcf6-p104">Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p104">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
 <span data-ttu-id="ebcf6-122">**네트워크 업로드를 사용할 수 있는 위치**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-122">**Where is network upload available?**</span></span>
  
<span data-ttu-id="ebcf6-p105">네트워크 업로드는 현재 미국, 캐나다, 브라질, 미국령, 프랑스, 유럽, 인도, 동부 아시아, 동남 아시아, 일본, 미국 및 오스트레일리아에서 사용할 수 있습니다. 네트워크 업로드가 곧 더 많은 지역에서 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p105">Network upload is currently available in the United States, Canada, Brazil, the United Kingdom, France, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Network upload will be available in more regions soon.</span></span>
  
 <span data-ttu-id="ebcf6-125">**네트워크 업로드를 사용 하 여 PST 파일을 가져오기 위한 가격은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-125">**What is the pricing for importing PST files by using network upload?**</span></span>
  
<span data-ttu-id="ebcf6-126">네트워크 업로드를 사용 하 여 PST 파일을 가져오는 것은 무료입니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-126">Using network upload to import PST files is free.</span></span>
  
<span data-ttu-id="ebcf6-p106">또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 Office 365 관리 센터의 완료 된 가져오기 작업에 대 한 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 **Office로 데이터 가져오기 365** 페이지에 표시 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p106">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Office 365 admin center. Although an import job might still be listed on the **Import data to Office 365** page, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="ebcf6-129">**Office 365로 가져올 때 지원 되는 PST 파일 형식의 버전은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-129">**What version of the PST file format is supported for importing to Office 365?**</span></span>
  
<span data-ttu-id="ebcf6-p107">PST 파일 형식에는 ANSI 및 Unicode의 두 가지 버전이 있습니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 DBCS (더블 바이트 문자 집합)를 사용 하는 언어와 같이 ANSI PST 파일 형식을 사용 하는 파일은 Office 365로도 가져올 수 있습니다. ANSI PST 파일 가져오기에 대 한 자세한 내용은 네트워크 업로드 사용의 4 단계에서 [조직의 PST 파일을 Office 365로 가져오기](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p107">There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. However, files that use the ANSI PST file format, such as those for languages that use a double-byte character set (DBCS), can also be imported to Office 365. For more information about importing ANSI PST files, see Step 4 in [Use network upload to import your organization's PST files to Office 365](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file).</span></span>
  
<span data-ttu-id="ebcf6-134">또한 Outlook 2007 이상 버전의 PST 파일을 Office 365로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-134">Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.</span></span>
  
 <span data-ttu-id="ebcf6-135">**azure storage 영역에 내 PST 파일을 업로드 한 후 삭제 하기 전에 azure에 보관 되는 기간**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-135">**After I upload my PST files to the Azure storage area, how long are they kept in Azure before they're deleted?**</span></span>
  
<span data-ttu-id="ebcf6-p108">네트워크 업로드 방법을 사용 하 여 PST 파일을 가져올 때는 **ingestiondata**이라는 Azure blob 컨테이너에 업로드 합니다. 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서 가져오기 작업이 진행 중이 아니면 Azure의 **ingestiondata** 컨테이너에 있는 모든 PST 파일이 보안 &amp;준수 센터 또한 PST 파일을 Azure에 업로드 하는 30 일 이내에 보안 &amp; 및 준수 센터 (네트워크 업로드 지침의 5 단계에 설명 됨)에서 새 가져오기 작업을 만들어야 한다는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p108">When you use the network upload method to import PST files, you upload them to an Azure blob container named **ingestiondata**. If there are no import jobs in progress on the **Import** page in the Security &amp; Compliance Center), then all PST files in the **ingestiondata** container in Azure are deleted 30 days after the most recent import job was created in the Security &amp; Compliance Center. That also means you have to create a new import job in the Security &amp; Compliance Center (described in Step 5 in the network upload instructions) within 30 days of uploading PST files to Azure.</span></span> 
  
<span data-ttu-id="ebcf6-p109">또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 보안 &amp; 및 준수 센터에서 완료 된 가져오기 작업의 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 보안 &amp; 준수 센터의 **가져오기** 페이지에 나열 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p109">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Security &amp; Compliance Center. Although an import job might still be listed on the **Import** page in the Security &amp; Compliance Center, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="ebcf6-141">**PST 파일을 사서함에 가져오는 데 소요 되는 시간**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-141">**How long does it take to import a PST file to a mailbox?**</span></span>
  
<span data-ttu-id="ebcf6-p110">네트워크 용량에 따라 다르지만 일반적으로 각 테라바이트 (tb)의 데이터를 조직의 Azure storage 영역에 업로드 하는 데 몇 시간 정도 걸립니다. pst 파일이 Azure storage 영역에 복사 된 후에는 pst 파일을 하루 중 24gb 이상으로 Office 365 사서함으로 가져옵니다. 이 속도가 사용자의 요구를 충족 하지 않는 경우 전자 메일 데이터를 Office 365로 마이그레이션하는 다른 방법을 고려할 수 있습니다. 자세한 내용은 [여러 전자 메일 계정을 Office 365로 마이그레이션하는 방법을](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p110">It depends on the capacity of your network, but it typically takes several hours for each terabyte (TB) of data to be uploaded to the Azure storage area for your organization. After the PST files are copied to the Azure storage area, a PST file is imported to an Office 365 mailbox at a rate of at least 24 GB per day. If this rate doesn't meet your needs, you might consider other methods for migrating email data to Office 365. For more information, see [Ways to migrate multiple email accounts to Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).</span></span>
  
<span data-ttu-id="ebcf6-p111">서로 다른 PST 파일을 다른 대상 사서함으로 가져오는 경우 가져오기 프로세스는 동시에 수행 됩니다. 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로 여러 PST 파일을 같은 사서함으로 가져오는 경우 동시에 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p111">If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Likewise, if multiple PST files are imported to the same mailbox, they will be simultaneously imported.</span></span>
  
 <span data-ttu-id="ebcf6-148">**PST 파일을 가져올 때 메시지 크기 제한이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-148">**Is there a message size limit when importing PST files?**</span></span>
  
<span data-ttu-id="ebcf6-p112">예로. PST 파일에 150 보다 큰 사서함 항목이 포함 되어 있으면 가져오기 프로세스 중에 해당 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p112">Yes. If a PST file contains a mailbox item that is larger than 150 MB, the item will be skipped during the import process.</span></span>
  
 <span data-ttu-id="ebcf6-151">**메시지를 보내거나 받은 경우와 같이 PST 파일을 Office 365 사서함으로 가져올 때 받는 사람 및 기타 속성 목록이 보존 되는 메시지 속성입니다.**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-151">**Are message properties, such as when the message was sent or received, the list of recipients and other properties, preserved when PST files are imported to an Office 365 mailbox?**</span></span>
  
<span data-ttu-id="ebcf6-p113">예로. 원본 메시지 메타 데이터는 가져오기 프로세스 중에 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p113">Yes. The original message metadata isn't changed during the import process.</span></span>
  
 <span data-ttu-id="ebcf6-154">**사서함으로 가져오려는 PST 파일에 대 한 폴더 계층 구조의 수준 수에 제한이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-154">**Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**</span></span>
  
<span data-ttu-id="ebcf6-p114">예로. 300 개 이상의 중첩 된 폴더를 포함 하는 PST 파일은 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p114">Yes. You can't import a PST file that has 300 or more levels of nested folders.</span></span>
  
 <span data-ttu-id="ebcf6-157">**네트워크 업로드를 사용 하 여 PST 파일을 Office 365의 비활성 사서함으로 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-157">**Can I use network upload to import PST files to an inactive mailbox in Office 365?**</span></span>
  
<span data-ttu-id="ebcf6-158">예, 이제이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-158">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="ebcf6-159">**네트워크 업로드를 사용 하 여 Exchange 하이브리드 배포의 온라인 보관 사서함으로 PST 파일을 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-159">**Can I use network upload to import PST files to an online archive mailbox in an Exchange hybrid deployment?**</span></span>
  
<span data-ttu-id="ebcf6-160">예, 이제이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-160">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="ebcf6-161">**네트워크 업로드를 사용 하 여 PST 파일을 Exchange Online의 공용 폴더에 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-161">**Can I use network upload to import PST files to public folders in Exchange Online?**</span></span>
  
<span data-ttu-id="ebcf6-162">아니요, PST 파일을 공용 폴더로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-162">No, you can't import PST files to public folders.</span></span>
  
## <a name="using-drive-shipping-to-import-pst-files"></a><span data-ttu-id="ebcf6-163">드라이브 전달을 사용 하 여 PST 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="ebcf6-163">Using drive shipping to import PST files</span></span>

<span data-ttu-id="ebcf6-164">단계별 지침은 [drive 발송을 사용 하 여 PST 파일을 Office 365에 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-164">For step-by-step instructions, see [Use drive shipping to import PST files to Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md).</span></span>
  
 <span data-ttu-id="ebcf6-165">**Office 365 가져오기 서비스에서 가져오기 작업을 만드는 데 필요한 사용 권한은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-165">**What permissions are required to create import jobs in the Office 365 Import Service?**</span></span>
  
<span data-ttu-id="ebcf6-p115">PST 파일을 Office 365 사서함으로 가져오려면 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 자신 또는 다른 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p115">You have to be assigned the Mailbox Import Export role to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
  
<span data-ttu-id="ebcf6-171">또한 Office 365 보안 &amp; 및 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-171">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
  
- <span data-ttu-id="ebcf6-p116">Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p116">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="ebcf6-174">또는</span><span class="sxs-lookup"><span data-stu-id="ebcf6-174">Or</span></span>
    
- <span data-ttu-id="ebcf6-175">Office 365 조 직의 전역 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-175">You have to be a global administrator in your Office 365 organization.</span></span>
    
> [!TIP]
> <span data-ttu-id="ebcf6-p117">Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p117">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
 <span data-ttu-id="ebcf6-178">**드라이브 배송을 사용할 수 있는 위치**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-178">**Where is drive shipping available?**</span></span>
  
<span data-ttu-id="ebcf6-p118">드라이브 전달은 미국, 캐나다, 브라질, 영국, 유럽, 인도, 동부 아시아, 동남 아시아, 일본, 한국, 호주, 오스트레일리아 이제 더 많은 지역에서 드라이브 전달을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p118">Drive shipping is currently available in the United States, Canada, Brazil, the United Kingdom, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Drive shipping will be available in more regions soon.</span></span>
  
 <span data-ttu-id="ebcf6-181">**드라이브 전달을 지 원하는 상업적 라이선스 계약은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-181">**What commercial licensing agreements support drive shipping?**</span></span>
  
<span data-ttu-id="ebcf6-p119">Office 365로 PST 파일을 가져오기 위한 드라이브 전달은 EA (Microsoft 엔터프라이즈 계약)를 통해 제공 됩니다. Microsoft 제품 및 서비스 계약 (mpsa)을 통해서는 드라이브 전달을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p119">Drive shipping to import PST files to Office 365 is available through a Microsoft Enterprise Agreement (EA). Drive shipping isn't available through a Microsoft Products and Services Agreement (MPSA).</span></span>
  
 <span data-ttu-id="ebcf6-184">**드라이브 전달을 사용 하 여 PST 파일을 Office 365로 가져올 때의 가격은 얼마 인가요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-184">**What is the pricing for using drive shipping to import PST files to Office 365?**</span></span>
  
<span data-ttu-id="ebcf6-p120">드라이브 전달을 사용 하 여 PST 파일을 Office 365 사서함으로 가져오는 비용은 데이터의 GB 당 $2 USD입니다. 예를 들어, 1000 기가바이트 (1tb)의 PST 파일을 포함 하는 하드 드라이브를 제공 하는 경우 비용은 $2000 USD입니다. 파트너와 협력 하 여 가져오기 비용을 지불 해 볼 수 있습니다. 파트너를 찾는 방법에 대 한 자세한 내용은 [Office 365 파트너 또는 대리점 찾기를](https://go.microsoft.com/fwlink/p/?LinkId=785197)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p120">The cost to use drive shipping to import PST files to Office 365 mailboxes is $2 USD per GB of data. For example, if you ship a hard drive that contains 1,000 GB (1 TB) of PST files, the cost is $2,000 USD. You can work with a partner to pay the import fee. For information about finding a partner, see [Find your Office 365 partner or reseller](https://go.microsoft.com/fwlink/p/?LinkId=785197).</span></span>
  
 <span data-ttu-id="ebcf6-189">**드라이브 전달에 대해 지원 되는 하드 드라이브 종류는 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-189">**What kind of hard drives are supported for drive shipping?**</span></span>
  
<span data-ttu-id="ebcf6-p121">Office 365 가져오기 서비스와 함께 사용할 경우에는 2.5 인치 ssd (고체 드라이브) 또는 2.5 또는 3.5 인치 SATA II/III 내부 하드 드라이브만 지원 됩니다. 하드 드라이브는 최대 10mb까지 사용할 수 있습니다. 가져오기 작업의 경우에는 하드 드라이브의 첫 번째 데이터 볼륨만 처리 됩니다. 데이터 볼륨은 NTFS로 포맷 해야 합니다. 데이터를 하드 드라이브에 복사 하는 경우, 2.5 인치 ssd 또는 2.5 또는 3.5 인치 sata ii/iii 커넥터를 사용 하 여 직접 연결 하거나 외부 2.5 cm SSD 또는 2.5 또는 3.5 인치 sata ii/iii USB 어댑터를 사용 하 여 외부에서 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p121">Only 2.5 inch solid-state drives (SSDs) or 2.5 or 3.5 inch SATA II/III internal hard drives are supported for use with the Office 365 Import service. You can use hard drives up to 10 TB. For import jobs, only the first data volume on the hard drive will be processed. The data volume must be formatted with NTFS. When copying data to a hard drive, you can attach it directly using a 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III connector or you can attach it externally using an external 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III USB adaptor.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ebcf6-p122">기본 제공 USB 어댑터와 함께 제공 되는 외부 하드 드라이브는 Office 365 가져오기 서비스에서 지원 되지 않습니다. 또한 외부 하드 드라이브 대/소문자 내의 디스크는 사용할 수 없습니다. 외부 하드 드라이브를 배송 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p122">External hard drives that come with an built-in USB adaptor aren't supported by the Office 365 Import service. Additionally, the disk inside the casing of an external hard drive can't be used. Please don't ship external hard drives.</span></span> 
  
 <span data-ttu-id="ebcf6-198">**단일 가져오기 작업에 사용할 수 있는 하드 드라이브는 몇 개입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-198">**How many hard drives can I ship for a single import job?**</span></span>
  
<span data-ttu-id="ebcf6-199">단일 가져오기 작업에 최대 10 개의 하드 드라이브를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-199">You can ship a maximum of 10 hard drives for a single import job.</span></span>
  
 <span data-ttu-id="ebcf6-200">**하드 드라이브를 배송 하 고 나 서 Microsoft 데이터 센터에 액세스 하는 데 어느 정도의 시간이 걸립니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-200">**After I ship my hard drive, how long does it take to get to the Microsoft data center?**</span></span>
  
<span data-ttu-id="ebcf6-p123">Microsoft 데이터 센터와 같이 하드 드라이브를 제공 하는 데 사용 하는 배송 옵션 (예:, 다음 영업일 배송, 2 일 배송 또는 지상 배달)과 같은 몇 가지 사항에 따라 달라 집니다. 대부분의 운송 업체에서는 추적 번호를 사용 하 여 배달 상태를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p123">That depends on a few things, such as your proximity to the Microsoft data center and what kind of shipping option you used to ship your hard drive (such as, next-day delivery, two-day delivery, or ground-delivery). With most shippers, you can use the tracking number to track the status of your delivery.</span></span>
  
 <span data-ttu-id="ebcf6-203">**Microsoft 데이터 센터에 하드 드라이브가 도착 한 후 Azure에 내 PST 파일을 업로드 하는 데 얼마나 걸립니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-203">**After my hard drive arrives at the Microsoft data center, how long does it take to upload my PST files to Azure?**</span></span>
  
<span data-ttu-id="ebcf6-p124">microsoft 데이터 센터에서 하드 드라이브를 받은 후에는 해당 조직의 microsoft Azure storage 영역에 PST 파일을 업로드 하기 위해 7 일에서 10 일까 지를 담당 합니다. PST 파일이 **ingestiondata**라는 Azure blob 컨테이너에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p124">After your hard drive is received at the Microsoft data center, it will take between 7 to 10 business days to upload the PST files to the Microsoft Azure storage area for your organization. The PST files will be uploaded to a Azure blob container named **ingestiondata**.</span></span> 
  
 <span data-ttu-id="ebcf6-206">**PST 파일을 사서함에 가져오는 데 소요 되는 시간**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-206">**How long does it take to import a PST file to a mailbox?**</span></span>
  
<span data-ttu-id="ebcf6-p125">pst 파일이 Azure storage 영역에 업로드 된 후에 Office 365는 pst 파일의 데이터를 안전 하 고 안전한 방식으로 분석 하 여 항목의 보존 기간 및 pst 파일에 포함 된 다양 한 메시지 유형을 식별 합니다. 이 분석이 완료 되 면 PST 파일의 모든 데이터를 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하는 옵션을 사용할 수 있습니다. 가져오기 작업을 시작한 후에는 PST 파일을 하루 중 24gb 이상으로 Office 365 사서함으로 가져옵니다. 이 속도가 사용자의 요구를 충족 하지 않는 경우 전자 메일 데이터를 Office 365로 가져오는 다른 방법을 고려할 수 있습니다. 자세한 내용은 [여러 전자 메일 계정을 Office 365로 마이그레이션하는 방법을](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p125">After the PST files are uploaded to the Azure storage area, Office 365 analyzes the data in the PST files (in a safe and secure manner) to identify the age of the items and the different message types included in the PST files. When this analysis is complete, you'll have the option to import all the data in the PST files or set filters to that control what data gets imported. After you start the import job, a PST file is imported to an Office 365 mailbox at a rate of at least 24 GB per day. If this rate doesn't meet your needs, you might consider other methods for importing email data to Office 365. For more information, see [Ways to migrate multiple email accounts to Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).</span></span>
  
<span data-ttu-id="ebcf6-p126">서로 다른 PST 파일을 다른 대상 사서함으로 가져오는 경우 가져오기 프로세스는 동시에 수행 됩니다. 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로 여러 PST 파일을 같은 사서함으로 가져오는 경우 동시에 가져오게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p126">If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Likewise, if multiple PST files are imported to the same mailbox, they will be simultaneously imported.</span></span>
  
 <span data-ttu-id="ebcf6-214">**Microsoft에서 내 PST 파일을 azure로 업로드 한 후 삭제 하기 전에 azure에 보관 되는 기간**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-214">**After Microsoft uploads my PST files to Azure, how long are they kept in Azure before they're deleted?**</span></span>
  
<span data-ttu-id="ebcf6-215">조직의 Azure 저장소 위치에 있는 모든 PST 파일 ( **ingestiondata** 이라는 blob 컨테이너)은 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서 최근 가져오기 작업을 만든 후 30 일이 지나면 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-215">All PST files in the Azure storage location for your organization (in blob container named **ingestiondata** ), are deleted 30 days after the most recent import job was created on the **Import** page in the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="ebcf6-p127">또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 보안 &amp; 및 준수 센터에서 완료 된 가져오기 작업의 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 보안 &amp; 준수 센터의 **가져오기** 페이지에 나열 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p127">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Security &amp; Compliance Center. Although an import job might still be listed on the **Import** page in the Security &amp; Compliance Center, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="ebcf6-218">**Office 365로 가져올 때 지원 되는 PST 파일 형식의 버전은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-218">**What version of the PST file format is supported for importing to Office 365?**</span></span>
  
<span data-ttu-id="ebcf6-p128">PST 파일 형식에는 ANSI 및 Unicode의 두 가지 버전이 있습니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 DBCS (더블 바이트 문자 집합)를 사용 하는 언어와 같이 ANSI PST 파일 형식을 사용 하는 파일은 Office 365로도 가져올 수 있습니다. ANSI PST 파일을 가져오는 방법에 대 한 자세한 내용은 on [drive 발송을 사용 하 여 PST 파일을 Office 365로 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file)의 3 단계를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p128">There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. However, files that use the ANSI PST file format, such as those for languages that use a double-byte character set (DBCS), can also be imported to Office 365. For more information about importing ANSI PST files, see Step 3 in [Use drive shipping to import PST files to Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).</span></span>
  
<span data-ttu-id="ebcf6-223">또한 Outlook 2007 이상 버전의 PST 파일을 Office 365로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-223">Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.</span></span>
  
 <span data-ttu-id="ebcf6-224">**PST 파일을 가져올 때 메시지 크기 제한이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-224">**Is there a message size limit when importing PST files?**</span></span>
  
<span data-ttu-id="ebcf6-p129">예로. PST 파일에 150 보다 큰 사서함 항목이 포함 되어 있으면 가져오기 프로세스 중에 해당 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p129">Yes. If a PST file contains a mailbox item that is larger than 150 MB, the item will be skipped during the import process.</span></span>
  
 <span data-ttu-id="ebcf6-227">**메시지를 보내거나 받은 경우와 같이 PST 파일을 Office 365 사서함으로 가져올 때 받는 사람 및 기타 속성 목록이 보존 되는 메시지 속성입니다.**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-227">**Are message properties, such as when the message was sent or received, the list of recipients and other properties, preserved when PST files are imported to an Office 365 mailbox?**</span></span>
  
<span data-ttu-id="ebcf6-p130">예로. 원본 메시지 메타 데이터는 가져오기 프로세스 중에 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p130">Yes. The original message metadata isn't changed during the import process</span></span>
  
 <span data-ttu-id="ebcf6-230">**사서함으로 가져오려는 PST 파일에 대 한 폴더 계층 구조의 수준 수에 제한이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-230">**Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**</span></span>
  
<span data-ttu-id="ebcf6-p131">예로. 300 개 이상의 중첩 된 폴더를 포함 하는 PST 파일은 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p131">Yes. You can't import a PST file that has 300 or more levels of nested folders.</span></span>
  
 <span data-ttu-id="ebcf6-233">**Office 365에서 드라이브 전달을 사용 하 여 PST 파일을 비활성 사서함으로 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-233">**Can I use drive shipping to import PST files to an inactive mailbox in Office 365?**</span></span>
  
<span data-ttu-id="ebcf6-234">예, 이제이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-234">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="ebcf6-235">**드라이브 전달을 사용 하 여 PST 파일을 Exchange 하이브리드 배포의 온라인 보관 사서함으로 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-235">**Can I use drive shipping to import PST files to an online archive mailbox in an Exchange hybrid deployment?**</span></span>
  
<span data-ttu-id="ebcf6-236">예, 이제이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-236">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="ebcf6-237">**드라이브 전달을 사용 하 여 PST 파일을 Exchange Online의 공용 폴더로 가져올 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-237">**Can I use drive shipping to import PST files to public folders in Exchange Online?**</span></span>
  
<span data-ttu-id="ebcf6-238">아니요, PST 파일을 공용 폴더로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-238">No, you can't import PST files to public folders.</span></span>
  
 <span data-ttu-id="ebcf6-239">**Microsoft에서 내 하드 드라이브를 초기화 한 후에 다시 출하 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-239">**Can Microsoft wipe my hard drive before they ship it back to me?**</span></span>
  
<span data-ttu-id="ebcf6-p132">아니요, Microsoft는 고객에 게 다시 배송 하기 전에 하드 드라이브를 제거할 수 없습니다. 하드 드라이브를 Microsoft에서 받은 것과 같은 상태로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p132">No, Microsoft can't wipe hard drives before shipping them back to customers. Hard drives are returned to you in the same state they were in when they were received by Microsoft.</span></span>
  
 <span data-ttu-id="ebcf6-242">**Microsoft에서 내 하드 드라이브를 다시 배송 하지 않고 shred 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-242">**Can Microsoft shred my hard drive instead of shipping it back to me?**</span></span>
  
<span data-ttu-id="ebcf6-p133">아니요, Microsoft에서 하드 드라이브를 삭제할 수 없습니다. 하드 드라이브를 Microsoft에서 받은 것과 같은 상태로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p133">No, Microsoft can't destroy your hard drive. Hard drives are returned to you in the same state they were in when they were received by Microsoft.</span></span>
  
 <span data-ttu-id="ebcf6-245">**반품 상품을 위해 지원 되는 courier services는 무엇 인가요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-245">**What courier services are supported for return shipping?**</span></span>
  
<span data-ttu-id="ebcf6-p134">미국 또는 유럽의 고객 인 경우 Microsoft는 FedEx을 사용 하 여 하드 드라이브를 반환 합니다. 다른 모든 지역에 대해 Microsoft는 DHL를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p134">If you're a customer in the United States or Europe, Microsoft uses FedEx to return your hard drive. For all other regions, Microsoft uses DHL.</span></span>
  
 <span data-ttu-id="ebcf6-248">**반품 배송 비용은 얼마 입니까?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-248">**What are the return shipping costs?**</span></span>
  
<span data-ttu-id="ebcf6-p135">반품 비용은 하드 드라이브를 전달한 Microsoft 데이터 센터에 따라 달라 집니다. Microsoft는 하드 드라이브를 반환 하기 위해 FedEx 또는 DHL 계정을 청구할 것입니다. 반품 비용은 귀하의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p135">Return shipping costs vary, depending on your proximity to the Microsoft data center that you shipped your hard drive to. Microsoft will bill your FedEx or DHL account to return your hard drive. The cost of return shipping is your responsibility.</span></span>
  
 <span data-ttu-id="ebcf6-252">**FedEx 사용자 지정 운송과 같은 사용자 지정 courier 선적 서비스를 사용 하 여 Microsoft에 하드 드라이브를 제공할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-252">**Can I use a custom courier shipping service, such as FedEx Custom Shipping, to ship my hard drive to Microsoft?**</span></span>
  
<span data-ttu-id="ebcf6-253">예.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-253">Yes.</span></span>
  
 <span data-ttu-id="ebcf6-254">**하드 드라이브를 다른 국가로 배송 해야 하는 경우에는 필요한 모든 작업을 수행 해야 하나요?**</span><span class="sxs-lookup"><span data-stu-id="ebcf6-254">**If I have to ship my hard drive to another country, is there anything I need to do?**</span></span>
  
<span data-ttu-id="ebcf6-p136">Microsoft에 제공 하는 하드 드라이브는 해외 테두리를 교차 해야 할 수도 있습니다. 이 경우 해당 하는 법률에 따라 하드 드라이브와 해당 파일에 포함 된 데이터를 가져오고/또는 내보내도록 합니다. 하드 드라이브를 출시 하기 전에 관리자에 게 문의 하 여 드라이브 및 데이터가 지정 된 Microsoft 데이터 센터로 합법적으로 전달 될 수 있는지 확인 합니다. 이렇게 하면 Microsoft에 적시에 도달 하는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-p136">The hard drive that you ship to Microsoft might have to cross international borders. If this is the case, you're responsible for ensuring that the hard drive and the data it contains are imported and/or exported in accordance with the applicable laws. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the specified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.</span></span>
