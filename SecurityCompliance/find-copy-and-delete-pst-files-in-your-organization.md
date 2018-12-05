---
title: PST 컬렉션 도구를 사용 하 여 찾기, 복사 및 조직에서 PST 파일을 삭제 하려면
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 7a150c84-049c-4a9c-8c91-22355b35f2a7
description: Microsoft PST 컬렉션 도구를 사용 하 여 조직의 네트워크를 검색 하는 조직 전체에 걸쳐 분산 된 PST 파일의 인벤토리를 가져옵니다. PST 파일을 찾은 후에 Office 365로 가져올 수 있도록 하는 중앙 위치에 복사 하는 PST 컬렉션 도구를 사용할 수 있습니다.
ms.openlocfilehash: 34395eee7776d8bff1ddccb7fed5b683e97c02c7
ms.sourcegitcommit: c59a082dca6593d0e35e58124ee6ba240547bfa5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2018
ms.locfileid: "27154214"
---
# <a name="use-the-pst-collection-tool-to-find-copy-and-delete-pst-files-in-your-organization"></a>PST 컬렉션 도구를 사용 하 여 찾기, 복사 및 조직에서 PST 파일을 삭제 하려면

> [!IMPORTANT]
> 이 문서에서 설명 하는 PST 컬렉션 도구는 Microsoft 표준 지원 프로그램이 나 서비스에서 지원 되지 않습니다. 이 도구는 어떠한 보증도 없이 있는 그대로 제공 됩니다. Microsoft 추가로 포함 하 여, 제한 되지 않고 하는 모든 묵시적된 보증을 부인 묵시적 보증 상품성 또는 특정 목적에의 적합성입니다. 사용 또는 성능 도구 및 설명서에 발생 하는 위험은 있습니다. 어떠한 이벤트에 Microsoft, 해당 작성자 또는 다른 만들기, 제작, 또는 도구의 배달에 참여 하는 모든 책임을 지지 모든 손해에 대해 (포함 하 되, 제한 되지 않고 비즈니스 이익, 영업 중단, 손실 손실에 대 한 손해 비즈니스 정보 또는 기타 금전적 손실을) Microsoft가 그와 같은 손해의 가능성을 사전에 알고 있었던 경우에 사용 또는 설명서를 확인 하는 도구를 사용 하 여 원인으로 발생 합니다.

Microsoft PST 컬렉션 도구를 사용 하 여 PST 파일에 대 한 조직의 네트워크에서 검색할 수 있습니다. 이 도구를 사용 하면 조직 전체에 걸쳐 분산 되어 PST 파일의 인벤토리를 가져올 수 있습니다. PST 파일을 찾은 후에 중앙 위치에서 복사할 PST 컬렉션 도구를 사용할 수 있습니다. Pst 한 곳에 있는 다음 가져올 수 있도록 Exchange Online 사서함 (또는 단일 Exchange Online 사서함) 수는 다양 한 Office 365의 규정 준수 기능 집합이 다음 적용할 수 있습니다. 사용자의 사서함에 eDiscovery를 사용 하 여 메시지를 보관 eDiscovery 검색 도구를 사용 하 여 가져온 PST 파일에서 특정 메시지에 대 한 검색을 포함 하 고 보관 및 Office 365 보존 정책에서 pst로 가져오기 (영문) 및 수명 관리 주기는 메시징를 사용 하 여 이러한 메시지의 레코드 관리 기능 Exchange 온라인 합니다. 확신할 수 없을 때는 사용자가 수집한 PST 파일을 Office 365 성공적으로 끝나면 되었는지, 후 네트워크에서의 원래 위치에서 삭제 하는 도구를 사용할 수 있습니다. 
  
PST 컬렉션 도구를 사용 하 여 할 수 있는 다른 작업은 사용자가 새 PST 파일을 만들고 하다 고 생각 네트워크에서 기존 PST 파일을 변경 하지 못하도록 합니다. 이러한 "블록" 기능을 사용 하면 찾기를 수집 하 고 PST 파일의 알려진된 집합을 Office 365 가져오고 조직에서 PST 파일의 미래 확산 방지 수 있습니다. 
  
## <a name="how-the-pst-collection-tool-works"></a>PST 컬렉션 도구 작동 하는 방법

PST 컬렉션 도구를 사용 하 여 찾기, 제어, 수집 및 조직에서 PST 파일을 삭제 하는 프로세스에 대 한 빠른 개요는 다음과 같습니다.
  
![PST 컬렉션 도구 프로세스 개요](media/67a29f27-f83c-4f0a-9df4-7ed92d3086fe.png)
  
