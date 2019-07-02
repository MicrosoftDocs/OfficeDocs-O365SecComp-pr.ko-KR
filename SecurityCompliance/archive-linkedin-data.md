---
title: Office 365에서 LinkedIn 데이터를 보관 하는 커넥터 설정 (미리 보기)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 관리자는 기본 커넥터를 설정 하 여 LinkedIn 회사 페이지에서 Office 365로 데이터를 가져올 수 있습니다. 이를 통해 Office 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터에 대 한 준수를 관리할 수도 있습니다.
ms.openlocfilehash: 618cef7c0208378179d41a94f4a274a0bddadee9
ms.sourcegitcommit: ecc823c2a4f1465114cf1d3a4630e31c47779ddc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/19/2019
ms.locfileid: "35079382"
---
# <a name="set-up-a-connector-to-archive-linkedin-data-in-office-365-preview"></a>Office 365에서 LinkedIn 데이터를 보관 하는 커넥터 설정 (미리 보기)

Office 365에서 LinkedIn 회사 페이지의 데이터를 보관 하는 커넥터 기능이 미리 보기에 있습니다.

Office 365의 보안 & 준수 센터에서 네이티브 커넥터를 사용 하 여 LinkedIn 회사 페이지에서 데이터를 가져오고 보관 합니다. 커넥터를 설정 하 고 구성한 후에는 24 시간 마다 한 번씩 특정 LinkedIn 회사 페이지의 계정에 연결 됩니다. 이 커넥터는 회사 페이지에 게시 된 메시지를 전자 메일 메시지로 변환한 다음 해당 항목을 Office 365의 사서함으로 가져옵니다.

LinkedIn 회사 페이지 데이터가 사서함에 저장 되 면 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사 및 Office 365 고정 정책과 같은 Office 365 준수 기능을 LinkedIn 데이터에 적용할 수 있습니다. 예를 들어 콘텐츠 검색을 사용 하 여 이러한 항목을 검색 하거나, 고급 eDiscovery 사례의 custodian에 저장소 사서함을 연결할 수 있습니다. Office 365에서 LinkedIn 데이터를 가져오고 보관 하기 위한 커넥터를 만들면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.

## <a name="before-you--begin"></a>시작 하기 전에

- 조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다. 이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Office 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다.

- LinkedIn 회사 페이지 커넥터를 만드는 사용자에 게 Exchange Online의 사서함 가져오기 내보내기 역할이 할당 되어야 합니다. 이는 보안 & 준수 센터에서 **타사 데이터 보관** 페이지에 액세스 하는 데 필요 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.

- 보관 하려는 LinkedIn 회사 페이지의 관리자 인 LinkedIn 사용자 계정의 로그인 자격 증명 (전자 메일 주소 또는 전화 번호와 암호)이 있어야 합니다. 커넥터를 설정할 때 이러한 자격 증명을 사용 하 여 LinkedIn에 로그인 합니다.

## <a name="create-a-linkedin-connector"></a>LinkedIn 커넥터 만들기

1. 로 이동한 후 **데이터 거 버 넌 \> 스 가져오기를** 클릭 한 다음 **타사 데이터 보관**을 클릭 합니다. <https://protection.office.com>

2. **타사 데이터 보관** 페이지에서 **커넥터 추가**를 클릭 한 다음 **LinkedIn**을 클릭 합니다.

3. **서비스 약관** 페이지에서 **수락**을 클릭 합니다.

4. LinkedIn을 **사용** 하 여 로그인 페이지에서 **Linkedin과 함께 로그인**을 클릭 합니다.

   LinkedIn 로그인 페이지가 표시 됩니다.

   ![LinkedIn 로그인 페이지](media/LinkedInSigninPage.png)

