---
title: Office 365에서 보안 팁 사용 여부 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
description: Office 365와 EOP 관리자를 사용 하도록 설정 하 고 전자 메일 메시지에 안전 팁을 사용 하지 않도록 설정 하는 방법에 지시 합니다.
ms.openlocfilehash: 8e5d8bf1d2f831b5d74ca3accd8b434519bfeaab
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180858"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a>Office 365에서 보안 팁 사용 여부 설정

추가 하는 Exchange Online Protection (EOP) 또는 스탬프는 안전 팁을 제공 하는 전자 메일 메시지를 합니다. 메시지에 표시 된 스팸으로 Office 365에서 다음과 같은 피싱 사기 의심 스러운 메시지에 포함 하는 경우 또는 외부 이미지를 포함 하는 경우 보낸 사람이 확인 이러한 안전 팁 받는 사람에 게 메시지를 안전 하 고에서 인지 확인 하는 빠른, 시각적 방법을 제공합니다 차단 되었습니다. Office 365와 EOP 독립 실행형 관리자를 사용 하도록 설정 하거나 다른 데스크톱 전자 메일 클라이언트 및 Outlook의 전자 메일에 표시 되지 않도록 안전 팁을 사용 하지 않도록 설정 하려면 스팸 정책 설정을 편집할 수 있습니다. 
  
Office 365 안전 팁을 사용 하면 조직에 대 한 기본으로 설정 하 고 그대로 사용 하는 스팸 및 피싱 공격을 위해 사용 하는 것이 좋습니다. 웹에서 Outlook에 대 한 안전 팁을 사용 하지 않도록 설정할 수는 없습니다.
  
예를 보려면 하 고 안전 팁에 표시 되는 정보에 대해 자세히 알아보려면 참조 [안전 팁 (영문) Office 365에서 전자 메일 메시지에.](safety-tips-in-office-365.md)
  
이 항목의 내용:
  
- [Office 365 보안을 사용 하 여 안전 팁을 사용 하지 않도록 설정 하거나 사용 &amp; 준수 센터](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [PowerShell을 사용 하 여 안전 팁을 사용 하지 않도록 설정 하거나 사용](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a>Office 365 보안을 사용 하 여 안전 팁을 사용 하지 않도록 설정 하거나 사용 &amp; 준수 센터
<a name="SandCCsafetytip"> </a>

1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정으로 Office 365에 로그인합니다.
    
3. **위협 관리** 를 선택 \> **정책**입니다. 
    
4. **정책** 페이지에서 **스팸 방지**를 선택 합니다.
    
    ![이 스크린샷은 보안에서 스팸 방지 설정 페이지로 이동 하는 방법을 보여주는 &amp; 준수 센터입니다.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. **스팸 방지 설정** 페이지에서 **사용자 지정** 탭을 선택 합니다. 
    
    ![스팸 방지 설정 페이지의 보안에서 사용자 지정 탭의 위치를 표시 하는이 스크린샷은 &amp; 준수 센터입니다.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. 필요한 경우 사용자 지정 설정 사용을 **사용자 지정 설정** 스위치를 선택 합니다. 사용자 지정 설정을 스위치는 **Off**로 설정 되어, 스팸 필터 정책을 수정할 수 없습니다.
    
    ![이 스크린샷은 해제 하는 정책 설정을 사용자 지정 스팸 방지 필터를 보여줍니다.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. 수정 하 고 다음 **정책 편집**을 선택 하려면 스팸 정책을 확장 합니다. 예, **정책 필터링 하는 기본 스팸**옆에 있는 아래쪽 화살표를 선택 합니다. 또는 원하는 하는 경우 **추가 정책을**선택 하 여 새 정책을 만들 수 있습니다.
    
8. **스팸 및 대량** 작업을 확장 합니다. 
    
9. **안전 팁**을 아래에서 안전 팁을 사용 하도록 설정 하려면 확인란을 선택 **에서** 합니다. 안전 팁을 사용 하지 않으려면 **에서** 확인란의 선택을 취소 합니다. 
    
10. **Save(저장)** 를 선택합니다.
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a>PowerShell을 사용 하 여 안전 팁을 사용 하지 않도록 설정 하거나 사용
<a name="pshellsafetytip"> </a>

관리자는 Exchange Online PowerShell을 사용 하 여 안전 팁을 사용할지 여부를 수 있습니다. Set-hostedcontentfilterpolicy cmdlet을 사용 하 여 스팸 필터 정책에 안전 팁을 사용 하지 않도록 설정 하거나 사용 합니다.
  
1. Exchange Online PowerShell에 연결 합니다. 내용은 [Connect to Exchange Online PowerShell를](http://go.microsoft.com/fwlink/p/?LinkId=396554)참조 하십시오.
    
2. 안전 팁을 사용할지 여부를 Set-hostedcontentfilterpolicy cmdlet을 실행 합니다.
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
    
  -  *정책* 이름은 **기본**예 수정할 정책의 이름입니다.
    
  -  `$true`스팸 필터 정책에 대 한 안전 팁을 사용 하도록 설정 합니다. 
    
  -  `$false`스팸 필터 정책에 대 한 안전 팁을 사용 하지 않도록 설정 합니다. 
    
    예, 기본 스팸 필터 정책에 대 한 안전 팁을 사용 하지 않으려면 다음 명령을 실행 합니다.
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

이 cmdlet에 대 한 자세한 내용은 [Set-hostedcontentfilterpolicy](https://technet.microsoft.com/library/jj200781.aspx)을 참조 하십시오.
    
## <a name="still-need-help"></a>여전히 도움이 필요하세요?
<a name="pshellsafetytip"> </a>

안전 팁을 사용 하지 않도록 설정 하 고 여전히 전자 메일 메시지에 표시 하는이 기능을 확인 합니다.
  
- 웹에서 Outlook에 대 한 안전 팁을 사용 하지 않도록 설정할 수는 없습니다. Outlook 등의 다른 클라이언트에서 동일한 전자 메일을 확인 하십시오.
    
- 안전 팁은 모든 하나 EOP를 사용 하 여 사용자에 대해 기본적으로 Office 365를 가진 모든 사람을 포함 하 여 합니다. 전자 메일에 표시에서 안전 팁을 해제 하려면이 항목의 설명에 따라 스팸 필터 정책을 사용 하 여 비활성화 해야 있습니다. 정책 설정 했을 때 사용할 수 있는지 확인 합니다. 스팸 필터 정책을 사용 하도록 설정에 대 한 정보를 [스팸 필터 정책 구성](https://technet.microsoft.com/library/jj200684.aspx)을 참조 하십시오.
    
다양 한 방법으로 스팸 및 피싱 방지 하기 위해, [Office 365 전자 메일 스팸 방지 보호 기능](anti-spam-protection.md)을 참조 하십시오.
  

