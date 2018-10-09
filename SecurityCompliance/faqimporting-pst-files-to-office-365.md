---
title: Office 365에 PST 파일 가져오기 (영문) 하는 방법에 대 한 FAQ
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 2fe71b05-f5a2-4182-ade7-4dc5cabdfd51
description: '질문과 대답 관리자를 위한 Office 365 사서함으로 프로그램 organizaiton PST 파일을 가져오려면 Office 365 가져오기 서비스를 사용 하는 방법에 대 한 합니다. '
ms.openlocfilehash: 7230e68f896766df643f12b2a132f987670e9afa
ms.sourcegitcommit: eecf6f3aafbf460ee2ff9988f2b055e62b1fdb9d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454055"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a><span data-ttu-id="d28b9-103">Office 365에 PST 파일 가져오기 (영문) 하는 방법에 대 한 FAQ</span><span class="sxs-lookup"><span data-stu-id="d28b9-103">FAQ about importing PST files to Office 365</span></span>

<span data-ttu-id="d28b9-104">**이 문서는 관리자입니다. 자신의 사서함에 PST 파일을 가져올 하 시겠습니까? [가져오기 전자 메일, 연락처 및 일정 Outlook.pst 파일에서](https://go.microsoft.com/fwlink/p/?LinkID=785075) 를 참조 하십시오.**|</span><span class="sxs-lookup"><span data-stu-id="d28b9-104">**This article is for administrators. Do you want to import PST files to your own mailbox? See [Import email, contacts, and calendar from an Outlook .pst file](https://go.microsoft.com/fwlink/p/?LinkID=785075)**|</span></span>
   
<span data-ttu-id="d28b9-p101">다음은 대량 가져오기 PST 파일을 Office 365 사서함을 Office 365 가져오기 서비스를 사용 하는 방법에 대 한 몇가지 질문과 대답입니다. PST 파일을 가져오는 방법에 대 한 자세한 내용은 [Office 365에 PST 파일 가져오기 (영문)의 개요](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p101">Here are some frequently asked questions about using the Office 365 Import Service to bulk-import PST files to Office 365 mailboxes. For more information about how to import PST files, see [Overview of importing PST files to Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84).</span></span>
  
## <a name="using-network-upload-to-import-pst-files"></a><span data-ttu-id="d28b9-107">네트워크 업로드를 사용 하 여 PST 파일을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="d28b9-107">Using network upload to import PST files</span></span>

<span data-ttu-id="d28b9-108">단계별 지침은 [Office 365에 PST 파일을 가져오려면 업로드 사용 하 여 네트워크](use-network-upload-to-import-pst-files.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d28b9-108">For step-by-step instructions, see [Use network upload to import PST files to Office 365](use-network-upload-to-import-pst-files.md).</span></span>
  
 <span data-ttu-id="d28b9-109">**Office 365 가져오기 서비스에서 가져오기 작업을 만들 필요가 권한은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-109">**What permissions are required to create import jobs in the Office 365 Import Service?**</span></span>
  
<span data-ttu-id="d28b9-p102">역할을 할당 사서함 가져오기 내보내기 Exchange 온라인 Office 365 사서함에 PST 파일을 가져오려면 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 사용자가 직접 또는 다른 사용자가 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹 Exchange Online의](https://go.microsoft.com/fwlink/p/?LinkId=730688)"역할 그룹 만들기" 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p102">You have to be assigned the Mailbox Import Export role in Exchange Online to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
  
<span data-ttu-id="d28b9-115">또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-115">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
  
- <span data-ttu-id="d28b9-p103">역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p103">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="d28b9-118">또는</span><span class="sxs-lookup"><span data-stu-id="d28b9-118">Or</span></span>
    
- <span data-ttu-id="d28b9-119">Office 365 조직에서 전역 관리자 여야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-119">You have to be a global administrator in your Office 365 organization.</span></span>
    
> [!TIP]
> <span data-ttu-id="d28b9-p104">Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p104">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
 <span data-ttu-id="d28b9-122">**네트워크 업로드는 사용할 수 있는 어디 입니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-122">**Where is network upload available?**</span></span>
  
<span data-ttu-id="d28b9-p105">네트워크 업로드는 미국, 캐나다, 브라질, 영국, 프랑스, 유럽, 인도, 한국, 남동쪽 아시아, 일본, 대한민국, 및 오스트레일리아에서 현재 사용할 수 있습니다. 네트워크 업로드 곧 사용할 수 있는 더 많은 지역에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p105">Network upload is currently available in the United States, Canada, Brazil, the United Kingdom, France, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Network upload will be available in more regions soon.</span></span>
  
 <span data-ttu-id="d28b9-125">**네트워크 업로드를 사용 하 여 PST 파일을 가져오기 위한 가격 이란 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-125">**What is the pricing for importing PST files by using network upload?**</span></span>
  
<span data-ttu-id="d28b9-126">네트워크 업로드를 사용 하 여 PST 파일을 가져올 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-126">Using network upload to import PST files is free.</span></span>
  
<span data-ttu-id="d28b9-p106">즉,는 Azure 저장소 영역에서 PST 파일을 삭제 하 고, 후 더이상 표시 Office 365 관리 센터에서 완료 된 가져오기 작업에 대 한 파일의 목록입니다. 가져오기 작업은 **Office 365로 데이터 가져오기** 페이지에서 계속 표시 될 수 있습니다, 하지만 오래 된 가져오기 작업의 세부 정보를 볼 때에 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p106">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Office 365 admin center. Although an import job might still be listed on the **Import data to Office 365** page, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="d28b9-129">**PST 파일 형식의 어떤 버전은 Office 365로 가져오기에 대 한 지원 합니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-129">**What version of the PST file format is supported for importing to Office 365?**</span></span>
  
<span data-ttu-id="d28b9-p107">PST 파일 형식의 두 버전이: ANSI 및 유니코드 합니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 ANSI PST 파일 형식 더블 바이트 문자를 사용 하는 언어에 대 한 예를 사용 하는 파일 (DBCS) 설정, Office 365로 가져올 수도 있습니다. ANSI PST 파일 가져오기 (영문) 하는 방법에 대 한 자세한 내용은 [Office 365에 조직의 PST 파일을 가져오려면 업로드 사용 하 여 네트워크](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file)에서 4 단계를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p107">There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. However, files that use the ANSI PST file format, such as those for languages that use a double-byte character set (DBCS), can also be imported to Office 365. For more information about importing ANSI PST files, see Step 4 in [Use network upload to import your organization's PST files to Office 365](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file).</span></span>
  
<span data-ttu-id="d28b9-134">또한 Office 365로 Outlook 2007 및 그 이후 버전에서 PST 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-134">Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.</span></span>
  
 <span data-ttu-id="d28b9-135">**Azure 저장소 영역 내 PST 파일을 업로드 하 한 후 얼마나 오래 자신이에 보관 되는 Azure 삭제 되기 전에?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-135">**After I upload my PST files to the Azure storage area, how long are they kept in Azure before they're deleted?**</span></span>
  
<span data-ttu-id="d28b9-p108">PST 파일을 가져오려면 네트워크 업로드 메서드를 사용 하면 **ingestiondata**라는 Azure blob 컨테이너에 업로드 있습니다. 에 없는 경우 가져오기 작업이 진행 중인 **가져오기** 페이지에서 보안을 &amp; 준수 센터), Azure의 **ingestiondata** 컨테이너에 있는 모든 PST 파일 30 일 &amp;준수 센터입니다. 보안에서 새 가져오기 작업을 만들 필요가 의미 &amp; Azure에 파일을 업로드 PST의 30 일 이내에 준수 센터 (네트워크 업로드 지침의 5 단계에에서 설명 된).</span><span class="sxs-lookup"><span data-stu-id="d28b9-p108">When you use the network upload method to import PST files, you upload them to an Azure blob container named **ingestiondata**. If there are no import jobs in progress on the **Import** page in the Security &amp; Compliance Center), then all PST files in the **ingestiondata** container in Azure are deleted 30 days after the most recent import job was created in the Security &amp; Compliance Center. That also means you have to create a new import job in the Security &amp; Compliance Center (described in Step 5 in the network upload instructions) within 30 days of uploading PST files to Azure.</span></span> 
  
<span data-ttu-id="d28b9-p109">즉, Azure 저장소 영역에서 PST 파일을 삭제 하 고, 후 자신이 더이상 표시 되는지의 보안에서 완료 된 가져오기 작업에 대 한 파일 목록에서 &amp; 준수 센터입니다. 가져오기 작업 **가져오기** 페이지의 보안에 계속 표시 될 수 있습니다 있지만 &amp; 준수 센터 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p109">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Security &amp; Compliance Center. Although an import job might still be listed on the **Import** page in the Security &amp; Compliance Center, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="d28b9-141">**걸리는 사서함에 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-141">**How long does it take to import a PST file to a mailbox?**</span></span>
  
<span data-ttu-id="d28b9-p110">네트워크 용량에 따라 달라 집니다 있지만 조직에 대 한 Azure 저장소 영역에 업로드 하는 데이터의 각 테라바이트 (테라바이트)에 대 한 몇 시간이 오래 걸립니다. PST 파일은 Azure 저장소 영역을 복사한 후 하루 24GB 이상인의 속도로 Office 365 사서함에는 PST 파일을 가져옵니다. 이 속도가 하지 사용자의 요구를 충족 하는 경우에 Office 365로 전자 메일 데이터를 마이그레이션하기 위한 다른 방법을 좋습니다. 자세한 내용은 [Office 365에 여러 전자 메일 계정으로 마이그레이션하는 방법](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p110">It depends on the capacity of your network, but it typically takes several hours for each terabyte (TB) of data to be uploaded to the Azure storage area for your organization. After the PST files are copied to the Azure storage area, a PST file is imported to an Office 365 mailbox at a rate of at least 24 GB per day. If this rate doesn't meet your needs, you might consider other methods for migrating email data to Office 365. For more information, see [Ways to migrate multiple email accounts to Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).</span></span>
  
<span data-ttu-id="d28b9-p111">가져오기 프로세스 병렬로; 발생 서로 다른 대상 사서함에 다른 PST 파일을 가져오는 경우 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로, 동일한 사서함에 여러 PST 파일을 가져오는 경우 자신이 됩니다 동시에 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p111">If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Likewise, if multiple PST files are imported to the same mailbox, they will be simultaneously imported.</span></span>
  
 <span data-ttu-id="d28b9-148">**메시지 크기 제한을 PST 파일을 가져올 때 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-148">**Is there a message size limit when importing PST files?**</span></span>
  
<span data-ttu-id="d28b9-p112">예입니다. PST 파일 150MB 보다 큰 사서함 항목을 포함 하는 경우 항목 가져오기 프로세스를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p112">Yes. If a PST file contains a mailbox item that is larger than 150 MB, the item will be skipped during the import process.</span></span>
  
 <span data-ttu-id="d28b9-151">**메시지를 보내거나 받은, 받는 사람 목록과 기타 속성을 Office 365 사서함에 PST 파일을 가져올 때 유지 하는 경우와 같은 메시지 속성은?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-151">**Are message properties, such as when the message was sent or received, the list of recipients and other properties, preserved when PST files are imported to an Office 365 mailbox?**</span></span>
  
<span data-ttu-id="d28b9-p113">예입니다. 원본 메시지 메타 데이터 가져오기 과정에서 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p113">Yes. The original message metadata isn't changed during the import process.</span></span>
  
 <span data-ttu-id="d28b9-154">**이 사서함에 가져오려는 PST 파일에 대 한 폴더 계층 구조에 있는 수준 수에 제한이 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-154">**Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**</span></span>
  
<span data-ttu-id="d28b9-p114">예입니다. 중첩 된 폴더의 300 개 이상인 수준이 있는 PST 파일을 가져올 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p114">Yes. You can't import a PST file that has 300 or more levels of nested folders.</span></span>
  
 <span data-ttu-id="d28b9-157">**네트워크 업로드를 사용 하 여 Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-157">**Can I use network upload to import PST files to an inactive mailbox in Office 365?**</span></span>
  
<span data-ttu-id="d28b9-158">예, 이제이 기능은 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-158">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="d28b9-159">**네트워크 업로드를 사용 하 여 Exchange 하이브리드 배포에서 온라인 보관 사서함을 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-159">**Can I use network upload to import PST files to an online archive mailbox in an Exchange hybrid deployment?**</span></span>
  
<span data-ttu-id="d28b9-160">예, 이제이 기능은 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-160">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="d28b9-161">**네트워크 업로드를 사용 하 여 Exchange Online에서 공용 폴더에 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-161">**Can I use network upload to import PST files to public folders in Exchange Online?**</span></span>
  
<span data-ttu-id="d28b9-162">아니요, 공용 폴더에는 PST 파일을 가져올 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-162">No, you can't import PST files to public folders.</span></span>
  
## <a name="using-drive-shipping-to-import-pst-files"></a><span data-ttu-id="d28b9-163">드라이브 전달을 사용 하 여 PST 파일을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="d28b9-163">Using drive shipping to import PST files</span></span>

<span data-ttu-id="d28b9-164">단계별 지침은 [Office 365에 PST 파일을 가져오려면 전달 하는 드라이브를 사용 하 여](use-drive-shipping-to-import-pst-files-to-office-365.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d28b9-164">For step-by-step instructions, see [Use drive shipping to import PST files to Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md).</span></span>
  
 <span data-ttu-id="d28b9-165">**Office 365 가져오기 서비스에서 가져오기 작업을 만들 필요가 권한은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-165">**What permissions are required to create import jobs in the Office 365 Import Service?**</span></span>
  
<span data-ttu-id="d28b9-p115">Office 365 사서함에 PST 파일을 가져오려면 사서함 가져오기 내보내기 역할을 할당 해야 합니다. 기본적으로이 역할 되지 할당 된 모든 역할 그룹에 Exchange 온라인 합니다. 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들, 사서함 가져오기 내보내기 역할을 할당 한 사용자가 직접 또는 다른 사용자가 구성원으로 추가 합니다. 자세한 내용은 "역할 그룹에 역할 추가"를 참조 또는 [관리 역할 그룹 Exchange Online의](https://go.microsoft.com/fwlink/p/?LinkId=730688)"역할 그룹 만들기" 섹션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p115">You have to be assigned the Mailbox Import Export role to import PST files to Office 365 mailboxes. By default, this role isn't assigned to any role group in Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. For more information, see the "Add a role to a role group" or the "Create a role group" sections in [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).</span></span>
  
<span data-ttu-id="d28b9-171">또한 가져오기 작성 하려면 Office 365 보안에서 작업 &amp; 는 다음 중 하나를 준수 센터 조건이 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-171">Additionally, to create import jobs in the Office 365 Security &amp; Compliance Center, one of the following must be true:</span></span>
  
- <span data-ttu-id="d28b9-p116">역할을 할당 메일 받는 사람에 게 Exchange 온라인 해야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p116">You have to be assigned the Mail Recipients role in Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.</span></span>
    
    <span data-ttu-id="d28b9-174">또는</span><span class="sxs-lookup"><span data-stu-id="d28b9-174">Or</span></span>
    
- <span data-ttu-id="d28b9-175">Office 365 조직에서 전역 관리자 여야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-175">You have to be a global administrator in your Office 365 organization.</span></span>
    
> [!TIP]
> <span data-ttu-id="d28b9-p117">Exchange online을 Office 365 PST 파일을 가져오기 위한 구체적으로 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오려면 필요한 권한을 최소 수준에 대 한 새 역할 그룹에는 사서함 가져오기 내보내기 및 편지 병합 받는 사람 역할을 할당 하 고 구성원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p117">Consider creating a new role group in Exchange Online that's specifically intended for importing PST files to Office 365. For the minimum level of privileges required to import PST files, assign the Mailbox Import Export and Mail Recipients roles to the new role group, and then add members.</span></span> 
  
 <span data-ttu-id="d28b9-178">**여기서 제공 되는 드라이브 사용할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-178">**Where is drive shipping available?**</span></span>
  
<span data-ttu-id="d28b9-p118">드라이브 전달은 미국, 캐나다, 브라질, 영국, 유럽, 인도, 한국, 남동쪽 아시아, 일본, 대한민국, 및 오스트레일리아 현재 사용할 수 있습니다. 드라이브 전달 곧 사용할 수 있는 더 많은 지역에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p118">Drive shipping is currently available in the United States, Canada, Brazil, the United Kingdom, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Drive shipping will be available in more regions soon.</span></span>
  
 <span data-ttu-id="d28b9-181">**어떤 상업용 라이선스 계약 드라이브 전달이 지원 합니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-181">**What commercial licensing agreements support drive shipping?**</span></span>
  
<span data-ttu-id="d28b9-p119">Office 365에 PST 파일을 가져오려면 전달 하는 드라이브를 사용할 수를 통해는 Microsoft EA (기업 계약). 드라이브 전달 Microsoft 제품 및 서비스 계약 (MPSA)를 통해 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p119">Drive shipping to import PST files to Office 365 is available through a Microsoft Enterprise Agreement (EA). Drive shipping isn't available through a Microsoft Products and Services Agreement (MPSA).</span></span>
  
 <span data-ttu-id="d28b9-184">**Office 365에 PST 파일을 가져오려면 전달 하는 드라이브를 사용 하는 것에 대 한 가격 이란 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-184">**What is the pricing for using drive shipping to import PST files to Office 365?**</span></span>
  
<span data-ttu-id="d28b9-p120">Office 365 사서함에 PST 파일을 가져오려면 드라이브 전달을 사용 하 여 비용은 $2 달러 (미국) GB의 데이터입니다. 예, 1, 000 g B (1TB)의 PST 파일을 포함 하는 하드 드라이브를 제공 하는 경우는 비용은 $ 2, 000 USD입니다. 가져오기 요금을 지불 하는 파트너를 사용 하 여 작업할 수 있습니다. 파트너 찾기 (영문) 하는 방법에 대 한 정보를 [Office 365 파트너 또는 대리점 찾기](https://go.microsoft.com/fwlink/p/?LinkId=785197)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p120">The cost to use drive shipping to import PST files to Office 365 mailboxes is $2 USD per GB of data. For example, if you ship a hard drive that contains 1,000 GB (1 TB) of PST files, the cost is $2,000 USD. You can work with a partner to pay the import fee. For information about finding a partner, see [Find your Office 365 partner or reseller](https://go.microsoft.com/fwlink/p/?LinkId=785197).</span></span>
  
 <span data-ttu-id="d28b9-189">**어떤 종류의 하드 드라이브 드라이브 전달에 대 한 지원 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-189">**What kind of hard drives are supported for drive shipping?**</span></span>
  
<span data-ttu-id="d28b9-p121">2.5 인치만 반도체 드라이브 (Ssd) 또는 2.5 또는 3.5 인치 SATA II/III 내부 하드 드라이브에 Office 365 가져오기 서비스와 함께 사용할 수 있도록 지원 합니다. 하드 드라이브를 사용할 수 있는 최대 10TB 합니다. 가져오기 작업에 대 한 하드 드라이브에 첫번째 데이터 볼륨을 처리 됩니다. 데이터 볼륨 NTFS로 포맷 되어야 합니다. 하드 드라이브에 데이터를 복사, 2.5 인치 SSD를 사용 하 여 직접 연결할 수 있습니다 또는 2.5 또는 3.5 인치 SATA II/III 커넥터 또는 외부 2.5 인치 SSD를 사용 하 여 외부에서 또는 2.5 또는 3.5 인치 SATA II/III USB 어댑터를 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p121">Only 2.5 inch solid-state drives (SSDs) or 2.5 or 3.5 inch SATA II/III internal hard drives are supported for use with the Office 365 Import service. You can use hard drives up to 10 TB. For import jobs, only the first data volume on the hard drive will be processed. The data volume must be formatted with NTFS. When copying data to a hard drive, you can attach it directly using a 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III connector or you can attach it externally using an external 2.5 inch SSD or 2.5 or 3.5 inch SATA II/III USB adaptor.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d28b9-p122">외부 하드 드라이브에 사용 된 기본 제공 된 USB 어댑터와 함께 제공 되는 Office 365 가져오기 서비스에서 지원 되지 않습니다. 또한 외부 하드 드라이브의 대/소문자 내부 디스크를 사용할 수 없습니다. 하드 드라이브에 외부 하십시오 제공 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p122">External hard drives that come with an built-in USB adaptor aren't supported by the Office 365 Import service. Additionally, the disk inside the casing of an external hard drive can't be used. Please don't ship external hard drives.</span></span> 
  
 <span data-ttu-id="d28b9-198">**단일 가져오기 작업에 대 한 제공할 수 하드 드라이브에 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-198">**How many hard drives can I ship for a single import job?**</span></span>
  
<span data-ttu-id="d28b9-199">단일 가져오기 작업에 대 한 하드 드라이브에 10의 최대를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-199">You can ship a maximum of 10 hard drives for a single import job.</span></span>
  
 <span data-ttu-id="d28b9-200">**후 내 하드 드라이브를 제공 하는 소요 Microsoft 데이터 센터를?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-200">**After I ship my hard drive, how long does it take to get to the Microsoft data center?**</span></span>
  
<span data-ttu-id="d28b9-p123">Microsoft 데이터 센터에 근접 하 여 같은 몇가지 작업에 따라 다릅니다 하 고 사용자의 하드 드라이브 (예: 다음 일 배송, 2 일 배달 날짜 또는 밑면 배달)를 제공 하는 데 사용 전달 옵션의 종류입니다. 대부분 shippers와 프로그램 배달의 상태를 추적 하려면 추적 번호를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p123">That depends on a few things, such as your proximity to the Microsoft data center and what kind of shipping option you used to ship your hard drive (such as, next-day delivery, two-day delivery, or ground-delivery). With most shippers, you can use the tracking number to track the status of your delivery.</span></span>
  
 <span data-ttu-id="d28b9-203">**Microsoft 데이터 센터에 도착 하면 내 하드 드라이브는 걸리는 Azure에 내 PST 파일을 업로드할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-203">**After my hard drive arrives at the Microsoft data center, how long does it take to upload my PST files to Azure?**</span></span>
  
<span data-ttu-id="d28b9-p124">하드 드라이브에 Microsoft 데이터 센터를 받은 후에 조직에 대 한 Microsoft Azure 저장소 영역에 PST 파일을 업로드 하려면 7 ~ 10 일 사이의 수행 됩니다. **Ingestiondata**라는 Azure blob 컨테이너에 PST 파일을 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p124">After your hard drive is received at the Microsoft data center, it will take between 7 to 10 business days to upload the PST files to the Microsoft Azure storage area for your organization. The PST files will be uploaded to a Azure blob container named **ingestiondata**.</span></span> 
  
 <span data-ttu-id="d28b9-206">**걸리는 사서함에 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-206">**How long does it take to import a PST file to a mailbox?**</span></span>
  
<span data-ttu-id="d28b9-p125">PST 파일 Azure 저장소 영역으로 업로드 된 후 Office 365를 분석 PST 파일의 데이터 (을 안전 하 게 방식으로)를 다양 한 메시지 형식과 PST 파일에 포함 된 항목의 보존 기간을 식별 합니다. 이 분석 완료 되 면 PST 파일에 있는 모든 데이터를 가져올 수 있는 옵션 해야 또는 하는 필터 설정 제어 가져온 데이터를 가져옵니다. 가져오기 작업을 시작한 후 하루 24GB 이상인의 속도로 Office 365 사서함에는 PST 파일을 가져옵니다. 이 속도가 하지 사용자의 요구를 충족 하는 경우에 Office 365로 전자 메일 데이터를 가져오기 위한 다른 방법을 좋습니다. 자세한 내용은 [Office 365에 여러 전자 메일 계정으로 마이그레이션하는 방법](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p125">After the PST files are uploaded to the Azure storage area, Office 365 analyzes the data in the PST files (in a safe and secure manner) to identify the age of the items and the different message types included in the PST files. When this analysis is complete, you'll have the option to import all the data in the PST files or set filters to that control what data gets imported. After you start the import job, a PST file is imported to an Office 365 mailbox at a rate of at least 24 GB per day. If this rate doesn't meet your needs, you might consider other methods for importing email data to Office 365. For more information, see [Ways to migrate multiple email accounts to Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).</span></span>
  
<span data-ttu-id="d28b9-p126">가져오기 프로세스 병렬로; 발생 서로 다른 대상 사서함에 다른 PST 파일을 가져오는 경우 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로, 동일한 사서함에 여러 PST 파일을 가져오는 경우 자신이 됩니다 동시에 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p126">If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Likewise, if multiple PST files are imported to the same mailbox, they will be simultaneously imported.</span></span>
  
 <span data-ttu-id="d28b9-214">**Microsoft Azure에 내 PST 파일을 업로드, 후 얼마나 오래 자신이에 보관 되는 Azure 삭제 되기 전에?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-214">**After Microsoft uploads my PST files to Azure, how long are they kept in Azure before they're deleted?**</span></span>
  
<span data-ttu-id="d28b9-215">Azure 저장소 위치에 있는 모든 PST 파일 (blob 컨테이너에 **ingestiondata** 라는), 조직에 대 한 일 **가져오기** 페이지의 보안에서 가장 최근의 가져오기 작업이 만들어진 후에 삭제 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-215">All PST files in the Azure storage location for your organization (in blob container named **ingestiondata** ), are deleted 30 days after the most recent import job was created on the **Import** page in the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="d28b9-p127">즉, Azure 저장소 영역에서 PST 파일을 삭제 하 고, 후 자신이 더이상 표시 되는지의 보안에서 완료 된 가져오기 작업에 대 한 파일 목록에서 &amp; 준수 센터입니다. 가져오기 작업 **가져오기** 페이지의 보안에 계속 표시 될 수 있습니다 있지만 &amp; 준수 센터 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p127">This also means that after PST files are deleted from the Azure storage area, they're no longer displayed in the list of files for a completed import job in the Security &amp; Compliance Center. Although an import job might still be listed on the **Import** page in the Security &amp; Compliance Center, the list of PST files might be empty when you view the details of older import jobs.</span></span> 
  
 <span data-ttu-id="d28b9-218">**PST 파일 형식의 어떤 버전은 Office 365로 가져오기에 대 한 지원 합니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-218">**What version of the PST file format is supported for importing to Office 365?**</span></span>
  
<span data-ttu-id="d28b9-p128">PST 파일 형식의 두 버전이: ANSI 및 유니코드 합니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 ANSI PST 파일 형식 더블 바이트 문자를 사용 하는 언어에 대 한 예를 사용 하는 파일 (DBCS) 설정, Office 365로 가져올 수도 있습니다. ANSI PST 파일 가져오기 (영문) 하는 방법에 대 한 자세한 내용은 [Office 365에 PST 파일을 가져오려면 전달 하는 드라이브를 사용 하 여](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file)에서 3 단계를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p128">There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. However, files that use the ANSI PST file format, such as those for languages that use a double-byte character set (DBCS), can also be imported to Office 365. For more information about importing ANSI PST files, see Step 3 in [Use drive shipping to import PST files to Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).</span></span>
  
<span data-ttu-id="d28b9-223">또한 Office 365로 Outlook 2007 및 그 이후 버전에서 PST 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-223">Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.</span></span>
  
 <span data-ttu-id="d28b9-224">**메시지 크기 제한을 PST 파일을 가져올 때 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-224">**Is there a message size limit when importing PST files?**</span></span>
  
<span data-ttu-id="d28b9-p129">예입니다. PST 파일 150MB 보다 큰 사서함 항목을 포함 하는 경우 항목 가져오기 프로세스를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p129">Yes. If a PST file contains a mailbox item that is larger than 150 MB, the item will be skipped during the import process.</span></span>
  
 <span data-ttu-id="d28b9-227">**메시지를 보내거나 받은, 받는 사람 목록과 기타 속성을 Office 365 사서함에 PST 파일을 가져올 때 유지 하는 경우와 같은 메시지 속성은?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-227">**Are message properties, such as when the message was sent or received, the list of recipients and other properties, preserved when PST files are imported to an Office 365 mailbox?**</span></span>
  
<span data-ttu-id="d28b9-p130">예입니다. 가져오기 프로세스 중에 원본 메시지 메타 데이터 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p130">Yes. The original message metadata isn't changed during the import process</span></span>
  
 <span data-ttu-id="d28b9-230">**이 사서함에 가져오려는 PST 파일에 대 한 폴더 계층 구조에 있는 수준 수에 제한이 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-230">**Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**</span></span>
  
<span data-ttu-id="d28b9-p131">예입니다. 중첩 된 폴더의 300 개 이상인 수준이 있는 PST 파일을 가져올 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p131">Yes. You can't import a PST file that has 300 or more levels of nested folders.</span></span>
  
 <span data-ttu-id="d28b9-233">**드라이브 전달을 사용 하 여 Office 365에서 비활성 사서함을 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-233">**Can I use drive shipping to import PST files to an inactive mailbox in Office 365?**</span></span>
  
<span data-ttu-id="d28b9-234">예, 이제이 기능은 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-234">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="d28b9-235">**드라이브 전달을 사용 하 여 Exchange 하이브리드 배포에서 온라인 보관 사서함을 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-235">**Can I use drive shipping to import PST files to an online archive mailbox in an Exchange hybrid deployment?**</span></span>
  
<span data-ttu-id="d28b9-236">예, 이제이 기능은 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-236">Yes, this capability is now available.</span></span>
  
 <span data-ttu-id="d28b9-237">**드라이브 전달을 사용 하 여 Exchange Online에서 공용 폴더에 PST 파일을 가져올 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-237">**Can I use drive shipping to import PST files to public folders in Exchange Online?**</span></span>
  
<span data-ttu-id="d28b9-238">아니요, 공용 폴더에는 PST 파일을 가져올 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-238">No, you can't import PST files to public folders.</span></span>
  
 <span data-ttu-id="d28b9-239">**Microsoft 본인에 게 다시 제공 될 전에 내 하드 드라이브 지우기 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-239">**Can Microsoft wipe my hard drive before they ship it back to me?**</span></span>
  
<span data-ttu-id="d28b9-p132">아니요, Microsoft 고객에 게이 제공 하기 전에 하드 드라이브를 지울 수 없습니다. 하드 드라이브 시점의 Microsoft에서 수신 되는 동일한 상태에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p132">No, Microsoft can't wipe hard drives before shipping them back to customers. Hard drives are returned to you in the same state they were in when they were received by Microsoft.</span></span>
  
 <span data-ttu-id="d28b9-242">**Microsoft 본인에 게 다시 전달 하는 대신 내 하드 드라이브를 구입 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-242">**Can Microsoft shred my hard drive instead of shipping it back to me?**</span></span>
  
<span data-ttu-id="d28b9-p133">아니요, Microsoft 하드 드라이브를 삭제할 수 없습니다. 하드 드라이브 시점의 Microsoft에서 수신 되는 동일한 상태에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p133">No, Microsoft can't destroy your hard drive. Hard drives are returned to you in the same state they were in when they were received by Microsoft.</span></span>
  
 <span data-ttu-id="d28b9-245">**어떤 courier 서비스 반환 전달에 대 한 지원 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-245">**What courier services are supported for return shipping?**</span></span>
  
<span data-ttu-id="d28b9-p134">미국 또는 유럽 고객 인 경우 Microsoft FedEx을 사용 하 여 사용자의 하드 드라이브를 반환 합니다. 다른 모든 지역에 대 한 Microsoft DHL를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p134">If you're a customer in the United States or Europe, Microsoft uses FedEx to return your hard drive. For all other regions, Microsoft uses DHL.</span></span>
  
 <span data-ttu-id="d28b9-248">**반환 운송 비용 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-248">**What are the return shipping costs?**</span></span>
  
<span data-ttu-id="d28b9-p135">운송 비용에 따라 다를 Microsoft 데이터 센터에 하드 드라이브를 전달 하는 근접 하 여 반환 합니다. Microsoft는 사용자의 하드 드라이브를 반환 하려면 FedEx 또는 DHL 계정을 청구 됩니다. 반환 배송 비용은 귀하의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p135">Return shipping costs vary, depending on your proximity to the Microsoft data center that you shipped your hard drive to. Microsoft will bill your FedEx or DHL account to return your hard drive. The cost of return shipping is your responsibility.</span></span>
  
 <span data-ttu-id="d28b9-252">**FedEx 사용자 지정 전달 등 사용자 지정 courier 배송 서비스를 사용 하 여 Microsoft에 내 하드 드라이브를 제공 하려면 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-252">**Can I use a custom courier shipping service, such as FedEx Custom Shipping, to ship my hard drive to Microsoft?**</span></span>
  
<span data-ttu-id="d28b9-253">예.</span><span class="sxs-lookup"><span data-stu-id="d28b9-253">Yes.</span></span>
  
 <span data-ttu-id="d28b9-254">**다른 국가에 내 하드 드라이브 제공 있으면는 사항이 취해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="d28b9-254">**If I have to ship my hard drive to another country, is there anything I need to do?**</span></span>
  
<span data-ttu-id="d28b9-p136">Microsoft에 제공 되는 하드 드라이브 국제 테두리를 교차 하 게 될 수 있습니다. 이 경우에 하드 드라이브와 포함 된 데이터는 가져온 및/또는 관련 법률에 따라를 내보낼 수 있는지 확인 하는 일을 담당 것입니다. 하드 드라이브를 전달 하기 전에 드라이브와 데이터 합법적으로 전달할 수 있습니다. 지정 된 Microsoft 데이터 센터를 확인 하 여 문에 확인. 이 적시에 Microsoft에 도달 하기 위해 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d28b9-p136">The hard drive that you ship to Microsoft might have to cross international borders. If this is the case, you're responsible for ensuring that the hard drive and the data it contains are imported and/or exported in accordance with the applicable laws. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the specified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.</span></span>
