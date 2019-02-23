---
title: Office 365 서비스 암호화
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: Microsoft Office 365의 데이터 복구 기능을 이해 합니다.'
ms.openlocfilehash: 4e9dd52adbeada92d14db369b386ff1ca7e42fc5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220348"
---
# <a name="office-365-service-encryption"></a>Office 365 서비스 암호화

볼륨 수준 암호화, Exchange online, 비즈니스용 Skype, SharePoint Online 및 비즈니스용 OneDrive를 사용 하는 것 외에도 서비스 암호화를 사용 하 여 고객 데이터를 암호화 합니다. 서비스 암호화를 사용 하면 다음과 같은 두 가지 주요 관리 옵션을 사용할 수 있습니다.
- Microsoft는 모든 암호화 키를 관리 합니다. (이 옵션은 현재 SharePoint Online, 비즈니스용 OneDrive 및 비즈니스용 Skype에서 사용할 수 있습니다. 현재는 Exchange Online에 대 한 로드맵을 사용할 수 있습니다.
- 고객은 서비스 암호화에 사용 되는 루트 키를 제공 하며, 고객은 Azure Key Vault를 사용 하 여 이러한 키를 관리 합니다. Microsoft는 다른 모든 키를 관리 합니다. 이 옵션은 고객 키 라고 하며, 현재 Exchange online, SharePoint Online 및 비즈니스용 OneDrive에 사용할 수 있습니다. 이전에는 고급 암호화 라고 합니다. 원래 공지 사항을 보려면 [Office 365 고객을 위해 투명도 및 컨트롤 향상](http://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) 을 참조 하세요.

서비스 암호화는 여러 가지 이점을 제공 합니다. 예를 들어 다음과 같은 경우를 예로 들 수 있습니다.
- 강력한 암호화 보호에 대 한 권한 보호 및 관리 기능을 제공 합니다.
- 다중 테 넌 트 서비스가 테 넌 트 기준 키 관리를 제공할 수 있도록 하는 고객 키 옵션이 포함 됩니다.
- Windows 운영 체제 관리자가 운영 체제에 의해 저장 되거나 처리 되는 고객 데이터에 대 한 액세스와의 분리를 제공 합니다.
- 암호화에 대 한 준수 요구 사항이 있는 고객의 요구 사항을 충족 하기 위해 Office 365의 기능을 향상 시킵니다.

## <a name="customer-key"></a>고객 키
고객 키를 사용 하 여 온-프레미스 HSM 또는 Azure 키 자격 증명 모음을 사용 하 여 자체 암호화 키를 생성할 수 있습니다. 키를 생성 하는 방법에 관계 없이 고객은 Azure 키 자격 증명 모음을 사용 하 여 Office 365에서 사용 되는 암호화 키를 제어 하 고 관리 합니다. 키가 Azure Key Vault에 저장 되 면 Exchange online 및 SharePoint online과 같은 작업에 할당 될 수 있으며 사서함 데이터 및 파일을 암호화 하는 데 사용 되는 자격 증명 집합의 루트로 사용 됩니다. 고객 키를 사용 하는 경우의 또 다른 장점 중 하나는 Microsoft에서 고객 데이터를 처리 하는 기능을 제어 하는 것입니다. 이 기능은 고객이 Microsoft에 서비스를 종료 하거나 클라우드에 저장 된 데이터 중 일부를 제거 하는 경우와 같이 Office 365에서 데이터를 제거 하려는 고객이이를 수행할 수 있도록 하 고, 고객 키를 기술 컨트롤로 사용 하 여 아무도 없는지 확인 합니다. Microsoft를 포함 하 여 데이터에 액세스 하거나 처리할 수 있습니다. Microsoft 담당자가 고객 데이터에 대 한 액세스를 제어 하는 데 사용할 수 있는 추가 (및 보완) 기능을 고객 Lockbox 기능과 함께 사용 합니다.

Exchange Online, 비즈니스용 Skype, SharePoint Online 및 비즈니스용 OneDrive에 대해 office 365에 대 한 고객 키를 설정 하는 방법에 대 한 자세한 내용은 [고객 키를 사용 하 여 office 365에서 데이터 제어](https://support.office.com/article/Controlling-your-data-in-Office-365-using-Customer-Key-f2cd475a-e592-46cf-80a3-1bfb0fa17697)를 참조 하세요. 자세한 내용은 [Office 용 고객 키 365 FAQ](https://support.office.com/article/Customer-Key-for-Office-365-FAQ-41ae293a-bd5c-4083-acd8-e1a2b4329da6)를 참조 하 고, [고객 키에 규정 준수 요구 사항을 충족 하는 데 도움이 되는 데이터를 관리 및 제어](https://techcommunity.microsoft.com/t5/Microsoft-Ignite-Content-2017/Manage-and-control-your-data-to-help-meet-compliance-needs-with/td-p/117580)합니다.
