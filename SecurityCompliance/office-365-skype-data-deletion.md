---
title: 비즈니스 데이터 삭제에 대 한 office 365 Skype
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 비즈니스를 위한 Skype에서 데이터 삭제는를 설명 합니다.
ms.openlocfilehash: f3ddd0ad0797c465857919e8f7b28341492769ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533751"
---
# <a name="skype-for-business-data-deletion-in-office-365"></a><span data-ttu-id="ed6f1-103">Office 365의에서 비즈니스 데이터 삭제 용 Skype</span><span class="sxs-lookup"><span data-stu-id="ed6f1-103">Skype for Business Data Deletion in Office 365</span></span>

<span data-ttu-id="ed6f1-p101">비즈니스를 위한 Skype 피어-투-피어 인스턴트 메시지, 단체 인스턴트 메시지 및 모임에 콘텐츠 업로드 활동의 보관을 제공 합니다. 보관 기능 Exchange 필요 하 고 사용자의 Exchange 사서함 원본 위치 유지 특성으로, 비즈니스 내용에 대 한 전자 메일 및 Skype 모두 보관 하는 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p101">Skype for Business provides archiving of peer-to-peer instant messages, multiparty instant messages, and content upload activities in meetings. The archiving capability requires Exchange and is controlled by the user's Exchange mailbox In-Place Hold attribute, which archives both email and Skype for Business contents.</span></span>

<span data-ttu-id="ed6f1-p102">비즈니스를 위한 Skype에서 모든 보관 것으로 간주 됩니다 "사용자 수준 보관"를 사용 하도록 설정 하거나, 구성, 만들고 이러한 사용자에 대 한 사용자 수준의 보관 정책을 적용 하 여 하나 이상의 특정 사용자 또는 사용자 그룹에 대 한 비활성화 하기 때문에 있습니다. 비즈니스 관리 센터에 대 한 Skype 내에서 보관 설정의 직접적인 제어 되지 않음</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p102">All archiving in Skype for Business is considered "user-level archiving" because you enable or disable it for one or more specific users or groups of users by creating, configuring, and applying a user-level archiving policy for those users. There is no direct control of archiving settings from within the Skype for Business admin center.</span></span>

<span data-ttu-id="ed6f1-108">비즈니스를 위한 Skype에는 다음과 같은 유형의 콘텐츠를 보관 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-108">The following types of content are not archived in Skype for Business:</span></span> 
- <span data-ttu-id="ed6f1-109">피어 투 피어 파일 전송</span><span class="sxs-lookup"><span data-stu-id="ed6f1-109">Peer-to-peer file transfers</span></span>
- <span data-ttu-id="ed6f1-110">피어 투 피어 메신저 메시지 및 전화 회의 오디오/비디오</span><span class="sxs-lookup"><span data-stu-id="ed6f1-110">Audio/video for peer-to-peer instant messages and conferences</span></span>
- <span data-ttu-id="ed6f1-111">피어 투 피어 메신저 메시지 및 전화 회의 응용 프로그램 공유</span><span class="sxs-lookup"><span data-stu-id="ed6f1-111">Application sharing for peer-to-peer instant messages and conferences</span></span>
- <span data-ttu-id="ed6f1-112">회의 주석</span><span class="sxs-lookup"><span data-stu-id="ed6f1-112">Conferencing annotations</span></span> 

