---
title: 스팸 메일을 보낸 후 제한된 사용자 포털에서 사용자 제거
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: 사용자가 스팸으로 분류 된 Office 365에서 전자 메일을 계속 보내면 더 이상 메시지를 보낼 수 없게 됩니다.
ms.openlocfilehash: 3e05b250d5a3cdca79c7cf494b84be02ce3ecdc9
ms.sourcegitcommit: 5a93c2f3df35d06a59a7fbaff5c91f7afde11781
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34857628"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a>스팸 메일을 보낸 후 제한된 사용자 포털에서 사용자 제거

사용자가 계속 해 서 Office 365의 스팸으로 분류 된 전자 메일을 보내는 경우 전자 메일을 보낼 수는 없으며 여전히 해당 메시지를 받을 수도 있습니다. 사용자는 잘못 된 아웃 바운드 보낸 사람으로 서비스에 나열 되며 다음과 같은 경우 배달 못 함 보고서 (NDR)를 받게 됩니다.

> "유효한 보낸 사람으로 인식 하지 못했으므로 메시지를 배달할 수 없습니다. 가장 일반적인 이유는 전자 메일 주소가 스팸을 보낼 때 의심 되며 더 이상 전자 메일을 보낼 수 없게 되기 때문입니다.  도움이 필요 하면 전자 메일 관리자에 게 문의 하세요. 원격 서버에서 ' 550 5.1.8 액세스 거부, 잘못 된 아웃 바운드 보낸 사람 "을 반환 했습니다.

## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

예상 완료 시간: 5분
  
이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인 하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 에서 "스팸 방지 항목" 항목을 참조 하십시오.

또한 원격 PowerShell을 통해 다음 절차를 수행할 수 있습니다. BlockedSenderAddress cmdlet을 사용 하 여 제한 된 사용자 목록을 가져오고, BlockedSenderAddress를 제거 하 여 제한을 제거할 수 있습니다. Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>차단 된 Office 365 전자 메일 계정에 대 한 제한 제거

SCC (보안 & 준수 센터)에서이 작업을 완료 합니다. SCC에 대 한 자세한 내용은 [Security & 준수 센터를](go-to-the-securitycompliance-center.md) 참조 하세요. 이러한 기능을 수행 하려면 **조직 관리** 또는 **보안 관리자** 역할 그룹에 있어야 합니다. SCC 역할 그룹에 대 한 자세한 내용은 [Security & 준수 센터의 사용 권한으로 이동](permissions-in-the-security-and-compliance-center.md) 하십시오.

1. Office 365 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 Office 365 보안 및 준수 센터에 로그인 하 고 왼쪽에 있는 목록에서 **위협 관리**를 확장 한 다음 **검토**를 선택 하 고 제한 됨을 선택 합니다. ** 사용자**입니다.
    
    > [!TIP]
    > 보안 &amp; 및 준수 센터에서 **제한 된 사용자** 페이지 (이전에는 알림 센터로 알려짐)로 바로 이동 하려면 다음 URL을 사용 합니다. >[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. 이 페이지에는 전자 메일을 보낼 수 없도록 차단 된 사용자의 목록이 포함 됩니다.  제한을 제거할 사용자를 찾고 **차단 해제**를 선택 합니다.

3. 플라이 아웃은 송신이 제한 된 계정에 대 한 세부 정보로 이동 합니다. 이 권장 사항을 확인 하 여 계정이 실제로 손상 되는 경우 적절 한 조치를 취해야 합니다. 완료 되 면 **다음** 을 클릭 합니다.

4. 다음 화면에서는 나중에 손상을 방지 하기 위한 권장 사항을 제공 합니다. MFA (multi-factor authentication)를 사용 하도록 설정 하 고 암호를 변경 하는 것이 적절 한 방어 방법입니다. 완료 시 **사용자 차단 해제** 를 클릭 합니다.

5. **예** 를 클릭 하 여 변경 내용을 확인 합니다.

    > [!NOTE]
    > 제한이 제거 되기 전에 30 분 이상 소요 될 수 있습니다. 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a>이 경우 관리자에 게 경고 합니다.

"전자 메일을 보내는 사용자가 제한 되었습니다." 알림을 Office 365 보안 & 준수 경고 정책 페이지의 정책으로 사용할 수 있습니다. 이전에는 아웃 바운드 스팸 정책 였으 며 이제는 Office 365 경고 플랫폼의 기본이 되었습니다. 경고에 대 한 자세한 내용은 [Security & 준수 센터의 경고 정책](alert-policies.md) 으로 이동 하십시오.

> [!IMPORTANT]
> 알림이 작동 하려면 감사 로그 검색을 설정 해야 합니다. 자세한 내용은 [Office 365 감사 로그 검색을 설정 또는 해제](turn-audit-log-search-on-or-off.md) 하는 방법을 참조 하세요.

이 경고에 대 한 정책은 기본값 이며 모든 Office 365 테 넌 트와 함께 제공 되며 설정할 필요가 없습니다. 심각도가 높은 경고로 간주 되며, 사용자가 메일을 보낼 수 없을 때마다 경고가 발생 하는 경우 구성 된 TenantAdmins 그룹을 전자 메일로 보냅니다. 관리자는 SCC 포털 > 경고로 이동 하 여 전자 메일을 보낼 수 없도록 하 > 사용자에 게 알림 > 경고를 표시 하 여이 경고가 발생할 경우 알림을 받게 됩니다.

알림을 편집 하 여 다음을 수행할 수 있습니다.
- 전자 메일 알림 설정/해제
- 필요한 받는 사람에 게 전자 메일 보내기
- 하루에 받는 알림 제한

## <a name="for-more-information"></a>자세한 내용

[손상 된 전자 메일 계정에 응답](responding-to-a-compromised-email-account.md)

[전자 메일 알림을 보내는 것이 제한 된 사용자 이해](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)

[보안 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)

[보안 & 준수 센터의 경고 정책](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)
