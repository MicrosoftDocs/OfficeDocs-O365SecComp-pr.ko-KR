---
title: 스팸 메일을 보낸 후 제한된 사용자 포털에서 사용자 제거
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/10/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: 사용자가 스팸으로 분류되는 Office 365에서 계속해서 전자 메일을 보내는 경우 더 이상 메시지를 보낼 수 없게 됩니다.
ms.openlocfilehash: 56f1a34fe4b47a722ff1dace73dd001f0c4812a2
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854722"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a>스팸 메일을 보낸 후 제한된 사용자 포털에서 사용자 제거

사용자가 계속해서 Office 365의 스팸으로 분류되는 전자 메일을 보내면 전자 메일을 보낼 수 없게 되지만 받을 수는 있습니다. 사용자가 서비스에 잘못된 아웃 바운드 보낸 사람으로 나열되고 다음의 경우 배달 못 함 보고서(NDR)를 받습니다.

> "유효한 보낸 사람으로 인식되지 않았기 때문에 메시지를 배달할 수 없습니다. 가장 일반적인 이유는 전자 메일 주소가 스팸 메일을 보내는 것으로 의심어서 더 이상 전자 메일을 보낼 수 없는 경우입니다.  도움이 필요하면 전자 메일 관리자에게 문의하세요. 원격 서버에서 '550 5.1.8 액세스가 거부되었습니다. 잘못된 아웃 바운드 보낸 사람"이 반환되었습니다.

## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 사항은 무엇인가요?
<a name="sectionSection0"> </a>

예상 완료 시간: 5분
  
이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 권한을 확인하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목에서 스팸 방지 항목을 참조하세요.

또한 원격 PowerShell을 통해 다음 절차를 수행할 수 있습니다. BlockedSenderAddress cmdlet을 사용하여 제한된 사용자 목록을 가져오고 Remove-BlockedSenderAddress을 사용하여 제한을 제거합니다. Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>차단된 Office 365 전자 메일 계정에 대한 제한 사항 제거

SCC(보안 및 준수 센터)에서 이 작업을 완료합니다. SCC에 대한 자세한 내용은 [보안 및 준수 센터로 이동하세요.](go-to-the-securitycompliance-center.md) 이러한 기능을 수행하려면 **조직 관리** 또는 **보안 관리자** 역할 그룹에 있어야 합니다. SCC 역학 그룹에 대한 자세한 내용은 [보안 및 준수 센터의 사용 권한으로 이동하세요.](permissions-in-the-security-and-compliance-center.md)

1. Office 365 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용하여 Office 365 보안 및 규정 준수 센터에 로그인하고 왼쪽에 있는 목록에서 **위협 관리**를 확장하고 **검토**를 선택한 다음 **제한된 사용자**를 선택합니다.
    
    > [!TIP]
    > 보안 &amp; 준수 센터에서 **제한된 사용자** 페이지(이전의 관리 센터)로 바로 이동하려면 다음 URL을 사용합니다. > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. 이 페이지에는 전자 메일을 보내지 못하도록 차단된 사용자 목록이 포함됩니다.  제한을 제거할 사용자를 찾은 다음 **차단 해제**를 선택합니다.

3. 플라이아웃하면 전송이 제한된 계정에 대한 세부 정보로 이동합니다. 계정이 실제로 손상될 경우에 적절한 조치를 취하는지 확인하기 위해 권장 사항을 검토해야 합니다. 완료되면 **다음**을 선택합니다.

4. 다음 화면에는 이후 손상을 방지하는 데 도움이 되는 권장 사항이 있습니다. MFA(다단계 인증)를 사용하도록 설정하고 암호를 변경하는 것이 좋습니다. 작업이 완료되면 **사용자 차단 해제**를 클릭합니다.

5. **예**를 클릭하여 변경 내용을 확인합니다.

    > [!NOTE]
    > 제한이 제거되기까지 30분 정도 걸릴 수 있습니다. 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a>이 경우에는 관리자에게 경고를 표시합니다.

"전자 메일 전송 제한 사용자" 경고는 Office 365 보안 및 준수 경고 정책 페이지에서 정책으로 제공됩니다. 이전에는 아웃 바운드 스팸 정책이었지만 이제는 Office 365 경고 플랫폼의 기본 기능입니다. 경고에 대한 자세한 내용은 [보안 및 준수 센터의 경고 정책](alert-policies.md)으로 이동하세요.

> [!IMPORTANT]
> 경고가 작동하려면 감사 로그 검색이 설정되어 있어야 합니다. 자세한 내용은 Office [365 감사 로그 검색을 설정하거나 해제](turn-audit-log-search-on-or-off.md)하는 방법을 참조하세요.

이 경고의 정책은 기본값이며 모든 Office 365 테넌트와 함께 제공되며 설정하지 않아도 됩니다. 심각도가 높은 경고로 간주되며 사용자가 메일을 보낼 수 없는 때마다 경고가 발생하면 구성된 TenantAdmins 그룹에 전자 메일을 보냅니다. 관리자는 SCC 포털 > 경고 > 경고 정책> 전자 메일 전송 제한 사용자 아래의 경고로 이동하여 이 경고가 발생했을 때 경고를 받는 그룹을 업데이트할 수 있습니다.

다음과 같은 경우 경고를 편집할 수 있게 됩니다.
- 전자 메일 알림 켜기/끄기
- 필수 받는 사람에게 전자 메일 보내기
- 하루당 받는 알림 제한

## <a name="checking-for-and-removing-restrictions-using-powershell"></a>PowerShell을 사용하여 제한 확인 및 제거
제한된 사용자에 대한 PowerShell 명령은 다음과 같습니다.
- `Get-BlockedSenderAddress`: 실행하여 전자 메일을 보낼 수 없는 사용자 목록 검색
- `Remove-BlockedSenderAddress`: 실행하여 제한된 사용자를 제거

## <a name="for-more-information"></a>자세한 내용

[손상된 이메일 계정에 응답](responding-to-a-compromised-email-account.md)

[전자 메일 전송 제한 사용자 경고 이해](https://docs.microsoft.com/ko-KR/office365/securitycompliance/alert-policies)

[아웃바운드 메시지용 높은 위험 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)

[보안 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)

[보안 및 준수 센터의 경고 정책](https://docs.microsoft.com/ko-KR/office365/securitycompliance/alert-policies)
