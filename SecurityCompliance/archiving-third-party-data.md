---
title: Office 365에서 타사 데이터 보관
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: '관리자는 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 Office 365 조 직의 사서함으로 타사 데이터를 가져올 수 있습니다. 이를 통해 Office 365의 Facebook, Twitter 및 데이터 원본에서 데이터를 보관할 수 있습니다. 그런 다음 Office 365 규정 준수 기능 (예: 법적 보존, 콘텐츠 검색 및 보존 정책)을 타사 데이터에 적용할 수 있습니다.'
ms.openlocfilehash: 6e5f40328c54a6f2c97cb6cfe14a1bc5727ae087
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32249614"
---
# <a name="archiving-third-party-data-in-office-365"></a>Office 365에서 타사 데이터 보관

관리자는 office 365을 사용 하 여 소셜 미디어 플랫폼, 인스턴트 메시징 플랫폼 및 문서 공동 작업 플랫폼에서 타사 데이터를 가져오고 office 365 조직의 사서함으로 보관할 수 있습니다. Office 365로 가져올 수 있는 타사 데이터 원본의 예는 다음과 같습니다. 
  
- **교류** -Twitter, Facebook, Yammer 및 LinkedIn 
    
- **인스턴트 메시징** -Yahoo Messenger, GoogleTalk 및 Cisco jabber 
    
- **문서 공동 작업** 상자 및 DropBox 
    
- **세로 산업** -고객 관계 관리 (예: Salesforce Chatter) 및 금융 서비스 (예:: thomson reuters 및 Bloomberg) 
    
- **SMS/텍스트 메시징** -BlackBerry 
    
타사 데이터를 가져온 후에는이 데이터에 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사 및 office 365 보존 정책 등의 office 365 준수 기능을 적용할 수 있습니다. 예를 들어 사서함에 소송 보존이 적용되면 타사 데이터가 보존됩니다. 콘텐츠 검색을 사용 하 여 타사 데이터를 검색할 수 있습니다. 또는 Microsoft 데이터의 경우처럼 타사 데이터에도 보관 및 삭제 정책을 적용할 수 있습니다. 간단히 말해서 Office 365에서 타사 데이터를 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.
  
타사 데이터를 Office 365로 가져오는 데 필요한 프로세스 및 단계의 개요는 다음과 같습니다.

