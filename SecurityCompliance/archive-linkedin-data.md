---
title: Office 365에서 LinkedIn 데이터를 보관 하는 커넥터 설정 (미리 보기)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: 관리자는 기본 커넥터를 설정 하 여 LinkedIn 회사 페이지에서 Office 365로 데이터를 가져올 수 있습니다. 이를 통해 Office 365의 타사 데이터 원본에서 데이터를 보관할 수 있으므로 법적 보존, 콘텐츠 검색 및 보존 정책과 같은 규정 준수 기능을 사용 하 여 조직의 타사 데이터에 대 한 준수를 관리할 수도 있습니다.
ms.openlocfilehash: 618cef7c0208378179d41a94f4a274a0bddadee9
ms.sourcegitcommit: ecc823c2a4f1465114cf1d3a4630e31c47779ddc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/19/2019
ms.locfileid: "35079382"
---
# <a name="set-up-a-connector-to-archive-linkedin-data-in-office-365-preview"></a><span data-ttu-id="ab0ab-104">Office 365에서 LinkedIn 데이터를 보관 하는 커넥터 설정 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="ab0ab-104">Set up a connector to archive LinkedIn data in Office 365 (Preview)</span></span>

<span data-ttu-id="ab0ab-105">Office 365에서 LinkedIn 회사 페이지의 데이터를 보관 하는 커넥터 기능이 미리 보기에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-105">The connector feature to archive data from LinkedIn Company pages in Office 365 is in Preview.</span></span>

<span data-ttu-id="ab0ab-106">Office 365의 보안 & 준수 센터에서 네이티브 커넥터를 사용 하 여 LinkedIn 회사 페이지에서 데이터를 가져오고 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-106">Use a native connector in the Security & Compliance Center in Office 365 to import and archive data from LinkedIn Company pages.</span></span> <span data-ttu-id="ab0ab-107">커넥터를 설정 하 고 구성한 후에는 24 시간 마다 한 번씩 특정 LinkedIn 회사 페이지의 계정에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-107">After you set up and configure a connector, it connects to the account for the specific LinkedIn Company page once every 24 hours.</span></span> <span data-ttu-id="ab0ab-108">이 커넥터는 회사 페이지에 게시 된 메시지를 전자 메일 메시지로 변환한 다음 해당 항목을 Office 365의 사서함으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-108">The connector converts the messages posted to the Company page to an email message, and then imports those items to a mailbox in Office 365.</span></span>

<span data-ttu-id="ab0ab-109">LinkedIn 회사 페이지 데이터가 사서함에 저장 되 면 소송 보존, 콘텐츠 검색, 원본 위치 보관, 감사 및 Office 365 고정 정책과 같은 Office 365 준수 기능을 LinkedIn 데이터에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-109">After the LinkedIn Company page data is stored in a mailbox, you can apply Office 365 compliance features such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies to LinkedIn data.</span></span> <span data-ttu-id="ab0ab-110">예를 들어 콘텐츠 검색을 사용 하 여 이러한 항목을 검색 하거나, 고급 eDiscovery 사례의 custodian에 저장소 사서함을 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-110">For example, you can search for these items using Content Search or associate the storage mailbox with a custodian in an Advanced eDiscovery case.</span></span> <span data-ttu-id="ab0ab-111">Office 365에서 LinkedIn 데이터를 가져오고 보관 하기 위한 커넥터를 만들면 조직이 정부 및 규정 정책을 준수 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-111">Creating a connector to import and archive LinkedIn data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="before-you--begin"></a><span data-ttu-id="ab0ab-112">시작 하기 전에</span><span class="sxs-lookup"><span data-stu-id="ab0ab-112">Before you  begin</span></span>

