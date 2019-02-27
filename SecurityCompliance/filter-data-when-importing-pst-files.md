---
title: PST 파일을 Office 365로 가져올 때 데이터 필터링
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Office 365 가져오기 서비스의 새로운 지능형 가져오기 기능을 사용 하 여 실제로 대상 사서함으로 가져오는 항목을 필터링 합니다. 지능형 가져오기를 사용 하면 가져올 데이터와 뒤에 남길 작업을 사전에 결정할 수 있습니다. 또한 지능형 가져오기에서는 Office 365로 가져오는 데이터에 대 한 정보를 제공 합니다. '
ms.openlocfilehash: 6091f6cca75bffbb05bcd59f70cfae0dbdcb9040
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30297071"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a><span data-ttu-id="4202a-105">PST 파일을 Office 365로 가져올 때 데이터 필터링</span><span class="sxs-lookup"><span data-stu-id="4202a-105">Filter data when importing PST files to Office 365</span></span>

<span data-ttu-id="4202a-p102">Office 365 가져오기 서비스의 새로운 지능형 가져오기 기능을 사용 하면 실제로 대상 사서함으로 가져온 PST 파일의 항목을 필터링 할 수 있습니다. 작동 방식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p102">Use the new Intelligent Import feature in the Office 365 Import service to filter the items in PST files that actually get imported to the target mailboxes. Here's how it works:</span></span>
  
- <span data-ttu-id="4202a-108">pst 가져오기 작업을 만들고 전송 하 고 나면 pst 파일이 Microsoft 클라우드의 Azure storage 영역에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-108">After you create and submit a PST import job, PST files are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
    
- <span data-ttu-id="4202a-109">Office 365에서는 사서함 항목의 보존 기간 및 pst 파일에 포함 된 다양 한 메시지 유형을 식별 하 여 pst 파일의 데이터를 안전 하 고 안전한 방식으로 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-109">Office 365 analyzes the data in the PST files, in a safe and secure manner, by identifying the age of the mailbox items and the different message types included in the PST files.</span></span>
    
- <span data-ttu-id="4202a-p103">분석이 완료 되 고 데이터를 가져올 준비가 되 면 PST 파일의 모든 데이터를 그대로 가져오거나 가져올 데이터를 제어 하는 필터를 설정 하 여 가져온 데이터를 지울 수 있는 옵션이 있습니다. 예를 들어 다음을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p103">When the analysis is complete and the data is ready to import, you have the option to import all data in the PST files as is or trim the data that's imported by setting filters that control what data gets imported. For example, you can choose to:</span></span>
    
  - <span data-ttu-id="4202a-112">특정 연령에 게 있는 항목만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-112">Import only items of a certain age.</span></span>
    
  - <span data-ttu-id="4202a-113">선택한 메시지 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-113">Import selected message types.</span></span>
    
  - <span data-ttu-id="4202a-114">특정 사용자가 보내거나 받은 메시지를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-114">Exclude messages sent or received by specific people.</span></span>
    
- <span data-ttu-id="4202a-115">필터 설정을 구성한 후에는 Office 365에서 가져오기 작업에 지정 된 대상 사서함에 필터링 기준을 충족 하는 데이터만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-115">After you configure the filter settings, Office 365 imports only the data that meets the filtering criteria to the target mailboxes specified in the import job.</span></span>
    
<span data-ttu-id="4202a-116">다음 그림에서는 지능형 가져오기 프로세스를 보여 주고 수행 하는 작업 및 Office 365에서 수행 하는 작업을 강조 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-116">The following graphic shows the Intelligent Import process, and highlights the tasks you perform and the tasks performed by Office 365.</span></span>
  
