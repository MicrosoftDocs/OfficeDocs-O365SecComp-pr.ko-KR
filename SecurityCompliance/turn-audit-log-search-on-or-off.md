---
title: Office 365 감사 로그 검색 켜기 또는 끄기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색 기능을 설정할 수 있습니다. 생각이 변경 되 면 언제 든 지 설정을 해제할 수 있습니다. 감사 로그 검색이 해제 되 면 관리자가 조직의 사용자 및 관리자 활동에 대 한 Office 365 감사 로그를 검색할 수 없습니다.
ms.openlocfilehash: 17b98cce26054d073006fa78c55fe418b5f327d8
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295461"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="4a986-105">Office 365 감사 로그 검색 켜기 또는 끄기</span><span class="sxs-lookup"><span data-stu-id="4a986-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="4a986-p102">사용자 (또는 다른 관리자)가 감사 로깅을 켜야 Office 365 감사 로그 검색을 시작할 수 있습니다. Office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색이 설정 된 경우 조직의 사용자 및 관리자 활동이 감사 로그에 기록 되 고 90 일 동안 보존 됩니다. 그러나 조직에서 감사 로그 데이터를 기록 하 고 보존 하지 않을 수도 있습니다. 또는 타사의 siem (보안 정보 및 이벤트 관리) 응용 프로그램을 사용 하 여 감사 데이터에 액세스할 수 있습니다. 이러한 경우 전역 관리자가 Office 365에서 감사 로그 검색을 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-p102">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log. When audit log search in the Office 365 Security &amp; Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days. However, your organization might not want to record and retain audit log data. Or you might be using a third-party security information and event management (SIEM) application to access your auditing data. In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="4a986-111">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="4a986-111">Before you begin</span></span>

- <span data-ttu-id="4a986-p103">Office 365 조직에서 감사 로그 검색을 설정 하거나 해제 하려면 Exchange Online에서 감사 로그 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange 관리 센터의 **사용 권한** 페이지에 있는 준수 관리 및 조직 관리 역할 그룹에 할당 됩니다. Office 365의 전역 관리자는 Exchange Online의 조직 관리 역할 그룹의 구성원입니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-p103">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization. By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="4a986-p104">감사 로그 검색을 설정 또는 해제 하려면 사용자에 게 Exchange Online의 사용 권한을 할당 해야 합니다. 보안 &amp; 및 준수 센터의 **사용 권한** 페이지에서 사용자에 게 감사 로그 역할을 할당 하면 감사 로그 검색을 설정 하거나 해제할 수 없습니다. 이는 기본 cmdlet이 Exchange Online cmdlet 이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-p104">Users have to be assigned permissions in Exchange Online to turn audit log search on or off. If you assign users the Audit Logs role on the **Permissions** page in the Security &amp; Compliance Center, they won't be able to turn audit log search on or off. This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="4a986-p105">office 365에서 감사 로그 검색을 해제 해도 office 365 관리 작업 API를 사용 하 여 조직의 감사 데이터에 액세스할 수 있습니다. 이 문서에서 설명 하는 단계에 따라 감사 로그 검색을 해제 하면 보안 &amp; 및 준수 센터를 사용 하 여 감사 로그를 검색 하거나 Exchange Online에서 **search-unifiedauditlog** cmdlet을 실행할 때 결과가 반환 되지 않습니다. 슬래시. 그러나 Office 365 관리 활동 API를 통해 조직의 감사 데이터에 액세스 하도록 모든 응용 프로그램에 권한을 부여한 경우 해당 응용 프로그램은 계속 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-p105">If you turn off audit log search in Office 365, you can still use the Office 365 Management Activity API to access auditing data for your organization. Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security &amp; Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell. However, if you've authorized any application to access your organization's auditing data via the Office 365 Management Activity API , those applications will continue to work.</span></span> 
    
- <span data-ttu-id="4a986-121">office 365 감사 로그를 검색 하는 방법에 대 한 단계별 지침은 [office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a986-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="4a986-122">감사 로그 검색 켜기</span><span class="sxs-lookup"><span data-stu-id="4a986-122">Turn on audit log search</span></span>

<span data-ttu-id="4a986-p106">보안 &amp; 및 준수 센터 또는 PowerShell을 사용 하 여 Office 365에서 감사 로그 검색을 설정할 수 있습니다. 감사 로그 검색을 설정한 후에는 여러 시간이 걸릴 수 있습니다. 감사 로그 검색을 설정 하려면 Exchange Online에서 감사 로그 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-p106">You can use the Security &amp; Compliance Center or PowerShell to turn on audit log search in Office 365. It might take several hours after you turn on audit log search before you can return results when you search the audit log. You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="4a986-126">보안 &amp; 및 준수 센터를 사용 하 여 감사 로그 검색 설정</span><span class="sxs-lookup"><span data-stu-id="4a986-126">Use the Security &amp; Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="4a986-127">보안 &amp; 및 준수 센터에서 **검색 &amp; 조사** \> **감사 로그 검색**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-127">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="4a986-128">**사용자 및 관리 활동 기록을 시작**합니다 .를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-128">Click **Start recording user and admin activities**.</span></span>
    
    ![기록 시작 사용자 및 관리자 활동을 클릭하여 감사 기능을 설정](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="4a986-130">조직의 사용자 및 관리자 활동이 Office 365 감사 로그에 기록 되 고 보고서에서 볼 수 있음을 알리는 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="4a986-131">**켜기** 를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="4a986-132">감사 로그를 준비 중 이며 준비 완료 후 몇 시간 내에 검색을 실행할 수 있음을 알리는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="4a986-133">PowerShell을 사용 하 여 감사 로그 검색 설정</span><span class="sxs-lookup"><span data-stu-id="4a986-133">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="4a986-134">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="4a986-134">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="4a986-135">다음 PowerShell 명령을 실행 하 여 Office 365에서 감사 로그 검색을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="4a986-136">변경 내용이 적용 되는 데 최대 60 분이 걸릴 수 있다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="4a986-137">감사 로그 검색 해제</span><span class="sxs-lookup"><span data-stu-id="4a986-137">Turn off audit log search</span></span>

<span data-ttu-id="4a986-p107">감사 로그 검색을 해제 하려면 Exchange Online 조직에 연결 된 원격 PowerShell을 사용 해야 합니다. 감사 로그 검색을 설정 하는 것과 마찬가지로 감사 로그 검색을 해제 하려면 Exchange Online에서 감사 로그 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-p107">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search. Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="4a986-140">원격 PowerShell을 사용하여 Exchange Online에 연결</span><span class="sxs-lookup"><span data-stu-id="4a986-140">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="4a986-141">다음 PowerShell 명령을 실행 하 여 Office 365에서 감사 로그 검색을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="4a986-p108">잠시 후에 감사 로그 검색이 해제 되어 있는지 확인 합니다 (사용 하지 않도록 설정 됨). 이 작업을 수행 하는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-p108">After a while, verify that audit log search is turned off (disabled). There are two ways to do this:</span></span>
    
    - <span data-ttu-id="4a986-144">PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="4a986-145">UnifiedAuditLogIngestionEnabled 속성의 `False` 값은 __ 감사 로그 검색이 해제 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="4a986-146">보안 &amp; 및 준수 센터에서 \*\* &amp; 검색 조사\*\* \> **감사 로그 검색**으로 이동한 다음 **검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-146">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="4a986-147">감사 로그 검색이 설정 되지 않았다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a986-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![감사가 해제 된 경우 메시지가 dispayed](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
