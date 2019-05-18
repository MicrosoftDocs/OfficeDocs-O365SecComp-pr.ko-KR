---
title: PST 컬렉션 도구를 사용 하 여 조직의 PST 파일 찾기, 복사 및 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid: MOE150
ms.assetid: 7a150c84-049c-4a9c-8c91-22355b35f2a7
description: Microsoft PST 수집 도구를 사용 하 여 조직의 네트워크를 검색 하 여 조직 전체에 분산 된 PST 파일의 인벤토리를 가져옵니다. PST 파일을 찾은 후에는 PST 컬렉션 도구를 사용 하 여이를 중앙 위치에 복사 하 여 Office 365로 가져올 수 있습니다.
ms.openlocfilehash: 000da8aec988e85f935a96aabe9faa48932aaeaa
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152780"
---
# <a name="use-the-pst-collection-tool-to-find-copy-and-delete-pst-files-in-your-organization"></a>PST 컬렉션 도구를 사용 하 여 조직의 PST 파일 찾기, 복사 및 삭제

> [!IMPORTANT]
> 이 문서에서 설명 하는 PST 컬렉션 도구는 Microsoft standard 지원 프로그램 또는 서비스에서 지원 되지 않습니다. 이 도구는 모든 종류의 보증 없이 있는 그대로 제공 됩니다. Microsoft는 상품성 또는 특정 목적에 대 한 적합성에 대 한 묵시적 보증을 제한 없이 포함 하 여 모든 묵시적 보증을 배제 합니다. 도구 및 설명서의 사용 또는 성능에서 야기 되는 전체 위험은 그대로 유지 됩니다. Microsoft, 해당 작성자 또는 도구를 만드는 데 관여 된 모든 사용자에 게는 제한 (비즈니스 이익 손실에 대 한 손해, 비즈니스 중단, 손실 등)에 대 한 책임을 지지 않습니다. Microsoft에서 이러한 손해에 대 한 권고를 받은 경우에도, 도구 또는 설명서를 사용 하거나 사용 하지 못할 수 있는 비즈니스 정보 또는 기타 pecuniary 손실입니다.

Microsoft PST 수집 도구를 사용 하 여 조직의 네트워크에서 PST 파일을 검색할 수 있습니다. 이 도구를 사용 하 여 조직 전체에 분산 된 PST 파일의 인벤토리를 가져올 수 있습니다. PST 파일을 찾은 후에는 PST 모음 도구를 사용 하 여 중앙 위치에 복사할 수 있습니다. Pst를 한 위치에 두면 Exchange Online 사서함 (또는 단일 Exchange Online 사서함)으로 가져올 수 있으며,이 경우 Office 365에서 다양 한 준수 기능 집합을 적용할 수도 있습니다. 여기에는 Pst를 사용자의 보관 사서함으로 가져오기, eDiscovery 검색 도구를 사용 하 여 가져온 PST 파일의 특정 메시지 검색, eDiscovery 보류 및 Office 365 보존 정책을 사용 하 여 메시지 보존, 수명 관리 등이 포함 됩니다. Exchange Online의 메시징 레코드 관리 기능을 사용 하 여 이러한 메시지를 순환 합니다. 수집한 PST 파일을 Office 365로 성공적으로 가져왔는지 확신 하면이 도구를 사용 하 여 네트워크의 원래 위치에서 삭제할 수 있습니다. 
  
PST 컬렉션 도구를 사용 하면 사용자가 새 PST 파일을 만들고 네트워크에서 찾은 기존 PST 파일을 변경할 수 없게 됩니다. 이러한 "차단" 기능을 사용 하면 알려진 PST 파일 집합을 Office 365으로 찾고, 수집 하 고, 가져오고, 조직의 PST 파일을 향후에 확산 하지 않을 수 있습니다. 
  
## <a name="how-the-pst-collection-tool-works"></a>PST 컬렉션 도구의 작동 방식

다음은 PST 컬렉션 도구를 사용 하 여 조직에서 PST 파일을 찾고, 제어 하 고, 수집 하 고, 삭제 하는 프로세스에 대 한 간략 한 개요입니다.
  
![PST 모음 도구 프로세스 개요](media/67a29f27-f83c-4f0a-9df4-7ed92d3086fe.png)
  