![Office 365의 지능형 가져오기 프로세스](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a><span data-ttu-id="4202a-118">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="4202a-118">Before you begin</span></span>

- <span data-ttu-id="4202a-p104">이 항목의 단계에서는 네트워크 업로드 또는 드라이브 전달을 사용 하 여 Office 365 가져오기 서비스에 PST 가져오기 작업을 만든 것으로 가정 합니다. 단계별 지침은 다음 항목 중 하나를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4202a-p104">The steps in this topic assume that you've created a PST import job in the Office 365 Import service by using network upload or drive shipping. For step-by-step instructions, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="4202a-121">네트워크 업로드를 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="4202a-121">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
    
  - [<span data-ttu-id="4202a-122">드라이브 발송을 사용하여 PST 파일을 Office 365로 가져오기</span><span class="sxs-lookup"><span data-stu-id="4202a-122">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- <span data-ttu-id="4202a-p105">네트워크 업로드를 사용 하 여 가져오기 작업을 만든 후에는 office 365 보안 &amp; 및 준수 센터의 가져오기 페이지에서 가져오기 작업의 상태가 **진행**중으로 설정 되며,이는 office 365에서 PST 파일의 데이터를 분석 하는 것을 의미 합니다. 업로드. 새로](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) 고치기 새로 **고침**![을 클릭 하 여 가져오기 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p105">After you create an import job by using network upload, the status for the import job on the Import page in Office 365 Security &amp; Compliance Center is set to **Analysis in progress**, which means that Office 365 is analyzing the data in the PST files that you uploaded. Click **Refresh**![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) to update the status for the import job.</span></span> 
    
- <span data-ttu-id="4202a-125">드라이브 전달 가져오기 작업의 경우 Microsoft 데이터 센터 직원이 하드 드라이브를 수신 하 고 조직의 Azure storage 영역에 PST 파일을 업로드 한 후에 Office 365에서 데이터를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-125">For drive shipping import jobs, the data will be analyzed by Office 365 after Microsoft data center personnel receive your hard drive and upload the PST files to the Azure storage area for your organization.</span></span>
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a><span data-ttu-id="4202a-126">사서함으로 가져오는 데이터 필터링</span><span class="sxs-lookup"><span data-stu-id="4202a-126">Filter data that gets imported to mailboxes</span></span>

<span data-ttu-id="4202a-127">PST 가져오기 작업을 만든 후에는 다음 단계에 따라 데이터를 Office 365로 가져오기 전에 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-127">After you've created a PST import job, follow these steps to filter the data before you import it to Office 365.</span></span>
  
1. <span data-ttu-id="4202a-128">으로 이동 [https://protection.office.com/](https://protection.office.com/) 하 고 Office 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-128">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="4202a-129">Office 365 보안 &amp; 및 준수 센터의 왼쪽 창에서 **데이터 거 버 넌 스** \> **가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-129">In the left pane of the Office 365 Security &amp; Compliance Center, click **Data governance** \> **Import**.</span></span>
    
    <span data-ttu-id="4202a-p106">조직의 가져오기 작업은 **가져오기** 페이지에 나열 됩니다. **Status (상태** ) 열의 **분석 완료** 값은 Office 365에서 분석 되었으며 가져올 준비가 된 가져오기 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p106">The import jobs for your organization are listed on the **Import** page. Note that the **Analysis completed** value in the **Status** column indicates the import jobs that have been analyzed by Office 365 and are ready for you to import.</span></span> 
    
    ![분석 완료 상태는 Office 365에서 PST 파일의 데이터를 분석 했음을 나타냅니다.](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. <span data-ttu-id="4202a-133">완료 하려는 가져오기 작업에 대해 **준비를 클릭 하 여 Office 365로 가져옵니다** .</span><span class="sxs-lookup"><span data-stu-id="4202a-133">Click **Ready to import to Office 365** for the import job that you want to complete.</span></span> 
    
    <span data-ttu-id="4202a-134">가져오기 작업에 대 한 기타 정보 및 PST 파일에 대 한 정보가 포함 된 플라이 아웃 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-134">A fly out page is displayed with information about the PST files and other information about the import job.</span></span>
    
4. <span data-ttu-id="4202a-135">**Office 365로 가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-135">Click **Import to Office 365**.</span></span>
    
    <span data-ttu-id="4202a-p107">**데이터 필터링** 페이지가 표시 됩니다. 데이터의 기간에 대 한 정보를 비롯 하 여 가져오기 작업에 대 한 PST 파일의 데이터에 대 한 데이터 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p107">The **Filter your data** page is displayed. It contains data insights about the data in the PST files for the import job, including information about the age of the data.</span></span> 
    
    ![데이터 필터링 페이지에는 가져오기 작업에 대 한 PST 파일의 데이터 정보가 표시 됩니다.](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. <span data-ttu-id="4202a-139">Office 365로 가져오는 데이터를 트리밍할 지 여부에 따라 **데이터를 필터링**하 시겠습니까?에서 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-139">Based on whether or not you want to trim the data that's imported to Office 365, under **Do you want to filter your data?**, do one of the following:</span></span>
    
    <span data-ttu-id="4202a-p108">**예, 가져오기를 수행 하기 전에 필터링 하** 여 가져온 데이터를 트리밍하고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p108">a. Click **Yes, I want to filter it before importing** to trim the data that you import, and then click **Next**.</span></span>
    
    <span data-ttu-id="4202a-142">office \* **로 데이터 가져오기 365 페이지** 에는 office 365에서 수행한 분석의 자세한 데이터 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-142">The **Import data to Office 365 page** page is displayed with detailed data insights from the analysis that Office 365 performed.</span></span> 
    
    ![Office 365는 PST 파일 분석을 통해 자세한 데이터 정보를 표시 합니다.](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    <span data-ttu-id="4202a-p109">이 페이지의 그래프에는 가져올 데이터의 양이 표시 됩니다. PST 파일에 있는 각 메시지 유형에 대 한 정보가 그래프에 표시 됩니다. 각 막대 위에 커서를 놓아 해당 메시지 유형에 대 한 특정 정보를 표시할 수 있습니다. PST 파일의 분석을 기반으로 하는 다른 연령 값이 포함 된 드롭다운 목록도 있습니다. 드롭다운 목록에서 나이를 선택 하면 그래프가 업데이트 되어 선택한 기간 동안 가져올 데이터의 양이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p109">The graph on this page shows the amount of data that will be imported. Information about each message type found in the PST files is displayed in the graph. You can hover the cursor over each bar to display specific information about that message type. There is also a drop-down list with different age values based on the analysis of the PST files. When you select an age in the drop-down list, the graph is updated to show how much data will be imported for the selected age.</span></span> 
    
    <span data-ttu-id="4202a-p110">b. 가져올 데이터의 양을 줄이기 위한 추가 필터를 구성 하려면 **기타 필터링 옵션**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p110">b. To configure addition filters to reduce the amount of data that's imported, click **More filtering options**.</span></span>
    
    ![기타 옵션 페이지에서 필터를 구성 하 여 가져올 데이터를 잘라냅니다.](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    <span data-ttu-id="4202a-152">다음 필터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-152">You can configure these filters:</span></span>
    
      - <span data-ttu-id="4202a-p111">**age** -지정 된 기간 보다 더 최신인 항목만 가져오게 되도록 기간을 선택 합니다. Office 365에서 **연령** 필터에 대 한 연령별 버킷을 결정 하는 방법에 대 한 자세한 [내용은 More information](filter-data-when-importing-pst-files.md#moreinfo) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4202a-p111">**Age** - Select an age so only items that are newer than the specified age will be imported. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a description about how Office 365 determines the age buckets for the **Age** filter.</span></span> 
    
      - <span data-ttu-id="4202a-p112">**Type** -이 섹션에는 가져오기 작업에 대 한 PST 파일에서 찾은 모든 메시지 유형이 표시 됩니다. 제외 하려는 메시지 유형 옆의 상자를 선택 취소할 수 있습니다. 다른 메시지 유형은 제외할 수 없습니다. 다른 범주에 포함 된 사서함 항목의 목록에 대해서는 [추가 정보](filter-data-when-importing-pst-files.md#moreinfo) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4202a-p112">**Type** - This section shows all the message types that were found in the PST files for the import job. You can uncheck a box next to a message type that you want to exclude. Note that you can't exclude the Other message type. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a list of mailbox items that are included in the Other category.</span></span> 
    
      - <span data-ttu-id="4202a-p113">**사용자** -특정 사용자가 보내거나 받는 메시지를 제외할 수 있습니다. 보낸 사람: 필드에 표시 되는 사용자를 제외 하거나 메시지의 참조: 필드에는 받는 사람 유형 옆에 있는 **사용자 제외** 를 클릭 합니다. 해당 사용자의 전자 메일 주소 (SMTP 주소)를 입력 하 \*\*\*\*![고 새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) 추가를 클릭 하 여 해당 받는 사람 유형에 대 한 제외 된 사용자 목록에 추가한 다음 **저장** 을 클릭 하 여 제외 된 사용자 목록을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p113">**Users** - You can exclude messages that are sent or received by specific people. To exclude people who appear in the From: field, To: field, or the Cc: field of messages, click **Exclude users** next to that recipient type. Type the email address (SMTP address) of the person, click **Add**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) to add them to the list of excluded users for that recipient type, and then click **Save** to save the list of excluded users.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="4202a-p114">Office 365에는 **사용자** 필터를 설정 했을 때 발생 하는 데이터 정보가 표시 되지 않습니다. 그러나 특정 사용자가 보내거나 받는 메시지를 제외 하도록이 필터를 설정 하는 경우 해당 메시지는 실제 가져오기 프로세스 중에 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p114">Office 365 doesn't show data insights that result from setting the **People** filter. However, if you set this filter to exclude messages sent or received by specific people, those messages will be excluded during the actual import process.</span></span> 
  
    <span data-ttu-id="4202a-p115">c. 필터 설정을 저장 하려면 **기타 필터링 옵션** 페이지에서 **적용** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p115">c. Click **Apply** in the **More filtering options** fly out page to save your filter settings.</span></span> 
    
    <span data-ttu-id="4202a-p116">**Office로 데이터 가져오기 365** 페이지의 데이터 정보는 필터 설정에 따라 가져올 데이터의 총 양을 비롯 하 여 필터 설정에 따라 업데이트 됩니다. 필터 설정에 대 한 요약도 표시 됩니다. 필요한 경우 필터 옆의 **편집** 을 클릭 하 여 설정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p116">The data insights on the **Import data to Office 365** page are updated based on your filter settings, including the total amount of data that will be imported based on the filter settings. Note that a summary of the filter settings is also shown. You can click **Edit** next to a filter to change the setting if necessary.</span></span> 
    
    ![필터 설정에 따라 데이터 정보가 업데이트 됩니다.](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    <span data-ttu-id="4202a-p117">d. **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p117">d. Click **Next**.</span></span>
    
    <span data-ttu-id="4202a-p118">필터 설정이 표시 된 상태 페이지가 표시 됩니다. 다시 한번, 필터 설정을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p118">A status page is displayed showing your filter settings. Again, you can edit any of the filter settings.</span></span>
    
    <span data-ttu-id="4202a-p119">e. **데이터 가져오기를** 클릭 하 여 가져오기를 시작 합니다. 가져올 데이터의 총 양이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p119">e. Click **Import data** to start the import . Note that the total amount of data that will be imported is displayed.</span></span> 
    
    <span data-ttu-id="4202a-177">또는</span><span class="sxs-lookup"><span data-stu-id="4202a-177">Or</span></span>
    
    <span data-ttu-id="4202a-p120">a. **아니요, 모든 항목을 가져와서** PST 파일의 모든 데이터를 Office 365로 가져오고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p120">a. Click **No, I want to import everything** to import all data in the PST files to Office 365, and then click **Next**.</span></span>
    
    <span data-ttu-id="4202a-p121">b. **Office로 데이터 가져오기 365** 페이지에서 **데이터 가져오기를** 클릭 하 여 가져오기를 시작 합니다. 가져올 데이터의 총 양이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p121">b. On the **Import data to Office 365** page, click **Import data** to start the import. Note that the total amount of data that will be imported is displayed.</span></span> 
    
6. <span data-ttu-id="4202a-p122">**가져오기** 페이지에서 \*\*\*\* ![새로](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png)고침 새로고침을 클릭 합니다. 가져오기 작업의 상태가 **상태** 열에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p122">On the **Import** page, click **Refresh** ![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). The status for the import job is displayed in the **Status** column.</span></span> 
    
7. <span data-ttu-id="4202a-185">각 PST 파일의 상태와 구성한 필터 설정 등 자세한 정보를 표시 하려면 가져오기 작업을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-185">Click the import the job to display more detailed information, such as the status for each PST file and the filter settings that you configured.</span></span>

  
## <a name="more-information"></a><span data-ttu-id="4202a-186">추가 정보</span><span class="sxs-lookup"><span data-stu-id="4202a-186">More information</span></span>

- <span data-ttu-id="4202a-p123">Office 365이 보존 기간 필터의 증가를 어떻게 결정 하나요? PST 파일을 분석 하면 Office 365에서 각 항목의 보내거나 받은 시간 스탬프를 조사 합니다 (항목에 보낸 시간과 받은 타임 스탬프가 모두 있는 경우 가장 오래 된 날짜가 선택 됨). 그런 다음 Office 365는 해당 타임 스탬프에 대 한 연도 값을 확인 하 고이를 현재 날짜와 비교 하 여 항목의 보존 기간을 결정 합니다. 이러한 연령는 **보존 기간** 필터의 드롭다운 목록에 있는 값으로 사용 됩니다. 예를 들어 PST 파일에 2016, 2015 및 2014의 메시지가 있는 경우 **Age** 필터의 값은 **1 년**, **2 년**, **3 년**이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p123">How does Office 365 determine the increments for the age filter? When Office 365 analyzes a PST file, it looks at the sent or received time stamp of each item (if an item has both a sent and received timestamp, the oldest date is selected). Then Office 365 looks at the year value for that timestamp and compares it to the current date to determine the age of the item. These ages are then used as the values in the drop-down list for the **Age** filter. For example, if a PST file has messages from 2016, 2015, and 2014, then values in the **Age** filter would be **1 year**, **2 years**, and **3 years**.</span></span>
    
- <span data-ttu-id="4202a-p124">다음 표에는 기타 **옵션** 페이지의 기타 범주에 있는 **다른** 종류의 항목에 \*\*\*\* 포함 된 메시지 유형이 표시 됩니다 (이전 절차의 5b 단계 참조). 현재는 pst를 Office 365로 가져올 때 "기타" 범주의 항목을 제외할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-p124">The following table lists the message types that are included in the **Other** category in the **Type** filter on the **More options** fly out page (see Step 5b in the previous procedure). Currently, you can't exclude items in the "Other" category when you import PSTs to Office 365.</span></span> 
    
    |<span data-ttu-id="4202a-194">**메시지 클래스 ID**</span><span class="sxs-lookup"><span data-stu-id="4202a-194">**Message class ID**</span></span>|<span data-ttu-id="4202a-195">**이 메시지 클래스를 사용 하는 사서함 항목**</span><span class="sxs-lookup"><span data-stu-id="4202a-195">**Mailbox items that use this message class**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="4202a-196">ipm.note. 내용</span><span class="sxs-lookup"><span data-stu-id="4202a-196">IPM.Activity</span></span>  <br/> |<span data-ttu-id="4202a-197">업무 일지 항목</span><span class="sxs-lookup"><span data-stu-id="4202a-197">Journal entries</span></span>  <br/> |
    |<span data-ttu-id="4202a-198">ipm.note. 오피스</span><span class="sxs-lookup"><span data-stu-id="4202a-198">IPM.Document</span></span>  <br/> |<span data-ttu-id="4202a-199">문서 및 파일 (전자 메일 메시지에 첨부 되지 않음)</span><span class="sxs-lookup"><span data-stu-id="4202a-199">Documents and files (not attached to an email message)</span></span>  <br/> |
    |<span data-ttu-id="4202a-200">ipm.note. 파일</span><span class="sxs-lookup"><span data-stu-id="4202a-200">IPM.File</span></span>  <br/> |<span data-ttu-id="4202a-201">(IPM과 동일 합니다. 오피스</span><span class="sxs-lookup"><span data-stu-id="4202a-201">(same as IPM.Document)</span></span>  <br/> |
    |<span data-ttu-id="4202a-202">ipm.note. Note. IMC. 알림</span><span class="sxs-lookup"><span data-stu-id="4202a-202">IPM.Note.IMC.Notification</span></span>  <br/> |<span data-ttu-id="4202a-203">인터넷 메일 Connect에서 전송 되는 보고서 (인터넷에 대 한 Exchange Server 게이트웨이)</span><span class="sxs-lookup"><span data-stu-id="4202a-203">Reports sent by Internet Mail Connect, which is the Exchange Server gateway to the Internet</span></span>  <br/> |
    |<span data-ttu-id="4202a-204">ipm.note. Note. Microsoft 팩스</span><span class="sxs-lookup"><span data-stu-id="4202a-204">IPM.Note.Microsoft.Fax</span></span>  <br/> |<span data-ttu-id="4202a-205">팩스 메시지</span><span class="sxs-lookup"><span data-stu-id="4202a-205">Fax messages</span></span>  <br/> |
    |<span data-ttu-id="4202a-206">ipm.note. 주의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4202a-206">IPM.Note.Rules.Oof.Template.Microsoft</span></span>  <br/> |<span data-ttu-id="4202a-207">부재 중 자동 회신 메시지</span><span class="sxs-lookup"><span data-stu-id="4202a-207">Out-of-office auto-reply messages</span></span>  <br/> |
    |<span data-ttu-id="4202a-208">ipm.note. ReplyTemplate. Microsoft</span><span class="sxs-lookup"><span data-stu-id="4202a-208">IPM.Note.Rules.ReplyTemplate.Microsoft</span></span>  <br/> |<span data-ttu-id="4202a-209">받은 편지함 규칙에 의해 전송 된 회신</span><span class="sxs-lookup"><span data-stu-id="4202a-209">Replies sent by an inbox rule</span></span>  <br/> |
    |<span data-ttu-id="4202a-210">ipm.note. OLE. 클래스인</span><span class="sxs-lookup"><span data-stu-id="4202a-210">IPM.OLE.Class</span></span>  <br/> |<span data-ttu-id="4202a-211">되풀이 항목에 대 한 예외</span><span class="sxs-lookup"><span data-stu-id="4202a-211">Exceptions for a recurring series</span></span>  <br/> |
    |<span data-ttu-id="4202a-212">ipm.note. 회수 보고서</span><span class="sxs-lookup"><span data-stu-id="4202a-212">IPM.Recall.Report</span></span>  <br/> |<span data-ttu-id="4202a-213">메시지 회수 보고서</span><span class="sxs-lookup"><span data-stu-id="4202a-213">Message recall reports</span></span>  <br/> |
    |<span data-ttu-id="4202a-214">ipm.note. Remote</span><span class="sxs-lookup"><span data-stu-id="4202a-214">IPM.Remote</span></span>  <br/> |<span data-ttu-id="4202a-215">원격 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="4202a-215">Remote mail messages</span></span>  <br/> |
    |<span data-ttu-id="4202a-216">ipm.note. Report</span><span class="sxs-lookup"><span data-stu-id="4202a-216">IPM.Report</span></span>  <br/> |<span data-ttu-id="4202a-217">항목 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="4202a-217">Item status reports</span></span>  <br/> |
