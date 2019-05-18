---
title: 이벤트 구동 보존
ms.author: stephow
author: stephow-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 이 항목에서는 Microsoft 365 REST API를 사용하여 이벤트를 통한 보존을 자동화하는 비즈니스 프로세스 흐름을 설정하는 방법에 대해 설명합니다.
ms.openlocfilehash: c89abc373a6c0a1de6b6528c638dbd34e586b6d7
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152280"
---
# <a name="automate-event-based-retention"></a>이벤트 기반 보존 자동화

조직의 컨텐츠가 폭발적으로 증가하고 ROT(중복, 구식, 사소)가 될 가능성은 심각한 문제입니다. 법률, 비즈니스 및 규정 준수 문제를 지속적으로 충족하려면 기업은 중요한 정보를 보관하고 보호할 수 있어야하며 관련 정보를 신속하게 찾을 수 있어야 합니다. 중요하고 관련성 있는 정보만 보유하는 것이 비즈니스 성공의 열쇠입니다.

따라서 조직에서는 Office 365 보안 및 준수 센터의 보존 솔루션을 활용할 수 있습니다. 보관은 [보존 레이블](labels.md)을 이용하여 시작할 수 있습니다. 보존 레이블에는 [특정 이벤트에 보존 기간을 적용 ](event-driven-retention.md)할 수 있는 옵션이 있습니다. 일반적으로 보존 기간은 콘텐츠의 생성 날짜 또는 최종 수정 날짜와 같은 알려진 날짜를 기반으로 합니다. 그러나 조직에서는 직원이 퇴사한 후 7년이 경과한 경우와 같은 이벤트 발생에 따라 콘텐츠를 삭제해야 합니다.

규정을 준수하는 콘텐츠 처리를 보장하려면 이벤트 발생시기를 알아야 합니다. 콘텐츠의 양이 급속히 증가함에 따라 콘텐츠를 적시에 적법한 방법으로 보유하고 폐기하는 일이 어려워지고 있습니다.

이벤트 기반 보존은 이 문제점을 해결합니다. 이 항목에서는 Microsoft 365 REST API를 사용하여 이벤트를 통한 보존을 자동화하는 비즈니스 프로세스 흐름을 설정하는 방법에 대해 설명합니다.

## <a name="about-event-based-retention"></a>이벤트 기반 보존에 대한 설명

조직의 규모는 크거나 적정하거나 작을 수 있습니다. 일상적으로 생성되고 관리되는 비즈니스 문서, 법률 문서, 직원 파일, 계약서 및 제품 문서의 수는 급격히 증가하고 있습니다.

예를 들어, 매일, 수십, 수백 명의 직원이 조직에 가입하고 퇴사합니다. HR 부서에서는 비즈니스 요구 사항에 따라 직원 관련 문서를 계속 작성, 업데이트 또는 삭제합니다. 이 프로세스는 비즈니스에 대해 개괄적으로 명시된 다양한 보존 정책의 적용을 받습니다.

- ** 컨텐츠 보유 기간은 컨텐츠 작성, 최종 수정 또는 레이블 지정 날짜와 같은 알려진 날짜** 일 수 있습니다. 예를 들어, 문서를 작성한 후 7 년 동안 문서를 보존한 다음 삭제할 수 있습니다.

- **콘텐츠 보유 기간은 알 수 없는 날짜가 될 수도 있습니다**. 예를 들어 보존 레이블을 사용하면 직원이 조직을 떠나는 경우와 같이 특정 유형의 이벤트가 발생할 때에 대해 보존 기간을 설정할 수 있습니다.

이벤트가 보유 기간의 시작을 트리거하고 해당 이벤트 유형에 적용된 레이블이 있는 모든 컨텐츠는 레이블의 보유 조치를 받습니다. 이를 이벤트 기반 보존이라고합니다. 자세한 내용은 [이벤트 기반 보존 개요](event-driven-retention.md)를 참조하십시오.

## <a name="set-up-event-based-retention"></a>이벤트 기반 보존 설정

이 절에서는 콘텐츠를 보존하기 전에 수행해야 할 작업에 대해 설명합니다.

### <a name="identify-roles"></a>역할 확인

