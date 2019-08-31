---
title: 보안 및 준수 센터의 메시지 추적
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: 관리자는 보안 & 준수 센터에서 메시지 추적을 사용 하 여 메시지에 대 한 변경 내용을 확인할 수 있습니다.
ms.openlocfilehash: ad5e6e1f5e95b97cf9601890c11129f498fe95b9
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699226"
---
# <a name="message-trace-in-the-security--compliance-center"></a><span data-ttu-id="00774-103">보안 및 준수 센터의 메시지 추적</span><span class="sxs-lookup"><span data-stu-id="00774-103">Message trace in the Security & Compliance Center</span></span>

## <a name="overview"></a><span data-ttu-id="00774-104">개요</span><span class="sxs-lookup"><span data-stu-id="00774-104">Overview</span></span>

<span data-ttu-id="00774-105">보안 & 준수 센터의 메시지 추적은 Exchange Online 조직에서 이동 하는 전자 메일 메시지를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="00774-105">Message trace in the Security & Compliance Center follows email messages as they travel through your Exchange Online organization.</span></span> <span data-ttu-id="00774-106">서비스가 메시지를 수신, 거부, 지연 또는 배달 했는지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-106">You can determine if a message was received, rejected, deferred, or delivered by the service.</span></span> <span data-ttu-id="00774-107">또한 최종 상태에 도달 하기 전에 메시지에 대해 수행 된 작업을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00774-107">It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="00774-108">보안 & 준수 센터의 메시지 추적은 EAC (Exchange 관리 센터)에서 사용 가능 했던 메시지 추적에 대 한 개선 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-108">Message trace in the Security & Compliance Center improves upon message trace that was available in the Exchange admin center (EAC).</span></span> <span data-ttu-id="00774-109">메시지 추적의 정보를 사용 하 여 메시지에 발생 한 상황에 대 한 사용자 질문을 효율적으로 응답 하 고, 메일 흐름 문제를 해결 하 고, 정책 변경을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-109">You can use the information from message trace to efficiently answer user questions about what happened to their messages, troubleshoot mail flow issues, and validate policy changes.</span></span>

