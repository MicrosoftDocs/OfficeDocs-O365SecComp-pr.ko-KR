---
title: 보안 & 준수 센터의에서 메시지 추적
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: Admins 보안 & 준수 센터의에서 메시지 추적을 사용 하 여 메시지 셰이프시트에서 알아낼 수 있습니다.
ms.openlocfilehash: 9dfdab4adc5caba55664e93b49c8428791670ab3
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685583"
---
# <a name="message-trace-in-the-security--compliance-center"></a><span data-ttu-id="36e9a-103">보안 & 준수 센터의에서 메시지 추적</span><span class="sxs-lookup"><span data-stu-id="36e9a-103">Message trace in the Security & Compliance Center</span></span>

<span data-ttu-id="36e9a-p101">Exchange Online 조직을 통해 이동 되는 보안 & 준수 센터의에서 메시지 추적 전자 메일 메시지는 다음과 같습니다. 메시지 수신, 거부, 지연, 또는 서비스에 의해 전달 되는 경우를 확인할 수 있습니다. 또한 최종 상태에 도달 하기 전에 메시지에 어떤 작업을 수행 했는지를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p101">Message trace in the Security & Compliance Center follows email messages as they travel through your Exchange Online organization. You can determine if a message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="36e9a-p102">Exchange 관리 센터 (EAC)에서 사용할 수 있었던 메시지 추적에 따라 보안 & 준수 센터의에서 메시지 추적을 향상 시킵니다. 효율적으로 해당 메시지에 셰이프시트에서 변경 하는 방법에 대 한 사용자 질문에 대답, 메일 흐름 문제를 해결 하 고 정책 변경의 유효성을 검사 하는 메시지 추적 정보를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p102">Message trace in the Security & Compliance Center improves upon message trace that was available in the Exchange admin center (EAC). You can use the information from message trace to efficiently answer user questions about what happened to their messages, troubleshoot mail flow issues, and validate policy changes.</span></span>

## <a name="open-message-trace"></a><span data-ttu-id="36e9a-109">열린 메시지 추적</span><span class="sxs-lookup"><span data-stu-id="36e9a-109">Open message trace</span></span>

1. <span data-ttu-id="36e9a-110">회사 또는 학교 계정로 [Office 365에 로그인](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4)합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-110">[Sign in to Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span>

2. <span data-ttu-id="36e9a-111">왼쪽 위에서 앱 시작 관리자 아이콘 ![Office 365 앱 시작 관리자 아이콘](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png)을 선택하고 **관리자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-111">Select the app launcher icon ![Office 365 app launcher icon](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in the upper-left and choose **Admin**.</span></span>

3. <span data-ttu-id="36e9a-112">왼쪽 탐색 영역에서 **관리 센터** 를 확장 하 고 **보안 & 규정 준수를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-112">In the lower-left navigation, expand **Admin centers** and select **Security & Compliance**.</span></span>

4. <span data-ttu-id="36e9a-113">표시 되는 **보안 & 준수** 페이지에서 **메일 흐름**확장 하 고 **메시지 추적**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-113">In the **Security & Compliance** page that opens, expand **Mail flow**, and select **Message trace**.</span></span>

## <a name="message-trace-page"></a><span data-ttu-id="36e9a-114">메시지 추적 페이지</span><span class="sxs-lookup"><span data-stu-id="36e9a-114">Message trace page</span></span>

<span data-ttu-id="36e9a-p103">여기에서 **추적을 시작** 단추를 클릭 하 여 새 기본 추적을 시작할 수 있습니다. 이 검색할 모든 메시지에 대 한 모든 보낸사람 및 받는 사람에 대 한 마지막 2 일. 사용 가능한 쿼리 범주에서 저장 된 쿼리 중 하나를 사용 하 고으로 실행 하거나 또는-시작 쿼리를 직접 지점으로이 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p103">From here you can start a new default trace by clicking on the **Start a trace** button. This will search for all messages for all senders and recipients for the last two days. Or you can use one of the stored queries from the available query categories and either run them as-is or use them as starting points for your own queries:</span></span>

- <span data-ttu-id="36e9a-118">**기본 쿼리**: Office 365에서 제공 하는 기본 제공 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-118">**Default queries**: Built-in queries provided by Office 365.</span></span>

- <span data-ttu-id="36e9a-119">**사용자 정의 쿼리**: 쿼리 나중에 사용 하면 조직에서 관리자가 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-119">**Custom queries**: Queries saved by admins in your organization for future use.</span></span>

- <span data-ttu-id="36e9a-p104">**자동 저장 된 쿼리**: 마지막 10은 가장 최근에 쿼리를 실행 합니다. 이 목록을 사용 하면 간단 하 게 중지 했던 듭니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p104">**Autosaved queries**: The last ten most recently run queries. This list makes it simple to pick up where you left off.</span></span>

<span data-ttu-id="36e9a-122">또한이 페이지에는 **Downloadable 보고서** 섹션 보고서 자체는 물론 사용자가 제출한 요청에 대 한 다운로드 하기 위해 사용할 수 없을 때.</span><span class="sxs-lookup"><span data-stu-id="36e9a-122">Also on this page is a **Downloadable reports** section for the requests you've submitted, as well as the reports themselves when they're are available for download.</span></span>

## <a name="options-for-a-new-message-trace"></a><span data-ttu-id="36e9a-123">새 메시지 추적에 대 한 옵션</span><span class="sxs-lookup"><span data-stu-id="36e9a-123">Options for a new message trace</span></span>

### <a name="filter-by-senders-and-recipients"></a><span data-ttu-id="36e9a-124">보낸사람 및 받는 사람으로 필터링</span><span class="sxs-lookup"><span data-stu-id="36e9a-124">Filter by senders and recipients</span></span>

<span data-ttu-id="36e9a-125">기본 값은 **모든 보낸사람** 및 **받는 사람을 모두**하지만 다음 필드를 사용 하 여 결과 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-125">The default values are **All senders** and **All recipients**, but you can use the following fields to filter the results:</span></span>

- <span data-ttu-id="36e9a-p105">**이러한 사용자가**: 조직에서 하나 이상의 보낸사람을 선택 하려면이 필드에서를 클릭 합니다. 이름을 입력을 시작할 수 있습니다 하 고 목록에서 항목 입력 한 내용을, 훨씬 검색 페이지를 작동 하는 방식을 같은 의해 필터링 될 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p105">**By these people**: Click in this field to select one or more senders from your organization. You can also start to type a name and the items in the list will be filtered by what you've typed, much like how a search page behaves.</span></span>

- <span data-ttu-id="36e9a-128">**이러한 사람에 게**: 하나 이상의 받는 사람을 선택 하면 조직에서이 필드에서를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-128">**To these people**: Click in this field to select one or more recipients in your organization.</span></span>

<span data-ttu-id="36e9a-p106">또한 외부 보낸사람 및 받는 사람에 게 전자 메일 주소를 입력할 수 있습니다. 와일드 카드는 지원 (`*@contoso.com` 또는 `scot?@contoso.com`), 있지만 동시에 같은 필드에 여러 와일드 카드 항목을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p106">You can also type the email addresses of external senders and recipients. Wildcards are supported (`*@contoso.com` or `scot?@contoso.com`), but you can't use multiple wildcard entries in the same field at the same time.</span></span>

### <a name="time-range"></a><span data-ttu-id="36e9a-131">시간 범위</span><span class="sxs-lookup"><span data-stu-id="36e9a-131">Time range</span></span>

