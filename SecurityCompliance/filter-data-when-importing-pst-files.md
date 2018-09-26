---
title: Office 365에 PST 파일을 가져올 때 데이터를 필터링 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: '대상 사서함에 실제로 가져온 항목을 필터링 하는 Office 365 가져오기 서비스에서 새 지능형 가져오기 기능을 사용 합니다. 지능형 Import를 사용 하면 사전 가져오기 및 뒤에 그대로 대상에 데이터를 결정할 수 있습니다. 또한 지능형 가져오기 Office 365로 가져올 데이터에 정보를 제공 합니다. '
ms.openlocfilehash: c90d9df62c7d8c411196b283acec37959fc95e57
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038201"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a><span data-ttu-id="efa00-105">Office 365에 PST 파일을 가져올 때 데이터를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-105">Filter data when importing PST files to Office 365</span></span>

<span data-ttu-id="efa00-p102">대상 사서함에 실제로 가져온 PST 파일에 항목을 필터링 하는 Office 365 가져오기 서비스에서 새 지능형 가져오기 기능을 사용 합니다. 작동 방식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p102">Use the new Intelligent Import feature in the Office 365 Import service to filter the items in PST files that actually get imported to the target mailboxes. Here's how it works:</span></span>
  
- <span data-ttu-id="efa00-108">만들어 PST 가져오기 작업을 전송 하 고 PST 파일을 Microsoft 클라우드에서 Azure 저장소 영역에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-108">After you create and submit a PST import job, PST files are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
    
- <span data-ttu-id="efa00-109">Office 365 안전 하 게 방식으로 다양 한 메시지 형식과 PST 파일에 포함 된 사서함 항목의 보존 기간을 식별 하 여 PST 파일의 데이터를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-109">Office 365 analyzes the data in the PST files, in a safe and secure manner, by identifying the age of the mailbox items and the different message types included in the PST files.</span></span>
    
- <span data-ttu-id="efa00-p103">분석이 완료 되 고 데이터를 가져올 준비가 되었습니다를 두거나 데이터를 가져온 가져옵니다을 제어 하는 필터를 설정 하 여 가져온 데이터를 높이고 PST 파일에서 모든 데이터를 가져오려면 옵션도 있습니다. 예를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p103">When the analysis is complete and the data is ready to import, you have the option to import all data in the PST files as is or trim the data that's imported by setting filters that control what data gets imported. For example, you can choose to:</span></span>
    
  - <span data-ttu-id="efa00-112">특정 시간에만 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-112">Import only items of a certain age.</span></span>
    
  - <span data-ttu-id="efa00-113">선택한 메시지 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-113">Import selected message types.</span></span>
    
  - <span data-ttu-id="efa00-114">특정 사용자가 보내거나 받는 메시지를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-114">Exclude messages sent or received by specific people.</span></span>
    
- <span data-ttu-id="efa00-115">필터 설정을 구성한 후 Office 365 가져오기 작업에 지정 된 대상 사서함에 필터링 조건을 충족 하는 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-115">After you configure the filter settings, Office 365 imports only the data that meets the filtering criteria to the target mailboxes specified in the import job.</span></span>
    
<span data-ttu-id="efa00-116">다음 그림 지능형 가져오기 프로세스를 보여줍니다 및 수행 하는 작업 및 Office 365에서 수행 하는 작업을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-116">The following graphic shows the Intelligent Import process, and highlights the tasks you perform and the tasks performed by Office 365.</span></span>
  
