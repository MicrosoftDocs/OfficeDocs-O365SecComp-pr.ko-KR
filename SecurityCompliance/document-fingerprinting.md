---
title: 문서 지문
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
search.appverid: MET150
ms.service: exchange-online
localization_priority: Normal
ms.assetid: 1e0c579c-26e0-462a-a1b0-d7506dfe05fa
description: 조직의 정보 근로자는 일반적인 하루 중 많은 종류의 중요 한 정보를 처리 합니다. 문서 지문을를 사용 하면 조직 전체에서 사용 되는 표준 양식을 식별 하 여이 정보를 보다 쉽게 보호할 수 있습니다. 이 항목에서는 문서 지문을 개념 및 PowerShell을 사용 하 여 만드는 방법에 대해 설명 합니다.
ms.openlocfilehash: 20b9f59902c52d347e7c439cb6f380ee9fd4a30e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341289"
---
# <a name="document-fingerprinting"></a>문서 지문

조직의 정보 근로자는 일반적인 하루 중 많은 종류의 중요 한 정보를 처리 합니다. 보안 &amp; 및 준수 센터에서 문서 지문을를 사용 하면 조직 전체에서 사용 되는 표준 양식을 식별 하 여이 정보를 보다 쉽게 보호할 수 있습니다. 이 항목에서는 문서 지문을 개념 및 PowerShell을 사용 하 여 만드는 방법에 대해 설명 합니다.
  
## <a name="basic-scenario-for-document-fingerprinting"></a>문서 지문 관련 기본 시나리오

문서 지문을는 dlp (데이터 손실 방지) 기능을 사용 하 여 사용자가 특정 정보 유형으로 표준 양식을 변환 하 고, 이러한 유형은 해당 규칙에서 사용할 수 있습니다. 예를 들어 빈 특허 서식 파일을 기준으로 문서 지문을 만든 다음 중요 한 콘텐츠가 채워진 모든 보내는 특허 서식 파일을 검색 하 고 차단 하는 DLP 정책을 만들 수 있습니다. 경우에 따라 보낸 사람에 게 중요 한 정보를 보낼 수 있음을 알리는 [정책 팁](use-notifications-and-policy-tips.md) 을 설정 하 고 보낸 사람에 게 해당 받는 사람이 특허권을 받을 자격이 있는지 확인 해야 합니다. 이 프로세스는 조직에서 사용 되는 텍스트 기반 양식에서 작동 합니다. 업로드할 수 있는 양식의 추가 예는 다음과 같습니다. 
  
- 정부 양식
    
- HIPAA(Health Insurance Portability and Accountability Act) 준수 양식
    
- 인사 부서의 직원 정보 양식
    
- 조직용으로 특수 작성된 사용자 지정 양식
    
조직에서 특정 양식을 사용 하 여 중요 한 정보를 전송 하는 비즈니스 연습이 이미 설정 되어 있는 것이 이상적입니다. 문서 지 문으로 변환 되는 빈 양식을 업로드 하 고 해당 정책을 설정 하 고 나면 DLP는 아웃 바운드 메일에서 해당 지문과 일치 하는 문서를 검색 합니다.
  
## <a name="how-document-fingerprinting-works"></a>문서 지문의 작동 방식

문서에 실제 지문이 포함 되지 않은 것으로 추측 되었지만 이름이이 기능을 설명 하는 데 도움이 될 것입니다. 사용자의 지문에 고유한 패턴이 있는 것 처럼 문서에는 고유한 단어 패턴이 있습니다. 파일을 업로드 하면 DLP는 문서에서 고유한 단어 패턴을 식별 하 고, 해당 패턴을 기반으로 문서 지문을 만들며, 해당 문서 지문을 사용 하 여 동일한 패턴을 포함 하는 아웃 바운드 문서를 검색 합니다. 따라서 양식이 나 서식 파일을 업로드 하면 가장 효율적인 유형의 문서 지문을 만듭니다. 양식을 작성 하는 모든 사용자는 동일한 원본 단어 집합을 사용 하 고 문서에 자체 단어를 추가 합니다. 아웃 바운드 문서가 암호로 보호 되지 않고 원본 양식의 모든 텍스트를 포함 하는 경우 DLP는 문서가 문서 지문과 일치 하는지 여부를 확인할 수 있습니다.
  
