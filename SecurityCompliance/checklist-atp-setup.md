---
title: '빠른 시작: Office 365 Advanced Threat Protection 설정'
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: 여기에는 Office 365 ATP (Advanced Threat Protection)가 조직에 맞게 설정 되 고 구성 되었는지 확인 하는 데 사용할 수 있는 빠른 시작 가이드가 나와 있습니다.
ms.openlocfilehash: 5aecbdb63f30a620812de44907b29dcae838ba36
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693302"
---
# <a name="quick-start-guide-set-up-office-365-advanced-threat-protection"></a>빠른 시작 가이드: Office 365 Advanced Threat Protection 설정

다음은 조직에 Office 365의 ATP (Advanced Threat Protection)가 설정 되어 있는지 확인 하기 위한 검사 목록으로 사용할 수 있는 빠른 시작 가이드입니다. Office 365에서 위협 보호를 처음 사용 하는 경우 또는 시작할 위치를 모르는 경우에는 다음 지침을 출발점으로 활용 하세요. 

> [!IMPORTANT]
> **초기 권장 설정은 각 정책 유형에 대해 포함 되지만 대부분의 옵션을 사용할 수 있으며, 특정 조직의 요구에 맞게 설정을 조정할 수**있습니다. 정책이 나 변경 내용이 데이터 센터를 통해 작동 하는 데 약 30 분 정도 걸릴 수 있습니다.

## <a name="prerequisites"></a>필수 구성 요소

- 조직에 [Office 365 ATP (Advanced Threat Protection](office-365-atp.md) )가 포함 된 구독이 있어야 합니다.