[Step 1: Find a third-party data partner](#step-1-find-a-third-party-data-partner)

[Step 2: Create and configure a third-party data mailbox in Office 365](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[Step 3: Configure user mailboxes for third-party data](#step-3-configure-user-mailboxes-for-third-party-data)

[4단계: 파트너에게 정보 제공](#step-4-provide-your-partner-with-information)

[5 단계: Azure Active Directory에서 타사 데이터 커넥터 등록](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a>타사 데이터 가져오기 프로세스의 작동 방식

다음 그림과 설명은 타사 데이터 가져오기 프로세스의 작동 방식에 대해 설명합니다.
  
![타사 데이터 가져오기 프로세스의 작동 방식](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. 고객은 선택한 파트너와 함께 작업 하 여 타사 데이터 원본에서 항목을 추출 하 고 해당 항목을 Office 365로 가져오는 커넥터를 구성 합니다.
    
2. 파트너 커넥터가 타사 API (예약 또는 구성 된 기준)를 통해 타사 데이터 원본에 연결 하 고 데이터 원본에서 항목을 추출 합니다. 파트너 커넥터는 항목의 내용을 전자 메일 메시지 형식으로 변환합니다. 메시지 형식 스키마에 대한 설명을 보려면 [More information](#more-information)를 참조하세요. 
    
3. 파트너 커넥터는 잘 알려진 끝점을 통해 EWS (Exchange 웹 서비스)를 사용 하 여 Office 365의 Azure 서비스에 연결 합니다.
    
4. 항목은 특정 사용자의 사서함 또는 "범용" 타사 데이터 사서함으로 가져오기됩니다. 항목을 특정 사용자 사서함으로 가져올지 또는 타사 데이터 사서함으로 가져올지는 다음 기준을 기반으로 합니다.
    
    위한. **office 365 사용자 계정에 해당 하는 사용자 id** 가 있는 항목-파트너 커넥터가 타사 데이터 원본 항목의 사용자 id를 office 365의 특정 사용자 id에 매핑할 수 있는 경우 해당 항목은 사용자의 Rec에 있는 **제거** 폴더에 복사 됩니다. 과잉 항목 폴더 제거 폴더의 항목에는 액세스할 수 없습니다. 그러나 Office 365 eDiscovery 도구를 사용 하 여 제거 폴더에서 항목을 검색할 수는 있습니다.
    
    b. **office 365 사용자 계정에 해당 하는 사용자 id** 가 없는 항목-파트너 커넥터가 항목의 사용자 id를 office 365의 특정 사용자 id에 매핑할 수 없는 경우 항목은 타사 데이터 사서함의 **받은 편지함** 폴더에 복사 됩니다. 받은 편지함에 항목을 가져올 수 있으면 관리자 또는 조직의 누군가가 타사 사서함에 로그인하여 이러한 항목을 보고 관리할 수 있으며 파트너 커넥터 구성을 조정해야 하는지 확인할 수 있습니다.
 
## <a name="step-1-find-a-third-party-data-partner"></a>1단계: 타사 데이터 파트너 찾기

office 365에서 타사 데이터를 보관 하기 위한 주요 구성 요소는 타사 데이터 원본에서 데이터를 캡처하고 office 365로 가져오는 Microsoft 파트너를 찾고 사용 하는 것입니다. 데이터를 가져온 후에는 조직의 다른 Microsoft 데이터 (예: Exchange의 전자 메일, SharePoint의 문서 및 비즈니스용 OneDrive)와 함께 보관 하 고 보존할 수 있습니다. 파트너는 조직의 타사 데이터 원본 (예: BlackBerry, Facebook, Google +,: thomson reuters, Twitter)에서 데이터를 추출 하는 커넥터를 만들고 해당 데이터를 Exchange 사서함으로 항목을 가져오는 Office 365 API에 전달 합니다. 전자 메일 메시지 
  
다음 섹션에서는 Office 365에서 타사 데이터를 보관 하기 위한 프로그램에 참여 하는 Microsoft 파트너 및 지원 되는 타사 데이터 원본에 대해 설명 합니다.

[17a-4 LLC](#17a-4-llc)
  
[Actiance](#actiance)
  
[ArchiveSocial](#archivesocial)
  
[Globanet](#globanet)
  
[OpenText](#opentext)
  
[verba](#verba)
  
### <a name="17a-4-llc"></a>17a-4 LLC

17a-4 LLC에서는 다음의 타사 데이터 원본을 지원합니다.
  
- BlackBerry
    
- Bloomberg Data Streams
    
- Cisco Jabber
    
- FactSet
    
- HipChat
    
- InvestEdge
    
- LivePerson
    
- MessageLabs Data Streams
    
- OpenText
    
- Oracle/ATG 'click-to-call' Live Help
    
- Pivot IMTRADER
    
- Microsoft SharePoint
    
- MindAlign
    
- Sitrion One(Newsgator)
    
- 비즈니스용 Skype(Lync/OCS)
    
- 비즈니스용 Skype Online(Lync Online)
    
- SQL 데이터베이스
    
- Squawker
    
- Thomson Reuters Eikon Messenger
  
### <a name="actiance"></a>Actiance

[Actiance](https://www.actiance.com) 에서는 다음의 타사 데이터 원본을 지원 합니다. 
  
- AIM
    
- American Idol
    
- Apple Juice
    
- AOL with Pivot client
    
- Ares
    
- Bazaar Voice
    
- Bear Share
    
- Bit Torrent
    
- BlackBerry Call Logs(v5, v10, v12)
    
- BlackBerry Messenger(v5, v10, v12)
    
- BlackBerry PIN(v5, v10, v12)
    
- BlackBerry SMS(v5, v10, v12)
    
- Bloomberg Mail
    
- 셀 신뢰
    
- Chat Import
    
- Chat Real Time Logging and Policy
    
- Chatter
    
- Cisco IM &amp; 현재 상태 서버 (v 9.0.1, v 9.1, v 9.1.1 SU1, v10, v 10.5.1 SU1)
    
- Cisco Unified Presence Server(v8.6.3, v8.6.4, v8.6.5)
    
- Collaboration Import
    
- Collaboration Real Time Logging
    
- Direct Connect
    
- Facebook
    
- FactSet
    
- FastTrack
    
- Gnutella
    
- Google +
    
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
    
- 아이스/YellowJacket
    
- IM Import
    
- IM Real Time Logging and Policy
    
- Indii Messenger
    
- Instant Bloomberg
    
- IRC
    
- Jive
    
- Jive 6 Real Time Logging(v6, v7)
    
- Jive Import
    
- jxta
    
- LinkedIn
    
- Microsoft Lync(2010, 2013)
    
- mftp
    
- Microsoft Lync 2013 Voice
    
- Microsoft SharePoint(2010, 2013)
    
- Microsoft SharePoint Online
    
- Microsoft UC(Unified Communications)
    
- MindAlign
    
- Mobile Guard
    
- 수신
    
- My Space
    
- NEONetwork
    
- Office 365 Lync Dedicated
    
- Office 365 Shared IM
    
- 유 이율
    
- Pivot
    
- qq
    
- 비즈니스용 Skype 2015
    
- SoftEther
    
- Symphony
    
- Thomson Reuters Eikon
    
- Thomson Reuters Messenger
    
- 한자
    
- TTT
    
- Twitter
    
- winmx
    
- winny
    
- Yahoo
    
- Yammer
    
- YouTube
    
  
### <a name="archivesocial"></a>ArchiveSocial

[ArchiveSocial](https://www.archivesocial.com) 에서는 다음의 타사 데이터 원본을 지원 합니다. 
  
- Facebook
    
- Flickr
    
- 명령이 있는 agram
    
- LinkedIn
    
- 유 이율
    
- Twitter
    
- YouTube
    
- Vimeo
  
### <a name="globanet"></a>Globanet

[Globanet](https://www.globanet.com) 에서는 다음의 타사 데이터 원본을 지원 합니다. 
  
- AOL with Pivot Client  
    
- BlackBerry Call Logs(v5, v10, v12)
    
- BlackBerry Messenger(v5, v10, v12)
    
- BlackBerry PIN(v5, v10, v12)
    
- BlackBerry SMS(v5, v10, v12)
    
- Bloomberg Chat
    
- Bloomberg Mail
    
- Box
    
- CipherCloud for Salesforce Chatter
    
- Cisco IM &amp; 현재 상태 서버 (v10, v 10.5.1 SU1, v 11.0, v 11.5 SU2)

- Cisco Webex 팀

- Citrix 작업 &amp; 영역 sharefile

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

[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) 에서는 다음의 타사 데이터 원본을 지원 합니다. 
  
- Axs Encrypted
    
- Axs Exchange
    
- Axs Local Archive
    
- Axs PlaceHolder
    
- Axs Signed
    
- Bloomberg
    
- Thomson Reuters
  
### <a name="verba"></a>verba

[verba](https://www.verba.com) 는 다음 타사 데이터 원본을 지원 합니다. 
  
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
    
- Cisco c s p/c h i v 비디오
    
- Cisco c s p/c h 음성
    
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

다음은 Office 365로 데이터를 가져오기 위한 타사 데이터 사서함을 만들고 구성 하는 단계입니다. 앞에서 설명한 것 처럼 파트너 커넥터에서 항목의 사용자 ID를 Office 365 사용자 계정에 매핑할 수 없는 경우에는이 사서함으로 항목을 가져옵니다.
  
 **Microsoft 365 관리 센터에서이 작업 완료**
  
1. Office 365에서 새 사용자 계정을 만들고이 계정에 Exchange Online 계획 2 라이선스를 할당 합니다. [Office 365에 사용자 추가를](https://go.microsoft.com/fwlink/p/?LinkId=692098)참조 하세요. 계획 2 라이선스는 사서함을 소송 보존 상태로 설정 하거나 저장소 할당량이 무제한 인 보관 사서함을 사용 하는 데 필요 합니다.
    
2. 타사 데이터 사서함에 대 한 사용자 계정을 Office 365의 **Exchange 관리자** 관리자 역할에 추가 합니다. [Office 365에서 관리자 역할 할당을](https://go.microsoft.com/fwlink/p/?LinkId=532393)참조 하세요.
    
    > [!TIP]
    > 이 사용자 계정의 자격 증명을 기록해 둡니다. 4단계에서 설명한 것처럼 파트너에게 제공해야 합니다. 
  
 **Exchange 관리 센터에서 다음 작업 완료**
  
1. 조직의 주소록 및 기타 주소 목록에서 타사 데이터 사서함을 숨깁니다. [사용자 사서함 관리](https://go.microsoft.com/fwlink/p/?LinkId=616058)를 참조 하세요. 또는 다음 PowerShell 명령을 실행할 수 있습니다.
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. administrators 또는 규정 준수 관리자가 Outlook 데스크톱 클라이언트에서 타사 데이터 사서함을 열 수 있도록 타사 데이터 사서함에 대 한 **FullAccess** 권한을 할당 합니다. [받는 사람의 사용 권한 관리를](https://go.microsoft.com/fwlink/p/?LinkId=692104)참조 하세요.
    
3. 타사 데이터 사서함에 대해 다음과 같은 준수 관련 Office 365 기능을 사용 하도록 설정 합니다.
    
    - 보관 사서함을 사용 하도록 설정 합니다. [보관 사서함 사용](enable-archive-mailboxes.md) 및 [무제한 보관 사용](enable-unlimited-archiving.md)을 참조 하세요. 이렇게 하면 타사 데이터 항목을 보관 사서함으로 이동 하는 보관 정책을 설정 하 여 기본 사서함에서 저장소 공간을 확보할 수 있습니다. 이렇게 하면 타사 데이터에 대 한 무제한 저장소를 제공할 수 있습니다.
    
    - 타사 데이터 사서함에 소송 보존을 적용합니다. 보안 및 준수 센터에서 Office 365 보존 정책을 적용할 수도 있습니다. 이 사서함을 보존 상태로 두면 타사 데이터 항목 (무기한 또는 지정 된 기간 동안)이 유지 되 고 사서함에서 해당 항목이 제거 되는 것을 방지할 수 있습니다. 다음 항목 중 하나를 참조 하세요.
    
      - [소송 보존 만들기](create-a-litigation-hold.md)
    
      - [Office 365의 보존 정책 개요](retention-policies.md)
    
       
    
    - 타사 데이터 사서함에 대 한 소유자, 대리인 및 관리자 액세스에 대 한 사서함 감사 로깅을 사용 하도록 설정 합니다. [Office 365에서 사서함 감사 사용을](enable-mailbox-auditing.md)참조 하세요. 이렇게 하면 타사 데이터 사서함에 대 한 액세스 권한이 있는 모든 사용자가 수행한 모든 작업을 감사할 수 있습니다.

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a>3단계: 타사 데이터에 대한 사용자 사서함 구성

다음 단계는 타사 데이터를 지원하도록 사용자 사서함을 구성하는 것입니다. Exchange 관리 센터를 사용 하거나 해당 Windows PowerShell cmdlet을 사용 하 여 이러한 작업을 완료 합니다.
  
1. 각 사용자에 대해 보관 사서함을 사용 하도록 설정 합니다. [보관 사서함 사용](enable-archive-mailboxes.md) 및 [무제한 보관 사용](enable-unlimited-archiving.md)을 참조 하세요.
    
2. 사용자 사서함을 소송 보존으로 설정 하거나 Office 365 보관 정책을 적용 합니다. 다음 항목 중 하나를 참조 하세요. 
    
    - [소송 보존 만들기](create-a-litigation-hold.md)
    
    - [Office 365의 보존 정책 개요](retention-policies.md)
    
    앞서 언급한 것처럼 사서함을 보존하면 타사 데이터 원본의 항목을 보존하는 기간을 설정하거나 항목을 무기한 보존하도록 선택할 수 있습니다.

## <a name="step-4-provide-your-partner-with-information"></a>4단계: 파트너에게 정보 제공

마지막 단계는 Office 365 조직에 연결하여 사용자 사서함이나 타사 데이터 사서함으로 데이터를 가져오도록 커넥터를 구성할 수 있게 파트너에게 다음 정보를 제공하는 것입니다. 
  
- Office 365에서 Azure 서비스에 연결 하는 데 사용 되는 끝점:

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- 2 단계에서 만든 타사 데이터 사서함의 로그인 자격 증명 (Office 365 사용자 ID 및 암호)입니다. 이러한 자격 증명은 파트너 커넥터가 항목을 액세스하고 사용자 사서함 및 타사 데이터 사서함으로 가져올 수 있도록 하는 데 필요합니다.
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a>5 단계: Azure Active Directory에서 타사 데이터 커넥터 등록

2018 년 9 월 30 일부부터 office 365의 Azure service는 Exchange Online의 최신 인증을 사용 하 여 데이터를 가져오기 위해 office 365 조직에 연결을 시도 하는 타사 데이터 커넥터를 인증 합니다. 이러한 변경이 발생 하는 이유는 최신 인증이 이전에 설명한 끝점을 사용 하 여 Azure 서비스에 연결 하는 허용 목록이 타사 커넥터를 기반으로 하는 현재 방법 보다 더 많은 보안 기능을 제공 한다는 것입니다.

최신 인증 방법을 사용 하 여 타사 데이터 커넥터가 office 365에 연결 되도록 하려면 office 365 조직의 관리자가 해당 커넥터를 Azure Active Directory의 신뢰할 수 있는 서비스 응용 프로그램으로 등록 하는 것이 동의 해야 합니다. 이 작업은 사용 권한 요청을 수락 하 여 커넥터가 Azure Active Directory에서 조직의 데이터에 액세스할 수 있도록 허용 합니다. 이 요청을 수락 하면 타사 데이터 커넥터가 엔터프라이즈 응용 프로그램으로 Azure Active Directory에 추가 되 고 서비스 사용자로 표시 됩니다. 승인 프로세스에 대 한 자세한 내용은 [테 넌 트 관리자 동의](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent)를 참조 하십시오.

커넥터 등록을 위한 요청에 액세스 하 고 수락 하는 단계는 다음과 같습니다.

1. [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) 이동 하 여 Office 365 전역 관리자의 자격 증명을 사용 하 여 로그인 합니다.<br/><br/>다음 대화 상자가 표시 됩니다. carets를 확장 하 여 커넥터에 할당 되는 사용 권한을 검토할 수 있습니다.<br/><br/>![사용 권한 요청 대화 상자가 표시 됩니다.](media/O365_ThirdPartyDataConnector_OptIn1.png)
2. **Accept(동의함)** 를 클릭합니다.

요청을 수락 하면 [Azure portal](https://portal.azure.com) 이 표시 됩니다. 조직의 응용 프로그램 목록을 보려면 **Azure Active Directory** > **Enterprise 응용 프로그램**을 클릭 합니다. Office 365 타사 데이터 커넥터가 **엔터프라이즈 응용 프로그램** 블레이드에서 나열 됩니다.

> [!IMPORTANT]
> Azure Active Directory에 타사 데이터 커넥터를 등록 하지 않으면, 2018 년 9 월 30 일 이후에는 타사 데이터를 조직의 사서함으로 가져올 수 없게 됩니다. 참고 5 단계에 나와 있는 절차에 따라 기존 타사 데이터 커넥터 (9 월 30 일 이전에는 2018)도 Azure Active Directory에 등록 되어 있어야 합니다.

### <a name="revoking-consent-for-a-third-party-data-connector"></a>타사 데이터 커넥터에 대 한 동의 해지

조직이 Azure Active Directory에서 타사 데이터 커넥터를 등록 하기 위해 권한 요청을 consents 후에는 조직에서 언제 든 지 해당 동의를 해지할 수 있습니다. 그러나 커넥터에 대 한 동의를 취소 하면 타사 데이터 원본의 데이터를 더 이상 Office 365로 가져올 수 없습니다.

타사 데이터 커넥터에 대 한 동의를 해지 하려면 azure portal에서 **엔터프라이즈 응용 프로그램** 블레이드를 사용 하 여 azure Active Directory에서 해당 서비스 사용자를 삭제 하거나, 다음을 [사용 하 여 응용 프로그램을 삭제 하면 됩니다. Remove-(new-msolserviceprincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. Azure Active Directory PowerShell에서 [AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet을 사용할 수도 있습니다.
  
## <a name="more-information"></a>추가 정보

- 앞서 설명한 것처럼 타사 데이터 원본의 항목을 Exchange 사서함에 전자 메일 메시지로 가져옵니다. 파트너 커넥터는 Office 365 API에 필요한 스키마를 사용 하 여 항목을 가져옵니다. 다음 표에서는 타사 데이터 원본 항목을 Exchange 사서함에 전자 메일 메시지로 가져온 후, 타사 데이터 원본 항목에 대한 메시지 속성을 설명합니다. 또한 이 표는 메시지 속성이 필수인지 여부를 나타냅니다. 필수 속성은 채워야 합니다. 항목에 필수 속성이 없는 경우에는 Office 365로 가져올 수 없습니다. 가져오기 프로세스는 항목을 가져오지 않은 이유와 누락된 속성을 설명하는 오류 메시지를 반환합니다.
    
    |**메시지 속성**|**강제?**|**설명**|**예제 값**|
    |:-----|:-----|:-----|:-----|
    |**보낸 사람** <br/> |예  <br/> |타사 데이터 원본 항목을 처음 만들었거나 보낸 사람입니다. 파트너 커넥터는 원본 항목 (예: Twitter 핸들)의 사용자 ID를 모든 참가자 (시작 및 대상 필드의 사용자)에 대 한 Office 365 사용자 계정에 매핑하도록 시도 합니다. 메시지 복사본을 모든 참가자의 사서함으로 가져옵니다. 항목의 참가자가 office 365 사용자 계정에 매핑할 수 없는 경우에는 office 365에서 타사 보관 사서함으로 항목을 가져옵니다.  <br/> <br/> 항목을 보낸 사람으로 식별 된 참석자는 해당 항목을 가져올 Office 365 조직의 활성 사서함이 있어야 합니다. 보낸 사람에게 활성 사서함이 없으면 다음과 같은 오류가 반환됩니다.<br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |**받는 사람** <br/> |예  <br/> |데이터 원본의 항목을 받은 사람입니다(해당되는 경우).  <br/> | `bob@contoso.com` <br/> |
    |**제목** <br/> |아니요  <br/> |원본 항목의 제목입니다.  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |**종료일** <br/> |예  <br/> |항목을 처음 만들었거나 고객 데이터 원본에 게시한 날짜입니다. 예로 Twitter 메시지가 트윗된 날짜가 있습니다.  <br/> | `01 NOV 2015` <br/> |
    |**보내기** <br/> |아니요  <br/> |메시지 또는 게시물의 콘텐츠입니다. 일부 데이터 원본의 경우 이 속성의 콘텐츠는 **SUBJECT** 속성의 콘텐츠와 같을 수 있습니다. 가져오기 프로세스 동안 파트너 커넥터는 콘텐츠 원본의 충실도를 최대한 유지하려고 합니다. 가능한 경우 원본 항목의 본문에서 가져온 파일, 그래픽 또는 기타 콘텐츠가 이 속성에 포함됩니다. 그렇지 않은 경우 원본 항목의 콘텐츠가 **ATTACHMENT** 속성에 포함됩니다. 이 속성의 내용은 파트너 커넥터와 원본 플랫폼의 기능에 따라 달라 집니다.  <br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |**덧붙인** <br/> |아니요  <br/> |데이터 원본의 항목 (예: Twitter 또는 인스턴트 메시징 대화에 있는 tweet)에 첨부 된 파일이 있거나 이미지를 포함 하는 경우, 파트너 연결에서는 먼저 **BODY** 속성에 첨부 파일을 포함 하 려 합니다. 이것이 가능 하지 않으면 * * ATTACHMENT * * 속성에 추가 됩니다. 첨부 파일의 다른 예로는 Facebook의 좋아요, 콘텐츠 원본의 메타데이터, 메시지 또는 게시물에 대한 응답이 있습니다.  <br/> | `image.gif` <br/> |
    |**MESSAGECLASS** <br/> |예  <br/> | 파트너 커넥터가 만들어서 채우는 다중 값 속성입니다. 이 속성의 형식은 `IPM.NOTE.Source.Event`입니다. (이 속성은 다음으로 `IPM.NOTE`시작 해야 합니다 .이 형식은 `IPM.NOTE.X` message 클래스의 형식과 유사 합니다.) 이 속성에는 다음 정보가 포함 됩니다.  <br/><br/>`Source`-타사 데이터 원본을 나타냅니다. 예: Twitter, Facebook 또는 BlackBerry를 예로 들 있습니다.  <br/> <br/>  `Event`-항목을 생성 한 타사 데이터 원본에서 수행한 작업 유형을 나타냅니다. 예를 들어, Twitter에 있는 tweet 또는 Facebook의 게시물입니다. 이벤트는 데이터 원본에 따라 다릅니다.  <br/> <br/>  이 속성의 한 가지 목적은 항목이 시작된 데이터 원본이나 이벤트의 유형에 따라 특정 항목을 필터링하는 것입니다. 예를 들어 eDiscovery 검색에서 특정 사용자가 게시한 모든 트윗을 찾는 검색 쿼리를 만들 수 있습니다.  <br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- Office 365에서 사서함에 항목을 성공적으로 가져오면 고유한 식별자가 HTTP 응답의 일부로 다시 발신자에 게 반환 됩니다. 이 식별자 `x-IngestionCorrelationID`는 종단 간 항목 추적을 위해 파트너가 제공 하는 후속 문제 해결을 위해 사용 될 수 있습니다. 파트너는 이 정보를 수집하고 적절하게 기록해두는 것이 좋습니다. 이 식별자를 나타내는 HTTP 응답의 예는 다음과 같습니다.

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- 보안 및 준수 센터의 콘텐츠 검색 도구를 사용 하 여 타사 데이터 원본에서 Office 365의 사서함으로 가져온 항목을 검색할 수 있습니다. 이러한 가져온 항목을 구체적으로 검색 하려면 콘텐츠 검색의 키워드 상자에 다음과 같은 메시지 속성-값 쌍을 사용할 수 있습니다.
    
  - **`kind:externaldata`**-이 속성-값 쌍을 사용 하 여 모든 타사 데이터 형식을 검색 합니다. 예를 들어 타사 데이터 원본에서 가져온 항목과 가져온 항목의 Subject 속성에 "contoso" 라는 단어가 포함 된 항목을 검색 하려면 keyword 쿼리 `kind:externaldata AND subject:contoso`를 사용 합니다.
    
  - **`itemclass:ipm.externaldata.<third-party data type>`**-이 속성-값 쌍을 사용 하 여 지정 된 타사 데이터 형식만 검색 합니다. 예를 들어 Subject 속성에서 "contoso" 라는 단어가 포함 된 Facebook 데이터만 검색 하려면 keyword 쿼리 `itemclass:ipm.externaldata.Facebook* AND subject:contoso`를 사용 합니다. 

  `itemclass` 속성의 타사 데이터 형식에 사용할 값의 전체 목록은 [Office 365로 가져온 타사 데이터 검색을 사용 하 여 콘텐츠 검색](use-content-search-to-search-third-party-data-that-was-imported.md) 을 참조 하세요.
    
   콘텐츠 검색 사용 및 키워드 검색 쿼리를 만드는 방법에 대한 자세한 내용은 다음을 참조하세요.
    
  - [Office 365의 콘텐츠 검색](content-search.md)
    
  - [콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건](keyword-queries-and-search-conditions.md)
 
