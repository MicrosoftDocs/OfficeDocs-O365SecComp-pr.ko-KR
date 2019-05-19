---
title: Office 365 Enterprise의 암호화 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/2/2018
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e86fc991-0161-4f01-9c1c-d25e87733d06
description: Office 365에서는 일부 암호화 기능이 기본적으로 설정 됩니다. 특정 규정 준수 또는 법적 요구 사항을 충족 하도록 다른 기능을 구성할 수 있습니다.
ms.openlocfilehash: 3bb76d70bd364bd461721d6277516801b3675031
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158460"
---
# <a name="set-up-encryption-in-office-365-enterprise"></a>Office 365 Enterprise의 암호화 설정

암호화를 통해 권한이 없는 사용자가 콘텐츠를 읽지 못하도록 할 수 있습니다. [Office 365에서는](encryption.md) 다양 한 기술과 방법을 사용 하 여 암호화를 수행할 수 있기 때문에 암호화를 설정 하거나 설정 하는 한 가지 위치는 없습니다. 이 문서에서는 정보 보호 전략의 일환으로 암호화를 설정 하거나 구성할 수 있는 다양 한 방법에 대 한 정보를 제공 합니다.
  
> [!TIP]
> 암호화에 대 한 자세한 기술 정보를 보려면 [기술 참조에서 Office 365의 암호화에 대 한 세부 정보](technical-reference-details-about-encryption.md)를 참조 하세요.
  
Office 365에서는 기본적으로 몇 가지 암호화 기능을 사용할 수 있습니다. 특정 규정 준수 또는 법적 요구 사항을 충족 하도록 추가 암호화 기능을 구성할 수 있습니다. 다음 표에서는 여러 시나리오에 대 한 여러 암호화 방법에 대해 설명 합니다.
  
|**시나리오**|**암호화 방법**|
|:-----|:-----|
|Windows 컴퓨터에 저장 된 파일  <br/> |Windows 장치에서 BitLocker를 사용 하 여 컴퓨터 수준의 암호화를 수행할 수 있습니다. 엔터프라이즈 관리자 또는 IT 전문가는 MDT (Microsoft Deployment Toolkit)를 사용 하 여이를 설정할 수 있습니다. [BitLocker에 대 한 MDT 설정을](https://go.microsoft.com/fwlink/?linkid=849282)참조 하세요.  <br/> |
|파일이 모바일 장치에 저장 됩니다.  <br/> |일부 유형의 모바일 장치는 기본적으로 이러한 장치에 저장 되는 파일을 암호화 합니다. [Office 365에 대 한 기본 제공 모바일 장치 관리 기능](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0)을 사용 하 여 모바일 장치에서 office 365의 데이터에 액세스할 수 있도록 허용할지 여부를 결정 하는 정책을 설정할 수 있습니다. 예를 들어 콘텐츠를 암호화 하는 장치만 Office 365 데이터 액세스를 허용 하는 정책을 설정할 수 있습니다. [장치 보안 정책 만들기 및 배포를](https://support.office.com/article/d310f556-8bfb-497b-9bd7-fe3c36ea2fd6)참조 하세요.  <br/> 모바일 장치가 Office 365과 상호 작용 하는 방법에 대 한 추가 제어를 위해 [Microsoft Intune](https://aka.ms/qzln04)을 추가 하는 것을 고려할 수 있습니다. [Office 365 및 Microsoft Intune에 대해 MDM 간 선택을](https://support.office.com/article/c93d9ab9-efb2-4349-9b93-30c30562ee22)참조 하세요.  <br/> |
|Microsoft 데이터 센터에서 데이터를 암호화 하는 데 사용 되는 암호화 키를 제어 해야 합니다.  <br/> | Office 365 관리자는 조직의 암호화 키를 제어 하 고 Office 365를 구성 하 여 Microsoft의 데이터 센터에서 휴지 상태인 데이터를 암호화할 수 있습니다.  <br/> [고객 키를 사용하여 Office 365에서 데이터 제어](controlling-your-data-using-customer-key.md) <br/> [Office 365에 대 한 고객 키 FAQ](service-encryption-with-customer-key-faq.md) <br/> |
|사용자가 전자 메일을 통해 통신 하는 경우 (Exchange Online)  <br/> | Exchange Online 관리자는 전자 메일 암호화를 구성 하기 위한 몇 가지 옵션을 사용할 수 있습니다. 다음과 같은 다양한 알고리즘과 방법이 있습니다.  <br/>  Azure RMS (Azure 권한 관리)와 함께 [OME (Office 365 메시지 암호화)](set-up-new-message-encryption-capabilities.md) 를 사용 하 여 사용자가 조직 내부 또는 외부에서 암호화 된 메시지를 보낼 수 있도록 설정  <br/>  [메시지 서명 및 암호화에 S/MIME](https://aka.ms/c6dozg) 을 사용 하 여 전자 메일 메시지 암호화 및 디지털 서명  <br/>  TLS를 사용 하 여 [다른 조직과의 보안 메일 흐름에 대 한 커넥터 설정](https://aka.ms/hs809p) <br/>  [Office 365의 전자 메일 암호화를](https://aka.ms/hic3f7)참조 하세요.  <br/> |
|파일은 팀 사이트 또는 문서 라이브러리 (비즈니스용 OneDrive 또는 SharePoint Online)에서 액세스 합니다.  <br/> |사용자가 비즈니스용 OneDrive 또는 SharePoint Online에 저장 된 파일로 작업 하는 경우 TLS 연결이 사용 됩니다. 이 기능은 Office 365에서 자동으로 기본적으로 제공 됩니다. [비즈니스용 OneDrive 및 SharePoint Online의 데이터 암호화를](https://go.microsoft.com/fwlink/?linkid=526379)참조 하세요.  <br/> |
|온라인 모임 및 IM 대화에서 파일 공유 (비즈니스용 Skype Online)  <br/> |사용자가 비즈니스용 Skype 온라인을 사용 하 여 파일을 사용 하는 경우에는 TLS가 연결에 사용 됩니다. 이 기능은 Office 365에서 자동으로 기본적으로 제공 됩니다. [Security And 아카이빙 (비즈니스용 Skype Online)](https://aka.ms/nuq4ws)을 참조 하세요.  <br/> |

## <a name="additional-information"></a>추가 정보

암호화 옵션을 포함 하는 파일 보호 솔루션에 대 한 자세한 내용은 [Office 365의 파일 보호 솔루션](https://www.microsoft.com/en-us/download/details.aspx?id=55523)을 참조 하세요.