- ATP 기능에 액세스 하려면 적절 한 역할이 할당 되어 있어야 합니다. 다음 표에는 몇 가지 예가 나와 있습니다. 

    |역할 또는 역할 그룹  |자세한 정보  |
    |---------|---------|
    |Office 365 전역 관리자 |[Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
    |보안 관리자 |[Azure Active Directory의 관리자 역할 권한](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
    |Exchange Online 조직 관리 |[Exchange Online의 사용 권한](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>한<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

    ( [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)참조)

## <a name="part-1---anti-malware"></a>1 부-맬웨어 방지

1. [Office 365 Security & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **맬웨어 방지**를 선택 합니다.
2. **기본** 정책을 두 번 클릭 한 다음 **설정을**선택 합니다.
3. 다음 설정을 지정 합니다.
    - **맬웨어 검색 응답** 섹션에서 기본 설정인 **아니요**를 그대로 둡니다.
    - **일반 첨부 파일 형식 필터** 섹션에서 **설정**를 선택 합니다.
4. **저장**을 클릭합니다.

맬웨어 방지 정책 옵션에 대 한 자세한 내용은 [맬웨어 방지 정책 구성을](configure-anti-malware-policies.md)참조 하십시오.

## <a name="part-2---zero-day-protection"></a>2 부-0 일 보호

제로 일 보호는 ATP 안전한 링크 및 안전한 첨부 파일 정책과 같은 정책을 통해 설정 됩니다.

### <a name="atp-safe-attachments-policies"></a>ATP 안전한 첨부 파일 정책

1. [Office 365 보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 안전한 첨부 파일**을 선택 합니다.
2. **SharePoint, OneDrive 및 Microsoft 팀에 대 한 ATP 설정**옵션을 선택 합니다.
3. **전자 메일 첨부 파일 보호** 섹션에서 더하기 기호 (**+**)를 클릭 합니다.
4. 다음 설정을 지정 합니다.
    - **이름** 상자에를 입력 `Block malware`합니다.
    - 응답 섹션에서 **차단을**선택 합니다.
    - **첨부 파일 리디렉션** 섹션에서 **리디렉션 사용**옵션을 선택 하 고 조직의 보안 관리자 또는 검색 된 파일을 검토할 운영자의 전자 메일 주소를 지정 합니다.
    - **적용 대상** 섹션에서 **받는 사람 도메인**을 선택 합니다. 그런 다음 도메인을 선택 하 고 **추가**를 선택한 다음 **확인**을 클릭 합니다.
5. **저장**을 클릭합니다.
6. (권장 추가 단계) 전역 관리자 또는 SharePoint Online 관리자는 Office 365 환경에 대해 **DisallowInfectedFileDownload** 매개 변수를 *true* 로 설정 하 여 **[set-spotenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet을 실행 합니다. 따라서 사용자가 악성 파일로 검색 된 파일을 열거나 이동 하거나 복사 하거나 공유할 수 없습니다.  

자세한 내용은 [office 365 atp 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md) 및 [SharePoint, OneDrive 및 Microsoft 팀에 대 한 office 365 atp 켜기](turn-on-atp-for-spo-odb-and-teams.md)를 참조 하세요.

### <a name="atp-safe-links-policies"></a>ATP 안전한 링크 정책

ATP 안전한 링크를 설정 하려면 기본 정책을 검토 하 고 정책을 추가 합니다.

1. [Office 365 보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 안전한 링크**를 선택 합니다.
2. **기본** 정책을 두 번 클릭 합니다.
3. 다음 **의 안전한 링크 사용** 섹션에서 **office 365 ProPlus, iOS 및 Android 용 office**를 차례로 선택 하 고 **저장**을 클릭 합니다.
4. **특정 받는 사람에 게 적용 되는 정책** 섹션에서 더하기 기호 (**+**)를 클릭 합니다.
5. 다음 설정을 지정 합니다.
    - **이름** 상자에 이름을 입력 `Safe Links`합니다.
    - **작업 선택** 섹션에서 **설정**를 선택 합니다.
    - 다음 옵션을 선택 합니다.
        - **다운로드 가능한 콘텐츠를 검색 하기 위해 안전한 첨부 파일 사용** 
        - **조직 내에서 전송 된 전자 메일 메시지에 안전한 링크 적용**
        - **사용자가 원본 URL에 대 한 안전한 링크를 클릭 하는 것을 허용 하지 않음**
    - **적용 대상** 섹션에서 **받는 사람 도메인**을 선택 합니다. 그런 다음 도메인을 선택 하 고 **추가**를 선택한 다음 **확인**을 클릭 합니다.
6. **저장**을 클릭합니다.

자세한 내용은 [Office 365 ATP 안전한 링크 정책 설정을](set-up-atp-safe-links-policies.md)참조 하십시오. 

## <a name="part-3---anti-phishing"></a>3 부-피싱 방지 

1. [Office 365 보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 피싱 방지**를 선택 합니다.
2. **기본 정책을**클릭 합니다.
3. **가장** 섹션에서 **편집**을 클릭 하 고 다음 설정을 지정 합니다.
    -  **보호할 사용자 추가** 탭에서 보호를 설정 합니다. 그런 다음 조직의 보드 구성원, CEO, CFO 및 기타 선임 리더와 같은 사용자를 추가 합니다. (개별 전자 메일 주소를 입력 하거나를 클릭 하 여 목록을 표시할 수 있습니다.)
    - **보호할 도메인 추가** 탭에서 **자신이 소유한 도메인을 자동으로 포함**을 설정 합니다. 사용자 지정 도메인이 있는 경우 해당 도메인도 추가 합니다.
    - **작업** 탭에서 가장 된 사용자 및 가장 한 도메인에 대해 **받는 사람의 정크 메일 폴더로 메시지 이동을** 선택 하 고 보안 팁을 설정 합니다.
    - **사서함 인텔리전스** 탭에서 사서함 인텔리전스가 설정 되어 있는지 확인 합니다.
    - **설정 검토** 탭에서 설정을 검토 한 후 **저장**을 클릭 합니다.
4. **스푸핑** 섹션에서 **편집**을 클릭 하 고 다음 설정을 지정 합니다.
    - **스푸핑 필터 설정** 탭에서 스푸핑 방지 보호가 설정 되어 있는지 확인 합니다.
    - **작업** 탭에서 받는 사람의 정크 메일 폴더로 메시지 이동을 선택 합니다.
    - **설정 검토** 탭에서 설정을 검토 한 후 **저장**을 클릭 합니다. 변경 하지 않은 경우 **취소**를 클릭 합니다.
5. 기본 정책 설정 페이지를 닫습니다.

피싱 방지 정책 옵션에 대 한 자세한 내용은 [Set up Office 365 ATP 안티 피싱 및 피싱 방지 정책을](set-up-anti-phishing-policies.md)참조 하세요.

## <a name="part-4---anti-spam"></a>4 부-스팸 방지

1. [Office 365 보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **스팸 방지**를 선택 합니다.
2. **사용자 지정** 탭에서 **사용자 지정 설정을** 켭니다.
3. **기본 스팸 필터 정책을**확장 하 고 **정책 편집**을 클릭 한 후 다음 설정을 지정 합니다.
    - **스팸 및 대량 작업** 섹션에서 임계값을 5 또는 6으로 설정 합니다.
    - 허용 **목록** 섹션에서 허용 되는 보낸 사람 및 도메인을 검토 하 고 필요에 따라 편집 합니다.
4. **저장**을 클릭합니다.

스팸 방지 정책 옵션에 대 한 자세한 내용은 [스팸 방지 정책 구성을](configure-the-anti-spam-policies.md)참조 하세요.

## <a name="part-5---service-wide-settings"></a>5 부-서비스 수준 설정

### <a name="zero-hour-auto-purge"></a>제로 시간 자동 삭제

자동 삭제 (ZAP)는 기본적으로 설정 됩니다. 그러나 다음 조건을 충족 해야 합니다.
- 스팸 방지 정책에서 **정크 메일 폴더로 메시지를 이동** 하도록 스팸 작업을 설정 합니다.
- 사용자가 기본 정크 메일 설정을 유지 했으며 정크 메일 보호를 해제 하지 않았습니다.

자세한 내용은 스팸 및 맬웨어를 방지 하는 [0 시간 자동 삭제](zero-hour-auto-purge.md)를 참조 하세요.

### <a name="audit-logging"></a>감사 로깅

[보안 대시보드](security-dashboard.md) 및 [탐색기](use-explorer-in-security-and-compliance.md)와 같은 위협 보호 보고서의 데이터를 보려면 조직에 대해 감사 로깅을 설정 해야 합니다.

[Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.

## <a name="post-setup-tasks"></a>설치 후 작업

### <a name="watch-for-new-features-and-service-updates"></a>새로운 기능 및 서비스 업데이트 조사

- [Microsoft 365 로드맵 방문](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [Office 365 Advanced Threat Protection 서비스 설명 참조](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)

### <a name="see-how-atp-is-working-for-your-organization"></a>조직에서 ATP가 작동 하는 방식 확인

- [Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)

- [보안 &amp; 및 준수 센터에서 탐색기 사용](use-explorer-in-security-and-compliance.md)

### <a name="periodically-review-and-revise-your-atp-policies"></a>ATP 정책 주기적으로 검토 및 수정

- [office 365 사용자에 게 office 365 위협 조사 및 응답을 안전 하 게 유지](keep-users-safe-with-office-365-ti.md) 

- [Office 365 보안 &amp; 및 준수 센터에서 smart reports 및 insights 사용](reports-and-insights-in-security-and-compliance.md) 