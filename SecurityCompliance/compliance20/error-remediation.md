---
title: 데이터를 처리할 때 오류 수정
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
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608174"
---
# <a name="error-remediation-when-processing-data"></a>데이터를 처리할 때 오류 수정

오류 수정 eDiscovery 관리자 고급 eDiscovery (미리 보기) 콘텐츠를 제대로 처리 하지 못하도록 하는 데이터 문제를 해결 하는 기능을 허용 합니다. 예, 파일은 잠겨 되거나 암호화 된 이후 암호로 보호 된 파일을 처리할 수 없습니다. 오류 업데이트 관리를 사용 하 여 eDiscovery 관리자 수 이러한 오류와 함께 파일을 다운로드, 암호 보호를 제거 하 고 remediated 파일을 업로드 합니다.

다음과 같은 워크플로 사용 하 여 고급 eDiscovery (미리 보기)의 경우에는 오류와 함께 파일을 수정 합니다.

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a>오류 처리와 함께 파일을 수정 하는 오류 수정 세션 만들기 (영문)

>[!NOTE]
>하는 경우의 오류 수정 마법사는 다음 절차 중 언제 든 지 닫혀를 반환할 수 있습니다 오류 수정 세션에 **처리** 탭에서 **보기** 에 대 한 드롭다운 메뉴에서에서 **오류 개선** 를 선택 하 여 합니다.

1. 고급 eDiscovery (미리 보기) 사례 **처리** 탭에서 **보기** 에 대 한 드롭다운 메뉴에서에서 **오류** 를 선택 합니다.

2. 오류 유형 또는 파일 형식 옆에 있는 라디오 단추를 클릭 하 여 수정 하려는 오류를 선택 합니다.  다음 예제에서는 암호로 보호 된 파일을 수정 하는 합니다.

3. **+ 새 오류 업데이트 관리를**클릭 합니다.

    ![오류 수정](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    오류 수정 세션이 시작로 시작 하 여 준비 단계는 오류가 발생 하는 파일은 이동 되는 위치 Azure 안전한 위치에 다운로드할 수 있습니다.

    ![오류 수정 준비](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. 준비 완료 되 면 클릭 **다음: 파일을 다운로드** 다운로드 계속 진행할 수 있도록 합니다.

    ![파일 다운로드](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. 파일을 다운로드 하려면 **다운로드에 대 한 대상 경로**;를 지정 합니다. 파일을 다운로드 하 여 로컬 컴퓨터에 있는 경로입니다.  기본 경로 %USERPROFILE%\Downloads\errors, 로그인 한 사용자의 다운로드 폴더; 가리키는 필요에 따라 변경할 수 있습니다.

    >[!NOTE]
    >최적의 성능을 위해 원격 네트워크 경로 하는 대신 로컬 파일 경로 사용 하는 것이 좋습니다.

    > [!NOTE]
    > AzCopy를 설치 하지 않은 경우 여기에서 설치할 수 있습니다.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

6. **클립보드에 복사**를 클릭 하 여 미리 정의 된 명령에 복사 합니다. Windows 명령 프롬프트를 시작 하 고 명령에 붙여넣은 다음 **Enter**키를 누릅니다.  

    파일 다운로드 됩니다.

    ![오류 수정 준비](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > 이 명령을 실행 하는 문제를 사용 하는 경우 참조 https://go.microsoft.com/fwlink/?linkid=2038117 문제해결 팁입니다.

7. 파일을 다운로드 한 후 적절 한 수 있는 도구와 수정 수 있습니다. 암호로 보호 된 파일에 대 한 다양 한 암호 해독 도구를 사용할 수 있습니다. 파일에 대 한 암호를 알고 있는 경우에 열기 전에 수 있으며 암호 보호 기능을 제거할 수 있습니다.
    > [!NOTE]
    > IT은 그대로 유지 remediated 파일의 파일 이름과 디렉터리 구조를 유지 하는 것이 중요 합니다.  다운로드 한 파일에 사용 되는 모든 명명 규칙 및 폴더 수 있도록 원래 remdiated 파일에 연결 합니다.

8. 이제, 고급 eDiscovery (미리 보기)를 반환 하 고 클릭 **다음: 파일을 업로드할**합니다.  파일을 지금 업로드할 수 있는 다음 단계로 이동 됩니다.

    ![파일 업로드](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. **파일의 위치에 대 한 경로** 텍스트 상자에 remediated 파일의 위치를 지정 하기 위해 **clibpboard로 복사**를 클릭 합니다.

10. 명령은 Windows 명령 프롬프트에 붙여넣은 파일을 업로드 하려면 **Enter** 키를 누릅니다.

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. 마지막으로 고급 eDiscovery (미리 보기)를 반환 하 고 클릭 **다음: 파일을 처리**합니다.

12. 처리가 완료 되 면  작업 집합을 반환할 수 있으며 remediated 파일을 참조 하십시오.

## <a name="what-happens-when-files-are-remediated"></a>파일은 설정을 할 때 수행 하는 작업

설정을 파일 업로드 된 하는 경우에 다음 필드를 제외 하 고 원래 메타 데이터 보존 됩니다. 

- DocumentExtractedUrl
- ExtractedTextSize
- HasText
- IsErrorRemediate
- IsParentExtractedUrl
- ItemExtractedUrl
- LoadId
- ProcessingErrorMessage
- 상태
- 텍스트
- WordCount
- WorkingsetId

고급 eDiscovery (미리 보기)의 모든 문서 메타 데이터 필드의 정의 [문서 메타 데이터 필드](document-metadata-fields.md)를 참조 하십시오.