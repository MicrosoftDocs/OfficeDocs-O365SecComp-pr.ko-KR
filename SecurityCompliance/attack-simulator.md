---
title: Office 365의 공격 시뮬레이터
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/02/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Office 365 전역 관리자는 조직에서 사실적인 공격 시나리오를 실행 하려면 공격 시뮬레이터를 사용할 수 있습니다. 이 도울수 식별 하 고 실제 공격 비즈니스를 방문한 전에 공격에 취약 한 사용자를 찾을 수 있습니다.
ms.openlocfilehash: 1a1d22b0b36ce8b6a2086296be8f8b5d47d79280
ms.sourcegitcommit: d512c1df01377e305e8d5c0170c822cf78f09565
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/02/2019
ms.locfileid: "27472001"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="331d0-104">Office 365의 공격 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="331d0-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="331d0-p102">**요약** Office 365 전역 관리자 여야 하는 경우 조직에 [Office 365 위협 인텔리전스](office-365-ti.md)공격 시뮬레이터를 사용 하 여 사실적인 공격 시나리오를 실행 하 여 조직에서 수 있습니다. 이 도울수 식별 하 고 실제 공격 아래 줄에 영향을 줍니다 전에 공격에 취약 한 사용자를 찾을 수 있습니다. 자세한 내용은이 문서를 읽어보십시오.</span><span class="sxs-lookup"><span data-stu-id="331d0-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="331d0-108">공격</span><span class="sxs-lookup"><span data-stu-id="331d0-108">The Attacks</span></span>

<span data-ttu-id="331d0-109">세 종류의 공격 시뮬레이션 현재 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-109">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="331d0-110">표시 이름 창 피싱 공격</span><span class="sxs-lookup"><span data-stu-id="331d0-110">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="331d0-111">암호 스프레이 공격</span><span class="sxs-lookup"><span data-stu-id="331d0-111">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="331d0-112">대입 암호 공격</span><span class="sxs-lookup"><span data-stu-id="331d0-112">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="331d0-p103">성공적으로 실행 될 공격에 대 한 시뮬레이션 된 공격을 실행 하는 사용 하는 계정에 다단계 인증을 사용 합니다. 또한 Office 365 전역 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p103">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="331d0-115">조건부 액세스에 대 한 지원 출시 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-115">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="331d0-116">보안에서 공격 시뮬레이터에 액세스 하려면 &amp; 준수 센터 **위협 관리** 를 선택 \> **공격 시뮬레이터**합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-116">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="331d0-117">시작 하기 전에...</span><span class="sxs-lookup"><span data-stu-id="331d0-117">Before you begin...</span></span>

<span data-ttu-id="331d0-118">및 조직 공격 시뮬레이터에 대 한 다음과 같은 요구 사항을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-118">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="331d0-p104">조직의 전자 메일은 Exchange Online에서 호스팅됩니다. (공격 시뮬레이터 온-프레미스 전자 메일 서버에 대해 사용할 수 없는 경우)</span><span class="sxs-lookup"><span data-stu-id="331d0-p104">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="331d0-121">사용자가 Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="331d0-121">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="331d0-122">조직에서 사용 중인 [Office 365 사용자에 대해 다단계 인증](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="331d0-122">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="331d0-123">조직에 [Office 365 위협 인텔리전스](office-365-ti.md)공격 시뮬레이터 보안에 표시 된 &amp; 준수 센터 ( **위협 관리** 로 이동 \> **공격 시뮬레이터**)</span><span class="sxs-lookup"><span data-stu-id="331d0-123">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="331d0-124">![관리-공격 시뮬레이터 위협](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="331d0-124">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="331d0-125">표시 이름 창 피싱 공격</span><span class="sxs-lookup"><span data-stu-id="331d0-125">Display name spear-phishing attack</span></span>

<span data-ttu-id="331d0-p105">피싱은 사회 공학 스타일 공격으로 분류 하는 공격의 광범위 한 제품군에 대 한 일반 용어입니다. 이 공격에서는 창 피싱, 개인 또는 조직의 특정 그룹을 목표로 하는 더욱 효과적인된 공격에 초점을 맞춥니다. 일반적으로 사용자 지정 된 공격에 일부 검사를 수행 하 고 임원 조직 내에서 보낸 것 처럼 보이는 전자 메일 메시지와 같은 받는 사람에 대 한 신뢰를 생성 하는 표시 이름을 사용 하 여 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p105">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="331d0-p106">이 공격 알려주는 메시지의 표시 이름 및 인증 원본 주소를 변경 하 여에서 시작 된 것으로 표시 되는 조작 (영문)에 중점을 둡니다. 창 피싱 공격은 성공, 사용자의 자격 증명에 액세스할 사이버 범죄자 들에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p106">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="331d0-131">창 피싱 공격을 시뮬레이션 하기 위해</span><span class="sxs-lookup"><span data-stu-id="331d0-131">To simulate a spear-phishing attack</span></span>

