---
title: Office 365에서 타사 데이터 보관
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: '관리자는 Office 365 조직에서 사서함에 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 타사 데이터를 가져올 수 있습니다. 이 통해 Office 365에서 Facebook, Twitter 및 데이터 원본의 데이터를 보관할 수 있습니다. 다음을 제 3 자 데이터 (예: 법적 보유, 콘텐츠 검색 및 보존 정책) appply Office 365 규정 준수 기능을 수 있습니다.'
ms.openlocfilehash: 7af88338333e90bd208d693fbfd5bb691d44b538
ms.sourcegitcommit: 4c6c937ec51e8b754332e4c1c8d286e73e197e2c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "23827092"
---
# <a name="archiving-third-party-data-in-office-365"></a>Office 365에서 타사 데이터 보관

관리자가 가져오기 및 인스턴트 메시징 플랫폼을 및 Office 365 조직에서 사서함에 문서 공동 작업 플랫폼, 소셜 미디어 플랫폼에서 타사 데이터 보관 office 365 사용 수 있습니다. Office 365로 가져올 수 있는 타사 데이터 원본의 예는 다음과 같습니다. 
  
- **공유** -Twitter, Facebook, Yammer, 및 LinkedIn 
    
- **인스턴트 메시징** -yahoo Messenger, GoogleTalk, 및 Cisco Jabber 
    
- **문서 공동 작업** -상자 및 드롭 상자 
    
- **수직 산업은** -(예: 가지 Salesforce 채팅) 고객 관계 관리 하 고 Financials (예: 톰슨 Reuters 및 Bloomberg) 
    
- **SMS/텍스트 메시징** -BlackBerry 
    
제 3 자 데이터를 가져온 후에 Office 365 규정 준수 기능을 적용할 수 있습니다-예: 소송 보존으로 설정, 콘텐츠 검색, 원본 위치 보관, 감사, 및 Office 365 보존 정책-이 데이터에 있습니다. 예, 사서함은 소송 보존에 배치 되 면 제 3 자 데이터 유지 됩니다. 콘텐츠 검색을 사용 하 여 제 3 자 데이터를 검색할 수 있습니다. 또는 보관을 적용할 수 있습니다 및 타사 데이터와 마찬가지로 Microsoft 데이터에 대 한에 보존 정책입니다. 즉, Office 365의 타사 데이터 보관 정부 및 정책 규정 준수 상태를 유지 하 여 조직의 도움이 수 있습니다.
  
Office 365를 제 3 자 데이터를 가져오려면 필요한 단계 및 프로세스를 간략하게가 같습니다.

