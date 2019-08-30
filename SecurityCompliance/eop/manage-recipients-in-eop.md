---
title: EOP에서 받는 사람 관리
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 2921f544-8257-4bae-8e3a-ce9250e9f162
description: Microsoft EOP(Exchange Online Protection)에서는 메일 받는 사람을 관리하는 다양한 방법이 제공됩니다. 관리자는 EAC (Exchange 관리 센터) 내에서 또는 원격 Windows PowerShell을 사용 하 여 특정 관리 작업을 수행 하 고 Microsoft 365 관리 센터에서 수행 된 기타 관리 작업을 확인할 수 있습니다.
ms.openlocfilehash: 6b56bcf725fe461c7e059658e7981f27bd4c07eb
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676578"
---
# <a name="manage-recipients-in-eop"></a><span data-ttu-id="fe27b-104">EOP에서 받는 사람 관리</span><span class="sxs-lookup"><span data-stu-id="fe27b-104">Manage recipients in EOP</span></span>

<span data-ttu-id="fe27b-105">Microsoft EOP(Exchange Online Protection)에서는 메일 받는 사람을 관리하는 다양한 방법이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe27b-105">Microsoft Exchange Online Protection (EOP) offers several ways to manage your mail recipients.</span></span> <span data-ttu-id="fe27b-106">관리자는 EAC (Exchange 관리 센터) 내에서 또는 원격 Windows PowerShell을 사용 하 여 특정 관리 작업을 수행 하 고 Microsoft 365 관리 센터에서 수행 된 기타 관리 작업을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe27b-106">As an administrator, you can perform certain management tasks within the Exchange admin center (EAC) or using remote Windows PowerShell, and verify other management tasks performed in the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="fe27b-107">EOP는 다음과 같은 유형의 받는 사람을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe27b-107">EOP supports the following types of recipients:</span></span>
  
- <span data-ttu-id="fe27b-108">**메일 사용자**: 메일 사용자는 EOP 관리 되는 도메인의 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="fe27b-108">**Mail Users**: Mail users are recipients in your EOP managed domains.</span></span> <span data-ttu-id="fe27b-109">이러한 받는 사람은 Office 365 조 직에 로그온 자격 증명을 갖고 있지만 받는 사람의 사서함이 클라우드 조직 외부에 있다는 것을 의미 하는 외부 전자 메일 주소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe27b-109">These recipients have logon credentials in your Office 365 organization, but they have external email addresses, meaning that their recipient mailboxes are located outside of your cloud organization.</span></span>

  <span data-ttu-id="fe27b-110">메일 사용자를 추가 하 여 메일을 받을 수 있으며 특정 사용자에 대 한 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe27b-110">You can add mail users so that they can receive mail and you can also create mail flow rules (also known as transport rules) for specific users.</span></span> <span data-ttu-id="fe27b-111">조직의 메일 사용자에 게 역할을 할당할 수도 있습니다. 관리 역할 그룹 권한을 가진 사용자는 EAC (Exchange 관리 센터)에 액세스 하 고 특정 관리 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe27b-111">You can also assign roles to mail users in your organization; users with management role group privileges can access the Exchange admin center (EAC) and perform certain management tasks.</span></span> <span data-ttu-id="fe27b-112">사용자 역할에 대 한 자세한 내용을 확인 하 고 EOP에서 사용자 역할을 할당 하는 방법에 대 한 자세한 내용은 [EOP에서 관리자 역할 그룹 권한 관리](manage-admin-role-group-permissions-in-eop.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fe27b-112">To learn more about user roles and how to assign user roles in EOP, see [Manage admin role group permissions in EOP](manage-admin-role-group-permissions-in-eop.md).</span></span>

  <span data-ttu-id="fe27b-113">EOP에서 메일 사용자를 관리하는 방법에 대한 자세한 내용은 [EOP에서 메일 사용자 관리](manage-mail-users-in-eop.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fe27b-113">For more information about managing mail users in EOP, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>

- <span data-ttu-id="fe27b-114">**그룹**: 메일 사용자를 메일 그룹 또는 보안 그룹으로 그룹화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe27b-114">**Groups**: Mail users can be grouped together into distribution groups or security groups.</span></span>

<span data-ttu-id="fe27b-115">EOP에서 그룹을 관리하는 방법에 대한 자세한 내용은 [EOP에서 그룹 관리](manage-groups-in-eop.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fe27b-115">For more information about managing groups in EOP, see [Manage groups in EOP](manage-groups-in-eop.md).</span></span>
