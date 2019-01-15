---
title: Office 365 Cloud App Security와 SIEM 서버 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Office 365 클라우드 앱 보안이 포함 된 SIEM 서버를 통합할 수 있습니다. 작동 방식 및를 설정 하는 방법에 대 한 개요를 얻으려면이 문서를 읽어보십시오.
ms.openlocfilehash: 0e185dec44bed7657bed126f70dfc64ffc135611
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28015030"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="8c5cf-104">Office 365 Cloud App Security와 SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="8c5cf-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="8c5cf-105">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="8c5cf-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="8c5cf-106">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="8c5cf-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="8c5cf-107">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="8c5cf-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="8c5cf-108">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8c5cf-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="8c5cf-109">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="8c5cf-110">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="8c5cf-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="8c5cf-111">여기는!</span><span class="sxs-lookup"><span data-stu-id="8c5cf-111">You are here!</span></span>  <br/> [<span data-ttu-id="8c5cf-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="8c5cf-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="8c5cf-113">활용 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="8c5cf-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a><span data-ttu-id="8c5cf-114">개요 및 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="8c5cf-114">Overview and prerequisites</span></span>

<span data-ttu-id="8c5cf-p102">[Office 365 클라우드 앱 보안](get-ready-for-office-365-cas.md) 알림 중앙 집중화 된 모니터링을 활성화 하려면 보안 정보 및 이벤트 (SIEM) 관리 서버와 통합할 수 있습니다. 이것은 클라우드 서비스를 사용 하는 조직에 특히 유용 하 고 온-프레미스 서버 응용 프로그램입니다. SIEM 서버와 통합 보안 팀이 더 잘 특정 보안 절차를 자동화 하 고 클라우드 기반 간의 상호 연관 시키는 함으로써 일반적인 보안 워크플로 사용 하 여 유지 관리 하는 동안 Office 365 응용 프로그램을 보호할 수 있도록 온-프레미스 및 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p102">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts. This is especially beneficial for organizations who are using cloud services and on-premises server applications. Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="8c5cf-p103">Office 365 클라우드 응용 프로그램 보안 SIEM 서버에 부합 먼저 때 마지막 2 일에서 알림은 전달 됩니다 모든 알림을 SIEM 서버를 다음에서에서 (선택한 필터 기준). 또한 오랫동안 때 클래스를 활성화 하면 다시이 기능을 해제 하는 경우 지난 2 일의 알림 및 모든 알림을 다음 그 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p103">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select). Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>

### <a name="siem-integration-architecture"></a><span data-ttu-id="8c5cf-120">SIEM 통합 아키텍처</span><span class="sxs-lookup"><span data-stu-id="8c5cf-120">SIEM integration architecture</span></span>

<span data-ttu-id="8c5cf-p104">SIEM 에이전트 조직의 네트워크에 설정 됩니다. SIEM 에이전트 구성 된 데이터 형식 가져오는 배포 하 고 구성 하는 경우 Office 365 클라우드 앱 보안 RESTful Api를 사용 하 여 (경고). 트래픽이 포트 443에서 암호화 된 HTTPS 채널을 통해 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p104">A SIEM agent is set up in your organization's network. When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs. The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="8c5cf-124">Office 365 클라우드 응용 프로그램 보안에서 데이터를 검색 하는 SIEM 에이전트를 하는 경우 (TCP 또는 사용자 지정 포트와 UDP) 설치 하는 동안 제공 되는 네트워크 구성을 사용 하 여 로컬 SIEM 서버 Syslog 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-124">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![SIEM 및 클라우드 응용 프로그램 보안 아키텍처](media/siem-architecture.png)

### <a name="supported-siem-servers"></a><span data-ttu-id="8c5cf-126">지원 되는 SIEM 서버</span><span class="sxs-lookup"><span data-stu-id="8c5cf-126">Supported SIEM servers</span></span>

<span data-ttu-id="8c5cf-127">Office 365 클라우드 앱 보안 현재 다음 SIEM 서버를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-127">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="8c5cf-128">마이크로 포커스 ArcSight</span><span class="sxs-lookup"><span data-stu-id="8c5cf-128">Micro Focus ArcSight</span></span>
- <span data-ttu-id="8c5cf-129">일반 CEF</span><span class="sxs-lookup"><span data-stu-id="8c5cf-129">Generic CEF</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8c5cf-130">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="8c5cf-130">Prerequisites</span></span>

