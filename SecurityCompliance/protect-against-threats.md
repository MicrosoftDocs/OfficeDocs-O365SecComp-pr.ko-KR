---
title: Office 365에서 위협 으로부터 보호
ms.author: tracyp
author: msfttracyp
manager: laurawi
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: 이 문서를 참조 하 여 위협 방지 기능을 지금 구성 합니다.
ms.openlocfilehash: 065071999130f209d63bcafc09ad72daceceac04
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261636"
---
# <a name="protect-against-threats-in-office-365"></a><span data-ttu-id="dfc37-103">Office 365에서 위협 으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="dfc37-103">Protect against threats in Office 365</span></span>

<span data-ttu-id="dfc37-104">Office 365에는 다양 한 위협 보호 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-104">Office 365 includes a variety of threat protection features.</span></span> <span data-ttu-id="dfc37-105">여기에는 조직에 대해 위협 방지 기능이 설정 되었는지 확인 하기 위한 검사 목록으로 사용할 수 있는 빠른 시작 가이드가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-105">Here's a quick-start guide you can use as a checklist to make sure your threat protection features are set up for your organization.</span></span> <span data-ttu-id="dfc37-106">Office 365의 위협 방지 기능을 처음 사용 하는 경우 나 시작할 위치를 모르는 경우에는 다음 지침을 출발점으로 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="dfc37-106">If you're new to threat protection features in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="dfc37-107">**초기 권장 설정은 각 정책 유형에 대해 포함 되지만 대부분의 옵션을 사용할 수 있으며, 특정 조직의 요구에 맞게 설정을 조정할 수**있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-107">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="dfc37-108">정책이 나 변경 내용이 데이터 센터를 통해 작동 하는 데 약 30 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-108">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfc37-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="dfc37-109">Requirements</span></span>

### <a name="licenses"></a><span data-ttu-id="dfc37-110">라이선스</span><span class="sxs-lookup"><span data-stu-id="dfc37-110">Licenses</span></span>

<span data-ttu-id="dfc37-111">위협 보호 기능은 모든 Office 365 구독에 포함 되어 있습니다. 그러나 일부 구독에는 Office 365 advanced Threat Protection의 경우와 같은 고급 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-111">Threat protection features are included in all Office 365 subscriptions; however, some subscriptions include more advanced features, such as those in Office 365 Advanced Threat Protection.</span></span> <span data-ttu-id="dfc37-112">이 문서에는 각 보호 영역에 대 한 구독 요구 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-112">In this article we include subscription requirements for each protection area.</span></span>

<span data-ttu-id="dfc37-113">위협 방지 기능 및 subsriptions에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="dfc37-113">To learn more about threat protection features and subsriptions, see the following resources:</span></span>
- [<span data-ttu-id="dfc37-114">Office 365 Advanced Threat Protection 서비스 설명</span><span class="sxs-lookup"><span data-stu-id="dfc37-114">Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)
- [<span data-ttu-id="dfc37-115">Exchange Online Protection 서비스 설명</span><span class="sxs-lookup"><span data-stu-id="dfc37-115">Exchange Online Protection Service Description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-protection-service-description/exchange-online-protection-service-description)
- [<span data-ttu-id="dfc37-116">Office 365 보안 및 준수 센터</span><span class="sxs-lookup"><span data-stu-id="dfc37-116">Office 365 Security & Compliance Center</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)

### <a name="roles-and-permissions"></a><span data-ttu-id="dfc37-117">역할 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="dfc37-117">Roles and permissions</span></span>

<span data-ttu-id="dfc37-118">[보안 & 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)에서 정책을 구성 하려면 적절 한 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-118">You must be assigned an appropriate role to configure policies in the [Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span> <span data-ttu-id="dfc37-119">다음 표에는 몇 가지 예가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-119">The following table includes some examples:</span></span> 

