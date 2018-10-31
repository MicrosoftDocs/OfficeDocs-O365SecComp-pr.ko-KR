---
title: Office 365 메시지 암호화에 대해 Microsoft Azure AD Rights Management 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: Office 365 메시지 암호화의 이전 버전 Microsoft Azure 권한 관리 (이전의 Windows Azure Active Directory 권한 관리)에 따라 달라 집니다.
ms.openlocfilehash: f8759da8628d4c78fe5409f5c47e3fc2b3e9484e
ms.sourcegitcommit: c05076501dfe118e575998ecfc08ad69d13c8abc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25853073"
---
# <a name="this-article-applies-to-the-previous-version-of-ome"></a><span data-ttu-id="a2d64-103">이 문서는 OME의 이전 버전에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-103">This article applies to the previous version of OME</span></span>
<span data-ttu-id="a2d64-p101">새로운 OME 기능을 Office 365 조직을 아직 이동 하지 않은 OME를 이미 배포한 경우이 문서의 정보는 조직에 적용 됩니다. 것이 조직에 대 한 적당 하 게 하는 즉시 새 OME 기능으로 이동 하는 계획을 확인 하는 것이 좋습니다. 자세한 내용은 [새 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)합니다. 새로운 기능 먼저 작동 하는 방법에 대 한 자세한 정보를 계속 확인 하려는 경우 [Office 365 메시지 암호화](ome.md)를 참조 하십시오. 이 문서의 나머지 부분 릴리스 이전에 새 OME 기능 OME 동작을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p101">If you haven't yet moved your Office 365 organization to the new OME capabilities, but you have already deployed OME, then the information in this article applies to your organization. Microsoft recommends that you make a plan to move to the new OME capabilities as soon as it is reasonable for your organization. For instructions, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md). If you want to find out more about how the new capabilities work first, see [Office 365 Message Encryption](ome.md). The rest of this article refers to OME behavior before the release of the new OME capabilities.</span></span>

# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="a2d64-109">이전 버전의 Office 365 메시지 암호화에 대 한 Azure 권한 관리를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-109">Set up Azure Rights Management for the previous version of Office 365 Message Encryption</span></span>

<span data-ttu-id="a2d64-110">이 항목을 활성화 하 고 다음을 Azure RMS (권한 관리), Office 365 메시지 암호화 (OME) 함께 사용 하기 위해 Azure 정보 보호의 일부를 설정 하기 위해 수행 해야하는 단계를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-110">This topic describes the steps you need to follow in order to activate and then set up Azure Rights Management (RMS), part of Azure Information Protection, for use with Office 365 Message Encryption (OME).</span></span>
  
## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="a2d64-111">이전 버전의 Office 365 메시지 암호화를 사용 하기 위한 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="a2d64-111">Prerequisites for using the previous version of Office 365 Message Encryption</span></span>
<span data-ttu-id="a2d64-112"><a name="warmprereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="a2d64-112"></span></span>

<span data-ttu-id="a2d64-p102">Office 365 메시지 암호화 OME (), IRM을 포함 하 여 Azure 권한 관리 (Azure RMS)에 따라 달라 집니다. Azure RMS는 Azure 정보 보호에서 사용 하는 보호 기술입니다. OME을 사용 하려면 Office 365 조직 차례로 Azure 권한 관리 구독을 포함 하는 Exchange Online 또는 Exchange Online Protection 구독을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p102">Office 365 Message Encryption (OME), including IRM, depends on Azure Rights Management (Azure RMS). Azure RMS is the protection technology used by Azure Information Protection. To use OME, your Office 365 organization must include an Exchange Online or Exchange Online Protection subscription that, in turn, includes an Azure Rights Management subscription.</span></span>
  
- <span data-ttu-id="a2d64-116">구독에 포함 된 잘 모를 경우에 [메시지 정책, 복구 및 규정 준수에](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx)대 한 Exchange Online 서비스 설명을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a2d64-116">If you're not sure of what your subscription includes, see the Exchange Online service descriptions for [Message Policy, Recovery, and Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span></span>
    
- <span data-ttu-id="a2d64-117">Azure RMS 구독 Exchange Online 또는 Exchange Online 보호에 대 한를 설치 하지 않은 경우에 구독 구입 하 고 먼저 활성화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-117">If you don't have an Azure RMS subscription for Exchange Online or Exchange Online Protection, you must purchase a subscription and activate it first.</span></span>
    
    <span data-ttu-id="a2d64-p103">Azure 권한 관리에 대 한 구독 구입 하는 방법에 대 한 정보를 [Azure 권한 관리](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT)를 참조 하십시오. 다음 섹션 Azure 권한 관리를 활성화 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p103">For information about purchasing a subscription to Azure Rights Management, see [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). The next section gives you information about activating Azure Rights Management.</span></span>
    
