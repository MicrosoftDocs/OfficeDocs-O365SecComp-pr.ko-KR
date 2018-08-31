---
title: Exchange Online으로 대량 가져오기 외부 연락처
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: End User
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: 관리자가 Exchange Online PowerShell을 사용 하 고 CSV 파일을 대량으로 전체 주소 목록에 외부 연락처를 가져올 방법에 대해 알아봅니다.
ms.openlocfilehash: 4bde56d49ccf94dc91993df90e1ae693e25c961a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532986"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a>Exchange Online으로 대량 가져오기 외부 연락처

**이 문서는 관리자입니다. 자신의 사서함에 연락처를 가져올 하려고 합니까? [Outlook 연락처 가져오기를](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8) 참조 하십시오.**
   
회사에서 Exchange Online (전체 주소 목록) 공유 주소록에 포함 하려는 기존 고객사 연락처의 많은 게 있습니까? 회사 내부의 사용자와 수 하는 것 처럼 메일 그룹의 구성원으로 외부 연락처를 추가 하 시겠습니까? 그렇다면 Exchange Online PowerShell 및 대량을 CSV (쉼표로 구분 된 값) 파일을 사용할 수 있습니다 하는 경우 Exchange Online으로 외부 연락처를 가져옵니다. 그 다음 3 단계 프로세스로 구성 됩니다.
  
