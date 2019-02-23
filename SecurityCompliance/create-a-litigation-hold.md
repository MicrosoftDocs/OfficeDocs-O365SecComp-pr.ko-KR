---
title: Office 365에서 소송 보존 만들기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218658"
---
# <a name="create-a-litigation-hold-in-office-365"></a>Office 365에서 소송 보존 만들기

사서함에 대 한 소송 보존을 적용 하 여 삭제 된 항목을 비롯 한 모든 사서함 콘텐츠를 보존할 수 있습니다. 사용자 사서함에 소송 보존을 적용 하면 사용자의 보관 사서함에 있는 콘텐츠 (사용 하도록 설정 된 경우)도 유지 됩니다. 보류를 만들 때 삭제 및 수정 된 항목을 지정한 기간 동안 보존 하 고 사서함에서 영구적으로 삭제할 수 있도록 보존 기간 ( *시간 기반 보존*이 라고도 함)을 지정할 수도 있습니다. 또는 콘텐츠를 무기한 보존 ( *무기한 보류*라고 함) 하거나 소송 보존을 제거할 때까지 가능 합니다. 보존 기간을 지정 하는 경우에는 메시지가 수신 되거나 사서함 항목이 만들어진 날짜를 통해 계산 됩니다. 
  
소송 보존을 만들 때 수행 되는 작업은 다음과 같습니다.
  
- 사용자가 영구적으로 삭제 한 항목은 보류 기간 동안 사용자의 사서함에 있는 복구할 수 있는 항목 폴더에 보관 됩니다.
    
- 사용자가 복구 가능한 항목 폴더에서 제거 된 항목은 보류 기간 동안 보존 됩니다.
    
- 복구 가능한 항목 폴더의 저장소 할당량은 30gb에서 110 GB로 증가 합니다.
    
- 사용자의 기본 및 보관 사서함에 있는 항목은 유지 됩니다.
    
## <a name="before-you-begin"></a>시작하기 전에

- exchange online 사서함에 소송 보존을 적용 하려면 exchange online 계획 2 라이선스를 할당 받아야 합니다. 사서함에 Exchange online 계획 1 라이선스가 할당 되는 경우이를 보류 상태로 설정 하려면 별도의 exchange online 보관 라이선스를 할당 해야 합니다.
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a>Office 365 관리 센터에서 사서함에 소송 보존 설정

다음은 Office 365 관리 센터를 사용 하 여 maibox에 소송 보존을 적용 하는 단계입니다.

1. 로 이동 https://portal.office.com/adminportal/home 하 고 전역 관리자 계정을 사용 하 여 로그인 합니다.
2. 왼쪽 탐색 창에서 **사용자** > **활성 사용자** 를 클릭 합니다.
3. 사서함에 소송 보존을 적용 하려는 사용자를 선택 합니다.
4. 플라이 아웃 페이지에서 **메일 설정을**클릭 한 다음 **소송 보존**옆의 **편집** 을 클릭 합니다.
5. **소송 보존** 페이지에서 설정/해제를 클릭 하 여 소송 보존을 설정 하 고 표시 되는 다음 선택적 설정을 완료 합니다.
 
    ![O365_LitigationHold1-.png](media/O365-LitigationHold1.png)

    a: **보존 기간 (일)** -이 상자를 사용 하 여 시간 기반 보존을 만들고 사서함이 소송 보존 상태에 있을 때 사서함 항목이 보관 되는 기간을 지정 합니다. 기간은 사서함 항목을 받거나 만든 날짜 로부터 계산 됩니다. 이 상자를 비워 두면 항목이 무기한으로 또는 보존이 제거 될 때까지 유지 됩니다. 기간을 지정 하려면 days를 사용 합니다.
    
    b. **참고** -이 상자를 사용 하 여 사용자의 사서함이 소송 보존 상태에 있음을 알립니다. 메모는 Outlook 2010 이상 버전을 사용 중인 경우 사용자 사서함의 계정 정보 페이지에 표시 됩니다. 사용자는이 페이지에 액세스 하 여 Outlook에서 **파일** 을 클릭할 수 있습니다.
     
    c. **웹 페이지** -소송 보존에 대 한 자세한 내용은이 상자를 사용 하 여 웹 사이트를 사용자에 게 안내 합니다. 이 URL은 사용자 사서함의 계정 정보 페이지에서 Outlook 2010 이상 버전을 사용 하는 경우에 표시 됩니다. 사용자는이 페이지에 액세스 하 여 Outlook에서 **파일** 을 클릭할 수 있습니다.
 
6. **저장** 을 클릭 하 여 소송 보존을 만듭니다.

보류를 만든 후에는 플라이 아웃 페이지의 메일 설정에 선택한 사용자에 대 한 소송 보류가 설정 된 것으로 표시 됩니다.

![O365_LitigationHold2-.png](media/O365-LitigationHold2.png)

소송 보존을 만들고 관리 하는 방법과 Exchange Online PowerShell을 사용 하 여 소송 보존을 대량으로 만드는 방법에 대 한 자세한 내용은 [사서함에 소송 보존](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold)을 참조 하십시오.
