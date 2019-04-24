---
title: PST 파일을 Office 365로 가져오기에 대 한 FAQ
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 2fe71b05-f5a2-4182-ade7-4dc5cabdfd51
description: 'office 365 가져오기 서비스를 사용 하 여 office 365 사서함으로 organizaiton의 PST 파일을 가져오는 관리자에 대 한 질문과 대답을 자주 묻는 질문입니다. '
ms.openlocfilehash: 69767353a574336351b01fdc42a9c6117c5c31ed
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255436"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a>PST 파일을 Office 365로 가져오기에 대 한 FAQ

**이 문서는 관리자를 위한 것입니다. PST 파일을 자체 사서함으로 가져오시겠습니까? [Outlook .pst 파일에서 전자 메일, 연락처 및 일정 가져오기를](https://go.microsoft.com/fwlink/p/?LinkID=785075) 참조 하세요.**|
   
다음은 office 365 가져오기 서비스를 사용 하 여 PST 파일을 office 365 사서함으로 대량으로 가져오는 방법에 대 한 몇 가지 질문과 대답입니다. pst 파일을 가져오는 방법에 대 한 자세한 내용은 [pst 파일을 Office 365로 가져오기 개요](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84)를 참조 하세요.
  
## <a name="using-network-upload-to-import-pst-files"></a>네트워크 업로드를 사용 하 여 PST 파일 가져오기

단계별 지침은 [네트워크 업로드를 사용 하 여 PST 파일을 Office 365에 가져오기](use-network-upload-to-import-pst-files.md)를 참조 하세요.
  
 **Office 365 가져오기 서비스에서 가져오기 작업을 만드는 데 필요한 사용 권한은 무엇입니까?**
  
PST 파일을 Office 365 사서함으로 가져오려면 Exchange Online의 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. 자세한 내용은 [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하세요.
  
또한 보안 & 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.
  
- Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    또는
    
- Office 365 조 직의 전역 관리자 여야 합니다.
    
> [!TIP]
> Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다. 
  
 **네트워크 업로드를 사용할 수 있는 위치**
  
네트워크 업로드는 현재 미국, 캐나다, 브라질, 미국령, 프랑스, 유럽, 인도, 동부 아시아, 동남 아시아, 일본, 미국 및 오스트레일리아에서 사용할 수 있습니다. Network upload will be available in more regions soon.
  
 **What is the pricing for importing PST files by using network upload?**
  
Using network upload to import PST files is free.
  
또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 Microsoft 365 관리 센터의 완료 된 가져오기 작업에 대 한 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 **Office로 데이터 가져오기 365** 페이지에 표시 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다. 
  
 **What version of the PST file format is supported for importing to Office 365?**
  
There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. 그러나 DBCS (더블 바이트 문자 집합)를 사용 하는 언어와 같이 ANSI PST 파일 형식을 사용 하는 파일은 Office 365로도 가져올 수 있습니다. ANSI PST 파일 가져오기에 대 한 자세한 내용은 네트워크 업로드 사용의 4 단계에서 [조직의 PST 파일을 Office 365로 가져오기](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file)를 참조 하십시오.
  
Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.
  
 **azure storage 영역에 내 PST 파일을 업로드 한 후 삭제 하기 전에 azure에 보관 되는 기간**
  
네트워크 업로드 방법을 사용 하 여 PST 파일을 가져올 때는 **ingestiondata**이라는 Azure blob 컨테이너에 업로드 합니다. 보안 & 준수 센터의 **가져오기** 페이지에서 진행 중인 가져오기 작업이 없는 경우 Azure의 **ingestiondata** 컨테이너에 있는 모든 PST 파일은 보안 &에서 가장 최근 가져온 작업을 만든 후 30 일이 지나면 삭제 됩니다. 준수 센터 또한 PST 파일을 Azure에 업로드 하는 30 일 이내에 보안 & 준수 센터 (네트워크 업로드 지침의 5 단계에 설명 됨)에서 새 가져오기 작업을 만들어야 한다는 것을 의미 합니다. 
  
또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 보안 & 준수 센터의 완료 된 가져오기 작업에 대 한 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 Security & 준수 센터의 **가져오기** 페이지에 나열 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다. 
  
 **PST 파일을 사서함에 가져오는 데 소요 되는 시간**
  
It depends on the capacity of your network, but it typically takes several hours for each terabyte (TB) of data to be uploaded to the Azure storage area for your organization. pst 파일이 Azure storage 영역에 복사 된 후에는 pst 파일을 하루 중 24gb 이상으로 Office 365 사서함으로 가져옵니다. 이 속도가 사용자의 요구를 충족 하지 않는 경우 전자 메일 데이터를 Office 365로 마이그레이션하는 다른 방법을 고려할 수 있습니다. 자세한 내용은 [여러 전자 메일 계정을 Office 365로 마이그레이션하는 방법을](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)참조 하세요.
  
If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. 마찬가지로 여러 PST 파일을 같은 사서함으로 가져오는 경우 동시에 가져오게 됩니다.
  
 **Is there a message size limit when importing PST files?**
  
예. PST 파일에 150 보다 큰 사서함 항목이 포함 되어 있으면 가져오기 프로세스 중에 해당 항목을 건너뜁니다.
  
 **메시지를 보내거나 받은 경우와 같이 PST 파일을 Office 365 사서함으로 가져올 때 받는 사람 및 기타 속성 목록이 보존 되는 메시지 속성입니다.**
  
예. 원본 메시지 메타 데이터는 가져오기 프로세스 중에 변경 되지 않습니다.
  
 **Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**
  
Yes. You can't import a PST file that has 300 or more levels of nested folders.
  
 **Can I use network upload to import PST files to an inactive mailbox in Office 365?**
  
Yes, this capability is now available. 
  
 **Can I use network upload to import PST files to an online archive mailbox in an Exchange hybrid deployment?**
  
Yes, this capability is now available. 
  
 **네트워크 업로드를 사용 하 여 PST 파일을 Exchange Online의 공용 폴더에 가져올 수 있습니까?**
  
아니요, PST 파일을 공용 폴더로 가져올 수 없습니다.
  
## <a name="using-drive-shipping-to-import-pst-files"></a>드라이브 전달을 사용 하 여 PST 파일 가져오기

단계별 지침은 [drive 발송을 사용 하 여 PST 파일을 Office 365에 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md)를 참조 하세요.
  
 **Office 365 가져오기 서비스에서 가져오기 작업을 만드는 데 필요한 사용 권한은 무엇입니까?**
  
PST 파일을 Office 365 사서함으로 가져오려면 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. 자세한 내용은 [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하세요.
  
또한 보안 & 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.
  
- Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    또는
    
- Office 365 조 직의 전역 관리자 여야 합니다.
    
> [!TIP]
> Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다. 
  
 **드라이브 배송을 사용할 수 있는 위치**
  
드라이브 전달은 미국, 캐나다, 브라질, 영국, 유럽, 인도, 동부 아시아, 동남 아시아, 일본, 한국, 호주, 오스트레일리아 Drive shipping will be available in more regions soon.
  
 **What commercial licensing agreements support drive shipping?**
  
Office 365로 PST 파일을 가져오기 위한 드라이브 전달은 EA (Microsoft 엔터프라이즈 계약)를 통해 제공 됩니다. Microsoft 제품 및 서비스 계약 (mpsa)을 통해서는 드라이브 전달을 사용할 수 없습니다.
  
 **드라이브 전달을 사용 하 여 PST 파일을 Office 365로 가져올 때의 가격은 얼마 인가요?**
  
The cost to use drive shipping to import PST files to Office 365 mailboxes is $2 USD per GB of data. For example, if you ship a hard drive that contains 1,000 GB (1 TB) of PST files, the cost is $2,000 USD. You can work with a partner to pay the import fee. 파트너를 찾는 방법에 대 한 자세한 내용은 [Office 365 파트너 또는 대리점 찾기를](https://go.microsoft.com/fwlink/p/?LinkId=785197)참조 하세요.
  
 **What kind of hard drives are supported for drive shipping?**
  
Office 365 가져오기 서비스와 함께 사용할 경우에는 2.5 인치 ssd (고체 드라이브) 또는 2.5 또는 3.5 인치 SATA II/III 내부 하드 드라이브만 지원 됩니다. You can use hard drives up to 10 TB. 가져오기 작업의 경우에는 하드 드라이브의 첫 번째 데이터 볼륨만 처리 됩니다. The data volume must be formatted with NTFS. 데이터를 하드 드라이브에 복사 하는 경우, 2.5 인치 ssd 또는 2.5 또는 3.5 인치 sata ii/iii 커넥터를 사용 하 여 직접 연결 하거나 외부 2.5 cm SSD 또는 2.5 또는 3.5 인치 sata ii/iii USB 어댑터를 사용 하 여 외부에서 연결할 수 있습니다.
  
> [!IMPORTANT]
> 기본 제공 USB 어댑터와 함께 제공 되는 외부 하드 드라이브는 Office 365 가져오기 서비스에서 지원 되지 않습니다. Additionally, the disk inside the casing of an external hard drive can't be used. Please don't ship external hard drives. 
  
 **How many hard drives can I ship for a single import job?**
  
You can ship a maximum of 10 hard drives for a single import job.
  
 **After I ship my hard drive, how long does it take to get to the Microsoft data center?**
  
That depends on a few things, such as your proximity to the Microsoft data center and what kind of shipping option you used to ship your hard drive (such as, next-day delivery, two-day delivery, or ground-delivery). With most shippers, you can use the tracking number to track the status of your delivery.
  
 **Microsoft 데이터 센터에 하드 드라이브가 도착 한 후 Azure에 내 PST 파일을 업로드 하는 데 얼마나 걸립니까?**
  
microsoft 데이터 센터에서 하드 드라이브를 받은 후에는 해당 조직의 microsoft Azure storage 영역에 PST 파일을 업로드 하기 위해 7 일에서 10 일까 지를 담당 합니다. PST 파일이 **ingestiondata**라는 Azure blob 컨테이너에 업로드 됩니다. 
  
 **PST 파일을 사서함에 가져오는 데 소요 되는 시간**
  
pst 파일이 Azure storage 영역에 업로드 된 후에 Office 365는 pst 파일의 데이터를 안전 하 고 안전한 방식으로 분석 하 여 항목의 보존 기간 및 pst 파일에 포함 된 다양 한 메시지 유형을 식별 합니다. 이 분석이 완료 되 면 PST 파일의 모든 데이터를 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하는 옵션을 사용할 수 있습니다. 가져오기 작업을 시작한 후에는 PST 파일을 하루 중 24gb 이상으로 Office 365 사서함으로 가져옵니다. 이 속도가 사용자의 요구를 충족 하지 않는 경우 전자 메일 데이터를 Office 365로 가져오는 다른 방법을 고려할 수 있습니다. 자세한 내용은 [여러 전자 메일 계정을 Office 365로 마이그레이션하는 방법을](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)참조 하세요.
  
If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. 마찬가지로 여러 PST 파일을 같은 사서함으로 가져오는 경우 동시에 가져오게 됩니다.
  
 **Microsoft에서 내 PST 파일을 azure로 업로드 한 후 삭제 하기 전에 azure에 보관 되는 기간**
  
조직의 Azure 저장소 위치에 있는 모든 PST 파일 ( **ingestiondata** 이라는 blob 컨테이너)은 보안 & 준수 센터의 **가져오기** 페이지에서 최근 가져오기 작업을 만든 후 30 일이 지나면 삭제 됩니다. 
  
또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 보안 & 준수 센터의 완료 된 가져오기 작업에 대 한 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 Security & 준수 센터의 **가져오기** 페이지에 나열 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다. 
  
 **What version of the PST file format is supported for importing to Office 365?**
  
There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. 그러나 DBCS (더블 바이트 문자 집합)를 사용 하는 언어와 같이 ANSI PST 파일 형식을 사용 하는 파일은 Office 365로도 가져올 수 있습니다. ANSI PST 파일을 가져오는 방법에 대 한 자세한 내용은 on [drive 발송을 사용 하 여 PST 파일을 Office 365로 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file)의 3 단계를 참조 하세요.
  
Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.
  
 **Is there a message size limit when importing PST files?**
  
예. PST 파일에 150 보다 큰 사서함 항목이 포함 되어 있으면 가져오기 프로세스 중에 해당 항목을 건너뜁니다.
  
 **메시지를 보내거나 받은 경우와 같이 PST 파일을 Office 365 사서함으로 가져올 때 받는 사람 및 기타 속성 목록이 보존 되는 메시지 속성입니다.**
  
예. 원본 메시지 메타 데이터는 가져오기 프로세스 중에 변경 되지 않습니다.
  
 **Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**
  
Yes. You can't import a PST file that has 300 or more levels of nested folders.
  
 **Can I use drive shipping to import PST files to an inactive mailbox in Office 365?**
  
Yes, this capability is now available.
  
 **Can I use drive shipping to import PST files to an online archive mailbox in an Exchange hybrid deployment?**
  
Yes, this capability is now available. 
  
 **드라이브 전달을 사용 하 여 PST 파일을 Exchange Online의 공용 폴더로 가져올 수 있나요?**
  
아니요, PST 파일을 공용 폴더로 가져올 수 없습니다.
  
 **Can Microsoft wipe my hard drive before they ship it back to me?**
  
No, Microsoft can't wipe hard drives before shipping them back to customers. Hard drives are returned to you in the same state they were in when they were received by Microsoft.
  
 **Microsoft에서 내 하드 드라이브를 다시 배송 하지 않고 shred 수 있습니까?**
  
No, Microsoft can't destroy your hard drive. Hard drives are returned to you in the same state they were in when they were received by Microsoft.
  
 **반품 상품을 위해 지원 되는 courier services는 무엇 인가요?**
  
If you're a customer in the United States or Europe, Microsoft uses FedEx to return your hard drive. For all other regions, Microsoft uses DHL.
  
 **반품 배송 비용은 얼마 입니까?**
  
Return shipping costs vary, depending on your proximity to the Microsoft data center that you shipped your hard drive to. Microsoft will bill your FedEx or DHL account to return your hard drive. The cost of return shipping is your responsibility.
  
 **FedEx 사용자 지정 운송과 같은 사용자 지정 courier 선적 서비스를 사용 하 여 Microsoft에 하드 드라이브를 제공할 수 있나요?**
  
예.
  
 **If I have to ship my hard drive to another country, is there anything I need to do?**
  
The hard drive that you ship to Microsoft might have to cross international borders. If this is the case, you're responsible for ensuring that the hard drive and the data it contains are imported and/or exported in accordance with the applicable laws. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the specified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.