- <span data-ttu-id="ab0ab-113">조직에서는 Office 365 가져오기 서비스가 조직의 사서함 데이터에 액세스할 수 있도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-113">Your organization must consent to allow the Office 365 Import service to access mailbox data in your organization.</span></span> <span data-ttu-id="ab0ab-114">이 요청에 동의 하려면 [이 페이지로](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent)이동 하 여 Office 365 전역 관리자의 자격 증명으로 로그인 한 다음 요청을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-114">To consent to this request, go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), sign in with the credentials of an Office 365 global admin, and then accept the request.</span></span>

- <span data-ttu-id="ab0ab-115">LinkedIn 회사 페이지 커넥터를 만드는 사용자에 게 Exchange Online의 사서함 가져오기 내보내기 역할이 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-115">The user who creates a LinkedIn Company Page connector must be assigned the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="ab0ab-116">이는 보안 & 준수 센터에서 **타사 데이터 보관** 페이지에 액세스 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-116">This is required to access the **Archive third-party data** page in the Security & Compliance Center.</span></span> <span data-ttu-id="ab0ab-117">기본적으로이 역할은 Exchange Online의 어떠한 역할 그룹에도 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-117">By default, this role isn't assigned to any role group in Exchange Online.</span></span> <span data-ttu-id="ab0ab-118">Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-118">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="ab0ab-119">또는 역할 그룹을 만들고 사서함 가져오기 내보내기 역할을 할당 한 다음 해당 사용자를 구성원으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-119">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="ab0ab-120">자세한 내용은 "Exchange Online에서 역할 그룹 관리" 문서의 [역할 그룹 만들기](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) 또는 [역할 그룹 수정](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-120">For more information, see the  [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

- <span data-ttu-id="ab0ab-121">보관 하려는 LinkedIn 회사 페이지의 관리자 인 LinkedIn 사용자 계정의 로그인 자격 증명 (전자 메일 주소 또는 전화 번호와 암호)이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-121">You must have the sign-in credentials (email address or phone number and password) of a LinkedIn user account that is an admin for the LinkedIn Company Page that you want to archive.</span></span> <span data-ttu-id="ab0ab-122">커넥터를 설정할 때 이러한 자격 증명을 사용 하 여 LinkedIn에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-122">You use these credentials to sign in to LinkedIn when setting up the connector.</span></span>

## <a name="create-a-linkedin-connector"></a><span data-ttu-id="ab0ab-123">LinkedIn 커넥터 만들기</span><span class="sxs-lookup"><span data-stu-id="ab0ab-123">Create a LinkedIn connector</span></span>

1. <span data-ttu-id="ab0ab-124">로 이동한 후 **데이터 거 버 넌 \> 스 가져오기를** 클릭 한 다음 **타사 데이터 보관**을 클릭 합니다. <https://protection.office.com></span><span class="sxs-lookup"><span data-stu-id="ab0ab-124">Go to <https://protection.office.com> and then click **Data governance \> Import** and then click **Archive third-party data**.</span></span>

2. <span data-ttu-id="ab0ab-125">**타사 데이터 보관** 페이지에서 **커넥터 추가**를 클릭 한 다음 **LinkedIn**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-125">On the **Archive third-party data** page, click **Add a connector**, and then click **LinkedIn**.</span></span>

3. <span data-ttu-id="ab0ab-126">**서비스 약관** 페이지에서 **수락**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-126">On the **Terms of service** page, click **Accept**.</span></span>

4. <span data-ttu-id="ab0ab-127">LinkedIn을 **사용** 하 여 로그인 페이지에서 **Linkedin과 함께 로그인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-127">On the **Sign in with LinkedIn** page, click **Sign in with LinkedIn**.</span></span>

   <span data-ttu-id="ab0ab-128">LinkedIn 로그인 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-128">The LinkedIn sign in page is displayed.</span></span>

   ![LinkedIn 로그인 페이지](media/LinkedInSigninPage.png)

5. <span data-ttu-id="ab0ab-130">LinkedIn 로그인 페이지에서 보관 하려는 회사 페이지와 연결 된 LinkedIn 계정의 전자 메일 주소 (또는 전화 번호)와 암호를 입력 하 고 **로그인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-130">On the LinkedIn sign in page, enter the email address (or phone number) and password for the LinkedIn account that associated with the company page that you want to archive, and then click **Sign in**.</span></span>

   <span data-ttu-id="ab0ab-131">로그인 한 계정에 연결 된 모든 LinkedIn 회사 페이지 목록과 함께 마법사 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-131">A wizard page is displayed with a list of all LinkedIn Company Pages associated with the account that you signed in to.</span></span> <span data-ttu-id="ab0ab-132">커넥터는 한 회사 페이지에 대해서만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-132">A connector can only be configured for one company page.</span></span> <span data-ttu-id="ab0ab-133">조직에 LinkedIn 회사 페이지가 여러 개 있는 경우 각 페이지에 대 한 커넥터를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-133">If your organization has multiple LinkedIn Company Pages, you have to create a connector for each one.</span></span>

   ![LinkedIn 회사 페이지 목록이 있는 페이지가 표시 됨](media/LinkedInSelectCompanyPage.png)

6. <span data-ttu-id="ab0ab-135">항목을 보관 하려는 회사 페이지를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-135">Select the company page that you want to archive items from, and then click **Next**.</span></span>

7. <span data-ttu-id="ab0ab-136">**필터 설정** 페이지에서 특정 기간에 해당 하는 항목을 처음 가져올 때 필터를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-136">On the **Set filters** page, you can apply a filter to initially import items that are a certain age.</span></span> <span data-ttu-id="ab0ab-137">보존 기간을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-137">Select an age, and then click **Next**.</span></span>

8. <span data-ttu-id="ab0ab-138">**저장소 계정 설정** 페이지에서 LinkedIn 항목을 가져올 Office 365 사서함의 전자 메일 주소를 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-138">On the **Set storage account** page, type the email address of an Office 365 mailbox that the LinkedIn items will be imported to, and then click **Next**.</span></span> <span data-ttu-id="ab0ab-139">이 사서함의 받은 편지함 폴더로 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-139">Items are imported to the Inbox folder in this mailbox.</span></span>

9. <span data-ttu-id="ab0ab-140">커넥터 설정을 검토 하 고 **저장** 을 클릭 하 여 커넥터 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-140">Review the connector settings and then click **Save** to complete the connector setup.</span></span>

<span data-ttu-id="ab0ab-141">커넥터를 만든 후에는 **타사 데이터 보관** 페이지로 돌아갈 수 있습니다 (필요한 경우 **새로 고침** 을 클릭 하 여 커넥터 목록 업데이트). 새 커넥터 보기</span><span class="sxs-lookup"><span data-stu-id="ab0ab-141">After you create the connector, you can go back to the **Archive third-party data** page (click **Refresh** if necessary to update the list of connectors) a view the new connector.</span></span> <span data-ttu-id="ab0ab-142">**상태** 열의 값이 **시작을 기다리는 중**입니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-142">The value in the **Status** column is **Waiting to start**.</span></span> <span data-ttu-id="ab0ab-143">초기 가져오기 프로세스를 시작 하는 데 최대 24 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-143">It takes up to 24 hours for the initial import process to be started.</span></span> <span data-ttu-id="ab0ab-144">처음에 커넥터를 실행 하 고 LinkedIn 항목을 가져온 후에는 24 시간 마다 한 번씩 커넥터가 실행 되 고 이전 24 시간 동안 LinkedIn 회사 페이지에서 만든 모든 새 항목이 가져오기 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-144">After the first time the connector runs and imports the LinkedIn items, the connector will run once every 24 hours and import any new items that are created on the LinkedIn Company Page in the previous 24 hours.</span></span>

<span data-ttu-id="ab0ab-145">자세한 내용을 보려면 **타사 데이터 보관** 페이지의 목록에서 커넥터를 클릭 하 여 플라이 아웃 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-145">To view more details, click the connector in the list on the **Archive third-party data** page to display the flyout page.</span></span> <span data-ttu-id="ab0ab-146">**상태**에서 표시 되는 날짜 범위는 커넥터를 만들 때 선택한 연령 필터를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-146">Under **Status**, the date range that's displayed indicates the age filter that was selected when the connector was created.</span></span> 

## <a name="more-information"></a><span data-ttu-id="ab0ab-147">추가 정보</span><span class="sxs-lookup"><span data-stu-id="ab0ab-147">More information</span></span>

- <span data-ttu-id="ab0ab-148">LinkedIn 항목은 Office 365의 저장소 사서함에 있는 받은 편지함 폴더로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-148">LinkedIn items are imported to the Inbox folder in the storage mailbox in Office 365.</span></span> <span data-ttu-id="ab0ab-149">전자 메일 메시지로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-149">They appear as email messages.</span></span> <span data-ttu-id="ab0ab-150">메시지를 보낸 사람의 표시 이름은 LinkedIn 회사 페이지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-150">The display name of the sender of the message is the name of the LinkedIn Company Page.</span></span> <span data-ttu-id="ab0ab-151">보낸 사람의 실제 전자 메일 주소는 저장소 사서함의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-151">The actual email address of the sender is the email address of the storage mailbox.</span></span> <span data-ttu-id="ab0ab-152">회사 페이지의 이름도 제목 줄에도 미리 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-152">The name of the company page is also pre-appended to the subject line.</span></span> 

- <span data-ttu-id="ab0ab-153">이전 동작으로 인해 Microsoft eDiscovery 도구를 사용 하 `from` 여 `subject` Office 365에 보관 된 LinkedIn 항목을 검색할 때 또는 전자 메일 속성을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-153">Because of the previous behavior, you can search the `from` or `subject` email properties when using a Microsoft eDiscovery tool to search LinkedIn items that are archived in Office 365.</span></span> <span data-ttu-id="ab0ab-154">예를 들어 회사 페이지의 이름이 "Contoso Company Page" 인 경우 키워드 검색 쿼리의 다음 *속성: 값* 쌍 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-154">For example if the name of the company page is "Contoso Company Page", then you can use one of the following *property:value* pairs in the keyword search query:</span></span>
   
   ```
   from:"Contoso Company Page"
   ```

    <span data-ttu-id="ab0ab-155">또는</span><span class="sxs-lookup"><span data-stu-id="ab0ab-155">Or</span></span>

   ```
   subject:"Contoso Company Page"
   ```

- <span data-ttu-id="ab0ab-156">Office 365로 가져온 LinkedIn 항목을 쉽게 찾거나 관리 하기 위해 저장소 사서함 (또는 FullAccess 권한이 할당 된 사용자)의 소유자가 항목을 LinkedIn 회사 페이지에서 특정 폴더로 이동 하는 받은 편지함 규칙을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-156">To make it easier to locate or manage LinkedIn items imported to Office 365, the owner of the storage mailbox (or anyone assigned the FullAccess permission) can set up an inbox rule to move the items from a LinkedIn Company Page to a specific folder.</span></span> <span data-ttu-id="ab0ab-157">이 기능은 저장소 사서함을 사용 하 여 다른 타사 데이터 원본에서 가져온 항목을 보관 하는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-157">This is helpful if the storage mailbox is used to archive items imported from different third-party data sources.</span></span> <span data-ttu-id="ab0ab-158">예를 들어 제목 필드에 있는 특정 LinkedIn 회사 페이지의 이름을 포함 하는 모든 항목을 특정 폴더로 이동 하는 받은 편지함 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-158">For example, you can create an inbox rule that moves all items that contain the name of a specific LinkedIn Company Page in the subject field to a specific folder.</span></span>