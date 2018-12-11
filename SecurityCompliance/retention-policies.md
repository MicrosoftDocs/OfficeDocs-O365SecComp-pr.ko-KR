---
title: 보존 정책 개요
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 11/16/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 5e377752-700d-4870-9b6d-12bfc12d2423
description: 보존 정책을 사용하면 콘텐츠를 보존할지, 삭제할지, 아니면 보존했다가 삭제할지, 단일 정책을 전체 조직에 적용할지 아니면 특정 위치나 사용자에게 적용할지, 정책을 모든 콘텐츠에 적용할지 아니면 특정 조건에 부합되는 콘텐츠에만 적용할지 등을 자동으로 결정할 수 있습니다.
ms.openlocfilehash: 57f782046fcac2bd28830a0204e0b663d69de842
ms.sourcegitcommit: 8c5a88433cff23c59b436260808cf3d91b06fdef
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/07/2018
ms.locfileid: "27194709"
---
# <a name="overview-of-retention-policies"></a><span data-ttu-id="44e24-103">보존 정책 개요</span><span class="sxs-lookup"><span data-stu-id="44e24-103">Overview of retention policies</span></span>

<span data-ttu-id="44e24-p101">대부분의 조직에서는 전자 메일, 문서, 인스턴트 메시지 등을 비롯한 데이터의 양과 복잡성이 매일 계속해서 증가하고 있습니다. 이러한 정보를 효과적으로 관리하거나 제어하는 일은 다음 작업을 수행해야 하므로 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p101">For most organizations, the volume and complexity of their data is increasing daily - email, documents, instant messages, and more. Effectively managing or governing this information is important because you need to:</span></span>
  
- <span data-ttu-id="44e24-106">**산업 규정 및 내부 정책을 자동으로 준수** - 최소 기간 동안 콘텐츠를 보존하도록 요구합니다. 예를 들어 Sarbanes-Oxley Act에서는 7년 동안 특정 유형의 콘텐츠를 보존하도록 요구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-106">**Comply proactively with industry regulations and internal policies** that require you to retain content for a minimum period of time - for example, the Sarbanes-Oxley Act might require you to retain certain types of content for seven years.</span></span> 
    
- <span data-ttu-id="44e24-107">**소송 또는 보안 위반 시 위험 감소** - 더 이상 보존할 필요가 없는 오래된 콘텐츠를 영구적으로 삭제</span><span class="sxs-lookup"><span data-stu-id="44e24-107">**Reduce your risk in the event of litigation or a security breach** by permanently deleting old content that you're no longer required to keep.</span></span> 
    
- <span data-ttu-id="44e24-108">**조직에서 효과적이면서 좀 더 민첩하게 지식을 공유하도록 지원** - 사용자가 관련이 있는 최신 콘텐츠만 사용하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-108">**Help your organization to share knowledge effectively and be more agile** by ensuring that your users work only with content that's current and relevant to them.</span></span> 
    
<span data-ttu-id="44e24-p102">Office 365의 보존 정책은 이러한 모든 목표를 달성하는 데 도움을 줄 수 있습니다. 일반적으로 콘텐츠를 관리하려면 다음 두 가지 작업이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p102">A retention policy in Office 365 can help you achieve all of these goals. Managing content commonly requires two actions:</span></span>
  
- <span data-ttu-id="44e24-111">**보존** - 콘텐츠가 보존 기간이 끝나기 전에 영구적으로 삭제되지 않도록 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-111">**Retaining** content so that it can't be permanently deleted before the end of the retention period.</span></span> 
    
- <span data-ttu-id="44e24-112">**삭제** - 보존 기간이 끝나면 콘텐츠를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-112">**Deleting** content permanently at the end of the retention period.</span></span> 
    
<span data-ttu-id="44e24-113">보존 정책을 사용하여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-113">With a retention policy, you can:</span></span>
  
- <span data-ttu-id="44e24-114">있는지 여부를 콘텐츠를 보존할지, 삭제할지, 아니면 보존했다가 삭제할지를 자동으로 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-114">Decide proactively whether to retain content, delete content, or both - retain and then delete the content.</span></span>
    
- <span data-ttu-id="44e24-115">전체 조직 또는 특정 위치나 사용자에는 단일 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-115">Apply a single policy to the entire organization or just specific locations or users.</span></span>
    
- <span data-ttu-id="44e24-116">모든 콘텐츠 또는 특정 조건을 충족하는 콘텐츠(예: 특정 키워드 또는 [특정 유형의 중요 정보](what-the-sensitive-information-types-look-for.md)를 포함하는 콘텐츠)에 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-116">Apply a policy to all content or just content meeting certain conditions, such as content containing specific keywords or [specific types of sensitive information](what-the-sensitive-information-types-look-for.md).</span></span>
    
<span data-ttu-id="44e24-p103">콘텐츠가 보존 정책을 따르는 경우라도 콘텐츠는 원래 위치에 그대로 보존되므로 아무 것도 변경되지 않는 것과 같이, 계속해서 콘텐츠를 편집하고 사용할 수 있습니다. 그러나 보존 정책을 따르는 콘텐츠를 다른 사용자가 편집 또는 삭제한 경우에는 복사본이 안전한 위치에 저장되어 정책이 적용되는 동안 이 위치에 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p103">When content is subject to a retention policy, people can continue to edit and work with the content as if nothing's changed because the content is retained in place, in its original location. But if someone edits or deletes content that's subject to the policy, a copy is saved to a secure location where it's retained while the policy is in effect.</span></span>
  
<span data-ttu-id="44e24-p104">마지막으로 일부 조직에서는 SEC(Securities and Exchange Commission) 규칙 17a-4와 같은 규정을 준수해야 합니다. 따라서 예약 정책을 켠 후에는 끄거나 덜 제한적인 정책으로 변경할 수 없습니다. 이 요구 사항을 위해서는 보존 잠금을 사용할 수 있습니다. 정책이 잠궈지면 관리자를 비롯한 어느 누구도 정책을 해제하거나 덜 제한적으로 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p104">Finally, some organizations might need to comply with regulations such as Securities and Exchange Commission (SEC) Rule 17a-4, which requires that after a retention policy is turned on, it cannot be turned off or made less restrictive. To meet this requirement, you can use Preservation Lock. After a policy's been locked, no one—including the administrator—can turn off the policy or make it less restrictive.</span></span>
  
<span data-ttu-id="44e24-122">Office 365 보안 및 준수 센터의 **보존** 페이지에서 보존 정책을 만들고 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-122">You create and manage retention policies on the **Retention** page in the Office 365 Security &amp; Compliance Center.</span></span> 
  
![보안 및 준수 센터의 보존 페이지](media/107fc33a-6a29-44d1-85e4-0efef0544147.png)
  
> [!NOTE]
> <span data-ttu-id="44e24-p105">보존 정책에 Exchange Online 사서함을 포함하려면 사서함에 Exchange Online 요금제 2 라이선스가 할당되어야 합니다. 사서함에 Exchange Online 요금제 1 라이선스가 할당되면 보존 정책에 포함하기 위해 별도의 Exchange Online Archiving 라이선스를 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p105">To include an Exchange Online mailbox in a retention policy, the mailbox must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to include it in a retention policy.</span></span> 
  
## <a name="how-a-retention-policy-works-with-content-in-place"></a><span data-ttu-id="44e24-126">보존 정책이 원본 위치의 콘텐츠에 작동하는 방식</span><span class="sxs-lookup"><span data-stu-id="44e24-126">How a retention policy works with content in place</span></span>

<span data-ttu-id="44e24-p106">보존 정책에 사이트나 사서함과 같은 위치를 포함하면 콘텐츠가 원본 위치에 남아 있게 됩니다. 사용자는 아무 내용도 변경되지 않은 것처럼 문서 또는 메일을 계속 사용할 수 있습니다. 그렇지만 정책에 포함된 콘텐츠를 편집하거나 삭제하면 정책 적용 시 존재했던 콘텐츠의 사본이 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p106">When you include a location such as a site or mailbox in a retention policy, the content remains in its original location. People can continue to work with their documents or mail as if nothing's changed. But if they edit or delete content that's included in the policy, a copy of the content as it existed when you applied the policy is retained.</span></span>
  
<span data-ttu-id="44e24-p107">사이트의 경우, 사용자가 콘텐츠를 편집하거나 삭제할 경우 원본 콘텐츠의 사본이 자료 보존 라이브러리에 보존되고, 전자 메일 및 공용 폴더의 경우에는 사본이 복구 가능한 항목 폴더에 보존됩니다. 이러한 보안 위치 및 보존된 콘텐츠는 대부분의 사용자에게 표시되지 않습니다. 보존 정책을 사용하면 사용자는 해당 콘텐츠에 정책이 적용된다는 사실도 알 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p107">For sites, a copy of the original content is retained in the Preservation Hold library when users edit or delete it; for email and public folders, the copy is retained in the Recoverable Items folder. These secure locations and the retained content are not visible to most people. With a retention policy, people do not even need to know that their content is subject to the policy.</span></span>
  
<span data-ttu-id="44e24-133">참고:</span><span class="sxs-lookup"><span data-stu-id="44e24-133">Notes:</span></span>
  
- <span data-ttu-id="44e24-134">Skype 콘텐츠는 Exchange에 저장되며 이때 정책은 메시지 유형(전자 메일 또는 대화)에 따라 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-134">Skype content is stored in Exchange, where the policy is applied based on message type (email or conversation).</span></span>
    
- <span data-ttu-id="44e24-135">Office 365 그룹에 적용되는 보존 정책에는 그룹 사서함과 사이트가 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-135">A retention policy applied to an Office 365 group includes both the group mailbox and site.</span></span>
    