> [!NOTE]
> <span data-ttu-id="00774-110">처음 5만 개의 메시지만 결과에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-110">Only the first 50000 messages are displayed in the results.</span></span> <span data-ttu-id="00774-111">Exchange Online PowerShell 또는 Exchange Online Protection PowerShell의 [get-historicalsearch](https://docs.microsoft.com/powershell/module/exchange/reporting/get-historicalsearch) cmdlet은 결과의 모든 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-111">The [Get-HistoricalSearch](https://docs.microsoft.com/powershell/module/exchange/reporting/get-historicalsearch) cmdlet in Exchange Online PowerShell or Exchange Online Protection PowerShell returns all messages in the results.</span></span>

## <a name="open-message-trace"></a><span data-ttu-id="00774-112">메시지 추적 열기</span><span class="sxs-lookup"><span data-stu-id="00774-112">Open message trace</span></span>

1. <span data-ttu-id="00774-113">회사 또는 학교 계정로 [Office 365에 로그인](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4)합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-113">[Sign in to Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span>

2. <span data-ttu-id="00774-114">왼쪽 위에서 앱 시작 관리자 아이콘 ![Office 365 앱 시작 관리자 아이콘](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png)을 선택하고 **관리자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-114">Select the app launcher icon ![Office 365 app launcher icon](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in the upper-left and choose **Admin**.</span></span>

3. <span data-ttu-id="00774-115">왼쪽 아래 탐색 창에서 **관리 센터** 를 확장 하 고 **보안 & 준수**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-115">In the lower-left navigation, expand **Admin centers** and select **Security & Compliance**.</span></span>

4. <span data-ttu-id="00774-116">열리는 **보안 & 준수** 페이지에서 **메일 흐름**을 확장 하 고 **메시지 추적**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-116">In the **Security & Compliance** page that opens, expand **Mail flow**, and select **Message trace**.</span></span>

## <a name="message-trace-page"></a><span data-ttu-id="00774-117">메시지 추적 페이지</span><span class="sxs-lookup"><span data-stu-id="00774-117">Message trace page</span></span>

<span data-ttu-id="00774-118">여기에서 **추적 시작** 단추를 클릭 하 여 새 기본 추적을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-118">From here you can start a new default trace by clicking on the **Start a trace** button.</span></span> <span data-ttu-id="00774-119">지난 2 일 동안의 모든 보낸 사람과 받는 사람에 대 한 모든 메시지를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-119">This will search for all messages for all senders and recipients for the last two days.</span></span> <span data-ttu-id="00774-120">또는 사용 가능한 쿼리 범주에서 저장 된 쿼리 중 하나를 사용 하 여이를 그대로 실행 하거나 직접 쿼리를 위한 시작 점으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-120">Or you can use one of the stored queries from the available query categories and either run them as-is or use them as starting points for your own queries:</span></span>

- <span data-ttu-id="00774-121">**기본 쿼리**: Office 365에서 제공 하는 기본 제공 쿼리</span><span class="sxs-lookup"><span data-stu-id="00774-121">**Default queries**: Built-in queries provided by Office 365.</span></span>

- <span data-ttu-id="00774-122">**사용자 지정 쿼리**: 나중에 사용 하기 위해 조직의 관리자가 저장 한 쿼리</span><span class="sxs-lookup"><span data-stu-id="00774-122">**Custom queries**: Queries saved by admins in your organization for future use.</span></span>

- <span data-ttu-id="00774-123">자동 **저장 된 쿼리**: 가장 최근에 실행 한 지난 10 개의 쿼리</span><span class="sxs-lookup"><span data-stu-id="00774-123">**Autosaved queries**: The last ten most recently run queries.</span></span> <span data-ttu-id="00774-124">이 목록을 사용 하면 중단 된 위치를 쉽게 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-124">This list makes it simple to pick up where you left off.</span></span>

<span data-ttu-id="00774-125">또한이 페이지에서 다운로드 가능한 보고서 뿐 아니라 제출한 요청에 대 한 **다운로드 가능한 보고서** 섹션도 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-125">Also on this page is a **Downloadable reports** section for the requests you've submitted, as well as the reports themselves when they're are available for download.</span></span>

## <a name="options-for-a-new-message-trace"></a><span data-ttu-id="00774-126">새 메시지 추적에 대 한 옵션</span><span class="sxs-lookup"><span data-stu-id="00774-126">Options for a new message trace</span></span>

### <a name="filter-by-senders-and-recipients"></a><span data-ttu-id="00774-127">보낸 사람 및 받는 사람 별로 필터링</span><span class="sxs-lookup"><span data-stu-id="00774-127">Filter by senders and recipients</span></span>

<span data-ttu-id="00774-128">기본값은 **모든 보낸 사람** 및 **모든 받는 사람**이지만 다음 필드를 사용 하 여 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-128">The default values are **All senders** and **All recipients**, but you can use the following fields to filter the results:</span></span>

- <span data-ttu-id="00774-129">**다음 사용자가**이 필드를 클릭 하 여 조직에서 보낸 사람을 한 명 이상 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-129">**By these people**: Click in this field to select one or more senders from your organization.</span></span> <span data-ttu-id="00774-130">또한 검색 페이지의 작동 방식과 마찬가지로, 이름 입력을 시작 하 고 목록의 항목이 입력 한 대로 필터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-130">You can also start to type a name and the items in the list will be filtered by what you've typed, much like how a search page behaves.</span></span>

- <span data-ttu-id="00774-131">다음 **사용자에 게**:이 필드를 클릭 하 여 조직에서 하나 이상의 받는 사람을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-131">**To these people**: Click in this field to select one or more recipients in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="00774-132">외부의 보낸 사람 및 받는 사람의 전자 메일 주소를 입력할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-132">You can also type the email addresses of external senders and recipients.</span></span> <span data-ttu-id="00774-133">와일드 카드는 지원`*@contoso.com` ( `scot?@contoso.com`또는) 되지만 동시에 같은 필드에 여러 와일드 카드 항목을 사용할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-133">Wildcards are supported (`*@contoso.com` or `scot?@contoso.com`), but you can't use multiple wildcard entries in the same field at the same time.</span></span><br/><span data-ttu-id="00774-134">여러 보낸 사람 또는 받는 사람 목록을 세미콜론 (`;`)으로 구분 하 여 붙여 넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-134">You can paste multiple senders or recipients list separated with semicolon (`;`).</span></span> <span data-ttu-id="00774-135">공백 (`\s`), 캐리지 리턴 (`\r`) 또는 다음 줄 (`\n`) 기호를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-135">Spaces (`\s`), carriage return (`\r`) or next lines (`\n`) symbols are allowed.</span></span>

### <a name="time-range"></a><span data-ttu-id="00774-136">시간 범위</span><span class="sxs-lookup"><span data-stu-id="00774-136">Time range</span></span>

<span data-ttu-id="00774-137">기본값은 **2 일**이지만 날짜/시간 범위를 최대 90 일로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-137">The default value is **2 days**, but you can specify date/time ranges of up to 90 days.</span></span> <span data-ttu-id="00774-138">날짜/시간 범위를 사용 하는 경우 다음 문제를 고려 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00774-138">When you use date/time ranges, consider these issues:</span></span>

- <span data-ttu-id="00774-139">기본적으로 **슬라이더** 보기의 시간 범위는 시간 선을 사용 하 여 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-139">By default, you select the time range in **Slider** view using a time line.</span></span> <span data-ttu-id="00774-140">표시 되는 일 또는 시간 설정만 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-140">You can only select the day or time settings that are displayed.</span></span> <span data-ttu-id="00774-141">범위 내 값을 선택 하면 가장 가까운 표시 설정에 시작/종료 버블이 맞춰집니다.</span><span class="sxs-lookup"><span data-stu-id="00774-141">Trying to select an in-between value will snap the start/end bubble to the nearest displayed setting.</span></span>

   ![보안 & 준수 센터의 새 메시지 추적에서 슬라이더 시간 범위](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   <span data-ttu-id="00774-143">그러나 **시작 날짜** 및 **끝 날짜** 값 (시간 포함)을 지정할 수 있는 **사용자 지정** 보기로 전환한 다음 날짜/시간 범위의 **표준 시간대** 를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-143">But, you can also switch to **Custom** view where you can specify the **Start date** and **End date** values (including times), and you can also select the **Time zone** for the date/time range.</span></span> <span data-ttu-id="00774-144">**표준 시간대** 설정은 쿼리 입력과 쿼리 결과에 모두 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-144">Note that the **Time zone** setting applies to both your query inputs and your query results.</span></span>

   ![보안 & 준수 센터의 새 메시지 추적에 사용자 지정 시간 범위](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   <span data-ttu-id="00774-146">10 일 이하인 경우 결과를 **요약** 보고서로 즉시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-146">For 10 days or less, the results are available instantly as a **Summary** report.</span></span> <span data-ttu-id="00774-147">10 일 보다 약간 큰 시간 범위를 지정 하면 다운로드 가능한 CSV 파일 ( **고급 요약** 또는 **확장** 보고서)로만 사용할 수 있으므로 결과가 지연 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-147">If you specify a time range that's even slightly greater than 10 days, the results will be delayed as they are only available as a downloadable CSV file ( **Enhanced summary** or **Extended** reports).</span></span>

   <span data-ttu-id="00774-148">다양 한 보고서 유형에 대 한 자세한 내용은이 항목의 [보고서 유형 선택](#choose-report-type) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00774-148">For more information about the different report types, see the [Choose report type](#choose-report-type) section in this topic.</span></span>

   <span data-ttu-id="00774-149">**참고**: 확장 된 요약 및 확장 보고서는 보관 메시지 추적 데이터를 사용 하 여 준비 되며, 보고서를 다운로드 하는 데 몇 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-149">**Note**: Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available for download.</span></span> <span data-ttu-id="00774-150">동시에 보고서 요청을 제출한 다른 관리자의 수에 따라 대기 중인 요청에 대해 처리가 시작 되기 전에 지연이 발생할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-150">Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before processing starts for your queued request.</span></span>

- <span data-ttu-id="00774-151">**슬라이더** 보기에 쿼리를 저장 하면 상대 시간 범위 (예: 오늘 3 일)가 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-151">Saving a query in **Slider** view saves the relative time range (for example, 3 days from today).</span></span> <span data-ttu-id="00774-152">쿼리를 **사용자 지정** 보기에 저장 하면 절대 날짜/시간 범위 (예: 2018-05-06 13:00-2018-05-08 18:00)가 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-152">Saving a query in **Custom** view saves the absolute date/time range (for example, 2018-05-06 13:00 to 2018-05-08 18:00).</span></span>

### <a name="more-search-options"></a><span data-ttu-id="00774-153">기타 검색 옵션</span><span class="sxs-lookup"><span data-stu-id="00774-153">More search options</span></span>

#### <a name="delivery-status"></a><span data-ttu-id="00774-154">배달 상태</span><span class="sxs-lookup"><span data-stu-id="00774-154">Delivery status</span></span>

<span data-ttu-id="00774-155">기본값을 **모두** 선택 된 채로 두거나 다음 값 중 하나를 선택 하 여 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-155">You can leave the default value **All** selected, or you can select one of the following values to filter the results:</span></span>

- <span data-ttu-id="00774-156">**배달**됨: 메시지가 의도 한 대상에 배달 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-156">**Delivered**: The message was successfully delivered to the intended destination.</span></span>

- <span data-ttu-id="00774-157">**Pending**: 메시지 배달이 시도 중이거나 다시 시도 중입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-157">**Pending**: Delivery of the message is being attempted or re-attempted.</span></span>

- <span data-ttu-id="00774-158">**확장**: 메일 그룹 받는 사람이 그룹의 개별 구성원에 게 배달 되기 전에 확장 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-158">**Expanded**: A distribution group recipient was expanded before delivery to the individual members of the group.</span></span>

- <span data-ttu-id="00774-159">**실패**: 메시지가 배달 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-159">**Failed**: The message was not delivered.</span></span>

- <span data-ttu-id="00774-160">**격리**됨: 메시지가 스팸, 대량 메일 또는 피싱 메일로 격리 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-160">**Quarantined**: The message was quarantined (as spam, bulk mail, or phishing).</span></span> <span data-ttu-id="00774-161">자세한 내용은 [Office 365에서 전자 메일 메시지 격리](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00774-161">For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span></span>

- <span data-ttu-id="00774-162">**스팸으로 필터링**됨: 메시지가 스팸으로 식별 되었으며, 거부 되거나 차단 (격리 되지 않음) 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-162">**Filtered as spam**: The message was identified spam, and was rejected or blocked (not quarantined).</span></span>

- <span data-ttu-id="00774-163">**상태 가져오기:** 최근에 Office 365에서 메시지를 받았지만 다른 상태 데이터는 아직 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-163">**Getting status:** The message was recently received by Office 365, but no other status data is yet available.</span></span> <span data-ttu-id="00774-164">잠시 후 다시 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="00774-164">Check back in a few minutes.</span></span>

<span data-ttu-id="00774-165">**참고**: **Pending,** **검역** **됨 및 Filter로 필터링** 은 10 일 미만의 검색에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-165">**Note**: The values **Pending,** **Quarantined**, and **Filter as spam** are only available for searches less than 10 days.</span></span> <span data-ttu-id="00774-166">또한 실제 및 보고 된 배달 상태 사이에도 5 ~ 10 분의 지연이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-166">Also, there might be a 5 to 10 minute delay between the actual and reported delivery status.</span></span>

#### <a name="message-id"></a><span data-ttu-id="00774-167">메시지 ID</span><span class="sxs-lookup"><span data-stu-id="00774-167">Message ID</span></span>

<span data-ttu-id="00774-168">메시지 헤더의 **메시지 id:** 헤더 필드에 있는 인터넷 메시지 Id (클라이언트 ID 라고도 함)입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-168">This is the internet message ID (also known as the Client ID) that's found in the **Message-ID:** header field in the message header.</span></span> <span data-ttu-id="00774-169">사용자는 특정 메시지를 조사 하기 위해이 값을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-169">Users can give you this value to investigate specific messages.</span></span>

<span data-ttu-id="00774-170">이 값은 메시지 수명을 나타내는 상수입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-170">This value is constant for the lifetime of the message.</span></span> <span data-ttu-id="00774-171">Office 365 또는 Exchange에서 만든 메시지의 경우이 값은 꺾쇠 괄호 ( `<GUID@ServerFQDN>`\< \>)를 포함 하는 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-171">For messages created in Office 365 or Exchange, the value is in the format `<GUID@ServerFQDN>`, including the angle brackets (\< \>).</span></span> <span data-ttu-id="00774-172">예를 들면 `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-172">For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span> <span data-ttu-id="00774-173">다른 메시징 시스템에서는 다른 구문이 나 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-173">Other messaging systems might use different syntax or values.</span></span> <span data-ttu-id="00774-174">이 값은 고유 해야 하지만 일부 전자 메일 시스템에서는이 요구 사항을 엄격 하 게 따르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-174">This value is supposed to be unique, but not all email systems strictly follow this requirement.</span></span> <span data-ttu-id="00774-175">**메시지 ID:** 헤더 필드가 존재 하지 않거나 외부 원본의 받는 메시지에 대해 비어 있는 경우 임의의 값이 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-175">If the **Message-ID:** header field doesn't exist or is blank for incoming messages from external sources, an arbitrary value is assigned.</span></span>

<span data-ttu-id="00774-176">**메시지 ID** 를 사용 하 여 결과를 필터링 할 때 꺾쇠 괄호를 포함 하 여 전체 문자열을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-176">When you use **Message ID** to filter the results, be sure to include the full string, including any angle brackets.</span></span>

#### <a name="direction"></a><span data-ttu-id="00774-177">Direction</span><span class="sxs-lookup"><span data-stu-id="00774-177">Direction</span></span>

<span data-ttu-id="00774-178">기본값을 **모두** 선택 된 채로 두거나, **인바운드** (조직의 받는 사람에 게 보낸 메시지) 또는 **아웃 바운드** (조직의 사용자가 보낸 메시지)를 선택 하 여 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-178">You can leave the default value **All** selected, or you can select **Inbound** (messages sent to recipients in your organization) or **Outbound** (messages sent from users in your organization) to filter the results.</span></span>

#### <a name="original-client-ip-address"></a><span data-ttu-id="00774-179">원래 클라이언트 IP 주소</span><span class="sxs-lookup"><span data-stu-id="00774-179">Original client IP address</span></span>

<span data-ttu-id="00774-180">클라이언트 IP 주소로 결과를 filer 하 여 많은 양의 스팸 또는 맬웨어를 보내는 해킹 당한 컴퓨터를 조사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-180">You can filer the results by client IP address to investigate hacked computers that are sending large amounts of spam or malware.</span></span> <span data-ttu-id="00774-181">메시지가 여러 보낸 사람 으로부터 온 것 처럼 보일 수 있지만 동일한 컴퓨터에서 모든 메시지를 생성 하 고 있을 가능성이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-181">Although the messages might appear to come from multiple senders, it's likely that the same computer is generating all of the messages.</span></span>

<span data-ttu-id="00774-182">**참고**: 클라이언트 IP 주소 정보는 10 일 동안에만 사용할 수 있으며, **고급 요약** 또는 **확장** 보고서 (다운로드 가능 CSV 파일) 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-182">**Note**: The client IP address information is only available for 10 days, and is only available in the **Enhanced summary** or **Extended** reports (downloadable CSV files).</span></span>

### <a name="choose-report-type"></a><span data-ttu-id="00774-183">보고서 유형 선택</span><span class="sxs-lookup"><span data-stu-id="00774-183">Choose report type</span></span>

<span data-ttu-id="00774-184">사용 가능한 보고서 유형은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-184">The available report types are:</span></span>

- <span data-ttu-id="00774-185">**요약**: 시간 범위가 10 일 미만이 면 사용 가능, 추가 필터링 옵션을 사용 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-185">**Summary**: Available if the time range is less than 10 days, and requires no additional filtering options.</span></span> <span data-ttu-id="00774-186">결과는 **검색**을 클릭 하면 즉시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-186">The results are available almost immediately after you click **Search**.</span></span>

- <span data-ttu-id="00774-187">**향상 된 요약** 또는 **확장**: 이러한 보고서는 다운로드 가능한 CSV 파일로만 제공 되며, **이러한 사용자** \*\*\*\* **에의 한 시간 범위에 관계 없이 다음 필터링 옵션 중 하나 이상이 필요 합니다. 메시지 ID**입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-187">**Enhanced summary** or **Extended**: These reports are only available as downloadable CSV files, and require one or more of the following filtering options regardless of the time range: **By these people**, **To these people**, or **Message ID**.</span></span> <span data-ttu-id="00774-188">보낸 사람 또는 받는 사람 (예: \*@contoso .com)에 와일드 카드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-188">You can use wildcards for the senders or the recipients (for example, \*@contoso.com).</span></span>

<span data-ttu-id="00774-189">**참고:**</span><span class="sxs-lookup"><span data-stu-id="00774-189">**Notes**:</span></span>

- <span data-ttu-id="00774-190">향상 된 요약 및 확장 보고서는 아카이브된 메시지 추적 데이터를 사용 하 여 준비 되며, 보고서를 다운로드 하는 데 몇 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-190">Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available to download.</span></span> <span data-ttu-id="00774-191">동시에 보고서 요청을 제출한 다른 관리자의 수에 따라 대기 요청이 처리 되기 시작 하기 전에 지연이 발생할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-191">Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before your queued request starts to be processed.</span></span>

- <span data-ttu-id="00774-192">날짜/시간 범위에 대해 고급 요약 또는 확장 보고서를 선택할 수 있지만 일반적으로 이러한 두 가지 유형의 보고서에서는 보관 된 데이터의 마지막 4 시간을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-192">While you can select an Enhanced summary or Extended report for any date/time range, commonly the last four hours of archived data will not yet be available for these two types of reports.</span></span>

<span data-ttu-id="00774-193">**다음**을 클릭 하면 선택한 필터링 옵션, 보고서의 고유한 제목, 메시지 추적이 완료 되 면 알림을 받는 전자 메일 주소 (편집 가능)가 나열 된 요약 페이지와 함께 표시 됩니다. 조직의 허용 도메인 중 하나에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-193">When you click **Next**, you're presented with a summary page that lists the filtering options that you selected, a unique (editable) title for the report, and the email address that receives the notification when the message trace completes (also editable, and must be in one of your organization's accepted domains).</span></span> <span data-ttu-id="00774-194">**보고서 준비** 를 클릭 하 여 메시지 추적을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-194">Click **Prepare report** to submit the message trace.</span></span> <span data-ttu-id="00774-195">주 **메시지 추적** 페이지에서 **다운로드 가능한 보고서** 섹션에서 보고서의 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-195">On the main **Message trace** page, you can see the status of the report in the **Downloadable reports** section.</span></span>

<span data-ttu-id="00774-196">서로 다른 보고서 유형에 서 반환 되는 정보에 대 한 자세한 내용은 다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00774-196">For more information about the information that's returned in the different report types, see the next section.</span></span>

## <a name="message-trace-results"></a><span data-ttu-id="00774-197">메시지 추적 결과</span><span class="sxs-lookup"><span data-stu-id="00774-197">Message trace results</span></span>

<span data-ttu-id="00774-198">각 보고서 유형은 서로 다른 정보 수준을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-198">The different report types return different levels of information.</span></span> <span data-ttu-id="00774-199">다음 섹션에서는 각 보고서에서 사용할 수 있는 정보에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-199">The information that's available in the different reports is described in the following sections.</span></span>

### <a name="summary-report-output"></a><span data-ttu-id="00774-200">요약 보고서 출력</span><span class="sxs-lookup"><span data-stu-id="00774-200">Summary report output</span></span>

<span data-ttu-id="00774-201">메시지 추적을 실행 한 후 결과가 나열 되 고 내림차순 날짜/시간 (가장 최근 것부터)을 기준으로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-201">After running the message trace, the results will be listed, sorted by descending date/time (most recent first).</span></span>

![보안 & 준수 센터의 메시지 추적에 대 한 요약 보고서 결과](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

<span data-ttu-id="00774-203">요약 보고서에는 다음과 같은 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-203">The summary report contains the following information:</span></span>

- <span data-ttu-id="00774-204">**날짜**: 구성 된 UTC 표준 시간대를 사용 하 여 서비스에서 메시지를 받은 날짜와 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-204">**Date**: The date and time at which the message was received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="00774-205">**보낸 사람**: 보낸 사람의 전자 메일 주소 (*별칭*@*도메인*)입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-205">**Sender**: The email address of the sender (*alias*@*domain*).</span></span>

- <span data-ttu-id="00774-206">**받는 사람**: 받는 사람의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-206">**Recipient**: The email address of the recipient or recipients.</span></span> <span data-ttu-id="00774-207">여러 받는 사람에 게 보내는 메시지의 경우 받는 사람당 한 줄이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-207">For a message sent to multiple recipients, there's one line per recipient.</span></span> <span data-ttu-id="00774-208">받는 사람이 메일 그룹, 동적 메일 그룹 또는 메일 사용이 가능한 보안 그룹인 경우 그룹은 첫 번째 받는 사람이 되며, 그룹의 각 구성원은 별도의 줄에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-208">If the recipient is a distribution group, dynamic distribution group, or mail-enabled security group, the group will be the first recipient, and then each member of the group is on a separate line.</span></span>

- <span data-ttu-id="00774-209">**제목**: 메시지 **제목:** 필드의 처음 256 자입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-209">**Subject**: The first 256 characters of the message's **Subject:** field.</span></span>

- <span data-ttu-id="00774-210">**상태**: 이러한 값은 [배달 상태](#delivery-status) 섹션에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-210">**Status**: These values are described in the [Delivery status](#delivery-status) section.</span></span>

<span data-ttu-id="00774-211">기본적으로 첫 번째 250 결과가 로드 되어 즉시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-211">By default, the first 250 results are loaded and readily available.</span></span> <span data-ttu-id="00774-212">아래로 스크롤하면 다음 결과 배치가 로드 될 때 약간의 일시 중지가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-212">When you scroll down, there's a slight pause as the next batch of results are loaded.</span></span> <span data-ttu-id="00774-213">스크롤 대신 **모두 로드** 를 클릭 하 여 모든 결과를 최대 1만까지 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-213">Instead of scrolling, you can click **Load all** to load all of the results up to a maximum of 10,000.</span></span>

<span data-ttu-id="00774-214">열 머리글을 클릭 하 여 해당 열의 값을 기준으로 오름차순 또는 내림차순으로 결과를 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-214">You can click on the column headers to sort the results by the values in that column in ascending or descending order.</span></span>

<span data-ttu-id="00774-215">**필터 결과** 를 클릭 하 여 하나 이상의 열을 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-215">You can click **Filter results** to filter the results by one or more columns.</span></span>

<span data-ttu-id="00774-216">**결과** 내보내기를 클릭 한 후 **모든 결과**내보내기, **로드 된 결과 내보내기**또는 **선택한 내보내기를**선택 하 여 하나 이상의 행을 선택한 후 결과를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-216">You can export the results after you've selected one or more rows by clicking **Export results** and then selecting **Export all results**, **Export loaded results**, or **Export selected**.</span></span>

#### <a name="find-related-records-for-this-message"></a><span data-ttu-id="00774-217">이 메시지에 대 한 관련 레코드 찾기</span><span class="sxs-lookup"><span data-stu-id="00774-217">Find related records for this message</span></span>

<span data-ttu-id="00774-218">관련 메시지 레코드는 동일한 메시지 ID를 공유 하는 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-218">Related message records are records that shared the same Message ID.</span></span> <span data-ttu-id="00774-219">두 사용자 간에 전송 되는 단일 메시지는 여러 레코드를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-219">Remember, even a single message sent between two people can generate multiple records.</span></span> <span data-ttu-id="00774-220">메일 그룹 확장, 전달, 메일 흐름 규칙 (전송 규칙이 라고도 함) 등으로 인해 메시지가 영향을 받는 경우 레코드 수가 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-220">The number of records increases when the message is affected by distribution group expansion, forwarding, mail flow rules (also known as transport rules), etc.</span></span>

<span data-ttu-id="00774-221">행의 확인란을 선택한 후에는 **관련** 된 레코드 찾기 단추를 클릭 하거나](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **이 메시지에 대 한 관련 레코드**보다 더 많은 추가 **옵션** ![을 선택 하 여 해당 메시지에 대 한 관련 기록을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-221">After you select a row's check box, you can find related records for the message by clicking the **Find related** button that appears, or by selecting **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Find related records for this message**).</span></span>

<span data-ttu-id="00774-222">메시지 ID에 대 한 자세한 내용은이 항목 앞부분의 메시지 ID 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00774-222">For more information about the Message ID, see the Message ID section earlier in this topic.</span></span>

#### <a name="message-trace-details"></a><span data-ttu-id="00774-223">메시지 추적 정보</span><span class="sxs-lookup"><span data-stu-id="00774-223">Message trace details</span></span>

<span data-ttu-id="00774-224">요약 보고서 출력에서 다음 방법 중 하나를 사용 하 여 메시지에 대 한 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-224">In the summary report output, you can view details about a message by using either of the following methods:</span></span>

- <span data-ttu-id="00774-225">행을 선택 하 고 확인란을 제외 하 고 행의 아무 곳 이나 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-225">Select the row (click anywhere in the row except the check box).</span></span>

- <span data-ttu-id="00774-226">행의 확인란을 선택 하 고 **기타 옵션** ![기타](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **메시지 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-226">Select the row's check box and click **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **View message details**.</span></span>

   ![요약 보고서 메시지 추적에서 행을 두 번 클릭 하면 보안 & 준수 센터의 결과가 반환 됩니다.](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

<span data-ttu-id="00774-228">메시지 추적 세부 정보에는 요약 보고서에 표시 되지 않는 다음과 같은 추가 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-228">The message trace details contain the following additional information that's not present in the summary report:</span></span>

- <span data-ttu-id="00774-229">**메시지 이벤트**:이 섹션에는 서비스에서 메시지에 대해 수행 하는 작업을 분류 하는 데 도움이 되는 분류가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-229">**Message events**: This section contains classifications that help categorize the actions that the service takes on messages.</span></span> <span data-ttu-id="00774-230">발생할 수 있는 **몇 가지 흥미로운 이벤트** 는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-230">**Some of the more interesting events** that you might encounter are:</span></span>

  - <span data-ttu-id="00774-231">**Receive**: 서비스가 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-231">**Receive**: The message was received by the service.</span></span>

  - <span data-ttu-id="00774-232">**Send**: 메시지가 서비스에 의해 전송 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-232">**Send**: The message was sent by the service.</span></span>

  - <span data-ttu-id="00774-233">**Fail**: 메시지를 배달 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-233">**Fail**: The message failed to be delivered.</span></span>

  - <span data-ttu-id="00774-234">**배달**: 메시지가 사서함에 배달 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-234">**Deliver**: The message was delivered to a mailbox.</span></span>

  - <span data-ttu-id="00774-235">**Expand**: 확장 된 메일 그룹으로 메시지를 보냈습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-235">**Expand**: The message was sent to a distribution group that was expanded.</span></span>

  - <span data-ttu-id="00774-236">**전송**: 콘텐츠 변환, 메시지 받는 사람 제한 또는 에이전트로 인해 받는 사람이 분기 메시지로 메시지로 이동 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-236">**Transfer**: Recipients were moved to a bifurcated message because of content conversion, message recipient limits, or agents.</span></span>

  - <span data-ttu-id="00774-237">**지연**: 메시지 배달이 연기 되었으며 나중에 다시 시도 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-237">**Defer**: The message delivery was postponed and might be re-attempted later.</span></span>

  - <span data-ttu-id="00774-238">**해결 됨**: 메시지가 Active Directory 조회를 기반으로 하는 새 받는 사람 주소로 리디렉션 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-238">**Resolved**: The message was redirected to a new recipient address based on an Active Directory look up.</span></span> <span data-ttu-id="00774-239">이 경우 원본 받는 사람 주소가 메시지 추적에 별도의 행으로 표시되고 메시지의 최종 배달 상태가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-239">When this happens, the original recipient address is listed in a separate row in the message trace along with the final delivery status for the message.</span></span>

  <span data-ttu-id="00774-240">참고:</span><span class="sxs-lookup"><span data-stu-id="00774-240">Notes:</span></span>

  - <span data-ttu-id="00774-241">성공적으로 배달 되는 이벤트가 없는는 메시지 추적에 여러 **이벤트** 항목을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-241">An uneventful message that's successfully delivered will generate multiple **Event** entries in the message trace.</span></span>

  - <span data-ttu-id="00774-242">이 목록은 포괄적이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="00774-242">This list is not meant to be exhaustive.</span></span> <span data-ttu-id="00774-243">자세한 이벤트에 대 한 설명은 [메시지 추적 로그의 이벤트 유형을](https://docs.microsoft.com/Exchange/mail-flow/transport-logs/message-tracking#event-types-in-the-message-tracking-log)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00774-243">For descriptions of more events, see [Event types in the message tracking log](https://docs.microsoft.com/Exchange/mail-flow/transport-logs/message-tracking#event-types-in-the-message-tracking-log).</span></span> <span data-ttu-id="00774-244">이 링크는 Exchange Server (온-프레미스 Exchange) 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-244">Note that this link is an Exchange Server (on-premises Exchange) topic.</span></span>

- <span data-ttu-id="00774-245">**추가 정보**:이 섹션에는 다음과 같은 세부 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-245">**More information**: This section contains the following details:</span></span>

  - <span data-ttu-id="00774-246">**메시지 id**:이 값은이 항목 앞부분의 [메시지 id](#message-id) 섹션에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-246">**Message ID**: This value is described in the [Message ID](#message-id) section earlier in this topic.</span></span> <span data-ttu-id="00774-247">예를 들면 `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-247">For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

  - <span data-ttu-id="00774-248">**메시지 크기**   첨부 파일 등을 비롯한 메시지 크기(KB)입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-248">**Message size**</span></span>

  - <span data-ttu-id="00774-249">**보낸 사람 IP**: 메시지를 보낸 컴퓨터의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-249">**From IP**: The IP address of the computer that sent the message.</span></span> <span data-ttu-id="00774-250">Exchange Online에서 전송되는 아웃바운드 메시지의 경우 이 값은 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-250">For outbound messages sent from Exchange Online, this value is blank.</span></span>

  - <span data-ttu-id="00774-251">**받는 사람 ip**: 서비스에서 메시지 배달을 시도한 IP 주소 또는 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-251">**To IP**: The IP address or addresses where the service attempted to deliver the message.</span></span> <span data-ttu-id="00774-252">받는 사람이 여러 명일 경우 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-252">If the message has multiple recipients, these are displayed.</span></span> <span data-ttu-id="00774-253">Exchange Online으로 전송되는 인바운드 메시지의 경우 이 값은 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-253">For inbound messages sent to Exchange Online, this value is blank.</span></span>

### <a name="enhanced-summary-reports"></a><span data-ttu-id="00774-254">향상 된 요약 보고서</span><span class="sxs-lookup"><span data-stu-id="00774-254">Enhanced summary reports</span></span>

<span data-ttu-id="00774-255">사용 가능 (완료 됨) 향상 된 요약 보고서는 시작 메시지 추적의 **다운로드 가능한 보고서** 섹션에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-255">Available (completed) Enhanced summary reports are available in the **Downloadable reports** section at the beginning message trace.</span></span> <span data-ttu-id="00774-256">보고서에서는 다음과 같은 정보를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-256">The following information is available in the report:</span></span>

- <span data-ttu-id="00774-257">**origin_timestamp**<sup>\*</sup>: 구성 된 UTC 표준 시간대를 사용 하 여 서비스에서 처음으로 메시지를 받은 날짜와 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-257">**origin_timestamp**<sup>\*</sup>: The date and time when the message was initially received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="00774-258">**sender_address**: 보낸 사람의 전자 메일 주소 (*별칭*@*도메인*)입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-258">**sender_address**: The sender's email address (*alias*@*domain*).</span></span>

- <span data-ttu-id="00774-259">**Recipient_status**: 받는 사람에 대 한 메시지 배달 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-259">**Recipient_status**: The status of the delivery of the message to the recipient.</span></span> <span data-ttu-id="00774-260">메시지가 여러 받는 사람에 게 전송 되 면 \< *전자 메일 주소*\>##\<*상태*\>와 같은 형식으로 모든 받는 사람과 해당 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-260">If the message was sent to multiple recipients, it will show all the recipients and the corresponding status for each, in the format: \<*email address*\>##\<*status*\>.</span></span> <span data-ttu-id="00774-261">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-261">For example:</span></span>

  - <span data-ttu-id="00774-262">**# #Receive, Send** 는 서비스에서 메시지를 받았으며 의도 한 대상으로 전송 되었음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-262">**##Receive, Send** means the message was received by the service and was sent to the intended destination.</span></span>

  - <span data-ttu-id="00774-263">**# #Receive, Fail** 은 서비스에서 메시지를 받았지만 의도 한 대상에 배달 하지 못했음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-263">**##Receive, Fail** means the message was received by the service but delivery to the intended destination failed.</span></span>

  - <span data-ttu-id="00774-264">**# #Receive, 배달** 이란 서비스가 메시지를 받았으며 받는 사람의 사서함으로 배달 되었음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-264">**##Receive, Deliver** means the message was received by the service and was delivered to the recipient's mailbox.</span></span>

- <span data-ttu-id="00774-265">**message_subject**: 메시지의 **제목** 필드에서 처음 256 자입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-265">**message_subject**: The first 256 characters of the message's **Subject** field.</span></span>

- <span data-ttu-id="00774-266">**total_bytes**: 첨부 파일을 포함 한 메시지의 크기 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-266">**total_bytes**: The size of the message in bytes, including attachments.</span></span>

- <span data-ttu-id="00774-267">**message_id**:이 값은이 항목 앞부분의 [메시지 id](#message-id) 섹션에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-267">**message_id**: This value is described in the [Message ID](#message-id) section earlier in this topic.</span></span> <span data-ttu-id="00774-268">예를 들면 `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-268">For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

- <span data-ttu-id="00774-269">**network_message_id**: 분기 또는 메일 그룹 확장으로 인해 만들어질 수 있는 모든 메시지 복사본에 걸쳐 유지 되는 고유한 메시지 id 값입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-269">**network_message_id**: A unique message ID value that persists across all copies of the message that might be created due to bifurcation or distribution group expansion.</span></span> <span data-ttu-id="00774-270">예를 들면 값 `1341ac7b13fb42ab4d4408cf7f55890f`은입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-270">An example value is `1341ac7b13fb42ab4d4408cf7f55890f`.</span></span>

- <span data-ttu-id="00774-271">**original_client_ip**: 보낸 사람의 클라이언트 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-271">**original_client_ip**: The IP address of the sender's client.</span></span>

- <span data-ttu-id="00774-272">**방향성**: 메시지가 조직에 전송 된 인바운드 (1) 인지 또는 조직에서 보낸 아웃 바운드 메시지 (2)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="00774-272">**directionality**: Indicates whether the message was sent inbound (1) to your organization, or whether it was sent outbound (2) from your organization.</span></span>

- <span data-ttu-id="00774-273">**connector_id**: 원본 또는 대상 커넥터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-273">**connector_id**: The name of the source or destination connector.</span></span> <span data-ttu-id="00774-274">Exchange Online의 커넥터에 대 한 자세한 내용은 [Office 365에서 커넥터를 사용 하 여 메일 흐름 구성을](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00774-274">For more information about connectors in Exchange Online, see [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span></span>

- <span data-ttu-id="00774-275">**delivery_priority**<sup>\*</sup>: 메시지가 **높음**, **낮음**또는 **보통** 우선 순위와 함께 전송 되었는지 여부</span><span class="sxs-lookup"><span data-stu-id="00774-275">**delivery_priority**<sup>\*</sup>: Whether the message was sent with **High**, **Low**, or **Normal** priority.</span></span>

<span data-ttu-id="00774-276"><sup>\*</sup>이러한 속성은 향상 된 요약 보고서 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-276"><sup>\*</sup>These properties are only available in Enhanced summary reports.</span></span>

### <a name="extended-reports"></a><span data-ttu-id="00774-277">확장 된 보고서</span><span class="sxs-lookup"><span data-stu-id="00774-277">Extended reports</span></span>

<span data-ttu-id="00774-278">사용 가능 (완료 됨) 확장 보고서는 메시지 추적을 시작할 때 **다운로드 가능한 보고서** 섹션에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-278">Available (completed) Extended reports are available in the **Downloadable reports** section at the beginning of message trace.</span></span> <span data-ttu-id="00774-279">고급 요약 보고서의 모든 정보는 **origin_timestamp** 및 **delivery_priority**를 제외 하 고 확장 된 보고서에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-279">Virtually all of the information from an Enhanced summary report is available in an Extended report (with the exception of **origin_timestamp** and **delivery_priority**).</span></span> <span data-ttu-id="00774-280">다음 추가 정보는 확장 된 보고서 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-280">The following additional information is only available in an Extended report:</span></span>

- <span data-ttu-id="00774-281">**client_ip**: 메시지를 전송한 전자 메일 서버 또는 메시징 클라이언트의 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-281">**client_ip**: The IP address of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="00774-282">**client_hostname**: 메시지를 전송한 전자 메일 서버 또는 메시징 클라이언트의 호스트 이름 또는 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-282">**client_hostname**: The host name or FQDN of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="00774-283">**server_ip**: 원본 또는 대상 서버의 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-283">**server_ip**: The IP address of the source or destination server.</span></span>

- <span data-ttu-id="00774-284">**server_hostname**: 대상 서버의 호스트 이름 또는 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-284">**server_hostname**: The host name or FQDN of the destination server.</span></span>

- <span data-ttu-id="00774-285">**source_context**: **원본** 필드와 관련 된 추가 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-285">**source_context**: Extra information associated with the **source** field.</span></span> <span data-ttu-id="00774-286">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-286">For example:</span></span>

  - `Protocol Filter Agent`

  - `3489061114359050000`

- <span data-ttu-id="00774-287">**원본**: 이벤트를 담당 하는 Exchange Online 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-287">**source**: The Exchange Online component that's responsible for the event.</span></span> <span data-ttu-id="00774-288">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-288">For example:</span></span>

  - `AGENT`

  - `MAILBOXRULE`

  - `SMTP`

- <span data-ttu-id="00774-289">**event_id**: [이 메시지의 관련 레코드 찾기](#find-related-records-for-this-message) 섹션에서 설명 하는 **메시지 이벤트** 값에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-289">**event_id**: These correspond to the **Message event** values that are explained in the [Find related records for this message](#find-related-records-for-this-message) section.</span></span>

- <span data-ttu-id="00774-290">**internal_message_id**: 현재 메시지를 처리 하는 Exchange Online 서버에서 할당 한 메시지 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-290">**internal_message_id**: A message identifier that's assigned by the Exchange Online server that's currently processing the message.</span></span>

- <span data-ttu-id="00774-291">**recipient_address**: 메시지 받는 사람의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-291">**recipient_address**: The email addresses of the message's recipients.</span></span> <span data-ttu-id="00774-292">전자 메일 주소가 여러 개인 경우 세미콜론(;)으로 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-292">Multiple email addresses are separated by the semicolon character (;).</span></span>

- <span data-ttu-id="00774-293">**recipient_count**: 메시지의 총 받는 사람 수입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-293">**recipient_count**: The total number of recipients in the message.</span></span>

- <span data-ttu-id="00774-294">**related_recipient_address**:, 및 `EXPAND` `RESOLVE` 이벤트 `REDIRECT`와 함께 사용 하 여 메시지와 연결 된 다른 받는 사람의 전자 메일 주소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-294">**related_recipient_address**: Used with `EXPAND`, `REDIRECT`, and `RESOLVE` events to display other recipient email addresses that are associated with the message.</span></span>

- <span data-ttu-id="00774-295">**참조**:이 필드에는 특정 유형의 이벤트에 대 한 추가 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-295">**reference**: This field contains additional information for specific types of events.</span></span> <span data-ttu-id="00774-296">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-296">For example:</span></span>

  - <span data-ttu-id="00774-297">**Dsn**:이 이벤트 다음에 dsn이 생성 되는 경우 관련 된 배달 상태 알림 (dsn, 배달 못 함 보고서, NDR 또는 바운스 메시지)의 **message_id** 값을 나타내는 보고서 링크가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-297">**DSN**: Contains the report link, which is the **message_id** value of the associated delivery status notification (also known as a DSN, non-delivery report, NDR, or bounce message) if a DSN is generated subsequent to this event.</span></span> <span data-ttu-id="00774-298">DSN 메시지의 경우이 필드에는 DSN이 생성 된 원본 메시지의 **message_id** 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-298">If this is a DSN message, this field contains the **message_id** value of the original message that the DSN was generated for.</span></span>

  - <span data-ttu-id="00774-299">**EXPAND**: 관련 메시지의 **related_recipient_address** 값을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-299">**EXPAND**: Contains the **related_recipient_address** value of the related messages.</span></span>

  - <span data-ttu-id="00774-300">**RECEIVE**: 다른 프로세스에서 메시지를 생성 한 경우 (예를 들어, 받은 편지함 규칙) 관련 메시지의 **message_id** 값을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-300">**RECEIVE**: Might contain the **message_id** value of the related message if the message was generated by other processes (for example, Inbox rules).</span></span>

  - <span data-ttu-id="00774-301">**SEND**: DSN 메시지의 **internal_message_id** 값을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-301">**SEND**: Contains the **internal_message_id** value of any DSN messages.</span></span>

  - <span data-ttu-id="00774-302">**TRANSFER**: 분기 중인 메시지의 **internal_message_id** 값을 포함 합니다 (예를 들어 콘텐츠 변환, 메시지 받는 사람 제한 또는 에이전트).</span><span class="sxs-lookup"><span data-stu-id="00774-302">**TRANSFER**: Contains the **internal_message_id** value of the message that's being forked (for example, by content conversion, message recipient limits, or agents).</span></span>

  - <span data-ttu-id="00774-303">**MAILBOXRULE**: 받은 편지함 규칙에서 아웃 바운드 메시지를 생성 하도록 만든 인바운드 메시지의 **internal_message_id** 값을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-303">**MAILBOXRULE**: Contains the **internal_message_id** value of the inbound message that caused the Inbox rule to generate the outbound message.</span></span>

    <span data-ttu-id="00774-304">다른 이벤트 유형의 경우에는이 필드는 대개 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-304">For other types of events, this field is usually blank.</span></span>

- <span data-ttu-id="00774-305">**return_path**: 메시지를 보낸 **메일** 보낸 사람 명령에 지정 된 반송 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-305">**return_path**: The return email address specified by the **MAIL FROM** command that sent the message.</span></span> <span data-ttu-id="00774-306">이 필드는 비어 있지 않지만로 `<>`표시 되는 null 보낸 사람 주소 값을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-306">Although this field is never empty, it can have the null sender address value represented as `<>`.</span></span>

- <span data-ttu-id="00774-307">**message_info**: 메시지에 대 한 추가 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-307">**message_info**: Additional information about the message.</span></span> <span data-ttu-id="00774-308">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-308">For example:</span></span>

  - <span data-ttu-id="00774-309">이벤트에 대 한 `DELIVER` UTC의 메시지 시작 날짜 및 `SEND` 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-309">The message origination date-time in UTC for `DELIVER` and `SEND` events.</span></span> <span data-ttu-id="00774-310">시작 날짜-시간은 메시지가 처음으로 Exchange Online 조직에 입력 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-310">The origination date-time is the time when the message first entered the Exchange Online organization.</span></span> <span data-ttu-id="00774-311">UTC 날짜 `yyyy-mm-ddThh:mm:ss.fffZ`-시간은 ISO 8601 날짜/시간 형식으로 표시 되며, 여기서 `yyyy` = 년, `mm` = month, `dd` = 일은 시간 구성 요소의 `T` 시작을 `hh` 나타내고 = hour, `mm` = minute, `ss` = second, `fff` =를 나타냅니다. 초의 소수 부분을 나타내고 UTC `Z` 를 `Zulu`표시 하는 또 다른 방법인 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-311">The UTC date-time is represented in the ISO 8601 date-time format: `yyyy-mm-ddThh:mm:ss.fffZ`, where `yyyy` = year, `mm` = month, `dd` = day, `T` indicates the beginning of the time component, `hh` = hour, `mm` = minute, `ss` = second, `fff` = fractions of a second, and `Z` signifies `Zulu`, which is another way to denote UTC.</span></span>

  - <span data-ttu-id="00774-312">인증 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-312">Authentication errors.</span></span> <span data-ttu-id="00774-313">예를 들어, 인증 오류가 발생 했 `11a` 을 때 사용 된 인증의 유형 및 값을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-313">For example, you might see the value `11a` and the type of authentication that was used when the authentication error occurred.</span></span>

- <span data-ttu-id="00774-314">**tenant_id**: Exchange Online 조직 (예를 `39238e87-b5ab-4ef6-a559-af54c6b07b42`들어)을 나타내는 GUID 값입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-314">**tenant_id**: A GUID value that represents the Exchange Online organization (for example, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span></span>

- <span data-ttu-id="00774-315">**original_server_ip**: 원래 서버의 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-315">**original_server_ip**: The IP address of the original server.</span></span>

- <span data-ttu-id="00774-316">**custom_data**: 특정 이벤트 유형과 관련 된 데이터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-316">**custom_data**: Contains data related to specific event types.</span></span> <span data-ttu-id="00774-317">자세한 내용은 다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00774-317">For more information, see the following sections.</span></span>

#### <a name="custom_data-values"></a><span data-ttu-id="00774-318">custom_data 값</span><span class="sxs-lookup"><span data-stu-id="00774-318">custom_data values</span></span>

<span data-ttu-id="00774-319">이벤트의 custom_data 필드는 다양 한 Exchange Online 에이전트에서 메시지 처리 정보를 기록 하는 데 사용 됩니다. \*\*\*\* `AGENTINFO`</span><span class="sxs-lookup"><span data-stu-id="00774-319">The **custom_data** field for an `AGENTINFO` event is used by a variety of Exchange Online agents to log message processing details.</span></span> <span data-ttu-id="00774-320">다음 섹션에서는 보다 흥미로운 에이전트 중 일부에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-320">Some of the more interesting agents are described in the following sections.</span></span>

#### <a name="spam-filter-agent"></a><span data-ttu-id="00774-321">스팸 필터 에이전트</span><span class="sxs-lookup"><span data-stu-id="00774-321">Spam filter agent</span></span>

<span data-ttu-id="00774-322">다음 \*\*\*\* 으로 `S:SFA` 시작 하는 custom_data 값은 스팸 필터 에이전트입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-322">A **custom_data** value that starts with `S:SFA` is from the spam filter agent.</span></span> <span data-ttu-id="00774-323">주요 세부 정보는 다음 표에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-323">The key details are described in the following table:</span></span>

|<span data-ttu-id="00774-324">**값**</span><span class="sxs-lookup"><span data-stu-id="00774-324">**Value**</span></span>|<span data-ttu-id="00774-325">**설명**</span><span class="sxs-lookup"><span data-stu-id="00774-325">**Description**</span></span>|
|:-----|:-----|
|`SFV=NSPM`|<span data-ttu-id="00774-326">메시지가 스팸이 아닌 것으로 표시되었으며 받는 사람에게 전송되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-326">The message was marked as non-spam and was sent to the intended recipients.</span></span>|
|`SFV=SPM`|<span data-ttu-id="00774-327">메시지가 콘텐츠 필터에 의해 스팸으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-327">The message was marked as spam by the content filter.</span></span>|
|`SFV=BLK`|<span data-ttu-id="00774-328">수신 거부된 보낸 사람이 보낸 메시지이므로 필터링을 건너뛰었으며 메시지가 차단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-328">Filtering was skipped and the message was blocked because it originated from a blocked sender.</span></span>|
|`SFV=SKS`|<span data-ttu-id="00774-p153">메시지가 콘텐츠 필터에 의해 처리되기 전에 이미 스팸으로 표시되었습니다. 전송 규칙과 일치하여 스팸으로 자동 표시되고 모든 추가 필터링을 무시하는 메시지가 여기에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-p153">The message was marked as spam prior to being processed by the content filter. This includes messages where the message matched a Transport rule to automatically mark it as spam and bypass all additional filtering.</span></span>|
|`SCL=<number>`|<span data-ttu-id="00774-331">다양 한 SCL 값과 그 의미에 대 한 자세한 내용은 [스팸 신뢰 수준](https://technet.microsoft.com/library/jj200686.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00774-331">For more information about the different SCL values and what they mean, see [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`PCL=<number>`|<span data-ttu-id="00774-332">메시지의 PCL(피싱 지수) 값입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-332">The Phishing Confidence Level (PCL) value of the message.</span></span> <span data-ttu-id="00774-333">스팸 지 수 [수준](https://technet.microsoft.com/library/jj200686.aspx)에 문서화 된 SCL 값과 같은 방식으로 해석 될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-333">These can be interpreted the same way as the SCL values documented in [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`DI=SB`|<span data-ttu-id="00774-334">메시지의 보낸 사람이 차단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-334">The sender of the message was blocked.</span></span>|
|`DI=SQ`|<span data-ttu-id="00774-335">메시지가 격리되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-335">The message was quarantined.</span></span>|
|`DI=SD`|<span data-ttu-id="00774-336">메시지가 삭제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-336">The message was deleted.</span></span>|
|`DI=SJ`|<span data-ttu-id="00774-337">메시지가 받는 사람의 정크 메일 폴더로 전송 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-337">The message was sent to the recipient's Junk Email folder.</span></span>|
|`DI=SN`|<span data-ttu-id="00774-338">메시지가 위험 수준이 높은 배달 풀을 통해 라우팅되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-338">The message was routed through the higher risk delivery pool.</span></span> <span data-ttu-id="00774-339">자세한 내용은 [아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀](https://technet.microsoft.com/library/jj200746.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00774-339">For more information, see [High-risk delivery pool for outbound messages](https://technet.microsoft.com/library/jj200746.aspx).</span></span>|
|`DI=SO`|<span data-ttu-id="00774-340">메시지가 일반 아웃바운드 배달 풀을 통해 라우팅되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-340">The message was routed through the normal outbound delivery pool.</span></span>|
|`SFS=[a]|SFS=[b]`|<span data-ttu-id="00774-341">스팸 규칙이 일치했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="00774-341">This denotes that spam rules were matched.</span></span>|
|`IPV=CAL`|<span data-ttu-id="00774-342">연결 필터의 IP 허용 목록에 IP 주소가 지정되어 있어 메시지가 스팸 필터를 통과하도록 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-342">The message was allowed through the spam filters because the IP address was specified in an IP Allow list in the connection filter.</span></span>|
|`H=<EHLOstring>`|<span data-ttu-id="00774-343">연결 하는 전자 메일 서버의 HELO 또는 EHLO 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-343">The HELO or EHLO string of the connecting email server.</span></span>|
|`PTR=<ReverseDNS>`|<span data-ttu-id="00774-344">보내는 IP 주소의 PTR 레코드로, 역방향 DNS 주소라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="00774-344">The PTR record of the sending IP address, also known as the reverse DNS address.</span></span>|

<span data-ttu-id="00774-345">다음과 같이 스팸을 필터링 한 메시지에 대 한 예제 **custom_data** 값입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-345">An example **custom_data** value for a message that's filtered for spam like this:</span></span>

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a><span data-ttu-id="00774-346">맬웨어 필터 에이전트</span><span class="sxs-lookup"><span data-stu-id="00774-346">Malware filter agent</span></span>

<span data-ttu-id="00774-347">다음 \*\*\*\* 으로 `S:AMA` 시작 하는 custom_data 값은 맬웨어 필터 에이전트입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-347">A **custom_data** value that starts with `S:AMA` is from the malware filter agent.</span></span> <span data-ttu-id="00774-348">주요 세부 정보는 다음 표에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-348">The key details are described in the following table:</span></span>

|<span data-ttu-id="00774-349">**값**</span><span class="sxs-lookup"><span data-stu-id="00774-349">**Value**</span></span>|<span data-ttu-id="00774-350">**설명**</span><span class="sxs-lookup"><span data-stu-id="00774-350">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00774-351">`AMA=SUM|v=1|`사용자나`AMA=EV|v=1`</span><span class="sxs-lookup"><span data-stu-id="00774-351">`AMA=SUM|v=1|` or `AMA=EV|v=1`</span></span>|<span data-ttu-id="00774-352">메시지에 맬웨어가 포함된 것으로 확인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-352">The message was determined to contain malware.</span></span> <span data-ttu-id="00774-353">`SUM`여러 엔진에서 맬웨어를 검색할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="00774-353">`SUM` indicates the malware could've been detected by any number of engines.</span></span> <span data-ttu-id="00774-354">`EV`특정 엔진에 의해 맬웨어가 검색 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="00774-354">`EV` indicates the malware was detected by a specific engine.</span></span> <span data-ttu-id="00774-355">맬웨어가 엔진에서 검색되면 후속 작업이 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-355">When malware is detected by an engine this triggers the subsequent actions.</span></span>|
|`Action=r`|<span data-ttu-id="00774-356">메시지가 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-356">The message was replaced.</span></span>|
|`Action=p`|<span data-ttu-id="00774-357">메시지가 무시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-357">The message was bypassed.</span></span>|
|`Action=d`|<span data-ttu-id="00774-358">메시지가 지연되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-358">The message was deferred.</span></span>|
|`Action=s`|<span data-ttu-id="00774-359">메시지가 삭제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-359">The message was deleted.</span></span>|
|`Action=st`|<span data-ttu-id="00774-360">메시지가 무시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-360">The message was bypassed.</span></span>|
|`Action=sy`|<span data-ttu-id="00774-361">메시지가 무시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-361">The message was bypassed.</span></span>|
|`Action=ni`|<span data-ttu-id="00774-362">메시지가 거부되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-362">The message was rejected.</span></span>|
|`Action=ne`|<span data-ttu-id="00774-363">메시지가 거부되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-363">The message was rejected.</span></span>|
|`Action=b`|<span data-ttu-id="00774-364">메시지가 차단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-364">The message was blocked.</span></span>|
|`Name=<malware>`|<span data-ttu-id="00774-365">검색된 맬웨어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-365">The name of the malware that was detected.</span></span>|
|`File=<filename>`|<span data-ttu-id="00774-366">맬웨어가 포함된 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-366">The name of the file that contained the malware.</span></span>|

<span data-ttu-id="00774-367">맬웨어를 포함 하는 메시지에 대 한 **custom_data** 값 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-367">An example **custom_data** value for a message that contains malware looks like this:</span></span>

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a><span data-ttu-id="00774-368">전송 규칙 에이전트</span><span class="sxs-lookup"><span data-stu-id="00774-368">Transport Rule agent</span></span>

<span data-ttu-id="00774-369">다음 \*\*\*\* 으로`S:TRA` 시작 하는 custom_data 값은 메일 흐름 규칙 (전송 규칙이 라고도 함)에 대 한 전송 규칙 에이전트입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-369">A **custom_data** value that starts with`S:TRA` is from the Transport Rule agent for mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="00774-370">주요 세부 정보는 다음 표에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-370">The key details are described in the following table:</span></span>

|<span data-ttu-id="00774-371">**값**</span><span class="sxs-lookup"><span data-stu-id="00774-371">**Value**</span></span>|<span data-ttu-id="00774-372">**설명**</span><span class="sxs-lookup"><span data-stu-id="00774-372">**Description**</span></span>|
|:-----|:-----|
|`ETR|ruleId=<guid>`|<span data-ttu-id="00774-373">일치된 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-373">The rule ID that was matched.</span></span>|
|`St=<datetime>`|<span data-ttu-id="00774-374">규칙 일치가 발생 한 날짜 및 시간 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-374">The date and time in UTC when the rule match occurred.</span></span>|
|`Action=<ActionDefinition>`|<span data-ttu-id="00774-375">적용된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-375">The action that was applied.</span></span> <span data-ttu-id="00774-376">사용 가능한 작업 목록은 [Mail flow rule actions In Exchange Online](https://technet.microsoft.com/library/jj919237.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00774-376">For a list of available actions, see [Mail flow rule actions in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span></span>|
|`Mode=<Mode>`|<span data-ttu-id="00774-377">규칙의 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="00774-377">The mode of the rule.</span></span> <span data-ttu-id="00774-378">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-378">Valid values are:</span></span> <br/><span data-ttu-id="00774-379">• **적용**: 규칙에 대 한 모든 작업이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00774-379">• **Enforce**: All actions on the rule will be enforced.</span></span> <br/><span data-ttu-id="00774-380">• **정책 팁으로 테스트:**: 모든 정책 설명 작업이 전송 되지만 다른 적용 작업은 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-380">• **Test with Policy Tips:**: Any Policy Tip actions will be sent, but other enforcement actions will not be acted on.</span></span> <br/><span data-ttu-id="00774-381">• **정책 설명이 없는 테스트**: 작업이 로그 파일에 나열 되지만 보낸 사람에 게 어떤 식으로도 알림이 제공 되지 않으며 적용 작업이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-381">• **Test without Policy Tips**: Actions will be listed in a log file, but senders will not be notified in any way, and enforcement actions will not be acted on.</span></span>|

<span data-ttu-id="00774-382">메일 흐름 규칙의 조건과 일치 하는 메시지에 대 한 **custom_data** 값 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00774-382">An example **custom_data** value for a messages that matches the conditions of a mail flow rule looks like this:</span></span>

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`
