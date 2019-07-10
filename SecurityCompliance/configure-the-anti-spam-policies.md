---
title: 스팸 방지 정책 구성
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 6/9/2015
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
ms.collection:
- M365-security-compliance
description: 스팸 필터링은 기본 스팸 방지 정책 (연결 필터, 스팸 필터 및 아웃 바운드 스팸)을 통해 회사 차원에서 자동으로 사용 하도록 설정 됩니다. 관리자는 기본 스팸 방지 정책을 보고 편집하여 조직의 요구에 가장 잘 맞게 조정할 수 있지만 삭제할 수는 없습니다. 세분성을 높이기 위해 사용자 지정 정책을 만들어 조직의 지정 된 사용자, 그룹 또는 도메인에 적용할 수도 있습니다. 기본적으로 사용자 지정 정책은 기본 정책보다 우선하지만 정책의 우선 순위를 변경할 수 있습니다.
ms.openlocfilehash: f6690ddf0f50762aaa7b9ff61385c279f66716c8
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600114"
---
# <a name="configure-the-anti-spam-policies"></a><span data-ttu-id="34868-106">스팸 방지 정책 구성</span><span class="sxs-lookup"><span data-stu-id="34868-106">Configure the anti-spam policies</span></span>

<span data-ttu-id="34868-107">스팸 필터링은 기본 스팸 방지 정책 (연결 필터, 스팸 필터 및 아웃 바운드 스팸)을 통해 회사 차원에서 자동으로 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34868-107">Spam filtering is automatically enabled company-wide through the default anti-spam policies (connection filter, spam filter, and outbound spam).</span></span> <span data-ttu-id="34868-108">관리자는 기본 스팸 방지 정책을 보고 편집하여 조직의 요구에 가장 잘 맞게 조정할 수 있지만 삭제할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="34868-108">As an administrator, you can view and edit, but not delete, the default anti-spam policies so that they are tailored to best meet the needs of your organization.</span></span> <span data-ttu-id="34868-109">세분성을 높이기 위해 사용자 지정 정책을 만들어 조직의 지정 된 사용자, 그룹 또는 도메인에 적용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34868-109">For greater granularity, you can also create custom policies and apply them to specified users, groups, or domains in your organization.</span></span> <span data-ttu-id="34868-110">기본적으로 사용자 지정 정책은 기본 정책보다 우선하지만 정책의 우선 순위를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34868-110">By default, custom policies take precedence over the default policy, but you can change the priority of your policies.</span></span> 
  
<span data-ttu-id="34868-111">스팸 방지 정책을 구성하는 방법에 대한 자세한 내용은 다음 항목을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="34868-111">For more about configuring your anti-spam policies, see the following topics:</span></span>
  
[<span data-ttu-id="34868-112">연결 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="34868-112">Configure the connection filter policy</span></span>](configure-the-connection-filter-policy.md)
  
[<span data-ttu-id="34868-113">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="34868-113">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> <span data-ttu-id="34868-114">EOP 독립 실행형 고객의 경우 기본적으로 EOP 콘텐츠 필터는 스팸으로 검색된 메시지를 각 받는 사람의 정크 메일 폴더로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="34868-114">For EOP standalone customers: By default, the EOP content filters send spam-detected messages to each recipients' Junk Email folder.</span></span> <span data-ttu-id="34868-115">그러나 온-프레미스 사서함을 사용 하 여 **정크 메일 폴더로 메시지 이동** 작업을 수행 하려면 온-프레미스 서버에서 두 개의 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 구성 하 여 사용자가 추가한 스팸 헤더를 검색 해야 합니다. EOP.</span><span class="sxs-lookup"><span data-stu-id="34868-115">However, in order to ensure that the **Move message to Junk Email folder** action will work with on-premises mailboxes, you must configure two Exchange mail flow rules (also known as transport rules) on your on-premises servers to detect spam headers added by EOP.</span></span> <span data-ttu-id="34868-116">자세한 내용은 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="34868-116">For details, see [Ensure that spam is routed to each user's Junk Email folder](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> 
  
[<span data-ttu-id="34868-117">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="34868-117">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  

