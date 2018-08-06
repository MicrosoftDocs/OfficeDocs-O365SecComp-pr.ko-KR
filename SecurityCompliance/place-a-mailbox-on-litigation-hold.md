---
title: 전체 사서함에 소송 보존으로 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: '사서함 삭제 된 항목 및 수정 된 항목의 원래 버전을 포함 하 여 모든 사서함 콘텐츠를 유지 하기 위해 소송 보존에 배치 합니다. '
ms.openlocfilehash: 8f440f5fc0bc7dafd639bdf8136808aa2f3bd35f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026445"
---
# <a name="place-a-mailbox-on-litigation-hold"></a>전체 사서함에 소송 보존으로 설정
 
사서함 삭제 된 항목 및 수정 된 항목의 원래 버전을 포함 하 여 모든 사서함 콘텐츠를 유지 하기 위해 소송 보존에 배치 합니다. 사용자를 배치 하는 경우 ' 사서함이 소송 보존으로 설정 합니다 (활성화 되어 있음) 하는 경우 사용자의 보관 사서함의 콘텐츠에도 대기 상태로 설정 됩니다. 항목을 삭제 하 고 수정 된 지정된 된 기간에 대 한 또는 소송 보존으로 설정에서 사서함을 제거할 때까지 유지 됩니다. 이러한 모든 사서함 항목은 [원본 위치 eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) 검색에서 반환 됩니다. 
  
> [!IMPORTANT]
> 사용자의 사서함의 복구 가능한 항목 폴더에서 항목을 유지 하는 소송 보존 합니다. 번호 및 삭제 되거나 수정 된 항목의 크기에 따라 사서함의 복구 가능한 항목 폴더의 크기는 신속 하 게 증가할 수 있습니다. 복구 가능한 항목 폴더는 기본적으로 높은 할당량으로 구성 됩니다. Exchange Online에서이 할당량은 소송 보존으로 설정에서 사서함을 할 때 증가 자동으로 합니다. Exchange Server 2013, 것이 좋습니다의 복구 가능한 항목 할당량 제한에 도달한 하지 되도록 매주 소송 보존에 배치 되는 사서함을 모니터링 하는 합니다. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

- 예상 완료 시간: 5분
    
- 소송 보존 설정을 적용 하려면 60 분까지 걸릴 수 있습니다.
    
- 이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [메시징 정책 및 규정 준수 권한](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) 항목의 "원본 위치 유지" 항목을 참조 하십시오. 
    
- Exchange Online 사서함에 소송 보존 하려면, Exchange Online (계획 2) 라이선스를 할당 해야 합니다. 사서함에는 Exchange Online (계획 1) 라이선스를 할당 되 면 보류에 추가 하는 별도 Exchange Online 보관 라이선스가 할당 해야 합니다.
    
- 앞에서 설명한 것 처럼 사용자의 사서함에 소송 보존을 할 때 사용자의 보관 사서함의 콘텐츠도 대기 상태로 설정 됩니다. Exchange 하이브리드 배포에는 온-프레미스 기본 사서함에 소송 보존을 배치 하는 경우 클라우드 기반 보관 사서함 (활성화 된 경우)도 대기 상태로 설정 됩니다.
    
- 복구 가능한 항목 폴더에 대 한 할당량 Exchange Online에서 자동으로 소송 보존으로 설정에서 사서함을 할 때 100GB로 증가 되었습니다. 이 폴더의 기본 크기가 30GB입니다.
    
- 삭제 된 항목을 유지 하 고도 보존이 제거 될 때까지 수정 된 항목의 원래 버전을 유지 하는 소송 보존 합니다. 필요에 따라 지정 된 기간 동안 사서함 항목을 보존 하는 보존 기간을 지정할 수 있습니다. 보류 기간 기간을 지정 하면 메시지를 받은 또는 사서함 항목을 만들 날짜부터 계산 됩니다. 사용자 지정 된 조건을 충족 하는 항목을 유지 하려면 쿼리 기반 보류를 만들려면 In-place Hold를 사용 합니다. 자세한 내용은 [만들기 또는 제거 In-place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx)를 참조 합니다.
    
- 셸을 사용 하 여 Exchange Online 사서함을 보류 하, Exchange Online PowerShell을 사용 해야 합니다. 자세한 내용은 [Connect to Exchange Online를 사용 하 여 원격 PowerShell을](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx)참조 하십시오.
    
