---
title: FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContentPropertyContainsWords
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: 많은 조직에서는 이미 Windows Server FCI(파일 분류 인프라)의 분류 속성, SharePoint의 문서 속성 또는 타사 시스템을 통해 적용된 문서 속성을 사용하여 중요한 정보를 식별하고 분류하는 프로세스를 유지하고 있습니다. 이 정책이 조직에 대해 설명하는 경우 Office 365에서 Windows Server FCI 또는 다른 시스템을 통해 문서에 적용된 속성을 인식하는 DLP 정책을 만들어 DLP 정책이 특정 FCI 또는 기타 속성 값을 갖는 Office 문서에 적용되도록 할 수 있습니다.
ms.openlocfilehash: ad643c77d477f6b9aaecb122010584510ea9bf7e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265320"
---
# <a name="create-a-dlp-policy-to-protect-documents-with-fci-or-other-properties"></a>FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기

Office 365에서 DLP(데이터 손실 방지) 정책을 사용하여 중요한 정보를 식별하고, 모니터링하고, 보호할 수 있습니다. 많은 조직에서는 이미 Windows Server FCI(파일 분류 인프라)의 분류 속성, SharePoint의 문서 속성 또는 타사 시스템을 통해 적용된 문서 속성을 사용하여 중요한 정보를 식별하고 분류하는 프로세스를 유지하고 있습니다. 이 정책이 조직에 대해 설명하는 경우 Office 365에서 Windows Server FCI 또는 다른 시스템을 통해 문서에 적용된 속성을 인식하는 DLP 정책을 만들어 DLP 정책이 특정 FCI 또는 기타 속성 값을 갖는 Office 문서에 적용되도록 할 수 있습니다.
  
![Office 365 외부 분류 시스템을 보여 주는 다이어그램](media/59ad0ac1-4146-4919-abd1-c74d8508d25e.png)
  
예를 들어 조직에서 Windows Server FCI를 사용하여 주민 등록 번호와 같은 PII(개인 식별이 가능한 정보)를 사용하여 문서를 식별한 다음, 문서에 나오는 PII의 종류 및 횟수에 따라 **개인 식별 정보** 속성을 **높음**, **보통**, **낮음**, **공용** 또는 **PII 아님**으로 설정하여 문서를 분류할 수 있습니다. Office 365에서 해당 속성이 **높음** 및 **보통**과 같은 특정 값으로 설정된 문서를 식별한 다음 해당 파일에 대한 액세스 차단과 같은 작업을 수행하는 DLP 정책을 만들 수 있습니다. 해당 속성이 **낮음**으로 설정된 경우에는 전자 메일 알림 전송 등의 다른 작업을 수행하는 다른 규칙을 동일한 정책에 만들 수도 있습니다. 이러한 방식으로 office 365의 DLP는 windows server fci와 통합 되며, windows server 기반 파일 서버에서 office 365를 업로드 하거나 공유 하는 office 문서를 보호 하는 데 도움이 될 수 있습니다.
  
DLP 정책은 단순히 특정 속성 이름/값 쌍을 찾습니다. 문서 속성에 SharePoint 검색에 대한 해당 관리 속성이 있으면 어떤 속성도 사용할 수 있습니다. 예를 들어 SharePoint 사이트 모음에서 **고객** 필수 필드가 있는 **출장 보고서**라는 콘텐츠 형식을 사용할 수 있습니다. 사용자는 출장 보고서를 만들 때마다 고객 이름을 입력해야 합니다. 이 속성 이름/값 쌍을 DLP 정책에서도 사용할 수 있습니다. 예를 들어 **고객** 필드에 **Contoso**가 포함되어 있을 때 외부 사용자의 문서 액세스를 차단하는 규칙을 원할 수 있습니다.
  
