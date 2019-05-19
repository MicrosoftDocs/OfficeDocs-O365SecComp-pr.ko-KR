---
title: Office 365에서 위협 으로부터 보호
ms.author: tracyp
author: msfttracyp
manager: laurawi
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: 이 문서를 참조 하 여 위협 방지 기능을 지금 구성 합니다.
ms.openlocfilehash: 1697904dac69e3b634c0f853fbd48c5a5b5257d8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157300"
---
# <a name="protect-against-threats-in-office-365"></a><span data-ttu-id="a4ac0-103">Office 365에서 위협 으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="a4ac0-103">Protect against threats in Office 365</span></span>

<span data-ttu-id="a4ac0-104">Office 365에는 다양 한 위협 보호 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-104">Office 365 includes a variety of threat protection features.</span></span> <span data-ttu-id="a4ac0-105">여기에는 조직에 대해 위협 방지 기능이 설정 되었는지 확인 하기 위한 검사 목록으로 사용할 수 있는 빠른 시작 가이드가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-105">Here's a quick-start guide you can use as a checklist to make sure your threat protection features are set up for your organization.</span></span> <span data-ttu-id="a4ac0-106">Office 365의 위협 방지 기능을 처음 사용 하는 경우 나 시작할 위치를 모르는 경우에는 다음 지침을 출발점으로 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-106">If you're new to threat protection features in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="a4ac0-107">**초기 권장 설정은 각 정책 유형에 대해 포함 되지만 대부분의 옵션을 사용할 수 있으며, 특정 조직의 요구에 맞게 설정을 조정할 수**있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-107">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="a4ac0-108">정책이 나 변경 내용이 데이터 센터를 통해 작동 하는 데 약 30 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-108">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4ac0-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a4ac0-109">Requirements</span></span>

### <a name="subscriptions"></a><span data-ttu-id="a4ac0-110">구독</span><span class="sxs-lookup"><span data-stu-id="a4ac0-110">Subscriptions</span></span>

<span data-ttu-id="a4ac0-111">위협 보호 기능은 모든 Office 365 구독에 포함 되어 있습니다. 그러나 일부 구독에는 고급 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-111">Threat protection features are included in all Office 365 subscriptions; however, some subscriptions include more advanced features.</span></span> <span data-ttu-id="a4ac0-112">다음 표에는이 문서에 포함 된 모든 보호 기능과 최소 구독 요구 사항이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-112">The following table lists the protection features included in this article together with the minimum subscription requirements.</span></span><br/>

