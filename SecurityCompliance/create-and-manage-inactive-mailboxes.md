---
title: Office 365에서 비활성 사서함 만들기 및 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 296a02bd-ebde-4022-900e-547acf38ddd7
description: 사서함을 보류 또는 Office 365 보존 정책을 적용 한 후 해당 하는 Office 365 사용자 계정의 삭제 하 여 Office 365에서 비활성 사서함을 만들 수 있습니다. 비활성 사서함의 항목은 비활성 적용 되기 전에에 적용 된 보존 또는 보존 정책의 기간에 대 한 보관 됩니다. 비활성 사서함을 영구적으로 삭제 하려면 방금 보류 또는 보존 정책을 제거 합니다.
ms.openlocfilehash: de67068ded30f63e46a8a94c1030d45a12b56a2e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29740840"
---
# <a name="create-and-manage-inactive-mailboxes-in-office-365"></a>Office 365에서 비활성 사서함 만들기 및 관리

Office 365를 사용 하면 삭제 된 사서함의 내용을 유지할 수 있습니다. 이 기능을 [비활성 사서함](inactive-mailboxes-in-office-365.md)을 호출 합니다. 비활성 사서함을 사용 하면 조직 남기기 후 이전 직원의 전자 메일을 보존 합니다. 사서함이 소송 보존 또는 Office 365 보존 정책 때 비활성화 (Office 365 보안에서 만든 &amp; 준수 센터) 해당 Office 365 사용자 계정이 삭제 되기 전에 사서함에 적용 됩니다. 비활성 사서함의 내용은 비활성 적용 되기 전에 사서함에 배치 된 보류의 기간에 대 한 보관 됩니다. 이 통해 관리자, 규정 준수 관리자 및 레코드 관리자 보안에서 콘텐츠 검색을 사용 하 여 &amp; 준수 센터 검색 하 고 비활성 사서함의 내용을 내보냅니다. 비활성 사서함 전자 메일을 수신할 수 없음 및 조직의 공유 주소록 또는 다른 목록에 표시 되지 않습니다.
  
> [!NOTE]
> 사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 사서함을 비활성화 하려면, 할당 되어야 합니다 Exchange Online 계획 2 라이선스 소송 보존 또는 Office 365 보존 정책을 삭제 하기 전에 사서함에 적용 될 수 있도록 합니다. Exchange Online 계획 2 라이선스를 사용 하면 한 Office 365 엔터프라이즈 E3 및 e 5 구독에 속합니다. 사서함 (즉, 부분에서는 Office 365 Enterprise E1 구독) Exchange Online 계획 1 라이선스를 할당 되 면 보류 삭제 되기 전에 사서함에 적용 될 수 있도록 별도 Exchange Online 보관 라이선스 할당 해야 합니다. 자세한 내용은 [Exchange Online Archiving](https://go.microsoft.com/fwlink/p/?LinkId=286153)을 참조 하십시오.
    
- 해당 하는 Office 365 사용자 계정을 삭제 한 후 삭제 된 Exchange Online 사서함에 연결 된 라이선스를 사용할 수 있습니다. 그런 다음 [비즈니스를 위한 Office 365에서 사용자에 게 라이선스 할당](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) 다른 사용자에 게 있습니다. 
    
- 소송 보존 또는 Office 365 보존 정책을 삭제 하기 전에 사서함에 적용 되지 않습니다, 하는 경우 사서함의 내용을 보존 또는 검색할 수 없습니다. 삭제 된 사서함의 삭제, 30 일 이내에 복구할 수 있는 하지만 사서함 및 해당 콘텐츠를 영구적으로 삭제 됩니다 30 일 후 복구 되지 않습니다.
    
- 소송 보존으로 설정 하는 방법에 대 한 자세한 내용은 [원본 위치 유지 및 소송 보존](https://go.microsoft.com/fwlink/p/?LinkId=846124)을 참조 하십시오. 보안에서 Office 365 보존 정책에 대 한 자세한 내용은 &amp; 준수 센터 [Office 365의 보존 정책 개요](retention-policies.md)를 참조 하십시오.
  
## <a name="create-an-inactive-mailbox"></a>비활성 사서함 만들기

사서함을 비활성 만들기는 두 단계로: 1)의 사서함을 배치 소송 보존으로 설정 하거나는 Office 365 보존 정책을 적용 하 고, 2) 사서함을 삭제 하는 중에 또는 해당 Office 365 사용자 계정입니다. 사서함 활성화 되 면 해당 내용은 보류 또는 보존 정책이 제거 될 때까지 유지 됩니다.
  