1. **[1 단계: 네트워크에서 PST 파일을 찾을](#step-1-find-pst-files-on-your-network)** -클라이언트 및 서버 컴퓨터에 대 한 Active Directory 개체를 포함 하는 조직 구성 단위와 같은 위치를 지정 하면 PST 파일을 찾는데 도구를 실행 하는 경우. 특정 컴퓨터 또는 네트워크 파일 공유를 검색할 수도 있습니다. 이 도구를 실행 하면 "경량" 컬렉션 에이전트 대상 컴퓨터에 설치 됩니다. 이 에이전트는 PST 파일에 대 한 대상 컴퓨터를 검색 하 고 발견 PST 파일에 대 한 PST 컬렉션 도구를 다시 정보를 보냅니다. 이 도구는 지정 된 위치에서 발견 된 PST 파일에 대 한 정보를 포함 하는 로그 파일을 만듭니다. 이러한 파일은 이후 단계에서 도구를 실행 하는 경우 사용 됩니다. 
    
2. **[(선택 사항) 2 단계: PST 파일에 대 한 액세스를 제어](#optional-step-2-control-access-to-pst-files)** -도구는 사용자가 만들거나 PST 파일을 변경 하지 못하도록 하는 설정을 사용 하 여 그룹 정책 개체 (GPO)를 만듭니다. 이 GPO가 사용자 도메인의 모든 사용자에 게 적용 됩니다. 이 단계를 사용 하면 "잠그는" 수집, 가져오기 및 새 PST 파일 작성 하지 않고도 삭제할 수 있도록 1 단계에서에서 발견 된 PST 파일 또는 변경 된 기존 PST 파일 수 있습니다. 
    
3. **[3 단계: 컬렉션 위치로 PST 파일에 복사](#step-3-copy-the-pst-files-to-a-collection-location)** -4 단계에서에서 Office 365를 가져올 서비스를 사용 하 여 Exchange Online 사서함으로 가져올 수 있습니다를 한 위치에 PST 파일을 수집 수 있습니다. "수집" 모드에서 도구를 실행 하는 경우 각 컬렉션 에이전트는 에이전트 컬렉션 위치에 설치 된 대상 컴퓨터에서 PST 파일을 복사 합니다. 
    
4. **[4 단계: Office 365로 PST 파일을 가져오는](#step-4-import-the-pst-files-to-office-365)** -Exchange Online 사서함으로 가져오려면 준비가 복사한 후 PST 파일을 한곳에 표시 합니다. 
    
5. **[5 단계: PST 파일을 네트워크에서 찾을 삭제](#step-5-delete-the-pst-files-found-on-your-network)** -후 PST 파일을 발견 하 고 수집 가져왔는지 Office 365의 Exchange Online 사서함으로, 원래 위치에서 PST 파일을 삭제 하려면 PST 컬렉션 도구를 사용할 수 있는 자신이 1 단계에서에서 발견 되었습니다. 

## <a name="before-you-begin"></a>시작하기 전에

- 로컬 컴퓨터에 PST 컬렉션 도구를 다운로드 하려면 다음이 단계를 수행 합니다. 
    
    1. [PST 컬렉션 도구를 다운로드](https://aka.ms/pstcollectiontool)합니다.
    
    2. 팝업 창에서 **저장** 을 클릭 \> 로컬 컴퓨터의 폴더에 PSTCollectionTool.zip 파일을 저장 하려면 **로 저장** 합니다. 
    
    3. 로컬 컴퓨터의 폴더에 PSTCollectionTool.zip 파일을 추출 기본 폴더 이름은 PSTCollectionTool입니다.
    
- (찾기, 차단, 복사 또는 삭제) 모드에서 PST 컬렉션 도구를 실행 하려면 Active Directory 도메인에서 Domain Administrators 그룹의 구성원 이어야 해야 합니다. 

## <a name="step-1-find-pst-files-on-your-network"></a>1 단계: 네트워크에서 PST 파일 찾기

첫번째 단계 PST 컬렉션 도구를 사용 하면 조직에서 PST 파일을 실행 하는 것입니다. 다음과 같은 종류의 위치를 검색 하는 도구를 사용할 수 있습니다. 
  
- 온-프레미스 Active Directory 도메인에 조직 구성 단위 (Ou). 지정 된 OU에 포함 된 모든 컴퓨터를 검색 하는 도구입니다. 
    
- 클라이언트 및 서버 컴퓨터입니다. 이 도구는 지정 된 컴퓨터를 검색합니다. 
    
- 네트워크 파일 공유 합니다. 지정 된 네트워크 파일 공유를 검색 하는 도구입니다. 
    
에 대 한 설명을 참조는 `Locations` 각 이러한 위치 유형에 대해 사용 하 여 구문의 예제를 보려면 다음 절차에는 테이블의 매개 변수입니다. 
  
> [!IMPORTANT]
> 실행 찾기 모드에서 PST 컬렉션 도구 전에 해야 차단, 수집 하 고, 또는 PST 파일을 삭제 하는 등의 다른 작업을 수행할 수 있습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트 (관리자 권한으로 실행)를 엽니다.
    
2. PSTCollectionTool 폴더 (또는 PSTCollectionTool.zip 파일을 추출한 폴더)로 이동 합니다.
    
3. DataCollectorMaster 디렉터리로 변경 합니다.
    
4. 지정된 된 위치에서 PST 파일을 찾으려면 다음 명령을 실행 합니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName <Name> -Locations <Locations to search for PSTs> -LogLocation <Location to store log files> -ConfigurationLocation <Location to store configuration files>
    ```

    다음 표에서 PST 파일을 찾는데 DataCollectorMaster.exe 명령을 실행할 때 매개 변수 및 해당 필수 값을 설명 합니다. 
    
    |매개 변수 * * *|****Description****|예 * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |검색할 데이터 유형을 지정 합니다. 현재, PST 파일을 검색 하는 PST 컬렉션 도구를 사용할 수 있습니다.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |이 도구는 수행 하는 작업의 종류를 지정 합니다. 값을 사용 하 여 `Find` 지정 된 위치에서 PST 파일을 찾습니다. Note 도구 찾기 하 고 Outlook 프로필에 연결 된 Outlook 및 PST 파일에 열려 있는 PST 파일에 대 한 정보를 얻을 수 있습니다.<br/> | `-Mode Find` <br/> |
    | `JobName` <br/> |PST 컬렉션 작업의 이름을 지정합니다. 차단, 수집 및 PST 파일을 찾는데 도구를 실행할 때 발견 되는 PST 파일을 삭제 하려면 PST 컬렉션 도구를 실행할 때이 같은 작업 이름을 사용 합니다. 작업 이름은 로그 및 구성 파일 이름에도 추가 됩니다.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> | PST 파일을 검색 하려면 하나 이상의 위치를 지정 합니다. 둘 이상의 위치를 지정 하는 경우 개별 위치를 구분 하려면 세미콜론 (;)를 사용 합니다. 주위에 큰따옴표 함께이 매개 변수는 개별 값을 확인 ("").<br/><br/>   다음은 검색할 수 있는 위치 유형에 대 한 필수 identity 값 형식입니다.  <br/><br/>        **Ou** -Ou 행위를 식별 하는 DN (고유 이름) 사용 예를 들어:`"OU=NorthAmerica,OU=NWRegion,OU=ITServices,DC=contoso,DC=com"` <br/> > [!IMPORTANT]> 기본 제공 컴퓨터 컨테이너를 지정할 수 없습니다 있습니다 (예: CN 컴퓨터, DC = = contoso, DC = com ") 조직 구성 단위 수 있으므로 합니다.<br/> <br/> **컴퓨터** -; 네트워크에서 클라이언트와 서버 컴퓨터를 식별 하는 DN 사용 또는 정규화 된 도메인 이름 (FQDN) 예를 들어:  <br/>  DN:`"CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"` <br/>  또는  <br/>  FQDN:`"FILESERVER01.contoso.com"` <br/><br/>  **네트워크 파일 공유** -네트워크 파일 공유;를 식별 하는 UNC 이름 사용 예를 들어`"\\FILESERVER02\Users"` <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `LogLocation` <br/> |로그 파일에 복사 되는 폴더를 지정 합니다. 폴더가 존재 하지 않는 경우이 도구를 실행할 때 만들어집니다.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ConfigurationLocation` <br/> |.Xml 구성 파일에 복사 되는 폴더를 지정 합니다. 이 파일의 도구를 실행할 때 발견 되는 각 PST 파일에 대 한 정보를 포함 합니다. 이 파일은 발견 되는 PST 파일을 복사 하려면 3 단계에서에서 도구를 실행 하는 경우에 사용 됩니다.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `ExcludedLocations` <br/> |이 선택적 매개 변수는 찾기 작업 하는 동안 건너뛸 위치를 지정 합니다. 특정 Ou, 컴퓨터 및 네트워크 파일 공유를 제외할 수 있습니다. 예: SQL server (또는 다른 종류의 응용 프로그램 서버)로 구성 된 컴퓨터와 같은 컴퓨터를 제외할 수, 사용자가 액세스할 수 없습니다. 제외할 둘 이상의 위치를 지정 하는 경우 개별 위치를 구분 하려면 세미콜론 (;)를 사용 합니다. 주위에 큰따옴표 함께이 매개 변수는 개별 값을 확인 ("").  <br/> | `-ExcludedLocations "SQLSERVER01.contoso.com"` <br/> |
    | `ForceRestart` <br/> |선택적이 스위치를 사용 하면 기존 PST 컬렉션 작업에 대 한 찾기 모드에서 도구를 실행할 수 있습니다. 사용 하는 경우는 `ForceRestart` 전환, 이전 찾기 작업에서 결과 대 한 작업이 무시 됩니다.이 도구를 다시 지정 된 위치를 검색 하 고 새 로그 및 구성 파일을 만듭니다.<br/> | `-ForceRestart` <br/> |
   
    실제 값을 사용 하 여 각 매개 변수에 대 한 DataCollectorMaster.exe 명령에 대 한 구문의 예는 다음과 같습니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -LogLocation "c:\users\admin\desktop\PSTCollection" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"
    ```

    명령을 실행 하면 지정 된 위치에서 PST 파일을 찾아의 진행률을 표시 하는 자세한 상태 메시지가 표시 됩니다. 잠시 후 최종 상태 메시지를 발견 된 PST 파일의 총 수, 작업이 완료 되었는지 여부 및 모든 오류 마치를 표시 합니다. 동일한 상태 메시지는.log 파일에 복사 됩니다.
    
### <a name="results-of-running-datacollectormasterexe-in-the-find-mode"></a>DataCollectorMaster.exe 찾기 모드에서 실행 한 결과

다음 파일이 생성 되 고 변수로 지정한 폴더에 저장 된 PST 컬렉션 도구 찾기 모드 성공적으로 실행을 하 고 나면는 `LogLocation` 및 `ConfigurationLocation` 매개 변수입니다. 
  
- **\<작업 이름\>_찾기_\<DateTimeStamp\>.log** -로그 파일 표시 되었던 상태 메시지를 포함 합니다. 이 파일은 지정 된 폴더에 만들어집니다는 `LogLocation` 매개 변수입니다. 
    
- **\<작업 이름\>_찾기_\<DateTimeStamp\>.csv** -는 CSV 파일을 찾을 수 있는 각 PST 파일에 대 한 행을 포함 합니다. 각 PST에 대 한 정보를 PST 파일을 찾지, PST 파일의 전체 파일 경로 위치, PST 파일과 크기 (kb) PST 파일의 소유자는 컴퓨터를 포함 합니다. 이 파일은 지정 된 폴더에 만들어집니다는 `LogLocation` 매개 변수입니다. 
    
    > [!TIP]
    > Excel에서 자동 합계 도구를 사용 하 여 CSV 파일에 나열 된 모든 PST 파일의 (KB)의 총 크기를 계산 합니다. 그런 다음 전체 크기 (mb) 또는 기가바이트 (GB)를 변환 하려면 변환 계산기를 사용할 수 있습니다. 
  
- **\<작업 이름\>_찾기_\<DateTimeStamp\>.xml** -에 대 한 정보를 포함 하는 XML 파일 찾기 모드에서 도구를 실행 하는 경우를 사용 하는 매개 변수는 값입니다. 또한이 파일을 찾을 수 있는 모든 PST 파일에 대 한 정보를 포함 합니다. 이 파일의에서 데이터를 수집, block, 작업 같은 대 한 도구를 다시 실행 또는 발견 된 삭제 PST 파일을 실행 하는 경우에 사용 됩니다. 이 파일은 지정 된 폴더에 만들어집니다는 `ConfigurationLocation` 매개 변수입니다. 
    
    > [!IMPORTANT]
    > 하지 이름바꾸기 되, 변경 또는이 파일을 이동 합니다. 블록, 복사, 도구를 다시 실행 하거나 동일한 작업에 대 한 모드를 삭제할 때 PST 컬렉션 도구에서 사용 됩니다. 

## <a name="optional-step-2-control-access-to-pst-files"></a>(선택 사항) 2 단계: PST 파일에 대 한 액세스를 제어 합니다.

이 단계를 사용 하면 "잠그는" 수집할 수 있도록 1 단계에서에서 발견 된 PST 파일 및 Office 365에 알려진된 집합이 PST 파일을 가져올 수 있습니다. 블록 모드에서 PST 수집 도구를 실행 하는 경우에 다음 작업이 수행 됩니다. 
  
- 도구는 그룹 정책 개체 (GPO) 라는 *PST 사용 현황 컨트롤* 을 만듭니다. 이 GPO 사용자의 도메인에 연결 하 고 조직에서 모든 인증 된 사용자에 게 적용 합니다. 
    
- PST 사용 현황 컨트롤 GPO 조직에는 컴퓨터에서 레지스트리 설정을 만듭니다. 사용 하는 매개 변수에 따라 사용자가 새 PST 파일을 만들지 못하도록 하려면 레지스트리 설정 및 사용자가 기존 PST 파일을 변경 하지 못하게 하는 레지스트리 설정을 만들 수 있습니다.
    
> [!NOTE]
> PST 파일에 대 한 액세스 제어를 조직에 대 한 너무 손상 된 경우에 중앙 위치에 PST 파일을 복사 하려면 3 단계를 수행 하 고이 단계를 건너뜁니다를 고려할 수 있습니다. 1 단계를 반복 하 여 동일한 작업에 대 한 다음 (을 사용 하 여는 `ForceRestart` 매개 변수) 컬렉션 위치로 Pst 파일을 복사한 후 만들어진 추가 Pst 파일을 찾을 수 있습니다. 새 PST 파일 발견 되 면 컬렉션 위치로 복사할 수 있습니다. 사용 하는 경우는 `ForceRestart` 찾기 모드에서 도구를 다시 실행 하 고 결과 작업에 대 한 이전 찾기 작업에서 무시 됩니다.이 도구는 지정 된 위치를 검색 다시 때 매개 변수입니다. 

PST 파일에 대 한 액세스를 차단 합니다.

1. 로컬 컴퓨터에서 명령 프롬프트 (관리자 권한으로 실행)를 엽니다.
    
2. PST 컬렉션 도구를 다운로드 한 디렉터리로 이동 합니다.
    
3. 1 단계에서에서 찾은 PST 파일에 대 한 액세스를 차단 하려면 다음 명령을 실행 합니다.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -BlockChangesToFiles -BlockNewFiles
    ```

    다음 표에서 작성 하 고 PST 파일의 변경 차단 하도록 DataCollectorMaster.exe 명령을 실행할 때 매개 변수 및 해당 필수 값을 설명 합니다. 
    
    |매개 변수 * * *|****Description****|예 * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |검색할 데이터 유형을 지정 합니다. 현재, PST 파일을 검색 하는 PST 컬렉션 도구를 사용할 수 있습니다.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |이 도구는 수행 하는 작업의 종류를 지정 합니다. 값을 사용 하 여 `Block` 사용자가 새 PST 파일을 만들고 기존 PST 파일에 변경 작업을 수행 하지 못하도록 합니다.<br/> | `-Mode Block` <br/> |
    | `JobName` <br/> |기존 PST 컬렉션 작업의 이름을 지정합니다. 1 단계에서에서 Find 모드에서 도구를 실행 했을 때 사용 되는 것이 같은 작업 이름을 사용 해야 합니다. 이 작업 이름은 블록 모드에서 도구를 실행할 때 만들어지는 로그 파일의 이름에도 추가 됩니다.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |Find 모드에서 도구를 실행 했을 때 만들어진.xml 구성 파일을 포함 하는 폴더를 지정 합니다. 1 단계에서에서이 매개 변수를 사용 하는 동일한 값을 사용 합니다.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |블록 작업에 대 한 로그 파일에 복사 되는 폴더를 지정 합니다. 선택적 매개 변수입니다. 이 포함 하지 않으면 로그 파일 PST 컬렉션 도구를 다운로드 한 폴더에 복사 됩니다. 로그 파일을 모두 같은 폴더에 저장 되도록 1 단계에서에서 Find 모드에서 도구를 실행 했을 때 사용한 동일한 로그 위치를 사용 하는 것이 좋습니다.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `BlockChangesToFiles` <br/> |이 스위치를 사용 하 여 사용자가 PST 파일을 변경 하지 못하도록 합니다. 다음 레지스트리 항목은 만든이 스위치를 사용 하는 경우: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\PST\PstDisableGrow` 데이터 값을 1로 설정 하 고 있습니다. 이 레지스트리 설정은 블록 모드에서 PST 컬렉션 도구를 실행할 때 생성 되는 GPO에서 조직에 있는 컴퓨터에 만들어집니다.<br/> | `-BlockChangesToFiles` <br/> |
    | `BlockNewFiles` <br/> |이 스위치를 사용 하 여 사용자가 새 PST 파일 만들기 (영문), 열기 및 outlook에서 PST 파일 가져오기 (영문) 및 Outlook에서 PST 파일 내보내기 (영문) 하지 못하도록 합니다. 다음 레지스트리 항목은 만든이 스위치를 사용 하는 경우: `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\DisablePst` 데이터 값을 1로 설정 하 고 있습니다. 이 레지스트리 설정은 블록 모드에서 PST 컬렉션 도구를 실행할 때 생성 되는 GPO에서 조직에 있는 컴퓨터에 만들어집니다.<br/> | `-BlockNewFiles` <br/> |
   
    실제 값을 사용 하 여 각 매개 변수에 대 한 DataCollectorMaster.exe 명령에 대 한 구문의 예는 다음과 같습니다.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection" -BlockChangesToFiles -BlockNewFiles
    ```
    
    차단할 새 PST 파일 또는 기존 PST 파일의 변경 내용을 확인 하 라는 메시지가 표시 됩니다. 계속 하려면 하 고 명령이 성공적으로 실행 하 여 확인 한 후 "PST 사용 현황 컨트롤" 이라는 새 GPO를 이미 만들었다고 없다는 메시지가 표시 됩니다.
    
## <a name="step-3-copy-the-pst-files-to-a-collection-location"></a>3 단계: 컬렉션 위치로 PST 파일에 복사

다음 단계는 복사 하는 PST 파일 찾기 모드에서 PST 컬렉션 도구를 실행 하기를 찾는 위치입니다. 이렇게 하면 Office 365를 나중에 가져올 수 있도록 한 위치에 PST 파일을 수집할 수 있습니다. PST 파일 컬렉션 위치를 복사 하기 전에 필요한 저장 공간의 총 크기를 결정 하는 것이 좋습니다. 모든 PST 파일의 총 크기를 계산 하려면 1 단계에서에서 만든 CSV 파일을 사용 하 여 수행할 수 있습니다.
  
> [!NOTE]
> Office 365로 가져온 PST 파일의 원래 위치에서 들을 삭제 했을 때 후에이 단계에서 복사한 수 있는 컬렉션 위치에서 끝점을 삭제 하는 것이 좋습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트 (관리자 권한으로 실행)를 엽니다.
    
2. PST 컬렉션 도구를 다운로드 한 디렉터리로 이동 합니다.
    
3. 지정한 위치에 PST 파일을 복사 하려면 다음 명령을 실행 합니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName <Name of job from Step 1> -Locations <same locations from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    다음 표에서 PST 파일을 복사 하려면 DataCollectorMaster.exe 명령을 실행할 때 매개 변수 및 해당 필수 값을 설명 합니다. 
    
    |매개 변수 * * *|****Description****|예 * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |검색할 데이터 유형을 지정 합니다. 현재, PST 파일을 검색 하는 PST 컬렉션 도구를 사용할 수 있습니다.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |이 도구는 수행 하는 작업의 종류를 지정 합니다. 값을 사용 하 여 `Collect` 찾기 모드에서 도구를 실행 하는 경우 발견 된 PST 파일을 복사 합니다. 이 도구는 Outlook에서 열려 있으며 Outlook 프로필에 연결 된 PST 파일을 복사 하는 PST 파일 수 복사는 note 합니다.<br/> | `-Mode Collect` <br/> |
    | `JobName` <br/> |기존 PST 컬렉션 작업의 이름을 지정합니다. 1 단계에서에서 Find 모드에서 도구를 실행 했을 때 사용 되는 것이 같은 작업 이름을 사용 해야 합니다. 이 작업 이름은 수집 모드에서 도구를 실행할 때 만들어지는 로그 파일의 이름에도 추가 됩니다.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> |에 사용 했던 동일한 값을 사용 하 여 `Locations` 1 단계에서에서 매개 변수입니다. 5 단계에서에서 원본 위치에서 PST 파일을 삭제 하는 도구를 다시 실행 하려는 경우에 도구 수집 모드에서 실행 하는 경우에이 매개 변수를 포함 한 합니다.<br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"; "CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `ConfigurationLocation` <br/> |Find 모드에서 도구를 실행 했을 때 만들어진.xml 구성 파일이 들어 있는 폴더를 지정 합니다. 1 단계에서에서이 매개 변수를 사용 하는 동일한 값을 사용 합니다.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop \PSTCollection\Configuration"` <br/> |
    | `CopyLocation` <br/> |PST 파일을 복사 하려면 컬렉션 위치를 지정 합니다. 파일 서버, 네트워크 파일 공유 또는 하드 드라이브에 파일을 복사할 수 있습니다. 위치는 수집 모드에서 도구를 실행 하기 전에 존재 해야 합니다. 이 도구는 위치를 생성 하지 않습니다 하며 존재 하지 않는 없다는 오류가 반환 됩니다.  <br/> 또한이 매개 변수에 의해 지정 된 컬렉션 위치에 쓰기 권한을 해야 합니다.  <br/> | `-CopyLocation "\\FILESERVER03\PSTs"` <br/> |
    | `LogLocation` <br/> |수집 모드에 대 한 로그 파일에 복사 되는 폴더를 지정 합니다. 선택적 매개 변수입니다. 이 포함 하지 않으면 로그 파일 PST 컬렉션 도구를 다운로드 한 폴더에 복사 됩니다. 로그 파일을 모두 같은 폴더에 저장 되도록 1 단계에서에서 Find 모드에서 도구를 실행 했을 때 사용한 동일한 로그 위치를 사용 하는 것이 좋습니다.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |선택적이 스위치를 사용 하면 기존 PST 컬렉션 작업에 대 한 컬렉션 모드에서 도구를 다시 실행 수 있습니다. 이전에 수집 모드에서 도구를 실행 하지만 다음 도구를 사용 하 여 찾기 모드에서 다시 실행 하는 경우는 `ForceRestart` 다시 PST 파일에 대 한 위치를 검사 하려면 전환, 컬렉션 모드에서 도구를 다시 실행 하 고 다시 않았던 경우 발견 PST 파일을 복사 하려면이 스위치를 사용할 수 있는 사용자 다시 위치를 검색 합니다. 사용 하는 경우는 `ForceRestart` 스위치는 도구 모음 모드로 이전 컬렉션 작업을 무시 하 고 처음부터 PST 파일에 복사 하려고 합니다.<br/> | `-ForceRestart` <br/> |
   
    각 매개 변수에 대 한 실제 값을 사용 하 여 DataCollectorMaster.exe 도구에 대 한 구문의 예는 다음과 같습니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -CopyLocation "\\FILESERVER03\PSTs" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```

    명령을 입력 한 후 1 단계에서에서 발견 된 PST 파일을 수집의 진행률을 표시 하는 자세한 상태 메시지가 표시 됩니다. 잠시 후 최종 상태 메시지는 모든 오류와 로그를 복사 하는 위치 마치 표시 합니다. 동일한 상태 메시지는.log 파일에 복사 됩니다.
    
### <a name="results-of-running-datacollectormasterexe-in-the-collect-mode"></a>DataCollectorMaster.exe 수집 모드에서 실행 한 결과

다음 파일이 생성 되 고 하 여 지정 된 폴더에 저장 된 수집 모드에서 DataCollectorMaster.exe을 성공적으로 실행한후는 `LogLocation` 및 `ConfigurationLocation` 매개 변수입니다. 
  
- **\<작업 이름\>_수집_\<DateTimeStamp\>.log** -로그 파일 표시 되었던 상태 메시지를 포함 합니다. 이 파일은 지정 된 폴더에 만들어집니다는 `LogLocation` 매개 변수입니다. 
    
- **\<작업 이름\>_수집_\<DateTimeStamp\>.xml** -를 사용 하 여 도구 수집 모드에서 실행 된 매개 변수 값에 대 한 정보를만 포함 하는 XML 파일입니다. 실행 하는 경우이 파일의 데이터에에서 사용 되는; PST 파일을 삭제 하는 DataCollectorMaster.exe 도구를 다시 실행 [5 단계를](#step-5-delete-the-pst-files-found-on-your-network)참조 하십시오.
    

## <a name="step-4-import-the-pst-files-to-office-365"></a>4 단계: Office 365에 PST 파일 가져오기

1 단계에서에서 찾은 PST 파일을 수집한 했을 때 한 후 Office 365에서 사서함으로 가져오려면 다음 단계가입니다. 가져오기 프로세스 또는 일부로 가져오기 하려는 각 PST 파일의 행이 포함 된 CSV 매핑 파일을 만들기 위해 해야 합니다. 각 행의 정보 사용자의 전자 메일 주소, PST 파일의 이름을 지정 하 고 사용자에 게 PST 파일을 가져올 것인지 여부의 기본 또는 사서함 보관 합니다. 에 대 한 정보를 사용 하는 **작업 이름\>_찾기_\<DateTimeStamp.csv** (단계에서 만든) 파일 1 CSV 매핑 파일을 만들 수 있도록 합니다. 
  
Office 365에 PST 파일을 가져오려면 단계별 지침은 다음 항목 중 하나를 참조 하십시오.
  
- [네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기](use-network-upload-to-import-pst-files.md)
    
- [드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md)
    

## <a name="step-5-delete-the-pst-files-found-on-your-network"></a>네트워크에 있는 PST 파일을 삭제 하는 5 단계:

Office 365의 Exchange Online 사서함을 발견 하 고 수집 하는 PST 파일을 가져온 후에 1 단계에서에서 발견 된 원래 원본 위치에서 PST 파일을 삭제 하는 PST 컬렉션 도구를 사용할 수 있습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트 (관리자 권한으로 실행)를 엽니다.
    
2. PST 컬렉션 도구를 다운로드 한 디렉터리로 이동 합니다.
    
3. PST 파일을 삭제 하려면 다음 명령을 실행 합니다.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    다음 표에서 PST 파일을 삭제 하려면 DataCollectorMaster.exe 명령을 실행할 때 매개 변수 및 해당 필수 값을 설명 합니다. 
    
    |매개 변수 * * *|****Description****|예 * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |검색할 데이터 유형을 지정 합니다. 현재, PST 파일을 검색 하는 PST 컬렉션 도구를 사용할 수 있습니다. ![공백](media/b078d05c-3aee-4b9f-8805-6a8a9d8970ee.png)           <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |이 도구는 수행 하는 작업의 종류를 지정 합니다. 값을 사용 하 여 `Delete` 찾기 모드에서 도구를 실행 하는 경우 발견 된 PST 파일을 삭제 합니다.<br/> | `-Mode Delete` <br/> |
    | `JobName` <br/> |기존 PST 컬렉션 작업의 이름을 지정합니다. 찾기 모드와 1 단계 및 3 단계에서 수집 모드에서 도구를 실행 했을 때 사용 되는 것이 같은 작업 이름을 사용 해야 합니다. 이 작업 이름은 삭제 모드에서 도구를 실행할 때 만들어지는 로그 파일의 이름에도 추가 됩니다.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |수집 모드에서 도구를 실행 했을 때 만들어진.xml 구성 파일이 들어 있는 폴더를 지정 합니다. 3 단계에서에서이 매개 변수를 사용 하는 동일한 값을 사용 합니다.  <br/> | `-ConfigurationLocation "c:\users\admin\ desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |삭제 모드에 대 한 로그 파일에 복사 되는 폴더를 지정 합니다. 선택적 매개 변수입니다. 이 포함 하지 않으면 로그 파일 PST 컬렉션 도구를 다운로드 한 폴더에 복사 됩니다. 로그 파일을 모두 같은 폴더에 저장 되도록 찾기 및 1 단계 및 3 단계에서 수집 모드에서 도구를 실행 했을 때 사용한 동일한 로그 위치를 사용 하는 것이 좋습니다.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |선택적이 스위치를 사용 하면 기존 PST 컬렉션 작업에 대 한 삭제 모드에서 도구를 다시 실행 수 있습니다. 이전에 삭제 모드에서 도구를 실행 하지만 다음 도구를 사용 하 여 찾기 모드에서 다시 실행 하는 경우는 `ForceRestart` 다시 PST 파일에 대 한 위치를 검사 하려면 전환, 삭제 모드에서 도구를 다시 실행 하 고 않았던 경우 발견 PST 파일을 삭제 하려면이 스위치를 사용할 수 있는 프로그램 다시 sca nned 위치입니다. 사용 하는 경우는 `ForceRestart` 삭제 모드에서는 도구는 스위치 이전 삭제 작업을 무시 하 고 다시 PST 파일을 삭제 하려고 합니다.<br/> | `-ForceRestart` <br/> 

    각 매개 변수에 대 한 실제 값을 사용 하 여 DataCollectorMaster.exe 도구에 대 한 구문의 예는 다음과 같습니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```
   
    명령을 입력 한 후 1 단계에서에서 발견 하 고 3 단계에서에서 수집 된 PST 파일을 삭제 하는의 진행률을 표시 하는 자세한 상태 메시지가 표시 됩니다. 잠시 후 최종 상태 메시지는 모든 오류와 로그를 복사 하는 위치 마치 표시 합니다. 동일한 상태 메시지는.log 파일에 복사 됩니다.
    
### <a name="results-of-running-datacollectormasterexe-in-the-delete-mode"></a>DataCollectorMaster.exe 삭제 모드에서 실행 한 결과

다음 파일이 생성 되 고 지정 된 폴더에 저장 된 삭제 모드에서 DataCollectorMaster.exe을 성공적으로 실행한후는 `LogLocation` 및 `ConfigurationLocation` 매개 변수입니다. 
  
- **\<작업 이름\>_삭제_\<DateTimeStamp\>.log** -로그 파일 표시 되었던 상태 메시지를 포함 합니다. 이 파일은 지정 된 폴더에 만들어집니다는 `LogLocation` 매개 변수입니다. 
    
- **\<작업 이름\>_삭제_\<DateTimeStamp\>.xml** -를 사용 하 여 도구 삭제 모드에서 실행 된 매개 변수 값에 대 한 정보를만 포함 하는 XML 파일입니다. 또한 삭제 된 각 PST 파일의 이름과 파일 경로 나열 합니다. 이 파일은 지정 된 폴더에 만들어집니다는 `ConfigurationLocation` 매개 변수입니다. 
