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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258638"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>iOS 장치용 APNs 인증서 만들기

 Office 365의 모바일 장치 관리에서 iPad 및 iphone와 같은 iOS 장치를 관리 하려면 APNs 인증서를 만들어야 합니다. 
  
이렇게 하려면 포털의 **설정** 링크에 있는 단계를 수행 합니다. ( **보안 &amp; 및 준수 센터** \> **보안 정책** \> 으로 이동 **장치 관리** \> **설정을 관리**합니다.)
  
![모바일 장치 관리 필수 및 권장 단계 설정](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.
    
2. Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember. 
    
    ![APN 인증서 설치 대화 상자](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3.  Select **Next**. 
    
4.  Create an APN certificate.
    
  - Select **Apple APNS Portal** to open the Apple Push Certificates Portal.  
    
    ![Apple APNS 포털이 선택 된 APN 알림 인증서 대화 상자 설치](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Sign in with an Apple ID.
    
    > [!IMPORTANT]
    > Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate. 
  
  - Select **Create a Certificate** and accept the **Terms of Use**.
    
  - **Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.
    
  - **Download** the APN certificate created by the Apple Push Certificate Portal to your computer. 
    
    > [!TIP]
    > If you're having trouble downloading the certificate, refresh your browser. 
  
5. Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page. 
    
6.  Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.
    
    ![검색 단추를 클릭 하 여 Apple에서 다운로드 한 APNS 인증서를 선택 합니다.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Select **Finish**.
    
**보안 &amp; 및 준수 센터** \> **보안 정책** \> 으로 돌아가기 **장치 관리** \> **설정을 관리** 하 여 설치를 완료 합니다. 
  