1. **[1 단계: 네트워크에서 pst 파일 찾기](#step-1-find-pst-files-on-your-network)** -도구를 실행 하 여 pst 파일을 찾을 때 클라이언트 및 서버 컴퓨터에 대 한 Active Directory 개체를 포함 하는 위치 (예: 조직 구성 단위)를 지정 합니다. 특정 컴퓨터나 네트워크 파일 공유를 검색할 수도 있습니다. 이 도구를 실행 하면 대상 컴퓨터에 "경량" 컬렉션 에이전트가 설치 됩니다. 이 에이전트는 대상 컴퓨터에서 PST 파일을 검색 한 다음 해당 pst 파일에 대 한 정보를 PST 컬렉션 도구에 다시 보냅니다. 이 도구는 지정 된 위치에서 찾은 PST 파일에 대 한 정보가 포함 된 로그 파일을 만듭니다. 이러한 파일은 이후 단계에서 도구를 실행할 때 사용 됩니다. 
    
2. **[(옵션) 2 단계: pst 파일에 대 한 액세스 제어](#optional-step-2-control-access-to-pst-files)** -이 도구는 사용자가 pst 파일을 만들거나 변경할 수 없도록 설정 된 GPO (그룹 정책 개체)를 만듭니다. 이 GPO는 도메인의 모든 사용자에 게 적용 됩니다. 이 선택적 단계는 1 단계에서 찾은 PST 파일을 "잠가 두고, 새 PST 파일을 만들거나 기존 PST 파일을 변경 하지 않고 수집, 가져오기 및 삭제할 수 있도록 도와줍니다. 
    
3. **[3 단계: pst 파일을 모음 위치에 복사](#step-3-copy-the-pst-files-to-a-collection-location)** -이 방법을 사용 하면 4 단계에서 Office 365 가져오기 서비스를 사용 하 여 Exchange Online 사서함으로 가져올 수 있도록 pst 파일을 한 위치에 수집 합니다. "Collect" 모드에서 도구를 실행 하면 각 모음 에이전트는 에이전트를 설치 하는 대상 컴퓨터의 PST 파일을 모음 위치에 복사 합니다. 
    
4. **[4 단계: pst 파일을 Office 365로 가져오기](#step-4-import-the-pst-files-to-office-365)** -pst 파일을 한 위치에 복사한 후 Exchange Online 사서함으로 가져올 수 있습니다. 
    
5. **[5 단계: 네트워크에서 찾은 pst 파일 삭제](#step-5-delete-the-pst-files-found-on-your-network)** -Office 365에서 Exchange Online 사서함으로 가져온 pst 파일을 삭제 한 후에 pst 모음 도구를 사용 하 여 해당 pst 파일을 삭제할 수 있습니다. 1 단계에서 찾을 수 있습니다. 

## <a name="before-you-begin"></a>시작하기 전에

- 다음 단계에 따라 PST 컬렉션 도구를 로컬 컴퓨터에 다운로드 합니다. 
    
    1. [PST 컬렉션 도구를 다운로드](https://aka.ms/pstcollectiontool)합니다.
    
    2. 팝업 창에서 다른 **** \> **이름으로 저장** 을 클릭 하 여 로컬 컴퓨터의 폴더에 PSTCollectionTool 파일을 저장 합니다. 
    
    3. 로컬 컴퓨터의 폴더에 PSTCollectionTool 파일을 추출 합니다. 기본 폴더 이름은 PSTCollectionTool입니다.
    
- 모든 모드 (찾기, 차단, 복사 또는 삭제)에서 PST 모음 도구를 실행 하려면 Active Directory 도메인에서 Domain Administrators 그룹의 구성원 이어야 합니다. 

## <a name="step-1-find-pst-files-on-your-network"></a>1 단계: 네트워크에서 PST 파일 찾기

첫 번째 단계는 PST 모음 도구를 실행 하 여 조직에서 PST 파일을 찾는 것입니다. 이 도구를 사용 하 여 다음 유형의 위치를 검색할 수 있습니다. 
  
- 온-프레미스 Active Directory 도메인의 Ou (조직 구성 단위)입니다. 이 도구는 지정 된 OU에 포함 된 모든 컴퓨터를 검색 합니다. 
    
- 클라이언트 및 서버 컴퓨터 이 도구는 지정 된 컴퓨터를 검색 합니다. 
    
- 네트워크 파일 공유 이 도구는 지정 된 네트워크 파일 공유를 검색 합니다. 
    
이러한 각 위치 유형에 사용할 `Locations` 구문의 예는 다음 절차의 table의 매개 변수에 대 한 설명을 참조 하십시오. 
  
> [!IMPORTANT]
> PST 파일 차단, 수집 또는 삭제와 같은 다른 작업을 수행 하려면 찾기 모드에서 PST 수집 도구를 실행 해야 합니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트 (관리자 권한으로 실행)를 엽니다.
    
2. PSTCollectionTool 폴더 (또는 PSTCollectionTool 파일을 추출한 폴더)로 이동 합니다.
    
3. DataCollectorMaster 디렉터리로 변경 합니다.
    
4. 다음 명령을 실행 하 여 지정 된 위치에서 PST 파일을 찾습니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName <Name> -Locations <Locations to search for PSTs> -LogLocation <Location to store log files> -ConfigurationLocation <Location to store configuration files>
    ```

    다음 표에는 DataCollectorMaster 명령을 실행 하 여 PST 파일을 찾기 위한 매개 변수 및 해당 필수 값에 대 한 설명이 나와 있습니다. 
    
    |매개 변수 * * * *|****설명****|예 * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |검색할 데이터 유형을 지정 합니다. 현재는 PST 모음 도구를 사용 하 여 PST 파일을 검색할 수 있습니다.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |도구에서 수행 하는 작업의 유형을 지정 합니다. 값 `Find` 을 사용 하 여 지정 된 위치에서 PST 파일을 찾습니다. 이 도구는 outlook 프로필에 연결 된 Outlook 및 PST 파일에 열려 있는 PST 파일에 대 한 정보를 찾아서 가져올 수 있습니다.  <br/> | `-Mode Find` <br/> |
    | `JobName` <br/> |PST 컬렉션 작업의 이름을 지정 합니다. PST 컬렉션 도구를 실행 하 여 pst 파일을 찾기 위해 도구를 실행할 때 찾은 PST 파일을 차단, 수집 및 삭제할 때 동일한 작업 이름을 사용 하 게 됩니다. 작업 이름이 로그 및 구성 파일 이름에도 추가 됩니다.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> | PST 파일을 검색할 위치를 하나 이상 지정 합니다. 두 개 이상의 위치를 지정 하는 경우 세미콜론 (;))을 사용 합니다. 개별 위치를 구분 합니다. 이 매개 변수의 개별 값을 큰따옴표 ("")로 묶어야 합니다.  <br/><br/>   다음은 검색할 수 있는 위치 유형에 대 한 필수 id 값 형식입니다.  <br/><br/>        **Ou** -DN (고유 이름)을 사용 하 여 ou를 식별 합니다. 예를 들어:`"OU=NorthAmerica,OU=NWRegion,OU=ITServices,DC=contoso,DC=com"` <br/> > [!IMPORTANT]>는 조직 구성 단위가 아니므로 기본 제공 컴퓨터 컨테이너 (예: CN = Computers, DC = contoso, DC = com ")를 지정할 수 없습니다.<br/> <br/> **컴퓨터** -DN 또는 FQDN (정규화 된 도메인 이름)을 사용 하 여 네트워크에서 클라이언트 및 서버 컴퓨터를 식별 합니다. 예를 들어:  <br/>  D`"CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"` <br/>  또는  <br/>  사용한`"FILESERVER01.contoso.com"` <br/><br/>  **네트워크 파일 공유** -UNC 이름을 사용 하 여 네트워크 파일 공유를 식별 합니다. 예를 들어`"\\FILESERVER02\Users"` <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `LogLocation` <br/> |로그 파일을 복사할 폴더를 지정 합니다. 폴더가 없는 경우에는 도구를 실행할 때 만들어집니다.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ConfigurationLocation` <br/> |.Xml 구성 파일이 복사 될 폴더를 지정 합니다. 이 파일에는 도구를 실행할 때 발견 된 각 PST 파일에 대 한 정보가 포함 되어 있습니다. 이 파일은 3 단계에서 도구를 실행 하 여 찾은 PST 파일을 복사 하는 경우에 사용 됩니다.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `ExcludedLocations` <br/> |이 선택적 매개 변수는 찾기 작업 중에 건너뛸 위치를 지정 합니다. 특정 Ou, 컴퓨터 및 네트워크 파일 공유를 제외할 수 있습니다. 예를 들어 시스템을 SQL server (또는 다른 종류의 응용 프로그램 서버)로 구성 하는 컴퓨터를 해당 사용자가 액세스할 수 없는 컴퓨터를 제외 하면 됩니다. 제외할 위치를 두 개 이상 지정 하는 경우 세미콜론 (;))을 사용 합니다. 개별 위치를 구분 합니다. 이 매개 변수의 개별 값을 큰따옴표 ("")로 묶어야 합니다.  <br/> | `-ExcludedLocations "SQLSERVER01.contoso.com"` <br/> |
    | `ForceRestart` <br/> |이 선택적 스위치를 사용 하 여 기존 PST 수집 작업에 대 한 찾기 모드에서 도구를 실행할 수 있습니다. `ForceRestart` 스위치를 사용 하는 경우 작업에 대 한 이전 찾기 작업의 결과가 무시 되 고 도구는 지정 된 위치를 다시 검사 하 여 새 로그 및 구성 파일을 만듭니다.  <br/> | `-ForceRestart` <br/> |
   
    다음은 각 매개 변수에 대 한 실제 값을 사용 하는 DataCollectorMaster 명령 구문의 예입니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Find -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -LogLocation "c:\users\admin\desktop\PSTCollection" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"
    ```

    명령을 실행 한 후에는 지정 된 위치에서 PST 파일을 찾는 과정을 보여 주는 자세한 상태 메시지가 표시 됩니다. 잠시 후에 최종 상태 메시지에는 검색 된 PST 파일의 총 수, 작업이 완료 되었는지 여부 및 오류가 발생 했는지가 표시 됩니다. 동일한 상태 메시지가 .log 파일에 복사 됩니다.
    
### <a name="results-of-running-datacollectormasterexe-in-the-find-mode"></a>찾기 모드에서 DataCollectorMaster를 실행 한 결과

찾기 모드에서 PST 컬렉션 도구를 성공적으로 실행 하면 다음 파일이 만들어지고 `LogLocation` 및 `ConfigurationLocation` 매개 변수에 지정 된 폴더에 저장 됩니다. 
  
- **JobName\>__ datetimestamp\>. .log-로그 파일에는 표시 된 상태 메시지가 포함 됩니다.\< \<** 이 파일은 `LogLocation` 매개 변수에 지정 된 폴더에 만들어집니다. 
    
- **\<\>JobName\>Find datema csv 파일에는 검색 된 각 PST 파일에 대 한 행이 포함 되어 있습니다.__ \<** 각 PST에는 PST 파일이 있는 컴퓨터, pst 파일의 전체 경로 위치, pst 파일의 소유자, PST 파일의 크기 (킬로바이트, Kb)가 포함 되어 있습니다. 이 파일은 `LogLocation` 매개 변수에 지정 된 폴더에 만들어집니다. 
    
    > [!TIP]
    > Excel에서 자동 합계 도구를 사용 하 여 CSV 파일에 나열 된 모든 PST 파일의 전체 크기 (MB)를 계산 합니다. 그런 다음 변환 계산기를 사용 하 여 총 크기를 메가바이트 (MB) 나 기가바이트 (GB)로 변환할 수 있습니다. 
  
- **\>__\>JobName find\<datetimestamp-xml 파일에는 찾기 모드에서 도구를 실행할 때 사용 되는 매개 변수 값에 대 한 정보가 들어 \<있습니다.** 이 파일에는 찾은 모든 PST 파일에 대 한 정보도 포함 됩니다. 이 파일의 데이터는 동일한 작업에 대해 도구를 다시 실행 하 여 검색 된 PST 파일을 차단, 수집 또는 삭제 하는 데 사용 됩니다. 이 파일은 `ConfigurationLocation` 매개 변수에 지정 된 폴더에 만들어집니다. 
    
    > [!IMPORTANT]
    > 이 파일의 이름을 바꾸거나 변경 하거나 이동 하지 않습니다. 이 도구는 동일한 작업에 대 한 차단, 복사 또는 삭제 모드에서 공구를 다시 실행할 때 PST 컬렉션 도구에서 사용 됩니다. 

## <a name="optional-step-2-control-access-to-pst-files"></a>반드시 2 단계: PST 파일에 대 한 액세스 제어

이 선택적 단계를 사용 하면 1 단계에서 찾은 PST 파일을 "잠가"이를 통해 알려진 PST 파일 집합을 수집 하 고 Office 365로 가져올 수 있습니다. 차단 모드에서 PST 컬렉션 도구를 실행 하면 다음과 같은 결과가 발생 합니다. 
  
- 이 도구는 *PST 사용 컨트롤* 이라는 GPO (그룹 정책 개체)를 만듭니다. 이 GPO는 도메인에 연결 되어 있으며 조직의 모든 인증 된 사용자에 게 적용 됩니다. 
    
- PST 사용 컨트롤 GPO는 조직의 컴퓨터에 레지스트리 설정을 만듭니다. 사용 하는 매개 변수에 따라 사용자가 기존 PST 파일을 변경할 수 없도록 하는 레지스트리 설정 및 새 PST 파일을 만드는 것을 방지 하는 레지스트리 설정을 만들 수 있습니다.
    
> [!NOTE]
> 조직의 PST 파일에 대 한 액세스 제어가 너무 방해가 되는 경우이 단계를 건너뛰고 3 단계를 수행 하 여 PST 파일을 중앙 위치에 복사할 수 있습니다. 그런 다음이 `ForceRestart` 매개 변수를 사용 하 여 동일한 작업에 대해 1 단계를 반복 하 여 pst 파일을 컬렉션 위치로 복사한 후에 만든 추가 pst 파일을 찾을 수 있습니다. 새 PST 파일이 있으면 모음 위치에 복사할 수 있습니다. 이 매개 변수를 `ForceRestart` 사용 하면 찾기 모드에서 도구를 다시 실행할 때 작업에 대 한 이전 찾기 작업의 결과가 무시 되 고 지정 된 위치를 다시 검사 합니다. 

PST 파일에 대 한 액세스를 차단 하려면:

1. 로컬 컴퓨터에서 명령 프롬프트 (관리자 권한으로 실행)를 엽니다.
    
2. PST 수집 도구를 다운로드 한 디렉터리로 이동 합니다.
    
3. 1 단계에서 찾은 PST 파일에 대 한 액세스를 차단 하려면 다음 명령을 실행 합니다.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -BlockChangesToFiles -BlockNewFiles
    ```

    다음 표에서는 DataCollectorMaster 명령을 실행 하 여 PST 파일의 생성 및 변경을 차단 하는 경우 매개 변수 및 해당 필수 값에 대해 설명 합니다. 
    
    |매개 변수 * * * *|****설명****|예 * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |검색할 데이터 유형을 지정 합니다. 현재는 PST 모음 도구를 사용 하 여 PST 파일을 검색할 수 있습니다.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |도구에서 수행 하는 작업의 유형을 지정 합니다. 이 값 `Block` 을 사용 하 여 사용자가 새 pst 파일을 만들고 기존 pst 파일을 변경 하지 못하도록 할 수 있습니다.  <br/> | `-Mode Block` <br/> |
    | `JobName` <br/> |기존 PST 컬렉션 작업의 이름을 지정 합니다. 1 단계의 찾기 모드에서 도구를 실행할 때 사용한 것과 동일한 작업 이름을 사용 해야 합니다. 이 작업 이름은 차단 모드에서 도구를 실행할 때 만들어지는 로그 파일의 이름에도 추가 됩니다.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |찾기 모드에서 도구를 실행할 때 만든 .xml 구성 파일을 포함 하는 폴더를 지정 합니다. 1 단계에서이 매개 변수에 사용한 것과 같은 값을 사용 합니다.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |Block 작업의 로그 파일이 복사 될 폴더를 지정 합니다. 선택적 매개 변수입니다. 이 파일을 포함 하지 않으면 PST 컬렉션 도구를 다운로드 한 폴더에 로그 파일이 복사 됩니다. 모든 로그 파일이 같은 폴더에 저장 되도록 1 단계의 찾기 모드에서 도구를 실행할 때 사용한 것과 동일한 로그 위치를 사용 하는 것이 좋습니다.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `BlockChangesToFiles` <br/> |이 스위치를 사용 하 여 사용자가 PST 파일을 변경 하지 못하도록 합니다. 이 스위치를 사용 하면 다음 레지스트리 항목이 만들어지고 데이터 값은 1 `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\PST\PstDisableGrow` 로 설정 됩니다. 이 레지스트리 설정은 차단 모드에서 PST 컬렉션 도구를 실행할 때 만들어지는 GPO에 의해 조직의 컴퓨터에서 만들어집니다.  <br/> | `-BlockChangesToFiles` <br/> |
    | `BlockNewFiles` <br/> |이 스위치를 사용 하 여 사용자가 새 PST 파일을 만들거나 Outlook으로 PST 파일을 열고 Outlook에서 PST 파일을 내보내는 것을 방지할 수 있습니다. 이 스위치를 사용 하면 다음 레지스트리 항목이 만들어지고 데이터 값은 1 `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\<version>\Outlook\DisablePst` 로 설정 됩니다. 이 레지스트리 설정은 차단 모드에서 PST 컬렉션 도구를 실행할 때 만들어지는 GPO에 의해 조직의 컴퓨터에서 만들어집니다.  <br/> | `-BlockNewFiles` <br/> |
   
    다음은 각 매개 변수에 대 한 실제 값을 사용 하는 DataCollectorMaster 명령 구문의 예입니다.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Block -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection" -BlockChangesToFiles -BlockNewFiles
    ```
    
    새 PST 파일 또는 기존 PST 파일에 대 한 변경 내용을 차단할지 확인 하는 메시지가 표시 됩니다. 계속할 것을 확인 하 고 명령이 성공적으로 실행 되 면 "PST 사용 컨트롤" 이라는 새 GPO가 만들어져 있음을 알리는 메시지가 표시 됩니다.
    
## <a name="step-3-copy-the-pst-files-to-a-collection-location"></a>3 단계: PST 파일을 모음 위치에 복사

다음 단계는 찾기 모드에서 PST 컬렉션 도구를 실행할 때 찾은 PST 파일을 복사 하는 것입니다. 이를 통해 나중에 Office 365로 가져올 수 있도록 PST 파일을 한 위치에서 수집 합니다. PST 파일을 모음 위치에 복사 하기 전에 필요한 총 저장 공간을 결정 하는 것이 좋습니다. 1 단계에서 만든 CSV 파일을 사용 하 여 모든 PST 파일의 총 크기를 계산 하는 방법으로이 작업을 수행할 수 있습니다.
  
> [!NOTE]
> PST 파일을 Office 365로 가져오고 원래 위치에서 삭제 한 후에는이 단계에서 복사한 컬렉션 위치에서 삭제 하는 것이 좋습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트 (관리자 권한으로 실행)를 엽니다.
    
2. PST 수집 도구를 다운로드 한 디렉터리로 이동 합니다.
    
3. 다음 명령을 실행 하 여 PST 파일을 지정 된 위치에 복사 합니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName <Name of job from Step 1> -Locations <same locations from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    다음 표에는 DataCollectorMaster 명령을 실행 하 여 PST 파일을 복사할 때의 매개 변수 및 해당 필수 값에 대 한 설명이 나와 있습니다. 
    
    |매개 변수 * * * *|****설명****|예 * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |검색할 데이터 유형을 지정 합니다. 현재는 PST 모음 도구를 사용 하 여 PST 파일을 검색할 수 있습니다.  <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |도구에서 수행 하는 작업의 유형을 지정 합니다. 이 값 `Collect` 을 사용 하 여 찾기 모드에서 도구를 실행할 때 찾은 해당 PST 파일을 복사 합니다. 이 도구는 outlook에 열려 있는 pst 파일을 복사 하 고 outlook 프로필에 연결 된 PST 파일을 복사할 수 있습니다.  <br/> | `-Mode Collect` <br/> |
    | `JobName` <br/> |기존 PST 컬렉션 작업의 이름을 지정 합니다. 1 단계의 찾기 모드에서 도구를 실행할 때 사용한 것과 동일한 작업 이름을 사용 해야 합니다. 이 작업 이름은 수집 모드에서 도구를 실행할 때 만들어지는 로그 파일의 이름에도 추가 됩니다.  <br/> | `-JobName PstSearch1` <br/> |
    | `Locations` <br/> |1 단계에서 `Locations` 매개 변수에 사용한 것과 같은 값을 사용 합니다. 도구를 다시 실행 하 여 5 단계에서 원본 위치에 있는 PST 파일을 삭제 하려면이 도구를 Collect 모드에서 실행할 때이 매개 변수를 포함 해야 합니다.  <br/> | `-Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com"; "CN=FILESERVER02,CN=Computers,DC=contoso,DC=com"` <br/> |
    | `ConfigurationLocation` <br/> |찾기 모드에서 도구를 실행할 때 만들어진 .xml 구성 파일을 포함 하는 폴더를 지정 합니다. 1 단계에서이 매개 변수에 사용한 것과 같은 값을 사용 합니다.  <br/> | `-ConfigurationLocation "c:\users\admin\desktop \PSTCollection\Configuration"` <br/> |
    | `CopyLocation` <br/> |PST 파일을 복사해 넣을 컬렉션 위치를 지정 합니다. 파일 서버, 네트워크 파일 공유 또는 하드 드라이브로 파일을 복사할 수 있습니다. 수집 모드에서 도구를 실행 하기 전에 위치가 존재 해야 합니다. 도구에서 위치를 만들지 않으며 해당 위치가 존재 하지 않는다는 오류가 반환 됩니다.  <br/> 또한이 매개 변수로 지정 된 컬렉션 위치에 대 한 사용 권한을 써야 합니다.  <br/> | `-CopyLocation "\\FILESERVER03\PSTs"` <br/> |
    | `LogLocation` <br/> |수집 모드의 로그 파일이 복사 될 폴더를 지정 합니다. 선택적 매개 변수입니다. 이 파일을 포함 하지 않으면 PST 컬렉션 도구를 다운로드 한 폴더에 로그 파일이 복사 됩니다. 모든 로그 파일이 같은 폴더에 저장 되도록 1 단계의 찾기 모드에서 도구를 실행할 때 사용한 것과 동일한 로그 위치를 사용 하는 것이 좋습니다.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |이 선택적 스위치를 사용 하면 기존 PST 수집 작업에 대 한 도구를 모음 모드로 다시 실행할 수 있습니다. 이전에 수집 모드에서 도구를 실행 했지만 PST 파일에 대 한 다시 검사 위치를 사용 하 여 찾기 모드 `ForceRestart` 에서 도구를 다시 실행 한 경우에는이 스위치를 사용 하 여 도구를 모음 모드에서 다시 실행할 수 있고, 해당 사용자가 찾은 pst 파일을 다시 복사할 수도 있습니다. 위치를 다시 검사 합니다. 컬렉션 모드에서 `ForceRestart` 스위치를 사용 하는 경우이 도구는 이전 수집 작업을 무시 하 고 PST 파일을 처음부터 복사 하려고 시도 합니다.  <br/> | `-ForceRestart` <br/> |
   
    다음은 각 매개 변수에 대 한 실제 값을 사용 하는 DataCollectorMaster의 구문 예입니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Collect -JobName PstSearch1 -Locations "CN=FILESERVER01,CN=Computers,DC=contoso,DC=com";"CN=FILESERVER02,CN=Computers,DC=contoso,DC=com" -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -CopyLocation "\\FILESERVER03\PSTs" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```

    명령을 실행 한 후에는 1 단계에서 찾은 PST 파일 수집 진행 상황을 보여 주는 자세한 상태 메시지가 표시 됩니다. 잠시 후에 오류 및 로그를 복사 하는 위치에 대 한 최종 상태 메시지가 표시 됩니다. 동일한 상태 메시지가 .log 파일에 복사 됩니다.
    
### <a name="results-of-running-datacollectormasterexe-in-the-collect-mode"></a>수집 모드에서 DataCollectorMaster를 실행 한 결과

Collect 모드에서 DataCollectorMaster를 실행 한 후에는 `LogLocation` 및 `ConfigurationLocation` 매개 변수로 지정 된 폴더에 다음 파일이 만들어지고 저장 됩니다. 
  
- **JobName\>__ datetimestamp\>. .log-로그 파일에는 표시 된 상태 메시지가 포함 됩니다.\< \<** 이 파일은 `LogLocation` 매개 변수에 지정 된 폴더에 만들어집니다. 
    
- **\>__ JobName에서\<datetimestamp\>.xml-xml 파일에는 도구에서 사용 하는 수집 모드에서 실행 된 매개 변수 값에 대 한 정보만 포함 \<** 됩니다. DataCollectorMaster 도구를 다시 실행 하 여 PST 파일을 삭제 하면이 파일의 데이터가 사용 됩니다. [5 단계](#step-5-delete-the-pst-files-found-on-your-network)를 참조 하세요.
    

## <a name="step-4-import-the-pst-files-to-office-365"></a>4 단계: PST 파일을 Office 365로 가져오기

1 단계에서 찾은 PST 파일을 수집한 후에는 Office 365에서 사서함으로 해당 항목을 가져옵니다. 가져오기 프로세스를 수행할 때 가져올 각 PST 파일의 행이 포함 된 CSV 매핑 파일을 만들어야 합니다. 각 행에 있는 정보는 PST 파일의 이름, 사용자의 전자 메일 주소, PST 파일을 사용자의 기본 사서함으로 가져올지 아니면 보관할지를 사용할 것인지를 지정 합니다. Csv 매핑 파일을 만들려면 **JobName\>_Find_\<datetimestamp** 파일 (1 단계에서 만들어짐)의 정보를 사용 합니다. 
  
PST 파일을 Office 365로 가져오는 단계별 지침은 다음 항목 중 하나를 참조 하십시오.
  
- [네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기](use-network-upload-to-import-pst-files.md)
    
- [드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md)
    

## <a name="step-5-delete-the-pst-files-found-on-your-network"></a>5 단계: 네트워크에서 찾은 PST 파일 삭제

찾은 후 수집한 PST 파일을 Office 365에서 Exchange Online 사서함으로 가져온 후에는 PST 컬렉션 도구를 사용 하 여 1 단계에서 찾은 원래 원본 위치에서 PST 파일을 삭제할 수 있습니다. 
  
1. 로컬 컴퓨터에서 명령 프롬프트 (관리자 권한으로 실행)를 엽니다.
    
2. PST 수집 도구를 다운로드 한 디렉터리로 이동 합니다.
    
3. 다음 명령을 실행 하 여 PST 파일을 삭제 합니다.

    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName <Name of job from Step 1> -ConfigurationLocation <Location of configuration files from Step 1> -CopyLocation <Location to copy PST files to>
    ```

    다음 표에는 DataCollectorMaster 명령을 실행 하 여 PST 파일을 삭제할 때의 매개 변수 및 해당 필수 값에 대 한 설명이 나와 있습니다. 
    
    |매개 변수 * * * *|****설명****|예 * * * *|
    |:-----|:-----|:-----|
    | `DataSource` <br/> |검색할 데이터 유형을 지정 합니다. 현재는 PST 모음 도구를 사용 하 여 PST 파일을 검색할 수 있습니다. ![>](media/b078d05c-3aee-4b9f-8805-6a8a9d8970ee.png)           <br/> | `-DataSource Pst` <br/> |
    | `Mode` <br/> |도구에서 수행 하는 작업의 유형을 지정 합니다. 이 값 `Delete` 을 사용 하 여 찾기 모드에서 도구를 실행할 때 찾은 해당 PST 파일을 삭제 합니다.  <br/> | `-Mode Delete` <br/> |
    | `JobName` <br/> |기존 PST 컬렉션 작업의 이름을 지정 합니다. 찾기 모드에서 도구를 실행할 때 사용한 것과 동일한 작업 이름과 1 단계 및 3 단계의 수집 모드를 사용 해야 합니다. 이 작업 이름은 삭제 모드에서 도구를 실행할 때 만들어지는 로그 파일의 이름에도 추가 됩니다.  <br/> | `-JobName PstSearch1` <br/> |
    | `ConfigurationLocation` <br/> |수집 모드에서 도구를 실행할 때 만든 .xml 구성 파일이 포함 된 폴더를 지정 합니다. 3 단계에서이 매개 변수에 사용한 것과 같은 값을 사용 합니다.  <br/> | `-ConfigurationLocation "c:\users\admin\ desktop\PSTCollection\Configuration"` <br/> |
    | `LogLocation` <br/> |삭제 모드에 대 한 로그 파일이 복사 될 폴더를 지정 합니다. 선택적 매개 변수입니다. 이 파일을 포함 하지 않으면 PST 컬렉션 도구를 다운로드 한 폴더에 로그 파일이 복사 됩니다. 모든 로그 파일이 같은 폴더에 저장 되도록 1 단계와 3 단계의 찾기 및 수집 모드에서 도구를 실행할 때 사용한 것과 동일한 로그 위치를 사용 하는 것이 좋습니다.  <br/> | `-LogLocation "c:\users\admin\desktop\PSTCollection"` <br/> |
    | `ForceRestart` <br/> |이 선택적 스위치를 사용 하 여 기존 PST 수집 작업에 대 한 삭제 모드에서 도구를 다시 실행할 수 있습니다. 이전에 삭제 모드에서 도구를 실행 했지만 PST 파일의 위치를 다시 검사 하는 `ForceRestart` 스위치를 사용 하 여 찾기 모드에서 도구를 다시 실행 한 경우이 스위치를 사용 하 여 삭제 모드에서 도구를 재실행 하 고 다시 sca에서 찾은 PST 파일을 삭제할 수 있습니다. n 위치를 했습니다. 삭제 모드에서 `ForceRestart` 스위치를 사용 하는 경우이 도구는 이전 삭제 작업을 무시 하 고 PST 파일 삭제를 시도 합니다.  <br/> | `-ForceRestart` <br/> 

    다음은 각 매개 변수에 대 한 실제 값을 사용 하는 DataCollectorMaster의 구문 예입니다.
    
    ```
    DataCollectorMaster.exe -DataSource Pst -Mode Delete -JobName PstSearch1 -ConfigurationLocation "c:\users\admin\desktop\PSTCollection\Configuration" -LogLocation "c:\users\admin\desktop\PSTCollection"
    ```
   
    명령을 실행 하면 1 단계에서 확인 하 여 3 단계에서 수집한 PST 파일 삭제 진행률을 보여 주는 자세한 상태 메시지가 표시 됩니다. 잠시 후에 오류 및 로그를 복사 하는 위치에 대 한 최종 상태 메시지가 표시 됩니다. 동일한 상태 메시지가 .log 파일에 복사 됩니다.
    
### <a name="results-of-running-datacollectormasterexe-in-the-delete-mode"></a>삭제 모드에서 DataCollectorMaster를 실행 한 결과

삭제 모드에서 DataCollectorMaster를 실행 한 후에는 `LogLocation` 및 `ConfigurationLocation` 매개 변수에 지정 된 폴더에 다음 파일이 만들어지고 저장 됩니다. 
  
- **JobName\>__ datetimestamp\>. .log-로그 파일에 표시 된 상태 메시지가 포함 됩니다.\< \<** 이 파일은 `LogLocation` 매개 변수에 지정 된 폴더에 만들어집니다. 
    
- **\>__\>JobName delete\<datetimestamp .xml-xml 파일에는 도구에서 사용 하는 삭제 모드에서 실행 된 매개 변수 값에 대 한 정보만 포함 \<** 됩니다. 또한 삭제 된 각 PST 파일의 이름과 파일 경로가 나열 됩니다. 이 파일은 `ConfigurationLocation` 매개 변수에 지정 된 폴더에 만들어집니다. 
