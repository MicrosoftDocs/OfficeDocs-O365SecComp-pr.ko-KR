---
title: Office 365 Cloud App Security와 SIEM 서버 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: siem server를 Office 365 Cloud App Security와 통합할 수 있습니다. 이 문서를 읽으면 작동 방식 및 설정 방법에 대 한 개요를 볼 수 있습니다.
ms.openlocfilehash: 82b5e0e6467bd42acba3c40d67e4e0363a7e0f72
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254788"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="ac45f-104">Office 365 Cloud App Security와 SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="ac45f-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="ac45f-105">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ac45f-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="ac45f-106">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ac45f-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="ac45f-107">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ac45f-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="ac45f-108">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ac45f-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="ac45f-109">평가 시작</span><span class="sxs-lookup"><span data-stu-id="ac45f-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="ac45f-110">계획 시작</span><span class="sxs-lookup"><span data-stu-id="ac45f-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="ac45f-111">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="ac45f-111">You are here!</span></span>  <br/> [<span data-ttu-id="ac45f-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="ac45f-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="ac45f-113">활용 시작</span><span class="sxs-lookup"><span data-stu-id="ac45f-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a><span data-ttu-id="ac45f-114">개요 및 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="ac45f-114">Overview and prerequisites</span></span>

<span data-ttu-id="ac45f-115">[Office 365 Cloud App security](get-ready-for-office-365-cas.md) 을 siem (보안 정보 및 이벤트 관리) 서버와 통합 하 여 중앙 집중식 경고 모니터링을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-115">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts.</span></span> <span data-ttu-id="ac45f-116">이는 클라우드 서비스 및 온-프레미스 서버 응용 프로그램을 사용 하는 조직에 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-116">This is especially beneficial for organizations who are using cloud services and on-premises server applications.</span></span> <span data-ttu-id="ac45f-117">siem 서버를 통합 하 여 Office 365 Cloud App Security의 알림 및 활동을 siem 서버로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-117">You can integrate your SIEM server to pull alerts and activities from Office 365 Cloud App Security into your SIEM server.</span></span> <span data-ttu-id="ac45f-118">siem server와의 통합을 통해 보안 팀은 일반적인 보안 절차를 자동화 하 고 클라우드 기반 및 온-프레미스 이벤트 간의 상관 관계를 자동으로 유지 하 여 Office 365 응용 프로그램을 보다 효율적으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-118">Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="ac45f-119">siem server를 Office 365 Cloud App Security와 처음 통합 하면 지난 2 일의 알림이 siem 서버에 전달 되 고, 선택한 모든 필터를 기반으로 하는 모든 경고가 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-119">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select).</span></span> <span data-ttu-id="ac45f-120">또한 연장 된 기간에 대해이 기능을 사용 하지 않도록 설정 하면 다시 사용 하도록 설정할 때 이전의 두 날의 알림을 전달 하 고 이후의 모든 경고를 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-120">Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>

### <a name="siem-integration-architecture"></a><span data-ttu-id="ac45f-121">siem 통합 아키텍처</span><span class="sxs-lookup"><span data-stu-id="ac45f-121">SIEM integration architecture</span></span>

<span data-ttu-id="ac45f-122">siem 에이전트는 조직의 네트워크에 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-122">A SIEM agent is set up in your organization's network.</span></span> <span data-ttu-id="ac45f-123">siem 에이전트는 배포 및 구성 된 경우 Office 365 Cloud App Security RESTful api를 사용 하 여 구성 된 (경고) 데이터 형식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-123">When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs.</span></span> <span data-ttu-id="ac45f-124">그런 다음 포트 443에서 암호화 된 HTTPS 채널을 통해 트래픽을 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-124">The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="ac45f-125">siem 에이전트가 Office 365 Cloud App Security에서 데이터를 검색 하는 경우 설치 중에 제공 되는 네트워크 구성 (TCP 또는 사용자 지정 포트를 사용 하 여 UDP)을 사용 하 여 로컬 siem 서버에 Syslog 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-125">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![siem 및 Cloud App Security 아키텍처](media/siem-architecture.png)

### <a name="supported-siem-servers"></a><span data-ttu-id="ac45f-127">지원 되는 siem 서버</span><span class="sxs-lookup"><span data-stu-id="ac45f-127">Supported SIEM servers</span></span>

<span data-ttu-id="ac45f-128">Office 365 Cloud App Security에서는 현재 다음과 같은 siem 서버를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-128">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="ac45f-129">마이크로 포커스 arcsight</span><span class="sxs-lookup"><span data-stu-id="ac45f-129">Micro Focus ArcSight</span></span>
- <span data-ttu-id="ac45f-130">일반 cef</span><span class="sxs-lookup"><span data-stu-id="ac45f-130">Generic CEF</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ac45f-131">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="ac45f-131">Prerequisites</span></span>

- <span data-ttu-id="ac45f-132">이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-132">You must be a global administrator or security administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="ac45f-133">[Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md) 보기</span><span class="sxs-lookup"><span data-stu-id="ac45f-133">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="ac45f-134">조직에 대해 [Office 365 Cloud App Security가 사용 하도록 설정](turn-on-office-365-cas.md) 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-134">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="ac45f-135">Office 365에 대해 [감사 로깅을](turn-audit-log-search-on-or-off.md) 켜야 함</span><span class="sxs-lookup"><span data-stu-id="ac45f-135">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="ac45f-136">siem 서버 통합을 구성 하기 위해 다음 요구 사항을 충족 하는 표준 서버가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-136">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="ac45f-137">OS: Windows 또는 Linux (가상 컴퓨터 일 수 있음)</span><span class="sxs-lookup"><span data-stu-id="ac45f-137">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="ac45f-138">CPU: 2</span><span class="sxs-lookup"><span data-stu-id="ac45f-138">CPU: 2</span></span>
    - <span data-ttu-id="ac45f-139">디스크 공간: 20gb</span><span class="sxs-lookup"><span data-stu-id="ac45f-139">Disk space: 20 GB</span></span>
    - <span data-ttu-id="ac45f-140">RAM: 2gb</span><span class="sxs-lookup"><span data-stu-id="ac45f-140">RAM: 2 GB</span></span>
    - <span data-ttu-id="ac45f-141">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) 설치</span><span class="sxs-lookup"><span data-stu-id="ac45f-141">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="ac45f-142">[네트워크 요구 사항](https://docs.microsoft.com/cloud-app-security/network-requirements) 에 설명 된 대로 방화벽이 구성 됨</span><span class="sxs-lookup"><span data-stu-id="ac45f-142">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="ac45f-143">**원격 syslog 호스트** 및 **syslot 포트 번호**에 대 한 세부 정보가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-143">You must have details about your **Remote syslog host** and **Syslot port number**.</span></span> <span data-ttu-id="ac45f-144">네트워크 관리자 또는 보안 관리자는 해당 정보를 찾는 데 도움을 드릴 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-144">A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="ac45f-145">siem 서버를 통합 하는 데 필요한 [JAR 파일](https://go.microsoft.com/fwlink/?linkid=838596) 을 다운로드 하려면 [소프트웨어 사용 조건](https://go.microsoft.com/fwlink/?linkid=862491) 에 동의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-145">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a><span data-ttu-id="ac45f-146">1 단계: Office 365 Cloud App Security에서 siem 에이전트로 설정</span><span class="sxs-lookup"><span data-stu-id="ac45f-146">Step 1: Set it up a SIEM agent in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="ac45f-147">Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-147">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="ac45f-148">**설정** \> **보안 확장**을 클릭 한 다음 siem 에이전트를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-148">Click **Settings** \> **Security extensions**, and then choose SIEM agents.</span></span><br/>
<span data-ttu-id="ac45f-149">![설정 > 보안 확장을 선택 합니다.](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-149">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

3. <span data-ttu-id="ac45f-150">**siem 에이전트 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-150">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="ac45f-151">![siem 에이전트 추가를 선택 합니다.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-151">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
4. <span data-ttu-id="ac45f-152">**마법사 시작**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-152">Choose **Start wizard**.</span></span><br/><span data-ttu-id="ac45f-153">![도움말 보기 또는 마법사 시작](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-153">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
5. <span data-ttu-id="ac45f-154">**일반** 단계에서 이름을 지정 하 고 **siem 형식을 선택한** 다음 해당 형식과 관련 된 **고급 설정을** 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-154">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format.</span></span> <span data-ttu-id="ac45f-155">다음을 \*\*\*\* 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-155">Then choose **Next**.</span></span><br/><span data-ttu-id="ac45f-156">![이름 및 유형 지정](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-156">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
6. <span data-ttu-id="ac45f-157">**원격 syslog** 단계에서 **원격 syslog 호스트** 의 IP 주소 또는 호스트 이름 및 **Syslog 포트 번호**를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-157">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**.</span></span> <span data-ttu-id="ac45f-158">원격 Syslog 프로토콜로 TCP 또는 UDP를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-158">Select TCP or UDP as the Remote Syslog protocol.</span></span> <span data-ttu-id="ac45f-159">(사용자가 없는 경우 네트워크 관리자 또는 보안 관리자와 함께 작업 하 여 이러한 세부 정보를 얻을 수 있습니다.) 다음을 \*\*\*\* 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-159">(You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="ac45f-160">![원격 Syslog 세부 정보 지정](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-160">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
7. <span data-ttu-id="ac45f-161">**데이터 형식** 단계에서 다음 중 하나를 수행한 후 **Next (다음**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-161">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="ac45f-162">**모든 알림의** 기본 설정 유지</span><span class="sxs-lookup"><span data-stu-id="ac45f-162">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="ac45f-163">또는</span><span class="sxs-lookup"><span data-stu-id="ac45f-163">OR</span></span>
    - <span data-ttu-id="ac45f-164">**모든 경고**를 클릭 한 다음 **특정 필터**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-164">Click **All alerts**, and then choose **Specific filters**.</span></span> <span data-ttu-id="ac45f-165">siem 서버에 보낼 알림 종류를 선택 하는 필터를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-165">Define filters to select the kinds of alerts you want to send to your SIEM server.</span></span>
<br/><span data-ttu-id="ac45f-166">![마법사의 데이터 형식 단계](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-166">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
8. <span data-ttu-id="ac45f-167">축 하 합니다 화면에서 토큰을 복사 하 고 나중에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-167">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![siem 에이전트 만들어짐 화면](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="ac45f-169">이제 Office 365 Cloud App Security에서 siem 에이전트를 설정 했지만 siem server 통합은 아직 완료 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-169">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished.</span></span> <span data-ttu-id="ac45f-170">다음 단계로 이동 하 여 siem server 통합을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-170">Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="ac45f-171">닫기를 클릭 하 고 마법사를 종료 한 후에는 보안 확장 화면에서 테이블에 추가한 siem 에이전트를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-171">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table.</span></span> <span data-ttu-id="ac45f-172">나중에 연결 될 때까지 **만들어진** 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-172">It will show a status of **Created** until it's connected later.</span></span>

![siem 에이전트를 만들었습니다.](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a><span data-ttu-id="ac45f-174">2 단계: siem 서버에서 JAR 파일 다운로드 및 실행</span><span class="sxs-lookup"><span data-stu-id="ac45f-174">Step 2: Download a JAR file and run it on your SIEM server</span></span>

1. <span data-ttu-id="ac45f-175">[Microsoft Cloud App Security siem 에이전트](https://go.microsoft.com/fwlink/?linkid=838596) 를 다운로드 하 고 폴더의 압축을 풉니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-175">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder.</span></span> <span data-ttu-id="ac45f-176">(계속 하려면 [소프트웨어 사용권 조항](https://go.microsoft.com/fwlink/?linkid=862491) 에 동의 해야 합니다.)</span><span class="sxs-lookup"><span data-stu-id="ac45f-176">(You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="ac45f-177">압축 폴더에서 .jar 파일을 추출 하 여 siem 서버에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-177">Extract the .jar file from the zipped folder and run it on your SIEM server.</span></span>
    
3. <span data-ttu-id="ac45f-178">파일을 실행 한 후 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-178">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a><span data-ttu-id="ac45f-179">중요 참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac45f-179">Important notes</span></span>

- <span data-ttu-id="ac45f-180">파일 이름은 siem 에이전트 버전에 따라 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-180">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="ac45f-181">서버 설치 중에 siem 서버에서 JAR 파일을 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-181">We recommend that you run the JAR file on your SIEM server during server setup.</span></span>

    - <span data-ttu-id="ac45f-182">**Windows**: 예약 된 작업으로 실행 하 고, **사용자의 로그온 여부에 관계 없이 실행** 되도록 작업을 구성 하 고, 작업이 다음 **보다 오래 실행 되 면 중지** 옵션의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-182">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="ac45f-183">**Linux**: **&** `rc.local` 파일에 with를 사용 하 여 run 명령을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-183">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="ac45f-184">예제:</span><span class="sxs-lookup"><span data-stu-id="ac45f-184">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="ac45f-185">대괄호의 매개 변수는 선택 사항이 며 관련성이 있는 경우에만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-185">Parameters in brackets [] are optional, and should be used only if relevant.</span></span> <span data-ttu-id="ac45f-186">다음 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-186">Use the following variables:</span></span>

    - <span data-ttu-id="ac45f-187">**tname** 은 로컬 에이전트 디버그 로그에 사용 하려는 디렉터리의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-187">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>

    - <span data-ttu-id="ac45f-188">**ADDRESS [:P ort]** 는 서버에서 인터넷에 연결 하는 데 사용 하는 프록시 서버 주소 및 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-188">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>

    - <span data-ttu-id="ac45f-189">**TOKEN** 은 첫 번째 절차에서 복사한 siem 에이전트 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-189">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>

    - <span data-ttu-id="ac45f-190">도움말을 보려면를 입력 `-h`합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-190">To get help, type `-h`.</span></span> 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="ac45f-191">3 단계: siem 에이전트가 작동 하는지 확인</span><span class="sxs-lookup"><span data-stu-id="ac45f-191">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="ac45f-192">Office 365 Cloud App Security 포털의 siem 에이전트 상태가 **연결 오류** 또는 **연결이 끊어져** 표시 되지 않으며 에이전트 알림이 없음을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-192">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="ac45f-193">예를 들어 다음과 같이 siem server가 연결 된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-193">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="ac45f-194">![siem 서버 연결 됨](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-194">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="ac45f-195">여기서는 siem server의 연결이 끊어져 있는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-195">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="ac45f-196">![siem 서버가 연결 되지 않음](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-196">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="ac45f-197">Syslog/siem server에서는 Office 365 Cloud App Security에서 알림이 수신 되었음을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-197">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="what-the-logfiles-look-like"></a><span data-ttu-id="ac45f-198">로그 파일이 어떤 모습 인지 확인</span><span class="sxs-lookup"><span data-stu-id="ac45f-198">What the logfiles look like</span></span>

<span data-ttu-id="ac45f-199">다음은 siem 서버로 전송 될 수 있는 경고 로그 파일 예입니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-199">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="ac45f-200">다음은 cef 형식에서이에 해당 하는 다른 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-200">And here's another sample, this time in CEF format:</span></span>


|<span data-ttu-id="ac45f-201">cef 필드 이름</span><span class="sxs-lookup"><span data-stu-id="ac45f-201">CEF field name</span></span>  | <span data-ttu-id="ac45f-202">설명</span><span class="sxs-lookup"><span data-stu-id="ac45f-202">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="ac45f-203">우선</span><span class="sxs-lookup"><span data-stu-id="ac45f-203">start</span></span>     | <span data-ttu-id="ac45f-204">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="ac45f-204">alert timestamp</span></span>        |
|<span data-ttu-id="ac45f-205">끝나야</span><span class="sxs-lookup"><span data-stu-id="ac45f-205">end</span></span>     | <span data-ttu-id="ac45f-206">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="ac45f-206">alert timestamp</span></span>        |
|<span data-ttu-id="ac45f-207">rt</span><span class="sxs-lookup"><span data-stu-id="ac45f-207">rt</span></span>     | <span data-ttu-id="ac45f-208">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="ac45f-208">alert timestamp</span></span>        |
|<span data-ttu-id="ac45f-209">.msg</span><span class="sxs-lookup"><span data-stu-id="ac45f-209">msg</span></span>     | <span data-ttu-id="ac45f-210">Office 365 Cloud App Security 포털에 표시 되는 경고 설명</span><span class="sxs-lookup"><span data-stu-id="ac45f-210">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="ac45f-211">suser</span><span class="sxs-lookup"><span data-stu-id="ac45f-211">suser</span></span>     | <span data-ttu-id="ac45f-212">알림 주체 사용자</span><span class="sxs-lookup"><span data-stu-id="ac45f-212">alert subject user</span></span>        |
|<span data-ttu-id="ac45f-213">destinationservicename</span><span class="sxs-lookup"><span data-stu-id="ac45f-213">destinationServiceName</span></span>     | <span data-ttu-id="ac45f-214">Office 365, SharePoint 또는 OneDrive와 같은 시작 응용 프로그램 알림</span><span class="sxs-lookup"><span data-stu-id="ac45f-214">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="ac45f-215">cslabel</span><span class="sxs-lookup"><span data-stu-id="ac45f-215">csLabel</span></span>     | <span data-ttu-id="ac45f-216">다양 한 의미를 갖는 레이블로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-216">Varies (labels have different meanings).</span></span> <span data-ttu-id="ac45f-217">일반적으로 레이블은 targetobjects와 같은 설명이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-217">Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="ac45f-218">진단</span><span class="sxs-lookup"><span data-stu-id="ac45f-218">cs</span></span>     | <span data-ttu-id="ac45f-219">레이블에 해당 하는 정보 (예: 레이블 예제에 대 한 경고의 대상 사용자)</span><span class="sxs-lookup"><span data-stu-id="ac45f-219">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |

## <a name="additional-tasks-as-needed"></a><span data-ttu-id="ac45f-220">추가 작업 (필요한 경우)</span><span class="sxs-lookup"><span data-stu-id="ac45f-220">Additional tasks (as needed)</span></span>

<span data-ttu-id="ac45f-221">siem 서버를 구성 하 고 Office 365 Cloud App Security과 통합 한 후에는 토큰을 다시 생성 하거나, siem 에이전트를 편집 하거나, siem 에이전트를 삭제 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-221">After you have configured your SIEM server and have integrated it with Office 365 Cloud App Security, you might need to regenerate a token, edit a SIEM agent, or delete a SIEM agent.</span></span> <span data-ttu-id="ac45f-222">다음 섹션에서는 이러한 작업을 수행 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-222">The following sections describe how to perform these tasks.</span></span>

### <a name="regenerate-a-token"></a><span data-ttu-id="ac45f-223">토큰 다시 생성</span><span class="sxs-lookup"><span data-stu-id="ac45f-223">Regenerate a token</span></span>

<span data-ttu-id="ac45f-224">토큰을 분실 한 경우 다시 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-224">If you lose your token, you can regenerate one.</span></span> 

1. <span data-ttu-id="ac45f-225">Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-225">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="ac45f-226">표에서 siem 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-226">In the table, locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="ac45f-227">줄임표를 클릭 한 다음 **토큰 다시 생성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-227">Click the ellipses, and then choose **Regenerate token**.</span></span><br/><span data-ttu-id="ac45f-228">![siem 에이전트에 대 한 줄임표를 클릭 하 여 토큰 다시 생성](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-228">![Regenerate a token by clicking the ellipsis for your SIEM agent](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span></span>
  
### <a name="edit-a-siem-agent"></a><span data-ttu-id="ac45f-229">siem 에이전트 편집</span><span class="sxs-lookup"><span data-stu-id="ac45f-229">Edit a SIEM agent</span></span>

1. <span data-ttu-id="ac45f-230">Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-230">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="ac45f-231">siem 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-231">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="ac45f-232">줄임표를 클릭 한 다음 **편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-232">Click the ellipses, and then choose **Edit**.</span></span> <span data-ttu-id="ac45f-233">siem 에이전트를 편집 하는 경우에는 .jar 파일을 다시 실행할 필요가 없으며 자동으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-233">(If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.)</span></span> <br/><span data-ttu-id="ac45f-234">![siem 에이전트를 편집 하려면 줄임표를 선택 하 고 편집을 선택 합니다.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-234">![To edit your SIEM agent, choose the ellipses, and then choose Edit.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span></span>
  
### <a name="delete-a-siem-agent"></a><span data-ttu-id="ac45f-235">siem 에이전트 삭제</span><span class="sxs-lookup"><span data-stu-id="ac45f-235">Delete a SIEM agent</span></span>

1. <span data-ttu-id="ac45f-236">Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-236">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="ac45f-237">siem 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-237">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="ac45f-238">줄임표를 클릭 한 다음 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac45f-238">Click the ellipses, and then choose **Delete**.</span></span><br/><span data-ttu-id="ac45f-239">![siem 에이전트를 삭제 하려면 줄임표를 선택한 다음 삭제를 선택 합니다.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span><span class="sxs-lookup"><span data-stu-id="ac45f-239">![To delete a SIEM agent, choose the ellipses, and then choose Delete.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span></span>

  
## <a name="next-steps"></a><span data-ttu-id="ac45f-240">다음 단계</span><span class="sxs-lookup"><span data-stu-id="ac45f-240">Next steps</span></span>

- [<span data-ttu-id="ac45f-241">Office 365 Cloud App Security 적용한 후 사용률 활동</span><span class="sxs-lookup"><span data-stu-id="ac45f-241">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="ac45f-242">경고 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="ac45f-242">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="ac45f-243">관리를 간소화 하는 IP 주소 그룹화</span><span class="sxs-lookup"><span data-stu-id="ac45f-243">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

