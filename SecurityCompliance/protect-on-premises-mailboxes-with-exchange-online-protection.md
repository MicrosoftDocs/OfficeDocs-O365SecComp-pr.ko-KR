---
title: Exchange Online Protection을 사용 하 여 온-프레미스 사서함 보호
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 6/1/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- GEU150
- GMA150
- GPA150
- MET150
ms.assetid: c5e95951-da67-4ec7-92c5-982abd477e69
ms.collection:
- M365-security-compliance
description: 온-프레미스에서 사서함의 일부 또는 전체를 호스트 하는 경우에도 EOP (Exchange Online Protection)를 사용 하 여 사서함을 보호할 수 있습니다. 커넥터를 구성하려면 Office 365 전역 관리자 또는 Exchange 회사 관리자(조직 관리 역할 그룹)여야 합니다. Office 365 권한이 Exchange 권한과 관련 된 방식에 대 한 자세한 내용은 21Vianet에서 운영 하는 Office 365에서 관리자 역할 할당을 참조 하세요. 모든 Exchange 사서함이 온-프레미스에 있는 경우 다음 단계를 수행 하 여 EOP 서비스를 설정 합니다.
ms.openlocfilehash: 787c01ff7d06943b51916675b9e30dc3f020d5e1
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600494"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a>Exchange Online Protection을 사용 하 여 온-프레미스 사서함 보호

> [!NOTE]
> 이 문서는 중국의 21Vianet에서 운영 하는 Office 365에만 적용 됩니다. 
  
온-프레미스에서 사서함의 일부 또는 전체를 호스트 하는 경우에도 EOP (Exchange Online Protection)를 사용 하 여 사서함을 보호할 수 있습니다. 커넥터를 구성하려면 Office 365 전역 관리자 또는 Exchange 회사 관리자(조직 관리 역할 그룹)여야 합니다. Office 365 권한이 Exchange 권한과 관련 된 방식에 대 한 자세한 내용은 [21vianet에서 운영 하는 office 365에서 관리자 역할 할당](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac)을 참조 하세요. 모든 Exchange 사서함이 온-프레미스에 있는 경우 다음 단계를 수행 하 여 EOP 서비스를 설정 합니다. 
  
## <a name="step-1-use-the-microsoft-365-admin-center-to-add-and-verify-your-domain"></a>1 단계: Microsoft 365 관리 센터를 사용 하 여 도메인 추가 및 확인

1. Microsoft 365 관리 센터에서 설정으로 이동 하 여 서비스에 도메인을 추가 합니다.
    
2.  도메인 소유권을 확인 하기 위해 포털의 단계에 따라 DNS 호스팅 공급자에 게 해당 DNS 레코드를 추가 합니다. 
    
> [!TIP]
> 도메인 [및 사용자를 21vianet에서 운영 하는 office 365에 추가](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) 하 고, [dns 레코드를 관리할 때 office 365에 대 한 Dns 레코드를 만들려면](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) 도메인을 서비스에 추가 하 고 dns를 구성할 때 참조 하면 도움이 되는 리소스입니다. 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a>2 단계: 받는 사람 추가 및 도메인 유형 구성

