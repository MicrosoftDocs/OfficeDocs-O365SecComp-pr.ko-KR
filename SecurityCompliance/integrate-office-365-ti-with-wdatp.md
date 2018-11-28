---
title: Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: 보다 자세한 위협 관리 정보를 보려면 Windows Defender 고급 위협 보호와 Office 365 고급 위협 보호를 통합 합니다.
ms.openlocfilehash: 1198f53c47811d69b93106c413e3d3a09d83e736
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706142"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="25552-103">Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="25552-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="25552-p101">조직의 보안 팀의 일부인 경우와 Windows Defender 고급 위협 보호 (ATP) Office 365를 통합할 수 있습니다. 이 신속 하 게 하는 경우 사용자의 컴퓨터를 위험이 Office 365에 대 한 위협 요소를 조사 하는 경우를 이해할 수 있습니다. 등의 통합을 사용 하는 사용 하도록 설정 하면 많은 최근 경고 Windows Defender ATP 있는 이러한 장치와 어떻게 검색 된 전자 메일 메시지의 받는 사람에 사용 되는 컴퓨터의 목록도 참조 할 수 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25552-p101">If you are part of your organization's security team, you can integrate Office 365 with Windows Defender Advanced Threat Protection (ATP). This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender ATP.</span></span>
  
<span data-ttu-id="25552-107">다음 이미지에서 확인할 수 있는 Windows Defender ATP 통합을 사용 하도록 설정한 경우 표시 됩니다 **장치** 탭에서:</span><span class="sxs-lookup"><span data-stu-id="25552-107">The following image shows the **Devices** tab that you'll see when have Windows Defender ATP integration enabled:</span></span> 
  
![Windows Defender ATP 사용 하는 경우 알림 사용 하는 컴퓨터의 목록을 볼 수 있습니다.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="25552-p102">이 예제에서는 전자 메일 메시지의 받는 사람에 게는 4 개의 컴퓨터가 하 고 Windows Defender ATP에 대 한 알림을 한 명를 볼 수 있습니다. 새 탭에서 Windows Defender ATP에서 컴퓨터 페이지를 엽니다를 컴퓨터에 대 한 링크를 클릭 하.</span><span class="sxs-lookup"><span data-stu-id="25552-p102">In this example, you can see that the recipients of the email message have four machines and one has an alert in Windows Defender ATP. Clicking the link to a machine opens the machine page in Windows Defender ATP in a new tab.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="25552-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="25552-111">Requirements</span></span>

- <span data-ttu-id="25552-112">조직에 Office 365 위협 인텔리전스 및 Windows Defender ATP 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25552-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="25552-p103">Office 365 전역 관리자 이거나 보안 관리자 역할에 할당 된 [보안 &amp; 준수 센터](https://security.microsoft.com)합니다. (참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="25552-p103">You must be an Office 365 global administrator or have a security administrator role assigned in the [Security &amp; Compliance Center](https://security.microsoft.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="25552-115">Office 365 위협 인텔리전스와 Windows Defender ATP 포털에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25552-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender ATP portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="25552-116">Windows Defender ATP와 Office 365 위협 인텔리전스를 통합 하려면</span><span class="sxs-lookup"><span data-stu-id="25552-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="25552-117">Office 365와 Windows Defender ATP 포털에서 모두 Windows Defender ATP와 Office 365 위협 인텔리전스 통합 (영문) 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25552-117">Integrating Office 365 Threat Intelligence with Windows Defender ATP is set up both in Office 365 and in the Windows Defender ATP portal.</span></span>
  
1. <span data-ttu-id="25552-118">Office 365 전역 또는 보안 관리자로 이동 [https://security.microsoft.com](https://security.microsoft.com) 와 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="25552-118">As an Office 365 global or a security administrator, go to [https://security.microsoft.com](https://security.microsoft.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="25552-119">**위협 관리** 를 선택 \> **위협 탐색기**입니다.</span><span class="sxs-lookup"><span data-stu-id="25552-119">Choose **Threat management** \> **Threat explorer**.</span></span>
    
3. <span data-ttu-id="25552-120">**더 많은** 메뉴에서 **WDATP 설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="25552-120">On the **More** menu, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="25552-121">**Windows ATP에 연결**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="25552-121">Select **Connect to Windows ATP**.</span></span>
    
<span data-ttu-id="25552-p104">Office 365의 설정을 사용 하면를 변경한 후에 Windows Defender ATP에서 연결을 활성화 해야 합니다. 이렇게 하려면 [Windows Defender 고급 위협 보호 포털 사용](https://go.microsoft.com/fwlink/?linkid=859690)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="25552-p104">After you have changed the settings in Office 365, you must enable the connection from Windows Defender ATP. To do that, see [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="25552-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="25552-124">Related topics</span></span>

[<span data-ttu-id="25552-125">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="25552-125">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="25552-126">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="25552-126">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

