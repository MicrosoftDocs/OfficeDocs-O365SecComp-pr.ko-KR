---
title: SharePoint, OneDrive, 또는 팀이 Microsoft에서 감지 된 악의적인 파일에 대 한 정보 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: SharePoint, OneDrive, 또는 팀에서 감지 된 악의적인 파일에 대 한 정보를 보려면 이동할 위치를 하 고 해당 파일에서 작업을 수행 하는 방법에 알아봅니다.
ms.openlocfilehash: ba1dc3551e66800213a9cb988ebe9fc5e03e31f2
ms.sourcegitcommit: 147768bbe44c8c98c02fa29ae9d882cee4ec2d6b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "26238510"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="1f569-103">SharePoint, OneDrive, 또는 팀이 Microsoft에서 감지 된 악의적인 파일에 대 한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="1f569-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="1f569-p101">문서 라이브러리 및 팀 사이트의 악의적인 파일을 통해 조직을 보호 하는 [SharePoint, OneDrive 및 팀이 Microsoft office 365 ATP](atp-for-spo-odb-and-teams.md) 입니다. 악의적인 파일 감지 되 면 해당 파일 열기, 복사, 이동 또는 조직의 보안 팀에 의해 추가 조치가 때까지 공유할 수 있는 아무도 있도록 차단 됩니다. 검색 된 파일에 대 한 정보를 확인 하는 방법 및 수행할 동작을 자세히 알아보려면이 문서를 읽어보십시오.</span><span class="sxs-lookup"><span data-stu-id="1f569-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="1f569-107">이 문서에서 설명 하는 작업을 수행 하기 위해 필요한 있어야 [Office 365 보안에 할당 된 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-107">In order to perform the tasks described in this article, you must have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="1f569-108">검색 된 파일에 대 한 정보가 포함 된 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="1f569-108">View reports with information about detected files</span></span>

<span data-ttu-id="1f569-109">상태 및 Office 365 ATP 하 여 검색 된 파일에 대 한 자세한 정보를 보려면 위협 보호 상태 보고서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat Protection Status report.</span></span>
  
1. <span data-ttu-id="1f569-110">Office 365 보안에서 &amp; 준수 센터 **보고서** 선택 \> **대시보드** \> **위협 보호 상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-110">In the Office 365 Security &amp; Compliance Center, choose **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
    
2. <span data-ttu-id="1f569-111">다음은 보고서의 오른쪽 위 모서리에서 **보기 세부 정보 테이블**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="1f569-112">다음은 보고서에서 검색 된 파일의 목록을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="1f569-113">자세한 내용은 다음을 수행 하는 작업을 포함 하 여, 파일 이름, 파일 경로 등을 보려면 목록에서 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="1f569-114">같은 관찰 된 동작 및 분석 세부 정보를 보려면 **고급 분석** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="1f569-115">격리에서 파일에 대해 조치를 취할 및 보기</span><span class="sxs-lookup"><span data-stu-id="1f569-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="1f569-116">Office 365 보안에서 &amp; 준수 센터 **위협 관리** 를 선택 \> **검토** \> **격리**합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="1f569-117">왼쪽된 위 모서리에서 필터 **전자 메일** 에서 **콘텐츠**를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="1f569-118">파일의 URL을 포함 하 여 자세한 정보를 보려면 목록에서 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="1f569-119">사용 가능한 동작을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="1f569-120">선택 **릴리스 &amp; 보고서** 파일 차단을 해제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="1f569-121">파일을 Microsoft에 가양성으로 보고를 **Microsoft에 보고서 보내기** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="1f569-122">**파일을 다운로드** 하 여 파일을 추가 조사를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="1f569-p102">격리 된 항목의 목록에서 파일을 제거 하려면 **삭제** 를 선택 합니다. 이 옵션을 선택 하는 경우 비즈니스, 또는 Microsoft 팀의 SharePoint Online, OneDrive에서 해당 라이브러리에서 파일을도 삭제 해야 있습니다. 이 옵션 못 파일 차단을 해제 하지 열거나 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="1f569-126">선택한 항목에 대 한 세부 정보를 닫으려면 **닫기** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f569-126">Choose **Close** to close the details for a selected item.</span></span> 
  
  

