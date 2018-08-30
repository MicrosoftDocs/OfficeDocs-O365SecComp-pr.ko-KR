---
title: Outlook 데스크톱의 감독 추가 기능 설치
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- ZOL160
ms.assetid: 6c5620e6-aba3-4910-8f3a-b55451656ff7
description: Outlook의 데스크톱 버전은 Office 365 감독 추가 기능 설치
ms.openlocfilehash: 0bddf305087bf0d9552c7671da5306db8352143f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533010"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a><span data-ttu-id="3c51c-103">Outlook 데스크톱의 감독 추가 기능 설치</span><span class="sxs-lookup"><span data-stu-id="3c51c-103">Install the Supervision add-in for Outlook desktop</span></span>

<span data-ttu-id="3c51c-p101">감독 정책에 의해 식별 된 통신을 검토 하려면 검토자의 감독 추가 기능에서 사용 Outlook 및 Outlook 용 응용 프로그램 웹. 추가 기능에 자동으로 설치 Outlook web app에서 정책에 지정 하는 모든 검토자에 대 한. 그러나 검토자 데스크톱 버전의 Outlook 설치 하는 일부 단계를 통해 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-p101">To review communications identified by a supervision policy, reviewers use the Supervision add-in for Outlook and Outlook web app. The add-in is installed automatically in Outlook web app for all reviewers you specified in the policy. However, reviewers must run through some steps to install it in the desktop version of Outlook.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3c51c-p102">감독 정책을 사용 하 여 조직에 대 한 Office 365 e 5를 구독을 해야 합니다. 해당 요금제에 가입한 상태 감독 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-p102">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="3c51c-109">1 단계: 감독 사서함에 대 한 주소를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-109">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="3c51c-110">Outlook 데스크톱 용 추가 기능에서 설치를 사용 하 여 감독 정책 설치의 일부로 만들어진 감독 사서함에 대 한 주소가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-110">To install the add-in for Outlook desktop, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3c51c-111">다른 사람이 만든 정책, 하는 경우이 주소를 추가 기능을 설치 하도록 받이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-111">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span> 
  
 <span data-ttu-id="3c51c-112">**감독 사서함 주소를 찾으려면**</span><span class="sxs-lookup"><span data-stu-id="3c51c-112">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="3c51c-113">에 로그인은 [보안 &amp; 준수 센터](https://protection.office.com) Office 365 조직에서 관리 계정에 대 한 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-113">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="3c51c-114">**데이터 관리 방식** 으로 이동 \> **감독**합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-114">Go to **Data governance** \> **Supervision**.</span></span>
    
3. <span data-ttu-id="3c51c-115">수집 하 고 검토 하려는 통신 감독 정책을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-115">Click the supervision policy that's gathering the communications you want to review.</span></span>
    
4. <span data-ttu-id="3c51c-116">정책에 자세히 설명 플라이 아웃, 아래에서 * * 감독 사서함 * *, 주소를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-116">In the policy details flyout, under ** Supervision mailbox **, copy the address.</span></span> 
    
    ![강조 표시 된 감독 사서함 주소를 표시 한 감독 정책 세부 정보 플라이 아웃의 ' 감독 사서함 ' 섹션](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a><span data-ttu-id="3c51c-118">2 단계: Outlook 데스크톱 액세스에 대 한 감독 사서함 구성</span><span class="sxs-lookup"><span data-stu-id="3c51c-118">Step 2: Configure the supervision mailbox for Outlook desktop access</span></span>

<span data-ttu-id="3c51c-119">다음으로, 검토자는 두 Exchange Online PowerShell 명령을 실행 하 여 Outlook 감독 사서함에 연결할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-119">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="3c51c-p103">Exchange Online PowerShell에 연결 합니다. [어떻게 해야 합니까?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="3c51c-p103">Connect to Exchange Online PowerShell. [How do I do this?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span></span>
    
2. <span data-ttu-id="3c51c-122">다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-122">Run the following commands.</span></span>
    
  ```
  Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccessSet-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false
  ```

    <span data-ttu-id="3c51c-123">여기서 *SupervisoryReview{GUID}@domain.onmicrosoft.com* 위의 1 단계에서에서 복사한 주소 이며 *사용자* 가 다음 단계에서 감독 사서함에 연결 하는 검토자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-123">Where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in the next step.</span></span> 
    
3. <span data-ttu-id="3c51c-124">대기 아래 3 단계로 이동 하기 전에 1 시간 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-124">Wait at least an hour before moving on to Step 3 below.</span></span>
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="3c51c-125">3 단계: 감독 사서함에 연결 하 여 Outlook 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="3c51c-125">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="3c51c-126">마지막 단계에 대 한 검토자 감독 사서함에 연결 하는 Outlook 프로필을 만들려면 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-126">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3c51c-p104">새 Outlook 프로필을 만들려면 Windows 제어판의 메일 설정을 사용 합니다. 이러한 설정으로 이동 하기 위해 취할 경로 사용 하는 Windows 운영 체제 (Windows 7, Windows 8 또는 Windows 10) 하 고 설치 된 outlook 버전에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-p104">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel. The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using and which version of Outlook is installed.</span></span> 
  
1. <span data-ttu-id="3c51c-129">제어판을 열고 위쪽 창에 **검색** 상자에서 **메일**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-129">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="3c51c-p105">확실 하지 않은 경우 제어판으로 이동 하는 방법? 참조 [제어판이?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)</span><span class="sxs-lookup"><span data-stu-id="3c51c-p105">Not sure how to get to the Control Panel? See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)</span></span>
  
2. <span data-ttu-id="3c51c-132">**메일** 앱을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-132">Open the **Mail** app.</span></span> 
    
3. <span data-ttu-id="3c51c-133">**메일 설정-Outlook** **프로필 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-133">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span>
    
    ![' 메일 설정-Outlook'' 프로필 보기 ' 단추를 강조 표시 된 대화 상자](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. <span data-ttu-id="3c51c-p106">**메일** **추가**클릭 합니다. 그런 다음, **새 프로필**(예: **감독**) 감독 사서함에 대 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-p106">In **Mail**, click **Add**. Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span>
    
    ![' 프로 파일 이름 ' 상자에 대화명 '감독' ' 새 프로필 ' 대화 상자](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. <span data-ttu-id="3c51c-138">**Office 365에 연결 Outlook** **다른 계정으로 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-138">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span>
    
    ![강조 표시 한 '다른 계정으로 연결' 링크와 함께 ' Office 365로 Outlook에 연결 ' 메시지](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. <span data-ttu-id="3c51c-140">**자동 계정 설정**,에서 **수동 설치 또는 추가 서버 유형**, 선택 하 고 **** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-140">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="3c51c-p107">**계정 유형 선택** **Office 365**를 선택 합니다. 그런 다음, **전자 메일 주소** 상자에서 이전에 복사한 감독 사서함의 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-p107">In **Choose Your Account Type**, choose **Office 365**. Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span> 
    
    ![강조 표시 하 고 ' 전자 메일 주소 ' 상자를 표시 하는 Outlook에서 계정 추가 ' 대화의 ' 계정 유형 선택 ' 페이지입니다.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. <span data-ttu-id="3c51c-144">대화 상자가 나타나면 Office 365 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-144">When prompted, enter your Office 365 credentials.</span></span>
    
9. <span data-ttu-id="3c51c-145">성공적인를 볼 수 있습니다는 **감독- \<정책 이름\> ** Outlook에서 폴더 목록 보기에 나열 된 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="3c51c-145">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span> 
    

