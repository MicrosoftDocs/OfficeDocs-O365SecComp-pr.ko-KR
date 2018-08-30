---
title: 모바일 장치 관리 (MDM) Office 365의 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_OverviewMDM
- 'O365E_OverviewMDM '
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: dd892318-bc44-4eb1-af00-9db5430be3cd
description: Office 365에 대 한 기본 제공 되는 모바일 장치 관리를 사용 하면 보안을 유지 하 고 Iphone, Ipad, Androids, 같은 사용자의 모바일 장치를 관리 하 고 Windows 전화 합니다. 시작 하기를 활성화 하 고 Office 365에 대 한 모바일 장치 관리를 설정 하려면 다음이 단계를 수행 합니다.
ms.openlocfilehash: c92290170b2937067e7407787282eaaa368b25b7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272363"
---
# <a name="set-up-mobile-device-management-mdm-in-office-365"></a>모바일 장치 관리 (MDM) Office 365의 설정

Office 365에 대 한 기본 제공 모바일 장치 관리 (MDM)는를 사용 하면 보안을 유지 하 고 Iphone, Ipad, Androids, 같은 사용자의 모바일 장치를 관리 하 고 Windows 전화 합니다. 수 및 장치 보안 정책 관리, 원격으로 장치 지우기 시도 만들고 자세한 장치 보고서를 볼 합니다.
  
질문이 있습니까? [도움말 주소 관련 된 일반적인 질문에 대 한 FAQ](frequently-asked-questions-about-mdm.md)를 준비 했습니다. 사용할 수는 없습니다 주의 [파트너: 위임 된 관리 제공](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) Office 365에 대 한 모바일 장치 관리를 관리 하 합니다. 
  
장치 관리는 보안의 일부 &amp; 준수 센터 MDM 설치를 시작 하려면 다음과 같은 이동 해야 합니다.
  
Office 365에 대 한 모바일 장치 관리를 설정 하려면에 필요 합니다.
  
