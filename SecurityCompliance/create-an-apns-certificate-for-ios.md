---
title: iOS 장치용 APNs 인증서 만들기
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Office 365에 대 한 모바일 장치 관리에서 iPad 및 iphone와 같은 iOS 장치를 관리 하려면 다음 단계에 따라 APNs 인증서를 먼저 만듭니다.
ms.openlocfilehash: 5f82690f0add5f1aae95a089d9cdfc0b320ae596
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220458"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="6ec2a-103">iOS 장치용 APNs 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="6ec2a-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="6ec2a-104">Office 365의 모바일 장치 관리에서 iPad 및 iphone와 같은 iOS 장치를 관리 하려면 APNs 인증서를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="6ec2a-p101">이렇게 하려면 포털의 **설정** 링크에 있는 단계를 수행 합니다. ( **보안 &amp; 및 준수 센터** \> **보안 정책** \> 으로 이동 **장치 관리** \> **설정을 관리**합니다.)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-p101">To do this, follow the steps from the **Set up** link on the portal page. (Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![모바일 장치 관리 필수 및 권장 단계 설정](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="6ec2a-108">**iOS 장치용 APNs 인증서 구성**옆에 있는 **설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="6ec2a-109">**CSR 파일 다운로드** 를 선택 하 고 사용자가 잊어버린 컴퓨터에 인증서 서명 요청을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![APN 인증서 설치 대화 상자](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="6ec2a-111">**다음** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="6ec2a-112">APN 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="6ec2a-113">apple **APNS portal** 을 선택 하 여 apple Push certificate portal을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Apple APNS 포털이 선택 된 APN 알림 인증서 대화 상자 설치](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="6ec2a-115">Apple ID로 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="6ec2a-p102">계정을 관리 하는 사용자가 퇴사 하더라도 조직에 남아 있는 전자 메일 계정과 연결 된 회사 Apple ID를 사용 합니다. 이 id는 인증서를 갱신할 때 같은 id를 사용 해야 하므로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="6ec2a-118">**인증서 만들기** 및 **사용 약관**에 동의를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="6ec2a-119">Office 365에서 컴퓨터로 다운로드 한 인증서 서명 요청으로 **이동한** 후 **업로드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="6ec2a-120">Apple Push certificate Portal에서 만든 APN 인증서를 컴퓨터로 **다운로드** 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="6ec2a-121">인증서를 다운로드 하는 데 문제가 있으면 브라우저를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="6ec2a-122">Office 365로 돌아가 **다음** 을 선택 하 여 **APNS 인증서 업로드** 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="6ec2a-123">Apple Push certificate 포털에서 다운로드 한 APN 인증서로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![검색 단추를 클릭 하 여 Apple에서 다운로드 한 APNS 인증서를 선택 합니다.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="6ec2a-125">**마침을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-125">Select **Finish**.</span></span>
    
<span data-ttu-id="6ec2a-126">**보안 &amp; 및 준수 센터** \> **보안 정책** \> 으로 돌아가기 **장치 관리** \> **설정을 관리** 하 여 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

