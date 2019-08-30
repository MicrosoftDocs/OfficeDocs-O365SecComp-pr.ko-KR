---
title: EOP에서 관리자 역할 그룹 권한 관리
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: 관리자는 Exchange Online Protection의 EAC (Exchange 관리 센터)에서 사용 권한을 할당 하거나 제거 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: 7bd1a6959dd03a118608dfe45faa253fd56539d4
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676728"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a>EOP에서 관리자 역할 그룹 권한 관리
  
Microsoft EOP(Exchange Online Protection)에서는 EAC(Exchange 관리 센터)를 통해 사용자를 하나 이상의 역할 그룹 구성원으로 지정하여 해당 그룹에 특정 관리 작업을 수행하기 위한 권한을 할당할 수 있습니다. 또한 EAC를 사용하여 하나 이상의 역할 그룹에서 사용자를 제거할 수도 있습니다.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

- 예상 완료 시간: 5~10분

- Exchange 관리 센터를 열려면 exchange [Online Protection의 exchange 관리 센터](../exchange-admin-center-in-exchange-online-protection-eop.md)를 참조 하세요.

- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md)의 "사용자, 연락처 및 역할 그룹" 항목

- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대 한 자세한 내용은 [Exchange Online에서 exchange 관리 센터에 대 한 바로 가기 키](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)를 참조 하십시오.

> [!TIP]
> 문제가 있습니까? [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 포럼에서 도움을 요청 하세요.
  
## <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a>EAC를 사용하여 관리자 역할 그룹에 구성원 할당

1. EAC에서 **사용 권한** \> **관리자 역할로**이동 하 여 사용자를 추가 하려는 역할 그룹을 클릭 한 다음 편집 아이콘 **** ![](../media/ITPro-EAC-EditIcon.gif)편집을 클릭 합니다.

2. 구성원 아래에서 **** ![추가 아이콘](../media/ITPro-EAC-AddIcon.gif)추가를 클릭 합니다. 구성원 선택 창이 나타납니다.

3. 추가할 사용자를 한 명 이상 검색하거나 목록에서 선택합니다.

4. 추가할 사용자를 한 명 이상 선택한 후 **추가**, **확인**을 차례로 클릭합니다. 그러면 구성원 선택 창이 닫힙니다.

5. 사용자가 **구성원** 창에 추가된 것을 확인할 수 있습니다. **저장**을 클릭합니다.

   > [!NOTE]
   > 구성원을 역할 그룹에 추가하거나 역할 그룹에서 제거한 후 사용자가 관리 권한 변경 내용을 확인하려면 로그아웃했다가 다시 로그인해야 할 수 있습니다. 
  
## <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a>EAC를 사용하여 관리자 역할 그룹에서 구성원 제거

1. EAC에서 **사용 권한** \> **관리자 역할로**이동 하 여 사용자를 제거할 역할 그룹을 클릭 한 다음 편집 아이콘 **** ![](../media/ITPro-EAC-EditIcon.gif)편집을 클릭 합니다.

2. 구성원에서 제거할 사용자를 한 명 이상 선택 하 고 제거 아이콘](../media/ITPro-EAC-RemoveIcon.gif) **제거** ![를 클릭 합니다.

3. **저장**을 클릭하여 역할 그룹의 변경 내용을 저장하고 **관리자 역할** 페이지로 돌아갑니다. 사용자가 관리자 역할 그룹에서 제거되었는지 확인하려면 해당 구성원이 선택한 역할 그룹의 세부 정보 창에서 구성원 아래에 더 이상 표시되지 않는지 확인합니다.

   > [!NOTE]
   > 구성원을 역할 그룹에 추가하거나 역할 그룹에서 제거한 후 사용자가 관리 권한 변경 내용을 확인하려면 로그아웃했다가 다시 로그인해야 할 수 있습니다.
  
## <a name="for-more-information"></a>추가 정보

[EOP의 기능 사용 권한](feature-permissions-in-eop.md)