## <a name="meeting-content-retention"></a><span data-ttu-id="ed6f1-113">모임 콘텐츠 보존</span><span class="sxs-lookup"><span data-stu-id="ed6f1-113">Meeting Content Retention</span></span>
<span data-ttu-id="ed6f1-p103">고객 Skype를 사용 하 여 비즈니스를 위한 PowerPoint 프레젠테이션, OneNote 파일 및 기타 파일 등의 첨부 파일로 비즈니스 모임에 대 한 Skype에 콘텐츠를 업로드할 수 있습니다. 모임에 업로드 된 콘텐츠에 대 한 보존 기간은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p103">Customers using Skype for Business can upload content to a Skype for Business meeting as attachments, such as PowerPoint presentations, OneNote files, and other files. The retention period for content that has been uploaded to a meeting is as follows:</span></span>
- <span data-ttu-id="ed6f1-116">**일회성 모임** -콘텐츠는 마지막 사람이 모임을 떠난에서 시작 하는 15 일 동안 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-116">**One-time meeting** - Content is retained for 15 days starting from when the last person leaves the meeting.</span></span>
- <span data-ttu-id="ed6f1-p104">**되풀이 모임** -콘텐츠는 마지막 사람이 모임 마지막 세션을 벗어난 후 15 일 동안 보존 됩니다. 다른 사용자가 15 일 이내에 동일한 회의 세션에 참가 하는 경우에 다시 설정 하는 보존 타이머 합니다. 예, 비즈니스 모임에 대 한 Skype 1 년에 대 한 주간 별로 수행 되도록 설정 되어 있다고 가정 하 고 첫번째 인스턴스 하는 동안 모임에 업로드 된 파일입니다. 한 명 이상의 사용자가 회의 세션 매주 해당 요일에 참가, 파일 전체 연도 마지막 사람이 시리즈의 마지막 회의 벗어난 후 15 일에 대 한 비즈니스 온라인 서버에 대 한 Skype에 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p104">**Recurring meeting** - Content is retained for 15 days after the last person leaves the last session of the meeting. The retention timer resets if someone joins the same meeting session within 15 days. For example, assume a Skype for Business meeting is scheduled to occur on a weekly basis for one year, and a file is uploaded to the meeting during the first instance. If at least one person joins the meeting session every week, the file is retained in Skype for Business Online servers for the entire year plus 15 days after the last person leaves the last meeting of the series.</span></span>
- <span data-ttu-id="ed6f1-121">**모임 시작 모임** -콘텐츠는 모임 종료 시간 후 8 시간 동안 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-121">**Meet Now meeting** - Content is retained for 8 hours after the meeting end time.</span></span>

> [!NOTE]
> <span data-ttu-id="ed6f1-122">사용자 사용이 허가 된 경우 (예: 하는 경우 **msRTCSIP 경우** *False*로 설정 됨)을 사용 하지 않도록 설정, 하 고 다음 다시 사용이 허가 된 또는 다시 사용 하도록 설정, 모임 콘텐츠 보존 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-122">If a user is unlicensed or disabled (e.g., if **msRTCSIP-userenabled** is set to *False*), and is then re-licensed or reenabled, meeting content is not retained.</span></span>

## <a name="meeting-expiration"></a><span data-ttu-id="ed6f1-123">모임 만료</span><span class="sxs-lookup"><span data-stu-id="ed6f1-123">Meeting Expiration</span></span>
<span data-ttu-id="ed6f1-124">사용자는 모임이 종료된 후 특정 모임에 액세스할 수 있습니다(다음 만료 기간이 적용됨).</span><span class="sxs-lookup"><span data-stu-id="ed6f1-124">Users can access a specific meeting after the meeting has ended, subject to the following expiration time periods:</span></span>
- <span data-ttu-id="ed6f1-125">**일회성 모임** -14 일 예약 된 모임 종료 시간 후 모임이 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-125">**One-time meeting** - Meeting expires 14 days after the scheduled meeting end time.</span></span>
- <span data-ttu-id="ed6f1-126">**종료 날짜를 사용 하 여 되풀이 모임** -14 일 마지막 모임 발생의 예약 된 종료 시간 후 모임이 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-126">**Recurring meeting with end date** - Meeting expires 14 days after the scheduled end time of the last meeting occurrence.</span></span>
- <span data-ttu-id="ed6f1-127">**모임 시작 모임** -8 시간 후 모임이 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-127">**Meet Now meeting** - Meeting expires after 8 hours.</span></span>