- <span data-ttu-id="a2d64-120">이 문서에서는 Azure 권한 관리 활성화 하는 방법을 설명 Azure 권한 관리 있지만 Exchange Online 또는 Exchange Online 보호에 대 한 설정 되지 않은 경우 다음은 Azure 권한 관리를 사용 하도록 OME를 설정 하는 최상의 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-120">If you have Azure Rights Management but it's not set up for Exchange Online or Exchange Online Protection, this article explains how to activate Azure Rights Management and then the describes the best way to set up OME to work with Azure Rights Management.</span></span>
    
- <span data-ttu-id="a2d64-p104">위쪽, 설정한 방법에 따라 Exchange Online 또는 Exchange Online Protection Azure 권한 관리와 작동 하도록 OME를 이미 설정 했을 때을 즉시 OME 및 해당 새 기능을 사용 하 여 시작할 수 있습니다. 이 문서에서는 하는 경우 설정한 OME 올바르게 결정 하는 방법, 사용자 설정을 변경 해야하는 경우 수행할 작업을 하 고 설정을 변경 하지 않도록 선택 하는 경우에 대해 설명 합니다. 등의 새로운 기능을 사용 하려면 OME와 Azure RMS를 사용 해야 있습니다. 온-프레미스 Active Directory RMS와 새 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p104">If you've already set up OME to work with Azure Rights Management for Exchange Online or Exchange Online Protection, depending on how you set it up, you may be ready to start using OME and its new capabilities right away. This article explains how to determine if you've set OME up correctly, what to do if you need to change your setup, and what happens if you choose not to change your setup. For example, in order to use the new capabilities, you must use Azure RMS with OME. You can't use the new capabilities with an on-premises Active Directory RMS.</span></span>
    
## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a><span data-ttu-id="a2d64-125">Office 365에서 OME의 이전 버전에 대 한 Azure 권한 관리 활성화</span><span class="sxs-lookup"><span data-stu-id="a2d64-125">Activate Azure Rights Management for  the previous version of OME in Office 365</span></span>
<span data-ttu-id="a2d64-126"><a name="activatewarm"> </a></span><span class="sxs-lookup"><span data-stu-id="a2d64-126"></span></span>

