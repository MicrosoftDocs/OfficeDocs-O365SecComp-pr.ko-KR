---
title: EOP 서비스 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/23/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d74c6ddf-11b0-43ee-b298-8bb0340895f0
description: 이 항목에서는 Microsoft EOP(Exchange Online Protection)를 설정하는 방법에 대해 설명합니다. Office 365 도메인 마법사에서 여기로 이동했으며 Exchange Online Protection를 사용하지 않으려면 Office 365 도메인 마법사로 돌아갑니다. 커넥터 구성 방법에 대한 자세한 내용를 보려면 Configure mail flow using connectors in Office 365을 참조하세요.
ms.openlocfilehash: 96751f1f68e0b73c1d92b6868e99f4eb1c2739bf
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670613"
---
# <a name="set-up-your-eop-service"></a>EOP 서비스 설정

이 항목에서는 Microsoft EOP(Exchange Online Protection)를 설정하는 방법에 대해 설명합니다. Office 365 도메인 마법사에서 여기로 이동했으며 Exchange Online Protection를 사용하지 않으려면 Office 365 도메인 마법사로 돌아갑니다. 커넥터 구성 방법에 대한 자세한 내용를 보려면 [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx)을 참조하세요.
  
> [!NOTE]
> 여기서는 사용자에게 온-프레미스 사서함이 있으며 EOP를 통해 해당 사서함을 보호하려 한다고 가정합니다. 이를 독립 실행형 시나리오라고 합니다. Exchange Online을 사용하여 클라우드에서 모든 사서함을 호스트하려는 경우에는 이 항목의 모든 단계를 완료할 필요가 없습니다. [Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286312)으로 이동하여 등록을 하고 클라우드 사서함을 구입하면 됩니다. 온-프레미스와 클라우드 둘 다에서 사서함을 호스트하려는 경우를 하이브리드 시나리오라고 합니다. 이 시나리오에서는 고급 메일 흐름 설정을 사용해야 합니다. 하이브리드 메일 흐름에 대한 설명과 해당 메일 흐름을 설정하는 방법을 보여주는 리소스의 링크는 [Exchange Server 2013 Hybrid Deployments](http://technet.microsoft.com/library/59e32000-4fcf-417f-a491-f1d8f9aeef9b.aspx)에 나와 있습니다. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

- 이 작업의 예상 완료 시간: 1시간
    
- 커넥터를 구성하려면 Office 365 전역 관리자 또는 Exchange 회사 관리자(조직 관리 역할 그룹)여야 합니다. Office 365 사용 권한과 Exchange 사용 권한의 관계에 대한 자세한 내용은 [Office 365의 사용 권한](https://go.microsoft.com/fwlink/p/?LinkID=335814)을 참조하세요.
    
- 아직 EOP에 등록하지 않은 경우 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=282660)을 방문하여 서비스를 구입하거나 평가판을 신청합니다. 
    
- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.
    
> [!TIP]
> 문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 
  
## <a name="how-do-you-do-this"></a>어떻게 해야 합니까?

### <a name="step-1-use-the-microsoft-365-admin-center-to-add-and-verify-your-domain"></a>1 단계: Microsoft 365 관리 센터를 사용 하 여 도메인 추가 및 확인

1. Microsoft 365 관리 센터에서 **설정** 으로 이동 하 여 서비스에 도메인을 추가 합니다. 
    
    Microsoft 365 관리 센터를 어디에서 찾을 수 있나요? 자세한 내용은 [Microsoft 365 관리 센터를](https://go.microsoft.com/fwlink/p/?LinkId=521888)참고 하세요.
    
2. 도메인 소유권 확인을 위해 해당 DNS 레코드를 DNS 호스팅 공급자에 추가하는 단계를 수행합니다.
    
> [!TIP]
> 서비스에 도메인을 추가하고 DNS를 구성할 때 참조하면 유용한 리소스인 [Office 365에 도메인 추가](https://support.office.com/en-us/article/add-a-domain-to-office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611) 및 [Office 365용 DNS 레코드 만들기](https://support.office.com/en-us/article/create-dns-records-at-any-dns-hosting-provider-for-office-365-7b7b075d-79f9-4e37-8a9e-fb60c1d95166)의 내용을 확인하십시오. 
  
### <a name="step-2-add-recipients-and-optionally-enable-dbeb"></a>2단계: 받는 사람을 추가하고 선택적으로 DBEB 사용

메일이 EOP 서비스를 통해 전달되도록 구성하려는 경우 먼저 받는 사람을 서비스에 추가하는 것이 좋습니다. [EOP에서 메일 사용자 관리](manage-mail-users-in-eop.md)에 설명된 것처럼 이러한 방법에는 몇 가지가 있습니다. 또한 받는 사람을 추가한 후에 서비스 내에서 받는 사람 확인을 적용하기 위해 DBEB(디렉터리 기반 Edge 차단)를 사용 가능하게 설정하려면 도메인 유형을 신뢰할 수 있음으로 설정해야 합니다. DBEB에 대한 자세한 내용은 [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)를 참조하세요.
  
### <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>3단계: EAC를 사용하여 메일 흐름 설정

EOP 및 온-프레미스 메일 서버 간의 메일 흐름을 가능하게 하는 커넥터를 EAC(Exchange 관리 센터)에서 만듭니다. 자세한 내용은 [Set up connectors to route mail between Office 365 and your own email servers](http://technet.microsoft.com/library/2e93fd60-a5ef-4e64-8e62-2b862b2d1033.aspx)을 참조하세요.
  
#### <a name="how-do-you-know-this-task-worked"></a>이 작업의 작동 여부는 어떻게 확인하나요?

원격 연결 분석기를 사용하여 서비스와 환경 간의 메일 흐름을 검사하는 테스트를 실행합니다. 자세한 내용은 [Testing Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx)의 "원격 연결 분석기를 사용하여 이메일 배달 테스트" 섹션을 참조하세요.
  
### <a name="step-4-allow-inbound-port-25-smtp-access"></a>4단계: 인바운드 포트 25 SMTP 액세스 허용

커넥터를 구성한 후에 DNS 레코드 업데이트가 전파될 수 있게 72시간 동안 기다립니다. 그런 후에 EOP 데이터 센터(구체적으로는 [Exchange Online Protection IP 주소](exchange-online-protection-ip-addresses.md)에 나와 있는 IP 주소)에서 보내는 메일만 수락하도록 방화벽이나 메일 서버의 인바운드 포트 25 SMTP 트래픽을 제한합니다. 이렇게 하면 수신 가능한 인바운드 메시지 범위를 제한하여 온-프레미스 환경을 보호할 수 있습니다. 또한 메일 릴레이를 위한 연결이 허용된 IP 주소를 제어하는 설정이 메일 서버에 있는 경우에는 해당 설정도 업데이트합니다.
  
> [!TIP]
> 연결 제한 시간을 60초로 지정하여 SMTP 서버의 설정을 구성합니다. 이 설정은 대부분의 상황에 적합하며 대용량 첨부 파일 포함된 메시지를 보내는 등의 경우 어느 정도의 지연이 허용됩니다. 
  
### <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>5단계: 셸을 사용하여 스팸이 각 사용자의 정크 메일 폴더로 라우팅되도록 설정

스팸(정크) 메일이 각 사용자의 정크 메일 폴더로 라우팅되도록 하려면 몇 가지 구성 단계를 수행해야 합니다. [각 사용자의 정크 메일 폴더로 스팸을 라우팅되도록 하기](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)위한 단계를 제공 합니다.
  
각 사용자의 정크 메일 폴더로 메시지를 옮기지 않으려면 Exchange 관리 센터에서 콘텐츠 필터 정책을 편집하여 다른 작업을 선택할 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성을](../configure-your-spam-filter-policies.md)참조 하세요.
  
### <a name="step-6-use-the-microsoft-365-admin-center-to-point-your-mx-record-to-eop"></a>6 단계: Microsoft 365 관리 센터를 사용 하 여 MX 레코드가 EOP를 가리키도록 지정

Office 365 도메인 구성 단계에 따라 도메인의 MX 레코드를 업데이트하여 인바운드 전자 메일이 EOP를 통해 이동하도록 할 수 있습니다. 타사 필터링 서비스가 전자 메일을 EOP로 릴레이할 때와 달리 MX 레코드가 EOP를 직접 가리키도록 해야 합니다. 자세한 내용은 [Office 365용 DNS 레코드 만들기](https://go.microsoft.com/fwlink/p/?LinkId=304219)를 참조하세요.
  
#### <a name="how-do-you-know-this-task-worked"></a>이 작업의 작동 여부는 어떻게 확인하나요?

원격 연결 분석기를 사용하여 MX 레코드를 확인하는 테스트를 실행합니다. 자세한 내용은 [Testing Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx)의 "원격 연결 분석기를 사용하여 MX 레코드 및 아웃바운드 커넥터 테스트" 섹션을 참조하세요. 
  
이 시점은 제대로 구성된 아웃바운드 온-프레미스 커넥터에 대한 서비스 배달을 확인했으며 MX 레코드가 EOP를 가리키고 있는지 확인한 상태입니다. 이제 다음 추가 테스트를 실행하도록 선택하여 서비스에서 온-프레미스 환경으로 이메일이 전달되는지 확인할 수 있습니다.
  
- 원격 연결 분석기에서 **Office 365** 탭을 클릭한 다음 **인터넷 전자 메일 테스트** 아래에 있는 **인바운드 SMTP 전자 메일** 테스트를 실행합니다. 
    
- 도메인이 서비스에 추가한 도메인과 일치하는 조직의 메일 받는 사람에게 웹 기반 전자 메일 계정에서 전자 메일 메시지를 보냅니다. Microsoft Outlook 또는 다른 전자 메일 클라이언트를 사용하여 온-프레미스 사서함으로의 메시지 배달을 확인합니다.
    
- 아웃바운드 전자 메일 테스트를 실행하려면 조직 사용자가 웹 기반 전자 메일 계정에 전자 메일을 보내도록 한 다음 메시지 수신을 확인하면 됩니다.
    
> [!TIP]
> 설정이 완료된 후 EOP에서 스팸 및 맬웨어를 제거하도록 추가 단계를 수행할 필요는 없습니다. EOP는 스팸과 맬웨어를 자동으로 제거합니다. 그러나 비즈니스 요구 사항에 따라 EAC에서 설정을 미세 조정할 수는 있습니다. 자세한 내용은 [Anti-Spam and Anti-Malware Protection](http://technet.microsoft.com/library/93c6c227-7442-4293-b64d-ec8f15c928db.aspx)을 참조하십시오. > 서비스가 실행되면 EOP 설정 후의 고려 사항 및 권장 설정에 대해 설명하는 [EOP 구성을 위한 모범 사례](best-practices-for-configuring-eop.md)를 읽어보는 것이 좋습니다. 
  