### <a name="content-in-onedrive-accounts-and-sharepoint-sites"></a><span data-ttu-id="44e24-136">OneDrive 계정 및 SharePoint 사이트의 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="44e24-136">Content in OneDrive accounts and SharePoint sites</span></span>

<span data-ttu-id="44e24-p108">보존 정책이 사이트 수준에서 적용됩니다. 자료 보존 라이브러리가 아직 없는 경우 보존 정책에 SharePoint 사이트 또는 OneDrive 계정을 포함시키면 하나가 생성됩니다. 자료 보존 라이브러리는 사이트 모음 관리자만 볼 수 있기 때문에 대부분의 사용자는 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p108">A retention policy is applied at the level of a site. When you include a SharePoint site or OneDrive account in a retention policy, a Preservation Hold library is created, if one doesn't already exist. Most users can't view the Preservation Hold library because it's visible only to site collection administrators.</span></span>
  
<span data-ttu-id="44e24-p109">사용자가 보존 정책을 따르는 사이트의 콘텐츠를 변경하거나 삭제하려고 하면 보존 정책은 먼저 보존 정책이 적용된 이후 콘텐츠가 변경되었는지 여부를 확인합니다. 보존 정책이 적용되고 처음 변경한 경우라면 보존 정책은 해당 콘텐츠를 자료 보존 라이브러리로 복사하고 해당 사용자가 원본 콘텐츠를 변경하거나 삭제할 수 있도록 허용합니다. 사이트의 콘텐츠는 보존 정책에서 사용하는 쿼리 필터와 일치하지 않더라도 자료 보존 라이브러리로 복사될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p109">If a person attempts to change or delete content in a site that's subject to a retention policy, first the policy checks whether the content's been changed since the policy was applied. If this is the first change since the policy was applied, the retention policy copies the content to the Preservation Hold library, and then allows the person to change or delete the original content. Note that any content in the site can be copied to the Preservation Hold library, even if the content does not match the query used by the retention policy.</span></span>
  
<span data-ttu-id="44e24-p110">그런 다음, 타이머 작업이 자료 보존 라이브러리를 정리합니다. 타이머 작업은 주기적으로 실행되면서 자료 보존 라이브러리의 모든 콘텐츠를 사이트의 보존 정책에서 사용하는 모든 쿼리와 비교합니다. 콘텐츠가 하나 이상의 쿼리와 일치하지 않는 한, 타이머 작업은 자료 보존 라이브러리에서 해당 콘텐츠를 영구히 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p110">Then a timer job cleans up the Preservation Hold library. The timer job runs periodically and compares all content in the Preservation Hold library to all of the queries used by the retention policies on the site. Unless content matches at least one of the queries, the timer job permanently deletes the content from the Preservation Hold library.</span></span>
  
<span data-ttu-id="44e24-p111">이러한 방식은 보존 정책이 적용될 때 존재하던 콘텐츠에 적용됩니다. 또한 사이트가 정책에 포함된 후에 해당 사이트에서 생성되었거나 추가된 새 콘텐츠는 삭제 후에도 보존됩니다. 그렇지만 새 콘텐츠는 처음 편집할 때는 자료 보존 라이브러리에 복사되지 않고 삭제되었을 때만 복사됩니다. 파일의 모든 버전을 보존하려면 버전 관리 기능을 켜야 합니다. 버전 관리에 대한 내용은 아래 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p111">The previous applies to content that exists when the retention policy is applied. In addition, any new content that's created or added to the site after it was included in the policy will be retained after deletion. However, new content isn't copied to the Preservation Hold library the first time it's edited, only when it's deleted. To retain all versions of a file, you need to turn on versioning — see the below section on versioning.</span></span>
  
<span data-ttu-id="44e24-p112">보존 정책이 적용되는 라이브러리, 목록, 폴더 또는 사이트를 삭제하려고 하는 경우 오류가 표시됩니다. 정책이 적용되는 폴더의 파일을 먼저 이동하거나 삭제하면 폴더를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p112">Note that a user will receive an error if they try to delete a library, list, folder, or site that's subject to a retention policy. A user can delete a folder if they first move or delete any files in the folder that are subject to the policy.</span></span>
  
![SharePoint 및 OneDrive의 보존 흐름 다이어그램](media/858702f8-5a09-4464-86d0-3b16fed800f3.png)
  
<span data-ttu-id="44e24-153">보존 정책이 OneDrive 계정 또는 SharePoint 사이트에 할당되면 콘텐츠는 다음 두 가지 경로 중 하나를 따를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-153">After a retention policy is assigned to a OneDrive account or SharePoint site, content can follow one of two paths:</span></span>
  
1. <span data-ttu-id="44e24-p113">**보존 기간 동안 콘텐츠가 수정되거나 삭제되는 경우** 보존 정책이 할당되었을 때 존재하던 원본 콘텐츠의 사본이 자료 보존 라이브러리에 만들어집니다. 여기에서 타이머 작업이 주기적으로 실행되고 해당 보존 기간이 만료된 항목을 식별되며, 이러한 항목은 보존 기간이 종료되고 7일 이내에 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p113">**If the content is modified or deleted** during the retention period, a copy of the original content as it existed when the retention policy was assigned is created in the Preservation Hold library. There, a timer job runs periodically and identifies items whose retention period has expired, and these items are permanently deleted within seven days of the end of the retention period.</span></span> 
    
2. <span data-ttu-id="44e24-p114">**보존 기간 동안 콘텐츠 수정되거나 삭제되지 않는 경우** 보존 기간이 끝나면 1단계 휴지통으로 이동됩니다. 사용자가 여기에서 해당 콘텐츠를 삭제하거나 이 휴지통을 비우면(제거라고도 함) 문서는 2단계 휴지통으로 이동됩니다. 93일의 보존 기간은 1단계 및 2단계 휴지통 둘 다에 걸쳐 적용됩니다. 93일이 끝나면 문서는 해당 위치(1단계 또는 2단계 휴지통)에서 영구적으로 삭제됩니다. 휴지통은 인덱싱되지 않으므로 검색 시 해당 위치에서 콘텐츠가 검색되지 않습니다. 즉, eDiscovery 보존 기능은 휴지통에 있는 콘텐츠를 보류하기 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p114">**If the content is not modified or deleted** during the retention period, it's moved to the first-stage Recycle Bin at the end of the retention period. If a user deletes the content from there or empties this Recycle Bin (also known as purging), the document is moved to the second-stage Recycle Bin. A 93-day retention period spans both the first- and second-stage recycle bins. At the end of 93 days, the document is permanently deleted from wherever it resides, in either the first- or second-stage Recycle Bin. Note that the Recycle Bin is not indexed and therefore searches do not find content there. This means that an eDiscovery hold can't locate any content in the Recycle Bin in order to hold it.</span></span> 
    
### <a name="content-in-mailboxes-and-public-folders"></a><span data-ttu-id="44e24-161">사서함 및 공용 폴더의 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="44e24-161">Content in mailboxes and public folders</span></span>

<span data-ttu-id="44e24-p115">사용자의 메일, 일정 및 기타 항목의 경우 보존 정책은 사서함 수준에서 적용됩니다. 공용 폴더의 경우 사서함 수준이 아닌 폴더 수준에서 보존 정책이 적용됩니다. 사서함 및 공용 폴더 모두 항목을 보존하기 위해 복구 가능한 항목 폴더를 사용합니다. eDiscovery 권한을 부여 받은 사용자만 다른 사용자의 복구 가능한 항목 폴더에서 항목을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p115">For a user's mail, calendar, and other items, a retention policy is applied at the level of a mailbox. For a public folder, a retention policy is applied at the folder level, not the mailbox level. Both a mailbox and a public folder use the Recoverable Items folder to retain items. Only people whom have been assigned eDiscovery permissions can view items in another user's Recoverable Items folder.</span></span>
  
<span data-ttu-id="44e24-p116">사용자가 지운 편지함 폴더 이외의 폴더에서 메시지를 삭제하면 해당 메시지는 기본적으로 지운 편지함 폴더로 이동됩니다. 사용자가 지운 편지함 폴더에서 항목을 삭제하면 메시지가 복구할 수 있는 항목 폴더로 이동됩니다. 또한 사용자는 Shift+Delete를 눌러 항목을 일시적으로 삭제할 수 있습니다. 이 경우 지운 편지함 폴더가 무시되고 항목이 복구할 수 있는 항목 폴더로 바로 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p116">By default, when a person deletes a message in a folder other than the Deleted Items folder, the message is moved to the Deleted Items folder. When a person deletes an item in the Deleted Items folder, the message is moved to the Recoverable Items folder. In addition, a person can soft delete an item (SHIFT+DELETE) in any folder, which bypasses the Deleted Items folder and moves the item directly to the Recoverable Items folder.</span></span>
  
<span data-ttu-id="44e24-p117">프로세스는 복구 가능한 항목 폴더에서 정기적으로 항목을 평가합니다. 항목이 하나 이상의 보존 정책 규칙과 일치하지 않으면 항목은 복구 가능한 항목 폴더에서 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p117">A process periodically evaluates items in the Recoverable Items folder. If an item doesn't match the rules of at least one retention policy, the item is permanently deleted (also called hard deleted) from the Recoverable Items folder.</span></span>
  
