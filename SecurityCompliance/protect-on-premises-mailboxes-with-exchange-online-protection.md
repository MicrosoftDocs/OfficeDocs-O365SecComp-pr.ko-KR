---
title: Exchange Online 보호와 함께 온-프레미스 사서함을 보호 합니다.
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/1/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- GEU150
- GMA150
- GPA150
- MET150
ms.assetid: c5e95951-da67-4ec7-92c5-982abd477e69
description: 사서함에서 온-프레미스의 일부 또는 전부를 호스트 하려는 경우에 여전히와 Exchange Online Protection (EOP) 사서함을 보호할 수 있습니다. 커넥터를 구성 하려면 사용자 계정이 Office 365 전역 관리자 또는 Exchange 회사 관리자 (조직 관리 역할 그룹) 여야 합니다. Exchange 권한을 Office 365 사용 권한 관련 되는 방법에 대 한 정보를 21Vianet에서 운영 하는 Office 365의 관리 역할 할당을 참조 하십시오. 온-프레미스 Exchange 사서함의 모든 경우에 EOP 서비스를 설정 하려면 다음이 단계를 수행 합니다.
ms.openlocfilehash: 4751bb2183e61d292805d1799519644b77b08c2a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534149"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a>Exchange Online 보호와 함께 온-프레미스 사서함을 보호 합니다.

> [!NOTE]
> 이 문서는 중국에서 21Vianet으로 운영 하는 Office 365에만 적용 됩니다. 
  
사서함에서 온-프레미스의 일부 또는 전부를 호스트 하려는 경우에 여전히와 Exchange Online Protection (EOP) 사서함을 보호할 수 있습니다. 커넥터를 구성 하려면 사용자 계정이 Office 365 전역 관리자 또는 Exchange 회사 관리자 (조직 관리 역할 그룹) 여야 합니다. Exchange 권한을 Office 365 사용 권한 관련 되는 방법에 대 한 정보를 [21Vianet에서 운영 하는 Office 365의 관리 역할 할당을](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac)참조 하십시오. 온-프레미스 Exchange 사서함의 모든 경우에 EOP 서비스를 설정 하려면 다음이 단계를 수행 합니다. 
  
## <a name="step-1-use-the-office-365-admin-center-to-add-and-verify-your-domain"></a>1단계: Office 365 관리 센터를 사용하여 도메인 추가 및 확인

1. Office 365 관리 센터에서 설정으로 이동하여 서비스에 도메인을 추가합니다.
    
2.  도메인 소유권을 확인 하기 위해 해당 DNS 레코드를 DNS 호스팅 공급자 추가를 포털의 단계를 수행 합니다. 
    
> [!TIP]
> [도메인 추가 및 사용자를 Office 365 21Vianet으로 운영 하](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) 고 [DNS 레코드를 관리 하는 경우 Office 365 용 DNS 레코드 만들기](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) 서비스에 도메인을 추가 하 고 DNS를 구성할 때 참조 하면 유용한 리소스인 됩니다. 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a>2단계: 받는 사람 추가 및 도메인 유형 구성

