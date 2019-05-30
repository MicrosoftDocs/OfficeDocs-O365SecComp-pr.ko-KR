---
title: Office 365에서 Twitter 데이터를 보관 하기 위한 커넥터 배포
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: 관리자는 Twitter 데이터를 가져와 Office 365에 보관 하는 기본 커넥터를 설정할 수 있습니다. 이 데이터를 Office 365로 가져온 후 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 Twitter 데이터에 대 한 관리를 관리할 수 있습니다.
ms.openlocfilehash: 4d3bce8418ef2fa62c40d221549e6e089dee9647
ms.sourcegitcommit: 6c0fcb82178a4ac26375545f328389a6852a81be
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/28/2019
ms.locfileid: "34490551"
---
# <a name="deploy-a-connector-to-archive-twitter-data-in-office-365"></a>Office 365에서 Twitter 데이터를 보관 하기 위한 커넥터 배포

이 문서에는 Office 365 가져오기 서비스를 사용 하 여 조직의 Twitter 계정에서 Office 365로 데이터를 가져오는 커넥터를 배포 하는 단계별 프로세스가 포함 되어 있습니다. 이 프로세스에 대 한 간략 한 개요와 Twitter 커넥터를 배포 하는 데 필요한 필수 구성 요소 목록은 [예제 커넥터를 사용 하 여 Office 365 (미리 보기)에서 twitter 데이터를 보관](archive-twitter-data-with-sample-connector.md)합니다 .를 참조 하십시오. 

## <a name="step-1-download-the-package"></a>1 단계: 패키지 다운로드

GitHub 리포지토리의 릴리스 섹션에서 미리 작성 된 패키지를 다운로드 [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases)합니다. 최신 버전의 경우 **SampleConnector**라는 zip 파일을 다운로드 합니다. 4 단계에서이 zip 파일을 Azure에 업로드 합니다.

## <a name="step-2-create-an-app-in-azure-active-directory"></a>2 단계: Azure Active Directory에 앱 만들기

1. 으로 이동 <https://portal.azure.com> 하 고 Office 365 전역 관리자 계정의 자격 증명을 사용 하 여 로그인 합니다.

   ![](media/TCimage01.png)

2. 왼쪽 탐색 창에서 **Azure Active Directory**를 클릭 합니다.

   ![](media/TCimage02.png)

3. 왼쪽 탐색 창에서 **앱 등록 (미리 보기)** 을 클릭 하 고 **새 등록**을 클릭 합니다.

   ![](media/TCimage03.png)

4. 응용 프로그램을 등록 합니다. **Uri 리디렉션 (선택 사항)** 아래의 응용 프로그램 형식 드롭다운 목록에서 웹을 선택한 다음 URI <https://portal.azure.com> 에 대 한 상자에 입력 합니다.

   ![](media/TCimage04.png)

5. **응용 프로그램 (클라이언트) id** 및 **디렉터리 (테 넌 트) id** 를 복사한 다음 텍스트 파일 또는 기타 안전한 위치에 저장 합니다. 이러한 Id는 이후 단계에서 사용 합니다.

    ![](media/TCimage05.png)

6. **새 앱에 대 한 인증서 & 비밀** 으로 이동 하 고 **클라이언트 암호** 에서 **새 클라이언트 암호**를 클릭 합니다.

   ![](media/TCimage06.png)

7. 새 암호를 만듭니다. 설명 상자에 암호를 입력 하 고 만료 기간을 선택 합니다. 

   ![](media/TCimage08.png)

8. 비밀 값을 복사 하 여 텍스트 파일 또는 기타 저장 위치에 저장 합니다. 이는 이후 단계에서 사용할 AAD 응용 프로그램 비밀입니다.

   ![](media/TCimage09.png)