- 공용 폴더 사서함에 소송 보존을 배치할 수 없습니다. 공용 폴더에 대 한 보류 시키려면 원본 위치 유지를 사용 해야 합니다.
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a>EAC를 사용 하 여 사서함에 소송 보존 하려면
<a name="sectionSection1"> </a>

1. **받는 사람** 에 게 이동 \> **사서함**입니다.
    
2. 사용자 사서함 목록에서 소송 보존에 배치 하려는 사서함을 클릭 하 고 **편집**을 클릭 한 다음![편집 아이콘](media/ITPro-EAC-EditIcon.png)합니다.
    
3. 사서함 속성 페이지에서 클릭 **사서함 기능.**
    
4. 아래에서 **소송 보존: 비활성화 된**, 사서함에 소송 보존 하려면 **사용** 을 클릭 합니다. 
    
5. **소송 보존으로 설정** 페이지에서 다음과 같은 선택적 정보를 입력 합니다. 
    
  - **소송 보존 기간 (일)** 이 상자를 사용 하 여 사서함이 소송 보존으로 설정 중일 때 사서함 항목이 보관 되는 기간을 지정 합니다. 사서함 항목을 받거나 만든 날짜에서 기간 계산 됩니다. 이 상자를 비워두면 하는 경우 항목은 무기한 또는 보존이 제거 될 때까지 보관 됩니다. 기간을 지정 하려면 날짜를 사용 합니다. 
    
  - **참고 사항** 이 상자를 사용 하 여 자신의 사서함이 소송 보존으로 설정에 사용자에 게 알립니다. Outlook 2010 이상 사용 하 여 하는 경우 사용자의 사서함에 메모가 표시 됩니다. 
    
  - **URL** 이 상자를 사용 하 여 사용자 소송 보존으로 설정 하는 방법에 대 한 자세한 내용은 웹사이트에 직접 보내도록 지정 합니다. Outlook 2010 이상를 사용 하는 경우이 URL이 사용자의 사서함에 나타납니다. 
    
6. **소송 보존으로 설정** 페이지에서 **저장** 을 클릭 하 고 사서함 속성 페이지에서 **저장** 을 클릭 합니다. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a>셸을 사용 하 여 사서함에 소송 보존 하려면 무기한
<a name="sectionSection2"> </a>

사서함 bsuneja@contoso.com 소송 보존으로 설정에 저장 하는이 예제입니다. 사서함의 항목은 무기한 또는 보존이 제거 될 때까지 유지 됩니다.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> _LitigationHoldDuration_ 속성 사서함에 대 한 값을 로설정하면를 할 때 사서함에 소송 보존으로 설정 무기한 (하 여 기간 기간을 지정 하지 않으면) `Unlimited`합니다. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a>셸을 사용 하 여 사서함 소송 보존에 배치 하 고 지정 된 기간에 대 한 항목을 보존
<a name="sectionSection3"> </a>

이 예에서는 사서함 bsuneja@contoso.com 소송 보존에 배치 하 고 2555 일 (약 7 년)에 대 한 항목을 유지 합니다. 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a>셸을 사용 하 여 지정 된 기간에 대 한 소송 보존으로 설정에서 모든 사서함을 보류
<a name="sectionSection4"> </a>

조직의 특정 기간에 대 한 모든 사서함 데이터를 유지 하는 필요할 수 있습니다. 소송 보존으로 설정에 조직에서 모든 사서함을 배치 하기 전에 다음 사항을 고려 합니다.
  
1 년 (365 일)에 대 한 소송 보존으로 설정에서 조직에서 모든 사용자 사서함을 저장 하는이 예제입니다.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

