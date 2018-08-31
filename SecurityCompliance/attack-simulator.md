---
title: Office 365의 공격 시뮬레이터
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/19/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: 인터넷 공격 공격 시뮬레이터를 사용 하 여 실행할 수의 약 3 다양 한 종류에 알아봅니다.
ms.openlocfilehash: 364144c0b2f8109c67fb262ce879414088380ebe
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533233"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="859f1-103">Office 365의 공격 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="859f1-103">Attack Simulator in Office 365</span></span>

<span data-ttu-id="859f1-p101">공격 시뮬레이터 (에 포함 된 [Office 365 위협 인텔리전스](office-365-ti.md))와 조직의 보안 팀의 구성원 이어야 하는 경우 실행할 수 있습니다 사실적인 공격 시나리오 조직에서. 이 도울수 식별 하 고 실제 공격 아래 줄에 영향을 줍니다 전에 공격에 취약 한 사용자를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p101">With Attack Simulator (included in [Office 365 Threat Intelligence](office-365-ti.md)), if you are a member of your organization's security team, you can run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="859f1-106">공격</span><span class="sxs-lookup"><span data-stu-id="859f1-106">The Attacks</span></span>

<span data-ttu-id="859f1-107">미리 보기 버전에서 세 종류의 실행할 수 있는 공격 시뮬레이션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-107">At preview release we offer three kinds of attack simulations that you can run:</span></span>
  