다음 예에서는 특허 서식 파일을 기준으로 문서 지문을 만들 때 수행되는 작업을 설명하지만 원하는 모든 양식을 기준으로 문서 지문을 만들 수 있습니다.
  
**특허 서식 파일의 문서 지문과 일치하는 특허 문서의 예**

![Document_Fingerprinting_diagram-.png](media/Document_Fingerprinting_diagram.png)
  
특허 서식 파일에는 "특허 title", "Inventors", "설명" 이라는 빈 필드와 각 필드에 대 한 설명 (단어 패턴)이 포함 되어 있습니다. 원본 특허 서식 파일을 업로드 하는 경우 지원 되는 파일 형식 중 하 나와 일반 텍스트로 입력 해야 합니다. DLP는이 단어 패턴을 원본 텍스트를 나타내는 고유한 해시 값을 포함 하는 작은 유니코드 XML 파일인 문서 지 수로 변환 하 고, 지문은 Active Directory에서 데이터 분류로 저장 됩니다. 보안을 위해 원본 문서 자체는 서비스에 저장 되지 않으며, 해시 값만 저장 되며, 원래 문서를 해시 값에서 다시 구성할 수 없습니다. 그런 다음 특허 지문을 사용 하 여 DLP 정책과 연결할 수 있는 중요 한 정보 유형이 됩니다. 지문을 dlp 정책과 연결한 후 dlp는 특허 지문과 일치 하는 문서를 포함 하는 아웃 바운드 전자 메일을 검색 하 고 조직의 정책에 따라 처리 합니다. 

예를 들어 일반 직원이 특허를 포함 하는 보내는 메시지를 보내지 못하게 하는 DLP 정책을 설정할 수 있습니다. DLP는 특허권 지문을 사용 하 여 특허권을 검색 하 고 해당 전자 메일을 차단 합니다. 또한 업무상 필요한 업무에 따라 법적 부서에 게 다른 조직에 특허권을 보낼 수 있도록 하는 것이 좋습니다. DLP 정책에서 해당 부서에 대 한 예외를 만들어 특정 부서가 중요 한 정보를 보내도록 허용 하거나, 사용자가 비즈니스 정당성을 사용 하 여 정책 팁을 재정의 하도록 허용할 수 있습니다.
  
### <a name="supported-file-types"></a>지원되는 파일 형식

문서 지문을는 메일 흐름 규칙 (전송 규칙이 라고도 함)에서 지원 되는 것과 동일한 파일 형식을 지원 합니다. 지원 되는 파일 형식 목록은 [메일 흐름 규칙 콘텐츠 검사에 지원 되는 파일 형식을](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection)참조 하세요. 파일 형식에 대 한 한 가지 간단한 참고 사항: 메일 흐름 규칙 및 문서 지문을는 dotx 파일 형식을 지원 하지 않으므로 Word의 서식 파일 이기 때문에 혼란을 가져올 수 있습니다. 이 문서 및 기타 Document 지문을 항목에 "template" 이라는 단어가 표시 되 면 서식 파일 형식이 아닌 표준 양식으로 설정한 문서를 참조 합니다.
  
#### <a name="limitations-of-document-fingerprinting"></a>문서 지문의 제한

문서 지문을는 다음과 같은 경우에 중요 한 정보를 검색 하지 않습니다.
  
- 암호로 보호된 파일
    
- 이미지만 포함된 파일
    
- 문서 지문을 만드는 데 사용된 원본 양식의 모든 텍스트가 포함되지 않는 문서
    