### <a name="step-1-place-a-mailbox-on-litigation-hold-or-apply-an-office-365-retention-policy"></a>1 단계: 소송 보존에 배치 하는 사서함 또는 Office 365 보존 정책 적용

사서함을 소송 보존으로 설정 하거나 Office 365 보존 정책 적용 삭제 되기 전에 사서함의 내용을 유지 합니다. 두 유형의 보류 삭제 된 항목 및 수정 된 항목의 원래 버전을 포함 하 여 모든 사서함 콘텐츠를 유지 합니다. 비활성 사서함에 적용 되는 보류 또는 보존 정책을 제거 하 여 비활성 사서함을 영구적으로 삭제 될 때까지 또는 지정된 된 기간에 대 한 항목을 삭제 하 고 수정 된 비활성 사서함에 유지 됩니다.
  
보류 된 사서함에 이미 배치 되어 또는 사서함에는 Office 365 보존 정책을 이미 적용 한 경우 다음 작업을 수행 하기 됩니다 2 단계에서에서 설명한 것 처럼 해당 Office 365 사용자 계정을 삭제 합니다.
  
사서함을 소송 보존으로 설정 하거나 Office 365 보존 정책 적용에 대 한 단계별 절차를 참조 합니다.
  
- [사서함을 소송 자료 보존으로 설정](https://go.microsoft.com/fwlink/?linkid=856286)
    
- [Office 365의 보존 정책 개요](retention-policies.md)
    
> [!NOTE]
> 소송 보존을 포함 하 고 및 Office 365 보존 정책에 대 한 무기한 보류를 만들 수도 있고 대기 시간 기반 키를 누릅니다. 무기한 보존 설정에서 비활성 사서함의 내용을 무한대로 유지 됩니다 또는 보존 기간이 변경 되는 보존이 제거 될 때까지 또는까지 합니다. 보류 또는 보존 정책 (가정 하 고 사서함 30 일 보다 삭제 된)를 제거한 후 비활성 사서함을 영구적으로 삭제에 대 한 표시 됩니다 및 사서함의 내용을 더이상 보존 또는 검색할 수 없습니다. 시간 기반 보존 또는 Office 365 보존 정책에서 보류의 길이 지정합니다. 이 기간 항목 당 별로 이며 사서함 항목을 받은 되었거나 만들어진 날짜부터 계산 됩니다. 보류를 만료 되 면 사서함 항목에 대 한 항목을 나타내는 이동 또는 비활성 사서함의 복구 가능한 항목 폴더에 있는 한 후 해당 항목은 영구적으로 삭제 (비우기) 비활성 사서함에서 삭제 된 항목 보존 기간이 만료 후. 
  
### <a name="step-2-delete-the-mailbox"></a>2단계: 사서함 삭제

사서함은 대기 상태에 놓일을 사용 하거나 후는 Office 365 보존 정책을 적용할 사서함을 삭제 하려면 다음 단계가입니다. 사서함을 삭제 하는 가장 좋은 방법은 Office 365 관리 센터에서 해당 하는 Office 365 사용자 계정을 삭제 하려면 됩니다. Office 365 사용자 계정을 삭제 하는 방법에 대 한 정보를 [조직에서 사용자 삭제](https://support.office.com/article/d5155593-3bac-4d8d-9d8b-f4513a81479e)를 참고 하십시오.
  
> [!NOTE]
> Exchange Online PowerShell에서 **Remove-mailbox** cmdlet을 사용 하 여 사서함을 삭제할 수도 있습니다. 자세한 내용은 [Exchange Online 사용자 사서함을 복원 또는 삭제](https://go.microsoft.com/fwlink/?linkid=856287)를 참조 하십시오. 
  

## <a name="view-a-list-of-inactive-mailboxes"></a>비활성 사서함의 목록 보기


조직에서 비활성 사서함 목록을 보려면
  
1. 이동 [https://protection.office.com/](https://protection.office.com/) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다. 
    
2. 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> * * 보존 * *.
    
3. **보존** 페이지에서 **자세히**를 클릭![탐색 모음 타원](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif), **비활성 사서함**을 차례로 클릭 하 고 있습니다.
    
    ![보존 페이지에서 자세히를 클릭 하 고 비활성 사서함 목록을 표시 하려면 비활성 사서함을 클릭 한 다음](media/761bd90c-3e37-48f9-b1b9-479e90fea267.png)
  
    **비활성 사서함** 페이지가 표시 됩니다. 참고 하면 조직에서 비활성 사서함의 총 수에 표시 됩니다. 
    
    ![조직에서 모든 비활성 사서함의 목록이 표시 됩니다.](media/57d9d183-0c6c-4bd8-82e7-115f7b7b6de7.png)
  
또는 실행할 수도 있습니다 다음 명령은 Exchange 온라인 비활성 사서함 목록을 표시 하는 PowerShell 합니다.

```
 Get-Mailbox -InactiveMailboxOnly | FT DisplayName,PrimarySMTPAddress,WhenSoftDeleted
```

클릭 수 ![내보내기 검색 결과 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **내보내기** 를 보거나 조직에서 비활성 사서함에 대 한 추가 정보가 포함 된 CSV 파일을 다운로드 합니다. 
  
비활성 사서함의 목록 및 기타 정보를 CSV 파일로 내보내려면 다음 명령을 실행할 수도 있습니다. 이 예제에서는 현재 디렉터리에 CSV 파일이 만들어집니다.

```
Get-Mailbox -InactiveMailboxOnly | Select Displayname,PrimarySMTPAddress,DistinguishedName,ExchangeGuid,WhenSoftDeleted | Export-Csv InactiveMailboxes.csv -NoType
```
   
> [!NOTE]
> 것을 비활성 사서함 활성 사용자 사서함으로 동일한 SMTP 주소를 할 수도 있습니다. 이 경우 비활성 사서함을 고유 하 게 식별 하는 **고유 이름** 또는 **ExchangeGuid** 속성의 값을 사용할 수 있습니다. 
  
## <a name="search-and-export-the-contents-of-an-inactive-mailbox"></a>검색 및 비활성 사서함의 내용을 내보내기

보안에서 콘텐츠 검색 도구를 사용 하 여 비활성 사서함의 내용에 액세스할 수 있습니다 &amp; 준수 센터입니다. 비활성 사서함을 검색 하는 경우에 특정 항목에 대 한 검색 키워드 검색 쿼리를 만들 수 있습니다 또는 비활성 사서함의 전체 콘텐츠를 반환할 수 있습니다. 검색 결과 미리 보고 하거나 Outlook 데이터 (PST) 파일 또는 개별 전자 메일 메시지로 검색 결과 내보낼 수 있습니다. 사서함을 검색 하 고 검색 결과 내보내기 (영문)에 대 한 단계별 절차에 대 한 다음 항목을 참조 합니다.
  
- [Office 365의에서 콘텐츠 검색](content-search.md)
    
- [Office 365 보안에서 콘텐츠 검색 결과 내보낼 &amp; 준수 센터](export-search-results.md)
    
다음은 비활성 사서함을 검색할 때 주의 해야할 사항입니다.
  
- 콘텐츠 검색 사용자 사서함을 포함 하는 경우 해당 사서함 그런 다음 비활성 이루어집니다 비활성 하 게 되 면 검색을 다시 실행 하는 경우 비활성 사서함을 검색 하는 콘텐츠 검색을 계속 됩니다.
    
- 일부 경우에는 사용자는 활성 사서함과 동일한 SMTP 주소를가지고 있는 비활성 사서함 있을 수 있습니다. 이 경우 콘텐츠 검색에 대 한 위치도를 선택 하면 특정 사서함만 검색 됩니다. 즉, 검색 하는 사용자의 사서함을 추가 하는 경우 가정할 수 없습니다는 자신의 활성 및 비활성 사서함 검색 됩니다 되지 않습니다. 검색에 명시적으로 추가 하는 사서함을 검색 합니다.
    
- 활성 사서함과 동일한 SMTP 주소를 사용 하 여 비활성 사서함 필요 하지 못하도록 하는 것이 좋습니다. 비활성 사서함을 복구 하거나 활성 사서함이 있는 (또는 활성 사서함의 보관) 비활성 사서함의 내용을 복원 하는 다음 삭제를 권장 비활성 사서함에 현재 할당 된 SMTP 주소를 다시 사용 해야하는 경우는 비활성 사서함입니다.
    
## <a name="change-the-hold-duration-for-an-inactive-mailbox"></a>비활성 사서함의 유지 보존 기간 변경

사서함 비활성 이루어진 후에 보류 또는 비활성 사서함에 적용 되는 Office 365 보존 정책을의 기간을 변경할 수 있습니다. 단계별 절차에 대 한 [변경을 Office 365에서 비활성 사서함에 대 한 보존 기간을](change-the-hold-duration-for-an-inactive-mailbox.md)참조 합니다.
  
## <a name="recover-an-inactive-mailbox"></a>비활성 사서함 복구

이전 직원이 조직에 반환 하는 경우 또는 이전된 직원의 직무에 적용할 새 직원 고용 하는 경우 비활성 사서함의 내용을 복구할 수 있습니다. 비활성 사서함을 복구 하는 경우 사서함 새 사서함으로 변환 됩니다 내용과 비활성 사서함의 폴더 구조 유지 되므로 및 사서함을 새 사용자 계정에 연결 됩니다. 복구한 후 비활성 사서함 존재 하지 않습니다. 단계별 절차 및 방법에 대 한 자세한 내용은 비활성 사서함을 복구 하는 경우 수행 되는, [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)참조 합니다.
  
## <a name="restore-the-contents-of-an-inactive-mailbox-to-another-mailbox"></a>비활성 사서함의 내용을 다른 사서함 복원

이전 직원의 직무에 가져와 다른 직원 또는 다른 사람을 비활성 사서함의 내용에 대 한 액세스를 요구 하는 경우 사용자 수 복원 (또는 병합) 기존 사서함을 비활성 사서함의 내용을 합니다. 비활성 사서함을 복원 하는 경우에 내용은 다른 사서함에 복사 됩니다. 비활성 사서함은 유지 하 고 비활성 사서함을 유지 됩니다. 비활성 사서함 여전히 검색 가능한 eDiscovery를 사용 하 여, 다른 사서함의 내용을 복원할 수 또는 복구 되거나 나중에 삭제 될 수 있습니다. 단계별 절차에 대 한 [Office 365에서 비활성 사서함 복원](restore-an-inactive-mailbox.md)을 참조 하십시오.
  
## <a name="delete-an-inactive-mailbox"></a>비활성 사서함 삭제

더이상 비활성 사서함의 내용을 유지 해야하는 경우에 보류를 제거 하거나 비활성 사서함에 적용 되는 Office 365 보존 정책을 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 없습니다. 사서함에서 30 일이 경과, 삭제 된 경우 사서함 보류를 제거 하 고 사서함을 복구할 수 없는 될 후 영구적으로 삭제에 대 한 표시 됩니다. 지난 30 일, 삭제 된 사서함 하는 경우 보류 또는 보존 정책을 제거한 후 사서함을 복구할 수 있습니다. 보류 또는 비활성 사서함을 영구적으로 삭제 하는 Office 365 보존 정책을 제거 하기 위한 단계별 절차에 대 한 [Office 365에서 비활성 사서함 삭제](delete-an-inactive-mailbox.md)를 참조 합니다.