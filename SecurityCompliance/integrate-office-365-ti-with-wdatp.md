---
title: Microsoft Defender Advanced Threat Protection을 사용 하 여 Office 365 Advanced Threat Protection 통합
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 01/22/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection:
- M365-security-compliance
description: Microsoft Defender Advanced Threat Protection과 Office 365 Advanced Threat Protection을 통합 하 여 보다 자세한 위협 관리 정보를 확인 합니다.
ms.openlocfilehash: 640c073e9ef5b32ffaa8d38a426d86b60d80d2aa
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599054"
---
# <a name="integrate-office-365-advanced-threat-protection-with-microsoft-defender-advanced-threat-protection"></a><span data-ttu-id="8ab7a-103">Microsoft Defender Advanced Threat Protection을 사용 하 여 Office 365 Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="8ab7a-103">Integrate Office 365 Advanced Threat Protection with Microsoft Defender Advanced Threat Protection</span></span>

<span data-ttu-id="8ab7a-104">조직의 보안 팀에 속한 경우에는 [Microsoft Defender Advanced Threat protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)과 [Office 365 Advanced threat protection](office-365-atp.md) 및 관련 조사 및 응답 기능을 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-104">If you are part of your organization's security team, you can integrate [Office 365 Advanced Threat Protection](office-365-atp.md) and related investigation and response features with [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection).</span></span> <span data-ttu-id="8ab7a-105">이를 통해 Office 365의 위협을 조사할 때 사용자의 컴퓨터가 위험에 처 했는지 여부를 빠르게 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-105">This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365.</span></span> <span data-ttu-id="8ab7a-106">예를 들어 통합이 설정 되 면 검색 된 전자 메일 메시지를 받는 사람이 사용 하는 컴퓨터 목록과 해당 컴퓨터가 Microsoft Defender Advanced Threat Protection에 갖는 최근 알림을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-106">For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Microsoft Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="8ab7a-107">다음 이미지에는 Microsoft Defender ATP 통합을 사용 하는 경우 표시 되는 **장치** 탭이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-107">The following image shows the **Devices** tab that you'll see when have Microsoft Defender ATP integration enabled:</span></span>
  
![Microsoft Defender ATP가 사용 하도록 설정 되 면 경고가 포함 된 컴퓨터 목록을 볼 수 있습니다.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="8ab7a-109">이 예에서는 전자 메일 메시지의 받는 사람에 게 4 개의 장치가 있고 하나에 경고가 있음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-109">In this example, you can see that the recipients of the email message have four devices and one has an alert.</span></span> <span data-ttu-id="8ab7a-110">장치에 대 한 링크를 클릭 하면 Microsoft Defender 보안 센터에서 해당 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-110">Clicking the link for a device opens its page in the Microsoft Defender Security Center.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="8ab7a-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8ab7a-111">Requirements</span></span>

- <span data-ttu-id="8ab7a-112">조직에 Office 365 ATP 계획 2 (또는 Office 365 E5)와 Microsoft Defender ATP가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-112">Your organization must have Office 365 ATP Plan 2 (or Office 365 E5) and Microsoft Defender ATP.</span></span>
    
- <span data-ttu-id="8ab7a-113">보안 및 [ &amp; 준수 센터](https://protection.office.com)에서 Office 365 전역 관리자 이거나 보안 관리자 역할 (예: 보안 관리자)을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-113">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="8ab7a-114">( [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)참조)</span><span class="sxs-lookup"><span data-stu-id="8ab7a-114">(See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="8ab7a-115">보안 & 준수 센터 및 Microsoft Defender 보안 센터에서 두 [탐색기 (또는 실시간 검색)](threat-explorer.md) 에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-115">You must have access to both [Explorer (or real-time detections)](threat-explorer.md) in the Security & Compliance Center and the Microsoft Defender Security Center.</span></span>
    
## <a name="to-integrate-office-365-atp-with-microsoft-defender-atp"></a><span data-ttu-id="8ab7a-116">Office 365 ATP를 Microsoft Defender ATP와 통합 하려면</span><span class="sxs-lookup"><span data-stu-id="8ab7a-116">To integrate Office 365 ATP with Microsoft Defender ATP</span></span>

<span data-ttu-id="8ab7a-117">Microsoft Defender ATP와 Office 365 ATP를 통합 하는 기능은 보안 & 준수 센터와 Microsoft Defender 보안 센터를 모두 사용 하 여 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-117">Integrating Office 365 ATP with Microsoft Defender ATP is set up by using both the Security & Compliance Center AND the Microsoft Defender Security Center.</span></span>
  
1. <span data-ttu-id="8ab7a-118">Office 365 전역 관리자 또는 보안 관리자 인 경우으로 이동 [https://protection.office.com](https://protection.office.com) 하 여 office 365에 대 한 회사 또는 학교 계정으로 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span>
    
2. <span data-ttu-id="8ab7a-119">**위협 관리** \> **탐색기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="8ab7a-120">![위협 관리 메뉴의 탐색기](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="8ab7a-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="8ab7a-121">화면의 오른쪽 위 모서리에서 **Wdatp 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="8ab7a-122">Windows Defender ATP 연결 대화 상자에서 Windows ATP에 연결을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Microsoft Defender ATP 연결](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="8ab7a-124">Microsoft Defender 보안 센터에서 연결을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab7a-124">Enable the connection in the Microsoft Defender Security Center.</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="8ab7a-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8ab7a-125">Related topics</span></span>

[<span data-ttu-id="8ab7a-126">Office 365 위협 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="8ab7a-126">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)
  
[<span data-ttu-id="8ab7a-127">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8ab7a-127">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

