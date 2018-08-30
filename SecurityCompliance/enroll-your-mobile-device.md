---
title: Office 365의 모바일 장치 등록
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/25/2018
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- MED150
- MBS150
ms.assetid: c8ac722d-dcaf-4135-8345-3e6327f5d3c5
description: Office 365 서비스를 장치와 함께 사용할 수 있으려면 Office 365 (MDM)에 대 한 모바일 장치 관리에 등록 하려면 다음이 단계를 수행 해야할 수 있습니다. 진행 중인 작업을 추가 하거나 처음에 대 한 전자 메일 계정을 장치로 학교 때이 수행 됩니다.
ms.openlocfilehash: 63e4052d42007d97928f158a704beb9721758a44
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272303"
---
# <a name="enroll-your-mobile-device-in-office-365"></a><span data-ttu-id="25f56-104">Office 365의 모바일 장치 등록</span><span class="sxs-lookup"><span data-stu-id="25f56-104">Enroll your mobile device in Office 365</span></span>

<span data-ttu-id="25f56-p102">작업에 대 한 전화, 태블릿 및 기타 모바일 장치를 사용 하 여 이며 편리 하 게 유지 관련 정보를 받아보십시오 사무실 밖에 있는 동안 비즈니스 프로젝트에서 작업 합니다. Office 365 서비스를 장치와 함께 사용할 수 있으려면 먼저 등록 해당 모바일 장치 관리에 대 한 Office 365 (MDM) Microsoft Intune 회사 포털을 사용 하 여 해야할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-p102">Using your phone, tablet, and other mobile devices for work is a great way to stay informed and work on business projects while you're away from the office. Before you can use Office 365 services with your device, you may need to first enroll it in Mobile Device Management for Office 365 (MDM) using Microsoft Intune Company Portal.</span></span>
  
