---
title: Office 365에 대 한 MDM 및 Microsoft Intune 중에서 선택
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/3/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c93d9ab9-efb2-4349-9b93-30c30562ee22
description: Microsoft Intune 및 Office 365에 대 한 기본 제공 모바일 장치 관리는 조직에서 모바일 장치를 관리할 수 있는 기능을 제공 합니다. 하지만이 항목에서 설명 하는 주요 차이점이 있습니다.
ms.openlocfilehash: 339399e2e518c22fa9f0f7482fc527990f1a8541
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532963"
---
# <a name="choose-between-mdm-for-office-365-and-microsoft-intune"></a>Office 365에 대 한 MDM 및 Microsoft Intune 중에서 선택

Microsoft Intune 및 Office 365에 대 한 기본 제공 모바일 장치 관리는 조직에서 모바일 장치를 관리할 수 있는 기능을 제공 합니다. 하지만 다음 표에 설명 하는 주요 차이점이 있습니다.
  
> [!NOTE]
> 사용자와 같은 Office 365 테 넌 트에 Intune와 Office 365를 사용 하 여 모바일 장치를 관리할 수 있습니다. Intune 및 MDM 모두 설정 하 여 특정 사용자와 장치에 가장 적합 한 솔루션을 결정 수 있습니다. 사용할 수 있는 두 옵션을 사용 하는 경우 Office 365 또는 더 풍부한 기능을 갖춘 Intune 솔루션에 대 한 MDM 사용 하 여 사용자의 장치를 관리 하 여부를 선택할 수 있습니다. 
  
||||
|:-----|:-----|:-----|
|**기능 영역** <br/> |**Office 365용 MDM** <br/> |**Microsoft Intune** <br/> |
|Cost  <br/> |많은 Office 365 상업용 구독에 포함 된.  <br/> |Microsoft Intune 유료 구독 해야 하거나 Enterprise 이동성 제품군을 구입할 수 있습니다.  <br/> |
|장치를 관리 하는 방법  <br/> |장치를 사용 하 여 관리는 [Office 365 보안으로 이동 &amp; 준수 센터](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) Office 365 합니다.  <br/> |단독으로 Intune를 사용 하는 경우 Intune 관리 콘솔을 사용 하 여 장치를 관리할 수 있습니다.  <br/> Configuration Manager 콘솔을 사용 하 여 장치 온-프레미스를 관리 하려면 System Center 2012 Configuration Manager와 Intune를 통합 하는 경우와 클라우드 합니다.  <br/> |
|장치를 관리할 수 있습니다  <br/> |IOS, Android, 및 Windows에 대 한 관리 클라우드 기반 장치  <br/> |클라우드 기반 관리 iOS, Mac OS X, Android, Windows 8.1 (전화 및 PC) 하 고 나중에 Windows 10을 포함 합니다. <br/> |
|주요 기능  <br/> |전화 및 태블릿 회사에서 관리 되 고 규격이 IT 정책에 Office 365 회사 전자 메일 및 문서에 액세스할 수 있는지 확인 하는 데 도움이 됩니다.  <br/> 설정 하 고 장치 수준 pin 잠금 및 jailbreak 감지, 권한이 없는 사용자가 분실 또는 도난당 한 경우 회사 전자 메일 및 장치에서 데이터에 액세스 하는 것을 방지 하려면 다음과 같은 보안 정책을 관리 합니다.  <br/> 현재 위치에서 자신의 개인 데이터를 유지 하면서 직원의 장치에서 Office 365 회사 데이터를 제거 합니다.  <br/> 자세한 내용은 [Office 365에 대 한 기본 제공 모바일 장치 관리의 기능](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0)에 포함 됩니다.  <br/> |Office 365 기능에 대 한 MDM plus:  <br/> 안전 하 게 인증서, Wi-fi, VPN 및 전자 메일 프로필을 사용 하 여 회사 리소스에 액세스 하는 사용자는 데 도움이 됩니다.  <br/> 등록 하 고 회사 소유의 장치, 정책 및 응용 프로그램 배포를 단순화 하는 컬렉션을 관리 합니다.  <br/> 사용자에 게 내부 비즈니스 라인 응용 프로그램 및 저장소에서 앱을 배포 합니다.  <br/> 사용 하면 사용자가 모바일 Office를 사용 하 여 회사 정보 및 즉 비즈니스 앱의 줄에 보다 안전 하 게 액세스할 수, 제한 하 여 데이터의 보안을 강화 하는 동안 작업 복사, 잘라내기, 붙여넣기를 선택 하 고 Intune가 관리 하는 앱에 다른 이름으로 저장 합니다.  <br/> 관리 되는 브라우저 Intune app를 사용 하 여 보다 안전한 웹 검색을 사용 하도록 설정 합니다.  <br/> Intune를 사용 하 여 필요 없는 인프라와 클라우드에서 Pc를 관리 하거나 Intune 모든 Pc, Mac, Linux 및 UNIX를 포함 하 여 장치를 관리 하려면 구성 관리자를 연결할 서버 및 단일 관리 콘솔에서 모바일 장치입니다.  <br/> 또한 Intune 구독을 사용 하면 사용자의 장치 Intune에 등록 되지 않은 경우에 Azure 포털을 사용 하 여 MAM (모바일 응용 프로그램 관리) 정책을 설정할 수 있습니다. [MAM 정책을 사용 하 여 응용 프로그램 데이터를 보호를](https://go.microsoft.com/fwlink/?LinkId=825439)참조 하십시오.<br/> |


## <a name="related-topics"></a>관련 항목
   
비디오 교육 코스와 Microsoft Intune 하는 방법에 대 한 자세한 내용은 [Microsoft 클라우드 서비스: Office 365를 관리 하 고 Intune](https://support.office.com/article/c1224e20-3d49-4f40-99ee-fd0991880376.aspx), LinkedIn 학습에 의해 제공자 합니다.
  

