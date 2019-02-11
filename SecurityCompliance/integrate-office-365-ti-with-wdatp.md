---
title: Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: 보다 자세한 위협 관리 정보를 보려면 Windows Defender 고급 위협 보호와 Office 365 고급 위협 보호를 통합 합니다.
ms.openlocfilehash: e5070e003972ae5308415dcdcca85b069d1163ac
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29382541"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="e30e9-103">Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="e30e9-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="e30e9-p101">조직의 보안 팀의 일부인 경우에 Windows Defender 고급 위협 보호 된 Office 365 고급 위협 보호 및 위협 인텔리전스 기능을 통합할 수 있습니다. 이 신속 하 게 하는 경우 사용자의 컴퓨터를 위험이 Office 365에 대 한 위협 요소를 조사 하는 경우를 이해할 수 있습니다. 등의 통합을 사용 하는 사용 하도록 설정 하면 많은 최근 경고 Windows Defender 고급 위협 보호 있는 이러한 장치와 어떻게 검색 된 전자 메일 메시지의 받는 사람에 사용 되는 컴퓨터의 목록도 참조 할 수를 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="e30e9-107">다음 이미지에서 확인할 수 있는 Windows Defender 고급 위협 보호 통합을 사용 하도록 설정한 경우 표시 됩니다 **장치** 탭에서:</span><span class="sxs-lookup"><span data-stu-id="e30e9-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Windows Defender ATP 사용 하는 경우 알림 사용 하는 컴퓨터의 목록을 볼 수 있습니다.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="e30e9-p102">이 예제에서는 전자 메일 메시지의 받는 사람에 게 4 개의 장치 하 고 알림을 한 명 있는지 확인할 수 있습니다. 장치에 대 한 링크를 클릭 하는 Windows Defender 고급 위협 보호 포털에서 해당 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="e30e9-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e30e9-111">Requirements</span></span>

- <span data-ttu-id="e30e9-112">조직에 Office 365 위협 인텔리전스 및 Windows Defender ATP 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="e30e9-p103">Office 365 전역 관리자 이거나에 할당 된 보안 관리자 역할 (예: 보안 관리자)는 [보안 &amp; 준수 센터](https://protection.office.com)합니다. (참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="e30e9-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="e30e9-115">Office 365 위협 인텔리전스와 Windows Defender 고급 위협 보호 포털에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="e30e9-116">Windows Defender ATP와 Office 365 위협 인텔리전스를 통합 하려면</span><span class="sxs-lookup"><span data-stu-id="e30e9-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="e30e9-117">규정 준수 센터 및 Windows Defender 고급 위협 보호 포털 Office 365 보안 &는 모두를 사용 하 여 Windows Defender 고급 위협 보호 된 Office 365 위협 인텔리전스 통합 (영문) 기능이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="e30e9-118">Office 365 전역 관리자 또는 보안 관리자도로 이동 [https://protection.office.com](https://protection.office.com) 와 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="e30e9-119">**위협 관리** 를 선택 \> **탐색기**입니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="e30e9-120">![위협 관리 메뉴에서 탐색기](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="e30e9-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="e30e9-121">화면 오른쪽 위 모서리에서 **WDATP 설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="e30e9-122">Windows Defender ATP 연결 대화 상자에서 Windows ATP에 연결을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30e9-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Windows Defender ATP 연결](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="e30e9-p104">Windows Defender 고급 위협 보호에 대 한 연결을 사용 하도록 설정 합니다. [Windows Defender 고급 위협 보호 포털 사용](https://go.microsoft.com/fwlink/?linkid=859690)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e30e9-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="e30e9-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e30e9-126">Related topics</span></span>

[<span data-ttu-id="e30e9-127">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="e30e9-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="e30e9-128">Office 365 Advanced Threat Protection 방지</span><span class="sxs-lookup"><span data-stu-id="e30e9-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