- <span data-ttu-id="8c5cf-p105">이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p105">You must be a global administrator or security administrator to perform the tasks described in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="8c5cf-133">조직에 대 한 [Office 365 클라우드 앱 보안 사용 하도록 설정](turn-on-office-365-cas.md) 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-133">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="8c5cf-134">[감사 로깅](turn-audit-log-search-on-or-off.md) 설정 해야 Office 365에 대 한</span><span class="sxs-lookup"><span data-stu-id="8c5cf-134">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="8c5cf-135">SIEM 서버 통합을 구성 하려면 다음 요구 사항을 충족 하는 표준 서버가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-135">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="8c5cf-136">운영 체제: Windows 또는 Linux (가상 컴퓨터 될 수 있음)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-136">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="8c5cf-137">CPU: 2</span><span class="sxs-lookup"><span data-stu-id="8c5cf-137">CPU: 2</span></span>
    - <span data-ttu-id="8c5cf-138">디스크 공간: 20GB</span><span class="sxs-lookup"><span data-stu-id="8c5cf-138">Disk space: 20 GB</span></span>
    - <span data-ttu-id="8c5cf-139">RAM: 2GB</span><span class="sxs-lookup"><span data-stu-id="8c5cf-139">RAM: 2 GB</span></span>
    - <span data-ttu-id="8c5cf-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) 설치</span><span class="sxs-lookup"><span data-stu-id="8c5cf-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="8c5cf-141">[네트워크 요구 사항](https://docs.microsoft.com/cloud-app-security/network-requirements) 에서 설명한 대로 구성 하는 방화벽</span><span class="sxs-lookup"><span data-stu-id="8c5cf-141">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="8c5cf-p106">**원격 syslog 호스트** 및 **포트 번호 Syslot**하는 방법에 대 한 자세한 내용은 있어야 합니다. 보안 관리자나 네트워크 관리자에 게 해당 정보를 찾을 수 있도록 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p106">You must have details about your **Remote syslog host** and **Syslot port number**. A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="8c5cf-144">[파일을 병](https://go.microsoft.com/fwlink/?linkid=838596) SIEM 서버에 통합 하는데 필요한을 다운로드 하려면 [소프트웨어 사용 조건](https://go.microsoft.com/fwlink/?linkid=862491) 에 동의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-144">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a><span data-ttu-id="8c5cf-145">1 단계: Office 365 클라우드 앱 보안에서 SIEM 에이전트를 설정</span><span class="sxs-lookup"><span data-stu-id="8c5cf-145">Step 1: Set it up a SIEM agent in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="8c5cf-p107">이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. (이렇게 하면 보안 &amp; 준수 센터.)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p107">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="8c5cf-148">**경고** 로 이동 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-148">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="8c5cf-p108">**Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p108">Choose **Go to Office 365 Cloud App Security**. </span></span><br/>
    <span data-ttu-id="8c5cf-150">![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-150">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="8c5cf-151">**설정** 을 클릭 \> **보안 확장**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-151">Click **Settings** \> **Security extensions**.</span></span><br/>
<span data-ttu-id="8c5cf-152">![설정을 선택 > 보안 확장](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-152">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

5. <span data-ttu-id="8c5cf-153">**추가 SIEM 에이전트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-153">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="8c5cf-154">![추가 SIEM 에이전트를 선택 합니다.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-154">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
6. <span data-ttu-id="8c5cf-155">**마법사를 시작**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-155">Choose **Start wizard**.</span></span><br/><span data-ttu-id="8c5cf-156">![마법사를 시작 하거나 대 한 도움말 보기](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-156">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
7. <span data-ttu-id="8c5cf-p109">**일반** 단계에서 이름 및 **SIEM 형식 선택** 지정 하 고 모든 **고급 설정** 해당 형식에 관련 된 설정입니다. **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p109">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format. Then choose **Next**.</span></span><br/><span data-ttu-id="8c5cf-159">![이름 및 유형 지정](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-159">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
8. <span data-ttu-id="8c5cf-p110">**원격 Syslog** 단계에서 IP 주소 또는 호스트 이름을 **원격 syslog 호스트** 및 **Syslog 포트 번호**를 지정 합니다. 원격 Syslog 프로토콜로 TCP 또는 UDP를 선택 합니다. (네트워크 관리자나 보안 관리자가 없는 경우 해당 하는 경우 이러한 세부 정보를 가져오는데 함께 작업할 수 있습니다.) **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p110">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**. Select TCP or UDP as the Remote Syslog protocol. (You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="8c5cf-163">![원격 Syslog 세부 정보를 지정 합니다.](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-163">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
9. <span data-ttu-id="8c5cf-164">**데이터 형식** 단계에서 다음 중 하나를 수행 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-164">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="8c5cf-165">**모든** 알림 기본 설정을 유지합니다</span><span class="sxs-lookup"><span data-stu-id="8c5cf-165">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="8c5cf-166">또는</span><span class="sxs-lookup"><span data-stu-id="8c5cf-166">OR</span></span>
    - <span data-ttu-id="8c5cf-p111">**모든 알림**을 클릭 하 고 **특정 필터**를 선택 합니다. SIEM 서버에 보낼 알림의 종류를 선택 하는 필터를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p111">Click **All alerts**, and then choose **Specific filters**. Define filters to select the kinds of alerts you want to send to your SIEM server. </span></span><br/><span data-ttu-id="8c5cf-169">![마법사의 데이터 형식 단계](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-169">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
10. <span data-ttu-id="8c5cf-170">축 하 합니다. 화면에서 토큰을 복사 하 고 나중에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-170">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![SIEM 만든 에이전트 화면](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="8c5cf-p112">이 시점 Office 365 클라우드 응용 프로그램 보안에서 SIEM 에이전트를 설정한 경우 SIEM 서버 통합이 아직 완료 되지 않음 SIEM 서버 통합을 계속 하려면 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p112">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished. Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="8c5cf-p113">닫기를 클릭 하 고 보안 확장 화면에는 마법사를 유지 한 후에 테이블에 추가 된 SIEM 에이전트를 볼 수 있습니다. 나중에 연결 될 때까지 **Created** 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p113">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table. It will show a status of **Created** until it's connected later.</span></span>

![만든 SIEM 에이전트](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a><span data-ttu-id="8c5cf-177">2 단계: JAR 파일을 다운로드 하 고 SIEM 서버에서 실행</span><span class="sxs-lookup"><span data-stu-id="8c5cf-177">Step 2: Download a JAR file and run it on your SIEM server</span></span>

1. <span data-ttu-id="8c5cf-p114">[Microsoft 클라우드 응용 프로그램 보안 SIEM 에이전트](https://go.microsoft.com/fwlink/?linkid=838596) 를 다운로드 하 고 폴더 압축을 풉니다. (동의 해야 [소프트웨어 사용 조건](https://go.microsoft.com/fwlink/?linkid=862491) 에 진행 하기 위해.)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p114">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder. (You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="8c5cf-180">압축 된 폴더에서.jar 파일 압축을 풀고 SIEM 서버에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-180">Extract the .jar file from the zipped folder and run it on your SIEM server.</span></span>
    
3. <span data-ttu-id="8c5cf-181">파일을 실행 한 후 다음을 실행: 명령 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-181">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a><span data-ttu-id="8c5cf-182">중요 한 참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c5cf-182">Important notes</span></span>

- <span data-ttu-id="8c5cf-183">파일 이름 SIEM 에이전트의 버전에 따라 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-183">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="8c5cf-184">서버 설치 하는 동안 SIEM 서버에서 JAR 파일을 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-184">We recommend that you run the JAR file on your SIEM server during server setup.</span></span>

    - <span data-ttu-id="8c5cf-185">**Windows**: 실행 된 예약 된 작업을 하 고 작업을 **실행 하는 사용자의 로그온 여부** 를 구성 하 고 **기간 이상 실행 하는 경우 작업을 중지** 옵션의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-185">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="8c5cf-186">**Linux**: 함께 실행된 명령을 추가 **&** 에 `rc.local` 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-186">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="8c5cf-187">예제:</span><span class="sxs-lookup"><span data-stu-id="8c5cf-187">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="8c5cf-p115">대괄호는 선택적 매개 변수와 관련 된 경우에 사용 해야 합니다. 다음 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p115">Parameters in brackets [] are optional, and should be used only if relevant. Use the following variables:</span></span>

    - <span data-ttu-id="8c5cf-190">**DIRNAME** 는 경로에 로컬 에이전트 디버그 로그를 사용 하려는 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-190">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>

    - <span data-ttu-id="8c5cf-191">**주소 [: 포트]** 프록시 서버 주소와 인터넷에 연결 하는 서버를 사용 하는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-191">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>

    - <span data-ttu-id="8c5cf-192">**토큰** 은 첫번째 절차에서 복사한 SIEM 에이전트 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-192">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>

    - <span data-ttu-id="8c5cf-193">도움말을 보려면 다음을 입력 `-h`합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-193">To get help, type `-h`.</span></span> 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="8c5cf-194">3 단계: SIEM 에이전트 작동 하는지 확인</span><span class="sxs-lookup"><span data-stu-id="8c5cf-194">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="8c5cf-195">Office 365 클라우드 응용 프로그램 보안 포털에서 SIEM 에이전트의 상태 **연결** 오류로 표시 되지 않거나는 없는 에이전트 알림 **Disconnected** 하 고 있는 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-195">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="8c5cf-196">예, 여기는 볼 수 SIEM 서버가 연결 된:</span><span class="sxs-lookup"><span data-stu-id="8c5cf-196">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="8c5cf-197">![연결 된 SIEM 서버](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-197">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="8c5cf-198">및는 여기에 SIEM 서버 연결이 끊어지면 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-198">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="8c5cf-199">![연결 되지 않은 SIEM 서버](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-199">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="8c5cf-200">프로그램 Syslog/SIEM 서버에서 Office 365 클라우드 응용 프로그램 보안에서 알림 도착 하는 것이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-200">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="what-the-logfiles-look-like"></a><span data-ttu-id="8c5cf-201">로그 파일의 모양을</span><span class="sxs-lookup"><span data-stu-id="8c5cf-201">What the logfiles look like</span></span>

<span data-ttu-id="8c5cf-202">SIEM 서버로 전송 될 수 있는 알림 로그 파일 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-202">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="8c5cf-203">그리고 다른 샘플 CEF 형식에서이 시간 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-203">And here's another sample, this time in CEF format:</span></span>


|<span data-ttu-id="8c5cf-204">CEF 필드 이름</span><span class="sxs-lookup"><span data-stu-id="8c5cf-204">CEF field name</span></span>  | <span data-ttu-id="8c5cf-205">설명</span><span class="sxs-lookup"><span data-stu-id="8c5cf-205">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="8c5cf-206">시작</span><span class="sxs-lookup"><span data-stu-id="8c5cf-206">start</span></span>     | <span data-ttu-id="8c5cf-207">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="8c5cf-207">alert timestamp</span></span>        |
|<span data-ttu-id="8c5cf-208">끝</span><span class="sxs-lookup"><span data-stu-id="8c5cf-208">end</span></span>     | <span data-ttu-id="8c5cf-209">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="8c5cf-209">alert timestamp</span></span>        |
|<span data-ttu-id="8c5cf-210">rt</span><span class="sxs-lookup"><span data-stu-id="8c5cf-210">rt</span></span>     | <span data-ttu-id="8c5cf-211">경고 타임 스탬프</span><span class="sxs-lookup"><span data-stu-id="8c5cf-211">alert timestamp</span></span>        |
|<span data-ttu-id="8c5cf-212">msg</span><span class="sxs-lookup"><span data-stu-id="8c5cf-212">msg</span></span>     | <span data-ttu-id="8c5cf-213">Office 365 클라우드 응용 프로그램 보안 포털에 표시 된 대로 설명 경으십시오</span><span class="sxs-lookup"><span data-stu-id="8c5cf-213">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="8c5cf-214">suser</span><span class="sxs-lookup"><span data-stu-id="8c5cf-214">suser</span></span>     | <span data-ttu-id="8c5cf-215">알림 제목 사용자</span><span class="sxs-lookup"><span data-stu-id="8c5cf-215">alert subject user</span></span>        |
|<span data-ttu-id="8c5cf-216">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="8c5cf-216">destinationServiceName</span></span>     | <span data-ttu-id="8c5cf-217">Office 365, SharePoint, 또는 OneDrive와 같은 응용 프로그램에서 들어오는 경고</span><span class="sxs-lookup"><span data-stu-id="8c5cf-217">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="8c5cf-218">csLabel</span><span class="sxs-lookup"><span data-stu-id="8c5cf-218">csLabel</span></span>     | <span data-ttu-id="8c5cf-p116">다름 (레이블에 다음과 같은 의미). 일반적으로 레이블이 targetObjects 같은 쉽게 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p116">Varies (labels have different meanings). Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="8c5cf-221">cs</span><span class="sxs-lookup"><span data-stu-id="8c5cf-221">cs</span></span>     | <span data-ttu-id="8c5cf-222">정보에 해당 하는 레이블 (예: 레이블 예제에 따라 알림의 대상 사용자)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-222">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |

## <a name="additional-tasks-as-needed"></a><span data-ttu-id="8c5cf-223">(필요한)로 추가 작업</span><span class="sxs-lookup"><span data-stu-id="8c5cf-223">Additional tasks (as needed)</span></span>

<span data-ttu-id="8c5cf-p117">SIEM 서버를 구성 하 고 Office 365 클라우드 응용 프로그램 보안와 통합 하였습니다, 후 토큰을 다시 생성, SIEM 에이전트를 편집 하거나 SIEM 에이전트를 삭제 하는 필요할수도 있습니다. 다음 섹션에서는 이러한 작업을 수행 하는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p117">After you have configured your SIEM server and have integrated it with Office 365 Cloud App Security, you might need to regenerate a token, edit a SIEM agent, or delete a SIEM agent. The following sections describe how to perform these tasks.</span></span>

### <a name="regenerate-a-token"></a><span data-ttu-id="8c5cf-226">토큰을 다시 생성</span><span class="sxs-lookup"><span data-stu-id="8c5cf-226">Regenerate a token</span></span>

<span data-ttu-id="8c5cf-227">사용자 토큰을 손실 된 경우에 하나 다시 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-227">If you lose your token, you can regenerate one.</span></span> 

1. <span data-ttu-id="8c5cf-228">Office 365 클라우드 응용 프로그램 보안 포털에서 **설정**을 선택 > **보안 확장**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-228">In the Office 365 Cloud App Security portal, choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="8c5cf-229">테이블에서 SIEM 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-229">In the table, locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="8c5cf-230">있는 줄임표를 클릭 하 고 **토큰을 다시 생성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-230">Click the ellipses, and then choose **Regenerate token**.</span></span><br/><span data-ttu-id="8c5cf-231">![SIEM 에이전트에 대 한 줄임표를 클릭 하 여 토큰을 다시 생성](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-231">![Regenerate a token by clicking the ellipsis for your SIEM agent](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span></span>
  
### <a name="edit-a-siem-agent"></a><span data-ttu-id="8c5cf-232">SIEM 에이전트를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-232">Edit a SIEM agent</span></span>

1. <span data-ttu-id="8c5cf-233">Office 365 클라우드 응용 프로그램 보안 포털에서 **설정**을 선택 > **보안 확장**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-233">In the Office 365 Cloud App Security portal, choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="8c5cf-234">SIEM 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-234">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="8c5cf-p118">있는 줄임표를 클릭 하 고 **편집**을 선택 합니다. (SIEM 에이전트를 편집 하는 경우에.jar 파일을 실행 하는 다시 필요가 없습니다; 자동으로 업데이트 하는 것입니다.)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-p118">Click the ellipses, and then choose **Edit**. (If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.) </span></span><br/><span data-ttu-id="8c5cf-237">![SIEM 에이전트를 편집 하려면 타원을 선택한 다음 편집을 선택 합니다.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-237">![To edit your SIEM agent, choose the ellipses, and then choose Edit.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span></span>
  
### <a name="delete-a-siem-agent"></a><span data-ttu-id="8c5cf-238">SIEM 에이전트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-238">Delete a SIEM agent</span></span>

1. <span data-ttu-id="8c5cf-239">Office 365 클라우드 응용 프로그램 보안 포털에서 **설정**을 선택 > **보안 확장**합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-239">In the Office 365 Cloud App Security portal, choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="8c5cf-240">SIEM 에이전트에 대 한 행을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-240">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="8c5cf-241">있는 줄임표를 클릭 한 다음 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-241">Click the ellipses, and then choose **Delete**.</span></span><br/><span data-ttu-id="8c5cf-242">![SIEM 에이전트를 삭제 하려면 타원을 선택한 다음 삭제를 선택 합니다.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-242">![To delete a SIEM agent, choose the ellipses, and then choose Delete.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span></span>

  
## <a name="next-steps"></a><span data-ttu-id="8c5cf-243">다음 단계</span><span class="sxs-lookup"><span data-stu-id="8c5cf-243">Next steps</span></span>

- [<span data-ttu-id="8c5cf-244">Office 365 Cloud App Security 적용한 후 사용률 활동</span><span class="sxs-lookup"><span data-stu-id="8c5cf-244">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="8c5cf-245">검토 및 알림 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-245">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="8c5cf-246">관리를 단순화 하 여 IP 주소를 그룹화</span><span class="sxs-lookup"><span data-stu-id="8c5cf-246">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

