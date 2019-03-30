---
title: 고급 eDiscovery 분석을 위해 비 Office 365 콘텐츠 가져오기
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: aed로 분석할 수 있도록 O365에 저장 되지 않은 콘텐츠를 Azure blob로 가져오는 방법에 대해 설명 하는 방법
ms.openlocfilehash: 7b7694754b26951aa02930fd101631ba9060bc17
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001171"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a>고급 eDiscovery 분석을 위해 비 Office 365 콘텐츠 가져오기

office 365 Advanced eDiscovery를 사용 하 여 분석 해야 하는 모든 문서는 office 365에 살고 있습니다. 고급 ediscovery의 office가 아닌 365 콘텐츠 가져오기 기능을 사용 하는 경우 PST 파일을 제외한 office 365에 없는 문서를 연결 된 Azure storage blob에 업로드 하 고 고급 ediscovery로 분석할 수 있습니다. 이 절차에서는 분석을 위해 비 Office 365 문서를 고급 eDiscovery로 가져오는 방법을 보여 줍니다.
  
> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
> [!NOTE]
> office가 아닌 365 콘텐츠에 대 한 office 365 Advanced eDiscovery 데이터 저장소 추가 기능 구독을 구매할 수 있습니다. 이 기능은 고급 eDiscovery를 사용 하 여 분석 되는 콘텐츠에 대해서만 사용할 수 있습니다. [비즈니스용 office 365에 대 한 구매 또는 편집 및 추가 기능](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) 의 단계를 따르고 office 365 Advanced eDiscovery 저장소 추가 기능을 구입 합니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

이 절차에 설명 된 대로 Office 이외에 업로드 365 기능을 사용 하려면 다음이 필요 합니다.
  
- 고급 규정 준수 추가 기능 또는 E5 구독이 포함 된 Office 365 E3
    
- 비 Office 365 콘텐츠가 업로드 되는 모든 custodians에는 고급 준수 추가 기능 또는 E5 라이선스가 포함 된 E3이 있어야 합니다.
    
- 기존 eDiscovery 사례
    
- 업로드 하기 위한 모든 파일은 custodian 마다 폴더가 하나이 고 폴더 이름이이 형식 *별칭 @ domainname* 에 있는 폴더로 수집 됩니다. *alias @ domainname* 은 사용자의 Office 365 별칭 및 도메인 이어야 합니다. 모든 *alias @ domainname* 폴더를 루트 폴더로 수집할 수 있습니다. 루트 폴더에는 *별칭 @ domainname* 폴더만 포함할 수 있으며 루트 폴더에는 느슨한 파일이 없어야 합니다. 
    
- ediscovery 관리자 또는 ediscovery 관리자 인 계정
    
- Office가 아닌 365 콘텐츠 폴더 구조에 대 한 액세스 권한이 있는 컴퓨터에 설치 된 [Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) 입니다. 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Office 이외의 365 콘텐츠를 고급 eDiscovery에 업로드

1. ediscovery 관리자 또는 ediscovery 관리자로 서 **ediscovery**를 열고 비 Office 365 데이터가 업로드 될 사례를 엽니다. 사례를 만들어야 하는 경우 [에는 Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례 관리](manage-ediscovery-cases.md) 를 참조 하세요.
    
2. **고급 eDiscovery로 전환을 클릭 합니다** .
    
3. **원본 형식** 아래에서 **비 Office 365 데이터**를 선택 합니다.
    
4. **컨테이너 추가**를 클릭 합니다. 컨테이너의 이름을 입력 하 고 설명을 추가 합니다.
    
5. 컨테이너 목록에서 새로 추가 된 컨테이너를 선택 하 고 컨테이너 세부 정보 창에 표시 되는 URL을 복사한 다음 창을 닫습니다.
    
6. 관리자 권한으로 명령 프롬프트를 열고 AzCopy이 설치 된 폴더로 디렉터리를 변경 합니다.
    
7. AzCopy 명령줄을 구성 하 여 다음과 같은 파일을 업로드 합니다.
    
    AzCopy/Source: " *로컬 컴퓨터의 루트 폴더* 에 대 한 전체 경로"/dest: " *컨테이너 URL까지* (으)로 이동 하 고?  "/DestSAS:"의 *컨테이너 url의 나머지 부분은? 끝* "/S. 
    
    예를 들어 다음 값을 사용 합니다. 
    
  - 루트 폴더-c:\collected 데이터 
    
  - 컨테이너 url- https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;si = NonOfficeData15% 7c0&amp;sig = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA% 3d
    
    AzCopy 명령줄 구문은 다음과 같습니다.
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    Azcopy 구문에 대 한 자세한 내용은 [Windows의 Azcopy을 사용 하 여 데이터 전송](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) 를 참조 하세요. 
    
    > [!IMPORTANT]
    > 사용자 마다 루트 폴더가 1 개 있어야 하며 폴더 이름은 *alias @ domainname* 형식 이어야 합니다. 
  
8. 폴더 업로드가 완료 되 면 고급 eDiscovery로 다시 전환 합니다. 업로드 한 폴더의 콘텐츠를 이제 고급 eDiscovery에서 처리할 준비가 되었습니다. 컨테이너를 선택 하 고 처리 단추를 클릭 합니다. 고급 ediscovery 처리에 대 한 자세한 내용은 [Office 365 Advanced ediscovery에서 프로세스 모듈 실행 및 데이터 로드](run-the-process-module-and-load-data-in-advanced-ediscovery.md) 를 참조 하세요.
    
    > [!IMPORTANT]
    > 고급 eDiscovery에서 컨테이너를 성공적으로 처리 하면 더 이상 Azure의 SAS 저장소에 새 콘텐츠를 추가할 수 없게 됩니다. 추가 콘텐츠를 수집 하 고 고급 eDiscovery 분석을 위해 사례에 추가 하려는 경우에는 **Office가 아닌 새 데이터** 컨테이너를 만들고이 절차를 반복 해야 합니다. 
  
    > [!NOTE]
    > *폴더 명명 문제로 인해 컨테이너가 제대로 처리 되지* 않는 경우 문제를 해결 하는 경우에도이 문서의 절차에 따라 새 컨테이너를 만들고 다시 연결 하 고 업로드 해야 합니다. 
  