9. 다음 스크린샷에 표시 된 대로 **매니페스트로** 이동 하 여 IDENTIFIERURIS (AAD 응용 프로그램 Uri 라고도 함)를 복사 합니다. AAD 응용 프로그램 Uri를 텍스트 파일 또는 기타 저장 위치에 복사 합니다. 6 단계에서 사용 합니다.

    ![](media/TCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a>3 단계: Azure storage 계정 만들기

1.  조직의 Azure 홈 페이지로 이동 합니다.

    ![](media/TCimage11.png)

2. **리소스 만들기** 를 클릭 하 고 검색 상자에 **저장소 계정을** 입력 합니다.

   ![](media/TCimage12.png)

3. **저장소**를 클릭 한 다음 **저장소 계정을**클릭 합니다.

   ![](media/TCimage13.png)

4. **저장소 계정 만들기** 페이지의 구독 상자에서 사용 중인 Azure 구독 유형에 따라 **유료** 또는 **무료 평가판** 을 선택 합니다. 

   ![](media/TCimage14.png)

5. 리소스 그룹을 선택 하거나 만듭니다.

   ![](media/TCimage15.png)

6. 저장소 계정의 이름을 입력 합니다.

   ![](media/TCimage16.png)

7. 검토 한 다음 **만들기** 를 클릭 하 여 저장소 계정을 만듭니다.

   ![](media/TCimage17.png)

8. 잠시 후 **새로 고침** 을 클릭 하 고 **리소스로 이동을** 클릭 하 여 저장소 계정으로 이동 합니다.

   ![](media/TCimage18.png)

9. 왼쪽 탐색 창에서 **Access 키** 를 클릭 합니다.

   ![](media/TCimage19.png)

10. **연결 문자열** 을 복사 하 여 텍스트 파일 또는 기타 저장 위치에 저장 합니다. 이는 4 단계에서 웹 앱 리소스를 만들 때 사용 합니다.

    ![](media/TCimage20.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a>4 단계: Azure에서 새 웹 앱 리소스 만들기

1. Azure portal의 **홈** 페이지에서 **모든 \> \> 리소스 만들기 웹 앱**을 클릭 합니다. **웹 앱** 페이지에서 **만들기**를 클릭 합니다.

   ![](media/TCimage21.png)

2. 아래와 같이 세부 정보를 입력 하 고 웹 앱을 만듭니다. **앱 이름** 상자에 입력 하는 이름은 Azure 앱 서비스 URL을 만드는 데 사용 됩니다. 예: twitterconnector.azurewebsites.net.

   ![](media/TCimage22.png)

3. 새로 만든 웹 앱 리소스로 이동 하 여 왼쪽 탐색 창에서 **응용 프로그램 설정을** 클릭 합니다. **응용 프로그램 설정**에서 **새 설정 추가** 를 클릭 하 고 다음 세 가지 설정을 추가 합니다. 이전 단계의 텍스트 파일에 복사한 값을 사용 합니다. 

    - **APISecretKey** – 임의의 값을 비밀로 입력할 수 있습니다. 이는 7 단계에서 커넥터 웹 앱에 액세스 하는 데 사용 됩니다.

    - **Storageaccountconnectionstring** -3 단계에서 Azure storage 계정을 만든 후 복사한 연결 문자열 Uri입니다.

    - **tenantId** -2 단계에서 Azure Active Directory에 Twitter 커넥터 앱을 만든 후 복사한 Office 365 조직의 테 넌 트 ID입니다.

    ![](media/TCimage23.png)

4. **일반 설정**에서 Always ( **** **켜기**) 옆의을 클릭 합니다. 페이지 맨 위에 있는 **저장** 을 클릭 하 여 응용 프로그램 설정을 저장 합니다.

   ![](media/TCimage24.png)

5. 마지막 단계에서는 1 단계에서 다운로드 한 Azure에 커넥터 응용 프로그램 소스 코드를 업로드 합니다. 웹 브라우저에서 scm.azurewebsites.net/ZipDeployUi로 이동 합니다.<AzureAppResourceName>https://. 예를 들어이 섹션의 2 단계에서 이름이 지정 된 Azure 앱 리소스의 이름이 **twitterconnector**인 경우로 https://twitterconnector.scm.azurewebsites.net/ZipDeployUi이동 합니다.

6. 1 단계에서 다운로드 한 SampleConnector을이 페이지로 끌어서 놓습니다. 파일이 업로드 되 고 배포가 성공 하면 페이지는 다음 스크린샷과 유사 하 게 표시 됩니다.

   ![](media/TCimage25.png)

## <a name="step-5-create-the-twitter-app"></a>5 단계: Twitter 응용 프로그램 만들기

1. https://developer.twitter.com으로 이동 하 고 조직의 개발자 계정에 대 한 자격 증명을 사용 하 여 로그인 한 다음 **앱**을 클릭 합니다.

   ![TCimage25-5-.png](media/TCimage25-5.png)
2. **앱 만들기**를 클릭 합니다.
   
   ![](media/TCimage26.png)

3. **앱 세부 정보**에서 응용 프로그램에 대 한 정보를 추가 합니다.

   ![](media/TCimage27.png)

4. Twitter 개발자 대시보드에서 방금 만든 앱을 선택 하 고 표시 된 앱 ID를 복사한 다음 텍스트 파일 또는 기타 저장 위치에 저장 합니다. 그런 다음 **세부 정보**를 클릭 합니다.
   
   ![](media/TCimage28.png)

5. **키 및 토큰** 탭의 **Consumer api 키** 아래에서 API 비밀 키를 복사 하 여 텍스트 파일 또는 기타 저장 위치에 저장 합니다. 그런 다음 **만들기** 를 클릭 하 여 액세스 토큰과 액세스 토큰 비밀을 생성 한 다음 텍스트 파일 또는 기타 저장소 위치로 복사 합니다.
   
   ![](media/TCimage29.png)

   그런 다음 **만들기** 를 클릭 하 여 액세스 토큰과 액세스 토큰 비밀을 생성 한 다음 텍스트 파일 또는 기타 저장소 위치로 복사 합니다.

6. **사용 권한** 탭을 클릭 하 고 다음 스크린샷에 표시 된 대로 사용 권한을 구성 합니다.

   ![](media/TCimage30.png)

7. 사용 권한 설정을 저장 한 후에 **앱 세부 정보** 탭을 클릭 한 다음 **> 편집 세부 정보**편집을 클릭 합니다.

   ![](media/TCimage31.png)

8. 다음 작업을 수행 합니다.

   - 커넥터 앱이 Twitter에 로그인 하도록 허용 하는 확인란을 선택 합니다.
   
   - **Connectorserviceuri>/Views/twitteroauth와 같은 형식을 사용 하 여 OAuth 리디렉션 Uri를 추가 하 고 connectorserviceuri의 값은 조직의 Azure app 서비스 URL입니다. \<** ** 예를 https://twitterconnector.azurewebsites.net/Views/TwitterOAuth들어

   ![](media/TCimage32.png)

이제 Twitter 개발자 앱을 사용할 준비가 되었습니다.

## <a name="step-6-configure-the-connector-web-app"></a>6 단계: 커넥터 웹 응용 프로그램 구성 

1. Https://\<AzureAppResourceName> (여기서 **AzureAppResourceName** 은 4 단계에서 이름이 지정 된 Azure 앱 리소스의 이름)로 이동 합니다. 예를 들어, 이름이 **twitterconnector**인 경우로 https://twitterconnector.azurewebsites.net이동 합니다. 앱의 홈 페이지는 다음 스크린샷 처럼 표시 됩니다.

   ![](media/FBCimage41.png)

2. **구성을** 클릭 하 여 로그인 페이지를 표시 합니다.

   ![](media/FBCimage42.png)

3. 테 넌 트 Id 상자에 2 단계에서 받은 테 넌 트 Id를 입력 하거나 붙여 넣습니다. 암호 상자에 2 단계에서 구한 APISecretKey를 입력 하거나 붙여 넣은 다음 **구성 설정 설정을** 클릭 하 여 **구성 세부 정보** 페이지를 표시 합니다.

   ![](media/TCimage35.png)

4. **구성 세부 정보**에서 다음 구성 설정을 입력 합니다. 

   - **Twitter Api 키** -5 단계에서 만든 Twitter 응용 프로그램의 앱 ID입니다.
   - **Twitter Api 비밀 키** -5 단계에서 만든 Twitter 응용 프로그램에 대 한 Api 비밀 키입니다.
   - **Twitter 액세스 토큰** -5 단계에서 만든 액세스 토큰입니다.
   - **Twitter 액세스 토큰 비밀** -5 단계에서 만든 액세스 토큰 비밀입니다.
   - **AAD 응용 프로그램 id** -2 단계에서 만든 Azure Active Directory 앱의 응용 프로그램 id
   - **AAD 응용 프로그램 비밀** -4 단계에서 만든 APISecretKey 암호의 값입니다.
   - **Aad 응용 프로그램 uri** -2 단계에서 가져온 aad 응용 프로그램 uri 예를 https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213들면입니다.
   - **App Insights Instrumentation 키** -이 상자를 비워 둡니다.

5. **저장** 을 클릭 하 여 커넥터 설정을 저장 합니다.

## <a name="step-7-set-up-a-custom-connector-in-the-security-and-compliance-center"></a>7 단계: 보안 및 준수 센터에서 사용자 지정 커넥터 설정

1.  로 이동한 <https://protection.office.com> 후 **데이터 거 버 넌 \> 스 \> 가져오기 보관 타사 데이터**를 클릭 합니다.

    ![](media/TCimage36.png)

2. **커넥터 추가** 를 클릭 한 다음 **Twitter**를 클릭 합니다.

   ![](media/TCimage37.png)

3. **커넥터 앱 추가** 페이지에서 다음 정보를 입력 하 고 **커넥터 유효성 검사**를 클릭 합니다.

    - 첫 번째 상자에 **Twitter**와 같은 커넥터의 이름을 입력 합니다.
    - 두 번째 상자에 4 단계에서 추가한 APISecretKey의 값을 입력 하거나 붙여넣습니다.
    - 세 번째 상자에 Azure 앱 서비스 URL을 입력 하거나 붙여넣습니다. 예를 **https://twitterconnector.azurewebsites.net**들어

   커넥터 유효성 검사가 완료 되 면 **다음**을 클릭 합니다.

   ![](media/TCimage38.png)

4. **커넥터 앱을 사용 하 여 로그인을**클릭 합니다.

   ![](media/TCimage39.png)

5. APISecretKey를 다시 입력 하거나 붙여 넣은 다음 **커넥터 서비스에 로그인을**클릭 합니다.

   ![](media/TCimage40.png)


6. **Twitter를 사용 하 여 계속을**클릭 합니다.

7. Twitter 로그인 페이지에서 조직의 Twitter 계정에 대 한 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.

   ![](media/TCimage42.png)

   로그인 하면 Twitter 페이지에 "Twitter 커넥터 작업을 설정 했습니다." 라는 메시지가 표시 됩니다.

8. **마침을** 클릭 하 여 Twitter 커넥터 설정을 완료 합니다.

9. **필터 설정** 페이지에서 특정 연령 인 항목을 가져오고 보관 하는 필터를 적용할 수 있습니다. **다음**을 클릭합니다.

   ![](media/TCimage44.png)

10. **저장소 계정 설정** 페이지에서 Twitter 항목을 가져올 Office 365 사서함을 선택 합니다.

    ![](media/TCimage45.png)

11. 설정을 검토 하 고 **마침을** 클릭 하 여 Security _AMP_ 준수 센터에서 커넥터 설정을 완료 합니다.

    ![](media/TCimage46.png)

    ![](media/TCimage47.png)

12. **타사 데이터 보관** 페이지로 이동 하 여 가져오기 프로세스의 진행 상황을 확인 합니다.

    ![](media/TCimage48.png)
