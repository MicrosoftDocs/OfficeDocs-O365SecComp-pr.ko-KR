---
title: 보류 알림 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: fa83a90448250a91d6c2ccbf43588ee18e00619c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241265"
---
# <a name="manage-hold-notifications"></a>보류 알림 관리

법적 보존 알림 워크플로를 시작한 후에는 고급 eDiscovery (미리 보기)를 활용 하 여 통신 상태를 추적할 수 있습니다. Communications 탭에는 고급 eDiscovery (미리 보기) 사례 내의 모든 보존 알림이 포함 됩니다. 여기에서 세부 정보 (예: 지정 된 custodians 수 또는 통지를 승인 받은 개수)를 볼 수 있습니다.

## <a name="view-communication-details"></a>통신 세부 정보 보기

### <a name="track-acknowledgements"></a>승인 추적

**통신**탭에서 통신을 선택한 후에는 보류 알림을 승인 하는 custodians 목록을 볼 수 있습니다. 

### <a name="preview-acknowledgements"></a>미리 보기 승인

통신 세부 정보 플라이 아웃에서 법적 보존 통신에 대 한 세부 정보를 미리 볼 수 있습니다. **미리 보기** 패널에는 워크플로 알림의 설정 및 콘텐츠 뿐만 아니라 법적 보존 알림을 빠르게 확인할 수 있습니다. 미리 보기 패널에도 통지를 이미 승인한 custodians에 대 한 세부 정보가 표시 됩니다.

## <a name="taking-action-on-existing-communications"></a>기존 통신에 대 한 작업 수행

### <a name="re-send-a-hold-notice"></a>보류 알림 다시 보내기

경우에 따라 custodians에서 일상 업무로 인 한 전자 메일을 추적 하지 못하게 됩니다. 또는 오랫동안 실행 되는 소송에 대 한 custodian에 연락 하 여 알림을 다시 보낼 수 있습니다. 법적 보존 알림을 사용 하 여 워크플로를 관리할 때는 알림을 다시 보내 사용자 사서함의 "맨 위로" 이동 해야 할 수 있습니다.

다음을 수행 하 여 custodian에 보류 알림을 다시 보낼 수 있습니다.
1. **보안 및 준수 > Advanced eDiscovery (Preview)** 내의 사례를 탐색 합니다.
2. 사례를 선택한 후 **통신** 탭으로 이동 합니다.
3. 법적 보존 알림을 custodian에 다시 보내려면 통신을 선택 하 고 **다시 보내기** 옵션을 클릭 합니다.
4. custodian에서 해당 보존 알림을 아직 승인 하지 않은 경우 미리 알림 및 에스컬레이션 흐름이 다시 시작 됩니다. custodian에서 이미 보존 알림을 승인 했다면 custodian는 초기 보존 알림의 복사본만 받게 됩니다.

> [!NOTE]
> 통신에 할당 된 custodians에만 법적 보존 알림을 다시 보낼 수 있습니다. 

### <a name="edit-a-communication"></a>통신 편집

#### <a name="update-preservation-requirements"></a>업데이트 보존 요구 사항
  
사례가 진행 됨에 따라 custodians는 이전에 지시 된 것 보다 더 많은 데이터를 보존 해야 할 수 있습니다. eDiscovery 용어를 사용 하는 경우 업데이트 된 콘텐츠로 보존 알림을 다시 발행 해야 합니다.

초기 보존 알림의 내용을 업데이트 하려면 다음을 수행 합니다.

1. **보안 및 준수 > Advanced eDiscovery (Preview)** 내의 사례를 탐색 합니다.
2. 사례를 선택한 후 **통신** 탭으로 이동 합니다.
3. 업데이트할 보존 알림을 선택 하 고 **편집**을 클릭 합니다.
4. 워크플로 편집에서 **포털 콘텐츠 정의** 및 알림 내용 업데이트를 선택 합니다. 
5. **저장**을 클릭합니다. 저장 한 후에는 법적 고 지 사항에 현재 할당 되어 있는 모든 custodians에 게 재발급 알림이 전송 됩니다. 또한 미리 알림/에스컬레이션 알림을 사용 하도록 설정 된 경우 이러한 워크플로도 다시 시작 됩니다. 


#### <a name="update-legal-hold-notifications-and-settings"></a>법적 보존 알림 및 설정 업데이트

발급, 릴리스, 재발급, 미리 알림 또는 에스컬레이션 알림의 콘텐츠 또는 설정을 업데이트할 때 이러한 변경 내용은 워크플로에서 생성 되는 모든 이후 통신에 적용 됩니다.

## <a name="related-information"></a>관련 정보 

- [법적 보존 알림 만들기](create-hold-notification.md)
    
- [보류 알림 승인](acknowledge-hold-notification.md)
    
- [보유자를 사례에 추가](add-custodians-to-case.md)