[1 단계: 외부 연락처에 대 한 정보가 포함 된 CSV 파일 만들기](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[2 단계: PowerShell을 사용한 외부 연락처 만들기](#step-2-create-the-external-contacts-with-powershell) 

[3 단계: 외부 연락처의 속성에 정보를 추가 합니다.](#step-3-add-information-to-the-properties-of-the-external-contacts)

연락처를 가져오려면 다음이 단계를 완료 한 후에 이러한 추가 작업을 수행할 수 있습니다.
  
- [더 외부 연락처를 추가 합니다.](bulk-import-external-contacts.md#AddMore)
  
- [공유 주소록에서 외부 연락처 숨기기](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a>1 단계: 외부 연락처에 대 한 정보가 포함 된 CSV 파일 만들기

첫번째 단계에서는 Exchange Online으로 가져올 수 있는 각 외부 연락처에 대 한 정보가 포함 된 CSV 파일을 만드는 것입니다. 
  
1. 메모장에서 텍스트 파일에 다음 텍스트를 복사 하 고 저장 바탕 화면에 CSV 파일로.csv, 파일 이름 접미사를 사용 하 여 예: ExternalContacts.csv 합니다.
    
    > [!TIP]
    > 하는 경우 해당 하는 언어 u t F-8 또는 메모장에서 파일을 저장 하는 경우 기타 유니코드 인코딩을 사용 하 여 CSV 파일 저장 (예: **å**, **ä**및 스웨덴어에서 **ö** )의 특수 문자를 포함 합니다. 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    첫째 행 또는 CSV 파일의 머리글 행을 Exchange Online을 가져올 때 사용할 수 있는 연락처의 속성을 나열 합니다. 각 속성 이름은 쉼표로 구분 됩니다. 각 행 머리글 행에서 단일 외부 연락처 가져오기 (영문)에 대 한 속성 값을 나타냅니다. 
    
    > [!NOTE]
    > 이 텍스트는 삭제할 수 있는 샘플 데이터를 포함 합니다. 하지만 삭제 하거나 (헤더) 행 1을 변경 하지 마십시오. 외부 연락처에 대 한 속성을 모두 포함 됩니다. 
  
2. CSV 파일을 편집 하려면 Excel을 사용 하 여 훨씬 쉽습니다 때문에 CSV 파일을 편집 하려면 Microsoft Excel에서 CSV 파일을 엽니다.
    
3. Exchange Online으로 가져올 각 연락처에 대 한 행을 만듭니다. 셀을 가능한 한 많은 채웁니다. 이 정보는 각 연락처에 대 한 공유 주소록에 표시 됩니다. 
    
    > [!IMPORTANT]
    >  (처음 네 항목이 머리글 행에)는 다음과 같은 속성은 외부 연락처를 만들 수 필요 하 고 CSV 파일에 채워야: **ExternalEmailAddress**, **이름**, **FirstName**, **LastName**합니다. 2 단계에서에서 실행 하는 PowerShell 명령에서 연락처를 만들려면 이러한 속성에 대 한 값을 사용 합니다. 

## <a name="step-2-create-the-external-contacts-with-powershell"></a>2 단계: PowerShell을 사용한 외부 연락처 만들기

다음 단계에서는 1 단계에서에서 만든 CSV 파일을 사용 하는 및 대량 하는 PowerShell을 Exchange Online CSV 파일에 나열 된 외부 연락처를 가져옵니다. 
  
1.  PowerShell Exchange Online 조직에 연결 합니다. 단계별 지침은 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하십시오. Exchange Online PowerShell에 연결할 때 Office 365 전역 관리자 계정에 대 한 사용자 이름 및 암호를 사용 해야 합니다. 
    
2. 1 단계;에서 CSV 파일을 저장 한 위치 바탕 화면 폴더로 이동 하는 PowerShell을 Exchange Online으로 연결한 후 예 `C:\Users\Administrator\desktop`합니다.
    
3. 외부 연락처를 만들려면 다음 명령을 실행 합니다.

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    가져올 수에 따라 새 연락처를 만들 하려면 시간이 걸릴 수 있습니다. 명령이 완료 되 면 실행 되 고 PowerShell 만들어진 새 대화 상대 목록이 표시 됩니다. 
    
4. 새 외부 연락처를 보려면 Exchange 관리 센터 (EAC)로 이동 하 고 **받는 사람** 을 클릭 한 다음 \> **연락처**입니다. 
    
    > [!TIP]
    > EAC에 연결 하기 위한 지침을 [Exchange 관리 센터의 Exchange Online을](https://go.microsoft.com/fwlink/p/?LinkId=328197)참조 하십시오. 
  
5. 필요한 경우 **새로 고침** 을 클릭 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 하 목록을 업데이트 하 고 가져온 외부 연락처를 참조 하십시오. 
    
    가져온된 연락처는 Outlook 및 웹에 있는 Outlook에서 공유 주소록에 표시 됩니다.
    
    > [!NOTE]
    > **사용자** 에 게 이동 하 여 Office 365 관리 센터에서 연락처를 볼 수도 있습니다 \> **연락처**입니다. 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a>3 단계: 외부 연락처의 속성에 정보를 추가 합니다.

2 단계에서에서 명령을 실행 하 고 나면 외부 연락처는 만들어지지만 CSV 파일에 있는 셀의 대부분의 정보는 대화 상대 또는 조직 정보를 포함 하지 않습니다. 즉, 새 외부 연락처를 만들 때 필요한 속성에 대해서만 채워집니다. CSV 파일에서 채워지지 모든 정보가 없는 경우 걱정 하지 마십시오. 해당 없으면 추가할 수 없습니다.
  
1.  PowerShell Exchange Online 조직에 연결 합니다. 단계별 지침은 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하십시오.
    
2. 단계 1;에서 CSV 파일을 저장 하는 바탕 화면 폴더로 이동 예 `C:\Users\Administrator\desktop`합니다.
    
3. 2 단계에서에서 만든 외부 연락처를 CSV 파일에서 다른 속성을 추가 하려면 다음의 두 명령을 실행 합니다.
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > _Manager_ 매개 변수는 문제가 발생할 수 있습니다. CSV 파일에는 셀이 비어 있으면 오류가 발생 하면 하 고 없는 속성 정보는 연락처에 추가 됩니다. 관리자를 지정 하지 않아도 하는 경우 다음 방금 삭제 ` -Manager $_.Manager ` 이전 PowerShell 명령에서 합니다. 
  
    다시 1 단계에서에서 가져온 수에 따라 여러 연락처를 업데이트 하려면 시간이 걸릴 수 있습니다. 
    
4. 속성 대화 상대에 추가 되었는지 확인. 
    
1. EAC에서 **받는 사람** \> **연락처**로 이동합니다.
    
2. 대화 상대를 클릭 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) 는 연락처의 속성을 표시 합니다. 
    
그거에요! 대화 상대와 Outlook 주소록에 대 한 추가 정보 및 웹의 Outlook에서 사용자가 볼 수 있습니다.
  
## <a name="add-more-external-contacts"></a>더 외부 연락처를 추가 합니다.

단계 1-Exchange 온라인 새 외부 연락처를 추가 하려면 3 단계를 반복할 수 있습니다. 또는 회사에서 사용자가 새 대화 상대에 대 한 CSV 파일에 새 행을 추가할 방금 수 있습니다. 그런 다음 PowerShell 명령을 만들고 새 대화 상대에 게 정보를 추가 하려면 2 단계와 3 단계에서 실행할 수 있습니다.
  
> [!NOTE]
> 새 연락처를 만들 명령을 실행 하면 이전 이미 작성 된 연락처가 존재 하 없다는 오류가 표시를 얻을 수 있습니다. 하지만 CSV 파일에 추가 하는 새 연락처가 만들어집니다. 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a>공유 주소록에서 외부 연락처 숨기기 >

일부 회사에서는 외부 연락처를 사용 하 여 메일 그룹의 구성원으로 추가할 수 있도록에 될 수 있습니다. 이 시나리오에서는 외부 연락처 공유 주소록에서 숨기려면 정의할 수 있습니다. 다음은 방법:
  
1.  PowerShell Exchange Online 조직에 연결 합니다. 단계별 지침은 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하십시오.
    
2. 단일 외부 대화 상대를 숨기려면 다음 명령을 실행 합니다.
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    예 공유 주소록에서 Pilar Pinilla를 숨기려면이 명령을 실행 합니다.

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. 공유 주소록에서 모든 외부 연락처를 숨기려면이 명령을 실행 합니다.

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

숨길 수 후 외부 연락처가 공유 주소록에 표시 되지 않습니다 있지만 메일 그룹의 구성원으로 계속 추가할 수 있습니다.
