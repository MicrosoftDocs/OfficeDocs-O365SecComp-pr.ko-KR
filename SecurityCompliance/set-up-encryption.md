---
title: Office 365 Enterprise의 암호화 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/2/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e86fc991-0161-4f01-9c1c-d25e87733d06
description: Office 365와 일부 암호화 기능은 기본적으로 설정 합니다. 특정 준수 또는 법적 요구 사항을 충족 하기 위해 다른 기능을 구성할 수 있습니다.
ms.openlocfilehash: 80deced80283ac36d82ac15cee9af6d390c4749a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533247"
---
# <a name="set-up-encryption-in-office-365-enterprise"></a>Office 365 Enterprise의 암호화 설정

암호화는 권한이 없는 사용자가 읽고에서 콘텐츠를 보호할 수 있습니다. [Office 365에서 암호화](encryption.md) 를 수행할 수 있으므로 단일 위치를 설정 하거나 암호화를 설정 없는 다양 한 기술 및 메서드를 사용 합니다. 이 문서를 설정 하거나 정보 보호 전략의 일부분으로 암호화를 구성할 수 있는 다양 한 방법에 대 한 정보를 제공 합니다. 
  
> [!TIP]
> 암호화에 대 한 자세한 기술 정보를 찾고 하는 경우 [Office 365의 암호화에 대 한 자세한 내용은 기술 참조 (영문)를](technical-reference-details-about-encryption.md)참조 하십시오. 
  
Office 365 여러 암호화 기능을 기본적으로 사용할 수 있습니다. 특정 준수 또는 법적 요구 사항을 충족 하기 위해 추가 암호화 기능을 구성할 수 있습니다. 다음 표에서 다양 한 시나리오에 대 한 여러 암호화 방법을 설명합니다.
  
|**시나리오**|**암호화 방법**|
|:-----|:-----|
|Windows 컴퓨터에 저장 된 파일  <br/> |컴퓨터 수준에서 암호화를 수행할 수 있습니다 BitLocker를 사용 하 여 Windows 장치입니다. 엔터프라이즈 관리자 또는 IT 전문가, Microsoft Deployment Toolkit (MDT)를 사용 하 여이 설정할 수 있습니다. [MDT BitLocker에 대 한 설정](https://go.microsoft.com/fwlink/?linkid=849282)을 참조 하십시오.<br/> |
|모바일 장치에 저장 된 파일  <br/> |일부 종류의 모바일 장치는 기본적으로 해당 장치에 저장 된 파일을 암호화 합니다. [Office 365에 대 한 기본 제공 모바일 장치 관리의 기능](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0)을 모바일 장치에서 Office 365의 데이터에 액세스를 허용할지 여부를 결정 하는 정책을 설정할 수 있습니다. 예, Office 365 데이터에 액세스 하는 콘텐츠를 암호화 하는 장치에만 허용 하는 정책을 설정할 수 있습니다. 참조 [만들기 및 장치 보안 정책 배포](https://support.office.com/article/d310f556-8bfb-497b-9bd7-fe3c36ea2fd6)합니다.<br/> Office 365와의 상호작용 방식 모바일 장치에 대 한 추가 제어에 대 한, [Microsoft Intune](https://aka.ms/qzln04)추가 (영문)를 고려할 수 있습니다. [Office 365에 대 한 MDM 및 Microsoft Intune 중에서 선택](https://support.office.com/article/c93d9ab9-efb2-4349-9b93-30c30562ee22)을 참조 하십시오.<br/> |
|Microsoft의 데이터 센터에서 데이터를 암호화 하는데 사용 되는 암호화 키에 대 한 제어를 필요  <br/> | Office 365 관리자로 조직의 암호화 키를 제어할 수 있으며 다음 Microsoft의 데이터 센터의 나머지 부분에서 데이터를 암호화 하 고 사용 하 여 Office 365를 구성할 수 있습니다.  <br/> [고객 키를 사용하여 Office 365에서 데이터 제어](controlling-your-data-using-customer-key.md) <br/> [Office 365 FAQ에 대 한 고객 키](service-encryption-with-customer-key-faq.md) <br/> |
|전자 메일 (Exchange Online)를 통해 통신 하 고 사용자  <br/> | Exchange Online 관리자 권한으로 전자 메일 암호화를 구성 하기 위한 여러 옵션 해야 합니다. 다음과 같습니다.<br/>  Azure 권한 관리 (Azure RMS)와 [Office 365 메시지 암호화 (OME)를](set-up-new-message-encryption-capabilities.md) 사용 하 여 내부 또는 외부 조직에는 암호화 된 메시지를 보낼 수 있는 사용자를 사용 하도록 설정 하려면  <br/>  [S/MIME 메시지 서명 및 암호화를](https://aka.ms/c6dozg) 사용 하 여를 암호화 하 여 전자 메일 메시지에 디지털 서명  <br/>  TLS를 사용 하 여 [다른 조직과 보안 메일 흐름에 대 한 커넥터를 설정](https://aka.ms/hs809p) 하려면 <br/>  [Office 365에서 전자 메일 암호화](https://aka.ms/hic3f7)를 참조 하십시오.  <br/> |
|팀 사이트 또는 문서 라이브러리 (비즈니스 또는 SharePoint Online에 대 한 OneDrive)에서 파일은 액세스  <br/> |사용자는 비즈니스 또는 SharePoint Online에 대 한 OneDrive에 저장 된 파일을 사용 하는 경우에 TLS 연결 사용 됩니다. 이것은 Office 365에 자동 구성 합니다. [SharePoint Online 비즈니스용 OneDrive에 대 한 데이터 암호화](https://go.microsoft.com/fwlink/?linkid=526379)를 참조 하십시오.<br/> |
|온라인 모임 및 IM 대화 (비즈니스 Online 용 Skype)에서 공유 하는 파일  <br/> |사람들이 Skype를 사용 하 여 온라인 비즈니스에 대 한 파일을 사용 하 여 작업할 TLS 연결에 사용 됩니다. 이것은 Office 365에 자동 구성 합니다. [보안 및 보관 (온라인 비즈니스에 대 한 Skype)를](https://aka.ms/nuq4ws)참조 하십시오.<br/> |
   
## <a name="additional-information"></a>추가 정보

암호화 옵션을 포함 하는 파일 보호 솔루션에 대 한 자세한 내용은 [Office 365에서 파일 보호 솔루션](https://www.microsoft.com/en-us/download/details.aspx?id=55523)을 참조 합니다.
  