메일이 EOP 서비스를 통해 전달되도록 구성하려는 경우 먼저 받는 사람을 서비스에 추가하는 것이 좋습니다. [EOP에서 메일 사용자 관리](https://go.microsoft.com/fwlink/?LinkId=506782)에 설명된 것처럼 이러한 방법에는 몇 가지가 있습니다. 또한 받는 사람을 추가한 후에 서비스 내에서 받는 사람 확인을 적용하기 위해 DBEB(디렉터리 기반 Edge 차단)를 사용 가능하게 설정하려면 도메인 유형을 신뢰할 수 있음으로 설정해야 합니다. DBEB에 대한 자세한 내용은 [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781)를 참조하세요.
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>3단계: EAC를 사용하여 메일 흐름 설정

EOP 및 온-프레미스 메일 서버 간의 메일 흐름을 가능하게 하는 커넥터를 EAC(Exchange 관리 센터)에서 만듭니다. 자세한 내용은 [EOP를 통한 기본 전자 메일 흐름을 설정 하는 필수 커넥터 만들기](https://go.microsoft.com/fwlink/?LinkId=506780)를 참조 하세요.
  
 이 작업의 작동 여부를 확인하려면 어떻게 해야 합니까? 
  
 원격 연결 분석기를 사용하여 서비스와 환경 간의 메일 흐름을 검사하는 테스트를 실행합니다. 자세한 내용은 [원격 연결 분석기를 사용 하 여 메일 흐름 테스트](https://go.microsoft.com/fwlink/?LinkId=506784)의 "원격 연결 분석기를 사용 하 여 전자 메일 배달 테스트" 섹션을 참조 하십시오.
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a>4단계: 인바운드 포트 25 SMTP 액세스 허용

커넥터를 구성한 후에 DNS 레코드 업데이트가 전파될 수 있게 72시간 동안 기다립니다. 이를 통해 방화벽 또는 메일 서버에서 인바운드 포트 25 SMTP 트래픽을 제한 하 여 EOP 데이터 센터 로부터의 메일 (특히 [21vianet에서 운영 하는 Office 365의 url 및 ip 주소 범위](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection)에 포함 된 주소)을 허용 하도록 합니다. 이렇게 하면 수신 가능한 인바운드 메시지 범위를 제한하여 온-프레미스 환경을 보호할 수 있습니다. 또한 메일 릴레이를 위한 연결이 허용된 IP 주소를 제어하는 설정이 메일 서버에 있는 경우에는 해당 설정도 업데이트합니다.
  
> [!TIP]
> 연결 제한 시간을 60초로 지정하여 SMTP 서버의 설정을 구성합니다. 이 설정은 대부분의 상황에 적합하며 대용량 첨부 파일 포함된 메시지를 보내는 등의 경우 어느 정도의 지연이 허용됩니다. 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>5단계: 셸을 사용하여 스팸이 각 사용자의 정크 메일 폴더로 라우팅되도록 설정

스팸(정크) 메일이 각 사용자의 정크 메일 폴더로 라우팅되도록 하려면 몇 가지 구성 단계를 수행해야 합니다. [각 사용자의 정크 메일 폴더로 스팸을 라우팅되도록 하기](https://go.microsoft.com/fwlink/?LinkId=506804)위한 단계를 제공 합니다. 각 사용자의 정크 메일 폴더로 메시지를 옮기지 않으려면 Exchange 관리 센터에서 콘텐츠 필터 정책을 편집하여 다른 작업을 선택할 수 있습니다. 자세한 내용은 [Configure Content Filter Policies](https://go.microsoft.com/fwlink/?LinkId=506805)을 참조하세요. 
  
## <a name="step-6-use-the-microsoft-365-admin-center-to-point-your-mx-record-to-eop"></a>6 단계: Microsoft 365 관리 센터를 사용 하 여 MX 레코드가 EOP를 가리키도록 지정

Office 365 도메인 구성 단계에 따라 도메인의 MX 레코드를 업데이트하여 인바운드 전자 메일이 EOP를 통해 이동하도록 할 수 있습니다. 자세한 내용은 [dns 레코드를 관리할 때 Office 365에 대 한 dns 레코드 만들기](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b)를 다시 참조 하십시오.
  
이 작업의 작동 여부는 어떻게 확인합니까?
  
 원격 연결 분석기를 사용하여 MX 레코드를 확인하는 테스트를 실행합니다. 자세한 내용은 [원격 연결 분석기를 사용 하 여 메일 흐름 테스트](https://go.microsoft.com/fwlink/?LinkId=506784)의 "원격 연결 분석기를 사용 하 여 MX 레코드 및 아웃 바운드 커넥터 테스트" 섹션을 참조 하십시오. 
  
이 시점은 제대로 구성된 아웃바운드 온-프레미스 커넥터에 대한 서비스 배달을 확인했으며 MX 레코드가 EOP를 가리키고 있는지 확인한 상태입니다. 이제 다음 추가 테스트를 실행하도록 선택하여 서비스에서 온-프레미스 환경으로 이메일이 전달되는지 확인할 수 있습니다.
  
- 원격 연결 분석기에서 **Office 365** 탭을 클릭한 다음 **인터넷 전자 메일 테스트** 아래에 있는 **인바운드 SMTP 전자 메일** 테스트를 실행합니다.
    
- 도메인이 서비스에 추가한 도메인과 일치하는 조직의 메일 받는 사람에게 웹 기반 전자 메일 계정에서 전자 메일 메시지를 보냅니다. Microsoft Outlook 또는 다른 전자 메일 클라이언트를 사용하여 온-프레미스 사서함으로의 메시지 배달을 확인합니다.
    
- 아웃바운드 전자 메일 테스트를 실행하려면 조직 사용자가 웹 기반 전자 메일 계정에 전자 메일을 보내도록 한 다음 메시지 수신을 확인하면 됩니다.
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a>덜 일반적인 경우: 온-프레미스 및 클라우드에서 사서함이 포함 된 하이브리드 설정

Exchange Online에서 Exchange 사서함 온-프레미스와 클라우드에서 하나 이상의 사서함을 사용 하는 경우 *하이브리드* 설치가 진행 됩니다. 하이브리드 설정에서 약속 있음/없음 일정 공유 및 메일 라우팅과 같은 기능은 온-프레미스 및 클라우드 환경에서 함께 작동 합니다. 사서함을 Exchange Online으로 전환 하는 동안 하이브리드 설치가 진행 되 고 있을 수 있습니다. 하이브리드 환경은 EOP 독립 실행형 보호와는 다른 방식으로 설정 됩니다. 
  
대부분의 직원에 대해 클라우드 기반 전자 메일을 활용 하려면 하이브리드 시나리오를 선택할 수 있습니다. 이 작업은 온-프레미스의 일부 사서함을 호스트 하는 동안에도 가능 합니다. 예를 들어 법률 부서에 적합 합니다. 
  
하이브리드 설치는 복잡할 수 있지만 다양 한 이점이 있습니다. Exchange에서 하이브리드 시나리오를 설정 하는 방법에 대 한 자세한 내용은 [21vianet에서 운영 하는 Office 365을 사용 하 여 exchange 하이브리드 배포 기능 구성을](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d)참조 하세요.
  