[1단계: 타사 데이터 파트너 찾기](#step-1-find-a-third-party-data-partner)

[2단계: Office 365에서 타사 데이터 사서함 만들기 및 구성](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[3단계: 타사 데이터에 대한 사용자 사서함 구성](#step-3-configure-user-mailboxes-for-third-party-data)

[4단계: 파트너에게 정보 제공](#step-4-provide-your-partner-with-information)

[5 단계: Azure Active Directory에 제 3 자 데이터 커넥터를 등록 합니다.](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a>타사 데이터 가져오기 프로세스 어떻게 작동 하는 >

다음 그림과 설명은 타사 데이터 가져오기 프로세스의 작동 방식에 대해 설명합니다.
  
![타사 데이터 가져오기 프로세스의 작동 방식](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. 선택한 항목 제 3 자 데이터 원본에서 추출을 Office 365에 해당 항목을 가져오는 있는 커넥터를 구성 하는 파트너와 고객 작동 합니다.
    
2. 파트너 커넥터 (프로그램 별로 또는 예약 된 구성으로) 타사 API 통해 타사 데이터 원본에 연결 하 고 데이터 원본에서 항목을 추출 합니다. 전자 메일 메시지 형식에 있는 항목의 콘텐츠를 변환 하는 파트너 커넥터입니다. 메시지 형식 스키마에 대 한 설명에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 
    
3. 파트너 커넥터 잘 알려진 끝점을 통해 Exchange 웹 서비스 (EWS)를 사용 하 여 Office 365에서 Azure 서비스에 연결 합니다.
    
4. 항목은 특정 사용자의 사서함 또는 "범용" 타사 데이터 사서함으로 가져오기됩니다. 항목을 특정 사용자 사서함으로 가져올지 또는 타사 데이터 사서함으로 가져올지는 다음 기준을 기반으로 합니다.
    
    a. **는 Office 365 사용자 계정에 해당 하는 사용자 ID를 갖는 항목** 파트너 커넥터 Office 365, 항목의에서 ID는 사용자의 **제거** 폴더에 복사는 특정 사용자에 게 타사 데이터 원본에 있는 항목의 사용자 ID를 매핑할 수 있는 경우 복구 가능한 항목 폴더입니다. 사용자가 제거 폴더의 항목에 액세스할 수 없습니다. 그러나 Office 365 eDiscovery 도구를 사용 하 여 제거 폴더에서 항목을 검색할 수 있습니다.
    
    b. **하는 Office 365 사용자 계정에 해당 하는 사용자 ID가 없는 항목** -경우 파트너 커넥터 Office 365, 항목의에서 ID를 제 3 자 데이터 사서함의 **받은 편지함** 폴더에 복사 되는 특정 사용자에 게 항목의 사용자 ID를 매핑할 수 없습니다. 받은 편지함에 항목 가져오기 (영문) 보고 이러한 항목을 관리 하 고 파트너 커넥터 구성에서 필요에 따라 수정 해야하는 경우를 참조 하는 타사 사서함에 로그인 하 여 조직에서 사용자 또는 다른 있습니다.
 
## <a name="step-1-find-a-third-party-data-partner"></a>1단계: 타사 데이터 파트너 찾기

Office 365의 제 3 자 데이터를 보관 하기 위한 주요 구성 요소를 찾아 제 3 자 데이터 원본에서 데이터 캡처 및 Office 365로 가져오기에 대해 전문적으로 담당 하는 Microsoft 파트너 (영문). 데이터를 가져온 다음, 해당 수 보관 하 고와 함께 유지 하면 조직에서 Exchange 전자 메일 및 SharePoint와 비즈니스용 OneDrive에서 문서와 같은 다른 Microsoft 데이터의 합니다. 파트너는 조직의 타사 데이터 원본 (예: BlackBerry, Facebook, Google +, 톰슨 Reuters, Twitter, 및 YouTube)에서 데이터를 추출 하 고 항목으로 Exchange 사서함으로 가져옵니다 하는 Office 365 API를 해당 데이터를 전달 하는 커넥터를 만듭니다. 전자 메일 메시지입니다. 
  
다음 섹션에서는 Microsoft 파트너 목록을-하 고 지 원하는 타사 데이터 원본-하는 Office 365의 제 3 자 데이터를 보관 하기 위한 프로그램에 참여 하 고 있습니다.

[17a-4 LLC](#17a-4-llc)
  
[Actiance](#actiance)
  
[ArchiveSocial](#archivesocial)
  
[Globanet](#globanet)
  
[OpenText](#opentext)
  
[Verba](#verba)
  
### <a name="17a-4-llc"></a>17a-4 LLC

17a-4 LLC에서는 다음의 타사 데이터 원본을 지원합니다.
  
- BlackBerry
    
- Bloomberg Data Streams
    
- Cisco Jabber
    
- FactSet
    
- HipChat
    
- InvestEdge
    
- LivePerson
    
- 
MessageLabs Data Streams

    
- OpenText
    
- Oracle/ATG 'click-to-call' Live Help

    
- Pivot IMTRADER

    
- Microsoft SharePoint
    
- MindAlign
    
- Sitrion One(Newsgator)
    
- 
비즈니스용 Skype(Lync/OCS)
    
- 
비즈니스용 Skype Online(Lync Online)

    
- SQL 데이터베이스
    
- 
Squawker

    
- Thomson Reuters Eikon Messenger

  
### <a name="actiance"></a>Actiance

[Actiance](https://www.actiance.com) 에서는 다음과 같은 제 3 자 데이터 원본을 지원합니다. 
  
- AIM
    
- American Idol
    
- Apple Juice
    
- 
AOL with Pivot client

    
- Ares
    
- Bazaar Voice
    
- Bear Share
    
- Bit Torrent
    
- BlackBerry Call Logs(v5, v10, v12)
    
- BlackBerry Messenger(v5, v10, v12)
    
- BlackBerry PIN(v5, v10, v12)
    
- BlackBerry SMS(v5, v10, v12)
    
- Bloomberg Mail

    
- CellTrust
    
- Chat Import

    
- Chat Real Time Logging and Policy

    
- Chatter

    
- IM cisco &amp; 현재 상태 서버 (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)
    
- Cisco Unified Presence Server(v8.6.3, v8.6.4, v8.6.5)

    
- Collaboration Import

    
- Collaboration Real Time Logging

    
- Direct Connect
    
- Facebook
    
- FactSet
    
- FastTrack
    
- Gnutella
    
- Google+

    
- GoToMyPC
    
- Hopster
    
- HubConnex
    
- IBM Connections(v3.0.1, v4.0, v4.5, v4.5 CR3, v5)

    
- IBM Connections Chat Cloud

    
- IBM Connections Social Cloud

    
- IBM SameTime Advanced 8.5.2 IFR1

    
- IBM SameTime Communicate 9.0

    
- IBM SameTime Community(v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)

    
- IBM SameTime Complete 9.0

    
- IBM SameTime Conference 9.0

    
- IBM SameTime Meeting 8.5.2 IFR1

    
- ICE/YellowJacket
    
- IM Import

    
- IM Real Time Logging and Policy

    
- Indii Messenger

    
- Instant Bloomberg

    
- IRC
    
- Jive

    
- Jive 6 Real Time Logging(v6, v7)

    
- Jive Import
    
- JXTA
    
- LinkedIn
    
- 
Microsoft Lync(2010, 2013)

    
- MFTP
    
- Microsoft Lync 2013 Voice

    
- Microsoft SharePoint(2010, 2013)

    
- Microsoft SharePoint Online
    
- Microsoft UC(Unified Communications)
    
- MindAlign
    
- Mobile Guard
    
- MSN
    
- My Space
    
- NEONetwork
    
- Office 365 Lync Dedicated

    
- Office 365 Shared IM

    
- Pinterest
    
- Pivot
    
- QQ
    
- 비즈니스용 Skype 2015
    
- SoftEther
    
- Symphony

    
- Thomson Reuters Eikon

    
- Thomson Reuters Messenger

    
- Tor
    
- TTT
    
- Twitter
    
- WinMX
    
- Winny
    
- Yahoo

    
- Yammer
    
- YouTube
    
  
### <a name="archivesocial"></a>ArchiveSocial

[ArchiveSocial](https://www.archivesocial.com) 에서는 다음과 같은 제 3 자 데이터 원본을 지원합니다. 
  
- Facebook
    
- Flickr

    
- Instagram

    
- LinkedIn
    
- Pinterest
    
- Twitter
    
- YouTube
    
- Vimeo
  
### <a name="globanet"></a>Globanet

[Globanet](https://www.globanet.com) 에서는 다음과 같은 제 3 자 데이터 원본을 지원합니다. 
  
- AOL with Pivot Client  
    
- BlackBerry Call Logs(v5, v10, v12)
    
- BlackBerry Messenger(v5, v10, v12)
    
- BlackBerry PIN(v5, v10, v12)
    
- BlackBerry SMS(v5, v10, v12)
    
- Bloomberg Chat

    
- Bloomberg Mail

    
- Box

    
- CipherCloud for Salesforce Chatter
    
- IM cisco &amp; 현재 상태 서버 (v10, v10.5.1 SU1 v11.0, v11.5 SU2)

- Cisco Webex 팀

- Citrix 작업 영역 &amp; ShareFile

- CrowdCompass

- 사용자 지정 구분 텍스트 파일

    
- 사용자 지정 XML 파일

    
- Facebook (페이지)
    
- Factset

    
- FXConnect
    
- ICE Chat/YellowJacket
    
- Jive

    
- Macgregor XIP


- Microsoft Exchange Server
    
- Microsoft 비즈니스용 OneDrive

- Microsoft Teams
       
- Microsoft Yammer

    
- Mobile Guard
    
- Pivot
    
- Salesforce Chatter

- 비즈니스용 Skype Online
    
- 비즈니스용 Skype, 버전 2007 R2 - 2016(온-프레미스)

    
- Slack Enterprise Grid
    
- Symphony

    
- Thomson Reuters Eikon

    
- Thomson Reuters Messenger

    
- Thomson Reuters Dealings 3000 / FX Trading

    
- Twitter
    
- UBS Chat

    
- YouTube
  
### <a name="opentext"></a>OpenText

[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) 에서는 다음과 같은 제 3 자 데이터 원본을 지원합니다. 
  
- Axs Encrypted
    
- Axs Exchange
    
- Axs Local Archive
    
- Axs PlaceHolder
    
- Axs Signed
    
- Bloomberg
    
- Thomson Reuters
  
### <a name="verba"></a>Verba

[Verba](https://www.verba.com) 에서는 다음과 같은 제 3 자 데이터 원본을 지원합니다. 
  
- Avaya Aura Video

    
- Avaya Aura Voice

    
- Avtec Radio

    
- Bosch/Telex Radio

    
- BroadSoft Video

    
- BroadSoft Voice

    
- Centile Voice

    
- Cisco Jabber IM

    
- Cisco UC Video

    
- Cisco UC Voice

    
- Cisco UCCX/UCCE 비디오
    
- Cisco UCCX/UCCE 음성
    
- ESChat Radio
    
- Geoman Contact Expert
    
- IP Trade Voice

    
- Luware LUCS Contact Center
    
- Microsoft UC(Unified Communications)
    
- Mitel MiContact Center for Lync(prairieFyre) 

    
- Oracle/Acme Packet Session Border Controller Video  

    
- Oracle/Acme Packet Session Border Controller Voice

    
- Singtel Mobile Voice

    
- SIPREC Video
    
-  SIPREC Voice 
    
- 비즈니스용 Skype/Lync IM

    
- 비즈니스용 Skype/Lync Video

    
- 비즈니스용 Skype/Lync Voice

    
- Speakerbus Voice

    
- Standard SIP/H.323 Video 

    
- Standard SIP/H.323 Voice 

    
- Truphone Voice

    
- TwistedPair Radio

    
- Windows 데스크톱 컴퓨터 화면 

  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a>2단계: Office 365에서 타사 데이터 사서함 만들기 및 구성

만들기 (영문) 및 Office 365로 데이터 가져오기 (영문)에 대 한 제 3 자 데이터 사서함을 구성 하기 위한 단계는 다음과 같습니다. 같이 이전 설명, 파트너 커넥터는 Office 365 사용자 계정에는 항목의 사용자 ID를 매핑할 수 없는 경우이 사서함에 항목이 가져와집니다.
  
 **Office 365 관리 센터에서 이러한 작업을 완료**
  
1. Office 365에서 새 사용자 계정 만들기 및 Exchange Online 계획 2는 운영 체제 버전; 할당 [Office 365에 사용자 추가](https://go.microsoft.com/fwlink/p/?LinkId=692098)참조 하십시오. 소송 보존에 배치 하는 사서함 또는 무제한 저장소 할당량을 된 보관 사서함을 사용 하도록 설정 하는 계획 2 라이선스가 필요 합니다.
    
2. 타사 데이터 사서함에 대 한 사용자 계정을 Office 365;에서 **Exchange 관리자가** 관리자 역할에 추가 [Office 365의 관리 역할 할당](https://go.microsoft.com/fwlink/p/?LinkId=532393)을 참조 하십시오.
    
    > [!TIP]
    > 이 사용자 계정의 자격 증명을 기록해 둡니다. 4단계에서 설명한 것처럼 파트너에게 제공해야 합니다. 
  
 **Exchange 관리 센터에서 이러한 작업을 완료**
  
1. 주소록 및 조직에서 다른 주소 목록에서 제 3 자 데이터 사서함 숨기기 [관리 사용자 사서함](https://go.microsoft.com/fwlink/p/?LinkId=616058)을 참조 하십시오. 또는 다음 PowerShell 명령을 실행할 수 있습니다.
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. 관리자 또는 규정 준수 담당자는 Outlook 데스크톱 클라이언트;에서 제 3 자 데이터 사서함을 열 수 있도록 제 3 자 데이터 사서함에 대 한 **FullAccess** 권한이 할당 [받는 사람에 대 한 사용 권한 관리를](https://go.microsoft.com/fwlink/p/?LinkId=692104)참조 하십시오.
    
3. 타사 데이터 사서함에 대 한 다음 준수와 관련 된 Office 365 기능을 사용 합니다.
    
    - 보관 사서함;를 사용 하도록 설정 참조 [Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터](enable-archive-mailboxes.md) 고 [Office 365에서 무제한 보관을 사용](enable-unlimited-archiving.md)합니다. 이렇게 하면 타사 데이터 항목의 보관 사서함으로 이동 하는 보관 정책의을 설정 하 여 주 사서함에서 약속 접속 저장 공간입니다. 타사 데이터에 대 한 무제한 저장소와 함께 제공 됩니다이 합니다.
    
    - 전체 제 3 자 데이터 사서함에 소송 보존으로 설정 합니다. Office 365 보안에는 Office 365 보존 정책을 적용할 수 있습니다 &amp; 준수 센터입니다. 보류에서이 사서함을 배치 제 3 자 데이터 항목 (무기한 또는 지정 된 기간에 대 한)를 유지 하 고 사서함에서 삭제 되 고에서 금지 됩니다. 다음 항목 중 하나를 참조 하십시오.
    
      - [사서함을 소송 자료 보존으로 설정](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [Office 365의 보존 정책 개요](retention-policies.md)
    
       
    
    - 사서함 감사 소유자, 대리인, 및 관리자의 사서함 액세스를 제 3 자 데이터;에 대 한 로깅을 사용 하도록 설정 [Office 365의 감사 사서함 사용](enable-mailbox-auditing.md)을 참조 하십시오. 이렇게 하면 타사 데이터 사서함에 액세스할 수 있는 모든 사용자에 의해 수행 되는 모든 작업을 감사할 수 있습니다.

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a>3단계: 타사 데이터에 대한 사용자 사서함 구성

다음 단계에서는 제 3 자 데이터를 지원 하도록 사용자 사서함을 구성 하는 것입니다. Exchange 관리 센터를 사용 하 여 또는 해당 Windows PowerShell cmdlet을 사용 하 여 이러한 작업을 완료 합니다.
  
1. 각 사용자에 대 한 보관 사서함을 사용 하도록 설정 참조 [Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터](enable-archive-mailboxes.md) 고 [Office 365에서 무제한 보관을 사용](enable-unlimited-archiving.md)합니다.
    
2. 소송 보존에 배치 하는 사용자 사서함 또는 Office 365 보존 정책 적용 다음 항목 중 하나를 참조 하십시오. 
    
    - [사서함을 소송 자료 보존으로 설정](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [Office 365의 보존 정책 개요](retention-policies.md)
    
    앞서 언급한 것처럼 사서함을 보존하면 타사 데이터 원본의 항목을 보존하는 기간을 설정하거나 항목을 무기한 보존하도록 선택할 수 있습니다.

## <a name="step-4-provide-your-partner-with-information"></a>4단계: 파트너에게 정보 제공

마지막 단계는 Office 365 조직에 연결하여 사용자 사서함이나 타사 데이터 사서함으로 데이터를 가져오도록 커넥터를 구성할 수 있게 파트너에게 다음 정보를 제공하는 것입니다. 
  
- Office 365에서 Azure 서비스에 연결할 때 사용 하는 끝점:

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- 자격 증명 (Office 365 사용자 ID 및 암호)의 2 단계에서에서 만든 타사 데이터 사서함에에서 로그인 합니다. 파트너 커넥터에 액세스 하 고 사용자 사서함을 제 3 자 데이터 사서함에 게 항목을 가져올 수 있도록 이러한 자격 증명이 필요 합니다.
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a>5 단계: Azure Active Directory에 제 3 자 데이터 커넥터를 등록 합니다.

2018, 년 9 월 30 시작 Office 365에서 Azure 서비스를 사용 하 여 최신 인증 Exchange 온라인 데이터를 가져오려면 Office 365 조직에 대 한 연결을 시도 하는 타사 데이터 커넥터 인증 시작 됩니다. 이 변경에 대 한 이유는 현대 인증 하는 앞에서 설명한 것된 끝점을 사용 하 여 Azure 서비스에 연결할 whitelisting 타사 커넥터를 기반으로 하는 현재 방법 보다 더 많은 보안을 제공 합니다.

새 현대 인증 방법을 사용 하 여 Office 365에 연결에 대 한 제 3 자 데이터 커넥터를 사용 하도록 설정 하려면 Office 365 조직에서 관리자는 Azure Active Directory에서 신뢰할 수 있는 서비스 응용 프로그램으로 커넥터를 등록 동의 해야 합니다. 이 커넥터 Azure Active Directory에서 조직의 데이터에 액세스할 수 있도록 사용 권한 요청을 수락 하 여 수행 됩니다. 이 요청을 수락 하면 후 제 3 자 데이터 커넥터 Azure Active Directory는 엔터프라이즈 응용 프로그램으로 추가 되 고 서비스 사용자로 표시 합니다. 자세한 내용은 사용자의 동의 하는 프로세스에 대 한 [테 넌 트 관리 동의](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent)참조 합니다.

액세스 하 고 커넥터를 등록 하려면 요청을 수락 하는 단계는 다음과 같습니다.

1. [이](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) 페이지로 이동 하 고 Office 365 전역 관리자의 자격 증명을 사용 하 여 로그인 합니다.<br/><br/>다음과 같은 대화 상자가 표시 됩니다. 커넥터에 할당 되는 권한 검토를 캐럿을 확장할 수 있습니다.<br/><br/>![사용 권한 요청 대화 상자가 표시 됩니다.](media/O365_ThirdPartyDataConnector_OptIn1.png)
2. **수락**을 클릭 합니다.

요청을 수락 하면 후 [Azure 포털](https://portal.azure.com) 표시 됩니다. **Azure Active Directory**를 클릭 하면 조직에 대 한 응용 프로그램의 목록을 보려면 > **엔터프라이즈 응용 프로그램**입니다. Office 365 제 3 자 데이터 커넥터는 **엔터프라이즈 응용 프로그램** 블레이드에 표시 됩니다.

> [!IMPORTANT]
> 2018, 년 9 월 30 후 제 3 자 데이터 더이상로 가져올 것임 조직 내의 사서함에에서 Azure Active Directory에 제 3 자 데이터 커넥터를 등록 하지 하는 경우. 또한 타사 데이터 커넥터 (2018 년 9 월 30, 이전에 만들어진 이러한) 기존 참고 5 단계에서에서 절차를 수행 하 여 Azure Active Directory에 등록 되어 있어야 합니다.

### <a name="revoking-consent-for-a-third-party-data-connector"></a>타사 데이터 커넥터에 대 한 사용자의 동의 해지합니다.

Azure Active Directory에 제 3 자 데이터 커넥터를 등록 하기 위해 사용 권한 요청에 조직 승인을 거친, 후 조직 언제 든 지 해당 사용자의 동의 취소할 수 있습니다. 그러나 연결선에 대 한 동의 해지는 의미 제 3 자 데이터 원본에서 데이터는 더이상 Office 365로 가져올 수 없습니다.

제 3 자 데이터 커넥터에 대 한 사용자의 동의 해지 하 여 삭제할 수 있습니다는 응용 프로그램을 (해당 서비스 사용자를 삭제) Azure 포털에서 또는 [를 사용 하 여 **엔터프라이즈 응용 프로그램** 블레이드를 사용 하 여 Azure Active Directory에서 제거 MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) Office 365 PowerShell에서 합니다. PowerShell Azure Active Directory에서에서 [제거 AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet을 사용할 수도 있습니다.
  
## <a name="more-information"></a>추가 정보

- 같이 이전 설명의 경우, 항목에서 타사 데이터 원본 전자 메일 메시지로 Exchange 사서함으로 가져옵니다. 파트너 커넥터는 Office 365 API에 필요한 스키마를 사용 하 여 항목을 가져옵니다. 다음 표에서 Exchange 사서함으로 전자 메일 메시지를 가져온 후 타사 데이터 원본에서 항목의 메시지 속성을 설명 합니다. 또한 표에 메시지 속성이 필수 인지를 나타냅니다. 필수 속성을 채워야 합니다. 항목 속성을 필수로 없으면 Office 365로 가져올 수 없습니다. 가져오기 프로세스에는 항목을 가져온 되지 않은 및 어느 속성이 없는 이유를 설명 하는 오류 메시지가 반환 됩니다.
    
    |**메시지 속성**|**필수 여부**|**설명**|**예제 값**|
    |:-----|:-----|:-----|:-----|
    |**FROM** <br/> |예  <br/> |사용자가 원래 만든 또는 타사 데이터 원본에서 항목을 전송 합니다. 파트너 커넥터는 모든 참가자에 게 (FROM 및 TO 필드의 사용자)에 대 한 Office 365 사용자 계정에 원본 항목 (예: Twitter 핸들)에서 사용자 ID를 매핑할 하려고 합니다. 모든 참가자의 사서함에 메시지의 복사본을 가져옵니다. Office 365 사용자 계정에 매핑될 수 없는 항목에서 참가자를 Office 365에서 타사 보관 사서함에 항목을 가져옵니다.<br/> <br/> 참가자에 게 보낸 사람이 항목으로 식별 되는 활성 사서함 항목을 가져오는 Office 365 조직에 있어야 합니다. 보낸 사람이 중인 사서함이 있는 없으면 다음 오류가 반환 됩니다.<br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |**TO** <br/> |예  <br/> |데이터 원본의 항목을 받은 사람입니다(해당되는 경우).  <br/> | `bob@contoso.com` <br/> |
    |**SUBJECT** <br/> |아니요  <br/> |원본 항목의 제목입니다.  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |**날짜** <br/> |예  <br/> |항목을 처음 만들었거나 고객 데이터 원본에 게시한 날짜입니다. 예로 Twitter 메시지가 트윗된 날짜가 있습니다.  <br/> | `01 NOV 2015` <br/> |
    |**BODY** <br/> |아니요  <br/> |메시지 또는 게시물의 내용입니다. 일부 데이터 원본의 경우이 속성의 내용을 **SUBJECT** 속성에 대 한 콘텐츠와 동일 하 게 일 수 있습니다. 가져오기 프로세스 동안 파트너 커넥터는 완전 한 충실도 가능한 콘텐츠 원본에서 유지 관리 하려고 합니다. 가능 하면 파일, 그래픽, 또는 기타 콘텐츠 원본 항목의 본문에서이 속성에 포함 됩니다. 그렇지 않은 경우 콘텐츠 원본 항목에서 **첨부 파일** 속성에 포함 됩니다. 이 속성의 내용을 파트너 커넥터 및 원본 플랫폼의 기능에 따라 달라 집니다.<br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |**ATTACHMENT** <br/> |아니요  <br/> |항목 (예: Twitter 또는 인스턴트 메시징 대화에서 소리) 데이터 원본에서 첨부 파일에 또는 이미지를 포함 하는 경우 파트너 **BODY** 속성에 첨부 파일을 포함 하는 첫번째 시도 연결 합니다. 가능한, 반드시 그럴 경우 다음에 추가 되는 * * 첨부 파일 * * 속성입니다. 다른 첨부 파일의 예로 좋아요 Facebook, 콘텐츠 원본 및 메시지 또는 게시물에 대 한 응답에서 메타 데이터에에서 있습니다.<br/> | `image.gif` <br/> |
    |**MESSAGECLASS** <br/> |예  <br/> | 이 속성은 이미 만들어져 파트너 커넥터에 의해 채워진 하는 다중값 속성입니다. 이 속성의 형식은 `IPM.NOTE.Source.Event`합니다. (이 속성은로 시작 되어야 `IPM.NOTE`,이 형식에 대 한 것과 비슷합니다는 `IPM.NOTE.X` 메시지 클래스입니다.) 이 속성에는 다음 정보가 포함 됩니다.<br/><br/>`Source`-제 3 자 데이터 원본;를 나타냅니다. 예: Twitter, Facebook, 또는 BlackBerry 합니다.  <br/> <br/>  `Event`-; 항목을 생성 하는 타사 데이터 원본에서 수행 된 활동의 종류를 나타냅니다. 예, Facebook에서 게시 하거나 Twitter에서 소리입니다. 이벤트는 데이터 원본에 따라 다릅니다.<br/> <br/>  이 속성의 용도 항목을 유발한 또는 이벤트의 형식에 따라 여기에서 데이터 원본을 기초로 하는 특정 항목을 필터링 하는 것입니다. 예, eDiscovery 검색에서 특정 사용자가 게시 된 모든 tweets 찾으려고 검색 쿼리를 만들 수 있습니다.<br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- Office 365에서 사서함에 항목이 성공적으로 가져온 고유 식별자를 HTTP 응답의 일부로 호출자에 게 반환 됩니다. 이 식별자-라는 `x-IngestionCorrelationID`-항목의 끝-추적을 위한 파트너에 의해 후속 문제해결 목적을 위해 사용할 수 있습니다. 파트너가이 정보를 캡처 및 그에 따라 기록 것이 좋습니다 끝에서 합니다. 이 식별자를 표시 하는 HTTP 응답의 예는 다음과 같습니다.

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- 콘텐츠 검색 도구를 사용 하 여 Office 365 보안에서 수 &amp; 준수 센터 타사 데이터 원본에서 Office 365에서 사서함에 가져온 항목을 찾으려고 합니다. 특히 이러한 가져온된 항목을 검색 하려면 콘텐츠 검색에 대 한 키워드 상자에는 다음과 같은 메시지 속성-값 쌍을 사용할 수 있습니다. . 
    
  - **`kind:externaldata`**-모든 타사 데이터 형식을 검색 하려면이 속성 값 쌍을 사용 합니다. 예, 제 3 자 데이터 원본에서 가져온 하 고 가져온된 항목의 Subject 속성에 "contoso" 라는 단어를 포함 하는 항목을 검색 하려면 있습니다 사용 키워드 쿼리 `kind:externaldata AND subject:contoso`합니다.
    
  - **`itemclass:ipm.externaldata.<third-party data type>`**-지정 형식의 제 3 자 데이터를 검색만이 속성 값 쌍을 사용 합니다. 예, 하려면 Subject 속성에 사용 되는 "contoso" 라는 단어를 포함 하는 Facebook 데이터를 검색만 사용 키워드 쿼리 `itemclass:ipm.externaldata.Facebook* AND subject:contoso`합니다. 

  타사 데이터 형식을 사용 하 여 값의 전체 목록은 `itemclass` 속성을 [검색 하는 Office 365로 가져온 제 3 자 데이터를 사용 하 여 콘텐츠 검색](use-content-search-to-search-third-party-data-that-was-imported.md) 을 참조 하십시오
    
   콘텐츠 검색 사용 및 키워드 검색 쿼리를 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.
    
  - [Office 365의에서 콘텐츠 검색](content-search.md)
    
  - [콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건](keyword-queries-and-search-conditions.md)
 
