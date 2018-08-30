---
title: FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContentPropertyContainsWords
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.assetid: 1b9e3c6c-4308-4a20-b11e-c37b8013e177
description: 대부분의 조직에 이미를 식별 하 고 Windows Server 파일 분류 인프라 (FCI), SharePoint에서 문서 속성 또는 문서 속성의 분류 속성을 사용 하 여 중요 한 정보를 분류 하는 프로세스 타사 시스템에 의해 적용 합니다. DLP 정책 특정 FCI 또는 기타를 사용 하 여 Office 문서에 적용 될 수 있도록 다른 시스템 또는 Windows Server FCI 하 여 문서에 적용 된 속성을 인식 하는 Office 365에서 DLP 정책을 조직을 설명 하는 경우 만들 수 있습니다. 속성 값입니다.
ms.openlocfilehash: 057cdad981249e39d6f39f231d8d60ab977e717a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013692"
---
# <a name="create-a-dlp-policy-to-protect-documents-with-fci-or-other-properties"></a>FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기

Office 365에서 DLP(데이터 손실 방지) 정책을 사용하여 중요한 정보를 식별하고, 모니터링하고, 보호할 수 있습니다. 많은 조직에서는 이미 Windows Server FCI(파일 분류 인프라)의 분류 속성, SharePoint의 문서 속성 또는 타사 시스템을 통해 적용된 문서 속성을 사용하여 중요한 정보를 식별하고 분류하는 프로세스를 유지하고 있습니다. 이 정책이 조직에 대해 설명하는 경우 Office 365에서 Windows Server FCI 또는 다른 시스템을 통해 문서에 적용된 속성을 인식하는 DLP 정책을 만들어 DLP 정책이 특정 FCI 또는 기타 속성 값을 갖는 Office 문서에 적용되도록 할 수 있습니다.
  
![Office 365 외부 분류 시스템을 보여 주는 다이어그램](media/59ad0ac1-4146-4919-abd1-c74d8508d25e.png)
  
조직 수 주민등록 번호, 예: 개인 식별 정보 (pii 개인)와 문서를 식별 하려면 Windows Server FCI을 사용 하 고 **개인 식별 정보** 를 설정 하 여 문서를 분류 하는 예 **높음**, **보통**, **낮음**, **공용**, 또는 **하지 PII** 속성 형식에 따라 및 문서에서 발견 PII의 횟수입니다. Office 365의 해당 속성이 **높은** 및 **중간**규모와 같은 특정 값으로 설정 된 문서를 식별 하 고 다음 해당 파일에 액세스 차단 등는 작업을 수행 하는 DLP 정책을 만들 수 있습니다. 동일한 정책을 속성은 전자 메일 알림을 보내는 것과 같은 **Low**설정 된 경우 다른 작업을 수행 되는 다른 규칙을 사용할 수 있습니다. 이와 같은 방식이으로 DLP Office 365에 대 한 Windows Server FCI와 통합 하 고 Office 문서 업로드 또는 Windows Server 기반 파일 서버에서 Office 365에 공유를 보호할 수 있습니다.
  
DLP 정책은 단순히 특정 속성 이름/값 쌍을 찾습니다. 문서 속성에 SharePoint 검색에 대한 해당 관리 속성이 있으면 어떤 속성도 사용할 수 있습니다. 예를 들어 SharePoint 사이트 모음에서 **고객** 필수 필드가 있는 **출장 보고서**라는 콘텐츠 형식을 사용할 수 있습니다. 사용자는 출장 보고서를 만들 때마다 고객 이름을 입력해야 합니다. 이 속성 이름/값 쌍을 DLP 정책에서도 사용할 수 있습니다. 예를 들어 **고객** 필드에 **Contoso**가 포함되어 있을 때 외부 사용자의 문서 액세스를 차단하는 규칙을 원할 수 있습니다.
  