<span data-ttu-id="a2d64-p105">조직에서 사용자 정보 보호, 보내는 메시지에 적용 하 고 메시지와 Azure 권한 관리 서비스에 의해 보호 된 파일을 열 수 있도록 Azure 권한 관리를 활성화 해야 합니다. 자세한 내용은 [Azure 권한 관리 활성화](https://go.microsoft.com/fwlink/p/?LinkId=525775)를 참조 하십시오. 활성화를 완료 했으면, 여기를 반환 하 고이 문서의 작업을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p105">You need to activate Azure Rights Management so that the users in your organization can apply information protection to messages that they send, and open messages and files that have been protected by the Azure Rights Management service. For instructions, see [Activating Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Once you've completed the activation, return here and continue with the tasks in this article.</span></span>
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a><span data-ttu-id="a2d64-130">트러스트 된 게시 도메인 (TPDs)를 가져와서 Azure RMS를 사용 하 여 이전 버전의 OME 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-130">Set up the previous version of OME to use Azure RMS by importing trusted publishing domains (TPDs)</span></span>
<span data-ttu-id="a2d64-131"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="a2d64-131"></span></span>

<span data-ttu-id="a2d64-p106">TPD 조직의 권한 관리 설정에 대 한 정보를 포함 하는 XML 파일은입니다. 예, TPD 인증서 및 라이선스 서명 및 암호화에 사용 되는 서버 사용 허가자 인증서 (SLC)에 대 한 정보를 포함 하는 Url 라이선스 및 게시, 사용 하 고, 합니다. Windows PowerShell을 사용 하 여 Office 365 조직에 TPD를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p106">A TPD is an XML file that contains information about your organization's rights management settings. For example, the TPD contains information about the server licensor certificate (SLC) used for signing and encrypting certificates and licenses, the URLs used for licensing and publishing, and so on. You import the TPD into your Office 365 organization by using Windows PowerShell.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a2d64-p107">이전에 Office 365 조직에 Active Directory Rights Management 서비스 (AD RMS)에서 TPDs를 가져오는 하도록 선택할 수 있습니다. 그러나 이렇게 새 OME 기능을 사용 하 여 방지 하 고 권장 되지 않습니다. Office 365 조직은 현재이 방식으로 구성 하는 경우 Azure 정보 보호 클라우드 기반 온-프레미스 Active Directory RMS에서 마이그레이션하는 계획을 만드는 것이 좋습니다. 자세한 내용은 [Azure 정보 보호 AD RMS에서 마이그레이션](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)을 참조 하십시오. Azure 정보 보호 마이그레이션 완료 될 때까지 새 OME 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p107">Previously, you could choose to import TPDs from the Active Directory Rights Management service (AD RMS) into your Office 365 organization. However, doing so will prevent you from using the new OME capabilities and is not recommended. If your Office 365 organization is currently configured this way, Microsoft recommends that you create a plan to migrate from your on-premises Active Directory RMS to cloud-based Azure Information Protection. For more information, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). You will not be able to use the new OME capabilities until you have completed the migration to Azure Information Protection.</span></span> 
  
 <span data-ttu-id="a2d64-140">**Azure RMS에서 TPDs를 가져오려면**</span><span class="sxs-lookup"><span data-stu-id="a2d64-140">**To import TPDs from Azure RMS**</span></span>
  
1. <span data-ttu-id="a2d64-141">[원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-141">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="a2d64-142">Office 365 조직의 지리적 위치에 해당 하는 키 공유 URL을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-142">Choose the key-sharing URL that corresponds to your Office 365 organization's geographic location:</span></span>
    
|<span data-ttu-id="a2d64-143">**위치**</span><span class="sxs-lookup"><span data-stu-id="a2d64-143">**Location**</span></span>|<span data-ttu-id="a2d64-144">**위치 URL을 공유 하는 키**</span><span class="sxs-lookup"><span data-stu-id="a2d64-144">**Key sharing location URL**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2d64-145">북미</span><span class="sxs-lookup"><span data-stu-id="a2d64-145">North America</span></span>  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="a2d64-146">유럽 연합</span><span class="sxs-lookup"><span data-stu-id="a2d64-146">European Union</span></span>  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="a2d64-147">아시아</span><span class="sxs-lookup"><span data-stu-id="a2d64-147">Asia</span></span>  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="a2d64-148">남미</span><span class="sxs-lookup"><span data-stu-id="a2d64-148">South America</span></span>  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="a2d64-149">Office 365 Government(정부 커뮤니티 클라우드)</span><span class="sxs-lookup"><span data-stu-id="a2d64-149">Office 365 for Government (Government Community Cloud)</span></span>  <br/> <span data-ttu-id="a2d64-150">이 RMS 키 공유 위치는 Office 365 Government Sku 구입한 고객을 위해 예약 되어있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-150">This RMS key-sharing location is reserved for customers who have purchased Office 365 for Government SKUs.</span></span>  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. <span data-ttu-id="a2d64-151">다음과 같이 [Set-irmconfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet을 실행 하 여 키 공유 위치를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-151">Configure the key-sharing location by running the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet as follows:</span></span> 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    <span data-ttu-id="a2d64-152">예: 조직 북미에 있는 경우 위치를 공유 하는 키를 구성 하려면:</span><span class="sxs-lookup"><span data-stu-id="a2d64-152">For example, to configure the key sharing location if your organization is located in North America:</span></span>
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. <span data-ttu-id="a2d64-153">TPD를 가져오려면 Azure 권한 관리에서-RMSOnline 스위치와 함께 [Import-rmstrustedpublishingdomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-153">Run the [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet with the -RMSOnline switch to import the TPD from Azure Rights Management:</span></span> 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    <span data-ttu-id="a2d64-p108">TPD에 대 한 사용 하려는 *TPDName* 이름입니다. 예, "Contoso 북미 TPD" 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p108">Where  *TPDName*  is the name you want to use for the TPD. For example, "Contoso North American TPD".</span></span> 
    
5. <span data-ttu-id="a2d64-156">Azure 권한 관리 서비스를 사용 하 여 Office 365 조직을 성공적으로 구성 했는지를 확인 하려면-RMSOnline 스위치와 함께 [Test-irmconfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet을 다음과 같이 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-156">To verify that you successfully configured your Office 365 organization to use the Azure Rights Management service, run the [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet with the -RMSOnline switch as follows:</span></span> 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    <span data-ttu-id="a2d64-157">무엇 보다이 cmdlet Azure 권한 관리 서비스와의 연결을 확인, TPD를 다운로드 하 고의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-157">Among other things, this cmdlet checks connectivity with the Azure Rights Management service, downloads the TPD, and checks its validity.</span></span>
    
6. <span data-ttu-id="a2d64-158">웹 및 Outlook에서 Outlook에서 사용할 수 없도록 Azure 권한 관리 서식 파일을 사용 하지 않도록 설정 하려면 다음과 같이 [Set-irmconfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-158">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to disable Azure Rights Management templates from being available in Outlook on the web and Outlook:</span></span> 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. <span data-ttu-id="a2d64-159">클라우드 기반 전자 메일 조직에 대해 Azure 권한 관리를 사용 하도록 설정 하 고 Office 365 메시지 암호화에 대 한 Azure 권한 관리를 사용 하도록 구성 하려면 다음과 같이 [Set-irmconfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-159">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to enable Azure Rights Management for your cloud-based email organization and configure it to use Azure Rights Management for Office 365 Message Encryption:</span></span> 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. <span data-ttu-id="a2d64-p109">하면가 성공적으로 TPD를 가져오고 확인 Azure 권한 관리를 사용 하도록 설정, Azure 권한 관리 기능을 테스트 하려면 Test-irmconfiguration cmdlet을 사용 합니다. 자세한 내용은 [Test-irmconfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx)에서 "예 1"를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p109">To verify that you have successfully imported the TPD and enabled Azure Rights Management, use the Test-IRMConfiguration cmdlet to test Azure Rights Management functionality. For details, see "Example 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span></span>
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a><span data-ttu-id="a2d64-162">이전 버전의 Active Directory 권한 관리 하지 Azure 정보 보호를 사용 하 여 설정 하는 OME가 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="a2d64-162">I have the previous version of OME set up with Active Directory Rights Management not Azure Information Protection, what do I do?</span></span>
<span data-ttu-id="a2d64-163"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="a2d64-163"></span></span>

<span data-ttu-id="a2d64-p110">Active Directory 권한 관리를 사용 하면 기존 Office 365 메시지 암호화 메일 흐름 규칙을 사용 하 여 계속할 수 있지만 구성 하거나 새 OME 기능을 사용할 수 없습니다. 대신, Azure 정보 보호를 마이그레이션하려면 해야 합니다. 마이그레이션 및 조직에 대 한이 의미 하는 방법에 대 한 정보를 [AD RMS Azure 정보 보호에서 마이그레이션](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a2d64-p110">You can continue to use your existing Office 365 Message Encryption mail flow rules with Active Directory Rights Management, but you can't configure or use the new OME capabilities. Instead, you need to migrate to Azure Information Protection. For information about migration and what this means for your organization, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="a2d64-167">다음 단계</span><span class="sxs-lookup"><span data-stu-id="a2d64-167">Next steps</span></span>
<span data-ttu-id="a2d64-168"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="a2d64-168"></span></span>

<span data-ttu-id="a2d64-169">참조 하십시오 새 OME 기능을 사용 하도록 설정 하려는 경우에 Azure 권한 관리 설치를 완료 했으면 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정 합니다.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span><span class="sxs-lookup"><span data-stu-id="a2d64-169">Once you've completed Azure Rights Management setup, if you want to enable the new OME capabilities, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span></span>
  
<span data-ttu-id="a2d64-170">조직에서 새 OME 기능을 사용 하도록 설정한 [새 OME 기능을 갖춘 전자 메일 메시지를 보호 하기 위해 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)를 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a2d64-170">After you've set up your organization to use the new OME capabilities, you're ready to [Define mail flow rules to protect email messages with new OME capabilities](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="a2d64-171">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a2d64-171">Related topics</span></span>
<span data-ttu-id="a2d64-172"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="a2d64-172"></span></span>

[<span data-ttu-id="a2d64-173">Office 365의 암호화</span><span class="sxs-lookup"><span data-stu-id="a2d64-173">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="a2d64-174">Office 365의 암호화에 대한 기술 참조 세부 정보</span><span class="sxs-lookup"><span data-stu-id="a2d64-174">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="a2d64-175">Azure 권한 관리 이란?</span><span class="sxs-lookup"><span data-stu-id="a2d64-175">What is Azure Rights Management?</span></span>](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  

