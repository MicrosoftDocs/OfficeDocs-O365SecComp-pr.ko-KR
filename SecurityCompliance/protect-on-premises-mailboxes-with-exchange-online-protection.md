---
title: Exchange Online Protection을 사용 하 여 온-프레미스 사서함 보호
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/1/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- GEU150
- GMA150
- GPA150
- MET150
ms.assetid: c5e95951-da67-4ec7-92c5-982abd477e69
description: 온-프레미스에서 사서함의 일부 또는 전체를 호스트 하는 경우에도 EOP (Exchange Online Protection)를 사용 하 여 사서함을 보호할 수 있습니다. 커넥터를 구성 하려면 계정이 Office 365 전역 관리자 또는 Exchange 회사 관리자 (조직 관리 역할 그룹) 여야 합니다. office 365 권한이 Exchange 권한과 관련 된 방식에 대 한 자세한 내용은 21vianet에서 운영 하는 office 365에서 관리자 역할 할당을 참조 하세요. 모든 Exchange 사서함이 온-프레미스에 있는 경우 다음 단계를 수행 하 여 EOP 서비스를 설정 합니다.
ms.openlocfilehash: 01a364accd40bfd5889e7b0203cfaa7e156d0997
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216635"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a><span data-ttu-id="4cda2-106">Exchange Online Protection을 사용 하 여 온-프레미스 사서함 보호</span><span class="sxs-lookup"><span data-stu-id="4cda2-106">Protect on-premises mailboxes with Exchange Online Protection</span></span>

> [!NOTE]
> <span data-ttu-id="4cda2-107">이 문서는 중국의 21vianet에서 운영 하는 Office 365에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-107">This article applies only to Office 365 operated by 21Vianet in China.</span></span> 
  
<span data-ttu-id="4cda2-p102">온-프레미스에서 사서함의 일부 또는 전체를 호스트 하는 경우에도 EOP (Exchange Online Protection)를 사용 하 여 사서함을 보호할 수 있습니다. 커넥터를 구성 하려면 계정이 Office 365 전역 관리자 또는 Exchange 회사 관리자 (조직 관리 역할 그룹) 여야 합니다. office 365 권한이 Exchange 권한과 관련 된 방식에 대 한 자세한 내용은 [21vianet에서 운영 하는 office 365에서 관리자 역할 할당](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac)을 참조 하세요. 모든 Exchange 사서함이 온-프레미스에 있는 경우 다음 단계를 수행 하 여 EOP 서비스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p102">Even if you plan to host some or all of your mailboxes on-premises, you can still protect the mailboxes with Exchange Online Protection (EOP). To configure connectors, your account must be an Office 365 Global Admin, or an Exchange Company Administrator (the Organization Management role group). For information about how Office 365 permissions relate to Exchange permissions, see [Assigning admin roles in Office 365 operated by 21Vianet](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac). If all of your Exchange mailboxes are on-premise, follow these steps to set up your EOP service.</span></span> 
  
## <a name="step-1-use-the-office-365-admin-center-to-add-and-verify-your-domain"></a><span data-ttu-id="4cda2-112">1단계: Office 365 관리 센터를 사용하여 도메인 추가 및 확인</span><span class="sxs-lookup"><span data-stu-id="4cda2-112">Step 1: Use the Office 365 admin center to add and verify your domain</span></span>

1. <span data-ttu-id="4cda2-113">Office 365 관리 센터에서 설정으로 이동하여 서비스에 도메인을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-113">In the Office 365 admin center, navigate to Setup to add your domain to the service.</span></span>
    
2.  <span data-ttu-id="4cda2-114">도메인 소유권을 확인 하기 위해 포털의 단계에 따라 dns 호스팅 공급자에 게 해당 dns 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-114">Follow the steps in the portal to add the applicable DNS records to your DNS-hosting provider in order to verify domain ownership.</span></span> 
    
> [!TIP]
> <span data-ttu-id="4cda2-115">도메인 [및 사용자를 21vianet에서 운영 하는 office 365에 추가](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) 하 고, [dns 레코드를 관리할 때 office 365에 대 한 dns 레코드를 만들려면](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) 도메인을 서비스에 추가 하 고 dns를 구성할 때 참조 하면 도움이 되는 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-115">[Add your domain and users to Office 365 operated by 21Vianet](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) and [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) are helpful resources to reference as you add your domain to the service and configure DNS.</span></span> 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a><span data-ttu-id="4cda2-116">2단계: 받는 사람 추가 및 도메인 유형 구성</span><span class="sxs-lookup"><span data-stu-id="4cda2-116">Step 2: Add recipients and configure the domain type</span></span>

