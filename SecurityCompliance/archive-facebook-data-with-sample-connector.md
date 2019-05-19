---
title: 샘플 커넥터를 사용 하 여 Office 365에서 Facebook 데이터 보관 (미리 보기)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 관리자는 기본 커넥터를 설정 하 여 Facebook Business 페이지, LinkedIn 회사 페이지 및 인스턴트 Bloomberg 같은 데이터 원본에서 타사 데이터를 가져올 수 있습니다. 이를 통해 Office 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터를 관리 하는 것을 관리할 수도 있습니다.
ms.openlocfilehash: 7a71eac07d3d3260809f90cd2e470c32c44e9dda
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152190"
---
# <a name="use-a-sample-connector-to-archive-facebook-data-in-office-365-preview"></a>샘플 커넥터를 사용 하 여 Office 365에서 Facebook 데이터 보관 (미리 보기)

Office 365의 Facebook 데이터를 보관 하는 샘플 커넥터 기능은 미리 보기에 있습니다.

Office 365의 Security & 준수 센터에 있는 예제 커넥터를 사용 하 여 Facebook Business pages, LinkedIn, Twitter, Bloomberg 등의 타사 데이터 원본에서 데이터를 가져오고 보관 합니다. 샘플 커넥터를 설정 하 고 구성한 후에는 예약 된 방식으로 타사 데이터 원본에 연결 하 고, 항목의 콘텐츠를 전자 메일 메시지 형식으로 변환한 다음 해당 항목을 Office 365의 사서함으로 가져옵니다.

타사 데이터를 가져온 후에는 타사 데이터에 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사, 감독 및 Office 365 고정 정책과 같은 Office 365 준수 기능을 적용할 수 있습니다. 예를 들어, 사서함이 소송 보존으로 설정 되거나 할당 되 면 타사 데이터는 유지 됩니다. 콘텐츠 검색을 사용 하 여 타사 데이터를 검색 하거나, 고급 eDiscovery 사례에서 custodian과 연결할 수 있습니다. 샘플 커넥터를 사용 하 여 Office 365에서 타사 데이터를 가져오고 보관 하면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.

> [!NOTE]
> 현재로 서는 Facebook Business pages 및 [Twitter](archive-twitter-data-with-sample-connector.md) 에 대 한 샘플 커넥터만 미리 볼 수 있습니다. 더 많은 샘플 커넥터가 곧 제공 될 예정입니다.


## <a name="prerequisites-for-setting-up-a-connector-for-facebook-business-pages"></a>Facebook Business 페이지에 대 한 커넥터를 설정 하기 위한 필수 구성 요소

보안 & 준수 센터에서 샘플 커넥터를 설정 및 구성 하 여 조직의 Facebook Business 페이지에서 데이터를 가져오고 보관 하려면 먼저 다음 필수 구성 요소를 완료 해야 합니다. 

- 조직의 비즈니스 페이지에 대 한 Facebook 계정이 필요 합니다 (커넥터를 설정할 때이 계정에 로그인 해야 합니다.). 현재는 Facebook Business 페이지의 데이터만 보관할 수 있습니다. 개별 Facebook 프로필에서 데이터를 보관할 수 없습니다.

