---
title: Office 365에서 인스턴트 Bloomberg 데이터를 보관 하는 커넥터 설정 (미리 보기)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 관리자는 기본 커넥터를 설정 하 여 인스턴트 Bloomberg 채팅 도구에서 Office 365로 데이터를 가져올 수 있습니다. 이렇게 하면 Office 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터를 관리할 수도 있습니다.
ms.openlocfilehash: 0b69ddaa21196bd0e149eba672fec104eabe2e5e
ms.sourcegitcommit: ab16ddf4c050a995471a058150767a0778be0b88
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35431611"
---
# <a name="set-up-a-connector-to-archive-instant-bloomberg-data-in-office-365-preview"></a>Office 365에서 인스턴트 Bloomberg 데이터를 보관 하는 커넥터 설정 (미리 보기)

Office 365에서 인스턴트 Bloomberg 데이터를 보관 하는 커넥터 기능이 미리 보기에 있습니다.

Office 365의 보안 & 준수 센터에서 네이티브 커넥터를 사용 하 여 [인스턴트 Bloomberg](https://www.bloomberg.com/professional/product/collaboration/) 공동 작업 도구에서 금융 서비스 채팅 데이터를 가져오고 보관 합니다. 커넥터를 설정 하 고 구성한 후에는 조직에서 매월 Bloomberg 보안 FTP 사이트 (SFTP)에 연결 하 고, 채팅 메시지의 콘텐츠를 전자 메일 메시지 형식으로 변환한 다음, 해당 항목을 Office 365의 사서함으로 가져옵니다.

인스턴트 Bloomberg 데이터를 사용자 사서함에 저장 한 후에는 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사 및 Office 365 고정 정책과 같은 Office 365 준수 기능을 인스턴트 Bloomberg 데이터에 적용할 수 있습니다. 예를 들어 콘텐츠 검색을 사용 하 여 인스턴트 Bloomberg 채팅 메시지를 검색 하거나, 고급 eDiscovery 사례의 custodian에 인스턴트 Bloomberg 데이터가 포함 된 사서함을 연결할 수 있습니다. 인스턴트 Bloomberg 커넥터를 사용 하 여 Office 365에서 데이터를 가져오고 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.

## <a name="overview-of-archiving-instant-bloomberg-data"></a>인스턴트 Bloomberg 데이터 보관 개요

다음 개요에서는 커넥터를 사용 하 여 Office 365에서 인스턴트 Bloomberg 채팅 데이터를 보관 하는 프로세스에 대해 설명 합니다. 

![인스턴트 Bloomberg 가져오기 및 보관 프로세스](media/InstantBloombergDataArchiving.png)

1. 조직에서 Bloomberg를 사용 하 여 Bloomberg SFTP 사이트를 설정 합니다. 또한 Bloomberg을 사용 하 여 Bloomberg SFTP 사이트에 채팅 메시지를 복사 하도록 인스턴트 Bloomberg을 구성 합니다.

2. 24 시간 마다 한 번씩 인스턴트 Bloomberg의 채팅 메시지가 Bloomberg SFTP 사이트로 복사 됩니다.
    
3. Security & 준수 센터에서 만든 인스턴트 Bloomberg 커넥터는 매일 Bloomberg SFTP 사이트에 연결 하 고 이전 24 시간에서 Microsoft 클라우드의 안전한 Azure Storage 영역으로 채팅 메시지를 전송 합니다. 또한이 커넥터는 채팅 massage의 콘텐츠를 전자 메일 메시지 형식으로 변환 합니다.
    
4. 커넥터는 채팅 메시지 항목을 특정 사용자의 사서함 또는 대체 사서함으로 가져옵니다. 커넥터에서 *CorporateEmailAddress* 속성 값을 사용 합니다. 모든 채팅 메시지에는 채팅 메시지의 모든 참가자의 전자 메일 주소로 채워지는이 속성이 포함 되어 있습니다. 특정 사용자 사서함 또는 대체 사서함으로 항목을 가져올지 여부는 다음 기준에 따라 결정 됩니다.
    
    위한. **Office 365 사용자 계정에 해당 하는 CorporateEmailAddress 속성의 값** 이 있는 항목-커넥터가 *CorporateEmailAddress* 속성의 전자 메일 주소를 office 365의 특정 사용자 계정에 연결할 수 있는 경우 사용자 Office 365 사서함의 받은 편지함 폴더에 항목이 복사 됩니다.
    
    b. **CorporateEmailAddress 속성의 값이 office 365 사용자 계정에 해당 하지 않는 항목** -커넥터가 *CorporateEmailAddress* 속성의 전자 메일 주소를 office의 특정 사용자 계정과 연결할 수 없는 경우 365에서 항목은 Office 365의 대체 "수신-전체" 사서함의 받은 편지함 폴더에 복사 됩니다.

## <a name="before-you-begin"></a>시작하기 전에

인스턴트 Bloomberg 데이터를 보관 하는 데 필요한 대부분의 구현 단계는 Office 365 외부에 있으므로 보안 & 준수 센터에서 커넥터를 만들기 전에 완료 해야 합니다.

- [Blooomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA)를 구독 합니다. 이는 Bloomberg Anywhere에 로그인 하 여 설정 하 고 구성 해야 하는 Bloomberg SFTP 사이트에 액세스할 수 있도록 하는 데 필요 합니다.

- Bloomberg SFTP (보안 파일 전송 프로토콜) 사이트를 설정 합니다. Bloomberg을 사용 하 여 SFTP 사이트를 설정한 후에는 인스턴트 Bloomberg의 데이터가 매일 SFTP 사이트로 업로드 됩니다. 2 단계에서 만든 커넥터가이 SFTP 사이트에 연결 되 고 채팅 데이터를 Office 365 사서함으로 전송 합니다. 또한 SFTP는 전송 프로세스 중에 Office 365 사서함으로 전송 되는 인스턴트 Bloomberg 채팅 데이터를 암호화 합니다.

    Bloomberg SFTP에 대 한 자세한 내용은 *BB-sftp*라고도 합니다.

    - [Bloomberg 지원](https://www.bloomberg.com/professional/support/documentation/)에서 "SFTP 연결 표준" 문서를 참조 하세요.
    
    - [Bloomberg 고객 지원](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc)에 문의 합니다.

    Bloomberg을 사용 하 여 SFTP 사이트를 설정한 후 Bloomberg에서는 Bloomberg 구현 전자 메일 메시지에 응답 한 후 몇 가지 정보를 제공 합니다. 다음 정보의 복사본을 저장 합니다. 이 도구를 사용 하 여 3 단계에서 커넥터를 설정 합니다.

    - 기업 코드-조직의 ID 이며 Bloomberg SFTP 사이트에 로그인 하는 데 사용 됩니다.

    - Bloomberg SFTP 사이트의 암호

    - Bloomberg SFTP 사이트의 URL (예: sftp.bloomberg.com)

    - Bloomberg SFTP 사이트의 포트 번호

- 조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다. 이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Office 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다. 3 단계에서 인스턴트 Bloomberg 커넥터를 성공적으로 만들기 전에이 단계를 완료 해야 합니다.

- 3 단계에서 인스턴트 Bloomberg 커넥터를 만들고 1 단계에서 공개 키와 IP 주소를 다운로드 하는 사용자에 게 Exchange Online의 사서함 가져오기 내보내기 역할이 할당 되어야 합니다. 이는 보안 & 준수 센터에서 **타사 데이터 보관** 페이지에 액세스 하는 데 필요 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.

## <a name="step-1-obtain-ssh-and-pgp-public-keys"></a>1 단계: SSH 및 PGP 공개 키 획득

첫 번째 단계는 SSH (Secure Shell) 용 공개 키와 PGP (매우 좋은 개인 정보)의 복사본을 가져오는 것입니다. 2 단계에서 이러한 키를 사용 하 여 3 단계에서 만든 커넥터에서 SFTP 사이트에 연결 하 고 인스턴트 Bloomberg 채팅 데이터를 Office 365 사서함으로 전송 하도록 Bloomberg SFTP 사이트를 구성 합니다. 또한 Bloomberg SFTP 사이트를 구성할 때 사용 하는이 단계에서 IP 주소를 가져옵니다.

1. 로 이동한 후 **데이터 거 버 넌 \> 스 가져오기를** 클릭 한 다음 **타사 데이터 보관**을 클릭 합니다. <https://protection.office.com>

2. **타사 데이터 보관** 페이지에서 **커넥터 추가**를 클릭 한 다음 **인스턴트 Bloomberg**을 클릭 합니다.

3. **서비스 약관** 페이지에서 **수락**을 클릭 합니다.

4. 1 단계 아래에 있는 **Bloomberg에 대 한 자격 증명 추가 사이트** 에서 **SSH 키 다운로드** 및 **PGP 키** 다운로드 링크 다운로드를 클릭 하 여 각 공개 키 파일의 복사본을 로컬 컴퓨터에 저장 합니다. 이러한 파일에는 2 단계에서 Bloomberg SFTP 사이트를 구성 하는 데 사용 되는 다음과 같은 항목이 포함 되어 있습니다.

   - SSH 공개 키-이 키는 커넥터가 Bloomberg SFTP 사이트에 연결 될 때 보안 원격 로그인을 사용 하도록 허용 하도록 SSH (Secure Shell)를 구성 하는 데 사용 됩니다.

   - PGP 공개 키-이 키는 Bloomberg SFTP 사이트에서 Office 365로 전송 되는 데이터의 암호화를 구성 하는 데 사용 됩니다.

   - IP 주소-Bloomberg SFTP 사이트는 3 단계에서 만든 인스턴트 Bloomberg 커넥터에서 사용 하는이 IP 주소 로부터의 연결 요청만 수락 하도록 구성 됩니다. 

5. **취소** 를 클릭 하 여 마법사를 닫습니다. 3 단계의이 마법사로 돌아와서 커넥터를 만듭니다.

## <a name="step-2-configure-the-bloomberg-sftp-site"></a>2 단계: Bloomberg SFTP 사이트 구성

다음 단계에서는 1 단계에서 가져온 SSH 및 PGP 공개 키와 IP 주소를 사용 하 여 Bloomberg SFTP 사이트에 대 한 SSH 인증 및 PGP 암호화를 구성 합니다. 이렇게 하면 3 단계에서 만든 인스턴트 Bloomberg 커넥터를 사용 하 여 Bloomberg SFTP 사이트에 연결 하 고 인스턴트 Bloomberg 데이터를 Office 365에 전송할 수 있습니다. 이 기능을 설정 하는 데 도움이 필요한 경우 [Bloomberg 고객 지원](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) 에 문의 하세요.

1. 조직의 계정을 사용 하 여 Bloomberg CCNS 제어판에 로그인 합니다.

2. CCNS로 이동 하 여 **공개 키** 탭을 클릭 합니다.

3. SSH 인증을 사용 하도록 설정 하려면 **추가**를 클릭 합니다.

4. **공개 키 추가** 창에서 **키 유형** 드롭다운 목록을 클릭 한 다음 **로그인**을 클릭 합니다.

5. 1 단계에서 다운로드 한 전체 SSH 공개 키 (큰따옴표를 포함 하지 않고 큰따옴표로 묶은 모든 문자)를 복사 하 여이 필드에 붙여 넣은 다음 **제출을** 클릭 하 여 키를 저장 합니다.
 
    예를 들어 다음 SSH 공개 키를 복사 합니다.

    `
    ssh-rsa
    AAAAB3NzaC1yc2EAAAABIwAAAQEA1dxAyc0JzCmc5NzgyzRYhnj3FGHK5Kd9T2cwZNkmL/9nFhQupQor081rmuw9gACAmeot7y+V/fmijo/q4rxDe3Auu3hfLl1NpWlIssQJHzycms8zimtdQcXbMKwDQOnRthpEocF5ySs76KE72vaYQJTvclAamWWq0D75SUmXDFFr7afvEy57F7KgMD1ecg6lH7q8seSKbiiWxX1Ul0kL15fzpUyhjDP41owb1XC/dF7fJwAmCO1+HZfDLEp62q4tnApLpdd92KoR41LZTryO5dICKhk+S+JxPLkksxL0wm5YevOr2n4ScuRdsBV8mWKZ1Xw+cOss9O6L7cCcEiB3Ow==
    `

6. PGP 암호화를 사용 하도록 설정 하려면 **공개 키** 탭에서 다시 **추가** 를 클릭 하 고 **키 형식** 드롭다운 목록을 클릭 한 다음이 시간에 **암호화**를 클릭 합니다.

7. 1 단계에서 다운로드 한 전체 PGP 공개 키 (큰따옴표를 포함 하지 않고 큰따옴표로 묶은 모든 문자)를 복사 하 여이 필드에 붙여 넣은 다음 **제출을** 클릭 하 여 키를 저장 합니다. 

    예를 들어 다음 PGP 공개 키를 복사 합니다.

    `
    -----BEGIN PGP PUBLIC KEY BLOCK-----
    Version: BCPG C# v1.7.4137.9688
    nmQENBFz+6UQBCACKC4ilYoVOP5b/F0CO+oQYbag79Ov4NZxM4EKW51lUAvKNExRM\nc1C/gwXm8bghht8GEODckXXqx8qSSXUEeA/ROweXNtD1u1kn7PgYEFUeD/qE739m\nm5lxXF9Vod26AtKQ9Y1EvYoQEltwztAaXg8K8LQzB+tzN079d1cxM5tbiRQLttAh\nOt5amLXuINt8+dWyNas3DfgIBUmwfkwCbUO0ElrIhvvO3A85K97SX9Q6Py0SkfkK\nQpnULuhdjSm+7k7qlVMf0s8e/9jUXYKbMFkxlOoMq052vV0l0VQNSeuKoC+m6+LT\nEPab89AMt6S4Ujum9wTUy1eWNx9vV0y/w8N7ABEBAAG0JDM5MjM4ZTg3LWI1YWIt\nNGVmNi1hNTU5LWFmNTRjNmIwN2I0MokBHAQQAQIABgUCXP7pRAAKCRAJQdjaG//S\nCy70B/wKrR2CcqtZx56yrGJFfVy3niEt16VEA3xJM3D9nX0gmgo85Nh5gkiY3ahH\nnNEmgW5vlCM1gcgFeoZWe8A80G4QoabslSUzLbq9HsHOOAQApsfhrhXpylrAVa4n\nI53XUOxWdOTa4xsOob8hSRADqJbwHPOsoAr2A87TvZ9LSi2Mii5omeTq416CLnoS\nPBAEhelZm+ruy5JhzA1yXvWYFH08wNqSHO3bskdES2yW5SyQmYlcoEztWE0Q0Z+G\nZT3kOa/W2MbcZovFCQIfqhwVfXtIzx5uYUmxgk5cFKUJJMlO0AZK/HwM22xuuIWe\ndMa6OMo/n8tvEBxrLQMdVPlz+hZ6
    =AwmP
    -----END PGP PUBLIC KEY BLOCK-----
    `
8. CCNS 제어판의 주 창에서 **여기에 IP 주소 추가**에 **주소 추가 필드**의 다음 Ip 주소 (1 단계에서 다운로드 한 Keys 파일에 포함 됨)를 입력 합니다.

   `
   40.124.28.216
   `

## <a name="step-3-create-an-instant-bloomberg-connector"></a>3 단계: 인스턴트 Bloomberg 커넥터 만들기

마지막 단계는 보안 & 준수 센터에서 인스턴트 Bloomberg 커넥터를 만드는 것입니다. 커넥터는 제공 하는 정보를 사용 하 여 Bloomberg SFTP 사이트에 연결 하 고 채팅 메시지를 Office 365의 해당 사용자 사서함 상자로 전송 합니다. 

1. 로 이동한 후 **데이터 거 버 넌 \> 스 가져오기를** 클릭 한 다음 **타사 데이터 보관**을 클릭 합니다. <https://protection.office.com>

2. **타사 데이터 보관** 페이지에서 **커넥터 추가**를 클릭 한 다음 **인스턴트 Bloomberg**을 클릭 합니다.

3. **서비스 약관** 페이지에서 **수락**을 클릭 합니다.

4. **BLOOMBERG SFTP 사이트에 대 한 자격 증명 추가** 페이지의 3 단계에서 다음 상자에 필요한 정보를 입력 하 고 **다음**을 클릭 합니다.

    - **회사 코드** – 조직의 ID 이며 Bloomberg SFTP 사이트의 사용자 이름으로 사용 됩니다.

    - **Password** -Bloomberg SFTP 사이트의 암호입니다.

    - **SFTP url** -Bloomberg SFTP 사이트의 URL (예: sftp.bloomberg.com)입니다.

    - **SFTP 포트** -Bloomberg SFTP 사이트의 포트 번호입니다. 커넥터는이를 사용 하 여 SFTP 사이트에 연결 합니다.

5. **대체 사서함** 페이지에서 조직의 사용자 사서함에 연결할 수 없는 인스턴트 Bloomberg 채팅 메시지를 저장 하는 데 사용 되는 사서함의 전자 메일 주소를 입력 합니다.

   > [!NOTE]
   > 인스턴트 Bloomberg에 있는 모든 대화의 모든 채팅 메시지에는 채팅 참가자의 조직의 전자 메일 주소를 포함 하는 *CorporateEmailAddress*라는 속성이 포함 되어 있습니다. 가져오기 프로세스 중에 커넥터는 *CorporateEmailAddress* 속성에 있는 것과 동일한 전자 메일 주소를 가진 Office 365의 사용자 사서함으로 채팅 메시지를 가져오려고 시도 합니다. *CorporateEmailAddress* 속성에 있는 것과 같은 주소를 가진 Office 365 사서함이 없는 경우 커넥터는이 페이지에서 지정한 대체 사서함으로 채팅 메시지를 가져옵니다. 현재 대체 사서함에 보관 된 인스턴트 Bloomberg 채팅 메시지는 Office 365의 감독 정책에 의해 모니터링 되지 않습니다.

6. **다음**을 클릭 하 고 설정을 검토 한 다음 **준비** 를 클릭 하 여 커넥터를 만듭니다.

7. **타사 데이터 보관** 페이지로 이동 하 여 새 커넥터에 대 한 가져오기 프로세스의 진행 상황을 확인 합니다.
