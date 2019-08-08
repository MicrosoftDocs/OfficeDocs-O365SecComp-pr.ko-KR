---
title: Office 365의 무제한 보관 개요
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Exchange Online 사서함에 대 한 무제한 보관 저장소를 제공 하는 Office 365의 자동 확장 보관에 대해 알아봅니다.
ms.openlocfilehash: 21489683bbb9f3e2addb5e95a38d8f8a418639de
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36231082"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a>Office 365의 무제한 보관 개요

Office 365에서 보관 사서함은 사용자에 게 사서함 저장소 공간을 추가로 제공 합니다. 사용자의 보관 사서함을 사용 하도록 설정한 후에는 최대 100의 추가 저장소를 사용할 수 있습니다. 이전에는 100 GB 저장소 할당량에 도달 했을 때 조직에서 Microsoft에 연락 하 여 보관 사서함에 대 한 추가 저장소 공간을 요청 해야 했습니다. 더 이상 이러한 경우는 아닙니다.

Office 365의 무제한 보관 기능(*자동 확장 보관 기능*이라고도 함)은 보관 사서함의 무제한 저장소 용량을 제공합니다. 이제 보관 사서함의 저장소 할당량에 도달 하면 Office 365에서 자동으로 보관 함의 크기를 증가 시키며, 따라서 사용자에 게 사서함 저장소 공간이 부족 하지 않고 관리자가 보관 사서함에 대해 추가 저장소를 요청할 필요가 없습니다. .
  
자동 확장 보관을 설정 하는 단계별 지침은 [Office 365에서 무제한 보관을 사용 하도록 설정을](enable-unlimited-archiving.md)참조 하십시오.
  
> [!NOTE]
> 자동 확장 보관 기능은 공유 사서함도 지원합니다. 공유 사서함에 대 한 보관 함을 사용 하도록 설정 하려면 exchange online 계획 2 라이선스 또는 교환 라이선스가 있는 exchange online 계획 1 라이선스가 필요 합니다. 
  
## <a name="how-auto-expanding-archiving-works"></a>자동 확장 보관의 작동 방식

앞에서 설명한 것 처럼 사용자의 보관 사서함을 사용 하도록 설정 하면 추가 사서함 저장소 공간이 만들어집니다. 자동 확장 보관을 사용 하도록 설정 하면 Office 365에서 보관 사서함의 크기를 주기적으로 확인 합니다. 보관 사서함이 저장 용량 제한에 근접 하면 Office 365에서 자동으로 보관에 대 한 추가 저장소 공간을 만듭니다. 사용자가이 추가 저장 공간을 모두 실행 하는 경우 Office 365에서는 사용자의 보관 사서함에 저장 공간을 더 추가 합니다. 이 프로세스가 자동으로 수행 되므로 관리자가 추가 보관 저장소를 요청 하거나 자동 확장 보관을 관리할 필요가 없습니다. 
  
프로세스에 대 한 간략 한 개요는 다음과 같습니다.
  
