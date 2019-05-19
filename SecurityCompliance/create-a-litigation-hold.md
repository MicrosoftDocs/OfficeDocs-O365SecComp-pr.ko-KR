---
title: 소송 보존 만들기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: e6201fc938f7481a524a8d3c4171d4c1b67997e9
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153750"
---
# <a name="create-a-litigation-hold"></a>소송 보존 만들기

사서함에 대 한 소송 보존을 적용 하 여 삭제 된 항목을 비롯 한 모든 사서함 콘텐츠를 보존할 수 있습니다. 사용자 사서함에 소송 보존을 적용 하면 사용자의 보관 사서함에 있는 콘텐츠 (사용 하도록 설정 된 경우)도 유지 됩니다. 보류를 만들 때 삭제 및 수정 된 항목을 지정한 기간 동안 보존 하 고 사서함에서 영구적으로 삭제할 수 있도록 보존 기간 ( *시간 기반 보존*이 라고도 함)을 지정할 수도 있습니다. 또는 콘텐츠를 무기한 보존 ( *무기한 보류*라고 함) 하거나 소송 보존을 제거할 때까지 가능 합니다. 보존 기간을 지정 하는 경우에는 메시지가 수신 되거나 사서함 항목이 만들어진 날짜를 통해 계산 됩니다. 
  
소송 보존을 만들 때 수행 되는 작업은 다음과 같습니다.
  
- 사용자가 영구적으로 삭제 한 항목은 보류 기간 동안 사용자의 사서함에 있는 복구할 수 있는 항목 폴더에 보관 됩니다.
    
- 사용자가 복구 가능한 항목 폴더에서 제거 된 항목은 보류 기간 동안 보존 됩니다.
    
- 복구 가능한 항목 폴더의 저장소 할당량은 30gb에서 110 GB로 증가 합니다.
    
- 사용자의 기본 및 보관 사서함에 있는 항목은 유지 됩니다.
    
## <a name="before-you-begin"></a>시작하기 전에

- Exchange Online 사서함에 소송 보존을 적용 하려면 Exchange Online 계획 2 라이선스를 할당 받아야 합니다. 사서함에 Exchange Online 계획 1 라이선스가 할당 되는 경우이를 보류 상태로 설정 하려면 별도의 Exchange Online 보관 라이선스를 할당 해야 합니다.
    

## <a name="place-a-mailbox-on-litigation-hold"></a>사서함을 소송 자료 보존으로 설정

다음은 Exchange 관리 센터를 사용 하 여 사서함에 소송 보존을 적용 하는 단계입니다.

