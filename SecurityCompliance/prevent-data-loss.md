---
title: Office 365의 데이터 손실을 방지합니다
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 6a888faa-c114-4395-b20d-a5b8ebd1ac0c
description: 데이터 손실 방지 (DLP) 정책을 사용 하 여 식별, 모니터링 및 자동으로 Office 365에서 중요 한 정보를 보호할 수 있습니다. 예, 방지할 수 있습니다 신용 카드 번호, 주민등록 번호, 또는 상태 레코드와 같은 중요 한 정보 유출 조직 외부에서 합니다.
ms.openlocfilehash: 617120fbf521a12291414ffc2054d559fd7323a4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533195"
---
# <a name="prevent-data-loss-in-office-365"></a>Office 365의 데이터 손실을 방지합니다

데이터 손실 방지 (DLP) 정책을 사용 하 여 식별, 모니터링 및 자동으로 Office 365에서 중요 한 정보를 보호할 수 있습니다. 예, 방지할 수 있습니다 신용 카드 번호, 주민등록 번호, 또는 상태 레코드와 같은 중요 한 정보 유출 조직 외부에서 합니다.
  
## <a name="learn-about-dlp"></a>DLP에 대 한 설명

해당 기능, 작동 방식 및 사용 하 여 중요 한 정보를 보호 하는 방법을 포함 하 여 DLP의 개요를 확인 합니다. 
  
- [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)
    
- [DLP 확장된 개요 보기](https://go.microsoft.com/fwlink/?linkid=852300)
    
## <a name="set-up-dlp"></a>DLP 설정

Office 365 보안에서 DLP 정책을 만듭니다 &amp; 준수 센터입니다.
  
- [DLP 정책 권장 시작](get-started-with-dlp-policy-recommendations.md)
    
- [템플릿에서 DLP 정책 만들기](create-a-dlp-policy-from-a-template.md)
    
- [전자 메일 알림을 보내고 DLP 정책에 대 한 정책 팁을 표시 합니다.](use-notifications-and-policy-tips.md)
    
- [DLP 정책 템플릿에 포함되는 내용](what-the-dlp-policy-templates-include.md)
    
- [FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기](protect-documents-that-have-fci-or-other-properties.md)
    
- [데이터 손실 방지에 대한 보고서 보기](view-the-dlp-reports.md)
    
## <a name="understand-the-sensitive-information-types"></a>중요 한 정보 유형 이해

이 항목에서는 사용 하 여 정확 하 게 DLP 모양은 대 한 중요 한 정보를 식별 하는 경우를 이해 합니다. 또한 기존 중요 한 정보 형식을 사용자 지정 하거나 페이지를 만들 새 사용자 지정 하기 위해이 정보를 사용할 수 있습니다.
  
- [중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)
    
- [DLP 기능이 찾는 항목](what-the-dlp-functions-look-for.md)
    
## <a name="customize-the-sensitive-information-types"></a>중요 한 정보 유형 사용자 지정

DLP 신용 카드 번호 또는 은행 계좌 번호와 같은 사용 하 여 사용할 수 있는 여러 기본 제공 중요 한 정보 유형을 포함 합니다. 복사 하 고 XML 파일을 수정 하 여 이러한 기본 제공 형식을 사용자 지정할 수 있습니다. 있으며 식별 하 고 다양 한 유형의-중요 한 정보를 보호 해야 하는 경우 예-조직에 특정 한 형식을 사용 하는 직원 ID 만들 수 있습니다 사용자 지정 중요 한 정보 유형입니다.
  
- [사용자 지정 DLP 확장된 개요 보기](https://go.microsoft.com/fwlink/?linkid=852306)
    
- [기본 제공 중요한 정보 유형 사용자 지정](customize-a-built-in-sensitive-information-type.md)
    
- [사용자 지정 중요한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)
    
- [키워드 사전 만들기](create-a-keyword-dictionary.md)
    
## <a name="extend-dlp"></a>DLP를 확장 합니다.

DLP 이벤트에 대 한 데이터는 Office 365 관리 활동 API에서 제공 됩니다. 이 감사 데이터 등의 어떤 규칙 및 정책 일치, 어떤 유형의 중요 한 정보를 찾을 수 및 취한 조치를 포함 합니다. 권한을 부여 하면 한 후이 데이터는 타사 응용 프로그램에서 사용할 수 있습니다.
  
- [Office 365 관리 활동 API 참조 (영문)](https://go.microsoft.com/fwlink/?linkid=852309)
    
- [Office 365 관리 활동 API 스키마](https://go.microsoft.com/fwlink/?linkid=852308)
    
## <a name="more-information"></a>추가 정보

- [DLP 보안 간에 작동 하는 방법 &amp; 준수 센터 및 Exchange 관리 센터](how-dlp-works-between-admin-centers.md)
    
- [DLP Exchange Online에 대 한](https://go.microsoft.com/fwlink/?linkid=852311)
    
- [데이터 손실 방지 (DLP) cmdlet](https://go.microsoft.com/fwlink/?linkid=852310)
    

