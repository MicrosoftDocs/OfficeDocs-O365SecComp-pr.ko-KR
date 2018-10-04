---
title: Office 365 SharePoint 온라인 데이터 삭제
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: SharePoint Online에서 데이터 삭제에 대 한 설명을 합니다.
ms.openlocfilehash: 97f3eaea471c08ba61c0fc749b806c1960c0182f
ms.sourcegitcommit: ee1d7037d9ad14d7f0dbc53114177a3d04614d6e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25402042"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a>Office 365의에서 SharePoint Online 데이터 삭제

SharePoint Online 응용 프로그램 데이터베이스 내에서 추상화 된 코드로 개체를 저장합니다. SharePoint Online에 파일을 업로드 하는 사용자 때 해당 파일은 분해 하 고 응용 프로그램 코드로 변환 하 고 여러 데이터베이스에 걸쳐 여러 테이블에 저장 합니다. SharePoint Online에서 고객을 업로드 하는 모든 콘텐츠 (잠재적으로 사용 하 여 암호화 여러 AES 256 비트 키), 청크를 나누어 이며 데이터 센터에 걸쳐 분산 합니다. 청크와 암호화 프로세스에 대 한 구체적인 정보에 대 한 [Microsoft 클라우드에서 암호화](office-365-encryption-in-the-microsoft-cloud-overview.md)를 참조 하십시오. SharePoint Online 데이터 손실을 방지 하려면 데이터 보호 서비스 제공 됩니다. 특히, 백업은 12 시간 마다 수행 되며 14 일 동안 보존 됩니다.

SharePoint Online 사이트에서 콘텐츠를 삭제 하면 즉시 삭제 되지 않습니다. 필요한 경우을 사이트 휴지통으로, 여기서 복원할 수, 보내집니다. (참조 [삭제 된 사이트 모음 휴지통에서 항목 복원](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) 복원 단계에 대 한). 기본 사이트 휴지통 보존 시간은 약 90 일입니다. 사이트 휴지통에서 콘텐츠를 삭제 하는 경우 사이트 모음 휴지통으로, 93 일의 보존 기간에는 전송 됩니다. 관리자가 휴지통에서 항목을 유지 하는 시간을 구성할 수 있습니다 하지만 기본 보존 기간은 약 90 일이 없는 경우에는, 합니다. 사이트 모음 저장 용량 할당량 및 [목록 보기 임계값](https://support.office.com/article/List-View-Threshold-b8588dae-9387-48c2-9248-c24122f07c59)에 대해 사이트 recycle bin 저장소를 계산합니다.

사이트 모음을 삭제 하는 경우에 컬렉션에 있는 모든 콘텐츠 및 사용자 정보를 포함 하는 사이트의 계층 구조를 삭제 하려는 있습니다.
- 문서 및 문서 라이브러리
- 목록 및 목록 데이터
- 사이트 구성 설정
- 사이트 또는 사이트의 하위 사이트와 관련 된 역할 및 보안 정보
- 하위 사이트의 최상위 웹사이트, 콘텐츠 및 사용자 정보

사이트 모음을 삭제 하기 전에에서는 SharePoint Online 사이트에 대 한 Microsoft에 의해 유지 관리 하는 데이터 백업 일정에 설명 하는 계획을 위한 SharePoint Online 서비스 설명을 검토 하는 것이 좋습니다. 또한 백업에서 복원을 수 있는 메모는 사이트 모음 또는 하위 사이트, 파일, 목록 또는 라이브러리에 대해서만 있습니다. 이러한 복구 해야하는 경우 휴지통을 사용 합니다. 사이트 모음을 실수로 삭제 한 경우 복원할 수는 사이트 모음 휴지통에서 사이트 모음 관리자가 93 일 이내입니다.

하드 삭제 하거나 [Remove-spodeletedsite cmdlet](https://docs.microsoft.com/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps)을 사용 하 여 사이트 모음을 영구적으로 삭제 하는 관리자는 사용자가 사이트 휴지통에서 삭제 된 항목을 제거 하 고 보존 및 백업 기간 만료 될 때 발생 합니다. 사용자 하드 삭제 하는 경우 (영구적으로 삭제 또는 제거) SharePoint Online에서 콘텐츠를 삭제 된 청크에 대 한 모든 암호화 키도 삭제 됩니다. 이전에 삭제 된 청크를 저장 하는 디스크에 대 한 차단은 사용 하지 않는 되어 사용할 수는 다시 사용으로 표시 됩니다.
