---
title: Office 365 고급 메시지 암호화로 암호화 된 전자 메일에 대 한 만료 날짜 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: office 365 메시지 암호화 (OME)의 맨 위에 office 365 고급 메시지 암호화 기능을 사용 하 여 사용자 지정 브랜드 서식 파일을 통해 전자 메일에 만료 날짜를 설정 하 여 이메일 보안을 확장할 수 있습니다.
ms.openlocfilehash: c1fb876724bed970095e950906500ff551d93cee
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506730"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a>Office 365 고급 메시지 암호화로 암호화 된 전자 메일에 대 한 만료 날짜 설정

office 365에서는 특정 구독의 office 365 메시지 암호화 중 위에서 고급 메시지 암호화를 사용할 수 있습니다. 고급 메시지 암호화는 [Microsoft 365 enterprise e5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise e5 및 Office 365 교육 A5에 포함 되어 있습니다. 조직에 office 365 고급 메시지 암호화를 포함 하지 않는 office 365 구독이 있는 경우 고급 메시지 암호화는 advanced 준수 SKU의 E5 규격을 사용 하 여 추가 기능으로 구입할 수 있습니다.

사용자가 OME 포털을 사용 하 여 암호화 된 전자 메일에 액세스 하는 외부의 받는 사람에 게 보내는 전자 메일에 메시지 만료를 사용할 수 있습니다. Windows Powershell에서 만료 날짜를 지정 하는 사용자 지정 브랜드 서식 파일을 사용 하 여 조직에서 보낸 암호화 된 전자 메일을 보고 회신할 때 받는 사람이 OME 포털을 사용 하도록 강제 합니다.

O365 전역 관리자 인 경우 회사 브랜딩을 적용 하 여 Office 365 조직의 전자 메일 메시지의 모양을 사용자 지정 하는 경우 이러한 전자 메일 메시지에 대 한 만료를 지정할 수도 있습니다. Office 365 고급 메시지 암호화를 사용 하면 조직에서 보내는 암호화 된 전자 메일용으로 여러 템플릿을 만들 수 있습니다. 서식 파일을 사용 하면 받는 사람에 게 사용자가 보낸 메일에 대 한 액세스 권한이 있는 기간을 제어할 수 있습니다.

최종 사용자가 만료 날짜가 설정 된 메일을 받는 경우 사용자는 래퍼 전자 메일에서 만료 날짜를 볼 수 있습니다. 사용자가 만료 된 메일을 열려고 하면 OME 포털에 오류가 표시 됩니다.

외부의 받는 사람에 대 한 전자 메일만 expirable 됩니다.

office 365 고급 메시지 암호화를 사용 하면 사용자 지정 브랜딩을 적용할 때마다 office 365에서 해당 래퍼를 서식 파일을 적용 하는 메일 흐름 규칙에 맞는 전자 메일에 적용 합니다. 또한 사용자 지정 브랜딩을 사용 하는 경우에만 만료를 사용할 수 있습니다.

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a>PowerShell을 사용 하 여 메일 만료를 적용 하는 사용자 지정 브랜딩 서식 파일 만들기

1. Office 365 테 넌 트에서 전역 관리자 권한이 있는 계정을 사용 하 여 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) 합니다.

2. set-omeconfiguration cmdlet을 실행 합니다.

     ```powershell
     New-OMEConfiguration -Identity "Expire in 7 days" ExternalMailExpiryInDays 7
     ```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.

- Identity는 사용자 지정 서식 파일의 이름입니다.

- ExternalMailExpiryInDays는 받는 사람이 만료 되기 전에 메일을 보존할 일 수를 식별 합니다. 1 ~ 730 일 사이의 값을 사용할 수 있습니다.

## <a name="more-information-about-office-365-advanced-message-encryption"></a>Office 365 고급 메시지 암호화에 대 한 추가 정보

- [Office 365 고급 메시지 암호화](ome-advanced-message-encryption.md)

- [Office 365 고급 메시지 암호화로 암호화 된 전자 메일 해지](revoke-ome-encrypted-mail.md)

- [메시지 정책 및 규정 준수 서비스 설명](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)