1. [모바일 장치 관리 서비스를 활성화 합니다.](#activate-the-mobile-device-management-service)  
2. [모바일 장치 관리 설정](#set-up-mobile-device-management)
3. [사용자가 자신의 장치 등록 되었는지 확인](#step-4-recommended-manage-device-security-policies)
  
## <a name="activate-the-mobile-device-management-service"></a>모바일 장치 관리 서비스를 활성화 합니다.

1. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다. 
    
2. 이동 [보안 &amp; 준수 센터](https://protection.office.com)합니다.
    
3. **데이터 손실 방지** 로 이동 \> **장치 관리** **아래의 단계를 시작** 하는 정품 인증 프로세스를 시작 하기를 클릭 하 고 있습니다. 
    
    ![Office 365에 대 한 모바일 장치 관리 설정](media/368e1026-9aa5-431b-a722-8f7cf528f263.png)
  
4. 시작 하는데 도움이 수에 대 한 기본 보안 정책을 만들었습니다. 이 페이지에는 보안 정책의 이름을 업데이트 하 고 **설치 프로그램을 시작**을 클릭 합니다.
    
    ![모바일 장치 관리 보안 정책 설정](media/5619a2d1-f900-4268-9050-5d7eb57429a5.png)
  
5. 서비스를 설정에서 진행 상태를 표시 하는 설치 화면을 볼 수 있습니다.
    
    ![MDM 설치 진행률](media/db45d1bb-d247-4ac0-9deb-1b0c1ace9bfa.png)
  
> [!TIP]
> 검색을 통해 **MDM 설치** 찾을 수 있습니다. Office 365 관리 센터에서 \> **홈** 페이지에서 **검색** 상자에 종류 모바일 장치 관리 합니다. > ![관리 센터에서 모바일 장치 관리에 대 한 검색](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)
  
Office 365에 대 한 모바일 장치 관리를 활성화 하려면 시간이 다소 걸릴 수 하지만 적용 하려면 다음 단계를 설명 하는 전자 메일 받게 완료 되 면 합니다.
  
## <a name="set-up-mobile-device-management"></a>모바일 장치 관리 설정

서비스를 수행할 준비가 되 면 설치를 완료 하는 다음 네가지 단계를 완료 합니다. **장치 관리** 페이지에서 보안 [설정 관리를](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) 클릭 해야 &amp; 준수 센터에서는 다음 설정을 볼 수 있습니다. 
  
![권장 되는 단계 및 필요한 모바일 장치 관리 설정](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
### <a name="step-1-required-configure-domains-for-mdm"></a>MDM에 대 한 1 단계: (필수) 구성 도메인

Office 365와 관련 된 사용자 지정 도메인 없는 또는 하지 Windows 장치를 관리 하는 경우에이 섹션을 건너뛸 수 있습니다. 그렇지 않은 경우 DNS 호스트에는 도메인에 대 한 DNS 레코드를 추가 하려면 필요 합니다. Office 365를 사용 하 여 도메인 설정의 일부로 이미, 레코드를 추가한 경우 모두 설정 합니다. 레코드를 추가한 후 사용자 지정 도메인을 사용 하는 전자 메일 주소와 해당 Windows 장치에 로그인 하면 조직에서 Office 365 사용자를 Office 365에 대 한 MDM에 등록할 리디렉션됩니다.
  
레코드를 설정 하는 데 도움이 필요 하세요? [DNS 레코드를 관리 하는 경우 Office 365 용 DNS 레코드 만들기](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) 에 제공 된 목록에서 도메인 등록자를 찾아 DNS 레코드 만들기 (영문)에 대 한 단계별 도움말으로 이동 하려면 등록자 이름을 선택 합니다. 이러한 지침을 사용 하 여 다음 두 레코드를 추가 하려면: 
  
|**호스트 이름**|**레코드 유형**|**주소**|**TTL**|
|:-----|:-----|:-----|:-----|
|EnterpriseEnrollment  <br/> |CNAME  <br/> |EnterpriseEnrollment.manage.microsoft.com  <br/> |3600  <br/> |
|EnterpriseRegistration  <br/> |CNAME  <br/> |EnterpriseRegistration.windows.net  <br/> |3600  <br/> |
   
두 레코드를 추가한 후 보안으로 다시 이동 &amp; 준수 센터 **장치 관리** 로 이동 하 고 \> 다음 단계를 완료 하려면 **관리 설정** 합니다. 
  
### <a name="step-2-required-configure-an-apns-certificate-for-ios-devices"></a>2 단계: (필수) 구성 iOS 장치에 대 한 한 apn을 사용할 인증서를

IPad / Iphone 같은 iOS 장치를 관리 하려면 한 apn을 사용할 인증서를 만들려면 해야 합니다.
  
이 위해 **설치 모바일 장치 관리 페이지**에서 **설정** 링크에서 단계를 수행 합니다.
  
1. **IOS 장치에 대 한 한 apn을 사용할 인증서 구성**옆에 있는 **설정**을 선택 합니다.
    
2. **CSR 파일 다운로드** 를 선택 하 고 인증서 서명 요청을 곳에 저장 기억할 수 있는 컴퓨터에 있습니다. 
    
    ![APN 인증서 대화 상자를 설치 합니다.](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. **다음**을 선택 합니다.
    
4. APN 인증서를 만듭니다.
    
  - **Apple 한 apn을 사용할 포털** Apple 푸시 인증서 포털을 선택 합니다. 
    
    ![Apple 한 apn을 사용할 포털을 선택 된 APN 알림 인증서 대화 상자를 설치 합니다.](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Apple ID를 사용 하 여 로그인
    
    > [!IMPORTANT]
    > Apple ID 관리 하는 계정 사용자를 떠날 하는 경우에 사용자의 조직과 상태로 유지 되는 전자 메일 계정과 연결 된 회사를 사용 합니다. 인증서를 갱신 하는 경우 동일한 ID를 사용 하 여 수행 해야 하기 때문에이 ID를 저장 합니다. 
  
  - **인증서 만들기** 를 선택 하 고 **사용 약관에**동의 합니다.
    
  - Office 365 및 **업로드**선택에서 사용자 컴퓨터로 다운로드 한 인증서 서명 요청 **이동** 합니다.
    
  - APN 인증서는 Apple 푸시 인증서 포털에서 사용자의 컴퓨터에 만든 **다운로드** 합니다. 
    
    > [!TIP]
    > 인증서를 다운로드 하는데 문제가 경우 브라우저를 새로 고쳐 합니다. 
  
5. Office 365로 다시 이동 하 고 **다음** **한 apn을 업로드 하는 사용할 인증서** 페이지를 선택 합니다. 
    
6. Apple 푸시 인증서 포털에서 다운로드 한 APN 인증서로 이동 합니다.
    
    ![Apple에서 다운로드 한 apn을 사용할 인증서를 선택 하려면 찾아보기 단추를 클릭 합니다.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. **완료 날짜**를 선택 합니다.
    
APN 인증서를 추가한 후 보안으로 다시 이동 &amp; 준수 센터 **장치 관리** 로 이동 하 고 \> 다음 단계를 완료 하려면 **관리 설정** 합니다. 
  
### <a name="step-3-recommended-set-up-multi-factor-authentication"></a>3 단계: 다단계 인증 설정 (권장)

다단계 인증 (MFA) **권장 단계**아래에 표시 되지 않으면, 하는 경우에이 섹션을 건너뛸 수 있습니다. 이 옵션은 표시 하는 경우에 Office 365 등록 프로세스에 대 한 모바일 장치 관리의 보안을 강화 하기 Azure AD 포털에서 MFA에 설정 하는 것이 좋습니다. 기본적으로 해제 되어 합니다.
  
MFA 두번째 형태의 인증을 요구 하 여 모바일 장치 등록을 위한 Office 365에 로그인 secure 도움이 됩니다. 사용자가 전화 통화, 텍스트 메시지 또는 올바르게 자신의 작업 계정 암호를 입력 한 후가 모바일 장치에서 응용 프로그램 알림 승인 하는 데 필요 합니다. 인증의 두번째 폼이 완료 되 면 해당 장치만 등록할 수 있습니다. 사용자의 장치는 Office 365에 대 한 모바일 장치 관리에 등록 된, 사용자가 자신의 작업 계정에만 사용 하 여 Office 365 리소스 액세스할 수 있습니다.
  
**다단계 인증 설정**옆에 있는 **설정**을 선택 합니다. MFA Azure AD 포털에서 사용 하는 방법을 알아보려면 [다단계 인증 설정](https://go.microsoft.com/fwlink/p/?LinkId=519255)을 참조 하십시오.
  
MFA를 설정한 후 보안으로 다시 이동 &amp; 준수 센터 **장치 관리** 로 이동 하 고 \> 다음 단계를 완료 하려면 **관리 설정** 합니다. 
  
### <a name="step-4-recommended-manage-device-security-policies"></a>4 단계: (권장) 관리 장치 보안 정책

다음 단계를 만들고 Office 365 조직의 데이터를 보호 하는 장치 보안 정책 배포 됩니다. 사용자가 비활성 5 분 후 잠금 장치에는 정책을 만들어 해당 장치를 잃어버린 경우 데이터 손실을 방지 하 고 장치가 도움이 되는 예 3-로그인 실패 한 후 데이터 삭제 합니다.
  
**보안 &amp; 준수 센터** **보안 정책** 으로 이동, \> **장치 보안 정책** 장치 보안 정책을 만들고이 규칙에 액세스 합니다. 
  
![장치 보안 정책 추가](media/69a027f5-fbfb-482a-b850-9ccb280b8c62.png)
  
새 정책을 만들려면 하는 방법에는 단계별 지침을 참조 하십시오. [만들기 및 장치 보안 정책 배포](create-device-security-policies.md)합니다.
  
> [!TIP]
>  새 정책을 만들 때에 사용자의 장치 정책와 호환 되지 않습니다 액세스 및 보고서 정책 위반을 허용 하도록 정책을 설정 하는 것이 좋습니다. 이 얼마나 많은 모바일 장치에서 Office 365에 대 한 액세스를 차단 하지 않고 정책에 의해 영향을 받는 것을 볼 수 있습니다. > 새 정책을 모든 사람에 게 조직에 배포 하기 전에 사용자 수가 적은에서 사용 하는 장치에서 테스트 하는 것이 좋습니다. > 또한 정책을 배포 하기 전에 Office 365에 대 한 MDM에서 장치를 등록의 잠재적 영향을 알고 있는 조직 수 있도록 합니다. 정책 설정 방법에 따라 이러한 (비준수 장치)를 준수 하지 장치는 Office 365에 액세스 하지 못하도록 차단할 수 있습니다. 비 호환 장치 앱 설치, 사진 및 기타 개인 정보는 등록 된 장치에서 삭제 될 수 있습니다는 장치 데이터 삭제 하는 경우는 있을 수 있습니다. 추가 정보: [Office 365의 모바일 장치 지우기 시도](wipe-a-mobile-device.md)합니다. 
  
## <a name="make-sure-users-enroll-their-devices"></a>사용자가 자신의 장치 등록 되었는지 확인

만들어 모바일 장치 관리 정책 배포 했을 때 후 장치 정책에 적용 되는 조직에서 사용이 허가 된 각 Office 365 사용자가 받습니다 등록 메시지 다음에 자신의 모바일 장치에서 Office 365에 로그인 합니다. Office 365 전자 메일 및 문서에 액세스할 수 있으려면 등록 및 정품 인증 단계를 완료 해야 있습니다. [작업 또는 학교에 대 한 모바일 장치 등록](enroll-your-mobile-device.md)을 참조 하십시오.
  
> [!IMPORTANT]
> 사용자의 기본 설정된 언어 등록 프로세스에 의해 지원 되지 않으면 사용자가 다른 언어로 등록 알림 및 작업 단계는 모바일 장치에서 받을 수 있습니다. Office 365에서 지원 되는 일부 언어는 모바일 장치에는 등록 프로세스에 대 한 현재 지원 됩니다. 
  
Android 또는 iOS 장치를 사용 하는 사용자는 등록 프로세스의 일부로 회사 포털 응용 프로그램을 설치 해야 합니다.
  
## <a name="related-topics"></a>관련 항목

[모바일 장치 관리의 기능](capabilities-of-mobile-device-management.md)
  
[장치 보안 정책 만들기 및 배포](create-device-security-policies.md)
  

