---
title: IOS 장치용 APNs 인증서 만들기
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
audience: Admin
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
description: Office 365에 대 한 모바일 장치 관리에서 iPad 및 Iphone와 같은 iOS 장치를 관리 하려면 다음 단계에 따라 APNs 인증서를 먼저 만듭니다.
ms.openlocfilehash: 17dae3e02520cdac2b1381039844d1657b12c4eb
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153760"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="8fe90-103">IOS 장치용 APNs 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="8fe90-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="8fe90-104">Office 365의 모바일 장치 관리에서 iPad 및 Iphone와 같은 iOS 장치를 관리 하려면 APNs 인증서를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe90-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="8fe90-105">이렇게 하려면 포털의 **설정** 링크에 있는 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe90-105">To do this, follow the steps from the **Set up** link on the portal page.</span></span> <span data-ttu-id="8fe90-106">( **보안 &amp; 및 준수 센터** \> **보안 정책** \> 으로 이동 **장치 관리** \> **설정을 관리**합니다.)</span><span class="sxs-lookup"><span data-stu-id="8fe90-106">(Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![모바일 장치 관리 필수 및 권장 단계 설정](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="8fe90-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span><span class="sxs-lookup"><span data-stu-id="8fe90-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="8fe90-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span><span class="sxs-lookup"><span data-stu-id="8fe90-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![APN 인증서 설치 대화 상자](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="8fe90-111"> Select *\*Next*\*. </span><span class="sxs-lookup"><span data-stu-id="8fe90-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="8fe90-112"> Create an APN certificate.</span><span class="sxs-lookup"><span data-stu-id="8fe90-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="8fe90-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal. </span><span class="sxs-lookup"><span data-stu-id="8fe90-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Apple APNS 포털이 선택 된 APN 알림 인증서 대화 상자 설치](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="8fe90-115">Sign in with an Apple ID.</span><span class="sxs-lookup"><span data-stu-id="8fe90-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="8fe90-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span><span class="sxs-lookup"><span data-stu-id="8fe90-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="8fe90-118">Select **Create a Certificate** and accept the **Terms of Use**.</span><span class="sxs-lookup"><span data-stu-id="8fe90-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="8fe90-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span><span class="sxs-lookup"><span data-stu-id="8fe90-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="8fe90-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span><span class="sxs-lookup"><span data-stu-id="8fe90-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="8fe90-121">If you're having trouble downloading the certificate, refresh your browser.</span><span class="sxs-lookup"><span data-stu-id="8fe90-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="8fe90-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span><span class="sxs-lookup"><span data-stu-id="8fe90-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="8fe90-123"> Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span><span class="sxs-lookup"><span data-stu-id="8fe90-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![검색 단추를 클릭 하 여 Apple에서 다운로드 한 APNS 인증서를 선택 합니다.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="8fe90-125">Select **Finish**.</span><span class="sxs-lookup"><span data-stu-id="8fe90-125">Select **Finish**.</span></span>
    
<span data-ttu-id="8fe90-126">**보안 &amp; 및 준수 센터** \> **보안 정책** \> 으로 돌아가기 **장치 관리** \> **설정을 관리** 하 여 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe90-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

