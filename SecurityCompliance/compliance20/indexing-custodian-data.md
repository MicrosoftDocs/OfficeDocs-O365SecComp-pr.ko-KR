---
title: 보유자 데이터의 고급 인덱싱
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218668"
---
# <a name="advanced-indexing-of-custodian-data"></a>보유자 데이터의 고급 인덱싱

고급 eDiscovery (미리 보기) 사례에 custodian을 추가 하면 부분적으로 인덱싱된 것으로 간주 되는 Office 365의 콘텐츠가 완전히 검색 가능 하도록 다시 처리 됩니다.  이 프로세스를 *고급 인덱싱*이라고 합니다. 이미지의 존재 여부, 지원 되지 않는 파일 형식 또는 파일 크기 제한에 도달 하는 경우에는 여러 가지 이유로 인해 콘텐츠를 부분적으로 인덱싱할 수 있습니다.  부분적으로 인덱싱된 항목에 대 한 자세한 내용은 [Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)을 참조 하세요.

## <a name="viewing-advanced-indexing-results"></a>고급 인덱싱 결과 보기

고급 인덱싱 프로세스가 완료 되 면 다시 처리할 때의 효과를 이해 하는 데 도움이 될 수 있습니다.  Custodian 인덱싱 보기에서 그래프에는 *하이브리드 인덱스*에 추가 된 모든 항목이 나열 됩니다.  하이브리드 인덱스는 고급 eDiscovery (미리 보기)에서 다시 처리 된 콘텐츠가 저장 되는 위치입니다.

또한 그래프에는 수정이 필요한 항목 수와 파일 형식별로 다른 오류 그래프가 포함 되어 있습니다. 자세한 내용은 [데이터를 처리할 때 오류 수정을](error-remediation.md)참조 하십시오.

## <a name="updating-advanced-indexes-for-custodians"></a>custodians에 대 한 고급 인덱스 업데이트

고급 eDiscovery (미리 보기) 케이스에 custodian을 추가 하면 부분적으로 인덱싱된 항목이 모두 다시 처리 됩니다. 그러나 시간 경과에 따라 보다 부분적으로 인덱싱된 항목이 사용자의 사서함 또는 OneDrive 계정에 추가 될 수 있습니다.  필요한 경우 인덱스를 업데이트할 수 있습니다.

> [!NOTE]
> custodian 인덱스를 업데이트 하는 과정은 장기 실행 프로세스입니다. 인덱스를 하루에 한 번 이상 업데이트 하지 않는 것이 좋습니다.
