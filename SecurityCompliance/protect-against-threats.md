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
description: 이 문서를 참조 하 여 위협 방지 기능을 즉시 구성 하는 방법을 설명 합니다.
ms.openlocfilehash: c651c13d5aacf1a7f95a93cacf5030e8ade4b8fd
ms.sourcegitcommit: 895f67531f2b4afe46c7487ca5b44555ca791bae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/12/2019
ms.locfileid: "31836832"
---
# <a name="protect-against-threats-in-office-365"></a><span data-ttu-id="a6a60-103">Office 365에서 위협 으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="a6a60-103">Protect against threats in Office 365</span></span>

<span data-ttu-id="a6a60-104">Office 365에는 다양 한 위협 보호 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-104">Office 365 includes a variety of threat protection features.</span></span> <span data-ttu-id="a6a60-105">여기에는 조직에 대해 위협 방지 기능이 설정 되었는지 확인 하기 위한 검사 목록으로 사용할 수 있는 빠른 시작 가이드가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-105">Here's a quick-start guide you can use as a checklist to make sure your threat protection features are set up for your organization.</span></span> <span data-ttu-id="a6a60-106">Office 365의 위협 방지 기능을 처음 사용 하는 경우 나 시작할 위치를 모르는 경우에는 다음 지침을 출발점으로 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="a6a60-106">If you're new to threat protection features in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="a6a60-107">**초기 권장 설정은 각 정책 유형에 대해 포함 되지만 대부분의 옵션을 사용할 수 있으며, 특정 조직의 요구에 맞게 설정을 조정할 수**있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-107">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="a6a60-108">정책이 나 변경 내용이 데이터 센터를 통해 작동 하는 데 약 30 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-108">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a6a60-109">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="a6a60-109">Prerequisites</span></span>

<span data-ttu-id="a6a60-110">[보안 & 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)에서 정책을 구성 하려면 적절 한 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-110">You must be assigned an appropriate role to configure policies in the [Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span> <span data-ttu-id="a6a60-111">다음 표에는 몇 가지 예가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-111">The following table includes some examples:</span></span> 

