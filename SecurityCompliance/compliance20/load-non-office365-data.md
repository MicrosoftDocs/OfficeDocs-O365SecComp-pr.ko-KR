---
title: 작업 집합에 비 Office 365 데이터 로드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 1dad52075303450673e7f48b87e2952e35629a5e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706089"
---
# <a name="load-non-office-365-data-into-a-working-set"></a>작업 집합에 비 Office 365 데이터 로드

Office 365 고급 eDiscovery와 분석 해야할 수 있는 모든 문서는 Office 365에서 live 됩니다. 비-Office 365 콘텐츠가 포함 된 고급 eDiscovery로 분석 되어 있으므로 작업 집합으로 Office 365에서 살고 있지는 문서를 업로드할 수 있는 고급 eDiscovery의 기능을 가져옵니다. 이 절차를 분석을 위해 고급 eDiscovery에 Office 365가 아닌 문서를 가져오는 방법을 보여줍니다.

>[!Note]
>Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 Office 365 Enterprise E5 평가판을 등록할 수 있습니다.

## <a name="before-you-begin"></a>시작하기 전에
이 절차의 설명에 따라 업로드 비 Office 365 기능을 사용 하 여가 있어야 합니다.

- 고급 준수 추가 기능 또는 e 5 구독 Office 365 E3 합니다.

- Office 365가 아닌 콘텐츠가 업로드 될 모든 custodians 고급 준수 추가 기능 또는 e 5 라이선스 E3 있어야 합니다.

- 기존 eDiscovery 사례입니다.

- 더불어 당 하나의 폴더가 있으면 폴더의 이름은이 형식 *alias@domainname* 폴더에 업로드 하는 것에 대 한 파일을 모두 수집 합니다. 사용자가 Office 365 별칭 및 도메인 *alias@domainname* 이어야 합니다. 루트 폴더에 있는 모든 *alias@domainname* 폴더를 수집할 수 있습니다. 루트 폴더만 *alias@domainname* 폴더를 포함할 수을 루트 폴더에 넓게 파일이 없습니다 있어야 합니다.

- EDiscovery 관리자 또는 eDiscovery 관리자가 Microsoft Azure 저장소 도구를 Office 365가 아닌 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 설치 되는 계정입니다.

- 여기에서 수행할 수 있는 AzCopy를 설치 합니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>고급 eDiscovery에 Office 365가 아닌 콘텐츠를 업로드 합니다.

1. EDiscovery 관리자 또는 eDiscovery 관리자, 고급 eDiscovery 후에 Office 365가 아닌 데이터를 업로드는 대/소문자를 엽니다.  **집합 (영문)** 탭을 클릭 한 다음 비 Office 365 데이터를 로드 하려는 작업 집합을 선택 합니다.  작업 집합을 아직 만들지 않은 경우 그렇게 지금 수행할 수 있습니다.  마지막으로 클릭 하 고 **수행 하는 작업 관리 설정** 되지 않은 Office 365 데이터 섹션에서 **보기 업로드**

2. 비-Office 365 데이터 가져오기 마법사를 시작 하려면 **파일 업로드** 단추를 클릭 합니다.

![파일 업로드](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. 마법사의 첫번째 단계는 단순히 파일을 업로드 하도록에 대 한 보안 Azure blob를 준비 합니다.  준비 compelted 후에을 클릭 하 고 **다음: 파일을 업로드할** 단추.

![비 Office 365 가져오기-준비](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. **파일 업로드** 단계에서 **파일의 위치에 대 한 경로**지정 이것이 가져오기 (영문)에 계획 되지 않은 Office 365 데이터입니다.  명령은 제대로 업데이트는 AzCopy를 통해 올바른 위치를 설정 합니다.

> [!NOTE]
> AzCopy 아직 설치 하지 않은 경우 여기에서이 수행할 수 있습니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. **클립보드에 복사** 링크를 클릭 하 여 미리 정의 된 명령에 복사 합니다. Windows 명령 프롬프트를 시작 하 고 명령 붙여넣고 enter 키를 누릅니다.  다음 단계에 대 한 보안 Azure blob 저장소에 파일을 업로드 됩니다.

![비-Office 365 가져오기-파일 업로드](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![비 Office 365 가져오기-AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. 마지막으로, 보안 & 준수에 다시 반환 하 고 클릭 하 고 **다음: 파일을 처리** 단추.  이 처리, 텍스트 추출 및 업로드 된 파일의 인덱싱 시작 됩니다.  처리 여기 또는 **작업** 탭에서의 진행률을 추적할 수 있습니다.  완료 되 면 새 파일 작업 집합에서 제공 됩니다.  처리가 완료 되 면 마법사를 취소할 수 있습니다.

![비-Office 365 가져오기-파일 처리](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