특정 Office 365 레이블이 있는 콘텐츠에 DLP 정책을 적용 하려는 경우에는 여기에 나와 있는 단계를 수행 하지 않는 것이 좋습니다. 대신, [레이블을 DLP 정책의 조건으로 사용](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy)하는 방법을 알아보세요.
  
## <a name="before-you-create-the-dlp-policy"></a>DLP 정책 만들기 전

DLP 정책에서 Windows Server FCI 속성 또는 기타 속성을 사용하려면 먼저 SharePoint 관리 센터에서 관리 속성을 만들어야 합니다. 그 이유는 다음과 같습니다.
  
예제
  
Office 365의 DLP는 검색 크롤러를 사용하여 사이트의 중요한 정보를 식별하고 분류한 다음, 검색 인덱스의 보안 부분에 중요한 정보를 저장하기 때문에 이 기능이 중요합니다. Office 365로 문서를 업로드하는 경우 SharePoint는 문서 속성을 기준으로 크롤링된 속성을 자동으로 만듭니다. 그러나 FCI 또는 DLP 정책의 다른 속성을 사용하려면 해당 속성을 갖는 콘텐츠가 인덱스에 보관될 수 있게 크롤링된 속성이 관리 속성에 매핑되어야 합니다.
  
검색 및 관리 속성에 대 한 자세한 내용은 [SharePoint Online에서 검색 스키마 관리](http://go.microsoft.com/fwlink/p/?LinkID=627454)를 참조 하세요.
  
### <a name="step-1-upload-a-document-with-the-needed-property-to-office-365"></a>1단계: 필요한 속성을 갖는 문서를 Office 365에 업로드합니다.

먼저 DLP 정책에서 참조하려는 속성을 갖는 문서를 업로드해야 합니다. Office 365는 해당 속성을 검색한 후 이 속성에서 크롤링된 속성을 자동으로 만듭니다. 다음 단계에서는 관리 속성을 만든 다음 관리 속성을이 크롤링 속성에 매핑합니다.
  
### <a name="step-2-create-a-managed-property"></a>2단계: 관리 속성 만들기

1. Microsoft 365 관리 센터에 로그인 합니다.
    
2. 왼쪽 탐색 영역에서 **관리 센터** \> **SharePoint**를 선택 합니다. 이제 사용자는 SharePoint 관리 센터에 있습니다.
    
3. 왼쪽 탐색 창의 검색 **관리** 페이지 **** \> \> 에서 검색 **스키마 관리**를 선택 합니다.
    
    ![검색 관리 페이지의 SharePoint 관리 센터](media/6bcd3aec-d11a-4f8c-9987-8f35da14d80b.png)
  
4. **관리 속성** 페이지 \> 에서 **새 관리 속성**을 설정 합니다.
    
    ![관리 속성 페이지에서 새 관리 속성 단추가 강조 표시 된](media/b161c764-414c-4037-83ed-503a49fb4410.png)
  
5. 속성의 이름 및 설명을 입력합니다. 이 이름은 DLP 정책에 표시되는 이름입니다.
    
6. **형식**에서 **텍스트**를 선택합니다. 
    
7. **기본 특징** 아래에서 **쿼리 가능** 및 **조회 가능**을 선택합니다.
    
8. **크롤링 속성** \> 에 매핑 아래에서 **매핑을 추가**합니다.
    
9. **크롤링 속성 선택** 대화 상자 \> 에서 DLP 정책 \> **확인**에 사용할 Windows Server fci 속성 또는 기타 속성에 해당 하는 크롤링 속성을 찾아 선택 합니다.
    
    ![크롤링된 속성 선택](media/aeda1dce-1342-48bf-9594-a8e4f230e8aa.png)
  
10. 페이지 \> 맨 아래에서 **확인을**선택 합니다.
    
## <a name="create-a-dlp-policy-that-uses-an-fci-property-or-other-property"></a>FCI 속성 또는 기타 속성을 사용하는 DLP 정책 만들기

이 예에서는 조직에서 Windows Server 기반 파일 서버에 fci를 사용 하 고 있습니다. 특히 **높은**, **중간**, **낮음**, **공용**, **PII가 아닌**사용할 수 있는 **개인 식별** 이 가능한 값이 포함 된 fci 분류 속성을 사용 하 고 있습니다. 이제 Office 365의 DLP 정책에서 기존 fci 분류를 활용 하려고 합니다.
  
먼저 위 단계에 따라 SharePoint Online에서 관리 속성을 만듭니다. 이 속성은 FCI 속성에서 자동으로 만들어진 크롤링 속성에 매핑됩니다.
  
다음으로, 조건 **문서 속성**을 사용 하는 두 개의 규칙을 포함 하는 DLP 정책을 만듭니다.
  
- **fci PII 콘텐츠-높음, 보통** 첫 번째 규칙은 fci 분류 속성 **개인 식별 정보가** **높은** 또는 **보통** 이 고 문서가 조직 외부의 사용자와 공유 되는 경우 문서에 대 한 액세스를 제한 합니다. 
    
- **fci PII 콘텐츠-낮음** 두 번째 규칙은 fci 분류 속성 **개인 식별 정보가** **낮은** 정보이 고 문서가 조직 외부의 사용자와 공유 되는 경우 문서 소유자에 게 알림을 보냅니다. 
    
### <a name="create-the-dlp-policy-by-using-powershell"></a>PowerShell을 사용 하 여 DLP 정책 만들기

조건 **문서 속성** 에는 보안 &amp; 및 준수 센터의 UI에서 일시적으로 사용할 수 없지만 PowerShell을 사용 하 여이 조건을 계속 사용할 수 있습니다. `New\Set\Get-DlpCompliancePolicy` cmdlet을 사용 하 여 DLP 정책에 대 한 작업을 수행 하 고 `New\Set\Get-DlpComplianceRule` `ContentPropertyContainsWords` 매개 변수와 함께 cmdlet을 사용 하 여 조건을 추가할 수 있습니다 **문서 속성에 이러한 값이 포함 되어**있습니다.
  
이러한 cmdlet에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터 cmdlet](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)를 참조 하세요.
  
