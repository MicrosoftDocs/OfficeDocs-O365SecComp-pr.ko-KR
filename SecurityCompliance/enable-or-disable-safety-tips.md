---
title: Office 365에서 보안 팁 사용 여부 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
ms.collection:
- M365-security-compliance
description: 전자 메일 메시지에서 보안 팁을 사용 하거나 사용 하지 않도록 설정 하는 방법을 Office 365 및 EOP 관리자에 게 알립니다.
ms.openlocfilehash: a782c9a1eca874c2aa2128b6129257067c63219a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154760"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a>Office 365에서 보안 팁 사용 여부 설정

EOP (Exchange Online Protection)는 배달 되는 전자 메일 메시지에 보안 팁을 추가 하거나 스탬프 처리 합니다. 이러한 보안 팁을 통해 받는 사람에 게는 메시지가 안전한 지 확인 하 고, 메시지가 Office 365에서 스팸으로 표시 되는 경우, 메시지에 피싱 사기와 같은 의심 스러운 항목이 포함 되어 있거나 외부 이미지에 있는 경우 메시지를 빠르게 확인할 수 있습니다. 차단 되었습니다. Office 365 및 EOP 독립 실행형 관리자는 스팸 정책 설정을 편집 하 여 Outlook 및 기타 데스크톱 전자 메일 클라이언트에서 보안 팁이 전자 메일에 표시 되지 않도록 설정할 수 있습니다. 
  
Office 365에서는 조직에 기본적으로 보안 팁을 사용할 수 있으며, 스팸 및 피싱 공격을 방지 하는 데 도움이 되도록 사용 하도록 설정 하는 것이 좋습니다. 웹용 Outlook에 대 한 보안 팁은 사용 하지 않도록 설정할 수 없습니다.
  
예제를 확인 하 고 보안 팁에 표시 되는 정보에 대 한 자세한 내용은 [Office 365의 전자 메일 메시지에 있는 보안 팁](safety-tips-in-office-365.md) 을 참조 하십시오.
  
이 항목의 내용:
  
- [Office 365 보안 &amp; 및 준수 센터를 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 하려면](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [PowerShell을 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 하려면](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a>Office 365 보안 &amp; 및 준수 센터를 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 하려면
<a name="SandCCsafetytip"> </a>

1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정으로 Office 365에 로그인합니다.
    
3. **위협 관리** \> **정책을**선택 합니다. 
    
4. **정책** 페이지에서 **스팸 방지**를 선택 합니다.
    
    ![이 스크린샷에서는 보안 &amp; 및 준수 센터의 스팸 방지 설정 페이지로 이동 하는 방법을 보여 줍니다.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. **스팸 방지 설정** 페이지에서 **사용자 지정** 탭을 선택 합니다. 
    
    ![이 스크린샷에서는 보안 &amp; 및 준수 센터의 스팸 방지 설정 페이지에 있는 사용자 지정 탭의 위치를 보여 줍니다.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. 필요한 경우 사용자 지정 **설정** 스위치를 선택 하 여 사용자 지정 설정을 켭니다. 사용자 지정 설정 스위치를 **Off**로 설정 하면 스팸 필터 정책을 수정할 수 없습니다.
    
    ![이 스크린샷에는 해제 된 사용자 지정 스팸 방지 필터 정책 설정이 표시 됩니다.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. 수정 하려는 스팸 정책을 확장 한 다음 **정책 편집**을 선택 합니다. 예를 들어 **기본 스팸 필터 정책**옆에 있는 아래쪽 화살표를 선택 합니다. 또는 원하는 경우 **정책 추가**를 선택 하 여 새 정책을 만들 수 있습니다.
    
8. **스팸 및 대량 작업을** 확장 합니다. 
    
9. 보안 팁을 사용 하도록 설정 하려면 **안전 팁**에서 설정 **** 확인란을 선택 합니다. 보안 팁을 사용 하지 않으려면 설정 **** 확인란의 선택을 취소 합니다. 
    
10. **저장**을 선택합니다.
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a>PowerShell을 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 하려면
<a name="pshellsafetytip"> </a>

관리자는 Exchange Online PowerShell을 사용 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정할 수 있습니다. Get-hostedcontentfilterpolicy cmdlet을 사용 하면 스팸 필터 정책에서 보안 팁을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.
  
1. Exchange Online PowerShell에 연결합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](http://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하세요.
    
2. Get-hostedcontentfilterpolicy cmdlet을 실행 하 여 보안 팁을 사용 하거나 사용 하지 않도록 설정 합니다.
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
    
  -  *정책 이름은* 수정할 정책의 이름입니다 (예: **기본값**).
    
  -  `$true`스팸 필터 정책에 대 한 보안 팁을 사용 하도록 설정 합니다. 
    
  -  `$false`스팸 필터 정책에 대 한 보안 팁을 사용 하지 않도록 설정 합니다. 
    
    예를 들어 기본 스팸 필터 정책에 대 한 보안 팁을 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다.
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

이 cmdlet에 대 한 자세한 내용은 [get-hostedcontentfilterpolicy](https://technet.microsoft.com/library/jj200781.aspx)를 참조 하십시오.
    
## <a name="still-need-help"></a>여전히 도움이 필요하세요?
<a name="pshellsafetytip"> </a>

보안 팁을 사용 하지 않도록 설정 했지만 여전히 전자 메일 메시지에 표시 하려면 다음 항목을 확인 하세요.
  
- 웹용 Outlook에 대 한 보안 팁은 사용 하지 않도록 설정할 수 없습니다. Outlook과 같은 다른 클라이언트에서 같은 전자 메일을 확인 하세요.
    
- 보안 팁은 EOP를 사용 하는 모든 사용자에 대해 기본적으로 설정 되며, 여기에는 Office 365이 있는 모든 사람이 포함 됩니다. 전자 메일에 보안 팁이 표시 되지 않도록 하려면이 항목에서 설명 하는 대로 스팸 필터 정책을 사용 하 여 사용 하지 않도록 설정 해야 합니다. 정책을 설정한 후에는 사용 하도록 설정 되어 있는지 확인 합니다. 스팸 필터 정책을 사용 하는 방법에 대 한 자세한 내용은 [스팸 필터 정책 구성을](https://technet.microsoft.com/library/jj200684.aspx)참조 하세요.
    
스팸 및 피싱 사기를 방지 하는 자세한 방법은 [Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md)를 참조 하세요.
  