<span data-ttu-id="25f56-p103">조직에서는 직원 모바일 장치를 사용 하 여 업무상 중요 한 데이터를 통해 보호 하 고 위해 준수 요구 사항을 충족 하는 동안 작업 전자 메일, 일정 및 문서를 안전 하 게 액세스할 수 있도록 MDM를 선택 합니다. [Office 365의에서 MDM에 알아봅니다](https://go.microsoft.com/fwlink/?LinkId=615142).</span><span class="sxs-lookup"><span data-stu-id="25f56-p103">Organizations choose MDM so that employees can use their mobile devices to securely access work email, calendars, and documents while the business secures important data and meets their compliance requirements. [Learn about MDM in Office 365](https://go.microsoft.com/fwlink/?LinkId=615142).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="25f56-p104">Office 365에 대 한 MDM에서 장치를 등록 하는 경우 장치 지우기 작업 조직에 대 한 옵션을 허용 하는 함께 암호를 설정 하려면 필요할 합니다. 장치 지우기 수행할 수 있습니다 (Office 365 관리 센터)에서 등 사용 현황 용어는 손상 된 경우 또는 암호를 잘못 입력 너무 여러 번 반복 하는 경우 장치에서 모든 데이터를 제거 하려면.</span><span class="sxs-lookup"><span data-stu-id="25f56-p104">When you enroll your device in MDM for Office 365, you might be required to set up a password, together with allowing the option for your work organization to wipe the device. A device wipe can be performed (from the Office 365 admin center), for example, to remove all data from the device if the password is entered incorrectly too many times or if usage terms are broken.</span></span> 
  
 <span data-ttu-id="25f56-111">**지원되는 장치**</span><span class="sxs-lookup"><span data-stu-id="25f56-111">**Supported devices**</span></span>
  
<span data-ttu-id="25f56-p105">MDM 및 InTune 대부분을 모두는 아니지만, 모바일 장치에서 작동 합니다. 다음은 지원 MDM Office 365에 대 한.</span><span class="sxs-lookup"><span data-stu-id="25f56-p105">MDM and InTune works with most, but not all, mobile devices. The following are supported with MDM for Office 365.</span></span>
  
- <span data-ttu-id="25f56-114">iOS 7.1 이상</span><span class="sxs-lookup"><span data-stu-id="25f56-114">iOS 7.1 or later</span></span>
    
- <span data-ttu-id="25f56-115">Android 4 이상</span><span class="sxs-lookup"><span data-stu-id="25f56-115">Android 4 or later</span></span>
    
- <span data-ttu-id="25f56-116">Windows 8.1 (전화 및 PC) 및 Windows 10을 포함 하는 나중에</span><span class="sxs-lookup"><span data-stu-id="25f56-116">Windows 8.1 (Phone and PC) and later to include Windows 10</span></span>
    
- <span data-ttu-id="25f56-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="25f56-117">Windows 10</span></span>
    
<span data-ttu-id="25f56-118">장치, 위에 나열 되지 않으면 MDM 및 Intune 함께 사용 해야 하는 경우 작업이 나 교육용 관리자에 게 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-118">If your device is not listed above, and you need to use it with MDM and Intune, contact your work or school administrator.</span></span>
  
> [!TIP]
> <span data-ttu-id="25f56-119">장치를 등록 하는데 문제가 경우 참조: [Office 365에 대 한 mdm Troubleshoot 장치 등록](troubleshoot-mdm.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-119">If you're having trouble enrolling your device, see: [Troubleshoot device enrollment with MDM for Office 365](troubleshoot-mdm.md).</span></span> 
  
## <a name="set-up-your-mobile-device-with-intune-and-mdm-for-office-365"></a><span data-ttu-id="25f56-120">Office 365에 대 한 Intune MDM와 모바일 장치를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-120">Set up your mobile device with Intune and MDM for Office 365</span></span>

<span data-ttu-id="25f56-121">Office 365 및 MDM.에 의해 관리를 위한 장치를 사용 하면 Intune 회사 포털</span><span class="sxs-lookup"><span data-stu-id="25f56-121">The Intune Company Portal enables a device to be managed by Office 365 and MDM.</span></span>
  
### <a name="iphone-or-ipad"></a><span data-ttu-id="25f56-122">iPhone 또는 iPad</span><span class="sxs-lookup"><span data-stu-id="25f56-122">iPhone or iPad</span></span>

> [!TIP]
> <span data-ttu-id="25f56-123">이 단계를 완료할 때까지 전자 메일을 송수신 하는 작업을 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-123">You won't be able to send and receive email until you complete this step.</span></span> 
  
> <span data-ttu-id="25f56-124">이동, Apple App Store를 다운로드 하 고 Intune 회사 포털을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-124">Go to the Apple App Store, download and install Intune Company Portal.</span></span>
    
> <span data-ttu-id="25f56-125">IOS 전화기를 [구성 하 고 연결 하려면 다음이 단계를 수행](https://go.microsoft.com/fwlink/?linkid=875316) 하거나 태블릿 Office 365에 회사 포털을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-125">[Follow these steps to configure and connect](https://go.microsoft.com/fwlink/?linkid=875316) your iOS phone or tablet with the Company portal to Office 365.</span></span> 
    
### <a name="android-phone-or-tablet"></a><span data-ttu-id="25f56-126">Android 휴대폰 또는 태블릿</span><span class="sxs-lookup"><span data-stu-id="25f56-126">Android phone or tablet</span></span>

> [!TIP]
> <span data-ttu-id="25f56-127">이 단계를 완료할 때까지 전자 메일을 송수신 하는 작업을 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-127">You won't be able to send and receive email until you complete this step.</span></span> 
  
> <span data-ttu-id="25f56-128">이동 Google 재생 저장소에 다운로드 하 고 Intune 회사 포털을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-128">Go to the Google Play store, download and install Intune Company Portal.</span></span>
    
> <span data-ttu-id="25f56-129">Android 휴대폰을 [구성 하 고 연결 하려면 다음이 단계를 수행](https://go.microsoft.com/fwlink/?linkid=875317) 하거나 태블릿 Office 365에 회사 포털을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-129">[Follow these steps to configure and connect](https://go.microsoft.com/fwlink/?linkid=875317) your Android phone or tablet with the Company portal to Office 365.</span></span> 
    
## <a name="whats-next"></a><span data-ttu-id="25f56-130">다음</span><span class="sxs-lookup"><span data-stu-id="25f56-130">What's next</span></span>

<span data-ttu-id="25f56-131">장치는 Office 365에 대 한 MDM에 등록 되, 장치에서 Office 응용 프로그램을 사용 하 여 전자 메일, 일정, 연락처 및 문서 작업을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25f56-131">After your device is enrolled in MDM for Office 365, you can start using Office apps on your device to work with email, calendar, contacts, and documents.</span></span>
  