효과적이고 효율적인 비즈니스 문서 보존을 담당하는 레코드 관리 작업을 수행하는 조직 안의 다양한 역할을 식별합니다.

  | **가상 사용자**| **역할**|
  | - | - |
  | 관리자 | SharePoint에 보존 이벤트 유형, 보존 레이블 및 레코드 리포지토리를 만듭니다. |
  | 레코드 관리자                                  | 보존 정책과 보존 일정 지침 및 준수 세부사항을 제공합니다.   |
  | 시스템 관리자(회사)                          | Microsoft 365에서 작동하도록 외부 시스템을 설정하고 관리합니다.                       |
  | 정보 근로자                               | 비즈니스 프로세스(HR, 재무, IT 등)의 수명 주기를 관리합니다.                 |

### <a name="set-up-the-security--compliance-center"></a>보안 및 준수 센터 설정
  
1. 규정 준수 관리자가 직원 퇴사, 계약 만료 또는 제품 제조 종료와 같은 이벤트 유형을 만듭니다([이벤트 기반 보존](https://docs.microsoft.com/ko-KR/office365/securitycompliance/event-driven-retention)의 단계별 프로세스 참조).
    
1. 규정 준수 관리자가 이벤트를 기반으로 보존 레이블을 만들고 레이블을 이벤트 유형과 연결합니다.
    
1. 보존 레이블에 대해 다음과 같이 4종류의 트리거가 있습니다.
            
    1. 만든 날짜
                
    1. 마지막으로 수정한 날짜
                
    1. 레이블 날짜(콘텐츠 레이블이 지정 된 때)
                
    1. 이벤트 기반
    
1. 규정 준수 관리자가 보존 레이블을 게시합니다.

### <a name="set-up-sharepoint"></a>SharePoint 설정
   
레코드 저장소를 만들기 위해 규정 준수 관리자는 다음 작업을 수행합니다.

1. SharePoint 사이트를 생성합니다.

1. 다음 중 하나를 수행합니다.
        
    - SharePoint 라이브러리 만들기: 라이브러리 수준에서 이벤트 기반 레이블을 설정합니다. 자세한 내용은 [ SharePoint 라이브러리, 폴더 또는 문서 집합의 모든 콘텐츠에 기본 보존 레이블 적용](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set)을 참조하십시오.
          
    - SharePoint에서 문서 집합을 설정합니다. 자세한 내용은 [문서 집합 소개](https://support.office.com/ko-KR/article/Introduction-to-Document-Sets-3DBCD93E-0BED-46B7-B1BA-B31DE2BCD234)를 참조하십시오.
      
1. 자산 ID(자산 ID는 조직에서 사용하는 제품 이름 또는 코드입니다. 예를 들어 사원 번호도 자산 ID가 될 수 있습니다)를 각 직원 문서 세트에 할당합니다(자산 ID를 폴더에 할당하면 해당 폴더의 모든 항목이 자동으로 동일한 자산 ID를 상속받게 됩니다. 이는 모든 항목의 보존 기간이 동일한 이벤트에 의해 트리거 될 수 있음을 의미합니다.

## <a name="ways-to-trigger-event-based-retention"></a>이벤트 기반 보존을 트리거하는 방법

두 가지 방법으로 이벤트 기반 보존을 트리거할 수 있습니다.

- **관리 센터 UI 사용** 이 기능은 한 번에 적은 컨텐츠를 유지하거나 보존을 트리거하는 빈도가 월 단위 또는 연 단위처럼 빈번하지 않은 경우 사용할 수 있는 프로세스입니다. 이 방법에 대한 자세한 내용은 [이벤트 기반 보존 개요](event-driven-retention.md)를 참조하세요. 그러나 이처럼 보존을 트리거하는 방법은 시간이 많이 걸리고 오류가 발생하기 쉽기 때문에 확장성이 떨어집니다. 따라서 보존을 트리거하는 완벽한 자동화 솔루션은 데이터의 보안 및 준수를 향상시킬 수 있습니다.

- ** M365 REST API 사용** 이 프로세스는 대용량의 콘텐츠를 한 번에 보존 및/또는 보존을 트리거하는 빈도가 일일 또는 주간과 같이 빈번한 경우에 사용할 수 있습니다. 이 흐름은 기간 업무(LOB) 시스템에서 이벤트가 발생하면이를 감지 한 다음 보안 및 규정 준수 센터에서 관련 이벤트를 자동으로 만듭니다. UI가 발생할 때마다 UI에 수동으로 이벤트를 만들 필요가 없습니다.

REST API를 사용할 수 있는 옵션은 다음과 같이 두 가지가 있습니다.

- ** Microsoft Flow 또는 유사 애플리케이션**을 사용하여 이벤트 발생을 자동으로 트리거할 수 있습니다. Microsoft Flow를 통해 다른 시스템과의 연결을 조정할 수 있습니다. 사용자 지정 솔루션이 없어도 Microsoft Flow를 사용할 수 있습니다.

- **REST API를 호출하는 PowerShell 또는 HTTP 클라이언트** PowerShell (버전 6 이상)을 사용하여 Microsoft 365 REST API를 호출하여 이벤트를 만듭니다. 

Rest API는 서비스 자원에 대한 작성/검색/갱신/삭제 액세스를 제공하는 HTTP 조작(메소드) 세트를 지원하는 서비스 엔드 포인트입니다. 자세한 정보는 [ REST API 요청/응답 구성 요소](https://docs.microsoft.com/ko-KR/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse). 이 경우 Microsoft 365 REST API를 사용하여 POST 및 GET 메서드를 사용하여 이벤트를 만들고 검색 할 수 있습니다.

## <a name="example-scenarios"></a>예제 시나리오

다음과 같은 시나리오를 고려해 봅시다.

### <a name="scenario-1-employees-leaving-the-organization"></a>시나리오 1: 조직을 떠나는 직원 

조직은 직원 한 명당 수많은 직원 관련 문서를 작성하고 저장합니다. 이 서류들은 각 직원의 고용 기간 동안 관리되고 유지됩니다. 그러나 직원이 조직을 떠나거나 고용이 해지되는 경우 조직은 법률 및 비즈니스 요구사항에 따라 해당 직원의 문서를 규정된 기간 동안 보유해야 합니다.

이제 여러 명의 직원이 매일 조직을 떠나는 경우 조직에서는 매일 수천 개의 문서가 아니라도 수백 가지의 보존 시계를 트리거해야 합니다.

이 외에도 직원 보유 기간은 직원 기록의 유형에 따라 종업원의lotus jam 근무 종료일자 + 일수, 개월수 또는 연수로 계산해야 합니다. 예를 들어, 동일한 직원에 대한 근로자 보상과 수당 서류의 보존 기간이 서로 다를 수 있습니다.

아래 다이어그램은 단일 이벤트와 연관된 레이블이 어떻게 여러 개가 존재할 수 있는지 보여줍니다. 여기서 Worker 's compensation 레이블 아래의 모든 파일과 Employee benefits 레이블 아래의 모든 파일은 조직을 떠나는 직원이라는 단일 이벤트와 연관됩니다. 이러한 서로 다른 파일에는 서로 다른 보존 시계가 있습니다. 따라서 직원이 조직을 떠날 때 각 레이블 내의 파일에는 다른 보존 기간이 적용됩니다. 각 종업원의 개별 파일 유형 또는 레이블에 대해 이러한 다양한 보존 시계를 실행하는 것은 매우 어려운 작업입니다. 여러 직원에게이 작업을 수행한다고 가정해 보십시오.

![이벤트 유형, 이벤트 및 레이블 다이어그램](media/automate-event-driven-retention-event-diagram-employee-leaving.png)

따라서 여러 직원에 대해 서로 다른 보존 시계를 트리거하는 자동화된 프로세스는 시간을 절약해주고 오류가 없으며 매우 효율적입니다.

**이 시나리오에 대한 자동 이벤트 기반 보유 구성:**

![조직을 떠나는 직원 시나리오에 대한 역할 및 작업 다이어그램](media/automate-event-driven-retention-employee-termination-diagram.png)

  - 관리자는 문서 집합에 Jane Doe, John Smith와 같은 직원 폴더를 생성합니다.

  - 관리자는 수당, 급여, 근로 보상 등과 같은 직원 파일을 각 직원 폴더에 추가합니다.

  - 관리자는 각 직원 폴더에 자산 Id를 할당합니다. 

  - SCC 관리자 l

  - 보안 및 준수 센터에 로그인

  - SCC 관리자가 “직원 퇴사”, “직원 채용” 이벤트와 같은 직원 관련 이벤트 유형을 만듭니다.

  - SCC 관리자가 “직원 보존” 레이블을 만듭니다.

  - 이 "직원 보존"레이블은 SharePoint의 직원 파일에 수동 또는 자동으로게시되고 적용됩니다.

  - Workday와 같은 HR 관리 시스템은 Microsoft Flow와 함께 정기적으로 실행되어 직원 파일을 관리할 수 있습니다.

  - 직원이 조직을 떠난 경우 Flow는 특정 직원의 파일에 대한 보존 시계를 시작할 M365 이벤트 기반 보존 REST API를 트리거합니다.

#### <a name="using-microsoft-flow"></a>Microsoft Flow 사용

1단계- Flow를 생성하여 Microsoft 365 REST API를 사용하는 이벤트를 만듭니다.

![Flow를 사용해 이벤트 만들기](media/automate-event-driven-retention-flow-1.png)

![Flow를 사용해 REST API 호출하기](media/automate-event-driven-retention-flow-2.png)

##### <a name="create-an-event"></a>이벤트 만들기

REST API를 호출하는 샘플 코드

<table>
<thead>
<tr class="header">
<th>메서드</th>
<th>POST</th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>URL</td>
<td>https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent)</td>
<td></td>
</tr>
<tr class="even">
<td>머리글</td>
<td>Content-Type</td>
<td>application/atom+xml</td>
</tr>
<tr class="odd">
<td>본문</td>
<td><p>&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</p>
<p>&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</p>
<p>xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</p>
<p>xmlns='http://www.w3.org/2005/Atom'&gt;</p>
<p>&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</p>
<p>&lt;updated&gt;9/9/2017 10:50:00 PM&lt;/updated&gt;</p>
<p>&lt;content type='application/xml'&gt;</p>
<p>&lt;m:properties&gt;</p>
<p>&lt;d:Name&gt;Employee Termination &lt;/d:Name&gt;</p>
<p>&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</p>
<p>&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</p>
<p>&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</p>
<p>&lt;/m:properties&gt;</p>
<p>&lt;/content&gt;</p>
<p>&lt;/entry&gt;</p></td>
<td></td>
</tr>
<tr class="even">
<td>인증</td>
<td>기본</td>
<td></td>
</tr>
<tr class="odd">
<td>사용자 이름</td>
<td>“Complianceuser”</td>
<td></td>
</tr>
<tr class="even">
<td>암호</td>
<td>“Compliancepassword”</td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="available-parameters"></a>사용 가능한 매개 변수

<table>
<thead>
<tr class="header">
<th><strong>매개 변수</strong></th>
<th><strong>설명</strong></th>
<th><strong>참고</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&lt;d:Name&gt;&lt;/d:Name&gt;</td>
<td>이벤트에 대해 고유한 이름을 제공하고,</td>
<td>후행 공백 및 다음 문자를 사용할 수 없습니다. % *\&amp; &lt; &gt; | # ? , : ;</td>
</tr>
<tr class="even">
<td>&lt;d:EventType&gt;&lt;/d:EventType&gt;</td>
<td>이벤트 유형 이름(또는 Guid)을 입력합니다.</td>
<td>예제: "직원 고용 계약 완료". 이벤트 유형은 보존 레이블과 관련되어야 합니다.</td>
</tr>
<tr class="odd">
<td>&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</td>
<td>“ComplianceAssetId:”와 직원 Id를 입력합니다.</td>
<td>예제:&quot;ComplianceAssetId:12345&quot;</td>
</tr>
<tr class="even">
<td>&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</td>
<td>이벤트 날짜 및 시간</td>
<td><p>형식: yyyy-MM-ddTHH:mm:ssZ, 예제:</p>
<p>2018-12-01T00:00:00Z</p></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a>응답코드

| **응답 코드** | **설명**       |
| ----------------- | --------------------- |
| 302               | 리디렉션              |
| 201               | 만든 날짜               |
| 403               | 인증 실패  |
| 401               | 인증 실패 |

##### <a name="get-events-based-on-time-range"></a>이벤트를 시간 범위를 기준으로 설정

<table>
<thead>
<tr class="header">
<th>메서드</th>
<th>GET</th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>URL</td>
<td><ol start="4" type="1">
<li><p>https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</p></li>
</ol></td>
<td></td>
</tr>
<tr class="even">
<td>머리글</td>
<td>Content-Type</td>
<td>application/atom+xml</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>인증</td>
<td>기본</td>
<td></td>
</tr>
<tr class="odd">
<td>사용자 이름</td>
<td>“Complianceuser”</td>
<td></td>
</tr>
<tr class="even">
<td>암호</td>
<td>“Compliancepassword”</td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a>응답코드

| **응답 코드** | **설명**                   |
| ----------------- | --------------------------------- |
| 200               | 확인, atom + xml의 이벤트 목록 |
| 404               | 찾을 수 없음                         |
| 302               | 리디렉션                          |
| 401               | 인증 실패              |
| 403               | 인증 실패             |

##### <a name="get-an-event-by-id"></a>이벤트 ID로 가져오기

| 메서드         | GET   |                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------- |
| URL            | [https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\)) |                      |
| Header         | Content-Type                                                                                                                                                                                                                                                       | application/atom+xml |
| 인증 | 기본                                                                                                                                                                                                                                                              |                      |
| 사용자 이름       | “Complianceuser”                                                                                                                                                                                                                                                   |                      |
| 암호       | “Compliancepassword”                                                                                                                                                                                                                                               |                      |

##### <a name="response-codes"></a>응답코드

| **응답 코드** | **설명**                                      |
| ----------------- | ---------------------------------------------------- |
| 200               | 확인, 응답 본문에 atom + xml 이벤트가 포함되어 있습니다. |
| 404               | 찾을 수 없음                                            |
| 302               | 리디렉션                                             |
| 401               | 인증 실패                                 |
| 403               | 인증 실패                                |

##### <a name="get-an-event-by-name"></a>이벤트 이름으로 받기

| 메서드         | GET       |                      |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| URL            | <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('EventByRESTPost-2226bfebcc2841a8968ba71f9516b763')> |                      |
| 머리글        | Content-Type                                                                                                                                 | application/atom+xml |
| 인증 | 기본                                                                                                                                        |                      |
| 사용자 이름       | “Complianceuser”                                                                                                                             |                      |
| 암호       | “Compliancepassword”                                                                                                                         |                      |

##### <a name="response-codes"></a>응답코드

| **응답 코드** | **설명**                                      |
| ----------------- | ---------------------------------------------------- |
| 200               | 확인, 응답 본문에 atom + xml 이벤트가 포함되어 있습니다. |
| 404               | 찾을 수 없음                                            |
| 302               | 리디렉션                                             |
| 401               | 인증 실패                                 |
| 403               | 인증 실패                                |

#### <a name="using-powershell-ver6-or-higher-or-any-http-client"></a>PowerShell(ver.6 이상) 또는 HTTP 클라이언트 사용

1단계: PowerShell에 연결합니다.

2단계: 다음 스크립트를 실행합니다.

<table>
<tbody>
<tr class="odd">
<td><p>param([string]$baseUri)</p>
<p>$userName = &quot;UserName&quot;</p>
<p>$password = &quot;Password&quot;</p>
<p>$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</p>
<p>$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</p>
<p>$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</p>
<p>호스트 쓰기 &quot;시작하여 다음의 이름으로 이벤트 생성: $EventName&quot;</p>
<p>$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</p>
<p>&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</p>
<p>xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</p>
<p>xmlns='http://www.w3.org/2005/Atom'&gt;</p>
<p>&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</p>
<p>&lt;updated&gt;7/14/2017 2:03:36 PM&lt;/updated&gt;</p>
<p>&lt;content type='application/xml'&gt;</p>
<p>&lt;m:properties&gt;</p>
<p>&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</p>
<p>&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</p>
<p>&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</p>
<p>&lt;/m:properties&gt;</p>
<p>&lt;/content&gt;</p>
<p>&lt;/entry&gt;&quot;</p>
<p>$event = $null</p>
<p>시도</p>
<p>{</p>
<p>$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri &quot;$baseUri/ComplianceRetentionEvent&quot; -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</p>
<p>}</p>
<p>catch</p>
<p>{</p>
<p>$response = $_.Exception.Response</p>
<p>if($response.StatusCode -eq &quot;Redirect&quot;)</p>
<p>{</p>
<p>$url = $response.Headers.Location</p>
<p>Write-Host &quot;redirected to $url&quot;</p>
<p>$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri $url -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</p>
<p>}</p>
<p>}</p>
<p>$event | fl *</p></td>
</tr>
</tbody>
</table>

#### <a name="verify-the-outcome-in-both-options"></a>두 옵션 모두에서 결과 확인하기

1단계: 보안 및 준수 센터로 이동합니다.

2 단계 : 데이터 거버넌스에서 이벤트를 클릭합니다.

3 단계: 이벤트를 생성되었는지 확인합니다.

마찬가지로 이벤트 기반 보존을 자동화하는 위의 옵션을 다음 시나리오에도 사용할 수 있습니다.

### <a name="scenario-2-contracts-expiring"></a>시나리오 2: 계약 만료

조직은 고객, 공급 업체 및 파트너와의 단일 계약에 대해 여러 레코드를 보유할 수 있습니다. 이러한 문서는 SharePoint와 같은 문서 라이브러리에있을 수 있습니다. 장기 구매 계약이 끝나면 계약과 연관된 문서의 보존 기간이 시작됩니다. 예를 들어 계약과 관련된 모든 기록은 계약이 만료된 때로부터 5년간 보관해야합니다. 5 년 보존 기간을 트리거시키는 이벤트는 계약기간 만료입니다.

CRM(고객 관계 관리) 시스템은 Microsoft 365와 함께 작동하고 계약 문서의 보존을 트리거 할 수 있습니다.

**이 시나리오에 대한 자동 이벤트 기반 보유 구성:**

![계약 만료 시나리오에 대한 역할 및 작업 다이어그램](media/automate-event-driven-retention-contract-expiration.png)

  - 관리자는 각 계약 유형별로 다양한 폴더가 있는 SharePoint 라이브러리를 만듭니다.

  - 관리자는 라이센스 계약, 개발 계약과 같은 계약 파일을 각 계약 폴더에 추가합니다.

  - 관리자는 각 계약 폴더에 자산 Id를 할당합니다.

  - SCC 관리자는 보안 및 준수 센터로 로그인합니다.

  - SCC 관리자가 “계약 생성”, “계약 만료” 등과 같은 계약 관련 이벤트 유형을 만듭니다.

  - SCC 관리자가 “계약 만료” 레이블을 만듭니다.

  - 이 "계약 만료 " 레이블은 SharePoint의 계약 파일에 수동 또는 자동으로 게시되고 적용됩니다.

  - 계약 관리 시스템은 Microsoft Flow 또는 이와 유사한 응용 프로그램과 함께 정기적으로 실행되어 계약 파일을 관리할 수 있습니다.

  - 계약이 만료되면 Microsoft Flow는 M365 이벤트 기반 보존 REST API를 트리거하여 특정 계약의 파일에 대한 보존 시계를 시작합니다.

### <a name="scenario-3-end-of-product-manufacturing"></a>시나리오 3: 제품 제조 종료

제품 라인을 다르게 생산하는 제조 회사는 많은 종류의 제조 사양 및 가격 책정 문서를 작성합니다. 제품이 더 이상 제조되지 않게 되면 이 제품과 관련된 모든 사양 및 문서를 제품 수명 만료 후 일정한 기간 동안 보존해야 합니다.

ERP(Enterprise Resource Planning) 시스템은 Microsoft 365 및 Microsoft Flow와 함께 사용해 보존을 트리거할 수 있습니다.

**이 시나리오에 대한 이벤트 기반 자동 보존 구성하기:**

![제품 수명 주기 시나리오에 대한 역할 및 작업 다이어그램](media/automate-event-driven-retention-product-lifecycle-expiration.png)

  - 관리자는 제품 1, 제품 2 등과 같이 문서 집합에 제품 폴더를 만듭니다.

  - 관리자는 제조 사양, 제품 가격, 제품 라이센스와 같은 제품 파일을 각 제품 폴더에 추가합니다.

  - 관리자는 각 제품폴더에 자산 Id를 할당합니다.

  - SCC 관리자는 보안 및 준수 센터로 로그인합니다.

  - SCC 관리자가 “제품 제조 시작”, “제품 제조 종료”와 같은 직원 관련 이벤트 유형을 만듭니다.

  - SCC 관리자가 “제품 제조 종료” 레이블을 만듭니다.

  - 이 "제품 제조 종료" 레이블은 SharePoint의 제품 파일에 수동 또는 자동으로 게시되고 적용됩니다.

  - ERP 시스템은 Microsoft Flow 또는 이와 유사한 응용 프로그램과 함께 정기적으로 실행되어 제품 파일을 관리할 수 있습니다.

  - 제품 제조가 끝나면 Microsoft Flow는 M365 이벤트 기반 보존 REST API를 트리거하여 특정 제품의 파일에 대한 보존 시계를 시작합니다.

## <a name="appendix"></a>부록

### <a name="using-redirect-302-response-results-to-call-the-rest-api"></a>Redirect 302 응답 결과를 이용하여 REST API 호출

1.  REST API URL <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent>을 사용하여 POST 보존 이벤트 호출 호출 (전역 관리자 권한 필요)

2.  응답 코드를 확인하십시오. URL이 302인 경우 응답 헤더의 위치 속성에서 리디렉션 된 URL을 가져옵니다.

3.  리디렉션된 URL을 사용하여 POST 보존 이벤트 호출을 다시 호출하십시오.

## <a name="credits"></a>크레딧

이 주제의 검토자:

Antonio Maio<br/>Microsoft Office 앱 및 서비스 MVP<br/> Antonio.Maio@Protiviti.com