<span data-ttu-id="4cda2-p103">메일이 EOP 서비스를 통해 전달되도록 구성하려는 경우 먼저 받는 사람을 서비스에 추가하는 것이 좋습니다. [EOP에서 메일 사용자 관리](https://go.microsoft.com/fwlink/?LinkId=506782)에 설명된 것처럼 이러한 방법에는 몇 가지가 있습니다. 또한 받는 사람을 추가한 후에 서비스 내에서 받는 사람 확인을 적용하기 위해 DBEB(디렉터리 기반 Edge 차단)를 사용 가능하게 설정하려면 도메인 유형을 신뢰할 수 있음으로 설정해야 합니다. DBEB에 대한 자세한 내용은 [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p103">Before configuring your mail to flow to and from the EOP service, we recommend adding your recipients to the service. There are several ways in which you can do this, as documented in [Manage mail users in EOP](https://go.microsoft.com/fwlink/?LinkId=506782). Also, if you want to enable Directory Based Edge Blocking (DBEB) in order to enforce recipient verification within the service after adding your recipients, you need to set your domain type to Authoritative. For more information about DBEB, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781).</span></span>
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a><span data-ttu-id="4cda2-121">3단계: EAC를 사용하여 메일 흐름 설정</span><span class="sxs-lookup"><span data-stu-id="4cda2-121">Step 3: Use the EAC to set up mail flow</span></span>

<span data-ttu-id="4cda2-p104">EOP와 온-프레미스 메일 서버 간의 메일 흐름을 가능 하 게 하는 커넥터를 EAC (Exchange 관리 센터)에서 만듭니다. 자세한 내용은 [EOP를 통한 기본 전자 메일 흐름을 설정 하는 필수 커넥터 만들기](https://go.microsoft.com/fwlink/?LinkId=506780)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p104">Create connectors in the Exchange admin center (EAC) that enable mail flow between EOP and your on-premises mail servers. For detailed instructions, see [Create required connectors to set up basic email flow through EOP](https://go.microsoft.com/fwlink/?LinkId=506780).</span></span>
  
 <span data-ttu-id="4cda2-124">이 작업의 작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="4cda2-124">How do you know this task worked?</span></span> 
  
 <span data-ttu-id="4cda2-p105">원격 연결 분석기를 사용 하 여 서비스와 환경 간의 메일 흐름을 검사 하는 테스트를 실행 합니다. 자세한 내용은 [원격 연결 분석기를 사용 하 여 메일 흐름 테스트](https://go.microsoft.com/fwlink/?LinkId=506784)의 "원격 연결 분석기를 사용 하 여 전자 메일 배달 테스트" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p105">Use the Remote Connectivity Analyzer to run a test that checks mail flow between the service and your environment. For more information, see the "Use the Remote Connectivity Analyzer to test email delivery" section in [Test mail flow with the Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?LinkId=506784).</span></span>
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a><span data-ttu-id="4cda2-127">4단계: 인바운드 포트 25 SMTP 액세스 허용</span><span class="sxs-lookup"><span data-stu-id="4cda2-127">Step 4: Allow inbound port 25 SMTP access</span></span>

<span data-ttu-id="4cda2-p106">커넥터를 구성한 후에는 DNS 레코드 업데이트의 전파를 허용 하는 데 72 시간을 기다립니다. 이를 통해 방화벽 또는 메일 서버에서 인바운드 포트 25 SMTP 트래픽을 제한 하 여 EOP 데이터 센터 로부터의 메일 (특히 [21vianet에서 운영 하는 Office 365의 url 및 ip 주소 범위](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection)에 포함 된 주소)을 허용 하도록 합니다. 이를 통해 수신 하는 인바운드 메시지의 범위를 제한 하 여 온-프레미스 환경을 보호 합니다. 또한 메일 릴레이에 대 한 연결을 허용 하는 IP 주소를 제어 하는 설정이 사용자에 게 있는 경우에는 해당 설정도 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p106">After you configured connectors, wait 72 hours to allow propagation of your DNS-record updates. Following this, restrict inbound port-25 SMTP traffic on your firewall or mail servers to accept mail only from the EOP datacenters, specifically from the IP addresses listed at [URLs and IP address ranges for Office 365 operated by 21Vianet](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection). This protects your on-premises environment by limiting the scope of inbound messages you can receive. Additionally, if you have settings on your mail server that control the IP addresses allowed to connect for mail relay, update those settings as well.</span></span>
  
> [!TIP]
> <span data-ttu-id="4cda2-p107">연결 제한 시간을 60초로 지정하여 SMTP 서버의 설정을 구성합니다. 이 설정은 대부분의 상황에 적합하며 대용량 첨부 파일 포함된 메시지를 보내는 등의 경우 어느 정도의 지연이 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p107">Configure settings on the SMTP server with a connection time out of 60 seconds. This setting is acceptable for most situations, allowing for some delay in the case of a message sent with a large attachment, for instance.</span></span> 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a><span data-ttu-id="4cda2-134">5단계: 셸을 사용하여 스팸이 각 사용자의 정크 메일 폴더로 라우팅되도록 설정</span><span class="sxs-lookup"><span data-stu-id="4cda2-134">Step 5: Use the Shell to ensure that spam is routed to each user's junk email folder</span></span>

<span data-ttu-id="4cda2-p108">스팸 (정크) 전자 메일을 각 사용자의 정크 메일 폴더로 올바르게 라우팅해야 확인 하려면 몇 가지 구성 단계를 수행 해야 합니다. [각 사용자의 정크 메일 폴더로 스팸을 라우팅되도록 하기](https://go.microsoft.com/fwlink/?LinkId=506804)위한 단계를 제공 합니다. 각 사용자의 정크 메일 폴더로 메시지를 이동 하지 않으려면 Exchange 관리 센터에서 콘텐츠 필터 정책을 편집 하 여 다른 작업을 선택할 수 있습니다. 자세한 내용은 [콘텐츠 필터 정책 구성을](https://go.microsoft.com/fwlink/?LinkId=506805)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p108">To ensure that spam (junk) email is routed correctly to each user's Junk Email folder, you must perform a couple of configuration steps. The steps are provided in [Ensure that spam is routed to each user's Junk Email folder](https://go.microsoft.com/fwlink/?LinkId=506804). If you don't want to move messages to each user's Junk Email folder, you may choose another action by editing your content filter policies in the Exchange admin center. For more information, see [Configure Content Filter Policies](https://go.microsoft.com/fwlink/?LinkId=506805).</span></span> 
  
## <a name="step-6-use-the-office-365-admin-center-to-point-your-mx-record-to-eop"></a><span data-ttu-id="4cda2-139">6단계: Office 365 관리 센터를 사용하여 MX 레코드가 EOP를 가리키도록 지정</span><span class="sxs-lookup"><span data-stu-id="4cda2-139">Step 6: Use the Office 365 admin center to point your MX record to EOP</span></span>

<span data-ttu-id="4cda2-p109">Office 365 도메인 구성 단계에 따라 도메인의 MX 레코드를 업데이트 하 여 인바운드 전자 메일이 EOP를 통해 흐릅니다. 자세한 내용은 [dns 레코드를 관리할 때 Office 365에 대 한 dns 레코드 만들기](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b)를 다시 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p109">Follow the Office 365 domain configuration steps to update your MX record for your domain, so that your inbound email flows through EOP. For more information, you can again reference [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b).</span></span>
  
<span data-ttu-id="4cda2-142">이 작업의 작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="4cda2-142">How do you know this task worked?</span></span>
  
 <span data-ttu-id="4cda2-p110">원격 연결 분석기를 사용 하 여 MX 레코드를 확인 하는 테스트를 실행 합니다. 자세한 내용은 [원격 연결 분석기를 사용 하 여 메일 흐름 테스트](https://go.microsoft.com/fwlink/?LinkId=506784)의 "원격 연결 분석기를 사용 하 여 MX 레코드 및 아웃 바운드 커넥터 테스트" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p110">Use the Remote Connectivity Analyzer to run a test that verifies your MX record. For more information, see the "Use the Remote Connectivity Analyzer to test your MX record and Outbound connector" section in [Test mail flow with the Remote Connectivity Analyzer](https://go.microsoft.com/fwlink/?LinkId=506784).</span></span> 
  
<span data-ttu-id="4cda2-p111">이 시점은 제대로 구성된 아웃바운드 온-프레미스 커넥터에 대한 서비스 배달을 확인했으며 MX 레코드가 EOP를 가리키고 있는지 확인한 상태입니다. 이제 다음 추가 테스트를 실행하도록 선택하여 서비스에서 온-프레미스 환경으로 이메일이 전달되는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p111">At this point, you've verified service delivery for a properly configured Outbound on-premises connector, and you've verified that your MX record is pointing to EOP. You can now choose to run the following additional tests to verify that an email will be successfully delivered by the service to your on-premises environment:</span></span>
  
- <span data-ttu-id="4cda2-147">원격 연결 분석기에서 **Office 365** 탭을 클릭한 다음 **인터넷 전자 메일 테스트** 아래에 있는 **인바운드 SMTP 전자 메일** 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-147">In the Remote Connectivity Analyzer, click the **Office 365** tab, and then run the **Inbound SMTP Email** test located under **Internet Email Tests**.</span></span>
    
- <span data-ttu-id="4cda2-p112">도메인이 서비스에 추가한 도메인과 일치하는 조직의 메일 받는 사람에게 웹 기반 전자 메일 계정에서 전자 메일 메시지를 보냅니다. Microsoft Outlook 또는 다른 전자 메일 클라이언트를 사용하여 온-프레미스 사서함으로의 메시지 배달을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p112">Send an email message from any web-based email account to a mail recipient in your organization whose domain matches the domain you added to the service. Confirm delivery of the message to the on-premises mailbox using Microsoft Outlook or another email client.</span></span>
    
- <span data-ttu-id="4cda2-150">아웃바운드 전자 메일 테스트를 실행하려면 조직 사용자가 웹 기반 전자 메일 계정에 전자 메일을 보내도록 한 다음 메시지 수신을 확인하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-150">If you want to run an outbound email test, you can send an email message from a user in your organization to a web-based email account and confirm that the message is received.</span></span>
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a><span data-ttu-id="4cda2-151">덜 일반적인 경우: 온-프레미스 및 클라우드에서 사서함이 포함 된 하이브리드 설정</span><span class="sxs-lookup"><span data-stu-id="4cda2-151">Less common: A hybrid setup with mailboxes on-premises and in the cloud</span></span>

<span data-ttu-id="4cda2-p113">exchange Online에서 exchange 사서함 온-프레미스와 클라우드에서 하나 이상의 사서함을 사용 하는 경우 *하이브리드* 설치가 진행 됩니다. 하이브리드 설정에서 약속 있음/없음 일정 공유 및 메일 라우팅과 같은 기능은 온-프레미스 및 클라우드 환경에서 함께 작동 합니다. 사서함을 Exchange Online으로 전환 하는 동안 하이브리드 설치가 진행 되 고 있을 수 있습니다. 하이브리드 환경은 EOP 독립 실행형 보호와는 다른 방식으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p113">If you have Exchange mailboxes on-premises and one or more mailboxes in the cloud in Exchange Online, you have a  *hybrid*  setup. In a hybrid setup, features such as free/busy calendar sharing and mail routing work together in your on-premises and cloud environments. You might have a hybrid setup in place while you transition mailboxes to Exchange Online. A hybrid environment is set up differently than EOP standalone protection.</span></span> 
  
<span data-ttu-id="4cda2-p114">대부분의 직원에 대해 클라우드 기반 전자 메일을 활용 하려면 하이브리드 시나리오를 선택할 수 있습니다. 이 작업은 온-프레미스의 일부 사서함을 호스트 하는 동안에도 가능 합니다. 예를 들어 법률 부서에 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p114">You might choose a hybrid scenario to take advantage of cloud-based email for most of your employees. You can do this while also hosting some mailboxes on-premises; for example, for your legal department.</span></span> 
  
<span data-ttu-id="4cda2-p115">하이브리드 설치는 복잡할 수 있지만 다양 한 이점이 있습니다. exchange에서 하이브리드 시나리오를 설정 하는 방법에 대 한 자세한 내용은 [21vianet에서 운영 하는 Office 365을 사용 하 여 exchange 하이브리드 배포 기능 구성을](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cda2-p115">A hybrid setup can be complex, but it has many benefits. To learn more about setting up hybrid scenarios with Exchange, see [Configuring Exchange hybrid deployment features with Office 365 operated by 21Vianet](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d).</span></span>
  