|<span data-ttu-id="a6a60-112">역할 또는 역할 그룹</span><span class="sxs-lookup"><span data-stu-id="a6a60-112">Role or role group</span></span>  |<span data-ttu-id="a6a60-113">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="a6a60-113">Where to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="a6a60-114">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="a6a60-114">Office 365 Global Administrator</span></span> |[<span data-ttu-id="a6a60-115">Office 365 관리자 역할 정보</span><span class="sxs-lookup"><span data-stu-id="a6a60-115">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|<span data-ttu-id="a6a60-116">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="a6a60-116">Security Administrator</span></span> |[<span data-ttu-id="a6a60-117">Azure Active Directory의 관리자 역할 권한</span><span class="sxs-lookup"><span data-stu-id="a6a60-117">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|<span data-ttu-id="a6a60-118">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="a6a60-118">Exchange Online Organization Management</span></span> |[<span data-ttu-id="a6a60-119">Exchange Online의 사용 권한</span><span class="sxs-lookup"><span data-stu-id="a6a60-119">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="a6a60-120">한</span><span class="sxs-lookup"><span data-stu-id="a6a60-120">and</span></span><br> [<span data-ttu-id="a6a60-121">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6a60-121">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

<span data-ttu-id="a6a60-122">자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6a60-122">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="part-1---anti-malware"></a><span data-ttu-id="a6a60-123">1 부-맬웨어 방지</span><span class="sxs-lookup"><span data-stu-id="a6a60-123">Part 1 - Anti-malware</span></span>

<span data-ttu-id="a6a60-124">맬웨어 방지 보호는 EOP ( [Exchange Online protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) )를 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-124">Anti-malware protection is available in subscriptions that include [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span></span> 

1. <span data-ttu-id="a6a60-125">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **맬웨어 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-125">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>
2. <span data-ttu-id="a6a60-126">**기본** 정책을 두 번 클릭 한 다음 **설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-126">Double-click the **Default** policy, and then choose **settings**.</span></span>
3. <span data-ttu-id="a6a60-127">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-127">Specify the following settings:</span></span>
    - <span data-ttu-id="a6a60-128">**맬웨어 검색 응답** 섹션에서 기본 설정인 **아니요**를 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-128">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>
    - <span data-ttu-id="a6a60-129">**일반 첨부 파일 형식 필터** 섹션에서 **설정**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-129">In the **Common Attachment Types Filter** section, choose **On**.</span></span>
4. <span data-ttu-id="a6a60-130">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-130">Click **Save**.</span></span>

<span data-ttu-id="a6a60-131">맬웨어 방지 정책 옵션에 대 한 자세한 내용은 [맬웨어 방지 정책 구성을](configure-anti-malware-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a6a60-131">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---zero-day-protection"></a><span data-ttu-id="a6a60-132">2 부-0 일 보호</span><span class="sxs-lookup"><span data-stu-id="a6a60-132">Part 2 - Zero-day protection</span></span>

<span data-ttu-id="a6a60-133">제로 일 보호는 [Office 365 atp (Advanced Threat protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) )를 포함 하는 구독에서 사용할 수 있으며 [atp 안전한 링크](atp-safe-links.md) 및 [atp 안전한 첨부 파일](atp-safe-attachments.md) 정책을 통해 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-133">Zero-day protection is available in subscriptions that include [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), and is set up through [ATP Safe Links](atp-safe-links.md) and [ATP Safe Attachments](atp-safe-attachments.md) policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="a6a60-134">ATP 안전한 첨부 파일 정책</span><span class="sxs-lookup"><span data-stu-id="a6a60-134">ATP Safe Attachments policies</span></span>

1. <span data-ttu-id="a6a60-135">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 안전한 첨부 파일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-135">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>
2. <span data-ttu-id="a6a60-136">**SharePoint, OneDrive 및 Microsoft 팀에 대 한 ATP 설정**옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-136">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>
3. <span data-ttu-id="a6a60-137">**전자 메일 첨부 파일 보호** 섹션에서 더하기 기호 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-137">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>
4. <span data-ttu-id="a6a60-138">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-138">Specify the following settings:</span></span>
    - <span data-ttu-id="a6a60-139">**이름** 상자에를 입력 `Block malware`합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-139">In the **Name** box, type `Block malware`.</span></span>
    - <span data-ttu-id="a6a60-140">응답 섹션에서 **차단을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-140">In the response section, choose **Block**.</span></span>
    - <span data-ttu-id="a6a60-141">**첨부 파일 리디렉션** 섹션에서 **리디렉션 사용**옵션을 선택 하 고 조직의 보안 관리자 또는 검색 된 파일을 검토할 운영자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-141">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>
    - <span data-ttu-id="a6a60-142">**적용 대상** 섹션에서 **받는 사람 도메인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-142">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="a6a60-143">그런 다음 도메인을 선택 하 고 **추가**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-143">Then, select your domain, choose **Add**, and then click **OK**.</span></span>
5. <span data-ttu-id="a6a60-144">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-144">Click **Save**.</span></span>
6. <span data-ttu-id="a6a60-145">(권장 추가 단계) 전역 관리자 또는 SharePoint Online 관리자는 Office 365 환경에 대해 **DisallowInfectedFileDownload** 매개 변수를 *true* 로 설정 하 여 **[set-spotenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-145">(Recommended additional step) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="a6a60-146">따라서 사용자가 악성 파일로 검색 된 파일을 열거나 이동 하거나 복사 하거나 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-146">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="a6a60-147">자세한 내용은 [office 365 atp 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md) 및 [SharePoint, OneDrive 및 Microsoft 팀에 대 한 office 365 atp 켜기](turn-on-atp-for-spo-odb-and-teams.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6a60-147">To learn more, see [Set up Office 365 ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>

### <a name="atp-safe-links-policies"></a><span data-ttu-id="a6a60-148">ATP 안전한 링크 정책</span><span class="sxs-lookup"><span data-stu-id="a6a60-148">ATP Safe Links policies</span></span>

<span data-ttu-id="a6a60-149">ATP 안전한 링크를 설정 하려면 기본 정책을 검토 하 고 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-149">To set up ATP Safe Links, review your default policy and add a policy.</span></span>

1. <span data-ttu-id="a6a60-150">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 안전한 링크**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-150">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>
2. <span data-ttu-id="a6a60-151">**기본** 정책을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-151">Double-click the **Default** policy.</span></span>
3. <span data-ttu-id="a6a60-152">다음 **의 안전한 링크 사용** 섹션에서 **office 365 ProPlus, iOS 및 Android 용 office**를 차례로 선택 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-152">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>
4. <span data-ttu-id="a6a60-153">**특정 받는 사람에 게 적용 되는 정책** 섹션에서 더하기 기호 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-153">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>
5. <span data-ttu-id="a6a60-154">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-154">Specify the following settings:</span></span>
    - <span data-ttu-id="a6a60-155">**이름** 상자에 이름을 입력 `Safe Links`합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-155">In the **Name** box, type a name, such as `Safe Links`.</span></span>
    - <span data-ttu-id="a6a60-156">**작업 선택** 섹션에서 **설정**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-156">In the **Select the action** section, choose **On**.</span></span>
    - <span data-ttu-id="a6a60-157">다음 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-157">Select these options:</span></span>
        - <span data-ttu-id="a6a60-158">**다운로드 가능한 콘텐츠를 검색 하기 위해 안전한 첨부 파일 사용**</span><span class="sxs-lookup"><span data-stu-id="a6a60-158">**Use safe attachments to scan downloadable content**</span></span> 
        - <span data-ttu-id="a6a60-159">**조직 내에서 전송 된 전자 메일 메시지에 안전한 링크 적용**</span><span class="sxs-lookup"><span data-stu-id="a6a60-159">**Apply safe links to email messages sent within the organization**</span></span>
        - <span data-ttu-id="a6a60-160">**사용자가 원본 URL에 대 한 안전한 링크를 클릭 하는 것을 허용 하지 않음**</span><span class="sxs-lookup"><span data-stu-id="a6a60-160">**Do not let users click through safe links to original URL**</span></span>
    - <span data-ttu-id="a6a60-161">**적용 대상** 섹션에서 **받는 사람 도메인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-161">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="a6a60-162">그런 다음 도메인을 선택 하 고 **추가**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-162">Then, select your domain, choose **Add**, and then click **OK**.</span></span>
6. <span data-ttu-id="a6a60-163">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-163">Click **Save**.</span></span>

<span data-ttu-id="a6a60-164">자세한 내용은 [Office 365 ATP 안전한 링크 정책 설정을](set-up-atp-safe-links-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a6a60-164">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing"></a><span data-ttu-id="a6a60-165">3 부-피싱 방지</span><span class="sxs-lookup"><span data-stu-id="a6a60-165">Part 3 - Anti-phishing</span></span> 

<span data-ttu-id="a6a60-166">피싱 방지 보호 기능은 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)을 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-166">Anti-phishing protection is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="a6a60-167">고급 피싱 방지 보호는 [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-167">Advanced anti-phishing protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> <span data-ttu-id="a6a60-168">다음 절차에서는 ATP 피싱 방지 정책을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-168">The following procedure describes how to configure an ATP anti-phishing policy.</span></span> <span data-ttu-id="a6a60-169">이 단계는 피싱 방지 정책 (ATP 없이)을 구성 하는 경우에도 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-169">The steps are similar for configuring an anti-phishing policy (without ATP).</span></span>

1. <span data-ttu-id="a6a60-170">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 피싱 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-170">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>
2. <span data-ttu-id="a6a60-171">**기본 정책을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-171">Click **Default policy**.</span></span>
3. <span data-ttu-id="a6a60-172">**가장** 섹션에서 **편집**을 클릭 하 고 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-172">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>
    -  <span data-ttu-id="a6a60-173">**보호할 사용자 추가** 탭에서 보호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-173">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="a6a60-174">그런 다음 조직의 보드 구성원, CEO, CFO 및 기타 선임 리더와 같은 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-174">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="a6a60-175">(개별 전자 메일 주소를 입력 하거나를 클릭 하 여 목록을 표시할 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="a6a60-175">(You can type an individual email address, or click to display a list.)</span></span>
    - <span data-ttu-id="a6a60-176">**보호할 도메인 추가** 탭에서 **자신이 소유한 도메인을 자동으로 포함**을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-176">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="a6a60-177">사용자 지정 도메인이 있는 경우 해당 도메인도 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-177">If you have custom domains, add those as well.</span></span>
    - <span data-ttu-id="a6a60-178">**작업** 탭에서 가장 된 사용자 및 가장 한 도메인에 대해 **받는 사람의 정크 메일 폴더로 메시지 이동을** 선택 하 고 보안 팁을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-178">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>
    - <span data-ttu-id="a6a60-179">**사서함 인텔리전스** 탭에서 사서함 인텔리전스가 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-179">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>
    - <span data-ttu-id="a6a60-180">**설정 검토** 탭에서 설정을 검토 한 후 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-180">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>
4. <span data-ttu-id="a6a60-181">**스푸핑** 섹션에서 **편집**을 클릭 하 고 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-181">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>
    - <span data-ttu-id="a6a60-182">**스푸핑 필터 설정** 탭에서 스푸핑 방지 보호가 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-182">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>
    - <span data-ttu-id="a6a60-183">**작업** 탭에서 받는 사람의 정크 메일 폴더로 메시지 이동을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-183">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>
    - <span data-ttu-id="a6a60-184">**설정 검토** 탭에서 설정을 검토 한 후 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-184">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="a6a60-185">변경 하지 않은 경우 **취소**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-185">(If you didn't make any changes, click **Cancel**.)</span></span>
5. <span data-ttu-id="a6a60-186">기본 정책 설정 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-186">Close the default policy settings page.</span></span>

<span data-ttu-id="a6a60-187">피싱 방지 정책 옵션에 대 한 자세한 내용은 [Set up Office 365 ATP 안티 피싱 및 피싱 방지 정책을](set-up-anti-phishing-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6a60-187">To learn more about your anti-phishing policy options, see [Set up Office 365 ATP anti-phishing and anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam"></a><span data-ttu-id="a6a60-188">4 부-스팸 방지</span><span class="sxs-lookup"><span data-stu-id="a6a60-188">Part 4 - Anti-spam</span></span>

<span data-ttu-id="a6a60-189">스팸 방지 보호 기능은 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)을 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-189">Anti-spam protection is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span>

1. <span data-ttu-id="a6a60-190">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **스팸 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-190">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>
2. <span data-ttu-id="a6a60-191">**사용자 지정** 탭에서 **사용자 지정 설정을** 켭니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-191">On the **Custom** tab, turn **Custom settings** on.</span></span>
3. <span data-ttu-id="a6a60-192">**기본 스팸 필터 정책을**확장 하 고 **정책 편집**을 클릭 한 후 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-192">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>
    - <span data-ttu-id="a6a60-193">**스팸 및 대량 작업** 섹션에서 임계값을 5 또는 6으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-193">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>
    - <span data-ttu-id="a6a60-194">허용 **목록** 섹션에서 허용 되는 보낸 사람 및 도메인을 검토 하 고 필요에 따라 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-194">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>
4. <span data-ttu-id="a6a60-195">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-195">Click **Save**.</span></span>

<span data-ttu-id="a6a60-196">스팸 방지 정책 옵션에 대 한 자세한 내용은 [스팸 방지 정책 구성을](configure-the-anti-spam-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6a60-196">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---service-wide-settings"></a><span data-ttu-id="a6a60-197">5 부-서비스 수준 설정</span><span class="sxs-lookup"><span data-stu-id="a6a60-197">Part 5 - Service-wide settings</span></span>

### <a name="zero-hour-auto-purge"></a><span data-ttu-id="a6a60-198">제로 시간 자동 삭제</span><span class="sxs-lookup"><span data-stu-id="a6a60-198">Zero-hour auto purge</span></span>

<span data-ttu-id="a6a60-199">[EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)을 포함 하는 구독에서 0 시간 자동 삭제 (ZAP)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-199">Zero-hour auto purge (ZAP) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="a6a60-200">이 보호 기능은 기본적으로 설정 되어 있습니다. 그러나 보호 기능을 적용 하려면 다음 조건을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-200">This protection is turned on by default; however, the following conditions must be met for protection to be in effect:</span></span>
- <span data-ttu-id="a6a60-201">스팸 방지 정책에서 **정크 메일 폴더로 메시지를 이동** 하도록 스팸 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-201">Spam actions are set to **Move message to Junk Email folder** in anti-spam policies.</span></span>
- <span data-ttu-id="a6a60-202">사용자가 기본 정크 메일 설정을 유지 했으며 정크 메일 보호를 해제 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-202">Users have kept their default junk email settings, and have not turned off junk email protection.</span></span>

<span data-ttu-id="a6a60-203">자세한 내용은 스팸 및 맬웨어를 방지 하는 [0 시간 자동 삭제](zero-hour-auto-purge.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6a60-203">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging"></a><span data-ttu-id="a6a60-204">감사 로깅</span><span class="sxs-lookup"><span data-stu-id="a6a60-204">Audit logging</span></span>

<span data-ttu-id="a6a60-205">감사 로깅은 [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)이 포함 된 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-205">Audit logging is available in subscriptions that include [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span></span> <span data-ttu-id="a6a60-206">[보안 대시보드](security-dashboard.md), [전자 메일 보안 보고서](view-email-security-reports.md)및 [탐색기](use-explorer-in-security-and-compliance.md)와 같은 위협 보호 보고서의 데이터를 보려면 조직에 대해 감사 로깅을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a60-206">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md), [email security reports](view-email-security-reports.md), and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span> <span data-ttu-id="a6a60-207">자세한 내용은 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6a60-207">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="a6a60-208">설치 후 작업</span><span class="sxs-lookup"><span data-stu-id="a6a60-208">Post-setup tasks</span></span>

### <a name="watch-for-new-features-and-service-updates"></a><span data-ttu-id="a6a60-209">새로운 기능 및 서비스 업데이트 조사</span><span class="sxs-lookup"><span data-stu-id="a6a60-209">Watch for new features and service updates</span></span>

- [<span data-ttu-id="a6a60-210">Microsoft 365 로드맵 방문</span><span class="sxs-lookup"><span data-stu-id="a6a60-210">Visit the Microsoft 365 Roadmap</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [<span data-ttu-id="a6a60-211">Office 365 Advanced Threat Protection 서비스 설명 참조</span><span class="sxs-lookup"><span data-stu-id="a6a60-211">See the Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)

### <a name="see-how-atp-is-working-for-your-organization"></a><span data-ttu-id="a6a60-212">조직에서 ATP가 작동 하는 방식 확인</span><span class="sxs-lookup"><span data-stu-id="a6a60-212">See how ATP is working for your organization</span></span>

- [<span data-ttu-id="a6a60-213">Office 365 Advanced Threat Protection에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="a6a60-213">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

- [<span data-ttu-id="a6a60-214">보안 &amp; 및 준수 센터에서 탐색기 사용</span><span class="sxs-lookup"><span data-stu-id="a6a60-214">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)

### <a name="periodically-review-and-revise-your-atp-policies"></a><span data-ttu-id="a6a60-215">ATP 정책 주기적으로 검토 및 수정</span><span class="sxs-lookup"><span data-stu-id="a6a60-215">Periodically review and revise your ATP policies</span></span>

- [<span data-ttu-id="a6a60-216">office 365 사용자에 게 office 365 위협 조사 및 응답을 안전 하 게 유지</span><span class="sxs-lookup"><span data-stu-id="a6a60-216">Keep your Office 365 users safe with Office 365 threat investigation and response</span></span>](keep-users-safe-with-office-365-ti.md) 

- [<span data-ttu-id="a6a60-217">Office 365 보안 &amp; 및 준수 센터에서 smart reports 및 insights 사용</span><span class="sxs-lookup"><span data-stu-id="a6a60-217">Use the smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md) 