---
title: 스팸 방지 정책 구성
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
description: 기본 스팸 방지 정책 (연결 필터, 스팸 필터 및 아웃 바운드 스팸)을 통해 자동으로 활성화 된 회사 전체에서 수행 스팸 필터링 합니다. 관리자로 서 있습니다 수 보고 하 고 편집, 있지만 하지 삭제할 수, 기본 스팸 방지 정책은 가장 하 여 조직의 요구를 충족 하도록 맞게 조정 되도록 합니다. 더 큰 단위의 대 한 사용자 지정 정책을 만들 하 고 조직에 지정 된 사용자, 그룹 또는 도메인에 적용 합니다. 기본적으로 사용자 지정 정책을 기본 정책 보다 우선 하지만 정책의 우선순위를 변경할 수 있습니다.
ms.openlocfilehash: b96620705b0a62b8e8f7804f518651a10e0a63c1
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026255"
---
# <a name="configure-the-anti-spam-policies"></a><span data-ttu-id="4050a-106">스팸 방지 정책 구성</span><span class="sxs-lookup"><span data-stu-id="4050a-106">Configure the anti-spam policies</span></span>

<span data-ttu-id="4050a-p102">기본 스팸 방지 정책 (연결 필터, 스팸 필터 및 아웃 바운드 스팸)을 통해 자동으로 활성화 된 회사 전체에서 수행 스팸 필터링 합니다. 관리자로 서 있습니다 수 보고 하 고 편집, 있지만 하지 삭제할 수, 기본 스팸 방지 정책은 가장 하 여 조직의 요구를 충족 하도록 맞게 조정 되도록 합니다. 더 큰 단위의 대 한 사용자 지정 정책을 만들 하 고 조직에 지정 된 사용자, 그룹 또는 도메인에 적용 합니다. 기본적으로 사용자 지정 정책을 기본 정책 보다 우선 하지만 정책의 우선순위를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4050a-p102">Spam filtering is automatically enabled company-wide through the default anti-spam policies (connection filter, spam filter, and outbound spam). As an administrator, you can view and edit, but not delete, the default anti-spam policies so that they are tailored to best meet the needs of your organization. For greater granularity, you can also create custom policies and apply them to specified users, groups, or domains in your organization. By default, custom policies take precedence over the default policy, but you can change the priority of your policies.</span></span> 
  
<span data-ttu-id="4050a-111">스팸 방지 정책을 구성하는 방법에 대한 자세한 내용은 다음 항목을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="4050a-111">For more about configuring your anti-spam policies, see the following topics:</span></span>
  
[<span data-ttu-id="4050a-112">연결 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="4050a-112">Configure the connection filter policy</span></span>](configure-the-connection-filter-policy.md)
  
[<span data-ttu-id="4050a-113">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="4050a-113">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> <span data-ttu-id="4050a-p103">EOP 독립 실행형 고객의 경우 기본적으로 EOP 콘텐츠 필터는 스팸으로 검색된 메시지를 각 받는 사람의 정크 메일 폴더로 보냅니다. 그러나 온-프레미스 사서함에서 **정크 메일 폴더로 메시지 이동** 작업이 작동하도록 하려면 EOP에서 추가한 스팸 헤더를 검색하도록 온-프레미스 서버에서 Exchange 전송 규칙 두 개를 구성해야 합니다. 자세한 내용은 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4050a-p103">For EOP standalone customers: By default, the EOP content filters send spam-detected messages to each recipients' Junk Email folder. However, in order to ensure that the **Move message to Junk Email folder** action will work with on-premises mailboxes, you must configure two Exchange Transport rules on your on-premises servers to detect spam headers added by EOP. For details, see [Ensure that spam is routed to each user's Junk Email folder](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> 
  
[<span data-ttu-id="4050a-117">아웃 바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="4050a-117">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  