메모는 DLP 정책에 따라 특정 Office 365 레이블을 사용 하 여 콘텐츠를 적용 하려는 경우 하지 따라야 여기에 단계입니다. 대신, 설명 [레이블 DLP 정책에서 조건으로 사용](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy)하는 방법입니다.
  
## <a name="before-you-create-the-dlp-policy"></a>DLP 정책 만들기 전

Windows Server FCI 속성 또는 다른 DLP 정책을 사용할 수 있으려면 SharePoint 관리 센터에서 관리 되는 속성을 만들려면 해야 합니다. 그 이유는 다음과 같습니다.
  
예제
  
Office 365의 DLP는 검색 크롤러를 사용하여 사이트의 중요한 정보를 식별하고 분류한 다음, 검색 인덱스의 보안 부분에 중요한 정보를 저장하기 때문에 이 기능이 중요합니다. Office 365로 문서를 업로드하는 경우 SharePoint는 문서 속성을 기준으로 크롤링된 속성을 자동으로 만듭니다. 그러나 FCI 또는 DLP 정책의 다른 속성을 사용하려면 해당 속성을 갖는 콘텐츠가 인덱스에 보관될 수 있게 크롤링된 속성이 관리 속성에 매핑되어야 합니다.
  
검색 및 관리 속성에 대 한 자세한 내용은 [SharePoint Online에서 검색 스키마 관리](http://go.microsoft.com/fwlink/p/?LinkID=627454)를 참조 하십시오.
  
### <a name="step-1-upload-a-document-with-the-needed-property-to-office-365"></a>1단계: 필요한 속성을 갖는 문서를 Office 365에 업로드합니다.

먼저 DLP 정책에서 참조 하는 원하는 속성을 사용 하 여 문서를 업로드 해야 합니다. Office 365의 속성을 검색 하 고에서 크롤링된 속성을 자동으로 만들 됩니다. 다음 단계에서 관리 속성을 만들고이 크롤링된 속성을 관리 속성에 매핑합니다.
  
### <a name="step-2-create-a-managed-property"></a>2단계: 관리 속성 만들기

1. Office 365 관리 센터에 로그인합니다.
    
2. 왼쪽 탐색 영역에서 **관리 센터** 를 선택 \> **SharePoint**합니다. 넌 이제 SharePoint 관리 센터에서.
    
3. 왼쪽 탐색 영역에서 **검색** 을 선택 \> **검색 관리** 페이지에서 \> **검색 스키마를 관리**합니다.
    
    ![검색 관리 페이지의 SharePoint 관리 센터](media/6bcd3aec-d11a-4f8c-9987-8f35da14d80b.png)
  
4. **관리 속성** 페이지에서 \> **새 관리 속성**입니다.
    
    ![관리 속성 페이지에서 새 관리 속성 단추가 강조 표시 된](media/b161c764-414c-4037-83ed-503a49fb4410.png)
  
5. 속성의 이름 및 설명을 입력합니다. 이 이름은 DLP 정책에 표시되는 이름입니다.
    
6. **형식**에서 **텍스트**를 선택합니다. 
    
7. **기본 특징** 아래에서 **쿼리 가능** 및 **조회 가능**을 선택합니다.
    
8. **크롤링 속성에 대 한 매핑을** 아래에서 \> **매핑 추가**합니다.
    
9. **크롤링 속성 선택** 대화 상자에서 \> 찾기 및 Windows Server FCI 속성이 나 DLP 정책에서 사용할 다른 속성에 해당 하는 크롤링된 속성 선택 \> **확인**합니다.
    
    ![크롤링된 속성 선택](media/aeda1dce-1342-48bf-9594-a8e4f230e8aa.png)
  
10. 페이지의 맨 아래에 \> **확인**합니다.
    
## <a name="create-a-dlp-policy-that-uses-an-fci-property-or-other-property"></a>FCI 속성 또는 기타 속성을 사용하는 DLP 정책 만들기

이 예제에서는 조직에서 Windows 서버 기반 파일 서버의 FCI을 사용 특히, **높음**, **보통**, **낮음**, **공용**및 **하지 PII**의 가능한 값을 사용 하 여 **개인 식별 정보** 를 라는 FCI 분류 속성을 사용 하 든 합니다. 이제을 Office 365의 해당 DLP 정책에서 자신의 기존 FCI 분류를 활용 하 여 원합니다.
  
먼저 위 단계에 따라 SharePoint Online에서 관리 속성을 만듭니다. 이 속성은 FCI 속성에서 자동으로 만들어진 크롤링 속성에 매핑됩니다.
  
다음으로, DLP 정책을 조건을 **문서 속성이 포함 하 고 다음이 값 중 하나**를 사용 모두 두 규칙을 만듭니다.
  
- **FCI PII 콘텐츠-높음, 보통 수준의** 첫번째 규칙 FCI 분류 속성 **개인 식별 정보** 는 **높은** 또는 **보통** 및 조직 외부의 사용자와 문서를 공유 하는 경우 문서에 대 한 액세스를 제한 합니다. 
    
- **FCI PII 콘텐츠-낮음** 두번째 규칙 FCI 분류 속성 **개인 식별 정보** **낮음** 및 문서와 같으면 문서 소유자에 대 한 알림을 조직 외부의 사용자와 공유를 보냅니다. 
    
### <a name="create-the-dlp-policy-by-using-powershell"></a>PowerShell을 사용 하 여 DLP 정책 만들기

**문서 속성이 포함 하 고 이러한 값** 조건 일시적으로 사용할 수 없다는 보안의 UI에서 참고 &amp; 수 있지만 준수 센터는 PowerShell을 사용 하 여이 조건은 계속 사용할 수 있습니다. 사용할 수 있습니다는 `New\Set\Get-DlpCompliancePolicy` DLP 정책을 사용 하 고 사용 하기 위한 cmdlet는 `New\Set\Get-DlpComplianceRule` 으로 cmdlet은 `ContentPropertyContainsWords` **문서 속성이 포함 하 고 다음이 값 중 하나라도**조건을 추가 하려면 매개 변수입니다.
  
이러한 cmdlet에 대 한 자세한 내용은 참조 하십시오. [Office 365 보안 &amp; 준수 센터 cmdlet](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)합니다.
  
1. [Office 365 보안 연결할 &amp; 원격 PowerShell을 사용 하 여 준수 센터](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. 정책을 사용 하 여 만들기 `New-DlpCompliancePolicy`합니다.
    
    모든 위치에 적용 되는 DLP 정책을 생성 하는 PowerShell 예는 다음과 같습니다.
    
      ```
      New-DlpCompliancePolicy -Name FCI_PII_policy -ExchangeLocation All -SharePointLocation All -OneDriveLocation All -Mode Enable
      ```

3. 사용 하 여 위에서 설명한 두 규칙을 만들 `New-DlpComplianceRule`, 여기서 **낮** 은 값에 대 한 규칙을 하나이 고 다른 규칙은 **높은** 위험과 **보통** 값입니다. 
    
    이러한 두 규칙을 만드는 PowerShell 예제는 다음과 같습니다. Note 속성 이름/값 쌍은 따옴표로 묶인, 하 고 속성 이름을 다음과 같이 공백 없이 쉼표로 구분 하는 여러 값을 지정할 수 있습니다`"<Property1>:<Value1>,<Value2>","<Property2>:<Value3>,<Value4>"....`
    
      ```
      New-DlpComplianceRule -Name FCI_PII_content-High,Moderate -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $true -ContentPropertyContainsWords "Personally Identifiable Information:High,Moderate" -Disabled $falseNew-DlpComplianceRule -Name FCI_PII_content-Low -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $false -ContentPropertyContainsWords "Personally Identifiable Information:Low" -Disabled $false -NotifyUser Owner
      ```

    Windows Server FCI이 예제에 사용 되는 **개인 식별 정보** 를 포함 하 여 기본 제공 속성을 포함 하는 메모 합니다. 각 속성에 사용 가능한 값은 모든 조직에 대 한 다 수 있습니다. **높음**, **보통**, **낮** 은 값과 여기에서 사용은 예제 일 뿐입니다. 조직에 대 한 Windows 서버 기반 파일 서버에 있는 파일 서버 리소스 관리자에서에서 사용할 수 있는 해당 값을 사용 하 여 Windows Server FCI 분류 속성을 볼 수 있습니다. 자세한 내용은 [분류 속성 만들기](http://go.microsoft.com/fwlink/p/?LinkID=627456)를 참조 하십시오.
    
확인이 끝나면 정책에 따라 두 새 규칙을 모두 조건을 사용 하 여는 **문서 속성이 포함 하 고 다음이 값 중 하나** 있어야 합니다. 이 조건이 나타나지 않습니다 UI에 하지만 다른 조건, 작업 및 설정을 참고 표시 됩니다. 
  
규칙을 하나 블록 여기서 **개인 식별 정보** 속성은 **높음** 또는 **보통**콘텐츠에 액세스 합니다. 두번째 규칙 **낮음** **개인 식별 정보** 속성과 일치 하는 여기서 콘텐츠에 대 한 알림을 보냅니다.
  
![방금 만든 두 규칙을 보여 주는 새로운 DLP 정책 대화](media/5c56c13b-62a5-4f25-8eb7-ce83a844bb12.png)
  
## <a name="after-you-create-the-dlp-policy"></a>DLP 정책을 만든 후

이전 섹션의 단계를 수행 하는 신속 하 게를 감지 하는 DLP 정책을 콘텐츠 새로 (하는 콘텐츠 인덱싱)을 업로드 하는 경우만 해당 속성을 사용 하 여 콘텐츠를 만들거나 콘텐츠 하는 경우를 이전 하지만 바로 편집 (하는 콘텐츠 다시 인덱싱) .
  
모든 위치에서 해당 속성을 갖는 콘텐츠를 검색하려는 경우 DLP 정책이 해당 속성의 모든 콘텐츠를 인식할 수 있게 라이브러리, 사이트 또는 사이트 모음을 다시 인덱싱하도록 수동으로 요청할 수 있습니다. SharePoint Online에서 콘텐츠는 정의된 크롤링 일정에 따라 자동으로 크롤링됩니다. 크롤러는 마지막 크롤링 이후에 변경된 콘텐츠를 선택하고 인덱스를 업데이트합니다. 예약된 다음 크롤링 전에 DLP 정책을 통해 콘텐츠를 보호해야 할 경우 다음 단계를 수행할 수 있습니다.
  
> [!CAUTION]
> 사이트를 다시 인덱싱 대규모 부하 검색 시스템에서 발생할 수 있습니다. 시나리오 절대적으로 필요 하지 않은 경우 사이트를 인덱스 다시 하지 마십시오. 
  
자세한 내용은 [크롤링 및 사이트, 라이브러리 또는 목록 다시 인덱싱 수동으로 요청](http://go.microsoft.com/fwlink/p/?LinkID=627457)을 참조 하십시오.
  
### <a name="re-index-a-site-optional"></a>사이트 다시 인덱싱(선택 사항)

1. 사이트 **설정** (오른쪽 위에서 기어 아이콘)을 선택 \> **사이트 설정**합니다.
    
2. **검색** **검색 및 오프 라인 사용 가능 여부를** 선택 \> **사이트를 다시 인덱싱해야**합니다.
    
## <a name="more-information"></a>추가 정보

- [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)
    
- [템플릿에서 DLP 정책 만들기](create-a-dlp-policy-from-a-template.md)
    
- [DLP 정책에 대한 알림 보내기 및 정책 팁 표시](use-notifications-and-policy-tips.md)
    
- [DLP 정책 템플릿에 포함되는 내용](what-the-dlp-policy-templates-include.md)
    
- [중요 한 정보 유형 목록](what-the-sensitive-information-types-look-for.md)
    