- [<span data-ttu-id="859f1-108">표시 이름 창 피싱 공격</span><span class="sxs-lookup"><span data-stu-id="859f1-108">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="859f1-109">암호 스프레이 공격</span><span class="sxs-lookup"><span data-stu-id="859f1-109">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="859f1-110">대입 암호 공격</span><span class="sxs-lookup"><span data-stu-id="859f1-110">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="859f1-111">공격이 성공적으로 시작 하는 공격을 실행 하 고 로그온 하는 계정이 다단계 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-111">For an attack to be successfully launched, the account that is running the attack and logged on must use multi-factor authentication.</span></span>
  
> [!NOTE]
> <span data-ttu-id="859f1-112">조건부 액세스에 대 한 지원 출시 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-112">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="859f1-113">보안에서 공격 시뮬레이터에 액세스 하려면 &amp; 준수 센터 **위협 관리** 를 선택 \> **공격 시뮬레이터**합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-113">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="859f1-114">시작 하기 전에...</span><span class="sxs-lookup"><span data-stu-id="859f1-114">Before you begin...</span></span>

<span data-ttu-id="859f1-115">및 조직 공격 시뮬레이터에 대 한 다음과 같은 요구 사항을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-115">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
  
- <span data-ttu-id="859f1-116">조직에 [Office 365 위협 인텔리전스](office-365-ti.md)공격 시뮬레이터 보안에 표시 된 &amp; 준수 센터 ( **위협 관리** 로 이동 \> **공격 시뮬레이터**)</span><span class="sxs-lookup"><span data-stu-id="859f1-116">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span>
    
- <span data-ttu-id="859f1-p102">조직의 전자 메일은 Exchange Online에서 호스팅됩니다. (공격 시뮬레이터 온-프레미스 전자 메일 서버에 대해 사용할 수 없는 경우)</span><span class="sxs-lookup"><span data-stu-id="859f1-p102">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="859f1-119">사용자가 Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="859f1-119">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="859f1-120">조직에서 사용 중인 [Office 365 사용자에 대해 다단계 인증](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span><span class="sxs-lookup"><span data-stu-id="859f1-120">Your organization is using [Multi-factor authentication for Office 365 users](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span></span>
    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="859f1-121">표시 이름 창 피싱 공격</span><span class="sxs-lookup"><span data-stu-id="859f1-121">Display name spear-phishing attack</span></span>

<span data-ttu-id="859f1-p103">피싱은 사회 공학 스타일 공격으로 분류 하는 공격의 광범위 한 제품군에 대 한 일반 용어입니다. 이 공격에서는 창 피싱, 개인 또는 조직의 특정 그룹을 목표로 하는 더욱 효과적인된 공격에 초점을 맞춥니다. 일반적으로 사용자 지정 된 공격에 일부 검사를 수행 하 고 임원 조직 내에서 보낸 것 처럼 보이는 전자 메일 메시지와 같은 받는 사람에 대 한 신뢰를 생성 하는 표시 이름을 사용 하 여 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p103">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="859f1-p104">이 공격 알려주는 메시지의 표시 이름 및 인증 원본 주소를 변경 하 여에서 시작 된 것으로 표시 되는 조작 (영문)에 중점을 둡니다. 창 피싱 공격은 성공, 사용자의 자격 증명에 액세스할 사이버 범죄자 들에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p104">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="859f1-127">창 피싱 공격을 시뮬레이션 하기 위해</span><span class="sxs-lookup"><span data-stu-id="859f1-127">To simulate a spear-phishing attack</span></span>

![전자 메일 본문 작성](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="859f1-p105">**전자 메일 본문** 필드 자체에서 직접 서식 있는 HTML 편집기를 만들 수도 있고 HTML 원본으로 작업할 수 있습니다. HTML에 포함 될 내용에 대 한 중요 한 필드를 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p105">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source. There are two important fields for inclusion in the HTML:</span></span> 
  
1. <span data-ttu-id="859f1-131">보안에서 &amp; 준수 센터 **위협 관리** 를 선택 \> **공격 시뮬레이터**합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-131">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="859f1-132">공격에 대 한 의미 있는 캠페인 이름을 지정 하거나 서식 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-132">Specify a meaningful campaign name for the attack or select a template.</span></span>
    
    ![피싱 시작 페이지](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="859f1-p106">대상 받는 사람을 지정 합니다. 이 개인 또는 조직에서 그룹 수 있습니다. 대상이 지정 된 받는 사람을 성공적으로 수행 하는 공격에 대 한 순서 대로 Exchange Online 사서함 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p106">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
    ![받는 사람 선택](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="859f1-138">피싱 메일 세부 정보를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-138">Configure the Phishing email details.</span></span>
    
    ![전자 메일 세부 정보를 구성 합니다.](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
  
    <span data-ttu-id="859f1-p107">HTML 서식을 수도 있고 같이 복잡 한 기본 캠페인이 알아야 합니다. HTML 그대로 이미지와 believability를 향상 시키기 위해 텍스트를 삽입할 수 있습니다. 받는 전자 메일 클라이언트에서 받은 메시지 모양을에서 제어할을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p107">The HTML formatting can be as complex or basic as your campaign needs. As it is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
1. <span data-ttu-id="859f1-p108">**(이름)에서** 필드에 대 한 텍스트를 입력 합니다. 받는 전자 메일 클라이언트에 **표시 이름** 을 표시 하는 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p108">Enter text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
2. <span data-ttu-id="859f1-p109">텍스트 또는 **에서** 필드를 입력 합니다. 받는 전자 메일 클라이언트에서 보낸 사람의 전자 메일 주소으로 표시 하는 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p109">Enter text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="859f1-p110">조직 내에서 기존 전자 메일 네임 스페이스를 입력할 수 있습니다 (이 수행 하는 확인 실제로 매우 높음 보안 모델을 용이 하 게 받는 클라이언트에서 해결 하는 전자 메일 주소)을 하거나 외부 전자 메일 주소를 입력할 수 있습니다. 하지만 실제로 존재 하지 않아도 지정 하는 전자 메일 주소 user@domainname.extension와 같은 유효한 SMTP 주소를의 형식에 따라 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p110">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
3. <span data-ttu-id="859f1-p111">드롭다운 선택기를 사용 하 여 공격 받을 수 있는 내 해야 콘텐츠 형식의 반영 하는 피싱 로그인 서버 URL을 선택 합니다. 여러 테마가 적용 된 Url 문서 배달, 기술, 급여 등 등,를 선택할 수 제공 됩니다. 이것이 효과적으로 URL을 대상으로 지정 된 사용자를 클릭 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p111">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
4. <span data-ttu-id="859f1-p112">사용자 지정 시작 페이지 URL을 입력 합니다. 이 사용 하 여 공격에 성공의 끝에 지정 된 URL로 사용자 리디렉션 됩니다. 내부 인식 교육을 설치한 경우 등 지정할 수 있습니다는 여기.</span><span class="sxs-lookup"><span data-stu-id="859f1-p112">Enter a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
5. <span data-ttu-id="859f1-p113">**제목** 필드에 대 한 텍스트를 입력 합니다. 받는 전자 메일 클라이언트에서 **주체 이름** 으로 표시 하는 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p113">Enter text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
5. <span data-ttu-id="859f1-156">대상을 받을 **전자 메일 본문** 을 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-156">Compose the **Email body** that the target will receive.</span></span> 
  
 <span data-ttu-id="859f1-157">전자 메일 본문에 대상 이름을 삽입 하는 **${username}**</span><span class="sxs-lookup"><span data-stu-id="859f1-157">**${username}** inserts the targets name into the Email body</span></span> 
  
 <span data-ttu-id="859f1-158">대상 사용자가 클릭 하 원합니다 URL을 삽입 하는 **${loginserverurl}**</span><span class="sxs-lookup"><span data-stu-id="859f1-158">**${loginserverurl}** inserts the URL we want target users to click</span></span> 
    
6. <span data-ttu-id="859f1-p114">**다음을** 차례로 **완료 날짜** 는 공격을 시작 하려면 선택 합니다. 창 피싱 전자 메일 메시지는 대상 받는 사람의 사서함으로 배달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p114">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="859f1-161">암호 스프레이 공격</span><span class="sxs-lookup"><span data-stu-id="859f1-161">Password-spray attack</span></span>

<span data-ttu-id="859f1-p115">조직에 대해 암호 스프레이 공격은 매우 나쁨 작업자는 테 넌 트를 사용 하는 일반적인 암호의 지식을 활용 하 여에서 유효한 사용자 목록을 열거 성공적으로 후에 일반적으로 사용 됩니다. 것이 저렴 공격을 실행 하 고 있기 때문에 널리 사용 되 고 무작위 접근 방법 보다 검색 하기 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p115">A password spray attack against an organization is typically used after a bad actor has successfully enumerated a list of valid users from the tenant, utilizing their knowledge of common passwords used. It is utilized widely as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="859f1-164">이 공격 큰 대상 밑이 사용자에 대 한 일반적인 암호를 지정할 수에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-164">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="859f1-165">암호 스프레이 공격을 시뮬레이션 하기 위해</span><span class="sxs-lookup"><span data-stu-id="859f1-165">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="859f1-166">보안에서 &amp; 준수 센터 **위협 관리** 를 선택 \> **공격 시뮬레이터**합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-166">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="859f1-167">공격에 대 한 의미 있는 캠페인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-167">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="859f1-p116">대상 받는 사람을 지정 합니다. 이 개인 또는 조직에서 그룹 수 있습니다. 대상이 지정 된 받는 사람을 성공적으로 수행 하는 공격에 대 한 순서 대로 Exchange Online 사서함 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p116">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="859f1-p117">공격에 대 한 사용에 대 한 암호를 지정 합니다. 예, 시도할 수 하는 하나의 일반적이 고 관련 암호는 `Fall2017`합니다. 다른 수도 `Spring2018`, 또는 `Password1`합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p117">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="859f1-174">공격을 시작 하려면 **완료 날짜** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-174">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="859f1-175">대입 암호 공격</span><span class="sxs-lookup"><span data-stu-id="859f1-175">Brute-force password attack</span></span>

<span data-ttu-id="859f1-p118">조직에 대해 무작위 암호 공격은 매우 나쁨 작업자는 테 넌 트의 주요 사용자 목록을 열거 성공적으로 후에 일반적으로 사용 됩니다. 이 공격 집합을 단일 사용자에 대해 암호를 지정할 수에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p118">A brute-force password attack against an organization is typically used after a bad actor has successfully enumerated a list of key users from the tenant. This attack focuses on letting you specify a set of passwords against a single user.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="859f1-178">무작위 암호 공격을 시뮬레이션 하기 위해</span><span class="sxs-lookup"><span data-stu-id="859f1-178">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="859f1-179">보안에서 &amp; 준수 센터 **위협 관리** 를 선택 \> **공격 시뮬레이터**합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-179">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="859f1-180">공격에 대 한 의미 있는 캠페인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-180">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="859f1-p119">대상 받는 사람을 지정 합니다. 대상이 지정 된 받는 사람을 성공적으로 수행 하는 공격에 대 한 순서 대로 Exchange Online 사서함 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p119">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="859f1-p120">공격에 사용 하 여 암호의 집합을 지정 합니다. 예, 시도할 수 하는 하나의 일반적이 고 관련 암호는 `Fall2017`합니다. 다른 수도 `Spring2018`, 또는 `Password1`합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-p120">Specify a set of passwords to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="859f1-186">공격을 시작 하려면 **완료 날짜** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="859f1-186">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="related-topics"></a><span data-ttu-id="859f1-187">관련 항목</span><span class="sxs-lookup"><span data-stu-id="859f1-187">Related topics</span></span>

[<span data-ttu-id="859f1-188">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="859f1-188">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  

