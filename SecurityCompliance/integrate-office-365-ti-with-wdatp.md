---
title: Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection: M365-security-compliance
description: Windows Defender advanced threat protection을 사용 하 여 Office 365 advanced threat protection을 통합 하 여 보다 자세한 위협 관리 정보를 확인 합니다.
ms.openlocfilehash: ec7c7f565a4a316085b586168512699bb13cad47
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220928"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="5e3e8-103">Office 365 위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="5e3e8-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="5e3e8-p101">조직의 보안 팀에 속한 경우에는 Windows Defender advanced threat protection과 함께 Office 365 advanced threat protection 및 위협 인텔리전스 기능을 통합할 수 있습니다. 이를 통해 Office 365의 위협을 조사할 때 사용자의 컴퓨터가 위험에 처 했는지 여부를 빠르게 파악할 수 있습니다. 예를 들어 통합이 설정 되 면 검색 된 전자 메일 메시지를 받는 사람이 사용 하는 컴퓨터 목록과 해당 컴퓨터가 Windows Defender Advanced Threat Protection에 가지는 최근 알림을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="5e3e8-107">다음 이미지에는 Windows Defender Advanced Threat Protection 통합을 사용 하는 경우 표시 되는 **장치** 탭이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Windows Defender ATP가 사용 하도록 설정 되 면 경고가 포함 된 컴퓨터 목록을 볼 수 있습니다.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="5e3e8-p102">이 예에서는 전자 메일 메시지의 받는 사람에 게 4 개의 장치가 있고 하나에 경고가 있음을 확인할 수 있습니다. 장치에 대 한 링크를 클릭 하면 Windows Defender Advanced Threat Protection 포털에서 해당 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="5e3e8-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="5e3e8-111">Requirements</span></span>

- <span data-ttu-id="5e3e8-112">조직에 Office 365 위협 인텔리전스 및 Windows Defender ATP가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="5e3e8-p103">보안 및 [ &amp; 준수 센터](https://protection.office.com)에서 Office 365 전역 관리자 이거나 보안 관리자 역할 (예: 보안 관리자)을 할당 받아야 합니다. ( [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)참조)</span><span class="sxs-lookup"><span data-stu-id="5e3e8-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="5e3e8-115">Office 365 위협 인텔리전스 및 Windows Defender Advanced Threat Protection 포털에 모두 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="5e3e8-116">Windows Defender ATP에 Office 365 위협 인텔리전스를 통합 하려면</span><span class="sxs-lookup"><span data-stu-id="5e3e8-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="5e3e8-117">office 365과 windows defender advanced threat protection을 함께 사용 하는 것은 office 365 Security & 준수 센터와 Windows defender advanced threat protection 포털을 모두 통해 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="5e3e8-118">office 365 전역 관리자 또는 보안 관리자 인 경우으로 이동 [https://protection.office.com](https://protection.office.com) 하 여 office 365에 대 한 회사 또는 학교 계정으로 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="5e3e8-119">**위협 관리** \> **탐색기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="5e3e8-120">![위협 관리 메뉴의 탐색기](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="5e3e8-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="5e3e8-121">화면의 오른쪽 위 모서리에서 **wdatp 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="5e3e8-122">windows Defender ATP 연결 대화 상자에서 windows ATP에 연결을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Windows Defender ATP 연결](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="5e3e8-p104">Windows Defender Advanced Threat Protection에서 연결을 사용 하도록 설정 합니다. [Windows Defender Advanced Threat Protection 포털 사용을](https://go.microsoft.com/fwlink/?linkid=859690)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5e3e8-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="5e3e8-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5e3e8-126">Related topics</span></span>

[<span data-ttu-id="5e3e8-127">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="5e3e8-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="5e3e8-128">Office 365 Advanced Threat Protection 방지</span><span class="sxs-lookup"><span data-stu-id="5e3e8-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