## <a name="use-powershell-to-create-a-classification-rule-package-based-on-document-fingerprinting"></a>PowerShell을 사용 하 여 문서 지문을를 기반으로 분류 규칙 패키지 만들기

현재 보안 &amp; 및 준수 센터에서 PowerShell을 사용 하 여 문서 지문을 만들 수 있습니다. 연결 하려면 [connect to Office 365 Security & 준수 센터 PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)를 참조 하세요.

DLP는 분류 규칙 패키지를 사용 하 여 중요 한 콘텐츠를 검색 합니다. 문서 지문을 기준으로 분류 규칙 패키지를 만들려면 **DlpSensitiveInformationType** cmdlet을 사용 합니다 **** . **새-dlpfingerprint** 의 결과는 데이터 분류 규칙의 외부에 저장 되지 않으므로 항상 **DlpSensitiveInformationType** 에서 **새-dlpfingerprint** 및 **DlpSensitiveInformationType** 를 실행 합니다. PowerShell 세션 다음은 C:\My documents\contoso Employee 서식 파일을 기반으로 새 문서 지문을 만드는 예제입니다. 새 지문을 변수로 저장 하 여 동일한 PowerShell 세션에서 **DlpSensitiveInformationType** cmdlet과 함께 사용할 수 있도록 합니다. 
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Employee Template.docx" -Encoding byte -ReadCount 0
$Employee_Fingerprint = New-DlpFingerprint -FileData $Employee_Template -Description "Contoso Employee Template"
```

C:\My Documents\Contoso Customer Information Form.docx 파일의 문서 지문을 사용하는 "Contoso Employee Confidential"이라는 새 데이터 분류 규칙을 만들어 보겠습니다.
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Customer Information Form.docx" -Encoding byte -ReadCount 0
$Customer_Fingerprint = New-DlpFingerprint -FileData $Customer_Form -Description "Contoso Customer Information Form"
New-DlpSensitiveInformationType -Name "Contoso Customer Confidential" -Fingerprints $Customer_Fingerprint -Description "Message contains Contoso customer information." 
```

이제 **DlpSensitiveInformationType** cmdlet을 사용 하 여 모든 DLP 데이터 분류 규칙 패키지를 찾을 수 있으며이 예에서 "Contoso 고객 기밀"은 데이터 분류 규칙 패키지 목록의 일부입니다. 
  
마지막으로, 보안 &amp; 및 준수 센터에서 "Contoso 고객 기밀" 데이터 분류 규칙 패키지를 DLP 정책에 추가 합니다. 이 예에서는 "ConfidentialPolicy" 라는 기존 DLP 정책에 규칙을 추가 합니다.

```
New-DlpComplianceRule -Name "ContosoConfidentialRule" -Policy "ConfidentialPolicy" -ContentContainsSensitiveInformation @{Name="Contoso Customer Confidential"} -BlockAccess $True
```

다음 예제와 같이 Exchange Online의 메일 흐름 규칙에서 데이터 분류 규칙 패키지를 사용할 수도 있습니다. 이 명령을 실행 하려면 먼저 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)해야 합니다. 또한 규칙 패키지를 보안 &amp; 준수 센터에서 Exchange 관리 센터와 동기화 하는 데 시간이 오래 걸립니다.
  
```
New-TransportRule -Name "Notify :External Recipient Contoso confidential" -NotifySender NotifyOnly -Mode Enforce -SentToScope NotInOrganization -MessageContainsDataClassification @{Name=" Contoso Customer Confidential"}

```

이제 DLP는 Contoso Customer 양식과 일치 하는 문서를 검색 합니다.
  
구문 및 매개 변수 정보는 다음 항목을 참조 하십시오.

- [새 dlpfingerprint](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpFingerprint)
- [DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpSensitiveInformationType)
- [DlpSensitiveInformationType을 제거 합니다.](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Remove-DlpSensitiveInformationType)
- [DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpSensitiveInformationType)
- [DlpSensitiveInformationType](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpSensitiveInformationType)
