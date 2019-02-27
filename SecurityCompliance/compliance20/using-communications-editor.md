---
title: 커뮤니케이션 편집기 사용
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
ms.openlocfilehash: c2957c88217bce4c9a34f8d3f9a9e291f1223cc9
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30294971"
---
# <a name="use-the-communications-editor"></a>커뮤니케이션 편집기 사용

포털 콘텐츠, 법적 보존 알림 및 관련 미리 알림/에스컬레이션의 콘텐츠를 정의할 때 통신 편집기를 활용 하 여 콘텐츠를 포맷 하 고 동적으로 사용자 지정할 수 있습니다.

## <a name="rich-text-editor"></a>서식 있는 텍스트 편집기 

사용자는 통신 편집기를 사용 하 여 편집기 옵션을 통해 텍스트를 사용자 지정할 수 있습니다. 예를 들어 사용자는 글꼴 종류를 변경 하 고, 글머리 기호 목록을 만들고, 콘텐츠를 강조 표시할 수 있습니다. 

## <a name="merge-field-variables"></a>병합 필드 변수

통신 편집기에서 전자 메일 병합 변수를 활용 하 여 사용자 지정 된 custodian 특성을 통신의 본문 텍스트에 포함할 수 있습니다. custodian로 전송 되 면 병합 필드에 해당 하는 필드가 채워집니다. 예를 들어 custodian John Smith에 게 보내면 병합 필드 [custodian Name]은 해당 이름으로 변환 됩니다. 

서식 있는 텍스트 편집기 컨트롤 위쪽에서 **병합 필드** 아이콘을 선택 하 여 전자 메일 병합 필드를 사용할 수 있습니다. 사용자 커서 위치에 따라 자리 표시 자가 추가 됩니다. 

### <a name="list-of-merge-field-variables"></a>병합 필드 변수 목록

| 필드 이름                  | 필드 세부 정보 | 
| :------------------- | :------------------- |
| 표시 이름  | custodian의 성과 이름입니다. | 
| 승인 링크 | 각 custodian의 승인을 기록 하기 위한 사용자 지정 링크입니다.|                 |
| 포털 링크     | custodian 준수 포털에 대 한 사용자 지정 링크입니다.|                |
| 관리자 발급                   | 지정한 발급 관리자의 전자 메일 주소입니다.|                   |
| 발급 날짜                   | 확인이 실행 된 날짜입니다 (UTC).              |