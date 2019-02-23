---
title: 아웃 바운드 스팸 정책 구성
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/10/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: 아웃바운드 전자 메일 보내기 서비스를 사용하는 경우 아웃바운드 스팸 필터링이 항상 사용하도록 설정되므로 서비스와 받는 사람을 사용하여 조직을 보호할 수 있습니다.
ms.openlocfilehash: 095098c058a5ca5165e0ad24ef48296c980eadcf
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214528"
---
# <a name="configure-the-outbound-spam-policy"></a>아웃 바운드 스팸 정책 구성

아웃바운드 전자 메일 보내기 서비스를 사용하는 경우 아웃바운드 스팸 필터링이 항상 사용하도록 설정되므로 서비스와 받는 사람을 사용하여 조직을 보호할 수 있습니다. 인바운드 필터링과 마찬가지로 아웃바운드 스팸 필터링도 연결 필터링과 콘텐츠 필터링으로 구성되지만, 아웃바운드 필터 설정은 구성할 수 없습니다. 스팸으로 확인된 아웃바운드 메시지는 위험성이 높은 배달 풀을 통해 라우팅되므로 일반 아웃바운드 IP 풀이 차단 목록에 추가될 가능성이 줄어듭니다. 서비스를 통해 아웃바운드 스팸을 계속 보내는 고객에 대해서는 메시지 보내기가 차단됩니다. 아웃바운드 스팸 필터링을 사용하지 않도록 설정하거나 변경할 수는 없지만 기본 아웃바운드 스팸 정책을 통해 다양한 회사 전체 아웃바운드 스팸 설정을 구성할 수 있습니다. 
  
다음 비디오에서는 아웃바운드 스팸 정책을 구성하는 방법을 보여줍니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

예상 완료 시간: 5분
  
이 절차를 수행 하려면 먼저 사용 권한을 할당 받아야 합니다. 필요한 사용 권한을 확인 하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 에서 "스팸 방지 항목" 항목을 참조 하십시오. 
  
이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.
  
또한 원격 PowerShell을 통해 다음 절차를 수행할 수 있습니다. [get-hostedoutboundspamfilterpolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) cmdlet을 사용 하 여 설정을 검토 하 고 [get-hostedoutboundspamfilterpolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) 에서 아웃 바운드 스팸 정책 설정을 편집할 수 있습니다. Windows PowerShell을 사용 하 여 exchange online protection에 연결 하는 방법에 대 한 자세한 내용은 [connect to exchange online protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290)을 참조 하십시오. Windows PowerShell을 사용 하 여 exchange online에 연결 하는 방법에 대 한 자세한 내용은 [connect to exchange online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하십시오.
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a>EAC를 사용하여 기본 아웃바운드 스팸 정책 편집
<a name="sectionSection1"> </a>

다음 절차에 따라 기본 아웃바운드 스팸 정책을 편집합니다.
  
### <a name="to-configure-the-default-outbound-spam-policy"></a>기본 아웃바운드 스팸 정책을 구성하려면 다음을 수행합니다.

1. EAC(Exchange 관리 센터)에서 **보호** \> **아웃바운드 스팸**으로 이동한 다음 기본 정책을 두 번 클릭합니다.
    
2. **아웃바운드 스팸 기본 설정** 메뉴 옵션을 선택합니다. 
    
3. 아웃바운드 메시지와 관련된 다음 확인란을 선택하고 함께 제공되는 입력란에 연관된 전자 메일 주소를 하나 이상 지정합니다. 전자 메일 주소가 유효한 SMTP 대상으로 확인되는 경우에는 메일 그룹을 입력할 수 있습니다.
    
1. **의심스러운 모든 아웃바운드 전자 메일 메시지의 복사본을 다음 전자 메일 주소로 보내기**. 이러한 메시지는 SCL 등급에 관계없이 필터에 의해 스팸으로 표시되며, 필터에서 거부되지는 않지만 위험성이 높은 배달 풀을 통해 라우팅됩니다. 주소가 여러 개인 경우 세미콜론으로 구분합니다. 지정된 받는 사람은 보낸 사람 및 받는 사람 필드에 원래 보낸 사람 및 받는 사람이 표시되는 Bcc(숨은 참조) 주소로 메시지를 받습니다.
    
2. **보낸 사람이 아웃바운드 스팸을 보낼 수 없도록 차단된 경우 다음 전자 메일 주소로 알림 보내기**. 주소가 여러 개인 경우 세미콜론으로 구분합니다.
    
    특정 사용자가 상당한 양의 스팸을 발생 하는 경우 사용자가 전자 메일 메시지를 보낼 수 없습니다. 이 설정을 사용 하 여 지정 된 도메인의 관리자에 게는이 사용자에 대해 아웃 바운드 메시지가 차단 됨을 알리는 메시지가 표시 됩니다. 이 알림의 모양을 보려면 [보낸 사람이 보내는 아웃 바운드 스팸 차단 되 면 샘플 알림을](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)참조 하세요. 다시 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 [스팸 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소 제거](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx)를 참조 하세요.
    
4. **저장**을 클릭합니다. 기본 정책 설정에 대한 요약이 오른쪽 창에 표시됩니다.
    
## <a name="for-more-information"></a>자세한 내용
<a name="sectionSection2"> </a>

[아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)
  
[스팸 방지 보호 기능 FAQ](anti-spam-protection-faq.md)
  

