---
title: Office 365 사서함 마이그레이션
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Office 365 사서함 마이그레이션에 사용 되는 cmdlet에 대 한 간략 한 요약입니다.
ms.openlocfilehash: 8e0f23a3efbbcf6f84364c09e667678972120e18
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219148"
---
# <a name="office-365-mailbox-migrations"></a>Office 365 사서함 마이그레이션
exchange 기반 하이브리드 배포를 사용 하는 경우 고객은 온-프레미스 exchange 사서함을 [exchange online](https://docs.microsoft.com/Exchange/exchange-online) 조직으로 이동 하거나 exchange online 사서함을 [exchange 온-프레미스](https://docs.microsoft.com/Exchange/exchange-server) 조직으로 이동할 수 있습니다. 마이그레이션 일괄 처리는 온-프레미스 조직과 Exchange Online 조직 간에 사서함을 이동할 때 사용 됩니다. 고객은 다음 cmdlet을 사용 하 여 사서함 마이그레이션에 대 한 통계 및 기타 정보를 검토할 수 있습니다.

- [get-moverequeststatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) -상태, 사서함 크기, 보관 사서함 크기 및 완료율이 포함 된 사용자 사서함에 대 한 기본 통계를 제공 합니다.
- [Get-mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) -조직의 사서함 개체 및 특성에 대 한 요약 목록을 제공 합니다.
- [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) -사서함, 메일 사용자, 연락처, 메일 그룹 등의 기존 메일 사용 가능 개체 목록을 제공 합니다.
- [new-moverequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) -진행 중인 사서함 마이그레이션의 자세한 상태를 제공 합니다.
- [get-migrationuser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) -사서함 이동 및 마이그레이션 사용자에 대 한 정보를 제공 합니다.
- [new-migrationbatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) -현재 마이그레이션 일괄 처리의 상태에 대 한 정보를 제공 합니다.
- [get-migrationuserstatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) -특정 사용자의 마이그레이션 상태에 대 한 자세한 정보를 제공 합니다.
- [get-mailboxstatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) -사서함에 대 한 정보 (예: 크기, 메시지 수, 마지막으로 액세스 한 시간)를 제공 합니다.

추가 cmdlet에 대 한 자세한 내용은 [Exchange Online의 이동 및 마이그레이션 cmdlet](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)을 참조 하세요.
