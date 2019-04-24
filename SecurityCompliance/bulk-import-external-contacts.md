---
title: Exchange Online으로 외부 연락처 대량 가져오기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: 관리자가 Exchange Online PowerShell 및 CSV 파일을 사용 하 여 전체 주소 목록에 외부 연락처를 대량으로 가져오는 방법을 알아봅니다.
ms.openlocfilehash: 2948332d7cdf2d1364b2b563f94efdb3e8d0672d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32244509"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a>Exchange Online으로 외부 연락처 대량 가져오기

**이 문서는 관리자를 위한 것입니다. 연락처를 사용자의 사서함으로 가져오시겠습니까? [Outlook으로 연락처 가져오기를](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8) 참조 하세요.**
   
회사에서 Exchange Online의 공유 주소록 (전체 주소 목록)에 포함 하려는 기존 고객사 연락처가 많이 있습니까? 외부 연락처를 메일 그룹의 구성원으로 추가 하 시겠습니까? 회사 내부 사용자와 마찬가지로 사용 하는 것이 좋습니다. 그렇다면 exchange online PowerShell 및 CSV (쉼표로 구분 된 값) 파일을 사용 하 여 외부 연락처를 exchange online으로 대량으로 가져올 수 있습니다. 이 프로세스는 다음 세 단계로 진행 됩니다.
  
