---
title: SharePoint, OneDrive 또는 Microsoft Teams에서 감지한 악성 파일에 대한 정보 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
ms.collection:
- M365-security-compliance
description: SharePoint, OneDrive 또는 팀에서 검색 된 악성 파일에 대 한 정보를 볼 수 있는 위치 및 해당 파일에 대해 작업을 수행 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 070640d9aa1d28cc1a49a9d8b88e5bf5780d3622
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077584"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="76405-103">SharePoint, OneDrive 또는 Microsoft Teams에서 감지한 악성 파일에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="76405-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="76405-104">[SharePoint, OneDrive 및 Microsoft 팀에서는 Office 365 ATP](atp-for-spo-odb-and-teams.md) 가 문서 라이브러리 및 팀 사이트의 악의적인 파일 로부터 조직을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-104">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites.</span></span> <span data-ttu-id="76405-105">악성 파일이 검색 되 면 해당 파일이 차단 되므로 조직의 보안 팀이 추가 작업을 수행할 때까지 아무도 해당 파일을 열거나 복사 하거나 이동 하거나 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76405-105">When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team.</span></span> <span data-ttu-id="76405-106">검색 된 파일에 대 한 정보 및 수행할 작업을 확인 하는 방법에 대 한 자세한 내용은이 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76405-106">Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="76405-107">이 문서에서 설명 하는 작업을 수행 하려면 [Office 365 보안 &amp; 및 준수 센터에 필요한 권한이](permissions-in-the-security-and-compliance-center.md)있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-107">In order to perform the tasks described in this article, you must have the necessary [permissions for the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="76405-108">검색 된 파일에 대 한 정보가 있는 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="76405-108">View reports with information about detected files</span></span>

<span data-ttu-id="76405-109">Office 365 ATP가 검색 한 파일에 대 한 상태 및 자세한 정보를 보려면 위협 방지 상태 보고서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76405-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat Protection Status report.</span></span>
  
1. <span data-ttu-id="76405-110">[Office 365 보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **위협 보호 상태**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-110">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
    
2. <span data-ttu-id="76405-111">보고서의 오른쪽 위 모서리에서 **정보 테이블 보기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="76405-112">보고서에서 검색 된 파일의 목록을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="76405-113">수행 된 작업, 파일 이름, 파일 경로 등 자세한 정보를 보려면 목록에서 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="76405-114">**고급 분석** 탭을 선택 하 여 관찰 된 동작 및 분석 세부 정보 등의 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="76405-115">격리에서 파일 보기 및 작업 수행</span><span class="sxs-lookup"><span data-stu-id="76405-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="76405-116">Office 365 보안 &amp; 및 준수 센터에서 **위협 관리** \> **검토** \> **격리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="76405-117">왼쪽 위 모서리에서 **전자 메일** 에서 **콘텐트로**필터를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="76405-118">파일의 URL을 포함 하 여 세부 정보를 보려면 목록에서 항목을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="76405-119">사용 가능한 작업을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="76405-120">파일 차단을 해제 하려면 **릴리스 &amp; 보고서** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="76405-121">Microsoft **에 보고서 보내기를** 선택 하 여 파일을 가양성으로 microsoft에 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="76405-122">파일 **다운로드** 를 선택 하 여 파일을 더 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="76405-123">**삭제** 를 선택 하 여 격리 된 항목 목록에서 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-123">Choose **Delete** to remove the file from the list of quarantined items.</span></span> <span data-ttu-id="76405-124">이 옵션을 선택 하는 경우 SharePoint Online, 비즈니스용 OneDrive 또는 Microsoft 팀의 각 라이브러리 에서도 해당 파일을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76405-124">If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams.</span></span> <span data-ttu-id="76405-125">이 옵션을 선택 해도 파일이 열리거나 공유 되지 않도록 차단 해제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76405-125">This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="76405-126">**닫기를** 선택 하 여 선택한 항목에 대 한 세부 정보를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="76405-126">Choose **Close** to close the details for a selected item.</span></span> 
  
  