<span data-ttu-id="36e9a-p107">기본값은 **일**, 하지만 최대 90 일의 날짜/시간 범위를 지정할 수 있습니다. 날짜/시간 범위를 사용 하면 이러한 문제를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p107">The default value is **2 days**, but you can specify date/time ranges of up to 90 days. When you use date/time ranges, consider these issues:</span></span>

- <span data-ttu-id="36e9a-p108">기본적으로 시간 표시 막대를 사용 하 여 **슬라이더** 보기에서 시간 범위를 선택 합니다. 만 일을 선택 하거나 시간 표시 되는 설정을 수 있습니다. 시작/종료 거품에 맞춰집니다 중간 값을 선택 하는 동안 가장 가까운 설정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p108">By default, you select the time range in **Slider** view using a time line. You can only select the day or time settings that are displayed. Trying to select an in-between value will snap the start/end bubble to the nearest displayed setting.</span></span>

   ![보안 & 준수 센터에서에서 새 메시지 추적에 슬라이더 시간 범위](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   <span data-ttu-id="36e9a-p109">하지만 여기서 (시간 포함), **시작 날짜와** **종료 날짜** 값을 지정할 수 및 날짜/시간 범위에 대 한 **표준 시간대** 를 선택할 수도 있습니다 **사용자 정의** 보기를 전환할 수 있습니다. 쿼리 입력 및 쿼리 결과 모두 적용 하는 **표준 시간대** 설정 하는 내용의 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p109">But, you can also switch to **Custom** view where you can specify the **Start date** and **End date** values (including times), and you can also select the **Time zone** for the date/time range. Note that the **Time zone** setting applies to both your query inputs and your query results.</span></span>

   ![보안 & 준수 센터에서에서 새 메시지 추적에는 사용자 정의 시간 범위](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   <span data-ttu-id="36e9a-p110">10 일 이하인, 결과 **요약** 보고서로 즉시 사용할 수 있습니다. 10 일 보다 약간 더 큰 시간 범위를 지정 하는 경우에 다운로드 가능한 CSV 파일 ( **향상 된 요약** 또는 **확장 된** 보고서)으로 사용할 수 있는 결과 지연 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p110">For 10 days or less, the results are available instantly as a **Summary** report. If you specify a time range that's even slightly greater than 10 days, the results will be delayed as they are only available as a downloadable CSV file ( **Enhanced summary** or **Extended** reports).</span></span>

   <span data-ttu-id="36e9a-143">다른 보고서 유형에 대 한 자세한 내용은이 항목의 [보고서 형식 선택](#choose-report-type) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-143">For more information about the different report types, see the [Choose report type](#choose-report-type) section in this topic.</span></span>

   <span data-ttu-id="36e9a-p111">**참고**: 향상 된 요약 및 확장 된 보고서는 보관 된 메시지 추적 데이터를 사용 하 여 사용 되 고 보고서를 다운로드할 수 있는 하기 전에 몇 시간까지 걸릴 수 있으므로 합니다. 다른 얼마나 많은 관리자가 같은 시간 주위 보고서 요청 제출도 따라 큐에 대기 중인된 요청에 대 한 처리를 시작 하기 전에 지연을 또한 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p111">**Note**: Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available for download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before processing starts for your queued request.</span></span>

- <span data-ttu-id="36e9a-p112">상대 시간 범위 (예: 오늘부터 3 일)을 저장 **슬라이더** 보기에서 쿼리를 저장 합니다. 쿼리를 **사용자 지정** 보기에 저장 하면 절대 날짜/시간 범위 (예: 2018-05-06 13 시 2018-05-08-18시).</span><span class="sxs-lookup"><span data-stu-id="36e9a-p112">Saving a query in **Slider** view saves the relative time range (for example, 3 days from today). Saving a query in **Custom** view saves the absolute date/time range (for example, 2018-05-06 13:00 to 2018-05-08 18:00).</span></span>

### <a name="more-search-options"></a><span data-ttu-id="36e9a-148">더 많은 검색 옵션</span><span class="sxs-lookup"><span data-stu-id="36e9a-148">More search options</span></span>

#### <a name="delivery-status"></a><span data-ttu-id="36e9a-149">배달 상태</span><span class="sxs-lookup"><span data-stu-id="36e9a-149">Delivery status</span></span>

<span data-ttu-id="36e9a-150">**모든** 옵션을 선택 기본값 두거나 결과 필터링 하는 다음 값 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-150">You can leave the default value **All** selected, or you can select one of the following values to filter the results:</span></span>

- <span data-ttu-id="36e9a-151">**배달 된**: 메시지가 의도 한 대상에 배달 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-151">**Delivered**: The message was successfully delivered to the intended destination.</span></span>

- <span data-ttu-id="36e9a-152">**보류 중인**: 되 고 해당 메시지의 배달이 시도 중이거나 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-152">**Pending**: Delivery of the message is being attempted or re-attempted.</span></span>

- <span data-ttu-id="36e9a-153">**전체 확장**: 메일 그룹 받는 사람 그룹의 개별 구성원에 게 배달 전에 확장 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-153">**Expanded**: A distribution group recipient was expanded before delivery to the individual members of the group.</span></span>

- <span data-ttu-id="36e9a-154">**실패**: 메시지가 배달 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-154">**Failed**: The message was not delivered.</span></span>

- <span data-ttu-id="36e9a-p113">**격리 된**: (스팸, 대량 메일 또는 피싱)로 격리 된 메시지입니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 격리를](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p113">**Quarantined**: The message was quarantined (as spam, bulk mail, or phishing). For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span></span>

- <span data-ttu-id="36e9a-157">**스팸 필터링 됨**: 메시지가 스팸을 식별 하 고 거부 되었거나 (하지 격리 된)를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-157">**Filtered as spam**: The message was identified spam, and was rejected or blocked (not quarantined).</span></span>

- <span data-ttu-id="36e9a-p114">**상태:** Office 365에서 메시지를 받은 최근에 하지만 다른 상태 데이터가 없는 아직 사용할 수 있습니다. 잠시 후에 다시 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p114">**Getting status:** The message was recently received by Office 365, but no other status data is yet available. Check back in a few minutes.</span></span>

<span data-ttu-id="36e9a-p115">**참고**: **보류 중인,** **격리 된**및 **스팸이 필터** 값만 사용할 수 검색에 대 한 일 보다 작은 합니다. 또한 있을 수 있습니다 5 ~ 10 분 지연 실제 및 보고 된 배달 상태 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p115">**Note**: The values **Pending,** **Quarantined**, and **Filter as spam** are only available for searches less than 10 days. Also, there might be a 5 to 10 minute delay between the actual and reported delivery status.</span></span>

#### <a name="message-id"></a><span data-ttu-id="36e9a-162">메시지 ID</span><span class="sxs-lookup"><span data-stu-id="36e9a-162">Message ID</span></span>

<span data-ttu-id="36e9a-p116">이것은에서 발견 되는 인터넷 메시지 ID (클라이언트 ID 라고도 함)는 **메시지 ID:** 메시지 헤더의 헤더 필드입니다. 사용자가 특정 메시지를 조사 하이 값을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p116">This is the internet message ID (also known as the Client ID) that's found in the **Message-ID:** header field in the message header. Users can give you this value to investigate specific messages.</span></span>

<span data-ttu-id="36e9a-p117">이 값은 메시지의 수명 동안 상수입니다. Office 365 또는 Exchange에서 만든 메시지,이 속성 값은 형식에서 `<GUID@ServerFQDN>`, 꺾쇠 괄호를 포함 하 여 (\< \>). 예, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`합니다. 다른 메시징 시스템 다른 구문 또는 값을 사용할 수 있습니다. 이 값은 고유 하지만 일부 전자 메일 시스템은 엄격 하 게이 요구 사항을 준수. 하는 경우는 **메시지 ID:** 헤더 필드 내 존재 하지 않거나 외부 원본에서 들어오는 메시지에 대 한 비어는 임의의 값이 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p117">This value is constant for the lifetime of the message. For messages created in Office 365 or Exchange, the value is in the format `<GUID@ServerFQDN>`, including the angle brackets (\< \>). For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Other messaging systems might use different syntax or values. This value is supposed to be unique, but not all email systems strictly follow this requirement. If the **Message-ID:** header field doesn't exist or is blank for incoming messages from external sources, an arbitrary value is assigned.</span></span>

<span data-ttu-id="36e9a-171">**메시지 ID** 를 사용 하 여 결과 필터링 하는 꺾쇠 괄호를 포함 하 여 전체 문자열을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-171">When you use **Message ID** to filter the results, be sure to include the full string, including any angle brackets.</span></span>

#### <a name="direction"></a><span data-ttu-id="36e9a-172">Direction</span><span class="sxs-lookup"><span data-stu-id="36e9a-172">Direction</span></span>

<span data-ttu-id="36e9a-173">**모두** 선택 하 고, 기본값을 남길 수 또는 (조직의 받는 사람에에서 게 보내는 메시지) **인바운드** 또는 **아웃 바운드** (조직의 사용자가 보낸 메시지가)을 선택할 수 있습니다는 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-173">You can leave the default value **All** selected, or you can select **Inbound** (messages sent to recipients in your organization) or **Outbound** (messages sent from users in your organization) to filter the results.</span></span>

#### <a name="original-client-ip-address"></a><span data-ttu-id="36e9a-174">원래 클라이언트 IP 주소</span><span class="sxs-lookup"><span data-stu-id="36e9a-174">Original client IP address</span></span>

<span data-ttu-id="36e9a-p118">하 여 필터 결과 클라이언트 IP 주소를 전송 하는 많은 양의 스팸 또는 맬웨어로 해킹된 컴퓨터를 조사 합니다. 여러 사람이 보낸에서 수신 메시지가 나타날 수 있습니다, 하지만 같은 컴퓨터의 모든 메시지를 생성은 가능성이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p118">You can filer the results by client IP address to investigate hacked computers that are sending large amounts of spam or malware. Although the messages might appear to come from multiple senders, it's likely that the same computer is generating all of the messages.</span></span>

<span data-ttu-id="36e9a-177">**참고**: 클라이언트 IP 주소 정보만 사용할 수 있는 10 일 이며만 **향상 된 요약** 또는 **확장 된** 보고서 (다운로드 가능한 CSV 파일)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-177">**Note**: The client IP address information is only available for 10 days, and is only available in the **Enhanced summary** or **Extended** reports (downloadable CSV files).</span></span>

### <a name="choose-report-type"></a><span data-ttu-id="36e9a-178">보고서 유형 선택</span><span class="sxs-lookup"><span data-stu-id="36e9a-178">Choose report type</span></span>

<span data-ttu-id="36e9a-179">사용 가능한 보고서 유형은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-179">The available report types are:</span></span>

- <span data-ttu-id="36e9a-p119">**요약**: 시간 범위 10 일 보다 작은 요소 이며 추가 필터링 옵션이 없습니다 필요 하는 경우에 사용할 수 있습니다. **검색**을 클릭 한 후에 곧바로 결과 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p119">**Summary**: Available if the time range is less than 10 days, and requires no additional filtering options. The results are available almost immediately after you click **Search**.</span></span>

- <span data-ttu-id="36e9a-p120">**향상 된 요약** 이나 **Extended**: 이러한 보고서는 다운로드 가능한 CSV 파일로 사용할 수만 하 고 시간 범위에 관계 없이 필터링 다음 옵션 중 하나 이상이 필요: **이러한 사용자가**, **이러한 사람에 게**사람 또는 \*\* 메시지 ID\*\*합니다. 보낸사람 또는 받는 사람에 대 한 와일드 카드를 사용할 수 있습니다 (예를들어, \*@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="36e9a-p120">**Enhanced summary** or **Extended**: These reports are only available as downloadable CSV files, and require one or more of the following filtering options regardless of the time range: **By these people**, **To these people**, or **Message ID**. You can use wildcards for the senders or the recipients (for example, \*@contoso.com).</span></span>

<span data-ttu-id="36e9a-184">**참고:**</span><span class="sxs-lookup"><span data-stu-id="36e9a-184">**Notes**:</span></span>

- <span data-ttu-id="36e9a-p121">향상 된 요약 및 확장 된 보고서는 보관 된 메시지 추적 데이터를 사용 하 여 사용 되 고 보고서가 다운로드를 사용할 수 있는 전에 몇 시간까지 걸릴 수 있으므로 합니다. 다른 얼마나 많은 관리자가 같은 시간 주위 보고서 요청 제출도 따라 처리 큐에 대기 중인된 요청을 시작 하기 전에 지연을 또한 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p121">Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available to download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before your queued request starts to be processed.</span></span>

- <span data-ttu-id="36e9a-187">선택할 수 있습니다. 하는 동안 같은 향상 된 요약 또는 확장 된 보고서를 날짜/시간 범위, 일반적으로 보관 된 데이터의 마지막 4 시간 되지 않습니다 아직 이러한 두 종류의 보고서에 대해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-187">While you can select an Enhanced summary or Extended report for any date/time range, commonly the last four hours of archived data will not yet be available for these two types of reports.</span></span>

<span data-ttu-id="36e9a-p122">요약 페이지를 선택한 필터링 옵션을 나열 하는 보고서 및 메시지 추적 (도 편집, 완료 될 때 알림을 수신 하는 전자 메일 주소에 대 한 고유 (편집) 제목 발표자는 **다음**을 클릭 하는 경우 및 조직의 허용된 도메인 중 하나 여야 합니다). 메시지 추적을 전송 하도록 **준비 보고서** 클릭 합니다. 주에서 **메시지 추적** 페이지 **Downloadable 보고** 섹션에서 보고서의 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p122">When you click **Next**, you're presented with a summary page that lists the filtering options that you selected, a unique (editable) title for the report, and the email address that receives the notification when the message trace completes (also editable, and must be in one of your organization's accepted domains). Click **Prepare report** to submit the message trace. On the main **Message trace** page, you can see the status of the report in the **Downloadable reports** section.</span></span>

<span data-ttu-id="36e9a-191">다른 보고서 종류에서 반환 되는 정보에 대 한 자세한 내용은 다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-191">For more information about the information that's returned in the different report types, see the next section.</span></span>

## <a name="message-trace-results"></a><span data-ttu-id="36e9a-192">메시지 추적 결과</span><span class="sxs-lookup"><span data-stu-id="36e9a-192">Message trace results</span></span>

<span data-ttu-id="36e9a-p123">다른 보고서 형식은 다양 한 수준의 정보를 반환합니다. 다양 한 보고서에서 사용할 수 있는 정보는 다음 섹션에 설명 되어있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p123">The different report types return different levels of information. The information that's available in the different reports is described in the following sections.</span></span>

### <a name="summary-report-output"></a><span data-ttu-id="36e9a-195">요약 보고서 출력</span><span class="sxs-lookup"><span data-stu-id="36e9a-195">Summary report output</span></span>

<span data-ttu-id="36e9a-196">메시지 추적을 실행 한 후 결과 나열, 날짜/시간 (가장 최근의 것부터)를 내림차순으로 정렬 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-196">After running the message trace, the results will be listed, sorted by descending date/time (most recent first).</span></span>

![보안 & 준수 센터의에서 메시지 추적에 대 한 요약 보고서 결과](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

<span data-ttu-id="36e9a-198">요약 보고서는 다음과 같은 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-198">The summary report contains the following information:</span></span>

- <span data-ttu-id="36e9a-199">**날짜**: 구성 된 UTC 표준 시간대를 사용 하 여 서비스에서 메시지를 받은 시간과 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-199">**Date**: The date and time at which the message was received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="36e9a-200">**보낸사람**: 보낸 사람의 전자 메일 주소 (*별칭*@*도메인*).</span><span class="sxs-lookup"><span data-stu-id="36e9a-200">**Sender**: The email address of the sender (*alias*@*domain*).</span></span>

- <span data-ttu-id="36e9a-p124">**받는 사람**: 전자 메일 주소를 받는 사람이 나 받는 사람입니다. 여러 받는 사람에 게 보낸 메시지를 받는 사람 당한 줄이 있습니다. 받는 사람이 메일 그룹, 동적 메일 그룹 또는 메일 사용이 가능한 보안 그룹 경우 그룹 첫번째 받는 사람 수와 별도 줄에는 그룹의 각 구성원은 다음 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p124">**Recipient**: The email address of the recipient or recipients. For a message sent to multiple recipients, there's one line per recipient. If the recipient is a distribution group, dynamic distribution group, or mail-enabled security group, the group will be the first recipient, and then each member of the group is on a separate line.</span></span>

- <span data-ttu-id="36e9a-204">**제목**: 메시지의 처음 256 자 **제목:** 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-204">**Subject**: The first 256 characters of the message's **Subject:** field.</span></span>

- <span data-ttu-id="36e9a-205">**상태**:이 값은 [배달 상태](#delivery-status) 섹션에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-205">**Status**: These values are described in the [Delivery status](#delivery-status) section.</span></span>

<span data-ttu-id="36e9a-p125">기본적으로 처음 250 결과 로드 하 고 쉽게 사용할 수 있습니다. 아래로 스크롤할 때 약간의 일시 중지에는 결과의 다음 일괄 처리 로드 됩니다. 스크롤을 하는 대신 10, 000 개 있는 최대 결과의 모든 부하를 **모두 로드** 를 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p125">By default, the first 250 results are loaded and readily available. When you scroll down, there's a slight pause as the next batch of results are loaded. Instead of scrolling, you can click **Load all** to load all of the results up to a maximum of 10,000.</span></span>

<span data-ttu-id="36e9a-209">오름차순 또는 내림차순으로 정렬 해당 열의 값을 기준으로 결과 정렬 하려면 열 머리글을 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-209">You can click on the column headers to sort the results by the values in that column in ascending or descending order.</span></span>

<span data-ttu-id="36e9a-210">하나 이상의 열을 기준으로 결과 필터링 하려면 **필터 결과** 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-210">You can click **Filter results** to filter the results by one or more columns.</span></span>

<span data-ttu-id="36e9a-211">**결과 내보내기** 를 클릭 한 다음 **모든 결과 내보낼**, **내보내기 결과 로드**또는 **선택한 내보내기**을 선택 하 여 하나 이상의 행을 선택한 후 결과 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-211">You can export the results after you've selected one or more rows by clicking **Export results** and then selecting **Export all results**, **Export loaded results**, or **Export selected**.</span></span>

#### <a name="find-related-records-for-this-message"></a><span data-ttu-id="36e9a-212">이 메시지에 대 한 관련된 레코드 찾기</span><span class="sxs-lookup"><span data-stu-id="36e9a-212">Find related records for this message</span></span>

<span data-ttu-id="36e9a-p126">관련된 메시지 레코드는 동일한 메시지 ID를 공유 하는 레코드 기억 두 사용자 간에 보낸 단일 메시지 여러 레코드를 생성할 수 있습니다. 레코드 수가 메시지는 메일 그룹 확장, 전달, 메일 흐름 규칙 (전송 규칙이 라고도 함)에 의해 영향을 받을 때 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p126">Related message records are records that shared the same Message ID. Remember, even a single message sent between two people can generate multiple records. The number of records increases when the message is affected by distribution group expansion, forwarding, mail flow rules (also known as transport rules), etc.</span></span>

<span data-ttu-id="36e9a-216">나타나는 **찾기 관련** 단추를 클릭 하 여 또는 **기타 옵션** 을 선택 하 여 메시지에 대 한 관련된 레코드를 찾을 수 있는 행의 확인란을 선택한 후 ![더 많은](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **이 메시지에 대 한 관련된 레코드 찾기**).</span><span class="sxs-lookup"><span data-stu-id="36e9a-216">After you select a row's check box, you can find related records for the message by clicking the **Find related** button that appears, or by selecting **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Find related records for this message**).</span></span>

<span data-ttu-id="36e9a-217">메시지 ID에 대 한 자세한 내용은이 항목의 앞부분에서 메시지 ID 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-217">For more information about the Message ID, see the Message ID section earlier in this topic.</span></span>

#### <a name="message-trace-details"></a><span data-ttu-id="36e9a-218">메시지 추적 세부 정보</span><span class="sxs-lookup"><span data-stu-id="36e9a-218">Message trace details</span></span>

<span data-ttu-id="36e9a-219">요약 보고서 출력에는 다음 방법 중 하나를 사용 하 여 메시지에 대 한 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-219">In the summary report output, you can view details about a message by using either of the following methods:</span></span>

- <span data-ttu-id="36e9a-220">(확인란을 제외한 행의 아무곳 이나 클릭) 하는 행을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-220">Select the row (click anywhere in the row except the check box).</span></span>

- <span data-ttu-id="36e9a-221">행의 확인란을 선택 하 고 **기타 옵션** 을 클릭 ![더 많은](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **메시지 세부 정보 보기**입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-221">Select the row's check box and click **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **View message details**.</span></span>

   ![보안 & 준수 센터의에서 요약 보고서 메시지 추적 결과에 행을 두번클릭 한 후 세부 정보](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

<span data-ttu-id="36e9a-223">요약 보고서에 존재 하지 않는 다음과 같은 추가 정보를 포함 하는 메시지 추적 세부 정보:</span><span class="sxs-lookup"><span data-stu-id="36e9a-223">The message trace details contain the following additional information that's not present in the summary report:</span></span>

- <span data-ttu-id="36e9a-p127">**이벤트 메시지**:이 섹션에서는 메시지에는 서비스에서 수행 되는 작업을 분류 하는 데 도움이 되는 분류 합니다. 발생할 수 있는 유용한 이벤트는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p127">**Message events**: This section contains classifications that help categorize the actions that the service takes on messages. Some of the more interesting events that you might encounter are:</span></span>

   - <span data-ttu-id="36e9a-226">**수신**: 서비스에서 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-226">**Receive**: The message was received by the service.</span></span>

   - <span data-ttu-id="36e9a-227">**보내기**: 서비스에서 메시지를 보냈습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-227">**Send**: The message was sent by the service.</span></span>

   - <span data-ttu-id="36e9a-228">**실패**: 메시지 배달 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-228">**Fail**: The message failed to be delivered.</span></span>

   - <span data-ttu-id="36e9a-229">**제공**: 메시지를 사서함으로 배달 했습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-229">**Deliver**: The message was delivered to a mailbox.</span></span>

   - <span data-ttu-id="36e9a-230">**확장**: 확장 된 메일 그룹에 메시지를 보냈습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-230">**Expand**: The message was sent to a distribution group that was expanded.</span></span>

   - <span data-ttu-id="36e9a-231">**전송**: 콘텐츠 변환, 메시지 받는 사람 수 제한 또는 에이전트로 인해 받는 사람이 분기 된 메시지로 이동 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-231">**Transfer**: Recipients were moved to a bifurcated message because of content conversion, message recipient limits, or agents.</span></span>

   - <span data-ttu-id="36e9a-232">**지연**: 메시지 배달이 연기 하 고 나중에 다시 시도 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-232">**Defer**: The message delivery was postponed and might be re-attempted later.</span></span>

   - <span data-ttu-id="36e9a-p128">**해결 됨**: 메시지는 Active Directory 조회에 따라 새 받는 사람 주소로 리디렉션 되었습니다. 이 경우 원래 받는 사람 주소는 메시지에 대 한 마지막 배달 상태 메시지 추적에 별도 행에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p128">**Resolved**: The message was redirected to a new recipient address based on an Active Directory look up. When this happens, the original recipient address is listed in a separate row in the message trace along with the final delivery status for the message.</span></span>

   <span data-ttu-id="36e9a-235">참고를 성공적으로 배달 되는 일반적인 메시지에도 메시지 추적에 여러 **이벤트** 항목을 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-235">Note that even an uneventful message that's successfully delivered will generate multiple **Event** entries in the message trace.</span></span>

- <span data-ttu-id="36e9a-236">**자세한 내용**은:이 섹션에서는 다음과 같은 세부 정보:</span><span class="sxs-lookup"><span data-stu-id="36e9a-236">**More information**: This section contains the following details:</span></span>

   - <span data-ttu-id="36e9a-p129">**메시지 ID**:이 값이이 항목의 앞부분에서 [메시지 ID](#message-id) 섹션에서 설명 합니다. 예, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p129">**Message ID**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

   - <span data-ttu-id="36e9a-239">**메시지 크기**</span><span class="sxs-lookup"><span data-stu-id="36e9a-239">**Message size**</span></span>

   - <span data-ttu-id="36e9a-p130">**IP**: 메시지를 전송 하는 컴퓨터의 IP 주소입니다. Exchange Online에서 보낸 아웃 바운드 메시지에 대 한이 값은 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p130">**From IP**: The IP address of the computer that sent the message. For outbound messages sent from Exchange Online, this value is blank.</span></span>

   - <span data-ttu-id="36e9a-p131">**IP**: IP 주소를 하나 이상 서비스 있는 메시지를 배달 하려고 합니다. 메시지에 여러 받는 사람, 이러한 표시 됩니다. Exchange Online으로 보내는 인바운드 메시지에 대 한이 값은 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p131">**To IP**: The IP address or addresses where the service attempted to deliver the message. If the message has multiple recipients, these are displayed. For inbound messages sent to Exchange Online, this value is blank.</span></span>

### <a name="enhanced-summary-reports"></a><span data-ttu-id="36e9a-245">향상 된 요약 보고서</span><span class="sxs-lookup"><span data-stu-id="36e9a-245">Enhanced summary reports</span></span>

<span data-ttu-id="36e9a-p132">사용 가능한 (완료) 향상 된 요약 보고서는 시작 메시지 추적에 **Downloadable 보고** 섹션에서 사용할 수 있습니다. 다음 정보는 보고서에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p132">Available (completed) Enhanced summary reports are available in the **Downloadable reports** section at the beginning message trace. The following information is available in the report:</span></span>

- <span data-ttu-id="36e9a-248">**origin_timestamp**<sup>\*</sup>: 날짜 및 시간 메시지에 처음으로 구성 된 UTC 표준 시간대를 사용 하 여 서비스를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-248">**origin_timestamp**<sup>\*</sup>: The date and time when the message was initially received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="36e9a-249">**sender_address 사람의**: 보낸 사람의 전자 메일 주소 (*별칭*@*도메인*).</span><span class="sxs-lookup"><span data-stu-id="36e9a-249">**sender_address**: The sender's email address (*alias*@*domain*).</span></span>

- <span data-ttu-id="36e9a-p133">**Recipient_status**: 받는 사람에 게 메시지의 배달 상태입니다. 모든 받는 사람 및 해당 상태 각 형식에서에 대 한 표시 됩니다 여러 받는 사람에 게 메시지를 보냈습니다, 하는 경우: \< *전자 메일 주소*\>##\<*상태*\>합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="36e9a-p133">**Recipient_status**: The status of the delivery of the message to the recipient. If the message was sent to multiple recipients, it will show all the recipients and the corresponding status for each, in the format: \<*email address*\>##\<*status*\>. For example:</span></span>

   - <span data-ttu-id="36e9a-253">**##Receive, 보내기** 메시지가 서비스에 의해 받았으며 의도 한 대상으로 전송 된 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-253">**##Receive, Send** means the message was received by the service and was sent to the intended destination.</span></span>

   - <span data-ttu-id="36e9a-254">**##Receive, 실패** 서비스 하지만 실패 의도 한 대상에 배달 된 메시지를 수신한 하는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-254">**##Receive, Fail** means the message was received by the service but delivery to the intended destination failed.</span></span>

   - <span data-ttu-id="36e9a-255">메시지 서비스에 의해 받았으며 받는 사람의 사서함으로 배달 했습니다 의미 **##Receive를 제공** 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-255">**##Receive, Deliver** means the message was received by the service and was delivered to the recipient's mailbox.</span></span>

- <span data-ttu-id="36e9a-256">**message_subject**: 메시지의 **제목** 필드의 처음 256 자입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-256">**message_subject**: The first 256 characters of the message's **Subject** field.</span></span>

- <span data-ttu-id="36e9a-257">**total_bytes**: 첨부 파일을 포함 하 여 바이트에서 메시지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-257">**total_bytes**: The size of the message in bytes, including attachments.</span></span>

- <span data-ttu-id="36e9a-p134">**message_id**:이 값이이 항목의 앞부분에서 [메시지 ID](#message-id) 섹션에서 설명 합니다. 예, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p134">**message_id**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

- <span data-ttu-id="36e9a-p135">**network_message_id**: 분기 또는 메일 그룹 확장으로 인해 만들 수 있는 메시지의 모든 복사본에서 유지 하는 고유한 메시지 ID 값입니다. 예제 값은 `1341ac7b13fb42ab4d4408cf7f55890f`합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p135">**network_message_id**: A unique message ID value that persists across all copies of the message that might be created due to bifurcation or distribution group expansion. An example value is `1341ac7b13fb42ab4d4408cf7f55890f`.</span></span>

- <span data-ttu-id="36e9a-262">**original_client_ip**: 보낸 사람의 클라이언트의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-262">**original_client_ip**: The IP address of the sender's client.</span></span>

- <span data-ttu-id="36e9a-263">**directionality**: 여부는 메시지에 전송 된 인바운드 (1) 조직 또는 여부 아웃 바운드 (2)에서 보낸 조직을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-263">**directionality**: Indicates whether the message was sent inbound (1) to your organization, or whether it was sent outbound (2) from your organization.</span></span>

- <span data-ttu-id="36e9a-p136">**connector_id**: 원본 또는 대상 커넥터의 이름입니다. Exchange Online에서 커넥터에 대 한 자세한 내용은 [Office 365의 커넥터를 사용 하 여 구성을 메일 흐름](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p136">**connector_id**: The name of the source or destination connector. For more information about connectors in Exchange Online, see [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span></span>

- <span data-ttu-id="36e9a-266">**delivery_priority**<sup>\*</sup>: **높음**, **낮음**또는 **보통** 우선순위는 메시지를 보냈습니다 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-266">**delivery_priority**<sup>\*</sup>: Whether the message was sent with **High**, **Low**, or **Normal** priority.</span></span>

<span data-ttu-id="36e9a-267"><sup>\*</sup>이 속성은 향상 된 요약 보고서에서 사용할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-267"><sup>\*</sup>These properties are only available in Enhanced summary reports.</span></span>

### <a name="extended-reports"></a><span data-ttu-id="36e9a-268">확장 된 보고서</span><span class="sxs-lookup"><span data-stu-id="36e9a-268">Extended reports</span></span>

<span data-ttu-id="36e9a-p137">사용 가능한 (완료) Extended 보고서는 메시지 추적의 시작 부분에 **Downloadable 보고** 섹션에서 사용할 수 있습니다. 향상 된 요약 보고서에서 정보를 모두 거의 모든 (제외 하 고 **origin_timestamp** 및 **delivery_priority**)는 확장 된 보고서에서 제공 됩니다. 다음과 같은 추가 정보는 에서만 확장 된 보고서를 사용할 수 있습니다:</span><span class="sxs-lookup"><span data-stu-id="36e9a-p137">Available (completed) Extended reports are available in the **Downloadable reports** section at the beginning of message trace. Virtually all of the information from an Enhanced summary report is available in an Extended report (with the exception of **origin_timestamp** and **delivery_priority**). The following additional information is only available in an Extended report:</span></span>

- <span data-ttu-id="36e9a-272">**client_ip**: 전자 메일 서버 또는 메시지를 전송 하는 메시징 클라이언트의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-272">**client_ip**: The IP address of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="36e9a-273">**client_hostname**: 호스트 이름 또는 전자 메일 서버 또는 메시지를 전송 하는 메시징 클라이언트의 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-273">**client_hostname**: The host name or FQDN of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="36e9a-274">**server_ip**: 원본 또는 대상 서버의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-274">**server_ip**: The IP address of the source or destination server.</span></span>

- <span data-ttu-id="36e9a-275">**server_hostname**: 호스트 이름 또는 대상 서버의 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-275">**server_hostname**: The host name or FQDN of the destination server.</span></span>

- <span data-ttu-id="36e9a-p138">**source_context**: **원본** 필드와 관련 된 추가 정보입니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="36e9a-p138">**source_context**: Extra information associated with the **source** field. For example:</span></span>

   - `Protocol Filter Agent`

   - `3489061114359050000`

- <span data-ttu-id="36e9a-p139">**원본**: 이벤트를 담당 하는 Exchange Online 구성 요소입니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="36e9a-p139">**source**: The Exchange Online component that's responsible for the event. For example:</span></span>

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- <span data-ttu-id="36e9a-280">**event_id**: 이러한 값에 해당 하는 **메시지 이벤트** [이 메시지에 대 한 관련된 레코드 찾기](#find-related-records-for-this-message) 섹션에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-280">**event_id**: These correspond to the **Message event** values that are explained in the [Find related records for this message](#find-related-records-for-this-message) section.</span></span>

- <span data-ttu-id="36e9a-281">**internal_message_id**: 현재 메시지를 처리 하는 Exchange Online 서버에서 할당 하는 메시지 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-281">**internal_message_id**: A message identifier that's assigned by the Exchange Online server that's currently processing the message.</span></span>

- <span data-ttu-id="36e9a-p140">**recipient_address**: 메시지의 받는 사람 전자 메일 주소입니다. 여러 전자 메일 주소는 세미콜론 (;)으로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p140">**recipient_address**: The email addresses of the message's recipients. Multiple email addresses are separated by the semicolon character (;).</span></span>

- <span data-ttu-id="36e9a-284">**recipient_count**: 메시지의 받는 사람에 게의 총 수입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-284">**recipient_count**: The total number of recipients in the message.</span></span>

- <span data-ttu-id="36e9a-285">**related_recipient_address**:와 함께 사용 `EXPAND`, `REDIRECT`, 및 `RESOLVE` 다른 받는 사람을 표시 하는 이벤트 전자 메일 메시지와 연결 된 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-285">**related_recipient_address**: Used with `EXPAND`, `REDIRECT`, and `RESOLVE` events to display other recipient email addresses that are associated with the message.</span></span>

- <span data-ttu-id="36e9a-p141">**참고**:이 필드는 특정 유형의 이벤트에 대 한 추가 정보를 포함 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="36e9a-p141">**reference**: This field contains additional information for specific types of events. For example:</span></span>

   - <span data-ttu-id="36e9a-p142">**DSN**:이 이벤트 된 이후 DSN가 생성 하는 경우의 연결 된 배달 상태 알림 (로 알려져 DSN, 배달 못함 보고서, NDR, 또는 튀어오르 메시지) **message_id** 값을 사용 하는 보고서 링크를 포함 합니다. DSN 메시지 인 경우이 필드는 DSN에 대해 생성 된 원본 메시지의 **message_id** 값을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p142">**DSN**: Contains the report link, which is the **message_id** value of the associated delivery status notification (also known as a DSN, non-delivery report, NDR, or bounce message) if a DSN is generated subsequent to this event. If this is a DSN message, this field contains the **message_id** value of the original message that the DSN was generated for.</span></span>

   - <span data-ttu-id="36e9a-290">**확장**: 관련된 메시지의 **related_recipient_address** 값을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-290">**EXPAND**: Contains the **related_recipient_address** value of the related messages.</span></span>

   - <span data-ttu-id="36e9a-291">**수신**: 메시지 (예: 받은 편지함 규칙) 다른 프로세스에서 생성 하는 경우 관련된 메시지의 **message_id** 값이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-291">**RECEIVE**: Might contain the **message_id** value of the related message if the message was generated by other processes (for example, Inbox rules).</span></span>

   - <span data-ttu-id="36e9a-292">**보내기**: 모든 DSN 메시지의 **internal_message_id** 값을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-292">**SEND**: Contains the **internal_message_id** value of any DSN messages.</span></span>

   - <span data-ttu-id="36e9a-293">**전송**: (등 하 여 콘텐츠 변환, 메시지 받는 사람 수 제한 또는 에이전트) 분기 된 되는 메시지의 **internal_message_id** 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-293">**TRANSFER**: Contains the **internal_message_id** value of the message that's being forked (for example, by content conversion, message recipient limits, or agents).</span></span>

   - <span data-ttu-id="36e9a-294">**MAILBOXRULE**: 아웃 바운드 메시지를 생성 하는 받은 편지함 규칙을 발생 시킨 인바운드 메시지의 **internal_message_id** 값을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-294">**MAILBOXRULE**: Contains the **internal_message_id** value of the inbound message that caused the Inbox rule to generate the outbound message.</span></span>

   <span data-ttu-id="36e9a-295">다른 유형의 이벤트에 대해이 필드는 일반적으로 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-295">For other types of events, this field is usually blank.</span></span>

- <span data-ttu-id="36e9a-p143">**return_path**: 메시지를 보낸 **MAIL FROM** 명령에 의해 지정 된 반송 전자 메일 주소입니다. 으로 표시 되는 null 보낸사람 주소 값을 가질 수 있습니다이 필드가 비어 하지 않지만 `<>`합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p143">**return_path**: The return email address specified by the **MAIL FROM** command that sent the message. Although this field is never empty, it can have the null sender address value represented as `<>`.</span></span>

- <span data-ttu-id="36e9a-p144">**message_info**: 메시지에 대 한 추가 정보입니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="36e9a-p144">**message_info**: Additional information about the message. For example:</span></span>

   - <span data-ttu-id="36e9a-p145">메시지 시작 날짜-시간에 대 한 utc `DELIVER` 및 `SEND` 이벤트입니다. 시작 날짜 및 시간에는 메시지, Exchange Online 조직을 먼저 입력할 때 시간입니다. 문화권이 날짜 및 시간 형식에서 표시 되는 UTC 날짜 및 시간: `yyyy-mm-ddThh:mm:ss.fffZ`, 여기서 `yyyy` = 년, `mm` = 월, `dd` = 일, `T` 시간 구성 요소의 시작 부분을 나타냅니다 `hh` = 시간, `mm` (분)을 = `ss` = 둘째, `fff` 두번째, 소수로 = 및 `Z` 의미 `Zulu`, UTC를 표시 하는 다른 방법은 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p145">The message origination date-time in UTC for `DELIVER` and `SEND` events. The origination date-time is the time when the message first entered the Exchange Online organization. The UTC date-time is represented in the ISO 8601 date-time format: `yyyy-mm-ddThh:mm:ss.fffZ`, where `yyyy` = year, `mm` = month, `dd` = day, `T` indicates the beginning of the time component, `hh` = hour, `mm` = minute, `ss` = second, `fff` = fractions of a second, and `Z` signifies `Zulu`, which is another way to denote UTC.</span></span>

   - <span data-ttu-id="36e9a-p146">인증 오류가 발생 했습니다. 값을 볼 수 등 `11a` 및 인증 오류가 발생 했을 때 사용 된 인증 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p146">Authentication errors. For example, you might see the value `11a` and the type of authentication that was used when the authentication error occurred.</span></span>

- <span data-ttu-id="36e9a-305">**tenant_id**: Exchange Online 조직을 나타내는 GUID 값 (예 `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span><span class="sxs-lookup"><span data-stu-id="36e9a-305">**tenant_id**: A GUID value that represents the Exchange Online organization (for example, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span></span>

- <span data-ttu-id="36e9a-306">**original_server_ip**: 원본 서버의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-306">**original_server_ip**: The IP address of the original server.</span></span>

- <span data-ttu-id="36e9a-p147">**custom_data**: 특정 이벤트 종류에 관련 된 데이터를 포함 합니다. 자세한 내용은 다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p147">**custom_data**: Contains data related to specific event types. For more information, see the following sections.</span></span>

#### <a name="customdata-values"></a><span data-ttu-id="36e9a-309">custom_data 값</span><span class="sxs-lookup"><span data-stu-id="36e9a-309">custom_data values</span></span>

<span data-ttu-id="36e9a-p148">에 대 한 **custom_data** 필드는 `AGENTINFO` 이벤트 로그 메시지 처리 세부 정보를 다양 한 Exchange Online 에이전트 사용 됩니다. 다음 섹션에 설명 된 흥미 에이전트의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p148">The **custom_data** field for an `AGENTINFO` event is used by a variety of Exchange Online agents to log message processing details. Some of the more interesting agents are described in the following sections.</span></span>

#### <a name="spam-filter-agent"></a><span data-ttu-id="36e9a-312">스팸 필터 에이전트</span><span class="sxs-lookup"><span data-stu-id="36e9a-312">Spam filter agent</span></span>

<span data-ttu-id="36e9a-p149">로 시작 하는 **custom_data** 값 `S:SFA` 스팸 필터 에이전트에서 시작 됩니다. 중요 한 세부 정보는 다음 표에에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p149">A **custom_data** value that starts with `S:SFA` is from the spam filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="36e9a-315">**값**</span><span class="sxs-lookup"><span data-stu-id="36e9a-315">**Value**</span></span>|<span data-ttu-id="36e9a-316">**설명**</span><span class="sxs-lookup"><span data-stu-id="36e9a-316">**Description**</span></span>|
|:-----|:-----|
|`SFV=NSPM`|<span data-ttu-id="36e9a-317">메시지가 스팸이 아닌 것으로 표시되었으며 받는 사람에게 전송되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-317">The message was marked as non-spam and was sent to the intended recipients.</span></span>|
|`SFV=SPM`|<span data-ttu-id="36e9a-318">메시지가 콘텐츠 필터에 의해 스팸으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-318">The message was marked as spam by the content filter.</span></span>|
|`SFV=BLK`|<span data-ttu-id="36e9a-319">수신 거부된 보낸 사람이 보낸 메시지이므로 필터링을 건너뛰었으며 메시지가 차단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-319">Filtering was skipped and the message was blocked because it originated from a blocked sender.</span></span>|
|`SFV=SKS`|<span data-ttu-id="36e9a-p150">메시지가 콘텐츠 필터에 의해 처리되기 전에 이미 스팸으로 표시되었습니다. 전송 규칙과 일치하여 스팸으로 자동 표시되고 모든 추가 필터링을 무시하는 메시지가 여기에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p150">The message was marked as spam prior to being processed by the content filter. This includes messages where the message matched a Transport rule to automatically mark it as spam and bypass all additional filtering.</span></span>|
|`SCL=<number>`|<span data-ttu-id="36e9a-322">여러 SCL 값과 그 의미에 대 한 자세한 내용은 [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-322">For more information about the different SCL values and what they mean, see [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`PCL=<number>`|<span data-ttu-id="36e9a-p151">메시지의 피싱 신뢰 수준 (PCL) 값입니다. SCL와 동일한 방식으로 해석 될 수 있는 이러한 [스팸 신뢰 수준](https://technet.microsoft.com/library/jj200686.aspx)에서 설명 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p151">The Phishing Confidence Level (PCL) value of the message. These can be interpreted the same way as the SCL values documented in [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`DI=SB`|<span data-ttu-id="36e9a-325">메시지의 보낸 사람이 차단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-325">The sender of the message was blocked.</span></span>|
|`DI=SQ`|<span data-ttu-id="36e9a-326">메시지가 격리되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-326">The message was quarantined.</span></span>|
|`DI=SD`|<span data-ttu-id="36e9a-327">메시지가 삭제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-327">The message was deleted.</span></span>|
|`DI=SJ`|<span data-ttu-id="36e9a-328">받는 사람의 정크 메일 폴더로 메시지를 보냈습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-328">The message was sent to the recipient's Junk Email folder.</span></span>|
|`DI=SN`|<span data-ttu-id="36e9a-p152">메시지는 위험성이 높은 배달 풀을 통해 라우팅 되었습니다. 자세한 내용은 [아웃 바운드 메시지 용 위험성이 높은 배달 풀](https://technet.microsoft.com/library/jj200746.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p152">The message was routed through the higher risk delivery pool. For more information, see [High-risk delivery pool for outbound messages](https://technet.microsoft.com/library/jj200746.aspx).</span></span>|
|`DI=SO`|<span data-ttu-id="36e9a-331">메시지가 일반 아웃바운드 배달 풀을 통해 라우팅되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-331">The message was routed through the normal outbound delivery pool.</span></span>|
|<span data-ttu-id="36e9a-332">' SFS = [a]</span><span class="sxs-lookup"><span data-stu-id="36e9a-332">\`SFS=[a]</span></span>|<span data-ttu-id="36e9a-333">SFS = [b]'</span><span class="sxs-lookup"><span data-stu-id="36e9a-333">SFS=[b]\`</span></span>|<span data-ttu-id="36e9a-334">스팸 규칙이 일치했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-334">This denotes that spam rules were matched.</span></span>|
|`IPV=CAL`|<span data-ttu-id="36e9a-335">연결 필터의 IP 허용 목록에 IP 주소가 지정되어 있어 메시지가 스팸 필터를 통과하도록 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-335">The message was allowed through the spam filters because the IP address was specified in an IP Allow list in the connection filter.</span></span>|
|`H=<EHLOstring>`|<span data-ttu-id="36e9a-336">연결 된 전자 메일 서버의 HELO 또는 EHLO 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-336">The HELO or EHLO string of the connecting email server.</span></span>|
|`PTR=<ReverseDNS>`|<span data-ttu-id="36e9a-337">보내는 IP 주소의 PTR 레코드로, 역방향 DNS 주소라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-337">The PTR record of the sending IP address, also known as the reverse DNS address.</span></span>|

<span data-ttu-id="36e9a-338">다음과 같은 스팸 필터링 된 메시지에 대 한 예제 **custom_data** 값:</span><span class="sxs-lookup"><span data-stu-id="36e9a-338">An example **custom_data** value for a message that's filtered for spam like this:</span></span>

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a><span data-ttu-id="36e9a-339">맬웨어 필터 에이전트</span><span class="sxs-lookup"><span data-stu-id="36e9a-339">Malware filter agent</span></span>

<span data-ttu-id="36e9a-p153">로 시작 하는 **custom_data** 값 `S:AMA` 맬웨어 필터 에이전트에서 시작 됩니다. 중요 한 세부 정보는 다음 표에에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p153">A **custom_data** value that starts with `S:AMA` is from the malware filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="36e9a-342">**값**</span><span class="sxs-lookup"><span data-stu-id="36e9a-342">**Value**</span></span>|<span data-ttu-id="36e9a-343">**설명**</span><span class="sxs-lookup"><span data-stu-id="36e9a-343">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36e9a-344">' AMA = SUM</span><span class="sxs-lookup"><span data-stu-id="36e9a-344">\`AMA=SUM</span></span>|<span data-ttu-id="36e9a-345">v = 1</span><span class="sxs-lookup"><span data-stu-id="36e9a-345">v=1</span></span>|<span data-ttu-id="36e9a-346">` or `AMA EV =</span><span class="sxs-lookup"><span data-stu-id="36e9a-346">` or `AMA=EV</span></span>|<span data-ttu-id="36e9a-347">v = 1'</span><span class="sxs-lookup"><span data-stu-id="36e9a-347">v=1\`</span></span>|<span data-ttu-id="36e9a-p154">맬웨어를 포함 하는 메시지 결정 됩니다. `SUM` 맬웨어가 수 했을 때 발견 되었음을 나타냅니다 엔진의 모든 수 있습니다. `EV` 맬웨어가 특정 엔진에서 찾을 수를 나타냅니다. 맬웨어 감지 되 면는 엔진에 의해이 후속 작업을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p154">The message was determined to contain malware. `SUM` indicates the malware could've been detected by any number of engines. `EV` indicates the malware was detected by a specific engine. When malware is detected by an engine this triggers the subsequent actions.</span></span>|
|`Action=r`|<span data-ttu-id="36e9a-352">메시지가 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-352">The message was replaced.</span></span>|
|`Action=p`|<span data-ttu-id="36e9a-353">메시지가 무시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-353">The message was bypassed.</span></span>|
|`Action=d`|<span data-ttu-id="36e9a-354">메시지가 지연되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-354">The message was deferred.</span></span>|
|`Action=s`|<span data-ttu-id="36e9a-355">메시지가 삭제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-355">The message was deleted.</span></span>|
|`Action=st`|<span data-ttu-id="36e9a-356">메시지가 무시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-356">The message was bypassed.</span></span>|
|`Action=sy`|<span data-ttu-id="36e9a-357">메시지가 무시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-357">The message was bypassed.</span></span>|
|`Action=ni`|<span data-ttu-id="36e9a-358">메시지가 거부되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-358">The message was rejected.</span></span>|
|`Action=ne`|<span data-ttu-id="36e9a-359">메시지가 거부되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-359">The message was rejected.</span></span>|
|`Action=b`|<span data-ttu-id="36e9a-360">메시지가 차단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-360">The message was blocked.</span></span>|
|`Name=<malware>`|<span data-ttu-id="36e9a-361">검색된 맬웨어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-361">The name of the malware that was detected.</span></span>|
|`File=<filename>`|<span data-ttu-id="36e9a-362">맬웨어가 포함된 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-362">The name of the file that contained the malware.</span></span>|

<span data-ttu-id="36e9a-363">맬웨어를 포함 하는 메시지에 대 한 예제 **custom_data** 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-363">An example **custom_data** value for a message that contains malware looks like this:</span></span>

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a><span data-ttu-id="36e9a-364">전송 규칙 에이전트</span><span class="sxs-lookup"><span data-stu-id="36e9a-364">Transport rule agent</span></span>

<span data-ttu-id="36e9a-p155">로 시작 하는 **custom_data** 값`S:TRA` 메일 흐름 규칙 (전송 규칙이 라고도 함)에 대 한 전송 규칙 에이전트에서 시작 됩니다. 중요 한 세부 정보는 다음 표에에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p155">A **custom_data** value that starts with`S:TRA` is from the transport rule agent for mail flow rules (also known as transport rules). The key details are described in the following table:</span></span>

|<span data-ttu-id="36e9a-367">**값**</span><span class="sxs-lookup"><span data-stu-id="36e9a-367">**Value**</span></span>|<span data-ttu-id="36e9a-368">**설명**</span><span class="sxs-lookup"><span data-stu-id="36e9a-368">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36e9a-369">' ETR</span><span class="sxs-lookup"><span data-stu-id="36e9a-369">\`ETR</span></span>|<span data-ttu-id="36e9a-370">규칙 id가 =<guid>\`</span><span class="sxs-lookup"><span data-stu-id="36e9a-370">ruleId=<guid>\`</span></span>|<span data-ttu-id="36e9a-371">일치된 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-371">The rule ID that was matched.</span></span>|
|`St=<datetime>`|<span data-ttu-id="36e9a-372">날짜 및 시간 규칙 일치가 발생 했을 때 UTC입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-372">The date and time in UTC when the rule match occurred.</span></span>|
|`Action=<ActionDefinition>`|<span data-ttu-id="36e9a-p156">이 작업에 적용 된입니다. 사용 가능한 작업 목록이 [메일 흐름 규칙 동작 Exchange Online](https://technet.microsoft.com/library/jj919237.aspx)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p156">The action that was applied. For a list of available actions, see [Mail flow rule actions in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span></span>|
|`Mode=<Mode>`|<span data-ttu-id="36e9a-p157">규칙의 모드입니다. 유효한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-p157">The mode of the rule. Valid values are: </span></span><br/><span data-ttu-id="36e9a-377">• **적용**: 규칙에 대 한 모든 작업이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-377">• **Enforce**: All actions on the rule will be enforced.</span></span> <br/><span data-ttu-id="36e9a-378">• **정책 설명이 있는 테스트:**: 모든 정책 설명 작업이 전송 되지만 다른 적용 작업은 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-378">• **Test with Policy Tips:**: Any Policy Tip actions will be sent, but other enforcement actions will not be acted on.</span></span> <br/><span data-ttu-id="36e9a-379">• **정책 설명이 없는 테스트**: 작업이 로그 파일에 나열 되지만 보낸사람 어떤 식으로도 알림을 받지 못합니다 및 적용 작업은 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-379">• **Test without Policy Tips**: Actions will be listed in a log file, but senders will not be notified in any way, and enforcement actions will not be acted on.</span></span>|

<span data-ttu-id="36e9a-380">예제 **custom_data** 하는 값을 메시지에 대 한 메일 흐름 규칙의 조건과 일치 하는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="36e9a-380">An example **custom_data** value for a messages that matches the conditions of a mail flow rule looks like this:</span></span>

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`