1. 로 이동 [https://outlook.office.com/ecp](https://outlook.office.com/ecp) 하 고 전역 관리자 계정을 사용 하 여 로그인 합니다.

2. 왼쪽 탐색 창에서 **받는 사람 _GT_ 사서함** 을 클릭 합니다.

3. 소송 보존에 적용할 사서함을 선택 하 고 **편집**을 클릭 합니다.

4. 사서함 속성 페이지에서 **사서함 기능**을 클릭 합니다.
    
5. **소송 보존: 사용 안 함**에서 **사용** 을 클릭 하 여 사서함을 소송 보존 상태로 설정 합니다.
    
6. **소송 보존** 페이지에서 다음 선택적 정보를 입력 합니다. 
    
    - **소송 보존 기간 (일)** -이 상자를 사용 하 여 시간 기반 보존을 만들고 사서함이 소송 보존 상태에 있을 때 사서함 항목이 보관 되는 기간을 지정 합니다. 기간은 사서함 항목이 수신되거나 만들어진 날짜부터 계산됩니다. 특정 항목에 대해 보존 기간이 만료 되 면 해당 항목은 더 이상 보존 되지 않습니다. 이 상자를 비워 두면 항목이 무기한 보존 되거나 보류가 제거 될 때까지 유지 됩니다. 기간을 지정 하려면 days를 사용 합니다.
    
    - **참고** -이 상자를 사용 하 여 사서함이 소송 보존 상태 인지를 사용자에 게 알립니다. 메모는 Outlook 2010 이상 버전을 사용 중인 경우 사용자 사서함의 계정 정보 페이지에 표시 됩니다. 사용자는이 페이지에 액세스 하 여 Outlook에서 **파일** 을 클릭할 수 있습니다.
    
    - **URL** -소송 보존에 대 한 자세한 내용은이 상자를 사용 하 여 사용자에 게 웹 사이트를 안내 합니다. 이 URL은 사용자 사서함의 계정 정보 페이지에서 Outlook 2010 이상 버전을 사용 하는 경우에 표시 됩니다. 사용자는이 페이지에 액세스 하 여 Outlook에서 **파일** 을 클릭할 수 있습니다.

7. **소송 보존** 페이지에서 **저장** 을 클릭 한 다음 사서함 속성 페이지에서 **저장** 을 클릭 합니다.

### <a name="create-a-litigation-hold-using-powershell"></a>PowerShell을 사용 하 여 소송 보존 만들기

[Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)에서 다음 명령을 실행 하 여 소송 보존을 만들 수도 있습니다.

```
Set-Mailbox <username> -LitigationHoldEnabled $true
```

이전 명령은 보존 기간이 지정 되지 않았으므로 항목을 무기한 보존 합니다. 다음 명령을 사용 하 여 시간 기반 보존을 만들 수 있습니다.

```
Set-Mailbox <username> -LitigationHoldEnabled $true -LitigationHoldDuration <number of days>
```

자세한 내용은 [Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/set-mailbox)를 참조 하십시오.

## <a name="how-does-litigation-hold-work"></a>소송 보존의 작동 방식

일반 삭제 된 항목 워크플로에서 사서함 항목은 사용자가 영구적으로 삭제 (Shift + Delete) 되거나 지운 편지함 폴더에서 삭제 될 때 복구 가능한 항목 폴더의 삭제 하위 폴더로 이동 됩니다. 삭제 보존 작업을 사용 하 여 구성 된 보존 태그 인 삭제 정책은 보존 기간이 만료 되 면 항목을 삭제 하위 폴더로 이동 합니다. 사용자가 복구 가능한 항목 폴더에서 항목을 제거 하거나 삭제 된 항목 보존 기간이 항목에 대해 만료 되는 경우 복구 가능한 항목 폴더의 제거 하위 폴더로 이동 되 고 영구 삭제 되도록 표시 됩니다. 다음에는 MFA (관리 되는 폴더 도우미)에서 사서함을 처리할 때 Exchange에서 제거 됩니다.

사서함을 소송 보존 상태로 설정 하면 제거 하위 폴더의 항목은 소송 보존에 지정 된 보존 기간 동안 보존 됩니다. 보존 기간은 항목이 수신 되거나 만들어진 원래 날짜 로부터 계산 되며, 제거 하위 폴더의 항목이 보관 되는 기간을 정의 합니다. 제거 하위 폴더에 있는 항목에 대 한 보존 기간이 만료 되 면 해당 항목은 영구 삭제 되도록 표시 되며 다음에는 해당 사서함이 MFA에 의해 처리 될 때 Exchange에서 제거 됩니다. 사서함에 무기한 보류가 적용 되 면 항목은 제거 된 하위 폴더에서 제거 되지 않습니다.

다음 그림에서는 복구 가능한 항목 폴더 및 보류 워크플로 프로세스의 하위 폴더를 보여 줍니다.

![소송 보존 수명 주기](media/LitigationHoldLifeCycle.png)

> [!NOTE]
> EDiscovery 사례와 관련 된 보류를 사서함에 저장 하면 제거 된 항목은 삭제 하위 폴더에서 DiscoveryHolds 하위 폴더로 이동 되 고 사서함이 eDiscovery 보류에서 릴리스될 때까지 보존 됩니다.
  