![전자 메일 본문 작성](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="331d0-133">**전자 메일 본문** 필드 자체에서 직접 서식 있는 HTML 편집기를 만들 수도 있고 HTML 원본으로 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-133">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="331d0-134">[보안 &amp; 준수 센터](https://security.microsoft.com), **위협 관리** 를 선택 \> **공격 시뮬레이터**합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-134">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="331d0-135">공격에 대 한 의미 있는 캠페인 이름을 지정 하거나 서식 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-135">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![피싱 시작 페이지](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="331d0-p107">대상 받는 사람을 지정 합니다. 이 개인 또는 조직에서 그룹 수 있습니다. 각 대상으로 지정 된 받는 사람을 성공적으로 수행 하는 공격에 대 한 순서 대로 Exchange Online 사서함 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p107">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![받는 사람 선택](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="331d0-141">피싱 메일 세부 정보를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-141">Configure the Phishing email details.</span></span> <br/>![전자 메일 세부 정보를 구성 합니다.](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="331d0-p108">HTML 서식을 수도 있고 같이 복잡 한 기본 캠페인이 알아야 합니다. 전자 메일 서식 있는 HTML을 그대로 이미지와 believability를 향상 시키기 위해 텍스트를 삽입할 수 있습니다. 받는 전자 메일 클라이언트에서 받은 메시지 모양을에서 제어할을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p108">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="331d0-p109">**(이름)에서** 필드에 대 한 텍스트를 지정 합니다. 받는 전자 메일 클라이언트에 **표시 이름** 을 표시 하는 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p109">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="331d0-p110">텍스트 또는 **에서** 필드를 지정 합니다. 받는 전자 메일 클라이언트에서 보낸 사람의 전자 메일 주소으로 표시 하는 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p110">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="331d0-p111">조직 내에서 기존 전자 메일 네임 스페이스를 입력할 수 있습니다 (이 수행 하는 확인 실제로 매우 높음 보안 모델을 용이 하 게 받는 클라이언트에서 해결 하는 전자 메일 주소)을 하거나 외부 전자 메일 주소를 입력할 수 있습니다. 하지만 실제로 존재 하지 않아도 지정 하는 전자 메일 주소 user@domainname.extension와 같은 유효한 SMTP 주소를의 형식에 따라 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p111">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="331d0-p112">드롭다운 선택기를 사용 하 여 공격 받을 수 있는 내 해야 콘텐츠 형식의 반영 하는 피싱 로그인 서버 URL을 선택 합니다. 여러 테마가 적용 된 Url 문서 배달, 기술, 급여 등 등,를 선택할 수 제공 됩니다. 이것이 효과적으로 URL을 대상으로 지정 된 사용자를 클릭 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p112">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="331d0-p113">사용자 지정 시작 페이지 URL을 지정 합니다. 이 사용 하 여 공격에 성공의 끝에 지정 된 URL로 사용자 리디렉션 됩니다. 내부 인식 교육을 설치한 경우 등 지정할 수 있습니다는 여기.</span><span class="sxs-lookup"><span data-stu-id="331d0-p113">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="331d0-p114">**제목** 필드에 대 한 텍스트를 지정 합니다. 받는 전자 메일 클라이언트에서 **주체 이름** 으로 표시 하는 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p114">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="331d0-159">대상을 받을 **전자 메일 본문** 을 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-159">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="331d0-160">`${username}`대상 이름을 전자 메일 본문에 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-160">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="331d0-161">`${loginserverurl}`삽입 하는 대상 사용자가 클릭 하 원합니다 URL</span><span class="sxs-lookup"><span data-stu-id="331d0-161">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="331d0-p115">**다음을** 차례로 **완료 날짜** 는 공격을 시작 하려면 선택 합니다. 창 피싱 전자 메일 메시지는 대상 받는 사람의 사서함으로 배달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p115">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="331d0-164">암호 스프레이 공격</span><span class="sxs-lookup"><span data-stu-id="331d0-164">Password-spray attack</span></span>

<span data-ttu-id="331d0-p116">조직에 대해 암호 스프레이 공격에는 나쁜 작업자 테 넌 트에서 유효한 사용자 목록을 성공적으로 획득 한 후에 일반적으로 사용 됩니다. 사람들이 사용 하는 일반적인 암호에 대 한 잘못 된 작업자 알 수 있습니다. 실행, 및를 무작위 접근 방법 보다 검색 하기가 어렵습니다 저렴 공격으로는 널리 사용 되는 공격입니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p116">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="331d0-168">이 공격 큰 대상 밑이 사용자에 대 한 일반적인 암호를 지정할 수에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-168">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="331d0-169">암호 스프레이 공격을 시뮬레이션 하기 위해</span><span class="sxs-lookup"><span data-stu-id="331d0-169">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="331d0-170">[보안 &amp; 준수 센터](https://security.microsoft.com), **위협 관리** 를 선택 \> **공격 시뮬레이터**합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-170">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="331d0-171">공격에 대 한 의미 있는 캠페인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-171">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="331d0-p117">대상 받는 사람을 지정 합니다. 이 개인 또는 조직에서 그룹 수 있습니다. 대상이 지정 된 받는 사람을 성공적으로 수행 하는 공격에 대 한 순서 대로 Exchange Online 사서함 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p117">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="331d0-p118">공격에 대 한 사용에 대 한 암호를 지정 합니다. 예, 시도할 수 하는 하나의 일반적이 고 관련 암호는 `Fall2017`합니다. 다른 수도 `Spring2018`, 또는 `Password1`합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p118">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="331d0-178">공격을 시작 하려면 **완료 날짜** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-178">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="331d0-179">대입 암호 공격</span><span class="sxs-lookup"><span data-stu-id="331d0-179">Brute-force password attack</span></span>

<span data-ttu-id="331d0-p119">조직에 대해 무작위 암호 공격에는 나쁜 작업자 테 넌 트의 주요 사용자 목록을 성공적으로 획득 한 후에 일반적으로 사용 됩니다. 이 공격을 단일 사용자의 계정에 대 한 암호의 집합을 시도에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p119">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="331d0-182">무작위 암호 공격을 시뮬레이션 하기 위해</span><span class="sxs-lookup"><span data-stu-id="331d0-182">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="331d0-183">[보안 &amp; 준수 센터](https://security.microsoft.com), **위협 관리** 를 선택 \> **공격 시뮬레이터**합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-183">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="331d0-184">공격에 대 한 의미 있는 캠페인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-184">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="331d0-p120">대상 받는 사람을 지정 합니다. 대상이 지정 된 받는 사람을 성공적으로 수행 하는 공격에 대 한 순서 대로 Exchange Online 사서함 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p120">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="331d0-p121">공격에 사용 하 여 암호의 집합을 지정 합니다. 이 작업을 수행 하려면 암호의 대화 목록에 대 한 텍스트 파일 (.txt)을 사용할 수 있습니다. 텍스트 파일의 파일 크기가 10MB를 초과할 수 없습니다. 줄당 한 암호를 사용 하 고 하드 리턴 후 마지막 암호를 목록에 포함 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p121">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="331d0-191">공격을 시작 하려면 **완료 날짜** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-191">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="331d0-192">공격 시뮬레이터의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="331d0-192">New features in Attack Simulator</span></span>

<span data-ttu-id="331d0-p122">새로운 기능 공격 시뮬레이터에 추가 되 고 됩니다. 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p122">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="331d0-p123">**고급 보고 기능을 제공**합니다. 열려는 공격 시뮬레이션 전자 메일 메시지를 가장 빠른 (또는 가장 느린) 시간, 메시지 등의 링크를 클릭 하는 가장 빠른 (또는 가장 느린) 시간 등의 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p123">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="331d0-p124">**전자 메일 템플릿 편집기**입니다. 앞으로 공격 시뮬레이션에 사용할 수 있는 사용자 지정, 다시 사용할 수 있는 전자 메일 서식 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="331d0-p124">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="331d0-199">[Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap) 개발에는 무엇이, 롤아웃은 기능 및 기능 이미 시작 된 참조를 참고 하십시오.</span><span class="sxs-lookup"><span data-stu-id="331d0-199">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>