- 조직에 유효한 Azure 구독이 있어야 합니다. 기존 Azure 구독이 없는 경우 다음 옵션 중 하나를 등록할 수 있습니다.

    - [무료 1 년 Azure 구독 등록](https://azure.microsoft.com/free) 

    - [방문 비용 청구 Azure 구독에 등록](https://azure.microsoft.com/pricing/purchase-options/pay-as-you-go/)

    > [!NOTE]
    > Office 365 구독에 포함 된 [무료 Azure Active Directory 구독은](use-your-free-azure-ad-subscription-in-office-365.md) 보안 _AMP_ 준수 센터의 예제 커넥터를 지원 하지 않습니다.

- 조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다. 이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Office 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다.

- 보안 & 준수 (7 단계)에서 사용자 지정 커넥터를 설정 하는 사용자에 게 Exchange Online의 사서함 가져오기 내보내기 역할이 할당 되어야 합니다. 기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다. Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 또는 새 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다. 자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.

## <a name="step-1-download-the-pre-built-connector-app-package-from-github"></a>1 단계: Github에서 미리 작성 된 커넥터 앱 패키지 다운로드

첫 번째 단계는 Facebook API를 사용 하 여 facebook Business 페이지에 연결 하 고 Facebook 데이터를 추출 하 여 Office 365로 가져올 수 있도록 미리 작성 된 Facebook 커넥터 앱의 소스 코드를 다운로드 하는 것입니다.

1. [이 GitHub 사이트로](https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases)이동 합니다. 
2. 최신 버전에서 **SampleConnector** 파일을 클릭 합니다.
3. 로컬 컴퓨터의 위치에 ZIP 파일을 저장 합니다. 4 단계에서이 zip 파일을 Azure에 업로드 합니다.

## <a name="step-2-create-an-app-in-azure-active-directory"></a>2 단계: Azure Active Directory에 앱 만들기

다음 단계에서는 AAD (Azure Active Directory)에서 새 앱을 등록 합니다. 이 앱은 Facebook 커넥터에 대해 4 단계에서 구현 하는 웹 앱 리소스에 해당 합니다. 

단계별 지침은 [Azure Active Directory에서 앱 만들기](deploy-facebook-connector.md#step-2-create-an-app-in-azure-active-directory)를 참조 하세요.

단계별 지침에 따라이 단계를 완료 하는 동안 다음 정보를 텍스트 파일에 저장 합니다. 이러한 값은 배포 프로세스의 이후 단계에서 사용 됩니다.

- AAD 응용 프로그램 ID
- AAD 응용 프로그램 비밀
- AAD 응용 프로그램 Uri
- 테 넌 트 Id

## <a name="step-3-create-an-azure-storage-account"></a>3 단계: Azure storage 계정 만들기

조직에 대해 배포 하는 Facebook 커넥터는 Facebook Business 페이지의 항목을이 단계에서 만든 Azure 저장소 위치로 업로드 합니다. 보안 & 준수 센터 (7 단계)에서 사용자 지정 커넥터를 만든 후에는 Office 365 가져오기 서비스가 Azure storage 위치에서 Office 365의 사서함으로 Facebook 데이터를 복사 합니다. 앞에서 설명한 것 처럼 [필수 구성 요소](#prerequisites-for-setting-up-a-connector-for-facebook-business-pages) 섹션에서 azure storage 계정을 만들려면 유효한 azure 구독이 있어야 합니다.

단계별 지침은 [Azure storage 계정 만들기](deploy-facebook-connector.md#step-3-create-an-azure-storage-account)항목을 참조 하십시오.

단계별 지침에 따라이 단계를 완료 하는 동안 생성 되는 연결 문자열 Uri를 저장 합니다. 이 문자열을 사용 하 여 4 단계에서 Azure에서 웹 앱 리소스를 만들 수 있습니다.

## <a name="step-4-create-a-web-app-resource-in-azure"></a>4 단계: Azure에서 웹 앱 리소스 만들기

다음 단계는 Facebook 커넥터에 대 한 Azure에서 웹 앱 리소스를 만드는 것입니다. 

단계별 지침은 [Azure에서 새 웹 앱 리소스 만들기](deploy-facebook-connector.md#step-4-create-a-new-web-app-resource-in-azure)를 참조 하세요.

이 단계를 완료 하는 동안 단계별 지침을 따라 웹 앱 리소스를 만들 때 다음 정보 (이전 단계를 완료 한 후에 텍스트 파일로 복사)를 제공 합니다.

- APISecretKey –이 단계를 완료 하는 동안이 비밀을 만듭니다. 7 단계에서 사용 됩니다.
- StorageAccountConnectionString-3 단계에서 Azure storage 계정을 만든 후 복사한 연결 문자열 Uri입니다.
- tenantId-2 단계에서 Azure Active Directory에 Facebook 커넥터 앱을 만든 후 복사한 Office 365 조직의 테 넌 트 ID입니다.

또한이 단계에서 1 단계에서 다운로드 한 SampleConnector 파일을 업로드 하 여 Facebook 커넥터 응용 프로그램에 대 한 소스 코드를 배포 합니다.

이 단계를 완료 한 후에는 앱 서비스 URL (예:을 https://fbconnector.azurewebsites.net)복사 해야 합니다. 이를 사용 하 여 5 단계, 6 단계 및 7 단계를 완료 해야 합니다.

## <a name="step-5-register-the-web-app-on-facebook"></a>5 단계: Facebook에서 웹 앱 등록

다음 단계는 Facebook에서 새 앱을 만들고 구성 하는 것입니다. 7 단계에서 만든 사용자 지정 커넥터는 facebook 웹 앱을 사용 하 여 facebook API와 상호 작용 하 여 조직의 Facebook 비즈니스 페이지에서 데이터를 가져옵니다.

단계별 지침은 [Facebook 앱 등록](deploy-facebook-connector.md#step-5-register-the-facebook-app)을 참조 하십시오.

단계별 지침에 따라이 단계를 완료 하는 동안 다음 정보를 텍스트 파일에 저장 합니다. 이러한 값은 6 단계에서 Facebook 커넥터 앱을 구성 하는 데 사용 됩니다.

- Facebook 응용 프로그램 ID
- Facebook 응용 프로그램 비밀
- Facebook webhook 확인 토큰

## <a name="step-6-configure-the-facebook-connector-app"></a>6 단계: Facebook 커넥터 응용 프로그램 구성

다음 단계에서는 4 단계에서 Azure web app 리소스를 만들 때 업로드 한 Facebook 커넥터 앱에 구성 설정을 추가 합니다. 이렇게 하려면 커넥터 응용 프로그램의 홈 페이지로 이동 하 여 구성 합니다.

단계별 지침은 [6 단계: 커넥터 웹 앱 구성을](deploy-facebook-connector.md#step-6-configure-the-connector-web-app)참조 하십시오.

단계별 지침에 따라이 단계를 완료 하는 동안 이전 단계를 완료 한 후에 텍스트 파일로 복사한 다음 정보를 제공 합니다.

- Facebook 응용 프로그램 ID (5 단계에서 가져옴)
- Facebook 응용 프로그램 비밀 (5 단계에서 가져옴)
- Facebook webhook 확인 토큰 (5 단계에서 가져옴)
- Azure Active Directory 응용 프로그램 ID (2 단계에서 가져온 AAD 응용 프로그램 ID)
- Azure Active Directory 응용 프로그램 비밀 (2 단계에서 얻은 AAD 응용 프로그램 암호)
- Azure Active Directory 응용 프로그램 Uri (2 단계에서 가져온 AAD 응용 프로그램 Uri (예:https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213)

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a>7 단계: 보안 & 준수 센터에서 사용자 지정 커넥터 설정

마지막 단계에서는 Facebook Business 페이지의 데이터를 Office 365의 지정 된 사서함으로 가져올 보안 & 준수 센터에서 사용자 지정 커넥터를 설정 합니다. 이 단계를 성공적으로 완료 하면 Office 365 가져오기 서비스가 Facebook Business 페이지에서 Office 365로 데이터를 가져오는 프로세스를 시작 합니다. 

단계별 지침은 [Security _AMP_ 준수 센터에서 사용자 지정 커넥터 설정을](deploy-facebook-connector.md#step-7-set-up-a-custom-connector-in-the-security--compliance-center)참조 하십시오. 

단계별 지침에 따라이 단계를 완료 하는 동안 다음 정보를 제공 합니다 (단계 완료 후 텍스트 파일로 복사).

- 4 단계에서 얻은 Azure app service URL (예:https://fbconnector.azurewebsites.net)
- APISecretKey (4 단계에서 만든 것)