<span data-ttu-id="44e24-p118">사용자가 메시지의 제목, 본문, 첨부 파일, 보낸 사람 및 받는 사람, 보낸 날짜 또는 받은 날짜와 같은 사서함 항목의 특정 속성을 변경하려고 하면 변경이 커밋되기 전에 원본 항목의 복사본이 복구 가능한 항목 폴더에 저장됩니다. 이 작업은 후속 변경이 있을 때마다 진행됩니다. 보존 기간이 끝나면 복구 가능한 항목 폴더의 사본이 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p118">When a person attempts to change certain properties of a mailbox item — such as the subject, body, attachments, senders and recipients, or date sent or received for a message — a copy of the original item is saved to the Recoverable Items folder before the change is committed. This happens for each subsequent change. At the end of the retention period, copies in the Recoverable Items folder are permanently deleted.</span></span>
  
<span data-ttu-id="44e24-p119">사용자가 조직을 떠나며 해당 사서함이 보존 정책에 포함된 경우 사용자의 Office 365 계정이 삭제되면 사서함은 비활성 사서함이 됩니다. 비활성 사서함의 콘텐츠는 해당 사서함이 비활성 상태가 되기 전에 지정된 보존 정책이 계속 적용되며, eDiscovery 검색에서 해당 콘텐츠를 사용할 수 있습니다. 자세한 내용은 [Exchange Online의 비활성 사서함](https://go.microsoft.com/fwlink/?linkid=846909)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p119">If a user leaves your organization, and their mailbox is included in a retention policy, the mailbox becomes an inactive mailbox when the user's Office 365 account is deleted. The contents of an inactive mailbox are still subject to any retention policy that was placed on the mailbox before it was made inactive, and the contents are available to an eDiscovery search. For more information, see [Inactive mailboxes in Exchange Online](https://go.microsoft.com/fwlink/?linkid=846909).</span></span>
  
![전자 메일 및 공용 폴더의 보존 흐름 다이어그램](media/88f174cc-bbf4-4305-93d7-0515f496c8f9.png)
  
<span data-ttu-id="44e24-178">보존 정책이 사서함 또는 공용 폴더에 할당되면 콘텐츠는 다음 두 가지 경로 중 하나를 따를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-178">After a retention policy is assigned to a mailbox or public folder, content can follow one of two paths:</span></span>
  
1. <span data-ttu-id="44e24-p120">**보존 기간 동안 사용자가 항목을 수정하거나 영구적으로 삭제하는 경우**(Shift + Delete 사용 또는 지운 편지함에서 삭제) 항목은 복구 가능한 항목 폴더로 이동(또는 편집의 경우 복사)됩니다. 여기에서 프로세스가 주기적으로 실행되고 보존 기간이 만료된 항목이 식별되며, 이러한 항목은 보존 기간이 끝나고 14일 이내에 영구적으로 삭제됩니다. 14일은 기본 설정이지만 최대 30일로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p120">**If the item is modified or permanently deleted** by the user (either SHIFT+DELETE or deleted from Deleted Items) during the retention period, the item is moved (or copied, in the case of edit) to the Recoverable Items folder. There, a process runs periodically and identifies items whose retention period has expired, and these items are permanently deleted within 14 days of the end of the retention period. Note that 14 days is the default setting, but it can be configured up to 30 days.</span></span> 
    
2. <span data-ttu-id="44e24-p121">**보존 기간 동안 항목이 수정되거나 삭제되지 않는 경우** 동일한 프로세스가 사서함의 모든 폴더에 대해 주기적으로 실행되고 보존 기간이 만료된 항목이 식별되며, 이러한 항목은 보존 기간이 끝나고 14일 이내에 영구적으로 삭제됩니다. 14일은 기본 설정이지만 최대 30일로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p121">**If the item is not modified or deleted** during the retention period, the same process runs periodically on all folders in the mailbox and identifies items whose retention period has expired, and these items are permanently deleted within 14 days of the end of the retention period. Note that 14 days is the default setting but it can be configured up to 30 days.</span></span> 
    
## <a name="how-a-retention-policy-works-with-document-versions-in-a-site"></a><span data-ttu-id="44e24-184">보존 정책이 사이트의 문서 버전에 작동하는 방식</span><span class="sxs-lookup"><span data-stu-id="44e24-184">How a retention policy works with document versions in a site</span></span>

<span data-ttu-id="44e24-p122">버전 관리는 SharePoint Online 및 비즈니스용 OneDrive에서 모든 문서 라이브러리의 기능입니다. 기본적으로 버전 관리는 최소 500개의 주 버전을 유지하며, 이 제한은 늘릴 수 있습니다. 자세한 내용은 [목록 또는 라이브러리의 버전 관리 사용 및 구성](https://support.office.com/article/1555d642-23ee-446a-990a-bcab618c7a37)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p122">Versioning is a feature of all document libraries in SharePoint Online and OneDrive for Business. By default, versioning retains a minimum of one hundred major versions, though you can increase this limit. For more information, see [Enable and configure versioning for a list or library](https://support.office.com/article/1555d642-23ee-446a-990a-bcab618c7a37).</span></span>
  
<span data-ttu-id="44e24-p123">보존 정책은 SharePoint 사이트 또는 OneDrive 계정에 있는 문서의 모든 버전을 유지합니다. 보존 정책이 적용되는 문서를 편집 또는 삭제할 때마다 버전이 자료 보존 라이브러리에 복사됩니다. 자료 보존 라이브러리에 있는 문서의 각 버전은 고유한 보존 기간이 있는 별도 항목으로 존재합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p123">A retention policy retains all versions of a document in a SharePoint site or OneDrive account. Each time a document subject to a retention policy is edited or deleted, a version is copied to the Preservation Hold library. Each version of a document in the Preservation Hold library exists as a separate item with its own retention period:</span></span>
  
- <span data-ttu-id="44e24-p124">보존 정책이 콘텐츠가 만들어진 시점을 기준으로 하는 경우 각 버전은 원본 문서와 동일한 만료 날짜를 갖습니다. 따라서 원본 문서 및 해당 버전은 동시에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p124">If the retention policy is based on when the content was created, each version has the same expiration date as the original document. The original document and its versions all expire at the same time.</span></span>
    
- <span data-ttu-id="44e24-p125">보존 정책이 콘텐츠가 마지막으로 수정된 시점을 기준으로 하는 경우 각 버전은 원본 문서가 해당 버전을 만들기 위해 수정된 시점을 기준으로 하는 자체 만료 날짜를 가집니다. 따라서 원본 문서와 해당 버전는 별도로 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p125">If the retention policy is based on when the content was last modified, each version has its own expiration date based on when the original document was modified to create that version. The original documents and its versions expire independently of each other.</span></span>
    
## <a name="retaining-content-for-a-specific-period-of-time"></a><span data-ttu-id="44e24-195">특정 기간 동안 콘텐츠 보존</span><span class="sxs-lookup"><span data-stu-id="44e24-195">Retaining content for a specific period of time</span></span>

<span data-ttu-id="44e24-p126">보존 정책을 사용하면 콘텐츠를 무한 기간 동안 또는 특정 일, 월 및 년 동안 보존할 수 있습니다. 콘텐츠가 보존되는 기간은 보존 정책이 적용된 시점이 아닌, 콘텐츠 사용 기간에 따라 계산됩니다. 사용 기간이 콘텐츠 생성 시점을 기준으로 할지 또는 (OneDrive 및 SharePoint) 마지막으로 수정된 시점을 기준으로 할지를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p126">With a retention policy, you can retain content indefinitely or for a specific number of days, months, or years. Note that the duration for how long content is retained is calculated from the age of the content, not from when the retention policy is applied. You can choose whether the age is based on when the content was created or (for OneDrive and SharePoint) when it was last modified.</span></span>
  
<span data-ttu-id="44e24-p127">예를 들어 사이트의 콘텐츠를 마지막으로 수정한 이후부터 7년 동안 보존하려고 하고 해당 사이트의 문서가 6년 동안 수정되지 않았다면, 문서는 수정되지 않은 1년 동안 더 보존됩니다. 문서를 다시 편집하면 문서 사용 기간은 마지막으로 수정한 날부터 계산되고 이후 7년 동안 더 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p127">For example, if you want to retain content in a site for seven years since it was last modified, and a document in that site hasn't been modified in six years, the document will be retained for only another year if it's not modified. If the document is edited again, the age of the document is calculated from the new last modified date, and it will be retained for another seven years.</span></span>
  
<span data-ttu-id="44e24-p128">마찬가지로 사서함의 콘텐츠를 7년 동안 보존하려고 하고 6년 전에 메시지가 전송된 경우 해당 메시지만 1년 동안 보존됩니다. Exchange 콘텐츠의 경우 사용 기간은 항상 수신 또는 전송된 날짜(동일하게 취급)를 기준으로 합니다. 마지막으로 수정된 시점을 기준으로 콘텐츠를 보존할 경우 OneDrive 및 SharePoint의 사이트 콘텐츠에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p128">Similarly, if you want to retain content in a mailbox for seven years, and a message was sent six years ago, the message will be retained for only one year. For Exchange content, the age is always based on the date received or sent (they are the same). Retaining content based on when it was last modified applies only to site content in OneDrive and SharePoint.</span></span>
  
<span data-ttu-id="44e24-p129">콘텐츠를 보존 기간이 끝나고 영구적으로 삭제할지 여부를 선택할 수 있습니다. 보존 정책으로 오래된 콘텐츠를 보존하지 않고 단순히 삭제할 수도 있습니다. 다음 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p129">You can choose whether you want the content to be permanently deleted at the end of the retention period. A retention policy can also simply delete old content without retaining it - see the next section.</span></span>
  
![보존 설정 페이지](media/b05f84e5-fc71-4717-8f7b-d06a29dc4f29.png)
  
## <a name="deleting-content-thats-older-than-a-specific-age"></a><span data-ttu-id="44e24-207">특정 사용 기간보다 오래된 콘텐츠 삭제</span><span class="sxs-lookup"><span data-stu-id="44e24-207">Deleting content that's older than a specific age</span></span>

<span data-ttu-id="44e24-208">보존 정책은 콘텐츠를 보존했다가 삭제하거나, 보존하지 않고 오래된 콘텐츠를 단순히 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-208">A retention policy can both retain and then delete content, or simply delete old content without retaining it.</span></span>
  
<span data-ttu-id="44e24-209">보존 정책이 콘텐츠를 삭제할 경우 보존 정책에 대해 지정된 기간은 정책이 할당된 시점이 아니라 콘텐츠가 만들어졌거나 수정된 이후부터 계산된다는 사실에 유의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-209">If your retention policy deletes content, it's important to understand that the time period specified for a retention policy is calculated from the time when the content was created or modified, not the time since the policy was assigned.</span></span>
  
![삭제 설정](media/042f9571-96f4-458f-8f38-fad3ed68ed31.png)
  
<span data-ttu-id="44e24-p130">예를 들어, 3년 후에 콘텐츠를 삭제하는 보존 정책을 만든 후, 해당 정책을 3~5년 전에 만들어진 콘텐츠가 많이 포함되어 있는 모든 OneDrive 계정에 할당한다고 가정합니다. 이 경우 많은 콘텐츠가 보존 정책을 처음 할당한 직후에 삭제됩니다. 이러한 이유로 **콘텐츠를 삭제하는 보존 정책은 콘텐츠에 상당한 영향을 미칠 수 있습니다**.</span><span class="sxs-lookup"><span data-stu-id="44e24-p130">For example, suppose that you create a retention policy that deletes content after three years, and then assign that policy to all OneDrive accounts, which contain a lot of content that was created four or five years ago. In this case, a lot of content will be deleted soon after assigning the retention policy for the first time. For this reason, **a retention policy that deletes content can have a considerable impact on your content**.</span></span> 
  
<span data-ttu-id="44e24-p131">따라서 처음으로 사이트에 보존 정책을 할당하기 전에 먼저 콘텐츠의 사용 기간과 정책이 기존 콘텐츠에 어떤 영향을 줄 수 있는지 고려해야 합니다. 또한 새 정책을 할당하기 전에 사용자에게 미리 알려, 가능한 영향을 평가할 시간을 줄 수도 있습니다. 보존 정책을 만들기 바로 전에 해당 설정을 검토할 때 나타나는 다음 경고에 유의하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p131">Therefore, before you assign a retention policy to a site for the first time, you should first consider the age of the existing content and how the policy may impact that content. You may also want to communicate the new policy to your users before assigning it, to give them time to assess the possible impact. Note this warning that appears when you review the settings for your retention policy just before creating it.</span></span>
  
![콘텐츠 삭제 경고](media/59c26b19-3628-4cc1-9a73-a05127a8e81b.png)
  
## <a name="advanced-settings-that-apply-a-policy-only-to-content-that-meets-certain-conditions"></a><span data-ttu-id="44e24-218">특정 조건을 충족하는 콘텐츠에만 정책을 적용하는 고급 설정</span><span class="sxs-lookup"><span data-stu-id="44e24-218">Advanced settings that apply a policy only to content that meets certain conditions</span></span>

<span data-ttu-id="44e24-219">보존 정책을 포함하는 위치의 모든 콘텐츠에 적용할 수도 있고, 특정 키워드 또는 [특정 유형의 중요 정보](what-the-sensitive-information-types-look-for.md)를 포함하는 콘텐츠에만 보존 정책을 적용하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-219">A retention policy can apply to all content in the locations that it includes, or you can choose to apply a retention policy only to content that contains specific keywords or [specific types of sensitive information](what-the-sensitive-information-types-look-for.md).</span></span>
  
![고급 보존 옵션](media/e8d9dd42-c062-4e8b-a2ca-bffe3ea298e0.png)
  
### <a name="retain-content-that-contains-specific-keywords"></a><span data-ttu-id="44e24-221">특정 키워드를 포함하는 콘텐츠 보존</span><span class="sxs-lookup"><span data-stu-id="44e24-221">Retain content that contains specific keywords</span></span>

<span data-ttu-id="44e24-p132">특정 조건을 충족하는 콘텐츠에만 보존 정책을 적용한 후, 해당 콘텐츠에만 보존 작업을 수행할 수 있습니다. 현재 사용 가능한 조건은 특정 단어 또는 구를 포함하는 콘텐츠에만 보존 정책을 적용하도록 지원합니다. AND, OR 및 NOT과 같은 검색 연산자를 사용하여 쿼리를 구체화할 수 있습니다. 이러한 연산자에 대한 자세한 내용은 [콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건](keyword-queries-and-search-conditions.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p132">You can apply a retention policy only to content that satisfies certain conditions, and then take retention actions on just that content. The conditions available now support applying a retention policy to content that contains specific words or phrases. You can refine your query by using search operators like AND, OR, and NOT. For more information on these operators, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
<span data-ttu-id="44e24-226">검색 가능한 속성(예: **제목:**)을 추가하는 기능이 곧 지원될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-226">Support for adding searchable properties (for example, **subject:**) is coming soon.</span></span>
  
<span data-ttu-id="44e24-227">쿼리 기반 보존은 검색 인덱스를 사용하여 콘텐츠를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-227">Note that query-based retention uses the search index to identify content.</span></span>
  
![쿼리 편집기](media/2c31b412-922e-4a88-89e4-5175c23d9b5f.png)
  
### <a name="retain-content-that-contains-sensitive-information"></a><span data-ttu-id="44e24-229">중요한 정보가 포함된 콘텐츠 보존</span><span class="sxs-lookup"><span data-stu-id="44e24-229">Retain content that contains sensitive information</span></span>

<span data-ttu-id="44e24-p133">[특정 유형의 중요 정보](what-the-sensitive-information-types-look-for.md)를 포함하는 콘텐츠에만 보존 정책을 적용할 수도 있습니다. 예를 들어, 납세자 ID 번호, 주민 등록 번호 또는 여권 번호 등 PII(개인 식별이 가능한 정보)를 포함하는 콘텐츠에만 고유한 보존 요구 사항을 적용하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p133">You can also apply a retention policy only to content that contains [specific types of sensitive information](what-the-sensitive-information-types-look-for.md). For example, you can choose to apply unique retention requirements only to content that contains personally identifiable information (PII) such as taxpayer identification numbers, social security numbers, or passport numbers.</span></span>
  
![중요한 정보 유형 페이지](media/8b104819-d185-4d58-b6b3-d06e82686a05.png)
  
<span data-ttu-id="44e24-233">참고:</span><span class="sxs-lookup"><span data-stu-id="44e24-233">Notes:</span></span>
  
- <span data-ttu-id="44e24-234">중요한 정보에 대한 고급 보존이 Exchange 공용 폴더 및 비즈니스용 Skype에는 적용되지 않습니다. 이러한 위치는 중요한 정보 유형을 지원하지 않기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-234">Advanced retention for sensitive information doesn't apply to Exchange public folders or Skype for Business because those locations don't support sensitive information types.</span></span>
    
- <span data-ttu-id="44e24-p134">Exchange Online에서는 전송 규칙을 사용하여 중요한 정보를 식별하므로 사서함에 이미 저장된 모든 항목이 아닌 전송 중인 메시지에만 이러한 고급 보존이 적용됩니다. 따라서 Exchange Online의 경우 보존 정책이 중요한 정보를 식별할 수 있고 정책이 사서함에 적용된 **후에** 수신된 메시지에만 보존 작업을 수행할 수 있습니다. (이전 섹션에 설명된 쿼리 기반 보존은 검색 인덱스를 사용하여 콘텐츠를 식별하기 때문에 이러한 제한이 적용되지 않습니다.)</span><span class="sxs-lookup"><span data-stu-id="44e24-p134">You should understand that Exchange Online uses transport rules to identify sensitive information, so this works only on messages in transit — not on all items already stored in a mailbox. For Exchange Online, this means that a retention policy can identify sensitive information and take retention actions only on messages that are received **after** the policy is applied to the mailbox. (Note that query-based retention described in the previous section doesn't have this limitation because it uses the search index to identify content.)</span></span> 
    
## <a name="applying-a-retention-policy-to-an-entire-organization-or-specific-locations"></a><span data-ttu-id="44e24-238">전체 조직 또는 특정 위치에 보존 정책 적용</span><span class="sxs-lookup"><span data-stu-id="44e24-238">Applying a retention policy to an entire organization or specific locations</span></span>

<span data-ttu-id="44e24-239">전체 조직, 전체 위치 또는 특정 위치나 사용자에 보존 정책을 쉽게 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-239">You can easily apply a retention policy to an entire organization, entire locations, or only to specific locations or users.</span></span>
  
### <a name="org-wide-policy"></a><span data-ttu-id="44e24-240">조직 전체 정책</span><span class="sxs-lookup"><span data-stu-id="44e24-240">Org-wide policy</span></span>

<span data-ttu-id="44e24-241">보존 정책의 가장 강력한 기능 중 하나는 기본적으로 다음을 비롯한 Office 365의 위치에 적용된다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-241">One of the most powerful features of a retention policy is that by default it applies to locations across Office 365, including:</span></span>
  
- <span data-ttu-id="44e24-242">Exchange 전자 메일</span><span class="sxs-lookup"><span data-stu-id="44e24-242">Exchange email</span></span>
    
- <span data-ttu-id="44e24-243">SharePoint 사이트</span><span class="sxs-lookup"><span data-stu-id="44e24-243">SharePoint sites</span></span>
    
- <span data-ttu-id="44e24-244">OneDrive 계정</span><span class="sxs-lookup"><span data-stu-id="44e24-244">OneDrive accounts</span></span>
    
- <span data-ttu-id="44e24-p135">Office 365 그룹(그룹의 사서함, 사이트 및 문서에 있는 콘텐츠에 적용됩니다. Planner, Yammer 및 CRM 콘텐츠에 대한 지원도 곧 제공될 예정입니다.)</span><span class="sxs-lookup"><span data-stu-id="44e24-p135">Office 365 groups (applies to content in the group's mailbox, site, and documents. Support for content in Planner, Yammer, and CRM is coming soon.)</span></span>
    
- <span data-ttu-id="44e24-247">Exchange 공용 폴더</span><span class="sxs-lookup"><span data-stu-id="44e24-247">Exchange public folders</span></span>
    
![모든 위치 옵션](media/c343bd8e-42ac-4f17-a338-36f3c9598a86.png)
  
<span data-ttu-id="44e24-249">조직 전체 보존 정책의 기타 중요한 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-249">Other important features of an org-wide retention policy include:</span></span>
  
- <span data-ttu-id="44e24-250">정책이 포함할 수 있는 사서함 또는 사이트 개수에 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-250">There is no limit to the number of mailboxes or sites the policy can include.</span></span>
    
- <span data-ttu-id="44e24-251">Exchange의 경우 정책이 적용된 후에 만들어진 모든 새 사서함은 해당 정책을 자동으로 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-251">For Exchange, any new mailbox created after the policy is applied will automatically inherit the policy.</span></span>
  
### <a name="a-policy-that-applies-to-entire-locations"></a><span data-ttu-id="44e24-252">전체 위치에 적용되는 정책</span><span class="sxs-lookup"><span data-stu-id="44e24-252">A policy that applies to entire locations</span></span>

<span data-ttu-id="44e24-p136">위치를 선택할 때 Exchange 전자 메일이나 OneDrive 계정 등, 전체 위치를 쉽게 포함하거나 제외할 수 있습니다. 이를 위해 해당 위치의 **상태**를 설정 또는 해제하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p136">When you choose locations, you can easily include or exclude an entire location, such as Exchange email or OneDrive accounts. To do so, simply toggle the **Status** of that location on or off.</span></span> 
  
<span data-ttu-id="44e24-p137">조직 전체 정책과 마찬가지로, 전체 위치 조합에 정책이 적용될 경우 정책에 포함될 수 있는 사서함 또는 사이트 수에는 제한이 없습니다. 예를 들어, 정책에 모든 Exchange 전자 메일과 모든 SharePoint 사이트가 포함될 경우, 개수에 관계없이 모든 사이트와 사서함이 포함됩니다. 또한 Exchange의 경우 정책이 적용된 후 만들어진 모든 새 사서함은 자동으로 해당 정책을 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p137">Like an org-wide policy, if a policy applies to any combination of entire locations, there is no limit to the number of mailboxes or sites the policy can include. For example, if a policy includes all Exchange email and all SharePoint sites, all sites and mailboxes will be included, no matter how many. And for Exchange, any new mailbox created after the policy is applied will automatically inherit the policy.</span></span>
 
![위치 선택 페이지](media/6ac0c2d6-1abf-4690-b3f6-9ca506887ba3.png)
  
### <a name="a-policy-with-specific-inclusions-or-exclusions"></a><span data-ttu-id="44e24-259">특정 포함 또는 제외가 적용된 정책</span><span class="sxs-lookup"><span data-stu-id="44e24-259">A policy with specific inclusions or exclusions</span></span>

<span data-ttu-id="44e24-p138">특정 사용자에게 보존 정책을 적용할 수도 있습니다. 이를 위해 해당 위치의 **상태**를 설정으로 전환한 후 링크를 사용하여 특정 사용자, Office 365 그룹 또는 위치를 포함하거나 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p138">You can also apply a retention policy to specific users. To do so, toggle the **Status** of that location on, and then use the links to include or exclude specific users, Office 365 groups, or locations.</span></span> 
  
<span data-ttu-id="44e24-262">그러나 1,000명이 넘는 특정 사용자를 포함하거나 제외하는 보존 정책에는 다음과 같은 제한이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-262">However, note that the following limits exist for a retention policy that includes or excludes over 1,000 specific users:</span></span>
  
- <span data-ttu-id="44e24-263">이러한 보존 정책에는 1,000개 이하의 사서함과 100개 이하의 사이트를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-263">Such a retention policy can contain no more than 1,000 mailboxes and 100 sites.</span></span>
    
- <span data-ttu-id="44e24-264">테넌트에는 1,000개 이하의 이러한 보존 정책이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-264">A tenant can contain no more than 1,000 such retention policies.</span></span>
    
<span data-ttu-id="44e24-265">이러한 제한이 있지만, 조직 전체 정책이나 전체 위치에 적용되는 정책을 적용 하면 이러한 제한을 극복할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-265">Although these limits exist, understand that you can get over these limits by applying either an org-wide policy or a policy that applies to entire locations.</span></span>
  
### <a name="skype-locations"></a><span data-ttu-id="44e24-266">Skype 위치</span><span class="sxs-lookup"><span data-stu-id="44e24-266">Skype locations</span></span>

<span data-ttu-id="44e24-267">Exchange 전자 메일과 달리, Skype 위치의 상태는 간단히 설정으로 전환하여 모든 사용자를 포함할 수 없습니다. 그렇지만 해당 위치를 켠 후 해당 대화를 보존하려는 사용자를 수동으로 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-267">Unlike Exchange email, you can't simply toggle the status of the Skype location on to include all users, but you can turn on that location and then manually choose the users whose conversations you want to retain.</span></span>
  
<span data-ttu-id="44e24-p139">그러나 비즈니스용 Skype 사용자를 선택하는 경우 열 머리글에서 **이름** 상자를 선택하여 모든 사용자를 빠르게 포함할 수 있습니다. 그렇지만 정책에서 각 사용자는 고유한 포함 개수로 게산된다는 점을 이해해야 합니다. 따라서 1,000명이 넘는 사용자를 포함하는 경우 이전 섹션에서 언급한 제한이 적용됩니다. 여기에서 모든 Skype 사용자를 선택하는 경우 조직 전체 정책을 사용할 때 기본적으로 모든 Skype 사용자를 포함할 수 있는 것과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p139">When you choose Skype for Business users, you can quickly include all users by selecting the **Name** box in the column header - however, it's important to understand that each user counts as a specific inclusion in the policy. Therefore, if you include over 1,000 users, the limits noted in the previous section apply. Selecting all Skype users here is not the same as if an org-wide policy were able to include all Skype users by default.</span></span> 
  
![Skype 사용자 선택 페이지](media/f1742493-741a-4142-a564-d7d41ab0236a.png)
  
<span data-ttu-id="44e24-p140">Outlook의 **대화 내용** 폴더는 Skype 보관과 아무 관계가 없는 기능입니다. **대화 내용**은 최종 사용자가 해제할 수 있지만 Skype 보관은 사용자는 액세스할 수 없고 eDiscovery에서 사용할 수 있는 숨겨진 폴더에 Skype 대화 사본을 저장하여 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p140">Note that **Conversation History**, a folder in Outlook, is a feature that has nothing to do with Skype archiving. **Conversation History** can be turned off by the end user, but archiving for Skype is done by storing a copy of Skype conversations in a hidden folder that is inaccessible to the user but available to eDiscovery.</span></span> 
  
### <a name="teams-locations"></a><span data-ttu-id="44e24-274">Teams 위치</span><span class="sxs-lookup"><span data-stu-id="44e24-274">Teams locations</span></span>

<span data-ttu-id="44e24-p141">Teams에서 보존 정책을 사용하여 채팅 및 채널 메시지를 보존할 수 있습니다. Teams 채팅은 채팅에 포함된 각 사용자의 사서함에 있는 숨겨진 폴더에 저장되고, Teams 채널 메시지는 팀의 그룹 사서함에 있는 비슷한 숨겨진 폴더에 저장됩니다. 그렇지만 Teams에서 이 데이터도 저장하는 Azure 지원 채팅 서비스를 사용하며, 기본적으로 이 서비스는 데이터를 영구히 저장한다는 점을 이해하는 것이 중요합니다. 이 때문에 Teams 데이터를 보존 및 삭제할 때는 Teams 위치를 사용하는 것이 좋습니다. Teams 위치를 사용하면 Exchange 사서함과 기본 Azure 지원 채팅 서비스 둘 다에서 데이터가 영구적으로 삭제됩니다. 자세한 내용은 [Microsoft Teams의 보안 및 규정 준수 개요](https://go.microsoft.com/fwlink/?linkid=871258)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p141">You can use a retention policy to retain chats and channel messages in Teams. Teams chats are stored in a hidden folder in the mailbox of each user included in the chat, and Teams channel messages are stored in a similar hidden folder in the group mailbox for the team. However, it's important to understand that Teams uses an Azure-powered chat service that also stores this data, and by default this service stores the data forever. For this reason, we strongly recommend that you use the Teams location to retain and delete Teams data. Using the Teams location will permanently delete data from both the Exchange mailboxes and the underlying Azure-powered chat service. For more information, see [Overview of security and compliance in Microsoft Teams](https://go.microsoft.com/fwlink/?linkid=871258).</span></span>
  
<span data-ttu-id="44e24-p142">Teams 채팅 및 채널 메시지는 Exchange 또는 Office 365 그룹 위치의 사용자 또는 그룹 사서함에 적용되는 보존 정책의 영향을 받지 않습니다. Teams 채팅 및 채널 메시지는 Exchange에 저장되지만 Teams 위치에 적용되는 보존 정책에 의해서만 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p142">Note that Teams chats and channel messages are not affected by retention policies applied to user or group mailboxes in the Exchange or Office 365 groups locations. Even though Teams chats and channel messages are stored in Exchange, they're affected only by a retention policy that's applied to the Teams location.</span></span>
  
<span data-ttu-id="44e24-p143">Teams의 보존 기능에 대한 작업이 진행 중이며 추가 기능이 제공될 예정입니다. 당분간은 다음과 같은 몇 가지 제한에 유의하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p143">We're still working on retention in Teams, and additional features are coming. In the meantime, here are a few limitations to be aware of:</span></span>
  
- <span data-ttu-id="44e24-p144">**Teams에 별도 보존 정책 필요** Teams 위치에서 보존 정책을 만들고 해당 정책을 켜면 다른 모든 위치는 꺼집니다. Teams를 포함하는 보존 정책에는 Teams 위치만 포함될 수 있고 다른 위치는 포함될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p144">**Teams require a separate retention policy** When you create a retention policy and toggle on the Teams location, all other locations toggle off. A retention policy that includes Teams can include only Teams and no other locations.</span></span> 
    
- <span data-ttu-id="44e24-287">**Teams는 조직 전체 정책에 포함되지 않음** Teams에는 별도 보존 정책 필요하므로 조직 전체 정책을 만들어도 여기에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-287">**Teams are not included in an org-wide policy** If you create an org-wide policy, Teams are not included because they require a separate retention policy.</span></span> 
    
- <span data-ttu-id="44e24-p145">**Teams는 고급 보존을 지원하지 않음** 보존 정책을 만들 때 [특정 조건을 충족하는 콘텐츠에만 정책을 적용하는 고급 설정](retention-policies.md#advanced)을 선택하면 Teams 위치를 사용할 수 없습니다.  이 경우 Teams의 보존 정책이 모든 채팅 및 채널 메시지 콘텐츠에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p145">**Teams doesn't support advanced retention** When you create a retention policy, if you choose the [Advanced settings that apply a policy only to content that meets certain conditions](retention-policies.md#advanced), the Teams location is not available. At this time, retention in Teams applies to all of the chat and channel message content.</span></span>
    
- <span data-ttu-id="44e24-p146">**30일 이전의 Teams 콘텐츠만 삭제할 수 있음** 현재, 30일보다 오래되지 않은 Teams 콘텐츠를 삭제하는 정책을 만드는 것은 지원되지 않습니다. 이 정책을 Teams 콘텐츠에 적용하려는 경우 30일보다 크거나 같은 보존 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p146">**Teams content must be at least 30 days old to be deleted** At this time, creating a policy to delete Teams content that's less than 30 days old is not supported. If you want this policy to apply to Teams content, specify a retention period that's equal to or greater than 30 days.</span></span> 
    
- <span data-ttu-id="44e24-p147">**Teams에서 보존된 콘텐츠를 정리하는 데 최대 30일이 소요될 수 있음** Teams에 적용되는 보존 정책은 모든 관련 저장소 위치에서 콘텐츠를 삭제합니다. 그러나 시작된 후 즉시, Teams 클라이언트가 보존 정책에 따라 콘텐츠를 정리하는 데 최대 30일이 걸릴 수 있습니다. 하지만 보존 기간이 끝난 후에는 콘텐츠가 Teams 클라이언트에 계속 표시되더라도 콘텐츠 검색 또는 eDiscovery에는 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p147">**Teams may take up to 30 days to clean up retained content** A retention policy applied to Teams will delete the content from all relevant storage locations. However, immediately after launch, it may take up to 30 days for Teams clients to clean up content based on the retention policy. But even though content still appears in the Teams clients, that content will not appear in content search or eDiscovery after the end of the retention period.</span></span> 
    
<span data-ttu-id="44e24-p148">팀에서 채팅 시 공유된 파일이 파일을 공유한 사용자의 OneDrive 계정에 저장됩니다. 채널에 업로드된 파일은 팀용 SharePoint 사이트에 저장됩니다. 따라서 Teams에서 파일을 보존하거나 삭제하려면 SharePoint 및 OneDrive 위치에 적용되는 보존 정책을 만들어야 합니다. 특정 팀의 파일에만 정책을 적용하려는 경우 팀용 SharePoint 사이트와 팀에 포함된 사용자의 OneDrive 계정을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p148">In a Team, files that are shared in chat are stored in the OneDrive account of the user who shared the file. Files that are uploaded into channels are stored in the SharePoint site for the Team. Therefore, to retain or delete files in a Team, you need to create a retention policy that applies to the SharePoint and OneDrive locations. If you want to apply a policy to the files of just a specific team, you can choose the SharePoint site for the Team and the OneDrive accounts of users in the Team.</span></span>
  
<span data-ttu-id="44e24-299">Teams에 적용되는 보존 정책은 [유지 잠금](retention-policies.md#locking)을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-299">A retention policy that applies to Teams can use [Preservation Lock](retention-policies.md#locking).</span></span>
  
![채팅 및 채널 메시지에 대한 Teams 위치](media/127345da-e802-4b3a-afc7-6e354dc3f409.png)
  
## <a name="excluding-specific-types-of-exchange-items-from-a-retention-policy"></a><span data-ttu-id="44e24-301">보존 정책에서 특정 유형의 Exchange 항목 제외</span><span class="sxs-lookup"><span data-stu-id="44e24-301">Excluding specific types of Exchange items from a retention policy</span></span>
<span data-ttu-id="44e24-p149">PowerShell을 사용하여 특정 유형의 Exchange 항목을 보존 정책에서 제외할 수 있습니다. 예를 들어, 사서함의 음성 메일 메시지, 메신저 대화 및 기타 비즈니스용 Skype Online 콘텐츠를 제외할 수 있습니다. 또한 일정, 메모 및 작업 항목도 제외할 수 있습니다. 이 기능은 PowerShell을 통해서만 사용할 수 있으며 보존 정책을 만들 때 UI에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p149">By using PowerShell, you can exclude specific types of Exchange items from a retention policy. For example, you can exclude voicemail messages, IM conversations, and other Skype for Business Online content in mailboxes. You can also exclude calendar, note, and task items. This capability is available only by using PowerShell; it's not available in the UI when you create a retention policy.</span></span>
  
<span data-ttu-id="44e24-p150">이를 수행하려면 `New-RetentionComplianceRule` 및 `Set-RetentionComplianceRule` cmdlet의 `ExcludedItemClasses` 매개 변수를 사용합니다. PowerShell에 대한 자세한 내용은 아래의 [보존 정책에 대한 PowerShell cmdlet 찾기](#find-the-powershell-cmdlets-for-retention-policies) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p150">To do this, use the  `ExcludedItemClasses` parameter of the  `New-RetentionComplianceRule` and  `Set-RetentionComplianceRule` cmdlets. For more information about PowerShell, see the below section [Find the PowerShell cmdlets for retention policies](#find-the-powershell-cmdlets-for-retention-policies).</span></span>
  
## <a name="locking-a-retention-policy"></a><span data-ttu-id="44e24-308">보존 정책 잠그기</span><span class="sxs-lookup"><span data-stu-id="44e24-308">Locking a retention policy</span></span>
<span data-ttu-id="44e24-p151">일부 조직에서는 SEC(Securities and Exchange Commission) 규칙 17a-4와 같은 규제 기구에서 정의한 규칙을 준수해야 합니다. 따라서 예약 정책을 켠 후에는 끄거나 덜 제한적인 정책으로 변경할 수 없습니다. 보존 잠금을 사용하면 정책을 잠궈 관리자를 비롯한 어느 누구도 정책을 해제하거나 덜 제한적으로 만들지 못하게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p151">Some organizations may need to comply with rules defined by regulatory bodies such as the Securities and Exchange Commission (SEC) Rule 17a-4, which requires that after a retention policy is turned on, it cannot be turned off or made less restrictive. With Preservation Lock, you can lock the policy so that no one—including the administrator—can turn off the policy or make it less restrictive.</span></span>
  
<span data-ttu-id="44e24-p152">정책을 잠그면 누구도 정책을 해제하거나 정책에서 위치를 제거할 수 없습니다. 또한 보존 기간 동안 해당 정책이 적용되는 콘텐츠를 수정하거나 삭제할 수 없습니다. 정책이 잠긴 후에는 위치를 추가하거나 기간을 확장해야만 보존 정책을 수정할 수 있습니다. 잠겨 있는 정책은 늘리거나 확장할 수 있지만 줄이거나 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p152">After a policy's been locked, no one can turn it off or remove locations from the policy. And it's not possible to modify or delete content that's subject to the policy during the retention period. After the policy's been locked, the only ways you can modify the retention policy are by adding locations to it or extending its duration. A locked policy can be increased or extended, but it can't be reduced or turned off.</span></span>
  
<span data-ttu-id="44e24-315">따라서 보존 정책을 잠그기 전에 조직의 규정 준수 요구 사항을 **이해하고** 본인에게 필요한 정책인지 **확실해진 후에 잠그도록 해야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-315">Therefore, before you lock a retention policy, it's **critical** that you understand your organization's compliance requirements, and that **you do not lock a policy** until you're certain that it's what you need.</span></span>
  
<span data-ttu-id="44e24-p153">PowerShell을 사용해야만 보존 정책을 잠글 수 있습니다. `New-RetentionCompliancePolicy` 또는 `Set-RetentionCompliancePolicy` cmdlet의 `RestrictiveRetention` 매개 변수를 사용합니다. PowerShell에 대한 자세한 내용은 아래의 [보존 정책에 대한 PowerShell cmdlet 찾기](#find-the-powershell-cmdlets-for-retention-policies) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p153">You can lock a retention policy only by using PowerShell. Use the  `RestrictiveRetention` parameter of the  `New-RetentionCompliancePolicy` or  `Set-RetentionCompliancePolicy` cmdlet. For more information about PowerShell, see the below section [Find the PowerShell cmdlets for retention policies](#find-the-powershell-cmdlets-for-retention-policies).</span></span>
  
## <a name="the-principles-of-retention-or-what-takes-precedence"></a><span data-ttu-id="44e24-319">보존 원칙 또는 우선 순위</span><span class="sxs-lookup"><span data-stu-id="44e24-319">The principles of retention, or what takes precedence?</span></span>

<span data-ttu-id="44e24-p154">콘텐츠에 각기 다른 작업(보존, 삭제 또는 둘 다) 및 보존 기간을 지정하는 여러 보존 정책이 적용될 수 있습니다. 우선 순위는 어떨까요? 분명한 것은 가장 높은 수준에서 한 정책을 통해 보존되는 콘텐츠가 다른 정책에 의해 영구적으로 삭제될 수 없다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p154">It's possible or even likely that content might have several retention policies applied to it, each with a different action (retain, delete, or both) and retention period. What takes precedence? At the highest level, rest assured that content being retained by one policy can't be permanently deleted by another policy.</span></span>
  
![보존 원칙 다이어그램](media/1693d6ec-b340-4805-9da3-89aa41bc6afb.png)
  
<span data-ttu-id="44e24-324">여러 다른 보존 정책 콘텐츠에 적용되는 방식을 이해하려면 다음과 같은 보존 원칙에 유의합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-324">To understand how different retention policies are applied to content, keep these principles of retention in mind:</span></span>
  
1. <span data-ttu-id="44e24-p155">**보존이 삭제보다 우선합니다.** 한 보존 정책은 3년 후에 Exchange 전자 메일을 삭제하도록 지정하지만 다른 보존 정책은 5년 동안 Exchange 전자 메일을 보존했다가 삭제하도록 지정하는 경우를 가정해보세요. 3년에 도달한 모든 콘텐츠는 삭제되고 사용자가 볼 수 없게 숨겨지지만, 5년에 도달할 때까지 복구 가능한 항목 폴더에 보존되었다가 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p155">**Retention wins over deletion.** Suppose that one retention policy says to delete Exchange email after three years, but another retention policy says to retain Exchange email for five years and then delete it. Any content that reaches three years old will be deleted and hidden from the users' view, but still retained in the Recoverable Items folder until the content reaches five years old, when it will be permanently deleted.</span></span> 
    
2. <span data-ttu-id="44e24-p156">**가장 긴 보존 기간이 우선합니다.** 콘텐츠에 여러 콘텐츠 보존 정책이 적용되는 경우 가장 긴 보존 기간이 끝날 때까지 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p156">**The longest retention period wins.** If content's subject to multiple policies that retain content, it will be retained until the end of the longest retention period.</span></span> 
    
3. <span data-ttu-id="44e24-p157">**명시적 포함이 암시적 포함보다 우선합니다.** 이것은 다음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p157">**Explicit inclusion wins over implicit inclusion.** This means:</span></span> 
    
    1. <span data-ttu-id="44e24-p158">사용자가 보존 설정이 포함된 레이블을 Exchange 전자 메일 또는 OneDrive 문서와 같은 항목에 수동으로 할당하면 해당 레이블은 사이트 또는 사서함 수준에서 할당된 정책과 문서 라이브러리에 의해 할당된 기본 레이블보다 우선적으로 적용됩니다. 예를 들어, 명시적 레이블에 10년 동안 보존하도록 지정되어 있지만 사이트에 할당된 정책은 5년만 보존하도록 지정하는 경우 레이블이 우선합니다. 자동 적용 레이블은 Office 365에 의해 자동으로 적용되므로 명시적이 아니라 암시적으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p158">If a label with retention settings is manually assigned by a user to an item, such as an Exchange email or OneDrive document, that label takes precedence over both a policy assigned at the site or mailbox level and a default label assigned by the document library. For example, if the explicit label says to retain for ten years, but the policy assigned to the site says to retain for only five years, the label takes precedence. Note that auto-apply labels are considered implicit, not explicit, because they're applied automatically by Office 365.</span></span>
    
    2. <span data-ttu-id="44e24-335">보존 정책에 특정 사용자의 사서함 또는 OneDrive용 비즈니스 계정과 같은 특정 위치가 포함되는 경우 해당 정책이 모든 사용자의 사서함 또는 비즈니스용 OneDrive 계정에 적용되지만 해당 사용자의 사서함을 특별히 포함하지 않는 다른 보존 정책보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-335">If a retention policy includes a specific location, such as a specific user's mailbox or OneDrive for Business account, that policy takes precedence over another retention policy that applies to all users' mailboxes or OneDrive for Business accounts but doesn't specifically include that user's mailbox.</span></span>
    
4. <span data-ttu-id="44e24-p159">**가장 짧은 삭제 기간이 우선적으로 적용됩니다.** 마찬가지로 콘텐츠에 여러 콘텐츠 삭제 정책이 적용되는 경우(보존 없음) 가장 짧은 보존 기간이 끝나면 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p159">**The shortest deletion period wins.** Similarly, if content's subject to multiple policies that delete content (with no retention), it will be deleted at the end of the shortest retention period.</span></span> 
    
<span data-ttu-id="44e24-338">보존 원칙은 위에서 아래로 균형을 깨는 흐름처럼 작동한다는 점을 이해하도록 합니다. 모든 정책 또는 레이블에 의해 적용되는 규칙이 하나의 수준에서 동일한 경우 규칙이 적용되는 우선 순위를 결정하기 위해 흐름은 아래의 다음 수준으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-338">Understand that the principles of retention work as a tie-breaking flow from top to bottom: If the rules applied by all policies or labels are the same at one level, the flow moves down to the next level to determine precedence for which rule is applied.</span></span>
  
<span data-ttu-id="44e24-p160">마지막으로, 보존 정책 또는 레이블은 eDiscovery 보류 상태인 콘텐츠를 영구적으로 삭제할 수 없습니다. 보류가 해제되면 다시 위에 설명된 정리 프로세스가 해당 콘텐츠에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p160">Finally, a retention policy or label cannot permanently delete any content that's on hold for eDiscovery. When the hold is released, the content again becomes eligible for the cleanup process described above.</span></span>
  
## <a name="use-a-retention-policy-instead-of-these-features"></a><span data-ttu-id="44e24-341">이러한 기능 대신 보존 정책 사용</span><span class="sxs-lookup"><span data-stu-id="44e24-341">Use a retention policy instead of these features</span></span>

<span data-ttu-id="44e24-p161">하나의 보존 정책을 Exchange Online, SharePoint Online, 비즈니스용 OneDrive 및 Office 365 그룹을 포함하는 Office 365의 전체 조직 및 위치에 쉽게 적용할 수 있습니다. Office 365에서 콘텐츠를 보존하거나 삭제해야 할 경우 보존 정책을 사용하는 것이 좋습니다. 보존 설정과 함께 레이블을 사용할 수도 있습니다. 자세한 내용은 [레이블 개요](labels.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-p161">A single retention policy can easily apply to an entire organization and locations across Office 365, including Exchange Online, SharePoint Online, OneDrive for Business, and Office 365 groups. If you need to retain or delete content anywhere in Office 365, we recommend that you use a retention policy. (You can also use labels with retention settings - for more information, see [Overview of labels](labels.md).)</span></span>
  
<span data-ttu-id="44e24-p162">Office 365에서 콘텐츠를 보존하거나 삭제하기 위해 이전에 사용되던 여러 다른 기능이 있습니다. 이러한 기능은 아래에 나와 있습니다. 이러한 기능은 보안 및 준수 센터에서 만든 보존 정책 및 레이블과 함께 계속 사용할 수 있습니다. 그렇지만 앞으로는 데이터 거버넌스를 위해 이러한 모든 기능 대신 보존 정책이나 레이블을 사용하는 것이 좋습니다. 보존 정책이 Office 365에서 콘텐츠를 보존 및 삭제할 수 있는 유일한 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p162">There are several other features that have previously been used to retain or delete content in Office 365. These are listed below. These features will continue to work side by side with retention policies and labels created in the Security &amp; Compliance Center. But moving forward, for data governance, we recommend that you use a retention policy or labels instead of all of these features. A retention policy is the only feature that can both retain and delete content across Office 365.</span></span>
  
### <a name="exchange-online"></a><span data-ttu-id="44e24-350">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="44e24-350">Exchange Online</span></span>

- <span data-ttu-id="44e24-351">[Office 365 보안 및 준수 센터에서 eDiscovery 사례 관리](https://support.office.com/article/edea80d6-20a7-40fb-b8c4-5e8c8395f6da)(eDiscovery 보류)</span><span class="sxs-lookup"><span data-stu-id="44e24-351">[Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](https://support.office.com/article/edea80d6-20a7-40fb-b8c4-5e8c8395f6da) (eDiscovery hold)</span></span> 
    
- <span data-ttu-id="44e24-352">[원본 위치 유지 및 소송 보존](https://go.microsoft.com/fwlink/?linkid=846124)(eDiscovery 보류)</span><span class="sxs-lookup"><span data-stu-id="44e24-352">[In-Place Hold and Litigation Hold](https://go.microsoft.com/fwlink/?linkid=846124) (eDiscovery hold)</span></span> 
    
- <span data-ttu-id="44e24-353">[보존 태그 및 보존 정책](https://go.microsoft.com/fwlink/?linkid=846125)([[MRM(메시징 레코드 관리)라고도 함]](https://go.microsoft.com/fwlink/?linkid=846126)(삭제만 해당)</span><span class="sxs-lookup"><span data-stu-id="44e24-353">[Retention tags and retention policies](https://go.microsoft.com/fwlink/?linkid=846125), also known as [messaging records management (MRM)](https://go.microsoft.com/fwlink/?linkid=846126) (Deletion only)</span></span> 
    
### <a name="sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="44e24-354">SharePoint Online 및 비즈니스용 OneDrive</span><span class="sxs-lookup"><span data-stu-id="44e24-354">SharePoint Online and OneDrive for Business</span></span>

- <span data-ttu-id="44e24-355">[Office 365 보안 및 준수 센터에서 eDiscovery 사례 관리](https://support.office.com/article/edea80d6-20a7-40fb-b8c4-5e8c8395f6da)(eDiscovery 보류)</span><span class="sxs-lookup"><span data-stu-id="44e24-355">[Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](https://support.office.com/article/edea80d6-20a7-40fb-b8c4-5e8c8395f6da) (eDiscovery hold)</span></span> 
    
- <span data-ttu-id="44e24-356">[eDiscovery 센터에서 사례에 콘텐츠 추가 및 원본 우 위치 유지](https://support.office.com/article/54d70de9-1ec2-4325-84f3-aeb588554479)(eDiscovery 보류)</span><span class="sxs-lookup"><span data-stu-id="44e24-356">[Add content to a case and place sources on hold in the eDiscovery Center](https://support.office.com/article/54d70de9-1ec2-4325-84f3-aeb588554479) (eDiscovery hold)</span></span> 
    
- <span data-ttu-id="44e24-357">[문서 삭제 정책 개요](https://support.office.com/article/55e8d858-f278-482b-a198-2e62d6a2e6e5)(삭제만 해당)</span><span class="sxs-lookup"><span data-stu-id="44e24-357">[Overview of document deletion policies](https://support.office.com/article/55e8d858-f278-482b-a198-2e62d6a2e6e5) (Deletion only)</span></span> 
    
- <span data-ttu-id="44e24-358">[ 현재 위치 레코드 관리 구성](https://support.office.com/article/7707a878-780c-4be6-9cb0-9718ecde050a)(보존)</span><span class="sxs-lookup"><span data-stu-id="44e24-358">[Configuring in place records management](https://support.office.com/article/7707a878-780c-4be6-9cb0-9718ecde050a) (Retention)</span></span> 
    
- <span data-ttu-id="44e24-359">[사이트 폐쇄 및 삭제에 대한 정책 사용](https://support.office.com/article/a8280d82-27fd-48c5-9adf-8a5431208ba5)(삭제만 해당)</span><span class="sxs-lookup"><span data-stu-id="44e24-359">[Use policies for site closure and deletion](https://support.office.com/article/a8280d82-27fd-48c5-9adf-8a5431208ba5) (Deletion only)</span></span> 
    
- <span data-ttu-id="44e24-360">[정보 관리 정책](intro-to-info-mgmt-policies.md)(삭제만 해당)</span><span class="sxs-lookup"><span data-stu-id="44e24-360">[Information management policies](intro-to-info-mgmt-policies.md) (Deletion only)</span></span> 
    
<span data-ttu-id="44e24-p163">이전에 데이터 거버넌스를 위해 eDiscovery 보류를 사용한 경우 대신, 자동 규정 준수를 위해 보존 정책을 사용해야 합니다. eDiscovery만을 위해서는 보안 및 준수 센터에서 만든 보류를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p163">Note that if you've previously used any of the eDiscovery holds for the purpose of data governance, you should instead use a retention policy for proactive compliance. You should use a hold created in the Security &amp; Compliance Center only for eDiscovery.</span></span>
  
### <a name="retention-policies-override-information-management-policies"></a><span data-ttu-id="44e24-363">보존 정책은 정보 관리 정책을 재정의함</span><span class="sxs-lookup"><span data-stu-id="44e24-363">Retention policies override information management policies</span></span>

<span data-ttu-id="44e24-p164">SharePoint 사이트에서 [정보 관리 정책](intro-to-info-mgmt-policies.md)을 사용하여 콘텐츠를 보존할 수 있습니다. 보안 및 준수 센터에서 만든 보존 정책을 목록 또는 라이브러리에 대해 콘텐츠 형식 정책 또는 정보 관리 정책을 이미 사용하는 사이트에 적용하면 보존 정책이 적용되는 동안 해당 정책은 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p164">In SharePoint sites, you may be using [information management policies](intro-to-info-mgmt-policies.md) to retain content. If you apply a retention policy created in the Security and Compliance Center to a site that already uses content type policies or information management policies for a list or library, those policies are ignored while the retention policy is in effect.</span></span> 
  
## <a name="what-happened-to-preservation-policies"></a><span data-ttu-id="44e24-366">보류 정책은 어떻게 되었나요?</span><span class="sxs-lookup"><span data-stu-id="44e24-366">What happened to preservation policies?</span></span>

<span data-ttu-id="44e24-p165">보류 정책을 사용한 경우 해당 정책은 보존 작업만 사용하는 보존 정책으로 자동 변환되었습니다. 즉, 이러한 보존 정책은 콘텐츠를 삭제하지 않습니다. 보류 정책은 게속 작동하며, 사용자에게 변경을 요구하지 않고 콘텐츠를 계속 보존합니다. 이러한 정책은 보안 및 준수 센터의 **보존** 페이지에서 찾을 수 있습니다. 보류 정책을 편집하여 보존 기간을 변경할 수 있지만, 위치 추가나 제거와 같은 다른 변경은 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p165">If you were using a preservation policy, that policy has been automatically converted to a retention policy that uses only the retain action - the policy won't delete content. The preservation policy will continue to work and preserve your content without requiring any changes from you. You can find these policies on the **Retention** page in the Security &amp; Compliance Center. You can edit a preservation policy to change the retention period, but you can't make other changes, such as adding or removing locations.</span></span> 
  
## <a name="permissions"></a><span data-ttu-id="44e24-371">사용 권한</span><span class="sxs-lookup"><span data-stu-id="44e24-371">Permissions</span></span>

<span data-ttu-id="44e24-p166">보존 정책을 만드는 규정 준수 팀의 구성원에게는 보안 및 준수 센터에 대한 권한이 필요합니다. 기본적으로 테넌트 관리자는 이 위치에 액세스할 수 있으며, 준수 관리자 및 기타 사용자에게 테넌트 관리를 위한 모든 권한을 부여하지는 않으면서, 보안 및 준수 센터에 대한 액세스 권한을 부여할 수 있습니다. 이렇게 하기 위해 보안 및 준수 센터의 **권한** 페이지로 이동한 후 **준수 관리자** 역할 그룹을 편집하고 해당 역할 그룹에 구성원을 추가하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p166">Members of your compliance team who will create retention policies need permissions to the Security &amp; Compliance Center. By default, your tenant admin will have access to this location and can give compliance officers and other people access to the Security &amp; Compliance Center, without giving them all of the permissions of a tenant admin. To do this, we recommend that you go to the **Permissions** page of the Security &amp; Compliance Center, edit the **Compliance Administrator** role group, and add members to that role group.</span></span> 
  
<span data-ttu-id="44e24-374">자세한 내용은 [사용자에게 Office 365 보안 및 준수 센터에 대한 액세스 권한 부여](grant-access-to-the-security-and-compliance-center.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44e24-374">For more information, see [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md).</span></span>
  
<span data-ttu-id="44e24-p167">이러한 정책은 보존 정책을 만들고 적용하는 데만 필요합니다. 정책 적용을 위해서는 콘텐츠에 액세스하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-p167">These permissions are required only to create and apply a retention policy. Policy enforcement does not require access to the content.</span></span>
  
## <a name="find-the-powershell-cmdlets-for-retention-policies"></a><span data-ttu-id="44e24-377">보존 정책에 대한 PowerShell cmdlet 찾기</span><span class="sxs-lookup"><span data-stu-id="44e24-377">Find the PowerShell cmdlets for retention policies</span></span>

<span data-ttu-id="44e24-378">보존 정책 cmdlet을 사용하려면 다음을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e24-378">To use the retention policy cmdlets, you need to:</span></span>
  
1. [<span data-ttu-id="44e24-379">원격 PowerShell을 사용하여 Office 365 보안 및 준수 센터에 연결</span><span class="sxs-lookup"><span data-stu-id="44e24-379">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. <span data-ttu-id="44e24-380">다음 [Office 365 보안 및 준수 센터 cmdlet](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409) 사용</span><span class="sxs-lookup"><span data-stu-id="44e24-380">Use these [Office 365 Security &amp; Compliance Center cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span></span>
    
## <a name="more-information"></a><span data-ttu-id="44e24-381">추가 정보</span><span class="sxs-lookup"><span data-stu-id="44e24-381">More information</span></span>

- [<span data-ttu-id="44e24-382">레이블 개요</span><span class="sxs-lookup"><span data-stu-id="44e24-382">Overview of labels</span></span>](labels.md)
    

