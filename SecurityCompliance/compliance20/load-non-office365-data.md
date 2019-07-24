---
title: 검토 집합에 비 Office 365 데이터 로드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 고급 eDiscovery 사례에서 Office 이외 365 데이터를 검토 집합으로 가져옵니다.
ms.openlocfilehash: 37f8c2a5c97452845152e2a12578b9d243ab6711
ms.sourcegitcommit: 82ee560bf3ac84079764cbb4a2d858c321f65145
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/24/2019
ms.locfileid: "35840870"
---
# <a name="load-non-office-365-data-into-a-review-set"></a>검토 집합에 비 Office 365 데이터 로드

고급 eDiscovery에서 분석 하는 데 필요한 모든 문서가 Office 365에 있습니다. 고급 eDiscovery의 비 Office 365 데이터 가져오기 기능을 사용 하 여 Office 365에 없는 문서를 검토 집합에 업로드할 수 있습니다. 이 문서에서는 분석을 위해 비 Office 365 문서를 고급 eDiscovery로 가져오는 방법을 설명 합니다.

>[!Note]
>고급 eDiscovery에는 조직에 대 한 Microsoft 365 또는 Office 365 E5 구독 또는 고급 준수 추가 기능 구독이 포함 된 E3 구독이 필요 합니다. 고급 eDiscovery를 만들려고 하는 계획이 없는 경우 Office 365 Enterprise E5의 평가판에 등록할 수 있습니다.

## <a name="before-you-begin"></a>시작하기 전에

이 문서에서 설명 하는 Office 이외 365 업로드 기능을 사용 하려면 다음이 필요 합니다.

- 비 Office 365 콘텐츠를 연결 하려는 모든 custodians에는 E5 라이선스 또는 고급 준수 추가 기능 라이선스가 포함 된 E3 라이선스가 할당 되어야 합니다.

- 기존 고급 eDiscovery 사례

- 비 Office 365 데이터를 업로드 하 고 여기에 연결 하려면 Custodians를 사례에 추가 해야 합니다.

- Office가 아닌 365 데이터는 고급 eDiscovery에서 지 원하는 파일 형식 이어야 합니다. 자세한 내용은 [Advanced eDiscovery에서 지원 되는 파일 형식을](supported-filetypes-ediscovery20.md)참조 하세요.

- 검토 집합에 업로드 되는 모든 파일은 각 폴더가 특정 custodian 연결 되는 폴더에 있어야 합니다. 이러한 폴더의 이름은 *alias @ domainname*을 사용 해야 합니다. *Alias @ domainname* 은 사용자의 Office 365 별칭 및 도메인 이어야 합니다. 루트 폴더에 있는 모든 *alias @ domainname* 폴더를 수집할 수 있습니다. 루트 폴더에는 *alias @ domainname* 폴더만 포함 될 수 있습니다. 루트 폴더의 느슨한 파일은 지원 되지 않습니다.

   업로드할 비 Office 365 데이터에 대 한 폴더 구조는 다음 예와 비슷합니다.

   - c:\nonO365\abraham.mcmahon@contoso.com
   - c:\nonO365\jewell.gordon@contoso.com
   - c:\nonO365\staci.gonzalez@contoso.com

   여기서 abraham.mcmahon@contoso.com, jewell.gordon@contoso.com 및 staci.gonzalez@contoso.com는 대/소문자에서 custodians의 SMTP 주소입니다.

   ![Office가 아닌 365 데이터 업로드 폴더 구조](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- EDiscovery 관리자 역할 그룹에 할당 되 고 eDiscovery 관리자로 추가 된 계정입니다.

- Office가 아닌 365 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 설치 된 Microsoft Azure Storage Tools입니다. AzCopy을 설치 하려면 [AzCopy 시작](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy)하기를 참조 하세요. 기본 위치인 **% ProgramFiles (x86)% \ Microsoft SDKs\Azure\AzCopy**에 AzCopy을 (를) 설치 해야 합니다.


## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Office 이외의 365 콘텐츠를 고급 eDiscovery에 업로드

1. EDiscovery 관리자 또는 eDiscovery 관리자로 서, 고급 eDiscovery를 열고 비 Office 365 데이터가 업로드 되는 사례를 엽니다.  

2. **검토 집합**을 클릭 한 다음 검토 집합을 선택 하 여 비 Office 365 데이터를 업로드 합니다.  검토 집합이 없는 경우에는 해당 집합을 만들 수 있습니다. 
 
3. 검토 집합에서 **검토 설정 관리**를 클릭 한 다음 **비 Office 365 데이터** 타일에서 **업로드 보기** 를 클릭 합니다.

4. **파일 업로드** 를 클릭 하 여 비 Office 365 데이터 가져오기 마법사를 시작 합니다.

   ![파일 업로드](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

   마법사의 첫 번째 단계에서는 Microsoft에서 제공한 안전한 Azure 저장소 위치를 준비 하 여 파일을 업로드 합니다.  준비가 완료 되 면 **다음: 파일 업로드** 단추가 활성화 됩니다.

   ![비 Office 365 가져오기: 준비](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
5. **다음: 파일 업로드**를 클릭 합니다.

6. **파일 업로드** 페이지에서 다음을 수행 합니다.

   ![비 Office 365 가져오기: 파일 업로드](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   위한. **파일 위치 경로** 상자에서 업로드 하려는 비 Office 365 데이터를 저장 한 루트 폴더의 위치를 확인 하거나 입력 합니다. 예를 들어 **시작 하기 전에 구역**에 표시 된 예제 파일의 위치에는 **%USERPROFILE\Downloads\nonO365**를 입력 합니다. 올바른 위치를 제공 하면 경로 아래의 상자에 표시 되는 AzCopy 명령이 제대로 업데이트 됩니다.

   b. 상자에 표시 된 명령을 복사 하려면 **클립보드에 복사** 를 클릭 합니다. Windows 명령 프롬프트를 시작 하 고 명령을 붙여 넣은 다음 enter 키를 누릅니다.  파일이 보안 Azure blob 저장소에 업로드 되 고 다음 단계를 진행 합니다.

7. Windows 명령 프롬프트를 시작 하 고 이전 단계에서 복사한 명령을 붙여 넣은 다음 enter 키를 눌러 AzCopy **** 명령을 시작 합니다.  명령을 시작한 후에는 Office가 아닌 365 파일이 4 단계에서 준비 된 Azure 저장소 위치로 업로드 됩니다.

   ![비 Office 365 가져오기: AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > 제공 된 AzCopy 명령이 실패 하면 [Advanced eDiscovery에서 AzCopy 문제 해결](troubleshooting-azcopy.md) 을 참조 하세요.

8. 보안 & 준수 센터로 돌아간 후 **다음: 마법사에서 프로세스 파일** 을 클릭 합니다.  이렇게 하면 Azure 저장소 위치로 업로드 된 비 Office 365 파일의 처리, 텍스트 추출 및 인덱싱이 시작 됩니다.  

9. **검토 집합에 365 부재 중 365 데이터를 추가**하는 작업을 확인 하 여 **프로세스 파일** 페이지 또는 **작업** 탭에서 office 이외 범위의 파일 처리 진행률을 추적 합니다.  작업이 완료 되 면 검토 집합에서 새 파일을 사용할 수 있습니다.

   ![비 Office 365 가져오기: 프로세스 파일](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

10. 처리가 완료 되 면 마법사를 닫을 수 있습니다.