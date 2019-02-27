---
title: 사서함을 소송 자료 보존으로 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: '사서함에 소송 보존을 적용 하 여 삭제 된 항목 및 수정 된 항목의 원본 버전을 비롯 한 모든 사서함 콘텐츠를 유지 합니다. '
ms.openlocfilehash: b2d2a60fddb51aa310d01a765c1ebbbf127ecd19
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296981"
---
# <a name="place-a-mailbox-on-litigation-hold"></a>사서함을 소송 자료 보존으로 설정
 
사서함에 소송 보존을 적용 하 여 삭제 된 항목 및 수정 된 항목의 원본 버전을 비롯 한 모든 사서함 콘텐츠를 유지 합니다. 사용자 사서함에 소송 보존을 적용 하면 사용자의 보관 사서함에 있는 콘텐츠 (사용 하도록 설정 된 경우)도 보존 됩니다. 삭제 되 고 수정 된 항목은 지정 된 기간 동안 또는 소송 보존에서 사서함을 제거할 때까지 보존 됩니다. 이러한 모든 사서함 항목은 원본 [위치 eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) 검색에서 반환 됩니다. 
  
> [!IMPORTANT]
> 소송 보존은 사용자 사서함의 복구 가능한 항목 폴더에 있는 항목을 보존 합니다. 삭제 되거나 수정 된 항목의 수와 크기에 따라 사서함의 복구 가능한 항목 폴더 크기가 빠르게 증가할 수 있습니다. 복구 가능한 항목 폴더는 기본적으로 높은 할당량을 사용 하 여 구성 됩니다. Exchange Online에서 사서함을 소송 보존 상태로 설정 하면이 할당량이 자동으로 증가 합니다. Exchange Server 2013에서는 주 단위로 소송 보존 상태로 설정 된 사서함을 모니터링 하 여 복구 가능한 항목 할당량의 제한에 도달 하지 않았는지 확인 하는 것이 좋습니다. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

- 예상 완료 시간: 5분
    
- 소송 보존 설정이 적용 되려면 최대 60 분이 소요 될 수 있습니다.
    
- 이 절차를 수행 하려면 먼저 사용 권한을 할당 받아야 합니다. 필요한 사용 권한을 확인 하려면 [메시징 정책 및 규정 준수 권한](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) 항목의 "원본 위치 유지" 항목을 참조 하십시오. 
    
- exchange online 사서함에 소송 보존을 적용 하려면 exchange online (요금제 2) 라이선스를 할당 받아야 합니다. 사서함에 Exchange online (요금제 1) 라이선스가 할당 되는 경우이를 보류 상태로 설정 하려면 별도의 exchange online 보관 라이선스를 할당 해야 합니다.
    
- 앞에서 설명한 것 처럼 사용자 사서함에 소송 보존을 적용 하면 사용자의 보관 사서함에 포함 된 콘텐츠도 보존 됩니다. Exchange 하이브리드 배포에서 온-프레미스 기본 사서함에 소송 보존을 적용 하면 클라우드 기반 보관 사서함 (사용 하도록 설정 된 경우)도 보존 됩니다.
    
- Exchange Online에서 사서함을 소송 보존 상태로 설정 하면 복구 가능한 항목 폴더에 대 한 할당량이 자동으로 100 GB로 증가 합니다. 이 폴더의 기본 크기는 30gb입니다.
    
- 소송 보존은 삭제 된 항목을 보존 하 고 보존을 제거할 때까지 수정한 항목의 원래 버전도 보존 합니다. 원하는 경우 보존 기간을 지정 하 여 지정 된 기간 동안 사서함 항목을 보존할 수 있습니다. 보존 기간을 지정 하는 경우에는 메시지가 수신 되거나 사서함 항목이 만들어진 날짜부터 계산 됩니다. 지정 된 조건을 충족 하는 항목을 보존 하려면 원본 위치 유지를 사용 하 여 쿼리 기반 보존을 만듭니다. 자세한 내용은 원본 [위치 유지 만들기 또는 제거](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx)를 참조 하세요.
    
- 셸을 사용 하 여 exchange online 사서함을 보류 상태로 설정 하려면 exchange online PowerShell을 사용 해야 합니다. 자세한 내용은 [원격 PowerShell을 사용 하 여 Exchange Online에 연결](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx)을 참조 하세요.
    
