---
title: Office 365의에서 소송 보존 만들기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: 18b3b3a42e5671b1507522c89faaa4ae34198831
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533895"
---
# <a name="create-a-litigation-hold-in-office-365"></a>Office 365의에서 소송 보존 만들기

삭제 된 항목 및 수정 된 항목의 원래 버전을 포함 하 여 모든 사서함 콘텐츠를 유지 하려면 소송 보존으로 설정에서 사서함을 배치할 수 있습니다. 소송 보존으로 설정에서 사용자 사서함을 할 때 사용자의 보관 사서함의 콘텐츠 (활성화 되어 있음) 하는 경우도 그대로 유지 됩니다. 보류를 만들 때는 하 여 삭제 보류 기간 ( *시간 기반 보존*라고도 함)을 지정할 수 및 수정 된 항목은 지정된 된 기간 동안 보존 사서함에서 영구적으로 삭제 합니다. 또는 콘텐츠를 무기한 보존 방금 수 ( *무한 대기*는 라고 함) 되거나 제거 되는 소송 보존으로 설정 합니다. 보류 기간 동안 지정 수행, 메시지를 받은 또는 사서함 항목을 만들 날짜부터 계산 됩니다. 
  
소송 보존을 만들 때 수행 되는 작업 다음과 같습니다.
  
- 사용자가 영구적으로 삭제 된 항목 보존 기간에 대 한 사용자의 사서함에서 복구 가능한 항목 폴더에 유지 됩니다.
    
- 사용자가 복구 가능한 항목 폴더에서 삭제 된 항목 보존 기간 동안 유지 됩니다.
    
- 복구 가능한 항목 폴더에 대 한 저장소 할당량은 30GB에서 110 g B로 증가 되었습니다.
    
- 사용자의 기본 및 보관 사서함에 대 한 항목의 보존
    
## <a name="before-you-begin"></a>시작하기 전에

- Exchange Online 사서함에 소송 보존 하려면, Exchange Online 계획 2 라이선스를 할당 해야 합니다. 사서함이 Exchange Online 계획 1 라이선스에 할당 하는 경우에 보류에 추가 하는 별도 Exchange Online 보관 라이선스가 할당 해야 합니다.
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a>전체 사서함에 소송 보존으로 Office 365 관리 센터에서 설정

Office 365 관리 센터를 사용 하 여 소송 보존으로 설정에 트리거하를 배치 하는 단계는 다음과 같습니다.

1. 이동 https://portal.office.com/adminportal/home 및 전역 관리자 계정을 사용 하 여 로그인 합니다.
2. **사용자가**를 클릭 > 왼쪽된 탐색 창의**현재 사용자** 입니다.
3. 사용자 사서함을 소송 보존에 배치를 선택 합니다.
4. 플라이 아웃 페이지에서 **메일 설정**을 클릭 하 고 **소송 보존으로 설정**옆에 있는 **편집** 을 클릭 합니다.
5. **소송 보존으로 설정** 페이지에서 설정 소송 보존으로 설정 하 고 표시 되는 다음과 같은 옵션 설정을 완료 표시/숨기기를 클릭 합니다.
 
    ![O365_LitigationHold1.png](media/O365-LitigationHold1.png)

    a. **보존 기간 (일)** -이 상자를 사용 하 여 시간 기반 보존을 만들고 사서함이 소송 보존으로 설정 중일 때 사서함 항목이 보관 되는 기간을 지정 합니다. 사서함 항목을 받거나 만든 날짜에서 기간 계산 됩니다. 이 상자를 비워두면 하는 경우 항목은 무기한 또는 보존이 제거 될 때까지 보관 됩니다. 기간을 지정 하려면 날짜를 사용 합니다.
    
    b. **메모** -이 상자를 사용 하 여 자신의 사서함이 소송 보존으로 설정 하는 사용자에 게 알리기를 합니다. Outlook 2010 이상 사용 하 여 하는 경우 사용자의 사서함에서 계정 정보 페이지에 메모가 표시 됩니다. 이 페이지에 액세스 하려면 사용자가 Outlook에서 **파일** 클릭 수 있습니다.
     
    이 상자를 사용 하 여 소송 보존으로 설정 하는 방법에 대 한 자세한 내용은 웹사이트에 사용자를 리디렉션하는 c. **웹 페이지** . Outlook 2010 이상를 사용 하는 경우이 URL이 사용자의 사서함에서 계정 정보 페이지에 나타납니다. 이 페이지에 액세스 하려면 사용자가 Outlook에서 **파일** 클릭 수 있습니다.
 
6. 소송 보존 만들려는 **저장** 을 클릭 합니다.

보류를 만든 후 플라이 아웃 페이지에서 메일 설정 소송 보존으로 설정 켜져 있는지 선택한 사용자를 표시 합니다.

![O365_LitigationHold2.png](media/O365-LitigationHold2.png)

만들기 (영문) 및 소송 보존을 포함 하 고 관리 하 고 Exchange Online PowerShell을 사용 하 여 대량 만들기 소송 보유 하는 방법에 대 한 자세한 내용은 [전체 사서함에 소송 보존으로 설정](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold)을 참조 하십시오.
