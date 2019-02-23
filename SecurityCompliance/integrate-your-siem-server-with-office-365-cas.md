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
ms.openlocfilehash: b4baeda3cb836c0b1aa528d29176bbf4321d1fe2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215878"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="23745-104">Office 365 Cloud App Security와 SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="23745-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="23745-105">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="23745-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="23745-106">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="23745-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="23745-107">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="23745-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="23745-108">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="23745-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="23745-109">평가 시작</span><span class="sxs-lookup"><span data-stu-id="23745-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="23745-110">계획 시작</span><span class="sxs-lookup"><span data-stu-id="23745-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="23745-111">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="23745-111">You are here!</span></span>  <br/> [<span data-ttu-id="23745-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="23745-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="23745-113">활용 시작</span><span class="sxs-lookup"><span data-stu-id="23745-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a><span data-ttu-id="23745-114">개요 및 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="23745-114">Overview and prerequisites</span></span>

<span data-ttu-id="23745-p102">[Office 365 Cloud App security](get-ready-for-office-365-cas.md) 을 siem (보안 정보 및 이벤트 관리) 서버와 통합 하 여 중앙 집중식 경고 모니터링을 사용 하도록 설정할 수 있습니다. 이는 클라우드 서비스 및 온-프레미스 서버 응용 프로그램을 사용 하는 조직에 특히 유용 합니다. siem server와의 통합을 통해 보안 팀은 일반적인 보안 절차를 자동화 하 고 클라우드 기반 및 온-프레미스 이벤트 간의 상관 관계를 자동으로 유지 하 여 Office 365 응용 프로그램을 보다 효율적으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p102">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts. This is especially beneficial for organizations who are using cloud services and on-premises server applications. Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="23745-p103">siem server를 Office 365 Cloud App Security와 처음 통합 하면 지난 2 일의 알림이 siem 서버에 전달 되 고, 선택한 모든 필터를 기반으로 하는 모든 경고가 전송 됩니다. 또한 연장 된 기간에 대해이 기능을 사용 하지 않도록 설정 하면 다시 사용 하도록 설정할 때 이전의 두 날의 알림을 전달 하 고 이후의 모든 경고를 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p103">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select). Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>

### <a name="siem-integration-architecture"></a><span data-ttu-id="23745-120">siem 통합 아키텍처</span><span class="sxs-lookup"><span data-stu-id="23745-120">SIEM integration architecture</span></span>

<span data-ttu-id="23745-p104">siem 에이전트는 조직의 네트워크에 설정 됩니다. siem 에이전트는 배포 및 구성 된 경우 Office 365 Cloud App Security RESTful api를 사용 하 여 구성 된 (경고) 데이터 형식을 가져옵니다. 그런 다음 포트 443에서 암호화 된 HTTPS 채널을 통해 트래픽을 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p104">A SIEM agent is set up in your organization's network. When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs. The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="23745-124">siem 에이전트가 Office 365 Cloud App Security에서 데이터를 검색 하는 경우 설치 중에 제공 되는 네트워크 구성 (TCP 또는 사용자 지정 포트를 사용 하 여 UDP)을 사용 하 여 로컬 siem 서버에 Syslog 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="23745-124">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![siem 및 Cloud App Security 아키텍처](media/siem-architecture.png)

### <a name="supported-siem-servers"></a><span data-ttu-id="23745-126">지원 되는 siem 서버</span><span class="sxs-lookup"><span data-stu-id="23745-126">Supported SIEM servers</span></span>

<span data-ttu-id="23745-127">Office 365 Cloud App Security에서는 현재 다음과 같은 siem 서버를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-127">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="23745-128">마이크로 포커스 arcsight</span><span class="sxs-lookup"><span data-stu-id="23745-128">Micro Focus ArcSight</span></span>
- <span data-ttu-id="23745-129">일반 cef</span><span class="sxs-lookup"><span data-stu-id="23745-129">Generic CEF</span></span>

### <a name="prerequisites"></a><span data-ttu-id="23745-130">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="23745-130">Prerequisites</span></span>

