---
title: 작업 집합에 비 Office 365 데이터 로드
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
ms.openlocfilehash: 2ac12cf8c447e3341724d9e853da0f32b7c232fb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242957"
---
# <a name="load-non-office-365-data-into-a-working-set"></a>작업 집합에 비 Office 365 데이터 로드

office 365 Advanced eDiscovery를 사용 하 여 분석 해야 하는 모든 문서는 office 365에 살고 있습니다. 고급 ediscovery의 office가 아닌 365 콘텐츠 가져오기 기능을 사용 하 여 office 365에 없는 문서를 고급 ediscovery로 분석 하도록 작업 집합에 업로드할 수 있습니다. 이 절차에서는 분석을 위해 비 Office 365 문서를 고급 eDiscovery로 가져오는 방법을 보여 줍니다.

>[!Note]
>고급 eDiscovery를 사용 하려면 조직의 고급 준수 추가 기능 또는 E5 구독에 Office 365 E3이 필요 합니다. 고급 eDiscovery를 만들려고 하는 계획이 없는 경우 Office 365 Enterprise E5의 평가판에 등록할 수 있습니다.

## <a name="before-you-begin"></a>시작하기 전에
이 절차에 설명 된 대로 Office 이외에 업로드 365 기능을 사용 하려면 다음이 필요 합니다.

- 고급 규정 준수 추가 기능 또는 E5 구독을 포함 하는 Office 365 E3

- 비 Office 365 콘텐츠가 업로드 되는 모든 custodians에는 고급 규정 준수 추가 기능 또는 E5 라이선스가 포함 된 E3이 있어야 합니다.

- 기존 eDiscovery 사례

- 업로드 하기 위한 모든 파일은 custodian 마다 폴더가 하나이 고 폴더 이름이이 형식 *별칭 @ domainname* 에 있는 폴더로 수집 됩니다. *alias @ domainname* 은 사용자의 Office 365 별칭 및 도메인 이어야 합니다. 모든 *alias @ domainname* 폴더를 루트 폴더로 수집할 수 있습니다. 루트 폴더에는 *별칭 @ domainname* 폴더만 포함할 수 있으며 루트 폴더에는 느슨한 파일이 없어야 합니다.

   업로드할 계획인 비 Office 365 데이터에 대 한 폴더 구조는 다음과 같습니다.

   - c:\nonO365\abraham.mcmahon@contoso.com
   - c:\nonO365\jewell.gordon@contoso.com
   - c:\nonO365\staci.gonzalez@contoso.com

   여기서 abraham.mcmahon@contoso.com, jewell.gordon@contoso.com 및 staci.gonzalez@contoso.com는 custodians의 SMTP 주소입니다.

![Office가 아닌 365 데이터 업로드 폴더 구조](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- 비 Office 365 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 ediscovery 관리자 또는 ediscovery 관리자 Microsoft Azure Storage Tools가 설치 되어 있는 계정입니다.

- 다음에서 수행할 수 있는 AzCopy을 설치 합니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Office 이외의 365 콘텐츠를 고급 eDiscovery에 업로드

1. ediscovery 관리자 또는 ediscovery 관리자로 서, 고급 eDiscovery를 열고 비 Office 365 데이터가 업로드 되는 사례를 엽니다.  **작업 집합** 탭을 클릭 한 다음 비 Office 365 데이터를 로드할 작업 집합을 선택 합니다.  작업 집합을 아직 만들지 않은 경우 지금 만들 수 있습니다.  마지막으로, 기능 **집합 관리** 를 클릭 하 고 비 Office 365 데이터 섹션에서 **업로드를 확인** 합니다.

2. **파일 업로드** 단추를 클릭 하 여 비 Office 365 데이터 가져오기 마법사를 시작 합니다.

![파일 업로드](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. 마법사의 첫 번째 단계에서는 업로드할 파일에 대 한 안전한 Azure blob만 준비 합니다.  준비가 완료 되 면 **다음: 파일 업로드** 단추를 클릭 합니다.

![비 Office 365 가져오기-준비](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. **파일 업로드** 단계에서 **파일의 위치에 대 한 경로**를 지정 합니다. 여기서는 가져오기에 사용 하는 비 Office 365 데이터가 있는 위치입니다.  올바른 위치를 설정 하면 AzCopy 명령이 제대로 업데이트 됩니다.

> [!NOTE]
> AzCopy을 아직 설치 하지 않은 경우 여기에서이 작업을 수행할 수 있습니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. **클립보드에 복사** 링크를 클릭 하 여 미리 정의 된 명령을 복사 합니다. windows 명령 프롬프트를 시작 하 고 명령을 붙여 넣은 다음 enter 키를 누릅니다.  파일이 보안 Azure blob 저장소에 업로드 되 고 다음 단계를 진행 합니다.

![Office가 아닌 365 가져오기-업로드 파일](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![비 Office 365 가져오기-AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

> [!NOTE]
> 제공 된 AzCopy 명령이 실패 하면 [Advanced eDiscovery (Preview)에서 AzCopy 문제 해결](troubleshooting-azcopy.md) 을 참조 하세요.

6. 마지막으로 보안 & 규정 준수로 돌아간 후 **다음: 프로세스 파일** 단추를 클릭 합니다.  이렇게 하면 업로드 된 파일의 처리, 텍스트 추출 및 인덱싱이 시작 됩니다.  여기에서 처리의 진행 상황과 **작업** 탭을 추적할 수 있습니다.  완료 되 면 새 파일을 작업 집합에서 사용할 수 있게 됩니다.  처리가 완료 되 면 마법사를 해제할 수 있습니다.

![Office가 아닌 365 가져오기 프로세스 파일](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