## <a name="whiteboard-collaboration"></a><span data-ttu-id="ed6f1-128">화이트 보드 공동 작업</span><span class="sxs-lookup"><span data-stu-id="ed6f1-128">Whiteboard Collaboration</span></span>
<span data-ttu-id="ed6f1-p105">화이트 보드에서 주석 모든 참가자에 게 표시 됩니다. 화이트 보드를 저장할 때 화이트 보드 및 주석 모두에 저장 됩니다 비즈니스 서버에 대 한 Skype 하 고 관리자가 설정한 모임 콘텐츠 만료 정책에 따라 서버에 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p105">Annotations made on whiteboards will be seen by all participants. When saving a whiteboard, the whiteboard and all annotations will be stored on a Skype for Business server, and it will be retained on the server according to meeting content expiration policies set by the administrator.</span></span>

## <a name="audio-test-service"></a><span data-ttu-id="ed6f1-131">오디오 테스트 서비스</span><span class="sxs-lookup"><span data-stu-id="ed6f1-131">Audio Test Service</span></span>
<span data-ttu-id="ed6f1-p106">음성의 짧은 (약 5 초) 샘플 기록 된 오디오 테스트 서비스를 호출 하는 동안 합니다. 음성 샘플 사용 하는 사용자가 확인 및/또는 녹음/녹화의 품질에 따라 비즈니스 통화에 대 한 프로그램 Skype의 사운드 품질을 확인 합니다. 오디오 테스트 서비스 통화 종료 되 면 음성 샘플 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p106">A short (approximately 5 seconds) sample of your voice is recorded during the Audio Test Service call. The voice sample is used by you to check and/or verify the sound quality of your Skype for Business call based on the quality of the recording. When the Audio Test Service call ends, the voice sample is deleted.</span></span>

## <a name="persistent-group-chat"></a><span data-ttu-id="ed6f1-135">영구 그룹 채팅</span><span class="sxs-lookup"><span data-stu-id="ed6f1-135">Persistent Group Chat</span></span>
<span data-ttu-id="ed6f1-p107">영구 그룹 채팅 그룹 채팅 대화의 내용을 저장합니다. 이 옵션을 설정 하는 경우 관리자가 그룹 채팅 기록을 준수 또는 기타 용도로 보관 하는 경우이 정보를 저장 하는 서버 보존 기간을 제어를 업데이트 하 고 채팅방에서 모든 속성 관리/수정할 수 있습니다. 다양 한 역할을 사용 하는 사용자에 액세스할 수 다른 영구 데이터를 다음과 같이 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p107">Persistent Group Chat stores the content of group chat conversations. If enabled, the administrator can control the retention period, the server on which this information is stored, if Group Chat history is archived for compliance or other purposes, and manage/modify any properties on a room. Users with different roles have different access to the persisted data, as follows:</span></span>
- <span data-ttu-id="ed6f1-p108">관리자는 크게 증가 하는 데이터베이스의 크기를 유지 하려면 모든 대화방에서 오래 된 콘텐츠 (예: 특정 날짜 이전에 게시 된 콘텐츠)을 삭제할 수 있습니다. 또는 제거 하거나 메시지를 교체할 수 지정된 대화방에 대 한 잘못 된 것으로 간주 (또는 부적절 한 것으로 간주).</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p108">Administrators can delete older content (for example, content posted before a certain date) from any chat room to keep the size of the database from growing greatly. Or, they can remove or replace messages considered inappropriate for a given chat room (or considered unsuitable).</span></span>
- <span data-ttu-id="ed6f1-141">최종 사용자에 게 메시지 작성자를 포함 하 여 모든 대화방에서 콘텐츠를 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-141">End-users, including message authors, cannot delete content from any chat room.</span></span>
- <span data-ttu-id="ed6f1-p109">대화방 관리자 대화방 사용 하지 않도록 설정할 수 있지만 대화방을 삭제할 수 없습니다. 작성 한 후 관리자만 대화방을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f1-p109">Chat room managers can disable rooms but cannot delete rooms. Only administrators can delete a chat room after it is created.</span></span>