- 공용 폴더 사서함에 소송 보존을 설정 하는 것은 지원 되지 않습니다. 원본 위치 유지를 사용 하 여 공용 폴더를 보존 해야 합니다.
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a>EAC를 사용 하 여 사서함을 소송 보존으로 설정
<a name="sectionSection1"> </a>

1. **받는 사람** \> **사서함**으로 이동 합니다.
    
2. 사용자 사서함 목록에서 소송 보존에 추가할 사서함을 클릭 한 다음 편집 아이콘](media/ITPro-EAC-EditIcon.gif) **편집** ![을 클릭 합니다.
    
3. 사서함 속성 페이지에서 **사서함 기능을 클릭 합니다.**
    
4. **소송 보존: 사용 안 함**에서 **사용** 을 클릭 하 여 사서함을 소송 보존 상태로 설정 합니다. 
    
5. **소송 보존** 페이지에서 다음 선택적 정보를 입력 합니다. 
    
  - **소송 보존 기간 (일)** 이 상자를 사용 하 여 사서함이 소송 보존 상태에 있을 때 사서함 항목이 보관 되는 기간을 지정 합니다. 기간은 사서함 항목을 받거나 만든 날짜 로부터 계산 됩니다. 이 상자를 비워 두면 항목이 무기한으로 또는 보존이 제거 될 때까지 유지 됩니다. 기간을 지정 하려면 days를 사용 합니다. 
    
  - **참고 사항** 이 상자를 사용 하 여 사서함이 소송 보존 상태 인지를 사용자에 게 알립니다. 메모는 Outlook 2010 이상 버전을 사용 하는 경우 사용자의 사서함에 표시 됩니다. 
    
  - **URL** 이 상자를 사용 하 여 소송 보존에 대 한 자세한 내용을 보려면 웹 사이트에 사용자를 안내 합니다. 이 URL은 사용자의 사서함에 Outlook 2010 이상 버전을 사용 하는 경우에 표시 됩니다. 
    
6. **소송 보존** 페이지에서 **저장** 을 클릭 한 다음 사서함 속성 페이지에서 **저장** 을 클릭 합니다. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a>셸을 사용 하 여 사서함에 소송 보존을 무제한으로 설정
<a name="sectionSection2"> </a>

이 예에서는 사서함 bsuneja@contoso.com에 소송 보존을 설정 합니다. 사서함의 항목은 무기한으로 또는 보류가 제거 될 때까지 유지 됩니다.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> 일정 기간을 지정 하지 않고 사서함에 소송 보존을 적용 하면 _LitigationHoldDuration_ 속성 사서함의 값이로 `Unlimited`설정 됩니다. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a>셸을 사용 하 여 사서함을 소송 보존 상태로 설정 하 고 지정 된 기간 동안 항목을 보존 합니다.
<a name="sectionSection3"> </a>

이 예에서는 사서함 bsuneja@contoso.com에 소송 보존을 설정 하 고 2555 일 (약 7 년) 동안 항목을 보존 합니다. 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a>셸을 사용 하 여 지정 된 기간 동안 모든 사서함을 소송 보존으로 설정
<a name="sectionSection4"> </a>

조직에서 일정 기간 동안 모든 사서함 데이터를 보존 해야 할 수도 있습니다. 조직의 모든 사서함을 소송 보존으로 설정 하기 전에 다음을 고려 하세요.
  
이 예에서는 1 년 (365 일) 동안 조직의 모든 사용자 사서함에 소송 보존을 추가 합니다.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

이 예에서는 [Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet을 사용 하 여 조직의 모든 사서함을 검색 하 고, 모든 사용자 사서함이 포함 된 받는 사람 필터를 지정 하 고, 사서함 목록을 [사서함](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet으로 파이프 하 여 소송 보존을 사용 하도록 설정 하 고, 보존 기간 
  
모든 사용자 사서함을 무기한 보존 상태로 설정 하려면 이전 명령을 실행 하 되 _LitigationHoldDuration_ 매개 변수는 포함 하지 않습니다. 
  
필터에 다른 받는 사람 속성을 사용 하 여 하나 이상의 사서함을 포함 하거나 제외 하는 방법에 대 한 예는 [추가 정보](#moreinfo.md) 섹션을 참조 하십시오. 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a>셸을 사용 하 여 사서함이 소송 보존 상태에서 제거 됩니다.
<a name="sectionSection5"> </a>

이 예에서는 사서함 bsuneja@contoso.com에서 소송 보존을 제거 합니다.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

P
## <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인합니까?
<a name="sectionSection6"> </a>

사서함이 소송 보존 상태 인지 확인 하려면 다음 중 하나를 수행 합니다.
  
- EAC에서:
    
1. **받는 사람** \> **사서함**으로 이동 합니다.
    
2. 사용자 사서함 목록에서 소송 보존 설정을 확인 하려는 사서함을 클릭 한 다음 편집 아이콘](media/ITPro-EAC-EditIcon.gif) **편집** ![을 클릭 합니다.
    
3. 사서함 속성 페이지에서 **사서함 기능을 클릭 합니다.**
    
4. **소송 보존**에서 보류가 사용 되도록 설정 되어 있는지 확인 합니다.
    
5. **세부 정보 보기** 를 클릭 하 여 사서함이 소송 보존 및 해당 담당자에 게 들어간 시기를 확인 합니다. 선택적 **소송 보존 기간 (일)**, **메모**및 **URL** 상자의 값을 확인 하거나 변경할 수도 있습니다. 
    
- 셸에서 다음 명령 중 하나를 실행 합니다.
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    또는
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    사서함이 소송 보존 상태로 유지 되는 경우 _LitigationHoldDuration_ 속성 사서함의 값이로 `Unlimited`설정 됩니다.
    
## <a name="more-information"></a>추가 정보
<a name="moreinfo"> </a>

- 조직에서 모든 사서함 데이터를 특정 기간 동안 보존 해야 하는 경우 조직의 모든 사서함을 소송 보존 상태로 설정 하기 전에 다음을 고려 하십시오.
    
  - 이전 명령을 사용 하 여 조직의 모든 사서함 (또는 지정 된 받는 사람 필터와 일치 하는 사서함의 하위 집합)을 유지 하는 경우 명령을 실행 하는 시점에 있는 사서함만 보류 됩니다. 나중에 새 사서함을 만드는 경우이 명령을 다시 실행 하 여 새 사서함을 보류 상태로 설정 해야 합니다. 새 사서함을 자주 만드는 경우에는 필요한 만큼 명령을 예약 된 작업으로 실행할 수 있습니다.
    
  - 모든 사서함을 소송 보존으로 두면 사서함 크기에 큰 영향을 줄 수 있습니다. Exchange Server 2013 조직에서 조직의 보존 요구 사항에 맞는 적절 한 저장소를 계획 합니다.
    
  - 복구 가능한 항목 폴더에는 고유한 저장 제한이 있으므로 폴더의 항목이 사서함 저장 용량 한도를 초과 하지 않도록 합니다. 앞에서 설명한 것 처럼 오랫동안 사서함 데이터를 보존 하면 사용자 사서함에 복구 가능한 항목 폴더가 증가 하 게 됩니다. Exchange Online의 이러한 증가에 맞게 사서함을 소송 보존 상태로 설정 하면 복구 가능한 항목 폴더에 대 한 할당량이 자동으로 30gb에서 100 GB로 증가 합니다. 
    
    Exchange Server 2013에서는 복구 가능한 항목 폴더에 대 한 기본 저장 제한도 30gb입니다. 이 폴더의 크기를 주기적으로 모니터링 하 여 제한에 도달 하지 않았는지 확인 하는 것이 좋습니다. 자세한 내용은 [복구 가능한 항목 폴더](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx)를 참조 하십시오.
    
- 모든 사서함에 대 한 보류를 설정 하는 이전 명령은 모든 사용자 사서함을 반환 하는 받는 사람 필터를 사용 합니다. 다른 받는 사람 속성을 사용 하 여 사서함 cmdlet을 파이프 하 여 해당 사서함에 소송 보존을 **설정할** 수 있는 특정 사서함 목록을 반환할 수 있습니다. 
    
    다음은 일반 사용자 또는 사서함 속성에 따라 사서함의 하위 집합을 반환 하기 위해 **get-Mailbox** 및 **Recipient** cmdlet을 사용 하는 몇 가지 예입니다. 이러한 예에서는 _customattributen_ 또는 _부서_와 같은 관련 사서함 속성이 채워져 있다고 가정 합니다.
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    필터에 다른 사용자 사서함 속성을 사용 하 여 사서함을 포함 하거나 제외할 수 있습니다. 자세한 내용은 [-Filter 매개 변수의 필터링 할 수 있는 속성](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx)을 참조 하십시오.
    

