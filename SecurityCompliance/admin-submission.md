---
title: Office 365, O365 전송, Office 365 스팸 문제, O365 가양성, 검색을 위한 전자 메일 전송, office 365에서 의심 스러운 전자 메일, 메일 검색, 365 피싱에 대 한 Microsoft 검색, Microsoft scan for 피싱, submit for 스팸, 제출 전자 메일, 메일 제출
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 08/06/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Office 365 테 넌 트에서 의심 스러운 전자 메일, 의심 스러운 메일, 스팸 및 기타 해로운 메시지, Url 및 파일을 검색을 위해 Microsoft에 제출 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 5a909e8b587e2a1265c1b2afbd5e063d46a04e2c
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230952"
---
# <a name="how-to-submit-suspected-spam-phish-urls-and-files-to-microsoft-for-office-365-scanning"></a>Microsoft에 Office 365를 검색 하기 위해 의심 스러운 스팸, 피싱, Url 및 파일을 제출 하는 방법

관리자는 Office 365에서 Microsoft가 검색을 위해 파일 또는 네트워크 메시지 ID, Url 및 파일을 사용 하 여 전자 메일을 보낼 수 있습니다. 업데이트 된 전송 섹션에도 사용자가 보고 한 메시지가 포함 되며, EOP을 사용 하는 모든 고객이 사용할 수 있습니다.

전자 메일을 제출 하면 메일에 포함 된 Url 및 첨부 파일을 검사 하는 것은 물론 수신 전자 메일을 허용 했을 수 있는 모든 정책에 대 한 정보를 받게 됩니다. 메일을 허용할 수 있는 정책에는 개인 사용자의 수신 허용-보낸 사람 목록 및 ETR 규칙과 같은 테 넌 트 수준 정책이 포함 됩니다. 

## <a name="how-to-submit-content-to-microsoft-for-office-365-scanning"></a>Office 365 검색을 위해 Microsoft에 콘텐츠를 전송 하는 방법

Microsoft로 콘텐츠를 전송 하려면 제출 페이지의 왼쪽 위에 있는 **새 제출** 단추를 클릭 합니다. 전자 메일, URL 또는 파일을 전송 하는 옵션을 사용 하 여 페이지 오른쪽에 플라이 아웃이 표시 됩니다. 

### <a name="submit-an-email-to-microsoft"></a>Microsoft에 전자 메일 제출
![전자 메일 전송 예](media/submission-flyout-email.PNG)
1. 전자 메일을 제출 하려면 **전자 메일** 을 선택 하 고 전자 메일 **네트워크 메시지 ID** 를 지정 하거나 전자 메일 파일을 업로드 합니다. 

2. 정책 확인을 실행 하려는 받는 사람을 지정 합니다. 정책 확인은 사용자 또는 테 넌 트 수준 정책으로 인해 전자 메일에서 검색이 사용 되지 않는지 확인 합니다. 

3. 전자 메일이 차단 되었는지 여부를 지정 합니다. 전자 메일이 차단 되어야 하는 경우 스팸, 피싱 또는 맬웨어로 차단 되어야 하는지 여부를 지정 합니다. 어떤 형식을 사용할 수 있는지 잘 모르는 경우에는 최상의 judgement를 사용 합니다.  

* 전송 시 정책으로 인해 필터가 생략 되 면 해당 정책에 대 한 정보를 볼 수 있습니다.

* 하나 이상의 정책으로 인해 필터가 무시 되지 않으면 몇 분 안에 검색이 완료 됩니다. 상태 링크를 클릭 하 여 전송에 대 한 추가 정보를 볼 수 있습니다. 여기에는 정책 확인 및 다시 검사 결과의 결과가 포함 됩니다. 참고 Office 365 ATP 전체 필터링 스택을 통해 전자 메일을 다시 실행 하지만 메일, URL 또는 파일의 특정 특성에 따라 부분 다시 검사를 실행 하는 것은 아닙니다. 

4. **제출** 단추를 클릭 합니다.

### <a name="submit-a-url-to-microsoft"></a>Microsoft에 URL 제출
![전자 메일 전송 예](media/submission-url-flyout.png)
1. URL을 제출 하려면 플라이 아웃에서 **url** 을 선택 합니다. 프로토콜 (**https://**)을 포함 하 여 전체 URL을 입력 합니다. 

* **필터**를 선택한 경우 URL이 피싱 또는 맬웨어 인지 지정 합니다.

2. **제출** 단추를 클릭 합니다. 


### <a name="submit-a-file-to-microsoft"></a>Microsoft로 파일 제출
![전자 메일 전송 예](media/submission-file-flyout.PNG)
1. 파일을 제출 하려면 플라이 아웃에서 **파일** 을 선택 하 고 검색할 파일을 업로드 합니다. 

2. **제출** 단추를 클릭 합니다.


## <a name="related-topics"></a>관련 항목

[Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)
  
[Office 365에서 위협 으로부터 보호](protect-against-threats.md)
  
[Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)
  

