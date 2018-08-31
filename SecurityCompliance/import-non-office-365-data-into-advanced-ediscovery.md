---
title: Advanced eDiscovery 분석을 위해 비 Office 365 콘텐츠 가져오기
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: 어떻게 o 365에는 Azure에 저장 되지 않은 콘텐츠를 가져올 단계로 AeD와 분석할 수 있도록 blob
ms.openlocfilehash: ab6c7ac76a159603a34719aa8edb51de3a4fabbb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534162"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a>Advanced eDiscovery 분석을 위해 비 Office 365 콘텐츠 가져오기

Office 365 고급 eDiscovery와 분석 해야할 수 있는 모든 문서는 Office 365에서 live 됩니다. 비-Office 365 콘텐츠가 포함 된 고급 ediscovery 사례 연결 된, Azure 저장소 blob로 (PST 파일)을 제외한 Office 365에 거주 하 고 고급 eDiscovery 사용 하 여 분석 하지는 문서를 업로드할 수 있는 기능을 가져옵니다. 이 절차를 분석을 위해 고급 eDiscovery에 Office 365가 아닌 문서를 가져오는 방법을 보여줍니다.
  
> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
> [!NOTE]
> Office 365가 아닌 콘텐츠는 Office 365 고급 eDiscovery 데이터 저장소 추가 기능 구독을 구입할 수 있습니다. 이 고급 eDiscovery를 사용 하 여 분석 되어야 하는 콘텐츠에 대 한 단독으로 사용할 수 있습니다. [구입 하거나 편집 하 고 비즈니스를 위한 Office 365에 대 한 추가 기능의](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) 단계를 수행 하 고 Office 365 고급 eDiscovery 저장소 추가 기능을 구입 합니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

이 절차의 설명에 따라 업로드 비 Office 365 기능을 사용 하 여가 있어야 합니다.
  
- Office 365 E3 준수 고급 추가 기능 또는 e 5 구독
    
- Office 365가 아닌 콘텐츠가 업로드 될 모든 custodians 고급 준수 추가 기능 또는 e 5 라이선스 E3 있어야
    
- 기존 eDiscovery 사례
    
- 더불어 당 하나의 폴더가 있으면 폴더의 이름은이 형식 *alias@domainname* 폴더에 업로드 하는 것에 대 한 파일을 모두 수집 합니다. 사용자가 Office 365 별칭 및 도메인 *alias@domainname* 이어야 합니다. 루트 폴더에 있는 모든 *alias@domainname* 폴더를 수집할 수 있습니다. 루트 폴더만 *alias@domainname* 폴더를 포함할 수, 루트 폴더에 없는 느슨한 파일 이어야 합니다. 
    
- EDiscovery 관리자 또는 eDiscovery 관리자 계정
    
- [Microsoft Azure 저장소 도구](https://aka.ms/downloadazcopy) 를 Office 365가 아닌 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 설치 합니다. 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>고급 eDiscovery에 Office 365가 아닌 콘텐츠를 업로드 합니다.

1. EDiscovery 관리자 또는 관리자가 eDiscovery, **eDiscovery**열고 Office 365가 아닌 데이터 업로드 하는 대/소문자를 엽니다. 사례를 만들려면 해야하는 경우 참조 [Office 365 보안에서 eDiscovery 사례 관리 &amp; 준수 센터](manage-ediscovery-cases.md)
    
2. **고급 ediscovery 스위치** 를 클릭 합니다.
    
3. **원본 유형에** 서 **비 Office 365 데이터**를 선택 합니다.
    
4. **추가 컨테이너**를 클릭 합니다. 컨테이너 이름을 지정 하 고 설명을 추가 합니다.
    
5. 컨테이너 목록에서 새로 추가 된 컨테이너를 선택 하 고 컨테이너 세부 정보 창에 표시 하 고 닫은 다음 창에서 URL을 복사
    
6. 관리자 권한으로 명령 프롬프트를 열고 설치 AzCopy가 있는 폴더로 디렉터리를 변경.
    
7. 다음과 같은 파일을 업로드 하려면 AzCopy 명령줄 다음과 같이 구성 합니다.
    
    AzCopy 명령을: " *로컬 컴퓨터에 루트 폴더에 대 한 전체 경로* " /Dest: " *까지 컨테이너 URL 하지만 포함 하지 않는?* " /DestSAS: "에서 컨테이너 url로 나눈 나머지가 *는? 끝으로* "/ S. 
    
    예,이 값을 사용 하 여: 
    
  - 루트 폴더-C:\Collected 데이터 
    
  - 컨테이너 url- https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr c =&amp;si NonOfficeData15 = %7 C 0&amp;sig = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA %3 차원
    
    AzCopy 명령줄 구문은 다음과 같습니다.
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    구문을 참조, Azcopy 대 한 자세한 내용은 [Windows에서 AzCopy 사용 하 여 데이터를 전송](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) 합니다. 
    
    > [!IMPORTANT]
    > 사용자 당 하나의 루트 폴더 여야 하 고 폴더 이름을 *alias@domainname* 형식 이어야 합니다. 
  
8. 폴더가 있는 업로드가 완료 되 면 고급 eDiscovery로 다시 전환 합니다. 업로드 한 폴더의 콘텐츠를 고급 ediscovery에서 처리할 준비가 되었습니다. 컨테이너를 선택 하 고 프로세스 단추를 클릭 합니다. 고급 eDiscovery에 대 한 자세한 내용은 대 한 처리를 참조 하십시오 [프로세스 모듈을 실행 하 고 Office 365 고급 eDiscovery의 데이터를 로드](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
    
    > [!IMPORTANT]
    > 컨테이너 고급 eDiscovery에 성공적으로 처리 Azure의 SAS 저장소에 새 콘텐츠를 추가할 수 나타나지 않습니다. 추가 콘텐츠를 수집 하는 경우 고급 eDiscovery 분석을 위해 사례에 추가할 새 **비 Office 365 데이터** 컨테이너를 만들고이 절차를 반복 해야 합니다. 
  
    > [!NOTE]
    > *폴더 이름 지정 문제로 인해 성공적으로 처리 하지 않는* 컨테이너와 사용자 문제를 해결 한 다음, 새 컨테이너를 만들고에 다시 연결 하 고이 문서의 절차를 사용 하 여 다시 업로드 하려면 해야 계속 합니다. 
  