5. LinkedIn 로그인 페이지에서 보관 하려는 회사 페이지와 연결 된 LinkedIn 계정의 전자 메일 주소 (또는 전화 번호)와 암호를 입력 하 고 **로그인**을 클릭 합니다.

   로그인 한 계정에 연결 된 모든 LinkedIn 회사 페이지 목록과 함께 마법사 페이지가 표시 됩니다. 커넥터는 한 회사 페이지에 대해서만 구성할 수 있습니다. 조직에 LinkedIn 회사 페이지가 여러 개 있는 경우 각 페이지에 대 한 커넥터를 만들어야 합니다.

   ![LinkedIn 회사 페이지 목록이 있는 페이지가 표시 됨](media/LinkedInSelectCompanyPage.png)

6. 항목을 보관 하려는 회사 페이지를 선택 하 고 **다음**을 클릭 합니다.

7. **필터 설정** 페이지에서 특정 기간에 해당 하는 항목을 처음 가져올 때 필터를 적용할 수 있습니다. 보존 기간을 선택 하 고 **다음**을 클릭 합니다.

8. **저장소 계정 설정** 페이지에서 LinkedIn 항목을 가져올 Office 365 사서함의 전자 메일 주소를 입력 하 고 **다음**을 클릭 합니다. 이 사서함의 받은 편지함 폴더로 항목을 가져옵니다.

9. 커넥터 설정을 검토 하 고 **저장** 을 클릭 하 여 커넥터 설치를 완료 합니다.

커넥터를 만든 후에는 **타사 데이터 보관** 페이지로 돌아갈 수 있습니다 (필요한 경우 **새로 고침** 을 클릭 하 여 커넥터 목록 업데이트). 새 커넥터 보기 **상태** 열의 값이 **시작을 기다리는 중**입니다. 초기 가져오기 프로세스를 시작 하는 데 최대 24 시간이 걸릴 수 있습니다. 처음에 커넥터를 실행 하 고 LinkedIn 항목을 가져온 후에는 24 시간 마다 한 번씩 커넥터가 실행 되 고 이전 24 시간 동안 LinkedIn 회사 페이지에서 만든 모든 새 항목이 가져오기 됩니다.

자세한 내용을 보려면 **타사 데이터 보관** 페이지의 목록에서 커넥터를 클릭 하 여 플라이 아웃 페이지를 표시 합니다. **상태**에서 표시 되는 날짜 범위는 커넥터를 만들 때 선택한 연령 필터를 나타냅니다. 

## <a name="more-information"></a>추가 정보

- LinkedIn 항목은 Office 365의 저장소 사서함에 있는 받은 편지함 폴더로 가져옵니다. 전자 메일 메시지로 나타납니다. 메시지를 보낸 사람의 표시 이름은 LinkedIn 회사 페이지의 이름입니다. 보낸 사람의 실제 전자 메일 주소는 저장소 사서함의 전자 메일 주소입니다. 회사 페이지의 이름도 제목 줄에도 미리 추가 됩니다. 

- 이전 동작으로 인해 Microsoft eDiscovery 도구를 사용 하 `from` 여 `subject` Office 365에 보관 된 LinkedIn 항목을 검색할 때 또는 전자 메일 속성을 검색할 수 있습니다. 예를 들어 회사 페이지의 이름이 "Contoso Company Page" 인 경우 키워드 검색 쿼리의 다음 *속성: 값* 쌍 중 하나를 사용할 수 있습니다.
   
   ```
   from:"Contoso Company Page"
   ```

    또는

   ```
   subject:"Contoso Company Page"
   ```

- Office 365로 가져온 LinkedIn 항목을 쉽게 찾거나 관리 하기 위해 저장소 사서함 (또는 FullAccess 권한이 할당 된 사용자)의 소유자가 항목을 LinkedIn 회사 페이지에서 특정 폴더로 이동 하는 받은 편지함 규칙을 설정할 수 있습니다. 이 기능은 저장소 사서함을 사용 하 여 다른 타사 데이터 원본에서 가져온 항목을 보관 하는 경우에 유용 합니다. 예를 들어 제목 필드에 있는 특정 LinkedIn 회사 페이지의 이름을 포함 하는 모든 항목을 특정 폴더로 이동 하는 받은 편지함 규칙을 만들 수 있습니다.