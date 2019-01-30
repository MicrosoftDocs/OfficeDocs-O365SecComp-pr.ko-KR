---
title: Office 365 메시지 암호화로 암호화된 전자 메일 취소
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/29/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Office 365 관리자 권한으로 Office 365 메시지 암호화를 사용 하 여 암호화 된 특정 전자 메일을 취소할 수 있습니다.
ms.openlocfilehash: a3f5c08d2c8660e56c378fc5fa7a850ff2c12eb5
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614392"
---
# <a name="office-365-message-encryption-email-revocation"></a>Office 365 메시지 암호화 전자 메일 해지

이 문서는 [Office 365 메시지 암호화](ome.md)에 대 한 문서를 더 큰 시리즈의 일부입니다. 이제 오른쪽, 암호화 된 전자 메일 해지 미리 보기입니다. 예상 되는 업데이트 및 변경 된 기능 및 콘텐츠를 사용해 제공을 개선 하기 위해 계속 되는 대로 합니다.

이미 보낸 전자 메일을 해지 하려면 하는 것이 더 필요할 수 있습니다. 전자 메일 Office 365 메시지 암호화를 사용 하 여 암호화 된 경우 Office 365 관리자는 특정 조건에서 전자 메일에 대 한이 수행할 수 있습니다. 이 문서에서 어떤 경우에이 작업이 가능 하 고 작업을 수행 하는 방법에 설명 합니다.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>해지할 수 있는 암호화 된 전자 메일

받는 사람이 받은 프로그램 링크 기반 암호화 된 전자 메일을 브랜드 하는 경우에 암호화 된 전자 메일을 해지할 수 있습니다. 받는 사람이 네이티브 인라인 환경이 지원 되는 Outlook 클라이언트에서을 받은 경우 해당 전자 메일이 해지 수는 없습니다.

있는지 여부를 받는 수신 링크 기반 환경 또는 인라인 경험 받는 사람 id 형식에 따라 달라 집니다: Office 365와 Microsoft 계정 받는 사람 (예: outlook.com 사용자) 지원 되는 Outlook 클라이언트를 인라인 환경에서 확인할 수 있습니다. 모든 받는 사람 같은 다른 유형을 Gmail 받는 사람에 게 링크 기반 경험을 가져옵니다.

출시 예정 조직이 id가 받는 사람에 관계 없이 링크 기반 환경을 강제 실행 하는 기능입니다. 이와 같은 방식이으로 모든 받는 사람에 게 자신이 됩니다 수 있는 읽기 및 암호화 된 전자 메일에 회신 하는 Office 365 메시지 암호화 포털에 대 한 링크와 브랜드 전자 메일을 받습니다. 이러한 암호화 된 전자 메일 재생산할 수 있습니다.
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a>해지 된 암호화 된 전자 메일 받는 사람 환경

전자 메일을 해지 되 면 받는 됩니다 오류가 발생 하는 Office 365 메시지 암호화 포털을 통해 암호화 된 전자 메일에 액세스 하려고 할 때: "메시지 해지 된 보낸 사람이" 합니다.

![해지 된 암호화 된 전자 메일을 보여주는 스크린샷](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a>암호화 된 전자 메일을 해지 하는 방법

### <a name="step-1-obtain-the-message-id-of-the-email"></a>1 단계입니다. 전자 메일의 메시지 ID를 가져오려면

암호화 된 메일을 해지할 수 있습니다 전에 메일의 메시지 ID를 수집 하는 것이 해야 합니다. MessageId은 일반적으로 다음과 형식입니다.

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

여러 방법으로 해지 하려고 하는 전자 메일의 메시지 ID를 찾을 수 있습니다. 이 섹션에서는 메시지를 몇 옵션을 설명 하지만 ID를 제공 하는 모든 메서드를 사용할 수 있습니다.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>보안에서 메시지 추적을 사용 하 여 해지 하려면 전자 메일의 메시지 ID를 확인 하려면 &amp; 준수 센터

1. 보낸 사람이 나 받는 사람이 [Office 365 보안 & 준수 센터에서에서 새 메시지 추적](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)을 사용 하 여 전자 메일을 검색 합니다.
2. 찾았으면는 전자 메일 **메시지 추적 세부 정보** 창에서 불러올 수 선택 합니다. 메시지 id. 찾으려고 **추가 정보** 확장 합니다.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>보안에서 Office 메시지 암호화 보고서를 사용 하 여 해지 하려면 전자 메일의 메시지 ID를 확인 하려면 &amp; 준수 센터

1. 보안에서 &amp; 준수 센터 **메시지 암호화 보고서**로 이동 합니다.
2. **세부 정보 보기** 테이블을 선택 하 고 해지 하려는 메시지를 확인 합니다.
3. 메시지 id. 메시지를 포함 하는 세부 정보 보기를 두번클릭 합니다.

### <a name="step-2-revoke-the-mail"></a>2 단계입니다. 메일을 해지  

해지 하려면 전자 메일의 메시지 ID를 알고 있으면 집합 OMEMessageRevocation cmdlet을 사용 하 여 전자 메일을 취소할 수 있습니다.

1. [원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)합니다.

2. 다음과 같이 설정 OMEMessageRevocation cmdlet를 실행 합니다.

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```  

3. 전자 메일이 해지 되었습니다 있는지 여부를 확인 하려면 다음과 같이 입력 하는 Get OMEMessageStatus cmdlet를 실행 합니다.

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | fl Revoked
    ```  
    해지에 성공 하면 cmdlet은 다음과 같은 결과 반환 합니다.  

    `Revoked: True`