![Office 365의 지능형 가져오기 프로세스](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a><span data-ttu-id="efa00-118">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="efa00-118">Before you begin</span></span>

- <span data-ttu-id="efa00-p104">이 항목의 단계 네트워크 업로드 또는 드라이브 전달을 사용 하 여 PST 가져오기 작업을 만든 Office 365를 가져올 서비스에서 했을 때으로 가정 합니다. 단계별 지침은 다음 항목 중 하나를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="efa00-p104">The steps in this topic assume that you've created a PST import job in the Office 365 Import service by using network upload or drive shipping. For step-by-step instructions, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="efa00-121">네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="efa00-121">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
    
  - [<span data-ttu-id="efa00-122">드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="efa00-122">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- <span data-ttu-id="efa00-p105">Office 365 보안에서 가져오기에서 가져오기 작업에 대 한 상태 페이지 네트워크 업로드를 사용 하 여 가져오기 작업을 만든 후 &amp; 준수 센터로 설정 된 **진행 중인 분석**하는 Office 365 PST 파일에서 데이터를 분석 되는 것을 의미 해야 업로드 합니다. **새로고침**을 클릭![새로고침](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) 가져오기 작업에 대 한 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p105">After you create an import job by using network upload, the status for the import job on the Import page in Office 365 Security &amp; Compliance Center is set to **Analysis in progress**, which means that Office 365 is analyzing the data in the PST files that you uploaded. Click **Refresh**![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) to update the status for the import job.</span></span> 
    
- <span data-ttu-id="efa00-125">가져오기 작업을 전달 하는 드라이브에 대 한 Microsoft 데이터 센터 담당자가 사용자의 하드 드라이브를 받고 조직에 대 한 Azure 저장소 영역을 PST 파일을 업로드 한 후 Office 365에서 데이터를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-125">For drive shipping import jobs, the data will be analyzed by Office 365 after Microsoft data center personnel receive your hard drive and upload the PST files to the Azure storage area for your organization.</span></span>
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a><span data-ttu-id="efa00-126">사서함에 가져온 가져옵니다 데이터 필터링</span><span class="sxs-lookup"><span data-stu-id="efa00-126">Filter data that gets imported to mailboxes</span></span>

<span data-ttu-id="efa00-127">만든 후에 PST 가져오기 작업, Office 365로 가져오기 전에 데이터를 필터링 하려면 다음이 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-127">After you've created a PST import job, follow these steps to filter the data before you import it to Office 365.</span></span>
  
1. <span data-ttu-id="efa00-128">이동 [https://protection.office.com/](https://protection.office.com/) 및 Office 365 조직에서 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-128">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="efa00-129">Office 365 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **가져오기**.</span><span class="sxs-lookup"><span data-stu-id="efa00-129">In the left pane of the Office 365 Security &amp; Compliance Center, click **Data governance** \> **Import**.</span></span>
    
    <span data-ttu-id="efa00-p106">조직에 대 한 가져오기 작업 **가져오기** 페이지에 나열 됩니다. Note **분석이 완료** 값의 **상태** 열에서 Office 365에서 분석 하 고 가져올 수에 대 한 준비가 완료 하는 가져오기 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p106">The import jobs for your organization are listed on the **Import** page. Note that the **Analysis completed** value in the **Status** column indicates the import jobs that have been analyzed by Office 365 and are ready for you to import.</span></span> 
    
    ![Office 365의 PST 파일의 데이터를 분석 하는 분석 완료 상태를 나타냅니다.](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. <span data-ttu-id="efa00-133">완료 하려는 가져오기 작업에 대 한 **Office 365로 가져올 준비** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-133">Click **Ready to import to Office 365** for the import job that you want to complete.</span></span> 
    
    <span data-ttu-id="efa00-134">페이지 날아가기 PST 파일에 대 한 정보 및 가져오기 작업에 대 한 기타 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-134">A fly out page is displayed with information about the PST files and other information about the import job.</span></span>
    
4. <span data-ttu-id="efa00-135">**Office 365에 가져오기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-135">Click **Import to Office 365**.</span></span>
    
    <span data-ttu-id="efa00-p107">**데이터를 필터링** 페이지가 표시 됩니다. 데이터의 기간에 대 한 정보를 포함 하는 가져오기 작업에 대 한 PST 파일의 데이터에 대 한 데이터 인 사이트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p107">The **Filter your data** page is displayed. It contains data insights about the data in the PST files for the import job, including information about the age of the data.</span></span> 
    
    ![가져오기 작업에 대 한 PST 파일의 데이터 정보를 표시 하는 데이터 페이지에서 제품 키 필터](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. <span data-ttu-id="efa00-139">아래에서 Office 365로 가져올 데이터를 높이고 하려는 여부에 따라 **데이터를 필터링 하 시겠습니까?**, 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-139">Based on whether or not you want to trim the data that's imported to Office 365, under **Do you want to filter your data?**, do one of the following:</span></span>
    
    <span data-ttu-id="efa00-p108">a.을 가져올 수 있는 데이터를 트리밍할 **예, 가져오기 전에으로 필터링 합니다.** 를 클릭 하 고 \*\*\*\* 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p108">a. Click **Yes, I want to filter it before importing** to trim the data that you import, and then click **Next**.</span></span>
    
    <span data-ttu-id="efa00-142">**Office 365 페이지로 데이터 가져오기** 페이지에서 Office 365 수행 하는 분석 세부 데이터 인 사이트 함께 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-142">The **Import data to Office 365 page** page is displayed with detailed data insights from the analysis that Office 365 performed.</span></span> 
    
    ![Office 365에서 PST 파일의 분석을 통해 자세한 데이터 정보를 표시합니다.](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    <span data-ttu-id="efa00-p109">이 페이지에서 그래프에는 가져올 데이터의 양을 보여줍니다. PST 파일에 있는 각 메시지 형식에 대 한 정보는 그래프에 표시 됩니다. 커서 해당 메시지 형식에 대 한 특정 정보를 표시 하려면 각 막대 가리키면 수 있습니다. 분석 PST 파일을 기반으로 다른 기간 값을 가진 드롭다운 목록 이기도 합니다. 드롭다운 목록에는 시간을 선택 하면 그래프는 선택한 기간에 대 한 데이터의 양을 가져올 수를 표시 하도록 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p109">The graph on this page shows the amount of data that will be imported. Information about each message type found in the PST files is displayed in the graph. You can hover the cursor over each bar to display specific information about that message type. There is also a drop-down list with different age values based on the analysis of the PST files. When you select an age in the drop-down list, the graph is updated to show how much data will be imported for the selected age.</span></span> 
    
    <span data-ttu-id="efa00-p110">b. 가져오기가 수행 되는 데이터의 양을 줄일 수 추가 필터를 구성 하려면 **추가 필터링 옵션**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p110">b. To configure addition filters to reduce the amount of data that's imported, click **More filtering options**.</span></span>
    
    ![Trim 가져오기가 수행 되는 데이터를 더 많은 옵션 페이지에서 필터를 구성 합니다.](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    <span data-ttu-id="efa00-152">이러한 필터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-152">You can configure these filters:</span></span>
    
      - <span data-ttu-id="efa00-p111">**기간** -하므로 지정 된 기간 보다 최신 버전인는 항목만 한 시대 가져올 것임을 선택 합니다. Office 365 **기간** 필터에 대 한 보존 기간 버킷을 결정 하는 방법에 대 한 설명에 대 한 [자세한 내용](filter-data-when-importing-pst-files.md#moreinfo) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="efa00-p111">**Age** - Select an age so only items that are newer than the specified age will be imported. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a description about how Office 365 determines the age buckets for the **Age** filter.</span></span> 
    
      - <span data-ttu-id="efa00-p112">**형식** -이 섹션에는 가져오기 작업에 대 한 PST 파일에서 발견 된 모든 메시지 유형이 표시 합니다. 제외 하려는 메시지 유형 옆에 있는 상자를 선택 취소 수 있습니다. 참고 다른 메시지 유형을 제외 수는 없습니다. 다른 범주에 포함 된 사서함 항목의 목록에 대 한 [자세한 내용](filter-data-when-importing-pst-files.md#moreinfo) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="efa00-p112">**Type** - This section shows all the message types that were found in the PST files for the import job. You can uncheck a box next to a message type that you want to exclude. Note that you can't exclude the Other message type. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a list of mailbox items that are included in the Other category.</span></span> 
    
      - <span data-ttu-id="efa00-p113">**사용자가** -전송 또는 특정 사용자가 받은 메시지를 제외할 수 있습니다. From에 표시 하는 사람을 제외 하도록: 필드를: 필드나는 Cc: 메시지의 필드 해당 받는 사람 유형 옆에 있는 **사용자를 제외** 를 클릭 합니다. 사용자의 전자 메일 주소 (SMTP 주소)를 입력 한 다음 **추가**클릭 합니다![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) 해당 받는 사람 유형에 대 한 제외 된 사용자의 목록에 추가할 한 후 제외 된 사용자의 목록을 저장 하려면 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p113">**Users** - You can exclude messages that are sent or received by specific people. To exclude people who appear in the From: field, To: field, or the Cc: field of messages, click **Exclude users** next to that recipient type. Type the email address (SMTP address) of the person, click **Add**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) to add them to the list of excluded users for that recipient type, and then click **Save** to save the list of excluded users.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="efa00-p114">Office 365 **사용자** 필터 설정에서 생성 되는 데이터 인 사이트를 표시 하지 않습니다. 그러나 특정 사용자가 보내거나 받는 메시지를 제외 하려면이 필터를 설정 하는 경우 해당 메시지는 실제 가져오기 프로세스 중 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p114">Office 365 doesn't show data insights that result from setting the **People** filter. However, if you set this filter to exclude messages sent or received by specific people, those messages will be excluded during the actual import process.</span></span> 
  
    <span data-ttu-id="efa00-p115">c. **더 필터링 옵션** 에 대 한 날아가기 필터 설정을 저장 하는 페이지에서에서 **적용** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p115">c. Click **Apply** in the **More filtering options** fly out page to save your filter settings.</span></span> 
    
    <span data-ttu-id="efa00-p116">**Office 365로 데이터 가져오기** 페이지에서 인 사이트 필터 설정을 기반으로 업데이트 되는 데이터를 가져올 데이터의 총 크기를 포함 하 여 필터 설정을 기반으로 합니다. 필터 설정의 요약을 표시 되는 또한 메모 합니다. 필요한 경우 설정을 변경 하는 필터 옆에 있는 **편집** 을 클릭 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p116">The data insights on the **Import data to Office 365** page are updated based on your filter settings, including the total amount of data that will be imported based on the filter settings. Note that a summary of the filter settings is also shown. You can click **Edit** next to a filter to change the setting if necessary.</span></span> 
    
    ![필터 설정에 따라 데이터 정보 업데이트](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    <span data-ttu-id="efa00-p117">d. **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p117">d. Click **Next**.</span></span>
    
    <span data-ttu-id="efa00-p118">상태 페이지 필터 설정을 보여주는 표시 됩니다. 다시, 필터 설정을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p118">A status page is displayed showing your filter settings. Again, you can edit any of the filter settings.</span></span>
    
    <span data-ttu-id="efa00-p119">e. **데이터 가져오기** 는 가져오기를 시작 하려면 클릭 합니다. Note 가져올 데이터의 양과 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p119">e. Click **Import data** to start the import . Note that the total amount of data that will be imported is displayed.</span></span> 
    
    <span data-ttu-id="efa00-177">또는</span><span class="sxs-lookup"><span data-stu-id="efa00-177">Or</span></span>
    
    <span data-ttu-id="efa00-p120">a. Office 365에 PST 파일의 모든 데이터를 가져오려면 **아니오, 모든 작업을 가져오려면 합니다.** 를 클릭 하 고 \*\*\*\* 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p120">a. Click **No, I want to import everything** to import all data in the PST files to Office 365, and then click **Next**.</span></span>
    
    <span data-ttu-id="efa00-p121">b. **Office 365로 데이터 가져오기** 페이지에서 **데이터 가져오기** 는 가져오기를 시작 하려면 클릭 합니다. Note 가져올 데이터의 양과 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p121">b. On the **Import data to Office 365** page, click **Import data** to start the import. Note that the total amount of data that will be imported is displayed.</span></span> 
    
6. <span data-ttu-id="efa00-p122">**가져오기** 페이지에서 **새로 고칠** 을 클릭 ![새로고침](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png)합니다. 가져오기 작업의 상태가 **상태** 열에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p122">On the **Import** page, click **Refresh** ![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). The status for the import job is displayed in the **Status** column.</span></span> 
    
7. <span data-ttu-id="efa00-185">가져오기 각 PST 파일과으로 구성 된 필터 설정에 대 한 상태와 같은 자세한 정보를 표시 하는 작업을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-185">Click the import the job to display more detailed information, such as the status for each PST file and the filter settings that you configured.</span></span>

  
## <a name="more-information"></a><span data-ttu-id="efa00-186">추가 정보</span><span class="sxs-lookup"><span data-stu-id="efa00-186">More information</span></span>

- <span data-ttu-id="efa00-p123">Office 365 기간 필터에 대 한 씩 증가 결정 하는 방법 Office 365을 분석 하 여 PST 파일을 검색할 때 각 항목의 보내거나 받은 타임 스탬프에 찾습니다 (경우 항목에는 보내고 받은 타임 스탬프, 가장 오래 된 날짜 선택). 그런 다음 Office 365 해당 타임 스탬프에 대 한 연도 값을 확인 하 고 항목의 보존 기간을 결정 하는 현재 날짜를 비교 합니다. 이러한 나이가 다음 **기간** 필터에 대 한 드롭다운 목록에 있는 값으로 사용 됩니다. 등 PST 파일에 2015, 2016, 2014 년에서 메시지를 시작한 다음 **기간** 필터에 값이 **1 년**, **2 년**및 **3 년**일 것입니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p123">How does Office 365 determine the increments for the age filter? When Office 365 analyzes a PST file, it looks at the sent or received time stamp of each item (if an item has both a sent and received timestamp, the oldest date is selected). Then Office 365 looks at the year value for that timestamp and compares it to the current date to determine the age of the item. These ages are then used as the values in the drop-down list for the **Age** filter. For example, if a PST file has messages from 2016, 2015, and 2014, then values in the **Age** filter would be **1 year**, **2 years**, and **3 years**.</span></span>
    
- <span data-ttu-id="efa00-p124">다음 표에 **추가 옵션** 에 대 한 날아가기 페이지에 대 한 **형식** 필터에서 **다른** 범주에 포함 된 메시지 유형 (이전 절차에서 5b 단계 참조). 현재 Office 365에 Pst을 가져올 때 "다른" 범주에 있는 항목을 제외할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-p124">The following table lists the message types that are included in the **Other** category in the **Type** filter on the **More options** fly out page (see Step 5b in the previous procedure). Currently, you can't exclude items in the "Other" category when you import PSTs to Office 365.</span></span> 
    
    |<span data-ttu-id="efa00-194">**메시지 클래스 ID**</span><span class="sxs-lookup"><span data-stu-id="efa00-194">**Message class ID**</span></span>|<span data-ttu-id="efa00-195">**이 메시지 클래스를 사용 하는 사서함 항목**</span><span class="sxs-lookup"><span data-stu-id="efa00-195">**Mailbox items that use this message class**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="efa00-196">IPM입니다. 활동</span><span class="sxs-lookup"><span data-stu-id="efa00-196">IPM.Activity</span></span>  <br/> |<span data-ttu-id="efa00-197">저널 항목</span><span class="sxs-lookup"><span data-stu-id="efa00-197">Journal entries</span></span>  <br/> |
    |<span data-ttu-id="efa00-198">IPM입니다. 문서</span><span class="sxs-lookup"><span data-stu-id="efa00-198">IPM.Document</span></span>  <br/> |<span data-ttu-id="efa00-199">문서 및 파일 (전자 메일 메시지에 연결 되지 않은)</span><span class="sxs-lookup"><span data-stu-id="efa00-199">Documents and files (not attached to an email message)</span></span>  <br/> |
    |<span data-ttu-id="efa00-200">IPM입니다. 파일</span><span class="sxs-lookup"><span data-stu-id="efa00-200">IPM.File</span></span>  <br/> |<span data-ttu-id="efa00-201">(IPM와 동일 합니다. 문서)</span><span class="sxs-lookup"><span data-stu-id="efa00-201">(same as IPM.Document)</span></span>  <br/> |
    |<span data-ttu-id="efa00-202">IPM입니다. Note.IMC.Notification</span><span class="sxs-lookup"><span data-stu-id="efa00-202">IPM.Note.IMC.Notification</span></span>  <br/> |<span data-ttu-id="efa00-203">보고서가 인터넷에는 Exchange Server 게이트웨이가 되어야 하는 인터넷 메일 커넥터 연결 하 여 전송</span><span class="sxs-lookup"><span data-stu-id="efa00-203">Reports sent by Internet Mail Connect, which is the Exchange Server gateway to the Internet</span></span>  <br/> |
    |<span data-ttu-id="efa00-204">IPM입니다. Note.Microsoft.Fax</span><span class="sxs-lookup"><span data-stu-id="efa00-204">IPM.Note.Microsoft.Fax</span></span>  <br/> |<span data-ttu-id="efa00-205">팩스 메시지</span><span class="sxs-lookup"><span data-stu-id="efa00-205">Fax messages</span></span>  <br/> |
    |<span data-ttu-id="efa00-206">IPM입니다. Note.Rules.Oof.Template.Microsoft</span><span class="sxs-lookup"><span data-stu-id="efa00-206">IPM.Note.Rules.Oof.Template.Microsoft</span></span>  <br/> |<span data-ttu-id="efa00-207">부재중의 자동 응답 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="efa00-207">Out-of-office auto-reply messages</span></span>  <br/> |
    |<span data-ttu-id="efa00-208">IPM입니다. Note.Rules.ReplyTemplate.Microsoft</span><span class="sxs-lookup"><span data-stu-id="efa00-208">IPM.Note.Rules.ReplyTemplate.Microsoft</span></span>  <br/> |<span data-ttu-id="efa00-209">받은 편지함 규칙에 의해 전송 회신</span><span class="sxs-lookup"><span data-stu-id="efa00-209">Replies sent by an inbox rule</span></span>  <br/> |
    |<span data-ttu-id="efa00-210">IPM입니다. OLE 합니다. 클래스</span><span class="sxs-lookup"><span data-stu-id="efa00-210">IPM.OLE.Class</span></span>  <br/> |<span data-ttu-id="efa00-211">되풀이 항목에 대 한 예외</span><span class="sxs-lookup"><span data-stu-id="efa00-211">Exceptions for a recurring series</span></span>  <br/> |
    |<span data-ttu-id="efa00-212">IPM입니다. Recall.Report</span><span class="sxs-lookup"><span data-stu-id="efa00-212">IPM.Recall.Report</span></span>  <br/> |<span data-ttu-id="efa00-213">메시지 회수 보고서</span><span class="sxs-lookup"><span data-stu-id="efa00-213">Message recall reports</span></span>  <br/> |
    |<span data-ttu-id="efa00-214">IPM입니다. 원격</span><span class="sxs-lookup"><span data-stu-id="efa00-214">IPM.Remote</span></span>  <br/> |<span data-ttu-id="efa00-215">원격 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="efa00-215">Remote mail messages</span></span>  <br/> |
    |<span data-ttu-id="efa00-216">IPM입니다. 보고서</span><span class="sxs-lookup"><span data-stu-id="efa00-216">IPM.Report</span></span>  <br/> |<span data-ttu-id="efa00-217">항목 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="efa00-217">Item status reports</span></span>  <br/> |