[1 단계: 외부 연락처에 대 한 정보가 포함 된 CSV 파일 만들기](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[2 단계: PowerShell을 사용 하 여 외부 연락처 만들기](#step-2-create-the-external-contacts-with-powershell) 

[3 단계: 외부 연락처의 속성에 정보 추가](#step-3-add-information-to-the-properties-of-the-external-contacts)

이러한 단계를 완료 하 여 연락처를 가져온 후에는 다음 추가 작업을 수행할 수 있습니다.
  
- [외부 연락처 추가](#add-more-external-contacts)
  
- [공유 주소록에서 외부 연락처 숨기기](#hide-external-contacts-from-the-shared-address-book)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a>1 단계: 외부 연락처에 대 한 정보가 포함 된 CSV 파일 만들기

첫 번째 단계는 Exchange Online으로 가져오려는 각 외부 연락처에 대 한 정보가 포함 된 CSV 파일을 만드는 것입니다. 
  
1. 다음 텍스트를 메모장에서 텍스트 파일로 복사 하 고 파일 이름 접미사를 사용 하 여 데스크톱에 csv 파일로 저장 합니다. 예: externalcontacts.
    
    > [!TIP]
    > 언어에 특수 문자 (예: **å**, **ä**및 **ö** )가 포함 되어 있는 경우 메모장에 파일을 저장할 때 CSV 파일을 utf-8 또는 기타 유니코드 인코딩으로 저장 합니다. 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    CSV 파일의 첫 번째 행 또는 머리글 행에는 Exchange Online으로 가져올 때 사용할 수 있는 연락처의 속성이 나열 됩니다. 각 속성 이름은 쉼표로 구분 됩니다. 머리글 행 아래의 각 행은 단일 외부 연락처를 가져오기 위한 속성 값을 나타냅니다. 
    
    > [!NOTE]
    > 이 텍스트에는 예제 데이터가 있으며 여기에 삭제할 수 있습니다. 하지만 첫 번째 (머리글) 행을 삭제 하거나 변경 하지 않습니다. 외부 연락처에 대 한 모든 속성이 포함 되어 있습니다. 
  
2. Excel을 사용 하 여 csv 파일을 편집 하는 것이 훨씬 더 쉬우므로 csv 파일을 편집 하기 위해 Microsoft excel에서 csv 파일을 엽니다.
    
3. Exchange Online으로 가져오려는 각 연락처에 대해 행을 만듭니다. 가능한 한 많은 셀을 채웁니다. 이 정보는 각 연락처에 대 한 공유 주소록에 표시 됩니다. 
    
    > [!IMPORTANT]
    >  외부 연락처를 만들려면 다음 속성 (머리글 행의 처음 네 개 항목)이 필요 하며 CSV 파일 ( **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**)에 채워야 합니다. 2 단계에서 실행 하는 PowerShell 명령은 이러한 속성의 값을 사용 하 여 연락처를 만듭니다. 

## <a name="step-2-create-the-external-contacts-with-powershell"></a>2 단계: PowerShell을 사용 하 여 외부 연락처 만들기

다음 단계에서는 1 단계 및 PowerShell에서 만든 csv 파일을 사용 하 여 csv 파일에 나열 된 외부 연락처를 Exchange Online으로 대량으로 가져옵니다. 
  
1.  Exchange Online 조직에 PowerShell을 연결 합니다. 단계별 지침은 [Exchange Online PowerShell에 연결을](https://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하십시오. Exchange Online PowerShell에 연결 하는 경우에는 Office 365 전역 관리자 계정의 사용자 이름과 암호를 사용 해야 합니다. 
    
2. PowerShell을 Exchange Online에 연결한 후 1 단계에서 CSV 파일을 저장 한 데스크톱 폴더로 이동 합니다. 예를 `C:\Users\Administrator\desktop`들어
    
3. 다음 명령을 실행 하 여 외부 연락처를 만듭니다.

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    가져오는 수에 따라 새 연락처를 만드는 데 시간이 오래 걸릴 수 있습니다. 명령이 실행을 마치면 PowerShell에 새로 만들어진 연락처 목록이 표시 됩니다. 
    
4. 새 외부 연락처를 보려면 EAC (Exchange 관리 센터)로 이동 하 여 **받는 사람** \> **연락처**를 클릭 합니다. 
    
    > [!TIP]
    > EAC에 연결 하는 방법에 대 한 자세한 내용은 exchange [Online의 exchange 관리 센터](https://go.microsoft.com/fwlink/p/?LinkId=328197)를 참조 하십시오. 
  
5. 필요한 경우 새로 고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) **새로 고침** ![을 클릭 하 여 목록을 업데이트 하 고 가져온 외부 연락처를 확인 합니다. 
    
    가져온 연락처가 outlook 및 웹용 outlook의 공유 주소록에 나타납니다.
    
    > [!NOTE]
    > **사용자** \> **연락처로**이동 하 여 Microsoft 365 관리 센터에서 연락처를 볼 수도 있습니다. 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a>3 단계: 외부 연락처의 속성에 정보 추가

2 단계에서 명령을 실행 한 후에는 외부 연락처가 만들어지지만, 연락처 또는 조직 정보 (CSV 파일에 있는 대부분의 셀 정보)는 포함 되지 않습니다. 이는 새 외부 연락처를 만들 때 필요한 속성만 채워져 있기 때문입니다. CSV 파일에 모든 정보가 채워지지 않더라도 걱정할 필요는 없습니다. 해당 내용이 없는 경우에는 추가 되지 않습니다.
  
1.  Exchange Online 조직에 PowerShell을 연결 합니다. 단계별 지침은 [Exchange Online PowerShell에 연결을](https://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하십시오.
    
2. 1 단계에서 CSV 파일을 저장 한 데스크톱 폴더로 이동 합니다. 예를 `C:\Users\Administrator\desktop`들어
    
3. 다음 두 명령을 실행 하 여 CSV 파일의 다른 속성을 2 단계에서 만든 외부 연락처에 추가 합니다.
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > _Manager_ 매개 변수에 문제가 있을 수 있습니다. CSV 파일에서 셀이 비어 있으면 오류가 발생 하 고 해당 연락처에 추가 되는 속성 정보가 없습니다. 관리자를 지정할 필요가 없는 경우에는 이전 PowerShell 명령을 삭제 ` -Manager $_.Manager ` 하면 됩니다. 
  
    이번에는 1 단계에서 가져온 수에 따라 연락처를 업데이트 하는 데 시간이 걸릴 수 있습니다. 
    
4. 속성이 연락처에 추가 되었는지 확인 하려면 다음을 수행 합니다. 
    
1. EAC에서 **받는 사람** \> **연락처**로 이동합니다.
    
2. 연락처를 클릭 한 다음 편집 **** ![아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) 편집을 클릭 하 여 연락처의 속성을 표시 합니다. 
    
모두 완료되었습니다. 사용자는 주소록 Outlook 및 웹용 outlook에서 연락처 및 추가 정보를 볼 수 있습니다.
  
## <a name="add-more-external-contacts"></a>외부 연락처 추가

Exchange Online에서 새 외부 연락처를 추가 하려면 1 ~ 3 단계를 반복할 수 있습니다. 또는 회사의 사용자가 새 연락처에 대 한 CSV 파일에 새 행을 추가 하기만 하면 됩니다. 그런 다음 2 단계와 3 단계에서 PowerShell 명령을 실행 하 여 새 연락처에 정보를 추가 하 고 추가할 수 있습니다.
  
> [!NOTE]
> 명령을 실행 하 여 새 연락처를 만드는 경우 이전에 만든 연락처가 이미 있음을 알리는 오류가 표시 될 수 있습니다. 하지만 CSV 파일에 추가 된 모든 새 연락처가 만들어집니다. 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a>공유 주소 book>에서 외부 연락처 숨기기

일부 회사에서는 외부 연락처만 사용 하 여 메일 그룹의 구성원으로 추가할 수 있습니다. 이 시나리오에서는 공유 주소록에서 외부 연락처를 숨기려는 경우가 있습니다. 방법은 다음과 같습니다.
  
1.  Exchange Online 조직에 PowerShell을 연결 합니다. 단계별 지침은 [Exchange Online PowerShell에 연결을](https://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하십시오.
    
2. 단일 외부 연락처를 숨기려면 다음 명령을 실행 합니다.
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    예를 들어 Pilar Pinilla을 공유 주소록에서 숨기려면 다음 명령을 실행 합니다.

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. 공유 주소록에서 모든 외부 연락처를 숨기려면 다음 명령을 실행 합니다.

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

그룹을 숨기면 외부 연락처가 공유 주소록에 표시 되지 않지만 여전히 메일 그룹의 구성원으로 추가할 수 있습니다.