이 예제에서는 [Get-mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet을 사용 하 여 조직에서 모든 사서함을 검색 모든 사용자 사서함을 포함 하는 받는 사람 필터를 지정 하 고 다음 사서함을 소송 보존을 사용 하도록 설정 하려면 [Set-mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet 목록이 파이프 하 고 보존 기간입니다. 
  
모든 사용자 사서함에는 무기한 보존 설정 시키려면 이전 명령을 실행 하지만 _LitigationHoldDuration_ 매개 변수를 포함 하지 마십시오. 
  
포함 하거나 하나 이상의 사서함을 제외 하는 필터에 다른 받는 사람 속성을 사용 하는 예제에 대 한 [자세한 내용](#moreinfo.md) 은 섹션을 참조 하십시오. 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a>셸을 사용 하 여 소송 보존으로 설정에서 사서함을 제거 하려면
<a name="sectionSection5"> </a>

소송 보존으로 설정에서 사서함 bsuneja@contoso.com를 제거 하는이 예제입니다.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

P
## <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인합니까?
<a name="sectionSection6"> </a>

소송 보존으로 설정에 사서함을 성공적으로 배치 되도록을 확인 하려면 다음 중 하나를 수행 합니다.
  
- EAC에서:
    
1. **받는 사람** 에 게 이동 \> **사서함**입니다.
    
2. 사용자 사서함 목록에서 사서함을 소송 보존 설정을 확인 하려면을 클릭 하 고 **편집**을 클릭 한 다음![편집 아이콘](media/ITPro-EAC-EditIcon.png)합니다.
    
3. 사서함 속성 페이지에서 클릭 **사서함 기능.**
    
4. **소송 보존으로 설정**, 아래에서 보류를 사용할 수 있는지를 확인 합니다.
    
5. 사서함에 소송 보존으로 설정 하 고 사람 했을 때 확인 하려면 **세부 정보 보기** 클릭 합니다. 확인 하거나 선택적 값을 변경할 수도 **소송 보존 기간 (일)**, **메모**및 **URL** 상자입니다. 
    
- 셸에서 다음 명령 중 하나를 실행 합니다.
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    또는
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    경우 사서함에 배치 소송 보존으로 설정 무기한, 값 _LitigationHoldDuration_ 속성 사서함이 설정에 대 한 `Unlimited`합니다.
    
## <a name="more-information"></a>추가 정보
<a name="moreinfo"> </a>

- 조직에 필요한 모든 사서함 데이터에는 특정 기간에 대 한 보존을 하는 경우에 소송 보존으로 설정에 조직에서 모든 사서함을 배치 하기 전에 다음을 고려 하십시오.
    
  - 이전 명령을 사용 하 여 보류에 배치 하는 명령을 실행 하는 시간에 존재 하는 모든 조직 (또는 지정 된 받는 사람 필터와 일치 하는 사서함의 하위 집합)의 사서함만 사서함 보류에 배치 됩니다. 나중에 새 사서함을 만들 경우 다시 새 사서함을 보류 하는 명령을 실행 해야 합니다. 새 사서함을 자주 만들어야 하는 경우 필요에 따라 자주 명령으로 예약 된 작업을 실행할 수 있습니다.
    
  - 모든 사서함을 소송 보존에 배치 사서함 크기 큰 영향을 줄 수 있습니다. Exchange Server 2013의 조직에서 조직의 보존 요구를 충족 하기 위해 적절 한 저장소를 계획 합니다.
    
  - 복구 가능한 항목 폴더는 폴더의 항목 사서함 저장소 제한에 가깝게 계산 하지 않도록 자체 저장 용량 제한을 있습니다. 앞에서 설명한 것 처럼 오랜 시간 동안에 대 한 사서함 데이터를 보존 됩니다 사용자의 사서함에서 복구 가능한 항목 폴더의 성장에 발생 하 고 보관 합니다. 을 수용 하기 위해이 증가 대 한 Exchange Online 복구 가능한 항목 폴더에 대 한 할당량은 자동으로 증가 30GB에서 100GB로 소송 보존으로 설정에서 사서함을 할 때 합니다. 
    
    Exchange Server 2013, 복구 가능한 항목 폴더에 대 한 기본 저장 용량 제한 30GB 이기도합니다. 업그레이드를 주기적으로 제한에 도달 하지 것을 확인 하려면이 폴더의 크기를 모니터링 하는 것이 좋습니다. 자세한 내용은 [복구 가능한 항목 폴더](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx)를 참조 하십시오.
    
- 이전 명령은 모든 사서함을 보류 하는 모든 사용자 사서함을 반환 하는 받는 사람 필터를 사용 합니다. 다음에 연결할 수 **Set-mailbox** cmdlet에 해당 사서함에 소송 보존을 배치 하는 특정 사서함의 목록을 반환 하려면 다른 받는 사람 속성을 사용할 수 있습니다. 
    
    다음은 일반적인 사용자 또는 사서함 속성을 기준으로 사서함의 하위 집합을 반환 하려면 **Get-mailbox** 및 **Get-recipient** cmdlet을 사용 하 여의 몇가지 예입니다. 이 예제에서는 관련 사서함 속성 (예: _CustomAttributeN_ 또는 _부서_) 채워지고 가정 합니다.
    
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

    포함 하거나 사서함을 제외 하는 필터에 다른 사용자 사서함 속성을 사용할 수 있습니다. 자세한 내용은 참조 [필터링 할 수 있는 속성은-Filter 매개 변수에 대 한](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx)합니다.
    