|<span data-ttu-id="a4ac0-113">보호 유형</span><span class="sxs-lookup"><span data-stu-id="a4ac0-113">Protection type</span></span>  |<span data-ttu-id="a4ac0-114">구독 요구 사항</span><span class="sxs-lookup"><span data-stu-id="a4ac0-114">Subscription requirement</span></span>  |
|---------|---------|
|<span data-ttu-id="a4ac0-115">맬웨어 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="a4ac0-115">Anti-malware protection</span></span>    | <span data-ttu-id="a4ac0-116">[Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) EOP</span><span class="sxs-lookup"><span data-stu-id="a4ac0-116">[Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP)</span></span>        |
|<span data-ttu-id="a4ac0-117">전자 메일 및 Office 문서의 악성 Url 및 파일 로부터 보호</span><span class="sxs-lookup"><span data-stu-id="a4ac0-117">Protection from malicious URLs and files in email and Office documents</span></span>    | [<span data-ttu-id="a4ac0-118">Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="a4ac0-118">Office 365 ATP</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)        |
|<span data-ttu-id="a4ac0-119">피싱 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="a4ac0-119">Anti-phishing protection</span></span>    | [<span data-ttu-id="a4ac0-120">EOP</span><span class="sxs-lookup"><span data-stu-id="a4ac0-120">EOP</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)      |
|<span data-ttu-id="a4ac0-121">고급 피싱 방지 보호</span><span class="sxs-lookup"><span data-stu-id="a4ac0-121">Advanced anti-phishing protection</span></span>    | [<span data-ttu-id="a4ac0-122">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a4ac0-122">Office 365 Advanced Threat Protection</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)   |
|<span data-ttu-id="a4ac0-123">스팸 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="a4ac0-123">Anti-spam protection</span></span>     | [<span data-ttu-id="a4ac0-124">EOP</span><span class="sxs-lookup"><span data-stu-id="a4ac0-124">EOP</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)       |
|<span data-ttu-id="a4ac0-125">0 시간 자동 삭제 (전자 메일의 경우)</span><span class="sxs-lookup"><span data-stu-id="a4ac0-125">Zero-hour auto purge (for email)</span></span>    | <span data-ttu-id="a4ac0-126">[EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) EOP</span><span class="sxs-lookup"><span data-stu-id="a4ac0-126">[EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP)</span></span>        |
|<span data-ttu-id="a4ac0-127">감사 로깅 (보고 목적으로 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="a4ac0-127">Audit logging (this is used for reporting purposes)</span></span>    | [<span data-ttu-id="a4ac0-128">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a4ac0-128">Exchange Online</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)        |

### <a name="roles-and-permissions"></a><span data-ttu-id="a4ac0-129">역할 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="a4ac0-129">Roles and permissions</span></span>

<span data-ttu-id="a4ac0-130">[보안 _AMP_ 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)에서 정책을 구성 하려면 적절 한 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-130">You must be assigned an appropriate role to configure policies in the [Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span> <span data-ttu-id="a4ac0-131">다음 표에는 몇 가지 예가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-131">The following table includes some examples:</span></span> 

|<span data-ttu-id="a4ac0-132">역할 또는 역할 그룹</span><span class="sxs-lookup"><span data-stu-id="a4ac0-132">Role or role group</span></span>  |<span data-ttu-id="a4ac0-133">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="a4ac0-133">Where to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="a4ac0-134">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="a4ac0-134">Office 365 Global Administrator</span></span> |[<span data-ttu-id="a4ac0-135">Office 365 관리자 역할 정보</span><span class="sxs-lookup"><span data-stu-id="a4ac0-135">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|<span data-ttu-id="a4ac0-136">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="a4ac0-136">Security Administrator</span></span> |[<span data-ttu-id="a4ac0-137">Azure Active Directory의 관리자 역할 권한</span><span class="sxs-lookup"><span data-stu-id="a4ac0-137">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|<span data-ttu-id="a4ac0-138">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="a4ac0-138">Exchange Online Organization Management</span></span> |[<span data-ttu-id="a4ac0-139">Exchange Online의 사용 권한</span><span class="sxs-lookup"><span data-stu-id="a4ac0-139">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="a4ac0-140">한</span><span class="sxs-lookup"><span data-stu-id="a4ac0-140">and</span></span><br> [<span data-ttu-id="a4ac0-141">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="a4ac0-141">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

<span data-ttu-id="a4ac0-142">자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-142">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="part-1---anti-malware-protection"></a><span data-ttu-id="a4ac0-143">1 부-맬웨어 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="a4ac0-143">Part 1 - Anti-malware protection</span></span>

<span data-ttu-id="a4ac0-144">[맬웨어 방지 보호](anti-malware-protection.md) 는 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP)을 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-144">[Anti-malware protection](anti-malware-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span></span> 

1. <span data-ttu-id="a4ac0-145">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **맬웨어 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-145">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>

2. <span data-ttu-id="a4ac0-146">**기본** 정책을 두 번 클릭 한 다음 **설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-146">Double-click the **Default** policy, and then choose **settings**.</span></span>

3. <span data-ttu-id="a4ac0-147">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-147">Specify the following settings:</span></span>

    - <span data-ttu-id="a4ac0-148">**맬웨어 검색 응답** 섹션에서 기본 설정인 **아니요**를 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-148">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>

    - <span data-ttu-id="a4ac0-149">**일반 첨부 파일 형식 필터** 섹션에서 **설정**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-149">In the **Common Attachment Types Filter** section, choose **On**.</span></span>

4. <span data-ttu-id="a4ac0-150">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-150">Click **Save**.</span></span>

<span data-ttu-id="a4ac0-151">맬웨어 방지 정책 옵션에 대 한 자세한 내용은 [맬웨어 방지 정책 구성을](configure-anti-malware-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-151">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---protection-from-malicious-urls-and-files"></a><span data-ttu-id="a4ac0-152">2 부-악성 Url 및 파일의 보호 기능</span><span class="sxs-lookup"><span data-stu-id="a4ac0-152">Part 2 - Protection from malicious URLs and files</span></span>

<span data-ttu-id="a4ac0-153">악성 Url 및 파일 로부터의 클릭 시간 보호는 atp ( [Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) )를 포함 하는 구독에서 사용할 수 있으며 [atp Safe Attachments](atp-safe-attachments.md) 및 [atp 안전한 링크](atp-safe-links.md) 정책을 통해 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-153">Time-of-click protection from malicious URLs and files is available in subscriptions that include [Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), and is set up through [ATP Safe Attachments](atp-safe-attachments.md) and [ATP Safe Links](atp-safe-links.md) policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="a4ac0-154">ATP 안전한 첨부 파일 정책</span><span class="sxs-lookup"><span data-stu-id="a4ac0-154">ATP Safe Attachments policies</span></span>

<span data-ttu-id="a4ac0-155">[Atp 안전한 첨부 파일](atp-safe-attachments.md)을 설정 하려면 Atp 안전 첨부 파일 정책을 하나 이상 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-155">To set up [ATP Safe Attachments](atp-safe-attachments.md), you must define at least one ATP Safe Attachments policy.</span></span> 

1. <span data-ttu-id="a4ac0-156">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 안전한 첨부 파일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-156">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>

2. <span data-ttu-id="a4ac0-157">**SharePoint, OneDrive 및 Microsoft 팀에 대 한 ATP 설정**옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-157">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

3. <span data-ttu-id="a4ac0-158">**전자 메일 첨부 파일 보호** 섹션에서 더하기 기호 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-158">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>

4. <span data-ttu-id="a4ac0-159">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-159">Specify the following settings:</span></span>

    - <span data-ttu-id="a4ac0-160">**이름** 상자에를 입력 `Block malware`합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-160">In the **Name** box, type `Block malware`.</span></span>

    - <span data-ttu-id="a4ac0-161">응답 섹션에서 **차단을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-161">In the response section, choose **Block**.</span></span>

    - <span data-ttu-id="a4ac0-162">**첨부 파일 리디렉션** 섹션에서 **리디렉션 사용**옵션을 선택 하 고 조직의 보안 관리자 또는 검색 된 파일을 검토할 운영자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-162">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>

    - <span data-ttu-id="a4ac0-163">**적용 대상** 섹션에서 **받는 사람 도메인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-163">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="a4ac0-164">그런 다음 도메인을 선택 하 고 **추가**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-164">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

5. <span data-ttu-id="a4ac0-165">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-165">Click **Save**.</span></span>

6. <span data-ttu-id="a4ac0-166">(**권장 추가 단계**) 전역 관리자 또는 SharePoint Online 관리자는 Office 365 환경에 대해 **DisallowInfectedFileDownload** 매개 변수를 *true* 로 설정 하 여 **[set-spotenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-166">(**Recommended additional step**) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="a4ac0-167">따라서 사용자가 악성 파일로 검색 된 파일을 열거나 이동 하거나 복사 하거나 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-167">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="a4ac0-168">자세한 내용은 [office 365 Atp 안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md) 및 [SharePoint, OneDrive 및 Microsoft 팀에 대 한 Office 365 atp 켜기](turn-on-atp-for-spo-odb-and-teams.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-168">To learn more, see [Set up Office 365 ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>

### <a name="atp-safe-links-policies"></a><span data-ttu-id="a4ac0-169">ATP 안전한 링크 정책</span><span class="sxs-lookup"><span data-stu-id="a4ac0-169">ATP Safe Links policies</span></span>

<span data-ttu-id="a4ac0-170">[ATP 안전한 링크](atp-safe-links.md)를 설정 하려면 기본 정책을 검토 및 편집 하 고 특정 사용자에 대 한 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-170">To set up [ATP Safe Links](atp-safe-links.md), review and edit your default policy, and add a policy for specific users.</span></span>

1. <span data-ttu-id="a4ac0-171">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 안전한 링크**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-171">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>

2. <span data-ttu-id="a4ac0-172">**기본** 정책을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-172">Double-click the **Default** policy.</span></span>

3. <span data-ttu-id="a4ac0-173">다음 **의 안전한 링크 사용** 섹션에서 **office 365 ProPlus, iOS 및 Android 용 office**를 차례로 선택 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-173">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>

4. <span data-ttu-id="a4ac0-174">**특정 받는 사람에 게 적용 되는 정책** 섹션에서 더하기 기호 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-174">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>

5. <span data-ttu-id="a4ac0-175">다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-175">Specify the following settings:</span></span>

    - <span data-ttu-id="a4ac0-176">**이름** 상자에 이름을 입력 `Safe Links`합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-176">In the **Name** box, type a name, such as `Safe Links`.</span></span>

    - <span data-ttu-id="a4ac0-177">**작업 선택** 섹션에서 **설정**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-177">In the **Select the action** section, choose **On**.</span></span>

    - <span data-ttu-id="a4ac0-178">다음 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-178">Select these options:</span></span>

        - <span data-ttu-id="a4ac0-179">**다운로드 가능한 콘텐츠를 검색 하기 위해 안전한 첨부 파일 사용**</span><span class="sxs-lookup"><span data-stu-id="a4ac0-179">**Use safe attachments to scan downloadable content**</span></span> 

        - <span data-ttu-id="a4ac0-180">**조직 내에서 전송 된 전자 메일 메시지에 안전한 링크 적용**</span><span class="sxs-lookup"><span data-stu-id="a4ac0-180">**Apply safe links to email messages sent within the organization**</span></span>

        - <span data-ttu-id="a4ac0-181">**사용자가 원본 URL에 대 한 안전한 링크를 클릭 하는 것을 허용 하지 않음**</span><span class="sxs-lookup"><span data-stu-id="a4ac0-181">**Do not let users click through safe links to original URL**</span></span>

    - <span data-ttu-id="a4ac0-182">**적용 대상** 섹션에서 **받는 사람 도메인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-182">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="a4ac0-183">그런 다음 도메인을 선택 하 고 **추가**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-183">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

6. <span data-ttu-id="a4ac0-184">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-184">Click **Save**.</span></span>

<span data-ttu-id="a4ac0-185">자세한 내용은 [Office 365 ATP 안전한 링크 정책 설정을](set-up-atp-safe-links-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-185">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing-protection"></a><span data-ttu-id="a4ac0-186">3 부-피싱 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="a4ac0-186">Part 3 - Anti-phishing protection</span></span>

<span data-ttu-id="a4ac0-187">[피싱 방지 보호](anti-phishing-protection.md) 기능은 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)을 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-187">[Anti-phishing protection](anti-phishing-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="a4ac0-188">고급 피싱 방지 보호는 [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-188">Advanced anti-phishing protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> <span data-ttu-id="a4ac0-189">다음 절차에서는 ATP 피싱 방지 정책을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-189">The following procedure describes how to configure an ATP anti-phishing policy.</span></span> <span data-ttu-id="a4ac0-190">이 단계는 피싱 방지 정책 (ATP 없이)을 구성 하는 경우에도 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-190">The steps are similar for configuring an anti-phishing policy (without ATP).</span></span>

1. <span data-ttu-id="a4ac0-191">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **ATP 피싱 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-191">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="a4ac0-192">**기본 정책을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-192">Click **Default policy**.</span></span>

3. <span data-ttu-id="a4ac0-193">**가장** 섹션에서 **편집**을 클릭 하 고 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-193">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="a4ac0-194">**보호할 사용자 추가** 탭에서 보호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-194">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="a4ac0-195">그런 다음 조직의 보드 구성원, CEO, CFO 및 기타 선임 리더와 같은 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-195">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="a4ac0-196">(개별 전자 메일 주소를 입력 하거나를 클릭 하 여 목록을 표시할 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="a4ac0-196">(You can type an individual email address, or click to display a list.)</span></span>

    - <span data-ttu-id="a4ac0-197">**보호할 도메인 추가** 탭에서 **자신이 소유한 도메인을 자동으로 포함**을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-197">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="a4ac0-198">사용자 지정 도메인이 있는 경우 해당 도메인도 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-198">If you have custom domains, add those as well.</span></span>

    - <span data-ttu-id="a4ac0-199">**작업** 탭에서 가장 된 사용자 및 가장 한 도메인에 대해 **받는 사람의 정크 메일 폴더로 메시지 이동을** 선택 하 고 보안 팁을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-199">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>

    - <span data-ttu-id="a4ac0-200">**사서함 인텔리전스** 탭에서 사서함 인텔리전스가 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-200">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>

    - <span data-ttu-id="a4ac0-201">**설정 검토** 탭에서 설정을 검토 한 후 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-201">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>

4. <span data-ttu-id="a4ac0-202">**스푸핑** 섹션에서 **편집**을 클릭 하 고 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-202">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="a4ac0-203">**스푸핑 필터 설정** 탭에서 스푸핑 방지 보호가 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-203">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>

    - <span data-ttu-id="a4ac0-204">**작업** 탭에서 받는 사람의 정크 메일 폴더로 메시지 이동을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-204">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>

    - <span data-ttu-id="a4ac0-205">**설정 검토** 탭에서 설정을 검토 한 후 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-205">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="a4ac0-206">변경 하지 않은 경우 **취소**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-206">(If you didn't make any changes, click **Cancel**.)</span></span>

5. <span data-ttu-id="a4ac0-207">기본 정책 설정 페이지를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-207">Close the default policy settings page.</span></span>

<span data-ttu-id="a4ac0-208">피싱 방지 정책 옵션에 대 한 자세한 내용은 [피싱 방지 정책 설정을](set-up-anti-phishing-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-208">To learn more about your anti-phishing policy options, see [Set up anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam-protection"></a><span data-ttu-id="a4ac0-209">4 부-스팸 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="a4ac0-209">Part 4 - Anti-spam protection</span></span>

<span data-ttu-id="a4ac0-210">[스팸 방지 보호](anti-spam-protection.md) 기능은 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)을 포함 하는 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-210">[Anti-spam protection](anti-spam-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span>

1. <span data-ttu-id="a4ac0-211">[보안 & 준수 센터](https://protection.office.com)에서 **위협 관리** > **정책** > **스팸 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-211">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>

2. <span data-ttu-id="a4ac0-212">**사용자 지정** 탭에서 **사용자 지정 설정을** 켭니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-212">On the **Custom** tab, turn **Custom settings** on.</span></span>

3. <span data-ttu-id="a4ac0-213">**기본 스팸 필터 정책을**확장 하 고 **정책 편집**을 클릭 한 후 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-213">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>

    - <span data-ttu-id="a4ac0-214">**스팸 및 대량 작업** 섹션에서 임계값을 5 또는 6으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-214">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>

    - <span data-ttu-id="a4ac0-215">허용 **목록** 섹션에서 허용 되는 보낸 사람 및 도메인을 검토 하 고 필요에 따라 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-215">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>

4. <span data-ttu-id="a4ac0-216">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-216">Click **Save**.</span></span>

<span data-ttu-id="a4ac0-217">스팸 방지 정책 옵션에 대 한 자세한 내용은 [스팸 방지 정책 구성을](configure-the-anti-spam-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-217">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---additional-settings-to-configure"></a><span data-ttu-id="a4ac0-218">5 부-구성할 추가 설정</span><span class="sxs-lookup"><span data-stu-id="a4ac0-218">Part 5 - Additional settings to configure</span></span>

<span data-ttu-id="a4ac0-219">맬웨어, 악성 Url, 파일, 피싱 및 스팸 으로부터 보호를 구성 하는 것 외에도 0 시간 자동 삭제 및 감사 로깅 설정을 구성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-219">In addition to configuring protection from malware, malicious URLs and files, phishing, and spam, we recommend that you configure your zero-hour auto purge and audit logging settings.</span></span>

### <a name="zero-hour-auto-purge-for-email"></a><span data-ttu-id="a4ac0-220">전자 메일에 대 한 제로 시간 자동 삭제</span><span class="sxs-lookup"><span data-stu-id="a4ac0-220">Zero-hour auto purge for email</span></span>

<span data-ttu-id="a4ac0-221">[제로 시간 자동 삭제](zero-hour-auto-purge.md) (ZAP)은 [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description)이 포함 된 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-221">[Zero-hour auto purge](zero-hour-auto-purge.md) (ZAP) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="a4ac0-222">이 보호 기능은 기본적으로 설정 되어 있습니다. 그러나 보호 기능을 적용 하려면 다음 조건을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-222">This protection is turned on by default; however, the following conditions must be met for protection to be in effect:</span></span>

- <span data-ttu-id="a4ac0-223">스팸 [방지 정책](anti-spam-protection.md)에서 **정크 메일 폴더로 메시지를 이동** 하도록 스팸 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-223">Spam actions are set to **Move message to Junk Email folder** in [anti-spam policies](anti-spam-protection.md).</span></span>

- <span data-ttu-id="a4ac0-224">사용자가 기본 [정크 메일 설정을](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)유지 했으며 정크 메일 보호를 해제 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-224">Users have kept their default [junk email settings](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md), and have not turned off junk email protection.</span></span>

<span data-ttu-id="a4ac0-225">자세한 내용은 스팸 및 맬웨어를 방지 하는 [0 시간 자동 삭제](zero-hour-auto-purge.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-225">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging-for-reporting-and-investigation"></a><span data-ttu-id="a4ac0-226">보고 및 조사에 대 한 감사 로깅</span><span class="sxs-lookup"><span data-stu-id="a4ac0-226">Audit logging for reporting and investigation</span></span>

<span data-ttu-id="a4ac0-227">감사 로깅은 [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description)이 포함 된 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-227">Audit logging is available in subscriptions that include [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span></span> <span data-ttu-id="a4ac0-228">[보안 대시보드](security-dashboard.md), [전자 메일 보안 보고서](view-email-security-reports.md)및 [탐색기](use-explorer-in-security-and-compliance.md)와 같은 위협 보호 보고서의 데이터를 보려면 조직에 대해 감사 로깅을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-228">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md), [email security reports](view-email-security-reports.md), and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span> <span data-ttu-id="a4ac0-229">자세한 내용은 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-229">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="a4ac0-230">설치 후 작업</span><span class="sxs-lookup"><span data-stu-id="a4ac0-230">Post-setup tasks</span></span>

<span data-ttu-id="a4ac0-231">위협 방지 기능을 구성한 후에는 이러한 기능이 작동 하는 방식을 모니터링 하 고, 필요에 따라 정책을 검토 및 수정 하 고, 새로운 기능 및 서비스 업데이트를 시청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ac0-231">After you have configured your threat protection features, make sure to monitor how those features are working, review and revise your policies as needed, and watch for new features and service updates.</span></span>

|<span data-ttu-id="a4ac0-232">수행할 작업</span><span class="sxs-lookup"><span data-stu-id="a4ac0-232">What to do</span></span>  |<span data-ttu-id="a4ac0-233">자세한 정보를 볼 수 있는 리소스</span><span class="sxs-lookup"><span data-stu-id="a4ac0-233">Resources to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="a4ac0-234">보고서를 확인 하 여 조직에서 위협 방지 기능을 사용 하는 방법 보기</span><span class="sxs-lookup"><span data-stu-id="a4ac0-234">See how threat protection features are working for your organization by viewing reports</span></span>    |[<span data-ttu-id="a4ac0-235">보안 대시보드</span><span class="sxs-lookup"><span data-stu-id="a4ac0-235">Security dashboard</span></span>](security-dashboard.md)<br/>[<span data-ttu-id="a4ac0-236">전자 메일 보안 보고서</span><span class="sxs-lookup"><span data-stu-id="a4ac0-236">Email security reports</span></span>](view-email-security-reports.md)<br/>[<span data-ttu-id="a4ac0-237">Office 365 ATP에 대 한 보고서</span><span class="sxs-lookup"><span data-stu-id="a4ac0-237">Reports for Office 365 ATP</span></span>](view-reports-for-atp.md)<br/>[<span data-ttu-id="a4ac0-238">위협 탐색기</span><span class="sxs-lookup"><span data-stu-id="a4ac0-238">Threat Explorer</span></span>](use-explorer-in-security-and-compliance.md)    |
|<span data-ttu-id="a4ac0-239">필요에 따라 위협 보호 정책 주기적으로 검토 및 수정</span><span class="sxs-lookup"><span data-stu-id="a4ac0-239">Periodically review and revise your threat protection policies as needed</span></span>    |[<span data-ttu-id="a4ac0-240">보안 점수</span><span class="sxs-lookup"><span data-stu-id="a4ac0-240">Secure Score</span></span>](microsoft-secure-score.md)<br/>[<span data-ttu-id="a4ac0-241">스마트 보고서 및 통찰력</span><span class="sxs-lookup"><span data-stu-id="a4ac0-241">Smart reports and insights</span></span>](reports-and-insights-in-security-and-compliance.md)<br/>[<span data-ttu-id="a4ac0-242">Office 365 위협 조사 및 응답 기능</span><span class="sxs-lookup"><span data-stu-id="a4ac0-242">Office 365 threat investigation and response features</span></span>](keep-users-safe-with-office-365-ti.md)          |
|<span data-ttu-id="a4ac0-243">새로운 기능 및 서비스 업데이트 조사</span><span class="sxs-lookup"><span data-stu-id="a4ac0-243">Watch for new features and service updates</span></span>     |[<span data-ttu-id="a4ac0-244">표준 및 대상 지정 된 릴리스 옵션</span><span class="sxs-lookup"><span data-stu-id="a4ac0-244">Standard and Targeted release options</span></span>](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)<br/>[<span data-ttu-id="a4ac0-245">메시지 센터</span><span class="sxs-lookup"><span data-stu-id="a4ac0-245">Message Center</span></span>](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide)<br/>[<span data-ttu-id="a4ac0-246">Microsoft 365 로드맵</span><span class="sxs-lookup"><span data-stu-id="a4ac0-246">Microsoft 365 Roadmap</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)<br/>[<span data-ttu-id="a4ac0-247">서비스 설명</span><span class="sxs-lookup"><span data-stu-id="a4ac0-247">Service Descriptions</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)         |