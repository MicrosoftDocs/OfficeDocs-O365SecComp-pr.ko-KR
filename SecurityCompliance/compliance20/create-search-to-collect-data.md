---
title: 검색을 만들어서 데이터 수집
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
ms.openlocfilehash: 14f90b29cbff9c1a588b816563178039c7af7da6
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243416"
---
# <a name="create-a-search-to-collect-data"></a>검색을 만들어서 데이터 수집

사례에 있는 **검색** 탭에서 **새 검색** 을 클릭 하 고 마법사를 수행 하 여 새 검색을 만들 수 있습니다.

## <a name="name-your-search-and-give-description"></a>검색 이름 지정 및 설명 입력

케이스가 포함 된 각 검색의 이름은 고유 해야 합니다. 선택적으로 검색에 대 한 설명을 제공할 수 있습니다. 

## <a name="define-your-conditions"></a>조건 정의

미리 작성 된 조건 카드를 사용 하거나 KQL (키워드 쿼리 언어)를 사용 하 여 검색 조건을 정의할 수 있습니다. 자세한 내용은 [빌드 검색 쿼리](building-search-queries.md)를 참조 하십시오.

## <a name="choose-the-custodians-to-search-from"></a>검색할 custodians 선택

조건을 정의한 후에는 검색 하려는 위치를 선택 해야 합니다. 이 작업을 수행 하는 한 가지 방법은 검색 하려는 사례에 이미 추가한 custodians를 지정 하는 것입니다. custodian를 선택 하 여 custodian에 매핑된 모든 데이터 원본에 대해 검색을 실행 합니다. 사례에 custodians을 추가 하 고 해당 데이터 원본을 관리 하는 방법에 대 한 자세한 내용은 [custodians with Work](managing-custodians.md) 를 참조 하십시오.

## <a name="choose-non-custodial-locations"></a>비 custodial 위치 선택

어떤 경우에는 custodian에 매핑되지 않은 데이터 원본을 검색할 수도 있습니다. 이 경우 검색할 위치를 지정 하거나, 모든 Exchange 사서함 또는 모든 SharePoint 및 비즈니스용 OneDrive 사이트 검색과 같은 특정 Office 365 서비스의 모든 콘텐츠 위치를 검색 하도록 선택할 수 있습니다.