- <span data-ttu-id="23745-p105">이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md) 보기</span><span class="sxs-lookup"><span data-stu-id="23745-p105">You must be a global administrator or security administrator to perform the tasks described in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="23745-133">조직에 대해 [Office 365 Cloud App Security가 사용 하도록 설정](turn-on-office-365-cas.md) 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-133">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="23745-134">Office 365에 대해 [감사 로깅을](turn-audit-log-search-on-or-off.md) 켜야 함</span><span class="sxs-lookup"><span data-stu-id="23745-134">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="23745-135">siem 서버 통합을 구성 하기 위해 다음 요구 사항을 충족 하는 표준 서버가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-135">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="23745-136">OS: Windows 또는 Linux (가상 컴퓨터 일 수 있음)</span><span class="sxs-lookup"><span data-stu-id="23745-136">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="23745-137">CPU: 2</span><span class="sxs-lookup"><span data-stu-id="23745-137">CPU: 2</span></span>
    - <span data-ttu-id="23745-138">디스크 공간: 20gb</span><span class="sxs-lookup"><span data-stu-id="23745-138">Disk space: 20 GB</span></span>
    - <span data-ttu-id="23745-139">RAM: 2gb</span><span class="sxs-lookup"><span data-stu-id="23745-139">RAM: 2 GB</span></span>
    - <span data-ttu-id="23745-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) 설치</span><span class="sxs-lookup"><span data-stu-id="23745-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="23745-141">[네트워크 요구 사항](https://docs.microsoft.com/cloud-app-security/network-requirements) 에 설명 된 대로 방화벽이 구성 됨</span><span class="sxs-lookup"><span data-stu-id="23745-141">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="23745-p106">**원격 syslog 호스트** 및 **syslot 포트 번호**에 대 한 세부 정보가 있어야 합니다. 네트워크 관리자 또는 보안 관리자는 해당 정보를 찾는 데 도움을 드릴 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p106">You must have details about your **Remote syslog host** and **Syslot port number**. A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="23745-144">siem 서버를 통합 하는 데 필요한 [JAR 파일](https://go.microsoft.com/fwlink/?linkid=838596) 을 다운로드 하려면 [소프트웨어 사용 조건](https://go.microsoft.com/fwlink/?linkid=862491) 에 동의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-144">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a><span data-ttu-id="23745-145">1 단계: Office 365 Cloud App Security에서 siem 에이전트로 설정</span><span class="sxs-lookup"><span data-stu-id="23745-145">Step 1: Set it up a SIEM agent in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="23745-146">Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-146">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="23745-147">**설정** \> **보안 확장**을 클릭 한 다음 siem 에이전트를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-147">Click **Settings** \> **Security extensions**, and then choose SIEM agents.</span></span><br/>
<span data-ttu-id="23745-148">![설정 > 보안 확장을 선택 합니다.](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="23745-148">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

3. <span data-ttu-id="23745-149">**siem 에이전트 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-149">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="23745-150">![siem 에이전트 추가를 선택 합니다.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="23745-150">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
4. <span data-ttu-id="23745-151">**마법사 시작**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-151">Choose **Start wizard**.</span></span><br/><span data-ttu-id="23745-152">![도움말 보기 또는 마법사 시작](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="23745-152">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
5. <span data-ttu-id="23745-p107">**일반** 단계에서 이름을 지정 하 고 **siem 형식을 선택한** 다음 해당 형식과 관련 된 **고급 설정을** 설정 합니다. 다음을 \*\*\*\* 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p107">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format. Then choose **Next**.</span></span><br/><span data-ttu-id="23745-155">![이름 및 유형 지정](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="23745-155">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
6. <span data-ttu-id="23745-p108">**원격 syslog** 단계에서 **원격 syslog 호스트** 의 IP 주소 또는 호스트 이름 및 **Syslog 포트 번호**를 지정 합니다. 원격 Syslog 프로토콜로 TCP 또는 UDP를 선택 합니다. (사용자가 없는 경우 네트워크 관리자 또는 보안 관리자와 함께 작업 하 여 이러한 세부 정보를 얻을 수 있습니다.) 다음을 \*\*\*\* 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p108">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**. Select TCP or UDP as the Remote Syslog protocol. (You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="23745-159">![원격 Syslog 세부 정보 지정](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="23745-159">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
7. <span data-ttu-id="23745-160">**데이터 형식** 단계에서 다음 중 하나를 수행한 후 **Next (다음**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-160">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="23745-161">**모든 알림의** 기본 설정 유지</span><span class="sxs-lookup"><span data-stu-id="23745-161">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="23745-162">또는</span><span class="sxs-lookup"><span data-stu-id="23745-162">OR</span></span>
    - <span data-ttu-id="23745-p109">**모든 경고**를 클릭 한 다음 **특정 필터**를 선택 합니다. siem 서버에 보낼 알림 종류를 선택 하는 필터를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p109">Click **All alerts**, and then choose **Specific filters**. Define filters to select the kinds of alerts you want to send to your SIEM server. </span></span><br/><span data-ttu-id="23745-165">![마법사의 데이터 형식 단계](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="23745-165">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
8. <span data-ttu-id="23745-166">축 하 합니다 화면에서 토큰을 복사 하 고 나중에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-166">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![siem 에이전트 만들어짐 화면](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="23745-p110">이제 Office 365 Cloud App Security에서 siem 에이전트를 설정 했지만 siem server 통합은 아직 완료 되지 않았습니다. 다음 단계로 이동 하 여 siem server 통합을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p110">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished. Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="23745-p111">닫기를 클릭 하 고 마법사를 종료 한 후에는 보안 확장 화면에서 테이블에 추가한 siem 에이전트를 볼 수 있습니다. 나중에 연결 될 때까지 **만들어진** 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p111">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table. It will show a status of **Created** until it's connected later.</span></span>

![siem 에이전트를 만들었습니다.](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a><span data-ttu-id="23745-173">2 단계: siem 서버에서 JAR 파일 다운로드 및 실행</span><span class="sxs-lookup"><span data-stu-id="23745-173">Step 2: Download a JAR file and run it on your SIEM server</span></span>

1. <span data-ttu-id="23745-p112">[Microsoft Cloud App Security siem 에이전트](https://go.microsoft.com/fwlink/?linkid=838596) 를 다운로드 하 고 폴더의 압축을 풉니다. (계속 하려면 [소프트웨어 사용권 조항](https://go.microsoft.com/fwlink/?linkid=862491) 에 동의 해야 합니다.)</span><span class="sxs-lookup"><span data-stu-id="23745-p112">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder. (You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="23745-176">압축 폴더에서 .jar 파일을 추출 하 여 siem 서버에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-176">Extract the .jar file from the zipped folder and run it on your SIEM server.</span></span>
    
3. <span data-ttu-id="23745-177">파일을 실행 한 후 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-177">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a><span data-ttu-id="23745-178">중요 참고 사항</span><span class="sxs-lookup"><span data-stu-id="23745-178">Important notes</span></span>

- <span data-ttu-id="23745-179">파일 이름은 siem 에이전트 버전에 따라 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-179">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="23745-180">서버 설치 중에 siem 서버에서 JAR 파일을 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-180">We recommend that you run the JAR file on your SIEM server during server setup.</span></span>

    - <span data-ttu-id="23745-181">**Windows**: 예약 된 작업으로 실행 하 고, **사용자의 로그온 여부에 관계 없이 실행** 되도록 작업을 구성 하 고, 작업이 다음 **보다 오래 실행 되 면 중지** 옵션의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-181">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="23745-182">**Linux**: **&** `rc.local` 파일에 with를 사용 하 여 run 명령을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-182">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="23745-183">예제:</span><span class="sxs-lookup"><span data-stu-id="23745-183">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="23745-p113">대괄호의 매개 변수는 선택 사항이 며 관련성이 있는 경우에만 사용 해야 합니다. 다음 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p113">Parameters in brackets [] are optional, and should be used only if relevant. Use the following variables:</span></span>

    - <span data-ttu-id="23745-186">**tname** 은 로컬 에이전트 디버그 로그에 사용 하려는 디렉터리의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="23745-186">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>

    - <span data-ttu-id="23745-187">**ADDRESS [:P ort]** 는 서버에서 인터넷에 연결 하는 데 사용 하는 프록시 서버 주소 및 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="23745-187">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>

    - <span data-ttu-id="23745-188">**TOKEN** 은 첫 번째 절차에서 복사한 siem 에이전트 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="23745-188">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>

    - <span data-ttu-id="23745-189">도움말을 보려면를 입력 `-h`합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-189">To get help, type `-h`.</span></span> 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="23745-190">3 단계: siem 에이전트가 작동 하는지 확인</span><span class="sxs-lookup"><span data-stu-id="23745-190">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="23745-191">Office 365 Cloud App Security 포털의 siem 에이전트 상태가 **연결 오류** 또는 **연결이 끊어져** 표시 되지 않으며 에이전트 알림이 없음을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-191">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="23745-192">예를 들어 다음과 같이 siem server가 연결 된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-192">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="23745-193">![siem 서버 연결 됨](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="23745-193">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="23745-194">여기서는 siem server의 연결이 끊어져 있는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-194">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="23745-195">![siem 서버가 연결 되지 않음](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="23745-195">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="23745-196">Syslog/siem server에서는 Office 365 Cloud App Security에서 알림이 수신 되었음을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-196">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="what-the-logfiles-look-like"></a><span data-ttu-id="23745-197">로그 파일이 어떤 모습 인지 확인</span><span class="sxs-lookup"><span data-stu-id="23745-197">What the logfiles look like</span></span>

<span data-ttu-id="23745-198">다음은 siem 서버로 전송 될 수 있는 경고 로그 파일 예입니다.</span><span class="sxs-lookup"><span data-stu-id="23745-198">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="23745-199">다음은 cef 형식에서이에 해당 하는 다른 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="23745-199">And here's another sample, this time in CEF format:</span></span>


|<span data-ttu-id="23745-200">cef 필드 이름</span><span class="sxs-lookup"><span data-stu-id="23745-200">CEF field name</span></span>  | <span data-ttu-id="23745-201">Description</span><span class="sxs-lookup"><span data-stu-id="23745-201">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="23745-202">우선</span><span class="sxs-lookup"><span data-stu-id="23745-202">start</span></span>     | <span data-ttu-id="23745-203">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="23745-203">alert timestamp</span></span>        |
|<span data-ttu-id="23745-204">끝나야</span><span class="sxs-lookup"><span data-stu-id="23745-204">end</span></span>     | <span data-ttu-id="23745-205">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="23745-205">alert timestamp</span></span>        |
|<span data-ttu-id="23745-206">rt</span><span class="sxs-lookup"><span data-stu-id="23745-206">rt</span></span>     | <span data-ttu-id="23745-207">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="23745-207">alert timestamp</span></span>        |
|<span data-ttu-id="23745-208">msg</span><span class="sxs-lookup"><span data-stu-id="23745-208">msg</span></span>     | <span data-ttu-id="23745-209">Office 365 Cloud App Security 포털에 표시 되는 경고 설명</span><span class="sxs-lookup"><span data-stu-id="23745-209">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="23745-210">suser</span><span class="sxs-lookup"><span data-stu-id="23745-210">suser</span></span>     | <span data-ttu-id="23745-211">알림 주체 사용자</span><span class="sxs-lookup"><span data-stu-id="23745-211">alert subject user</span></span>        |
|<span data-ttu-id="23745-212">destinationservicename</span><span class="sxs-lookup"><span data-stu-id="23745-212">destinationServiceName</span></span>     | <span data-ttu-id="23745-213">Office 365, SharePoint 또는 OneDrive와 같은 시작 응용 프로그램 알림</span><span class="sxs-lookup"><span data-stu-id="23745-213">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="23745-214">cslabel</span><span class="sxs-lookup"><span data-stu-id="23745-214">csLabel</span></span>     | <span data-ttu-id="23745-p114">다양 한 의미를 갖는 레이블로 변경 합니다. 일반적으로 레이블은 targetobjects와 같은 설명이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p114">Varies (labels have different meanings). Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="23745-217">cs</span><span class="sxs-lookup"><span data-stu-id="23745-217">cs</span></span>     | <span data-ttu-id="23745-218">레이블에 해당 하는 정보 (예: 레이블 예제에 대 한 경고의 대상 사용자)</span><span class="sxs-lookup"><span data-stu-id="23745-218">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |

## <a name="additional-tasks-as-needed"></a><span data-ttu-id="23745-219">추가 작업 (필요한 경우)</span><span class="sxs-lookup"><span data-stu-id="23745-219">Additional tasks (as needed)</span></span>

<span data-ttu-id="23745-p115">siem 서버를 구성 하 고 Office 365 Cloud App Security과 통합 한 후에는 토큰을 다시 생성 하거나, siem 에이전트를 편집 하거나, siem 에이전트를 삭제 해야 할 수 있습니다. 다음 섹션에서는 이러한 작업을 수행 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p115">After you have configured your SIEM server and have integrated it with Office 365 Cloud App Security, you might need to regenerate a token, edit a SIEM agent, or delete a SIEM agent. The following sections describe how to perform these tasks.</span></span>

### <a name="regenerate-a-token"></a><span data-ttu-id="23745-222">토큰 다시 생성</span><span class="sxs-lookup"><span data-stu-id="23745-222">Regenerate a token</span></span>

<span data-ttu-id="23745-223">토큰을 분실 한 경우 다시 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-223">If you lose your token, you can regenerate one.</span></span> 

1. <span data-ttu-id="23745-224">Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-224">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="23745-225">표에서 siem 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-225">In the table, locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="23745-226">줄임표를 클릭 한 다음 **토큰 다시 생성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-226">Click the ellipses, and then choose **Regenerate token**.</span></span><br/><span data-ttu-id="23745-227">![siem 에이전트에 대 한 줄임표를 클릭 하 여 토큰 다시 생성](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span><span class="sxs-lookup"><span data-stu-id="23745-227">![Regenerate a token by clicking the ellipsis for your SIEM agent](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span></span>
  
### <a name="edit-a-siem-agent"></a><span data-ttu-id="23745-228">siem 에이전트 편집</span><span class="sxs-lookup"><span data-stu-id="23745-228">Edit a SIEM agent</span></span>

1. <span data-ttu-id="23745-229">Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-229">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="23745-230">siem 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-230">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="23745-p116">줄임표를 클릭 한 다음 **편집**을 선택 합니다. siem 에이전트를 편집 하는 경우에는 .jar 파일을 다시 실행할 필요가 없으며 자동으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23745-p116">Click the ellipses, and then choose **Edit**. (If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.) </span></span><br/><span data-ttu-id="23745-233">![siem 에이전트를 편집 하려면 줄임표를 선택 하 고 편집을 선택 합니다.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span><span class="sxs-lookup"><span data-stu-id="23745-233">![To edit your SIEM agent, choose the ellipses, and then choose Edit.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span></span>
  
### <a name="delete-a-siem-agent"></a><span data-ttu-id="23745-234">siem 에이전트 삭제</span><span class="sxs-lookup"><span data-stu-id="23745-234">Delete a SIEM agent</span></span>

1. <span data-ttu-id="23745-235">Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-235">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="23745-236">siem 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="23745-236">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="23745-237">줄임표를 클릭 한 다음 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23745-237">Click the ellipses, and then choose **Delete**.</span></span><br/><span data-ttu-id="23745-238">![siem 에이전트를 삭제 하려면 줄임표를 선택한 다음 삭제를 선택 합니다.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span><span class="sxs-lookup"><span data-stu-id="23745-238">![To delete a SIEM agent, choose the ellipses, and then choose Delete.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span></span>

  
## <a name="next-steps"></a><span data-ttu-id="23745-239">다음 단계</span><span class="sxs-lookup"><span data-stu-id="23745-239">Next steps</span></span>

- [<span data-ttu-id="23745-240">Office 365 Cloud App Security 적용한 후 사용률 활동</span><span class="sxs-lookup"><span data-stu-id="23745-240">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="23745-241">경고 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="23745-241">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="23745-242">관리를 간소화 하는 IP 주소 그룹화</span><span class="sxs-lookup"><span data-stu-id="23745-242">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