|<span data-ttu-id="dfc37-120">역할 또는 역할 그룹</span><span class="sxs-lookup"><span data-stu-id="dfc37-120">Role or role group</span></span>  |<span data-ttu-id="dfc37-121">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="dfc37-121">Where to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="dfc37-122">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="dfc37-122">Office 365 Global Administrator</span></span> |[<span data-ttu-id="dfc37-123">Office 365 관리자 역할 정보</span><span class="sxs-lookup"><span data-stu-id="dfc37-123">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|<span data-ttu-id="dfc37-124">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="dfc37-124">Security Administrator</span></span> |[<span data-ttu-id="dfc37-125">Azure Active Directory의 관리자 역할 권한</span><span class="sxs-lookup"><span data-stu-id="dfc37-125">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|<span data-ttu-id="dfc37-126">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="dfc37-126">Exchange Online Organization Management</span></span> |[<span data-ttu-id="dfc37-127">Exchange Online의 사용 권한</span><span class="sxs-lookup"><span data-stu-id="dfc37-127">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="dfc37-128">한</span><span class="sxs-lookup"><span data-stu-id="dfc37-128">and</span></span><br> [<span data-ttu-id="dfc37-129">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="dfc37-129">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

<span data-ttu-id="dfc37-130">자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfc37-130">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="part-1---anti-malware"></a><span data-ttu-id="dfc37-131">1 부-맬웨어 방지</span><span class="sxs-lookup"><span data-stu-id="dfc37-131">Part 1 - Anti-malware</span></span>

<span data-ttu-id="dfc37-132">[맬웨어 방지 보호](anti-malware-protection.md) 는 EOP ( [Exchange Online protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) )를 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-132">[Anti-malware protection](anti-malware-protection.md) is available in subscriptions that include [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span></span> 

1. <span data-ttu-id="dfc37-133">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **맬웨어 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-133">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>

2. <span data-ttu-id="dfc37-134">**기본** 정책을 두 번 클릭 한 다음 **설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-134">Double-click the **Default** policy, and then choose **settings**.</span></span>

3. <span data-ttu-id="dfc37-135">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-135">Specify the following settings:</span></span>
    
    - <span data-ttu-id="dfc37-136">**맬웨어 검색 응답** 섹션에서 기본 설정인 **아니요**를 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-136">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>
   
    - <span data-ttu-id="dfc37-137">**일반 첨부 파일 형식 필터** 섹션에서 **설정**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-137">In the **Common Attachment Types Filter** section, choose **On**.</span></span>

4. <span data-ttu-id="dfc37-138">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-138">Click **Save**.</span></span>

<span data-ttu-id="dfc37-139">맬웨어 방지 정책 옵션에 대 한 자세한 내용은 [맬웨어 방지 정책 구성을](configure-anti-malware-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="dfc37-139">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---zero-day-protection"></a><span data-ttu-id="dfc37-140">2 부-0 일 보호</span><span class="sxs-lookup"><span data-stu-id="dfc37-140">Part 2 - Zero-day protection</span></span>

<span data-ttu-id="dfc37-141">제로 일 보호는 [Office 365 atp (Advanced Threat protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) )를 포함 하는 구독에서 사용할 수 있으며 [atp 안전한 첨부 파일](atp-safe-attachments.md) 및 [atp 안전한 링크](atp-safe-links.md) 정책을 통해 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-141">Zero-day protection is available in subscriptions that include [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), and is set up through [ATP Safe Attachments](atp-safe-attachments.md) and [ATP Safe Links](atp-safe-links.md) policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="dfc37-142">ATP 안전한 첨부 파일 정책</span><span class="sxs-lookup"><span data-stu-id="dfc37-142">ATP Safe Attachments policies</span></span>

<span data-ttu-id="dfc37-143">[atp 안전한 첨부 파일](atp-safe-attachments.md)을 설정 하려면 atp 안전 첨부 파일 정책을 하나 이상 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-143">To set up [ATP Safe Attachments](atp-safe-attachments.md), you must define at least one ATP Safe Attachments policy.</span></span> 

1. <span data-ttu-id="dfc37-144">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 안전한 첨부 파일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-144">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>

2. <span data-ttu-id="dfc37-145">**SharePoint, OneDrive 및 Microsoft 팀에 대 한 ATP 설정**옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-145">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

3. <span data-ttu-id="dfc37-146">**전자 메일 첨부 파일 보호** 섹션에서 더하기 기호 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-146">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>

4. <span data-ttu-id="dfc37-147">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-147">Specify the following settings:</span></span>

    - <span data-ttu-id="dfc37-148">**이름** 상자에를 입력 `Block malware`합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-148">In the **Name** box, type `Block malware`.</span></span>

    - <span data-ttu-id="dfc37-149">응답 섹션에서 **차단을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-149">In the response section, choose **Block**.</span></span>

    - <span data-ttu-id="dfc37-150">**첨부 파일 리디렉션** 섹션에서 **리디렉션 사용**옵션을 선택 하 고 조직의 보안 관리자 또는 검색 된 파일을 검토할 운영자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-150">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>

    - <span data-ttu-id="dfc37-151">**적용 대상** 섹션에서 **받는 사람 도메인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-151">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="dfc37-152">그런 다음 도메인을 선택 하 고 **추가**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-152">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

5. <span data-ttu-id="dfc37-153">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-153">Click **Save**.</span></span>

6. <span data-ttu-id="dfc37-154">(**권장 추가 단계**) 전역 관리자 또는 SharePoint Online 관리자는 Office 365 환경에 대해 **DisallowInfectedFileDownload** 매개 변수를 *true* 로 설정 하 여 **[set-spotenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-154">(**Recommended additional step**) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="dfc37-155">따라서 사용자가 악성 파일로 검색 된 파일을 열거나 이동 하거나 복사 하거나 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-155">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="dfc37-156">자세한 내용은 다음을 참조하세요:</span><span class="sxs-lookup"><span data-stu-id="dfc37-156">To learn more, see:</span></span> 
- [<span data-ttu-id="dfc37-157">Office 365 ATP 안전한 첨부 파일 정책 설정</span><span class="sxs-lookup"><span data-stu-id="dfc37-157">Set up Office 365 ATP Safe Attachments policies</span></span>](set-up-atp-safe-attachments-policies.md)
- [<span data-ttu-id="dfc37-158">SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행</span><span class="sxs-lookup"><span data-stu-id="dfc37-158">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)

### <a name="atp-safe-links-policies"></a><span data-ttu-id="dfc37-159">ATP 안전한 링크 정책</span><span class="sxs-lookup"><span data-stu-id="dfc37-159">ATP Safe Links policies</span></span>

<span data-ttu-id="dfc37-160">[ATP 안전한 링크](atp-safe-links.md)를 설정 하려면 기본 정책을 검토 및 편집 하 고 특정 사용자에 대 한 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-160">To set up [ATP Safe Links](atp-safe-links.md), review and edit your default policy, and add a policy for specific users.</span></span>

1. <span data-ttu-id="dfc37-161">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 안전한 링크**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-161">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>

2. <span data-ttu-id="dfc37-162">**기본** 정책을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-162">Double-click the **Default** policy.</span></span>

3. <span data-ttu-id="dfc37-163">다음 **의 안전한 링크 사용** 섹션에서 **office 365 ProPlus, iOS 및 Android 용 office**를 차례로 선택 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-163">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>

4. <span data-ttu-id="dfc37-164">**특정 받는 사람에 게 적용 되는 정책** 섹션에서 더하기 기호 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-164">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>

5. <span data-ttu-id="dfc37-165">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-165">Specify the following settings:</span></span>

    - <span data-ttu-id="dfc37-166">**이름** 상자에 이름을 입력 `Safe Links`합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-166">In the **Name** box, type a name, such as `Safe Links`.</span></span>

    - <span data-ttu-id="dfc37-167">**작업 선택** 섹션에서 **설정**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-167">In the **Select the action** section, choose **On**.</span></span>

    - <span data-ttu-id="dfc37-168">다음 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-168">Select these options:</span></span>

        - <span data-ttu-id="dfc37-169">**다운로드 가능한 콘텐츠를 검색 하기 위해 안전한 첨부 파일 사용**</span><span class="sxs-lookup"><span data-stu-id="dfc37-169">**Use safe attachments to scan downloadable content**</span></span> 

        - <span data-ttu-id="dfc37-170">**조직 내에서 전송 된 전자 메일 메시지에 안전한 링크 적용**</span><span class="sxs-lookup"><span data-stu-id="dfc37-170">**Apply safe links to email messages sent within the organization**</span></span>

        - <span data-ttu-id="dfc37-171">**사용자가 원본 URL에 대 한 안전한 링크를 클릭 하는 것을 허용 하지 않음**</span><span class="sxs-lookup"><span data-stu-id="dfc37-171">**Do not let users click through safe links to original URL**</span></span>

    - <span data-ttu-id="dfc37-172">**적용 대상** 섹션에서 **받는 사람 도메인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-172">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="dfc37-173">그런 다음 도메인을 선택 하 고 **추가**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-173">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

6. <span data-ttu-id="dfc37-174">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-174">Click **Save**.</span></span>

<span data-ttu-id="dfc37-175">자세한 내용은 [Office 365 ATP 안전한 링크 정책 설정을](set-up-atp-safe-links-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="dfc37-175">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing"></a><span data-ttu-id="dfc37-176">3 부-피싱 방지</span><span class="sxs-lookup"><span data-stu-id="dfc37-176">Part 3 - Anti-phishing</span></span> 

<span data-ttu-id="dfc37-177">[피싱 방지 보호](anti-phishing-protection.md) 기능은 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)을 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-177">[Anti-phishing protection](anti-phishing-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="dfc37-178">고급 피싱 방지 보호는 [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-178">Advanced anti-phishing protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> <span data-ttu-id="dfc37-179">다음 절차에서는 ATP 피싱 방지 정책을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-179">The following procedure describes how to configure an ATP anti-phishing policy.</span></span> <span data-ttu-id="dfc37-180">이 단계는 피싱 방지 정책 (ATP 없이)을 구성 하는 경우에도 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-180">The steps are similar for configuring an anti-phishing policy (without ATP).</span></span>

1. <span data-ttu-id="dfc37-181">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 피싱 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-181">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="dfc37-182">**기본 정책을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-182">Click **Default policy**.</span></span>

3. <span data-ttu-id="dfc37-183">**가장** 섹션에서 **편집**을 클릭 하 고 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-183">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>

    -  <span data-ttu-id="dfc37-184">**보호할 사용자 추가** 탭에서 보호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-184">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="dfc37-185">그런 다음 조직의 보드 구성원, CEO, CFO 및 기타 선임 리더와 같은 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-185">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="dfc37-186">(개별 전자 메일 주소를 입력 하거나를 클릭 하 여 목록을 표시할 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="dfc37-186">(You can type an individual email address, or click to display a list.)</span></span>

    - <span data-ttu-id="dfc37-187">**보호할 도메인 추가** 탭에서 **자신이 소유한 도메인을 자동으로 포함**을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-187">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="dfc37-188">사용자 지정 도메인이 있는 경우 해당 도메인도 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-188">If you have custom domains, add those as well.</span></span>

    - <span data-ttu-id="dfc37-189">**작업** 탭에서 가장 된 사용자 및 가장 한 도메인에 대해 **받는 사람의 정크 메일 폴더로 메시지 이동을** 선택 하 고 보안 팁을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-189">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>

    - <span data-ttu-id="dfc37-190">**사서함 인텔리전스** 탭에서 사서함 인텔리전스가 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-190">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>

    - <span data-ttu-id="dfc37-191">**설정 검토** 탭에서 설정을 검토 한 후 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-191">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>

4. <span data-ttu-id="dfc37-192">**스푸핑** 섹션에서 **편집**을 클릭 하 고 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-192">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="dfc37-193">**스푸핑 필터 설정** 탭에서 스푸핑 방지 보호가 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-193">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>

    - <span data-ttu-id="dfc37-194">**작업** 탭에서 받는 사람의 정크 메일 폴더로 메시지 이동을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-194">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>

    - <span data-ttu-id="dfc37-195">**설정 검토** 탭에서 설정을 검토 한 후 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-195">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="dfc37-196">변경 하지 않은 경우 **취소**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-196">(If you didn't make any changes, click **Cancel**.)</span></span>

5. <span data-ttu-id="dfc37-197">기본 정책 설정 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-197">Close the default policy settings page.</span></span>

<span data-ttu-id="dfc37-198">피싱 방지 정책 옵션에 대 한 자세한 내용은 [피싱 방지 정책 설정을](set-up-anti-phishing-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="dfc37-198">To learn more about your anti-phishing policy options, see [Set up anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam"></a><span data-ttu-id="dfc37-199">4 부-스팸 방지</span><span class="sxs-lookup"><span data-stu-id="dfc37-199">Part 4 - Anti-spam</span></span>

<span data-ttu-id="dfc37-200">[스팸 방지 보호](anti-spam-protection.md) 기능은 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)을 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-200">[Anti-spam protection](anti-spam-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span>

1. <span data-ttu-id="dfc37-201">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **스팸 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-201">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>

2. <span data-ttu-id="dfc37-202">**사용자 지정** 탭에서 **사용자 지정 설정을** 켭니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-202">On the **Custom** tab, turn **Custom settings** on.</span></span>

3. <span data-ttu-id="dfc37-203">**기본 스팸 필터 정책을**확장 하 고 **정책 편집**을 클릭 한 후 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-203">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>

    - <span data-ttu-id="dfc37-204">**스팸 및 대량 작업** 섹션에서 임계값을 5 또는 6으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-204">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>

    - <span data-ttu-id="dfc37-205">허용 **목록** 섹션에서 허용 되는 보낸 사람 및 도메인을 검토 하 고 필요에 따라 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-205">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>

4. <span data-ttu-id="dfc37-206">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-206">Click **Save**.</span></span>

<span data-ttu-id="dfc37-207">스팸 방지 정책 옵션에 대 한 자세한 내용은 [스팸 방지 정책 구성을](configure-the-anti-spam-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfc37-207">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---service-wide-settings"></a><span data-ttu-id="dfc37-208">5 부-서비스 수준 설정</span><span class="sxs-lookup"><span data-stu-id="dfc37-208">Part 5 - Service-wide settings</span></span>

### <a name="zero-hour-auto-purge"></a><span data-ttu-id="dfc37-209">제로 시간 자동 삭제</span><span class="sxs-lookup"><span data-stu-id="dfc37-209">Zero-hour auto purge</span></span>

<span data-ttu-id="dfc37-210">[제로 시간 자동 삭제](zero-hour-auto-purge.md) (ZAP)은 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)이 포함 된 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-210">[Zero-hour auto purge](zero-hour-auto-purge.md) (ZAP) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="dfc37-211">이 보호 기능은 기본적으로 설정 되어 있습니다. 그러나 보호 기능을 적용 하려면 다음 조건을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-211">This protection is turned on by default; however, the following conditions must be met for protection to be in effect:</span></span>

- <span data-ttu-id="dfc37-212">스팸 [방지 정책](anti-spam-protection.md)에서 **정크 메일 폴더로 메시지를 이동** 하도록 스팸 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-212">Spam actions are set to **Move message to Junk Email folder** in [anti-spam policies](anti-spam-protection.md).</span></span>

- <span data-ttu-id="dfc37-213">사용자가 기본 [정크 메일 설정을](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)유지 했으며 정크 메일 보호를 해제 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-213">Users have kept their default [junk email settings](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md), and have not turned off junk email protection.</span></span>

<span data-ttu-id="dfc37-214">자세한 내용은 스팸 및 맬웨어를 방지 하는 [0 시간 자동 삭제](zero-hour-auto-purge.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfc37-214">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging"></a><span data-ttu-id="dfc37-215">감사 로깅</span><span class="sxs-lookup"><span data-stu-id="dfc37-215">Audit logging</span></span>

<span data-ttu-id="dfc37-216">감사 로깅은 [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)이 포함 된 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-216">Audit logging is available in subscriptions that include [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span></span> <span data-ttu-id="dfc37-217">[보안 대시보드](security-dashboard.md), [전자 메일 보안 보고서](view-email-security-reports.md)및 [탐색기](use-explorer-in-security-and-compliance.md)와 같은 위협 보호 보고서의 데이터를 보려면 조직에 대해 감사 로깅을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc37-217">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md), [email security reports](view-email-security-reports.md), and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span> <span data-ttu-id="dfc37-218">자세한 내용은 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfc37-218">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="dfc37-219">설치 후 작업</span><span class="sxs-lookup"><span data-stu-id="dfc37-219">Post-setup tasks</span></span>

### <a name="watch-for-new-features-and-service-updates"></a><span data-ttu-id="dfc37-220">새로운 기능 및 서비스 업데이트 조사</span><span class="sxs-lookup"><span data-stu-id="dfc37-220">Watch for new features and service updates</span></span>

- [<span data-ttu-id="dfc37-221">표준 또는 대상 지정 된 릴리스 옵션 설정</span><span class="sxs-lookup"><span data-stu-id="dfc37-221">Set up the Standard or Targeted release options</span></span>](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)

- [<span data-ttu-id="dfc37-222">메시지 센터로 이동 하 여 기능 알림 보기</span><span class="sxs-lookup"><span data-stu-id="dfc37-222">Go to your Message center to view feature announcements</span></span>](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide) 

- [<span data-ttu-id="dfc37-223">Microsoft 365 로드맵를 방문 하 여 새 기능의 상태 확인</span><span class="sxs-lookup"><span data-stu-id="dfc37-223">Visit the Microsoft 365 Roadmap to see status of new features</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [<span data-ttu-id="dfc37-224">Office 365 서비스 설명 검토</span><span class="sxs-lookup"><span data-stu-id="dfc37-224">Review the Office 365 Service Descriptions</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)

### <a name="see-how-threat-protection-features-are-working-for-your-organization"></a><span data-ttu-id="dfc37-225">조직에 대 한 위협 보호 기능 작동 방식 확인</span><span class="sxs-lookup"><span data-stu-id="dfc37-225">See how threat protection features are working for your organization</span></span>

- [<span data-ttu-id="dfc37-226">보안 대시보드 방문</span><span class="sxs-lookup"><span data-stu-id="dfc37-226">Visit your security dashboard</span></span>](security-dashboard.md)

- <span data-ttu-id="dfc37-227">[탐색기](use-explorer-in-security-and-compliance.md) 를 포함 하 여 [Office 365 ATP에 대 한 보고서 보기](view-reports-for-atp.md)</span><span class="sxs-lookup"><span data-stu-id="dfc37-227">[View the reports for Office 365 ATP](view-reports-for-atp.md), including [Explorer](use-explorer-in-security-and-compliance.md)</span></span>

- [<span data-ttu-id="dfc37-228">전자 메일 보안 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="dfc37-228">View your email security reports</span></span>](view-email-security-reports.md)

### <a name="periodically-review-and-revise-your-threat-protection-policies"></a><span data-ttu-id="dfc37-229">위협 보호 정책 주기적으로 검토 및 수정</span><span class="sxs-lookup"><span data-stu-id="dfc37-229">Periodically review and revise your threat protection policies</span></span>

- [<span data-ttu-id="dfc37-230">보안 점수 검토</span><span class="sxs-lookup"><span data-stu-id="dfc37-230">Review your Secure Score</span></span>](microsoft-secure-score.md)

- [<span data-ttu-id="dfc37-231">보안 &amp; 및 준수 센터에서 smart reports 및 insights 사용</span><span class="sxs-lookup"><span data-stu-id="dfc37-231">Use your smart reports and insights in the Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md) 

- [<span data-ttu-id="dfc37-232">Office 365 위협 조사 및 응답 기능을 통해 사용자를 안전 하 게 유지</span><span class="sxs-lookup"><span data-stu-id="dfc37-232">Keep users safe with Office 365 threat investigation and response features</span></span>](keep-users-safe-with-office-365-ti.md) 
 