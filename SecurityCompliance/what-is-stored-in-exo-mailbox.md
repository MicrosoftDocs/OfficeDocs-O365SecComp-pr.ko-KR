---
title: Exchange Online 사서함에 저장 된 콘텐츠
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
description: Office 365에서 클라우드 기반 앱에 의해 생성 된 데이터는 Microsoft 클라우드의 사용자 Exchange Online 사서함에 저장 됩니다.
ms.openlocfilehash: 6f7a81842df5972a03648a2f93d4bd6fbd738fec
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32266900"
---
# <a name="content-stored-in-exchange-online-mailboxes"></a>Exchange Online 사서함에 저장 된 콘텐츠

Exchange Online의 사서함은 주로 메시지, 일정 항목, 작업 및 메모와 같은 전자 메일 관련 항목을 저장 하는 데 사용 됩니다. 하지만 클라우드 기반 Office 365 앱 에서도 사용자 사서함에 데이터를 저장 하는 것이 좋습니다. 사서함에 데이터를 저장 하는 경우의 한 가지 이점은 콘텐츠 검색, eDiscovery, 고급 eDiscovery 및 데이터 조사에서 검색 도구를 사용 하 여 이러한 클라우드 기반 앱에서 데이터를 찾고, 보고, 내보낼 수 있다는 것입니다. 이러한 앱 중 일부의 데이터는 사서함의 비 IPM 메시지 하위 트리에 있는 숨겨진 폴더에 저장 됩니다. 즉, 사용자가 Outlook 또는 다른 메일 클라이언트를 사용 하 여 자신의 사서함에 액세스 하는 경우 해당 데이터는 해당 보기에서 숨겨집니다.

다음 표에는 클라우드 기반 사서함에 데이터를 저장 하는 Office 365 앱이 나와 있습니다. 이 표에서는 각 앱이 저장 하는 콘텐츠 형식에 대해서도 설명 합니다.

|Office 365 앱  |설명  |
|:---------|:---------|
|양식     <br/> |양식 (PDF 파일로 저장)과 양식 (CSV 파일에 저장 됨)에 대 한 응답은 전자 메일 메시지에 첨부 되 고 양식을 만든 사용자의 사서함에 있는 숨겨진 폴더에 저장 됩니다. PST 파일의 양식에서 콘텐츠를 내보낼 때이 데이터는 다음과 같은 guid (globally unique identification)를 사용 하 여 이름이 지정 된 하위 폴더의 **ApplicationDataRoot** 폴더에 있습니다. ****        <br/> |
|MyAnalytics    <br/> |   myanalytics 사용자에 게 자신의 사서함에 있는 메일 및 일정 데이터를 기반으로 시간을 보내는 방법을 설명 합니다. 이 데이터는 사용자 사서함의 숨겨진 폴더에 저장 됩니다. myanalytics 데이터 및 내보내는 방법에 대 한 자세한 내용은 [myanalytics에서 데이터 내보내기를](manage-gdpr-data-subject-requests-with-the-dsr-case-tool.md#exporting-data-from-myanalytics-and-the-office-roaming-service)참조 하십시오.      <br/> |
|Office 365 그룹    <br/>|  전자 메일 메시지, 일정 항목, 연락처 (사용자), 메모 및 작업은 Office 365 그룹과 연결 된 사서함에 저장 됩니다.       <br/> |
|Outlook/Exchange Online<br/>|  전자 메일 메시지, 일정 항목, 연락처 (사용자), 메모 및 작업은 사용자의 사서함에 저장 됩니다.       <br/> |
|People    <br/> |  사용자 앱 (Outlook에서 액세스할 수 있는 연락처와 같은 대화 상대 응용 프로그램)의 대화 상대는 user의 사서함에 저장 됩니다.      <br/> |
|Planner     <br/> |   Planner에서 만든 요금제는 새 요금제를 만들 때 프로 비전 되는 해당 Office 365 그룹의 사서함에 저장 됩니다. 그룹 사서함의 별칭은 계획의 이름입니다.      <br/> |
|비즈니스용 Skype    <br/>  | 비즈니스용 Skype의 대화는 사용자 사서함의 대화 내용 폴더에 저장 됩니다. Skype 모임 참가자의 사서함을 소송 보존으로 설정 하거나 보관 정책에 할당 하는 경우 모임에 첨부 된 파일이 참가자 사서함에 보존 됩니다.         <br/> |
|Sway     <br/> |  sway는 전자 메일 메시지에 첨부 되 고 sway를 만든 사용자의 사서함에 있는 숨겨진 폴더에 저장 되는 HTML 파일로 저장 됩니다. PST 파일의 Sway에서 콘텐츠를 내보낼 때이 데이터는 다음 GUID로 이름이 지정 된 하위 폴더의 **ApplicationDataRoot** 폴더에 있습니다 **905fcf26-4eb7-48a0-9ff0-8dcc7194b5ba**합니다.       <br/> |
|작업    <br/> |  작업 앱 (Outlook에서 액세스할 수 있는 작업과 같은 작업)의 작업은 사용자의 사서함에 저장 됩니다.       <br/> |
|Teams    <br/>  |팀 채널의 일부인 대화는 팀과 연결 된 사서함에 저장 됩니다. 팀에서 채팅 목록의 일부인 대화 ( *1 x N 채팅*이 라고도 함)는 채팅에 참가 하는 사용자의 사서함에 저장 됩니다. 또한 팀 채널의 모임 및 통화에 대 한 요약 정보는 모임 또는 통화에 전화를 거는 사용자의 사서함에 저장 됩니다. <br/> | 
|To-Do  <br/> | 할 일 앱에 있는-do 목록에 저장 되는 작업 ( *dos*로 호출 됨)은 사용자의 사서함에 저장 됩니다.        <br/> |
||||

> [!NOTE]
> 현재, 고급 eDiscovery (미리 보기)에서 custodian 사서함에 보류가 설정 된 경우 양식 및 Sway의 콘텐츠가 보류에 의해 보존 되지 않습니다. 