1. [원격 PowerShell을 사용하여 Office 365 보안 및 준수 센터에 연결](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. 을 사용 하 `New-DlpCompliancePolicy`여 정책을 만듭니다.
    
    다음은 모든 위치에 적용 되는 DLP 정책을 만드는 PowerShell 예제입니다.
    
      ```
      New-DlpCompliancePolicy -Name FCI_PII_policy -ExchangeLocation All -SharePointLocation All -OneDriveLocation All -Mode Enable
      ```

3. 위에서 설명한 두 가지 규칙을 사용 하 `New-DlpComplianceRule`여, 즉 **낮은** 값에 대 한 규칙을 만들고, **높은** 값과 **중간** 가치에 대해 다른 규칙을 만듭니다. 
    
    다음은 이러한 두 가지 규칙을 만드는 PowerShell 예제입니다. 속성 이름/값 쌍은 따옴표로 묶여 있고 속성 이름에는 다음과 같이 공백 없이 쉼표로 구분 하 여 여러 값을 지정할 수 있습니다.`"<Property1>:<Value1>,<Value2>","<Property2>:<Value3>,<Value4>"....`
    
      ```
      New-DlpComplianceRule -Name FCI_PII_content-High,Moderate -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $true -ContentPropertyContainsWords "Personally Identifiable Information:High,Moderate" -Disabled $falseNew-DlpComplianceRule -Name FCI_PII_content-Low -Policy FCI_PII_policy -AccessScope NotInOrganization -BlockAccess $false -ContentPropertyContainsWords "Personally Identifiable Information:Low" -Disabled $false -NotifyUser Owner
      ```

    Windows Server fci에는이 예에서 사용 되는 **개인 식별** 이 가능한 정보를 포함 하 여 기본 제공 되는 여러 속성이 포함 되어 있습니다. 각 속성에 사용할 수 있는 값은 조직 마다 다를 수 있습니다. 여기에서 사용 되는 **높은**값, **중간 규모**및 **낮음을** 예로 들 수 있습니다. 조직의 경우 windows server fci 분류 속성을 사용할 수 있는 값을 포함 하는 파일 서버 기반 파일 서버 자세한 내용은 [분류 속성 만들기](http://go.microsoft.com/fwlink/p/?LinkID=627456)항목을 참조 하십시오.
    
완료 되 면 정책에는 문서 속성을 사용 하는 두 가지 새 규칙에 **이러한 값 조건이 포함** 되어 있어야 합니다. 이 조건은 UI에는 표시 되지 않지만 다른 조건, 작업 및 설정은 표시 됩니다. 
  
규칙 하나는 **개인 식별 정보** 속성이 **높은** 또는 **보통**인 콘텐츠에 대한 액세스를 차단합니다. 또 다른 규칙은 **개인 식별 정보** 속성이 **낮음**인 콘텐츠에 대해 알림을 보냅니다.
  
![방금 만든 두 규칙을 보여 주는 새로운 DLP 정책 대화](media/5c56c13b-62a5-4f25-8eb7-ce83a844bb12.png)
  
## <a name="after-you-create-the-dlp-policy"></a>DLP 정책을 만든 후

이전 섹션의 단계를 수행 하면 해당 속성을 사용 하 여 콘텐츠를 빠르게 검색할 DLP 정책이 생성 되지만 콘텐츠가 새로 업로드 되는 경우 (콘텐츠가 인덱싱되는 경우) 또는 해당 콘텐츠가 이전에 편집 된 경우에 한 해 콘텐츠를 다시 인덱싱할 수 있습니다. .
  
모든 위치에서 해당 속성을 갖는 콘텐츠를 검색하려는 경우 DLP 정책이 해당 속성의 모든 콘텐츠를 인식할 수 있게 라이브러리, 사이트 또는 사이트 모음을 다시 인덱싱하도록 수동으로 요청할 수 있습니다. SharePoint Online에서 콘텐츠는 정의된 크롤링 일정에 따라 자동으로 크롤링됩니다. 크롤러는 마지막 크롤링 이후에 변경된 콘텐츠를 선택하고 인덱스를 업데이트합니다. 예약된 다음 크롤링 전에 DLP 정책을 통해 콘텐츠를 보호해야 할 경우 다음 단계를 수행할 수 있습니다.
  
> [!CAUTION]
> 사이트를 다시 인덱싱하면 검색 시스템에서 대량의 부하가 발생할 수 있습니다. 시나리오에서 절대적으로 필요한 경우가 아니면 사이트를 다시 인덱싱하지 마세요. 
  
자세한 내용은 [사이트, 라이브러리 또는 목록에 대 한 크롤링 수동 요청과 다시 인덱싱](http://go.microsoft.com/fwlink/p/?LinkID=627457)를 참조 하세요.
  
### <a name="re-index-a-site-optional"></a>사이트 다시 인덱싱(선택 사항)

1. 사이트에서 **설정** (오른쪽 위의 기어 아이콘) \> **사이트 설정을**선택 합니다.
    
2. **검색**에서 **검색 및 오프 라인 가용성** \> 다시 **인덱싱 사이트**를 선택 합니다.
    
## <a name="more-information"></a>추가 정보

- [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)
    
- [템플릿에서 DLP 정책 만들기](create-a-dlp-policy-from-a-template.md)
    
- [DLP 정책에 대한 알림 보내기 및 정책 팁 표시](use-notifications-and-policy-tips.md)
    
- [DLP 정책 템플릿에 포함되는 내용](what-the-dlp-policy-templates-include.md)
    
- [중요 한 정보 유형 목록](what-the-sensitive-information-types-look-for.md)
    