메일이 EOP 서비스를 통해 전달되도록 구성하려는 경우 먼저 받는 사람을 서비스에 추가하는 것이 좋습니다. [EOP에서 메일 사용자 관리](https://go.microsoft.com/fwlink/?LinkId=506782)에 설명된 것처럼 이러한 방법에는 몇 가지가 있습니다. 또한 받는 사람을 추가한 후에 서비스 내에서 받는 사람 확인을 적용하기 위해 DBEB(디렉터리 기반 Edge 차단)를 사용 가능하게 설정하려면 도메인 유형을 신뢰할 수 있음으로 설정해야 합니다. DBEB에 대한 자세한 내용은 [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781)를 참조하세요.
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>3단계: EAC를 사용하여 메일 흐름 설정

EOP 및 온-프레미스 메일 서버 간의 메일 흐름을 사용할 수 있는 Exchange 관리 센터 (EAC)에서 커넥터를 만듭니다. 자세한 내용은 [만들기 필요한 EOP 통한 기본 전자 메일 흐름 설정에 대 한 커넥터를](https://go.microsoft.com/fwlink/?LinkId=506780)참조 하십시오.
  
 이 작업의 작동 여부는 어떻게 확인하나요? 
  
 원격 연결 분석기를 사용 하 여 서비스 및 환경 간의 메일 흐름을 검사 하는 테스트를 실행 합니다. 자세한 내용은 [원격 연결 분석기를 사용 하 여 메일 흐름 테스트](https://go.microsoft.com/fwlink/?LinkId=506784)에서 "사용 하 여 원격 연결 분석기 테스트 전자 메일 배달" 섹션을 참조 하십시오.
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a>4단계: 인바운드 포트 25 SMTP 액세스 허용

커넥터를 구성 해 놓은 후에 DNS 레코드 업데이트의 전파를 허용 하도록 72 시간 대기 합니다. 그런 다음에 [Url 및 IP 주소 21Vianet에서 운영 하는 Office 365에 대 한 범위에](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection)나열 된 IP 주소에서 특히 EOP 데이터 센터에서에서 메일을 수락 하도록 방화벽 또는 메일 서버에서 인바운드 포트 25 SMTP 트래픽을 제한 합니다. 인바운드 메시지를 받을 수의 범위를 제한 하 여 온-프레미스 환경을 보호 됩니다. 또한 메일 릴레이 하기 위해 연결할 수 있도록 허용 하는 IP 주소를 제어 하는 메일 서버에서 설정 하는 경우 이러한 설정은를 업데이트 합니다.
  
> [!TIP]
> 연결 제한 시간을 60초로 지정하여 SMTP 서버의 설정을 구성합니다. 이 설정은 대부분의 상황에 적합하며 대용량 첨부 파일 포함된 메시지를 보내는 등의 경우 어느 정도의 지연이 허용됩니다. 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>5단계: 셸을 사용하여 스팸이 각 사용자의 정크 메일 폴더로 라우팅되도록 설정

스팸 (정크) 전자 메일을 각 사용자의 정크 메일 폴더로 올바르게 라우팅됩니다 되도록는 관련 된 몇가지 구성 단계를 수행 해야 합니다. 단계는 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인](https://go.microsoft.com/fwlink/?LinkId=506804)에 제공 됩니다. 각 사용자의 정크 메일 폴더로 메시지 이동 하지 않으려면 하는 경우에 Exchange 관리 센터에서 콘텐츠 필터 정책을 편집 하 여 다른 작업을 선택할 수 있습니다. 자세한 내용은 [콘텐츠 필터 정책 구성](https://go.microsoft.com/fwlink/?LinkId=506805)을 참조 하십시오. 
  
## <a name="step-6-use-the-office-365-admin-center-to-point-your-mx-record-to-eop"></a>6단계: Office 365 관리 센터를 사용하여 MX 레코드가 EOP를 가리키도록 지정

EOP를 통한 인바운드 전자 메일 흐름 되도록 해당 도메인에 대해 MX 레코드를 업데이트 하는 Office 365 도메인 구성 단계를 따릅니다. 자세한 정보에 대 한 [DNS 레코드를 관리 하는 경우 Office 365 용 DNS 레코드 만들기](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b)를 다시 참조할 수 있습니다.
  
이 작업의 작동 여부는 어떻게 확인하나요?
  
 원격 연결 분석기를 사용 하 여 MX 레코드를 확인 하는 테스트를 실행 합니다. 자세한 내용은 [원격 연결 분석기를 사용 하 여 메일 흐름 테스트](https://go.microsoft.com/fwlink/?LinkId=506784)에서 "사용 하 여 원격 연결 분석기 MX 레코드 및 아웃 바운드 커넥터 테스트" 섹션을 참조 하십시오. 
  
이 시점은 제대로 구성된 아웃바운드 온-프레미스 커넥터에 대한 서비스 배달을 확인했으며 MX 레코드가 EOP를 가리키고 있는지 확인한 상태입니다. 이제 다음 추가 테스트를 실행하도록 선택하여 서비스에서 온-프레미스 환경으로 이메일이 전달되는지 확인할 수 있습니다.
  
- 원격 연결 분석기에서 **Office 365** 탭을 클릭한 다음 **인터넷 전자 메일 테스트** 아래에 있는 **인바운드 SMTP 전자 메일** 테스트를 실행합니다.
    
- 도메인이 서비스에 추가한 도메인과 일치하는 조직의 메일 받는 사람에게 웹 기반 전자 메일 계정에서 전자 메일 메시지를 보냅니다. Microsoft Outlook 또는 다른 전자 메일 클라이언트를 사용하여 온-프레미스 사서함으로의 메시지 배달을 확인합니다.
    
- 아웃바운드 전자 메일 테스트를 실행하려면 조직 사용자가 웹 기반 전자 메일 계정에 전자 메일을 보내도록 한 다음 메시지 수신을 확인하면 됩니다.
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a>공통 덜: 사서함 온-프레미스 및 클라우드에서 하이브리드 설치 프로그램

Exchange 온-프레미스 사서함을 사용 하는 경우 및 하나 이상의 사서함을 Exchange Online에서 클라우드에서 *하이브리드* 설치 해야 합니다. 하이브리드 설치와 같은 기능 약속 있음/없음 일정 공유 및 작동 하 여 온-프레미스 및 클라우드 환경을 메일 라우팅. Exchange Online으로 사서함을 전환 하는 동안 하이브리드 설치 위치에 있을 수 있습니다. 하이브리드 환경 EOP 독립 실행형 보호 다르게 설정 됩니다. 
  
대부분의 직원 들에 대 한 클라우드 기반 전자 메일을 활용 하는 하이브리드 시나리오를 선택할 수도 있습니다. 또한 일부 온-프레미스 사서함;를 호스트 하는 동안 수행할 수 있는 작업 예: 법률 부서 합니다. 
  
하이브리드 설치 복잡할 수 있지만 많은 이점이 있습니다. Exchange와 하이브리드 시나리오를 설정 하는 방법에 대 한 자세한 내용을 보려면 [21Vianet에서 운영 하는 Office 365와 함께 구성 Exchange 하이브리드 배포 기능](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d)을 참조 하십시오.
  

