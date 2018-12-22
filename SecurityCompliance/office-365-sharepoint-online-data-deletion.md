---
title: Office 365 SharePoint 온라인 데이터 삭제
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: SharePoint Online에서 데이터 삭제에 대 한 설명을 합니다.
ms.openlocfilehash: 8a84859ce170a4c3ca713c751aef2b6d5b911c55
ms.sourcegitcommit: 29ba4c36af8e90ddc8d885863ef25bac2cffbe94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/22/2018
ms.locfileid: "27411164"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a>Office 365의에서 SharePoint Online 데이터 삭제

SharePoint Online 응용 프로그램 데이터베이스 내에서 추상화 된 코드로 개체를 저장합니다. SharePoint Online에 파일을 업로드 하는 사용자 때 해당 파일은 분해 하 고 응용 프로그램 코드로 변환 하 고 여러 데이터베이스에 걸쳐 여러 테이블에 저장 합니다. SharePoint Online에서 고객을 업로드 하는 모든 콘텐츠 (잠재적으로 사용 하 여 암호화 여러 AES 256 비트 키), 청크를 나누어 이며 데이터 센터에 걸쳐 분산 합니다. 청크와 암호화 프로세스에 대 한 구체적인 정보에 대 한 [Microsoft 클라우드에서 암호화](office-365-encryption-in-the-microsoft-cloud-overview.md)를 참조 하십시오. 

SharePoint Online에서 항목의 원래 위치에서 삭제할 시간부터 93 일 동안 보관 됩니다. 계속 해 서 표시 사이트의 휴지통에 전체 시간 경우가 아니면 다른 여기에서이 삭제는 휴지통을 비웁니다. 이 경우 사이트 모음 휴지통, 여기서 계속 해 서 표시 93 일의 나머지 부분에 대 한 항목 이동 합니다. 삭제 된 항목을 복원 하는 방법에 대 한 정보를 [SharePoint 사이트의 휴지통에서 항목을 복원](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) 하 고 [삭제 된 사이트 모음 휴지통에서 항목 복원을](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)참조 하십시오. 휴지통 보존 시간은 SharePoint Online에서 구성할 수 있습니다.

사이트 모음을 삭제 하는 경우에 폴더 내의 모든 콘텐츠는 컬렉션에는 사이트의 계층 구조 삭제 하려는:
- 문서 및 문서 라이브러리
- 목록 및 목록 데이터
- 사이트 구성 설정
- 사이트 또는 사이트의 하위 사이트와 관련 된 역할 및 보안 정보
- 하위 사이트의 최상위 웹사이트, 콘텐츠 및 사용자 정보

전역 또는 SharePoint 복원할 수는 사이트 모음을 실수로 삭제 한 경우 SharePoint 관리 센터를 사용 하 여 관리 합니다. 

하드 삭제 사용자는 보존 및 백업 기간 만료 또는 관리자가 [Remove-spodeletedsite cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps)을 사용 하 여 사이트 모음을 영구적으로 삭제 하는 경우 사이트 모음을 휴지통에서 삭제 된 항목을 제거 하는 경우에 발생 합니다. 사용자 하드 삭제 하는 경우 (영구적으로 삭제 또는 제거) SharePoint Online에서 콘텐츠를 삭제 된 청크에 대 한 모든 암호화 키도 삭제 됩니다. 이전에 삭제 된 청크를 저장 하는 디스크에 대 한 차단은 사용 하지 않는 되어 사용할 수는 다시 사용으로 표시 됩니다.
