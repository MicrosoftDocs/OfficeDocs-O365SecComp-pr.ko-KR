---
title: 스팸 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소 제거
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/01/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: 사용자가 스팸으로 분류 된 Office 365에서 전자 메일 메시지를 계속 보내는 경우 더 이상 메시지를 보낼 수 없게 됩니다.
ms.openlocfilehash: 870e5eabca9e799dfca1e99846a5bfe845f65df4
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275938"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>스팸 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소 제거

사용자가 스팸으로 분류 된 Office 365에서 전자 메일 메시지를 계속 보내는 경우 더 이상 메시지를 보낼 수 없게 됩니다. 사용자는 잘못 된 아웃 바운드 보낸 사람으로 서비스에 나열 되며 다음과 같은 경우 배달 못 함 보고서 (NDR)를 받게 됩니다.

- 유효한 보낸 사람으로 인식 되지 않아 메시지를 배달할 수 없습니다. 가장 일반적인 이유는 전자 메일 주소가 스팸을 보낼 때 의심 되며, 더 이상 조직 외부에서 메시지를 보낼 수 없게 되기 때문입니다. 도움이 필요 하면 전자 메일 관리자에 게 문의 하세요.  원격 서버에서 ' 550 5.1.8 액세스 거부, 잘못 된 아웃 바운드 보낸 사람 '을 반환 했습니다.

또한 테 넌 트 관리자는 사용자가 더 이상 아웃 바운드 메시지를 보내지 못하도록 제한 되었다는 경고도 수신 됩니다.

## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

예상 완료 시간: 5분
  
이 절차를 수행 하려면 먼저 사용 권한을 할당 받아야 합니다. 필요한 사용 권한을 확인 하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 에서 "스팸 방지 항목" 항목을 참조 하십시오.

또한 원격 PowerShell을 통해 다음 절차를 수행할 수 있습니다. BlockedSenderAddress cmdlet을 사용 하 여 제한 된 사용자 목록을 가져오고, BlockedSenderAddress를 제거 하 여 제한을 제거할 수 있습니다. Windows PowerShell을 사용 하 여 exchange online에 연결 하는 방법에 대 한 자세한 내용은 [connect to exchange online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하십시오.

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a>차단 된 Office 365 전자 메일 계정에 대 한 제한 제거

이 작업은 Office 365 보안 & 준수 센터 (SCC)에서 완료 해야 합니다. SCC에 대 한 자세한 내용은 [Office 365 Security & 준수 센터로 이동 하세요](go-to-the-securitycompliance-center.md) . 이러한 기능을 수행 하려면 **조직 관리** 또는 **보안 관리자** 역할 그룹에 있어야 합니다. SCC 역할 그룹에 대 한 자세한 내용은 [Office 365 Security & 준수 센터의 사용 권한으로 이동](permissions-in-the-security-and-compliance-center.md) 하십시오.

1. office 365 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 office 365 보안 및 준수 센터에 로그인 하 고 왼쪽에 있는 목록에서 **위협 관리**를 확장 한 다음 **검토**를 선택 하 고 제한 됨을 선택 합니다. ** 사용자**입니다.
    
    > [!TIP]
    > 보안 &amp; 및 준수 센터에서 **제한 된 사용자** 페이지 (이전에는 알림 센터로 알려짐)로 바로 이동 하려면 다음 URL을 사용 합니다. >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)

2. 이 페이지에는 조직 외부로 메일을 보낼 수 없도록 차단 된 사용자 목록이 포함 됩니다.  제한을 제거할 사용자를 찾은 다음 **차단을 해제**를 클릭 합니다.

3. **예** 를 클릭 하 여 변경 내용을 확인 합니다. 
    
> [!NOTE]
> 테 넌 트 관리자가 계정을 차단 해제할 수 있는 횟수에는 제한이 있습니다. 사용자 제한을 초과 하면 오류 메시지가 나타납니다. 사용자의 차단을 해제 하려면 지원에 문의 해야 합니다.<br/><br/> 사용자가 차단 해제 되려면 최대 1 시간이 걸릴 수 있습니다.
  
## <a name="third-party-block-lists"></a>타사 차단 목록

Exchange Online Protection은 또한 타사 차단 목록을 사용 하 여 스팸 필터링에서 의사 결정을 내리는 데 도움을 줍니다. 사용자, 웹 사이트, 도메인 및 IP 주소는 스팸 메시지에 나타나는 것 처럼 차단 목록에 추가할 수 있습니다. Office 365 관리자는 타사 목록 공급자가 속해 있는 경우 이러한 개체를 제거 해야 합니다.

> [!NOTE]
> office 365 외부의 사용자가 office 365 계정으로 메시지를 보낼 수 없는 경우 해당 계정이 외부의 수신 거부 목록에 있을 수 있습니다. Office 365 외부의 사용자는 [셀프 서비스 목록 \ 포털](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)을 사용 하 여 자신을 제거할 수 있습니다. 

## <a name="for-more-information"></a>자세한 내용

[손상 된 전자 메일 계정에 응답](responding-to-a-compromised-email-account.md)

[아웃바운드 스팸 정책 구성](configure-the-outbound-spam-policy.md)
  
[아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)

[Office 365 Security & 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)

  

