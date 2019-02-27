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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: '관리자: Office 365 보안 &amp; 및 준수 센터에서 가져오기 서비스를 사용 하 여 Exchange Online의 사용자 사서함에 대 한 전자 메일 데이터 (PST 파일)를 대량으로 가져오는 방법에 대해 알아봅니다. 이 항목에서는 faq를 제공 하 고 PST 가져오기 프로세스의 작동 방식에 대해 설명 합니다.'
ms.openlocfilehash: 89aa1a351d0a9bcc70819f4b2657d04adc7599e2
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296781"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a>Overview of importing your organization PST files to Office 365

> [!NOTE]
> 이 문서는 관리자를 위한 것입니다. PST 파일을 자체 사서함으로 가져오시겠습니까? [Outlook .pst 파일에서 전자 메일, 연락처 및 일정 가져오기를](https://go.microsoft.com/fwlink/p/?LinkID=785075) 참조 하세요.

office 365 보안 &amp; 및 준수 센터의 가져오기 서비스를 사용 하 여 office 365 조직의 Exchange Online 사서함으로 PST 파일을 빠르게 대량으로 가져올 수 있습니다. PST 파일을 Office 365로 가져오는 방법에는 두 가지가 있습니다.
   
- **네트워크 업로드** ![클라우드 업로드](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) -네트워크를 통해 PST 파일을 Microsoft 클라우드의 임시 Azure 저장소 위치로 업로드 합니다. 그런 다음 office 365 가져오기 서비스를 사용 하 여 office 365 조직의 사서함으로 PST 데이터를 가져옵니다. 

- **드라이브 전달** ![하드 디스크](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) -PST 파일을 BitLocker로 암호화 된 하드 드라이브에 복사한 다음 물리적으로 Microsoft에 드라이브를 배송 합니다. microsoft는 하드 드라이브를 수신 하는 경우 데이터 센터 직원은 microsoft 클라우드의 임시 Azure 저장소 위치에 데이터를 업로드 합니다. 그런 다음 office 365 가져오기 서비스를 사용 하 여 office 365 조직의 사서함으로 데이터를 가져옵니다.

## <a name="step-by-step-instructions"></a>단계별 지침
  
조직의 PST 파일을 Office 365로 대량 가져오는 방법에 대 한 단계별 지침을 보려면 다음 항목 중 하나를 참조 하세요. 
   
- [네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기](use-network-upload-to-import-pst-files.md)
- [드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>PST 파일을 가져오는 방법

다음은 전체 PST 가져오기 프로세스에 대 한 설명입니다. 다음 그림에서는 기본 워크플로를 보여 주고 네트워크 업로드 및 드라이브 전달 방법 간의 차이점을 강조 표시 합니다.
  
![PST 가져오기 프로세스 워크플로](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **pst 가져오기 도구 및 키를 사설 Azure 저장소 위치로 다운로드** -pst 파일을 업로드 하거나 하드 드라이브에 복사 하는 데 사용 되는 도구 및 액세스 키를 다운로드 하는 첫 번째 단계입니다. Office 365 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서이를 가져옵니다. 키를 사용 하면 개인 및 안전한 Azure storage 위치에 PST 파일을 업로드 하는 데 필요한 사용 권한 (또는 드라이브 전달의 경우 Microsoft data center 직원)이 제공 됩니다. 이 선택 키는 조직에서 고유 하며, Microsoft 클라우드로 업로드 된 후에 해당 PST 파일에 대 한 무단 액세스를 방지 하는 데 도움이 됩니다. PST 파일을 Office 365로 가져오는 경우 조직에서 별도의 Azure 구독을 사용할 필요가 없습니다. 
    
2. **pst 파일 업로드 또는 복사** -다음 단계는 네트워크 업로드 또는 드라이브 전달을 사용 하 여 pst 파일을 가져올지 여부에 따라 달라 집니다. 두 경우 모두 이전 단계에서 얻은 도구 및 보안 저장소 키를 사용 합니다.
    
    - **네트워크 업로드** 1 단계에서 다운로드 한 AzCopy 도구는 Microsoft 클라우드의 Azure 저장소 위치에 PST 파일을 업로드 하 고 저장 하는 데 사용 됩니다. PST 파일을 업로드 하는 Azure 저장소 위치는 Office 365 조직이 있는 동일한 지역 Microsoft 데이터 센터에 저장 됩니다. 
    
      이를 업로드 하려면 Office 365로 가져올 PST 파일이 조직의 파일 공유 또는 파일 서버에 있어야 합니다.
    
    - **드라이브 전달** 1 단계에서 다운로드 한 waimportexport 도구는 PST 파일을 하드 드라이브에 복사 하는 데 사용 됩니다. 이 도구는 BitLocker로 하드 드라이브를 암호화 한 다음 pst를 하드 드라이브에 복사 합니다. 네트워크 업로드와 마찬가지로 하드 드라이브에 복사할 PST 파일을 조직의 파일 공유 또는 파일 서버에 배치 해야 합니다.
    
3. **pst 가져오기 매핑 파일 만들기** -pst 파일이 Azure 저장 위치로 업로드 되거나 하드 드라이브에 복사 된 후에는 pst 파일을 가져올 사용자 사서함을 지정 하는 CSV (쉼표로 구분 된 값) 파일을 만듭니다 ( nd PST 파일을 사용자의 기본 사서함 이나 보관 사서함으로 가져올 수 있습니다. Office 365 가져오기 서비스는이 정보를 사용 하 여 PST 파일을 가져옵니다. 
    
4. **pst 가져오기 작업 만들기** -다음 단계는 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서 pst 가져오기 작업을 만들고 이전 단계에서 만든 pst 가져오기 매핑 파일을 제출 하는 것입니다. 네트워크 업로드의 경우 (pst 파일이 Azure에 업로드 되었기 때문에) Office 365에서 pst 파일의 데이터를 분석 한 다음, 실제로 pst 가져오기 매핑 파일에 지정 된 사서함으로 가져오는 데이터를 제어 하는 필터를 설정할 수 있는 방법을 제공 합니다. 
    
    드라이브 전달 시에는 프로세스의이 시점에서 몇 가지 추가 작업을 수행 합니다.
    
    - microsoft 데이터 센터에 실제로 하드 드라이브를 배송 하는 경우 (가져오기 작업을 만들 때 microsoft 데이터 센터의 배송 주소가 표시 됨)
    
    - Microsoft에서 하드 드라이브를 받으면 데이터 센터 직원은 하드 드라이브에 있는 pst 파일을 조직의 Azure storage 위치에 업로드 합니다. 앞에서 설명한 것 처럼 PST 파일은 Office 365 조직이 있는 동일한 지역 Microsoft 데이터 센터에 있는 Azure 저장소 위치로 업로드 됩니다.
    
      > [!NOTE]
      > 하드 드라이브에 있는 PST 파일은 Microsoft가 하드 드라이브를 수신 하는 동안 7 일에서 영업일까지 Azure에 업로드 됩니다. 
  
      네트워크 업로드 프로세스와 마찬가지로, Office 365은 pst 파일의 데이터를 분석 하 고, 실제로 pst 가져오기 매핑 파일에 지정 된 사서함으로 가져오는 데이터를 제어 하는 필터를 설정할 수 있는 기회를 제공 합니다.
    
    - Microsoft는 하드 드라이브를 사용자에 게 다시 제공 합니다. 
    
5. **사서함으로 가져올 pst 데이터** -가져오기 작업을 만든 후에, 즉 드라이브 전달 작업에서 pst 파일을 Azure 저장 위치로 업로드 한 후에는 Office 365에서 pst 파일의 데이터를 안전 하 고 안전 하 게 분석 합니다. 항목의 보존 기간 및 PST 파일에 포함 된 다양 한 메시지 유형을 식별 합니다. 분석이 완료 되 고 데이터를 가져올 준비가 되 면 PST 파일에 포함 된 모든 데이터를 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하 여 가져온 데이터를 트리밍하는 옵션을 사용할 수 있습니다. 
    
6. **pst 가져오기 작업 시작** -가져오기 작업을 시작한 후에 Office 365은 pst 가져오기 매핑 파일의 정보를 사용 하 여 Azure 저장소 위치에서 사용자 사서함으로 pst 파일을 가져옵니다. 가져오기 작업에 대 한 상태 정보 (가져올 각 PST 파일에 대 한 정보 포함)는 보안 **** &amp; 및 준수 센터의 가져오기 페이지에 표시 됩니다. 가져오기 작업이 완료 되 면 작업 상태가 **완료**로 설정 됩니다.
  
## <a name="why-import-email-data-to-office-365"></a>전자 메일 데이터를 Office 365로 가져오는 이유는 무엇 인가요?

- PST 파일을 사용자 사서함으로 가져오는 것은 조직의 전자 메일을 Office 365로 마이그레이션하는 한 가지 방법입니다.
    
- [지능형 가져오기](filter-data-when-importing-pst-files.md) 기능을 사용 하 여 실제로 대상 사서함으로 가져온 PST 파일의 항목을 필터링 할 수 있습니다. 이렇게 하면 가져올 데이터를 제어 하는 필터를 설정 하 여 가져온 데이터를 트리밍할 수 있습니다. 
    
- 전자 메일 데이터를 Office 365로 가져오면 조직의 준수 요구 사항에 따라 다음과 같은 작업을 수행할 수 있습니다.
    
  - [보관 사서함](enable-archive-mailboxes.md) 및 [무제한 보관](unlimited-archiving.md) 을 사용 하도록 설정 하 여 사용자에 게 사서함 저장소 공간을 추가로 제공 합니다. 
    
  - 콘텐츠를 보존 하려면 사서함을 [소송 보존 상태로](https://go.microsoft.com/fwlink/?linkid=841243) 설정 합니다. 
    
  - [콘텐츠 검색 도구](content-search.md) 를 사용 하 여 사서함 콘텐츠를 검색 합니다. 
    
  - [eDiscovery 사례](ediscovery-cases.md) 를 사용 하 여 조직의 법적 조사 관리 
    
  - 보안 &amp; 및 준수 센터에서 [보존 정책을](retention-policies.md) 사용 하 여 사서함 콘텐츠가 보존 되는 기간을 제어 하 고 보존 기간이 만료 된 후에 콘텐츠를 삭제 합니다. 
    
- 데이터를 Office 365로 가져오면 데이터 손실을 방지할 수 있습니다. Office 365로 가져오는 전자 메일 데이터는 Exchange Online의 고가용성 기능을 상속 합니다.
    
- Office 365의 전자 메일 데이터는 클라우드에 저장 되므로 모든 장치에서 사용자에 게 제공 됩니다.
    
## <a name="importing-sharepoint-data-to-office-365"></a>Office 365로 SharePoint 데이터 가져오기

Office 365 조 직에서 SharePoint 사이트 및 OneDrive 계정으로 파일 및 문서를 가져올 수도 있습니다. 자세한 내용은 다음 문서를 참조 하세요.

- [SharePoint Online으로 마이그레이션](https://docs.microsoft.com/sharepointmigration/migrate-to-sharepoint-online)

- [SharePoint 마이그레이션 도구 소개](https://docs.microsoft.com/sharepointmigration/introducing-the-sharepoint-migration-tool)

- [PowerShell을 사용하여 SharePoint Online으로 마이그레이션](https://docs.microsoft.com/sharepointmigration/overview-spmt-ps-cmdlets)

- [Azure Data Box를 사용 하 여 SharePoint Online으로 파일 공유 콘텐츠 마이그레이션](https://docs.microsoft.com/sharepointmigration/how-to-migrate-file-share-content-to-spo-using-azuredatabox)


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a>PST 파일을 Office 365로 가져오는 방법에 대 한 질문과 대답
  
다음은 office 365 가져오기 서비스를 사용 하 여 PST 파일을 office 365 사서함으로 대량으로 가져오는 방법에 대 한 몇 가지 질문과 대답입니다. 
  
- [네트워크 업로드를 사용 하 여 PST 파일 가져오기](#using-network-upload-to-import-pst-files)
  
- [드라이브 전달을 사용 하 여 PST 파일 가져오기](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a>네트워크 업로드를 사용 하 여 PST 파일 가져오기

 **Office 365 가져오기 서비스에서 가져오기 작업을 만드는 데 필요한 사용 권한은 무엇입니까?**
  
PST 파일을 Office 365 사서함으로 가져오려면 Exchange Online의 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 자신 또는 다른 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하세요.
  
또한 Office 365 보안 &amp; 및 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.
  
- Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.
    
    또는
    
- Office 365 조 직의 전역 관리자 여야 합니다.
    
> [!TIP]
> Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다. 
  
 **네트워크 업로드를 사용할 수 있는 위치**
  
네트워크 업로드는 현재 미국, 캐나다, 브라질, 영국, 유럽, 인도, 동부 아시아, 동남 아시아, 일본, 한국, 호주 및 오스트레일리아에서 사용할 수 있습니다. 네트워크 업로드가 곧 더 많은 지역에서 제공 될 예정입니다.
  
 **네트워크 업로드를 사용 하 여 PST 파일을 가져오기 위한 가격은 무엇입니까?**
  
네트워크 업로드를 사용 하 여 PST 파일을 가져오는 것은 무료입니다.
  
또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 Office 365 관리 센터의 완료 된 가져오기 작업에 대 한 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 **Office로 데이터 가져오기 365** 페이지에 표시 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다. 
  
 **Office 365로 가져올 때 지원 되는 PST 파일 형식의 버전은 무엇입니까?**
  
PST 파일 형식에는 ANSI 및 Unicode의 두 가지 버전이 있습니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 DBCS (더블 바이트 문자 집합)를 사용 하는 언어와 같이 ANSI PST 파일 형식을 사용 하는 파일은 Office 365로도 가져올 수 있습니다. ANSI PST 파일을 가져오는 방법에 대 한 자세한 내용은 네트워크 업로드 사용의 4 단계에서 [PST 파일을 Office 365로 가져오기](https://go.microsoft.com/fwlink/p/?LinkId=823074)를 참조 하십시오.
  
또한 Outlook 2007 이상 버전의 PST 파일을 Office 365로 가져올 수 있습니다.
  
 **azure storage 영역에 내 PST 파일을 업로드 한 후 삭제 하기 전에 azure에 보관 되는 기간**
  
네트워크 업로드 방법을 사용 하 여 PST 파일을 가져올 때는 **ingestiondata**이라는 Azure blob 컨테이너에 업로드 합니다. 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서 가져오기 작업이 진행 중이 아니면 Azure의 **ingestiondata** 컨테이너에 있는 모든 PST 파일이 보안 &amp;준수 센터 또한 PST 파일을 Azure에 업로드 하는 30 일 이내에 보안 &amp; 및 준수 센터 (네트워크 업로드 지침의 5 단계에 설명 됨)에서 새 가져오기 작업을 만들어야 한다는 것을 의미 합니다. 
  
또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 보안 &amp; 및 준수 센터에서 완료 된 가져오기 작업의 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 보안 &amp; 준수 센터의 **가져오기** 페이지에 나열 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다. 
  
 **PST 파일을 사서함에 가져오는 데 소요 되는 시간**
  
네트워크 용량에 따라 다르지만 일반적으로 각 테라바이트 (tb)의 데이터를 조직의 Azure storage 영역에 업로드 하는 데 몇 시간 정도 걸립니다. pst 파일이 Azure storage 영역에 복사 된 후에는 pst 파일을 하루 중 24gb 이상으로 Office 365 사서함으로 가져옵니다. 이 속도가 사용자의 요구를 충족 하지 않는 경우 전자 메일 데이터를 Office 365로 마이그레이션하는 다른 방법을 고려할 수 있습니다. 자세한 내용은 [여러 전자 메일 계정을 Office 365로 마이그레이션하는 방법을](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)참조 하세요.
  
서로 다른 PST 파일을 다른 대상 사서함으로 가져오는 경우 가져오기 프로세스는 동시에 수행 됩니다. 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로 여러 PST 파일을 같은 사서함으로 가져오는 경우 동시에 가져오게 됩니다.
  
 **PST 파일을 가져올 때 메시지 크기 제한이 있나요?**
  
예로. PST 파일에 150 보다 큰 사서함 항목이 포함 되어 있으면 가져오기 프로세스 중에 해당 항목을 건너뜁니다.
  
 **메시지를 보내거나 받은 경우와 같이 PST 파일을 Office 365 사서함으로 가져올 때 받는 사람 및 기타 속성 목록이 보존 되는 메시지 속성입니다.**
  
예로. 원본 메시지 메타 데이터는 가져오기 프로세스 중에 변경 되지 않습니다.
  
 **사서함으로 가져오려는 PST 파일에 대 한 폴더 계층 구조의 수준 수에 제한이 있나요?**
  
예로. 300 개 이상의 중첩 된 폴더를 포함 하는 PST 파일은 가져올 수 없습니다.
  
 **네트워크 업로드를 사용 하 여 PST 파일을 Office 365의 비활성 사서함으로 가져올 수 있나요?**
  
예, 이제이 기능을 사용할 수 있습니다.
  
 **네트워크 업로드를 사용 하 여 Exchange 하이브리드 배포의 온라인 보관 사서함으로 PST 파일을 가져올 수 있나요?**
  
예, 이제이 기능을 사용할 수 있습니다.
  
 **네트워크 업로드를 사용 하 여 PST 파일을 Exchange Online의 공용 폴더에 가져올 수 있습니까?**
  
아니요, PST 파일을 공용 폴더로 가져올 수 없습니다.
  
### <a name="using-drive-shipping-to-import-pst-files"></a>드라이브 전달을 사용 하 여 PST 파일 가져오기

 **Office 365 가져오기 서비스에서 가져오기 작업을 만드는 데 필요한 사용 권한은 무엇입니까?**
  
PST 파일을 Office 365 사서함으로 가져오려면 사서함 가져오기 내보내기 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 자신 또는 다른 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 [Manage role groups in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688)의 "역할 그룹에 역할 추가" 또는 "역할 그룹 만들기" 섹션을 참조 하세요.
  
또한 Office 365 보안 &amp; 및 준수 센터에서 가져오기 작업을 만들려면 다음 중 하나가 충족 되어야 합니다.
  
- Exchange Online에서 Mail Recipients 역할을 할당 받아야 합니다. 기본적으로이 역할은 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.
    
    또는
    
- Office 365 조 직의 전역 관리자 여야 합니다.
    
> [!TIP]
> Exchange Online에서 PST 파일을 Office 365로 가져오는 데 특별히 만들어진 새 역할 그룹을 만드는 것이 좋습니다. PST 파일을 가져오는 데 필요한 최소 수준의 권한으로는 사서함 가져오기 내보내기 및 메일 받는 사람 역할을 새 역할 그룹에 할당 하 고 구성원을 추가 합니다. 
  
 **드라이브 배송을 사용할 수 있는 위치**
  
드라이브 전달은 미국, 캐나다, 브라질, 영국, 유럽, 인도, 동부 아시아, 동남 아시아, 일본, 한국, 호주, 오스트레일리아 이제 더 많은 지역에서 드라이브 전달을 사용할 수 있습니다.
  
 **드라이브 전달을 지 원하는 상업적 라이선스 계약은 무엇입니까?**
  
Office 365로 PST 파일을 가져오기 위한 드라이브 전달은 EA (Microsoft 엔터프라이즈 계약)를 통해 제공 됩니다. Microsoft 제품 및 서비스 계약 (mpsa)을 통해서는 드라이브 전달을 사용할 수 없습니다.
  
 **드라이브 전달을 사용 하 여 PST 파일을 Office 365로 가져올 때의 가격은 얼마 인가요?**
  
드라이브 전달을 사용 하 여 PST 파일을 Office 365 사서함으로 가져오는 비용은 데이터의 GB 당 $2 USD입니다. 예를 들어, 1000 기가바이트 (1tb)의 PST 파일을 포함 하는 하드 드라이브를 제공 하는 경우 비용은 $2000 USD입니다. 파트너와 협력 하 여 가져오기 비용을 지불 해 볼 수 있습니다. 파트너를 찾는 방법에 대 한 자세한 내용은 [Office 365 파트너 또는 대리점 찾기를](https://go.microsoft.com/fwlink/p/?LinkId=785197)참조 하세요.
  
 **드라이브 전달에 대해 지원 되는 하드 드라이브 종류는 무엇입니까?**
  
Office 365 가져오기 서비스와 함께 사용할 경우에는 2.5 인치 ssd (고체 드라이브) 또는 2.5 또는 3.5 인치 SATA II/III 내부 하드 드라이브만 지원 됩니다. 하드 드라이브는 최대 10mb까지 사용할 수 있습니다. 가져오기 작업의 경우에는 하드 드라이브의 첫 번째 데이터 볼륨만 처리 됩니다. 데이터 볼륨은 NTFS로 포맷 해야 합니다. 데이터를 하드 드라이브에 복사 하는 경우, 2.5 인치 ssd 또는 2.5 또는 3.5 인치 sata ii/iii 커넥터를 사용 하 여 직접 연결 하거나 외부 2.5 cm SSD 또는 2.5 또는 3.5 인치 sata ii/iii USB 어댑터를 사용 하 여 외부에서 연결할 수 있습니다.
  
> [!IMPORTANT]
> 기본 제공 USB 어댑터와 함께 제공 되는 외부 하드 드라이브는 Office 365 가져오기 서비스에서 지원 되지 않습니다. 또한 외부 하드 드라이브 대/소문자 내의 디스크는 사용할 수 없습니다. 외부 하드 드라이브를 배송 하지 마세요. 
  
 **단일 가져오기 작업에 사용할 수 있는 하드 드라이브는 몇 개입니까?**
  
단일 가져오기 작업에 최대 10 개의 하드 드라이브를 제공할 수 있습니다.
  
 **하드 드라이브를 배송 하 고 나 서 Microsoft 데이터 센터에 액세스 하는 데 어느 정도의 시간이 걸립니까?**
  
Microsoft 데이터 센터와 같이 하드 드라이브를 제공 하는 데 사용 하는 배송 옵션 (예:, 다음 영업일 배송, 2 일 배송 또는 지상 배달)과 같은 몇 가지 사항에 따라 달라 집니다. 대부분의 운송 업체에서는 추적 번호를 사용 하 여 배달 상태를 추적할 수 있습니다.
  
 **Microsoft 데이터 센터에 하드 드라이브가 도착 한 후 Azure에 내 PST 파일을 업로드 하는 데 얼마나 걸립니까?**
  
microsoft 데이터 센터에서 하드 드라이브를 받은 후에는 해당 조직의 microsoft Azure storage 영역에 PST 파일을 업로드 하기 위해 7 일에서 10 일까 지를 담당 합니다. PST 파일이 라는 `ingestiondata`Azure blob 컨테이너에 업로드 됩니다. 
  
 **PST 파일을 사서함에 가져오는 데 소요 되는 시간**
  
pst 파일이 Azure storage 영역에 업로드 된 후에 Office 365는 pst 파일의 데이터를 안전 하 고 안전한 방식으로 분석 하 여 항목의 보존 기간 및 pst 파일에 포함 된 다양 한 메시지 유형을 식별 합니다. 이 분석이 완료 되 면 PST 파일의 모든 데이터를 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하는 옵션을 사용할 수 있습니다. 가져오기 작업을 시작한 후에는 PST 파일을 하루 중 24gb 이상으로 Office 365 사서함으로 가져옵니다. 이 속도가 사용자의 요구를 충족 하지 않는 경우 전자 메일 데이터를 Office 365로 가져오는 다른 방법을 고려할 수 있습니다. 자세한 내용은 [여러 전자 메일 계정을 Office 365로 마이그레이션하는 방법을](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842)참조 하세요.
  
서로 다른 PST 파일을 다른 대상 사서함으로 가져오는 경우 가져오기 프로세스는 동시에 수행 됩니다. 즉, 각 PST/사서함 쌍을 동시에 가져옵니다. 마찬가지로 여러 PST 파일을 같은 사서함으로 가져오는 경우 동시에 가져오게 됩니다.
  
 **Microsoft에서 내 PST 파일을 azure로 업로드 한 후 삭제 하기 전에 azure에 보관 되는 기간**
  
조직의 Azure 저장소 위치에 있는 모든 PST 파일 (blob 컨테이너 `ingestiondata`)에서 최근 가져오기 작업은 보안 &amp; 및 준수 센터의 **가져오기** 페이지에서 만든 후 30 일이 지나면 삭제 됩니다. 
  
또한 PST 파일이 Azure storage 영역에서 삭제 된 후에는 보안 &amp; 및 준수 센터에서 완료 된 가져오기 작업의 파일 목록에 더 이상 표시 되지 않습니다. 가져오기 작업은 여전히 보안 &amp; 준수 센터의 **가져오기** 페이지에 나열 되지만 이전 가져오기 작업의 세부 정보를 볼 때 PST 파일 목록이 비어 있을 수 있습니다. 
  
 **Office 365로 가져올 때 지원 되는 PST 파일 형식의 버전은 무엇입니까?**
  
PST 파일 형식에는 ANSI 및 Unicode의 두 가지 버전이 있습니다. 유니코드 PST 파일 형식을 사용 하는 파일을 가져오는 것이 좋습니다. 그러나 DBCS (더블 바이트 문자 집합)를 사용 하는 언어와 같이 ANSI PST 파일 형식을 사용 하는 파일은 Office 365로도 가져올 수 있습니다. ANSI PST 파일 가져오기에 대 한 자세한 내용은 on [drive 발송을 사용 하 여 조직 PST 파일을 Office 365로 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file)의 3 단계를 참조 하십시오.
  
또한 Outlook 2007 이상 버전의 PST 파일을 Office 365로 가져올 수 있습니다.
  
 **PST 파일을 가져올 때 메시지 크기 제한이 있나요?**
  
예로. PST 파일에 150 보다 큰 사서함 항목이 포함 되어 있으면 가져오기 프로세스 중에 해당 항목을 건너뜁니다.
  
 **메시지를 보내거나 받은 경우와 같이 PST 파일을 Office 365 사서함으로 가져올 때 받는 사람 및 기타 속성 목록이 보존 되는 메시지 속성입니다.**
  
예로. 원본 메시지 메타 데이터는 가져오기 프로세스 중에 변경 되지 않습니다.
  
 **사서함으로 가져오려는 PST 파일에 대 한 폴더 계층 구조의 수준 수에 제한이 있나요?**
  
예로. 300 개 이상의 중첩 된 폴더를 포함 하는 PST 파일은 가져올 수 없습니다.
  
 **Office 365에서 드라이브 전달을 사용 하 여 PST 파일을 비활성 사서함으로 가져올 수 있나요?**
  
예, 이제이 기능을 사용할 수 있습니다.
  
 **드라이브 전달을 사용 하 여 PST 파일을 Exchange 하이브리드 배포의 온라인 보관 사서함으로 가져올 수 있나요?**
  
예, 이제이 기능을 사용할 수 있습니다.
  
 **드라이브 전달을 사용 하 여 PST 파일을 Exchange Online의 공용 폴더로 가져올 수 있나요?**
  
아니요, PST 파일을 공용 폴더로 가져올 수 없습니다.
  
 **Microsoft에서 내 하드 드라이브를 초기화 한 후에 다시 출하 됩니까?**
  
아니요, Microsoft는 고객에 게 다시 배송 하기 전에 하드 드라이브를 제거할 수 없습니다. 하드 드라이브를 Microsoft에서 받은 것과 같은 상태로 되돌립니다.
  
 **Microsoft에서 내 하드 드라이브를 다시 배송 하지 않고 shred 수 있습니까?**
  
아니요, Microsoft에서 하드 드라이브를 삭제할 수 없습니다. 하드 드라이브를 Microsoft에서 받은 것과 같은 상태로 되돌립니다.
  
 **반품 상품을 위해 지원 되는 courier services는 무엇 인가요?**
  
미국 또는 유럽의 고객 인 경우 Microsoft는 FedEx을 사용 하 여 하드 드라이브를 반환 합니다. 다른 모든 지역에 대해 Microsoft는 DHL를 사용 합니다.
  
 **반품 배송 비용은 얼마 입니까?**
  
반품 비용은 하드 드라이브를 전달한 Microsoft 데이터 센터에 따라 달라 집니다. Microsoft는 하드 드라이브를 반환 하기 위해 FedEx 또는 DHL 계정을 청구할 것입니다. 반품 비용은 귀하의 책임입니다.
  
 **FedEx 사용자 지정 운송과 같은 사용자 지정 courier 선적 서비스를 사용 하 여 Microsoft에 하드 드라이브를 제공할 수 있나요?**
  
예.
  
 **하드 드라이브를 다른 국가로 배송 해야 하는 경우에는 필요한 모든 작업을 수행 해야 하나요?**
  
Microsoft에 제공 하는 하드 드라이브는 해외 테두리를 교차 해야 할 수도 있습니다. 이 경우 해당 하는 법률에 따라 하드 드라이브와 해당 파일에 포함 된 데이터를 가져오고/또는 내보내도록 합니다. 하드 드라이브를 출시 하기 전에 관리자에 게 문의 하 여 드라이브 및 데이터가 지정 된 Microsoft 데이터 센터로 합법적으로 전달 될 수 있는지 확인 합니다. 이렇게 하면 Microsoft에 적시에 도달 하는 것을 방지할 수 있습니다.
