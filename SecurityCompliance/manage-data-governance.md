---
title: Office 365의 관리 방식 데이터를 관리 합니다.
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 5/9/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 48064107-fed2-4db0-9e5c-aa5ddd5ccb09
description: 데이터 관리 방식은 모두에 대 한 필요할 때 중심으로 데이터를 유지 하 고 가져오는 제거할 그렇지 않은 경우. Office 365의 관리 방식 데이터를 유지 하 고 끝에 콘텐츠를 영구적으로 삭제 하는 정책을 작성을 시작 부분에 데이터를 저장 하 고 가져오기 (영문)에서 전체 콘텐츠 수명 주기를 관리할 수 있습니다.
ms.openlocfilehash: ca3443c3b90a067bf171ddf89be604d262a7b9a4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534016"
---
# <a name="manage-data-governance-in-office-365"></a>Office 365의 관리 방식 데이터를 관리 합니다.

데이터 관리 방식은 모두에 대 한 필요할 때 중심으로 데이터를 유지 하 고 가져오는 제거할 그렇지 않은 경우. Office 365의 관리 방식 데이터를 유지 하 고 끝에 콘텐츠를 영구적으로 삭제 하는 정책을 작성을 시작 부분에 데이터를 저장 하 고 가져오기 (영문)에서 전체 콘텐츠 수명 주기를 관리할 수 있습니다.
  
## <a name="import"></a>가져오기

데이터의 일부 클라우드, 온-프레미스 서버와 같이 또는 타사 응용 프로그램의 외부 위치에 저장 될 수 있습니다. 가져오기 서비스를 사용 하면 쉽게 메시징, SharePoint 및 OneDrive 비즈니스 데이터에 대 한 네트워크를 통해 직접 업로드 하거나 정보를 보면는 암호화 된 드라이브를 전달 하 여 Office 365로 가져올 수 있습니다. 대상 사서함에 실제로 가져온 PST 파일에 항목을 필터링 하는 가져오기 서비스에서 지능형 가져오기 기능을 사용할 수 있습니다. 
  
- [Office 365에 PST 파일 가져오기 (영문)의 개요 (영문)](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84)
    
- [네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기](use-network-upload-to-import-pst-files.md)
    
- [드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- [PST 컬렉션 도구를 사용 하 여 찾기, 복사 및 조직에서 PST 파일을 삭제 하려면](find-copy-and-delete-pst-files-in-your-organization.md)
    
- [Office 365에 PST 파일을 가져올 때 데이터를 필터링 합니다.](filter-data-when-importing-pst-files.md)
    
- [PowerShell cmdlet을 사용하여 SharePoint Online에 온-프레미스 콘텐츠 업로드](https://support.office.com/article/555049c6-15ef-45a6-9a1f-a1ef673b867c)
    
## <a name="govern-i-store-data"></a>I: 저장소 데이터를 제어 합니다.

데이터를 가져온 후 저장소가 증가 해야할 수 있습니다. (호출 자동 확장 보관) Office 365의 무제한 보관 기능의 보관 사서함에 저장 무제한 금액을 제공합니다.
  
- [Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터](enable-archive-mailboxes.md)

- [Office 365 무제한 보관의 개요 (영문)](unlimited-archiving.md)
    
- [Office 365 무제한 보관을 사용 하도록 설정](enable-unlimited-archiving.md)
    

    
## <a name="govern-ii-create-policies-and-labels-to-retain-content"></a>정책 및 콘텐츠를 유지 하려면 레이블 만들기 II를 제어 합니다.

보존 정책 준수 사전 업계 규정 및 내부 정책 보다 더 이상 하지만 필요에 따라 같이 긴 콘텐츠를 보관할 수 있도록 하 여 하는데 도움이 됩니다. 단일 보존 정책에는 전체 조직에 나타날 수 있습니다. 또한 관리 방식에 대 한 조직 전체에서 데이터를 분류 하 고 다음 해당 분류에 따라 보존 규칙을 적용 하 여 파일 계획을 구현 하려면 레이블을 사용할 수 있습니다.
  
- [보존 정책 개요](retention-policies.md)
    
- [레이블 개요](labels.md)
    
- [대량 만들기 및 PowerShell을 사용 하 여 레이블을 게시 합니다.](https://support.office.com/article/8986701b-ffa1-46ec-8fd0-8f7e81d5b25f.aspx)
    
- [처리 검토 개요](disposition-reviews.md)
    
- [이벤트 구동 보존 개요](event-driven-retention.md)
    
## <a name="govern-iii-retain-the-email-of-former-employees"></a>이전 직원의 전자 메일을 유지 III를 제어 합니다.

사용자 조직에서 나가는 경우 비활성 사서함을 만들어 전자 메일을 유지할 수 있습니다. 사서함을 소송 보존을 Office 365 보존 정책, 비활성화 됩니다 또는 다른 유형의 보류에 적용 되 하 고 해당 Office 365 사용자 계정을 삭제 합니다. 비활성 사서함의 항목은 보류 또는 보존 정책 비활성 적용 되기 전에 사서함에 설정 된 기간 동안 유지 됩니다.
  
- [Office 365에서 비활성 사서함의 개요 (영문)](inactive-mailboxes-in-office-365.md)
    
- [Office 365에서 비활성 사서함 만들기 및 관리](create-and-manage-inactive-mailboxes.md)

- [Office 365에서 비활성 사서함에 대 한 보존 기간 변경](change-the-hold-duration-for-an-inactive-mailbox.md)
  
- [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)
 
- [Office 365에서 비활성 사서함 복원](restore-an-inactive-mailbox.md)

- [Office 365에서 비활성 사서함 삭제](delete-an-inactive-mailbox.md)

## <a name="monitor"></a>모니터링

감독 내부 또는 외부 검토자가 검사할 수 있도록 전자 메일 및 조직에서 타사 통신 캡처 하는 정책을 정의할 수 있습니다. 검토자가 이러한 통신을 분류, 그들은 조직의 정책 준수 하는지 확인 하 고 수 필요한 경우 의심 스러운 자료를 전환 합니다.
  
레이블을 의도 한 대로 콘텐츠에 적용 되는 모니터링 데이터 관리 보고서 및 레이블 활동 탐색기를 사용할 수도 있습니다.
  
- [조직에 대한 감독 정책 구성](configure-supervision-policies.md)
    
- [감독 보고서](supervision-reports.md)
    
- [문서에 대한 레이블 활동 보기](view-label-activity-for-documents.md)
    
- [데이터 거버넌스 보고서 보기](view-the-data-governance-reports.md)
    
## <a name="more-information"></a>추가 정보

- [Microsoft 데이터 관리 팀의 비디오 보기](https://go.microsoft.com/fwlink/?linkid=867039)
    
- [Office 365에서 데이터 관리 방식 개요 비디오 시청](https://go.microsoft.com/fwlink/?linkid=852644)
    
- [Office 365 보안 &amp; 준수 센터 cmdlet](https://go.microsoft.com/fwlink/?linkid=852310)
    

