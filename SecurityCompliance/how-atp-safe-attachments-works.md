---
title: Office 365 ATP 안전 첨부 파일의 작동 방식
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.date: 05/17/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: 안전한 첨부 파일 기능은 전자 메일 첨부 파일을 클릭 하 여 확인할 시간을 제공 합니다. 안전한 첨부 파일을 사용 하 여 사용자가 전자 메일로 보내거나 받는 악의적인 파일 로부터 조직을 보호 합니다.
ms.openlocfilehash: 99d31e327343971f6a7630e2a43ffd3044fbf976
ms.sourcegitcommit: 424a614141c1f19a1c84a67ec2d71dd3d7ef6694
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/30/2019
ms.locfileid: "34592271"
---
# <a name="how-ffice-365-atp-safe-attachments-works"></a><span data-ttu-id="051f1-104">Ffice> 365 ATP에서 안전한 첨부 파일의 작동 방식</span><span class="sxs-lookup"><span data-stu-id="051f1-104">How ffice 365 ATP Safe Attachments works</span></span>

## <a name="how-it-works"></a><span data-ttu-id="051f1-105">작업 방법</span><span class="sxs-lookup"><span data-stu-id="051f1-105">How it works</span></span>

<span data-ttu-id="051f1-106">ATP 안전한 첨부 파일 기능은 조직의 사용자에 대해 전자 메일 첨부 파일을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-106">The ATP Safe Attachments feature checks email attachments for people in your organization.</span></span> <span data-ttu-id="051f1-107">ATP 안전한 첨부 파일 정책이 적용 되 고 해당 정책에서 다루는 누군가가 Office 365의 전자 메일을 볼 때, 해당 전자 메일 첨부 파일을 확인 하 고 ATP 안전한 첨부 파일 정책에 따라 적절 한 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-107">When an ATP Safe Attachments policy is in place and someone covered by that policy views their email in Office 365, their email attachments are checked and appropriate actions are taken, based on your ATP Safe Attachments policies.</span></span> <span data-ttu-id="051f1-108">정책이 정의 된 방식에 따라 사용자가 악성 파일을 보낸 것을 알지 못하면 작업을 계속할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-108">Depending on how your policies are defined, people can continue working without ever knowing they were sent malicious files.</span></span>
  
<span data-ttu-id="051f1-109">다음은 직장의 ATP 안전 첨부 파일에 대 한 두 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-109">Here are two examples of ATP Safe Attachments at work.</span></span>
  
- <span data-ttu-id="051f1-110">**예 1: 전자 메일 첨부 파일** Lee에서 첨부 파일이 있는 전자 메일 메시지를 수신 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-110">**Example 1: Email attachment** Suppose that Lee receives an email message that has an attachment.</span></span> <span data-ttu-id="051f1-111">해당 첨부 파일이 안전한 지 아니면 실제로 Lee의 사용자 자격 증명을 도용 하도록 설계 된 맬웨어가 있는지를 Lee는 것은 분명 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-111">It is not obvious to Lee whether that attachment is safe or actually contains malware designed to steal Lee's user credentials.</span></span> <span data-ttu-id="051f1-112">Lee의 조직에서는 보안 관리자가 ATP 안전한 첨부 파일 정책을 며칠 전에 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-112">In Lee's organization, a security administrator defined an ATP Safe Attachments policy a few days ago.</span></span> <span data-ttu-id="051f1-113">ATP 안전한 첨부 파일 기능을 사용 하 여 Lee가 수신 되기 전에 전자 메일 첨부 파일을 가상 환경에서 열고 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-113">With the ATP Safe Attachments feature, the email attachment is opened and tested in a virtual environment before Lee receives it.</span></span> <span data-ttu-id="051f1-114">첨부 파일이 악성 인 것으로 확인 되 면 자동으로 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-114">If the attachment is determined to be malicious, it will be removed automatically.</span></span> <span data-ttu-id="051f1-115">안전 하지 않은 첨부 파일은 Lee 클릭 하면 예상 대로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-115">If the attachment is safe, it will open as expected when Lee clicks on it.</span></span>

- <span data-ttu-id="051f1-116">**예 2: SharePoint Online의 파일** Jean에서 파일을 받아 SharePoint Online의 라이브러리에 업로드 했다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-116">**Example 2: File in SharePoint Online** Suppose that Jean received a file and uploaded it into a library in SharePoint Online.</span></span> <span data-ttu-id="051f1-117">Jean는 파일에 대 한 링크를 나머지 팀과 공유 하 여 실제로 악성 프로그램 인지를 알지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-117">Jean shares the link to the file with the rest of the team, not knowing that the file is actually malicious.</span></span> <span data-ttu-id="051f1-118">다행 스럽게도 [SharePoint, OneDrive 및 Microsoft 팀](atp-for-spo-odb-and-teams.md) 은 악성 파일을 검색 하 고 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-118">Fortunately, [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) detects the malicious file and blocks it.</span></span> <span data-ttu-id="051f1-119">며칠 후에 Chris가 문서를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-119">A few days later, Chris goes to open the document.</span></span> <span data-ttu-id="051f1-120">Chris가 파일을 볼 수는 있지만, chris의 컴퓨터와 악의 있는 파일을 보호 하는 공유를 열거나 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-120">Although Chris can see the file is there, Chris cannot open or share it, which protects Chris's computer and others from the malicious file.</span></span>

<span data-ttu-id="051f1-121">ATP 안전한 첨부 파일 정책은 조직의 특정 사용자 또는 그룹이 나 전체 도메인에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-121">ATP Safe Attachments policies can be applied to specific people or groups in your organization, or to your entire domain.</span></span> <span data-ttu-id="051f1-122">또한 ATP 안전한 첨부 파일 정책은 실제 첨부 파일을 검색 하는 동안 자리 표시자 첨부 파일을 사용 하도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-122">In addition, ATP Safe Attachments policies can be configured to use placeholder attachments while actual attachments are being scanned.</span></span> <span data-ttu-id="051f1-123">자세한 내용은 **[Office 365에서 ATP 안전한 첨부 파일 정책 설정을](set-up-atp-safe-attachments-policies.md)** 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="051f1-123">To learn more, see **[Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md)**.</span></span>

> [!NOTE]
> <span data-ttu-id="051f1-124">ATP 안전한 첨부 파일 검사는 Office 365 데이터가 있는 동일한 지역에서 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="051f1-124">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides.</span></span> <span data-ttu-id="051f1-125">데이터 센터 지역에 대 한 자세한 내용은 [어디에 있습니까?](https://products.office.com/where-is-your-data-located?geo=All) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="051f1-125">For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 