![자동 확장 보관 프로세스 개요](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. 사용자 사서함 또는 공유 사서함에 대해 보관을 사용 하도록 설정 합니다. 100 GB의 저장소 공간이 있는 보관 사서함이 만들어지고 보관 사서함에 대 한 경고 할당량이 90 g b로 설정 됩니다.
    
2. 관리자가 사서함에 대해 자동 확장 보관을 사용 하도록 설정 합니다. 그런 다음 보관 사서함 (복구 가능한 항목 폴더 포함)이 90에 도달 하면 자동 확장 보관 함으로 변환 되 고 Office 365에서 보관 함에 저장 공간을 추가 합니다. 추가 저장 공간을 프로 비전 하는 데 최대 30 일이 걸릴 수 있습니다.
    
3. Office 365에서는 필요한 경우 보관 사서함에 저장 공간을 자동으로 추가 합니다.
  
> [!IMPORTANT]
> 사서함이 보류 되거나 Office 365 보존 정책에 할당 된 경우에는 자동 확장 보관을 사용 하는 경우 보관 maibox의 저장소 할당량이 110 GB로 증가 합니다. 마찬가지로 보관 경고 할당량이 100 GB로 증가 합니다.

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a>추가 보관 저장소 공간으로 이동 하는 것은 무엇 인가요?

자동 확장 보관 저장소를 효율적으로 사용 하기 위해 폴더가 이동 될 수 있습니다. Office 365에서는 추가 저장소가 보관 사서함에 추가 될 때 이동할 폴더를 결정 합니다. 폴더를 이동 하면 Outlook 폴더 목록의 보관 부분에 있는 원래 폴더 아래에 하위 폴더가 자동으로 만들어집니다. 이 새 하위 폴더는 이동 된 항목을 가리킵니다. 이 폴더의 이름을 지정 하는 데 Office 365에서 사용 하는 명명 규칙은 ** \<\>_cm(mmm dd, yyyy h_mm에서 만들어짐)** 이며, 여기에서 다음을 수행 합니다. 
  
- **yyyy** 는 폴더에서 메시지가 수신 된 연도입니다. 
    
- **mmm dd, yyyy h_m** 는 사용자의 표준 시간대 및 Outlook의 국가별 설정에 따라 하위 폴더가 Office 365에서 만들어진 날짜 및 시간입니다. 
    
다음 스크린샷은 자동 확장 보관 사서함에서 메시지가 이동 되기 전과 후의 폴더 목록을 보여 줍니다.
  
 **추가 저장소가 추가 되기 전에**
  
![자동 확장 보관이 프로 비전 되기 전 보관 사서함의 폴더 목록](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 **추가 저장소가 추가 된 후**
  
![자동 확장 보관이 프로 비전 된 후 보관 사서함의 폴더 목록](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a>자동 확장 보관 함의 항목에 액세스 하기 위한 Outlook 요구 사항

자동 확장 보관 사서함에 저장 된 메시지에 액세스 하려면 사용자는 다음 Outlook 클라이언트 중 하나를 사용 해야 합니다.
  
- Windows 용 outlook 2016 또는 Outlook 2019
    
- 웹용 Outlook 
    
- Mac 용 outlook 2016 또는 Outlook 2019 
    
> [!NOTE]
> Outlook 2013 사용자는 원래 보관 사서함에 저장 된 항목에만 액세스할 수 있습니다. 추가 보관 저장소로 이동 되는 항목에는 액세스할 수 없습니다. 
  
다음은 Outlook 또는 웹용 Outlook을 사용 하 여 자동 확장 보관 함에 저장 된 메시지에 액세스 하는 경우 고려해 야 할 몇 가지 사항입니다.
  
- 자동 확장 된 저장 영역으로 이동 된 폴더를 포함 하 여 보관 사서함의 모든 편지함에 액세스할 수 있습니다.
    
- 폴더 자체를 검색 해야만 추가 저장소 영역으로 이동한 항목을 검색할 수 있습니다. 즉, 검색 범위로 **현재 폴더** 옵션을 선택 하려면 폴더 목록에서 보관 폴더를 선택 해야 합니다. 마찬가지로 자동 확장 된 저장소 영역의 폴더에 하위 폴더가 있는 경우 각 하위 폴더를 개별적으로 검색 해야 합니다. 
    
- 자동 확장 보관 함에서 Outlook 및 웹용 Outlook의 항목 수가 정확 하지 않을 수 있습니다.
    
- 자동 확장 된 저장 영역을 가리키는 하위 폴더의 항목을 삭제할 수는 있지만 해당 폴더 자체를 삭제할 수는 없습니다.
    
- 지운 편지함 복구 기능을 사용 하 여 자동 확장 된 저장소 영역에서 삭제 된 항목을 복구할 수는 없습니다.
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a>보관 및 기타 Office 365 준수 기능 자동 확장

이 섹션에서는 자동 확장 보관과 기타 Office 365 준수 및 데이터 거 버 넌 스 기능 간의 기능에 대해 설명 합니다.
  
- **eDiscovery** -콘텐츠 검색 또는 원본 위치 eDiscovery와 같은 Office 365 eDiscovery 도구를 사용 하면 자동 확장 보관 함의 추가 저장소 영역도 검색 됩니다.
    
- **보존** -Exchange Online의 소송 보존, 보안 및 준수 센터의 보존 정책 등의 도구를 사용 하 여 사서함을 보류할 때 자동 확장 된 보관 함에 있는 콘텐츠도 보존 됩니다.
    
- **Mrm (메시징 레코드 관리)** -Exchange Online에서 mrm 삭제 정책을 사용 하 여 만료 된 사서함 항목을 영구적으로 삭제 하는 경우에는 자동 확장 보관 함에 있는 만료 됨 항목도 삭제 됩니다.
    
- **서비스 가져오기** -Office 365 가져오기 서비스를 사용 하 여 PST 파일을 사용자의 자동 확장 보관으로 가져올 수 있습니다. PST 파일에서 사용자의 보관 사서함으로의 데이터를 최대 100 GB까지 가져올 수 있습니다. 

## <a name="more-information"></a>추가 정보

자동 확장 보관에 대 한 자세한 기술 정보는 [Office 365: 자동 확장 보관 함 FAQ](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/)를 참조 하십시오.