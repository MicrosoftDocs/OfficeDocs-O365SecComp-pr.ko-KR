---
title: 스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소를 제거
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 사용자는 계속 해 서 스팸으로 분류 하는 Office 365에서 전자 메일 메시지를 보내는, 모든 자세한 메시지를 보내지 못하도록 차단 됩니다.
ms.openlocfilehash: ce52ddfd96b582911bb519c15bbfe90351946db8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026335"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a>스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소를 제거

사용자는 계속 해 서 스팸으로 분류 하는 Office 365에서 전자 메일 메시지를 보내는, 모든 자세한 메시지를 보내지 못하도록 차단 됩니다. 
  
받은 배달 못함 보고서 (NDR 또는 전자 메일 메시지를 보내려면 실패) 보낸 전자 메일 메시지를 보내지 못하도록 차단 되 면 자신이 직접 차단을 해제 하기 위해 수행 해야하는 단계에 대 한 구체적인 정보를 제공 하는 합니다.
  
뿐 아니라 개별 사용자가 차단 될 수 있습니다,이 서비스는 하지만 특정 웹사이트, 도메인 및 IP 주소 차단 될 수 있습니다. 경우에 따라 도메인 이나 웹사이트 추가할 수 차단 목록에 스팸 메시지에 나타나는 해 서 합니다. Office 365 관리자, 사용자, 웹사이트, 도메인 및 타사 차단 목록에서 제거 하는 IP 주소를 가져올 시도할 수 있습니다. 이 항목의 맨 아래에 표에 링크를 사용 하 여 각 제 3 자에 게 문의 하 고 지침을 따릅니다. Office 365 계정에 메시지를 보낼 수 없는 Office 365 외부 사용자, 하는 경우 자신의 계정 외부 수신된 거부 목록에 결국 있을 수 있습니다. Office 365 외부 사용자가 자신 수신된 거부 목록에서 [목록 삭제 포털 자가 서비스](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)를 사용 하 여 제거 시도할 수 있습니다.
  
Office 365 사용자 스팸으로 분류 되는 전자 메일을 보내지 못하도록 차단 되 면 anotification를 받을 수 있도록 아웃 바운드 스팸 설정을 구성할 수 있습니다. 사용자의 사서함에 문제가 해결 되 면 해당 보낸사람에 블록을 제거할 수 있습니다.
  
## <a name="unblock-a-blocked-office-365-email-account"></a>차단 된 Office 365 전자 메일 계정 차단 해제

Exchange 관리 센터 (EAC)에서이 작업을 완료 합니다. EAC에 대 한 자세한 내용은 [Exchange 관리 센터의 Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) 아웃 확인 합니다. 
  
> [!NOTE]
> Exchange Online에 대 한 EAC 하 고 있는 경우가 아니면 관리 센터를 볼 수 없습니다. 
  
1. EAC에서 **보호** 이동 \> **관리 센터**입니다.
    
    ![Exchange 관리 센터의 관리 센터로 이동](media/9bbf0844-7b34-4a86-a2b7-8c7e9c8519a3.png)
  
2. **검색** 아이콘을 선택 하 고 차단 된 사용자의 SMTP 주소를 입력 합니다. 
    
    ![관리 센터에서 차단된 사용자 검색](media/f931b5a0-7115-4d95-9f6f-b403436031ba.png)
  
3. 설명 창에서 **계정을 차단 해제** 를 클릭 합니다. 
    
    ![관리 센터에서 사용자 차단 해제](media/c5d5b1b9-8416-45aa-9631-881e94d1d056.png)
  
4. **예** 하 여 변경 내용을 확인을 클릭 합니다. 
    
> [!NOTE]
> 테 넌 트 관리자 계정을 차단을 해제 수 있는 횟수에 제한이 사용자에 대 한 제한을 초과 되 면 오류 메시지가 나타납니다. 사용자의 차단을 해제 하는 지원 서비스에 문의 합니다. 
  
## <a name="third-party-block-lists"></a>타사 차단 목록

|**목록 이름**|**목록 삭제 포털**|**자세한 내용**|
|:-----|:-----|:-----|
|URIBL  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[URIBL 웹사이트](https://uribl.com/) <br/> |
|SURBL  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[SURBL URI 신뢰도 데이터 소개 (영문)](http://www.surbl.org/) <br/> |
|Spamhaus  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[이해 필터링 이해](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|invaluement  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[invaluement 스팸 방지 목록](http://dnsbl.invaluement.com/) <br/> |
|Phishtank  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[PhishTank FAQ](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> Exchange Online Protection 제 3 자 차단 목록을 사용 하 여 스팸 필터링에 대 한 합니다. 
   
## <a name="for-more-information"></a>자세한 내용

[아웃 바운드 스팸 정책 구성](configure-the-outbound-spam-policy.md)
  
[아웃 바운드 메시지 용 위험성이 높은 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)

[목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인 제거](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

